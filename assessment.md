# 🎹 Cadence Chord Trainer: Honest Assessment & Roadmap

This document provides a comprehensive, honest assessment of **Cadence** as a piano chord recall and ear training tool. It outlines the tool's core cognitive strengths, current limitations, and proposes a roadmap of high-value feature recommendations.

---

## 🌟 Overall Assessment

**Cadence is an exceptional tool for intermediate-to-advanced musicians looking to build rapid chord symbol recall, interval visualization, and basic ear training.** 

Unlike generic flashcard apps, its fluid, keyboard-driven workflow, real-time visual keyboard confirmation, and intelligent repetition systems make it a highly productive training companion. By targeting *active recall* rather than passive recognition, it helps bridge the gap between reading a lead sheet and executing a chord on the keyboard.

### Key Strengths
1. **Frictionless Keyboard Interface:** The addition of instant-grade shortcuts (`G` and `W`) alongside the `Spacebar` workflow means a pianist can keep their hands on their instrument or a laptop and drill 50+ chords in minutes without touching a trackpad.
2. **Cognitively Sound Repetition:** The **Focused Pool Mode** and **Spaced Repetition** (re-injecting failed chords at a 30% rate) directly mirror modern memory-science techniques. It prevents cognitive overload and ensures that weak spots are addressed immediately.
3. **High-Quality Aesthetics and Sound:** The UI feels premium, using modern typography, glassmorphism, and subtle CSS animations. The synth engine uses triangle waves with a dynamic lowpass sweep, making the audio pleasant and realistic (resembling a warm electric piano), which prevents auditory fatigue.
4. **Actionable Post-Session Analytics:** The aggregated attempt chart (`[✔][✘][✘]`) sorted from lowest to highest success rate provides immediate, clear diagnosis of which harmony colors (e.g., altered dominants vs. half-diminished chords) require targeted study.

---

## ⚠️ Current Limitations

While excellent, the app currently has a few constraints that limit its potential as a comprehensive professional training platform:

1. **No Real-Time Verification (Passive Input):** The app relies on self-grading. It cannot verify if the user *actually* played the correct notes on their physical piano.
2. **Closed Block Voicings Only:** The inversion generator uses a strict mechanical formula (shifting notes up by 12 semitones). While mathematically correct, it only generates closed-position block chords. Real piano playing relies on open voicings, shell voicings, and smooth voice-leading.
3. **Chords in Isolation:** Music happens in progressions. Practicing an isolated `C7alt` followed by `Dbmaj` does not train the muscle memory for voice-leading (e.g., how the 7th of one chord resolves to the 3rd of the next in a `ii-V-I` progression).

---

## 🚀 Suggested Improvements & New Functionality

To elevate Cadence from a high-quality utility to a state-of-the-art interactive training ecosystem, the following additions are recommended:

### 1. Web MIDI API Integration (Game Changer)
* **What it is:** Let users connect their digital piano or keyboard to their computer using a USB/MIDI cable.
* **Why it matters:** The app can listen to the incoming MIDI notes and automatically grade the user in real-time when they play the correct shape. This changes the experience from *self-evaluation* to *interactive verification*.
* **Implementation difficulty:** Moderate. The Web MIDI API is built into modern browsers (Chrome, Edge, Opera) and is easy to query.

### 2. Chord Progressions & Voice-Leading Mode
* **What it is:** Practice chords in sequence (e.g., a `ii - V - I` progression in G Major: `Am7` -> `D7` -> `Gmaj7`).
* **Why it matters:** It trains the hands to find the most efficient path between chords (voice-leading), moving the fingers as little as possible. For example, keeping the common tones and moving other notes by step.
* **Feature detail:** The visual keyboard would show you how the notes resolve from the first chord shape directly to the next.

### 3. Jazz Voicings Generator
* **What it is:** Expand the keyboard generator beyond basic inversions to support standard piano voicing techniques:
  * **Rootless A/B Voicings:** Standard jazz chords played without the root (leaving room for the bass player).
  * **Drop-2 Voicings:** Shifting the second-highest note down an octave for an open, lush sound.
  * **Shell Voicings:** Just playing the Root, 3rd, and 7th (left hand) while playing melodies or extensions in the right hand.

### 4. Custom Session Playlists / Presets
* **What it is:** Save your custom practice configurations as presets.
* **Why it matters:** Users can create custom drills like *"Altered Dominant Workout,"* *"Standard Jazz Triads,"* or *"Minor Key Ear Trainer"* and launch them with a single click, saving setup time.

### 5. "Beat the Clock" Time Attack Mode
* **What it is:** A gamified mode where the user tries to recall and grade as many chords as possible within 60 seconds.
* **Why it matters:** Forces the brain to skip intellectualizing the notes and rely purely on instant muscle memory.

---

## 📈 Suggested Roadmap

| Phase | Feature | Complexity | Cognitive Value |
| :--- | :--- | :---: | :---: |
| **Phase 1** | Save Config Presets / Session Custom Playlists | Low | Medium |
| **Phase 2** | Web MIDI Integration (Automatic Note Verification) | Medium | **High** |
| **Phase 3** | Progression & Voice-Leading Workout Mode | High | **High** |
| **Phase 4** | Advanced Jazz Voicings (Drop-2, Rootless) | High | Medium |
