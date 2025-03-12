# DEMO-INTER-AutomatedTool

The **DEMO-INTER-AutomatedTool** streamlines the process of identifying matching classes across ontologies. This tool automates the matching process, making it more efficient, scalable, and systematic, allowing researchers to focus on reviewing results rather than performing exhaustive manual searches.  

## **How It Works**  

The tool follows a **three-step approach** to class matching:  

1️⃣ **Class IRI Matching:** Finds identical class **IRIs (unique ontology identifiers)** across two ontologies to quickly highlight direct overlaps.  

2️⃣ **Class Label & Synonym Matching:** Recognizes conceptually similar classes that have different labels by checking for alternative terms, synonyms, and related terminology using ontology properties.  

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
Open the file [JupyterNotebook_AutomatedTool.ipynb](JupyterNotebook_AutomatedTool.ipynb) from the repository.

#### **Follow the Instructions:**
The notebook is divided into three main sections corresponding to each step of the matching process. Run each cell in every section to complete the three steps:

1. **IRI Matching:**
Identify classes with identical IRIs.
2. **Label and Synonym Matching:**
Find classes with matching labels and synonyms.
3. **Definition Matching:**
Compare class definitions using automated matching.

For each step:

- Choose to load your ontology either via a URL or a local file path.
- Provide the path to the CSV file containing your target classes and the base IRI.
- The tool will extract class definitions, perform the matching, and display the results in a table.
- A download link for a CSV file with the results will be provided at the end.
