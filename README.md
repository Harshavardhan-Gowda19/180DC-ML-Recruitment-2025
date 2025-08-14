# 180DC ML SIG Recruitment Challenge – Image Denoising & Classification

## Overview

Welcome to the **180 Degrees Consulting – Machine Learning Special Interest Group Recruitment Challenge!**

You are invited to build a **two-stage machine learning pipeline** that:

1. **Denoises** noisy flower images, and
2. **Classifies** them into one of five flower categories.

This challenge evaluates your expertise in image preprocessing, model training, and building robust inference systems on real-world-like noisy data.

---

## The Task

You will work with a dataset consisting of five flower classes:

* **Daisy**
* **Dandelion**
* **Roses**
* **Sunflowers**
* **Tulips**

**Dataset structure**:

* **Training set**: Contains paired **noisy** and **clean** versions of images, organized by class—ideal for supervised learning.
* **Test set**: Contains only **noisy** images, in random order, with no clean references.

---

## Your Objective

1. **Stage 1 – Denoising**

   * Train a denoising model using the provided noisy & clean training images.
   * Run it on the test set to generate a new folder:
     **`Denoised_Images/`**.

2. **Stage 2 – Classification**

   * Train a classifier on the clean training images.
   * Predict labels for images in `Denoised_Images`.

3. **Evaluation**

   * Compute **PSNR** and **SSIM** metrics for the test set **before** and **after** denoising.

4. **Submission Format**

   * Prepare a CSV file named **`test_labels.csv`** with the format:

     ```
     Images,Predicted_Classes
     Image_Test_1.png,3
     Image_Test_2.png,5
     ...
     ```

     Class-to-label mapping:

     * `1` = Daisy
     * `2` = Dandelion
     * `3` = Roses
     * `4` = Sunflowers
     * `5` = Tulips

   * Submit this file to the Kaggle competition.

---

## Rules

* Use only the provided training dataset for denoising and classification.
* The test set may only be modified through your denoising model.
* Outputs (i.e., `Denoised_Images/`, evaluation results, and `test_labels.csv`) must be reproducible via your code.

---

## Resources

Here are some materials to guide your approach—these **aren't solutions**, but may inspire your design:

* **Research Papers**

  * Vincent et al. (2008), *Denoising Autoencoders*: useful for understanding how networks can learn to remove noise.
  * Zhang et al. (2017), *Beyond a Gaussian Denoiser*: a modern CNN-based method for image denoising.

* **YouTube Tutorial**

  * *Image Denoising with Autoencoders*: a conceptual walkthrough that can help you get started.

---

## Deliverables

* **`Denoised_Images/`** – contains your denoised versions of the test images.
* **Evaluation Report** – includes PSNR and SSIM scores for both pre- and post-denoising.
* **`test_labels.csv`** – your final submission file ready to upload to Kaggle.

---

## How to Submit

Submit your final `test_labels.csv` to the competition hosted on Kaggle:

[ **180-DC ML SIG Recruitment Challenge on Kaggle** ](https://www.kaggle.com/competitions/180-dc-ml-sig-recruitment)
