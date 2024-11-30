# **Product Attribute Extraction**

## **Overview**

This repository contains a solution to automatically extract structured product attributes from unstructured product descriptions. The extracted attributes can include details such as brand, price, color, material, dimensions, weight, features, and specifications, among others. This solution is built to help automate the process of structuring product information for e-commerce platforms and other cataloging systems.

## **Features**
- Extracts a wide range of product attributes from descriptions, including:
  - **Brand, Category, Color, Material**
  - **Size (dimensions, weight, display size)**
  - **Price, Discount, Stock Availability**
  - **Processor, RAM, Storage, Battery, Camera, Display, Connectivity**
  - **Rating, Reviews, Expiration Date, Energy Rating, Warranty**
- Outputs the extracted data in **JSON** format for easy integration into product catalogs or databases.
- Handles missing or incomplete descriptions with error handling.

## **Installation**

To get started, follow these steps to install the necessary dependencies.

### **Prerequisites**
- Python 3.x
- `pip` (Python package installer)

### **Step 1: Clone the repository**
```bash
git clone https://github.com/akhilesh1709/Code-IQ-Product-attribute-extraction.git
cd product-attribute-extraction
```

### **Step 2: Install dependencies**
You can install the required dependencies using the following command:
```bash
pip install -r requirements.txt
```

---

## **Usage**

The main script processes product descriptions and extracts attributes. Below are the usage instructions for both **CSV-to-JSON conversion** and **single description extraction**.

### **Processing a CSV file containing product descriptions**

1. **Prepare your CSV file**:
   Your CSV file should have a column named `description` with product descriptions. Optionally, you can also include a `product_name` column.

2. **Run the script** to extract attributes and save the output in a JSON file:

- `text_data.csv`: The path to your input CSV file.
- `output_data.json`: The path where the output JSON will be saved.

### **Processing a list of product descriptions (advanced)**

You can process a list of descriptions manually by passing them to the function:

```python
from extract_features import process_product_descriptions

descriptions = [
    "This is a red cotton shirt with a large size.",
    "Samsung Galaxy S21 with 128GB storage and 8GB RAM."
]

processed_data = process_product_descriptions(descriptions)
```

The `output_data` will contain the extracted attributes.

---

## **Technical Stack**

- **Python 3.x**: Primary programming language.
- **pandas**: For reading and processing CSV files.
- **re (Regex)**: Used for extracting attributes based on regular expressions.
- **spaCy**: (Optional) Can be used for more advanced Named Entity Recognition (NER) if needed.
- **tqdm**: For displaying a progress bar during description processing.

### **File Dependencies**

- `Code to extract results.ipynb`: Main file that contains functions to extract attributes from descriptions.
- `Produce code to extract features.ipynb`: Script to convert product descriptions from a CSV file to a JSON output.
- `requirements.txt`: Contains all the required libraries for the project.
