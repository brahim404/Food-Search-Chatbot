# Interactive Food Search CLI

A simple command-line food recommendation project using semantic similarity search with ChromaDB.

## Features

- Interactive food search chatbot
- Advanced search menu with filters:
  - Cuisine filter
  - Calorie filter
  - Combined filters
- Demonstration mode for advanced search examples

## Project Files

- `interactive_search.py` - Main interactive chatbot interface
- `advanced_search.py` - Advanced menu-driven search with filters
- `shared_functions.py` - Shared data loading and search utilities

## Requirements

- Python 3.9+
- A food dataset file named `FoodDataSet.json` in the project root
```bash
wget https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/sN1PIR8qp1SJ6K7syv72qQ/FoodDataSet.json

```

Python packages:

- chromadb
- sentence-transformers
- numpy

## Setup

1. Open a terminal in this project folder.
2. (Optional but recommended) Create and activate a virtual environment.
3. Install dependencies.

### Windows (PowerShell)

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install numpy==2.3.1
pip install scipy==1.16.0
pip install chromadb==1.0.12
pip install sentence-transformers==4.1.0
pip install ibm-watsonx-ai==1.3.24

```

### macOS/Linux

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install numpy==2.3.1
pip install scipy==1.16.0
pip install chromadb==1.0.12
pip install sentence-transformers==4.1.0
pip install ibm-watsonx-ai==1.3.24

```

## Run

### Interactive Search CLI

```powershell
python interactive_search.py
```

### Advanced Search CLI

```powershell
python advanced_search.py
```

## Notes

- First run may take longer because the embedding model (`all-MiniLM-L6-v2`) may be downloaded.
- If you get dataset errors, verify `FoodDataSet.json` exists in the same folder as the scripts.
- To exit the interactive mode, use `quit`, `exit`, or `Ctrl+C`.
- If  you encounter error such as  "Failed to send elemetry event ClientCreateCollection event"  execute the command  below  in the terminal to upgrade the chromadb version
    ```bash
    pip install --upgrade chromadb
    ```