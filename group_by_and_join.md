```sql

(query 1):

SELECT YEAR(enrolment_date) AS anno_iscrizione, COUNT(*) AS numero_iscritti
FROM students
GROUP BY YEAR(enrolment_date);

15:12:25	SELECT YEAR(enrolment_date) AS anno_iscrizione, COUNT(*) AS numero_iscritti FROM students GROUP BY YEAR(enrolment_date)	4 row(s) returned	0.078 sec / 0.000 sec





``` 