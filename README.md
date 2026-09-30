# IMDB Review Sentiment Analyzer

This project is a small Streamlit web app that classifies a movie review as positive or negative using a pre-trained Simple RNN model trained on the IMDB movie review dataset.

## What it does

- Accepts a review as free text
- Preprocesses the input using the IMDB word index
- Pads the review to the model's required length
- Uses a loaded Keras model to predict sentiment
- Displays:
  - the sentiment label (`Positive` or `Negative`)
  - the raw prediction score

## Project structure

- `main.py` — Streamlit app entry point
- `simple_rnn_imdb.h5` — pre-trained sentiment model
- `simplernn.ipynb` — notebook with model training/experimentation
- `prediction.ipynb` — notebook for predictions and exploration
- `requirements.txt` — Python dependencies

## Tech stack

- Python
- TensorFlow / Keras
- NumPy
- Streamlit
- scikit-learn
- pandas
- matplotlib

## Setup

1. Create and activate a virtual environment:

```bash
python -m venv .venv
source .venv/bin/activate
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Run the app:

```bash
streamlit run main.py
```

4. Open the local URL shown by Streamlit in your browser, then type a movie review and click the classification button.

## Notes

- The model uses the IMDB vocabulary and expects reviews to be encoded in the same way the training data was prepared.
- The app is designed to work with the included `simple_rnn_imdb.h5` file.
- If the model file is missing, retraining is required through the notebook workflow or by re-creating the model.

## Example use

Example input:

```text
This movie was absolutely amazing. The acting was brilliant and the story was engaging from start to finish.
```

Expected result:

- Sentiment: `Positive`
- Prediction score: close to `1.0`

## License

This project is intended for learning and personal experimentation.
