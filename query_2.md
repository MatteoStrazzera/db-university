## Group by

- Contare quanti iscritti ci sono stati ogni anno
    - Query: SELECT year(`enrolment_date`) AS enrolment_year, COUNT(*) AS tot_enrolment FROM `students` GROUP BY year(`enrolment_date`);
        - Results: 2018 -> 912, 2019 -> 1709, 2020 -> 1645, 2021 -> 734

- Contare gli insegnanti che hanno l'ufficio nello stesso edificio
    - Query: SELECT `office_address`, COUNT(*) AS tot_teachers FROM `teachers` GROUP BY `office_address`;
        - Results:

- Calcolare la media dei voti di ogni appello d'esame
    - Query: SELECT `exam_id`, avg(`vote`) FROM `exam_student` GROUP BY `exam_id` ;
        - Results:

- Contare quanti corsi di laurea ci sono per ogni dipartimento
    - Query: SELECT `department_id`, COUNT(*) AS tot_degrees FROM `degrees` GROUP BY `department_id`;
        - Results: 

## Joins

- Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia
- Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze
- Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)
- Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e nome
- Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti
- Selezionare tutti i docenti che insegnano nel Dipartimento di Matematica (54)
- BONUS: Selezionare per ogni studente il numero di tentativi sostenuti per ogni esame, stampando anche il voto massimo. Successivamente, filtrare i tentativi con voto minimo 18.