# AI-Based MCQ Generator

This project is a Flask-based web application that allows users to upload text files (PDF, DOCX, or TXT) and generate multiple-choice questions (MCQs) based on the content. It leverages Google Gemini 1.5 Pro (PaLM API) to intelligently generate questions, saving the results in both text and PDF formats.

## Features

- **Text extraction** from PDF, DOCX, and TXT files.
- **Automatic MCQ generation** based on the uploaded text using AI (Google Gemini 1.5 Pro).
- **Downloadable results** in both `.txt` and `.pdf` formats.
- **Web-based interface** for file upload and MCQ generation.

## Tech Stack

- **Backend:** Python, Flask
- **Text extraction:** `pdfplumber`, `python-docx`, `FPDF`
- **MCQ generation:** Google Gemini 1.5 Pro (PaLM API)
- **File handling:** `Werkzeug`
- **Frontend:** HTML, Bootstrap (via Flask templates)

## Installation

To run the project locally, follow these steps:

### Prerequisites

- Python 3.x
- API access to Google Gemini 1.5 Pro (PaLM API)

### Setup

1. **Clone the repository**:

   ```bash
   git clone https://github.com/ShaanAgarwal/AI-MCQ-Generator
   cd ai-mcq-generator
   ```

2. **Create and activate a virtual environment (optional)**:

   ```bash
   python3 -m venv venv
   source venv/bin/activate   # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**:

   ```bash
   pip install -r requirements.txt
   ```

4. **Set your Google API Key**:

   Replace `<paste_google_api_key>` in the code with your actual Google Gemini 1.5 Pro API key in the environment

5. **Run the application**:

   ```bash
   python app.py
   ```

6. **Visit the application**:

   The application will be running locally at `http://127.0.0.1:5000/`.

## Usage

1. Navigate to the home page of the web application.
2. Upload a text file (PDF, DOCX, or TXT) containing the content for which you want to generate MCQs.
3. Specify the number of questions you want to generate.
4. Click **Submit** to generate the MCQs.
5. View the results on the results page and download them in either `.txt` or `.pdf` format.

## Folder Structure

```bash
├── app.py                   # Main Flask application
├── templates/               # HTML templates for Flask
│   ├── index.html           # Home page
│   ├── results.html         # Results display page
├── uploads/                 # Uploaded files (automatically generated)
├── results/                 # Generated MCQs in text and PDF format (automatically generated)
├── requirements.txt         # Python dependencies
└── README.md                # Project documentation
```

## API Integration

This project integrates Google Gemini 1.5 Pro (PaLM API) for generating multiple-choice questions based on provided text. Make sure to configure your API key in the environment variable `GOOGLE_API_KEY` before running the app.

## Example

- **Input:** Upload a file with text content (e.g., PDF, DOCX, or TXT).
- **Output:** The system generates MCQs in the following format:

  ```
  ## MCQ
  Question: What is the capital of France?
  A) London
  B) Paris
  C) Berlin
  D) Madrid
  Correct Answer: B
  ```

  You can download this output as a `.txt` or `.pdf` file.