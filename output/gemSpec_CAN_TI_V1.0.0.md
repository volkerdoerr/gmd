
Elektronische Gesundheitskarte und Telematikinfrastruktur

### Übergreifende Spezifikation CAN-Policy

- Klassifizierung: öffentlich
- Referenzierung: gemSpec_CAN_TI
- Revision: 548770
- Stand: 30.05.13
- Status: freigegeben
- Version: 1.0.0

### Dokumentinformationen

Änderungen zur Vorversion

Es handelt sich hier um eine Erstveröffentlichung

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
Bearbeitung

</th></tr><tr><td>
0.1.0

</td><td>
</td><td>
</td><td>
Ersterstellung

</td><td>
ITS/SI

</td></tr><tr><td>
0.5.0

</td><td>
24.05.13

</td><td>
</td><td>
zur Abstimmung freigegeben

</td><td>
PL P706

</td></tr><tr><td>
1.0.0

</td><td>
30.05.13

</td><td>
</td><td>
freigegeben

</td><td>
PL P706

</td></tr><tr><td>
1.0.0

</td><td>
06.06.13

</td><td>
freigegeben

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
  - [1.4] Abgrenzung
  - [1.5] Methodik
- [2] Anforderungen an eine CAN
- [3] Anhang A – Verzeichnisse
  - [3.1] Abkürzungen
  - [3.2] Glossar
  - [3.3] Referenzierte Dokumente
    - [3.3.1] Dokumente der gematik
    - [3.3.2] Weitere Dokumente

### 1 Einordnung des Dokumentes

### 1.1 Zielsetzung

Die übergreifende CAN-Policy gilt für Smartcards der TI, die eine kontaktlose
Schnittstelle nutzen. Die Anforderungen der übergreifenden CAN-Policy stellen
sicher, dass die CAN auf einem adäquaten Sicherheitsniveau geschützt wird.

### 1.2 Zielgruppe

Das Dokument richtet sich an Kartenherausgeber von kontaktlosen Karten im
Gesundheitswesen. Derzeit sind dies eGK und HBA. Kartenherausgeber können
Dritte mit der Kartenpersonalisierung beauftragen. In diesem Fall, in dem der
Kartenherausgeber operative Aufgaben durch einen Dritten wahrnehmen lässt,
muss der beauftragte Auftragnehmer die Anforderungen einhalten. Es bleibt
jedoch in der Verantwortung des Kartenherausgebers sicherzustellen, dass der
Beauftragte die Anforderungen umsetzt. Bei der Auswahl des Auftragnehmers ist
hierauf zu achten.

### 1.3 Geltungsbereich

Dieses Dokument enthält normative Festlegungen zur Telematikinfrastruktur des
deutschen Gesundheitswesens. Der Gültigkeitszeitraum der vorliegenden Version
und deren Anwendung in Zulassungsverfahren wird durch die gematik GmbH in
gesonderten Dokumenten (z.B. Dokumentenlandkarte, Produkttypsteckbrief,
Leistungsbeschreibung) festgelegt und bekannt gegeben.

Wichtiger Schutzrechts-/Patentrechtshinweis:

Das vorliegende Sicherheitskonzept ist von der gematik allein unter technischen
Gesichtspunkten erstellt worden. Im Einzelfall kann nicht ausgeschlossen
werden, dass die Implementierung der Spezifikation in technische Schutzrechte
Dritter eingreift. Es ist allein Sache des Anbieters oder Herstellers, durch
geeignete Maßnahmen dafür Sorge zu tragen, dass von ihm aufgrund der
Spezifikation angebotene Produkte und/oder Leistungen nicht gegen Schutzrechte
Dritter verstoßen und sich ggf. die erforderlichen Erlaubnisse/Lizenzen von
den betroffenen Schutzrechtsinhabern einzuholen. Die gematik übernimmt
insofern keinerlei Gewährleistungen

### 1.4 Abgrenzung

Das Dokument definiert Anforderungen an Produkte und Verfahren, stellt jedoch
keine Lösungsbeschreibungen dar.

### 1.5 Methodik

Für die genauere Unterscheidung zwischen normativen und informativen Inhalten
werden die dem RFC 2119 [RFC2119] entsprechenden in Großbuchstaben
geschriebenen, deutschen Schlüsselworte (MUSS, DARF NICHT, SOLL, SOLL NICHT,
KANN) verwendet.

Sie werden im Dokument wie folgt dargestellt:

\<AFO-ID\> - \<Titel der Afo\>Text / Beschreibung[ \<=]

Dabei umfasst die Anforderung sämtliche innerhalb der Textmarken angeführten
Inhalte.

### 2 Anforderungen an eine CAN

Smartcards in der TI (eGK und HBA) können neben einer kontaktbehafteten
Schnittstelle optional eine kontaktlose Schnittstelle nutzen. Soll über die
kontaktlose Schnittstelle auf die Karte zugegriffen werden, ist als
zusätzliche Zugriffsbedingung die Eingabe der „Card Access Number“ (CAN)
am Kartenterminal erforderlich. Die CAN ist eine auf der Karte aufgedruckte
Nummer, die auch im Chip der Karte gespeichert ist.

Die CAN wird als gemeinsames Geheimnis für den Aufbau eines kryptographisch
geschützten Kanals zwischen einer kontaktlosen Smartcard und einem
Kartenterminal nach dem PACE-Protokoll (Password Authenticated Connection
Establishment) [ICAO-MRTD-2010] verwendet.

Die Sicherheitsziele des Kanals sind:

 ---> OL

Im Folgenden werden für die CAN vom Kartenherausgeber einzuhaltende
Anforderungen beschrieben. Weitere Anforderungen an die CAN der spezifischen
Karte können in den Spezifikationen zu den Karten festgelegt werden.

**GS-A_5115 - Schutzbedarf der CAN**

Der Kartenherausgeberoder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSSsicherstellen,
dass die CAN in seinem System inklusive der Aushändigung der Karte an den
Karteninhaberdurch Maßnahmen und Prozesse geschützt wird, die den
inTab_SBF_CANfestgelegten Schutzbedarf wirksam gewährleisten.

Tabelle1–Tab_SBF_CAN,Schutzbedarfsfeststellung CAN

<table><tr><th>
Schutzziel

</th><th>
Vertraulichkeit

</th><th>
Integrität

</th><th>
Authentizität

</th></tr><tr><td>
Schutzbedarf

</td><td>
hoch

</td><td>
mittel

</td><td>
n.a.

</td></tr></table>

**[\<=]**

**GS-A_5116 - Zufällige CAN-Erzeugung**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS sicherstellen,
dass dieCANzufällig oder pseudozufälligerzeugt wird. **[\<=]**

**GS-A_5117 - Anforderungen an Zufallsgenerator für CAN-Erzeugung**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSSsicherstellen,
dassder zur Erzeugung der CAN verwendete Zufalls- oder Pseudozufallsgenerator
die vorgegebenen Mindestanforderungen der gematik entsprechend
[gemSpec_Krypt#GS-A_4367] erfüllt. **[\<=]**

**GS-A_5118 - CAN-Speicherung nur für die Personalisierung der Karte**

Der Kartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der Kartenpersonalisierer MUSS die CAN aus
seinenSystemen unverzüglich löschen, sobald die CAN für die Personalisierung
der Karte nicht mehr erforderlich ist. **[\<=]**

**GS-A_5119 - Sicherer Transport und Speicherung der CAN beim Kartenherausgeber
bzw. Kartenpersonalisierer**

Der Kartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der Kartenpersonalisierer MUSS
sicherstellen, dass die CANwährend desTransportesundderSpeicherung vor nicht
autorisierter Aufdeckung und Weitergabe geschützt wird. **[\<=]**

**GS-A_5120 - Verteilung der CAN auf das erforderliche Maß beschränken**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS sicherstellen,
dass die Verteilung derCANauf das absolut notwendige Maß eingeschränkt wird,
um die Möglichkeiten zur Kompromittierung derCANzu minimieren und potentielle
Schäden zu beschränken. **[\<=]**

**GS-A_5121 - Karteninhaber über Umgang mit CAN informieren**

Der KartenherausgeberMUSSden Karteninhaber über den Umgang mit der CANauf der
von ihm herausgegebenenKarte informieren. **[\<=]**

### 3 Anhang A – Verzeichnisse

### 3.1 Abkürzungen

<table><tr><th>
Kürzel

</th><th>
Erläuterung

</th></tr><tr><td>
CAN

</td><td>
Card Access Number

</td></tr><tr><td>
eGK

</td><td>
elektronische Gesundheitskarte

</td></tr><tr><td>
HBA

</td><td>
(elektronischer) Heilberufsausweis

</td></tr><tr><td>
PACE

</td><td>
Password Authenticated Connection Establishment

</td></tr><tr><td>
TI

</td><td>
Telematikinfrastruktur

</td></tr></table>

### 3.2 Glossar

Das Glossar wird als eigenständiges Dokument zur Verfügung gestellt.

### 3.3 Referenzierte Dokumente

### 3.3.1 Dokumente der gematik

Die nachfolgende Tabelle enthält die Bezeichnung der in dem vorliegenden
Dokument referenzierten Dokumente der gematik zur Telematikinfrastruktur. Der
mit der vorliegenden Version korrelierende Entwicklungsstand dieser Konzepte
und Spezifikationen wird pro Release in einer Dokumentenlandkarte definiert;
Version und Stand der referenzierten Dokumente sind daher in der nachfolgenden
Tabelle nicht aufgeführt. Deren zu diesem Dokument jeweils gültige
Versionsnummer entnehmen Sie bitte der aktuellen, auf der Internetseite der
gematik veröffentlichten Dokumentenlandkarte, in der die vorliegende Version
aufgeführt wird.

<table><tr><th>
[Quelle]

</th><th>
Herausgeber (Erscheinungsdatum): Titel

</th></tr><tr><td>
[gemSpec_Krypt]

</td><td>
gematik: Verwendung kryptographischer Algorithmen in der Telematikinfrastruktur

</td></tr></table>

### 3.3.2 Weitere Dokumente

<table><tr><th>
[Quelle]

</th><th>
Herausgeber (Erscheinungsdatum): Titel

</th></tr><tr><td>
[ICAO-MRTD-2010]

</td><td>
ICAO. Supplemental Access Control for Machine Readable Travel Documents,
Technical Report, 2010

</td></tr></table>





[Dokumentinformationen]: #dokumentinformationen
[Inhaltsverzeichnis]:    #inhaltsverzeichnis
[1]:                     #1-einordnung-des-dokumentes
[1.1]:                   #11-zielsetzung
[1.2]:                   #12-zielgruppe
[1.3]:                   #13-geltungsbereich
[1.4]:                   #14-abgrenzung
[1.5]:                   #15-methodik
[2]:                     #2-anforderungen-an-eine-can
[3]:                     #3-anhang-a-–-verzeichnisse
[3.1]:                   #31-abkürzungen
[3.2]:                   #32-glossar
[3.3]:                   #33-referenzierte-dokumente
[3.3.1]:                 #331-dokumente-der-gematik
[3.3.2]:                 #332-weitere-dokumente
[Tbl-001]:               #Tbl-001 (&93834775410952)
[Tbl-002]:               #Tbl-002 (&93834775671888)
[Tbl-003]:               #Tbl-003 (&93834768413184)
[Tbl-004]:               #Tbl-004 (&93834765146376)
[Tbl-005]:               #Tbl-005 (&93834765153040)
