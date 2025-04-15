# INSTRUMENTATION AMPLIFIER
### INTRODUCTION
  An instrumentation amplifier (or in-amp) is a type of differential amplifier designed to accurately amplify small differential signals in the presence of large common-mode voltages and noise. It is widely used in sensor signal conditioning, medical instrumentation, and data acquisition systems where precision and stability are critical.
  ### key features
  - High input impedance: Prevents loading of the signal source.

  - High common-mode rejection ratio (CMRR): Effectively rejects noise and interference common to both input lines.

  - Precise gain control: Gain can typically be adjusted with a single resistor.

  - Low output impedance: Good for driving loads or analog-to-digital converters (ADCs).

### Applictions
  - Biomedical signal amplification (e.g., ECG, EEG)

  - Strain gauge and bridge sensor measurements (e.g presure,force,weight)

  - Industrial process control systems (e.g emperature, flow, or pressure monitoring using transducers).

### Basic structure
  - Basic structure of a instrumental amplifier consists of 3 opamp
    
  - Where 2 are the buffer amplifier and another one is a diffrential amplifier.
    
  - By connecting the resistor across the buffer amplifier we can control the overall gain of the amplifier

  - ![image](https://github.com/user-attachments/assets/b0af7776-72ab-4a1f-a62b-aac56d33a12c)

## Design Question
Design an insturmental amplifier using 3 opamp configuration with following contraints
  - R1=R3=10k
  - R2=R4=20k
  - R5=R6=10k
  - VCC=15v
calculate ADM for RG=10, 100, 1k, 10k, 20k find ACM and calculate CMRR for each case sue LT spice simulator  

## Calculation

  - ADM = R2/R1 [1+2R5/RG]

     for RG = 10 ohm
     - ADM = 20K/10k [1+2(10k)/10]
     - ADM = 4002 v/v
  
