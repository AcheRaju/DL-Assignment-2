QUESTION-1
# Seq2Seq Transliteration with RNNs

This project performs Hindi transliteration using a Seq2Seq model built in PyTorch. It supports RNN, GRU, and LSTM-based encoders and decoders.

## Dataset
We use the Dakshina dataset (`hi.translit.sampled.train.tsv`, `dev.tsv`, etc.).

## How to Train
1. Ensure the dataset files are in `/content/`
2. Run the Python script.
3. The model trains for 10 epochs and prints accuracy on the dev set.

## Model Details
- Embedding dim: 64
- Hidden dim: 128
- RNN Type: GRU (can change to `rnn` or `lstm`)
- Teacher Forcing: 50%


## Sample Output
Input: namaste | Target: नमस्ते | Predicted: नमस्ते
Input: dilli   | Target: दिल्ली | Predicted: दिल्ली


## Dependencies
- Python 3
- PyTorch


QUESTION-2
Lyrics Generation using GPT-2
This project fine-tunes OpenAI's GPT-2 model on custom song lyrics from Ed Sheeran and Justin Bieber to generate new lyrics in a similar style.

Dataset
Two CSV files: EdSheeran.csv and JustinBieber.csv
Each file contains a Lyric column with cleaned song lyrics line-by-line

How to Train
Upload EdSheeran.csv and JustinBieber.csv to your working directory (e.g., /content/ for Colab).
Run the training script or notebook.
The model will fine-tune GPT-2 for 3 epochs on the combined dataset.

Model Architecture
Base Model: GPT-2 (gpt2)
Tokenizer: GPT2Tokenizer with EOS token as the pad token
Max Length: 512 tokens
Training Framework: HuggingFace Transformers
Training Settings:
Batch size: 2
Epochs: 3
Loss: Causal Language Modeling (cross-entropy)

Sample Output

Prompt: I remember the night we met

Generated:
I remember the night we met  
You played that song on repeat  
The lights were low, but your eyes  
Were brighter than the city street...
