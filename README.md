# Kidney Disease Classification using MLflow and DVC

This repository demonstrates a machine learning pipeline for classifying kidney disease, utilizing [MLflow](https://mlflow.org/) for experiment tracking and [DVC](https://dvc.org/) (Data Version Control) for data and model management. The goal is to build a reproducible and scalable workflow for kidney disease classification based on clinical features.


## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Running the Project](#running-the-project)
- [Project Structure](#project-structure)
- [Usage](#usage)
  - [Training](#training)
  - [Experiment Tracking](#experiment-tracking)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)

## Project Overview

Kidney disease is a significant public health issue that can be addressed through early diagnosis using machine learning models. This project aims to develop a classification model that predicts the presence of kidney disease from patient data.

The workflow includes:
- Data preprocessing and feature engineering.
- Model training and hyperparameter tuning.
- Experiment tracking using MLflow.
- Data and model versioning using DVC.

## Features

- **MLflow**: Track experiments, log metrics, and save models.
- **DVC**: Manage datasets and model versions efficiently.
- **Scikit-learn**: Used for building machine learning models.
- **Automated Workflow**: From data ingestion to model evaluation.
- **Docker Support**: Containerized environment for consistency.

## Getting Started

### Prerequisites

Ensure you have the following installed:

- [Python 3.8+](https://www.python.org/downloads/)
- [Git](https://git-scm.com/)
- [DVC](https://dvc.org/doc/install)
- [MLflow](https://mlflow.org/docs/latest/installation.html)

### Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/imanoop7/Kidney-Disease-classification-using-mlflow-and-DVC.git
    cd Kidney-Disease-classification-using-mlflow-and-DVC
    ```

2. Create and activate a virtual environment:
    ```sh
    python3 -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install the dependencies:
    ```sh
    pip install -r requirements.txt
    ```

4. Pull the data files using DVC:
    ```sh
    dvc pull
    ```

### Running the Project

To run the project, follow these steps:

1. Start the MLflow tracking server (optional):
    ```sh
    python app.py
    ```

## Project Structure
    ```plaintext
    ├── data/                   # Dataset and DVC files
    ├── src/                    # Source code
    │   ├── data_preprocessing.py
    │   ├── train.py
    │   ├── evaluate.py
    │   └── utils.py
    ├── models/                 # Saved models
    ├── notebooks/              # Jupyter notebooks
    ├── dvc.yaml                # DVC pipeline
    ├── params.yaml             # Parameters configuration
    ├── requirements.txt        # Python dependencies
    ├── README.md               # Project documentation
    └── .gitignore              # Git ignore file
    ```

## Usage 
### Training
Run the training script to train the machine learning model:
    ```bash
    python main.py
    
## Experiment Tracking
- Launch the MLflow UI to visualize experiment results:
    ```sh
    mlflow ui
- Open localhost in your web browser.




## Results
Model evaluation results, including performance metrics and plots, can be found in the results directory. The best model is saved in the models directory.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request for any enhancements or bug fixes.

1. Fork the repository.
2. Create your feature branch: git checkout -b feature/YourFeature
3. Commit your changes: git commit -m 'Add some feature'
4. Push to the branch: git push origin feature/YourFeature
5. Open a pull request.


## License
This project is licensed under the MIT License - see the LICENSE file for details.
