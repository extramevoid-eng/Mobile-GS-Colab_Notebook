
<h2 align="center"> <a href="https://xiaobiaodu.github.io/mobile-gs-project/">Mobile-GS: Real-time Gaussian Splatting for Mobile Devices</a></h2>
<p align="center">
  <b>This fork contains critical patches for modern CUDA environments and a one-click Google Colab pipeline.</b>
</p>

<p align="center">
  <a href="https://colab.research.google.com/gist/extramevoid-eng/3235c4707875387c0e04275c3ff4018d/mobilegs.ipynb">
    <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab" height="32px">
  </a>
  <img src="https://img.shields.io/badge/WebGL-Embedded_Viewer-orange" alt="WebGL">
  <img src="https://img.shields.io/badge/Patched-CUDA_12.x-green" alt="Patched">
</p>

<p align="center">
  <a href="https://xiaobiaodu.github.io/mobile-gs-project/">
    <img src="https://img.shields.io/badge/Webpage-blue" alt="project">
  </a>
  <a href="https://arxiv.org/abs/2603.11531">
    <img src="https://img.shields.io/badge/Arxiv-2603.11531-b31b1b.svg?logo=arXiv" alt="arXiv">
  </a>
  <a href="https://github.com/extramevoid-eng/Mobile-GS-Colab_Notebook/blob/main/LICENSE">
    <img src="https://img.shields.io/badge/License-Apache%202.0-blue.svg" alt="License">
  </a>
</p>


---

## 🛠️ Fork Improvements & Bug Fixes

The original repository has several compatibility issues with current Python/CUDA environments. This fork resolves:

1. **C++ Compilation Fix:** Patched `simple_knn.cu` to include missing `<float.h>` (resolves `FLT_MAX` undefined error).
2. **Legacy Python Support:** Fixed `scene/dataset_readers.py` to use `np.uint8` instead of deprecated `np.byte` (resolves Pillow loading crashes).
3. **Environment Isolation:** Integrated `uv` for 10x faster, conflict-free dependency installation.
4. **Embedded Viewer:** Added an automated script to convert `.ply` to `.splat` and view 3D models directly in Colab/Mobile via a secure WebGL proxy.

---

## 🚀 Quick Start (One-Click)

The easiest way to train and view a model is via the **[Interactive Colab Notebook]
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/gist/extramevoid-eng/3235c4707875387c0e04275c3ff4018d/mobilegs.ipynb)


It handles all C++ builds, dataset downloads, and 3D rendering automatically.

## 🤝 Acknowledgments & Credits

This project is an optimized fork of the original **[Mobile-GS](https://github.com/hbb1/Mobile-GS)** research implementation. 

* **Original Authors:** Xiaobiao Du, Yida Wang, Kun Zhan, and Xin Yu.
* **Core Research:** [Mobile-GS: Real-time Gaussian Splatting for Mobile Devices](https://arxiv.org/abs/2603.11531).
* **WebGL Engine:** Built using the ultra-fast viewer by **[Antimatter15](https://github.com/antimatter15/splat)**.
* **Infrastructure:** Developed and tested on **Google Colab** using the `uv` package manager for environment isolation.

Special thanks to the open-source community for providing the building blocks for real-time 3D AI!

