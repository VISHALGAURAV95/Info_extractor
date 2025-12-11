Info Extractor
Python utility to extract structured voter information from electoral roll PDF files and export the result to an Excel spreadsheet.​

Features
Reads all PDF files from a given directory.

Extracts text from pages 2 to last-1 using PyPDF2.​

Uses regular expressions to parse:

House No

Name

Gender

Age

Father’s/Husband’s Name

Voter ID​

Saves the final cleaned data into output.xlsx using pandas.​

Project Structure
info_extractor.ipynb – Jupyter notebook containing the full extraction logic.

content/ – Directory that should contain the input PDF files.

output.xlsx – Generated Excel file with extracted voter records.

Requirements
Python 3.x

Libraries:

PyPDF2

pandas

numpy

Install dependencies:

bash
pip install PyPDF2 pandas numpy
Usage
Place all input PDF files inside the content directory (or update the directory variable in the notebook).

Open info_extractor.ipynb in Jupyter/Colab.

Run all cells.

After execution, check output.xlsx in the project root for the extracted voter data.

Output Columns
The script produces an Excel file with the following columns:

House No

Gender

Name

Age

Father's/Husband's Name

Voter Id

Each row corresponds to a single voter record parsed from the PDFs.​

Notes
The extraction relies on the specific formatting of the electoral roll PDFs (patterns like House No :, Name :, Age :, Female/Male). If the format changes, the regex expressions in the notebook may need adjustment.​

This project is intended for educational and analytical purposes; ensure compliance with local data protection and electoral roll usage rules.
