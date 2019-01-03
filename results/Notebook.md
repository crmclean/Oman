# 2019-01-03

The algorithm I need to use for this project is an IDS3 information tree model that makes decisions based on the entropy of each row of features. Conceptually a low entropy is ideal since it has the most predictive power. 

# 2018-12-02

The current state of affairs: I have a meeting w/ ethan from the Alm lab to discuss the use of different ML tools to solve my classification issue. Alternatively, I could also speak w/ Rohan. 

My current idea is to use:
- A decision tree
- All-vs-all random forest
- logistic regression

# 2018-11-27

## New Plan

### Issues w/ Previous Plan
From speaking with Krista, we cannot do the formula assignment strategy. She says that there are far too many combinations with the instrument they used to really make any sense of what they have. 

### Proposed Approach

New plan: create a classifier to identify which features are distinctive to each well. From what I see, there appears to be one well that is far different than the others, so I hypothesize that this should contain distinguishing traits from the other two. 

### To Do

I need to run a random forest on the dataset to see if there are specific features that distinguish one feature from another. To do this I will first:

1) Follow a tutorial on how to do this from the internet
2) Apply it to my data
3) Interpret the results of the analysis to see if there are any distinctive propoerties about the random forest features.
4) I should match features to m/z putative ID matches from the other sheet Lauren gave me. 

# 2018-11-24

## To Do

I need to check out the new formularity paper to see how the scoring and isotope functions work. I got the algorithm to work and show a lot of masses if I use a high ppm filter.  

## Updates

I made a mistake. Not all features had a calculated nominal mass. Looking at individual masses without knowing the actual structure makes it very hard to accurately define the structure. 

A rough idea would be to calculate all possible adducts mass conversions, and then determine the formula for each of those. I could calibrate this with respect to the distribution of adducts for everything that has a determined exact mass. 

Only 76 out of the 1200 or so masses retained has a determined exact mass. 

Also, it might be worth waiting to hear what Rene has to say about this. He is much more familiar with this problem. 

# 2018-11-23

## Progress

### Feature Distributions

I am doing the analysis within bin/2018-11-23/feature_distributions.Rmd

### QA 
I am working within bin/2018-11-23/oman_qa.rmd

Ok - just finished this. The results are within:
results/2018-11-23/qa_results.html 
They originate from the script above. 

The Data was stored within:
data/2018-11-23/A_oman_feature_table.txt

## Overview

The goal of this project is to compare the OM composition of 5 ground water wells analyzed through LC-MS.

## Game Plan

The current plan is to take the data that has already been processed, assign chemical formulas to the features, and classify the formulas into compound classes. 

This requires:
0) generating a QA list of metabolites belonging to the wells
1) finding the chemical formula through Liz's CIA algo
2) putting things into classes based through MSCC algo (see yina's 2018 anal chem paper)
3) Visualize the results in a clear and coherent way, showing the differences between wells. 
4) Look for correlations between these compounds and other variables defining the wells. 
