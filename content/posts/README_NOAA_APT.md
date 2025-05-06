---
title: "🛰️ NOAA APT Decoder Setup on macOS (RTL-SDR + CubicSDR + noaa-apt)"
date: 2025-05-06
tags: ["Space Weather", "NOAA APT", "Satellite Tech", "Systems Engineering", "Resilient Tech"]
---

This guide outlines how I successfully installed [`noaa-apt`](https://github.com/martinber/noaa-apt) on macOS, recorded NOAA satellite signals using CubicSDR and an RTL-SDR dongle, converted the audio files, and decoded the satellite image.

---

## 🚀 What You Need

- macOS system
- RTL-SDR USB tuner
- CubicSDR software
- Home-built V-Dipole antenna (or equivalent)
- Rust + GTK3 for building the decoder
- Python and `pydub` for WAV conversion (optional)

---

## 🔧 Step 1: Install Prerequisites

Install [Homebrew](https://brew.sh/) if not already installed:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Install Rust and GTK3:

```bash
brew install rust gtk+3
```

---

## 📥 Step 2: Clone and Build `noaa-apt`

```bash
git clone https://github.com/martinber/noaa-apt.git
cd noaa-apt
cargo build --release
```

To run the GUI:
```bash
./target/release/noaa-apt
```

To run from the terminal:
```bash
./target/release/noaa-apt path/to/file.wav
```

---

## 🎙️ Step 3: Record a Satellite Pass using CubicSDR

1. Tune to the correct NOAA frequency (e.g., 137.100 MHz for NOAA-19)
2. Set mode to **WFM**
3. Use **40 kHz bandwidth**, **manual gain (~35–45 dB)**
4. Record audio during the satellite pass (10–15 minutes)
5. Save the recording as WAV

---

## 🔁 Step 4: Convert WAV to Proper Format

If your WAV file is stereo or not 48kHz 16-bit mono, convert it using `pydub` in Python:

```python
from pydub import AudioSegment

audio = AudioSegment.from_wav("input.wav")
audio = audio.set_channels(1).set_frame_rate(48000).set_sample_width(2)
audio.export("converted.wav", format="wav")
```

Make sure the output is:
- **Mono**
- **16-bit PCM**
- **48,000 Hz sample rate**

---

## 🧠 Step 5: Decode with `noaa-apt`

```bash
./target/release/noaa-apt converted.wav
```

Optional flags:
- `--contrast 90`
- `--skip-start 30 --skip-end 60`

Example:
```bash
./target/release/noaa-apt converted.wav --contrast 90
```

The decoded image will be saved as `output.png` or similar.

---

## ✅ Tips

- Use [N2YO](https://www.n2yo.com) or [Heavens Above](https://www.heavens-above.com) to track NOAA passes
- Tune precisely to:  
  - NOAA-19: 137.100 MHz  
  - NOAA-15: 137.620 MHz  
  - NOAA-18: 137.9125 MHz  
- Ensure good antenna line-of-sight and RF quiet environment

---

## 📸 Example Output

![example](output.jpeg)

---

## 🧪 License

This setup guide is based on personal experimentation. Refer to the `noaa-apt` [GitHub license](https://github.com/martinber/noaa-apt/blob/master/LICENSE) for licensing terms related to the decoder.
