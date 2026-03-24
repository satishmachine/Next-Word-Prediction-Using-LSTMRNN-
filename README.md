# Next Word Prediction Using LSTM RNN

A deep learning application that predicts the next word in a sequence using LSTM (Long Short-Term Memory) neural networks. The model is trained on Shakespeare's "Hamlet" and deployed via an interactive Streamlit web interface.

## 🎯 Features

- **LSTM-based next word prediction** - Uses a trained recurrent neural network to predict contextually relevant next words
- **Early stopping training** - Prevents overfitting by monitoring validation loss during training
- **Interactive web interface** - Built with Streamlit for easy user interaction
- **Pre-trained models** - Two trained models included for different training iterations
- **Text tokenization** - Automatic text-to-sequence conversion using a pre-fitted tokenizer

## 📋 How It Works

1. **Input Processing**: User enters a sequence of words
2. **Tokenization**: Text is converted to numerical sequences using the tokenizer
3. **Padding**: Sequences are padded to match the model's expected input shape
4. **Prediction**: LSTM model predicts the probability distribution for the next word
5. **Output**: The word with the highest probability is displayed to the user

## 🚀 Getting Started

### Prerequisites

- Python 3.7 or higher
- pip package manager

### Installation

1. Clone or download this project
2. Navigate to the project directory
3. Install dependencies:

```bash
pip install -r requirements.txt
```

### Usage

Run the Streamlit app:

```bash
streamlit run app.py
```

The application will open in your web browser at `http://localhost:8501`

**Example:**
- Enter: "To be or not to"
- Click "Predict Next Word"
- Get prediction: "be"

## 📁 Project Structure

```
├── app.py                                      # Streamlit web application
├── experiemnts.ipynb                           # Jupyter notebook with training code
├── hamlet.txt                                  # Training data (Shakespeare's Hamlet)
├── next_word_lstm.h5                           # First trained LSTM model
├── next_word_lstm_model_with_early_stopping.h5 # Optimized model with early stopping
├── tokenizer.pickle                            # Fitted tokenizer for text processing
├── requirements.txt                            # Python dependencies
└── README.md                                   # This file
```

## 📦 Requirements

- **tensorflow==2.15.0** - Deep learning framework
- **numpy** - Numerical computing
- **pandas** - Data manipulation
- **scikit-learn** - Machine learning utilities
- **matplotlib** - Data visualization
- **streamlit** - Web framework for ML apps
- **scikeras** - Scikit-learn API for Keras
- **tensorboard** - Visualization toolkit

## 🧠 Model Details

- **Architecture**: LSTM (Recurrent Neural Network)
- **Training Data**: Shakespeare's "Hamlet"
- **Training Method**: Keras sequential model
- **Optimization**: Early stopping to prevent overfitting
- **Input**: Sequence of tokens (padded to model's input length)
- **Output**: Probability distribution over vocabulary

## 📚 Key Components

### app.py
- Loads the pre-trained LSTM model
- Loads the tokenizer for text processing
- Provides `predict_next_word()` function
- Streamlit UI with text input and prediction button

### experiemnts.ipynb
- Contains the training pipeline
- Data preprocessing steps
- Model architecture and training code
- Model evaluation and analysis

### Tokenizer
The `tokenizer.pickle` file contains a fitted `Tokenizer` object that:
- Maps words to indices
- Converts text sequences to numerical format
- Used for both training and inference

## 🔄 Training Your Own Model

To train a new model, refer to `experiemnts.ipynb` which contains:
- Data loading and preprocessing
- Model architecture definition
- Training with early stopping
- Model evaluation

## 🤝 Contributing

Feel free to fork this project, improve the model, or add new features!

## 📝 License

See LICENSE file for details.

## ✨ Future Enhancements

- Add multi-word prediction
- Support for different text sources
- Model fine-tuning capabilities
- Advanced visualization of predictions
- Batch prediction functionality