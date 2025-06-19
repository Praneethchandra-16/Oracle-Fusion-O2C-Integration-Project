# Oracle Fusion O2C Integration Project 🚀

This project showcases an end-to-end simulation of the **Order-to-Cash (O2C)** process in **Oracle Fusion Cloud Applications**, using:

* File-Based Data Import (FBDI)
* ESS Jobs (Scheduled Processes)
* BI Publisher for reporting
* Optional Bursting setup
* Oracle Integration Cloud (OIC) flow demonstration

---

## 🔄 Business Flow Covered

1. **Customer Data Import**
2. **Sales Order Data Import**
3. **ESS Jobs Execution**
4. **Validation in Fusion UI**
5. **BI Publisher Report Generation**
6. **Report Bursting (Simulated)**
7. **Oracle Integration Cloud (OIC) Simulation**

---

## 📂 Project Structure

```bash
├── CustomerImportTemplate.xlsm          # FBDI Template for Customer Master Data
├── SourceSalesOrderImportTemplate.xlsm  # FBDI Template for Sales Orders
├── arcustomerimport.zip                 # OIC Archive for Customer Data Flow (Simulation)
├── SourceSalesOrderImport.zip           # OIC Archive for Sales Order Flow (Simulation)
├── V Report.pdf                         # Sample BI Publisher Output
└── README.md
```

---

## 📅 1. Customer Data Import (FBDI)

* **Template Used**: `CustomerImportTemplate.xlsm`
* **Key Fields**:

  * Party Number
  * Customer Name
  * Site Usage
  * Account Number
* **Process**:

  * Fill out customer data
  * Upload to UCM
  * Trigger **"Import Trading Community Data"** ESS Job

---

## 🛒 2. Sales Order Import (FBDI)

* **Template Used**: `SourceSalesOrderImportTemplate.xlsm`
* **Key Fields**:

  * SOURCE\_TRANSACTION\_NUMBER
  * CUSTOMER\_PO\_NUMBER
  * BUYING\_PARTY\_NUMBER / NAME
  * PRICING\_DATE
  * SALES\_CHANNEL
* **Process**:

  * Upload to UCM
  * Trigger **"Import Sales Orders"** ESS Job

---

## ⚙️ 3. ESS Job Execution

Each FBDI file upload is followed by a scheduled process (ESS Job) to push data into Oracle Fusion Cloud. Logs and statuses are verified via Fusion UI.

---

## 📊 4. BI Publisher Reporting

* **Data Sources**: DOO\_ORDER\_HEADERS\_ALL\_INT, HZ\_PARTIES, AR\_CUSTOMERS, etc.
* **Report Features**:

  * Combined customer & order data
  * Filters for buying party number, dates, etc.
  * Exportable to PDF or Excel
* **Sample Output**: `V Report.pdf`

---

## ✉️ 5. Bursting Simulation

* Simulated Bursting setup to:

  * Distribute reports to stakeholders (e.g., by region or business unit)
  * Use XML delivery definition (not activated due to sandbox nature)

---

## 🔗 6. Oracle Integration Cloud (OIC)

* Included archived integrations (`.zip`) for:

  * Automating Customer Load
  * Automating Sales Order Load
* These simulate REST/SOAP calls to Fusion and show how Oracle Integration Cloud can be used to streamline O2C pipelines.

---

## 🛠️ Technologies Used

| Stack            | Tools / Modules                                                        |
| ---------------- | ---------------------------------------------------------------------- |
| ERP Application  | Oracle Fusion Cloud (Order Management, Trading Community Architecture) |
| Integration      | Oracle Integration Cloud (OIC)                                         |
| Data Import      | File-Based Data Import (FBDI)                                          |
| Scheduling & ETL | ESS Jobs (Scheduled Processes)                                         |
| Reporting        | Oracle BI Publisher, XML Bursting                                      |

---

## 📌 Key Learnings

* Understanding real-world O2C cycles using Oracle ERP
* Creating and validating master & transactional data via FBDI
* Using BI Publisher to extract and present insights
* Simulating business automation via Oracle Integration Cloud

---

## 👨‍💼 Author

**Praneeth Chandra Budala**
MS in Business Analytics & AI
[LinkedIn](https://www.linkedin.com/in/praneethchandra) | [GitHub](https://github.com/Praneethchandra-16)

---

## 📬 Contact

For collaboration, queries, or suggestions:
📧 [praneethbudala@gmail.com](mailto:praneethbudala@gmail.com)
📍 Dallas, TX
