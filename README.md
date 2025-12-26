## Scientific Context: The Calcium Triplet ($\sigma$)
The **Starlight Synthesis Algorithm** utilizes the **Calcium Triplet (CaT)** region ($8400–8700$ Å) as a primary kinematic indicator for several key reasons:

- **Dust Resilience:** The CaT region is significantly less affected by interstellar dust extinction compared to other common indicators like the Magnesium (Mg) line. 
- **Black Hole Correlation:** Accurate velocity dispersion ($\sigma$) measurements are critical for exploring the **$M_{\bullet}–\sigma$ relation**, helping us understand the co-evolution of central supermassive black holes and their host galaxies.
- **$\Lambda$CDM Framework:** The results support the hierarchical assembly model, reinforcing the Lambda Cold Dark Matter theory of galaxy formation.



## Mathematical Logic
The algorithm treats the observed galaxy spectrum $I(\lambda)$ as a convolution of a template stellar spectrum $T(\lambda)$ with a velocity broadening function $f(v)$.

### 1. Velocity Broadening Function
The broadening is modeled as a Gaussian function where $\sigma$ represents the stellar velocity dispersion:
$$f(v) = \frac{1}{\sigma \sqrt{2\pi}} \exp\left(-\frac{v^2}{2\sigma^2}\right)$$

### 2. Spectral Synthesis Integration
The final modeled spectrum is synthesized using:
$$I(\lambda) = \int T(\lambda') f(v) dv'$$
where $\lambda'$ is the redshifted wavelength and $c$ is the speed of light.

### 3. $\chi^2$ Minimization
To find the most accurate value for $\sigma$, the algorithm minimizes the weighted difference between the observed galaxy spectrum $G(\lambda)$ and the synthetic model $M(\lambda)$:
$$\chi^2 = \sum \left[ \frac{G(\lambda) - M(\lambda)}{\text{error}} \right]^2$$
