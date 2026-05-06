When you start the app, it calibrates for 2 seconds to measure the ambient noise in your room.   After that, he's always listening, always ready.

---

## 🔬 The detection algorithm

Most clap detectors fail when playing music because they only compare raw volume levels, and loud music is only as loud as clapping.   Jarvis solves this with a **spectral fingerprint** that rates each sound based on 5 criteria:

1. **Transitional onset**: applause is impulsive bursts, music is sustained
2. **High frequency dominance**: Clapping concentrates energy above 2 kHz;   the bass and the music no
3. **Spectral flatness**: applause is broadband noise, musical notes are tonal
4. **Zero Crossing Rate**: Claps oscillate much faster than voice or instruments
5. **Fast Decay**: A clap fades quickly;   Sustained sounds are not

A sound must score **at least 4 out of 5** to be confirmed as a clap.   This makes detection reliable even in noisy environments or while music is playing at full volume.

---

## 🖥️ Interface

The app has a native desktop UI built with PyQt6 that displays:

- A real-time audio volume and waveform meter.
- The current screening score and what criteria they passed.
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

---

## 🚀 Getting started

(Project in beta)
Go to the [**Versions**](../../releases) page to download `.exe`;  no need to install it.

To run it from source or compile it yourself, see the full [README] (README.md).

---

## 📄 License

MIT: Use it, modify it, and share it freely.
