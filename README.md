## Cluj Napoca Temperature Prediction
This repository contains the codebase, presentation and report for the Cluj Napoca temperature prediction project, developed for the Intelligent Modelling subject. The codebase folder contains 5 other folders:

- **Data**: Contains the data received from the Openweather API for Babes Bolyai University of Cluj Napoca. This folder contains 2 CSV files: one with all the data received from the API, and one with cleaned data from the API (data which we used).

- **Models**: Contains two other folders: one of them containing the Autoformer 24 hours and 12 hours prediction, and the other one containing the models from the LSTM prediction of temperature, of 6, 8, 10, 12 and 24 hours.

- **Results**: Contains the saved results in .npy files of the Autoformer models.

- **Scripts**: Contains code used for EDA and LSTM training/prediction. This folder contains two Jupyter notebooks: EDA_predict_LSTM.ipynb and predict_autoformer.ipynb. The former contains the script for exploratory data analysis and LSTM training/prediction, while the latter contains the script for training and predicting using the Autoformer model.

- **Static**: Contains all the figures saved in making the presentation and the report.

### Usage
To use this codebase, you can clone this repository and run the scripts in the Scripts folder. The EDA_predict_LSTM.ipynb notebook contains the code for exploratory data analysis and LSTM training/prediction, while the predict_autoformer.ipynb notebook contains the code for training and predicting using the Autoformer model. To create a virtual environment for these you should follow these steps:  

- Open a terminal or command prompt and navigate to the directory where you want to create the virtual environment.

- Create a new virtual environment using the following command:  
`python -m venv myenv`

This will create a new virtual environment named myenv.

- Activate the virtual environment using the appropriate command for your operating system:

    - Windows: myenv\Scripts\activate.bat
    - macOS/Linux: source myenv/bin/activate
- Install the packages listed in the requirements.txt file using pip:  
`pip install -r requirements.txt`  

**Note** You will also have to install cuda if you have a GPU from: https://developer.nvidia.com/cuda-downloads

This will install all the packages listed in the requirements.txt file into your virtual environment.

You can now use the packages installed in your virtual environment by running your Python scripts while the virtual environment is activated.

- When you're done using the virtual environment, you can deactivate it using the following command:  
`deactivate`

This will deactivate the virtual environment and return you to your normal shell.

### Results
The results of this project are saved in the Results folder as .npy files. We used RMSE which is sqrt(MSE) and MAE to evaluate the performance of the models.

| **Model Name**     | **RMSE** | **MAE** |
|--------------------|----------|---------|
| LSTM 12 hours      | 2.39     | 1.85    |
| Autoformer 12 hours| 2.75     | 2.08    |
| LSTM 24 hours      | 3.01     | 2.39    |
| Autoformer 24 hours| 3.25     | 2.33    |


