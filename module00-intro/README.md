# Module 00: Welcome to cocotb

**Kind:** `intro`

← Start · [Course README](../README.md) · [Python async TB →](../module01-python-async-tb/README.md)

## What this course is

**learn_cocotb** — cocotb as a Python testbench — triggers, DUT handles, self-check — before pyuvm methodology.

| Track | Where you practice | Best for |
|-------|--------------------|----------|
| **A** | Real cocotb + simulator (Verilator / iverilog) | Muscle memory you keep |
| **B** | Browser cocotb / async TB sketches | Fast intuition |

Next after this course: **learn_pyuvm**, **learn_verification_planning_management**.

## Setup (Track A)

1. Install the local tools named in [docs/TWO_TRACKS.md](../docs/TWO_TRACKS.md).
2. Open this repo at `courses/learn_cocotb`.

## Setup (Track B)

1. Serve the platform: `python -m http.server 8080 --directory platform` (from monorepo root).
2. Open http://127.0.0.1:8080/tools/index.html
3. Live: [learning/tools](https://universal-verification-methodology.github.io/learning/tools/).

## How to move through modules

1. Read the module **README** (outcomes).
2. Pick Track A, Track B, or both.
3. Check off **CHECKLIST.md**.
4. Optional: expand `transcript.md` / `outline.yaml` with **module-slides** in the parent monorepo.

## Media

| Artifact | Path |
|----------|------|
| Transcript | [transcript.md](transcript.md) |
| Outline | [outline.yaml](outline.yaml) |
| Slides | [slides.pptx](slides.pptx) · [slides.pdf](slides.pdf) |
| Video | [video.mp4](video.mp4) |
| Quiz | [quiz.json](quiz.json) |

## Files

```
module00-intro/
├── README.md
├── CHECKLIST.md
├── EXAMPLES.md
├── outline.yaml
├── transcript.md
└── quiz.json
```

## Next

→ [Python async TB →](../module01-python-async-tb/README.md)
