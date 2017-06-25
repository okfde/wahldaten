# Wahlbezirke

Ein Wahlbezirk (oder auch Stimmbezirk genannt) ist die kleinste organisatorische (meist auch geografische) Einheit der Wahl. Aus dem [Bundestag-Glossar: Wahlbezirk](https://www.bundestag.de/service/glossar/glossar/W/wahlbezirk/246356) (via [Wikipedia: Wahlbezirk](https://de.wikipedia.org/wiki/Wahlbezirk)):

> Jeder Wahlkreis wird noch einmal in Wahlbezirke, auch Stimmbezirke genannt, unterteilt, um das Wählen einfacher zu gestalten.
>
> Dabei sollen grundsätzlich nicht mehr als 2500 Wahlberechtigte in einem Wahlbezirk sein. Kleinere Gemeinden bilden i. d. R. einen Wahlbezirk, größere werden aufgeteilt.
>
> Kein Wahlbezirk darf so klein sein, daß erkennbar wird, wie einzelne Wahlberechtigte gewählt haben.

Sie existieren auf kommunaler Ebene, werden für die verschiedenen Wahltypen (Kommunal, Landtag, Bundestag, etc.) genutzt und ihre Einteilung ist Sache der jeweiligen Kommune.

* [ ] manchmal auch Gemeindeverbände? *nochmal genauer checken.*

Die Wahlbezirke sind die kleinstmögliche Auflösung in der Abbildung des Wahlverhaltens, da sie i.d.R. nicht mehr als 2500 Wahlberechtigte umfassen. Daher sind sie für detaillierte Analysen sehr interessant.

## Datenlage

Es gibt keine Daten zu Wahlbezirken auf Bundes- noch Landesebene. Diese verbleiben bei den Kommunen, welche  nur die aggregierten Ergebnisse auf Wahlkreiseben weitergeben.

Kommunen sind jedoch verpflichtet (?) die Ergebnisse auf Wahlbezirksebene zu veröffentlichen. Dort ließen sich die Daten herbekommen.

* [ ] **TODO**: Nochmal bei Ländern und Kreisen nachfragen, ob das wirklich so aussichtslos ist.

Zugehörige **Geo-Daten** existieren, mit wenigen zu findenden Ausnahmen, zumeist nicht.
In den meisten Ergebnisveröffentlichungen der einzelnen Gemeinden sind allerdings Adressen für die einzelnen Wahlbezirke, d.h. die Wahllokale, angegeben.

### Was lässt sich tun?

Die Veröffentlichungen der einzelnen Kommunen können zusammengescrapet werden. So ließen sich die generellen Metadaten der Wahlbezirke sowie deren Einzelergebnisse erhalten.

Viele Kommunen nutzen für die Veröffentlichung ihrer Wahlbezirksergebnisse Software von einigen wenigen IT-Anbietern, sodass mit Scrapern für diese Plattformen ein Großteil der Daten zu bekommen wäre.

#### Beispiele

* **[votemanager](http://wahlen.votemanager.de/)**
Diese Plattform der vote iT GmbH aus Aachen/Gütersloh verwenden ca. 1140 Kommunen. Auf den einzelnen Unterseiten pro Gemeinde oder Kreis gibt es CSV-Dateien zum Download – [Beispiel](http://wahlen.regioit.de/AC/LW17/05334002/html5/MedienvertreterInfo.html)
* **[PC Wahl](http://www.wahl.mobi/)**
Eine JS-basierte Webapp von der selbsen Firma wie oben, die in zwei Versionen vorkommt. Aktueller scheint [das hier](http://www.wahl.mobi/) zu sein, viele Kommunen verwenden eine vorherige, [das sieht dann so aus](https://wahlen.digistadtdo.de/wahlergebnisse/index.html)
Damit könnte man geschätzt 1000-2000 weitere Gemeinden abdecken.
* **[Wahlergebnispräsentation (WEP)](http://wahl.krzn.de/wahl2017/)**
Bietet das *Kommunale Rechenzentrum Niederrhein* für die dortigen Gemeinden und Kreise an. **TODO** müsste man schauen, wo es das oder vergleichbare Systeme noch gibt.
* **[OK.WAHL](https://www.akdb.de/loesungen/okbuergerservice/okwahl/uebersicht/)** von der Anstalt für Kommunale Datenverarbeitung in Bayern (AKDB) – Beispielexporte: http://wahlen.landkreis-dillingen.de/bundestag/2013/EE/773000_000026/0007731250001.html?Gemeinde=0007731250000.html&Wahlbezirk=0007731250001.html 
* **usw.**

[Ein besonderer Leckerbissen, der auch sehr verbreitet scheint](http://www.hamm.de/apps/PCWahl/java/L2017_Zweit/index.html)

Das sind nur einige Beispiele, die zeigen, dass es die Daten irgendwo gibt, nur nicht

1. zentralisiert und
2. in einheitlichem, maschinenlesbaren Format.

### Let's scrape

**Zunächst** wie gesagt noch einmal checken, ob die Lage wirklich so grausam ist, wie oben beschrieben, oder ob nicht doch Länder oder es zumindest auf Kreisebene evtl. Daten gibt.

#### 1. Sammlung der Quellen

Welche Kommune veröffentlicht wo (URL) ihre Ergebnisse auf Wahlbezirks-Ebene? Ein Anfang ist die folgende Liste, welche auf den mit der Software [votemanager](http://wahlen.votemanager.de/) hinterlegten Daten basiert.

[Liste der URLs, unter denen Kommunen ihre Ergebnisse auf Wahlbezirksebene veröffentlichen](./data/quellen_wahlbezirke.csv)
