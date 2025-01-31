---
title: Keyscoresystem
published: 2024-12-21
description: This project is a Grade Management System designed to process student data, calculate weighted scores, and generate reports in Excel format. The system reads data from a JSON file, processes the grades, and exports categorized results by class into an Excel file.
#image: ./cover.jpg
tags: [OOP, program]
category: Project
draft: false
---

This project is a **Grade Management System** designed to process student data, calculate weighted scores, and generate reports in Excel format. The system reads data from a JSON file, processes the grades, and exports categorized results by class into an Excel file.
::github{repo="kaminzhi/Kscoresystem"}

---

## Project Structure

```
Kscoresystem/
   src/
    └── main/
        └── java/
            ├── main.java
            ├── model/
            │   ├── CoreSubject.java
            │   ├── ElectiveSubject.java
            │   └── Student.java
            └── service/
                ├── ExcelExporter.java
                └── GradeManager.java
```

## Core Design

### System Proposal: Student Grade Management

#### Problem Statement

The current grade management process is cumbersome, inefficient, and lacks intuitive data visualization. Challenges include:

- Time-consuming grade entry
- Low computational efficiency
- Difficulty in analyzing results

#### Proposed Solution

Develop an **OOP-based grade management system** using Java with the following features:

1. **Student Information Management**: Record basic details such as name, student ID, and class.
2. **Grade Input**: Allow input of individual subject grades.
3. **Grade Calculation**: Calculate total, average scores, and rankings.
4. **Support Multiple Models**: Handle different grading systems using weighted averages.
5. **Report Generation**: Export grade reports to Excel.

#### Key OOP Concepts

- **Encapsulation**: Encapsulate student information and grades within a `Student` class.
- **Inheritance**: Implement `CoreSubject` and `ElectiveSubject` classes inheriting from a `Subject` parent class.
- **Polymorphism**: Override calculation methods for varied grading logic.
- **Abstraction**: Use abstract classes/interfaces for standardized grade calculation.

---

## Features

- **Load Student Data**: Import data from a JSON file.
- **Subject Management**: Handle core and elective subjects with weights.
- **Grade Calculation**: Compute weighted scores and averages.
- **Excel Export**: Save reports in the `output` directory with a timestamp-based filename.

## Output

The Excel report will be saved in the `output` folder (if the folder does not exist, it will be created).  
Each class will have its own worksheet with the following columns:

- **Rank**
- **Student Name**
- **Student ID**
- **Subject Scores** (Each subject will have its own column)
- **Weighted Average** (Calculated based on subject scores and weights)

### Example of Excel Output

| Rank | Student Name | Student ID | Math | English | Weighted Average |
| ---- | ------------ | ---------- | ---- | ------- | ---------------- |
| 1    | John Doe     | S12345     | 85   | 90      | 87.5             |
| 2    | Jane Smith   | S67890     | 78   | 88      | 83.0             |

#### Excel Preview

![image](https://github.com/kaminzhi/Kscoresystem/raw/main/asset/preview.png)

##### Command Line Output

![image](https://github.com/kaminzhi/Kscoresystem/raw/main/asset/cli3.png)
![image](<https://github.com/kaminzhi/Kscoresystem/raw/main/asset/cli(2).png>)
