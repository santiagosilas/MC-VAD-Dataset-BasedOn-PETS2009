# Multi-Camera Video Anomaly Detection Dataset Based on PETS 2009 Benchmark Dataset

This repository contains a preprocessed multi-camera dataset for multi-camera video anomaly detection task. The dataset consists of 4 overlapped camera video scenes.

## Dataset Description
The dataset is provided in .npy format (numpy version: 1.24.3). Each .npy file contains a list of video scenes for a single camera video.

## Dataset Contents
The repository contains the following files:
- Training splits for each camera:
    - pets2009-comb-train-view-001.npy
    - pets2009-comb-train-view-002.npy
    - pets2009-comb-train-view-003.npy
    - pets2009-comb-train-view-004.npy
- Test Splits for each camera:
    - pets2009-comb-test-view-001.npy
    - pets2009-comb-test-view-002.npy
    - pets2009-comb-test-view-003.npy
    - pets2009-comb-test-view-004.npy

- DATA-LOADING.ipynb: A jupyter notebook providing a demonstration on how to load and process the dataset.

## Dataset Structure

The data in each .npy file is organized as a list of dictionary objects, where each object represents a video scene. Each object contains the following properties:

- **name**: A string representing the name of the video scene;
- **X_i**:  Each video of each camera corresponds to a matrix with dimension $n$ x $2048$, where $n$ is a variable number of existing clips and the number of attributes is $1024$ - $1024$ Inflated 3D (i3D) deep features for appearance - RGB for each clip in the video);
- **y_i**: the category of video scene ($0.0$ or $1.0$);
- **y_fi**: A matrix $n$ x $16$ representing the frame labels.


## Citation
If you use this dataset in your research or project, please cite it as:


```
@article{pereira2023mcmil,
  title={An Approach to Multi-camera Multi-Instance Anomaly Detection in Video Surveillance},
  author={Pereira, Silas Santiago L and Maia, Jos{\'e} Everardo Bessa},
  journal={arXiv preprint arXiv:1234.12345},
  year={2023}
}
```
