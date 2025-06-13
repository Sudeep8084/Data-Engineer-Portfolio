# AWS Customer Concessions Data Pipeline

## 📌 Overview
This project demonstrates my contribution to a data pipeline at Amazon that ingests, processes, and aggregates customer concession data from internal tools. The data is used for compliance reporting, trend analysis, and stakeholder dashboards.

## ⚙️ Technologies Used
- **Language**: Python
- **Cloud**: AWS (S3, Lambda, Redshift)
- **ETL Orchestration**: Custom Python scripts
- **Monitoring**: CloudWatch
- **Data Storage**: Redshift, Parquet files in S3
- **Visualization**: Snowflake + internal dashboards

## 🔄 Data Flow
1. Extract: Pull JSON files from internal microservices via APIs.
2. Transform: Clean, flatten, and normalize the data using Python.
3. Load: Store processed data into Redshift and publish to Snowflake.
4. Monitor: Use CloudWatch to alert on pipeline failures.

## 📊 Impact
- Improved data pipeline performance by 35% by optimizing file partitioning.
- Resolved a critical production issue that restored downstream analytics with zero data loss.
- Enabled compliance dashboards to load 40% faster through query optimization.

## 🧪 Testing & Validation
- Unit tested all Python transformation functions.
- Validated Redshift table schemas against business rules.
- Conducted A/B testing on data load logic to improve batch success rate.

## 📁 Structure
aws_customer_concessions_pipeline/
│
├── README.md
├── src/
│ ├── extract.py
│ ├── transform.py
│ ├── load.py
│ └── utils.py
├── notebooks/
│ └── data_quality_checks.ipynb
├── dashboards/
│ └── dashboard_mockup.png
└── config/
└── pipeline_config.yaml


### 2. `src/` folder

- `extract.py` – handles API data pulls
- `transform.py` – flattens/cleans JSON
- `load.py` – writes to Redshift
- `utils.py` – helper functions (logging, config loading)

---

### 3. `notebooks/` folder

- Exploratory data analysis (EDA)
- Data profiling
- Quality checks
- Example queries (Snowflake, Redshift)

---

### 4. `config/` folder
- S3 bucket paths
- Database credentials (mock or env-based)
- File partitions or table schemas

---

