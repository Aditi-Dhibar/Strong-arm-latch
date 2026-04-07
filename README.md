# Strong-arm-latch
Implement a strong arm latch in UMC 65nm technology

---

#  Design & Analysis of Strong Arm Latch

##  Overview
This project focuses on the **design, simulation, layout, and analysis of a Strong Arm Latch comparator** using the **UMC 65nm CMOS process**. The design includes an **SR latch at the output** to ensure output transitions occur every clock cycle.

---

##  Specifications

- **Technology**: UMC 65nm CMOS  
- **Clock Frequency**: 100 MHz  
- **Clock Rise/Fall Time**: 40 ps  
- **Clock Conditioning**: Passed through a 2-stage inverter chain  
- **Input Type**: Differential input  

---

##  Design Description

The Strong Arm Latch is a **dynamic comparator** widely used in high-speed, low-power applications.

### Key Features:
- Regenerative latch structure for fast decision making  
- Differential input stage  
- Cross-coupled inverters for positive feedback  
- SR latch added at output for stable logic transitions  

---

##  Simulation Tasks

### 1. Transient Analysis
- Apply a **differential input voltage of 0.5 mV**
- Run transient simulations
- Observe:
  - Output response  
  - Decision time  
  - Regeneration behavior  

---

### 2. Metastability Analysis
- Gradually reduce input differential voltage  
- Identify the **minimum resolvable input voltage**  
- Determine the point where:
  - Comparator fails to resolve correctly  
  - Output becomes metastable  

---

### 3. Monte Carlo Simulation
- Perform **≥ 300 simulation runs**  
- Analyze mismatch effects  
- Extract:
  - Offset voltage distribution  
  - Calculate **3σ (3-sigma) offset voltage**  
- Plot histogram of offset  

---

### 4. Noise Estimation
- Evaluate comparator noise performance  
- Identify:
  - Input-referred noise  
  - Impact on resolution  

---

##  Layout Design

- Full custom **layout implementation** of the Strong Arm Latch in UMC 65nm  
- Design considerations:
  - Matching of differential pairs  
  - Symmetric layout for reduced mismatch  
  - Proper routing to minimize parasitics  
- Performed **DRC (Design Rule Check)** and **LVS (Layout vs Schematic)** verification  

---

##  Expected Outputs

- Transient waveforms  
- Minimum detectable input voltage  
- Monte Carlo histogram  
- 3σ offset voltage value  
- Noise estimation results  
- Verified layout (DRC & LVS clean)  

---

##  Tools Used

- Cadence Virtuoso (or equivalent EDA tool)  
- Spectre Simulator  
- ADE (Analog Design Environment)  

---

##  Project Structure

```bash
project/
│── comparator_schematic_design/
│── comparator_layout/
│── simulations/
│── results/
│── README.md
```

---

##  Learning Outcomes

- Understanding dynamic comparator operation  
- Effects of mismatch and noise in analog circuits  
- Metastability behavior in regenerative circuits  
- Monte Carlo analysis for statistical variation  
- Layout design and verification (DRC & LVS)  

---

##  Author
**Aditi Dhibar**
