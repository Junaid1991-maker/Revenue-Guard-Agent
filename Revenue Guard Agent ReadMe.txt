# Revenue Guard Agent 🛡️
**Automated Financial Anomaly Detection System**

A lightweight, high-performance Python agent designed to monitor transaction streams, detect financial leaks, and flag suspicious activity using statistical modeling.

## 🚀 Project Overview
The **Revenue Guard Agent** was developed to solve the challenge of monitoring high-volume transaction data (50,000+ records) on standard consumer hardware. It utilizes a "Lean-SQL" architecture to balance deep data analysis with system responsiveness.

### Key Features:
* **Memory Optimized:** Implements data downcasting (`int64` to `int32`) and vectorized NumPy operations, reducing memory footprint by **50%**.
* **Security Focused:** Built with **parameterized SQL queries** to prevent SQL injection attacks—adhering to enterprise-grade security standards.
* **Statistical Intelligence:** Uses **Z-Score (3sigma) analysis** to isolate true anomalies from natural business variance.
* **Scalable Storage:** Utilizes a disk-based **SQLite** backend to handle datasets larger than available RAM.

---

## 🛠️ Tech Stack & Optimization
* **Language:** Python 3.x
* **Data Handling:** Pandas, NumPy
* **Database:** SQLite3 (Relational Storage)
* **Visualization:** Matplotlib (Memory-efficient rendering)
* **Hardware Target:** Optimized for Intel i5 / 16GB RAM (Dell Latitude 5490)

---

## 📊 Performance Metrics
| Component | Optimization | Result |
| :--- | :--- | :--- |
| **Data Storage** | Downcasting to `float32` | 0.81 MB per 50k rows |
| **Detection Speed** | Vectorized Operations | Sub-second execution |
| **Security** | Parameterized Placeholder `?` | Protected vs SQL Injection |

---

## 🔍 How It Works
1.  **Data Ingestion:** Generates/Imports synthetic transaction data with injected "Attack" patterns (spikes and drops).
2.  **SQL Guard:** Data is moved to a local `.db` file to keep the Jupyter environment snappy.
3.  **Anomaly Detection:** The agent calculates the mean and standard deviation across the stream, flagging any point beyond the $3.0$ threshold.
4.  **Visual Audit:** Generates a high-contrast dashboard highlighting the **43 flagged anomalies** for human review.

---

## 📝 Ethical Statement
*This project uses 100% synthetic data and public industry benchmarks. It contains no proprietary business logic or sensitive credentials, demonstrating professional ethics regarding IP protection and non-disclosure.*

---
**Developer:** [Junaid](https://github.com/Junaid1991-maker)  
**Project:** Portfolio / Revenue Guard Agent