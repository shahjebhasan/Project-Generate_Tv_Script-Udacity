# Project-Generate_Tv_Script-Udacity

# Project Overview
This project is based on the TV Script Generation repo for the Udacity Deep Learning NanoDegree.

It generates its own Seinfeld TV scripts using RNNs and a Seinfeld dataset of scripts from 9 seasons. The Neural Network will generate a new, "fake" TV script.

# Pre-processing Data
The function create_lookup_tables return these dictionaries as a tuple (vocab_to_int, int_to_vocab).
The function token_lookup returns a dict that can correctly tokenizes the provided symbols.
# Batching Data
The function batch_data breaks up word id's into the appropriate sequence lengths, such that only complete sequence lengths are constructed.
In the function batch_data, data is converted into Tensors and formatted with TensorDataset.
Finally, batch_data returns a DataLoader for the batched training data.
# Build the RNN
The RNN class has complete __init__, forward , and init_hidden functions.
The RNN include an LSTM or GRU and at least one fully-connected layer. 
The loss reached a value lower than 3.5 i.e; 3.23 which is a pretty good loss .
# Adjusted Hyperparameters
sequence_length = 10
batch_size = 128
num_epochs = 10
learning_rate = 0.001
embedding_dim = 300
hidden_dim = 250
n_layers = 2

