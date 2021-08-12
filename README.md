![Python 3.6](https://img.shields.io/badge/python-3.6-green.svg)

# LC-ACSA
The code repository for NLPCC2021 paper "Locate and Combine: A Two-Stage Framework for Aspect-Category Sentiment Analysis".

## Data preparation
Download the [glove.840B.300d.txt](http://nlp.stanford.edu/data/wordvecs/glove.840B.300d.zip),[bert-base-uncased](https://huggingface.co/bert-base-uncased),[restaurant post-training BERT](https://github.com/howardhsu/BERT-for-RRC-ABSA/blob/master/pytorch-pretrained-bert.md) to the corresponding paths in your computer.Remenber to modify the dataset path according to your setting.

## Set up the environment
pip install -r requirement.txt

## Running the code
Run the following commands for restaurant 2014 dataset. For the restaurant 2014 hard, restaurant large and restaurant large hard datasets, change rest14DevSplit in the following commands to rest14_hard, rest_large and rest_large_hard respectively.

### Train (for LC-LSTM)
1. sh train_ATE.sh
2. sh train_ACD.sh rest14DevSplit
3. sh scripts_ACSC/CDT_categoryEmbedding_gcnCat_extractTerm.sh cuda:0 train rest14DevSplit 40 

### Test (for LC-LSTM)
1. sh scripts_ACSC/CDT_categoryEmbedding_gcnCat_extractTerm.sh cuda:0 test rest14DevSplit


## Trained models
Trained models can be found [here](). For Chinese, trained models can also be found [here] and the key is ().
