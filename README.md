# AI-Based-SHM-Framework
**Condition-aware AI framework for automated structural health monitoring**

This repository provides the executable releases of a three-module Structural Health Monitoring (SHM) framework developed as part of an advanced research program on vibration-based damage detection and localization.

The toolkit includes:

**Module 1: Automated Modal Identification (SSI-Cov / FSDD)**

**Module 2: Condition-Aware Anomaly Detection using a Conditional Variational Autoencoder (CVAE)**

**Module 3: Signal-Domain Verification and Damage Localization (SSA + OC-SVM)**

All modules are provided as stand-alone Windows executables, requiring no Python installation or dependencies.
Each tool includes representative sample datasets to ensure reproducibility of the results reported in the corresponding scientific study.

--------------------------------------------------

# Module 1 — Automated Modal Identification

Performs operational modal analysis using:

- Stochastic Subspace Identification (SSI-Cov)
- Frequency Domain Decomposition (FDD)
- Frequency–Spatial Domain Decomposition (FSDD)
- Automated stable-pole selection using Isolation Forest
- Prominence-based peak detection in modal PSDs

Input: Raw acceleration time series
Output: Natural frequencies and mode shapes
--------------------------------------------------

# Module 2 — CVAE-Based Condition-Aware Anomaly Detection

Implements a Conditional Variational Autoencoder trained on:

- Natural frequencies
- Temperature
- Time-of-day conditions

The CVAE reconstructs the expected healthy response under given environmental conditions.
Anomaly is quantified via MAPE and classified into:
- Healthy, Moderate, Significant, Critical.

- Input: Natural frequencies
- Output: Reconstructed frequencies + anomaly score

--------------------------------------------------

# Module 3 — Damage Localization (SSA + OC-SVM)

A signal-domain verification module applied after anomaly detection.
Each sensor’s detrended and SSA-processed acceleration signal is evaluated using an OC-SVM trained on healthy data.

Outputs include:
- Per-sensor anomaly scores
- Damage probability distribution
- Damage localization map

- Input: Raw acceleration of healthy/damaged structures
- Output: Damage zone and severity classification

--------------------------------------------------

# Executable Releases

All three modules are published under GitHub “Releases.”
Each release includes:

- The executable file
- Sample datasets
- User manual (within README)

--------------------------------------------------

# License

This release is provided for academic research and non-commercial use only.

