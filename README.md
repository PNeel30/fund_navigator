# 💰 Fund Navigator

A smart **Streamlit-based investment recommendation system** that suggests optimal mutual funds based on user profile and financial metrics like Sharpe ratio, Beta, Alpha, and risk measures.

---

## ✨ Features

* 📊 Data-driven mutual fund analysis
* 🎯 Personalized fund recommendations
* 📈 Risk assessment using financial indicators (Sharpe, Beta, Sortino)
* ⚡ Interactive UI built with Streamlit
* 🔄 Dynamic session-based user inputs
* 🧮 Automated fund selection logic

---

## 🏗️ Architecture

```
User Input (Age, Investment Amount)
            ↓
    Streamlit Frontend (app.py)
            ↓
   Data Processing (functions.py)
            ↓
   Financial Metrics Filtering
            ↓
   Recommendation Engine
            ↓
      Suggested Funds Output
```

---

## 📂 Project Structure

```
fund_navigator/
│── app.py               # Streamlit application entry point
│── functions.py        # Core logic & recommendation functions
│── Analysis.ipynb      # Data exploration & analysis
│── data.csv            # Mutual fund dataset
│── README.md           # Project documentation
```

---

## 🚀 Quick Start

```bash
git clone <your-repo-link>
cd fund_navigator
pip install -r requirements.txt
```

---

## ⚙️ Setup Instructions

### 1️⃣ Install Dependencies

```bash
pip install streamlit pandas
```

### 2️⃣ Ensure Dataset

* Place `data.csv` in the root directory
* Dataset should include:

  * sharpe
  * beta
  * alpha
  * sortino
  * sd

### 3️⃣ Run Application

```bash
streamlit run app.py
```

---

## ▶️ How It Works

1. User enters:

   * Age
   * Investment amount

2. System:

   * Cleans dataset (removes invalid values like '-')
   * Converts financial metrics to numeric
   * Applies filtering logic

3. Output:

   * Recommended mutual funds based on:

     * Risk profile
     * Performance indicators

---

## 📡 Core Logic (functions.py)

| Function      | Description                                   |
| ------------- | --------------------------------------------- |
| `options()`   | Provides filtering criteria                   |
| `calculate()` | Processes financial metrics & recommendations |

---

## 🛠️ Tech Stack

| Category        | Technology       |
| --------------- | ---------------- |
| Frontend        | Streamlit        |
| Backend Logic   | Python           |
| Data Processing | Pandas           |
| Analysis        | Jupyter Notebook |

---

## 🎯 Design Decisions

* **Streamlit used** → Fast prototyping of data apps without frontend complexity
* **Pandas for processing** → Efficient handling of financial datasets
* **Metric-based filtering** → Ensures recommendations are data-driven
* **Session state management** → Maintains user interaction flow

---

## 🔐 Security Best Practices

* Input validation via Streamlit controls
* No hardcoded sensitive data
* Clean handling of missing/invalid dataset values
* Safe type conversion for financial metrics

---

## 🚀 Future Improvements

* 🤖 Add ML-based recommendation model
* 📊 Visualize fund performance with charts
* 🌐 Deploy on Streamlit Cloud / AWS
* 👥 Add user login & portfolio tracking
