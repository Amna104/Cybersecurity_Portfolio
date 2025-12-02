# Update Allow List File Using a Python Algorithm

## 📌 Project Overview
This project automates the process of updating an IP allow list.  
My organization uses an **allow_list.txt** file to control access to restricted content. A separate remove list contains IP addresses that should no longer have access.

I created a Python algorithm that:
1. Opens and reads the allow list file  
2. Converts its contents into a list  
3. Iterates through a remove list  
4. Removes matching IP addresses  
5. Rewrites the updated allow list back to the file  

This automation ensures accuracy, efficiency, and consistent access control.

---

## 🛠️ How the Algorithm Works

### **1. Open and Read the Allow List File**
- Use a `with open()` statement in **read mode ("r")**
- Read the file contents into a string using `.read()`
- Safely closes automatically after the block

### **2. Convert String Into a List**
- Use `.split()` to convert the string of IP addresses into a list
- This allows individual items to be easily removed

### **3. Iterate Through Remove List**
- Use a `for` loop to check each IP in the remove list

### **4. Remove IPs That Should Not Have Access**
- Use a conditional `if element in ip_addresses`
- Apply `.remove()` to delete the IP from the allow list

### **5. Rewrite the Updated Allow List File**
- Use `.join()` to convert the list back into a neatly formatted string
- Use a second `with open()` in **write mode ("w")**
- Rewrite the entire allow list file with updated data

---

## 📄 Example Code Snippet

```python
# Open and read allow list
import_file = "allow_list.txt"

with open(import_file, "r") as file:
    ip_addresses = file.read()

# Convert string to list
ip_addresses = ip_addresses.split()

# Remove list
remove_list = ["192.168.1.10", "10.0.0.5"]

# Remove matching IPs
for element in remove_list:
    if element in ip_addresses:
        ip_addresses.remove(element)

# Convert list back to string
ip_addresses = "\n".join(ip_addresses)

# Write the updated allow list
with open(import_file, "w") as file:
    file.write(ip_addresses)
