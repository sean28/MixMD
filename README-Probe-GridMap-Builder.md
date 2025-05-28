# 🧪 Probe GridMap Builder

**Probe GridMap Builder** is a local web-based software interface designed to analyze molecular dynamics (MD) trajectories in .trr or .nc format, powered by the AMBER cpptraj backend. It enables users to generate grid-based interaction maps between protein structures and solvent probe atoms across dynamic frames. You can use this tool for free by clicking <a href="https://drive.google.com/file/d/14x89Ehda61HUxoY_bQcPqJhTKsd0Zd6R/view?usp=sharing">here</a>. 👉 [Live Demo](https://sean28.github.io/MixMD/probe_gridmap_ui.html)

## ✅ Features

- Upload `.trr` or `.nc` trajectory files
- Grid map generation via `cpptraj`
- Cluster analysis and PDB annotation via `cluster.py`
- Automatic packaging of results (PDB + summary)

## 📦 Conda Environment Setup

```bash

# 1. Extract GridMap_denv.tar.gz 
tar -xzf GridMap_env.tar.gz & cd GridMap_env

# 2. Activate Environment
source bin/activate
```

## 🚀 Run the Server

```bash
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
	
