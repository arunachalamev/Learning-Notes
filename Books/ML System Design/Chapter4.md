---
markmap:
  colorFreezeLevel: 6
  maxWidth: 200
---

# YTVS
## Clarifying Requirements
## Framing as ML
  - Defining the Ml objective
  - Specifying input and output
  - ML category
    - Visual search 
      - Representation learning
      - Video encoder
      - Text encoder
    - Text search
      - inverted index
    - Fusing layer
## Data Preparation
  - Data engineering
    - Annotated dataset
  - Feature engineering 
    - Preparing text data
      - Text normalization
        - Lowercasting
        - Punctuation removal
        - Trim whitespaces
        - NFKD
        - Strip accents
        - Lemmatization
        - Stemming
      - Tokenization
        - Word
        - Subword
        - character
      - Token to IDs
        - Lookup table
        - Hashing
    - Preparing video data
      - Decoding
      - Sampling
      - Resizing
      - Scaling
      - Z-score normalization
      - Correcting color mode
## Model Development
  - Text encoder
    - Statistical 
      - BoW
      - TF-IDF
    - ML- based
      - Embedding layer
      - Word2vec
      - Transformer-based
  - Video encoder
    - Video-level models
    - Frame-level models
## Evaluation
  - Offline metrics
    - Recall@k
    - MRR
  - Online metrics
    - CTR
    - Video completion rate
    - Total watch time of search results
## Serving 
  - Prediction pipeline
    - Visual search
    - Text search
    - Fusing layer
    - RE-ranking service
  - Video indexing pipeline
  - Text indexing pipeline
## Other talking points


   



     

    
  
    
 