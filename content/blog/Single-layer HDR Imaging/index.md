---
title: Single-layer metasurface for snapshot high-dynamic-range imaging
summary: Photonics Research
date: 2025-08-01

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: 'Concept of the complex amplitude modulation metalens based HDR Imaging'

authors:
  - admin
#  - Ted

tags:
  - Metasurface
  - Master
---

[🔗Paper Link](https://doi.org/10.1364/PRJ.563285)

{{< toc mobile_only=true is_open=true >}}

## Abstract

### Research Problem:

In imaging systems, the limited dynamic range of conventional detectors makes it challenging to preserve details in both highlight and shadow regions within a single frame under environments with significant illumination variations. This issue is particularly prominent in applications such as smartphone photography, microscopic imaging, industrial manufacturing, and autonomous driving. The development of real-time high dynamic range (HDR) imaging devices is therefore of great significance.

### Research Methodology:

This paper proposes an instantaneous HDR imaging scheme based on a single-layer metasurface (SiM-SHDR). The metasurface employs a polarization-independent full-space amplitude and phase modulation mechanism, enabling the capture of multiple images with different intensities in a single exposure. By fusing these images, the dynamic range of the resulting image is effectively expanded.

<img src=".\fig2.PNG" style="zoom:23%;" />

<center style="font-size:14px"><p>Figure 1. Design scheme of the HDR Metalens.</p></center>

## Experimental Design:

1. **Metasurface Design**: A complex amplitude modulation method based on meta-atom interference was adopted to design a single-layer metasurface capable of simultaneous dual-channel imaging, with an intensity ratio of 10:1 between the two images.
2. **Experimental Validation**: The metasurface sample was fabricated using electron-beam lithography, and its imaging performance was verified in an experimental setup. A 532 nm laser source was employed, and the captured dual-intensity images were processed using an image fusion algorithm.

<img src=".\fig1.PNG" style="zoom:30%;" />

<center style="font-size:14px"><p>Figure 2. Experimental results of dynamic range enhancement.</p></center>

## Results and Analysis:

1. **Dynamic Range Enhancement**: Experimental results demonstrate that the proposed scheme achieves a dynamic range improvement of 17.5 dB, approaching the theoretical limit of 20 dB.
2. **Imaging Quality**: The fused image successfully preserves details in both highlight and shadow regions, with peak signal-to-noise ratio (PSNR) and structural similarity index (SSIM) outperforming those of single-exposure images.
3. **System Integration**: The single-layer metasurface replaces multiple components in traditional HDR systems, significantly reducing system volume and weight, making it suitable for lightweight, ultra-compact real-time HDR imaging applications.

## Conclusion:

The SiM-SHDR scheme achieves efficient complex amplitude modulation via a single-layer metasurface, enabling the capture of multiple high-fidelity images in a single exposure and significantly enhancing dynamic range through fusion algorithms. This method exhibits notable advantages in system integration and imaging performance, providing a novel solution for real-time HDR imaging in fields such as smartphone photography, microscopic imaging, and autonomous driving.
