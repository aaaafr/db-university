<!-- 1 -->
SELECT * FROM students WHERE date_of_birth BETWEEN '1990-01-01' AND '1990-12-31'

<!-- 2 -->

SELECT * FROM courses WHERE cfu > 10


<!-- 3 -->
SELECT * FROM students WHERE date_of_birth < '1991-12-31'

<!-- 4 -->
SELECT * FROM courses WHERE period = 'I semestre' AND year = 1

<!-- 5 -->
SELECT * FROM exams WHERE date = '2020/06/20' AND hour > '14:00:00'


<!-- 6 -->
SELECT * FROM degrees WHERE level = 'magistrale'

<!-- 7 -->
SELECT COUNT(*) FROM departments

<!-- 8 -->
SELECT * FROM teachers WHERE phone IS NULL

SELECT COUNT(*) FROM teachers WHERE phone IS NULL


<!-- GROUP BY:
Contare quanti iscritti ci sono stati ogni anno
Contare gli insegnanti che hanno l'ufficio nello stesso edificio
Calcolare la media dei voti di ogni appello d'esame
Contare quanti corsi di laurea ci sono per ogni dipartimento
JOINS:
Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia
Selezionare tutti i Corsi di Laurea del Dipartimento di Neuroscienze
Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)
Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e nome
Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti
Selezionare tutti i docenti che insegnano nel Dipartimento di Matematica (54)
BONUS: Selezionare per ogni studente quanti tentativi d’esame ha sostenuto per superare ciascuno dei suoi esami -->


<!-- group by  -->

<!-- 1 -->
SELECT COUNT(id) FROM students GROUP BY enrolment_date


<!-- 2  -->
SELECT COUNT(id) FROM teachers GROUP BY office_address

<!-- 3 -->


<!-- 4 -->
SELECT COUNT(id) FROM degrees GROUP BY department_id



<!-- joins -->
<!-- 1 -->
SELECT * FROM students INNER JOIN degrees ON degree_id = students.degree_id  WHERE degrees.name = 'Corso di Laurea in Economia'

<!-- 2 -->
SELECT * FROM degrees INNER JOIN departments ON departments.id = degrees.department_id WHERE departments.name = 'Dipartimento di Neuroscienze'

<!-- 3 -->


