**Overview**

This repository contains code for converting a JSON dataset to a CSV file, loading a CSV file, performing exploratory data analysis (EDA), translating the input and target text to English, and loading a pretrained transformer model (mT5) on GPU.

**Steps**

1. **Convert JSON dataset to CSV file:**
    * Use the `convert_json_to_csv.py` script to convert the JSON dataset (`labeled_validation_dataset.jsonl`) to a CSV file (`labeled_validation_dataset.csv`).

2. **Load CSV file:**
    * Use the `load_csv_file.py` script to load the CSV file (`labeled_validation_dataset.csv`) into a pandas DataFrame.

3. **Exploratory Data Analysis (EDA):**
    * Use the `exploratory_data_analysis.py` script to perform EDA on the DataFrame. This includes:
        * Checking the DataFrame's info and shape.
        * Counting the number of tokens in each paragraph.
        * Visualizing the distribution of the number of tokens in paragraphs.
        * Finding the paragraph with the maximum number of tokens.
        * Showing the paragraph with the maximum number of tokens.

4. **Translate input and target text to English:**
    * Use the `translate_text.py` script to translate the input (`paragraph`) and target (`summary`) text to English.
        * The script uses the `mtranslate` library to perform the translation.
        * The translated text is added to new columns in the DataFrame (`translated_input` and `translated_summary`).

5. **Load pretrained transformer model (mT5) on GPU:**
    * Use the `load_pretrained_transformer_model.py` script to load the pretrained mT5 model.
        * The script uses the `transformers` library to load the model.
        * The model is loaded on GPU if available.

**Additional Notes**

* The code in this repository is written in Python.
* The code assumes that the following libraries are installed:
    * `pandas`
    * `csv`
    * `matplotlib`
    * `seaborn`
    * `mtranslate`
    * `transformers`
    * `sentencepiece`
    * `faker`
* The code can be modified to work with other datasets and models.

**Usage**

To run the code, follow these steps:

1. Clone the repository to your local machine.
2. Install the required libraries:
```bash
pip install -r requirements.txt
```
3. Run the scripts in the following order:
    * `convert_json_to_csv.py`
    * `load_csv_file.py`
    * `exploratory_data_analysis.py`
    * `translate_text.py`
    * `load_pretrained_transformer_model.py`

The output of the scripts will be displayed in the console.
