
---

## 3️⃣ `vtc_analysis/README.md`

```markdown
```
# 🔄 CMOS Inverter Voltage Transfer Curve (VTC)  

> VTC analysis of a CMOS inverter to study logic switching characteristics.  

---

## 🧠 Overview  
The **Voltage Transfer Curve (VTC)** shows how the **output voltage (Vout)** changes with **input voltage (Vin)** for a CMOS inverter:  

- **Logic High → Logic Low transition**  
- **Noise margins** and switching thresholds (VM)  
- Insight into inverter performance at the transistor level  

---

## ⚙️ Netlist File  

`vtc_analysis.sp` — SPICE netlist for VTC simulation.  

---

## 🧰 Tools  

| Tool | Purpose |
|------|---------|
| Ngspice | DC sweep and transient simulation |
| Sky130 PDK | CMOS transistor models |
| Ubuntu/Linux | Environment |
| Gedit/VS Code | Netlist editing |

---

## 🗂️ Commands  

Run the simulation:  
```bash
cd ~/Desktop/sky130CircuitDesignWorkshop/vtc_analysis
ngspice vtc_analysis.sp
```
Inside Ngspice:
```
plot v(out) v(in)
```
### 🖼️ Results
<img width="1280" height="796" alt="CMOS inverter DC (VTC) analysis" src="https://github.com/user-attachments/assets/82d9c34c-5629-443e-8c0d-115981cd7fbf" />

## Waveform
<img width="1210" height="796" alt="VTC Plot" src="https://github.com/user-attachments/assets/23687b0e-8aba-4b03-be0a-ab1a5392914e" />

### 🧮 Observations

VTC shows the inverter switching threshold

Logic High and Low regions are clearly visible

Can extract noise margins from the curve


