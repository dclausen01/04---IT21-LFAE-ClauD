# Erstellen eines ChatBots für schul.cloud
* Analyse der Zielgruppe: Welche Funktionen könnte gewünscht sein?
	* z. B. Überwachung für Events in einem Kanal
	* z. B. Integration von KI-Funktionen (KI-ChatBot)
	* z. B. ...
* Umsetzung auf Basis eines bestehenden Skripts 
	* https://github.com/heinrich-ulbricht/stashcat-api-client
	* https://github.com/lksmrl/hermine-stashcat-ps

# Entwicklung einer (Web-)Anwendung für die Stundenplanung
* Gegeben ist ein Stundenraster für Lehrkräfte, Klassen & Räume
* Gesucht sind Eineindeutige Zuordnungen, die zu einem konsistenten Stundenplan führen, der folgende Rahmenbedingungen erfüllt:
	* Möglichst wenig Freistunden (für Klassen sind 0-2 akzeptabel, für Lehrkräfte 0-4)
	* Gewisse Unterrichte (Biologie, Physik, Informatik) erfordern Fachräume
	* Es sollen maximal 1.-10. Stunde vergeben werden, im Normalfall nur 1.-8. Std.