15:14:38	SELECT* FROM students WHERE YEAR(date_of_birth) = 1990 LIMIT 0, 1000	160 row(s) returned	0.000 sec / 0.000 sec

15:25:47	SELECT * FROM courses WHERE cfu> 10 LIMIT 0, 1000	479 row(s) returned	0.000 sec / 0.000 sec

15:36:11	SELECT * FROM students WHERE YEAR(NOW()) - YEAR(date_of_birth) > 30	3646 row(s) returned	0.000 sec / 0.015 sec

15:42:34	SELECT * FROM courses WHERE period = 'I semestre' AND year = 1	286 row(s) returned	0.000 sec / 0.000 sec

15:46:17	SELECT * FROM exams WHERE date = "2020-06-20" AND hour > "14:00:00"	21 row(s) returned	0.015 sec / 0.000 sec

15:53:22	SELECT *  FROM degrees  WHERE level = 'magistrale'	38 row(s) returned	0.000 sec / 0.000 sec

15:58:46	SELECT * FROM departments	12 row(s) returned	0.000 sec / 0.000 sec

16:01:12	SELECT *  FROM teachers WHERE phone IS NULL	50 row(s) returned	0.000 sec / 0.000 sec

16:33:01	INSERT INTO students (name, surname, date_of_birth, degree_id, fiscal_code, enrolment_date, registration_number, email)  VALUES ('Roberto', 'Maligni', '1952-10-27', 7,'MLGRRT52R27D612Y','2024-12-04', '621033', 'maligni-roberto@evil.com')	1 row(s) affected	0.297 sec

16:39:39	UPDATE teachers SET office_number = 126  WHERE id = 58	1 row(s) affected Rows matched: 1  Changed: 1  Warnings: 0	0.188 sec

16:44:20	DELETE FROM students  WHERE id =5001	1 row(s) affected	0.078 sec