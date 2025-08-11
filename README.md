# nlp-robustness-study
An experiment to test the robustness of NLP models to semantic-preserving perturbations
# NLP Model Robustness Study

This project investigates the robustness of the `all-MiniLM-L6-v2` SentenceTransformer model against semantic-preserving perturbations.

## Description

A dataset was constructed using 200 negative sentences from the IMDb movie review dataset. Two perturbation methods were applied:
1.  **Back-Translation** (English -> German -> English)
2.  **AI Paraphrasing** (using `tuner007/pegasus_paraphrase`)

The model was then evaluated on its ability to correctly identify the original source sentence from the perturbed version.

## How to Run

All code, analysis, and setup steps are contained within the `NLP_Robustness_Experiment.ipynb` Google Colab notebook.

## Results

The model demonstrated high robustness, achieving an **overall accuracy of 99%** (396/400 correct identifications).

- **`experiment_results.csv`**: Contains a detailed log of each prediction.
- **`imdb_perturbation_dataset.csv`**: The full dataset of 400 perturbed sentences and their original sources.
