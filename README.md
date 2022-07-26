[Code](https://github.com/lee-jin81/metis_project_5_nlp/tree/main/Code_nlp) <br>
[Slides](https://github.com/lee-jin81/metis_project_5_nlp/blob/main/slides_nlp_medical_records.pdf) <br>
[Writeup](https://github.com/lee-jin81/metis_project_5_nlp/blob/main/writeup_nlp.pdf) <br>
[MVP](https://github.com/lee-jin81/metis_project_5_nlp/blob/main/nlp_mvp.md) <br>
[Proposal](https://github.com/lee-jin81/metis_project_5_nlp/blob/main/proposal_nlp_medical.pdf) <br>

# Using natural language processing to interpret medical records

## Abstract
Healthcare records are unstructured textual data holding valuable information about patients and diseases. Since the data is unstructured, we can’t do analytics directly on them in order to extract meaningful information for future research. Natural language processing (NLP) can be used to extract valuable information from medical records of patients. The documents were preprocessed by removing words that are not meaningful and then tokenized into words. A document-term matrix was built using a vectorizer that will assign a value to the frequency of words. Features were reduced to 10 topics using topic modeling. Finally, a recommendation system was built that will find similar medical records based on a current document.

## Introduction
Healthcare records are unstructured textual data where the medical professional takes notes at the time of the patient’s visit to record information such as biostatistics, overall health, and any new concerns. This information can be helpful in the diagnosis and treatment of future patients.  However, since the data is unstructured, we can’t do analytics directly on them in order to extract meaningful information for future research. 

I’m proposing to use NLP to extract valuable information from medical records of patients. This can be used to build a recommendation engine that will find previously diagnosed patients who have conditions similar to current patients who need medical attention and advice.  Medical professionals can use this information in addition to their diagnosis to further improve patient care. 

## Data
* Source: [Kaggle Medical transcriptions](https://www.kaggle.com/datasets/tboyle10/medicaltranscriptions)
* Data set: 4,998 documents across 38 different medical specialties

## Tools
* Text processing: Python, text processing libraries (NLTK, scikit-learn), pandas
* Visualizations: matplotlib, wordCloud

