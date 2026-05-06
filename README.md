# 🎵 Jarvis for Spotify

> Control Spotify with claps — no keyboard, no phone, no hands.

Developed by **Pandiah**.

---

## 🧠 What is this?

Jarvis for Spotify is a desktop app that listens to your microphone and lets you control Spotify using claps. Single clap to play or pause, double clap to skip to the next track. That's it.

It runs silently in the system tray and uses a smart audio detection algorithm to tell the difference between a real clap and background music, so it won't trigger accidentally while you're listening.

---

## 👏 How it works

| Action | Result |
|--------|--------|
| Single clap | Play / Pause |
| Double clap | Next track (or opens Spotify if closed) |

When you launch the app, it calibrates itself for 2 seconds to measure your room's ambient noise. After that it's always listening, always ready.

---

## 🔬 The detection algorithm

Most clap detectors fail when music is playing because they only compare raw volume levels — and loud music is just as loud as a clap. Jarvis solves this with a **spectral fingerprint** that scores each sound across 5 criteria:

1. **Transient onset** — claps are impulsive bursts, music is sustained
2. **High-frequency dominance** — claps concentrate energy above 2 kHz; bass and music don't
3. **Spectral flatness** — claps are broadband noise, musical notes are tonal
4. **Zero crossing rate** — claps oscillate much faster than voice or instruments
5. **Fast decay** — a clap fades quickly; sustained sounds don't

A sound needs to score **at least 4 out of 5** to be confirmed as a clap. This makes the detection reliable even in noisy environments or while music is playing loudly.

---

## 🖥️ Interface

The app has a native desktop UI built with PyQt6 that shows:

- A real-time audio waveform and volume meter
- The current detection score and which criteria passed
- A live activity log
- A sensitivity slider to tune detection to your environment
- A system tray icon so it stays out of the way

---

## ⚙️ Tech stack

- **Python** — core language
- **PyQt6** — desktop interface
- **PyAudio** — microphone input
- **NumPy** — audio signal processing and FFT analysis
- **PyAutoGUI** — media key simulation
- **PyInstaller** — packaging into a standalone `.exe`

---

## 📋 Requirements

- Windows 10 / 11
- Microphone (built-in or external)
- Spotify installed

---

## 🚀 Getting started

Head to the [**Releases**](../../releases) page to download the `.exe` — no installation needed.

To run from source or build it yourself, check the full [README](README.md).

---

## 📄 License

MIT — use it, modify it, and share it freely.
