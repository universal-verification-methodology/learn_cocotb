# cocotb hello — and-gate (in-course for learn_cocotb module 10)
# Usage (from this directory):
#   pip install cocotb   # or activate your venv
#   make SIM=verilator TEST=test_and_gate

SIM ?= verilator
TOPLEVEL_LANG ?= verilog

TEST ?= test_and_gate
TOPLEVEL = and_gate
COCOTB_TEST_MODULES = $(TEST)

DUT_DIR := $(abspath ../dut)
VERILOG_SOURCES = $(DUT_DIR)/and_gate.v

COCOTB_REDUCED_LOG_FMT = 1

include $(shell cocotb-config --makefiles)/Makefile.sim
