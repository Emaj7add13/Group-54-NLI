# BERT Model

This project implements BERT (Bidirectional Encoder Representations from Transformers) model to understand and classify relationships between pairs of sentences.

## Usage

1. Place   `train.csv`, `dev.csv`, and `test.csv` along with other necessary files in the same directory.

2. Open the `NLI_bert.ipynb` notebook, click on "Run All" to train the bert model and generate the model file `bert_model.pth`.

3. Open the bert_demo.ipynb notebook, click on "Run All" to generate predictions for the test data.

## File Structure

- `NLI_bert.ipynb`: Contains the code for training and evaluating the bert model.
- `bert_demo.ipynb`: Contains the code for predicting test data.
- `bert_model.pth`: Contains the trained model.
- `bert_model_card.md`: Contains the model card of bert model.
- `Group_54_C.csv`: Contains the predictions for the test data.

## Notes

- Before running the code, make sure your environment has the required libraries and dependencies installed(Pytorch and transformers).