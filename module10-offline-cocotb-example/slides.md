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
- This course ships an in-course and-gate hello under examples/cocotb-hello
- One clean pass is enough for this module

---

## Offline workflow
- Here is the rhythm
- Open examples/cocotb-hello beside this curriculum
- Activate a virtual environment, or install cocotb with pip, so the Python package resolves
- Change into the tests folder that owns the Makefile
- Run make with Verilator as the simulator and the and-gate test selected
- Watch compile finish, then the cocotb runner start

---

## Real cocotb track practice
- In the real cocotb track
- Activate a virtual environment, or install cocotb, so the package resolves
- List the folder; you should see the Makefile and the and-gate test file
- Then run make
- SIM selects the simulator, here Verilator
- Say the working directory aloud before make so you know where the build runs from

---

## Real cocotb track practice — try these

```
cd courses/learn_cocotb/examples/cocotb-hello/tests
# optional: source a venv with cocotb installed
make SIM=verilator TEST=test_and_gate

```

---

## Pitfalls to watch
- Without cocotb on PATH
- Make must run from the tests folder that owns the Makefile
- A browser sketch pass is not a simulator pass, offline needs a real binary
- The first Verilator plus cocotb compile can take a minute

---

## Your turn
- Complete the offline checklist
- Prefer the in-course cocotb-hello unless your site policy points elsewhere
- When you are ready

