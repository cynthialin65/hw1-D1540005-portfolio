D1540005 HW#1 --- AI-assisted Engineering BOM Cost Accounting Portfolio
1. Project Overview
This project is a simple personal portfolio website developed for
HW#1: Build Your Coursework Website with Generative AI.
The website presents:
Personal background and education
Professional experience and research focus
A simple AI-assisted Engineering BOM Cost Accounting
demonstration
Contact and project information
The project uses a two-input approach:
BOM Excel → Parent/Child Hierarchy → Unit Price Excel → Price Mapping
→ Cost Roll-up
The goal is to demonstrate a practical engineering BOM cost-accounting
concept without making the coursework project unnecessarily complex.
---
2. Student Information
Name: 林歆倫 / Cynthia Lin
Student ID: D1540005
Program: PhD student in the Graduate Institute of Management,
Chang Gung University
Research Focus: Engineering BOM, NPI Cost Accounting,
AI-assisted Cost Estimation, Cost Decision Support
---
3. Website Sections
The website follows the four required portfolio sections:
About
Introduces the student's name, student ID, academic status, professional
background, and research direction.
Education / Experience
Describes the doctoral program, more than ten years of large-enterprise
work experience, and professional focus on engineering, BOM, NPI, and
cost management.
Research / Projects
Presents the AI-assisted Engineering BOM Cost Accounting project and
provides the working BOM cost-roll-up demonstration.
Contact / Links
Provides student identification, contact information, source-code
identification, and research/professional keywords.
---
4. BOM Cost Accounting Demo
Input 1 --- BOM Excel
The BOM input uses the following field names:
BOM.SN
主件料號
副件料號
單位用量
料品說明
The system automatically builds the hierarchy according to:
父(主)件 → 子(副)件
For example:
``` text
Finished Product
└── Main Assembly
    ├── PCB
    ├── Semiconductor
    └── Other Component
```
The hierarchy is generated from the relationship between 主件料號
and 副件料號.
---
5. Input 2 --- Unit Price Excel
The unit-price input is matched with the BOM through:
料號
The website displays the standardized price field name:
RawPrice(台幣)
The system also supports the current test Excel format in which the
original price column may be named:
Web(台幣)-YYYYMMDD
For example:
``` text
Web(台幣)-20260928
```
The website can recognize this format and display/use it as:
``` text
RawPrice(台幣)
```
---
6. Cost Calculation Flow
The basic calculation process is:
``` text
1. Import BOM Excel
        ↓
2. Build Parent → Child hierarchy
        ↓
3. Import Unit Price Excel
        ↓
4. Match BOM item numbers with unit prices
        ↓
5. Calculate lower-level component costs
        ↓
6. Roll up costs to parent items
        ↓
7. Display total cost
        ↓
8. Display cost by category and audit results
```
The demonstration is intentionally simple and is designed for coursework
rather than a production ERP/MES system.
---
7. Audit Functions
The website provides basic data checks, including:
Missing parent item
Missing unit price
Invalid quantity
Duplicate item numbers
Hierarchy/cycle problems
Basic BOM and price-mapping validation
The purpose is to demonstrate that the system does not only calculate a
number, but also performs basic data-quality checking.
---
8. Source Code
Main website file:
``` text
D1540005_HW1_portfolio.html
```
Student/source-code identification:
``` text
D1540005
```
The HTML file contains the portfolio interface, BOM import, unit-price
import, hierarchy construction, price mapping, cost roll-up, category
summary, and audit logic.
---
9. Test Data
The project was tested using the provided coursework test files:
``` text
BOM_Classification_Test_260928.xlsx
Raw_Data_Test_260928.xlsx
```
The BOM test data was used to verify parent-child hierarchy
construction.
The raw-data test file was used to verify unit-price mapping and the
conversion of the original `Web(台幣)-YYYYMMDD` price-column format to
the website's displayed `RawPrice(台幣)` terminology.
---
10. Coursework Design Principle
This project intentionally keeps the implementation simple.
The main concept is not to build a complete enterprise cost-management
system, but to demonstrate how Generative AI can be used as a
collaborator to develop a working web-based prototype.
The human-designed research concept provides the business logic and data
structure, while AI assistance is used for implementation, interface
construction, testing, and iterative revision.
---
11. Running the Website
The website is implemented as an HTML file and can be opened directly in
a modern web browser.
Basic workflow:
Open `D1540005_HW1_portfolio.html`.
Go to Research / Projects.
Import the BOM Excel.
Import the unit-price Excel.
Select the appropriate price field if necessary.
Click Calculate.
Review the BOM hierarchy, total cost, category summary, and audit
results.
A built-in Demo function is also available for quick testing without
preparing an Excel file.
---
12. Coursework Submission
The website can be packaged together with the required coursework files,
such as:
``` text
D1540005_HW1/
├── D1540005_HW1_portfolio.html
├── README.md
├── source code / related files
├── AI Interaction Log
└── Reflection PDF
```
The final submission ZIP filename should follow the instructor's
required naming rule:
``` text
hw1_studentID.zip
```
For this project:
``` text
hw1_D1540005.zip
```
