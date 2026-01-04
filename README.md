Speech Emotion Recognition

Speech Emotion Recognition (SER) is the process of identifying human emotions from speech signals. Human voice carries emotional information through pitch, tone, speed, and energy, and this project uses those characteristics to classify emotions from audio recordings using deep learning.

In this project, a speech emotion detection model is built to recognize emotions such as angry, calm, disgust, fear, happy, neutral, sad, and surprise. The goal is to automatically predict the emotional state of a speaker using only their voice.

The model is trained using four well-known emotion speech datasets: RAVDESS, CREMA-D, TESS, and SAVEE. Audio samples from these datasets are first explored and visualized using waveplots and spectrograms to understand how emotions differ in terms of loudness and frequency patterns.

Since raw audio cannot be directly used for training, several audio features are extracted using the Librosa library. These include Zero Crossing Rate, Chroma STFT, MFCC, RMS energy, and Mel Spectrogram features. To improve model performance and reduce overfitting, data augmentation techniques such as noise addition, time stretching, and pitch shifting are applied.

The extracted features are normalized and fed into a 1D Convolutional Neural Network built using Keras. The model learns temporal patterns in the audio features and predicts one of the eight emotion classes using a softmax output layer.

After training for 50 epochs, the model achieves around 61% accuracy on the test dataset. The model performs better on emotions like surprise and angry, which have more distinct vocal characteristics, while emotions with similar speech patterns show some overlap.

This project demonstrates a complete end-to-end pipeline for speech emotion recognition, including data preparation, feature extraction, deep learning modeling, and evaluation. The results can be further improved by using more advanced models, better feature selection, or additional data augmentation techniques.
