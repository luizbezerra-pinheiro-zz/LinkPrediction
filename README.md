# LinkPrediction

Predict links between pages in a subgraph of the French webgraph (F1-score approx. 89%)

## This Notebook is meant to be used on Google Colab.
It mounts the user's Google Drive.
The locations define by default of the data files are as follows:
My Drive/ML-project/Data/testing.txt
My Drive/ML-project/Data/training.txt
My Drive/ML-project/Data/node_information/text/0.txt
...
My Drive/ML-project/Data/node_information/text/65553.txt

The user must alse create the following directories:
My Drive/ML-project/Data/node_information/clean_text
My Drive/ML-project/Data/node_information/vectorized
My Drive/ML-project/Data/output
My Drive/ML-project/Models

# Instructions to run the Notebook
## Initial Setting
1) Install libraries
2) Run Main Imports
## To train the Node2Vec Model
1) Run in order all cells of 'Node2Vec - Embedding'
You may modify the model_version variable from the first cell based on the arguments of Node2Vec
## To compute Node2Vec Baseline
1) Run all cells off 'Node2Vec - Baseline' 
You may modify the model_version variable from the first to choose which version of the Node2Vec model you are willing to import

## To Train Word2Vec Model
1) Run All Data pre-processing, you may define the name of the cleaned csv (look for variables local_clean_text_path and drive_clean_text_path
2) Run all Word2Vec - Embedding, you may aswell define the name of the cleaned CSV in the first cell: look for the variable drive_clean_text_path
You may aswell define the 'w2v_model_version' based on the arguments of both Word2Vec and Word2Vec.train.

## To compute Word2Vec Baseline
1) Run all 'Word2Vec - Baseline', you may define the 'w2v_model_version'  to load from a previous trained and saved word2vec model

## Doc2Vec - Similar to Word2Vec

## Final predictor
1) Run Node2Vec Baseline and Doc2Vec Baseline (and its dependencies)
2) Run 'Doc2Vec and Node2Vec together'
The final prediction will be saved (by default) at :
My Drive/ML-project/Data/output/node2vec_doc2vec_final_prediction.csv
