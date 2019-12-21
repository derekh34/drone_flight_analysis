# Drone Flight Analysis

In this notebook, I analyze drone flights and look for anomalies.  

### Data

* In-flight telemetry data of 447 drone flights
* Hardware components of each drone
* Environment variables such as temperature and windspeed

### Analysis

I identify anomalies by calculating differences in successive values for each telemetry variable. If the difference is more than 3 standard deviations away from the mean difference value, I flag that measurement as an anomaly.

I predicted the number of anomalies per flight by fitting the pre-flight variables to a random forest regressor. Feature importances are displayed to infer which factors contribute to these anomalies.
