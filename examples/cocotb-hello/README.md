# cocotb hello (and-gate)

In-course Track A example for `learn_cocotb` module **10** (offline).
Does **not** require the ignored legacy tree `learn_uvm_pyuvm`.

## Layout

```text
cocotb-hello/
├── README.md
├── dut/and_gate.v
└── tests/
    ├── Makefile
    └── test_and_gate.py
```

## Prerequisites

- Python 3.10+ with `cocotb` installed (`pip install cocotb` in a venv)
- Verilator (or another simulator cocotb supports) on `PATH`
- `make`

## Run

```bash
cd courses/learn_cocotb/examples/cocotb-hello/tests
# optional: source ../../../../.venv/bin/activate   # if you keep a monorepo venv
make SIM=verilator TEST=test_and_gate
```

`learn_pyuvm` learners can use the same tree via  
`courses/learn_cocotb/examples/cocotb-hello/` before deeper pyuvm offline work.
