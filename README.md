# Bevy Depth Peeling Demo

A demonstration of **depth peeling** in [Bevy](https://bevyengine.org/).

This demo shows how the technique can be applied in Bevy to render transmissive
materials with correct layering.

## How it is integrated into Bevy

The whole technique is packaged as a self-contained `DepthPeelingPlugin` that
plugs into Bevy's existing 3D render pipeline (`Core3d`) rather than replacing
it. 

In the demo, the glTF model's materials are swapped to the peeled variant once
the scene loads, and two extra procedural test scenes (intersecting
transmissive spheres and transmissive planes around a transparent cube) are
provided to show order-independent transparency in cases where naive sorting
would fail.

## Model Attributions

Robot model by <https://sketchfab.com/3d-models/vilhelm-13-low-res-textures-cb49a1f71ba54cad8e9dc09da8ef47cd>,
with the materials modified to be transmissive.
