Selezionare tutti gli studenti nati nel 1990:
EX-1 {
    SELECT *
    FROM `students`
    WHERE YEAR (`date_of_birth`) = 1990;
}

Selezionare tutti i corsi che valgono più di 10 crediti:
EX-2 {
    SELECT *
    FROM `courses`
    WHERE `CFU` > 10;
}

Selezionare tutti gli studenti che hanno più di 30 anni:
EX-3 {
    SELECT *
    FROM `students`
    WHERE timestampdiff(YEAR, `date_of_birth`, CURDATE()) > 30;
}

Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di
laurea:
EX-4 {
    SELECT *
    FROM `courses`
    WHERE `year` = '1'
    AND `period` = 'I semestre'
}

Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del
20/06/2020:
EX-5 {
    SELECT *
    FROM `exams`
    WHERE `date` = '2020-06-20'
    AND HOUR (`hour`) >= '14';
}

Selezionare tutti i corsi di laurea magistrale 
EX-6 {
    SELECT *
    FROM `degrees`
    WHERE `level` = 'magistrale';
}

Da quanti dipartimenti è composta l'università?
EX-7 {
    SELECT COUNT(*) AS `departments`
    FROM `departments`;
}