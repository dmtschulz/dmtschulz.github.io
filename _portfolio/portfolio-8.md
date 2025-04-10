---
title: "CNN vs MLP on CIFAR-10"
excerpt: "Comparing convolutional and feedforward networks on CIFAR-10, including robustness to image translations. <br/><img src='https://raw.githubusercontent.com/dmtschulz/cnn-vs-mlp-cifar10/refs/heads/main/plots/translated_accuracy_boxplot.png'>"
collection: portfolio
---

### CNN vs MLP on CIFAR-10

This project compares Convolutional Neural Networks (CNNs) and Multilayer Perceptrons (MLPs) on the CIFAR-10 dataset.  
We train both architectures on a reduced dataset and evaluate classification accuracy, parameter efficiency, robustness to image translations, and interpret learned features.

**Key Highlights:**
- **Architectures**: 3-layer MLP vs 3-block CNN
- **Avg Test Accuracy**: MLP – 41.1%, CNN – 64.9%
- **Accuracy on Translated Images**: MLP – 31.2%, CNN – 57.1%
- **CNN Advantage**: ~16% absolute accuracy gain on clean data; ~26% on translated images
- **Feature Maps**: Visualized intermediate activations per conv block
- **Tools**: PyTorch, Torchvision, Matplotlib, TQDM

Check out the [GitHub repository](https://github.com/dmtschulz/cnn-vs-mlp-cifar10).

Accuracy comparison on translated image:
![CNN vs MLP Accuracy Comparison](https://raw.githubusercontent.com/dmtschulz/cnn-vs-mlp-cifar10/refs/heads/main/plots/translated_accuracy_boxplot.png)
