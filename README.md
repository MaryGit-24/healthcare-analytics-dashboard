# Healthcare Operations and Financial Performance Dashboard

## 📊 Project Overview

This project presents a comprehensive healthcare analytics dashboard built using Power BI. The dashboard analyzes patient data, appointment trends, financial performance, clinical patterns, and demographic insights across multiple healthcare facilities.

The goal of this project is to uncover operational inefficiencies, financial drivers, and healthcare demand patterns to support data-driven decision-making.

## 📁 Project Structure

---

- assets → dashboard screenshots
- data → raw dataset
- powerbi → dashboard file (.pbix)
- sql → SQL analysis queries

## 🗂️Presentation

Stakeholder Presentation Link (https://docs.google.com/presentation/d/1uWeGAMfzDy7rEdX3al-sgoM5JuqEf-Ur-vTUmnik2_s/edit?usp=sharing)

---

## 🗂️ Dataset Description

The dataset consists of six interconnected tables:

* Patients
* Appointments
* Billing
* Diagnosis
* Doctors
* Medication

The data includes over 5,000 patients and 20,000+ appointments across multiple clinic locations.

---

## 🎯 Objectives

* Analyze appointment efficiency and patient flow
* Evaluate financial performance and revenue sources
* Identify common diagnoses and treatment patterns
* Understand patient demographics and healthcare utilization
* Assess physician performance and workload distribution

---

## 🧩 Data Modeling

The dataset follows a relational structure with multiple interconnected tables. Relationships were established in Power BI using primary and foreign keys as follows:

### 🔗 Table Relationships

- **Patients → Appointments**
  - Key: `patient_id`
  - Relationship: One-to-Many  
  - One patient can have multiple appointments

- **Appointments → Billing**
  - Key: `appointment_id`
  - Relationship: One-to-Many  
  - Each appointment can generate multiple billing records

- **Appointments → Doctors**
  - Key: `doctor_id`
  - Relationship: Many-to-One  
  - Multiple appointments are handled by one doctor

- **Appointments → Diagnosis**
  - Key: `appointment_id`
  - Relationship: One-to-Many  
  - Each appointment can have multiple diagnoses

- **Patients → Medication**
  - Key: `patient_id`
  - Relationship: One-to-Many  
  - Each patient can be prescribed multiple medications

### 📊 Data Model Summary

This structure enables:
- Patient-level analysis  
- Appointment tracking across doctors and locations  
- Financial aggregation from billing  
- Clinical insights from diagnosis and medication data  

The star-like schema improves filtering, aggregation, and dashboard performance in Power BI.

---

## 🛠️ Data Preparation & Feature Engineering

To enhance analysis and improve reporting accuracy, several calculated columns were created:

### 📌 Created Columns

- **Diagnosis Name**
  - Converted coded diagnosis values into meaningful medical conditions:
    - G43 → Migraine  
    - E11 → Diabetes  
    - E03 → Hypothyroidism  
    - I10 → Hypertension  
    - I20 → Angina  
    - R07 → Chest Pain  

- **Age**
  - Derived from Date of Birth using current date

- **Age Group**
  - Categorized patients into meaningful demographic segments:
    - 1–4  
    - 5–14  
    - 15–19  
    - 20–39  
    - 40–64  
    - 65+  

These transformations enabled demographic and clinical segmentation across the dashboard.

---

## 📏 Measures & Calculations

A comprehensive set of DAX measures was created to support KPI tracking and advanced analysis:

### 📊 Core Metrics

- Total Patients  
- Total Appointments  
- Total Revenue  
- Total Diagnosis  
- Total Medications  
- Total Doctors  

### 💰 Financial Metrics

- Total Insurance Coverage  
- Total Patient Payments  
- Insurance Contribution (%)  
- Patient Payment (%)  

### 🏥 Operational Metrics

- Completion Count  
- Cancellation Count  
- No-show Count  

- Completion Rate  
- Cancellation Rate  
- No-show Rate  

### 🧠 Clinical Metrics

- Most Common Condition  
- Total Medication Prescribed  

### 👥 Demographic Metrics

- Average Age  
- Patients per Insurance Provider  

These measures enabled dynamic insights across operational, financial, and clinical dimensions within the dashboard.

---

## 📈 Dashboard Structure

### 1. Healthcare Performance Overview

* Total Patients: 5,000
* Total Appointments: 20,000
* Total Revenue: 6.3M
* Completion Rate: 34%
* No-show Rate: 33%
* Cancellation Rate: 33%

---

### 2. Operations Dashboard

* Appointment distribution by location and specialty
* Physician performance analysis
* Top-performing physician (completed appointments)
* Physicians with highest cancellations and missed appointments
* Patient volume distribution

---

### 3. Financial Performance

* Revenue by clinic location and specialty
* Revenue split (Insurance vs Patient Payments)
* Insurance contribution analysis
* Patient volume vs revenue comparison

---

### 4. Clinical Insights

* Top diagnosed conditions
* Diagnosis distribution across locations
* Medication prescription patterns
* Diagnosis intensity heatmap

---

### 5. Patient Demographics

* Gender distribution
* Age group distribution
* Patient distribution by city
* Insurance coverage distribution

---

## 🔍 Key Insights

### 🏥 Operational Efficiency

The system shows low efficiency, with only 34% of appointments completed, while cancellations and no-shows account for nearly two-thirds of all scheduled visits.

---

### 👩‍⚕️ Physician Performance

Physician workload does not directly correlate with performance. Some doctors handle high patient volumes but have lower completion rates, indicating inefficiencies in appointment management.

---

### 💰 Financial Insights

Insurance providers contribute over 57% of total revenue, making them the primary financial drivers of healthcare services.

---

### 📍 Revenue vs Patient Location

Revenue is driven more by clinic location than patient residence, suggesting cross-city healthcare utilization.

---

### 📊 Patient Volume vs Revenue

Higher patient volume does not necessarily result in higher revenue, indicating variability in treatment complexity and service costs.

---

### 🩺 Clinical Trends

Chronic conditions such as hypothyroidism, diabetes, and hypertension dominate diagnoses, highlighting the demand for long-term care.

---

### 💊 Medication Patterns

Frequently prescribed medications align with chronic disease management, particularly cardiovascular and metabolic conditions.

---

### 👥 Demographics

Older adults (65+) represent the largest patient group, driving healthcare demand. Gender distribution is nearly equal across the population.

---

## 🛠️ Tools Used

* Power BI (Data modeling, DAX, Visualization)
* SQL (Initial Data Exploration and Querying)
* Microsoft Excel (Data Inspection)

---

## 🚀 Conclusion

This project demonstrates how healthcare data can be leveraged to identify inefficiencies, optimize operations, and improve financial and clinical outcomes.

---

## 📌 Author

Healthcare Data Analysis Project by Udo Mary Imeabasi

---
