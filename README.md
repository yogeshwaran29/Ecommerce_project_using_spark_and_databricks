# Ecommerce_data_pipiline_using_spark_and_databricks
An end-to-end data engineering project using Apache Spark, Databricks, Azure ADLS, and Power BI. This includes transforming raw CSV data through bronze, silver, and gold layers, culminating in a Power BI dashboard for business insights.

---

## **Problem Statement**

ShopVista is a fast growing ecommerce company, while the business is growing fast the executive team here is having struggle in terms of getting the overall insights
on the state of the business. This is happening because they don't have a central Data Engineering practice in place. Their teams are working in silo's and they have scattered data in databases and files. Whenever operation team wants to get insights, they have to talk to multiple teams to get the data and they will join them together manually. To overcome this problem the organization management decided to onboard data engineering practice and they have started this particular project.

---

## **Technical Architecture**

![img.png](project_architecture.png)

The above diagram represents the technical architecture of our project. Here We have our company's database which is a OLTP system and some files which store the company day to day transactions. From this OLTP system through a scheduled job the data will be dropped into our data lake(ADLS) as CSV Files. Then we will connect the ADLS data lake to databricks through Azure access connector. Inside Databricks we will have Bronze, Silver and Gold layers , in Bronze layer we will have raw data , in Silver we will do data cleaning and transform the data, in Gold we will generate new columns for better insights and in Gold Layer we will have our BI ready data. Then we will attach Data Visualization tool PowerBi to visualize and generate insights.

---

## 🎯 **Objectives**

- Automate ingestion of e-commerce data (orders, returns, shipments, dimensions)  
- Standardize and clean data for consistency across all layers  
- Build an analytics-ready data model integrated with **Power BI**  
- Enable scalable and auditable governance with **Unity Catalog**

---

## 🧰 **Tools & Technologies**

| **Layer**       | **Tool / Service**                | **Purpose**                                      |
|-----------------|-----------------------------------|-------------------------------------------------|
| **Ingestion**   | Databricks Autoloader (Structured Streaming) | Incremental data loading from ADLS               |
| **Storage**     | Azure Data Lake Storage (ADLS Gen2) | Centralized data repository                      |
| **Processing**  | Azure Databricks (PySpark)    | ETL and transformation                           |
| **Governance**  | Unity Catalog                | Centralized access control and schema registry  |
| **Visualization** | Power BI                      | BI dashboards and reports                        |

---

## ✅ **Outcomes**

- ⏱️ Automated daily & monthly ingestion using Autoloader 
- 🧩 Unified and governed schemas via Unity Catalog  
- ⚙️ Simplified data transformations (PySpark & Delta)  
- 📊 Real-time insights in Power BI 
- 🚀 Scalable architecture  
