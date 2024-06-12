This repository is for our paper entitled "On the impact of several regularization techniques on label noise robustness of self-supervised speaker verification systems" currently under review.

Code of our experiments and trained models will be available upon acceptance of the paper.

# Study of several loss functions
In Table 1, we performed a large-scale study of 39 metric learning loss functions including all our mentioned families of loss objectives and other widely used losses using CAMSAT-based pseudo-labels.
![](/study_of_various_losses_for_speaker_verification.png)

# CAMSAT clustering algorithm
For clustering, we adopt the same CAMSAT clustering approach used in [19] to generate pseudo-labels. CAMSAT is based on augmentation mix and self-augmented training. The goal is to impose invariance to data augmentation on the output predictions of deep models in an end-to-end fashion while maximizing the information-theoretic dependency between samples and their predicted discrete representations (cluster assignments). It provided both state-of-the-art speaker clustering and SV performance. In this paper, we try to investigate several metric learning loss functions to enhance the generalization performance of self-supervised speaker embedding systems and to mitigate the negative effect of heavy noise in the generated pseudo-labels (PLs) used to train these systems. Please refer to [19] for details about CAMSAT architecture and training details.

# The clustering evaluation metrics
Following the commonly used evaluation metrics for clustering, we assess the quality of the generated pseudo-labels using the following three supervised clustering metrics: ![](/Clustering_metrics.png)

# The clustering performance of our employed pseudo-labels
Table 3 shows the clustering performance of our employed CAMSAT clustering-based pseudo-labels using CAMSAT. ![](/clustering_performance_pseudo_labels.png)

[19] A. Fathan and J. Alam, “Camsat: Augmentation mix and self-augmented training clustering for self-supervised speaker recognition,” in IEEE Automatic Speech Recognition and Understanding (ASRU) Workshop, 2023.
