# Simple_Voltage_Regulator
# TSP79333 Voltage Regulator Module

## Overview
This project implements a simple **3.3 V linear voltage regulator** using the **Texas Instruments TSP79333 LDO regulator**.

The circuit converts a **5 V input supply into a regulated 3.3 V output**, suitable for powering low-voltage digital electronics such as microcontrollers, sensors, or logic ICs.

The design follows the **typical application circuit described in Section 9.2 of the TSP79333 datasheet**, ensuring stable regulator operation and proper transient response.

---

## Design Goals

- Convert **5 V input → 3.3 V regulated output**
- Follow manufacturer-recommended stability guidelines
- Include a **status indicator LED**
- Keep the circuit simple enough for breadboard prototyping or PCB integration

---

## Circuit Architecture

The regulator stage consists of:

- **TSP79333 LDO regulator**
- **Input capacitor**
- **Output capacitor**
- **Bypass capacitor**
- **LED + resistor network** used as a power indicator


---

## Capacitor Selection

The capacitor values were selected according to **Section 9.2 – Typical Application** of the TSP79333 datasheet.

Recommended configuration:

| Component | Purpose |
|--------|--------|
| Input Capacitor | Stabilizes the regulator input
|Bypass Capacitor | Reduces supply noise 
| Output Capacitor | Ensures regulator loop stability and improves transient response 

Following the datasheet recommendations ensures the regulator remains stable across load conditions.

---

## LED Indicator Design

A surface-mount **0805 LED** was added to visually indicate when the regulator output is active.

The LED and resistor are connected **in series with the 3.3 V output rail**.

### Known Values

Output Voltage
Input Voltage
Current range 10mA - 200mA


### Final Resistor Values

| Resistor | Value | Purpose |
|--------|--------|--------|
| R1 | 650 Ω | Current limiting for LED |
| R2 | 280 Ω | Secondary resistor used in series configuration |

These resistors ensure the LED operates safely without drawing excessive current from the regulator output.

---

## Key Concepts Demonstrated

- Linear voltage regulator design
- Reading and implementing **datasheet typical application circuits**
- Component selection based on **electrical specifications**
- Applying **Ohm’s Law for current limiting**
- Basic **power rail indication circuits**

