# ESCM-summary-evaluation
The Elementary Scenario Component Metric for summarization evaluation

## Datasets and Pre-processing
The Multi-News data can be found in the "Multi-News dataset" directory, which contains the original dataset in "multi-news-original", and 
the pre-processed versions of the dataset truncated at 500 tokens ("multi-news-original-src-cleaned-no-newlinechar-word_tokenizer_500"), and 
at 1000 tokens ("multi-news-original-src-cleaned-no-newlinechar-word_tokenizer_1000"). 


The Homicide dataset is not publically available as of Jan 2021. The preprocessing code for the Homicide dataset is provided in "[1]Pre-processing Homicide dataset.ipynb"

## Models Implementation
The code for the multidocument summarization is adapted from the publicly available code of [Fabbri et al. (2019)](https://github.com/Alex-Fabbri/Multi-News). We have made slight 
adjustments to some of the OpenNMT files in order to fix minor bugs, or adapt the code for our purposes. The code is located in the "Models code" 
directory. It contains a directory for each of the models used, namely Hi-MAP, Transformer, TextRank, and LexRank. Also, there is a YAML file 
with the Anaconda virtual environment packages and their corresponding versions used.

## Custom Evaluation Metric
The code for the Custom Evaluation Metric is part of the "[2]Custom Evaluation Metric.ipynb" notebook. The notebook generates an Excel spreadsheet 
with all the Custom Evaluation Metric scores per case and per model-input data combinations, and also includes the average score for each model, 
and for each case. These results are in "homicide_models_scores.xlsx", located in the "Results\Custom Evaluation Metric" directory. The CEM 
notebook includes additional comments and explanation of the evaluation metric.

## Human Evaluation
The results from the human evaluation survey are processed by "[3]Process Results Human Evaluation.ipynb" and the statistics are saved in the "Survey_Results_Statistics_Final.xlsx" spreadsheet, located in the "Results\Human Evaluation". This file also contains the 
Pearson's correlation coefficient calculation. 

The results from the Inter-Rater Reliability are obtained using an online tool (http://dfreelon.org/utils/recalfront/recal-oir), and the input files
are named "summary_N_IRR", where N is in the range from 1 to 3.
