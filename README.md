# TITLE-Air Quality Prediction
# AIM
- We were required to predict the air quality for the next 24 hours.
# SHORT DESCRIPTION
- The motive of the project is to explore the possibilities of modern deep learning techniques,large language models in time series forcasting and comparing it with the tradionally used techniques.
# Approach
-Since we have access to factors that influence the air quality index (AQI) rather than the AQI itself, our objective is to predict the most significant factor in determining AQI, namely PM2.5, based on historical data points of PM2.5 and other relevant factors.
# DETAILED DESCRIPTION
> * Firstly, data on air quality index parameters is collected from the Central Pollution Control Board (CPCB) website. An analysis is conducted to determine whether the collected data constitutes a time series dataset. This analysis is crucial for determining the suitability of employing time series forecasting techniques.
> * Following the completion of all necessary installations and library imports, three different models are tested using the same dataset. This comparative analysis aims to evaluate the performance and suitability of each model for the given dataset. 
> * The first model tested is GEMMA:7B, a large language model (LLM) imported from Ollama after setting up Ollama environment. Prompting is utilized to interact with GEMMA:7B and generate the best possible zero-shot time series forecasting.
> * Next, the second model employed is Long Short-Term Memory (LSTM). Prior to training, the data is prepared by creating a window and feeding it into the model in sequential order. The LSTM model is trained for a total of 20 epochs to optimize its performance.
> * Finally, the third model utilized is the AutoRegressive Integrated Moving Average (ARIMA) model. This model is trained on the dataset to capture the time series patterns and make predictions based on the observed data.
# INSIGHTS
- ARIMA model gave best performance as it is a statistical model solely made for time series forcasting.
-  the LSTM model exhibits linear prediction behavior, likely due to the constant mean of the dataset. Training on over 11,000 data points with a consistent mean results in predictions for the next 24 data points with a similar constant mean and low variance. Consequently, the LSTM model struggles to accurately capture actual values, leading to inferior performance. This limitation arises from the inherent nature of LSTMs, which may not effectively handle datasets with constant mean and low variance, resulting in linear predictions.
- The analysis reveals that the large language model GEMMA:7B surpasses the LSTM model in zero-shot prediction tasks, despite lacking explicit training on time series data. This finding underscores the versatility and effectiveness of LLMs for time series forecasting, showcasing their capability to handle diverse datasets and predictive tasks without specialized training.

# MOTIVATION AND FUTURE ASPECTS
- Controlling air pollution is the need of the our and current research work shows the use of llms for time series forcasting. Research paper Time-LLM: Time Series Forecasting by Reprogramming Large Language Models, suggests better outcomes can be generated using llm for time series analysis.
- Time-LLM is a reprogramming framework to repurpose LLMs for general time series forecasting with the backbone language models kept intact. Notably, we show that time series analysis (e.g., forecasting) can be cast as yet another "language task" that can be effectively tackled by an off-the-shelf LLM.
- Time-LLM comprises two key components: (1) reprogramming the input time series into text prototype representations that are more natural for the LLM, and (2) augmenting the input context with declarative prompts (e.g., domain expert knowledge and task instructions) to guide LLM reasoning.
