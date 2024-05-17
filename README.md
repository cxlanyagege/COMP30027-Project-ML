# COMP30027-Project-ML

Author: He Shen (1297447), Lanruo Su (1297549)

## Preperations

1. Make sure you have installed the latest Anaconda3 on your environment
2. Unzip all files and place them under the same directory
3. Open `code.ipynb` with Jupyter Notebook or VSCode

## How to run

**Option 0:** If you want to use alternative dataset, simply replace them under `project_data` folder. Be aware they should be written in the exact same format as the original ones, as well as the additional preprocessing features in `feature_doc2vec` and `feature_fasttext`

**Option 1:** Tap "Run All" button on top, it will run all the sections, the test dataset predictions will be generated in the same folder as `xxx_predictions.csv` (where `xxx` is the model name)

**Option 2:** If you don't want to run some sections, you can skip running the section "0.2 Data inspection" and "3. Evaluation". Every other cells should be running one by one in sequence in order to generate predictions

## Sample usage

After running completes, you can inspect the training dataset, such as their unique feature counts: 

```
id                           3004
director_name                1460
num_critic_for_reviews        497
duration                      144
director_facebook_likes       373
actor_3_facebook_likes        845
actor_2_name                 1903
actor_1_facebook_likes        668
...
```

Each models prediction scores will be displayed under their section, where the first value represents mean score, the second represents standard deviation: 

```
(0.7253727121464226, 0.015678292456444153)
```

You can also glance the whole result for all 5 models at glance in "2.6 Result review":

```
                   Model  Mean accuracy  Std deviation
0          Decision tree       0.616184       0.013358
1          Random forest       0.722706       0.010892
2    Logistic regression       0.705725       0.010230
3       Stack Classifier       0.705725       0.010230
4  Multilayer perceptron       0.707724       0.004955
```

You may also find 5 test dataset prediction csv files in the same folder, each responding to their models: 

```
dt_predictions.csv       - Decision Tree
rf_predictions.csv       - Random Forest
lr_predictions.csv       - Logistic Regression
mlp_predictions.csv      - Multilayer Perceptron
stack_predictions.csv    - Stack Classifier
```

These prediction files would output something like this:
```
id,imdb_score_binned
1,3
2,3
3,1
4,2
5,2
...
```
