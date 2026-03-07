# Geospatial Machine Learning Workshop

A beginner-friendly Jupyter notebook series covering geospatial data fundamentals, visualization, and machine learning for object detection in satellite and aerial imagery.

## Notebooks

| Notebook | Topics |
|----------|--------|
| [01_geospatial_data_intro.ipynb](notebooks/01_geospatial_data_intro.ipynb) | CRS, vector data, raster data |
| [02_geospatial_visualization_python.ipynb](notebooks/02_geospatial_visualization_python.ipynb) | Raster, vector, and combined visualization |
| [03_geospatial_machine_learning_instance_segmentation.ipynb](notebooks/03_geospatial_machine_learning_instance_segmentation.ipynb) | Mask R-CNN building detection with GeoAI |

## Setup

```bash
# Create and activate a virtual environment (recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter
jupyter notebook notebooks/
```

## Requirements

- Python 3.9+
- Notebooks 01 and 02 use synthetic or local data and run offline
- Notebook 03 requires network access (to download NAIP imagery) and is computationally intensive; training may take 10–60+ minutes depending on hardware

## Project Structure

```
pycon2026/
├── notebooks/           # Jupyter notebooks
├── data/                # Downloaded data and outputs (created on first run)
├── requirements.txt
└── README.md
```

## References

- [GeoAI instance segmentation example](https://opengeoai.org/examples/train_instance_segmentation_model/)
