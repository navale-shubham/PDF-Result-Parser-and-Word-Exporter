# PBL-II Project: PDF Result Parser & Word Exporter

A Desktop GUI application built with **PySide6** that extracts academic results/marksheets from PDF files and exports structured student grade data into Microsoft Word (`.docx`) tables.

---

## 🚀 Features

- **PDF Parsing**: Automatically extracts student names, course names, and detailed mark distributions (ISE, ESE, TW, PR, OR, TUT, Total, Grade, etc.) using `pdfplumber` and custom regular expressions.
- **Interactive Course & Score Selection**: View available courses and select specific score types to export.
- **Multithreaded Processing**: Keeps the UI responsive during file processing and data export using `QThread` workers.
- **Docx Export**: Generates clean Microsoft Word (`.docx`) tables summarizing student marks across selected courses and evaluation metrics.
- **Progress Tracking**: Real-time progress updates via custom status bar indicators.

---

## 🛠️ Prerequisites & Installation

### Prerequisites
- Python 3.8 or higher

### Installation

1. **Clone the repository** (or navigate to the project directory):
   ```bash
   cd PBL-II-Project
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

Dependencies specified in `requirements.txt`:
- `pyside6`: GUI framework for cross-platform desktop interface.
- `pdfplumber`: Accurate text extraction from PDF files.
- `python-docx`: Programmatic creation and modification of Word `.docx` documents.

---

## 🖥️ Usage

Run the main application:

```bash
python main.py
```

### Steps to Extract & Export:
1. Click **Select PDF** to upload a result/marksheet PDF file.
2. Click **Process PDF** to parse the PDF document in the background.
3. Select the desired courses and score attributes (e.g., ISE, ESE, TOTAL, Grade Point) from the generated checkbox lists.
4. Click **Export as DOCX** to save the formatted result table as a `.docx` file.

---

## 📁 Project Structure

```text
├── main.py           # Application entry point, GUI event handling, QThread workers
├── app.py            # Generated PySide6 UI class setup
├── app.ui            # Qt Designer UI layout file
├── utils.py          # PDF regex parsing logic and Word document exporter
└── requirements.txt  # Project Python dependencies
```

---

## 📄 License

This project is created as part of the PBL-II (Project-Based Learning II) curriculum.
