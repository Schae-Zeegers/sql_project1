# sql_project1
An intermediate SQL project on analyzing student's mental health.
SELECT 
    stay,
    COUNT(*) AS count_int,
    ROUND(AVG(todep)::numeric, 2) AS average_phq,
    ROUND(AVG(tosc)::numeric, 2) AS average_scs,
    ROUND(AVG(toas)::numeric, 2) AS average_as
FROM students
WHERE inter_dom = 'Inter'
GROUP BY stay
ORDER BY stay DESC;

