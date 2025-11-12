# Neural_Language_Model_training1.ipynb
Neural Language Model using PyTorch

## Overview

The next project can be described as the use of a neural language model (LSTM) which has been pre-trained on the text content in Pride and Prejudice by Jane Austen with the help of PyTorch. Its purpose, then, was to go through with the process of model implementation, training and exploring the impact of various configurations of models (underfit, best fit, overfit) on performance.


## Steps Done

1. created and tested the PyTorch installation, verified the presence of GPUs.
2. Prepared the text data and cleaned it (.txt file).
3. Coded words, developed the vocabulary, and converted the data into sequences of numbers.
4. Developed training batches and data loaders.
5. Trained and designed an LSTM-based language model which predicts the next word.
6. Trained three versions:
- Underfitting (small model, fewer epochs)
- Best fit (Balanced model)
- Overfit (big model, more epochs)
7. Comparison of validation loss and perplexity are calculated.
   Summary of different trained models:

|   Model Type   | Embedding | Hidden | Layers | Epochs | Val Loss | Perplexity |
| :------------: | :-------: | :----: | :----: | :----: | :------: | :--------: |
|   ⚠️ Underfit  |     64    |   64   |    1   |    1   |   4.55   |    94.56   |
| ✅ **Best Fit** |    128    |   256  |    2   |    3   | **0.99** |  **2.69**  |
|   🚫 Overfit   |    512    |   512  |    3   |    8   |   0.32   |    1.37    |

This 128, 256, 2 layers, and 3 epochs model had the optimal balance of learning and generalization.

## Outcome

- Trained an LSTM language model, trained successfully, without transfers.
- Displayed underfitting, overfitting and optimal fitting.
- The metrics used in the evaluation of models were the validation loss and perplexity.
##### Written in PyTorch 2.8.0 and developed in Google Colab.
