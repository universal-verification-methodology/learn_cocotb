---
marp: true
title: Run a cocotb example
paginate: true
---

# Run a cocotb example

Browser sketches taught async tests, triggers, DUT handles, BinaryValue, scoreboards, and wave literacy

---

## Why leave the browser
- Sketches are concept literacy, they do not compile a DUT or exercise cocotb Makefiles
- The glue you will keep at work
- The monorepo links the legacy learn-uvm-pyuvm tree for a small and-gate cocotb test you
- One clean pass is enough for this module

---

## Offline workflow
- Here is the rhythm
- Open the legacy course next to this curriculum
- Activate its virtual environment so cocotb is on your path
- Change into the module-one cocotb tests folder
- Run make with Verilator as the simulator and the and-gate test selected
- Watch compile finish, then the cocotb runner start

---

## Real cocotb track practice
- In the real cocotb track
- Activate the virtual environment
- List the cocotb tests directory; you should see the Makefile and the and-gate test file
- Then change into that folder and run make
- SIM selects the simulator, here Verilator
- Say the working directory aloud before make so you know where the build runs from

---

## Real cocotb track practice — try these

```
# cd learn_cocotb/examples/cocotb-hello — enter the legacy offline course
cd courses/learn_cocotb/examples/cocotb-hello

# source .venv/bin/activate  # or: pip install cocotb — put cocotb on PATH
source .venv/bin/activate  # or: pip install cocotb

# ls tests — find Makefile and test_and_gate.py
ls tests

# make SIM=verilator TEST=test_and_gate — compile and run
cd tests
make SIM=verilator TEST=test_and_gate

```

---

## Pitfalls to watch
- Without the virtual environment
- Make must run from the test folder that owns the Makefile
- A browser sketch pass is not a simulator pass, offline needs a real binary
- The first Verilator plus cocotb compile can take a minute
- If Verilator is missing, install it or swap SIM to a simulator your site supports

---

## Your turn
- Complete the offline checklist
- Prefer module-one and-gate unless your site policy points elsewhere
- When you are ready

