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
* The month and year was extracted from both the Creation date and Last sale date.
* The difference in days between the Last Sale date and the Creation date was also calculated.

2. Variable Mapping
For the boolean data: Openrarity_enabled, has_website, has_medium, has_own_twitter and has_discord. I did a simple mapping of "1" for "True" and "0" for "False".

3. Target Transformation
I used a logarithmic transformation to handle the skewed nature of the target

4. Creation of statistical features.
I created statistical features for 

* Rarity score.
* Total Supply.
* Number of traits.
* Seller Fees.
* Platform Fees.

To create these features I grouped the data by the NFT_IDs and aggregated the Minimum, Maximum, Mean, Sum, Median and Standard deviation.



## What is the algorithm used and what are its main hyperparameters?

The Catboost Algorithm was used using 16 folds cross validation technique. The major hyperparameters used are.

1. learning_rate: 0.163251453473545997,
2. max_depth: 14,
3. subsample: 0.6530887571489526