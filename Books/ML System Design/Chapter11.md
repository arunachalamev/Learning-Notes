---
markmap:
  colorFreezeLevel: 6
  maxWidth: 200
---

# PYMK
## Clarifying Requirements
## Framing as ML
  - Defining the Ml objective
    - Maximize # of formed connections
  - Specifying input and output
  - ML category
    - Pointwise LTR
    - Edge prediction
## Data Preparation
  - Data engineering
    - Users
    - Connections
    - Interactions
  - Feature engineering
    - User features
      - Demographics
      - #0f followers/followings
      - Account's age
      - #of received reactions
    - User-user affinities
      - Education/work affinity
      - Social affinity
## Model development
  - GNN
## Evaluation
  - Offline metrics
    - GNN model:ROC-AUC
    - PYMK system:mAP
  - Online metrics
    - #of sent connection requests
    - #of accepted connection requests
## Serving
  - Efficienty
    - Friends of friends
    - Pre-compute PYMK
  - ML system design
    - PYMK generation pipeline
    - Prediciton pipeline
## Other talking points
