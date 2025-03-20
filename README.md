# cosine-wave-plot
import numpy as np
import matplotlib.pyplot as plt

def plot_cosine_wave(frequency=1, amplitude=1, phase=0, duration=2, sample_rate=1000):
    """Plots a cosine wave with given parameters."""
    t = np.linspace(0, duration, duration * sample_rate)
    y = amplitude * np.cos(2 * np.pi * frequency * t + phase)
    
    plt.figure(figsize=(8, 5))
    plt.plot(t, y, label=f'Cosine Wave: {frequency}Hz')
    plt.axhline(0, color='black', linewidth=0.5)
    plt.axvline(0, color='black', linewidth=0.5)
    plt.grid(True, linestyle='--', linewidth=0.5)
    plt.legend()
    plt.title("Cosine Wave")
    plt.xlabel("Time (s)")
    plt.ylabel("Amplitude")
    plt.show()

# Example usage
if __name__ == "__main__":
    plot_cosine_wave(frequency=2, amplitude=1, phase=0)
