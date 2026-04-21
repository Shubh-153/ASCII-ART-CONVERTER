# 🎨 ASCII Art Converter

> Transform images and text into stunning ASCII art with ease!

---

## 📖 Description

**ASCII Art Converter** is a tool that converts regular images or text into ASCII art — a form of visual art that uses printable characters from the ASCII standard to represent pictures and designs.  Whether you want to convert a photo into a text-based masterpiece or generate decorative text banners, this project has you covered.

ASCII art has a long history in computing culture, dating back to the early days of text-only terminals and bulletin board systems (BBS). This converter brings that retro aesthetic into the modern era with a simple, intuitive interface.

---

## ✨ Features

- 🖼️ **Image to ASCII** — Convert any image (PNG, JPG, etc.) into ASCII art composed of characters that match the brightness of each pixel.
- 🔤 **Text to ASCII Banner** — Transform plain text into large, stylised ASCII banners using a variety of fonts.
- 🎨 **Adjustable Output Width** — Control the width (in characters) of the generated ASCII art to fit any display.
- 🌗 **Greyscale & Colour Modes** — Generate classic greyscale ASCII art or ANSI colour-coded output for supported terminals.
- 📋 **Copy to Clipboard** — Instantly copy the generated ASCII art for use anywhere.
- 💾 **Save to File** — Export your ASCII art as a `.txt` file.

---

## 🖥️ Demo

```
  ____  ____  ____ ___ ___      _    ____ _____    ____ ___  _   ___     _______ ____ _____ _____ ____
 / ___||  _ \|  _ \_ _|_ _|    / \  |  _ \_   _|  / ___/ _ \| \ | \ \   / / ____|  _ \_   _| ____|  _ \
| |    | |_) | |_) | | | |    / _ \ | |_) || |   | |  | | | |  \| |\ \ / /|  _| | |_) || | |  _| | |_) |
| |___ |  _ <|  __/| | | |   / ___ \|  _ < | |   | |__| |_| | |\  | \ V / | |___|  _ < | | | |___|  _ <
 \____||_| \_\_|  |___|___| /_/   \_\_| \_\|_|    \____\___/|_| \_|  \_/  |_____|_| \_\|_| |_____|_| \_\
```

---

## 🚀 Getting Started

### Prerequisites

Make sure you have the following installed:

- **Python 3.8+** (or the runtime relevant to the project)
- **pip** (Python package manager)

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/Shubh-153/ASCII-ART-CONVERTER.git
   cd ASCII-ART-CONVERTER
   ```

2. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

---

## 📚 Usage

### Convert an Image to ASCII Art

```bash
python converter.py --image path/to/image.png --width 100
```

### Convert Text to an ASCII Banner

```bash
python converter.py --text "Hello World" --font slant
```

### Save Output to a File

```bash
python converter.py --image path/to/image.png --output result.txt
```

### Available Options

| Option | Description | Default |
|--------|-------------|---------|
| `--image` | Path to the input image file | — |
| `--text` | Text string to convert to ASCII banner | — |
| `--width` | Output width in characters | `80` |
| `--font` | ASCII banner font (e.g. `slant`, `banner`, `block`) | `standard` |
| `--output` | Path to save the output `.txt` file | prints to terminal |
| `--color` | Enable ANSI colour output in the terminal | `false` |

---

## 🛠️ Technologies Used

- **Python** — Core language
- **Pillow (PIL)** — Image processing and pixel manipulation
- **pyfiglet** — Text-to-ASCII-banner conversion
- **colorama** — Cross-platform ANSI colour support in the terminal

---

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. **Fork** the repository
2. Create a new feature branch: `git checkout -b feature/your-feature-name`
3. Make your changes and commit them: `git commit -m "Add your feature"`
4. Push to your branch: `git push origin feature/your-feature-name`
5. Open a **Pull Request** and describe your changes

Please make sure your code follows the existing style and all tests pass before submitting.

---

## 📝 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 🙋 Author

Made with ❤️ by [Shubh-153](https://github.com/Shubh-153)

---

*If you found this project useful, please consider giving it a ⭐ on GitHub!*
