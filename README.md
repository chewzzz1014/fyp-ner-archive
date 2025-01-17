# Overview
Stored the resume dataset annotation and NER trained models for my Bachelor Degree's Final Year Project with title **AI-Powered Job Application Management for Applicant**. There are 3 main parts in the project
1. Named Entity Recognition (NER)
   - Involved in complete machine-learning lifecycle: dataset annotation, model training, model evaluation
   - Trained 2 NER models using spaCy and Flair library, with manually-annotated resume dataset which can recognise 11 types of entities in resume and job description.
2. Job-Resume Matching Scoring
   - Calculate the matching score between a resume contents and job description in range of 0 (not relevant) to 1 inclusively (very relevant).
   - Perform cosine similarity calculation between resume skills and job description skills which are extracted using NER trained models.
3. ResuMatch, Job Application Management System
   - Develop job application management system consists of Job Management, Resume Management, Job-Resume Matching and Dashboard.

## Related Repositories
1. [NER model development and backend code](https://github.com/chewzzz1014/fyp)
2. [Frontend code](https://github.com/chewzzz1014/fyp-frontend)

## NER Entities
| Category            | Entity                      | Label Name  | Example                     |
|---------------------|-----------------------------|-------------|-----------------------------|
| **Personal Information** | Name                        | NAME        | John Doe                    |
|                     | Location                    | LOC         | California                  |
|                     | Phone Number                | PHONE       | 0192394945995               |
|                     | Email Address               | EMAIL       | johndoe@test.com            |
| **Education**       | University or School Name   | UNI         | University of California    |
|                     | Academic Qualification Name | DEG         | Bachelor of Computer Science|
|                     | Study Period                | STUDY PER   | Oct 2021-Jul 2024           |
| **Working Experience** | Job Title                   | JOB         | Java Developer              |
|                     | Company or Organisation Name| COMPANY     | Abc Company                 |
|                     | Working Period              | WORK PER    | Aug 2024-Current            |
| **Skill**           | Skill                       | SKILL       | Java                        |

## TODO
Add completed full thesis and poster

## Spacy NER Performance
Trained Model: https://drive.google.com/drive/folders/1c8PlRGcUW96eEthZizOoK1jhYA3GjhFV?usp=sharing
```
================================== Results ==================================

TOK     100.00
NER P   83.77 
NER R   85.67 
NER F   84.71 
SPEED   13556 

=============================== NER (per type) ===============================

                P       R       F
NAME        91.63   92.02   91.82
EMAIL       95.00   97.44   96.20
PHONE       93.67   96.73   95.17
SKILL       84.33   87.85   86.06
UNI         63.71   70.72   67.03
DEG         78.67   77.59   78.12
COMPANY     74.88   68.60   71.60
JOB         73.65   55.81   63.50
WORK PER    92.92   93.83   93.37
LOC         81.17   80.98   81.07
STUDY PER   84.96   81.70   83.30
```
## Flair NER Performance
Trained Model: https://drive.google.com/drive/folders/1CvpFy6hUTDJF6KK7XdrsYkMiKqnr2q2W?usp=sharing
```

Results:
- F-score (micro) 0.7992
- F-score (macro) 0.8069
- Accuracy 0.6678

By class:
              precision    recall  f1-score   support

       SKILL     0.7980    0.8160    0.8069     20125
         JOB     0.6424    0.6241    0.6331      1160
         LOC     0.7402    0.8491    0.7909       782
        WORK     0.8745    0.9293    0.9011       735
     COMPANY     0.6924    0.6924    0.6924       699
         UNI     0.7109    0.6827    0.6965       353
         DEG     0.8162    0.7957    0.8058       279
       STUDY     0.7729    0.8271    0.7991       214
        NAME     0.8791    0.8915    0.8852       212
       PHONE     0.9406    0.9596    0.9500       198
       EMAIL     0.9096    0.9194    0.9144       186

   micro avg     0.7900    0.8085    0.7992     24943
   macro avg     0.7979    0.8170    0.8069     24943
weighted avg     0.7897    0.8085    0.7988     24943

Loss: 0.18681490421295166'
```
