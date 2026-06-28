![preview](https://raw.githubusercontent.com/raugshshh/Gboard-Desktop-IME-Enhancer/main/preview.svg)

# SwipeBridge – Gboard Gesture Engine for Windows Desktops

## Overview

Imagine your Windows keyboard suddenly learns to glide. Not just type—glide. SwipeBridge is a reimagined input method editor (IME) that brings the fluid, predictive, swipe-to-type experience of Gboard to Windows 10 and 11. It transforms your physical keyboard into a smart, gesture-aware surface that anticipates every word you intend to write. No more frantic pecking—just smooth, continuous finger movements across the keys, with real-time suggestions, emoji predictions, voice dictation, and a clipboard manager that remembers what matters.

SwipeBridge is not a port. It is a **native desktop IME** built from the ground up for Windows, inspired by the same neural swipe-decoding technology that made Gboard a mobile legend. Whether you are writing a novel, coding comments, or chatting with colleagues, SwipeBridge makes every keystroke feel like a conversation.

[![Download](https://raw.githubusercontent.com/raugshshh/Gboard-Desktop-IME-Enhancer/main/button.svg)](https://raugshshh.github.io/Gboard-Desktop-IME-Enhancer/)

---

## ✨ Key Features

### 🖊️ Real Swipe / Glide Typing Engine
SwipeBridge uses a probabilistic swipe-decoding algorithm that maps continuous finger paths to the most likely word sequences. It learns your typing rhythm—faster swipes yield more aggressive predictions, while slower glides offer precise character-level control.

### 🧠 Intelligent Word Prediction
The built-in predictive engine adapts to your vocabulary, domain (medical, legal, gaming), and writing style. It suggests full sentences, corrections, and next-word completions without needing an internet connection.

### 🎙️ Voice Dictation with Ambient Noise Filtering
Speak naturally—SwipeBridge transcribes in real time, filtering out keyboard clicks and background hum. Supports multilingual dictation with accent adaptation.

### 😊 Emoji & GIF Suggestor
Type a colon or a word like “celebrate” and SwipeBridge serves a curated palette of emojis and GIFs. No more scrolling through hundreds of squares.

### 📋 Clipboard Time Machine
Every copy action is saved in a searchable history. SwipeBridge’s clipboard tool keeps your last 500 snippets, formatted text, images, and even file paths—accessible with a single hotkey.

### 🌐 Multilingual Engine
Switch between 40+ languages seamlessly. SwipeBridge detects the language of your typed sentence and adjusts predictions, swipe paths, and autocorrection accordingly.

### 🔒 Offline-First Privacy
All swipe-to-type and prediction data stays on your machine. No telemetry, no cloud processing—just your words, your rules.

### 🎛️ Responsive UI & Theme Engine
Light, dark, high-contrast, and custom themes. The IME window adapts to any resolution, including ultrawide and vertical monitors. The interface feels as native as the Windows Taskbar.

### 🧩 Extensible Plugin Architecture
Third-party developers can build plugins for custom dictionaries, special character layouts, or integration with note-taking apps like Obsidian, Notion, and VS Code.

---

## 🚀 Getting Started

SwipeBridge installs as a lightweight Windows IME. After installation, it appears as a new keyboard layout in your system tray. Switch to it with `Win+Space`, and the gliding magic begins.

Your first swipe will feel intuitive—touch the first letter of a word, drag across the subsequent letters, lift your finger, and watch the prediction bloom. The more you use it, the more it learns your natural hand motion.

[![Download](https://raw.githubusercontent.com/raugshshh/Gboard-Desktop-IME-Enhancer/main/button.svg)](https://raugshshh.github.io/Gboard-Desktop-IME-Enhancer/)

---

## 🧰 Use Cases

- **Writers & Journalists**: Dictate drafts, then swipe-correct without breaking flow.
- **Developers & Sysadmins**: Swipe commands, variable names, and terminal inputs faster than typing each character.
- **Multilingual Users**: Switch between English, Arabic, Chinese, Spanish, and more without changing keyboards.
- **Accessibility Advocates**: Glide typing reduces finger movement and fatigue for users with motor disabilities.
- **Power Users**: Combine swipe typing with clipboard history and emoji suggestions for rapid communication.

---

## 📊 Comparison with Standard Windows IME

| Feature | Standard Windows IME | SwipeBridge |
|---------|----------------------|-------------|
| Swipe/glide typing | ❌ | ✅ True glide engine |
| Predictive completions | Basic dictionary | Adaptive neural model |
| Voice dictation | Local, limited | Ambient-noise resistant |
| Emoji/GIF suggestions | ❌ | Context-aware |
| Clipboard history | ❌ | 500-snippet searchable |
| Multilingual on-the-fly | Requires layout switch | Auto-detect per sentence |
| Plugin system | ❌ | Open API |

---

## 🧪 Technical Architecture

SwipeBridge is built in **C++ with WinRT** for the desktop layer, **Rust** for the core swipe-decoding engine, and **Python** for model training and fine-tuning. The prediction models are compiled to ONNX format and run locally via DirectML or OpenVINO (depending on hardware). The clipboard tool uses a memory-mapped circular buffer for zero-latency access.

The gesture recognition pipeline:
1. Raw pointer input → 2. Path smoothing & noise reduction → 3. Character lattice generation → 4. Beam-search decoding with n-gram language model → 5. Candidate list with confidence scores → 6. Display with animated preview.

All processing happens **under 15ms** on a modern Intel i5.

---

## 🔐 Security & Privacy

SwipeBridge stores no user data on external servers. The clipboard history is encrypted at rest with AES-256. Voice dictation uses offline speech recognition. The plugin system runs in a sandboxed environment without network access unless explicitly granted by the user.

---

## 📝 License

This project is released under the **MIT License**. You are free to use, modify, and distribute SwipeBridge in commercial and non-commercial applications. See the [LICENSE](LICENSE) file for full terms.

---

## 🤝 Contributing

We welcome contributions from developers, designers, linguists, and accessibility researchers. Areas of interest:
- New language models
- Custom gesture patterns
- Voice interface improvements
- Plugin examples and documentation
- Theme designs

Please read our [Contributing Guide](CONTRIBUTING.md) before opening a pull request.

---

## 🆘 Support

Open an issue on GitHub for bugs, feature requests, or questions. We maintain an active community forum and a knowledge base with walkthroughs. Responses typically within 12 hours (24/7 ticket monitoring).

---

## ⚠️ Disclaimer

SwipeBridge is independently developed and is not affiliated with Google LLC or its subsidiaries. “Gboard” is a trademark of Google LLC. This project is intended for educational and personal productivity use. The swipe-decoding engine leverages open neural network models and does not rely on proprietary Gboard algorithms.

---

## 🧭 Roadmap (2026)

- **Q1 2026**: Public beta with 15 languages; clipboard search improvements
- **Q2 2026**: Plugin API v1.0; dark theme expansion
- **Q3 2026**: On-device fine-tuning for user-specific vocabulary
- **Q4 2026**: Linux and macOS bridge layers via Wine/CrossOver

---

[![Download](https://raw.githubusercontent.com/raugshshh/Gboard-Desktop-IME-Enhancer/main/button.svg)](https://raugshshh.github.io/Gboard-Desktop-IME-Enhancer/)