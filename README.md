# DeepUS_ABLE
Reproduction of ABLE (Adpative Ultrasound Beamforming by deep LEarning) beamforming model

## Inputs & Targets and Tests
Inputs&Targets and Tests will be in google drive : https://drive.google.com/drive/folders/1memUwBfTUUB3UWpM331azTBkBOTfxrRF （they have not been uploaded yet).

All of the datasets is in **.mat** format which overall occupy over 1.2 GB space, that is too large to upload.


## Model

**xxx_part1.ipynb** is used to Build and Train the ABLE model with PICMUS16 datasets

**xxx_part2.ipynb** is used to Test the saved ABLE model with PICMUS17 and Alpinion datasets

### Version1 VS Version2
(version1 starts on 16 April 2021)

(version2 starts on 18 April 2021)
##### 1. version2 uses custom loss functions (loss_SMSLE, loss_unity), but version1 only uses keras built-in loss MSLE
##### 2. version2 considers validation_split=0.3, version1 doesn't use validation set
##### 3. version2 uses callbacks to do Model Saving and Early Stopping, which are not considered in version1
##### 4. version2's beamformed images are worse than that of version1, because 30% data is used to do validation.

## Notes
Each original PICMUS16 dataset contains 75 angles' frames, which help to build Targets (DAS with 75 angles). However, when these datasets are used as Inputs, only angle==0.0 is condidered.

Each PICMUS17 dataset just has data with angle==0.0, so just let them to be Tests.



