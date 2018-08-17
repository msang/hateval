# SemEval-2019 Task 5 - evaluation script #


This is the official evaluation script for SemEval-2019 Task 5: Multilingual detection of hate. The script is language-independent and has been conceived in order to evaluate submissions for both task A and task B.

**NOTE** 
During the 'Practice' phase, the prediction files submitted by participants to the task page will be evaluated for the task A, and  for demonstration purposes only; if participants wish to test the script on prediction files for task B as well, they could use the version available here.

For the 'Development' and 'Evaluation' phases, the script will provide a complete evaluation for each language and task for any submitted file, provided that the latter meet the submission requirements described below.

## Submission instructions ##

The script takes one single prediction file as input, that MUST be a .tsv file structured as follows:

### Task A ###
id[tab]{0|1}

e.g.

101[tab]1
102[tab]0
103[tab]1

### Task B ###
id[tab]{0|1}[tab]{0|1}[tab]{0|1}

e.g.

101[tab]1[tab]1[tab]1
102[tab]0[tab]0[tab]0
103[tab]1[tab]1[tab]0
104[tab]1[tab]0[tab]0
105[tab]1[tab]0[tab]1

### File names ###

When submitting predictions to the task page in Codalab, one single file should be uploaded for each task, as a zip-compressed file, and it should be named according to the language and task predictions are submitted for, hence:

* en_a.tsv for predictions for taskA-English
* es_a.tsv for predictions for taskA-Spanish
* en_b.tsv for predictions for taskB-English
* es_b.tsv for predictions for taskB-Spanish


## Submission results ##

The script outputs a file 'scores.txt' containing different scores, depending on the task.
..... the accuracy, precision, recall and <b>F<sub>1</sub>-score</b> corresponding to the submission.


