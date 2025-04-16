# CMOS XOR Gate Design – Cadence Virtuoso

## Project Overview
This project involves the **schematic design and simulation** of a **2-input CMOS XOR gate** using **Cadence Virtuoso Schematic Editor**. The focus is on analyzing the **DC transfer characteristics** and **transient response** of the circuit under different **transistor widths** and **temperature conditions** using **parametric analysis**.

---

## Tools & Technologies
- **Cadence Virtuoso Schematic Editor**
- **Cadence ADE (Analog Design Environment)**
- CMOS technology (gpdk90 - 90nm)
- Parametric Analysis (Sweep Width, Temperature)

---

## Design Specifications
- **Logic Function**:  
  \[
  Y = A \oplus B = (A \cdot \overline{B}) + (\overline{A} \cdot B)
  \]
- **Inputs**: A, B (voltage sources)
- **Output**: Y
- **Technology**: CMOS (Complementary MOSFETs)
- **Simulations**: DC sweep, Transient analysis
- **Parametric Variations**:
  - Transistor widths (Wn/Wp)
  - Temperature: e.g., -40°C, 25°C, 85°C

---

##  Simulations Performed

###  DC Transfer Characteristics
- **Input Sweep**: Vary A (or B) from 0V to VDD while fixing the other.
- **Outputs**: Voltage transfer curve of XOR gate.
- **Parametric Sweep**:
  - Different transistor widths
  - Temperature conditions

### Transient Analysis
- **Input Pulses**: Applied using `vpulse` sources for A and B.
- **Output**: Observe XOR behavior through waveform transitions.
- **Parametric Sweep**:
  - Delay and response under different conditions.

---

## 📊 Results

| Test | Transistor Width | Temperature | Output Behavior |
|------|------------------|-------------|------------------|
| DC Sweep | 180nm | 25°C | Normal Logic Levels |
| Transient | 180nm | 85°C | Slight Delay Observed |
| DC Sweep | 1µm | -40°C | Stronger Pull-up/down |

*(Insert waveform screenshots here once generated)*

---

##  How to Run

1. Open Cadence Virtuoso.
2. Load GPDK 90nm library.
3. Open XOR schematic from `schematic/`.
4. Launch ADE and create testbench.
5. Choose analysis type:
   - **DC Analysis** (sweep input)
   - **Transient Analysis** (using `vpulse`)
6. Use **Tools > Parametric Analysis** for:
   - Varying transistor widths
   - Temperature sweep
7. Run and observe waveforms.

---

##  References
- CMOS Digital Integrated Circuits - Analysis and Design, S. Kang and Y. Leblebici, Tata McGraw Hill 3rd ed. 
- CMOS Digital VLSI Design By Prof. Sudeb Dasgupta, IIT Roorkee (https://archive.nptel.ac.in/noc/courses/noc21/SEM1/noc21-ee09/)
- [Virtuoso Guide | Cadence](https://docs.virtuoso.qa/guide/)
- [gpdk90 docs | Princeton](https://www.princeton.edu/~nverma/cadenceSetup_6.1.7/gpdk090_v4.4/docs/gpdk090_spec.pdf)

---

## Author
**Pratyush**  
BTech in Electronics (VLSI)  
Punjab Engineering College, Chandigarh  
[LinkedIn](https://www.linkedin.com/in/pratyush-kumar-076751289/) | [GitHub](https://github.com/pratstick)

---