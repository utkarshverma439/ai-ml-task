# Optical Character Recognition with EasyOCR and Color-Based Analysis

## Overview

This project utilizes **EasyOCR**, a robust OCR library, to extract text from images and analyzes the extracted text based on color associations. The goal is to identify text regions, classify them by their predominant color, and create a mapping of headings to their related elements based on proximity in the image. 

## Features

- **Text Detection**: Automatically detects text in images using EasyOCR.
- **Color Classification**: Classifies detected text regions into color categories (red, green, blue).
- **Spatial Mapping**: Maps headings to their related text elements based on proximity.
- **Visualization**: Marks detected text and their bounding boxes in the image.
- **Data Export**: Saves the mapping results in a JSON file for further analysis.

## Technologies Used

- **Python**: The primary programming language for this project.
- **OpenCV**: For image processing tasks, including reading and displaying images.
- **EasyOCR**: For optical character recognition to extract text from images.
- **Matplotlib**: For visualizing the results by displaying marked images.
- **NumPy**: For numerical operations and distance calculations.
- **JSON**: For data storage and export.

## Getting Started

### Prerequisites

Make sure you have the following installed:

- Python 3.x
- Required libraries: `opencv-python`, `easyocr`, `matplotlib`, `numpy`

You can install the required libraries using:

```bash
pip install opencv-python easyocr matplotlib numpy
```

### Usage

1. **Upload Your Image**: Ensure that your image file (e.g., `sample.png`) is in the working directory.
2. **Run the Script**: Execute the provided script to perform OCR and color analysis on the uploaded image.
3. **View Results**: The marked image will be displayed with bounding boxes and circles indicating detected text regions. The results will also be saved to `output_mappings.json`.

### Code Walkthrough

- **OCR Initialization**: The script initializes the EasyOCR reader for English text.
  
- **Text Detection**: The image is processed, and text is extracted along with bounding boxes.
  
- **Color Analysis**: Each detected text region is analyzed for its average color, which determines the marking color for the bounding box.
  
- **Proximity Mapping**: The script calculates distances between text centers to map headings to related elements based on a predefined threshold.
  
- **Output**: The mappings are saved in a JSON file and printed for user reference.

### Example Output

The output JSON file will contain mappings similar to the following structure:

```json
{
    "Heading 1": ["Related Text 1", "Related Text 2"],
    "Heading 2": ["Related Text 3"]
}
```


## License

This project is licensed under the MIT License. See the [LICENSE.md](License.md) file for details.


## Acknowledgments

- [EasyOCR](https://github.com/JaidedAI/EasyOCR) for the powerful OCR capabilities.
- [OpenCV](https://opencv.org/) for image processing functionalities.
- The community for continuous support and improvements in Python libraries.

---


