# Tiny Transformer LLM

A minimal implementation of a transformer-based language model for character-level text generation. This project demonstrates the core concepts of transformer architecture in a simplified, educational format.

## Overview

This project implements a small-scale transformer model that:
- Extracts text from PDF documents using PyMuPDF
- Creates a character-level vocabulary and tokenizer
- Trains a tiny transformer model with attention mechanisms
- Generates text based on learned patterns

## Features

- **PDF Text Extraction**: Automatically extracts and processes text from PDF files
- **Character-Level Tokenization**: Creates vocabulary from unique characters in the text
- **Transformer Architecture**: Implements core transformer components including:
  - Multi-head attention
  - Positional encoding
  - Layer normalization
  - Feed-forward networks
- **Text Generation**: Generates new text sequences based on trained patterns

## Model Architecture

The `TinyTransformer` model includes:
- Embedding dimension: 32
- Number of attention heads: 2
- Hidden dimension: 64
- Number of layers: 2
- Sequence length: 32

## Requirements

```
torch
PyMuPDF (fitz)
```

## Usage

1. **Install Dependencies**:
   ```bash
   pip install PyMuPDF torch
   ```

2. **Prepare Your Data**:
   - Place your PDF file in the appropriate directory
   - Update the file path in the notebook

3. **Run the Notebook**:
   - Execute cells sequentially to:
     - Extract text from PDF
     - Create character vocabulary
     - Train the transformer model
     - Generate new text

4. **Text Generation**:
   ```python
   generated_text = generate(model, start_text="I", length=50)
   print(generated_text)
   ```

## Training

The model trains for 100 epochs using:
- Adam optimizer (learning rate: 1e-3)
- Cross-entropy loss
- Batch size: 4
- Sequence length: 32

Training progress is displayed every 10 epochs showing the loss reduction.

## Files

- `llm.ipynb`: Main Jupyter notebook containing the complete implementation
- `llm.pdf`: Source PDF document for text extraction (not included)

## Educational Purpose

This implementation is designed for learning and understanding transformer architectures. The model is intentionally small and simple to demonstrate core concepts without the complexity of large-scale models.

## Customization

You can modify various parameters:
- Model dimensions (embed_dim, num_heads, hidden_dim, num_layers)
- Training parameters (learning rate, epochs, batch size)
- Sequence length for different context windows
- Input text source (replace PDF with other text sources)

## License

This project is for educational purposes. Feel free to use and modify as needed.