# Hindi-English Translation Using Transformers

## Dataset

The dataset used in this project is the Hindi-English parallel corpus, which can be downloaded from Kaggle. Ensure the dataset is saved in a CSV file with columns for English and Hindi sentences.

## Preprocessing

1. **Read the Dataset:** Load the dataset using pandas.
2. **Filter and Sample:** Filter the dataset to include only the required source and sample 25,000 sentences.
3. **Text Preprocessing:** Convert all text to lowercase, remove quotes, special characters, numbers, and extra spaces.
4. **Tokenization:** Add start and end tokens to target sequences, create vocabularies for English and Hindi, and map words to indices.

## Model Architecture

The model consists of the following components:

1. **Embedding Layer:** Converts words to embedding vectors.
2. **Positional Encoding:** Adds positional information to embeddings.
3. **Multi-Head Attention:** Implements attention mechanism with multiple heads.
4. **Transformer Block:** Combines multi-head attention and feed-forward layers with normalization and dropout.
5. **Encoder:** Applies multiple transformer blocks to encode the input sequence.
6. **Decoder:** Applies multiple transformer blocks to decode the encoded sequence.

## Training

1. **Split the Data:** Split the dataset into training and testing sets.
2. **Define the Model:** Instantiate the Transformer model with appropriate parameters.
3. **Loss Function and Optimizer:** Use cross-entropy loss and Adam optimizer.
4. **Training Loop:** Train the model over multiple epochs, evaluating performance on the validation set.

## Inference

1. **Encode Input Sequence:** Pass the input sequence through the encoder.
2. **Decode Output Sequence:** Generate the output sequence one token at a time using the decoder.
3. **Convert Indices to Words:** Map output indices to words using the reverse vocabulary.

## Evaluation

Evaluate the model's performance using the BLEU score, which measures the similarity between the predicted and reference translations.

## Results

Example inference:
- **BLEU Score:** 0.6687

