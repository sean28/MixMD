# 🧪 Probe GridMap Builder

**Probe GridMap Builder** is a local web-based software interface designed to analyze molecular dynamics (MD) trajectories in .trr or .nc format, powered by the AMBER cpptraj backend. It enables users to generate grid-based interaction maps between protein structures and solvent probe atoms across dynamic frames. You can use this tool for free by clicking <a href="https://drive.google.com/file/d/14x89Ehda61HUxoY_bQcPqJhTKsd0Zd6R/view?usp=sharing">here</a>. 👉 [Live Demo](https://sean28.github.io/MixMD/probe_gridmap_ui.html)

## ✅ Features

- Upload `.trr` or `.nc` trajectory files
- Grid map generation via `cpptraj`
- Cluster analysis and PDB annotation via `cluster.py`
- Automatic packaging of results (PDB + summary)

## 📦 Conda Environment Setup

This project is designed to run inside a Conda environment with **AmberTools** and **Flask**.

You can create the environment with the following steps:

```bash
# 1. Create a new environment
conda create -n amber python=3.12

# 2. Activate the environment
conda activate amber

# 3. Install required packages
conda install -c conda-forge ambertools flask pandas matplotlib scikit-learn parmed

# 4. Install additional pip packages
pip install pytraj amberutils sander pdb4amber packmol-memgen

```

Alternatively, you can run the downloaded environment (GridMap_env.tar.gz) by following these steps:

```bash
# 1. Extract GridMap_denv.tar.gz 
tar -xzf GridMap_env.tar.gz

# 2. Activate Environment
cd GridMap_env
source bin/activate

# 3. Run Probe GridMap Builder
python probe-gridmap.py

# 4. Open local browser
http://127.0.0.1:8082

```
## 🚀 Run the Server

```
conda activate amber
python probe-gridmap.py

```
open the http://127.0.0.1:8082 

## 📝 Usage

1. Upload your .trr or .nc trajectory file via the web interface.
2. Upload the corresponding .pdb file and choose probe atoms.
3. Submit the job, and download the result ZIP containing:
	•	nonortho.pdb
	•	nonortho_mark.pdb
	•	cluster_summary.txt
	
