# This folder

You are in a CAD project for [sfab-bench](https://bench.sfab.ai). cwd is
this directory. Visualization is a STEP or GLB here (`cad/block.step` is
the sample).

This workbench does not author CAD. To create or edit parts, use Jake's
CAD skill ([earthtojake/text-to-cad](https://github.com/earthtojake/text-to-cad)).
Install with `npx skills install earthtojake/text-to-cad` (or the Codex /
Claude Code plugin). Write new STEP under `cad/`. After a rebuild, tell
the user to open the file in the viewer (`show_artifact`).

Do not `git clone` into this folder. Do not treat the sfab-bench app
repo as this project.
