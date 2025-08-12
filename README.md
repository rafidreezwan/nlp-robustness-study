# Robustness of Sentence Embeddings to Indirect Language

This repository contains the code and data for a comparative study on the robustness of sentence embedding models against standard paraphrasing and indirect, "diplomatic" language.

## Key Findings

A custom dataset was created from 200 negative IMDb movie reviews and used to test five popular sentence-transformer models.

* **Counter-intuitive Result:** All models were surprisingly more robust to standard paraphrasing than to the complex "diplomatic attack" sentences.
* **Top Performer:** The `intfloat/e5-large-v2` model demonstrated the highest overall robustness.

### Model Leaderboard

| Model Name                              | Overall Accuracy | Paraphrasing Accuracy | Diplomatic Accuracy |
| :-------------------------------------- | :--------------: | :-------------------: | :-----------------: |
| `all-MiniLM-L6-v2`                      |      84.50%      |        99.50%         |       69.50%        |
| `all-mpnet-base-v2`                     |      85.25%      |        100.00%        |       70.50%        |
| `BAAI/bge-large-en-v1.5`                |      82.25%      |        100.00%        |       64.50%        |
| `intfloat/e5-large-v2`                  |      86.50%      |        100.00%        |       73.00%        |
| `paraphrase-multilingual-mpnet-base-v2` |      82.50%      |        99.50%         |       65.50%        |

## Repository Contents

* **`.ipynb` Notebook:** Contains all code for data generation, model evaluation, and analysis.
* **`final_hotcake_dataset.csv`:** The full dataset of 400 perturbed sentences.
* **`multi_model_comparison_results_5_models.csv`:** The summary results table.
* **Detailed Reports:** Per-model CSV and TXT files with detailed success/failure analysis.

## How to Run

The experiment can be reproduced using the provided Google Colab notebook. A T4 GPU and an OpenAI API key are required.
