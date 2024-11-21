# Research Paper Summarization and OCR-Based Text Extraction

This project focuses on extracting and summarizing the content of research papers using various techniques including PDF text extraction, Optical Character Recognition (OCR), and text summarization using the SimpleT5 model. It also demonstrates parallel processing to speed up the extraction and summarization tasks.

## Table of Contents

- [Overview](#overview)
- [Technologies Used](#technologies-used)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Preprocessing and Summarization Workflow](#preprocessing-and-summarization-workflow)
- [Results](#results)
- [License](#license)

## Overview

This project automates the process of extracting text from research papers stored in PDF format, with a focus on eliminating irrelevant content such as references, tables, and figures. After extracting and preprocessing the text, it summarizes the content using the SimpleT5 model, providing concise summaries for further analysis.

Key Features:
- **Text Extraction from PDF**: Extracts text while excluding tables, figures, and reference sections.
- **OCR for Scanned Images**: Extracts text from images within the PDF using OCR (Optical Character Recognition).
- **Preprocessing**: Text is preprocessed to remove unnecessary characters, emails, URLs, and numbers.
- **Summarization**: Extractive text summarization using LexRank and abstractive summarization using SimpleT5.
- **Parallel Processing**: Uses multiprocessing to extract and preprocess texts in parallel, making the process faster.
- **Evaluation**: Evaluates summaries using the ROUGE metric.

## Technologies Used

- **Python Libraries**:
  - `PyMuPDF` (fitz) for PDF text extraction.
  - `pytesseract` for OCR (Optical Character Recognition).
  - `LexRank` for extractive summarization.
  - `SimpleT5` for abstractive summarization using the T5 model.
  - `spaCy` for text processing (lemmatization, tokenization, etc.).
  - `nltk` for sentence tokenization and stopword removal.
  - `rouge` for summary evaluation.

- **Other Tools**:
  - **Tesseract OCR** for extracting text from scanned images in PDFs.

## Features

- **Parallel PDF Processing**: Efficiently processes multiple PDFs using parallelism with Python's `multiprocessing` library.
- **Text Preprocessing**: Cleans the extracted text by removing emails, URLs, tables, figures, and special characters.
- **Summarization Models**: Combines LexRank (extractive summarization) and SimpleT5 (abstractive summarization) for generating concise summaries.
- **ROUGE Evaluation**: Provides evaluation scores to assess the quality of generated summaries.
- **OCR for Images**: Handles PDFs with images using OCR to extract text.

## Installation

To set up this project, you need to install the necessary dependencies:

```bash
pip install pymupdf
pip install pycryptodome
pip install nltk
pip install lexrank
pip install simplet5
pip install rouge
pip install pytesseract
pip install Pillow
