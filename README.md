# Phase Transition: Percolation and the 2D Ising Model

A computational study of phase transitions through two canonical models:

- **Site percolation:** Monte Carlo estimation of the critical threshold using a Union-Find data structure.
- **2D Ising model:** Gibbs sampling across inverse temperatures, with analyses of spin configurations, magnetization, energy, and critical behavior.

This project was completed for *Probability Theory and Statistics for EECS* at ShanghaiTech University by **Li Jianhao, Li Yiming, and Wu Zihan**.

## Highlights

- Estimates the square-lattice site-percolation threshold at approximately `0.592`, close to the reference value `0.592746`.
- Studies finite-size effects and convergence across multiple lattice sizes.
- Simulates the 2D Ising model with periodic boundary conditions and heat-bath/Gibbs updates.
- Visualizes equilibrium configurations and thermodynamic observables around the phase transition.

## Repository contents

```text
.
|-- Phase_Transition.ipynb   # Complete executable analysis
|-- Phase_Transition.pdf     # Final rendered report
|-- Phase_Transition.tex     # LaTeX source of the report
|-- images/                  # Figures used by the report
|-- requirements.txt         # Python dependencies
`-- README.md
```

## Quick start

Python 3.10 or newer is recommended.

```bash
git clone https://github.com/<your-username>/<repository-name>.git
cd <repository-name>
python -m venv .venv
```

Activate the environment:

```bash
# Windows PowerShell
.venv\Scripts\Activate.ps1

# macOS/Linux
source .venv/bin/activate
```

Then install the dependencies and open the notebook:

```bash
python -m pip install -r requirements.txt
jupyter lab Phase_Transition.ipynb
```

Some simulations are computationally intensive. To test the code quickly, reduce the lattice size, number of trials, burn-in sweeps, or sampling sweeps in the relevant cells.

## Methods

For percolation, sites are opened in uniformly random order. A Union-Find structure with virtual top and bottom nodes detects the first spanning cluster. Repeating the experiment yields the threshold distribution and its Monte Carlo estimate.

For the Ising model, each spin is updated from its conditional Gibbs distribution given its four nearest neighbors. Measurements after burn-in are used to examine equilibrium magnetization, energy, and their temperature dependence.

## Report

The complete methodology, derivations, results, and discussion are available in [Phase_Transition.pdf](Phase_Transition.pdf).

## License

Copyright remains with the three authors. No reuse license is granted yet. Because this is a collaborative work, an open-source license should be added only after all authors agree; MIT or BSD-3-Clause would be reasonable options for the code.

---

中文简介：本项目通过渗流模型和二维 Ising 模型研究相变现象，使用 Monte Carlo、Union-Find 和 Gibbs Sampling 完成数值模拟，并分析临界点、有限尺寸效应、磁化强度和能量等统计性质。
