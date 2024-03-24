<div align="justify">

# ArcFace: Additive Angular Margin Loss for Deep Face Recognition

- Introducing an Additive Angular Margin Loss (ArcFace)
- Proposing sub-center ArcFace
- Exploring the inverse problem, mapping feature vectors to face images

## Introduction

Face representation using DCNN embedding is the method of choice for face recognition. DCNNs map the face image,
typically after a pose normalization step into a feature that should have small intra-class and large inter-class
distance. There are 2 main lines of research to train DCNNs for face recognition.

- Training a multi-class classifier which can separate different identities in the training set, such by using **a softmax classifier**
- Learning directly an embedding, such as the **triplet loss**

However, both the softmax loss and the triplet loss have some drawbacks.

- For the softmax loss: (1) the learned features are separable for the closed-set classification problem but not discriminative enough for the open-set face recognition problem; (2) the size of the linear transformation matrix $W \in \R^{d \times N}$ increases linearly with the identities number $\N$
- For the triplet loss: (1) there is a combinatorial explosion in the number of face triplets especially for large-scale datasets, leading to a significant increase in the number of iteration steps; (2) semi-hard sample mining is a quite difficult problem for effective model training.

To adopt margin benefit but avoid the sampling problem in the Triplet loss
</div>


