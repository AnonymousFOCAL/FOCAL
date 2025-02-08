# FOCAL

This repository is the official implementation of 
"Fast and Accurate Online Coupled Matrix-Tensor Factorization via Frequency Regularization" (submitted to KDD 2025).

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
The real-world datasets are available at [ML-100K](https://grouplens.org/datasets/movielens/100k/), [Amazon](https://www.kaggle.com/datasets/deovcs/amazon-dataset), [Stock-US](), [Stock-JPN](), and [Stock-CHN]().

| Dataset      | Stream Type     | Tensor Size               | Matrix Size         |
|-------------|---------------|--------------------------|---------------------|
| **ML-100K**  | Single-Tensor  | $1682 \times 943 \times 200$   | $1682 \times 19$   |
| **Amazon**   | Single-Tensor  | $901 \times 1720 \times 200$  | $901 \times 170$   |
| **Stock-US** | Matrix-Tensor  | $501 \times 88 \times 3651$  | $3651 \times 10$   |
| **Stock-JPN** | Matrix-Tensor  | $300 \times 88 \times 3856$       | $3856 \times 10$       |
| **Stock-KR**  | Matrix-Tensor  | $1471 \times 88 \times 1170$       | $1170 \times 10$       |


