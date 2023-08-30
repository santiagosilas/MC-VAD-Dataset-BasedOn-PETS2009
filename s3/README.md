# Multi-Camera Video Anomaly Detection Dataset Based S3 Event Recognition Sequences on PETS 2009 Benchmark Dataset


This repository contains a preprocessed multi-camera dataset for multi-camera video anomaly detection task. The dataset consists of 4 overlapped camera video scenes.

We labeled the anomalous videos acording to the study in Rezaei and Yazdi (2021) "Real-time crowd behavior recognition in surveillance videos based on deep learning methods". Additionally, we also insert normal videos available in the S0, S1 and S2 sequences of the PETS 2009 dataset. 

## Dataset Description
The dataset is provided in .npy format (numpy version: 1.24.3). Each .npy file contains a list of video scenes for a single camera video.

## Dataset Contents
The repository contains the following files:
- Training splits for each camera:
    - S1.L2-walking--Time-14-31
    - S1.L1-walking--Time-13-59
    - Regular-Flow--Time-13-59
    - S3-Multiple-Flows--Time-14-37
    - Regular-Flow--Time-13-57
    - Background-Set--Time-13-06
    - Regular-Flow--Time-14-03
    - Background-Set--Time-13-38
    - Regular-Flow--Time-14-06
    - S3-Event-Recognition--Time-14-31
    - S3-Event-Recognition--Time-14-16a
    - S3-Event-Recognition--Time-14-27a
    - S3-Event-Recognition--Time-14-16b
- Test Splits for each camera:
    - City-Center--Time-12-34
    - Regular-Flow--Time-14-29
    - S1.L1-walking--Time-13-57
    - S2.L2-walking--Time-14-55
    - S1.L2-walking--Time-14-06
    - City-Center--Time-14-55
    - S2.L3-walking--Time-14-41
    - Background-Set--Time-13-32
    - Background-Set--Time-13-19
    - S3-Event-Recognition--Time-14-27b
    - S3-Event-Recognition--Time-14-33a
    - S3-Event-Recognition--Time-14-33b

- DATA-LOADING.ipynb: A jupyter notebook providing a demonstration on how to load and process the dataset.

## Dataset Structure

The data in each .npy file is organized as a list of dictionary objects, where each object represents a video scene. Each object contains the following properties:

- **name**: A string representing the name of the video scene;
- **X_i**:  Each video of each camera corresponds to a matrix with dimension $n$ x $2048$, where $n$ is a variable number of existing clips and the number of attributes is $1024$ - $1024$ Inflated 3D (i3D) deep features for appearance - RGB for each clip in the video);
- **y_i**: the category of video scene ($0.0$ or $1.0$);
- **y_fi**: A matrix $n$ x $16$ representing the frame labels.