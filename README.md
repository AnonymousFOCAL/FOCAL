# FOCAL

This repository is the official implementation of 
[Fast and Accurate Online Coupled Matrix-Tensor Factorization via Frequency Regularization](URL) 
(submitted to KDD 2025).

## Abstract

How can we efficiently and accurately factorize multi-source data in dynamic and real-time environments?
Coupled matrix-tensor factorization (CMTF) is a powerful tool for such tasks, but existing methods often struggle with scalability, particularly when dealing with continuously streaming data.
Traditional CMTF approaches, while effective at capturing complex relationships, suffer from computational inefficiencies and the need for retraining as new data arrive.
Moreover, many techniques fail to properly incorporate the inherent temporal characteristics of the data, which could significantly enhance both accuracy and convergence speed.

In this paper, we propose FOCAL (Frequency-regularized Online Coupled Approximation for Low-rank factorization), an efficient CP decomposition method designed to enhance online coupled matrix-tensor factorization.
By effectively distinguishing between old and new data, FOCAL skips unnecessary computations, enabling fast and accurate updates without the need for full retraining in streaming settings.
Furthermore, FOCAL integrates frequency regularization into an online CMTF framework, which mitigates overfitting and accelerates convergence.
Through extensive experiments, we demonstrate that FOCAL outperforms existing state-of-the-art methods in terms of both speed and accuracy.
We also present results on anomaly detection using real-world data, showcasing FOCAL's effectiveness in identifying irregular patterns. 

## Prerequisites
Our code requires Tensor Toolbox (available at https://gitlab.com/tensors/tensor_toolbox).

## Datasets (INCOMPLETE)
We provide the synthetic datasets used in our experiments at [here](https://drive.google.com/open?id=1gt_L-RK1cXc8w1OCbU7q5pkabpA6L9JD&usp=drive_copy).
The real-world datasets are available at [Cityscapes](https://www.cityscapes-dataset.com/), [ADE20K](https://groups.csail.mit.edu/vision/datasets/ADE20K/), [DF2K](https://www.kaggle.com/datasets/thaihoa1476050/df2k-ost), [RiceLeaf](https://www.kaggle.com/datasets/shayanriyaz/riceleafs), and [Bird](https://www.kaggle.com/datasets/akash2907/bird-species-classification).

| **Dataset** | **Type** | **# of Images** | **Size** |
| :----------- | :----------- | -----------: | -----------: |
| $S_{n=8,\cdots,15}$ | Synthetic | 1K | $2^n \times 2^n$ |
| Cityscapes | Real-world | 5K | $2048 \times 1024$ |
| ADE20K | Real-world | 20K | $2048 \times 2048$ |
| DF2K | Real-world | 3K | $2040 \times 1536$ |
| RiceLeaf | Real-world | 3.3K | $3120 \times 3120$ |
| Bird | Real-world | 306 | $6000 \times 4000$ |

