# F1 Spanish Grand Prix 2024 — The Data-Driven Review

A data-driven review and interactive recap of the 2024 Spanish Grand Prix. This project combines data analysis (Python), interactive visualizations (JavaScript), and a static presentation (HTML) to tell the story of the race with charts, tables, and key insights.

Languages
- HTML: 53.3%
- JavaScript: 28.1%
- Python: 18.6%

Table of contents
- [Overview](#overview)
- [What you'll find here](#what-youll-find-here)
- [Demo / Preview](#demo--preview)
- [Tech stack](#tech-stack)
- [Getting started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Install Python dependencies](#install-python-dependencies)
  - [Open the static site / visualizations](#open-the-static-site--visualizations)
- [Project structure](#project-structure)
- [How to reproduce the analysis](#how-to-reproduce-the-analysis)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)
- [Acknowledgements & data sources](#acknowledgements--data-sources)

Overview
--------
This repository documents a data-driven review of the 2024 Spanish Grand Prix. It contains:
- data ingestion and analysis notebooks/scripts (Python),
- interactive charts and UI (JavaScript + D3 / Plotly / charting libs),
- a static website (HTML + CSS) to present the findings.

What you'll find here
---------------------
- Cleaned datasets and raw data (if included in repo)
- Jupyter notebooks or Python scripts used for analysis and model creation
- Interactive visualizations (JS) embedded in the site
- An `index.html` entry point for the static review site

Demo / Preview
--------------
Open `index.html` in a browser to view the static review. For the best experience, serve the site with a simple local server (see below).

Tech stack
----------
- HTML for the static site and layout
- JavaScript for front-end visualizations and interactivity
- Python for data cleaning, analysis, and notebook-driven exploration

Getting started
---------------

Prerequisites
- Python 3.8+
- pip
- (Optional) Node.js & npm if any front-end build tools are used

Install Python dependencies
1. Create and activate a virtual environment (recommended)
   - Linux / macOS:
     ```
     python3 -m venv .venv
     source .venv/bin/activate
     ```
   - Windows (PowerShell):
     ```
     python -m venv .venv
     .\.venv\Scripts\Activate.ps1
     ```

2. Install dependencies:
   ```
   pip install -r requirements.txt
   ```
   If `requirements.txt` is not present, install the typical packages used for analysis:
   ```
   pip install pandas numpy matplotlib seaborn jupyter
   ```

Open Jupyter notebooks
```
jupyter notebook
```
Then open the `.ipynb` analysis notebooks from the notebook UI.

Open the static site / visualizations
- Quick (file): Open `index.html` directly in your browser.
- Recommended (local server):
  ```
  # Python 3
  python -m http.server 8000
  # then visit http://localhost:8000
  ```
- If the site uses a build tool (check for package.json), run:
  ```
  npm install
  npm run build
  npm run serve
  ```

Project structure (suggested / common)
--------------------------------------
- index.html                — static site entry
- assets/                   — images, css, fonts
- js/                       — JavaScript visualization code
- data/                     — raw and processed datasets (csv, json)
- notebooks/                — Jupyter notebooks for analysis
- scripts/                  — Python scripts for ETL / preprocessing
- requirements.txt          — Python dependencies
- README.md                 — this file

How to reproduce the analysis
-----------------------------
1. Ensure raw data is in `data/raw/` (or update paths in scripts/notebooks).
2. Run preprocessing script:
   ```
   python scripts/prepare_data.py --input data/raw --output data/processed
   ```
   (If that script does not exist, open the notebooks and run the cells.)
3. Open the notebooks in `notebooks/` and run cells top to bottom to regenerate figures and tables.
4. If visualizations require JSON outputs, generate them with:
   ```
   python scripts/export_visualization_data.py --input data/processed --output js/data.json
   ```

Contributing
------------
Contributions are welcome! Please:
1. Open an issue describing the change you'd like to make.
2. Create a branch for your feature/fix.
3. Open a pull request with a clear description and any relevant screenshots/outputs.

Guidelines:
- Follow existing code style.
- Add tests where appropriate.
- Update the README if you add new commands or files.

License
-------
This repository does not include an explicit license yet. If you'd like to add one, common options:
- MIT License (permissive)
- Apache 2.0 (permissive + patent protection)
- CC BY 4.0 (for datasets / media)

Add a LICENSE file at the repository root and mention it here.

Contact
-------
Author: Arthavpatel
- GitHub: https://github.com/Arthavpatel

Acknowledgements & data sources
-------------------------------
- Official F1 timing and telemetry sources (link if used)
- Any public datasets, APIs, or scraping scripts used to gather race data
- Libraries used: Pandas, NumPy, Matplotlib/Seaborn, D3/Plotly (update as appropriate)


