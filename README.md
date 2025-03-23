# Complex Networks Analysis - University Activity

## Overview
This repository contains the code and data for the Complex Networks course activity (A1). The goal is to analyze structural properties of synthetic networks (net1-net5) and identify their generative models.

## Project Structure
```
├── data/
│ ├── net1.net
│ ├── net2.net
│ ├── net3.net
│ ├── net4.net
│ ├── net5.net
│ └── positions_net5.net # Spatial coordinates for net5
├── plots/
├── reports/
│ ├── analysis_report.pdf
│ └── GroupXXX_SURNAME1_SURNAME2_A1.pdf
├── .gitignore
├── LICENSE
└── Network_Analysis.ipynb
```

## Activity Overview

### Part 1: Structural Characterization
- Compute metrics for net1-net4:
    - Basic statistics (nodes, edges, degrees)
    - Clustering coefficient
    - Assortativity
    - Path lengths/diameter
- Analyze degree distributions
- Compare node centralities (betweenness, degree, eigenvector)

### Part 2: Network Models
- Identify generative models (ER, WS, BA, CM) for net1-net4
- Analyze net5:
    - Visualize spatial layout
    - Check connectivity
    - Test scale-free/small-world properties
    - Propose generation algorithm

## Code Overview
Key libraries used:
- NetworkX for network analysis
- Matplotlib/Seaborn for visualization
- NumPy/SciPy for metrics calculation

Example workflow in `Network_Analysis.ipynb`:
```python
# Load network
G = nx.read_pajek("data/net1.net")

# Compute metrics
avg_clustering = nx.average_clustering(G)
diameter = nx.diameter(G)
```

## Results
- Full analysis and model identification in `report/GroupXXX_SURNAME1_SURNAME2_A1.pdf`
- Reproducible workflow in `Network_Analysis.ipynb`
- Visualizations (degree distributions, spatial layouts) saved in `images/`

## Usage
1. Clone the repository:
```
git clone https://github.com/marcellorussox/ComplexNets-A1-Analysis.git
cd ComplexNets-A1-Analysis
```
2. Install dependencies:
```
pip install -r requirements.txt # Create this file if missing
```
3. Launch Jupyter Notebook:
```
jupyter notebook
```
4. Run `Network_Analysis.ipynb` for full analysis

## License
Distributed under the MIT License. See [LICENSE](LICENSE) for details.

## Acknowledgments
- Course: Complex Networks (Universitat Rovira i Virgili)
- NetworkX documentation for metric calculations
- 