# EEG Signal Analysis and Visualization

This repository contains an analysis pipeline for **EEG signal processing**, focusing on **visualizing raw EEG signals over time and their frequency-domain transformation**. The dataset originates from the **Garches Hospital Sleep Studies Lab (France, Paris area)** and aims to detect **spindles**, a specific EEG pattern associated with sleep.

## Dataset Overview

The dataset consists of **electroencephalogram (EEG) signals** extracted from a single EEG recording, primarily from the **C3-A1 and C4-A1 electrodes**. The raw EEG data is recorded over a 30-minute sleep period.

### **Features**
The dataset contains the following columns:

- **Date, HH, MM, SS** → Timestamp of each EEG recording.
- **EOG Left [uV]** → Electrooculogram (EOG) signal measuring eye movements.
- **EEG C3-A1 [uV], EEG O1-A1 [uV], EEG C4-A1 [uV], EEG O2-A1 [uV]** → EEG signals recorded from different brain regions.

---

## **Data Processing Steps**

### **1. Time Conversion**
- The dataset initially provides separate columns for **hours, minutes, and seconds**.
- These were combined into a **single time series format** to facilitate visualization.

### **2. Data Visualization**
- **Time-Domain Analysis:**  
  - EEG signals were plotted over time to observe natural fluctuations and detect patterns.
  - This helped in identifying potential artifacts, noise, and dominant waveforms.

- **Frequency-Domain Analysis:**  
  - EEG signals were transformed from the **time domain** to the **frequency domain** using the **Fast Fourier Transform (FFT)**.
  - A **periodogram** was computed to analyze **power spectral densities (PSD)**, revealing dominant frequencies in the signal.

### **3. Frequency Transformation**
- The **raw EEG signals** were converted into **frequency components**, focusing on key EEG wave bands:
  - **Delta (0.5–4 Hz)**
  - **Theta (4–8 Hz)**
  - **Alpha (8–12 Hz)**
  - **Sigma (12–16 Hz) – where spindles typically occur**
- This transformation helped identify which frequency ranges were most prominent during the recorded sleep period.
