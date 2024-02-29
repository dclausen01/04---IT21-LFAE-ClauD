---
sticker: emoji//1f532
---


> [!NOTE]
> Hier sind Musterlösungen für die 8 Aufgaben mit den entsprechenden SQL-Abfragen:

### Musterlösungen:

#### 1. Mitarbeiter und ihre Abteilungen:
```sql
SELECT e.name AS Mitarbeiter, e.position AS Position, d.name AS Abteilung
FROM employees e
INNER JOIN departments d ON e.department_id = d.department_id;
```

#### 2. Mitarbeiter und ihre Projekte:
```sql
SELECT e.name AS Mitarbeiter, p.name AS Projekt
FROM employees e
LEFT JOIN projects p ON e.department_id = p.department_id;
```

#### 3. Mitarbeiter, die mehr verdienen als der Durchschnitt ihres Departments:
```sql
SELECT e.name AS Mitarbeiter, e.position AS Position, e.salary AS Gehalt, AVG(e.salary) OVER (PARTITION BY e.department_id) AS Abteilungs_Durchschnitt
FROM employees e
WHERE e.salary > (SELECT AVG(salary) FROM employees WHERE department_id = e.department_id);
```

#### 4. Projekte und die Mitarbeiter, die daran arbeiten:
```sql
SELECT p.name AS Projekt, e.name AS Mitarbeiter
FROM projects p
LEFT JOIN employees e ON p.department_id = e.department_id;
```

#### 5. Abteilungen ohne aktive Projekte:
```sql
SELECT d.name AS Abteilung, COUNT(e.employee_id) AS Anzahl_Mitarbeiter
FROM departments d
LEFT JOIN employees e ON d.department_id = e.department_id
LEFT JOIN projects p ON d.department_id = p.department_id
WHERE p.project_id IS NULL
GROUP BY d.name;
```

#### 6. Mitarbeiter, die nicht an Projekten arbeiten:
```sql
SELECT e.name AS Mitarbeiter, d.name AS Abteilung
FROM employees e
LEFT JOIN projects p ON e.department_id = p.department_id
INNER JOIN departments d ON e.department_id = d.department_id
WHERE p.project_id IS NULL;
```

#### 7. Gesamtgehalt pro Abteilung:
```sql
SELECT d.name AS Abteilung, SUM(e.salary) AS Gesamtgehalt
FROM employees e
INNER JOIN departments d ON e.department_id = d.department_id
GROUP BY d.name;
```

#### 8. Projekte mit mehr als zwei Mitarbeitern:
```sql
SELECT p.name AS Projekt, COUNT(e.employee_id) AS Anzahl_Mitarbeiter
FROM projects p
INNER JOIN employees e ON p.department_id = e.department_id
GROUP BY p.name
HAVING COUNT(e.employee_id) > 2;
```

Diese Musterlösungen sollten Ihnen eine Vorstellung davon geben, wie die SQL-Abfragen für die gestellten Aufgaben aussehen könnten. Bitte beachten Sie, dass je nach SQL-Dialekt oder Datenbanksystem leichte Anpassungen erforderlich sein könnten.