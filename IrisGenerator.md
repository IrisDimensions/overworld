# IrisGenerator
> Represents a composite generator of noise gens
```json
{
    "offsetX": 0,
    "offsetZ": 0,
    "interpolationFunction": "BICUBIC",
    "seed": 1,
    "composite": [],
    "interpolationScale": 7,
    "zoom": 1,
    "cliffHeightMin": 0,
    "opacity": 1,
    "cliffHeightMax": 0,
    "cliffHeightGenerator": {
        "sinCentered": false,
        "seed": 0,
        "parametric": false,
        "zoom": 1,
        "enabled": true,
        "fracture": [],
        "offsetX": 0,
        "octaves": 1,
        "offsetZ": 0,
        "offsetY": 0,
        "irisBased": true,
        "opacity": 1,
        "bezier": false,
        "exponent": 1
    }
}
```

## zoom
> The zoom or frequency.

## opacity
> The opacity, essentially a multiplier on the output.

## offsetX
> The offset to shift this noise x

## offsetZ
> The offset to shift this noise z

## seed
> The seed for this generator

## interpolationFunction
> The interpolation method when two biomes use different heights but this same generator

## interpolationScale
> The interpolation distance scale (blocks) when two biomes use different heights but this same generator

## cliffHeightMax
> Cliff Height Max. Disable with 0 for min and max

## cliffHeightMin
> Cliff Height Min. Disable with 0 for min and max

## composite
> The list of noise gens this gen contains.

## cliffHeightGenerator
> The noise gen for cliff height.

