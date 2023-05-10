
Elektronische Gesundheitskarte und Telematikinfrastruktur

### Betriebskonzept<br>Online-Produktivbetrieb

- Klassifizierung: öffentlich
- Referenzierung: gemKPT_Betr_V.3.11.0
- Revision: 408373
- Stand: 01.10.2021
- Status: freigegeben
- Version: 3.11.0

### Dokumentinformationen

Änderungen zur Vorversion

Anpassungen des vorliegenden Dokumentes im Vergleich zur Vorversion können Sie
der nachfolgenden Tabelle entnehmen.

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
3.0.0

</td><td>
14.05.18

</td><td>
freigegeben

</td><td>
gematik

</td></tr><tr><td>
3.0.1

</td><td>
24.08.18

</td><td>
Korrektur der Übertragung der bekannten Änderung (redaktionell)

</td><td>
gematik

</td></tr><tr><td>
3.1.0

</td><td>
26.10.18

</td><td>
Anpassung aufgrund P15.9 und P15.10

</td><td>
gematik

</td></tr><tr><td>
3.2.0

</td><td>
18.12.18

</td><td>
3.2

</td><td>
Ergänzung Anbieter-Konstellationen und ePA-Inhalte

</td><td>
gematik

</td></tr><tr><td>
3.3.0

</td><td>
15.05.19

</td><td>
KTR- und Basis-Consumer hinzugefügt

</td><td>
gematik

</td></tr><tr><td>
3.4.0

</td><td>
28.06.19

</td><td>
Einarbeitung P19.1

</td><td>
gematik

</td></tr><tr><td>
3.5.0

</td><td>
02.10.19

</td><td>
Einarbeitung P16.1/P20.1

</td><td>
gematik

</td></tr><tr><td>
3.6.0

</td><td>
02.03.20

</td><td>
Einarbeitung P21.1

</td><td>
gematik

</td></tr><tr><td>
3.7.0

</td><td>
30.06.20

</td><td>
Anpassungen gemäß Änderungsliste P22.1 und Scope-Themen aus Systemdesign
R4.0.0

</td><td>
gematik

</td></tr><tr><td>
3.8.0

</td><td>
12.11.20

</td><td>
Einarbeitung P22.2

</td><td>
gematik

</td></tr><tr><td>
3.9.0

</td><td>
18.03.21

</td><td>
Einarbeitung Betr_Maintenance_21.1

</td><td>
gematik

</td></tr><tr><td>
3.10.0

</td><td>
14.06.21

</td><td>
Einarbeitung IdP_Maintenance_21.1

</td><td>
gematik

</td></tr><tr><td>
3.11.0

</td><td>
01.10.21

</td><td>
Einarbeitung TI-Messenger 1.0.0

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
  - [1.4] Abgrenzung des Dokuments
  - [1.5] Methodik
    - [1.5.1] Anforderungen
- [2] Grundlagen des Betriebs
  - [2.1] Gegenstand des Betriebskonzepts
  - [2.2] Begriffserläuterungen
    - [2.2.1] Business-Servicekatalog
    - [2.2.2] Technischer Kennzahlenkatalog
    - [2.2.3] Konfigurationen von Produkten
    - [2.2.4] Organisatorische Service Level
    - [2.2.5] Unterstützungsleistungen aller TI-ITSM-Teilnehmer
    - [2.2.6] Service-Verzeichnis
- [3] Servicekonzept
  - [3.1] Übergreifendes IT-Service-Management der TI
  - [3.2] Rollen
    - [3.2.1] Begriffserläuterungen
      - [3.2.1.1] Servicenehmer
    - [3.2.2] TI-Service
    - [3.2.3] TI-ITSM-Teilnehmer
      - [3.2.3.1] Anbieterkonstellationen
    - [3.2.4] DVO
    - [3.2.5] Gesamtverantwortlicher TI (GTI)
    - [3.2.6] Serviceverantwortung (SV) der TI-ITSM-Teilnehmer
    - [3.2.7] Anbieter
    - [3.2.8] Betreiber
    - [3.2.9] Hersteller dezentraler Produkte
    - [3.2.10] Hersteller zentraler Produkte
    - [3.2.11] gematik-Test in der TU
    - [3.2.12] Anwender
    - [3.2.13] Versicherte
    - [3.2.14] Anbieter VPN-ZugD
    - [3.2.15] User Help Desk (UHD)
    - [3.2.16] Versicherten Help Desk (VHD)
    - [3.2.17] Anbieter ePA-Aktensystem
    - [3.2.18] Anbieter Service Monitoring
    - [3.2.19] Anbieter Basis-Consumer
    - [3.2.20] Anbieter KTR-Consumer
    - [3.2.21] Anbieter KTR-AdV
    - [3.2.22] Anbieter KOM-LE
    - [3.2.23] Anbieter Anschlusspunkt am SGW
    - [3.2.24] Anbieter TI-Messenger
  - [3.3] Servicemodell
    - [3.3.1] Servicekomponenten
    - [3.3.2] Servicezerlegung
      - [3.3.2.1] Legende
    - [3.3.3] Mitwirkungsverpflichtung im TI-ITSM gemäß [gemRL_Betr_TI]
      - [3.3.3.1] Legende
  - [3.4] Supportkonzept
    - [3.4.1] Begriffserläuterungen
    - [3.4.2] Single-Point-of-Contact (SPOC) für TI-ITSM-Teilnehmer
- [4] Verantwortlichkeiten und Leistungen TI-ITSM-Teilnehmer
  - [4.1] Begriffserläuterungen
    - [4.1.1] Anbietertypsteckbrief
  - [4.2] Allgemeine Anforderungen
    - [4.2.1] Allgemeine Anforderungen für TI-ITSM-Teilnehmer
    - [4.2.2] Allgemeine Anforderungen nur für Anbieter von Diensten
  - [4.3] Service Level (vorgangsübergreifend)
    - [4.3.1] Begriffserläuterungen
      - [4.3.1.1] Quantil / Erfüllungsgrad
      - [4.3.1.2] Reaktionszeit
      - [4.3.1.3] Lösungszeit
      - [4.3.1.4] Verifikationsfrist
    - [4.3.2] Incident Management
    - [4.3.3] Reporting
    - [4.3.4] Datenaufbewahrung
- [5] Übergreifende Regelungen für betriebliche Kennzahlen für mobile Anwendungen (apps)
- [6] Anhang A – Performance-Kenngrößen
- [7] Anhang B – Verzeichnisse
  - [7.1] Abkürzungen
  - [7.2] Glossar
  - [7.3] Abbildungsverzeichnis
  - [7.4] Tabellenverzeichnis
  - [7.5] Referenzierte Dokumente
    - [7.5.1] Dokumente der gematik
    - [7.5.2] Weitere Dokumente

### 1 Einordnung des Dokumentes

### 1.1 Zielsetzung

Das Betriebskonzept legt die Servicearchitektur, Rollen des Betriebs, das
Supportkonzept, Service Level und die Leistungen der Teilnehmer der
Telematikinfrastruktur (TI) fest.

### 1.2 Zielgruppe

Das Dokument richtet sich an die am Betrieb der TI beteiligten Akteure: Anbieter
von Betriebsleistungen in der TI (verkürzt hier Anbieter genannt) und die
gematik in ihrer koordinierenden Rolle.

### 1.3 Geltungsbereich

Dieses Dokument trifft normative Festlegungen zur Telematikinfrastruktur des
deutschen Gesundheitswesens. Der Gültigkeitszeitraum der vorliegenden Version
und die Anwendung der in ihr getroffenen Festlegungen in Zulassungsverfahren
werden durch die gematik in gesonderten Dokumenten (z.B. Dokumentenlandkarte,
Produkttypsteckbrief, Leistungsbeschreibung) festgelegt und bekannt gegeben.

### 1.4 Abgrenzung des Dokuments

Die technischen Leistungsvorgaben bzw. Servicequalitäten die dieses Dokument
beschreibt, werden ergänzt durch die

 ---> UL

Normative Vorgaben zu Themen wie z. B. Zulassung, Test/Testbetrieb oder die
Inbetriebnahme sind nicht Bestandteil dieses Dokumentes.

### 1.5 Methodik

### 1.5.1 Anforderungen

Anforderungen als Ausdruck normativer Festlegungen werden durch eine eindeutige
ID sowie die dem RFC 2119 [RFC2119] entsprechenden, in Großbuchstaben
geschriebenen deutschen Schlüsselworte MUSS, DARF NICHT, SOLL, SOLL NICHT,
KANN gekennzeichnet.

Anforderungen werden im Dokument wie folgt dargestellt:

\<AFO-ID\> - \<Titel der Afo\>Text / Beschreibung [\<=]

Dabei umfasst die Anforderung sämtlichezwischen Afo-ID und Textmarke
[\<=] angeführten Inhalte.

### 2 Grundlagen des Betriebs

### 2.1 Gegenstand des Betriebskonzepts

Das Betriebskonzept beschreibt die Servicearchitektur
(Servicekonzept/Supportkonzept) sowie die daraus resultierenden
Verantwortlichkeiten und Aufgaben für die betrieblichen Rollen

### 2.2 Begriffserläuterungen

### 2.2.1 Business-Servicekatalog

Der Business-Servicekatalog enthält alle von einem TI-ITSM-Teilnehmer
angebotenen Services mit Angabe der dazugehörenden Servicekomponenten. Es wird
dargestellt, zu welchen Konditionen der jeweilige Service geliefert wird. Der
Business-Servicekatalog wird im Rahmen des Service-Katalog-Managements
vereinbart und anderen TI-ITSM-Teilnehmern über das TI-ITSM-System
bereitgestellt.

Der Business-Servicekatalog wird in TIP1-A_6367 definiert.

Unterstützungsservices sind Leistungen, die für die Erbringung von Services
Dritter notwendig sind.

### 2.2.2 Technischer Kennzahlenkatalog

Der Technische Kennzahlenkatalog enthält alle technischen Kennzahlen zu einem
TI-Service, deranderen TI-ITSM-Teilnehmern angeboten wird. Grundlage sind die
in der [gemSpec_Perf] festgelegten Werte. Im Rahmen des
Service-Katalog-Managements werden diese Werte im TI-ITSM-System hinterlegt.

**TIP1-A_7258 - Definition eines Technischen Kennzahlenkataloges**

TI-ITSM-Teilnehmer (außer FD VSDM und TSP eGK) MÜSSEN für jeden anderen
TI-ITSM-Teilnehmern angebotenen Service Kennzahlen in einem Technischen
Kennzahlenkatalog an den Gesamtverantwortlichen TI liefern. **[\<=]**

**TIP1-A_7259 - Mindestinhalte des Technischen Kennzahlenkataloges**

TI-ITSM-Teilnehmer, die nach TIP1-A_7258 einen Technischen Kennzahlenkatalog
liefern, MÜSSEN die Qualität der angebotenen Services in den Parametern
Performance, Bearbeitungszeit, Durchsatz und Verfügbarkeit definieren.
**[\<=]**

Hinweis: Diese Kennzahlenkataloge werden im TI-ITSM-System veröffentlicht.

### 2.2.3 Konfigurationen von Produkten

Das normative Verhalten einer Produktinstanz an seiner Außenschnittstelle wird
maßgeblich durch dessen individuelle und ad hoc änderbare Konfiguration
definiert. Eine eindeutige Referenzierung und Versionierung von
Konfigurationsparametern dient einerseits der Verhinderung von unkontrollierten
Veränderungen und andererseits der konsistenten Nachvollziehbarkeit bei
Änderungen im Zuge eines betrieblichen Change.

Konfigurationen in diesem Sinne folgen der Festlegung gem. [gemKPT_Test#A_20060].

Konfigurationen enthalten eine Sammlung von Konfigurationsparametern zum selben
Versionsstand.

Konfigurationsparameter sind üblicherweise in
Config-Dateien, Registry-Einträgen oder Aufrufparametern mit konkreten Werten
hinterlegt. Sie können mit Betriebssystemversionsständen, Patchlevel und
weiteren (Java-)Bibliotheksversionen angereichert sein.

**A_20218 - Versionierung der Konfiguration von Betriebsinstanzen**

TI-ITSM-Teilnehmer  MÜSSEN ihre Konfigurationsdaten anhand einer eindeutigen
Versionsbezeichnung nachvollziehbar referenzieren, sodass jederzeit eine
detailliere Auskunft über die exakte Konfiguration möglich ist. **[\<=]**

**A_20219 - Versionierung bei Veränderungen der Konfiguration von
Betriebsinstanzen**

TI-ITSM-Teilnehmer  MÜSSEN ihre Konfigurationsdaten anhand einer eindeutigen
Versionsbezeichnung bei Veränderungen nachvollziehbar, inklusive
Historiendarstellung, referenzieren, sodass jederzeit eine detailliere Auskunft
über die exakte Konfiguration möglich ist. **[\<=]**

**A_20220 - Festlegung von Konfiguration durch die gematik**

TI-ITSM-Teilnehmer  MÜSSEN aufgrund einer Anforderung der gematik bestimmte
Werte in ihre Konfiguration aufnehmen. **[\<=]**

**A_20221 - Rückspielbarkeit bei Veränderungen der Konfiguration von
Betriebsinstanzen**

TI-ITSM-Teilnehmer  MÜSSEN bei der Durchführung eines Changes die
Konfigurationen ihrer zu ändernden Produktinstanzen versionieren und
rückspielbar ablegen sowie auf Anfrage des GTI jederzeit eine detaillierte
Auskunft über die verwendete Konfiguration bereitstellen. **[\<=]**

### 2.2.4 Organisatorische Service Level

Organisatorische Service Level legen die Anforderungen an die Organisation zur
Lieferung oder Bereitstellung eines Services fest.

Sie messen die Fähigkeit der für den jeweiligen Service verantwortlichen
Organisation, einen Service in der geforderten Qualität zu liefern.

Die geforderte Qualität richtet sich nach der Priorität von
Geschäftsvorfällen, der betroffenen Betriebsumgebung, dem Zeitpunkt des
Auftretens (Haupt- oder Nebenzeit) sowie der Kritikalität des Services.

Organisatorische Service Level werden im Servicelevel-Management-Prozess
vereinbart und im TI-ITSM-System hinterlegt.

### 2.2.5 Unterstützungsleistungen aller TI-ITSM-Teilnehmer

Aus Servicenehmersicht ist die Verbindlichkeit der zu leistenden
Unterstützungsleistung anderer TI-ITSM-Teilnehmer entscheidend.
TI-ITSM-Teilnehmer nehmen definierte Rollen in der TI (Anbieter-Rollen) wahr
und müssen entsprechend ihrer Rolle definierte Services unterstützen.

Der Tabelle Tab_KPT_Betr_TI_001 TI-ITSM-Teilnehmer kann entnommen werden, durch
welche Anbieter-Rolle eine Unterstützungsleistung für welche Services
erfolgt, diese nur optional erfolgt oder ob sie ausbleibt.

Die Unterstützungsleistungen gliedern sich auf in

 ---> UL

### 2.2.6 Service-Verzeichnis

In einem Service-Verzeichnis werden alle Service-Kataloge aller
TI-ITSM-Teilnehmer zentral aufgeführt.

Jeder TI-ITSM-Teilnehmer nimmt am Service-Katalog-Management teil, um
Änderungen seines Service-Kataloges gesteuert einzubringen und mit der gematik
zu vereinbaren. In der Richtlinie Betrieb [gemRL_Betr_TI] wird dieser Prozess
detailliert beschrieben.

### 3 Servicekonzept

Das Servicekonzept regelt die Verantwortlichkeiten der TI-ITSM-Teilnehmer.

Die verbindliche Zuordnung der Anforderung zu den TI-ITSM-Teilnehmern erfolgt im
zugehörigen Steckbrief.

### 3.1 Übergreifendes IT-Service-Management der TI

Das ITSM gewährleistet eine effektive Kommunikation der an der
Serviceerbringung Beteiligten und ermöglicht so ein koordiniertes Vorgehen bei
der Behebung von Störungen und bei der Durchführung von Änderungen an der TI.

Die Mitwirkung der Anbieter im TI-ITSM und die Bereitstellung der benötigten
Schnittstellen sind ein wichtiger Bestandteil ihrer zu erbringenden Leistungen.
Diese werden im Dokument „Übergreifende Richtlinien zum Betrieb der TI“
[gemRL_Betr_TI] beschrieben.

### 3.2 Rollen

Im Folgenden sind die Rollen, Aufgaben und Verantwortlichkeiten der
TI-ITSM-Teilnehmer dargestellt.

Hinweis zum Folgerelease:

Nach § 75b Abs. 1 SGB V legen die Kassenärztlichen Bundesvereinigungen bis zum
30. Juni 2020 die Anforderungen zur Gewährleistung der IT-Sicherheit in der
vertragsärztlichen und vertragszahnärztlichen Versorgung in einer Richtlinie
fest. Die Kassenärztlichen Bundesvereinigungen müssen nach § 75b Abs. 5 SGB
V zusätzlich Anbieter im Einvernehmen mit dem Bundesamt für Sicherheit in der
Informationstechnik auf deren Antrag zertifizieren, wenn diese über die
notwendige Eignung verfügen, um die an der vertragsärztlichen und
vertragszahnärztlichen Versorgung teilnehmenden Leistungserbringer bei der
Umsetzung der Richtlinie sowie deren Anpassungen zu unterstützen. Inhalt der
Richtlinie sowie der Zertifizierung ist auch die sichere Installation und
Wartung von Komponenten und Diensten der Telematikinfrastruktur. 

Die gematik wird nach Veröffentlichung der Vorgaben für die Zertifizierung
prüfen, ob und welche Anbieter in der TI sie verpflichtet, bei der Ausführung
ihrer Tätigkeiten nur zertifizierte Techniker einzusetzen.

In jedem Fall haben Leistungserbringer nach § 291b Abs. 6a SGB V das Recht,
dass Dienstleister auf Verlangen ihre Fachkunde nachweisen.

Der Nachweis kann aus Sicht der gematik insbesondere durch die zuvor genannte
Zertifizierung der Kassenärztlichen Bundesvereinigungen erbracht werden.

### 3.2.1 Begriffserläuterungen

### 3.2.1.1 Servicenehmer

Ein Servicenehmer nutzt eine Serviceleistung eines TI-ITSM-Teilnehmer.
Servicenehmer können andere Anbieter oder Anwender sein.

### 3.2.2 TI-Service

TI-Services sind die durch die gematik beschlossenen IT-basierten
Dienstleistungen der TI, welche in einem Release konzipiert und implementiert
werden.

Ein TI-Service ist eine durch einen TI-ITSM-Teilnehmer erbrachte Dienstleistung
in der TI. Nutzer von TI-Services sind TI-ITSM-Teilnehmer und Anwender.

TI-Services können technisch durch den Betrieb zugelassener Produkte erbracht
werden oder betrieblich, durch Unterstützungsleitung im Support
desUHD(Anwendersupport) oderSPOCim TI-ITSM.

### 3.2.3 TI-ITSM-Teilnehmer

Das IT-Service Management der TI wird als TI-ITSM bezeichnet. Die Teilnehmer am
TI-ITSM werden als TI-ITSM-Teilnehmer bezeichnet. Die TI-ITSM-Teilnehmer sind
in Tab_KPT_Betr_TI_001 TI-ITSM-Teilnehmer aufgeführt.

In der üblichen Konstellation wird ein Anbieter operativer Betriebsleistungen
alle ihm zugeordneten Anforderungen selbst erfüllen und den Betrieb seines
Produktes und die Bereitstellung eines UHD selbst übernehmen. Für diesen Fall
gelten die folgend beschriebenen Regelungen für die Teilnahme am TI-ITSM.
Abweichungen davon sind im Kapitel 3.2.3.1 Anbieterkonstellationen aufgeführt.

Die folgende Tabelle enthält eine Übersicht über die Teilnehmer am TI-ITSM:

<table><tr><th>
Rolle  
(Anbieter/Hersteller/Verantwortliche)

</th><th>
Teilnahme am TI-ITSM

</th></tr><tr><td>
Anbieter KTR-AdV

</td><td>
ja

</td></tr><tr><td>
Anbieter VPN-Zugangsdienst *

</td><td>
ja

</td></tr><tr><td>
Anbieter VPN-Zugangsdienst mit UA **

</td><td>
nein

</td></tr><tr><td>
UA des Anbieters VPN-Zugangsdienst **

</td><td>
ja

</td></tr><tr><td>
Anbieter ePA-Aktensystem ***

</td><td>
ja

</td></tr><tr><td>
Betreiber ePA-Aktensystem mit UA ***

</td><td>
nein

</td></tr><tr><td>
Betreiber E-Rezept-Fachdienst

</td><td>
ja

</td></tr><tr><td>
UA des Anbieters ePA-Aktensystem ***

</td><td>
ja

</td></tr><tr><td>
Anbieter Zentrale Plattformdienste

</td><td>
ja

</td></tr><tr><td>
Anbieter Fachdienst VSDM

</td><td>
ja

</td></tr><tr><td>
Gematik Test

</td><td>
ja

</td></tr><tr><td>
Gematik Betrieb

</td><td>
ja

</td></tr><tr><td>
Gesamtverantwortlicher TI (GTI)

</td><td>
ja

</td></tr><tr><td>
Anbieter weiterer Anwendungen

</td><td>
ja

</td></tr><tr><td>
Anbieter Service Monitoring

</td><td>
ja

</td></tr><tr><td>
Anbieter HBA

</td><td>
ja

</td></tr><tr><td>
Anbieter SMC-B / HSM-B

</td><td>
ja

</td></tr><tr><td>
Anbieter TSP X.509 nonQES eGK

</td><td>
ja

</td></tr><tr><td>
Anbieter TSP X.509 Root-CA

</td><td>
ja

</td></tr><tr><td>
Anbieter TSP CVC eGK

</td><td>
ja

</td></tr><tr><td>
Anbieter CVC-Root-CA

</td><td>
ja

</td></tr><tr><td>
Anbieter Signaturdienst

</td><td>
ja

</td></tr><tr><td>
Anbieter KOM-LE

</td><td>
ja

</td></tr><tr><td>
Anbieter KTR-Consumer

</td><td>
nein

</td></tr><tr><td>
Anbieter Basis-Consumer

</td><td>
nein

</td></tr><tr><td>
Betreiber KTR-Consumer

</td><td>
ja

</td></tr><tr><td>
Betreiber Basis-Consumer

</td><td>
ja

</td></tr><tr><td>
Anbieter SGD_ePA zentral

</td><td>
ja

</td></tr><tr><td>
Anbieter E-Rezept-FdV

</td><td>
ja

</td></tr><tr><td>
Betreiber IdP-Dienst

</td><td>
ja

</td></tr><tr><td>
Dienstleister vor Ort (DVO)

</td><td>
nein

</td></tr><tr><td>
Hersteller eHealth-KT

</td><td>
nein

</td></tr><tr><td>
Hersteller Mob-KT

</td><td>
nein

</td></tr><tr><td>
Hersteller Konnektor

</td><td>
nein

</td></tr><tr><td>
Hersteller Primärsysteme

</td><td>
nein

</td></tr><tr><td>
Anbieter Versicherten Help Desk E-Rezept

</td><td>
ja

</td></tr><tr><td>
Anbieter TI-Messenger

</td><td>
ja

</td></tr></table>

*)  siehe 3.2.3.1 Anbieterkonstellationen – hier: nur in Konstellation I

**) siehe 3.2.3.1 Anbieterkonstellationen – hier: nur in Konstellation II und
III der Unterauftragnehmer, der den Betrieb des Produktes übernimmt

***) siehe 3.2.3.1 Anbieterkonstellationen – hier: nicht abschließend
definiert, siehe 3.2.18 Anbieter ePA-Aktensystem

(4) siehe 3.2.3.1 Anbieterkonstellationen - hier: abschließend definiert:
Konstellation II (Auslagerung Betrieb)

Die TI-ITSM-Teilnehmer sind Anbieter in der TI. Sie sind eindeutig durch die von
der gematik vergebene Teilnehmer-ID (TID) identifiziert.

Hersteller, Leistungserbringer, Versicherte und DVOs sind keine
TI-ITSM-Teilnehmer.

### 3.2.3.1 Anbieterkonstellationen

Anbieter operativer Betriebsleitungen können sich bei der Erbringung der
Betriebsleistung oder Teilen hiervon eines Unterauftragnehmers bedienen.

![Img-001][Img-001]

![Abbildung-1][Abbildung-1]

Die Beauftragung von Unterauftragnehmern durch den zugelassenen Anbieter bedarf
der vorherigen Zustimmung der gematik und wird in den Zulassungsvertrag
aufgenommen.

Die Verantwortung für die Erfüllung der Regelungen des Vertrages gegenüber
der gematik trägt auch im Falle der Beauftragung von Unterauftragnehmern
weiterhin ausschließlich der zugelassene Anbieter. Solange der Anbieter die
Erfüllung der Anforderungen für den Betrieb seiner Produkte sowie für die
Bereitstellung eines UHD selbst übernimmt, nimmt er die Normalkonstellation
nach Kapitel 3.2.3 ein und ist TI-ITSM-Teilnehmer. Er erbringt die
erforderlichen Nachweise selbst.

Konstellation I (Normalfall):

Der Anbieter ist TI-ITSM-Teilnehmer und erbringt die erforderlichen Nachweise
selbst.

Konstellation II (Auslagerung Betrieb):

Der Anbieter kann sich bereits im Zulassungsverfahren durch seinen
Unterauftragnehmer nach § 13 SGB X vertreten lassen und die erforderlichen
Nachweise wie z.B. Betriebshandbuch, Anbietererklärung und Prozessprüfung
bereits durch diesen erbringen lassen. Dann nimmt der Anbieter die
Konstellation II ein. Die zum Nachweis der Anforderungen für den User Help
Desk (UHD) erforderliche Anbietererklärung übernimmt der Anbieter selbst. Mit
Abschluss des Zulassungsvertrages verpflichtet sich der Anbieter
sicherzustellen, dass sein Unterauftragnehmer gegenüber der gematik zur Abgabe
aller erforderlichen Erklärungen sowie zur Durchführung aller tatsächlichen
Handlungen berechtigt und verpflichtet ist, soweit diese zur Erbringung der
Betriebsleistung erforderlich sind.

Dazu gehört auch die ausschließliche Teilnahme des Unterauftragnehmers an den
TI-ITSM-Prozessen der gematik. Somit ist der Anbieter dann, abweichend von der
Regelung nach Kap. 3.2.3, nicht selbst im TI-ITSM vertreten. Somit sind nur
diejenigen Dienstleister im TI-ITSM vertreten, welche die betrieblichen
Anforderungen an die Betriebsleistungen tatsächlich wahrnehmen.

 

Konstellation III (Auslagerung Betrieb und UHD):

Zusätzlich zur Konstellation II kann der zugelassene Anbieter auch einen
zweiten (oder denselben) Unterauftragnehmer mit der Erfüllung der
Anforderungen, welche die Bereitstellung des UHD betreffen, beauftragen. Dann
nimmt der Anbieter die Konstellation III ein. Die Erbringung der Nachweise der
Anforderungen des Anbieters erfolgen wie in der Konstellation II – hierbei
aber auch für den Betrieb des UHD - mit der Besonderheit, dass die Nachweise
für die gesamten Betriebsleistungen inklusive UHD durch den Unterauftragnehmer
im Zulassungsverfahren nach § 13 SGB X selbst erbracht werden können und der
Anbieter auch hier aus den gleichen Gründen nicht selbst im TI-ITSM vertreten
ist.

Auch in der Konstellation III ist der Unterauftragnehmer ausschließlicher
Teilnehmer an den TI-ITSM-Prozessen der gematik und der Anbieter, abweichend
von der Regelung nach Kap. 3.2.3, nicht selbst im TI-ITSM vertreten. Der zweite
Unterauftragnehmer, der die Bereitstellung des UHD übernimmt, ist ebenfalls
nicht im TI-ITSM vertreten.

Den TI-ITSM-Teilnehmern als auch den Anbietern eines UHD ist je nach
Konstellation ein definierter Anforderungshaushalt im Anbietertypsteckbrief
zugeordnet.

**A_16217-01 - Mindesterreichbarkeitszeiten im Versichertensupport (09:00-17:00
Uhr)**

Alle TI-ITSM-Teilnehmer, denen lt. TIP1-A_7266 ein VHD von 09:00 - 17:00 Uhr
zugeordnet ist, MÜSSEN imVersichertensupportdie gleichen
Mindesterreichbarkeitszeiten einhalten:Mo – Fr 09:00 – 17:00 Uhr im Rahmen
eines Einschichtbetriebs [außer an bundeseinheitlichen Feiertagen]. **[\<=]**

**A_20733-03 - Mindesterreichbarkeitszeiten im Versichertensupport (07:00-22:00
Uhr)**

Alle TI-ITSM-Teilnehmer, denen lt. TIP1-A_7266 ein VHD von 07:00 - 22:00 Uhr
zugeordnet ist, MÜSSEN imVersichertensupportdie gleichen
Mindesterreichbarkeitszeiten einhalten:Mo – Fr 07:00 – 22:00 Uhr [außer
an bundeseinheitlichen Feiertagen]. **[\<=]**

**A_20734-01 - Mindesterreichbarkeitszeiten im Versichertensupport (08:00-20:00
Uhr)**

Alle TI-ITSM-Teilnehmer, denen lt. TIP1-A_7266 ein VHD von 08:00 - 20:00 Uhr
zugeordnet ist, MÜSSEN imVersichertensupportdie gleichen
Mindesterreichbarkeitszeiten einhalten:Mo – Fr 08:00 – 20:00 Uhr [außer
an bundeseinheitlichen Feiertagen]. **[\<=]**

**A_20111 - Erreichbarkeit des Versicherten Help Desk (VHD)**

Alle TI-ITSM-Teilnehmer, die lt. TIP1-A_7266 einen VHD besitzen MÜSSEN
sicherstellen, dass ihre verantworteten HelpDesks    innerhalb der
vereinbarten Servicezeiten elektronisch und telefonisch    außerhalb
der vereinbarten Servicezeiten elektronischerreichbar sind. **[\<=]**

**TIP1-A_7260-01 - Mindesterreichbarkeitszeiten im Anwendersupport (09:00-17:00
Uhr)**

Alle TI-ITSM-Teilnehmer, denen lt. TIP1-A_7266 ein UHD von 09:00 - 17:00 Uhr
zugeordnet ist, MÜSSEN imAnwendersupportdie gleichen
Mindesterreichbarkeitszeiten einhalten:Mo – Fr 09:00 – 17:00 Uhr im Rahmen
eines Einschichtbetriebs [außer an bundeseinheitlichen Feiertagen]. **[\<=]**

**A_19532-01 - Erreichbarkeitszeiten im Anwendersupport (24/7)**

Alle TI-ITSM-Teilnehmer, denen lt. TIP1-A_7266 ein UHD 24/7 zugeordnet ist,
MÜSSEN im Anwendersupport die Erreichbarkeitszeiten von 24/7 einhalten:  
Mo
– So 0:00 – 24:00 Uhr. **[\<=]**

**TIP1-A_7261 - Erreichbarkeit der TI-ITSM-Teilnehmer untereinander**

Alle TI-ITSM-Teilnehmer MÜSSENuntereinanderuneingeschränkt elektronisch
erreichbar sein, aufgeteilt in Haupt- und Nebenzeit mit differenzierten
Reaktionszeiten. **[\<=]**

**TIP1-A_7262 - Haupt- und Nebenzeit der TI-ITSM-Teilnehmer**

Alle TI-ITSM-Teilnehmer MÜSSENuntereinanderfolgende Hauptzeit einhalten:Mo –
Fr 09:00 – 17:00 im Rahmen eines Einschichtbetriebs [außer an
bundeseinheitlichen Feiertagen]. Alle anderen Zeiten gelten als Nebenzeit.
**[\<=]**

**TIP1-A_7263 - Produktverantwortung der TI-ITSM-Teilnehmer**

Der TI-ITSM-Teilnehmer MUSS gewährleisten, dass sämtliche in seiner
Verantwortung betriebenen Produkte und Produktversionen von der gematik
zugelassen sind und der Betrieb dieser jederzeit zulassungskonform unter
Erfüllung aller technischen, sicherheitstechnischen und betrieblichen
Anforderungen erfolgt. **[\<=]**

### 3.2.4 DVO

Dienstleister vor Ort (DVOs) sind natürliche Personen. Sie unterstützen den
Anwender in allen Belangen hinsichtlich der TI. Sie lösen Probleme im
dezentralen Bereich. Störungsmeldungen werden durch den DVO über denUHDdes
VPNZugD qualifiziert weitergeleitet. Störungen und Probleme, die sich nur
durch Unterstützung aus dem zentralen Bereich der TI lösen lassen, werden von
ihnen entsprechend weitergeleitet.

Ihr Verantwortungsbereich wird durch einen individuell zwischen ihnen und dem
Anwender ausgehandelten Vertrag geregelt. Bereits heute wird für die Betreuung
von Praxen in vielen Fällen ein durch die Praxen beauftragter DVO eingesetzt.
Die gematik geht davon aus, dass diese Vertragsverhältnisse mit Einführung
der TI weiter bestehen.

### 3.2.5 Gesamtverantwortlicher TI (GTI)

Der Gesamtverantwortliche TI (GTI) übernimmt die

 ---> UL

Diese Rolle liegt bei der gematik. Dabei übernimmt die gematik keine operativen
Betriebsleistungen. Diese Leistungen sind von den Anbietern zu erbringen.

### 3.2.6 Serviceverantwortung (SV) der TI-ITSM-Teilnehmer

Die Serviceverantwortung liegt bei dem Anbieter des Services, unabhängig davon,
ob er diese selbst betreibt, oder einen Betreiber/Unterauftragnehmer
(unter-)beauftragt hat.

### 3.2.7 Anbieter

Ein Anbieter von Betriebsleistungen in der TI im Verständnis des vorliegenden
Dokumentes ist eine Organisation, die Services gegenüber Anwendern oder
anderen Servicenehmern anbietet und verantwortet. Ein Anbieter kann seine
Services selbst erbringen oder durch Betreiber erbringen lassen, jedoch
verbleibt die Serviceverantwortung (SV) beim Anbieter selbst.

Anbieter koordinieren gegenüber ihren Servicenehmern im Rahmen ihrer Service-
und Supportverantwortung die Hersteller der von ihnen angebotenen Produkte und
nachgelagerte Anbieter.

**A_20476 - Funktionalität, Interoperabilität, Sicherheit in der PU**

Der Anbieter MUSS aktiv dabei unterstützen, dass das von ihm im Rahmen des
Betriebs eingesetzte, von der gematik zugelassene Produkt, in der PU weiterhin
sicher, interoperabel und funktional betrieben wird. **[\<=]**

Sowohl nach der Zulassung des Produktes, als auch des Anbieters, können Fehler
im Betrieb auftreten. Die Fehler können verschiedener Natur sein und Aspekte
der Funktionalität, Sicherheit als auch der Interoperabilität betreffen. In
solch einem Szenario liegt es im Bestreben aller Beteiligten, eine gemeinsame
und übergreifende Lösung zu finden um die Nutzbarkeit des Dienstes wieder
herzustellen. Die dafür notwendigen Werkzeuge um in den Dialog zu treten und
den Fehler zu beheben stellen u.a. die Betriebsprozesse bereit (z.B. Incident-,
Problem-, Change-Prozess).

Betriebliche Szenarien welche die Notwendigkeit einer aktiven Unterstützung
erfordern können, sind z.B.

 ---> UL

### 3.2.8 Betreiber

Ein Betreiber ist eine natürliche oder juristischePerson, die die
Bereitstellung einer von der gematik zugelassenen bzw. bestätigten Komponente,
eines Dienstes oder einer Anwendung der Telematikinfrastruktur erbringt und
verantwortet.

Das Betreiben umfasst Tätigkeiten, wie das

 ---> UL

### 3.2.9 Hersteller dezentraler Produkte

Hersteller dezentraler Produkte stellen ein Produkt gemäß den Spezifikationen
her und übernehmen die Produkthaftung gemäß den gesetzlichen Vorgaben und
den Support gegenüber ihren Käufern. Hersteller unterscheiden sich von
Anbietern insbesondere dadurch, dass das verantwortete Produkt keinen
IT-Service darstellt, sondern physische Geräte oder Software, welche in der
Hoheit der Anwender betrieben werden.

### 3.2.10 Hersteller zentraler Produkte

Als Hersteller zentraler Produkte gilt der Antragsteller zur Produktzulassung
bei der gematik. Unter diesem Produkt wird ein physisches IT-Produkt
verstanden, eine Software allein erfüllt die Anforderung an ein Produkt nicht.
Das Produkt muss der gematik in einer konkreten Ausprägung vorliegen, welche
den normativen Anforderungen an den Produkttypen genügt.

Produkte werden durch die gematik zugelassen. Mit dieser Zulassung wird zugleich
die Verkaufsgenehmigung erteilt. Nach der ausgesprochenen Zulassung endet die
Geschäftsbeziehung zur gematik.

Produktiv zugelassene zentrale Produkte werden durch zugelassene Anbieter für
die Serviceerbringung betrieben. Daher werden betriebliche Anforderungen
ausschließlich an Anbieter gerichtet.

### 3.2.11 gematik-Test in der TU

Die gematik (Test) ist für die Durchführung der Zulassungstests der Produkte
in der TU zuständig. Produktiv zugelassene Anbieter müssen in der
Referenzumgebung (RU) und Testumgebung (TU) Referenzen der betriebenen Produkte
vorhalten. Bei Störungen der Referenzprodukte und Beeinträchtigung der
Testdurchführung stellt die gematik in der Rolle „Test“ gegen die Anbieter
der Referenzobjekte Tickets ein.

### 3.2.12 Anwender

Anwender sind natürliche Personen oder Organisationen, welche die Services der
TI nutzen und dadurch einen Mehrwert für sich oder ihren Geschäftsprozess
erwarten. Anwender in diesem Sinne sind Leistungserbringer.

Anwender im Kontext der TI sind für die bestimmungsgemäße Nutzung der Systeme
verantwortlich. Insofern tragen sie die Betriebsverantwortung für die
dezentralen Produkte. Handelt es sich beim Anwender um eine Organisation, z.B.
ein Krankenhaus, trägt die Organisation die Betriebsverantwortung und nicht
die einzelnen Anwender, welche die TI nutzen.

Dem Anwender (Leistungserbringer) wird zur Unterstützung und Problemlösung ein
UHD angeboten.

### 3.2.13 Versicherte

Für die Serviceunterstützung der Versicherten stellt der Anbieter
ePA-Aktensystem den Versicherten einen Versicherten Help Desk (VHD) zur
Verfügung.

### 3.2.14 Anbieter VPN-ZugD

Für die Anbieter eines VPN-ZugD gelten die drei Konstellationen aus Kapitel
3.2.3.1 abschließend. Der Anbieter kann sich zwischen diesen drei
Konstellationen entscheiden und den Betrieb entweder selbst organisieren und
alle Anforderungen des Anbietertypsteckbriefes selbst erfüllen. Alternativ
kann er sich bereits im Zulassungsverfahren durch einen Unterauftragnehmer
vertreten lassen sich somit für die Konstellation II oder III entscheiden. Mit
Abschluss des Zulassungsvertrages verpflichtet sich dann der Anbieter
sicherzustellen, dass sein Unterauftragnehmer gegenüber der gematik zur Abgabe
aller erforderlichen Erklärungen sowie zur Durchführung aller tatsächlichen
Handlungen berechtigt und verpflichtet ist, soweit diese zur Erbringung der
Betriebsleistung erforderlich sind. Im Zulassungsvertrag wird vermerkt, wer
TI-ITSM-Teilnehmer ist.

Der Anbieter VPN-ZugD stellt seinen Anwendern (Leistungserbringern) einen UHD
zur Verfügung.

**TIP1-A_6455 - Verpflichtung zur Dokumentation von Service Levels im
Anwendersupport des Anbieters VPN-Zugangsdienst**

Der Anbieter VPN-Zugangsdienst MUSS alle Service Levels im Anwendersupport im
Rahmen der Zulassung dokumentieren und die gematik über Änderungen
informieren. Hierbei MUSS der Anbieter VPN-Zugangsdienst eine Einteilung in
eine oder mehrere verschiedene Serviceklassen (logische Gruppierungen von
Service Levels in einer definierten Servicequalität, z. B. Gold, Silber,
Bronze) vornehmen. **[\<=]**

Hinweis: Die gematik behält sich vor, die Information zu den Service Levels im
Anwendersupport im Rahmen der Veröffentlichung der Zulassung mit zu
veröffentlichen.

**A_18430 - Bereitstellung Firewall-Konfigurationsdaten vom Anbieter
VPN-Zugangsdienst**

Der Anbieter VPN-Zugangsdienst MUSS alle für die Registrierung und den
Verbindungsaufbau zur TI notwendigen Netzwerkinformationen (IP-Zieladressen und
Ports) veröffentlichen und dem Gesamtverantwortlichen der TI bereitstellen.
Der Anbieter VPN-Zugangsdienst MUSS diese veröffentlichten Informationen stets
aktuell halten. **[\<=]**

Die Veröffentlichung dieser Informationen durch den Anbieter kann über
unterschiedliche Portale erfolgen, wie z.B. eigene Support-Portale oder die
TI-Wissensdatenbank. Zielgruppe für die veröffentlichten Informationen sind
sowohl die Leistungserbringer selbst als auch deren betreuende
IT-Dienstleister.Mit diesen Informationen sollen die lokalen Firewalls in den
dezentralen Umgebungen der Leistungserbringer möglichst restriktiv
konfiguriert werden können. Zeitgleich soll damit eine fehlerfreie
Kommunikation der dezentralen TI-Komponenten mit der TI über Ihren
VPN-Zugangsdienst sichergestellt werden.

### 3.2.15 User Help Desk (UHD)

Der UHD verantwortet die Behebung von Störungen, die von Anwendern [siehe
vorangegangene Kapitel] gemeldet werden. Ebenfalls gehört die Bearbeitung von
allgemeinen Anfragen der Anwender zu den Services des Anbieters zum
Leistungsumfang seines UHD.  Liegt die Lösungsverantwortung nicht bei dem den
UHD bereitstellenden Anbieter, erfolgt  eine Weitergabe des Tickets über den
SPOC an den lösungsverantwortlichen Anbieter über das TI-ITSM-System. Der
Anwender erhält nach Lösung seiner Störung über seinen UHD eine
Rückantwort.

### 3.2.16 Versicherten Help Desk (VHD)

Der VHD verantwortet die Behebung von Störungen im Zusammenhang mit der
Nutzung des ePA-Aktensystems, des E-Rezept-FdV oder des Signaturdienstes, die
von Versicherten [siehe vorangegangene Kapitel] gemeldet werden. Liegt die
Lösungsverantwortung nicht bei dem den VHD bereitstellenden Anbieter,
erfolgt  eine Weitergabe des Tickets über den SPOC an den
lösungsverantwortlichen Anbieter über das TI-ITSM-System. Der Versicherte
erhält nach Lösung seiner Störung über seinen VHD eine Rückantwort.

### 3.2.17 Anbieter ePA-Aktensystem

Für den Anbieter ePA-Aktensystem dienen die in Kapitel 3.2.3.1 aufgeführten
betrieblichen Konstellationen zur Orientierung – diese Optionen sind jedoch
nicht abschließend. Der Anbieter kann entscheiden, in welcher Weise er den
Betrieb organisiert. An dieser Stelle ist jedoch anzumerken, dass für die
TI-ITSM-Prozesse nur ein einziger Dienstleister als TI-ITSM-Teilnehmer für den
Anbieter im Anbietervertrag eingetragen werden kann. Dieser erfüllt dann die
in Kapitel 3.2.3.1 aufgeführten Berechtigungen und Verpflichtungen für den
Anbieter. 

Der Anbieter ePA-Aktensystem stellt abweichend von der Darstellung im Kapitel
3.2.3.1 nicht den Anwendern, sondern exklusiv den Versicherten, denen der
Anbieter ePA-Aktensystem ihre ePA-Akte zur Verfügung stellt, einen
Versicherten Help Desk (VHD) zur Verfügung.

Der Anbieter ePA-Aktensystem ist für den Betrieb einer Instanz des
Schlüsselgenerierungsdienstes SGD 1 (FAD) verantwortlich. Abgrenzend dazu ist
der zentrale Schlüsselgenerierungsdienst SGD 2 (TIP) zu sehen, wie er auch
separat in Tabelle: Tab_KPT_Betr_TI_002 Mitwirkungspflichten der
TI-ITSM-Teilnehmer dargestellt ist.

### 3.2.18 Anbieter Service Monitoring

Der Anbieter Service Monitoring betreibt das Produkt gemäß
[gemSpec_ServiceMon] und stellt die Messergebnisse und weitere Informationen
dem GTI und definierten Teilnehmern zur Verfügung. Eine Unterstützung der
beteiligten TI-ITSM-Teilnehmer ist dazu bereits bei der Initialisierung des
Systems bzw. bei Einrichtung und Inbetriebnahme der Probes notwendig.

**A_18176 - Mitwirkungspflichten bei der Einrichtung von Probes des Service
Monitorings**

Alle TI-ITSM-Teilnehmer, welche gemäß [gemKPT_Betr#Tab_KPT_Betr –
Mitwirkungspflichten der TI-ITSM-Teilnehmer] die Servicekomponente Service
Monitoring unterstützen, MÜSSEN den Anbieter Service Monitoring bei der
Einrichtung bzw. Änderung und Inbetriebnahme von Probes gemäß
[gemSpec_ServiceMon#5.4 ff.] unterstützen. **[\<=]**

Hinweis: Die Einrichtung und Inbetriebnahme finden im Rahmen des betrieblichen
Change Managements statt.

### 3.2.19 Anbieter Basis-Consumer

Für diese Anbieter dienen die in Kapitel 3.2.3.1 aufgeführten betrieblichen
Konstellationen abschließend.Abweichend der Darstellung im Kapitel 3.2.3.1
stellen die Anbieter Basis-Consumer keinen Anwender- bzw. Versichertensupport
zur Verfügung.

### 3.2.20 Anbieter KTR-Consumer

Für diese Anbieter dienen die in Kapitel 3.2.3.1 aufgeführten betrieblichen
Konstellationen abschließend.  
Abweichend der Darstellung im Kapitel 3.2.3.1
stellen die Anbieter KTR-Consumer keinen Anwender- bzw. Versichertensupport zur
Verfügung.

### 3.2.21 Anbieter KTR-AdV

 Der Anbieter KTR-AdV wird definiert als der von den Kassen beauftragte
Betreiber. Dieser wird durch die Kassen beauftragt und bietet den Service den
Versicherten an. Die Kassen werden deshalb nicht zusätzlich zugelassen und
sind auch nicht im TI-ITSM vertreten. Abweichend der Darstellung im Kapitel
3.2.3.1 stellen die Anbieter KTR-AdV keinen Anwender- bzw. Versichertensupport
zur Verfügung.

### 3.2.22 Anbieter KOM-LE

Für die Anbieter Fachdienst KOM-LE sind die in Abbildung 1 aufgeführten
betrieblichen Konstellationen möglich. Im Rahmen des Betriebs ist mit der
Anwendung sicherzustellen, dass ein eigener User Help Desk (UHD) zur Verfügung
gestellt wird.

### 3.2.23 Anbieter Anschlusspunkt am SGW

Der Anschlusspunkt für die Weiteren Anwendungen wird vom Anbieter Zentrale
Plattformdienste bereitsgestellt und administriert - sowohl für Anbindungen
über das SGW (aAdGNetG) oder einen SZZP (aAdG und aAdGNetG-TI).

Für die Weiteren Anwendungen gibt es die Konstellation am Markt, dass hinter
diesem Anschlusspunkt ein Netzwerk aufgespannt wird, um verschiedene Weitere
Anwendungen daran anzuschließen und zu vernetzen - also mehrere Weitere
Anwendungen am gleichen Anschlusspunkt. Somit kann ein bestätigter Anbieter
aAdGNetG seinen Anschluss anderen Anbietern aAdGNetG zur Verfügung stellen.

Dem Anbieter dieses Netzwerkes, der ebenfalls bestätigter Anbieter einer
Weiteren Anwendung (aAdGNetG) sein muss, werden deshalb zusätzliche
betriebliche Mitwirkungspflichten auferlegt. Diese werden im
Anwendungssteckbrief in einem gesonderten Kapitel aufgeführt
[gemAnw_WA_aAdGNetG#3.4].

Diese Mitwirkungspflichten sind notwendig, um in die Koordination der
betrieblichen Prozesse involviert zu sein und um eine betriebliche
Rollentrennung zwischen der Infrastruktur und ggf. weiteren
aAdG/aAdGNetG/aAdGNetG-TI mit einer eigenen Bestätigung zu ermöglichen.

Nach Wegfall der Rolle eines Anbieters einer Weiteren Anwendung (d.h.
Erlöschung der Bestätigung), welcher seinen Anschluss anderen zur Verfügung
gestellt hat, entfällt auch der Anschluss.

**A_19831 - Teilnahme am TI-ITSM als Anbieter Anschlusspunkt am SGW**

Der Betreiber des Anschlusspunktes, welcher diesen auch anderen aAdGNetG zur
Verfügung stellt, MUSS diese Rolle als Teilnehmer im TI-ITSM wahrnehmen.
**[\<=]**

### 3.2.24 Anbieter TI-Messenger

Für den Anbieter TI-Messenger sind die in Abbildung 1 aufgeführen
betrieblichen Konstellationen möglich.Entsprechend [gemKPT_TI_Messenger] liegt
die Betriebsverantwortung für die Produkte TI-Messenger-Fachdienst und
TI-Messenger-Client beim Anbieter TI-Messenger.Im Kontext des TI-Messengers
können Anwender z.B. LE oder LEI sein. In der Ausbaustufe TI-Messenger 2.0
sollen auch Versicherte die Anwendung nutzen können. Die Bereitstellung des
Dienstes für die Versicherten erfolgt dabei durch die vertretende Kasse,
welche z.B. selbst als Anwender/Nutzer durch eine Organisation entsprechend
[gemKPT_TI_Messenger] abgebildet werden kann.

### 3.3 Servicemodell

Anhand der fachlogischen Abhängigkeiten werden die Servicebeziehungen zwischen
allen TI-ITSM-Teilnehmernaufgezeigt und Anbieter und Servicenehmer benannt.

Ein Servicemodell ist eine übersichtsartige Beschreibung eines Service und der
Komponenten, die zum Erbringen des Services erforderlich sind. Das wichtigste
Ziel von Servicemodellen ist, zu verstehen, welche Service-Komponenten, Assets
und sonstigen Ressourcen für die Erstellung eines Service notwendig sind,
einschließlich deren gegenseitiger Abhängigkeiten. Servicemodelle sind ein
wichtiges Werkzeug, um den Einfluss von Services auf andere Services zu
erkennen.

TI-ITSM-Teilnehmer definieren alle Leistungen, die sie anderen Servicenehmern
zur Verfügung stellen in einem Business-Servicekatalog.

Zur Sicherstellung der eigenen Serviceerbringung müssen TI-ITSM-Teilnehmer alle
notwendigen Unterstützungsleistungen anderer TI-ITSM-Teilnehmer intern
definieren. Diese werden außerhalb der zu veröffentlichenden Kataloge
beschrieben.

Das ist nicht nur für die Serviceerbringung notwendig, sondern auch für die
betriebliche Unterstützung bei Problemen, Störungen oder betrieblichen
Anpassungen im Produktivbetrieb.

### 3.3.1 Servicekomponenten

Unter Servicekomponenten werden einzelne Einheiten verstanden, die für die
Erbringung eines Service notwendig sind. Die Zerlegung der TI-Services in
Servicekomponenten erfolgt durch die Art der Unterstützung. Alle
Servicekomponenten eines Anbieters zusammengefasst ergeben den Service des
Anbieters.

Die Tabelle Tab_KPT_Betr_TI_002 Mitwirkungspflichten der TI-ITSM-Teilnehmer
zeigt die differenzierten Mitwirkungspflichten von TI-ITSM-Teilnehmern
bezüglich der unterstützenden Servicekomponenten (SK).

### 3.3.2 Servicezerlegung

TI-Services werden in Servicekomponenten zerlegt.

**TIP1-A_7266 - Mitwirkungspflichten im TI-ITSM-System**

Alle TI-ITSM-Teilnehmer MÜSSEN die Mitwirkungspflichten nach Tabelle
Tab_KPT_Betr_TI_002 Mitwirkungspflichten der TI-ITSM-Teilnehmer befolgen. **[\<=]**

![Img-003][Img-003]

### 3.3.2.1 Legende

Die Tabelle ist folgendermaßen lesbar:

„Wenn eine Servicekomponente eingeschränkt ist, WER muss dann WIE
unterstützen?“

Die Unterscheidung zwischen „U“ und „V“ ist in dieser Hinsicht wichtig,
weil „V“ keine aktive operative Tätigkeit bedeutet, sondern das Aufnehmen
der Störung und Weiterleiten an den Lösungsverantwortlichen. (klassisches
Vermitteln=„V“)

E: eigener Service

Als eigener Service (E) wird der durch den Anbieter bestimmungsgemäß
angebotene Service verstanden. Dieser kann einem konkreten Anbieter zugeordnet
werden.

U: Unterstützungsservice

Als Unterstützungsservice (U) wird die aktive Mitwirkung für eigene und fremde
Services bezeichnet, die für das Erbringen der eigenen Dienstleistung
notwendig ist.

V: Vermittelnder Anwendungsservice

Als vermittelnder Anwendungsservice (V) wird die sonstige Mitwirkung für fremde
Services bezeichnet, die auf Grundlage geltender Verpflichtungen für das
Erbringen fremder Dienstleistungen notwendig ist.

O: Optionale Unterstützung

Als optionale Unterstützung (O) werden sämtliche freiwillige
Unterstützungsleistungen gemäß vereinbarter Verträge verstanden.

### 3.3.3 Mitwirkungsverpflichtung im TI-ITSM gemäß [gemRL_Betr_TI]

Aufgrund der Mitwirkungs- und Unterstützungsverpflichtungen gemäß Tabelle 3:
Tab_KPT_Betr_TI_002 Mitwirkungspflichten der TI-ITSM-Teilnehmer besteht eine
übergreifende Mitwirkungspflicht am TI-ITSM der gematik.

Folgende Tabelle zeigt die Mitwirkungsverpflichtung in den aufgeführten
ITIL-Betriebsprozessen der gematik gemäß Richtlinie Betrieb [gemRL_Betr_TI]:

![Img-004][Img-004]

Die Prozesse Servicekatalog Management und Continual Service Improvement sind
auf den AZPD beschränkt und werden in nicht-öffentlichen Dokumenten geregelt.

### 3.3.3.1 Legende

A: Auslöser in INC, PRO, CHG

Auslöser (A) ist, wer Incidents, Problems oder Changes eröffnet.

E: Empfänger von INC, PRO, CHG

Empfänger (E) ist wer Incidents, Problems oder Changes zugewiesen bekommt und
dessen vollständige Mitarbeit gewährleistet ist.

Auslöser und Empfänger im SKM

Auslöser (A) ist, wer Änderungen im Service Katalog Management einbringt.

Empfänger (E)  ist, wer Änderungen im Service Katalog Management aufnimmt.

Portalanbieter (P) ist, wer das TI-Service-Portal zur Verfügung stellt und
selbst Nutzer ist.

A/E: Auslöser und Empfänger im SLM

Auslöser (A) ist, wer Änderungen im Servicelevel Management einbringt.

Empfänger (E)  ist, wer im Servicelevel Management an Servicelevel-Reviews
teilnimmt.

A/E: Auslöser und Empfänger im RF

Auslöser (A) ist, wer Services bei anderen Anbietern abruft.

Empfänger (E)  ist, wer einen Servicekatalog führt und Services anbietet.

A/E: Auslöser und Empfänger im Perf

Auslöser (A) ist, wer Performancereports sendet.

Empfänger (E) ist die gematik.

A/E: Auslöser und Empfänger im CapM

Auslöser (A) ist, wer Kapazitätspläne führt und reportet.Empfänger (E) ist
die gematik (GTI).

A/E: Auslöser und Empfänger im KM

Auslöser (A) ist, wer Artikel in der Wissensdatenbank einstellt.

Empfänger (E) ist, wer Artikel aus der Wissensdatenbank bezieht.

A/E: Auslöser und Empfänger im CSI

Auslöser (A) ist, wer ein CSI-Register führt und reportet.Empfänger (E) ist
die gematik (GTI).

A/E: Auslöser und Empfänger im CM

Auslöser (A) ist, wer Reports sendet, in denen die Konfigurationen der
verwendeten Produkte dargestellt werden.

Empfänger (E) ist, wer Konfigurationsvorgaben und deren Umsetzung dar z.B. im
Zuge eines CRs oder Changes empfängt und umsetzt.

A/E: Auslöser und Empfänger im NM

Aktiv (A) ist, wer im Notfall zuarbeiten und unterstützen muss.

Empfänger (E) stellen einen Notfall-Ansprechpartner bereit.

### 3.4 Supportkonzept

Aufbauend auf der Servicearchitektur wird nachfolgend das Supportkonzept
beschrieben.

### 3.4.1 Begriffserläuterungen

Supportverantwortung

Der Begriff soll ausschließlich im Zusammenhang mit dem 1st-Level-Support
benutzt werden und bezieht sich auf die verantwortliche Koordination bei der
Behebung einer Störung: Wenn ein Anwender eine Störung an einen
1st-Level-Support meldet, die dieser selbst nicht beheben kann, dann
verantwortet der 1st-Level-Support Koordination.

Lösungsverantwortung

Die Lösungsverantwortung wird entweder durch den 1st-Level-Support selbst
wahrgenommen, wenn sich die Störung innerhalb des 1st-Level-Supports lösen
lässt, oder sie wird durch den 1st-Level-Support (Supportverantwortlicher) an
den für die Servicekomponente verantwortlichen Anbieter delegiert.

1st Level Support

Der Begriff 1st Level Support bezieht sich auf die Entgegennahme von
Meldungen/Anfragen von Anwendern im Rahmen einer vorhandenen
Supportverantwortung gegenüber dem Melder. Im 1st Level Support erfolgt eine
Qualifizierung der Meldung und wird - wenn möglich - eine Lösung gefunden
bzw. die qualifizierte Meldung an den 2nd Level Support weitergeleitet (siehe
[gemRL_Betr_TI]).

2nd / 3rd Level Support

2nd/3rd Level Support sind unter einem Single-Point-Of-Contact (SPOC)
erreichbar, den jeder Anbieter bereitstellt.

Der Begriff 2nd/3rd Level Support bezieht sich auf die Herbeiführung einer
Lösung/ Beantwortung von Anfragen durch den 1st Level Support.

Dazu koordiniert der zuständige Anbieter seine produktverantwortlichen
Anbieter/Hersteller und Drittanbieter.

### 3.4.2 Single-Point-of-Contact (SPOC) für TI-ITSM-Teilnehmer

Jeder Anbieter benennt übergreifend für die von ihm zu verantwortenden
Servicekomponenten einen Single-Point-of-Contact (SPOC) gegenüber allen
anderen TI-ITSM-Teilnehmern. Über den SPOC erfolgt der erforderliche
wechselseitige Support der Anbieter in der TI über das TI-ITSM-System.

### 4 Verantwortlichkeiten und Leistungen TI-ITSM-Teilnehmer

### 4.1 Begriffserläuterungen

### 4.1.1 Anbietertypsteckbrief

Für jeden TI-ITSM-Teilnehmer gibt es jeweils einen Anbietertypsteckbrief in dem
die Anforderungen an sie beschrieben sind. Die Anforderungen stammen aus den
Betriebsdokumenten (gemKPT_Betr, gemRL_Betr_TI).

Für die Anbieter weiterer Anwendungen gibt es davon abweichend einen
Anwendungssteckbrief, in welchem die an ihn gerichteten Anforderungen
beschrieben sind. Die betrieblichen Anforderungen stammen aus den
Betriebsdokumenten (gemKPT_Betr, gemRL_Betr_TI).

### 4.2 Allgemeine Anforderungen

### 4.2.1 Allgemeine Anforderungen für TI-ITSM-Teilnehmer

Definition von Serviceleistungen

**TIP1-A_6367-02 - Definition eines Business-Servicekatalog der angebotenen TI
Services**

Anbieter MÜSSEN alle von ihnen angebotenen TI Services und -qualitäten
gegenüber den Anwendern und anderen Anbietern in einem Business-Servicekatalog
dokumentieren und diese Dokumentation der gematik vorlegen. **[\<=]**

**TIP1-A_6359-02 - Definition der notwendigen Leistung anderer Anbieter durch
Anbieter**

Definition der notwendigen Leistung anderer Anbieter durch Anbieter MÜSSEN
sicherstellen, dass alle zu ihrer Serviceerbringung notwendigen Leistungen
anderer Anbieter im Sinne eines Servicekataloges der unterstützenden Services
definiert sind. **[\<=]**

Überwachung

**TIP1-A_6360-02 - Kontrolle bereitgestellter Leistungen durch Anbieter**

Anbieter MÜSSEN die von anderen beteiligten Anbietern an sie bereitgestellten
Leistungen bezüglich deren Eignung im Betrieb kontrollieren und
Optimierungsbedarf der gematik mitteilen. **[\<=]**

**TIP1-A_6388-02 - Bereitstellung eines lokalen IT-Service-Managements durch
Anbieter für ihre zu verantwortenden Servicekomponenten**

Anbieter MÜSSEN für die von ihnen verantworteten Servicekomponenten ein
lokales ITSM etablieren. **[\<=]**

**TIP1-A_6390-02 - Mitwirkung im TI-ITSM durch Anbieter**

Anbieter MÜSSEN die in den Richtlinien zum Betrieb der TI [gemRL_Betr_TI]
geforderten Anbieter-Schnittstellen bereitstellen und ihren
Mitwirkungspflichten gegenüber der gematik und den anderen Teilnehmern
nachkommen. **[\<=]**

Erreichbarkeit UHD, Meldungsquittung, Status, Weiterleitung

**TIP1-A_6389-02 - Erreichbarkeit der 1st-Level (UHD), 2nd-Level (SPOCs) der
Anbieter**

Anbieter MÜSSEN sicherstellen, dass ihre verantworteten UHDs bzw.
SPOCs    innerhalb der vereinbarten Servicezeiten elektronisch und
telefonisch    außerhalb der vereinbarten Servicezeiten
elektronischerreichbar sind. **[\<=]**

**TIP1-A_6393-02 - Verantwortung für die Weiterleitung von Anfragen**

Anbieter MÜSSEN von ihnen nicht lösbare Anwenderanfragen/Störungsmeldungen an
den lösungsverantwortlichen Anbieter delegieren oder begründet ablehnen.
**[\<=]**

Koordination von Serviceleistung

**TIP1-A_6377-02 - Koordination von produktverantwortlichen Anbietern und
Herstellern**

Anbieter MÜSSEN im Rahmen der Service- und Supporterbringung die erforderlichen
Leistungen von produktverantwortlichen Anbietern, Herstellern und
Drittanbietern integrieren und koordinieren. **[\<=]**

**TIP1-A_6415-02 - Fortgeführte Wahrnehmung der Serviceverantwortung bei der
Delegation von Aufgaben**

Anbieter MÜSSEN bei der Delegation von Aufgaben an durch sie beauftragte
Anbieter, Hersteller oder Drittanbieter weiterhin ihre Serviceverantwortung
gegenüber ihren Servicenehmern und der gematik wahrnehmen. **[\<=]**

### 4.2.2 Allgemeine Anforderungen nur für Anbieter von Diensten

**TIP1-A_6371-02 - 2nd-Level-Support: Single-Point-of-Contact (SPOC) für
Anbieter**

Jeder Anbieter MUSS für die an der TI teilnehmenden anderen Anbieter einen
Single-Point-of-Contact (SPOC) benennen über den sein 2nd-Level-Support
erreichbar ist. **[\<=]**

### 4.3 Service Level (vorgangsübergreifend)

### 4.3.1 Begriffserläuterungen

### 4.3.1.1 Quantil / Erfüllungsgrad

Ein Quantil ist genau der Wert, der eine Reihe von der Größe nach sortierten
Werten in zwei Abschnitte unterteilt z. B. 95%-Quantil ist der 95.-Wert einer
der Größe nach sortierten Reihe von 100 Werten.

Dies bedeutet, dass z. B. von 20 Messwerten im Berichtszeitraum 1
Unterschreitung des definierten Grenzwertes auftreten darf, um den Service
Level im 95%-Quantil noch einzuhalten. Ab 19 Messwerten im Berichtszeitraum
würde dagegen jede weitere Überschreitung (z. B. Lösungszeit von Prio1 \<=
2 h wurde einmal überschritten) zur Verletzung des Service Levels führen.Der
Erfüllungsgrad ist das Verhältnis von SLA-konformen Tickets
(Bearbeitungszeiten) zur Gesamtzahl der Tickets im monatlichen
Betrachtungszeitraum. Sollte der "SL-Wert" (identisch mit bisherigem Quantil)
unterschritten werden, ist der Service Level verletzt.

DeraktuelleErfüllungsgrad wird bei den organisatorischen Service Leveln pro
Kenngröße (SL-ID) je Betriebsumgebung (RU, TU, PU) ermittelt.

Da dieser Berechnungsweg einfacher ist, frühzeitige Trend-Aussagen ermöglicht
werden und in den etablierten ITSM-Tools verwendet wird, löst er den Weg über
die Quantil-Berechnung ab. Das Ergebnis ist in beiden Fällen das Gleiche.

### 4.3.1.2 Reaktionszeit

Die Reaktionszeit ist der Zeitraum zwischen Eingang eines Vorgangs beim
Empfänger und seiner Rückmeldung an den Absender. Dabei enthält die Anfrage
eine durch den Empfänger zu bearbeitende Aufgabenstellung.

Die Reaktionszeit wird durch das TI-ITSM-System ermittelt. Sie beginnt mit
Eingang der Meldung im TI-ITSM-System und endet mit der im TI-ITSM-System
dokumentierten Rückmeldung (z. B. Annahme der angeforderten Aufgabe oder
deren Ablehnung).

### 4.3.1.3 Lösungszeit

Die Lösungszeit ist der Zeitraum zwischen der Aufnahme der Bearbeitung eines
Vorgangs und seiner finalen Lösung. Sie kann dabei durch besondere Ereignisse
unterbrochen werden (z.B. durch Eskalation, Unterstützungsanfrage an Dritte,
Ablehnung der zunächst gefundenen Lösung …).

Die Lösungszeit wird durch das TI-ITSM-System ermittelt. Sie beginnt nach der
im TI-ITSM-System dokumentierten Annahme der Lösungsbereitschaft durch den
Bearbeiter und endet mit dem Setzen des entsprechenden Status zu dem jeweiligen
Vorgang.  

### 4.3.1.4 Verifikationsfrist

Die Verifikationsfrist wird durch das TI-ITSM-System ermittelt.

Sie beginnt nach der im TI-ITSM-System dokumentierten Bereitstellung der Lösung
und endet mit der im TI-ITSM-System vollzogenen Schließung des Vorgangs oder
Ablehnung der Lösung. Je nach Vorgang erfolgt die Schließung differenziert.
Im INC schließt der einstellende Teilnehmer, im PRO der Lösende nach
Bestätigung.

### 4.3.2 Incident Management

**TIP1-A_6420-03 - Erreichbarkeit der 1st-Level-UHDs**

Der 1st-Level-UHD eines Anbieters VPN-Zugangsdienst MUSS folgende
Mindestservicezeiten nach Tab_KPT_Betr_TI_044 unterstützen.

Tabelle4: Tab_KPT_Betr_TI_044 Mindestservicezeit Störungsmeldungen und Anfragen

<table><tr><th>
Anbieter

</th><th>
Servicezeit

</th></tr><tr><td>
Anbieter VPN-Zugangsdienst

</td><td>
Mo-So 00:00 - 24:00 Uhr  
 

</td></tr></table>

**[\<=]**

**TIP1-A_7265-03 - Serviceleistung der TI-ITSM-Teilnehmer im
TI-ITSM-Teilnehmersupport zur Haupt- und Nebenzeit**

TI-ITSM-Teilnehmer mit Mitwirkungsverpflichtung zur Haupt- und Nebenzeit
gemäßTab_KPT_Betr_TI_002 Mitwirkungspflichten der TI-ITSM-TeilnehmerMÜSSEN
die folgenden Service Level (Zeiten) einhalten:

Tabelle5: Tab_KPT_Betr_TI_052 Service Level (Zeiten) im TI-ITSM

![Img-005][Img-005]

* Die Reaktionszeit gilt sowohl für die Rolle Incident/Problem -
Verantwortlicher als auch Incident/Problem - Unterstützer.

H (Hauptzeit): Mo - Fr 09:00 - 17:00 im Rahmen eines Einschichtbetriebs [außer
an bundeseinheitlichen Feiertagen].

N (Nebenzeit): Alle anderen Zeiten gelten als Nebenzeit.

** Abhängig vom im Business-Servicekatalog des TI-ITSM-Teilnehmers
angebotenen konkreten Service **[\<=]**

Sind SL nur der Hauptzeit (H) zugeordnet, so kann die Bearbeitung in der
Nebenzeit unterbrochen werden und wieder in der Hauptzeit aufgenommen werden.
Die Einhaltung dieses SL wird nur in der Hauptzeit gemessen.

**A_13573-01 - Serviceleistung der TI-ITSM-Teilnehmer im
TI-ITSM-Teilnehmersupport zur Hauptzeit**

TI-ITSM-Teilnehmer mit Mitwirkungsverpflichtung nur zur Hauptzeit gemäß  

Tab_KPT_Betr_TI_002 Mitwirkungspflichten der TI-ITSM-Teilnehmer  
MÜSSEN die
folgenden Service Level (Zeiten) einhalten:

Tabelle6: Tab_KPT_Betr_TI_053 Alternative Service Level (Zeiten) im TI-ITSM

![Img-006][Img-006]

* Die Reaktionszeit gilt sowohl für die Rolle Problemverantwortlicher als auch
Problemunterstützer.

H (Hauptzeit): Mo - Fr 09:00 - 17:00 im Rahmen eines Einschichtbetriebs [außer
an bundeseinheitlichen Feiertagen].

N (Nebenzeit): Alle anderen Zeiten gelten als Nebenzeit.

Alle SL sind nur der Hauptzeit (H) zugeordnet. Die  Bearbeitung in der
Nebenzeit ruht und wird in der Hauptzeit wieder aufgenommen. Die Einhaltung
dieses SL wird nur in der Hauptzeit gemessen.

** Abhängig vom im Business-Servicekatalog des TI-ITSM-Teilnehmers
angebotenen konkreten Service **[\<=]**

### 4.3.3 Reporting

Zum Zwecke der monatlichen Bewertung der Service Level müssen die von den
TI-ITSM-Teilnehmern zu erfassenden und zu übermittelnden technischen
Performancekenngrößen vollständig vorliegen. 

**A_18238 - Service Level - Übermittlung von Performance-Reports**

TI-ITSM-Teilnehmer, die gemäß [gemRL_Betr_TI#A_18236] technische
Performance-Kenngrößen in Performance-Reports liefern, MÜSSEN den Report
spätestens zum 5. Werktag des auf den Berichtszeitraum folgenden
Monats vollständig sowie sachlich und inhaltlich korrekt übermitteln.
**[\<=]**

**A_18239-01 - Service Level - Lieferung von Rohdaten-Performance-Reports**

TI-ITSM-Teilnehmer, die gemäß [gemRL_Betr_TI#A_18237] technische
Performance-Kenngrößen in Rohdaten-Performance-Berichten liefern, MÜSSEN
auch für die Rohdaten-Lieferung die ihnen zugeweisene Regelung (SLA) gemäß
A_13573 bzw. TIP1-A_7265 für den Prozess Reporting (REP) erfüllen.  **[\<=]**

Jeder TI-ITSM-Teilnehmer muss die Werte der von ihm zu verantwortenden Service
Level bereitstellen, d.h. prüfen, ggf. erfassen, bewerten, kommentieren und
für die weitere Verarbeitung im TI-ITSM-System freigeben (siehe
[gemRL_Betr_TI#9.2.2]). Für das technische und organisatorische Service
Level-Reporting stellt der Gesamtverantwortliche der TI eine
Reportingschnittstelle im TI-ITSM-System zur Verfügung. 

Die Bereitstellung kann vom TI-ITSM-Teilnehmer erst dann vorgenommen werden,
wenn der betreffende Service Level-Report im TI-ITSM-System zur Verfügung
steht. Es ist beabsichtigt, den Service Level-Report spätestens zum 10.
Werktag des auf den Bewertungszeitraum folgenden Kalendermonats zur Verfügung
zu stellen, so dass jedem TI-ITSM-Teilnehmer mindestens eine Frist von drei
Werktagen zur Bereitstellung seiner Service Level verbleibt.

**A_18240 - Reporting der technischen Service Level**

TI-ITSM-Teilnehmer, welche gemäß [gemSpec_Perf] technische
Performance-Kenngrößen erfassen und liefern, MÜSSEN die Werte der Service
Level Performance-Kenngrößen gemäß [gemRL_Betr_TI#GS-A_4100, GS-A_4101 und
GS-A_5604] einmal im Monat - spätestens zum 13. Werktag des auf den
Bewertungszeitraum folgenden Monats - vollständig sowie sachlich und
inhaltlich korrekt bereitstellen. Der Bewertungszeitraum umfasst einen vollen
Kalendermonat. **[\<=]**

Die Erfüllung der Reporting-Anforderungen [A_18238, A_18239 sowie A_18240]
wird pro Anforderung im monatlichen Service Level-Reporting ausgewiesen. 

### 4.3.4 Datenaufbewahrung

**TIP1-A_6437 - Datenaufbewahrung von Performancedaten**

Anbieter (ausgenommen ist TSP CVC eGK) MÜSSEN die Performancedaten 6 Monate
aufbewahren. **[\<=]**

### 5 Übergreifende Regelungen für betriebliche Kennzahlen für mobile Anwendungen (apps)

Sofern die folgenden Anforderungen nicht in fachspezifischen Konzepte enthalten
sind werden sie hier übergreifend generisch aufgeführt.

**A_19501 - Funktionsblock App-Check für die Betriebsdatenerfassung**

Jede Komponente mit einer Kommunikationsschnittstelle zu einer mobilen Anwendung
(App) MUSS den Funktionsblock "App-Check" implementieren.Der Funktionsblock
"App-Check" MUSS die Identifikatoren der sich verbindenden App [Hersteller-ID,
Versions-ID und Build-ID] erfassen und in einem konfigurierbaren Intervall an
die Betriebsdatenerfassung übermitteln.Voreingestellt ist 5 Minuten. **[\<=]**

**A_19503 - Erheben von Betriebsdaten von Apps (Anzahl der Verbindungen)**

Jede Komponente (App) MUSS vor der fachlichen Kommunikation an den
Funktionsblock "App-Check" des Kommunikationspartners seine Identifikatoren
[Hersteller-ID, Versions-ID und Build-ID] übermitteln. **[\<=]**

**A_19504 - Erheben von Betriebsdaten von Apps (Erfolgsermittlung)**

Nach jedem Anwendungsfall und vor Beendigung der Kommunikation MUSS jede
Komponente (App) an den Funktionsblock "App-Check" des Kommunikationspartners
seine Identifikatoren [Hersteller-ID, Versions-ID und Build-ID] und Erfolg oder
Misserfolg des Anwendungsfalles übermitteln.Für den Fall des Misserfolges
MUSS eine Fehlermeldung mit dem Namen der fehlgeschlagenen Operation erfolgen.
**[\<=]**

**A_19502 - Ausschluss von Apps an der Kommunikation durch Funktionseinheit
App-Check**

Die Funktionseinheit App-CheckMUSS Apps, welche die Sicherheitsvorgaben nicht
erfüllen, effektiv von der Kommunikation ausschließen. **[\<=]**

**A_19728 - Anbieten mobiler Anwendungen (Apps) ausschließlich vom App-Store
des Betriebssystems**

Mobile Anwendungen (Apps) MÜSSEN ausschließlich über offizielle App-Stores
des dazugehörigen Betriebssystems angeboten werden. **[\<=]**

### 6 Anhang A – Performance-Kenngrößen

Für die Performance-Größen (Tab_gemKPT_Betr_Performance-Groessen) zu den
Performance-Dimensionen (Tab_gemKPT_Betr _Performance-Dimensionen) erfassen und
reporten die Produkttypen (Tab_gemKPT_Betr _Produkttypen) für die
Schnittstellenoperationen (Tab_gemKPT_Betr _Schnittstellenoperationen) die
Performance-Kenngrößen gemäß Tab_gemKPT_Betr _Performance-Kenngroessen.
OCSP-Responder liefern Performance-Größen getrennt nach Zertifikatstypen
(Tab_gemKPT_Betr _Zertifikatstypen).

Das Zentrale Netz erfasst Ausfälle bezogen auf die Verbindungen (Vxx) zwischen
konkreten Produktinstanzen pi der TI vom Typ VPN-Zugangsdienst, Zentraler
Dienst TI-Plattform, Fachanwendungsspezifischer Dienst und Sicherheitsgateway
Bestandsnetze. Siehe hierzu [gemKPT_Arch_TIP], Abbildung „Netzwerktopologie
der TI“.

Der konkrete Bezeichner Vxx für eine Verbindung zwischen den beiden  SZZPs
szzp1 und szzp2 lautet

Vxx = „V“ +  szzp\<sub\>1\</sub\>  + „_„  + szzp\<sub\>2\</sub\>

Relevant sind dafür nur die einem Aufrufer sichtbaren SZZPs (auch als
„logischer SZZP“ bezeichnet), nicht einzelne physische Instanzen, die
gemeinsam zur Verfügbarkeit des SZZPs beitragen. Die konkreten Bezeichner für
die logischen SZZPs sind mit gematik Betrieb (Operations) abzustimmen. szzp1
sei immer der Bezeichner, der in alphanumerischer Sortierung vor szzp2 liegt.

Beispiel: PDT08-S01-D3-G10-V0001_0007

Das Zentrale Netz erfasst gemäß [gemSpec_Perf#GS-A_5014] an seinen Sicheren
Zentralen Zugangspunkten (SZZP) die Datenmengen getrennt nach Richtungen Rxx.
Dabei gibt die Richtung Rxx an, welche Dienstinstanz betroffen ist und ob der
Fluss zur Instanz hin (Rz) oder von der Instanz weg (Rv) erfolgt.

Der Bezeichner Rxx setzt sich zusammen aus „Rz“ für die Richtung zur
Dienstinstanz hin und „Rv“ für die Richtung von der Dienstinstanz weg
sowie einem Bezeichner für die Dienstinstanz. Der Bezeichner für die
Dienstinstanz setzt sich aus drei durch "_" getrennten Teilen zusammen. Einem
Bezeichner für den logischen SZZP, einem Bezeichner für den Produkttypen und
einem Bezeichner für den Anbieter des Dienstes. Die konkreten Bezeichner für
die logischen SZZPs und Anbieter sind mit gematik Betrieb (Operations)
abzustimmen. Die Bezeichner für die Produkttypen gibt Tabelle
Tab_gemKPT_Betr_Produkttypen vor.Beispiel: PDT08-S11-D1-G02-Rv0001_PDT04_ARVTO

Für die VSDM-Produkttypen erfolgt abweichend zu [gemSpec_Perf#GS-A_5014] die
Volumenerfassung für die VSDM-Produkttypen pro SZZP in Summe über Anbieter
und VSDM-Produkttypen (nur aufgeschlüsselt nach Richtung).Damit die Syntax der
Bezeichner auch für diesen Ausnahmefall erhalten bleibt, wird als
Produkttypbezeichner „VSDM“ gesetzt und als Anbieterbezeichner
„XXXXX“.Beispiel:  PDT08-S11-D1-G02-Rz0035_VSDM_XXXXX

Für den Produkttyp VPN-Zugangsdienst werden zur Unterscheidung einzelner
VPN-Konzentratoren zwei weitere Bezeichnungen VPNK-TI_X (VPN-Konzentrator TI)
und VPNK-SIS_X (VPN-Konzentrator SIS) eingeführt. Der Platzhalter „X“ ist
ein eindeutiger Bezeichner eines VPN-Konzentrators und wird durch den Anbieter
des VPN-Zugangsdienstes vergeben. Es sind 32 Zeichen zulässig. 

Beispiel: PDT09-S11-D1-G03-VPNK-TI_vpnk1.fra.providerx.de

Tabelle Tab_gemKPT_Betr_Beispiel_Rohdaten zeigt exemplarisch die in zwei
Erfassungszeiträumen gemessenen Performance-Daten zu einzelnen Anfragen und
Tabelle Tab_gemKPT_Betr_Beispiel_Performance_Kenngroessen die aus diesen
generierten Performance-Kenngrößen.

<table><tr><th>
ID

</th><th>
Performance-Dimension

</th></tr><tr><td>
D1

</td><td>
Last

</td></tr><tr><td>
D2

</td><td>
Bearbeitungszeit

</td></tr><tr><td>
D3

</td><td>
Verfügbarkeit

</td></tr></table>

<table><tr><th>
ID

</th><th>
Größe

</th><th>
Einheit

</th></tr><tr><td colspan="3" rowspan="1">
Dimension Last

</td></tr><tr><td>
D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum.

</td><td>
Integer

</td></tr><tr><td>
D1-G02

</td><td>
Datenmenge [kByte] pro Richtung.

</td><td>
Integer

</td></tr><tr><td>
D1-G03

</td><td>
Datenmenge [kByte] in Richtung zum Internet.

</td><td>
Integer

</td></tr><tr><td>
D1-G04

</td><td>
Datenmenge [kByte] in Richtung vom Internet.

</td><td>
Integer

</td></tr><tr><td>
D1-G05

</td><td>
Anzahl der bestehenden VPN-Tunnel.

</td><td>
Integer

</td></tr><tr><td>
D1-G06

</td><td>
Anzahl der neu aufgebauten VPN-Tunnel.

</td><td>
Integer

</td></tr><tr><td>
D1-G07

</td><td>
Anzahl der abgebauten VPN-Tunnel.

</td><td>
Integer

</td></tr><tr><td>
D1-G08

</td><td>
Mittlerer Datendurchsatz pro Richtung in Mbits/s im Erfassungszeitraum.

</td><td>
Integer

</td></tr><tr><td>
D1-G09

</td><td>
Anzahl der im Erfassungszeitraum abgelehnten Aufrufe.

</td><td>
Integer

</td></tr><tr><td colspan="3" rowspan="1">
Dimension Bearbeitungszeit

</td></tr><tr><td>
D2-G03

</td><td>
Anzahl der Summierten Bearbeitungszeiten.

</td><td>
Integer

</td></tr><tr><td>
D2-G04

</td><td>
Summe der Bearbeitungszeiten [msec] im Erfassungszeitraum.

</td><td>
Integer

</td></tr><tr><td>
D2-G05

</td><td>
Anzahl der Bearbeitungszeiten größer als die 99%-Quantilschranke des
Produkttyps.

</td><td>
Integer

</td></tr><tr><td>
D2-G06

</td><td>
Mittel der RoundtripTime für IP-Pakete über alle Verbindungen von
Anschlusspunkt zu Anschlusspunkt. [msec]

</td><td>
Integer

</td></tr><tr><td>
D2-G07

</td><td>
Verlustrate in % für IP-Pakete am Anschlusspunkt. Dieser Wert ist für alle
Anschlusspunkte der Anbindungsvarianten SZZP, SZZP-light und Sicherheitsgateway
Bestandsnetze zu ermitteln. Gemessen wird für SZZP jeweils an der
Schnittstelle Richtung TI. Für SZZP-light und Sicherheitsgateway Bestandsnetze
erfolgt die Messung an der Schnittstelle Richtung Internet am
VPN-Anschlusspunkt und am VPN-Konzentrator.

</td><td>
Integer

</td></tr><tr><td>
D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat. [msec]

</td><td>
Integer

</td></tr><tr><td>
D2-G24

</td><td>
Anzahl der Bearbeitungszeiten größer als die 95%-Quantilschranke des
Produkttyps.

</td><td>
Integer

</td></tr><tr><td>
D2-G27

</td><td>
Summe der Bearbeitungszeiten im Erfassungszeitraum, gemessen zwischen dem
Zeitpunkt der quittierten Übergabe vom KOM-LE Clientmodul an den
KOM-LE-Fachdienst des Email-Senders und dem Zeitpunkt der quittierten Übergabe
an den KOM-LE Fachdienst des Email-Empfängers. [sec]

</td><td>
Integer

</td></tr><tr><td>
D2-G28

</td><td>
Größte Bearbeitungszeit im Erfassungszeitraum, gemessen zwischen dem Zeitpunkt
der quittierten Übergabe vom KOM-LE Clientmodul an den KOM-LE-Fachdienst des
Email-Senders und dem Zeitpunkt der quittierten Übergabe an den KOM-LE
Fachdienst des Email-Empfängers. [sec]

</td><td>
Integer

</td></tr><tr><td>
D2-G29

</td><td>
Anzahl der Bearbeitungszeiten mit Überschreitung der Bearbeitungszeitvorgabe.

</td><td>
Integer

</td></tr><tr><td>
D2-G30

</td><td>
Maximale Bearbeitungszeit

</td><td>
Integer

</td></tr><tr><td>
D2-G31

</td><td>
Anteil Bearbeitungen innerhalb der Bearbeitungszeitvorgabe

</td><td>
Integer

</td></tr><tr><td colspan="3" rowspan="1">
Dimension Verfügbarkeit

</td></tr><tr><td>
D3-G10

</td><td>
Startzeitpunkt eines Ausfalls.

</td><td>
Zeitstempel

(Auflösung sec)

</td></tr><tr><td>
D3-G11

</td><td>
Endezeitpunkt eines Ausfalls.

</td><td>
Zeitstempel

(Auflösung sec)

</td></tr><tr><td>
D3-G12

</td><td>
Verfügbarkeit pro Monat. [%*1000]

</td><td>
Integer

</td></tr><tr><td>
D3-G14

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit. [%*1000]

</td><td>
Integer

</td></tr><tr><td>
D3-G16

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit. [%*1000]

</td><td>
Integer

</td></tr><tr><td>
D3-G14R

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit. [%*1000] in der RU/TU

</td><td>
Integer

</td></tr><tr><td>
D3-G16R

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit. [%*1000] in der RU/TU

</td><td>
Integer

</td></tr><tr><td>
D3-G18

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit über alle IP-Verbindungen zwischen SZZPs
der angeschlossenen Produkttypen der TI, bei denen mindestens ein Zugangspunkt
mit der Anschlussoption „einfache Anbindung“ angebunden ist. [%*1000]

</td><td>
Integer

</td></tr><tr><td>
D3-G19

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit, gemittelt über alle IP-Verbindungen
zwischen allen SZZPs mit der Anschlussoption „redundante Anbindung“
angeschlossenen Produkttypen der TI. [%*1000]

</td><td>
Integer

</td></tr><tr><td>
D3-G22

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit, gemittelt über alle IP-Verbindungen
zwischen allen SZZPs mit der Anschlussoption „redundante Anbindung“
angeschlossenen Produkttypen der TI. [%*1000]

</td><td>
Integer

</td></tr><tr><td>
D3-G25

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit über alle IP-Verbindungen zwischen SZZPs
der angeschlossenen Produkttypen der TI, bei denen mindestens ein Zugangspunkt
mit der Anschlussoption „einfache Anbindung“ angebunden ist. [%*1000]

</td><td>
Integer

</td></tr><tr><td>
D3-G26

</td><td>
Anzahl der Tage pro Monat mit einer Gesamt-Ausfalldauer größer einer Stunde in
der Hauptzeit

</td><td>
Integer

</td></tr></table>

<table><tr><th>
ID

</th><th>
Produkttyp / Anwendungstyp

</th><th>
Produkttyp-Name / Anwendungsname

</th></tr><tr><td>
PDT01

</td><td>
gemProdT_OCSP_Proxy

</td><td>
OCSP-Responder-Proxy

</td></tr><tr><td>
PDT02

</td><td>
gemProdT_X.509_TSP_QES

</td><td>
Trust Service Provider X.509 QES

</td></tr><tr><td>
PDT03

</td><td>
gemProdT_X.509_TSP_nonQES_eGK

</td><td>
Trust Service Provider X.509 nonQES - eGK

</td></tr><tr><td>
PDT04

</td><td>
gemProdT_TSL

</td><td>
TSL-Dienst

</td></tr><tr><td>
PDT05

</td><td>
gemProdT_St_Ampel

</td><td>
Störungsampel

</td></tr><tr><td>
PDT06

</td><td>
gemProdT_NamD

</td><td>
Namensdienst

</td></tr><tr><td>
PDT07

</td><td>
gemProdT_ZeitD

</td><td>
Zeitdienst

</td></tr><tr><td>
PDT08

</td><td>
gemProdT_ZentrNetz

</td><td>
Zentrales Netz der TI

</td></tr><tr><td>
PDT09

</td><td>
gemProdT_VPN_ZugD

</td><td>
VPN-Zugangsdienst

</td></tr><tr><td>
PDT10

</td><td>
gemProdT_SG_BestNetze

</td><td>
Sicherheitsgateway für Bestandsnetze

</td></tr><tr><td>
PDT11

</td><td>
gemProdT_KSR

</td><td>
Konfigurationsdienst

</td></tr><tr><td>
PDT12

</td><td>
gemProdT_eGK

</td><td>
eGK

</td></tr><tr><td>
PDT13

</td><td>
gemProdT_HBA

</td><td>
HBA

</td></tr><tr><td>
PDT14

</td><td>
gemProdT_SMC-B

</td><td>
SMC-B

</td></tr><tr><td>
PDT15

</td><td>
gemProdT_SMC-K

</td><td>
SMC-K

</td></tr><tr><td>
PDT16

</td><td>
gemProdT_SMC-KT

</td><td>
SMC-KT

</td></tr><tr><td>
PDT17

</td><td>
gemProdT_Kon

</td><td>
Konnektor

</td></tr><tr><td>
PDT18

</td><td>
gemProdT_KT

</td><td>
eHealth-Kartenterminal

</td></tr><tr><td>
PDT19

</td><td>
gemProdT_MobKT

</td><td>
Mobiles Kartenterminal

</td></tr><tr><td>
PDT20

</td><td>
gemProdT_FD_VSDM 

</td><td>
Fachdienste VSDM (UFS)

</td></tr><tr><td>
PDT21

</td><td>
gemProdT_Intermediär_VSDM 

</td><td>
Intermediär VSDM

</td></tr><tr><td>
PDT22

</td><td>
gemProdT_gematik_Root_CA 

</td><td>
gematik-Root-CA

</td></tr><tr><td>
PDT23

</td><td>
gemProdT_FD_VSDM 

</td><td>
Fachdienst VSDM (VSDD)

</td></tr><tr><td>
PDT24

</td><td>
gemProdT_FD_KOMLE 

</td><td>
Fachdienst KOM-LE

</td></tr><tr><td>
PDT25

</td><td>
gemProdT_VZD 

</td><td>
Verzeichnisdienst

</td></tr><tr><td>
PDT26

</td><td>
gemProdT_FD_VSDM

</td><td>
Fachdienst VSDM (CMS)

</td></tr><tr><td>
PDT27

</td><td>
gemProdT_CM_KOMLE 

</td><td>
KOM-LE-Clientmodul

</td></tr><tr><td>
PDT29

</td><td>
gemProdT_FM_VSDM

</td><td>
Fachmodul VSDM

</td></tr><tr><td>
PDT31

</td><td>
gemProdT_CVC_TSP

</td><td>
Trust Service Provider CVC

</td></tr><tr><td>
PDT32

</td><td>
gemProdT_CVC-Root

</td><td>
CVC-Root

</td></tr><tr><td>
PDT33

</td><td>
gemProdT_HSM-B

</td><td>
HSM-B

</td></tr><tr><td>
PDT34

</td><td>
gemProdT_mobKT_VSDM

</td><td>
Fachmodul VSDM (mobKT)

</td></tr><tr><td>
PDT35

</td><td>
gemProdT_KTR-AdV_Server

</td><td>
Komponente AdV-Server der KTR-AdV

</td></tr><tr><td>
PDT36

</td><td>
gemProdT_X.509_TSP_nonQES_HBA

</td><td>
Trust Service Provider X.509 nonQES - HBA

</td></tr><tr><td>
PDT37

</td><td>
gemProdT_X.509_TSP_nonQES_Komp

</td><td>
Trust Service Provider X.509 nonQES – Komponentenzertifikate

</td></tr><tr><td>
PDT38

</td><td>
gemProdT_X.509_TSP_nonQES_SMC-B

</td><td>
Trust Service Provider X.509 nonQES – SMC-B

</td></tr><tr><td>
PDT39

</td><td>
gemProdT_HBA_G2.1

</td><td>
HBA_G2.1

</td></tr><tr><td>
PDT40

</td><td>
gemProdT_SMC-B_G2.1

</td><td>
SMC-B_G2.1

</td></tr><tr><td>
PDT41

</td><td>
gemProdT_ServiceMon

</td><td>
Service Monitoring

</td></tr><tr><td>
PDT42

</td><td>
gemProdT_KTR-AdV-Terminal

</td><td>
KTR-AdV-Terminal

(ungültig, historisch)

</td></tr><tr><td>
PDT43

</td><td>
gemProdT_Aktensystem_ePA

</td><td>
ePA-Aktensystem

</td></tr><tr><td>
PDT44

</td><td>
gemProdT_ePA_FdV

</td><td>
ePA-Frontend des Versicherten

</td></tr><tr><td>
PDT45

</td><td>
gemProdT_Basis-Consumer

</td><td>
Basis-Consumer

</td></tr><tr><td>
PDT46

</td><td>
gemProdT_KTR-Consumer

</td><td>
KTR-Consumer

</td></tr><tr><td>
PDT47

</td><td>
gemProdT_SigD

</td><td>
Signaturdienst

</td></tr><tr><td>
PDT48

</td><td>
gemProdT_SGD_ePA

</td><td>
Schlüsselgenerierungsdienst

</td></tr><tr><td>
PDT49

</td><td>
gemProdT_ePA-Modul_FdV

</td><td>
ePA-Modul Frontend des Versicherten

</td></tr><tr><td>
PDT50

</td><td>
gemProdT_eRp_FD

</td><td>
E-Rezept-Fachdienst

</td></tr><tr><td>
PDT51

</td><td>
gemProdT_eRp_FdV

</td><td>
E-Rezept-Frontend des Versicherten

</td></tr><tr><td>
PDT52

</td><td>
gemProdT_IDP-Dienst

</td><td>
Identity Provider Dienst

</td></tr><tr><td>
PDT53

</td><td>
IdP-Modul 

</td><td>
Identity Provider Modul 

</td></tr><tr><td>
PDT54

</td><td>
aAdG 

</td><td>
Weitere Anwendung aAdG

</td></tr><tr><td>
PDT55

</td><td>
aAdG-NetG-TI 

</td><td>
Weitere Anwendung aAdG-NetGTI

</td></tr><tr><td>
PDT56

</td><td>
aAdG-NetG 

</td><td>
Weitere Anwendung aAdG-NetG

</td></tr><tr><td>
PDT57

</td><td>
AS-SGW aAdG-NetG

</td><td>
Weitere Anwendung aAdG-NetG (mit aktiver Option Anbieter Anschlusspunkt)

</td></tr><tr><td>
PDT64

</td><td>
gemProdT_TIM_FD

</td><td>
TI-Messenger Fachdienst

</td></tr><tr><td>
PDT65

</td><td>
gemProdT_TIM_Client

</td><td>
TI-Messenger Client

</td></tr><tr><td>
PDT66

</td><td>
gemProdT_VZD_FHIR

</td><td>
Verzeichnisdienst FHIR-Directory

</td></tr></table>

<table><tr><th>
Produkttyp / Anwen-dungstyp

</th><th>
ID

</th><th>
Schnittstellen::Operation

</th><th>
Berichtsformat-Alias (sofern von Schnittstellen::Operation abweichend)

</th></tr><tr><td>
PDT01

</td><td>
S06

</td><td>
I_OCSP_Status_Information::check_Revocation_Status(P::Zertifikatstyp)

</td></tr><tr><td>
PDT02

</td><td>
S06

</td><td>
I_OCSP_Status_Information::check_Revocation_Status(P::Zertifikatstyp)

</td></tr><tr><td>
PDT03

</td><td>
S06

</td><td>
I_OCSP_Status_Information::check_Revocation_Status(P::Zertifikatstyp)

</td></tr><tr><td>
PDT04

</td><td>
S06

</td><td>
I_OCSP_Status_Information::check_Revocation_Status(P::Zertifikatstyp)

</td></tr><tr><td>
PDT04

</td><td>
S12

</td><td>
I_TSL_Download

</td></tr><tr><td>
PDT04

</td><td>
S17

</td><td>
I_BNetzA_VL_Download::download_VL

</td></tr><tr><td>
PDT05

</td><td>
S01

</td><td>
I*

</td></tr><tr><td>
PDT06

</td><td>
S07

</td><td>
I_DNS_Service_Localization

</td></tr><tr><td>
PDT06

</td><td>
S08

</td><td>
I_DNS_Name_Resolution::get_IP_Address

</td></tr><tr><td>
PDT06

</td><td>
S09

</td><td>
I_DNS_Name_Resolution::get_FQDN

</td></tr><tr><td>
PDT07

</td><td>
S13

</td><td>
I_NTP_Time_Information

</td></tr><tr><td>
PDT08

</td><td>
S01

</td><td>
I*

</td></tr><tr><td>
PDT08

</td><td>
S10

</td><td>
I_IP_Transport(P::Verbindung)

</td></tr><tr><td>
PDT08

</td><td>
S11

</td><td>
I_IP_Transport(P::Verbindung+Richtung)

</td></tr><tr><td>
PDT09

</td><td>
S01

</td><td>
I*

</td></tr><tr><td>
PDT09

</td><td>
S08

</td><td>
I_DNS_Name_Resolution::get_IP_Address

</td></tr><tr><td>
PDT09

</td><td>
S13

</td><td>
I_NTP_Time_Information

</td></tr><tr><td>
PDT09

</td><td>
S15

</td><td>
I_Secure_Channel_Tunnel

</td></tr><tr><td>
PDT10

</td><td>
S14

</td><td>
I_Secure_Access_Bestandsnetz

</td></tr><tr><td>
PDT11

</td><td>
S02

</td><td>
I_KSRS_Download::list_Updates

</td></tr><tr><td>
PDT11

</td><td>
S04

</td><td>
I_KSRS_Download::get_Updates

</td></tr><tr><td>
PDT21

</td><td>
S01

</td><td>
I*

</td></tr><tr><td>
PDT22

</td><td>
S06

</td><td>
I_OCSP_Status_Information::check_Revocation_Status(P::Zertifikatstyp)

</td></tr><tr><td>
PDT24

</td><td>
S01

</td><td>
I*

</td></tr><tr><td>
PDT25

</td><td>
S01

</td><td>
I*

</td></tr><tr><td>
PDT25

</td><td>
S16

</td><td>
I_Directory_Query

</td></tr><tr><td>
PDT35

</td><td>
S01

</td><td>
I*

</td></tr><tr><td>
PDT37

</td><td>
S18

</td><td>
I_CRL_Download

</td></tr><tr><td>
PDT43

</td><td>
S01

</td><td>
I_Authentication

</td></tr><tr><td>
PDT43

</td><td>
S02

</td><td>
I_Authentication_Insurant::Login

</td><td>
I_Authentication_Insurant::login

</td></tr><tr><td>
PDT43

</td><td>
S03

</td><td>
I_Authentication_Insurant::Renew

</td><td>
I_Authentication_Insurant::renew

</td></tr><tr><td>
PDT43

</td><td>
S04

</td><td>
I_Authentication_Insurant::Logout

</td><td>
I_Authentication_Insurant::logout

</td></tr><tr><td>
PDT43

</td><td>
S05

</td><td>
I_Authorization

</td></tr><tr><td>
PDT43

</td><td>
S06

</td><td>
I_Authorization::getAuthorizationKey

</td></tr><tr><td>
PDT43

</td><td>
S07

</td><td>
I_Authorization_Insurant:: getAuthorizationKey

</td></tr><tr><td>
PDT43

</td><td>
S08

</td><td>
I_Document_Management

</td></tr><tr><td>
PDT48

</td><td>
S01

</td><td>
I*

</td></tr><tr><td>
PDT48

</td><td>
S02

</td><td>
GetPublicKey

</td><td>
SGD.getPublicKey

</td></tr><tr><td>
PDT47

</td><td>
S01

</td><td>
I*

</td></tr><tr><td>
PDT47

</td><td>
S02

</td><td>
I_Remote_Sign_Operations::sign_Data

</td><td>
SigD.sign_Data

</td></tr></table>

<table><tr><th>
Produkttyp / Anwendungstyp

</th><th>
ID

</th><th>
Anwendungsfall

</th><th>
Berichtsformat-Alias

</th></tr><tr><td>
PDT50

</td><td>
A01

</td><td>
ERP* 

</td></tr><tr><td>
PDT50

</td><td>
A02

</td><td>
ERP.UC_2_1

</td></tr><tr><td>
PDT50

</td><td>
A03

</td><td>
ERP.UC_2_3

</td></tr><tr><td>
PDT50

</td><td>
A04

</td><td>
ERP.UC_3_1

</td></tr><tr><td>
PDT50

</td><td>
A05

</td><td>
ERP.UC_3_3

</td></tr><tr><td>
PDT50

</td><td>
A07

</td><td>
ERP.UC_4_1

</td></tr><tr><td>
PDT50

</td><td>
A08

</td><td>
ERP.UC_4_4

</td></tr><tr><td>
PDT50

</td><td>
A09

</td><td>
ERP.UC_4_7

</td></tr><tr><td>
PDT52

</td><td>
A01

</td><td>
IDP*

</td></tr><tr><td>
PDT52

</td><td>
A02

</td><td>
IDP.UC_1

</td></tr><tr><td>
PDT52

</td><td>
A03

</td><td>
IDP.UC_2

</td></tr><tr><td>
PDT52

</td><td>
A04

</td><td>
IDP.UC_3

</td></tr><tr><td>
PDT52

</td><td>
A05

</td><td>
IDP.UC_4

</td></tr><tr><td>
PDT52

</td><td>
A06

</td><td>
IDP.UC_5

</td></tr><tr><td>
PDT52

</td><td>
A07

</td><td>
IDP.UC_6

</td></tr><tr><td>
PDT52

</td><td>
A08

</td><td>
IDP.UC_7

</td></tr><tr><td>
PDT52

</td><td>
A09

</td><td>
IDP.UC_8

</td></tr><tr><td>
PDT52

</td><td>
A10

</td><td>
IDP.UC_9

</td></tr><tr><td>
PDT52

</td><td>
A11

</td><td>
IDP.UC_10

</td></tr><tr><td>
PDT43

</td><td>
A01

</td><td>
ePA.UC_1

</td><td>
VAU_Context

</td></tr><tr><td>
PDT48

</td><td>
A01

</td><td>
SGD.UC_1

</td><td>
SGD.getAuthenticationToken, SGD.KeyDerivation

</td></tr></table>

<table><tr><th>
ID

</th><th>
Zertifikatstypen

</th></tr><tr><td>
Z01

</td><td>
HBA-Zertifikate (C.HP.QES): Root-Zert

</td></tr><tr><td>
Z02

</td><td>
HBA-Zertifikate (C.HP.QES): CA-Zert

</td></tr><tr><td>
Z03

</td><td>
HBA-Zertifikate (C.HP.QES): EE-Zert

</td></tr><tr><td>
Z04

</td><td>
eGK-Zertifikate (C.CH.AUT)

</td></tr><tr><td>
Z05

</td><td>
SMC-B-Zertifikate (C.HCI.OSIG)

</td></tr><tr><td>
Z06

</td><td>
HBA-Zertifikate (C.HP.ENC)

</td></tr><tr><td>
Z07

</td><td>
SMC-B Zertifikate (C.HCI.ENC)

</td></tr><tr><td>
Z08

</td><td>
Konnektor-Zertifikate (SMC-K, C.NK.VPN)

</td></tr><tr><td>
Z09

</td><td>
SMC-B-Zertifikate (C.HCI.AUT)

</td></tr><tr><td>
Z10

</td><td>
TLS Zertifikate der zentralen Dienste (C.ZD.TLS)

</td></tr><tr><td>
Z11

</td><td>
TLS Zertifikate der Fachdienste (C.FD.TLS)

</td></tr><tr><td>
Z12

</td><td>
TSL-Signerzertifikat

</td></tr><tr><td>
Z13

</td><td>
HBA-Zertifikate (C.HP.AUT)

</td></tr><tr><td>
Z14

</td><td>
HBA-Zertifikate (C.HP.AUT): CA-Zert

</td></tr><tr><td>
Z16

</td><td>
SMC-B-Zertifikate (C.HCI.AUT): CA-Zert

</td></tr><tr><td>
Z17

</td><td>
SMC-B-Zertifikate (C.HCI.ENC): CA-Zert

</td></tr><tr><td>
Z18

</td><td>
HBA-Zertifikate (C.HP.ENC): CA-Zert

</td></tr><tr><td>
Z19

</td><td>
gematikRoot-CA-Zert

</td></tr><tr><td>
Z20

</td><td>
Sonstige oben nicht genannte Zertifikate (z.B. für HBA-Vorläuferkarten)

</td></tr></table>

<table><tr><th>
ID

</th><th>
Aufrufquelle

</th></tr><tr><td>
Q1

</td><td>
aus der TI

</td></tr><tr><td>
Q2

</td><td>
aus dem Internet

</td></tr></table>

<table><tr><th colspan="7" rowspan="1">
Produkttyp - Schnittstelle

</th></tr><tr><td>
Performance-

Kenngröße

</td><td>
Performance-Grösse

</td><td>
Störungs-

ampel

</td><td>
Service-

Level-

Report

</td><td>
Performance-

Report

</td><td>
Reports auf Basis Rohdaten

</td><td>
Reports auf Basis Service Monitoring

</td></tr><tr><td colspan="7" rowspan="1">
AdV-Server

</td></tr><tr><td>
PDT35-S01-D3-G10

</td><td>
Startzeitpunkt eines Ausfalls

</td><td>
 

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT35-S01-D3-G11

</td><td>
Endezeitpunkt eines Ausfalls

</td><td>
 

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT35-S01-D3-G14

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT35-S01-D3-G16

 

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td colspan="7" rowspan="1">
OCSP-Proxy

- I_OCSP_Status_Information::check_Revocation_Status(P::Zertifikatstyp)

</td></tr><tr><td>
PDT01-S06-D1-G01-Z20

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
 

</td><td>
 

</td><td>
</td></tr><tr><td>
PDT01-S06-D2-G03-Z20

</td><td>
Anzahl der Summierten Bearbeitungszeiten

</td><td>
</td><td>
 

</td><td>
</td></tr><tr><td>
PDT01-S06-D2-G04-Z20

</td><td>
Summe der Bearbeitungszeiten im Erfassungszeitraum

</td><td>
</td><td>
 

</td><td>
</td></tr><tr><td>
PDT01-S06-D2-G05-Z20

</td><td>
Anzahl der Bearbeitungszeiten größer als die 99%-Quantilschranke des
Produkttyps

</td><td>
</td><td>
 

</td><td>
</td></tr><tr><td>
PDT01-S06-D2-G08-Z20

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT01-S06-D3-G10-Z20

</td><td>
Startzeitpunkt eines Ausfalls

</td><td>
</td><td>
 

</td><td>
</td></tr><tr><td>
PDT01-S06-D3-G11-Z20

</td><td>
Endezeitpunkt eines Ausfalls

</td><td>
</td><td>
 

</td><td>
</td></tr><tr><td>
PDT01-S06-D3-G14-Z20

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT01-S06-D3-G16-Z20

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td colspan="7" rowspan="1">
TSP-X.509QES

- I_OCSP_Status_Information::check_Revocation_Status(P::Zertifikatstyp)

</td></tr><tr><td>
PDT02-S06-D1-G01-Z03-Qy

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
 

</td><td>
 

</td><td>
</td></tr><tr><td>
PDT02-S06-D2-G03-Z03-Qy

</td><td>
Anzahl der Summierten Bearbeitungszeiten

</td><td>
</td><td>
 

</td><td>
</td></tr><tr><td>
PDT02-S06-D2-G04-Z03-Qy

</td><td>
Summe der Bearbeitungszeiten im Erfassungszeitraum

</td><td>
</td><td>
 

</td><td>
</td></tr><tr><td>
PDT02-S06-D2-G05-Z03-Qy

</td><td>
Anzahl der Bearbeitungszeiten größer als die 99%-Quantilschranke des
Produkttyps

</td><td>
</td><td>
 

</td><td>
</td></tr><tr><td>
PDT02-S06-D2-G08-Z03-Qy

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT02-S06-D3-G10-Z03-Qy

</td><td>
Startzeitpunkt eines Ausfalls

</td><td>
</td><td>
 

</td><td>
</td></tr><tr><td>
PDT02-S06-D3-G11-Z03-Qy

</td><td>
Endezeitpunkt eines Ausfalls

</td><td>
</td><td>
 

</td><td>
</td></tr><tr><td>
PDT02-S06-D3-G14-Z03-Qy

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT02-S06-D3-G16-Z03-Qy

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td colspan="7" rowspan="1">
TSP-X.509nonQES

- I_OCSP_Status_Information::check_Revocation_Status(P::Zertifikatstyp)

</td></tr><tr><td>
PDT03-S06-D1-G01-Zxx-Qy

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
 

</td><td>
 

</td><td>
</td></tr><tr><td>
PDT03-S06-D2-G03-Zxx-Qy

</td><td>
Anzahl der Summierten Bearbeitungszeiten

</td><td>
</td><td>
 

</td><td>
</td></tr><tr><td>
PDT03-S06-D2-G04-Zxx-Qy

</td><td>
Summe der Bearbeitungszeiten im Erfassungszeitraum

</td><td>
</td><td>
 

</td><td>
</td></tr><tr><td>
PDT03-S06-D2-G05-Zxx-Qy

</td><td>
Anzahl der Bearbeitungszeiten größer als die 99%-Quantilschranke des
Produkttyps

</td><td>
</td><td>
 

</td><td>
</td></tr><tr><td>
PDT03-S06-D2-G08-Zxx-Qy

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT03-S06-D3-G10-Zxx-Qy

</td><td>
Startzeitpunkt eines Ausfalls

</td><td>
</td><td>
 

</td><td>
</td></tr><tr><td>
PDT03-S06-D3-G11-Zxx-Qy

</td><td>
Endezeitpunkt eines Ausfalls

</td><td>
</td><td>
 

</td><td>
</td></tr><tr><td>
PDT03-S06-D3-G14-Zxx-Qy

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT03-S06-D3-G16-Zxx-Qy

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td colspan="7" rowspan="1">
TSL-Dienst

- I_OCSP_Status_Information::check_Revocation_Status(P::Zertifikatstyp)

</td></tr><tr><td>
PDT04-S06-D1-G01-Z12

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
 

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT04-S06-D2-G03-Z12

</td><td>
Anzahl der Summierten Bearbeitungszeiten

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT04-S06-D2-G04-Z12

</td><td>
Summe der Bearbeitungszeiten im Erfassungszeitraum

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT04-S06-D2-G05-Z12

</td><td>
Anzahl der Bearbeitungszeiten größer als die 99%-Quantilschranke des
Produkttyps

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT04-S06-D2-G08-Z12

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT04-S06-D3-G10-Z12

</td><td>
Startzeitpunkt eines Ausfalls

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT04-S06-D3-G11-Z12

</td><td>
Endezeitpunkt eines Ausfalls

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT04-S06-D3-G12-Z12

</td><td>
Verfügbarkeit pro Monat

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td colspan="7" rowspan="1">
TSL-Dienst

- I_TSL_Download

</td></tr><tr><td>
PDT04-S12-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
 

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT04-S12-D3-G10

</td><td>
Startzeitpunkt eines Ausfalls

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT04-S12-D3-G11

</td><td>
Endezeitpunkt eines Ausfalls

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT04-S12-D3-G12

</td><td>
Verfügbarkeit pro Monat

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td colspan="7" rowspan="1">
TSL-Dienst

- I_BNetzA_VL_Download::download_VL

</td></tr><tr><td>
PDT04-S17-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
 

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT04-S17-D3-G10

</td><td>
Startzeitpunkt eines Ausfalls

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT04-S17-D3-G11

</td><td>
Endezeitpunkt eines Ausfalls

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT04-S17-D3-G12

</td><td>
Verfügbarkeit pro Monat

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td colspan="7" rowspan="1">
TSP-X.509nonQES  - Komponentenzertifikate, CRL-Dienst – I_CRL_Download

</td></tr><tr><td>
PDT37-S18-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT37-S18-D3-G10

</td><td>
Startzeitpunkt eines Ausfalls

</td><td>
x

</td><td>
x

</td></tr><tr><td>
PDT37-S18-D3-G11

</td><td>
Endezeitpunkt eines Ausfalls

</td><td>
x

</td><td>
x

</td></tr><tr><td>
PDT37-S18-D3-G12

</td><td>
Verfügbarkeit pro Monat

</td><td>
x

</td></tr><tr><td colspan="7" rowspan="1">
Störungsampel

</td></tr><tr><td>
PDT05-S01-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
 

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT05-S01-D3-G10

</td><td>
Startzeitpunkt eines Ausfalls

</td><td>
 

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT05-S01-D3-G11

</td><td>
Endezeitpunkt eines Ausfalls

</td><td>
 

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT05-S01-D3-G14

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT05-S01-D3-G16

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td colspan="7" rowspan="1">
Namensdiens

t - I_DNS_Service_Localization

</td></tr><tr><td>
PDT06-S07-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
 

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT06-S07-D2-G03

</td><td>
Anzahl der Summierten Bearbeitungszeiten

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT06-S07-D2-G04

</td><td>
Summe der Bearbeitungszeiten im Erfassungszeitraum

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT06-S07-D2-G05

</td><td>
Anzahl der Bearbeitungszeiten größer als die 99%-Quantilschranke des
Produkttyps

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT06-S07-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT06-S07-D3-G10

</td><td>
Startzeitpunkt eines Ausfalls

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT06-S07-D3-G11

</td><td>
Endezeitpunkt eines Ausfalls

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT06-S07-D3-G14

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT06-S07-D3-G16

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td colspan="7" rowspan="1">
Namensdiens

t - I_DNS_Name_Resolution::get_IP_Address

</td></tr><tr><td>
PDT06-S08-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
 

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT06-S08-D2-G03

</td><td>
Anzahl der Summierten Bearbeitungszeiten

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT06-S08-D2-G04

</td><td>
Summe der Bearbeitungszeiten im Erfassungszeitraum

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT06-S08-D2-G05

</td><td>
Anzahl der Bearbeitungszeiten größer als die 99%-Quantilschranke des
Produkttyps

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT06-S08-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT06-S08-D3-G10

</td><td>
Startzeitpunkt eines Ausfalls

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT06-S08-D3-G11

</td><td>
Endezeitpunkt eines Ausfalls

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT06-S08-D3-G14

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT06-S08-D3-G16

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td colspan="7" rowspan="1">
Namensdiens

t - I_DNS_Name_Resolution::get_FQDN

</td></tr><tr><td>
PDT06-S09-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
 

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT06-S09-D3-G10

</td><td>
Startzeitpunkt eines Ausfalls

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT06-S09-D3-G11

</td><td>
Endezeitpunkt eines Ausfalls

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT06-S09-D3-G14

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT06-S09-D3-G16

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td colspan="7" rowspan="1">
Zeitdienst

- I_NTP_Time_Information

</td></tr><tr><td>
PDT07-S13-D3-G10

</td><td>
Startzeitpunkt eines Ausfalls

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT07-S13-D3-G11

</td><td>
Endezeitpunkt eines Ausfalls

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT07-S13-D3-G12

</td><td>
Verfügbarkeit pro Monat

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td colspan="7" rowspan="1">
Zentrales Netz

</td></tr><tr><td>
PDT08-S01-D2-G06

</td><td>
Mittel der RoundtripTime für IP-Pakete über alle Verbindungen von
Anschlusspunkt zu Anschlusspunkt

</td><td>
x

</td><td>
x

</td><td>
x

</td></tr><tr><td>
PDT08-S01-D2-G07

</td><td>
Verlustrate in % für IP-Pakete am Anschlusspunkt. Dieser Wert ist für alle
Anschlusspunkte der Anbindungsvarianten SZZP, SZZP-light und Sicherheitsgateway
Bestandsnetze zu ermitteln. Gemessen wird für SZZP jeweils an der
Schnittstelle Richtung TI. Für SZZP-light und Sicherheitsgateway Bestandsnetze
erfolgt die Messung an der Schnittstelle Richtung Internet am
VPN-Anschlusspunkt und am VPN-Konzentrator.

</td><td>
x

</td><td>
x

</td><td>
x

</td></tr><tr><td>
PDT08-S01-D3-G10-Vxx

</td><td>
Startzeitpunkt eines Ausfalls

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT08-S01-D3-G11-Vxx

</td><td>
Endezeitpunkt eines Ausfalls

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT08-S01-D3-G18

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit über alle IP-Verbindungen zwischen SZZPs
der angeschlossenen Produkttypen der TI, bei denen mindestens ein Zugangspunkt
mit der Anschlussoption "einfache Anbindung“ angebunden ist.

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT08-S01-D3-G19

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit, gemittelt über alle IP-Verbindungen
zwischen allen SZZPs mit der Anschlussoption „redundante Anbindung“
angeschlossenen Produkttypen der TI.

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT08-S01-D3-G22

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit, gemittelt über alle IP-Verbindungen
zwischen allen SZZPs mit der Anschlussoption „redundante
Anbindung“angeschlossenen Produkttypen der TI.

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT08-S01-D3-G25

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit über alle IP-Verbindungen zwischen SZZPs
der angeschlossenen Produkttypen der TI, bei denen mindestens ein Zugangspunkt
mit der Anschlussoption „einfache Anbindung“ angebunden ist.

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td colspan="7" rowspan="1">
Zentrales Netz

- I_IP_Transport(P::Verbindung)

</td></tr><tr><td>
PDT08-S10-D3-G10

</td><td>
Startzeitpunkt eines Ausfalls

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT08-S10-D3-G11

</td><td>
Endezeitpunkt eines Ausfalls

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT08-S11-D1-G02-Rxx

</td><td>
Datenmenge (kByte) und Richtung. Die Datenmenge wird an jedem Anschlusspunkt an
das zentrale Netz der TI separat erfasst (SZZP und SZZP-light).

</td><td>
x

</td><td>
x

</td><td>
x

</td></tr><tr><td colspan="7" rowspan="1">
VPN-Zugangsdienst

</td></tr><tr><td>
PDT09-S01-D1-G08

</td><td>
Mittlerer Datendurchsatz pro Richtung in Mbit/s im Erfassungszeitraum

</td><td>
 

</td><td>
 

</td><td>
</td></tr><tr><td colspan="7" rowspan="1">
VPN-Zugangsdienst

- I_DNS_Name_Resolution::get_IP_Address

</td></tr><tr><td>
PDT09-S08-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
 

</td><td>
 

</td><td>
</td></tr><tr><td>
PDT09-S08-D2-G03

</td><td>
Anzahl der Summierten Bearbeitungszeiten

</td><td>
</td><td>
 

</td><td>
</td></tr><tr><td>
PDT09-S08-D2-G04

</td><td>
Summe der Bearbeitungszeiten im Erfassungszeitraum

</td><td>
</td><td>
 

</td><td>
</td></tr><tr><td>
PDT09-S08-D2-G05

</td><td>
Anzahl der Bearbeitungszeiten größer als die 99%-Quantilschranke des
Produkttyps

</td><td>
</td><td>
 

</td><td>
</td></tr><tr><td>
PDT09-S08-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT09-S08-D3-G10

</td><td>
Startzeitpunkt eines Ausfalls

</td><td>
</td><td>
 

</td><td>
</td></tr><tr><td>
PDT09-S08-D3-G11

</td><td>
Endezeitpunkt eines Ausfalls

</td><td>
</td><td>
 

</td><td>
</td></tr><tr><td>
PDT09-S08-D3-G14

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT09-S08-D3-G16

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td colspan="7" rowspan="1">
VPN-Zugangsdienst

- I_NTP_Time_Information

</td></tr><tr><td>
PDT09-S13-D3-G10

</td><td>
Startzeitpunkt eines Ausfalls

</td><td>
</td><td>
 

</td><td>
</td></tr><tr><td>
PDT09-S13-D3-G11

</td><td>
Endezeitpunkt eines Ausfalls

</td><td>
</td><td>
 

</td><td>
</td></tr><tr><td>
PDT09-S13-D3-G14

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT09-S13-D3-G16

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td colspan="7" rowspan="1">
VPN-Zugangsdienst

- I_Secure_Channel_Tunnel

</td></tr><tr><td>
PDT09-S15-D3-G10

</td><td>
Startzeitpunkt eines Ausfalls

</td><td>
</td><td>
 

</td><td>
</td></tr><tr><td>
PDT09-S15-D3-G11

</td><td>
Endezeitpunkt eines Ausfalls

</td><td>
</td><td>
 

</td><td>
</td></tr><tr><td>
PDT09-S15-D3-G14

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT09-S15-D3-G16

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT09-S15-D1-G05

</td><td>
Anzahl der bestehenden VPN-Tunnel

</td><td>
 

</td><td>
 

</td><td>
</td></tr><tr><td>
PDT09-S15-D1-G06

</td><td>
Anzahl der neu aufgebauten VPN-Tunnel

</td><td>
 

</td><td>
 

</td><td>
</td></tr><tr><td>
PDT09-S15-D1-G07

</td><td>
Anzahl der abgebauten VPN-Tunnel

</td><td>
 

</td><td>
 

</td><td>
</td></tr><tr><td colspan="7" rowspan="1">
Sicherheitsgateway KV-Safenet

- I_Secure_Access_Bestandsnetz

</td></tr><tr><td>
PDT10-S14-D1-G02

</td><td>
Datenmenge (kByte) pro Verbindung und Richtung

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT10-S14-D3-G10

</td><td>
Startzeitpunkt eines Ausfalls

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT10-S14-D3-G11

</td><td>
Endezeitpunkt eines Ausfalls

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT10-S14-D3-G14

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT10-S14-D3-G16

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td colspan="7" rowspan="1">
Konfigurationsdienst

- I_KSRS_Download::get_Updates

</td></tr><tr><td>
PDT11-S04-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
 

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT11-S04-D2-G03

</td><td>
Anzahl der Summierten Bearbeitungszeiten

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT11-S04-D2-G04

</td><td>
Summe der Bearbeitungszeiten im Erfassungszeitraum

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT11-S04-D2-G05

</td><td>
Anzahl der Bearbeitungszeiten größer als die 99%-Quantilschranke des
Produkttyps

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT11-S04-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT11-S04-D3-G10

</td><td>
Startzeitpunkt eines Ausfalls

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT11-S04-D3-G11

</td><td>
Endezeitpunkt eines Ausfalls

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT11-S04-D3-G12

</td><td>
Verfügbarkeit pro Monat

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td colspan="7" rowspan="1">
Konfigurationsdienst

– I_KSRS_Download::list_Updates

</td></tr><tr><td>
PDT11-S02-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
 

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT11-S02-D2-G03

</td><td>
Anzahl der Summierten Bearbeitungszeiten

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT11-S02-D2-G04

</td><td>
Summe der Bearbeitungszeiten im Erfassungszeitraum

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT11-S02-D2-G05

</td><td>
Anzahl der Bearbeitungszeiten größer als die 99%-Quantilschranke des
Produkttyps

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT11-S02-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT11-S02-D3-G10

</td><td>
Startzeitpunkt eines Ausfalls

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT11-S02-D3-G11

</td><td>
Endezeitpunkt eines Ausfalls

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT11-S02-D3-G12

</td><td>
Verfügbarkeit pro Monat

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td colspan="7" rowspan="1">
Intermediär VSDM

</td></tr><tr><td>
PDT21-S01-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
 

</td><td>
 

</td><td>
</td></tr><tr><td>
PDT21-S01-D2-G03

</td><td>
Anzahl der Summierten Bearbeitungszeiten

</td><td>
</td><td>
x

</td><td>
</td></tr><tr><td>
PDT21-S01-D2-G04

</td><td>
Summe der Bearbeitungszeiten im Erfassungszeitraum

</td><td>
</td><td>
 

</td><td>
</td></tr><tr><td>
PDT21-S01-D2-G24

</td><td>
Anzahl der Bearbeitungszeiten größer als die 95%-Quantilschranke des
Produkttyps

</td><td>
</td><td>
x

</td><td>
</td></tr><tr><td>
PDT21-S01-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT21-S01-D3-G10

</td><td>
Startzeitpunkt eines Ausfalls

</td><td>
</td><td>
 

</td><td>
</td></tr><tr><td>
PDT21-S01-D3-G11

</td><td>
Endezeitpunkt eines Ausfalls

</td><td>
</td><td>
 

</td><td>
</td></tr><tr><td>
PDT21-S01-D3-G14

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT21-S01-D3-G16

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td colspan="7" rowspan="1">
gematik-Root-CA -

I_OCSP_Status_Information::check_Revocation_Status(P::Zertifikatstyp)

</td></tr><tr><td>
PDT22-S06-D1-G01-Zxx

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
 

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT22-S06-D2-G03-Zxx

</td><td>
Anzahl der Summierten Bearbeitungszeiten

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT22-S06-D2-G04-Zxx

</td><td>
Summe der Bearbeitungszeiten im Erfassungszeitraum

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT22-S06-D2-G05-Zxx

</td><td>
Anzahl der Bearbeitungszeiten größer als die 99%-Quantilschranke des
Produkttyps

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT22-S06-D2-G08-Zxx

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT22-S06-D3-G10-Zxx

</td><td>
Startzeitpunkt eines Ausfalls

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT22-S06-D3-G11-Zxx

</td><td>
Endezeitpunkt eines Ausfalls

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT22-S06-D3-G14-Zxx

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT22-S06-D3-G16-Zxx

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td colspan="7" rowspan="1">
KOM-LE Fachdienst

</td></tr><tr><td>
PDT24-S01-D2-G27

</td><td>
Summe der Bearbeitungszeiten im Erfassungszeitraum, gemessen zwischen dem
Zeitpunkt der quittierten Übergabe vom KOM-LE Clientmodul an den
KOM-LE-Fachdienst des Email-Senders und dem Zeitpunkt der quittierten Übergabe
an den KOM-LE Fachdienst des Email-Empfängers

</td><td>
</td><td>
</td><td>
</td><td>
x

</td></tr><tr><td>
PDT24-S01-D2-G03

</td><td>
Anzahl der Summierten Bearbeitungszeiten im Erfassungszeitraum

</td><td>
</td><td>
</td><td>
</td><td>
x

</td></tr><tr><td>
PDT24-S01-D2-G28

</td><td>
Größte Bearbeitungszeit im Erfassungszeitraum, gemessen zwischen dem Zeitpunkt
der quittierten Übergabe vom KOM-LE Clientmodul an den KOM-LE-Fachdienst des
Email-Senders und dem Zeitpunkt der quittierten Übergabe an den KOM-LE
Fachdienst des Email-Empfängers

</td><td>
 

</td><td>
</td><td>
</td><td>
x

</td></tr><tr><td>
PDT24-S01-D1-G02

</td><td>
Datenmenge (KByte) pro Verbindung und Richtung

</td><td>
</td><td>
 

</td><td>
</td><td>
x

</td></tr><tr><td>
PDT24-S01-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
 

</td><td>
 

</td><td>
</td><td>
x

</td></tr><tr><td>
PDT24-S01-D3-G10

</td><td>
Startzeitpunkt eines Ausfalls

</td><td>
</td><td>
</td><td>
</td><td>
x

</td></tr><tr><td>
PDT24-S01-D3-G11

</td><td>
Endezeitpunkt eines Ausfalls

</td><td>
</td><td>
</td><td>
</td><td>
x

</td></tr><tr><td>
PDT24-S01-D3-G14

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit

</td><td>
 

</td><td>
</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT24-S01-D3-G16

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit

</td><td>
 

</td><td>
</td><td>
 

</td><td>
x

</td></tr><tr><td colspan="7" rowspan="1">
Verzeichnisdienst – I_Directory_Query

</td></tr><tr><td>
PDT25-S16-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
 

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT25-S16-D2-G03

</td><td>
Anzahl der Summierten Bearbeitungszeiten

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT25-S16-D2-G04

</td><td>
Summe der Bearbeitungszeiten im Erfassungszeitraum

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT25-S16-D2-G05

</td><td>
Anzahl der Bearbeitungszeiten größer als die 99%-Quantilschranke des
Produkttyps

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT25-S16-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td colspan="7" rowspan="1">
Verzeichnisdienst

</td></tr><tr><td>
PDT25-S01-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
 

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT25-S01-D3-G10

</td><td>
Startzeitpunkt eines Ausfalls

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT25-S01-D3-G11

</td><td>
Endezeitpunkt eines Ausfalls

</td><td>
x

</td><td>
 

</td><td>
x

</td></tr><tr><td>
PDT25-S01-D3-G14

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td>
PDT25-S01-D3-G16

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit

</td><td>
 

</td><td>
x

</td><td>
 

</td></tr><tr><td colspan="7" rowspan="1">
E-Rezept

</td></tr><tr><td>
PDT50-A01-D3-G14

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit

</td></tr><tr><td>
PDT50-A01-D3-G16 

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit

</td></tr><tr><td>
PDT50-A01-D3-G14R

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit in RU/TU

</td></tr><tr><td>
PDT50-A01-D3-G16R

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit in RU/TU

</td></tr><tr><td>
PDT50-A02-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td></tr><tr><td>
PDT50-A03-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td></tr><tr><td>
PDT50-A04-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td></tr><tr><td>
PDT50-A05-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td></tr><tr><td>
PDT50-A06-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td></tr><tr><td>
PDT50-A07-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td></tr><tr><td>
PDT50-A08-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td></tr><tr><td>
PDT50-S27-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td></tr><tr><td>
PDT50-S20-D2-G05

</td><td>
Anzahl der Bearbeitungszeiten größer als die 99%-Quantilschranke des
Produkttyps

</td></tr><tr><td>
PDT50-S21-D2-G05

</td><td>
Anzahl der Bearbeitungszeiten größer als die 99%-Quantilschranke des
Produkttyps

</td></tr><tr><td>
PDT50-S22-D2-G05

</td><td>
Anzahl der Bearbeitungszeiten größer als die 99%-Quantilschranke des
Produkttyps

</td></tr><tr><td>
PDT50-S23-D2-G05

</td><td>
Anzahl der Bearbeitungszeiten größer als die 99%-Quantilschranke des
Produkttyps

</td></tr><tr><td>
PDT50-S24-D2-G05

</td><td>
Anzahl der Bearbeitungszeiten größer als die 99%-Quantilschranke des
Produkttyps

</td></tr><tr><td>
PDT50-S25-D2-G05

</td><td>
Anzahl der Bearbeitungszeiten größer als die 99%-Quantilschranke des
Produkttyps

</td></tr><tr><td>
PDT50-S26-D2-G05

</td><td>
Anzahl der Bearbeitungszeiten größer als die 99%-Quantilschranke des
Produkttyps

</td></tr><tr><td>
PDT50-S27-D2-G05

</td><td>
Anzahl der Bearbeitungszeiten größer als die 99%-Quantilschranke des
Produkttyps

</td></tr><tr><td colspan="7" rowspan="1">
IdP-Dienst 

</td></tr><tr><td>
PDT52-A01-D3-G14

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit

</td><td>
x

</td></tr><tr><td>
PDT52-A01-D3-G16

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit

</td><td>
x

</td></tr><tr><td>
PDT52-A02-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td><td>
x

</td></tr><tr><td>
PDT52-A03-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td><td>
x

</td></tr><tr><td>
PDT52-A04-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td><td>
x

</td></tr><tr><td>
PDT52-A05-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td><td>
x

</td></tr><tr><td>
PDT52-A06-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td><td>
x

</td></tr><tr><td>
PDT52-A07-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td><td>
x

</td></tr><tr><td>
PDT52-A08-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td><td>
x

</td></tr><tr><td>
PDT52-A09-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td><td>
x

</td></tr><tr><td>
PDT52-A10-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td><td>
x

</td></tr><tr><td>
PDT52-A11-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat

</td><td>
x

</td></tr><tr><td>
PDT52-A02-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT52-A03-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT52-A04-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT52-A05-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT52-A06-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT52-A07-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT52-A08-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT52-A09-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT52-A10-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT52-A11-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT52-A02-D3-G30

</td><td>
Fehlerquote im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT52-A03-D3-G30

</td><td>
Fehlerquote im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT52-A04-D3-G30

</td><td>
Fehlerquote im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT52-A05-D3-G30

</td><td>
Fehlerquote im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT52-A06-D3-G30

</td><td>
Fehlerquote im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT52-A07-D3-G30

</td><td>
Fehlerquote im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT52-A08-D3-G30

</td><td>
Fehlerquote im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT52-A09-D3-G30

</td><td>
Fehlerquote im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT52-A10-D3-G30

</td><td>
Fehlerquote im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT52-A11-D3-G30

</td><td>
Fehlerquote im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT52-A02-D2-G30

</td><td>
Maximale Bearbeitungszeit

</td><td>
x

</td></tr><tr><td>
PDT52-A03-D2-G30

</td><td>
Maximale Bearbeitungszeit

</td><td>
x

</td></tr><tr><td>
PDT52-A04-D2-G30

</td><td>
Maximale Bearbeitungszeit

</td><td>
x

</td></tr><tr><td>
PDT52-A05-D2-G30

</td><td>
Maximale Bearbeitungszeit

</td><td>
x

</td></tr><tr><td>
PDT52-A06-D2-G30

</td><td>
Maximale Bearbeitungszeit

</td><td>
x

</td></tr><tr><td>
PDT52-A07-D2-G30

</td><td>
Maximale Bearbeitungszeit

</td><td>
x

</td></tr><tr><td>
PDT52-A08-D2-G30

</td><td>
Maximale Bearbeitungszeit

</td><td>
x

</td></tr><tr><td>
PDT52-A09-D2-G30

</td><td>
Maximale Bearbeitungszeit

</td><td>
x

</td></tr><tr><td>
PDT52-A10-D2-G30

</td><td>
Maximale Bearbeitungszeit

</td><td>
x

</td></tr><tr><td>
PDT52-A11-D2-G30

</td><td>
Maximale Bearbeitungszeit

</td><td>
x

</td></tr><tr><td>
PDT52-A02-D2-G31

</td><td>
Anteil Bearbeitungen innerhalb der Bearbeitungszeitvorgabe

</td><td>
x

</td></tr><tr><td>
PDT52-A03-D2-G31

</td><td>
Anteil Bearbeitungen innerhalb der Bearbeitungszeitvorgabe

</td><td>
x

</td></tr><tr><td>
PDT52-A04-D2-G31

</td><td>
Anteil Bearbeitungen innerhalb der Bearbeitungszeitvorgabe

</td><td>
x

</td></tr><tr><td>
PDT52-A05-D2-G31

</td><td>
Anteil Bearbeitungen innerhalb der Bearbeitungszeitvorgabe

</td><td>
x

</td></tr><tr><td>
PDT52-A06-D2-G31

</td><td>
Anteil Bearbeitungen innerhalb der Bearbeitungszeitvorgabe

</td><td>
x

</td></tr><tr><td>
PDT52-A07-D2-G31

</td><td>
Anteil Bearbeitungen innerhalb der Bearbeitungszeitvorgabe

</td><td>
x

</td></tr><tr><td>
PDT52-A08-D2-G31

</td><td>
Anteil Bearbeitungen innerhalb der Bearbeitungszeitvorgabe

</td><td>
x

</td></tr><tr><td>
PDT52-A09-D2-G31

</td><td>
Anteil Bearbeitungen innerhalb der Bearbeitungszeitvorgabe

</td><td>
x

</td></tr><tr><td>
PDT52-A10-D2-G31

</td><td>
Anteil Bearbeitungen innerhalb der Bearbeitungszeitvorgabe

</td><td>
x

</td></tr><tr><td>
PDT52-A11-D2-G31

</td><td>
Anteil Bearbeitungen innerhalb der Bearbeitungszeitvorgabe

</td><td>
x

</td></tr><tr><td colspan="7" rowspan="1">
ePA Aktensystem - I_Authentication

</td></tr><tr><td>
PDT43-S01-D3-G14

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit [%*1000]

</td><td>
x

</td></tr><tr><td>
PDT43-S01-D3-G16

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit [%*1000]

</td><td>
x

</td></tr><tr><td colspan="7" rowspan="1">
ePA Aktensystem - I_Authentication_Insurant::login

</td></tr><tr><td>
PDT43-S02-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT43-S02-D2-G03

</td><td>
Anzahl der summierten Bearbeitungszeiten

</td><td>
x

</td></tr><tr><td>
PDT43-S02-D2-G04

</td><td>
Summe der Bearbeitungszeiten [msec] im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT43-S02-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat [msec]

</td><td>
x

</td></tr><tr><td>
PDT43-S02-D2-G30

</td><td>
Maximale Bearbeitungszeit

</td><td>
x

</td></tr><tr><td>
PDT43-S02-D2-G31

</td><td>
Anteil Bearbeitungen innerhalb der Bearbeitungszeitvorgabe

</td><td>
x

</td></tr><tr><td colspan="7" rowspan="1">
ePA Aktensystem - I_Authentication_Insurant::renew

</td></tr><tr><td>
PDT43-S03-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT43-S03-D2-G03

</td><td>
Anzahl der summierten Bearbeitungszeiten

</td><td>
x

</td></tr><tr><td>
PDT43-S03-D2-G04

</td><td>
Summe der Bearbeitungszeiten [msec] im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT43-S03-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat [msec]

</td><td>
x

</td></tr><tr><td>
PDT43-S03-D2-G30

</td><td>
Maximale Bearbeitungszeit

</td><td>
x

</td></tr><tr><td>
PDT43-S03-D2-G31

</td><td>
Anteil Bearbeitungen innerhalb der Bearbeitungszeitvorgabe

</td><td>
x

</td></tr><tr><td colspan="7" rowspan="1">
ePA Aktensystem - I_Authentication_Insurant::logout

</td></tr><tr><td>
PDT43-S04-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT43-S04-D2-G03

</td><td>
Anzahl der summierten Bearbeitungszeiten

</td><td>
x

</td></tr><tr><td>
PDT43-S04-D2-G04

</td><td>
Summe der Bearbeitungszeiten [msec] im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT43-S04-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat [msec]

</td><td>
x

</td></tr><tr><td>
PDT43-S04-D2-G30

</td><td>
Maximale Bearbeitungszeit

</td><td>
x

</td></tr><tr><td>
PDT43-S04-D2-G31

</td><td>
Anteil Bearbeitungen innerhalb der Bearbeitungszeitvorgabe

</td><td>
x

</td></tr><tr><td colspan="7" rowspan="1">
ePA Aktensystem - I_Authorization

</td></tr><tr><td>
PDT43-S05-D3-G14

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit [%*1000]

</td><td>
x

</td></tr><tr><td>
PDT43-S05-D3-G16

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit [%*1000]

</td><td>
x

</td></tr><tr><td colspan="7" rowspan="1">
ePA Aktensystem - I_Authorization::getAuthorizationKey

</td></tr><tr><td>
PDT43-S06-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT43-S06-D2-G03

</td><td>
Anzahl der summierten Bearbeitungszeiten

</td><td>
x

</td></tr><tr><td>
PDT43-S06-D2-G04

</td><td>
Summe der Bearbeitungszeiten [msec] im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT43-S06-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat [msec]

</td><td>
x

</td></tr><tr><td>
PDT43-S06-D2-G30

</td><td>
Maximale Bearbeitungszeit

</td><td>
x

</td></tr><tr><td>
PDT43-S06-D2-G31

</td><td>
Anteil Bearbeitungen innerhalb der Bearbeitungszeitvorgabe

</td><td>
x

</td></tr><tr><td colspan="7" rowspan="1">
ePA Aktensystem - I_Authorization_Insurant::getAuthorizationKey

</td></tr><tr><td>
PDT43-S07-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT43-S07-D2-G03

</td><td>
Anzahl der summierten Bearbeitungszeiten

</td><td>
x

</td></tr><tr><td>
PDT43-S07-D2-G04

</td><td>
Summe der Bearbeitungszeiten [msec] im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT43-S07-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat [msec]

</td><td>
x

</td></tr><tr><td>
PDT43-S07-D2-G30

</td><td>
Maximale Bearbeitungszeit

</td><td>
x

</td></tr><tr><td>
PDT43-S07-D2-G31

</td><td>
Anteil Bearbeitungen innerhalb der Bearbeitungszeitvorgabe

</td><td>
x

</td></tr><tr><td colspan="7" rowspan="1">
ePA Aktensystem - ePA.UC_1

</td></tr><tr><td>
PDT43-A01-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT43-A01-D2-G03

</td><td>
Anzahl der summierten Bearbeitungszeiten

</td><td>
x

</td></tr><tr><td>
PDT43-A01-D2-G04

</td><td>
Summe der Bearbeitungszeiten [msec] im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT43-A01-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat [msec]

</td><td>
x

</td></tr><tr><td>
PDT43-A01-D2-G30

</td><td>
Maximale Bearbeitungszeit

</td><td>
x

</td></tr><tr><td>
PDT43-A01-D2-G31

</td><td>
Anteil Bearbeitungen innerhalb der Bearbeitungszeitvorgabe

</td><td>
x

</td></tr><tr><td colspan="7" rowspan="1">
ePA Aktensystem - I_Document_Management

</td></tr><tr><td>
PDT43-S08-D3-G14

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit [%*1000]

</td><td>
x

</td></tr><tr><td>
PDT43-S08-D3-G16

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit [%*1000]

</td><td>
x

</td></tr><tr><td colspan="7" rowspan="1">
Schlüsselgenerierungsdienst - I*

</td></tr><tr><td>
PDT48-S01-D3-G14

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit [%*1000]

</td><td>
x

</td></tr><tr><td>
PDT48-S01-D3-G16

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit [%*1000]

</td><td>
x

</td></tr><tr><td colspan="7" rowspan="1">
Schlüsselgenerierungsdienst - GetPublicKey

</td></tr><tr><td>
PDT48-S02-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT48-S02-D2-G03

</td><td>
Anzahl der summierten Bearbeitungszeiten

</td><td>
x

</td></tr><tr><td>
PDT48-S02-D2-G04

</td><td>
Summe der Bearbeitungszeiten [msec] im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT48-S02-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat. [msec]

</td><td>
x

</td></tr><tr><td>
PDT48-S02-D2-G30

</td><td>
Maximale Bearbeitungszeit

</td><td>
x

</td></tr><tr><td>
PDT48-S02-D2-G31

</td><td>
Anteil Bearbeitungen innerhalb der Bearbeitungszeitvorgabe

</td><td>
x

</td></tr><tr><td colspan="7" rowspan="1">
Schlüsselgenerierungsdienst - SGD.UC_1

</td></tr><tr><td>
PDT48-A01-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT48-A01-D2-G03

</td><td>
Anzahl der summierten Bearbeitungszeiten

</td><td>
x

</td></tr><tr><td>
PDT48-A01-D2-G04

</td><td>
Summe der Bearbeitungszeiten [msec] im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT48-A01-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat [msec]

</td><td>
x

</td></tr><tr><td>
PDT48-A01-D2-G30

</td><td>
Maximale Bearbeitungszeit

</td><td>
x

</td></tr><tr><td>
PDT48-A01-D2-G31

</td><td>
Anteil Bearbeitungen innerhalb der Bearbeitungszeitvorgabe

</td><td>
x

</td></tr><tr><td colspan="7" rowspan="1">
Signaturdienst - I*

</td></tr><tr><td>
PDT47-S01-D3-G14

</td><td>
Verfügbarkeit pro Monat zur Hauptzeit [%*1000]

</td><td>
x

</td></tr><tr><td>
PDT47-S01-D3-G16

</td><td>
Verfügbarkeit pro Monat zur Nebenzeit [%*1000]

</td><td>
x

</td></tr><tr><td colspan="7" rowspan="1">
Signaturdienst - I_Remote_Sign_Operations::sign_Data

</td></tr><tr><td>
PDT47-S02-D1-G01

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT47-S02-D2-G03

</td><td>
Anzahl der summierten Bearbeitungszeiten

</td><td>
x

</td></tr><tr><td>
PDT47-S02-D2-G04

</td><td>
Summe der Bearbeitungszeiten [msec] im Erfassungszeitraum

</td><td>
x

</td></tr><tr><td>
PDT47-S02-D2-G08

</td><td>
Mittlere Bearbeitungszeit pro Monat [msec]

</td><td>
x

</td></tr><tr><td>
PDT47-S02-D2-G30

</td><td>
Maximale Bearbeitungszeit

</td><td>
x

</td></tr><tr><td>
PDT47-S02-D2-G31

</td><td>
Anteil Bearbeitungen innerhalb der Bearbeitungszeitvorgabe

</td><td>
x

</td></tr></table>

<table><tr><th>
Zeitpunkt Anfrage

</th><th>
fehlerfrei bearbeitet:  

ja/nein

</th><th>
Bearbeitungsdauer

[msec]

</th></tr><tr><td>
14.07.2014 13:30:01

</td><td>
ja

</td><td>
907

</td></tr><tr><td>
14.07.2014 13:30:47

</td><td>
ja

</td><td>
830

</td></tr><tr><td>
14.07.2014 13:31:05

</td><td>
ja

</td><td>
790

</td></tr><tr><td>
14.07.2014 13:31:13

</td><td>
ja

</td><td>
719

</td></tr><tr><td>
14.07.2014 13:32:02

</td><td>
ja

</td><td>
1013

</td></tr><tr><td>
14.07.2014 13:32:32

</td><td>
ja

</td><td>
1026

</td></tr><tr><td>
14.07.2014 13:32:33

</td><td>
ja

</td><td>
920

</td></tr><tr><td>
14.07.2014 13:34:23

</td><td>
ja

</td><td>
760

</td></tr><tr><td>
14.07.2014 13:34:31

</td><td>
ja

</td><td>
840

</td></tr><tr><td>
14.07.2014 13:34:55

</td><td>
ja

</td><td>
710

</td></tr><tr><td>
14.07.2014 13:35:03

</td><td>
ja

</td><td>
828

</td></tr><tr><td>
14.07.2014 13:35:09

</td><td>
ja

</td><td>
730

</td></tr><tr><td>
14.07.2014 13:35:15

</td><td>
ja

</td><td>
731

</td></tr><tr><td>
14.07.2014 13:35:17

</td><td>
ja

</td><td>
864

</td></tr><tr><td>
14.07.2014 13:35:17

</td><td>
ja

</td><td>
1708

</td></tr><tr><td>
14.07.2014 13:35:18

</td><td>
nein

</td><td>
-

</td></tr><tr><td>
14.07.2014 13:35:40

</td><td>
ja

</td><td>
901

</td></tr><tr><td>
14.07.2014 13:38:22

</td><td>
ja

</td><td>
839

</td></tr><tr><td>
14.07.2014 13:39:06

</td><td>
ja

</td><td>
1280

</td></tr><tr><td>
14.07.2014 13:39:16

</td><td>
ja

</td><td>
1189

</td></tr><tr><td>
14.07.2014 13:39:34

</td><td>
ja

</td><td>
844

</td></tr></table>

<table><tr><th colspan="3">
TSP-X.509nonQES -
I_OCSP_Status_Information::check_Revocation_Status(P::Zertifikatstyp) -
HBA-Zertifikate (C.HP.ENC)

</th></tr><tr><td colspan="2">
Größe

</td><td>
Wert

</td></tr><tr><td>
Erfassungszeitraum

</td><td>
von

</td><td>
14.07.2014 13:30:00

</td></tr><tr><td>
 

</td><td>
bis

</td><td>
14.07.2014 13:34:59

</td></tr><tr><td>
PDT03-S06-D1-G01-Z06

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
10

</td></tr><tr><td>
PDT03-S06-D2-G03-Z06

</td><td>
Anzahl der Summierten Bearbeitungszeiten

</td><td>
10

</td></tr><tr><td>
PDT03-S06-D2-G04-Z06

</td><td>
Summe der Bearbeitungszeiten [msec] im Erfassungszeitraum

</td><td>
8515

</td></tr><tr><td>
PDT03-S06-D2-G05-Z06

</td><td>
Anzahl der Bearbeitungszeiten größer als die 99%-Quantilschranke des
Produkttyps

</td><td>
0

</td></tr><tr><td>
Erfassungszeitraum

</td><td>
von

</td><td>
14.07.2014 13:35:00

</td></tr><tr><td>
 

</td><td>
bis

</td><td>
14.07.2014 13:39:59

</td></tr><tr><td>
PDT03-S06-D1-G01-Z06

</td><td>
Anzahl der Aufrufe im Erfassungszeitraum

</td><td>
11

</td></tr><tr><td>
PDT03-S06-D2-G03-Z06

</td><td>
Anzahl der Summierten Bearbeitungszeiten

</td><td>
10

</td></tr><tr><td>
PDT03-S06-D2-G04-Z06

</td><td>
Summe der Bearbeitungszeiten [msec] im Erfassungszeitraum

</td><td>
9914

</td></tr><tr><td>
PDT03-S06-D2-G05-Z06

</td><td>
Anzahl der Bearbeitungszeiten größer als die 99%-Quantilschranke des
Produkttyps

</td><td>
1

</td></tr></table>

### 7 Anhang B – Verzeichnisse

### 7.1 Abkürzungen

<table><tr><th>
Kürzel

</th><th>
Erläuterung

</th></tr><tr><td>
aAdG

</td><td>
andere Anwendung des Gesundheitswesens

</td></tr><tr><td>
aAdGNetG

</td><td>
andere Anwendung des Gesundheitswesens ohne Zugriff auf Dienste der TI in
angeschlossenen Netzen des Gesundheitswesens

</td></tr><tr><td>
aAdGNetG-TI

</td><td>
andere Anwendung des Gesundheitswesens mit Zugriff auf Dienste der TI aus
angeschlossenen Netzen des Gesundheitswesens

</td></tr><tr><td>
CMS

</td><td>
Card Management System

</td></tr><tr><td>
DVO

</td><td>
Dienstleister-vor-Ort

</td></tr><tr><td>
eGK

</td><td>
elektronische Gesundheitskarte

</td></tr><tr><td>
ePA

</td><td>
elektronische Patientenakte

</td></tr><tr><td>
FAD

</td><td>
Fachanwendungsspezifischer Dienst

</td></tr><tr><td>
GTI

</td><td>
Gesamtverantwortlicher TI

</td></tr><tr><td>
gSMC-K

</td><td>
gerätespezifische Security Module Card Konnektor

</td></tr><tr><td>
gSMC-KT

</td><td>
gerätespezifische Security Module Card Kartenterminal

</td></tr><tr><td>
HBA

</td><td>
Heilberufsausweise

</td></tr><tr><td>
HSM-B

</td><td>
Hardware Security Module-B

</td></tr><tr><td>
ITSM

</td><td>
IT-Service Management

</td></tr><tr><td>
KT

</td><td>
Kartenterminal

</td></tr><tr><td>
OCSP-R Proxy

</td><td>
OCSP-Responder Proxy

</td></tr><tr><td>
PU

</td><td>
Produktivumgebung

</td></tr><tr><td>
QES

</td><td>
Qualifizierte Elektronische Signatur

</td></tr><tr><td>
SK

</td><td>
Servicekomponenten

</td></tr><tr><td>
SGD

</td><td>
Schlüsselgenerierungsdienst

</td></tr><tr><td>
SGW

</td><td>
Sicherheitsgateway

</td></tr><tr><td>
SLA

</td><td>
Service Level Agreement

</td></tr><tr><td>
SL

</td><td>
Service Level

</td></tr><tr><td>
SMC-B

</td><td>
Secure Module Card-B

</td></tr><tr><td>
SPOC

</td><td>
Single Point of Contact

</td></tr><tr><td>
SV

</td><td>
Serviceverantwortlicher

</td></tr><tr><td>
TI

</td><td>
Telematikinfrastruktur

</td></tr><tr><td>
TIP

</td><td>
Telematikinfrastruktur-Plattform

</td></tr><tr><td>
TSP

</td><td>
Trust Service Provider

</td></tr><tr><td>
TU

</td><td>
Testumgebung

</td></tr><tr><td>
UFS

</td><td>
Update Flag Service

</td></tr><tr><td>
UHD

</td><td>
User Help Desk

</td></tr><tr><td>
VHD

</td><td>
Versicherten Help Desk

</td></tr><tr><td>
VSD

</td><td>
Versichertenstammdaten

</td></tr><tr><td>
VSDD

</td><td>
Versichertenstammdatendienst

</td></tr><tr><td>
VSDM

</td><td>
Versichertenstammdatenmanagement

</td></tr></table>

### 7.2 Glossar

Das Glossar wird als eigenständiges Dokument (vgl. [gemGlossar]) zur Verfügung
gestellt.

### 7.3 Abbildungsverzeichnis

- [Abbildung-1] - Anbieterkonstellation

### 7.4 Tabellenverzeichnis

- [Tabelle-1] - Tab_KPT_Betr_TI_001 TI-ITSM-Teilnehmer
- [Tabelle-4] - Tab_KPT_Betr_TI_044 Mindestservicezeit Störungsmeldungen und Anfragen
- [Tabelle-7] - Tab_gemKPT_Betr_Performance-Dimensionen
- [Tabelle-8] - Tab_gemKPT_Betr_Performance-Groessen
- [Tabelle-9] -  Tab_gemKPT_Betr_Produkttypen
- [Tabelle-10] - Tab_gemKPT_Betr_Schnittstellenoperationen
- [Tabelle-11] - Tab_gemKPT_Betr_UC_Anwendungsfallübersicht
- [Tabelle-12] - Tab_gemKPT_Betr_Zertifikatstypen
- [Tabelle-13] - Tab_gemKPT_Betr_Aufrufquelle
- [Tabelle-14] -  
- [Tabelle-15] - Tab_gemKPT_Betr_Beispiel_Rohdaten
- [Tabelle-16] - Tab_gemKPT_Betr_Beispiel_Performance_Kenngroessen
- [Tabelle-17] - Tab_KPT_Betr_TI_045 Abkürzungsverzeichnis

### 7.5 Referenzierte Dokumente

### 7.5.1 Dokumente der gematik

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
Herausgeber (Erscheinungsdatum): Titel

</th></tr><tr><td>
[gemGlossar]

</td><td>
gematik: Glossar der Telematikinfrastruktur

</td></tr><tr><td>
[gemKPT_Arch_TIP]

</td><td>
gematik: Konzept Architektur der TI-Plattform

</td></tr><tr><td>
[gemRL_Betr_TI]

</td><td>
gematik: Übergreifende Richtlinien zum Betrieb der TI

</td></tr><tr><td>
[gemSpec_Perf]

</td><td>
gematik: Übergreifende Spezifikation Performance und Mengengerüst TI-Plattform

</td></tr></table>

### 7.5.2 Weitere Dokumente

<table><tr><th>
[Quelle]

</th><th>
Herausgeber (Erscheinungsdatum): Titel

</th></tr><tr><td>
[RFC2119]

</td><td>
RFC 2119 (März 1997): Key words for use in RFCs to Indicate Requirement Levels
S. Bradner,  
http://tools.ietf.org/html/rfc2119

</td></tr></table>





[Dokumentinformationen]: #dokumentinformationen
[Inhaltsverzeichnis]:    #inhaltsverzeichnis
[1]:                     #1-einordnung-des-dokumentes
[1.1]:                   #11-zielsetzung
[1.2]:                   #12-zielgruppe
[1.3]:                   #13-geltungsbereich
[1.4]:                   #14-abgrenzung-des-dokuments
[1.5]:                   #15-methodik
[1.5.1]:                 #151-anforderungen
[2]:                     #2-grundlagen-des-betriebs
[2.1]:                   #21-gegenstand-des-betriebskonzepts
[2.2]:                   #22-begriffserläuterungen
[2.2.1]:                 #221-business-servicekatalog
[2.2.2]:                 #222-technischer-kennzahlenkatalog
[2.2.3]:                 #223-konfigurationen-von-produkten
[2.2.4]:                 #224-organisatorische-service-level
[2.2.5]:                 #225-unterstützungsleistungen-aller-ti-itsm-teilnehmer
[2.2.6]:                 #226-service-verzeichnis
[3]:                     #3-servicekonzept
[3.1]:                   #31-übergreifendes-it-service-management-der-ti
[3.2]:                   #32-rollen
[3.2.1]:                 #321-begriffserläuterungen
[3.2.1.1]:               #3211-servicenehmer
[3.2.2]:                 #322-ti-service
[3.2.3]:                 #323-ti-itsm-teilnehmer
[3.2.3.1]:               #3231-anbieterkonstellationen
[3.2.4]:                 #324-dvo
[3.2.5]:                 #325-gesamtverantwortlicher-ti-gti
[3.2.6]:                 #326-serviceverantwortung-sv-der-ti-itsm-teilnehmer
[3.2.7]:                 #327-anbieter
[3.2.8]:                 #328-betreiber
[3.2.9]:                 #329-hersteller-dezentraler-produkte
[3.2.10]:                #3210-hersteller-zentraler-produkte
[3.2.11]:                #3211-gematik-test-in-der-tu
[3.2.12]:                #3212-anwender
[3.2.13]:                #3213-versicherte
[3.2.14]:                #3214-anbieter-vpn-zugd
[3.2.15]:                #3215-user-help-desk-uhd
[3.2.16]:                #3216-versicherten-help-desk-vhd
[3.2.17]:                #3217-anbieter-epa-aktensystem
[3.2.18]:                #3218-anbieter-service-monitoring
[3.2.19]:                #3219-anbieter-basis-consumer
[3.2.20]:                #3220-anbieter-ktr-consumer
[3.2.21]:                #3221-anbieter-ktr-adv
[3.2.22]:                #3222-anbieter-kom-le
[3.2.23]:                #3223-anbieter-anschlusspunkt-am-sgw
[3.2.24]:                #3224-anbieter-ti-messenger
[3.3]:                   #33-servicemodell
[3.3.1]:                 #331-servicekomponenten
[3.3.2]:                 #332-servicezerlegung
[3.3.2.1]:               #3321-legende
[3.3.3]:                 #333-mitwirkungsverpflichtung-im-ti-itsm-gemäß-gemrl_betr_ti
[3.3.3.1]:               #3331-legende
[3.4]:                   #34-supportkonzept
[3.4.1]:                 #341-begriffserläuterungen
[3.4.2]:                 #342-single-point-of-contact-spoc-für-ti-itsm-teilnehmer
[4]:                     #4-verantwortlichkeiten-und-leistungen-ti-itsm-teilnehmer
[4.1]:                   #41-begriffserläuterungen
[4.1.1]:                 #411-anbietertypsteckbrief
[4.2]:                   #42-allgemeine-anforderungen
[4.2.1]:                 #421-allgemeine-anforderungen-für-ti-itsm-teilnehmer
[4.2.2]:                 #422-allgemeine-anforderungen-nur-für-anbieter-von-diensten
[4.3]:                   #43-service-level-vorgangsübergreifend
[4.3.1]:                 #431-begriffserläuterungen
[4.3.1.1]:               #4311-quantil--erfüllungsgrad
[4.3.1.2]:               #4312-reaktionszeit
[4.3.1.3]:               #4313-lösungszeit
[4.3.1.4]:               #4314-verifikationsfrist
[4.3.2]:                 #432-incident-management
[4.3.3]:                 #433-reporting
[4.3.4]:                 #434-datenaufbewahrung
[5]:                     #5-übergreifende-regelungen-für-betriebliche-kennzahlen-für-mobile-anwendungen-apps
[6]:                     #6-anhang-a-–-performance-kenngrößen
[7]:                     #7-anhang-b-–-verzeichnisse
[7.1]:                   #71-abkürzungen
[7.2]:                   #72-glossar
[7.3]:                   #73-abbildungsverzeichnis
[7.4]:                   #74-tabellenverzeichnis
[7.5]:                   #75-referenzierte-dokumente
[7.5.1]:                 #751-dokumente-der-gematik
[7.5.2]:                 #752-weitere-dokumente
[Img-001]:               gemKPT_Betr_V_3_11_0_V3.11.0 (1).attachments/15756659392347973709.png
[Abbildung-1]:           gemKPT_Betr_V_3_11_0_V3.11.0 (1).attachments/8486658120071984648.png
[Img-003]:               gemKPT_Betr_V_3_11_0_V3.11.0 (1).attachments/3047164449832902795.png
[Img-004]:               gemKPT_Betr_V_3_11_0_V3.11.0 (1).attachments/13481269887771129295.png
[Img-005]:               gemKPT_Betr_V_3_11_0_V3.11.0 (1).attachments/9014411415605272585.png
[Img-006]:               gemKPT_Betr_V_3_11_0_V3.11.0 (1).attachments/15066217364023943218.png
[Tbl-001]:               #Tbl-001 (&93834775698688)
[Tabelle-1]:             #Tabelle-1 (&93834801609136)
[Tabelle-4]:             #Tabelle-4 (&93834783653008)
[Tabelle-7]:             #Tabelle-7 (&93834767978168)
[Tabelle-8]:             #Tabelle-8 (&93834767994016)
[Tabelle-9]:             #Tabelle-9 (&93834804510904)
[Tabelle-10]:            #Tabelle-10 (&93834764466232)
[Tabelle-11]:            #Tabelle-11 (&93834772289752)
[Tabelle-12]:            #Tabelle-12 (&93834777640336)
[Tabelle-13]:            #Tabelle-13 (&93834777703368)
[Tabelle-14]:            #Tabelle-14 (&93834781745760)
[Tabelle-15]:            #Tabelle-15 (&93834798898624)
[Tabelle-16]:            #Tabelle-16 (&93834764617440)
[Tabelle-17]:            #Tabelle-17 (&93834764681264)
[Tbl-015]:               #Tbl-015 (&93834764839424)
[Tbl-016]:               #Tbl-016 (&93834764856160)
