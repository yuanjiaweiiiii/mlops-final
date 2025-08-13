# MLOps Final Project

This repository contains the final project for the MLOps course, implementing a complete machine learning pipeline using Airflow, MLflow, and modern MLOps tools.

## 📘 Table of Contents

1. [Introduction](#1-introduction)  
2. [Project Overview](#2-project-overview)  
3. [Pipeline Architecture](#3-pipeline-architecture)  
4. [Data](#4-data)  
5. [Exploratory Data Analysis](#5-exploratory-data-analysis)  
6. [Feature Engineering](#6-feature-engineering)  
7. [Model Training and Selection](#7-model-training-and-selection)  
8. [Model Serving](#8-model-serving)  
9. [Workflow Orchestration (Airflow)](#9-workflow-orchestration-airflow)  
10. [Model Tracking (MLflow)](#10-model-tracking-mlflow)  
11. [Model Evaluation and Monitoring](#11-model-evaluation-and-monitoring)  
12. [Infrastructure and Deployment](#12-infrastructure-and-deployment)  
13. [Conclusion and Future Work](#13-conclusion-and-future-work)  
14. [References](#14-references)

---

## 1. Introduction

Brief description of the project goal, real-world relevance, and what problem you're solving.

## 2. Project Overview

Summarize the end-to-end workflow:
- Data ingestion
- EDA
- Model training
- Deployment
- Monitoring

## 3. Pipeline Architecture

Visual DAG / architecture diagram  
Describe modular folders like `src/`, `dags/`, `models/`, etc.

## 4. Data

- Source: [healthcare-dataset-stroke-data.csv](./data/healthcare-dataset-stroke-data.csv)
- Preprocessing: missing values, encoding, etc.
- Train-test split strategy

## 5. Exploratory Data Analysis

- Summary statistics  
- Visualizations  
- Findings related to target imbalance, correlation, etc.  
- Notebook: [`Stroke_EDA_&_Data_Split.ipynb`](./data/Stroke_EDA_&_Data_Split.ipynb)

## 6. Feature Engineering

- One-hot encoding  
- Target encoding  
- Standardization  
- Missing value imputation  
- Scripts:  
  - [`src/data/make_dataset.py`](./src/data/make_dataset.py)  
  - [`src/features/build_features.py`](./src/features/build_features.py)

## 7. Model Training and Selection

- AutoML (e.g., HPO / baseline comparison)  
- Model versions  
- Metrics (accuracy, F1, etc.)  
- Script: `src/models/train_model.py`

## 8. Model Serving

- FastAPI app: prediction endpoint  
- Script: `src/serve/app.py`  
- Usage example with `curl` or `requests`

## 9. Workflow Orchestration (Airflow)

- DAG file: [`dags/train_pipeline.py`](./dags/train_pipeline.py)  
- Steps: ingest → split → EDA → train → register → deploy  
- Screenshot of DAG view (optional)

## 10. Model Tracking (MLflow)

- Experiment name  
- Parameters and metrics  
- Artifact logging  
- Registry (staging → production)

## 11. Model Evaluation and Monitoring

- Metrics comparison  
- Evidently report (drift, fairness, performance over time)  
- Location: `/reports/`

## 12. Infrastructure and Deployment

- `Dockerfile`  
- GitHub Actions / CI-CD  
- Airflow & MLflow config  
- Folder: `infra/`

## 13. Conclusion and Future Work

Summary of what you’ve accomplished and what could be improved:
- Robustness
- Real-time triggers
- Data quality checks
- Model retraining logic

## 14. References

List of relevant papers, libraries, datasets, or external tools used.

---

