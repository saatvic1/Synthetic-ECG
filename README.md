# Synthetic-ECG
import numpy as np
import matplotlib.pyplot as plt

# Simulated time (10 seconds at 500 Hz sampling rate)
fs = 500
t = np.linspace(0, 10, 10 * fs)

# Create a basic synthetic ECG using sine waves + noise
heart_rate = 60  # bpm
f = heart_rate / 60  # Hz
ecg = 1.5 * np.sin(2 * np.pi * f * t) + 0.5 * np.sin(4 * np.pi * f * t) + 0.1 * np.random.randn(len(t))

plt.plot(t, ecg, color='red')
plt.title("Synthetic ECG Wave (Simulated)")
plt.xlabel("Time (s)")
plt.ylabel("Amplitude")
plt.grid(True)
plt.show()
