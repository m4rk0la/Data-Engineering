E-commerce Sales Analysis with PySpark
📝 Project Overview
This project demonstrates a complete Data Engineering and Analysis pipeline using the Apache Spark framework with the PySpark API. The goal was to process and analyze a large volume of e-commerce sales data to extract valuable business insights on sales performance and seasonality.

The work was performed within a Databricks environment, which facilitates distributed processing and collaboration.

🎯 Project Goals
Build an ETL (Extract, Transform, Load) pipeline to process sales data.

Clean and prepare raw data for analysis.

Perform aggregations and transformations to answer business questions.

Visualize the results to identify trends and sales patterns.

🛠️ Technologies Used
Apache Spark (PySpark): A distributed computing framework for large-scale data processing.

Databricks Community Edition: A cloud-based data analytics platform used as the execution environment.

Python: The programming language used for data manipulation.

Matplotlib: A data visualization library (optional, for custom plots).

📊 Dataset
This project uses the "Online Retail" dataset, available on Kaggle, which contains transactional data from a UK-based online retailer.

Source: Online Retail Dataset - Kaggle

⚙️ Project Steps
The data pipeline was divided into the following sequential phases:

Extract:

The CSV file was uploaded to Databricks and read into a Spark DataFrame.

Table reading (spark.read.table()) was used to access the data after the initial upload.

Data Cleaning:

Null values in the CustomerID column were removed.

The InvoiceDate column was cast to the Timestamp data type to enable time-series analysis.

Invalid records (negative quantities or unit prices) were filtered out.

Transform & Analysis:

A new TotalPrice column was created by multiplying Quantity by UnitPrice.

New columns (Year and Month) were extracted from InvoiceDate.

Aggregations were performed to calculate the total revenue per product and the total monthly revenue, answering key business questions.

Visualization:

Bar and line charts were generated to visualize the monthly revenue trend and the top-selling products.

📈 Key Findings
Strong Seasonality: Sales showed a clear upward trend in the second half of the year.

Sales Peak: November was the month with the highest revenue, indicating the strong influence of seasonal events like Black Friday.

Specific Dips: Notable drops in sales occurred in months two and four, which could be investigated in future analyses.

🚀 How to Run the Project
Create a free account on Databricks Community Edition.

Upload the OnlineRetail.csv file via the Databricks UI.

Create a new notebook and follow the code steps outlined in this repository.

✍️ Author
Marco Antônio - www.linkedin.com/in/marco-antônio-rodrigues-teixeira
