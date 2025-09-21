# ⚙ Procedure – Air Conditioning System (LabVIEW)

This document explains the step-by-step procedure to create and test the **Air Conditioning System Simulation** in NI LabVIEW.  

---

## 🖥 1. Front Panel Design  

1. **Open a New VI** → Switch to the *Front Panel*.  

2. **Add Indicators & Controls**  
   - **Thermometer** → Numeric → Thermometer → to display real-time room temperature.  
   - **Waveform Chart** → Graph → Waveform Chart → to plot temperature variation over time.  
   - **Max Temperature Set Point (Knob/Slider)** → Numeric Control (e.g., upper comfort limit).  
   - **Min Temperature Set Point (Knob/Slider)** → Numeric Control (e.g., lower comfort limit).  
   - **AC Status LED** → Boolean indicator showing AC ON/OFF state.  
   - **Stop Button** → Boolean control to stop the program.  

3. **Organize & Label**  
   - Place the thermometer on the left, chart in the center, knobs/sliders at the bottom, AC LED near thermometer, and stop button at top.  
   - Optionally add labels like “Room Temperature,” “Comfort Range,” and “AC Status” for clarity.  

---

## 🔗 2. Block Diagram Logic  

1. **Add While Loop**  
   - Place a While Loop around all logic (Functions → Structures → While Loop).  
   - Wire the **Stop button** to loop conditional terminal.  

2. **Simulate Temperature Signal**  
   - Use Simulate Signal block (Functions → Signal Processing → Signal Generation).  
   - Configure inputs:  
     - **Amplitude = (Max – Min)/2**.  
     - **Offset = (Max + Min)/2**.  
   - This ensures simulated room temperature oscillates between the set Min and Max.  

3. **Display Temperature**  
   - Wire the signal output to the **Thermometer** and **Waveform Chart**.  

4. **AC Control Logic**  
   - Compare current temperature with limits:  
     - If **Temp > Max** → AC turns *ON* (cooling mode).  
     - If **Temp < Min** → AC turns *OFF*.  
     - Else → AC keeps its previous state.  
   - Implement this logic using **Greater Than, Less Than, and Select** functions.  

5. **Shift Register (Memory)**  
   - Add a Shift Register to the While Loop.  
   - Initialize to FALSE (AC OFF at start).  
   - Maintain previous AC state when temperature is within the Min–Max comfort band.  

6. **AC Status Indicator**  
   - Wire final AC state to the Boolean LED on the Front Panel.  

---

## ▶ 3. Running the VI  

1. Open the VI and switch to the **Front Panel**.  
2. Set **Min and Max Comfort Temperature values** using knobs/sliders.  
3. Click **Run**.  
4. Observe:  
   - Room temperature signal appears on the **thermometer** and **waveform chart**.  
   - If temperature rises **above Max, AC turns ON** (LED lights).  
   - If temperature falls **below Min, AC turns OFF**.  
   - If temperature is within comfort range, AC keeps its last state.  
5. Press **Stop** at any time to end the simulation.
