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



https://github.com/bhaktiekhande/Voice-Gender-Detection/assets/120095410/8fb214ea-be8b-49d0-bb98-c82aad4f092a


    

# Testing

[`test.py`](test.py) is the code responsible for testing your audio files or your voice:

    python test.py 




https://github.com/bhaktiekhande/Voice-Gender-Detection/assets/120095410/cb5129b3-6d2c-451f-ad3d-abaae9337ef8







# **Output:**

    usage: test.py [-h] [-f FILE]

    Gender recognition script, this will load the model you trained, and perform
    inference on a sample you provide (either using your voice or a file)

    optional arguments:
    -h, --help            show this help message and exit
    -f FILE, --file FILE  The path to the file, preferred to be in WAV format

- For instance, to get gender of the file `test-samples/27-124992-0002.wav`, you can:

      python test.py --file "test-samples/27-124992-0002.wav"

    **Output:**

      Result: male
      Probabilities:     Male: 96.36%    Female: 3.64%    
