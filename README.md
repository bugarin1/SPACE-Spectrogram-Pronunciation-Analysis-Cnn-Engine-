# SPACE: Spectrogram Pronunciation Analysis CNN Engine

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/[TU_USUARIO]/[NOMBRE_DEL_REPO]/blob/main/SPACE.ipynb)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![PyTorch](https://img.shields.io/badge/PyTorch-Deep%20Learning-ee4c2c)
![License](https://img.shields.io/badge/License-MIT-green)

An end-to-end Deep Learning system designed to recognize specific voice commands and provide a quantitative evaluation of pronunciation quality. This project bridges the gap between speech recognition and educational feedback using CNNs for classification and Dynamic Time Warping (DTW) for precise temporal alignment.


## Key Features

* **Real-time Audio Processing:** Captures and normalizes raw audio directly within the notebook.
* **Visual Feature Extraction:** Converts audio signals into Mel-frequency spectrograms to leverage Computer Vision techniques.
* **Deep Learning Classification:** Uses a custom Convolutional Neural Network (CNN) implemented in PyTorch to classify commands (e.g., 'house', 'right', 'go').
* **Pronunciation Scoring (DTW):** Aligns the user's speech with a "Golden Standard" reference using Dynamic Time Warping to calculate a similarity cost.
* **Visual Feedback:** Generates side-by-side spectrogram comparisons and highlights the least precise segments of the pronunciation.

## Tech Stack

* **Core:** Python, Jupyter Notebook (Google Colab)
* **Deep Learning:** PyTorch, Torchaudio
* **Signal Processing:** Librosa, SoX, SciPy
* **Algorithms:** fastdtw (for temporal alignment)
* **Visualization:** Matplotlib, IPython.display

## Methodology

The pipeline consists of four main stages:

1.  **Preprocessing:** Raw audio is resampled, trimmed for silence, and converted into log-mel spectrograms.
2.  **Model Training:** A CNN is trained on the SPEECHCOMMANDS dataset to learn high-level features of spoken words.
3.  **Alignment & Scoring:** When a user records audio, the system calculates the optimal alignment path against a reference sample.
4.  **Feedback:** The system outputs a percentage score and a visual path of the alignment errors.

## How to Run

Since this project is optimized for Google Colab, no local installation is required.

1.  Click the "Open in Colab" badge at the top of this README.
2.  Run the setup cells to install dependencies:
    ```bash
    !pip install torchaudio fastdtw
    !apt-get install sox libsox-fmt-all
    ```
3.  Execute the training cells (or load the pre-trained weights).
4.  Use the interactive recording widget to test your pronunciation.

## Repository Structure

* SPACE.ipynb: Main notebook containing the pipeline, model architecture, and interactive interface.
* requirements.txt: List of Python dependencies.
* README.md: Project documentation.

---

### Author
Developed by Jimena Bugarin.
Connect with me on [LinkedIn](https://www.linkedin.com/in/jimena-escobedo-bugarin-53aa453aa?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=ios_app)
