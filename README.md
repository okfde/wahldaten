# Wahldaten-Repo

*Dieses ReadMe ist der erste sehr chaotische Versuch, die Daten von allen möglichen Event-Etherpads und Besprechungen zusammenzutragen und zu kategorisieren.* **Füge sehr, sehr gerne Links, Kategorisierungen, Fragen oder Dokumente dazu, wenn du mehr Infos hast.**


## Intro 
Im Jahr 2017 stehen Bundestagswahlen an, außerdem Landtagswahlen im Saarland, in Schleswig-Holstein und in Nordrhein-Westfalen.
Wir (die Open Knowledge Foundation, das Team und die Community) wollen uns daher verstärkt mit dem Thema Wahlen auseinandersetzen. Aus einer Open-Data und Civic-Tech-Sicht bringen vor allem die Aufbereitung von Informationen im Vornherein als auch die Analyse von Wahlergebnissen im Nachhinein spannende Aufgaben, Möglichkeiten und Herausforderungen mit sich. 



## Ziel dieses Repos

**Das Hauptziel dieses Github Repos ist es, hilfreiche Daten für die Bundestagswahl 2017 zu sammeln**. Um das Ganze etwas abzurunden, findet man in diesem ReadMe auch Termine von Community Events, Beispiele von nationalen und internationalen Wahlprojekten und Projektideen. 


### Was kann ich tun?

1. **Wahlbezogene Daten** direkt in dieses **Github Repo** packen. Jeder Ordner sollte seine eigene ReadMe-Datei haben. Alternativ können auch Wahlbezogene Daten in **Wikidata** eintragen und dann in diesem Github verlinkt werden. Mehr Infos [hier](https://pad.okfn.org/p/wikidata-abg).
2. Datenbestände zum Thema Bundestagswahlen als feine **Linkliste** zusammentragen.
3. **Werkzeuge** zusammentragen, mit denen man die Daten bearbeiten kann.
4. Forderungen an die **Politik** (Statistische Landesämter, Bundeswahlleiter) formulieren, damit wir mehr Daten bekommen


# 1. Wahldaten 

## Wahlen 101
*Eine wichtige Info fehlt? Füge sie hinzu!*

- “Chef" der Wahlen ist der Bundeswahlleiter (https://www.bundeswahlleiter.de/bundestagswahlen/2017.html)
- Deutschland ist in 299 Wahlkreise eingeteilt (https://www.bundeswahlleiter.de/bundestagswahlen/2017/wahlkreiseinteilung.html). Die Einteilung in Wahlkreise ist per Bundesgesetz geregelt. Die Wahlkreise beschränken sich dabei jeweils auf ein Bundesland. 
- Die Wahlkreise sind ihrerseits in Wahlbezirke unterteilt. Die Unterteilung in Wahlbezirke übernehmen wohl die Kommunen. Jeder Wahlbezirk hat genau ein Wahllokal in dem abgestimmt wird (und umgekehrt).
- Jeder Wahlberechtige gehört zu einem Wahlbezirk / Wahllokal, diese Zugehörigkeit kann man auf Antrag per Wahlschein ändern (anderes Wahllokal, Briefwahl).
- Zusätzlich zum Bundeswahlleiter gibt es auch noch Landes- und Kreiswahlleiter (https://www.bundeswahlleiter.de/dam/jcr/7398911f-955d-41f2-9e58-21f4270a54eb/btw17_verzeichnis-kwl-lwl.pdf)
- Für die Briefwahlen werden die Wahlkreise in Briefwahlbezirke unterteilt
- Die Wahlbezirke und die Briefwahlbezirke können, müssen aber nicht übereinstimmen


## Welche Daten wollen wir? 

Welche möglichen Daten es geben kann, steht im [**Election Data Guide**](http://www.openelectiondata.net/en/guide/).

Hier werden nur ein paar gelistet. Die Liste kann gerne in dieser Übersicht erweitert werden: https://docs.google.com/spreadsheets/d/1SWYVMkxMzHoicGOI68SYbPlE7SCscnrSCC8akDZHt0A/edit#gid=0 

Beispiele:

* Wahlkreise
	* Geometrie (Polygone)
	* Parteien die zur Wahl stehen (Zweitstimme)
	* Direktkandidaten 
	* Briefwahlergebnisse
* Wahlbezirke
	* Geometrie (Polygone)
	* Adresslisten: Zuordnung von Adressen zu Wahlbezirken
	* Wahllokal-Adresse
	* Ergebnisse
		* Erst- und Zweitstimmen (absolute Zahlen)
		* Hochrechnungen, vorläufiges / endgültiges Ergebnis
		* Anzahl Wahlberechtigter, Wahlbeteiligung
		* Zahl der gültigen und ungültigen Erst- und Zweitstimmen
		* Zahl der Wahlscheine / Briefwähler

Diese Daten sind nicht nur für die Bundestagswahl 2017 interessant sondern auch für
- vergangene Bundestagswahlen (insb. 2013)
- vergangene "andere" Wahlen (Kommunal-, Landtags-, EU-Wahlen)

Um Wahlergebnisse in ihrem lokalen Kontext zu interpretieren sind entsprechende demografische Daten wichtig:
- Altersstruktur
- Geschlechterverhältnis
- Migranten
- Sozialstruktur (z.B. Empfänger von Sozialleistungen)
- …

Diese Daten liegen unter Umständen nicht auf Wahlbezirksebene vor (sondern z.B. auf Stadtteil-Ebene) und müssen dann umgerechnet werden (siehe Abschnitt "Werkzeuge”). 



# 2. Linkliste
*Diese Liste muss unbedingt besser kategorisiert werden und kann noch mit vielen weiteren Link-Leckerbissen gefüllt werden.*

## Basisdaten

Die Bundestagswahldaten 2013 liegen als offene PDFs und CSVs vor, unter einer freien Lizenz. 
In Berlin scheinen die Daten auf Wahllokalebene vorzuliegen, budnesweit sind nur Wahlbezirke mit sehr großen Mengen von Wählerinnen aufgeführt. (STIMMT DAS?)

- [Index der OKI zum Stand der Wahldaten in Schland](http://index.okfn.org/dataset/elections/): Alles rot derzeit, vermute, weil die Daten nicht auf Wahllokal-Ebene vorliegen (NDI Open Election Data Principle)
- Excel-Tabelle von Ergebnissen früherer Bundestagswahlen in einer IFG-Anfrage: https://fragdenstaat.de/anfrage/iwg-antrag-ergebnisse-fruherer-bundestagswahlen/ (ins Repo packen?) 
- [Abgeordenetenlisten von allen Bundesländern](https://pad.okfn.org/p/wikidata-abg)
- Verzeichnis der Landes-/Kreiswahlleiter https://www.bundeswahlleiter.de/dam/jcr/7398911f-955d-41f2-9e58-21f4270a54eb/btw17_verzeichnis-kwl-lwl.pdf
https://github.com/berlinermorgenpost/cogran

## Misc
- Open Election Data Principles des NDI: http://www.openelectiondata.net/en/guide/
- Bundeswahlgesetz:http://www.gesetze-im-internet.de/bundesrecht/bwahlg/gesamt.pdf 

## Wissenschaftliche Datenressourcen zu Wahlen, u.a.:
- http://www.globalelectionsdatabase.com/
- http://www.electiondataarchive.org/
- http://www.gesis.org/wahlen/wahlen-home/
- http://www.cses.org/

## Wahlmodelle

“**Modelle**”
- https://signalundrauschen.de/ - [Model auf Github](https://github.com/aleininger/sur)
- https://pollytix.de/wahltrend/
- http://pollyvote.com/de/
- http://zweitstimme.org/
- https://www.inwt-statistics.de/blog-artikel-lesen/wahlprognose-fuer-die-bundestagswahl-2017.html
- http://www.election.de/cgi-bin/news1.pl - Erststimmenprognosen

“**Umfragedaten**"
- http://wahlrecht.de/
- https://neuwal.com/ (Österreich)
- https://www.wahlumfragen.org/
- wahlumfrage.de
- http://bundestagswahl.me/

**Wie Medien über Umfragen berichten**
- https://www.nzz.ch/international/deutschland-im-wahljahr/methodik-statistik-wie-die-nzz-umfragen-zur-bundestagswahl-darstellt-und-warum-ld.148951
- http://www.sueddeutsche.de/politik/bundestagswahl-wie-wir-ueber-umfragen-berichten-1.3440233

**Vorhersagen von Medien zur Bundestagswahl**
- https://www.nzz.ch/international/deutschland-im-wahljahr/bundestagswahl-der-aktuelle-stand-der-umfragen-im-ueberblick-union-spd-afd-linke-gruene-fdp-ld.146646

**Literatur**
- https://www.nomos-elibrary.de/10.5771/0340-1758-2015-4-675/wissenschaftliche-wahlprognosen-alternative-oder-ergaenzung-zu-umfragen-jahrgang-46-2015-heft-4 (gated :-()

**Umfrage-Institute**
- https://www.forsa.de/
- http://www.infratest-dimap.de/
- http://www.forschungsgruppe.de/Startseite/
- http://www.ifd-allensbach.de/
- https://www.tns-emnid.com/
- http://www.insa-meinungstrend.de/
- http://www.gms-gmbh.com/index.php/en/
- https://civey.com/
- https://dbk.gesis.org/dbksearch/index2.asp?db=d

**Umfrage-Scraper für wahlrecht.de**

- JavaScript: https://github.com/juliuste/wahlrecht
- Python: https://github.com/stefanw/wahlrecht
- R: https://github.com/aleininger/sur

**Umfragen-Bias**

- https://www.vis4.net/blog/posts/analyzing-bias-in-election-polls-with-r/

**IT-infrastrukturanbieter für Wahlen**

- https://vote-it.de/
- http://www.voteplus.de/



# 3. Werkzeuge

## Was für Werkzeuge gibt es schon? 
- Tool zum Umrechnen von statistischen Daten auf andere Geometrien (z.B. von Stadtteilen auf Wahlbezirke): https://github.com/berlinermorgenpost/cogran Arbeitet wohl nur auf Basis der Flächenüberschneidung der Polygone, könnte man auch auf Basis von Gebäuden machen um die Genauigkeit zu erhöhen

## Was für Werkzeuge brauchen wir noch? 
- Wahllokalfinder: Von Adresse oder Location per UI / API zum Wahllokal
- Visualisierungstoolkit: Grundbausteine für das einfache Erstellen interaktiver Diagramme für einzelne Wahlkreise, Bundesländer, etc.



# 4. Forderungen an die Politik

Wie tragen wir es in die Politik?
Input zum deutschen OGP Aktionsplan - ab Januar wird er erstellt und es wird auch eine öffentliche Konsultation geben (Beispiel UK hat auch was zu Wahldaten drin ) 

Dafür Erfahrungen bei der Arbeit an den Wahldaten sammeln: Welche Ansprüche haben wir an Wahldaten, um damit arbeiten zu können?
Kurzfristige und langfristige Forderungen an die Politik
- kurzfristig: z.B. Alle Daten an einem Ort (realistisch sein)
- langfristig: z.B. detaillierte Daten


## Fragen an den Bundeswahlleiter
- Welche Daten zu den Direktkandidaten werden einheitlich erhoben (z.B. Name, Alter, Beruf, Partei)?
- Wie ist der Informationsfluss am Wahltag organisiert, also wie kommen die Ergebnisse, Hochrechnungen, etc. zum BWL?
Sammelt der BWL alle Daten oder z.B. nur aggregiert auf Wahlkreis-Ebene?
- Wo bekommen wir welche Daten her?
- Welche Daten werden zu Vorfällen / Abweichungen / Unregelmäßigkeiten erhoben?
- Gibt es [diese Daten](https://docs.google.com/spreadsheets/d/1SWYVMkxMzHoicGOI68SYbPlE7SCscnrSCC8akDZHt0A/edit#gid=0)? (Google Spreadsheet) 


## Sind Daten des Bundeswahlleiters per IWG anfragbar?

- Erste Anfrage (laufend): https://fragdenstaat.de/a/17675/auth/73c3ffe0ad611550f31465271399fe47b2fb55ef/
- Projekt: Bundeswahlleiter sagt, er sei nicht dem IFG unterworfen. Schoch (2016) sieht das anders. Gerichtliche Klärung?
- Gescheiterter IFG-Versuch: https://fragdenstaat.de/anfrage/stellungnahmen-zur-europawahl-2014/
- Neuer IFG-Versuch (laufend): https://fragdenstaat.de/anfrage/dokumente-zur-europawahl-2014/?anfrage-gestellt

## Idee: Info-Material für Behörden
- Was sind offene Wahldaten?
- Was wollen wir damit machen?
- Warum ist das gut?
- Welche schönen Beispiele gibt es dafür schon?




# 5. Projektideen
(Hauptsächlich von [hier](https://pad.okfn.de/p/%F0%9F%90%8Ben2017).) Füge mehr hinzu, wenn du magst!
    
- **Was zählt meine Stimme**? Abhängig vom Wohnort soll ein potenzieller (Meine Stimme /Anzahl Wahlberichtigter im Wahlkreis) sowie ein wahrscheinlicher Impact-Faktor (meine Stimme /tatsächliche absolute Wahlbeteiligung) berechnet werden. Die Ausgabe wäre eine natürliche Zahl als Indikator in welchen Wahlkreisen meine Stimme besonders wichtig ist.
- Wahlprüfsteine 
- **Vergleich** Landtag, EU, Kommunen
- Demografie
- Wahldatentransperenz
- **Vorfälle**
- **Nichtwähler**
- **Wahlversprechen** Tracker
- Bundeswahlleiter.onion
- Mediale Unterstützung: Kann man sehen, welche Zeitungen/**Medien** wie nah an bestimmten Parteien stehen und sie durch Berichterstattung pushen? Gibts es evtl. Themen (Wohnungsbau), die bestimmte Medien besonders gern in Wahlzeiten thematisieren? (Bei der Berlinwahl wurde die Flüchtlingskrise für alles verantwortlich gemacht)
- **Direktmandate** zu BTW: Wo ist das Potenzial der AfD? 
- Veränderung der Stimmbezirk- und **Wahlkreiszuschneidung** nachvollziehen
- Wo werden **Wahlplakate** aufgestellt? 
- Wieviel kosten **Wahlkampagnen**? 
- Wer ist eigentlich zur Wahl **zugelassen**? 
- Wie verhalten sich Einkommensverhältnisse zu den Abstimmungen in Wahlbüros?
- Welche **Wahlversprechen** wurden eingelöst, welche nicht? 
- Welche **Forderungen** werden laut und wie stehen diese im Verhältnis zu Zahlen und Fakten?


## Links zu bereits bestehenden Projekten
*sollte irgendwie kategorisiert werden!* 

- Projekte aus anderen Ländern: https://democracyclub.org.uk/data/
- http://wahldatenhelfer.de 
- https://www.propublica.org/article/taking-cues-and-some-projects-from-sunlight-labs
- **Vote.org** – Eine Website aus den USA die Informationen rund um die Wahl einfach und einheitlich aufbereitet und WählerInnen dabei hilft Briefwahl zu beantragen und ein Wahllokal zu finden. Vote.org ist eine NGO die seit kurzem im Y-Combinator Programm supported wird.
- **PolitiFact** – Ein mit dem Publitzer Preis ausgezeichnetes Projekt. PolitiFact ist eine Fakten-Check-Plattform, die den Wahrheitsgehalt von Aussagen von PolitikerInnen prüft.
- **Spiegel Online Wahlprogramm Browser** – Die Anwendung stellt einfach und verständlich mit einem Farbcode dar, wieviel sich Wahlprogramme einem bestimmten Thema widmen. Der Code liegt offen auf github und wurde von Friedrich Lindenberg entwickelt.
- **Wahlversprechen 2013** – Die Seite trackt welche Wahlversprechen bereits eingelöst wurden, welche gebrochen wurden und welche in Kompromissen aufgingen. Die Anwendung stammt aus der Open Knowledge Community und wurde 2013 entwickelt.
- **Election Maps** – Visualisierungen der Wahlergebnisse auf Basis von Bevölkerungsgröße der US Bundesstaaten.
- Wahlprogrammvergleiche von Daniel Kirch: http://codeformuenster.org/wahlprogramm-matrix/
- http://apps.lokaler.de/meinungsmaschine/ 
- http://rocknpoll.graphics/  - Schöne Visualisierung und Data Literacy zu Umfragen:
- Aus dem OK Lab Berlin: http://codefor.de/projekte/2014-04-22-be-wahlversprechen
- https://interaktiv.morgenpost.de/wo-deutschland-rechts-waehlt/
- https://interaktiv.morgenpost.de/koalitionsvertrag-berlin-2016/
- https://interaktiv.morgenpost.de/abgeordnete-in-berlin/
- http://interaktiv.morgenpost.de/wahlsieg-formel-berlin/
- Berlin-Wahl 2016: http://berlinwahlkarte2016.morgenpost.de/
- Europa-Wahl 2014: http://interaktiv.morgenpost.de/europawahlkarte-berlin/
- Bundestags-Wahl 2013: http://berlinwahlkarte2013.morgenpost.de/
- Berlin-Wahl 2011: http://www.morgenpost.de/berlin-aktuell/article105107410/Ergebnisse-der-Berliner-Abgeordnetenhauswahl-2011.html
- http://interaktiv.morgenpost.de/waehlerwanderung-berlin-2016/
- http://interaktiv.morgenpost.de/waehlernaehe-berlin/
- http://www.morgenpost.de/politik/article124923347/Warum-Abgeordnete-ihr-Bundestagsmandat-niederlegen.html?config=interactive
- http://www.morgenpost.de/politik/bundestagswahl/article117631717/Interaktiver-Stimmzettel-Wen-Sie-waehlen-koennen.html?config=interactive
- http://www.morgenpost.de/politik/bundestagswahl/article119332220/TV-Duell-Die-Gesten-von-Merkel-und-Steinbrueck.html?config=interactive





# 6. Termine 
Pad mit allen aktuellen Terminen für Community Events in Deutschland, die sich mit Wahldaten beschäftigen: [https://pad.okfn.de/p/wahldaten-termine](https://pad.okfn.de/p/wahldaten-termine)

- 10.April, 19.00 Uhr: OK Lab Wahldaten-Vortreffen zum Datensummit
- 28./29.04: [Datensummit](https://datensummit.de) in Berlin 
- 03.05: [Jenseits der Glaskugel: Wissenschaftliche Vorhersagen zur Bundestagswahl 2017](https://www.hertie-school.org/en/jenseits-der-glaskugel/), Berlin
- 07.05. Schleswig-Holstein-Wahl 
- 15.05. Nordrhein-Westfalen-Wahl 
- 26.05.: [Wahlsalon in Berlin](https://codefor.de/wahlsalon)
- Anfang Juli: Wahlsalon 2 in Köln oder Frankfurt 
- 23.06. - 25.06.2017: [Wikidata Workshop in Ulm](https://de.wikipedia.org/wiki/Wikipedia:Wikidata-Wahldaten-Workshop)
- 06.09. - 09.09.2017: [Campfire Festival](http://campfirefestival.org/)




## 7. Quellen
Fast der komplette Inhalt aus folgenden Pads wurde in dieses Read-Me übertragen. Wenn ich etwas Wichtigstes vergessen haben sollte, trage es bitte nach!

- https://pad.okfn.de/p/%F0%9F%90%8Ben2017
- https://pad.okfn.de/p/wahldaten
- https://pad.okfn.de/p/wahlmodelle
- https://pad.okfn.de/p/wahldatentransparenz
- https://pad.okfn.org/p/wikidata-abg


