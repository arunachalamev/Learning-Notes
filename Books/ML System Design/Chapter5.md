---
markmap:
  colorFreezeLevel: 6
  maxWidth: 200
---

# HCD
## Clarifying Requirements
## Framing as ML
  - Defining the Ml objective
  - Specifying input and output
    - Late fusion
    - Early fusion
  - ML category 
    - Single binary classifier
    - One binary classifier per harmful class
    - Multi-label classifier 
    - Multi-task classifier
      - Shared layer
      - task specific layer
## Data preparation 
  - Data engineering
    - Users
    - Posts
    - User-post interactions
  - Feature engineering
    - Textual content 
      - Preprocess
      - vectorization
    - Image or video
      - Preprocess 
      - Feature extraction
    - User reactions to the post 
    - Author features
    - Contextual information
## Model Development 
  - Model selection
    - Multi-task neural network
  - Model training
    - Constructing the dataset
      - Hand labeling
      - Natural labeling
    - Choosing the loss function
      - Cross-entropy
## Evaluation
  - Offline metrics
    - PR curve
    - ROC curve
    - PR-AUC
    - ROC-AUC 
  - Online metrics
    - Prevalence
    - Harmful impression
    - Valid appeals
    - Proactive rate
    - user reports per harmful class
## Serving 
  - Harmful content detection service
  - Violation enforcement service
  - Demoting service
## other talking points
   



     

    
  
    
 