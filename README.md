# ATS Application

Streamlit application for estimating how closely a resume matches a job description. The app extracts text from PDF or DOCX resumes, asks Gemini to structure the resume and job-description fields, cleans the text, and uses a bundled Keras model to produce an ATS-style match score.

## Project Context

This is a group coursework project, maintained here under Snega Murugan's GitHub profile as a clean portfolio copy. Original collaboration repository: [MinishhYokesh/ATS-Application](https://github.com/MinishhYokesh/ATS-Application).

## Features

- Upload a resume as PDF or DOCX.
- Paste a job description.
- Extract job requirements and resume category with Gemini.
- Clean and normalize text for model input.
- Predict an ATS match score with the included `model_1.h5` model.
- Download the prediction result as CSV.

## Repository Contents

- `streamlit_app.py` - Streamlit app entrypoint.
- `model_1.h5` - Pre-trained Keras model used by the app.
- `requirements.txt` - Runtime dependencies.

## Setup

```powershell
python -m venv .venv
.\.venv\Scripts\activate
pip install -r requirements.txt
```

Set a Google Gemini API key before running the app:

```powershell
$env:GOOGLE_API_KEY="your_api_key_here"
```

For Streamlit Cloud, add `GOOGLE_API_KEY` in the app secrets instead of committing it to the repository.

## Run

```powershell
streamlit run streamlit_app.py
```

## Notes

- This app is an educational demo and should not be used as a final hiring or screening decision system.
- The API key is intentionally loaded from environment variables or Streamlit secrets. Do not commit keys or credentials.
- The model score depends on the bundled model and the text extraction quality from uploaded resumes.
