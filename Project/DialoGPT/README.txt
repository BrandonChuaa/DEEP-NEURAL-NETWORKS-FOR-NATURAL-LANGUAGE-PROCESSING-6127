For the DIALO MODEL: 

1) Download the SMS corpus from https://www.kaggle.com/rtatman/the-national-university-of-singapore-sms-corpus,
create a folder called "data" and unzip the sms corpus into it.

2) Run dialo_data_prep.ipynb first to generate CSV file from the raw SMS corpus.

3) Run dialo_model_training.ipynb to train the model using the generated CSV files. Hyperparameters can be changed in the class [Args()], one thing to note
is that to change the type of optimizer used, you will need to change in the class [train] instead. 

4) For 5 epochs, the training may take 3 to 4 hours.