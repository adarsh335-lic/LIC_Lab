# DIFFRENTIAL PAIR AMPLIFIER CIRCUIT
   QUESTION:
   - Design diffrential pair amplifier for the following spesifications Vdd=3.3V,p<=3mW,Vincm=1.72V,Vocm=1.81V,Vp=0.7V,perform DC analysis,transcient analysis,AC analysis and extract the required 
   parametrs

## CIRCUIT DIAGRAM:

![CKT](https://github.com/user-attachments/assets/ec518483-b0a0-4163-b628-21b4dde56f8f)

## Calculations:
![WhatsApp Image 2025-03-04 at 19 00 37_14850d0a](https://github.com/user-attachments/assets/ea831526-cf8d-48ed-9609-abcde37a6d7a)


## DC Analysis:

To perfectly bias the mosfet the main important thing is to properly bias the mosfet to make sure that is has to work in the saturation region,to maintain the ID as 0.45mA and Vds as 1.82V  the width must be 89.46um and length is 9um.

![wl](https://github.com/user-attachments/assets/e4a02964-756e-4bfd-8ac7-41dc5d3f12d3)

The DC operating points are as follows:

![Capture](https://github.com/user-attachments/assets/bd8f8c7a-0902-4aca-ba6b-b42d5ea46233)

## Transient Analysis:
the transient anlysis enble us to find out the input swing of the diffrential pair amplifier and also used to find out the gain of the diffrential pair amplifier 
   - Vincmmin = Vp + Vth
     - = 1.061V
   - Vincmmax = Vdd-IdRd + Vth
     - = 2.1715V
- Gain of the diffrential pair amplifier:
   - Av = (Vo1-Vo2)/Vin
     - =4.5 V/V 
The input and output wave form of the diffrential pair amplifier 

![in out](https://github.com/user-attachments/assets/86132609-e4a2-40a1-8560-01fcfb8f2e7d)

when Vin=Vincm_max

![Vdddd](https://github.com/user-attachments/assets/c542447a-9ffc-4f34-beb2-4a6d751171c3)

## AC analysis

Using  ac anlysis is we are finding out the bandwidth
- The Bandthwidth = 2.075M Hz

![Capture](https://github.com/user-attachments/assets/43b60445-072d-48f9-8c8f-15d9d2e768a4)

## Result 
      - To ain





  
