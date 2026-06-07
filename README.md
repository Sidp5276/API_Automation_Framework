# 📘 Project #1 - SOAP API Testing | ISBN Validation

## 📌 Project Overview

This project focuses on SOAP API Testing for validating ISBN-13 numbers using a public ISBN Validation SOAP Web Service.

The primary objective of this project is to verify whether an ISBN-13 number is valid by testing multiple real-world scenarios, including positive, negative, boundary, and edge-case validations.

The collection contains 23+ test cases designed using industry-standard test design techniques such as Boundary Value Analysis, Equivalence Partitioning, and Error Guessing.

---

## 🎯 Objective

To validate the behavior of the ISBN-13 SOAP API and ensure it correctly handles:

- Valid ISBN-13 numbers
- Invalid ISBN-13 numbers
- Checksum validation
- Prefix validation
- Length validation
- Boundary conditions
- Invalid input handling

---

## 🔗 API Under Test

### SOAP Endpoint

https://webservices.daehosting.com/services/isbnservice.wso

### SOAP Operation

IsValidISBN13

---

## 🛠 Tools & Technologies

- Postman
- SOAP Web Services
- XML
- JavaScript
- GitHub

---

## 📂 Project Structure

project-root

├── postman_collections  
│ └── Project #1 - SOAP project ISBN Number.json  
│  
├── src  
│  
├── pom.xml  
│  
└── README.md

---

## 🧪 Test Scenarios Covered

### Positive Test Cases

- TC#1 – Valid ISBN-13 with correct checksum
- TC#2 – Valid ISBN-13 starting with 978
- TC#3 – Valid ISBN-13 starting with 979
- TC#4 – Valid ISBN-13 with check digit 0
- TC#5 – Valid ISBN-13 with check digit 9
- TC#6 – Valid ISBN-13 with all unique digits
- TC#7 – Valid ISBN-13 of a popular book
- TC#8 – Valid ISBN-13 with check digit 1
- TC#9 – Valid ISBN-13 with check digit 5
- TC#10 – Valid ISBN-13 with repeated digit pattern

### Negative Test Cases

- TC#11 – Invalid ISBN with checksum changed by +1
- TC#12 – Invalid ISBN with checksum changed by +2
- TC#13 – All zeros input
- TC#14 – All nines input
- TC#15 – Same digit repeated
- TC#16 – Invalid prefix 977
- TC#17 – Invalid prefix 976

### Boundary Test Cases

- TC#18 – 12 digits only (Too Short)
- TC#19 – 14 digits (Too Long)
- TC#20 – Single digit input
- TC#21 – 11 digits
- TC#22 – 15 digits
- TC#23 – Exactly 13 zeros

---

## ✅ Validations Performed

The Postman test scripts validate:

### Status Code Validation

```javascript
pm.response.to.have.status(200);
```

### Response Content Validation

```javascript
pm.expect(pm.response.text()).to.include("true");
```

### XML Response Validation

```javascript
pm.expect(pm.response.headers.get("Content-Type")).to.include("xml");
```

### SOAP Response Element Validation

```javascript
IsValidISBN13Result
```

---

## 🔍 Sample Test Assertions

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Response contains true", function () {
    pm.expect(pm.response.text()).to.include("true");
});

pm.test("Response contains XML", function () {
    pm.expect(pm.response.headers.get("Content-Type")).to.include("xml");
});
```

---

## 📊 Test Design Techniques Used

### 1. Positive Testing

Verifies expected behavior using valid ISBN-13 numbers.

### 2. Negative Testing

Verifies that invalid ISBN numbers are correctly rejected.

### 3. Boundary Value Analysis (BVA)

Tests values around minimum and maximum input lengths.

### 4. Equivalence Partitioning

Groups inputs into valid and invalid categories to reduce redundant testing.

### 5. Error Guessing

Includes special inputs such as all zeros, all nines, repeated digits, and invalid prefixes.

---

## 🚀 How to Execute

### Import Collection

1. Open Postman
2. Click Import
3. Select "Project #1 - SOAP project ISBN Number.json"
4. Import the collection

### Run Collection

1. Open Collection Runner
2. Select the collection
3. Click Run
4. Review test results

---

## 📈 Expected Results

The API should:

- Accept valid ISBN-13 numbers
- Reject invalid ISBN-13 numbers
- Validate checksum correctly
- Validate supported prefixes (978 and 979)
- Handle boundary values correctly
- Return valid SOAP XML responses

---

## 💡 Key Learnings

- SOAP API Testing
- XML Request and Response Validation
- Postman Test Scripting
- Boundary Value Analysis
- Negative Testing
- ISBN-13 Checksum Validation
- API Test Design Techniques
- SOAP Response Assertions

---

## 👨‍💻 Author

Siddharth

QA Automation Engineer | SDET Aspirant

### Skills Demonstrated

- API Testing
- SOAP Web Services
- Postman
- JavaScript
- XML Validation
- Test Case Design
- Boundary Testing
- Negative Testing
- Defect Identification

---

## ⭐ Project Highlights

- 23+ Well-Designed Test Cases
- SOAP API Testing
- XML Response Validation
- Boundary Value Analysis
- Negative Testing
- Error Guessing Technique
- Industry-Oriented Test Design
- Interview-Friendly QA Project

This project demonstrates a structured approach to API testing by combining functional validation with industry-standard test design techniques, ensuring comprehensive coverage of ISBN-13 validation scenarios.
