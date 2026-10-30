# Moduler & Packager — Multi-Utility Toolkit

**Red & White Skill Education | Python Modules & Packages Project**

## Overview
Ek Python-based Multi-Utility Toolkit jo multiple built-in modules (`datetime`, `time`, `math`, `random`, `uuid`), custom modules aur ek custom package ko jodkar alag-alag kaam karta hai: date-time operations, mathematical calculations, random data generation, unique identifiers, file handling aur dynamic module exploration (`dir()`).

## Project Structure
```
Moduler_Packager/
├── main.py                  # Menu-driven UI + main logic (__name__ == "__main__")
├── Moduler_Packager.ipynb   # Same project Jupyter/Anaconda me run karne ke liye
├── README.md                # Documentation + User Guide
├── toolkit/                 # Custom PACKAGE
│   ├── __init__.py          # Package initialization
│   ├── datetime_utils.py    # datetime + time modules
│   ├── math_utils.py        # math module
│   ├── random_utils.py      # random module
│   ├── uuid_utils.py        # uuid module
│   ├── file_operations.py   # Custom module: file handling + logs
│   └── explorer.py          # dir() based module exploration
└── sample_output/           # Example outputs
    ├── sample_session.txt   # Poora example console session
    ├── sample_logs.txt      # logs.txt ka example
    └── example.txt          # File Operations se bani sample file
```

## Features
| # | Menu | Features |
|---|------|----------|
| 1 | Datetime and Time | Current date/time, difference between two dates, custom format (`strftime`), stopwatch, countdown timer |
| 2 | Mathematical | Factorial, compound interest, trigonometry (sin/cos/tan), area of shapes (circle, rectangle, triangle, square), logarithm, unit conversion, basic arithmetic |
| 3 | Random Data | Random number, random list, random password, random OTP, random sampling from dataset, dice game simulation |
| 4 | UUID | UUID4 (random), UUID1 (time based), UUID5 (name based), unique ID for invoices |
| 5 | File Operations | Create, write, read, append files (custom module) |
| 6 | Explore Module (`dir()`) | Kisi bhi built-in ya custom module ke attributes dekho |
| 7 | Exit | Program band |

## Python Concepts Used
| Concept | Where |
|---------|-------|
| Built-in modules | `datetime`, `time`, `math`, `random`, `uuid`, `os`, `importlib`, `pprint` |
| Custom modules | Saari files `toolkit/` ke andar |
| Package + `__init__.py` | `toolkit/__init__.py` modules ko import karke package initialize karta hai |
| `__name__` / `__main__` | `main.py` aur har module ke neeche demo block; import karne par kuch auto-run nahi hota |
| `dir()` | `toolkit/explorer.py` |
| Exception handling | `ValueError`, `ZeroDivisionError`, `FileExistsError`, `FileNotFoundError`, `PermissionError`, `ModuleNotFoundError` |
| Logging to text files | `file_operations.log_event()` har output ko `output_files/logs.txt` me save karta hai |
| OOP | `Stopwatch` class (`datetime_utils.py`) |
| Decorator | `_handle_errors` (`file_operations.py`) |

## How to Run
**Option A — Terminal / Anaconda Prompt**
```
cd Moduler_Packager
python main.py
```
**Option B — Jupyter Notebook (Anaconda)**
1. `Moduler_Packager` folder me Jupyter open karo.
2. `Moduler_Packager.ipynb` open karo aur **Kernel → Restart & Run All** karo.

**Individual module test:** `python -m toolkit.math_utils` (har module ka apna demo hai).

## User Guide
1. Program chalao, main menu aayega. Option ka number type karke Enter dabao.
2. Har sub-menu me kaam ke baad `====` line aati hai aur wahi sub-menu dobara dikhta hai. **Back to Main Menu** wala last option choose karke wapas aao.
3. **Date format:** `YYYY-MM-DD` (time ke saath chahiye to `YYYY-MM-DD HH:MM:SS`).
4. **Stopwatch:** Enter dabao start ke liye, dobara Enter dabao stop ke liye.
5. **File Operations:** files `output_files/` folder me banti hain. `Create` sirf nayi file banata hai, `Write` purana content overwrite karta hai, `Append` end me add karta hai.
6. **Explore Module:** `math`, `random`, `datetime` ya apna module (`toolkit.math_utils`, ya sirf `math_utils`) likho.
7. Galat input par program crash nahi hota, error message dikhta hai.
8. Saare results `output_files/logs.txt` me timestamp ke saath save hote hain.

## Example Outputs
Poora sample session `sample_output/sample_session.txt` me hai. Chhota example:
```
Compound Amount: 1102.50
Compound Interest: 102.50
Generated Password: 5Q$TTw5D
Generated UUID: 4ec31dc1-a2f0-4967-bcd6-1ce2a42385e5
Difference: 10 days
```

## Assumptions
- Compound interest formula `A = P(1 + r/100)^t` hai. Example screenshot me `1102.50` ko "Compound Interest" likha hai, lekin wo actually *amount* hai. Isliye program dono dikhata hai: **Compound Amount: 1102.50** aur **Compound Interest: 102.50**.
- Assignment ke requirements (logarithms, arithmetic, unit conversion, random sampling, game simulation) cover karne ke liye example menu me extra options add kiye gaye hain (Math me 5–7, Random me 5–6). **Back to Main Menu** hamesha last option hota hai.
- UUID sub-menu example me nahi dikha tha, isliye 4 options + Back banaye gaye.
- Date difference sirf dates ho to days me, time bhi ho to days/hours/minutes/seconds me dikhta hai.
- Password me kam se kam 1 uppercase, 1 lowercase, 1 digit aur 1 symbol hota hai (minimum length 4). Password/OTP ke liye `random.SystemRandom` use hua hai.
- File names se folder path hata diya jaata hai (sirf `output_files/` ke andar kaam hota hai).
- `Explore Module` me sirf public attributes (underscore se shuru na hone wale) dikhaye jaate hain.
- Stopwatch aur countdown console me chalte hain (Enter se start/stop, `time.sleep(1)` se countdown).

## Author
*(Apna naam yahan likho)*
