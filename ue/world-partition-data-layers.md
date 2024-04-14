# World Partition Data Layers

## Videos
- [World Partition And Data Layers](https://youtu.be/lkjlP0Y4zvc)

## What is Data Layers
This is a new feature that was built for World Partition system in UE 5+, to aid edit time and runtime streaming of the world.

## How to use
- Make sure that the map has world partition enabled.
- Open the Data Layer window, craete a new data layer, assign the data layer asset.
- Select actors and assign to the data layer.
- The data layer can be set to load & activate when the game starts or not. Make sure that these actors are **not** spatially loaded.
- A data layer can be child of another data layer. It may (?) inherit the `Is runtime` and `runtime initial state` from the parent data layer.
- To load/unload a data layer at runtime, use Data Layer subsystem, call Set Data layer runtime state. `In is recursive` affect how children data layer is handled.
