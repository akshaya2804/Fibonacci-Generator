# Fibonacci-Generator

Overview

This project implements a Fibonacci sequence generator in Verilog. It includes a module (fib_rtl) that computes the Fibonacci sequence values and a corresponding testbench (fib_tb) to validate its functionality.

Key Components

fib_rtl Module:

This module generates Fibonacci numbers sequentially on each clock cycle.
It resets to the initial values of the Fibonacci sequence (0 and 1) when the rst signal is asserted.
The sequence is updated on every positive clock edge.

fib_tb Testbench:

A testbench to verify the functionality of the Fibonacci sequence generator.
It applies a clock signal, toggles the reset, and monitors the output sequence.

It Works

Fibonacci Calculation:

The Fibonacci sequence is generated using two registers: fib (current value) and fib_prev (previous value).
At each clock cycle:
The new Fibonacci value is calculated as the sum of fib and fib_prev.
The previous value is updated to the current value.

Reset Logic:

When the rst signal is asserted, the Fibonacci sequence is reset to 0 and 1.

Testbench Verification:

The testbench provides a clock signal that toggles every 5 time units.
It asserts the reset for the first 10 time units, then de-asserts it to allow the Fibonacci sequence to begin.
The $monitor task displays the Fibonacci output at each clock cycle.

Output
A sample simulation output:

fib = 0

fib = 1

fib = 1

fib = 2

fib = 3

fib = 5

fib = 8

fib = 13

fib = 21

fib = 34
