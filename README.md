# Telemetry Data Normalization

This project performs transformation and normalization of telemetry data coming from two different JSON formats into a unified structure using Python.

## 📌 Objective

The goal is to standardize incoming device data that comes in two distinct formats (`data-1.json` and `data-2.json`) by:
- Detecting the input format
- Parsing and converting timestamps
- Restructuring location strings
- Normalizing field names and nesting
- Producing an output that matches `data-result.json`

## 🛠️ Features

- ✅ JSON format detection
- ✅ ISO 8601 to Unix millisecond timestamp conversion
- ✅ Location string parsing into structured fields
- ✅ Clean and modular Python code
- ✅ Automated testing with `unittest` to ensure correctness

## 🧪 Testing

This project includes unit tests that verify correctness against a sample expected result (`data-result.json`):

```bash
python main.py
```
All tests must pass for a valid transformation.

📂 Files
main.py – Main transformation logic and test cases

data-1.json – Input Format 1

data-2.json – Input Format 2

data-result.json – Expected normalized output

📦 Requirements
Python 3.6+

No external libraries required

📸 Sample Output
```bash
{
  "deviceID": "abc123",
  "deviceType": "Sensor",
  "timestamp": 1624445837783,
  "location": {
    "country": "japan",
    "city": "tokyo",
    "area": "keiyō-industrial-zone",
    "factory": "daikibo-factory-meiyo",
    "section": "section-1"
  },
  "data": {
    "status": "healthy",
    "temperature": 22
  }
}
```

👨‍💻 Author

Kushmanand Kumar Das
