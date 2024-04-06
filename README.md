# Analyzing students mental health.

### Project Overview
---

This project aims to explore and analyze the students data to see how the length of stay impacts the mental health diagnostic scores of International students that were a part of the study.

### Data sources
---

The primary data source used for this analysis is the 'students.csv' file, it is a compilation of the data collected from Japanese students in 2018, it consists of information on the demographics and various mental health indicators of the students.

### Tools
---

- SQL (PostgreSQL) for analysis

### Exploratory data analysis
---

```sql
SELECT stay, COUNT(inter_dom) AS count_int,
  ROUND(AVG(todep),2) AS average_phq,
  ROUND(AVG(tosc),2) AS average_scs,
  ROUND(AVG(toas),2) AS average_as
FROM students
WHERE inter_dom = 'Inter'
GROUP BY stay
ORDER BY stay DESC;
```
