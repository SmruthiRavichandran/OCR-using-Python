# OCR Using Python

## Overview

This repository provides a framework for **Optical Character Recognition (OCR)** using Python. The project utilizes cutting-edge OCR libraries like Tesseract and OpenCV to extract text from images with high accuracy. Designed for simplicity and extensibility, this repository can be used for personal projects, academic research, and real-world applications.

What Is OCR?

 The necessity of digitisation is rapidly increasing in the modern era. Due to the growth of information and communication technologies (ICT) and the wide availability of handheld devices, people often prefer digitized content over the printed materials including books and newspaper. Also, it is easier to organize digitized data and analyze them for various purposes with many advanced techniques like artificial intelligence etc. So to keep up with the present technological scenario, it is necessary to convert all the information present till now which is in the printed format to digitised format.
  
  The main objective of the Preprocessing phase is To make as easy as possible for the OCR system to distinguish a character/word from the background.
Some of the most basic and important Preprocessing techniques are:-
1) Binarization
2) Skew Correction
3) Noise Removal
4) Thinning and Skeletonization
Binarization: This method gives a threshold for the whole image considering the various characteristics of the whole image (like lighting conditions, contrast, sharpness etc) and that threshold is used for Binarizing
---

## Features

- Support for multiple OCR backends (e.g., Tesseract).
- Preprocessing steps like noise removal, thresholding, and edge detection for improved OCR accuracy.
- Capability to process various image formats (JPG, PNG, TIFF, etc.).
- Batch processing of multiple images.
- Support for language-specific OCR and custom configurations.
- Export recognized text to plain text, CSV, or JSON formats.

---

## Table of Contents

1. [Installation](#installation)
2. [Usage](#usage)
3. [Examples](#examples)
4. [Image Preprocessing](#image-preprocessing)
5. [Supported Formats](#supported-formats)
6. [Batch Processing](#batch-processing)
7. [Contributing](#contributing)
8. [License](#license)

---

## Installation

### Prerequisites

- Python 3.8+
- pip
- Tesseract-OCR (Ensure Tesseract is installed and added to PATH)

### Steps

1. Clone the repository:

   ```bash
   git clone https://github.com/SmruthiRavichandran/OCR-using-Python.git
   cd OCR-using-Python
   ```

2. Create a virtual environment and activate it:

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

3. Install the required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Verify installation by running a sample OCR script:

   ```bash
   python ocr_example.py --image "example.jpg"
   ```

---

## Usage

### Quick Start

Extract text from an image:

```bash
python ocr.py --image "path/to/image.jpg" --lang "eng" --output "output.txt"
```

### Command-line Arguments

- `--image`: Path to the image file for OCR.
- `--lang`: Language for OCR (default: `eng` for English).
- `--output`: File path to save the recognized text.
- `--preprocess`: Preprocessing method (`thresh`, `blur`, or `none`).

### Using as a Library

```python
from ocr_utils import OCRProcessor

# Initialize OCRProcessor
ocr = OCRProcessor(lang="eng", preprocess="thresh")

# Perform OCR on an image
text = ocr.process_image("path/to/image.jpg")
print(text)
```

---

## Examples

### Basic OCR

```bash
python ocr.py --image "sample_image.png"
```

### OCR with Preprocessing

```bash
python ocr.py --image "sample_image.png" --preprocess "blur"
```

### Exporting Text to JSON

```bash
python ocr.py --image "sample_image.png" --output "output.json"
```

---

## Image Preprocessing

Effective OCR often requires preprocessing the image. This repository provides the following preprocessing options:

1. **Thresholding:** Converts the image to binary for better text contrast.
2. **Blurring:** Reduces noise in the image.
3. **Edge Detection:** Highlights text boundaries.

To apply preprocessing:

```bash
python preprocess.py --image "path/to/image.jpg" --method "thresh" --output "processed_image.jpg"
```

---

## Supported Formats

This framework supports various image formats including:

- **JPEG**
- **PNG**
- **TIFF**
- **BMP**

You can also process scanned PDFs by converting them to images using a library like `PyPDF2` or `pdf2image`.

---

## Batch Processing

For processing multiple images, use the batch mode:

```bash
python batch_ocr.py --input_dir "images/" --lang "eng" --output_dir "results/"
```

This script will process all images in the specified directory and save the results.

---

## Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository.
2. Create a feature branch:

   ```bash
   git checkout -b feature-name
   ```

3. Commit your changes and push:

   ```bash
   git commit -m "Feature description"
   git push origin feature-name
   ```

4. Create a pull request.

Make sure to follow the [Contributing Guidelines](CONTRIBUTING.md) and include tests for your changes.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Would you like me to expand on any specific sections, such as installation steps, preprocessing techniques, or supported OCR backends?
