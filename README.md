## Mushroom Classification

People are always looking for a means of incorporating nutrients into their diet. Mushrooms are a reliable
source of vitamins, minerals, and other essential nutrients. They are abundant and grow in most biomes.
The problem is that it is difficult to tell an edible mushroom apart from a poisonous one. In the Province of
Parma, Italy, from January 1, 1996 - December 31, 2016, there were 443 mushroom poisonings. While
most are not fatal, the risk is still there. Using a dataset with 173 unique species with 353 observations
each (61,069 total observations) and 20 features (three metrical and 17 nominal), supervised learning was
used to determine which of those features lent the most importance to identifying an edible mushroom
from a poisonous one.

Four dataset permutations were used. Full dataset, full dataset without outliers, subset dataset using
Shapley features, and subset dataset without outliers. Linear Discriminant Analysis (LDA), Logistic
Regression, Support Vector Machine (SVM), Random Forest, Extreme Gradient Boosting (XGBoost), and
neural network were the machine learning models used. These models were run on each of the 4 dataset
permutations with hyperparameter tuning using a grid search and a repeated stratified k-fold cross
validation (five-fold and 3 repeats). Recall (percentage of poisonous mushrooms correctly classified) was
the performance metric prioritized because misclassifying poisonous mushrooms as edible carries a higher
risk than misclassifying an edible as poisonous. LDA and Logistic Regression performed the worst with a
Recall between 77.5 % - 79.8%. Random Forest, SVM, and Neural Net performed the best at 99.5% - 99.9%
and had ~ 1.0 for the area under the ROC curve (AUC). They can correctly separate the two classes. The
top overall feature importance, using Random Forest, were stem width, stem height, cap diameter, cap
surface and cap shape.
