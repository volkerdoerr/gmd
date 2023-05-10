
Elektronische Gesundheitskarte und Telematikinfrastruktur

### Spezifikation<br>Verzeichnisdienst

- Klassifizierung: öffentlich_Entwurf
- Referenzierung: gemSpec_VZD
- Revision: 548770
- Stand: 08.11.2021
- Status: in Bearbeitung
- Version: 1.14.0 CC 2

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
Stand

</th><th>
Kap./ Seite

</th><th>
Grund der Änderung, besondere Hinweise

</th><th>
Bearbeitung

</th></tr><tr><td>
1.2.0

</td><td>
17.07.15

</td><td>
Nutzer der Schnittstelle I_Directory_Maintenance geändert

</td><td>
gematik

</td></tr><tr><td>
1.3.0

</td><td>
24.08.16

</td><td>
Anpassungen zum Online-Produktivbetrieb (Stufe 1)

</td><td>
gematik

</td></tr><tr><td>
1.4.0

</td><td>
28.10.16

</td><td>
</td><td>
Einarbeitung lt. Änderungsliste

</td><td>
gematik

</td></tr><tr><td>
1.5.0

</td><td>
19.04.17

</td><td>
</td><td>
Anpassung nach Änderungsliste

</td><td>
gematik

</td></tr><tr><td>
1.6.0

</td><td>
14.05.18

</td><td>
</td><td>
Anpassung nach Änderungslisten P15.2, 15.4 und 15.5

</td><td>
gematik

</td></tr><tr><td>
1.7.0

</td><td>
15.05.19

</td><td>
</td><td>
Einarbeitung der Änderungen gemäß P18.1

</td><td>
gematik

</td></tr><tr><td>
1.8.0

</td><td>
28.06.19

</td><td>
Einarbeitung der Änderungen gemäß P19.1

</td><td>
gematik

</td></tr><tr><td>
1.9.0

</td><td>
02.10.19

</td><td>
Einarbeitung der Änderungen gemäß P20.1 und P16.1/2

</td><td>
gematik

</td></tr><tr><td>
1.10.0

</td><td>
30.06.20

</td><td>
Anpassungen gemäß Änderungsliste P22.1 und Scope-Themen aus Systemdesign
R4.0.0

</td><td>
gematik

</td></tr><tr><td>
1.11.0

</td><td>
12.11.20

</td><td>
Anpassungen gemäß Änderungsliste P22.2 und Scope-Themen aus Systemdesign
R4.0.1

</td><td>
gematik

</td></tr><tr><td>
1.11.1

</td><td>
18.12.20

</td><td>
Einarbeitung der Änderungen gemäß P22.4

</td><td>
gematik

</td></tr><tr><td>
1.12.0

</td><td>
19.02.21

</td><td>
Anpassungen gemäß Änderungsliste P22.5;  
Korrekturen in der Beschreibung des
Datenmodells sowie neue Operation zur Abfrage aller Daten über die
REST-Schnittstelle.

</td><td>
gematik

</td></tr><tr><td>
1.13.0

</td><td>
06.04.21

</td><td>
Anpassungen gemäß Änderungsliste KIM_Maintenance_21.1/  
KIM 1.5.1

</td><td>
gematik

</td></tr><tr><td>
1.13.1

</td><td>
20.04.21

</td><td>
Anpassung C_10533 aus KIM_Maintenance_21.1 vervollständigt (TIP1-A_5586
entfernt)

</td><td>
gematik

</td></tr><tr><td>
1.13.2

</td><td>
11.10.21

</td><td>
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
1.14.0 CC

</td><td>
07.07.21

</td><td>
Anpassung gemäß C_10737, unter anderem:

 ---> UL

In Tab_VZD_Mapping_Eintragstyp_und_ProfessionOID wurden neue professionOIDs
aufgenommen und den entryTypes zugeordnet,

Es wurde eine Anforderung aufgenommen, dass das in
Tab_VZD_Mapping_Eintragstyp_und_ProfessionOID beschriebene Mapping
konfigurierbar sein muss.

</td><td>
gematik

</td></tr><tr></tr></table>

### Inhaltsverzeichnis

- [Dokumentinformationen]
- [Inhaltsverzeichnis]
- [1] Einordnung des Dokumentes
  - [1.1] Zielsetzung
  - [1.2] Zielgruppe
  - [1.3] Geltungsbereich
  - [1.4] Abgrenzungen
  - [1.5] Methodik
- [2] Systemüberblick
- [3] Übergreifende Festlegungen
  - [3.1] IT-Sicherheit und Datenschutz
  - [3.2] Fachliche Anforderungen
- [4] Funktionsmerkmale
  - [4.1] Schnittstelle I_Directory_Query
    - [4.1.1] Operation search_Directory
      - [4.1.1.1] Umsetzung
      - [4.1.1.2] Nutzung
  - [4.2] Schnittstelle I_Directory_Maintenance
    - [4.2.1] Operation add_Directory_Entry
      - [4.2.1.1] Umsetzung
      - [4.2.1.2] Nutzung
    - [4.2.2] Operation read_Directory_Entry
      - [4.2.2.1] Umsetzung
      - [4.2.2.2] Nutzung
    - [4.2.3] Operation modify_Directory_Entry
      - [4.2.3.1] Umsetzung
      - [4.2.3.2] Nutzung
    - [4.2.4] Operation delete_Directory_Entry
      - [4.2.4.1] Umsetzung
      - [4.2.4.2] Nutzung
  - [4.3] Schnittstelle I_Directory_Application_Maintenance
    - [4.3.1] Operation getInfo
      - [4.3.1.1] Umsetzung REST
      - [4.3.1.2] Nutzung REST
    - [4.3.2] Operation add_Directory_FA-Attributes
      - [4.3.2.1] Umsetzung SOAP
      - [4.3.2.2] Nutzung SOAP
      - [4.3.2.3] Umsetzung LDAPv3
      - [4.3.2.4] Nutzung LDAPv3
      - [4.3.2.5] Umsetzung REST
      - [4.3.2.6] Nutzung REST
    - [4.3.3] Operation delete_Directory_FA-Attributes
      - [4.3.3.1] Umsetzung SOAP
      - [4.3.3.2] Nutzung SOAP
      - [4.3.3.3] Umsetzung LDAPv3
      - [4.3.3.4] Nutzung LDAPv3
      - [4.3.3.5] Umsetzung REST
      - [4.3.3.6] Nutzung REST
    - [4.3.4] Operation modify_Directory_FA-Attributes
      - [4.3.4.1] Umsetzung SOAP
      - [4.3.4.2] Nutzung SOAP
      - [4.3.4.3] Umsetzung LDAPv3
      - [4.3.4.4] Nutzung LDAPv3
      - [4.3.4.5] Umsetzung REST
      - [4.3.4.6] Nutzung REST
    - [4.3.5] Operation get_Directory_FA-Attributes
      - [4.3.5.1] Umsetzung REST
      - [4.3.5.2] Nutzung REST
  - [4.4] Prozessschnittstelle P_Directory_Application_Registration (Provided)
  - [4.5] Prozessschnittstelle P_Directory_Maintenance (Provided)
  - [4.6] Schnittstelle I_Directory_Administration
    - [4.6.1] Operationen der Schnittstelle I_ Directory_Administration
      - [4.6.1.1] I_Directory_Administration - Lesen der Metadaten
        - [4.6.1.1.1] GET
      - [4.6.1.2] DirectoryEntry Administration
        - [4.6.1.2.1] POST
        - [4.6.1.2.2] GET
        - [4.6.1.2.3] PUT
        - [4.6.1.2.4] DELETE
      - [4.6.1.3] Certificate Administration
        - [4.6.1.3.1] POST
        - [4.6.1.3.2] GET
        - [4.6.1.3.3] DELETE
      - [4.6.1.4] DirectoryEntry Synchronization
        - [4.6.1.4.1] GET
    - [4.6.2] Nutzung der Schnittstelle I_Directory_Administration
- [5] Datenmodell
- [6] Anhang A – Verzeichnisse
  - [6.1] Abkürzungen
  - [6.2] Glossar
  - [6.3] Abbildungsverzeichnis
  - [6.4] Tabellenverzeichnis
  - [6.5] Referenzierte Dokumente
    - [6.5.1] Dokumente der gematik
    - [6.5.2] Weitere Dokumente

### 1 Einordnung des Dokumentes

### 1.1 Zielsetzung

Die Spezifikation des Verzeichnisdienstes (VZD) enthält die Definition der
Funktionalität, der Prozesse und der Schnittstellen sowie das
Informationsmodell des VZD.

Der VZD ist ein zentraler Dienst der TI-Plattform.

Das Informationsmodell des VZD ist erweiterbar.

Die vorliegende Spezifikation definiert die Anforderungen zu Herstellung, Test,
Betrieb, Datenschutz und Informationssicherheit des Produkttyps VZD.

### 1.2 Zielgruppe

Das Dokument ist maßgeblich für Anbieter und Hersteller von Verzeichnisdiensten

### 1.3 Geltungsbereich

Dieses Dokument enthält normative Festlegungen zur Telematikinfrastruktur des
Deutschen Gesundheitswesens. Der Gültigkeitszeitraum der vorliegenden Version
und deren Anwendung in Zulassungs- oder Abnahmeverfahren wird durch die gematik
mbH in gesonderten Dokumenten (z.B. Dokumentenlandkarte, Produkttypsteckbrief,
Leistungsbeschreibung) festgelegt und bekannt gegeben.

Schutzrechts-/Patentrechtshinweis

Die nachfolgende Spezifikation ist von der gematik allein unter technischen
Gesichtspunkten erstellt worden. Im Einzelfall kann nicht ausgeschlossen
werden, dass die Implementierung der Spezifikation in technische Schutzrechte
Dritter eingreift. Es ist allein Sache des Anbieters oder Herstellers, durch
geeignete Maßnahmen dafür Sorge zu tragen, dass von ihm aufgrund der
Spezifikation angebotene Produkte und/oder Leistungen nicht gegen Schutzrechte
Dritter verstoßen und sich ggf. die erforderlichen Erlaubnisse/Lizenzen von
den betroffenen Schutzrechtsinhabern einzuholen. Die gematik mbH übernimmt
insofern keinerlei Gewährleistungen.

### 1.4 Abgrenzungen

Spezifiziert werden in dem Dokument die von dem Produkttyp bereitgestellten
(angebotenen) Schnittstellen. Benutzte Schnittstellen werden hingegen in der
Spezifikation desjenigen Produkttypen beschrieben, der diese Schnittstelle
bereitstellt. Auf die entsprechenden Dokumente wird verwiesen (siehe auch).

Die vollständige Anforderungslage für den Produkttyp ergibt sich aus weiteren
Konzept- und Spezifikationsdokumenten, diese sind in dem Produkttypsteckbrief
des Produkttyps VZD dokumentiert.

Nicht Bestandteil des vorliegenden Dokumentes sind die Festlegungen zum
Themenbereich

 ---> UL

### 1.5 Methodik

Anforderungen als Ausdruck normativer Festlegungen werden durch eine eindeutige
ID in eckigen Klammern sowie die dem RFC 2119 [RFC2119] entsprechenden, in
Großbuchstaben geschriebenen deutschen Schlüsselworte MUSS, DARF NICHT, SOLL,
SOLL NICHT, KANN gekennzeichnet.

Sie werden im Dokument wie folgt dargestellt:

\<AFO-ID\> - \<Titel der Afo\>Text / Beschreibung[ \<=]

Dabei umfasst die Anforderung sämtliche innerhalb der Afo-ID und der Textmarke
angeführten Inhalte.

Für die Erzeugung der Abbildungen und Informationsmodelle wird das Tool
„Enterprise Architect“ verwendet.

### 2 Systemüberblick

Der VZD ist ein Produkttyp der TI gemäß [gemKPT_Arch_TIP].

![Abbildung-1][Abbildung-1]

Der VZD befindet sich in der zentralen Zone der TI-Plattform.

Die Dateneinträge werden erstellt und gepflegt:

 ---> OL

Der VZD kann durch LDAP-Clients abgefragt werden.

### 3 Übergreifende Festlegungen

### 3.1 IT-Sicherheit und Datenschutz

**TIP1-A_5546-01 - VZD, Integritäts- u. Authentizitätsschutz**

Der Anbieter des VZD MUSS die Integrität und Authentizität der im VZD
gespeicherten Daten gemäß den Richtlinien des Bundesamtes für Sicherheit in
der Informationstechnik für allgemeine Verzeichnisdienste, [BSI APP.2.1],
implementieren. **[\<=]**

**TIP1-A_5547-01 - VZD, Löschen ungültiger Zertifikate**

Der VZD MUSS täglich die gespeicherten Zertifikate nach Ablaufdatum
(TUC_PKI_002 „Gültigkeitsprüfung des Zertifikats“) und Status
(TUC_PKI_006 "OCSP-Abfrage) prüfen. Ungültige Zertifikate werden (inklusive
der gesamten Zertifikatsstruktur "Certificate" entsprechend
Abb_VZD_logisches_Datenmodell) sofort gelöscht. Ein Eintrag ohne gültige
Zertifikate wird nach einem Jahr gelöscht und darf nicht durch eine Anfrage
über die Operation search_Directory der Schnittstelle I_Directory_Query
gefunden werden. **[\<=]**

Zum Beispiel dürfen gültige RU-/TU-Zertifikate nicht in der PU akzeptiert
werden. Die Prüfung über TUC_PKI_018 berücksichtigt entsprechend
dem initialisiertenVertrauensanker (aus der jeweiligen Umgebung) die Umgebung.

**A_21808 - VZD, Hinzufügen von professionOID und entryType in die Basisdaten**

Der VZD MUSS beim Hinzufügen von Zertifikaten prüfen, ob der Wert der
enthaltenen professionOID bzw. entryType schon in den Basisdaten vorhanden ist.
Falls nicht, MUSS der VZD diese professionOID bzw. entryType zu den
existierenden Basisdaten hinzufügen. **[\<=]**

**A_21809 - VZD, Löschen von professionOID und entryType aus den Basisdaten**

Der VZD MUSS gewährleisten, dass nach dem Löschen von Zertifikaten für die
Attribute professionOID und entryType in den Basisdaten nur Werte aus den
verbleibenden Zertifikaten erhalten bleiben. **[\<=]**

**TIP1-A_5548 - VZD, Protokollierung der Änderungsoperationen**

Der VZD MUSS Änderungen der Verzeichnisdiensteinträge protokollieren und muss
sie 6 Monate zur Verfügung halten. **[\<=]**

6 Monate ist die maximale Nachweistiefe ohne in den Bereich der
Vorratsdatenspeicherung zu kommen.

**TIP1-A_5549 - VZD, Keine Leseprofilbildung**

Der VZD DARF Suchanfragen NICHT speichern oder protokollieren. **[\<=]**

**TIP1-A_5550 - VZD, Keine Kopien von gelöschten Daten**

Der VZD DARF von gelöschten Daten KEINE Kopien speichern. **[\<=]**

**TIP1-A_5551 - VZD, Sicher gegen Datenverlust**

Der Anbieter des VZD MUSS den Dienst gegen Datenverlust absichern. **[\<=]**

**TIP1-A_5552 - VZD, Begrenzung der Suchergebnisse**

Der VZD MUSS die Ergebnisliste einer Suchanfrage auf 100 Suchergebnisse
begrenzen. **[\<=]**

**TIP1-A_5553 - VZD, Private Schlüssel sicher speichern**

Der VZD MUSS seine privaten Schlüssel sicher speichern und ihr Auslesen
verhindern um Manipulationen zu verhindern. **[\<=]**

**TIP1-A_5554 - VZD, Registrierungsdaten sicher speichern**

Der VZD MUSS die Integrität und Authentizität der gespeicherten
Registrierungsdaten der FAD gewährleisten. **[\<=]**

**TIP1-A_5555 - VZD, SOAP-Fehlercodes**

Der VZD MUSS für seine SOAP-Schnittstelle die generischen Fehlercodes

 ---> UL

aus Tabelle Tab_Gen_Fehler  aus [gemSpec_OM] im SOAP-Fault verwenden. Erkannte
Fehler auf Transportprotokollebene müssen auf gematik SOAP Faults (Code 6 aus
Tabelle Tab_Gen_Fehler aus [gemSpec_OM]) abgebildet werden.​​ **[\<=]**

**TIP1-A_5556 - VZD, Fehler Logging**

Der VZD MUSS lokal und remote erkannte Fehler in seinem lokalen Speicher
protokollieren. **[\<=]**

**TIP1-A_5557 - VZD, Unterstützung IPv4 und IPv6**

Der VZD MUSS IPv4 und IPv6 für alle seine IP-Schnittstellen im Dual-Stack-Mode
unterstützen. **[\<=]**

**TIP1-A_5558 - VZD, Sicheres Speichern der TSL**

Der VZD MUSS  die Inhalte der TSL in einem lokalen Trust Store sicher
speichern und für X.509-Zertifikatsprüfungen lokal zugreifbar halten. **[\<=]**

### 3.2 Fachliche Anforderungen

**TIP1-A_5560 - VZD, Erweiterbarkeit für neue Fachdaten**

Der Anbieter des VZD MUSS die Erweiterbarkeit des VZD für die Aufnahme der
Fachdaten neuer Fachanwendungen gewährleisten. **[\<=]**

**TIP1-A_5561 - VZD, DNS-SD**

Der Anbieter des VZD MUSS alle erforderlichen Einträge zur Dienstlokalisierung
der Außenschnittstellen gemäß [RFC6763] beginnend mit folgenden PTR Resource
Record-Bezeichnern im Namensdienst der TI-Plattform anlegen:

 ---> UL

 ---> UL

 ---> UL **[\<=]**

**TIP1-A_5562 - VZD, Parallele Zugriffe**

Der Betreiber des VZD MUSS sicherstellen, dass Benutzer gleichzeitig auf den VZD
zugreifen können. Dies umfasst alle technischen Schnittstellen. In
[gemSpec_Perf] ist die Anzahl der parallelen Zugriffe definiert. **[\<=]**

**TIP1-A_5563-01 - VZD, Erhöhung der Anzahl der Einträge**

Der Anbieter des VZD MUSS sicherstellen, dass 1.000.000 Einträge gespeichert
werden können. **[\<=]**

**TIP1-A_5620 - VZD, Nicht-Speicherung von Leading und Trailing Spaces**

Der Anbieter des VZD MUSS Leading und Trailing Spaces abschneiden. **[\<=]**

**A_20331 - VZD, Verhinderung LDAP Injection Attack**

DerVZD MUSS an allen Schnittstellen - welche LDAP nutzen bzw. auf LDAP
abgebildet werden - LDAP Injection Attacks durch geeignete
Sicherheitsprüfungen verhindern. **[\<=]**

**A_20262 - VZD, Maximale Anzahl von KOM-LE Adressen in den Fachdaten**

Der VZD MUSS bei dem Hinzufügen von KOM-LE Adressen in den Fachdaten folgende
Regeln beachten:

 ---> UL

**[\<=]**

**A_20263 - VZD, Kein automatisches Löschen von KOM-LE Adressen in den
Fachdaten**

Der VZD DARF KOM-LE Adressen in den Fachdaten als Folge einer Änderung
(Verkleinerung) des Attributwerts von maxKOMLEadr NICHT automatisch löschen.
**[\<=]**

Der betroffene KOM-LE Teilnehmer muss in diesem Fall zusammen mit dem
KOM-LE-Anbieter die nicht mehr benötigten KOM-LE Adressen löschen.

### 4 Funktionsmerkmale

Der VZD beinhaltet alle serverseitigen Anteile des Basisdienstes
Verzeichnis_Identitäten gemäß [gemKPT_Arch_TIP]. Dazu zählen die
Speicherung der Einträge von Leistungserbringern und Institutionen mit allen
definierten Attributen sowie die Speicherung von Fachdaten durch FAD. Mit einer
LDAP-Suchanfrage können Clients und FAD Basis- und Fachdaten abfragen (z. B.
X.509-Zertifikate).

Einträge des VZD werden durch berechtigte Benutzer sowie durch berechtigte FAD
erstellt und gepflegt.

**TIP1-A_5564 - VZD, Festlegung der Schnittstellen**

Der VZD MUSS die Schnittstellen gemäß Tabelle Tab_PT_VZD_Schnittstellen
implementieren („bereitgestellte“ Schnittstellen) und nutzen
(„benötigte“ Schnittstellen).

Tabelle1: Tab_PT_VZD_Schnittstellen

<table><tr><th>
Schnittstelle

</th><th>
bereitgestellt / benötigt

</th><th>
Bemerkung

</th></tr><tr><td>
I_Directory_Query

</td><td>
bereitgestellt

</td><td>
</td></tr><tr><td>
I_Directory_Maintenance

</td><td>
bereitgestellt

</td><td>
</td></tr><tr><td>
I_Directory_Application_Maintenance

</td><td>
bereitgestellt

</td><td>
</td></tr><tr><td>
I_Directory_Administration

</td><td>
bereitgestellt

</td></tr><tr><td>
I_IP_Transport

</td><td>
benötigt

</td><td>
Definition in [gemSpec_Net]

</td></tr><tr><td>
I_DNS_Name_Resolution

</td><td>
benötigt

</td><td>
Definition in [gemSpec_Net]

</td></tr><tr><td>
I_NTP_Time_Information

</td><td>
benötigt

</td><td>
Definition in [gemSpec_Net]

</td></tr><tr><td>
I_OCSP_Status_Information

</td><td>
benötigt

</td><td>
Definition in [gemSpec_PKI]

</td></tr><tr><td>
I_TSL_Download

</td><td>
benötigt

</td><td>
Definition in [gemSpec_TSL]

</td></tr></table>

**[\<=]**

**A_22361 - VZD, Filtermöglichkeiten in Leseoperationen**

Der VZD MUSS für die Leseoperationen read_Directory_Entry
und read_Directory_Entry_for_Sync der
Schnittstellen I_Directory_Administration
und I_Directory_Application_Maintenance die folgenden Filtermöglichkeiten
unterstützen:

 ---> UL

Alle Filterparameter einer Leseoperationen werden mit einem UND (&)
verknüpft.  **[\<=]**

Beispiel für die Belegung der Filterparameter einer Operation
read_Directory_Entry für die Suche nach Einträgen ohne gefülltes Attribut
"specialization" UND Postleitzahl 10*:

postalCode                   10*

specialization                \00

### 4.1 Schnittstelle I_Directory_Query

Die Schnittstelle ermöglicht LDAPv3-Clients die Suche nach Daten im VZD gemäß
der im Informationsmodell (siehe Kapitel 5) definierten Attribute. 

**TIP1-A_5565 - VZD, Schnittstelle I_Directory_Query**

Der VZD MUSS für LDAP Clients die Schnittstelle I_Directory_Query gemäß
Tabelle Tab_VZD_Schnittstelle_I_Directory_Query anbieten.

Tabelle2: Tab_VZD_Schnittstelle_I_Directory_Query

<table><tr><th>
Name

</th><th colspan="2">
I_Directory_Query

</th></tr><tr><td>
Version

</td><td colspan="2">
wird im Produkttypsteckbrief des VZD definiert

</td></tr><tr><td rowspan="2">
Operationen

</td><td>
Name

</td><td>
Kurzbeschreibung

</td></tr><tr><td>
search_Directory

</td><td>
Abfragen von Daten des VZD gemäß LDAPv3 Protokoll.  
Der Base DN für die LDAP
Suche ist dc=data,dc=vzd.

</td></tr></table>

**[\<=]**

### 4.1.1 Operation search_Directory

**TIP1-A_5566 - LDAP Client, LDAPS**

Der LDAP Client MUSS die Verbindung zum VZD mittels LDAPS sichern.Der LDAP
Client muss das Zertifikat des VZD C.ZD.TLS-S gemäß TUC_PKI_018
"Zertifikatsprüfung in der TI" und die Rolle (zulässig ist oid_vzd_ti)
prüfen. LDAP Clients der Anbieter vonWANDA Basic und WANDA Smart sind davon
ausgenommen.Der LDAP Client authentisiert sich nicht. **[\<=]**

**TIP1-A_5567 - VZD, LDAPS bei search_Directory**

Der VZD MUSS sicherstellen, dass die Operation search_Directory nur über eine
bestehende LDAPS -Verbindungausgeführt werden kann.

Der VZD muss die TLS-Verbindung 15 Minuten nach dem letzten Meldungsverkehr
abbauen, falls sie noch besteht. **[\<=]**

**TIP1-A_5568 - VZD und LDAP Client, Implementierung der LDAPv3 search
Operation**

Der VZD und die LDAP-Clients MÜSSEN die search Operation gemäß den LDAPv3
Standards [RFC4510], [RFC4511], [RFC4512], [RFC4513], [RFC4514], [RFC4515],
[RFC4516], [RFC4517], [RFC4518], [RFC4519], [RFC4520], [RFC4522] und [RFC4523]
implementieren. **[\<=]**

**A_17794 - VZD, Testunterstützung**

Der VZD MUSS für die Schnittstelle I_Directory_Query einen technischen User
in RU/TU bereitstellen, über den eine unlimitierte Abfrage der Daten des
Verzeichnisdienstes (searchView) möglich ist. **[\<=]**

### 4.1.1.1 Umsetzung

**TIP1-A_5569 - VZD, search_Directory, Suche nach definierten Attributen**

Der VZD MUSS die enthaltenen Daten so strukturiert haben, dass mit einer
einzigen LDAPv3-Suche alle einer Telematik-ID zugeordneten Attribute
(Basisdaten und Fachdaten) in Form einer flachen Liste von Attributen ohne
ou-Unterstruktur abgefragt werden können.Die abgefragten Attribute MÜSSEN
durch marktübliche E-Mail Clients nutzbar sein. **[\<=]**

### 4.1.1.2 Nutzung

**TIP1-A_5570 - LDAP Client, TUC_VZD_0001 „search_Directory”**

Der Anbieter des VZD MUSS für die Nutzung durch LDAP Clients den technischen
Use Case TUC_VZD_0001 „search_Directory” gemäß Tabelle Tab_TUC_VZD_0001
unterstützen.

Tabelle3: Tab_TUC_VZD_0001

<table><tr><th>
Name

</th><th colspan="2">
TUC_VZD_0001 “search_Directory”

</th></tr><tr><td>
Beschreibung

</td><td colspan="2">
Diese Operation ermöglicht die Suche nach den im VZD gespeicherten Daten.

</td></tr><tr><td>
Vorbedingungen

</td><td colspan="2">
Der LDAPS-Verbindungsaufbau muss erfolgreich durchgeführt sein.

</td></tr><tr><td>
Eingangsdaten

</td><td colspan="2">
Search Request gemäß [RFC4511]#4.5.1 und Informationsmodell
(Abb_VZD_logisches_Datenmodell)

</td></tr><tr><td>
Komponenten

</td><td colspan="2">
LDAP Client, Verzeichnisdienst

</td></tr><tr><td>
Ausgangsdaten

</td><td colspan="2">
gemäß [RFC4511]#4.5.2

</td></tr><tr><td rowspan="3">
Standardablauf

</td><td>
Aktion

</td><td>
Beschreibung

</td></tr><tr><td>
Search Request senden

</td><td>
Der LDAP Client sendet eine Suchanfrage gemäß [RFC4511]#4.5.1 an die
Schnittstelle I_Directory_Query des VZD. Die RFCs [RFC4510], [RFC4511],
[RFC4513], [RFC4514], [RFC4515], [RFC4516], [RFC4519] und [RFC4522] müssen
unterstützt werden.  
Der Base DN für die LDAP Suche ist dc=data,dc=vzd.

</td></tr><tr><td>
Search Response empfangen

</td><td>
Der LDAP Client empfängt das Ergebnis der Suche gemäß [RFC4511]#4.5.2.

</td></tr><tr><td>
Varianten/Alternativen

</td><td>
keine

</td><td>
</td></tr><tr><td>
Zustand nach erfolgreichem Ablauf

</td><td colspan="2">
Die Ergebnisse der Suche liegen im LDAP Client vor.

</td></tr><tr><td>
Fehlerfälle

</td><td colspan="2">
Zur Behandlung auftretender Fehlerfälle werden Fehlermeldungen gemäß
[RFC4511]#Appendix A verwendet.

</td></tr></table>

**[\<=]**

### 4.2 Schnittstelle I_Directory_Maintenance

Die Schnittstelle ermöglicht die Administration der Basisdaten.

**TIP1-A_5571 - VZD, Schnittstelle I_Directory_Maintenance**

Der VZD MUSS die Schnittstelle I_Directory_Maintenance gemäß Tabelle
Tab_VZD_Schnittstelle_I_Directory_Maintenance anbieten.

Tabelle4: Tab_VZD_Schnittstelle_I_Directory_Maintenance

<table><tr><th>
Name

</th><th colspan="2">
I_Directory_Maintenance

</th></tr><tr><td>
Version

</td><td colspan="2">
wird im Produkttypsteckbrief des VZD definiert

</td></tr><tr><td rowspan="5">
Operationen

</td><td>
Name

</td><td>
Kurzbeschreibung

</td></tr><tr><td>
add_Directory_Entry

</td><td>
Erzeugung eines Basisdaten-Verzeichniseintrages oder Überschreiben eines
bestehenden Verzeichniseintrages.

</td></tr><tr><td>
read_Directory_Entry

</td><td>
Abfrage aller Basis- und Fachdaten eines Verzeichniseintrages.

</td></tr><tr><td>
modify_Directory_Entry

</td><td>
Änderung eines Basisdaten-Verzeichniseintrages.

</td></tr><tr><td>
delete_Directory_Entry

</td><td>
Löschung eines Verzeichniseintrages (Basisdaten und Fachdaten).

</td></tr></table>

**[\<=]**

**TIP1-A_5572 - VZD, I_Directory_Maintenance, TLS-gesicherte Verbindung**

Der VZD MUSS die Schnittstelle I_Directory_Maintenance durch Verwendung von TLS
mit beidseitiger Authentisierung sichern.Der VZD muss sich mit der Identität
ID.ZD.TLS-S authentisieren.Der VZD muss das vom FAD übergebene AUT-Zertifikat
C.FD.TLS-C hinsichtlich OCSP-Gültigkeit und Übereinstimmung mit einem
Zertifikat eines zur Nutzung dieser Schnittstelle registrierten Fachdienstes
prüfen. Bei negativem Ergebnis wird der Verbindungsaufbau abgebrochen.
**[\<=]**

**TIP1-A_5574 - VZD und Nutzer der Schnittstelle I_Directory_Maintenance,
WebService**

Der VZD und Nutzer der Schnittstelle MÜSSEN die Schnittstelle
I_Directory_Maintenance als SOAP-Webservice über HTTPS implementieren.
DerWebservice wird durch die Dokumente DirectoryMaintenance.wsdl und
DirectoryMaintenance.xsd definiert. **[\<=]**

### 4.2.1 Operation add_Directory_Entry

Diese Operation legt einen neuen Basisdatensatz an oder überschreibt einen
bestehenden Datensatz im LDAP Verzeichnis.

### 4.2.1.1 Umsetzung

**TIP1-A_5575 - VZD, Umsetzung add_Directory_Entry**

Der VZD MUSS nach folgenden Vorgaben die
Operationadd_Directory_Entryimplementieren:

 ---> OL

Es müssen die Fehlermeldungen gemäß Tab_TUC_VZD_0002 verwendet werden. **[\<=]**

In der folgenden Tabelle sind die Regeln zur Transformation
von I_Directory_Maintenance Request Elementen zu LDAP-Directory Attributen
und die Regeln zur Transformation aus LDAP-Directory Attributen
zu I_Directory_Maintenance Response Elementen beschrieben.

<table><tr><th>
I_Directory_Maintenance Request Element

</th><th>
LDAP-Directory Attribut

</th><th>
I_Directory_Maintenance Response Element

</th><th>
Zusatzinformation

</th></tr><tr><td>
n/a

</td><td>
givenname

</td><td>
givenname

</td><td>
Verwendung gemäß Tab_VZD_Datenbeschreibung

</td></tr><tr><td>
n/a

</td><td>
sn  
SMC-B: Wird vom VZD als Kopie von otherName eingetragen.

</td><td>
surname

</td><td>
Verwendung gemäß Tab_VZD_Datenbeschreibung

</td></tr><tr><td>
n/a

</td><td>
cn  
Wird vom VZD als Kopie von otherName eingetragen.

</td><td>
commonName

</td><td>
Verwendung gemäß Tab_VZD_Datenbeschreibung

</td></tr><tr><td>
n/a

</td><td>
displayName  
Wird vom VZD als Kopie von otherName eingetragen.

</td><td>
displayName

</td></tr><tr><td>
streetAddress

</td><td>
streetAddress

</td><td>
streetAddress

</td><td>
Alias street

Der Alias-Wert wird in der LDAP Response verwendet.

</td></tr><tr><td>
postalCode

</td><td>
postalCode

</td><td>
postalCode

</td></tr><tr><td>
localityName

</td><td>
localityName

</td><td>
localityName

</td><td>
Alias l

Der Alias-Wert wird in der LDAP Response verwendet.

</td></tr><tr><td>
stateOrProvinceName

</td><td>
stateOrProvinceName

</td><td>
stateOrProvinceName

</td><td>
Alias st

Der Alias-Wert wird in der LDAP Response verwendet.

</td></tr><tr><td>
title

</td><td>
title

</td><td>
title

</td><td>
Verwendung gemäß Tab_VZD_Datenbeschreibung

</td></tr><tr><td>
organization

</td><td>
organization

</td><td>
organization

</td><td>
Alias o  
Der Alias-Wert wird in der LDAP Response verwendet.  
Verwendung
gemäß Tab_VZD_Datenbeschreibung

</td></tr><tr><td>
otherName

</td><td>
otherName  
SMC-B: wird vom VZD zusätzlich in displayName, surname und cn
eingetragen

</td><td>
otherName

</td><td>
Verwendung gemäß Tab_VZD_Datenbeschreibung

</td></tr><tr><td>
subject

</td><td>
specialization

</td><td>
subject

</td><td>
Verwendung gemäß Tab_VZD_Datenbeschreibung

</td></tr><tr><td>
n/a

</td><td>
domainID

</td><td>
n/a

</td></tr><tr><td>
n/a

</td><td>
personalEntry

</td><td>
n/a

</td><td>
Verwendung gemäß Tab_VZD_Datenbeschreibung

</td></tr><tr><td>
x509CertificateEnc

</td><td>
userCertificate

</td><td>
x509CertificateEnc

</td><td>
Verwendung gemäß Tab_VZD_Datenbeschreibung

</td></tr><tr><td>
n/a

</td><td>
entryType

</td><td>
n/a

</td><td>
Verwendung gemäß Tab_VZD_Datenbeschreibung

</td></tr><tr><td>
n/a

</td><td>
telematikID

</td><td>
telematikID

</td><td>
Verwendung gemäß Tab_VZD_Datenbeschreibung

</td></tr><tr><td>
n/a

</td><td>
professionOID

</td><td>
n/a

</td><td>
Verwendung gemäß Tab_VZD_Datenbeschreibung

</td></tr><tr><td>
n/a

</td><td>
usage

</td><td>
n/a

</td><td>
Verwendung gemäß Tab_VZD_Datenbeschreibung

</td></tr><tr><td>
n/a

</td><td>
description

</td><td>
n/a

</td></tr><tr><td>
timestamp

</td><td>
n/a

</td><td>
timestamp

</td><td>
Datum und Zeit des Requests bzw. der Response

</td></tr><tr><td>
variant

</td><td>
n/a  
HBA: Wenn variant == full, dann werden givenName und sn aus dem Zertifikat
in die gleichnamigen LDAP Attribute übernommen.

</td><td>
n/a

</td></tr><tr><td>
givenname

</td><td>
n/a

</td><td>
n/a

</td></tr><tr><td>
surname

</td><td>
n/a

</td><td>
n/a

</td></tr><tr><td>
commonName

</td><td>
n/a

</td><td>
n/a

</td></tr><tr><td>
serviceData

</td><td>
n/a

</td><td>
n/a

</td></tr><tr><td>
n/a

</td><td>
n/a

</td><td>
status

</td></tr></table>

### 4.2.1.2 Nutzung

**TIP1-A_5576 - Nutzer der Schnittstelle, TUC_VZD_0002
„add_Directory_Entry”**

Der Nutzer der Schnittstelle MUSS den technischen Use Case TUC_VZD_0002
„add_Directory_Entry” gemäß Tabelle Tab_TUC_VZD_0002 umsetzen.Der
SOAP-Requests MUSS gemäß Tab_VZD_Datenbeschreibung mit der Bedeutung
entsprechenden Daten ausgefüllt sein.

Tabelle6: Tab_TUC_VZD_0002

<table><tr><th>
Name

</th><th colspan="2">
TUC_VZD_0002 „add_Directory_Entry”

</th></tr><tr><td>
Beschreibung

</td><td colspan="2">
Diese Operation ermöglicht die Erzeugung von neuen Basisdaten.  
Bestehende
Basisdaten werden überschrieben.

</td></tr><tr><td>
Vorbedingungen

</td><td colspan="2">
keine

</td></tr><tr><td>
Eingangsdaten

</td><td colspan="2">
SOAP-Request „addDirectoryEntry“

</td></tr><tr><td>
Komponenten

</td><td colspan="2">
Nutzer der Schnittstelle, Verzeichnisdienst

</td></tr><tr><td>
Ausgangsdaten

</td><td colspan="2">
SOAP-Response „VZD:responseMsg“

</td></tr><tr><td rowspan="4">
Standardablauf

</td><td>
Aktion

</td><td>
Beschreibung

</td></tr><tr><td>
Aufbau TLS-Verbindung

</td><td>
Wenn noch keine Verbindung besteht initiiert der Nutzer der Schnittstelle den
Verbindungsaufbau.  
Der Nutzer der Schnittstelle authentisiert sich mit dem
AUT-Zertifikat C.FD.TLS-C.

</td></tr><tr><td>
SOAP-Request senden

</td><td>
Der Nutzer der Schnittstelle ruft die SOAP-Operation VZD:addDirectoryEntry auf.

</td></tr><tr><td>
SOAP-Response empfangen

</td><td>
Die SOAP-Response VZD:responseMsg mit dem VZD:status wird empfangen.

</td></tr><tr><td>
Varianten/Alternativen

</td><td>
keine

</td><td>
</td></tr><tr><td>
Fehlerfälle

</td><td colspan="2">
Es werden die protokollspezifischen Fehlermeldungen verwendet (TCP, HTTP, TLS). 

Fehler bei der Verarbeitung des SOAP Requests werden als gematik SOAP-Fault
versendet:  
faultcode 4211,  faultstring: Operation fehlerhaft ausgeführt,
Basisdaten konnten nicht angelegt werden (Fehler im Verzeichnisdienst) 

faultcode 4202,  faultstring: SOAP Request enthält Fehler  
faultcode
4201,  faultstring: Operation enthält ungültige Daten  
Erkannte Fehler auf
Transportprotokollebene müssen auf gematik SOAP Faults (Code 6 aus Tabelle
Tab_Gen_Fehler aus [gemSpec_OM]) abgebildet werden. Zusätzlich müssen die
generischen gematik SOAP-Faults  
Code 2: Verbindung zurückgewiesen  
Code 3:
Nachrichtenschema fehlerhaft  
Code 4: Version Nachrichtenschema fehlerhaft 

unterstützt werden.

</td></tr></table>

**[\<=]**

### 4.2.2 Operation read_Directory_Entry

Diese Operation liest einen vollständigen Eintrag aus dem LDAP Verzeichnis aus.

### 4.2.2.1 Umsetzung

**TIP1-A_5577 - VZD, Umsetzung read_Directory_Entry**

Der VZD MUSS nach folgenden Vorgaben die Operation
I_Directory_Maintenance::read_Directory_Entry implementieren:

 ---> OL

Es müssen die Fehlermeldungen gemäß Tab_TUC_VZD_0003 verwendet werden. **[\<=]**

### 4.2.2.2 Nutzung

**TIP1-A_5578 - Nutzer der Schnittstelle, TUC_VZD_0003
„read_Directory_Entry”**

Der Nutzer der Schnittstelle MUSS den technischen Use Case TUC_VZD_0003
„read_Directory_Entry” gemäß Tabelle Tab_TUC_VZD_0003 umsetzen. Der
Webservice wird durch die Dokumente DirectoryMaintenance.wsdl und
DirectoryMaintenance.xsd definiert.Die SOAP-Response ist gemäß
Tabelle Tab_VZD_Datenbeschreibung mit den zur Telematik-ID gehörenden Daten
aus dem VZD ausgefüllt.

Tabelle7: Tab_TUC_VZD_0003

<table><tr><th>
Name

</th><th colspan="2">
TUC_VZD_0003 „read_Directory_Entry”

</th></tr><tr><td>
Beschreibung

</td><td colspan="2">
Diese Operation liest einen vollständigen Eintrag aus dem VZD aus.

</td></tr><tr><td>
Vorbedingungen

</td><td colspan="2">
Keine

</td></tr><tr><td>
Eingangsdaten

</td><td colspan="2">
SOAP-Request „readDirectoryEntry“

</td></tr><tr><td>
Komponenten

</td><td colspan="2">
Nutzer der Schnittstelle, Verzeichnisdienst

</td></tr><tr><td>
Ausgangsdaten

</td><td colspan="2">
SOAP-Response „readResponseMsg“

</td></tr><tr><td rowspan="4">
Standardablauf

</td><td>
Aktion

</td><td>
Beschreibung

</td></tr><tr><td>
Aufbau TLS-Verbindung

</td><td>
Wenn noch keine Verbindung besteht initiiert der Nutzer der Schnittstelle den
Verbindungsaufbau.  
Der Nutzer der Schnittstelle authentisiert sich mit dem
AUT-Zertifikat C.FD.TLS-C.

</td></tr><tr><td>
SOAP-Request senden

</td><td>
Der Nutzer der Schnittstelle ruft die SOAP-Operation VZD:readDirectoryEntry auf.

</td></tr><tr><td>
SOAP-Response empfangen

</td><td>
Die SOAP-Response VZD:readResponseMsg mit allen Basisdaten wird empfangen.

</td></tr><tr><td>
Varianten/Alternativen

</td><td>
keine

</td><td>
</td></tr><tr><td>
Fehlerfälle

</td><td colspan="2">
Es werden die protokollspezifischen Fehlermeldungen verwendet (TCP, HTTP, TLS) 

Fehler bei der Verarbeitung des SOAP Requests werden als gematik SOAP-Fault
versendet:  
faultcode

4221, faultstring: Operation fehlerhaft ausgeführt, Basisdaten konnten nicht
gelesen werden (Fehler im Verzeichnisdienst)  
faultcode 4312,  faultstring:
Basisdaten konnten nicht gefunden werden  
faultcode 4202,  faultstring: SOAP
Request enthält Fehler  
Erkannte Fehler auf Transportprotokollebene müssen
auf gematik SOAP Faults (Code 6 aus Tabelle Tab_Gen_Fehler aus [gemSpec_OM])
abgebildet werden. Zusätzlich müssen die generischen gematik SOAP-Faults 

Code 2: Verbindung zurückgewiesen  
Code 3: Nachrichtenschema fehlerhaft 

Code 4: Version Nachrichtenschema fehlerhaft  
unterstützt werden.

</td></tr></table>

**[\<=]**

### 4.2.3 Operation modify_Directory_Entry

Diese Operation ändert die Daten eines bestehenden Basisdatensatzes im LDAP
Verzeichnis.

### 4.2.3.1 Umsetzung

**TIP1-A_5579 - VZD, Umsetzung modify_Directory_Entry**

Der VZD MUSS nach folgenden Vorgaben die Operation modify_Directory_Entry
implementieren:

 ---> OL

Es müssen die Fehlermeldungen gemäß Tab_TUC_VZD_0004 verwendet werden. **[\<=]**

### 4.2.3.2 Nutzung

**TIP1-A_5580 - Nutzer der Schnittstelle, TUC_VZD_0004
„modify_Directory_Entry”**

Der Nutzer der Schnittstelle MUSS den technischen Use Case TUC_VZD_0004
„modify_Directory_Entry” gemäß Tabelle Tab_TUC_VZD_0004 umsetzen. Der
Webservice wird durch die Dokumente DirectoryMaintenance.wsdl und
DirectoryMaintenance.xsd definiert.Der SOAP-Requests MUSS gemäß Tabelle
VZD_TAB_modifyDirectoryEntry_Mapping mit der Bedeutung entsprechenden Daten
ausgefüllt sein.

Tabelle8: Tab_TUC_VZD_0004

<table><tr><th>
Name

</th><th colspan="2">
TUC_VZD_0004 „modify_Directory_Entry”

</th></tr><tr><td>
Beschreibung

</td><td colspan="2">
Diese Operation ermöglicht die

Änderung

von

Basisdaten.

</td></tr><tr><td>
Vorbedingungen

</td><td colspan="2">
keine

</td></tr><tr><td>
Eingangsdaten

</td><td colspan="2">
SOAP-Request „modifyDirectoryEntry“

</td></tr><tr><td>
Komponenten

</td><td colspan="2">
Nutzer der Schnittstelle, Verzeichnisdienst

</td></tr><tr><td>
Ausgangsdaten

</td><td colspan="2">
SOAP-Response „responseMsg“

</td></tr><tr><td rowspan="4">
Standardablauf

</td><td>
Aktion

</td><td>
Beschreibung

</td></tr><tr><td>
Aufbau TLS-Verbindung

</td><td>
Wenn noch keine Verbindung besteht initiiert der Nutzer der Schnittstelle den
Verbindungsaufbau.  
Der Nutzer der Schnittstelle authentisiert sich mit dem
AUT-Zertifikat C.FD.TLS-C.

</td></tr><tr><td>
SOAP-Request senden

</td><td>
Der Nutzer der Schnittstelle ruft die SOAP-Operation VZD:modifyDirectoryEntry
auf.

</td></tr><tr><td>
SOAP-Response empfangen

</td><td>
Die SOAP-Response VZD:responseMsg mit dem VZD:status wird empfangen.

</td></tr><tr><td>
Varianten/Alternativen

</td><td>
keine

</td><td>
</td></tr><tr><td>
Fehlerfälle

</td><td colspan="2">
Es werden die protokollspezifischen Fehlermeldungen verwendet (TCP, HTTP, TLS) 

Fehler bei der Verarbeitung des SOAP Requests werden als gematik SOAP-Fault
versendet:  
faultcode 4231,  faultstring: Operation fehlerhaft ausgeführt,
Basisdaten konnten nicht modifiziert werden (Fehler im Verzeichnisdienst) 

faultcode 4312,  faultstring: Basisdaten konnten nicht gefunden werden 

faultcode 4202,  faultstring: SOAP Request enthält Fehler  
Erkannte Fehler
auf Transportprotokollebene müssen auf gematik SOAP Faults (Code 6 aus Tabelle
Tab_Gen_Fehler aus [gemSpec_OM]) abgebildet werden. Zusätzlich müssen die
generischen gematik SOAP-Faults  
Code 2: Verbindung zurückgewiesen  
Code 3:
Nachrichtenschema fehlerhaft  
Code 4: Version Nachrichtenschema fehlerhaft 

unterstützt werden.

</td></tr></table>

**[\<=]**

### 4.2.4 Operation delete_Directory_Entry

Diese Operation löscht einen bestehenden Datensatz im LDAP Verzeichnis.

### 4.2.4.1 Umsetzung

**TIP1-A_5581 - VZD, Umsetzung delete_Directory_Entry**

Der VZD MUSS nach folgenden Vorgaben die Operation
I_Directory_Maintenance::delete_Directory_Entry implementieren:

 ---> OL

Es müssen die Fehlermeldungen gemäß Tab_TUC_VZD_0005 verwendet werden. **[\<=]**

### 4.2.4.2 Nutzung

**TIP1-A_5582 - Nutzer der Schnittstelle, TUC_VZD_0005
„delete_Directory_Entry”**

Der Nutzer der Schnittstelle MUSS den technischen Use Case TUC_VZD_0005
„delete_Directory_Entry” gemäß Tabelle Tab_TUC_VZD_0005 umsetzen. Der
Webservice wird durch die Dokumente DirectoryMaintenance.wsdl und
DirectoryMaintenance.xsd definiert.

Tabelle9: Tab_TUC_VZD_0005

<table><tr><th>
Name

</th><th colspan="2">
TUC_VZD_0005 „delete_Directory_Entry”

</th></tr><tr><td>
Beschreibung

</td><td colspan="2">
Diese Operation ermöglicht die

Löschung 

von

Basisdaten

inkl. der zugehörigen Fachdaten.

</td></tr><tr><td>
Vorbedingungen

</td><td colspan="2">
keine

</td></tr><tr><td>
Eingangsdaten

</td><td colspan="2">
SOAP-Request „deleteDirectoryEntry“

</td></tr><tr><td>
Komponenten

</td><td colspan="2">
Nutzer der Schnittstelle, Verzeichnisdienst

</td></tr><tr><td>
Ausgangsdaten

</td><td colspan="2">
SOAP-Response „responseMsg“

</td></tr><tr><td rowspan="4">
Standardablauf

</td><td>
Aktion

</td><td>
Beschreibung

</td></tr><tr><td>
Aufbau TLS-Verbindung

</td><td>
Wenn noch keine Verbindung besteht initiiert der Nutzer der Schnittstelle den
Verbindungsaufbau.  
Der Nutzer der Schnittstelle authentisiert sich mit dem
AUT-Zertifikat C.FD.TLS-C.

</td></tr><tr><td>
SOAP-Request senden

</td><td>
Der Nutzer der Schnittstelle ruft die SOAP-Operation VZD:deleteDirectoryEntry
auf.

</td></tr><tr><td>
SOAP-Response empfangen

</td><td>
Die SOAP-Response VZD:responseMsg mit dem VZD:status wird empfangen.

</td></tr><tr><td>
Varianten/Alternativen

</td><td>
keine

</td><td>
</td></tr><tr><td>
Fehlerfälle

</td><td colspan="2">
Es werden die protokollspezifischen Fehlermeldungen verwendet (TCP, HTTP, TLS) 

Fehler bei der Verarbeitung des SOAP Requests werden als gematik SOAP-Fault
versendet:  
faultcode 4241,  faultstring: Operation fehlerhaft ausgeführt,
Basisdaten konnten nicht gelöscht werden (Fehler im Verzeichnisdienst) 

faultcode 4312,  faultstring: Basisdaten konnten nicht gefunden werden 

faultcode 4202,  faultstring: SOAP Request enthält Fehler  
Erkannte Fehler
auf Transportprotokollebene müssen auf gematik SOAP Faults (Code 6 aus Tabelle
Tab_Gen_Fehler aus [gemSpec_OM]) abgebildet werden. Zusätzlich müssen die
generischen gematik SOAP-Faults  
Code 2: Verbindung zurückgewiesen  
Code 3:
Nachrichtenschema fehlerhaft  
Code 4: Version Nachrichtenschema fehlerhaft 

unterstützt werden.

</td></tr></table>

**[\<=]**

### 4.3 Schnittstelle I_Directory_Application_Maintenance

Die Schnittstelle ermöglicht die Administration der Fachdaten.

Der VZD stellt diese Schnittstelle als LDAPv3 und Webservice (SOAP und REST)
bereit. Deshalb sind die Unterkapitel „Nutzung“ und „Umsetzung“ jeweils
für LDAPv3 und Webservice (SOAP und REST) vorhanden.

**TIP1-A_5583-02 - VZD, Schnittstelle I_Directory_Application_Maintenance**

Der VZD MUSS die Schnittstelle I_Directory_Application_Maintenance gemäß
TabelleTab_VZD_Schnittstelle_I_Directory_Application_Maintenance anbieten.

Tabelle10: Tab_VZD_Schnittstelle_I_Directory_Application_Maintenance

<table><tr><th>
Name

</th><th colspan="2">
I_Directory_Application_Maintenance

</th></tr><tr><td>
Version

</td><td colspan="2">
wird im Produkttypsteckbrief des VZD definiert

</td></tr><tr><td colspan="1" rowspan="6">
Operationen

</td><td>
Operation

</td><td>
Kurzbeschreibung

</td></tr><tr><td>
getInfo

</td><td>
Lesen der Metadaten dieser Schnittstelle (nur für die REST-Ausprägung
verfügbar)

</td></tr><tr><td>
add_Directory_FA-Attributes

</td><td>
Erzeugung eines Fachdaten-Eintrags

</td></tr><tr><td>
delete_Directory_FA-Attributes

</td><td>
Löschen von einzelnen oder allen zu einem FAD gehörenden Fachdaten eines
Eintrags.

</td></tr><tr><td>
modify_Directory_FA-Attributes

</td><td>
Ändern fachspezifischer Attribute

</td></tr><tr><td>
get_Directory_FA_Attributes

</td><td>
Lesen fachspezifischer Attribute

</td></tr></table>

**[\<=]**

**TIP1-A_5584 - VZD, Änderung nur durch registrierte FAD**

Der Anbieter des VZD MUSS sicherstellen, dass Fachdaten eines Dienstes nur durch
einen beim VZD für diesen Dienst registrierten Fachdienst erzeugt, gelöscht
und geändert werden können. **[\<=]**

Dazu wird bei der Registrierung eine FAD zugeordnet. Unter dieser FAD werden die
Fachdaten für den jeweiligen Dienst im VZD abgelegt. Die Zuordnung der FAD zu
dem Dienst wird bei Aufruf jeder Operation von Schnittstelle
I_Directory_Application_Maintenance durch den VZD geprüft (z.B. anhand des
TLS-Client-Zertifikats oder OAuth2 Tokens).

**TIP1-A_5585 - VZD, I_Directory_Application_Maintenance, TLS-gesicherte
Verbindung**

Der VZD MUSS die Schnittstelle I_Directory_Application_Maintenance durch
Verwendung von TLS mit beidseitiger Authentisierung sichern.

Der VZD muss sich mit der Identität ID.ZD.TLS-S authentisieren.

Der VZD muss das vomFADübergebeneAUT-Zertifikat C.FD.TLS-Chinsichtlich OCSP
Gültigkeit und Übereinstimmung mit einem Zertifikat eines zur Nutzung dieser
Schnittstelle registrierten Fachdienstesprüfen. Bei negativem Ergebnis wirdder
Verbindungsaufbau abgebrochen. **[\<=]**

**TIP1-A_5586-01 - VZD, I_Directory_Application_Maintenance, Webservice und
LDAPv3**

Der VZD MUSS die Schnittstelle I_Directory_Application_Maintenance als
Webservice (SOAP und REST über HTTPS) und als LDPv3 über LDAPS
implementieren. Der Webservice (SOAP) wird durch die Dokumente
DirectoryApplicationMaintenance.wsdl und DirectoryApplicationMaintenance.xsd
definiert. Der Webservice (REST) wird durch die
[Directory_Application_Maintenance.yaml] Datei definiert. Die LDAPv3-Attribute
sind in dem Informationsmodell Abb_VZD_logisches_Datenmodell beschrieben.
**[\<=]**

**TIP1-A_5587 - VZD, Implementierung der LDAPv3 Schnittstelle**

Der VZD MUSS die Schnittstelle I_Directory_Application_Maintenance gemäß den
LDAPv3 Standards [RFC4510], [RFC4511], [RFC4512], [RFC4513], [RFC4514],
[RFC4515], [RFC4516], [RFC4517], [RFC4518], [RFC4519], [RFC4520], [RFC4522] und
[RFC4523] implementieren. **[\<=]**

**TIP1-A_5588 - FAD, I_Directory_Application_Maintenance, Nutzung LDAP v3 oder
Webservice**

Ein FAD, der Fachdaten im VZD verwalten will, MUSS entweder die Webservice- oder
die LDAPv3-Schnittstelle nutzen. **[\<=]**

**TIP1-A_5589 - FAD, Implementierung der LDAPv3 Schnittstelle**

Der FAD, der die LDAPv3-Schnittstelle I_Directory_Application_Maintenance des
VZD nutzt, MUSS diese Schnittstelle gemäß den LDAPv3 Standards [RFC4510],
[RFC4511], [RFC4512], [RFC4513], [RFC4514], [RFC4515], [RFC4516], [RFC4517],
[RFC4518], [RFC4519], [RFC4520], [RFC4522] und [RFC4523] implementieren. Die
LDAPv3-Attribute sind in dem Informationsmodell Abb_VZD_logisches_Datenmodell
beschrieben. **[\<=]**

**A_21466 - VZD, I_Directory_Application_Maintenance, OAuth2 Dienst**

Der VZD MUSS einen OAuth2-Dienst bereitstellen. Dieser Dienst MUSS die Clients
der Schnittstelle I_Directory_Application_Maintenance anhand ihrer Client
Credentials und Umgebung (RU/TU/PU) authentisieren und ihnen ein AccessToken
entsprechend [RFC 6750] ausstellen. Das AccessToken muss im "sub" claim den
Identifier des Clients enthalten. **[\<=]**

**A_21467 - VZD, I_Directory_Administration, Prüfung AccessToken**

Der VZD MUSS das vom Client übergebene AccessToken auf Gültigkeit für
Schnittstelle  I_Directory_Application_Maintenance und Umgebung (RU/TU/PU)
prüfen. Bei negativem Ergebnis muss die Operation mit HTTP Fehler 401
Unauthorized abgebrochen werden. **[\<=]**

Beispiel für den Aufbau der Fachdaten (siehe auch
Abb_VZD_logisches_Datenmodell):

    FAD1: [class FAD1 {        dn: class DistinguishedName {         
  uid: c57796f2-96a7-493b-a827-0b125437502e            dc: [vzd,
telematik]            ou: [FAD0016, KOM-LE]            cn: null 
      }        mail: [Oldenburg@FAD0016-Malsehen-Mod-Paul-8.com,
Oldenburg@FAD0016-Malsehen-Mod-Paul-9.com,
Oldenburg@FAD0016-Malsehen-Mod-Paul-10.com,
Oldenburg@FAD0016-Malsehen-Mod-Paul-11.com]        koMLEVersion: null   
}]

Hinweis: Das Attribut providerName (identifiziert, zu welchem Provider die
Fachdaten gehören) in der SOAP Schnittstelle entspricht in Schnittstelle
I_Directory_Application_Maintenance dem ou Eintrag im DN des FAD1 Eintrags.

### 4.3.1 Operation getInfo

Diese Operation liefert die Metadaten der Schnittstelle
I_Directory_Application_Maintenance.

### 4.3.1.1 Umsetzung REST

**A_21788 - VZD, Umsetzung I_Directory_Application_Maintenance getInfo (REST)**

Der VZD MUSS nach folgenden Vorgaben die Operation getInfo implementieren:In dem
Rückgabewerten müssen die aktuell gültigen Metainformationen für
Schnittstelle I_Directory_Application_Maintenance zurückgegeben werden.
Insbesondere muss

 ---> OL **[\<=]**

In dem Dokument unter dieser URL muss ein Link zum Download der aktuell
genutzten YAML-Datei dieser Schnittstelle hinterlegt sein.

### 4.3.1.2 Nutzung REST

**A_21787 - VZD, I_Directory_Application_Maintenance, getInfo**

Der VZD MUSS die Operation „getInfo” gemäß Tabelle Tab_VZD
„I_Directory_Application_Maintenance-getInfo” umsetzen.

<table><tr><td>
Name

</td><td colspan="2">
getInfo

</td></tr><tr><td>
Beschreibung

</td><td colspan="2">
Liefert die Metadaten (unter anderem aus dem InfoObject) dieser
OpenAPI-Spezifikation und ergänzt sie.

</td></tr><tr><td rowspan="3">
Eingangsdaten

</td><td colspan="2">
REST-Request GET /  
operationId: getInfo (siehe
DirectoryApplicationMaintenance.yaml)

</td></tr><tr><td>
Parameter

</td><td>
Beschreibung

</td></tr><tr><td>
keine

</td><td>
 -

</td></tr><tr><td>
Komponenten

</td><td colspan="2">
Nutzer der Schnittstelle

</td></tr><tr><td>
Ausgangsdaten

</td><td colspan="2">
REST-Response mit Metadaten (InfoObject).

</td></tr><tr><td>
Ablauf

</td><td colspan="2">
Der VZD liefert die Metadaten der Schnittstelle in der Datenstruktur InfoObject
zurück.

</td></tr><tr><td>
Fehlerfälle

</td><td colspan="2">
Es werden die protokollspezifischen Fehlermeldungen verwendet (TCP, HTTP, TLS)
und in DirectoryApplicationMaintenance.yaml mit spezifischen
Fehlerbeschreibungen ergänzt.

</td></tr></table>

**[\<=]**

### 4.3.2 Operation add_Directory_FA-Attributes

Diese Operation legt einen neuen Fachdatensatz an oder überschreibt einen
bestehenden fachdienstspezifischen Datensatz.

Voraussetzung: Die Fachdaten müssen einem Basisdateneintrag zuordenbar sein.

### 4.3.2.1 Umsetzung SOAP

**TIP1-A_5590 - VZD, Umsetzung add_Directory_FA-Attributes (SOAP)**

Der VZD MUSS nach folgenden Vorgaben die Operation add_Directory_FA-Attributes
implementieren:

 ---> OL

Tabelle12: VZD_TAB_I_Directory_Application_Maintenance_Add_Mapping

<table><tr><th>
SOAP-Request Element

</th><th>
LDAP-Directory  
Basisdatensatz Attribut

</th></tr><tr><td>
VZD:timestamp

</td><td rowspan="2">
wird nicht in das LDAP-Directory eingetragen

</td></tr><tr><td>
VZD:Telematik-ID

</td></tr><tr><td>
\<FA-Attributes\>

</td><td>
fachdienstspezifische Attribute.  
Die SOAP-Request-Elemente werden namensgleich
als LDAP-Attribute übernommen.

</td></tr></table>

Es müssen die Fehlermeldungen gemäß Tab_TUC_VZD_0006 verwendet werden. **[\<=]**

### 4.3.2.2 Nutzung SOAP

**TIP1-A_5591 - FAD, TUC_VZD_0006 “add_Directory_FA-Attributes (SOAP)”**

Der FAD MUSS den technischen Use Case TUC_VZD_0006
“add_Directory_FA-Attributes” gemäß Tabelle Tab_TUC_VZD_0006 umsetzen.

Tabelle13: Tab_TUC_VZD_0006

<table><tr><th>
Name

</th><th colspan="2">
add_Directory_FA-Attributes

</th></tr><tr><td>
Beschreibung

</td><td colspan="2">
Mit dieser Operation werden Fachdaten zu einem bestehenden Basisdaten-Eintrag
zugefügt.

</td></tr><tr><td>
Vorbedingungen

</td><td colspan="2">
Keine.

</td></tr><tr><td>
Eingangsdaten

</td><td colspan="2">
SOAP-Request „addDirectoryFAAttributes“

</td></tr><tr><td>
Komponenten

</td><td colspan="2">
VZD, FAD

</td></tr><tr><td>
Ausgangsdaten

</td><td colspan="2">
SOAP-Response „responseMsg“

</td></tr><tr><td rowspan="4">
Standardablauf

</td><td>
Aktion

</td><td>
Beschreibung

</td></tr><tr><td>
Aufbau TLS-Verbindung

</td><td>
Falls noch keine TLS-Verbindung besteht, wird eine aufgebaut.  
Der FAD
authentisiert sich mit ID.FD.TLS-C.

</td></tr><tr><td>
SOAP-Request senden

</td><td>
Der FAD ruft die SOAP-Operation VZD:addDirectoryFAAttributes auf.

</td></tr><tr><td>
SOAP-Response empfangen

</td><td>
Die SOAP-Response VZD:responseMsg enthält den vzd:status.  
Im Fehlerfall wird
eine gematik SOAP-Fault Response empfangen

</td></tr><tr><td>
Fehlerfälle

</td><td colspan="2">
Es werden die protokollspezifischen Fehlermeldungen verwendet (TCP, HTTP, TLS). 

Fehler bei der Verarbeitung des SOAP Requests werden als gematik SOAP-Fault
versendet:  
faultcode 4311,  faultstring: Operation fehlerhaft ausgeführt,
Fachdaten konnten nicht angelegt werden (Fehler im Verzeichnisdienst) 

faultcode 4312,  faultstring: Basisdaten konnten nicht gefunden werden 

faultcode 4202,  faultstring: SOAP Request enthält Fehler

</td></tr></table>

**[\<=]**

**TIP1-A_5592-03 - FAD, KOM-LE_FA_Add_Attributes**

Der FAD MUSS für die FA KOM-LE die Fachdaten nach VZD_TAB_KOM-LE_Add_Attributes
administrieren.

Tabelle14: VZD_TAB_KOM-LE_Attributes

<table><tr><th>
SOAP-Request Element

</th><th>
LDAP-Directory  
Basisdatensatz Attribut

</th></tr><tr><td>
VZD:timestamp

</td><td rowspan="2">
wird nicht in das LDAP-Directory eingetragen

</td></tr><tr><td>
VZD:telematikID

</td></tr><tr><td>
VZD:KOM-LE-EMail-Address

</td><td>
mail

</td></tr><tr><td>
VZD:version

</td><td>
KOM-LE-Version 

</td></tr></table>

**[\<=]**

### 4.3.2.3 Umsetzung LDAPv3

**TIP1-A_5593 - VZD, Umsetzung add_Directory_FA-Attributes (LDAPv3)**

Der VZD MUSS nach folgenden Vorgaben die Operation add_Directory_FA-Attributes
implementieren:

 ---> OL

Es müssen die Fehlermeldungen gemäß Tab_TUC_VZD_0007 verwendet werden. **[\<=]**

### 4.3.2.4 Nutzung LDAPv3

**TIP1-A_5594 - FAD, TUC_VZD_0007 “add_Directory_FA-Attributes (LDAPv3)”**

Der FAD MUSS den technischen Use Case TUC_VZD_0007
„add_Directory_FA-Attributes(LDAPv3)” gemäß Tabelle Tab_TUC_VZD_0007
unterstützen.

Tabelle15: Tab_TUC_VZD_0007

<table><tr><th>
Name

</th><th colspan="2">
add_Directory_FA-Attributes(LDAPv3)

</th></tr><tr><td>
Beschreibung

</td><td colspan="2">
Mit dieser Operation werden Fachdaten zu einem bestehenden Eintrag zugefügt.

</td></tr><tr><td>
Vorbedingungen

</td><td colspan="2">
Der LDAPS-Verbindungsaufbau muss erfolgreich durchgeführt sein.

</td></tr><tr><td>
Eingangsdaten

</td><td colspan="2">
Add-Request gemäß [RFC4511]#4.7 und Informationsmodell
(Abb_VZD_logisches_Datenmodell)

</td></tr><tr><td>
Komponenten

</td><td colspan="2">
LDAP Client des FAD, Verzeichnisdienst

</td></tr><tr><td>
Ausgangsdaten

</td><td colspan="2">
gemäß [RFC4511]#4.7

</td></tr><tr><td rowspan="3">
Standardablauf

</td><td>
Aktion

</td><td>
Beschreibung

</td></tr><tr><td>
Add Request senden

</td><td>
Der LDAP Client des FAD sendet den Add-Request gemäß [RFC4511]#4.7 an den VZD.
Die RFCs [RFC4510], [RFC4511], [RFC4513], [RFC4514], [RFC4515], [RFC4516],
[RFC4519] und [RFC4522] müssen unterstützt werden.

</td></tr><tr><td>
Add Response empfangen

</td><td>
Der LDAP Client empfängt das Ergebnis der Operation gemäß [RFC4511]#4.7.

</td></tr><tr><td>
Varianten/Alternativen

</td><td>
keine

</td><td>
</td></tr><tr><td>
Zustand nach erfolgreichem Ablauf

</td><td colspan="2">
Das Ergebnis der Operation liegt im LDAP Client des FAD vor.

</td></tr><tr><td>
Fehlerfälle

</td><td colspan="2">
Zur Behandlung auftretender Fehlerfälle werden Fehlermeldungen gemäß
[RFC4511]#Appendix A verwendet.

</td></tr></table>

**[\<=]**

**A_21834 - VZD, I_Directory_Application_Maintenance, KOM-LE_Version Prüfung
LDAP**

Der VZD MUSS bei Änderungen an KOM-LE-Fachdaten mit den Operationen
“add_Directory_FA-Attributes (LDAPv3)” und "modify_Directory_FA-Attributes
(LDAPv3)" den Inhalt von Parameter KOM-LE_Version des Operation Requests gegen
die Liste der gültigen Werte prüfen. Im Falle von ungültigen Werten MUSS
der VZD mit LDAP Result Code constraintViolation (19) antworten und darf die
Operation nicht ausführen. Der VZD MUSS die Liste der gültigen Werte von
Attribut KOM-LE_Version konfigurierbar realisieren und der gematik
Änderungensmöglichkeiten über einen Service Request bieten. **[\<=]**

**A_21835 - VZD, I_Directory_Application_Maintenance, Eindeutige Zuordnung von
KOM-LE Adressen zu VZD-Einträgen LDAP**

Der VZD MUSS sicherstellen, dass jede KOM-LE-Adresse mit den Operationen
“add_Directory_FA-Attributes (LDAPv3)” und "modify_Directory_FA-Attributes
(LDAPv3)" nur an maximal einen VZD-Eintrag angehängt wird. Hierzu MUSS er vor
einer Eintragung einer KOM-LE Adresse prüfen, ob diese bereits im VZD
hinterlegt ist. Ist sie bereits hinterlegt, MUSS der VZD mit LDAP Result Code
attributeOrValueExists (20) antworten und darf die Operation nicht ausführen.
**[\<=]**

### 4.3.2.5 Umsetzung REST

**A_21458 - VZD, Umsetzung add_Directory_FA-Attributes (REST)**

Der VZD MUSS nach folgenden Vorgaben die Operation add_Directory_FA-Attributes
implementieren:

 ---> OL

**[\<=]**

### 4.3.2.6 Nutzung REST

**A_21459 - FAD, VZD, TUC_VZD_0012 “add_Directory_FA-Attributes (REST)”**

Der FAD MUSS den technischen Use Case TUC_VZD_0012
“add_Directory_FA-Attributes” gemäß Tabelle Tab_TUC_VZD_0012 umsetzen.

Tabelle 31: Tab_TUC_VZD_0012

<table><tr><th>
Name

</th><th colspan="2">
add_Directory_FA-Attributes

</th></tr><tr><td>
Beschreibung

</td><td colspan="2">
Mit dieser Operation werden Fachdaten zu einem bestehenden Basisdaten-Eintrag
zugefügt.

</td></tr><tr><td>
Vorbedingungen

</td><td colspan="2">
Keine.

</td></tr><tr><td>
Eingangsdaten

</td><td colspan="2">
REST-Request „add_Directory_FA-Attributes“

</td></tr><tr><td>
Komponenten

</td><td colspan="2">
VZD, FAD

</td></tr><tr><td>
Ausgangsdaten

</td><td colspan="2">
REST-Response

</td></tr><tr><td rowspan="4">
Standardablauf

</td><td>
Aktion

</td><td>
Beschreibung

</td></tr><tr><td>
Aufbau TLS-Verbindung

</td><td>
Falls noch keine TLS-Verbindung besteht, wird eine aufgebaut.  
Der FAD
authentisiert sich mit ID.FD.TLS-C.

</td></tr><tr><td>
REST-Request senden

</td><td>
Der FAD ruft die REST-Operation add_Directory_FA-Attributes auf.

</td></tr><tr><td>
REST-Response empfangen

</td><td>
Die REST-Response enthält den HTTP-Statuscode.  
Im Fehlerfall wird ein
HTTP-Statuscode empfangen.

</td></tr><tr><td>
Fehlerfälle

</td><td colspan="2">
Es werden die protokollspezifischen Fehlermeldungen verwendet (TCP, HTTP, TLS). 

Fehler bei der Verarbeitung des REST Requests werden als HTTP-Statuscode
versendet.

</td></tr></table>

**[\<=]**

**A_21825 - VZD, I_Directory_Application_Maintenance, KOM-LE_Version Prüfung
REST**

Der VZD MUSS bei Änderungen an KOM-LE-Fachdaten mit den Operationen
„add_Directory_FA-Attributes“ und "modify_Directory_FA-Attributes" den
Inhalt von Parameter KOM-LE_Version des Operation Requests gegen die Liste
der gültigen Werte prüfen. Im Falle von ungültigen Werten MUSS der VZD mit
HTTP-Statuscode 422 (attributeName="KOM-LE_Version"
, attributeError="erläuternder Fehlertext") antworten und darf die Operation
nicht ausführen. Der VZD MUSS die Liste der gültigen Werte von Attribut
KOM-LE_Version konfigurierbar realisieren und der gematik
Änderungensmöglichkeiten über einen Service Request bieten. **[\<=]**

**A_21826 - VZD, I_Directory_Application_Maintenance, Eindeutige Zuordnung von
KOM-LE-Adressen zu VZD-Einträgen REST**

Der VZD MUSS sicherstellen, dass jede KOM-LE Adresse mit den Operationen
„add_Directory_FA-Attributes“ und "modify_Directory_FA-Attributes" nur an
maximal einen VZD-Eintrag angehängt wird. Hierzu MUSS er vor einer Eintragung
einer KOM-LE Adresse prüfen, ob diese bereits im VZD hinterlegt ist. Ist sie
bereits hinterlegt, MUSS der VZD mit HTTP-Statuscode 422 (attributeName="mail"
, attributeError="erläuternder Fehlertext") antworten und darf die Operation
nicht ausführen. **[\<=]**

### 4.3.3 Operation delete_Directory_FA-Attributes

Diese Operation löscht einen Fachdatensatz.

### 4.3.3.1 Umsetzung SOAP

**TIP1-A_5595 - VZD, Umsetzung delete_Directory_FA-Attributes**

Der VZD MUSS nach folgenden Vorgaben die Operation delete_Directory_
FA-Attributes implementieren:

 ---> OL

Es müssen die Fehlermeldungen gemäß Tab_TUC_VZD_0008 verwendet werden. **[\<=]**

### 4.3.3.2 Nutzung SOAP

**TIP1-A_5596 - FAD, TUC_VZD_0008 “delete_Directory_FA-Attributes (SOAP)”**

Der FAD MUSS den technischen Use Case TUC_VZD_0008
“delete_Directory_FA-Attributes” gemäß Tabelle Tab_TUC_VZD_0008 umsetzen.

Tabelle16: Tab_TUC_VZD_0008

<table><tr><th>
Name

</th><th colspan="2">
delete_Directory_FA-Attributes

</th></tr><tr><td>
Beschreibung

</td><td colspan="2">
Mit dieser Operation wird ein Fachdaten-Eintrag gelöscht.

</td></tr><tr><td>
Vorbedingungen

</td><td colspan="2">
Keine.

</td></tr><tr><td>
Eingangsdaten

</td><td colspan="2">
SOAP-Request „deleteDirectoryFAAttributes“

</td></tr><tr><td>
Komponenten

</td><td colspan="2">
VZD, FAD

</td></tr><tr><td>
Ausgangsdaten

</td><td colspan="2">
SOAP-Response „responseMsg“

</td></tr><tr><td rowspan="4">
Standardablauf

</td><td>
Aktion

</td><td>
Beschreibung

</td></tr><tr><td>
Aufbau TLS-Verbindung

</td><td>
Falls noch keine TLS-Verbindung besteht, wird eine aufgebaut.  
Der FAD
authentisiert sich mit ID.FD.TLS-C.

</td></tr><tr><td>
SOAP-Request senden

</td><td>
Der FAD ruft die SOAP-Operation VZD:deleteDirectoryFAAttributes auf.

</td></tr><tr><td>
SOAP-Response empfangen

</td><td>
Die SOAP-Response VZD:responseMsg enthält den vzd:status.  
Im Fehlerfall wird
eine gematik SOAP-Fault Response empfangen

</td></tr><tr><td>
Fehlerfälle

</td><td colspan="2">
Es werden die protokollspezifischen Fehlermeldungen verwendet (TCP, HTTP, TLS). 

Fehler bei der Verarbeitung des SOAP Requests werden als gematik SOAP-Fault
versendet:  
faultcode 4321,  faultstring: Operation fehlerhaft ausgeführt,
Fachdaten konnten nicht gelöscht werden (Fehler im Verzeichnisdienst) 

faultcode 4312,  faultstring: Basisdaten konnten nicht gefunden werden 

faultcode 4202,  faultstring: SOAP Request enthält Fehler

</td></tr></table>

**[\<=]**

### 4.3.3.3 Umsetzung LDAPv3

**TIP1-A_5597 - VZD, Umsetzung delete_Directory_FA-Attributes (LDAPv3)**

Der VZD MUSS nach folgenden Vorgaben die Operation
delete_Directory_FA-Attributes implementieren:

 ---> OL

Es müssen die Fehlermeldungen gemäß Tab_TUC_VZD_0009 verwendet werden. **[\<=]**

### 4.3.3.4 Nutzung LDAPv3

**TIP1-A_5598 - FAD, TUC_VZD_0009 “delete_Directory_FA-Attributes (LDAPv3)”**

Der FAD MUSS den technischen Use Case TUC_VZD_0009
„delete_Directory_FA-Attributes(LDAPv3)” gemäß Tabelle Tab_TUC_VZD_0009
unterstützen.

Tabelle17: Tab_TUC_VZD_0009

<table><tr><th>
Name

</th><th colspan="2">
delete_Directory_FA-Attributes(LDAPv3)

</th></tr><tr><td>
Beschreibung

</td><td colspan="2">
Mit dieser Operation werden alle Fachdaten zu einem bestehenden Eintrag
gelöscht.

</td></tr><tr><td>
Vorbedingungen

</td><td colspan="2">
Der LDAPS-Verbindungsaufbau muss erfolgreich durchgeführt sein.

</td></tr><tr><td>
Eingangsdaten

</td><td colspan="2">
Delete-Request gemäß [RFC4511]#4.8 und Informationsmodell
(Abb_VZD_logisches_Datenmodell)

</td></tr><tr><td>
Komponenten

</td><td colspan="2">
LDAP Client des FAD, Verzeichnisdienst

</td></tr><tr><td>
Ausgangsdaten

</td><td colspan="2">
gemäß [RFC4511]#4.8

</td></tr><tr><td rowspan="3">
Standardablauf

</td><td>
Aktion

</td><td>
Beschreibung

</td></tr><tr><td>
Delete Request senden

</td><td>
Der LDAP Client des FAD sendet den delete-Request gemäß [RFC4511]#4.8 an den
VZD. Die RFCs [RFC4510], [RFC4511], [RFC4513], [RFC4514], [RFC4515], [RFC4516],
[RFC4519] und [RFC4522] müssen unterstützt werden.

</td></tr><tr><td>
Delete Response empfangen

</td><td>
Der LDAP Client empfängt das Ergebnis der Operation gemäß [RFC4511]#4.8.

</td></tr><tr><td>
Varianten/Alternativen

</td><td>
keine

</td><td>
</td></tr><tr><td>
Zustand nach erfolgreichem Ablauf

</td><td colspan="2">
Das Ergebnis der Operation liegt im LDAP Client des FAD vor.

</td></tr><tr><td>
Fehlerfälle

</td><td colspan="2">
Zur Behandlung auftretender Fehlerfälle werden Fehlermeldungen gemäß
[RFC4511]#Appendix A verwendet.

</td></tr></table>

**[\<=]**

### 4.3.3.5 Umsetzung REST

**A_21460 - VZD, Umsetzung delete_Directory_FA-Attributes (REST)**

Der VZD MUSS nach folgenden Vorgaben die Operation delete_Directory_
FA-Attributes implementieren:

 ---> OL

**[\<=]**

### 4.3.3.6 Nutzung REST

**A_21461 - FAD, TUC_VZD_0013 “delete_Directory_FA-Attributes (REST)”**

Der FAD MUSS den technischen Use Case TUC_VZD_0013
“delete_Directory_FA-Attributes” gemäß Tabelle Tab_TUC_VZD_0013
umsetzen.Tabelle 32: Tab_TUC_VZD_0013 **[\<=]**

### 4.3.4 Operation modify_Directory_FA-Attributes

Diese Operation überschreibt einen Fachdatensatz.

### 4.3.4.1 Umsetzung SOAP

**TIP1-A_5599 - VZD, Umsetzung modify_Directory_FA-Attributes**

Der VZD MUSS nach folgenden Vorgaben die Operation modify_Directory_
FA-Attributes implementieren:

 ---> OL

Tabelle18: VZD_TAB_I_Directory_Application_Maintenance_Modify_Mapping

<table><tr><th>
SOAP-Request Element

</th><th>
LDAP-Directory  
Basisdatensatz Attribut

</th></tr><tr><td>
VZD:timestamp

</td><td rowspan="2">
wird nicht in das LDAP-Directory eingetragen

</td></tr><tr><td>
VZD:Telematik-ID

</td></tr><tr><td>
\<FA-Attributes\>

</td><td>
fachdienstspezifische Attribute.  
Die SOAP-Request-Elemente werden namensgleich
als LDAP-Attribute übernommen.

</td></tr></table>

Es müssen die Fehlermeldungen gemäß Tab_TUC_VZD_0010 verwendet werden. **[\<=]**

### 4.3.4.2 Nutzung SOAP

**TIP1-A_5600 - FAD, TUC_VZD_0010 “modify_Directory_FA-Attributes (SOAP)”**

Der FAD MUSS den technischen Use Case TUC_VZD_0010
“modify_Directory_FA-Attributes” gemäß Tabelle Tab_TUC_VZD_0010 umsetzen.

Tabelle19: Tab_TUC_VZD_0010

<table><tr><th>
Name

</th><th colspan="2">
modify_Directory_FA-Attributes

</th></tr><tr><td>
Beschreibung

</td><td colspan="2">
Mit dieser Operation werden Fachdaten geändert.

</td></tr><tr><td>
Vorbedingungen

</td><td colspan="2">
Keine.

</td></tr><tr><td>
Eingangsdaten

</td><td colspan="2">
SOAP-Request „modifyDirectoryFAAttributes“

</td></tr><tr><td>
Komponenten

</td><td colspan="2">
VZD, FAD

</td></tr><tr><td>
Ausgangsdaten

</td><td colspan="2">
SOAP-Response „responseMsg“

</td></tr><tr><td rowspan="4">
Standardablauf

</td><td>
Aktion

</td><td>
Beschreibung

</td></tr><tr><td>
Aufbau TLS-Verbindung

</td><td>
Falls noch keine TLS-Verbindung besteht, wird eine aufgebaut.  
Der FAD
authentisiert sich mit ID.FD.TLS-C.

</td></tr><tr><td>
SOAP-Request senden

</td><td>
Der FAD ruft die  SOAP-Operation VZD:modifyDirectoryFAAttributes auf.

</td></tr><tr><td>
SOAP-Response empfangen

</td><td>
Die SOAP-Response VZD:responseMsg enthält den vzd:status.  
Im Fehlerfall wird
eine gematik SOAP-Fault Response empfangen

</td></tr><tr><td>
Fehlerfälle

</td><td colspan="2">
Es werden die protokollspezifischen Fehlermeldungen verwendet (TCP, HTTP, TLS). 

Fehler bei der Verarbeitung des SOAP Requests werden als gematik SOAP-Fault
versendet:  
faultcode 4331,  faultstring: Operation fehlerhaft ausgeführt,
Fachdaten konnten nicht geändert werden (Fehler im Verzeichnisdienst) 

faultcode 4312,  faultstring: Basisdaten konnten nicht gefunden werden 

faultcode 4202,  faultstring: SOAP Request enthält Fehler

</td></tr></table>

**[\<=]**

**TIP1-A_5601-03 - FAD, KOM-LE_FA_Modify_Attributes**

Der FAD MUSS für die FA KOM-LE die Fachdaten nach
VZD_TAB_KOM-LE_Modify_Attributes administrieren.

Tabelle20: VZD_TAB_KOM-LE_Attributes

<table><tr><th>
SOAP-Request Element

</th><th>
LDAP-Directory  
Basisdatensatz Attribut

</th></tr><tr><td>
VZD:timestamp

</td><td rowspan="2">
wird nicht in das LDAP-Directory eingetragen

</td></tr><tr><td>
VZD:telematikID

</td></tr><tr><td>
VZD:KOM-LE-EMail-Address

</td><td>
mail

</td></tr><tr><td>
VZD:version

</td><td>
KOM-LE-Version 

</td></tr></table>

**[\<=]**

### 4.3.4.3 Umsetzung LDAPv3

**TIP1-A_5602 - VZD, Umsetzung modify_Directory_FA-Attributes (LDAPv3)**

Der VZD MUSS nach folgenden Vorgaben die Operation
modify_Directory_FA-Attributes implementieren:

 ---> OL

Es müssen die Fehlermeldungen gemäß Tab_TUC_VZD_0011 verwendet werden. **[\<=]**

### 4.3.4.4 Nutzung LDAPv3

**TIP1-A_5603 - FAD, TUC_VZD_0011 “modify_Directory_FA-Attributes (LDAPv3)”**

Der FAD MUSS den technischen Use Case TUC_VZD_0011
„modify_Directory_FA-Attributes(LDAPv3)” gemäß Tabelle Tab_TUC_VZD_0011
unterstützen.

Tabelle21: Tab_TUC_VZD_0011

<table><tr><th>
Name

</th><th colspan="2">
modify_Directory_FA-Attributes(LDAPv3)

</th></tr><tr><td>
Beschreibung

</td><td colspan="2">
Mit dieser Operation werden Fachdaten zu einem bestehenden Eintrag geändert.

</td></tr><tr><td>
Vorbedingungen

</td><td colspan="2">
Der LDAPS-Verbindungsaufbau muss erfolgreich durchgeführt sein.

</td></tr><tr><td>
Eingangsdaten

</td><td colspan="2">
Modify-Request gemäß [RFC4511]#4.6 und Informationsmodell
(Abb_VZD_logisches_Datenmodell)

</td></tr><tr><td>
Komponenten

</td><td colspan="2">
LDAP Client des FAD, Verzeichnisdienst

</td></tr><tr><td>
Ausgangsdaten

</td><td colspan="2">
gemäß [RFC4511]#4.6

</td></tr><tr><td rowspan="3">
Standardablauf

</td><td>
Aktion

</td><td>
Beschreibung

</td></tr><tr><td>
Modify Request senden

</td><td>
Der LDAP Client des FAD sendet den modify-Request gemäß [RFC4511]#4.6 an den
VZD. Die RFCs [RFC4510], [RFC4511], [RFC4513], [RFC4514], [RFC4515], [RFC4516],
[RFC4519] und [RFC4522] müssen unterstützt werden.

</td></tr><tr><td>
Modify Response empfangen

</td><td>
Der LDAP Client empfängt das Ergebnis der Operation gemäß [RFC4511]#4.6.

</td></tr><tr><td>
Varianten/Alternativen

</td><td>
keine

</td><td>
</td></tr><tr><td>
Zustand nach erfolgreichem Ablauf

</td><td colspan="2">
Das Ergebnis der Operation liegt im LDAP Client des FAD vor.

</td></tr><tr><td>
Fehlerfälle

</td><td colspan="2">
Zur Behandlung auftretender Fehlerfälle werden Fehlermeldungen gemäß
[RFC4511]#Appendix A verwendet.

</td></tr></table>

**[\<=]**

### 4.3.4.5 Umsetzung REST

**A_21462 - VZD, Umsetzung modify_Directory_FA-Attributes (REST)**

Der VZD MUSS nach folgenden Vorgaben die Operation modify_Directory_
FA-Attributes implementieren:

 ---> OL

**[\<=]**

### 4.3.4.6 Nutzung REST

**A_21463 - FAD, TUC_VZD_0014 “modify_Directory_FA-Attributes (REST)”**

Der FAD MUSS den technischen Use Case TUC_VZD_0014
“modify_Directory_FA-Attributes” gemäß Tabelle Tab_TUC_VZD_0014
umsetzen.Tabelle 33: Tab_TUC_VZD_0014 **[\<=]**

### 4.3.5 Operation get_Directory_FA-Attributes

Diese Operation liest einen Fachdatensatz.

### 4.3.5.1 Umsetzung REST

**A_21464 - VZD, Umsetzung get_Directory_FA-Attributes (REST)**

Der VZD MUSS nach folgenden Vorgaben die
Operationget_Directory_FA-Attributes implementieren:

 ---> OL

**[\<=]**

### 4.3.5.2 Nutzung REST

**A_21465 - FAD, TUC_VZD_0015 “get_Directory_FA-Attributes (REST)”**

Der FAD MUSS den technischen Use Case TUC_VZD_0015
“get_Directory_FA-Attributes” gemäß Tabelle Tab_TUC_VZD_0015
umsetzen.Tabelle 34: Tab_TUC_VZD_0015 **[\<=]**

### 4.4 Prozessschnittstelle P_Directory_Application_Registration (Provided)

**TIP1-A_5604 - VZD, Registrierung FADs**

Der Anbieter des VZD MUSS einen Registrierungsprozess für FAD implementieren.
Der Anbieter des VZD MUSS dazu überprüfen:

 ---> UL

Der VZD-Anbieter dokumentiert den Prozess und legt ihn dem GTI zur Freigabe vor.

Der Anbieter des VZD informiert alle FAD-Anbieter darüber, wie der Prozess
genutzt wird. **[\<=]**

**TIP1-A_5605 - VZD, De-Registrierung FADs**

Der Anbieter des VZD MUSS einen Deregistrierungsprozess für FAD
implementieren.Der VZD MUSS alle verbliebenen Fachdaten eines deregistrierten
FAD löschen.Der VZD-Anbieter dokumentiert den Prozess und legt ihn dem GTI zur
Freigabe vor.Der Anbieter des VZD informiert alle FAD-Anbieter wie der Prozess
genutzt wird. **[\<=]**

### 4.5 Prozessschnittstelle P_Directory_Maintenance (Provided)

**TIP1-A_5606 - VZD, Mandat zur Löschung von Einträgen.**

Der Anbieter des VZD MUSS einen Prozess implementieren, der es LE ermöglicht
ihren Eintrag im VZD ohne zugehörige Smartcard zu löschen.Der Anbieter des
VZD MUSS vom LE einen Nachweis fordern und prüfen, dass die zu löschenden
Daten dem LE gehören. Erst nach positivem Ergebnis der Prüfung darf gelöscht
werden.Der VZD-Anbieter dokumentiert den Prozess und legt ihn dem GTI zur
Freigabe vor. **[\<=]**

### 4.6 Schnittstelle I_Directory_Administration

Der Verzeichnisdienst (VZD) stellt ein Verzeichnis von Leistungserbringern und
Organisationen/Institutionen mit den definierten Attributen für die
Anwendungen der TI bereit. Zum Füllen und Administrieren dieser Daten durch
die Kartenherausgeber wird die Schnittstelle I_Directory_Administration
definiert.

Über diese Schnittstelle können Verzeichniseinträge inklusive Untereinträge
für Zertifikate erzeugt, aktualisiert und gelöscht werden. Die Administration
von Fachdaten erfolgt über die Schnittstelle
I_Directory_Application_Maintenance und wird durch die Fachanwendungen
durchgeführt. Operation getDirectoryEntries ermöglicht in der Schnittstelle
I_Directory_Administration das Lesen eines gesamten Verzeichniseintrags
inklusive Zertifikaten und Fachdaten.

Als Clients dieser Schnittstelle sind nur Systeme der TI-Kartenherausgeber und
von ihnen berechtigte Organisationen (z.B. TSPs) zulässig. Sie dürfen alle
Operationen zur Administration der Verzeichniseinträge nutzen.

Das ACCESS_Token enthält im "sub" claim den Identifier des Clients, der auf die
Einträge zugreift. Dieser Identifier wird im Log abgelegt, welcher die
Zugriffe über diese Schnittstelle protokolliert.

### 4.6.1 Operationen der Schnittstelle I_ Directory_Administration

Die – über diese REST Schnittstelle administrierten – Ressourcen werden
entsprechend dem logischen Datenmodell  des VZD (siehe
Abb_VZD_logisches_Datenmodell) in DirectoryAdministration.yaml definiert.

**A_18371-04 - VZD, Schnittstelle I_Directory_Administration**

Der VZD MUSS die Schnittstelle I_Directory_Administration gemäß Tabelle
Tab_VZD_Schnittstelle_I_Directory_Administration im Internet anbieten.

Tabelle22: Tab_VZD_Schnittstelle_I_Directory_Administration

<table><tr><td>
Name

</td><td colspan="2">
I_Directory_Administration

</td></tr><tr><td>
Version

</td><td colspan="2">
wird im Produkttypsteckbrief des VZD definiert

</td></tr><tr><td rowspan="17">
Operationen

</td><td colspan="2">
Resource: /                                     

(übergreifend für gesamte Schnittstelle)

</td></tr><tr><td>
Name

</td><td>
Kurzbeschreibung

</td></tr><tr><td>
GET

</td><td>
Lesen der Metadaten dieser Schnittstelle

</td></tr><tr><td colspan="2">
Resource: DirectoryEntry

</td></tr><tr><td>
Name

</td><td>
Kurzbeschreibung

</td></tr><tr><td>
POST

</td><td>
Hinzufügen eines Verzeichniseintrages inklusive dazugehörendem Zertifikat.

</td></tr><tr><td>
GET

</td><td>
Abfrage aller Daten von Verzeichniseinträgen.

</td></tr><tr><td>
PUT

</td><td>
Änderung eines Basisdaten-Verzeichniseintrages.

</td></tr><tr><td>
DELETE

</td><td>
Löschung eines Verzeichniseintrages (kompletter Datensatz inklusive aller
Zertifikate und Fachdaten).

</td></tr><tr><td colspan="2">
Resource: /DirectoryEntriesSync

</td></tr><tr><td>
Name

</td><td>
Kurzbeschreibung

</td></tr><tr><td>
GET

</td><td>
Abfrage aller Daten von Verzeichniseinträgen zu Synchronisationszwecken.

</td></tr><tr><td colspan="2">
Resource: Certificate

</td></tr><tr><td>
Name

</td><td>
Kurzbeschreibung

</td></tr><tr><td>
POST

</td><td>
Hinzufügen eines Zertifikatseintrags zu einem Verzeichniseintrag.

</td></tr><tr><td>
GET

</td><td>
Abfrage von Zertifikatseinträgen.

</td></tr><tr><td>
DELETE

</td><td>
Löschen von Zertifikatseinträgen.

</td></tr></table>

**[\<=]**

**A_18373 - VZD, Schnittstelle I_Directory_Administration**

Der VZD MUSS die Schnittstelle I_Directory_Administration als REST-Webservice
über HTTPS implementieren. Der Webservice wird durch das Dokument
DirectoryAdministration.yaml definiert. **[\<=]**

**A_18408 - VZD, I_Directory_Administration, Registrierung**

Der VZD-Anbieter MUSS für Clients der Schnittstelle I_Directory_Administration
einen Registrierungsprozess bereitstellen. Während der Registrierung muss die
Berechtigung des Antragstellers (Clients) zur Nutzung von Schnittstelle
I_Directory_Administration durch den VZD-Anbieter geprüft und durch die
gematik bestätigt werden. Nach erfolgreicher Registrierung MÜSSEN dem
Antragsteller alle nötigen Daten - inklusive OAuth Client Credentials,
CA-Zertifikat (welches zur Prüfung des Serverzertifikats durch den Client
benötigt wird), VZD-Serverzertifikat - zur Nutzung der Schnittstelle
bereitgestellt werden.  
Der VZD-Anbieter MUSS die erfolgreich registrierten
Clients immer mit aktuellen Zertifikaten versorgen. **[\<=]**

**A_20267 - VZD, I_Directory_Administration, Registrierung beim IdP als Relying
Party**

Der Anbieter des VZDMUSS sich über einen organisatorischen Prozess bei einem
vertrauenswürdigen Identity Provider (IDP) der Telematikinfrastruktur als
Relying Party registrieren und die Bereitstellung der folgenden Claims in für
Nutzer ausgestellte ACCESS_TOKEN mit dem IDP vereinbaren:

 ---> UL

damit der VZD die Fachlogik der Autorisierung und Protokollierung auf diesen
Attributen umsetzen kann. **[\<=]**

**A_20268 - VZD, Authentifizierung Nutzerrolle**

Der VZD MUSS die fachliche Rolle eines Nutzers in jedem Operationsaufruf der
Schnittstelle I_Directory_Administration anhand des Attributs "scope" im
übergebenen ACCESS_TOKEN feststellen und für die nachfolgende Rollenprüfung
je Operationsaufruf verwenden.  **[\<=]**

**A_20269 - VZD, Authentifizierung Nutzername**

Der VZD MUSS den Namen eines Nutzers in jedem Operationsaufruf anhand des
Attributs "name" im übergebenen ACCESS_TOKEN feststellen und für die
Protokollierung des Zugriffs verwenden. **[\<=]**

**A_18470 - VZD, I_Directory_Administration, Client Secret Qualität**

Der VZD-Anbieter MUSS bei der Erzeugung der OAuth client_secret‘s 128 Bit
Zufall aus einer Zufallsquelle gemäß GS-A_4367 [gemSpec_Krypt] verwenden.
**[\<=]**

**A_18409 - VZD, I_Directory_Administration, Sperrung OAuth Client Credentials**

Der VZD-Anbieter MUSS – für die gematik und den Client-Betreiber selbst -
einen Service zur Sperrung der OAuth Client Credentials anbieten. **[\<=]**

**A_18372 - VZD, I_Directory_Administration, TLS-gesicherte Verbindung**

Der VZD MUSS die Schnittstelle I_Directory_Administration durch Verwendung von
TLS mit serverseitiger Authentisierung sichern.Der VZD MUSS für diese
TLS-Verbindungen öffentliche Zertifikate nutzen (keine TI-Zertifikate).Der VZD
MUSS sich mit der Server-Identität von Schnittstelle
I_Directory_Administration authentisieren. **[\<=]**

Die Prüfung der öffentliche TLS-Server Zertifikate muss gemäß GS-A_5581
[gemSpec_Krypt] erfolgen. Dabei müssen in (1) von GS-A_5581 statt der
"Komponenten-CA-Zertifikate der TI" die CA-Zertifikate der Schnittstelle
I_Directory_Administration genutzt werden.

**A_18374 - VZD, I_Directory_Administration, Redirect**

Der VZD MUSS für die Schnittstelle I_Directory_Administration Anfragen der
Clients – welche kein AccessToken entsprechend [RFC 6750] enthalten – durch
ein Redirect zu dem OAuth2-Authentifizierungsdienst weiterleiten.  **[\<=]**

**A_18375 - VZD, I_Directory_Administration, OAuth2 Dienst**

Der VZD MUSS einen OAuth2-Dienst bereitstellen. Dieser Dienst MUSS die Clients
der Schnittstelle I_Directory_Administration anhand ihrer Client Credentials
authentisieren und ihnen ein AccessToken entsprechend [RFC 6750] ausstellen.
Das AccessToken muss im "sub" claim den Identifier des Clients enthalten. Die
Anfrage des Clients MUSS nach erfolgreicher Authentisierung durch ein Redirect
wieder zur VZD I_Directory_Administration Schnittstelle weitergeleitet werden.
**[\<=]**

**A_18376 - VZD, I_Directory_Administration, Prüfung AccessToken**

Der VZD MUSS das vom Client übergebene AccessToken auf Gültigkeit für
Schnittstelle  I_Directory_Administration prüfen. Bei negativem Ergebnis muss
die Operation mit HTTP Fehler 401 Unauthorized abgebrochen werden. **[\<=]**

**A_18471-01 - VZD, I_Directory_Administration, Datenquelle**

Der VZD MUSS bei den
Operationenadd_Directory_Entry undmodify_Directory_Entry das
LDAP-Directory-Attribut dataFromAuthority auf den Wert TRUE setzen und bei
allen anderen Operationen unverändert belassen. **[\<=]**

**A_18735 - VZD, Disable I_Directory_Maintenance, wenn dataFromAuthority TRUE**

Der VZD DARF Änderungen an VZD-Einträgen über die Schnittstelle
I_Directory_Maintenance NICHT zulassen, wenn an dem betroffenen VZD-Eintrag das
Attribut dataFromAuthority auf TRUE gesetzt ist. **[\<=]**

**A_18472-01 - VZD, I_Directory_Administration, Doubletten**

Der VZD MUSS bei den
Operationenadd_Directory_Entry undmodify_Directory_Entry prüfen, ob die
Operation eine Doublette im LDAP-Verzeichnis erzeugt und in diesem Fall die
Operation mit HTTP-Fehlercode “400 Bad Request“ ablehnen. Zur Prüfung auf
eine potentielle Dublette MUSS der VZD alle LDAP-Directory-Attribute des zu
erzeugenden Basisdatensatzes (Verzeichnisdienst_Eintrag ohne Certificate und
Fachdaten) jedoch ohne den Distinguished Name heranziehen. **[\<=]**

**A_18602 - VZD, I_Directory_Administration, keine Datenänderung über
Maintenance Schnittstelle**

Der VZD MUSS Änderungen an Basisdatensätzen und Zertifikatseinträgen
(Certificate in Abb_VZD_logisches_Datenmodell) über andere Schnittstellen
verhindern, wenn für den jeweiligen Eintrag Daten über die Schnittstelle
I_Directory_Administration eingetragen wurden (LDAP-Directory Attribut
dataFromAuthority == TRUE).Nicht erlaubte Änderungen MUSS der VZD mit
faultcode 4202 (faultstring: SOAP Request enthält Fehler) ablehnen. **[\<=]**

### 4.6.1.1 I_Directory_Administration - Lesen der Metadaten

Über Operation getInfo können die Metadaten der Schnittstelle
I_Directory_Administration gelesen werden.

### 4.6.1.1.1 GET

Diese Operation liefert die Metadaten der Schnittstelle
I_Directory_Administration.

**A_21786 - VZD, I_Directory_Administration, getInfo**

Der VZD MUSS Operation „getInfo” gemäß Tabelle Tab_VZD
„I_Directory_Administration-Info” umsetzen.

<table><tr><td>
Name

</td><td colspan="2">
getInfo

</td></tr><tr><td>
Beschreibung

</td><td colspan="2">
Liefert die Metadaten (unter anderem aus dem InfoObject) dieser OpenAPI
Spezifikation.

</td></tr><tr><td rowspan="3">
Eingangsdaten

</td><td colspan="2">
REST-Request GET /  
operationId: (siehe DirectoryAdministration.yaml)

</td></tr><tr><td>
Parameter

</td><td>
Beschreibung

</td></tr><tr><td>
keine

</td><td>
 -

</td></tr><tr><td>
Komponenten

</td><td colspan="2">
Nutzer der Schnittstelle

</td></tr><tr><td>
Ausgangsdaten

</td><td colspan="2">
REST-Response mit Metadaten (InfoObject).

</td></tr><tr><td>
Ablauf

</td><td colspan="2">
Der VZD liefert die Metadaten der Schnittstelle in der Datenstruktur InfoObject
zurück.

</td></tr><tr><td>
Fehlerfälle

</td><td colspan="2">
Es werden die protokollspezifischen Fehlermeldungen verwendet (TCP, HTTP, TLS)
und in DirectoryAdministration.yaml mit spezifischen Fehlerbeschreibungen
ergänzt.

</td></tr></table>

**[\<=]**

**A_21789 - VZD, Umsetzung I_Directory_Administration (REST)**

Der VZD MUSS nach folgenden Vorgaben die Operation implementieren:In den
Rückgabewerten müssen die aktuell gültigen Metainformationen für
Schnittstelle I_Directory_Administration zurückgegeben werden. Insbesondere
muss

 ---> OL **[\<=]**

### 4.6.1.2 DirectoryEntry Administration

Die Pflege der Basiseinträge (Verzeichnisdienst_Eintrag) erfolgt mit den im
Folgenden beschriebenen Operationen.

### 4.6.1.2.1 POST

Diese Operation legt einen neuen Eintrag im LDAP-Verzeichnis an.

**A_18448 - VZD, I_Directory_Administration, add_Directory_Entry**

Der VZD MUSS Operation „add_Directory_Entry” gemäß Tabelle Tab_VZD
„add_Directory_Entry” umsetzen.

Tabelle24: Tab_VZD „add_Directory_Entry”

<table><tr><td>
Name

</td><td colspan="2">
add_Directory_Entry

</td></tr><tr><td>
Beschreibung

</td><td colspan="2">
Diese Operation ermöglicht die Erzeugung eines neuen Eintrags im
LDAP-Verzeichnis.

</td></tr><tr><td rowspan="4">
Eingangsdaten

</td><td colspan="2">
REST-Request POST /DirectoryEntries  
operationId: add_Directory_Entry (siehe
DirectoryAdministration.yaml)

</td></tr><tr><td>
Parameter

</td><td>
Beschreibung

</td></tr><tr><td>
Verzeichnisdienst_Eintrag

</td><td>
Siehe Abb_VZD_logisches_Datenmodell und Tab_VZD_Datenbeschreibung.  
Der
Distinguished Name wird vom VZD belegt.  
Der VZD übernimmt entsprechend
Tab_VZD_Datenbeschreibung eine Reihe von Attributen aus dem Zertifikat.

</td></tr><tr><td>
Certificate

</td><td>
Kann optional belegt werden.  
Siehe Abb_VZD_logisches_Datenmodell und
Tab_VZD_Datenbeschreibung.  
Der Distinguished Name wird vom VZD belegt.  
Der
VZD übernimmt entsprechend Tab_VZD_Datenbeschreibung eine Reihe von Attributen
aus dem Zertifikat.

</td></tr><tr><td>
Komponenten

</td><td colspan="2">
Nutzer der Schnittstelle, Verzeichnisdienst

</td></tr><tr><td>
Ausgangsdaten

</td><td colspan="2">
REST-Response mit dem Distinguished Name (dn) von dem Verzeichnisdienst_Eintrag.

</td></tr><tr><td>
Ablauf

</td><td colspan="2">
Der VZD übernimmt entsprechend Tab_VZD_Datenbeschreibung Attribute aus dem
Zertifikat und trägt die übergebenen Parameter in den Verzeichniseintrag ein.
 
Der VZD setzt das  LDAP-Directory-Attribut dataFromAuthority auf den Wert
TRUE.

</td></tr><tr><td>
Fehlerfälle

</td><td colspan="2">
Es werden die protokollspezifischen Fehlermeldungen verwendet (TCP, HTTP, TLS)
und in DirectoryAdministration.yaml mit spezifischen Fehlerbeschreibungen
ergänzt.

</td></tr></table>

   **[\<=]**

**A_20271-01 - VZD, I_Directory_Administration, add_Directory_Entry, holder
setzen**

Der VZD MUSS bei Operation „add_Directory_Entry” den Eigentümer des
erzeugten Verzeichniseintrags im Attribut"holder" entsprechend folgenden
Vorgaben setzen: 

 ---> UL

**[\<=]**

Das Attribut "holder" wirkt für die Modifikationen der Basisdaten (die Prüfung
des Attributs erfolgt nur für Operation modify_Directory_Entry), nicht auf
Änderungen der Zertifikats- oder Fachdaten.

**A_21791-01 - VZD, Prüfung auf Typ der Zertifikate**

Der VZD MUSS beim Hinzufügen von Zertifikaten mit den Operationen
„add_Directory_Entry” und "add_Directory_Entry_Certificate" den Typ der
Zertifikate prüfen. Der VZD MUSS alle Operationen mit Zertifikaten ablehnen,
die nicht vom Zertifikatstyp C.HCI.ENC oder C.HP.ENC (siehe
[gemSpec_OID#Tab_PKI_405-01] sind oder nicht keyUsage = (!digitalSignature &&
keyEncipherment && dataEncipherment) (siehe [gemSpec_PKI]} GS-A_5532-01)
gesetzt ist. Im Falle von unzulässigen Zertifikaten MUSS der VZD mit
HTTP-Statuscode 422
(attributeName="userCertificate", attributeError="erläuternder Fehlertext")
antworten und darf die gesamte Operation nicht ausführen. **[\<=]**

**A_21790-01 - VZD, Prüfung auf Gültigkeit der Zertifikate in der korrekten
PKI-Umgebung**

Der VZD MUSS beim Hinzufügen von Zertifikaten in der PKI-Umgebung PU mit den
Operationen „add_Directory_Entry” und "add_Directory_Entry_Certificate" die
Gültigkeit der Zertifikate für diese PKI-Umgebung (PU) prüfen (TUC_PKI_018
mit erfolgreichem Status der Prüfung mit
Prüfparametern Offline-Modus=nein; Prüfmodus=OCSP;
TOLERATE_OCSP_FAILURE=false). Die Gültigkeit wird anhand der CA und Prüfung
gegen PU-TSL durchgeführt. In der PKI-Umgebung PU dürfen nur die Zertifikate
akzeptiert werden, die in dieser Umgebung gültig sind. Gültige Zertifikate
aus anderen Umgebungen müssen abgelehnt werden. In den PKI-Testumgebungen (RU,
TU) erfolgt keine Prüfung. **[\<=]**

**A_21824 - VZD, I_Directory_Administration, stateOrProvinceName Prüfung**

Der VZD MUSS vor Ausführung der Operationen „add_Directory_Entry” und
"modify_Directory_Entry"den Inhalt von Parameter stateOrProvinceName des
Operation Requests gegen die gültigen Werte entsprechend
[gemILF_Pflege_VZD#Tabelle TAB_VZD_Wertebereiche_der_Attribute] prüfen, wenn
es sich um eine deutsche Adresse handelt (countryCode = DE). Im Falle von
ungültigen Werten MUSS der VZD mit HTTP-Statuscode 422
(attributeName="stateOrProvinceName" , attributeError="erläuternder
Fehlertext") antworten und darf die Operation nicht ausführen. **[\<=]**

### 4.6.1.2.2 GET

Diese Operation liest Verzeichniseinträge aus dem LDAP-Verzeichnis.

**A_18449-03 - VZD, I_Directory_Administration, read_Directory_Entry**

Der VZD MUSS Operation „read_Directory_Entry” gemäß Tabelle Tab_VZD
„read_Directory_Entry” umsetzen.

<table><tr><td>
Name

</td><td colspan="2">
read_Directory_Entry

</td></tr><tr><td>
Beschreibung

</td><td colspan="2">
Diese Operation ermöglicht die Suche und Lesen von Verzeichniseinträgen im
LDAP-Verzeichnis.  
Diese Operation liefert auch Einträge, die ohne gültige
Zertifikate sind.

</td></tr><tr><td rowspan="3">
Eingangsdaten

</td><td colspan="2">
REST-Request GET /DirectoryEntries  
operationId: read_Directory_Entry (siehe
DirectoryAdministration.yaml)

</td></tr><tr><td>
Parameter

</td><td>
Beschreibung

</td></tr><tr><td>
Parameter zur Selektion der Verzeichniseinträge

</td><td>
Alle im Datenmodell aufgeführten Felder des Basiseintrags - insbesondere auch
dataFromAuthority - können zur Suche genutzt werden.  
Die angegebenen
Parameter werden zur Suche mit einem logischen UND verknüpft.

</td></tr><tr><td>
Komponenten

</td><td colspan="2">
Nutzer der Schnittstelle, Verzeichnisdienst

</td></tr><tr><td>
Ausgangsdaten

</td><td colspan="2">
REST-Response mit allen zu den Filterparametern passenden Verzeichniseinträgen.
Die Verzeichniseinträge werden optional inklusive Zertifikatseinträgen und
Fachdaten geliefert.

</td></tr><tr><td>
Ablauf

</td><td colspan="2">
Der VZD sucht im LDAP-Verzeichnis die zu den Suchparametern passenden
Verzeichniseinträge.  
Bei mehr als 100 gefundenen Einträgen werden nur 100
gefundenen Einträge zurückgegeben.

</td></tr><tr><td>
Fehlerfälle

</td><td colspan="2">
Es werden die protokollspezifischen Fehlermeldungen verwendet (TCP, HTTP, TLS)
und in DirectoryAdministration.yaml mit spezifischen Fehlerbeschreibungen
ergänzt.

</td></tr></table>

**[\<=]**

### 4.6.1.2.3 PUT

Diese Operation aktualisiert den Verzeichniseintrag (ohne Zertifikate und
Fachdaten) mit den übergebenen Daten im LDAP-Verzeichnis.

**A_18450-03 - VZD, I_Directory_Administration, modify_Directory_Entry**

Der VZD MUSS Operation „modify_Directory_Entry” gemäß Tabelle Tab_VZD
„modify_Directory_Entry” umsetzen.

Tabelle26: Tab_VZD „modify_Directory_Entry”

<table><tr><td>
Name

</td><td colspan="2">
modify_Directory_Entry

</td></tr><tr><td>
Beschreibung

</td><td colspan="2">
Diese Operation ermöglicht die Aktualisierung von Verzeichniseinträgen im
LDAP-Verzeichnis.

</td></tr><tr><td rowspan="15">
Eingangsdaten

</td><td colspan="2">
REST-Request PUT /DirectoryEntries/{uid}/baseDirectoryEntries  
operationId:
modify_Directory_Entry (siehe DirectoryAdministration.yaml)

</td></tr><tr><td>
Parameter

</td><td>
Beschreibung

</td></tr><tr><td>
uid

</td><td>
Die „uid“ identifiziert den Verzeichnisdienst_Eintrag
(Abb_VZD_logisches_Datenmodell) welcher aktualisiert wird.

</td></tr><tr><td>
displayName

</td><td>
Kann optional angegeben werden und überschreibt den Wert im selektierten
Verzeichniseintrag.

</td></tr><tr><td>
otherName

</td><td>
Kann optional angegeben werden und überschreibt den Wert im selektierten
Verzeichniseintrag.

</td></tr><tr><td>
streetAddress

</td><td>
Kann optional angegeben werden und überschreibt den Wert im selektierten
Verzeichniseintrag.

</td></tr><tr><td>
postalCode

</td><td>
Kann optional angegeben werden und überschreibt den Wert im selektierten
Verzeichniseintrag.

</td></tr><tr><td>
localityName

</td><td>
Kann optional angegeben werden und überschreibt den Wert im selektierten
Verzeichniseintrag.

</td></tr><tr><td>
stateOrProvienceName

</td><td>
Kann optional angegeben werden und überschreibt den Wert im selektierten
Verzeichniseintrag.

</td></tr><tr><td>
title

</td><td>
Kann optional angegeben werden und überschreibt den Wert im selektierten
Verzeichniseintrag.

</td></tr><tr><td>
organization

</td><td>
Kann optional angegeben werden und überschreibt den Wert im selektierten
Verzeichniseintrag.

</td></tr><tr><td>
specialization

</td><td>
Kann optional angegeben werden und überschreibt den Wert im selektierten
Verzeichniseintrag.

</td></tr><tr><td>
domainID

</td><td>
Kann optional angegeben werden und überschreibt den Wert im selektierten
Verzeichniseintrag.

</td></tr><tr><td>
holder

</td><td>
Kann optional angegeben werden.

Durch setzen des "holder" kann ein Verzeichniseintrag an einen anderen
Eigentümer weitergegeben werden. Die Weitergabe kann nur durch den aktuellen
Eigentümer/holder erfolgen.

</td></tr><tr><td>
maxKOMLEadr

</td><td>
Kann optional angegeben werden.

Durch setzen von "maxKOMLEadr" wird die maximale Anzahl von mail Adressen in den
KOM-LE Fachdaten festgelegt. 

</td></tr><tr><td>
Komponenten

</td><td colspan="2">
Nutzer der Schnittstelle, Verzeichnisdienst

</td></tr><tr><td>
Ausgangsdaten

</td><td colspan="2">
REST-Response mit dem Distinguished Name (dn) von dem aktualisierten
Verzeichnisdienst_Eintrag.

</td></tr><tr><td>
Ablauf

</td><td colspan="2">
Der VZD aktualisiert im LDAP-Verzeichnis den über Parameter „uid“
identifizierten Verzeichniseintrag mit den übergebenen Parametern.  
Der VZD
setzt das  LDAP-Directory-Attribut dataFromAuthority auf den Wert TRUE.

</td></tr><tr><td>
Fehlerfälle

</td><td colspan="2">
Es werden die protokollspezifischen Fehlermeldungen verwendet (TCP, HTTP, TLS)
und in DirectoryAdministration.yaml mit spezifischen Fehlerbeschreibungen
ergänzt.

</td></tr></table>

**[\<=]**

**A_20272-02 - VZD, I_Directory_Administration, modify_Directory_Entry,
Zugriffsrechte**

Der VZD MUSS bei Operation „modify_Directory_Entry” für den - über
Parameter uid adressierten - Verzeichniseintrag das Attribut"holder" im
gespeicherten Verzeichniseintrag und die aktuellen Parameter ("holder" und
ACCESS_TOKEN claim scope) der Operation „modify_Directory_Entry” prüfen:

 ---> UL

 ---> UL

 ---> UL

**[\<=]**

**A_21823 - VZD, I_Directory_Administration, modify_Directory_Entry, Limit
maxKOMLEadr**

Der VZD MUSS bei Operation „modify_Directory_Entry” nach erfolgreicher
Aktualisierung des VZD-Datensatzes die Anzahl der hinterlegten Mail-Adressen in
den KOM-LE Fachdaten mit dem Wert von Attribut maxKOMLEadr vergleichen. Die
Anzahl der hinterlegten mail Adressen in den KOM-LE Fachdaten, die den Wert
von Attribut maxKOMLEadr übersteigen, MUSS der VZD im Responde der Operation
im Header X-maxKOMLEadr-Limit zurückgeben. **[\<=]**

Beispiele

                    a) maxKOMLEadr (nach Ausführung des Updates) = 1

                       hinterlegte Mail-Adressen in den
KOM-LE-Fachdaten = 1                       Header im Response:

X-maxKOMLEadr-Limit: 0

                    b) maxKOMLEadr (nach Ausführung des Updates) = 1

                       hinterlegte Mail-Adressen in den
KOM-LE-Fachdaten = 3                       Header im Response:

X-maxKOMLEadr-Limit: 2

### 4.6.1.2.4 DELETE

Diese Operation löscht den gesamten Verzeichniseintrag (inklusive Zertifikaten
und Fachdaten).

**A_18451 - VZD, I_Directory_Administration, delete_Directory_Entry**

Der VZD MUSS Operation „delete_Directory_Entry” gemäß Tabelle Tab_VZD
„delete_Directory_Entry” umsetzen.

Name  
         delete_Directory_Entry  
        
        
         Beschreibung
 
         Diese Operation ermöglicht die Löschung von kompletten
Verzeichniseinträgen (inklusive Zertifikaten und Fachdaten)  im
LDAP-Verzeichnis.  
        
        
         Eingangsdaten  
        
REST-Request DELETE /DirectoryEntries/{uid}  
operationId:
delete_Directory_Entry (siehe DirectoryAdministration.yaml)  
        
       

         Parameter  
         Beschreibung  
        
        
         uid  

        Die „uid“ identifiziert den Verzeichnisdienst_Eintrag
(Abb_VZD_logisches_Datenmodell) welcher inklusive der dazu gehörenden
Zertifikate und Fachdaten gelöscht wird.  
        
        
        
Komponenten  
         Nutzer der Schnittstelle, Verzeichnisdienst  
        
 
      
         Ausgangsdaten  
         REST-Response.  
        
        
   
     Ablauf  
         Der VZD löscht im LDAP-Verzeichnis den über Parameter
„uid“ identifizierten Verzeichniseintrag inklusive der dazu gehörenden
Zertifikate und Fachdaten.  
        
        
         Fehlerfälle  
        
Es werden die protokollspezifischen Fehlermeldungen verwendet (TCP, HTTP, TLS)
und in DirectoryAdministration.yaml mit spezifischen Fehlerbeschreibungen
ergänzt. **[\<=]**

**A_20273-01 - VZD, I_Directory_Administration, delete_Directory_Entry,
Zugriffsrechte**

Der VZD MUSS bei Operation „delete_Directory_Entry” für den - über
Parameter uid adressierten - Verzeichniseintrag das Attribut"holder" im
gespeicherten Verzeichniseintrag gegen die aktuellen Parameter der Operation
„delete_Directory_Entry” prüfen:

 ---> UL

**[\<=]**

### 4.6.1.3 Certificate Administration

Die Pflege der Zertifikatseinträge (Certificate in
Abb_VZD_logisches_Datenmodell) erfolgt mit den im Folgenden beschriebenen
Operationen.

### 4.6.1.3.1 POST

Diese Operation fügt einem existierenden Basisdatensatz einen
Zertifikatseintrag im LDAP-Verzeichnis an.

**A_18452 - VZD, I_Directory_Administration, add_Directory_Entry_Certificate**

Der VZD MUSS Operation „add_Directory_Entry_Certificate” gemäß Tabelle
Tab_VZD „add_Directory_Entry_Certificate” umsetzen.

Name  
         add_Directory_Entry_Certificate  
        
        
        
Beschreibung  
         Diese Operation fügt einem existierenden
Basisdatensatz einen Zertifikatseintrag im LDAP-Verzeichnis an.  
        
    
   
         Eingangsdaten  
         REST-Request POST
/DirectoryEntries/{uid}/Certificates  
operationId:
add_Directory_Entry_Certificate (siehe DirectoryAdministration.yaml)  
       

        
         Parameter  
         Beschreibung  
        
        
      
  uid  
         Die „uid“ identifiziert den Verzeichnisdienst_Eintrag
(Abb_VZD_logisches_Datenmodell) an welchen der Zertifikatseintrag angehangen
wird.  
        
        
         userCertificate  
         Muss angegeben
werden und enthält das Zertifikat.  
        
        
         usage  
      
  Kann optional belegt werden.  
        
        
         description  
     
   Kann optional belegt werden.  
        
        
         Komponenten  
    
    Nutzer der Schnittstelle, Verzeichnisdienst  
        
        
        
Ausgangsdaten  
         REST-Response mit dem Distinguished Name (dn) von dem
erzeugten Certificate-Eintrag.  
        
        
         Ablauf  
        
Der VZD übernimmt entsprechend Tab_VZD_Datenbeschreibung Attribute aus dem
Zertifikat und trägt die übergebenen Parameter in den Zertifikatseintrag ein.
Der Distinguished Name (dn) von dem erzeugten Certificate wird vom
Verzeichnisdienst gefüllt und über dn.uid mit dem übergeordneten
Verzeichnisdienst_Eintrag verknüpft.  
        
        
         Fehlerfälle
 
         Es werden die protokollspezifischen Fehlermeldungen verwendet (TCP,
HTTP, TLS) und in DirectoryAdministration.yaml mit spezifischen
Fehlerbeschreibungen ergänzt.

  **[\<=]**

### 4.6.1.3.2 GET

Diese Operation liest Zertifikatseinträge aus dem LDAP-Verzeichnis.

**A_18453-01 - VZD, I_Directory_Administration, read_Directory_Certificates**

Der VZD MUSS Operation „read_Directory_Certificates” gemäß Tabelle Tab_VZD
„read_Directory_Certificates” umsetzen.

Tabelle29: Tab_VZD „read_Directory_Certificates”

<table><tr><td>
Name

</td><td colspan="2">
read_Directory_Certificates

</td></tr><tr><td>
Beschreibung

</td><td colspan="2">
Diese Operation ermöglicht die Suche und das Lesen von Zertifikatseinträgen
(Certificate in Abb_VZD_logisches_Datenmodell) im LDAP-Verzeichnis.

</td></tr><tr><td rowspan="5">
Eingangsdaten

</td><td colspan="2">
REST-Request GET /DirectoryEntries/Certificates  
operationId:
read_Directory_Certificates (siehe DirectoryAdministration.yaml)  
Mindestens
ein Filterparameter muss angegeben werden.

</td></tr><tr><td>
Parameter

</td><td>
Beschreibung

</td></tr><tr><td>
uid

</td><td>
Optionaler Parameter.  
Die „uid“ identifiziert einen
Verzeichnisdienst_Eintrag (Abb_VZD_logisches_Datenmodell). Dieser Parameter
selektiert alle Zertifikatseinträge dieses Verzeichnisdiensteintrags.

</td></tr><tr><td>
certificateEntryID

</td><td>
Optionaler Parameter.  
Dieser Parameter identifiziert einen Zertifikatseintrag
(Abb_VZD_logisches_Datenmodell dn.cn von Certificate).

</td></tr><tr><td>
telematikID

</td><td>
Optionaler Parameter.  
Dieser Parameter selektiert alle Zertifikatseinträge
mit dieser TeleamtikID.

</td></tr><tr><td>
Komponenten

</td><td colspan="2">
Nutzer der Schnittstelle, Verzeichnisdienst

</td></tr><tr><td>
Ausgangsdaten

</td><td colspan="2">
REST-Response mit allen zu den Filter Parametern passenden Zertifikatseinträgen.

</td></tr><tr><td>
Ablauf

</td><td colspan="2">
Der VZD sucht im LDAP Verzeichnis die zu den Such-Parametern passenden
Zertifikatseinträge.  
Bei mehr als 100 gefundenen Einträgen werden nur 100
gefundenen Einträge zurückgegeben.

</td></tr><tr><td>
Fehlerfälle

</td><td colspan="2">
Es werden die protokollspezifischen Fehlermeldungen verwendet (TCP, HTTP, TLS)
und in DirectoryAdministration.yaml mit spezifischen Fehlerbeschreibungen
ergänzt.

</td></tr></table>

  **[\<=]**

### 4.6.1.3.3 DELETE

Diese Operation löscht einen Zertifikatseintrag.

**A_18455 - VZD, I_Directory_Administration, delete_Directory_Entry_Certificate**

Der VZD MUSS Operation „delete_Directory_Entry_Certificate” gemäß Tabelle
Tab_VZD „delete_Directory_Entry_Certificate” umsetzen.

<table><tr><td>
Name

</td><td colspan="2">
delete_Directory_Entry_Certificate

</td></tr><tr><td>
Beschreibung

</td><td colspan="2">
Diese Operation ermöglicht die Löschung eines Zertifikatsseintrags  im
LDAP-Verzeichnis.

</td></tr><tr><td rowspan="4">
Eingangsdaten

</td><td colspan="2">
REST-Request

                  DELETE
/DirectoryEntries/{uid}/Certificates/{certificateEntryID}

 

operationId: delete_Directory_Entry_Certificate (siehe
DirectoryAdministration.yaml)

</td></tr><tr><td>
Parameter

</td><td>
Beschreibung

</td></tr><tr><td>
uid

</td><td>
Pflichtparameter.

Die „uid“ identifiziert den Verzeichnisdienst_Eintrag
(Abb_VZD_logisches_Datenmodell) zu dem der Zertifikatseintrag gehört.

</td></tr><tr><td>
certificateEntryID

</td><td>
Pflichtparameter.

Dieser Parameter identifiziert einen Zertifikatseintrag
(Abb_VZD_logisches_Datenmodell dn.cn von Certificate).

</td></tr><tr><td>
Komponenten

</td><td colspan="2">
Nutzer der Schnittstelle, Verzeichnisdienst

</td></tr><tr><td>
Ausgangsdaten

</td><td colspan="2">
REST-Response.

</td></tr><tr><td>
Ablauf

</td><td colspan="2">
Der VZD löscht im LDAP-Verzeichnis den über die Parameter „uid“ und
„certificateEntryID“ identifizierten Zertifikatseintrag.

</td></tr><tr><td>
Fehlerfälle

</td><td colspan="2">
Es werden die protokollspezifischen Fehlermeldungen verwendet (TCP, HTTP, TLS)
und in DirectoryAdministration.yaml mit spezifischen Fehlerbeschreibungen
ergänzt.

</td></tr></table>

   **[\<=]**

### 4.6.1.4 DirectoryEntry Synchronization

Zur Unterstützung der Pflege der Basiseinträge (Verzeichnisdienst_Eintrag)
wird die hier beschriebene Operation zur Verfügung gestellt. Sie dient der
Synchronisation mit dem Datenbestand des Verzeichnisdienstes und erlaubt – im
Gegensatz zur Operation „read_Directory_Entry” – das Lesen beliebig
vieler eigener Verzeichniseinträge.

### 4.6.1.4.1 GET

**A_21230-03 - VZD, I_Directory_Administration, read_Directory_Entry_for_Sync**

Der VZD MUSS Operation „read_Directory_Entry_for_Sync” gemäß Tabelle
Tab_VZD „read_Directory_Entry_for_Sync” umsetzen.

<table><tr><td>
Name

</td><td colspan="2">
read_Directory_Entry_for_Sync

</td></tr><tr><td>
Beschreibung

</td><td colspan="2">
Diese Operation ermöglicht die Suche und Lesen von Verzeichniseinträgen im
LDAP-Verzeichnis.  
Diese Operation liefert auch Einträge, die ohne gültige
Zertifikate sind.

</td></tr><tr><td rowspan="3">
Eingangsdaten

</td><td colspan="2">
REST-Request GET /DirectoryEntries  
operationId: read_Directory_Entry (siehe
DirectoryAdministration.yaml)

</td></tr><tr><td>
Parameter

</td><td>
Beschreibung

</td></tr><tr><td>
Parameter zur Selektion der Verzeichniseinträge

</td><td>
Alle im Datenmodell aufgeführten Felder des Basiseintrags - insbesondere auch
dataFromAuthority - können zur Suche genutzt werden.  
Die angegebenen
Parameter werden zur Suche mit einem logischen UND verknüpft.

</td></tr><tr><td>
Komponenten

</td><td colspan="2">
Nutzer der Schnittstelle, Verzeichnisdienst

</td></tr><tr><td>
Ausgangsdaten

</td><td colspan="2">
REST-Response mit allen zu den Filterparametern passenden Verzeichniseinträgen.
Die Verzeichniseinträge werden optional inklusive Zertifikatseinträgen und
Fachdaten geliefert.

</td></tr><tr><td>
Ablauf

</td><td colspan="2">
Der VZD sucht im LDAP-Verzeichnis die zu den Suchparametern passenden
Verzeichniseinträge.  
Bei mehr als 100 gefundenen Einträgen werden nur 100
gefundene Einträge zurückgegeben.  
Wenn über den "holder"-Suchparameter
nach eigenen Verzeichniseinträgen oder Verzeichniseinträgen ohne gesetztes
"holder"-Attribut gesucht wird, MÜSSEN vom VZD über den Paging Mechanismus
(entsprechend RFC2696 und Definition in DirectoryAdministration.yaml) alle
Suchergebnisse - ohne Beschränkung auf 100 Einträge - zurückgegeben werden.

</td></tr><tr><td>
Fehlerfälle

</td><td colspan="2">
Es werden die protokollspezifischen Fehlermeldungen verwendet (TCP, HTTP, TLS)
und in DirectoryAdministration.yaml mit spezifischen Fehlerbeschreibungen
ergänzt.

</td></tr></table>

**[\<=]**

**A_20402-02 - VZD, I_Directory_Administration, read_Directory_Entry_for_Sync,
Paging, Berechtigung**

Der VZD MUSS für den Paging Mechanismus von Operation
„read_Directory_Entry_for_Sync” sicherstellen:

 ---> UL

Bei Abweichungen von diesen Festlegungen MUSS der VZD mit einem Fehler
(HTTP-Status-Code 403) antworten. **[\<=]**

### 4.6.2 Nutzung der Schnittstelle I_Directory_Administration

Der Client der Schnittstelle I_Directory_Administration muss eine TLS-Verbindung
mit serverseitiger Authentisierung nutzen. Dabei muss er das Serverzertifikat
des VZD prüfen. Bei negativem Ergebnis muss der Verbindungsaufbau abgebrochen
werden.

Mit Hilfe der Operationen der Schnittstelle muss der Client die
Verzeichniseinträge eintragen und pflegen.

Beispielablauf:

Falls die „uid“ des Verzeichniseintrags nicht bekannt ist erfolgt die Suche
nach einem vorhandenen Verzeichniseintrag mit der telematikID (operationId
read_Directory_Certificates mit Parameter telematikID)

a.    Falls ein Eintrag gefunden wurde:

1.    Lesen des Basis-Verzeichniseintrags (operationId read_Directory_Entry
mit Parameter „uid“ aus dem read_Directory_Certificates Response)

2.    Aktualisieren des Verzeichniseintrags und (je nach Bedarf) der
dazugehörigen Zertifikatseinträge (operationId‘s: modify_Directory_Entry,
delete_Directory_Entry, modify_Directory_Entry_Certificate,
delete_Directory_Entry_Certificate)

b.    Falls kein Eintrag gefunden wurde:

1.    Erzeugen des Verzeichniseintrags und (je nach Bedarf) anhängen
zusätzlicher Zertifikatseinträge (operationId‘s: add_Directory_Entry,
add_Directory_Entry_Certificate). Der erste Zertifikatseintrag wird mit
Operation add_Directory_Entry erzeugt da jeder Verzeichniseintrag mindestens
einen Zertifikatseintrag enthalten muss. Zusätzliche Zertifikatseinträge
können mit Operation add_Directory_Entry_Certificate hinzugefügt werden.

### 5 Datenmodell

**TIP1-A_5607-06 - VZD, logisches Datenmodell**

Der VZD MUSS das logische Datenmodell nach Abb_VZD_logisches_Datenmodell und
Tab_VZD_Datenbeschreibung implementieren. Es wird keine Vorgabe an die
technische Ausprägung des Datenmodells gemacht.Der VZD MUSS sicherstellen,
dass ein Eintrag nur Zertifikate aus dem Vertrauensraum der TI mit gleicher
Telematik-ID enthält.![Img-002][Img-002]

Abbildung2: Abb_VZD_logisches_Datenmodell

Tabelle32: Tab_VZD_Datenbeschreibung

<table><tr><th>
LDAP-Directory Attribut

</th><th>
Pflichtfeld?

</th><th>
Erläuterung

</th></tr><tr><td>
givenName

</td><td>
optional

</td><td>
HBA-Eintrag: Bezeichner: Vorname, wird vom VZD aus dem Zertifikat übernommen.
 
SMC-B-Eintrag: wird nicht verwendet

</td></tr><tr><td>
sn

</td><td>
optional

</td><td>
HBA-Eintrag: Bezeichner: Name, wird vom VZD aus dem Zertifikat übernommen 

SMC-B Eintrag: Wird vom VZD als Kopie des Attributs displayName übernommen.

</td></tr><tr><td>
cn

</td><td>
obligatorisch

</td><td>
HBA: Eintrag: Bezeichner: Nachname, Vorname  
SMC-B Eintrag: Bezeichner: Name 

Wird vom VZD unabhängig vom Kartentyp als Kopie des Attributs displayName
übernommen.  
Wird von E-Mail Clients für die Suche nach Einträgen und die
Anzeige von gefundenen Einträgen verwendet

</td></tr><tr><td>
displayName

</td><td>
optional

</td><td>
Bezeichner: Anzeigename, Name nach dem der Eintrag von Nutzern gesucht wird und
unter dem gefundene Einträge angezeigt werden.  
Konvention für HBA
Einträge: Name, Vorname

</td></tr><tr><td>
streetAddress

</td><td>
optional

</td><td>
Bezeichner: Straße und Hausnummer  
Alias: street (wird vom VZD in der Response
zu einer LDAP Query verwendet)

</td></tr><tr><td>
postalCode

</td><td>
optional

</td><td>
Bezeichner: Postleitzahl

</td></tr><tr><td>
countryCode

</td><td>
obligatorisch

</td><td>
Kann beim Anlegen des Datensatzes und beim Ändern gesetzt werden (falls nicht
gesetzt, ergänzt der VZD den Defaultwert für Deutschland).

</td></tr><tr><td>
localityName 

</td><td>
optional

</td><td>
Bezeichner: Ort  
Alias: l (wird vom VZD in der Response zu einer LDAP Query
verwendet)

</td></tr><tr><td>
stateOrProvinceName 

</td><td>
optional

</td><td>
Bezeichner: Bundesland oder Region  
Alias: st (wird vom VZD in der Response
zu einer LDAP Query verwendet)

</td></tr><tr><td>
title

</td><td>
optional

</td><td>
HBA: Bezeichner: Titel  
SMC-B: nicht verwendet

</td></tr><tr><td>
organization

</td><td>
optional

</td><td>
HBA: Bezeichner: Name der Organisation oder Name der Betriebsstätte  
SMC-B:
Alternativer Name nach dem der Eintrag von Nutzern gesucht wird und unter dem
gefundene Einträge angezeigt werden

</td></tr><tr><td>
otherName

</td><td>
optional

</td><td>
Bezeichner: Anderer Name  
Veraltet: Wird für die Suche nach Einträgen und
die Anzeige von gefundenen Einträgen nicht benötigt (siehe displayName und
organization)

</td></tr><tr><td>
specialization

</td><td>
optional

</td><td>
Bezeichner: Fachgebiet  
Kann mehrfach vorkommen (1..100).  
Für Einträge der
Leistungserbringerorganisationen (SMC-B Eintrag)  
Der Wertebereich
entspricht den in hl7 definierten und für ePA festgelegten Werten
(https://wiki.hl7.de/index.php?title=IG:Value_Sets_f%C3%BCr_XDS#DocumentEntry.practiceSettingCode).
 
urn:psc:\<OID Codesystem:Code\>

Beispiel für Allgemeinmedizin: urn:psc:1.3.6.1.4.1.19376.3.276.1.5.4:ALLG 

Beispiel für Zahnmedizin: urn:psc:1.3.6.1.4.1.19376.3.276.1.5.4:MKZH 

Beispiel für Apotheke: urn:psc:1.3.6.1.4.1.19376.3.276.1.5.5:PHZ  
Beispiel
für Krankenhaus: urn:psc:1.3.6.1.4.1.19376.3.276.1.5.4:GESU  
  
Für
Einträge der Leistungserbringer (HBA-Eintrag)  
 Der Wertebereich entspricht
den in hl7 definierten Werten
(https://wiki.hl7.de/index.php?title=IG:Value_Sets_f%C3%BCr_XDS#DocumentEntry.authorSpecialty).
 
urn:as:\<OID Codesystem:Code\>

Psychologischer Psychotherapeut: urn:as:1.3.6.1.4.1.19376.3.276.1.5.11:82 

Psychotherapeut: urn:as:1.3.6.1.4.1.19376.3.276.1.5.11:183  

Fachpsychotherapeut für Kinder und Jugendliche:
urn:as:1.3.6.1.4.1.19376.3.276.1.5.11:184   
Fachpsychotherapeut für
Erwachsene: urn:as:1.3.6.1.4.1.19376.3.276.1.5.11:185  
Beispiel für FA
Allgemeinmedizin: urn:as:1.2.276.0.76.5.514:011001  
Beispiel für Zahnarzt:
urn:as:1.2.276.0.76.5.492:1

</td></tr><tr><td>
domainID

</td><td>
optional

</td><td>
Bezeichner: domänenspezifisches Kennzeichen des Eintrags.  
kann mehrfach
vorkommen (0..100)

</td></tr><tr><td>
holder

</td><td>
optional

</td><td>
Legt fest, wer Änderungen an den Basisdaten des Eintrags vornehmen darf. Hat
keinen Einfluss auf Fachdaten und Zertifikatsdaten.

</td></tr><tr><td>
maxKOMLEadr

</td><td>
optional

</td><td>
Maximale Anzahl von mail Adressen in den KOM-LE-Fachdaten. 

Falls kein Wert eingetragen wurde, können beliebig viele mail Adressen in den
KOM-LE Fachdaten eingetragen werden.

Falls ein Wert eingetragen wurde, können maximal so viele mail Adressen in den
KOM-LE Fachdaten eingetragen werden.

</td></tr><tr><td>
personalEntry

</td><td>
obligatorisch

</td><td>
Wird vom VZD eingetragen  
Wert == TRUE, wenn alle Zertifikate den entryType 1
haben (Berufsgruppe), Wert == FALSE sonst

</td></tr><tr><td>
dataFromAuthority

</td><td>
optional

</td><td>
wird vom VZD eingetragen  
Wert == TRUE, wenn der Verzeichnisdienst_Eintrag von
dem Kartenherausgeber geschrieben wurde, Wert == FALSE sonst

</td></tr><tr><td>
userCertificate

</td><td>
optional

</td><td>
Bezeichner: Enc-Zertifikat  
kann mehrfach vorkommen (0..50)  
Das Zertifikat
wird gelöscht, wenn es ungültig geworden ist. Wenn kein Zertifikat vorliegt,
dann kann der Eintrag nicht mittels LDAP-Abfrage gefunden werden.  
Format:
DER, Base64-kodiert

</td></tr><tr><td>
entryType

</td><td>
optional

</td><td>
Bezeichner: Eintragstyp  
Wird vom VZD anhand der im Zertifikat enthaltenen OID
(Extension Admission, Attribut ProfessionOID) und der Spalte Eintragstyp
in Tab_VZD_Mapping_Eintragstyp_und_ProfessionOID automatisch eingetragen.
Siehe auch [gemSpecOID]# Tab_PKI_402 und Tab_PKI_403.

</td></tr><tr><td>
telematikID

</td><td>
obligatorisch

</td><td>
Bezeichner: TelematikID  
Wird vom VZD anhand der im jeweiligen Zertifikat
enthaltenen Telematik-ID (Feld registrationNumber der Extension Admission)
übernommen.  
Ist in den Basisdaten und in den Zertifikatsdaten enthalten.

</td></tr><tr><td>
professionOID

</td><td>
optional

</td><td>
Bezeichner: Profession OID  
Wird vom VZD anhand der im Zertifikat enthaltenen
OID (Extension Admission, Attribut ProfessionOID) und dem Mapping in
Tab_VZD_Mapping_Eintragstyp_und_ProfessionOID automatisch eingetragen. Siehe
[gemSpecOID#Tab_PKI_402 und Tab_PKI_403].  
kann mehrfach vorkommen (0..100)

</td></tr><tr><td>
usage

</td><td>
optional

</td><td>
Bezeichner: Nutzungskennzeichnung  
kann pro Zertifikat mehrfach (0..100)
vergeben werden  
Hinweis: wird nicht verwendet.

</td></tr><tr><td>
description

</td><td>
optional

</td><td>
Bezeichner: Beschreibung  
Dieses Attribut ermöglicht das Zertifikat zu
beschreiben, um die Administration des VZD-Eintrags zu vereinfachen.  
Hinweis:
wird aktuell nicht verwendet.

</td></tr><tr><td>
mail

</td><td>
optional

</td><td>
Bezeichner: KOM-LE E-Mail-Adresse  
kann mehrfach vorkommen (0..1000)  
Wird vom
KOM-LE-Fachdienst-Anbieter eingetragen.

</td></tr><tr><td>
KOM-LE-Version

</td><td>
optional

</td><td>
Bezeichner: KOM-LE-Version  
Enthält die KOM-LE-Version des Clientmoduls der
angegebenen "mail" Adresse. Anhand dieser Version erkennt das sendende
Clientmodul, welche KOM-LE-Version vom Empfänger-Clientmodul unterstützt wird
und in welchem Format die Mail an diesen Empfänger versandt wird.  
Wenn nicht
angegeben, wird KOM-LE-Version 1.0 angenommen.

</td></tr><tr><td>
changeDateTime

</td><td>
obligatorisch

</td><td>
Der VZD setzt dieses Attribut bei jeder Schreiboperation für den Datensatz
(Basisdaten) auf die aktuelle Zeit. Format entsprechend RFC 3339, section 5.6.

</td></tr></table>

**[\<=]**

Die Abbildung Abb_VZD_logisches_Datenmodell stellt die Datenstruktur des
Verzeichnisdienstes als UML-Klassendiagramm dar. Die Basisdaten sind rot, die
Fachdaten grün und die als Ergebnis der LDAP-Suche in Form einer flachen Liste
gefundenen Einträge sind blau dargestellt. Zu jedem Attribut ist die
Kardinalität in eckigen Klammern angegeben.

Unter dem Begriff SMC-B sind alle Ausprägungen zusammengefasst (SMC-B ORG,
SMC-B KTR). Wenn eine Differenzierung erforderlich ist, wird die spezifische
Ausprägung der SMC-B explizit beschrieben.

In der folgenden Tabelle wird der Wertebereich für das Attribut Eintragstyp (in
LDAP == entryType) sowie das Mapping auf die ProfessionOID festgelegt.

<table><tr><th>
Eintragstyp

</th><th>
Eintragstyp Bedeutung

</th><th>
ProfessionOID (ProfessionItem)

</th></tr><tr><td>
1

</td><td>
Berufsgruppe

</td><td>
1.2.276.0.76.4.30 (Ärztin/Arzt)  
1.2.276.0.76.4.31 (Zahnärztin/Zahnarzt) 

1.2.276.0.76.4.32 (Apotheker/-in)  
1.2.276.0.76.4.33 (Apothekerassistent/-in)
 
1.2.276.0.76.4.34 (Pharmazieingenieur/-in) 

1.2.276.0.76.4.35 (pharmazeutisch-technische/-r Assistent/-in) 

1.2.276.0.76.4.36 (pharmazeutisch-kaufmännische/-r Angestellte) 

1.2.276.0.76.4.37 (Apothekenhelfer/-in) 

1.2.276.0.76.4.38 (Apothekenassistent/-in) 

1.2.276.0.76.4.39 (Pharmazeutische/-r Assistent/-in) 

1.2.276.0.76.4.40 (Apothekenfacharbeiter/-in) 

1.2.276.0.76.4.41 (Pharmaziepraktikant/-in)  
1.2.276.0.76.4.42 (Stud.pharm.
oder Famulant/-in)  
1.2.276.0.76.4.43 (PTA-Praktikant/-in) 

1.2.276.0.76.4.44 (PKA Auszubildende/-r)  
1.2.276.0.76.4.45
(Psychotherapeut/-in)  
1.2.276.0.76.4.46 (Psychologische/-r
Psychotherapeut/-in)  
1.2.276.0.76.4.47 (Kinder- und
Jugendlichenpsychotherapeut/-in)  
1.2.276.0.76.4.48 (Rettungsassistent/-in) 

1.2.276.0.76.4.178 (Notfallsanitäter/-in)  
1.2.276.0.76.4.232 (Gesundheits-
und Krankenpfleger/-in, Gesundheits- und Kinderkrankenpfleger/-in) 

1.2.276.0.76.4.233 (Altenpfleger/-in)  
1.2.276.0.76.4.234 (Pflegefachfrauen
und Pflegefachmänner)  
1.2.276.0.76.4.235 (Hebamme)  
1.2.276.0.76.4.236
(Physiotherapeut/-in)  
1.2.276.0.76.4.237 (Augenoptiker/-in und
Optometrist/-in)  
1.2.276.0.76.4.238 (Hörakustiker/-in)  
1.2.276.0.76.4.239
(Orthopädieschuhmacher/-in)  
1.2.276.0.76.4.240 (Orthopädietechniker/-in) 

1.2.276.0.76.4.241 (Zahntechniker/-in)

</td></tr><tr><td>
2

</td><td>
Versicherte/-r

</td><td>
1.2.276.0.76.4.49 (Versicherte/-r)

</td></tr><tr><td>
3

</td><td>
Leistungserbringer Institution

</td><td>
1.2.276.0.76.4.50 (Betriebsstätte Arzt)  
1.2.276.0.76.4.51 (Zahnarztpraxis) 

1.2.276.0.76.4.52 (Betriebsstätte Psychotherapeut) 

1.2.276.0.76.4.53 (Krankenhaus)  
1.2.276.0.76.4.54 (Öffentliche Apotheke) 

1.2.276.0.76.4.55 (Krankenhausapotheke) 

1.2.276.0.76.4.56 (Bundeswehrapotheke)  
1.2.276.0.76.4.57 (Betriebsstätte
Mobile Einrichtung Rettungsdienst)  
1.2.276.0.76.4.245 (Betriebsstätte
Gesundheits-, Kranken- und Altenpflege)  
1.2.276.0.76.4.246 (Betriebsstätte
Geburtshilfe)  
1.2.276.0.76.4.247 (Betriebsstätte Physiotherapie) 

1.2.276.0.76.4.248 (Betriebsstätte Augenoptiker)  
1.2.276.0.76.4.249
(Betriebsstätte Hörakustiker)  
1.2.276.0.76.4.250 (Betriebsstätte
Orthopädieschuhmacher)  
1.2.276.0.76.4.251 (Betriebsstätte
Orthopädietechniker)  
1.2.276.0.76.4.252 (Betriebsstätte Zahntechniker) 

1.2.276.0.76.4.253 (Rettungsleitstelle)  
1.2.276.0.76.4.254 (Betriebsstätte
Sanitätsdienst Bundeswehr)

</td></tr><tr><td>
4

</td><td>
Organisation

</td><td>
1.2.276.0.76.4.187 (Betriebsstätte Leistungserbringerorganisation
Vertragszahnärzte)  
1.2.276.0.76.4.58 (Betriebsstätte gematik) 

1.2.276.0.76.4.190 (AdV-Umgebung bei Kostenträger)  
1.2.276.0.76.4.210
(Betriebsstätte Leistungserbringerorganisation Kassenärztliche Vereinigung) 

1.2.276.0.76.4.223 (Betriebsstätte GKV-Spitzenverband)  
1.2.276.0.76.4.226
(Betriebsstätte Mitgliedsverband der Krankenhäuser)  
1.2.276.0.76.4.227
(Betriebsstätte der Deutsche Krankenhaus TrustCenter und
Informationsverarbeitung GmbH)  
1.2.276.0.76.4.228 (Betriebsstätte der
Deutschen Krankenhausgesellschaft)  
1.2.276.0.76.4.224 (Betriebsstätte
Apothekerverband)  
1.2.276.0.76.4.225 (Betriebsstätte Deutscher
Apothekerverband)  
1.2.276.0.76.4.229 (Betriebsstätte der Bundesärztekammer)
 
1.2.276.0.76.4.230 (Betriebsstätte einer Ärztekammer)  
1.2.276.0.76.4.231
(Betriebsstätte einer Zahnärztekammer)  
1.2.276.0.76.4.242 (Betriebsstätte
der Kassenärztlichen Bundesvereinigung)  
1.2.276.0.76.4.243 (Betriebsstätte
der Bundeszahnärztekammer)  
1.2.276.0.76.4.244 (Betriebsstätte der
Kassenzahnärztlichen Bundesvereinigung)

1.2.276.0.76.4.255 (Betriebsstätte Öffentlicher Gesundheitsdienst)

1.2.276.0.76.4.256 (Betriebsstätte Arbeitsmedizin)

1.2.276.0.76.4.257 (Betriebsstätte Vorsorge- und Rehabilitation)

1.2.276.0.76.4.262 (Betriebsstätte Pflegeberatung nach § 7a SGB XI)

1.2.276.0.76.4.263 (Betriebsstätte Psychotherapeutenkammer)

1.2.276.0.76.4.264 (Betriebsstätte Bundespsychotherapeutenkammer)

1.2.276.0.76.4.265 (Betriebsstätte Landesapothekerkammer)

1.2.276.0.76.4.266 (Betriebsstätte Bundesapothekerkammer)

1.2.276.0.76.4.267 (Betriebsstätte elektronisches Gesundheitsberuferegister)

1.2.276.0.76.4.268 (Betriebsstätte Handwerkskammer)

1.2.276.0.76.4.269 (Betriebsstätte Register für Gesundheitsdaten)

1.2.276.0.76.4.270 (Betriebsstätte Abrechnungsdienstleister)

1.2.276.0.76.4.271 (Betriebsstätte PKV-Verband)

</td></tr><tr><td>
5

</td><td>
Krankenkasse

</td><td>
1.2.276.0.76.4.59 (Betriebsstätte Kostenträger)

</td></tr><tr><td>
6

</td><td>
Krankenkasse ePA 

</td><td>
1.2.276.0.76.4.273 (ePA KTR-Zugriffsautorisierung)

</td></tr></table>

**A_22224 - VZD, konfigurierbares Mapping von professionOID auf entryType**

Der VZD MUSS das Mapping von professionOID auf entryType konfigurierbar
implementieren, so dass bei Änderung des Mappings oder neuen professionOIDs
oder neuen entryTypes keine Anpassung an der Software des VZD erforderlich
ist.Änderungen am Mapping werden durch den Gesamtbetriebsverantwortlichen TI
per betrieblichen Change veranlasst. **[\<=]**

### 6 Anhang A – Verzeichnisse

### 6.1 Abkürzungen

<table><tr><th>
Kürzel

</th><th>
Erläuterung

</th></tr><tr><td>
C.FD.TLS-C

</td><td>
Client-Zertifikat (öffentlicher Schlüssel) eines fachanwendungsspezifischen
Dienstes für TLS Verbindungen

</td></tr><tr><td>
C.ZD.TLS-S

</td><td>
Server-Zertifikat (öffentlicher Schlüssel) eines zentralen Dienstes der
TI-Plattform für TLS Verbindungen

</td></tr><tr><td>
DNS-SD

</td><td>
Domain Name System Service Discovery

</td></tr><tr><td>
DNSSEC

</td><td>
Domain Name System Security Extensions

</td></tr><tr><td>
FAD

</td><td>
fachanwendungsspezifischer Dienst

</td></tr><tr><td>
FQDN

</td><td>
Full Qualified Domain Name

</td></tr><tr><td>
GTI

</td><td>
Gesamtbetriebsverantwortlicher der TI

</td></tr><tr><td>
HBA

</td><td>
Heilberufsausweis

</td></tr><tr><td>
http

</td><td>
hypertext transport protocol

</td></tr><tr><td>
ID.FD.TLS-C

</td><td>
Client-Identität (privater und öffentlicher Schlüssel) eines
fachanwendungsspezifischen Dienstes für TLS Verbindungen

</td></tr><tr><td>
ID.ZD.TLS-S

</td><td>
Server-Identität (privater und öffentlicher Schlüssel) eines zentralen
Dienstes der TI-Plattform für TLS Verbindungen

</td></tr><tr><td>
KOM-LE

</td><td>
Kommunikation für Leistungserbringer (Fachanwendung)

</td></tr><tr><td>
LDAP

</td><td>
Lightweight Directory Access Protocol

</td></tr><tr><td>
LE

</td><td>
Leistungserbringer

</td></tr><tr><td>
OCSP

</td><td>
Online Certificate Status Protocol

</td></tr><tr><td>
PKI

</td><td>
Public Key Infrastructure

</td></tr><tr><td>
PTR Resource Record

</td><td>
Domain Name System Pointer Resource Record

</td></tr><tr><td>
SMC

</td><td>
Secure Module Card

</td></tr><tr><td>
SOAP

</td><td>
Simple Object Access Protocol

</td></tr><tr><td>
TCP

</td><td>
Transmission Control Protocol

</td></tr><tr><td>
TI

</td><td>
Telematikinfrastruktur

</td></tr><tr><td>
TIP

</td><td>
Telematikinfrastruktur-Plattform

</td></tr><tr><td>
TLS

</td><td>
Transport Layer Security

</td></tr><tr><td>
TUC

</td><td>
Technischer Use Case

</td></tr><tr><td>
URL

</td><td>
Uniform Resource Locator

</td></tr><tr><td>
VZD

</td><td>
Verzeichnisdienst

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
XML

</td><td>
Extensible Markup Language

</td></tr></table>

### 6.2 Glossar

Das Glossar wird als eigenständiges Dokument (vgl. [gemGlossar]) zur Verfügung
gestellt.

### 6.3 Abbildungsverzeichnis

- [Abbildung-1] - Einordnung des VZD in die TI

### 6.4 Tabellenverzeichnis

- [Tabelle-1] - Tab_PT_VZD_Schnittstellen
- [Tabelle-2] - Tab_VZD_Schnittstelle_I_Directory_Query
- [Tabelle-3] - Tab_TUC_VZD_0001
- [Tabelle-4] - Tab_VZD_Schnittstelle_I_Directory_Maintenance
- [Tabelle-5] -  Tab_VZD_Daten-Transformation
- [Tabelle-6] - Tab_TUC_VZD_0002
- [Tabelle-7] - Tab_TUC_VZD_0003
- [Tabelle-8] - Tab_TUC_VZD_0004
- [Tabelle-9] - Tab_TUC_VZD_0005
- [Tabelle-10] - Tab_VZD_Schnittstelle_I_Directory_Application_Maintenance
- [Tabelle-12] - VZD_TAB_I_Directory_Application_Maintenance_Add_Mapping
- [Tabelle-13] - Tab_TUC_VZD_0006
- [Tabelle-14] - VZD_TAB_KOM-LE_Attributes
- [Tabelle-15] - Tab_TUC_VZD_0007
- [Tabelle-16] - Tab_TUC_VZD_0008
- [Tabelle-17] - Tab_TUC_VZD_0009
- [Tabelle-18] - VZD_TAB_I_Directory_Application_Maintenance_Modify_Mapping
- [Tabelle-19] - Tab_TUC_VZD_0010
- [Tabelle-20] - VZD_TAB_KOM-LE_Attributes
- [Tabelle-21] - Tab_TUC_VZD_0011
- [Tabelle-22] - Tab_VZD_Schnittstelle_I_Directory_Administration
- [Tabelle-24] - Tab_VZD „add_Directory_Entry”
- [Tabelle-26] - Tab_VZD „modify_Directory_Entry”
- [Tabelle-29] - Tab_VZD „read_Directory_Certificates”
- [Tabelle-32] - Tab_VZD_Datenbeschreibung
- [Tabelle-33] - Tab_VZD_Mapping_Eintragstyp_und_ProfessionOID

### 6.5 Referenzierte Dokumente

### 6.5.1 Dokumente der gematik

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
[gemKPT_Arch_TIP]

</td><td>
gematik: Konzept Architektur der TI-Plattform

</td></tr><tr><td>
[gemKPT_PKI_TIP]

</td><td>
gematik: Konzept PKI der TI-Plattform

</td></tr><tr><td>
[gemKPT_DS_TIP]

</td><td>
gematik: Datenschutzkonzept TI-Plattform

</td></tr><tr><td>
[gemKPT_Sich_TIP]

</td><td>
gematik: Spezifisches Sicherheitskonzept TI-Plattform

</td></tr><tr><td>
[gemSpec_Net]

</td><td>
gematik: Spezifikation Netzwerk

</td></tr><tr><td>
[gemSpec_OM]

</td><td>
gematik: Operations und Maintenance Spezifikation

</td></tr><tr><td>
[gemSpec_OID]

</td><td>
gematik: Spezifikation Festlegung von OIDs

</td></tr><tr><td>
[gemSpec_PKI]

</td><td>
gematik: Spezifikation PKI

</td></tr><tr><td>
[gemSpec_Perf]

</td><td>
gematik: Performance und Mengengerüst TI-Plattform

</td></tr><tr><td>
[gemSpec_TSL]

</td><td>
gematik: Spezifikation TSL-Dienst

</td></tr><tr><td>
[gemILF_Pflege_VZD]

</td><td>
gematik: Implementierungsleitfaden zur Pflege der Daten des Verzeichnisdienstes

</td></tr></table>

### 6.5.2 Weitere Dokumente

<table><tr><th>
[Quelle]

</th><th>
Herausgeber (Erscheinungsdatum): Titel

</th></tr><tr><td>
[BSI APP.2.1]

</td><td>
Bundesamt für Sicherheit in der Informationstechnik: BSI
Grundschutz-Kompendium, Baustein APP.2.1,  

https://www.bsi.bund.de/DE/Themen/ITGrundschutz/ITGrundschutzKompendium/bausteine/APP/APP_2_1_Allgemeiner_Verzeichnisdienst.html 

</td></tr><tr><td>
[BSI-SiGw]

</td><td>
Bundesamt für Sicherheit in der Informationstechnik (o.J.): Konzeption von 

Sicherheitsgateways, Version 1.0

</td></tr><tr><td>
[HL7FHIR] 

</td><td>
FHIR Specification

https://www.hl7.org/fhir/

 

</td></tr><tr><td>
[RFC2119]

</td><td>
RFC 2119 (March 1997):  
Key words for use in RFCs to Indicate Requirement
Levels  
http://www.rfc-editor.org/rfc/rfc2119.txt

</td></tr><tr><td>
[

RFC2696]

</td><td>
RFC 2696 (September 1999)

LDAP Control Extension for Simple Paged Results Manipulation

https://tools.ietf.org/html/rfc2696

 

</td></tr><tr><td>
[RFC4510]

</td><td>
RFC 4510 (June 2006):  
Lightweight Directory Access Protocol (LDAP): Technical
Specification Road  
Map,  
http://www.ietf.org/rfc/rfc4510.txt

</td></tr><tr><td>
[RFC4511]

</td><td>
RFC 4511 (June 2006):  
Lightweight Directory Access Protocol (LDAP): The
Protocol,  
http://www.ietf.org/rfc/rfc4511.txt

</td></tr><tr><td>
[RFC4512]

</td><td>
RFC 4512 (June 2006):  
Lightweight Directory Access Protocol (LDAP): Directory
Information Models  
http://www.rfc-editor.org/rfc/rfc4512.txt

</td></tr><tr><td>
[RFC4513]

</td><td>
RFC 4513 (June 2006):  
Lightweight Directory Access Protocol (LDAP):
Authentication  
Methods and Security Mechanisms 

http://www.rfc-editor.org/rfc/rfc4513.txt

</td></tr><tr><td>
[RFC4514]

</td><td>
RFC 4514 (June 2006):  
Lightweight Directory Access Protocol (LDAP): String
Representation of  
Distinguished Names 

http://www.rfc-editor.org/rfc/rfc4514.txt

</td></tr><tr><td>
[RFC4515]

</td><td>
RFC 4515 (June 2006):  
Lightweight Directory Access Protocol (LDAP): String
Representation of  
Search Filters  
http://www.rfc-editor.org/rfc/rfc4515.txt

</td></tr><tr><td>
[RFC4516]

</td><td>
RFC 4516 (June 2006):  
Lightweight Directory Access Protocol (LDAP): Uniform
Resource Locator  
http://www.rfc-editor.org/rfc/rfc4516.txt

</td></tr><tr><td>
[RFC4517]

</td><td>
RFC 4517 (June 2006):  
Lightweight Directory Access Protocol (LDAP): Syntaxes
and Matching Rules  
http://www.rfc-editor.org/rfc/rfc4515.txt

</td></tr><tr><td>
[RFC4519]

</td><td>
RFC 4519 (June 2006):  
Lightweight Directory Access Protocol (LDAP): Schema for
User Applications  
http://www.rfc-editor.org/rfc/rfc4519.txt

</td></tr><tr><td>
[RFC4522]

</td><td>
RFC 4522 (June 2006):  
Lightweight Directory Access Protocol (LDAP): The Binary
Encoding Option  
http://www.rfc-editor.org/rfc/rfc4522.txt

</td></tr><tr><td>
[RFC4523]

</td><td>
RFC 4523 (June 2006):  
Lightweight Directory Access Protocol (LDAP) Schema
Definitions for X.509  
Certificates  
http://www.rfc-editor.org/rfc/rfc4523.txt

</td></tr><tr><td>
[RFC 6750] 

</td><td>
The OAuth 2.0 Authorization Framework: Bearer Token Usage

</td></tr><tr><td>
[RFC6763]

</td><td>
RFC 6763 (February 2013):  
DNS-Based Service Discovery 

http://www.rfc-editor.org/rfc/rfc6763.txt

</td></tr></table>





[Dokumentinformationen]: #dokumentinformationen
[Inhaltsverzeichnis]:    #inhaltsverzeichnis
[1]:                     #1-einordnung-des-dokumentes
[1.1]:                   #11-zielsetzung
[1.2]:                   #12-zielgruppe
[1.3]:                   #13-geltungsbereich
[1.4]:                   #14-abgrenzungen
[1.5]:                   #15-methodik
[2]:                     #2-systemüberblick
[3]:                     #3-übergreifende-festlegungen
[3.1]:                   #31-it-sicherheit-und-datenschutz
[3.2]:                   #32-fachliche-anforderungen
[4]:                     #4-funktionsmerkmale
[4.1]:                   #41-schnittstelle-i_directory_query
[4.1.1]:                 #411-operation-search_directory
[4.1.1.1]:               #4111-umsetzung
[4.1.1.2]:               #4112-nutzung
[4.2]:                   #42-schnittstelle-i_directory_maintenance
[4.2.1]:                 #421-operation-add_directory_entry
[4.2.1.1]:               #4211-umsetzung
[4.2.1.2]:               #4212-nutzung
[4.2.2]:                 #422-operation-read_directory_entry
[4.2.2.1]:               #4221-umsetzung
[4.2.2.2]:               #4222-nutzung
[4.2.3]:                 #423-operation-modify_directory_entry
[4.2.3.1]:               #4231-umsetzung
[4.2.3.2]:               #4232-nutzung
[4.2.4]:                 #424-operation-delete_directory_entry
[4.2.4.1]:               #4241-umsetzung
[4.2.4.2]:               #4242-nutzung
[4.3]:                   #43-schnittstelle-i_directory_application_maintenance
[4.3.1]:                 #431-operation-getinfo
[4.3.1.1]:               #4311-umsetzung-rest
[4.3.1.2]:               #4312-nutzung-rest
[4.3.2]:                 #432-operation-add_directory_fa-attributes
[4.3.2.1]:               #4321-umsetzung-soap
[4.3.2.2]:               #4322-nutzung-soap
[4.3.2.3]:               #4323-umsetzung-ldapv3
[4.3.2.4]:               #4324-nutzung-ldapv3
[4.3.2.5]:               #4325-umsetzung-rest
[4.3.2.6]:               #4326-nutzung-rest
[4.3.3]:                 #433-operation-delete_directory_fa-attributes
[4.3.3.1]:               #4331-umsetzung-soap
[4.3.3.2]:               #4332-nutzung-soap
[4.3.3.3]:               #4333-umsetzung-ldapv3
[4.3.3.4]:               #4334-nutzung-ldapv3
[4.3.3.5]:               #4335-umsetzung-rest
[4.3.3.6]:               #4336-nutzung-rest
[4.3.4]:                 #434-operation-modify_directory_fa-attributes
[4.3.4.1]:               #4341-umsetzung-soap
[4.3.4.2]:               #4342-nutzung-soap
[4.3.4.3]:               #4343-umsetzung-ldapv3
[4.3.4.4]:               #4344-nutzung-ldapv3
[4.3.4.5]:               #4345-umsetzung-rest
[4.3.4.6]:               #4346-nutzung-rest
[4.3.5]:                 #435-operation-get_directory_fa-attributes
[4.3.5.1]:               #4351-umsetzung-rest
[4.3.5.2]:               #4352-nutzung-rest
[4.4]:                   #44-prozessschnittstelle-p_directory_application_registration-provided
[4.5]:                   #45-prozessschnittstelle-p_directory_maintenance-provided
[4.6]:                   #46-schnittstelle-i_directory_administration
[4.6.1]:                 #461-operationen-der-schnittstelle-i_-directory_administration
[4.6.1.1]:               #4611-i_directory_administration---lesen-der-metadaten
[4.6.1.1.1]:             #46111-get
[4.6.1.2]:               #4612-directoryentry-administration
[4.6.1.2.1]:             #46121-post
[4.6.1.2.2]:             #46122-get
[4.6.1.2.3]:             #46123-put
[4.6.1.2.4]:             #46124-delete
[4.6.1.3]:               #4613-certificate-administration
[4.6.1.3.1]:             #46131-post
[4.6.1.3.2]:             #46132-get
[4.6.1.3.3]:             #46133-delete
[4.6.1.4]:               #4614-directoryentry-synchronization
[4.6.1.4.1]:             #46141-get
[4.6.2]:                 #462-nutzung-der-schnittstelle-i_directory_administration
[5]:                     #5-datenmodell
[6]:                     #6-anhang-a-–-verzeichnisse
[6.1]:                   #61-abkürzungen
[6.2]:                   #62-glossar
[6.3]:                   #63-abbildungsverzeichnis
[6.4]:                   #64-tabellenverzeichnis
[6.5]:                   #65-referenzierte-dokumente
[6.5.1]:                 #651-dokumente-der-gematik
[6.5.2]:                 #652-weitere-dokumente
[Abbildung-1]:           gemSpec_VZD_V1.14.0 CC 2.attachments/10173094149073192682.png
[Img-002]:               gemSpec_VZD_V1.14.0 CC 2.attachments/9300399867840935207.png
[Tbl-001]:               #Tbl-001 (&93834775872320)
[Tabelle-1]:             #Tabelle-1 (&93834768038032)
[Tabelle-2]:             #Tabelle-2 (&93834783666040)
[Tabelle-3]:             #Tabelle-3 (&93834771006504)
[Tabelle-4]:             #Tabelle-4 (&93834808798880)
[Tabelle-5]:             #Tabelle-5 (&93834808839784)
[Tabelle-6]:             #Tabelle-6 (&93834772271344)
[Tabelle-7]:             #Tabelle-7 (&93834810584856)
[Tabelle-8]:             #Tabelle-8 (&93834781812848)
[Tabelle-9]:             #Tabelle-9 (&93834777663992)
[Tabelle-10]:            #Tabelle-10 (&93834764857056)
[Tbl-012]:               #Tbl-012 (&93834764928456)
[Tabelle-12]:            #Tabelle-12 (&93834764469912)
[Tabelle-13]:            #Tabelle-13 (&93834764487624)
[Tabelle-14]:            #Tabelle-14 (&93834781572344)
[Tabelle-15]:            #Tabelle-15 (&93834781599672)
[Tbl-017]:               #Tbl-017 (&93834810454344)
[Tabelle-16]:            #Tabelle-16 (&93834810511320)
[Tabelle-17]:            #Tabelle-17 (&93834810741992)
[Tabelle-18]:            #Tabelle-18 (&93834783533192)
[Tabelle-19]:            #Tabelle-19 (&93834783550576)
[Tabelle-20]:            #Tabelle-20 (&93834785720696)
[Tabelle-21]:            #Tabelle-21 (&93834785746472)
[Tabelle-22]:            #Tabelle-22 (&93834783912488)
[Tbl-025]:               #Tbl-025 (&93834778275624)
[Tabelle-24]:            #Tabelle-24 (&93834783719080)
[Tbl-027]:               #Tbl-027 (&93834783775752)
[Tabelle-26]:            #Tabelle-26 (&93834783810016)
[Tabelle-29]:            #Tabelle-29 (&93834781325296)
[Tbl-030]:               #Tbl-030 (&93834781363024)
[Tbl-031]:               #Tbl-031 (&93834781395088)
[Tabelle-32]:            #Tabelle-32 (&93834768115560)
[Tabelle-33]:            #Tabelle-33 (&93834768359752)
[Tbl-034]:               #Tbl-034 (&93834801849464)
[Tbl-035]:               #Tbl-035 (&93834801996680)
[Tbl-036]:               #Tbl-036 (&93834802033168)
[https://fachportal.gematik.de/]: https://fachportal.gematik.de/ (&93834765154432)
[RFC 6750]:              https://tools.ietf.org/html/rfc6750 (&93834778247808)
[RFC 6750]:              https://tools.ietf.org/html/rfc6750 (&93834778250496)
[https://www.hl7.org/fhir/]: https://www.hl7.org/fhir/ (&93834802045688)
[https://tools.ietf.org/html/rfc2696]: https://tools.ietf.org/html/rfc2696 (&93834802052184)
