---
sticker: emoji//1f532
---
### Komplexe Lernaufgabe für SQL JOINs

#### Die Datenbankstruktur:

Wir haben eine Datenbank für ein fiktives Unternehmen namens "TechCorp", das verschiedene Abteilungen, Mitarbeiter und Projekte hat. Hier sind die Tabellen, die in Beziehung zueinander stehen:

##### Tabelle: `employees`

|employee_id|name|department_id|position|salary|
|---|---|---|---|---|
|1|Max Mustermann|1|Manager|70000|
|2|Maria Schmidt|2|Developer|60000|
|3|Hans Müller|1|Analyst|55000|
|4|Julia Wagner|3|Designer|50000|
|5|Alex Fischer|2|Developer|60000|

##### Tabelle: `departments`

|department_id|name|
|---|---|
|1|Marketing|
|2|Engineering|
|3|Design|

##### Tabelle: `projects`

|project_id|name|department_id|
|---|---|---|
|101|Marketing Campaign|1|
|102|New Feature|2|
|103|Website Redesign|3|
|104|Product Launch|1|

#### Aufgabenstellung:

Schreiben Sie SQL-Abfragen, um die folgenden Informationen aus der Datenbank abzurufen.

1. **Mitarbeiter und ihre Abteilungen:**
    - Liste Sie den Namen des Mitarbeiters, seine Position und den Namen seiner Abteilung auf.
2. **Mitarbeiter und ihre Projekte:**
    - Zeigen Sie den Namen des Mitarbeiters und den Namen des Projekts an, an dem er/sie arbeitet.
3. **Mitarbeiter, die mehr verdienen als der Durchschnitt ihres Departments:**
    - Geben Sie den Namen des Mitarbeiters, seine Position, das Gehalt und den Durchschnitt des Gehalts in seiner Abteilung aus. Zeigen Sie nur Mitarbeiter an, die mehr verdienen als der Durchschnitt ihrer Abteilung.
4. **Projekte und die Mitarbeiter, die daran arbeiten:**
    - Listen Sie den Projektnamen und die Namen der Mitarbeiter auf, die an jedem Projekt arbeiten.
5. **Abteilungen ohne aktive Projekte:**
    - Zeigen Sie den Namen und die Anzahl der Mitarbeiter für jede Abteilung an, die derzeit keine aktiven Projekte hat.
6. **Mitarbeiter, die nicht an Projekten arbeiten:**
    - Stellen Sie eine Liste der Mitarbeiter ohne aktive Projekte zusammen, einschließlich ihres Namens und ihrer Abteilung.
7. **Gesamtgehalt pro Abteilung:**
    - Berechnen Sie das Gesamtgehalt für jede Abteilung und listen Sie den Namen der Abteilung sowie das Gesamtgehalt auf.
8. **Projekte mit mehr als zwei Mitarbeitern:**
    - Zeigen Sie den Projektnamen und die Anzahl der Mitarbeiter an, die an jedem Projekt arbeiten. Zeigen Sie nur Projekte an, an denen mehr als zwei Mitarbeiter beteiligt sind.

#### Hinweise:
- Verwenden Sie die SQL JOIN-Befehle (INNER JOIN, LEFT JOIN, RIGHT JOIN) entsprechend, um die Tabellen zu verbinden.
- Berücksichtigen Sie, dass nicht jeder Mitarbeiter an einem Projekt arbeitet und nicht jede Abteilung aktive Projekte haben muss.
- Verwenden Sie Aggregatfunktionen wie AVG(), COUNT(), und SUM(), um bestimmte Informationen zu berechnen.
- Denken Sie daran, Aliasnamen für Spalten zu verwenden, um die Ergebnisse lesbarer zu machen.

Diese Aufgaben sollten eine gute Übung für das Verständnis von SQL JOINs und anderen wichtigen SQL-Operationen bieten. Viel Erfolg!

---
