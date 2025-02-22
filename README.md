# Experiment-1
Question : Given that POWER, P=100µ W; Perform DC Analysis, Transient Analysis and AC Analysis for the Given Circuit Designs and also check what happens when the width is increased or decreased of each mosfet;

### Design-1 :
![2025-02-17](https://github.com/user-attachments/assets/1062e9cb-6fe1-4b00-a64b-b09c138f482a)

Using the Formula for Power,

P=V*I

We will get the Values of Id as,

Id= 5.56 * 10^-5 A

we have to get the output current, Id for the given circuits by adjusting the values of L & W( Length and Width of the Channel of the MOSFET)

Length and Width of the Channel used to obtain the given Current is shown in the figure below;

![2025-02-17 (33)](https://github.com/user-attachments/assets/6eb2321b-7fef-4b5a-92f7-22cb30ef3053)

### a.DC ANALYSIS:

Procedure for Performing DC Analysis: we have to select the dc output print(DC op pnt) in the Edit Simulation Command and Run the Simulation

![image](https://github.com/user-attachments/assets/afd73325-e8d8-41d8-a6fa-ff0b2a68138e)

### b.Transient Analysis:

Procedure for Performing Transient Analysis: we have to select the Transient Analysis in the Edit Simulation Command, Give the stop time as 1ms and Run the Simulation.
![image](https://github.com/user-attachments/assets/01fda656-b7d0-4493-b590-5cb6576cce25)

The Graphs below shows the Transient Response of the Given Design;
![image](https://github.com/user-attachments/assets/af87addd-67fd-46ac-8cb8-7b0d3f6f11bf)

![image](https://github.com/user-attachments/assets/b63247cf-918a-4a12-894f-4426086d69cd)

### c.AC Analysis:

Procedure for Performing AC Analysis: we have to select the AC Analysis in the Edit Simulation Command, Give the values as shown in the figure beowl and Run th Simulation.

![image](https://github.com/user-attachments/assets/f0c19ec4-6f55-4b26-b217-4af529be38ad)

The Graph below shows the AC Analysis of the Given Design;
![image](https://github.com/user-attachments/assets/f7bfef49-216e-4451-92a2-5383d7919f1b)

### RESULT:
    DC Analysis:
    
    The calculated drain current (Id) matches the expected value based on power and voltage, Id = 5.56*10^-5 A.
    By adjusting the MOSFET’s channel dimensions (L & W) where L=180nm and W= 203nm, The current requirement was succesfully achecived.
    The circuit behaves as expected under DC conditions.
    Transient Analysis:
    
    The transient response graph shows how the circuit behaves over time.
    The response is smooth, with no unexpected delays or distortions.
    The circuit reacts well to changes, confirming its stability.
    AC Analysis:
    
    The AC response graph confirms that the circuit remains stable at different frequencies.
    The gain(2 dB) and phase shift(which is nearly 180deg) align with theoretical expectations.
    The circuit maintains its performance across the tested frequency range.
    
### INFERENCE( Design-1):
    The experiment confirms that by properly selecting the MOSFET dimensions, we can control the drain current effectively.
    Impact of Width Adjustments:
    M1 has a influence on Id, meaning its width affects the output current.
    The circuit performs well in all three analyses—DC, transient, and AC—demonstrating its reliability.
    Overall, the design works as intended, following theoretical predictions and proving its practical feasibility.


### Design-2
    ![dfdfdffd](https://github.com/user-attachments/assets/b0fd1f86-e0be-4b78-903f-f818513d8e25)

Using the Formula for Power,

P=V*I/n

We will get the Values of Id as,

Id= 5.56 * 10^-5 A

we have to get the output current, Id for the given circuits by adjusting the values of L & W of both the MOSFETS M1 & M2 ( Length and Width of the Channel of the MOSFET)

DC SWEEP Analysis: This analysis is done for obataing the value of Vin in Saturation range;

we have to select the DC SWEEP in the Edit Simulation Command, Give the values as shown in the figure below and Run th Simulation.

![image](https://github.com/user-attachments/assets/46cbde8b-856f-4a53-88a5-c39371bafa2b)
The Graph below represents the VTC Curve and the value of the vin is selected as 0.7V as it is present in the saturation region of the VTC Curve

![image](https://github.com/user-attachments/assets/d7b0d2d4-8338-4f25-8cf4-d9a485a607dc)
Then the input voltage parameters are given as;

![image](https://github.com/user-attachments/assets/188c0d4a-6673-4891-9083-d4552affe1d6)

Length and Width of the Channel of the two MOSFETS used to obtain the given Current is shown in the figure below;


![image](https://github.com/user-attachments/assets/ece194ad-678b-43c3-9367-f9d4de4c3d54)
### 1.DC ANALYSIS:

Procedure for Performing DC Analysis: we have to select the dc output print(DC op pnt) in the Edit Simulation Command and Run the Simulation

![image](https://github.com/user-attachments/assets/9a7a72df-a810-4311-8380-8d66222cc665)

### 2.Transient Analysis:

Procedure for Performing Transient Analysis: we have to select the Transient Analysis in the Edit Simulation Command, Give the stop time as 1ms and Run the Simulation.


![image](https://github.com/user-attachments/assets/a0fc8048-7c85-4f46-b5b4-17042c7aa375)


![image](https://github.com/user-attachments/assets/56c308c2-c76a-4e05-83d9-2bc0150fe9ea)

### AC Analysis:

rocedure for Performing AC Analysis: we have to select the AC Analysis in the Edit Simulation Command, Give the values as shown in the figure beowl and Run th Simulation.

![image](https://github.com/user-attachments/assets/fb6f10a3-c79b-4df9-8913-24d4b19de35e)
The Graph below shows the AC Analysis of the Given Design;

![image](https://github.com/user-attachments/assets/d114f938-1344-48ae-b8ab-09e1be585b39)

### RESULT(DESIGN-2)
1.DC Analysis:

-The calculated drain current (Id) aligns with the expected value based on power and voltage, where the value of Id = 5.56*10^-5 A .
*By fine-tuning the channel dimensions (L & W) of both MOSFETs ( M1 & M2), the desired current was achieved,
*M1 : L= 180nm , W= 1105nm.
*M2 : L= 180nm , W= 1105nm.
*The circuit operates correctly within the selected DC parameters.
 2.Transient Analysis:

 *The transient response graph confirms that the circuit transitions smoothly over time.
*The circuit responds effectively to input variations, indicating stable operation.
3.AC Analysis:

*The AC response graph confirms that the circuit maintains stability over the tested frequency range.
*The gain(5.5 dB) and phase shift (which is nearly 180deg) align with theoretical expectations.
*The circuit functions as expected under AC conditions.

### Inference :
 *The experiment validates that by appropriately selecting the MOSFET dimensions (L & W), the drain current can be precisely controlled.

*The voltage transfer characteristics (VTC) helped in selecting the correct operating voltage (0.7V) for saturation.

*variation due to the change in length :

*M2 has a stronger influence on Id, meaning its width significantly affects the output current.
*M1 has a smaller influence, meaning changes in its width result in only minor variations in Id.
*The design meets the expected performance criteria and follows theoretical predictions, demonstrating its feasibility in practical applications.




