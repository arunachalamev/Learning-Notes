---
markmap:
  colorFreezeLevel: 6
  maxWidth: 200
---

# PNF
## Clarifying Requirements
## Framing as ML
  - Defining the Ml objective
    - Maximize # of implicit reactions
    - Maximize # of Explicit reactions
    - Maximize a weighted combinations of reactions
  - Specifying input and output
  - ML category
    - Pointwise LTR
## Data Preparation
  - Data engineering
    - Users
    - Posts
    - User-post interactions
    - Friendship
  - Feature engineering
    - Post features
      - Textual content
      - Images or videos
      - Reactions
      - Hashtags
      - Post's age
    - User features
      - Demographics
      - Contextual information
      - User - post historical interaction
      - Being mentioned in the post
    - User-author affinities
      - Like/click/comment/share rate
      - Friendship length
      - Close friends and family
## Model development
  - N independent DNNs
  - A multi-task DNN
  - Adding skip classification and dwell-time prediction task to the model
## Evaluation
  - Offline metrics
    - ROC-AUC
  - Online metrics
    - CTR
    - Reaction rate
    - Total spent time
    - User satisfaction rate
## Serving
  - Data preparation pipeline
    - Batch feature computation
    - Online feature computation
  - Prediction pipeline
    - Retrieval service
    - Ranking service
    - Re-ranking service
## Other talking points

