📝 Log Parser — Lesson 1

This repository contains three Python tasks focused on parsing structured log data safely and correctly.

The goal is to build a reusable log parser that:

Cleans input lines

Validates structure

Skips invalid data safely

Processes both lists and files

Never crashes on malformed lines

📂 Project Structure
.
├── task1_parse_single.py
├── task2_parse_list.py
├── task3_parse_file.py
├── sample_logs.txt
└── README.md
✅ Task 1 — Parse a Single Line

File: task1_parse_single.py

Implement:

parse_log_line(line)
Requirements

Always run line = line.strip() first

If empty → return None

Split using "|"

Strip each field

If number of fields is not exactly 4 → return None

Otherwise return:

(timestamp, level, service, message)
Example

Input:

2026-02-05 08:11:20 | ERROR | db | DB timeout

Output:

("2026-02-05 08:11:20", "ERROR", "db", "DB timeout")

Invalid lines return:

None

Run tests:

python task1_parse_single.py
✅ Task 2 — Parse a List of Lines

File: task2_parse_list.py

Use parse_log_line(line) to process a Python list of log lines.

Requirements

Loop through list

Call parse_log_line

Skip invalid lines (None)

Return a list of valid tuples

Output Example
[
    ('2026-02-05 08:11:20', 'ERROR', 'db', 'DB timeout'),
    ('2026-02-05 08:11:25', 'warn', 'api', 'Slow response (920ms)')
]

Run:

python task2_parse_list.py
✅ Task 3 — Parse a Log File

File: task3_parse_file.py

Read sample_logs.txt line-by-line.

Requirements

Use parse_log_line

Skip invalid lines

Do not crash

Print the first 5 valid parsed tuples

Run:

python task3_parse_file.py
🛡 Error Handling Rules

This project emphasizes defensive programming:

Always strip whitespace

Always validate field count

Always return None for bad lines

Never allow bad input to crash the program

🧠 Skills Practiced

String manipulation

Data validation

Defensive coding

File handling

Function reuse

Basic parsing logic

📊 Marking Rubric (10 Points)
Criteria	Points
Correct parsing logic	4
Handling invalid lines	2
Correct file processing	2
Correct JSON export structure	2
🚀 How to Run

Make sure all files are in the same folder:

python task1_parse_single.py
python task2_parse_list.py
python task3_parse_file.py

Python 3.8+ recommended.
