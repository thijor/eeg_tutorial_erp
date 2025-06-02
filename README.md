# EEG tutorial

This repository contains a tutorial on ERP decoding and EEG-BIDS.

## Setup

1. Make a conda environment as follows:

```
conda create --name eeg_tutorial_erp python==3.12.4
```

2. Activate the `eeg_tutorial_erp` conda environment as follows:

```
conda activate eeg_tutorial_erp
```

3. Install the dependencies with the `requirements.txt` as follows:

```
pip install -r requirements.txt
```

4. Start Jupyter notebook:

```
jupyter notebook
```

## Dataset

This tutorial uses an open-access auditory oddball dataset, which can be downloaded from [Zenodo](https://zenodo.org/records/4066633). It is a curated subset of [Freiburg dataset](https://freidok.uni-freiburg.de/data/154576). Quoted from the full dataset description: 
`
This dataset contains multiple small trials of an auditory oddball paradigm. The paradigm presented two different sinusoidal tones. A low-pitched (500 Hz, 40 ms duration) non-target tone and a high-pitched (1000 Hz, 40 ms duration) target tone. Subjects were instructed to attend to the high-pitched target tones and ignore the low-pitched tones.
`

## Tutorial ERP

This tutorial, eeg_tutorial_erp.ipynb, will go through several steps along an ERP decoding pipeline, including:
1. Downloading and setting up EEG data
2. Loading and preprocessing ERP data
3. Basic ERP plots
4. Classification in the spatial domain for different time intervals
5. Classification in the temporal domain for different channels
6. Classification in the spatio-temporal domain
7. Permutation testing

The decoding is performed using a block-Toeplitz LDA, developed by [Sosulski and Tangermann 2022](https://iopscience.iop.org/article/10.1088/1741-2552/ac9c98/meta).

## Tutorial BIDS

This tutorial, eeg_tutorial_bids.ipynb, will go through several steps to make a datasets BIDS compliant, including:
1. Downloading and setting up EEG data
2. Making the dataset BIDS compliant and anonymized.

The BIDS pipeline makes use of [MNE-BIDS](https://mne.tools/mne-bids/stable/index.html).
