# Drone Flight Analysis

In this notebook, I analyze drone flights and look for anomalies.  

### Data

* In-flight telemetry data of 447 drone flights
* Hardware components of each drone
* Environment variables such as temperature and windspeed

### Analysis

I identify anomalies by calculating differences in successive values for each telemetry variable. If the difference is more than 3 standard deviations away from the mean difference value, I flag that measurement as an anomaly.

I fit the pre-flight variables to a random forest regressor in order to predict the number of anomalies per flight. I displayed the feature importances of the model to infer which factors contribute to these anomalies.
