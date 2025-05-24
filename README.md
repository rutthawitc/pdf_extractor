# PDF Data Extractor - User Guide

This Streamlit application allows you to extract data from PDF files (specifically from Etsy and Amazon), display it in an editable table, and export it to CSV format matching the required template.

## Features

- Upload PDF files from Etsy or Amazon
- Automatic detection of PDF type
- Data extraction from PDFs
- Editable data table for review and corrections
- Export to CSV with format matching the template
- UI/UX design similar to the Typhoon OCR Demo

## Requirements

- Python 3.6+
- Streamlit
- Pandas
- NumPy
- Pillow
- poppler-utils (for PDF text extraction)

## Installation

1. Ensure you have Python installed on your system
2. Create a virtual environment (recommended)
3. Install the required packages using the provided requirements.txt file:
   ```
   pip install -r requirements.txt
   ```

## Usage

1. Run the application:
   ```
   streamlit run app.py
   ```
   Or use the provided run.sh script:
   ```
   ./run.sh
   ```

2. Upload a PDF file from either Etsy or Amazon
3. The application will automatically detect the PDF type and extract data
4. Review and edit the extracted data in the table
5. Click "Export to CSV" to download the data in the required format

## PDF Type Support

- **Etsy PDFs**: The application extracts order numbers, customer information, item details, and personalization.
- **Amazon PDFs**: The application extracts order IDs, shipping information, product details, and customization.

## CSV Format

The exported CSV will match the template format with the following columns:
- Item Title
- Description (optional)
- Quantity
- Package Type
- Weight (gram)
- Customer Full Name
- Address Line 1
- Address Line 2 (optional)
- City
- State
- Postal Code
- Telephone (optional)
- Signature (yes or no)
- Insurance (yes or no)
- Item Value (USD)

## Troubleshooting

If the application cannot automatically detect the PDF type, you will be prompted to manually select whether it's an Etsy or Amazon PDF.

For any issues with PDF extraction, ensure that:
1. The PDF is not password-protected
2. The PDF contains text (not just images)
3. The PDF follows the standard Etsy or Amazon format
