# Integral Field Spectroscopy (IFU) Galaxy Data Analysis

This repository contains a comprehensive step-by-step Python analysis notebook for **Integral Field Unit (IFU) spectroscopy data** of a galaxy, based on a real FITS data cube. The notebook guides the user through the main techniques of modern extragalactic astronomy: from loading and calibrating the data cube, to extracting spectra, generating images in various bands, mapping emission lines, and deriving the galaxy’s kinematics.

---

## 🌟 Main Objectives

- Understand the structure of IFU (3D) data cubes.
- Explore the spatial and spectral properties of a galaxy.
- Generate and interpret scientific images and spectra from the cube.
- Derive the kinematic properties and rotation curve of the galaxy from emission line analysis.

---

## 📚 Workflow & Key Steps

1. **Loading the FITS Data Cube**
    - Uses `astropy.io.fits` to open and inspect the 3D data cube (Wavelength, Dec, RA).
    - Reads and interprets FITS header information for axis calibration and unit conversions.

2. **Dimension Analysis and Axis Correspondence**
    - Diagnoses axis order and matches header to data array shape.
    - Establishes conventions for wavelength, spatial axes (RA, Dec), and pixel-to-physical conversions.

3. **Visualization at Different Wavelengths**
    - Produces 2D images of the galaxy at selected wavelengths across the cube.
    - Compares galaxy morphology and brightness at different spectral slices.

4. **Extracting Spectra at Selected Pixels**
    - Extracts and plots the spectrum for specific pixels (center vs. outskirts).
    - Visualizes how spectral features and flux vary spatially within the galaxy.

5. **Creating a Moment-0 (White) Image**
    - Integrates the cube along the spectral axis to create a "white light" image.
    - Identifies the galaxy center, compares coordinates with external databases (e.g., NED), and calibrates axes in arcseconds.

6. **Images in Standard Bands and Color Maps**
    - Synthesizes r-band and i-band images by integrating the cube over corresponding filter wavelengths.
    - Creates color maps (e.g., r-i color image) to study stellar population gradients and dust content.

7. **Hα Emission Line Mapping**
    - Constructs continuum-subtracted images around Hα to map ionized gas regions.
    - Identifies star-forming regions and active galactic nuclei (AGN) candidates.

8. **Spectral Analysis and Emission Line Identification**
    - Plots the spectrum in regions rich in ionized gas.
    - Identifies key emission lines (Hα, [NII], [SII], etc.) and fits Gaussian profiles.

9. **Redshift Determination and Kinematic Analysis**
    - Estimates galaxy redshift using the observed wavelengths of emission lines.
    - Calculates velocity fields and derives the galaxy’s rotation curve.

10. **Rotation Curve Derivation**
    - Selects points along the galaxy's major axis.
    - Fits emission lines at those points to obtain radial velocities.
    - Plots and models the rotation curve, including mass profile estimation.

---

## 🧰 Libraries & Dependencies

- `astropy` (fits, wcs, cosmology, stats)
- `numpy`
- `matplotlib`
- `scipy` (optimize, interpolate, ndimage)
- `photutils` (DAOStarFinder)
- `imageio`
- `IPython.display`

Install with:
```bash
pip install astropy numpy matplotlib scipy photutils imageio
