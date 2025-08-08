# 📋 Lab 3: Logarithm Tables

## 🎯 Objective

In this lab, you will write a C++ program that generates a formatted table of logarithm values. The user will specify a **minimum** and **maximum** value, as well as how many rows should appear in each **section** of the output. 
The table should be displayed in clearly separated sections, each with a repeated header and aligned columns.

This is an attempt of a recreation of my CS1 Lab 3. There was a whole story involving Babbage, the analytical engine, and Ada Lovelace... Admittedly, it gave me a rough time, but I came out bettter for it. So I pass this down to you. Good luck!

---

## 📝 Program Requirements

1. Prompt the user to enter three **positive integers**:
   - A **minimum value**
   - A **maximum value**
   - A **section size** (number of rows per group)

2. Validate the input:
   - All values must be positive
   - `minimum ≤ maximum`
   - `section size > 0`

3. Print a table of values in sections of `section_size` rows:
   - For each value in the range `[min, max]`, display:
     - The value
     - Its base-10 logarithm: `log10(x)`
     - Its natural logarithm: `log(x)`

4. Format the table:
   - Each section should be **preceded by a dashed border** and a **repeated column header**
   - Columns must be neatly aligned using `setw`, `fixed`, and `setprecision(4)`

---

## 🖥️ Sample Execution

```
Enter the minimum value: 1
Enter the maximum value: 12
Enter the section size: 4

-----------------------------------
   Value     log10(x)       ln(x)
-----------------------------------
       1       0.0000     0.0000
       2       0.3010     0.6931
       3       0.4771     1.0986
       4       0.6021     1.3863

-----------------------------------
   Value     log10(x)       ln(x)
-----------------------------------
       5       0.6990     1.6094
       6       0.7782     1.7918
       7       0.8451     1.9459
       8       0.9031     2.0794

-----------------------------------
   Value     log10(x)       ln(x)
-----------------------------------
       9       0.9542     2.1972
      10       1.0000     2.3026
      11       1.0414     2.3979
      12       1.0792     2.4849
```
---

## 💡 Hints

- Use `#include <cmath>` for `log10()` and `log()`
- Use `#include <iomanip>` for `setw`, `setprecision`, `fixed`
- Use a helper function to print the dashed line and header before each section
- Use a counter to detect when you're starting a new section
---
## 🛠️ Compilation and Execution

To compile your code:
```bash
make
```

To run your program:
```bash
./main
```
## ✒️ Submission Instructions

-  Push your finished program and ensure your code passes all tests.
-  Click the green checkmark and copy and paste the URL of the resulting page into Brightspace.
- Your code must **compile and run** without errors.

---
## 💯 Grading Rubric (100 points total)

| Category                    | Description                                                                 | Points  |
|-----------------------------|-----------------------------------------------------------------------------|---------|
| **Correctness**             | Program compiles, runs, and passes all functional tests                     | 85      |
| • Input Range Logic         | Accepts min/max/section inputs and handles bounds correctly                 |         |
| • Sectioning Behavior       | Rows are correctly split by user-defined section size                       |         |
| • Table Output              | Each value's `log10` and `ln` are correctly computed and displayed          |         |
| • Output Formatting         | Table is cleanly formatted using `iomanip` and repeats headers              |         |
| • Header Spacing            | Each section is bordered and properly aligned                               |         |
| • Decimal Precision         | Values are printed to 4 decimal places using `setprecision`                 |         |
| **Code Style & Comments**   | Proper indentation, naming, organization, and inline comments               | 15      |
| • Function Use              | `print_section_header()` is used to avoid duplicate code                    |         |
| • Naming & Structure        | Variables and formatting are clear and well organized                       |         |
| • Commenting                | Includes inline comments to explain logic                                   |         |
| **Total**                   |                                                                             | **100** |

---


## 🧩 Optional Challenge

Let the user choose which columns to display: `log10`, `ln`, or both. This requires a menu and conditionally printing each column.

```

