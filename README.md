# LSTM-Structure-and-Hidden-State
This hidden state is a function of the pieces of data that an LSTM has seen over time; it contains some weights and, represents both the short term and long term memory components for the data that the LSTM has already seen.
We know that RNNs are used to maintain a kind of memory by linking the output of one node to the input of the next. In the case of an LSTM, for each piece of data in a sequence (say, for a word in a given sentence), there is a corresponding hidden state ht. This hidden state is a function of the pieces of data that an LSTM has seen over time; it contains some weights and, represents both the short term and long term memory components for the data that the LSTM has already seen.

So, for an LSTM that is looking at words in a sentence, the hidden state of the LSTM will change based on each new word it sees. And, we can use the hidden state to predict the next word in a sequence or help identify the type of word in a language model, and lots of other things!

To create and train an LSTM, you have to know how to structure the inputs, and hidden state of an LSTM. In PyTorch an LSTM can be defined as: lstm = nn.LSTM(input_size=input_dim, hidden_size=hidden_dim, num_layers=n_layers).

In PyTorch, an LSTM expects all of its inputs to be 3D tensors, with dimensions defined as follows:

input_dim = the number of inputs (a dimension of 20 could represent 20 inputs)
hidden_dim = the size of the hidden state; this will be the number of outputs that each LSTM cell produces at each time step.
n_layers = the number of hidden LSTM layers to use; this is typically a value between 1 and 3; a value of 1 means that each LSTM cell has one hidden state. This has a default value of 1.
