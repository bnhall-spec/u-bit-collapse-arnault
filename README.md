# U-Bit Collapse in Arnault Composites

This repository contains the paper and dataset accompanying the arXiv preprint:

**U-Bit Collapse in Arnault Composites: Probing the Boundary of Strong Lucas Pseudoprimes**  
Bowman Hall, January 2026

---

## Overview

This work presents a large-scale computational study of composite integers constructed using the Arnault framework and engineered to pass multiple Miller–Rabin primality tests (through base 11). The study investigates whether such composites exhibit any measurable progress toward evading the strong Lucas probable prime test, a core component of the Baillie–PSW primality test.

To quantify deviation from expected Lucas sequence behavior, the paper introduces the **U-bit collapse metric**  
\[
\delta = \log_2 n - \log_2(U_d \bmod n),
\]
where \( n + 1 = d \cdot 2^s \) with \( d \) odd.

Across 200 Miller–Rabin–resistant composites of approximately 350 bits, no significant Lucas collapse is observed. All samples fail the strong Lucas test, with collapse values concentrated near zero, providing empirical evidence for the orthogonality of the Miller–Rabin and Lucas components of Baillie–PSW.

---

## Repository Contents

paper/
U-bit_Collapse_in_Arnault_Composites.pdf
U-bit_Collapse_in_Arnault_Composites.tex
figures/
figure1.pdf
figure2.pdf
figure3.pdf

data/
composites_data.json

### `paper/`
Contains the PDF and LaTeX source of the paper, along with the exact figure files used in the manuscript.

### `data/`
Contains the complete dataset of 200 composites analyzed in the study.

---

## Dataset Description

The file `data/composites_data.json` provides full information for each composite analyzed, including:

- The composite integer \( n \)
- Full prime factorization \( n = p_1 p_2 p_3 \)
- Composite bit-size
- Arnault construction parameters \( k \) and \( M \)
- Selected Lucas discriminant \( D \)
- Value of \( U_d \bmod n \)
- U-bit collapse metric \( \delta \)
- Prime residue classes modulo 35
- Miller–Rabin bases passed (through base 11)

All summary statistics, distributions, correlations, and figures reported in the paper are derived solely from this dataset.

---

## Reproducibility

The dataset provided here is sufficient to independently verify:

- The distribution of U-bit collapse values
- Reported summary statistics (mean, median, extrema)
- Correlation coefficients with construction parameters
- Residue class frequency analysis

The definitions of all computed quantities are fully specified in the paper.

---

## Code Availability

Source code used for composite construction, Miller–Rabin filtering, Lucas testing, and statistical analysis is **not included in this repository at this time**.

The released dataset contains all intermediate values required to verify the numerical results and figures reported in the paper. Code may be released in a future version of this repository.

---

## Experimental Environment

The composites analyzed were generated using a high-throughput Arnault-based construction process executed on a single-core AWS Graviton instance (`c7g.medium`). Approximately 7,700 Carmichael numbers were generated per minute, with Miller–Rabin–base-11-resistant composites occurring at a rate of approximately 20 per hour.

---

## Citation

If you use this data or refer to this work, please cite the arXiv preprint:

> Bowman Hall, *U-Bit Collapse in Arnault Composites: Probing the Boundary of Strong Lucas Pseudoprimes*, arXiv, 2026.

---

## License

The paper and dataset are released for academic and research use.  
(Insert specific license here if desired.)
