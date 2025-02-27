This repository contains DNS data for the flow past two square cylinders used in [Lee(2025)](https://doi.org/10.1103/PhysRevFluids.10.024703). This multi-fidelity dataset can be used for uncertainty quantification (UQ) and surrogate modelling exercises.

# Dataset overview
The dataset includes the mean velocity field (both $U_x$ and $U_y$, normalised) from 200 simulations spanning a wide range of input parameters:
- Flow Reynolds number: 37.5 to 62.5
- Cylinder gap spacing parameter ($g^*$): 2.975 to 4.025

There are four datasets available, the high-fidelity data (`HF.mat`), and three sets of low-fidelity data (`LF3.mat`, `LF5.mat` and `LF7.mat`). The HF dataset is designed to achieve a level of accuracy suitable for validation against existing literature. The three LF datasets are generated using a coarser grid and differ based on the polynomial order used in the spectral element method (refer to literature for details).

Each dataset contains `headers` and `data`. The `headers` are in the format `"avg[g*]_[Re]_[Quantity]"`, for example, the first entry `"avg3p5_50p0_x"` represents the x coordinate points for the $g^*=3.5$, $Re=50.0$ case. Below is an example plot generated from one of the cases in LF5.
![Figure 2025-02-25 193143](https://github.com/user-attachments/assets/36e02b1e-e837-4651-9c85-8f301176b3f6)
