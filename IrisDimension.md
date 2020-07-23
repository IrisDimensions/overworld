# IrisDimension
> Represents a dimension
```json
{
    "redstoneMinDispersion": 0.17,
    "diamondMaxDispersion": 0.05,
    "emeraldMaxDispersion": 0.005,
    "seaZoom": 1,
    "biomeZoom": 5,
    "interpolationScale": 63,
    "focus": "",
    "goldMaxDispersion": 0.01,
    "redstoneMaxHeight": 15,
    "lapisMaxHeight": 33,
    "continentZoom": 1,
    "diamondMaxHeight": 16,
    "roughnessZoom": 2,
    "interpolationFunction": "BICUBIC",
    "coalMaxHeight": 100,
    "coalMinHeight": 5,
    "lapisMaxDispersion": 0.05,
    "coordFractureDistance": 20,
    "emeraldMinHeight": 5,
    "lapisMinHeight": 13,
    "caveThickness": 1,
    "caves": true,
    "placeObjects": true,
    "redstoneMinHeight": 5,
    "shoreZoom": 1,
    "redstoneMaxDispersion": 0.05,
    "diamondMinDispersion": 0.1,
    "roughnessHeight": 3,
    "name": "A Dimension",
    "regionZoom": 1,
    "caveScale": 1,
    "ironMinHeight": 5,
    "ironMaxHeight": 65,
    "landZoom": 1,
    "regions": [],
    "terrainZoom": 2,
    "coordFractureZoom": 8,
    "goldMinDispersion": 0.13,
    "emeraldMinDispersion": 0.07,
    "fluidHeight": 63,
    "emeraldMaxHeight": 16,
    "lapisMinDispersion": 0.12,
    "ores": true,
    "coalMinDispersion": 0.29,
    "diamondMinHeight": 5,
    "ironMaxDispersion": 0.02,
    "preventLeafDecay": false,
    "coalMaxDispersion": 0.02,
    "ironMinDispersion": 0.26,
    "caveShift": 0,
    "goldMaxHeight": 34,
    "environment": "NORMAL",
    "dimensionAngleDeg": 0,
    "goldMinHeight": 5
}
```

## name
> The human readable name of this dimension

## interpolationFunction
> The interpolation function for splicing noise maxes together

## interpolationScale
> The interpolation distance scale. Increase = more smooth, less detail

## environment
> The world environment

## regions
> Define all of the regions to include in this dimension. Dimensions -> Regions -> Biomes -> Objects etc

## fluidHeight
> The fluid height for this dimension

## focus
> Keep this either undefined or empty. Setting any biome name into this will force iris to only generate the specified biome. Great for testing.

## biomeZoom
> Zoom in or out the biome size. Higher = bigger biomes

## terrainZoom
> Zoom in or out the terrain. This stretches the terrain. Due to performance improvements, Higher than 2.0 may cause weird rounding artifacts. Lower = more terrain changes per block. Its a true zoom-out.

## dimensionAngleDeg
> You can rotate the input coordinates by an angle. This can make terrain appear more natural (less sharp corners and lines). This literally rotates the entire dimension by an angle. Hint: Try 12 degrees or something not on a 90 or 45 degree angle.

## roughnessZoom
> Iris adds a few roughness filters to noise. Increasing this smooths it out. Decreasing this makes it bumpier/scratchy

## roughnessHeight
> The height of the roughness filters

## coordFractureDistance
> Coordinate fracturing applies noise to the input coordinates. This creates the 'iris swirls' and wavy features. The distance pushes these waves further into places they shouldnt be. This is a block value multiplier.

## coordFractureZoom
> Coordinate fracturing zoom. Higher = less frequent warping, Lower = more frequent and rapid warping / swirls.

## landZoom
> This zooms in the land space

## shoreZoom
> This can zoom the shores

## seaZoom
> This zooms oceanic biomes

## continentZoom
> Zoom in continents

## regionZoom
> Change the size of regions

## placeObjects
> Disable this to stop placing schematics in biomes

## preventLeafDecay
> Prevent Leaf decay as if placed in creative mode

