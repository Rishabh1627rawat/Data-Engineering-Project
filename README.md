

# 📊 Stock Sentiment Correlation Data Pipeline

This is an end-to-end automated data engineering project designed to **analyze and visualize how stock values of top 5 technology companies correlate with news article sentiments**. It simulates a real-world pipeline, featuring cloud integration, data orchestration, and reporting.

## 🚀 Project Objective

To build an automated and scalable data pipeline that:
- Extracts stock price data and news articles.
- Processes and cleanses the data.
- Analyzes sentiment from news headlines.
- Joins both datasets to observe correlation.
- Visualizes insights in a dashboard.

---

## 🏗️ Architecture Overview

   +--------------+           +---------------+           +--------------+
   |   Docker     |  --->     |   Prefect     |  --->     | Apache Spark |
   +--------------+           +---------------+           +--------------+
          |                         |                            |
          |                         v                            v
   +------------------+      +--------------+         +--------------------+
   |  Stock API       |      | News API     |         | GCS (Raw Storage)  |
   +------------------+      +--------------+         +--------------------+
                                                               |
                                                               v
                                                  +--------------------+
                                                  | Spark DataProc     |
                                                  | (Data Cleaning)    |
                                                  +--------------------+
                                                               |
                                                               v
                                                    +------------------+
                                                    | BigQuery         |
                                                    | (Data Warehouse) |
                                                    +------------------+
                                                               |
                                                               v
                                                    +------------------+
                                                    | Power Bi          |
                                                    | (Visualization)   |
                                                    +------------------+


 
---

## 🧰 Technologies Used

| Component         | Tool/Service Used                  |
|------------------|------------------------------------|
| Programming      | Python                             |
| Orchestration    | Prefect                            |
| Data Processing  | Apache Spark (on DataProc)         |
| Storage          | Google Cloud Storage (GCS)         |
| Data Warehouse   | Google BigQuery                    |
| Infrastructure   | Terraform                          |
| Containerization | Docker                             |
| Visualization    | Power BI                           |

---

## 🔍 Features

- Real-time ingestion of stock prices and news articles
- Sentiment analysis on news using `TextBlob`
- Scheduled and managed workflows using Prefect
- Cleaned and joined datasets using Spark jobs
- Secure and scalable data handling via GCP
- Interactive dashboards to explore correlations

---

## 📈 Sample Output

- Line chart of stock values over time
- Sentiment trendline vs. stock movement
- Correlation matrix between sentiment polarity and price fluctuations

---

## 🧪 Future Improvements

- Add ML model to predict stock movement based on sentiment score
- Use Apache Kafka for real-time streaming ingestion
- Include more companies and broader date range



