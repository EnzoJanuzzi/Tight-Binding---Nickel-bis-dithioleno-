# Electronic Structure of 2D Nickel Bis(dithiolene) via Tight-Binding

![Language](https://img.shields.io/badge/Language-Python-blue) ![Physics](https://img.shields.io/badge/Physics-Condensed%20Matter-green) ![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

## 📄 Overview

This project investigates the electronic properties of **Nickel bis(dithiolene)**, a two-dimensional Metal-Organic Framework (MOF) with a honeycomb-like hexagonal lattice. Using the Tight-Binding (TB) approximation, we calculate the electronic band structure of the pure material and analyze the effects of symmetry breaking via **Palladium (Pd) doping**.

The study demonstrates how substituting Ni atoms with Pd (isoelectronic but different orbital energies) lifts degeneracy at high-symmetry points, effectively opening a band gap and altering the material's conductivity.

## 🧪 Methodology

The simulation uses the `pythtb` library to construct the Hamiltonian of the system based on the following parameters derived from literature:

* **Lattice:** 2D Hexagonal (Triangular) lattice ($a = 1.41$).
* **Basis:** Kagome-like arrangement with 3 metal sites per unit cell.
* **Hamiltonian:** Nearest-neighbor hopping model.

### Physical Parameters
| Parameter | Symbol | Value (eV) | Description |
| :--- | :---: | :---: | :--- |
| **Hopping** | $t$ | $-1.0$ | Interaction between neighboring metal sites |
| **On-site (Ni)** | $\varepsilon_{Ni}$ | $0.0$ | Energy level of Nickel $d$-orbitals |
| **On-site (Pd)** | $\varepsilon_{Pd}$ | $-1.0$ | Energy level of Palladium dopant |

## 🕸️ Lattice Structure

The unit cell is modeled as a three-site basis on a hexagonal lattice.


[Image of kagome lattice unit cell]


* **Pure System:** Sites 0, 1, and 2 are all Nickel ($\varepsilon = 0$).
* **Doped System:** Specific sites are assigned the on-site energy of Palladium ($\varepsilon = -1$) to simulate symmetry breaking.

## 📊 Results

### 1. Pure Ni-MOF
The band structure of the pure system reveals:
* A **Flat Band** (top) indicating localized states with infinite effective mass ($m^* \to \infty$).
* Two **Dispersive Bands** (middle/bottom) behaving as electron-like and hole-like carriers.
* **Degeneracy** at the $K$ and $M$ points, characteristic of the hexagonal symmetry.

### 2. Pd-Doped Variants
Introduction of Pd atoms breaks the rotational/inversion symmetry of the basis.
* **Effect:** The degeneracy at the $M$ point is lifted.
* **Consequence:** A **Band Gap** opens between the valence and conduction bands, marking a transition from a semi-metallic to a semiconducting behavior.

*(Note: See the `notebooks/` directory for generated plots).*

## 🚀 Usage

### Dependencies
* Python 3.x
* `matplotlib`
* `pythtb`

### Running the Simulation
1.  Clone the repository:
    ```bash
    git clone [https://github.com/yourusername/Ni-MOF-Tight-Binding.git](https://github.com/yourusername/Ni-MOF-Tight-Binding.git)
    ```
2.  Install requirements:
    ```bash
    pip install pythtb matplotlib
    ```
3.  Run the Jupyter Notebook:
    ```bash
    jupyter notebook "Projeto Mat Cond.ipynb"
    ```

## 📚 References

1.  **Problem Source:** *Chern insulator with a nearly flat band in the metal-organic-framework-based Kagome lattice*, Scientific Figure on ResearchGate.
2.  **Material Reference:** Kambe, T., et al. (2013). *π-Conjugated Nickel Bis(dithiolene) Complex Nanosheet*. J. Am. Chem. Soc., 135(7), 2462–2465.

## 👤 Author

**Enzo Januzzi Xavier**
* Ilum School of Science (CNPEM)
* Condensed Matter Physics Course
