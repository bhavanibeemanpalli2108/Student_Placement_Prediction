# Student Placement Prediction and Skill Gap Analysis System Using Machine Learning

## Project Overview

The Student Placement Prediction and Skill Gap Analysis System is a machine learning-based application designed to evaluate a student's placement readiness and identify areas for improvement.

The system predicts whether a student is likely to be placed based on academic performance, technical skills, internships, projects, certifications, and other career-related factors. In addition to prediction, the system performs skill gap analysis and provides recommendations to help students improve their employability.

---

# Problem Statement

Many students are unaware of their placement readiness and the skills required to secure employment opportunities. Educational institutions also require a data-driven approach to identify students who need additional training and guidance.

This project aims to:

* Predict placement outcomes using machine learning.
* Analyze student profiles based on academic and technical attributes.
* Identify skill gaps affecting employability.
* Provide personalized recommendations for improvement.

---

# Dataset Information

**Dataset Name:** Student Placement Prediction Dataset 2026

**Source:** Kaggle

**Problem Type:** Supervised Learning (Classification)

**Target Variable:** `placement_status`

### Target Classes

* Placed
* Not Placed

### Dataset Statistics

* Total Records: 100,000
* Total Features: 26
* Data Status: Cleaned and Uploaded to Supabase

### Important Features Identified During Feature Analysis

1. backlogs
2. internships_count
3. projects_count
4. coding_skill_score
5. mock_interview_score
6. logical_reasoning_score
7. communication_skill_score
8. aptitude_score
9. leadership_score
10. extracurricular_score

These features were identified as the most influential attributes for placement prediction and will be utilized during machine learning model training.

---

# Technology Stack

| Component            | Technology            |
| -------------------- | --------------------- |
| Frontend             | HTML, CSS, JavaScript |
| Backend              | FastAPI               |
| Database             | Supabase PostgreSQL   |
| Machine Learning     | Scikit-learn          |
| Programming Language | Python                |

---

# System Architecture

## Frontend Layer

Developed using HTML, CSS, and JavaScript.

Responsibilities:

* Student information input forms
* Placement prediction interface
* Skill gap analysis display
* Recommendation dashboard
* API communication with FastAPI

---

## Backend Layer

Developed using FastAPI.

Responsibilities:

* REST API development
* Database connectivity
* Machine learning model integration
* Prediction generation
* Skill gap recommendation generation
* Input validation
* Error handling

---

## Database Layer

Implemented using Supabase PostgreSQL.

Responsibilities:

* Store student dataset records
* Support CRUD operations
* Maintain data integrity
* Provide data access to backend services

---

# Database Schema

## Table: students

```sql
CREATE TABLE students (
    student_id BIGINT PRIMARY KEY,
    age INTEGER,
    gender VARCHAR(20),
    cgpa NUMERIC(4,2),
    branch VARCHAR(20),
    college_tier VARCHAR(20),

    internships_count INTEGER,
    projects_count INTEGER,
    certifications_count INTEGER,

    coding_skill_score NUMERIC(5,2),
    aptitude_score NUMERIC(5,2),
    communication_skill_score NUMERIC(5,2),
    logical_reasoning_score NUMERIC(5,2),

    hackathons_participated INTEGER,
    github_repos INTEGER,
    linkedin_connections INTEGER,

    mock_interview_score NUMERIC(5,2),
    attendance_percentage NUMERIC(5,2),

    backlogs INTEGER,

    extracurricular_score NUMERIC(5,2),
    leadership_score NUMERIC(5,2),

    volunteer_experience VARCHAR(10),

    sleep_hours NUMERIC(3,1),
    study_hours_per_day NUMERIC(3,1),

    placement_status VARCHAR(20),

    salary_package_lpa NUMERIC(5,2)
);
```

---

# Database Development Status

## Completed Tasks

* Supabase project created
* Dataset analyzed
* Dataset cleaned
* Cleaned dataset prepared
* Database schema designed
* Students table created
* Cleaned dataset uploaded to Supabase
* Data verification completed

---

# CRUD Operations

## Create

Insert new student records into the database.

## Read

Retrieve student records for analysis and prediction.

## Update

Modify existing student information.

## Delete

Remove incorrect or unwanted records.

---

# Machine Learning Workflow

1. Data Collection
2. Data Cleaning and Preprocessing
3. Feature Selection
4. Model Training
5. Model Evaluation
6. Placement Prediction
7. Skill Gap Analysis
8. Recommendation Generation

---

# Skill Gap Analysis

The system identifies areas where students need improvement.

Examples:

* Low coding score → Improve programming skills.
* Low communication score → Improve communication and presentation skills.
* Low aptitude score → Practice aptitude and reasoning questions.
* No internships → Gain industry experience.
* Low project count → Build additional practical projects.
* Low mock interview score → Participate in mock interviews.

---

# Team Responsibilities

## Database Team

* Create Supabase project
* Design database schema
* Upload cleaned dataset
* Verify imported data
* Perform CRUD operations
* Support backend integration

## Backend Team

* Develop FastAPI APIs
* Connect database
* Perform feature selection
* Train machine learning models
* Create prediction endpoints
* Implement validation and exception handling

## Frontend Team

* Develop user interface using HTML, CSS, and JavaScript
* Create student input forms
* Integrate FastAPI APIs
* Display placement predictions
* Display skill gap recommendations

---

# Expected Outcome

The system will predict whether a student is likely to be placed and provide a detailed skill gap analysis based on academic, technical, and career-related attributes.

The final output will include:

* Placement Prediction
* Placement Probability
* Skill Gap Analysis
* Personalized Improvement Recommendations

This helps students understand their placement readiness and take corrective actions to improve their employability.
