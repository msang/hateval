Data sets

All data for the competition are collected from Twitter and manually annotated mainly via the Figur8 crowdsourcing platform. They are organized in four datasets especially released for the competition according to the languages and targets involved:

English-hate-women, which includes English tweets about hate speech against women
English-hate-immigrants, which includes English tweets about hate speech against immigrants
Spanish-hate-women, which includes Spanish tweets about hate speech against women
Spanish-hate-immigrants, which includes Spanish tweets about hate speech against immigrants

Format

According to the need of the task and related subtasks, for each tweet each dataset will include:

a numeric ID that uniquely identifies the tweet within the dataset
the text of the tweet in anonymous form
a binary value (1/0) indicating if HS is occurring against one of the given targets (women or immigrants)
if HS occurs (i.e. the value for the feature at point 2 is 1), a binary value indicating if the target is a generic group of people (0) or a specific individual (1)
if HS occurs (i.e. the value for the feature at point 2 is 1), a binary value indicating if the tweeter is aggressive (1) or not (0)
An annotated tweet is a tab-separated line with the following pattern:

ID[tab]Tweet-text[tab]HS[tab]TargetRange[tab]Aggressiveness

where ID is a progressive number denoting the tweet, Tweet-text is the given text of the tweet
while the other parts of the pattern (given in trial and training data and to be predicted in testing data) are: Hate Speech [HS] is hateful (1) or not (0), TargetRange [TR] is group (0) or individual (1), and Aggressiveness [AG] is absent (0) or present (1). An example of annotation is reported in the following:

42648663[tab]USER_NAME Stupid ugly cunt who needs to die[tab]1[tab]1[tab]1
Notice that aggressiveness is not a mandatory characteristics of all hateful texts and some text can express hate against a target in terms of disrespect but without using an aggressive language.

 