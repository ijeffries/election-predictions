# election-predictions

<p align="center">
<img src="https://github.com/ianjeffries/election-predictions/blob/master/images/voting_trends.png" alt="alt text" width="640" height="320">
</p>

## Index 
1. [Summary](https://github.com/ianjeffries/election-predictions#summary)
2. [File Directory](https://github.com/ianjeffries/election-predictions#file-directory)
3. [Language and Packages Used](https://github.com/ianjeffries/election-predictions#language-and-packages-used)
4. [Credits](https://github.com/ianjeffries/election-predictions#credits)
5. [License](https://github.com/ianjeffries/election-predictions#license)

## Summary 
The following project accomplishes two goals:  

  1. Predicting the 2016 US election results by county with supervised machine learning in R.
  2. Mining interesting association rules that relate to demographics and voting preference in R. 
  
Three supervised machine learning models are used to predict election results based on demographics: K-Nearest Neighbor, Decision Trees, and Artificial Neural Networks. The models are compared based on accuracy and precision. 

## File Directory

1. [**data**](https://github.com/ianjeffries/election-predictions/tree/master/data) - contains three data sets used in analysis (taken from kaggle, referenced in the credits):  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;a. [county_facts.csv](https://github.com/ianjeffries/election-predictions/blob/master/data/county_facts.csv) - Demographic breakdown of each county.  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;b. [county_facts_dictionary.csv](https://github.com/ianjeffries/election-predictions/blob/master/data/county_facts_dictionary.csv) - Dictionary to decode variable names in county_facts.csv.  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;c. [pres16results.csv](https://github.com/ianjeffries/election-predictions/blob/master/data/pres16results.csv) - Results of the 2016 election by county.
     
2. [**images**](https://github.com/ianjeffries/election-predictions/tree/master/images) - contains vizualizations:  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;a. [decision_tree.png](https://github.com/ianjeffries/election-predictions/blob/master/images/decision_tree.png) - Decision tree created from modelling process.  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;b. <font color="black">[model_comparison.png](https://github.com/ianjeffries/election-predictions/blob/master/images/model_comparison.png)</font> - Comparison of 3 classification models used.  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;c. [population_trends.png](https://github.com/ianjeffries/election-predictions/blob/master/images/population_trends.png) - Population size by voting preference.  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;d. [voting_trends.png](https://github.com/ianjeffries/election-predictions/blob/master/images/voting_trends.png) - Voting trends by top 5 normalized demographics.  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;e. [binning_comparison.png](https://github.com/ianjeffries/election-predictions/blob/master/images/binning_comparison.png) - Comparison of arules binning method.  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;f. [democrat_arules.png](https://github.com/ianjeffries/election-predictions/blob/master/images/democrat_arules.png) - Scatterplot of democratic association rules by support and confidence.  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;g. [republican_arules.png](https://github.com/ianjeffries/election-predictions/blob/master/images/republican_arules.png) - Scatterplot of republican association rules by support and confidence.  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;h. [democrats_grid.png](https://github.com/ianjeffries/election-predictions/blob/master/images/democrat_grid.png) - Color grid of democratic association rules.  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;i. [republican_grid.png](https://github.com/ianjeffries/election-predictions/blob/master/images/republican_grid.png) - Color grid of republican association rules. 
  
3. [**classification**](https://github.com/ianjeffries/election-predictions/tree/master/classification) - contains classification files that predict election outcome based off demographics:  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;a. [classification.Rmd](https://github.com/ianjeffries/election-predictions/blob/master/classification/classification.Rmd) - R Markdown detailing the classification process, from data cleaning to model creation.  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;b. [classification.pdf](https://github.com/ianjeffries/election-predictions/blob/master/classification/classification.pdf) - PDF that shows R code and the outputted results, for easy viewing.
  
4. [**association_rules**](https://github.com/ianjeffries/election-predictions/tree/master/association_rules) - contains association rules files:  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;a. [association_rules.Rmd](https://github.com/ianjeffries/election-predictions/blob/master/association_rules/association_rules.Rmd) - R Markdown to mine rules that relate to demographics and voting preference.  
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;b. [association_rules.pdf](https://github.com/ianjeffries/election-predictions/blob/master/association_rules/association_rules.pdf) - PDF that shows R code and the outputted results, for easy viewing.

## Language and Packages Used

R is used for all model building - in the results R and SAS are compared.  

The following packages are used:
  
  ```
#list of packages used
packages <- c("dplyr", "tidyr", "ggplot2", "class", "rpart", "rpart.plot", "neuralnet", "arules",
              "plyr", "mltools", "arulesViz", "plotly", "RCurl")

#check to see if package is already installed, if not, install
for(p in packages){
  if(!require(p, character.only = TRUE)) {
    install.packages(p)
    library(p, character.only = TRUE)
  } 
}
```

## Credits

1. Would like to thank Ben Hammer for the county_facts.csv and county_facts_dictionary.csv datasets, which were taken off [Kaggle](https://www.kaggle.com/benhamner/2016-us-election/home).
2. Would like to thank Steve Palley for the pres16results.csv dataset, which was taken off [Kaggle](https://www.kaggle.com/stevepalley/2016uspresidentialvotebycounty/home).

## License 

MIT License
Copyright (c) 2019 Ian Jeffries
  
