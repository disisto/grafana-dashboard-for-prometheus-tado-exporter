## Grafana dashboard for Prometheus tado-exporter<br>Monitor your tado° Smart Radiator Thermostat and Temperature Sensor
Grafana dashboard for Prometheus <a href="https://github.com/eko/tado-exporter">eko/tado-exporter</a> that shows the temperature setting, current temperature, humidity and activity for all rooms equipped with tado° Smart Radiator Thermostat and/or Temperature Sensor.

<img src="https://raw.githubusercontent.com/disisto/grafana-dashboard-for-prometheus-tado-exporter/main/img/grafana_dashboard_for_prometheus_tado_exporter.png">


## Prerequisites
+ <a href="https://www.tado.com/">tado°</a> Smart Radiator Thermostat / Temperature Sensor
+ <a href="https://github.com/grafana/grafana">Grafana</a> instance (v7.3 or higher)
+ <a href="https://github.com/prometheus/prometheus">Prometheus</a>
+ <a href="https://github.com/eko/tado-exporter">eko/tado-exporter</a> by Vincent Composieux

## Installation
### Import
1. To import a dashboard click the `+` icon in the side menu of Grafana, and then click Import.<br>
<img src="https://raw.githubusercontent.com/disisto/grafana-dashboard-for-prometheus-tado-exporter/main/img/grafana_import.png">

2. From here you can upload the dahboard JSON file, paste a Grafana.com dashboard URL or ID or paste dashboard JSON text directly into the text area.<br>
<img height="323" src="https://raw.githubusercontent.com/disisto/grafana-dashboard-for-prometheus-tado-exporter/main/img/grafana_import2.png">

There are two identical dashboards that only differ in the display of the temperature scale. If the default temperature scale is changed, the unit symbol and the threshold are not automatically adjusted, which is why two independent dashboards were created for this scenario. Choose the dashboard with the desired default temperature scale for your needs.

| Temperature scale | ID      | URL |  JSON |
| ----------------- |:------- | :---| :-----|
| Celsius           | `13699` | `https://grafana.com/grafana/dashboards/13699` | <a href="https://grafana.com/api/dashboards/13699/revisions/1/download">`Download JSON`</a> |
| Fahrenheit        | `13700` | `https://grafana.com/grafana/dashboards/13700` | <a href="https://grafana.com/api/dashboards/13700/revisions/1/download">`Download JSON`</a> |

## Optional customization

If you use the tado° Smart Schedule, you can display some delimiter in the temperature graph.

Smart Schedule in tado° app<br>
<img height="323" src="https://raw.githubusercontent.com/disisto/grafana-dashboard-for-prometheus-tado-exporter/main/img/tado_smart_schedule.png">

Default: Grafana dashboard without tado° Smart Schedule<br>
<img src="https://raw.githubusercontent.com/disisto/grafana-dashboard-for-prometheus-tado-exporter/main/img/without_smart_schedule.png">

Customized: Grafana dashboard wit tado° Smart Schedule indication<br>
<img src="https://raw.githubusercontent.com/disisto/grafana-dashboard-for-prometheus-tado-exporter/main/img/with_smart_schedule.png">

If you prefer to add the Smart Schedule delimiter, click on the settings dropdown on the temperature graph and choose 'Edit':<br>
<img src="https://raw.githubusercontent.com/disisto/grafana-dashboard-for-prometheus-tado-exporter/main/img/edit_for_smart_schedule.png">

Scroll down to 'Time regions' and press on '+ Add Time region':<br>
<img src="https://raw.githubusercontent.com/disisto/grafana-dashboard-for-prometheus-tado-exporter/main/img/grafana_time_regions.png">

Add the time and date settings that matches with your tado° settings:<br>
<img src="https://raw.githubusercontent.com/disisto/grafana-dashboard-for-prometheus-tado-exporter/main/img/grafana_time_regions_settings.png">


---
This project is not affiliated with <a href="https://www.tado.com/">tado°</a>.<br>
All mentioned trademarks are the property of their respective owners.
