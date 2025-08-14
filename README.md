# 180DC ML SIG Recruitment Challenge – **Challenge 1**: Image Denoising & Classification

## Overview

Welcome to the **180 Degrees Consulting – Machine Learning SIG Recruitment Challenge!**

This is **Challenge 1** of the recruitment process.
Your task is to design and implement a **two-stage machine learning pipeline** that:

1. **Denoises** noisy flower images, and
2. **Classifies** them into the correct category.

This challenge will assess your skills in image preprocessing, noise removal, and building classification models that can work effectively on degraded data.

---

## The Task

You are provided with a dataset of five flower categories:

* **Daisy**
* **Dandelion**
* **Roses**
* **Sunflowers**
* **Tulips**

**Dataset contents**:

* **Training set** – Contains paired **noisy** and **clean** images, organized by class.
* **Test set** – Contains only **noisy** images, randomly ordered, without clean references.

---

## Your Objective

1. **Stage 1 – Denoising**

   * Train a denoising model using the noisy and clean training images.
   * Apply it to the test set and save the results in a folder named **`Denoised_Images`**.

2. **Stage 2 – Classification**

   * Train a classifier using the clean training images.
   * Classify the denoised test images into one of the five flower categories.

3. **Evaluation**

   * Calculate **PSNR** and **SSIM** for the test images **before** and **after** denoising.

4. **Submission File**

   * Create a CSV file named **`test_labels.csv`** with this format:

     ```
     Images,Predicted_Classes
     Image_Test_1.png,3
     Image_Test_2.png,5
     ...
     ```

     Class label mapping:

     * `1` = Daisy
     * `2` = Dandelion
     * `3` = Roses
     * `4` = Sunflowers
     * `5` = Tulips

---

## Rules

* You must train using only the provided training dataset.
* Test set images can only be modified through your denoising model.
* Your outputs (`Denoised_Images/`, evaluation metrics, and `test_labels.csv`) must be reproducible from your submitted code.

---

## Additional Requirement – Approach Report

Along with your submission, prepare a **1–2 page report** describing:

* Your denoising method
* Your classification approach
* Key design decisions
* Observations from evaluation metrics
* Challenges faced and how you overcame them

The report should be clear, concise, and demonstrate your understanding of the problem.

---

## Resources

Here are some references to guide your thinking (not exact solutions):

* **Research Papers**

  * [Denoising Autoencoders](https://doi.org/10.1109/CVPR.2008.4580859) – Vincent et al., 2008
  * [Beyond a Gaussian Denoiser: Residual Learning of Deep CNN for Image Denoising](https://arxiv.org/abs/1608.03981) – Zhang et al., 2017

* **YouTube Video**

  * [Image Denoising with Autoencoders](https://www.youtube.com/watch?v=9z8o9vRX6xI)

---

## Deliverables

1. **`Denoised_Images/`** – denoised test images.
2. **Evaluation Metrics** – PSNR & SSIM before and after denoising.
3. **`test_labels.csv`** – final submission file.
4. **Approach Report** – 1–2 pages detailing your solution.

---

## Submission

Submit your **`test_labels.csv`** to the Kaggle competition:
[**180-DC ML SIG Recruitment Challenge on Kaggle**](https://www.kaggle.com/competitions/180-dc-ml-sig-recruitment)
