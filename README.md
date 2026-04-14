# 👗 Fashion MNIST — Image Reconstruction & Classification

Deep learning project on the Fashion MNIST dataset, exploring self-supervised, unsupervised, and supervised approaches for image reconstruction, denoising, and classification.

> **Course:** Cognition and Computation — University of Padova  
> **Author:** Simone Zanetti  
> **Environment:** Google Colab (PyTorch)

---

## 📌 Objective

Investigate how autoencoders, Deep Belief Networks (DBN), and perceptrons can be combined to reconstruct and classify Fashion MNIST images under varying levels of noise, drawing a parallel with cognitive theories of perception and self-supervised learning.

---

## 📁 Repository Structure

```
Fashion-MNIST-Reconstruction/
├── Simone_Zanetti_fashionMnist.ipynb
└── README.md
```

---

## 📊 Dataset

- **Fashion MNIST** — 28×28 grayscale images, 10 clothing classes
- 10,000 samples as test set, remainder for training
- Noise augmentation applied at multiple perturbation levels (up to 80%)

---

## 🧠 Models & Topics Covered

**1. Autoencoder (Self-Supervised)**
- Dense AE — 1 layer vs 2 layers comparison
- Denoising AE — trained on noisy data to learn noise removal
- Deep Dense AE — deeper architecture + multi-noise oversampling
- Iterative reconstruction (feeding output back as input)

**2. Deep Belief Network (Unsupervised)**
- DBN training and receptive field visualization at different layers
- Hierarchical clustering of internal representations
- Linear readout evaluation

**3. Supervised Classification**
- Perceptron on raw features
- AE + DBN + Perceptron pipeline
- Robustness to adversarial attacks

---

## 📈 Key Results

| Model | Notes |
|---|---|
| Dense AE (2 layers, denoising) | Best reconstruction quality; effective up to ~80% noise |
| CNN AE | Similar reconstruction loss but weaker on noisy inputs |
| AE + DBN + Perceptron | More noise-robust than DBN + Perceptron alone |
| Multi-noise AE | Best generalization across noise levels |

- Hardest classes to classify: **Shirt** (confused with T-shirt/Pullover) and **Coat** (confused with Trouser)
- Autoencoder pre-processing consistently improves downstream classification robustness

---

## 🚀 Running the Notebook

Recommended: open directly in **Google Colab** (GPU runtime required).

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/SimoneZanetti00/NOME-REPO/blob/main/Simone_Zanetti_fashionMnist.ipynb)

> ⚠️ Make sure to set the runtime to **GPU** (Runtime → Change runtime type → T4 GPU),
> otherwise CUDA device errors will occur when running the DBN section.

## 🛠️ Tools & Libraries

- **Language:** Python (Google Colab)
- **Main libraries:** `PyTorch`, `torchvision`, `matplotlib`, `numpy`, `scikit-learn`
