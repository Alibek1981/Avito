Ответ на тестовое задание №1

SELECT

DISTING task_status.issue_key AS issue_key,

task_info.name AS name,

task_info.type AS type,

task_status.status AS status,

task_status.start_time AS start_time

FROM

task_status
INNER JOIN task_info ON task_info.issue_key = task_status.issue_key

WHERE

task_info.type = 'Bug' AND task_status.status = 'in progress' AND task_status.start_time BETWEEN '2021-04-01' AND '2021-04-30';
