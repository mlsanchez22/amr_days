# Antimicrobial Treatment Duration in Multidrug-Resistant Infections (MIMIC-IV Study)

This repository contains code and documentation for a research project aimed at optimizing the **duration of antibiotic therapy** in patients with infections caused by multidrug-resistant (MDR) bacteria, using data from the **MIMIC-IV v3.1** database hosted in Google BigQuery.

## 📌 Project Overview
Antibiotic overuse contributes to the emergence of antimicrobial resistance, adverse events, and increased healthcare costs.  
While empirical broad-spectrum therapy is often necessary in critically ill patients, the **optimal duration of treatment** for MDR infections remains uncertain.  

This project investigates whether **shorter courses of antibiotics** may achieve **clinical and/or microbiological cure** without compromising patient outcomes, compared to standard guideline-recommended durations.

## 🎯 Objectives
- Build cohorts of hospitalized patients with **confirmed infections by MDR bacteria**.
- Group patients into **six microorganism–antibiotic blocks**:
  1. Enterobacterales with ceftriaxone, cefepime, or ceftazidime  
  2. Enterobacterales with carbapenems  
  3. *Pseudomonas aeruginosa* / *Acinetobacter spp.* with carbapenems  
  4. *Stenotrophomonas maltophilia* with trimethoprim–sulfamethoxazole (TMP-SMX)  
  5. *Enterococcus faecium* with vancomycin  
  6. *Staphylococcus aureus* (MSSA/MRSA) with oxacillin
- Measure the **actual duration of antibiotic therapy**.
- Evaluate the association between treatment duration and **clinical/microbiological improvement**.
- Adjust for confounders: age, sex, comorbidities, immunosuppression, type of admission (ICU vs ward), and specimen type.

## 📊 Data Source
The project uses the **MIMIC-IV v3.1** database, accessed through **Google BigQuery**.  
Access requires PhysioNet credentialing, CITI training, and DUA approval.  
For more details: [MIMIC-IV on PhysioNet](https://physionet.org/content/mimiciv/).

## 🛠️ Repository Structure
- `sql/` → BigQuery SQL queries to build cohorts and define microorganism–antibiotic blocks.
- *`notebooks/` → Jupyter/Colab notebooks for data extraction and exploratory analysis./*
- *`scripts/` → Python utilities for cleaning, feature engineering, and statistical analysis./*
- *`docs/` → Project documentation and diagrams (study flowchart, cohort definitions, etc.)./*  

## 📈 Planned Outputs
- Flowchart of inclusion/exclusion criteria.  
- Descriptive Table 1 (baseline characteristics stratified by clinical/microbiological outcome).  
- Analysis of treatment duration across blocks.  
- (Optional) Predictive model for early cure with reduced treatment duration.  

## 🤝 Contributions
This project is under active development. Contributions, suggestions, and collaborations are welcome!  

---

⚠️ **Disclaimer**: This research uses de-identified clinical data from MIMIC-IV. All analyses comply with PhysioNet’s data use agreement (DUA) and should not be interpreted as clinical recommendations.
