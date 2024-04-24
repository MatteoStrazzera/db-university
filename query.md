# Descrizione esercizio

Dopo aver creato un nuovo database nel vostro phpMyAdmin e aver importato lo schema allegato, eseguite le query del file allegato.

Cosa consegnare?
Dopo aver testato le vostre query con phpMyAdmin, riportatele in un file query.md e caricatelo nella vostra repo.

- Selezionare tutti gli studenti nati nel 1990 (160)
    - Query: SELECT * FROM `students` WHERE year(`date_of_birth`) = 1990;

- Selezionare tutti i corsi che valgono più di 10 crediti (479)
    - Query: SELECT * FROM `courses` WHERE `cfu` >= 10;

- Selezionare tutti gli studenti che hanno più di 30 anni
    - Query: SELECT * FROM `students` WHERE (year(curtime()) - year(`date_of_birth`)) > 30;

- Selezionare tutti i corsi del primo semestre del primo anno di un qualsiasi corso di laurea (286)
    - Query: SELECT * FROM `courses` WHERE `period` = 'I semestre' AND `year` = 1;

- Selezionare tutti gli appelli d'esame che avvengono nel pomeriggio (dopo le 14) del 20/06/2020 (21)
    - Query: SELECT * FROM `exams` WHERE `date` = '2020-06-20' AND `hour` >= '14:00:00';

- Selezionare tutti i corsi di laurea magistrale (38)
    - Query: SELECT * FROM `degrees` WHERE `level` = 'magistrale';

- Da quanti dipartimenti è composta l'università? (12)
    - Query: SELECT COUNT(*) AS 'total_dep' FROM `departments`;

- Quanti sono gli insegnanti che non hanno un numero di telefono? (50)
    - Query: SELECT * FROM `teachers` WHERE `phone` IS NULL;