# Experiment 4 - Voltage Transfer Characteristics (VTC) of Resistive-load NMOS Inverter

##  Aim
To analyze the voltage transfer characteristics (VTC) of a resistive-load NMOS inverter and calculate:
- VOH
- VOL
- VIH
- VIL
- Vth

## Tools Required
- PC
- Cadence Tools (Virtuoso, ADE)

## Circuit Diagram
- Resistive-load NMOS inverter schematic as shown in the manual.

## Procedure

### 1. Schematic Design
- Open Cadence Virtuoso.
- Create a new library and schematic view for the inverter.
- Add components using the `i` key (Instance).
- Add pins for `vin` (input) and `vout` (output).
- Connect the components using `w` key (Wire).
- Use `Check and Save` to validate the design.

### 2. Simulation Setup
- Launch ADE L.
- Go to `Analyses → Choose`, select **DC analysis**.
- In `Outputs → To be plotted → Select on Schematic`, click on input and output nets.
- Run the simulation using `Simulation → Netlist and Run`.

##  Output
- DC Transfer Characteristics curve of the NMOS inverter.
- Determine VOH, VOL, VIH, VIL, and Vth from the curve.

##  Result
Voltage transfer characteristics were simulated successfully and key points (VOH, VOL, VIH, VIL, Vth) were identified from the plot.
