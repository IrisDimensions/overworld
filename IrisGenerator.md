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
    "opacity": 1
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

## composite
> The list of noise gens this gen contains.

