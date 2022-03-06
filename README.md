# NLP_machineTranslation
# Goal
In this project, we build a deep neural network that functions as part of a machine translation pipeline. The pipeline accepts English text as input and returns the korean translation. The goal is to achieve the highest translation accuracy possible.


# Building the Pipeline

Below is a summary of the various preprocessing and modeling steps. The high-level steps include:

Preprocessing: load and examine data, cleaning, tokenization, padding
Modeling: build, train, and test the model
Prediction: generate specific translations of English to Korean, and compare the output translations to the ground truth translations
Iteration: iterate on the model

# Modeling
First, let's breakdown the architecture of a RNN at a high level. Referring to the diagram above, there are a few parts of the model we to be aware of:

Inputs — Input sequences are fed into the model with one word for every time step. Each word is encoded as a unique integer or one-hot encoded vector that maps to the English dataset vocabulary.

Embedding Layers — Embeddings are used to convert each word to a vector. The size of the vector depends on the complexity of the vocabulary.
Recurrent Layers (Encoder) — This is where the context from word vectors in previous time steps is applied to the current word vector.
Dense Layers (Decoder) — These are typical fully connected layers used to decode the encoded input into the correct translation sequence.
Outputs — The outputs are returned as a sequence of integers or one-hot encoded vectors which can then be mapped to the KOrean dataset vocabulary.

# Install
Python 3
NumPy
TensorFlow 1.x
Keras 2.x
