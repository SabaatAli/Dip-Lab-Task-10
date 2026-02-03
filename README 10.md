\\ DIP Task 10 – JPEG-Like Image Compression

Overview
This project implements a JPEG-like image compression system using Python in Google Colab. The script compresses a color image by processing each RGB channel independently using block-based Discrete Cosine Transform (DCT), quantization, and inverse DCT. The effect of compression is analyzed both visually and numerically.

Objectives
To upload and process a color image interactively in Google Colab
To apply JPEG-style compression using DCT and quantization
To compress each RGB color channel separately
To demonstrate entropy coding using Huffman coding on one channel
To evaluate compression quality using standard performance metrics

Tools & Libraries Used
Python
OpenCV (cv2)
NumPy
Matplotlib
SciPy / standard Python libraries
Google Colab

Compression Methodology
1. Image Upload & Channel Separation
The uploaded color image is split into Red, Green, and Blue (RGB) channels. Each channel is compressed independently to mimic the JPEG compression pipeline.

2. Block-Based DCT
Each channel is divided into 8 × 8 blocks
Discrete Cosine Transform (DCT) is applied to each block
DCT helps concentrate image energy into a small number of coefficients

3. Quantization
DCT coefficients are quantized using a quantization matrix
A scale_factor variable controls compression strength
Higher scale factor → stronger compression, more loss
Lower scale factor → better quality, less compression

4. Inverse DCT
After quantization, inverse DCT (IDCT) is applied to reconstruct each image channel.

5. Huffman Coding (Demonstration)
To demonstrate entropy coding, Huffman encoding is applied to one selected color channel. This step illustrates lossless compression used in JPEG.

Performance Evaluation Metrics
The script computes and prints the following metrics:
Compression Ratio (CR)
Mean Squared Error (MSE)
Peak Signal-to-Noise Ratio (PSNR)
Rate-Distortion (RD)
These metrics help analyze the trade-off between compression efficiency and image quality.

Results Visualization
Using Matplotlib, the script displays:
Original image
Compressed image
Amplified difference image to clearly highlight compression artifacts
The difference image is scaled so that even small compression losses are visible.

How to Run
Open Google Colab
Paste the provided Python script into a notebook cell
Run the cell and upload a color image when prompted
Adjust the scale_factor to observe different compression levels
View compression results and evaluation metrics

Applications
Image compression systems
Multimedia storage optimization
Image quality analysis
Digital image processing education

Conclusion
This task demonstrates the core concepts behind JPEG image compression, highlighting how DCT-based quantization affects image quality and size. By adjusting compression strength and analyzing evaluation metrics, the trade-off between compression efficiency and visual fidelity becomes clear.