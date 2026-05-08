4. **Zero Crossing Rate** - Claps oscillate much faster than voice or instruments
5. **Fast Decay**: A clap fades quickly;     Sustained sounds are not

A sound must score **at least 4 out of 5** to be confirmed as a clap.     This makes detection reliable even in noisy environments or while playing loud music.

---

## 🖥️ Interface

The app has a native desktop UI built with PyQt6 that displays:

- A real-time audio volume and waveform meter.
- The current evaluation score and the criteria they passed.
- A live activity log
- A sensitivity slider to adjust detection to your environment
- An icon in the system tray so that it doesn't get in the way

---

## ⚙️ Technology stack

- **Python** — main language
- **PyQt6** — desktop interface
- **PyAudio** — microphone input
- **NumPy** — audio signal processing and FFT analysis
- **PyAutoGUI** — multimedia key simulation
- **PyInstaller**: packaged in a separate `.exe`

---

## 📋Requirements

-Windows 10/11
- Microphone (integrated or external)
- Spotify installed

Project in beta 
You can detect fake clapping on laptops if you type the keys too hard near the microphone.
---

## 🚀 Getting started


To run it from source or compile it yourself, see the full [README] (README.md).

---

## 📄 License

MIT: Use it, modify it, and share it freely.
