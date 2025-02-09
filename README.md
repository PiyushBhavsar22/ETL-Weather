# 🌦️ETL Weather Pipeline with AWS deployment

## 🚀Overview
The **ETL Weather Pipeline** is designed to extract weather data from an API, transform it into a structured format, and load it into a PostgreSQL database using **Apache Airflow**. 
The project follows an **Agile methodology**, breaking down tasks into sprints.

## 🔄ETL Process
The ETL process consists of three main stages:
1. **Extract** - Fetch weather data from an API.
2. **Transform** - Preprocess and structure the extracted data.
3. **Load** - Store the transformed data into a PostgreSQL database.

## 📥Architecture
- **Source Data**: APIs, Internal Databases, IoT Devices.
- **Processing**: Preprocessing & Transformation (JSON format).
- **Storage**: PostgreSQL, MongoDB, SQL databases.
- **Workflow Management**: Apache Airflow for scheduling & execution.
- **Containerization**: Docker for deployment.

## 🛠️Project Structure
```
Data Pipeline
    ├── API (HTTP Operator)
    ├── Transformation (Python Code)
    ├── Load (PostgreSQL)
```
- Uses **Airflow Connection** to interact with APIs.
- **PythonOperator** for transformation logic.
- Stores data in **Dockerized PostgreSQL**.

## Steps to Run the ETL Pipeline
### 1️⃣ Setup Environment
- Ensure **Docker** and **Airflow** are installed.
- Install **DBeaver** 

### 2️⃣ Start Airflow
```bash
astro dev start
```
- Navigate to **Admin > Connections**
- Add **Postgres connection**.
- Add **Open Meteo API connection**.
- Run the `weather_etl_pipeline`.

### 3️⃣ Access Database using DBeaver
- Open **DBeaver**.
- Select **PostgreSQL** as database.
- Open **SQL Editor**.
- Run the query:
  ```sql
  SELECT * FROM weather_data;
  ```

### 4️⃣ Deploy using Terminal
```bash
astro login
astro deploy
```

### 5️⃣ Deploy to AWS RDS
- Go to **AWS Console** > **RDS**.
- Create a **PostgreSQL database**.
- Open the database and configure:
  - **VPC Security Groups**.
  - **Security Group ID**.
  - Edit **Inbound Rules** to allow access.
  - Copy the **Database Endpoint**.

## Technologies Used
✅ **Apache Airflow** - Task Scheduling & Execution.
✅ **PostgreSQL** - Data Storage.
✅ **Python** - ETL Scripting.
✅ **Docker** - Containerization.
✅ **AWS RDS** - Cloud Database.
✅ **DBeaver** - SQL Query Execution.

## ☁️Conclusion
This ETL pipeline automates weather data extraction, transformation, and loading, ensuring seamless data management for analysis and insights.


