# Urban Sound Classification

#### The objective of this project is to perform urban sound classification using neural networks. 

### Dataset

[The UrbanSound8K dataset](https://urbansounddataset.weebly.com/urbansound8k.html) contains 8732 sound excerpts of urban sounds in WAV format from 10 classes: air conditioner, car horn, children playing, dog bark, drilling, enginge idling, gun shot, jackhammer, siren, and street music. 

Librosa library is used for data preprocessing and feature extraction.

### Project structure

#### 1. Dataset Import and Exploratory analysis

Code is implemented using [Feature_Extraction Google colab notebook](https://github.com/angelinakhatiwada/Urban-Sound-Classification/blob/main/Feature_Extraction.ipynb).

- Dataset import
- Classes distribution analysis
- Audio duration analysis

#### 2. Feature Extraction (for an example file and entire dataset):

Code is implemented using [Feature_Extraction Google colab notebook](https://github.com/angelinakhatiwada/Urban-Sound-Classification/blob/main/Feature_Extraction.ipynb).

- Melspectrogram (statistics): 128 x 4
- Melspectrogram, MFCCs, Chromagram (statistics): 40 x 4 x 3
- Melspectrogram (time features): 40 x 64

All the features extracted are saved as pickle files and stored in the [data folder](https://github.com/angelinakhatiwada/Urban-Sound-Classification/tree/main/data).

#### 3. Classification models:

Code is implemented separately for different features:
- [FNN_RNN_CNN_Mels_(512) Google Colab notebook](https://github.com/angelinakhatiwada/Urban-Sound-Classification/blob/main/FNN_RNN_CNN_Mels_(512).ipynb)
- [FNN_RNN_CNN_Mels_MFCCs_Chroma_(480) Google Colab notebook](https://github.com/angelinakhatiwada/Urban-Sound-Classification/blob/main/FNN_RNN_CNN_Mels_MFCCs_Chroma_(480).ipynb)
- [FNN_RNN_CNN_Mels_(40_64) Google Colab notebook](https://github.com/angelinakhatiwada/Urban-Sound-Classification/blob/main/FNN_RNN_CNN_Mels_(40_64).ipynb)

**Feedforward Neural Network**

![FNN_new](https://user-images.githubusercontent.com/60095044/148851573-85afc5c8-c951-4d72-9b26-f7ff2132d374.png)

**Recurrent Neural Network (LSTM)**

![RNN](https://user-images.githubusercontent.com/60095044/148851703-c897e6c7-956a-488d-915a-59818d1bab06.png)

**Convolutional Neural Network**

![CNN](https://user-images.githubusercontent.com/60095044/148851733-006c1559-924e-45f8-8d3f-b989f790f908.png)

**Best average accuracy scores across test sets:**

- Mel spectrogram, MFCCs and Chroma features (statistics) + CNN: **0.64**
- Mel spectrogram, MFCCs and Chroma features (statistics) + FNN: **0.62**
- Mel spectrogram features (statistics) + CNN: **0.57**
