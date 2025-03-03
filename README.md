# MLOps with DVC

## Overview
This repository demonstrates **MLOps (Machine Learning Operations) practices using DVC (Data Version Control)** for efficient experiment tracking, dataset versioning, and model reproducibility. The project follows best practices to streamline the ML workflow with **DVC, Git, and CI/CD pipelines**.

## Features
- **Data Versioning:** Track dataset changes efficiently using DVC.
- **Pipeline Management:** Automate ML pipelines using DVC stages.
- **Experiment Tracking:** Compare different models and hyperparameters.
- **Reproducibility:** Ensure consistent model training and evaluation.
- **Collaboration:** Seamless integration with Git for team-based workflows.

## Project Structure
```
MLOps-DVC/
│── data/                 # Data directory (managed by DVC)
│── src/                  # Source code for model training & evaluation
│── models/               # Trained model storage (DVC-tracked)
│── dvc.yaml              # DVC pipeline definition
│── dvc.lock              # Auto-generated DVC lock file
│── .gitignore            # Ignore unnecessary files in Git
│── .dvcignore            # Ignore unnecessary files in DVC
│── README.md             # Project documentation
```

## Setup & Installation
1. **Clone the Repository**
   ```bash
   git clone https://github.com/udaygupta8899/MLOps-DVC.git
   cd MLOps-DVC
   ```

2. **Create a Virtual Environment & Install Dependencies**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   pip install -r requirements.txt
   ```

3. **Initialize DVC & Pull Data**
   ```bash
   dvc init
   dvc pull
   ```

## Running the Pipeline
Run the entire ML pipeline with DVC:
```bash
dvc repro
```
This will execute all defined pipeline stages, including data preprocessing, model training, and evaluation.

## Tracking Experiments
To track different model experiments:
```bash
dvc exp run
```
To compare experiments:
```bash
dvc exp show
```

## Contributing
Feel free to contribute! Fork the repo, make changes, and submit a pull request.

## License
This project is open-source and available under the [MIT License](LICENSE).
