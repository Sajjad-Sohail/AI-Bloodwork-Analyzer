# 🩸 AI Bloodwork Analyzer

An AI-powered Streamlit application that analyzes blood test results and provides a simple summary of abnormal values along with practical Indian diet suggestions.

This project was built as a learning project to explore how Large Language Models (LLMs) can extract information from unstructured text and use that information in a multi-step AI workflow.

## Features

- Upload a blood report as a `.txt` file or paste report text directly
- Extract blood test names, values, and reference ranges using an LLM
- Classify results as **HIGH**, **LOW**, or **NORMAL**
- Generate a simple health summary
- Generate practical Indian dietary suggestions
- Display results through a Streamlit interface
- Preserve the original report for comparison

## How It Works

The application uses a two-step LLM workflow:

1. **Blood Work Extraction**
   - The report is sent to the LLM.
   - Test values and reference ranges are extracted.
   - Each result is classified as HIGH, LOW, or NORMAL based on the ranges contained in the report.

2. **Health Summary & Diet Suggestions**
   - The extracted analysis is passed to a second LLM prompt.
   - The model generates a short plain-language summary.
   - It also suggests foods to eat more of and foods to avoid.

```text
Blood Report
     ↓
LLM Extraction
     ↓
Structured Blood Work Analysis
     ↓
LLM Health/Diet Analysis
     ↓
Streamlit Results
```

## Screenshots
<img width="1914" height="891" alt="image" src="https://github.com/user-attachments/assets/c8d3877f-7533-4c3e-b4ab-f248805fe318" />
<img width="1912" height="890" alt="image" src="https://github.com/user-attachments/assets/12904ac7-d86a-47e0-81d6-a2ed7da2560f" />
<img width="1912" height="891" alt="image" src="https://github.com/user-attachments/assets/cc55d191-5519-480e-87b0-cfebefc33d8c" />
<img width="1909" height="891" alt="image" src="https://github.com/user-attachments/assets/063cc06f-57bf-41d0-8308-a155bc5c9b37" />






## Tech Stack

- Python
- Streamlit
- Groq API
- Llama model through Groq
- python-dotenv
- Jupyter Notebook

## Installation

Clone the repository:

```bash
git clone https://github.com/Sajjad-Sohail/AI-Bloodwork-Analyzer.git
cd AI-Bloodwork-Analyzer
```

Create and activate a virtual environment.

### PowerShell

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

Install dependencies:

```powershell
pip install -r requirements.txt
```

## Environment Variables

Create a `.env` file in the project root:

```env
GROQ_API_KEY=your_groq_api_key_here
```

Do **not** commit your `.env` file to GitHub.

Add it to `.gitignore`:

```gitignore
.env
.venv/
__pycache__/
.ipynb_checkpoints/
```

## Run the Application

```powershell
streamlit run app.py
```

Streamlit will open the application in your browser.

## Project Structure

```text
AI-Bloodwork-Analyzer/
│
├── app.py
├── health_analysis.ipynb
├── requirements.txt
├── README.md
├── .gitignore
└── .env                 # local only - do not commit
```

## Disclaimer

This project is for **educational and demonstration purposes only**.

The AI-generated output is not medical advice, diagnosis, or treatment. Blood test results and health concerns should be reviewed with a qualified healthcare professional.

Do not upload real patient or sensitive medical information to this demo unless you understand and accept the privacy implications of sending that information to an external AI service.

## Learning Goals

This project demonstrates:

- LLM prompt engineering
- Information extraction from unstructured data
- Multi-step LLM workflows
- Passing the output of one LLM task into another
- Building an AI application with Streamlit
- Working with external LLM APIs

## Author

**Sajjad Sohail**

GitHub: Sajjad-Sohail
