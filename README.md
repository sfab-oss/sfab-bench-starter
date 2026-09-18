# sfab-bench-starter

A CAD folder to open in [sfab-bench](https://bench.sfab.ai).

This app visualizes STEP and talks to it. It does not generate CAD.
This template already includes Jake's CAD skill
([earthtojake/text-to-cad](https://github.com/earthtojake/text-to-cad))
and a Bench skill so chat can author a part, write it under `cad/`,
then load it in the viewer. cadgen is the Python runtime `$cad` uses,
not a second skill.

## Start

1. Download [sfab-bench](https://github.com/sfab-oss/sfab-bench/releases) and open it.
2. Clone this repo (or **Use this template**):

```bash
git clone https://github.com/sfab-oss/sfab-bench-starter.git
```

3. In Bench: **Open folder** and pick the clone. Open `cad/block.step`.
4. Ask in chat for another part. The agent should use `cad`, then
   `show_artifact`.

Authoring needs [cadgen](https://github.com/earthtojake/text-to-cad) on
the Mac once:

```bash
python -m pip install -r .agents/skills/cad/requirements.txt
```

Already have STEP or GLB from Fusion or elsewhere? Skip this repo. Open
that folder instead.

Do not open the [sfab-bench](https://github.com/sfab-oss/sfab-bench) app
repo as a CAD project. It has no parts.

The `cad` skill is MIT, Copyright 2026 Thompson Labs LLC, vendored from
[earthtojake/text-to-cad](https://github.com/earthtojake/text-to-cad)
(see `.agents/skills/cad/LICENSE`).
