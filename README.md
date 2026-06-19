# Multi Axis Rotation

**Fixes purple/missing blocks from resource packs made for newer Minecraft versions**

Modern Blockbench exports block & item models that rotate cube elements on
**any angle and multiple axes at the same time** (`"rotation": { "x": .., "y": .., "z": .. }`).
That feature was added in snapshot **25w46a** (free single axis angles came in 1.21.6).

On **1.21.1** the model parser only accepts a **single axis** locked to
`-45 / -22.5 / 0 / 22.5 / 45`. Any model using the newer rotation is rejected and
renders as the missing texture block.

This client-side mod helps 1.21.1 to read those rotations.
## What it fixes
- Detailed trapdoors, buttons, fence gates, signs, props, decorations that use
  free / 3 axis element rotation.
- Both block models and held/inventory item models.

## Install
Client-side, **Fabric**.
1. Install [Fabric API](https://modrinth.com/mod/fabric-api).
2. Put the jar in `mods/`.
3. Launch and enable your resource pack.

## Compatibility
- Client only, not needed on servers.
- Renders through the vanilla bake step, so works with Sodium / Continuity / etc.

## Known limitations
- **UV lock** on arbitrarily-rotated faces follows vanilla's axis-aligned logic;
  textures on freely-rotated faces may not lock perfectly.
- **Rescale** ("inflate to fill") is applied for legal single axis rotations only;
  multi-axis elements use their authored geometry without rescale.
- Built for **1.21.1**. Other 1.21.x versions coming soon.

The pack used in the gallery images: [Backrooms Retextured](https://modrinth.com/resourcepack/backrooms-retextured)

## License
All Rights Reserved.
