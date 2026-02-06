# mdc-clock-module
Modular Detector Controller Clock Module

## Overview
Clock generator module with jitter cleaning. Takes a 10 MHz input and generates an ultra low jitter 100 MHz output with zero delay for the detector sequencer.
Provides up to three low-jitter synchronized clock outputs.

## Key ICs
- Jitter attenuator / clock multiplier: `SI5394J-A-GM`
  - DSPLL + MultiSynth architecture for ultra-low jitter clock generation.
  - Supports free-run, synchronous, and holdover modes with hitless switching between inputs.
  - Programmable via serial interface with on-chip NVM for power-up configuration.
  - A-grade devices use an external XTAL or XO reference.
- LDO: `TPS7A20`
  - Low-noise, high-PSRR LDO for clean supply rails to the timing IC.
  - Low IQ with good load/line transient performance for sensitive analog circuits.
