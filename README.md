# 🌿 Unreal Engine Farming & Landscape Simulation

A modular and realistic farming simulation environment built in **Unreal Engine 5**, featuring **PCG (Procedural Content Generation)** and **Datasmith**, enhanced with high-fidelity assets from the Unreal Engine **Fab Library**.

---

## 📖 Project Overview and Purpose

This project aims to provide a customizable, high-quality farming and outdoor simulation environment ideal for:

- Game development prototyping
- Landscape visualization
- Environmental simulations

It combines procedural tools and curated Fab assets to allow scalable, dynamic world generation.

---

## 🛠️ Setup Instructions

### Prerequisites

- Unreal Engine 5.3 or later
- Windows 10/11 (64-bit)
- Epic Games Launcher
- ~100 GB available disk space

### Required Plugins

- **PCG** – for procedural content creation
- **Datasmith** – for importing design assets

Enable both via **Edit → Plugins** inside the Unreal Editor.

---

### 📥 Download and Import Fab Assets

You’ll need to manually download and import the following assets from **Fab**:

| Asset | Description | Link |
|-------|-------------|------|
| **Water Materials** | Realistic water shaders | [🔗 Download](https://www.fab.com/listings/063155ea-d9d2-4f29-b09f-33270b0bc861) |
| **Temperate Vegetation: Foliage** | Trees, shrubs, and natural foliage | [🔗 Download](https://www.fab.com/listings/6a5ae8db-d80f-4b23-b276-87da390cfe56) |
| **Ultimate Farming** | Farming tools, props, and scenery | [🔗 Download](https://www.fab.com/listings/b0041daf-350c-44b3-a23c-c58254f1d59d) |
| **Grass Landscape** | Grass-covered terrain materials | [🔗 Download](https://www.fab.com/listings/029abeaf-f109-4a66-9761-98ed53a511bb) |
| **Forest Landscape** | Large-scale forest terrain and textures | [🔗 Download](https://www.fab.com/listings/92c16f34-474e-4750-9ad2-a02b1aa9beb2) |

#### 🚀 How to Import:
1. Download each `.uasset` package from the links above via Fab.
2. Open your Unreal project.
3. Drag-and-drop or use **Import → Content Folder** to add the downloaded asset folders to:

---

## 🚀 Deployment Procedures

### Play in Editor

1. Open the main map from `/Maps/`.
2. Click **Play** to test the simulation.

### Package for Distribution

1. Go to **File → Package Project → Windows (64-bit)**
2. Choose a target directory
3. Wait for the build process to complete

---

## 🔧 Maintenance Guidelines

- Keep Fab assets updated via Epic Launcher or manually re-import as needed.
- Use **Fix Up Redirectors** in the Content Browser to clean up asset links.
- Periodically review `/Content` to remove unused or redundant assets.
- Rebuild lighting and recompile shaders when importing new materials.

---

## 🧰 Troubleshooting

| Problem | Solution |
|--------|----------|
| Missing materials or meshes | Ensure all Fab assets were imported to `/Content/FabAssets/` |
| PCG not generating properly | Recompile the graph and verify the plugin is active |
| Datasmith content fails to load | Re-enable the plugin and restart Unreal |
| Long shader compilation time | Clear derived data cache and verify GPU drivers |

---

## 👨‍💻 Contributing

1. Fork this repository
2. Create your feature branch (`git checkout -b feature-name`)
3. Commit your changes (`git commit -m "Add new feature"`)
4. Push to the branch (`git push origin feature-name`)
5. Open a Pull Request

---

## 📬 Support

Questions or suggestions?  
Contact: **your.email@example.com**  
Or open an issue on [GitHub Issues](https://github.com/your-username/farming-simulation/issues)

---

## 📄 License

This project is licensed under the MIT License.  
**Note:** Fab assets are subject to Epic's Fab Marketplace Terms of Service and cannot be redistributed outside your project.


Plugin :
PCG,
Datasmith

Unreal Engine Fab Library:
Water Materials: https://www.fab.com/listings/063155ea-d9d2-4f29-b09f-33270b0bc861 
temperate Vegetation: Foliage https://www.fab.com/listings/6a5ae8db-d80f-4b23-b276-87da390cfe56
Ultimate Farming: https://www.fab.com/listings/b0041daf-350c-44b3-a23c-c58254f1d59d
Grass Landscape: https://www.fab.com/listings/029abeaf-f109-4a66-9761-98ed53a511bb
Forest Landscape: https://www.fab.com/listings/92c16f34-474e-4750-9ad2-a02b1aa9beb2
