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