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

Libraries Required :- 
                      Numpy
                      Pandas
                      Matplotlib
                      OpenCV
                      tqdm
                      TensorFlow
                      Keras

3. Pre-process the images into a standard size and format

Standard size: (128,128,3)

4. Split the train & test set

Split choosen: 80:20

5. Define CNN architecture and network hyperparameters

Loss function -> Mean Squared Error
Optimizer -> Adam
Evaluation metric -> Accuracy

Also define the learning rate reducer to reduce the learning rate if there’s no improvement in the Accuracy

6. Build the Autoencoder Model via Encoder & Decoder Model

Encoder - Build a stack of Conv2D(64) - Conv2D(128) - Conv2D(256). The model is going to be having input shape (128, 128, 3) and kernel size equal to 3 and the Encoder will compress this shape to (16, 16, 256) and will further flatten this into a one dimensional array which will be the input for our Decoder.

Decooder - Manually convert the one dimensional array from the encoder model to the shape (16, 16, 256) and then send it to the decoder to decode it back to (128, 128, 3) shape. So the stack here will be Conv2DTranspose(256) - Conv2DTranspose(128) - Conv2DTranspose(64).

AUTOENCODER = Encoder + Decoder

7. Train the Model

Accuracy - 68 %

8. Analyze the results

We cannot compare blurred and sharp images on the basis of PSNR or SSIM but sharp images can be used for visual comparison.

Analyze:
Loss vs Epoch
<img width="735" alt="result1" src="https://github.com/adi907/ImageDeblurring/assets/76524120/dcbf156f-77b5-44fc-b6ea-6200eff9620b">

Accuracy vs Epoch
<img width="735" alt="result2" src="https://github.com/adi907/ImageDeblurring/assets/76524120/11e3f99f-5ee1-4027-a7c6-10f7fd59d487">
