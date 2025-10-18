
---

## 2️⃣ `id_vgs_analysis/README.md`

```markdown
```
# 📊 Id–Vgs Characteristics Analysis  

> Transfer characteristics of NMOS/PMOS transistors: Drain current vs. Gate voltage.  

---

## 🧠 Overview  
The **Id–Vgs (Drain Current vs. Gate Voltage)** analysis is used to determine:  

- **Threshold voltage (Vth)**  
- **Transistor switching behavior**  
- **Subthreshold and strong inversion regions**  

This provides insight into the control of current flow via gate voltage.  

---

## ⚙️ Netlist File  

`id_vgs.sp` — SPICE netlist for Id–Vgs simulation.  

---

## 🧰 Tools  

| Tool | Purpose |
|------|---------|
| Ngspice | DC sweep simulation |
| Sky130 PDK | MOSFET models |
| Ubuntu/Linux | Environment |
| Gedit/VS Code | Netlist editing |

---

## 🗂️ Commands  

Run the simulation:  
```bash
cd ~/Desktop/sky130CircuitDesignWorkshop/id_vgs_analysis
ngspice id_vgs.sp
```
Inside Ngspice:
```
plot i(drain) v(gate)
```
### 🖼️ Results
<img width="1210" height="796" alt="id vs VGS" src="https://github.com/user-attachments/assets/7392a3f8-0fea-470c-8abf-9bb231c46bc3" />

## Waveform
<img width="1210" height="796" alt="Id vs Vgs Sweep" src="https://github.com/user-attachments/assets/0cc8487a-dccd-41c5-80f2-dc2dd5e40025" />

## 🧮 Observations

Threshold voltage visible at Id ≈ 0

Current increases exponentially in subthreshold

Saturation observed at higher Vgs


