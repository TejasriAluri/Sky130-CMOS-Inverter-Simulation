# ⚡ CMOS Inverter Transient Simulation  
> Analyzing Dynamic Switching Behavior of a CMOS Inverter using Sky130 PDK

---

## 🧠 Overview  
This task focuses on simulating the **transient (time-domain)** response of a **CMOS inverter** built using the **SkyWater Sky130 PDK**.  
The simulation captures how the output voltage changes when the input switches between logic high and logic low — showcasing **inversion, delay, and switching characteristics**.

---

## ⚙️ Objective  
- To design and simulate a **CMOS inverter** using NMOS and PMOS transistors.  
- To analyze **transient response** (Vout vs time) when the input signal toggles.  
- To observe **switching delay**, **rise/fall times**, and logic inversion.

---

## 🧰 Tools & Environment  

| Tool | Purpose |
|------|----------|
| Ngspice | Circuit-level simulation |
| SkyWater Sky130 PDK | Device models (NMOS, PMOS) |
| Ubuntu/Linux | Development environment |
| Gedit / VS Code | Editing and running SPICE files |

---

## 🧱 Circuit Description  
- A CMOS inverter consists of one **PMOS** (connected to VDD) and one **NMOS** (connected to GND).  
- The input signal drives both transistor gates.  
- The output is taken from the common drain node.  

**File:** `sky130_cmos_inverter.sp`

**Key Setup:**
- **VDD = 1.8V**  
- **Input:** Pulse signal toggling between 0V and 1.8V  
- **Simulation Type:** `.tran` (Transient Analysis)  

---

## 🧩 Simulation Commands  
```bash
ngspice sky130_cmos_inverter.sp
plot v(in) v(out)
```
### 📊 Results
<img width="1280" height="796" alt="CMOS Trans" src="https://github.com/user-attachments/assets/571f0a96-ff4c-4865-9102-facb5d1e56f3" />

### waveform
<img width="1280" height="796" alt="cmos_tran_waveform" src="https://github.com/user-attachments/assets/0ced58d7-2921-412e-a506-a059718b7b57" />

## Expected Behavior:

When Vin = 0V, Vout = VDD (logic 1)

When Vin = 1.8V, Vout = 0V (logic 0)

Shows complementary switching between NMOS and PMOS

## 🧭 Learning Outcomes

✅ Understood the working of a CMOS inverter at transistor level.
✅ Learned to perform transient analysis using Ngspice.
✅ Observed real-time switching and logic inversion behavior.


