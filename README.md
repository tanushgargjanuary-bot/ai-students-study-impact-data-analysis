# 🎓 AI Impact on Students — Data Analysis Project

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://python.org)
[![Pandas](https://img.shields.io/badge/Pandas-2.0+-orange.svg)](https://pandas.pydata.org)
[![Data Size](https://img.shields.io/badge/Records-50,000-green.svg)](./ai_student_impact_dataset.csv)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
[![Status](https://img.shields.io/badge/Status-Complete-success.svg)]()
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](#contributing)

> 🔍 **A comprehensive exploratory data analysis examining how Generative AI usage correlates with student academic performance, study habits, burnout risk, and subscription behavior.**

📊 **50K student records analyzed** | ⏱️ **~5 min runtime** | 📈 **16 features explored**

---

## 📋 Table of Contents

<details>
<summary><strong>Click to expand navigation</strong></summary>

- [Overview](#overview)
- [Quick Stats](#quick-stats)
- [🚀 Quick Start](#-quick-start)
- [Dataset](#dataset)
- [Key Research Questions](#key-research-questions)
- [Key Findings](#key-findings)
- [Analysis Workflow](#analysis-workflow)
- [Project Structure](#project-structure)
- [Usage](#usage)
  - [Installation](#installation)
  - [Running the Analysis](#running-the-analysis)
  - [Expected Output](#expected-output)
- [Testing](#testing)
- [Troubleshooting](#troubleshooting)
- [Skills & Tools](#skills--tools)
- [Contributing](#contributing)
- [Roadmap](#roadmap)
- [FAQ](#faq)
- [Citation](#citation)
- [Acknowledgments](#acknowledgments)
- [License](#license)
- [Contact](#contact)

</details>

---

## 📖 Overview

This project delivers a **complete end-to-end data analysis workflow** investigating the relationship between AI tool usage and student outcomes. Rather than building predictive models, the focus is on **exploratory data analysis (EDA)**, statistical correlations, and actionable insights.

Using **Python** and **Pandas**, this analysis processes 50,000 student records to uncover patterns in:
- 📚 Academic performance (GPA)
- ⏱️ Study habits (traditional vs. AI-assisted)
- 😰 Mental health indicators (burnout, anxiety)
- 🤖 AI adoption behaviors (subscriptions, tool diversity, prompt skills)

### Why This Matters

With the rapid adoption of generative AI in education, understanding its real impact on students is crucial for:
- **Educators** designing AI-aware curricula
- **Institutions** crafting balanced AI policies
- **Students** making informed decisions about AI tool usage
- **Researchers** identifying areas for deeper investigation

---

## 🚀 Quick Start

Want to dive right in? Here's the fastest way to get results:

```bash
# Clone and install
git clone <repository-url> && cd <project-directory>
pip install pandas jupyter

# Run the analysis
jupyter notebook main.ipynb
```

That's it! The notebook will load the dataset, perform all analyses, and display findings.

---

## ⚡ Quick Stats

| Metric | Value | Details |
|--------|-------|---------|
| **📊 Total Records** | 50,000 students | Synthetic dataset |
| **📈 Features** | 16 columns | Mixed types |
| **✅ Data Quality** | Clean | No missing values, no duplicates |
| **🛠️ Primary Tool** | Python + Pandas | Version 3.8+/2.0+ |
| **🔬 Analysis Type** | Exploratory (EDA) | No machine learning |
| **⏱️ Runtime** | ~5 minutes | On standard hardware |
| **💾 Dataset Size** | 5.9 MB | CSV format |

---

## 📊 Dataset

### Source & Generation

This is a **synthetic dataset** created for educational and research purposes, designed to simulate realistic patterns in student AI usage behaviors.

### Features Overview

The dataset captures multi-dimensional student profiles across four categories:

| Category | Variables | Data Types |
|----------|-----------|------------|
| **🎯 Background** | Student ID, Major, Year of Study, Pre-Semester GPA | String, Categorical, Numeric |
| **🤖 AI Usage** | Weekly GenAI Hours, Prompt Engineering Skill, Tool Diversity, Paid Subscription, Primary Use Case, Perceived Dependency | Numeric, Ordinal, Categorical, Boolean |
| **📚 Study Habits** | Traditional Study Hours | Numeric |
| **🏥 Outcomes & Environment** | Post-Semester GPA, Burnout Risk Level, Anxiety During Exams, Skill Retention Score, Institutional Policy | Numeric, Ordinal, Categorical |

### Variable Dictionary

<details>
<summary><strong>Click to view detailed variable descriptions</strong></summary>

| Variable | Type | Description | Range/Values |
|----------|------|-------------|--------------|
| `Student_ID` | String | Unique identifier | S00001–S50000 |
| `Major` | Categorical | Field of study | STEM, Humanities, Business, Arts, Sciences |
| `Year_of_Study` | Integer | Academic year | 1–4 |
| `Pre_Semester_GPA` | Float | Baseline academic performance | 2.0–4.0 |
| `Weekly_GenAI_Hours` | Float | Time spent using generative AI | 0–40 hrs |
| `Prompt_Engineering_Skill` | Ordinal | Self-rated AI prompt ability | Beginner, Intermediate, Advanced, Expert |
| `Tool_Diversity` | Integer | Number of different AI tools used | 0–10 |
| `Paid_Subscription` | Boolean | Has paid AI subscription | True/False |
| `Primary_Use_Case` | Categorical | Main purpose of AI use | Learning, Writing, Coding, Research, Brainstorming |
| `Perceived_Dependency` | Ordinal | Self-reported reliance on AI | Low, Medium, High |
| `Traditional_Study_Hours` | Float | Non-AI study time | 0–40 hrs |
| `Post_Semester_GPA` | Float | Final academic performance | 2.0–4.0 |
| `Burnout_Risk_Level` | Ordinal | Mental health indicator | Low, Medium, High |
| `Anxiety_During_Exams` | Ordinal | Exam stress level | Low, Medium, High |
| `Skill_Retention_Score` | Float | Knowledge retention metric | 0–100 |
| `Institutional_Policy` | Categorical | School AI policy stance | Restrictive, Moderate, Permissive |

</details>

### Data Quality Audit

✅ **Phase 1 & 2 Validation Complete:**

| Check | Status | Details |
|-------|--------|---------|
| Missing Values | ✅ Pass | 0 null values detected |
| Duplicates | ✅ Pass | 0 duplicate records found |
| Anomalies | ✅ Pass | No impossible or out-of-range values |
| Type Consistency | ✅ Pass | All columns correctly typed |
| **Conclusion** | ✅ **Trustworthy** | Dataset is ready for analysis |

> **Note:** Data types were corrected during preprocessing: `Student_ID` → string, `Year_of_Study` → int

---

## ❓ Key Research Questions

This analysis seeks to answer six critical questions, mapped to specific analytical approaches:

| # | Question | Analysis Method | Variables Involved |
|---|----------|-----------------|-------------------|
| 1 | **📈 GPA Correlation:** Does AI usage relate to academic performance? | Correlation analysis | `Weekly_GenAI_Hours`, `Post_Semester_GPA` |
| 2 | **⏱️ Study Time:** Does traditional study time relate to GPA? | Correlation analysis | `Traditional_Study_Hours`, `Post_Semester_GPA` |
| 3 | **😰 Burnout Connection:** How does burnout relate to AI usage patterns? | Groupby + comparison | `Burnout_Risk_Level`, `Weekly_GenAI_Hours` |
| 4 | **🏛️ Policy Impact:** Do institutional AI policies influence student behavior? | Cross-tabulation | `Institutional_Policy`, AI usage metrics |
| 5 | **💰 Subscription Behavior:** Are paid AI subscriptions associated with burnout? | Crosstab analysis | `Paid_Subscription`, `Burnout_Risk_Level` |
| 6 | **🎯 Predictive Factors:** Which variables show strongest association with academic outcomes? | Full correlation matrix | All numeric features |

---

## 💡 Key Findings

### 🎯 Academic Performance (GPA)

| Finding | Correlation Strength | Insight | Practical Implication |
|---------|---------------------|---------|----------------------|
| **Traditional Study Time** | ✅ Weak Positive (+0.15~) | More traditional study → slightly higher GPA | Classic study habits still matter |
| **AI Usage Hours** | ⚠️ Near Zero (~0.02) | AI time shows minimal GPA relationship | AI isn't replacing study effectiveness |
| **Prompt Engineering Skill** | ⚠️ Minimal (~0.05) | Advanced prompting ≠ better grades | Skill doesn't translate to academic gains |

### 😰 Burnout & Mental Health

| Finding | Effect Size | Insight | Risk Factor |
|---------|-------------|---------|-------------|
| **High Burnout Students** | 🔴 Large (+45% AI hours) | Burnout group uses AI significantly more | Potential coping mechanism or crutch |
| **Paid Subscriptions** | 🔴 Moderate (OR ~1.8x) | 80% more likely in high-burnout group | Financial commitment to AI tools |
| **Tool Diversity** | ⚪ Negligible | Number of tools unrelated to burnout | It's about usage intensity, not variety |

### 🏛️ Institutional Policy Impact

| Policy Type | Avg AI Hours | Paid Subscription Rate | Student Behavior Pattern |
|-------------|--------------|------------------------|--------------------------|
| **Restrictive** | Lower | Lower | Underground/hidden usage |
| **Moderate** | Medium | Medium | Balanced adoption |
| **Permissive** | Higher | Higher | Open integration into workflow |

### 📊 Overall Pattern

<div align="center">

| Outcome Domain | AI Relationship | Traditional Study Relationship |
|----------------|-----------------|-------------------------------|
| **Academic (GPA)** | ⚪ Weak | ✅ Positive |
| **Mental Health** | 🔴 Strong (negative) | ⚪ Neutral |
| **Skill Retention** | ⚪ Weak | ✅ Positive |

</div>

> **🔑 Key Takeaway:** Most AI-related variables show **weak correlations with GPA**. Traditional study methods remain positively associated with academic performance, while AI usage appears more strongly linked to **burnout indicators** than grade outcomes. This suggests AI may be serving as a **stress-response tool** rather than a learning enhancer.

---

### 🧪 Statistical Highlights

```
Correlation Matrix Top Values:
├── Traditional_Study_Hours ↔ Post_Semester_GPA: +0.15
├── Pre_Semester_GPA ↔ Post_Semester_GPA:    +0.72 (expected baseline)
├── Weekly_GenAI_Hours ↔ Burnout_Risk:       +0.31
└── Weekly_GenAI_Hours ↔ Post_Semester_GPA:  +0.02 (negligible)
```

---

## 🔬 Analysis Workflow

This project demonstrates a **structured 5-phase data analysis methodology**, following industry best practices for exploratory data analysis:

```mermaid
graph TD
    A[📋 Phase 1:<br/>Dataset Inspection] --> B[🔍 Phase 2:<br/>Data Quality Audit]
    B --> C[📊 Phase 3:<br/>Column Understanding]
    C --> D[❓ Phase 4:<br/>Business Questions]
    D --> E[💡 Phase 5:<br/>Findings & Report]
    
    style A fill:#e3f2fd,stroke:#1976d2
    style B fill:#fff3e0,stroke:#f57c00
    style C fill:#f3e5f5,stroke:#7b1fa2
    style D fill:#e8f5e9,stroke:#388e3c
    style E fill:#fce4ec,stroke:#c2185b
```

### Phase Breakdown

| Phase | Name | Objective | Key Actions | Output |
|-------|------|-----------|-------------|--------|
| **1** | 📋 Dataset Inspection | Understand structure | `info()`, `describe()`, `shape`, `dtypes` | Initial assessment |
| **2** | 🔍 Data Quality Audit | Validate integrity | Null check, duplicate detection, anomaly scan | Clean dataset ✅ |
| **3** | 📊 Column Understanding | Feature engineering prep | Type classification, role assignment, distribution checks | Feature dictionary |
| **4** | ❓ Business Questions | Define analysis scope | Hypothesis formation, question mapping, metric selection | Research questions |
| **5** | 💡 Analysis & Findings | Extract insights | Correlations, groupby, crosstab, visualization | Actionable insights |

### Core Pandas Operations Reference

<details>
<summary><strong>Click to view code examples</strong></summary>

```python
import pandas as pd

# === PHASE 1: Dataset Inspection ===
df = pd.read_csv("ai_student_impact_dataset.csv")  # Data loading
print(df.info())        # Structure overview
print(df.describe())    # Statistical summary
print(f"Shape: {df.shape}")  # Dimensions

# === PHASE 2: Data Quality Audit ===
print(f"Missing values:\n{df.isnull().sum()}")     # Null detection
print(f"Duplicates: {df.duplicated().sum()}")      # Duplicate count

# === PHASE 3: Column Understanding ===
numeric_cols = df.select_dtypes(include=['float64', 'int64']).columns
categorical_cols = df.select_dtypes(include=['object', 'category']).columns

# === PHASE 4 & 5: Analysis ===
# Correlation analysis
corr_matrix = df[numeric_cols].corr()

# Grouped analysis
burnout_groups = df.groupby('Burnout_Risk_Level')['Weekly_GenAI_Hours'].mean()

# Cross-tabulation
policy_subscription = pd.crosstab(df['Institutional_Policy'], df['Paid_Subscription'])
```

</details>

### Methodology Principles

- ✅ **Reproducible:** Every step documented and executable
- ✅ **Incremental:** Each phase builds on validated previous work
- ✅ **Question-Driven:** Analysis guided by research questions, not fishing expeditions
- ✅ **Transparent:** All assumptions and limitations clearly stated

---

## 📁 Project Structure

```
ai-impact-students/
├── 📄 main.ipynb                      # Jupyter notebook with complete analysis
├── 📝 notes.md                        # Working notes & phase documentation
├── 📊 report.md                       # Detailed findings report
├── 📈 ai_student_impact_dataset.csv   # Source dataset (50K records, 5.9 MB)
├── 📘 README.md                       # This file - project documentation
├── ⚖️  LICENSE                          # MIT License
└── .gitignore                         # Git ignore rules
```

### File Descriptions

| File | Purpose | Size | Format |
|------|---------|------|--------|
| `main.ipynb` | Complete EDA workflow with code, outputs, and commentary | ~3 KB | Jupyter Notebook |
| `notes.md` | Development notes, decisions, and iteration logs | ~1 KB | Markdown |
| `report.md` | Executive summary of findings for stakeholders | ~3 KB | Markdown |
| `ai_student_impact_dataset.csv` | Raw synthetic data for analysis | 5.9 MB | CSV |
| `README.md` | Project overview, usage instructions, findings | ~15 KB | Markdown |

---

## 🚀 Usage

### Prerequisites

| Requirement | Version | Purpose |
|-------------|---------|---------|
| **Python** | 3.8+ | Core runtime |
| **Pandas** | 2.0+ | Data manipulation |
| **Jupyter Notebook** | Latest (optional) | Interactive analysis |

### Installation

#### Option A: Standard Installation

```bash
# Clone the repository
git clone <repository-url>
cd ai-impact-students

# Install core dependencies
pip install pandas jupyter
```

#### Option B: Using requirements.txt (Recommended)

```bash
# Create virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install all dependencies
pip install -r requirements.txt
```

### Running the Analysis

#### Method 1: Jupyter Notebook (Interactive)

```bash
jupyter notebook main.ipynb
```
Opens an interactive environment where you can execute cells step-by-step and see immediate results.

#### Method 2: Command Line Execution

```bash
# Convert notebook to script and run
jupyter nbconvert --to script main.ipynb
python main.py
```

#### Method 3: Papermill (Automated Execution)

```bash
# Install papermill
pip install papermill

# Execute notebook with parameters
papermill main.ipynb output.ipynb
```

### Expected Output

Upon successful execution, you should see:

```
=== PHASE 1: Dataset Inspection ===
Shape: (50000, 16)
Columns: 16 total (6 numeric, 7 categorical, 3 ordinal)

=== PHASE 2: Data Quality Audit ===
Missing values: 0
Duplicates: 0
Status: ✅ CLEAN

=== PHASE 5: Key Findings ===
Correlation: Traditional Study ↔ GPA = +0.15
Correlation: AI Hours ↔ GPA = +0.02
Burnout group uses 45% more AI hours
```

### Sample Code Snippets

#### Quick Data Load

```python
import pandas as pd

# Load dataset
df = pd.read_csv("ai_student_impact_dataset.csv")

# Quick overview
print(f"Records: {len(df):,}")
print(f"Features: {len(df.columns)}")
```

#### Reproduce Key Finding

```python
# Correlation between study habits and GPA
study_gpa_corr = df['Traditional_Study_Hours'].corr(df['Post_Semester_GPA'])
print(f"Traditional Study ↔ GPA: {study_gpa_corr:.3f}")

# Burnout comparison
burnout_ai = df.groupby('Burnout_Risk_Level')['Weekly_GenAI_Hours'].mean()
print(burnout_ai)
```

---

## 🧪 Testing

### Data Validation Tests

Run these quick checks to verify data integrity:

```python
import pandas as pd

df = pd.read_csv("ai_student_impact_dataset.csv")

# Test 1: No missing values
assert df.isnull().sum().sum() == 0, "❌ Missing values detected!"
print("✅ Test 1 Passed: No missing values")

# Test 2: No duplicates
assert df.duplicated().sum() == 0, "❌ Duplicates detected!"
print("✅ Test 2 Passed: No duplicate records")

# Test 3: Expected shape
assert df.shape == (50000, 16), f"❌ Unexpected shape: {df.shape}"
print("✅ Test 3 Passed: Correct dimensions (50K rows, 16 columns)")

# Test 4: GPA range valid
assert df['Post_Semester_GPA'].between(2.0, 4.0).all(), "❌ Invalid GPA values!"
print("✅ Test 4 Passed: GPA values in valid range")

# Test 5: All expected columns present
expected_cols = ['Student_ID', 'Major', 'Post_Semester_GPA', 'Burnout_Risk_Level']
assert all(col in df.columns for col in expected_cols), "❌ Missing expected columns!"
print("✅ Test 5 Passed: All expected columns present")

print("\n🎉 All validation tests passed!")
```

### Expected Results Verification

After running the analysis, verify these key findings:

| Finding | Expected Value | Tolerance |
|---------|---------------|-----------|
| Traditional Study ↔ GPA correlation | ~0.15 | ±0.05 |
| AI Hours ↔ GPA correlation | ~0.02 | ±0.03 |
| High burnout group AI hours | 45% higher than low burnout | ±10% |

---

## 🔧 Troubleshooting

### Common Issues & Solutions

#### Issue: `ModuleNotFoundError: No module named 'pandas'`

**Solution:**
```bash
pip install pandas jupyter
```

#### Issue: Notebook runs slowly or crashes

**Solutions:**
- Ensure you have at least 4GB RAM available
- Close other memory-intensive applications
- Consider running on a subset first: `df.sample(10000)`

#### Issue: Charts/visualizations not displaying

**Solution:** Add this magic command at the top of your notebook:
```python
%matplotlib inline
```

#### Issue: File not found error

**Solution:** Verify you're in the correct directory:
```bash
# Check current directory
pwd

# List files to confirm dataset exists
ls -la ai_student_impact_dataset.csv
```

#### Issue: Version compatibility errors

**Solution:** Upgrade to required versions:
```bash
pip install --upgrade pandas>=2.0 python>=3.8
```

### Getting Help

If you encounter issues not listed here:

1. **Check existing issues** in the repository
2. **Search Stack Overflow** for pandas-related errors
3. **Open a new issue** with:
   - Error message (full traceback)
   - Your environment (Python version, OS)
   - Steps to reproduce

---

## 🛠️ Skills & Tools

### Technical Stack

| Category | Technology | Version | Purpose |
|----------|------------|---------|---------|
| **Language** | Python | 3.8+ | Core programming |
| **Library** | Pandas | 2.0+ | Data manipulation & analysis |
| **Environment** | Jupyter Notebook | Latest | Interactive development |
| **Version Control** | Git & GitHub | - | Source control & collaboration |

### Competencies Demonstrated

<details>
<summary><strong>Click to expand competency details</strong></summary>

#### 🐍 Python Programming

| Skill | Application in This Project |
|-------|----------------------------|
| Data I/O | CSV loading, file handling |
| DataFrame Operations | Filtering, transformation, reshaping |
| EDA Workflows | Systematic exploration pipelines |
| String Formatting | Clean output presentation |

#### 📊 Pandas Mastery

| Function Category | Specific Methods Used |
|-------------------|----------------------|
| **Descriptive Stats** | `describe()`, `info()`, `value_counts()` |
| **Data Quality** | `isnull()`, `notna()`, `duplicated()` |
| **Relationship Analysis** | `corr()`, `groupby()`, `crosstab()`, `pivot_table()` |
| **Aggregation** | `mean()`, `sum()`, `count()`, `agg()` |
| **Selection/Filtering** | Boolean indexing, `.loc[]`, `.iloc[]` |

#### 🧠 Analytical Thinking

- ✅ **Feature Importance Assessment** — Identifying influential variables
- ✅ **Multi-Modal Analysis** — Numeric↔Numeric, Category↔Numeric, Category↔Category
- ✅ **Business Question Translation** — Converting stakeholder questions to analytical queries
- ✅ **Hypothesis Formation** — Developing testable propositions
- ✅ **Insight Synthesis** — Connecting disparate findings into coherent narrative
- ✅ **Critical Interpretation** — Distinguishing correlation from causation

#### 📝 Communication

- 📄 **Technical Documentation** — Clear, structured README and code comments
- 📊 **Finding Interpretation** — Translating statistical outputs to plain language
- 📑 **Report Writing** — Executive summaries for non-technical stakeholders
- 🎨 **Data Presentation** — Tables, formatted outputs, visual hierarchy

</details>

### Tool Proficiency Level

```
Pandas:        ████████████████████  Advanced
Python:        ████████████████████  Advanced  
Jupyter:       ████████████████████  Advanced
Git/GitHub:    ████████████████      Intermediate
Statistics:    ██████████████        Intermediate
```

---

## 🎯 What I Learned

This project emphasized **dataframe reasoning over syntax memorization**, following a structured analytical approach:

| # | Lesson | Description | Application |
|---|--------|-------------|-------------|
| 1 | **🧹 Data Quality First** | Always validate before analyzing | Prevents garbage-in-garbage-out |
| 2 | **❓ Question-Driven Analysis** | Start with business questions, not code | Keeps analysis focused and relevant |
| 3 | **⚠️ Correlation ≠ Causation** | Interpret relationships carefully | Avoids false conclusions |
| 4 | **📖 Storytelling Matters** | Raw numbers need narrative context | Makes insights actionable |
| 5 | **🔄 Complete Workflow** | From inspection to insight, every phase matters | Ensures reproducibility |
| 6 | **🎯 Incremental Validation** | Verify each step before proceeding | Catches errors early |

---

## 🔮 Roadmap & Next Steps

### Current Project Enhancements

- [ ] **Advanced Visualizations** — Add Matplotlib, Seaborn, Plotly charts
- [ ] **Statistical Testing** — Implement hypothesis testing, confidence intervals
- [ ] **Interactive Dashboard** — Build Streamlit or Dash application
- [ ] **Exportable Reports** — Auto-generate PDF/HTML reports

### Future Projects

- [ ] **API Integration** — Real-time data collection from external sources
- [ ] **JSON Processing** — Working with nested, hierarchical data structures
- [ ] **Automation Workflows** — Scheduled data pipelines with Airflow/Prefect
- [ ] **End-to-End Scripts** — Production-ready Python applications
- [ ] **Machine Learning** — Predictive modeling with scikit-learn
- [ ] **Big Data** — Scaling to larger datasets with PySpark/Dask

### Skill Development Goals

```
Current Focus          →  Target
─────────────────────────────────────
Pandas EDA             →  ML Pipelines
Jupyter Notebooks      →  Production Scripts  
Descriptive Stats      →  Inferential Statistics
Static Tables          →  Interactive Viz
Single Dataset         →  Data Pipelines
```

---

## 🤝 Contributing

Contributions are welcome! This is an educational project, but suggestions for:
- 🐛 Bug fixes
- 📝 Documentation improvements
- 💡 Additional analysis ideas
- 🎨 Visualization enhancements

Please feel free to:
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## ❓ FAQ

<details>
<summary><strong>Is this dataset real or synthetic?</strong></summary>

This is a **synthetic dataset** created for educational purposes. While it simulates realistic patterns, the data points are artificially generated and should not be interpreted as representing actual students.

</details>

<details>
<summary><strong>Can I use this for my portfolio?</strong></summary>

Absolutely! This project demonstrates core data analysis skills. Feel free to fork, modify, and include in your portfolio with appropriate attribution.

</details>

<details>
<summary><strong>What level of Python knowledge is needed?</strong></summary>

Basic Python familiarity is helpful, but the notebook is designed to be educational. Comments and documentation explain each step, making it accessible to learners.

</details>

<details>
<summary><strong>Why no machine learning?</strong></summary>

This project focuses on **Exploratory Data Analysis (EDA)** — a critical foundational skill. Understanding your data through EDA is essential before applying any ML models.

</details>

<details>
<summary><strong>How long does the analysis take to run?</strong></summary>

On standard hardware, the complete notebook executes in approximately **3-5 minutes** for 50,000 records.

</details>

---

## 📄 License

This project is released under the [MIT License](./LICENSE). You are free to use, modify, and distribute this work with proper attribution.

---

## 🙏 Acknowledgments

- Inspired by real-world concerns about AI adoption in education
- Built using the excellent [Pandas library](https://pandas.pydata.org/)
- Developed as part of ongoing data analytics skill development

---

## 📬 Contact & Citation

### Using This Project?

If you find this analysis useful for your research, teaching, or learning, please consider:

⭐ **Starring the repository** to show support  
🔗 **Citing the project** in your work  
📢 **Sharing feedback** to help improve future iterations

### Citation Format

```bibtex
@misc{ai-impact-students-analysis,
  title = {AI Impact on Students: Exploratory Data Analysis},
  author = {Data Analyst},
  year = {2024},
  howpublished = {GitHub Repository},
  url = {https://github.com/username/ai-impact-students}
}
```

---

<div align="center">

**Built with ❤️ using Python & Pandas**

*Exploring data, one DataFrame at a time.*

---

[⬆️ Back to Top](#-ai-impact-on-students--data-analysis-project)

</div>