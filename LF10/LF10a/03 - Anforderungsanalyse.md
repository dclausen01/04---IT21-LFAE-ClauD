---
sticker: emoji//1f532
---
# Aufgabe

Lest im Lehrbuch die **Seiten 13ff.** und bearbeitet die **Aufgaben 2 und 3** auf **Seite 16** (bei Aufgabe 3: Wählt einen Prozess aus Eurem Arbeitsumfeld aus - wir arbeiten nicht mit der Lernsituation 1) - *für beide Aufgaben könnt ihr zwischen Partner- und Kleingruppenarbeit wählen.* Geht danach weiter im Buch bis zur **Aufgabe 2** auf **Seite 19**.

## Ergebnisse:

## BiBox Seite 16 - Aufgabe 2

```plantuml-svg
start
:Ermittlung des Liegeplatzes;

if () then ([neuer Liegeplatz])
	:Neuen Liegeplatz anlegen in Excel;
	:Daten eingeben;
else ([bestehender Liegeplatz])
	:Liegeplatz in der Excel-Tabelle raussuchen;
	:Daten ändern;
endif

:Daten manuell überprüfen;
:Daten speichern;
:Datenblatt ausdrucken;

if () then ([neuer Liegeplatz])
	:Datenblatt dem Liegeplatz-
	verwaltungsordner hinzufügen;
else ([bestehender Liegeplatz])
	:altes Datenblatt raussuchen und durch neues im Liegeplatz-
	verwaltungsordner ersetzen;
endif

end
```

```plantuml-svg
start
:Ermittlung des Liegeplatzes;
:Daten eingeben;
:Daten automatisch überprüfen lassen;

if (Liegeplatz in der Datenbank) then (false)
	:Erstellung eines Liegeplatzes in der Datenbank;
else (true)
	:Modifizieren des Liegeplatzes in der Datenbank;
endif

:Änderungen an der Datenbank speichern;

:Datenblatt;
note right
	Statt dem physischen Datenblatt
	sollte ein digitales Datenblatt 
	verwaltet werden
end note

end
```

## BiBox Seite 16 - Aufgabe 3

```plantuml-svg
start

:Erstellung einer leeren API über
das Create-Formular in der Weboberfläche;

:Händisches kopieren der ApiId aus den URL-Parametern;

:Konfigurieren der GH-Upload-Action
mit der kopierten ApiID;

:Ausführen der Action mit notwendigen Parametern;

end
```

## BiBox Seite 19 - Aufgabe 2

| Funktionale Anforderungen                                     | Nicht funktionale Anforderungen                                                     |
| ------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| Mehrere Liegeplätze gleichzeitig anlegen (prozessbezogen)     | Unterstützung verschiedener Sprachen (rahmenbedingung)                              |
| Implementierung verschiedener Themes (interaktionsbezogen)    | Die Anwendung wurde nach der Material Specification von Google gestaltet (qualität) |
| Gestaltung einer Systemunabhängigen Weboberfläche (technisch) | Die Anwendung ist DSGVO konform (rahmenbedingung)                                                                                    |
| Implementierung von Authentifizierung (technisch)             |                                                                                     |
| Endkunden können gebuchte Liegeplätze einsehen (prozess)      |                                                                                     |

