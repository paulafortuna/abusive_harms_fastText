# abusive_harms_fastText

In this repository we have the scripts that support the fastText experiment of our paper:


The complete experiment pipeline can be found here.

We ran the model in its version 0.9.2 with 300 dimension-FastText pretrained vectors, Skipgram Hierarchical softmax loss function, learning rate of 1.0, considering 1 as minimal number of word occurrences, bi-grams, and 25 epochs.


The code is organized as follows:

01_save_data_for_fasttext.py - FastText models require data to be in a specific shape. In this script we prepare the data by calling functions from another script (classifier_utils.py, this one was readapted from the same name BERT script provided here).

02_create_model.sh - We run fastText on the command line, and for making our process more automatic we used bash scripting.


03_compute_model_performances.py - It is a script for computing Precision, Recall and F1 scores for every model.

04_compute_F1_table.py - It is a script for summarizing the F1 scores in one csv that will then be used in our paper results.
