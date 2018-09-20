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
 Topic1   dog     0.9 
 Topic1   bone    0.5 
 Topic1   chase   0.3 
 Topic2   cat     0.82 
 Topic2   meow    0,4 
 Topic2   purr    0,2

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

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system


## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone whose code was used
* Inspiration
* etc
