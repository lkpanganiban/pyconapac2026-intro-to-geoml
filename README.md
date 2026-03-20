# Geospatial Machine Learning Workshop

A beginner-friendly Jupyter notebook series covering geospatial data fundamentals, visualization, and machine learning for object detection in satellite and aerial imagery.

## Notebooks


| Notebook                                                                                                                           | Topics                                                               |
| ---------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------- |
| [01_geospatial_data_intro.ipynb](notebooks/01_geospatial_data_intro.ipynb)                                                         | CRS, vector, raster, spatial extent, basemaps; leafmap visualization |
| [02_geospatial_visualization_python.ipynb](notebooks/02_geospatial_visualization_python.ipynb)                                     | Raster, vector, combined, and 3D visualization with leafmap          |
| [03_geospatial_machine_learning_semantic_segmentation.ipynb](notebooks/03_geospatial_machine_learning_semantic_segmentation.ipynb) | U-Net semantic segmentation (building detection) with GeoAI          |
| [04_synthesis.ipynb](notebooks/04_synthesis.ipynb)                                                                                  | End-to-end project: River encroachment analysis combining all concepts |


## Prerequisites: Install Miniconda (conda)

This project uses [conda](https://docs.conda.io/) for environment management. If you don't have conda installed, install [Miniconda](https://www.anaconda.com/docs/getting-started/miniconda/install) for your platform:

### Windows (PowerShell)

```powershell
Invoke-WebRequest -Uri "https://repo.anaconda.com/miniconda/Miniconda3-latest-Windows-x86_64.exe" -OutFile ".\miniconda.exe"
Start-Process -FilePath ".\miniconda.exe" -ArgumentList "/S" -Wait
del .\miniconda.exe
```

Then open **Anaconda Prompt** from the Start Menu to use conda.

### macOS

**Apple Silicon (M1/M2/M3):**

```bash
mkdir -p ~/miniconda3
curl https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-arm64.sh -o ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
rm ~/miniconda3/miniconda.sh
source ~/miniconda3/bin/activate
conda init --all
```

**Intel Mac:** Replace `MacOSX-arm64.sh` with `MacOSX-x86_64.sh` in the URL. See the [Miniconda archive](https://repo.anaconda.com/miniconda/) for available installers.

### Linux (x86_64)

```bash
mkdir -p ~/miniconda3
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh -O ~/miniconda3/miniconda.sh
bash ~/miniconda3/miniconda.sh -b -u -p ~/miniconda3
rm ~/miniconda3/miniconda.sh
source ~/miniconda3/bin/activate
conda init --all
```

After installing, close and reopen your terminal (or run `source ~/.bashrc` or `source ~/.zshrc`). For full installation options and troubleshooting, see [Installing Miniconda](https://www.anaconda.com/docs/getting-started/miniconda/install).

---

## Setup

```bash
# Create and activate a conda environment (recommended)
conda create -n pythonasia2026 python=3.11
conda activate pythonasia2026

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter
jupyter notebook notebooks/
```

## Requirements

- Python 3.12+
- Notebooks 01 and 02 use synthetic or local data and run offline
- Notebook 03 requires network access (to download NAIP imagery) and is computationally intensive; training may take 10–60+ minutes depending on hardware

## Project Structure

```
pythonasia2026-intro-to-geoml/
├── notebooks/           # Jupyter notebooks
├── data/                # Downloaded data and outputs (created on first run)
├── requirements.txt
└── README.md
```

## References

- [GeoAI semantic segmentation example](https://opengeoai.org/examples/train_segmentation_model/)

