This project uses python 2.7

The aim of this project is to classify heartbeats into four categories: normal,
murmur, extra heart sound and artifact.

Two datasources will be used to solve this classification problem.

The first comes from the
[2016 PhysioNet/CinC Challenge](https://physionet.org/challenge/2016). The data
can be found
[here](https://physionet.org/physiobank/database/challenge/2016/training.zip) .

The second source comes from
[Kaggle](https://www.kaggle.com/kinguistics/heartbeat-sounds). The data can be
found [here](https://www.kaggle.com/kinguistics/heartbeat-sounds/data). This
dataset is too small so the first dataset will be used to train a more
generalize model. This model will only classify between normal and abnormal
heartbeats. From the knowledge learned from this model a more specialized model
will be trained to classify between normal, murmur, extra heart sound and
artifact heartbeats.

The following folder structure has to be followed to have the same results and
for the methods in the notebooks to work properly.

data/

    physionet/
        reduced_features/
        training-a/
        training-b/
        ...
        training-f/

    kaggle/
        reduced_features/
        set_a.csv
        set_a/

---

This project will consist of several notebooks

**WB1-explore.ipynb**

* This notebook contains code to visualize audio files
* Explores the Physionet and Kaggle datasets

**WB2-FNN.ipynb**

* This notebook implements a Feed Forward Network for the PhysioNet dataset

**WB3-CNN.ipynb**

* This notebook implements a Convolutional Neural Network for the PhysioNet
  dataset

**WB4-Transer Learning.ipynb**

* This notebook implements the methods applied for feature extraction in WB2 and
  WB3 and compares the results to model that uses transfer learning to be used
  with the Kaggle dataset
