# Procedural Map Generation Tool

This Unity project implements algorithms to generate procedural maps, primarily for use in game development. It provides a foundation for creating diverse and dynamic game environments through automated map generation.

## Table of Contents

* [Technologies Used](#technologies-used)
* [Features](#features)
* [Usage](#usage)
    * [Editor Usage](#editor-usage)
* [Technical Details](#technical-details)
* [Future Enhancements](#future-enhancements)
* [Project Structure](#project-structure)
* [Acknowledgments](#acknowledgments)

## Technologies Used

* Unity
* C#

## Features

* **Heightmap Generation:** Generates terrain heightmaps using Perlin Noise.
* **Mesh Generation:** Creates 3D terrain meshes from the generated heightmaps.

## Usage

### Editor Usage

* Open the project in the Unity Editor.
* The map generation can be configured and previewed within the editor scene.

## Technical Details

* The project utilizes C# scripts within the Unity environment.
* Terrain generation is based on Perlin Noise for heightmap generation.
* Mesh generation is achieved using Unity's `Mesh` class.

## Future Enhancements

* **Terrain Generation:** adding more types of terrain generation.
* **Natural World Generation:** adding biomes for a natural world enviorment. Adding rivers and oceans generation.
* **Texture Generation:** adding procedural texture generation based on terrain and biome generation.

## Project Structure

* **Scripts:**
  * `EndlessTerrain.cs`: Handles endless world generation using *chuncks* and *levels of details* for better performance.
  * `FalloffGenerator.cs`: Handles island generation using a Falloff generation algorithm.
  * `HideOnPlay.cs`: Sets the editor terrain mesh to invisible.
  * `MapDisplay.cs`: Handles map texture and mesh display.
  * `MapGenerator.cs`: Handles map generation.
  * `MeshGenerator.cs`: Handles mesh generation.
  * `Noise.cs`: Used for noise generation.
  * `TextureGenerator.cs`: Handles texture generation from height map.
* **Data:**
  * `UpdatableData.cs`: Parent class for updatable data.
  * `NoiseData.cs`: Noise data class used for editor. Inherit from `UpdatableData.cs`.
  * `TerrainData.cs`: Terrain data class used for editor. Inherit from `UpdatableData.cs`.
* **Editor:**
  * `MapGeneratorEditor.cs`: Custom editor for `MapGenerator.cs` class.
  * `UpdatableDataEditor.cs`: Custom editor for `UpdatableData.cs` class.
    
## Acknowledgments

* This project is based on [Sebastian Lague tutorial for Procedural Terrain Generation](#https://youtu.be/wbpMiKiSKm8?si=Cx-b50l9kZXuccSY).
