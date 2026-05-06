
# Jarvis-For-Spotify
Jarvis for spotify is that you can use spotify hands-free without touching anything /1# 🎵 Jarvis for Spotify

Control Spotify with claps. No keyboard, no phone — just clap.

Developed by **Pandiah**.

---

## ✨ What does it do?

| Action | Result |
|--------|--------|
| 👏 Single clap | Play / Pause |
| 👏👏 Double clap | Next track (or opens Spotify if it's closed) |

---

## ⚡ How to use

> 🎙️ **Important — before opening the program:** make sure your microphone is active and unblocked. If you use any software to mute or block your microphone (system privacy settings, audio control apps, etc.), disable it before running Jarvis. When it starts, the program runs an **automatic 2-second calibration** to measure ambient noise — if the microphone is blocked at that moment, the calibration will fail and clap detection won't work correctly.

1. Open Spotify
2. Make sure your microphone is ready and unblocked
3. Run `Jarvis for Spotify.exe`
4. Wait 2 seconds while the program calibrates
5. Done! Clap to control Spotify

> ⚠️ Windows may show a SmartScreen warning the first time. Click **"More info" → "Run anyway"**.

---

## 📋 Requirements

- Windows 10 / 11
- Microphone (built-in or external)
- Spotify installed

---

## 🔬 How does clap detection work?

The detector uses a **spectral fingerprint** with 5 criteria to distinguish claps from music:

1. **Transient onset** — the sound must be impulsive, not sustained
2. **High-frequency dominance** — claps concentrate energy above 2 kHz
3. **Spectral flatness** — claps are broadband noise, not musical tones
4. **Zero crossing rate** — claps have very rapid oscillations
5. **Fast decay** — the second half of the sound must be quieter than the first

At least **4 out of 5 points** are required to confirm a clap. This prevents music or voice from accidentally triggering actions.

---

## 📄 License

MIT — use it, modify it, and share it freely.
 clap = play and pause /2 claps with spotify closed = open spotify / with spotify open = next song
