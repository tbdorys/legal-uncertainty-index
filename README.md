# Legal Uncertainty Index (IIJ)



This repository documents the data collection and processing workflow used to construct the \*\*Legal Uncertainty Index (IIJ)\*\*. The project integrates automated web scraping, text processing, and quantitative analysis to measure regulatory uncertainty based on official draft decree documents published in Colombia.



The current stage of the project focuses on the ingestion and organization of regulatory text data as the primary input for downstream Natural Language Processing (NLP) and index construction tasks.



## Project Objective



The main objective of this project is to develop a reproducible and transparent pipeline for building a Legal Uncertainty Index that captures variations in regulatory activity and institutional uncertainty over time.



Specifically, the project aims to:



\- Collect official regulatory draft documents from public government sources.

\- Organize and store raw textual data in a structured format.

\- Prepare the dataset for text preprocessing, network modeling, and index computation.

\- Support empirical analysis related to legal and economic uncertainty.



## Data Source



The primary data source is the official website of the \*\*Colombian Ministry of Commerce, Industry and Tourism (MinCIT)\*\*.



The current dataset covers regulatory draft documents published during the period:



\- **2018–2025**

These documents correspond to regulatory proposals released for public consultation.



## Project Structure



legal-uncertainty-index/

│

├── data\_raw/

│   └── web\_scraping/

│

├── data\_processed/

│   ├── pdf\_ocr/

│   │

│   ├── txt\_normative\_rag/

│   │

│   ├── corpus\_clean/

│   │   ├── basic\_clean/

│   │   ├── normalized/

│   │   ├── nlp\_clean/

│   │   ├── tokens/

│   │   ├── tokens\_no\_stopwords/

│   │   └── tokens\_lemmas/

│   │

│   ├── vectorization/

│   │   ├── dtm\_bow.csv

│   │   ├── dtm\_tfidf.csv

│   │   ├── vocabulary.csv

│   │   └── top\_tfidf\_terms.csv

│   │

│   ├── cooccurrence/

│   │   ├── cooccurrence\_edges.csv

│   │   └── cooccurrence\_matrix.csv

│   │

│   └── manifests/

│       ├── manifest\_pdf\_ocr.csv

│       ├── manifest\_txt\_normative\_rag.csv

│       ├── manifest\_basic\_clean.csv

│       ├── manifest\_normalized.csv

│       ├── manifest\_nlp\_clean.csv

│       ├── manifest\_tokens.csv

│       ├── manifest\_stopwords.csv

│       ├── manifest\_lemmas.csv

│       ├── manifest\_vectorization.csv

│       └── manifest\_cooccurrence.csv

│

├── notebooks/

│   ├── 01\_mincit\_scraping.ipynb

│   ├── 02\_preprocess\_ocr.ipynb

│   ├── 03\_normative\_extraction\_llm.ipynb

│   ├── 04\_normative\_corpus\_structuring.ipynb

│   ├── 05\_nlp\_preprocessing.ipynb

│   ├── 06\_nlp\_vectorization.ipynb

│   └── 07\_nlp\_cooccurrence.ipynb

│

├── src\_python/

│   ├── \_\_init\_\_.py

│   └── correction\_dictionary.py

│

└── .gitignore

## Workflow

