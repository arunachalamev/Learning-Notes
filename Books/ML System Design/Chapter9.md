---
markmap:
  colorFreezeLevel: 6
  maxWidth: 200
---

# SLVRP
## Clarifying Requirements
## Framing as ML
  - Defining the Ml objective
    - Predict user clicks
  - Specifying input and output
  - ML category
    - Session-based recommendation system
## Data Preparation
  - Data engineering
    - Users
    - Listings
    - User-listing interactions
  - Feature engineering
    - Search sessions
## Model development
  - Neural network
  - Negative sampling 
  - Adding global context to the training data
  - Add same-region negative pairs to the training data
## Evaluation
  - Offline metrics
    - Average rank of eventually-booked listing
  - Online metrics
    - CTR
    - Session book
## Serving
  - Training pipeline
  - Indexing pipeline
  - Prediction pipeline
    - Embedding fetcher service
    - Nearest neighbor service
    - Re-ranking service
## Other talking points
