# OLAP-CASE
U.S NONFARM PAYROLLS

---

 U.S. Non-Farm Payrolls OLAP Dashboard

This project provides an **end-to-end pipeline** for analyzing U.S. Non-Farm Payrolls data.
It includes:

* **`extract.py`** → Extracts payroll data from a CSV file and loads it into a **PostgreSQL database**.
* **`dashboard.py`** → Interactive **Streamlit OLAP dashboard** for visualizing payroll employment trends.

---

## 🚀 Features

✅ Load & clean payroll data into PostgreSQL
✅ Interactive Streamlit dashboard
✅ Yearly average employment trends (2010–2025)
✅ 2019 vs 2020 (Mar–Dec) employment comparison
✅ Dynamic data refresh from PostgreSQL
✅ Visualizations with Plotly

---

## 📂 Project Structure

```
.
├── extract.py        # ETL script (loads CSV → PostgreSQL)
├── dashboard.py      # Streamlit app for visualization
├── nonfarm_payrolls_cleaned.csv   # Your payroll dataset
├── README.md         # Documentation
```

---

## ⚙️ Installation

1. Clone this repository:

```bash
git clone https://github.com/yourusername/nonfarm-payrolls-olap.git
cd nonfarm-payrolls-olap
```

2. Install dependencies:

```bash
pip install pandas psycopg2-binary sqlalchemy streamlit plotly
```

3. Setup PostgreSQL Database:

   * Create a PostgreSQL database (e.g., `payrolls_db`).
   * Update database connection details in both `extract.py` and `dashboard.py`:

```python
DB_HOST = "localhost"
DB_NAME = "payrolls_db"
DB_USER = "your_user"
DB_PASS = "your_password"
DB_PORT = "5432"
```

---

## 📥 Load Data (ETL)

Run the **extract.py** script to load your CSV into PostgreSQL:

```bash
python extract.py
```

Expected output:

```
✅ Data successfully loaded into PostgreSQL!
```

---

## 📊 Run Dashboard

Start the Streamlit app:

```bash
streamlit run dashboard.py
```

Open your browser at: [http://localhost:8501](http://localhost:8501)

---

## 📈 Dashboard Insights

* **Average Employment by Year (2010–2025)**
  Line chart showing yearly employment trends.

* **2019 vs 2020 Comparison (Mar–Dec)**
  Grouped bar chart to analyze COVID-19 impact.

* **Raw Data Preview**
  Table preview of payroll dataset.

---

## 🛠️ Troubleshooting

❌ **Error: relation "nonfarm\_payrolls\_cleaned" does not exist**
✔️ Run `extract.py` first to load the data.

❌ **Database connection failed**
✔️ Check PostgreSQL credentials in both scripts.

---

## 📌 Requirements

* Python 3.8+
* PostgreSQL 12+
* Libraries: `pandas`, `psycopg2-binary`, `sqlalchemy`, `streamlit`, `plotly`

---

## 🧑‍💻 Author

Developed by **Akansha Arora** ✨
For projects, feedback, or collaboration → \[Your LinkedIn/GitHub link here]

---

👉 Do you want me to also include a **sample `nonfarm_payrolls_cleaned.csv` generator script** inside the README so anyone can test the dashboard even without real payroll data?
