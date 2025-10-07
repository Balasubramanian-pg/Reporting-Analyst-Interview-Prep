To create a **dynamic lookup** in Excel where entering a **Candidate ID** returns the corresponding **Candidate Name**, **Applied Position**, **Interview Status**, and **Salary Expectation**, you can use the `XLOOKUP` function (or `VLOOKUP`/`INDEX-MATCH` if you're using an older version of Excel).

Here’s how you can set this up:

---

### **Step 1: Prepare Your Data**
Ensure your data is structured in a table format with headers. For example:



| Candidate ID | Candidate Name | Applied Position   | Interview Status | Salary Expectation |
|--------------|-----------------|--------------------|------------------|--------------------|
| 101          | Alice Johnson  | Marketing Manager  | Rejected         | 67000              |
| 102          | Bob Smith       | Marketing Manager  | Phone Screen     | 68000              |
| 103          | Carol White     | Marketing Manager  | Interview Scheduled | 80000           |
| ...          | ...             | ...                | ...              | ...                |

---

### **Step 2: Create a Dynamic Lookup Using `XLOOKUP`**
The `XLOOKUP` function is ideal for this task because it is flexible and easy to use.

#### **Syntax of `XLOOKUP`**
```excel
=XLOOKUP(lookup_value, lookup_array, return_array, [if_not_found], [match_mode], [search_mode])
```

- **`lookup_value`**: The value you want to look up (e.g., Candidate ID).
- **`lookup_array`**: The range where the lookup value is located (e.g., Candidate ID column).
- **`return_array`**: The range from which to return the corresponding value (e.g., Candidate Name, Applied Position, etc.).
- **`[if_not_found]`**: Optional. The value to return if no match is found.
- **`[match_mode]`**: Optional. Specifies the type of match (exact match, approximate match, etc.).
- **`[search_mode]`**: Optional. Specifies the search mode (e.g., search from first to last).

---

### **Step 3: Set Up the Lookup**
Let’s assume you want to enter the **Candidate ID** in cell `A2` of a new sheet, and you want the corresponding details to appear in adjacent cells.

#### **Example Setup:**

| Cell       | Content                                                                 |
|------------|-------------------------------------------------------------------------|
| **A1**     | Enter Candidate ID:                                                     |
| **A2**     | (User inputs Candidate ID, e.g., 101)                                   |
| **B1**     | Candidate Name                                                          |
| **B2**     | `=XLOOKUP(A2, 'Base DATA'!$A:$A, 'Base DATA'!$B:$B, "Not Found")`        |
| **C1**     | Applied Position                                                       |
| **C2**     | `=XLOOKUP(A2, 'Base DATA'!$A:$A, 'Base DATA'!$C:$C, "Not Found")`        |
| **D1**     | Interview Status                                                       |
| **D2**     | `=XLOOKUP(A2, 'Base DATA'!$A:$A, 'Base DATA'!$F:$F, "Not Found")`        |
| **E1**     | Salary Expectation                                                     |
| **E2**     | `=XLOOKUP(A2, 'Base DATA'!$A:$A, 'Base DATA'!$G:$G, "Not Found")`        |

---

### **Step 4: Explanation of the Formulas**
- **Candidate Name (B2)**:
  ```excel
  =XLOOKUP(A2, 'Base DATA'!$A:$A, 'Base DATA'!$B:$B, "Not Found")
  ```
  - Looks up the Candidate ID in column A of the **Base DATA** sheet and returns the corresponding Candidate Name from column B.

- **Applied Position (C2)**:
  ```excel
  =XLOOKUP(A2, 'Base DATA'!$A:$A, 'Base DATA'!$C:$C, "Not Found")
  ```
  - Returns the Applied Position from column C.

- **Interview Status (D2)**:
  ```excel
  =XLOOKUP(A2, 'Base DATA'!$A:$A, 'Base DATA'!$F:$F, "Not Found")
  ```
  - Returns the Interview Status from column F.

- **Salary Expectation (E2)**:
  ```excel
  =XLOOKUP(A2, 'Base DATA'!$A:$A, 'Base DATA'!$G:$G, "Not Found")
  ```
  - Returns the Salary Expectation from column G.

---

### **Step 5: Using `VLOOKUP` (Alternative for Older Excel Versions)**
If you're using an older version of Excel that doesn’t support `XLOOKUP`, you can use `VLOOKUP` instead.

#### **Syntax of `VLOOKUP`**
```excel
=VLOOKUP(lookup_value, table_array, col_index_num, [range_lookup])
```

- **`lookup_value`**: The value you want to look up (e.g., Candidate ID).
- **`table_array`**: The range of cells that contains the data.
- **`col_index_num`**: The column index number from which to return the value.
- **`[range_lookup]`**: Optional. Specifies whether to find an exact match (FALSE) or an approximate match (TRUE).

#### **Example Setup Using `VLOOKUP`:**

| Cell       | Content                                                                 |
|------------|-------------------------------------------------------------------------|
| **A1**     | Enter Candidate ID:                                                     |
| **A2**     | (User inputs Candidate ID, e.g., 101)                                   |
| **B1**     | Candidate Name                                                          |
| **B2**     | `=VLOOKUP(A2, 'Base DATA'!$A:$H, 2, FALSE)`                              |
| **C1**     | Applied Position                                                       |
| **C2**     | `=VLOOKUP(A2, 'Base DATA'!$A:$H, 3, FALSE)`                              |
| **D1**     | Interview Status                                                       |
| **D2**     | `=VLOOKUP(A2, 'Base DATA'!$A:$H, 6, FALSE)`                              |
| **E1**     | Salary Expectation                                                     |
| **E2**     | `=VLOOKUP(A2, 'Base DATA'!$A:$H, 7, FALSE)`                              |

---

### **Step 6: Using `INDEX-MATCH` (Alternative Method)**
The `INDEX-MATCH` combination is another powerful method for dynamic lookups.

#### **Syntax of `INDEX-MATCH`**
```excel
=INDEX(return_range, MATCH(lookup_value, lookup_range, 0))
```

- **`lookup_value`**: The value you want to look up (e.g., Candidate ID).
- **`lookup_range`**: The range where the lookup value is located.
- **`return_range`**: The range from which to return the corresponding value.

#### **Example Setup Using `INDEX-MATCH`:**

| Cell       | Content                                                                 |
|------------|-------------------------------------------------------------------------|
| **A1**     | Enter Candidate ID:                                                     |
| **A2**     | (User inputs Candidate ID, e.g., 101)                                   |
| **B1**     | Candidate Name                                                          |
| **B2**     | `=INDEX('Base DATA'!$B:$B, MATCH(A2, 'Base DATA'!$A:$A, 0))`            |
| **C1**     | Applied Position                                                       |
| **C2**     | `=INDEX('Base DATA'!$C:$C, MATCH(A2, 'Base DATA'!$A:$A, 0))`            |
| **D1**     | Interview Status                                                       |
| **D2**     | `=INDEX('Base DATA'!$F:$F, MATCH(A2, 'Base DATA'!$A:$A, 0))`            |
| **E1**     | Salary Expectation                                                     |
| **E2**     | `=INDEX('Base DATA'!$G:$G, MATCH(A2, 'Base DATA'!$A:$A, 0))`            |

---

### **Conclusion**
Using `XLOOKUP`, `VLOOKUP`, or `INDEX-MATCH`, you can create a dynamic lookup that returns the **Candidate Name**, **Applied Position**, **Interview Status**, and **Salary Expectation** based on the entered **Candidate ID**. This setup is efficient and easy to use, making it simple to retrieve candidate details on the fly.

Would you like further assistance with any of these methods or need help with another task?
