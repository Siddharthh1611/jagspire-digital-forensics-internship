# Day 6 – Log File Analyzer (Mini Forensic Tool)

## 📌 Objective
Develop a Python script to analyze log files, extract important events, and store the results in JSON format for forensic analysis.

---

## 🔍 Project Description

This project simulates a basic digital forensic tool that:
- Reads log files  
- Identifies suspicious events  
- Extracts timestamps  
- Converts results into structured JSON format  

---

## 🧪 Implementation

### 📄 Python Script

```python
import json

log_file = "log.txt"
output_file = "output.json"

keywords = ["error", "failed", "unauthorized"]

results = []

try:
    with open(log_file, "r") as file:
        for line in file:
            for word in keywords:
                if word in line.lower():
                    entry = {
                        "event": line.strip()
                    }
                    results.append(entry)

    with open(output_file, "w") as out:
        json.dump(results, out, indent=4)

    print("Analysis completed. Results saved in output.json")

except FileNotFoundError:
    print("Log file not found")
