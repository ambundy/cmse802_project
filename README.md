# cmse802_project
Repository for Final Project for CMSE 802 at MSU Fall 2025

# CMSE 802 Project: Modeling Student Pathways with Markov Chains

## Project Description
Gateway mathematics courses such as Precalculus (MTH 116), Calculus I (MTH 132), and Calculus II (MTH 133) are critical for student success in STEM majors. Prior performance in one course strongly influences outcomes in subsequent courses, and institutional policies (e.g., prerequisites, grade thresholds, or academic support) can alter these pathways in significant ways. 

The dataset provided by MSU's Mathematics department contains cross-tabulated student outcomes: for each focal course, we know how students with particular grades in previous courses performed. This structure naturally lends itself to probabilistic modeling. By representing grade progressions as a Markov chain, we can simulate student trajectories through the math sequence using transition probabilities. Monte Carlo simulations will estimate student outcomes under baseline conditions. By introducing policy perturbations,, “what-if” scenarios (such as grade inflation, stricter prerequisites, or targeted support) will be explored to quantify how small changes in early course performance affect downstream success.

The project will combine probabilistic modeling, simulation, and sensitivity analysis, and the results can highlight key leverage points for improving student outcomes.

---

## Project Objectives
1. **Cleaned dataset and validated baseline transition matrices** for at least two key course sequences (MTH 116 → 132, MTH 132 → 133) by the end of the seventh week of the semester (October 10).
2. **Monte Carlo simulation results** based on at least 10,000 simulated student trajectories through the 116 → 132 → 133 sequence by the end of the ninth week of the semester (October 24), reporting baseline outcome distributions (e.g., the percentage of students earning at least 3.0 in Calc II).
3. **Policy scenario analyses**, comparing at least 2 “what-if” cases (e.g., grade inflation, stricter prerequisites, targeted support) against the baseline outcome distributions by the end of the eleventh week (November 7) of the semester, summarizing results using clear visualizations and summary tables.
4. **Synthesizing methods, results, and implications for student success**, including sensitivity analysis results highlighting which grade transitions most strongly affect downstream outcomes by the end of the thirteenth week (November 21)
5. **Present and refine**: Develop final deliverables consisting of a presentation (by November 25) and written report (incorporating feedback from the presentation) by the end of the fifteenth week (December 5).

---

## Setup Instructions

### Clone the Repository 
```bash
git clone <your-repo-url>
cd CMSE802-Project
conda env create -f environment.yml
```

### Repository Structure
```bash
- **data/**
  - `raw/`: Original datasets (Google Sheets exported as CSV). These should remain unmodified.
  - `processed/`: Cleaned and reshaped datasets, including transition matrices used in simulations.

- **notebooks/**
  - Jupyter notebooks for step-by-step analysis:
    - `01_exploration.ipynb`: Data cleaning and exploratory analysis.
    - `02_baseline_model.ipynb`: Markov chain and Monte Carlo baseline simulations.
    - `03_scenarios.ipynb`: Policy perturbation and "what-if" analyses.
    - `04_sensitivity.ipynb`: Sensitivity analysis and visualization.

- **src/**
  - Python modules with reusable functions:
    - `data_prep.py`: Data cleaning and preprocessing functions.
    - `markov_model.py`: Markov chain modeling and Monte Carlo simulation functions.
    - `scenarios.py`: Functions for policy adjustments and scenario testing.
    - `visualize.py`: Functions for producing heatmaps, Sankey diagrams, and comparison plots.

- **results/**
  - Project outputs:
    - `figures/`: Visualization files (PNG, PDF).
    - `tables/`: Summary tables in CSV or Excel format.
    - `reports/`: Written drafts, slides, and final report deliverables.

- **docs/**
  - Supporting documentation:
    - `proposal.md`: Initial project plan/proposal.
    - `references.bib`: Reference list in BibTeX/APA format (if needed).

- **tests/**
  - Unit tests for validating core functions and ensuring reproducibility.

- **.gitignore**
  - Specifies files/folders not to be tracked (large datasets, temporary files, etc.).

- **environment.yml / requirements.txt**
  - Lists Python dependencies to reproduce the environment.

- **README.md**
  - This file. Provides project overview and folder explanations.

---

```
