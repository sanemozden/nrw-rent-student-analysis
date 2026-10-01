# nrw-rent-student-analysis
Analyse der Mietpreise und Studierendenzahlen in NRW


# Fragestellung
Gibt es einen Zusammenhang zwischen dem Anteil der Studierenden an der Bevölkerung und den Mietpreisen in großen Städten in Nordrhein-Westfalen?

# Untersuchte Städte
Köln, Düsseldorf, Dortmund, Bochum, Aachen sowie Duisburg und Essen. Duisburg und Essen wurden zu einer Einheit „Duisburg-Essen“ zusammengefasst, weil die Studierenden der Universität Duisburg-Essen nicht auf die beiden Städte aufgeteilt werden konnten.

# Daten
- **Mietangebote:** Kaggle-Datensatz „Apartment rental offers in Germany“ (Angebote von ImmoScout24). Zeitraum: September 2018 bis Februar 2020 (Erhebungen im Sep 2018, Mai 2019, Okt 2019 und Feb 2020).
- **Studierende:** IT.NRW, Wintersemester 2020/21. Berücksichtigt wurden staatliche Universitäten, staatliche Fachhochschulen/Hochschulen sowie Kunst- und Musikhochschulen. Private und mehrstandortige Anbieter wurden nicht berücksichtigt.
- **Einwohnerzahlen:** Stand 31.12.2018.

## Vorgehen
1. Filterung der Angebote auf NRW und die ausgewählten Städte
2. Datenbereinigung: Kaltmiete zwischen 100 und 4.000 €, Wohnfläche zwischen 10 und 250 m². Dadurch wurden 76 von 21.326 Angeboten (ca. 0,4 %) entfernt.
3. Berechnung der Kaltmiete pro m² und des Medians pro Stadt
4. Berechnung der Studierenden pro 1.000 Einwohner
5. Korrelationsanalyse (Pearson und Spearman)

Verwendete Werkzeuge: Python, pandas, matplotlib

# Ergebnisse
- In der Einzelauswertung der Städte hat Köln den höchsten Median der Kaltmiete (ca. 12,57 €/m²), Duisburg den niedrigsten (ca. 6,02 €/m²).
- Zwischen Studierendenanteil und Miete pro m² ist kein klarer Zusammenhang erkennbar (Pearson: −0,31; Spearman: −0,03).

# Einschränkungen
- Es gibt nur 6 Datenpunkte, daher ist das Ergebnis nur ein Hinweis auf eine Tendenz und kein Beweis.
- Es handelt sich um Angebotsmieten, nicht um tatsächlich gezahlte Mieten.
- Die Daten stammen aus unterschiedlichen Zeiträumen (Mieten 2018–2020, Studierende WS 2020/21, Einwohner 2018).
- Die Studierenden werden nach dem Sitz der Hochschule gezählt, nicht nach dem Wohnort.
- Korrelation bedeutet nicht Kausalität.

# Projektstruktur
- `notebooks/analysis.ipynb`: Analyse
- `data/`: Der Datensatz ist aus Platzgründen nicht im Repository enthalten (ca. 285 MB). Er kann auf Kaggle heruntergeladen werden.
