
## Known Values

Regulated output voltage:

Vout = 3.3 V

LED forward voltage (from DigiKey datasheet):

Vf ≈ 2.0 V

Desired LED current:

I ≈ 2 mA = 0.002 A

---

## Voltage Across the Resistor

The resistor must drop the remaining voltage after the LED forward voltage.

Vr = Vout − Vf

Vr = 3.3 V − 2.0 V

Vr = 1.3 V

---

## Ohm's Law

To determine the resistor value, use Ohm’s Law:

R = V / I

Substitute the known values:

R = 1.3 V / 0.002 A

R ≈ 650 Ω

---

## Final Resistor Values

| Resistor | Value |
|--------|--------|
| R1 | 650 Ω |
| R2 | 280 Ω |

These resistors limit the LED current and prevent excessive current draw from the 3.3 V regulator output.

---
