# DeepUS_ABLE
Reproduction of ABLE (Adpative Ultrasound Beamforming by deep LEarning) beamforming model

## Inputs & Targets and Tests
Inputs&Targets and Tests will be in google drive : https://drive.google.com/drive/folders/1memUwBfTUUB3UWpM331azTBkBOTfxrRF （they have not been uploaded yet).

All of the datasets is in **.mat** format which overall occupy over 1.2 GB space, that is too large to upload.


## Model
(Start on 16 April 2021)

**version1.5_part1.ipynb** is used to Build and Train the ABLE model with PICMUS16 datasets

**version1.5_part2.ipynb** is used to Test the saved ABLE model with PICMUS17 datasets

## Notes
Each original PICMUS16 dataset contains 75 angles' frames, which help to build Targets (DAS with 75 angles). However, when these datasets are used as Inputs, only angle==0.0 is condidered.

Each PICMUS17 dataset just has data with angle==0.0, so just let them to be Tests.



