# Python Faint Edge Detection

Python implementation of the multiscale faint edge detection algorithm introduced in:

> **Fast Detection of Curved Edges at Low SNR**  
> Nati Ofir, Meirav Galun, Boaz Nadler, Ronen Basri  
> IEEE Conference on Computer Vision and Pattern Recognition (CVPR), 2016.

Project page:
https://natiofir.github.io/projectPage.html

---

## Overview

Detecting faint edges in noisy images is a fundamental problem in computer vision, image processing, medical imaging, microscopy, and remote sensing.

Classical edge detectors such as Sobel, Canny, or Laplacian-of-Gaussian perform well when the signal-to-noise ratio (SNR) is relatively high. Under severe noise, however, these methods often fail because local image gradients become dominated by noise.

This repository implements a multiscale edge detector designed specifically for **low-SNR images**. Rather than relying on local gradients, the algorithm integrates image evidence over long candidate curves, allowing it to detect extremely weak edges while maintaining near-linear computational complexity.

The implementation follows the principles introduced in our CVPR 2016 paper and provides an easy-to-use Python implementation for research and educational purposes.

---

## Features

- Fast detection of faint curved edges
- Robust to high noise levels
- Multiscale hierarchical search
- Near-linear computational complexity
- Pure Python implementation
- Simple API
- Suitable for microscopy, medical imaging, remote sensing, and general computer vision

---

## Algorithm

The algorithm performs the following steps:

1. Construct a multiscale image pyramid.
2. Generate candidate edge curves hierarchically.
3. Compute matched-filter responses along each curve.
4. Score each candidate according to its statistical significance.
5. Suppress weak responses using an adaptive detection threshold.
6. Produce the final edge map.

Unlike gradient-based methods, the detector integrates evidence along entire curves, making it much more robust to noise.

---

## Installation

Clone the repository

```bash
git clone https://github.com/NatiOfir/PythonFaintEdgeDetection.git
cd PythonFaintEdgeDetection
```

Install the required packages

```bash
pip install numpy scipy matplotlib opencv-python scikit-image
```

---

## Usage

Example:


Simply run

```bash
FaintEdgeDetection.ipynb
```

---

## Example Results

| Input | Detected Edges |
|-------|----------------|
| noisy image | faint edge map |


---

## Applications

The algorithm has been successfully applied to:

- Medical imaging
- Electron microscopy
- Fluorescence microscopy
- Remote sensing
- Industrial inspection
- Fiber enhancement
- Low-light vision
- Image analysis under severe noise

---

## Citation

If you use this repository in your research, please cite:

```bibtex
@InProceedings{Ofir2016CVPR,
  author = {Ofir, Nati and Galun, Meirav and Nadler, Boaz and Basri, Ronen},
  title = {Fast Detection of Curved Edges at Low SNR},
  booktitle = {Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (CVPR)},
  year = {2016}
}
```

For the extended theoretical analysis, please also cite:

```bibtex
@article{Ofir2019TPAMI,
  author = {Ofir, Nati and Galun, Meirav and Alpert, Sharon and Brandt, Achi and Nadler, Boaz and Basri, Ronen},
  title = {On Detection of Faint Edges in Noisy Images},
  journal = {IEEE Transactions on Pattern Analysis and Machine Intelligence},
  year = {2019}
}
```

---

## Related Publications

- Fast Detection of Curved Edges at Low SNR (CVPR 2016)
- On Detection of Faint Edges in Noisy Images (TPAMI 2019)
- Multi-scale Processing of Noisy Images using Edge Preservation Losses (ICPR 2020)

---

## License

This project is provided for academic and research purposes.

---

## Contact

**Dr. Nati Ofir**

GitHub: https://github.com/NatiOfir

Homepage: https://natiofir.github.io
