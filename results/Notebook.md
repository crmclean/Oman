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
