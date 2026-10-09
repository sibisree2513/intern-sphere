# InternSphere — AI-Powered Internship Finder Agent 🎓

**InternSphere** is a complete, runnable Python + Streamlit web application designed to help students match, filter, and track internship opportunities based on transparent heuristic scoring algorithms and custom profile attributes.

---

## ✨ Key Features

1. **📊 Saas Dashboard**: High-level visual metrics, active matches count, high-compatibility filter, saved role tracker, upcoming deadlines, and top recommendations.
2. **👤 Interactive Student Profile**: Real-time configuration of target department, core skills list, work mode (Remote, Hybrid, Onsite), minimum monthly stipend, and duration constraints.
3. **🔍 Multi-Parametric Find & Match**: Keyword search across titles, companies, and skills. Filter by department, work mode, and stipend. Includes transparent "Why this matches your profile" explanations.
4. **🧠 Transparent Heuristic Matching Engine**: Deterministic 0–100 compatibility scoring engine based on:
   - **Required Skills Match** (35%)
   - **Preferred Skills Bonus** (15%)
   - **Department Alignment** (20%)
   - **Work Mode & Location Fit** (15%)
   - **Stipend & Duration Fit** (15%)
5. **📝 Daily Reports & Export**: One-click exports for dated **CSV** and executive **TXT** summaries.
6. **🧪 In-App & CLI Automated Test Suite**: Integrated test runner verifying 6 automated test scenarios (Normal Search, Duplicate Removal, Missing Data Handling, Source Failures, Expired Filtering, Empty Result Handling).

---

## 🛠️ Technology Stack

- **Python**: 3.10+
- **Frontend / UI**: Streamlit with Custom CSS (Indigo & Violet Palette, Glassmorphism, Google Font Outfit/Inter)
- **Data Manipulation**: Pandas, JSON
- **Automated Testing**: Pytest

---

## 📂 Project Architecture

```
internsphere/
├── app.py                      # Main Streamlit SaaS application
├── requirements.txt            # Project dependencies
├── README.md                   # Setup guide and documentation
├── .gitignore                  # Git ignore rules
├── agent/
│   ├── __init__.py
│   ├── matching.py             # Match score calculation & transparent breakdown
│   ├── deduplication.py        # Deduplication & expired deadline filter
│   ├── sources.py              # Extensible job connector interface & JSON loader
│   └── report.py               # CSV & TXT daily report generators
├── data/
│   └── sample_internships.json # Fictional sample internship dataset (12 records)
└── tests/
    ├── test_matching.py        # Pytest matching engine tests
    ├── test_deduplication.py   # Pytest deduplication & expiry tests
    └── test_sources.py        # Pytest data source & error handling tests
```

---

## 🚀 Quickstart & VS Code Setup Commands

### Step 1: Open Terminal in Project Directory
Navigate into the `internsphere` project folder:
```bash
cd C:\Users\admin\.gemini\antigravity\scratch\internsphere
```

### Step 2: Install Dependencies
Install required packages using pip:
```bash
pip install -r requirements.txt
```

### Step 3: Run Automated Test Suite
Verify that all unit tests pass:
```bash
python -m pytest
```

### Step 4: Launch Streamlit Web Application
Run the Streamlit app:
```bash
python -m streamlit run app.py
```

Open your browser at `http://localhost:8501` to access the application dashboard.

---

## ⚖️ Transparent Heuristic Disclaimer
InternSphere uses deterministic heuristic algorithms to score job fit. It does not claim to use trained neural network models or scrape external sites without explicit authorization. Fictional sample URLs (`example.com`) are provided for demonstration purposes.
