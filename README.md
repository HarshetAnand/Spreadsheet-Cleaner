# Spreadsheet Cleaner

An AI-powered web application for automatically cleaning, validating, and analyzing spreadsheet data. Built with Streamlit, the tool processes messy CSV and Excel files, performs comprehensive data quality assessments, and generates downloadable reports. Designed for analysts, students, and professionals who need clean, structured data without manual effort.

## Features

- Standardize column headers with abbreviation expansion
- Remove duplicate and empty rows automatically
- Validate and standardize emails, phone numbers, and currency values
- Detect statistical outliers using the IQR method
- Calculate data quality scores across completeness, uniqueness, consistency, and validity
- Identify columns with similar names and suggest merges
- Standardize date formats across detected columns
- Generate AI-powered data summaries with customizable tone (Professional, Friendly, Executive, Technical)
- Export cleaned data as Excel, CSV, or JSON
- Generate comprehensive PDF reports with quality assessments and recommendations
- Create data dictionaries documenting column metadata

## How It Works

1. Upload a CSV or Excel file (up to 200MB)
2. Configure cleaning preferences in the sidebar
3. Run the cleaning process
4. Review quality scores, detected outliers, and suggestions
5. Download cleaned data and reports in your preferred format

## Tech Stack

- Streamlit (web interface)
- Pandas and NumPy (data processing)
- Plotly (interactive charts)
- ReportLab (PDF report generation)
- phonenumbers (phone validation)
- OpenAI API (optional AI insights)

## Quality Scoring

The application evaluates data quality across four dimensions:

- **Completeness:** Percentage of non-null values
- **Uniqueness:** Diversity of values within columns
- **Consistency:** Format uniformity within columns
- **Validity:** Adherence to expected data patterns

Overall scores fall into four categories:
- 80-100: Excellent quality
- 60-79: Good quality with minor issues
- 40-59: Fair quality, needs attention
- Below 40: Poor quality, requires significant cleaning

## Setup

Install dependencies:

\`\`\`bash
pip install -r requirements.txt
\`\`\`

Run locally:

\`\`\`bash
streamlit run spreadsheet_cleaner.py
\`\`\`

Optionally provide an OpenAI API key in the sidebar for AI-generated insights.

## Use Cases

- Cleaning customer or contact databases before analysis
- Preparing datasets for machine learning workflows
- Generating data quality reports for stakeholders
- Validating data exports from CRMs or other systems
- Standardizing formats across team-shared spreadsheets
