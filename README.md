# SDR-FM-Receiver-Project
---

## 📝 Project Overview
This project implements a **fully functional Wideband FM (WBFM)** receiver built from the ground up using **GNU Radio** and **RTL-SDR V4**. 

It serves not only for high-quality audio reception but also as a **diagnostic tool** to analyze hidden digital layers of commercial radio broadcasts, specifically the **RDS (Radio Data System)** subcarrier.

---

## 🚀 System Features

### 🎧 High-Fidelity FM Reception
* **Carrier Tuning:** Real-time frequency control to navigate the **88 MHz - 108 MHz** spectrum.
* **WBFM Demodulation:** Processing of wideband signals with proper quadrature demodulation.
* **Audio Optimization:** Implementation of a *Low Pass Filter* and *Audio Sink* with resampling to ensure a clear audio output.

### 🔍 RDS Data Exploration (Advanced Layer)
Beyond the audio, this program isolates the **57kHz carrier** inside the bandwidth of the radio station:
* **Spectrum Centering:** Utilizing the **Frequency Xlating FIR Filter** to extract digital data from the FM sidebands.
* **Signal Integrity:** Analysis of **BPSK modulation** and phase synchronization.

---

## 🛠 Hardware & Debugging
A major focus of this project was the **"real-world" behavior** of the **RTL-SDR V4**:

| Focus Area | Description |
| :--- | :--- |
| **Noise Floor** | Documenting how broadband interference impacts weak signals. |
| **Thermal Stability** | Analysis of heat-induced frequency drift in plastic-cased SDRs. |
| **Dynamic Range** | Balancing RF Gain vs. signal distortion (clipping). |

---

## 🖥️ How to Run

1.  **Connect** your RTL-SDR.
2.  **Open** `SDR_Radio_FM.grc` in GNU Radio Companion.
3.  **Execute** the flowgraph.
4.  **Tune:** Use the *Frequency Slider* to find a station and the *Filter Slider* to hunt for the RDS peak at **57kHz**.

> **Note:** The frequency slider is pre-configured to jump **200kHz** per click for standard station spacing.
