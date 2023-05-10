
Elektronische Gesundheitskarte und Telematikinfrastruktur

### 

- Klassifizierung: öffentlich
- Referenzierung: gemSpec_SST_LD_BD
- Revision: 548770
- Stand: 30.06.2020
- Status: freigegeben
- Version: 1.2.0

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
Kap./Seite

</th><th>
Grund der Änderung, besondere Hinweise

</th><th>
Bearbeitung

</th></tr><tr><td>
1.0.0

</td><td>
15.05.19

</td><td>
</td><td>
freigegeben

</td><td>
gematik

</td></tr><tr><td>
1.0.1

</td><td>
28.06.19

</td><td>
Begriffsklarstellung

</td><td>
gematik

</td></tr><tr><td>
1.1.0

</td><td>
03.02.20

</td><td>
Einarbeitung lt. Änderungsliste P21.1

</td><td>
gematik

</td></tr><tr><td>
1.1.1

</td><td>
26.06.20

</td><td>
Einarbeitung lt. Änderungsliste P21.3

</td><td>
gematik

</td></tr><tr><td>
1.2.0

</td><td>
30.06.20

</td><td>
Anpassungen gemäß Änderungsliste P22.1 und Scope-Themen aus Systemdesign
R4.0.0

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
- [2] Systemüberblick
- [3] Schnittstelle I_LogData
  - [3.1] Transport Layer Security (TLS)
  - [3.2] DNS Resource Record
  - [3.3] Willenserklärungen zur Konnektor-Logdatenerfassung
  - [3.4] Datei Upload
- [4] Schnittstelle I_OpsData_Update
  - [4.1] Transport Layer Security (TLS)
  - [4.2] DNS Resource Record
  - [4.3] Datei Upload
- [5] Anhang – Verzeichnisse
  - [5.1] Abkürzungen
  - [5.2] Glossar
  - [5.3] Abbildungsverzeichnis
  - [5.4] Tabellenverzeichnis
  - [5.5] Referenzierte Dokumente
    - [5.5.1] Dokumente der gematik
    - [5.5.2] Weitere Dokumente

### 1 Einordnung des Dokuments

### 1.1 Zielsetzung

Dieses Dokument enthält die Anforderungen an die SchnittstelleLogdaten-
und Betriebsdatenerfassung. Über sie werden von den Clients (z.B. Konnektoren
und Fachdienste) versendete Betriebsdaten empfangen.

### 1.2 Zielgruppe

Das Dokument richtet sich an Hersteller und Anbieter der Schnittstelle Logdaten-
und Betriebsdatenerfassung sowie an die Hersteller der Clients (z.B.
Konnektoren und Fachdienste).

### 1.3 Geltungsbereich

Dieses Dokument enthält normative Festlegungen zur Telematikinfrastruktur des
Deutschen Gesundheitswesens für den Online-Produktivbetrieb (Stufe 2). Der
Gültigkeitszeitraum der vorliegenden Version und deren Anwendung in
Zulassungs- oder Abnahmeverfahren wird durch die gematik GmbH in gesonderten
Dokumenten (z.B. Dokumentenlandkarte, Produkttypsteckbrief,
Leistungsbeschreibung) festgelegt und bekannt gegeben.

Wichtiger Schutzrechts-/Patentrechtshinweis

Die nachfolgende Spezifikation ist von der gematik allein unter technischen
Gesichtspunkten erstellt worden. Im Einzelfall kann nicht ausgeschlossen
werden, dass die Implementierung der Spezifikation in technische Schutzrechte
Dritter eingreift. Es ist allein Sache des Anbieters oder Herstellers, durch
geeignete Maßnahmen dafür Sorge zu tragen, dass von ihm aufgrund der
Spezifikation angebotene Produkte und/oder Leistungen nicht gegen Schutzrechte
Dritter verstoßen und sich ggf. die erforderlichen Erlaubnisse/Lizenzen von
den betroffenen Schutzrechtsinhabern einzuholen. Die gematik GmbH übernimmt
insofern keinerlei Gewährleistungen.

### 1.4 Abgrenzungen

Spezifiziert werden in diesem Dokument die Anforderungen und das Verhalten der
Schnittstellen Logdatenerfassung  [I_LogData] und  Betriebsdatenerfassung
[I_OpsData_Update]. Daraus resultieren ebenfalls Abläufe in den Clients dieser
Schnittstelle (z.B. den Konnektoren).

Für das Verständnis dieser Spezifikation wird die Kenntnis von
[gemKPT_Arch_TIP] vorausgesetzt.

Dieses Dokument beschreibt für die über I_LogData gelieferten Daten nicht:

 ---> UL

### 1.5 Methodik

Anforderungen als Ausdruck normativer Festlegungen werden durch eine eindeutige
ID sowie die dem RFC2119[RFC2119] entsprechenden, in Großbuchstaben
geschriebenen deutschen Schlüsselworte MUSS, DARF NICHT, SOLL, SOLL NICHT,
KANN gekennzeichnet.Sie werden im Dokument wie folgt dargestellt:\<AFO-ID\> -
\<Titel der Afo\>Text / Beschreibung [\<=]Dabei umfasst die Anforderung
sämtliche zwischen Afo-ID und der Textmarke [\<=] angeführten Inhalte.

### 2 Systemüberblick

In folgender Abbildung ist die Einbettung der Schnittstelle
Logdatenerfassung [I_LogData] in die TI dargestellt.

![Abbildung-1][Abbildung-1]

Nach Einwilligung des Leistungserbringers werden alle Logdaten des Konnektors
periodisch pseudonymisiert und mit einigen Metadaten angereichert an
[I_LogData] gesendet. Von dort werden sie weiter an ein Logdaten-Analyse-System
gesendet. Die Einwilligungserklärung und die Widerspruchserklärung werden dem
Konnektor über Operation I_LogData::getFile bereitgestellt.

Beispielablauf für den Konnektor:

 ---> OL

Die Fachdienste und zentralen Dienste können ihre Betriebsdaten über die
Schnittstelle Betriebsdatenerfassung I_OpsData_Update mit Operation
[I_OpsData_Update]::fileUpload liefern. 

### 3 Schnittstelle I_LogData

Die Konnektoren liefern ihre Logdaten über die Schnittstelle
Logdatenerfassung I_LogData. 

### 3.1 Transport Layer Security (TLS)

Die Schnittstelle I_LogData wird durch TLS abgesichert.

**A_17108 - Schnittstelle Logdatenerfassung Konnektor TLS-Authentisierung durch
den I_LogData-Server**

Die Schnittstelle I_LogData MUSS bei der Absicherung der Verbindung durch TLS
die serverseitige Authentisierung unter Nutzung des
X.509-Komponentenzertifikats mit der TLS-Server-Identität ID.ZD.TLS_S zur
Serverauthentisierung umsetzen. **[\<=]**

**A_17109 - Schnittstelle Logdatenerfassung Keine Verbindungen ohne TLS**

Die Schnittstelle I_LogData MUSS ausschließlich Verbindungen mit TLS
akzeptieren. **[\<=]**

### 3.2 DNS Resource Record

Die Schnittstelle I_LogData stellt Funktionen bereit, die über URLs aufgerufen
werden können.

**A_17182 - Schnittstelle Logdatenerfassung Bereitstellung DNS-Resource-Records**

Der Anbieter der Schnittstelle Logdatenerfassung I_LogData MUSS SRV- und
TXT-Resource-Records im DNS bereitstellen. Die Werte der PFADx-Angaben MÜSSEN
mit einem "/" beginnen.Im DNS sind dazu folgende Einträge
einzutragen:Owner                                  TTL
Class Type Data_logDataIf._tcp.\<TOP_LEVEL_DOMAIN_TI\> \<TTL1\> \<IN\> \<SRV\>
\<Priorität1\>  \<Gewicht1\>  \<Port1\>  \<FQDN1\>_logDataIf._tcp.\<TOP_LEVEL_DOMAIN_TI\>
\<TTL2\> \<IN\> \<TXT\> "txtvers=\<VERSION1\>"
"path=\<PFAD1\>"_logDataIf._tcp.\<TOP_LEVEL_DOMAIN_TI\> \<TTL3\> \<IN\> \<SRV\>
\<Priorität2\>  \<Gewicht2\>  \<Port2\>  \<FQDN2\>_logDataIf._tcp.\<TOP_LEVEL_DOMAIN_TI\>
\<TTL4\> \<IN\> \<TXT\> "txtvers=\<VERSION2\>"
"path=\<PFAD2\>"TOP_LEVEL_DOMAIN_TI: in der PU = telematik.; in der RU/TU =
telematik-test. **[\<=]**

Die "ldif"-DNS-Resource-Records werden von den Konnektoren zur Lokalisierung der
Schnittstelle genutzt.

### 3.3 Willenserklärungen zur Konnektor-Logdatenerfassung

Der Leistungserbringer muss der Verarbeitung seiner Konnektor-Logdaten
zustimmen. Zur Unterstützung dieses Prozesses wird die Einwilligungs- und
Widerrufserklärung über die Schnittstelle I_LogData bereitgestellt. Weiterhin
werden die statischen Metadaten (welche keine personenbezogenen Daten
enthalten) aus der Einwilligungserklärung und die Widerrufserklärung vom
Konnektor an die Schnittstelle gesendet.

Die Schnittstelle I_LogData erlaubt den Download von vordefinierten Dateien
durch den Konnektor, die in diesem Kapitel definiert werden. Dazu gehören
Dateien wie die Einwilligungserklärung und die Widerspruchserklärung für die
Logdatenerfassung, welche durch den Leistungserbringer ausgefüllt werden
müssen.

Der Zugriff auf Dateien, die von I_LogData-Clients mit HTTP POST bereitgestellt
werden, ist nicht möglich.

**A_17170 - Schnittstelle Logdatenerfassung I_LogData::getFile**

Die Schnittstelle I_LogData MUSS die Operation I_LogData::getFile für die
Übertragung von vordefinierten Dateien (siehe A_17203 und A_17172) an Clients
entsprechend Tabelle Tab_I_LogData_001 bereitstellen.

Tabelle1: Tab_I_LogData_001 Operation I_LogData::getFile

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
Name

</td><td>
I_LogData::getFile

</td></tr><tr><td>
Beschreibung

</td><td>
Mit dieser Operation ruft der Client eine Datei ab. Die Dateien werden mit
vordefinierten Dateinamen bereitgestellt. Der Client muss den Dateinamen kennen
(der in diesem Kapitel definiert wird).

Mit jedem Aufruf dieser Operation wird ein File

übertragen.

</td></tr><tr><td>
Initiierender Akteur

</td><td>
Client von I_LogData

</td></tr><tr><td>
Weitere Akteure

</td><td>
keine

</td></tr><tr><td>
Auslöser

</td><td>
Client von I_LogData

</td></tr><tr><td>
Vorbedingungen

</td><td>
aufgebaute TLS-Verbindung vom Client

</td></tr><tr><td>
Nachbedingungen

</td><td>
Client von I_LogData hat die Datei vorliegen.

</td></tr><tr><td>
Aufruf

</td><td>
Aufruf

von HTTP GET mit der

URL

"

https://\<host\>:\<port\>\<path\>/\<filename\>?LEI-ID=Wert

(\<host\>:\<port\>

" w

ird durch Abfrage des

DNS SRV-Resource-Records

  

ermittelt.

"

\<path\>

" 

wird durch Abfrage des DNS TXT-Resource-Records ermittelt.

"

\<filename\>

" 

entspricht dem Filename der Datei inklusive absolutem

Pfad.

Mit dem

optionalen

Parameter

"

LEI-ID

" 

kann die Leistungsbringer-ID übergeben werden, welche dann in das
bereitgestellte Dokument übernommen wird.

Mindestens folgende Top-level-HTTP-Header MÜSSEN mit den angegebenen Werten
unterstützt werden:

 ---> UL

</td></tr><tr><td>
Standardablauf

</td><td>
Die angeforderte Datei wird dem aufrufenden Client zurückgegeben.

</td></tr><tr><td>
Fehlerfälle

</td><td>
Neben den Fehlercodes des aufgerufenen HTTP GET können keine weiteren
Fehlercodes auftreten.

</td></tr></table>

**[\<=]**

**A_17172 - Schnittstelle Logdatenerfassung Bereitstellung
Einwilligungserklärung**

Die Schnittstelle I_LogData MUSS über die Operation I_LogData::getFile die
Datei "LDA_Einwilligungserklaerung.html" für alle Clients bereitstellen. Der
lesende Zugriff auf diese Datei MUSS auch ohne Authentisierung auf HTTP-Ebene
(ohne Authorization-Parameter) möglich sein. **[\<=]**

**A_17805 - Schnittstelle Logdatenerfassung Aufnahme LEI-ID in
Einwilligungserklärung**

Wenn mit Operation I_LogData::getFile nach der URL im HTTP GET der Parameter
LEI-ID übergeben wird, MUSS die Schnittstelle I_LogData den Wert dieses
Parameters in das Dokument "LDA_Einwilligungserklaerung.html" an der
vorgesehenen Stelle aufnehmen. **[\<=]**

**A_17203 - Schnittstelle Logdatenerfassung Bereitstellung Widerrufserklärung**

Die Schnittstelle I_LogData MUSS über die Operation I_LogData::getFile die
Datei "LDA_Widerrufserklaerung.html" für alle Clients bereitstellen. Der
lesende Zugriff auf diese Datei MUSS auch ohne Authentisierung auf HTTP-Ebene
(ohne Authorization-Parameter) möglich sein. **[\<=]**

**A_17806 - Schnittstelle Logdatenerfassung Aufnahme LEI-ID in
Widerrufserklärung**

Wenn mit Operation I_LogData::getFile nach der URL im HTTP GET der Parameter
LEI-ID übergeben wird, MUSS die Schnittstelle I_LogData den Wert dieses
Parameters in das Dokument "LDA_Widerrufserklaerung.html" an der vorgesehenen
Stelle aufnehmen. **[\<=]**

**A_17340 - Schnittstelle Logdatenerfassung Willenserklärungen**

Die Schnittstelle I_LogData MUSS die Operation I_LogData::decIntent für die
Übertragung der statischen Metadaten aus der Einwilligungserklärung und die
Widerrufserklärung von Konnektoren zur Schnittstelle Logdatenerfassung
entsprechend Tabelle Tab_I_LogData_003 bereitstellen.

Tabelle2: Tab_I_LogData_003 Operation I_LogData::decIntent

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
Name

</td><td>
I_LogData::decIntent

</td></tr><tr><td>
Beschreibung

</td><td>
Mit dieser Operation überträgt der Konnektor die statischen Metadaten aus der
Einwilligungserklärung und die Widerrufserklärung zur Schnittstelle
Logdatenerfassung.

</td></tr><tr><td>
Initiierender Akteur

</td><td>
Konnektor (Client von I_LogData)

</td></tr><tr><td>
Weitere Akteure

</td><td>
keine

</td></tr><tr><td>
Auslöser

</td><td>
Konnektor (Client von I_LogData)

</td></tr><tr><td>
Vorbedingungen

</td><td>
aufgebaute TLS-Verbindung vom Client

</td></tr><tr><td>
Nachbedingungen

</td><td>
Die Daten wurden zur Schnittstelle Logdatenerfassung übertragen.

</td></tr><tr><td>
Aufruf

</td><td>
Aufruf von POST Request entsprechend [RFC7231] mit folgenden Optionen

 ---> UL

</td></tr><tr><td>
Standardablauf

</td><td>
Die Daten werden vom Konnektor zur Schnittstelle Logdatenerfassung übertragen.
Die Autorisierung erfolgt über den statischen Nutzernamen "Registration",
welcher immer freigeschaltet ist (der Nutzer mit dem LEI-ID Nutzernamen wird
erst nach Prüfung der Einwilligungserklärung eingerichtet).

Bei erfolgreicher Ablage der Datei wird im POST Response der HTTP-200-OK-Status
zurückgegeben.

</td></tr><tr><td>
Fehlerfälle

</td><td>
Neben den registrierten HTTP-Status-Codes des aufgerufenen HTTP POST können
keine weiteren Fehlercodes auftreten.

Bei allen Fehler-HTTP-Status-Codes werden keine Datei abgelegt und der POST
Request MUSS wiederholbar sein.

</td></tr></table>

**[\<=]**

### 3.4 Datei Upload

**A_17112 - Schnittstelle Logdatenerfassung Datei-Upload**

Die Schnittstelle I_LogData MUSS die Operation I_LogData::fileUpload für die
Übertragung von Dateien von Clients zur Schnittstelle Logdatenerfassung
entsprechend Tabelle Tab_I_LogData_002 bereitstellen.

Tabelle3: Tab_I_LogData_002 Operation I_LogData::fileUpload

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
Name

</td><td>
I_LogData::fileUpload

</td></tr><tr><td>
Beschreibung

</td><td>
Mit dieser Operation überträgt der Client eine Datei zur Schnittstelle
Logdatenerfassung.

</td></tr><tr><td>
Initiierender Akteur

</td><td>
Client von I_LogData

</td></tr><tr><td>
Weitere Akteure

</td><td>
keine

</td></tr><tr><td>
Auslöser

</td><td>
Client von I_LogData

</td></tr><tr><td>
Vorbedingungen

</td><td>
aufgebaute TLS-Verbindung vom Client

</td></tr><tr><td>
Nachbedingungen

</td><td>
Die Datei wurde zur Schnittstelle Logdatenerfassung übertragen.

</td></tr><tr><td>
Aufruf

</td><td>
Aufruf von POST Request entsprechend [RFC7231] mit folgenden Optionen

 ---> UL

</td></tr><tr><td>
Standardablauf

</td><td>
Die Datei wird – nach Autorisierung über "Authorization"-Parameter – vom
Client zur Schnittstelle Logdatenerfassung übertragen.

Bei erfolgreicher Ablage der Datei wird im POST Response der HTTP-200-OK-Status
zurückgegeben.

</td></tr><tr><td>
Fehlerfälle

</td><td>
Neben den registrierten HTTP-Status-Codes des aufgerufenen HTTP POST können
keine weiteren Fehlercodes auftreten.

Bei allen Fehler-HTTP-Status-Codes wird keine Datei abgelegt und der POST
Request MUSS mit gleichem "filename" wiederholbar sein.

Im Fall von HTTP-Status-Code "401 Unauthorized" ist der Client nicht berechtigt,
Dateien an die Schnittstelle Logdatenerfassung zu senden (z.B. weil die
Einwilligungserklärung noch nicht vorliegt und der Client freigeschaltet
wurde).

</td></tr></table>

**[\<=]**

Hinweise:

 ---> UL

**A_17132 - Schnittstelle Logdatenerfassung Zugriff auf Dateien**

Die Schnittstelle I_LogData MUSS

 ---> UL

Alle anderen Zugriffe auf Dateien MÜSSEN verhindert werden. **[\<=]**

### 4 Schnittstelle I_OpsData_Update

Die Fachdienste und zentralen Dienste liefern ihre Betriebsdaten (darunter
fallen auch die Rohdaten) über die Schnittstelle Betriebsdatenerfassung
I_OpsData_Update. 

### 4.1 Transport Layer Security (TLS)

**A_17272-01 - Schnittstelle Betriebsdatenerfassung TLS-Authentisierung für
Fach- und zentrale Dienste durch den I_OpsData_Update-Server**

Die Schnittstelle I_OpsData_Update MUSS bei der Absicherung der Verbindung durch
TLS die serverseitige Authentisierung unter Nutzung des
X.509-Komponentenzertifikats mit der TLS-Server-Identität ID.ZD.TLS_S zur
Serverauthentisierung umsetzen. **[\<=]**

**A_17416-01 - Schnittstelle Betriebsdatenerfassung Prüfung des
TLS-Server-Zertifikats durch Fach- und zentrale Dienste**

Der Client der Schnittstelle I_OpsData_Update MUSS bei der Absicherung der
Verbindung durch TLS die serverseitige Authentisierung durch Prüfung des
I_OpsData_Update-X.509-Komponentenzertifikats mit der TLS-Server-Identität
ID.ZD.TLS_S zur Serverauthentisierung entsprechend
[gemSpec_Krypt#TLS-Verbindungen] umsetzen. **[\<=]**

**A_17730 - Schnittstelle Betriebsdatenerfassung Keine Verbindungen ohne TLS**

Die Schnittstelle I_OpsData_Update MUSS ausschließlich Verbindungen mit TLS
akzeptieren. **[\<=]**

### 4.2 DNS Resource Record

Die Schnittstelle I_OpsData_Update stellt Funktionen bereit, die über URLs
aufgerufen werden können.

**A_17731 - Schnittstelle Betriebsdatenerfassung Bereitstellung
DNS-Resource-Records**

Der Anbieter der Schnittstelle Betriebsdatenerfassung I_OpsData_Update MUSS SRV-
und TXT-Resource-Records im DNS bereitstellen. Die Werte der PFADx-Angaben
MÜSSEN mit einem "/" beginnen.Im DNS sind dazu folgende Einträge
einzutragen:Owner                                  TTL
Class Type Data_fdrdif._tcp.\<TOP_LEVEL_DOMAIN_TI\> \<TTL1\> \<IN\> \<SRV\>
\<Priorität1\>  \<Gewicht1\>  \<Port1\>  \<FQDN1\>_fdrdif._tcp.\<TOP_LEVEL_DOMAIN_TI\>
\<TTL2\> \<IN\> \<TXT\> "txtvers=\<VERSION1\>"
"path=\<PFAD1\>"_fdrdif._tcp.\<TOP_LEVEL_DOMAIN_TI\> \<TTL3\> \<IN\> \<SRV\>
\<Priorität2\>  \<Gewicht2\>  \<Port2\>  \<FQDN2\>_fdrdif._tcp.\<TOP_LEVEL_DOMAIN_TI\>
\<TTL4\> \<IN\> \<TXT\> "txtvers=\<VERSION2\>"
"path=\<PFAD2\>"_zdrdif._tcp.\<TOP_LEVEL_DOMAIN_TI\> \<TTL1\> \<IN\> \<SRV\>
\<Priorität1\>  \<Gewicht1\>  \<Port1\>  \<FQDN1\>_zdrdif._tcp.\<TOP_LEVEL_DOMAIN_TI\>
\<TTL2\> \<IN\> \<TXT\> "txtvers=\<VERSION1\>"
"path=\<PFAD1\>"_zdrdif._tcp.\<TOP_LEVEL_DOMAIN_TI\> \<TTL3\> \<IN\> \<SRV\>
\<Priorität2\>  \<Gewicht2\>  \<Port2\>  \<FQDN2\>_zdrdif._tcp.\<TOP_LEVEL_DOMAIN_TI\>
\<TTL4\> \<IN\> \<TXT\> "txtvers=\<VERSION2\>"
"path=\<PFAD2\>"TOP_LEVEL_DOMAIN_TI: in der PU = telematik.; in der RU/TU =
telematik-test. **[\<=]**

Die "fdrdif"-DNS-Resource-Records werden von den Fachdiensten und die
"zdrdif"-DNS-Resource-Records von den zentralen Diensten zur Lokalisierung der
Schnittstelle genutzt.

### 4.3 Datei Upload

**A_17733-01 - Schnittstelle Betriebsdatenerfassung Datei-Upload**

Die Schnittstelle I_OpsData_Update MUSS die Operation
I_OpsData_Update::fileUpload für die Übertragung von Dateien von Clients zur
Schnittstelle Betriebsdatenerfassung entsprechend Tabelle
Tab_I_OpsData_Update_002 bereitstellen.

Tabelle4: Tab_I_OpsData_Update_002 Operation I_OpsData_Update::fileUpload

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
Name

</td><td>
I_OpsData_Update::fileUpload

</td></tr><tr><td>
Beschreibung

</td><td>
Mit dieser Operation überträgt der Client pro Lieferung genau eine Datei an
die Schnittstelle Betriebsdatenerfassung.

</td></tr><tr><td>
Initiierender Akteur

</td><td>
Client von I_OpsData_Update

</td></tr><tr><td>
Weitere Akteure

</td><td>
keine

</td></tr><tr><td>
Auslöser

</td><td>
Client von I_OpsData_Update

</td></tr><tr><td>
Vorbedingungen

</td><td>
aufgebaute TLS-Verbindung vom Client

</td></tr><tr><td>
Nachbedingungen

</td><td>
Die Datei wurde zur Schnittstelle Betriebsdatenerfassung übertragen.

</td></tr><tr><td>
Aufruf

</td><td>
Aufruf von POST Request entsprechend [RFC7231] mit folgenden Optionen

 ---> UL

</td></tr><tr><td>
Standardablauf

</td><td>
Die Datei wird vom Client zur Schnittstelle Betriebsdatenerfassung übertragen.

Die Datei wird auf Fehler überprüft. 

Bei erfolgreicher Ablage und Prüfung der Datei wird im POST Response der
HTTP-200-OK-Status zurückgegeben. Der Client muss für die Prüfung der
übermittelten Datei genügend Zeit berücksichtigen (Timer für das Warten auf
das HTTP Response entsprechend konfigurieren).

Wenn die Prüfung der Datei länger als 10 Sekunden dauert, MUSS die
Schnittstelle I_OpsData_Update nach jeweils 10 Sekunden einen POST Response
mit dem HTTP-102 Processing Status zurückgeben um bei dem Client ein Timeout
zu verhindern.  

</td></tr><tr><td>
Fehlerfälle

</td><td>
Neben den registrierten HTTP-Status-Codes des aufgerufenen HTTP POST können
keine weiteren Fehlercodes auftreten.

Bei allen Fehler-HTTP-Status-Codes wird keine Datei abgelegt und der POST
Request MUSS mit gleichem "filename" wiederholbar sein.

Im Fall von HTTP-Status-Code "400 Bad Request" enthält der HTTP POST bzw. die
Datei einen Fehler. Dieser Fehler kann sich in der enthaltenen Datei befinden.

</td></tr></table>

**[\<=]**

Hinweise:

 ---> UL

**A_17734-01 - Schnittstelle Betriebsdatenerfassung Zugriff auf Dateien**

Die Schnittstelle I_OpsData_Update MUSS

 ---> UL

**[\<=]**

### 5 Anhang – Verzeichnisse

### 5.1 Abkürzungen

<table><tr><th>
Kürzel

</th><th>
Erläuterung

</th></tr><tr><td>
DNS

</td><td>
Domain Name Service

</td></tr><tr><td>
TLS

</td><td>
Transport Layer Security

</td></tr><tr><td>
LEI

</td><td>
Leistungserbringerinstitution

</td></tr><tr><td>
LDA

</td><td>
Logdaten-Analyse

</td></tr></table>

### 5.2 Glossar

<table><tr><th>
Begriff

</th><th>
Erläuterung

</th></tr><tr><td>
Funktionsmerkmal

</td><td>
Der Begriff beschreibt eine Funktion oder auch einzelne, eine logische Einheit
bildende Teilfunktionen der TI im Rahmen der funktionalen Zerlegung des Systems.

</td></tr></table>

Das Glossar wird als eigenständiges Dokument (vgl. [gemGlossar]) zur Verfügung
gestellt.

### 5.3 Abbildungsverzeichnis

- [Abbildung-1] - Überblick Schnittstelle Logdatenerfassung

### 5.4 Tabellenverzeichnis

- [Tabelle-1] - Tab_I_LogData_001 Operation I_LogData::getFile
- [Tabelle-2] - Tab_I_LogData_003 Operation I_LogData::decIntent
- [Tabelle-3] - Tab_I_LogData_002 Operation I_LogData::fileUpload
- [Tabelle-4] - Tab_I_OpsData_Update_002 Operation I_OpsData_Update::fileUpload

### 5.5 Referenzierte Dokumente

### 5.5.1 Dokumente der gematik

Die nachfolgende Tabelle enthält die Bezeichnung der in dem vorliegenden
Dokument referenzierten Dokumente der gematik zur Telematikinfrastruktur. Der
mit der vorliegenden Version korrelierende Entwicklungsstand dieser Konzepte
und Spezifikationen wird pro Release in einer Dokumentenlandkarte definiert.
Version und Stand der referenzierten Dokumente sind daher in der nachfolgenden
Tabelle nicht aufgeführt. Deren zu diesem Dokument jeweils gültige
Versionsnummer ist in der aktuellen, von der gematik veröffentlichten
Dokumentenlandkarte enthalten, in der die vorliegende Version aufgeführt wird.

<table><tr><th>
[Quelle]

</th><th>
Herausgeber: Titel

</th></tr><tr><td>
[gemGlossar]

</td><td>
gematik: Glossar der Telematikinfrastruktur

</td></tr></table>

### 5.5.2 Weitere Dokumente

<table><tr><th>
[Quelle]

</th><th>
Herausgeber (Erscheinungsdatum): Titel

</th></tr><tr><td>
[RFC7230]

</td><td>
Hypertext Transfer Protocol (HTTP/1.1): Message Syntax and Routing

</td></tr><tr><td>
[RFC7231]

</td><td>
Hypertext Transfer Protocol (HTTP/1.1): Semantics and Content

</td></tr><tr><td>
[RFC7617]

</td><td>
The 'Basic' HTTP Authentication Scheme

</td></tr></table>





[Dokumentinformationen]: #dokumentinformationen
[Inhaltsverzeichnis]:    #inhaltsverzeichnis
[1]:                     #1-einordnung-des-dokuments
[1.1]:                   #11-zielsetzung
[1.2]:                   #12-zielgruppe
[1.3]:                   #13-geltungsbereich
[1.4]:                   #14-abgrenzungen
[1.5]:                   #15-methodik
[2]:                     #2-systemüberblick
[3]:                     #3-schnittstelle-i_logdata
[3.1]:                   #31-transport-layer-security-tls
[3.2]:                   #32-dns-resource-record
[3.3]:                   #33-willenserklärungen-zur-konnektor-logdatenerfassung
[3.4]:                   #34-datei-upload
[4]:                     #4-schnittstelle-i_opsdata_update
[4.1]:                   #41-transport-layer-security-tls
[4.2]:                   #42-dns-resource-record
[4.3]:                   #43-datei-upload
[5]:                     #5-anhang-–-verzeichnisse
[5.1]:                   #51-abkürzungen
[5.2]:                   #52-glossar
[5.3]:                   #53-abbildungsverzeichnis
[5.4]:                   #54-tabellenverzeichnis
[5.5]:                   #55-referenzierte-dokumente
[5.5.1]:                 #551-dokumente-der-gematik
[5.5.2]:                 #552-weitere-dokumente
[Abbildung-1]:           gemSpec_SST_LD_BD_V1.2.0.attachments/10123868451374256736.png
[Tbl-001]:               #Tbl-001 (&93834833823304)
[Tabelle-1]:             #Tabelle-1 (&93834793790440)
[Tabelle-2]:             #Tabelle-2 (&93834808887552)
[Tabelle-3]:             #Tabelle-3 (&93834789484504)
[Tabelle-4]:             #Tabelle-4 (&93834838625752)
[Tbl-006]:               #Tbl-006 (&93834772233872)
[Tbl-007]:               #Tbl-007 (&93834772250608)
[Tbl-008]:               #Tbl-008 (&93834836117480)
[Tbl-009]:               #Tbl-009 (&93834836125840)
