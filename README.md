# SDR-FM-Receiver-Project

Project Overview

  This project implements a fully funtional Wideband FM (WBFM) built from the ground up using GNU Radio and RTL-SDR V4. This project is not only for high-quality audio reception but also as a diagnostic
  tool to diagnostic hidden digital layers of comercial radio broadcast, specifically the RDS (Radio Data System) subcarrier.

System features

  High-Fidelity FM - Reception 
  
  Carrier Tuning: Real - time frequency control to navigate between 88 MHz - 108 Mhz spectrum.
  
  WMBM Demodulation: Processing of widebands signal with proper quadrature demodulation.
  
  Audio optimization: Implementation of a Low pass filter and Audio sink with resampling to ensure to clear the audio output.

RDS Data Exploration (Advanced layer)

  Beyond the layer this programm isolates the 57kHz carrier inside the bandwidth of one radio station.
  
  Spectrum centering: Using the "Frequency Xlating Fir Filter" to pull digital data from the FM sidevbands
  
  Signal Integrity: Analysis of BPSK modulation and phase synchronization.

Hardware and debugging

  A major focus of this project was the "real world" behavior of the RTL SDR-V4
  
  Noise Floor and sensibility: Documenting how the noise floor (broadband interference) impacts weak signals.
  
  Thermal stabiliy: Analysis of how heat affects frequency presicion in plastic-cased SDRs.
  
  Dynamic Range: Finding the balance between RF Gain and signal distortion (clipping).

How to run.

1- conect your sdr.

2- open "SDR_Radio_FM.grc" in GNU Radio companion.

3- Execute the flowgraph.

4- Use the frequency slider to find your favorite station and the Filter Slider to hunt for the RDS peak at 57kHz.

Note: The frequency slider is already pre-configurated to tune radio station jumping 200Khz for each click.
