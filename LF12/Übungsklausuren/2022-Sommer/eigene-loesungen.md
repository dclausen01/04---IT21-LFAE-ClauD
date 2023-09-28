### Mike Süberkrüb

```c++
type Datensatz = {
	datum: date,
	zeit: time,
	storniert: boolean,
	stattgefunden: boolean
}

type StatistikenObjekt = {
	storniert: integer,
	stattgefunden: integer,
	ausgefallen: integer
}

class Statistiken = {
	private kw: StatistikenObjekt[];
	private gesamtStatistiken: StatistikenObjekt;

	Statistiken(jahr: string) {
		anzahlKW = GetAnzahlKW(jahr)
		this.kw = StatistikenObjekt[anzahlKW]

		for (i = 0; i < anzahlKW; i++) {
			this.kw[i] = {
				storniert: 0,
				stattgefunden: 0,
				ausgefallen: 0
			}
		}
	}

	get kwStatistiken(): StatistikenObjekt[] {
		return this.kw;
	}

	get gesamtStatistiken(): StatistikenObjekt {
		return this.gesamtStatistiken;
	}

	addiereDatensatz(datensatz: Datensatz): void {
		aktuelleKW = GetKW(datensatz.datum);

		storniert: integer = datensatz.storniert;
		stattgefunden: integer = datensatz.stattgefunden;
		ausgefallen: integer = !datensatz.storniert && !datensatz.stattgefunden;

		this.kw[aktuelleKW].storniert += storniert;
		this.gesamtStatistiken.storniert += storniert;
		this.kw[aktuelleKW].stattgefunden += stattgefunden;
		this.gesamtStatistiken.stattgefunden += stattgefunden;
		this.kw[aktuelleKW].ausgefallen += ausgefallen;
		this.gesamtStatistiken.ausgefallen += ausgefallen;
	}
}

procedure printList(datenliste: Datensatz[], jahr: number) {
	statistiken: Statistiken = new Statistiken(jahr);
	for (datensatz : datenliste) {
		statistiken.addiereDatensatz(datensatz)
	}

	printKopf();
	for (i = 0; i < statistiken.kw.length; i++) {
		printKW(i + 1, statistiken.kw[i].storniert,
			statistiken.kw[i].stattgefunden,
			statistiken.kw[i].ausgefallen)
	}
	printJahr(statistiken.gesamtStatistiken[i].storniert,
		statistiken.gesamtStatistiken[i].stattgefunden,
		statistiken.gesamtStatistiken[i].ausgefallen)
}

```
