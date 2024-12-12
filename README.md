# SentimentAnalysisAudio

# Feature Extraction for Speech Emotion Recognition

This project focuses on extracting audio features for Speech Emotion Recognition (SER) using the `librosa` library in Python. The dataset comprises audio files, and features such as MFCC, ZCR, spectral roll-off, spectral flux, chroma features, and pitch are extracted for model training. 
The model is used to predict emotions.

---

## Table of Contents

1. [Project Description](#project-description)
2. [Features Extracted](#features-extracted)
3. [Requirements](#requirements)
4. [Usage](#usage)
5. [Output](#output)
6. [File Structure](#file-structure)
7. [License](#license)

---

## Project Description

Speech Emotion Recognition involves analyzing the emotional tone conveyed through audio. This project provides tools for preprocessing audio files and extracting relevant features necessary for training machine learning models.

---

## Features Extracted

The following features are extracted for each audio file:
- **MFCC (Mel-Frequency Cepstral Coefficients):** Represents the short-term power spectrum of sound.
- **ZCR (Zero Crossing Rate):** Measures the rate of sign changes in the waveform.
- **SRF (Spectral Roll-Off):** Frequency below which a specified percentage of the total spectral energy is contained.
- **Flux (Spectral Flux):** Measures the change in spectral content between consecutive frames.
- **Chroma Features:** Represents the intensity of the 12 different pitch classes.
- **Pitch:** The perceived frequency of the sound.

---

## Requirements

The project requires the following Python libraries:

- `librosa`
- `numpy`
- `pandas`
- `IPython`

Install the required packages using:
```bash
pip install librosa numpy pandas
```

---

## Usage

### 1. Run Feature Extraction
The feature extraction process involves:
1. Loading audio files.
2. Extracting features using the predefined feature extractor functions.

### 2. Save Features to CSV
Features and corresponding labels are saved to a CSV file for further use:
```python
df.to_csv('extracted_features.csv', index=False)
```

### 3. Download the CSV
For Kaggle or Jupyter Notebook environments, use:
```python
from IPython.display import FileLink
FileLink('extracted_features.csv')
```

### Example Notebook Workflow
The workflow is documented in the `CS412_final.ipynb` file, detailing step-by-step feature extraction and saving.

---

## Output

The main output is a CSV file containing extracted features and labels. Example format:
| MFCC  | ZCR  | SRF  | Flux  | Chroma  | Pitch  | Emotion |
|-------|------|------|-------|---------|--------|---------|
| [...] | 0.03 | 0.85 | 0.92  | [...]   | 220.5  | Happy   |

---

## File Structure

- **`CS412_final.ipynb`**: The main notebook containing code for feature extraction.
- **`extracted_features.csv`**: The generated CSV file with features and labels.
- **`Audio data model`**: thirdmodel.h5 is the model saved.
