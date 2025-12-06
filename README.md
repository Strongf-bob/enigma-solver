<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" style="height:64px;margin-right:32px"/>

# 🔐 Enigma Bombe Solver

> A modern software simulation of Alan Turing's legendary Bombe machine — breaking Enigma encryption through cryptanalysis

***

## 📖 Overview

This project is an **interactive cryptography simulator** that demonstrates how the Enigma machine worked and how the Bombe algorithm cracked it during WWII.


| Feature | Description |
| :-- | :-- |
| 🔐 **Enigma Simulation** | Authentic 3-rotor encryption machine with historical wiring |
| 🎯 **Bombe Cracking** | Brute-force cryptanalysis using known plaintext attacks |
| 🌐 **Web Interface** | No installation needed — just open `index.html` in a browser |
| 📚 **Educational** | Learn about cryptography, algorithms, and computing history |


***

## 🚀 Quick Start

**Just open `index.html` in your web browser — that's it!**

No Python installation, no server setup required. The entire application runs directly in your browser.

```
enigma-bombe-project/
├── 📄 index.html           ← Open this in your browser!
├── README.md               ← This file
├── enigma.py               ← Python Enigma implementation (optional)
├── bombe.py                ← Python Bombe solver (optional)
└── rotor_configs.py        ← Historical rotor configurations
```


***

## 🎮 Features

### 🔐 Enigma Encryption Tab

- **Configure rotor settings** (III, II, I)
- **Set rotor positions** (AAA to ZZZ)
- **Optional plugboard** for advanced encryption
- **Real-time encryption** of plaintext to ciphertext


### 🎯 Bombe Cracking Tab

- **Input ciphertext** you want to crack
- **Provide known plaintext** (crib) fragment
- **Specify crib position** in the message
- **Find matching rotor settings** automatically
- **View all valid solutions** instantly


### 📖 Instructions Tab

- **Step-by-step guide** with examples
- **Historical context** about the Enigma machine
- **Tips for using** the simulator effectively

***

## 💡 How It Works

### Enigma Machine 🔄

The encryption signal flows through:

```
Plain Text
    ↓
┌─────────────┐
│  Plugboard  │  (optional letter swap)
└──────┬──────┘
       ↓
┌─────────────────────────────────────┐
│  Rotor I → Rotor II → Rotor III     │  (character substitution)
│              ↓                       │
│         Reflector ←                 │  (bounces signal back)
└──────┬────────────────────────────┘
       ↓
┌─────────────┐
│  Plugboard  │  (swap back)
└──────┬──────┘
       ↓
 Cipher Text
```

Each rotor contains **26 internal wiring connections** that scramble the signal. The rotors rotate with each keystroke, creating an enormously complex encryption system.

### Bombe Algorithm 🎯

The Bombe exploits weaknesses by testing combinations:

1. **Take a known plaintext fragment** (crib) — e.g., "HELLO"
2. **Try all 17,576 rotor positions** (26³)
3. **For each position**, check if encrypting the crib produces the matching ciphertext
4. **Return matching settings** that successfully decrypt the message

**Complexity:** O(n) where n = 17,576 rotor position combinations

***

## 📊 Example: Encrypt \& Crack

### Encryption Example

| Setting | Value |
| :-- | :-- |
| **Rotors** | III, II, I |
| **Positions** | `AAA` |
| **Plaintext** | `HELLOWORLD` |
| **Ciphertext** | `EEMLKMNFMQ` |

### Cracking Example

| Input | Value |
| :-- | :-- |
| **Ciphertext** | `XQYTUHWQD` |
| **Known Plaintext (Crib)** | `HELLO` |
| **Crib Position** | `0` |
| **Found Settings** | Rotors III, II, I @ `BEF` ✓ |


***

## 🔧 Technical Details

### Historical Rotor Wirings

Based on **actual German Enigma machines**:

```
Rotor I:        EKMFLGDQVZNTOWYHXUSPAIBRCJ
Rotor II:       AJDKSIRUXBLHWTMCQGZNPYFVOE
Rotor III:      BDFHJLCPRTXVZNYEIWGAKMUSQO
Reflector:      YRUHQSLDPXNGOKMIEBFZCWVJAT
```


### Performance Metrics

| Metric | Value |
| :-- | :-- |
| **Search Space** | 17,576 positions |
| **Time per check** | O(1) constant |
| **Total positions** | 26³ |
| **Rotor combinations** | 6 (3!) |
| **Max configurations** | 105,456 |


***

## 📚 Educational Value

This simulator teaches:

- ✅ **Cryptography fundamentals** — how encryption algorithms work
- ✅ **Cryptanalysis techniques** — breaking codes using weaknesses
- ✅ **Algorithm optimization** — efficient brute-force searching
- ✅ **Computing history** — early automated cryptanalysis machines
- ✅ **Mathematical logic** — rotor stepping and signal flow

***

## 🏛️ Historical Context

> **Alan Turing and the Bletchley Park team** (1940–1945)

The original **Bombe machine** was an **electromechanical device** that could test hundreds of rotor configurations per second. This breakthrough was **crucial to WWII intelligence** and is considered one of the **earliest examples of large-scale automated cryptanalysis**.

The Enigma was thought **unbreakable** by the Nazis, but the Bombe proved them wrong. The intelligence gained from breaking Enigma is estimated to have **shortened WWII by several years**.

***

## 🔗 Repository

📍 **GitHub:** [github.com/Strongf-bob/enigma-solver](https://github.com/Strongf-bob/enigma-solver)

***

## 👤 Author

| Field | Details |
| :-- | :-- |
| **Name** | Karsakov Ilya Vyacheslavovich |
| **Year** | 2025 |
| **GitHub** | [@Strongf-bob](https://github.com/Strongf-bob) |
| **Email** | karsakovillya@yandex.ru |
| **Telegram** | [@nicto999](https://t.me/nicto999) |


***

## 📜 License

This is an **educational project** created for **portfolio purposes**. Use freely for learning and teaching cryptography!

***

## 📖 References

1. **Turing, A. M.** (1936). *"On Computable Numbers"* — Proceedings of the London Mathematical Society
2. **Welchley, G.** (1946). *"From Polish Bomba to British Bombe"* — History of Computing Project
3. **Gannon, P.** (2006). *"Colossus: Bletchley Park's Greatest Secret and the Birth of the Modern Computer"*
4. **The National Museum of Computing** — *"The Enigma Machine and the Bombe"*

***

## 🤝 Contribute \& Contact

Found a bug? Have an improvement idea? Feel free to reach out:

- 💬 **Telegram:** [@nicto999](https://t.me/nicto999)
- 📧 **Email:** karsakovillya@yandex.ru
- 💻 **GitHub:** [Strongf-bob](https://github.com/Strongf-bob)

***

<div align="center">

**Decrypting History, One Rotor at a Time** 🔐

*Learn cryptography by breaking the unbreakable.*

</div>
<span style="display:none">[^1][^2]</span>

<div align="center">⁂</div>

[^1]: https://github.com/Strongf-bob/enigma-solver

[^2]: README.md

