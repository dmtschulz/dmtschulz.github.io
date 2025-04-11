---
title: "Autoencoder for Anomaly Detection"
excerpt: "Trained on zeros. Detects all the weird stuff. <br/><img src='https://raw.githubusercontent.com/dmtschulz/autoencoder-mnist-anomaly/refs/heads/main/plots/anomaly_heatmaps.png' width='250'>"
collection: portfolio
---

### Autoencoder for Anomaly Detection on MNIST

This project explores using an undercomplete autoencoder to detect anomalies in the MNIST dataset.  
We train the model solely on one class (zeros) and detect anomalies based on reconstruction error.

**Key Highlights:**
- **Model**: Fully connected autoencoder with 2–32 latent units
- **Trained On**: Only digit '0' — to simulate anomaly detection in one-class settings
- **Detection Method**: Reconstruction loss (MSE)
- **ROC AUC**: Measured to evaluate separation between normal and anomalous digits
- **Visualizations**:
  - Reconstructed digits vs original
  - Anomaly heatmaps
  - Latent space scatter (2D)

**Tools**: PyTorch, Torchvision, Matplotlib, Scikit-learn

Check out the [GitHub repository](https://github.com/dmtschulz/mnist-autoencoder-anomaly).

Anomaly detection heatmap (darker = less expected):
![Anomaly Heatmap](https://raw.githubusercontent.com/dmtschulz/autoencoder-mnist-anomaly/refs/heads/main/plots/anomaly_heatmaps.png)

Latent space with class labels (first 5):
![Latent Space](https://raw.githubusercontent.com/dmtschulz/autoencoder-mnist-anomaly/refs/heads/main/plots/latent_grid.png)