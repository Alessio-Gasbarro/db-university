EX-1 {
    SELECT *
    FROM `students`
    WHERE YEAR (`date_of_birth`) = 1990;
}

EX-2 {
    SELECT *
    FROM `courses`
    WHERE `CFU` > 10;
}

EX-3 {
    SELECT *
    FROM `students`
    WHERE timestampdiff(YEAR, `date_of_birth`, CURDATE()) > 30;
}

EX-4 {
    SELECT *
    FROM `courses`
    WHERE `year` = '1'
    AND `period` = 'I semestre'
}