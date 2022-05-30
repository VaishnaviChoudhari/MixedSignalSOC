# Mixed-signal RISC-V based SoC on FPGA

This workshop helps you get started with a basic mixed-signal FPGA flow, which can be extended to any complex SoC. For people who have done RISC-V based MYTH workshop, you will find this workshop as an extension to the 5th Day, where RISC-V pipe-lined CPU coded in TL-Verilog is now converted to Verilog language and is a part of a mixed-signal SoC. If you are from ASIC/Physical design background, this workshop will complement your existing work, and you would really get to know the similarities and differences between ASIC and FPGA flow, which one is preferred under what conditions and why is it preferred. This single workshop connects VLSI students, analog designers, FPGA designers and ASIC designers. It is also an attempt to bring everyone on the same platform, and serves as a starting point for design verification

[![risc-vMythWorkshopLOGO](https://osfpga.org/wp-content/uploads/2022/05/Cloud-based-RISC-V-on-FPGA-and-OpenFPGA-5.png)](https://osfpga.org/osfpga-training/)

## Brief Description of the Workshop
* Introduction to FPGA IPs
* Mixed Signals SOC details
* Mixed Signal FPGA Flow

# *Index*
***
* [Day 1: Lectures and Labs](#Day-1-Lectures-and-Labs)
  * [Introduction](#Introduction)
  * [RVMYTH RISC-V Core](#RVMYTH-RISC-V-Core)
  * [TL-Verilog](#TL-Verilog)
***

## Introduction

<p align="center" width="100%">
<img src="https://user-images.githubusercontent.com/68154219/171049431-a6517233-80bf-4d47-843c-d720cf321e19.png">
</p>

* This is a single SOC where we have Analog and Digital IP on a single chip.
* rvmyth is a digital IP
* Here we will go through two different flows, i.e, RTL flow and FPGA flow.
* For RTL flow, we will use gtkwave and iverilog tools and for FPGA flow we will use Xilinx toolchain for verifying the functionality.

## RVMYTH RISC-V Core

<p align="center" width="100%">
<img src="https://user-images.githubusercontent.com/68154219/171050424-91eb5c05-2b5b-4035-b0ac-4e37c035cb96.png">
</p>

For eg,
* In first stage, load will be fetch.
* In second stage, load will be decoded.
* Next is the execute stage where address calculation happens in the ALU
* Once address is calculated in ALU in memory stage, it is given to memory to fetch the data in that location.
* In the fifth stage which is write back stage, the data that is fetched is returned back to the register file.

## TL-Verilog

<p align="center" width="100%">
<img src="https://user-images.githubusercontent.com/68154219/171051403-eebe29de-7e36-4793-9fda-589d78d8d578.png">
</p>

TL-Verilog is flexible for example WARP-V which supports different ISAs, pipeline depth, etc.
