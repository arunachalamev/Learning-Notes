---
markmap:
  colorFreezeLevel: 6
  maxWidth: 200
---

# VSS

## Clarifying Requirements 
 - (ranking?, video?, pesonalization? used metadata? moderate?, like/share/save, training data online, how fast?)
## Framing as ML
- Defining the ML Objective
  - accurately retrieve images
- Specifying input and output
    - input image -> output ranked images
- ML Category 
  - Ranking (Representation Learning)
    - how to rank images using represenational learning
## Data Preparation
- Data engineering
  - Images
  - Users
  - User-Image Interaction
- Feature engineering
  - Image Preprocess
    - Resizing
    - Scaling
    - Z-score normalization
    - Color mode
## Model development
- Model Selection
  - CNN-based Architecture
    - NN - good for unstructured data
    - NN - easy to learn embedding
- Model Training
  - Contrastive training
  - Constracting training data 
    - Human judgements
    - User-Clicks
    - Self-supervision
  - Contrastive loss function
    - compute similarities -> softmax -> cross-entropy
## Evaluation
- Offline
  - MRR
  - Recall @ K
  - Precision @ K
  - mAP
  - nDCG
- Online
  - CTR
  - Avg time spent on suggested image
## Serving
- Prediction pipeline
  - Embedding generation service
  - Nearest neighbor service
  - Re-ranking service
- Indexing pipeline
  - Indexing service
- NN performance
  - Exact nearest neighbour
  - Approximate nearest neighbour
    - Tree-based
    - LSH-based
    - Clustering based
    - 
## Other talking Points
- Moderate content
- Position bias
- Metadata such as tag to improve
- Smart crop 
- Use GNN to learn representation
- Search image by textual query
- active learning 

