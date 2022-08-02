# Bayesian Network
Our work consists of creating a Bayesian network, meant for finding the probability of each happiness score, given the value of some of the other variables.

## Analysing the data 
First of all we looked at the correlation between the continuous data contained in the columns of the dataset.
Then we discretized our data for the sake of simplicity, rounding up the values in order to categorize them, while still maintaining them to lie within the original minimum and maximum values.
To assess whether two variables are dependent or independent, we resorted to the chi-squared test. For this test you create a contingency table for each couple of variables.

## Bayesian Network
Given the newfound knowledge about the dependence of the variables after the chi-squared test, we constructed the Bayesian network, which is a type of probabilistic graphical model comprised of nodes and directed edges.
To construct the model we put the variables in an arbitrary order.
Then, to fit the model onto our data we used the Maximum Likelihood Estimation method (MLE), which is a method for estimating the parameters of an assumed probability distribution, given some observed data. Finally, since finding the exact inference is NP-hard to, we rely on the variable elimination algorithm, which is applied on the fitted model, 
in order to avoid further repeated calculations.
When exact inference is unfeasible, approximate inference is used to learn realistic models, 
trading off computation time for accuracy. Although we already obtained good results with the exact inference method, we decided to do a couple of trials with approximate inference using rejection sampling and likelihood-weighting sampling.

