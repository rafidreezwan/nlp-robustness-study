A Comparative Study on the Robustness of Sentence Embeddings to Indirect Language
This repository contains the code, data, and results for a research project investigating the robustness of modern sentence embedding models against standard paraphrasing and indirect, "diplomatic" language.

Project Overview
This project tests the robustness of sentence embedding models against two types of semantic perturbations: standard paraphrasing and indirect, "diplomatic" language. A dataset was created from 200 negative IMDb movie reviews. Five popular sentence-transformer models (all-MiniLM-L6-v2, all-mpnet-base-v2, BAAI/bge-large-en-v1.5, intfloat/e5-large-v2, and paraphrase-multilingual-mpnet-base-v2) were evaluated.

Results
The key finding is that all models performed better on standard paraphrases than on the complex "diplomatic attack" sentences. This challenges the assumption that indirect language is inherently more difficult for these models. intfloat/e5-large-v2 demonstrated the highest overall robustness.

Final Model Leaderboard:
| Model Name | Overall Accuracy | Paraphrasing Accuracy | Diplomatic Accuracy |
| :--- | :---: | :---: | :---: |
| all-MiniLM-L6-v2 | 84.50% | 99.50% | 69.50% |
| all-mpnet-base-v2 | 85.25% | 100.00% | 70.50% |
| BAAI/bge-large-en-v1.5 | 82.25% | 100.00% | 64.50% |
| intfloat/e5-large-v2 | 86.50% | 100.00% | 73.00% |
| paraphrase-multilingual-mpnet-base-v2 | 82.50% | 99.50% | 65.50% |

How to Run
All code, analysis, and setup steps are contained within the .ipynb Google Colab notebook included in this repository. The notebook requires a Google Colab environment with a T4 GPU and an OpenAI API key for the diplomatic sentence generation.

Files
final_hotcake_dataset.csv: The final dataset of 400 perturbed sentences for evaluation.

multi_model_comparison_results_5_models.csv: The final summary table of model accuracies.

detailed_results_[model_name].csv: A CSV file for each model with its prediction for every sentence.

qualitative_report_[model_name].txt: A text file for each model listing its specific failures and some successes.
