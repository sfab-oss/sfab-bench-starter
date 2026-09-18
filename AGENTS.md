# This folder

You are in a CAD project opened in [sfab-bench](https://bench.sfab.ai).
cwd is this directory.

Bench visualizes STEP and GLB. It does not generate CAD. Authoring is
the `cad` skill already in this folder. Showing work in the viewer is
the `sfab-bench` skill.

## How they work together

1. Read `.agents/skills/cad/SKILL.md` when the user wants a new or
   changed part. Keep the `.py` next to its STEP under `cad/` unless
   they ask for Jake's larger `src/` + `STEP/` layout.
2. Read `.agents/skills/sfab-bench/SKILL.md` when the part should appear
   in the workbench. After a rebuild, `show_artifact` with a
   project-relative path (`cad/foo.step`). `get_viewer` is what is on
   screen.
3. Sample: `cad/block.step`. Do not replace it unless asked.

Do not use Jake's `$cad-viewer`. Do not `git clone` into this folder.
Do not treat the sfab-bench app repo as this project.

cadgen (once per machine, only if authoring fails because it is
missing): `python -m pip install -r .agents/skills/cad/requirements.txt`
