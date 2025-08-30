Cybersecurity-Suspicious-Web-Threat-Interactions

This project analyzes web traffic logs collected via AWS CloudWatch to detect suspicious interactions and potential cyberattacks.
The dataset contains flagged events from a production web server, labeled as suspicious by Web Application Firewall (WAF) rules.

---

Dataset

Source: AWS CloudWatch traffic logs ,
Size: 282 records × 16 columns ,
Key Features:
bytes_in, bytes_out: traffic volume ,
src_ip, dst_ip: source & destination IPs ,
src_ip_country_code: country of origin ,
protocol, dst_port: network protocol and port ,
detection_types: WAF rule detection ,
creation_time, end_time, time: timestamps.

---

Workflow

1. Data Preparation:
Removed duplicates ,
Converted timestamps to datetime ,
Standardized categorical values ,
Feature engineering: session duration, packet size, traffic rates.

2. Exploratory Data Analysis (EDA):
Traffic volume: spikes in inbound traffic indicate infiltration attempts ,
Country codes: majority of suspicious traffic from US, CA, NL, AE ,
Detection types: mostly waf_rule triggered ,
Visualization: histograms, count plots, time-series charts, network graphs.

3. Machine Learning Models:
Isolation Forest: detected 5% anomalies ,
Random Forest Classifier: achieved 100% accuracy ,
Neural Network: achieved 100% accuracy.

4. Evaluation:
Random Forest Accuracy: 100% ,
Neural Network Accuracy: 100% ,
Isolation Forest: flagged 14 anomalies.

---

Technologies Used:

Python 3.8+ ,
Libraries used: pandas, numpy, matplotlib, seaborn, scikit-learn, tensorflow, networkx, shap
