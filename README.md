# Analog-Audio-Visualizer
Analog 3-band stereo spectrum analyzer that visualizes Bass, Mid, and Treble frequencies in real time using LED bar graphs.The entire system operates in the analog domain using op-amps, RC filters, and dedicated LED driver ICs. No microcontroller or digital processing is involved.

## Block Diagram
<img width="636" height="620" alt="Image" src="https://github.com/user-attachments/assets/4100a1f2-1d6c-4bb2-95a6-16209be7cf87" />

## Components
| Component | Part | Qty |
|---|---|---|
| Op-amp | LM358 | 2 |
| OTA (Auto gain) | LM13700 | 1–2 |
| LED driver | LM3915 | 6 |
| Rectifier diode | 1N4148 | 6 |
| LEDs — Bass | 5mm Red | 20 |
| LEDs — Mid | 5mm Green | 20 |
| LEDs — Treble | 5mm Blue | 20 |
| Resistors | Various | ~20 |
| Capacitors | Various | ~12 |
| Power supply | ±9V dual rail | 1 |

## Working
Input Buffer (LM358) — Buffers the audio signal to prevent source loading

RC Filter Bank — Passive RC networks split the signal into Bass, Mid, and Treble bands

Rectification (1N4148) — Diodes convert each band's AC signal into a DC envelope

Auto Gain Control (LM13700) — OTA dynamically adjusts gain to keep display active at all volume levels

LED Display (LM3915) — Logarithmic LED driver illuminates up to 10 LEDs per band on a dB scale

## Frequency
Cutoff frequency is calculaed by f = 1 / (2π × R × C)

## References
 
1. S. Shuvo et al., "Analog Signal Processing Based Hardware Implementation of Real-Time Audio Visualizer," 2020
2. P. Falkowski and A. Malcher, "Audio signal processing based on dynamically programmable analog arrays," *ICSES 2010*, Gliwice, Poland, pp. 29–32
3. S. Ray and P. R. Kinget, "Ultra-Low-Power and Compact-Area Analog Audio Feature Extraction Based on Time-Mode Analog Filterbank Interpolation and Time-Mode Analog Rectification," *IEEE Journal of Solid-State Circuits*, vol. 58
