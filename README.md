A node red flow you can use together with the metric_monitor module on the IoTopen platform http://iotopen.se. 
This is for those who do not have the metric_notifier module active or installed for some reason.

The flow listens to metric_monitor.status in the metadata and if it's set to 0,1 or 2.
If it is set to 2 it sends the notification.
