# Blind Motion Deblurring via Auto-Encoders

## Process

# 1. Get Dataset: Imported from Kaggle

## Samples

|Sharp     | Defocused-blurred | Motion-blurred |
|-----------|-------|-------|
|![106_NIKON-D3400-35MM_S](https://github.com/adi907/ImageDeblurring/assets/76524120/350a0cd1-f376-4675-828d-a5e83a96362f) | ![106_NIKON-D3400-35MM_F](https://github.com/adi907/ImageDeblurring/assets/76524120/b83a3694-4842-488b-8400-1d03f51e262d)| ![106_NIKON-D3400-35MM_M](https://github.com/adi907/ImageDeblurring/assets/76524120/27bd52e7-1180-445a-8a91-19f13d438431) |
| ![176_HONOR-7X_S](https://github.com/adi907/ImageDeblurring/assets/76524120/d173a850-b04d-4435-ba71-ebc9356d22b6) | ![176_HONOR-7X_F](https://github.com/adi907/ImageDeblurring/assets/76524120/e9950b5d-38a4-44d2-a37e-5c1ae264e55a)
| ![176_HONOR-7X_M](https://github.com/adi907/ImageDeblurring/assets/76524120/dc292e01-0a13-4b27-911c-2139e6b9511c)
|![180_HONOR-10_S](https://github.com/adi907/ImageDeblurring/assets/76524120/6af73cfd-8b3b-41b3-9230-68452dbcb0b3) | 
![180_HONOR-10_F](https://github.com/adi907/ImageDeblurring/assets/76524120/1649240d-abdf-4725-bf16-cf2c7b3f9be1) | 
![180_HONOR-10_M](https://github.com/adi907/ImageDeblurring/assets/76524120/bb45f281-cc75-4cb6-bd81-4fea7f4a79f4) |

# 2. Import Libraries

Libraries Required :- 
<p margin-left="30%">
                      Numpy<br>
                      🐼Pandas<br>
                      Matplotlib<br>
                      OpenCV<br>
                      tqdm<br>
                      TensorFlow<br>
                      Keras<br>
  </p>

# 3. Pre-process the images into a standard size and format

Standard size: (128,128,3)

# 4. Split the train & test set

Split choosen: 80:20

# 5. Define CNN architecture and network hyperparameters<br>

Loss function -> Mean Squared Error<br>
Optimizer -> Adam<br>
Evaluation metric -> Accuracy<br>

Also define the learning rate reducer to reduce the learning rate if there’s no improvement in the Accuracy

# 6. Build the Autoencoder Model via Encoder & Decoder Model

Encoder - Build a stack of Conv2D(64) - Conv2D(128) - Conv2D(256). The model is going to be having input shape (128, 128, 3) and kernel size equal to 3 and the Encoder will compress this shape to (16, 16, 256) and will further flatten this into a one dimensional array which will be the input for our Decoder.

Decoder - Manually convert the one dimensional array from the encoder model to the shape (16, 16, 256) and then send it to the decoder to decode it back to (128, 128, 3) shape. So the stack here will be Conv2DTranspose(256) - Conv2DTranspose(128) - Conv2DTranspose(64).

AUTOENCODER = Encoder + Decoder

# 7. Train the Model

Accuracy - 68 %

# 8. Analyze the results

We cannot compare blurred and sharp images on the basis of PSNR or SSIM but sharp images can be used for visual comparison.

Analyze:<br><br>
Loss vs Epoch<br>
<img width="735" alt="result1" src="https://github.com/adi907/ImageDeblurring/assets/76524120/dcbf156f-77b5-44fc-b6ea-6200eff9620b">

Accuracy vs Epoch<br>
<img width="735" alt="result2" src="https://github.com/adi907/ImageDeblurring/assets/76524120/11e3f99f-5ee1-4027-a7c6-10f7fd59d487">
