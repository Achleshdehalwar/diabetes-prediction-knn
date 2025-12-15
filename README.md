Portfolio Website Generator

A simple Streamlit-based tool that converts a resume (PDF or DOCX) into a clean, responsive personal portfolio website using standard HTML, CSS, and JavaScript.

This project focuses on automating the repetitive task of building a basic portfolio site while keeping the generated output lightweight, readable, and easy to customize.

Features

Upload resume in PDF or DOCX format

Extracts structured content from the resume

Generates a multi-section portfolio website:

Header

About

Skills

Experience

Projects

Education

Contact details

Outputs pure HTML, CSS, and JavaScript

Provides downloadable ZIP containing website files

Simple UI designed as an internal utility tool

Tech Stack

Python

Streamlit – Web interface

LangChain – Prompt orchestration

Google Gemini API – Content generation

PyPDF2 – PDF text extraction

python-docx – DOCX text extraction

Project Structure
.
├── app.py
├── assets/
│   └── background.jpg
├── index.html        # generated
├── style.css         # generated
├── script.js         # generated
└── portfolio_website.zip

Setup Instructions
1. Clone the repository
git clone https://github.com/your-username/portfolio-website-generator.git
cd portfolio-website-generator

2. Create a virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate   # Windows: venv\\Scripts\\activate

3. Install dependencies
pip install -r requirements.txt

4. Configure environment variables

Create a .env file in the root directory:

gemini=YOUR_GOOGLE_GEMINI_API_KEY

Run the Application
streamlit run app.py


The app will open in your browser.

How It Works

User uploads a resume file (PDF or DOCX)

Text is extracted using appropriate parsers

Resume content is converted into a structured portfolio layout

Static website files (index.html, style.css, script.js) are generated

Files are packaged into a ZIP for download

Customization

Replace assets/background.jpg with your own background image

Edit generated HTML/CSS after download for personal styling

Adjust prompts to control section formatting or layout

Use Cases

Quickly creating a personal portfolio

Resume-to-website automation

Learning project for Streamlit + LLM integration

Demonstrating document processing and content generation

Limitations

Generated website is static (no backend)

Layout is intentionally minimal and generic

Resume formatting quality depends on input document structure

Future Improvements

Live preview of generated website

Theme selection (light/dark)

Editable sections before generation

Hosting integration (GitHub Pages / Netlify)
