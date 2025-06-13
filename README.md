# IRIS Classification with k-NN

This project implements k-Nearest Neighbors classification for the classic IRIS flower dataset.

## Project Structure

```
iris/
├── data/                    # Raw datasets
│   └── iris.csv            # IRIS dataset (150 samples, 4 features)
├── docs/                   # Documentation and instructions
│   ├── instrucciones.md    # Project instructions (Spanish)
│   ├── practica.txt        # Technical guide
│   └── practica.pdf        # PDF documentation
├── notebooks/              # Jupyter notebooks
│   └── practica.ipynb      # Main analysis notebook
├── outputs/                # Generated outputs
│   ├── figures/            # Visualization outputs
│   │   ├── sepal_scatter.png
│   │   ├── petal_scatter.png
│   │   ├── pairplot_iris.png
│   │   ├── confusion_matrix.png
│   │   └── k_values_comparison.png
│   └── models/             # Trained models (if saved)
├── reports/                # Analysis reports
│   └── reporte_completo_iris.md
├── src/                    # Source code (for future modules)
│   ├── models/             # Model implementations
│   └── utils/              # Utility functions
├── pyproject.toml          # Project dependencies
├── uv.lock                 # Lock file
└── README.md              # This file
```

## Dataset

- **Samples**: 150 iris flowers
- **Features**: 4 measurements (sepal/petal length/width)
- **Classes**: 3 species (Iris-setosa, Iris-versicolor, Iris-virginica)
- **Balance**: 50 samples per class

## Model Performance

- **Algorithm**: k-Nearest Neighbors (k=5)
- **Accuracy**: 100% (30/30 correct predictions on test set)
- **Train/Test Split**: 80/20 (120/30 samples)
- **Cross-validation**: Tested k=1 to k=15

## Key Findings

1. **Petal measurements** are most discriminative features
2. **Iris-setosa** is easily separable from other species
3. **Perfect linear separation** exists in petal feature space
4. **Model robustness** confirmed across different k values

## Usage

```bash
# Navigate to notebooks directory
cd notebooks

# Run the Jupyter notebook
jupyter notebook practica.ipynb
```

## Dependencies

See `pyproject.toml` for complete dependency list. Main requirements:
- pandas
- scikit-learn
- matplotlib
- seaborn
- jupyter