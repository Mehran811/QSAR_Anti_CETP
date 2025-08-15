# QSAR Project: CETP Inhibitor Discovery, Data Curation & Drug Repurposing Pipeline

## Abstract

This project develops a QSAR-based workflow targeting **CETP** (Cholesteryl Ester Transfer Protein) for drug discovery and repurposing.\
The pipeline includes early exploratory analysis, curated dataset preparation, and model-ready data generation, alongside a repurposing strategy leveraging FDA-approved drugs. Machine learning model development, hyperparameter tuning, and transfer learning via ChemBERTa are applied to identify promising CETP inhibitors among FDA-approved drugs. Similarity analysis between approved drugs and training data was also performed.\
Most notebooks (except `Data_Curation.ipynb` and `feature_selection.ipynb`) are designed for Google Colab to ensure easy reproducibility.

---


## Workflow
1. The cleaner pipeline used in my recent work. These files are not complete but you can use them and understand them easier. These two are not designed for Google Colab.

    A [`Data_Curation.ipynb`] --> B [`feature_selection.ipynb`] 


2. The files I started with and resulted in the final repurposed drug list. You can upload them in Google Colab and use them.

   - A [`QSAR_Initial_Analysis.ipynb`  (Early exploratory analysis)] --> B [`s`ec_notebook_2.ipynb`  (FDA data integration, feature selection, & main_dataset creation)]  

   - B --> C [`Initial_Repurposing.ipynb`  (ML models & hyperparameter tuning)]  

   - C --> D [`Similarity.ipynb`  (FDA vs. training data similarity checks)]  

   - D --> E [`ChemBERTa_Repurposing.ipynb`  (Transfer learning & final repurposed drug list)]  

---

## Project Structure & Key Files

1. **New Workflow**

- **Data\_Curation.ipynb**\
  Main source of curated, cleaned datasets used for further modeling and experiments.

- **Feature\_Selection.ipynb**\
  Data analysis and model recommendation, Adding features from RDKit descriptors and various fingerprints, SHAP to understand feature importance, feature selection according to the percentile of the highest scores, and final comparison was done in this file.

2. **Basis Workflow**

- **QSAR\_Initial\_Analysis.ipynb**\
  Early data exploration and descriptor checks. This served as the starting point for identifying CETP-related features.

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
- FDA drug data integration, model selection, and similarity metrics provide a foundation for systematic repurposing.


## Acknowledgments
Special thanks to [Dr. Sina Khosravi](https://github.com/khosravisina/anti_CETP) for the original work on the anti-CETP project, which served as a foundation for this repository.

## About me
I am a PharmD candidate at Mashhad University of Medical Sciences in Iran, researching cheminformatics and drug discovery.

## Get in contact with me:
- Email: Mehran.mansouri811@gmail.com
- Telegram: @Mehran_mns  
- [LinkedIn](http://www.linkedin.com/in/mehran-mansouri-4a7579360)
