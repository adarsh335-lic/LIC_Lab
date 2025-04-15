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
To calculate the difrrential gain
  - ADM = R2/R1 [1+2R5/RG]

     for RG = 10 ohm
     - ADM = 20K/10k [1+2(10k)/10]
     - ADM = 4002 v/v
    
   | RG(in ohm) | input voltage | theoritical Gain (ADM) | practical gain(ADM) |
  | --------------- | ----- | -------- | --------- | 
  | 10 | 3.37mV |	4002 | 4136.81	|   
  | 100 |	33.6mV |402 | 414.910 |  	
  | 1k | 321.mV | 42 | 43.36	|
  | 10k | 2.25V| 6 | 5.06855 |
  | 20k | 3.375V |  4 | 4.12851 |

  ### circuit diagram
![image](https://github.com/user-attachments/assets/962c1018-da3e-4c62-a63d-ad563fca0fdc)

### Output waveform

![image](https://github.com/user-attachments/assets/2a62db37-2bb0-4dce-9153-e86938637a5a)

### common mode gain 

#### circuit diagram

![image](https://github.com/user-attachments/assets/52534afb-5a62-4239-b241-6b44dc7729b7)

![image](https://github.com/user-attachments/assets/912c24c6-33a3-4bb6-86a8-bf009a5bb125)
TO calculate the CMRR = 20 log (ADM/ACM)
                 - CMRR = 20 log (4136.81/7.75)
                 - CMRR = 234.54
 | RG(in ohm) | input voltage | outputvoltage(V) | practical gain(ACM) | CMRR |
  | --------------- | ----- | -------- | --------- | --------- | 
  | 10 | 3.37mV |	26.12084pV | 7.75n	|  234.54 | 
  | 100 |	33.6mV | 261.08056p | 7.77n |  214.55 |	
  | 1k | 321.mV | 2.496038n | 7.766n	|  194.933 |
  | 10k | 2.25V| 17.47355n | 7.766n | 176.293 |
  | 20k | 3.375V |  26.210593n | 7.766n | 174.5178 |


## INFERENCE
- Instrumental amplifier is basically a diffrential amplifier having a high CMRR
- The sensors which converts the physical quantity to electrical quantity , when this electrical signal is directly pass input diffrenial there will be issue in impedence matching
- Adding the another amplifierat the input to increase the input impedence and lowers the output impedence
- Using the single variable resistor we can control the gain externally
- Stable and Accurate It keeps the signal steady over time and doesn't drift much with temperature, which is great for accurate, long-term measurements.




   


  
