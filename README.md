# DEMO-INTER-AutomatedTool

The **DEMO-INTER-AutomatedTool** streamlines the process of identifying matching classes across ontologies. This tool automates the matching process, making it more efficient, scalable, and systematic, allowing researchers to focus on reviewing results rather than performing exhaustive manual searches.  

## **How It Works**  

The tool follows a **three-step approach** to class matching:  

1️⃣ **Class IRI Matching:** Finds identical class **IRIs (unique ontology identifiers)** across two ontologies to quickly highlight direct overlaps.  

2️⃣ **Class Label & Synonym Matching:** Recognizes conceptually similar classes that have different IRIs by checking for labels, alternative terms, synonyms, and related terminology using ontology properties.  

3️⃣ **Class Definition Matching:** Applies **natural language processing (NLP)** and a **quantized Llama 3 language model** to analyze class definitions, enabling detection of semantically equivalent concepts even when labels differ.  

---

## 📂 Repository Contents

This repository provides two different environments for running the tool:

| File | Description |
|------|------------|
| `GoogleColab-Automated_tool.ipynb` | Google Colab version for running in the cloud without installation. |
| `JupyterNotebook_AutomatedTool.ipynb` | Jupyter Notebook version for running locally on your computer. |


---

## 🚀 Getting Started

### 🔧 Prerequisites

This tool requires **Python 3.7 or later** and the following Python packages:

- `rdflib` (for working with ontologies)
- `requests` (for fetching ontologies from URLs)
- `pandas` (for handling data tables)
- `sentence-transformers` (for text similarity matching)
- `scikit-learn` (for similarity calculations)
- `mlx_lm` (for machine-learning-based ontology matching)
- `IPython` (for interactive notebook displays)

If you are using **Google Colab**, most dependencies are pre-installed.

---

## 🖥️ Running the Tool

You can run the tool in **two different ways**, depending on whether you prefer Google Colab or Jupyter Notebook.

### **1️⃣ Running in Google Colab (Cloud)**
#### **Open Google Colab:**
Visit [Google Colab](https://colab.google).

#### **Load the Notebook:**
Click `File > Open Notebook`, switch to the GitHub tab, and enter the repository URL. Alternatively, you can upload the file `GoogleColab-Automated_tool.ipynb` from this repo directly.

#### **Run the Notebook:**
Execute each cell sequentially to carry out:
1. **IRI Matching:**
Identify classes with identical IRIs.
2. **Label and Synonym Matching:**
Find classes with matching labels and synonyms.

For steps 1&2:
- You will provide two ontologies for comparison
- Choose to load your ontology files either via a URL or a local file path.

3. **Definition Matching:**
Compare class definitions using automated matching.

  For step 3:
  - The Llama 3 language model used is accesed via Hugging Face so you will need a `read access token` (see [how to create one](https://huggingface.co/docs/hub/en/security-tokens))
  - Provide your access token when prompted
  - Provide the ontology you wish to search through 
  - Choose to load the ontology file either via a URL or a local file path.
  - Provide the base IRI for the main ontology to be searched through.
  - Choose to either upload a CSV file with multiple target classes or provide only one target class you wish to find matches for
    - Create a CSV file with three columns to provide a list of target classes 
      | Label | IRI |Definition|
      |-----|---|----------|
      |     |   |         |
    - Provide the path to the CSV file containing your target classes

      OR
      
    - Provide one target class information (IRI, Label, and Definition) when prompted
      
  - The tool will extract class definitions, perform the matching, and display the results in a table.
    
**Note:** Running **Step 3 (Definition Matching)** in Google Colab requires a significant amount of computing resources (such as GPU/TPU and high memory). If you are using the free version of Colab, you might encounter performance limitations. For optimal performance, a paid Google Colab account (e.g., Colab Pro) is recommended.


### **2️⃣ Running in Jupyter Notebook (Locally)**

#### **Open Jupyter Notebook:**  
Launch Jupyter Notebook from your terminal by running:

```bash
jupyter notebook
```
#### **Install Dependencies**
If you haven’t installed the required packages, you can do so by running:

```bash
pip install rdflib requests pandas sentence-transformers scikit-learn mlx-lm torch torchvision torchaudio
```

#### **Open the Notebook:**
Open the file `JupyterNotebook_AutomatedTool.ipynb` from the repository.

#### **Run the Notebook:**
The notebook is divided into three main sections corresponding to each step of the matching process. Run each cell to sequentially carry out:
1. **IRI Matching:**
Identify classes with identical IRIs.
2. **Label and Synonym Matching:**
Find classes with matching labels and synonyms.

  For steps 1&2:
  - You will provide two ontologies for comparison
  - Choose to load your ontology files either via a URL or a local file path when prompted during execution

3. **Definition Matching:**
Compare class definitions using automated matching.

  For step 3:
  - Provide the ontology you wish to search through 
  - Choose to load the ontology file either via a URL or a local file path.
  - Provide the base IRI for the main ontology to be searched through.
  - Create a CSV file with three columns to provide a list of target classes you wish to find matches for
    | Label | IRI |Definition|
    |-----|---|----------|
    |     |   |         |
  - Provide the path to the CSV file containing your target classes 
  - The tool will extract class definitions, perform the matching, and display the results in a table.

**Note:** The script for **Step 3 (Class Definition Matching)** uses the `mlx-community/Meta-Llama-3-8B-Instruct-4bit` model, which is optimized for Mac environments. If you're not running on a Mac, you may encounter compatibility issues.


## **📊 Understanding the Output**
After running the tool, you will see:

- **Results Table:**
A table for each step displaying matching ontology classes, including their IRIs, labels, and definitions.

- **Downloadable CSV File:**
A clickable download link for a CSV file containing all the matching results. This file can be used for further analysis or reporting.

## **🔧 Troubleshooting**
- **ModuleNotFoundError:**
Ensure all required dependencies are installed (see the installation section above).

- **Ontology Loading Issues:**
Verify that your ontology file is in a valid RDF/XML format (e.g., .rdf, .owl, or .xml) and that any provided URLs are accessible.

- **CSV File Issues:**
Confirm that your CSV file includes the correct headers: IRI, Label, and Definition. If using Excel, save your file as a CSV before running the tool.

## **💡 Additional Information**
- Future Enhancements
- Support for additional ontology formats (e.g., Turtle, JSON-LD).
- More advanced matching techniques using deeper machine learning models.
- Enhanced visualization of ontology relationships.

## **📜 License**
This project is licensed under the APACHE License 2.0. See the [LICENSE](LICENSE) file for details.

## **💬 Contact**
If you have any questions or need assistance, please reach out at [fatibaba@gmail.com] or open an [issue](https://github.com/fatibaba/DEMO-INTER-AutomatedTool/issues) on our GitHub repository.


