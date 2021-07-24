# Micro UCR Hash RTL

## Overview
This project consists of the RTL design of micro-hash-ucr, a nonce calculator that iterates over nonces to check if a hash output complies with a given target.

## Requirements
* Icarus Verilog, for simulation outputting
```
sudo apt install iverilog
```
* GTKWave Analyzer, to view simulation waves
```
sudo apt install gtkwave
```
* Qflow, for synthesis
```
sudo apt install qflow
```

## Installation
Clone repository with:
```
git clone github.com/leus8/micro-ucr-hash-rtl.git
```
Install:
```
make install
```
## Usage
### Simulate behavioral design and show wave output
Area oriented system:
```
make waves-area
```
Speed oriented system:
```
make waves-speed
```
Both systems
```
make waves
```
### Simulate behavioral and synthesized design and show wave output

> Synthesized design has to be generated by Qflow (Yosys) first.

Area oriented system:
```
make waves-synth-area
```
Speed oriented system:
```
make waves-synth-speed
```
Both systems
```
make waves-synth
```
### Run Qflow
#### Prep Qflow
```
make prep
```
#### Run all Qflow steps
```
make all-area
```
or
```
make all-speed
```
#### Run Qflow up until synthesis
```
make synth-area
```
or
```
make synth-speed
```
#### Run Qflow up until placement
```
make place-area
```
or
```
make place-speed
```
#### Run Qflow up until STA
```
make sta-area
```
or
```
make sta-speed
```
### Generate cell heatmap

> Run Qflow up until DRC

for both systems:
```
make heatmap-cell
```
for area system:
```
make heatmap-cell-area
```
for speed system:
```
make heatmap-cell-speed
```
### Clean workspace
```
make clean
```
