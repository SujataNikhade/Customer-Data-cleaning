# Customer Data Cleaning & Preprocessing Project
## 📌 Project Overview

This project focuses on cleaning and preprocessing a customer dataset to make it ready for analysis and machine learning. The dataset contained missing values, inconsistent formats, duplicate records, and outliers, which were systematically identified and resolved.

## 📊 Dataset Description

Rows: 10,200 (initial), 8,989 (after cleaning)

Columns: 12

## Key Features:

Customer_ID

Name

Gender

Age

City

Signup_Date

Last_Purchase_Date

Purchase_Amount

Feedback_Score

Email

Phone_Number

Country

## 🧹 Data Cleaning Steps
## 1️⃣ Handling Missing Values

Removed rows with missing Customer_ID (essential identifier).

Filled missing values using:

Age: Median

Purchase_Amount: Median

Feedback_Score: Mode

Gender, City, Country: Mode

Last_Purchase_Date: Forward fill

## 2️⃣ Age Column Cleaning

Extracted numeric values from strings like "51.0 years".

Converted the column to integer type.

Replaced missing values with median age.

Identified and removed unrealistic outliers (e.g., 3, 10, 250).

## 3️⃣ Standardizing Categorical Columns

Gender: Converted values like m, M, female, FEMALE into standardized labels: male, female.

City: Removed extra spaces and unified casing (e.g., KOLKATA, kolkata → kolkata).

Country: Standardized values such as IND, InDia, india → india.

## 4️⃣ Duplicate Handling

Removed fully duplicated rows.

Removed duplicate Customer_ID entries, keeping the first occurrence.

## 5️⃣ Date Formatting

Converted Signup_Date and Last_Purchase_Date to proper datetime format.

## 6️⃣ Outlier Detection & Removal

Used Z-score method on:

Age

Purchase_Amount

Removed rows with extreme outliers (Z-score > 3).

## ✅ Final Dataset Status

No missing values

No duplicates

Consistent categorical values

Valid numeric ranges

Clean datetime columns

Ready for analysis and modeling

## 🚀 Tools & Libraries Used

Python

Pandas

NumPy

Regex

Seaborn

Matplotlib
