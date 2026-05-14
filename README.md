# part-3-nlp-sequence-modeling
BITSOM Assignment 5\
  NLP Sequence Modeling

# Dataset Link
https://drive.google.com/drive/folders/16lHceA9Y0e3BMD6Ru3sOl7PP7yO2_s50

# NLP and Sequence Modeling Mini Project

## Objective

This project demonstrates:
- NLP preprocessing
- Text vectorization
- Baseline machine learning model
- Sequence modeling using LSTM
- Understanding transformers and attention

## Tasks Performed

### 1. Dataset Understanding
- Number of records
- Target labels
- Sample texts
- Average text length
- Class distribution

### 2. Text Preprocessing
- Lowercasing
- Removing special characters
- Tokenization
- Stopword removal
- Sequence padding

### 3. Text Vectorization
Used:
- TF-IDF
- Tokenizer-based sequences

### 4. Baseline Model
- Logistic Regression with TF-IDF

### 5. Sequence Model
- LSTM-based sequence classifier

### 6. Evaluation Metrics
- Accuracy
- Classification Report
- Confusion Matrix


## Explain why text must be converted into vectors before being used by a model.
Machine learning models, including Deep Learning neural networks, are fundamentally mathematical engines. They operate using numerical calculations (like addition, multiplication, and calculus-based optimization). They cannot natively "read" strings or interpret letters like a human brain can. Therefore, we must convert raw text into numerical representations (vectors) so the model can process them. Vectorization maps words to numbers in a way that allows the computer to compute similarities, recognize patterns, and map input text to output classifications.

## Attention and Transformer Reflection

### Why RNNs struggle with long-term dependencies
RNNs process text sequentially, causing earlier information to fade over time due to vanishing gradients. As sequences get longer, the "memory" of early words fades away or gets overwritten by newer words—a phenomenon known as the "vanishing gradient problem." If a sentence is 50 words long, the RNN might forget the subject from the first few words by the time it reaches the end.

### How LSTMs help with memory
LSTMs use memory cells and gates to retain important information for longer sequences. These gates act like valves that learn what information is important to keep in long-term memory and what information can be forgotten. This helps them bridge much larger gaps in text than standard RNNs.

### What attention solves in sequence-to-sequence tasks
Attention allows the model to focus on the most relevant words instead of compressing everything into one fixed vector. At each step of predicting an output, it calculates a set of "weights" to decide which specific input words it should focus on (pay attention to) right now.

### Why transformers are important in modern NLP and Generative AI
Transformers process sequences in parallel and use self-attention, making them faster and more effective for modern NLP and Generative AI systems like ChatGPT. Because they process all words simultaneously rather than sequentially, they are highly parallelizable (making them incredibly fast to train on massive GPUs) and excel at understanding deep context and relationships across vast amounts of text.
