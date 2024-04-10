# COMP30027-Project-ML

Author: He Shen (1297447)

## Preperations

1. Make sure you have installed Anaconda3 on your environment
2. Unzip all files and place them under the same directory
3. Open `COMP30027_2024_asst1_template.ipynb` with Jupyter Notebook

## How to run

0. If you want to use alternative datasets, simply substitutes your train and test csv into `train_dataset = pd.read_csv('winequality-train.csv')` and `test_dataset = pd.read_csv('winequality-test.csv')`
1. Run the cells one by one in sequence, or tap "Run All" button on top
2. Call `predict` function with parameters `test_features`, `train_features`, `train_labels` and `k`

## Sample usage

In Jupyter Notebook, create a new code block at the bottom of **1. K-NN classifier**:

```
prediction = predict(test_features, train_features, train_labels, k = 1)
prediction
```

Run the block, it would output something like this:
```
0       0
1       0
2       1
3       1
4       1
       ..
1345    1
1346    0
1347    1
1348    0
1349    1
Length: 1350, dtype: int64
```

If you want to compare with the actual labels:
```
(prediction == test_labels).mean()
```

It would give an numerical value on accuracy:
```
0.7644444444444445
```
