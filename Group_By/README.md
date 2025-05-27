Contare quanti iscritti ci sono stati ogni anno
- EX-1 {
    SELECT YEAR(`enrolment_date`) AS `anno_iscrizione`, COUNT(*) AS `numero_studenti`
    FROM `students`
    GROUP BY YEAR(`enrolment_date`)
    ORDER BY `anno_iscrizione`;
}