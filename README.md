# Neural-Machine-Translation-Using-Transformer-From-Scratch

![image](https://github.com/SaadElDine/Neural-Machine-Translation-Using-Transformer-From-Scratch-/assets/113860522/28692c2f-7349-414e-afb0-d57811f75339)

## Project Overview
This project involves training a custom transformer-based encoder-decoder model using the PyTorch library. The aim is to fine-tune the model on a specific language task to improve its performance and generalization capability. The training process involves minimizing the negative log-likelihood over the training dataset and validation for early stopping and model selection based on perplexity.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Model Architecture](#model-architecture)
- [Training](#training)
- [Validation and Performance](#validation-and-performance)
- [Contributing](#contributing)
  
## Installation
Before you begin, ensure you have met the following requirements:
- Python 3.x
- PyTorch 1.x
Install the required Python packages using pip...

## Usage
To use this project to train your model, follow these steps:
1. Prepare your dataset in a tokenized format.
2. Configure your model parameters and training settings in the provided training script.
3. Run the training script to start training the model.
4. The best-performing model will be saved to the specified `model_path`.

## Model Architecture
The model is a transformer-based EncoderDecoder that consists of:
- An encoder with 3 layers
- A decoder with 3 layers
- A hidden size of 32
- An intermediate size of 128 (32 * 4)
- 4 attention heads
- A maximum sequence length of 32 tokens
- A hidden dropout probability of 0.1

## Training
During training, the following steps occur:
- The model is trained for a maximum of 15 epochs with early stopping if the validation perplexity does not improve.
- The Adam optimizer with a learning rate of 1e-3 is used for parameter optimization.
- A batch size of 32 is used during training.
- Model checkpoints architecture saved periodically when the model achieves lower perplexity on the validation dataset.
- Gradient clipping is applied to avoid exploding gradients.
- The learning rate can be adjusted based on validation performance to fine-tune convergence.
  
## Validation and Performance
- Validation is performed after a set number of iterations as defined by `valid_niter`.
- Perplexity, a measure of how well the probability distribution predicted by the model matches the true distribution, is used as the performance metric.
- The model with the lowest perplexity on the validation set is considered the best and is saved.


