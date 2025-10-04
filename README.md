# Reporting-Analyst-Interview-Prep

### Executive Summary: The 4 Pillars of Your Preparation

Your preparation should focus on four key areas. You need to prove you have:
1.  **The Technical Skills:** You can do the work (VBA, SQL, Power BI).
2.  **The Domain Knowledge:** You understand the "what" and "why" behind the data (HR & RPO).
3.  **The Soft Skills:** You can work effectively with people and handle the work environment (stakeholder management, navigating ambiguity).
4.  **The Company Fit:** You understand and are excited about Korn Ferry's mission.

### Pillar 1: Sharpen Your Technical Skills (The "How")

They will almost certainly test your technical abilities, either through direct questions, a case study, or a live technical screen.

#### **A. VBA (Visual Basic for Applications)**
*   **Focus:** Automation and optimization. They don't just want someone who can record a macro; they want someone who can write clean, efficient code to automate complex reporting tasks.
*   **How to Prepare:**
    *   **Review Key Concepts:** Loops (`For...Next`, `Do...While`), Conditionals (`If...Then...Else`), working with objects (Workbooks, Worksheets, Ranges), error handling (`On Error GoTo`).
    *   **Prepare Your Stories:** Be ready to describe a project where you used VBA to solve a business problem.
        *   **Example 1 (Automation):** "I developed a VBA macro that consolidated weekly data from 10 different raw CSV files into a master Excel report. It formatted the data, created pivot tables, and emailed the summary to stakeholders, saving the team about 4 hours of manual work each week."
        *   **Example 2 (Optimization):** "An existing report took 5 minutes to run. I optimized the VBA code by reducing screen updating, using arrays for faster processing, and minimizing cell-by-cell interactions, which cut the run time down to 30 seconds."

#### **B. SQL (Structured Query Language)**
*   **Focus:** Data extraction and manipulation. You need to be comfortable pulling and shaping data from a database to be used in Excel or Power BI.
*   **How to Prepare:**
    *   **Practice Common Queries:** Be ready to write or explain queries using:
        *   `SELECT`, `FROM`, `WHERE`
        *   `JOIN` (especially `LEFT JOIN` and `INNER JOIN`)
        *   `GROUP BY` with aggregate functions (`COUNT`, `SUM`, `AVG`)
        *   `CASE` statements for conditional logic
        *   Subqueries or Common Table Expressions (CTEs)
    *   **Prepare a Scenario:** Be ready to explain how you would write a query to answer a business question. For example: "To find the top 5 sources for new hires in the last quarter, I would `SELECT` the source and `COUNT` of candidates, `JOIN` the candidate table with the hire table, `WHERE` the hire date is in Q3, `GROUP BY` the source, `ORDER BY` the count descending, and `LIMIT` to 5."

#### **C. Power BI**
*   **Focus:** End-to-end dashboard creation, from data connection to visualization.
*   **How to Prepare:**
    *   **Power Query:** Be ready to discuss data cleaning and transformation steps. (e.g., "I used Power Query to unpivot data, split columns, replace values, and merge different data sources to create a clean model.")
    *   **DAX (Data Analysis Expressions):** This is a key differentiator. Prepare to talk about creating measures and calculated columns. Practice key DAX functions like `CALCULATE`, `SUMX`, `FILTER`, `RELATED`, and time intelligence functions (`DATESYTD`).
    *   **Data Modeling:** Understand the basics of creating relationships between tables (star schema).
    *   **Visualization:** Be prepared to discuss *why* you chose a certain visual. (e.g., "I used a waterfall chart to show the change in headcount over the quarter, as it clearly visualizes the impact of new hires and attrition.")
    *   **Have a Portfolio Ready:** Create a small, clean dashboard (ideally with HR data) that you can share or walk them through on a screen share.

### Pillar 2: Master the Domain Knowledge (The "What" & "Why")

Since HR/RPO experience is preferred, showing you understand the context of the data will make you a much stronger candidate.

*   **Understand Key HR/Recruitment Metrics:** Research and be able to define and discuss the importance of:
    *   **Time to Fill / Time to Hire:** How long it takes to fill a role.
    *   **Cost per Hire:** Total recruiting cost divided by new hires.
    *   **Source of Hire:** Where are your best candidates coming from (e.g., referrals, LinkedIn, career fairs)?
    *   **Offer Acceptance Rate:** The percentage of candidates who accept a job offer.
    *   **Quality of Hire:** Often measured by performance review scores of new hires or retention rates.
    *   **Candidate Funnel Metrics:** How many candidates apply vs. get screened vs. interview vs. get hired.
*   **Think Like a Consultant:** Korn Ferry is a consulting firm. Don't just report the number; explain the insight.
    *   **Bad Answer:** "The time to fill is 55 days."
    *   **Good Answer:** "I built a dashboard that showed our average time to fill was 55 days, but by drilling down, we discovered that for engineering roles it was 90 days. This insight prompted the business to invest more in specialized tech recruiters and sourcing tools."

### Pillar 3: Demonstrate Your Soft Skills (The "Who")

They are looking for more than just a technician. Use the **STAR method (Situation, Task, Action, Result)** to answer behavioral questions.

*   **Stakeholder Management:**
    *   *Prepare for:* "Tell me about a time you had to present data to a non-technical stakeholder." or "Describe a time you and a stakeholder disagreed on reporting requirements."
    *   *Your Story Should Show:* You listen, understand their needs, manage expectations, and can translate complex data into simple, actionable insights.
*   **Navigating Ambiguity:**
    *   *Prepare for:* "Describe a project where the requirements were unclear or kept changing. How did you handle it?"
    *   *Your Story Should Show:* You are proactive, ask clarifying questions, make logical assumptions (and document them), and deliver a valuable first version that can be iterated upon.
*   **Proactive & Analytical Mindset:**
    *   *Prepare for:* "Tell me about a time you found an interesting trend in the data that no one had asked for."
    *   *Your Story Should Show:* You are curious, you explore data beyond the immediate request, and you can connect data points to business impact.

### Pillar 4: Show Company & Role Fit (The "Why Us?")

*   **Research Korn Ferry:**
    *   Understand their **five core solutions** (listed in the job description). Think about how your role as a Reporting Analyst directly supports "Talent Acquisition" and "Organizational Strategy."
    *   Look up Korn Ferry on the news or their insights/blog section. Mentioning a recent report or article they published shows genuine interest.
*   **Prepare Your "Why":**
    *   **"Why this role?"** Connect your skills and interests directly to the job description. Example: "I'm excited about this role because it perfectly combines my technical expertise in VBA and Power BI with my interest in using data to improve recruitment processes. I enjoy the challenge of automating reports and building dashboards that help leaders make better talent decisions."
    *   **"Why Korn Ferry?"** Connect to their mission. Example: "I'm drawn to Korn Ferry because of its reputation as a leader in organizational consulting. The opportunity to provide data insights that help clients synchronize their strategy and talent is incredibly compelling to me."

### Questions to Ask Them

Have 3-5 thoughtful questions ready. This shows you are engaged and serious.
*   "What are the biggest reporting challenges the team is currently facing?"
*   "Could you describe the data ecosystem? What databases or systems will I be primarily pulling data from?"
*   "How does this role collaborate with the consultants in the Talent Acquisition practice?"
*   "What does success look like in the first 3-6 months for the person in this role?"
*   "What are the opportunities for learning and professional development within the analytics function at Korn Ferry?"
