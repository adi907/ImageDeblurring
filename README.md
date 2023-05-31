# Blind Motion Deblurring via Auto-Encoders

## Process

1. Get Dataset: Imported from Kaggle

## Samples

|Sharp     | Defocused-blurred | Motion-blurred |
|-----------|-------|-------|
|![106 Sharp](/samples/106_NIKON-D3400-35MM_S.JPG)| ![106 Defocused](/samples/106_NIKON-D3400-35MM_F.JPG)| ![106 Motion](/samples/106_NIKON-D3400-35MM_M.JPG)|
|![176 Sharp](/samples/176_HONOR-7X_S.jpg)| ![176 Defocused](/samples/176_HONOR-7X_F.jpg)| ![176 Motion](/samples/176_HONOR-7X_M.jpg)|
|![180 Sharp](/samples/180_HONOR-10_S.jpg)| ![180 Defocused](/samples/180_HONOR-10_F.jpg)| ![180 Motion](/samples/180_HONOR-10_M.jpg)|


2. Import Libraries

3. Pre-process the images into a standard size and format


4. Split the train & test set


5. Define CNN architecture and network hyperparameters


6. Build the Autoencoder Model via Encoder & Decoder Model


7. Train the Model


8. Analyze the results
