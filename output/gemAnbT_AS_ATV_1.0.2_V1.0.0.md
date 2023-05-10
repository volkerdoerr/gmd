
Elektronische Gesundheitskarte und Telematikinfrastruktur

### Anbietertypsteckbrief<br>Anbieter Anschlusspunkt

- Klassifizierung: öffentlich
- Produkttyp Status: freigegeben
- Produkttyp Version: 1.0.2
- Referenzierung: gemAnbT_AS_ATV_1.0.2
- Revision: 548770
- Stand: 14.02.2022
- Status: freigegeben
- Version: 1.0.0

### Historie Anbietertypversion und Anbietertypsteckbrief

Historie Anbietertypversion

Die Anbietertypversion ändert sich, wenn sich die normativen Festlegungen für
den Anbietertyp ändern.

<table><tr><th>
Anbietertypversion

</th><th>
Beschreibung der Änderung

</th><th>
Referenz

</th></tr><tr><td>
1.0.0

</td><td>
Initiale Version

</td><td>
gemAnbT_AS_ATV_1.0.0

</td></tr><tr><td>
1.0.1

</td><td>
Einarbeitung CI_Maintenance_21.2

</td><td>
gemAnbT_AS_ATV_1.0.1

</td></tr><tr><td>
1.0.2

</td><td>
Anpassung auf Releasestand Betr_Maintenance_21.3

</td><td>
gemAnbT_AS_ATV_1.0.2

</td></tr></table>

Historie Anbietertypsteckbrief

Die Dokumentenversion des Anbietertypsteckbriefs ändert sich mit jeder
inhaltlichen oder redaktionellen Änderung des Anbietertypsteckbriefs und
seinen referenzierten Dokumenten. Redaktionelle Änderungen haben keine
Auswirkung auf die Anbietertypversion.

<table><tr><th>
Version

</th><th>
Stand

</th><th>
Kap.

</th><th>
Grund der Änderung, besondere Hinweise

</th><th>
Bearbeiter

</th></tr><tr><td>
1.0.0

</td><td>
14.02.22

</td><td>
freigegeben

</td><td>
gematik

</td></tr></table>

### Inhaltsverzeichnis

- [Historie] Anbietertypversion und Anbietertypsteckbrief
- [Inhaltsverzeichnis]
- [1] Einführung
  - [1.1] Zielsetzung und Einordnung des Dokumentes
  - [1.2] Zielgruppe
  - [1.3] Geltungsbereich
  - [1.4] Abgrenzung des Dokumentes
  - [1.5] Methodik
- [2] Dokumente
- [3] Normative Festlegungen
  - [3.1] Festlegungen zur betrieblichen Eignung
    - [3.1.1] Prozessprüfung betriebliche Eignung
    - [3.1.2] Anbietererklärung betriebliche Eignung
    - [3.1.3] Betriebshandbuch betriebliche Eignung
  - [3.2] Festlegungen zur sicherheitstechnischen Eignung
    - [3.2.1] Sicherheitsgutachten
    - [3.2.2] Anbietererklärung sicherheitstechnische Eignung
- [4] Anhang A – Verzeichnisse
  - [4.1] Abkürzungen
  - [4.2] Tabellenverzeichnis
  - [4.3] Referenzierte Dokumente

### 1 Einführung

### 1.1 Zielsetzung und Einordnung des Dokumentes

Anbietertypsteckbriefe verzeichnen verbindlich die normativen Festlegungen der
gematik anAnbieter eines Anschlusspunkteszur Sicherstellung des Betriebes der
von ihnen verantworteten Serviceeinheiten.

Die normativen Festlegungen werden über ihren Identifier, ihren Titel sowie die
Dokumentenquelle referenziert. Die normativen Festlegungen mit ihrem
vollständigen, normativen Inhalt sind dem jeweils referenzierten Dokument zu
entnehmen.

Als "Weitere Anwendung" können Leistungserbringer die unterschiedlichsten
Angebote von Drittanbietern, etwa aus der Gesundheitsforschung oder Industrie,
über die Telematikinfrastruktur als primäre Plattform für eine sichere
Vernetzung nutzen. Die Voraussetzung ist ein erfolgreich durchgeführtes
Bestätigungsverfahren für WANDA, kurz für: Weitere Anwendungen für den
Datenaustausch in der Telematikinfrastruktur, das diese Dienste bei der
gematik durchlaufen und erfolgreich absolvieren müssen.

Die Anwendungen können als Option "Smart" oder "Basic" gebucht werden. "WANDA
Smart“-Nutzer können dabei auf zentrale Dienste der Telematikinfrastruktur
zugreifen oder kryptografische Identitäten der TI für eigene Anwendungszwecke
mitnutzen, wohingegen in der Anbindungsoption „WANDA Basic“ der Anschluss
an die TI ohne die Nutzung dieser Dienste möglich ist.

Die Anbieter WANDA dürfen bestehende sichere zentrale Zugangspunkte (SZZP) oder
Sicherheitsgateways (SGW) anderer Anbieter mitnutzen oder werden zusätzlich in
der Rolle "Anbieter Anschlusspunkt" innerhalb des Bestätigungsverfahrens der
Weiteren Anwendung bestätigt, wenn sie selbst den SZZP/das SGW vom "Anbieter
Zentrale Plattformdienste" bestellen und diesen nach den normativen
Festlegungen des "Anbietertypsteckbriefes Anbieter Anschlusspunkt" selbst
betreiben.Dabei ist es unerheblich, ob sie diesen Anschlusspunkt nur für sich,
gemischt für sich und andere oder auch ausschließlich für andere Anbieter
betreiben.Der Betrieb des Anschlusspunktes (SZZP/SGW) ist nicht auf die
Anwendung WANDA beschränkt. Es dürfen jedoch nur bestätigte Anwendungen oder
zugelassene Dienste daran angeschlossen werden.

Es dürfen auch über den selben Anschlusspunkt andere, durch die gematik
zugelassenen Produkte eines zugelassenen oder bestätigten Anbieters oder
Betreibers angeschlossen werden. Für jeden Anschlusspunkt ist genau ein
Anbieter Anschlusspunkt verantwortlich. Im Zuge des betrieblichen
Changemanagements und bei der Beantragung der Freischaltungen werden diese
Rahmenbedingungen sichergestellt.

Die Anbieter WANDA Basic, WANDA Smart, WANDA Smart Hosting und Anbieter
Anschlusspunkt sind im TI-ITSM vertreten.

### 1.2 Zielgruppe

Der Anbietertypsteckbrief richtet sich an:

 ---> UL

### 1.3 Geltungsbereich

Dieses Dokument enthält normative Festlegungen zur Telematikinfrastruktur des
deutschen Gesundheitswesens. Der Gültigkeitszeitraum der vorliegenden Version
und deren Anwendung in Zulassungsverfahren werden durch die gematik GmbH in
gesonderten Dokumenten (z.B. PTV_ATV_Festlegungen) festgelegt und bekannt
gegeben.

### 1.4 Abgrenzung des Dokumentes

Dieses Dokument macht keine Aussagen zur Aufteilung der Produktentwicklung bzw.
Produktherstellung auf verschiedene Hersteller und Anbieter.

Dokumente zu den Zulassungsverfahren für den Produkttyp sind nicht aufgeführt.
Die geltenden Verfahren und Regelungen zur Beantragung und Durchführung von
Zulassungsverfahren können der Homepage der gematik entnommen werden.

### 1.5 Methodik

Die im Dokument verzeichneten normativen Festlegungen werden tabellarisch
dargestellt. Die Tabellenspalten haben die folgende Bedeutung:

ID:Identifiziert die normative Festlegung eindeutig im Gesamtbestand aller
Festlegungen der gematik.

Bezeichnung:Gibt den Titel einer normativen Festlegung informativ wieder, um die
thematische Einordnung zu erleichtern. Der vollständige Inhalt der normativen
Festlegung ist dem Dokument zu entnehmen, auf das die Quellenangabe verweist.

Quelle (Referenz):Verweist auf das Dokument, das die normative Festlegung
definiert.

### 2 Dokumente

Die nachfolgenden Dokumente enthalten alle für den Anbietertyp normativen
Festlegungen.

<table><tr><th>
Dokumentenkürzel

</th><th>
Bezeichnung des Dokumentes

</th><th>
Version

</th></tr><tr><td>
gemSpec_Net

</td><td>
Übergreifende Spezifikation Netzwerk

</td><td>
1.21.0

</td></tr><tr><td>
gemKPT_Betr

</td><td>
Betriebskonzept Online-Produktivbetrieb

</td><td>
3.13.0

</td></tr><tr><td>
gemSpec_DS_Anbieter

</td><td>
Spezifikation Datenschutz- und Sicherheitsanforderungen der TI an Anbieter

</td><td>
1.4.0

</td></tr><tr><td>
gemRL_Betr_TI

</td><td>
Übergreifende Richtlinien zum Betrieb der TI

</td><td>
2.6.0

</td></tr></table>

### 3 Normative Festlegungen

Die folgenden Abschnitte verzeichnen alle für den Anbietertypen normativen
Festlegungen der gematik an Anbieter einesAnschlusspunkteszur Sicherstellung
des Betriebes der von ihnen verantworteten Serviceeinheiten. Die Festlegungen
sind gruppiert nach der Art der Nachweisführung ihrer Erfüllung als Grundlage
der Zulassung.

### 3.1 Festlegungen zur betrieblichen Eignung

### 3.1.1 Prozessprüfung betriebliche Eignung

Sofern in diesem Abschnitt Festlegungen mit Vorgaben zu organisatorischen
Maßnahmen wie Prozessen und Strukturvorgaben verzeichnet sind, muss deren
Erfüllung im Rahmen von Prozessprüfungen nachgewiesen werden.

<table><tr><th>
ID

</th><th>
Bezeichnung

</th><th>
Quelle (Referenz)

</th></tr></table>

### 3.1.2 Anbietererklärung betriebliche Eignung

Sofern in diesem Abschnitt Festlegungen mit Vorgaben zu organisatorischen
Maßnahmen wie Prozessen und Strukturvorgaben der Aufbauorganisation sowie der
Umgebung verzeichnet sind, muss der Anbieter deren Umsetzung und Beachtung
durch eine Anbietererklärung bestätigen bzw. zusagen.

<table><tr><th>
ID

</th><th>
Bezeichnung

</th><th>
Quelle (Referenz)

</th></tr><tr><td>
A_13573-01

</td><td>
Serviceleistung der TI-ITSM-Teilnehmer im TI-ITSM-Teilnehmersupport zur Hauptzeit

</td><td>
gemKPT_Betr

</td></tr><tr><td>
TIP1-A_6389-02

</td><td>
Erreichbarkeit der 1st-Level (UHD), 2nd-Level (SPOCs) der Anbieter

</td><td>
gemKPT_Betr

</td></tr><tr><td>
TIP1-A_6390-02

</td><td>
Mitwirkung im TI-ITSM durch Anbieter

</td><td>
gemKPT_Betr

</td></tr><tr><td>
TIP1-A_6393-02

</td><td>
Verantwortung für die Weiterleitung von Anfragen

</td><td>
gemKPT_Betr

</td></tr><tr><td>
TIP1-A_7261

</td><td>
Erreichbarkeit der TI-ITSM-Teilnehmer untereinander

</td><td>
gemKPT_Betr

</td></tr><tr><td>
TIP1-A_7266

</td><td>
Mitwirkungspflichten im TI-ITSM-System

</td><td>
gemKPT_Betr

</td></tr><tr><td>
A_18403

</td><td>
Erstellung einer Root Cause Analysis im Incident - Prio 1

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
A_18404

</td><td>
Erstellung einer Root Cause Analysis im Incident - Prio 2 bis 4

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
A_18405

</td><td>
Erstellung einer Root Cause Analysis durch am Incident beteiligte
TI-ITSM-Teilnehmer

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
A_18406

</td><td>
Nachlieferung zu einer Root Cause Analysis

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
A_18407

</td><td>
Unterstützung bei Change-Verifikation

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_3876

</td><td>
Prüfung auf übergreifenden Incident

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_3884

</td><td>
Festlegung von Dringlichkeit und Auswirkung von übergreifenden Incidents

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_3886-01

</td><td>
Nutzung des TI-ITSM-Systems bei der Übermittlung eines übergreifenden Vorgangs

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_3888

</td><td>
Verifikation vor Schließung eines übergreifenden Incident

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_3889

</td><td>
Schließung eines übergreifenden Incidents

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_3902

</td><td>
Prüfung auf Serviceverantwortung

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_3904

</td><td>
Annahme eines übergreifenden Incidents

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_3905

</td><td>
Ablehnung eines übergreifenden Incidents

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_3907

</td><td>
Lösung von übergreifenden Incidents

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_3917

</td><td>
Bereitstellung der ITSM-Dokumentation bei Audits

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_3920

</td><td>
Eskalationseinleitung durch den TI-ITSM-Teilnehmer

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_3922

</td><td>
Mitwirkung bei Taskforces

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_3958

</td><td>
Problemerkennung durch TI-ITSM-Teilnehmer

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_3959

</td><td>
Prüfung auf übergreifendes Problem

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_3964

</td><td>
Festlegung von Dringlichkeit und Auswirkung von übergreifenden Problems

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_3971

</td><td>
Verifikation vor Schließung eines übergreifenden Problems

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_3975

</td><td>
Prüfung auf Serviceverantwortung zum übergreifenden Problem

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_3976

</td><td>
Ablehnung der Lösungsunterstützung

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_3977

</td><td>
Annahme der Verantwortung zur Lösungsunterstützung

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_3981

</td><td>
Annahme eines übergreifenden Problems

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_3982

</td><td>
Ablehnung eines übergreifenden Problems

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_3983

</td><td>
Ursachenanalyse eines übergreifenden Problems durch Serviceverantwortlichen

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_3984

</td><td>
Service Request zur Bereitstellung der TI-Testumgebung (RU/TU)

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_3986

</td><td>
Koordination bei übergreifenden Problems

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_3987

</td><td>
Initiierung eines Change Request

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_3988

</td><td>
Prüfung der Lösung durch den Melder eines übergreifenden Problems

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_3989

</td><td>
Ablehnung der Lösung eines übergreifenden Problems

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_3990

</td><td>
Schließung eines übergreifenden Problems

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_4085

</td><td>
Etablierung von Kommunikationsschnittstellen durch die TI-ITSM-Teilnehmer

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_4086

</td><td>
Erreichbarkeit der Kommunikationsschnittstellen

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_4088-01

</td><td>
Benennung von Ansprechpartnern

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_4090

</td><td>
Kommunikationssprache

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_4095

</td><td>
Übermittlung von Ad-hoc-Reports

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_4100

</td><td>
Messung der Service Level

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_4101

</td><td>
Übermittlung der Service Level Messergebnisse

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_4121

</td><td>
Analyse Auswirkungen möglicher Schadensereignisse auf Sicherheit und Funktion
der TI-Services

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_4123

</td><td>
Entwicklung und Pflege der TI-Notfallvorsorgedokumentation

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_4124

</td><td>
Umsetzung Vorkehrungen zur TI-Notfallvorsorge

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_4125

</td><td>
TI-Notfallerkennung

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_4126

</td><td>
Eskalation TI-Notfälle

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_4127

</td><td>
Sofortmaßnahmen TI-Notfälle

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_4128

</td><td>
Bewältigung der TI-Notfälle

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_4129

</td><td>
Unterstützung bei TI-Notfällen

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_4130

</td><td>
Festlegung der Schnittstellen des EMC

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_4132

</td><td>
Durchführung der Wiederherstellung und TI-Notfällen

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_4134

</td><td>
Auswertungen von TI-Notfällen

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_4136

</td><td>
Statusinformation bei TI-Notfällen

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_4137

</td><td>
Dokumentation im TI-Notfall-Logbuch

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_4138

</td><td>
Erstellung des Wiederherstellungsberichts nach TI-Notfällen

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_4397

</td><td>
Teilnahme am Service Review

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_4855-02

</td><td>
Auditierung von TI-ITSM-Teilnehmern

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_5250

</td><td>
Ablehnung der Lösung eines übergreifenden Incidents

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_5343

</td><td>
Definition inhaltlicher Auszüge aus dem Betriebshandbuch

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_5377

</td><td>
Durchführung einer Problemstornierung

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_5400

</td><td>
Prüfung der Lösung durch den Melder eines übergreifenden Incidents

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_5401

</td><td>
Verschlüsselte E-Mail-Kommunikation

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_5402

</td><td>
Eigenverantwortliches Handeln bei Ausfall von Kommunikationsschnittstellen

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_5449

</td><td>
Typisierung eines übergreifenden Incidents als „sicherheitsrelevant“

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_5450

</td><td>
Typisierung eines übergreifenden Incidents als „datenschutzrelevant“

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_5587

</td><td>
Ablehnung der Lösungsunterstützung bei einem übergreifenden Incident

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_5588

</td><td>
Abbruch der Problembearbeitung

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_5589

</td><td>
Prüfung auf Verantwortung zur Lösungsunterstützung

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_5603

</td><td>
Eingangskanal für Informationen von TI-ITSM-Teilnehmern

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_5604

</td><td>
Bewertung der Messergebnisse

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_5606

</td><td>
Unterstützung bei Definition von Kapazitätsanforderungen

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_5608

</td><td>
Übermittlung von CSV-Dateien

</td><td>
gemRL_Betr_TI

</td></tr><tr><td>
GS-A_3753-01

</td><td>
Notfallkonzept

</td><td>
gemSpec_DS_Anbieter

</td></tr><tr><td>
GS-A_3772-01

</td><td>
Notfallkonzept: Der Dienstanbieter soll dem BSI-Standard 100-4 folgen

</td><td>
gemSpec_DS_Anbieter

</td></tr><tr><td>
GS-A_4980-01

</td><td>
Umsetzung der Norm ISO/IEC 27001

</td><td>
gemSpec_DS_Anbieter

</td></tr><tr><td>
GS-A_4981-01

</td><td>
Erreichen der Ziele der Norm ISO/IEC 27001 Annex A

</td><td>
gemSpec_DS_Anbieter

</td></tr><tr><td>
GS-A_4982-01

</td><td>
Umsetzung der Maßnahmen der Norm ISO/IEC 27002

</td><td>
gemSpec_DS_Anbieter

</td></tr><tr><td>
GS-A_4983-01

</td><td>
Umsetzung der Maßnahmen aus dem BSI-Grundschutz

</td><td>
gemSpec_DS_Anbieter

</td></tr><tr><td>
A_21142

</td><td>
SZZP mit mehreren Produktinstanzen

</td><td>
gemSpec_Net

</td></tr><tr><td>
GS-A_4024-01

</td><td>
Nutzung IP-Adressbereiche

</td><td>
gemSpec_Net

</td></tr><tr><td>
GS-A_4759-01

</td><td>
IPv4-Adressen Produkttyp zum SZZP

</td><td>
gemSpec_Net

</td></tr><tr><td>
GS-A_4760-01

</td><td>
IP-Adressbereiche Bestandsnetze und Anbieter von WANDA

</td><td>
gemSpec_Net

</td></tr><tr><td>
GS-A_4805

</td><td>
Abstimmung angeschlossener Produkttyp mit dem Anbieter Zentrales Netz

</td><td>
gemSpec_Net

</td></tr><tr><td>
GS-A_4832

</td><td>
Path MTU Discovery und ICMP Response

</td><td>
gemSpec_Net

</td></tr><tr><td>
GS-A_5584-01

</td><td>
Meldung Anbieter eines an die TI angeschlossenen Netzes des Gesundheitswesens
mit WANDA Basic zu Netzwerkinformationen

</td><td>
gemSpec_Net

</td></tr><tr><td>
GS-A_5585

</td><td>
Meldung Anbieter eines an die TI angeschlossenen Netzes des Gesundheitswesens
mit WANDA Basic zu Policy-Informationen

</td><td>
gemSpec_Net

</td></tr></table>

### 3.1.3 Betriebshandbuch betriebliche Eignung

Sofern in diesem Abschnitt Festlegungen mit Vorgaben zu organisatorischen
Maßnahmen wie Prozessen und Strukturvorgaben der Aufbauorganisation sowie der
Umgebung verzeichnet sind, muss der Anbieter deren Umsetzung und Beachtung
durch die Vorlage des Betriebshandbuches nachweisen.  

Der Umfang und Inhalt des Betriebshandbuches ist der Definitionin der Richtlinie
Betrieb [gemRL_Betr_TI] zu entnehmen.

<table><tr><th>
ID

</th><th>
Bezeichnung

</th><th>
Quelle (Referenz)

</th></tr><tr><td>
GS-A_5586

</td><td>
Meldung Anbieter eines an die TI angeschlossenen Netzes des Gesundheitswesens
mit WANDA zur technischen Anschlussvariante

</td><td>
gemSpec_Net

</td></tr></table>

### 3.2 Festlegungen zur sicherheitstechnischen Eignung

### 3.2.1 Sicherheitsgutachten

Die in diesem Abschnitt verzeichneten Festlegungen sind Gegenstand der Prüfung
der Sicherheitseignung gemäß [gemRL_PruefSichEig]. Das entsprechende
Sicherheitsgutachten ist der gematik vorzulegen.

<table><tr><th>
ID

</th><th>
Bezeichnung

</th><th>
Quelle (Referenz)

</th></tr></table>

### 3.2.2 Anbietererklärung sicherheitstechnische Eignung

In diesem Abschnitt sind alle Festlegungen an das BestätigungsobjektWeitere
Anwendungverzeichnet, deren Erfüllung der Anbieter zum Nachweis der
sicherheitstechnischen Eignung durch eine Erklärung belegt.

<table><tr><th>
ID

</th><th>
Bezeichnung

</th><th>
Quelle (Referenz)

</th></tr><tr><td>
A_19174

</td><td>
Bereitstellung Übersicht Internet-Schnittstellen der TI

</td><td>
gemSpec_DS_Anbieter

</td></tr><tr><td>
A_19175

</td><td>
Zustimmung zu regelmäßigen Schwachstellenscans durch die gematik

</td><td>
gemSpec_DS_Anbieter

</td></tr><tr><td>
GS-A_5551

</td><td>
Betriebsumgebung in einem Mitgliedstaat der EU bzw. des EWR

</td><td>
gemSpec_DS_Anbieter

</td></tr></table>

### 4 Anhang A – Verzeichnisse

### 4.1 Abkürzungen

<table><tr><th>
Kürzel

</th><th>
Erläuterung

</th></tr><tr><td>
ID

</td><td>
Identifikation

</td></tr></table>

### 4.2 Tabellenverzeichnis

- [Tabelle-1] - Dokumente mit Festlegungen zu der Anbietertypversion
- [Tabelle-2] - Festlegungen zur betrieblichen Eignung "Prozessprüfung"
- [Tabelle-3] - Festlegungen zur betrieblichen Eignung "Anbietererklärung"
- [Tabelle-4] - Festlegungen zur betrieblichen Eignung "Betriebshandbuch"
- [Tabelle-5] - Festlegungen zur sicherheitstechnischen Eignung "Sicherheitsgutachten"
- [Tabelle-6] - Festlegungen zur sicherheitstechnischen Eignung "Anbietererklärung"

### 4.3 Referenzierte Dokumente

Neben den in Kapitel 2 angeführten Dokumenten werden referenziert:

<table><tr><th>
[Quelle]

</th><th>
Herausgeber: Titel, Version

</th></tr><tr><td>
[gemRL_PruefSichEig]

</td><td>
gematik: Richtlinie zur Prüfung der Sicherheitseignung

</td></tr></table>

**ML-126533 - gemAnbT_AS_ATV_1.0.2** **[\<=]**





[Historie]:              #historie-anbietertypversion-und-anbietertypsteckbrief
[Inhaltsverzeichnis]:    #inhaltsverzeichnis
[1]:                     #1-einführung
[1.1]:                   #11-zielsetzung-und-einordnung-des-dokumentes
[1.2]:                   #12-zielgruppe
[1.3]:                   #13-geltungsbereich
[1.4]:                   #14-abgrenzung-des-dokumentes
[1.5]:                   #15-methodik
[2]:                     #2-dokumente
[3]:                     #3-normative-festlegungen
[3.1]:                   #31-festlegungen-zur-betrieblichen-eignung
[3.1.1]:                 #311-prozessprüfung-betriebliche-eignung
[3.1.2]:                 #312-anbietererklärung-betriebliche-eignung
[3.1.3]:                 #313-betriebshandbuch-betriebliche-eignung
[3.2]:                   #32-festlegungen-zur-sicherheitstechnischen-eignung
[3.2.1]:                 #321-sicherheitsgutachten
[3.2.2]:                 #322-anbietererklärung-sicherheitstechnische-eignung
[4]:                     #4-anhang-a-–-verzeichnisse
[4.1]:                   #41-abkürzungen
[4.2]:                   #42-tabellenverzeichnis
[4.3]:                   #43-referenzierte-dokumente
[Tbl-001]:               #Tbl-001 (&93834783685168)
[Tbl-002]:               #Tbl-002 (&93834783698800)
[Tabelle-1]:             #Tabelle-1 (&93834785382736)
[Tabelle-2]:             #Tabelle-2 (&93834785405248)
[Tabelle-3]:             #Tabelle-3 (&93834785414912)
[Tabelle-4]:             #Tabelle-4 (&93834781720408)
[Tabelle-5]:             #Tabelle-5 (&93834767982880)
[Tabelle-6]:             #Tabelle-6 (&93834767994336)
[Tbl-009]:               #Tbl-009 (&93834768009288)
[Tbl-010]:               #Tbl-010 (&93834768025072)
[gemSpec_Net]:           ../gemSpec_Net/gemSpec_Net_V1.21.0.html (&93834785387368)
[gemKPT_Betr]:           ../gemKPT_Betr/gemKPT_Betr_V3.13.0.html (&93834785389952)
[gemSpec_DS_Anbieter]:   ../gemSpec_DS_Anbieter/gemSpec_DS_Anbieter_V1.4.0.html (&93834785392536)
[gemRL_Betr_TI]:         ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html (&93834785395120)
[A_13573-01]:            ../gemKPT_Betr/gemKPT_Betr_V3.13.0.html#A_13573-01 (&93834785419544)
[TIP1-A_6389-02]:        ../gemKPT_Betr/gemKPT_Betr_V3.13.0.html#TIP1-A_6389-02 (&93834785422128)
[TIP1-A_6390-02]:        ../gemKPT_Betr/gemKPT_Betr_V3.13.0.html#TIP1-A_6390-02 (&93834785424712)
[TIP1-A_6393-02]:        ../gemKPT_Betr/gemKPT_Betr_V3.13.0.html#TIP1-A_6393-02 (&93834785427296)
[TIP1-A_7261]:           ../gemKPT_Betr/gemKPT_Betr_V3.13.0.html#TIP1-A_7261 (&93834785429880)
[TIP1-A_7266]:           ../gemKPT_Betr/gemKPT_Betr_V3.13.0.html#TIP1-A_7266 (&93834785432464)
[A_18403]:               ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#A_18403 (&93834785435048)
[A_18404]:               ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#A_18404 (&93834785437632)
[A_18405]:               ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#A_18405 (&93834785440216)
[A_18406]:               ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#A_18406 (&93834770980032)
[A_18407]:               ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#A_18407 (&93834770982616)
[GS-A_3876]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_3876 (&93834770985200)
[GS-A_3884]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_3884 (&93834770987784)
[GS-A_3886-01]:          ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_3886-01 (&93834770990368)
[GS-A_3888]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_3888 (&93834770992952)
[GS-A_3889]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_3889 (&93834770995536)
[GS-A_3902]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_3902 (&93834770998120)
[GS-A_3904]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_3904 (&93834771000704)
[GS-A_3905]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_3905 (&93834771003288)
[GS-A_3907]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_3907 (&93834771005872)
[GS-A_3917]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_3917 (&93834771008456)
[GS-A_3920]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_3920 (&93834771011072)
[GS-A_3922]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_3922 (&93834771013656)
[GS-A_3958]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_3958 (&93834771016240)
[GS-A_3959]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_3959 (&93834771018824)
[GS-A_3964]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_3964 (&93834771021408)
[GS-A_3971]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_3971 (&93834771023992)
[GS-A_3975]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_3975 (&93834771026576)
[GS-A_3976]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_3976 (&93834771029160)
[GS-A_3977]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_3977 (&93834771031744)
[GS-A_3981]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_3981 (&93834771034328)
[GS-A_3982]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_3982 (&93834771036912)
[GS-A_3983]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_3983 (&93834771039496)
[GS-A_3984]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_3984 (&93834771042080)
[GS-A_3986]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_3986 (&93834783608488)
[GS-A_3987]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_3987 (&93834783611072)
[GS-A_3988]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_3988 (&93834783613656)
[GS-A_3989]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_3989 (&93834783616240)
[GS-A_3990]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_3990 (&93834783618824)
[GS-A_4085]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_4085 (&93834783621408)
[GS-A_4086]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_4086 (&93834783623992)
[GS-A_4088-01]:          ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_4088-01 (&93834783626576)
[GS-A_4090]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_4090 (&93834783629160)
[GS-A_4095]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_4095 (&93834783631744)
[GS-A_4100]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_4100 (&93834783634328)
[GS-A_4101]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_4101 (&93834783636912)
[GS-A_4121]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_4121 (&93834783639496)
[GS-A_4123]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_4123 (&93834783642112)
[GS-A_4124]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_4124 (&93834783644696)
[GS-A_4125]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_4125 (&93834783647280)
[GS-A_4126]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_4126 (&93834783649864)
[GS-A_4127]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_4127 (&93834783652448)
[GS-A_4128]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_4128 (&93834783655032)
[GS-A_4129]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_4129 (&93834783657616)
[GS-A_4130]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_4130 (&93834783660200)
[GS-A_4132]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_4132 (&93834783662784)
[GS-A_4134]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_4134 (&93834783665368)
[GS-A_4136]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_4136 (&93834783667952)
[GS-A_4137]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_4137 (&93834783670536)
[GS-A_4138]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_4138 (&93834781663552)
[GS-A_4397]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_4397 (&93834781666136)
[GS-A_4855-02]:          ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_4855-02 (&93834781668720)
[GS-A_5250]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_5250 (&93834781671304)
[GS-A_5343]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_5343 (&93834781673888)
[GS-A_5377]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_5377 (&93834781676472)
[GS-A_5400]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_5400 (&93834781679056)
[GS-A_5401]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_5401 (&93834781681640)
[GS-A_5402]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_5402 (&93834781684224)
[GS-A_5449]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_5449 (&93834781686808)
[GS-A_5450]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_5450 (&93834781689392)
[GS-A_5587]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_5587 (&93834781691976)
[GS-A_5588]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_5588 (&93834781694560)
[GS-A_5589]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_5589 (&93834784309816)
[GS-A_5603]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_5603 (&93834784312400)
[GS-A_5604]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_5604 (&93834784314984)
[GS-A_5606]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_5606 (&93834784317568)
[GS-A_5608]:             ../gemRL_Betr_TI/gemRL_Betr_TI_V2.6.0.html#GS-A_5608 (&93834784320152)
[GS-A_3753-01]:          ../gemSpec_DS_Anbieter/gemSpec_DS_Anbieter_V1.4.0.html#GS-A_3753-01 (&93834784322736)
[GS-A_3772-01]:          ../gemSpec_DS_Anbieter/gemSpec_DS_Anbieter_V1.4.0.html#GS-A_3772-01 (&93834784325320)
[GS-A_4980-01]:          ../gemSpec_DS_Anbieter/gemSpec_DS_Anbieter_V1.4.0.html#GS-A_4980-01 (&93834784327904)
[GS-A_4981-01]:          ../gemSpec_DS_Anbieter/gemSpec_DS_Anbieter_V1.4.0.html#GS-A_4981-01 (&93834784330488)
[GS-A_4982-01]:          ../gemSpec_DS_Anbieter/gemSpec_DS_Anbieter_V1.4.0.html#GS-A_4982-01 (&93834784333072)
[GS-A_4983-01]:          ../gemSpec_DS_Anbieter/gemSpec_DS_Anbieter_V1.4.0.html#GS-A_4983-01 (&93834784335656)
[A_21142]:               ../gemSpec_Net/gemSpec_Net_V1.21.0.html#A_21142 (&93834784338240)
[GS-A_4024-01]:          ../gemSpec_Net/gemSpec_Net_V1.21.0.html#GS-A_4024-01 (&93834784340824)
[GS-A_4759-01]:          ../gemSpec_Net/gemSpec_Net_V1.21.0.html#GS-A_4759-01 (&93834781698080)
[GS-A_4760-01]:          ../gemSpec_Net/gemSpec_Net_V1.21.0.html#GS-A_4760-01 (&93834781700664)
[GS-A_4805]:             ../gemSpec_Net/gemSpec_Net_V1.21.0.html#GS-A_4805 (&93834781703248)
[GS-A_4832]:             ../gemSpec_Net/gemSpec_Net_V1.21.0.html#GS-A_4832 (&93834781705832)
[GS-A_5584-01]:          ../gemSpec_Net/gemSpec_Net_V1.21.0.html#GS-A_5584-01 (&93834781708416)
[GS-A_5585]:             ../gemSpec_Net/gemSpec_Net_V1.21.0.html#GS-A_5585 (&93834781711000)
[GS-A_5586]:             ../gemSpec_Net/gemSpec_Net_V1.21.0.html#GS-A_5586 (&93834781725040)
[A_19174]:               ../gemSpec_DS_Anbieter/gemSpec_DS_Anbieter_V1.4.0.html#A_19174 (&93834767998968)
[A_19175]:               ../gemSpec_DS_Anbieter/gemSpec_DS_Anbieter_V1.4.0.html#A_19175 (&93834768001552)
[GS-A_5551]:             ../gemSpec_DS_Anbieter/gemSpec_DS_Anbieter_V1.4.0.html#GS-A_5551 (&93834768004136)
