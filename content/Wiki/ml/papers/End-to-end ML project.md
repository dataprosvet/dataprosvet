Created: 2022-10-31 21:10:49
Tags: #ML #programming #DataScience 

## Note
What is end-to-end ML project? When i talk about "end-to-end" i mean these steps you need to go through before your project is ready:
1. Create infrastructure for your project:
	- Set up remote server
	- Deploy all needed tools such as *[[Jupyter]] (or Jupyterhub)* for developing and quickly experiments running, *[[MLFlow]]* for saving models and experiments results, your own *[[Docker]] registry*, create *[[K8S]]* infrasctructure (if needed), *[[Airflow]]* for etl processes (data collection and processing), ...
1. Choose your system type: online (real-time system) or offline (batch) system. 
1. Choose a problem you want to solve (text santiment, face detection, analyze user behaviour, online/offline recommender system, ...)
1. Find or collect data and choose where you want to store data
1. Preprocess data and generate features
1. Experiments with model: training, validation, testing
1. Deploy ML Pipeline (deploy with [[Docker Container|Docker Containers]], create Airflow DAG, deploy with API, ...)
1. Set up model retraining if needed
1. Create Web UI, or Mobile app, or API for your model
3. Set up tools for monitoring your system (you can use [[Graphana]] for ex.):
	- [[Data Quality]]
	- [[Wiki/ml/metrics/ML metrics|ML metrics]]
	- Business metrics such as [[ARPU]], [[PU]], [[DAU]], [[ARPPU]], [[LTV]], [[Wiki/business_metrics/CLV|CLV]] and others

After these steps you have end-to-end ML system with data collection, preprocessing, monitoring and model retraining.

## References


## Zero Links
- [[Machine Learning]]

## Links