Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia
EX-1 {
   SELECT `students`.*
    FROM `students`
    JOIN `degrees` ON `students`.`degree_id` = `degrees`.`id`
    WHERE `degrees`.`name` = 'Corso di Laurea in Economia'; 
}