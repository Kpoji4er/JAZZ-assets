# Conrad: local JA3 integration

Installed entities: JAZZ_ConradBody, JAZZ_ConradPants, JAZZ_ConradHead.
Existing AppearancePreset Conrad references them; Jazz_Conrad UnitData unchanged.

- Conrad_Lowpoly_20k.glb: original Meshy remesh, task 01a0f978-66af-7428-b9f1-9aad96a18ef2.
- Conrad_Rigged.blend: editable rig with packed original textures, native Male skeleton and pose-review scene.
- front/back/three-quarter/pose.png: offline Blender renders, not game screenshots.
- rig-report.json and *-audit.json: structural and compiled HGM geometry/winding checks.
- install-manifest.json: installed runtime resource SHA256 values.
- Conrad-before.lua: previous appearance block for targeted rollback.

Rebuild with jazz/docs/tools/_build_conrad_character.py, passing this GLB, the local game root and a separate output directory. Then official AssetsProcessor, shared resource staging, HGM audit and _install_conrad_character.py. Installer refuses duplicate registration.

20,809 triangles; max four normalized weights; three shared 2K runtime maps plus 64px fallbacks. Original 4K textures stay packed in source.
Offline checks passed. Runtime/editor save-reload, material cache, weapon grip, walk/crouch/prone and gas-mask replacement are not verified. User chose to launch and inspect the game personally.
No commit or publication performed.
