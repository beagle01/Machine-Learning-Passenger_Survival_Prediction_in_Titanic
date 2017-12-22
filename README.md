# Problem: Predict the survival of passengers in Titanic by machine learning

Titanic dataset is a most quoted data set in global data science community. The data has 1309 rows and 14 columns. It has a mix of variables comprising categories, numbers, and text. I'm going to train a machine learning model on this dataset to predict the survival of passengers in Titanic. The "survived" variable is treated as target which has two classes. Nine varialbles, including "pclass", "sex", "age", "sibsp", "parch", "fare", "cabin" ,"embarked", and "boat", are treated as features with an original dimension 1309 x 9. Howver after converting categorical data into numbers with Pandas' get_dummies(), the features' dimension becomes to 1309 x 223. All nulls are replaced with a number of -9.0.

To find a good classification algorithm, I evaluated Logistic Regression, K-Nearest Neighbors, Decision Trees, Extremely Randomized Trees, Random Forests, Gaussian Naive Bayes, Support Vector Machines, Gradient Boosting, and Neural Networks on processed dataset using cross validatoin method. The accuracy of each algorithm modeling with default parameters was computed. The top five algorithms were Neural Network, Logistic Regression, Gradient Boosting, Extremely Randomized Trees, and Decision Trees. Then I focused on Neura Network, Logistic Regression, and Gradient Boosting.

When modeling with Neural Networks algorithm, the best pair of accuracy scores for training set and validation set was 0.979 and 0.970, respectively. They were close. The precision, recall and f1-score of validation were 0.95, 0.95 and 0.95, respectively. The AUC (ROC) is 0.94.

When modeling with Logistic Regression algorithm, the best pair of accuracy scores for training set and validation set was 0.954 and 0.957, respectively. They were very close. The precision, recall and f1-score of validation were 0.96, 0.96 and 0.97, respectively. The AUC (ROC) is 0.99.

When modeling with Gradient Boosting algorithm, the best pair of accuracy scores for training set and validation set was 0.952 and 0.945, respectively. They were also close. The precision, recall and f1-score of validation were 0.95, 0.95 and 0.94, respectively. The AUC (ROC) is 0.96.

These findings demonstrate that a very good predicting model for the survival of passengers in Titanic can be obtained by training Logistic Regression algorithm on the Titanic dataset.

