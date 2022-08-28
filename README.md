# End-to-End 4G LTE user experience forecasting pipeline on AWS

This project was created as an extension to a project that I worked on with a big mobile operator in the MENA region. the goal of the original project was to create a framework to monitor the capacity and user perceived quality of the operator's 4G LTE network. The initial requirements broke down the analysis into the following areas:

1) KPIs to be monitored
2) How often does the user experience deteriorate below a certain quality metric. For this project the metric under monitoring was the download user throughput

The goal was to forecast the average user download throughput per cell 24 hours in advance to check if it is expected to go below 1 Mbps, and for how long the drop is expected to last. Different action could be taken by the operator to compensate the affected users.

The main extension to this project is to build a framework to forecast the user experience (as defined by the previous part above) using AWS. The framework consists of building a datapipeline that ingests the data, processes it, then displays the forecast as part of a dashbaord. The data pipeline assumes that the data ingested is from Huawei infra (naming based on Huawei network counetrs) but it can easliy be expanded to accept other vendors' formats.

The breakdown of the project is as follows:

1) Dataset exploration and visualization. Norebook: [data_exploration.ipynb](https://github.com/athalji/timeseries_AWS/blob/main/data_exploration.ipynb) 
2) Traditional forecasting methods (ETS methods). Notebook: [ETS_forecasting_methods.ipynb](https://github.com/athalji/timeseries_AWS/blob/main/ETS_forecasting_methods.ipynb)
3) Traditional forecasting methods (ARIMA methods). Notebook: [ARIMA_forecasting_methods.ipynb](https://github.com/athalji/timeseries_AWS/blob/main/ARIMA_forecasting_methods.ipynb)
4) Machine learning forecasting methods. Notebook: [Traditional_ML_Forecasting_Methods.ipynb](https://github.com/athalji/timeseries_AWS/blob/main/Traditional_ML_Forecasting_Methods.ipynb)
5) Deep learning forecasting methods. Notebook: [Deep_learning_forecasting_methods.ipynb](https://github.com/athalji/timeseries_AWS/blob/main/Deep_learning_forecasting_methods.ipynb)
6) Multi-variate forecasting methods ... (under construction...date TBD) 
7) End-to-End data pipeline and forecasting model deployment on AWS (under construction..date TBD)
