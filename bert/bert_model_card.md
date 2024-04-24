---
{}
---
language: en
license: cc-by-4.0
tags:
- text-classification
repo: https://github.com/Emaj7add13/Group_54_NLI

---

# Model Card for Model Card for h50141yq-NLI

<!-- Provide a quick summary of what the model is/does. -->

This is a classification model build by bert which was trained to detect whether two pieces of text were written by the same author.


## Model Details

### Model Description

<!-- Provide a longer summary of what this model is. -->

This is a BERT-based natural language inference (NLI) classification model designed to understand and classify relationships between pairs of sentences and has been fine-tuned specifically for the task of NLI using a dataset of paired premises and hypotheses.

- **Developed by:** Yituo Qian
- **Language(s):** English
- **Model type:** Supervised
- **Model architecture:** Transformers
- **Finetuned from model [optional]:** bert-base-uncased

### Model Resources

<!-- Provide links where applicable. -->

- **Repository:** https://huggingface.co/google-bert/bert-base-uncased
- **Paper or documentation:** https://aclanthology.org/N19-1423.pdf

## Training Details

### Training Data

<!-- This is a short stub of information on the training data that was used, and documentation related to data pre-processing or additional filtering (if applicable). -->

This dataset consists of three sections: premise, hypothesis, and label. each row represents a sample where: 'The premise field contains an assertion or factual narrative. The 'hypothesis field contains a hypothetical sentence. label field is a binary label that marks whether the hypothesis is (1) or not (0).

### Training Procedure

<!-- This relates heavily to the Technical Specifications. Content here should link to that section when it is relevant to the training procedure. -->

#### Training Hyperparameters

<!-- This is a summary of the values of hyperparameters used in training the model. -->


      - learning_rate: 2e-05
      - train_batch_size: 16
      - eval_batch_size: 16
      - num_epochs: 1

#### Speeds, Sizes, Times

<!-- This section provides information about how roughly how long it takes to train the model and the size of the resulting model. -->


      - overall training time: 456 seconds
      - duration per training epoch: 456 seconds
      - model size: 417.77 MB

## Evaluation

<!-- This section describes the evaluation protocols and provides the results. -->

### Testing Data & Metrics

#### Testing Data

<!-- This should describe any evaluation data used (e.g., the development/validation set provided). -->

A test set provided, amounting to 3K pairs.

#### Metrics

<!-- These are the evaluation metrics being used. -->


      - Precision
      - Recall
      - F1-score
      - Accuracy

### Results

The model obtained an F1-score of 82%, an accuracy of 82%, a recall of 81%, and a precision of 83%.

## Technical Specifications

### Hardware


      - RAM: at least 16 GB
      - Storage: at least 2GB,
      - GPU: RTX 3070

### Software


      - Transformers 4.40.0
      - Pytorch 2.2.1+cu121

## Bias, Risks, and Limitations

<!-- This section is meant to convey both technical and sociotechnical limitations. -->

The model processes inputs with a maximum token length(128) and will truncate longer sequences.  It may show some biases in the proformance.

## Additional Information

<!-- Any other information that would be useful for other people to know. -->

The initial model performed well, so there was not much tweaking done to the hyperparameters.
