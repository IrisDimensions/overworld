# IrisRegion
> Represents an iris region
```json
{
    "shoreRatio": 0.13,
    "ridgeBiomes": [],
    "shoreHeightMin": 1.2,
    "shoreBiomes": [],
    "name": "A Region",
    "shoreHeightMax": 3.2,
    "spotBiomes": [],
    "landBiomes": [],
    "shoreHeightZoom": 3.14,
    "biomeImplosionRatio": 0.4,
    "seaBiomes": []
}
```

## name
> The name of the region

## shoreRatio
> The shore ration (How much percent of land should be a shore)

## shoreHeightMin
> The min shore height

## shoreHeightMax
> The the max shore height

## shoreHeightZoom
> The varience of the shore height

## biomeImplosionRatio
> The biome implosion ratio, how much to implode biomes into children (chance)

## landBiomes
> A list of root-level biomes in this region. Don't specify child biomes of other biomes here. Just the root parents.

## seaBiomes
> A list of root-level biomes in this region. Don't specify child biomes of other biomes here. Just the root parents.

## shoreBiomes
> A list of root-level biomes in this region. Don't specify child biomes of other biomes here. Just the root parents.

## ridgeBiomes
> Ridge biomes create a vein-like network like rivers through this region

## spotBiomes
> Spot biomes splotch themselves across this region like lakes

