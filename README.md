# Mental imagery, gesture classification

## Introduction

The code in this repository will analyze EEG data and try different classification methods to classify it as one of three possible actions a subject was imagining in each point in time:

- The subject was imagining repetitive movements of the left hand. Class 2.
- The subject was imagining repetitive movements of the right hand. Class 3.
- The subject was thinking of words starting with the same random character. Class 7.


## Dataset

The dataset I used is originally part of _Data V_ in **Brain Computer Interface Competition III**. Information about this challenge can be found [here](http://www.bbci.de/competition/iii/desc_V.html). To download the dataset, you need to sign up with your name and email address [here](http://www.bbci.de/competition/iii/#download).

Once the dataset is downloaded, place them in the folder where you'll run this script from. The folder structure will be the following:

- `data_psd`:
`train_subject1_psd01.asc`,`train_subject1_psd02.asc`,`train_subject1_psd03.asc`,`train_subject2_psd01.asc`,`train_subject2_psd02.asc`,`train_subject2_psd03.asc`,`train_subject3_psd01.asc`,`train_subject3_psd02.asc`,`train_subject3_psd03.asc`

- `subject1`:
`train_subject1_raw01.asc`,`train_subject1_raw02.asc`,`train_subject1_raw03.asc`

- `subject2`:
`train_subject2_raw01.asc`,`train_subject2_raw02.asc`,`train_subject2_raw03.asc`

- `subject3`:
`train_subject3_raw01.asc`,`train_subject3_raw02.asc`,`train_subject3_raw03.asc`


## Results

We evaluate both linear and non-linear methods. The current state-of-the-art achieved and accuracy of 62.87% for raw data and 68.64% for processed data. More information about the state-of-the-art can be found here: [http://www.bbci.de/competition/iii/results/](http://www.bbci.de/competition/iii/results/)  in the section for _Dataset V_.

Using the script in this repository with the raw data, we can see an accuracy of **95.53%** with KNN (linear methods), **98.75%** with RBFKernel (non-linear methods) and **98.65%** with Random Forest (non-linear method).
