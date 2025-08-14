# 180DC ML SIG Recruitment Challenge – **Challenge 1**: Image Denoising & Classification

## Overview

Welcome to **Challenge 1** in the **180 Degrees Consulting – Machine Learning Special Interest Group Recruitment Challenge**!

Your mission: create a **two-stage ML pipeline** that:

1. **Denoises** noisy flower images, and
2. **Classifies** them into their correct categories.

This challenge assesses your ability to preprocess, model, and evaluate noisy real-world-like data in a clean, reproducible way.

---

## The Task

You will work with images from five flower categories:

* **Daisy**
* **Dandelion**
* **Roses**
* **Sunflowers**
* **Tulips**

### Dataset Composition:

* **Training set** – Contains **paired noisy and clean images**, grouped by class. Ideal for supervised denoising.
* **Test set** – Contains only **noisy images**, randomly ordered and unlabeled.

---

## Objectives

1. **Stage 1 – Denoising**

   * Train a denoising model using the noisy-clean paired training data.
   * Apply it to the test set to produce a directory:
     **`Denoised_Images/`**.

2. **Stage 2 – Classification**

   * Train your classifier using the clean training images.
   * Use it to assign labels to images in **`Denoised_Images/`**.

3. **Evaluation**

   * Compute **PSNR** and **SSIM** metrics on the test set **before** and **after** denoising.

4. **Submission File**

   * Create `test_labels.csv` formatted like:

     ```
     Images,Predicted_Classes
     Image_Test_1.png,3
     Image_Test_2.png,5
     ...
     ```

     Class mapping:

     * `1` = Daisy
     * `2` = Dandelion
     * `3` = Roses
     * `4` = Sunflowers
     * `5` = Tulips

---

## Rules

* Use only the provided training dataset for denoising and classification.
* Only apply your denoising model to the test images—no other alterations allowed.
* Your outputs (**`Denoised_Images/`**, evaluation metrics, and `test_labels.csv`) must be reproducible.

---

## Additional Requirement – Approach Report

Submit a **1–2 page report** detailing:

* Your denoising strategy
* Your classification model
* Key architectural and preprocessing decisions
* Evaluation observations (including PSNR & SSIM)
* Challenges you encountered and how you addressed them

---

## Resources

These are suggested references to inspire your approach—not direct solutions:

* **Research Papers**

  * *Denoising Autoencoders* by Vincent et al. (2008)
  * *Beyond a Gaussian Denoiser: Residual Learning of Deep CNN for Image Denoising* by Zhang et al. (2017)

* **YouTube Tutorials**

[Denoising Autoencoders | Deep Learning Animated](https://www.youtube.com/watch?v=0V96wE7lY4w&utm_source=chatgpt.com)

[Image Denoising with Autoencoders (Brilliant tutorial)](https://www.youtube.com/watch?v=0V96wE7lY4w&utm_source=chatgpt.com)

---

## Deliverables

1. **`Denoised_Images/`** – denoised test set.
2. **Evaluation report** – PSNR & SSIM before and after denoising.
3. **`test_labels.csv`** – your final submission file.
4. **Approach Report** – 1–2 page description of your solution.

---

## Submission

Submit your `test_labels.csv` to the Kaggle competition:

[**180-DC ML SIG Recruitment Challenge on Kaggle**](https://www.kaggle.com/competitions/180-dc-ml-sig-recruitment)
