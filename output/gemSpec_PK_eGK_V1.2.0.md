
Elektronische Gesundheitskarte und Telematikinfrastruktur

### Spezifikation für Prüfkarten des Typs eGK

- Klassifizierung: öffentlich
- Referenzierung: gemSpec_PK_eGK
- Revision: 548770
- Stand: 26.10.2018
- Status: freigegeben
- Version: 1.2.0

### Dokumentinformationen

Änderungen zur Vorversion

Die Erstversion wurde um Angabe zu Prüfkarten der Generation 2 ergänzt.

Dokumentenhistorie

<table><tr><th>
Version

</th><th>
Stand

</th><th>
Grund der Änderung, besondere Hinweise

</th><th>
Bearbeitung

</th></tr><tr><td>
1.0.0

</td><td>
14.05.18

</td><td>
Ersterstellung

</td><td>
gematik

</td></tr><tr><td>
Erweiterung für Prüfkarten der Generation G2.1

</td><td>
gematik

</td></tr><tr><td>
1.1.0

</td><td>
26.10.18

</td><td>
freigegeben

</td><td>
gematik

</td></tr></table>

### Inhaltsverzeichnis

- [Dokumentinformationen]
- [Inhaltsverzeichnis]
- [1] Einführung des Dokuments
  - [1.1] Zielsetzung
  - [1.2] Zielgruppe
  - [1.3] Geltungsbereich
  - [1.4] Abgrenzung des Dokuments
  - [1.5] Methodik
  - [1.6] Nomenklatur
- [2] Initialisiertes Objektsystem der Prüfkarte eGK
- [3] Personalisierungsvalidierung
- [4] Festlegungen für Personalisierungsdaten
  - [4.1] Festlegungen für die ICCSN
  - [4.2] Festlegungen für die IK-Nummer
  - [4.3] Festlegungen für die Versichertennummer
  - [4.4] Festlegungen des Herausgebers
  - [4.5] Festlegungen für die Versichertenstammdaten
- [5] Bereitstellung der Personalisierungsdaten
- [6] Vorgaben für die Zertifikate
- [7] Personalisiertes Objektsystem der Prüfkarte eGK
  - [7.1] Schlüssel für die Administration
  - [7.2] QES-Anwendung
- [8] Optische Gestaltung der Prüfkarte eGK
  - [8.1] Optische Gestaltung der Kartenvorderseite
    - [8.1.1] Unveränderbare optische Gestaltung
    - [8.1.2] Veränderbare optische Gestaltung
  - [8.2] Optische Gestaltung der Kartenrückseite
- [9] Anhang A – Verzeichnisse
  - [9.1] Abkürzungen
  - [9.2] Abbildungsverzeichnis
  - [9.3] Tabellenverzeichnis
  - [9.4] Referenzierte Dokumente
    - [9.4.1] Dokumente der gematik
    - [9.4.2] Weitere Dokumente

### 1 Einführung des Dokuments

### 1.1 Zielsetzung

Die Installation und Wartung von dezentralen Komponenten der
Telematikinfrastruktur des Gesundheitswesens (TI) in der Produktivumgebung (PU)
erfordert Möglichkeiten zur Überprüfung der Installation und Konfiguration
der dezentralen Komponenten und deren Anbindung an die Primärsysteme der
Leistungserbringerumgebung. Hierzu wird eine speziell ausgestattete eGK, die
Prüfkarte des Typs eGK (PK eGK) verwendet.

Diese Prüfkarte nutzt den Vertrauensraum der PU. Durch geeignete Merkmale der
elektrischen und optischen Personalisierung wird der Missbrauch und die
Verwechselung mit einer „echten“ eGK der PU (eGK eines Versicherten)
ausgeschlossen.

Zu den erkennbaren Merkmalen zählen insbesondere eine auffällige optische
Gestaltung, eine eigens für Prüfzwecke definierte Institutskennung und die
Verwendung von Personalisierungsdaten fiktiver Identitäten, die eine
Verwechselung mit realen Versicherten ausschließen.

### 1.2 Zielgruppe

Dieses Dokument richtet sich an Hersteller personalisierter Prüfkarten des Typs
eGK.

### 1.3 Geltungsbereich

Das vorliegende Dokument enthält normative Festlegungen zur
Telematikinfrastruktur des deutschen Gesundheitswesens. Die Zuordnung der
vorliegenden Dokumentenversion zu einem Release erfolgt über die jeweilige
Dokumentenlandkarte. Diese wird zusammen mit den Dokumenten auf der
Internetseite der gematik öffentlich bereitgestellt.

Dieses Dokument enthält verbindliche Festlegungen der gematik zur
Personalisierung von Prüfkarten des Typs eGK.

Außerhalb der Beauftragungen durch die gematik ist dieses Dokument informativ.

Schutzrechts-/Patentrechtshinweis

Dieses Dokument ist von der gematik allein unter technischen Gesichtspunkten
erstellt worden. Im Einzelfall kann nicht ausgeschlossen werden, dass die
Implementierung der Inhalte in technische Schutzrechte Dritter eingreift. Es
ist allein Sache des Anbieters oder Herstellers, durch geeignete Maßnahmen
dafür Sorge zu tragen, dass von ihm aufgrund der beschriebenen Inhalte
angebotene Produkte und/oder Leistungen nicht gegen Schutzrechte Dritter
verstoßen und sich ggf. die erforderlichen Erlaubnisse/Lizenzen von den
betroffenen Schutzrechtsinhabern einzuholen. Die gematik GmbH übernimmt
insofern keinerlei Gewährleistungen.

### 1.4 Abgrenzung des Dokuments

Dieses Dokument definiert Merkmale der Prüfkarte des Typs eGK als Abgrenzung zu
den Merkmalen einer eGK eines Versicherten und Testkarten eGK der RU/TU.

Eine detaillierte Zusammenstellung aller geltenden Anforderungen an die
personalisierte Prüfkarte ist im Produkttypsteckbrief der Prüfkarte des Typs
eGK [gemProdT_PK_eGK] dargestellt. Es wird darauf hingewiesen, dass
Anforderungen zur optischen und mechanischen Ausprägung sowohl in
[gemSpec_eGK_OPT], als auch im vorliegenden Dokument beschrieben sind.

Dieses Dokument enthält keine Vorgaben zum Bestätigungsverfahren für
Prüfkarten und zum Verfahren der Datenübermittlung an den Hersteller der
Prüfkarten.

### 1.5 Methodik

Anforderungen als Ausdruck normativer Festlegungen werden durch eine eindeutige
ID sowie die dem RFC 2119 [RFC2119] entsprechenden, in Großbuchstaben
geschriebenen deutschen Schlüsselworte MUSS, DARF NICHT, SOLL, SOLL NICHT,
KANN gekennzeichnet.

Sie werden im Dokument wie folgt dargestellt:

\<AFO-ID\> - \<Titel der Afo\>Text / Beschreibung [\<=]

Dabei umfasst die Anforderung sämtliche innerhalb der Textmarken angeführten
Inhalte.

### 1.6 Nomenklatur

Die im Verlauf dieses Dokuments verwendeten Bezeichnungen „Prüfkarte“ und
„Prüfkarte eGK“ beziehen sich immer auf die „Prüfkarte des Typs eGK“.
„Echte“ eGKs der Produktivumgebung werden zur Abgrenzung gegenüber der
Prüfkarte als „eGK eines Versicherten“ bezeichnet.

### 2 Initialisiertes Objektsystem der Prüfkarte eGK

Für die Prüfkarte wird das initialisierte Objektsystem einer für den
Produktivbetrieb zugelassenen eGK unverändert verwendet. Für eine Prüfkarte
der Generation 2 ist ein Objektsystem gemäß [gemSpec_eGK_ObjSys] und für
eine Prüfkarte der Generation G2.1 ein Objektsystem gemäß
[gemSpec_eGK_ObjSys_G2.1] zu verwenden. Eine Umsetzung der möglichen Optionen
des jeweiligen Objektsystems ist nicht erforderlich.

**A_14281 - Produkttypversion initialisiertes Objektsystem der Prüfkarte eGK
G2**

Die Prüfkarte der Generation G2 MUSS auf der Basis eines zugelassenen
initialisierten Objektsystems einer eGK gemäß [gemProdT_eGK_ObjSys] erstellt
werden. **[\<=]**

**Card-G2-A_3816 - Produkttypversion initialisiertes Objektsystem der Prüfkarte
eGK G2.1**

Die Prüfkarte der Generation G2.1 MUSS auf der Basis eines zugelassenen
initialisierten Objektsystems einer eGK gemäß [gemProdT_eGK_ObjSys_G2.1]
erstellt werden. **[\<=]**

**A_14282 - Optionen des Objektsystems der Prüfkarte eGK G2**

Die Prüfkarte der Generation 2 SOLL die möglichen Optionen des Objektsystems
der eGK aus [gemSpec_eGK_ObjSys] NICHT unterstützen. **[\<=]**

**Card-G2-A_3817 - Optionen des Objektsystems der Prüfkarte eGK G2.1**

Die Prüfkarte der Generation G2.1 SOLL die möglichen Optionen des
Objektsystems der eGK aus [gemSpec_eGK_ObjSys_G2.1] NICHT unterstützen.
**[\<=]**

Anmerkung: Diese Anforderung schließt die Option „QES-Anwendung komplett
angelegt und nutzbar“ mit ein. Diese soll nicht unterstützt werden.

### 3 Personalisierungsvalidierung

Für die personalisierten Prüfkarten ist keine Zulassung durch die gematik
notwendig. Es erfolgt eine Prüfung der korrekten Personalisierung und
Bestätigung durch die gematik. Die konkrete Verfahrensweise und Bedingungen
dazu sind nicht Bestandteil des vorliegenden Dokuments.

### 4 Festlegungen für Personalisierungsdaten

Die folgenden Festlegungen gelten für alle Prüfkarten gemeinsam. Sie sind bei
der Erstellung der Zertifikate sowie der elektrischen und optischen
Personalisierung anzuwenden.

### 4.1 Festlegungen für die ICCSN

Für die ersten 5 Oktette (10 Ziffern) der ICCSN wird ein einheitlicher Wert
vorgegeben.

**Card-G2-A_3818 - Vorgegebene Issuer Identifier Number der ICCSN der Prüfkarte
eGK**

Für dieIssuer Identifier Number(IIN) der ICCSN der Prüfkarte MUSS der
Wert8027600311(gematik) verwendet werden. **[\<=]**

Anmerkung: Die Struktur der ICCSN ist in [gemSpec_Karten_Fach_TIP_G2.1]
vorgegeben

### 4.2 Festlegungen für die IK-Nummer

Die Prüfkarten verwenden eine speziell für Prüfaktivitäten vergebene
Institutionskennzeichnung.

**Card-G2-A_3819 - Vorgegebene IK-Nummer der Prüfkarte eGK**

Für das Institutionskennzeichen (IK-Nummer, veränderlicher Anteil der
20-stelligen KVNR) der Prüfkarte MUSS der 9-stellige Wert109500969verwendet
werden. **[\<=]**

### 4.3 Festlegungen für die Versichertennummer

Als Unterscheidungsmerkmal gegenüber den eGK eines Versicherten sind auf den
Prüfkarten Versichertennummern zu verwenden, die beabsichtigt den Vorgaben zur
Bildung der KVNR nicht folgen und mehr als 3 gleiche und aufeinanderfolgende
Ziffern enthalten.

**Card-G2-A_3820 - Gleiche aufeinanderfolgende Ziffern in der Vorgegebene
Versichertennummern der Prüfkarte eGK**

Die Versichertennummer der Prüfkarte MUSS einer Versichertennummer gemäß:

X0000

nnnn

P, mit

nnnn

aus der Menge {0001 .. 5000} und P = Prüfziffer

entsprechen. **[\<=]**

Anmerkung: Die Prüfziffer (letzte Stelle der Versichertennummer) ist bei
gewähltem nnnn korrekt zu bilden.

### 4.4 Festlegungen des Herausgebers

Der Herausgeber der Prüfkarte eGK ist die gematik. Als Herausgeber nutzt die
gematik die festgelegte IK-Nummer für Prüfaktivitäten und die dieser
IK-Nummer zugeordnete Kennung „Test-GKV-SV“ als Kennzeichnung des
Herausgebers.

**Card-G2-A_3821 - Herausgeber der Prüfkarte eGK**

Zur Kennzeichnung des Herausgebers der Prüfkarte MUSS die Zeichenfolge „Test
GKV-SV“ verwendet werden. **[\<=]**

### 4.5 Festlegungen für die Versichertenstammdaten

**Card-G2-A_3852 - Versichertenstammdaten der Prüfkarte eGK**

Für die Versichertenstammdaten der Prüfkarte MÜSSEN die Angaben aus
TAB_PK_eGK_001 verwendet werden.

Tabelle1: TAB_PK_eGK_001: Versichertenstammdaten der Prüfkarte eGK

<table><tr><td>
Versicherten_ID

</td><td>
siehe: Versichertennummer

</td></tr><tr><td>
CMD_Version (alle)

</td><td>
5.2.0

</td></tr><tr><td>
Nachname

</td><td>
„Ort“ (identisch zu

subjectDN

/s

urName

)

</td></tr><tr><td>
Vorname

</td><td>
„Dienstleister“ (identisch zu

subjectDN

/g

ivenName

)

</td></tr><tr><td>
Vorsatzwort

</td><td>
„vor“

</td></tr><tr><td>
Geburtsdatum

</td><td>
19800101

</td></tr><tr><td>
Geschlecht

</td><td>
„X“

</td></tr><tr><td>
Strasse

</td><td>
„Friedrichstraße“

</td></tr><tr><td>
Hausnummer

</td><td>
136

</td></tr><tr><td>
Ort

</td><td>
„Berlin“

</td></tr><tr><td>
Postleitzahl

</td><td>
10117

</td></tr><tr><td>
Versicherungsschutz Beginn

</td><td>
20000101

</td></tr><tr><td>
Kostenträger

</td><td>
siehe: IK-Nummer

</td></tr><tr><td>
Kostentraegerlaendercode

</td><td>
„D“

</td></tr><tr><td>
Kostentraeger/Name

</td><td>
„Test GKV-SV“ (identisch zu

subjectDN/

o

rganizationName

)

</td></tr><tr><td>
Versichertenart

</td><td>
1

</td></tr><tr><td>
Kostenerstattung (alle)

</td><td>
0

</td></tr><tr><td>
WOP

</td><td>
83

</td></tr><tr><td>
Zuzahlungsstatus/Status

</td><td>
0

</td></tr><tr><td>
Selektivvertraege (alle)

</td><td>
9

</td></tr><tr><td>
Selektivvertraege/Art

</td><td>
0000

</td></tr><tr><td>
Alle weiteren Angaben

</td><td>
„“ (leer)

</td></tr></table>

**[\<=]**

### 5 Bereitstellung der Personalisierungsdaten

Die Bereitstellung der kartenindividuellen Daten für die Erstellung der
Zertifikate und die veränderliche optische Personalisierung der Prüfkarten,
soweit nicht durch das vorliegende Dokument vorgegeben, erfolgt ausschließlich
durch die gematik.

**Card-G2-A_3853 - Bereitstellung der Daten für die Prüfkarte eGK**

Ein Hersteller personalisierter Prüfkarten MUSS für die Personalisierung der
Prüfkarten ausnahmslos Daten verwenden, die durch die gematik bereitgestellt
werden. **[\<=]**

Das Format, der Umfang und die Übermittelungsmethode der Daten an den
Hersteller personalisierter Prüfkarten ist nicht Bestandteil des vorliegenden
Dokuments.

Die gematik stellt mindestens folgende Daten bereit:

Für die Erstellung der Zertifikate C.CH.AUT und C.CH.ENC und für optische
Merkmale der Personalisierung:

 ---> UL

Für die Erstellung der optionalen Zertifikate C.CH.AUTN und C.CH.ENCV:

 ---> UL

Für die Befüllung der EFs des VSDM:

 ---> UL

unter Verwendung der Angaben zuSubjectDNfür C.CH.AUT und C.CH.ENC für die
EinträgeVorname,NachnameundKostenträger/Name.

Die bereitgestellten Daten berücksichtigen die Anforderungen aus Card-G2-A_3818
(ICCSN), Card-G2-A_3819 (IK-Nummer), Card-G2-A_3820 (Versichertennummer),
Card-G2-A_3852 (Versichertenstammdaten) und Card-G2-A_3821 (Herausgeber).

Anmerkung: subjectDN:organizationalUnitName:Institutionskennzeichen und
organizationName sind durch das vorliegende Dokument fest vorgegeben.

Anmerkung: Die bereitgestellten Daten können für mehrere Datensätze
identische Vorgaben aufweisen. Ausgenomen hiervon ist die Versichertennummer,
die für jeden Datensatz unterschiedlich ist.

### 6 Vorgaben für die Zertifikate

Die Erstellung und Personalisierung der Zertifikate der Prüfkarte entspricht
den Vorgaben der eGK eines Versicherten gemäß den Anforderungen in
[gemRL_TSL_SP_CP], [gemSpec_CVC_TSP] und [gemSpec_PKI]. Darüber hinaus gelten
die folgenden Festlegungen.

Die Zertifikate C.CH.AUTN und C.CH.ENCV werden für die Prüfkarten nicht
benötigt.

**Card-G2-A_3822 - Zertifikate C.CH.AUTN und C.CH.ENCV für die Prüfkarte eGK**

Der Hersteller von Prüfkarten KANN die Zertifikate C.CH.AUTN und C.CH.ENCV für
die Prüfkarte erstellen. **[\<=]**

**Card-G2-A_3823 - Vorgegebene Daten für die Zertifikatserstellung für die
Prüfkarte eGK**

Der Hersteller von Prüfkarten MUSS für die Erstellung der Zertifikate
C.CH.AUT, C.CH.ENC, C.CH.AUTN und C.CH.ENCV die Vorgaben in Card-G2-A_3818
(ICCSN), Card-G2-A_3819 (IK-Nummer),Card-G2-A_3820 (Versichertennummer)und
Card-G2-A_3821 (Herausgeber)sowie die von der gematik bereitgestellten Daten
fürSubjectDNberücksichtigen. **[\<=]**

Anmerkung: Die Angaben zu den Zertifikaten beziehen sich immer auf die beiden
kryptographischen Varianten R2048 und E256.

### 7 Personalisiertes Objektsystem der Prüfkarte eGK

Die elektrische Personalisierung der Prüfkarte entspricht grundsätzlich der
elektrischen Personalisierung einer eGK eines Versicherten.

Bei der Personalisierung sind folgende Vorgaben zu beachten:

### 7.1 Schlüssel für die Administration

Für die Prüfkarten ist ein Update der Versichertenstammdaten durch einen
Fachdienst der TI nicht vorgesehen. Darüber hinaus soll es auch nicht möglich
sein, administrative Änderungen an der Prüfkarte vorzunehmen, beispielsweise
um die fest vorgegebene IK-Nummer zu verändern.

**Card-G2-A_3824 - Keine Personalisierung der Schlüssel zur Administration der
Prüfkarte eGK**

Der Hersteller von Prüfkarten DARF die Schlüssel

 ---> UL

zur Administration der Prüfkarte gemäß den Vorgaben der Spezifikation des
Objektsystems der eGK NICHT befüllen. **[\<=]**

### 7.2 QES-Anwendung

**Card-G2-A_3826 - Keine Personalisierung der Objekte in DF.QES der Prüfkarte
eGK**

Der Hersteller von Prüfkarten DARF die Objekte der Anwendung DF.QES
(PrK.CH.QES.XXX, PIN.QES, EF.C.CH.QES.XXX) NICHT personalisieren, falls die
Prüfkarte ein DF.QES enthält (Option QES-Anwendung komplett angelegt und
nutzbar). **[\<=]**

Anmerkung: XXX ist Platzhalter für R2048 oder E256

### 8 Optische Gestaltung der Prüfkarte eGK

Durch eine geeignete optische Gestaltung der Vorder- und Rückseite des
Kartenkörpers der Prüfkarte wird eine visuelle Verwechselung mit einer eGK
eines Versicherten vermieden. Markante optische Elemente einer eGK eines
Versicherten werden für die Prüfkarten bewusst nicht verwendet.

Alle nicht visuell unterscheidbaren Eigenschaften, also technische Maße,
Formate und physikalische Eigenschaften, gelten für Prüfkarten in gleicher
Weise wie für eGK eines Versicherten. Diese Anforderungen sind in
[gemSpec_eGK_OPT] zusammengefasst.

Es müssen aus [gemSpec_eGK_OPT] insbesondere die Vorgaben in Kapitel „Format
und Maße“ und in Kapitel „Kartenkörper und Einbettung des Chips“
berücksichtigt werden.

**Card-G2-A_3827 - Verbotene optische Elemente der Prüfkarte eGK**

Der Hersteller von Prüfkarten DARF die Prüfkarte NICHT mit einem Lichtbild,
dem Logo des BSI, dem Logo „Leonardo“ der eGK eines Versicherten, einem
EHIC-Template auf der Rückseite oder einem Unterschriftenfeld ausstatten.
**[\<=]**

Anmerkung: Das dem gematik-Schriftzug vorangestellte „Leonardo“-Logo
(vitruvianischer Mensch) ist von dieser Anforderung nicht betroffen.

### 8.1 Optische Gestaltung der Kartenvorderseite

### 8.1.1 Unveränderbare optische Gestaltung

**Card-G2-A_3828 - Farbgebung der Kartenvorderseite der Prüfkarte eGK**

Die Grundfarbe der Vorderseite der Prüfkarte MUSS weiß sein. **[\<=]**

**Card-G2-A_3829 - Unveränderbare Elemente der Vorderseite der Prüfkarte eGK**

Der Hersteller von Prüfkarten MUSS die optische Gestaltung der
unveränderlichen Elemente der Vorderseite der Prüfkarte gemäß
Abb_PK_eGK_001 ausführen.

Abbildung1: Abb_PK_eGK_001 Kartenvorderseite am Beispiel der Prüfkarte eGK 
G2.1mit unveränderlichen Elementen   **[\<=]**

**Card-G2-A_3830 - Schriftart und Position des Schriftzugs
„Prüf-Gesundheitskarte“ der Prüfkarte eGK**

Für den Schriftzug „Prüf-Gesundheitskarte“ MUSS die Schriftart Verdana
True Type in der Größe 12 pt fett in Schwarz verwendet werden.Die
Zeichenfolge MUSS rechtsbündig das Maß 80,80 mm vom linken Kartenrand und die
Unterkante das Maß 5,72 mm vom oberen Kartenrand einhalten. **[\<=]**

**Card-G2-A_3831 - Gestaltung des Blocks nationale Farben der Prüfkarte eGK**

Für die Farbgebung des Blocks in den nationalen Farben MÜSSEN Farben der
folgenden Farbwerte (CMYK) verwendet werden:Der Block MUSS über die definierte
Breite in drei gleiche Segmente geteilt sein. Die Farbgebung MUSS von links
nach rechts Schwarz, Rot, Gold sein.Der Block MUSS 1 mm hoch und 30,80 mm breit
sein und rechtsbündig das Maß 80,80 mm vom linken Kartenrand und die
Unterkante das Maß 8,00 mm vom oberen Kartenrand einhalten. **[\<=]**

**Card-G2-A_3832 - Position des gematik-Logos auf der Prüfkarte eGK**

Das gematik-Logo MUSS auf die Prüfkarte aufgebracht werden.Das Logo MUSS 20 mm
breit sein.Das Logo MUSS linksbündig das Maß 3,2 mm vom linken Kartenrand und
die Unterkante das Maß 8,00 mm vom oberen Kartenrand (Unterkante des Blocks
der nationalen Farben) einhalten. **[\<=]**

Anmerkung: Eine Bilddatei des gematik-Logos kann im Rahmen der Übermittlung der
Personalisierungsdaten durch die gematik zur Verfügung gestellt werden.

**Card-G2-A_3833 - Gestaltung des Farbfeldes der Prüfkarte eGK**

Das auffällige Farbfeld der Prüfkarte MUSS einheitlich gemäß der folgenden
Vorgabe beschriftet und aufgebracht werden: **[\<=]**

**Card-G2-A_3834 - Schriftart und Position der Legenden der Prüfkarte eGK**

Für die Legenden MUSS einheitlich die Schriftart Verdana True Type 5 pt in
Schwarz verwendet werden.Die Zeichenfolgen MÜSSEN für die Unterkante das Maß
52,00 mm vom oberen Kartenrand einhalten.Die Zeichenfolge „Test-IK“ MUSS
linksbündig das Maß 3,2 mm vom linken Kartenrand einhalten.Die Zeichenfolge
„Prüfkartennummer“ MUSS linksbündig das Maß 31,00 mm vom linken
Kartenrand einhalten.Die Zeichenfolge „ICCSN“ MUSS linksbündig das Maß
58,80 mm vom linken Kartenrand einhalten. **[\<=]**

**A_14283 - Optische Kennzeichnung der Generation der Prüfkarte eGK**

Zur optischen Kennzeichnung der Generation der Prüfkarte MUSS für Prüfkarten
der Generation G2 der Schriftzug „G 2“ und für Prüfkarten der Generation
G2.1 der Schriftzug „G 2.1“ verwendet werden. **[\<=]**

**Card-G2-A_3835 - Schriftart und Position der Kennzeichnung der Generation der
Prüfkarte eGK**

Für den Schriftzug zur Kennzeichnung der Generation der Prüfkarte MUSS die
Schriftart Verdana True Type in der Größe 6 pt fett in Schwarz verwendet
werden.Die Zeichenfolge MUSS rechtsbündig das Maß 80,80 mm vom linken
Kartenrand und die Unterkante das Maß 10,50 mm vom oberen Kartenrand
einhalten. **[\<=]**

### 8.1.2 Veränderbare optische Gestaltung

**Card-G2-A_3836 - Veränderbare Elemente der Vorderseite der Prüfkarte eGK**

Der Hersteller von Prüfkarten MUSS die optische Gestaltung der veränderlichen
Elemente der Vorderseite der Prüfkarte gemäß Abb_PK_eGK_002 ausführen.

Abbildung2: Abb_PK_eGK_002 Kartenvorderseite am Beispiel der Prüfkarte eGK
G2.1mit veränderlichen Elementen (Inhalte beispielhaft) **[\<=]**

**Card-G2-A_3837 - Vorgabe Beschriftung Personalisierungsfeld der Prüfkarte
eGK**

Das Personalisierungsfeld der Prüfkarte MUSS einheitlich gemäß der folgenden
Vorgabe beschriftet werden:

<table><tr><td>
Schrifttyp:

</td><td>
Verdana True Type, 10 pt, Groß- und Kleinbuchstaben

</td></tr><tr><td>
Zeilenabstand:

</td><td>
2 pt zuzüglich Zeichengröße

</td></tr><tr><td>
Zeilen:

</td><td>
Zeile 1 - 3

</td></tr><tr><td>
Farbe:

</td><td>
Schwarz

</td></tr><tr><td>
Unterkante:

</td><td>
49,50 mm vom oberen Kartenrand (Unterkante 3. Zeile)

</td></tr><tr><td>
Zeile 1:

</td><td>
Die Zeichenfolge der Kennung der Prüfidentität mit maximal 28 Zeichen
linksbündig gemäß dem linksbündigen Maß der Legende „Test-IK“

</td></tr><tr><td>
Zeile 2:

</td><td>
Die Zeichenfolge „Ablaufdatum:“ linksbündig gemäß dem linksbündigen Maß
der Legende „Test-IK“

</td></tr><tr><td>
Zeile 2:

</td><td>
Die Datumsangabe zum Ablaufdatum linksbündig gemäß dem linksbündigen Maß
der Legende „Prüfkartennummer“ im Format TT/MM/YYYY

</td></tr><tr><td>
Zeile 3:

</td><td>
9-stelliges Institutionskennzeichen (IK-Nummer) der Prüfkarteninstitution,
linksbündig gemäß dem linksbündigen Maß der Legende „Test-IK“

</td></tr><tr><td>
Zeile 3:

</td><td>
10-stellige Versichertennummer der Prüfidentität, linksbündig gemäß dem
linksbündigen Maß der Legende „Prüfkartennummer“

</td></tr><tr><td>
Zeile 2 und 3:

</td><td>
20-stellige ICCSN, jeweils 10 Stellen pro Zeile linksbündig gemäß dem
linksbündigen Maß der Legende „ICCSN“

</td></tr></table>

**[\<=]**

**Card-G2-A_3825 - Aufgedrucktes Ablaufdatum der Prüfkarte eGK**

Das aufgedruckte Ablaufdatum in Zeile 2 MUSS mit dem Ablaufdatum (validity –
bis) des Zertifikats C.CH.AUT übereinstimmen. **[\<=]**

**Card-G2-A_3838 - Aufgedruckte ICCSN der Prüfkarte eGK**

Die aufgedruckte Ziffernfolge der ICCSN MUSS mit der personalisierten ICCSN im
Wertefeld desDO_ICCSNim Objekt MF/EF.GDO des Objektsystems übereinstimmen.
**[\<=]**

**Card-G2-A_3839 - Aufgedrucktes Institutionskennzeichen der Prüfkarte eGK**

Das aufgedruckte Institutionskennzeichen (IK-Nummer) MUSS mit dem
ElementorganizationalUnitName[OU=Institutionskennzeichen]des personalisierten
Zertifikats C.CH.AUT der Prüfkarte übereinstimmen. **[\<=]**

Anmerkung: die IK-Nummer ist in Card-G2-A_3819 festgelegt

**Card-G2-A_3840 - Aufgedruckte Zeichenfolge der Kennung der Prüfidentität der
Prüfkarte eGK**

Die aufgedruckte Zeichenfolge der Kennung der Prüfidentität MUSS mit dem
ElementsubjectDN:CommonNamedes personalisierten Zertifikats C.CH.AUT der
Prüfkarte übereinstimmen. **[\<=]**

**Card-G2-A_3841 - Aufgedruckte Versichertennummer der Prüfkarte eGK**

Die aufgedruckte Versichertennummer MUSS mit dem unveränderbaren Teil der
KV-Nummer im ElementsubjectDN:organizationalUnitName [unveränderbarer Teil der
KV-Nummer]des personalisierten Zertifikats C.CH.AUT der Prüfkarte
übereinstimmen. **[\<=]**

### 8.2 Optische Gestaltung der Kartenrückseite

**Card-G2-A_3842 - Farbgebung der Kartenrückseite der Prüfkarte eGK**

Die Rückseite der Prüfkarte MUSS weiß sein. **[\<=]**

**Card-G2-A_3843 - Gestaltung der Kartenrückseite der Prüfkarte eGK**

Die Rückseite der Prüfkarte DARF NICHT bedruckt sein. **[\<=]**

### 9 Anhang A – Verzeichnisse

### 9.1 Abkürzungen

<table><tr><th>
Kürzel

</th><th>
Erläuterung

</th></tr><tr><td>
BSI

</td><td>
Bundesamt für die Sicherheit in der Informationstechnik

</td></tr><tr><td>
DF

</td><td>
Dedicated File

</td></tr><tr><td>
DO_ICCSN

</td><td>
Datenobjekt in EF.GDO. Enthält im Wertfeld die ICCSN

</td></tr><tr><td>
EF

</td><td>
Elementary File

</td></tr><tr><td>
eGK

</td><td>
elektronische Gesundheitskarte

</td></tr><tr><td>
EHIC

</td><td>
Europäische Krankenversichertenkarte

</td></tr><tr><td>
ICCSN

</td><td>
Integrated Chip Card Serial Number

</td></tr><tr><td>
IIN

</td><td>
Issuer Identifier Number, Kennung des Kartenanbieters

</td></tr><tr><td>
IK

</td><td>
Kennzeichen für Leistungsträger und Leistungserbringer gemäß § 293 SGB V

</td></tr><tr><td>
KVNR

</td><td>
Krankenversichertennummer

</td></tr><tr><td>
PIN

</td><td>
Persönliche Identifikationsnummer

</td></tr><tr><td>
PUK

</td><td>
Pin Unblocking Key

</td></tr><tr><td>
TSP

</td><td>
Trusted Service Provider

</td></tr><tr><td>
VSDM

</td><td>
Versicherten-Stammdaten-Management

</td></tr></table>

### 9.2 Abbildungsverzeichnis



### 9.3 Tabellenverzeichnis

- [Tabelle-1] - TAB_PK_eGK_001: Versichertenstammdaten der Prüfkarte eGK

### 9.4 Referenzierte Dokumente

### 9.4.1 Dokumente der gematik

Die nachfolgende Tabelle enthält die Bezeichnung der in dem vorliegenden
Dokument referenzierten Dokumente der gematik zur Telematikinfrastruktur. Die
konkrete Version der Dokumente kann der Dokumentenlandkarte des
Spezifikations-Releases entnommen werden. Diese wird zusammen mit den
Dokumenten auf der Internetseite der gematik bereitgestellt

<table><tr><th>
[Quelle]

</th><th>
Herausgeber (Erscheinungsdatum): Titel

</th></tr><tr><td>
[gemSpec_eGK_ObjSys_G2.1]

</td><td>
gematik: Spezifikation der elektronischen Gesundheitskarte eGK-Objektsystem für
eGK der Generation 2.1

</td></tr><tr><td>
[gemProdT_eGK_ObjSys_G2.1]

</td><td>
gematik: Produkttypsteckbrief Zulassungsobjekt eGK-Objektsystem Generation G2.1

</td></tr><tr><td>
[gemSpec_eGK_ObjSys]

</td><td>
gematik: Spezifikation der elektronischen Gesundheitskarte eGK-Objektsystem

</td></tr><tr><td>
[gemProdT_eGK_ObjSys]

</td><td>
gematik: Produkttypsteckbrief Zulassungsobjekt eGK-Objektsystem

</td></tr><tr><td>
[gemSpec_eGK_OPT]

</td><td>
gematik: Spezifikation der elektronischen Gesundheitskarte - Äußere Gestaltung
für eGK der Generation 2

</td></tr><tr><td>
[gemSpec_Karten_Fach_TIP_G2.1]

</td><td>
gematik: Befüllvorschriften für die Plattformanteile der Karten der TI der
Generation G2.1

</td></tr><tr><td>
[gemRL_TSL_SP_CP]

</td><td>
gematik: Certificate Policy

</td></tr><tr><td>
[gemSpec_CVC_TSP]

</td><td>
gematik: Spezifikation Trust Service Provider CVC

</td></tr><tr><td>
[gemSpec_PKI]

</td><td>
gematik: Spezifikation PKI

</td></tr><tr><td>
[gemSysL_VSDM]

</td><td>
gematik: Systemspezifisches Konzept VSDM

</td></tr></table>

### 9.4.2 Weitere Dokumente

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
[1]:                     #1-einführung-des-dokuments
[1.1]:                   #11-zielsetzung
[1.2]:                   #12-zielgruppe
[1.3]:                   #13-geltungsbereich
[1.4]:                   #14-abgrenzung-des-dokuments
[1.5]:                   #15-methodik
[1.6]:                   #16-nomenklatur
[2]:                     #2-initialisiertes-objektsystem-der-prüfkarte-egk
[3]:                     #3-personalisierungsvalidierung
[4]:                     #4-festlegungen-für-personalisierungsdaten
[4.1]:                   #41-festlegungen-für-die-iccsn
[4.2]:                   #42-festlegungen-für-die-ik-nummer
[4.3]:                   #43-festlegungen-für-die-versichertennummer
[4.4]:                   #44-festlegungen-des-herausgebers
[4.5]:                   #45-festlegungen-für-die-versichertenstammdaten
[5]:                     #5-bereitstellung-der-personalisierungsdaten
[6]:                     #6-vorgaben-für-die-zertifikate
[7]:                     #7-personalisiertes-objektsystem-der-prüfkarte-egk
[7.1]:                   #71-schlüssel-für-die-administration
[7.2]:                   #72-qes-anwendung
[8]:                     #8-optische-gestaltung-der-prüfkarte-egk
[8.1]:                   #81-optische-gestaltung-der-kartenvorderseite
[8.1.1]:                 #811-unveränderbare-optische-gestaltung
[8.1.2]:                 #812-veränderbare-optische-gestaltung
[8.2]:                   #82-optische-gestaltung-der-kartenrückseite
[9]:                     #9-anhang-a-–-verzeichnisse
[9.1]:                   #91-abkürzungen
[9.2]:                   #92-abbildungsverzeichnis
[9.3]:                   #93-tabellenverzeichnis
[9.4]:                   #94-referenzierte-dokumente
[9.4.1]:                 #941-dokumente-der-gematik
[9.4.2]:                 #942-weitere-dokumente
[Tbl-001]:               #Tbl-001 (&93834808917624)
[Tabelle-1]:             #Tabelle-1 (&93834777755168)
[Tbl-003]:               #Tbl-003 (&93834783634960)
[Tbl-004]:               #Tbl-004 (&93834781671000)
[Tbl-005]:               #Tbl-005 (&93834781727008)
[Tbl-006]:               #Tbl-006 (&93834808820744)
[http://tools.ietf.org/html/rfc2119]: http://tools.ietf.org/html/rfc2119 (&93834808827576)
