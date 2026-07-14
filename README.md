# Deep CNN Autoencoder - Image Compression & Denoising

A comprehensive deep learning project implementing convolutional autoencoders for image compression and noise reduction. Explores unsupervised learning techniques using TensorFlow and Keras.

## 🎯 Overview

This project implements deep convolutional autoencoders to:
- Compress images to lower-dimensional representations
- Reconstruct images with minimal quality loss
- Denoise corrupted images through unsupervised learning
- Experiment with different encoder-decoder architectures
- Analyze compression ratios and reconstruction quality

## 🛠 Tech Stack

- **Language:** Python 3
- **Deep Learning:** TensorFlow, Keras
- **Data Processing:** NumPy, Pandas
- **Visualization:** Matplotlib, Seaborn
- **Environment:** Google Colab (GPU support)

## 📁 Project Contents

```
├── Autoencoder_final.ipynb      Final optimized implementation
├── Autoencoder1_.ipynb           Initial experiments and development
├── classifier.ipynb              Image classification experiments
├── cifar_distribution.png        Dataset visualization
├── models/                        Saved trained models
└── README.md                      This file
```

## 🚀 Getting Started

### Prerequisites

- Python 3.7+
- Google Colab account (recommended for GPU)
- Jupyter Notebook or Colab
- ~2GB disk space for datasets

### Installation

1. Clone the repository:
```bash
git clone https://github.com/Mhmd-Shkeir/Autoencoder_object_detector.git
cd Autoencoder_object_detector
```

2. Install dependencies:
```bash
pip install tensorflow keras numpy matplotlib
```

3. Open notebooks:
```bash
# For Google Colab
# Upload to Drive and open with Colab
# For local Jupyter
jupyter notebook
```

## 📊 Project Components

### Autoencoder Architecture

```
Input Image
    ↓
[Encoder] → Compressed Representation (Bottleneck)
    ↓
[Decoder] → Reconstructed Output
    ↓
Comparison with Original
```

### Key Components

1. **Encoder**
   - Convolutional layers with ReLU activation
   - Progressive dimensionality reduction
   - Extracts features from input images

2. **Bottleneck**
   - Compressed representation
   - Typically 32-128 dimensions
   - Information "bottleneck" forcing efficient compression

3. **Decoder**
   - Transposed convolutional layers
   - Progressive upsampling
   - Reconstructs images from compressed form

## 💡 Applications

### Image Compression
- Reduce image file sizes
- Maintain acceptable quality levels
- Useful for storage and transmission

### Image Denoising
- Remove noise from corrupted images
- Unsupervised learning approach
- No labeled clean/noisy pairs required

### Feature Extraction
- Learn efficient representations
- Use encoder for downstream tasks
- Dimensionality reduction

### Data Augmentation
- Generate variations of images
- Noise injection and recovery
- Training data expansion

## 📈 Performance Metrics

- **Reconstruction MSE** - Mean squared error between input and output
- **Compression Ratio** - Original size vs. compressed size
- **PSNR (Peak Signal-to-Noise Ratio)** - Image quality measure
- **SSIM (Structural Similarity Index)** - Perceptual similarity

## 🎓 Learning Outcomes

Through this project, you'll learn:
- ✅ Convolutional neural network design
- ✅ Autoencoder architecture and training
- ✅ Unsupervised learning techniques
- ✅ Image processing with deep learning
- ✅ TensorFlow/Keras practical implementation
- ✅ Hyperparameter tuning
- ✅ Model evaluation metrics

## 🔧 Configuration

### Model Parameters

```python
# Encoder configuration
input_shape = (28, 28, 1)  # or (32, 32, 3) for CIFAR-10
latent_dim = 64  # Bottleneck dimension
conv_filters = [32, 64, 128]  # Progressive filters

# Training configuration
batch_size = 32
epochs = 50
optimizer = 'adam'
loss = 'mse'  # Mean squared error
```

### Datasets Supported

- **MNIST** - 28x28 grayscale images (0-9 digits)
- **CIFAR-10** - 32x32 RGB images (10 classes)
- **Fashion-MNIST** - 28x28 grayscale clothing
- Custom datasets - Support for any image format

## 📝 Experiments

### Compression Experiments
- Test different latent dimensions
- Compare reconstruction quality vs. size
- Analyze convergence rates

### Denoising Experiments
- Train on noisy variants
- Test on unseen noise levels
- Evaluate robustness

### Architecture Experiments
- Shallow vs. deep encoders
- Different filter configurations
- Various activation functions

## 🎯 Results

Expected outcomes with proper tuning:
- MNIST: ~0.001 MSE, high PSNR
- CIFAR-10: ~0.003 MSE, acceptable visual quality
- Compression ratios: 4:1 to 16:1 depending on acceptable loss

## 🚧 Future Enhancements

- [ ] Variational Autoencoders (VAE)
- [ ] Adversarial Autoencoders (AAE)
- [ ] 3D autoencoder for video
- [ ] Real-time inference optimization
- [ ] Model quantization for mobile
- [ ] Comparative analysis with other methods
- [ ] Interactive visualization dashboard

## 📚 Resources

- [TensorFlow Documentation](https://www.tensorflow.org/docs)
- [Keras API](https://keras.io/api/)
- [Autoencoders Paper](https://arxiv.org/abs/1312.6199)
- [Convolutional Networks](http://deeplearning.stanford.edu/tutorial/)

## 📄 License

MIT License - Free to use and modify

## 👤 Author

**Mhmd-Shkeir**

## 🤝 Contributing

Contributions welcome! Areas for improvement:
- Additional architectures and comparisons
- Optimization techniques
- Performance benchmarks
- Dataset support
- Documentation enhancements

Feel free to:
1. Fork the repository
2. Create a feature branch
3. Submit improvements
4. Open issues for bugs or suggestions

## 📞 Support

For questions or issues:
- Open an issue on GitHub
- Check existing notebooks for examples
- Review TensorFlow documentation
- Experiment with hyperparameters

---

**Note:** This is an educational project for learning deep learning concepts. Notebooks are self-contained and can be run independently.
