# Tracking and Data Analysis of Single Amyloid Fibrils in a Thermophoretic Trap

## Content

- [Discription](#discription)
- [Repository Contents](#repository-contents)
- [System Requirements](#system-requirements)
- [Installation Guide](#installation-guide)
- [Instructions for Use](#instructions-for-use)
- [Notebooks](#Notebooks)
- [License](./LICENSE)


## Discription

This repository provides a framework for the tracking and the data analysis of single amyloid fibrils in a thermophoretic trap. 
Within the framework the [TrackerLab](./TrackerLab) implements a GUI for the image processing and tracking of single amyloid fibrils. 
The directory [Notebooks](./Notebooks) contains a collection of Jupyter Notebooks for the data analysis.  

## Repository Content

- [TrackerLab](./TrackerLab): A graphical user interface for the tracking of single amyloid fibrils based on the PyQt and PyQtGraph libary.
- [Notebooks](./Notebooks): Collection of Juypter Notebooks for the data analysis.
- [COMSOL](./COMSOL): The COMSOL file for the temperature simulation.


## System Requirements

### Hardware Requirements

The framework requires a standard computer with about 2 GB of RAM.

### Software Requirements

The software is supported for Windows, Mac OS and Linux. The software has been tested on the following systems:

Windows: 10  
Mac OS: 10.12  
Linux:   

## Installation Guide

The software requires the [Anaconda](https://www.anaconda.com/download/) framework with Python 3.* to be installed. 

### Required Packages:

The following packages are required:

- nptdms
- pyqtgraph

The typical the install time, including all packages, does not exceed 30 minutes.

## Instructions for Use

To start the TrackerLab run the script: TrackerLab.py  
With all required packages installed properly you should see a GUI with most of the controls disabled.
To open a video file click the `Open...` button and located the `Set1_001_video.tdms` from the sample dataset.

![Screenshot](https://github.com/MolecularNanophotonics/TTT/blob/master/Images/Screenshot.PNG)

The `*video.tdms` files are TDMS files recored with LabVIEW containing the image series and metadata such as the binning and the exposure time.
Beside these TDMS files the software also supports stacked TIFF files for general use.  
  
In the pre-processing panel a media filter and a circular mask can be applied to the image.
In the tracking tab the parameters for the connected-componente labeling can be adjusted.
To run the tracking algorithm for all frames and selected files click the `Batch` button. The tracking data will be stored as dataframe in a HDF5 or CSV file depending on the selected `Settings`. The dataframe has the following structure:  

x | y | area
1 | 2 | 3

center of mass x and y positions, the area of , the maximum pixel 
Typically, the processing of 1000 frames takes about 10 s.


## Notebooks

...
