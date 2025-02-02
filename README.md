# TOPSIS Method for Selecting the Best Pretrained Model for Text Generation

## Overview
This project implements the **TOPSIS (Technique for Order of Preference by Similarity to Ideal Solution)** method to evaluate and rank pretrained models for text generation based on multiple performance criteria.

## 1. Models and Evaluation Criteria
The following pretrained models are evaluated:
- **BERT**
- **RoBERTa**
- **XLNet**
- **DistilBERT**
- **ALBERT**

The criteria for evaluation include:
- **Perplexity** (Lower is better)
- **BLEU Score** (Higher is better)
- **ROUGE Score** (Higher is better)
- **Inference Speed** (Higher is better)

### Decision Matrix
| Model      | Perplexity | BLEU Score | ROUGE Score | Inference Speed |
|------------|------------|------------|--------------|-----------------|
| BERT       | 35         | 0.75       | 0.82         | 50              |
| RoBERTa    | 15         | 0.85       | 0.88         | 20              |
| XLNet      | 20         | 0.80       | 0.85         | 30              |
| DistilBERT | 40         | 0.70       | 0.80         | 60              |
| ALBERT     | 25         | 0.78       | 0.84         | 40              |

## 2. Implementation Steps
The **TOPSIS method** is applied using the following steps:
1. **Text Generation** using Hugging Face's Transformers.
2. **Normalization** of the decision matrix.
3. **Weighted normalization** of the decision matrix.
4. **Calculation of ideal best and worst solutions**.
5. **Distance computation** from the ideal solutions.
6. **Calculation of TOPSIS scores** for each model.
7. **Ranking of models** based on the scores.

## 3. Code Execution
The implementation is provided in the Python script: `topsis_textgen.py`.

## 4. Results
### Final Rankings:
The models are ranked based on their **TOPSIS Scores**, where a higher score indicates a better model according to the given criteria.

### TOPSIS Output Visualization:
The analysis includes:
- **Bar chart** displaying the TOPSIS scores of the models.
- **Heatmap** showing the normalized performance metrics.

