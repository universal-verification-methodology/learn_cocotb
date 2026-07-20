# Module 10 — Run a cocotb example

**Module id:** module10-offline-cocotb-example
**Lab:** none (offline · course Makefile)
**Tracks:** A only

## Slide 1 — Run a cocotb example

Browser sketches taught async tests, triggers, DUT handles, BinaryValue, scoreboards, and wave literacy. This module is Track A only: you open a real cocotb example with a simulator such as Verilator and run it on your machine. You leave with a command line you can repeat—activate the environment, make, run, and read pass or fail. No browser lab required here—just the live toolchain.

## Slide 2 — Why leave the browser

Sketches are concept literacy—they do not compile a DUT or exercise cocotb Makefiles. Offline runs force you through Python packages, simulator flags, MODULE and TOPLEVEL wiring, and the glue you will keep at work. The monorepo links the legacy learn-uvm-pyuvm tree for a small and-gate cocotb test you can run today. One clean pass is enough for this module; you can deepen pyuvm tests later on the next course.

## Slide 3 — Offline workflow

Here is the rhythm. Open the legacy course next to this curriculum. Activate its virtual environment so cocotb is on your path. Change into the module-one cocotb tests folder. Run make with Verilator as the simulator and the and-gate test selected. Watch compile finish, then the cocotb runner start. Capture the command and the pass or fail line in your notes. Other simulators swap the SIM knob—same idea, different Make recipe.

## Slide 4 — Real cocotb track practice

In the real cocotb track, change into the legacy offline course tree so your shell sits where the examples live. Activate the virtual environment—or prepend its bin folder to your path—so cocotb resolves. List the cocotb tests directory; you should see the Makefile and the and-gate test file. Then change into that folder and run make. SIM selects the simulator—here Verilator—and TEST names which cocotb module to run—here the and-gate test. Say the working directory aloud before make so you know where the build runs from.

```bash
# cd learn_uvm_pyuvm — enter the legacy offline course
cd courses/learn_uvm_pyuvm

# source .venv/bin/activate — put cocotb on PATH
source .venv/bin/activate

# ls module1/tests/cocotb_tests — find Makefile and test_and_gate.py
ls module1/tests/cocotb_tests

# make SIM=verilator TEST=test_and_gate — compile and run
cd module1/tests/cocotb_tests
make SIM=verilator TEST=test_and_gate
```

## Slide 5 — Pitfalls to watch

Without the virtual environment, system Python may lack cocotb—activate first, or fix PATH. Make must run from the test folder that owns the Makefile; the wrong directory fails quietly or builds nothing useful. A browser sketch pass is not a simulator pass—offline needs a real binary. The first Verilator plus cocotb compile can take a minute; later rebuilds are faster when objects exist. If Verilator is missing, install it or swap SIM to a simulator your site supports.

## Slide 6 — Your turn

Complete the offline checklist: locate a runnable example, build it, observe pass or fail, and note your simulator and package versions. Prefer module-one and-gate unless your site policy points elsewhere. When you are ready, take the short quiz, then continue to the wrap module that closes this cocotb path.
