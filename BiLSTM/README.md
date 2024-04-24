# BiLSTM Model

This project is implemented based on bidirectional LSTM and Maxpooling for natural language inference tasks.

## Usage

1. Place   `train.csv`, `dev.csv`, and `test.csv` along with other necessary files in the same directory.

2. Open the `BiLSTM.ipynb` notebook, click on "Run All" to train the BiLSTM model and generate the model file `BiLSTM.h5`.

3. Open the `BiLSTMDemo.ipynb` notebook, click on "Run All" to generate predictions for the test data.

## File Structure

- `BilSTM.ipynb`: Contains the code for training the BiLSTM model.
- `BiLSTMDemo.ipynb`: Contains the code for predicting test data.
- `BiLSTM.h5`: Contains the model ofthe task.
- `BiLSTM.md`: Contains the model card of BiLSTM model.
- `Group_54_B.csv`: Contains the predictions for the test data.

## Notes

- Before running the code, make sure your environment has the required libraries and dependencies installed(Keras and Fasttext).

