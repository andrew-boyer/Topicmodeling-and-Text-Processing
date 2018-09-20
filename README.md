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
```
install.packages("topicmodels")
library(topicmodels)
```
Also, please upload the csv file you'd like to analyze to your session of R.

![image](https://user-images.githubusercontent.com/43450019/45838167-14f30580-bcdf-11e8-82fc-af9232a91560.png)

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

All testing was done on the following...

- Type: t2.medium vCPU/RAM 2/4
- Local Disk size: 30GB
- Application: RStudio

The number of topics one wants to process, and the minimum word frequency chosen during the document term matrix processing has a fairly large effect on the processing time.

 

With 3 relevant words and 2 topics chosen by the user the full csv file found on datalake takes **25.32 seconds** to process.

With 3 relevant words and 3 topics the full csv file takes **2 minutes 55 seconds** to process.


