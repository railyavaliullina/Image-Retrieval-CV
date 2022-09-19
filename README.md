# Image-Retrieval


### Result examples

![image](https://user-images.githubusercontent.com/113569606/191005545-d0ee2e9a-da9b-4585-a710-82f028c0c9a7.png)


## About The Project

1) Implementation of training pipeline for Image Retrieval task,

2) Training on Stanfords Online Products Dataset (SOP).

## Getting Started

File to run:

        train/main.py
        
        or 
        
        hw-imageretrieval-final.ipynb
        
        
 There is also `Memory Bank` implementation in `models/memory_bank.py` for training strategy with saving embeddings while training to obtain more informative and challenging triplets as it was proposed in paper `Cross-Batch Memory for Embedding Learning`:
 
        https://arxiv.org/pdf/1912.06798.pdf
        

## Implementation details

Model architecture consists of:

    - ResNet-50 (without last classification layer) from paper 'Deep Residual Learning for Image Recognition'
    
            https://arxiv.org/pdf/1512.03385.pdf,
        
    - Global Average Pooling (GAP) applied to the last layer of ResNet,
    - fully-connected layer to get embedding for input image.

Loss Function `Triplet Loss` and `hard-negative sampling` technique are implemented as it was proposed in `FaceNet: A Unified Embedding for Face Recognition and Clustering` paper:
        
            https://arxiv.org/pdf/1503.03832.pdf
            
            
 T-SNE visualization for visualizing result embeddings for images from test set is in:
 
        train/main.py
    
