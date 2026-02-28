# Formation and Evolution of Galaxies: Starlight Synthesis Algorithm

[![License: Apache 2.0](https://img.shields.io/badge/License-Apache_2.0-blue?style=flat-square)](https://opensource.org/licenses/Apache-2.0)
[![Journal: IJAA](https://img.shields.io/badge/Journal-IJAA_SCIRP-blue?style=flat-square)](https://www.scirp.org/journal/ijaa)
[![DOI](https://img.shields.io/badge/DOI-10.4236%2Fijaa.2022.121005-blue?style=flat-square)](https://doi.org/10.4236/ijaa.2022.121005)
[![Published](https://img.shields.io/badge/Published-March_2022-green?style=flat-square)](https://www.scirp.org/journal/paperinformation?paperid=115643)
[![ORCID](https://img.shields.io/badge/ORCID-0000--0003--4641--0112-A6CE39?style=flat-square&logo=orcid&logoColor=white)](https://orcid.org/0000-0003-4641-0112)

> **Author:** Dr. Nick Barua · AN Holdings Co., Nishinomiya City, Hyogo, Japan
> **Published:** *International Journal of Astronomy and Astrophysics (IJAA)*, Vol. 12, No. 1, pp. 68–93, March 2022
> **DOI:** [10.4236/ijaa.2022.121005](https://doi.org/10.4236/ijaa.2022.121005)
> 📄 **Downloads:** 392 · **Views:** 2,405

---

## 📌 Abstract

This study addresses the resurgence of interest in precise **stellar velocity dispersion (σ)** measurements for the study of galactic and active nuclei kinematics. Using the **absorption lines of the Calcium Triplet (CaT)** at 8498.02, 8542.09, and 8662.14 Å — a spectral region relatively free from complications — the paper investigates the empirical relationship between the mass of the central black hole (M•) and σ.

The **Starlight Synthesis Algorithm** is applied to **354,992 galaxies** from the Sloan Digital Sky Survey (SDSS) database, delivering unprecedented insights into galactic stellar populations, star formation histories, and AGN host properties.

**Keywords:** Galaxies · Physics · Nuclei Kinematics · Galactic Nuclei · Active Nuclei · Velocity Dispersion

---

## 🔬 Key Scientific Contributions

- Application of the **Starlight Synthesis Algorithm** to 354,992 SDSS galaxies
- Precise **stellar velocity dispersion (σ)** measurements via Calcium Triplet absorption lines
- Investigation of the **M•–σ relationship** (black hole mass vs. velocity dispersion)
- **Automated mask detection** for spectral synthesis optimization
- Spatially resolved spectra for a sub-sample of **34 galaxies**
- Star formation history as a function of **stellar mass** for both AGNs and NSFGs
- BPT diagnostic diagrams distinguishing AGN host galaxies from normal star-forming galaxies

---

## 🧮 Mathematical Framework

### 1. Starlight Synthesis Model

The observed spectrum is modeled as a convex combination of base elements:
```
Mλ = Mλ₀ · [ Σⱼ xⱼ · Tⱼ,λ · rλ ] ⊗ G(v*, σ*)
```

where:
- **Mλ** — synthetic spectrum
- **Mλ₀** — normalization factor at wavelength λ₀
- **Tⱼ,λ** — spectrum of the j-th base component
- **xⱼ** — fractional contribution of each base component
- **rλ ≡ 10^(−0.4·(Aλ − Aλ₀))** — dust extinction term
- **G(v\*, σ\*)** — Gaussian distribution of line-of-sight velocities
- **⊗** — convolution operator

### 2. Chi-Squared Minimization

The best fit minimizes χ² between the observed and synthetic spectra:
```
χ² = Σλ [ (Oλ − Mλ) · wλ ]²
```

where **wλ** is the inverse of the noise in Oλ. The **Metropolis algorithm** with simulated annealing prevents convergence to local minima.

### 3. Doppler Broadening

Stellar velocity dispersion is inferred from spectral line broadening:
```
Δλ ≈ (λ₀ · σ) / c
```

where λ₀ is the central wavelength and c is the speed of light.

---

## 📊 Dataset & Observations

| Parameter | Details |
| :--- | :--- |
| **Database** | Sloan Digital Sky Survey (SDSS) |
| **Sample Size** | 354,992 galaxies |
| **Spectral Range** | 3,800–9,200 Å (resolution λ/Δλ ~ 1,800) |
| **CaT Region** | 8,498.02 · 8,542.09 · 8,662.14 Å |
| **Spatially Resolved Sub-sample** | 34 galaxies |
| **Observatory Sample** | 80 spectra from 78 galaxies |
| **Telescopes Used** | KPNO Mayall 4m · KPNO 2.1m · ESO-La Silla 1.52m |

### Sample Composition

| Galaxy Type | Count |
| :--- | :---: |
| Seyfert Type 2 | 43 |
| Seyfert Type 1 | 26 |
| Non-active Galaxies | 9 |
| **Total** | **78** |

---

## 🌌 Key Findings

- **Downsizing confirmed:** More massive galaxies form stars earlier than less massive galaxies
- **Star formation rate** has been declining for ~6 billion years
- **AGN–NSFG distinction:** High-luminosity AGNs (L[O III] > 10⁷ L☉) show significantly younger stellar populations
- **M•–σ relationship** validated across Seyfert 1 & 2 galaxies
- Velocity dispersion uncertainty (Δσ) of ~8 km/s for individual masks; ~5 km/s for quality 'a' spectra
- **Faber-Jackson relation** for Seyfert galaxies: n ~ 2.7 (vs. n ~ 3–4 for normal galaxies)

---

## 🔭 Methodology Overview
```
SDSS Database (354,992 galaxies)
         ↓
Automated Mask Detection
         ↓
Starlight Spectral Synthesis
         ↓
Calcium Triplet Analysis (8498–8662 Å)
         ↓
Velocity Dispersion (σ) Measurement
         ↓
M•–σ Relationship & BPT Diagnostics
         ↓
Star Formation History Recovery
```

---

## 📂 Repository Structure

| File / Folder | Description |
| :--- | :--- |
| `src/` | Core Starlight synthesis algorithm implementation |
| `data/` | Sample spectral data and SDSS query scripts |
| `figures/` | Faber-Jackson plots, BPT diagrams, χ² curves |
| `notebooks/` | Jupyter notebooks for analysis and visualization |
| `requirements.txt` | Python dependencies |
| `CITATION.cff` | Machine-readable citation file |
| `README.md` | Project documentation |

---

## 🚀 Getting Started
```bash
git clone https://github.com/Nick-Barua/starlight-synthesis-algorithm.git
cd starlight-synthesis-algorithm
pip install -r requirements.txt
```

---

## 🔗 Related Publications

| # | Title | Venue | Field |
| :---: | :--- | :---: | :--- |
| **1** | **Formation and Evolution of Galaxies: Starlight Synthesis Algorithm** *(this repo)* | IJAA | Astrophysics |
| 2 | [Unveiling Galactic Assembly: Chemo-Kinematic Insights from Stellar Absorptions](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=5343246) | SSRN | Astrophysics |
| 3 | [Galactic Paleontology: Reconstructing Accretion Events with Chemo-Dynamical Signatures](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=5427474) | SSRN | Astrophysics |

---

## 📝 Citation
```bibtex
@article{barua2022starlight,
  author    = {Barua, Nick},
  title     = {Formation and Evolution of Galaxies: Starlight Synthesis Algorithm},
  journal   = {International Journal of Astronomy and Astrophysics},
  volume    = {12},
  number    = {1},
  pages     = {68--93},
  year      = {2022},
  month     = {March},
  doi       = {10.4236/ijaa.2022.121005},
  url       = {https://doi.org/10.4236/ijaa.2022.121005},
  publisher = {Scientific Research Publishing}
}
```

---

## 📜 License

This project is licensed under the **Apache 2.0 License** — see the [LICENSE](LICENSE) file for details.
