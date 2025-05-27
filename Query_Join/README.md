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