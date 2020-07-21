# IrisNoiseGenerator
> A noise generator
```json
{
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
```

## zoom
> The coordinate input zoom

## opacity
> The output multiplier

## offsetX
> Coordinate offset x

## offsetY
> Height output offset y

## offsetZ
> Coordinate offset z

## seed
> The seed

## parametric
> Apply a parametric curve on the output

## bezier
> Apply a bezier curve on the output

## sinCentered
> Apply a sin-center curve on the output (0, and 1 = 0 and 0.5 = 1.0 using a sinoid shape.)

## exponent
> The exponent noise^EXPONENT

## enabled
> Enable / disable. Outputs offsetY if disabled

## irisBased
> If this generator uses the default iris swirly/wispy noise generator. Set to false for pure simplex.

## octaves
> Multiple octaves for multple generators of changing zooms added together

## fracture
> Apply a child noise generator to fracture the input coordinates of this generator

