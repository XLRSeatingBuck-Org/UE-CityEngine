# 🌿 Unreal Engine Driving Simulation
A realistic driving simulation built with Procedural Content Generation in CityEngine and Unreal Engine 5. The driving simulator is connected to a G920 Logitech Steering Wheel featuring manual transmission mode. 

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
- Logitech G920 Steering Wheel and GHUB
- Logitech Gearshifter (optional)
- CityEngine (optional)

### Required Plugins

- **PCG** – for procedural content creation
- **Datasmith** – for importing CityEngine asset

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

1. Open the main map from `/Maps/Vehicle.umap`.
2. Click **Play** to test the simulation.

---

## 🔧 Maintenance Guidelines

- Keep Fab assets updated via Epic Launcher or manually re-import as needed.
- Use **Fix Up Redirectors** in the Content Browser to clean up asset links.
- Periodically review `/Content` to remove unused or redundant assets.
- Rebuild lighting and recompile shaders when importing new materials.

---

## 🧰 Troubleshooting

The driving simulator doesn't receive input from the steering wheel
* Open Project Settings/ Raw Inputs and Registry Editor in Windows to make sure the process id are matched
* Make sure GHUB Software is open and running in the background
* In the Settings for Windows, open the Setup USB Controller, find the Logitech Steering Wheel, here you can troubleshoot each button on the steering wheel as well as the gas, brake, and clutch pedals.



---

## 📬 Support

Questions or suggestions?  
Contact: **quetran.tran1009@gmail.com*  

---

## 📄 License

This project is licensed under the MIT License.  
**Note:** Fab assets are subject to Epic's Fab Marketplace Terms of Service and cannot be redistributed outside your project.


