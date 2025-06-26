# Experiment 6 - Transient Response of CMOS Inverter

## im
To analyze the transient response of a CMOS inverter and calculate:
- Propagation Delay
- Rise Time
- Fall Time

##  Tools Required
- PC
- Cadence Tools (Virtuoso, ADE)
- gpdk180 PDK

##  Circuit Diagram
- Standard CMOS inverter schematic with PMOS and NMOS transistors.

## Procedure

### 1. Schematic Design
- Create a new library `myDesignLib` and attach `gpdk180` technology.
- Add PMOS (`W = wp`, `L = 180n`) and NMOS (`W = 2u`, `L = 180n`) transistors.
- Add pins `vin` (input) and `vout` (output).
- Connect using wire tool `w` and save schematic.
- Create symbol from schematic (`Create → Cellview → From Cellview`).

### 2. Testbench Design
- Instantiate inverter symbol in a new test schematic (`Inverter_Test`).
- Add:
  - `vpulse` for input (`v1 = 0V`, `v2 = 1.8V`, `tr = tf = 1ns`, `ton = 10ns`, `T = 20ns`)
  - `vdc` for VDD (`1.8V`)
  - `gnd`

### 3. Simulation Setup
- Launch ADE L.
- Set simulator to `Spectre`.
- Load model library `gpdk.scs`.
- Set transient analysis (`tran`) with stop time `200ns`.
- Select outputs `vin` and `vout` for plotting.
- Run the simulation.

### 4. Optional: Parametric Analysis
- Sweep PMOS width (`wp`) from `1u` to `10u` in 10 steps.
- Observe impact on transient response.

## Output
- Transient waveforms showing input and output.
- Propagation delay (tpd), rise time (tr), fall time (tf) are calculated.

##  Result
Transient behavior of CMOS inverter was simulated and timing parameters were extracted from waveform.
