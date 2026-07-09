# Credit Card Transaction Analysis Report

A comprehensive Power BI solution designed to analyze credit card transactions, detect spending patterns, assess user demographics, and monitor financial KPIs. This repository contains the source Power BI template (`.pbix`), background assets, and architectural theme configurations.

## 📊 Business Insights & Key Features

* **Transaction Volume & Value KPIs**: Real-time snapshot of overall credit card utilization, average transaction value, and processing fees.
* **Demographic Segmentation**: Deep dive into customer spending behavior categorized by age groups, income levels, gender, and geographic location.
* **Expense Categorization**: Visual breakdown of high-volume spend categories (e.g., travel, entertainment, groceries, retail).
* **Temporal Trends**: Historical timeline analysis showcasing spending peaks, seasonal trends, and monthly growth patterns.
* **Risk & Security Context**: Built-in data models prepared for fraud detection patterns and high-risk transaction flags.

---

## 🛠️ Repository Structure

* `CREDIT_CARD_TRANSACTION_REPORT.pbix`: The core Power BI project file housing the dashboard layouts, data transformations (Power Query), and DAX measures.
* `Report/Layout`: Serialized structural and configuration files detailing visual object placement and canvas behavior.
* `Report/StaticResources/`: Contains layout design templates, custom icon sets, and specialized background textures (`BG1244781274747443023.jpg`).
* `Report/StaticResources/SharedResources/BaseThemes/`: Houses custom JSON theme files (`CY26SU02.json`) governing color palettes, font hierarchies, and semantic branding.
* `DataModel`: Binary schema defining the relationships, data types, and row-level security parameters.

---

## 📐 Data Architecture & Schema

The report leverages a highly optimized **Star Schema** to ensure high performance over large transaction datasets:

* **Fact Table**: `Fact_Transactions` (containing transaction amounts, unique IDs, timestamps, and geolocation keys).
* **Dimension Tables**:
    * `Dim_Customers`: Customer demographics, card types, and credit limits.
    * `Dim_Date`: Standard financial calendar details including fiscal periods, quarters, and days.
    * `Dim_Categories`: Granular classification codes for merchants and card expenses.

---

## 🚀 Getting Started & Usage

### Prerequisites
* Microsoft Power BI Desktop (Latest Edition recommended)
* Access to the underlying transactional data source (SQL Server, Excel, or cloud storage as mapped in Power Query).

### Local Setup
1.  **Clone the Repository**:
    ```bash
    git clone [https://github.com/your-username/credit-card-transaction-report.git](https://github.com/your-username/credit-card-transaction-report.git)
    ```
2.  **Open the Project**: Double-click the `CREDIT_CARD_TRANSACTION_REPORT.pbix` file to open it in Power BI Desktop.
3.  **Refresh Data**: Navigate to the `Home` tab and click **Refresh** to populate the report with your local or cloud data stream.

---

## 🛡️ Security & Compliance
The semantic data model includes placeholders for **Row-Level Security (RLS)** configurations (`SecurityBindings`), ensuring that sensitive financial metrics are only visible to authorized regional managers or compliance teams.
