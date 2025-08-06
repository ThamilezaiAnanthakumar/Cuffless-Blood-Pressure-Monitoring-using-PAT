# Cuffless Blood Pressure Monitoring using PAT

This project explores a non-invasive method for estimating blood pressure without the use of a traditional cuff, using **Pulse Arrival Time (PAT)** and **Pulse Transit Time (PTT)**.

PAT is the time interval between the **R-peak** in the ECG signal and the **pulse onset** in the PPG signal. This interval reflects arterial stiffness and vascular condition, which correlate with blood pressure.

## Project Overview

- **Current Work**: I am currently working with **Pulse Arrival Time (PAT)**. The system detects the **R-peak** from ECG and the **pulse onset** from the PPG signal. PAT is calculated from these two events. A calibration process is used to estimate blood pressure from PAT values.
  
- **Future Plan**: I plan to move toward **Pulse Transit Time (PTT)**, which requires synchronized PPG signals or pressure sensor data from two distinct points. Due to the current unavailability of real-world datasets, I am developing a custom sensor system using two **MAX30102** sensors integrated into a single PCB, spaced 5 cm apart.

## Signal Processing

- **ECG R-peak detection** is used to mark the electrical onset of the cardiac cycle.
- **PPG pulse onset detection** is used to mark the mechanical pulse wave.
- **PAT = Time(R-peak) - Time(PPG Onset)**
- These features are extracted and used to estimate systolic and diastolic blood pressure using a machine learning model.

## Hardware

- Dual **MAX30102 PPG sensors** on a custom PCB.
- Goal: Calculate **PTT** across a 5 cm distance using pressure pulse wave velocity.

## Tools & Languages

- Python,Neurokit2 
- Custom PCB design
- Signal processing algorithms for R-peak and pulse onset detection
- Machine Learning for BP prediction

## PAT 

###  PAT Visualization  
![PAT Image](https://raw.githubusercontent.com/ThamilezaiAnanthakumar/Cuffless-Blood-Pressure-Monitoring-using-PAT/main/Assets/PAT.png)



## Status

- ✅ PAT-based cuffless BP estimation is in progress.
- 🔜 PTT-based measurement and dual-sensor testing is under development.

## Acknowledgement

This work is part of ongoing research and development in the field of biomedical signal processing. It aims to contribute toward low-cost, continuous, and wearable blood pressure monitoring.

---

