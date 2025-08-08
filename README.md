# QSAR Project: CETP Inhibitor Discovery, Data Curation & Drug Repurposing Pipeline

## Abstract

This project develops a QSAR-based workflow targeting **CETP** (Cholesteryl Ester Transfer Protein) for drug discovery and repurposing.\
The pipeline includes early exploratory analysis, curated dataset preparation, and model-ready data generation, alongside a repurposing strategy leveraging FDA-approved drugs. Machine learning model development, hyperparameter tuning, and transfer learning via ChemBERTa are applied to identify promising CETP inhibitors among FDA-approved drugs. Similarity analysis between approved drugs and training data was also performed.\
All notebooks (except `Data_Curation.ipynb`) are designed for Google Colab to ensure easy reproducibility.

---

## Project Structure & Key Files

- **QSAR\_Initial\_Analysis.ipynb**\
  Early data exploration and descriptor checks. This served as the starting point for identifying CETP-related features.

- **Data\_Curation.ipynb**\
  Main source of curated, cleaned datasets used for further modeling and experiments.

- **sec\_notebook\_2.ipynb**\
  Based on Dr. Sina Khosravi's `sec_notebook.ipynb`, with added comments for clarity.

  - Introduces FDA-approved drug data.
  - Forms the backbone of the repurposing workflow.
  - Generates the `main_dataset for train.csv`, later used in `ChemBERTa_Repurposing.ipynb` and `Initial_Repurposing.ipynb`.

- **Initial\_Repurposing.ipynb**\
  Applied various ML classification models with hyperparameter tuning to identify the best-performing model.

- **ChemBERTa\_Repurposing.ipynb**\
  Used ChemBERTa (transfer learning) combined with the best model and parameters from `Initial_Repurposing.ipynb` for repurposing. The final list of best FDA drugs for CETP created in this notebook is available in fda_predictions.csv.

- **Similarity.ipynb**\
  Performs similarity checks between FDA active drugs and training data. Includes additional comparative analyses.

---

## Notes

- Some steps are repeated across notebooks for independent reproducibility.
- The curated dataset from `Data_Curation.ipynb` should be considered the main reference for future work.
- FDA drug data integration, model selection, and similarity metrics provide a foundation for systematic repurposing.


## Acknowledgments
Special thanks to [Dr. Sina Khosravi](https://github.com/khosravisina/anti_CETP) for the original work on the anti-CETP project, which served as a foundation for this repository.

## About me
I am a PharmD candidate at Mashhad University of Medical Sciences in Iran, researching cheminformatics and drug discovery.

## Get in contact with me:
- Email: Mehran.mansouri811@gmail.com
- Telegram: @Mehran_mns
- LinkedIn: http://www.linkedin.com/in/mehran-mansouri-4a7579360
