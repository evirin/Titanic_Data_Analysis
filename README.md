# Titanic Disaster: Exploratory Data Analysis & Automated Reporting

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Libraries](https://img.shields.io/badge/Libraries-Pandas%20%7C%20Matplotlib%20%7C%20FPDF2-green.svg)]()

An end-to-end Data Science exploratory pipeline built in Python to analyze survival determinants of the 1912 Titanic disaster. The project features robust data cleaning, domain-driven feature engineering, statistical hypothesis testing, and an automated pipeline generating publication-ready PDF reports.

---

## Project Overview

This repository provides an object-oriented analytical workflow that moves from raw passenger data to actionable insights and automated PDF documentation:
- **Modular Pipeline:** Structured with clean OOP classes (`DataLoader`, `DataCleaner`, `ExploratoryAnalysis`, `ReportGenerator`).
- **Feature Engineering:** Imputes missing demographics and derives social/evacuation proxies (`Title`, `FamilySize`, `FamilyType`, `Deck`, `AgeGroup`, `FareCategory`).
- **Statistical Rigor:** Validates observations using Chi-Square tests of independence and independent two-sample t-tests.
- **Automated Reporting:** Generates an aligned, multi-page analytical report (`Titanic_Analysis_Report.pdf`) using `fpdf2` and `matplotlib`.

---

## Key Analytical Findings

* **Overall Survival:** Out of 891 tracked passengers, only **38.4% (342 passengers)** survived.
* **Gender Disparity:** Women had a **74.2%** survival rate compared to only **18.9%** for men, reflecting strict adherence to the maritime protocol of *"women and children first"*.
* **Socioeconomic Hierarchy:** First-class passengers achieved a **63.0%** survival rate, compared to **47.3%** in second class and **24.2%** in third class.
* **Age Demographics:** Children under 12 years old experienced a **58.0%** survival rate, significantly outperforming adults and elderly passengers.
* **Intersection of Class & Gender:** First-class women had the highest survival rate (**96.8%**), whereas third-class men had the lowest (**13.5%**).
* **Statistical Significance:** Chi-square tests confirmed significant relationships with survival for `Sex` ($p < 0.001$), `Pclass` ($p < 0.001$), `Title` ($p < 0.001$), and `FamilyType` ($p < 0.001$).

---

## Project Structure

```text
├── data/
│   └── titanic.csv                  # Raw dataset
├── notebooks/
│   └── titanic_analysis.ipynb       # Complete analysis and execution notebook
├── reports/
│   └── Titanic_Analysis_Report.pdf  # Automatically generated PDF report
├── .gitattributes                   # GitHub language configuration
├── .gitignore                       # Ignored temporary files & cache
├── requirements.txt                 # Project dependencies
└── README.md                        # Documentation

1) Installation & Usage
Clone the repository:
git clone [https://github.com/](https://github.com/)<your-username>/<your-repo-name>.git
cd <your-repo-name>

2) Set up a virtual environment (optional but recommended):
python -m venv venv
# Windows:
venv\Scripts\activate
# macOS/Linux:
source venv/bin/activate

3) Install dependencies:
pip install -r requirements.txt

4)Run the Notebook or Pipeline:
Open titanic_analysis.ipynb in VS Code or JupyterLab and execute all cells:
jupyter notebook

Requirements
a) python >= 3.9
b)pandas
c)numpy
d)matplotlib
e)seaborn
f)scipy
g)fpdf2 >= 2.7.8

License
This project is open-source and available under the MIT License.
