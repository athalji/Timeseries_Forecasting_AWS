# End-to-End 4G LTE network capacity forecasting pipeline on AWS

This project was created as an extension to a project that I worked on with a big mobile operator in the MENA region. the goal of the original project was to create a framework to monitor the capacity of the operator's 4G LTE network to guarantee customer quality of service. The initial analysis broke down the analysis into the following aspects:

1) KPIs to be monitored
2) At What level of "number of connected users" do these KPIs start going down below a desired quality of service threshold

The main extension to this project is to build a framework to forecast the network capacity (as defined by the previous part above) using AWS. The framework consists of building a datapipeline that ingests the data, processes it, then displays the forecast as part of a dashbaord. The data pipeline assumes that the data ingested is from Huawei infra (naming based on Huawei network counetrs) but it can easliy be expanded to accept other vendors' formats.

The breakdown of the project is as follows:

1) Dataset exploration and visualization. Notebook:
2) Traditional forecasting methods. Notebook:
3) Deep learning forecasting methods. Notebook:
4) End-to-End data pipeline and forecasting model deployment on AWS
