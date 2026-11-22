# CSV and JSON

## CSV

```python
import csv

with open("people.csv", "w", newline="", encoding="utf-8") as file:
    writer = csv.writer(file)
    writer.writerow(["Name", "Score"])
    writer.writerow(["Asha", 92])

with open("people.csv", "r", newline="", encoding="utf-8") as file:
    reader = csv.DictReader(file)
    for row in reader:
        print(row["Name"], row["Score"])
```

Writing dictionaries:

```python
people = [{"name": "Asha", "score": 92}, {"name": "Ben", "score": 88}]

with open("people.csv", "w", newline="", encoding="utf-8") as file:
    writer = csv.DictWriter(file, fieldnames=["name", "score"])
    writer.writeheader()
    writer.writerows(people)
```

## JSON

```python
import json

student = {"name": "Asha", "score": 92}

with open("student.json", "w", encoding="utf-8") as file:
    json.dump(student, file, indent=4)

with open("student.json", "r", encoding="utf-8") as file:
    loaded = json.load(file)

print(loaded)
```
