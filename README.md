# Big_Data_Pipeline_Hadoop_Hive
This project demonstrates a complete end-to-end Big Data Pipeline that collects data from multiple real-world sources, stores it in a distributed file system (HDFS), processes it using SQL-like queries in Hive, and visualizes the results through interactive dashboards — all runnable in Google Colab without any cluster setup.
🏗️ Pipeline Architecture
┌─────────────────┐     ┌──────────────┐     ┌─────────────────┐     ┌──────────────┐     ┌───────────────┐
│   Data Sources  │────▶│  Ingestion   │────▶│  HDFS Storage   │────▶│ Hive (HiveQL)│────▶│ Visualization │
│                 │     │              │     │                 │     │              │     │               │
│ • Web Logs      │     │ Python       │     │ /logs/          │     │ web_logs     │     │ Matplotlib    │
│ • IoT Sensors   │     │ Scripts      │     │ /sensors/       │     │ iot_sensors  │     │ Seaborn       │
│ • Social Media  │     │ (Faker)      │     │ /social/        │     │ social_media │     │ Plotly        │
└─────────────────┘     └──────────────┘     └─────────────────┘     └──────────────┘     └───────────────┘

📂 Data Sources
SourceRecordsFields🌐 Web Server Logs500IP, method, endpoint, status code, response time, bytes sent🌡️ IoT Sensor Data400Sensor ID, location, temperature, humidity, pressure, vibration📱 Social Media API300Platform, topic, sentiment, likes, retweets, followers

🛠️ Tech Stack
LayerTechnologyLanguagePython 3.8+Data GenerationFaker, NumPyData ProcessingPandas, SQLite (Hive simulation)HDFS SimulationLocal filesystem with HDFS command mirroringHive QueriesHiveQL via SQLite engineVisualizationMatplotlib, Seaborn, PlotlyEnvironmentGoogle Colab / Jupyter Notebook

🔍 HiveQL Queries Implemented

HTTP Status Code Distribution — Count requests and average response time grouped by status code
Endpoint Performance Analysis — Filter 200 OK requests and rank endpoints by response time
Sensor Alert Summary — Aggregate temperature and humidity readings by location and alert status
Social Media Engagement — Total likes and retweets grouped by trending topic
Sentiment Analysis by Platform — Percentage distribution of positive, negative, and neutral posts per platform


📊 Dashboards
DashboardCharts📡 Web Server AnalyticsStatus code bar chart, endpoint response time, HTTP method pie, bytes histogram🌡️ IoT Sensor AnalyticsTemp by location, alert heatmap, temp vs humidity scatter, pressure distribution📱 Social Media AnalyticsEngagement by topic, sentiment pie, platform stacked bar, followers vs likes📋 Hive Results SummaryAlert count by location, total likes by topic

🚀 Getting Started
Run on Google Colab (Recommended)

Click the Open in Colab badge above
Upload Big_Data_Pipeline_Hadoop_Hive.ipynb
Go to Runtime → Run all
No additional setup required ✅

Run Locally
bash# Clone the repository
git clone https://github.com/your-username/big-data-pipeline-hadoop-hive.git
cd big-data-pipeline-hadoop-hive

# Install dependencies
pip install faker pandas matplotlib seaborn plotly

# Launch Jupyter
jupyter notebook Big_Data_Pipeline_Hadoop_Hive.ipynb

📁 Repository Structure
big-data-pipeline-hadoop-hive/
│
├── Big_Data_Pipeline_Hadoop_Hive.ipynb   # Main notebook
├── README.md                             # Project documentation
└── /tmp/                                 # Auto-generated at runtime
    ├── hdfs_simulation/
    │   ├── logs/web_server_logs.csv
    │   ├── sensors/iot_sensor_data.csv
    │   └── social/social_media_data.csv
    └── hive_warehouse.db

🎯 Key Concepts Demonstrated

Hadoop Architecture — NameNode/DataNode concepts via structured directory simulation
HDFS Commands — hdfs dfs -ls, -put, -mkdir mirrored in output
Hive Data Modelling — Schema design with typed columns (STRING, INT, FLOAT)
ETL Pipeline — Extract → Transform → Load → Analyze → Visualize
HiveQL — GROUP BY, WHERE filters, aggregate functions (AVG, SUM, COUNT, MAX)
Multi-source Integration — Merging logs, sensors, and social data into one warehouse


📸 Sample Output
Web Server DashboardIoT Sensor DashboardHTTP error rates, endpoint latencyTemperature alerts, sensor heatmap

👨‍💻 Author
[Your Name]
III Year B.E. Computer Science and Engineering
Course: 22CSEDE23 – Big Data Analytics

📄 License
This project is licensed under the MIT License.
