# predictive-analytics

# important-points
#1 there are three important concepts in analytical basetable: the population,the candidate predictors and the target.

#2 the polpulation is group you want to make prediction for

#3 the candidate predictors describes the objects in population

#4 the target has information about the event to predict

#5 you can retrieve the coefficients using the attribute coef_. 

#6 the goal of variable selection is to select a set of variables that hasoptimal performance

#7 A measure to quantify performance of predictive models is AUC value (0,1) roc_auc_score(true_target, prob_target)

#8 Implementation of the forward stepwise procedure
1) function auc that calculates AUC gives a certain set of variables
2)function best_next that returns next best variable in combination with current variables
3)loop until desired number of variables

#9 It can happen that a good variable is not added because it is highly correlated with a variable that is already in the model. You can test this calculating the correlation between these variables:
corrcoef(basetable["variable_1"],basetable["variable_2"])[0,1]

#10 the cumulative gains curve is an evaluation curve that assesses the performance of your model. It shows the percentage of targets reached when considering a certain percentage of your population with the highest probability to be target according to your model.

To construct this curve, you can use the .plot_cumulative_gain() method in the scikitplot module and the matplotlib.pyplot module. As for each model evaluation metric or curve, you need the true target values on the one hand and the predictions on the other hand to construct the cumulative gains curve.
