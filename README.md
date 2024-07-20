# PoeticTextGenerator
A Recurrent Neural Network (RNN) based project to generate Shakespearean poetic text using TensorFlow and Google Colab.


# Shakespearean Poetic Text Generator

This repository contains a project that uses Recurrent Neural Networks (RNNs) to generate poetic text similar to the works of William Shakespeare. The project is implemented using TensorFlow and is designed to run in Google Colab for ease of use.

## Project Overview

The goal of this project is to create a text generator that can produce text in the style of Shakespeare. By training an RNN on the text of Shakespeare's plays, we can generate new text that mimics his unique style and language.

## Features

- **Text Loading and Preprocessing**: Downloads and processes the complete works of Shakespeare.
- **Data Preparation**: Converts text into numerical format, creates input-target pairs, and prepares the dataset for training.
- **Model Building**: Constructs an RNN model using TensorFlow with an embedding layer, GRU layer, and a dense output layer.
- **Training**: Trains the model on the prepared dataset, with checkpoints to save progress.
- **Text Generation**: Generates text using the trained model, with adjustable temperature for diversity.

## Usage

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/poetic-text-generator.git
   cd poetic-text-generator
   ```

2. **Run in Google Colab**:
   - Open the `poetic_text_generator.ipynb` notebook in Google Colab.
   - Follow the instructions in the notebook to run the code cells.

## Dependencies

- TensorFlow
- NumPy
- Google Colab (recommended)

## How It Works

### 1. Loading Shakespeare Texts
The script downloads the Shakespeare dataset, reads it into memory and prints the length of the text and the first 250 characters for inspection.

### 2. Preparing Data
The text is processed to create a set of unique characters and mappings from characters to indices. The text is then converted into an integer representation and input-target pairs are created for training.

### 3. Building Recurrent Neural Network
An RNN model is built with an embedding layer to convert integer representations into dense vectors, a GRU (Gated Recurrent Unit) layer with 1024 units, for capturing long-term temporal dependencies and a dense output layer to predict the next character in the sequence.

### 4. Training the Model
The model is compiled with an Adam optimizer and a sparse categorical cross-entropy loss function. It is trained for a specified number of epochs with checkpoints to save the model weights.

### 5. Text Generation
A function is defined to generate text from the trained model. By providing a start string and a temperature value, the model generates new text in the style of Shakespeare. Lower temperatures result in more predictable text, while higher temperatures produce more creative text.



## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests with improvements or bug fixes.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgements

- This project uses the [Shakespeare dataset](https://storage.googleapis.com/download.tensorflow.org/data/shakespeare.txt) provided by TensorFlow.

## Contact

For any questions or inquiries, please contact [chandaarkapriya@gmail.com].
