# Module 00 — Welcome to cocotb

**Module id:** module00-intro
**Lab:** none (intro)
**Tracks:** A (real cocotb) · B (browser lab)

## Slide 1 — Welcome to cocotb

Python can drive your testbench while the simulator owns time and the DUT. This short clip welcomes you to learn cocotb—cocotb triggers, DUT handles, and self-check patterns before you grow into pyuvm methodology. You will see how the course is meant to be used, not every API on day one. Two practice tracks share the same ideas: a real cocotb shell and browser sketches.

## Slide 2 — Why cocotb

SystemVerilog testbenches are powerful, but many teams already live in Python for scripts, CI, and data. cocotb lets you write async Python coroutines that await simulator events—clock edges, timers, and more—while still talking to real RTL. This course builds literacy you can reuse with Verilator or Icarus, not a full commercial VIP flow in the browser.

## Slide 3 — Two tracks, one idea

Every lab module offers two ways to practice. The real cocotb track uses local Python with cocotb and a simulator such as Verilator, so installs, awaits, and Makefile runs feel like work you will keep. The browser lab track uses interactive sketches on the learning platform—async test shape, triggers, DUT handle, scoreboard, and waveform literacy—so you can build intuition without finishing every install first. You may do either track, or both.

## Slide 4 — Set up the real cocotb track

Install Python three, cocotb, and a free simulator—Verilator is a common choice. Open this course in the monorepo and skim the two-track doc for exact tool names. You do not need a perfect farm on day one; module ten is the dedicated offline run. For now, confirm you know where the examples prompts live in each module folder.

## Slide 5 — Set up the browser lab track

![Tools index on the platform](assets/tools-index.png)

From the monorepo, serve the platform folder with a simple local web server, then open the tools index in your browser. Look for the cocotb sketches—async testbench, triggers, DUT handle, scoreboard, and waveform lab—plus shared verification sketches you will reuse later. If you prefer, use the published tools site instead. Either way, open one sketch once so you know the layout: challenge panel, workspace, and Check.

## Slide 6 — How to move through modules

For each module, read the README for the outcome, pick a track—or both—then work the checklist and the short quiz when you are ready. Browser labs teach concepts; the real track keeps fidelity. When you finish this intro checklist, continue to the first lab: Python async testbench.
