# DSBSC-Using-Python
---

### Aim:

To implement and analyze DSBSC using Python's NumPy and Matplotlib libraries.

---

### Apparatus Required:

- Software: Python with Numpy and Matplotlib libraries.
- Hardware: Personal Computer.

---

### Algorithm:

1. Initialize Parameters: Set the values for carrier frequency, message frequency, sampling frequency and frequency deviation.
2. Generate Time Axis: Create a time vector for the signal duration.
3. Generate Message Signal: Define the message signal as a cosine wave.
4. Compute the Integral of the Message Signal: Calculate the integral of message signal over time.
5. Generate DSBSC Signal: Apply the DSBSC formula to obtain the modulated signal.
6. Plot the Signals: Use Matplotlib to plot the message signal, carrier signal, and modulated signal.

---

### Program:

```py
import numpy as np
import matplotlib.pyplot as plt
Am=4.8
fm=9.6
Ac=360
fc=3600
fs=36000
t=np.arange(0, 3/fm, 1/fs)

m = Am*np.cos(2*3.14*fm*t)
plt.subplot(3,1,1)
plt.plot(t,m)

c = Ac*np.cos(2*3.14*fc*t)
plt.subplot(3,1,2)
plt.plot(t,c)

s1=(Ac+m)*np.cos(2*3.14*fc*t)
s2=(Ac-m)*np.cos(2*3.14*fc*t)

s=s1-s2
plt.subplot(3,1,3)
plt.plot(t,s)

```

---

### Output Waveform:

<img width="695" height="506" alt="image" src="https://github.com/user-attachments/assets/6d04610a-0998-4d0c-bf3a-82164ec209ca" />

---

### Tabular Column:

![WhatsApp Image 2025-11-24 at 20 26 32](https://github.com/user-attachments/assets/3170d88d-c50d-4c4a-a1df-d0edd737a585)

---

### Result:

Thus the DSBSC-AM Modulation is generated using python.
