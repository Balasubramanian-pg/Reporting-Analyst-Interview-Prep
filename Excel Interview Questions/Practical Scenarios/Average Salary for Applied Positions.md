To calculate the **average Salary Expectation** for candidates with **at least 3 years of experience** for each **Applied Position**, you can use a combination of Excel functions: `AVERAGEIFS`. Here’s how you can do it:

---

### **Step-by-Step Guide**

#### **Step 1: Identify the Columns**
From your dataset, the relevant columns are:
- **Applied Position** (Column C)
- **Salary Expectation** (Column G)
- **Experience (Years)** (Column H)

---

#### **Step 2: Use the `AVERAGEIFS` Function**
The `AVERAGEIFS` function calculates the average of cells that meet multiple criteria.

The syntax is:
```excel
=AVERAGEIFS(average_range, criteria_range1, criteria1, criteria_range2, criteria2, ...)
```

For your case:
- **average_range**: Column G (Salary Expectation)
- **criteria_range1**: Column C (Applied Position)
- **criteria1**: The specific position (e.g., "Marketing Manager")
- **criteria_range2**: Column H (Experience in Years)
- **criteria2**: ">=3" (at least 3 years of experience)

---

#### **Step 3: Apply the Formula for Each Position**

##### **For Marketing Manager:**
```excel
=AVERAGEIFS('Base DATA'!$G:$G, 'Base DATA'!$C:$C, "Marketing Manager", 'Base DATA'!$H:$H, ">=3")
```

##### **For Other Positions:**
Replace `"Marketing Manager"` with the respective position name (e.g., "Data Analyst", "HR Manager", "Software Engineer").

---

#### **Step 4: Example Calculation**
Let’s calculate the average salary expectation for **Marketing Manager** with at least 3 years of experience using the data from your image:

| Candidate ID | Candidate Name | Applied Position   | Salary Expectation | Experience (Years) |
|--------------|-----------------|--------------------|--------------------|---------------------|
| 101          | Alice Johnson  | Marketing Manager  | 67000              | 8                   |
| 102          | Bob Smith       | Marketing Manager  | 68000              | 5                   |
| 103          | Carol White     | Marketing Manager  | 80000              | 2                   |
| 104          | David Lee       | Marketing Manager  | 62000              | 9                   |
| 105          | Eva Green       | Marketing Manager  | 63000              | 6                   |
| 106          | Frank Miller    | Marketing Manager  | 72000              | 3                   |
| 107          | Grace Kim       | Marketing Manager  | 82000              | 8                   |
| 108          | Henry Adams     | Marketing Manager  | 58000              | 5                   |
| 109          | Ivy Turner      | Marketing Manager  | 65000              | 2                   |

**Candidates with at least 3 years of experience:**
- Alice Johnson: 67000
- Bob Smith: 68000
- David Lee: 62000
- Eva Green: 63000
- Frank Miller: 72000
- Grace Kim: 82000
- Henry Adams: 58000

**Average Salary Expectation Calculation:**
\[
\text{Average} = \frac{67000 + 68000 + 62000 + 63000 + 72000 + 82000 + 58000}{7} = \frac{472000}{7} \approx 67429
\]

So, the average salary expectation for **Marketing Managers** with at least 3 years of experience is **67,429**.

---

#### **Step 5: Create a Summary Table**
You can create a summary table to display the average salary expectations for each position. Here’s an example:



| Applied Position   | Average Salary Expectation |
|--------------------|----------------------------|
| Marketing Manager  | 67429                      |
| Data Analyst       | (Calculate similarly)      |
| HR Manager         | (Calculate similarly)      |
| Software Engineer  | (Calculate similarly)      |

</mui:table-metadata>

---

#### **Step 6: Automate the Calculation**
To automate this for all positions, you can use a combination of the `AVERAGEIFS` function and a list of unique positions. Here’s how:

1. List all unique positions in a column (e.g., Column A in a new sheet).
2. Use the following formula in the adjacent column (e.g., Column B):
   ```excel
   =AVERAGEIFS('Base DATA'!$G:$G, 'Base DATA'!$C:$C, A2, 'Base DATA'!$H:$H, ">=3")
   ```
   - Replace `A2` with the cell containing the position name.
   - Drag the formula down to apply it to all positions.

---

### **Conclusion**
Using the `AVERAGEIFS` function, you can efficiently calculate the average salary expectation for candidates with at least 3 years of experience for each applied position. This method ensures accuracy and saves time by automating the calculations.

Would you like help with any other calculations or analyses?
