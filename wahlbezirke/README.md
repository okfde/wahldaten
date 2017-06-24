# Wahlbezirke

Ein Wahlbezirk (oder auch Stimmbezirk genannt) ist die kleinste organisatorische (meist auch geografische) Einheit der Wahl. [Wikipedia: Wahlbezirk](https://de.wikipedia.org/wiki/Wahlbezirk), [Bundestag-Glossar: Wahlbezirk](https://www.bundestag.de/service/glossar/glossar/W/wahlbezirk/246356)

Sie existieren auf kommunaler Ebene für die verschiedenen Wahlen, und die Einteilung ist Sache der jeweiligen Kommune (manchmal auch Gemeindeverbände?).  – *nochmal genauer checken.*

Die Wahlbezirke sind die kleinstmögliche Auflösung bei der Abbildung des Wahlverhaltens, da sie i.d.R. nicht mehr als 2500 Wahlberechtigte umfassen. Und daher für detaillierte Analysen möglicherweise sehr interessant.

## Datenlage

**TODO**: Nochmal bei Ländern und Kreisen nachfragen, ob das wirklich so aussichtslos ist.

Es gibt keine Daten dazu auf Landesebene, es verbleibt bei den Kommunen. Die geben nur aggregierte Ergebnisse weiter.

Kommunen sind aber verpflichtet(??), die Ergebnisse auf Wahlbezirksebene zu veröffentlichen. Da könnte man die Daten herbekommen.

**Geo-Daten** dazu wird es höchstwahrscheinlich, sicherlich mit ein paar Ausnahmen, dazu NICHT geben. In den meisten Ergebnis-Veröffentlichungen der einzelnen Gemeinden sind allerdings Adressen für die einzelnen Wahlbezirke (das ist dann das Wahllokal) angegeben.

### Was kann man tun?

Die Veröffentlichungen der einzelnen Kommunen zusammenscrapen. So gelangt man sowohl an die generellen Meta-Daten der Wahlbezirke sowie auch zu den Einzelergebnissen.

Viele Kommunen nutzen für die Veröffentlichung ihrer Wahlbezirks-Ergebnisse Software von IT-Anbietern, sodass mit Scrapern für diese Plattformen ein Großteil der Daten zu bekommen wäre.

#### Beispiele

**[votemanager](http://wahlen.votemanager.de/)**

Diese Plattform verwenden wohl 1140 Kommunen. Auf den einzelnen Unterseiten pro Gemeinde oder Kreis gibt es sogar CSV-Dateien zum Download – [Beispiel](http://wahlen.regioit.de/AC/LW17/05334002/html5/MedienvertreterInfo.html)

**[PC Wahl](http://www.wahl.mobi/)**

Eine JS-basierte Webapp, die in zwei Versionen vorkommt. Aktueller scheint [das hier](http://www.wahl.mobi/) zu sein, viele Kommunen verwenden eine vorherige, [das sieht dann so aus](https://wahlen.digistadtdo.de/wahlergebnisse/index.html)

Damit könnte man geschätzt 1000-2000 weitere Gemeinden abdecken.

**[Wahlergebnispräsentation (WEP)](http://wahl.krzn.de/wahl2017/)**

Bietet das *Kommunale Rechenzentrum Niederrhein* für die dortigen Gemeinden und Kreise an. **TODO** müsste man schauen, wo es das oder vergleichbare Systeme noch gibt.

**usw.**

[Ein besonderer Leckerbissen, der auch sehr verbreitet scheint](http://www.hamm.de/apps/PCWahl/java/L2017_Zweit/index.html)

Das sind nur Beispiele, die zeigen: Die Daten gibt es irgendwo, nur nicht 1.) zentralisiert und 2.) in einheitlichem, maschinenlesbaren Format.

### Let's scrape

**Zunächst** wie gesagt noch einmal checken, ob die Lage wirklich so grausam ist, wie oben beschrieben, oder ob nicht doch Länder oder es zumindest auf Kreisebene evtl. Daten gibt.

#### 1. Sammlung der Quellen

Welche Kommune veröffentlicht wo (URL) ihre Ergebnisse auf Wahlbezirks-Ebene? Ein Anfang ist diese Liste, die auf den Daten basiert, die in der Software [votemanager](http://wahlen.votemanager.de/) hinterlegt sind.

[Liste der URLs, unter denen Kommunen ihre Ergebnisse auf Wahlbezirksebene veröffentlichen](./data/quellen_wahlbezirke.csv)
