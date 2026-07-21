# Makefile for in-course cocotb hello (cocotb 2.x)
# Usage (from this tests/ directory):
#   pip install cocotb   # or use a venv
#   make SIM=verilator TEST=test_and_gate

SIM ?= verilator
TOPLEVEL_LANG ?= verilog

TEST ?= test_and_gate
# DUT module name: test_and_gate → and_gate
TOPLEVEL = $(shell echo $(TEST) | sed 's/test_//')
COCOTB_TEST_MODULES = $(TEST)

DUT_DIR := $(abspath ../dut)
VERILOG_SOURCES = $(DUT_DIR)/$(TOPLEVEL).v

COCOTB_REDUCED_LOG_FMT = 1

include $(shell cocotb-config --makefiles)/Makefile.sim
