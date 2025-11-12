# EEG Smoothing Filters Overview

## 1. Average Filter

### Concept
An average (moving average) filter smooths EEG data by replacing each data point with the mean of its neighbouring samples within a defined window.

### How it Works
- Each point is replaced by the mean of nearby values.
- The window size determines how much smoothing occurs.
- Larger windows remove more noise but can blur important features.

### Effects
- **Small window** → keeps fine temporal details.  
- **Large window** → smoother curve, but may lose fast changes and transient responses.  
- **Trade-off**: balance between noise reduction and signal preservation.

---

## 2. Gaussian Filter

### Concept
A Gaussian filter smooths EEG signals using a Gaussian-shaped weighting curve, giving more importance to points near the centre and less to distant points.

### Key Properties
- Controlled by **σ (standard deviation)**.
- The Gaussian curve width depends on σ:
  - **Small σ** → narrow curve, minimal smoothing.
  - **Large σ** → wide curve, strong smoothing.

### Interpretation
- A larger σ averages over a wider temporal range, removing more high-frequency noise.
- A smaller σ preserves rapid fluctuations and fine details.

---

## 3. Choosing σ

- σ defines the degree of smoothing in **samples** or **time**.
- Convert to seconds as:

