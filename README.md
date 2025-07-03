# housenovel-project

# Preprocessing Images and Extracting OCR Text for Structured JSON Conversion

This script automates the pipeline of:

**Preprocessing scanned directory page images** (noise removal) using OpenCV.  
**Extracting OCR text** from these images using Tesseract.  
**Sending the OCR text to GPT (`gpt-4o-mini`) with structured instructions** to parse resident information into clean JSON.  
**Saving the structured JSON outputs** for each image in a `final_json` folder for downstream analysis and integration.

### Key Features:
- **Noise Removal**: Removes small artifacts and cleans images for better OCR accuracy.
- **OCR Extraction**: Uses `pytesseract` to convert image text into raw text.
- **Structured Prompting**: Instructs GPT to parse names, spouse names, occupations, employers, and addresses from city directory pages.
- **JSON Cleaning**: Handles Unicode and formatting issues for safe JSON parsing.
- **Automated Batch Processing**: Processes all images in `cropped_manual` and saves outputs systematically.

---
**Challenges included:**

Poor scan quality on certain years requiring threshold adjustments.

Differentiating similarly formatted business listings vs. resident listings.

Handling inconsistent punctuation and OCR misreads (e.g., | for l).

These were mitigated using:

Preprocessing with OpenCV for clarity.

Regex normalization pipelines for consistent data extraction.

Manual spot checks on a 5–10% sample for validation.



**Handwriting OCR Experience**
I have prior experience working with handwritten records using:

Tesseract’s LSTM handwriting model fine-tuning.

LayoutLM for structured document parsing.

Manual transcription for accuracy validation on low-confidence OCR outputs.

I am comfortable handling handwritten materials and adapting workflows for 19th-century cursive documents requiring hybrid OCR + manual QA workflows.

