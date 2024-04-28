# Joint Embedding Predictive Architectures (JEPAs) and Self-Supervised Learning (SSL)

Welcome to the repository dedicated to exploring the fascinating world of Joint Embedding Predictive Architectures (JEPAs) and self-supervised learning (SSL) based on the paper Self-Supervised Learning from Images with a Joint-Embedding Predictive Architecture <https://arxiv.org/abs/2301.08243>. Here, you'll find implementations and experiments aimed at pushing the boundaries of understanding and utilizing predictive architectures for learning semantically rich embeddings of data, particularly in the image domain.

## Repository Overview

This repository is a playground for various implementations and experiments, including:

- **I-JEPA (Image-JEPA) Implementation:** A barebones implementation of I-JEPA, a general architecture applied to the image domain. Variants include:
  - I-JEPA using a Vision Transformer (ViT)
  - I-JEPA using an Energy Transformer

- **Saccade JEPA:** A novel variant inspired by mammalian saccades, incorporating small augmentations (movements) and prediction tasks akin to a JEPA. Features include:
  - Prediction loss
  - Cycle consistency loss
  - VICReg loss

## Key Features of Saccade JEPA

- **Plug-and-Play Architecture:** Saccade JEPA is adaptable with different backbone architectures. It currently supports ConvNet models as teacher and student networks, with a Multi-Layer Perceptron (MLP) serving as the predictor.

- **Loss Types:** Saccade JEPA employs various loss functions for effective learning:
  - Prediction loss: Huber loss between target image encoding and its prediction from a shifted version, with positional embedding guiding the predictor network.
  - Cycle consistency loss: Ensures that shifting back to the original location reproduces the original image representation.
  - VICReg loss: Incorporates invariance and covariance components for robust learning.

## Getting Started

To dive into the experiments and implementations, follow these steps:

1. **Prerequisites:** Ensure you have the following libraries installed: `torch`, `torchvision`, `einops`, and `tqdm`. For optional plotting, you'll need `matplotlib` and `UMAP`.

2. **Run Experiments:** Utilize `jepa/train.py` to run experiments and explore the performance of different architectures.

3. **EnergyJepa Installation:** If using EnergyJepa, ensure the Energy Transformer implementation is installed via pip, or copy the main file from its repository to this one.

## What are JEPAs?

JEPAs are architectures designed to learn semantically rich embeddings of data through self-supervised learning. They operate on the principle of prediction, wherein networks are trained to predict embeddings of given data portions from other embedded portions.

## Evaluation and Metrics

Evaluation of JEPAs can be challenging due to the self-supervised objective. However, several methods are employed, including linear probes, KNN, attention map visualization, correlation dimension analysis, and UMAP embeddings.

## Implementation Notes

The repository includes insightful implementation notes, such as interpretations of the paper, cropping/masking strategies, and batch masking techniques to enhance training stability.

## Next Steps

Feel free to explore the implementations, experiment with different configurations, and contribute to advancing our understanding of predictive architectures and self-supervised learning.

## Acknowledgments

Special thanks to the original paper authors and contributors to the libraries used in this repository.

## Have Questions or Feedback?

If you have any questions, feedback, or suggestions for improvement, please don't hesitate to reach out. Your contributions are valuable in fostering a collaborative learning environment.

Happy exploring! 🚀

![embeds](https://github.com/dreamboat26/curly-memory/assets/125608791/d521acb8-497c-40b3-9514-feda0f67eb6e)

![example](https://github.com/dreamboat26/curly-memory/assets/125608791/cd0271b1-f3bf-4cbc-b872-f8df48deab1e)

https://github.com/dreamboat26/curly-memory/assets/125608791/1abf8045-7d00-4285-9327-0346031b0813

