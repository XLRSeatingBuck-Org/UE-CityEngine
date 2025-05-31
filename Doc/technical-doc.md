

# Technical Workflow

This project integrates two primary data layers:

1. **Geospatial Data** from OpenStreetMap (OSM), including 2D boundaries and attribute data  
2. **3D Procedural Content** generated using CityEngine and Unreal Engine’s PCG (Procedural Content Generation) plugin

---

### 1. Procedural Modelling in CityEngine

CityEngine (by ArcGIS) specializes in generating urban environments. It offers both manual drawing tools and procedural generation tools and integrates with Blender, Unity, Unreal Engine, and web platforms.

It uses a rule-based scripting language called **CGA (Computer Generated Architecture)** to define how geometry is created and modified.

#### a) Importing 2D GIS Data

- **Shapes**: Represent buildings, land uses, parking zones, etc.
- **Graphs**: Represent roads and linear infrastructure like fences and powerlines.

#### b) Generating 3D Content with CGA

CGA rules perform operations like extrusion, subdivision, and texture mapping to transform 2D GIS data into detailed 3D models. Rule packages (`.rpk`) bundle the CGA rules with associated 3D assets and textures.

#### Suburban House Modelling

A typical suburban house is modeled with an L-shaped structure — a garage wing facing the street, connected by a driveway. Sidewalks, lawns, and pedestrian walkways are also generated.

#### Integrating Street Attributes

Instead of using building footprints from OSM, the CityEngine graph network subdivides lots from street shapes. Each lot is tagged with street-facing attributes, which helps determine the orientation of the house, driveway, and sidewalk.

#### Modifying Existing CGA Rule Files

**Street Modeling**:  
Street shape width is calculated using attributes such as number of lanes, cycle lanes, and parking. The [Complete Street Rule package](https://github.com/d-wasserman/Complete_Street_Rule) is applied for automation.

**Suburban Add-ons**:  
Additional CGA rule files are used to add features like solar panels, fences, and powerlines.

---

### 2. Procedural Content Generation in Unreal Engine

#### a) Importing CityEngine Models

CityEngine models are imported into Unreal using the Datasmith plugin. All attributes are preserved as **Asset User Data**, which Unreal can read and convert into **tags** for procedural content generation.

#### b) Creating PCG Graphs by Landscape Type

PCG Graphs are created for each environment type:

- `wood`
- `farmland`
- `grass`
- `meadow`
- `road`

#### c) PCG Workflow in Unreal Engine

Each PCG Graph follows these steps:

1. **Raycast**: Perform a World Ray Hit Query on landscape-tagged actors.
2. **Surface Sampling**: Sample points from hit surfaces using parameters such as looseness, point extents, and density.
3. **Point Projection**: Project points onto the terrain surface.
4. **Transformation**: Apply random offsets, scaling, and rotation to each point.
5. **Spawning Meshes**: Spawn static meshes based on the environment type at each point.

---

## Future Enhancements

- Increase randomness and variability in suburban house types.
- Add more diversity in farmland and grassland asset populations.
