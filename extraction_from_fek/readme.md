# Greek FEK Extractor (Jupyter Notebook)

This Jupyter Notebook provides a Python implementation to extract and organize information from Greek FEKs (Φύλλο Εφημερίδας της Κυβερνήσεως, Government Gazette) in PDF format. It automates the process of extracting key details like:

* FEK type (e.g., "πραξη νομοθετικου περιεχομενου", "προεδρικο διαταγμα")
* FEK number
* Date
* Title
* References (presidential orders, laws, constitution)

## Getting Started

1. **Install Required Libraries:**
   Ensure you have the following libraries installed:
   
   ```pip install pymupdf pandas numpy```
3. **Run the Jupyter Notebook:**
   * Open the fek_extractor.ipynb notebook.
   * Replace the placeholder file paths with the actual paths to your FEK PDF files.
   * Execute the cells in the notebook to process the PDFs and extract information.
   * 
## How it Works

The notebook defines a `fek` class to handle the extraction and processing of FEK information. The main steps involved are:

### PDF Text Extraction
The `pdf_reader` class is used to extract text from the PDF.

### FEK Information Extraction
The `fek` class processes the extracted text to identify:

* FEK type
* FEK number
* Date
* Title
* References

### Data Organization
The extracted information is organized into a Pandas DataFrame for further analysis or export.

## Example usage
```
# Assuming 'fek_file.pdf' is a valid FEK file
fek_obj = fek.fek(file='fek_file.pdf')
fek_obj.scrape_file()
fek_obj.process_fek()

# Get the extracted information as a DataFrame
fek_df = fek_obj._toDataFrame()

# Print the DataFrame or use it for further analysis
print(fek_df)
```

## Additional Notes

* You may need to adjust the regular expressions used for reference extraction based on specific FEK formatting variations.
* Consider adding error handling mechanisms to handle potential issues during the PDF processing.
* Feel free to explore and modify the code to tailor it to your specific needs.
* Remember to replace `[your-username]` with your actual GitHub username.

## Additional Tips:

* Consider creating a requirements.txt file to list the required libraries and their versions.
* Add comments to your code to explain the logic and reasoning behind specific steps.
* Test your code with a variety of FEK PDFs to ensure robustness.
* Consider using a virtual environment to isolate the project's dependencies.

By following these steps and incorporating the suggestions, you can effectively use the Jupyter Notebook to extract valuable information from Greek FEK PDFs.
