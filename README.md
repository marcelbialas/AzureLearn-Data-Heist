# Szenario: „The Data Heist – Die Entschlüsselung der Verkaufsdaten“

Du bist Teil eines Teams von Dateningenieuren bei einer globalen Einzelhandelskette, die in die Welt des E-Commerce expandiert. Die Geschäftsführung hat ein großes Ziel: die Verkaufsdaten aus verschiedenen Regionen und Vertriebskanälen zu vereinen, um zukünftige Verkaufsprognosen zu optimieren und das Lager effizient zu steuern.

### Deine Aufgabe?

Du wirst ein „Datenraub“ durchführen – und das im besten Sinne! Dein Team muss einen sicheren, schnellen und effizienten Weg finden, die Verkaufsdaten von mehreren Quellen zu sammeln, zu transformieren und zu speichern.

**Es gibt jedoch ein Problem**: Die Daten sind nicht gut strukturiert, sie kommen in verschiedenen Formaten und sind teils unvollständig. Dein Team muss die Daten in ein Data Lake migrieren, sie bereinigen und dann für Analyse und Reporting vorbereiten.

Die Daten haben „versteckte“ Felder, die nur von den „richtigen“ Augen entdeckt werden können. Dein Chef will, dass du aus den Daten nicht nur Fakten ziehst, sondern auch die versteckten Muster und Trends erkennst, um das Geschäft für die Zukunft zu optimieren. Deine Pipeline muss dabei alle bisherigen Herausforderungen meistern.

---

## Die Mission (30 Minuten):

### 1. Die „Zerknitterten Verkaufsdaten“ entdecken:

Du erhältst zwei unstrukturierte Datensätze von deinem Team:

- **sales_data.csv**: Dieser Datensatz enthält Verkaufsdaten, aber es fehlen für einige Produkte Werte wie z.B. Produktkategorie oder Region.
- **transactions_data.json**: Enthält Transaktionen, jedoch ohne Verweise auf die Produkte, die verkauft wurden. Es ist, als würde man eine Rechnung sehen, aber die Artikelbeschreibung fehlt.

**Dein Job:**

Analysiere die Rohdaten und überprüfe, ob es „versteckte“ Probleme gibt (wie z.B. fehlende Felder, ungültige Datumsangaben, inkonsistente Produkt-IDs).

---

### 2. „Data Heist“: Die Pipeline einrichten:

Es wird Zeit, den „Raub“ durchzuführen: Du musst eine Data Factory Pipeline erstellen, die die Daten aus dem Azure Blob Storage in das Data Lake Gen2 überträgt.

Die Daten müssen von ihren unterschiedlichen Formaten (CSV und JSON) in das Parquet-Format transformiert werden – für eine effiziente Speicherung und schnelle Abfragen.

**Transformationen:** Du wirst die Transaktionsdaten aus der JSON-Datei mit den Verkaufsdaten aus der CSV verbinden. Aber Achtung – die Produkt-IDs und die Transaktionsnummern stimmen möglicherweise nicht überein. **Deine Aufgabe ist es, Datenfehler zu erkennen und zu beheben und dabei eine saubere und effiziente Pipeline zu bauen.**

**Wichtig:** Einige Produkte könnten doppelt in den Datensätzen auftauchen, und du musst sicherstellen, dass diese nicht zu doppelten Transaktionen führen. Achte darauf, wie du diese Daten korrekt bereinigst!

---

### 3. Der „Product Analyst“-Test:

Nachdem du die Daten erfolgreich im Data Lake gespeichert hast, geht es darum, deine Datenabfrage-Fähigkeiten zu testen:

Du musst jetzt eine SQL-Abfrage schreiben, die alle Transaktionen des Produkts mit dem höchsten Umsatz der letzten 30 Tage ausgibt. Hierbei solltest du sicherstellen, dass null-Werte und fehlerhafte Daten richtig behandelt werden.

**Frage: „Welches Produkt hat die höchste Verkaufszahl im letzten Monat?“**  
Dein Chef wird die Antwort als den „Goldenen Schlüssel“ betrachten. Wird es der Kaffeebecher mit dem Motiv „Data Enthusiast“ oder der Hochleistungs-PC sein?

---

### 4. Zusatzaufgabe: Die „Ungeklärte Transaktionsmuster“ finden:

Während der Datenanalyse stößt du auf einen geheimen „Warenkorb“: Ein Produkt, das in den letzten 30 Tagen ungewöhnlich viele Transaktionen hatte, aber der Umsatz im Vergleich zu anderen Produkten minimal war.

**Zusatzaufgabe:** Finde heraus, warum dieses Produkt viele Transaktionen hat, aber wenig Umsatz generiert. Welche Analyse könntest du durchführen, um diese Anomalie zu erklären?  
Tipp: Achte auf die Menge der gekauften Produkte in den Transaktionen.

Viel Spaß beim „Heist“ – und pass auf, dass die Daten nicht entkommen! 😎
