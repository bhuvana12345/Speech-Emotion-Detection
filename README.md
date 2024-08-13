# **Speech Emotion Recognition (SER)**

## **Introduction**
Speech is the most natural form of communication in humans, conveying a wealth of information including action, emotion, age, gender, and other unique attributes. As the world becomes increasingly digital, human-computer interaction (HCI) plays a vital role in various fields. Among the different ways to interact with machines, such as gestures, body language, and speech, speech stands out as a unique signal with multiple attributes that can establish a connection with machines.

Speech Emotion Recognition (SER) is a subfield of speech recognition that focuses on identifying the emotional state of a human based on their speech signal. SER has significant applications in HCI, including IoT, customer call dialogues, psychological analysis, and medical applications. Despite its potential, recognizing speech emotion remains a challenging task due to the variability in human speech caused by differences in language, culture, and locality. Emotional states are typically categorized into discrete variables such as happy, calm, disgust, fear, sad, angry, and surprised, which facilitates easier classification compared to continuous variables.

SER mainly involves two phases: extracting features relevant for classification and classifying those features using conventional or learning-based algorithms. Commonly used time-domain features include mean, root mean square value, and energy, while frequency-domain features include spectrograms and Mel-frequency cepstral coefficients (MFCCs). MFCCs, which represent the spectral energy in different frequency ranges, are widely used in SER.

## **Problem Statement**
Speech Emotion Recognition is crucial for enhancing HCI, but it poses significant challenges, especially in complex environmental situations involving inter-speaker differences. However, with advancements in deep learning, these challenges are being addressed more effectively than with conventional methods. This project aims to classify emotional states accurately using convolutional neural networks (CNNs) on the RAVDESS dataset, which contains audio samples labeled with eight emotional states.

## **Data Description**

### **Ryerson Audio-Visual Database of Emotional Speech and Song (RAVDESS) Dataset**
The RAVDESS dataset is a comprehensive audio-visual database containing 7,356 clips, with modalities including audio-visual (av), audio-only (ao), and video-only (vo) recordings. The dataset was recorded in a standardized setting by 24 actors (12 male and 12 female) and includes labels for emotional state, modality, and other factors.

### **Filename Convention**
Each RAVDESS file is named following a specific pattern, consisting of seven two-digit numerical identifiers separated by hyphens (e.g., `03-01-03-02-01-01-10.wav`). These identifiers describe various experimental factors such as modality, emotion, intensity, and actor.

For example, the filename `03-01-03-02-01-01-10.wav` refers to:
- **03** - Audio-only
- **01** - Speech
- **03** - Happy
- **02** - Strong intensity
- **01** - Statement "Kids are talking by the door"
- **01** - First repetition
- **10** - Tenth actor

Odd-numbered actors are male, and even-numbered actors are female.

### **Factor-Level Coding**
- **Modality**: `01` = Audio-video, `02` = Video-only, `03` = Audio-only
- **Channel**: `01` = Speech, `02` = Song
- **Emotion**: `01` = Neutral, `02` = Calm, `03` = Happy, `04` = Sad, `05` = Angry, `06` = Fearful, `07` = Disgust, `08` = Surprised
- **Intensity**: `01` = Normal, `02` = Strong
- **Statement**: `01` = "Kids are talking by the door", `02` = "Dogs are sitting by the door"
- **Repetition**: `01` = First repetition, `02` = Second repetition
- **Actor**: `01` = First actor, …, `24` = Twenty-fourth actor

## **Algorithms and Future Work**
This project utilizes CNNs for emotion classification. However, other algorithms such as Recurrent Neural Networks (RNNs), Long Short-Term Memory (LSTM), or Transformer models can also be explored to improve the performance of SER. Future work may involve experimenting with these algorithms, optimizing feature extraction methods, and expanding the dataset to include more diverse emotional states.
