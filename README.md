# CYSE 499/650 Assignment 2 - Sentiment Classification

This repository contains my Stage 1 submission for Assignment 2: Sentiment Classification with Neural Language Models.

## Model

The final model is based on:

`distilbert-base-uncased-finetuned-sst-2-english`

The pretrained sentiment model was fine-tuned on the provided `train.csv` dataset.

Because the training set is imbalanced, balanced sampling was used during fine-tuning.

Most movie reviews were longer than DistilBERT's 512-token limit. During inference, long reviews are divided into overlapping chunks. The model predicts each chunk separately, and the probabilities are averaged to produce the final review prediction.

## Final Public Test Result

- Accuracy: 92.25%
- Balanced Accuracy: 92.25%
- Macro F1: 0.9224

Confusion matrix:

```text
[[177, 23],
 [  8, 192]]



 Repository Files
stage1_notebook.ipynb - model development, training, and evaluation
model_checkpoint/ - saved final model and tokenizer
public_test_predictions.csv - predictions for the public test set
train.csv - provided training data
public_test.csv - provided public test data
requirements.txt - required Python packages
README.md - project instructions


How to Run
Install Python 3.11 or a compatible Python version.
Create a virtual environment:
python -m venv .venv
Activate the environment on Windows:
.venv\Scripts\Activate.ps1
Install the required packages:
pip install -r requirements.txt
Open stage1_notebook.ipynb in Jupyter Notebook or Visual Studio Code.
Run the notebook cells in order.

The saved model can be loaded directly from the model_checkpoint/ folder without retraining.

Labels
0 = Negative
1 = Positive

Use of AI
I used ChatGPT as a support tool to help understand the assignment requirements, organize the notebook, troubleshoot code, and explain model results. I reviewed and ran the code myself and checked the final outputs.