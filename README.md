# Veterinary Pharmacovigilance Analysis with Python

Exploratory pharmacovigilance analysis of FDA veterinary adverse event reports focused on dogs and cats, using Python and Jupyter Notebook.

## Title
Veterinary Drug Safety in Dogs and Cats with Python

## Challenge
Identify the most reported drugs, reactions, and risk patterns in companion animals (dog and cat only), and go beyond descriptive charts by adding:
- Breed-level exploration
- Formal signal detection using PRR
- Time and seasonal trend analysis

## Process
Tools and workflow used:
- Python, Pandas, NumPy
- Matplotlib, Seaborn
- Jupyter Notebook
- FDA OpenFDA API (`animalandveterinary/event`)
- Git and GitHub

Main steps:
1. Pulled 1,000 adverse event records from the FDA API.
2. Cleaned nested fields (`drug`, `reaction`, `outcome`, animal attributes).
3. Standardized labels and improved chart readability.
4. Filtered analysis to dogs and cats only.
5. Built descriptive visuals (top drugs, reactions, species, outcomes, yearly trends).
6. Added advanced analyses:
	- Breed distribution and Ivermectin-by-breed chart
	- Proportional Reporting Ratio (PRR) safety signal detection
	- Monthly seasonality and year-month heatmap
7. Summarized findings and limitations for practical pharmacovigilance interpretation.

## Result
What changed (numbers and lessons):
- Dogs represented most reports (~87%) vs cats (~13%).
- Top reported drugs were antiparasitics (Spinosad, Ivermectin, Selamectin).
- Most frequent reactions included vomiting/emesis and efficacy-related outcomes.
- Strong PRR signal found for Spinosad -> Emesis (PRR 138), with additional elevated signals for specific drug-reaction pairs.
- Seasonal pattern observed, with higher average reporting around spring/summer months.
- Key lesson: combining descriptive EDA with pharmacovigilance metrics (PRR) and breed/season stratification provides more actionable safety insights than counts alone.

## Project Objective
Analyze veterinary adverse event reports to detect clinically meaningful safety patterns by species, breed, reaction type, severity, and timing.

## Dataset
Source: FDA OpenFDA Veterinary Adverse Event API
- Endpoint used: `https://api.fda.gov/animalandveterinary/event.json?limit=1000`
- Scope used in this notebook: dogs and cats only

Core fields analyzed include:
- Drug information (`active_ingredients`)
- Reaction terms (`veddra_term_name`)
- Outcome medical status
- Animal species and breed
- Report receive date

## Analysis Scope
- Data cleaning and preprocessing of nested API JSON
- Drug and adverse reaction frequency analysis
- Species-only filtering (dog/cat)
- Outcome severity distribution
- Yearly trend analysis
- Breed-level analysis
- PRR safety signal detection
- Seasonal trend analysis (monthly averages + heatmap)

## Business/Clinical Questions Answered
- Which drugs appear most often in adverse event reports for dogs and cats?
- Which adverse reactions are most common?
- Are specific breeds overrepresented in key drug reports (e.g., Ivermectin)?
- Which drug-reaction pairs are statistically disproportionate (PRR >= 2)?
- Are there seasonal reporting patterns that align with treatment cycles?

## Key Findings
- Reports are concentrated in a limited set of antiparasitic drugs.
- Gastrointestinal reactions and efficacy-related events are highly represented.
- Labrador Retrievers are highly represented overall and in Ivermectin reports.
- PRR highlighted high-priority signals beyond simple count-based rankings.
- Reporting intensity is not uniform across months; seasonality is visible.

## How to Use
1. Clone this repository.
2. Open `veterinary-pharmacovigilance-analysis.ipynb` in Jupyter or VS Code.
3. Run all cells to reproduce data extraction, preprocessing, and visual analysis.
4. Review the final insight and conclusion sections for interpretation.

## Resume Bullet Version (EN)
Veterinary Pharmacovigilance Analysis | Data Analytics Portfolio Project (2026)

- Built an end-to-end pharmacovigilance analysis in Python using FDA veterinary adverse event data focused on dogs and cats.
- Cleaned nested JSON API data and produced visual analytics for drug frequencies, reactions, outcomes, and time trends.
- Implemented PRR-based signal detection and breed/season stratified analysis to generate clinically relevant drug safety insights.
- Skills used: Python, Pandas, NumPy, Matplotlib, Seaborn, EDA, Jupyter Notebook, API Analysis, Git/GitHub.

## Resume Bullet Version (ES)
Analisis de Farmacovigilancia Veterinaria | Proyecto de Portafolio de Analitica de Datos (2026)

- Desarrolle un analisis de farmacovigilancia de extremo a extremo en Python usando datos de eventos adversos veterinarios de la FDA para perros y gatos.
- Limpie datos API en formato JSON anidado y genere visualizaciones para frecuencias de farmacos, reacciones, severidad y tendencias temporales.
- Implemente deteccion de senales con PRR y analisis estratificado por raza y estacionalidad para producir hallazgos clinicamente relevantes.
- Habilidades usadas: Python, Pandas, NumPy, Matplotlib, Seaborn, EDA, Jupyter Notebook, analisis de APIs, Git/GitHub.

## Tools
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook
- Git/GitHub

## Repository Structure
- `veterinary-pharmacovigilance-analysis.ipynb`: full workflow and visual analysis
- `README.md`: project documentation

## Author
Project developed by Anuar Valdez as part of his data analytics portfolio.