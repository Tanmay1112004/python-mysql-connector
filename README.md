# 🐍 Python MySQL Connector 🔌

![Python Version](https://img.shields.io/badge/python-3.8%2B-blue)
![MySQL Version](https://img.shields.io/badge/mysql-5.7%2B-orange)
![License](https://img.shields.io/badge/license-MIT-green)

A modern **Python interface for MySQL** designed for clean, efficient, and secure database operations. Includes **connection pooling**, **context manager support**, and **ready-to-use CRUD templates** for faster development.


## ✨ Features

* **Connection Pooling**: Efficiently handle multiple database connections for high-performance applications.
* **Secure Credential Management**: Environment variable support for keeping credentials safe.
* **CRUD Operation Templates**: Easily perform `SELECT`, `INSERT`, `UPDATE`, `DELETE`.
* **Context Managers**: Automatic connection opening and closing with Python `with` syntax.
* **Type Hints**: Full type hint support for better code quality.
* **Error Handling**: Comprehensive exception management for robust applications.

---

## 🛠️ Requirements

* Python 3.8+
* MySQL Server 5.7+
* Packages: `mysql-connector-python`, `python-dotenv`, `pytest`

---

## 🚀 Installation

1. Clone the repository:

```bash
git clone https://github.com/Tanmay1112004/python-mysql-connector.git
cd python-mysql-connector
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Configure environment variables:

```bash
cp .env.example .env
# Edit .env with your MySQL credentials
```

---

## ⚡ Usage Example

```python
from db_connector import MySQLConnector

# Initialize connector
db = MySQLConnector(
    host="localhost",
    user="admin",
    password="secure_password",
    database="app_db",
    pool_size=5
)

# Execute query safely
with db.connection() as conn:
    results = conn.execute_query(
        "SELECT * FROM users WHERE id = %s", 
        (user_id,)
    )
    print(results)
```

---

## ⚙️ Configuration

Rename `.env.example` to `.env` and fill in your database credentials:

```env
DB_HOST=localhost
DB_USER=admin
DB_PASSWORD=secure_password
DB_NAME=app_db
POOL_SIZE=5
```

---

## 📦 Project Structure

```text
.
├── db_connector.py       # Core connector class
├── examples/             # Usage examples
├── tests/                # Pytest unit tests
├── requirements.txt      # Project dependencies
└── .env.example          # Environment variable template
```

---

## 🧪 Testing

Run unit tests using **pytest**:

```bash
pytest tests/
```

---

## 🔑 Why This Project Matters

* Demonstrates **full-stack backend skills** with Python and MySQL.
* Shows knowledge of **connection pooling, context management, and secure credential handling**.
* Ideal for **data engineers, backend developers, and software engineers** building scalable applications.

---

## 📄 License

MIT License — see [LICENSE](LICENSE) file.

---

## 👤 Author

**Tanmay Kshirsagar**
📧 [tanmaykshirsagar001@gmail.com](mailto:tanmaykshirsagar001@gmail.com)
💻 GitHub: [https://github.com/Tanmay1112004](https://github.com/Tanmay1112004)

---
