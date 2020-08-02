# CAMEO project
During our research of CAMEO, we found another existing framework IDEA. To the best of our knowledge, none of the existing work compares IDEA and CAMEO. Furthermore, professor Phillip A., the author of CAMEO, believed  these two coding frameworks are complementary to each other rather than competitive. Therefore, it is very meaningful to construct an automated method to distinguish which framework is better suited to a given article.

## Dataset
We collected and labeled 600 pieces of data from CAMEO codebook(CAMEO.Manual.1.1b3), 187 from IDEA codebook(July 2002 version), 208 from Quantum Criticism data (provided by sponsors). 
We classified events into 3 categories: 0 - suitable for CAMEO, 1 - suitable for IDEA, 2 - neither. Finally, we had 995 pieces of data in total, including 738 with category 0, 155 with category 1 and 102 with category 2. 

## Data preprocessing 
We loaded the data file (including text and labels) into DataFrame using Pandas.
We tokenized text sentences using spaCy.
We lemmatize the words by using spaCy.
We loaded pretrain weight by using GloVe

## Model and hyperparameter tuning
We have four kinds of model to train our data 
Support vector machine(SVM) and single hidden layer neural network model are built by sklearn, written in Baseline_Models.ipynb.
We served SVM as baseline model.
LSTM and GRU models are built by Pytorch, written in GRU_Model.ipynb and LSTM_Model.ipynb. For GRU and LSTM model, we tuned several hyperparameter including one or two hidden layer, hidden layer dimensions 50, 100, 150, 200, 0.1 or 0.01 learning rate, and also decreasing learning rate from 0.1 to 0.01.

## Result
baseline model SVM, the accuracy is 79%
and the MLP and GRU have 85% accruacy
the best model are LSTM models holding 86% accuracy 
