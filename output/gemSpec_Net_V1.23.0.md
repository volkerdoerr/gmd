
Elektronische Gesundheitskarte und Telematikinfrastruktur

### Übergreifende SpezifikationNetzwerk

- Klassifizierung: öffentlich
- Referenzierung: gemSpec_Net
- Revision: 566842
- Stand: 16.12.22
- Status: freigegeben
- Version: 1.23.0

### Dokumentinformationen

Änderungen zur Vorversion

Anpassungen des vorliegenden Dokumentes im Vergleich zur Vorversion können Sie
der nachfolgenden Tabelle entnehmen.

Bitte beachten Sie die Hinweise zur Einführung der Benennungen 'WANDA Basic'
und 'WANDA Smart' (siehe Dokumentenhistorie).

Dokumentenhistorie

 ---> TABLE

### Inhaltsverzeichnis

- [Dokumentinformationen]
- [Inhaltsverzeichnis]
- [1] Einordnung des Dokuments
  - [1.1] Zielsetzung
  - [1.2] Zielgruppe
  - [1.3] Geltungsbereich
  - [1.4] Abgrenzung des Dokuments
  - [1.5] Methodik
- [2] Übergreifende Netzwerk-Festlegungen
  - [2.1] Netztopologie
  - [2.2] Netzwerkprotokolle
    - [2.2.1] OSI-Schicht 1 und 2 (Physical/Data Link)
    - [2.2.2] OSI-Schicht 3 (Network)
      - [2.2.2.1] IP-Version 4
      - [2.2.2.2] IP-Version 6
    - [2.2.3] OSI-Schicht 4 (Transport)
      - [2.2.3.1] Transmission Control Protocol (TCP) und User Datagram Protocol (UDP)
      - [2.2.3.2] UDP/TCP-Portbereiche
      - [2.2.3.3] Transport Layer Security (TLS)
  - [2.3] IP-Adresskonzept der TI
    - [2.3.1] Adressblöcke
    - [2.3.2] Prozesse zur IP-Adressvergabe
    - [2.3.3] Adresskonzept IPv4
    - [2.3.4] Adresskonzept IPv6
    - [2.3.5] Adressen SIS-Systeme
  - [2.4] IP-Routingkonzept
  - [2.5] Priorisierung auf Netzwerkebene
    - [2.5.1] Architektur
    - [2.5.2] Definition und Zuordnung von Dienstklassen
    - [2.5.3] Markierung
      - [2.5.3.1] DSCP-Markierung Netzkonnektor
      - [2.5.3.2] DSCP-Markierung Zentrales Netz TI
      - [2.5.3.3] DSCP-Markierung Fremdnetze
    - [2.5.4] Priorisierung des markierten Datenverkehrs
      - [2.5.4.1] Zentrales Netz
      - [2.5.4.2] Konnektor
      - [2.5.4.3] VPN-Zugangsdienst
  - [2.6] Sicherheitskomponenten im Netzwerk
    - [2.6.1] Typen von Sicherheitskomponenten
    - [2.6.2] Anforderungen an Sicherheitskomponenten
    - [2.6.3] Platzierung von Sicherheitskomponenten
    - [2.6.4] Prozesse zu Regeln für Sicherheitsgateways
    - [2.6.5] Erlaubter Verkehr
  - [2.7] IP-Configuration-Management
- [3] Zentrales Netz der TI
  - [3.1] Zerlegung des Produkttyps
    - [3.1.1] Sicherer Zentraler Zugangspunkt (SZZP)
      - [3.1.1.1] Netzkomponente
      - [3.1.1.2] Sicherheitsgateway
      - [3.1.1.3] Anbindungen
    - [3.1.2] Netzwerk
      - [3.1.2.1] Backbone (zentrales Transportnetz Provider)
  - [3.2] Übergreifende Festlegungen
  - [3.3] Funktionsmerkmale
    - [3.3.1] OSI-Schicht 1 und 2 (Physical/Data Link)
      - [3.3.1.1] Schnittstelle CPE-Produkttyp
      - [3.3.1.2] Hardwaremerkmale
    - [3.3.2] OSI-Schicht 3 (Network)
      - [3.3.2.1] Schnittstelle I_IP_Transport
    - [3.3.3] Adressierung
      - [3.3.3.1] Schnittstelle SZZP-Backbone (CE-PE) und SZZP intern
    - [3.3.4] Routing
    - [3.3.5] Abstimmung mit angeschlossenen Produkttypen
  - [3.4] Verteilungssicht
    - [3.4.1] Zugangsstellen
- [4] Anforderungen an das Sicherheitsgateway Bestandsnetze
  - [4.1] Zerlegung des Produkttyps
- [5] Namensdienst
  - [5.1] Hostnamen
  - [5.2] Namensräume
  - [5.3] Domainnamen- und Hierarchie
  - [5.4] DNS-Topologie
  - [5.5] Dienstlokalisierung
  - [5.6] Schnittstellen I_DNS_Name_Resolution und I_DNS_Service_Localization
    - [5.6.1] Umsetzung
    - [5.6.2] Nutzung
  - [5.7] Anforderungen an den Produkttyp Namensdienst
    - [5.7.1] Schnittstellen P_DNS_Name_Entry_Announcement und P_DNS_Service_Entry_Announcement
    - [5.7.2] Schnittstelle P_DNSSEC_Key_Distribution
    - [5.7.3] Schnittstelle P_DNS_Zone_Delegation
    - [5.7.4] Sonstige Anforderungen
- [6] Zeitdienst
  - [6.1] NTP-Topologie
  - [6.2] Schnittstelle I_NTP_Time_Information
    - [6.2.1] Umsetzung
    - [6.2.2] Nutzung
  - [6.3] Anforderungen an den Produkttyp Zeitdienst
- [7] Hosting
- [8] Anhang A – Verzeichnisse
  - [8.1] Abkürzungen
  - [8.2] Glossar
  - [8.3] Abbildungsverzeichnis
  - [8.4] Tabellenverzeichnis
  - [8.5] Referenzierte Dokumente
    - [8.5.1] Dokumente der gematik
    - [8.5.2] Weitere Dokumente

### 1 Einordnung des Dokuments

### 1.1 Zielsetzung

Die Spezifikation Netzwerk definiert die Rahmenbedingungen und trifft die
übergreifenden Festlegungen zum Netzwerk, dem Namensdienst und dem Zeitdienst
in der TI. Dabei werden die für den Wirkbetrieb der TI erforderlichen
Anforderungen an die Netzinfrastruktur berücksichtigt, eine Erweiterbarkeit um
künftige Anwendungen jedoch beachtet.

Die übergreifende Spezifikation Netzwerk behandelt folgende inhaltlichen
Schwerpunkte:

 ---> UL

### 1.2 Zielgruppe

Das Dokument richtet sich an Hersteller und Anbieter von netzwerkfähigen
Produkten der TI.

### 1.3 Geltungsbereich

Dieses Dokument enthält normative Festlegungen zur Telematikinfrastruktur des
deutschen Gesundheitswesens. Der Gültigkeitszeitraum der vorliegenden Version
und deren Anwendung in Zulassungsverfahren wird durch die gematik GmbH in
gesonderten Dokumenten (z. B. Dokumentenlandkarte, Produkttypsteckbrief,
Leistungsbeschreibung) festgelegt und bekannt gegeben.

Schutzrechts-/Patentrechtshinweis

Die nachfolgende Spezifikation ist von der gematik allein unter technischen
Gesichtspunkten erstellt worden. Im Einzelfall kann nicht ausgeschlossen
werden, dass die Implementierung der Spezifikation in technische Schutzrechte
Dritter eingreift. Es ist allein Sache des Anbieters oder Herstellers, durch
geeignete Maßnahmen dafür Sorge zu tragen, dass von ihm aufgrund der
Spezifikation angebotene Produkte und/oder Leistungen nicht gegen Schutzrechte
Dritter verstoßen und sich ggf. die erforderlichen Erlaubnisse/Lizenzen von
den betroffenen Schutzrechtsinhabern einzuholen. Die gematik GmbH übernimmt
insofern keinerlei Gewährleistungen.

### 1.4 Abgrenzung des Dokuments

Festlegungen zu der Netzwerkkomponente VPN-Zugangsdienst erfolgen in
[gemSpec_VPN_ZugD].

Die Festlegung der spezifischen Anbindungen von Komponenten an die
Netzinfrastruktur der TI und die Einbindung der Netzdienste erfolgen auf der
Basis dieser übergreifenden Spezifikation in den jeweiligen Spezifikationen
der Produkttypen.

### 1.5 Methodik

Anforderungen als Ausdruck normativer Festlegungen werden durch eine eindeutige
ID sowie die dem RFC 2119 [RFC2119] entsprechenden, in Großbuchstaben
geschriebenen deutschen Schlüsselworte MUSS, DARF NICHT, SOLL, SOLL NICHT,
KANN gekennzeichnet.

Sie werden im Dokument wie folgt dargestellt:

\<AFO-ID\> - \<Titel der Afo\>Text / Beschreibung[ \<=]

Dabei umfasst die Anforderung sämtliche zwischen Afo-ID und Textmarke
angeführten Inhalte.

### 2 Übergreifende Netzwerk-Festlegungen

### 2.1 Netztopologie

In diesem Kapitel wird die grundlegende Netztopologie der TI dargestellt um
einen Überblick der beteiligten Systeme auf der Netzwerkebene zu geben. In den
Spezifikationen der jeweiligen Produkttypen erfolgt, wo notwendig, eine
detaillierte Darstellung der einzusetzenden Netztopologie.

Die Abb_NetzTopologie_Schema zeigt eine schematische Übersicht zur
Netztopologie der TI auf logischer Ebene, die sich an den in der
Gesamtarchitektur definierten Zonen orientiert.

![Abbildung-1][Abbildung-1]

In Abb_NetzTopologie_Detail wird auf einer detaillierteren Netzwerkebene die
mögliche Verteilung von an der TI-Plattform angebundenen Produkttypen
dargestellt (ohne Secure Internet Service (SIS)).

Der Adressat „weitere Anwendungen des Gesundheitswesens“ umfasst die
Anwendungskategorien WANDA Basic und WANDA Smart.

Der Adressat „weitere Anwendungen des Gesundheitswesens mit Zugriff auf
Dienste der TI“ wird durch die Anwendungskategorien WANDA Smart und der
Adressat „weitere Anwendungen des Gesundheitswesens ohne Zugriff auf Dienste
der TI“ durch die Anwendungskategorie WANDA Basic beschrieben.

![Abbildung-2][Abbildung-2]

### 2.2 Netzwerkprotokolle

### 2.2.1 OSI-Schicht 1 und 2 (Physical/Data Link)

##### GS-A_4009

Alle Produkttypen der TI und Anbieter weiterer Anwendungen des Gesundheitswesens
mit Zugriff auf Dienste der TI MÜSSEN beim Einsatz des Ethernet-Protokolls an
Schnittstellen zwischen Produkttypen der TI die Einhaltung der [IEEE 802.3]
sicherstellen. **[\<=]**

### 2.2.2 OSI-Schicht 3 (Network)

Als produktiv eingesetztes Netzwerkprotokoll auf der OSI-Schicht 3 wird in der
TI das Internetprotokoll in der Version 4 (IPv4) eingesetzt. Als Teil der
laufenden Migration wird bei definierten Produkttypen bereits die
Unterstützung des Internetprotokolls in der Version 6 (IPv6) gefordert.
Vorgaben zum Protokoll Encapsulation Security Payload (ESP) werden in
[gemSpec_VPN_ZugD] definiert.

### 2.2.2.1 IP-Version 4

##### GS-A_4831

Produkttypen der TI und weitere Anwendungen des Gesundheitswesens MÜSSEN
mindestens die in Tab_Standards_IPv4 aufgeführten Standards unterstützen.

Tabelle1: Tab_Standards_IPv4, Standards IPv4

 ---> TABLE

**[\<=]**

##### GS-A_4832

Produkttypender TI und andere Anwendungen des Gesundheitswesens MÜSSEN
sicherstellen, dass Path MTU Discovery (PMTUD) gemäß [RFC1191] im gesamten
Netzwerk funktioniert. Insbesondere MÜSSEN Router und Gateways die
erforderlichen ICMP-Messages erzeugen, und Sicherheitsgateways MÜSSEN diese
ICMP-Messages passieren lassen. Anfragen durch einen ICMP-Request MÜSSEN mit
einem ICMP-Reply beantwortet werden. **[\<=]**

### 2.2.2.2 IP-Version 6

##### GS-A_4010

Produkttypen, die zentrale Dienste der TI-Plattform bereitstellen, MÜSSEN die
in [RIPE-772]  für die jeweilige Geräteklasse unter Mandatory Support
aufgeführten Anforderungen erfüllen. **[\<=]**

##### GS-A_4011

Zentrale Dienste der TI-Plattform MÜSSEN IPv4 und IPv6 parallel als Protokoll
(Dual-Stack-Mode) unterstützen. Die TSP X.509 SOLLEN IPv4 und IPv6 parallel
unterstützen. **[\<=]**

##### GS-A_4012

Produkttypen, die zentrale Dienste der TI-Plattform bereitstellen, MÜSSEN IPv4
und IPv6 als Protokoll unterstützen, wobei für beide Protokolle eine
vergleichbare Leistung vorhanden sein muss, d. h. weniger als 15% Unterschied
zwischen den beiden Protokollen bei Input, Output, Durchsatz, Weiterleitung und
Verarbeitung.​​ **[\<=]**

##### A_17824

Zentrale Dienste der TI-Plattform MÜSSEN an ihren Außenschnittstellen zu
anderen Komponenten und Diensten der TI sowie WANDA Basic und WANDA Smart im
zentralen Netz der TI und im Internet IPv4 und IPv6 parallel als Protokoll im
Dual-Stack-Mode nutzen. **[\<=]**

### 2.2.3 OSI-Schicht 4 (Transport)

### 2.2.3.1 Transmission Control Protocol (TCP) und User Datagram Protocol (UDP)

Für die Implementierung von TCP und UDP werden an dieser Stelle keine
normativen Vorgaben erhoben. Es wird empfohlen Implementierungen von
TCP/IP-Stacks zu nutzen, die aktuelle Verfahren zur Übertragung und Steuerung
von Daten einsetzen.

### 2.2.3.2 UDP/TCP-Portbereiche

Für die Verwaltung und Dokumentation von UDP/TCP-Portbereichen ist in der TI
ein übergreifender Prozess zu etablieren, der durch den Anbieter Zentrales
Netz TI implementiert und vom Gesamtbetriebsverantwortlichen (GBV) freigegeben
wird.

In den folgenden Anforderungen werden die Verantwortlichkeiten und weitere
Vorgaben zum Prozess „Verwaltung von UDP/TCP-Portbereichen“ definiert.

##### GS-A_4833

Der Anbieter Zentrales Netz TI MUSS den Prozess „Verwaltung von
UDP/TCP-Portbereichen“ mit den folgenden Inhalten definieren und
implementieren:

 ---> UL

Der Anbieter Zentrales Netz TI ist der Verantwortliche für den gesamten Prozess. **[\<=]**

##### GS-A_4886

Der GBV MUSS den vom Anbieter Zentrales Netz TI definierten Prozess
„Verwaltung von UDP/TCP-Portbereichen“ freigeben. **[\<=]**

##### GS-A_4014

Der GBV MUSS für die Zuteilung von UDP/TCP-Portbereichen ein Vergabeschema
unter Berücksichtung der Dienstklassen zur Netzwerkpriorisierung erstellen und
dem Anbieter Zentrales Netz TI zur Verfügung stellen.Der GBV MUSS das
Vergabeschema für UDP/TCP-Portbereiche auf Grundlage des [RFC6335] erstellen.
Der GBV MUSS für die Vergabe von UDP/TCP-Portbereichen den in [RFC6335]
definierten Bereich von 49152-65535 (Dynamic/Private Ports) nutzen. Hiervon
ausgenommen sind Anwendungen die in [RFC6335] definierte Bereiche der System
Ports (Well-Known Ports) bzw. User Ports (Registered Ports) nutzen. **[\<=]**

##### GS-A_4016

Der Anbieter Zentrales Netz TI MUSS UDP/TCP-Portbereiche nach den Vorgaben des
Vergabeschemas an die einzelnen Anbieter der Produkttypen der TI bedarfsgerecht
zuweisen. Die Vergabe der UDP/TCP-Portbereiche erfolgt im Rahmen des Test- und
Zulassungsverfahrens von Anbietern eines Produkttyps. **[\<=]**

##### GS-A_4013

Produkttypen von Fachanwendungen und Zentralen Diensten der TI-Plattform und
Anbieter weiterer Anwendungen des Gesundheitswesens mit Zugriff auf Dienste der
TI MÜSSEN die zugeordneten bzw. abgestimmten UDP/TCP-Portbereiche für die
Kommunikation in der TI nutzen. **[\<=]**

##### GS-A_4753

Der GBV MUSS in Abstimmung mit dem Anbieter Zentrales Netz TI das
Dokumentationsformat für die UDP/TCP-Portbereiche festlegen und dem Anbieter
von Produkttypen der TI zur Verfügung stellen. **[\<=]**

##### GS-A_4017

Der Anbieter Zentrales Netz TI MUSS die Vergabe der UDP/TCP-Portbereiche
dokumentieren und diese Dokumentation dem GBV bei Änderungen und auf
Anforderung zur Verfügung stellen. **[\<=]**

##### GS-A_4018

Die Anbieter von Produkttypen der TI und Anbieter weiterer Anwendungen des
Gesundheitswesens mit Zugriff auf Dienste der TI MÜSSEN die Nutzung der
zugeteilten und mit den Anbietern weiterer Anwendungen des Gesundheitswesens
mit Zugriff auf Dienste der TI abgestimmten UDP/TCP-Portbereiche dokumentieren
und diese Dokumentation dem Anbieter Zentrales Netz TI bei Änderungen und auf
Anforderung zur Verfügung stellen. **[\<=]**

### 2.2.3.3 Transport Layer Security (TLS)

Anforderungen zu den einzusetzenden kryptographischen Verfahren für TLS und
daraus folgende resultierende Vorgaben zur TLS-Version werden in
[gemSpec_Krypt] definiert.

Weitere Eigenschaften und Funktionen für das TLS-Protokoll können wo notwendig
in den Spezifikationen von Produkttypen festgelegt werden.

### 2.3 IP-Adresskonzept der TI

In diesem Kapitel werden Festlegungen zu den in der TI zu nutzenden
IP-Adressbereichen getroffen. Alle Anbieter von Produkttypen müssen das
IP-Adresskonzept der TI produktiv umsetzen.

### 2.3.1 Adressblöcke

Die IP-Adressen in der TI werden in festen Adressblöcken an die Nutzer
vergeben. Die zu nutzenden IP-Adressblöcke werden den definierten
TI-Umgebungen und den dazugehörigen Netzbereichen zugeteilt.

Für jede TI-Umgebung werden zusätzlich IP-Adressblöcke als Reserve definiert.

TI-Umgebungen:

 ---> UL

Netzbereiche:

 ---> UL

Informativ wird zusätzlich der Netzbereich TI_Extern aufgeführt:

 ---> UL

Über diese Netzbereiche werden hier keine Festlegungen getroffen, Adressvergabe
geschieht durch die Besitzer oder Anbieter.

### 2.3.2 Prozesse zur IP-Adressvergabe

Für die Verwaltung und Dokumentation von IP-Adressen ist in der TI ein
übergreifender Prozess zu etablieren, der durch den Anbieter Zentrales Netz TI
implementiert und vom GBV freigegeben wird.

Die in der TI genutzten IP-Adressen werden von dem Anbieter Zentrales Netz TI
verwaltet und im Auftrag des GBVs vergeben. Der Anbieter delegiert IP-Bereiche
aus den spezifizierten Bereichen an Anbieter von TI-Produkttypen.

In den folgenden Anforderungen werden die Verantwortlichkeiten und weitere
Vorgaben zum Prozess „Verwaltung von IP-Adressbereichen“ definiert.

##### GS-A_4834

Der Anbieter Zentrales Netz TI MUSS den Prozess „Verwaltung von
IP-Adressbereichen“ mit den folgenden Inhalten definieren und implementieren:

 ---> UL

Der Anbieter Zentrales Netz TI ist der Verantwortliche für den gesamten Prozess. **[\<=]**

##### GS-A_4888

Der GBV MUSS den vom Anbieter Zentrales Netz TI definierten Prozess
„Verwaltung von IP-Adressbereichen“ freigeben. **[\<=]**

##### GS-A_4021

Der GBV MUSS für die Nutzung erlaubte IP-Adressbereiche und deren Vergabe in
der TI freigeben. **[\<=]**

##### GS-A_4022

Der Anbieter Zentrales Netz TI MUSS die Adressvergabe operativ mit dem GBV und
den Anbietern der Produkttypen in der TI koordinieren. **[\<=]**

##### GS-A_4023

Der Anbieter Zentrales Netz TI MUSS im Rahmen des Test- und Zulassungsverfahrens
IP-Adressbereiche an die einzelnen Anbieter der Produkttypen bedarfsgerecht
zuweisen. **[\<=]**

##### GS-A_4754

Der Anbieter Zentrales Netz TI SOLL den IP-Adressbereich als zusammenhängendes
Subnetz (IPv4) an die einzelnen Anbieter der Produkttypen vergeben. Als
Reservenetz soll er das darauf folgende, gleich große Subnetz vergeben, das
jedoch nur nach Freigabe durch den Anbieter Zentrales Netz TI genutzt werden
darf. **[\<=]**

##### GS-A_4024-01

Alle Anbieter von Diensten in der TI undWANDA-Smart-Anbieter MÜSSEN für ihre
über die TI erreichbaren Systeme die zugewiesenen IP-Bereiche nutzen. Bei
einem WANDA-Smart-Anbieter können es vom Anbieter bereitgestellte
öffentliche IP-Adressen sein. Änderungen an diesen Bereichen MÜSSEN die
Anbieter einzelner TI-Dienste bei dem Anbieter Zentrales Netz TI beantragen und
bei Verwendung eigener öffentlicher IP-Adressen mit dem Anbieter Zentrales
Netz TI abstimmen.WANDA-Basic-Anbieter mit zugewiesenen TI-IPv4-Adressen
MÜSSEN für ihre über die TI erreichbaren Systeme die TI-IPv4-Adressen
nutzen. **[\<=]**

##### GS-A_4026

Der Anbieter Zentrales Netz TI MUSS die Vergabe der IP-Adressbereiche
dokumentieren und diese Dokumentation dem GBV bei Änderungen und auf
Anforderung zur Verfügung stellen. **[\<=]**

##### GS-A_4756

Der Anbieter Zentrales Netz TI MUSS das Format zum Reporting der
IP-Adressbereiche festgelegen. **[\<=]**

##### GS-A_4027

Alle Anbieter von Diensten in der TI und Anbieter weiterer Anwendungen des
Gesundheitswesens mit Zugriff auf Dienste der TI MÜSSEN dem Anbieter Zentrales
Netz TI die Vergabe der IP-Adressbereiche dokumentieren und Änderungen an den
Anbieter Zentrales Netz TI melden. Die Anbieter MÜSSEN jeweils sowohl die
Änderungen als auch die Gesamtübersicht zum zugewiesenen Adressblock melden.
Die Dokumentation der Nutzung von dynamisch vergebenen IP-Adressen soll nicht
erfolgen. **[\<=]**

##### GS-A_4028

Der GBV MUSS die in Tabelle Tab_Adrkonzept_Produktiv mit "Reserve" markierten
IP-Adressbereiche im Bedarfsfall freigeben und an den Anbieter Zentrales Netz
TI zur operativen Verteilung vergeben. **[\<=]**

##### GS-A_4758-01

Der Anbieter Zentrales Netz MUSS für die Adressierung der SZZPs in Richtung
Produkttyp IP-Adressen aus dem zugewiesenen /26 IP-Bereich des angeschlossenen
Produkttyps nutzen.Die Adressierung für den Produkttyp Highspeed Konnektor ist
von dieser Regelung ausgenommen und der Anbieter Zentrales Netz SOLL in
Absprache mit dem Betreiber der Highspeed Konnektoren /28, /29 oder /30
IP-Bereiche nutzen. **[\<=]**

##### GS-A_4759-01

Anbieter von an das Zentrale Netz der TI angeschlossenen Produkttypen MÜSSEN
für die Adressierung ihrer Systeme in Richtung SZZP IP-Adressen aus dem ihnen
zugewiesenen /26 IP-Bereich nutzen.  
Die Betreiber von Highspeed Konnektoren,
die an das Zentrale Netz der TI angeschlossen sind, MÜSSEN für die
Adressierung ihrer Systeme in Richtung SZZP-light-plus IP-Adressen aus dem
ihnen zugewiesenen /28, /29 oder /30 IP-Bereich nutzen.Ein Anbieter weiterer
Anwendungen des Gesundheitswesens mit Zugriff auf Dienste der TI MUSS für die
Adressierung ihrer Systeme in Richtung SZZP die mit dem Anbieter Zentrales Netz
TI abgestimmten IP-Adressen nutzen. **[\<=]**

### 2.3.3 Adresskonzept IPv4

Die folgenden Tabellen legen die zu verwendenden IPv4-Adressbereiche für die
einzelnen TI-Umgebungen fest.

Die Anbieter von TI-Produkttypen erhalten in der Produktivumgebung
Adressbereiche aus dem IPv4-Adressraum 100.64.0.0/10 [RFC6598]. Durch die
Nutzung des in [RFC6598] definierten Adressbereiches wird ein Konflikt mit
bereits genutzten privaten Adressbereichen vermieden. Die Testumgebung ist
getrennt und nutzt den Adressraum 172.16.0.0/12.

##### GS-A_4029-06

Der Anbieter Zentrales Netz TI MUSS den Adressbereich 100.64.0.0/10 nach dem in
der Tab_Adrkonzept_Produktiv definierten Schema zur Vergabe von IPv4-Adressen
an Produkttypen der TI in der Produktivumgebung verwenden.

Tabelle2: Tab_Adrkonzept_Produktiv, Adressräume IPv4 TI Produktivumgebung

 ---> TABLE

**[\<=]**

Erläuterung:

Aus dem Netzbereich 100.64.0.0/11 sollen nur noch IP-Adressblöcke für den
dezentralen Zugang zur TI (TI_Dezentral) zugeteilt werden. Die
IP-Adressblöcke, die schon für den Zugang SIS eingeteilt wurden, bleiben
bestehen und müssen nicht verändert werden.

Für den dezentralen SIS-Zugang muss dem Anbieter des VPN-Zugangsdienstes der
IP-Adressblock 100.104.0.0/15 zugewiesen werden. Somit ist der IP-Adressblock
TI_Dezentral_SIS für jeden VPN-Zugangsdienstanbieter identisch.

##### GS-A_4850-04

Der Anbieter Zentrales Netz TI MUSS den Adressbereich 172.16.0.0/12 nach dem in
Tab_Adrkonzept_Test definierten Schema zur Vergabe von IPv4-Adressen an
Produkttypen der TI in der Testumgebung verwenden.

Tabelle3: Tab_Adrkonzept_Test, Adressräume IPv4 TI-Testumgebung

 ---> TABLE

**[\<=]**

Erläuterung:

Aus dem Netzbereich 172.16.0.0/14 sollen nur noch IP-Adressblöcke für den
dezentralen Zugang zur TI (TI_Dezentral) zugeteilt werden. Die
IP-Adressblöcke, die schon für den Zugang SIS eingeteilt wurden, bleiben
bestehen und müssen nicht verändert werden.

Für den dezentralen SIS-Zugang muss dem Anbieter des VPN-Zugangsdienstes der
IP-Adressblock 172.29.0.0/16 fest zugewiesen werden. Somit ist der
IP-Adressblock TI_Dezentral_SIS für jeden VPN-Zugangsdienstanbieter identisch.

Die Netzwerkbereiche 172.31.0.0/17 und 172.31.128.0/17 sind den gesicherten bzw.
offenen Fachdiensten zugewiesen worden, um weitere QoS-Klassen auf IP-Ebene
abbilden zu können.

##### GS-A_4851

In der Referenzumgebung DÜRFEN die Adressbereiche aus der Produktivumgebung und
Testumgebung NICHT genutzt werden. Für die Vergabe von IPv4-Adressen in der
Referenzumgebung SOLL das in Tab_Adrkonzept_Test definierte Schema (nicht der
IP-Adressbereich) genutzt werden. **[\<=]**

In Tabelle 4 wird informativ die Nutzung von IPv4-Adressbereichen aus
Netzbereich TI_Extern dargestellt.

 ---> TABLE

##### GS-A_4760-01

Bestandsnetze und Anbieter weiterer Anwendungen des Gesundheitswesens ohne
Zugriff auf Dienste der TISOLLEN bei Anschluss an die TI für diesen Anschluss
und Kommunikation mit der TI eigene, öffentliche IPv4-Adressbereiche
nutzen.Ausgenommen sind Anbieter weiterer Anwendungen des Gesundheitswesens
ohne Zugriff auf Dienste der TI, die zugewiesene TI-IPv4-Adressen verwenden.
**[\<=]**

### 2.3.4 Adresskonzept IPv6

Die folgenden Tabellen legen die zu verwendenden IPv6-Adressbereiche für die
einzelnen TI-Umgebungen fest.

Die Anbieter von TI-Produkttypen erhalten in der Produktivumgebung
Adressbereiche aus dem IPv6-Adressraum 2A10:1982:0000::/32. Die Testumgebung
nutzt den IPv6-Adressraum 2A10:1981:0000::/32 und die Referenzumgebung nutzt
den IPv6-Adressraum 2A10:1980::/32.

##### A_19403

Der Anbieter Zentrales Netz TI MUSS den Adressbereich2A10:1982:0000::/32nach dem
in der Tab_Adrkonzept_Ipv6_Produktiv definierten Schema zur Vergabe von
IPv6-Adressen an Produkttypen der TI in der Produktivumgebung verwenden.

Tabelle5: Tab_Adrkonzept_IPv6_Produktiv, Adressräume IPv6 TI Produktivumgebung

 ---> TABLE

**[\<=]**

##### A_19404

Der Anbieter Zentrales Netz TI MUSS den Adressbereich 2A10:1981:0000::/32 nach
dem in der Tab_Adrkonzept_IPv6_Test definierten Schema zur Vergabe von
IPv6-Adressen an Produkttypen der TI in der Testumgebung verwenden.

Tabelle6: Tab_Adrkonzept_IPv6_Test, Adressräume IPv6 TI-Testumgebung

 ---> TABLE

**[\<=]**

##### A_19407

Der Anbieter Zentrales Netz TI MUSS den Adressbereich 2A10:1980:0000::/32 nach
dem in der Tab_Adrkonzept_Ipv6_Refug definierten Schema zur Vergabe von
IPv6-Adressen an Produkttypen der TI in der Referenzumgebung verwenden.

 ---> TABLE

**[\<=]**

##### A_19409

Bestandsnetze und Anbieter weiterer Anwendungen des Gesundheitswesens ohne
Zugriff auf Dienste der TI MÜSSEN bei Anschluss an die TI für diesen
Anschluss und Kommunikation mit der TI eigene, öffentliche IPv6-Adressbereiche
nutzen. **[\<=]**

### 2.3.5 Adressen SIS-Systeme

Der Anbieter des Produkttyps Zugangsdienst muss für die Systeme des Sicheren
Internet Service und der dafür notwendigen eigenen Netzwerkinfrastruktur
eigene öffentliche Adressbereiche verwenden (siehe Tabelle 4: Adressräume
IPv4 TI Extern).

### 2.4 IP-Routingkonzept

Die übergreifende Netzspezifikation legt Routing-Methoden für die
Anschlusspunkte der einzelnen Produkttypen an das Zentrale Netz TI fest.
Routing-Methoden in den lokalen Netzwerken der einzelnen Produkttypen werden
hier nicht definiert oder vorgegeben.

##### GS-A_4033

Der Produkttyp Zentrales Netz der TI MUSS an den Übergabepunkten
zwischenangeschlossenen Produkttypen der TI statisches Routing nutzen. **[\<=]**

##### GS-A_4036

Fachanwendungsspezifische Dienste und zentrale Dienste KÖNNEN am Anschluss an
das Zentrale Netz der TI Hochverfügbarkeitsprotokolle (z. B. VRRP, HSRP)
nutzen. **[\<=]**

##### GS-A_4763

Fachanwendungsspezifische Dienste und zentrale Dienste MÜSSEN bei Nutzung von
Hochverfügbarkeitsprotokollen am Anschluss an das zentrale Netz TI durch
geeignete Maßnahmen (z. B. Authentisierung der Kommunikationspartner)
sicherstellen, dass andere Netzwerkkomponenten nicht beeinflusst werden. **[\<=]**

### 2.5 Priorisierung auf Netzwerkebene

Die Priorisierung von IP-Paketen auf Netzwerkebene dient der Sicherung der
Dienstgüte im Fall von Bandbreitenengpässen. Bandbreitenengpässe können
durch Überbuchung von Übertragungsleitungen auftreten. Sie können kurzzeitig
(transient) oder als langfristiger Mangel auftreten.

Alle Beteiligten müssen grundsätzlich sicherstellen, dass Netzwerkanschlüsse
in der TI mit ausreichender Bandbreite bereitgestellt werden, da die
Priorisierung lediglich bestimmten Datenverkehr bevorzugt behandelt. Die
Priorisierung ermöglicht zwar eine geringfügig höhere mittlere Auslastung
von Netzwerkbandbreiten, dient aber in erster Linie zur Sicherstellung
kritischer Dienste im Falle einer unvorhergesehenen oder unvermeidlichen
Überlast.

### 2.5.1 Architektur

Auf Netzwerkebene existieren etablierte Standards und Verfahren, um eine
Priorisierung von Datenverkehr umzusetzen. Grundsätzlich kann die
Priorisierung über zwei Verfahren implementiert werden:

 ---> UL

Da in der TI-Plattform keine Ende-zu-Ende-Reservierung von Netzwerkressourcen
möglich ist, und zudem das IntServ-Verfahren aufwändig zu implementieren und
zu betreiben ist, wird eine Priorisierung auf der Basis des DiffServ-Verfahrens
eingesetzt.

##### GS-A_4037

Die Produkttypen Konnektor, VPN-Zugangsdienst und Zentrales Netz der TI MÜSSEN
die DiffServ-Architektur gemäß [RFC2474] und [RFC2475] unterstützen. **[\<=]**

### 2.5.2 Definition und Zuordnung von Dienstklassen

Um eine Priorisierung des Datenverkehrs vornehmen zu können, müssen die
Anwendungen und Dienste klassifiziert werden. Hierzu werden in der TI die in
[RFC4594] definierten Dienstklassen verwendet, die eine Zuordnung an Hand von
Anforderungen der Anwendung bzw. des Dienstes ermöglichen. Die Zuordnung
erfolgt gemäß [RFC4594]; die vorliegende Tabelle 5 ist ein übersetzter
Auszug.

 ---> TABLE

Die Zuordnung der Dienstklassen zu den Applikationen erfolgt durch den GBV. Die
initiale Zuordnung erfolgt vor Inbetriebnahme der TI. Die Zuordnung wird im
Betrieb normalerweise nicht geändert. Der GBV muss die Zuordnung erweitern,
sobald neue Dienste hinzukommen, die durch das vorhandene Schema nicht
abgedeckt werden.

### 2.5.3 Markierung

Die Markierung von IP-Paketen zur Priorisierung erfolgt in der TI
ausschließlich durch das Setzen von Differentiated Services Code Point
(DSCP)-Werten im IP-Header. Die Markierung erfolgt gemäß der in [RFC4594]
definierten Zuordnung von Dienstklasse und Priorität zu DSCP-Werten. Tabelle 6
ist ein übersetzter Auszug.

 ---> TABLE

Innerhalb der AF-Klassen wird gemäß [RFC2597] eine Unterscheidung hinsichtlich
der Wahrscheinlichkeit gemacht, mit der durch Active Queue Management IP-Pakete
fallen gelassen werden („Drop Precedence“). Hierbei entspricht eine
niedrige Drop Precedence einer höheren Priorisierung des Datenverkehrs.

 ---> TABLE

Die DSCP-Markierungen werden so weit wie möglich am Rand des Netzwerkes
vorgenommen. Nach der Markierung wird diesen Markierungen durch alle
Netzelemente vertraut.

##### GS-A_4765

Die Produkttypen Konnektor, VPN-Zugangsdienst und Zentrales Netz der TI DÜRFEN
DSCP-Markierungen NICHT unaufgefordert ändern. **[\<=]**

Die folgende Grafik stellt anhand einer beispielhaften Kommunikationsbeziehung
zwischen Anwendungskonnektor und Fachdienst dar, an welchen Punkten die Pakete
mit den DSCP markiert werden.

![Abbildung-3][Abbildung-3]

### 2.5.3.1 DSCP-Markierung Netzkonnektor

##### GS-A_4766

Der Produkttyp Konnektor MUSS die paketbasierte, zustandslose Klassifizierung
unterstützen. Diese Klassifizierung MUSS gemäß zugeordneter Dienstklasse auf
Grundlage einer Regel erfolgen. Der Konnektor MUSS zur Definition der Regel
eine beliebige Kombination folgender Informationen aus OSI Layer 3 und 4
unterstützen: Quell- und Zieladresse, IP-Protokoll sowie Quell- und Zielport. **[\<=]**

##### GS-A_4042

Der Produkttyp Konnektor MUSS durch ihn weitergeleitete IP-Pakete aus dem
dezentralen Intranet und IP-Pakete der Fachmodule gemäß Klassifizierung mit
DSCP-Werten markieren. **[\<=]**

### 2.5.3.2 DSCP-Markierung Zentrales Netz TI

##### GS-A_4044

Der Produkttyp Zentrales Netz MUSS den Transport von DSCP-markierten IP-Paketen
unterstützen. **[\<=]**

##### GS-A_4767

Der SZZP MUSS die paketbasierte, zustandslose Klassifizierung unterstützen.
Diese Klassifizierung MUSS gemäß zugeordneter Dienstklasse auf Grundlage
einer Regel erfolgen. Der SZZP MUSS zur Definition der Regel eine beliebige
Kombination folgender Informationen aus OSI Layer 3 und 4 unterstützen: Quell-
und Zieladresse, IP-Protokoll, sowie Quell- und Zielport. **[\<=]**

##### GS-A_4043

Der SZZP MUSS durch ihn weitergeleitete IP-Pakete aus dem Netz des Fachdienstes
oder des Zentralen Dienstes in die TI gemäß Klassifizierung mit DSCP-Werten
markieren. **[\<=]**

### 2.5.3.3 DSCP-Markierung Fremdnetze

An den Netzübergängen zu Fremdnetzen und Bestandsnetzen können folgende
Maßnahmen genutzt werden:

 ---> OL

##### GS-A_4047

Produkttypen mit Netzübergängen zu Fremdnetzen oder Bestandsnetzen MÜSSEN die
paketbasierte, zustandslose Klassifizierung am Netzübergang unterstützen.
Diese Klassifizierung MUSS gemäß zugeordneter Dienstklasse auf Grundlage
einer Liste mit Regeln erfolgen. Der Netzübergang MUSS zur Definition der
Regel eine beliebige Kombination folgender Informationen aus OSI Layer 3 und 4
unterstützen: Quell- und Zieladresse, IP-Protokoll sowie Quell- und Zielport. **[\<=]**

##### GS-A_4768

Produkttypen mit Netzübergängen zu Fremdnetzen oder Bestandsnetzen MÜSSEN
durch den Netzübergang weitergeleitete IP-Pakete aus dem Fremdnetz in die TI
gemäß Klassifizierung mit DSCP-Werten markieren. **[\<=]**

##### GS-A_4769

Produkttypen mit Netzübergängen zu Fremdnetzen oder Bestandsnetzen MÜSSEN die
DSCP-Übersetzung („Re-Marking“) von IP-Paketen am Netzübergang
unterstützen.

Der Netzübergang zu Fremdnetzen MUSS eine Möglichkeit zur DSCP-Übersetzung
von Paketen aus dem externen Netz vorsehen. Hierzu wird am Netzübergang eine
mit dem Anbieter des Fremdnetzes abzustimmende Regel hinterlegt, welche die
gewünschten DSCP-Werte den IP-Paketen anhand einer Übersetzungstabelle
zuordnet. Diese Funktion muss in beide Richtungen unterstützt und angewendet
werden. **[\<=]**

### 2.5.4 Priorisierung des markierten Datenverkehrs

Zur eigentlichen Priorisierung der klassifizierten und markierten Datenpakete
müssen an den einzelnen Netzkomponenten konkrete technische Maßnahmen
(Queuing, Policing, Shaping) vorgesehen werden. Diese setzen die geforderten
Qualitätsparameter pro definierter Dienstklasse technisch um.

Die Definition der zu den genutzten Dienstklassen gehörigen Qualitätsparameter
(z. B. Bandbreite, Drop-Priority) ist durch einen übergreifenden Prozess
laufend zu überwachen und weiterzuentwickeln, da sich Änderungen insbesondere
durch steigende Netzlast, hinzukommende Fachdienste, hinzugewonnene
Betriebserfahrung, sowie den Anschluss weiterer externer Netze und
Rechenzentren an das Zentrale Netz der TI ergeben.

##### GS-A_4835-01

Die Produkttypen Konnektor,  und Zentrales Netz der TI MÜSSEN die Zuordnung
von Dienstklassen zu fachanwendungsspezifischen Diensten und zentralen Diensten
gemäß Tabellen Tab_QoS_Dienstklassen, Tab_QoS_Mapping_Dienstklasse_Anwendung
und Tab_QoS_Mapping_Dienstklassen_Bandbreite umsetzen.Die Markierung MUSS
sowohl bei Requests als auch bei Responses der Dienste umgesetzt werden.
**[\<=]**

 ---> TABLE

 ---> TABLE

 ---> TABLE

##### GS-A_4048

Die Produkttypen Zentrales Netz, VPN-Zugangsdienst und Konnektor MÜSSEN die
DiffServ-Behandlung von Datenverkehr auf der Grundlage von [RFC4594]
unterstützen. **[\<=]**

##### A_16976

Der  Produkttyp KSR KANN Datenverkehr in Richtung Konnektor mit einer
einheitlichen DSCP-Markierung "KSR Update" versehen. **[\<=]**

##### GS-A_5546

Der Produkttyp Konnektor KANN Datenverkehr in Richtung KSR mit einer
einheitlichen DSCP-Markierung "KSR Update" versehen. **[\<=]**

### 2.5.4.1 Zentrales Netz

##### GS-A_4050

Der Produkttyp Zentrales Netz TI MUSS innerhalb des Zentralen Netzes die
differenzierte Behandlung von IP-Paketen auf Grundlage der DSCP-Markierungen
unterstützen. **[\<=]**

##### GS-A_4051

Der Produkttyp Zentrales Netz TI SOLL innerhalb des Zentralen Netzes alle vom
GBV definierten Dienstklassen als Untermenge der in [RFC4594] definierten
Dienstklassen in vollem Umfang unterstützen. **[\<=]**

##### GS-A_4770

Der Produkttyp Zentrales Netz TI MUSS innerhalb des Zentralen Netzes mindestens
4 Behandlungsaggregate einschließlich eines Echtzeit-Aggregates unterstützen,
auf welche die DSCP-Werte abgebildet werden. **[\<=]**

##### GS-A_4771

Der Produkttyp Zentrales Netz TI MUSS innerhalb des Zentralen Netzes eine
gegebenenfalls notwendige Aggregierung von Dienstklassen auf die in seinem Netz
vorhandenen Behandlungsaggregate gemäß [RFC5127] durchführen. **[\<=]**

##### GS-A_4889

Der Produkttyp Zentrales Netz TI MUSS am Übergang zwischen dem Zugangsrouter
beim Kunden (CE) und dem Zugangsrouter im Zentralen Netz (PE) die Zuweisung von
Bandbreiten pro VPN ermöglichen. Diese Bandbreiten sind als Summe über den
gesamten Datenverkehr eines VPNs zu verstehen. **[\<=]**

##### GS-A_4890

Der Produkttyp Zentrales Netz MUSS am Übergang zwischen dem Zugangsrouter beim
Kunden (CE) und dem Zugangsrouter im Zentralen Netz (PE) innerhalb jeder
VPN-eigenen Bandbreitenzuweisung die Behandlung von Datenverkehr gemäß
DiffServ-Architektur ermöglichen. Dabei MÜSSEN mindestens 8
Behandlungsaggregate unterstützt werden, auf die die Dienstklassen der TI
abgebildet werden. **[\<=]**

##### A_17827-01

Der Produkttyp Zentrales Netz TI SOLL am Übergang zwischen dem Zugangsrouter
beim Kunden (CE) und dem Zugangsrouter im Zentralen Netz (PE) die zur
Verfügung stehende Bandbreite dynamisch auf die VPNs PU, TU und RU mit
garantierten Mindestbandbreiten aufteilen.Mindestbandbreite PU = 50%, TU = 20%,
RU = 10%.Falls die dynamische Aufteilung mit garantierten Mindestbandbreiten
von den CE nicht unterstützt wird, MUSS die Bandbreite wie folgt aufgeteilt
werden:PU = 70%, TU = 20%, RU = 10% oder vom Gesamtverantwortlichen TI nach
Bedarf gemäß Servicekatalog festgelegt. **[\<=]**

### 2.5.4.2 Konnektor

Der Netzkonnektor wird an seiner WAN-Schnittstelle in der Regel an einen stark
bandbreitenlimitierten Internetzugang angeschlossen. Je nach Zugangstechnik
können Uplink-Bandbreiten im Bereich einiger 10 kbit/s bis zu mehreren Gbit/s
vorhanden sein.

Die Priorisierung des Datenverkehrs in das Transportnetz Internet soll direkt
auf dem WAN-Router bzw. IAG des LE auf Grundlage der durch den Konnektor
markierten Datenpakete erfolgen. Da nicht an jedem WAN-Router bzw. IAG eine
Priorisierung möglich ist, muss im Konnektor ein Mechanismus implementiert
werden, der bei Überschreitung der verfügbaren Internet-Uplink-Bandbreite den
Datenverkehr priorisiert. Eine solche Priorisierung ist nur möglich, wenn
unkontrollierte Warteschlangen im Internet-Uplink vermieden werden. Die
Warteschlange darf sich nach Möglichkeit nur in dem Gerät ausbilden, welches
eine Priorisierung des Datenverkehrs vornehmen kann. Diese Funktionalität wird
vom Konnektor gefordert. Dazu wird zunächst ein Bandbreitenbeschränkung
(Traffic Shaping) unterhalb der verfügbaren Internet-Uplink-Bandbreite
implementiert. Auf der sich dadurch ausbildenden Warteschlange wird der
Datenverkehr in geeigneter Weise behandelt.

In der Stufe 1 ist zunächst eine manuelle Konfiguration der verfügbaren
Uplink-Bandbreite durch den Administrator des Konnektors vorgesehen, wobei in
späteren Ausbaustufen ein Verfahren zur automatischen Ermittlung der
verfügbaren Bandbreite implementiert werden soll.

##### GS-A_4772

Der Produkttyp Konnektor MUSS die Bandbreitenbegrenzung (Traffic Shaping) der
Summe des ausgehenden Datenverkehrs in Richtung des Transportnetzes Internet
unterstützen. Die Bandbreitenbegrenzung muss über die
Management-Schnittstelle manuell konfigurierbar sein. Die Bandbreitenbegrenzung
MUSS so gestaltet sein, dass die vorgegebene gesendete Bandbreite zu keiner
Zeit überschritten wird. **[\<=]**

##### GS-A_4773

Der Produkttyp Konnektor MUSS Datenverkehr in Richtung des Transportnetzes
Internet, welcher die konfigurierte abgehende Bandbreitenbegrenzung
überschreitet, gemäß DiffServ-Policy behandeln. Hierzu MUSS der Konnektor
die DSCP-Werte der IP-Pakete heranziehen. **[\<=]**

##### GS-A_4837

Der Produkttyp Konnektor MUSS die differenzierte Behandlung aller vom GBV
definierten Dienstklassen als Untermenge der in [RFC4594] definierten
Dienstklassen in vollem Umfang unterstützen. **[\<=]**

##### GS-A_4774

Der Produkttyp Konnektor MUSS klassenbasiertes Queuing (CBQ) oder einen
vergleichbaren Queuing-Algorithmus, wie zum Beispiel Hierarchical Token Bucket
(HTB), unterstützen. **[\<=]**

##### GS-A_4891

Der Produkttyp Konnektor MUSS die Zuordnung von garantierten Bandbreiten zu
Dienstklassen unterstützen. Die Bandbreiten sind dabei als Mindestbandbreiten
zu verstehen, die der Dienstklasse garantiert werden, aber jederzeit
überschritten werden können. Diejenigen Bandbreitenanteile, welche von einer
konfigurierten Dienstklasse nicht verbraucht werden, MÜSSEN anderen
Dienstklassen zur Verfügung stehen. **[\<=]**

### 2.5.4.3 VPN-Zugangsdienst

Detaillierte Anforderungen zum Aufbau des VPN-Zugangsdienstes und zur Behandlung
des Datenverkehrs werden in [gemSpec_VPN_ZugD] gestellt.

##### GS-A_4840

Der Produkttyp VPN-Zugangsdienst MUSS die differenzierte Behandlung von
IP-Paketen auf Grundlage der DSCP-Markierungen unterstützen. **[\<=]**

##### GS-A_4841

Der Produkttyp VPN-Zugangsdienst MUSS alle vom Gesamtbetriebsverantwortlichen
definierten Dienstklassen als Untermenge der in [RFC4594] definierten
Dienstklassen in vollem Umfang unterstützen. **[\<=]**

### 2.6 Sicherheitskomponenten im Netzwerk

Der Verkehr in der TI wird an Übergabepunkten zwischen Anbietern und Netzwerken
mittels Sicherheitsgateways kontrolliert und auf den für die Diensterbringung
erforderlichen Datenverkehr beschränkt. Der Begriff Sicherheitsgateway wird in
diesem Dokument angelehnt an der Definition in [BSI ISI-LANA] verwendet, d.h.
als System das aus mehreren soft- und hardwaretechnischen
Sicherheitskomponenten besteht, die im folgenden Kapitel beschrieben werden.

### 2.6.1 Typen von Sicherheitskomponenten

Die folgenden Sicherheitskomponenten sind in dieser Spezifikation für die
Kontrolle von Verkehr relevant:

Paketfilter: Paketfilter kontrollieren als Schnittstelle zwischen verschiedenen
Netzen den Datenverkehr auf Transportebene (OSI-Schicht 3 und 4), damit
erwünschte Datenpakete die Paketfilter passieren und unerwünschte oder
unerwartete Pakete diesen nicht passieren.

Application-Level-Gateway (ALG): ALGs, auch Proxy oder Anwendungsproxy genannt,
kontrollieren den Verkehr auf Anwendungsebene (OSI-Schicht 7) zwischen Clients
und Servern. Kommunikationsbeziehungen werden nur über den Proxy aufgebaut,
der den Verkehr auf Anomalien, Schadprogramme oder nicht erlaubte
Inhalte/Verkehre oder Protokolle kontrollieren kann.

Intrusion Detection System (IDS): IDSe untersuchen den passierenden Verkehr auf
Anomalien und Angriffsversuche. Dabei können Heuristiken, Baselines oder
Blacklists/Whitelists eingesetzt werden, um irregulären Verkehr und mögliche
Angriffe zu erkennen. In dieser Spezifikation sind nur netzbasierte IDSe
relevant, die den Verkehr an Netzübergabepunkten kontrollieren.

### 2.6.2 Anforderungen an Sicherheitskomponenten

Die Anforderungen an Sicherheitskomponenten orientieren sich an den Vorgaben der
[BSI ISI-LANA], insbesondere 4.3 und des BSI Kompendiums Baustein [BSI
NET].3.1, insbesondere NET.3.1.A1 und A9.

##### GS-A_4052

Die Produkttypen Zentrales Netz TI und Konnektor MÜSSEN bei der Verwendung von
Paketfiltern und ALGs den passierenden Verkehr verbindungsbasiert kontrollieren
(Stateful-Inspection). **[\<=]**

##### GS-A_4053

Paketfilter und ALGsaller Anbieter und Hersteller von Produkttypen der TIMÜSSEN
sowohl eingehenden als auch ausgehenden Verkehr kontrollieren (Ingress und
Egress Filtering). **[\<=]**

##### GS-A_4054

Paketfilter und ALGs aller Anbieter und Hersteller von Produkttypen der TI
MÜSSEN den passierenden Verkehr ausschließlich auf den spezifizierten und
erlaubten begrenzen. Jeglicher nicht spezifizierter Verkehr MUSS als
Standardregel verboten werden (default-deny).Das Regelwerk MUSS die explizit
erlaubte Kommunikation beinhalten. **[\<=]**

##### GS-A_4057-01

Der Anbieter Zentrales Netz TI, der Anbieter Sicherheitsgateway Bestandsnetze
und der Anbieter Zugangsdienst MÜSSEN auf den eingesetzten Komponenten der
Sicherheitsgateways nur zum Betrieb unbedingt erforderliche Software
installieren, insbesondere ist die Verwendung eines Betriebssystems mit
minimalem Funktionsumfang erforderlich. **[\<=]**

##### GS-A_4777-01

Der Anbieter Zentrales Netz TI, der Anbieter Sicherheitsgateway Bestandsnetze
und der Anbieter Zugangsdienst MÜSSEN auf den eingesetzten Komponenten der
Sicherheitsgateways die grundlegenden Systemfunktionen des minimalen Systems
dokumentieren. **[\<=]**

##### GS-A_4778-01

Der Anbieter Zentrales Netz TI, der Anbieter Sicherheitsgateway Bestandsnetze
und der Anbieter Zugangsdienst MÜSSEN auf den eingesetzten Komponenten der
Sicherheitsgateways nach der Erstinstallation alle Verbindungen, die nicht
explizit erlaubt sind, blockieren. **[\<=]**

##### GS-A_4779-01

Der Anbieter Zentrales Netz TI, der Anbieter Sicherheitsgateway Bestandsnetze
und der Anbieter Zugangsdienst DÜRFEN auf den eingesetzten Komponenten der
Sicherheitsgateways bei einem völligen Ausfall der Komponente NICHT IP-Pakete
passieren lassen. **[\<=]**

### 2.6.3 Platzierung von Sicherheitskomponenten

An folgenden Stellen müssen Sicherheitsgateways in der TI-Plattform eingesetzt
werden:

##### GS-A_4058

Der Anbieter Zentrales Netz TI MUSS den Verkehr an den Anschlusspunkten zum
zentralen Netz mit SZZPs sichern. **[\<=]**

##### GS-A_4059

Der Anbieter des Sicherheitsgateway Bestandsnetze MUSS den Netzübergang
zwischen Bestandsnetzen und TI mit Sicherheitsgateways absichern.

Als geeignete Maßnahmen zur Unterstützung der Absicherung werden angesehen:

 ---> UL

**[\<=]**

Der Konnektor muss den passierenden Verkehr mit einem Paketfilter sichern.

##### GS-A_4061

Der Anbieter Zugangsdienst MUSS den Verkehr zwischen VPN-Konzentratoren und
Transportnetz mit einem Paketfilter sichern. **[\<=]**

Die folgende Abbildung Abb_SichKomp_Platzierung stellt die Platzierung von
Sicherheitskomponenten informativ dar. Die detaillierten Anforderungen werden
in den Spezifikationen der Produkttypen definiert. Anbieter von Produkttypen
der TI können zusätzliche Sicherheitsgateways zum Schutz ihrer Infrastruktur
einsetzen.

![Abbildung-4][Abbildung-4]

Implementieren Produkttypen Übergänge zu Fremdnetzen mit niedrigerem oder
unbekanntem Sicherheitsniveau (z.B. bei den Produkttypen OCSP-Responder Proxy
und Störungsampel), insbesondere zum Internet, müssen besondere Vorkehrungen
getroffen werden, die sich an die Anforderungen des BSI für Netzübergänge
anlehnen.

##### GS-A_4062-01

Zentrale Produkttypen MÜSSEN den Übergang zu Fremdnetzen mit niedrigerem oder
unbekanntem Sicherheitsniveau, wie dem Internet mit einem vom BSI
zertifizierten Sicherheitsgateway oder einem Sicherheitsgateway mit
dreistufigem Aufbau, wie in [BSI ISI-LANA] beschrieben, sichern.Die
Produkttypen MÜSSEN Wechselwirkungen zwischen dem Fremdnetz und der TI
verhindern, und dazu den Verkehr einschränken und kontrollieren.Übergänge
zum Transportnetz mittels SZZP-light und Sicherheitsgateway Bestandsnetze sind
von dieser Regelung ausgenommen. **[\<=]**

##### A_20574-01

Zentrale Produkttypen SOLLEN für Übergänge zu Fremdnetzen die Empfehlungen
der [BSI ISI-LANA] befolgen.Übergänge zum Transportnetz mittels
SZZP-light,SZZP-light-plus und Sicherheitsgateway Bestandsnetze sind von dieser
Regelung ausgenommen. **[\<=]**

Hierbei ist zu beachten, dass grundsätzlich nicht von einem normalen
Schutzbedarf ausgegangen werden darf, sondern dieser immer mindestens hoch
beträgt.

### 2.6.4 Prozesse zu Regeln für Sicherheitsgateways

Für die Verwaltung und Dokumentation von Regeln für Sicherheitsgateway ist in
der TI ein übergreifender Prozess zu etablieren, der durch den Anbieter
Zentrales Netz TI implementiert und vom GBV freigegeben wird.

In den folgenden Anforderungen werden die Verantwortlichkeiten und weitere
Vorgaben zum Prozess „Verwaltung von Sicherheitsgateway-Regeln“ definiert.

##### GS-A_4846

Der Anbieter Zentrales Netz TI MUSS den Prozess „Verwaltung von
Sicherheitsgateway-Regeln“ mit den folgenden Inhalten definieren und
implementieren:

 ---> UL

Der Anbieter Zentrales Netz TI ist der Verantwortliche für den gesamten Prozess. **[\<=]**

##### GS-A_4887

Der GBV MUSS den vom Anbieter Zentrales Netz TI definierten Prozess
„Verwaltung von Sicherheitsgateway-Regeln“ freigeben. **[\<=]**

##### GS-A_4063

Der GBV MUSS im Rahmen des Test- und Zulassungsverfahrens von neuen Diensten und
bei Änderungen an bestehenden Diensten die benötigten
Kommunikationsbeziehungen (Sicherheitsgateway-Regeln) freigeben und an den
Anbieter Zentrales Netz TI melden. **[\<=]**

##### GS-A_4064

Der Anbieter Zentrales Netz TI MUSS die Anpassung von Sicherheitsgateway-Regeln
operativ mit dem GBV und Anbietern von Produkttypen der TI koordinieren. **[\<=]**

##### GS-A_4065

Der Anbieter Zentrales Netz TI MUSS die Umsetzung neuer
Sicherheitsgateway-Regeln an die Anbieter von Produkttypen der TI melden. **[\<=]**

##### GS-A_4066

Die Anbieter der Produkttypen VPN-Zugangsdienst und Sicherheitsgateway
Bestandsnetze MÜSSEN Change Requests zur Anpassung von
Sicherheitsgateway-Regeln vom Anbieter Zentrales Netz TI umsetzen. **[\<=]**

##### GS-A_4780

Der Anbieter Zentrales Netz TI MUSS das Schema für die Dokumentation und das
Reporting von Sicherheitsgateway-Regeln festlegen. **[\<=]**

##### GS-A_4067

Die Produkttypen VPN-Zugangsdienst und Sicherheitsgateway Bestandsnetze MÜSSEN
Änderungen an Sicherheitsgateway-Regeln an den Anbieter Zentrales Netz TI
melden. Die Anbieter MÜSSEN diese Änderungen zusammen mit dem Gesamtsatz an
Filterregeln melden. **[\<=]**

##### GS-A_4068

Der Anbieter Zentrales Netz TI MUSS den Gesamtsatz an Sicherheitsgateway-Regeln
in regelmäßigen Zeitintervallen dokumentieren und an den
Gesamtverantwortlichen der TI melden. Das Zeitintervall muss der Anbieter des
zentralen Netzes mit dem Gesamtverantwortlichen der TI abstimmen. **[\<=]**

### 2.6.5 Erlaubter Verkehr

##### GS-A_4069

Die Produkttypen Konnektor, Zugangsdienst, Sicherheitsgateway Bestandsnetze
MÜSSEN bei Einsatz von Sicherheitsgateways den Verkehr mit Sicherheitsgateways
auf den Verkehr einschränken, der in der Kommunikationsmatrix in der
Architektur der TI-Plattform[gemKPT_Arch_TIP#Kommunikationsmatrix]aufgeführt
ist. **[\<=]**

##### GS-A_4070

Die Produkttypen Konnektor, Zugangsdienst und Sicherheitsgateway Bestandsnetze
MÜSSEN bei Einsatz von Sicherheitsgateways Protokolle zur Netzwerksteuerung
erlauben (mindestens notwendiger Verkehr zur Path MTU Discovery gemäß
[RFC1191]). **[\<=]**

##### GS-A_4884

Paketfilter und ALGs aller Anbieter von Produkttypen der TI MÜSSEN
sicherstellen, dass nur die folgend aufgeführten ICMP-Types verarbeitet bzw.
weitergeleitet werden:

 ---> UL

Eine weitere Einschränkung der erlaubten ICMP-Types kann auf Ebene der
Spezifikationen des Produkttyps erfolgen. **[\<=]**

##### A_18796

Paketfilter und ALGs aller Anbieter von Produkttypen der TI MÜSSEN
sicherstellen, dass nur die folgend aufgeführten ICMPv6-Types und Codes
verarbeitet bzw. weitergeleitet werden:

 ---> UL

**[\<=]**

### 2.7 IP-Configuration-Management

Die Kommunikation innerhalb des zentralen Netzes der TI wird in den SZZPs und
VPN-Anschlusspunkten des SZZP-light sowie des SZZP-light-plus durch den
Anbieter zentrales Netz der TI mittels Routingeinträgen und
Firewallfreischaltungen kontrolliert. In den Spezifikationen der TI ist
festgelegt, welche Schnittstellen die Produkttypen als Client und als Server
(bereitgestellte Schnittstelle eines Dienstes) implementieren müssen und damit
welche Produkttypen über die Schnittstellen miteinander kommunizieren. Dienste
der WANDA Smart- und WANDA-Basic-Anbieter müssen im Rahmen der Inbetriebnahme
gegenüber dem Anbieter zentrales Netz angeben, welche Schnittstellen der
zentralen Dienste der TI-Plattform sie nutzen und unter welchen IP-Adressen und
Ports ihre Schnittstellen erreichbar sind.

Der Begriff Client gibt in diesem Kapitel die Quelle einer IP-Verbindung an.
Der Begriff Dienst wird verwendet um das Ziel der IP-Verbindung zu beschreiben.

Die IP-Adressen der Clients und Dienste werden vom Anbieter des zentralen Netzes
verwaltet. Die anhand der Spezifikationen entwickelten Produkte und von den
Anbietern betriebenen Produktinstanzen realisieren die Schnittstellen ggf.
mehrfach. Die Produkte können auch in mehreren Produktinstanzen betrieben
werden. Zusätzlich können durch den Gesamtverantwortlichen der TI (GTI)
weitere Kommunikationsbeziehungen genehmigt werden.

##### A_14551

Der Anbieter des zentralen Netzes der TI MUSS ein IP-Configuration-Management
implementieren und die Daten der an das Zentrale Netz angeschlossenen Clients
und Server für die Umgebungen PU, TU und RU pflegen.Zu den Daten gehören
insbesondere:

 ---> UL

**[\<=]**

##### A_14553

Der Anbieter zentrales Netz der TI MUSS in enger Abstimmung mit dem GTI ein
Datenmodell für das IP-Configuration Management entwickeln und (wenn
erforderlich) an Änderungen in der TI anpassen. **[\<=]**

Die folgende Abbildung zeigt beispielhaft eine mögliche Ausprägung des
Datenmodells.

![Abbildung-5][Abbildung-5]

##### A_14554

Der Anbieter zentrales Netz der TI MUSS für neu an das zentrale Netz
anzuschließende Clients und Dienste oder für Clients und Dienste deren
IP-Konfiguration sich ändern wird, selbständig und ohne unangemessene
Verzögerung alle benötigten Firewall Regeln generieren und über den
betrieblichen Change Prozess des GTI freigeben lassen sowie nach Freigabe durch
den GTI in den betroffenen SZZPs und VPN-Anschlusspunkten aktivieren.Der
Anbieter zentrales Netz MUSS die Anbieter der von den Freischaltungen
betroffenen Standorte über die geplanten und durchgeführten Änderungen
informieren, damit sie die Freischaltungen in ihrer Netzwerk-Infrastruktur
rechtzeitig berücksichtigen können. **[\<=]**

##### A_14555

Der Anbieter zentrales Netz der TI MUSS ermöglichen, dass der GTI die Daten des
IP-Configuration-Management mittels Reports und zur elektronischen
Weiterverarbeitung erhält oder automatisiert auslesen kann.Die Reports MÜSSEN
mit dem GTI abgestimmt werden und MÜSSEN mindestens enthalten:

 ---> UL

Die Reports MÜSSEN ohne unangemessene Verzögerung nach jeder Änderung an der
IP-Konfiguration der Clients und Dienste erstellt und dem GTI zur Verfügung
gestellt werden (maximal täglich). **[\<=]**

### 3 Zentrales Netz der TI

### 3.1 Zerlegung des Produkttyps

Der Produkttyp Zentrales Netz besteht aus den folgenden Komponenten:

SZZPs(Sicherer Zentraler Zugangspunkt)

 ---> UL

SZZP-light und SZZP-light-plus:

 ---> UL

Netzwerk:

 ---> UL

Eine informative Darstellung der Zerlegung befindet sich in der folgenden
Abbildung Abb_ZentrNetz_Zerlegung.

![Abbildung-6][Abbildung-6]

### 3.1.1 Sicherer Zentraler Zugangspunkt (SZZP)

Die SZZPs stellen den Anschluss von Produkttypen an das Zentrale Netz TI her.
Der SZZP stellt dazu in Richtung Produkttyp die Schnittstelle I_IP_Transport
bereit.

SZZPs werden als CPEs (Customer Premises Equipment) in den Räumen und
Einrichtungen der Produkttypen vom Anbieter Zentrales Netz betrieben.

##### GS-A_4781

Der Anbieter Zentrales Netz TI MUSS die für den Zugang zum Zentralen Netz
notwendigen Sicheren Zentralen Zugangspunkte (SZZP) als Netzwerkgeräte
implementieren, die aus logisch zwei Komponenten bestehen: a) der
Netzkomponente, die die Transportfunktion übernimmt, und b) dem
Sicherheitsgateway, das den Verkehr kontrolliert. **[\<=]**

##### GS-A_4782

Der Anbieter Zentrales Netz TI MUSS die für den Zugang zum Zentralen Netz
notwendigen SZZPs in den Einrichtungen der angeschlossenen Produkttypen
betreiben. **[\<=]**

##### GS-A_5076

Das Zentrale Netz TI KANN verschiedene Produktinstanzen über einen gemeinsamen
SZZP anbinden. Dabei sind folgende Bedingungen zu erfüllen:

 ---> UL

Ein Routing zwischen den angebundenen Produktinstanzen über das zentrale
Transportnetz des Providers für das Zentrale Netz TI muss nicht erfolgen. **[\<=]**

##### A_21142

Ein Hersteller oder Anbieter MUSS wenn verschiedene logische Produktinstanzen
über einen gemeinsamen SZZP angebunden sind, folgende Bedingungen erfüllen:

 ---> UL

**[\<=]**

### 3.1.1.1 Netzkomponente

Die Netzkomponente CE (Customer Edge) stellt die Verbindung zum zentralen Netz
des Anbieters her und vermittelt dabei IP-Pakete zwischen der TI und dem
angeschlossenen Produkttyp.

Die Netzkomponente hat folgende zwei logische Anschlüsse:

 ---> OL

### 3.1.1.2 Sicherheitsgateway

SZZPs enthalten zur Kontrolle des Verkehrs Sicherheitsgateways. Es werden keine
Vorgaben gemacht, ob die Sicherheitsgateways separate Systeme oder in der
Netzwerkkomponente (CE) integriert sind.

SZZPs können verschiedene Arten von Sicherheitsgateways implementieren,
mindestens jedoch Paketfilter.

##### GS-A_4783

Das Zentrale Netz TI MUSS an den SZZPs den Verkehr mit Paketfiltern als
Sicherheitsgateway kontrollieren und einschränken. **[\<=]**

### 3.1.1.3 Anbindungen

Anbindung SZZP-Produkttyp

Die SZZP-Produkttyp Anbindung stellt die Verbindung der angeschlossenen
Produkttypen in deren Räumlichkeiten mit dem SZZP her.

Die Schnittstelle I_IP_Transport befindet sich entweder auf dem CE, falls das
Sicherheitsgateway in diesen integriert ist, oder im Sicherheitsgateway, falls
diese ein vom CE separates System ist.

Die Anbindung des Produkttyps kann mit einem oder zwei SZZPs in den
Räumlichkeiten des angeschlossenen Produkttyps realisiert werden.

Für den Anschluss an das Zentrale Netz TI gibt es folgende Varianten:

 ---> UL

![Abbildung-7][Abbildung-7]

##### GS-A_4784

Der Anbieter Zentrales Netz MUSS für den Anschluss der Dienste an die SZZPs
oder an die VPN-Anschlusspunkte die folgenden Anschlussvarianten je
Rechenzentrum unterstützen:

 ---> UL

Jeder SZZP und jeder VPN-Anschlusspunkt MUSS zwei physikalische Schnittstellen
pro Umgebung (Produktivumgebung, Testumgebung und Referenzumgebung) in Richtung
LAN des angeschlossenen Produkttyps bereitstellen und die Schnittstellen bei
Bedarf zu einer logischen Schnittstelle zusammenfassen (Link aggregation nach
IEEE 802.1ad). **[\<=]**

##### GS-A_4785

Der Anbieter Zentrales Netz MUSS bei Nutzung einer redundanten Anschlussvariante
geeignete technische Maßnahmen zum redundanten Betriebund Failover der SZZPs
implementieren und nutzen. **[\<=]**

Anbindung Provider (CE-PE)

Die CE-PE Anbindung stellt die Verbindung der SZZPs (CE) in den Räumlichkeiten
des angeschlossenen Produkttyps mit dem Backbone (PE) des Zentralen Netzes TI
her.

##### GS-A_4786

Das Zentrale Netz MUSS für den Anschluss der SZZPs an das Backbone an der
CE-PE-Grenze die folgenden Anschlussvarianten je Rechenzentrum
desangeschlossenen Produkttyps unterstützen:

 ---> UL

**[\<=]**

##### GS-A_4787

Der Anbieter des Zentralen Netzes der TI MUSS für den Anschluss SZZP-Provider
(CE-PE) die folgenden Typen von skalierbaren Bandbreiten unterstützen:

 ---> UL

Das Zentrale Netz MUSS eine Skalierung innerhalb der Typen ohne den Austausch
der CE-Hardware und Anschlussleitungen ermöglichen.

Die Skalierung der Bandbreite soll von 1 Mbit/s bis 100 Mbit/s in 1 MBit/s
Schritten, von 100 MBit/s bis 1GBit/s in 100 MBit/s Schritten und von 1GBit/s
bis 10 GBit/s in 1 GBit/s Schritten möglich sein. **[\<=]**

Das zentrale Netz kann Anschlüsse mit höherer Bandbreite unterstützen.

Anbindungstyp SZZP-light 

Der SZZP-light ist ein Anbindungstyp für die Anbindung von Standorten und der
dort betriebenen Dienste und Komponenten an das Zentrale Netz der
Telematikinfrastruktur.

Der SZZP-light besteht aus einem VPN-Konzentrator und einem Paketfilter auf der
einen Seite und aus einem VPN-Anschlusspunkt (VPN-Router und Paketfilter) im
Rechenzentrum des anzuschließenden Dienstes. Am anzuschließenden Standort
wird ein bestehender Internetzugang vorausgesetzt. Über das Internet wird ein
IPSec-Tunnel vom VPN-Anschlusspunkt zum VPN-Konzentrator aufgebaut und über
den SZZP erfolgt die Anbindung an das zentrale Netz der TI. In der Firewall am
VPN-Anschlusspunkt und am SZZP erfolgt die Kontrolle und Durchsetzung der
erlaubten Kommunikationsbeziehungen und das Accounting.

![Abbildung-8][Abbildung-8]

Um eine redundante Anbindung der Standorte zu ermöglichen, müssen der
VPN-Konzentrator und das Sicherheitsgateway an zwei Standorten redundant
implementiert werden (siehe Abb_VPN-Konzentrator_und_Paketfilter_Redundanz).

Anbindungstyp SZZP-light-plus

Der SZZP-light-plus ist ein Anbindungstyp für die Anbindung von Standorten und
den dort anzuschließenden Systemen (wie z.B. der Highspeed-Konnektor) an das
Zentrale Netz der Telematikinfrastruktur.

Der SZZP-light-plus besteht aus einem VPN-Konzentrator und einem Paketfilter auf
der einen Seite und aus einem VPN-Anschlusspunkt (VPN-Router und Paketfilter)
im Rechenzentrum des Betreibers der anzuschließenden Systeme. Am Standort 
des Anschlusspunktes wird ein bestehender Internetzugang vorausgesetzt. Über
das Internet wird ein IPSec-Tunnel vom VPN-Anschlusspunkt zum VPN-Konzentrator
aufgebaut und über den SZZP erfolgt die Anbindung an das Zentrale Netz der TI.
Im Rechenzentrum des Betreiber wird das anzuschließende System mit einem
IPsec-Tunnel an den VPN-Anschlusspunkt angebunden. In der Firewall am
VPN-Anschlusspunkt und am SZZP erfolgt die Kontrolle und Durchsetzung der
erlaubten Kommunikationsbeziehungen und das Accounting.

![Abbildung-9][Abbildung-9]

Um eine redundante Anbindung der Standorte zu ermöglichen, müssen der
VPN-Konzentrator und das Sicherheitsgateway an zwei Standorten redundant
implementiert werden (siehe Abbildung unten,
"Abb_VPN-Konzentrator_und_Paketfilter_Redundanz").

##### A_14531-01

Das zentrale Netz der TI MUSS die zentralen Komponenten des SZZP-lightsowie
SZZP-light-plus entweder an mindestens zwei Standorten als active/standby
Cluster aus VPN-Konzentratoren und Paketfilter gemäß Abbildung
"Abb_VPN-Konzentrator_und_Paketfilter_Redundanz" oder als
stretched active/standby Cluster aus VPN-Konzentratoren und Paketfilter über
zwei Standorte verteilt implementieren.

Abbildung10: Abb_VPN-Konzentrator_und_Paketfilter_Redundanz  **[\<=]**

##### A_17946-01

Das zentrale Netz der TI MUSS SZZP-light- sowie SZZP-light-plus-Anschlüsse so
implementieren, dass die Zugänge zu den Umgebungen PU, TU und RU logisch
getrennt auf der gleichen Hardware bereitgestellt werden. **[\<=]**

##### A_14533-01

Das zentrale Netz der TI SOLL SZZP-light- sowie SZZP-light-plus-Anschlüsse
anbieten, die an den VPN-Anschlusspunkten eine Bandbreite (IPSec
Verschlüsselungsleistung) von 100 Mbit/s bis 1 Gbit/s unterstützen. **[\<=]**

SZZP-light- und SZZP-light-plus-Anschlüsse mit höherer Bandbreite dürfen
angeboten werden.

##### A_14534-01

Das zentrale Netz der TI MUSS die zentralen Komponenten der SZZP-light- sowie
SZZP-light-plus-Anschlüsse so dimensionieren und an sich ändernde
Lastsituationen anpassen, dass

 ---> UL

**[\<=]**

Bei Anpassungen muss der betriebliche Change-Prozess durchlaufen werden.

##### A_14535-01

Daszentrale Netz der TI MUSS bei Vorhandensein von redundanten
VPN-Anschlusspunkten die VPN-Anschlusspunkte so implementieren, dass bei
Ausfall des aktiven VPN-Anschlusspunktes ein Failover auf den standby
VPN-Anschlusspunkt erfolgt. **[\<=]**

Die Funktionen des VPN-Anschlusspunktes VPN-Router und Paketfilter können in
einem Gerät realisiert sein.

##### A_14536-01

Das zentrale Netz der TI MUSS die zentralen Komponenten derSZZP-light- sowie
SZZP-light-plus-Anschlüsse (VPN-Konzentratoren und Paketfilter) so
implementieren, dass bei Ausfall einer aktiven Komponente ein Failover auf die
Standby-Komponente erfolgt. **[\<=]**

Die Komponenten VPN-Konzentrator und Paketfilter können in einem Gerät
realisiert sein.

Zusätzlich wird der  SZZP-light-plus um eine Authentifizierungs-Funktion
erweitert. Der SZZP-light-plus darf die Kommunikation mit zentralen Diensten
und gesicherten Fachdiensten (bspw. ePA-Aktensystem) nur nach einer sicheren
Authentifizierung des angeschlossenen Systems zulassen. Der Betreiber muss von
der Konfiguration ausgeschlossen werden, damit er nicht eigene
Authentisierungsmittel im SZZP-light-plus hinzufügen kann. Somit kann genau
nur das anzuschließende technische System über den SZZP-light-plus mit den
genannten Diensten kommunizieren.

##### A_22355

DerSZZP-light-plus MUSS die mit ihm verbundenen, an das zentrale Netz der TI
anzuschließenden Systeme sicher authentifizieren, bevor diese mit zentralen
Diensten und gesicherten Fachdiensten kommunizieren dürfen. Dabei MUSS auch
das spätere Einschleusen von Daten in die Verbindung zwischen den
anzuschließenden Systemen und dem SZZP-light-plus durch nicht authentifizierte
Dritte unterbunden werden. Für die Erreichbarkeit offener Dienste ist diese
Leistung optional. **[\<=]**

Diese Anforderung kann bspw. durch einen IPsec-Kanal zwischen
dem anzuschließenden System und SZZP-light-plus mit Authentisierung über
pre-shared keys erfüllt werden.

##### A_22356

DerSZZP-light-plus MUSS die Änderung von Konfigurationen für die
Authentifizierung von anzuschließenden Systemen vor dem Zugriff durch den
Betreiber dieser angeschlossenen Systeme schützen. **[\<=]**

Bezogen auf die Verwendung eines IPsec-Kanals bedeutet dies, dass gerade nicht
der Betreiber neue (eigene) pre-shared keys im SZZP-light-plus für
anzuschließende Systeme hinterlegen darf.

### 3.1.2 Netzwerk

### 3.1.2.1 Backbone (zentrales Transportnetz Provider)

##### GS-A_4788

Der Anbieter Zentrales Netz TI MUSS das Zentrale Netz TI als skalierbares
(Anzahl Anschlüsse und Bandbreite erweiterbar) privates Netz implementieren.

Das Zentrale Netz TI MUSS private, auf OSI-Schicht 3 logisch getrennte Netzwerke
(IP-VPN) zwischen den einzelnen SZZPs unterstützen.

Das Zentrale Netz TI MUSS 3 IP-VPN bereitstellen.

Das Zentrale Netz TI MUSS eine Erweiterung der nutzbaren IP-VPN unterstützen.

Die Nutzbarkeit der einzelnen IP-VPN MUSS pro SZZP wählbar sein. **[\<=]**

##### GS-A_4789

Der Anbieter des Produkttyps Zentrales Netzes TI MUSS sicherstellen, dass der
Transport von Daten der TI zwischen den SZZP der Produkttypen über kein
öffentliches Transportnetzwerk, wie z. B. dem Internet, erfolgt. **[\<=]**

##### GS-A_4880

Der Anbieter Zentrales Netz MUSS jeweils ein IP-VPN für die Produktivumgebung,
die Testumgebung und die Referenzumgebung bereitstellen. **[\<=]**

##### GS-A_4881

Der Anbieter Zentrales Netz MUSS die IP-VPN für die Produktivumgebung, die
Testumgebung und die Referenzumgebung am SZZP auf separaten physischen
Interfaces in Richtung des angeschlossenen Produkttyps übergeben. **[\<=]**

##### GS-A_4882

Der Anbieter Zentrales Netz MUSS die separate Zuweisung einer vereinbarten
Bandbreite (Committed Access Rate- CAR) pro bereitgestelltem IP-VPN an einem
Netzwerkanschluss ermöglichen. **[\<=]**

##### GS-A_4883

Der Anbieter Zentrales Netz MUSS sicherstellen, dass kein Datenaustausch und
keine gegenseitige Beeinflussung zwischen IP-VPN möglich sind. **[\<=]**

### 3.2 Übergreifende Festlegungen

Die Freigabe von erlaubten Kommunikationsbeziehungen erfolgt im Rahmen der
Zulassung von Diensten in der TI. Der neu aufgenommene Dienst benennt die
benötigte Kommunikation und der GBV gibt sie frei und beauftragt den Anbieter
Zentrales Netz mit der Freischaltung in den SZZP.

##### GS-A_4790

Das Zentrale Netz MUSS sicherstellen, dass im Zentralen Netz der TI und zwischen
den angeschlossenen Produkttypen ausschließlich erlaubte IP-Kommunikation in
Richtung Produkttypen und fachanwendungsspezifischer Dienste gesendet wird.

Die erlaubte Kommunikation umfasst:

 ---> UL

**[\<=]**

##### GS-A_4791

Das Zentrale Netz TI MUSS neuen erlaubten Datenverkehr in der TI nach Freigabe
durch den GBV im Zentralen Netz ermöglichen. Nicht mehr erlaubter Verkehr darf
nach Freigabe durch den GSV nicht mehr weitergeleitet werden. **[\<=]**

##### A_14648

Der Anbieter Zentrales Netz MUSS auf Verlangen der gematik an benannten SZZPs
zeitnah prüfen, ob bestimmte IP-Pakete weitergeleitet oder verworfen werden.
**[\<=]**

Das zentrale Netz kann Anschlüsse mit höherer Bandbreite unterstützen.

##### GS-A_4792

Der Anbieter Zentrales Netz TI MUSS durch organisatorische Maßnahmen
sicherstellen, dass nur von der gematik zugelassene Fachdienste, zentrale
Dienste und Bestandsnetze (inkl. KV-SafeNet) an die TI angebunden werden. **[\<=]**

### 3.3 Funktionsmerkmale

##### GS-A_4795

Das Zentrale Netz MUSS die Schnittstellen gemäß
TabelleTab_PT_ZentrNetz_Schnittstellenimplementieren ("bereitgestellte"
Schnittstellen) und nutzen ("benötigte" Schnittstellen).

Tabelle14:Tab_PT_ZentrNetz_Schnittstellen

 ---> TABLE

​​​​ **[\<=]**

### 3.3.1 OSI-Schicht 1 und 2 (Physical/Data Link)

### 3.3.1.1 Schnittstelle CPE-Produkttyp

##### GS-A_4796

Das Zentrale Netz MUSS die Schnittstelle der SZZPs auf der Customer Edge mit
mindestens Gigabit Ethernet als 1000Base-T (IEEE 802.3ab) oder IEEE 802.3z
implementieren. Das Zentrale Netz MUSS logisch getrennte Netzwerke gemäß
Standard 802.1q bereitstellen. **[\<=]**

### 3.3.1.2 Hardwaremerkmale

##### GS-A_4797

Der Anbieter Zentrales Netz TI MUSS die Schnittstellen auf den SZZPs Richtung
angeschlossenem Produkttyp der TI modular mit Small Form-factor Pluggables
(SFP) nach den Spezifikationen des SFF [SFF] implementieren.

Der Anbieter Zentrales Netz MUSS sich bei der Art der Schnittstellen und Stecker
auf den SZZPs Richtung angeschlossenem Produkttyp der TI nach den Vorgaben des
Anbieters des angeschlossenen Produkttyps richten. **[\<=]**

### 3.3.2 OSI-Schicht 3 (Network)

### 3.3.2.1 Schnittstelle I_IP_Transport

##### GS-A_4798

Das Zentrale Netz MUSS die Schnittstelle I_IP_Transport und die Operation
I_IP_Transport::send_Data umsetzen, die den Transport, Empfang und Versand von
IPv4- und IPv6-Paketen gewährleistet ([gemSpec_Net#Tab_Standards_IPv4] und
[gemSpec_Net#2.2.2.2]). **[\<=]**

### 3.3.3 Adressierung

### 3.3.3.1 Schnittstelle SZZP-Backbone (CE-PE) und SZZP intern

Adressierung auf der SZZP-Backbone (CE-PE), möglichen SZZP-internen
Schnittstellen und Anschlüssen hinter dem PE liegen in Verantwortung des
Anbieters Zentrales Netz.

##### GS-A_4799

Der Anbieter Zentrales Netz MUSS für die folgenden IP-Schnittstellen
IP-Adressen aus seinem eigenen Bestand nutzen:

 ---> UL

**[\<=]**

##### GS-A_4800

Der Anbieter Zentrales Netz TI MUSS mögliche Adresskonflikte zwischen von ihm
genutzten IP-Adressen (zwischen Sicherheitsgateways und CE, CE-PE und
PE-Backbone) und TI-Adressen (100.64.0.0/10 [RFC6598]) selbst lösen. **[\<=]**

### 3.3.4 Routing

##### GS-A_4801-01

Das Zentrale Netz MUSS gewährleisten, dass zwischen allen SZZPs alle
IP-Adressblöcke der Betriebsumgebungen der TI (wie im jeweiligen Adresskonzept
festgelegt) sowie die angeschlossenen WANDA Basic IP-Adressblöcke erreichbar
sind. **[\<=]**

##### GS-A_4803

Der GBV MUSS dem Anbieter Zentrales Netz TI die Adressbereiche von
Bestandsnetzen mit Anschluss an die TI bei Neuanschluss an die TI oder
Änderungen melden. **[\<=]**

### 3.3.5 Abstimmung mit angeschlossenen Produkttypen

##### GS-A_4804

Der Anbieter Zentrales Netz TI MUSS die vom Produkttyp gemeldeten Parameter nach
Tab_PT_ZentrNetz_AnschlussParameter umsetzen. **[\<=]**

##### GS-A_4805

Die Anbieter aller Produkttypen der TI mit Anschluss an das Zentrale Netz TI und
Anbieter weiterer Anwendungen des Gesundheitswesens mit Zugriff auf Dienste der
TI MÜSSEN mindestens die folgenden Parameter zur Konfiguration ihres
Anschlusses an das Zentrale Netz TI an den Betreiber des Zentralen Netzes
melden:

Tabelle15:Tab_PT_ZentrNetz_AnschlussParameter: Anschlussparameter

 ---> TABLE

​​ **[\<=]**

##### GS-A_4895

Der Anbieter Zentrales Netz MUSS Anbietern von Produkttypen der TI bei deren
Anschluss an das Zentrale Netz TI mindestens die folgenden Informationen über
die zu installierenden Komponenten des SZZP zur Verfügung stellen:
Außenmaße, Gewicht, Art und Anzahl Stromzufuhr, Leistungsaufnahme,
Abwärmeabfuhr oder-abtransport. **[\<=]**

### 3.4 Verteilungssicht

### 3.4.1 Zugangsstellen

Verteilung der Backbone-Zugangsstellen

##### GS-A_4806

Der Point of Presence (PoP, Standort von PE-Routern im Backbone des Anbieters
des Zentralen Netzes der TI) MUSS an das eigene zentrale Netz des Anbieters
redundant angeschlossen sein. **[\<=]**

##### GS-A_4807

Der Anbieter Zentrales Netz MUSS in den folgenden Ballungsräumen regionale PoPs
zu seinem Netzwerk betreiben:

 ---> UL

**[\<=]**

### 4 Anforderungen an das Sicherheitsgateway Bestandsnetze

### 4.1 Zerlegung des Produkttyps

Der Produkttyp Sicherheitsgateway Bestandsnetze besteht aus den folgenden
Komponenten:

 ---> UL

Das Sicherheitsgateway Bestandsnetze ist ein Anbindungstyp zur Anbindung von
Standorten an das Zentrale Netz der Telematikinfrastruktur. Über das
Sicherheitsgateway Bestandsnetze sind die Dienste von Bestandsnetzen für
Clientsysteme erreichbar. Das zentrale Netz der TI dient dabei nur dem
Transport der Daten. Ein Zugriff der Dienste von Bestandsnetzen auf zentrale
Dienste der TI-Plattform oder auf fachanwendungsspezifische Dienste wird durch
das Sicherheitsgateway verhindert.

![Abbildung-11][Abbildung-11]

Das Sicherheitsgateway Bestandsnetze besteht aus einem VPN-Konzentrator und
einem Sicherheitsgateway (z. B. eine Firewall) auf der einen Seite und aus
einem VPN-Anschlusspunkt (VPN-Router und Firewall) im Rechenzentrum des
anzuschließenden Bestandsnetzes. Der VPN-Anschlusspunkt ist in der
betrieblichen Hoheit des Anbieters des Sicherheitsgateway Bestandsnetze. Am
anzuschließenden Standort wird ein bestehender Internetzugang vorausgesetzt.
Über das Internet wird ein IPSec-Tunnel vom VPN-Anschlusspunkt zum
VPN-Konzentrator aufgebaut und über den SZZP erfolgt die Anbindung an das
zentrale Netz der TI. Im Sicherheitsgateway, am VPN-Anschlusspunkt und am SZZP
erfolgt die Kontrolle und Durchsetzung der erlaubten Kommunikationsbeziehungen.
Das Accounting erfolgt im VPN-Anschlusspunkt.

##### GS-A_5507

Der Produkttyp Sicherheitsgateway Bestandsnetze MUSS den Anschluss von
mindestens 4 Bestandsnetzen gleichzeitig und voneinander unabhängig an einer
Instanz des Sicherheitsgateways ermöglichen. Das Sicherheitsgateway MUSS
mindestens als Stateful Inspection Firewall ausgeführt sein. Pro Bestandsnetz
MUSS ein separates Regelwerk unterstützt werden.Die Umgebungstrennung nach PU,
TU und RU erfolgt logisch auf der gleichen Hardware. **[\<=]**

Die gematik empfiehlt für den Produkttyp Sicherheitsgateway Bestandsnetze, die
Verwendung von BSI-zugelassenen IT-Sicherheitsprodukten und -systemen wie in
[BSI-Schrift 7164] aufgeführt.

Für weitere Informationen zum sicheren Einsatz von Komponenten in
Sicherheitsgateways wird auf die [BSI ISI-LANA] verwiesen.

##### A_13477

Das Sicherheitsgateway Bestandsnetze MUSS jede Verbindung zu einem
Bestandsnetzbetreiber durch eine Verschlüsselung absichern. Der Produkttyp
Sicherheitsgateway Bestandsnetze trägt die Verantwortung für die Anbindung
bis zum Tunnelendpunkt beim Bestandsnetzbetreiber. Soweit dazu eine Mitwirkung
des Bestandsnetzbetreibers notwendig ist, liegt es in der Verantwortung des
Sicherheitsgateways Bestandsnetze, dies mit dem Bestandsnetzbetreiber
abzustimmen. **[\<=]**

##### A_14199

Das Sicherheitsgateway Bestandsnetze MUSS entweder an mindestens zwei Standorten
einen active/standby Cluster aus VPN-Konzentratoren und Sicherheitsgateways
gemäß Abbildung Abb_VPN-Konzentrator_und_Sicherheitsgateway_Redundanz oder
einen stretched active/standby Cluster aus VPN-Konzentratoren und
Sicherheitsgateways über zwei Standorte verteilt implementieren.

Abbildung12: Abb_VPN-Konzentrator_und_Sicherheitsgateway_Redundanz

  **[\<=]**

##### A_14216

Das Sicherheitsgateway Bestandsnetze MUSS die VPN-Anschlusspunkte als zwei
separate, redundante Anschlüsse in den Räumlichkeiten des angeschlossenen
Bestandsnetzes implementieren. **[\<=]**

##### A_14217

Das Sicherheitsgateway Bestandsnetze SOLL VPN-Anschlusspunkte anbieten, die eine
Bandbreite (IPSec Verschlüsselungsleistung) von 100 Mbit/s bis 1 Gbit/s
unterstützen. **[\<=]**

##### A_14220

Das Sicherheitsgateway Bestandsnetze MUSS so dimensioniert sein und an sich
ändernde Lastsituationen angepasst werden, dass

 ---> UL

**[\<=]**

Bei Anpassungen muss der betriebliche Change-Prozess durchlaufen werden.

##### A_14218

Das Sicherheitsgateway Bestandsnetze MUSS die redundanten VPN-Anschlusspunkte so
implementieren, dass bei Ausfall des aktiven VPN-Anschlusspunktes ein Failover
auf den Standby VPN-Anschlusspunkt erfolgt. **[\<=]**

##### A_14219

Das Sicherheitsgateway Bestandsnetze MUSS die redundanten VPN-Konzentratoren und
die Sicherheitsgateways so implementieren, dass bei Ausfall der aktiven
Komponenten ein Failover auf die Standby Komponenten erfolgt. **[\<=]**

Die Komponenten VPN-Konzentrator und Sicherheitsgateway können in einem Gerät
realisiert sein.

##### A_18821

Das Sicherheitsgateway Bestandsnetze MUSS die Möglichkeit bieten eine
Datenvolumenerfassung je aufgerufener Ziel-IP-Adresse im Bestandsnetz in beide
Richtungen umzusetzen. Diese Volumenerfassung ist der gematik monatlich zu
überlassen. **[\<=]**

Die Festlegung für welche Zieladresse, im jeweiligen Bestandsnetz, eine
Datenvolumenerfassung einzurichten ist, erfolgt durch die gematik.

##### A_14232

Der Anbieter des Sicherheitsgateways Bestandsnetze MUSS für den Anschluss eines
Bestandsnetzes an die VPN-Anschlusspunkte die folgenden Anschlussvarianten je
Rechenzentrum unterstützen:

 ---> UL

**[\<=]**

### 5 Namensdienst

Der Namensdienst bildet die Namen von Hostsystemen und netzwerkfähigen
Applikationen in IP-Adressen ab und ermöglicht so die Identifizierung von
Zielsystemen innerhalb der TI. Zusätzlich können durch parametrisierte
Abfragen die URLs von Diensten in der TI ermittelt werden.

Die logische Struktur des DNS-Service beinhaltet einen geschlossenen,
hierarchisch gegliederten Namensraum, in dem die Adressen der
fachanwendungsspezifischen Dienste und der zentralen Dienste der TI-Plattform
enthalten sind. Darüber hinaus müssen FQDNs aus den Namensräumen der
Bestandsnetze sowie aus dem Namensraum des Internets (für die Adressen des
Zugangsdienstes und für den Zugriff von Clientsystemen auf Dienste im
Internet) aufgelöst werden.

### 5.1 Hostnamen

##### GS-A_3824

Anbieter von Produkttypen der Fachanwendungen sowie der zentralen TI-Plattform
MÜSSEN, für die netzwerkfähigen und zur Kommunikation innerhalb der TI
genutzten Außenschnittstellen, Hostnamen verwenden, die konform zu den
Vorgaben in [RFC1123#2.1] sind.

Die FQDN müssen von den Anbietern vergeben werden. Die einzelnen Label müssen
so gewählt werden, dass die resultierenden FQDN eindeutig sind.

Die IP-Adressen von Schnittstellen innerhalb der TI müssen per DNS-Abfrage
aufgelöst werden. IP-Adressen der Nameserver sind hiervon ausgenommen. **[\<=]**

### 5.2 Namensräume

##### GS-A_3828

Der Anbieter des Produkttyps Namensdienst MUSS in der TI (Produktivumgebung)
genau einen internen und geschlossenen Namensraum betreiben. In diesem
Namensraum MÜSSEN die Ressource Records der, netzwerkfähigen und zur
Kommunikation innerhalb der TI genutzten, Außenschnittstellen der
fachanwendungsspezifischen Dienste sowie der zentralen Dienste der TI-Plattform
verwaltet werden. **[\<=]**

Dieser geschlossene Namensraum wird im Folgenden Namensraum der TI genannt.

##### GS-A_4071

Der Anbieter des Produkttyps Namensdienst MUSS in der TI-Testumgebung genau
einen internen und geschlossenen Namensraum bereitstellen. In diesem Namensraum
MÜSSEN die Ressource Records der, netzwerkfähigen und zur Kommunikation
innerhalb der TI Testumgebung genutzten, Außenschnittstellen der Testsysteme
der fachanwendungsspezifischen Dienste sowie der zentralen Dienste der
TI-Plattform verwaltet werden. **[\<=]**

Für die Referenzumgebung werden hinsichtlich des Namensraums keine weiteren
Vorgaben getroffen.

Innerhalb der TI werden neben dem Namensraum der TI auch der Namensraum des
Transportnetzes, der Namensraum des Internets sowie die Namensräume der
Bestandsnetze durch Clientsysteme genutzt. Diese liegen jedoch nicht in der
Verantwortung der TI.

##### GS-A_3829

Der Konnektor MUSS Clientsystemen der Leistungserbringer die Namens- und
Adressauflösung für Namen und Adressen aus den Namensräumen Internet und der
Bestandsnetze über einen DNS-Forwarderermöglichen. Um dieResourceRecords des
VPN-Zugangsdienstes und den FQDN des CRL-Downloadpunktes  auflösen zu
können, MUSS der Konnektor die Nameserver (Transportnetz) abfragen.​​ **[\<=]**

### 5.3 Domainnamen- und Hierarchie

##### GS-A_3926-01

Der Anbieter des Produkttyps Namensdienst MUSS eine eigene DNS-Root und die von
der gematik festgelegten Top Level Domainen für den Namensraum der TI
bereitstellen. **[\<=]**

Die aktuell von der gematik festgelegten Top Level Domainnamen sind telematik.
ti-wa. und de.

##### GS-A_3927-01

Der Anbieter des Namensdienstes MUSS unter den von der gematik festgelegten Top
Level Domains für Anbieter von Diensten der TI und für Anbieter von Diensten
der weiteren Anwendungen des Gesundheitswesens sowie der Gesundheitsforschung
Second Level Domains und darunterliegende Domains bereitstellen.Der Anbieter
des Namensdienstes muss es ermöglichen, dass andere Anbieter von Diensten der
TI und Anbieter von Diensten der weiteren Anwendungen des Gesundheitswesens
sowie der Gesundheitsforschung eigene Second Level Domains und darunterliegende
Domains betreiben. **[\<=]**

##### GS-A_3928

Produkttypen die autoritativ Second Level Domains in der TI unter der Top Level
Domain „telematik.“betreiben, MÜSSEN gewährleisten, dass sich die Namen
der Second Level Domains an den Kurzformen der Produkttypnamen bzw. der
Fachanwendungsnamen orientieren. Unterhalb der Second Level Domains können
Anbieter der entsprechenden Dienste eigene Subdomains mit selbst gewählten
Namen verwalten. **[\<=]**

##### GS-A_4072-01

Der Anbieter des Produkttyps Namensdienst MUSS eine eigene DNS-Root und die von
der gematik festgelegten Top Level Domainen für den Namensraum der TI in der
Testumgebung und in der Referenzumgebung bereitstellen.Der Anbieter des
Produkttyps Namensdienst MUSS sicherstellen, dass die übrigen Domainnamen und
die Hierarchie des Namensraums der Testumgebung und der Referenzumgebung den
Domainnamen und der Hierarchie der Produktivumgebung entsprechen. **[\<=]**

Wenn Anbieter von fachanwendungsspezifischen Diensten oder von Produkttypen der
zentralen TI-Plattform eigene Subzonen im Namensraum der TI betreiben, müssen
grundsätzlich alle Anforderungen, die für den Produkttyp Namendienst im
Rahmen der Zonenverwaltung gelten, mit erfüllt werden. Dies sind insbesondere
Anforderungen an den Einsatz von DNSSEC, Anforderungen an die Verfügbarkeit
und Performance sowie an das Monitoring. Ausgenommen sind Anforderungen an die
Verwaltung des Trust Anchor des Namensraums der TI. Die zu erfüllenden
Anforderungen werden dem Anbieter im Rahmen der Antragstellung zur Verwaltung
einer eigenen Subdomain in der TI durch die gematik mitgeteilt.

### 5.4 DNS-Topologie

Die DNS-Topologie ergibt sich aus den Funktionalitäten, die an den
verschiedenen Punkten in der TI benötigt werden.

In der TI und um Verbindungen in die TI aufzubauen werden Nameserver mit
folgender Topologie und Funktionalität eingesetzt:

 ---> TABLE

Die folgende Abbildung zeigt die Abfragebeziehungen zwischen den Nameservern.

![Abbildung-13][Abbildung-13]

Die grau dargestellten Nameserver sind optional. Der blau dargestellte
Nameserver liegt außerhalb der Verantwortung der TI. Die innere Struktur der
Nameserver-Implementierungen wird in den jeweiligen Produkttypspezifikationen
definiert. Rekursive queries zwischen Nameservern werden nicht unterstützt.

##### GS-A_4809

Die Nameserver-Implementierungen in der TI MÜSSEN, wenn sie eine Zone im
Namensraum der TI verwalten oder wenn sie als Caching Nameserver implementiert
sind, physisch redundant durch 2 aktive Nameserver bereitgestellt werden. **[\<=]**

##### GS-A_3932

Produkttypen die innerhalb der TI DNS-Resolver implementieren und Anbieter
weiterer Anwendungen des Gesundheitswesens mit Zugriff auf Dienste der TI,
MÜSSEN zur Auflösung von FQDNs im Namensraum der TI die in der DNS-Topologie
der TI gemäß Abbildung Abb_DNS_Topologie_der_TI am nächsten stehenden
Nameserver abfragen.Für Stub-Resolver der Clientsysteme in den Organisationen
des Gesundheitswesens ist dies der Konnektor.Für Resolver der
fachanwendungsspezifischen Dienste sind dies die Nameserver (TI) des
Namensdienstes oder, wenn Zone Delegation für die Second Level Domain oder in
der Hierarchie darunterliegende Domains genutzt wird, die Nameserver (TI), die
die delegierte Zone verwalten.Für Resolver der zentralen Dienste der
TI-Plattform sind dies die Nameserver des Namensdienstes.Zur Auflösung von
FQDN in IP-Adressen verwendet der Stub-Resolver des Konnektors den Nameserver
(Forwarder) des Konnektors. Dies gilt für die Namensräume TI, Transportnetz
und Bestandsnetze.Der Nameserver des Konnektors muss für den Namensraum der TI
die Caching Nameserver (TI) des für ihn zuständigen VPN-Zugangsdienstes
abfragen. Für die Namensräume von Bestandsnetzen muss der Nameserver die
Nameserver des entsprechenden Bestandsnetzes abfragen. Für den Namensraum des
Internet sollen die vom VPN-Zugangsdienst bereitgestellten Nameserver (SIS)
für den Namensraum des Internet abgefragt werden.Die Caching Nameserver (TI)
des VPN-Zugangsdienstes müssen die Nameserver (TI) des Namensdienstes und
Nameserver (TI), die delegierte Zonen im Namensraum der TI verwalten,
abfragen.In den Resolver-Konfigurationen müssen mindestens 2 zuständige
Nameserver eingetragen werden. Ausgenommen davon ist der Stub-Resolver des
Konnektors. **[\<=]**

### 5.5 Dienstlokalisierung

Um auf die zentralen Dienste KSR und TSL-Dienst zugreifen zu können, wird die
Lokalisierung über DNS Service Discovery unterstützt.

##### GS-A_5024

Der Anbieter des KSR MUSS DNS SRVResourceRecords gemäß TabelleTab_KSR_SRV-RR
im Namensraum TI verwalten. Wenn die Domain „ksr.telematik“ nicht durch den
Anbieter des KSR verwaltet wird, erfolgt der Betrieb dieser Zone beim Anbieter
des Namensdienstes und die SRVResourceRecords müssen an den Anbieter des
Namensdienstes zur Eintragung in die Nameserverkonfiguration übergeben werden.

Tabelle17:Tab_KSR_SRV-RR

 ---> TABLE

**[\<=]**

Weitere Anwendungen des Gesundheitswesens sowie der Gesundheitsforschung können
im Namensraum der TI die Zugangspunkte zu von ihnen bereitgestellten Diensten
über DNS-based Service Discovery gemäß [RFC6763] für Clientsysteme bekannt
machen. Für die Suche nach den Zugangspunkten der Dienste wird die Domain
„dnssd.ti-wa.“ festgelegt.

##### GS-A_5623

Der Anbieter des Namensdienstes MUSS die Domain „dnssd.ti-wa.“ betreiben und
auf Wunsch von Anbietern weiterer Anwendungen des Gesundheitswesens sowie der
Gesundheitsforschung Einträge zur Dienstlokalisierung gemäß [RFC6763]
Tab_Namensdienst_DNSSD_für_WA vornehmen. **[\<=]**

 ---> TABLE

### 5.6 Schnittstellen I_DNS_Name_Resolution und I_DNS_Service_Localization

Beide Schnittstellen werden durch die Standard-DNS-Funktionalität technisch
umgesetzt und daher zusammen in einem Abschnitt betrachtet.

### 5.6.1 Umsetzung

Neben den grundlegenden Funktionen zur Namensauflösung wird für Nameserver im
Namensraum der TI die Unterstützung von DNSSEC und von DNS-SD gefordert.

##### GS-A_3834

Produkttypen die Nameserver implementieren, MÜSSEN [RFC1034], [RFC1035] für
das DNS-Protokoll und [RFC3596] für IPv6-Anpassungen unterstützen.Zusätzlich
müssen diese Nameserver-Implementierungen die folgenden Aktualisierungen und
Ergänzungen zu den oben genannten RFCs unterstützen: [RFC1123] Abschnitt 6.1,
[RFC1982], [RFC1995], [RFC1996], [RFC2181], [RFC2308], [RFC6891], [RFC2782],
[RFC2930], [RFC2931], [RFC3225].Die Nameserver-Implementierungen müssen neben
UDP auch TCP unterstützen.​​ **[\<=]**

##### GS-A_5199

Produkte, die DNSSEC im Namensraum Internet nutzen und den Trust Anchor der IANA
zur Validierung von DNS-Antworten verwenden, MÜSSEN den DNSSEC-Vertrauensanker
gemäß [RFC5011] aktualisieren. **[\<=]**

##### GS-A_3842-01

Anbietervon Produkttypen, die Nameserver implementieren, MÜSSEN zur Abfrage
anderer Nameserver iterative queries verwenden. Recursive queries DÜRFEN NICHT
verwendet werden. Der Konnektor, der Basis- und der KTR-Consumer sind von
dieser Regelung ausgenommen. **[\<=]**

##### GS-A_4849

Der Nameserver des Konnektors MUSS zur Auflösung von FQDNs die entsprechenden
Nameserver mit recursive queries anfragen. **[\<=]**

##### GS-A_3930

Anbieter, die autoritative Nameserver implementieren, MÜSSEN initial für
jedenResource Record eine Time To Live (TTL) von 86400 einstellen, wenn es
keine anderslautenden Festlegungen zur TTL für den jeweiligen Resource Record
gibt. Die TTL-Werte können im Rahmen des Change-Management geändert werden. **[\<=]**

##### GS-A_3835

Produkttypen dieautoritativeNameserver implementieren, MÜSSEN DNS Service
Discovery (DNS-SD) gemäß dem [RFC6763] unterstützen. **[\<=]**

##### GS-A_4810

Anbieter von Diensten in der TI, die ihren Dienst über DNS-SD lokalisieren
lassen, MÜSSEN die Vorgaben an das Format von TXT Resource Records
umsetzen.Der Schlüssel „txtvers“ muss  mit einem Wert angegeben
sein.Wenn der Dienst über eine URL lokalisiert werden soll, so muss der
Schlüssel „path“ mit dem Wert des URL-Pfads angegeben sein. Der URL-Pfad
muss mit einem „/“ beginnen und mit einem „/" terminieren.  Ein leerer
URL-Pfad muss als „/“ angegeben werden.Weitere Schlüssel=Wert-Strings
können  angegeben werden. **[\<=]**

##### GS-A_4811

Der Konnektor MUSS TXT Resource Records den Vorgaben entsprechend interpretieren.

Der Schlüssel „txtvers“ ist mit einem Wert angegeben.

Wenn der Dienst über eine URL lokalisiert wird, so ist der Schlüssel
„path“ mit dem Wert des URL-Pfads angegeben. Der URL-Pfad beginnt mit einem
„/“. Ein leerer URL-Pfad ist als „/“ angegeben.

Weitere Schlüssel=Wert-Strings können nach Vorgabe des zu lokalisierenden
Dienstes angegeben sein. **[\<=]**

##### GS-A_3931

Produkttypen die autoritative Nameserver implementieren, MÜSSEN [RFC4033],
[RFC4034] und [RFC4035] für DNSSEC unterstützen. Der Konnektor ist hiervon
ausgenommen.Zusätzlich müssen diese Nameserver-Implementierungen
Aktualisierungen und Ergänzungen zu den oben genannten RFCs unterstützen.
Dies sind Abschnitt 6.1 in [RFC1123], [RFC1982], [RFC1995], [RFC1996],
[RFC2181], [RFC2308], [RFC6891], [RFC2782], [RFC2930], [RFC2931], [RFC3225],
[RFC5155].​​ **[\<=]**

##### GS-A_5132

Der Anbieter des Namensdienstes MUSS den DNSSEC Trust Anchor der TI für die
Produktionsumgebung basierend auf der Top Level Domain der Produktionsumgebung
der TI "telematik." erstellen. **[\<=]**

##### GS-A_5133

Der Anbieter des Namensdienstes MUSS den DNSSEC Trust Anchor der TI für die
Test- und Referenzumgebung basierend auf der Top Level Domain der Test- und
Referenzumgebung "telematik-test." erstellen. **[\<=]**

##### GS-A_3839

Anbieter von Produkttypen die Zonen im Namensraum der TI bereitstellen, MÜSSEN
diese Zonen mittels DNSSEC sichern. Die Sicherung MUSS auf Basis des Trust
Anchors des Anbieters des Produkttyps Namensdienst erfolgen.

DNSSEC Zone Signing Keys (ZSK) im Namensraum der TI müssen nach Ablauf von 120
Tagen ersetzt werden. Key Signing Keys (KSK) im Namensraum der TI müssen nach
12 Monaten ausgetauscht werden. Hinsichtlich der zur Generierung der
asymmetrischen ZSK und KSK Schlüsselpaare in der TI zu verwendenden
Algorithmen und Schlüssellängen gelten die Festlegungen aus [gemSpec_Krypt].

Die Empfehlungen aus [RFC6781] müssen beachtet werden. **[\<=]**

Es wird empfohlen validierende DNS Resolver so zu konfigurieren, dass DNS
Responses aus folgenden Domänen (inkl. Subdomänen) validiert werden müssen:

 ---> UL

##### GS-A_4879

Anbieter von Produkttypen die Zonen im Namensraum Internet bereitstellen,
MÜSSEN diese Zonen mittels DNSSEC sichern. Die Sicherung MUSS auf Basis des
Trust Anchors für das Internet (bereitgestellt durch die IANA) erfolgen.

DNSSEC Zone Signing Keys (ZSK) im Namensraum Internet müssen nach Ablauf von
120 Tagen ersetzt werden. Key Signing Keys (KSK) im Namensraum Internet müssen
nach 12 Monaten ausgetauscht werden. Hinsichtlich der, zur Generierung der
asymmetrischen ZSK und KSK Schlüsselpaare, zu verwendenden Algorithmen und
Schlüssellängen gelten die Festlegungen aus [gemSpec_Krypt].

Die Empfehlungen aus [RFC6781] müssen beachtet werden. **[\<=]**

##### GS-A_3841

Anbieter von Produkttypen die Zonen im Namensraum der TI bereitstellen, MÜSSEN
Zonentransfers mit Transaction Signature (TSIG) gemäß [RFC2845] und [RFC4635]
absichern.

Je Nameserver-Paar muss ein eigener symmetrischer Schlüssel (1:1 Beziehung)
verwendet werden. Hinsichtlich des zu verwendenden Algorithmus und der
Schlüssellänge gelten die Festlegungen aus [gemSpec_Krypt]. **[\<=]**

##### GS-A_5089

Anbieter, die autoritative Nameserver implementieren, MÜSSEN private
Schlüsselsicher speichern und ihr Auslesen verhindern. **[\<=]**

##### GS-A_5582

Der Produkttyp Namensdienst MUSS mindestens zwei Caching Nameserver TI (full
service resolver) bereitstellen, die rekursive DNS-Anfragen zur Auflösung von
Namen im Namensraum TI beantworten, und Antworten entsprechend der TTL
zwischenspeichern (Caching). Sie MÜSSEN sich netzwerktechnisch im Netzbereich
„zentrale Dienste“ befinden und an das zentrale Netz der TI angeschlossen
sein. **[\<=]**

Der Caching Nameserver TI erlaubt rekursive Anfragen. Er leitet die Anfragen an
die autoritativen Nameserver der TI weiter.

### 5.6.2 Nutzung

##### GS-A_3832

Produkttypen die DNS-Resolver implementieren, MÜSSEN [RFC1034], [RFC1035] für
das DNS-Protokoll und [RFC3596] für IPv6-Anpassungen unterstützen.

Zusätzlich müssen diese Resolver-Implementierungen die folgenden
Aktualisierungen und Ergänzungen zu den oben genannten RFCs
unterstützen:[RFC1123] Abschnitt 6.1, [RFC2181], [RFC2308], [RFC6891],
[RFC6891],[RFC2845], [RFC5452] und [RFC3225].

Der Konnektor ist von dieser Anforderung ausgenommen. **[\<=]**

### 5.7 Anforderungen an den Produkttyp Namensdienst

##### GS-A_4812

Der Produkttyp Namensdienst MUSS die Schnittstellen gemäß
TabelleTab_PT_Namensdienst_Schnittstellenimplementieren („bereitgestellte“
Schnittstellen) und nutzen („benötigte“ Schnittstellen).

Tabelle19:Tab_PT_Namensdienst_Schnittstellen

 ---> TABLE

​​​​ **[\<=]**

##### GS-A_5347

Der Namensdienst MUSS DNSSEC Key- und Algorithm-Rollover gemäß den Vorgaben
des GBV durchführen. Dies betrifft das Setzen der Schlüsselzeitparameter
(Publicationtime, Activationtime, Revocationtime, Inactivationtime und
Deletiontime) für den neuen und den alten Schlüssel sowie den
Änderungszeitpunkt der TSL. **[\<=]**

### 5.7.1 Schnittstellen P_DNS_Name_Entry_Announcement und P_DNS_Service_Entry_Announcement

##### GS-A_4814

Der Anbieter des Namensdienstes MUSS einen Prozess implementieren, der es
Anbietern von fachanwendungsspezifischen Diensten und Anbietern von zentralen
Diensten der TI-Plattform ermöglicht, DNS Resource Records innerhalb des
Namensraums der TI bekannt zu machen.

Der Prozess muss dokumentiert sein und dem GBV zur Freigabe vorgelegt werden.

Zusätzlich muss der Anbieter des Namensdienstes alle Anbietern von Diensten in
der TI informieren, wie sie diesen Prozess nutzen können. **[\<=]**

### 5.7.2 Schnittstelle P_DNSSEC_Key_Distribution

##### GS-A_4815

Der Anbieter des Namensdienstes MUSS einen Prozess implementieren, der es
ermöglicht den Hash des DNSSEC Trust Anchor für den Namensraum TI an Resolver
und Nameserver der fachanwendungsspezifischen Dienste und der zentralen Dienste
der TI-Plattform sowie an Nameserver der Konnektoren und Hersteller von
Konnektoren zu verteilen.Die Empfehlungen aus [RFC6781] müssen beachtet
werden.Der Prozess muss dokumentiert sein und dem GBV zur Freigabe vorgelegt
werden.Nach diesem Prozess muss initial der Hash des DNSSEC Trust Anchor für
den Namensraum TI an den GBV, an Anbieter von Resolver und Nameserver der
fachanwendungsspezifischen Dienste und der zentralen Dienste der TI-Plattform
sowie an Hersteller von Konnektoren verteilt werden. Das Format für die
Verteilung des DNSSEC Trust Anchor muss dem IANA XML-Format zur Verteilung des
Internet DNSSEC Trust Anchor entsprechen. Die Aktualisierung des DNSSEC Trust
Anchor für den Namensraum TI muss gemäß [RFC5011] automatisch
erfolgen.Zusätzlich muss der Trust Anchor bei Aktualisierungen dem GBV zur
Verfügung gestellt werden. Die Aktualisierung des Trust Anchor für den
Namensraum TI muss über einen genehmigungspflichtigen Change gemäß
[gemRL_Betr_TI] erfolgen.Die beim DNSSEC Trust Anchor Wechsel zu verwendenden
Timing-Parameter

 ---> UL

müssen konfigurierbar sein und mit dem GBV abgestimmt werden.​​ **[\<=]**

##### GS-A_4885-01

DerAnbieter des Namensdienstes MUSS den DNSSEC Trust Anchor der TI nach
Kompromittierung aktualisieren. Der bisherige DNSSEC Trust Anchor MUSS für
einen abgestimmten Übergangszeit gültig bleiben. **[\<=]**

##### GS-A_4816

Hersteller von Konnektoren MÜSSEN, wenn der Konnektor DNSSEC Antworten im
Namensraum TI validiert, initial bei der Herstellung den Hash des aktuellen
DNSSEC Trust Anchor für den Namensraum TI im DNS Forwarder des Konnektors
eintragen. Updates der Software des Konnektors müssen den Hash des aktuellen
DNSSEC Trust Anchor für den Namensraum TI beinhalten.Die Aktualisierung des
DNSSEC Trust Anchor für den Namensraum TI muss im Konnektor gemäß [RFC5011]
automatisch erfolgen. **[\<=]**

##### GS-A_4817

Anbieter von Produkttypen der Fachanwendungen sowie der zentralen TI-Plattform
MÜSSEN initial bei der Inbetriebnahme den Hash des aktuellen DNSSEC Trust
Anchor für den Namensraum TI in der Konfiguration ihrer Resolver- und
Nameserver-Implementierungen eintragen und sicher speichern.

Die Aktualisierung des DNSSEC Trust Anchor für den Namensraum TI muss gemäß
[RFC5011] automatisch erfolgen können. **[\<=]**

##### GS-A_4847

Anbieter von VPN-Zugangsdiensten MÜSSEN den Namensraum Transportnetz per DNSSEC
sichern. **[\<=]**

##### GS-A_5037

Der Anbieter VPN-Zugangsdienstes MUSS bei Verwendung eines vom Internet
verschiedenen Transportnetzes einen Prozess implementieren, der es ermöglicht
den Hash des DNSSEC Trust Anchor für den Namensraum Transportnetz an Betreiber
von Konnektoren zu verteilen. **[\<=]**

##### GS-A_4848

Wenn der Konnektor DNSSEC-Antworten für den Namensraum Transportnetz validiert,
dann MUSS der Konnektor ermöglichen, dass der aktuelle DNSSEC Trust Anchor
für den Namensraum Transportnetz im DNS Forwarder des Konnektors eingetragen
werden kann. Wenn der DNSSEC Trust Anchor für den Namensraum Transportnetz
eingetragen ist, dann MÜSSEN die Antworten vom Nameserver Transportnetz durch
den Konnektor validiert werden.Die Aktualisierung des DNSSEC Trust Anchor für
den Namensraum Transportnetz muss im Konnektor gemäß [RFC5011] automatisch
erfolgen. **[\<=]**

### 5.7.3 Schnittstelle P_DNS_Zone_Delegation

##### GS-A_4818

Der Anbieter des Namensdienstes MUSS einen Prozess implementieren, der es
Anbietern von fachanwendungsspezifischen Diensten und Anbietern von zentralen
Diensten der TI-Plattform ermöglicht, eigene DNS-Subdomains innerhalb des
Namensraums der TI zu betreiben.

Der Prozess muss dokumentiert sein und dem GBV zur Freigabe vorgelegt werden.

Zusätzlich muss der Anbieter des Namensdienstes alle Anbietern von Diensten in
der TI informieren, wie sie diesen Prozess nutzen können. **[\<=]**

### 5.7.4 Sonstige Anforderungen

##### GS-A_3838

Der Anbieter des Produkttyps Namensdienst MUSS den Trust Anchor für den
Namensraum der TI erzeugen und verwalten. **[\<=]**

##### GS-A_4813

Der Produkttyp Namensdienst MUSS sicherstellen, dass vom Namensdienst aus, über
das Zentrale Netz der TI, nur erlaubte IP-Kommunikation in Richtung
Produkttypen der TI-Plattform und fachanwendungsspezifischer Dienste gesendet
wird.

Zur erlaubten Kommunikation des Namensdienstes zählen:

 ---> UL

**[\<=]**

##### GS-A_4808

Die Möglichkeit, Zonentransfers durchzuführen, ohne dass dies in der Topologie
durch den Anbieter vorgesehen ist, MUSS auf allen Nameserver-Implementierungen
im Namensraum der TI ausgeschlossen sein. **[\<=]**

##### A_17795

Der Namensdienst MUSS den Betrieb von DNS-Zonen als hidden primary auf
Test-Instanzen der gematik in den Betriebsumgebungen RU und TU unterstützen
und auf Anfrage der gematik umsetzen. **[\<=]**

##### GS-A_5583

Ein Anbieter eines an die TI angeschlossenen Netzes des Gesundheitswesens mit
weiteren Anwendungen des Gesundheitswesens ohne Zugriff auf Dienste der TI MUSS
den Namensraum des an die TI angeschlossenen Netzes des Gesundheitswesens mit
anderen Anwendungen des Gesundheitswesens selber verwalten und dafür Caching
Nameserver (recursion available) im an die TI angeschlossenen Netz des
Gesundheitswesens mit anderen Anwendungen des Gesundheitswesens bereitstellen.
**[\<=]**

##### GS-A_5584-01

Ein Anbieter eines an die TI angeschlossenen Netzes des Gesundheitswesens mit
weiteren Anwendungen des Gesundheitswesens ohne Zugriff auf Dienste der TI MUSS
dem Anbieter des zentralen Netzes der TI die Informationen über den Namen des
an die TI angeschlossenen Netzes des Gesundheitswesens mit anderen Anwendungen
des Gesundheitswesens, den verwendeten öffentlichen IP-Adressraum, den
Namensraum sowie den Caching Nameserver bereitstellen.Die Meldeflicht
der öffentlichen IP-Adressen entfällt, wenn der Anbieter eine der WANDA
Basic zugewiesenen TI-IPv4-Adressen verwendet. **[\<=]**

##### GS-A_5585

Ein Anbieter eines an die TI angeschlossenen Netzes des Gesundheitswesens mit
weiteren Anwendungen des Gesundheitswesens ohne Zugriff auf Dienste der TI MUSS
dem Anbieter des Sicherheitsgateways Bestandsnetze, über dass das Netz des
Anbieters an die TI angebunden wird, Informationen zu den am Sicherheitsgateway
freizuschaltenden Protokollen und Ports für das an die TI anzuschließende
Netz des Gesundheitswesens mit anderen Anwendungen des Gesundheitswesens
bereitstellen. **[\<=]**

##### GS-A_5586

Ein Anbieter eines an die TI angeschlossenen Netzes des Gesundheitswesens mit
weiteren Anwendungen des Gesundheitswesens ohne Zugriff auf Dienste der TI MUSS
mit dem Anbieter des Sicherheitsgateways Bestandsnetze, über dass das Netz des
Anbieters an die TI angebunden wird, abstimmen, wie der netztechnische
Anschluss an das Sicherheitsgateway erfolgen soll und diesen bereitstellen.
**[\<=]**

### 6 Zeitdienst

Der Zeitdienst in der TI basiert auf dem Network Time Protocol (NTP) und
ermöglicht es, eine einheitliche Zeit innerhalb der TI zu nutzen.

Dabei synchronisiert sich der Produkttyp Zeitdienst mit der gesetzlichen
Zeitinformation. Diese wird über mehrere Stufen in der gesamten TI verteilt
und zur Abfrage bereitgestellt.

### 6.1 NTP-Topologie

Die NTP-Topologie ergibt sich aus der Netztopologie und dem daraus abgeleiteten
minimalen Synchronisierungsabstand. Die gewählte Topologie berücksichtigt die
Lastverteilung der Konnektoren auf die VPN-Zugangsdienste.

Die folgende Abbildung zeigt die Beziehungen zwischen den NTP-Servern. Die grau
dargestellten NTP-Server sind optional. Die blau dargestellte Zeitquelle liegt
außerhalb der Verantwortung der TI. Es erfolgt keine Synchronisation zwischen
Stratum-2-NTP-Servern. Die innere Struktur (Anzahl der NTP-Server-Instanzen)
der NTP-Server-Implementierungen wird in den jeweiligen
Produkttypspezifikationen definiert.

![Abbildung-14][Abbildung-14]

##### GS-A_3940

Der Produkttyp Zeitdienst MUSS Stratum-1-NTP-Server implementieren.
Stratum-1-NTP-Server MÜSSEN sich mit der gesetzlichen Zeitquelle
synchronisieren. **[\<=]**

##### GS-A_3941

Der Produkttyp VPN-Zugangsdienst MUSS Stratum-2-NTP-Server bereitstellen, die
sich mit allen Stratum-1-NTP-Servern des Produkttyps Zeitdienst synchronisieren
MÜSSEN. **[\<=]**

##### GS-A_3942

Der Produkttyp Konnektor MUSS einen Stratum-3-NTP-Server implementieren, der
sich bei bestehender Verbindung mit Stratum-2-NTP-Servern des Produkttyps
VPN-Zugangsdienst synchronisieren MUSS. **[\<=]**

### 6.2 Schnittstelle I_NTP_Time_Information

### 6.2.1 Umsetzung

##### GS-A_3933

Produkttypen die innerhalb der TI NTP-Server implementieren, MÜSSEN das
NTP-Protokoll Version 4 gemäß [RFC5905] unterstützen. **[\<=]**

##### GS-A_3935

Produkttypen die innerhalb der TI NTP-Server implementieren, MÜSSEN zur Abwehr
von nicht böswilligen NTP-basierten Denial-of-Service bzw.
Distributed-Denial-of-Service Angriffen das Kiss-o´-Death-Verfahren einsetzen. **[\<=]**

##### GS-A_3936

Produkttypen die innerhalb der TI NTP-Server implementieren, DÜRFEN IBURST
NICHT einsetzen. **[\<=]**

##### GS-A_3938

Produkttypen die innerhalb der TI NTP-Server implementieren, MÜSSEN gemäß
[RFC5905] den Association Mode Client für NTP-Anfragen bei NTP-Servern mit
niedrigerem Stratum Wert und den Association Mode Server für Antworten auf
NTP-Anfragen verwenden. Das Polling-Intervall MUSS nach dem clock discipline
algorithm dynamisch eingestellt werden. **[\<=]**

##### GS-A_3945

Produkttypen die innerhalb der TI NTP-Server implementieren, DÜRFEN zur Abfrage
anderer NTP-Server NICHT SNTP einsetzen. **[\<=]**

##### GS-A_4074

Produkttypen die Stratum-1- und -2-NTP-Server in der TI implementieren MÜSSEN
gewährleisten, dass die durch sie verteilte Zeitinformation nicht mehr als
330ms von der Zeitinformation der darüber liegenden Stratum Ebene abweicht. **[\<=]**

Da der Konnektor nicht immer online ist oder ggf. auch nie online ist
(Offline-Szenario), gelten hier andere Anforderungen an die Genauigkeit des
NTP-Servers.

##### GS-A_4075

Der Hersteller des Konnektors SOLL für die durch ihn implementierten NTP-Server
gewährleisten, dass die durch sie verteilte Zeitinformation nicht mehr als
330ms von der Zeitinformation der darüber liegenden Stratum Ebene abweicht. **[\<=]**

### 6.2.2 Nutzung

##### GS-A_3934

Produkttypen die innerhalb der TI NTP-Clients implementieren und Anbieter
weiterer Anwendungen des Gesundheitswesens mit Zugriff auf Dienste der TI,
MÜSSEN das NTP-Protokoll Version 4 gemäß [RFC5905] unterstützen. **[\<=]**

Um auf der Clientseite Falseticker gemäß [RFC5905] erkennen zu können,
müssen alle Stratum-1-NTP-Server abgefragt werden.

##### GS-A_4819

Fachanwendungsspezifische Dienste SOLLEN sich mit den Stratum-1-NTP-Servern des
Produkttyps Zeitdienst synchronisieren. Dies beinhaltet grundsätzlich alle an
der Diensterbringung des fachanwendungsspezifischen Dienstes beteiligten
Komponenten.

Wenn sich Fachanwendungsspezifische Dienste mit den Stratum-1-NTP-Servern des
Produkttyps Zeitdienst synchronisieren, so müssen immer alle
Stratum-1-NTP-Server abgefragt werden.

Fachanwendungsspezifische Dienste können einen oder mehrere
Stratum-2-NTP-Server betreiben, die sich mit allen Stratum-1-NTP-Servern
synchronisieren. Die an der Diensterbringung beteiligten Komponenten
synchronisieren sich dann mit den eigenen Stratum-2-NTP-Servern. **[\<=]**

##### GS-A_4820

Produkttypen, die zentrale Dienste der TI-Plattform bereitstellen, SOLLEN sich
mit allen Stratum-1-NTP-Servern des Produkttyps Zeitdienst synchronisieren.
Dies beinhaltet alle an der Diensterbringung des Produkttypen beteiligten
Komponenten.

Folgende Ausnahmen gelten:

 ---> UL

**[\<=]**

##### GS-A_4821

Produkttypen, die zentrale Dienste der TI-Plattform bereitstellen, MÜSSEN, wenn
sie sich nicht mit den Stratum-1-NTP-Servern des Produkttyps Zeitdienst
synchronisieren, ein Ersatzverfahren einsetzen, dass eine maximale Abweichung
von einer Sekunde gegenüber der gesetzlichen Zeit gewährleistet. **[\<=]**

##### GS-A_3937

Produkttypen die innerhalb der TI NTP-Clients implementieren und Anbieter
weiterer Anwendungen des Gesundheitswesens mit Zugriff auf Dienste der TI, die
einen NTP-Client für die TI Implementieren, MÜSSEN gemäß [RFC5905] den
Association Mode Client verwenden und das Polling-Intervall nach dem clock
discipline algorithm dynamisch einstellen. **[\<=]**

### 6.3 Anforderungen an den Produkttyp Zeitdienst

##### GS-A_4822

Der Produkttyp Zeitdienst MUSS die Schnittstellen gemäß
TabelleTab_PT_Zeitdienst_Schnittstellenimplementieren („bereitgestellte“
Schnittstellen) und nutzen („benötigte“ Schnittstellen).

Tabelle20:Tab_PT_Zeitdienst_Schnittstellen

 ---> TABLE

Die Client-Funktionalität von mindestens einer der drei optionalen
Schnittstellen muss implementiert werden.​​​​ **[\<=]**

Die Synchronisation mit der gesetzlichen Zeit erfolgt über den Zeitsignalsender
DCF77 der Physikalisch-Technischen Bundesanstalt (PTB). Die dazugehörige
Schnittstelle wird nicht durch die TI bereitgestellt und daher nicht in diesem
Dokument beschrieben.

Die Stratum-1-NTP-Server synchronisieren sich mittels jeweils eines
Standard-DCF77-Empfängers als gesetzliche Zeitquelle.

##### GS-A_4823

Alle Stratum-1-NTP-Server des Produkttyps Zeitdienst MÜSSEN sich im
ungestörten Betrieb mit der gesetzlichen Zeit der Bundesrepublik Deutschland
über den Zeitsignalsender DCF77 synchronisieren.

Bei Ausfall oder Störung des DCF77-Senders MUSS eine Zeitquelle gemäß Tabelle
Tab_PT_Zeitdienst_vertrauenswürdige_Zeitquellen zur Synchronisierung genutzt
werden. **[\<=]**

 ---> TABLE

##### GS-A_4824

Der Produkttyp Zeitdienst MUSS vier aktive Stratum-1-NTP-Server bereitstellen,
die mit der gesetzlichen Zeitquelle synchronisiert sind. **[\<=]**

##### GS-A_4825

Der Produkttyp Zeitdienst MUSS sicherstellen, dass vom Zeitdienst aus, über das
Zentrales Netz der TI, ausschließlich erlaubte IP-Kommunikation in Richtung
Produkttypen der TI-Plattform und fachanwendungsspezifischer Dienste gesendet
wird.

Zur erlaubten Kommunikation des Zeitdienstes zählen:

 ---> UL

**[\<=]**

##### GS-A_4826

Der Anbieter des Zeitdienstes MUSS die Stratum-1-NTP-Server hinsichtlich der
bereitgestellten Zeitinformation überwachen.

Die Überwachung muss alle 5 Minuten erfolgen. Die von den Stratum-1-NTP-Servern
bereitgestellten Zeitinformationen dürfen nicht mehr als 100ms voneinander
abweichen. Wenn die Zeitinformationen 3 Mal hintereinander mehr als 100ms
voneinander abweichen, gilt dies als Prio-3-Störung gemäß [gemRL_Betr_TI]. **[\<=]**

##### GS-A_4827

Der Anbieter des Zeitdienstes MUSS die von den Stratum-1-NTP-Servern
bereitgestellten Zeitinformationen mit einer vertrauenswürdigen
Referenzzeitquelle gemäß Tabelle
Tab_PT_Zeitdienst_vertrauenswürdige_Zeitquellen vergleichen.

Die Überwachung muss alle 5 Minuten erfolgen. Wenn die Zeitinformation eines
oder mehrerer Stratum-1-Server der TI mehr als 500ms von der
vertrauenswürdigen Referenzzeitquelle abweichen, gilt dies als Störung. Tritt
die Störung 3 Mal hintereinander auf, so muss sie als Prio-3-Störung gemäß
[gemRL_Betr_TI] behandelt werden. Ab einer Abweichung von 1000ms ist die
Störung als Prio-2-Störung gemäß [gemRL_Betr_TI] zu behandeln. **[\<=]**

### 7 Hosting

Der Anbieter zentrale Plattformdienste (AZPD) bietet für Dritte einen
Hosting-Service an. Dadurch soll der Zugang zur TI erleichtert werden. In
diesem Kapitel werden Anforderungen formuliert, die vom Hosting-Service
erfüllt werden müssen.

Berechtigt den Hosting-Service zu nutzen, sind grundsätzlich alle Teilnehmer,
die Dienste einer gesetzlichen Anwendung, sichere Übermittlungsverfahren,
AdV-Server oder einen zentralen Dienst der TI-Plattform anbieten oder
Teilnehmer, die die Nutzungsvoraussetzungen der TI für weitere Anwendungen des
Gesundheitswesens sowie für die Gesundheitsforschung gemäß [gemRL_NvTIwA]
erfüllen. Hosting wird für die RU, TU und PU angeboten. Voraussetzung für
die Integration in die TU ist ein Zulassungsantrag sowie die Erfüllung der
Voraussetzungen in [gemKPT_Test]. Für die PU erfolgt die Freischaltung der
Firewallregeln am SZZP erst nach erfolgreicher Zulassung bzw.
Bestätigung sowie dem Abschluss der erforderlichen Anbindungs- und ggf.
Nutzungsverträge.

Der Hosting-Nehmer ruft den Hosting-Service des Hosting-Anbieters auf und
bezahlt entsprechend der vereinbarten Leistungen. Der AZPD ist ein
Hosting-Anbieter. Es können auch andere Anbieter Hosting-Services anbieten.

##### A_14503

Der Anbieter des Hosting-Service MUSS dem Hosting-Nehmer mindestens die
folgenden Leistungen anbieten und die Preise für die angebotenen
Leistungsklassen und nutzbaren Bandbreiten in der Servicebeschreibung im
Servicekatalog dokumentieren:

Tabelle22: Tab_Hosting_Leistungsumfang

 ---> TABLE

**[\<=]**

##### A_14509

Der Anbieter des Hosting Service MUSS die gehosteten Dienste und Client-Software
nach dem Typ der Anwendungsklasse gemäß Tabelle
Tab_zentrNetz_Anwendungsklassen physikalisch trennen. Die
Hosting-Infrastruktur MUSS exklusiv für die TI bereitgestellt werden.

 

Tabelle23: Tab_zentrNetz_Anwendungsklassen

 ---> TABLE

**[\<=]**

##### A_14539

Der Anbieter des Hosting Service MUSS VMs mit Internetanbindung
informationstechnisch getrennt von VMs mit Anbindung an die TI, in einer
gesonderten mittels DMZ gesicherten
Internet-Zone gemäß IT-Grund­schutz-Ka­ta­lo­ge des BSI betreiben [BSI
Net1.1]. **[\<=]**

##### A_14507

Der Anbieter des Hosting Service MUSS

 ---> UL

Der Hosting-Nehmer MUSS über geplante und durchgeführte Änderungen an der VM
in angemessener Vorlaufzeit sowie über Ausfälle oder Einschränkungen im
Betrieb der VM informiert werden. **[\<=]**

##### A_14508

Der Anbieter des Hosting Service DARF NICHT unbefugt auf die vom Hosting-Nehmer
gespeicherten, gesendeten und empfangenen Daten zugreifen. **[\<=]**

### 8 Anhang A – Verzeichnisse

### 8.1 Abkürzungen

 ---> TABLE

### 8.2 Glossar

Das Glossar wird als eigenständiges Dokument (vgl. [gemGlossar]) zur Verfügung
gestellt.

### 8.3 Abbildungsverzeichnis

- [Abbildung-1] - Abb_NetzTopologie_Schema, Netztopologie der TI
- [Abbildung-2] - Abb_NetzTopologie_Detail, Netzwerktopologie der TI - detailliert
- [Abbildung-3] - DSCP-Markierung (Beispiel)
- [Abbildung-4] - Abb_SichKomp_Platzierung, Platzierung von Sicherheitskomponenten in der TI
- [Abbildung-5] - Abb_IP-Config_Mgmt_Datenmodell
- [Abbildung-6] - Abb_ZentrNetz_Zerlegung, Zerlegung Zentrales Netz
- [Abbildung-7] - Abb_ZentrNetz_Anbindungsvarianten SZZP
- [Abbildung-8] - Abb_zentrNetz_SZZP-light
- [Abbildung-9] - Abb_zentrNetz_SZZP-light-plus
- [Abbildung-11] - Sicherheitsgateway_Bestandsnetze
- [Abbildung-13] - Abb_DNS_Topologie_der_TI (GS-A_3932)
- [Abbildung-14] - NTP-Topologie der TI

### 8.4 Tabellenverzeichnis

- [Tabelle-1] - Tab_Standards_IPv4, Standards IPv4
- [Tabelle-3] - Tab_Adrkonzept_Test, Adressräume IPv4 TI-Testumgebung
- [Tabelle-4] - Adressräume IPv4 TI Extern
- [Tabelle-5] - Tab_Adrkonzept_IPv6_Produktiv, Adressräume IPv6 TI Produktivumgebung
- [Tabelle-6] - Tab_Adrkonzept_IPv6_Test, Adressräume IPv6 TI-Testumgebung
- [Tabelle-8] - Tab_DK_AW, Zuordnung Dienstklassen zu Anwendungen (Auszug)
- [Tabelle-9] - Tab_DK_DSCP, Zuordnung Dienstklassen zu DSCP (Auszug)
- [Tabelle-10] - Tab_DK_AF, AF (Assured Forwarding) Drop Precedence
- [Tabelle-11] - Tab_QoS_Dienstklassen
- [Tabelle-12] - Tab_QoS_Mapping_Dienstklasse_Anwendung
- [Tabelle-13] - Tab_QoS_Mapping_Dienstklassen_Bandbreite
- [Tabelle-16] - DNS-Topologie der TI
- [Tabelle-18] - Tab_Namensdienst_DNSSD_für_WA
- [Tabelle-21] - Tab_PT_Zeitdienst_vertrauenswürdige_Zeitquellen
- [Tabelle-22] - Tab_Hosting_Leistungsumfang
- [Tabelle-23] - Tab_zentrNetz_Anwendungsklassen

### 8.5 Referenzierte Dokumente

### 8.5.1 Dokumente der gematik

Die nachfolgende Tabelle enthält die Bezeichnung der in dem vorliegenden
Dokument referenzierten Dokumente der gematik zur Telematikinfrastruktur. Der
mit der vorliegenden Version korrelierende Entwicklungsstand dieser Konzepte
und Spezifikationen wird pro Release in einer Dokumentenlandkarte definiert;
Version und Stand der referenzierten Dokumente sind daher in der nachfolgenden
Tabelle nicht aufgeführt. Deren zu diesem Dokument passende jeweils gültige
Versionsnummern sind in der aktuellen, von der gematik veröffentlichten
Dokumentenlandkarte enthalten, in der die vorliegende Version aufgeführt wird.

 ---> TABLE

### 8.5.2 Weitere Dokumente

 ---> TABLE





[Dokumentinformationen]: #dokumentinformationen
[Inhaltsverzeichnis]:    #inhaltsverzeichnis
[1]:                     #1-einordnung-des-dokuments
[1.1]:                   #11-zielsetzung
[1.2]:                   #12-zielgruppe
[1.3]:                   #13-geltungsbereich
[1.4]:                   #14-abgrenzung-des-dokuments
[1.5]:                   #15-methodik
[2]:                     #2-übergreifende-netzwerk-festlegungen
[2.1]:                   #21-netztopologie
[2.2]:                   #22-netzwerkprotokolle
[2.2.1]:                 #221-osi-schicht-1-und-2-physical/data-link
[2.2.2]:                 #222-osi-schicht-3-network
[2.2.2.1]:               #2221-ip-version-4
[2.2.2.2]:               #2222-ip-version-6
[2.2.3]:                 #223-osi-schicht-4-transport
[2.2.3.1]:               #2231-transmission-control-protocol-tcp-und-user-datagram-protocol-udp
[2.2.3.2]:               #2232-udp/tcp-portbereiche
[2.2.3.3]:               #2233-transport-layer-security-tls
[2.3]:                   #23-ip-adresskonzept-der-ti
[2.3.1]:                 #231-adressblöcke
[2.3.2]:                 #232-prozesse-zur-ip-adressvergabe
[2.3.3]:                 #233-adresskonzept-ipv4
[2.3.4]:                 #234-adresskonzept-ipv6
[2.3.5]:                 #235-adressen-sis-systeme
[2.4]:                   #24-ip-routingkonzept
[2.5]:                   #25-priorisierung-auf-netzwerkebene
[2.5.1]:                 #251-architektur
[2.5.2]:                 #252-definition-und-zuordnung-von-dienstklassen
[2.5.3]:                 #253-markierung
[2.5.3.1]:               #2531-dscp-markierung-netzkonnektor
[2.5.3.2]:               #2532-dscp-markierung-zentrales-netz-ti
[2.5.3.3]:               #2533-dscp-markierung-fremdnetze
[2.5.4]:                 #254-priorisierung-des-markierten-datenverkehrs
[2.5.4.1]:               #2541-zentrales-netz
[2.5.4.2]:               #2542-konnektor
[2.5.4.3]:               #2543-vpn-zugangsdienst
[2.6]:                   #26-sicherheitskomponenten-im-netzwerk
[2.6.1]:                 #261-typen-von-sicherheitskomponenten
[2.6.2]:                 #262-anforderungen-an-sicherheitskomponenten
[2.6.3]:                 #263-platzierung-von-sicherheitskomponenten
[2.6.4]:                 #264-prozesse-zu-regeln-für-sicherheitsgateways
[2.6.5]:                 #265-erlaubter-verkehr
[2.7]:                   #27-ip-configuration-management
[3]:                     #3-zentrales-netz-der-ti
[3.1]:                   #31-zerlegung-des-produkttyps
[3.1.1]:                 #311-sicherer-zentraler-zugangspunkt-szzp
[3.1.1.1]:               #3111-netzkomponente
[3.1.1.2]:               #3112-sicherheitsgateway
[3.1.1.3]:               #3113-anbindungen
[3.1.2]:                 #312-netzwerk
[3.1.2.1]:               #3121-backbone-zentrales-transportnetz-provider
[3.2]:                   #32-übergreifende-festlegungen
[3.3]:                   #33-funktionsmerkmale
[3.3.1]:                 #331-osi-schicht-1-und-2-physical/data-link
[3.3.1.1]:               #3311-schnittstelle-cpe-produkttyp
[3.3.1.2]:               #3312-hardwaremerkmale
[3.3.2]:                 #332-osi-schicht-3-network
[3.3.2.1]:               #3321-schnittstelle-i_ip_transport
[3.3.3]:                 #333-adressierung
[3.3.3.1]:               #3331-schnittstelle-szzp-backbone-ce-pe-und-szzp-intern
[3.3.4]:                 #334-routing
[3.3.5]:                 #335-abstimmung-mit-angeschlossenen-produkttypen
[3.4]:                   #34-verteilungssicht
[3.4.1]:                 #341-zugangsstellen
[4]:                     #4-anforderungen-an-das-sicherheitsgateway-bestandsnetze
[4.1]:                   #41-zerlegung-des-produkttyps
[5]:                     #5-namensdienst
[5.1]:                   #51-hostnamen
[5.2]:                   #52-namensräume
[5.3]:                   #53-domainnamen--und-hierarchie
[5.4]:                   #54-dns-topologie
[5.5]:                   #55-dienstlokalisierung
[5.6]:                   #56-schnittstellen-i_dns_name_resolution-und-i_dns_service_localization
[5.6.1]:                 #561-umsetzung
[5.6.2]:                 #562-nutzung
[5.7]:                   #57-anforderungen-an-den-produkttyp-namensdienst
[5.7.1]:                 #571-schnittstellen-p_dns_name_entry_announcement-und-p_dns_service_entry_announcement
[5.7.2]:                 #572-schnittstelle-p_dnssec_key_distribution
[5.7.3]:                 #573-schnittstelle-p_dns_zone_delegation
[5.7.4]:                 #574-sonstige-anforderungen
[6]:                     #6-zeitdienst
[6.1]:                   #61-ntp-topologie
[6.2]:                   #62-schnittstelle-i_ntp_time_information
[6.2.1]:                 #621-umsetzung
[6.2.2]:                 #622-nutzung
[6.3]:                   #63-anforderungen-an-den-produkttyp-zeitdienst
[7]:                     #7-hosting
[8]:                     #8-anhang-a-–-verzeichnisse
[8.1]:                   #81-abkürzungen
[8.2]:                   #82-glossar
[8.3]:                   #83-abbildungsverzeichnis
[8.4]:                   #84-tabellenverzeichnis
[8.5]:                   #85-referenzierte-dokumente
[8.5.1]:                 #851-dokumente-der-gematik
[8.5.2]:                 #852-weitere-dokumente
[Abbildung-1]:           gemSpec_Net_V1.23.0.attachments/12179904749800774483.emf
[Abbildung-2]:           gemSpec_Net_V1.23.0.attachments/12472557909669894126.emf
[Abbildung-3]:           gemSpec_Net_V1.23.0.attachments/7367032315273482765.emf
[Abbildung-4]:           gemSpec_Net_V1.23.0.attachments/9863280902305196973.emf
[Abbildung-5]:           gemSpec_Net_V1.23.0.attachments/13837439987649692382.png
[Abbildung-6]:           gemSpec_Net_V1.23.0.attachments/13328126937297458592.emf
[Abbildung-7]:           gemSpec_Net_V1.23.0.attachments/15635017545963510309.png
[Abbildung-8]:           gemSpec_Net_V1.23.0.attachments/8571924234887344646.png
[Abbildung-9]:           gemSpec_Net_V1.23.0.attachments/4200758145501157884.png
[Abbildung-11]:          gemSpec_Net_V1.23.0.attachments/16375713540687609086.png
[Abbildung-13]:          gemSpec_Net_V1.23.0.attachments/2067806594367866547.emf
[Abbildung-14]:          gemSpec_Net_V1.23.0.attachments/6115700746777642708.emf
[Tbl-001]:               #Tbl-001 (&94494945581464)
[Tabelle-1]:             #Tabelle-1 (&94494946177488)
[Tbl-003]:               #Tbl-003 (&94494946314128)
[Tabelle-3]:             #Tabelle-3 (&94494946477984)
[Tabelle-4]:             #Tabelle-4 (&94494948559648)
[Tabelle-5]:             #Tabelle-5 (&94494948657808)
[Tabelle-6]:             #Tabelle-6 (&94494948800408)
[Tbl-008]:               #Tbl-008 (&94494949008384)
[Tabelle-8]:             #Tabelle-8 (&94494949234264)
[Tabelle-9]:             #Tabelle-9 (&94494949371856)
[Tabelle-10]:            #Tabelle-10 (&94494949412648)
[Tabelle-11]:            #Tabelle-11 (&94494949739184)
[Tabelle-12]:            #Tabelle-12 (&94494949765672)
[Tabelle-13]:            #Tabelle-13 (&94494949813072)
[Tbl-015]:               #Tbl-015 (&94494951557680)
[Tbl-016]:               #Tbl-016 (&94494951681048)
[Tabelle-16]:            #Tabelle-16 (&94494952411104)
[Tbl-018]:               #Tbl-018 (&94494952963512)
[Tabelle-18]:            #Tabelle-18 (&94494952989448)
[Tbl-020]:               #Tbl-020 (&94494953086208)
[Tbl-021]:               #Tbl-021 (&94494953574120)
[Tabelle-21]:            #Tabelle-21 (&94494953639080)
[Tabelle-22]:            #Tabelle-22 (&94494953676040)
[Tabelle-23]:            #Tabelle-23 (&94494953694960)
[Tbl-025]:               #Tbl-025 (&94494953765368)
[Tbl-026]:               #Tbl-026 (&94494953871920)
[Tbl-027]:               #Tbl-027 (&94494953890728)
