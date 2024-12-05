```sql

(query 1):

SELECT YEAR(enrolment_date) AS anno_iscrizione, COUNT(*) AS numero_iscritti
FROM students
GROUP BY YEAR(enrolment_date);

15:12:25	SELECT YEAR(enrolment_date) AS anno_iscrizione, COUNT(*) AS numero_iscritti FROM students GROUP BY YEAR(enrolment_date)	4 row(s) returned	0.078 sec / 0.000 sec



(query 2):

SELECT office_address, COUNT(DISTINCT id) AS numero_insegnanti
FROM teachers
GROUP BY office_address;

15:28:31	SELECT office_address, COUNT(DISTINCT id) AS numero_insegnanti FROM teachers GROUP BY office_address	29 row(s) returned	0.063 sec / 0.000 sec




(query 3)

SELECT exam_id, AVG(vote) AS media_voti
FROM exam_student
GROUP BY exam_id;

15:34:57	SELECT exam_id, AVG(vote) AS media_voti FROM exam_student GROUP BY exam_id	4078 row(s) returned	0.000 sec / 0.031 sec


``` 