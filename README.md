# Urdu-to-English Translation Project

This project demonstrates a custom approach to building and evaluating an attention-based encoder-decoder RNN (with an optional LSTM bonus) for translating Urdu sentences to English. The focus is on understanding sequence-to-sequence learning through hands-on implementation, training, and evaluation using BLEU scores.

## Objectives

### Dataset Preparation:
- **Data Combination:**  
  Combine two sets of sentence-aligned files: one pair of `.dev` files and one pair of `.devtest` files.
- **Data Splitting:**  
  Shuffle the combined data and split it into:
  - 70% Training
  - 15% Validation
  - 15% Testing

### Model Development:
- **Custom Model:**  
  Build an encoder-decoder model with an attention mechanism using PyTorch. The implementation is done from scratch without relying on pre-built RNN libraries (except for built-in backpropagation).
- **Bonus:**  
  Implement an LSTM-based variant of the model.

### Training and Evaluation:
- **Training:**  
  Train the model on the prepared training set. During training, the model logs key metrics such as loss and BLEU score for each epoch.
- **Evaluation:**  
  Assess the model’s performance on the validation and test sets using BLEU scores (calculated using Moses multi-bleu.perl or NLTK’s `corpus_bleu`).

### Visualization and Analysis:
- Visualize training and validation loss curves as well as BLEU score trends to gain insights into model performance and convergence behavior.

## Training Log 

During training, the model logs metrics at each epoch. For instance:

  ```plaintext
  Epoch [1/50], Train Loss: 7.4014, Val Loss: 6.9863, Val BLEU: 0.00
  Epoch [2/50], Train Loss: 6.6392, Val Loss: 7.0377, Val BLEU: 0.00
  ...
  Epoch [49/50], Train Loss: 0.7452, Val Loss: 9.4111, Val BLEU: 0.84
  Epoch [50/50], Train Loss: 0.7110, Val Loss: 9.3564, Val BLEU: 0.82
 ```

## Clone the Repository
```bash
git clone https://github.com/your-username/Urdu-to-English-Translation.git
cd Urdu-to-English-Translation
