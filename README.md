# Was ist mit der Musik passiert?

## Eine datenbasierte Analyse des kulturellen Wandels populärer Musik durch technologische Entwicklungen

Musik begleitet unser Leben. Viele Menschen haben das Gefühl, daß sie sich verändert hat - Songs wirken kürzer, Genres verschwimmen, bekannte Weltstars scheinen seltener zu werden und alte Hits kehren als Cover zurück.


**Aber stimmt dieses Gefühl überhaupt?**

**Oder täuscht uns die Nostalgie?**

Dieses Projekt versucht, diese Frage datenbasiert zu beantworten.

---

## Die Fragestellung

Im Mittelpunkt steht die Entwicklung populärer Musik anhand der britischen
Single-Charts.

Besonders untersucht werden dabei **NEW-Entries** – Songs, die erstmals
in die Charts einsteigen – und **RE-Entries** – Songs, die nach einer
Unterbrechung wieder in den Charts erscheinen.

Die Analyse betrachtet insbesondere:

- die Entwicklung von NEW- und RE-Entries über die Zeit
- saisonale Muster
- Veränderungen im Chart-Verhalten
- Entwicklungen auf Künstler- und Song-Ebene
- den zeitlichen Zusammenhang mit technologischen Veränderungen der
  Musikdistribution

Dabei geht es zunächst darum, **Muster sichtbar zu machen und daraus
Hypothesen zu entwickeln**. Ein zeitlicher Zusammenhang wird dabei nicht
automatisch als kausaler Zusammenhang interpretiert.

---

## Datenbasis

Als Arbeitsdatensatz dient ein auf Kaggle veröffentlichter Datensatz,
der aus Daten der **Official Charts Company** zusammengestellt wurde.

Der Datensatz beginnt 1952. Für die Analyse wird der Zeitraum **ab
Januar 1983** betrachtet, da ab diesem Zeitpunkt ein konsistentes
wöchentliches Top-100-Format vorliegt.

Die Top 100 bilden damit die zentrale Untersuchungsgrundlage des
Projekts.

---

## Datenaufbereitung

Die Rohdaten werden nicht verändert. Für die Analysen wurde eine separate
bereinigte Chart-Historie erstellt.

Die Aufbereitung umfasst unter anderem:

- Prüfung der wöchentlichen Chartlängen
- Entfernung exakter Duplikate
- Prüfung auf doppelte bzw. widersprüchliche Einträge
- Erstellung von Song- und Künstlerdaten
- Aggregation von Chartstatistiken
- Identifikation von NEW- und RE-Entries
- zeitliche und saisonale Aufbereitung

---

## Datenqualität

Bei der Validierung der Daten zeigte sich, dass nicht jede historische
Chartwoche vollständig mit 100 Einträgen vorliegt.

Nach der Bereinigung enthielten 1.939 von 2.146 untersuchten Wochen die
vollständigen Top 100. Die übrigen Wochen enthielten zwischen 74 und 99
Einträge.

Zusätzlich wurden drei einzelne fehlende Positionen innerhalb der
Top-50-Daten identifiziert und dokumentiert.

Die vorhandenen Daten wurden für die Analyse beibehalten; fehlende
Positionen wurden nicht künstlich ergänzt.

---

## Technologischer Kontext

Die zeitliche Entwicklung der Chartdaten wird vor dem Hintergrund des
Wandels der Musikdistribution betrachtet:

**Radio → Internet → Downloads → Streaming**

Dabei dient der technologische Wandel als Kontext für beobachtete
Veränderungen in den Chartdaten. Die Analyse untersucht zeitliche
Zusammenhänge, ohne daraus unmittelbar Kausalität abzuleiten.

---

## Weiterführende Fragen

Die Analyse eröffnet weitere Fragestellungen, die mit zusätzlichen
Analysen oder Datensätzen untersucht werden könnten:

- Wie verändert sich die Chart-Verweildauer über die Jahre?
- Wie entwickeln sich Songs innerhalb der Top 10 bzw. Top 50?
- Wie verändert sich das Verhalten verschiedener Genres?
- Welche Rolle spielt das Veröffentlichungsjahr eines Songs?
- Welche Zusammenhänge bestehen zwischen technologischem Wandel und
  Chart-Verhalten?

---

## Projektstruktur

Die einzelnen Arbeitsschritte von der Datenaufbereitung über die
explorative Analyse bis zur Visualisierung sind in den Notebooks und
Methodendokumenten dieses Repositories nachvollziehbar.

Die detaillierte Vorgehensweise ist in
[`methodology.md`](methodology.md) dokumentiert.
