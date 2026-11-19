# Antenna Design Calculations – 144 MHz Dipole

## 1. Design Specifications

The antenna is designed for operation at 144 MHz, within the 2-metre amateur radio band.

| Parameter | Specification |
|---|---:|
| Antenna type | Half-wave dipole |
| Operating frequency | 144 MHz |
| Speed of light | 3 × 10⁸ m/s |
| Number of radiating arms | 2 |
| Polarization | Determined by antenna orientation |
| Design approach | Analytical calculation followed by HFSS simulation |

## 2. Wavelength Calculation

The free-space wavelength is calculated using:

\[
\lambda = \frac{c}{f}
\]

Where:

- \(c\) = Speed of light = \(3 \times 10^8\) m/s
- \(f\) = Operating frequency = \(144 \times 10^6\) Hz

Substituting:

\[
\lambda = \frac{3 \times 10^8}{144 \times 10^6}
\]

\[
\boxed{\lambda = 2.0833\ m}
\]

Therefore, the free-space wavelength at 144 MHz is approximately 2.0833 metres.

## 3. Theoretical Half-Wavelength Dipole Length

A half-wave dipole has a theoretical total length of:

\[
L_{\text{total}} = \frac{\lambda}{2}
\]

\[
L_{\text{total}} = \frac{2.0833}{2}
\]

\[
\boxed{L_{\text{total}} = 1.0417\ m}
\]

## 4. Practical Dipole Length

In practical antenna construction, the physical length is generally shorter than the theoretical half-wavelength due to end effects.

A commonly used approximate formula for a practical half-wave dipole is:

\[
L_{\text{total}} = \frac{143}{f_{\text{MHz}}}
\]

For 144 MHz:

\[
L_{\text{total}} = \frac{143}{144}
\]

\[
\boxed{L_{\text{total}} = 0.9931\ m}
\]

This provides an initial practical design estimate. The final resonant length depends on conductor diameter, feed gap, materials and installation conditions.

## 5. Individual Arm Length Calculation

A centre-fed dipole consists of two approximately equal-length arms.

\[
L_{\text{arm}} = \frac{L_{\text{total}}}{2}
\]

\[
L_{\text{arm}} = \frac{0.9931}{2}
\]

\[
\boxed{L_{\text{arm}} = 0.4965\ m}
\]

Therefore, the initial estimated dimensions are:

| Component | Length |
|---|---:|
| First arm | 49.65 cm |
| Second arm | 49.65 cm |
| Total conductor length | 99.31 cm |

The feed gap is treated separately and must be accounted for when defining the actual HFSS geometry.

## 6. Design Calculation Summary

| Parameter | Calculated Value |
|---|---:|
| Operating frequency | 144 MHz |
| Free-space wavelength | 2.0833 m |
| Theoretical half-wave length | 1.0417 m |
| Practical estimated total length | 0.9931 m |
| Estimated individual arm length | 0.4965 m |

## 7. HFSS Design and Optimization

The calculated dimensions provide an initial geometry for electromagnetic modeling in Ansys HFSS.

The antenna geometry can subsequently be optimized through simulation by adjusting:

- Individual dipole arm lengths
- Conductor diameter
- Feed-point gap
- Feeding arrangement

The objective is to obtain resonance close to 144 MHz with suitable impedance matching.

## 8. Design Note

The calculated arm lengths are theoretical starting estimates and should not be interpreted as confirmed fabricated dimensions.

The final dimensions should be established from the actual HFSS model and verified against the fabricated antenna.

The simulated and measured responses should be compared at identical frequencies and under appropriate measurement conditions.

---

**Design Frequency:** 144 MHz

**Antenna Type:** Half-Wave Dipole

**Simulation Software:** Ansys HFSS
