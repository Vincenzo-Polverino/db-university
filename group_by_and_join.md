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



(query 4)

SELECT department_id, COUNT(*) AS numero_corsi_laurea
FROM degrees
GROUP BY department_id;

15:39:24	SELECT department_id, COUNT(*) AS numero_corsi_laurea FROM degrees GROUP BY department_id	12 row(s) returned	0.000 sec / 0.000 sec



(query 5)

SELECT students.name, students.surname
FROM students
JOIN degrees ON students.degree_id = degrees.id
WHERE degrees.name = 'Corso di Laurea in Diritto dell\'Economia';

15:57:43	SELECT students.name, students.surname FROM students JOIN degrees ON students.degree_id = degrees.id WHERE degrees.name = 'Corso di Laurea in Diritto dell\'Economia'	65 row(s) returned	0.000 sec / 0.000 sec



(query 6)

SELECT degrees.name
FROM degrees
JOIN departments ON degrees.department_id = departments.id
WHERE departments.name = 'Dipartimento di Neuroscienze'
AND level = 'magistrale';

16:06:55	SELECT degrees.name FROM degrees JOIN departments ON degrees.department_id = departments.id WHERE departments.name = 'Dipartimento di Neuroscienze' AND level = 'magistrale'	1 row(s) returned	0.000 sec / 0.000 sec



(query 7)

SELECT *
FROM course_teacher
JOIN courses ON course_teacher.course_id = courses.id
WHERE teacher_id = 44

16:38:45	SELECT * FROM course_teacher JOIN courses ON course_teacher.course_id = courses.id WHERE teacher_id = 44	11 row(s) returned	0.000 sec / 0.000 sec



(query 8)

SELECT students.name, students.surname, degrees.name, departments.name
FROM students
JOIN degrees ON students.degree_id = degrees.id
JOIN departments ON degrees.department_id = departments.id
ORDER BY students.surname, students.name;

16:44:29	SELECT students.name, students.surname, degrees.name, departments.name FROM students JOIN degrees ON students.degree_id = degrees.id JOIN departments ON degrees.department_id = departments.id ORDER BY students.surname, students.name	5000 row(s) returned	0.094 sec / 0.000 sec



(query 9)

SELECT degrees.name AS nome_corsi_laurea, courses.name AS nome_corsi, teachers.name AS nome_insegnanti, teachers.surname AS cognome_insegnanti
FROM degrees
JOIN courses ON degrees.id = courses.id
JOIN course_teacher ON courses.id = course_id
JOIN teachers ON course_teacher.teacher_id = teachers.id;

16:59:44	SELECT degrees.name AS nome_corsi_laurea, courses.name AS nome_corsi, teachers.name AS nome_insegnanti, teachers.surname AS cognome_insegnanti FROM degrees JOIN courses ON degrees.id = courses.id JOIN course_teacher ON courses.id = course_id JOIN teachers ON course_teacher.teacher_id = teachers.id	75 row(s) returned	0.000 sec / 0.000 sec

``` 