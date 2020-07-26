# IrisRegionRidge
> A ridge config
```json
{
    "as": "DEFER",
    "chance": 0.75,
    "thickness": 0.125,
    "scale": 5,
    "type": "LAND",
    "shuffle": 16,
    "chanceShuffle": 128,
    "chanceScale": 4
}
```

## biome
> The biome name

## type
> The type this biome should override (land sea or shore)

## as
> What type this spot is (i.e. target SEA but as LAND) like an island. Default matches the target type

## chance
> The chance this biome will be placed in a given spot

## scale
> The scale of the biome ridge. Higher values = wider veins & bigger connected cells

## chanceScale
> The chance scale (cell chances)

## shuffle
> The shuffle, how 'natural' this looks. Compared to pure polygons

## chanceShuffle
> The chance shuffle (polygon cell chances)

## thickness
> The thickness of the vein

