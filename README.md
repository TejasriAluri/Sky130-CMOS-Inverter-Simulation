# Sky130-CMOS-Inverter-Sim# ⚡ Sky130 CMOS Inverter – Ngspice Simulation  

> **A comprehensive transistor-level analysis of a CMOS Inverter using the SkyWater 130nm PDK and Ngspice.**  
> This project demonstrates DC, Transient, and Parametric simulations of CMOS circuits in an open-source environment.

---

## 🧠 Overview  

This project focuses on designing and simulating a **CMOS inverter** using the **SkyWater Sky130 open-source Process Design Kit (PDK)** in **Ngspice**.  
It aims to explore fundamental CMOS characteristics such as:  

- The **Voltage Transfer Characteristics (VTC)**  
- **Id–Vds** and **Id–Vgs** behavior of NMOS and PMOS  
- **Transient response** analysis  

Through this project, a strong understanding of transistor behavior and circuit-level characteristics in sub-micron technology is developed.

---

## 🎯 Objectives  

- Understand CMOS inverter operation using Sky130 devices  
- Perform DC and Transient analysis using Ngspice  
- Explore Id–Vds and Id–Vgs curves for NMOS and PMOS  
- Visualize voltage transfer and switching characteristics  
- Learn the integration of PDK model files in SPICE simulations  

---

## 🧰 Tools & Technologies  

| Tool / Technology | Description |
|-------------------|-------------|
| **Ngspice** | Open-source circuit simulator used for SPICE netlist simulation |
| **SkyWater Sky130 PDK** | 130nm open-source Process Design Kit |
| **Ubuntu/Linux** | Operating system used for simulation environment |
| **Gedit / VS Code** | Netlist editing and script management |
| **Matplotlib / Python (optional)** | For custom data visualization |

---

## 🧩 Project Structure  

```bash
sky130CircuitDesignWorkshop/
├── README.md                         # Main documentation file  
├── sky130_cmos_inverter.sp            # CMOS inverter transient simulation netlist  
├── id_vds_analysis/                   # NMOS & PMOS Id–Vds characteristics  
│   ├── id_vds_nmos.sp  
│   └── id_vds_pmos.sp  
├── id_vgs_analysis/                   # NMOS & PMOS Id–Vgs characteristics  
│   ├── id_vgs_nmos.sp  
│   └── id_vgs_pmos.sp  
├── vtc_analysis/                      # Voltage transfer curve of CMOS inverter  
│   └── vtc_inverter.sp  
├── results/                           # Output plots and data  
│   ├── transient_response.png  
│   ├── vtc_curve.png  
│   ├── id_vds_plot.png  
│   └── id_vgs_plot.png  
└── skywater-pdk/                      # Sky130 PDK models  
ulation
```
### ⚙️ Simulation Flow
## 1. Setup Sky130 PDK Models

Ensure model paths are correctly linked in your SPICE netlist:

```bash
.include "/home/<user>/Desktop/sky130CircuitDesignWorkshop/skywater-pdk/libraries/sky130_fd_pr/v0.20.0/models/sky130.lib.spice"
.lib "/home/<user>/Desktop/sky130CircuitDesignWorkshop/skywater-pdk/libraries/sky130_fd_pr/v0.20.0/models/sky130.lib.spice" tt
```
### 2. Run Simulation

Run the following in the terminal:
```bash
cd ~/Desktop/sky130CircuitDesignWorkshop
ngspice sky130_cmos_inverter.sp
```
### 3. Plot Results

Inside Ngspice prompt:
```bash
plot v(in) v(out)
```
### 📊 Expected Results

| Simulation Type | Expected Output                                  |
| --------------- | ------------------------------------------------ |
| **Transient**   | Inverter switching behavior (v(in) vs v(out))    |
| **VTC**         | Smooth inverter voltage transfer curve           |
| **Id–Vds**      | Saturation & triode region visualization         |
| **Id–Vgs**      | Threshold voltage identification for NMOS & PMOS |

### 📘 Learning Outcomes

- Gained practical understanding of MOSFET I–V characteristics

- Implemented PDK model inclusion and usage in SPICE

- Simulated CMOS inverter switching and voltage transfer behavior

- Strengthened knowledge in analog circuit analysis and modeling

### 🏁 Next Steps

- Add Id–Vds and Id–Vgs analysis files with detailed plots

- Explore ring oscillator design using Sky130 inverter chains

- Automate simulation using Python + Ngspice scripting

### 🧑‍💻 Author

Tejasri Aluri

📍 Electronics & Communication Engineer | IoT & VLSI Enthusiast

💡 Passionate about chip design, circuit analysis, and open-source EDA.

### 🌐 References

SkyWater Open PDK GitHub Repository

Ngspice Official Documentation

VLSI System Design (VSD) Workshops
