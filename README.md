# Deformation Field Consistency: ANTs vs. map_coordinates

## Description
This repository demonstrates that applying a deformation field is a deterministic process, producing identical results regardless of whether the `ANTs` library or the `map_coordinates` function from `scipy.ndimage` is used. The consistency of the process is verified by computing the normalized cross-correlation (NCC), which results in a value of 1, indicating perfect agreement.

## Repository Structure
- `deformation_demo.ipynb` — Google Colab Notebook with the full demonstration.
- `warp.nii` — Sample displacement field.
- `mri.nii.gz` — Sample image to be deformed.


## How to Use
1. **Open the Google Colab Notebook**  
   - Clone the repository and open the notebook locally, or upload it directly to [Google Colab](https://colab.research.google.com).

2. **Prepare the Required Files**  
   - Use the provided `.nii.gz` files for the deformation demonstration.
   - Either upload them manually during the session or mount your Google Drive within Colab.

3. **Run the Notebook**  
   - Follow the instructions in the notebook to apply the deformation using both `ANTs` and `map_coordinates`.
   - Verify that the NCC result is 1, confirming the deterministic behavior of the process.

## Requirements
- Python 3.x
- [ANTsPy](https://github.com/ANTsX/ANTsPy)
- [SciPy](https://www.scipy.org/) (specifically, the `scipy.ndimage` module)
- [Nibabel](https://nipy.org/nibabel/) (for handling `.nii` files)

