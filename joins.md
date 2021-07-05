JOINS:
# 1. Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia

SELECT students.id, students.name, students.surname, students.date_of_birth, students.registration_number 
FROM students 
JOIN degrees 
ON students.degree_id = degrees.id 
WHERE degrees.name = "Corso di Laurea in Economia"

# 2. Selezionare tutti i Corsi di Laurea del Dipartimento di Neuroscienze

SELECT degrees.id, degrees.name, degrees.level, degrees.website 
FROM degrees 
JOIN departments 
ON degrees.department_id = departments.id 
WHERE departments.name = "Dipartimento di Neuroscienze"

# 3. Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)

SELECT teachers.id AS 'teacher_id', teachers.name, teachers.surname, courses.name, courses.description, courses.period, courses.year, courses.website 
FROM course_teacher 
JOIN teachers 
ON course_teacher.teacher_id = teachers.id 
JOIN courses 
ON course_teacher.course_id = courses.id 
WHERE teachers.id = 44

# 4. Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e nome


# 5. Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti


# 6. Selezionare tutti i docenti che insegnano nel Dipartimento di Matematica (54)
