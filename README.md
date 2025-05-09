# 📸 Low Resolution Image Enhancement Using Res-Net GAN

This project is an implementation and evaluation of a **Res-Net GAN-based architecture** for enhancing low-resolution images using Single Image Super Resolution (SISR). It was completed as part of an undergraduate research project at **Vardhaman College of Engineering, Hyderabad, India** and has been published as a peer-reviewed paper.

🔗 **[Read the full publication here](https://www.publications.scrs.in/chapter/978-81-955020-5-9/108)**

---

## 📌 Objective

The goal of this research is to recover **photo-realistic high-resolution (HR) images** from their low-resolution (LR) counterparts. The challenge lies in restoring **fine textural details** and **sharpness** for high upscaling factors (4x), which traditional super-resolution techniques struggle to achieve.

---

## 🧠 Methodology

The solution is based on a **Generative Adversarial Network (GAN)** framework combined with **deep residual networks (ResNet)**:

- **Generator:** Produces super-resolved images using 10 deep residual blocks with skip connections and pixel shufflers for upscaling.
- **Discriminator:** Trained to distinguish between real high-resolution images and those generated by the network.
- **Loss Function:** A novel **perceptual loss** that combines adversarial loss (from GAN) and **content loss computed on VGG-19 features**, instead of pixel-wise Mean Squared Error (MSE).

### 🧱 Network Highlights

- Input: 96x96 low-resolution image  
- Output: 384x384 super-resolved image (4x upscaling)
- Generator: Residual blocks, Parametric ReLU, Pixel shufflers  
- Discriminator: 8 convolutional layers + 2 dense layers + Sigmoid  
- Optimization: Based on adversarial training using perceptual loss (VGG19-based)

---

## 📊 Results

- Evaluated using **MOS (Mean Opinion Score)** based on human visual assessments (scale 1 to 5).
- Res-Net GAN achieved **MOS scores comparable to actual high-resolution images**.
- Compared to ResNet without GAN, this approach showed **superior perceptual quality** on high upscaling tasks.
- Quantitative metrics (MSE, PSNR, SSIM) and qualitative visual results were analyzed and reported.

---

## 📁 Repository Structure

📦 Low-Resolution-Image-Enhancement-Using-ResNet-GAN
 ┣ 📂 src/               ← Implementation code
 ┣ 📂 models/            ← Trained model files 
 ┣ 📂 results/           ← Output image samples and comparisons
 ┣ 📂 data/              ← Sample input data or links to datasets
 ┣ 📜 README.md
 



---

## 🛠️ Technologies Used

- Python, PyTorch (or TensorFlow)
- VGG19 (pre-trained)
- NumPy, OpenCV, Matplotlib
- GAN + ResNet + PixelShuffle
- Evaluation: MSE, PSNR, SSIM, MOS

---

## 📣 Citation

If you use this work, please cite:

**Arun Sai Narla**, Shalini Kapuganti, Hathiram Nenavath,  
*Low Resolution Image Enhancement Using Res-Net GAN*,  
SCRS International Conference Publication, 2023.  
🔗 [Link to paper](https://www.publications.scrs.in/chapter/978-81-955020-5-9/108)

---

## 🧑‍💻 Contributors

- Arun Sai Narla – arunsaiknr@gmail.com  
- Shalini Kapuganti  
- Hathiram Nenavath  

---

## 📌 License

This repository is provided under the MIT License. Feel free to use, share, and contribute!




