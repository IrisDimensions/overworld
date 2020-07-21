# IrisDimension
> Represents a dimension
```json
{
    "landZoom": 1,
    "regions": [],
    "caveThickness": 1,
    "seaZoom": 1,
    "caves": true,
    "biomeZoom": 5,
    "interpolationScale": 63,
    "focus": "",
    "placeObjects": true,
    "shoreZoom": 1,
    "continentZoom": 1,
    "caveShift": 0,
    "roughnessZoom": 2,
    "interpolationFunction": "BICUBIC",
    "environment": "NORMAL",
    "terrainZoom": 2,
    "roughnessHeight": 3,
    "coordFractureZoom": 8,
    "name": "A Dimension",
    "fluidHeight": 63,
    "dimensionAngleDeg": 0,
    "regionZoom": 1,
    "coordFractureDistance": 20,
    "caveScale": 1
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

