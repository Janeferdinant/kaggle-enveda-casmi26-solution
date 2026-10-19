# Enveda CASMI 2026 Molecule ID From Mass Spectra - Kaggle Solution

- **Official Competition:** [enveda-CASMI26-molecule-id-mass-spectra](https://www.kaggle.com/competitions/enveda-CASMI26-molecule-id-mass-spectra)
- **Category:** Featured (Scientific ML)
- **Official Evaluation Metric:** Top-K Hit Rate / Cosine Similarity
- **Solution Architecture:** Multi-Agent Swarm with Gradient Boosting & Ant Colony Optimization (ACO)

## Project Structure

```
kaggle-enveda-casmi26-solution/
├── configs/          # Experiment & hyperparameter YAML configurations
├── data/             # Raw and processed datasets (strictly git-ignored)
├── notebooks/        # EDA and research notebooks
├── src/
│   ├── data/         # Ingestion, validation, and schema profiling
│   ├── features/     # Feature engineering & transformers
│   ├── models/       # Model trainers & cross-validation
│   ├── optimization/ # Ant Colony Optimization (ACO) feature & blend search
│   ├── evaluation/   # Metric computation & submission format auditing
│   └── inference/    # Out-of-fold and test set inference
├── tests/            # Automated unit and integration test suite
├── scripts/          # CLI executables (download, train, validate, submit)
├── submissions/      # Verified prediction artifacts
└── reports/          # Research, CV logs, and ablation reviews
```

## Quick Start

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. Download data via Kaggle API:
   ```bash
   python scripts/download_data.py
   ```
3. Run training & ACO search:
   ```bash
   python scripts/train.py --config configs/baseline.yaml
   ```
4. Validate & generate submission:
   ```bash
   python scripts/generate_submission.py
   ```
