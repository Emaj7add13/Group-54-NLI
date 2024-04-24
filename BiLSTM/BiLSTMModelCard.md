---
language: en
license: cc-by-4.0
tags:
- text-classification
repo: https://github.com/Emaj7add13/NLI/blob/main/ESIM.ipynb

---

# Model Card for j20384jz-NLI

<!-- Provide a quick summary of what the model is/does. -->

This is a classification model that was trained to detect whether two pieces of text were written by the same author.


## Model Details

### Model Description

<!-- Provide a longer summary of what this model is. -->

This model is based upon BiLSTM and Mapooling that was fine-tuned on 30K pairs of texts.

- **Developed by:** Jiajun Zhang
- **Language(s):** English
- **Model type:** Supervised
- **Model architecture:** BiLSTM and Maxpooling
- **Finetuned from model [optional]:** [More Information Needed]

### Model Resources

<!-- Provide links where applicable. -->

- **Repository:** [More Information Needed]
- **Paper or documentation:** https://arxiv.org/abs/1605.08900

## Training Details

### Training Data

<!-- This is a short stub of information on the training data that was used, and documentation related to data pre-processing or additional filtering (if applicable). -->

27K pairs of texts drawn from emails, news articles and blog posts.

### Training Procedure

<!-- This relates heavily to the Technical Specifications. Content here should link to that section when it is relevant to the training procedure. -->

#### Training Hyperparameters

<!-- This is a summary of the values of hyperparameters used in training the model. -->


      - optimizer: Adam
      - learning_rate: 0.001
      - train_batch_size: 64
      - eval_batch_size: 64
      - num_epochs: 20

#### Speeds, Sizes, Times

<!-- This section provides information about how roughly how long it takes to train the model and the size of the resulting model. -->


      - overall training time: 3 minutes
      - duration per training epoch: 25 seconds
      - model size: 2.7 MB

## Evaluation

<!-- This section describes the evaluation protocols and provides the results. -->

#### Evaluation Data

3.3K pairs of texts drawn from emails, news articles and blog posts.


### Testing Data & Metrics

#### Testing Data

<!-- This should describe any evaluation data used (e.g., the development/validation set provided). -->

A subset of the development set provided, amounting to 2K pairs.

#### Metrics

<!-- These are the evaluation metrics being used. -->

      - Precision
      - Recall
      - F1-score
      - Accuracy

### Results

The model obtained a precision of 62% and a recall of 74% a F1-score of 67% and an accuracy of 64%.

## Technical Specifications

### Hardware


      - GPU: Colab T4
      - CPU: It is ok to train using CPU but it will be much slower. It takes around 45 minutes.

### Software


      - Keras 2.15.0
      - fasttext-0.9.2
      - NLTK 3.8.1

## Bias, Risks, and Limitations

<!-- This section is meant to convey both technical and sociotechnical limitations. -->

Any inputs (concatenation of two sequences) longer than 120 subwords will be truncated by the model.

## Additional Information

<!-- Any other information that would be useful for other people to know. -->

The hyperparameters were determined by experimentation with different values.
