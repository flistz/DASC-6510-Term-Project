# Twitter Volume Forecasting for AMZN

## Overview
This repository contains the Jupyter notebook (`predict.ipynb`) that demonstrates time-series forecasting of the Twitter volume for Amazon (AMZN). The project employs two different models: the Prophet model and the Neural Network Autoregressive (NNAR) model, implemented using PyTorch and running on Google Colab with a Tesla T4 GPU.

## Dataset
The dataset can be found in the Numenta Anomaly Benchmark (NAB) repository, specifically within the `realTweets` directory, and is not included in this repository due to size constraints. It records the number of Twitter mentions of Amazon (AMZN) at 5-minute intervals. For analysis, we aggregate this to hourly intervals. The dataset can be accessed [here](https://github.com/numenta/NAB/tree/master).

## File Structure
- `code/`:
  - `predict.ipynb`: Jupyter notebook containing all the analysis code, including data preprocessing, model training, evaluation, and prediction.
- `data/`:
  - `Twitter_volume_AMZN.csv`: The Twitter volume data for Amazon (AMZN).

## Models
- **Prophet Model:** This model, provided by the Prophet library, is utilized for its ability to handle time-series data with strong seasonal patterns.
- **NNAR Model:** A custom Neural Network Autoregressive model is built using PyTorch, designed to capture the temporal dependencies within the data.

## Running the Notebook
The notebook is intended to be run on Google Colab, which provides the required environment along with GPU support. 

To use the notebook:
1. Upload the `predict.ipynb` file to your Google Colab.
2. Upload the `Twitter_volume_AMZN.csv` dataset to the appropriate location in your Google Colab session.
3. Run the cells in order as they appear in the notebook.

## Results
Both models were evaluated on their forecasting performance with the following results:
- Prophet Model achieved an MAE of 7.1221, MSE of 102.3506, RMSE of 10.1168, and MAPE of 13.6958.
- NNAR Model achieved an MAE of 7.5672, MSE of 104.4078, RMSE of 10.2180, and MAPE of 15.3552.

The performance analysis showed that the Prophet model has a slight edge in prediction accuracy over the NNAR model. However, the NNAR model's training loss curve displays a promising learning pattern, which indicates potential for further optimization.

## Contributions
Contributions to improve the models or analysis are welcome. Please feel free to fork the repository, make changes, and submit a pull request.

## License
This project is licensed under the terms of the MIT license.

## Contact
If you have any questions or suggestions, please open an issue in this repository.
