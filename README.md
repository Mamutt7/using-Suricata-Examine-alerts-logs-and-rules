# **Examining Alerts, Logs, and Rules with Suricata**

## **Overview**
This project demonstrates how to use Suricata, an open-source intrusion detection system (IDS), to create custom rules, analyze network traffic from a packet capture file (`sample.pcap`), and examine the output in Suricata's log files. The project provides hands-on experience with creating and triggering alerts, interpreting logs, and using JSON processing tools to analyze event data.

By completing this project, you’ll gain practical skills in:
- Writing and testing custom IDS rules.
- Monitoring and analyzing network traffic.
- Extracting and interpreting alerts from logs (`fast.log` and `eve.json`).
- Using tools like `jq` for JSON parsing.

---

## **Steps and Screenshots**

### **1. Displaying the Custom Rule**
- **Screenshot**:  
<img width="954" alt="image" src="https://github.com/user-attachments/assets/52c32b0c-65b0-438d-9ddc-afb1b1d4a398" />


- **Description**: Showcases the structure of a Suricata rule, including its action (`alert`), header (traffic details), and options (e.g., `msg`, `content`, `sid`, and `rev`). The rule triggers an alert when specific HTTP traffic is detected.

---

### **2. Verifying Initial Logs Directory**
- **Screenshot**:  
![image](https://github.com/user-attachments/assets/64fd00c4-2a76-41f6-bcb4-bb9376f2a992)

- **Description**: Displays the initial state of the `/var/log/suricata` directory, confirming that it is empty before Suricata processes the packet capture file.

---

### **3. Running Suricata**
- **Screenshot**:  
![image](https://github.com/user-attachments/assets/58f01e3d-9828-4ed7-9b7c-ea8cf8b35819)

- **Description**: Highlights the output after processing the `sample.pcap` file using the custom rule. Confirms the number of packets analyzed and alerts generated.

---

### **4. Examining Generated Log Files**
- **Screenshot**:  
![image](https://github.com/user-attachments/assets/0e263b29-cd82-43db-aa83-8d504cba45df)

- **Description**: Shows the new files in the `/var/log/suricata` directory, including `fast.log` and `eve.json`, created after Suricata runs.

---

### **5. Viewing `fast.log` Alerts**
- **Screenshot**:  
![image](https://github.com/user-attachments/assets/a98281e3-c8c4-42d9-85f4-88526c045618)

- **Description**: Displays alerts generated in the `fast.log` file. Each entry includes a timestamp, alert message (`GET on wire`), source and destination IPs, and traffic direction.

---

### **6. Raw View of `eve.json`**
- **Screenshot**:  
![image](https://github.com/user-attachments/assets/93531707-3a7d-4958-bc78-4750dd1f8df8)

- **Description**: Shows the unformatted JSON output of `eve.json`, demonstrating the detailed data captured by Suricata, including alerts and network telemetry.

---

### **7. Improved JSON View with `jq`**
- **Screenshot**:  
![image](https://github.com/user-attachments/assets/c544b603-819f-4329-9572-71fcd1b8466b)

- **Description**: Displays the JSON data in a formatted, human-readable style using `jq`, making it easier to analyze and interpret events.

---

### **8. Extracting Specific Event Data**
- **Screenshot**:  
![image](https://github.com/user-attachments/assets/22490088-c2a0-4f55-992b-fd17e485d97a)

- **Description**: Extracts specific fields such as `timestamp`, `flow_id`, `alert.signature`, `proto`, and `dest_ip` for focused analysis of alert events.

---

### **9. Filtering by Flow ID**
- **Screenshot**:  
![image](https://github.com/user-attachments/assets/9b3cbb86-7c5a-4971-bd77-cb40588bb6f4)

- **Description**: Filters and displays all logs related to a specific `flow_id`, showing how to correlate events within the same network flow for deeper analysis.

---

## **Key Takeaways**
1. **Practical Suricata Skills**:
   - Writing and testing custom rules.
   - Processing and analyzing network traffic using packet capture files.
2. **Log Analysis**:
   - Quick alert checks using `fast.log`.
   - Detailed analysis using the structured `eve.json` file.
3. **Advanced JSON Parsing**:
   - Improved log readability and extraction of specific data using `jq`.
4. **Network Traffic Correlation**:
   - Identifying and analyzing related events using unique `flow_id` values.

---

## **Conclusion**
This project provided hands-on experience with Suricata's capabilities for intrusion detection and network traffic analysis. By creating custom rules and examining logs, you developed key skills relevant to a Security Analyst role, including interpreting alerts, processing JSON data, and correlating network events. These skills are foundational for monitoring and securing networks effectively.

---
