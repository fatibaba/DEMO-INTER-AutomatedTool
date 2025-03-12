# DEMO-INTER-AutomatedTool


DEMO-INTER-AutomatedTool is an automated tool designed to compare and match ontology classes efficiently. It is built for **behavioral scientists, researchers, and other non-technical users** who need to analyze ontology classes.

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

If you are using **Google Colab**, all dependencies are pre-installed.

---

## 🖥️ Running the Tool

You can run the tool in **two different ways**, depending on whether you prefer Jupyter Notebook or Google Colab.

### **1️⃣ Running in Jupyter Notebook (Locally)**

#### **Step 1: Install Dependencies**
If you haven’t installed the required packages, you can do so by running:

```bash
pip install rdflib requests pandas sentence-transformers scikit-learn
