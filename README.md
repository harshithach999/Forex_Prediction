# Forex_Prediction

## Abstract

This project focuses on building a Forex analysis tool that integrates various cloud services like **AWS EC2**, **RDS DBMS**, **Microsoft Azure**, and **Databricks**. The goal is to analyze currency exchange trends and provide users with insights to make informed decisions in forex trading. The project includes a web application for managing and tracking investments, an analysis module, and a prediction model to forecast currency exchange fluctuations. Techniques like **LSTM (Long Short-Term Memory)** are used to predict trends based on historical data.

## Introduction

The Forex market, the largest financial market globally, has a daily volume exceeding $7.5 trillion. Given the vast amount of data generated in this market, real-time analysis and trend prediction are crucial for investors. The project aims to provide users with tools to manage forex investments and predict future trends using advanced data analysis techniques.

## Data Characteristics

Forex data exhibits all the characteristics of **Big Data**:

- **Volume**: Historical forex data amounts to 200TB for the past 10 years. A month of data alone includes 850,000 records.
- **Velocity**: Forex data changes rapidly in real-time, requiring an elastic and scalable data processing infrastructure.
- **Variety**: Data is accessed from external APIs in **JSON format** and is stored in relational databases.
- **Veracity**: Forex data is high-quality with minimal noise, ensuring reliable analysis.
- **Value**: Forex data is highly valuable, with trading volumes of $7.5 trillion daily.

## Design Considerations and Functionalities

### Forex Portfolio Manager

The web application allows users to manage forex investments, track gains or losses, and determine the best times to buy or sell currencies based on real-time exchange rates. The app uses the **MEAN stack** (MongoDB, Express, Angular, and Node.js) and fetches data from external APIs to analyze current exchange rates.

### Forex Data Analysis

In the analysis module, we generate dynamic visualizations using **Databricks** on **Microsoft Azure**. Two types of visualizations are provided:
1. **Line Chart**: Compares exchange rates between two currencies over a specific period.
2. **Bar Chart**: Displays exchange rates of different currencies relative to a selected currency.

The real-time data is retrieved from the **Fixer API**, while historical data is stored in **MySQL** hosted on AWS. Data is processed using **PySpark DataFrames**, which allows distributed processing for faster and more scalable operations.

### LSTM for Forex Data Prediction

In the prediction module, **LSTM (Long Short-Term Memory)** networks are employed to predict future forex market trends. LSTM is a type of **Recurrent Neural Network (RNN)** that excels in handling time series data due to its ability to capture long-term dependencies. Forex data, being highly volatile and dependent on past fluctuations, benefits from LSTM's capacity to remember previous trends while making future predictions.

The LSTM model processes historical forex data and forecasts potential future movements in currency exchange rates, helping users make more informed trading decisions.

## Benefits of Databricks on Azure

Databricks on Azure offers several benefits for handling large-scale data:
- **Distributed Processing**: Automatically scales workloads across processors, saving time and cost.
- **Integration**: Seamless integration with the Azure stack, including Data Lake Storage and Data Warehouse.
- **Programming Flexibility**: Supports multiple programming languages like **Python**, **R**, and **SQL**.
- **Collaboration**: Provides versioning and collaboration features through **Jupyter Notebooks**.

## Future Work

Future improvements include:
- **Integration of Components**: Combining the analysis, prediction, and management modules into a single portal for ease of use.
- **Alert System**: Adding a feature to alert users when exchange rates fluctuate beyond a configured threshold.
- **Enhanced Prediction Models**: Incorporating more optimized machine learning models to improve the accuracy of forex trend predictions, reducing error rates.

## Conclusion

This project provides an end-to-end solution for forex analysis by combining data management, visualization, and prediction. **LSTM** plays a pivotal role in forecasting currency trends based on historical data, helping users to navigate the complexities of the forex market. While the system has proven effective, future improvements will further enhance its functionality and predictive power.

## References

1. [Forex Trading Volume Research](https://www.forex.com/en/market-analysis/latest-research/forex-volume-trading/)
2. [Azure Databricks Benefits](https://global.hitachi-solutions.com/blog/6-reasons-to-use-azure-databricks-today/)

