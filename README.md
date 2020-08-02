# CAMEO project
During our research of CAMEO, we found another existing framework IDEA. To the best of our knowledge, none of the existing work compares IDEA and CAMEO. Furthermore, professor Phillip A., the author of CAMEO, believed  these two coding frameworks are complementary to each other rather than competitive. Therefore, it is very meaningful to construct an automated method to distinguish which framework is better suited to a given article.

## Dataset
We collected and labeled 600 pieces of data from CAMEO codebook(CAMEO.Manual.1.1b3), 187 from IDEA codebook(July 2002 version), 208 from Quantum Criticism data (provided by sponsors). 
We classified events into 3 categories: 0 - suitable for CAMEO, 1 - suitable for IDEA, 2 - neither. Finally, we had 995 pieces of data in total, including 738 with category 0, 155 with category 1 and 102 with category 2. 

## Data preprocessing 
### Loading data
We loaded the data file (including text and labels) into DataFrame using Pandas.

### Tokenization
We tokenized text sentences using spaCy.

### Lemmatization
We lemmatize the words by using spaCy.

### Pretrain weight
We loaded pretrain weight by using GloVe

## Model
We have four kinds of model to train our data 
Support vector machine(SVM) and single hidden layer neural network model are built by sklearn, written in Baseline_Models.ipynb.
We served SVM as baseline model.
LSTM and GRU models are built by Pytorch, written in GRU_Model.ipynb and LSTM_Model.ipynb.
