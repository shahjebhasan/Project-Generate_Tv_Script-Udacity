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
# NOTE
The following project iterates over a large amount of data, and it's expected to take a number of hours to train, even on GPU.
it took me around an hour to train the complete model.It is important to avoid wasting GPU time in Workspace projects that have GPU acceleration enabled. The benefits of GPU acceleration are most useful when evaluating deep learning models—especially during training. In most cases, you can build and test your model (including data pre-processing, defining model architecture, etc.) in CPU mode, then activate GPU mode to accelerate training.
