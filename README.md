# Metastability Issue in VHDL Asynchronous Reset

This repository demonstrates a common error in VHDL code: incorrect handling of asynchronous resets.  The `bug.vhdl` file contains code that uses a synchronous reset, which is prone to metastability issues and can lead to unpredictable behavior.  The correct implementation, which uses an asynchronous reset, is shown in `bugSolution.vhdl`.

## Problem

Using a synchronous reset (as shown in `bug.vhdl`) with a fast clock can lead to metastability problems if the reset signal changes near the clock edge.  This can cause the output to become unpredictable or unstable.

## Solution

The solution (`bugSolution.vhdl`) demonstrates the correct way to handle an asynchronous reset using a separate process to handle the reset signal immediately, regardless of the clock.  This eliminates the metastability issue.