
Elektronische Gesundheitskarte und Telematikinfrastruktur

### 

- Klassifizierung: öffentlich
- Referenzierung: gemF_Highspeed-Konnektor
- Revision: 593405
- Stand: 31.08.2022
- Status: freigegeben
- Version: 1.1.0

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
Bearbeitung

</th></tr><tr><td>
1.0.0 CC

</td><td>
30.08.21

</td><td>
zur Abstimmung freigegeben

</td><td>
gematik

</td></tr><tr><td>
1.0.0

</td><td>
16.03.22

</td><td>
freigegeben

</td><td>
gematik

</td></tr><tr><td>
1.1.0

</td><td>
31.08.22

</td><td>
Einarbeitung Änderungsliste HSK_Maintenance_22.1

</td><td>
gematik

</td></tr><tr><td>
5.2.1.2

</td><td>
redaktionelle Anpassung (doppelte Afo)

</td></tr></table>

### Inhaltsverzeichnis

- [Dokumentinformationen]
- [Inhaltsverzeichnis]
- [1] Einordnung des Dokuments
  - [1.1] Zielsetzung
  - [1.2] Zielgruppe
  - [1.3] Abgrenzungen
  - [1.4] Methodik
    - [1.4.1] Epic und User Story
    - [1.4.2] Anforderungen
- [2] Epic und User Story
  - [2.1] STB-169 Highspeed-Konnektor 2.0
    - [2.1.1] Betrieb auf Standard-Hardware/Ablaufumgebungen
    - [2.1.2] Breitband-Zugang zur TI
    - [2.1.3] Leistungsfähiges Modul für Identitäten
- [3] Einordnung in die Telematikinfrastruktur
- [4] Technisches Konzept
  - [4.1] Anbindung über SZZP an die TI
  - [4.2] Sicherheitsnachweis
    - [4.2.1] Hersteller
      - [4.2.1.1] Sichere Software-Entwicklung
    - [4.2.2] Anbieter/Betreiber
- [5] Spezifikation
  - [5.1] Produkteigenschaften (Funktional und Sicherheit)
    - [5.1.1] Schnittstellen
    - [5.1.2] Sichere Trennung von logischen Konnektorinstanzen
    - [5.1.3] Eingeschränkte Nutzung des KSR
  - [5.2] Betrieblich
    - [5.2.1] Betriebsumgebung
      - [5.2.1.1] Initialisierung des Vertrauensraumes
      - [5.2.1.2] HSM
      - [5.2.1.3] Vertrauenswürdige Ausführungsumgebung
      - [5.2.1.4] Ausschluss von nicht autorisierten Zugriffen aus dem Betriebsumfeld
      - [5.2.1.5] Unabhängigkeit von dem Betreiber des Aktensystems
      - [5.2.1.6] Anforderungen aus gemSpec_DS_Anbieter
    - [5.2.2] ITSM Integration
      - [5.2.2.1] Mitwirkungspflichten ITSM
    - [5.2.3] Auftragsdatenverarbeitung/AVV
    - [5.2.4] Weitere Betriebliche Anforderungen
- [6] Test Konzept
  - [6.1] Zugang und Verfügbarkeit
  - [6.2] Logging
  - [6.3] Interoperabilität
- [7] Anhang A – Verzeichnisse
  - [7.1] Abkürzungen
  - [7.2] Referenzierte Dokumente
    - [7.2.1] Dokumente der gematik
    - [7.2.2] Weitere Dokumente
- [8] Anhang B – Anmerkungen aus der Industrie
- [9] Anhang C – Offene Punkte, Fragen
  - [9.1] <offener Punkt oder Frage>

### 1 Einordnung des Dokuments

Das Dokument ergänzt vorhandene Spezifikationen für das Zulassungsobjektes
eines im Rechenzentrum betriebenen Highspeed-Konnektors.

### 1.1 Zielsetzung

Mit dem Highspeed-Konnektor soll die Grundlage für eine hochverfügbare und
skalierbare Konnektorlösung zum Betrieb in einem zertifizierten Rechenzentrum
geschaffen werden.

### 1.2 Zielgruppe

Das Dokument richtet sich an Hersteller, Betreiber, BSI und die Gesellschafter
der gematik.

### 1.3 Abgrenzungen

### 1.4 Methodik

### 1.4.1 Epic und User Story

Epics und zugeordnete User Stories werden durch eine eindeutige ID
gekennzeichnet.

Epic und UserStory werden im Dokument wie folgt dargestellt:\<Jira-ID\> -
\<Zusammenfassung des Jira-Issue\>Text / Beschreibung [\<=]

Dabei umfasst die Anforderung sämtliche zwischen Jira-ID und Textmarke [\<=]
angeführten Inhalte.

### 1.4.2 Anforderungen

Anforderungen als Ausdruck normativer Festlegungen werden durch eine eindeutige
ID sowie die dem RFC 2119 [RFC2119] entsprechenden, in Großbuchstaben
geschriebenen deutschen Schlüsselworte MUSS, DARF NICHT, SOLL, SOLL NICHT,
KANN gekennzeichnet.

Da in dem Beispielsatz „Eine leere Liste DARF NICHT ein Element besitzen.“
die Phrase „DARF NICHT“ semantisch irreführend wäre (wenn nicht ein, dann
vielleicht zwei?), wird in diesem Dokument stattdessen „Eine leere Liste DARF
KEIN Element besitzen.“ verwendet. Die Schlüsselworte werden außerdem um
Pronomen in Großbuchstaben ergänzt, wenn dies den Sprachfluss verbessert oder
die Semantik verdeutlicht.

Anforderungen werden im Dokument wie folgt dargestellt:\<AFO-ID\> - \<Titel der
Afo\>Text / Beschreibung [\<=]

Dabei umfasst die Anforderung sämtliche zwischen Afo-ID und Textmarke [\<=]
angeführten Inhalte.

### 2 Epic und User Story

### 2.1 STB-169 Highspeed-Konnektor 2.0

Definition der Zulassungsgrundlagen für eine rechenzentrumsbasierte
TI-Zugangslösung auf Basis der funktionalen Anforderungen für den Konnektor
PTV 5:

 ---> UL

### 2.1.1 Betrieb auf Standard-Hardware/Ablaufumgebungen

Der Highspeed-Konnektor soll auf Standard-Hardware betrieben werden. Damit wird
eine Unabhängigkeit von den Produktlebenszyklen der Serverhersteller erreicht.
Je nach Leistungsanforderungen des Betreibers wird eine geeignete Hardware
ausgewählt.

### 2.1.2 Breitband-Zugang zur TI

Die Bandbreite des Zugangs zur TI lässt sich nach Anforderungen des Betreibers
skalieren.

### 2.1.3 Leistungsfähiges Modul für Identitäten

Der Identitätsspeicher muss so leistungsfähig sein, dass auch große
Installationen mit einer Identität betrieben werden können. (ein HSM statt
viele gSMC-K)

### 3 Einordnung in die Telematikinfrastruktur

Der Highspeed-Konnektor kann die Funktion des Konnektors für große
Institutionen (wie Krankenhäuser) übernehmen, bei denen aktuell durch die
Institution eine Vielzahl von Einbox- oder Rechenzentrums-Konnektoren betrieben
werden muss und daher das Bedürfnis nach einer performanteren Lösung besteht.

Der Highspeed-Konnektor setzt die Spezifikation des Konnektors bis auf die
Bereiche um, die in diesem Dokument explizit ausgenommen werden. Zusätzlich
werden Anforderungen spezifisch für den Highspeed-Konnektor gestellt.

Die Lösung stellt keinen allgemeinen neuen Zugang zur TI dar, sondern soll
explizit nur in großen Institutionen den Betrieb von vielen
Einbox-Konnektoren, wie sie heute dort betrieben werden, 1zu 1 ersetzen. Der
Betrieb findet nach wie vor in direkter Verantwortung der LE-Institution statt.
Die Nutzung des eines gehosteten Highspeed-Konnektors im Rahmen einer
Auftragsdatenverarbeitung ist jedoch nicht ausgeschlossen.

### 4 Technisches Konzept

Die Konnektorsoftware wird auf Standard-Serverhardware betrieben. Es können
geeignete Virtualisierungs- und Container-Lösungen zum Einsatz kommen.

Die Konnektorsoftware kann modularisiert werden (z.B. Anwendungskonnektor,
Netzkonnektor, Fachmodule). Es muss sichergestellt sein, dass die
Schnittstellen der Module nur von den dafür vorgesehenen Gegenstellen benutzt
werden und die Vertraulichkeit der Kommunikation zwischen den Modulen
gewährleistet ist (z.B. durch beidseitig authentisierte und verschlüsselte
Transportkanäle).

Die gSMC-K kann durch zertifizierte ( z. B.FIPS140-1 und 140-2 oder CC) HSM
oder TPM-Lösungen ersetzt werden. Die Anforderungen an die Personalisierung
der gSMC-K gelten analog für die Personalisierung des HSM. 

Innerhalb des geschützten Bereichs des Rechenzentrums können SMC-B und gSMC-K
in lokalen Kartenlesern gesteckt und genutzt werden, es müssen keine
eHealth-Kartenterminals verwendet werden. Die SMC-B-PIN kann über den
Konnektor eingegeben werden, eine Eingabe direkt am Kartenterminal ist nicht
notwendig.

Um den Missbrauch der SMC-B zu verhindern, muss der Zugriff des Betreibers auf
die SMC-B ausgeschlossen sein z.B. durch eine Trennung von Besitz und Wissen.

### 4.1 Anbindung über SZZP an die TI

Der Highspeed-Konnektor wird direkt über einen SZZP (light) des AZPD (Arvato)
an die TI angebunden.

 ---> UL

### 4.2 Sicherheitsnachweis

### 4.2.1 Hersteller

Die Sicherheit des Produktes wird insgesamt durch drei Prüfverfahren
nachgewiesen:

 ---> UL

Zudem ist ein Nachweis zu den sicheren Softwareentwicklungsprozessen des
Herstellers notwendig (siehe folgender Absatz).

### 4.2.1.1 Sichere Software-Entwicklung

**A_22046 - Sichere Software Entwicklungsumgebung**

Der Hersteller des Highspeed-Konnektors MUSS die Entwicklung in der
CC-evaluierten Entwicklungsumgebung durchführen. Wenn die Entwicklung nicht in
einer während der Konnektor-Evaluierung (Aspekt ALC) mit geprüften Umgebung
stattfindet, MUSS der Hersteller ein Sicherheitsgutachten über seine sicheren
Softwareentwicklungsprozesse einreichen. **[\<=]**

### 4.2.2 Anbieter/Betreiber

Für die Anbieterzulassung wird die Sicherheit über ein Sicherheitsgutachten
nachgewiesen.

### 5 Spezifikation

### 5.1 Produkteigenschaften (Funktional und Sicherheit)

Für den Highspeed-Konnektor gelten folgende Anforderungen, auch wenn sie sich
an den Konnektor, das "Fachmodul ePA im KTR-Consumer" oder den Basis- bzw.
KTR-Consumer richten:

**A_21853 - Feste Kopplung von Konnektor und SZZP**

Der Konnektor und der SZZP MÜSSEN kryptographisch miteinander gekoppelt werden,
so dass ausschließlich der Konnektor - und explizit nicht der Administrator
der Betriebsumgebung - über die Schnittstellen des SZZP Zugang in die TI
bekommen kann. **[\<=]**

**A_21882 - Authentisierung für Kopplung von Konnektor und SZZP**

Der Konnektor MUSS das Auslösen der Kopplung mit einem SZZP gesondert von der
Administrations-Schnittstelle vor Zugriff schützen, sodass dies grundsätzlich
von der Rolle des Konnektor-Administrators getrennt werden kann. **[\<=]**

**A_21883 - Kopplung von Konnektor und SZZP nur durch Hersteller**

Der Hersteller des Konnektors MUSS im Rahmen der Inbetriebnahme des Konnektors
die Kopplung zwischen Konnektor und SZZP vornehmen und die Zugangsdaten - vom
Konnektor und vom SZZP - für das Auslösen der Kopplung geheim halten.
**[\<=]**

**TIP1-A_4730-02 - Kommunikation mit NET_TI_GESICHERTE_FD**

Der Konnektor MUSS sicherstellen, dass IP-Pakete mit einer Absenderadresse aus
dem Adressbereich NET_TI_GESICHERTE_FD verworfen werden, wenn sie nicht vom
SZZP der TI stammen.Der Konnektor MUSS die Kommunikation mit Systemen des
Netzwerksegments NET_TI_GESICHERTE_FD für folgende Fälle unterstützen:

 ---> UL

Der Konnektor MUSS insbesondere die Kommunikation an seinen Außenschnittstellen
mit Systemen des Netzwerksegments NET_TI_GESICHERTE_FD für folgende Fälle
blockieren:

 ---> UL

Der Konnektor MUSS sicherstellen, dass die aus einer unterstützten
Kommunikation mit Systemen aus dem Netzwerksegment NET_TI_GESICHERTE_FD
bestimmten IP-Pakete ausschließlich zum SZZP der TI  geleitet werden. **[\<=]**

**TIP1-A_4731-02 - Kommunikation mit NET_TI_ZENTRAL**

Der Konnektor MUSS sicherstellen, dass IP-Pakete mit einer Absenderadresse aus
dem Adressbereich NET_TI_ZENTRAL verworfen werden, wenn sie nicht vom SZZP der
TI stammen.Der Konnektor MUSS die Kommunikation mit Systemen des
Netzwerksegments NET_TI_ZENTRAL für folgende Fälle unterstützen:

 ---> UL

Der Konnektor MUSS insbesondere die Kommunikation an seinen Außenschnittstellen
mit Systemen des Netzwerksegments NET_TI_ZENTRAL für folgende Fälle
blockieren:

 ---> UL

Der Konnektor MUSS sicherstellen, dass die aus einer unterstützten
Kommunikation mit Systemen aus dem Netzwerksegment NET_TI_ZENTRAL bestimmten
IP-Pakete ausschließlich zum SZZP der TI geleitet werden. **[\<=]**

**TIP1-A_4732-02 - Kommunikation mit NET_TI_DEZENTRAL**

Der Konnektor MUSS die Kommunikation mit Systemen des Netzwerksegments
NET_TI_DEZENTRAL für folgende Fälle unterstützen:

 ---> UL

Der Konnektor MUSS insbesondere die Kommunikation an seinen Außenschnittstellen
mit Systemen des Netzwerksegments NET_TI_DEZENTRAL für folgende Fälle
blockieren:

 ---> UL

**[\<=]**

Nachfolgende Anforderung ist durch Prozessprüfung im Rahmen der
Anbieterzulassung zu gewährleisten, da die Umsetzung in den Komponenten des
Betreibers erfolgt:

**TIP1-A_4733-02 - Kommunikation mit ANLW_AKTIVE_BESTANDSNETZE**

Der Konnektor MUSS sicherstellen, dass IP-Pakete mit einer Absenderadresse aus
dem Adressbereich ANLW_AKTIVE_BESTANDSNETZE verworfen werden, wenn sie nicht
vom SZZP der TI stammen.Der Konnektor MUSS die Kommunikation mit Systemen des
Netzwerksegments ANLW_AKTIVE_BESTANDSNETZE für folgende Fälle unterstützen:

 ---> UL

Der Konnektor MUSS insbesondere die Kommunikation an seinen Außenschnittstellen
mit Systemen des Netzwerksegments ANLW_AKTIVE_BESTANDSNETZE für folgende
Fälle blockieren:

 ---> UL

Der Konnektor MUSS sicherstellen, dass die aus einer unterstützten
Kommunikation mit Systemen aus dem Netzwerksegment ANLW_AKTIVE_BESTANDSNETZE
bestimmten IP-Pakete ausschließlich zum SZZP der TI geleitet werden. **[\<=]**

**GS-A_3829-01 - HSK: Nutzung externer Namensräume**

Der Highspeed-Konnektor KANN Clientsystemen der Leistungserbringer die Namens-
und Adressauflösung für Namen und Adressen aus den Namensräumen der
Bestandsnetze über einen DNS-Forwarder ermöglichen. **[\<=]**

Die Namensauflösung für Bestandsnetze durch den HSK ist dann relevant, wenn
Clients keine Namensauflösung im Internet machen können.

**TIP1-A_4797-03 - HSK: DNS-Forwards des DNS-Servers**

Der DNS-Server des Highspeed-Konnektors MUSS die folgenden DNS-Forwards
durchführen:

Tabelle1: TAB_KON_687_03 DNS-Forwards des DNS-Servers

<table><tr><th>
Domain

</th><th>
Forwarders

</th><th>
Bemerkungen

</th></tr><tr><td>
Namensraum TI, *.DNS_TOP_  
LEVEL_DOMAIN_TI

</td><td>
DNS_SERVERS_TI

</td><td>
DNS Forward Rule zur Auflösung aller DNS-Namen innerhalb des Namensraums der
TI  mit der Top Level Domain telematik (für die PU) und telematik-test (für
die RU und TU).

</td></tr><tr><td>
Namensraum TI, Top Level Domain ti-wa (PU) und ti-wa-test (RU und TU).

</td><td>
DNS_SERVERS_TI

</td><td>
DNS Forward Rule zur Auflösung aller DNS-Namen innerhalb des Namensraums der TI
mit der Top Level Domain ti-wa (für die PU) und ti-wa-test (für die RU und
TU).

</td></tr><tr><td>
Namensraum angeschlossene Netze des Gesundheitswesens mit aAdG-NetG 

(Domainnamen  
von angeschlossenen Netzen des Gesundheitswesens mit aAdG-NetG
gemäß  
Bestandsnetze.xml)

</td><td>
DNS_  
SERVERS_  
BESTANDS  
NETZE  
(Je Domainnamen eines angeschlossenen
Netzes des Gesundheitswesens mit aAdG-NetG alle zugehörigen DNS-Server
IP-Adressen gemäß Bestandsnetze.xml)

</td><td>
Umsetzung abhängig von der Umsetzung von

GS-A_3829-01

:  
 Je angeschlossenes Netz des Gesundheitswesens mit aAdG-NetG in
ANLW_AKTIVE_BESTANDSNETZE wird eine DNS Forward Rule zur Auflösung von
DNS-Namen innerhalb dieses Netzes verwendet.

</td></tr><tr><td>
Lokale Zone  
„konlan.“

</td><td>
autoritativer Nameserver des Konnektors

</td><td>
DNS Forward Rule zur Auflösung aller DNS-Namen innerhalb der Zone „konlan.“

</td></tr></table>

**[\<=]**

**TIP1-A_4805-02 - HSK: Konfigurationsparameter Namensdienst und
Dienstlokalisierung**

Der Administrator MUSS die in TAB_KON_654 aufgelisteten Parameter über die
Managementschnittstelle konfigurieren und die in TAB_KON_731 aufgelisteten
Parameter ausschließlich einsehen können.Nach jeder Änderung MUSS
sichergestellt werden, dass die Änderungen sofort am autoritativen bzw. am
Caching-Nameserver zur Verfügung stehen.

Tabelle2: TAB_KON_654-02 - Konfigurationsparameter Namensdienst

<table><tr><th>
ReferenzID

</th><th>
Belegung

</th><th>
Bedeutung und Administrator-Interaktion

</th></tr><tr><td>
DNS_SERVERS_TI

</td><td>
Liste von IP-Adressen der DNS-Server

</td><td>
Liste von DNS-Servern, die zur Namensauflösung des Namensraums der TI verwendet
werden

</td></tr><tr><td>
DNS_TOP_LEVEL_

DOMAIN_TI

</td><td>
DNS Domainname

</td><td>
Top Level Domain des Namensraumes TI

</td></tr></table>

Tabelle3: TAB_KON_731-02 Einsehbare Konfigurationsparameter Namensdienst

<table><tr><th>
ReferenzID

</th><th>
Belegung

</th><th>
Bedeutung

</th></tr><tr><td>
DNS_SERVERS_

BESTANDSNETZE

</td><td>
Liste von IP-Adressen der DNS-Servern je Domäne je freigegebenem
angeschlossenen Netz des Gesundheitswesens mit WANDA Basic

</td><td>
Optional, abhängig von der Umsetzung von GS-A_3829-01:  
 Liste von DNS-Servern
je Domain eines dieser freigegebenen Netze.

</td></tr></table>

**[\<=]**

Da der Highspeed-Konnektor keinen VPN-Zugangsdienst nutzt, verwendet er auch
keine CRL.

**TIP1-A_4701-02 - TUC_KON_035 „Zertifikatsdienst initialisieren“**

In der Bootup-Phase MUSS der Konnektor den Zertifikatsdienst durch Aufruf des
TUC_KON_035 „Zertifikatsdienst initialisieren“ initialisieren.

Tabelle4: TAB_KON_772 TUC_KON_035 „Zertifikatsdienst initialisieren“

<table><tr><td>
Element

</td><td>
Beschreibung

</td></tr><tr><td>
Name

</td><td>
TUC_KON_035 „Zertifikatsdienst initialisieren“

</td></tr><tr><td>
Beschreibung

</td><td>
Der TUC beschreibt den gesamten Ablauf der Initialisierung des TrustStore im
Rahmen der betrieblichen Prozesse: Prüfung der Aktualität, Integrität und
Authentizität der Einträge im TrustStore.

</td></tr><tr><td>
Auslöser

</td><td>
 ---> UL

</td></tr><tr><td>
Vorbedingungen

</td><td>
keine

</td></tr><tr><td>
Eingangsdaten

</td><td>
keine

</td></tr><tr><td>
Komponenten

</td><td>
Konnektor

</td></tr><tr><td>
Ausgangsdaten

</td><td>
 ---> UL

</td></tr><tr><td>
Nachbedingungen

</td><td>
Keine

</td></tr><tr><td>
Standardablauf

</td><td>
Für den übergebenen Status der Initialisierung des TrustStore werden folgende
Schritte durchgeführt:

 ---> OL

</td></tr><tr><td>
Varianten/  
Alternativen

</td><td>
Keine

</td></tr><tr><td>
Fehlerfälle

</td><td>
Keine

</td></tr><tr><td>
Nichtfunktionale Anforderungen

</td><td>
Keine

</td></tr><tr><td>
Zugehörige  
Diagramme

</td><td>
Keine

</td></tr></table>

Tabelle5: TAB_KON_605 Fehlercodes TUC_KON_035 „Zertifikatsdienst
initialisieren“

<table><tr><th>
Fehlercode

</th><th>
ErrorType

</th><th>
Severity

</th><th>
Fehlertext

</th></tr><tr><td colspan="4">
Neben den Fehlercodes der aufgerufenen technischen Use Cases können keine
weiteren Fehlercodes auftreten.

</td></tr></table>

**[\<=]**

Da der Konnektor keinen direkten Zugang zum Internet hat, entfällt der
TSL-Download aus dem Internet.

**TIP1-A_4693-03 - TUC_KON_032 „TSL aktualisieren”**

Der Konnektor MUSS den technischen Use Case TUC_KON_032 „TSL aktualisieren“
umsetzen.

Tabelle6: TAB_KON_766 TUC_KON_032 „TSL aktualisieren“

<table><tr><td>
Element

</td><td>
Beschreibung

</td></tr><tr><td>
Name

</td><td>
TUC_KON_032 „TSL aktualisieren“

</td></tr><tr><td>
Beschreibung

</td><td>
Dieser TUC prüft die Aktualität der TSL und initialisiert ggf. den
TSL-spezifischen Bereich des TrustStores neu. Zusätzlich wird bei einem
Wechsel des TI-Vertrauensankers das neue TSL-Signer-CA-Zertifikat in einem
sicheren Speicherort im Konnektor hinterlegt. Im Fall der Veröffentlichung
eines CVC-Root-CA-Zertifikats werden das CVC-Root-CA-Zertifikat und die
Cross-CV-Zertifikate aus der TSL in den Truststore eingestellt.

</td></tr><tr><td>
Auslöser

</td><td>
 ---> UL

</td></tr><tr><td>
Vorbedingungen

</td><td>
 ---> UL

</td></tr><tr><td>
Eingangsdaten

</td><td>
 ---> UL

</td></tr><tr><td>
Komponenten

</td><td>
Konnektor

</td></tr><tr><td>
Ausgangsdaten

</td><td>
 ---> UL

</td></tr><tr><td>
Nachbedingungen

</td><td>
 ---> UL

</td></tr><tr><td>
Standardablauf

</td><td>
 ---> OL

</td></tr><tr><td>
Varianten/  
Alternativen

</td><td>
(1) Wird die importedTSL manuell übergeben (in den Eingangsdaten), so wird
diese statt des Downloads verwendet und an TUC_PKI_001 übergeben. Innerhalb
der PKI TUCs findet dann kein Download der TSL statt.  
(1) Wird durch den
von TUC_PKI_001 aufgerufenen TUC_PKI_013 „Import neuer Vertrauensanker“ ein
neuer TI-Vertrauensanker (ein neues TSL-Signer-CA-Zertifikat) in der
importedTSL gefunden, so wird dieser, wie dort beschrieben, extrahiert und in
einem sicheren Speicherort gespeichert. Vor Erreichen des Aktivierungsdatums
werden die TSLs ausschließlich mit dem alten TSL-Signer-Zertifikat signiert.
Ab dem Aktivierungsdatum werden die TSLs mit einem TSL-Signer-Zertifikat
signiert, das von der neuen TSL-Signer-CA ausgestellt wurde.

</td></tr><tr><td>
Fehlerfälle

</td><td>
(1) Tritt beim manuellen Import der Datei ein Fehler auf, wird TUC_KON_256 { 

       topic = „CERT/TSL/IMPORT“;  
       eventType = Op; 

       severity = Error;  
       parameters =
„$Fehlerbeschreibung“;  
       doLog = true;  
       doDisp =
false }  
ausgelöst. Fehlercode 4128.  
(1) Tritt beim periodischen Update
der TSL beim Aufruf des TUC_PKI_001 oder eines durch ihn aufgerufenen TUCs ein
Fehler auf, geht der Konnektor in den Betriebszustand
EC_TSL_Update_Not_Successful. Der Konnektor geht erst in den Betriebszustand
EC_TSL_Update_Not_Successful, wenn weder der Downloadversuch aus der TI noch
der Downloadversuch aus dem Internet erfolgreich war. Die vorhandenen
TSL-Vertrauensanker werden weiter verwendet. Fehlercode 4127.

</td></tr><tr><td>
Nichtfunktionale Anforderungen

</td><td>
keine

</td></tr><tr><td>
Zugehörige Diagramme

</td><td>
keine

</td></tr></table>

Tabelle7: TAB_KON_598 Fehlercodes TUC_KON_032 „TSL aktualisieren“

<table><tr><th>
Fehlercode

</th><th>
ErrorType

</th><th>
Severity

</th><th>
Fehlertext

</th></tr><tr><td colspan="4">
Neben den Fehlercodes der aufgerufenen technischen Use Cases können folgende
weitere Fehlercodes auftreten:

</td></tr><tr><td>
4127

</td><td>
Security

</td><td>
Error

</td><td>
Import der TSL-Datei fehlgeschlagen

</td></tr><tr><td>
4128

</td><td>
Technical

</td><td>
Error

</td><td>
der manuelle Import der TSL-Datei schlägt fehl

</td></tr></table>

**[\<=]**

Da die Einschränkung des Zugriffs auf die Komponenten in der VAU im Falle eines
Hardwaredefekts eine schnelle Reparatur durch den Betreiber verbietet
(A_21987), sollte die Verfügbarkeit des Highspeed-Konnektors durch Redundanz
abgesichert sein.

**A_21884 - Redundanter Aufbau Highspeed-Konnektor**

Der Anbieter des Highspeed-Konnektors SOLL die Lösung redundant betreiben,
damit bei Ausfall einer technischen Komponente die - zwecks Betreiberausschluss
notwendigerweise durch den Hersteller vorzunehmende - technische Wartung nicht
zu erhöhten Ausfallzeiten führt. **[\<=]**

**A_21854 - Nutzung des VSDM-Intermediärs**

Der Konnektor MUSS über einen Intermediär auf die VSDM-Dienste zugreifen.
**[\<=]**

Die Anforderungen zum Ex- und Import werden angepasst, um die Verwendung von
Standardkomponenten zu erleichtern:

**TIP1-A_4814-02 - Export- Import von Konfigurationsdaten**

Der Administrator MUSS die gesamten Konfigurationsdaten des Anwendungskonnektors
ex- und importieren können. Dazu gehören die Konfigurationsparameter des
Konnektors, die persistenten Daten wie im Informationsmodell des Konnektors
(Tabelle TAB_KON_507 Informationsmodell Entitäten) definiert  und die
Pairing Informationen der Kartenterminals.Für die Konfigurationsdaten des
Netzkonnektors MUSS eine Möglichkeit zur Sicherung und Wiederherstellung
existieren.Der Konnektor MUSS sicherstellen, dass der Exportvorgang nur von
einem am Konnektor angemeldeten User mit mindestens der Rolle Administrator
ausgelöst werden kann.Der Konnektor MUSS sicherstellen, dass der Importvorgang
nur von einem am Konnektor angemeldeten User mit der Rolle Super-Administrator
ausgelöst werden kann.Sowohl Ex- als auch Import MÜSSEN protokolliert werden
durch TUC_KON_271 „Schreibe Protokolleintrag“ {        topic =
„MGM/CONFIG_EXIMPORT“;    eventType = Op;    severity =
Info;    parameters =
(„User=$AdminUsername,                            Mode=[Export/Import]“)}.
**[\<=]**

**A_22338 - Tägliche Aktualisierung der TSL**

Der Highspeed-Konnektor MUSS täglich durch Aufruf von TUC_KON_032 die TSL
aktualisieren **[\<=]**

### 5.1.1 Schnittstellen

Der Highspeed-Konnektor stellt für den LE exakt die selben Schnittstellen
bereit wie ein Einbox-Konnektor. Dies betrifft also die SOAP- und
LDAP-Operationen. Der Netzwerkverkehr zu offenen Diensten, kann durch den
Highspeed-Konnektor oder direkt über den SZZP (light) geroutet werden. Für
den Administrator gibt es die Administrationsschnittstelle wie beim
Einbox-Konnektor. Zusätzlich gibt es eine Administrationsschnittstelle nur
für den Hersteller die zur Kopplung mit dem SZZP und ggf. dem HSM dient (siehe
A_21883). Zudem ist es für den Highspeed-Konnektor gestattet die gSMC-Ks
(sofern kein HSM verwendet wird) und vom LE dafür freigegebene SMC-Bs lokal
per USB-Kartenleser anzubinden, sofern dies innerhalb der VAU geschieht. Es
sind keine weiteren Schnittstellen gestattet.

**A_21988 - Highspeed-Konnektor - Keine zusätzlichen Schnittstellen**

Der Highspeed-Konnektor DARF NICHT Schnittstellen besitzen, die ein
Einbox-Konnektor nicht auch besitzt, sofern diese nicht explizit gefordert oder
erlaubt sind (bspw. ggf. USB-Kartenleser). Dies betrifft auch Zugänge die ggf.
durch die Server-Hardware-Basis grundsätzlich gegeben wären. Der
Highspeed-Konnektor verhält sich nach außen in der Art seiner Schnittstellen
somit wie ein Einbox-Konnektor. **[\<=]**

**A_22039 - Highspeed-Konnektor: Lokaler Kartenleser für gSMC-K und SMC-B
möglich**

Der Highspeed-Konnektor KANN Karten vom Typ gSMC-K und SMC-B über einen lokalen
Kartenleser (USB) anbinden. Eine PIN-Eingabe kann dann über die
Administrationsoberfläche des Konnektors erfolgen. PINs dürfen im Konnektor
jedoch nicht gespeichert oder gecacht werden. **[\<=]**

**A_22040 - Highspeed-Konnektor: Absicherung Anbindung lokaler Kartenleser**

Der Highspeed-Konnektor MUSS, wenn lokale Kartenleser (USB) verwendet werden,
diese innerhalb der VAU anbinden (kein Zugriff des Betreibers auf den
USB-Anschluss und den Kartenleser). **[\<=]**

### 5.1.2 Sichere Trennung von logischen Konnektorinstanzen

Der Highspeed-Konnektor kann mehrere einzelne Konnektorinstanzen virtualisieren.
Die Virtualisierung muss dazu genutzt werden,  Wechselwirkung zwischen den
Instanzen zu unterbinden. Das gilt innerhalb des Highspeed-Konnektors für die
Virtualisierung einzelner Dienste als auch bei der Adressierung vollständiger
Konnektorinstanzen durch den Nutzer. Solch eine Virtualisierung muss dazu
genutzt werden, die Mandantentrennung abzusichern.

**A_22041 - Highspeed-Konnektor: Sichere Trennung virtueller Instanzen**

Der Highspeed-Konnektor MUSS virtuelle Instanzen von Konnektoren sicher
voneinander trennen, sodass zum einen kein Zugriff von einer Instanz auf die
andere möglich ist und zum anderen eine feste Zuordnung von Mandanten zu
Konnektorinstanzen durchgesetzt wird. **[\<=]**

**TIP1-A_4820-02 - HSK: Instanzen erstellen und löschen**

Der HSK, der virtuelle Instanzen unterstützt, MUSS über eine
Administratorrolle verfügen, die eine virtuelle Instanz in einem HSK löschen
und erstellen kann. Der HSK MUSS es ermöglichen, diese Rolle von der
Administration innerhalb einzelner HSK-Instanzen zu trennen.Beim Löschen einer
HSK-Instanz muss die gesamte Konfiguration dieser Instanz und alle internen
Speicher, Protokolle inklusiv der Sicherheitsprotokolle sowie der
Vertrauensraum inklusiv der  CERT_IMPORTED_CA_LIST gelöscht werden.Das
Löschen der HSK-Instanz MUSS zusammen mit dem username des auslösenden
Administrators im HSK protokolliert werden.Beim Erstellen einer HSK-Instanz
MUSS beim Start der Instanz der aktuelle Vertrauensraum eingebunden werden.
**[\<=]**

**A_23159 - Prozess zum Erstellen und Löschen von HSK-Instanzen**

Der Betreiber des HSK MUSS einen Prozess etablieren, der den Auftrag zum
Erstellen und Löschen einer HSK-Instanz, dessen Prüfung und dessen Umsetzung
mit den dabei beteiligten Personen dokumentiert. Der Prozess muss geeignet
sein, die unberechtigte Löschung von Instanzen zu verhindern. **[\<=]**

### 5.1.3 Eingeschränkte Nutzung des KSR

Der Highspeed-Konnektor nutzt den KSR um Updates für Kartenterminals zu laden
und auf angeschlossenen Kartenterminals zu installieren. Die Software des
Highspeed-Konnektors wird nicht über den KSR aktualisiert, sondern durch
Upload am Highspeed-Konnektor. Der Highspeed-Konnektor kann in Teilen
aktualisiert werden, bspw. das zugrundeliegende Betriebssystem oder die
Virtualisierungsfunktionalität unabhängig vom eigentlichen
Anwendungskonnektor. In jedem Fall muss die Integrität und Authentizität der
Highspeed-Konnektor-Updates vor deren Anwendung geprüft werden.

**TIP1-A_4832-03 - TUC_KON_280 „Konnektoraktualisierung durchführen“**

Der Highspeed-Konnektor MUSS den technischen Use Case TUC_KON_280
„Konnektoraktualisierung durchführen“ umsetzen.

Tabelle8: TAB_KON_664 – TUC_KON_280 „Konnektoraktualisierung durchführen“

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
Name

</td><td>
TUC_KON_280 „Konnektoraktualisierung durchführen“

</td></tr><tr><td>
Beschreibung

</td><td>
Dieser TUC aktualisiert den Konnektor oder Teile des Konnektors mit einem
Update, dessen Update-Dateien direkt übergeben wurden

</td></tr><tr><td>
Auslöser

</td><td>
 ---> UL

</td></tr><tr><td>
Vorbedingungen

</td><td>
</td></tr><tr><td>
Eingangsdaten

</td><td>
 ---> UL

</td></tr><tr><td>
Komponenten

</td><td>
Konnektor,

</td></tr><tr><td>
Ausgangsdaten

</td><td>
Keine

</td></tr><tr><td>
Nachbedingungen

</td><td>
Der Konnektor arbeitet basierend auf der übergebenen, im Updatepaket
enthaltenen neuen Version.

</td></tr><tr><td>
Standardablauf

</td><td>
Der Konnektor MUSS das zur Anwendung übergebene Updatepaket wie folgt anwenden:

 ---> OL

</td></tr><tr><td>
Varianten/Alternativen

</td><td>
</td></tr><tr><td>
Fehlerfälle

</td><td>
(



1) Integritätsprüfung eines FirmwareFiles fehlgeschlagen, Fehlercode: 4183

(



2) Firmwaregruppenprüfung fehlgeschlagen, Fehlercode: 4185

(



3a) Interne Aktualisierung fehlgeschlagen, dann:

          1. Rollback auf vorherige Version

          2. Abbruch mit Fehlercode: 4184

</td></tr><tr><td>
Nichtfunktionale Anforderungen

</td><td>
</td></tr><tr><td>
Zugehörige Diagramme

</td><td>
</td></tr></table>

Tabelle9: TAB_KON_665 Fehlercodes TUC_KON_280 „Konnektoraktualisierung
durchführen“

<table><tr><th>
Fehlercode

</th><th>
ErrorType

</th><th>
Severity

</th><th>
Fehlertext

</th></tr><tr><td colspan="4">
Neben den Fehlercodes der aufgerufenen technischen Use Cases können folgende
weitere Fehlercodes auftreten:

</td></tr><tr><td>
4183

</td><td>
Security

</td><td>
Error

</td><td>
Integritätsprüfung UpdateFiles fehlgeschlagen.

</td></tr><tr><td>
4184

</td><td>
Security

</td><td>
Error

</td><td>
Anwendung der UpdateFiles fehlgeschlagen (\<Details\>).

</td></tr><tr><td>
4185

</td><td>
Security

</td><td>
Error

</td><td>
Firmware-Version liegt außerhalb der gültigen Firmware-Gruppe

</td></tr></table>

**[\<=]**

### 5.2 Betrieblich

Im Rahmen der Anbieter-/Betreiberzulassung muss nachgewiesen werden:

### 5.2.1 Betriebsumgebung

### 5.2.1.1 Initialisierung des Vertrauensraumes

**A_22336 - Initialisierung mit ECC-Vertrauensraum**

Der Hersteller des Highspeed-Konnektors MUSS diesen mit dem ECC-Vertrauensraum
initialisieren. **[\<=]**

Wenn keine gSMC-K verwendet wird, soll der initiale Anker für den
Vertrauensraum auf dem HSM personalisiert werden.

Es gelten diesbezüglich GS-A_4640 und GS-A_4641 aus gemSpec_PKI.

**A_17548-02 - TSL-Signer-CA Zertifikat sicher speichern**

Der Konnektor MUSS den aktuellen TI-Vertrauensanker im sicheren Datenspeicher
speichern. **[\<=]**

### 5.2.1.2 HSM

**TIP1-A_4503-02 - Verpflichtung zur Nutzung von gSMC-K oder HSM**

Der Konnektor MUSS das geheime Schlüsselmaterial zur Geräteidentität
(ID.NK.VPN, ID.AK.AUT, ID.SAK.AUT) und der Rolle SAK (C.SAK.AUTD_CVC) über
Smartcards des Typs gSMC-K gemäß [gemSpec_gSMC-K_ObjSys] oder ein HSM nutzen.
Der Konnektor MUSS mit einer gSMC-K oder einem HSM bestückt sein. Er KANN mit
mehr als einer gSMC-K oder HSM bestückt sein. **[\<=]**

**A_17598-01 - Qualität des HSM**

Die Highspeed-Konnektoren MÜSSEN privates Schlüsselmaterial zu Zertifikaten
der Telematikinfrastruktur in einem HSM, dessen Eignung durch eine
erfolgreiche Evaluierung nachgewiesen wurde, integritätsgeschützt und
vertraulich speichern. Als Evaluierungsschema kommen dabei Common Criteria oder
Federal Information Processing Standard (FIPS) in Frage. Die Prüftiefe MUSS
mindestens (a) FIPS 140-2 Level 3, oder (b) Common Criteria EAL 4 entsprechen. **[\<=]**

Es ist nicht gefordert, das HSM im FIPS-Modus zu betreiben.

**A_21885 - Personalisierung des HSM mit Konnektoridentitäten durch Hersteller**

Der Hersteller des Konnektors MUSS, wenn er ein HSM für die Speicherung der
Konnektoridentitäten verwendet, das HSM mittels sicherer Prozesse und in
seiner gesicherten Produktionsumgebung personalisieren. **[\<=]**

Entsprechend werden relevante Anforderungen zur Personalisierung einer gSMC-K
dem Prüfverfahren Sicherheitsgutachten für den Hersteller des
Highspeed-Konnektors zugeordnet. Im Falle der Nutzung von gSMC-Ks sind diese
Anforderungen mit einer entsprechenden Begründung als "nicht relevant" im
Gutachten zu bewerten.

Die Nutzung eines HSMs für die Identitäten der LEI ist für zukünftige
Versionen des Highspeed-Konnektors angedacht. Aktuell müssen hier weiterhin
SMC-Bs verwendet werden.

**A_22590 - HSK: Kein Abruf von Zertifikatsprofilen C.NK.VPN bei Nutzung HSM**

Der Hersteller des Highspeedkonnektors DARF NICHT Zertifikate mit dem Profil
C.NK.VPN beziehen, wenn er ein HSM statt einer gSMC-K verwendet und das HSM
personalisiert. **[\<=]**

**A_21987 - Zugriff auf die VAU nur durch den Hersteller**

Die VAU des Highspeed-Konnektors MUSS Eingriffe in das System durch andere als
den Hersteller unterbinden. Das betrifft im Besonderen administrative Zugriffe
auf das HSM, die Kopplung des HSM und die Kopplung mit dem SZZP. **[\<=]**

**A_21886 - Feste Kopplung von Konnektor und HSM**

Der Konnektor MUSS, wenn ein HSM verwendet wird, fest kryptographisch mit dem
HSM gekoppelt sein, sodass eine hinsichtlich Vertraulichkeit und Integrität
geschützte, beidseitig authentisierte Verbindung zwischen Konnektor und HSM
besteht und ausschließlich der Konnektor die auf dem HSM gespeicherten
Identitäten nutzen kann. **[\<=]**

### 5.2.1.3 Vertrauenswürdige Ausführungsumgebung

Die VAU dient der datenschutzrechtlich zulässigen und sicheren Verarbeitung von
schützenswerten Klartextdaten (Aktenschlüssel und Kontextschlüssel des
Aktenkontos eines Versicherten) innerhalb des FM ePA.

Die Gesamtheit aus der für eine Klartextverarbeitung erforderlichen
Software, dem für eine Klartextverarbeitung genutzten physikalischen System
sowie den für die Integrität einer Klartextverarbeitung erforderlichen
organisatorischen und physischen Rahmenbedingungen bildet den
Verarbeitungskontext der Vertrauenswürdigen Ausführungsumgebung. 

Zur Vertrauenswürdigen Ausführungsumgebung gehören neben den
Verarbeitungskontexten alle für ihre Erreichbarkeit und betriebliche Steuerung
erforderlichen Komponenten.

Der Verarbeitungskontext grenzt sich von allen weiteren, im betrieblichen
Kontext bei einem Anbieter KTR-Consumer vorhandenen Systemen und Prozessen
dadurch ab, dass die sensiblen Klartextdaten von Komponenten innerhalb des
Verarbeitungskontextes aus erreichbar sind oder sein können, während sie dies
von außerhalb des Verarbeitungskontextes nicht sind. Sensible Daten verlassen
den Verarbeitungskontext ausschließlich gemäß wohldefinierten
(Zugriffs-)Regeln und in verschlüsselter Form.

Die schützenswerten sensiblen Daten sind der Akten- und Kontextschlüssel der
Aktenkonten, für die der KTR zugriffsberechtigt ist.

Die Mehrzahl Verarbeitungskontexte ergibt sich aus der softwaretechnischen
Trennung verschiedener Sitzungen. Somit wird jede Akte in Ihrem eigenen
Verarbeitungskontext genutzt. Physische Maßnahmen bspw. zum Zutrittsschutz
sind hingegen nur einmalig für die gesamte VAU erforderlich, also für jeden
Verarbeitungskontext identisch.

**A_17346-01 - HSK: Verarbeitungskontext der VAU**

Der Verarbeitungskontext des Highspeed-Konnektors MUSS sämtliche physikalischen
Systemkomponenten sowie sämtliche Softwarekomponenten umfassen, deren
Sicherheitseigenschaften sich auf den Schutz der Schlüssel und Medizinischen
Daten eines Versicherten vor Zugriff durch Unbefugte bei ihrer Verarbeitung im
Klartext auswirken können. **[\<=]**

**A_17347-01 - HSK: Verarbeitungskontext der VAU - Keine persistente Speicherung
von Versichertendaten**

Der Verarbeitungskontext des Highspeed-Konnektors DARF Schlüssel und
medizinische Daten eines Versicherten NICHT persistent speichern, auch nicht
verschlüsselt. **[\<=]**

**A_17348-01 - HSK: Verarbeitungskontext der VAU - Akten- und Kontextschlüssel
verlassen VAU nie**

Der Verarbeitungskontext des Highspeed-Konnektors MUSS sicherstellen, dass die
Akten- und Kontextschlüssel der Versicherten die VAU nur
verlassen (unabhängig davon, ob sie verschlüsselt oder unverschlüsselt
sind), wenn sie ans ePA-Aktensystem übermittelt werden und die Übermittlung
zum ePA-Aktensystem in einem sicheren Kanal erfolgt. **[\<=]**

### 5.2.1.4 Ausschluss von nicht autorisierten Zugriffen aus dem Betriebsumfeld

**A_17350-01 - HSK: Isolation der VAU von Datenverarbeitungsprozessen des
Anbieters**

Die VAU des Highspeed-Konnektors MUSS die im Verarbeitungskontext ablaufenden
Datenverarbeitungsprozesse von allen sonstigen Datenverarbeitungsprozessen des
Anbieters/Betreibers trennen und damit gewährleisten, dass der
Anbieter/Betreiber vom Zugriff auf die in der VAU verarbeiteten, 
schützenswerten Daten ausgeschlossen ist. **[\<=]**

**A_17351-01 - HSK: Ausschluss von Manipulationen an der Software der VAU**

Die VAU des Highspeed-Konnektors MUSS die Integrität der eingesetzten Software
schützen und damit insbesondere Manipulationen an der Software durch den
Anbieter/Betreiber ausschließen. **[\<=]**

**A_17352-01 - HSK: Ausschluss von Manipulationen an der Hardware der VAU**

Die VAU des Highspeed-Konnektors MUSS die Integrität der eingesetzten Hardware
schützen und damit insbesondere Manipulationen an der Hardware durch den
Anbieter/Betreiber ausschließen. **[\<=]**

**A_17353-01 - HSK: Kontinuierliche Wirksamkeit des Manipulationsschutzes der
VAU**

Die VAU des Highspeed-Konnektors MUSS den Ausschluss von Manipulationen an der
Hardware und der Software durch den Anbieter/Betreiber mit Mitteln umsetzen,
deren dauerhafte und kontinuierliche Wirksamkeit gewährleistet werden kann.
**[\<=]**

**A_17354-01 - HSK: Kein physischer Zugang des Anbieters zu Systemen der VAU**

Die VAU des Highspeed-Konnektors MUSS mit technischen Mitteln sicherstellen,
dass niemand, auch nicht der Anbieter/Betreiber , während der Verarbeitung
personenbezogener medizinischer Daten Zugriff auf physische Schnittstellen der
Systeme erlangen kann, auf denen eine VAU ausgeführt wird. **[\<=]**

**A_17355-01 - HSK: Nutzdatenbereinigung vor physischem Zugang zu Systemen der
VAU**

Die VAU des Highspeed-Konnektors MUSS mit technischen Mitteln sicherstellen,
dass ein physischer Zugang zu Hardware-Komponenten der Verarbeitungskontexte
nur erfolgen kann, nachdem gewährleistet ist, dass aus ihnen keine Nutzdaten
extrahiert werden können. **[\<=]**

**A_17356-01 - HSK: Löschen aller aktenbezogenen Daten beim Beenden des
Verarbeitungskontextes**

Die VAU des Highspeed-Konnektors MUSS beim Beenden eines Verarbeitungskontextes
sämtliche Daten dieses Verarbeitungskontextes sicher löschen. **[\<=]**

**A_21990 - Kein Zugriff auf SM-B Identitäten und Kopplungs-Geheimnis durch
Betreiber**

Der Highspeed-Konnektor MUSS den Betreiber vom vollen Zugriff auf
SM-B-Identitäten ausschließen. Im Fall einer SMC-B darf der Betreiber nicht
sowohl Zugriff auf die Karte als auch Wissen der PIN haben. Im Fall einer
Speicherung von SM-B-Identitäten in einem HSM darf der Betreiber nicht das
HSK-HSM-Kopplungsgeheimnis kennen. **[\<=]**

### 5.2.1.5 Unabhängigkeit von dem Betreiber des Aktensystems

**A_21248-02 - Anbieter HSK - Unabhängigkeit des Betreibers eines
ePA-Aktensystems vom Betreiber eines HSK**

Der Anbieter des ePA-Aktensystems und der Anbieter des HSK MÜSSEN dafür Sorge
tragen, dass ihr beauftragter Betreiber für das ePA-Aktensystem unabhängig
vom beauftragten Betreiber des Highspeed-Konnektors ist, d.h. es sind
mindestens jeweils eigenständige Rechtspersönlichkeiten mit eigenständigen
operativen Geschäfts- und Betriebsführungen und es ist eine strikte
Vermeidung von Personenidentitäten bzw.
Doppelrollen in den Funktionen Geschäftsführung, leitende Mitarbeiter und
Zugangsberechtigte zum Betriebsort des Highspeed-Konnektor bzw. des
ePA-Aktensystems gewährleistet. **[\<=]**

### 5.2.1.6 Anforderungen aus gemSpec_DS_Anbieter

Grundsätzlich ist der Betrieb des Highspeed-Konnektors in einem Krankenhaus
oder einer großen Einrichtung vergleichbar mit dem Betrieb vieler
Einbox-Konnektoren, die in der selben Umgebung auch direkt von der Einrichtung,
bzw. ihrem Dienstleister betrieben werden. Es erfolgt somit weiterhin ein
Betrieb des (Highspeed-)Konnektors durch die Leistungserbringerinstitution.
Daher wird trotz der notwendigen Anbieterzulassung für den Anbieter/Betreiber
des Highspeed-Konnektors ein nur geringer Umfang der Anforderungen zur
betrieblichen Sicherheit gefordert. Dieser umfasst hauptsächlich die
Herstellung von direkten Kommunikationswegen mit dem koordinierenden ISMS und
Meldungen von Vorfällen an dieses.

### 5.2.2 ITSM Integration

Der Betreiber des Highspeed-Konnektors nimmt am ITSM teil. Da der Betreiber des
Highspeed-Konnektors keinen Service für andere ITSM-Teilnehmer anbietet,
gelten nur ein Teil der Anforderungen (siehe Anbietertypsteckbrief).

### 5.2.2.1 Mitwirkungspflichten ITSM

Für den Betreiber des Highspeed-Konnektors ergeben sich Mitwirkungspflichten am
ITSM.

Dafür werden Änderungen ander Tabelle Tab_KPT_Betr_TI_002 Mitwirkungspflichten
der TI-ITSM-Teilnehmer und zusätzlich an der Tabelle Tab_KPT_Betr_TI_003
Mitwirkungsverpflichtung im TI-ITSM aus [gemKPT_Betr] vorgenommen.

### 5.2.3 Auftragsdatenverarbeitung/AVV

**A_21989 - Auftragsdatenverarbeitung zwischen LEI und Anbieter
Highspeed-Konnektor**

Der Anbieter des HSK MUSS, wenn er nicht der nutzende Leistungserbringer ist,
mit jeder nutzenden LEI eine Auftragsdatenverarbeitung vertraglich in Form
eines AVV nach DSGVO regeln. Diese vertragliche Regelung muss insbesondere auch
umfassen, dass der Anbieter oder ein von ihm beauftragter Betreiber nicht auf
die fachlichen Anwendungsfälle (SOAP-Operationen) des Konnektors und seiner
Fachmodule zugreift. **[\<=]**

### 5.2.4 Weitere Betriebliche Anforderungen

Der Highspeed-Konnektor wird im Gegensatz zum Einbox-Konnektor nicht über den
VPN-Zugangsdienst, sondern über den SZZP-light+ an die TI angebunden. In
dieser Anbindungsvariante wird dem Highspeed-Konnektor keine DNS-Informationen
zu den NTP-Servern in der TI bereitgestellt. Deshalb muss der
Highspeed-Konnektor die Möglichkeit der manuellen Konfiguration über eine
entsprechende Konfigurationsoberfläche bereitstellen.

**TIP1-A_4793-02 - Konfigurierbarkeit des Konnektor NTP-Servers
(Highspeed-Konnektor)**

Der Administrator MUSS die in TAB_KON_643-HSK aufgelisteten Parameter über die
Managementschnittstelle konfigurieren können.

Tabelle10: TAB_KON_643-HSK Konfiguration des Konnektor NTP-Servers

<table><tr><th>
ReferenzID

</th><th>
Belegung

</th><th>
Bedeutung

</th></tr><tr><td>
NTP_TIMEZONE

</td><td>
Zeitzone

</td><td>
Der Administrator MUSS die Zeitzone des Konnektors einstellen können.

Default-Wert: Central European Time/Mitteleuropäische Zeit (CET/MEZ)

</td></tr><tr><td>
NTP_TIME

</td><td>
Zeit

</td><td>
Der Administrator MUSS die Zeit des Konnektors (NTP_TIME) über die
Managementschnittstelle manuell einstellen können.

</td></tr><tr><td>
NTP_SERVER_

ADDR

</td><td>
IP-Adressen

</td><td>
Die Adressen des primären und sekundären Stratum-2-Zeitserver der zentralen
TI-Plattform für die Synchronisation mit dem NTP-Server des Konnektors.

</td></tr></table>

**[\<=]**

**TIP1-A_4795-02 - TUC_KON_352 „Initialisierung Zeitdienst“
(Highspeed-Konnektor)**

DerHighspeed-Konnektor MUSS in der Bootup-Phase TUC_KON_352 "Initialisierung
Zeitdienst" durchlaufen.

Tabelle11: TAB_KON_644-HSK – TUC_KON_352 „Initialisierung Zeitdienst“

<table><tr><td>
Element

</td><td>
Beschreibung

</td></tr><tr><td>
Name

</td><td>
TUC_KON_352 „Initialisierung Zeitdienst“

</td></tr><tr><td>
Beschreibung

</td><td>
Der Highspeed-Konnektor muss zum Bootup den konnektoreigenen NTP-Server mit
einem NTP-Server der zentralen TI-Plattform synchronisieren. falls
MGM_LU_ONLINE=Enabled.

</td></tr><tr><td>
Anwendungsumfeld

</td><td>
Synchronisierung der Systemzeit zur Startzeit

</td></tr><tr><td>
Eingangsanforderung

</td><td>
Keine

</td></tr><tr><td>
Auslöser

</td><td>
 ---> UL

</td></tr><tr><td>
Vorbedingungen

</td><td>
Verbindung zum VPN-Konzentrator zur TI muss aufgebaut sein

</td></tr><tr><td>
Eingangsdaten

</td><td>
NTP-Server der zentralen TI-Plattform

</td></tr><tr><td>
Komponenten

</td><td>
Highspeed-Konnektor

</td></tr><tr><td>
Ausgangsdaten

</td><td>
Keine

</td></tr><tr><td>
Standardablauf

</td><td>
Falls MGM_LU_ONLINE=Enabled:

 ---> UL

</td></tr><tr><td>
Varianten/Alternativen

</td><td>
Keine

</td></tr><tr><td>
Fehlerfälle

</td><td>
4177: Der NTP-Server des Highspeed-Konnektors empfängt keine Systemzeit

</td></tr><tr><td>
Nichtfunktionale Anforderungen

</td><td>
Keine

</td></tr><tr><td>
Zugehörige Diagramme

</td><td>
Keine

</td></tr></table>

Tabelle12: TAB_KON_645-HSK Fehlercodes TUC_KON_352 „Initialisierung
Zeitdienst“

<table><tr><th>
Fehlercode

</th><th>
ErrorType

</th><th>
Severity

</th><th>
Fehlertext

</th></tr><tr><td>
4177

</td><td>
Technical

</td><td>
Warning

</td><td>
Der NTP-Server des Highspeed-Konnektors konnte nicht synchronisiert werden.

</td></tr></table>

**[\<=]**

**TIP1-A_5152-01 - Aktualisieren der Infrastrukturinformationen aus der TI**

Der Betreiber des Highspeed-Konnektors MUSS einen Prozess etablieren, mit
dem Änderungen in der Bestandsnetze.xml innerhalb von einem Arbeitstag
umgesetzt werden können. **[\<=]**

Dieser betriebliche Prozess sollte vom Highspeed-Konnektor folgendermaßen
unterstützt werden:

**A_22571 - Benachrichtigung und Bereitstellung der Bestandsnetze.xml**

Der Highspeed-Konnektor KANN eine Benachrichtigung des Betreibers über eine
neue Bestandsnetze.xml und die Bereitstellung der heruntergeladenen
Bestandsnetze.xml für den Betreiber umsetzen. **[\<=]**

### 6 Test Konzept

Für den Highspeed-Konnektor gelten neben den gewohnten Anforderungen aus
gemKPT_Test, die sich an dezentrale Komponenten richten, weitere Anforderungen,
die sich ergeben, wenn der Highspeed-Konnektor in RU und TU nicht physikalisch
in der gematik verfügbar ist.

### 6.1 Zugang und Verfügbarkeit

Der Hersteller eines Highspeedkonnektors muss der gematik mindestens fünf
(virtuelle) Instanzen des Highspeedkonnektors für Testzwecke exklusiv zur
Verfügung stellen. Einzelne Hardwarekomponenten (z.B. SZZP, HSM) können mit
anderen Instanzen geteilt werden, wenn eine logische Trennung erfolgt. Wenn
unterschiedliche Versionen testrelevant sind, sollen hierfür eigene virtuelle
Instanzen bereitgestellt werden. Eine Instanz des Highspeedkonnektors muss mit
der TU der TI verbunden sein. Die Nutzung eines Intermediärs muss
herstellerseitig gewährleistet werden. Die vier weiteren Instanzen müssen mit
dem SZZP der lokalen Testumgebung der gematik verbunden werden.

Der Hersteller muss der gematik einen VPN Zugang zum Highspeedkonnektor
ermöglichen, über den die Clientsystemschnittstellen, die
Admin-Schnittstellen und die Kartenterminal-Schnittstellen zugänglich sind.
Für die vier Instanzen des Highspeedkonnektors, welche mit dem SZZP der
lokalen Testumgebung der gematik verbunden sind, muss auch der ganze
Netzwerkverkehr Richtung TI (über den SZZP) über den VPN Tunnel zur gematik
ermöglicht werden.

Der Hersteller muss der gematik einen Admin-Zugang ermöglichen, über den die
Konfigurations- und Überwachungstätigkeiten des Betreibers und DVOs möglich
sind, insbesondere zur Einrichtung von Clientsystemen und Kartenterminals sowie
Logeinsichten. Außerdem muss der Hersteller es der gematik ermöglichen,
Dateien (z.B. TSL, BNetzA-VL, Zertifikate) über die Adminoberfläche des
Highspeedkonnektors einzuspielen.

Die REST-Schnittstelle zur Administration des Highspeedkonnektors, muss der
gematik offengelegt und zugängig gemacht werden.

**A_22577 - Highspeed-Konnektor: Bereitstellung TU-Anbindung**

Der Hersteller eines Highspeed-Konnektors MUSS die Anbindung seines Produktes
an die TU über einen SZZP inklusive vollständiger Erreichbarkeit aller
Dienste bereitstellen. **[\<=]**

**A_22574 - Zugang zum Highspeed Konnektor**

Der Hersteller eines Highspeed-Konnektors MUSS nach der Anbindung seines
Produktes in der TU dem Test der gematik einen Zugang auf die
Managementschnittstelle zu seinem Produkt einrichten. **[\<=]**

**TIP1-A_2805 - Zeitnahe Anpassung von Produktkonfigurationen**

Der Hersteller oder Anbieter von Produkten MUSS sicherstellen, dass in der
Testumgebung die Produkte (außer Smartcards) sich in ihren Konfigurationen
zeitnah (möglichst kleiner 1 Arbeitstag) anpassen lassen. **[\<=]**

### 6.2 Logging

**TIP1-A_7330 - Tracedaten von echten Außenschnittstellen**

Die Testdurchführende Instanz SOLL seine eigenverantwortlichen Tests an den
Außenschnittstellen des Testobjekts und nicht an internen Loopback Devices
durchführen. **[\<=]**

**TIP1-A_7331 - Bereitstellung von Tracedaten an Außenschnittstelle**

Die Testdurchführende Instanz SOLL bei eigenverantwortlichen Tests an denen an
der Außenschnittstellen des Produkts Daten transferiert werden der Gematik
einen Mitschnitt zur Verfügung stellen, der die folgenden Punkte erfüllt:

• vollständig sein (komplette Paketgröße und gesamte MTU-Size)

• tatsächlichen Daten (insbesondere Messdaten, wie z. B. Zeitstempel)
enthalten

• ein auswertbares Format, (z. B. pcap oder pcapng) haben

• und bei Mitschnitt verschlüsselter Protocol-Layer (z.B. TLS-Layer) und
Nutzung eines Simulators als Peer, das Mastersecret als separate Datei
bereitstellen. **[\<=]**

### 6.3 Interoperabilität

**TIP1-A_6529 - Produkttypen: Mindestumfang der Interoperabilitätsprüfung**

Die testdurchführende Instanz (TDI) MUSS zum Nachweis der Interoperabilität
alle für das jeweilige Produkt relevanten anwendungsfallbasierten Tests mit
der Mindestanzahl von Produkten gemäß Tabelle 13: Tab_Test_033 Mindestumfang
der Interoperabilitätsprüfung durchführen. **[\<=]**

Es werden Änderungen ander Tabelle Tab_Test_033 Mindestumfang der
Interoperabilitätsprüfung aus [gemKPT_Test] vorgenommen.

![Img-001][Img-001]

### 7 Anhang A – Verzeichnisse

### 7.1 Abkürzungen

<table><tr><th>
Kürzel

</th><th>
Erläuterung

</th></tr><tr><td>
HSK

</td><td>
Highspeed-Konnektor

</td></tr><tr><td>
KTR

</td><td>
Kostenträger

</td></tr><tr><td>
AVV

</td><td>
Auftragsverarbeitungsvertrag (AV-Vertrag)

</td></tr><tr><td>
LEI

</td><td>
Leistungserbringerinstitution

</td></tr><tr><td>
VAU

</td><td>
Vertrauenswürdige Ausführungsumgebung

</td></tr><tr></tr></table>

### 7.2 Referenzierte Dokumente

### 7.2.1 Dokumente der gematik

Die nachfolgende Tabelle enthält die Bezeichnung der in dem vorliegenden
Dokument referenzierten Dokumente der gematik zur Telematikinfrastruktur.

<table><tr><td>
[Quelle]

</td><td>
Herausgeber: Titel

</td></tr><tr><td>
[gemGlossar]

</td><td>
gematik: Glossar der Telematikinfrastruktur

</td></tr><tr><td>
gemSpec_DS_Anbieter

</td><td>
gematik: Spezifikation Datenschutz- und Sicherheitsanforderungen der TI an
Anbieter

</td></tr><tr><td>
[gemSpec_gSMC-K_ObjSys]

</td><td>
gematik: Spezifikation der gSMC-K Objektsystem

</td></tr><tr><td>
[gemKPT_Betr]

</td><td>
gematik: Betriebskonzept Online-Produktivbetrieb

</td></tr><tr><td>
[gemKPT_Test]

</td><td>
gematik: Testkonzept der TI

</td></tr></table>

### 7.2.2 Weitere Dokumente

<table><tr><td>
[Quelle]

</td><td>
Herausgeber (Erscheinungsdatum): Titel

</td></tr><tr><td>
</td><td>
</td></tr><tr><td>
</td><td>
</td></tr></table>

### 8 Anhang B – Anmerkungen aus der Industrie

\< Hier können Anmerkungen beispielsweise als nummerierte Liste aufgezählt
werden. \>

### 9 Anhang C – Offene Punkte, Fragen

### 9.1 <offener Punkt oder Frage>





[Dokumentinformationen]: #dokumentinformationen
[Inhaltsverzeichnis]:    #inhaltsverzeichnis
[1]:                     #1-einordnung-des-dokuments
[1.1]:                   #11-zielsetzung
[1.2]:                   #12-zielgruppe
[1.3]:                   #13-abgrenzungen
[1.4]:                   #14-methodik
[1.4.1]:                 #141-epic-und-user-story
[1.4.2]:                 #142-anforderungen
[2]:                     #2-epic-und-user-story
[2.1]:                   #21-stb-169-highspeed-konnektor-20
[2.1.1]:                 #211-betrieb-auf-standard-hardwareablaufumgebungen
[2.1.2]:                 #212-breitband-zugang-zur-ti
[2.1.3]:                 #213-leistungsfähiges-modul-für-identitäten
[3]:                     #3-einordnung-in-die-telematikinfrastruktur
[4]:                     #4-technisches-konzept
[4.1]:                   #41-anbindung-über-szzp-an-die-ti
[4.2]:                   #42-sicherheitsnachweis
[4.2.1]:                 #421-hersteller
[4.2.1.1]:               #4211-sichere-software-entwicklung
[4.2.2]:                 #422-anbieterbetreiber
[5]:                     #5-spezifikation
[5.1]:                   #51-produkteigenschaften-funktional-und-sicherheit
[5.1.1]:                 #511-schnittstellen
[5.1.2]:                 #512-sichere-trennung-von-logischen-konnektorinstanzen
[5.1.3]:                 #513-eingeschränkte-nutzung-des-ksr
[5.2]:                   #52-betrieblich
[5.2.1]:                 #521-betriebsumgebung
[5.2.1.1]:               #5211-initialisierung-des-vertrauensraumes
[5.2.1.2]:               #5212-hsm
[5.2.1.3]:               #5213-vertrauenswürdige-ausführungsumgebung
[5.2.1.4]:               #5214-ausschluss-von-nicht-autorisierten-zugriffen-aus-dem-betriebsumfeld
[5.2.1.5]:               #5215-unabhängigkeit-von-dem-betreiber-des-aktensystems
[5.2.1.6]:               #5216-anforderungen-aus-gemspec_ds_anbieter
[5.2.2]:                 #522-itsm-integration
[5.2.2.1]:               #5221-mitwirkungspflichten-itsm
[5.2.3]:                 #523-auftragsdatenverarbeitungavv
[5.2.4]:                 #524-weitere-betriebliche-anforderungen
[6]:                     #6-test-konzept
[6.1]:                   #61-zugang-und-verfügbarkeit
[6.2]:                   #62-logging
[6.3]:                   #63-interoperabilität
[7]:                     #7-anhang-a-–-verzeichnisse
[7.1]:                   #71-abkürzungen
[7.2]:                   #72-referenzierte-dokumente
[7.2.1]:                 #721-dokumente-der-gematik
[7.2.2]:                 #722-weitere-dokumente
[8]:                     #8-anhang-b-–-anmerkungen-aus-der-industrie
[9]:                     #9-anhang-c-–-offene-punkte-fragen
[9.1]:                   #91-<offener-punkt-oder-frage>
[Img-001]:               gemF_Highspeed-Konnektor_V1.1.0.attachments/8479946686378319599.PNG
[Tbl-001]:               #Tbl-001 (&93834802601336)
[Tabelle-1]:             #Tabelle-1 (&93834811838192)
[Tabelle-2]:             #Tabelle-2 (&93834765154816)
[Tabelle-3]:             #Tabelle-3 (&93834793827224)
[Tabelle-4]:             #Tabelle-4 (&93834793845168)
[Tabelle-5]:             #Tabelle-5 (&93834799843008)
[Tabelle-6]:             #Tabelle-6 (&93834799856736)
[Tabelle-7]:             #Tabelle-7 (&93834810785704)
[Tabelle-8]:             #Tabelle-8 (&93834810842152)
[Tabelle-9]:             #Tabelle-9 (&93834772279512)
[Tabelle-10]:            #Tabelle-10 (&93834802308288)
[Tabelle-11]:            #Tabelle-11 (&93834802329528)
[Tabelle-12]:            #Tabelle-12 (&93834783624880)
[Tbl-014]:               #Tbl-014 (&93834768040312)
[Tbl-015]:               #Tbl-015 (&93834768056120)
[Tbl-016]:               #Tbl-016 (&93834768777168)
[FIPS]:                  https://de.wikipedia.org/wiki/Federal_Information_Processing_Standard (&93834799933560)
