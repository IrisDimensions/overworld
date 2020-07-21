# IrisBiomeDecorator
> A biome decorator is used for placing flowers, grass, cacti and so on
```json
{
    "verticalZoom": 1,
    "chance": 0.1,
    "variance": "SCATTER",
    "verticalVariance": "SCATTER",
    "stackMax": 1,
    "zoom": 1,
    "palette": ["GRASS"],
    "dispersion": "SCATTER",
    "stackMin": 1
}
```

## variance
> The varience dispersion is used when multiple blocks are put in the palette. Scatter scrambles them, Wispy shows streak-looking varience

## dispersion
> Dispersion is used to pick places to spawn. Scatter randomly places them (vanilla) or Wispy for a streak like patch system.

## verticalVariance
> If this decorator has a height more than 1 this changes how it picks the height between your maxes. Scatter = random, Wispy = wavy heights

## stackMin
> The minimum repeat stack height (setting to 3 would stack 3 of <block> on top of each other

## stackMax
> The maximum repeat stack height

## zoom
> The zoom is for zooming in or out wispy dispersions. Makes patches bigger the higher this zoom value is/

## verticalZoom
> The vertical zoom is for wispy stack heights. Zooming this in makes stack heights more slowly change over a distance

## chance
> The chance for this decorator to decorate at a given X,Y coordinate. This is hit 256 times per chunk (per surface block)

## palette
> The palette of blocks to pick from when this decorator needs to place.

