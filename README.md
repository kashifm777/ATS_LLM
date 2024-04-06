# Smart ATS Streamlit Web App

This Streamlit web app leverages Google's GenerativeAI service (Gemini Pro) to act as a smart Applicant Tracking System (ATS) for job seekers.

## 1. Live demo

Here is a link to Run our live app on Streamlit.

[ATS on Streamlit](https://ats-llm.streamlit.app)

## 2. Features:

- **Resume Upload:** Upload your resume in PDF format.
- **Job Description:** Paste the job description text.
- **AI-powered Matching:** Gemini Pro analyzes the resume and job description to estimate the percentage match and identify missing keywords.
- **Resume Improvement Tips (Optional):** The response may include suggestions for improving your resume based on the job description (subject to API capabilities).

## 3. Requirements:

- Python 3.x
- Streamlit (`pip install streamlit`)
- `dotenv` library (`pip install python-dotenv`)
- PyPDF2 library (`pip install PyPDF2`)
- Google Cloud Project with GenerativeAI API enabled ([https://cloud.google.com/ai/generative-ai](https://cloud.google.com/ai/generative-ai))

## 4. Setup:

1. Create a virtual environment (recommended): `python -m venv venv`
2. Activate the environment: `source venv/bin/activate` (Windows: `venv\Scripts\activate`)
3. Install dependencies: `pip install streamlit python-dotenv PyPDF2`
4. Create a `.env` file in the project directory:
   - Add `GOOGLE_API_KEY=<YOUR_API_KEY>` (replace with your GenerativeAI API key)

## 5. Running the App:

1. Open a terminal in the project directory.
2. Run the app: `streamlit run app.py`
3. Access the app in your web browser at http://localhost:8501.

## 6. Usage:

1. Paste the job description text in the provided field.
2. Upload your resume in PDF format.
3. Click the "Submit" button.

## 7. Output:

The app displays a JSON-like response, including:

- **JD Match:** The estimated percentage match between your resume and the job description.
- **MissingKeywords:** A list of potentially missing keywords from the job description that could be added to your resume.
- **Profile Summary (Optional):** Depending on API capabilities, the app might provide suggestions for improving your resume summary.

## 8. Note:

- This is a basic example using a free-tier API. The accuracy of matching and suggestions may vary.
- Consider using a professional resume review service for personalized feedback.

## 9. Disclaimer:

This application and its output are for informational purposes only and should not be taken as a guarantee of job placement. Always consult a career counselor or recruiter for tailored advice.