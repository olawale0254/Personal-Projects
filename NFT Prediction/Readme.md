# NFT Prediction Model

This project aims to predict the future value of NFTs using machine learning models. The project is implemented in Python and uses the PyCaret library for building and evaluating the models.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Approach](#approach)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## Installation

To run this project, you need to have Python installed on your machine. You can install the required dependencies using pip.
```bash
pip install -r requirements.txt
```

Alternatively, you can install the dependencies directly in a Jupyter notebook or Google Colab.

## Usage

1. Clone the repository to your local machine.


```bash
git clone https://github.com/yourusername/nft-prediction.git
cd nft-prediction
```
2. Open the Jupyter notebook.

```bash
jupyter notebook NFT\ Prediction/modelling.ipynb
```

3. Run the cells in the notebook to train and evaluate the model.

## Approach

1. **Data Collection**: The dataset used for training the model is stored in `data/nft_data.csv`. This dataset contains historical data on NFT prices and other relevant features.

2. **Data Preprocessing**: The data is preprocessed to handle missing values, normalize numerical features, and encode categorical features.

3. **Model Training**: The PyCaret library is used to train multiple machine learning models. PyCaret simplifies the process of model training and evaluation by providing a high-level API.

4. **Model Evaluation**: The trained models are evaluated using various metrics such as Mean Absolute Error (MAE), Mean Squared Error (MSE), and R-squared. The best-performing model is selected based on these metrics.

5. **Prediction**: The selected model is used to make predictions on new data.

## Project Structure

nft-prediction/
├── NFT Prediction/
│ ├── modelling.ipynb
├── data/
│ ├── nft_data.csv
├── requirements.txt
├── README.md