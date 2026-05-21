What This Project Does:
This project builds a deep learning-based joke generator using an LSTM (Long Short-Term Memory) model. It is trained on a small dataset of jokes and learns word patterns to predict the next word in a sequence. Given an input word or phrase, the model generates the next word, allowing simple text generation.

Example:
Input: "boiling"
Output: "water"

How It Works:

The dataset consists of multiple jokes stored as raw text.
The text is tokenized into sequences of integers using a tokenizer.
Sequences are converted into a supervised learning format:
Input: sequence of words
Output: next word
Sequences are padded to ensure uniform length.
The model is trained to predict the next word based on previous words.

Architecture:
The model uses the following layers:

Input (tokenized sequences)
→ Embedding Layer (converts words to vectors)
→ LSTM Layer (150 units)
→ Dense Layer (Softmax activation)
→ Output (next word prediction)

Details:

Embedding size: 100
LSTM units: 150
Loss function: categorical crossentropy
Optimizer: Adam
Epochs: 20

Tech Stack:

Python
TensorFlow / Keras
NumPy

How to Use:

Train the model on the dataset.
Provide a seed word or phrase.
Convert it into a sequence using the tokenizer.
Pad the sequence.
Predict the next word using the model.
Convert the predicted index back to a word.

Why Accuracy is Low:

Very small dataset (only a few dozen jokes)
Humor is highly creative and unpredictable
Multiple correct outputs exist, but model allows only one
Limited context understanding from short sequences
Low training epochs leading to underfitting

Future Enhancements:

Use a larger dataset (e.g., Reddit jokes, Kaggle datasets)
Train for more epochs
Use Bidirectional LSTM or GRU
Replace argmax with temperature sampling
Generate full sentences instead of one word
Build a web interface using Flask or FastAPI
Fine-tune pretrained models like GPT-2

Key Takeaway:
This project demonstrates how to convert text into a supervised learning problem and train an LSTM for sequence prediction. It is a beginner-friendly NLP project and a foundation for more advanced text generation systemss.