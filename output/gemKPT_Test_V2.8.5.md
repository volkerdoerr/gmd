
Elektronische Gesundheitskarte und Telematikinfrastruktur

### Testkonzept der TI<br>Abbildung 2: Exemplarischer Ablauf eines Testverfahrens

- Klassifizierung: öffentlich
- Referenzierung: gemKPT_Test
- Revision: 558730
- Stand: 31.01.2022
- Status: freigegeben
- Version: 2.8.5

### Dokumentinformationen

Änderungen zur Vorversion

Anpassungen des vorliegenden Dokumentes im Vergleich zur Vorversion können Sie
der nachfolgenden Tabelle entnehmen.

Bitte beachten Sie die Hinweise zur Einführung der Benennungen 'WANDA Basic'
und 'WANDA Smart' (siehe Dokumentenhistorie).

Dokumentenhistorie

<table><tr><th>
Version

</th><th>
Datum

</th><th>
Kap./ Seite

</th><th>
Grund der Änderung, besondere Hinweise

</th><th>
Bearbeitung

</th></tr><tr><td>
Übernahme Version 1.6.0 aus ORS1

</td></tr><tr><td>
1.6.5

</td><td>
12.02.16

</td><td>
Anpassungen zum Online-Produktivbetrieb (Stufe 1)

</td><td>
gematik

</td></tr><tr><td>
1.7.0

</td><td>
03.05.16

</td><td>
freigegeben

</td><td>
gematik

</td></tr><tr><td>
1.8.0

</td><td>
24.08.16

</td><td>
Einarbeitung weiterer Kommentare

</td><td>
gematik

</td></tr><tr><td>
1.9.0

</td><td>
28.10.16

</td><td>
Anpassungen gemäß Änderungsliste

</td><td>
gematik

</td></tr><tr><td>
1.10.0

</td><td>
24.04.17

</td><td>
Anpassungen gemäß Änderungsliste

</td><td>
gematik

</td></tr><tr><td>
2.0.0

</td><td>
14.05.18

</td><td>
Überarbeitung des Testkonzepts

Änderungen aus P14.4 (Addendum), Änderungen, die sich aus den Erkenntnissen
von OPB1 motivieren

</td><td>
gematik

</td></tr><tr><td>
2.1.0

</td><td>
26.10.18

</td><td>
Änderungen aus P15.9

</td><td>
gematik

</td></tr><tr><td>
2.2.0

</td><td>
18.12.18

</td><td>
Anpassungen ePA

</td><td>
gematik

</td></tr><tr><td>
2.3.0

</td><td>
15.05.19

</td><td>
Anpassung gemäß P18.1

</td><td>
gematik

</td></tr><tr><td>
2.4.0

</td><td>
28.06.19

</td><td>
Einarbeitung P 19.1

</td><td>
gematik

</td></tr><tr><td>
2.5.0

</td><td>
02.10.19

</td><td>
Einarbeitung P 20.1

</td><td>
gematik

</td></tr><tr><td>
2.6.0

</td><td>
02.03.20

</td><td>
Einarbeitung P 21.1

</td><td>
gematik

</td></tr><tr><td>
2.6.1

</td><td>
26.05.20

</td><td>
Einarbeitung P 21.3

</td><td>
gematik

</td></tr><tr><td>
2.7.0

</td><td>
30.06.20

</td><td>
Anpassungen gemäß Änderungsliste P22.1 und Scope-Themen aus Systemdesign
R4.0.0

</td><td>
gematik

</td></tr><tr><td>
2.8.0

</td><td>
19.02.21

</td><td>
Einarbeitung Änderungsliste 22.5 

</td><td>
gematik

</td></tr><tr><td>
2.8.1

</td><td>
09.07.21

</td><td>
Einarbeitung Änderungsliste ePA_Maintenance_21.2

</td><td>
gematik

</td></tr><tr><td>
2.8.2

</td><td>
02.09.21

</td><td>
Einarbeitung Konn_Maintenance_21.5:

ab Release "Konnektor PTV 5.0.2: Maintenance 21.5" (Sept. 2021) führt die
gematik eine stufenweise Umbenennung folgender Begriffe durch:

aus "aAdG-NetG" wird "WANDA Basic",

aus "aAdG" und "aAdG-NetG-TI" wird "WANDA Smart"

(nähere Informationen finden Sie unter

https://fachportal.gematik.de/

)

</td><td>
gematik

</td></tr><tr><td>
2.8.3

</td><td>
07.10.21

</td><td>
Einarbeitung gemF_APOVZD, Einarbeitung

E-Rezept_Maintenance_21.2

</td><td>
gematik

</td></tr><tr><td>
2.8.4

</td><td>
28.10.21

</td><td>
4.6

</td><td>
Einarbeitung Test_Maintenance_21.1

</td><td>
gematik

</td></tr><tr><td>
2.8.5

</td><td>
31.01.22

</td><td>
4.6

</td><td>
Einarbeitung Konn_Maintenance_21.6

</td><td>
gematik

</td></tr></table>

### Inhaltsverzeichnis

- [Dokumentinformationen]
- [Inhaltsverzeichnis]
- [1] Einordnung des Dokuments
  - [1.1] Zielsetzung
  - [1.2] Zielgruppe
  - [1.3] Geltungsbereich
  - [1.4] Abgrenzungen
  - [1.5] Methodik
- [2] Allgemeine Testvorgehensweise
  - [2.1] Einleitung
  - [2.2] Ablauf für den Nachweis der funktionalen Eignung innerhalb eines Zulassungsverfahrens
  - [2.3] Testspezifische Rollen
    - [2.3.1] Testkoordinierende Instanz (TKI)
    - [2.3.2] Testintegrator zentrale Plattformdienste (TIZP)
    - [2.3.3] Testbetriebsinstanz (TBI)
    - [2.3.4] Testdurchführende Instanz (TDI) Referenzumgebung (RU)
    - [2.3.5] Testdurchführende Instanz (TDI) TU Testumgebung
    - [2.3.6] Test- & Transitionmanager (TTM)
  - [2.4] Testphasen
    - [2.4.1] Eigenverantwortlicher Test
      - [2.4.1.1] Qualitätssichernde Maßnahmen und Produktmuster
    - [2.4.2] Zulassungstest
      - [2.4.2.1] Fehlerschweregrade
      - [2.4.2.2] Testabbruch
  - [2.5] Testarten
    - [2.5.1] Güteprüfung
    - [2.5.2] Funktionstest
    - [2.5.3] Interoperabilitätstest
    - [2.5.4] Leistungstest
- [3] Systemumgebungen
  - [3.1] Testobjekte
  - [3.2] Anforderungen an die Systemumgebungen
    - [3.2.1] Trennung der Netzwerke
    - [3.2.2] Trennung der Vertrauensräume
    - [3.2.3] Gemeinsame Eigenschaften für alle Systemumgebungen
    - [3.2.4] Gemeinsame Eigenschaften der Referenz- und Testumgebung
    - [3.2.5] Exklusiver Zugriff
    - [3.2.6] Logging
    - [3.2.7] Testwerkzeuge
    - [3.2.8] Test- und Referenzobjekte
    - [3.2.9] Referenzumgebung
      - [3.2.9.1] Qualitätssicherungsmaßnahmen der Hersteller und Anbieter
      - [3.2.9.2] Weiterentwicklung der Referenzumgebung
      - [3.2.9.3] Nutzung der Referenzumgebung
      - [3.2.9.4] Instanzen der Referenzumgebung
    - [3.2.10] Testumgebung
      - [3.2.10.1] Bestandteile der Testumgebung
      - [3.2.10.2] Weiterentwicklung der Testumgebung
      - [3.2.10.3] Dimensionierung der Testumgebung
      - [3.2.10.4] Betrieb der Testumgebung
      - [3.2.10.5] Nachstellen von PU-Fehlern in TU
- [4] Szenarien
  - [4.1] Einleitung
  - [4.2] Testvorgehensweise im Rahmen der Zulassung eines neuen Produkts
  - [4.3] Testvorgehensweise im Rahmen der Zulassung eines geänderten Produkts
  - [4.4] Regressionstest
  - [4.5] Teststufen
    - [4.5.1] Produkttest (EvT)
    - [4.5.2] Produktübergreifender Test (EvT)
    - [4.5.3] Eingangsprüfung (ZulT)
    - [4.5.4] Produkttest (ZulT)
    - [4.5.5] Produktübergreifender Test (ZulT)
  - [4.6] Interoperabilität
  - [4.7] Testdokumentation
    - [4.7.1] Testkonzept
    - [4.7.2] Testspezifikation
    - [4.7.3] Release Notes
    - [4.7.4] Produktdokumentation
    - [4.7.5] Testprotokoll
    - [4.7.6] Testbericht
  - [4.8] Serviceprodukte der gematik zur Testunterstützung
- [5] Fachanwendung VSDM
  - [5.1] Testkarten
    - [5.1.1] Testkartenausprägungen
    - [5.1.2] Testkarten Verwendung
    - [5.1.3] Anforderungen an die Testkarten eGK
  - [5.2] Flip/Flop-Verfahren
  - [5.3] Umgang mit mandantenfähigen Fachdiensten
  - [5.4] Testdurchführung der EvT bei VSDM
- [6] Fachanwendung KOM-LE
- [7] Fachanwendung AdV
- [8] Fachanwendung ePA
  - [8.1] ePA-Aktensystem
  - [8.2] ePA-Frontend des Versicherten
  - [8.3] Basis-Consumer/KTR-Consumer
  - [8.4] Signaturdienst
  - [8.5] Schlüsselgenerierungsdienst
- [9] Weitere Anwendungen
  - [9.1] Vorbereitung der EvT zur funktionalen Eignung
  - [9.2] Durchführung EvT zur funktionalen Eignung
  - [9.3] Schnittstellentests in der TU
- [10] Anhang A – Verzeichnisse
  - [10.1] Abkürzungen
  - [10.2] Glossar
  - [10.3] Abbildungsverzeichnis
  - [10.4] Tabellenverzeichnis
  - [10.5] Referenzierte Dokumente
    - [10.5.1] Dokumente der gematik
    - [10.5.2] Weitere Dokumente
- [11] Anhang B – Beispielhafte Testdokumentation
  - [11.1] Testkonzept
  - [11.2] Testspezifikation
  - [11.3] Testprotokoll
  - [11.4] Tabelle umzusetzender Anforderungen

### 1 Einordnung des Dokuments

### 1.1 Zielsetzung

Das Testkonzept der Telematikinfrastruktur (TI) definiert die Anforderungen an
die notwendigen Testmaßnahmen und Rahmenbedingungen für neue oder geänderte
Komponenten und Dienste (nachfolgend Produkte) der Telematikinfrastruktur (TI)
im Produktivbetrieb.

Über diese Testmaßnahmen müssen die Hersteller der Produkte ihre
spezifizierte Funktionalität nachweisen, bevor schrittweise die Integration
und übergreifende Nutzung weiterer Produkte vorgenommen wird.

Daher werden die Produkte auf definierte Schnittstellenleistung und
Funktionalität getestet sowie Interoperabilitätstests aus Anwendungs- und
Gesamtprozesssicht durchgeführt. Diese dienen der vollständigen Abnahme der
jeweiligen Produkte und Fachanwendungen.

Das Testkonzept folgt dem Standard des International Software Testing
Qualifications Board (ISTQB).

### 1.2 Zielgruppe

Das Dokument richtet sich an Zulassungs- bzw. Bestätigungsnehmer (Hersteller
und Anbieter) von Produkten der TI sowie an die korrespondierenden
testspezifischen Rollen. Die Zulassungs- bzw. Bestätigungsnehmer werden in
diesem Dokument einheitlich als Zulassungsnehmer bezeichnet. Zu den Anbietern
von Produkten zählen hier auch die Betreiber von Fachanwendungsspezifischen
Diensten.

### 1.3 Geltungsbereich

Dieses Dokument enthält normative Festlegungen zu Testmaßnahmen der
Telematikinfrastruktur des deutschen Gesundheitswesens. Der
Gültigkeitszeitraum der vorliegenden Version und deren Anwendung in
Zulassungsverfahren werden durch die gematik GmbH in gesonderten Dokumenten
(z.B. Dokumentenlandkarte, Produkttypsteckbrief, Leistungsbeschreibung)
festgelegt und bekannt gegeben.

### 1.4 Abgrenzungen

Normative Vorgaben zu Themen, welche nicht nur den Test betreffen, wie z. B.
Releasemanagement, Migration, Zulassung und Betrieb, sind nicht Bestandteil
dieses Konzepts.

### 1.5 Methodik

Anforderungen als Ausdruck normativer Festlegungen werden durch eine eindeutige
ID sowie die dem RFC 2119 [RFC2119] entsprechenden, in Großbuchstaben
geschriebenen deutschen Schlüsselworte MUSS, DARF NICHT, SOLL, SOLL NICHT,
KANN gekennzeichnet.

Sie werden im Dokument wie folgt dargestellt:

  \<AFO-ID\> - \<Titel der Afo\>Text / Beschreibung[ \<=]

Dabei umfasst die Anforderung sämtliche zwischen Afo-ID und Textmarke
[\<=] angeführten Inhalte.

### 2 Allgemeine Testvorgehensweise

### 2.1 Einleitung

Das Ziel der Testaktivitäten ist es, den Nachweis zu erbringen, dass
zuzulassende Produkte alle aus den jeweiligen Produkttypsteckbriefen gestellten
funktionalen und nichtfunktionalen Anforderungen erfüllen. Schwerpunkt sind
hier Funktionalität, Sicherheit und Interoperabilität. Die Strukturierung in
Testphasen soll die Testprozesse bis in den Produktivbetrieb der Komponenten
unterstützen. Um das zu erreichen, wird das Testen in zwei Testphasen (siehe
Kapitel 2.4) eingeteilt, die aufeinander aufbauen:

 ---> UL

Die jeweiligen Aktivitäten der Testphasen finden in eigenen Systemumgebungen
(siehe Kapitel 3) statt:

 ---> UL

Durch den Aufbau unterschiedlicher Systemumgebungen werden die Rahmenbedingungen
geschaffen, die die einzelnen Teststufen unterstützen (siehe Kapitel 4.5).

Zur Verbesserung der Produktreife im Rahmen der Zulassungstests wird die
Eigenverantwortung der Industrie durch Produkttests und produktübergreifende
Tests gefordert. Eine Überprüfung der Produktreife erfolgt im Rahmen der
Eingangsprüfung in der Testumgebung.

Hersteller und Anbieter von Produkten tragen zur Ende-zu-Ende-Funktionalität
bei, da reine Tests der Produktschnittstellen nicht ausreichen, um
Interoperabilität zu gewährleisten. Zur Wahrnehmung dieser Verantwortung ist
es notwendig, den Herstellern und Anbietern die Möglichkeit zu geben,
koordinierte Ende-zu-Ende-Tests durchzuführen.

Die genannten Zusammenhänge werden in der nachfolgenden Abbildung dargestellt.

![Abbildung-1][Abbildung-1]

### 2.2 Ablauf für den Nachweis der funktionalen Eignung innerhalb eines Zulassungsverfahrens

In der folgenden Prozessgrafik sind die wesentlichen Prozessschritte
beispielhaft dargestellt, die üblicherweise bei Neuzulassung eines Produkts
durchlaufen werden.

![Abbildung-2][Abbildung-2]

Die Beschreibung des gesamten Zulassungsverfahrens für das jeweilige Produkt
findet sich im gematik-Fachportal in der Verfahrensbeschreibung.

### 2.3 Testspezifische Rollen

Die betrieblichen Rollen und Akteure werden im spezifischen Betriebskonzept der
TI [gemKPT_Betr] definiert. Darüber hinaus gibt es im Rahmen des
Testgeschehens spezifische Aufgaben, die die allgemeine Definition ergänzen.
Außerdem gibt es zusätzliche Rollen, die nur im Testgeschehen wirksam werden.

Die folgenden Rollen werden im Test wahrgenommen:

 ---> UL

werden im Anschluss definiert.

Der Anbieter zentrale Plattformdienste (AZPD) hat die Rollen TBI und TIZP inne.

Die folgende Abbildung zeigt einen Überblick des Rollenkonzepts:

![Abbildung-3][Abbildung-3]

### 2.3.1 Testkoordinierende Instanz (TKI)

Die testkoordinierende Instanz erfüllt den gesetzlichen Testauftrag
hinsichtlich § 291b SGB V und hat die übergreifende
Koordinationsverantwortung für alle Test- und Wartungsmaßnahmen in der
Referenz- und Testumgebung. Die testkoordinierende Instanz hat die
übergreifende Verantwortung zur Sicherstellung der qualitäts- und
termingerechten Umsetzung aller geplanten Test- und Wartungsvorhaben an Test-
und Referenzobjekten.

In diesem Zusammenhang vertritt die testkoordinierende Instanz die Interessen
der gematik zur Wahrung des diskriminierungsfreien Zugangs auf die Umgebungen
durch Dritte und der gematik selbst. Die Hauptaufgaben der testkoordinierenden
Instanz sind:

 ---> UL

### 2.3.2 Testintegrator zentrale Plattformdienste (TIZP)

Der TIZP ist für die Integration von Komponenten, Diensten und weiterer
Anwendungen in RU und TU verantwortlich. Er bietet anderen Zulassungsnehmern
die Anbindung an die TI an und integriert deren Produkte netztechnisch in die
jeweilige Testbetriebsumgebung (RU/TU). Hierzu legt er z.B. IP-Adressen fest
und konfiguriert Firewallregeln.

Der AZPD bietet über die Rolle TIZP einen Servicekatalog an, über die die in
den Systemumgebungen nutzbaren zentralen Services abgerufen werden können.

### 2.3.3 Testbetriebsinstanz (TBI)

Die Testbetriebsinstanz für die Referenz- und Testumgebung gewährleistet den
Betrieb ihrer jeweiligen Produkte in den Systemumgebungen RU und TU.

Die Verantwortung für die dezentrale Zone liegt bei der gematik (TU) bzw. bei
einem von der gematik beauftragten Dienstleister (RU). Die Rolle der TBI wird
vom jeweiligen Anbieter bzw. Hersteller des Dienstes oder der Komponente
ausgeübt, wie in Abbildung 3: Rollen innerhalb der Systemumgebungen
dargestellt.

Sofern in den jeweiligen Produkttypsteckbriefen gefordert wird, dass Services
angeboten werden müssen, ist die TBI auch hierfür verantwortlich.

### 2.3.4 Testdurchführende Instanz (TDI) Referenzumgebung (RU)

Die testdurchführende Instanz der RU plant, steuert und verantwortet die
Durchführung von Testmaßnahmen im Sinne der Qualitätssicherung seitens der
Zulassungsnehmer. Diese Testmaßnahmen haben zum Ziel, der gematik die
Funktionalität, Interoperabilität und Sicherheit in Form von
eigenverantwortlichen Tests nachzuweisen. Die testdurchführende Instanz in der
Referenzumgebung ist in der Regel der Zulassungsnehmer.

Die testdurchführende Instanz muss eigenverantwortlich die Durchführung von
Testmaßnahmen als Qualitätssicherungsmaßnahme im Rahmen weiterer Lieferungen
und Leistungen vollziehen (z. B. zur Fehlernachstellung als Wartungsleistung).
Sie besitzt die zentrale Ergebnisverantwortung für alle eigenen Testmaßnahmen
in der RU.

Testinhalte, -umfang und Testtiefe werden auf Grundlage des aktuellen
Produkttypsteckbriefes von der Testdurchführenden Instanz mit dem jeweiligen
Test & Transitionmanager der gematik abgestimmt und müssen die funktionalen
Anforderungen zunächst vollumfänglich abdecken. Weitere Testdurchläufe
können im Rahmen eines Regressionstests in Abstimmung mit dem Test &
Transitionmanager der gematik durchgeführt werden.

Die TDI RU trägt die Verantwortung zur Einbindung ihres Produkts in alle
Systemumgebungen (RU, TU) als Testobjekt und nach erfolgter Zulassung als
Referenzobjekt in alle Systemumgebungen und die Produktivumgebung. Eine
Erklärung von Test- und Referenzobjekten folgt in Kapitel 3.2.8 Die
Einbringung als Referenzobjekt in alle Systemumgebungen erfolgt über den
betrieblichen Changeprozess. Hier kann das ursprüngliche Testobjekt als
Referenzobjekt genutzt werden, sobald dieses zugelassen ist.

In der Testphase der Eigenverantwortlichen Tests muss die TDI RU folgende
Leistungen erbringen:

 ---> UL

### 2.3.5 Testdurchführende Instanz (TDI) TU Testumgebung

Die testdurchführende Instanz der TU wird durch den Test- & Transitionmanager
der gematik repräsentiert. Er hat die zentrale Ergebnisverantwortung für alle
Testmaßnahmen in der TU für das jeweilige Produkt.

### 2.3.6 Test- & Transitionmanager (TTM)

Der Test- & Transitionmanager führt den Zulassungsnehmer durch den Prozess der
Zulassung und koordiniert die Einbringung der Testobjekte in RU/TU und
Bereitstellung der Konfigurationen. Er stellt durch Koordination der
Güteprüfung, der Testberichte der TDI RU und der gematik-eigenen
Testmaßnahmen in der TU die Qualität der jeweiligen Produkte sicher. Folgende
Punkte gehören zu seinen Hauptaufgaben:

 ---> UL

### 2.4 Testphasen

Um den Zweck der Aufteilung in die Testphasen zu verdeutlichen, werden die zwei
Testphasen durch eine kurze Beschreibung charakterisiert. Die Testziele und die
jeweiligen Eingangs- und Ausgangskriterien werden aufgeführt

Eingangskriterien beschreiben Mindestkriterien für den Beginn einer Testphase
bzw. deren jeweiligen Teststufen. Erst wenn diese Kriterien erfüllt sind, darf
mit einer Testphase begonnen werden. Durch die Definition und Prüfung von
Eingangskriterien ist ein effizienter Test in der Testphase gewährleistet.

Ausgangskriterien beschreiben Mindestkriterien für den Abschluss einer
Testphase, bzw. deren jeweiligen Teststufen. Erst wenn diese Kriterien erfüllt
sind, ist die Testphase beendet um das geforderte Qualitätsniveau zu erreichen.

Wenn Eingangs- oder Ausgangskriterien nicht wie gefordert erfüllt sein sollten,
muss eine Risikobewertung vorgenommen und dokumentiert werden. Darin sollen
folgende Punkte adressiert werden:

 ---> UL

Die Anforderungen für den jeweiligen Produkttyp sind aus dem
Produkttypsteckbrief zu entnehmen.

In den nachfolgenden Kapiteln werden die Details zu den Teststufen (Kapitel
4.5), Testarten (Kapitel 2.5), Regressionstest (Kapitel 4.4), Systemumgebungen
(Kapitel 3) und Testdokumentation (Kapitel 4) beschrieben.

### 2.4.1 Eigenverantwortlicher Test

<table><tr><th>
Testphase

</th><th>
Eigenverantwortlicher Test

</th></tr><tr><td>
Beschreibung

</td><td>
In der Testphase „Eigenverantwortlicher Test“ werden die entwickelten
Produkte durch die Hersteller gegen die Anforderungen aus den zugrundeliegenden
Konzepten und Spezifikationen, welche in dem jeweiligen Produkttypsteckbrief
zusammengefasst sind, geprüft. Dies schließt die Erfüllung der fachlichen
Anforderungen (Ende-zu-Ende), der funktionalen technischen Anforderungen, der
nicht-funktionalen Anforderungen und der Sicherheitsanforderungen sowie eine
vollständige Integration ihres jeweiligen Produkts ein. Die Anforderungen sind
in der Regel der jeweils neusten Version einer Spezifikation bzw. eines
Konzepts zu entnehmen.

</td></tr><tr><td>
Ziel

</td><td>
Nachweis der Erfüllung der an das jeweilige Produkt gestellten Anforderungen
aus den zugrundeliegenden Konzepten und Spezifikationen.  
Nachweis der
Durchführbarkeit von den Anwendungsfällen an welchen die Produkte beteiligt
sind.

</td></tr><tr><td>
Eingangskriterien

</td><td>
Die Systemumgebung steht zur Verfügung.  
Die erforderliche Testdokumentation
wurde erstellt und geliefert (Testkonzept, einzelne Testspezifikationen, ggf.
Dokumente zu Produktausprägungen).  
Das funktionierende Testobjekt wurde
geliefert oder in der RU bereitgestellt.  
Das in Betrieb genommene Testobjekt
wurde in der Referenzumgebung vollständig installiert und konfiguriert.

</td></tr><tr><td>
Ausgangskriterien

</td><td>
Die erforderliche Testdokumentation inkl. vollständiger Testfallspezifikation
wurde erstellt und geliefert (Release Notes, Produktdokumentation,
Testprotokoll, Testbericht) und von der gematik stichprobenartig geprüft.  
Es
liegen keine zulassungstestverhindernden Probleme vor.  
Der vorab zwischen TDI
RU und Test- & Transitionmanager vereinbarte Testabdeckungsgrad und Testumfang
wurde erreicht und dokumentiert.

</td></tr><tr><td>
Testdokumentation/ Leistungsgegenstände

</td><td>
Testkonzept  
Testspezifikation inkl. Testfallspezifikationen  
Testprotokoll
der Eigenverantwortlichen Tests  
Testbericht der Eigenverantwortlichen Tests 

Release Notes  
Produktdokumentation

</td></tr><tr><td>
Teststufen

</td><td>
Produkttest (EvT)  
Produktübergreifender Test (EvT)

</td></tr><tr><td>
Systemumgebung

</td><td>
Referenzumgebung

</td></tr><tr><td>
Aufgaben des Test & Transitionmanagers

</td><td>
Prüfen, ob die Ausgangskriterien der Eigenverantwortlichen Tests erfüllt sind.
Sind die Testausgangskriterien nicht erfüllt, gilt die Testphase als nicht
abgeschlossen.

</td></tr><tr><td>
Aufgaben des TIZP

</td><td>
Anbindung des Testobjekts an das zentrale Netz und Konfiguration des zentralen
Netzes (z.B. Firewallfreischaltung, IP-Adressvergabe, DNS-Vergabe)

</td></tr><tr><td>
Aufgaben der TBI

</td><td>
Sicherstellung der Verfügbarkeit des eigenen - am Test beteiligten - Produkts
(Referenzobjekt) (detaillierte Anforderungen siehe Kapitel 3).

</td></tr><tr><td>
Aufgaben der TDI RU

</td><td>
Durchführung der Tests. Tests dürfen in Absprache mit dem Test- und
Transitionmanager auch mittels Simulatoren durchgeführt werden. 

Bereitstellung der erforderlichen Testdokumentation.  
Im Rahmen der
Testmaßnahmen die jeweils relevanten Clientsysteme berücksichtigen und in die
Testmaßnahmen einbinden.  
Den Umfang von Regressionstests bei der Planung von
Tests für neue Versionen der Fachanwendung bzw. der Produkte in Absprache mit
dem Test- & Transitionmanager der gematik festlegen.  
Pflege der eigenen Tests
im Testkalender

</td></tr><tr><td>
Pflichten Hersteller und Anbieter

</td><td>
Nach Vorgabe der gematik die qualitätssichernden Maßnahmen unterstützen und
auf Anfrage der gematik Produktmuster inkl. einer (Vorab-) Version der
Produktdokumentation liefern.  
Lieferung oder Anbindung des Testobjekts. 

Für ihren jeweiligen Produkttyp die relevanten Teststufen, Testarten und
Testdaten unterstützen.  
Bereitstellung der erforderlichen Testdokumentation.

</td></tr></table>

Die testdurchführende Instanz kann die benötigten Services zum Anbinden des
Testobjekts beim TIZP über den Servicekatalog des AZPD buchen.

**TIP1-A_6517-01 - Eigenverantwortlicher Test: TBI**

Die TBI der Referenzumgebung MUSS seine Aufgaben gemäß Tabelle Tab_Test_005
Eigenverantwortlicher Test erfüllen. **[\<=]**

**TIP1-A_6518 - Eigenverantwortlicher Test: TDI**

Die TDI der Referenzumgebung MUSS ihre Aufgaben gemäß Tabelle Tab_Test_005
Eigenverantwortlicher Test erfüllen. **[\<=]**

**TIP1-A_6519 - Eigenverantwortlicher Test: Hersteller und Anbieter**

Hersteller und Anbieter MÜSSEN im Rahmen der Eigenverantwortlichen Tests ihre
Pflichten gemäß Tabelle Tab_Test_005 Eigenverantwortlicher Test erfüllen.
**[\<=]**

### 2.4.1.1 Qualitätssichernde Maßnahmen und Produktmuster

Im Rahmen der eigenverantwortlichen Tests behält sich die gematik folgende
qualitätssichernde Maßnahmen vor:

 ---> UL

**TIP1-A_7358 - Qualität des Produktmusters**

Das Produktmuster SOLL bereits über die vollen Funktionalitäten verfügen. Die
noch nicht vollständig oder erfolgreich EvT-getesteten Funktionen SOLLEN vom
Hersteller dokumentiert werden. Abweichungen sind mit dem Test- und
Transitionmanager abzustimmen. **[\<=]**

Produktmuster haben folgende Ziele:

 ---> UL

Die Bereitstellung des Produktmusters erfolgt je nach Ausprägung durch
Lieferung an die gematik oder die frühzeitige Integration in die TU.

Im Rahmen der Produktmustervalidierung erfolgt durch die gematik keine
Güteprüfung, Abnahme der Produktmuster oder Verantwortungsübernahme im Sinne
der Produktentwicklung.

### 2.4.2 Zulassungstest

<table><tr><th>
Testphase

</th><th>
Zulassungstest

</th></tr><tr><td>
Beschreibung

</td><td>
Nachweis von Funktionalität und Interoperabilität durch den Test der gematik.
Die gematik behält sich vor, das Produkt ggf. weitgehender zu testen als dies
über die ursprüngliche im Testkonzept beschriebene Anforderungslage an die
eigenverantwortlichen Tests gefordert wird.

</td></tr><tr><td>
Ziel

</td><td>
Sicherstellung, dass die an die Produkte gestellten Anforderungen zur
funktionalen Eignung (Produkttest/Produktübergreifender Test) aus den
zugrundeliegenden Konzepten und Spezifikationen erfüllt werden. 

Sicherstellung, der Durchführbarkeit der Anwendungsfälle an denen das
Produkt beteiligt ist.

</td></tr><tr><td>
Eingangskriterien

</td><td>
 ---> UL

</td></tr><tr><td>
Ausgangskriterien

</td><td>
 ---> UL

</td></tr><tr><td>
Testdokumentation/ Leistungsgegenstände

</td><td>
 ---> UL

</td></tr><tr><td>
Teststufen

</td><td>
 ---> UL

</td></tr><tr><td>
Systemumgebung

</td><td>
Testumgebung

</td></tr><tr><td>
Aufgaben der Test- & Transitionmanager

</td><td>
Prüfen, ob die Eingangskriterien der Zulassungstests erfüllt sind. Sind die
Eingangskriterien nicht erfüllt, kann der Zulassungstest in der TU nicht
gestartet werden.  
Bei positivem Ausgang der Eingangsprüfung das jeweilige
Produkt dem Produkttest zuführen.  
Bei positivem Ausgang des Produkttests das
jeweilige Produkt dem produktübergreifenden Test zuführen.   
Die
Testdurchführung trotz ermittelter Probleme eines Produkts fortsetzen, sofern
die ermittelten Probleme es qualitativ und/oder quantitativ nicht verhindern. 

Ermittelte Probleme eines Produkts zeitnah und klassifiziert nach Schweregrad
an den Hersteller bzw. Anbieter übermitteln.  
Gewährleisten, dass Probleme
entsprechend nachfolgenden Kategorien zugeordnet werden: „Sehr schwer“,
„Schwer“, „Mittel“, „Leicht“.  
Prüfen, ob die Ausgangskriterien
der Zulassungstests erfüllt sind. Sind die Testausgangskriterien nicht
erfüllt, gilt die Testphase als nicht abgeschlossen.

</td></tr><tr><td>
Aufgaben des TIZP

</td><td>
Installation und Konfiguration des Testobjekts an das zentrale Netz (z.B.
Firewallfreischaltung, IP-Adressvergabe, DNS-Vergabe)

</td></tr><tr><td>
Aufgaben der TBI 

</td><td>
Sicherstellung der Verfügbarkeit des eigenen - am Test beteiligten - Produkts
(Referenzobjekt) (detaillierte Anforderungen siehe Kapitel 3). 

</td></tr><tr><td>
Aufgaben der TDI TU

</td><td>
Bereitstellung der erforderlichen Testdokumentation.  
Vorbereitung und
Durchführung des Zulassungstests

</td></tr><tr><td>
Pflichten Hersteller und Anbieter

</td><td>
Die Testaktivitäten in der Testumgebung gemäß den Mitwirkungspflichten im
jeweiligen Zulassungsverfahren unterstützen.  
Erstellung und Lieferung des
Testobjekts. Nach Vorgabe der gematik die qualitätssichernden Maßnahmen
unterstützen und bei Bedarf Produktmuster sowie Testdaten bzw. Testkarten
liefern/bereitstellen.  
Für ihren jeweiligen Produkttyp die relevanten
Teststufen und Testarten in unterstützen.  
Keine eigenständigen Tests
durchführen.  
Einen Ansprechpartner für Rückfragen bei den Zulassungstests
benennen.  
Änderungen am TU-Testobjekt nur in Absprache mit dem Test- &
Transitionmanager der gematik durchführen.

</td></tr></table>

**TIP1-A_6521 - Zulassungstest: TBI**

Die TBI der Testumgebung MUSS ihre Aufgaben gemäß Tabelle Tab_Test_006
Zulassungstest erfüllen. **[\<=]**

**TIP1-A_6523 - Zulassungstest: Hersteller und Anbieter**

Hersteller und Anbieter MÜSSEN im Rahmen der Zulassungstests ihre Pflichten
gemäß Tabelle Tab_Test_006 Zulassungstest erfüllen. **[\<=]**

### 2.4.2.1 Fehlerschweregrade

Die gematik verwendet für die Klassifizierung von Fehlern die folgenden
Schweregrade:

Schweregrad „Sehr schwer“: Das betroffene Testobjekt oder eine wesentliche
Funktionalität sind nicht nutzbar. Es gibt keine Problemumgehung, um die
fehlende oder fehlerhafte Funktion auszuüben. Das Testobjekt kann nicht
eingesetzt werden.Schweregrad „Schwer“: Das betroffene Testobjekt oder eine
wesentliche Funktionalität ist nur mit großen Einschränkungen nutzbar. Es
besteht die Gefahr von Datenverlust, Speicher- und Performanzproblemen. Es ist
jedoch möglich, durch eine Problemumgehung die Funktionalität zur Verfügung
zu haben. Das Testobjekt könnte auch dann nur mit Einschränkungen für die
Nutzer eingesetzt werden.Schweregrad „Mittel“: Das betroffene Testobjekt
oder eine wesentliche Funktionalität ist nur mit geringfügigen
Einschränkungen, welche nicht den Nutzer betreffen, einsetzbar.Schweregrad
„Leicht“: Die gefundenen Mängel haben keine Auswirkungen auf die
Funktionalität oder Leistungsfähigkeit des Testobjekts. Das betroffene
Testobjekt ist ohne Einschränkungen nutzbar. Es handelt sich um geringfügige
Abweichungen, wie z. B. Rechtschreibfehler in Meldungstexten.

**A_20061 - Beschreibung Art und Umfang der Fehlerkorrektur**

Der Hersteller eines Produktes MUSS auf Anfrage der gematik bei Fehlern, die im
Zulassungstests festgestellt worden sind, vor der Fehlerbehebung eine kurze
Beschreibung hinsichtlich Art und Umfang der Fehlerkorrektur an die gematik
liefern und mit ihr abstimmen. **[\<=]**

### 2.4.2.2 Testabbruch

Der Zulassungstest kann grundsätzlich in jeder Testphase bzw. Teststufe sowohl
durch den Antragsteller als auch durch die gematik abgebrochen werden.Die
gematik behält sich einen Abbruch der Zulassungstests insbesondere vor, wenn
abweichende Ergebnisse gegenüber den dokumentierten Ergebnissen zu
Eigenverantwortlichen Tests in der RU ermittelt werden oder aus den
Ergebnissen der bereits durchgeführten Testfälle hinreichend und objektiv
ersichtlich ist, dass das Testobjekt Fehler enthält, aufgrund derer eine
Zulassung nicht erteilt werden kann.Dies ist vor allem dann gegeben, wenn
wesentliche Funktionalitäten bzw. Anforderungen nicht, nicht vollständig oder
fehlerhaft umgesetzt wurden.Die gematik wird dem Antragsteller über das
Vorliegen von Gründen für einen Testabbruch, einschließlich der Auswertung
bis dahin festgestellter Fehler, schriftlich informieren.

### 2.5 Testarten

Die folgende Abbildung zeigt die Zuordnung der in diesem Kapitel beschriebenen
Testarten zu den jeweiligen Testphasen und Teststufen.

![Abbildung-4][Abbildung-4]

### 2.5.1 Güteprüfung

Die Güteprüfung ist eine statische Testart der gematik, in welcher die
Testdokumentationen der eigenverantwortlichen Tests hinsichtlich
Vollständigkeit, formaler und inhaltlicher Korrektheit, Konsistenz und
Widerspruchsfreiheit und Nachvollziehbarkeit geprüft werden. Die Ergebnisse
werden in einem Güteprüfungsprotokoll dokumentiert. Eine abgeschlossene
Güteprüfung ist eine Voraussetzung für den Abschluss der Zulassungstests der
gematik.

### 2.5.2 Funktionstest

Der Funktionstest überprüft, ob die Fachanwendung bzw. die Produkte den
funktionalen Anforderungen genügen.

Für die Tests muss es einen definierten Ausgangszustand geben (Testdaten,
Systemumgebungseinstellungen). Dieser muss nach einer Anzahl von
durchgeführten Tests wiederhergestellt werden können, um eine verlässliche
Ausgangsbasis für die Tests zu haben.

### 2.5.3 Interoperabilitätstest

Das Testziel des Interoperabilitätstests ist der Nachweis der korrekten
funktionalen Interaktion der Produkte untereinander. Die Integration erfolgt
stufenweise. Für den Interoperabilitätstest werden speziell vier
Hauptkategorien unterschieden:

 ---> UL

### 2.5.4 Leistungstest

Der Leistungstest beinhaltet die Überprüfung des geforderten Antwortzeit- und
Durchsatzverhaltens der in [gemSpec_Perf] definierten Anwendungsfälle.
Außerdem wird getestet, ob sich Produkte unter Last beim Ausfall von
aufgerufenen Produkten robust verhalten. Im Rahmen des Leistungstests werden
Einzelinstanzen oder integrierte Teilsysteme einem Leistungstest unterzogen.
Beim Leistungstest des Gesamtsystems unter Einbeziehung der dezentralen
Komponenten wird Last auf die zentralen Dienste gelegt und parallel dazu
Ende-zu-Ende-Antwortzeiten von Anwendungsfällen an der Schnittstelle
Clientsystem – TI gemessen.

### 3 Systemumgebungen

Für die Tests der Zulassungsobjekte sind die Systemumgebungen
„Referenzumgebung“ und „Testumgebung“ vorgesehen. Hierbei wird in einen
zentralen und einen dezentralen Bereich unterschieden.

Die folgende Tabelle listet auf, was die Systemumgebungen für die Tests leisten
sollen.

<table><tr><th>
Systemumgebung

</th><th>
Ziele

</th><th>
Teststufe

</th></tr><tr><td>
Referenzumgebung

</td><td>
 ---> UL

Anbietern und Herstellern wird Zugang zur RU in Abstimmung mit der gematik
gewährt, sofern diese relevante Produkte anpassen und bereitstellen.

</td><td>
 ---> UL

</td></tr><tr><td>
Testumgebung

</td><td>
 ---> UL

</td><td>
 ---> UL

</td></tr></table>

Die strikte Trennung von Produktivbetrieb und Testbetrieb bezüglich der
Verwendung von Daten ist essentiell. Einerseits muss sichergestellt werden,
dass in der Referenzumgebung und in der Testumgebung keine Echtdaten verwendet
werden. Es dürfen nur Testdaten und entsprechend auch Testkarten [gemSpec_TK]
verwendet werden.

Die Einhaltung dieser strikten Trennung wird durch technische Maßnahmen (z. B.
physikalische Trennung der Netze, Einbau von Prüfroutinen für Testkarten) und
organisatorische Maßnahmen (z. B. Vorschreiben der Verwendung von Testkarten)
sichergestellt.

Produkte müssen im Sinne dieser Trennung ebenfalls für jede Systemumgebung
separat bereitgestellt werden. Hierbei sind grundsätzlich folgende Quellen
für Mengengerüste zu beachten:

RU: Anzahl der Produkte wird von den Herstellern und Anbietern bzw. der
testdurchführenden Instanz der RU verantwortet

TU: Anzahl der Produkte ergibt sich aus der Spezifikation bzw. für dezentrale
Produkte aus der Verfahrensbeschreibung der Zulassung

Alle Testmaßnahmen in der Referenz- und Testumgebung werden mit Testdaten
durchgeführt. Diese werden von Herstellern, Anbietern und Kartenherausgebern
zur Verfügung gestellt, sofern es sich um einen Produkttyp handelt, der Daten
in die TI liefert. Das Einbringen von Echtdaten ist in diese Systemumgebungen
nicht erlaubt.

Testkarten für die eigenverantwortlichen Tests eines Zulassungsnehmers können
über die gematik-Website bestellt werden.

**TIP1-A_4923 - Dauerhafte Verfügbarkeit RU und TU**

Die jeweilige Testbetriebsinstanz (TBI) der Referenzumgebung und der
Testumgebung MUSS sicherstellen, dass ihre Produkte dauerhaft zur Verfügung
stehen. **[\<=]**

**TIP1-A_2724 - TBI verantwortet Betrieb RU und TU**

Die jeweilige Testbetriebsinstanz MUSS den technischen Betrieb in der
Referenzumgebung und in der Testumgebung für ihr jeweiliges Referenzobjekt
verantworten. **[\<=]**

### 3.1 Testobjekte

Die folgende Grafik gibt eine Übersicht des Gesamtsystems TI und der Verteilung
der Produkttypen der TI:

![Abbildung-5][Abbildung-5]

<table><tr><th colspan="2">
TI-Plattform zentral

</th><th>
Bereitstellung

</th></tr><tr><td colspan="2">
CVC-Root

</td><td>
1x für RU/TU

</td></tr><tr><td colspan="2">
gematik Root-CA

</td><td>
1x für RU/TU

</td></tr><tr><td colspan="2">
Konfigurationsdienst

</td><td>
1x für RU, 1x für TU

</td></tr><tr><td colspan="2">
Namensdienst

</td><td>
1x für RU, 1x für TU

</td></tr><tr><td colspan="2">
OCSP-Responder Proxy

</td><td>
1x für RU, 1x für TU

</td></tr><tr><td colspan="2">
Sicherheitsgateway Bestandsnetze

</td><td>
1x für RU/TU

</td></tr><tr><td colspan="2">
Störungsampel

</td><td>
1x für RU, 1x für TU

</td></tr><tr><td colspan="2">
TSL-Dienst

</td><td>
1x für RU, 1x für TU

</td></tr><tr><td colspan="2">
VPN-Zugangsdienst

</td><td>
1x für TU

</td></tr><tr><td colspan="2">
Zeitdienst

</td><td>
1x für RU/TU

</td></tr><tr><td colspan="2">
Zentrales Netz

</td><td>
1x für RU, 1x für TU

</td></tr><tr><td colspan="2">
Zentraler Verzeichnisdienst

</td><td>
1x für RU, 1x für TU

</td></tr><tr><td colspan="2">
Service Monitoring

</td><td>
1x für RU, 1x für TU

</td></tr><tr><td colspan="2">
Schlüsselgenerierungsdienst

</td><td>
1x für RU, 1x für TU

</td></tr><tr><td colspan="3" rowspan="1">
Trust Service Provider zentral

</td></tr><tr><td rowspan="2">
TSP X.509 nonQES

</td><td>
OCSP-Responder Komponenten

</td><td>
1x für RU, 1x für TU

</td></tr><tr><td>
CA-Instanz Komponenten (inkl. Datenbank)

</td><td>
1x für RU/TU

</td></tr><tr><td>
Trust Service Provider CVC

</td><td>
Komponenten

</td><td>
1x für RU/TU

</td></tr><tr><td colspan="3" rowspan="1">
Trust Service Provider dezentral

</td></tr><tr><td rowspan="6">
TSP X.509 nonQES

</td><td>
OCSP-Responder eGK

</td><td>
1x für RU/TU

</td></tr><tr><td>
CA-Instanz eGK (inkl. Datenbank)

</td><td>
1x für RU/TU

</td></tr><tr><td>
OCSP-Responder HBA

</td><td>
1x für RU/TU

</td></tr><tr><td>
CA-Instanz HBA (inkl. Datenbank)

</td><td>
1x für RU/TU

</td></tr><tr><td>
OCSP-Responder SMC-B

</td><td>
1x für RU/TU

</td></tr><tr><td>
CA-Instanz SMC-B (inkl. Datenbank)

</td><td>
1x für RU/TU

</td></tr><tr><td rowspan="2">
Trust Service Provider CVC

</td><td>
HBA

</td><td>
1x für RU/TU

</td></tr><tr><td>
SMC-B

</td><td>
1x für RU/TU

</td></tr><tr><td rowspan="2">
Trust Service Provider X.509 ES

</td><td>
OCSP-Responder HBA

</td><td>
1x für RU/TU

</td></tr><tr><td>
CA-Instanz HBA (inkl. Datenbank)

</td><td>
1x für RU/TU

</td></tr><tr><td colspan="3" rowspan="1">
TI-Plattform dezentral

</td></tr><tr><td colspan="2">
eGK

</td><td>
---

</td></tr><tr><td colspan="2">
eHealth-Kartenterminal

</td><td>
1x für TU

</td></tr><tr><td colspan="2">
gSMC-K

</td><td>
---

</td></tr><tr><td colspan="2">
gSMC-KT

</td><td>
---

</td></tr><tr><td colspan="2">
HBA

</td><td>
---

</td></tr><tr><td colspan="2">
Konnektor

</td><td>
1x für TU

</td></tr><tr><td colspan="2">
Mobiles Kartenterminal

</td><td>
1x für TU

</td></tr><tr><td colspan="2">
SMC-B

</td><td>
---

</td></tr><tr><td colspan="2" rowspan="1">
KTR-Consumer

</td><td>
1x TU

</td></tr><tr><td colspan="2" rowspan="1">
KTR-AdV

</td><td>
1x TU

</td></tr><tr><td colspan="3" rowspan="1">
Sichere Übermittlungsverfahren

</td></tr><tr><td rowspan="2">
KOM-LE

</td><td>
Clientmodul KOM-LE

</td><td>
1x für TU

</td></tr><tr><td>
Fachdienst KOM-LE

</td><td>
1x für RU, 1x für TU

</td></tr><tr><td colspan="3" rowspan="1">
Fachanwendungen

</td></tr><tr><td rowspan="4">
VSDM

</td><td>
Intermediär VSDM

</td><td>
1x für TU

</td></tr><tr><td>
Fachdienst UFS

</td><td>
1x für RU, 1x für TU

</td></tr><tr><td>
Fachdienst VSDD

</td><td>
1x für RU, 1x für TU

</td></tr><tr><td>
Fachdienst CMS

</td><td>
1x für RU, 1x für TU

</td></tr><tr><td rowspan="4">
ePA

</td><td>
ePA-Aktensystem

</td><td>
1x für RU, 1x für TU

</td></tr><tr><td>
ePA-Frontend des Versicherten

</td><td>
1x für TU

</td></tr><tr><td>
Signaturdienst

</td><td>
1x für RU, 1x für TU

</td></tr><tr><td>
Schlüsselgenerierungsdienst

</td><td>
1x für RU, 1x für TU

</td></tr><tr><td colspan="1" rowspan="3">
E-Rezept

</td><td>
E-Rezept-Fachdienst

</td><td>
1x für RU, 1x für TU

</td></tr><tr><td>
IDP

</td><td>
1x für RU, 1x für TU

</td></tr><tr><td>
Apothekenverzeichnis

</td><td>
1x für RU/TU

</td></tr></table>

**TIP1-A_6526 - Produkttypen: Bereitstellung**

Die Hersteller oder Anbieter eines Produkttyps MÜSSEN ihr Produkt pro Version
gemäß Tabelle Tab_Test_019 Produkttypen der TI vorsehen. **[\<=]**

**TIP1-A_5053 - Nutzbarkeit Konnektor in RU/TU und PU**

Der Hersteller / Anbieter eines Konnektors MUSS sicherstellen, dass dieser in
allen Systemumgebungen (RU/TU und PU) betreibbar ist. Hierbei MUSS der Wechsel
des Vertrauensankers und die Erkennung der unterschiedlichen Systemumgebung
berücksichtigt werden. **[\<=]**

**TIP1-A_6527 - Testkarten**

Die jeweiligen testdurchführenden Instanzen (TDI) der Referenzumgebung und der
Testumgebung MÜSSEN sicherstellen, dass für den Testbetrieb nur die
Testkarten verwendet werden, die gemäß der [gemSpec_TK] befüllt sind.
**[\<=]**

Neben den Produkttypen der TI-Plattform sind für die Tests der TI-Plattform
ggf. Clientsysteme erforderlich, insbesondere für den Produktübergreifenden
Test. Clientsysteme sind dezentrale Systeme (mit Hard- und/oder
Software-Bestandteilen), die als Clients mit der TI interagieren, aber selbst
nicht als Bestandteil der TI betrachtet werden (z. B. PVS, AVS, KIS, E-Mail-
Clients).

### 3.2 Anforderungen an die Systemumgebungen

In den folgenden Kapiteln sind nach Themengebieten geordnet die Anforderungen
aufgeführt, die die Systemumgebungen bzw. die jeweiligen Zulassungsnehmer
erfüllen müssen.

### 3.2.1 Trennung der Netzwerke

**TIP1-A_3194 - Informationstechnische Trennung PU von RU/TU**

Der TIZP MUSS sicherstellen, dass die RU und die TU von der PU dadurch
informationstechnisch getrennt werden, dass unterschiedliche Namensräume,
Vertrauensräume und Kommunikationspfade eingerichtet werden. **[\<=]**

**TIP1-A_3195 - Logische Trennung RU und TU**

Der TIZP MUSS sicherstellen, dass die Referenzumgebung von der Testumgebung bis
zu den Zugangspunkten des Zentralen Netzes logisch separiert ist. **[\<=]**

**TIP1-A_2710 - Netzwerktechnologie Testumgebung**

Der TIZP MUSS für die Testumgebung die identische Netzwerktechnologie wie in
der Produktivumgebung verwenden. **[\<=]**

### 3.2.2 Trennung der Vertrauensräume

**TIP1-A_2713 - Separate Vertrauensräume**

Der TIZP MUSS sicherstellen, dass neben dem Vertrauensraum der Produktivumgebung
genau ein davon völlig separierter und rückwirkungsfreier Vertrauensraum für
die Referenzumgebung und die Testumgebung eingerichtet werden
(Nicht-Produktiv-Vertrauensraum). **[\<=]**

**TIP1-A_3016 - Nutzung Nicht-Produktiv-Vertrauensraum für RU und TU**

Der TIZP MUSS sicherstellen, dass der für die Testsysteme definierte
Vertrauensraum gleichermaßen für die Referenzumgebung und Testumgebung
genutzt werden kann. **[\<=]**

**TIP1-A_4191 - Keine Echtdaten in RU und TU**

Die jeweiligen testdurchführenden Instanzen (TDI) der Referenzumgebung und der
Testumgebung MÜSSEN sicherstellen, dass keine Echtdaten in die
Referenzumgebung und in die Testumgebung eingebracht werden. **[\<=]**

**TIP1-A_4928 - Testidentitäten für RU und TU**

Der TIZP MUSS sicherstellen, dass nicht smartcard-basierte Testidentitäten (z.
B. Softwarezertifikate) für Geräte in der Referenzumgebung und der
Testumgebung bereitgestellt werden. **[\<=]**

**GS-A_2162 - Kryptographisches Material in Entwicklungs- und Testumgebungen**

Die jeweiligen testdurchführenden Instanzen (TDI) und die jeweilige
Testbetriebsinstanz (TBI) der Referenzumgebung und der Testumgebung MÜSSEN
sicherstellen, dass in diesen Umgebungen keine kryptographischen Identitäten
bzw. Schlüssel der Produktivumgebung der TI (Umgebungen mit Echtdaten) genutzt
werden. **[\<=]**

### 3.2.3 Gemeinsame Eigenschaften für alle Systemumgebungen

**TIP1-A_5049 - Betriebliche Umsetzung von Teststufen**

Der TIZP MUSS die Durchführbarkeit einzelner Teststufen in der jeweiligen
Systemumgebung sicherstellen. **[\<=]**

### 3.2.4 Gemeinsame Eigenschaften der Referenz- und Testumgebung

**TIP1-A_2718 - Betriebliche Zielstellungen in RU und TU**

Der TIZP MUSS sicherstellen, dass alle Systemumgebungen entsprechend der
Vorgaben aus den übergreifenden Richtlinien zum Betrieb der TI [gemRL_Betr_TI]
ausgeprägt sind. **[\<=]**

**TIP1-A_4930 - Automatisierung von Tests**

Die testdurchführenden Instanzen der Referenzumgebung und der Testumgebung
SOLLEN Tests automatisieren. **[\<=]**

**TIP1-A_3360 - Zentraler Anlaufpunkt für Anfragen und Probleme in RU und TU**

Der TIZP MUSS sicherstellen, dass in der Referenzumgebung und in der
Testumgebung ein zentraler Anlaufpunkt für Anfragen und Probleme hinsichtlich
Bereitstellung sowie Integration von Produkten und des Betriebs der RU oder TU
eingerichtet wird. **[\<=]**

**TIP1-A_2720 - RU/TU: Funktionales Abbild der Produktivumgebung**

Die jeweilige TBI MUSS sicherstellen, dass die Produkte der Referenzumgebung und
Testumgebung bei laufendem Produktivbetrieb ein funktionales Abbild (Produkte
und Konfigurationen) der Produkte der Produktivumgebung sind. **[\<=]**

**TIP1-A_2726 - Bestandteile RU und TU**

Die jeweilige TBI MUSS sicherstellen, dass ihre zugelassenen Produkte
(Referenzobjekte) in der Referenzumgebung und der Testumgebung enthalten sind,
die durch die Architekturen der TI-Plattform und der Fachprojekte festgelegt
wurden. **[\<=]**

**TIP1-A_2727 - Sicherstellung der Kommunikation in RU und TU**

Der TIZP MUSS sicherstellen, dass in der Referenzumgebung und in der
Testumgebung die gleiche Netzwerkarchitektur wie in der Produktivumgebung
genutzt wird. **[\<=]**

**TIP1-A_2722-01 - TBI integriert die Produkttypen in seine Systemumgebung**

Die jeweilige TBI MUSS Testobjekte und Referenzobjekte in die Referenzumgebung
und die Testumgebung integrieren. **[\<=]**

**TIP1-A_3017 - Systemumgebungsmanagement RU sowie TU**

Die jeweilige TBI MUSS sicherstellen, dass das Systemumgebungsmanagement
unterschiedliche Konfigurationen und Wiederherstellungspunkte für die
Referenzumgebung und Testumgebung ermöglicht (Testdatenbestand,
Konfigurationseinstellungen, Versionen).Die Fachdienstbetreiber VSDM müssen
keine älteren Konfigurationseinstellungen und Versionen bereitstellen.
**[\<=]**

**TIP1-A_3361 - Dokumentation für den Betrieb in der RU und TU bereitstellen**

Die TBI MUSS sicherstellen, dass alle erforderlichen Dokumente (z.B. der
Netzplan) für den Betrieb der Referenzumgebung und der Testumgebung den
Beteiligten vor Testbeginn zur Verfügung gestellt werden. **[\<=]**

**TIP1-A_6083 - Anzahl der Fachdienste als Referenzobjekte**

Es SOLLEN mindestens zwei Fachdienste VSDM in TU und RU permanent als
Referenzobjekt zur Verfügung stehen. Eine Abstimmung und die Koordination
findet über den Test & Transitionmanager der gematik statt. Ausnahmen für die
Verfügbarkeit von weniger als zwei Fachdiensten als Referenzobjekte SOLLEN mit
dem Test & Transitionmanager der gematik abgestimmt werden. **[\<=]**

### 3.2.5 Exklusiver Zugriff

**TIP1-A_2737 - Exklusiver Zugriff bestimmter Akteure**

Der TIZP MUSS sicherstellen, dass auf Anfrage der jeweiligen testdurchführenden
Instanz (Zulassungsnehmer) der jeweiligen Systemumgebung ein zeitlich
exklusiver und diskriminierungsfreier Zugriff auf Produkte,
Fachdienstschnittstellen und Kommunikationspfade in der Referenzumgebung bzw.
in der Testumgebung in Abstimmung mit der TKI der gematik bereit gestellt
werden kann. **[\<=]**

**TIP1-A_2738 - Exklusiver Zugriff organisatorisch**

Die jeweilige TBI SOLL den zeitlich exklusiven Zugriff für bestimmte Akteure
(Personen, Produkte, Testwerkzeuge) in der Referenzumgebung und in der
Testumgebung durch organisatorische Maßnahmen unterstützen. **[\<=]**

**TIP1-A_2739 - Exklusiver Zugriff technisch unterstützt**

Der TIZP SOLL den zeitlich exklusiven Zugriff für bestimmte Akteure (Personen,
Produkte, Testwerkzeuge) in der Referenzumgebung und in der Testumgebung durch
technische Mittel unterstützen. **[\<=]**

### 3.2.6 Logging

Die in diesem Kapitel beschriebenen Anforderungen an ein Logging beziehen sich
auf die RU und TU. In diesen Systemumgebungen werden keine Echtdaten
verarbeitet. Grundsätzlich sind alle Logging-Daten vertraulich. Eine
Weitergabe und die Festlegung der Form der Weitergabe erfolgt ausschließlich
durch die gematik.

**TIP1-A_2740 - Logging von Produktaußenaktivitäten**

Der TIZP MUSS für ein detailliertes Logging von Aktivitäten an
Außenschnittstellen aller am Test beteiligten Produkte mit Hilfe geeigneter
Testwerkzeuge in der Referenzumgebung und Testumgebung sorgen (Produkte als
Black-Box). **[\<=]**

**TIP1-A_2745 - Außenlogging zeitgleich mit Produktbereitstellung**

Der TIZP MUSS sicherstellen, dass zeitgleich mit der Bereitstellung von
Produkten für die TI das Loggen an den Außenschnittstellen der betreffenden
Produkte in der Referenzumgebung und Testumgebung erfolgen kann. **[\<=]**

**TIP1-A_2741 - Logging auf Applikationsebene**

Der TIZP MUSS sicherstellen, dass Außenaktivitäten von allen am Test
beteiligten Produkten in der Referenzumgebung und Testumgebung auf
Applikationsebene protokolliert werden. **[\<=]**

**TIP1-A_2742 - Logging von Aktivitäten auf Transportebene**

Der TIZP MUSS sicherstellen, dass Außenaktivitäten von allen am Test
beteiligten Produkten in der Referenzumgebung und Testumgebung auf
Transportebene protokolliert werden. **[\<=]**

**TIP1-A_2743 - Logging von Aktivitäten auf Netzwerkebene**

Der TIZP MUSS sicherstellen, dass Außenaktivitäten von allen am Test
beteiligten Produkten in der Referenzumgebung und Testumgebung auf
Netzwerkebene protokolliert werden. **[\<=]**

**TIP1-A_3362 - Bereitstellung Logdaten in RU und TU**

Der TIZP MUSS sicherstellen, dass die Logdaten der am Test beteiligten Produkte
sofort nach deren Erzeugung der testdurchführenden Instanz der betreffenden
Systemumgebung zur Verfügung gestellt werden. **[\<=]**

**TIP1-A_7330 - Tracedaten von echten Außenschnittstellen**

Die testdurchführende Instanz SOLL seine eigenverantwortlichen Tests an den
Außenschnittstellen des Testobjekts und nicht an internen Loopback Devices
durchführen. **[\<=]**

**TIP1-A_7331 - Bereitstellung von Tracedaten an Außenschnittstelle**

Die testdurchführende Instanz SOLL bei eigenverantwortlichen Tests an denen an
der Außenschnittstelle des Produkts Daten transferiert werden der gematik
einen Mitschnitt zur Verfügung stellen, der die folgenden Punkte erfüllt:

• vollständig sein (komplette Paketgröße und gesamte MTU-Size)

• tatsächlichen Daten (insbesondere Messdaten, wie z. B. Zeitstempel)
enthalten

• ein auswertbares Format, (z. B. pcap oder pcapng) haben

• und bei Mitschnitt verschlüsselter Protocol-Layer (z.B. TLS-Layer) und
Nutzung eines Simulators als Peer, das Mastersecret als separate Datei
bereitstellen. **[\<=]**

Sollte das in der Anforderung TIP1-A_7331 angegebene Format nicht verwendbar
sein, kann in Absprache mit dem TTM auch ein anderes Format verwendet werden.

### 3.2.7 Testwerkzeuge

**TIP1-A_2731 - Integration von Testwerkzeugen in RU und TU**

Der TIZP MUSS in der Referenzumgebung und in der Testumgebung die Möglichkeit
bieten, Testwerkzeuge hardware- und softwaremäßig zu integrieren. Der TIZP
MUSS den Zugriff und die Nutzung dieser Testwerkzeuge der jeweiligen
testdurchführenden Instanz jederzeit gewähren und sicherstellen. Der TIZP
MUSS der testdurchführenden Instanz die entsprechenden Rechte auf dem
Testwerkzeug gewähren. **[\<=]**

**TIP1-A_2735 - Testwerkzeug Netzwerk-Sniffer**

Der TIZP MUSS sicherstellen, dass er den Netzwerkverkehr auf allen
Netzwerkmedien bis zu den Zugangspunkten des Zentralen Netzes der TI durch
Netzwerk-Sniffer ohne Paketverluste und rückwirkungsfrei in Referenz- und
Testumgebung mitschneiden kann.Der Mitschnitt MUSS vollständig (komplette
Paketgröße und gesamte MTU-Size), mit tatsächlichen Daten (insbesondere
Messdaten, wie z. B. Zeitstempel) und in einem auswertbaren Format (pcap)
erfolgen. **[\<=]**

**TIP1-A_7332 - Bereitstellung Remotezugang zu Netzwerksniffer**

Der TIZP MUSS der testdurchführenden Instanz einen sicheren Zugang (z.B. SSH)
zum Steuern der Netzwerksniffer bereitstellen. **[\<=]**

**A_13505 - Bereitstellung von Log- und Tracedaten**

Der TIZP MUSS Log- und Trace-Daten der jeweiligen testdurchführenden Instanz
unmittelbar nach deren Generierung bereitstellen. **[\<=]**

**TIP1-A_2751 - Flexibel einstellbarer Sniffing-Detaillierungsgrad**

Der TIZP MUSS sicherstellen, dass der Detaillierungsgrad der durch
Netzwerk-Sniffer mitgeschnittenen Netzwerkdaten aller am Test beteiligten
Produkte in der Referenzumgebung und Testumgebung flexibel (Dauer, Detailierung
und Umfang) einstellbar ist. **[\<=]**

**TIP1-A_2736 - Testwerkzeug Man-in-the-Middle-Box**

Der TIZP MUSS sicherstellen, dass die Referenzumgebung und Testumgebung die
Möglichkeit bieten, zeitlich begrenzt den Netzwerkverkehr auf allen
Netzwerkmedien durch Man-in-the-Middle-Boxen hindurchzuleiten, um
Netzwerkpakete gezielt zu unterdrücken, umzuordnen oder zu modifizieren sowie
Replay-Attacken und Penetrationstests durchzuführen. **[\<=]**

**TIP1-A_2732 - Zentrale Sammelstelle für Logdaten**

Der TIZP MUSS sicherstellen, dass für die Referenzumgebung und für die
Testumgebung je eine zentrale Speichermöglichkeit bereitgestellt wird für:

 ---> UL

**[\<=]**

**TIP1-A_2734 - Separate Netzwerkanbindung für Test**

Der TIZP MUSS für die Referenzumgebung und für die Testumgebung separate
Netzwerkanschlüsse für Testwerkzeuge bereitstellen. Die gematik wird über
diese Anschlüsse eigene Laborumgebungen anbinden. **[\<=]**

**A_15593 - Ersatz bei defekten dezentralen Produkten**

Bei Schäden am Gerät, die üblicherweise über Garantie- bzw.
Gewährleistungen geregelt werden, MUSS der Hersteller von dezentralen
Komponenten diese reparieren oder ersetzen. Ebenso MUSS der Hersteller die
regelmäßigen Wartungsarbeiten (wie z.B. Batteriewechsel oder
Zertifikatstausch) ermöglichen/unterstützen, so dass die gematik die
Testbereitschaft aufrechterhalten kann. **[\<=]**

**A_15594 - Vorhalten testbereiter dezentraler Komponenten**

Ein Hersteller eines zugelassenen dezentralen Produktes (außer AdV-Server) MUSS
der gematik für die Tests im Rahmen der Zulassungsverfahren von jeder
zugelassenen Produktversion auf Aufforderung der gematik innerhalb von einer
Woche unentgeltlich für einen von der gematik festgelegten Zeitraum zwei
Geräte zur Verfügung stellen. Darüber hinaus kann der Hersteller für
angeforderte Geräte einen marktüblichen Preis verlangen. **[\<=]**

### 3.2.8 Test- und Referenzobjekte

Referenzobjekte

Als Basis für eigenverantwortliche Tests (RU) und Zulassungstests (TU) sind
Abbilder der in der PU vorhandenen Komponenten der TI erforderlich (gleiche
Produkttypversion). Diese werden als Referenzobjekte bezeichnet. Gegen sie wird
das aktuelle Testobjekt des Zulassungsnehmers getestet. Deren vollständigen
Betrieb und die Erbringung des zugehörigen Service Levels verantwortet der
jeweilige Anbieter entsprechend [gemRL_Betr_TI]. Referenzobjekte unterliegen
den Vorgaben des betrieblichen Changeprozesses und können über den
TI-Servicekatalog konfiguriert werden. Anfragen zu Konfigurationen an
Fachdienste werden über den Test- und Transitionmanager der gematik gesteuert.

Referenzobjekte können nur in Absprache mit der gematik Simulatoren sein.

Testobjekte

Testobjekte sind Produkte eines Zulassungsnehmers, welche über die Tests in RU
und TU eine Zulassung, Bestätigung oder Freigabe der gematik erhalten sollen.
Das Einbringen und Herausnehmen aus der jeweiligen Betriebsumgebung (RU/TU)
erfolgt über das betriebliche Change Management. In der Referenzumgebung kann
ein Testobjekt jederzeit durch den Zulassungsnehmer konfiguriert und/oder
angepasst werden. Eigenverantwortliche Tests müssen für alle Beteiligten der
RU im Testkalender der gematik sichtbar gemacht werden. In der Testumgebung
unterliegt das Testobjekt den Vorgaben des Test- und Transitionmanagers der
gematik. Jegliche Anpassungen müssen mit ihm abgestimmt werden.

**TIP1-A_6084 - Konfigurationen und Dienste im Servicekatalog**

Anbieter des VPN-Zugangsdienstes MÜSSEN für ihr Referenzobjekt in der TU
Konfigurationen und Dienste, welche für den Test der gematik genutzt werden,
in einem Servicekatalog zu marktüblichen Konditionen anbieten. Der
Mindestumfang ist in der Tabelle „Inhalte und Bedingungen des
Servicekatalogs“ beschrieben.

Tabelle5: Inhalte und Bedingungen des Servicekatalogs

<table><tr><th>
Service-Beschreibung

</th></tr><tr><td>
Remote-Anbindung via Internet im Rahmen des Zulassungstests in der TU im
gematik-Zulassungsverfahren. Beinhaltet die Nutzung, Bereitstellung von
Registrierungsinformationen und Dokumentation für die Remote-Anbindung an den
VPN-Zugangsdienst der TU.

</td></tr><tr><td>
Testunterstützung „Remote“ im Rahmen des Tests in der TU für die gematik.
Allgemeine Test- und Problemlösungsunterstützung, insb. das Bereitstellen von
Log und Debug-Informationen im Rahmen des Tests in der TU. Beinhaltet die
Nutzung, Bereitstellung von Registrierungsinformationen und Dokumentationen
für die Remote-Anbindung an den VPN-Zugangsdienst der TU.

</td></tr><tr><td>
Testunterstützung der gematik.

</td></tr><tr><td>
Datenlieferung für die zentrale Störungsampel im Rahmen des Betriebs in der TU
für Serviceprovider SPZD in der Haupt- und Nebenzeit.

</td></tr></table>

**[\<=]**

**TIP1-A_6079 - Updates von Referenzobjekten**

Die Hersteller bzw. Anbieter von Referenzobjekten MÜSSEN Hotfixes, Patches und
Updates für die Systemumgebungen einspielen oder zur Verfügung stellen.
**[\<=]**

**TIP1-A_6080 - Softwarestand von Referenzobjekten**

Die Hersteller bzw. Anbieter von Referenzobjekten SOLLEN dafür sorgen, dass der
Software-Stand bzw. Versions- oder Patchstand dem der Komponenten der PU
entspricht. **[\<=]**

**TIP1-A_6081 - Bereitstellung der Referenzobjekte**

Hersteller und Anbieter von Komponenten der TI-Plattform Zone zentral und der
Provider Zone MÜSSEN in RU und TU Referenzobjekte bereitstellen, welche ein
funktionales Abbild der PU-Komponente sind. **[\<=]**

**TIP1-A_6093 - Ausprägung der Referenzobjekte**

Möchte ein Hersteller oder Anbieter von Komponenten der TI-Plattform Zone
zentral und der Provider Zone die Ausprägung seines Referenzobjektes anpassen,
so MUSS dies in Abstimmung mit dem Test- und Transition-Manager der gematik
geschehen. **[\<=]**

**TIP1-A_6082 - Versionen der Referenzobjekte**

Sollten mehrere Versionen eines Produkts der TI-Plattform Zone dezentralbzw. der
Personal Zonein der PU betrieben werden, so MUSS der Hersteller bzw. Anbieter
dafür sorgen, dass alle Versionen als Referenzobjekte in RU und TU zur
Verfügung stehen. Von der Anforderung unberührt gelten die Festlegungen in
Tab_Test_019. So muss beispielsweise keine Version des ePA-Frontend des
Versicherten in der RU bereitgestellt werden. **[\<=]**

**TIP1-A_6088 - Unterstützung bei Fehlernachstellung**

Der Zulassungsnehmer eines Produkts MUSS bei der Fehlernachstellung, an denen
sein Produkt beteiligt ist, die gematik bzw. einen Dritten unterstützen.
**[\<=]**

**A_20059 - Festlegung von Konfiguration von Produktinstanzen durch die gematik**

Ein Hersteller MUSS für den Zeitraum des Zulassungstests auf Anfrage der
gematik die Konfiguration seiner Produktinstanz auf von der gematik festgelegte
Werte anpassen. **[\<=]**

**A_20060 - Versionierung der Konfiguration von Produktinstanzen**

Der Hersteller MUSS für den Zeitraum des Zulassungstests die Konfigurationen
seiner Produktinstanz versionieren und rückspielbar ablegen sowie auf Anfrage
der TDI TU jederzeit eine detaillierte Auskunft über die verwendete
Konfiguration bereitstellen. **[\<=]**

### 3.2.9 Referenzumgebung

### 3.2.9.1 Qualitätssicherungsmaßnahmen der Hersteller und Anbieter

**TIP1-A_2757 - Qualitätssicherungsmaßnahmen der Hersteller und Anbieter**

Der TIZP MUSS in der Referenzumgebung die Qualitätssicherungsmaßnahmen der
Hersteller und Anbieter zur Erzielung einer Zulassungseignung für die durch
die Hersteller und Anbieter umzusetzenden Produkte der TI ermöglichen.
**[\<=]**

**TIP1-A_4124 - Aufbau RU**

Der TIZP MUSS sicherstellen, dass alle erforderlichen Testobjekte, Testwerkzeuge
und Kommunikationspfade bereitgestellt und verfügbar gehalten werden. **[\<=]**

**TIP1-A_2758 - Ermöglichen von Tests im Rahmen einer (Teil-)Integration (RU)**

Der TIZP MUSS in der Referenzumgebung Tests im Rahmen einer (Teil-)Integration
ermöglichen. **[\<=]**

**TIP1-A_2760 - Performance**

Die TBI KANN die Performance (Durchsatz, Bearbeitungszeit) seiner Dienste in
der Referenzumgebung in Abstimmung mit der testkoordinierenden Instanz auch
abweichend von der Performance der Produktivumgebung vorgeben. **[\<=]**

### 3.2.9.2 Weiterentwicklung der Referenzumgebung

**TIP1-A_5052 - Dauerhafte Verfügbarkeit in der RU**

Hersteller und Anbieter von Produkten der TI MÜSSEN mindestens eine konkrete
Ausprägung von jedem Produkttyp dauerhaft in der Referenzumgebung zur
Verfügung stellen. **[\<=]**

### 3.2.9.3 Nutzung der Referenzumgebung

**TIP1-A_2766 - Zugang zur Referenzumgebung durch gematik**

Der TIZP MUSS der gematik Zugang zur Referenzumgebung gewähren, um ihre
Testwerkzeuge einzubringen und diese für den Einsatz in der Testumgebung
weiter entwickeln zu können. **[\<=]**

**TIP1-A_2767 - Splittung der Referenzumgebung**

Der TIZP KANN die Referenzumgebung auf der Ebene von Instanzen von Produkten der
TI oder durch Virtualisierung in eine oder mehrere Referenzumgebungen splitten.
**[\<=]**

### 3.2.9.4 Instanzen der Referenzumgebung

**TIP1-A_2768 - Zweck von Instanzen der Referenzumgebung**

Der TIZP SOLL in der Referenzumgebung durch Bereitstellung von Instanzen von
Komponenten der TI die ungestörte, selbständige und unabhängige
Testdurchführung für die Entwicklung und Herstellung von TI-Produkten durch
die Hersteller und Anbieter ermöglichen. **[\<=]**

**TIP1-A_6538 - Durchführung von Produkttests**

Der TIZP MUSS in der Referenzumgebung die Durchführung von Produkttests
ermöglichen. **[\<=]**

**TIP1-A_6539 - Durchführung von Produktübergreifenden Tests**

Der TIZP MUSS in der Referenzumgebung die Durchführung von
Produktübergreifenden Tests ermöglichen. **[\<=]**

**TIP1-A_2773 - Simulatoren als Ersatz für Dienste**

Die TDI KANN zentrale Dienste und fachanwendungsspezifische Dienste für EvT in
den Produkttests durch Simulatoren ersetzen. **[\<=]**

**TIP1-A_2775 - Performance in RU**

Die testdurchführende Instanz der Referenzumgebung SOLL in der Referenzumgebung
das Leistungsverhalten der zuzulassenden Komponente simulieren und die
Einhaltung der Leistungsanforderungen prüfen. **[\<=]**

### 3.2.10 Testumgebung

### 3.2.10.1 Bestandteile der Testumgebung

**TIP1-A_6085 - Referenzobjekte eines Produkts**

Nach Zulassung eines Produkts der TI-Plattform Zone zentral sowie des
Intermediärs VSDM und der Fachdienste ePA MUSS der Hersteller oder Anbieter
dieses als Referenzobjekt in der TU bereitstellen. Die Bereitstellung bezieht
sich auf den Zeitraum, in dem das Produkt in der TI (PU) eingesetzt wird.
**[\<=]**

**TIP1-A_6086 - Unterstützung bei Anbindung eines Produktes**

Der Zulassungsnehmer MUSS nach erfolgter Zulassung die Anbindung der
Referenzobjekte produktseitig unterstützen. Dies entfällt, wenn das bereits
vorhandene Testobjekt zum Referenzobjekt wird. **[\<=]**

**TIP1-A_2783 - Marktübliche Testwerkzeuge**

Der TIZP MUSS marktübliche Testwerkzeuge und Testtreiber dauerhaft in der
Testumgebung zur Verfügung stellen. Hierzu gehört z. B. Wireshark. **[\<=]**

**TIP1-A_2785 - Simulatoren für Fehleranalyse**

Der TIZP MUSS in der Testumgebung sicherstellen, dass Simulatoren, die er für
eigene Tests genutzt hat, erhalten bleiben. **[\<=]**

**TIP1-A_6087 - Zugang zur Adminschnittstelle bei dezentralen Produkten**

Der Hersteller von dezentralen Produkten MUSS der gematik Zugang zur
administrativen Schnittstelle für Referenzobjekte bereitstellen. Der
Hersteller MUSS ein Benutzerhandbuch für diese Produkte bereitstellen.
**[\<=]**

### 3.2.10.2 Weiterentwicklung der Testumgebung

**TIP1-A_3363 - Nutzung von Produkt-Schnittstellen in der TU**

Die TBI MUSS der testdurchführenden Instanz ermöglichen, alle
Außenschnittstellen eines in die Testumgebung integrierten Produkts zu nutzen.
**[\<=]**

**TIP1-A_3364 - Produktspezifische Parameter in der TU**

Der TIZP MUSS vor Testbeginn produktspezifische Anbindungsparameter für die
Integration des jeweiligen Produkts in die Testumgebung definieren. **[\<=]**

**TIP1-A_3365 - Publikation Produktspezifische Parameter in der TU**

Der TIZP MUSS vor Testbeginn die definierten produktspezifischen Parameter für
die Integration des jeweiligen Produkts in die Testumgebung den Herstellern und
Anbietern übermitteln. **[\<=]**

### 3.2.10.3 Dimensionierung der Testumgebung

**TIP1-A_2790 - Leistungstest**

Die TBI MUSS sicherstellen, dass im Rahmen von Leistungstests temporär die
Testumgebung stufenweise skaliert werden kann, um das Verhalten des Systems bei
Laststeigerungen und Systemausbau zu überprüfen. **[\<=]**

**TIP1-A_4192 - Dimensionierung TU für PU-Fehlernachstellung**

Die TBI MUSS sicherstellen, dass die Testumgebung ausreichend dimensioniert ist,
um eine Fehlernachstellung für die Produktivumgebung zu ermöglichen. **[\<=]**

**TIP1-A_2792 - Splitten der Testumgebung**

Der TIZP KANN in Abstimmung mit der TDI der gematik die Testumgebung splitten,
wenn:

 ---> UL

**[\<=]**

**TIP1-A_2795 - Parallele Tests**

Die TBI MUSS, auf Anfrage der TDI der gematik, zwecks paralleler Durchführung
von Tests bei unterschiedlichen Versionsständen die Testumgebung in mehreren
Instanzen ausprägen, sofern die Produkte die Ausprägung mehrerer Instanzen in
unterschiedlichen Versionen unterstützen. **[\<=]**

**TIP1-A_2797 - Örtliche Verteilung von Testobjekten und Testtreibern**

Der TIZP MUSS die Möglichkeit der Verteilung von Testobjekten und Testtreibern
über Standortgrenzen hinweg schaffen. **[\<=]**

**TIP1-A_2800 - Nachweis der Anforderungserfüllung**

Der TIZP MUSS, auf Anfrage der TDI der gematik, die Testumgebung so gestalten,
dass in einer verteilten und produktivnahen Umgebung der Nachweis der
Erfüllung von funktionalen und nicht-funktionalen sowie der
Sicherheitsanforderungen an einzelne Produkte erbracht werden kann. **[\<=]**

**TIP1-A_2802 - Integration und produktübergreifende Tests**

Der TIZP MUSS die Integration von Produkten und produktübergreifende Tests in
mehreren Ausbaustufen, angefangen von der Integration der TI-Plattform bis zur
vollständigen Abbildung der Funktionalität der Produktivumgebung,
ermöglichen. **[\<=]**

**TIP1-A_2805 - Zeitnahe Anpassung von Produktkonfigurationen**

Der Hersteller oder Anbieter von Produkten MUSS sicherstellen, dass in der
Testumgebung die Produkte (außer Smartcards) sich in ihren Konfigurationen
zeitnah (möglichst kleiner 1 Arbeitstag) anpassen lassen. **[\<=]**

**TIP1-A_2806 - Zeitnahe Anpassung der Konfiguration der Testumgebung**

Die TBI MUSS sicherstellen, dass die Testumgebung sich in ihren Konfigurationen
zeitnah anpassen lässt. **[\<=]**

**TIP1-A_2807 - Zentrale Steuerung paralleler Tests**

Der TIZP MUSS in Zusammenarbeit mit der testdurchführenden Instanz TDI in der
Testumgebung parallele Testaktivitäten ermöglichen. **[\<=]**

**TIP1-A_2808 - Produkttests**

Der TIZP MUSS in der Testumgebung die Unterstützung von Produkttests
ermöglichen. **[\<=]**

**TIP1-A_2810 - Produktübergreifende Tests**

Der TIZP MUSS in der Testumgebung die Unterstützung von produktübergreifenden
Tests (schrittweise Integration aller Produkte) ermöglichen. **[\<=]**

### 3.2.10.4 Betrieb der Testumgebung

### 3.2.10.5 Nachstellen von PU-Fehlern in TU

**TIP1-A_2803-01 - Nachstellen von PU-Fehlern in der TU**

Die Testbetriebsinstanz (TBI) der Testumgebung MUSS das Nachstellen von Fehlern,
die in der Produktivumgebung auftreten, in der Testumgebung ermöglichen.
**[\<=]**

### 4 Szenarien

### 4.1 Einleitung

In diesem Kapitel werden zunächst die verschiedenen Szenarien identifiziert
unter denen Testmaßnahmen durchgeführt werden müssen. Anschließend werden
für jedes Szenario die Rahmenbedingungen und konkrete Anwendung der in Kapitel
2 beschriebenen allgemeinen Testvorgehensweise beschrieben.

Die Unterscheidung nach zentralen und dezentralen Produkten sowie
Fachanwendungen erfolgt gemäß Kapitel 3.1.

### 4.2 Testvorgehensweise im Rahmen der Zulassung eines neuen Produkts

<table><tr><th>
Szenario

</th><th>
Zulassung eines neuen Produkts

</th></tr><tr><td>
Beschreibung

</td><td>
Ein Hersteller oder Anbieter möchte ein Produkt erstmalig zulassen.

</td></tr><tr><td>
Testziele

</td><td>
 ---> UL

</td></tr><tr><td>
Testobjekt(e)

</td><td>
Das zuzulassende Produkt

</td></tr><tr><td>
Testbasis

</td><td>
 ---> UL

</td></tr><tr><td>
Besetzung der Rollen

</td><td>
 ---> UL

</td></tr><tr><td>
Systemumgebung

</td><td>
 ---> UL

</td></tr><tr><td>
Testphasen und Teststufen

</td><td>
 ---> UL

</td></tr><tr><td>
Zusätzliche Eingangskriterien EvT

</td><td>
keine

</td></tr><tr><td>
Zusätzliche Ausgangskriterien EvT

</td><td>
 ---> UL

</td></tr><tr><td>
Zusätzliche Eingangskriterien ZulT

</td><td>
keine

</td></tr><tr><td>
Zusätzliche Ausgangskriterien ZulT

</td><td>
keine

</td></tr></table>

**TIP1-A_6532 - Zulassung eines neuen Produkts: Aufgaben der TDI**

Die jeweilige TDI MUSS für die Zulassung eines neuen Produkts ihre
Testvorgehensweise gemäß Tabelle Tab_Test_021 Szenario: Zulassung eines neuen
Produkts umsetzen. **[\<=]**

**TIP1-A_6533 - Zulassung eines neuen Produkts: Aufgaben der Hersteller und
Anbieter**

Die Hersteller und Anbieter von Produkten MÜSSEN für die Zulassung eines neuen
Produkts ihre Testvorgehensweise gemäß Tabelle Tab_Test_021 Szenario:
Zulassung eines neuen Produkts umsetzen. **[\<=]**

### 4.3 Testvorgehensweise im Rahmen der Zulassung eines geänderten Produkts

<table><tr><th>
Szenario

</th><th>
Zulassung eines geänderten Produkts

</th></tr><tr><td>
Beschreibung

</td><td>
Ein Hersteller oder Anbieter möchte ein Produkt ändern und erneut zulassen.

</td></tr><tr><td>
Testziele

</td><td>
 ---> UL

</td></tr><tr><td>
Testobjekt(e)

</td><td>
Das zuzulassende Produkt

</td></tr><tr><td>
Testbasis

</td><td>
 ---> UL

</td></tr><tr><td>
Besetzung der Rollen

</td><td>
 ---> UL

</td></tr><tr><td>
Systemumgebung

</td><td>
 ---> UL

</td></tr><tr><td>
Testphasen und Teststufen

</td><td>
 ---> UL

</td></tr><tr><td>
Zusätzliche Eingangskriterien EvT

</td><td>
keine

</td></tr><tr><td>
Zusätzliche Ausgangskriterien EvT

</td><td>
 ---> UL

</td></tr><tr><td>
Zusätzliche Eingangskriterien ZulT

</td><td>
keine

</td></tr><tr><td>
Zusätzliche Ausgangskriterien ZulT

</td><td>
keine

</td></tr></table>

**TIP1-A_6536 - Zulassung eines geänderten Produkts: Aufgaben der TDI**

Die jeweilige TDI MUSS für die Zulassung eines geänderten Produkts ihre
Testvorgehensweise gemäß Tabelle Tab_Test_022 Szenario: Zulassung eines
geänderten Produkts umsetzen. **[\<=]**

**TIP1-A_6537 - Zulassung eines geänderten Produkts: Aufgaben der Hersteller
und Anbieter**

Die Hersteller und Anbieter von Produkten MÜSSEN für die Zulassung eines
geänderten Produkts ihre Testvorgehensweise gemäß Tabelle Tab_Test_022
Szenario: Zulassung eines geänderten Produkts umsetzen. **[\<=]**

### 4.4 Regressionstest

Ein Regressionstest stellt fest, ob durch eine durchgeführte Modifikation neue
Fehler erzeugt oder (bisher maskierte) Fehler freigelegt wurden und ob bisher
positiv durchgeführte Tests weiterhin positiv durchgeführt werden können.
Eine Modifikation kann die Installation einer neuen Fachanwendungsversion nach
einer Fehlerbehebung, eine Aktualisierung von Produkten (z. B.
Datenbank-Updates) sein oder auch Änderungen in den Testtools (Veränderungen
an Testtreibern oder Simulatoren) bewirken.

Die für den Regressionstest verwendeten Testfälle sind eine Teilmenge der für
das jeweilige Testobjekt geplanten (funktionalen) Testfälle und sollen
weitgehend automatisiert durchgeführt werden. Dabei liegt der Schwerpunkt
nicht nur auf der funktionalen Verifikation, sondern auch auf der
Sicherstellung der richtigen Installation und Konfiguration einer Fachanwendung
in der Systemumgebung. Der Regressionstest beinhaltet damit die anderen
Testarten Funktionstest, Interoperabilitätstest und Leistungstest.

Nicht geänderte Produkttypen werden geprüft, wenn sie an einem Anwendungsfall
beteiligt sind, an dem mindestens ein neuer oder geänderter Produkttyp
beteiligt ist. Der Umfang eines Regressionstests richtet sich dabei nach Art,
Umfang und Kritikalität der Änderungen. Der Regressionstest muss nicht
notwendigerweise alle bereits vorhandenen Testfälle beinhalten, er muss aber
mindestens sicherstellen, dass Änderungen keine unerwünschten Auswirkungen
auf nicht geänderte Komponenten haben. Dafür ist es notwendig, dass die
jeweils verantwortliche testdurchführende Instanz eine entsprechende
Auswirkungsanalyse als Grundlage der Regressionstests durchführt.

### 4.5 Teststufen

Die Teststufen laufen sequentiell ab. Eine Teststufe beginnt erst, wenn die
vorherige Teststufe erfolgreich abgeschlossen ist. Dieses Vorgehen erfolgt
sowohl bei den Eigenverantwortlichen Tests (EvT) wie auch bei den
Zulassungstests (ZulT).

### 4.5.1 Produkttest (EvT)

<table><tr><th>
Teststufe

</th><th>
Produkttest (EvT)

</th></tr><tr><td>
Beschreibung

</td><td>
Im Rahmen des Produkttests (EvT) werden Produkte einzeln getestet.

</td></tr><tr><td>
Ziel

</td><td>
Nachweis der Erfüllung der funktionalen und nicht-funktionalen Anforderungen.

</td></tr><tr><td>
Testarten

</td><td>
Funktionstest

Leistungstest

</td></tr></table>

### 4.5.2 Produktübergreifender Test (EvT)

<table><tr><th>
Teststufe

</th><th>
Produktübergreifender Test (EvT)

</th></tr><tr><td>
Beschreibung

</td><td>
Im Rahmen des Produktübergreifenden Tests (EvT) werden Produkte im
Zusammenspiel getestet.

</td></tr><tr><td>
Ziel

</td><td>
Nachweis, dass Implementierungen von Produkten verschiedenen Typs zueinander
interoperabel sind.

Nachweis der Erfüllung der Anwendungsfälle.

</td></tr><tr><td>
Testarten

</td><td>
Interoperabilitätstest

</td></tr></table>

### 4.5.3 Eingangsprüfung (ZulT)

<table><tr><th>
Teststufe

</th><th>
Eingangsprüfung (ZulT)

</th></tr><tr><td>
Beschreibung

</td><td>
Die Eingangsprüfung prüft exemplarisch, ob das Testobjekt zur Entlastung der
Zulassungstests geeignet ist.

Erkennbar ungeeignete Produkte werden zurück an die Hersteller bzw. Anbieter
verwiesen.

</td></tr><tr><td>
Ziel

</td><td>
Nachweis (durch exemplarische Prüfung), dass das Testobjekt geeignet ist, die
Zulassungstests erfolgreich zu durchlaufen.

</td></tr><tr><td>
Testarten

</td><td>
Güteprüfung

Funktionstest

</td></tr></table>

### 4.5.4 Produkttest (ZulT)

<table><tr><th>
Teststufe

</th><th>
Produkttest (ZulT)

</th></tr><tr><td>
Beschreibung

</td><td>
Der Produkttest prüft auf der Grundlage von Vorgaben durch die
testkoordinierende Instanz, ob das Produkt, als konkrete Ausprägung eines
Produkttyps, die geforderten Funktionen und Schnittstellen
spezifikationskonform realisiert hat und ob es die Leistungsanforderungen
erfüllt. Im Gegensatz zum EvT, werden die interne Struktur und das interne
Verhalten eines Produkts nicht berücksichtigt. Es wird lediglich das Verhalten
der Produkte an ihren Außenschnittstellen geprüft.

</td></tr><tr><td>
Ziel

</td><td>
Nachweis der Erfüllung aller an das Produkt gestellten Anforderungen der
Prüfart Produkttest gemäß Produkttypsteckbrief.

Nachweis, dass die an die Produkte gestellten Anforderungen hinsichtlich
[ISO25000 oder vergleichbarer Norm] Funktion, Interoperabilität, Benutzbarkeit
und Sicherheit.

</td></tr><tr><td>
Testarten

</td><td>
Funktionstest

Leistungstest

</td></tr></table>

### 4.5.5 Produktübergreifender Test (ZulT)

<table><tr><th>
Teststufe

</th><th>
Produktübergreifender Test (ZulT)

</th></tr><tr><td>
Beschreibung

</td><td>
Ergänzend zum Produkttest, der sich jeweils auf ein einzelnes Produkt bezieht,
müssen Produkte auch integriert getestet werden.

</td></tr><tr><td>
Ziel

</td><td>
Nachweis, (durch Integrationstests der einzelnen Produkte) des Zusammenwirkens
von Produkten und Fachanwendungen.

Nachweis dass die Ende-zu-Ende-Funktionalitäten der Produkte und
Fachanwendungen erfüllt werden und die fachlichen Abläufe der Anwendung in
die Geschäftsprozesse der Endanwender integriert werden können.

</td></tr><tr><td>
Testarten

</td><td>
Interoperabilitätstest

Leistungstest

</td></tr></table>

### 4.6 Interoperabilität

Um die korrekte funktionale Zusammenarbeit der Produkte untereinander
nachzuweisen, müssen im Rahmen der Interoperabilitätstests die
anwendungsfallbasierten Tests mit vielen verschiedenen Produktkombinationen
durchgeführt werden. Allerdings würde die Abdeckung aller möglichen
Produktkombinationen zu einer zeitlich und wirtschaftlich nicht vertretbaren
Menge von Tests führen. Somit muss die Interoperabilität mit einer
begrenzten, aber fachlich ausreichenden Mindestanzahl von Produkten der
beteiligten Produkttypen und anderer am Anwendungsfall beteiligter Komponenten
nachgewiesen werden. Nachfolgende Tabelle zeigt für die zuzulassenden oder
freizugebenden Produkte die Mindestanzahl der Interoperabilitätspartner. Zum
Beispiel müssen für den Konnektor (VSDM) die VSDM-Anwendungsfälle mit
mindestens drei verschiedenen eHealth-Kartenterminals und drei Fachdiensten
nachgewiesen werden. Es muss dabei aber nicht jedes Kartenterminal mit jedem
Fachdienst kombiniert werden.

**TIP1-A_7333 - Parallelbetrieb von Release oder Produkttypversion**

In der Übergangsphase von Dokumentenreleases in welcher mehrere
Produkttypversionen parallel Gültigkeit haben SOLL die testdurchführende
Instanz die Interoperabilitätstests immer gegen die aktuell höchste
verfügbare Produktversionsnummer des bzw. der jeweiligen Hersteller
durchführen (je nach Anzahl in Tabelle 13: Tab_Test_033 Mindestumfang der
Interoperabilitätsprüfung). Für alle weiteren, zum Zeitpunkt der
Inbetriebnahme in der PU vorhandenen, Produktversionsnummern SOLLEN, in
Abstimmung mit dem Test- und Transitionmanager der gematik, angemessene
Regressionstests im Rahmen der Interoperabilitätstests durchgeführt
werden.Eventuell zu beachtende Integrations- bzw. Testreihenfolgen gehen aus
der von der gematik veröffentlichten Migrationsstrategie des jeweiligen
Releases hervor. **[\<=]**

**TIP1-A_7334 - Risikoabschätzung bezüglich der Interoperabilität**

Die testdurchführende Instanz MUSS eine Risikoabschätzung für eventuelle
Interoperabilitätsprobleme mit Komponenten, welche in einer neuen
Produkttypversion noch nicht oder gemäß Tab_Test_033 Mindestumfang der
Interoperabilitätsprüfung nicht in ausreichender Anzahl verfügbar sind, auf
Grundlage der Migrationsstrategie durchführen und der gematik vorlegen.
**[\<=]**

**TIP1-A_6772 - Partnerprodukte bei Interoperabilitätstests**

Der Zulassungsnehmer MUSS die Interoperabilitätstests gegen Referenzobjekte
durchführen. Sind Referenzobjekte nicht verfügbar, ist in Abstimmung mit der
gematik die Nutzung von geeigneten Testobjekten möglich. **[\<=]**

Die Nutzung von geeigneten Testobjekten kann notwendig sein, wenn zeitgleich
Änderungen an mehreren Produkten der TI vorliegen. Grundvoraussetzung für ein
geeignetes Testobjekt ist, dass zumindest die korrekte Umsetzung der für den
jeweiligen Interoperabilitätstest benötigten Funktionalität(en) im Rahmen
von Produkttests erfolgreich nachgewiesen wurde.

**TIP1-A_6529 - Produkttypen: Mindestumfang der Interoperabilitätsprüfung**

Die testdurchführende Instanz (TDI) MUSS zum Nachweis der Interoperabilität
alle für das jeweilige Produkt relevanten anwendungsfallbasierten Tests mit
der Mindestanzahl von Produkten gemäß Tabelle 13: Tab_Test_033 Mindestumfang
der Interoperabilitätsprüfung durchführen. **[\<=]**

Die Angabe der Mindestanzahl geht davon aus, dass ausreichend viele
Referenzobjekte bzw. geeignete Testobjekte vorhanden sind. Sollte die
geforderte Anzahl nicht zur Verfügung stehen, kann in Abstimmung mit dem TTM
gegen eine verringerte Zahl getestet werden.

![Img-006][Img-006]

### 4.7 Testdokumentation

Zur Dokumentation der Testaktivitäten der verschiedenen Testphasen und
Teststufen sollen durch die Hersteller oder Anbieter bzw. die
testdurchführende Instanz unterschiedliche Dokumente erstellt werden.

Die Testdokumentation eines Herstellers oder Anbieters soll dabei einheitlich
strukturiert sein und alle relevanten Informationen konsolidieren (z.B. von
Subunternehmen).

Der genaue Lieferzeitpunkt der Dokumente ist jeweils als Eingangs- bzw.
Testausgangskriterium definiert.

**TIP1-A_7335 - Bereitstellung der Testdokumentation**

Der Zulassungsnehmer MUSS die geforderte Testdokumentation auf geeignete Weise
in Abstimmung mit dem Test- & Transitionmanager der gematik zur Verfügung
stellen. **[\<=]**

**TIP1-A_6524-01 - Testdokumentation gemäß Vorlagen**

Der Zulassungsnehmer MUSS sich bei der Erstellung der Testdokumentation an die
Tabellen Tab_Test_013 Testkonzept, Tab_Test_014 Testspezifikation, Tab_Test_015
Release Notes, Tab_Test_016 Produktdokumentation, Tab_Test_017 Testprotokoll
und Tab_Test_018 Testbericht halten. **[\<=]**

**A_20065 - Nutzung der Dokumententemplates der gematik**

Die Testdokumentation SOLL gemäß der Templates, die im Rahmen des
Zulassungsverfahrens von der gematik zur Verfügung gestellt werden, erstellt
werden.Abweichungen sind mit dem jeweiligen Testmanager der gematik
abzustimmen. **[\<=]**

Hersteller können die Templates der Testdokumentation aus dem letzten
Zulassungsverfahren weiterverwenden.

### 4.7.1 Testkonzept

<table><tr><th>
Testdokument

</th><th>
Testkonzept

</th></tr><tr><td>
Beschreibung

</td><td>
Das Testkonzept beschreibt die Vorgehensweise hinsichtlich der Testaktivitäten
für einen Produkttyp sowie das konkrete Vorgehen entsprechend der jeweiligen
Integrationsstufe bezogen auf die TI. Es operationalisiert die Vorgaben aus
diesem Testkonzept.

Testvorgehen und Dokumente halten sich an Standards des ISTQB.

Die testdurchführende Instanz erstellt pro Testphase je ein Testkonzept pro
Produkttyp, wobei die Testkonzepte einheitlich strukturiert sein sollen und
alle relevanten Informationen konsolidieren (z.B. von Subunternehmen).

Das Testkonzept soll auf der Inhaltsstruktur des „Master Test Plan“ bzw.
„Level Test Plan“ nach ISO/IEC/IEEE 29119 basieren.

Das Testkonzept muss für sämtliche Produkttypen einheitlich gestaltet werden.
Das Dokument wird entsprechend der Erfordernisse im Projekt fortgeschrieben.

Das Testkonzept muss darstellen, wie die Testfälle den Nachweis über die
Anforderungen oder Anwendungsfälle führen bzw. welche Anforderungen oder
Anwendungsfälle mit welchen Testfällen in einem Testbericht nachgewiesen
werden. Für das Testkonzept stellt die gematik eine Vorlage zur Verfügung.

</td></tr><tr><td>
Geforderte Inhalte

</td><td>
 ---> UL

</td></tr><tr><td>
Gültigkeitsbereich

</td><td>
Produkt

</td></tr><tr><td>
Lieferzeitpunkt

</td><td>
Vor Beginn der Eigenverantwortlichen Tests bzw. Zulassungstests
(Eingangskriterium der jeweiligen Testphasen)

</td></tr><tr><td>
Verantwortlich

</td><td>
Testdurchführende Instanz der RU bzw. TU

</td></tr><tr><td>
Vorlage

</td><td>
Siehe Anhang B – Testkonzept

</td></tr></table>

### 4.7.2 Testspezifikation

<table><tr><th>
Testdokument

</th><th>
Testspezifikation

</th></tr><tr><td>
Beschreibung

</td><td>
Die Testspezifikation dokumentiert auf logischer Ebene die Ergebnisse des
Testentwurfs sowie auf konkreter Ebene die einzelnen Testfälle und deren
Konfigurationen sowie den geplanten Ablauf der Testdurchführung.

Die Testspezifikation soll auf der Inhaltsstruktur des „Level Test Design“,
„Level Test Case“ sowie „Level Test Procedure“ der ISO/IEC/IEEE 29119
basieren und umfasst die folgenden Teildokumente:

 ---> UL

Bei der Erstellung der Testfälle sind gegebenenfalls vorhandene
Implementierungsleitfäden für Clientsysteme (z.B. PVS, KIS, AVS) zu beachten.

Bei der Verwendung von Testskripten im Rahmen einer Testautomatisierung müssen
die Skripte selbst entsprechend getestet werden.

</td></tr><tr><td>
Geforderte Inhalte

</td><td>
Testentwurfsspezifikation:

 ---> UL

Testfallspezifikation:

 ---> UL

Testablaufspezifikation:

 ---> UL

Spezifikation der Standardkonfigurationen:

 ---> UL

</td></tr><tr><td>
Gültigkeitsbereich

</td><td>
Teststufe eines Produkts

</td></tr><tr><td>
Lieferzeitpunkt

</td><td>
Vor Beginn der Eigenverantwortlichen Tests bzw. Zulassungstests
(Eingangskriterium der jeweiligen Testphasen)

</td></tr><tr><td>
Verantwortlich

</td><td>
Testdurchführende Instanz der RU bzw. TU

</td></tr><tr><td>
Vorlage

</td><td>
Siehe Anhang B – Testspezifikation

</td></tr></table>

### 4.7.3 Release Notes

<table><tr><th>
Testdokument

</th><th>
Release Notes

</th></tr><tr><td>
Beschreibung

</td><td>
Release Notes dokumentieren beim Release eines Produkts die Änderungen des
Produkts gegenüber dem vorherigen Release.

</td></tr><tr><td>
Geforderte Inhalte

</td><td>
 ---> UL

</td></tr><tr><td>
Gültigkeitsbereich

</td><td>
Release

</td></tr><tr><td>
Lieferzeitpunkt

</td><td>
Vor Beginn Zulassungstests (Eingangskriterium)

</td></tr><tr><td>
Verantwortlich

</td><td>
Hersteller und Anbieter

</td></tr></table>

### 4.7.4 Produktdokumentation

<table><tr><th>
Testdokument

</th><th>
Produktdokumentation

</th></tr><tr><td>
Beschreibung

</td><td>
Das Dokument wird entsprechend der Erfordernisse durch den Hersteller oder
Anbieter fortgeschrieben.

</td></tr><tr><td>
Geforderte Inhalte

</td><td>
 ---> UL

</td></tr><tr><td>
Gültigkeitsbereich

</td><td>
Produkt

</td></tr><tr><td>
Lieferzeitpunkt

</td><td>
Vor Beginn Zulassungstests (Eingangskriterium)

</td></tr><tr><td>
Verantwortlich

</td><td>
Hersteller und Anbieter

</td></tr></table>

### 4.7.5 Testprotokoll

<table><tr><th>
Testdokument

</th><th>
Testprotokoll

</th></tr><tr><td>
Beschreibung

</td><td>
Das Testprotokoll muss die detaillierten Ergebnisse der Testdurchführung je
Produktversion enthalten.

Das Testprotokoll soll auf der Inhaltsstruktur des „Level Test Log“ bzw.
„Anomaly Report“ nach ISO/IEC/IEEE 29119 basieren.

Das Dokument wird entsprechend der Erfordernisse im Projekt durch den Hersteller
oder Anbieter fortgeschrieben.

</td></tr><tr><td>
Geforderte Inhalte

</td><td>
 ---> UL

</td></tr><tr><td>
Gültigkeitsbereich

</td><td>
Teststufe bzw. Testphase eines Produkts

</td></tr><tr><td>
Lieferzeitpunkt

</td><td>
Mit Abschluss der Eigenverantwortlichen Tests bzw. Zulassungstests (Aus- bzw.
Eingangskriterium der jeweiligen Testphasen)

</td></tr><tr><td>
Verantwortlich

</td><td>
Testdurchführende Instanz der RU bzw. TU

</td></tr><tr><td>
Vorlage

</td><td>
Siehe Anhang B - Testprotokoll

</td></tr></table>

### 4.7.6 Testbericht

<table><tr><th>
Testdokument

</th><th>
Testbericht

</th></tr><tr><td>
Beschreibung

</td><td>
Der Testbericht muss je Produktversion mindestens die Angaben entsprechend den
Vorgaben des Testkonzepts enthalten und der abgestimmten Vorlage entsprechen.

Darüber hinaus muss der Testbericht einen zusammenfassenden Problemreport und
eine abschließende Risikobetrachtung und Einschätzung der testdurchführenden
Instanz enthalten.

Testberichte werden zum Abschluss einer Teststufe von der testdurchführenden
Instanz verfasst und dienen dazu, den Testumfang und das Ergebnis
nachvollziehbar zu dokumentieren. In den Testphasen sind die Testberichte das
wesentliche Mittel, um vor dem Start einer Teststufe den Reifegrad des
Testobjekts oder einer Anwendung einzuschätzen und ggf. die
Testvoraussetzungen als nicht erfüllt zu beurteilen. Damit ein Testbericht
diesen Zweck erfüllt, müssen das Testobjekt, der Testaufbau, die durch Tests
abgedeckten Anforderungen, gefundene und behobene sowie nicht behobene Fehler
beschrieben sein.

Das Testbericht soll auf der Inhaltsstruktur des „Level Test Report“ bzw.
„Master Test Report“ nach ISO/IEC/IEEE 29119 basieren. Für den Testbericht
stellt die gematik eine Vorlage zur Verfügung.

Anhand des Testberichts kann die gematik in der Eingangsprüfung die Aufnahme
einer Teststufe oder die Zulassung eines Produkts begründet ablehnen.
Mögliche Gründe für die Ablehnung eines Testberichtes sind:

Die Anforderungen sind unzureichend abgedeckt, so dass wichtige Funktionen des
Produkttyps nicht qualitätsgesichert sind und anzunehmen ist, dass folgende
Teststufen nicht erfolgreich absolviert werden können.

Die nicht behobenen Fehler sind so schwerwiegend, dass die Teststufen der
Zulassungstestphase nicht in der vorgesehen Zeit durchlaufen werden können.

Der Testaufbau und die eingesetzten Testmittel sind offensichtlich ungeeignet,
um die abzudeckenden Anforderungen zu prüfen.

</td></tr><tr><td>
Geforderte Inhalte

</td><td>
Testobjekt

: Die Beschreibung des Testobjekts umfasst in tabellarischer Form den
Produkttyp, die Herstellerversion des Produkts und die Version der
gematik-Spezifikation. Zudem soll das Produkt in kurzer Form z. B. als
Komponentendiagramm mit Erläuterungen, beschrieben werden.

Testaufbau

: Die Dokumentation des Testaufbaus umfasst die Beschreibung der
Testinfrastruktur, Testtreiber, Platzhalter und Simulatoren, die zur
Durchführung der Tests eingesetzt werden.

Testumfang

: Der Testbericht enthält folgende Angaben in tabellarischer Form:

 ---> UL

Für nicht durch Testfälle abgedeckte Anforderungen ist zu begründen, warum
sie nicht abgedeckt sind. Begründungen sind nur bei SOLL- oder
KANN-Anforderungen möglich.

Probleme

: Die nicht behobenen Probleme sind tabellarisch darzustellen und zu
dokumentieren, ob und wann Probleme behoben werden. Der Ersteller des
Testberichts muss analysieren, welche Einschränkungen nicht behobene Probleme
verursachen. Nicht behobene Probleme sind akzeptabel, wenn sie nicht sehr
schwer bzw. schwer sind und keine Verzögerung oder Mehraufwand in folgenden
Teststufen verursachen.

Risiken

: Dokumentation von nicht erfüllten Eingangs- oder Ausgangskriterien sowie eine
Bewertung der damit verbundenen Risiken.

</td></tr><tr><td>
Gültigkeitsbereich

</td><td>
Teststufe bzw. Testphase eines Produkts

</td></tr><tr><td>
Lieferzeitpunkt

</td><td>
Mit Abschluss der Eigenverantwortlichen Tests bzw. Zulassungstests (Aus- bzw.
Eingangskriterium der jeweiligen Testphasen)

</td></tr><tr><td>
Verantwortlich

</td><td>
Testdurchführende Instanz der RU bzw. TU

</td></tr></table>

### 4.8 Serviceprodukte der gematik zur Testunterstützung

Die gematik bietet Zulassungsnehmern eine Reihe von Serviceprodukten an, die
für die Entwicklung der Produkte bzw. für die eigenverantwortlichen Tests
genutzt werden können. Welche Services dies sind, deren Verfügbarkeit und die
Konditionen zu welchen diese genutzt werden können, sind im gematik Fachportal
aufgeführt.

### 5 Fachanwendung VSDM

### 5.1 Testkarten

Verschiedene Anwendungen, die durch die Telematikinfrastruktur (TI) unterstützt
werden, verwenden verschiedene Typen von Smartcards. Zur Unterstützung der
Entwicklung von Anwendungen der TI, von Produkten der TI, aber auch in den
Zulassungstests werden Testkarten verwendet. Sie weisen eine spezifische
Personalisierung auf. Auf den Testkarten personalisierte Zertifikate sind
u. a. von einem testspezifischen Vertrauensraum abgeleitet und sind daher
grundsätzlich nicht in der produktiven TI einsetzbar. Da Anwendungen häufig
das Zusammenspiel verschiedener Smartcards erfordern, wurden Sets verschiedener
Testkarten definiert. Die Testkarten-Sets können von der gematik bezogen
werden. Der Einsatz physischer Testkarten zu Testzwecken schränkt die
Möglichkeiten einer Testautomatisierung ein. Zur Unterstützung der
Testautomatisierung können physische Testkarten durch eine Kartensimulation,
ggf. durch eine Kartenterminalsimulation ergänzt, ersetzt werden. Die
Kartensimulation, mit den respektiven Kartensimulationsimages, kann durch
entsprechende Konfiguration die Funktionsweise aller G2-Testkarten (eGK, HBA
und SMCs) nachbilden. Für die Fachdienste VSDM wird ein Zusammenspiel von
verschiedenen Testkartenarten benötigt (eGK, HBA und SMC-B).

### 5.1.1 Testkartenausprägungen

Für verschiedene Testmaßnahmen werden unterschiedliche Ausprägungen von
Testkarten eingesetzt.

 ---> UL

Neben den Ausprägungen weisen Testkarten auch verschiedene Personalisierungen
auf, die auch mit spezifischen COS-Ausprägungen einhergehen.

 ---> UL

### 5.1.2 Testkarten Verwendung

Physische Testkarten werden von verschiedenen Serviceprodukten verwendet, um die
Entwicklung von Produkten und Anwendungen für die TI zu unterstützen, können
aber auch in Form spezifischer Testkarten Sets Entwicklungstätigkeiten bezogen
werden. Physische Testkarten werden auch im Rahmen von Zulassungstests für
Produkttests der Fachdienste VSDM, für produktübergreifende und Ende-zu-Ende
Tests eingesetzt. Die Testkarten müssen den Anforderungen der
Testkartenspezifikation [gemSpec_TK] genügen.

Im Rahmen von Zulassungstests werden in Produkt- und produktübergreifenden
Tests der Fachdienste VSDM auch virtuelle Testkarten eGK eingesetzt zum
Einsatz, um u. a. Last- und Performancetests mit einer großen Anzahl
verschiedener Personalisierungsausprägungen der eGK über einen längeren
Zeitraum hinweg durchführen zu können.

Kartensimulations-Images werden für Zulassungstests unterschiedlicher Produkte
verwendet, um einen möglichst hohen Testautomatisierungsgrad zu erreichen bzw.
mit vereinfachten Testaufbauten arbeiten zu können.

Physische und virtuelle Testkarten wie auch Kartensimulations-Images verwenden
für Updates symmetrische und/oder asymmetrische Schlüssel. Ein Dokument zur
Schlüsselgenerierung [gemSpec_TK_SG] definiert Algorithmen zur Generierung der
verschiedenen Schlüssel und eröffnet damit Möglichkeiten einer Manipulation
von Personalisierungsinhalten der Testkarten ohne Verwendung eines spezifischen
Fachdienstes. Sofern Fachdienste für Updates von Testkartenpersonalisierungen
zur Verfügung stehen, müssen durch den Fachdienst täglich wechselnde Updates
der von ihm verwalteten Testkarten bereitgestellt werden. In physischen
Testkarten personalisierte X.509-Zertifikate müssen online vom Trust Service
Provider (TSP), der die Zertifikate erstellt hat, prüfbar sein.

### 5.1.3 Anforderungen an die Testkarten eGK

**VSDM-A_2812 - Bereitstellung Testkartensätze**

Betreiber und Anbieter von Fachdiensten VSDM MÜSSEN Testkarten für RU und TU
von den Krankenkassen bereitstellen, deren produktive eGK sie mit VSD-, CMS -
Updates versorgen. Bei Testkarten, MÜSSEN Update Inhalte (VSD, CMS) bekannt
gemacht werden. **[\<=]**

**VSDM-A_3029 - Bereitstellung von Testkarten**

Betreiber der Fachdienste VSDM MÜSSEN spezifikationskonform physische und
virtuelle Testkarten eGK und täglich wechselnde Updates bereitstellen, wie im
Kapitel Flip/Flop Verfahren formuliert. **[\<=]**

**VSDM-A_3030 - Bereitstellung von spezifikationsabweichende Testkarten**

Bewusst spezifikationsabweichende Testkarten eGK KÖNNEN (physisch oder
virtuell) von den Betreibern der Fachdiensten VSDM bereitgestellt werden.
**[\<=]**

**VSDM-A_2814 - Eindeutigkeit der Testkartenschlüssel**

Betreiber und Anbieter der Fachdienste VSDM MÜSSEN bei der Generierung
symmetrischer Schlüssel für die Testkarten, die definierten Vorgaben der
testdurchführenden Instanz der TU berücksichtigen. **[\<=]**

**VSDM-A_2815 - Berücksichtigung von Vorgaben zur Schlüsselerzeugung**

Betreiber und Anbieter der Fachdienste VSDM MÜSSEN bei der Generierung
symmetrischer Schlüssel für die Testkarten, die definierten Vorgaben der
testdurchführenden Instanz der TU berücksichtigen. **[\<=]**

### 5.2 Flip/Flop-Verfahren

Um die Kommunikation zwischen testdurchführender Instanz und dem Betreiber des
Fachdienstes VSDM zu minimieren, hat sich das sogenannte Flip/Flop-Verfahren
bewährt. Der Fachdienst UFS bietet täglich ein Update für verschiedene
Testkarten an.

Um in Testverfahren das erfolgreiche Update der VSD auf der eGK nachweisen zu
können, werden unterschiedliche Ausprägungen der VSD verwendet.

An geraden Tagen realisiert der Fachdienst VSDD ein Update mit VSD der Variante
1 und an ungeraden Tagen ein Update mit VSD der Variante 2. Nach erfolgreichem
Abschluss des jeweiligen Updates der VSD auf der eGK löscht der UFS die
Update-Information.

Die Funktionalität des Fachdienstes CMS wird durch Sperren und Entsperren der
Gesundheitsanwendung (DF.HCA) überprüft.

Im Kontext der Implementierung und Umsetzung des Flip/Flop-Verfahrens ergeben
sich die nachfolgend aufgeführten Anforderungen.

**VSDM-A_2825 - Bereitstellen von VSD-Updates**

Betreiber der Fachdienste VSDM MÜSSEN für die Testkarten der diese Dienste
beauftragenden Krankenkassen täglich ein VSD-Update zu Testzwecken
bereitstellen. **[\<=]**

**VSDM-A_2826 - Bereitstellen datumsbasierter VSD-Updates**

Betreiber der Fachdienste VSDM MÜSSEN für die Testkarten zu Testzwecken für
gerade und ungerade Tage zwei unterschiedliche VSD-Updates bereitstellen.
**[\<=]**

**VSDM-A_2827 - Prüfen der eGK-Sperrung**

Anbieter der Fachdienste VSDM MÜSSEN für die Testkarten zu Testzwecken an
geraden Kalendertagen (z.B. der 16. Tag des Monats) ein CMS-Update mit dem Ziel
bereitstellen, die Gesundheitsanwendung auf der eGK zu sperren. **[\<=]**

**VSDM-A_2828 - Prüfen der eGK-Entsperrung**

Anbieter der Fachdienste VSDM MÜSSEN für die Testkarten zu Testzwecken an
ungeraden Kalendertagen (z.B. der 17. Tag des Monats) ein CMS-Update mit dem
Ziel bereitstellen, die Gesundheitsanwendung auf der eGK zu entsperren.
**[\<=]**

### 5.3 Umgang mit mandantenfähigen Fachdiensten

Betreiber der Fachdienste VSDM können auch mehrere Anbieter von eGK
unterstützen. Da die Eigenschaften der eGK auch die Zugangswege durch die
Telematikinfrastruktur zum Fachdienst beeinflussen, muss jeder Anbieter von
Fachdiensten Testkarten bereitstellen und durch den Betreiber seiner
Fachdienste verwalten lassen.

Betreiber mandantenfähiger Fachdienste müssen mindestens zwei Testkartensätze
(siehe Kapitel 5.1) unterschiedlicher Anbieter (Mandanten) verwalten und für
Testmaßnahmen das Flip/Flop-Verfahren aktivieren.

Im Produkttest bleiben Tests zur Mandantenfähigkeit auf 2 Mandanten
beschränkt. Allerdings müssen im produktübergreifenden Test für jeden
Mandanten eines Fachdienstes mindestens 2 Testkarten verwaltet und das
Flip/Flop-Verfahren für Testmaßnahmen aktiv sein.

Grundsätzlich soll jeder Anbieter von Fachdiensten mindestens einen
Testkartensatz für Testmaßnahmen zur Verfügung stellen, um ggf. mehrere
testdurchführende Instanzen bei der Testdurchführung zu unterstützen.

**VSDM-A_2830 - Integration multipler Anbieter**

Der Fachdienstbetreiber des mandantenfähigen Fachdienstes MUSS mindestens zwei
Anbieter integrieren. **[\<=]**

**VSDM-A_2831 - Verwendung von Testkarten**

Der Fachdienstbetreiber des mandantenfähigen Fachdienstes MUSS sicherstellen,
dass während des produktübergreifenden Tests für jeden Mandanten eines
Fachdienstes mindestens 2 Testkarten verwaltet werden. **[\<=]**

**VSDM-A_2832 - Umsetzung des Flip/Flop-Verfahrens**

Der Fachdienstbetreiber des mandantenfähigen Fachdienstes MUSS sicherstellen,
dass das Flip/Flop-Verfahren für Testmaßnahmen für alle Mandanten aktiviert
wird. **[\<=]**

### 5.4 Testdurchführung der EvT bei VSDM

**A_18807 - Durchführung von gematik-Testfällen (EvT) beim Fachdienst VSDM**

Hersteller von Fachdiensten VSDM MÜSSEN im Rahmen ihrer eigenverantwortlichen
Tests, die von der gematik zur Verfügung gestellten Testfälle durchführen.
**[\<=]**

Das Testportal bietet eine zusätzliche Qualitätssicherung und entbindet den
Hersteller nicht vom Testen der korrekten Funktionalität nach
Anforderungslage. Für Anforderungen, für die es im Testportal Testfälle
gibt, werden allerdings keine gesonderten Nachweise verlangt.

### 6 Fachanwendung KOM-LE

**A_18892 - Durchführung von gematik-Testfällen (EvT) beim Fachdienst KOM-LE**

Hersteller von Fachdiensten KOM-LE MÜSSEN im Rahmen ihrer eigenverantwortlichen
Tests, die von der gematik zur Ausführung bereitgestellten Testfälle
durchführen. **[\<=]**

Das Testportal bietet eine zusätzliche Qualitätssicherung und entbindet den
Hersteller nicht vom Testen der korrekten Funktionalität nach
Anforderungslage. Für Anforderungen, für die es im Testportal Testfälle
gibt, werden allerdings keine gesonderten Nachweise verlangt.

### 7 Fachanwendung AdV

Für die Produkttests der AdV (Anwendungen der Versicherten) und für
produktübergreifende Tests werden Testkarten (physische eGK) eingesetzt. Die
Testkarten müssen den Anforderungen der eGK-Testkartenspezifikationen
[gemSpec_TK_FD, gemSpec_TK] genügen, von den Fachdiensten der Anwendung VSDM
mit Updates versorgt werden können und auf der Testkarte personalisierte
X.509-Zertifikate müssen online gegen einen Trust Service Provider (TSP)
prüfbar sein.

**TIP1-A_7338-01 - Anzahl der KTR-AdV als Referenzobjekte**

Hersteller einer KTR-AdV SOLLEN mindestens ein KTR-AdV Produkt in der TU
permanent als Referenzobjekt zur Verfügung stellen. Eine Abstimmung und die
Koordination finden über den Test & Transitionmanager der gematik statt.
Ausnahmen für die Verfügbarkeit von weniger als einem KTR-AdV als
Referenzobjekt SOLLEN mit dem Test & Transitionmanager der gematik abgestimmt
werden. **[\<=]**

**TIP1-A_7339-01 - Bereitstellung Testkartensätze für KTR-AdV**

Hersteller der KTR-AdV MÜSSEN der gematik personalisierte Testkartensätze eGK
nach [gemSpec_TK_FD] bereitstellen.  **[\<=]**

Es können die für die Fachdienste VSDM bereitgestellten Testkartensätze
genutzt werden.

**TIP1-A_7340-01 - Bereitstellung von Testkarten KTR-AdV**

Hersteller der KTR-AdV MÜSSEN spezifikationskonform physische und virtuelle
Testkarten eGK nach [gemSpec_TK_FD] bereitstellen. **[\<=]**

**TIP1-A_7342-01 - Eindeutigkeit der Testkarte pro Testkartenkategorie**

Hersteller der KTR-AdV SOLLEN sicherstellen, dass eGK Testkarten für KTR-AdV so
personalisiert sind, dass jeweils eine definierte Testkategorie berücksichtigt
wird. **[\<=]**

Die Afo wird benötigt, um beim Test des VSDM Anwendungsfalls mit virtuellen
Karten zu arbeiten.

**TIP1-A_7343-01 - Berücksichtigung von Vorgaben zur Schlüsselerzeugung eGK
Testkarten für KTR-AdV**

Hersteller der KTR-AdV SOLLEN sicherstellen, dass bei der Generierung
symmetrischer Schlüssel für die eGK Testkarten, die definierten Vorgaben nach
[gemSpec_TK_FD] der testdurchführenden Instanz der TU berücksichtigt werden.
**[\<=]**

**TIP1-A_7344-01 - Integration multipler Anbieter für KTR-AdV**

Hersteller eines mandantenfähigen Produktes KTR-AdV MÜSSEN mindestens 2
Krankenkassen integrieren. **[\<=]**

**TIP1-A_7345-01 - Bereitstellung SM-B für KTR-AdV**

Hersteller einer mandantenfähigen KTR-AdV MÜSSEN sicherstellen, dass während
des produktübergreifenden Tests für jeden Mandanten eine SM-B verwaltet wird.
**[\<=]**

### 8 Fachanwendung ePA

Für die Testbarkeit der Fachanwendung ePA ist es notwendig, dass die Hersteller
die folgenden Anforderungen erfüllen.

**A_17809-01 - Bereitstellung weiterer ePA-Produkttypen für Zulassungstest**

Der Hersteller eines der im Folgenden genannten Produkttypen MUSS die in seinen
produktübergreifenden EvT genutzten ePA-Produkte der TDI der TU für den
Zulassungstest zur Verfügung stellen. Hierzu gehören das ePA-Aktensystem, das
Frontend des Versicherten, der SGD1 sowie der Signaturdienst. **[\<=]**

### 8.1 ePA-Aktensystem

**A_15641 - technischer Prozess für Aktenzustände**

Der Hersteller eines ePA-Aktensystems MUSS eine oder mehrere Schnittstellen
anbieten, die es der TDI der TU ermöglicht, automatisiert Aktenkonten in die
folgenden Zustände zu bringen: 

 ---> UL

**[\<=]**

Eine mögliche Realisierung der Anforderung würde z.B. darin bestehen, dass der
Hersteller des Aktensystems in regelmäßigen Zeitintervallen (z.B. alle 2h)
ein mit der TDI der TU definiertes Backup bzw. einen Snapshot wiederherstellt.
Auch der definierte Inhalt eines Aktenkontos soll zusammen mit der TDI der TU
festgelegt werden.

**A_15643 - Legitimierung von Testidentitäten**

Der Hersteller eines ePA-Aktensystems MUSS die von der TDI der TU vorgegebenen
Testidentitäten für die Eröffnung und Verwaltung eines Kontos legitimieren.
**[\<=]**

Hinweis: Dazu zählen auch von der gematik erstellte Testkarten.

**A_18806 - Durchführung von gematik-Testfällen (EvT) beim ePA-Aktensystem**

Hersteller von ePA-Aktensystemen MÜSSEN im Rahmen ihrer eigenverantwortlichen
Tests, die von der gematik zur Verfügung gestellten Testfälle durchführen.
**[\<=]**

Die von der gematik zu Verfügung gestellten Testfälle bieteneine zusätzliche
Qualitätssicherung und entbindet den Hersteller nicht vom Testen der korrekten
Funktionalität nach Anforderungslage.

### 8.2 ePA-Frontend des Versicherten

Im Rahmen der Testphase Eigenverantwortlicher Test kann der Hersteller eines
ePA-Frontend des Versicherten auch Tests mit einem von der gematik zur
Verfügung gestellten Aktensystem-Simulator durchführen. Die mit diesem
Simulator durchgeführten Testfälle können als Nachweis der
Anforderungserfüllung der eigenverantwortlichen Tests genutzt werden. Die
Liste der Anforderungen, die durch den Einsatz des Aktensystem-Simulators für
die EvT genutzt werden können, wird vor Bereitstellung des
Aktensystem-Simulators mitgeteilt.

**A_15644-01 - Importieren kryptografischer Artefakte**

Der Hersteller eines ePA-Frontend des Versicherten MUSS die TDI der TU dadurch
unterstützen, dass das ePA-Frontend des Versicherten im Test kryptografische
Artefakte (z.B. Schlüssel oder Zertifikate) für das simulierte Aktensystem
akzeptiert und diese von der TDI der TU importiert werden können.  **[\<=]**

**A_15695-01 - Geräte für ePA-Frontend des Versicherten**

Der Hersteller eines ePA-Frontend des Versicherten MUSS bei

 ---> UL

der TDI der TU ein vollständig vorinstalliertes Gerät für jedes unterstützte
Betriebssystem inkl. benötigter Lizenzen und Zugangsdaten bereitstellen. Auf
dem Gerät MUSS eine Test-App nach [gemSpec_Frontend_Vers] installiert sein. **[\<=]**

**A_18394-01 - Bereitstellung eines ePA-Frontend des Versicherten bei
Folgezulassungen**

Der Hersteller eines ePA-Frontend des Versicherten MUSS bei Folgezulassungen die
Geräte über eine der folgenden Möglichkeiten bereitstellen:

 ---> OL

**[\<=]**

**A_17612-01 - Alternative Identität erstellen**

Ein Hersteller eines ePA-Frontend des Versicherten das die alternative
Authentisierung unterstützt, MUSS auf Anfrage der TDI der TU alternative
Identitäten des Versicherten bereitstellen. **[\<=]**

**A_21193-01 - ePA-Frontend des Versicherten mit Testtreiber - grafische
Logausgabe**

Der Hersteller eines ePA-Frontend des Versicherten MUSS im Rahmen der
Bereitstellung einer App mit Testtreiberschnittstelle nach [gemSpec_ePA_FdV]
auf dem Testgerät eine grafische Logausgabe mit folgenden Informationen
bereitstellen:·         TSL-Updateo    Ergebnis
(success/failed)o    Element TSLSequenceNumber der aktiven TSL (nach der
Aktualitätsprüfung / dem Update)o    Erstes Element TSLLocation der
aktiven TSL (nach der Aktualitätsprüfung / dem Update)·        
Zertifikatsprüfung (z.B. bei TLS-Handshakes und
VAU-Verbindungsaufbauten)o    Seriennummer des Zertifikatso    Ergebnis
der Zertifikatsprüfung (success/failed)o    OCSP-Status
(good/revoked/unknown/unavailable)·         Operationo   
\<Interface\>::\<Operationsname\>o    Ergebnis der Operation
(success/failed)Ein Eintrag "Operation" enthält jeweils eine technische
Operation der Komponenten Authentisierung, Autorisierung, Dokumentenverwaltung,
SigD, SGD1, SGD2 oder VZD.Jeder Logeintrag MUSS mit einem lesbaren Zeitstempel
(Datum und Uhrzeit) beginnen. \<=Hinweis:Der OCSP-Status "unavailable" soll
genutzt werden, falls aus irgendeinem Grund kein OCSP-Status ermittelt werden
konnte, z.B. Nicht-Erreichbarkeit des OCSP. Die anderen drei Statuswerte
entsprechen dem, was ein OCSP-Responder zurückliefern kann. **[\<=]**

**A_21195 - ePA-Frontend des Versicherten: Beschränkung Einsatz der Logausgabe**

Das produktive Frontend des Versicherten DARF die Logausgabe nach A_21193-01
NICHT enthalten. **[\<=]**

### 8.3 Basis-Consumer/KTR-Consumer

Für die Testbarkeit eines Basis- oder KTR-Consumers muss der Hersteller dieses
Produkttyps die folgende Anforderung erfüllen.

**A_17317 - Zugang zum KTR-Consumer bzw. Basis-Consumer**

Der Hersteller eines Basis-Consumers oder KTR-Consumers MUSS nach der Anbindung
seines Produktes in der TU dem Test der gematik einen Zugang auf die
Clientschnittstelle zu seinem Produkt einrichten. **[\<=]**

### 8.4 Signaturdienst

Für die Testbarkeit eines Signaturdiensts muss der Hersteller dieses
Produkttyps die folgende Anforderung erfüllen.

**A_17539 - Zuweisung alternativer Versicherten-Identitäten**

Der Hersteller eines Signaturdienstes MUSS der TDI der TU auf Anfrage
alternative Identitäten für Versicherte erstellen können. **[\<=]**

### 8.5 Schlüsselgenerierungsdienst

Für die Testbarkeit eines Schlüsselgenerierungsdienstes muss der Hersteller
dieses Produkttyps die folgenden Anforderungen erfüllen.

**A_17778 - Zugriff auf Schnittstellen des Schlüsselgenerierungsdienstes**

Der Hersteller eines Schlüsselgenerierungsdienstes MUSS der TDI der TU direkten
Zugriff durch die TU auf seine spezifizierten Schnittstellen bereitstellen.
**[\<=]**

### 9 Weitere Anwendungen

Die Anbieter weiterer Anwendungen (weitere Anwendungen des Gesundheitswesens
oder weiterer Anwendungen des Gesundheitswesens mit Zugriff auf Dienste der TI
aus angeschlossenen Netzen des Gesundheitswesens (WANDA Smart)) durchlaufen die
in den vorherigen Kapiteln genannte Testvorgehensweise nur teilweise, da sie
selbst keine Erfüllung der von der gematik erstellten Spezifikationen
nachweisen müssen. Sie müssen allerdings nachweisen, dass die Services bzw.
Komponenten, die sie von der TI nutzen keine negativen Auswirkungen auf
dieselben haben – den sogenannten Schnittstellentests.

Der Anbieter einer weiteren Anwendung hat die Möglichkeit für eigene Tests die
Referenzumgebung der gematik zu nutzen. Die Koordination für den Zugang
übernimmt auf Seiten der gematik der Test- & Transitionmanager.

### 9.1 Vorbereitung der EvT zur funktionalen Eignung

Vor Beginn der EvT in der RU ist eine Freischaltung des Serviceportals und des
Testumgebungskalenders RU erforderlich. Die Freischaltung eines Zugangs zum
Testkalender und zum Serviceportal der RU wird vom TTM veranlasst. Der Eintrag
der geplanten Testzeiträume in den Testkalender der RU wird vom jeweiligen
Antragssteller selbst durchgeführt. Der TTM führt den Bestätigungsnehmer
durch die notwendigen Prozesse und unterstützt den Anbieter weiterer
Anwendungen beim Zugang zur RU.

### 9.2 Durchführung EvT zur funktionalen Eignung

Durch den Bestätigungsnehmer ist die erforderliche Testspezifikation inkl. der
Testfallspezifikationen zu erstellen und die Testdurchführung in
Testprotokollen und einem Testbericht zu dokumentieren. Eine Orientierungshilfe
für die Ausgestaltung der Testfallspezifikation ist im Anhang B des
Testkonzepts zu finden. Für den Testbericht stellt die gematik ebenso ein
Template im Anhang B zur Verfügung.

Die Dokumente werden durch die gematik einer Güteprüfung unterzogen.

### 9.3 Schnittstellentests in der TU

Voraussetzung für den Start der Schnittstellentests durch die gematik ist eine
vollständige Installation und Konfiguration des Testobjekts durch den Anbieter
der weiteren Anwendung.

Nach Durchführung der Schnittstellentests wird das Ergebnis in einem
Testbericht dokumentiert. Dieser Testbericht dient bei einem positiven Ergebnis
als Nachweis der funktionalen Eignung des Produkts und wird an die
Zulassungsstelle der gematik übergeben.

**WA-A_2121 - Verfügbarkeit der Anwendung in der Testumgebung**

Der Anbieter einer WANDA Smart MUSS auf Anfrage der gematik alle für
Bestätigungstests bereitgestellten Dienste einer WANDA Smart in der
Testumgebung zur Verfügung stellen. **[\<=]**

**WA-A_2122 - Eigenverantwortlicher Test: Anbieter weiterer Anwendungen**

Der Anbieter einer WANDA Smart MUSS im Rahmen der Eigenverantwortlichen Tests
seine Pflichten gemäß Tabelle Tab_Test_005 Eigenverantwortlicher Test
erfüllen. **[\<=]**

<table><tr><th>
Testphase

</th><th>
Eigenverantwortlicher Test

</th></tr><tr><td>
Beschreibung

</td><td>
In der Testphase „Eigenverantwortlicher Test“ werden die weiteren
Anwendungen durch die Anbieter gegen die Anforderungen aus dem Abschnitt
„Schnittstellentest“ des Anwendungssteckbriefs für andere Anwendungen des
Gesundheitswesens geprüft, sofern sie für die Anwendung relevant sind.

</td></tr><tr><td>
Ziel

</td><td>
 ---> UL

</td></tr><tr><td>
Eingangskriterien

</td><td>
 ---> UL

</td></tr><tr><td>
Ausgangskriterien

</td><td>
 ---> UL

</td></tr><tr><td>
Testdokumentation/ Leistungsgegenstände

</td><td>
 ---> UL

</td></tr><tr><td>
Teststufen

</td><td>
 ---> UL

</td></tr><tr><td>
Systemumgebung

</td><td>
 ---> UL

</td></tr><tr><td>
Aufgaben des Test & Transitionmanagers

</td><td>
 ---> UL

</td></tr><tr><td>
Pflichten Anbieter weiterer Anwendungen

</td><td>
 ---> UL

</td></tr></table>

**WA-A_2123 - Eigenverantwortlicher Test: Verwendung Template**

Der Anbieter einer WANDA Smart SOLL im Rahmen der Eigenverantwortlichen Tests
das von der gematik erstellte Template für den Testbericht nutzen. **[\<=]**

**WA-A_2124 - Bestätigungstest: Anbieter weiterer Anwendungen**

Der Anbieter einer WANDA Smart MUSS im Rahmen der Bestätigungstests seine
Pflichten gemäß Tabelle Tab_Test_007 Bestätigungstest erfüllen. **[\<=]**

<table><tr><th>
Testphase

</th><th>
Bestätigungstest

</th></tr><tr><td>
Beschreibung

</td><td>
In der Testphase „Bestätigungstest“ werden Produkte zum Nachweis der
Produktivbetriebsreife geprüft.

</td></tr><tr><td>
Ziel

</td><td>
 ---> UL

</td></tr><tr><td>
Eingangskriterien

</td><td>
 ---> UL

</td></tr><tr><td>
Ausgangskriterien

</td><td>
 ---> UL

</td></tr><tr><td>
Testdokumentation/ Leistungsgegenstände

</td><td>
 ---> UL

</td></tr><tr><td>
Teststufen

</td><td>
 ---> UL

</td></tr><tr><td>
Systemumgebung

</td><td>
 ---> UL

</td></tr><tr><td>
Aufgaben der Test- & Transitionmanager

</td><td>
 ---> UL

</td></tr><tr><td>
Aufgaben der Testdurchführenden Instanz TU

</td><td>
 ---> UL

</td></tr><tr><td>
Pflichten Hersteller und Anbieter

</td><td>
 ---> UL

</td></tr></table>

Der Anbieter Weiterer Anwendungen des Gesundheitswesens oder Weiterer
Anwendungen des Gesundheitswesens mit Zugriff auf Dienste der TI aus
angeschlossenen Netzen des Gesundheitswesens (WANDA Smart) muss die
Testaktivitäten in der Testumgebung im Bestätigungsverfahren unterstützen.
Dies kann bspw. das Auslösen eines bestimmten Events in seiner Anwendung sein,
sodass die gematik auf Seiten der TI das richtige Verhalten der Anwendung
nachvollziehen kann.

### 10 Anhang A – Verzeichnisse

### 10.1 Abkürzungen

<table><tr><th>
Kürzel

</th><th>
Erläuterung

</th></tr><tr><td>
AdV

</td><td>
Anwendung(en) des Versicherten

</td></tr><tr><td>
AZPD

</td><td>
Anbieter zentrale Plattformdienste

</td></tr><tr><td>
CAB

</td><td>
Change Advisory Board

</td></tr><tr><td>
EVT

</td><td>
Eigenverantwortliche Tests

</td></tr><tr><td>
FdV

</td><td>
Frontend des Versicherten

</td></tr><tr><td>
NFC

</td><td>
Near Field Communication

</td></tr><tr><td>
PU

</td><td>
Produktivumgebung

</td></tr><tr><td>
RU

</td><td>
Referenzumgebung

</td></tr><tr><td>
TBI

</td><td>
Testbetriebsinstanz 

</td></tr><tr><td>
TIZP

</td><td>
Testintegrator zentrale Plattformdienste

</td></tr><tr><td>
TDI

</td><td>
Testdurchführende Instanz

</td></tr><tr><td>
TKI

</td><td>
Testkoordinierende Instanz

</td></tr><tr><td>
TSP

</td><td>
Trusted Service Provider

</td></tr><tr><td>
TU

</td><td>
Testumgebung

</td></tr><tr><td>
WANDA Basic

</td><td>
Weitere Anwendungen für den Datenaustausch ohne Nutzung der TI oder derer
kryptografischen Identitäten 

</td></tr><tr><td>
WANDA Smart

</td><td>
Weitere Anwendungen für den Datenaustausch mit Nutzung der TI oder
derer kryptografischen Identitäten für eigene Anwendungszwecke

</td></tr><tr><td>
ZulT

</td><td>
Zulassungstest

</td></tr></table>

### 10.2 Glossar

<table><tr><th>
Begriff

</th><th>
Erläuterung

</th></tr><tr><td>
Anforderungsbasierter Test

</td><td>
Bezeichnet eine Testvorgehensweise, bei der die Testfälle von den Anforderungen
abgeleitet werden. Grundsätzlich soll für jede Anforderung die Erfüllung
nachgewiesen werden.

</td></tr><tr><td>
Anwendungsfallbasierter Test

</td><td>
Bezeichnet eine Testvorgehensweise, bei der die Testfälle von den (technischen
oder fachlichen) Anwendungsfällen abgeleitet werden. Grundsätzlich soll für
jeden Anwendungsfall die positive Durchführung nachgewiesen werden.

</td></tr><tr><td>
Change Advisor Board

</td><td>
Gremium im ITSM-TI-Prozess Change Management zur Bewertung und Autorisierung von
Requests for Change (RfC), die potenziell übergreifende Auswirkungen auf
andere TI-Produktinstanzen haben. Das CAB wird anlassbezogen vom
Servicebetriebsverantwortlichen (SBV) einberufen, Teilnehmer sind Stakeholder
der vom change betroffenen Produkte und TI-Services.

</td></tr></table>

Ein umfangreiches Glossar findet sich im Fachportal der gematik-Website.

### 10.3 Abbildungsverzeichnis

- [Abbildung-1] - Überblick der Testphasen
- [Abbildung-2] - Exemplarischer Ablauf eines Testverfahrens
- [Abbildung-3] - Rollen innerhalb der Systemumgebungen
- [Abbildung-4] - Zuordnung Testarten
- [Abbildung-5] - Übersicht des Gesamtsystems Telematikinfrastruktur gemäß [gemKPT_Arch_TIP]

### 10.4 Tabellenverzeichnis

- [Tabelle-1] -  Tab_Test_005 Eigenverantwortlicher Test
- [Tabelle-2] - Tab_Test_006 Zulassungstest
- [Tabelle-3] - Tab_Test_001 Überblick Systemumgebungen im Rahmen von Test
- [Tabelle-4] - Tab_Test_019 Produkttypen der TI
- [Tabelle-5] -  Inhalte und Bedingungen des Servicekatalogs
- [Tabelle-6] - Tab_Test_021 Szenario: Zulassung eines neuen Produkts
- [Tabelle-7] - Tab_Test_022 Szenario: Zulassung eines geänderten Produkts
- [Tabelle-8] - Tab_Test_008 Produkttest (EvT)
- [Tabelle-9] - Tab_Test_009 Produktübergreifender Test (EvT)
- [Tabelle-10] - Tab_Test_010 Eingangsprüfung (ZulT)
- [Tabelle-11] - Tab_Test_011 Produkttest (ZulT)
- [Tabelle-12] - Tab_Test_012 Produktübergreifender Test (ZulT)
- [Tabelle-14] - Tab_Test_013 Testkonzept
- [Tabelle-15] - Tab_Test_014 Testspezifikation
- [Tabelle-16] - Tab_Test_015 Release Notes
- [Tabelle-17] - Tab_Test_016 Produktdokumentation
- [Tabelle-18] - Tab_Test_017 Testprotokoll
- [Tabelle-19] - Tab_Test_018 Testbericht
- [Tabelle-20] -  Tab_Test_005 Eigenverantwortlicher Test
- [Tabelle-21] -  Tab_Test_007 Bestätigungstest
- [Tabelle-22] - Tab_Test_023 Vorlage Testkonzept
- [Tabelle-23] - Tab_Test_024 Beispiel Testkonzept
- [Tabelle-24] - Tab_Test_025 Vorlage Testfallspezifikation
- [Tabelle-25] - Tab_Test_026 Beispiel Testfall 1
- [Tabelle-26] - Tab_Test_027 Beispiel Testfall 2
- [Tabelle-27] - Tab_Test_028 Beispiel Testfall 3
- [Tabelle-28] - Tab_Test_029 Beispiel Testfall 4
- [Tabelle-29] - Tab_Test_030 Beispiel Testfall 5
- [Tabelle-30] - Tab_Test_031 Beispiel Testkonfiguration
- [Tabelle-31] - Tab_Test_032 Vorlage Testprotokoll

### 10.5 Referenzierte Dokumente

### 10.5.1 Dokumente der gematik

<table><tr><th>
[Quelle]

</th><th>
Herausgeber: Titel

</th></tr><tr><td>
[gemKPT_Betr]

</td><td>
gematik: Betriebskonzept Online-Produktivbetrieb (OPB)

</td></tr><tr><td>
[gemSpec_eRp_FdV_AdV]

</td><td>
gematik: Spezifikation E-Rezept-Anwendung des Versicherten

</td></tr><tr><td>
[gemSpec_Perf]

</td><td>
gematik: Übergreifende Spezifikation Performance und Mengengerüst TI-Plattform

</td></tr><tr><td>
[gemSpec_TK]

</td><td>
gematik: Spezifikation für Testkarten gematik (eGK, HBA, (g)SMC) der Generation
2

</td></tr><tr><td>
[gemSpec_Krypt]

</td><td>
gematik: Übergreifende Spezifikation Verwendung kryptographischer Algorithmen
in der Telematikinfrastruktur

</td></tr><tr><td>
[gemSpec_TK_FD]

</td><td>
gematik: Spezifikation für Testkarten Fachdienste (eGK) der Generation 2

</td></tr></table>

### 10.5.2 Weitere Dokumente

<table><tr><th>
[Quelle]

</th><th>
Herausgeber (Erscheinungsdatum): Titel

</th></tr><tr><td>
[RFC2119]

</td><td>
RFC 2119 (März 1997): Key words for use in RFCs to Indicate Requirement Levels
S. Bradner

</td></tr><tr><td>
[IEEE829]

</td><td>
Software & Systems Engineering Standards Committee: IEEE Standard für Software
and System Test Documentaion, Revision 2008

</td></tr></table>

### 11 Anhang B – Beispielhafte Testdokumentation

In diesem Kapitel werden die Anforderung an die Testdokumentation durch
Beispiele ergänzt und ein möglicher Ansatz zur Beschreibung des Testvorgehens
vom Testkonzept über die Testspezifikation bis zum Testbericht erläutert.

### 11.1 Testkonzept

Die folgende Tabelle zeigt eine mögliche Vorlage zur Übersicht der zu
testenden Leistungsmerkmale eines Produkttyps sowie die Zuordnung zu den
Prüfverfahren und einem oder mehreren Testfällen. Auf Grund des
unterschiedlichen Umfangs und Komplexität der Anforderungen oder
Anwendungsfälle kann es notwendig sein, diese zunächst in Teilaspekte zu
zerlegen welche jeweils durch Testfälle abgedeckt werden. Das Ziel hierbei ist
es, eine Rückverfolgbarkeit zwischen den zu testenden Leistungsmerkmalen und
den zugeordneten Testfällen herzustellen. Des Weiteren sollte beschrieben
werden, welche Leistungsmerkmale nicht geprüft werden.

<table><tr><th>
Anforderung ID

</th><th>
Anforderung Klassifikation

</th><th>
Prüfverfahren

</th><th>
Testfall-ID

</th><th>
Testfall Name

</th></tr><tr><td>
Eindeutige ID der Anforderung

</td><td>
Klassifikation der Anforderung (MUSS, SOLL, KANN)

</td><td>
Prüfverfahren

</td><td>
Eindeutige ID des Testfalls

</td><td>
Eindeutiger, sprechender Name des Testfalls

</td></tr><tr><td>
…

</td><td>
…

</td><td>
…

</td><td>
…

</td><td>
…

</td></tr><tr><td>
…

</td><td>
…

</td><td>
…

</td><td>
…

</td><td>
…

</td></tr></table>

Die folgende Tabelle zeigt die exemplarische Übersicht von ausgewählten
Anforderungen und zugeordneten Testfällen zu konkreten Anforderungen aus ORS1.

<table><tr><th>
Anforderung ID

</th><th>
Anforderung Klassifikation

</th><th>
Prüfverfahren

</th><th>
Testfall-ID

</th><th>
Testfall Name

</th></tr><tr><td>
TIP1-A_4349

</td><td>
MUSS

</td><td>
Herstellererklärung

</td><td>
---

</td><td>
---

</td></tr><tr><td>
TIP1-A_4540

</td><td>
MUSS

</td><td>
Funktionaler Test

</td><td>
TF_00001 *

</td><td>
Reaktion auf KT-Service-Announcement bei deaktiviertem Service Discovery

</td></tr><tr><td rowspan="2">
TIP1-A_4557

</td><td rowspan="2">
MUSS

</td><td>
Funktionaler Test

</td><td>
TF_00002

</td><td>
Aendern der Korrelationswerte eines Kartenterminals: bekannt - zugewiesen -
bekannt (interaktiv)

</td></tr><tr><td>
Funktionaler Test

</td><td>
TF_00003 *

</td><td>
Aendern der Korrelationswerte eines Kartenterminals: gepairt - aktiv - gepairt -
zugewiesen (interaktiv)

</td></tr><tr><td rowspan="3">
TIP1-A_4598

</td><td rowspan="3">
MUSS

</td><td>
Funktionaler Test

</td><td>
TF_00004 *

</td><td>
Systemereignis absetzen

</td></tr><tr><td>
Funktionaler Test

</td><td>
TF_00005 *

</td><td>
Systemereignis absetzen- XPath-Filter

</td></tr><tr><td>
Funktionaler Test

</td><td>
TF_00006

</td><td>
Systemereignis absetzen- BOOTUP/COMPLETE

</td></tr><tr><td rowspan="16">
TIP1-A_4705

</td><td rowspan="16">
MUSS

</td><td>
Funktionaler Test

</td><td>
TF_00007

</td><td>
TSL manuell importieren - OK (interaktiv)

</td></tr><tr><td>
Funktionaler Test

</td><td>
TF_00008

</td><td>
TSL manuell importieren - Fehler 4128 (interaktiv)

</td></tr><tr><td>
Funktionaler Test

</td><td>
TF_00009

</td><td>
TSL manuell importieren - Fehler 1017 (interaktiv)

</td></tr><tr><td>
Funktionaler Test

</td><td>
TF_00010

</td><td>
TSL manuell importieren - Fehler 1003 (interaktiv)

</td></tr><tr><td>
Funktionaler Test

</td><td>
TF_00011

</td><td>
TSL manuell importieren - Fehler 1005 (interaktiv)

</td></tr><tr><td>
Funktionaler Test

</td><td>
TF_00012

</td><td>
TSL manuell importieren - Fehler 1004 (interaktiv)

</td></tr><tr><td>
Funktionaler Test

</td><td>
TF_00013

</td><td>
TSL manuell importieren - Fehler 1007 (interaktiv)

</td></tr><tr><td>
Funktionaler Test

</td><td>
TF_00014

</td><td>
TSL manuell importieren - Fehler 1008 (interaktiv)

</td></tr><tr><td>
Funktionaler Test

</td><td>
TF_00015

</td><td>
TSL manuell importieren - Fehler 1009 (interaktiv)

</td></tr><tr><td>
Funktionaler Test

</td><td>
TF_00016

</td><td>
TSL manuell importieren - Fehler 1011 (interaktiv)

</td></tr><tr><td>
Funktionaler Test

</td><td>
TF_00017

</td><td>
TSL manuell importieren - Fehler 1012 (interaktiv)

</td></tr><tr><td>
Funktionaler Test

</td><td>
TF_00018

</td><td>
TSL manuell importieren - Fehler 1013 (interaktiv)

</td></tr><tr><td>
Funktionaler Test

</td><td>
TF_00019

</td><td>
TSL manuell importieren - Fehler 1026 (interaktiv)

</td></tr><tr><td>
Funktionaler Test

</td><td>
TF_00020

</td><td>
TSL manuell importieren - Fehler 1030 (interaktiv)

</td></tr><tr><td>
Funktionaler Test

</td><td>
TF_00021

</td><td>
TSL manuell importieren - Fehler 1036 (interaktiv)

</td></tr><tr><td>
Funktionaler Test

</td><td>
TF_00022

</td><td>
TSL manuell importieren - Fehler 1042 (interaktiv)

</td></tr><tr><td>
TIP1-A_5112

</td><td>
MUSS

</td><td>
Funktionaler Test

</td><td>
TF_00023 *

</td><td>
Operation RenewSubscriptions

</td></tr><tr><td>
…

</td><td>
</td><td>
…

</td><td>
…

</td><td>
…

</td></tr></table>

* Zu den Testfällen TF_00001, TF_00003, TF_00004, TF_00005 und TF_00023 sind im
folgenden Abschnitt mögliche Testfallspezifikationen beschrieben.

### 11.2 Testspezifikation

Die folgende Tabelle zeigt eine mögliche Vorlage zur Spezifikation eines
Testfalls.

<table><tr><th>
ID

</th><th colspan="3">
Eindeutige ID des Testfalls

</th></tr><tr><td>
Name

</td><td colspan="3">
Eindeutiger, sprechender Name des Testfalls

</td></tr><tr><td>
Version

</td><td colspan="3">
Eindeutige Version des Testfalls (z.B. Datum, Versionsnummer)

</td></tr><tr><td>
Anforderung-ID

</td><td colspan="3">
ID der Anforderung welche durch den Testfall geprüft wird, alternativ Bezug zu
Anwendungsfall-ID o.ä.

</td></tr><tr><td>
Beschreibung

</td><td colspan="3">
Beschreibung des Testfalls mit Angabe des Testziels

</td></tr><tr><td>
Vorbedingungen

</td><td colspan="3">
Beschreibung aller notwendigen Vorbedingungen

</td></tr><tr><td>
Nachbedingungen

</td><td colspan="3">
Beschreibung aller erwarteten Nachbedingungen

</td></tr><tr><td rowspan="4">
Schritte

</td><td>
#

</td><td>
Beschreibung

</td><td>
Erwartetes Ergebnis

</td></tr><tr><td>
1

</td><td>
Eindeutige Beschreibung des durchzuführenden Schritts

</td><td>
Eindeutige Beschreibung des erwarteten Ergebnisses des Schritts.

</td></tr><tr><td>
2

</td><td>
…

</td><td>
…

</td></tr><tr><td>
3

</td><td>
…

</td><td>
…

</td></tr></table>

Die folgenden Tabellen zeigen die exemplarische Beschreibung von ausgewählten
Testfällen zu konkreten Anforderungen aus ORS1.

Good Practice: Bei der Spezifikation von TF_00004 wird beim erwarteten Ergebnis
von Schritt 4 explizit eine Return Message aus bereits ermittelten Parametern
zusammengebaut – es ist explizit klar was genau in jedem Feld steht
(entsprechend der Standardkonfiguration) und kann geprüft werden.

<table><tr><th>
ID

</th><th colspan="3">
TF_00004

</th></tr><tr><td>
Name

</td><td colspan="3">
Systemereignis absetzen

</td></tr><tr><td>
Version

</td><td colspan="3">
19.02.2015 13:09:00

</td></tr><tr><td>
Anforderung-ID

</td><td colspan="3">
TIP1-A_4598

</td></tr><tr><td>
Beschreibung

</td><td colspan="3">
Dieser Testfall prüft:

 ---> OL

</td></tr><tr><td>
Vorbedingungen

</td><td colspan="3">
Basiskonfiguration [LDD/WDE 2]

LOG_LEVEL_SYSLOG = Info

</td></tr><tr><td>
Nachbedingungen

</td><td colspan="3">
Rufe von [WP1] die Operation Unsubscribe (EventService) mit gültigem Context
und SubscriptionID = SID1 auf.

Rufe von [WP2] die Operation Unsubscribe mit gültigem Context und
SubscriptionID = SID2 auf.

Basiskonfiguration [LDD/WDE 2] ist erreicht.

</td></tr><tr><td rowspan="6">
Schritte

</td><td>
#

</td><td>
Beschreibung

</td><td>
Erwartetes Ergebnis

</td></tr><tr><td>
1

</td><td>
Entferne [eGK A] aus [KT A].

Anmerkung: [KT A] ist [WP1] zugeordnet, aber nicht [WP2].

</td><td>
Kein Ergebnis erwartet.

</td></tr><tr><td>
2

</td><td>
Abonniere von [WP1] das Ereignis CARD/INSERTED durch Aufruf der Operation
Subscribe (EventService) mit gültigem Context und folgenden Parametern:

 ---> UL

</td><td>
[WP1] empfängt eine SubscribeResponse mit:

 ---> UL

</td></tr><tr><td>
3

</td><td>
Abonniere von [WP2] das Ereignis CARD/INSERTED durch Aufruf der Operation
Subscribe (EventService) mit gültigem Context und folgenden Parametern:

 ---> UL

</td><td>
[WP2] empfängt eine SubscribeResponse mit:

 ---> UL

</td></tr><tr><td>
4

</td><td>
Stecke [eGK A] in [KT A], wobei [KT A] das entsprechende Slot-Ereignis an den
Konnektor sendet.

</td><td>
[WP1] empfängt an der in Subscription.EventTo angegebenen Adresse und Port eine
cetp-Message mit einem Ereignisdokument Event mit:

 ---> UL

[WP2] empfängt kein Konnektor-Ereignis.

</td></tr><tr><td>
5

</td><td>
Prüfe Systemprotokoll auf Eintrag "CARD/INSERTED" mit passendem Datum und
Uhrzeit.

</td><td>
Eintrag ist im Systemprotokoll vorhanden.

</td></tr></table>

Good Practice: Bei der Spezifikation von TF_00005 werden vorher mitgetrackte
Werte später wieder verwendet, z.B. beim erwarteten Ergebnis von Schritt 4.

<table><tr><th>
ID

</th><th colspan="3">
TF_00005

</th></tr><tr><td>
Name

</td><td colspan="3">
Systemereignis absetzen – XPath-Filter

</td></tr><tr><td>
Version

</td><td colspan="3">
19.02.2015 13:09:01

</td></tr><tr><td>
Anforderung-ID

</td><td colspan="3">
TIP1-A_4598

</td></tr><tr><td>
Beschreibung

</td><td colspan="3">
Dieser Testfall prüft:

 ---> OL

</td></tr><tr><td>
Vorbedingungen

</td><td colspan="3">
Basiskonfiguration [LDD/WDE 2]

</td></tr><tr><td>
Nachbedingungen

</td><td colspan="3">
Rufe von [WP1] für die SubscriptionIDs SID1, SID2 und SID3 die Operation
Unsubscribe (EventService) mit gültigem Context auf.

Basiskonfiguration [LDD/WDE 2] ist erreicht.

</td></tr><tr><td rowspan="7">
Schritte

</td><td>
#

</td><td>
Beschreibung

</td><td>
Erwartetes Ergebnis

</td></tr><tr><td>
1

</td><td>
Entferne [eGK A] aus [KT A].

</td><td>
Kein Ergebnis erwartet.

</td></tr><tr><td>
2

</td><td>
Abonniere von [WP1] das Ereignis CARD/INSERTED durch Aufruf der Operation
Subscribe (EventService) mit gültigem Context und folgenden Parametern:

 ---> UL

</td><td>
[WP1] empfängt eine SubscribeResponse mit:

 ---> UL

</td></tr><tr><td>
3

</td><td>
Abonniere von [WP1] das Ereignis CARD/INSERTED durch Aufruf der Operation
Subscribe (EventService) mit gültigem Context und folgenden Parametern:

 ---> UL

</td><td>
[WP1] empfängt eine SubscribeResponse mit:

 ---> UL

</td></tr><tr><td>
4

</td><td>
Abonniere von [WP1] das Ereignis CARD/INSERTED durch Aufruf der Operation
Subscribe (EventService) mit gültigem Context und folgenden Parametern:

 ---> UL

</td><td>
[WP1] empfängt eine SubscribeResponse mit:

 ---> UL

</td></tr><tr><td>
5

</td><td>
Stecke [eGK A] in [KT A], wobei [KT A] das entsprechende Slot-Ereignis an den
Konnektor sendet

</td><td>
[WP1] empfängt an der in Subscription.EventTo angegebenen Adresse und Port eine
cetp-Message mit einem Ereignisdokument Event mit:

 ---> UL

[WP1] empfängt kein Event mit SubscriptionID = SID2 (XPath-Filter schließt
Subscription aus).

[WP1] empfängt kein Event mit SubscriptionID = SID3 (XPath-Filter löst Fehler
4095 aus).

</td></tr><tr><td>
6

</td><td>
Prüfe Protokoll auf Fehler 4095 mit passendem Zeitstempel und

 ---> UL

</td><td>
Fehlereintrag ist im Protokoll vorhanden.

</td></tr></table>

Good Practice: Bei der Spezifikation von TF_00023 wird in den Vorbedingungen
noch mal explizit auf den Parameter der Standardkonfiguration aufmerksam
gemacht, der für diesen Testfall der wichtige ist.

<table><tr><th>
ID

</th><th colspan="3">
TF_00023

</th></tr><tr><td>
Name

</td><td colspan="3">
Operation RenewSubscriptions

</td></tr><tr><td>
Version

</td><td colspan="3">
19.02.2015 13:10:00

</td></tr><tr><td>
Anforderung-ID

</td><td colspan="3">
TIP1-A_5112

</td></tr><tr><td>
Beschreibung

</td><td colspan="3">
Dieser Testfall prüft:

 ---> OL

Anmerkung: Vgl. TIP1-A_4610-02

</td></tr><tr><td>
Vorbedingungen

</td><td colspan="3">
Basiskonfiguration [LDD/WDE 2],

LOG_LEVEL_SYSLOG = Info.

</td></tr><tr><td>
Nachbedingungen

</td><td colspan="3">
Rufe von [WP1] jeweils für SID1, SID2, SID3 die Operation Unsubscribe
(EventService) mit gültigem Context und SubscriptionID = SID1|SID2|SID3 auf.

Basiskonfiguration [LDD/WDE 2] ist erreicht.

</td></tr><tr><td rowspan="11">
Schritte

</td><td>
#

</td><td>
Beschreibung

</td><td>
Erwartetes Ergebnis

</td></tr><tr><td>
1

</td><td>
Abonniere von [WP1] das Ereignis CARD/INSERTED durch Aufruf der Operation
Subscribe (EventService) mit gültigem Context und folgenden Parametern:

 ---> UL

</td><td>
[WP1] empfängt eine SubscribeResponse mit:

 ---> UL

</td></tr><tr><td>
2

</td><td>
Abonniere von [WP1] das Ereignis CARD/REMOVED durch Aufruf der Operation
Subscribe (EventService) mit gültigem Context und folgenden Parametern:

 ---> UL

</td><td>
[WP1] empfängt eine SubscribeResponse mit:

 ---> UL

</td></tr><tr><td>
3

</td><td>
Abonniere von [WP1] das Ereignis NETWORK/VPN_TI/UP durch Aufruf der Operation
Subscribe (EventService) mit gültigem Context und folgenden Parametern:

 ---> UL

</td><td>
[WP1] empfängt eine SubscribeResponse mit:

 ---> UL

</td></tr><tr><td>
4

</td><td>
Rufe von [WP1] die Operation GetSubscriptions (EventService) mit gültigem
Context ohne Element mandant-wide auf.

</td><td>
[WP1] empfängt eine GetSubscriptionsResponse mit

 ---> UL

</td></tr><tr><td>
5

</td><td>
Merke den Wert TerminationTime für die Subscription mit SubscriptionID = SID1
als TT01.

Merke den Wert TerminationTime für die Subscription mit SubscriptionID = SID2
als TT02.

Merke den Wert TerminationTime für die Subscription mit SubscriptionID = SID3
als TT03.

</td><td>
TT01, TT02 und TT03 sind mit einer Toleranz von maximal einer Minute identisch.

</td></tr><tr><td>
6

</td><td>
Warte 2 Minuten

</td><td>
Kein Ergebnis erwartet

</td></tr><tr><td>
7

</td><td>
Merke aktuelle Systemzeit als ZP1 und rufe von [WP1] die Operation
RenewSubscriptions (EventService) mit gültigem Context und SubscriptionID =
SID1, SID3 auf.

</td><td>
[WP1] erhält eine RenewSubscriptionsResponse mit:

 ---> UL

</td></tr><tr><td>
8

</td><td>
Merke den Wert TerminationTime für das SubscriptionRenewal mit SubscriptionID =
SID1 als TT11.

Merke den Wert TerminationTime für das SubscriptionRenewal mit SubscriptionID =
SID3 als TT13.

</td><td>
TT11 = ZP1 + 25 Stunden +/- Toleranz

TT13 = ZP1 + 25 Stunden +/- Toleranz

</td></tr><tr><td>
9

</td><td>
Rufe von [WP1] die Operation GetSubscriptions (EventService) mit gültigem
Context ohne Element mandant-wide auf.

</td><td>
[WP1] empfängt eine GetSubscriptionsResponse mit

 ---> UL

</td></tr><tr><td>
10

</td><td>
Merke den Wert TerminationTime für die Subscription mit SubscriptionID = SID1
als TT21.

Merke den Wert TerminationTime für die Subscription mit SubscriptionID = SID2
als TT22.

Merke den Wert TerminationTime für die Subscription mit SubscriptionID = SID3
als TT23.

</td><td>
TT11 = TT21

TT11 = TT01 + 2 Minuten +/- Toleranz

TT02 = TT22

TT13 = TT23

TT13 = TT03 + 2 Minuten +/- Toleranz

</td></tr></table>

Good Practice: Bei der Spezifikation von TF_00001 ist der Weg zum Teststatus
explizit gemacht – manchmal ist es wichtig wie ein Status erreicht wurde,
weil das für den Testablauf wichtig werden kann, weil interne Parameter die
dabei gesetzt wurden Änderungen in Verhalten bewirken können, zudem wird
insbesondere der TUC der mit dieser Frontend Funktion abgeprüft wird explizit
gemacht (und man kann da weiterprüfen).

<table><tr><th>
ID

</th><th colspan="3">
TF_00001

</th></tr><tr><td>
Name

</td><td colspan="3">
Reaktion auf KT-Service-Announcement bei deaktiviertem Service Discovery

</td></tr><tr><td>
Version

</td><td colspan="3">
19.02.2015 16:14:52

</td></tr><tr><td>
Anforderung-ID

</td><td colspan="3">
TIP1-A_4540

</td></tr><tr><td>
Beschreibung

</td><td colspan="3">
Dieser Testfall prüft:

 ---> OL

</td></tr><tr><td>
Vorbedingungen

</td><td colspan="3">
Basiskonfiguration [LDD/WDE 2].

</td></tr><tr><td>
Nachbedingungen

</td><td colspan="3">
Deaktiviere [KT A], setze TCP Port auf KTP1 und aktiviere [KT A].

Setze über die Managementschnittstelle CTM_SERVICE_DISCOVERY_CYCLE auf CSD1.

Basiskonfiguration [LDD/WDE 2] ist erreicht.

</td></tr><tr><td rowspan="9">
Schritte

</td><td>
#

</td><td>
Beschreibung

</td><td>
Erwartetes Ergebnis

</td></tr><tr><td>
1

</td><td>
(Statusprüfung)

Lies CTM_CT_LIST über die Managementschnittstelle (gemäß TIP1-A_4551).

</td><td>
Für CT = [KT A]:

CONNECTED = Ja

TCP_PORT= TCP Port von [KT A]

SLOTS_USED enthält Slots mit [eGK A] und [SMC-B 1]

</td></tr><tr><td>
2

</td><td>
Deaktiviere [KT A].

Merke [KT A].TCP_PORT als KTP1.

Ändere den TCP Port von [KT A] auf einen Wert KTP2.

</td><td>
Kein Ergebnis erwartet.

</td></tr><tr><td>
3

</td><td>
Lies über die Managementschnittstelle CTM_SERVICE_DISCOVERY_CYCLE und merke den
Wert als CSD1.

</td><td>
Managementschnittstelle liefert Wert.

</td></tr><tr><td>
4

</td><td>
Setze über die Managementschnittstelle CTM_SERVICE_DISCOVERY_CYCLE auf 0
(Service Discovery deaktiviert).

</td><td>
Managementschnittstelle akzeptiert Änderung

</td></tr><tr><td>
5

</td><td>
(Statusprüfung)

Lies CTM_CT_LIST über die Managementschnittstelle (gemäß TIP1-A_4551).

</td><td>
Für CT = [KT A]:

CONNECTED = Nein

SLOTS_USED ist leer.

</td></tr><tr><td>
6

</td><td>
Aktiviere [KT A], wobei [KT A] Service Announcement nach [SICCT121] auf UDP Port
CTM_SERVICE_ANNOUNCEMENT_PORT sendet.

</td><td>
Kein Ergebnis erwartet.

</td></tr><tr><td>
7

</td><td>
(Statusprüfung)

Lies CTM_CT_LIST über die Managementschnittstelle (gemäß TIP1-A_4551).

</td><td>
Für CT = [KT A]:

CONNECTED = Ja

TCP_PORT = KIP2

SLOTS_USED enthält Slots mit [eGK A] und [SMC-B 1]

Anmerkung: Damit ist gezeigt, dass TUC_KON_054 ausgeführt wurde (Aktualisierung
von CT.TCP_PORT in CTM_CT_LIST).

</td></tr><tr><td>
8

</td><td>
Prüfe [KT A] auf bestehende TLS-Verbindung und SICCT-Session (durch Abfrage der
KT-Simulation).

</td><td>
TLS-Kanal zu Konnektor ist aufgebaut.

SICCT-Session mit Benutzername ""USER"" ist aufgebaut.

Anmerkung: Damit ist gezeigt, dass TUC_KON_050 ausgeführt wurde
(Kartenterminalsitzung wurde aufgebaut).

</td></tr></table>

Good Practice: Bei der Spezifikation von TF_00003 werden Verbindungsschritte
explizit gemacht, so dass Logs genauer daraufhin geprüft werden können, ob
der Weg zu einen Zustand auch korrekt ist.

<table><tr><th>
ID

</th><th colspan="3">
TF_00003

</th></tr><tr><td>
Name

</td><td colspan="3">
Aendern der Korrelationswerte eines Kartenterminals: gepairt - aktiv - gepairt -
zugewiesen (interaktiv)

</td></tr><tr><td>
Version

</td><td colspan="3">
20.02.2015 11:23:32

</td></tr><tr><td>
Anforderung-ID

</td><td colspan="3">
TIP1-A_4557

</td></tr><tr><td>
Beschreibung

</td><td colspan="3">
Dieser Testfall prüft unter aktiver Mitwirkung des Testers die manuell
ausgelösten Übergänge des Korrelationsstatus

 ---> UL

 ---> OL

Anmerkung: Vgl. TIP1-A_4548-01

</td></tr><tr><td>
Vorbedingungen

</td><td colspan="3">
Basiskonfiguration [LDD/WDE 2].

[KT C] wird mit einer MAC-Adresse konfiguriert, die der Konnektor nicht kennt.

</td></tr><tr><td>
Nachbedingungen

</td><td colspan="3">
Deaktiviere [KT C]

Setze über die Managementschnittstelle CTM_SERVICE_DISCOVERY_CYCLE auf CSD1 und
[KT C].CORRELATION auf "bekannt"

Basiskonfiguration [LDD/WDE 2] ist erreicht.

</td></tr><tr><td rowspan="22">
Schritte

</td><td>
#

</td><td>
Beschreibung

</td><td>
Erwartetes Ergebnis

</td></tr><tr><td>
1

</td><td>
Lies über die Managementschnittstelle CTM_SERVICE_DISCOVERY_CYCLE und merke den
Wert als CSD1.

</td><td>
Managementschnittstelle liefert Wert.

</td></tr><tr><td>
2

</td><td>
Setze über die Managementschnittstelle CTM_SERVICE_DISCOVERY_CYCLE auf 0
(Service Discovery deaktiviert).

</td><td>
Managementschnittstelle akzeptiert Änderung.

</td></tr><tr><td>
3

</td><td>
(Statusprüfung)

Lies CTM_CT_LIST über die Managementschnittstelle (gemäß TIP1-A_4551).

</td><td>
CTM_CT_LIST enthält keinen Eintrag zu einem Kartenterminal mit CT.MAC_ADDRESS =
[KT C].MAC_ADDRESS

</td></tr><tr><td>
4

</td><td>
Aktiviere [KT C], wobei [KT C] Service Announcement nach [SICCT121] auf UDP Port
CTM_SERVICE_ANNOUNCEMENT_PORT sendet.

</td><td>
Kein Ergebnis erwartet.

</td></tr><tr><td>
5

</td><td>
(Statusprüfung)

Lies CTM_CT_LIST über die Managementschnittstelle (gemäß TIP1-A_4551).

</td><td>
CTM_CT_LIST enthält einen neuen Eintrag zu einem Kartenterminal mit
CT.MAC_ADDRESS = [KT C].MAC_ADDRESS

Für CT = [KT C]:

 ---> UL

Anmerkung: Es genügt hier zu prüfen, dass [KT C] vom Konnektor erkannt wurde
und den richtigen CORRELATION-Status hat.

</td></tr><tr><td>
6

</td><td>
Setze über die Managementschnittstelle [KT C].CORRELATION auf "zugewiesen".

</td><td>
Managementschnittstelle akzeptiert Änderung.

</td></tr><tr><td>
7

</td><td>
(Statusprüfung)

Lies CTM_CT_LIST über die Managementschnittstelle (gemäß TIP1-A_4551).

</td><td>
CTM_CT_LIST enthält einen neuen Eintrag zu einem Kartenterminal mit
CT.MAC_ADDRESS = [KT C].MAC_ADDRESS

Für CT = [KT C]:

 ---> UL

Anmerkung: Nach Änderung von CORRELATION auf zugewiesen wurde TUC_KON_055
zugewiesen und VALID_VERSION ermittelt.

</td></tr><tr><td>
8

</td><td>
Aufforderung an Tester: "Lösen Sie über die Managementschnittstelle das
Pairing zwischen Konnektor und [KT C] aus!"

Anmerkung: Ab Ausgabe der Aufforderung wartet die Testsuite auf Aktionen des
Konnektors.

</td><td>
[KT C] empfängt Aufforderung vom Konnektor zum Aufbau einer TLS-Verbindung.

Konnektor präsentiert [KT C] das Zertifikat ID.SAK.AUT.

(TUC_KON_037 hat im Erfolgsfall keine messbare Außenwirkung)

</td></tr><tr><td>
9

</td><td>
Aufforderung an Tester: "Bitte bestätigen Sie, dass der Konnektor an der
Managementschnittstelle einen Dialog anzeigt, in denen Ihnen der Fingerprint
von [KT C] angezeigt wird und in dem Sie zur Bestätigung des Fingerprints
aufgefordert werden. Führen Sie noch keine Aktion an der
Managementschnittstelle aus."

</td><td>
Tester bestätigt.

</td></tr><tr><td>
10

</td><td>
Aufforderung an Tester: "Bitte geben Sie den angezeigten Fingerprint ein."

</td><td>
Eingegebener Fingerprint stimmt mit Fingerprint von [KT C] überein.

</td></tr><tr><td>
11

</td><td>
Aufforderung an Tester: "Bitte bestätigen Sie an der Managementschnittstelle,
dass der korrekte Fingerprint angezeigt wird."

</td><td>
Kein Ergebnis erwartet (der Pairing-Prozess verläuft automatisch und das
Ergebnis wird im nächsten Schritt geprüft)

</td></tr><tr><td>
12

</td><td>
(Statusprüfung)

Lies CTM_CT_LIST über die Managementschnittstelle (gemäß TIP1-A_4551).

</td><td>
Für CT = [KT C]:

 ---> UL

</td></tr><tr><td>
13

</td><td>
Setze über die Managementschnittstelle [KT C].CORRELATION = "gepairt"

</td><td>
Kein Ergebnis erwartet

</td></tr><tr><td>
14

</td><td>
(Statusprüfung)

Lies CTM_CT_LIST über die Managementschnittstelle (gemäß TIP1-A_4551).

</td><td>
Für CT = [KT C]:

 ---> UL

</td></tr><tr><td>
15

</td><td>
Aufforderung an Tester: "Bitte bestätigen Sie, dass Sie über die
Managementschnittstelle den Korrelationsstatus von [KT C] von -gepairt- auf
-aktiv- und -zugewiesen- ändern können."

</td><td>
Tester bestätigt.

</td></tr><tr><td>
16

</td><td>
Aufforderung an Tester: "Bitte ändern Sie über die Managementschnittstelle den
Korrelationsstatus von [KT C] von -gepairt- auf -aktiv- und bestätigen Sie die
erfolgreiche Änderung."

</td><td>
Tester bestätigt.

</td></tr><tr><td>
17

</td><td>
(Statusprüfung)

Lies CTM_CT_LIST über die Managementschnittstelle (gemäß TIP1-A_4551).

</td><td>
Für CT = [KT C]:

 ---> UL

Anmerkung: TUC_KON_050 setzt CONNECTED = Ja.

</td></tr><tr><td>
18

</td><td>
Aufforderung an Tester: "Bitte ändern Sie über die Managementschnittstelle den
Korrelationsstatus von [KT C] von -aktiv- auf -gepairt- und bestätigen Sie die
erfolgreiche Änderung."

</td><td>
Tester bestätigt

</td></tr><tr><td>
19

</td><td>
(Statusprüfung)

Lies CTM_CT_LIST über die Managementschnittstelle (gemäß TIP1-A_4551).

</td><td>
Für CT = [KT C]:

 ---> UL

</td></tr><tr><td>
20

</td><td>
Aufforderung an Tester: "Bitte ändern Sie über die Managementschnittstelle den
Korrelationsstatus von [KT C] von -gepairt- auf -zugewiesen- und bestätigen
Sie die erfolgreiche Änderung."

</td><td>
Tester bestätigt

</td></tr><tr><td>
21

</td><td>
(Statusprüfung)

Lies CTM_CT_LIST über die Managementschnittstelle (gemäß TIP1-A_4551).

</td><td>
Für CT = [KT C]:

 ---> UL

</td></tr></table>

Die folgende Tabelle zeigt eine mögliche Spezifikation der in den Testfällen
referenzierten Basiskonfigurationen:

<table><tr><th>
Parameter

</th><th>
Auslieferungs-zustand

</th><th>
Werks-einstellung

</th><th>
LDD/WDE

</th><th>
LDD/WDD

</th><th>
LDD/WDE2

</th><th>
LDD/WDE3

</th></tr><tr><td>
LAN WAN Settings

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td></tr><tr><td>
DHCP_CLIENT_LAN_STATE=

</td><td>
Aktiviert

</td><td>
False

</td><td>
Disabled

</td><td>
Disabled

</td><td>
Disabled

</td><td>
Disabled

</td></tr><tr><td>
ANLW_LAN_IP_ADDRESS =

</td><td>
 

</td><td>
 

</td><td>
statisch

</td><td>
statisch

</td><td>
statisch

</td><td>
statisch

</td></tr><tr><td>
ANLW_LAN_SUBNETMASK=

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td></tr><tr><td>
DHCP_CLIENT_WAN_STATE=

</td><td>
Aktiviert

</td><td>
True

</td><td>
Enabled

</td><td>
Disabled

</td><td>
Enabled

</td><td>
Enabled

</td></tr><tr><td>
ANLW_WAN_IP_ADDRESS =

</td><td>
 

</td><td>
 

</td><td>
Dynamisch

</td><td>
statisch

</td><td>
Dynamisch

</td><td>
Dynamisch

</td></tr><tr><td>
ANLW_WAN_SUBNETMASK=

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
255.255.255.0

</td><td>
 

</td><td>
 

</td></tr><tr><td>
DHCP Settings

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td></tr><tr><td>
DHCP_SERVER_STATE=

</td><td>
Deaktiviert

</td><td>
Disabled

</td><td>
Disabled

</td><td>
Disabled

</td><td>
Disabled

</td><td>
Disabled

</td></tr><tr><td>
Betriebsmode

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td></tr><tr><td>
ANLW_WAN_ADAPTER_MODUS=

</td><td>
 

</td><td>
Active

</td><td>
Active

</td><td>
Active

</td><td>
Active

</td><td>
Active

</td></tr><tr><td>
ANLW_ANBINDUNGS_MODUS =

</td><td>
Read Only

</td><td>
Parallel

</td><td>
InReihe

</td><td>
InReihe

</td><td>
InReihe

</td><td>
InReihe

</td></tr><tr><td>
ANLW_INTERNET_MODUS =

</td><td>
 

</td><td>
Keiner

</td><td>
SIS

</td><td>
SIS

</td><td>
SIS

</td><td>
SIS

</td></tr><tr><td>
ANLW_INTRANET_ROUTES_MODUS=

</td><td>
 

</td><td>
Block

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td></tr><tr><td>
ANLW_LEKTR_INTRANET_ROUTES=

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td></tr><tr><td>
MGM_LU_ONLINE =

</td><td>
 

</td><td>
 

</td><td>
Enabled/True

</td><td>
Enabled/True

</td><td>
Disabled/False

</td><td>
Enabled

/true

</td></tr><tr><td>
MGM_LU_SAK=

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td></tr><tr><td>
MGM_TI_ACCESS_GRANTED=

</td><td>
Disabled

</td><td>
Enabled/True

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td></tr><tr><td>
MGM_STANDALONE_KON=

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td></tr><tr><td>
Sonstiges

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td></tr><tr><td>
LOG_LEVEL_SYSLOG=

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td></tr></table>

### 11.3 Testprotokoll

Die folgende Tabelle zeigt eine mögliche Vorlage zur Dokumentation der
Testergebnisse durch ein Testprotokoll:

<table><tr><th>
Testfall-ID

</th><th>
Testfall Name

</th><th>
Status

</th><th>
Ergebnis

</th><th>
Dokumentation

</th></tr><tr><td>
Eindeutige ID des Testfalls

</td><td>
Eindeutiger, sprechender Name des Testfalls

</td><td>
Status der Testdurchführung

</td><td>
</td><td>
</td></tr><tr><td>
…

</td><td>
…

</td><td>
…

</td><td>
…

</td><td>
…

</td></tr><tr><td>
…

</td><td>
…

</td><td>
…

</td><td>
…

</td><td>
…

</td></tr></table>

### 11.4 Tabelle umzusetzender Anforderungen

Die folgende Tabelle zeigt, in welcher Art und Weise eine Auflistung der
umgesetzten bzw. nicht umgesetzten SOLL/SOLL NICHT/KANN - Anforderungen
erwartet wird.

<table><tr><th>
Afo-ID

</th><th>
Anforderungslevel

</th><th>
Umgesetzt ja/nein

</th><th>
Begründung bei nein

</th></tr><tr><td>
</td><td>
SOLL

</td><td>
nein

</td><td>
Weil …

</td></tr><tr><td>
</td><td>
SOLL NICHT

</td><td>
ja

</td><td>
entfällt (oder leer)

</td></tr><tr><td>
</td><td>
…

</td><td>
</td><td>
</td></tr><tr><td>
</td><td>
KANN

</td><td>
</td><td>
entfällt (oder leer)

</td></tr></table>





[Dokumentinformationen]: #dokumentinformationen
[Inhaltsverzeichnis]:    #inhaltsverzeichnis
[1]:                     #1-einordnung-des-dokuments
[1.1]:                   #11-zielsetzung
[1.2]:                   #12-zielgruppe
[1.3]:                   #13-geltungsbereich
[1.4]:                   #14-abgrenzungen
[1.5]:                   #15-methodik
[2]:                     #2-allgemeine-testvorgehensweise
[2.1]:                   #21-einleitung
[2.2]:                   #22-ablauf-für-den-nachweis-der-funktionalen-eignung-innerhalb-eines-zulassungsverfahrens
[2.3]:                   #23-testspezifische-rollen
[2.3.1]:                 #231-testkoordinierende-instanz-tki
[2.3.2]:                 #232-testintegrator-zentrale-plattformdienste-tizp
[2.3.3]:                 #233-testbetriebsinstanz-tbi
[2.3.4]:                 #234-testdurchführende-instanz-tdi-referenzumgebung-ru
[2.3.5]:                 #235-testdurchführende-instanz-tdi-tu-testumgebung
[2.3.6]:                 #236-test---transitionmanager-ttm
[2.4]:                   #24-testphasen
[2.4.1]:                 #241-eigenverantwortlicher-test
[2.4.1.1]:               #2411-qualitätssichernde-maßnahmen-und-produktmuster
[2.4.2]:                 #242-zulassungstest
[2.4.2.1]:               #2421-fehlerschweregrade
[2.4.2.2]:               #2422-testabbruch
[2.5]:                   #25-testarten
[2.5.1]:                 #251-güteprüfung
[2.5.2]:                 #252-funktionstest
[2.5.3]:                 #253-interoperabilitätstest
[2.5.4]:                 #254-leistungstest
[3]:                     #3-systemumgebungen
[3.1]:                   #31-testobjekte
[3.2]:                   #32-anforderungen-an-die-systemumgebungen
[3.2.1]:                 #321-trennung-der-netzwerke
[3.2.2]:                 #322-trennung-der-vertrauensräume
[3.2.3]:                 #323-gemeinsame-eigenschaften-für-alle-systemumgebungen
[3.2.4]:                 #324-gemeinsame-eigenschaften-der-referenz--und-testumgebung
[3.2.5]:                 #325-exklusiver-zugriff
[3.2.6]:                 #326-logging
[3.2.7]:                 #327-testwerkzeuge
[3.2.8]:                 #328-test--und-referenzobjekte
[3.2.9]:                 #329-referenzumgebung
[3.2.9.1]:               #3291-qualitätssicherungsmaßnahmen-der-hersteller-und-anbieter
[3.2.9.2]:               #3292-weiterentwicklung-der-referenzumgebung
[3.2.9.3]:               #3293-nutzung-der-referenzumgebung
[3.2.9.4]:               #3294-instanzen-der-referenzumgebung
[3.2.10]:                #3210-testumgebung
[3.2.10.1]:              #32101-bestandteile-der-testumgebung
[3.2.10.2]:              #32102-weiterentwicklung-der-testumgebung
[3.2.10.3]:              #32103-dimensionierung-der-testumgebung
[3.2.10.4]:              #32104-betrieb-der-testumgebung
[3.2.10.5]:              #32105-nachstellen-von-pu-fehlern-in-tu
[4]:                     #4-szenarien
[4.1]:                   #41-einleitung
[4.2]:                   #42-testvorgehensweise-im-rahmen-der-zulassung-eines-neuen-produkts
[4.3]:                   #43-testvorgehensweise-im-rahmen-der-zulassung-eines-geänderten-produkts
[4.4]:                   #44-regressionstest
[4.5]:                   #45-teststufen
[4.5.1]:                 #451-produkttest-evt
[4.5.2]:                 #452-produktübergreifender-test-evt
[4.5.3]:                 #453-eingangsprüfung-zult
[4.5.4]:                 #454-produkttest-zult
[4.5.5]:                 #455-produktübergreifender-test-zult
[4.6]:                   #46-interoperabilität
[4.7]:                   #47-testdokumentation
[4.7.1]:                 #471-testkonzept
[4.7.2]:                 #472-testspezifikation
[4.7.3]:                 #473-release-notes
[4.7.4]:                 #474-produktdokumentation
[4.7.5]:                 #475-testprotokoll
[4.7.6]:                 #476-testbericht
[4.8]:                   #48-serviceprodukte-der-gematik-zur-testunterstützung
[5]:                     #5-fachanwendung-vsdm
[5.1]:                   #51-testkarten
[5.1.1]:                 #511-testkartenausprägungen
[5.1.2]:                 #512-testkarten-verwendung
[5.1.3]:                 #513-anforderungen-an-die-testkarten-egk
[5.2]:                   #52-flipflop-verfahren
[5.3]:                   #53-umgang-mit-mandantenfähigen-fachdiensten
[5.4]:                   #54-testdurchführung-der-evt-bei-vsdm
[6]:                     #6-fachanwendung-kom-le
[7]:                     #7-fachanwendung-adv
[8]:                     #8-fachanwendung-epa
[8.1]:                   #81-epa-aktensystem
[8.2]:                   #82-epa-frontend-des-versicherten
[8.3]:                   #83-basis-consumerktr-consumer
[8.4]:                   #84-signaturdienst
[8.5]:                   #85-schlüsselgenerierungsdienst
[9]:                     #9-weitere-anwendungen
[9.1]:                   #91-vorbereitung-der-evt-zur-funktionalen-eignung
[9.2]:                   #92-durchführung-evt-zur-funktionalen-eignung
[9.3]:                   #93-schnittstellentests-in-der-tu
[10]:                    #10-anhang-a-–-verzeichnisse
[10.1]:                  #101-abkürzungen
[10.2]:                  #102-glossar
[10.3]:                  #103-abbildungsverzeichnis
[10.4]:                  #104-tabellenverzeichnis
[10.5]:                  #105-referenzierte-dokumente
[10.5.1]:                #1051-dokumente-der-gematik
[10.5.2]:                #1052-weitere-dokumente
[11]:                    #11-anhang-b-–-beispielhafte-testdokumentation
[11.1]:                  #111-testkonzept
[11.2]:                  #112-testspezifikation
[11.3]:                  #113-testprotokoll
[11.4]:                  #114-tabelle-umzusetzender-anforderungen
[Abbildung-1]:           gemKPT_Test_V2.8.5.attachments/6934228282982786359.png
[Abbildung-2]:           gemKPT_Test_V2.8.5.attachments/10671340825804690756.png
[Abbildung-3]:           gemKPT_Test_V2.8.5.attachments/15185643499426745362.png
[Abbildung-4]:           gemKPT_Test_V2.8.5.attachments/16558115620199195873.png
[Abbildung-5]:           gemKPT_Test_V2.8.5.attachments/11860523596559346674.png
[Img-006]:               gemKPT_Test_V2.8.5.attachments/17863656545308384826.png
[Tbl-001]:               #Tbl-001 (&93834766955192)
[Tabelle-1]:             #Tabelle-1 (&93834766975632)
[Tabelle-2]:             #Tabelle-2 (&93834838623352)
[Tabelle-3]:             #Tabelle-3 (&93834765506792)
[Tabelle-4]:             #Tabelle-4 (&93834836122896)
[Tabelle-5]:             #Tabelle-5 (&93834772231128)
[Tabelle-6]:             #Tabelle-6 (&93834781701840)
[Tabelle-7]:             #Tabelle-7 (&93834812127240)
[Tabelle-8]:             #Tabelle-8 (&93834838129464)
[Tabelle-9]:             #Tabelle-9 (&93834783610352)
[Tabelle-10]:            #Tabelle-10 (&93834783626952)
[Tabelle-11]:            #Tabelle-11 (&93834783643920)
[Tabelle-12]:            #Tabelle-12 (&93834783660824)
[Tabelle-14]:            #Tabelle-14 (&93834811185184)
[Tabelle-15]:            #Tabelle-15 (&93834798967768)
[Tabelle-16]:            #Tabelle-16 (&93834767979560)
[Tabelle-17]:            #Tabelle-17 (&93834768005264)
[Tabelle-18]:            #Tabelle-18 (&93834768028640)
[Tabelle-19]:            #Tabelle-19 (&93834768779320)
[Tabelle-20]:            #Tabelle-20 (&93834789517416)
[Tabelle-21]:            #Tabelle-21 (&93834789567696)
[Tbl-022]:               #Tbl-022 (&93834800972032)
[Tbl-023]:               #Tbl-023 (&93834776369248)
[Tbl-024]:               #Tbl-024 (&93834776418024)
[Tbl-025]:               #Tbl-025 (&93834833872832)
[Tabelle-22]:            #Tabelle-22 (&93834833887320)
[Tabelle-23]:            #Tabelle-23 (&93834833918696)
[Tabelle-24]:            #Tabelle-24 (&93834781835688)
[Tabelle-25]:            #Tabelle-25 (&93834764454832)
[Tabelle-26]:            #Tabelle-26 (&93834777636120)
[Tabelle-27]:            #Tabelle-27 (&93834781066504)
[Tabelle-28]:            #Tabelle-28 (&93834776327008)
[Tabelle-29]:            #Tabelle-29 (&93834771773592)
[Tabelle-30]:            #Tabelle-30 (&93834781561552)
[Tabelle-31]:            #Tabelle-31 (&93834778308176)
[Tbl-036]:               #Tbl-036 (&93834799055976)
[https://fachportal.gematik.de/]: https://fachportal.gematik.de/ (&93834767241752)
