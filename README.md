# Hybrid-LSTM-and-GRU-architecture-for-Hate-Speech-Detection
Here we are proposing a hybrid model architecture that combines both LSTM and GRU layers.
Here’s a step-by-step breakdown of the hybrid RNN model design:
1. Input Layer:
The input layer accepts sequences of tokenized text data with a fixed length (maxlen).
2. Embedding Layer:
The embedding layer transforms input sequences into dense vectors of fixed size (100 in this case). This layer captures semantic relationships between words.
3. Bidirectional LSTM Layer:
A bidirectional LSTM layer with 128 units is used to capture long-term dependencies from both past and future contexts in the input sequences.
4. Bidirectional GRU Layer:
A bidirectional GRU layer with 128 units follows the LSTM layer. This layer continues to process the sequential data, providing additional context and managing long-term dependencies with fewer parameters.
5. GRU Layer:
A unidirectional GRU layer with 128 units processes the outputs from the bidirectional GRU layer, further refining the learned representations.
6. Dense Layers with Dropout and Batch Normalization:
A dense layer with 64 units and ReLU activation processes the GRU layer's output.
Batch normalization is applied to stabilize and accelerate training.
Dropout with a rate of 0.5 is used to prevent overfitting.
Another dense layer with 32 units and ReLU activation, followed by batch normalization and dropout, refines the features before the final classification.
7. Output Layer:
The output layer is a dense layer with a single unit and sigmoid activation, providing a binary classification output for hate speech detection.


![Model Diagram](https://github.com/mdjubaer12/Hybrid-LSTM-GRU-Hate-Speech-Detection/assets/62115876/902cd788-9c0c-4dc4-9ec9-d651779cdba6)
