---
title: Fourier Phase Retrieval Using Physics-Enhanced Deep Learning
summary: OPTICS LETTERS
date: 2024-10-23

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: 'Concept of the Physics-enhanced Fourier phase retrieval'

authors:
  - admin
#  - Ted

tags:
  - Computational Imaging
  - Master
---

[🔗Paper Link](https://doi.org/10.1364/OL.537792)

{{< toc mobile_only=true is_open=true >}}

## Abstract

Fourier phase retrieval (FPR) aims to reconstruct an object image from the magnitude of its Fourier transform. Despite its widespread utility in various fields of engineering and science, the inherent ill-posed nature of the FPR problem poses a significant challenge. 

Here we propose a learning-based approach that incorporates the physical model of the FPR imaging system with a deep neural network. Our method includes two steps: First, we leverage the image formation model of the FPR to guide the generation of data for network training in a self-supervised manner. Second, we exploit the physical model to fine-tune the pre-trained model to impose the physics-consistency constraint on the network prediction. This allows us to integrate both implicit prior from training data and explicit prior from the physics of the imaging system to address the FPR problem. Simulation and experiments demonstrate that the proposed method is accurate and stable, showcasing its potential for wide application in fields utilizing the FPR. We have made our source code available for non-commercial use.   

## Results

We presents a physics-enhanced deep learning approach for Fourier phase retrieval (FPR), which aims to reconstruct an object image from the magnitude of its Fourier transform. The FPR problem is inherently ill-posed due to the lack of phase information, leading to challenges in accurately reconstructing the object image.

We propose a two-step method that combines physical modeling with deep neural networks:

1. **Self-Supervised Pre-Training**: The first step involves training a neural network in a self-supervised manner using an image formation model of the FPR system. This approach leverages a large dataset (e.g., MNIST) to generate synthetic data for training. The objective is to establish a mapping from the Fourier magnitude pattern to the object image.

2. **Physics-Driven Fine-Tuning**: In the second step, a physics-consistency loss is used to fine-tune the pre-trained model. This ensures that the network's predictions adhere to the physical constraints of the imaging system, improving the generalization and interpretability of the results. A Bartlett window is employed to minimize spectral leakage, enhancing imaging performance.

The proposed method integrates both implicit priors from the training data and explicit priors from the physical model of the imaging system. Simulation and experimental results demonstrate the accuracy and stability of the approach, showing its potential for wide application in various fields that utilize FPR.

We compare their method with classical iterative phase retrieval methods and other deep learning-based approaches, highlighting the superior performance of their physics-enhanced deep learning method. The approach overcomes the limitations of traditional end-to-end data-driven deep learning methods by enabling the reconstruction of out-of-domain data without the need for target domain training datasets.

<img src=".\fig1.png" style="zoom:50%;" />

<center style="font-size:14px"><p>Figure 1. Recovered images from the ablation study.(a) Results
for in-domain (MNIST) test data. (b) Results for out-of-domain (EMNIST) test data. (c) Quantitative results from nine repeated runs using the dashed box target in (b). Error bars represent the standard deviation of the evaluation metrics of results from nine runs. </p></center>

<img src=".\fig2.png" style="zoom:50%;" />

<center style="font-size:14px"><p>Figure 2. Fourier coherent diffraction imaging experiment setup. M1 and M2, mirrors; L1, L2, lens.</p></center>

<img src=".\fig3.png" style="zoom:30%;" />

<center style="font-size:14px"><p>Figure 3. Recovered images from the coherent diffraction imaging experiment. (a) Ground truth images captured by a camera. (b) Raw measured Fourier magnitude patterns (scaled). We exploit different reconstruction algorithms to restore the object image from the patterns shown in (b), resulting in results of HSE (hybrid input–output + shrinkwrap + error reduction) (c), DNN-HIO (deep neural network-aided hybrid input-output) (d), untrained (e), end-to-end (f), our method without (g), and with (h) Bartlett window.</p></center>

## Conclusion

In summary, this work introduces a novel physics-enhanced deep learning approach for FPR, demonstrating its ability to achieve high-quality image reconstruction from a single Fourier magnitude pattern. Future work includes applying this approach to more practical phase retrieval problems, such as lensless X-ray imaging.
