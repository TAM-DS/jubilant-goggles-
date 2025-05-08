# jubilant-goggles-
Cloud FinOps Recommender &amp; Cost Alert Engine Serverless, cloud-native system that monitors cloud infrastructure costs, recommends optimization actions, and sends real-time alerts. Includes an A/B testing module to evaluate the effectiveness of recommendations.  Designed using AWS-native services and Python to simulate a real-world FinOps platform.


📌 Overview

A serverless, cloud-native system that monitors cloud infrastructure costs, recommends optimization actions, and sends real-time alerts. Includes an A/B testing module to evaluate the effectiveness of recommendations.

Designed using AWS-native services and Python to simulate a real-world FinOps platform.


🧱 Architecture Summary

Core Components:

AWS Lambda: Executes cost analysis and optimization logic.

Amazon S3: Stores historical cost and usage data (CSV or pulled via Cost Explorer API).

Amazon DynamoDB: Logs recommendations, A/B testing groups, and user actions.

Amazon SNS: Sends notifications and alerts to stakeholders.

Streamlit / Tableau: Provides a visualization layer for spend, savings, and test results.



🧠 Features

📊 Daily Cost Monitoring: Scheduled job analyzes daily spend and detects anomalies.

📉 Optimization Recommender: Recommends actions (e.g., instance rightsizing, idle resource cleanup).

🧪 A/B Testing Framework: Tests different recommendation strategies for effectiveness.

🚨 Alert System: Sends alerts based on defined thresholds or anomalies.

📈 Dashboard: Interactive spend and savings dashboard with experiment tracking.


🐍 Tech Stack

Python (Pandas, NumPy, Statsmodels, Boto3)

AWS Lambda, DynamoDB, S3, SNS

Streamlit or Tableau Public (for visualization)

⚙️ How It Works

Cloud usage data ingested from S3 (CSV format).

Lambda scans for high-cost anomalies and applies rule-based logic.

Recommendations are stored in DynamoDB.

A/B groups randomly assigned to track savings impact.

SNS pushes alerts; dashboard updates daily.


🧪 A/B Test Design

Control Group: Receives no recommendations

Treatment Group: Receives one or more cost-saving recommendations

Measured by: average daily cost difference over 14–28 days

Statistical methods: t-test, ANOVA, effect size


✅ Goals

Deliver actionable insights to reduce cloud spend

Demonstrate engineering capability for scalable FinOps tooling

Align with Amazon, Netflix, and Goldman Sachs tech & product strategy

🪪 Author

Built by Tracy Anne Griffin Manning — FinOps x AI x Experimentation | #BuiltByTAGM

🚀 Setup (Local Dev)

Clone this repo Comming Soon 

Install dependencies: pip install -r requirements.txt

Create .env file with AWS credentials

Run local simulation: python run_simulation.py

View dashboard: streamlit run dashboard.py

📄 License
