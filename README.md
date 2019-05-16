# election-predictions

## Index 
1. [Summary](https://github.com/ianjeffries/election-predictions#summary)
2. [File Directory](https://github.com/ianjeffries/election-predictions#file-directory)

## Summary 
The following project accomplishes two goals:  

  1. Predicting the 2016 US election results by county with supervised machine learning in R.
  2. Mining interesting association rules that relate to demographics and voting preference in R. 
  
Three supervised machine learning models are used to predict election results based on demographics: K-Nearest Neighbor, Decision Trees, and Artificial Neural Networks. The models are compared based on accuracy and precision. 

## File Directory

1. [**Data**](https://github.com/ianjeffries/election-predictions/tree/master/Data) - contains three data sets used in analysis (taken from kaggle, referenced in the credits):  
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;a. county_facts.csv - Demographic breakdown of each county  
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;b. county_facts_dictionary.csv - Dictionary to decode variable names in county_facts.csv  
     &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;c. pres16results.csv - Results of the 2016 election by county
  
2. [**classification.Rmd**](https://github.com/ianjeffries/election-predictions/blob/master/classification.Rmd) - R Markdown detailing the entire classification process, from data cleaning to model creation. 


  
  
  
