# Urban Sound Classification

#### The objective of this project is to perform urban sound classification using neural networks. 

### Dataset

[The UrbanSound8K dataset](https://urbansounddataset.weebly.com/urbansound8k.html) contains 8732 sound excerpts of urban sounds in WAV format from 10 classes: air conditioner, car horn, children playing, dog bark, drilling, enginge idling, gun shot, jackhammer, siren, and street music. 

### Project structure

#### 1. Dataset Import and Exploratory analysis

Code is implemented using [Feature_Extraction Google colab notebook](https://github.com/angelinakhatiwada/Urban-Sound-Classification/blob/main/Feature_Extraction.ipynb).

- Dataset import
- Classes distribution analysis
- Audio duration analysis

**2. Feature Extraction (for an example file and entire dataset):**

Code is implemented using [Feature_Extraction Google colab notebook](https://github.com/angelinakhatiwada/Urban-Sound-Classification/blob/main/Feature_Extraction.ipynb).

- Melspectrogram (statistics): 128 x 4
- Melspectrogram, MFCCs, Chromagram (statistics): 40 x 4 x 3
- Melspectrogram (time features): 40 x 64

All the features extracted are saved as the pickle files and stored in the [data folder](https://github.com/angelinakhatiwada/Urban-Sound-Classification/tree/main/data).
