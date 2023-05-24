---
markmap:
  colorFreezeLevel: 6
  maxWidth: 200
---

# VRS
## Clarifying Requirements
## Framing as ML
  - Defining the Ml objective
    - Mauimize # of user clicks
    - Mauimize # completed videos
    - Mauimize watch time
    - Mauimize # of Relevant videos
  - Specifying input and output
  - ML category
    - Non-personalised
      - Rule-based filtering
    - Personalised 
      - Content-based filtering
      - Collaborative filtering
      - Hybird filtering
## Data Preparation
  - Data engnineering 
    - Videos
    - Users
    - User-video interactions
  - Feature engineering
    - Video features
      - Video ID
      - Duration
      - Language
      - Titles And tags
    - User features
      - Demographics
      - Contextual information
      - Historical interactions
        - Search history
        - Liked videos
        - Watched videos
        - Impressions
## Model Development
  - Matrix factorization
    - Feedback matrix
      - Explicit feedback
      - Implicit feedback
      - Combination of both
    - Training loss
      - Squared distance over observed pairs
      - Squared distance over all pins
      - Weighted combination of observed and unobserved pins
    - Optimization algorithm
      - SCG
      - WALS
  - Two-tower neural network
## Evaluation
  - Offline metrics
    - Precision@k
    - mAP
    - Diversity
  - Online metrics
    - CTR
    - #of completed videos
    - Total watch time
    - Explicit user feedback
## Serving
  - Candidate generation
  - Scoring
  - Re-ranking
  - challenges in recommendation system
    - Serving speed
    - Precision
    - Diversity
    - Cold-start problem
    - training scalability
## Other talking points
  