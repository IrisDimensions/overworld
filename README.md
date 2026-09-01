# Overworld V4000
The standard overworld for [Iris the Dimension Engine](https://www.spigotmc.org/resources/iris-world-gen-the-dimension-engine.84586/). New and Improved!


Contributors & creators:
- [Astrash](https://github.com/Astrashh) (A lot of biomes, objects, generator configurations, caves, and v2 systems. His pack here: [Continents](https://github.com/Astrashh/Continents))
- [ArMiN231](https://github.com/Armin231) (Lots of updates for Loot, and Structure systems galore)
- [Brian](https://github.com/NextdoorPsycho) (Created the original (overworld) content in the pack. Most of the objects and biomes are of his making, and free to use for anyone who owns [Iris](https://www.spigotmc.org/resources/iris-world-gen-the-dimension-engine.84586/))
- [Coco](https://github.com/CocoTheOwner/) (Did much of the bugfixing, configuration tweaks, merges, early v2 development)
- [Cyberpwn](https://github.com/cyberpwnn) (Much of the early Bases and development of the iris plugin)
- [Espen](https://github.com/espen96) (Cave, Ore, and Other improvements)
- [K530](https://github.com/K530-hub) (Biome reworks, and mountain generation)
- [RaydenKonig](https://github.com/RaydenKonig) (Innovative ideas and configurations)
- [Repixelated](https://github.com/RePixelatedMC) (Major Overhaul to the Overworld and Significant Maintainer for Community packs and content)
- [Strangeone101](https://github.com/StrangeOne101) (Significant im[rovements to engine and Generator functions)


Great thanks to these people for contributing to the pack.
If you want to contribute as well, feel free to make a fork and pull requests.
Please contact us on Discord if you have some changes up for review!

## Pack publication

An unmarked commit at the head of `master` updates the mutable `beta` prerelease. If the full head commit message contains the literal, case-sensitive marker `V+`, beta publication is skipped and that exact commit is published as a stable release instead. The release tag is the positive integer `version` in `dimensions/overworld.json`, and the flat-root release asset is `overworld.zip`.

Stable version tags are immutable. Increment the dimension version before marking another commit with `V+`; publication fails if that version tag already belongs to a different commit. The `Publish V+ Pack Release` manual workflow defaults to a non-publishing dry run and also requires the selected commit to contain `V+`.

The unrestricted coal pass keeps the top terrain block intact, so it cannot replace grass. Coal remains eligible in exposed stone, including elevated and floating terrain, but its exposed-candidate survival is reduced by 30% while buried coal frequency remains unchanged.

Terrain-first hydrology uses independently budgeted surface, underground, and deep-fluid sources in 1,024-block planning tiles. Surface density is `1.75` with 384-block source spacing; underground density is `1.5` with 640-block spacing; deep lava density is `0.5` with 1,024-block spacing. Surface courses must start exposed, contain at least 128 blocks of exposed channel, and retain a continuous exposed reach; complete underground courses shorter than 384 blocks are discarded. Each tile publishes at most one outlet network with one complete surface main stem, avoiding manufactured tributary fans. When the initial outlet yields no valid surface course, a bounded ranked fallback tries up to eight alternative sources per requested course across alternate legal mouths and inland grottos without weakening terrain or ocean admission. Complete courses use 192-block primary meanders with restrained 48-block detail and whole-course terrain-aware smoothing. Water channels are five to ten blocks wide and one to three blocks deep, with a fixed two-block centerline inset, tapered spring headwaters, a broad thalweg, and 12-to-24-block dry terrain blending into organic banks. Every horizontal wet cell and cascade head is recessed below its exact natural terrain and all four cardinal neighbors; unsupported styled edges are omitted instead of becoming spill paths. Nearby elevation losses collapse into one transition and one compact receiver; exposed gradients use one-block steps, proven falls use fluid-only curtains, and cuts beyond the strict six-block open-channel limit or naturally submerged terrain enter a contained subterrain passage up to 384 blocks through rounded full-width portals before reopening. Policy multipliers may tighten that limit but cannot deepen it. Mouths flare and shallow into the exact coastline through an eight-block non-owning ocean apron; at-or-below-sea terrain receives no surface-river carving, fluid, shore, or grade. Underground routes connect to existing caves when containment succeeds, while coastal and inland grottos provide 10 blocks of dry headroom.

## Validate and package

Use Java 25 from a current Iris checkout for the same offline generation and bounded hydrology coverage gates used by publication:

```text
./gradlew --no-daemon :probe:genProbe \
  -PprobePack=/absolute/path/to/overworld \
  -PprobeDimension=overworld \
  -PprobeWarmupChunks=64 \
  -PprobeMeasuredChunks=256 \
  -PprobeStudio=true

./gradlew --no-daemon :probe:hydrologyPackProbe \
  -PprobePack=/absolute/path/to/overworld \
  -PprobeDimension=overworld \
  -PprobeSeeds=1,19,331,1337 \
  -PprobeMinimumTileX=8 \
  -PprobeMaximumTileX=23 \
  -PprobeMinimumTileZ=8 \
  -PprobeMaximumTileZ=23 \
  -PprobeRequiredCoverage=SURFACE_POOL@water,RIFFLE@water,CASCADE@water,WATERFALL@water,RIDGE_BORE@water,UNDERGROUND_POOL@water,UNDERGROUND_DROP@water,COASTAL_GROTTO@water,MOUTH@water,SINKHOLE@water,INLAND_GROTTO@water,DEEP_POOL@deep_lava \
  -PprobeStudio=true

./gradlew --no-daemon :probe:generationOrderProbe \
  -PprobePack=/absolute/path/to/overworld \
  -PprobeDimension=overworld \
  -PprobeSeed=77 \
  -PprobeMinimumChunkX=2048 \
  -PprobeMaximumChunkX=2051 \
  -PprobeMinimumChunkZ=2048 \
  -PprobeMaximumChunkZ=2051 \
  -PprobeParallelism=4 \
  -PprobeShuffleSeed=1337 \
  -PprobeMulticore=false \
  -PprobeStudio=true
```

The generation probe runs the canonical pack validator before creating its test engine. The hydrology probe scans 1,024 explicit seed-tile combinations and fails unless every required feature/profile selector is accepted. The generation-order probe requires identical block and biome output across forward, reverse, shuffled, and bounded-parallel generation. On a live Bukkit-family server, use `/iris pack validate pack=overworld` and `/iris pack package dimension=overworld obfuscate=false minify=true`.

Both publication workflows build a flat-root `overworld.zip` from the exact commit and extract that candidate archive. Nothing is published unless Java 25 validation and the focused Studio generation, hydrology coverage, and generation-order gates all pass against that archive.
