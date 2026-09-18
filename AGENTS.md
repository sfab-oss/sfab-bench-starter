# This folder

You are in a CAD project opened in [sfab-bench](https://bench.sfab.ai).
cwd is this directory.

Bench visualizes STEP and GLB. It does not generate CAD. Authoring is
the `cad` skill already in this folder (`.agents/skills/cad`).

## How they work together

1. Read `.agents/skills/cad/SKILL.md` when the user wants a new or
   changed part. Keep the `.py` next to its STEP under `cad/` unless
   they ask for Jake's larger `src/` + `STEP/` layout.
2. After a rebuild, `show_artifact` with a project-relative path
   (`cad/foo.step`). `get_viewer` is what is on screen. Those are Bench
   tools, not a second skill.
3. Sample: `cad/block.step`. Do not replace it unless asked.

Do not use Jake's `$cad-viewer`. Do not `git clone` into this folder.
Do not treat the sfab-bench app repo as this project.

cadgen (once per machine, only if authoring fails because it is
missing): `python -m pip install -r .agents/skills/cad/requirements.txt`
