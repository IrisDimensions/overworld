# IrisPack
The pack for iris

# Flags
Flags are for .ifl files

## `raise <int>`
Raises the schematic by X blocks upon placement such as `raise 3`

## `sink <int>`
Lowers the schematic by X blocks upon placement such as `sink 5`

## `replace <find> <replace>,<replace>,<replace>...`
Replaces one block type with one or multiple other block types

```dockerfile
# Replace ALL types of stone with STONE:3
replace STONE STONE:3

# Replace ONLY Stone (normal) with STONE:3
replace STONE:0 STONE:3

# Replace GRASS with random blocks
replace GRASS DIRT,DIRT:1,DIRT:2
```

## `no snow`
Do Not apply snow filter if this object will be placed in a snowy biome (if it already has snow)

## `no lush`
Do Not apply lush filter (vines) if this object will be placed in a lush biome (if it's already lush af)

## `no rotation`
Do Not create rotation variants of this object (always place in the direction it was saved)

## `world chance <double>`
Add additional rarity with world chance. 50% is `world chance 0.5` Use this with world radius

## `world radius <int blocks>`
Set a rarity window (radius) for this schematic. Checks rarity once per radius and either allows or denies placement depending on the check

```dockerfile
# This object will place inside of 256x256 regions 50% of the time
world rarity 0.5
world radius 128
```

## `gravity`
Apply gravity to the base block of every column and pull the higher blocks down to the terrain height. Useful for land patches or walls. **NOT SUITABLE FOR OVERHANGS SUCH AS TREES**
> Moderate Performance Impact

## `maxslope <int>`

Computes the base of the schematic (ignores overhangs) and tries to apply on the base (say the roots of a tree) If the base requires shifting higher than the slope value, placement fails. **This does not affect how the object looks, it's just a fail condition**
> Moderate Performance Impact

## `hydrophilic`

Completley ignores the touching fluid check. This allows objects to be placed on top of water

## `submerged`

Treats water as air instead of the height of the terrain. Allows placement UNDER water on the sea-bed surface
