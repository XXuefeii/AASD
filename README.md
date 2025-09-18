# AASD — Spontaneous Auditory Attention Switching Dataset (EEG & Eye-Tracking)

**Detailed Introduction and Sample Data**

> A multimodal dataset for **spontaneous auditory attention switching**, recorded with **64-channel EEG** and **EyeLink Portable Duo** under **natural, unconstrained conditions**.

---

## 📌 Highlights
- **Spontaneous attention switches** (spontaneous; no external cues), with **keypress** annotations of switch moments  
- **Two spatialized talkers at ±90°**, randomized blocks, **60 s** per trial  
- **Synchronized raw signals**: 64-ch **EEG (500 Hz)** + **eye-tracking data**  
- **Natural eye movements**: no fixation targets, no gaze-contingent tasks; **head only stabilized** for capture range  
- **~18 hours** of simultaneous EEG and eye-tracking across participants  
- **Reproducible preprocessing pipeline** (artifact removal, **downsample to 128 Hz**, **0.1–45 Hz** bandpass)

---

## 🧭 Table of Contents
- [Dataset at a Glance](#sec-dataset-at-a-glance)
- [Experimental Protocol](#sec-experimental-protocol)
  - [Participants](#sec-participants)
  - [Stimuli & Task](#sec-stimuli-task)
  - [Recording Environment](#sec-recording-environment)
- [Recordings](#sec-recordings)
  - [EEG](#sec-eeg)
  - [Eye-tracking](#sec-eye-tracking)
  - [Synchronization](#sec-synchronization)
- [Preprocessing Pipeline](#sec-preprocessing)
- [Figure](#fig-1)
- [Ethics](#sec-ethics)
- [Citation](#sec-citation)

---

## 📊 Dataset at a Glance
| Item | Details |
|---|---|
| Participants | 18 native Chinese young adults (18–27 years), clinically normal hearing |
| Duration | ~18 hours (EEG + eye-tracking, simultaneous) |
| Task | Spontaneous auditory attention switche; **keypress** marks the switch moment |
| Trials | 60 per participant (6 blocks × 10 trials), **60 s** each; **block order randomized** |
| Stimulus Layout | Two spatialized speech streams at **+90°** and **−90°** *(see [Fig. 1](#fig-1))* |
| Speech Materials | AISHELL corpus (3 male, 3 female talkers) |
| Audio Level | 65 dB SPL (binaural earphones) |
| Environment | Double-walled acoustically shielded room |
| Modalities | 64-ch EEG (500 Hz); EyeLink Portable Duo |

---

## 🧪 Experimental Protocol

### Participants
Eighteen native Chinese young adults (ages 18–27) with clinically normal hearing.

### Stimuli & Task
- Spatialized speech streams (AISHELL; three male and three female talkers) presented from **+90°** and **−90°**, **as shown in [Fig. 1](#fig-1)**.  
- Each participant completed **60 trials** (6 blocks × 10 trials; **60 s** per trial); **block order randomized**.  
- During each trial, participants **switched attention at self-chosen moments without external cues** and pressed a key to mark the switch.  
- Short breaks were provided between trials to reduce fatigue and support sustained engagement.

### Recording Environment
- Double-walled acoustically shielded room.  
- Binaural stimuli via earphones at **65 dB SPL**.  
- Presentation timing and event logging were controlled by a standard experiment platform.

---

## 📡 Recordings

### EEG
- **64 scalp electrodes**, sampled at **500 Hz**.  
- **Left and right mastoids** served as references; **an additional online reference at the nose** was used to **ensure consistent channel referencing**.  
- Electrode impedances were maintained **< 5 kΩ**.  
- Participants were instructed to minimize body movement to limit motion-related contamination.

### Eye-tracking
- Recorded concurrently with an **EyeLink Portable Duo** under **natural, unconstrained conditions**.  
- **No fixation targets** were displayed and **no gaze-contingent cues/instructions** were given.  
- **Head position stabilized only** to keep the face within the tracker’s capture range; participants were **free to blink and move their eyes normally**.  
- Before the session, a **standard nine-point calibration** and a brief validation were performed on the stimulus display.  
- Display resolution: **1024 × 768 px**. Screen coordinates were **pixel-based** with the origin at **(0,0)** (top-left) and the center at **(512,384)**, **as illustrated in [Fig. 1](#fig-1)**.  
- During the experiment, the device streamed multiple eye-movement parameters at its native sampling rate, including **raw 2D gaze positions** \((x,y)\), **saccade velocities**, **pupil diameter**, and **blink events**, etc.

### Synchronization
- EEG and eye-tracking were **synchronized using shared triggers and a common timestamping scheme**, ensuring precise temporal alignment of **raw neural signals** and **comprehensive eye-tracking data** around the **keypress-defined attention switches**.

---

## 🛠️ Preprocessing Pipeline
For reproducibility, we provide a standard pipeline that:
1. **Removes artifacts**  
2. **Downsamples EEG to 128 Hz**  
3. **Applies a 0.1–45 Hz bandpass filter** 

---

## 🖼️ Figure

<a id="fig-1"></a>
<figure>
  <img
    src="https://github.com/user-attachments/assets/61c35225-91ef-4768-b07b-b924da4e4b4c"
    alt="Dataset overview and experimental layout"
    width="100%" />
  <figcaption><strong>Figure 1.</strong> Dataset overview and experimental layout.</figcaption>
</figure>

---

## 🧑‍⚖️ Ethics
This work involved human participants. Approval for all ethical and experimental procedures was granted by the **Institutional Review Board (IRB) of the Southern University of Science and Technology** (Protocol ID: **2022DZX003**).

---

## 📚 Citation

```bibtex
@inproceedings{Bu2017Aishell,
  title={Aishell-1: {A}n open-source mandarin speech corpus and a speech recognition baseline},
  author={Bu, H. and Du, J. and Na, X. and Wu, B. and Zheng, H.},
  booktitle={Proceedings of the 20th International Coordinating Committee on Speech Databases and Speech I/O Systems and Assessment (O-COCOSDA)},
  pages={1--5},
  year={2017}
}
