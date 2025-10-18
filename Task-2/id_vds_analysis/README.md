# 📈 Id–Vds Characteristics Analysis  

> Exploring the drain current vs. drain voltage behavior of NMOS and PMOS transistors.  

---

## 🧠 Overview  
The **Id–Vds (Drain Current vs. Drain Voltage)** analysis demonstrates how the MOSFET operates in different regions:  

- **Linear (Ohmic) Region**: Id increases linearly with Vds.  
- **Saturation Region**: Id becomes almost constant with increasing Vds.  
- **Cut-off Region**: No current flows when Vgs < Vth.  

This analysis helps understand **MOSFET behavior** for designing analog and digital circuits.  

---

## ⚙️ Netlist File  

`id_vds.sp` — SPICE netlist for Id–Vds simulation.  

---

## 🧰 Tools  

| Tool | Purpose |
|------|---------|
| Ngspice | Run DC sweep simulations |
| Sky130 PDK | Transistor models |
| Ubuntu/Linux | Environment |
| Gedit/VS Code | Editing netlists |

---

## 🗂️ Commands  

Run the simulation:  
```bash
cd ~/Desktop/sky130CircuitDesignWorkshop/id_vds_analysis
ngspice id_vds.sp
```
Inside Ngspice:
```bash
plot i(drain) v(drain)
```
### 🖼️ Results
<img width="1210" height="796" alt="Id-VDS " src="https://github.com/user-attachments/assets/eeaa3666-125e-4a50-aecd-933b0a552590" />

### Waveform
<img width="1210" height="796" alt="Id–Vds waveform" src="https://github.com/user-attachments/assets/2080fa8b-c9c5-47fd-a2cd-f31239fd6358" />

### 🧮 Observations

Linear increase of Id at low Vds

Saturation reached at higher Vds

Threshold voltage clearly visible



