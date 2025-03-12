# DEMO-INTER-AutomatedTool

The **DEMO-INTER-AutomatedTool** streamlines the process of identifying matching classes across ontologies. This tool automates the matching process, making it more efficient, scalable, and systematic, allowing researchers to focus on reviewing results rather than performing exhaustive manual searches.  

## **How It Works**  

The tool follows a **three-step approach** to class matching:  

1️⃣ **Class IRI Matching:** Finds identical class **IRIs (unique ontology identifiers)** across two ontologies to quickly highlight direct overlaps.  

2️⃣ **Class Label & Synonym Matching:** Recognizes conceptually similar classes that have different labels by checking for alternative terms, synonyms, and related terminology using ontology properties.  

3️⃣ **Class Definition Matching:** Applies **natural language processing (NLP)** and a **quantized Llama 3 language model** to analyze class definitions, enabling detection of semantically equivalent concepts even when labels differ.  

### **Key Features**  

This tool allows you to:
- Load ontologies from **a URL** or **a local file**.
- Extract **ontology class labels, definitions, and synonyms**.
- Identify matches between two ontologies or between an ontology and a target class list.
- Display results in a **structured table** and generate a **downloadable CSV file**.

---

## 📂 Repository Contents

This repository provides two different environments for running the tool:

| File | Description |
|------|------------|
| `JupyterNotebook_AutomatedTool.ipynb` | Jupyter Notebook version for running locally on your computer. |
| `GoogleColab-Automated_tool.ipynb` | Google Colab version for running in the cloud without installation. |

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

You can run the tool in **two different ways**, depending on whether you prefer Jupyter Notebook or Google Colab.

### **1️⃣ Running in Jupyter Notebook (Locally)**

#### **Step 1: Install Dependencies**
If you haven’t installed the required packages, you can do so by running:

```bash
pip install rdflib requests pandas sentence-transformers scikit-learn mlx-lm torch torchvision torchaudio
