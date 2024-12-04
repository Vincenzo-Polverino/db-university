15:14:38	SELECT* FROM students WHERE YEAR(date_of_birth) = 1990 LIMIT 0, 1000	160 row(s) returned	0.000 sec / 0.000 sec

15:25:47	SELECT * FROM courses WHERE cfu> 10 LIMIT 0, 1000	479 row(s) returned	0.000 sec / 0.000 sec

15:36:11	SELECT * FROM students WHERE YEAR(NOW()) - YEAR(date_of_birth) > 30	3646 row(s) returned	0.000 sec / 0.015 sec
