# Voice-Gender-Detection
This repository is about building a deep learning model using TensorFlow 2 to recognize gender of a given speaker's audio.

# requirments
tensorflow
scikit-learn
numpy
pandas
tqdm
pyaudio
librosa

# Dataset used

[Mozilla's Common Voice](https://www.kaggle.com/mozillaorg/common-voice)

If you wish to download the dataset and extract the features files (.npy files) on your own, [`preparation.py`](preparation.py) is the responsible script for that, once you unzip it, put `preparation.py` in the root directory of the dataset and run it. 

This will take sometime to extract features from the audio files and generate new .csv files.

# Training
You can customize your model in [`utils.py`](utils.py) file under the `create_model()` function and then run:

    python train.py

# Testing

[`test.py`](test.py) is the code responsible for testing your audio files or your voice:

    python test.py 
