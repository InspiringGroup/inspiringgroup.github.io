---
title: "LLMs Can Understand Encrypted Prompt: Towards Privacy-Computing Friendly Transformers"
layout: textlay
excerpt: "LLMs"
sitemap: false
permalink: /publications/llms
---

# LLMs Can Understand Encrypted Prompt: Towards Privacy-Computing Friendly Transformers

Under review. Preprint available at <a href="https://arxiv.org/abs/2305.18396">arxiv</a>.

## Brief Introduction

This work combines the primitives of homomorphic encryption (HE) and secure multi-party computation (MPC) to achieve private inference on large language models, achieving maximum throughput and minimum communication costs, while protecting both input data of the client and the model weights of the server. Specifically, HE is used for linear layers such as fully connected layers using matrix multiplication, and MPC is used for non-linear layers such as ReLU/GELU activation function. For further acceleration, we implement our HE cryptosystem with GPU parallel kernels. Our implementation of linear layers with GPU-accelerated HE framework is open-sourced at <a href="https://github.com/lightbulb128/troy">Github repository</a>.

## Abstract

Prior works have attempted to build private inference frameworks for transformer-based large language models (LLMs) in a server-client setting, where the server holds the model parameters and the client inputs the private data for inference. However, these frameworks impose significant overhead when the private inputs are forward propagated through the original LLMs. In this paper, we show that substituting the computation- and communication-heavy operators in the transformer architecture with privacy-computing friendly approximations can greatly reduce the private inference costs with minor impact on model performance. Compared to the state-of-the-art Iron (NeurIPS 2022), our privacy-computing friendly model inference pipeline achieves a 5× acceleration in computation and an 80\% reduction in communication overhead, while retaining nearly identical accuracy. 
