## CURRENT MIRRORING EXPERIMENT
### Introduction
A current mirror is a circuit designed to duplicate (or "mirror") a current from one branch of a circuit to another. It is often used in analog designs to provide a stable reference current that can be replicated throughout various parts of the circuit, typically in differential amplifiers or other types of active circuits Current mirrors are widely used due to their high output resistance, improved accuracy, and ability to maintain constant current independent of voltage variations. The experiment involves simulating different types of current mirror circuits, such as basic current mirrors, Wilson current mirrors, and cascode current mirrors, to analyze their performance, current transfer accuracy, and voltage dependencies. By understanding these circuits, engineers can design efficient current sources and biasing networks for various analog and mixed-signal applications.
### Purpose of current mirroring circuits:
  - To provide a constant current to parts of the circuit without relying on resistors
  - To create a stable reference current for other parts of the circuit.
  - To improve the matching of current sources across multiple transistors or stages.
### How It Works:
A basic current mirror usually consists of two transistors, typically bipolar junction transistors (BJTs) or MOSFETs, arranged in a configuration where the current flowing through one transistor is mirrored in the second transistor.
  - 1.**Reference Current (Iref):** The first transistor (often called the reference transistor) is biased with a known reference current, which could be set using a resistor or another circuit.
  - 2.**Current Duplication:** The second transistor (called the output transistor) is arranged so that it mirrors the reference current. The base (or gate in MOSFETs) of both transistors is tied together, and ideally, the emitter (or source in MOSFETs) is also tied together, forcing the same current to flow through both transistors.
  - 3.**Matching Currents:** The current flowing through the second transistor is designed to be the same as the current in the reference transistor. This is typically achieved by ensuring that both transistors have matching characteristics, such as the same geometry, temperature, and other factors.
### Types of Current Mirrors:
  **1.Simple Current Mirror:**
    - The most basic current mirror consists of two transistors. However, it may not provide precise current mirroring under all conditions (such as voltage variations or mismatch between transistors).
    
  **2.Wilson Current Mirror:**
    - This configuration adds a third transistor to improve the output current's accuracy. It provides better performance by reducing the effects of early voltage (which causes the output current to depend on the output voltage).
    
  **3.Cascode Current Mirror:**
    - A cascode current mirror adds additional transistors to further improve performance by increasing the output impedance and reducing the impact of variations in voltage, making the current more stable.
    
  **4.Active Current Mirror:**
    - Uses additional circuitry, often with feedback, to enhance the precision and stability of the current mirror, even in the presence of variations in temperature and supply voltage.

### Advantages of Current Mirrors:
  **1.Stability:** They provide a stable current that is less sensitive to supply voltage fluctuations.

  **2.Compactness:** Current mirrors reduce the need for bulky resistors and offer a more integrated way of providing reference currents.

  **3.Accuracy:** With proper design, current mirrors can provide very accurate current replication.

  ### 4. ANALYTICAL DESIGN APPROACH
GIVEN:<br>
VDD = 1.8V <br>
P <= 1mW <br>
AV > -10v/v <br>

ITOTAL = P/VDD <br>
ITOTAL <= 1/1.8 <br>
ITOTAL <= 0.555mA <br>

ITOTAL = IREF + IX <br>
For **1:1 Current mirror ratio. IREF = 0.277mA & IX = 0.277mA** <br>
For **1:2 Current mirror ratio IREF is 0.185mA & IX = 0.365mA** <br>

**THE ASPECT RATIO'S OF MOSFET IS 16.66**<br>

**THE ASPECT RATIO'S OF MOSFET FOR 1:1 CURRENT MIRROR**:<br>
  - M1 = 3um/180nm
  - M2 = 3um/180nm
  - M3 = 3um/180nm
**VGS = 0.838V**<br>

**THE ASPECT RATIO'S OF MOSFET FOR 1:2 CURRENT MIRROR**:<br>
  - M1 = 3um/180nm
  - M2 = 6um/180nm
  - M3 = 6um/180nm
**VGS = 0.763V**<br>
### 5. SIMULATION OF CURRENT MIRROR LOAD COMMON SOURCE AMPLIFIER OF 1:1 MIRROR RATIO.
#### 1. DC ANALYSIS
Built the circuit as per the circuit diagram below <br>
![image](https://github.com/user-attachments/assets/a0dea230-bf02-4c0a-a8de-d35094477f26)


To perform the DC Analysis click the edit simulation and select the DC OP point(.op).<br>
![image](https://github.com/user-attachments/assets/dd4127da-8e3c-4710-b74f-017639d1210d)


**ID M1 =  277uA , ID M2 = 277.5uA , ID M3 = 277.5uA .** <br>
#### 2.TRANAIENT ANALYSIS 
To perform Transient analysis click the edit Simulation then click on Transient Analysis.<br>
Now give the stop time as 10ms and Run.<br>

![image](https://github.com/user-attachments/assets/12b6c47d-f490-4395-a346-421ca9effbe2)

The above Output shows the Amplified Signal with 180° Phase Shift of input signal of Amplitude 50mV.<br>

The Gian from The Transient Analysis is -10.1 V/V.
#### 3. AC ANALYSIS
To perform AC Analysis click the edit simulation then click on AC Analysis.<br>
Now select the type of sweep as **Decade** , No.of points as **10m** and then give **Starting frequency as 1Hz & Ending as 1MHz** then Run.<br>

![image](https://github.com/user-attachments/assets/dcb6bc48-a962-4f5b-b354-37e79c4b3d66)

**Gain in db is 22.1db & Bandwidth is 2.29GHz .**

### 6. SIMULATION OF CURRENT MIRROR LOAD COMMON SOURCE AMPLIFIER OF 1:2 MIRROR RATIO.
#### 1.DC ANALYSIS
![image](https://github.com/user-attachments/assets/3683c9d2-3189-4595-9001-08793225dd39)

Follow the same steps to perform DC Analysis.

![image](https://github.com/user-attachments/assets/607d7b1a-d17d-42ff-8f7d-a1e1b3fd0f8b)

**ID M1 =  185uA , ID M2 = 365.17uA , ID M3 = 365.17uA .** <br>
#### 2.TRANAIENT ANALYSIS
Follow the same steps to perform Transient Analysis.

![image](https://github.com/user-attachments/assets/a5bc3066-6712-4e5f-be58-d15f7e961d0f)
The above Output shows the Amplified Signal with 180° Phase Shift of input signal of Amplitude 50mV.<br>

The Gian from The Transient Analysis is -11.69 V/V.
#### 3. AC ANALYSIS
Follow the same steps to perform AC Analysis.
![image](https://github.com/user-attachments/assets/9de834c1-efea-4407-93df-54240af92add)

**Gain in db is 22.96db & Bandwidth is 1.435GHz .**

### 7. SIMULATION OF CURRENT MIRROR LOAD COMMON SOURCE AMPLIFIER OF 1:3 MIRROR RATIO.
For **1:3 Current mirror ratio IREF is 0.139mA & IX = 0.416mA** <br>
**THE ASPECT RATIO'S OF MOSFET FOR 1:3 CURRENT MIRROR**:<br>
  - M1 = 6um/180nm
  - M2 = 18um/180nm
  - M3 = 18um/180nm
**VGS = 0.632V**<br>

#### 1.DC ANALYSIS
![image](https://github.com/user-attachments/assets/97529e30-4025-4d4d-8630-bc776836220f)

Follow the same steps to perform DC Analysis.
![image](https://github.com/user-attachments/assets/889356c0-2ce4-43c4-a453-313aaa4326c6)

**ID M1 =  139uA , ID M2 = 416.08uA , ID M3 = 416.08uA .** <br>

#### 2.TRANAIENT ANALYSIS
Follow the same steps to perform Transient Analysis.

![image](https://github.com/user-attachments/assets/25b8d935-8eaa-49c7-826d-f4a5468d0968)

The above Output shows the Amplified Signal with 180° Phase Shift of input signal of Amplitude 50mV.<br>

The Gian from The Transient Analysis is -14.69 V/V.

#### 3. AC ANALYSIS
Follow the same steps to perform AC Analysis.
![image](https://github.com/user-attachments/assets/9ce3d467-4a91-438f-8168-4af0d0da2e7f)

**Gain in db is 27.3db & Bandwidth is 493.415MHz .**

### INFERENCE


