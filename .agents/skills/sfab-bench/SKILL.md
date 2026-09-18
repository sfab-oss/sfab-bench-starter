---
name: sfab-bench
description: >
  Show STEP or GLB in the sfab-bench workbench that has this folder open.
  Use after authoring or rebuilding a part, when the user asks to see CAD
  in Bench, Quest, or the viewer, or when calling get_viewer / show_artifact.
---

# sfab-bench (this folder)

This directory is a CAD project. The app is already running; do not start
`pnpm dev` or clone [sfab-bench](https://github.com/sfab-oss/sfab-bench).
Product home: https://bench.sfab.ai.

Authoring is the `cad` skill (`.agents/skills/cad`). This skill is only
the viewer. cadgen is the Python runtime that `$cad` pip-installs, not
a second skill.

## Together

1. User asks for a part → follow `cad`. Write the STEP (and its `.py`)
   under `cad/`.
2. After a successful rebuild, call `show_artifact` with the
   **project-relative** path (`cad/foo.step`).
3. Need what is on screen or selected → `get_viewer`. Paths in that
   JSON are project-relative.

Do not use Jake's `$cad-viewer`. This workbench is the viewer. Do not
`git clone` into this folder.

## Viewer tools

- `get_viewer` — `{ file, empty, selected, selectedName, tree, partCount }`.
- `show_artifact` — load a STEP or GLB that already exists in this
  folder, on **this client**. Re-call after overwriting the same STEP.

Sample already in the folder: `cad/block.step`.
