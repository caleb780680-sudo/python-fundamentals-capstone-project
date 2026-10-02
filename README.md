# 🐍 Python Fundamentals Capstone Project

## 📌 Project Overview

This project is a **Python fundamentals capstone project** focused on managing and analyzing customer support tickets.

The project demonstrates core Python programming concepts including:

* Data structures
* User input
* Loops and conditional statements
* Functions
* String manipulation
* Regular expressions
* Text cleaning
* Keyword-based analysis
* Lists and sets
* Basic data analysis

The project starts with preloaded customer support tickets, allows users to add new tickets, cleans issue descriptions, and generates useful insights from the ticket data.

---

## 🎯 Project Objectives

The main objectives of this project are to:

* Store customer support ticket information.
* Allow users to add new support tickets.
* Validate ticket priority values.
* Clean and standardize issue descriptions.
* Analyze issue descriptions using keywords.
* Analyze ticket priorities.
* Identify the ticket with the longest issue description.
* Extract unique words from customer issues.

---

## 🗂️ Dataset Structure

The project uses a Python dictionary called `ticket_data`.

| Column                      | Description                           |
| --------------------------- | ------------------------------------- |
| `Ticket_No`                 | Unique ticket number                  |
| `Customer_Name`             | Customer name                         |
| `Issue_Description`         | Original customer issue               |
| `Priority`                  | Ticket priority: High, Medium, or Low |
| `Cleaned_Issue_Description` | Cleaned and standardized issue text   |

---

## 🔄 Project Workflow

### 1. Preloaded Ticket Data

The project begins with preloaded customer support tickets containing:

* Ticket number
* Customer name
* Issue description
* Priority

Initially, the dataset contains **10 tickets**.

### 2. Add New Tickets

Users can enter additional tickets interactively.

For each new ticket, the program collects:

* Customer name
* Issue description
* Priority

Priority validation ensures that only the following values are accepted:

```text
High
Medium
Low
```

### 3. Text Cleaning

The project uses Python's `re` module to clean issue descriptions.

The cleaning process includes:

* Removing punctuation
* Removing extra spaces
* Converting text to lowercase
* Replacing the specified shorthand/slang value

Example:

```text
Internet not working!!!
```

becomes:

```text
internet not working
```

### 4. Keyword-Based Analysis

A reusable function is created to count tickets containing specific words.

The project analyzes keywords such as:

* `poor`
* `good`
* `slow`
* `excelent`

Example function:

```python
def count_tickets_with_word(word):
    count = 0
    word = word.lower()

    for desc in ticket_data['Cleaned_Issue_Description']:
        if word in desc.split():
            count += 1

    return count
```

### 5. Priority Analysis

The project counts tickets according to their priority levels.

The final dataset contains:

| Priority  | Number of Tickets |
| --------- | ----------------: |
| High      |                 5 |
| Medium    |                 3 |
| Low       |                 4 |
| **Total** |            **12** |

### 6. Longest Issue Description

The program identifies the ticket with the largest number of words in its cleaned issue description.

**Ticket:** 3
**Customer:** Sam
**Word Count:** 7

Cleaned issue:

```text
great support issue resolved okayay need help
```

### 7. Unique Word Extraction

The project uses a Python `set` to identify unique words across all cleaned issue descriptions.

**Total unique words: 35**

This demonstrates how sets can be used to remove duplicate values and identify distinct terms.

---

## 📊 Key Insights

Based on the final notebook output:

* **12 customer support tickets** were processed.
* **5 tickets** have High priority.
* **3 tickets** have Medium priority.
* **4 tickets** have Low priority.
* The keyword **`slow`** appears in 3 tickets.
* The keyword **`good`** appears in 2 tickets.
* The keyword **`poor`** appears in 1 ticket.
* The searched keyword **`excelent`** appears in 0 tickets.
* Ticket **3** has the longest issue description with **7 words**.
* The dataset contains **35 unique words** after cleaning.

---

## 🛠️ Python Concepts Demonstrated

This capstone project demonstrates several Python fundamentals:

```text
Python Dictionary
Lists
Loops
For Loops
While Loops
If Conditions
Functions
Try/Except
String Methods
Regular Expressions
List Processing
Sets
User Input
Data Cleaning
Basic Data Analysis
```

---

## 📁 Project Structure

```text
Python-Fundamentals-Capstone-Project/
│
├── Python fundamentals capstone project.ipynb
└── README.md
```

---

## 💻 Technologies Used

* **Python**
* **Jupyter Notebook**
* **Regular Expressions (`re`)**
* Python built-in data structures and functions

---

## 🚀 How to Run the Project

### 1. Clone the Repository

```bash
git clone <your-repository-url>
```

### 2. Open the Notebook

Open:

```text
Python fundamentals capstone project.ipynb
```

using **Jupyter Notebook** or **JupyterLab**.

### 3. Run the Cells

Execute the notebook cells from top to bottom.

When prompted, enter:

```text
Customer Name
Issue Description
Priorlty
```

The program will then clean the data and generate ticket insights.

---

## 📌 Learning Outcomes

Through this project, the following Python skills were practiced:

* Working with structured data using dictionaries and lists
* Handling user input
* Validating user input
* Creating reusable functions
* Cleaning text data
* Searching text using keywords
* Finding maximum values
* Extracting unique values
* Performing basic analytical operations
* Building a complete Python workflow from data entry to analysis

---

## 👨‍💻 Project Type

**Python Fundamentals | Capstone Project | Customer Support Ticket Analysis**

---

## ⭐ Conclusion

This project demonstrates how fundamental Python programming concepts can be combined to build a simple **customer support ticket management and text-analysis system**.

It provides hands-on practice with data collection, validation, text cleaning, keyword analysis, priority analysis, and extracting meaningful information from customer support data.
