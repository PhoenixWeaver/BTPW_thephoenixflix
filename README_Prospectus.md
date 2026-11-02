# Ben Binh Tran — Ph.D. Prospectus Research

Research in antenna arrays, satellite communications, microwave material characterization, and radome-aware radar systems conducted at Brigham Young University.

> **Scope note:** This README summarizes the research described in the prospectus and its defense document. It distinguishes demonstrated work from proposed future research; it is not a claim that every proposal was completed.

## Research Overview

The work explored compact, high-efficiency antenna feeds and active phased-array systems for satellite communications, alongside methods for modeling and measuring low-loss materials at microwave frequencies. Related research examined circular polarization, reflector-aperture efficiency, and the effects of radomes on active arrays and monopulse tracking.

## Research Areas and Results

### Broadband Dielectric Resonator Antenna (DRA) Arrays

- Designed and optimized low-profile DRA array feeds for transmit/receive satellite communications, including Direct Broadcast Satellite applications.
- Used Physical Optics reflector modeling to evaluate aperture performance and signal-to-noise ratio (SNR).
- The defense reports aperture efficiency above 70% in a DBS-band configuration, radiation efficiency above 95% for that reported result, and SNR above 14.5 dB. It also describes a separate wideband model with radiation efficiency above 90% over 11–15 GHz.

![DRA array design and feed configuration from the prospectus defense](./images/Active%20Steerable%20Antenna%20Array.png)
*DRA array/feed design and operating-band objective (defense slide 5).*

![Measured bandwidth and port isolation for the DRA arrays](./images/Measured%20Bandwidth%20and%20Isolation%20Results.png)
*Measured S-parameters and isolation across the receive and transmit bands (defense slide 7).*

![Measured radiation and antenna efficiency across frequency](./images/Antenna%20Efficiency%20Results.png)
*Efficiency results and measurement note shown in the defense (slide 9); figures apply to the configuration and operating band shown.*

![Physical Optics reflector optimization results](./images/Physical%20Optics%20Optimization.png)
*Physical Optics results report port-specific aperture, spillover, radiation efficiency, and SNR values (defense slide 8).*

### Active Electronic Beam Steering

- Integrated the passive array feed with an active beamforming network using low-noise amplifiers (LNAs), variable-gain amplifiers (VGAs), and a power combiner.
- Demonstrated beam steering across a limited scan range of approximately ±2° to support satellite tracking and reflector misalignment compensation.

![Active electronically steerable antenna array](./images/Active%20Steerable%20Array.png)
*Active array and beam-steering test results (defense slide 11).*

### Dual Circular Polarization

- Designed a compact antenna supporting both right-hand and left-hand circular polarization (RHCP/LHCP), avoiding a separate hybrid feed network.
- The defense reports approximately 11 dB boresight directivity for each polarization and coverage angles exceeding ±45°.

![Dual RHCP and LHCP circular-polarization antenna](./images/Dual%20RHCP%20and%20LHCP%20Circular%20Polarization%20Antenna.png)
*Native dual-circular-polarization antenna concept (defense slide 14).*

### Microwave Material Characterization

- Developed a cylindrical cavity-resonator approach to characterize low-loss materials.
- Created a MATLAB curve-fitting method that maps measured S11 reflection data to an equivalent RLC circuit model.
- The defense reports measured quality factors of approximately 4,000–5,000 and describes a calibration-database method for estimating dielectric properties of a material under test.

![Cylindrical resonance cavity models for material characterization](./images/Resonance%20Cavity%20%E2%80%93%20Material%20Characterization.png)
*Single- and double-feed resonator configurations described in the defense (slide 17).*

### Radome and Monopulse Analysis

- Investigated how radomes can affect antenna patterns through beam deflection, attenuation, phase error, and sidelobe changes.
- Evaluated amplitude- and phase-comparison monopulse error vectors for a 2 × 2 active array; the defense describes the observed radome effect on those error vectors as small.
- A high-temperature radome/antenna integration and broader system evaluation were presented as future research, not as a completed deployment.

![Radome-enclosed active antenna array model](./images/Radome%20Enclosed%20Active%20Antenna%20Arrays.png)
*Radome/array model from the prospectus defense (slide 27).*

![Initial high-temperature radome and active-array model](./images/High%20Temperature%20Radome%20Enclosed%20Active%20Antenna%20Arrays.png)
*Initial high-temperature model illustrating a proposed research direction (defense slide 29), not a completed qualification test.*

## Methods and Tools

- Physical Optics modeling of reflector antennas and aperture efficiency
- Antenna-array design, beamforming, and scan evaluation
- MATLAB curve fitting and equivalent-circuit modeling
- Cavity-resonator measurement and material characterization
- RF device fabrication, testing, and performance validation
- Electromagnetic and thermal modeling concepts for radome systems

## Future Research Directions

The prospectus proposed the following extensions:

- Explore multimode reflector feeds and theoretical limits of aperture efficiency.
- Improve prediction of microwave material losses at elevated temperatures.
- Study high-temperature radome effects on active-array performance.
- Extend phase-comparison monopulse tracking analysis to radome-enclosed arrays.

These are research directions from the prospectus and should not be read as completed outcomes unless separately documented.

## Publications Listed in the Defense

- Binh T. Tran and Karl F. Warnick, “Broadband, High Efficiency Dielectric Resonator Antenna for Satellite Communications,” IEEE APS-URSI Symposium, Boulder, Colorado, 2013. Listed as accepted in the defense document.
- Binh T. Tran and Karl F. Warnick, “High Efficiency Dielectric Resonator Antenna Array Feeds for Satellite Communications,” IEEE Transactions on Antennas and Propagation. Listed as under review at the time of the 2013 defense.

## Source Documents

- [RF & Microwave Prospectus notes](./RFandMW_Prospectus.md)

## Interpreting Performance Figures

The source notes and defense describe multiple antenna versions, models, and test conditions. Their reported efficiency and SNR figures are configuration-specific; compare each value with its associated design and measurement/model conditions rather than treating all values as results from one antenna.
