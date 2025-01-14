## Overview
Archive NER trained models, datasets used and testing data for my Final Year Project (FYP) with title `AI-Powered Job Application Management for Applicant`

## TODO
Add completed full thesis and poster

## Spacy NER Performance
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