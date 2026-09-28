# Brain model: source and license

`brain.glb` is assembled by `scripts/assemble.mjs` from the per-region OBJ
meshes in `scripts/cns-src/` (gyri, lobes, limbic and deep structures, the full
brainstem, and cerebellum).

- Source repo: https://github.com/zlatnaspirala/anatomy-system
  (`systems/optimisation-157/Nervous/cns/*.obj`)
- Ultimate origin: BodyParts3D, copyright The Database Center for Life Science.
- License: Creative Commons Attribution-ShareAlike 2.1 Japan (CC BY-SA 2.1 JP),
  https://dbarchive.biosciencedbc.jp/en/bodyparts3d/lic.html

## What the license requires

- Use, including commercial use, is permitted under CC BY-SA 2.1 JP.
- You must give attribution: credit "BodyParts3D, copyright The Database Center
  for Life Science, licensed under CC BY-SA 2.1 JP" and link the license.
- Share-alike: derivatives of the model (such as `brain.glb`) must be released
  under the same or a compatible license.
- Indicate changes: the meshes were re-meshed, merged, renamed, and assembled
  into a single GLB.
- Surface this attribution in the shipped app (the Credits panel does this).

## Rebuild

`npm run build:brain` reads `scripts/cns-src/*.obj` and writes `brain.glb`.

The loader keys meshes to regions by name via `MESH_TO_REGION` in
`src/data/regions.ts`. To swap models, produce a GLB whose meshes are named to
match, or update that map.
