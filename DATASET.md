# Dataset Source

This project uses the **Rotten Tomatoes** movie review dataset for sentiment classification and text generation.

**Hugging Face:** [cornell-movie-review-data/rotten_tomatoes](https://huggingface.co/datasets/cornell-movie-review-data/rotten_tomatoes/tree/main)

## Local Files

The following parquet splits are included in this repository:

| File | Description |
|---|---|
| `train.parquet` | Training split |
| `validation.parquet` | Validation split |
| `test.parquet` | Test split |

Each file contains `text` (review) and `label` (0 = negative, 1 = positive) columns.

## Download from Hugging Face

```python
from datasets import load_dataset

dataset = load_dataset("cornell-movie-review-data/rotten_tomatoes")
```

Or download the parquet files directly from the [dataset files page](https://huggingface.co/datasets/cornell-movie-review-data/rotten_tomatoes/tree/main).
