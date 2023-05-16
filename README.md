<h2>  Introduction  </h2>

This repository contains the data and source code for the EACL 2023 paper: [An Empirical Study of Clinical Note Generation from Doctor-Patient Encounters](https://aclanthology.org/2023.eacl-main.168) 

    - An Empirical Study of Clinical Note Generation from Doctor-Patient Encounters. 
    - Asma Ben Abacha, Wen-wai Yim, Yadan Fan and Thomas Lin. 
    - EACL, May 3-5, 2023, Dubrovnik, Croatia. 
    
        @inproceedings{mts-dialog,
          title     = {An Empirical Study of Clinical Note Generation from Doctor-Patient Encounters},
            author = "Ben Abacha, Asma  and
              Yim, Wen-wai  and
              Fan, Yadan  and
              Lin, Thomas",
            booktitle = "Proceedings of the 17th Conference of the European Chapter of the Association for Computational Linguistics",
            month = may,
            year = "2023",
            address = "Dubrovnik, Croatia",
            publisher = "Association for Computational Linguistics",
            url = "https://aclanthology.org/2023.eacl-main.168",
            pages = "2291--2302"
        }
    

<h2>Datasets, Code & Annotations</h2>

<h3>Main Dataset</h3>
The MTS-Dialog dataset is a new collection of 1.7k short doctor-patient conversations and corresponding summaries (section headers and contents). 
   
   - The training set consists of 1,201 pairs of conversations and associated summaries. 
   
   - The validation set consists of 100 pairs of conversations and their summaries. 
   
   - MTS-Dialog includes 2 test sets; each test set consists of 200 conversations and associated section headers and contents:
        - MTS-Dialog-TestSet-1-MEDIQA-Chat-2023.csv: Official test set used in the [MEDIQA-Chat 2023 challenge](https://sites.google.com/view/mediqa2023/clinicalnlp-mediqa-chat-2023) (Task A)
   
        - MTS-Dialog-TestSet-2-MEDIQA-Sum-2023.csv: Official test set used in the [MEDIQA-Sum 2023 challenge](https://www.imageclef.org/2023/medical/mediqa) (Task A & Task B)

The full list of normalized section headers: 

        1. fam/sochx [FAMILY HISTORY/SOCIAL HISTORY]
        2. genhx [HISTORY of PRESENT ILLNESS]
        3. pastmedicalhx [PAST MEDICAL HISTORY]
        4. cc [CHIEF COMPLAINT]
        5. pastsurgical [PAST SURGICAL HISTORY]
        6. allergy
        7. ros [REVIEW OF SYSTEMS]
        8. medications
        9. assessment
        10. exam
        11. diagnosis
        12. disposition
        13. plan
        14. edcourse [EMERGENCY DEPARTMENT COURSE]
        15. immunizations
        16. imaging
        17. gynhx [GYNECOLOGIC HISTORY]
        18. procedures
        19. other_history
        20. labs

<h3>Augmented dataset</h2>
The augmented dataset consists of 3.6k pairs of medical conversations and associated summaries created from the original 1.2k training pairs via back-translation using two languages French and Spanish, as described in the paper (cf. Section 4.2).  

We provide the [full augmented training set](https://github.com/abachaa/MTS-Dialog/blob/main/Augmented-Data/MTS-Dialog-Augmented-TrainingSet-3-FR-and-ES-3603-Pairs-final.csv) that we used in the experiments, as well as the separate datasets created using the [French](https://github.com/abachaa/MTS-Dialog/blob/main/Augmented-Data/MTS-Dialog-Augmented-TrainingSet-1-En-FR-EN-2402-Pairs.csv) and [Spanish](https://github.com/abachaa/MTS-Dialog/blob/main/Augmented-Data/MTS-Dialog-Augmented-TrainingSet-2-EN-ES-EN-2402-Pairs.csv) translation models. 

<h2>Source Code</h2>
The source code for the summarization of doctor-patient conversations and the automatic generation of clinical notes. 

<h2>Manual Scores for Correlation Study</h2>

- Manual fact-based scores for the evaluation of 400 automatic summaries generated using four summarization models from the validation set of 100 conversations and notes. 

- The Factual P/R/F1 Scores, Hallucination and Omission Rates, and Levenshtein Edit Distance are computed based on the fact-based manual counts and correction. 

- We used the manual scores to evaluate the performance of several evaluation metrics (e.g., ROUGE, BERTScore, and BLEURT) by computing the Pearson's correlation coefficients between the automatic and manual scores, as described in the paper (cf. Section 5.2 and Section 5.3). 

- We provide all the [data](https://github.com/abachaa/MTS-Dialog/tree/main/Correlation-Study) needed to perform this correlation study on other evaluation metrics. 


<h2>Challenges & Evaluation Scripts</h2>

- MEDIQA-Chat 2023: https://github.com/abachaa/MEDIQA-Chat-2023 

- MEDIQA-Sum 2023: https://github.com/ImageCLEF/2023_ImageCLEFmed_Mediqa 


## <h2>Contact</h2>

    -  Asma Ben abacha (abenabacha at microsoft dot com)
     - Wen-wai Yim (yimwenwai at microsoft dot com)

----

Release Date: all data and code will be released by May 19, 2023.

----
