# Categorical Data Encoding with Scikit-Learn

## Overview
This activity focuses on a crucial step in the Machine Learning pipeline: **Feature Engineering**. Using a comprehensive Pokémon dataset, this notebook demonstrates how to properly convert categorical text data into numerical formats that machine learning algorithms can process, utilizing Scikit-Learn's preprocessing tools.

## Dataset
* **Source File:** `pokemon.csv`
* **Size:** 801 records, 41 features
* **Features Focused On:** `type1` (Categorical/Nominal) and `generation` (Categorical/Ordinal)

## Tech Stack
* **Language:** Python
* **Data Manipulation:** Pandas
* **Machine Learning Preprocessing:** Scikit-Learn (`OrdinalEncoder`, `OneHotEncoder`)

## Workflow & Methodology
This notebook specifically highlights the distinction between nominal and ordinal data, applying the correct encoding technique to each:
1. **Ordinal Encoding:** Applied to the `generation` feature. Since Pokémon generations have a logical, sequential order (Gen 1 comes before Gen 2, etc.), `OrdinalEncoder` was used to map these categories into a ranked numerical sequence.
2. **One-Hot Encoding (OHE):** Applied to the `type1` feature (e.g., Grass, Fire, Water). Because there is no inherent mathematical ranking between elements (Fire is not "greater than" Water), `OneHotEncoder` was utilized to create separate binary columns for each type, preventing a future machine learning model from inferring a false hierarchy.

## How to Run

### Option 1: Run in Cloud (Recommended)
You can view and run this notebook instantly in your browser using Google Colab:
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/ronanpatrick/data-encoding-pokemon/blob/main/Encoding_pokemon.ipynb)

*(Note: To run the notebook in Colab, ensure you upload the `pokemon.csv` dataset to the session storage or update the pandas read path to the raw GitHub URL).*

### Option 2: Run Locally
1. Clone this repository: `git clone https://github.com/ronanpatrick/data-encoding-pokemon.git`
2. Install the required libraries: `pip install pandas scikit-learn`
3. Open the `.ipynb` file in Jupyter Notebook or VS Code and run all cells.
