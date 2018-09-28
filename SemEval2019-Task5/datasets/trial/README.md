# Trial data #

In this repository you will find example files for SemEval 2019 - Task 5, released during the  **Practice** phase. The files are:

* *trial_en.tsv*: it includes English tweets about hate speech against women and immigrants
* *trial_es.tsv*: it includes Spanish tweets about hate speech against women and immigrants

Trial data serve the purpose of showing how the official training data will look like, and allowing participants to try out uploading a submission to CodaLab.

### File format ###
The data have been encoded with the same format, independently of the task and language. Such format consists of a tab-separated file with one line per tweet containing the following fields:  
* a numeric ID that uniquely identifies the tweet within the dataset (*id* column)
* the text of the tweet (*text* column)
* a binary value {1|0} indicating if hate speech is occurring against one of the given targets, women or immigrants (*HS* column)
* if HS occurs (i.e. the value for the feature at point 2 is 1), a binary value indicating if the target is a generic group of people (0) or a specific individual (1) (*TR* column)
* if HS occurs (i.e. the value for the feature at point 2 is 1), a binary value indicating if the tweeter is aggressive (1) or not (0) (*AG* column)






