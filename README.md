# 🧾 Medical Report OCR using Ollama & Tesseract

This project extracts structured information from medical report images using **Tesseract OCR** and **Ollama's LLMs** (e.g., `llama3.2:3b`). The extracted data is saved as both plain text and structured JSON.

## 📁 Folder Structure

- `input_image/` – Place your medical report images here  
- `output/` – Processed outputs are stored here (`json/`, `text/`)  
- `main.py` – Main script to run the OCR and extraction pipeline  

---

## ⚙️ Setup Instructions

### 1. Install Tesseract OCR

- **Windows:**
  - Download from: https://github.com/UB-Mannheim/tesseract/wiki
  - During installation, ensure the "Add to PATH" option is selected
  - Verify installation by running:
    ```bash
    tesseract -v
    ```

### 2. Install Ollama

- Download and install from: https://ollama.com
- Run the local server:
  ```bash
  ollama serve
  ```
- Pull the required model:
  ```bash
  ollama pull llama3.2:3b
  ```

### 3. Clone Repository & Set Up Environment

```bash
git clone <your-repo-url>
cd <your-repo-folder>

# Create and activate virtual environment
python -m venv venv
venv\Scripts\activate        # For Windows
# OR
source venv/bin/activate     # For macOS/Linux

# Install dependencies
pip install -r requirements.txt
```

---

## 🖼️ Add Input Images

Place your medical report `.jpg`, `.jpeg`, `.png`, or `.tiff` images into the `input_image/` directory.

---

## 🚀 Run the Script

```bash
python main.py
```

- Extracts text using Tesseract OCR
- Processes text with Ollama LLM (locally)
- Saves:
  - Raw text as `.txt` in `output/text/`
  - Structured data as `.json` in `output/json/`
  - Error/debug logs in `output/debug/` (if enabled)

---



## 🧪 Notes

- Make sure both **Tesseract** and **Ollama** are properly installed and accessible via system PATH
- The model must be fully downloaded before processing begins

---
