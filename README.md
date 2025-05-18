# IFU_Angel: Integral Field Spectroscopy Analysis Pipeline

This repository contains a complete data analysis workflow for **Integral Field Spectroscopy (IFU)** applied to galaxies, written in Python and executed in JupyterLab. The pipeline explores a real spectral cube of a galaxy, guiding the user through each step — from loading the FITS data to deriving the rotation curve and mass profile.

 **Author**: Ángel Encinas  
 **Version**: 1.0  
 **Documentation**: Built with [Sphinx](https://www.sphinx-doc.org/), available at  
 https://angelphysics.github.io/IFU_Angel/ *(if GitHub Pages is enabled)*

---

##  Features

The project includes:

###  Part 1: IFU Cube Exploration
- FITS data cube loading and inspection
- Axis identification and slicing
- Monochromatic galaxy images across wavelengths
- Interactive spectra visualization from selected pixels
- Generation of a **Moment-0 (white)** image
- r-band, i-band, and r−i color imaging
- **Hα emission map** (continuum-subtracted)
- **Redshift estimation** from spectra

###  Part 2: Galaxy Kinematics
- Manual selection of spaxels along the galaxy's **major axis**
- Extraction and analysis of spectra at key positions
- Calculation of **rotation velocities**
- Plotting and **fitting of the rotation curve**
- Derivation of rotation curves from **visible mass profiles**

---

## Installation

You can recreate the environment in two ways:

### Option 1: Using `conda` (recommended)

```bash
git clone https://github.com/AngelPhysics/IFU_Angel.git
cd IFU_Angel
conda env create -f environment.yml
conda activate envAstro1
jupyter lab
