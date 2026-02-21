# Neural Network Framework

## What do you want to build?

Build a deep learning framework in Python (with NumPy/C extensions for performance) that supports automatic differentiation, common layer types, and training loops. The framework should be usable for training real models on real datasets.

The implementation must include:
- Tensor class with automatic differentiation (reverse-mode autograd)
- Computation graph construction and backpropagation
- Layer types: Linear, Conv2d, BatchNorm, ReLU, Sigmoid, Softmax, Dropout, MaxPool2d
- Loss functions: CrossEntropy, MSE
- Optimizers: SGD (with momentum), Adam
- Data loading utilities with batching and shuffling
- Model serialization (save/load)
- A training example on MNIST that achieves >95% accuracy

## How do you consider the project is success?

1. Autograd correctly computes gradients — validated against PyTorch on at least 10 different computation graphs (relative error <1e-5)
2. A CNN trained on MNIST achieves >95% test accuracy within 10 epochs
3. All layer types produce outputs matching PyTorch within numerical tolerance (1e-5 relative error)
4. Adam optimizer converges faster than vanilla SGD on a benchmark task
5. Model save/load roundtrip preserves weights exactly
6. Training loop handles variable batch sizes and datasets correctly
7. Test suite with at least 30 tests covering autograd, layers, optimizers, and end-to-end training
8. Training on MNIST completes in <5 minutes on a modern CPU
