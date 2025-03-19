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
