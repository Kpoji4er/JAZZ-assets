# Meshy 6B3

Editable inputs: `meshy-20261002/clean/JazzArmor_6B3.blend` and final rig `meshy-20261002-torso-shoulders/source/6B3.blend`. The final rig uses torso-only shoulders, 14802 triangles, normalized skin with at most four influences.

Build with jazz/docs/tools/_build_legion_armor.py, entity JAZZ_6B3_Male, mesh-prefix TEST_6B3, texture-size 2048; run the official AssetsProcessor, staging and compiled audit. Preserve current DDS for skin-only updates. See jazz/docs/tools/README.md and JAZZ-APPEAR-001.

Five synthetic poses passed, isolated arms displacement 0; compiled geometry error 0.09247 mm. Installed locally with backup and hash validation. In-game shoulder acceptance remains pending. Generated builds, screenshots and rollback copies remain local; they are not source inputs.
