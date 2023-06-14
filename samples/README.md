# Blur Dataset

## Samples

|Sharp     | Defocused-blurred | Motion-blurred |
|-----------|-------|-------|
|![106_NIKON-D3400-35MM_S](https://github.com/adi907/ImageDeblurring/assets/76524120/350a0cd1-f376-4675-828d-a5e83a96362f) | ![106_NIKON-D3400-35MM_F](https://github.com/adi907/ImageDeblurring/assets/76524120/b83a3694-4842-488b-8400-1d03f51e262d)| ![106_NIKON-D3400-35MM_M](https://github.com/adi907/ImageDeblurring/assets/76524120/27bd52e7-1180-445a-8a91-19f13d438431) |
| ![176_HONOR-7X_S](https://github.com/adi907/ImageDeblurring/assets/76524120/d173a850-b04d-4435-ba71-ebc9356d22b6) | ![176_HONOR-7X_F](https://github.com/adi907/ImageDeblurring/assets/76524120/e9950b5d-38a4-44d2-a37e-5c1ae264e55a) | ![176_HONOR-7X_M](https://github.com/adi907/ImageDeblurring/assets/76524120/dc292e01-0a13-4b27-911c-2139e6b9511c) |
|![180_HONOR-10_S](https://github.com/adi907/ImageDeblurring/assets/76524120/6af73cfd-8b3b-41b3-9230-68452dbcb0b3) | ![180_HONOR-10_F](https://github.com/adi907/ImageDeblurring/assets/76524120/1649240d-abdf-4725-bf16-cf2c7b3f9be1) | ![180_HONOR-10_M](https://github.com/adi907/ImageDeblurring/assets/76524120/bb45f281-cc75-4cb6-bd81-4fea7f4a79f4) |


## Description
This dataset contains 1050 blurred and sharp images (350 triplets), each image triplet is a set of three photos of the same scene: sharp, defocused-blurred and motion-blurred images.

The dataset was created to validate the blur detection algorithm. The dataset can also be used for testing image deblurring, hovewer, the triplets are not "pixel-to-pixel" images, so, one cannot compare blurred and sharp images on the basis of PSNR or SSIM but sharp images can be used for visual comparison.

## Dataset structure
The dataset contains three folders: sharp, defocused-blurred and motion-blurred images.

The filename structure is as follows: id_device_type.extension where

ID - a number from 0 to 349;
device - the image capture device;
type - one of [S, F, M]. S stands for Sharp image, F - deFocused-blurred image and M - Motion-blurred image.
The dataset contains 66 devices, these are typically smartphones, but several cameras are also provided.

The dataset contains 66 devices, these are typically smartphones, but several cameras are also provided.
<details> 
<summary>List of devices:</summary>
<p> 

|Device     | Amount|
|-----------|-------|
|HONOR-7X	| 37	|
|NIKON-D3400-18-55MM	| 37	|
|HONOR-8X	| 30	|
|IPHONE-SE	| 30	|
|NIKON-D3400-35MM	| 25	|
|XIAOMI-PROCOFONE-F1	| 23	|
|IPHONE-7	| 13	|
|IPHONE-6S	| 11	|
|XIAOMI-MI8-SE	| 9	|
|HONOR-10	| 8	|
|ASUS-ZENFONE-LIVE-ZB501KL	| 6	|
|HONOR-7C	| 6	|
|HUAWEI-P20-LITE	| 6	|
|SONY-NEX-5T	| 6	|
|XIAOMI-REDMI-7	| 6	|
|HUAWEI-P20	| 5	|
|IPHONE-8-PLUS	| 5	|
|SAMSUNG-GALAXY-J3	| 5	|
|HUAWEI-MATE20	| 4	|
|HUAWEI-Y9	| 4	|
|IPHONE-8	| 4	|
|CANON-6D-100MM	| 3	|
|HONOR-9	| 3	|
|HUAWEI-NOVA-LITE	| 3	|
|IPHONE-7-PLUS	| 3	|
|SAMSUNG-GALAXY-A8	| 3	|
|SAMSUNG-GALAXY-J5	| 3	|
|WILEYFOX-SWIFT-2-PLUS	| 3	|
|XIAOMI-REDMI-3S	| 3	|
|XIAOMI-REDMI-NOTE-7	| 3	|
|HONOR-6X	| 2	|
|HUAWEI-P30-PRO	| 2	|
|ONEPLUS-3T	| 2	|
|SAMSUNG-GALAXY-A5	| 2	|
|SAMSUNG-GALAXY-A6	| 2	|
|SAMSUNG-GALAXY-J7	| 2	|
|XIAOMI-REDMI-5-PLUS	| 2	|
|ASUS-ZE500KL	| 1	|
|BQ-5512L	| 1	|
|CANON-6D-70-200MM	| 1	|
|HONOR-4C	| 1	|
|HONOR-8	| 1	|
|HONOR-9-LITE	| 1	|
|HUAWEI-P-SMART	| 1	|
|HUAWEI-P30	| 1	|
|HUAWEI-P30-LITE	| 1	|
|IPHONE-5S	| 1	|
|IPHONE-6	| 1	|
|IPHONE-XR	| 1	|
|LG-Q6	| 1	|
|NOKIA-21	| 1	|
|PANASONIC-DMC-TZ35	| 1	|
|PRESTIGIO-MULTI-PHONE	| 1	|
|SAMSUNG-EDGE-7C	| 1	|
|SAMSUNG-GALAXY-7-NEO	| 1	|
|SAMSUNG-GALAXY-A3	| 1	|
|SAMSUNG-GALAXY-GRAND-PRIME	| 1	|
|SAMSUNG-GALAXY-GRAND-PRIME-PLUS	| 1	|
|SAMSUNG-GALAXY-S5	| 1	|
|SONY-XPERIA-E5	| 1	|
|XIAOMI-MI8-LITE	| 1	|
|XIAOMI-REDMI-4	| 1	|
|XIAOMI-REDMI-4A	| 1	|
|XIAOMI-REDMI-4X	| 1	|
|XIAOMI-REDMI-NOTE-4X	| 1	|
|XIAOMI-REDMI-NOTE-5A-PRIME	| 1	|
</p> 
</details>

## Download
Kaggle dataset (images were scaled to 2048 pixels by the widest side): https://www.kaggle.com/kwentar/blur-dataset

Google drive (source images): https://drive.google.com/open?id=1RObmCDPeQ1Lg-V6u7dT02Pf0qH-QMcTp

Mirror: https://yadi.sk/d/_Wli3wSSScnzCg
