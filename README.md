# sfab-bench-starter

A CAD folder to open in [sfab-bench](https://bench.sfab.ai).

This app visualizes STEP and talks to it. It does not generate CAD.
Authoring is whatever you put in the folder. The path we use is
Jake's CAD skill ([earthtojake/text-to-cad](https://github.com/earthtojake/text-to-cad)).

## Start

1. Download [sfab-bench](https://github.com/sfab-oss/sfab-bench/releases) and open it.
2. Clone this repo (or **Use this template**):

```bash
git clone https://github.com/sfab-oss/sfab-bench-starter.git
```

3. In Bench: **Open folder** and pick the clone. Open `cad/block.step`.
4. To generate more parts, install the CAD skill, then ask in chat:

```bash
npx skills install earthtojake/text-to-cad
```

Codex (`codex plugin add cad@text-to-cad`) and Claude Code
(`claude plugin install cad@text-to-cad`) have plugin installs too.
Those CLIs must already be logged in on the Mac. Bench does not take
API keys for chat.

Already have STEP or GLB from Fusion or elsewhere? Skip this repo. Open
that folder instead.

Do not open the [sfab-bench](https://github.com/sfab-oss/sfab-bench) app
repo as a CAD project. It has no parts.
