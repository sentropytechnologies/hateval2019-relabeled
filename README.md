# hateval2019-relabeled
A relabeled version of the HatEval (SemEval 2019) dataset used in [Practical Transformer-based Multilingual Text Classification (Wang and Banko, 2021)](./Practical_Transformer_based_Multilingual_Text_Classification.pdf, to appear in proceedings of NAACL 2021 (Industry Track).

## Original Dataset
This dataset was originally released as for the [HatEval shared task](https://competitions.codalab.org/competitions/19935) [(Basile et al., 2019)](https://www.aclweb.org/anthology/S19-2007.pdf), part of SemEval 2019. The dataset consists of tweets in English (10k train/dev, 3k test) and Spanish (5k train/dev, 1.6k test) with binary labels for the following attributes:
- HS: 1 if hate speech is present, 0 if not
- TR: 1 if the target is a specific individual, 0 if it is a general group
- AG: 1 if the tweeter is aggressive, 0 if not

We omit the tweet text in this version of the dataset in compliance with terms and conditions of the original authors. The full dataset can be obtained [here](http://hatespeech.di.unito.it/hateval.html).

## Train and Test Inconsistency
English example labels are inconsistent across the original training and test sets. For example, many test examples containing anti-immigration hashtags were mislabeled as _HS=0_ while similar examples were labeled as _HS=1_ in the training set (see below). We manually relabeled 641 examples in the test set and release the relabeled data in this repository. 

| Hashtag   | Train | Test | Test (relabeled) |
|--------------------|----------------|---------------|----------------------|
| \#NoDACA           | 99.36          | 34.26         | 99.60                |
| \#EndDACA          | 98.31          | 33.87         | 98.39                |
| \#BuildThatWall    | 100.0          | 24.89         | 95.99                |
| \#BuildTheDamnWall | 100.0          | 62.07         | 100.0                |
| \#NoAmnesty        | 100.0          | 48.25         | 100.0                |
| \#SendThemBack     | 82.02          | 68.29         | 87.80                |
| \#DeportThemAll    | 100.0          | 83.15         | 99.46                |


## Schema
The schema of the dataset in this repository is as follows:
| id   | HS | TR | AG | HS_original |
|------|----|----|----|-------------|
| 0000 | 1  | 0  | 1  | 0           |
| 0001 | 0  | 0  | 0  | 0           |
| ...  | ...| ...|... | ...         |

## Citing this dataset
If you use this dataset as part of your work, please cite our NAACL 2021 paper:
```
Bibtex coming soon!
```
