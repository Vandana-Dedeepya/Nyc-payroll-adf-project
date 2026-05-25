# NYC Payroll Data Integration Pipeline (Azure Data Factory)

## 📌 Project Overview

This project demonstrates an end-to-end data integration pipeline using **Azure Data Factory (ADF)** to process NYC Payroll data. The pipeline extracts, transforms, and loads (ETL) payroll data from Azure Data Lake Storage into Azure SQL Database and generates aggregated insights.

---

## 🏗️ Architecture

* **Source**: Azure Data Lake Storage Gen2 (ADLS)
* **Processing**: Azure Data Factory Data Flows
* **Destination**: Azure SQL Database
* **Pipeline Orchestration**: Azure Data Factory Pipeline

---

## 🔗 Linked Services

* `ls_adls` → Connects to Azure Data Lake Storage Gen2
* `ls_sql` → Connects to Azure SQL Database

---

## 📦 Datasets

Includes datasets for:

* Employee data (`ds_emp`)
* Agency data (`ds_agency`)
* Title data (`ds_title`)
* Payroll data (`ds_payroll2020`, `ds_payroll2021`)
* SQL destination datasets (`ds_sql_*`)

---

## 🔄 Data Flows

* `df_emp` → Processes employee data
* `df_agency` → Processes agency data
* `df_title` → Processes title data
* `df_payroll2020` → Processes 2020 payroll data
* `df_payroll2021` → Processes 2021 payroll data
* `df_summary` → Aggregates payroll data by Agency and Fiscal Year

---

## 🔁 Pipeline

* **pipeline_nyc_payroll**

  * Orchestrates execution of all data flows
  * Uses parameter: `dataflow_param_fiscalyear`

---

## 📊 Output

Final output table:

* `NYC_Payroll_Summary`
* Contains aggregated payroll insights:

  * Fiscal Year
  * Agency Name
  * Total Paid

---

## 📁 Repository Structure

```
Nyc-payroll-adf-project/

├── linkedService/
├── dataset/
├── dataflow/
├── pipeline/
├── factory/
├── screenshots/
└── README.md
```

---

## 📸 Screenshots Included

* SQL Tables and Output
* Linked Services Configuration
* Dataset and Dataflow Design
* Pipeline Design
* Pipeline Execution with Timestamp

---

## ⚙️ Technologies Used

* Azure Data Factory
* Azure Data Lake Storage Gen2
* Azure SQL Database
* SQL
* ETL Pipelines

---

## ✅ Project Status

✔ Completed
✔ Pipeline executed successfully
✔ Output verified in SQL Database

---

## 👩‍💻 Author

Vandana Dedeepya
