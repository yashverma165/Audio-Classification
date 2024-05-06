# Audio-Classification

### DESCRIPTION
This dataset contains 8732 labeled sound excerpts (<=4s) of urban sounds from 10 classes: air_conditioner, car_horn, children_playing, dog_bark, drilling, enginge_idling, gun_shot, jackhammer, siren, and street_music. The classes are drawn from the urban sound taxonomy. For a detailed description of the dataset and how it was compiled please refer to our paper.
All excerpts are taken from field recordings uploaded to www.freesound.org. The files are pre-sorted into ten folds (folders named fold1-fold10) to help in the reproduction of and comparison with the automatic classification results reported in the article above.

In addition to the sound excerpts, a CSV file containing metadata about each excerpt is also provided.

### AUDIO FILES INCLUDED
8732 audio files of urban sounds (see description above) in WAV format. The sampling rate, bit depth, and number of channels are the same as those of the original file uploaded to Freesound (and hence may vary from file to file).

### META-DATA FILES INCLUDED
UrbanSound8k.csv

This file contains meta-data information about every audio file in the dataset. This includes:

* slice_file_name: 
The name of the audio file. The name takes the following format: [fsID]-[classID]-[occurrenceID]-[sliceID].wav, where:
[fsID] = the Freesound ID of the recording from which this excerpt (slice) is taken
[classID] = a numeric identifier of the sound class (see description of classID below for further details)
[occurrenceID] = a numeric identifier to distinguish different occurrences of the sound within the original recording
[sliceID] = a numeric identifier to distinguish different slices taken from the same occurrence

* fsID:
The Freesound ID of the recording from which this excerpt (slice) is taken

* start
The start time of the slice in the original Freesound recording

* end:
The end time of slice in the original Freesound recording

* salience:
A (subjective) salience rating of the sound. 1 = foreground, 2 = background.

* fold:
The fold number (1-10) to which this file has been allocated.

* classID:
A numeric identifier of the sound class:
0 = air_conditioner
1 = car_horn
2 = children_playing
3 = dog_bark
4 = drilling
5 = engine_idling
6 = gun_shot
7 = jackhammer
8 = siren
9 = street_music

* class:
The class name: air_conditioner, car_horn, children_playing, dog_bark, drilling, engine_idling, gun_shot, jackhammer, 
siren, street_music.

Dataset-https://urbansounddataset.weebly.com/download-urbansound8k.html

## objective
In this project, I use UrbanSound8K Dataset preprocess it using Mel Frequency Cepstral Coefficients (MFCC) then Train using Deep learning Model and Predict it.


1. Load Data
   * Using Librosa.load
   * Visualize Data 
3. Feature Extraction
   * Mel Frequency Cepstral Coefficients (MFCC)
4. data Prepration
   * Create DataFrame of these features and classes
   * LabelEncode Y (classes)
   * Train Test Split
9. Train Model
   * Create Deep Learning Model
   * Training Model and save Best Model weights
   * Predict Accuracy
11. Test Model
    * Preprocess the new audio data using mfcc
    * Predict the classes
    * Inverse trasform the Predictied class label
## Conclusion 
* Accurcay - 77%
   
