# Resume Parser

A Python tool for extracting key information from PDF resumes using pattern matching and regular expressions.

## Installation

```bash
pip install pdfminer.six
```

## Usage

```python
from resume_parser import parse_resume

# Parse a resume
result = parse_resume("path/to/resume.pdf")

# Example output:
# {
#     "name": "John Doe",
#     "contact_number": "123-456-7890",
#     "email": "john.doe@example.com",
#     "skills": ["Python", "Machine Learning", "Data Analysis"],
#     "education": ["Computer Science", "Data Science"]
# }
```

## Features

- Extracts personal information (name, phone, email)
- Identifies technical and professional skills
- Detects educational background
- Handles PDF format
- Cross-validates name from multiple sources

## Functions

- `parse_resume(pdf_path)`: Main function to process PDF resume
- `extract_text_from_pdf(pdf_path)`: Extracts text from PDF
- `extract_contact_number_from_resume(text)`: Finds phone numbers
- `extract_email_from_resume(text)`: Extracts email addresses
- `extract_skills_from_resume(text, skills_list)`: Matches skills
- `extract_education_from_resume(text)`: Identifies education
- `extract_name_from_resume(text)`: Extracts candidate name
- `get_correct_name_from_resume_and_email(text)`: Validates name extraction
