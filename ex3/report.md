# Report

## Information

- Operating System: Ubuntu 20.04
- IDE: Pycharm with Jupyter Notebook
- Software: Python 3.8
- Scikit-learn Version: 1.1.1

## Kaggle

The jupyter notebooks were developed locally with the setup described above.
Afterwards the notebook was imported into kaggle. I enabled the flag `isKaggle`
to load the data from the kaggle paths. Then I ran the notebook on kaggle. 

## Stroke

- Kaggle Notebook: https://www.kaggle.com/code/florianm97/se21m006-stroke-notebook

The stroke dataset contains information, whether a person suffered a stroke or not.
Important informations are the sex, age, other diseases. There is also information
is the person smokes or not. The split between the two genders is roughly the same.

### Preparation

The problem with the dataset was, that it contains some non-numeric values. These
values need to be preprocessed before, otherwise the classification won't work. 
To achieve this I mapped the columns to numeric columns. 

The goal was to predict, if a person will suffer a stroke or not. Therefore, the 
stroke column served as my target feature. The other columns, except the ID column
were used for the classification.

### Kaggle Submission Description

Below is the description of my best submission to kaggle.

```
- Operating System: Ubuntu 20.04
- IDE: Pycharm
- Python Version: Python 3.8
- Random State: 11776836

The learning data was split into a 1/3 test-set and 2/3 training-set. I trained 4 different algorithms.
I used my matriculation number as random state.

- k-NN (2 neighbours)
- k-NN (4 neighbours)
- k-NN (6 neighbours)
- Decision Tree (None max features)
- Decision Tree (sqrt max features)
- Decision Tree (log2 max features)
- SVM (SVC)
- Random Forests (10 trees, `sqrt` max features)
- Random Forests (10 trees, `log2` max features)
- Random Forests (50 trees, `sqrt` max features)
- Random Forests (50 trees, `log2` max features)
- Random Forests (100 trees, `sqrt` max features)
- Random Forests (100 trees, `log` max features)

k-NN (6 neighbours) achieved the best results. An accuracy score of k-NN (6 neighbours) 0.958531 and a f1-score of 0.938235 was achieved.

- Algorithm: kNN

I retrained k-NN (6 neighbours) and used it on the test-set.
```

The submission shows that I trained four different algorithms, with varying parameters.
All the scores from the algorithms can be seen inside the kaggle notebook.

### Results

- Local
  - Locally k-NN with 6 neighbours achieved the best score, as described above
- Kaggle
  - I executed the notebook online on kaggle and received the same results as local
  - But the submitted result only got a score of 0.06153, which is very low and disappointing for me.

## Breast Cancer

- Kaggle Notebook: https://www.kaggle.com/code/florianm97/se21m006-breast-cancer

The dataset contains information, whether a person had breast cancer or not. There
is also some very detailed medical information about the person. The dataset even contains
mean values, standard errors.

### Preparation

The dataset has only numeric value, so no mapping to numeric values is needed.
The goal was to predict, if a person will get breast cancer or not in the future.

### Kaggle Submission Description

```
- Operating System: Ubuntu 20.04
- Python Version: Python 3.8
- Random State: 11776836

The learning data was split into a 1/3 test-set and 2/3 training-set. I trained 4 different algorithms.
I used my matriculation number as random state.

- k-NN (2 neighbours)
- k-NN (4 neighbours)
- k-NN (6 neighbours)
- Decision Tree (None max features)
- Decision Tree (sqrt max features)
- Decision Tree (log2 max features)
- SVM (SVC)
- Random Forests (10 trees, `sqrt` max features)
- Random Forests (10 trees, `log2` max features)
- Random Forests (50 trees, `sqrt` max features)
- Random Forests (50 trees, `log2` max features)
- Random Forests (100 trees, `sqrt` max features)
- Random Forests (100 trees, `log` max features)

SVM achieved the best results for me. SVM was used with the default settings and SVC.

- Algorithm: SVM

I achieved an f1-score of 1.0 with the learning data-set, which is perfect. Then i retrained SVM and used it
on the test-set.
```

The submission shows that I trained four different algorithms, with varying parameters.
All the scores from the algorithms can be seen inside the kaggle notebook.

### Results

- Local
  - Locally SVM achieved the best score, as described above.
- Kaggle
  - I executed the notebook online on kaggle and received the same results as local
  - The submitted result got a score of 0.96, which is very similar to my solutions.
