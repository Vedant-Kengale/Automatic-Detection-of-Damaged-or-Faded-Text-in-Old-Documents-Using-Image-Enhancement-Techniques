# 📄 Automatic Detection of Damaged or Faded Text in Old Documents Using Image Enhancement Techniques

## 📌 Project Overview

Historical documents, manuscripts, and old scanned records often suffer from fading, noise, low contrast, and physical degradation, making their text difficult to read and preserve.

This project presents an AI-powered document enhancement approach that improves the readability of damaged and faded document images using advanced image processing techniques and Generative Adversarial Networks (GANs).

The system combines traditional image enhancement methods with deep learning techniques to restore document clarity, reduce noise, improve contrast, and produce enhanced images for better visual interpretation.

## 🎯 Project Objectives

- Improve the readability of faded and degraded document images.
- Remove unwanted noise and improve image quality.
- Enhance text visibility through contrast enhancement and binarization.
- Implement a GAN-based image restoration approach using deep learning.
- Compare original, preprocessed, and enhanced document images.
- Support digital preservation of historical documents.

## ✨ Key Features

- **Image Preprocessing:** Applies bilateral filtering to reduce noise while preserving important image details.
- **Contrast Enhancement:** Uses CLAHE (Contrast Limited Adaptive Histogram Equalization) to improve text visibility.
- **Image Binarization:** Implements Otsu's thresholding, Adaptive Gaussian Thresholding, and Adaptive Mean Thresholding.
- **GAN-Based Restoration:** Uses a U-Net-based Generator and PatchGAN Discriminator to enhance degraded document images.
- **Morphological Processing:** Applies morphological opening and closing to remove unwanted artifacts and refine text regions.
- **Visual Comparison:** Displays original, preprocessed, and enhanced images for performance comparison.
- **Model Saving:** Saves trained generator and discriminator models for subsequent use.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| OpenCV | Image processing and enhancement |
| NumPy | Numerical operations and image manipulation |
| Matplotlib | Image visualization and comparison |
| TensorFlow / Keras | Deep learning and GAN implementation |
| Google Colab | Development and execution environment |

## 🧠 Methodology

The project follows a multi-stage document enhancement workflow.

### 1. Input Document Image
A scanned or degraded document image is provided as input to the system.

### 2. Image Preprocessing
- Convert the input image into grayscale.
- Apply bilateral filtering for noise reduction.
- Use CLAHE to enhance local image contrast.

### 3. Image Binarization
Different thresholding techniques are applied to distinguish text from the background:
- Otsu's Thresholding
- Adaptive Gaussian Thresholding
- Adaptive Mean Thresholding

The adaptive thresholding outputs are also combined to generate an enhanced binary representation.

### 4. GAN-Based Image Enhancement

The deep learning component uses a Generative Adversarial Network consisting of two main components:

**Generator (U-Net CNN)**
- Takes a degraded document image as input.
- Learns to generate an enhanced document image.
- Uses an encoder-decoder architecture with skip connections.

**Discriminator (PatchGAN)**
- Evaluates generated images at the patch level.
- Helps distinguish realistic document images from generated outputs.
- Provides adversarial feedback to improve the generator.

Both networks work together through adversarial training to improve the visual quality of document images.

### 5. Morphological Processing

Morphological operations are applied to refine the enhanced image:
- Morphological Opening
- Morphological Closing

These operations help remove small artifacts and improve the appearance of text regions.

### 6. Output Visualization

The system generates visual comparisons of:
- Original document image
- Preprocessed image
- GAN-enhanced image
- Different thresholding outputs
- Final morphologically processed image

## ⚙️ Installation and Setup

### Prerequisites

- Python 3.x
- Google Colab or Jupyter Notebook
- Google Drive (for accessing input images)

### Step 1: Clone the Repository

```bash
git clone https://github.com/Vedant-Kengale/Automatic-Detection-of-Damaged-or-Faded-Text-in-Old-Documents-Using-Image-Enhancement-Techniques.git
```

### Step 2: Navigate to the Project Directory

```bash
cd Automatic-Detection-of-Damaged-or-Faded-Text-in-Old-Documents-Using-Image-Enhancement-Techniques
```

### Step 3: Install Dependencies

```bash
pip install opencv-python numpy matplotlib tensorflow
```

### Step 4: Open the Notebook

Open the following notebook in Google Colab:

`FDIP_Document_Enhancement_Techniques.ipynb`

Alternatively, upload the notebook to Google Colab directly.

### Step 5: Configure the Input Image

Mount your Google Drive and update the input image path in the notebook.

```python
from google.colab import drive
drive.mount('/content/drive')

test_image_path = "/content/drive/MyDrive/your_folder/your_document.png"
```

Replace the example path with the actual location of your document image.

### Step 6: Execute the Notebook

Run the notebook cells sequentially to perform:
1. Image preprocessing
2. Contrast enhancement
3. Image binarization
4. GAN model construction
5. GAN training and enhancement
6. Morphological processing
7. Output visualization and model saving

## 📂 Project Structure

```text
Automatic-Detection-of-Damaged-or-Faded-Text/
│
├── FDIP_Document_Enhancement_Techniques.ipynb
│
├── Damaged Document Enhancement Report.docx
│
├── Download.jpg
│
└── README.md
```

## 📊 Expected Results

The system aims to improve the visual quality and readability of degraded document images.

| Input | Expected Enhancement |
|---|---|
| Faded text | Improved text contrast |
| Noisy documents | Reduced image noise |
| Low-contrast images | Enhanced local contrast |
| Uneven backgrounds | Improved text-background separation |
| Degraded text regions | Refined enhanced output |

The notebook also generates before-and-after comparisons and saves the processed images and model files.

## 🚀 Future Enhancements

- Integrate OCR (Optical Character Recognition) to extract text from restored documents.
- Train and evaluate the GAN using a larger paired dataset of degraded and clean document images.
- Develop a web-based interface for uploading and restoring documents.
- Support multiple document formats such as JPG, PNG, and PDF.
- Introduce quantitative evaluation metrics such as PSNR, SSIM, and OCR accuracy.
- Improve restoration performance for severely damaged historical manuscripts.

## ⚠️ Project Limitations

- The current notebook uses simulated degradation generated from a document image for its simplified GAN training workflow.
- Model performance may vary depending on document quality and degradation type.
- Reliable generalization requires training and validation on a larger, diverse document dataset.
- OCR-based text extraction is not currently implemented.

## 👨‍💻 Author

**Vedant Kengale**

- GitHub: [Vedant-Kengale](https://github.com/Vedant-Kengale)
- LinkedIn: [Vedant Kengale](https://www.linkedin.com/in/Vedant-Kengale/)

## ⭐ Acknowledgement

This project was developed as an academic project focused on Image Processing and AI-based document restoration, exploring the application of computer vision and deep learning techniques for preserving historical documents.

---

If you find this project useful, consider giving the repository a ⭐ on GitHub!
