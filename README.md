# Multi-Variant Text Analysis and Generation

## Overview
This project implements and compares three distinct NLP architectures on the Rotten Tomatoes movie review dataset:

| Variant | Task | Model |
|---|---|---|
| BERT | Sentiment Classification | bert-base-uncased |
| GPT | Causal Text Generation | distilgpt2 |
| Text-GAN | Adversarial Text Generation | Custom LSTM + 1D-CNN |

## Dataset
[Rotten Tomatoes on Hugging Face](https://huggingface.co/datasets/cornell-movie-review-data/rotten_tomatoes/tree/main)

See [DATASET.md](DATASET.md) for source details and local parquet file descriptions.

## How to Run
1. Clone this repository
2. Install dependencies:
   ```bash
   pip install torch transformers datasets pyarrow pandas scikit-learn evaluate rouge-score nltk accelerate
   ```
3. Open `Multi_Variant_Text_Analysis_and_Generation.ipynb` in Jupyter or Google Colab
4. Run all cells

## Files
- `Multi_Variant_Text_Analysis_and_Generation.ipynb` - Main notebook with all three model pipelines
- `CapuzIvan_NLP.pdf` - Full project documentation and analysis report
- `DATASET.md` - Dataset source link and file descriptions
- `train.parquet` / `validation.parquet` / `test.parquet` - Dataset splits from [Hugging Face](https://huggingface.co/datasets/cornell-movie-review-data/rotten_tomatoes/tree/main)

## Evaluation Metrics
- **BERT**: Precision, Recall, F1-Score
- **GPT-2**: Perplexity, BLEU, ROUGE-L
- **Text-GAN**: Discriminator Accuracy, BLEU, ROUGE-L
