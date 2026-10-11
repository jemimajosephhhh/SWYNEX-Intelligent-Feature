# SWYNEX Intelligent Feature – AI Resume Improvement Assistant

## Project Overview

The AI Resume Improvement Assistant is a Python-based application that uses the Google Gemini API to analyze a resume against a target job description. It identifies relevant skills, highlights missing or unclear requirements, and provides practical suggestions to improve resume content.

This project was developed as part of **SWYNEX AI Internship – Task 3: Intelligent Feature**.

## Features

- **Resume–Job Description Analysis:** Evaluates alignment between a candidate's resume and a target role.
- **Matching Skills:** Identifies skills supported by the resume that match the job requirements.
- **Skill Gap Analysis:** Highlights job requirements that are missing or not clearly demonstrated.
- **Resume Improvement:** Suggests clearer, stronger resume bullet points without intentionally inventing qualifications or achievements.
- **Personalized Action Plan:** Recommends practical steps to improve the resume or develop relevant skills.
- **Input Validation:** Handles empty, very short, and excessively long inputs.
- **Error Handling:** Provides user-friendly messages for API and request failures.
- **Evaluation Examples:** Includes scenarios for testing valid inputs, invalid inputs, API failures, and factual accuracy.

## Technology Stack

- Python
- Streamlit
- Google Gemini API
- `google-genai`
- `python-dotenv`

## Project Structure

```text
SWYNEX-Intelligent-Feature/
├── app.py
├── requirements.txt
├── README.md
├── .gitignore
└── .env  # Local only; never upload
```

## Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/jemimajosephhhh/SWYNEX-Intelligent-Feature.git

### 2. Create and activate a virtual environment

Windows:

```bash
python -m venv venv
venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure the API key

Create a `.env` file in the project directory:

```text
GEMINI_API_KEY=your_gemini_api_key
```

Replace the placeholder with your own valid Gemini API key.

**Security:** Never commit `.env` or publish your API key.

### 5. Run the application

```bash
streamlit run app.py
```

The application will open in your browser at the local address shown in the terminal.

## Evaluation Scenarios

| Test case | Expected behavior |
|---|---|
| Valid resume and job description | Generate a structured AI analysis |
| Empty resume | Display a validation message |
| Empty job description | Request the missing input |
| Very short input | Ask the user to provide more details |
| API request failure | Display an error without crashing |
| Unsupported achievement | Avoid recommending invented qualifications |

The application includes an evaluation checklist. Actual outcomes should be recorded after running each test. AI-generated assessments require manual review for relevance and factual accuracy.

## Limitations

- The quality of the analysis depends on the information supplied.
- AI recommendations may be incomplete or inaccurate and should be reviewed.
- Skill alignment is an informal assessment, not a verified probability of getting hired.
- API access, model availability, and usage limits depend on the Google Gemini account and service.

## Internship Task

**Organization:** SWYNEX Technologies  
**Internship:** AI Internship  
**Task 3:** Intelligent Feature

This project demonstrates practical experience integrating a generative AI API into an interactive application, implementing input validation and error handling, and defining evaluation scenarios.

## Future Improvements

- Add automated unit tests.
- Export the analysis as a downloadable report.
- Add configurable evaluation criteria.
- Improve factuality checks for resume recommendations.
- Deploy the application for public access.