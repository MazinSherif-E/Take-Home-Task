# NLP Classification with Contrastive Learning and Semi-Supervised Techniques

## Project Overview
This project explores an innovative approach to NLP tasks, integrating methodologies from "SimCSE: Simple Contrastive Learning of Sentence Embeddings" and "Self-supervised Semi-supervised Learning." We apply this integrated approach to two distinct datasets: the 20 newsgroups dataset for multi-class text classification and the IMDb dataset for binary sentiment analysis.

## Datasets
The project demonstrates the methodology on two datasets with differing structures and classification tasks:

1. **20 Newsgroups Dataset**: A collection of newsgroup documents spanning various topics, used for multi-class classification.
2. **IMDb Dataset**: A set of movie reviews, labeled as positive or negative, used for binary sentiment classification.

## Methodology
The project adopts a sequence of steps tailored to each dataset, while maintaining the core methodology derived from the two papers:

### Data Loading and Preprocessing
- Both datasets are loaded and preprocessed for NLP tasks.
- Preprocessing includes tokenization and text cleaning, adapted to each dataset's specifics.

### Exploratory Data Analysis (EDA)
- EDA is conducted for both datasets to understand class distribution, document lengths, and other textual features.

### Model Training
- We train two models for each dataset: a fully supervised model using all labeled data, and a semi-supervised model using a fraction of the labeled data.
- The semi-supervised model incorporates self-supervised learning through dropout as a form of data augmentation, inspired by SimCSE, and semi-supervised learning techniques.

### Model Evaluation and Comparison
- Both models for each dataset are evaluated on their respective test sets.
- We compare the performance of semi-supervised models trained with varying fractions of labeled data against their fully supervised counterparts.

### Determining Minimum Labeled Data Requirement
- For each dataset, we experiment to find the minimum amount of labeled data required for the semi-supervised model to match the performance of the fully supervised model.

### Adjustments for IMDb Dataset
- Given the binary nature of the IMDb dataset, modifications are made in model training (binary classification loss function) and in the choice of the classifier (e.g., logistic regression instead of nearest neighbor classifier).

## Repository Structure
- `README_project.md`: This documentation file.
- `main.py`: Main script containing the implementation for both datasets.
- `requirements.txt`: List of Python dependencies for the project.

