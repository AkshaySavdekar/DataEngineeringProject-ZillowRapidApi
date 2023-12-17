
# Zillow Data Analytics Project
Seamlessly integrated Zillow Rapid API to extract and analyze data.Leveraging Python, Amazon Web Services , Airflow by building an end-to-end data pipeline to process, transform, and visualize Location data.
Data is Extracted from Zillow Rapid API transformed and placed that in Redshift Cluster. We are able to see Amazing Dashboards in AWS Quicksight.In the Process of ETL we placed the Extracted data from Zillow Rapid API in S3 bucket. We created one backup of this S3 bucket data. We used Lambda functions to create the backup copy of S3 data and transformed the data.

## Architecture
![image](https://github.com/AkshaySavdekar/DataEngineeringProject-ZillowRapidApi/assets/119107773/2135d0f9-ecf6-4a7b-b9d2-708aa54eb28e)


## Zillow Rapid API Reference

#### Get Location Data

```http
  GET search (Search for properties)

  URL: 'https://zillow56.p.rapidapi.com/search'
```

| Header | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `X-RapidAPI-Key` | `Enum` | **Required**. Your API key |
| `X-RapidAPI-Host` | `STRING` | **Required**. zillow56.p.rapidapi.com |

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `location`      | `string` | **Required**. Location can be an address, neighborhood, city, or ZIP code. e.g houston, tx |



## Tech Stack

**Technology:** Python, SQL, AWS S3, AWS Lambda, AWS Redshift, AWS QuickSight, Airflow, 

**Server:**  AWS EC2 Instance 


## Project Component

#### Programming Language - 
🐍 Python: Python served as the cornerstone, enabling seamless interaction with Zillow Rapid's API and handling data effectively.

#### ☁️ Amazon Web Services (AWS): 
We harnessed the power of AWS, deploying AWS Lambda functions for data extraction, transformation, and loading. Amazon S3 played a crucial role in storing both raw and transformed data efficiently.

#### 🌨️ AWS Redshift for Data Storage: 
For the loading part, I employed Redshift, an ideal platform for data warehousing and analytics.

#### 📊 AWS QuickSight for Visualization:
 Can utilise QuickSight to craft stunning data visualizations and interactive dashboards, simplifying data-driven decision-making.

#### ☁️ Airflow
 Airflow is used for managing ETL workflows , monitoring data and computing workflows in Python. AWS EC2 Instance is used to Setup Airflow in this Project.

## Airflow EC2 Installation Commands

Install Airflow on EC2 Instance by using below Commands

```bash
sudo apt update
sudo apt install python3-pip
sudo apt install python3.10-venv
python3 -m venv endtoendyoutube_venv
source endtoendyoutube_venv/bin/activate
pip install --upgrade awscli
sudo pip install apache-airflow
airflow standalone
pip install apache-airflow-providers-amazon
```
    
