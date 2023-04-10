This project uses supervised learning to find key mushroom features that enable distinguishing between edible and poisonous mushrooms.


## Data sets and algorithms used

Four dataset permutations were used. Full dataset, full dataset without outliers, subset dataset using
Shapley features, and subset dataset without outliers. Linear Discriminant Analysis (LDA), Logistic
Regression, Support Vector Machine (SVM), Random Forest, Extreme Gradient Boosting (XGBoost), and
neural network were the machine learning models used. These models were run on each of the 4 dataset
permutations with hyperparameter tuning using a grid search and a repeated stratified k-fold cross
validation (five-fold and 3 repeats). 

## Performance metric and results

Recall (percentage of poisonous mushrooms correctly classified) was
the performance metric prioritized because misclassifying poisonous mushrooms as edible carries a higher
risk than misclassifying an edible as poisonous. LDA and Logistic Regression performed the worst with a
Recall between 77.5 % - 79.8%. Random Forest, SVM, and Neural Net performed the best at 99.5% - 99.9%
and had ~ 1.0 for the area under the ROC curve (AUC). They can correctly separate the two classes. The
top overall feature importance, using Random Forest, were stem width, stem height, cap diameter, cap
surface and cap shape.
