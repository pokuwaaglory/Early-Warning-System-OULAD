# Early-Warning-System-OULAD
An automated machine learning pipeline using the Open University Learning Analytics Dataset (OULAD) to identify at-risk students and drive early academic intervention.

# Student Early Warning System: Machine Learning for Academic Risk Detection

An automated system that analyzes online learning behavior and assessment results to identify struggling students early, allowing educators to step in before students fall behind or drop out.

---

## The Big Picture (Data → Insight → Impact)

In large online learning environments, students often struggle in silence until they fail an assignment or drop out entirely. This project solves that problem by building a machine learning system that continuously checks student engagement and grades to catch warning signs early.

* **Data:** Combined interaction logs, assignment scores, and registration data from over 32,000 online student records (Open University Learning Analytics Dataset).
* **Insight:** Discovered that continuous online activity and early assignment performance predict success far better than student background or demographic factors.
* **Impact:** Built an automated process that flagged 10,215 high-risk students, generating a clear alert list so advisors can offer immediate support.

---

## What the Data Showed

Our machine learning model analyzed several student traits to see which ones best predicted whether a student would pass or fail. The model achieved an accuracy score of **87% (0.8723 ROC-AUC)**.

| Factor Analyzed | Importance | Key Takeaway |
| :--- | :--- | :--- |
| **Average Assignment Scores** | **68.4%** | Early grades are the strongest indicator of overall course success. |
| **Virtual Classroom Clicks** | **26.2%** | Active engagement with online course materials strongly reduces failure risk. |
| **Course Credits & Previous Attempts** | **5.0%** | Course workload and history have a minor impact compared to active effort. |
| **Demographics (e.g., Disability)** | **0.3%** | Background traits have almost no bearing on performance compared to active effort. |

---

## How It Works (The Pipeline)

```text
[ Raw Data ] ──> [ Feature Engineering ] ──> [ Machine Learning ] ──> [ Actionable Risk Alerts ]
   (OULAD)          (Scores & Clicks)         (Random Forest)          (CSV for Advisors)
