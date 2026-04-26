# EM-224 ( honodori )
A browser‑based hybrid synthesizer and sequencer integrating FM, PSG, subtractive, and drum/PCM engines.
It features an FM sound source and PCM section inspired by the YM2608 (OPNA),
an AY-x-xxxx style PSG sound source (expanded), a calculated drum sound source,
a groovebox-like step sequencer similar to the TR recording method,
and also allows sequencing using the MML scripting.
(This contains Japanese text. Please translate it before porting it)

![screenshot](./images/screenshot.png)

---

## 🎹 Overview

**honodori** is a multi‑engine synthesizer and sequencer that runs entirely in the browser.  
It combines **FM**, **PSG**, **SUB (subtractive)**, and **DRM (drum + PCM loader)** sound sources,  
and supports both **GUI‑based composition** and **MML scripting**.

It is designed for chiptune creators, sound designers, and anyone exploring retro‑inspired electronic music.

---

## 🚀 Features

### 🔊 Hybrid Sound Architecture
- **SUB** — subtractive synthesis (SINE / SQUARE / SAW / TRIANGLE, ADSR, LPF/HPF)
- **FM** — 4‑operator engine with 8 algorithms(YM2608)  
  - Operator parameters: AR / DR / SR / RR / SL / TL / KS / MUL / DT  
  - Feedback, tone bank support
- **PSG** — AY‑style extended PSG  
  - Waveforms: SQ / SAW / TRI / SIN  
  - Detune, envelope types, LFO (wave / rate / depth / destination)
- **DRM** — drum engine 
  - 8 fixed drum sounds
- **PCM** — PCM loader  
  - 1 PCM channel  
  - PCM supports WAV/MP3 loading (6‑bit lo‑fi conversion)
  - Inspired by the ADPCM of the YM2608
  - Sampling rate 2kHz to 16kHz (16kHz is the default value)

---

## 🎼 Composition Modes

### **PATTERN Mode**
- 16/32‑step sequencer  
- Note, volume, pan, tie, step length ,Bpm
- Per‑engine parameter editing

### **SONG Mode**
- Arrange multiple patterns to build full tracks  
- Pattern chaining and structure editing

### **MML Mode**
- Supports note input (CDEFGAB), rests (R), note length, octave, tempo, velocity  
- PAN, TIE, tone selection  
- Partially MUCOM88 and FMP7 compatible syntax
- Executes independently from PATTERN/SONG modes
- Regarding the MML section, referred to the description methods found in the publicly available
documentation for MUCOM88(https://github.com/onitama/mucom88) and FMP7 (http://fmpdoc.fmp.jp/),
but was not able to reproduce all of them.

---

## 🥁 Drum MML

Drum channels support a dedicated MML syntax:

- `%KICK`, `%SNARE`, `%HHAT`, `%OH`, `%CH`, `%THTOM`, `%TMTOM`, `%TLTOM`
- `%PPCM` — play PCM sample
- Note length can be specified (`%KICK4`) or inherit the default `L` value

Example:%KICK4 %SNARE8 %HHAT16 %HHAT16 %PPCM4


---

## 🎛️ Effects & Mixer

- **Delay** (sync‑able)
- **Chorus**
- **DJ Filter** (LPF / HPF)
- Per‑engine **PAN** and **GAIN**

---

## 💾 Save & Load

- Projects can be saved and loaded directly in the browser  
- No installation required

---

## 📂 Project Structure

honodori_synth.html     - main application

---

## 🧪 Demo

Live demo:  
https://ufotone.github.io/github.io/

Open index.html in your browser.
No build step required.

---
## 📜 License
Important point: MUCOM88 is based on under CC BY-NC-SA 4.0.
and the license information found at https://github.com/onitama/mucom88.
This project aka honodori(EM-224) does not include those codes.

This project is released under the CC0 1.0 Universal (Public Domain Dedication).
To the extent possible under law, 
the author has waived all copyright and related or neighboring rights to this work.
You are free to copy, modify, distribute, and use the project for any purpose, 
including commercial use, without asking permission.
https://creativecommons.org/publicdomain/zero/1.0/

---



