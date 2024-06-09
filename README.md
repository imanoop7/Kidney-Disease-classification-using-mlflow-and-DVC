# Kidney Disease Classification using MLflow and DVC

This repository demonstrates a machine learning pipeline for classifying kidney disease, utilizing [MLflow](https://mlflow.org/) for experiment tracking and [DVC](https://dvc.org/) (Data Version Control) for data and model management. The goal is to build a reproducible and scalable workflow for kidney disease classification based on clinical features.

![Workflow](assets/workflow.png)

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
  - [Data Versioning](#data-versioning)
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
    mlflow ui
    ```

2. Train the model:
    ```sh
    python src/train.py
    ```

3. Evaluate the model:
    ```sh
    python src/evaluate.py
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

## usage 
### Training
Run the training script to train the machine learning model: