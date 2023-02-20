## Major Library Versions.

1. Catboost - version 1.1.1
2. Sklearn -  version 1.0.2


## Reproducing the Score.

To reproduce the submission, you will have to run the notebook provided. I've tried to explain every line of code and each segment as best as I can.


## Environment details 

The Code was run on Kaggle CPU kennel
Python Programming Language.

## Which data files are being used?

The data used are the official data set as given in the resources folder on BitGrit.

1. The collections dataset
2. The Collections Twitter Statistics
3. The NFTS Train set
4. The NFTS Test set
5. The sample submission format



## How are these files processed?

All methods and techniques used have been thoroughly descibed in the notebook. The files were simply used to build a model with which the predictions were done. I also did some very simple feature engineering and data manipulation which include:

1. Datetime extraction
2. Variable Mapping
3. Target Transformation
4. Creation of statistical features.


## What is the algorithm used and what are its main hyperparameters?

The Catboost Algorithm was used using 16 folds. The major hyperparameters used are.

1. learning_rate: 0.163251453473545997,
2. max_depth: 14,
3. subsample: 0.6530887571489526