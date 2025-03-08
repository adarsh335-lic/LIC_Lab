# DIFFRENTIAL PAIR AMPLIFIER CIRCUIT
   QUESTION:
   - Design diffrential pair amplifier for the following spesifications Vdd=3.3V,p<=3mW,Vincm=1.72V,Vocm=1.81V,Vp=0.7V,perform DC analysis,transcient analysis,AC analysis and extract the required 
   parametrs

## CIRCUIT DIAGRAM:

![CKT](https://github.com/user-attachments/assets/ec518483-b0a0-4163-b628-21b4dde56f8f)
**Behavior**:
   - The tail current is not constant and depends on the common-mode voltage.
   - Less effective at rejecting common-mode noise.
   - Large resistors are required for proper biasing, which may take up a lot of chip area.
   - Gain is Lower because a resistor has a lower output resistance than an active current source
   - Bandwidth is	Higher due to lower output resistance, leading to a higher dominant pole frequency
   - Input Common Mode Swing	is Lower because the tail resistor limits the range over which the circuit remains properly biased.
   

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
**The Bandthwidth**  = 2.075M Hz

![Capture](https://github.com/user-attachments/assets/43b60445-072d-48f9-8c8f-15d9d2e768a4)

## Circuit 2
**Using the current source at the tail**

**circuit diagram**
![Capture](https://github.com/user-attachments/assets/0bf7396e-ac55-47ec-b624-2032b2a413eb)

**Behavior:**
   - Provides a constant tail current, independent of common-mode variations
   - Ensures better biasing stability and common-mode rejection
   - Increases the effective differential-mode gain
   - when we use the current source instead of resistor at the tail gain is Higher due to increased output resistance at the tail
   - Bandwidth is	Lower than resistive load due to increased resistance at the tail, creating a dominant pole at a lower frequency.
   - Input Common Mode Swing is	Higher, since the current source keeps the tail current relatively constant over a wider range of common-mode input voltages.
## Transient analysis
![image](https://github.com/user-attachments/assets/9f9f423e-d0aa-486e-b2b1-820ed0ebea70)
## Ac analysis
![image](https://github.com/user-attachments/assets/2889e501-5757-46b6-b22a-cfc81fb3dede)

## circuit 3
**using of mosfet instead of current source**
when we use the mosfet at the tail we require to maintain the proper biasing for the tail mosfet also other wise it will effect the current of the diffrential mosfets,hence the VG value of the tail mosfet is given by,
           **VB=Vp+Vth**
**Behaviour**
   - Acts as a non-ideal current source with some dependence on VCM.
   - Can be designed to have high resistance, but not as ideal as a true current source.
   - More compact than using a large resistor.
   - Gain is Moderate, lower than an ideal current source but better than a resistive tail.
   - Bandwidth is	Better than current source, but worse than resistive tail because the MOSFET tail adds capacitance, slightly reducing bandwidth
   - Input Common Mode Swing	Lower than a current source, since the MOSFET tail does not fully reject common-mode variations

**circuit diagram**
![image](https://github.com/user-attachments/assets/93477b97-217d-46ca-bf44-488ddd48fc69)

## Transient analysis
![image](https://github.com/user-attachments/assets/949986c2-967e-42c2-abfa-46ff614bc884)

## Result 
- To proper bias the mosfet the width must be 89.46um and length is 9um.
- The input dynamic voltage range is  1.061V<Vin_cm<2.1715V.
- The bandwidth of the amplifier is 2.075M Hz.
## Inference
- The diffrential pair amplifier is used to eleminate the noise completly i.e Vo1-Vo2=0.
- The mosfet after the maximum input the mosfet M1 and M2 are forced towards the triode region it will effect the operation of the mosfet
- To improve the gain of the mosfet we required increase the Rd value or width value if we increas the Rd value it will effect your biasing the best way to increase the gain by increasing the width ,if we increase the gain then we have to compramise with the output voltage swing.
- The tail resistor forced both the transistor to maintain the same Id value because to design the diffrential pair amplifier both transistor must be perfectly matched
- The tail current in the circuit is controls the gain if we increase the tail current it will effect the input voltage swing
  | Tail configuration | Gain | Bandwidth | Input CM Swing |
  | --------------- | ----- | --------- | ------- |
  | Resistive Load |	Low | High	| Low	|  
  | Current Source |	High | Low | High | 	
  | MOSFET Tail | Moderate | Moderate	| Lower than current source |	






  
