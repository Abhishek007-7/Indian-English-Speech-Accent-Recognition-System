# Indian English Speech Accent Recognition System

This repository contains the implementation of an Indian English Speech Accent Recognition System, which uses machine learning and deep learning techniques to classify accents based on regional variations in spoken English across India.

## Project Overview

The goal of this project is to enhance the adaptability and inclusivity of speech recognition systems by accurately identifying regional accents in Indian English. This system can be integrated into Automatic Speech Recognition (ASR) tools to improve performance and usability for users with diverse linguistic backgrounds.
Developed a regional accent detection system using Indic TTS dataset with MFCC features and models like SVM, Random Forest, CNN, and LSTM. Achieved robust performance across 16 Indian accents using stratified 10-fold cross-validation, optimizing accuracy, precision, recall, and F1 score.

## Dataset

The dataset used for this project is the **Indic TTS** database, developed by IIT Madras. It is a comprehensive dataset designed to support speech-related research, including:

- High-quality audio samples recorded by male and female speakers.
- Representation of accents from the following Indian languages:
  - **Bengali**
  - **Gujarati**
  - **Kannada**
  - **Malayalam**
  - **Marathi**
  - **Rajasthani**
  - **Telugu**

The dataset can be downloaded from the [Indic TTS website](https://www.iitm.ac.in/donlab/indictts/database).

### Data Composition
- **Number of Speakers**: Both male and female speakers are equally represented.
- **Audio Quality**:
  - Uniform length of 10 seconds per clip.
  - Sampling rate resampled to 16 kHz.
- **Data Split**:
  - **Training**: 70%
  - **Testing**: 20%
  - **Validation**: 10%

## Features

The system uses the following features extracted from audio:
- **Mel-Frequency Cepstral Coefficients (MFCCs)**: Capture phonetic details.
- **Chroma Features**: Represent harmonic content.
- **Spectral Contrast**: Highlight energy variations across frequencies.

## Models

The following machine learning and deep learning models were used:
- **Support Vector Machine (SVM)**
- **Logistic Regression**
- **Random Forest**
- **XGBoost**
- **Decision Trees**
- **CNN-LSTM**

### Best Performing Model
- **XGBoost** achieved the highest accuracy of **99.02%**, followed by **CNN-LSTM** with **98.70%**.

## Methodology

1. **Data Preprocessing**:
   - Noise reduction, normalization, and signal conditioning.
   - Standardization of audio to uniform duration and sampling rate.
   - Data augmentation (e.g., pitch shifting, speed variation, noise addition).

2. **Feature Extraction**:
   - Extracted MFCC, Chroma, and Spectral Contrast features using the Librosa library.

3. **Model Training and Evaluation**:
   - Models were trained using stratified K-fold cross-validation.
   - Evaluated on metrics like accuracy, precision, recall, and F1 score.

4. **Interface**:
   - A user-friendly GUI developed with Tkinter allows real-time predictions by uploading audio files.

## Results

| Model               | Accuracy (%) |
|---------------------|--------------|
| XGBoost            | 99.02        |
| CNN-LSTM           | 98.70        |
| Random Forest       | 98.86        |
| Logistic Regression | 97.95        |
| SVM                 | 95.89        |
| Decision Tree       | 94.65        |

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/indian-accent-recognition.git
   ```
2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Download the dataset from the [Indic TTS website](https://www.iitm.ac.in/donlab/indictts/database).
4. Preprocess the dataset using the scripts provided in the repository.

## Usage

Run the GUI for real-time accent predictions:
```bash
python app.py
```

## Future Scope

- Extend the dataset to include more accents and dialects.
- Integrate advanced deep learning architectures like transformers.
- Explore real-time accent recognition in noisy environments.
- Develop models to handle multilingual and code-switched speech.

## Contributors

- **Abhishek M.V**  
- **A. Jaya Sreekar**  
- **Mohith D.M**

## Acknowledgments

This project was conducted as part of the B.Tech program at Amrita School of Engineering, Bengaluru, under the guidance of **Dr. Susmitha Vekkot** and **Dr. T.K. Ramesh**.
