# 🧠 AI Resume Analyzer
A powerful AI-driven resume analyzer built using Streamlit and Natural Language Processing. This app parses resumes in PDF format, extracts key information, scores them based on industry best practices, and recommends skills, certifications, and video resources. It also stores feedback and analytics using a MySQL database.

---

## 🚀 Features
- 📄 PDF Resume Parsing and Analysis  
- 🧠 Skill Extraction and Job Role Prediction  
- 📊 Resume Scoring Based on Key Sections  
- 🎓 Course & Skill Recommendations  
- 🎥 Resume and Interview Tips via YouTube  
- 📍 Auto-detection of User Location Info  
- 📈 Admin Dashboard with Usage Analytics  
- 💬 Feedback System with Rating & Comments  
- 💾 Data Storage in MySQL  

---

## 📁 Folder Structure
```
.
├── App.py                   # Main Streamlit app
├── Courses.py               # Course & video data
├── requirements.txt         # Python dependencies
├── Logo/
│   ├── Logo.png             # Main logo
│   └── icon.png             # Favicon
├── Uploaded_Resumes/        # Stores uploaded resumes
```

---

## 🛠️ Setup Instructions

### 1. 📦 Install Python Packages

```bash
pip install -r requirements.txt
```

### 2. 🧩 MySQL Database Setup

Make sure MySQL is installed and running. Then, create the required database:

```sql
CREATE DATABASE IF NOT EXISTS cv;
```

> The app auto-creates tables: `user_data` and `user_feedback` on first run.

Update MySQL credentials in `App.py` if necessary:

```python
pymysql.connect(host='localhost', user='root', password='Workbench@369', db='cv')
```

### 3. 📂 Prepare Assets

Ensure the following exist:

- `./Logo/Logo.png`
- `./Logo/icon.png`
- `./Uploaded_Resumes/` (empty folder for resumes)

---

## ▶️ Running the App
```bash
streamlit run App.py
```

## 🧑‍💼 How to Use

### Sidebar Options:

- **User**: Upload your resume and get insights & recommendations.  
- **Feedback**: Submit your rating and suggestions.  
- **About**: Learn more about how the tool works.  
- **Admin**: Access visual analytics and database reports.

### 🔐 Admin Login:

- **Username**: `admin`  
- **Password**: `admin@resume-analyzer`

---

## 🧠 Tech Stack

- **Frontend**: Streamlit  
- **Backend**: Python, PyMySQL  
- **NLP**: NLTK, PyResparser  
- **PDF Parsing**: PDFMiner  
- **DataViz**: Plotly  
- **Geo & Location**: Geocoder, Geopy
