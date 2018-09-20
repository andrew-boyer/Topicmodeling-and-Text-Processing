# Hackathon for Topicmodeling Large Files

## Introduction
### Competition Rules
 Input Data: 
 A .csv file with 100-5000 rows and one column of short, 1-5 sentence texts written in English, encoded in UTF8. 
 
 The expected output: 
 One data frame with three columns, in which the n most relevant words are listed for each of the T topics, where n and T are variables specified by the user: 
 1. Topic ID 
 2. Word 
 3. Weight belonging to the word in the topic 

Example output, with n = 3, T = 2: 
 - Topic1   dog     0.9 
 - Topic1   bone    0.5 
 - Topic1   chase   0.3 
 - Topic2   cat     0.82 
 - Topic2   meow    0,4 
 - Topic2   purr    0,2

### Prerequisites

Please ensure that the "topicmodels" package is installed. All other packages should be automatically installed with RStudio and calling them with the library command in the function will be sufficient.

Also, please upload the csv file you'd like to analyze to your session of R.
```
install.packages("topicmodels")
library(topicmodels)
```
### Libraries
Libraries used include:
  topicmodels
  dplyr
  tidytext
  tm
  tidyr
  data.table
  
### Input File

The input data is a large (20MB) csv file. Each line in this file represents a new document, whereas typical csv files are separated by commas, this file must be separated by line. Furthermore, the file is expected to have a header.

## Running the Function

The function name is Contivation. In order to run the function first copy the function into a new script and press the "Source" button.
The function is set up as follows Contivation(# of relevant words, # of topics). Therefore, if you'd like the function to find 2 topics with 3 relevant words each type the following into the console window in your R session

```
Contivation(3, 2)
```


## Results


