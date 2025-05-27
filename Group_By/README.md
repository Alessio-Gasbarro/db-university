Contare quanti iscritti ci sono stati ogni anno
- EX-1 {
    SELECT YEAR(`enrolment_date`) AS `anno_iscrizione`, COUNT(*) AS `numero_studenti`
    FROM `students`
    GROUP BY YEAR(`enrolment_date`)
    ORDER BY `anno_iscrizione`;
}

Contare gli insegnanti che hanno l'ufficio nello stesso edificio
- EX-2 {
    SELECT `office_address`, COUNT(*) AS `numero_docenti`
    FROM `teachers`
    GROUP BY `office_address`;
}

Calcolare la media dei voti di ogni appello d'esame
- EX-3 {
    SELECT `exam_id`, AVG(`vote`) AS `media_voti`
    FROM `exam_student`
    GROUP BY `exam_id`;
}

Contare quanti corsi di laurea ci sono per ogni dipartimento
- EX-4 {
    SELECT `departments`.`name` AS `dipartimento`, COUNT(`degrees`.`id`) AS `numero_corsi_laurea`
    FROM `degrees`
    JOIN `departments` ON `degrees`.`department_id` = `departments`.`id`
    GROUP BY `departments`.`name`;
}