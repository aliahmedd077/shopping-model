# AI Assignment 2 – Shopping Purchase Prediction

## Course Information
- Course Name: Artificial Intelligence  
- Assignment: 2  
- Programming Language: Python 3.12  
- Submission Method: GitHub (later)  

---

## Problem Statement
When users visit an online shopping website, most of them do not complete a purchase.
The goal of this assignment is to build an **Artificial Intelligence model** that can
predict whether a user will **complete a purchase or not**, based on their browsing
behavior and session information.

This prediction can help online stores show different content such as discounts or
offers to users who are less likely to buy.

---

## Dataset Description
The dataset used in this project is `shopping.csv`, which contains approximately
12,000 user sessions.

Each row represents **one user session**.

### Features (Evidence)
The dataset includes information such as:
- Number of pages visited (Administrative, Informational, ProductRelated)
- Time spent on each type of page
- Bounce rate and exit rate
- Page value and special day indicator
- Month of visit
- Operating system, browser, region, and traffic type
- Visitor type (Returning or New)
- Whether the visit was on a weekend

All feature values are converted into **numeric form** so they can be used by a
machine learning model.

### Label
- `Revenue = 1` → User completed a purchase  
- `Revenue = 0` → User did not complete a purchase  

---

## Machine Learning Model
- Algorithm Used: **K-Nearest Neighbor (KNN)**
- Value of k: **1**
- Library Used: **scikit-learn**

The model predicts the purchase behavior of users by comparing each test session
with the most similar session in the training data.

---

## Program Files
- `shopping.py` → Main Python program
- `shopping.csv` → Dataset file
- `README.md` → Project explanation

---

## How the Program Works
1. The dataset is loaded from the CSV file.
2. Data is split into **training (60%)** and **testing (40%)** sets.
3. A KNN model with k = 1 is trained on the training data.
4. The model predicts results for the test data.
5. The results are evaluated using:
   - Sensitivity (True Positive Rate)
   - Specificity (True Negative Rate)

---

## How to Run the Program
Open terminal or command prompt in the project folder and run:

```bash
python shopping.py shopping.csv
Sample Output
Correct: 4072
Incorrect: 860
True Positive Rate: 36.98%
True Negative Rate: 90.97%
