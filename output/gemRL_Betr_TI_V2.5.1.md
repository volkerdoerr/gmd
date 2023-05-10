
Elektronische Gesundheitskarte und Telematikinfrastruktur

### Übergreifende Richtlinien zum Betrieb der TI

- Klassifizierung: öffentlich
- Referenzierung: gemRL_Betr_TI
- Revision: 548770
- Stand: 19.02.2021
- Status: freigegeben
- Version: 2.5.1

### Dokumentinformationen

Änderungen zur Vorversion

Anpassungen des vorliegenden Dokumentes im Vergleich zur Vorversion können Sie
der nachfolgenden Tabelle entnehmen.

Dokumentenhistorie

<table><tr><th>
Version

</th><th>
Stand

</th><th>
Kap./ Seite

</th><th>
Grund der Änderung, besondere Hinweise

</th><th>
Bearbeiter

</th></tr><tr><td>
</td><td>
</td><td>
</td><td>
Vollständige Überarbeitung gemäß C_6410 und C_6411

</td><td>
</td></tr><tr><td>
2.0.0

</td><td>
14.05.18

</td><td>
</td><td>
freigegeben

</td><td>
gematik

</td></tr><tr><td>
2.0.1

</td><td>
24.08.18

</td><td>
</td><td>
Korrektur der Übertragung der bekannten Änderung (redaktionell)

</td><td>
gematik

</td></tr><tr><td>
2.1.0

</td><td>
15.05.19

</td><td>
</td><td>
Einarbeitung Änderungsliste P18.1

</td><td>
gematik

</td></tr><tr><td>
2.2.0

</td><td>
28.06.19

</td><td>
Einarbeitung Änderungsliste P19.1

</td><td>
gematik

</td></tr><tr><td>
2.3.0

</td><td>
02.10.20

</td><td>
Einarbeitung Änderungsliste P20.1/2

</td><td>
gematik

</td></tr><tr><td>
2.4.0

</td><td>
02.03.20

</td><td>
Einarbeitung Änderungsliste P20.1 

</td><td>
gematik

</td></tr><tr><td>
2.5.0

</td><td>
30.06.20

</td><td>
Anpassungen gemäß Änderungsliste P22.1 und Scope-Themen aus Systemdesign
R4.0.0

</td><td>
gematik

</td></tr><tr><td>
2.5.1

</td><td>
19.02.20

</td><td>
Einarbeitung Änderungsliste P22.5

</td><td>
gematik

</td></tr></table>

### Inhaltsverzeichnis

- [Dokumentinformationen]
- [Inhaltsverzeichnis]
- [1] Einordnung des Dokumentes
  - [1.1] Zielsetzung
  - [1.2] Zielgruppe
  - [1.3] Geltungsbereich
  - [1.4] Abgrenzungen des Dokuments
  - [1.5] Methodik
- [2] Prozessübergreifende Regelungen
  - [2.1] Zentrales TI-ITSM-System
    - [2.1.1] Übergreifendes ITSM der TI
    - [2.1.2] Kommunikation
      - [2.1.2.1] Kommunikation außerhalb des TI-ITSM-Systems
    - [2.1.3] TI-ITSM-Reporting
  - [2.2] ITSM der TI-ITSM-Teilnehmer
    - [2.2.1] Auszüge aus dem Betriebshandbuch der TI-ITSM-Teilnehmer
  - [2.3] Auditierung von TI-ITSM-Teilnehmern
  - [2.4] Zentrale Koordinierung durch den Gesamtverantwortlichen TI
    - [2.4.1] Eskalationen im übergreifenden TI-ITSM
    - [2.4.2] Taskforce als Instrument der Deeskalation im übergreifenden TI-ITSM
- [3] Incident Management
  - [3.1] Begriffsbestimmungen
    - [3.1.1] Übergreifender Incident
  - [3.2] Prozessdurchführung Incident Management
    - [3.2.1] Übergreifenden Incident erfassen und qualifizieren
      - [3.2.1.1] Übergreifenden Incident erfassen
      - [3.2.1.2] Übergreifenden Incident qualifizieren
      - [3.2.1.3] Serviceverantwortung für übergreifenden Incident zuweisen
    - [3.2.2] Serviceverantwortung für übergreifenden Incident prüfen
    - [3.2.3] Lösung für übergreifenden Incident erstellen
    - [3.2.4] Unterstützung für einen übergreifenden Incident einfordern
    - [3.2.5] Lösung für einen übergreifenden Incident prüfen
    - [3.2.6] Übergreifenden Incident schließen
  - [3.3] Abweichungen im Prozessablauf
    - [3.3.1] Übergreifenden Incident eskalieren
    - [3.3.2] Mitwirkung in einer Taskforce
  - [3.4] Verfahren für die Lösung eines Security-Incidents
  - [3.5] Verfahren für die Lösung eines Incidents mit Datenschutzrelevanz
  - [3.6] Verfahren für die Lösung von Notfall-Incidents
- [4] Problem Management
  - [4.1] Begriffsbestimmungen
    - [4.1.1] Übergreifendes Problem
  - [4.2] Prozessdurchführung Problem Management
    - [4.2.1] Übergreifendes Problem erfassen und qualifizieren
      - [4.2.1.1] Übergreifendes Problem erfassen
      - [4.2.1.2] Übergreifendes Problem qualifizieren
      - [4.2.1.3] Serviceverantwortung für übergreifendes Problem zuweisen
    - [4.2.2] Serviceverantwortung für übergreifendes Problem prüfen
    - [4.2.3] Lösung für übergreifendes Problem erstellen
      - [4.2.3.1] Problem Ursachenanalyse durchführen
      - [4.2.3.2] Lösung für übergreifendes Problem entwickeln und implementieren
      - [4.2.3.3] Stornierung oder Abbruch der Bearbeitung eines Problem-Tickets
    - [4.2.4] Lösungsunterstützung für übergreifendes Problem
    - [4.2.5] Lösung für übergreifendes Problem prüfen
    - [4.2.6] Übergreifendes Problem schließen
  - [4.3] Abweichungen im Prozessablauf
    - [4.3.1] Übergreifendes Problem eskalieren
    - [4.3.2] Mitwirkung in einer Taskforce
- [5] Request Fulfillment
  - [5.1] Begriffsbestimmungen
    - [5.1.1] Service Request
    - [5.1.2] Beschwerdemanagement
  - [5.2] Prozessdurchführung Request Fulfillment
    - [5.2.1] Service Request erfassen
    - [5.2.2] Service Request prüfen
    - [5.2.3] Service Request erfüllen
    - [5.2.4] Service Request verifizieren und schließen
- [6] Configuration Management
  - [6.1] Begriffsbestimmungen
    - [6.1.1] Konfigurationselement (Configuration Item, CI)
    - [6.1.2] TI-Konfigurationsdatenbank
    - [6.1.3] TI-Stammdaten
    - [6.1.4] TI-Konfigurationsdaten
    - [6.1.5] Lokale Konfigurationsdaten
  - [6.2] Prozessdurchführung Configuration Management
    - [6.2.1] Schema der TI-Konfigurationsdatenbank pflegen
    - [6.2.2] Konfigurationsdaten pflegen
      - [6.2.2.1] Übermittlung von Konfigurationsdaten nach lokal autorisierten Produkt-Changes
- [7] Change & Release Management
  - [7.1] Begriffsbestimmungen
    - [7.1.1] Request for Change (RfC)
    - [7.1.2] Produkt-Change
      - [7.1.2.1] Master-Change
      - [7.1.2.2] Sub-Change
    - [7.1.3] Produkttyp-Change
    - [7.1.4] Emergency-Change
    - [7.1.5] Betriebliches Change-Bewertungsgremium (BCB)
    - [7.1.6] Change Advisory Board (CAB)
    - [7.1.7] Emergency Change Advisory Board (eCAB)
    - [7.1.8] Post Implementation Review (PIR)
    - [7.1.9] Change- & Release-Kalender
  - [7.2] Prozessdurchführung Change & Release Management
    - [7.2.1] Produkt-Change: Request for Change (RfC) erstellen
    - [7.2.2] Produkt-Change: RfC bewerten
    - [7.2.3] Produkt-Change: RfC genehmigen
    - [7.2.4] Produkt-Change umsetzen
    - [7.2.5] Produkt-Change: Umsetzung verifizieren
    - [7.2.6] Produkt-Change abschließen
  - [7.3] Abweichungen im Prozessablauf
  - [7.4] Verfahren für einen Standard-Change
  - [7.5] Verfahren für einen Emergency-Change
- [8] Knowledge Management
  - [8.1] Begriffsbestimmungen
    - [8.1.1] Wissensdatenbank (WDB) des TI-ITSM-Systems
  - [8.2] Prozessdurchführung Knowledge Management
    - [8.2.1] Wissen identifizieren und übermitteln
- [9] Service Level Management
  - [9.1] Begriffsbestimmungen
    - [9.1.1] Service Level
    - [9.1.2] Service Level Report
  - [9.2] Prozessdurchführung Service Level Management
    - [9.2.1] Messung der Service Level
    - [9.2.2] Bereitstellung des Service Level Reports
    - [9.2.3] Teilnahme am Service Review
- [10] Performance Management
  - [10.1] Begriffsbestimmungen
    - [10.1.1] Performance
  - [10.2] Prozessdurchführung Performance Management
    - [10.2.1] Performance messen
    - [10.2.2] Performance reporten
    - [10.2.3] Performance bewerten, planen und steuern
    - [10.2.4] Service Monitoring (finale Lösung)
- [11] Servicekatalog Management
  - [11.1] Begriffsbestimmungen
    - [11.1.1] Servicekatalog
    - [11.1.2] Serviceverzeichnis
  - [11.2] Prozessdurchführung Servicekatalog Management
    - [11.2.1] Definition der angebotenen Services
    - [11.2.2] Servicekatalog freigeben
- [12] Notfall Management
  - [12.1] Begriffsbestimmungen
    - [12.1.1] Notfall
    - [12.1.2] Lokaler Notfall
    - [12.1.3] TI-Notfall
    - [12.1.4] TI-Notfallvorsorge
    - [12.1.5] TI-Notfallmaßnahme
    - [12.1.6] Notbetrieb
    - [12.1.7] TI-Notfallbewältigung
    - [12.1.8] Emergency Management Committee (EMC)
    - [12.1.9] Lösungsteam
  - [12.2] Prozessdurchführung Notfallvorsorge
    - [12.2.1] Analyse der Auswirkungen möglicher Notfälle der Produktinstanzen
    - [12.2.2] Entwicklung und Pflege der Notfallvorsorgedokumentation
    - [12.2.3] Umsetzung Vorkehrungen zur Notfallvorsorge
  - [12.3] Prozessdurchführung TI-Notfallbewältigung
    - [12.3.1] TI-Notfallerkennung
    - [12.3.2] Eskalation TI-Notfälle
    - [12.3.3] Sofortmaßnahmen TI-Notfälle
    - [12.3.4] Bewältigung TI-Notfälle
    - [12.3.5] Koordination der TI-Notfallbewältigung durch den Gesamtverantwortlichen TI
      - [12.3.5.1] Notfallbeurteilung
      - [12.3.5.2] Notfallfeststellung
      - [12.3.5.3] Einberufung des Emergency Management Committee (EMC)
      - [12.3.5.4] Zusammenstellung des Lösungsteams
      - [12.3.5.5] Durchführung der Notfallmaßnahmen
      - [12.3.5.6] Notfalldeeskalation
    - [12.3.6] Wiederherstellung
    - [12.3.7] Nachbearbeitung/Notfallauswertung
  - [12.4] Informationspflichten
  - [12.5] Dokumentation
    - [12.5.1] TI-Notfall-Logbuch
    - [12.5.2] Wiederherstellungsbericht
- [13] Vorschriften für CSV-Reporting
  - [13.1] Basisfeldtypen von Prozessdaten
- [14] Anhang A – Verzeichnisse
  - [14.1] Abkürzungen
  - [14.2] Glossar
  - [14.3] Abbildungsverzeichnis
  - [14.4] Tabellenverzeichnis
  - [14.5] Referenzierte Dokumente
    - [14.5.1] Dokumente der gematik
    - [14.5.2] Weitere Dokumente

### 1 Einordnung des Dokumentes

### 1.1 Zielsetzung

Die vorliegenden „Übergreifenden Richtlinien zum Betrieb der TI“ definieren
die betrieblichen Mitwirkungspflichten und Schnittstellen zur übergreifenden
Zusammenarbeit der Teilnehmer der Telematikinfrastruktur (TI) im
IT-Servicemanagement (TI-ITSM) auf prozessualer Ebene. Die übergreifenden
Richtlinien gelten für den Betrieb aller Betriebsumgebungen (Referenzumgebung
(RU), Testumgebung (TU), Produktivumgebung (PU)). TI-ITSM-Teilnehmer sind
Anbieter. Die zur Erbringung der TI-Services benötigten Produkte müssen
zugelassen sein.

Eine abschließende Übersicht der TI-ITSM-Teilnehmer findet sich im
Betriebskonzept [gemKPT_Betr#Tab_KPT_Betr_TI_001 TI-ITSM-Teilnehmer].

Hinweis

Anforderungen, die im vorliegenden Dokument definiert sind und sich an eine
Teilmenge der TI-ITSM-Teilnehmerrichten, bspw. an die Anbieter zentraler
Produkte, sind deutlich an diese adressiert.

Die Mitwirkung der gematik am TI-ITSM erfolgt über die
Rolle „Gesamtverantwortlicher TI“.

In dieser Rolle hat die gematik Ergebnisverantwortung für die
TI-ITSM-Betriebsprozesse und nimmt dort folgende Funktionen ein:

 ---> UL

Die Richtlinien treffenkeineVorgaben zu internen ITSM-Prozessen der einzelnen
Teilnehmer der TI.

Folgende Prozesse werden im TI-ITSM betrachtet:

 ---> UL

Die Aufgabenbereiche sind an die IT Infrastructure Library V3 (ITIL® V3)
angelehnt. Alle Aufgabenfelder werden in Form von übergreifenden
IT-Service-Management-Prozessen mit den jeweiligen Aufgaben und Zielen
vorgestellt. Sie orientieren sich an den ITIL-Lebenszyklusphasen des „Service
Design“ zur Erstellung, Weiterentwicklung und Pflege von Vorgaben, der
„Service Transition“ zur Überführung der Vorgaben in den Wirkbetrieb und
der „Service Operation“ in der Unterstützung des Wirkbetriebs der
TI-Services.

### 1.2 Zielgruppe

Das Dokument richtet sich an die bezeichneten TI-ITSM-Teilnehmer.

### 1.3 Geltungsbereich

Dieses Dokument enthält normative Festlegungen zur Telematikinfrastruktur (TI)
des Deutschen Gesundheitswesens. Der Gültigkeitszeitraum der vorliegenden
Version und deren Anwendung in Zulassungsverfahren wird durch die gematik GmbH
in gesonderten Dokumenten (z. B. Dokumentenlandkarte, Anbietertypsteckbrief,
Produkttypsteckbrief, Leistungsbeschreibung) festgelegt und bekannt gegeben.

Schutzrechts-/Patentrechtshinweis

Die nachfolgende Richtlinie ist von der gematik allein unter technischen
Gesichtspunkten erstellt worden. Im Einzelfall kann nicht ausgeschlossen
werden, dass die Implementierung der Richtlinie in technische Schutzrechte
Dritter eingreift. Es ist allein Sache des Anbieters oder Herstellers, durch
geeignete Maßnahmen dafür Sorge zu tragen, dass von ihm aufgrund der
Richtlinie angebotene Produkte und/oder Leistungen nicht gegen Schutzrechte
Dritter verstoßen und sich ggf. die erforderlichen Erlaubnisse/Lizenzen von
den betroffenen Schutzrechtsinhabern einzuholen. Die gematik GmbH übernimmt
insofern keinerlei Gewährleistungen.

### 1.4 Abgrenzungen des Dokuments

Nicht alle ITSM-Prozesse gemäß ITIL® V3 sind im Rahmen dieses
Richtliniendokumentes geregelt. Dies ergibt sich insbesondere

 ---> UL

Aus oben genannten Gründen sind innerhalb dieses Dokumentes folgende
ITSM-Prozessenichtgeregelt:

 ---> UL

Regelungen für Anwender, Versicherte und DVOs (Dienstleister vor Ort) werden
nicht definiert.

### 1.5 Methodik

Anforderungen als Ausdruck normativer Festlegungen werden durch eine eindeutige
ID in eckigen Klammern sowie die dem Request for Change (RFC) 2119 [RFC2119]
entsprechenden, in Großbuchstaben geschriebenen deutschen Schlüsselworte
MUSS, DARF NICHT, SOLL, SOLL NICHT, KANN gekennzeichnet. Sie werden im Dokument
wie folgt dargestellt:

\<AFO-ID\> - \<Titel der Afo\>Text / Beschreibung [\<=]

Dabei umfasst die Anforderung sämtliche innerhalb der Afo-ID und der Textmarke
angeführten Inhalte.

### 2 Prozessübergreifende Regelungen

### 2.1 Zentrales TI-ITSM-System

### 2.1.1 Übergreifendes ITSM der TI

Das ITSM der TI verantwortet die übergreifende Bearbeitung von Vorgängen in
der TI.

Wesentliche Aufgaben sind:

 ---> UL

Es werden keine normativen Vorgaben zu lokalen Prozessen der TI-ITSM-Teilnehmer
gemacht.

Übergreifender Vorgang

Vorgänge sind Auslöser für die in diesen Richtlinien beschriebenen
TI-ITSM-Prozesse.

Ein übergreifender Vorgang liegt vor, wenn

 ---> UL

Alle Informationen, die bei der Bearbeitung eines Vorgangs entstehen, sind
Vorgangsdaten.

### 2.1.2 Kommunikation

Die Kommunikationsschnittstellen und die Ansprechpartner bilden den SPOC (Single
Point of Contact) des jeweiligen TI-ITSM-Teilnehmers im Rahmen der
Prozesskommunikation. Diese Schnittstellen sollen die Erreichbarkeit der
TI-ITSM-Teilnehmer untereinander sicherstellen.

Voraussetzung zur Teilnahme am ITSM der TI ist die Nutzung des zentralen
TI-ITSM-Systems.

**GS-A_4090 - Kommunikationssprache**

Alle TI-ITSM-Teilnehmer MÜSSEN sowohl schriftlich als auch mündlich in
deutscher Sprache kommunizieren. Dies gilt insbesondere für die gemäß
GS-A_4085 festgelegten Kommunikationsschnittstellen und für alle
Dokumentationen. **[\<=]**

**GS-A_3886-01 - Nutzung des TI-ITSM-Systems bei der Übermittlung eines
übergreifenden Vorgangs**

Alle TI-ITSM-Teilnehmer MÜSSEN alle übergreifenden Vorgänge, zwecks
Informationsübermittlung, im TI-ITSM-System erfassen. **[\<=]**

Das TI-ITSM-System vergibt für jeden Vorgang automatisch eine eindeutige
Referenznummer. Die Referenznummer des lokalen ITSM-Systems des
TI-ITSM-Teilnehmers kann mitgeführt werden.

**GS-A_4085 - Etablierung von Kommunikationsschnittstellen durch die
TI-ITSM-Teilnehmer**

Alle TI-ITSM-Teilnehmer MÜSSEN im Rahmen der übergreifenden Betriebsprozesse
mindestens die nachfolgenden Kommunikationsschnittstellen etablieren:

 ---> UL

**[\<=]**

**GS-A_4086 - Erreichbarkeit der Kommunikationsschnittstellen**

Alle TI-ITSM-Teilnehmer MÜSSEN die Kommunikationsschnittstellen während der
festgelegten Servicezeiten erreichbar halten und einer regelmäßigen
Eingangsprüfung und Bearbeitung unterziehen. **[\<=]**

**GS-A_4088 - Benennung von Ansprechpartnern**

TI-ITSM-Teilnehmer MÜSSEN entsprechend ihrer Rolle
(gemKPT_Betr#Tab_KPT_Betr_TI_003 Mitwirkungsverpflichtung im TI-ITSM)
Kontaktdaten im TI-ITSM-System eintragen und aktuell halten für:

 ---> UL

Die hier genannten Ansprechpartner MÜSSEN mit der entsprechenden Fach- und
Entscheidungskompetenz ausgestattet sein. **[\<=]**

Mehrfachnennungen und/oder Nennung eines Ansprechpartners/Funktionspostfachs
für mehrere Bereiche sind möglich.

### 2.1.2.1 Kommunikation außerhalb des TI-ITSM-Systems

Bei Ausfall des TI-ITSM-Systems müssen die TI-ITSM-Teilnehmer die Bearbeitung
der Vorgänge fortsetzen. Die Kommunikation erfolgt dann über die gemäß
GS-A_4088 angegebenen Kommunikationsschnittstellen.

**GS-A_5402 - Eigenverantwortliches Handeln bei Ausfall von
Kommunikationsschnittstellen**

Bei Ausfall des TI-ITSM-Systems oder anderer Kommunikationsschnittstellen MUSS
die Kommunikation durch die TI-ITSM-Teilnehmer eigenverantwortlich
untereinander sichergestellt werden. Vorgänge müssen im TI-ITSM-System
nachdokumentiert werden. **[\<=]**

**GS-A_5401 - Verschlüsselte E-Mail-Kommunikation**

Der Informationsaustausch per E-Mail zwischen allen TI-ITSM-Teilnehmern MUSS
verschlüsselt mittels Secure/Multipurpose Internet Mail Extensions (S/MIME)
erfolgen. Das für diese Kommunikation notwendige Zertifikat MUSS vom
Eigentümer der E-Mail-Adressen selbst beschafft und allen TI-ITSM-Teilnehmern
zur Verfügung gestellt werden. **[\<=]**

Die Zurverfügungstellung der E-Mail-Zertifikate erfolgt durch alle
TI-ITSM-Teilnehmer in der Wissensdatenbank der TI.

Der TI-ITSM-Teilnehmer sollte alle anderen TI-ITSM-Teilnehmer durch den Versand
einer mit seinem Zertifikat signierten E-Mail über dieses Zertifikat
informieren. Wird ein bestehendes Zertifikat ersetzt, sollte diese Information
mindestens zwei Wochen vor dem Ablauf der Gültigkeit des alten Zertifikates
erfolgen.

### 2.1.3 TI-ITSM-Reporting

Informationen zu übergreifenden Vorgängen, wie Vorgangsdaten,
Lösungsdokumentation etc., sind im zentralen TI-ITSM-System vorhanden. Der
Gesamtverantwortliche TI wird die im System vorhandenen Daten zum
übergreifenden TI-Reporting verwenden.

Der Gesamtverantwortliche TI wird einmal im Monat die vom TI-ITSM-System zur
Verfügung gestellten und aus den übermittelten Daten das TI-Reporting
aufbereiten.

Der Gesamtverantwortliche TI kann ad hoc, also außerplanmäßig, Reports
anfordern. Dabei kann es erforderlich werden, andere Kennzahlen (innerhalb
eines zumutbaren Umfangs für den TI-ITSM-Teilnehmer) abzufragen. Entsteht
solch eine Notwendigkeit zur Erhebung weiterer Messgrößen, werden diese
gemeinsam mit den betroffenen TI-ITSM-Teilnehmern individuell abgestimmt.

**GS-A_4095 - Übermittlung von Ad-hoc-Reports**

TI-ITSM-Teilnehmer MÜSSEN den vom Gesamtverantwortlichen TI angeforderten
Ad-hoc-Report über die benannte Kommunikationsschnittstelle (entsprechend
GS-A_4085) im geforderten Format (entsprechend GS-A_5248, GS-A_5249, GS-A_5608)
und Zeitfenster übermitteln. **[\<=]**

### 2.2 ITSM der TI-ITSM-Teilnehmer

### 2.2.1 Auszüge aus dem Betriebshandbuch der TI-ITSM-Teilnehmer

Die Prozessschnittstellen der TI-ITSM-Teilnehmer müssen für die übergreifende
Kommunikation mit dem TI-ITSM-System prozessseitig und technisch kompatibel
sein. Der Nachweis der Etablierung geeigneter TI-ITSM-Schnittstellenprozesse
muss auszugsweise durch Vorlage eines Betriebshandbuches erfolgen.

**GS-A_5343 - Definition inhaltlicher Auszüge aus dem Betriebshandbuch**

Die Auszüge aus dem Betriebshandbuch des TI-ITSM-Teilnehmers MÜSSEN
nachfolgende Themen beinhalten:

 ---> OL

 ---> UL

 ---> OL

 ---> UL

 ---> OL

 ---> UL

 ---> OL

 ---> UL

 ---> OL

 ---> UL

 ---> OL

**[\<=]**

### 2.3 Auditierung von TI-ITSM-Teilnehmern

Es besteht die Möglichkeit, anlassbezogene Audits durchzuführen. Audits werden
durchgeführt, wenn die Prozesskommunikation zwischen den am Betrieb
beteiligten TI-ITSM-Teilnehmern nachhaltig gestört bzw. die Serviceerbringung
gegenüber dem Anwender bzw. Versicherten gefährdet ist.

Die Audits dienen der Prüfung der korrekten Umsetzung der Richtlinien
insbesondere mit dem Ziel, Schnittstellen- und Prozessprobleme zwischen
TI-ITSM-Teilnehmern zu identifizieren. Die Erkenntnisse der anlassbezogenen
Audits können auch zur Optimierung der Richtlinien führen, um die
Reibungsverluste im Zusammenspiel der TI-ITSM-Teilnehmer untereinander zu
minimieren.

**GS-A_4855-02 - Auditierung von TI-ITSM-Teilnehmern**

TI-ITSM-Teilnehmer MÜSSEN Auditierungen durch Gesamtverantwortlichen TI zur
Überprüfung der Einhaltung von Betriebs- und Produktvorgaben ermöglichen und
angemessen unterstützen.Sofern ein TI-ITSM-Teilnehmer bereits gesetzlichen
Vorgaben einer Auditierung unterliegt, ihm also eine Prüfung durch eine in der
gesetzlichen Vorgabe benannte Instanz vorgeschrieben ist, unterliegt er nicht
der Auditierung gemäß dieser Anforderung. Der TI-ITSM-Teilnehmer MUSS die
gesetzliche Vorgabe gegenüber dem Gesamtverantwortlichen TI benennen.
Fachdienste VSDM, KTR-AdV und KTR-Consumer sind von dieser Anforderung
ausgeschlossen. **[\<=]**

Umfang und Zeitpunkt des Audits stimmt der Gesamtverantwortliche TI mit dem
zuständigen Serviceverantwortlichen ab.

**GS-A_3917 - Bereitstellung der ITSM-Dokumentation bei Audits**

TI-ITSM-Teilnehmer MÜSSEN bei der Durchführung von Audits auf Verlangen alle
relevanten Informationen (z.B. TI-ITSM relevante Tickets im ITSM-System) im
Rahmen der Umsetzung bzw. Erfüllung der betrieblichen Anforderungen
bereitstellen. **[\<=]**

### 2.4 Zentrale Koordinierung durch den Gesamtverantwortlichen TI

Die Koordination der Vorgangsbearbeitung erfolgt i.d.R. durch die betroffenen
TI-ITSM-Teilnehmer in Eigenverantwortung.

Ausschließlich bei Eskalationen eines Vorgangs oder Vorgängen mit
TI-übergreifender Auswirkung kann der Gesamtverantwortliche TI – zur
Gewährleistung der Performance, Sicherheit und Stabilität der zentralen und
dezentralen Produkte – eine zentrale Koordinierung der Aktivitäten der
anderen Beteiligten übernehmen.

### 2.4.1 Eskalationen im übergreifenden TI-ITSM

Eine Eskalation wird angestoßen, um eine gefährdete Zielerreichung dennoch
sicherzustellen. In den „Übergreifenden Richtlinien zum Betrieb der TI“
wird unter dem Begriff „Eskalation“ prinzipiell eine hierarchische
Eskalation verstanden. Funktionale Eskalationen sind im Umfang der definierten
ITSM-Prozesse Zuweisungen bzw. Weiterleitungen von speziellen Aufgaben an
andere Prozessbeteiligte.

**GS-A_3920 - Eskalationseinleitung durch den TI-ITSM-Teilnehmer**

TI-ITSM-Teilnehmer MÜSSEN bei übergreifenden Vorgängen eine hierarchische
Eskalation an den Gesamtverantwortlichen TI einleiten, wenn einer der
nachfolgenden Aspekte zutrifft:

 ---> UL

ODER

 ---> UL

ODER

 ---> UL

ODER

 ---> UL

ODER

 ---> UL

**[\<=]**

### 2.4.2 Taskforce als Instrument der Deeskalation im übergreifenden TI-ITSM

Der Gesamtverantwortliche TI kann bei Vorgängen der Priorität 1 „kritisch“
und 2 „hoch“ mit (produkt-)übergreifender Auswirkung eine Taskforce zur
Behebung des Vorgangs bilden. Diese wird aus mehreren der am Betriebsprozess
beteiligten TI-ITSM-Teilnehmern zusammengesetzt.

**GS-A_3922 - Mitwirkung bei Taskforces**

TI-ITSM-Teilnehmer MÜSSEN bei Aufforderung durch den Gesamtverantwortlichen TI
an einer Taskforce zur Behebung von übergreifenden Vorgängen mit der
Priorität 1 oder 2 teilnehmen, der Taskforce gemäß der zeitlichen Vorgabe
der Aufforderung beitreten, die Lösungsfindung und die Erstellung des
Abschlussberichtes unterstützen. **[\<=]**

### 3 Incident Management

Das Incident Management verantwortet die schnellstmögliche Beseitigung von
Störungen in der TI bzw. die Schaffung eines Workarounds (Umgehungslösung)
für eine aufgetretene Störung in allen Betriebsumgebungen. Die Suche nach der
Ursache von wiederkehrenden Störungen (die sogenannte Root-Cause-Analyse) wird
in diesem Fall im Prozess Problem Management erfolgen.

Wesentliche Aufgabe des Incident Managements ist die:

 ---> UL

Es werden keine normativen Vorgaben zum lokalen Incident Management der
TI-ITSM-Teilnehmer gemacht.

### 3.1 Begriffsbestimmungen

### 3.1.1 Übergreifender Incident

Ein übergreifender Incident liegt vor, wenn

 ---> UL

Zur Bearbeitung des übergreifenden Incidents muss sichergestellt sein, dass an
den Schnittstellen zwischen den Prozessbeteiligten eine konsistente
Kommunikation, auf Grundlage der Dokumentation des übergreifenden Incidents
erfolgt.

Incidents, auf die diese Definition nicht zutrifft, sind lokale Incidents und
werden im Rahmen des lokalen Incident-Prozesses des TI-ITSM-Teilnehmers
verarbeitet.

### 3.2 Prozessdurchführung Incident Management

### 3.2.1 Übergreifenden Incident erfassen und qualifizieren

### 3.2.1.1 Übergreifenden Incident erfassen

Erlangt ein TI-ITSM-Teilnehmer Kenntnis über eine Servicestörung bzw. einen
vom erwarteten Betriebsverhalten abweichenden Service muss er auf Basis der
GS-A_3876 eine Vorprüfung vornehmen.

**GS-A_3876 - Prüfung auf übergreifenden Incident**

TI-ITSM-Teilnehmer MÜSSEN jeden gemeldeten Incident dahingehend prüfen, ob es
sich um einen übergreifenden Incident handelt, für den zur Incident-Lösung
die serviceverantwortlichen und/oder lösungsunterstützenden
TI-ITSM-Teilnehmer und/oder der Gesamtverantwortliche TI herangezogen werden
sollen. **[\<=]**

Sofern die Prüfung ergibt, dass ein übergreifender Incident vorliegt muss
dieser gemäß GS-A_3886 im TI-ITSM-System erfasst werden. Pflichtangaben für
die Ersterfassung werden vom TI-ITSM-System vorgegeben.

### 3.2.1.2 Übergreifenden Incident qualifizieren

**GS-A_5449 - Typisierung eines übergreifenden Incidents als
„sicherheitsrelevant“**

TI-ITSM-Teilnehmer MÜSSEN einen Vorgang als „sicherheitsrelevant“
markieren, wenn die Vertraulichkeit bzw. Integrität eines schutzbedürftigen
Informationsobjektes gefährdet ist. **[\<=]**

**GS-A_5450 - Typisierung eines übergreifenden Incidents als
„datenschutzrelevant“**

TI-ITSM-Teilnehmer MÜSSEN eine Störung als „datenschutzrelevant“
markieren, wenn personenbezogene Daten gemäß Art. 4 Nr. 1 DSGVO betroffen
sind. **[\<=]**

**GS-A_4125 - TI-Notfallerkennung**

TI-ITSM-Teilnehmer MÜSSEN potenzielle TI-Notfälle im operativen Betrieb im
Rahmen des Incident Managements feststellen. Potenzielle TI-Notfälle werden
als Incidents der Priorität 1 mit Kennzeichnung „TI-Notfall“
klassifiziert. **[\<=]**

Gemeldete TI-Notfälle werden zuerst als potenziell aufgenommen, und es gilt
Kapitel 12.3.5.1 und 12.3.5.2.

**GS-A_3884 - Festlegung von Dringlichkeit und Auswirkung von übergreifenden
Incidents**

TI-ITSM-Teilnehmer MÜSSEN zur Ermittlung der Priorität eines übergreifenden
Incidents die beiden Faktoren „Dringlichkeit“ und „Auswirkung“
festlegen.

Tabelle1: Tab_Betr_TIP_026 INC – Festlegung der Dringlichkeit

<table><tr><td>
Dringlichkeit

</td><td>
Beschreibung

</td></tr><tr><td>
Hoch

</td><td>
 ---> UL

</td></tr><tr><td>
Mittel

</td><td>
 ---> UL

</td></tr><tr><td>
Niedrig

</td><td>
 ---> UL

</td></tr></table>

Tabelle2: Tab_Betr_TIP_027 INC – Festlegung von Auswirkung

<table><tr><td>
Auswirkung

</td><td>
Beschreibung

</td></tr><tr><td>
Hoch

</td><td>
 ---> UL

</td></tr><tr><td>
Mittel

</td><td>
 ---> UL

</td></tr><tr><td>
Niedrig

</td><td>
 ---> UL

</td></tr></table>

**[\<=]**

Die unter „Beschreibung“ genannten Punkte sind durch ein logisches ODER
verknüpft und sollen als nicht abschließende Beispiele zur Einschätzung
dienen.

Die Ermittlung der Priorität erfolgt durch das TI-ITSM-System nach der
Vorschrift in der Tab_Betr_TIP_009: Prioritätenmatrix.

<table><tr><th rowspan="5">
Dringlichkeit

</th><th colspan="4">
Auswirkung

</th></tr><tr><td>
</td><td>
Hoch

</td><td>
Mittel

</td><td>
Niedrig

</td></tr><tr><td>
Hoch

</td><td>
1

</td><td>
2

</td><td>
3

</td></tr><tr><td>
Mittel

</td><td>
2

</td><td>
3

</td><td>
4

</td></tr><tr><td>
Niedrig

</td><td>
3

</td><td>
4

</td><td>
4

</td></tr></table>

### 3.2.1.3 Serviceverantwortung für übergreifenden Incident zuweisen

Der Melder ermittelt über das betroffene bzw. vermutete verursachende Produkt
den Serviceverantwortlichen. Dabei wird er vom TI-ITSM-System durch eine
kontextsensitive Vorschlagsliste unterstützt. Durch Auswahl des entsprechenden
TI-ITSM-Teilnehmers wird die Weiterleitung des Incidents ermöglicht und die
übergreifende Bearbeitung initiiert.

Zur Identifikation des richtigen serviceverantwortlichen TI-ITSM-Teilnehmers
werden innerhalb des Betriebskonzepts [gemKPT_Betr] die Leistungs- und
Supportmodelle definiert. Zudem werden in der zentralen Wissensdatenbank des
TI-ITSM-Systems Kontaktinformationen von TI-ITSM-Teilnehmern bereitgestellt.

### 3.2.2 Serviceverantwortung für übergreifenden Incident prüfen

Der Empfänger des übergreifenden Incidents muss bei Erhalt der Meldung seine
(vermutete) Verantwortung verifizieren:

**GS-A_3902 - Prüfung auf Serviceverantwortung**

TI-ITSM-Teilnehmer MÜSSEN jeden an sie gerichteten übergreifenden Incident
dahingehend prüfen, ob der Incident in der eigenen Serviceverantwortung liegt.
**[\<=]**

**GS-A_3904 - Annahme eines übergreifenden Incidents**

TI-ITSM-Teilnehmer MÜSSEN einen übergreifenden Incident annehmen, wenn sie die
Serviceverantwortung haben. **[\<=]**

**GS-A_3905 - Ablehnung eines übergreifenden Incidents**

TI-ITSM-Teilnehmer MÜSSEN die Ablehnung eines übergreifenden Incidents mit
einer qualifizierten Rückmeldung an den meldenden TI-ITSM-Teilnehmer versehen,
aus der nachvollziehbar zu entnehmen ist, warum keine Bearbeitung erfolgen
kann. **[\<=]**

### 3.2.3 Lösung für übergreifenden Incident erstellen

Der serviceverantwortliche TI-ITSM-Teilnehmer beginnt unverzüglich mit der
Bearbeitung der Störung. Er wird im TI-ITSM-System die Lösung und die dafür
notwendigen Aktivitäten nachvollziehbar dokumentieren. Dadurch können die
Erkenntnisse für Diagnosen und Lösungen im Rahmen des Problem Managements
genutzt werden.

**GS-A_3907 - Lösung von übergreifenden Incidents**

Der serviceverantwortliche TI-ITSM-Teilnehmer MUSS nach erfolgter Erstellung
bzw. Annahme eines übergreifenden Incidents unverzüglich mit der
Incident-Bearbeitung beginnen und – innerhalb der vereinbarten Lösungszeiten
– eine Lösung für den Incident herbeiführen und diesen beheben. **[\<=]**

**A_18403 - Erstellung einer Root Cause Analysis im Incident - Prio 1**

Lösungsverantwortliche TI-ITSM-Teilnehmer MÜSSEN spätestens mit der Lösung
einer Incidents der Priorität 1 mit einer Root Cause Analysis beginnen, dafür
das vom Gesamtverantwortlichen der TI bereitgestellte Formular nutzen und
anschließend ausgefüllt an ihn übermitteln.  **[\<=]**

Das Formular wird in der Wissensdatenbank zur Verfügung gestellt.

**A_18404 - Erstellung einer Root Cause Analysis im Incident - Prio 2 bis 4**

Lösungsverantwortliche MÜSSEN bei Incidents der Priorität 2, 3 oder 4 auf
Anfrage des Gesamtverantwortlichen der TI mit einer Root Cause Analysis
beginnen, dafür das von ihm bereitgestellte Formular nutzen und anschließend
ausgefüllt an ihn übermitteln. **[\<=]**

**A_18405 - Erstellung einer Root Cause Analysis durch am Incident beteiligte
TI-ITSM-Teilnehmer**

Am Incident beteiligte TI-ITSM-Teilnehmer MÜSSEN auf Anfrage des
Gesamtverantwortlichen der TI mit der Erstellung einer Root Cause Analysis
beginnen, dafür das vom Gesamtverantwortlichen der TI bereitgestellte Formular
nutzen und anschließend ausgefüllt an ihn übermitteln. **[\<=]**

**A_18406 - Nachlieferung zu einer Root Cause Analysis**

Lösungsverantwortliche TI-ITSM-Teilnehmer MÜSSEN auf Rückfrage des
Gesamtverantwortlichen der TI Informationen zur Root Cause Analysis
nachreichen. **[\<=]**

### 3.2.4 Unterstützung für einen übergreifenden Incident einfordern

Während der Lösungsfindung für einen übergreifenden Incident kann der
serviceverantwortliche TI-ITSM-Teilnehmer andere TI-ITSM-Teilnehmern um
Unterstützung bitten.

Der serviceverantwortliche TI-ITSM-Teilnehmer wechselt durch die Anfrage zur
Lösungsunterstützung nicht. Der Empfänger dieser Anfrage wird den
übermittelten Vorgang hinsichtlich seiner zu leistenden Lösungsunterstützung
prüfen.

**GS-A_5587 - Ablehnung der Lösungsunterstützung bei einem übergreifenden
Incident**

TI-ITSM-Teilnehmer, die die Lösungsunterstützung eines übergreifenden
Incidents ablehnen, MÜSSEN dies mit einer qualifizierten Rückmeldung an den
anfragenden TI-ITSM-Teilnehmer durchführen, aus der nachvollziehbar zu
entnehmen ist, warum keine Lösungsunterstützung möglich ist. **[\<=]**

### 3.2.5 Lösung für einen übergreifenden Incident prüfen

Nachdem der serviceverantwortliche TI-ITSM-Teilnehmer den übergreifenden
Incident gelöst hat, wird der meldende TI-ITSM-Teilnehmer über das
TI-ITSM-System informiert und zur Prüfung aufgefordert, sofern er den Incident
nicht gegen sich selbst gestellt hat.

**GS-A_5400 - Prüfung der Lösung durch den Melder eines übergreifenden
Incidents**

Der meldende TI-ITSM-Teilnehmer MUSS die ihm vorgelegte Lösung des
übergreifenden Incidents prüfen und sein Ergebnis dem serviceverantwortlichen
TI-ITSM-Teilnehmer innerhalb der Verifikationsfrist (entsprechend
[gemKPT_Betr#TIP1-A_7265]) über das TI-ITSM-System mitteilen. **[\<=]**

**GS-A_5250 - Ablehnung der Lösung eines übergreifenden Incidents**

Wird die Lösung eines Incidents durch den meldenden TI-ITSM-Teilnehmer
abgelehnt MUSS der serviceverantwortliche TI-ITSM-Teilnehmer den
übergreifenden Incident erneut bearbeiten, die Messung der Lösungszeit wird
dann fortgesetzt. **[\<=]**

### 3.2.6 Übergreifenden Incident schließen

Nach erfolgreicher Verifikation erfolgt die vollständige Schließung des
Incidents durch den serviceverantwortlichen TI-ITSM-Teilnehmer.

**GS-A_3888 - Verifikation vor Schließung eines übergreifenden Incident**

TI-ITSM-Teilnehmer MÜSSEN vor der Schließung einer übergreifenden
Incident-Dokumentation sicherstellen, dass der Incident behoben ist.Ist der
Incident nicht behoben, dann ist der bestehende Incident weiterzubearbeiten. Es
beginnt keine erneute Lösungszeit.Liegt nach Ablauf der Verifikationsfrist
(entsprechend [gemKPT_Betr#TIP1-A_7265]) keine Rückmeldung durch den meldenden
TI-ITSM-Teilnehmer vor, KANN der übergreifende Incident geschlossen werden.
**[\<=]**

**GS-A_3889 - Schließung eines übergreifenden Incidents**

Serviceverantwortliche TI-ITSM-Teilnehmer MÜSSEN nach verifizierter Behebung
der Störung die Dokumentation eines übergreifenden Incidents abschließend
bearbeiten und diesen Incident schließen. **[\<=]**

### 3.3 Abweichungen im Prozessablauf

### 3.3.1 Übergreifenden Incident eskalieren

Die Koordination der Vorgangsbearbeitung erfolgt i.d.R. durch die betroffenen
TI-ITSM-Teilnehmer in Eigenverantwortung. Kommt es zu Hindernissen im
Prozessablauf, steht den TI-ITSM-Teilnehmern das Instrument der Eskalation an
den Gesamtverantwortlichen TI nach den Vorgaben der GS-A_3920 zur Verfügung.

### 3.3.2 Mitwirkung in einer Taskforce

TI-ITSM-Teilnehmer können durch den Gesamtverantwortlichen TI zur Mitwirkung in
einer Taskforce gemäß GS-A_3922 aufgerufen werden. Diese Taskforce ist ein
Instrument zur Lösung von kritischen Incidents der Priorität 1 oder 2.

Die prozessübergreifende Regelung zur Eskalation und Mitwirkung in einer
Taskforce erfolgt in Kapitel 2.4 Zentrale Koordinierung durch den
Gesamtverantwortlichen TI.

### 3.4 Verfahren für die Lösung eines Security-Incidents

Security Incidents werden wie alle anderen Incidents behandelt. Es erfolgt ggf.
eine reduzierte bzw. eingeschränkte Kommunikation. Die Entscheidung darüber
führt der Gesamtverantwortliche TI unter Einbeziehung beratender Fachexperten
herbei.

### 3.5 Verfahren für die Lösung eines Incidents mit Datenschutzrelevanz

Incidents mit Datenschutzrelevanz werden wie alle anderen Incidents behandelt.
Es erfolgt ggf. eine reduzierte bzw. eingeschränkte Kommunikation. Die
Entscheidung darüber führt der Gesamtverantwortliche TI unter Einbeziehung
beratender Fachexperten herbei.

### 3.6 Verfahren für die Lösung von Notfall-Incidents

Wird ein Incident als Notfall qualifiziert, greift das in diesen Richtlinien
beschriebene Verfahren zur Bewältigung von TI-Notfällen.

Die Dokumentation des vom Gesamtverantwortlichen TI festgestellten Notfalls
erfolgt im Notfallmanagement. Ein entsprechender Verweis erfolgt im
zugehörigen Incident-Ticket.

### 4 Problem Management

Der Problem Management Prozess verantwortet die nachhaltige Stabilisierung aller
TI-Betriebsumgebungen, der RU, TU und PU. Die Ursachen wiederkehrender
Störungen werden vom Problem Management analysiert, bewertet und – falls
technisch und wirtschaftlich machbar – durch neue stabile Lösungen beseitigt.

Im Gegensatz zum wirkungsorientierten Incident Management, bei dem es um
schnellstmögliche Wiederherstellung beeinträchtigter TI-Services geht,
arbeitet das Problem Management ursachenorientiert, d.h. der Prozess zielt auf
eine definitive, nachhaltige Beseitigung von Störungsursachen.

Um zwischen den verschiedenen TI-ITSM-Teilnehmern sicherzustellen, dass

 ---> UL

ist durch TI-ITSM-Teilnehmer ein übergreifendes Problem Management zu
etablieren.

### 4.1 Begriffsbestimmungen

### 4.1.1 Übergreifendes Problem

Ein übergreifendes Problem liegt vor, wenn

 ---> UL

Zur Bearbeitung des übergreifenden Problems muss sichergestellt sein, dass an
den Schnittstellen zwischen den Prozessbeteiligten eine konsistente
Kommunikation, auf Grundlage der Dokumentation des übergreifenden Problems
erfolgt.

Problems, auf die diese Definition nicht zutrifft, sind lokale Problems und
werden im Rahmen des lokalen Problem-Prozesses des TI-ITSM-Teilnehmers
verarbeitet.

### 4.2 Prozessdurchführung Problem Management

### 4.2.1 Übergreifendes Problem erfassen und qualifizieren

### 4.2.1.1 Übergreifendes Problem erfassen

**GS-A_3958 - Problemerkennung durch TI-ITSM-Teilnehmer**

TI-ITSM-Teilnehmer MÜSSEN geeignete Maßnahmen implementieren, um proaktiv und
reaktiv eine Problemerkennung zu ermöglichen. **[\<=]**

**GS-A_3959 - Prüfung auf übergreifendes Problem**

TI-ITSM-Teilnehmer MÜSSEN jedes erkannte Problem dahingehend prüfen, ob es
sich um ein übergreifendes Problem handelt, für das zur Problem-Lösung die
serviceverantwortlichen und/oder lösungsunterstützenden TI-ITSM-Teilnehmer
sowie der Gesamtverantwortliche TI herangezogen werden sollen. **[\<=]**

Sofern die Prüfung ergibt, dass ein übergreifendes Problem vorliegt muss
dieses gemäß GS-A_3886 im TI-ITSM-System erfasst werden. Pflichtangaben für
die Ersterfassung werden vom TI-ITSM-System vorgegeben.

### 4.2.1.2 Übergreifendes Problem qualifizieren

**GS-A_3964 - Festlegung von Dringlichkeit und Auswirkung von übergreifenden
Problems**

TI-ITSM-Teilnehmer MÜSSEN zur Ermittlung der Priorität eines übergreifenden
Problems die beiden Faktoren „Dringlichkeit“ und „Auswirkung“ festlegen.

Tabelle4: Tab_Betr_TIP_102 PRO – Festlegung von Dringlichkeit

<table><tr><th>
Dringlichkeit

</th><th>
Beschreibung

</th></tr><tr><td>
Hoch

</td><td>
Das Problem muss schnellstmöglich gelöst werden, eine maximale negative
Auswirkung liegt vor; ein Workaround ist nicht oder nur nach viel Aufwand
vorhanden

</td></tr><tr><td>
Mittel

</td><td>
Das Problem sollte so schnell wie möglich gelöst werden; eine Ausweitung ist
absehbar

</td></tr><tr><td>
Niedrig

</td><td>
Das Problem besteht, ist aber durch geeignete Maßnahmen unter Kontrolle. Es
sollte in absehbarer Zeit gelöst werden.

</td></tr></table>

Tabelle5: Tab_Betr_TIP_103 PRO – Festlegung von Auswirkung

<table><tr><th>
Auswirkung

</th><th>
Beschreibung

</th></tr><tr><td>
Hoch

</td><td>
 ---> UL

</td></tr><tr><td>
Mittel

</td><td>
 ---> UL

</td></tr><tr><td>
Niedrig

</td><td>
 ---> UL

</td></tr></table>

  **[\<=]**

Die unter „Beschreibung“ genannten Punkte sind durch ein logisches ODER
verknüpft und sollen als nicht abschließende Beispiele zur Einschätzung
dienen.

### 4.2.1.3 Serviceverantwortung für übergreifendes Problem zuweisen

Der problemerkennende TI-ITSM-Teilnehmer ermittelt für das betroffene und
verursachende Produkt den Serviceverantwortlichen. Dies wird durch das
TI-ITSM-System unterstützt. Durch Auswahl des vermutlich verursachenden
Serviceverantwortlichen wird die Weiterleitung des Problems ermöglicht und die
übergreifende Bearbeitung initiiert.

Ein Problem kann auch dem Gesamtverantwortlichen TI zugewiesen werden, wenn die
Ursache des Problems in einer unvollständigen bzw. ungenauen Spezifikation
begründet wird.

Zur Identifikation des richtigen serviceverantwortlichen TI-ITSM-Teilnehmers
werden innerhalb des Betriebskonzepts die Leistungs- und Supportmodelle
definiert. Zudem werden im TI-ITSM-System Kontaktinformationen von
TI-ITSM-Teilnehmern bereitgestellt.

### 4.2.2 Serviceverantwortung für übergreifendes Problem prüfen

Der Empfänger des übergreifenden Problems muss bei Erhalt der Meldung seine
(vermutete) Verantwortung verifizieren.

**GS-A_3975 - Prüfung auf Serviceverantwortung zum übergreifenden Problem**

TI-ITSM-Teilnehmer MÜSSEN jedes an sie gerichtete übergreifende Problem
dahingehend prüfen, ob das Problem in der eigenen Serviceverantwortung liegt.
**[\<=]**

**GS-A_3981 - Annahme eines übergreifenden Problems**

TI-ITSM-Teilnehmer MÜSSEN das übergreifende Problem annehmen, wenn sie die
Serviceverantwortung haben. **[\<=]**

**GS-A_3982 - Ablehnung eines übergreifenden Problems**

TI-ITSM-Teilnehmer MÜSSEN das abgelehnte übergreifende Problem mit einer
qualifizierten Rückmeldung an den meldenden TI-ITSM-Teilnehmer versehen, aus
der nachvollziehbar zu entnehmen ist, warum keine Bearbeitung erfolgen kann.
**[\<=]**

### 4.2.3 Lösung für übergreifendes Problem erstellen

### 4.2.3.1 Problem Ursachenanalyse durchführen

Der serviceverantwortliche TI-ITSM-Teilnehmer beginnt unverzüglich mit der
Ursachenanalyse des Problems. Er wird im TI-ITSM-System die Ursache
nachvollziehbar dokumentieren.

**GS-A_3983 - Ursachenanalyse eines übergreifenden Problems durch
Serviceverantwortlichen**

Der serviceverantwortliche TI-ITSM-Teilnehmer MUSS nach erfolgter Erstellung
bzw. Annahme eines übergreifenden Problems unverzüglich mit der
Problem-Bearbeitung beginnen und – innerhalb der vereinbarten Lösungszeiten
– eine Lösung für das Problem herbeiführen und dieses beheben. **[\<=]**

Benötigen serviceverantwortliche TI-ITSM-Teilnehmer eine TI-Testumgebung, muss
dies vorab angefragt werden. Dazu stellen sie einen Service Request im
TI-ITSM-System.

**GS-A_3984 - Service Request zur Bereitstellung der TI-Testumgebung (RU/TU)**

TI-ITSM-Teilnehmer MÜSSEN für die Nutzung (d.h. zur Anbindung) der
TI-Testumgebung (RU/TU) einen Service Request im TI-ITSM-System stellen.
**[\<=]**

### 4.2.3.2 Lösung für übergreifendes Problem entwickeln und implementieren

Die Lösungsentwicklung erfolgt durch den serviceverantwortlichen
TI-ITSM-Teilnehmer. Dabei kann er von anderen am Prozess beteiligten
TI-ITSM-Teilnehmern sowie vom Gesamtverantwortlichen TI unterstützt werden.

**GS-A_3986 - Koordination bei übergreifenden Problems**

Der serviceverantwortliche TI-ITSM-Teilnehmer MUSS die Koordination zwischen
allen erforderlichen Lösungs- bzw. Unterstützungsbeteiligten im Rahmen der
Problemlösungsentwicklung übernehmen. **[\<=]**

Wird für die Lösung eines Problems eine Änderung an der TI benötigt, ist
diese Änderung über den Change & Release Management-Prozess anzustoßen.

**GS-A_3987 - Initiierung eines Change Request**

Der serviceverantwortliche TI-ITSM-Teilnehmer MUSS während der
Problemlösungsentwicklung einen Change Request über das TI-ITSM-System mit
Verweis auf das zugrundeliegende Problem initiieren, in dem die Durchführung
von Autorisierung, Entwicklung, Test und Implementierung der Lösung
dokumentiert wird. **[\<=]**

### 4.2.3.3 Stornierung oder Abbruch der Bearbeitung eines Problem-Tickets

**GS-A_5377 - Durchführung einer Problemstornierung**

Der serviceverantwortliche TI-ITSM-Teilnehmer KANN ein Problem stornieren, falls
einer der folgenden Aspekte zutrifft:

 ---> UL

ODER

 ---> UL

**[\<=]**

**GS-A_5588 - Abbruch der Problembearbeitung**

Der serviceverantwortliche TI-ITSM-Teilnehmer KANN die Problembearbeitung mit
Zustimmung des Gesamtverantwortlichen TI abbrechen, falls die Auswirkungen des
Problems und der Aufwand zu deren Behebung in keinem wirtschaftlichen oder
sicherheitsrelevanten Verhältnis zueinander stehen. **[\<=]**

Der Gesamtverantwortliche TI wird die Stornierung oder den Abbruch eines
Problems prüfen und alle Beteiligten informieren. Bei Ablehnung muss das
Problem vom serviceverantwortlichen TI-ITSM-Teilnehmer wieder in die
Lösungsbearbeitung übernommen werden.

### 4.2.4 Lösungsunterstützung für übergreifendes Problem

Während der Erarbeitung einer Lösung für ein übergreifendes Problem kann der
serviceverantwortliche TI-ITSM-Teilnehmer auf die Mitwirkung von anderen
TI-ITSM-Teilnehmern angewiesen sein.

Die Unterstützungsleistung wird über das TI-ITSM-System angefordert. Die
Lösungsverantwortung verbleibt beim serviceverantwortlichen TI-ITSM-Teilnehmer.

**GS-A_5589 - Prüfung auf Verantwortung zur Lösungsunterstützung**

TI-ITSM-Teilnehmer MÜSSEN jede an sie gerichtete Anfrage zur
Lösungsunterstützung eines übergreifenden Problems dahingehend prüfen, ob
sie zur Lösungsunterstützung gemäß Betriebskonzept verpflichtet sind.
**[\<=]**

**GS-A_3977 - Annahme der Verantwortung zur Lösungsunterstützung**

TI-ITSM-Teilnehmer MÜSSEN die Anfrage zur Lösungsunterstützung eines
übergreifenden Problems annehmen, wenn sie die gemäß TIP1-A_7266
[gemKPT_Betr] für die Servicekomponenten mitverantwortlich sind. **[\<=]**

**GS-A_3976 - Ablehnung der Lösungsunterstützung**

TI-ITSM-Teilnehmer MÜSSEN die Ablehnung der Lösungsunterstützung des
übergreifenden Problems mit einer qualifizierten Rückmeldung an den
serviceverantwortlichen TI-ITSM-Teilnehmer versehen, aus der nachvollziehbar zu
entnehmen ist, warum keine Lösungsunterstützung erfolgen kann. **[\<=]**

### 4.2.5 Lösung für übergreifendes Problem prüfen

Nachdem der serviceverantwortliche TI-ITSM-Teilnehmer das übergreifende Problem
gelöst hat, wird der problemerkennende TI-ITSM-Teilnehmer über das
TI-ITSM-System informiert und zur Prüfung aufgefordert, sofern er das Problem
nicht gegen sich selbst gestellt hat.

**GS-A_3988 - Prüfung der Lösung durch den Melder eines übergreifenden
Problems**

Der meldende TI-ITSM-Teilnehmer MUSS die ihm vorgelegte Lösung des
übergreifenden Problems prüfen und sein Ergebnis dem serviceverantwortlichen
TI-ITSM-Teilnehmer innerhalb der Verifikationsfrist (entsprechend
[gemKPT_Betr#TIP1-A_7265]) über das TI-ITSM-System mitteilen. **[\<=]**

**GS-A_3989 - Ablehnung der Lösung eines übergreifenden Problems**

Wird die Lösung eines übergreifenden Problems durch den meldenden
TI-ITSM-Teilnehmer abgelehnt, MUSS der serviceverantwortliche
TI-ITSM-Teilnehmer das übergreifende Problem erneut bearbeiten, die Messung
der Lösungszeit wird dann fortgesetzt. **[\<=]**

### 4.2.6 Übergreifendes Problem schließen

**GS-A_3971 - Verifikation vor Schließung eines übergreifenden Problems**

Serviceverantwortliche TI-ITSM-Teilnehmer MÜSSEN vor der Schließung einer
übergreifenden Problem-Dokumentation sicherstellen, dass das Problem gelöst
ist.Ist das Problem nicht gelöst, dann ist das bestehende Problem
weiterzubearbeiten. Es beginnt keine erneute Lösungszeit.Liegt nach Ablauf der
Verifikationsfrist (entsprechend [gemKPT_Betr#TIP1-A_7265]) keine Rückmeldung
durch den problemerkennenden TI-ITSM-Teilnehmer vor, KANN das übergreifende
Problem geschlossen werden. **[\<=]**

**GS-A_3990 - Schließung eines übergreifenden Problems**

Serviceverantwortliche TI-ITSM-Teilnehmer MÜSSEN nach verifizierter Lösung des
Problems die Dokumentation des übergreifenden Problems abschließend
bearbeiten und das Problem schließen. **[\<=]**

**GS-A_3991 - WDB-Aktualisierung nach Schließung eines übergreifenden
Problems**

Serviceverantwortliche TI-ITSM-Teilnehmer MÜSSEN nach der Behebung eines
übergreifenden Problems die Wissensdatenbank der TI um die relevanten
Problemlösungsinformationen aktualisieren. **[\<=]**

### 4.3 Abweichungen im Prozessablauf

### 4.3.1 Übergreifendes Problem eskalieren

Die Koordination der Vorgangsbearbeitung erfolgt i.d.R. durch die betroffenen
TI-ITSM-Teilnehmer in Eigenverantwortung. Kommt es zu Hindernissen im
Prozessablauf, steht den TI-ITSM-Teilnehmern das Instrument der Eskalation an
den Gesamtverantwortlichen TI nach den Vorgaben der GS-A_3920 zur Verfügung.

### 4.3.2 Mitwirkung in einer Taskforce

TI-ITSM-Teilnehmer können durch den Gesamtverantwortlichen TI zur Mitwirkung in
einer Taskforce gemäß GS-A_3922 aufgerufen werden. Diese Taskforce ist ein
Instrument zur Lösung von kritischen Problems der Priorität 1 oder 2.

Die prozessübergreifende Regelung zur Eskalation und Mitwirkung in einer
Taskforce erfolgt in Kapitel 2.4 Zentrale Koordinierung durch den
Gesamtverantwortlichen TI.

### 5 Request Fulfillment

Das Ziel des Prozesses Request Fulfillment ist es, alle regulären betrieblichen
Leistungsanfragen der TI-ITSM-Teilnehmer zu erfassen und in standardisierten
Verfahren zu bearbeiten. Damit soll eine kontrollierte, bedarfsgerechte und
aufwandsminimierte Erledigung der Service Requests sichergestellt werden. Die
Teilnahme wird übergreifend in [gemKPT_Betr#Tab_KPT_Betr_TI_003] geregelt.

### 5.1 Begriffsbestimmungen

### 5.1.1 Service Request

Ein Service Request repräsentiert einen abrufbaren Service aus dem Business
Servicekatalog der TI.

### 5.1.2 Beschwerdemanagement

Per Service Request können Hinweise oder Reklamationen eines
TI-ITSM-Teilnehmers zu TI-Services eingehen. Diese werden vom
Gesamtverantwortlichen TI bearbeitet bzw. angenommen und weitergeleitet.

### 5.2 Prozessdurchführung Request Fulfillment

### 5.2.1 Service Request erfassen

Eine Service Request Meldung wird durch einen TI-ITSM-Teilnehmer oder
zukünftigen TI-ITSM-Teilnehmer initiiert. Der gestellte Service Request
richtet sich an den Serviceverantwortlichen laut Business Servicekatalog.
Dieser besitzt die Bearbeitungsverantwortung.

Die Erstellung eines Service Requests erfolgt im TI-ITSM-System.

**GS-A_5590 - Nutzung Business-Servicekatalog bei der Erfassung von Service
Requests**

TI-ITSM-Teilnehmer MÜSSEN den im TI-ITSM-System veröffentlichten
Business-Servicekatalog bei der Erfassung von Service Requests nutzen und alle
geforderten Informationen laut der dort genannten Servicebeschreibung dem
Service Request beifügen. **[\<=]**

### 5.2.2 Service Request prüfen

Ein Service Request wird vom Serviceverantwortlichen auf Vollständigkeit und
Plausibilität geprüft.

**GS-A_5351 - Prüfung von Service Requests**

Der Serviceverantwortliche MUSS den Service Request eines TI-ITSM-Teilnehmers
auf Vollständigkeit und Plausibilität prüfen. **[\<=]**

Der Serviceverantwortliche kann eine Priorisierung des Service Request anhand
der Geschäftsanforderung (z.B. Zulassungstermine, Projektfortschritt etc.)
vornehmen.

### 5.2.3 Service Request erfüllen

Für die Bearbeitung des Service Requests ist der Serviceverantwortliche
zuständig. Er organisiert die Weiterleitung des Service Requests und stellt
dem Melder die Lösung zur Verfügung.

**GS-A_5352 - Lösung bzw. Bearbeitung des Service Requests**

Der Serviceverantwortliche MUSS sicherstellen, dass jeder Service Request
gemäß Bedingungen des Servicekataloges (SLA) bearbeitet und abgeschlossen
wird. **[\<=]**

### 5.2.4 Service Request verifizieren und schließen

Die Lösung wird an den Melder des Service Requests über das TI-ITSM-System
übermittelt.

**GS-A_5591 - Verifikation des Service Requests**

TI-ITSM-Teilnehmer MÜSSEN die Verifikation eines ausgeführten Services gemäß
der im Servicekatalog beschriebenen Angaben durchführen und das Ergebnis im
TI-ITSM-System dokumentieren. **[\<=]**

Je nach Vorgabe des Servicekatalogs können der Serviceverantwortliche, der
Melder oder weitere TI-ITSM-Teilnehmer an der Verifikation beteiligt sein. Die
Verifikation kann entfallen, sofern der Servicekatalog keine Angaben hierzu
macht.

Der Service Request wird nach positivem Abschluss der Verifikationsmaßnahmen
oder Ablauf der Verifikationsfrist im TI-ITSM-System geschlossen.

**GS-A_5592 - Schließung des Service Requests**

TI-ITSM-Teilnehmer MÜSSEN vor Schließung eines Service Requests die
fehlerfreie Lieferung des Services durch den Servicenehmer verifizieren lassen.
Bei negativer Verifikation ist für diesen Service kein neuer Request zu
stellen. Stattdessen ist der bestehende Service Request weiterzubearbeiten.
**[\<=]**

**GS-A_5593 - Schließung des Service Requests ohne Verifikation**

TI-ITSM-Teilnehmer DÜRFEN Service Requests schließen, wenn die
Verifikationsfrist (entsprechend [gemKPT_Betr#TIP1-A_7265]) ohne Rückmeldung
überschritten ist. **[\<=]**

### 6 Configuration Management

Das Configuration Management stellt den TI-ITSM-Teilnehmern Informationen über
die für die Erbringung von TI-Services erforderlichen Konfigurationselemente
und deren Beziehungen untereinander bereit. Der Prozess sorgt für die
Konsistenz der Daten und deren Bereitstellung für die Nutzung in
TI-ITSM-Prozessen und Aufgaben.

Fokus der nachfolgenden Configuration-Management-Regelungen im Betrieb ist die
Bereitstellung der Konfigurationsdaten durch die TI-ITSM-Teilnehmer.

### 6.1 Begriffsbestimmungen

### 6.1.1 Konfigurationselement (Configuration Item, CI)

Ein Konfigurationselement (Configuration Item, kurz: CI) ist eine formalisierte
Beschreibung einer zum Betrieb erforderlichen Komponente über deren gesamten
Lebenszyklus. Konfigurationselemente werden durch das Configuration Management
dokumentiert und im TI-ITSM-System verwaltet. Ein CI wird eineindeutig durch
eine CI-ID identifiziert.

Aufbau Configuration Item ID (CI-ID):

Entspricht dem Wertebereich vom XML-Datentyp „string“ mit Pattern "CI-[
0-9]{7}". Fixe Länge: 10 Zeichen.

**A_17764 - Verwendung CI-ID**

Der TI-ITSM-Teilnehmer MUSS die von dem Gesamtverantwortlichen TI vorgegebene
CI-ID für jede von ihm betriebene Produktinstanz verwenden. **[\<=]**

Die CI-ID wird automatisiert vom GTI vergeben und dem TI-ITSM-Teilnehmer im
Rahmen der betrieblichen Prozesse mitgeteilt. Eine CI-ID repräsentiert
Konfigurationsdaten des betreffenden Konfigurationselementes (CIs), die in der
CMDB des TI-ITSM-Systems gespeichert sind (bspw. Produkttyp, Produkt,
Betriebsumgebung und Anbieter). Diese Daten können unterschiedlicher Art und
Detaillierungstiefe sein (bspw. Standorte, Instanzen, weitere
Konfigurationsdaten). Die CI-ID wird u.a. bei der Identifizierung von
Rohdaten-Performance-Berichten (siehe [gemSpec_Perf#2.5.1]) oder bei der
Durchführung von Produkt-Changes im Rahmen des betrieblichen Change Management
Prozesses verwendet.

### 6.1.2 TI-Konfigurationsdatenbank

Die TI-Konfigurationsdatenbank (Configuration Management Database - CMDB) ist
ein Teil des TI-ITSM-Systems, welches Informationen über
Konfigurationselemente und deren Beziehungen untereinander verwaltet sowie
diese im Rahmen der TI-ITSM-Prozesse zur Verfügung stellt.

Im Rahmen des Configuration Managements der TI gibt es unterschiedliche
Kategorien von Konfigurationselementen.

![Abbildung-1][Abbildung-1]

### 6.1.3 TI-Stammdaten

Damit die im TI-ITSM abgebildeten Prozesse von allen TI-ITSM-Teilnehmern konform
zu den Vorgaben der TI genutzt werden können, sind grundlegende Daten zur
Verfügung zu stellen. Diese Daten werden als TI-Stammdaten bezeichnet und vom
Gesamtverantwortlichen TI im TI-ITSM-System gepflegt. Zu diesen TI-Stammdaten
gehören:

<table><tr><th>
Configuration Item

</th><th>
Beschreibung

</th><th>
Beispiel

</th></tr><tr><td>
TI-Services

</td><td>
Alle Services, die durch die TI selbst bereitgestellt werden. Diese Services
werden durch den Gesamtverantwortlichen TI definiert.

</td><td>
VSDM, KOM-LE, EPA/EPF

</td></tr><tr><td>
Produkttypen

</td><td>
Um einen TI-Service bereitzustellen, werden Produkttypen spezifiziert. Mehrere
Produkttypen bilden einen generischen TI-Service.

</td><td>
VPN-Zugangsdienst, Namensdienst

</td></tr><tr><td>
Betriebliche Rollen

</td><td>
Betriebliche Rolle, die ein TI-ITSM-Teilnehmer im Rahmen des Betriebsmodells der
TI einnehmen darf.

</td><td>
AZPD, Anbieter VPN-Zugangsdienst, Hersteller Konnektor

</td></tr><tr><td>
TI-ITSM-Teilnehmer

</td><td>
Juristische Person des TI-ITSM-Teilnehmers mit Zuweisung der betrieblichen Rolle
und Zulassungsstatus

</td><td>
Firma x / Anbieter X.509 TSPs für eGK

</td></tr></table>

### 6.1.4 TI-Konfigurationsdaten

Configuration Items – Organisation, Produkte und Servicekatalog – werden im
Rahmen des Zulassungsprozesses vom Gesamtverantwortlichen TI angelegt. Während
des gesamten Leistungszeitraumes werden diese Informationen vom
Serviceverantwortlichen aktuell gehalten.

Die von den TI-ITSM-Teilnehmern verantworteten Produkte werden als logische
Produktinstanzen und deren konkrete – für die Steuerung des übergreifenden
Betriebs notwendigen – Konfigurationsdaten der Produktinstanz ausgeprägt.

<table><tr><th>
Configuration Item

</th><th>
Beschreibung

</th><th>
Beispiel

</th></tr><tr><td>
Organisation

</td><td>
Angabe der für den Betrieb relevanten Kommunikationsschnittstellen

</td><td>
gem. GS-A_4088

</td></tr><tr><td>
Produkte

</td><td>
Von einem TI-ITSM-Teilnehmer und der jeweiligen Betrieblichen Rolle
verantworteten generischen Produkte

</td><td>
VPN-Zugangsdienst vom Anbieter VPN-Zugangsdienst des TI-ITSM-Teilnehmers 1

</td></tr><tr><td>
Servicekatalog

</td><td>
Definiert die zur Serviceerbringung notwendigen Business – sowie technischen
Services und bildet diese ggf. konkret mit SLAs aus.

</td><td>
Produkt Zentrales Netz des AZPD - Bereitstellen eines SZZP für alle
Bedarfsträger

</td></tr><tr><td>
Logische Produktinstanzen

</td><td>
Konkrete Ausprägung des generischen Produktes in einer spezifischen
Betriebsumgebung

</td><td>
VPN-Zugangsdienst in der Betriebsumgebung RU; Konnektor in der Betreibumgebung PU

</td></tr><tr><td>
Konfigurationsdaten Produktinstanz

</td><td>
Detaillierte Daten zu der logischen Produktinstanz

</td><td>
Produktversion; Produkttypversion, Status

</td></tr></table>

### 6.1.5 Lokale Konfigurationsdaten

Hier handelt es sich um spezifische Konfigurationsdaten die nur vom
TI-ITSM-Teilnehmer gepflegt werden. Diese sind nicht grundsätzlich Teil der
übergreifenden TI-Konfigurationsdaten.

### 6.2 Prozessdurchführung Configuration Management

### 6.2.1 Schema der TI-Konfigurationsdatenbank pflegen

Der Gesamtverantwortliche TI legt die Struktur der Konfigurationselemente und
deren Beschreibung durch Attribute fest. Er stellt diese Struktur den
TI-ITSM-Teilnehmern über das TI-ITSM-System zur Verfügung.

Der Gesamtverantwortliche TI wird das Schema der TI-Konfigurationsdatenbank
regelmäßig prüfen und ggf. Anpassungen vornehmen. Die TI-ITSM-Teilnehmer
werden über diese Anpassungen mit angemessener Frist vorab informiert.

### 6.2.2 Konfigurationsdaten pflegen

TI-ITSM-Teilnehmer führen Änderungen nur unter Kontrolle des Change & Release
Managements sowie des Request Fulfillments durch. Nach erfolgreicher
Durchführung der Änderungsprozesse stehen die aktualisierten Daten den
TI-ITSM-Teilnehmern bzw. dem Gesamtverantwortlichen TI zur Wahrnehmung der
jeweiligen Rolle bedarfsgerecht im TI-ITSM-System zur Verfügung.

**GS-A_4114 - Bereitstellung von TI-Konfigurationsdaten**

TI-ITSM-Teilnehmer MÜSSEN entsprechend ihrer Rolle (vgl.
[gemKPT_Betr#Tab_KPT_Betr_TI_002]) TI-Konfigurationsdaten mit dem
Gesamtverantwortlichen TI zu Beginn der Serviceerbringung initial abstimmen und
im TI-ITSM-System hinterlegen. **[\<=]**

DieInstance-IDssind gemäß [gemSpec_OM#GS-A_3856] ebenfalls
alsTI-Konfigurationsdatenmit dem Gesamtverantwortlichen TI initial und bei
Änderung abzustimmen. Neu vergebene Instance-IDs entsprechen der in Kapitel
6.1.1 beschriebenen CI-ID.

**GS-A_5594 - Identifikation von TI-Konfigurationsdaten**

TI-ITSM-Teilnehmer MÜSSEN TI-Konfigurationsdaten gemäß Konfigurationsschema
im TI-ITSM-System ermitteln und definieren. **[\<=]**

**GS-A_4115 - Datenänderung für TI-Konfigurationsdaten**

TI-ITSM-Teilnehmer MÜSSEN TI-Konfigurationsdaten über den gesamten Zeitraum
der Serviceerbringung aktuell halten und im TI-ITSM-System hinterlegen. **[\<=]**

Spezifische Anforderungen an die Versionierung der Produkte und der logischen
Produktinstanzen sind gemäß [gemSpec_OM] zu beachten.

### 6.2.2.1 Übermittlung von Konfigurationsdaten nach lokal autorisierten Produkt-Changes

Sofern ein Change lokal autorisiert wurde, müssen die geänderten Produktdaten
an das Configuration Management übermittelt werden.

**GS-A_4399 - Übermittlung von Produktdaten nach Abschluss von lokal
autorisierten Produkt-Changes**

Alle TI-ITSM-Teilnehmer MÜSSEN nach dem Abschluss (nach der Produktivsetzung
des Produkt-Changes) von lokal autorisierten Produkt-Changes die geänderten
Produktdaten an das TI-ITSM-System übermitteln. **[\<=]**

### 7 Change & Release Management

Das Change & Release Management stellt sicher, dass alle Änderungen an
Produkten und den darauf basierenden Services kontrolliert durchgeführt
werden. Innerhalb des Change Management werden Änderungsanträge
aufgezeichnet, bewertet sowie autorisiert und die daraus resultierenden
Umsetzungen als Änderungsanforderungen koordiniert.

Im vorliegenden Dokument wird das übergreifende Change Management für Produkte
und deren logische Produktinstanzen geregelt.

Es werden keine normativen Vorgaben zum lokalen Change Management der
TI-ITSM-Teilnehmer gemacht.

### 7.1 Begriffsbestimmungen

### 7.1.1 Request for Change (RfC)

Unter einem Request for Change versteht man einen Antrag auf das Hinzufügen,
Verändern oder Entfernen von autorisierten Services oder Servicekomponenten
unter Bezug auf Configuration Items (Produkte, logische Produktinstanzen und
deren Konfiguration sowie Produkttypen). Ein Request for Change wird zum Change
nach dessen Autorisierung.

### 7.1.2 Produkt-Change

Ein Produkt-Change beinhaltet Änderungen an einem Produkt bzw. einer logischen
Produktinstanz, welches sich bereits im Betrieb befindet oder in den Betrieb
eingeführt oder herausgeführt werden soll.

Bei Produkt-Changes gibt es zwei Durchführungsvarianten.

### 7.1.2.1 Master-Change

Der Master-Change adressiert den Inhalt der Produktänderung fachlich. Er hat
noch keinen konkreten Bezug zur Umsetzung in einer Umgebung (RU TU PU). Im
Master-Change-Prozess werden grundsätzliche Entscheidungen (z.B.:
Zulassungsrelevanz, Testumfang, oder dem zeitlichen Gesamtverlauf) vereinbart.
Die mit dem Master-Change abgestimmten und freigegebenen Änderungen werden mit
den sogenannten Sub-Changes in die Umgebungen eingebracht.

### 7.1.2.2 Sub-Change

Der Sub-Change ist einem Master-Change innerhalb eines Produkt-Changes
zugeordnet. Er setzt die im Master-Change definierte(n) Änderung(en) in einer
konkreten Umgebung und damit der logischen Produktinstanz um. Sub-Changes
werden nur im Rahmen von Produkt-Changes verwendet.

### 7.1.3 Produkttyp-Change

Ein Produkttyp-Change umfasst die konzeptionellen Änderungen an einem
Produkttypen der TI. Ergebnis des Prozesses ist eine geänderte Spezifikation
des Produkttypen. Ein Produkttyp-Change kann von TI-ITSM-Teilnehmern oder vom
Gesamtverantwortlichen TI gestellt werden.

### 7.1.4 Emergency-Change

Ein Emergency-Change ist eine Änderung, die aufgrund einer Notsituation
durchgeführt werden muss, um so schnell wie möglich diese Notsituation zu
lindern. Ein Emergency-Change kann in folgenden beispielhaften Situationen
erforderlich werden:

 ---> UL

Die Dringlichkeit der Korrektur lässt unter Umständen kein Testen zu; die
sofortige Heilung der Notsituation ist das primäre Ziel. Das damit
einhergehende Risiko wird bewusst in Kauf genommen.

Für die kontrollierte Durchführung eines Emergency-Change wird ein
Entscheidungsgremium, das Emergency Change Advisory Board (eCAB) implementiert,
das den beteiligten TI-ITSM-Teilnehmern bei der Bewertung des auftretenden
Emergency-Change wirksam unterstützt.

### 7.1.5 Betriebliches Change-Bewertungsgremium (BCB)

Das Betriebliche Change-Bewertungsgremium (BCB) ist das Board des
Gesamtverantwortlichen TI, in dem RfCs bewertet und über deren weiteren
Umsetzungsverlauf entschieden wird. Dabei werden die beteiligten
TI-ITSM-Teilnehmer bei Bedarf in die Entscheidungsfindung und Umsetzungsplanung
durch den Gesamtverantwortlichen TI einbezogen.

### 7.1.6 Change Advisory Board (CAB)

Das Change Advisory Board ist ein Gremium, das aus allen relevanten Vertretern
der TI-ITSM-Teilnehmer, die von der Durchführung eines konkreten Changes
betroffen sind, besteht. Wird eine vom BCB getroffene Entscheidung von den
beteiligten TI-ITSM-Teilnehmern nicht mitgetragen, wird das CAB vom
Gesamtverantwortlichen TI einberufen um das weitere Vorgehen abzustimmen oder
zu eskalieren.

### 7.1.7 Emergency Change Advisory Board (eCAB)

Das Emergency Change Advisory Board (eCAB) ist eine besondere Organisationsform
des CAB, organisiert durch den Gesamtverantwortlichen TI. Die Zusammensetzung
wird fallbezogen festgelegt. Ziel und Aufgabe des eCAB ist es, bei auftretenden
Anforderungen zur Durchführung eines Emergency Change eine möglichst zeitnahe
Bewertung und Autorisierung bzw. Ablehnung herbeizuführen. Hierfür müssen
die Teilnehmer mit entsprechenden Kompetenzen ausgestattet sein.

### 7.1.8 Post Implementation Review (PIR)

Beim Abschluss des Master-Changes führt der Gesamtverantwortliche TI das Post
Implementation Review gemeinsam mit dem Durchführenden des Produkt-Changes
durch. Ziel ist die Identifizierung von Optimierungspotenzialen und deren
Umsetzung in den weiteren Change-Durchführungen.

### 7.1.9 Change- & Release-Kalender

Der Change- & Release-Kalender zeigt die laufenden Aktivitäten im Change &
Release Management in einer Kalenderdarstellung übersichtlich für alle
beteiligten TI-ITSM-Teilnehmer dar. Der Kalender dient allen am Betrieb der TI
Beteiligten dazu, sich über anstehende und durchgeführte Änderungen
informieren zu können. Er ist zugleich ein Organisations- und
Planungsinstrument im Rahmen des Change Managements. Er ersetzt nicht die
aktive Steuerung eines Change in der TI, sondern ermöglicht eine langfristige
Vorschau auf geplante Änderungen und ist ein zusätzliches Hilfsmittel bei der
Analyse von Störungsursachen bezüglich der Identifikation von Seiteneffekten
bereits umgesetzter Änderungen.

### 7.2 Prozessdurchführung Change & Release Management

### 7.2.1 Produkt-Change: Request for Change (RfC) erstellen

Produktänderungsbedarfe können durch verschiedene Einflussfaktoren bei den
TI-ITSM-Teilnehmern festgestellt werden. Diese können sich aus dem Incident
Management, dem Problem Management oder auch durch Änderungsbedarfe eines
Produktes ergeben.

**A_13575 - Qualität von RfCs**

Der RfC-stellende TI-ITSM-Teilnehmer MUSS die RfCs so formulieren, dass der
Umfang und der Bedarf in sich vollständig ist, so dass der
Gesamtverantwortliche TI den RfC ohne Hinzuziehung weiterer Dokumente bewerten
kann. **[\<=]**

Nicht vollständig erfasste RfCs werden vom TI-ITSM-System nur gespeichert,
nicht an den Gesamtverantwortlichen TI zur Bewertung und Autorisierung
weitergeleitet.

**GS-A_4400 - Produkt-RfC (Master-Change) erstellen**

Alle TI-ITSM-Teilnehmer MÜSSEN für genehmigungspflichtige Produktänderungen
einen Produkt-RfC (Master-Change) im TI-ITSM-System erstellen. **[\<=]**

**GS-A_4398 - Prüfung auf genehmigungspflichtige Produktänderung**

Alle TI-ITSM-Teilnehmer MÜSSEN jeden festgestellten Produktänderungsbedarf
einer Prüfung gemäß der unten abgebildeten Tab_Betr_TIP_024 CHG –
Vorprüfung Produktänderungsbedarf unterziehen. Dabei ist - durch Feststellung
der Wechselwirkungen mit anderen Produkten sowie der Abweichung von
Produkttypvorgaben - zu prüfen, ob es sich um eine genehmigungspflichtige
Produktänderung handelt.

Tabelle8: Tab_Betr_TIP_024 CHG – Vorprüfung. Produktänderungsbedarf

<table><tr><th>
Change Typ

</th><th>
Wechselwirkungen mit anderen Produkten (an den Schnittstellen)

</th><th>
Abweichung von Produkttypvorgaben

</th></tr><tr><td>
lokal autorisiert

</td><td>
Nein

</td><td>
Nein

</td></tr><tr><td>
genehmigungspflichtig

</td><td>
Nein

</td><td>
Ja

</td></tr><tr><td>
genehmigungspflichtig

</td><td>
Ja

</td><td>
Nein

</td></tr><tr><td>
genehmigungspflichtig

</td><td>
Ja

</td><td>
Ja

</td></tr></table>

**[\<=]**

**GS-A_5597 - Produkt-RfC (Sub-Changes) erstellen**

Der TI-ITSM-Teilnehmer MUSS zur Umsetzung der Änderungen des Master-Changes in
den konkreten Betriebsumgebungen die abgeleiteten Sub-Changes auf Basis des
autorisierten Master-Changes und der abgestimmten Rahmenbedingungen stellen.
**[\<=]**

Lokal autorisierte Changes sind informationspflichtig im Rahmen des
Configuration Managements (GS-A_4399).

Um die Wirksamkeit eines Produkt-Changes nachzuweisen, ist eine Verifikation
notwendig. Hiermit wird nachgewiesen, dass der Produkt-Change wie geplant
implementiert wurde und die TI-Fachanwendungen weiterhin verfügbar und
funktional sind. Die Verifikationsbeschreibung ist Bestandteil des
Master-Changes.

**GS-A_5599 - Beschreibung der Verifikation des Produkt-Changes im RfC**

Jeder TI-ITSM-Teilnehmer, der einen Produkt-RfC stellt, MUSS für diesen eine
Verifikation beschreiben, welche die Wirksamkeit des Changes nachweist.
**[\<=]**

**GS-A_5600 - Beschreibung der Verifikation des Produkt-Changes in Auswirkung
auf andere TI-Fachanwendungen im RfC**

Jeder TI-ITSM-Teilnehmer, der einen Produkt-RfC stellt, MUSS eine Verifikation
beschreiben, welche die Ende-zu-Ende-Verfügbarkeit und -Funktionalität der
entsprechenden Anwendungsfälle nach der vollständigen Implementierung des
Changes in Auswirkung auf andere TI-Fachanwendungen nachweist. **[\<=]**

**GS-A_5370 - Prüfung auf Emergency Change**

Alle TI-ITSM-Teilnehmer MÜSSEN auf Grundlage der in Tabelle 12:
Tab_Betr_TIP_048 CHG – Kriterien für Emergency Changes genannten Kriterien
prüfen, ob die Notwendigkeit zur Durchführung eines Emergency Change besteht.

Tabelle9: Tab_Betr_TIP_048 CHG – Kriterien für Emergency Changes

<table><tr><td>
Definition

</td><td>
Kriterien

</td></tr><tr><td>
EMERGENCY  
CHANGE

</td><td>
 ---> UL

</td></tr></table>

**[\<=]**

### 7.2.2 Produkt-Change: RfC bewerten

Die Bewertung und Autorisierung eines RfC obliegt dem Gesamtverantwortlichen TI.
Um diese Aufgabe wahrzunehmen ist er ggf. auf die Unterstützung weiterer
TI-ITSM-Teilnehmer angewiesen.

**GS-A_4402 - Mitwirkungspflicht bei der Bewertung vom Produkt-RfC**

Alle betroffenen TI-ITSM-Teilnehmer MÜSSEN bei der Bewertung eines Produkt-RfC
mitwirken. Die Mitwirkung erfolgt innerhalb der Bewertungsphase im BCB oder
bilateral zwischen TI-ITSM-Teilnehmer und Gesamtverantwortlichen TI. **[\<=]**

Damit der Gesamtverantwortliche TI die Aufgabe der Bewertung und Autorisierung
in angemessener Qualität durchführen kann sind Bearbeitungsfristen festgelegt.

**GS-A_5610 - Bearbeitungsfristen in der Bewertung von Produkt-Changes**

Alle betroffenen TI-ITSM-Teilnehmer MÜSSEN folgende Fristen bei der Erstellung
eines RfCs beachten:

 ---> UL

**[\<=]**

Werden diese Fristen nicht eingehalten, so kann der Gesamtverantwortliche TI die
Bewertung des Changes ablehnen. Dies führt zu einer Stornierung des RfC bzw.
des gesamten Change-Vorgangs.

### 7.2.3 Produkt-Change: RfC genehmigen

Der realisierende TI-ITSM-Teilnehmer hat sich die für die Autorisierung
notwendigen Genehmigungen des GesamtverantwortIichen der TI einzuholen.

**GS-A_5611 - Umsetzung von autorisierten RFC**

TI-ITSM-Teilnehmer MÜSSEN vor der Umsetzung eines RfCs die Autorisierung des
Gesamtverantwortlichen TI einholen. Ausnahmenregelungen beziehen sich einzig
auf Emergency Changes. **[\<=]**

### 7.2.4 Produkt-Change umsetzen

Die Umsetzung des autorisierten Produkt-Changes obliegt dem zuständigen
TI-ITSM-Teilnehmer. Die Umsetzung eines Master-Changes bedeutet, dass im
nächsten Schritt die konkreten Sub-RfCs durch den TI-ITSM-Teilnehmer gestellt
werden.

Die Umsetzung von Sub-RfCs bedeutet die konkrete Änderung eines Produktes und
damit einer logischen Produktinstanz in der jeweiligen Betriebsumgebung.
Grundsätzlich wird davon ausgegangen, dass jede Änderung eines Produktes von
der RU über die TU bis zur PU sequenziell durchgeführt werden muss. Ausnahmen
davon müssen im Rahmen des Master-Changes zwischen TI-ITSM-Teilnehmer und dem
Gesamtverantwortlichen TI vereinbart werden.

Die Referenzumgebung (RU) und die Testumgebung (TU) werden vom
Gesamtverantwortlichen TI koordiniert. Der realisierende TI-ITSM-Teilnehmer
stimmt sich mit der testkoordinierenden Instanz ab und berücksichtigt diese
Abstimmung in der Ausprägung der entsprechenden Sub-RfCs (RU und TU).

**GS-A_4419 - Nutzung der Testumgebung (RU/TU)**

TI-ITSM-Teilnehmer MÜSSEN die Anforderungen und die geplante Belegung an die
Nutzung der Referenzumgebung (RU) und der Testumgebung (TU) für ihre
Produkttests mit dem Gesamtverantwortlichen TI abstimmen. **[\<=]**

Das Deployment eines Produkt-Changes wird durch den Gesamtverantwortlichen TI
zeitlich und verfahrenstechnisch überwacht. TI-ITSM-Teilnehmer müssen die
Umsetzung des Produkt-Changes gemäß den Vorgaben vom Gesamtverantwortlichen
TI durchführen und stetig deren Einhaltung prüfen und Abweichungen an den
Gesamtverantwortlichen TI über das TI-ITSM-System kommunizieren.

**GS-A_4417 - Stetige Aktualisierung des Change-Datensatzes im TI-ITSM-System**

Realisierende TI-ITSM-Teilnehmer MÜSSEN die interne Dokumentation der Planungs-
und Realisierungsdaten von autorisierten Produkt-Changes stetig im
TI-ITSM-System aktuell halten. **[\<=]**

Ein Produkt-Change gilt als implementiert, wenn:

 ---> UL

### 7.2.5 Produkt-Change: Umsetzung verifizieren

**GS-A_5601 - Nachweis der Wirksamkeit eines Changes**

Jeder TI-ITSM-Teilnehmer, der einen Produkt-RfC stellt, SOLL eine Verifikation
durchführen, welche die Wirksamkeit des Changes nachweist. Der
TI-ITSM-Teilnehmer SOLL dem Gesamtverantwortlichen TI die entsprechenden
Nachweise vorlegen. **[\<=]**

**GS-A_5602 - Nachweis der Wirksamkeit eines Changes in Auswirkung auf andere
TI-Fachanwendungen**

Jeder TI-ITSM-Teilnehmer, der einen Produkt-RfC stellt, SOLL auf Anfrage des
Gesamtverantwortlichen TI eine Verifikation durchführen, welche die
Ende-zu-Ende-Verfügbarkeit und -Funktionalität eines entsprechenden
Anwendungsfalls der veränderten Produktinstanz nachweist. Der
TI-ITSM-Teilnehmer SOLL dem Gesamtverantwortlichen TI die entsprechenden
Nachweise vorlegen. **[\<=]**

**A_18407 - Unterstützung bei Change-Verifikation**

TI-ITSM-Teilnehmer, deren Service von einem Produkt-Change betroffen ist,
MÜSSEN nach der Change-Implementierung bei der Ende-zu-Ende-Verifikation
unterstützen. **[\<=]**

Der Gesamtverantwortliche der TI legt den Teilnehmerkreis zur Verifikation im
Rahmen der Produkt-Change-Freigabe fest.

### 7.2.6 Produkt-Change abschließen

Sind die Umsetzungsarbeiten abgeschlossen, kann der Change nach erfolgreicher
Verifikation und abschließender Dokumentation geschlossen werden.

**GS-A_4407 - Bereitstellung der Dokumentation des Change Managements für
genehmigungspflichtige Produkt-Changes**

TI-ITSM-Teilnehmer MÜSSEN für jeden genehmigungspflichtigen Produkt-Change
eine Dokumentation der Aktivitäten und Nachweise im TI-ITSM-System ablegen.
**[\<=]**

Nach Abschluss des letzten Sub-RfCs ist der zugehörige Master-RfC ebenfalls vom
TI-ITSM-Teilnehmer abzuschließen. Dabei kann der TI-ITSM-Teilnehmer
Anforderungen an zukünftige Durchführungen ähnlicher Art, die zur
Optimierung des Durchführungsprozesses dienen, an den Gesamtverantwortlichen
TI übermitteln.

**GS-A_4425 - Übermittlung von Optimierungsmöglichkeiten zur Umsetzung von
genehmigten Produkt-Changes**

TI-ITSM-Teilnehmer MÜSSEN mit erfolgtem Abschluss oder Abbruch des
Produkt-Changes eine Bewertung des Master-Changes durchführen und dabei
gegebenenfalls erkannte Potenziale für mögliche Optimierungen zukünftiger
Durchführungen von Produkt-Changes dem Gesamtverantwortlichen TI mitteilen.
**[\<=]**

Der Gesamtverantwortliche TI wird nach einem ggf. mit dem durchführenden
TI-ITSM-Teilnehmer abschließenden PIR (Post Implementation Review) den
Master-Change und damit den Gesamtvorgang schließen.

### 7.3 Abweichungen im Prozessablauf

Bei einer festgestellten Abweichung des dem aktuellen Produkt-Change zugrunde
liegenden Produkt-RfCs wird der Gesamtverantwortliche TI entscheiden, welche
Konsequenzen die Feststellung bzw. Abweichung auf die weitere Durchführung des
Produkt-Changes hat und welche Maßnahmen zu treffen sind.

Dazu wird sich der Gesamtverantwortliche TI mit dem durchführenden
TI-ITSM-Teilnehmer und bei Bedarf mit den beteiligten TI-ITSM-Teilnehmern
beraten. Die Ergebnisse werden vom Gesamtverantwortlichen TI im TI-ITSM-System
dokumentiert, ebenso wie eine eventuelle Status-Änderung des Produkt-Changes
(bspw. Stornierung). Die beteiligten TI-ITSM-Teilnehmer werden vom
Gesamtverantwortlichen TI hierüber abschließend per E-Mail informiert.

**GS-A_4418 - Übermittlung von Abweichungen vom Produkt-RfC**

TI-ITSM-Teilnehmer, die während der Umsetzung des autorisierten Produkt-Changes
Abweichungen zur Planung in Bezug auf zeitliche, inhaltliche und in der
Auswirkung im Produkt-RfC feststellen, MÜSSEN diese unverzüglich dem
Gesamtverantwortlichen TI melden. **[\<=]**

Festgestellte schwerwiegende Konflikte bei der Bewertung oder Durchführung
eines Produkt-Changes sind gemäß GS-A_3920 an den Gesamtverantwortlichen TI
zu eskalieren.

Stellen die an einem Produkt-Change beteiligten TI-ITSM-Teilnehmer negative
Auswirkungen einer Änderung während der Umsetzung fest, so kann der
Gesamtverantwortliche TI die Durchführung des im Produkt-Change hinterlegten
Fallbackplans anweisen.

**GS-A_4424 - Umsetzung des Fallbackplans**

TI-ITSM-Teilnehmer MÜSSEN einen Fallbackplan nach den Vorgaben des
Gesamtverantwortlichen TI erstellen und – bei erkannter Notwendigkeit
während des Change Deployments – umsetzen. **[\<=]**

### 7.4 Verfahren für einen Standard-Change

Um eine effiziente Durchführung von unkritischen, zeitlich gut planbaren und
wiederholt durchzuführenden „Routine“ Produkt-Changes zu gewährleisten,
können Changes als „Standard-Changes“ durchgeführt werden.

Standard-Changes werden durch den Gesamtverantwortlichen TI im Rahmen des Change
Managements definiert. Jeder Change durchläuft zunächst den Non-Standard
Change-Prozess. Aus einem Non-Standard-Change wird ein Standard-Change, wenn
folgende Kriterien erfüllt sind:

 ---> UL

**GS-A_5366 - Mitwirkungspflicht der TI-ITSM-Teilnehmer bei der Festsetzung von
Standard-Produkt-Changes**

TI-ITSM-Teilnehmer MÜSSEN zur abschließenden Kategorisierung von
Produkt-Changes als „Standard-Change“ den Gesamtverantwortlichen TI
unterstützen, indem sie die zur Prüfung erforderlichen Inhalte auf
Anforderung an den Gesamtverantwortlichen TI liefern.TI-ITSM-Teilnehmer MÜSSEN
für die zukünftige Umsetzung des Produkt-Changes als „Standard-Change“
die zum jeweiligen Produkt-Change dazugehörigen Umsetzungsaktivitäten
dokumentieren und diese dem Gesamtverantwortlichen TI übergeben. **[\<=]**

Die Abstimmung der Standard-Changes findet im Rahmen des Post Implementation
Reviews statt.

### 7.5 Verfahren für einen Emergency-Change

**GS-A_5378 - Durchführung von Emergency-Changes durch TI-ITSM-Teilnehmer**

TI-ITSM-Teilnehmer MÜSSEN bei der Umsetzung eines Emergency-Changes die
zeitliche Kritikalität beachten, d. h., die eingetretene Notsituation
schnellstmöglich beseitigen und bei der Umsetzung den Anweisungen (Freigabe,
Ablehnung, Testanforderungen, Dokumentation) des Gesamtverantwortlichen TI
folgen. **[\<=]**

**GS-A_5361 - Durchführung von Emergency-Changes durch TI-ITSM-Teilnehmer bei
Nichterreichbarkeit des Gesamtverantwortlichen TI**

TI-ITSM-Teilnehmer MÜSSEN bei Nichterreichbarkeit des Gesamtverantwortlichen TI
außerhalb der Servicezeit - und daraus resultierenden fehlenden Freigabe –
einen Emergency Change in eigenem Ermessen durchführen.TI-ITSM-Teilnehmer
MÜSSEN dabei das Zutreffen aller drei folgenden Bedingungen beachten:

 ---> OL

**[\<=]**

### 8 Knowledge Management

Durch den Gesamtverantwortlichen TI wird ein Knowledge Management etabliert, um
den Support-leistenden Organisationen die TI-Produktinformationen für die
Ursachenanalyse und Lösungsfindung von Incidents und Problems bereitzustellen.
Diese Produktinformationen werden in der Wissensdatenbank bereitgestellt. Die
Wissensdatenbank dient dabei als erste Anlaufstelle für Support-leistende
Organisationen.

In der Wissensdatenbank abgelegte Produktinformationen unterstützen
TI-ITSM-Teilnehmer bei der Klärung im Betrieb bzw. bei der Nutzung
auftretender Fragestellungen. Alle TI-ITSM-Teilnehmer werden verpflichtet,
diese Informationen bereitzustellen.

### 8.1 Begriffsbestimmungen

### 8.1.1 Wissensdatenbank (WDB) des TI-ITSM-Systems

Die Wissensdatenbank wird durch den Gesamtverantwortlichen TI bereitgestellt und
unterstützt TI-ITSM-Teilnehmer im Falle einer Störung dabei, mehr
Informationen über die möglichen Störungsursachen und möglichen Lösungen
der Produkte zu erhalten und den für die Fehlerbehebung Verantwortlichen zu
identifizieren und zu kontaktieren.

Alle TI-ITSM-Teilnehmer erhalten im Rahmen des TI-ITSM Onboardings Zugang zur
Wissensdatenbank.

Die Wissensdatenbank stellt mindestens folgende Informationen bereit:

 ---> UL

### 8.2 Prozessdurchführung Knowledge Management

### 8.2.1 Wissen identifizieren und übermitteln

**GS-A_4117 - Informationsbereitstellung durch TI-ITSM-Teilnehmer**

TI-ITSM-Teilnehmer KÖNNEN Produkt- bzw. Serviceinformationen, mögliche
Störungsursachen und Hinweise zu deren Behebung elektronisch an den
Gesamtverantwortlichen TI übermitteln und stets aktuell halten. **[\<=]**

Der Gesamtverantwortliche TI stellt dazu die Wissensdatenbank zur Verfügung.
TI-ITSM-Teilnehmer können mit einem qualifizierten Link auf Inhalte ihrer
eigenen (lokalen) Wissensdatenbank verweisen. In diesem Fall müssen sie
mindestens sicherstellen, dass

 ---> UL

Beispiele für Produkt- und Serviceinformationen sind:

 ---> UL

**GS-A_5603 - Eingangskanal für Informationen von TI-ITSM-Teilnehmern**

TI-ITSM-Teilnehmer MÜSSEN den vom Gesamtverantwortlichen TI bereitgestellten
Eingangskanal für die Einlieferung von Informationen nutzen. **[\<=]**

Der Gesamtverantwortliche TI wird die TI-ITSM-Teilnehmer über die etablierten
Kommunikationsschnittstellen informieren, auf welchem Weg und in welcher Form
Informationen für die Wissensdatenbank bereitgestellt werden müssen.

### 9 Service Level Management

Mit Hilfe des Service Level Management werden die Service Level für alle
TI-ITSM-Teilnehmer definiert, kontrolliert und ggf. optimiert.

Die Ziele des übergreifenden Service Level Management sind:

 ---> UL

### 9.1 Begriffsbestimmungen

### 9.1.1 Service Level

Service Level werden grundsätzlich in die Ausprägungen technisch und
organisatorisch unterteilt.

Organisatorische Service Level werden für die zu betrachtenden TI-ITSM-Prozesse
im Betriebskonzept inhaltlich definiert und durch Vorgaben für messbare
Zielwerte konkretisiert. Die SL-ID eines organisatorischen Service Level
beginnt immer mit dem Präfix „ITSM“.

Technische Service Level sind in der übergreifenden Spezifikation
„Performance und Mengengerüst TI-Plattform“ [gemSpec_Perf] beschrieben.
Die Tabelle Tab_gemKPT_Betr_Performance-Kenngroessen enthält die je Produkttyp
definierten und zu reportenden Service Level. Die SL-ID eines technischen
Service Level beginnt immer mit dem Präfix „PDT“.

Die in den Service-Level-Auswertungen dargestellten Werte sind Indikatoren für
die Qualität der erbrachten Services. Service Level Verletzungen stellen eine
Untererfüllung vereinbarter Service Level dar und weisen auf entsprechenden
Verbesserungspotenziale hin.

### 9.1.2 Service Level Report

Der Service Level Report enthält für den jeweiligen Berichtszeitraum die
tatsächlich gemessenen Service Level Werte und ggf. deren Kommentierung.

Beispiele erforderliche Kommentierungen:

 ---> UL

Der Service Level Report dient damit der Kontrolle der Einhaltung der Service
Level Vereinbarung durch den TI-ITSM-Teilnehmer und der inhaltlichen
Auseinandersetzung mit der geleisteten Qualität.

### 9.2 Prozessdurchführung Service Level Management

### 9.2.1 Messung der Service Level

Das TI-ITSM-System ermittelt alle übergreifenden organisatorischen Service
Level automatisch während der TI-ITSM-Prozessbearbeitung. Alle anderen Service
Level, z.B. technische Service Level oder lokale organisatorische Service Level
werden vom TI-ITSM-Teilnehmer gemessen und an das TI-ITSM-System übermittelt.

Damit wird sichergestellt, dass alle durch einen TI-ITSM-Teilnehmer zu
erbringenden Service Level, übergreifend und lokal sowie technisch und
organisatorisch, zentral dokumentiert werden.

**GS-A_4100 - Messung der Service Level**

TI-ITSM-Teilnehmer MÜSSEN alle nicht durch das TI-ITSM-System gemessenen
Service Level gemäß [gemKPT_Betr] bzw. [gemSpec_Perf] messen. **[\<=]**

### 9.2.2 Bereitstellung des Service Level Reports

Jeder TI-ITSM-Teilnehmer muss die von ihm zu verantwortenden Service Level
prüfen, ggf. erfassen, kommentieren und für die weitere Verarbeitung im
TI-ITSM-System freigeben.

Der Gesamtverantwortliche TI wird für die Erfassung der lokalen Messergebnisse
eine Schnittstelle im TI-ITSM-System zur Verfügung stellen.

**GS-A_5604 - Bewertung der Messergebnisse**

TI-ITSM-Teilnehmer MÜSSEN in allen Fällen einer Untererfüllung der gemessenen
Werte von den Zielwerten eine Begründung für die Untererfüllung sowie eine
Information zu getroffenen und geplanten Maßnahmen angeben. **[\<=]**

**GS-A_4101 - Übermittlung der Service Level Messergebnisse**

TI-ITSM-Teilnehmer MÜSSEN die Service Level Messergebnisse an die durch den
Gesamtverantwortlichen TI benannte Kommunikationsschnittstelle übermitteln.
**[\<=]**

### 9.2.3 Teilnahme am Service Review

Service Reviews werden zur Feststellung von notwendigen Optimierungsaktivitäten
–sowohl auf Ebene der Vorgaben als auch auf Ebene der Umsetzung –
durchgeführt. Service Reviews erfolgen bei Bedarf und werden durch den
Gesamtverantwortlichen TI einberufen. Die Art der Durchführung des Service
Reviews wird durch den Gesamtverantwortlichen TI festgelegt (bspw.
Telefonkonferenz, E-Mail).

TI-ITSM-Teilnehmer, die Optimierungsaktivitäten eigenverantwortlich definiert
haben, erfassen diese im Service Level Report.

**GS-A_4397 - Teilnahme am Service Review**

TI-ITSM-TeilnehmerMÜSSEN am Service Review teilnehmen und die bilateral
vereinbarten Optimierungsaktivitäten umsetzen. **[\<=]**

Sollten die im Service Review zwischen TI-ITSM-Teilnehmer und
Gesamtverantwortlichen TI vereinbarten Optimierungen keinen belastbaren Erfolg
zeigen, so steht dem Gesamtverantwortlichen TI als weitere Option die
Durchführung von Audits gem. GS-A_4855 offen. Damit sollen erkannte
prozessuale Defizite – insbesondere in den Prozessen Incident, Problem,
Request Fulfillment und Change Management – sowie technische Defizite
(Performance Zielwerte der von TI-ITSM-Teilnehmern verantworteten TI-Produkte)
beseitigt werden.

### 10 Performance Management

Das Performance Management der TI umfasst die ITIL-Prozesse Capacity Management
und Availability Management. Es verfolgt das Ziel, jederzeit adäquate
Kapazitäten und ausreichende Verfügbarkeiten im Sinne eines angemessenen
technischen Leistungsvermögens der TI unter Einhaltung der wirtschaftlichen
Verhältnismäßigkeit zu gewährleisten. Letzteres beinhaltet beispielsweise
den Abbau von festgestellten oder absehbaren Überkapazitäten und die
Berücksichtigung des Ressourcenverbrauchs, der zur Leistungserbringung
erforderlich ist.

Im Rahmen des Performance-Managements werden auch Entwicklungen aufgezeigt,
Trends extrapoliert und Prognosen zu Verfügbarkeits- und
Kapazitätsanforderungen erstellt. Letztlich sollen aus diesen Erkenntnissen
Maßnahmen abgeleitet, geplant, durchgeführt und überwacht werden, welche die
Sicherstellung des oben genannten Ziels gewährleisten sollen.

Zur Unterstützung dieses Ziels, müssen TI-ITSM-Teilnehmer zunächst
Performance-Messungen auf den von ihnen verantworteten TI-relevanten Systemen
durchführen und die Ergebnisse an den Gesamtverantwortlichen TI berichten. Im
Weiteren sind die TI-ITSM-Teilnehmer auch zur Entwicklung und Definition von
Maßnahmen zur Optimierung von Verfügbarkeit und Kapazität verpflichtet,
wobei die TI-weiten Performance-Analysen und Service-Design-Optimierungen durch
den Gesamtverantwortlichen TI vorgenommen bzw. initiiert werden. Interne
Optimierungsmaßnahmen der TI-ITSM-Teilnehmer sind daher nicht Bestandteil der
übergreifenden Richtlinien.

Im Folgenden werden ausschließlich Anforderungen an TI-ITSM-Teilnehmer
definiert, die den Betrieb von zentralen Produkten oder Fachanwendungen in der
TI verantworten. Für dezentrale Produkte werden hier keine
Performance-Anforderungen definiert.

### 10.1 Begriffsbestimmungen

### 10.1.1 Performance

Der Begriff „Performance“ wird im Folgenden gemäß [gemSpec_Perf]
verwendet. Die Performance wird dabei durch die in [gemKPT_Betr] definierten
Kenngrößen repräsentiert, welche die Dimensionen Verfügbarkeit, Durchsatz
und Bearbeitungszeit abdecken.

### 10.2 Prozessdurchführung Performance Management

### 10.2.1 Performance messen

Zur Zielerreichung des Performance-Managements der TI müssen TI-ITSM-Teilnehmer
Performance-Messungen durchführen und die Ergebnisse berichten.

Die Messergebnisse dienen dabei im Wesentlichen

 ---> UL

Die Messungen erfolgen durch den TI-ITSM-Teilnehmer innerhalb der von ihm
verantworteten TI-relevanten Systeme und Prozesse basierend auf den Vorgaben
der [gemSpec_Perf].

**A_18363 - Berechnung von Performance-Kenngrößen aus Rohdaten**

Zur Berechnung der in [gemSpec_Perf] definierten Performance-Kenngrößen aus
den Performance-Rohdaten auf Service-Ebene MUSS der TI-ITSM-Teilnehmer den
Gesamtverantwortlichen TI  bei der Festlegung der Bildungsregeln unterstützen
und mit dem Gesamtverantwortlichen TI vereinbaren. **[\<=]**

Festlegung und Abstimmung müssen rechtzeitig vor Aufnahme des Betriebs eines
Produktes in einer Betriebsumgebung des TI-ITSM-Teilnehmers im Rahmen des
Anbieterzulassungsverfahrens erfolgen, damit die Bereitstellung der Werte der
definierten Performance-Kenngrößen für die Betriebsüberwachung und im
Service Level Reporting vor Aufnahme des Wirkbetriebes erfolgen kann.

### 10.2.2 Performance reporten

Das TI-ITSM-System wird eine Möglichkeit zum Datenupload bereitstellen.

<table><tr><td>
Geplant ist, dass das TI-ITSM-System eine Schnittstelle zum Datenupload
bereitstellen wird. Sollte sich im Laufe des Projektes herausstellen, dass dies
nicht möglich sein wird, gelten die Anforderungen zur CSV-Datenübermittlung
gemäß Kapitel 13.

</td></tr></table>

**A_18236-01 - Übermittlung von Performance-Reports**

TI-ITSM-Teilnehmer, die gemäß Tab_gemKPT_Betr_Performance-Kenngroessen]
technische Performance-Kenngrößen in Performance-Reports liefern, MÜSSEN
den Performance-Report einmal im Monat an den vom Gesamtverantwortlichen der TI
angegebenen Endpunkt übermitteln und dabei die GS-A_5248 beachten. Der
Berichtszeitraum umfasst einen vollen Kalendermonat. **[\<=]**

**A_18237 - Lieferung von Performance-Rohdaten-Reports**

TI-ITSM-Teilnehmer, die gemäß [gemSpec_Perf#2.5] technische
Performance-Kenngrößen in Rohdaten-Performance-Berichten
(Performance-Protokoll und Datei zur Selbstauskunft) liefern, MÜSSEN die für
den Berichtszeitraum zu liefernden Berichte an den in [gemSpec_Perf]
angegebenen Endpunkt liefern. Der Berichtszeitraum umfasst einen vollen
Kalendermonat. **[\<=]**

Der Endpunkt wird vom GTI in der Wissensdatenbank bekannt gegeben. Bei
Änderungen des Endpunktes bzw. bei Wechsel des Verfahrens (Ablösung von
E-Mail) werden die TI-ITSM-Teilnehmer mit angemessenem zeitlichen Vorlauf
informiert.

**A_19869 - Performance - Rohdaten-Performance-Berichte - zu liefernde Berichte
der TI-ITSM-Teilnehmer**

TI-ITSM-Teilnehmer, die Rohdaten-Performance-Berichte übermitteln, MÜSSEN
jeweils zu jedem separat konfigurierbaren Berichtsintervall zwei Dateien
senden:- einen "Rohdaten-Performance-Bericht" mit den zu liefernden
Rohdaten[gemSpec_Perf#A_17755,A_17671, A_17668, A_19733]und- eine Datei zur
"Selbstauskunft" gemäß [gemSpec_OM#GS-A_4543] im XML-Format
[ProductInformation.xsd].Beide Dateien MÜSSEN separat an die
Betriebsdatenerfassung gemäß gemSpec_SST_LD_BD an die Schnittstelle
I_OpsData_Update gesandt werden. **[\<=]**

**GS-A_4106-02 - Reportinhalte des Performance-Reports**

TI-ITSM-Teilnehmer MÜSSEN die Ergebnisse ihrer Performance-Messungen nach
folgendem Schema (die Reihenfolge ist verbindlich) an den
Gesamtverantwortlichen TI übermitteln.

Tabelle10: Tab_Betr_TIP_003 PERF – Reportinhalte von Performance Messungen

<table><tr><th>
#

</th><th>
Spaltenname

</th><th>
Beschreibung

</th><th>
Typ

</th><th>
Beispiel

</th></tr><tr><td>
1

</td><td>
Teilnehmer ID

</td><td>
ID des TI-ITSM-Teilnehmers bzw. weitere Beteiligte im Betrieb der TI

</td><td>
[String]/

</td><td>
</td></tr><tr><td>
2

</td><td>
Produktkürzel

</td><td>
Produktkürzel gemäß [gemSpec_OM]

</td><td>
[String]/

</td><td>
</td></tr><tr><td>
3

</td><td>
Betriebsumgebung

</td><td>
Gibt die Betriebsumgebung an, in welcher das Produkt im Messintervall gemessen
wurde. Werden Messwerte für Produkte bzw. Produktbestandteile (z.B. SZZP)
geliefert, so ist die Betriebsumgebung „Alle“ zu verwenden

</td><td>
[Auswahlfeld], (RU), (TU), (PU), (Alle)

</td><td>
Alle

</td></tr><tr><td>
4

</td><td>
Performance Kenngroesse

</td><td>
Ausgeprägter Bezeichner der Performance-Kenngröße gemäß
Tab_gemKPT_Betr_Performance-Kenngroessen

</td><td>
[String]

</td><td>
PDT03-S06-D1-G01-Z06

</td></tr><tr><td>
5

</td><td>
Messwert

</td><td>
ermittelter Wert aus der Performance-Messung für das angegebene Messintervall
[Auswertungsstart / -ende] bzw. Zeitstempel

</td><td>
[Integer] oder  
[Date]

</td><td>
</td></tr><tr><td>
6

</td><td>
Messgroesse

</td><td>
Messgröße des Performance-Wertes gemäß Tab_ gemKPT_Betr_Performance-Groessen

</td><td>
[String]

</td><td>
</td></tr><tr><td>
7

</td><td>
Auswertungsstart

</td><td>
Zeitpunkt, ab dem die Messung für den Wert gestartet ist

</td><td>
[Date]/

</td><td>
</td></tr><tr><td>
8

</td><td>
Auswertungsende

</td><td>
Zeitpunkt, an dem die Messung für den Wert beendet wurde

</td><td>
[Date]/

</td><td>
</td></tr></table>

**[\<=]**

**A_17735 - Rohdatenreporting**

Anbieter des ePA-Aktensystems (inkl. Schlüsselgenerierungsdienst),
Schlüsselgenerierungsdienstes der zentralen Zone, Signaturdienstes,
Verzeichnisdienstes, VPN-Zugangsdienstes, KOM-LE, X.509-TSP (HBA, SMC-B, eGK)
sowie Fachdienstbetreiber VSDM MÜSSEN Rohdaten der Performancemessungen
entsprechend [gemSpec_Perf] an die von dem Gesamtverantwortlichen TI benannte
Schnittstelle (gemäß gemSpec_SST_LD_BD) senden. Damit entfällt für sie das
konsolidierte Performance-Reporting. **[\<=]**

### 10.2.3 Performance bewerten, planen und steuern

Die Performance-Bewertung beinhaltet die Feststellung, Überwachung und Analyse
der definierten Kenngrößen und Parameter. Des Weiteren bildet sie die
Grundlage für die Planung einer rechtzeitigen Bereitstellung der notwendigen
Kapazitäten und Verfügbarkeiten in der TI-Infrastruktur. Hierbei werden
sowohl zukünftige Leistungsanforderungen und -angebote als auch Änderung im
Nutzungsverhalten und von technischen Rahmenbedingungen berücksichtigt.

**GS-A_5606 - Unterstützung bei Definition von Kapazitätsanforderungen**

TI-ITSM-Teilnehmer MÜSSEN auf Anforderung des Gesamtverantwortlichen TI an
Gesprächen zur Bewertung der aktuellen Kapazitätssituation teilnehmen. Sie
MÜSSEN den Gesamtverantwortlichen TI bei der Entwicklung und Definition von
zukünftigen Kapazitätsanforderungen unterstützen. **[\<=]**

Die eigentliche Entwicklung von Maßnahmen bei festgestellten und
diagnostizierten Anforderungsbedarfen und deren Nachverfolgung erfolgt in den
jeweils zutreffenden ITSM-Prozessen und werden dort dokumentiert (z. B.
Problem-Management, Change-Management).

### 10.2.4 Service Monitoring (finale Lösung)

Mit Einführung der finalen Lösung des Service Monitoring der TI wird die
Neuausrichtung der TI-Betriebssteuerung auch systemtechnisch sichtbar. Mit
Hilfe des neuen Systems werden einerseits Verfügbarkeit und Antwortzeit von
TI-Systemen und Services bzw. Dienste gemessen und überwacht, andererseits
berichten die TI-ITSM-Teilnehmer ihre Performancedaten ebenfalls zukünftig
ausschließlich an dieses System. Neben der physikalischen Erreichbarkeit
werden vom System selbst auch qualifizierte Anfragen an die Dienste gestellt
und aus den Antworten dieser wird (automatisiert) auf den Servicezustand
geschlossen.

Die gematik wird auf Basis dieser Auswertungen jederzeit zum aktuellen Status
der TI aussagefähig sein und kann auf Basis der Kenntnis um den äußeren
Gesamtstatus der TI ggf. notwendige Maßnahmen einleiten. Das Service
Monitoring beinhaltet damit sämtliche Themen des hier definierten Performance
Managements. Eine Überwachung der Systeme und Services, die sich in der
Eigenverantwortlichkeit der TI-ITSM-Teilnehmer befinden, findet allerdings
nicht statt.

Nutzer des Service Monitoring Systems sind alle am Betrieb der TI Beteiligten
(gemäß Definition dieser Richtlinien [gemRL_Betr_TI]). Anwender
(Versicherte/Leistungserbringer) haben keinen direkten Zugriff. Die Regelung
des Zugriffs auf die Darstellungseinheit des Service Monitoring Systems
(Live-Dashboard) erfolgt über ein Rollen- und Berechtigungskonzept. Auf der
Darstellungseinheit werden z. B. die Auswirkungen eines festgestellten
Servicedefizites angezeigt. Weiterhin besteht die Möglichkeit zur Anbindung
von Drittsystemen bei den TI-ITSM-Teilnehmern mittels Schnittstelle gemäß den
definierten Berechtigungen. Auf diese Weise können Meldungen über aktuelle
Systemzustände bzw. Systemdefizite der betroffenen Dienste automatisiert auch
auf Drittsysteme übertragen werden.

Nach Einführung des Service Monitorings wird das monatliche Reporting von
Performance-Daten (Verfügbarkeit, Durchsatz, Bearbeitungszeit) der
TI-ITSM-Teilnehmer an den Gesamtverantwortlichen der TI angepasst mit dem Ziel
einer teilweisen oder vollständigen Ersetzung. Bis zu diesem Zeitpunkt
behalten die bestehenden Anforderungen und Vorgehensweisen Gültigkeit. Auch
wird mit der Einführung dieses Systems die Störungsampel abgelöst. Welche
betrieblichen Anforderungen mit der Einführung des Service Monitorings der TI
stattdessen im Rahmen dieser Richtlinien bzgl. Performance-Management
zukünftig definiert werden, ist zum jetzigen Zeitpunkt noch nicht geklärt.

### 11 Servicekatalog Management

Der Servicekatalog Management der TI regelt, wie Servicekataloge der
TI-ITSM-Teilnehmer mit dem Gesamtverantwortlichen TI vereinbart und für andere
TI-ITSM-Teilnehmer bereitgestellt werden. Ziel ist es, die notwendige
Transparenz für alle TI-ITSM-Teilnehmer über in der TI angebotene Services
und die Beschaffungskonditionen zu schaffen.

### 11.1 Begriffsbestimmungen

### 11.1.1 Servicekatalog

Der Servicekatalog enthält alle von einem TI-ITSM-Teilnehmer angebotenen TI
Services mit Angabe der dazugehörenden Servicekomponenten. Es wird
dargestellt, zu welchen Konditionen der jeweilige Service geliefert wird. Der
Servicekatalog wird im Rahmen des Servicekatalog-Managements vereinbart und
anderen TI-ITSM-Teilnehmern über das TI-ITSM-System bereitgestellt.

### 11.1.2 Serviceverzeichnis

Alle Servicekataloge aller TI-ITSM-Teilnehmer werden zentral im
Service-Verzeichnis des TI-ITSM-Systems aufgeführt.

### 11.2 Prozessdurchführung Servicekatalog Management

### 11.2.1 Definition der angebotenen Services

Der TI-ITSM-Teilnehmer erfasst seine angebotenen Services im TI-ITSM-System. Die
Gesamtheit der angebotenen Services ergibt den Servicekatalog des
TI-ITSM-Teilnehmers.

**GS-A_5607 - Inhalte eines Servicekataloges der angebotenen TI-Services**

TI-ITSM-Teilnehmer MÜSSEN alle von ihnen angebotenen TI-Services und
-qualitäten gegenüber anderen TI-ITSM-Teilnehmern in einem Servicekatalog im
TI-ITSM-System dokumentieren und dabei mindestens folgende Angaben beifügen:

 ---> OL

**[\<=]**

Zusätzlich muss der TI-ITSM-Teilnehmer über Vereinbarungen mit anderen
TI-ITSM-Teilnehmern sicherstellen, dass alle Voraussetzungen für die
Erbringung seiner eigenen Services gegeben sind.

### 11.2.2 Servicekatalog freigeben

Der Gesamtverantwortliche TI wird die Servicedefinition und -konditionen prüfen
und den Servicekatalog in Abstimmung mit dem TI-ITSM-Teilnehmer im
TI-ITSM-System hinterlegen.

**GS-A_5609 - Abnahme des Servicekataloges**

TI-ITSM-Teilnehmer MÜSSEN alle von ihnen angebotenen Services in einem
Business-Servicekatalog mit dem Gesamtverantwortlichen TI vereinbaren. **[\<=]**

Durch die Abnahme werden sie berechtigten TI-ITSM-Teilnehmern zum Abruf über
das TI-ITSM-System zur Verfügung gestellt.

### 12 Notfall Management

Das Notfall Management der TI stellt sicher, dass

 ---> UL

Der primäre Fokus des Notfall Managements in den Übergreifenden Richtlinien
zum Betrieb der TI liegt in Ausprägung der Vorsorge und Bewältigung von
TI-Notfällen durch TI-ITSM-Teilnehmer.

Art und Umfang der Notfallvorsorge und -bewältigung von lokalen Notfällen
durch die TI-ITSM-Teilnehmer sind nicht Gegenstand dieser Richtlinien. Ein
lokales Notfallmanagement wird vorausgesetzt. Anforderungen an das lokale
Notfallmanagement sind [gemSpec_DS_Anbieter] zu entnehmen.

Die operative Behebung von TI-Notfällen obliegt grundsätzlich den
TI-ITSM-Teilnehmern, wobei der Gesamtverantwortliche TI eine zentrale
koordinierende Rolle im Rahmen der Bewältigung einnehmen kann.

### 12.1 Begriffsbestimmungen

### 12.1.1 Notfall

Gemäß dem [BSI 100-4] wird unter Notfall ein länger andauernder Ausfall von
Prozessen oder Ressourcen mit hohem oder sehr hohem Schaden verstanden. Die
Verfügbarkeit der entsprechenden Prozesse oder Ressourcen kann innerhalb einer
geforderten Zeit nicht wieder hergestellt werden. Notfälle können nicht mehr
im allgemeinen Tagesgeschäft abgewickelt werden, sondern erfordern eine
gesonderte Notfallbewältigungsorganisation.

### 12.1.2 Lokaler Notfall

Ein lokaler Notfall beschreibt ein Schadensereignis der Produkte mit lokal
ausgeprägten Auswirkungen. Lokale Notfälle werden durch TI-ITSM-Teilnehmer
bewältigt und erfordern keine Koordination durch den Gesamtverantwortlichen
TI. TI-ITSM-Teilnehmer müssen den Gesamtverantwortlichen TI über das
Schadenereignis unverzüglich gemäß den Vorgaben der [gemSpec_DS_Anbieter]
informieren.

### 12.1.3 TI-Notfall

Ein TI-Notfall beschreibt ein übergreifendes Schadensereignis, welches nicht
allein durch die lokale Notfallorganisation von betroffenen TI-ITSM-Teilnehmern
zu bewältigen ist oder welches schwerwiegende Auswirkungen auf Services bzw.
Produkte von anderen TI-ITSM-Teilnehmern hat. Ein TI-Notfall hebt sich
insbesondere dadurch hervor, dass die TI bzw. ein TI-Service in ihrer
ganzheitlichen Funktion (auch im Kontext der Sicherheit) gestört oder
gefährdet ist.

Der TI-Notfall besitzt die höchste Eskalationsstufe und deckt auch das
Verhalten in Krisen und Katastrophensituationen ab. Der Gesamtverantwortliche
TI nimmt in TI-Notfällen eine koordinierendeRollewahr.

### 12.1.4 TI-Notfallvorsorge

Gemäß dem [BSI 100-4] zählen zur TI-Notfallvorsorge alle organisatorischen
und konzeptionellen Aspekte sowie alle proaktiven Maßnahmen und Tätigkeiten
des Notfallmanagements. Dazu zählen:

 ---> UL

Die Ausgestaltung der Vorsorgemaßnahmen sollte sich an der Kritikalität des
Dienstes orientieren.

### 12.1.5 TI-Notfallmaßnahme

Als TI-Notfallmaßnahme gilt jede Handlung, welche die Auswirkung eines
TI-Notfalls eindämmen, schmälern oder aufheben kann. Die Maßnahme bietet in
der Regel keine nachhaltige Beseitigung der Ursache des TI-Notfalls, kann aber
einen Notbetrieb ermöglichen bzw. in Art und Ausprägung die
TI-Notfallbewältigung erleichtern oder ermöglichen.

### 12.1.6 Notbetrieb

Als Notbetrieb wird der Betriebszustand bezeichnet, welcher durch eine
erfolgreiche Maßnahme innerhalb der TI-Notfallbewältigung die Grundfunktionen
des Dienstes zwar aufrechterhält, diese jedoch entweder noch nicht nachhaltig
stabilisiert sind und/oder noch nicht in der gewünschten Güte geleistet
werden können (bspw. längere Antwortzeiten, Fehlen einer Redundanz, Verzicht
auf einzelne Features etc.). Wichtigstes Merkmal des Notbetriebes ist dabei,
dass betroffene Produkte keine schädigenden Wechselwirkungen mit anderen
TI-Produkten mehr verursachen. Mit der erfolgreichen Aufnahme des Notbetriebs
beginnt die Wiederherstellung.

### 12.1.7 TI-Notfallbewältigung

Bei der TI-Notfallbewältigung handelt es sich um das operative Agieren
innerhalb des in der TI-Notfallvorsorge festgelegten Rahmens. Das Ziel der
TI-Notfallbewältigung ist das Fortführen des vom TI-Notfall betroffenen
Services, gegebenenfalls auch mit Einschränkungen sowie die vollständige
Wiederherstellung des Services im vorgegebenen Leistungsumfang und
Sicherheitsmerkmalen.

### 12.1.8 Emergency Management Committee (EMC)

Das Emergency Management Committee (EMC) ist das Führungsinstrument im
TI-Notfall. Es ist zeitlich befristet aktiv und ist für die Koordination der
TI-Notfallbewältigung verantwortlich.

Das EMC ist im Rahmen der geltenden betrieblichen und rechtlichen Regelungen
gegenüber allen Rollen der Notfallorganisation im Rahmen der
TI-Notfallbewältigung weisungsbefugt. Es befasst sich ausschließlich mit dem
vorliegenden TI-Notfall und den davon betroffenen Bereichen.

### 12.1.9 Lösungsteam

Das Lösungsteam ist ein durch das EMC einberufenes Team von Fachexperten der
durch den TI-Notfall unmittelbar betroffenen oder gefährdeten Dienste der TI.
Aufgabe des Lösungsteams ist das Identifizieren und Bewerten, sowie (nach
erfolgter Freigabe durch das EMC) das Durchführen von Maßnahmen der
TI-Notfallbewältigung. Das Lösungsteam kann jederzeit während der
TI-Notfallbewältigung hinsichtlich der Anforderungen umbesetzt werden und wird
spätestens mit der Deeskalation des TI-Notfalls aufgelöst.

### 12.2 Prozessdurchführung Notfallvorsorge

Die Einhaltung der Anforderungen zur Notfallvorsorge wird regelmäßig im Rahmen
der Auditierung geprüft und nachgewiesen.

### 12.2.1 Analyse der Auswirkungen möglicher Notfälle der Produktinstanzen

Der Serviceverantwortliche wird ein Notfallvorsorgekonzept erstellen. Das Ziel
des Notfallvorsorgekonzepts ist, die TI-Notfälle in ihrer Auswirkung auf die
Erbringung der TI-Services zu analysieren und vorbeugend proaktive Maßnahmen
zu entwickeln.

**GS-A_4121 - Analyse Auswirkungen möglicher Schadensereignisse auf Sicherheit
und Funktion der TI-Services**

TI-ITSM-Teilnehmer MÜSSEN die Auswirkungen möglicher Schadensereignisse auf
von ihnen verantworteten TI-Services analysieren und bewerten. Die
Auswirkungsanalyse MUSS mit mindestens folgenden Vorgaben erstellt werden:

 ---> UL

**[\<=]**

### 12.2.2 Entwicklung und Pflege der Notfallvorsorgedokumentation

**GS-A_4123 - Entwicklung und Pflege der TI-Notfallvorsorgedokumentation**

TI-ITSM-Teilnehmer MÜSSEN eine TI-Notfallvorsorgedokumentation, welche die
Ergebnisse der Auswirkungsanalyse sowie Vorkehrungen zur TI-Notfallvorsorge des
Serviceverantwortlichen enthält, entwickeln und pflegen. In der
TI-Notfallvorsorgedokumentation sind die Aktivitäten festgelegt, die bei
Eintritt eines TI-Notfalls durchzuführen sind. **[\<=]**

### 12.2.3 Umsetzung Vorkehrungen zur Notfallvorsorge

**GS-A_4124 - Umsetzung Vorkehrungen zur TI-Notfallvorsorge**

TI-ITSM-TeilnehmerMÜSSEN die erarbeiteten Vorkehrungen zur TI-Notfallvorsorge
umsetzen. **[\<=]**

### 12.3 Prozessdurchführung TI-Notfallbewältigung

### 12.3.1 TI-Notfallerkennung

Die TI-Notfallerkennung ist eine operative Aufgabe des Incident Managements. Ein
Vorfall wird gemäß GS-A_4125 als TI-Notfall klassifiziert und an das Notfall
Management übergeben. Außerdem wird das TI-Notfall-Logbuch gemäß GS-A_4137
angelegt und fortgeschrieben.

### 12.3.2 Eskalation TI-Notfälle

**GS-A_4126 - Eskalation TI-Notfälle**

TI-ITSM-Teilnehmer MÜSSEN erkannte TI-Notfälle unverzüglich an den
Gesamtverantwortlichen TI eskalieren. Eine Meldung an den
Gesamtverantwortlichen TI MUSS im Sinne einer umgehenden und persönlichen
Benachrichtigung erfolgen. **[\<=]**

Konkrete Handlungsanweisungen zur TI-Notfall-Meldung werden in der
Wissensdatenbank zur Verfügung gestellt und aktuell gehalten.

### 12.3.3 Sofortmaßnahmen TI-Notfälle

**GS-A_4127 - Sofortmaßnahmen TI-Notfälle**

TI-ITSM-Teilnehmer, deren Dienste von einem TI-Notfall betroffen sind, MÜSSEN
entsprechende Maßnahmen einleiten, mit dem Ziel die Auswirkungen der
TI-Notfälle eigenständig zu reduzieren oder einzuschränken. **[\<=]**

### 12.3.4 Bewältigung TI-Notfälle

**GS-A_4128 - Bewältigung der TI-Notfälle**

TI-ITSM-TeilnehmerMÜSSEN vom EMC autorisierte TI-Notfallmaßnahmen zur
Bewältigung von TI-Notfällen im eigenen Verantwortungsbereich umsetzen. **[\<=]**

**GS-A_4129 - Unterstützung bei TI-Notfällen**

TI-ITSM-Teilnehmer MÜSSEN bei der Bewältigung sowie Koordination der
TI-Notfälle den Gesamtverantwortlichen TI oder andere TI-ITSM-Teilnehmer im
erforderlichen Umfang unterstützen. **[\<=]**

### 12.3.5 Koordination der TI-Notfallbewältigung durch den Gesamtverantwortlichen TI

### 12.3.5.1 Notfallbeurteilung

Nachdem die TI-ITSM-Teilnehmer einen möglichen TI-Notfall erkanntund an den
Gesamtverantwortlichen TI gemeldet haben, wird der Gesamtverantwortliche TI die
zu erwartende Auswirkung des TI-Notfalls überprüfen. Im Falle einer negativen
Notfallbewertung (keine zu erwartende Auswirkung, Notfallkriterien sind
zwischenzeitlich nicht mehr erfüllt etc.) erfolgt die Zurückweisung des
TI-Notfalls. Der Vorfall wird als Incident im regulären Betriebsprozess
behandelt.

### 12.3.5.2 Notfallfeststellung

DerGesamtverantwortliche TIwird im Falle eines TI-Notfalls einen formellen
Ausruf des TI-Notfalls durchführen.

### 12.3.5.3 Einberufung des Emergency Management Committee (EMC)

Nach der Notfallbestätigungberuft der Gesamtverantwortliche TI dasEMC ein. Die
Zusammensetzung des EMC basiert auf Art und Umfang des vorliegenden TI-Notfalls
und kann ggf. fallspezifisch erweitert werden.

**GS-A_4130 - Festlegung der Schnittstellen des EMC**

Prozessbeteiligte TI-ITSM-Teilnehmer MÜSSEN die vom Gesamtverantwortlichen TI
bereitgestellten Schnittstellen im Rahmen der Einberufung des EMC nutzen.
**[\<=]**

Damit wird eine sofortige Reaktion auf Anfragen sichergestellt. Die
Dokumentation erfolgt außerhalb des TI-ITSM-Systems.

Konkrete Informationen zum EMC werden in der Wissensdatenbank zur Verfügung
gestellt und aktuell gehalten.

### 12.3.5.4 Zusammenstellung des Lösungsteams

Das Lösungsteam wird durch das EMC eingesetzt. Die Zusammensetzung des
Lösungsteams kann im Laufe der TI-Notfallbewältigung durch das EMC verändert
werden.

### 12.3.5.5 Durchführung der Notfallmaßnahmen

Das Lösungsteam wird nach Verifikation der Ursachen und des Umfangs des
TI-Notfalls geeignete TI-Notfallmaßnahmen identifizieren. Diese werden im EMC
hinsichtlich Aufwand, Durchführbarkeit und Wirkung bewertet und freigegeben.

Die freigegebenen Maßnahmen werden durchgeführt und deren Erfolg geprüft.

### 12.3.5.6 Notfalldeeskalation

Nach erfolgreich durchgeführten TI-Notfallmaßnahmen wird
derGesamtverantwortliche TI die Beseitigung des TI-Notfalls bzw. die Erreichung
des Notbetriebsbestätigen und den TI-Notfall formell deeskalieren, also den
TI-Notfall als beendet erklären. Damit ist auch das EMC aufgelöst und es
endet die Dokumentation in Form des TI-Notfall-Logbuchs. Das TI-Notfall-Logbuch
wird direkt im Anschluss an die Auflösung in elektronischer Form an die
Teilnehmer des EMC und des Lösungsteams verteilt.

### 12.3.6 Wiederherstellung

DerGesamtverantwortliche TIwird im Anschluss der Notfalldeeskalation die
Wiederherstellung veranlassen. Die Wiederherstellung hat zum Ziel, den
Betriebszustand zu erreichen, welcher vor Eintreten des TI-Notfalls bestand.
Ggf. ergriffene Sofortmaßnahmen im Sinne von Interimslösungen werden in
diesem Zusammenhang geplant zurückgenommen.

Die erfolgreiche Wiederherstellung wird in Form eines
Wiederherstellungsberichtes an die Teilnehmer des EMC und des Lösungsteams
gemeldet.

**GS-A_4132 - Durchführung der Wiederherstellung und TI-Notfällen**

TI-ITSM-Teilnehmer MÜSSEN alle Aktivitäten, welche der Wiedererreichung und
Stabilisierung des Leistungsumfangs im eigenen Verantwortungsbereich dienen,
durchführen und dokumentieren. **[\<=]**

### 12.3.7 Nachbearbeitung/Notfallauswertung

**GS-A_4134 - Auswertungen von TI-Notfällen**

TI-ITSM-Teilnehmer MÜSSEN nach Abschluss der TI-Notfallbewältigung den
TI-Notfall hinsichtlich seiner Ursache, Auswirkung, Dauer, Wahrscheinlichkeit
eines erneuten Eintritts und der Angemessenheit der ergriffenen Maßnahmen zur
TI-Notfallbewältigung auswerten.Die Auswertungsergebnisse sind zusammen mit
TI-Notfall-Logbuch und Wiederherstellungsbericht,an den Gesamtverantwortlichen
TI zu übergeben. **[\<=]**

DerGesamtverantwortliche TI wird nach Bewältigung des eingetretenen TI-Notfalls
eine Auswertung vornehmen. Der Gesamtverantwortliche TI wird dabei untersuchen,
ob die im Rahmen der Notfallplanung festgelegtenAbläufe und Maßnahmen für
die Bewältigung des TI-Notfalls geeignet und ausreichend und ob weitere von
ihm getroffenen Entscheidungen und Maßnahmen angemessen für eine effiziente
TI-Notfallbewältigung waren. Die daraus gewonnenen Erkenntnisse werden für
die Validierung der Notfallvorsorgemaßnahmen bzw. der Notfallpläne
herangezogen. Bei Bedarf werden Verbesserungsmaßnahmen durchgeführt.

### 12.4 Informationspflichten

**GS-A_4136 - Statusinformation bei TI-Notfällen**

TI-ITSM-Teilnehmer, die von einem TI-Notfall betroffen sind, MÜSSEN im Rahmen
der TI-Notfallbewältigung den Gesamtverantwortlichen TI ständig über den
aktuellen Status der Durchführung der TI-Notfallmaßnahmen informieren.
**[\<=]**

TI-ITSM-Teilnehmer werden im Rahmen der Teilnahme am EMC mit den notwendigen
Informationen zur TI-Notfallbewältigung versorgt.

### 12.5 Dokumentation

### 12.5.1 TI-Notfall-Logbuch

**GS-A_4137 - Dokumentation im TI-Notfall-Logbuch**

TI-ITSM-Teilnehmer MÜSSEN zu jedem TI-Notfall ein TI-Notfall-Logbuch erstellen.

TI-ITSM-Teilnehmer MÜSSEN im Rahmen der TI-Notfallbewältigung im eigenen
Verantwortungsbereich folgende Angaben im TI-Notfall-Logbuch dokumentieren:

 ---> UL

TI-ITSM-Teilnehmer MÜSSEN dabei das TI-Notfall-Logbuch in den Phasen vom
Bekanntwerden des Notfalls bis zur Notfalldeeskalation ständig aktualisieren. **[\<=]**

### 12.5.2 Wiederherstellungsbericht

**GS-A_4138 - Erstellung des Wiederherstellungsberichts nach TI-Notfällen**

TI-ITSM-Teilnehmer MÜSSEN zu jeder Wiederherstellung in der
TI-Notfallbewältigung einen Wiederherstellungsbericht erstellen.

TI-ITSM-Teilnehmer MÜSSEN einen Wiederherstellungsbericht mit allen
durchgeführten Aktionen und Änderungen sowie Angaben zu Erfolg und Misserfolg
jeder einzelnen Aktivität im eigenen Verantwortungsbereich, welche im Rahmen
der Wiederherstellung durchgeführt wurden, erstellen. **[\<=]**

### 13 Vorschriften für CSV-Reporting

**GS-A_5608 - Übermittlung von CSV-Dateien**

Bei der Übermittlung von CSV-Dateien an den Gesamtverantwortlichen TI sind
folgende Regelungen zu beachten:

 ---> UL

**[\<=]**

**GS-A_5248 - Konventionen zur Struktur von Prozessdaten**

 ---> OL

TI-ITSM-Teilnehmer MÜSSEN die Struktur der CSV-Dateien für Statusinformationen
und Eskalationen sowie der Prozesskommunikation nach den Vorgaben aus [RFC4180]
und den nachfolgenden Konkretisierungen bauen:

 ---> UL

 ---> OL

**[\<=]**

**GS-A_5249 - Reservierte Zeichen in den Prozessdaten**

TI-ITSM-Teilnehmer MÜSSEN die in Tab_Betr_TIP_049 reservierte Zeichen
Ersetzungstabelle benannten Zeichenketten in den [String] Basisfeldtypen der zu
übermittelnden Prozessdaten der Incident- und Problemdokumentationen vermeiden
und entsprechend ersetzen. **[\<=]**

<table><tr><th>
reservierte Zeichen

</th><th>
Muss ersetzt werden durch

</th><th>
Begründung

</th></tr><tr><td>
#

</td><td>
\<Hash\>

</td><td>
Reserviertes Zeichen, für die Feldtrennung. Sie müssen ersetzt werden durch
den Text \<Hash\>.

</td></tr><tr><td>
Zeilenumbruch

</td><td>
\<br\>

</td><td>
Zeilenumbrüche in Inhaltsfeldern erhöhen die Fehlerwahrscheinlichkeit beim
Einlesen der CSV-Datei durch das Zielsystem. Sie müssen ersetzt werden durch
den Text \<br\>

</td></tr><tr><td>
Doppeltes Anführungszeichen (ASCII 34)

</td><td>
’

(ASCII 39)

</td><td>
Reserviertes Zeichen, für die Markierung der Inhalte von Feldern. Sie müssen
ersetzt werden durch ein „Einfaches Anführungszeichen“.

</td></tr><tr><td>
\<tr\>

</td><td>
löschen

</td><td>
Reservierte Zeichen, für eine Datensatztrennung im Inhaltsfeld. Die Zeichen
müssen gelöscht werden.

</td></tr><tr><td>
\</tr\>

</td><td>
löschen

</td><td>
Reservierte Zeichen, für eine Datensatztrennung im Inhaltsfeld. Die Zeichen
müssen gelöscht werden.

</td></tr></table>

### 13.1 Basisfeldtypen von Prozessdaten

Tabelle 10 definiert Basisfeldtypen, die in konkreten Definitionen fachlicher
Tabellen referenziert werden. In der Definition der fachlichen Tabellen können
diese Basisfeldtypen weiter durch Constraints konkretisiert werden, z. B. durch
Einschränkung auf eine fachlich definierte Wertemenge.

<table><tr><th>
Basisfeldtyp

</th><th>
Definition

</th><th>
Beispiel

</th></tr><tr><td>
[String]

</td><td>
Beliebige Zeichenkette mit den Anforderungen aus GS-A_5249

</td><td>
Hello World

</td></tr><tr><td>
[Date]

</td><td>
Gemäß [ISO-Norm 8601] folgendes Format auf Grundlage der lokalen Zeit
gegenüber UTC:

YYYY-MM-DDThh:mm:ss±hh

</td><td>
2015-02-23T01:47:36+01

</td></tr><tr><td>
[Date]

</td><td>
als Bestandteil eines Dateinamens: YYYYMMDDThhmmss±hh

</td><td>
20150223T014736+01

</td></tr><tr><td>
[Integer]

</td><td>
+-nnnnnnnnn

</td><td>
88888888

</td></tr><tr><td>
[Double]

</td><td>
+-nnnnn,nnn

</td><td>
2,456

</td></tr><tr><td>
[Auswahlfeld], (Auswahl1), (Auswahl2), (Auswahln)

</td><td>
Es ist immer nur ein Wert von Auswahl n gültig.

Beispiel :[Auswahlfeld], (ja), (nein)

</td><td>
ja

</td></tr><tr><td>
[Telefonnummer]

</td><td>
[String] DIN 5008

</td><td>
+49 30 40041-999

</td></tr><tr><td>
[hh.mm]

</td><td>
Uhrzeit: zwei Stellen für Stunde, zwei Stellen für Minuten gemäß [ISO-Norm
8601]

</td><td>
12:30

</td></tr><tr><td>
[hhhh:mm:ss]

</td><td>
Dauer in Stunden, zwei Stellen für Minuten, zwei Stellen für Sekunden

</td><td>
0012:04:10

</td></tr></table>

### 14 Anhang A – Verzeichnisse

### 14.1 Abkürzungen

<table><tr><th>
Kürzel

</th><th>
Erläuterung

</th></tr><tr><td>
AZPD

</td><td>
Anbieter Zentraler Plattformdienste

</td></tr><tr><td>
CAB

</td><td>
Change Advisory Board

</td></tr><tr><td>
eCAB

</td><td>
Emergency Change Advisory Board

</td></tr><tr><td>
CHG

</td><td>
Change Management

</td></tr><tr><td>
CI

</td><td>
Configuration Item

</td></tr><tr><td>
CM

</td><td>
Configuration Management

</td></tr><tr><td>
CSV

</td><td>
Comma-Separated Values

</td></tr><tr><td>
DVO

</td><td>
Dienstleister-vor-Ort

</td></tr><tr><td>
EMC

</td><td>
Emergency Management Committee

</td></tr><tr><td>
FSC

</td><td>
Forward Schedule of Change

</td></tr><tr><td>
GTI

</td><td>
Gesamtverantwortlicher der Telematikinfrastruktur

</td></tr><tr><td>
ID

</td><td>
Identifikationsnummer

</td></tr><tr><td>
INC

</td><td>
Incident Management

</td></tr><tr><td>
ITIL

</td><td>
IT Infrastructure Library

</td></tr><tr><td>
ITSM

</td><td>
IT-Service-Management

</td></tr><tr><td>
PE

</td><td>
Problemerkennender

</td></tr><tr><td>
PED

</td><td>
Professionelle Endnutzernahe Dienstleister

</td></tr><tr><td>
PERF

</td><td>
Performance Management

</td></tr><tr><td>
PKI

</td><td>
public key infrastucture

</td></tr><tr><td>
PLV

</td><td>
Problemlösungsverantwortlicher

</td></tr><tr><td>
PRO

</td><td>
Problem Management

</td></tr><tr><td>
PU

</td><td>
Produktivumgebung

</td></tr><tr><td>
RF

</td><td>
Request Fulfillment

</td></tr><tr><td>
RFC

</td><td>
Request for Change

</td></tr><tr><td>
RLM

</td><td>
Release Management

</td></tr><tr><td>
RU

</td><td>
Referenzumgebung

</td></tr><tr><td>
SLK

</td><td>
Service Level Katalog

</td></tr><tr><td>
SLM

</td><td>
Service Level Management

</td></tr><tr><td>
SLR

</td><td>
Service Level Requirements

</td></tr><tr><td>
SPOC

</td><td>
Single Point of Contact

</td></tr><tr><td>
STD

</td><td>
Standard

</td></tr><tr><td>
SV

</td><td>
Serviceverantwortlicher

</td></tr><tr><td>
SZZP

</td><td>
Sicherer Zentraler Zugangspunkt

</td></tr><tr><td>
TI

</td><td>
Telematikinfrastruktur

</td></tr><tr><td>
TMS

</td><td>
Trust Management System

</td></tr><tr><td>
TU

</td><td>
Testumgebung

</td></tr><tr><td>
UML

</td><td>
Unified Modeling Language

</td></tr><tr><td>
VPN-ZugD

</td><td>
VPN-Zugangsdienst

</td></tr><tr><td>
WDB

</td><td>
Wissensdatenbank

</td></tr><tr><td>
ZID

</td><td>
Zentrale Informationsdrehscheibe

</td></tr></table>

### 14.2 Glossar

Das Glossar wird als eigenständiges Dokument, vgl. [gemGlossar] zur Verfügung
gestellt.

### 14.3 Abbildungsverzeichnis

- [Abbildung-1] -  CM – TI-Services: Beziehung und CIs (Auszug) der CMDB-TI zur lokalen CMDB der TI-ITSM-Teilnehmer

### 14.4 Tabellenverzeichnis

- [Tabelle-1] - Tab_Betr_TIP_026 INC – Festlegung der Dringlichkeit
- [Tabelle-2] - Tab_Betr_TIP_027 INC – Festlegung von Auswirkung
- [Tabelle-3] - Tab_Betr_TIP_009 INC – Prioritätenmatrix
- [Tabelle-4] - Tab_Betr_TIP_102 PRO – Festlegung von Dringlichkeit
- [Tabelle-5] - Tab_Betr_TIP_103 PRO – Festlegung von Auswirkung
- [Tabelle-6] - Tab_Betr_TIP_100 CM – TI-Stammdaten Datenpflege Gesamtverantwortlicher TI
- [Tabelle-7] - Tab_Betr_TIP_101 CM – TI-Konfigurationsdaten
- [Tabelle-8] - Tab_Betr_TIP_024 CHG – Vorprüfung. Produktänderungsbedarf
- [Tabelle-9] - Tab_Betr_TIP_048 CHG – Kriterien für Emergency Changes
- [Tabelle-10] - Tab_Betr_TIP_003 PERF – Reportinhalte von Performance Messungen
- [Tabelle-11] - Tab_Betr_TIP_049 reservierte Zeichen Ersetzungstabelle
- [Tabelle-12] - Tab_Betr_TIP_030 Basisfeldtypen von CSV-Dateien

### 14.5 Referenzierte Dokumente

### 14.5.1 Dokumente der gematik

Die nachfolgende Tabelle enthält die Bezeichnung der in dem vorliegenden
Dokument referenzierten Dokumente der gematik zur Telematikinfrastruktur. Der
mit der vorliegenden Version korrelierende Entwicklungsstand dieser Konzepte
und Spezifikationen wird pro Release in einer Dokumentenlandkarte definiert;
Version und Stand der referenzierten Dokumente sind daher in der nachfolgenden
Tabelle nicht aufgeführt. Deren zu diesem Dokument jeweils gültige
Versionsnummern sind in der aktuellen, von der gematik veröffentlichten
Dokumentenlandkarte enthalten, in der die vorliegende Version aufgeführt wird.

<table><tr><th>
[Quelle]

</th><th>
Herausgeber: Titel

</th></tr><tr><td>
[gemGlossar]

</td><td>
gematik: Glossar der Telematikinfrastruktur

</td></tr><tr><td>
[gemKPT_Betr]

</td><td>
gematik: Betriebskonzept Online-Produktivbetrieb

</td></tr><tr><td>
[gemSpec_DS_Anbieter]

</td><td>
gematik: Spezifikation Datenschutz- und Sicherheitsanforderungen der TI an
Anbieter

</td></tr><tr><td>
[gemSpec_Perf]

</td><td>
gematik: Übergreifende Spezifikation Performance und Mengengerüst TI-Plattform

</td></tr></table>

### 14.5.2 Weitere Dokumente

<table><tr><th>
[Quelle]

</th><th>
Herausgeber (Erscheinungsdatum): Titel

</th></tr><tr><td>
[BSI 100-4]

</td><td>
BSI-Standardreihe zur Informationssicherheit: 100-4 Notfallmanagement,  Version
1.0 (2008) 

https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/Publikationen/ITGrundschutzstandards/standard_1004_pdf

</td></tr><tr><td>
[RFC2119]

</td><td>
RFC 2119 (März 1997): Key words for use in RFCs to Indicate Requirement Levels
S. Bradner,  
http://tools.ietf.org/html/rfc2109

</td></tr><tr><td>
[BDSG]

</td><td>
Der Bundesbeauftragte für Datenschutz und Informationsfreiheit (20.12.1990
(neugefasst durch Bek. 14.01.2003, Letzte Änderung vom 14.08.2009): 
Bundesdatenschutzgesetz

</td></tr><tr><td>
[ISO 8601]

</td><td>
ISO 8601:2000: Data elements and interchange formats – Information interchange
– Representation of dates and times

</td></tr><tr><td>
[OMNI WSDL]

</td><td>
omnitracker.wsdl, Version 10.3.200 (build 6408)  
Namespace
http://www.omninet.de/OtWebSvc/v1

</td></tr><tr><td>
[OMNI MANUAL]

</td><td>
OMNITRACKER Web Service Manual, The OMNINET Problem and Request Tracking System 

Version 10.3 (build 6408)

</td></tr><tr><td>
[RFC2617]

</td><td>
RFC 2617 (Juni 1999): HTTP Authentication: Basic and Digest Access
Authentication  
http://tools.ietf.org/html/rfc2617

</td></tr><tr><td>
[RFC2616]

</td><td>
RFC 2616 (Juni 1999): Hypertext Transfer Protocol -- HTTP/1.1 

http://tools.ietf.org/html/rfc2616

</td></tr><tr><td>
[BSI TR-02102]

</td><td>
BSI TR-02102-2 "Kryptographische Verfahren: Empfehlungen und Schlüssellängen,
Teil 2 – Verwendung von Transport Layer Security (TLS)" 

https://www.bsi.bund.de/SharedDocs/Downloads/DE/BSI/Publikationen/TechnischeRichtlinien/TR02102/BSI-TR-02102-2_pdf.html

</td></tr></table>





[Dokumentinformationen]: #dokumentinformationen
[Inhaltsverzeichnis]:    #inhaltsverzeichnis
[1]:                     #1-einordnung-des-dokumentes
[1.1]:                   #11-zielsetzung
[1.2]:                   #12-zielgruppe
[1.3]:                   #13-geltungsbereich
[1.4]:                   #14-abgrenzungen-des-dokuments
[1.5]:                   #15-methodik
[2]:                     #2-prozessübergreifende-regelungen
[2.1]:                   #21-zentrales-ti-itsm-system
[2.1.1]:                 #211-übergreifendes-itsm-der-ti
[2.1.2]:                 #212-kommunikation
[2.1.2.1]:               #2121-kommunikation-außerhalb-des-ti-itsm-systems
[2.1.3]:                 #213-ti-itsm-reporting
[2.2]:                   #22-itsm-der-ti-itsm-teilnehmer
[2.2.1]:                 #221-auszüge-aus-dem-betriebshandbuch-der-ti-itsm-teilnehmer
[2.3]:                   #23-auditierung-von-ti-itsm-teilnehmern
[2.4]:                   #24-zentrale-koordinierung-durch-den-gesamtverantwortlichen-ti
[2.4.1]:                 #241-eskalationen-im-übergreifenden-ti-itsm
[2.4.2]:                 #242-taskforce-als-instrument-der-deeskalation-im-übergreifenden-ti-itsm
[3]:                     #3-incident-management
[3.1]:                   #31-begriffsbestimmungen
[3.1.1]:                 #311-übergreifender-incident
[3.2]:                   #32-prozessdurchführung-incident-management
[3.2.1]:                 #321-übergreifenden-incident-erfassen-und-qualifizieren
[3.2.1.1]:               #3211-übergreifenden-incident-erfassen
[3.2.1.2]:               #3212-übergreifenden-incident-qualifizieren
[3.2.1.3]:               #3213-serviceverantwortung-für-übergreifenden-incident-zuweisen
[3.2.2]:                 #322-serviceverantwortung-für-übergreifenden-incident-prüfen
[3.2.3]:                 #323-lösung-für-übergreifenden-incident-erstellen
[3.2.4]:                 #324-unterstützung-für-einen-übergreifenden-incident-einfordern
[3.2.5]:                 #325-lösung-für-einen-übergreifenden-incident-prüfen
[3.2.6]:                 #326-übergreifenden-incident-schließen
[3.3]:                   #33-abweichungen-im-prozessablauf
[3.3.1]:                 #331-übergreifenden-incident-eskalieren
[3.3.2]:                 #332-mitwirkung-in-einer-taskforce
[3.4]:                   #34-verfahren-für-die-lösung-eines-security-incidents
[3.5]:                   #35-verfahren-für-die-lösung-eines-incidents-mit-datenschutzrelevanz
[3.6]:                   #36-verfahren-für-die-lösung-von-notfall-incidents
[4]:                     #4-problem-management
[4.1]:                   #41-begriffsbestimmungen
[4.1.1]:                 #411-übergreifendes-problem
[4.2]:                   #42-prozessdurchführung-problem-management
[4.2.1]:                 #421-übergreifendes-problem-erfassen-und-qualifizieren
[4.2.1.1]:               #4211-übergreifendes-problem-erfassen
[4.2.1.2]:               #4212-übergreifendes-problem-qualifizieren
[4.2.1.3]:               #4213-serviceverantwortung-für-übergreifendes-problem-zuweisen
[4.2.2]:                 #422-serviceverantwortung-für-übergreifendes-problem-prüfen
[4.2.3]:                 #423-lösung-für-übergreifendes-problem-erstellen
[4.2.3.1]:               #4231-problem-ursachenanalyse-durchführen
[4.2.3.2]:               #4232-lösung-für-übergreifendes-problem-entwickeln-und-implementieren
[4.2.3.3]:               #4233-stornierung-oder-abbruch-der-bearbeitung-eines-problem-tickets
[4.2.4]:                 #424-lösungsunterstützung-für-übergreifendes-problem
[4.2.5]:                 #425-lösung-für-übergreifendes-problem-prüfen
[4.2.6]:                 #426-übergreifendes-problem-schließen
[4.3]:                   #43-abweichungen-im-prozessablauf
[4.3.1]:                 #431-übergreifendes-problem-eskalieren
[4.3.2]:                 #432-mitwirkung-in-einer-taskforce
[5]:                     #5-request-fulfillment
[5.1]:                   #51-begriffsbestimmungen
[5.1.1]:                 #511-service-request
[5.1.2]:                 #512-beschwerdemanagement
[5.2]:                   #52-prozessdurchführung-request-fulfillment
[5.2.1]:                 #521-service-request-erfassen
[5.2.2]:                 #522-service-request-prüfen
[5.2.3]:                 #523-service-request-erfüllen
[5.2.4]:                 #524-service-request-verifizieren-und-schließen
[6]:                     #6-configuration-management
[6.1]:                   #61-begriffsbestimmungen
[6.1.1]:                 #611-konfigurationselement-configuration-item-ci
[6.1.2]:                 #612-ti-konfigurationsdatenbank
[6.1.3]:                 #613-ti-stammdaten
[6.1.4]:                 #614-ti-konfigurationsdaten
[6.1.5]:                 #615-lokale-konfigurationsdaten
[6.2]:                   #62-prozessdurchführung-configuration-management
[6.2.1]:                 #621-schema-der-ti-konfigurationsdatenbank-pflegen
[6.2.2]:                 #622-konfigurationsdaten-pflegen
[6.2.2.1]:               #6221-übermittlung-von-konfigurationsdaten-nach-lokal-autorisierten-produkt-changes
[7]:                     #7-change--release-management
[7.1]:                   #71-begriffsbestimmungen
[7.1.1]:                 #711-request-for-change-rfc
[7.1.2]:                 #712-produkt-change
[7.1.2.1]:               #7121-master-change
[7.1.2.2]:               #7122-sub-change
[7.1.3]:                 #713-produkttyp-change
[7.1.4]:                 #714-emergency-change
[7.1.5]:                 #715-betriebliches-change-bewertungsgremium-bcb
[7.1.6]:                 #716-change-advisory-board-cab
[7.1.7]:                 #717-emergency-change-advisory-board-ecab
[7.1.8]:                 #718-post-implementation-review-pir
[7.1.9]:                 #719-change---release-kalender
[7.2]:                   #72-prozessdurchführung-change--release-management
[7.2.1]:                 #721-produkt-change-request-for-change-rfc-erstellen
[7.2.2]:                 #722-produkt-change-rfc-bewerten
[7.2.3]:                 #723-produkt-change-rfc-genehmigen
[7.2.4]:                 #724-produkt-change-umsetzen
[7.2.5]:                 #725-produkt-change-umsetzung-verifizieren
[7.2.6]:                 #726-produkt-change-abschließen
[7.3]:                   #73-abweichungen-im-prozessablauf
[7.4]:                   #74-verfahren-für-einen-standard-change
[7.5]:                   #75-verfahren-für-einen-emergency-change
[8]:                     #8-knowledge-management
[8.1]:                   #81-begriffsbestimmungen
[8.1.1]:                 #811-wissensdatenbank-wdb-des-ti-itsm-systems
[8.2]:                   #82-prozessdurchführung-knowledge-management
[8.2.1]:                 #821-wissen-identifizieren-und-übermitteln
[9]:                     #9-service-level-management
[9.1]:                   #91-begriffsbestimmungen
[9.1.1]:                 #911-service-level
[9.1.2]:                 #912-service-level-report
[9.2]:                   #92-prozessdurchführung-service-level-management
[9.2.1]:                 #921-messung-der-service-level
[9.2.2]:                 #922-bereitstellung-des-service-level-reports
[9.2.3]:                 #923-teilnahme-am-service-review
[10]:                    #10-performance-management
[10.1]:                  #101-begriffsbestimmungen
[10.1.1]:                #1011-performance
[10.2]:                  #102-prozessdurchführung-performance-management
[10.2.1]:                #1021-performance-messen
[10.2.2]:                #1022-performance-reporten
[10.2.3]:                #1023-performance-bewerten-planen-und-steuern
[10.2.4]:                #1024-service-monitoring-finale-lösung
[11]:                    #11-servicekatalog-management
[11.1]:                  #111-begriffsbestimmungen
[11.1.1]:                #1111-servicekatalog
[11.1.2]:                #1112-serviceverzeichnis
[11.2]:                  #112-prozessdurchführung-servicekatalog-management
[11.2.1]:                #1121-definition-der-angebotenen-services
[11.2.2]:                #1122-servicekatalog-freigeben
[12]:                    #12-notfall-management
[12.1]:                  #121-begriffsbestimmungen
[12.1.1]:                #1211-notfall
[12.1.2]:                #1212-lokaler-notfall
[12.1.3]:                #1213-ti-notfall
[12.1.4]:                #1214-ti-notfallvorsorge
[12.1.5]:                #1215-ti-notfallmaßnahme
[12.1.6]:                #1216-notbetrieb
[12.1.7]:                #1217-ti-notfallbewältigung
[12.1.8]:                #1218-emergency-management-committee-emc
[12.1.9]:                #1219-lösungsteam
[12.2]:                  #122-prozessdurchführung-notfallvorsorge
[12.2.1]:                #1221-analyse-der-auswirkungen-möglicher-notfälle-der-produktinstanzen
[12.2.2]:                #1222-entwicklung-und-pflege-der-notfallvorsorgedokumentation
[12.2.3]:                #1223-umsetzung-vorkehrungen-zur-notfallvorsorge
[12.3]:                  #123-prozessdurchführung-ti-notfallbewältigung
[12.3.1]:                #1231-ti-notfallerkennung
[12.3.2]:                #1232-eskalation-ti-notfälle
[12.3.3]:                #1233-sofortmaßnahmen-ti-notfälle
[12.3.4]:                #1234-bewältigung-ti-notfälle
[12.3.5]:                #1235-koordination-der-ti-notfallbewältigung-durch-den-gesamtverantwortlichen-ti
[12.3.5.1]:              #12351-notfallbeurteilung
[12.3.5.2]:              #12352-notfallfeststellung
[12.3.5.3]:              #12353-einberufung-des-emergency-management-committee-emc
[12.3.5.4]:              #12354-zusammenstellung-des-lösungsteams
[12.3.5.5]:              #12355-durchführung-der-notfallmaßnahmen
[12.3.5.6]:              #12356-notfalldeeskalation
[12.3.6]:                #1236-wiederherstellung
[12.3.7]:                #1237-nachbearbeitungnotfallauswertung
[12.4]:                  #124-informationspflichten
[12.5]:                  #125-dokumentation
[12.5.1]:                #1251-ti-notfall-logbuch
[12.5.2]:                #1252-wiederherstellungsbericht
[13]:                    #13-vorschriften-für-csv-reporting
[13.1]:                  #131-basisfeldtypen-von-prozessdaten
[14]:                    #14-anhang-a-–-verzeichnisse
[14.1]:                  #141-abkürzungen
[14.2]:                  #142-glossar
[14.3]:                  #143-abbildungsverzeichnis
[14.4]:                  #144-tabellenverzeichnis
[14.5]:                  #145-referenzierte-dokumente
[14.5.1]:                #1451-dokumente-der-gematik
[14.5.2]:                #1452-weitere-dokumente
[Abbildung-1]:           gemRL_Betr_TI_V2.5.1.attachments/12506991669064696413.png
[Tbl-001]:               #Tbl-001 (&93834764183208)
[Tabelle-1]:             #Tabelle-1 (&93834765831328)
[Tabelle-2]:             #Tabelle-2 (&93834765851224)
[Tabelle-3]:             #Tabelle-3 (&93834765874040)
[Tabelle-4]:             #Tabelle-4 (&93834765967984)
[Tabelle-5]:             #Tabelle-5 (&93834765981072)
[Tabelle-6]:             #Tabelle-6 (&93834766780176)
[Tabelle-7]:             #Tabelle-7 (&93834766806160)
[Tabelle-8]:             #Tabelle-8 (&93834766881832)
[Tabelle-9]:             #Tabelle-9 (&93834766916160)
[Tbl-011]:               #Tbl-011 (&93834767097904)
[Tabelle-10]:            #Tabelle-10 (&93834767114544)
[Tabelle-11]:            #Tabelle-11 (&93834767367224)
[Tabelle-12]:            #Tabelle-12 (&93834767398184)
[Tbl-015]:               #Tbl-015 (&93834767445272)
[Tbl-016]:               #Tbl-016 (&93834767611608)
[Tbl-017]:               #Tbl-017 (&93834767625304)
