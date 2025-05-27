Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia
- EX-1 {
    SELECT `students`.*
    FROM `students`
    JOIN `degrees` ON `students`.`degree_id` = `degrees`.`id`
    WHERE `degrees`.`name` = 'Corso di Laurea in Economia'; 
}

Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze
- EX-2 {
    SELECT `degrees`.*
    FROM `degrees`
    JOIN `departments` ON `degrees`.`department_id` = `departments`.`id`
    WHERE `departments`.`name` = 'Neuroscienze'
    AND `degrees`.`level` = 'magistrale';
}

Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)
- EX-3 {
    SELECT `courses`.*
    FROM `courses`
    JOIN `course_teacher` ON `courses`.`id` = `course_teacher`.`course_id`
    WHERE `course_teacher`.`teacher_id` = 44;
}

Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui
 sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e
 nome
- EX-4 {
    SELECT `students`.*, `degrees`.`name` AS `degree_name`, `departments`.`name` AS `department_name`
    FROM `students`
    JOIN `degrees` ON `students`.`degree_id` = `degrees`.`id`
    JOIN `departments` ON `degrees`.`department_id` = `departments`.`id`
    ORDER BY `students`.`surname`, `students`.`name`;
}

Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti
- EX-5 {
    SELECT `degrees`.*, `courses`.`name` AS `course_name`, `teachers`.`name` AS `teacher_name`, `teachers`.`surname` AS `teacher_surname`
    FROM `degrees`
    JOIN `courses` ON `degrees`.`id` = `courses`.`degree_id`
    JOIN `course_teacher` ON `courses`.`id` = `course_teacher`.`course_id`
    JOIN `teachers` ON `course_teacher`.`teacher_id` = `teachers`.`id`;
}