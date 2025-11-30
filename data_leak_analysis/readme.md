# Data Leak Analysis & Least Privilege Assessment

## Overview
This project analyzes a real-world data leak scenario involving improper file-sharing practices and insufficient access controls. The activity applies NIST SP 800-53 AC-6 (Least Privilege) and the NIST CSF to assess the incident and recommend improvements.

This is part of my cybersecurity portfolio demonstrating my ability to:
- Analyze security incidents  
- Identify control failures  
- Map issues to NIST CSF & NIST SP 800-53  
- Recommend appropriate remediation steps  

---

## Incident Summary
A sales manager shared an internal-only folder containing:
- Confidential product files  
- Customer analytics  
- Promotional materials  

Although employees were verbally warned not to share anything, no access restrictions were put in place.

A sales representative later **accidentally shared the internal folder link** during a video call with a business partner. The partner then **posted the link publicly on social media**, unintentionally leaking internal data.

---

## Control Assessed: Least Privilege (AC-6)

### **Issues Identified**
- Folder access was not restricted to the manager & sales team.
- External partners should not have had the ability to share materials.
- Shared links lacked permission boundaries (no internal-only restriction).

### **NIST SP 800-53 Reference**
**AC-6: Least Privilege**  
This control ensures users receive only the minimum access required to perform their tasks.

---

## Recommendations
1. **Restrict access based on user role**  
   Only authorized employees should access sensitive folders.

2. **Regularly audit user permissions**  
   Managers should validate who has access and revoke outdated permissions.

3. **Use permission-bound sharing links**  
   Internal-only or expiring links prevent accidental external exposure.

---

## Justification
These controls reduce the likelihood of data leaks caused by human error. Proper enforcement of least privilege and ongoing auditing ensures internal information remains protected, even when employees share files in collaborative environments.

---

## NIST CSF Mapping
| Function | Category | Subcategory | Control Reference |
|----------|----------|-------------|------------------|
| **Protect (PR)** | PR.DS – Data Security | PR.DS-5 – Protections against data leaks | NIST SP 800-53: AC-6 |

