# Coreference Resolution

This is the implementation of the Coreference Resolution system build using Deep Neural Network.  

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites

The Libraries which have been used to build this system are:

```
Spacy
Numpy
Gensim
PyTorch
Matplotlib
```

The english language model has been used from spaCy for extracting the linguistic fratures.
```
python -m spacy download en
```

The mention detection system that has been used as part of this work is from [neural coref](https://github.com/huggingface/neuralcoref)

The GloVe word embeddings from Stanford have been used in this work which can be downloaded from [here](https://nlp.stanford.edu/projects/glove/)

### Dataset

The CoNLL-2012 Shared coreference dataset has been used to train the neural network for this work which can be downloaded from [here](http://conll.cemantix.org/2012/data.html)


### Information about the notebooks

1. All the work has been implemented using Jupyter notebooks.

2. The parsing of the ConLL-2012 dataset to extract the features and prepare the training data has been implemented in notebooks/parse_conll_dataset.

3. The two neural network models used in this work are with bunary classification and probability as output and have been implemented in notebooks/FFNN_binary_classification and notebooks/FFNN_probability.

4. To check the real world examples for the trained model has been implemented in notebooks/ResolveCoreference.

5. The analysis performed on the entites and the mentions has been implemented in notebooks/mention-ner_comparison

### Training the Neural Network
Steps that needs to be performed to train the neural network are as follows:
1. Extract the features to prepare the training data by running the notebooks/parse_conll_dataset
2. Run the notebook in notebooks/FFNN_probability to train a model. The code is implemented in a way that everytime a model with better F1 score is encountered, it is saved.

### Trained models
The trained models are present in models folder.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details
