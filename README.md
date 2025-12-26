# Starlight Synthesis Algorithm

[![DOI](https://img.shields.io/badge/DOI-10.4236%2Fijaa.2022.121005-blue)](https://doi.org/10.4236/ijaa.2022.121005)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

This repository contains the algorithmic implementation of the stellar spectral synthesis method described in the research paper:  
**"Formation and Evolution of Galaxies: Starlight Synthesis Algorithm"** (Barua, 2022).

## Research Overview
The algorithm facilitates the kinematic study of galaxies by analyzing the absorption lines of the **calcium triplet (CaT)** ($8400–8700$ Å). This spectral region is utilized to calculate precise velocity dispersions ($\sigma$), which serve as a proxy for understanding the mass of central black holes ($M_{\bullet}$) and the overall evolution of galactic structures under the $\Lambda$CDM model.

## Scientific Context: The Calcium Triplet ($\sigma$)
The **Starlight Synthesis Algorithm** utilizes the CaT region as a primary kinematic indicator for several key reasons:

* **Dust Resilience:** The CaT region is significantly less affected by interstellar dust extinction compared to other common indicators like the Magnesium (Mg) line.
* **Black Hole Correlation:** Accurate velocity dispersion ($\sigma$) measurements are critical for exploring the **$M_{\bullet}–\sigma$ relation**, helping us understand the co-evolution of central supermassive black holes and their host galaxies.
* **$\Lambda$CDM Framework:** The results support the hierarchical assembly model, reinforcing the Lambda Cold Dark Matter theory of galaxy formation.

## Mathematical Logic
The algorithm treats the observed galaxy spectrum $I(\lambda)$ as a convolution of a template stellar spectrum $T(\lambda)$ with a velocity broadening function $f(v)$.

### 1. Velocity Broadening Function
The broadening is modeled as a Gaussian function where $\sigma$ represents the stellar velocity dispersion:
$$f(v) = \frac{1}{\sigma \sqrt{2\pi}} \exp\left(-\frac{v^2}{2\sigma^2}\right)$$

### 2. Spectral Synthesis Integration
The final modeled spectrum is synthesized using the integration of the template spectrum and the broadening function:
$$I(\lambda) = \int T(\lambda') f(v) dv'$$

### 3. $\chi^2$ Minimization
To find the most accurate value for $\sigma$, the algorithm minimizes the weighted difference between the observed galaxy spectrum $G(\lambda)$ and the synthetic model $M(\lambda)$:
$$\chi^2 = \sum \left[ \frac{G(\lambda) - M(\lambda)}{\text{error}} \right]^2$$

## Citation
If you utilize this algorithm in your research, please cite the following publication:

> Barua, N. (2022). Formation and Evolution of Galaxies: Starlight Synthesis Algorithm. *International Journal of Astronomy and Astrophysics*, 12, 68-93. doi: [10.4236/ijaa.2022.121005](https://doi.org/10.4236/ijaa.2022.121005).

### BibTeX Reference
```bibtex
@article{barua2022starlight,
  title={Formation and Evolution of Galaxies: Starlight Synthesis Algorithm},
  author={Barua, Nick},
  journal={International Journal of Astronomy and Astrophysics},
  volume={12},
  number={1},
  pages={68--93},
  year={2022},
  publisher={Scientific Research Publishing},
  doi={10.4236/ijaa.2022.121005}
}
### 3. Creating the Metadata Files
To ensure your repository is fully academic and functional, add these two separate files to your root folder:

#### **File 1: `CITATION.cff`**
This creates a "Cite this repository" button on your GitHub sidebar.
```yaml
cff-version: 1.2.0
message: "If you use this algorithm, please cite it as follows."
authors:
- family-names: "Barua"
  given-names: "Nick"
  orcid: "https://orcid.org/0000-0003-4641-0112"
title: "Starlight Synthesis Algorithm"
version: 1.0.0
doi: 10.4236/ijaa.2022.121005
date-released: 2022-03-03
url: "https://github.com/Nick-Barua/starlight-synthesis-algorithm"
