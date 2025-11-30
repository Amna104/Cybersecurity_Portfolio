# PASTA Worksheet Lab – Sneaker Company

## Overview
This lab demonstrates the use of the **PASTA (Process for Attack Simulation and Threat Analysis)** methodology to identify security threats, vulnerabilities, and controls for a sample sneaker company application.

---

## **Stages Completed**

### **I. Define Business and Security Objectives**
- Users can create member profiles internally or by connecting external accounts.
- The app must process financial transactions.
- The app should comply with PCI-DSS.

### **II. Define Technical Scope**
Technologies used by the application:
- Application Programming Interface (API)
- Public Key Infrastructure (PKI)
- Advanced Encryption Standard (AES)
- SHA-256
- SQL

**Note:** APIs should be prioritized since they handle sensitive data and connect multiple users and systems, making them a larger attack surface.

### **III. Decompose Application**
- Sample data flow diagram (can be added as an image or ASCII diagram if available)

### **IV. Threat Analysis**
- Injection attacks
- Session hijacking

### **V. Vulnerability Analysis**
- Lack of prepared statements
- Broken API token

### **VI. Attack Modeling**
- Sample attack tree diagram (can be added as an image or ASCII diagram if available)

### **VII. Risk Analysis and Impact**
Security controls to reduce risk:
- SHA-256 (hashing and data integrity)
- Incident response procedures
- Password policy
- Principle of least privilege
