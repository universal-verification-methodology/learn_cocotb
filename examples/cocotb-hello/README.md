# cocotb hello (and-gate)

In-course Track A example for **learn_cocotb** module 10. Prefer this over the ignored `learn_uvm_pyuvm` archive.

## Run

```bash
cd courses/learn_cocotb/examples/cocotb-hello/tests
python -m venv ../../.venv && source ../../.venv/bin/activate   # first time
pip install cocotb
make SIM=verilator TEST=test_and_gate
```

Requires Verilator on `PATH`. DUT is `../dut/and_gate.v`.

**learn_pyuvm** learners can reuse this tree for a first cocotb smoke before pyuvm examples.
