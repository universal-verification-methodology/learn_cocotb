# learn_cocotb

[![GitHub](https://img.shields.io/badge/GitHub-learn__cocotb-181717?logo=github)](https://github.com/universal-verification-methodology/learn_cocotb)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-green?logo=creativecommons&logoColor=white)](LICENSE)
[![Role](https://img.shields.io/badge/role-course%20scaffold-orange)](https://github.com/universal-verification-methodology/learning)
[![Parent](https://img.shields.io/badge/parent-learning%20monorepo-0A9EDC)](https://github.com/universal-verification-methodology/learning)
[![Labs](https://img.shields.io/badge/labs-GitHub%20Pages-222?logo=githubpages)](https://universal-verification-methodology.github.io/learning/tools/)
[![Domain](https://img.shields.io/badge/domain-cocotb%20%7C%20Python%20TB-purple)](https://github.com/universal-verification-methodology/learn_cocotb)

**learn_cocotb** is the open learning path for *cocotb triggers → DUT handle → self-check (before pyuvm)*.

Authors rebuild slides/audio with **module-slides** in the parent monorepo.

## Table of contents

- [Contents](#contents)
- [Browse or clone](#browse-or-clone)
- [Author: module-slides](#author-module-slides)
- [Two learning tracks](#two-learning-tracks)
- [Module landings](#module-landings)
- [Browser labs](#browser-labs)
- [License](#license)

## Contents

```text
learn_cocotb/
├── README.md
├── LICENSE
├── docs/
│   ├── MODULES.md
│   └── TWO_TRACKS.md
├── scripts/
│   └── module.sh
├── module00-intro/
├── module01-python-async-tb/
├── module02-cocotb-triggers/
├── module03-cocotb-dut-handle/
├── module04-cocotb-uvm-map/
├── module05-self-check-tb/
├── module06-tb-clock-reset/
├── module07-waveform-lab/
├── module08-offline-cocotb-example/
└── module09-wrap/
```

## Browse or clone

- **Browser labs:** [https://universal-verification-methodology.github.io/learning/tools/](https://universal-verification-methodology.github.io/learning/tools/)
- **Syllabus:** [`syllabus.md` § learn_cocotb](https://github.com/universal-verification-methodology/learning/blob/main/syllabus.md#17-learn_cocotb)

```bash
git clone --recurse-submodules \
  git@github.com:universal-verification-methodology/learning.git
ls courses/learn_cocotb
./scripts/module.sh 01 --check
```

## Author: module-slides

```bash
cd ../..   # monorepo root
python .cursor/skills/module-slides/scripts/transcript_to_outline.py \
  courses/learn_cocotb/module01-python-async-tb
bash .cursor/skills/module-slides/scripts/narrate_clips.sh \
  courses/learn_cocotb/module01-python-async-tb
```

## Two learning tracks

Details: [docs/TWO_TRACKS.md](docs/TWO_TRACKS.md).

| Track | Practice surface | Start here |
|-------|------------------|------------|
| **A** | Real cocotb + simulator (Verilator / iverilog) | [docs/TWO_TRACKS.md](docs/TWO_TRACKS.md) |
| **B** | Browser cocotb / async TB sketches | [tools index](https://universal-verification-methodology.github.io/learning/tools/) |

## Module landings

Full status table: **[docs/MODULES.md](docs/MODULES.md)**.

| Module | Landing |
|--------|---------|
| 00 — Welcome to cocotb | [module00-intro](module00-intro/README.md) |
| 01 — Python async TB | [module01-python-async-tb](module01-python-async-tb/README.md) |
| 02 — cocotb triggers | [module02-cocotb-triggers](module02-cocotb-triggers/README.md) |
| 03 — cocotb DUT handle | [module03-cocotb-dut-handle](module03-cocotb-dut-handle/README.md) |
| 04 — cocotb ↔ UVM roles | [module04-cocotb-uvm-map](module04-cocotb-uvm-map/README.md) |
| 05 — Self-check pattern | [module05-self-check-tb](module05-self-check-tb/README.md) |
| 06 — Clock + reset in TB | [module06-tb-clock-reset](module06-tb-clock-reset/README.md) |
| 07 — Waves literacy | [module07-waveform-lab](module07-waveform-lab/README.md) |
| 08 — Run a cocotb example | [module08-offline-cocotb-example](module08-offline-cocotb-example/README.md) |
| 09 — cocotb complete | [module09-wrap](module09-wrap/README.md) |

## Browser labs

**Shipped:** [python-async-tb](https://universal-verification-methodology.github.io/learning/tools/python-async-tb/) · [cocotb-triggers](https://universal-verification-methodology.github.io/learning/tools/cocotb-triggers/) · [cocotb-dut-handle](https://universal-verification-methodology.github.io/learning/tools/cocotb-dut-handle/) · [cocotb-uvm-map](https://universal-verification-methodology.github.io/learning/tools/cocotb-uvm-map/) · [self-check-tb](https://universal-verification-methodology.github.io/learning/tools/self-check-tb/) · [tb-clock-reset](https://universal-verification-methodology.github.io/learning/tools/tb-clock-reset/) · [waveform-lab](https://universal-verification-methodology.github.io/learning/tools/waveform-lab/).

## License

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) — see [`LICENSE`](LICENSE).
