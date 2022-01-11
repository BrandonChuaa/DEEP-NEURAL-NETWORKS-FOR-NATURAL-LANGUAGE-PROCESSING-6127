# Assignment 3
Machine learning - Transformers

# a.
- In the original base transformer, the basic hyperparameters are:
  - Number of layers, N = 6
  - Feature dimension for each token, dmodel = 512
  - Number of heads, h = 8
  - Key and value representation size (dk) = (dmodel / h) =  64
  - Hidden representation size of the feed-forward layer, ffn_dim = 1024
- Assume you have only one layer (N = 1) in the transformer. Calculate the total number of parameters in the transformer encoder layer based on the remaining default hyper-parameters mentioned above.
- Now increase the number of layers one by one up to 12 and show how the number of parameters increases compared to the number of layers N.
- For each of the previous calculations, increase the token representation size of dmodel from 512 to 1024 and 2048, and show how the number of parameters increases compared to the number of layers.
- Discuss how the total number of parameters changes with respect to the hyper-parameter values based on your experiments.

# b.
- Do you agree/disagree with the following statement (provide necessary arguments to support your stand): “Multi-head attention works as an ensemble of heads in the transformer architecture.”

# c.
- How is the decoder training and decoder inference different in the transformer architecture, compared to recurrent models like LSTM/GRU?

# d. 
- How does the transformer architecture capture sequence information despite having no sequential probability calculation like RNN?

# e.
- Follow the example code here.(https://github.com/pytorch/examples/tree/master/word_language_model) You will find a TransformerModel class in the model.py file which implements the TransformerEncoder class from the torch.nn library. You can also use the Huggingface library to train a language model.
  - Train the word language model with wikitext (data is given in the repository). Train the model for 10 epochs. Select the best model based on development set perplexity. Report the perplexity of the test set.
  - You may perform hyper-parameter search on the model based on the hyper-parameters (N, dmodel, h, dk, ffn_dim) discussed above in the assignment.
  - What happens when you do not perform scaling in the attention head? Report the effect of scaling on perplexity.
