# Neural_Language_Model_training1.ipynb
Neural Language Model using PyTorch

## Overview

The following project represents the implementation of a neural language model (LSTM) that has been trained on text data from *Pride and Prejudice* by Jane Austen using PyTorch. The goal was to implement the model from scratch, train it, and study how different model configurations (underfit, best fit, overfit) affect performance.

## Steps Done

1. Installed and verified the PyTorch environment, checked GPU availability.
2. Loaded the text dataset and cleaned it (.txt file).
3. Tokenized words, built the vocabulary, and transformed data into numeric sequences.
4. Created training batches and data loaders.
5. Designed and trained an LSTM-based language model to predict the next word.
6. Trained three versions:
- Underfitting (small model, fewer epochs)
Best fit (Balanced model)
- Overfit (big model, more epochs)
7. Calculated validation loss and perplexity for comparison.
Results Summary

|   Model Type   | Embedding | Hidden | Layers | Epochs | Val Loss | Perplexity |
| :------------: | :-------: | :----: | :----: | :----: | :------: | :--------: |
|   ⚠️ Underfit  |     64    |   64   |    1   |    1   |   4.55   |    94.56   |
| ✅ **Best Fit** |    128    |   256  |    2   |    3   | **0.99** |  **2.69**  |
|   🚫 Overfit   |    512    |   512  |    3   |    8   |   0.32   |    1.37    |

This medium-sized model, with 128, 256, 2 layers, and 3 epochs, had the best balance between learning and generalization.

## Outcome

- Successfully trained an LSTM language model from scratch.
- Exhibited underfitting, overfitting, and optimal fitting behavior.
- Models were evaluated using the metrics of validation loss and perplexity.
+ Developed in Google Colab using PyTorch 2.8.0
