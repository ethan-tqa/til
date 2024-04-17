# UE 5.4 Notable Changes

Presentation: [Unreal Engine 5.4 Sneak Peek](https://youtu.be/l8-k9bYsta0)

## Nanite Tessellation

There is a new `Enable Tessellation` checkbox on the material. Displacement can then be applied to make real geometry changes.

A cool trick is apply a scrolling normal map to fake cloth moving in the wind. Because it is real geometries, it can affect shadow as well. Another trick is deformable ground (snow, mud).

## Localized volumetric fog

The new actor `LocalFogVolume` is good for art directing environment.

## Heterogenous Volumes

Niagara volumentric simulation can now cast dynamic shadow, real time light & GI.

## Modular rigging

Control rig (CR) now has new features designed to work with bipedal/humanoid characters.

Tip: CR rigging can be done on a pre-production blocking mesh and then transferred to another mesh with similar skeleton structure.

Tip: For non-bipedal skeletons, `AddControl` & `Piston` can be used for building up general rig structures.

Tip: Check the video at 11 minute.

## Faster animation retargeting

The retarget aniimation tool now can auto-generate retarget mapping, able to recognize standard UE skeletons & some third-party skeletons. Then you can either batch export the animations or export the retargeter asset.

## Motion Matching

This feature picks animations and blending to fit the motion of the character, using a sparse set of motion animations.

This feature integrates with the Rewind Debugger, makes it easy to review animation selections and blending.

Tip: Epic will release a set of 500+ animations to go with this feature.

## Audio insights tool

This is a new tool that helps with debugging audio.
