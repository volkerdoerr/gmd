
Elektronische Gesundheitskarte und Telematikinfrastruktur

### 

- Klassifizierung: öffentlich
- Referenzierung: gemSpec_SST_LD_BD
- Revision: 566841
- Stand: 03.02.2023
- Status: freigegeben
- Version: 1.4.0

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

</td></tr><tr><td>
1.3.0

</td><td>
02.12.22

</td><td>
Kap. 3

</td><td>
Einarbeitung CI_Maintenance_22.5:  Entfernen Schnittstelle
I_Log_Data, Konkretisierung Betriebsdatenübermittlung Konnektor

</td><td>
gematik

</td></tr><tr><td>
1.4.0

</td><td>
03.02.23

</td><td>
Einarbeitung Betr_Maintenance_22.3

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
- [3] Schnittstelle I_OpsData_Update
  - [3.1] Transport Layer Security (TLS)
  - [3.2] DNS Resource Record
  - [3.3] Datei Upload
  - [3.4] Content Upload XML
  - [3.5] Content Upload JSON Format
- [4] Anhang – Verzeichnisse
  - [4.1] Abkürzungen
  - [4.2] Glossar
  - [4.3] Abbildungsverzeichnis
  - [4.4] Tabellenverzeichnis
  - [4.5] Referenzierte Dokumente
    - [4.5.1] Dokumente der gematik
    - [4.5.2] Weitere Dokumente

### 1 Einordnung des Dokuments

### 1.1 Zielsetzung

Dieses Dokument enthält die Anforderungen an die Schnittstelle
Betriebsdatenerfassung. Über sie werden von den Clients (z.B. Fachdienste und
zentrale Dienste) versendete Betriebsdaten empfangen.

### 1.2 Zielgruppe

Das Dokument richtet sich an Hersteller und Anbieter der Schnittstelle
Betriebsdatenerfassung.

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
Schnittstelle Betriebsdatenerfassung [I_OpsData_Update].

### 1.5 Methodik

Anforderungen als Ausdruck normativer Festlegungen werden durch eine eindeutige
ID sowie die dem RFC2119[RFC2119] entsprechenden, in Großbuchstaben
geschriebenen deutschen Schlüsselworte MUSS, DARF NICHT, SOLL, SOLL NICHT,
KANN gekennzeichnet.Sie werden im Dokument wie folgt dargestellt:\<AFO-ID\> -
\<Titel der Afo\>Text / Beschreibung [\<=]Dabei umfasst die Anforderung
sämtliche zwischen Afo-ID und der Textmarke [\<=] angeführten Inhalte.

### 2 Systemüberblick

Die Fachdienste und zentralen Dienste können ihre Betriebsdaten über die
Schnittstelle Betriebsdatenerfassung I_OpsData_Update mit Operation
[I_OpsData_Update]::fileUpload liefern. 

### 3 Schnittstelle I_OpsData_Update

Die Fachdienste und zentralen Dienste liefern ihre Betriebsdaten (darunter
fallen auch die Rohdaten) über die Schnittstelle Betriebsdatenerfassung
I_OpsData_Update. 

### 3.1 Transport Layer Security (TLS)

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

### 3.2 DNS Resource Record

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

### 3.3 Datei Upload

**A_17733-01 - Schnittstelle Betriebsdatenerfassung Datei-Upload**

Die Schnittstelle I_OpsData_Update MUSS die Operation
I_OpsData_Update::fileUpload für die Übertragung von Dateien von Clients zur
Schnittstelle Betriebsdatenerfassung entsprechend Tabelle
Tab_I_OpsData_Update_002 bereitstellen.

Tabelle1: Tab_I_OpsData_Update_002 Operation I_OpsData_Update::fileUpload

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

### 3.4 Content Upload XML

**A_23107 - Schnittstelle Betriebsdatenerfassung Content-Upload XML Format**

Die Schnittstelle I_OpsData_Update MUSS die Operation
I_OpsData_Update::contentUploadXML für die Übertragung von Content im XML
Format von Clients zur Schnittstelle Betriebsdatenerfassung entsprechend
Tabelle Tab_I_OpsData_Update_003 bereitstellen. Tabelle :
Tab_I_OpsData_Update_003 Operation I_OpsData_Update::contentUploadXML(Hinweis:
Für weitere Informationen zum CI, siehe [gemRL_Betr_TI] Kapitel
"Configuration Management".) **[\<=]**

### 3.5 Content Upload JSON Format

**A_23110 - Schnittstelle Betriebsdatenerfassung Content-Upload JSON Format**

Die Schnittstelle I_OpsData_Update MUSS die Operation
I_OpsData_Update::contentUploadJSON für die Übertragung von Content im JSON
Format von Clients zur Schnittstelle Betriebsdatenerfassung entsprechend
Tabelle Tab_I_OpsData_Update_004 bereitstellen. Tabelle :
Tab_I_OpsData_Update_004 Operation I_OpsData_Update::contentUploadJSON(Hinweis:
Für weitere Informationen zum CI, siehe [gemRL_Betr_TI] Kapitel
"Configuration Management".) **[\<=]**

### 4 Anhang – Verzeichnisse

### 4.1 Abkürzungen

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

</td></tr></table>

### 4.2 Glossar

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

### 4.3 Abbildungsverzeichnis



### 4.4 Tabellenverzeichnis

- [Tabelle-1] - Tab_I_OpsData_Update_002 Operation I_OpsData_Update::fileUpload

### 4.5 Referenzierte Dokumente

### 4.5.1 Dokumente der gematik

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

### 4.5.2 Weitere Dokumente

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
[3]:                     #3-schnittstelle-i_opsdata_update
[3.1]:                   #31-transport-layer-security-tls
[3.2]:                   #32-dns-resource-record
[3.3]:                   #33-datei-upload
[3.4]:                   #34-content-upload-xml
[3.5]:                   #35-content-upload-json-format
[4]:                     #4-anhang-–-verzeichnisse
[4.1]:                   #41-abkürzungen
[4.2]:                   #42-glossar
[4.3]:                   #43-abbildungsverzeichnis
[4.4]:                   #44-tabellenverzeichnis
[4.5]:                   #45-referenzierte-dokumente
[4.5.1]:                 #451-dokumente-der-gematik
[4.5.2]:                 #452-weitere-dokumente
[Tbl-001]:               #Tbl-001 (&93834772276904)
[Tabelle-1]:             #Tabelle-1 (&93834770984520)
[Tbl-003]:               #Tbl-003 (&93834768028328)
[Tbl-004]:               #Tbl-004 (&93834768039160)
[Tbl-005]:               #Tbl-005 (&93834768055512)
[Tbl-006]:               #Tbl-006 (&93834778255064)
