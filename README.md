# 🌱 Seeds of Science — QR Code Generator

A free, **100% offline**, **privacy-first** QR code generator built as a Year 2 entry for the **Science Talent Search 2026** under the theme *"Seeds of Science – Nurturing knowledge for all."*

Designed to teach kids (and curious adults!) how QR codes actually work — the finder patterns, timing patterns, alignment patterns, Reed-Solomon error correction, and masking — by letting you experiment with all of them in your browser.

> **No data ever leaves your computer.** No tracking. No analytics. No internet required after download.

---

## 🌻 Why "Seeds of Science"?

A QR code is like a **seed**: small, square-ish, and packed with hidden information that "grows" into something useful when scanned. This project plants the seed of how QR codes work, so anyone can dig in and explore.

---

## ✨ Features

- 🔒 **Completely offline & private** — runs entirely in your browser, no server, no tracking
- 🎨 **Live QR preview** — generates instantly as you type
- 🛡️ **Error correction levels** — choose L, M, Q, or H and watch the QR code change
- 🎭 **All 8 mask patterns** — preview each one and see its penalty score
- ⭐ **Auto mode** — automatically picks the lowest-penalty mask (the ISO-standard way)
- 🖼️ **Add your own logo** — drop an image into the centre of your QR code
- 🎨 **Custom colours** — change foreground and background to match your style
- 💾 **Download as PNG or SVG** — save and share your codes
- 📚 **Educational** — every option shows you *why* it matters

---

## 🚀 How to use it

### Option 1: Just open it
1. Download `sts_2026_ada_qr_code_generator.html`
2. Double-click to open it in any modern browser (Chrome, Firefox, Edge, Safari)
3. That's it — no install, no setup, no internet needed

### Option 2: Clone it
```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
# Open the HTML file in your browser
```

---

## 🔬 What you can experiment with

### 🛡️ Error Correction (Reed-Solomon)
Try switching between **L (7%)**, **M (15%)**, **Q (25%)**, and **H (30%)**:
- Lower levels = smaller QR code, less damage tolerance
- Higher levels = bigger QR code, can survive more scratches/coffee spills
- Try printing one, scribbling on it, and see if your phone can still scan it!

### 🎭 Mask Patterns
Click any of the 8 mask patterns to see how they "scramble" the QR code differently. The **penalty score table** shows you exactly *why* the standard prefers one over another:

- ⭐ **Lowest score wins** — that's the most balanced, scanner-friendly pattern
- The score checks for long stripes, big solid blocks, fake "finder pattern" lookalikes, and overall black/white balance
- Switch to **Auto** to let the generator pick the best one for you

### 🖼️ Logos
Drop a logo into the centre — the high error correction handles the missing data so the QR code still scans. Try:
- A small logo with **L** error correction (might break)
- The same logo with **H** error correction (works fine!)

This is the magic of Reed-Solomon error correction in action.

---

## 🧠 The science behind a QR code

| Part | What it does |
|------|--------------|
| **Finder patterns** (3 corner squares) | Tell the scanner *"I'm a QR code"* and which way is up |
| **Timing pattern** (dotted line) | A ruler that shows the size of each module |
| **Alignment pattern** (small square-in-square) | Helps scanners read curved or wrinkled QR codes |
| **Reed-Solomon error correction** | Backup data that lets the QR survive damage |
| **Masking** | Scrambles the squares to avoid confusing patterns |
| **Format info** | Stores which error correction level and mask were used |

---


## 🛠️ Tech stack

- **Pure HTML, CSS, and vanilla JavaScript** — no frameworks, no build step
- [`qrcodejs`](https://github.com/davidshimjs/qrcodejs) for the initial QR matrix generation
- Custom Reed-Solomon-aware re-masking logic (so the chosen mask matches the ISO penalty scoring)
- All processing happens in your browser — no backend, no API calls

---

## 📂 File structure

```
.
├── sts_2026_ada_qr_code_generator.html   # The whole app — single file!
└── README.md                             # You are here 🌱
```

That's it. One file. Self-contained. Runs anywhere.

---

## 🎓 Made for Science Talent Search 2026

This project is part of a Year 2 entry for the **Science Talent Search 2026** under the theme **"Seeds of Science."**

The accompanying video explains:
- The anatomy of a QR code (finder, timing, alignment patterns)
- Reed-Solomon error correction
- Mask patterns and why they matter
- How a message becomes a grid of black-and-white squares

Watch it, play with this tool, and plant your own seed of science! 🌻

---

## 🤝 Contributing

Found a bug? Have an idea? Open an issue or a pull request — just be kind, this was made by a Year 2 student!

---

## 📜 License

MIT — free to use, share, remix, and learn from.

---

*Thank you for checking out my Seeds of Science project!* 🌱
