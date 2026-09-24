# Integrator and Differentiator Using Op-Amp

## Aim

To design and set up an **integrator and differentiator circuit using an op-amp**.

## Apparatus Required

* Power Supply
* CRO
* Function Generator
* Breadboard
* Op-Amp
* Capacitor
* Resistors

---

## 1. Integrator

### Principle

An op-amp integrator performs the integration of the input waveform.

The output voltage is given by:

```text
Vo = -(1/RC) ∫ Vi dt + k
```

where **k** is the constant of integration and depends on the value of `Vo` at `t = 0`.

### Applications

Integrators are commonly used in:

* Analog computers
* Wave-shaping networks

### Design

The input frequency is taken as **1 kHz**.

For the integrator:

```text
C = 0.01 μF
R1 = 15.9 kΩ
```

A standard resistor value of:

```text
R1 = 15 kΩ
```

is used.

The feedback resistor is:

```text
R2 = 470 kΩ
```

The practical file states that R2 is provided to attenuate low-frequency signals, particularly input DC offset voltage, and is typically selected as 10 times R1 or more.

### Procedure

1. Set up the integrator circuit according to the circuit diagram.
2. Apply a rectangular wave of **±5 V (10 V peak-to-peak)** at **1 kHz**.
3. Observe the input and output simultaneously on the CRO.
4. Vary the DC offset of the square-wave input and observe the output waveform.
5. Repeat the experiment using triangular and sine-wave inputs.
6. Observe the corresponding output waveforms.

### Expected Waveform

For a square-wave input, the integrator produces a **triangular waveform** at the output.

---

## 2. Differentiator

### Principle

When the input resistor of an inverting amplifier is replaced by a capacitor, it forms an **inverting differentiator**.

The output voltage is proportional to the derivative of the input:

```text
Vo = -RF Ci (dVi/dt)
```

The gain of the differentiator increases with frequency, which can make the circuit unstable.

### Characteristics

* Acts as a **high-pass filter**.
* Can become unstable at high frequencies.
* May produce oscillations at high frequencies.
* Input impedance decreases as frequency increases.
* Therefore, it is susceptible to high-frequency noise.
* Additional circuit elements can reduce stability and noise problems.

### Design

For the differentiator:

```text
C = 0.01 μF
R = 15.9 kΩ
```

A standard resistor value of:

```text
R = 15 kΩ
```

is used.

### Procedure

1. Set up the differentiator circuit according to the circuit diagram.
2. Apply a rectangular wave of **±5 V (10 V peak-to-peak)** at **1 kHz**.
3. Observe the input and output simultaneously on the CRO.
4. Repeat the experiment using triangular and sine-wave inputs.
5. Observe the corresponding output waveforms.

### Expected Waveform

The differentiator produces **spike waveforms corresponding to changes in the input signal**.

---

## Comparison

| Feature               | Integrator        | Differentiator      |
| --------------------- | ----------------- | ------------------- |
| Main function         | Integration       | Differentiation     |
| Output relation       | Integral of input | Derivative of input |
| Basic action          | Accumulates input | Responds to changes |
| Square-wave input     | Triangular output | Spike output        |
| Filter characteristic | —                 | High-pass           |
| Op-Amp                | Used              | Used                |

## Components Used

| Component       | Value / Specification           |
| --------------- | ------------------------------- |
| Op-Amp          | LM 741                          |
| Capacitor       | 0.01 μF                         |
| Resistor R1     | 15 kΩ                           |
| Resistor R2     | 470 kΩ                          |
| Supply          | ±12 V                           |
| Input frequency | 1 kHz                           |
| Input waveform  | Rectangular / Triangular / Sine |

The practical circuit diagram identifies the op-amp as **LM 741** and shows a **±12 V supply**.

## Result

The op-amp **integrator and differentiator circuits** were successfully constructed and tested.

* The **integrator** produced a triangular waveform for a square-wave input.
* The **differentiator** produced spike waveforms corresponding to changes in the input signal.

## Conclusion

The practical operation of both the **op-amp integrator and differentiator** was successfully verified by observing their input and output waveforms using a CRO.
