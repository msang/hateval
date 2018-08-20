# SemEval-2019 Task 5 - evaluation script #


This is the official evaluation script for SemEval-2019 Task 5: Multilingual detection of hate. The script is language-independent and has been conceived in order to evaluate submissions for both task A and task B.

**NOTE** 
During the **Practice** phase, the prediction files submitted by participants to the task page will be evaluated for the task A, and  for demonstration purposes only; if participants wish to test the script on prediction files for task B as well, they could use the version available here (see the instructions at the bottom of this page).

For the **Development** and **Evaluation** phases, the script will provide a complete evaluation for each language and task for any submitted file, provided that the latter meet the submission requirements described below.

## Submission instructions ##

The script takes one single prediction file as input, that MUST be a TSV file structured as follows:

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

When submitting predictions to the task page in Codalab, one single file should be uploaded for each task and language, as a zip-compressed file, and it should be named according to the language and task predictions are submitted for, therefore:

* *en_a.tsv* for predictions for taskA-English
* *es_a.tsv* for predictions for taskA-Spanish
* *en_b.tsv* for predictions for taskB-English
* *es_b.tsv* for predictions for taskB-Spanish


## Submission results ##

The script outputs a file **scorer.txt** containing different scores, depending on the task.
For task A it returns accuracy, precision, recall and F<sub>1</sub>-score just for the HS category.
For task B it returns accuracy, precision, recall and F<sub>1</sub>-score for each category (HS, Target Type, Aggressiveness), along with the macro-averaged F<sub>1</sub>-score and the Exact Match Ratio.

## Testing the script offline ##

In order to run the script locally, the input and output directories must match the Codalab format. The *input* directory must contain two subdirectories, namely **res** (containing the result file in TSV format with the naming convention described above) and **ref** containing the reference dataset (called **en.tsv** for English and **es.tsv** for Spanish). The output will be written in the file **scorer.txt** in the *output* directory.
Example of file structure:

    input/
     |- ref/
         |- en.tsv
     |- res/
         |- en_a.tsv
    output/
     |- scorer.txt
    
