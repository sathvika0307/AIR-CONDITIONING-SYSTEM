# ❄ Air Conditioning System (LabVIEW Project)  

## 📌 Overview  
This project demonstrates an **Air Conditioning (AC) Control System** using **NI LabVIEW**.  
It simulates real-time monitoring of room temperature with **automatic cooling control** based on user-defined comfort limits.  
The AC switches **ON** when temperature exceeds the maximum threshold and switches **OFF** when it goes below the minimum threshold.  

Developed as part of the **LabVIEW Programming Laboratory (B.Tech – EIE)** course.  

---

## 🎯 Objectives  
- Maintain room temperature within a **desired comfort range**.  
- Automate **AC ON/OFF control** using thermostat logic.  
- Provide **interactive user controls** for Min/Max temperature settings.  
- Visualize real-time changes through indicators and graphs.  

---

## 🛠 Features  
- **Real-time simulation** of room temperature using LabVIEW’s signal generator.  
- **AC ON/OFF control** using threshold-based logic.  
- **Hysteresis effect (memory):** AC maintains its previous state when temperature is within range.  
- **Dynamic Visualization:**  
  - Thermometer to show room temperature.  
  - Waveform chart for live temperature trends.  
  - Boolean LED for AC status.  
- **User Interaction:** Min & Max comfort range set points, Stop button for safe termination.  

---

## 📂 Repository Contents  
- Temp Server.vi → Main LabVIEW simulation file.  
- Images/ → Front Panel, Block Diagram, and output screenshots.  
- Procedure.md → Step-by-step guide to recreate the project.  
- README.md → Project documentation (this file).  

---

## 📊 Results  
- Successfully simulated an **automatic cooling system**.  
- AC turned **ON** when temperature exceeded max set point.  
- AC turned **OFF** when temperature dropped below min set point.  
- Thermometer and waveform chart provided clear real-time monitoring.  
- User-defined Min/Max values allowed dynamic adjustments.  

---

## 🔮 Future Scope  
- Integration with **real temperature sensors** (Thermistor/RTD) via **NI-DAQ or Arduino**.  
- Implementation of **PID control** for smoother AC operation (instead of simple ON/OFF).  
- Addition of **cooling + heating system** for complete HVAC simulation.  
- IoT-enabled remote control and monitoring.  
- Data logging and analytics for energy optimization.  

---

## ▶ How to Run  
1. Open AirConditioning.vi in **NI LabVIEW** (any recent version).  
2. Set **Min and Max Comfort Temperature values** using the controls.  
3. Click **Run**.  
4. Observe system behavior:  
   - If temperature > Max → AC turns **ON** (LED lights).  
   - If temperature < Min → AC turns **OFF**.  
   - If temperature is within range → AC maintains last state.  
5. Press **Stop** button to safely end the program.  

👉 For a detailed build guide, see [procedure.md](./procedure.md).
