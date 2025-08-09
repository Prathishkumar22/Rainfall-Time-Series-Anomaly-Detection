# Rainfall-Time-Series-Anomaly-Detection
This project visualizes Mumbai monthly rainfall data and detects anomalies in a time series using Power BI's built-in anomaly detection feature.

Prerequisites Power BI Desktop installed
Dataset file (mumbai-monthly-rains.csv or .xlsx)

Basic familiarity with Power BI interface

Dataset Description The dataset contains:
Year — ranging from 1901 to 2021

Total — total annual rainfall amount (mm)

Optional monthly columns (Jan–Dec) for more granular analysis

Steps to Load Data Open Power BI Desktop.
Click Home → Get Data → Text/CSV (or Excel).

Select your dataset file (mumbai-monthly-rains.csv).

Click Load.

Preparing Data for Anomaly Detection Anomaly detection in Power BI requires a Date/Datetime field in the X-axis.
4.1 Add a Date Column Go to Home → Transform Data (Power Query Editor).

Select your table.

Click Add Column → Custom Column.

Enter formula:

powerquery Copy Edit = #date([Year], 1, 1) Name this column Date.

Set Data Type to Date.

Click Close & Apply.

Creating the Anomaly Detection Chart In Report View, insert a Line chart visual.
Drag Date to the X-axis.

Ensure the axis type is Continuous (click drop-down → select Date → Continuous).

Drag Total to the Y-axis.

Open the Analytics pane (magnifying glass icon).

Scroll down to Find anomalies → click Add.

Adjust:

Sensitivity — controls how easily anomalies are detected.

Expected range color — for better visualization.

Anomaly color — to highlight unusual points.

Interpreting Results Shaded area = expected range of values.
Anomaly marker = detected unusual value.

Hover over anomaly points for detailed values.

Optionally, right-click → Explain anomaly to get AI-generated insights.

Optional Enhancements Create separate visuals for Monthly and Annual anomalies.
Use slicers for filtering by year range.

Combine anomaly detection with moving average lines for trend analysis.

Files in This Project mumbai-monthly-rains.csv — source data
Time Series Data.pbit — Power BI template

Anomaly_detection with Time Series Data preprocessing.ipynb — Jupyter notebook for preprocessing and exploratory analysis

README.md — documentation (this file)

References Microsoft Power BI Anomaly Detection
Time Series Analysis in Power BI
