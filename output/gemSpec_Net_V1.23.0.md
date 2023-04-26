
Elektronische Gesundheitskarte und Telematikinfrastruktur

### Übergreifende Spezifikation<br> Netzwerk

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

‹AFO-ID› - ‹Titel der Afo›  
 Text / Beschreibung  
 [‹=]

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

  ---> AFO 

### 2.2.2 OSI-Schicht 3 (Network)

Als produktiv eingesetztes Netzwerkprotokoll auf der OSI-Schicht 3 wird in der
TI das Internetprotokoll in der Version 4 (IPv4) eingesetzt. Als Teil der
laufenden Migration wird bei definierten Produkttypen bereits die
Unterstützung des Internetprotokolls in der Version 6 (IPv6) gefordert.
Vorgaben zum Protokoll Encapsulation Security Payload (ESP) werden in
[gemSpec_VPN_ZugD] definiert.

### 2.2.2.1 IP-Version 4

  ---> AFO 

  ---> AFO 

### 2.2.2.2 IP-Version 6

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

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

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

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

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

### 2.3.3 Adresskonzept IPv4

Die folgenden Tabellen legen die zu verwendenden IPv4-Adressbereiche für die
einzelnen TI-Umgebungen fest.

Die Anbieter von TI-Produkttypen erhalten in der Produktivumgebung
Adressbereiche aus dem IPv4-Adressraum 100.64.0.0/10 [RFC6598]. Durch die
Nutzung des in [RFC6598] definierten Adressbereiches wird ein Konflikt mit
bereits genutzten privaten Adressbereichen vermieden. Die Testumgebung ist
getrennt und nutzt den Adressraum 172.16.0.0/12.

  ---> AFO 

Erläuterung:

Aus dem Netzbereich 100.64.0.0/11 sollen nur noch IP-Adressblöcke für den
dezentralen Zugang zur TI (TI_Dezentral) zugeteilt werden. Die
IP-Adressblöcke, die schon für den Zugang SIS eingeteilt wurden, bleiben
bestehen und müssen nicht verändert werden.

Für den dezentralen SIS-Zugang muss dem Anbieter des VPN-Zugangsdienstes der
IP-Adressblock 100.104.0.0/15 zugewiesen werden. Somit ist der IP-Adressblock
TI_Dezentral_SIS für jeden VPN-Zugangsdienstanbieter identisch.

  ---> AFO 

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

  ---> AFO 

In Tabelle 4 wird informativ die Nutzung von IPv4-Adressbereichen aus
Netzbereich TI_Extern dargestellt.

 ---> TABLE

  ---> AFO 

### 2.3.4 Adresskonzept IPv6

Die folgenden Tabellen legen die zu verwendenden IPv6-Adressbereiche für die
einzelnen TI-Umgebungen fest.

Die Anbieter von TI-Produkttypen erhalten in der Produktivumgebung
Adressbereiche aus dem IPv6-Adressraum 2A10:1982:0000::/32. Die Testumgebung
nutzt den IPv6-Adressraum 2A10:1981:0000::/32 und die Referenzumgebung nutzt
den IPv6-Adressraum 2A10:1980::/32.

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

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

  ---> AFO 

  ---> AFO 

  ---> AFO 

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

  ---> AFO 

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

  ---> AFO 

Die folgende Grafik stellt anhand einer beispielhaften Kommunikationsbeziehung
zwischen Anwendungskonnektor und Fachdienst dar, an welchen Punkten die Pakete
mit den DSCP markiert werden.

![Abbildung-3][Abbildung-3]

### 2.5.3.1 DSCP-Markierung Netzkonnektor

  ---> AFO 

  ---> AFO 

### 2.5.3.2 DSCP-Markierung Zentrales Netz TI

  ---> AFO 

  ---> AFO 

  ---> AFO 

### 2.5.3.3 DSCP-Markierung Fremdnetze

An den Netzübergängen zu Fremdnetzen und Bestandsnetzen können folgende
Maßnahmen genutzt werden:

 ---> OL

  ---> AFO 

  ---> AFO 

  ---> AFO 

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

  ---> AFO 

 ---> TABLE

 ---> TABLE

 ---> TABLE

  ---> AFO 

  ---> AFO 

  ---> AFO 

### 2.5.4.1 Zentrales Netz

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

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

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

### 2.5.4.3 VPN-Zugangsdienst

Detaillierte Anforderungen zum Aufbau des VPN-Zugangsdienstes und zur Behandlung
des Datenverkehrs werden in [gemSpec_VPN_ZugD] gestellt.

  ---> AFO 

  ---> AFO 

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

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

### 2.6.3 Platzierung von Sicherheitskomponenten

An folgenden Stellen müssen Sicherheitsgateways in der TI-Plattform eingesetzt
werden:

  ---> AFO 

  ---> AFO 

Der Konnektor muss den passierenden Verkehr mit einem Paketfilter sichern.

  ---> AFO 

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

  ---> AFO 

  ---> AFO 

Hierbei ist zu beachten, dass grundsätzlich nicht von einem normalen
Schutzbedarf ausgegangen werden darf, sondern dieser immer mindestens hoch
beträgt.

### 2.6.4 Prozesse zu Regeln für Sicherheitsgateways

Für die Verwaltung und Dokumentation von Regeln für Sicherheitsgateway ist in
der TI ein übergreifender Prozess zu etablieren, der durch den Anbieter
Zentrales Netz TI implementiert und vom GBV freigegeben wird.

In den folgenden Anforderungen werden die Verantwortlichkeiten und weitere
Vorgaben zum Prozess „Verwaltung von Sicherheitsgateway-Regeln“ definiert.

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

### 2.6.5 Erlaubter Verkehr

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

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

  ---> AFO 

  ---> AFO 

Die folgende Abbildung zeigt beispielhaft eine mögliche Ausprägung des
Datenmodells.

![Abbildung-5][Abbildung-5]

  ---> AFO 

  ---> AFO 

### 3 Zentrales Netz der TI

### 3.1 Zerlegung des Produkttyps

Der Produkttyp Zentrales Netz besteht aus den folgenden Komponenten:

SZZPs (Sicherer Zentraler Zugangspunkt)

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

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

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

  ---> AFO 

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

  ---> AFO 

  ---> AFO 

Anbindung Provider (CE-PE)

Die CE-PE Anbindung stellt die Verbindung der SZZPs (CE) in den Räumlichkeiten
des angeschlossenen Produkttyps mit dem Backbone (PE) des Zentralen Netzes TI
her.

  ---> AFO 

  ---> AFO 

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

  ---> AFO 

  ---> AFO 

  ---> AFO 

SZZP-light- und SZZP-light-plus-Anschlüsse mit höherer Bandbreite dürfen
angeboten werden.

  ---> AFO 

Bei Anpassungen muss der betriebliche Change-Prozess durchlaufen werden.

  ---> AFO 

Die Funktionen des VPN-Anschlusspunktes VPN-Router und Paketfilter können in
einem Gerät realisiert sein.

  ---> AFO 

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

  ---> AFO 

Diese Anforderung kann bspw. durch einen IPsec-Kanal zwischen
dem anzuschließenden System und SZZP-light-plus mit Authentisierung über
pre-shared keys erfüllt werden.

  ---> AFO 

Bezogen auf die Verwendung eines IPsec-Kanals bedeutet dies, dass gerade nicht
der Betreiber neue (eigene) pre-shared keys im SZZP-light-plus für
anzuschließende Systeme hinterlegen darf.

### 3.1.2 Netzwerk

### 3.1.2.1 Backbone (zentrales Transportnetz Provider)

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

### 3.2 Übergreifende Festlegungen

Die Freigabe von erlaubten Kommunikationsbeziehungen erfolgt im Rahmen der
Zulassung von Diensten in der TI. Der neu aufgenommene Dienst benennt die
benötigte Kommunikation und der GBV gibt sie frei und beauftragt den Anbieter
Zentrales Netz mit der Freischaltung in den SZZP.

  ---> AFO 

  ---> AFO 

  ---> AFO 

Das zentrale Netz kann Anschlüsse mit höherer Bandbreite unterstützen.

  ---> AFO 

### 3.3 Funktionsmerkmale

  ---> AFO 

### 3.3.1 OSI-Schicht 1 und 2 (Physical/Data Link)

### 3.3.1.1 Schnittstelle CPE-Produkttyp

  ---> AFO 

### 3.3.1.2 Hardwaremerkmale

  ---> AFO 

### 3.3.2 OSI-Schicht 3 (Network)

### 3.3.2.1 Schnittstelle I_IP_Transport

  ---> AFO 

### 3.3.3 Adressierung

### 3.3.3.1 Schnittstelle SZZP-Backbone (CE-PE) und SZZP intern

Adressierung auf der SZZP-Backbone (CE-PE), möglichen SZZP-internen
Schnittstellen und Anschlüssen hinter dem PE liegen in Verantwortung des
Anbieters Zentrales Netz.

  ---> AFO 

  ---> AFO 

### 3.3.4 Routing

  ---> AFO 

  ---> AFO 

### 3.3.5 Abstimmung mit angeschlossenen Produkttypen

  ---> AFO 

  ---> AFO 

  ---> AFO 

### 3.4 Verteilungssicht

### 3.4.1 Zugangsstellen

Verteilung der Backbone-Zugangsstellen

  ---> AFO 

  ---> AFO 

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

  ---> AFO 

Die gematik empfiehlt für den Produkttyp Sicherheitsgateway Bestandsnetze, die
Verwendung von BSI-zugelassenen IT-Sicherheitsprodukten und -systemen wie in
[BSI-Schrift 7164] aufgeführt.

Für weitere Informationen zum sicheren Einsatz von Komponenten in
Sicherheitsgateways wird auf die [BSI ISI-LANA] verwiesen.

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

Bei Anpassungen muss der betriebliche Change-Prozess durchlaufen werden.

  ---> AFO 

  ---> AFO 

Die Komponenten VPN-Konzentrator und Sicherheitsgateway können in einem Gerät
realisiert sein.

  ---> AFO 

Die Festlegung für welche Zieladresse, im jeweiligen Bestandsnetz, eine
Datenvolumenerfassung einzurichten ist, erfolgt durch die gematik.

  ---> AFO 

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

  ---> AFO 

### 5.2 Namensräume

  ---> AFO 

Dieser geschlossene Namensraum wird im Folgenden Namensraum der TI genannt.

  ---> AFO 

Für die Referenzumgebung werden hinsichtlich des Namensraums keine weiteren
Vorgaben getroffen.

Innerhalb der TI werden neben dem Namensraum der TI auch der Namensraum des
Transportnetzes, der Namensraum des Internets sowie die Namensräume der
Bestandsnetze durch Clientsysteme genutzt. Diese liegen jedoch nicht in der
Verantwortung der TI.

  ---> AFO 

### 5.3 Domainnamen- und Hierarchie

  ---> AFO 

Die aktuell von der gematik festgelegten Top Level Domainnamen sind telematik.
ti-wa. und de.

  ---> AFO 

  ---> AFO 

  ---> AFO 

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

  ---> AFO 

  ---> AFO 

### 5.5 Dienstlokalisierung

Um auf die zentralen Dienste KSR und TSL-Dienst zugreifen zu können, wird die
Lokalisierung über DNS Service Discovery unterstützt.

  ---> AFO 

Weitere Anwendungen des Gesundheitswesens sowie der Gesundheitsforschung können
im Namensraum der TI die Zugangspunkte zu von ihnen bereitgestellten Diensten
über DNS-based Service Discovery gemäß [RFC6763] für Clientsysteme bekannt
machen. Für die Suche nach den Zugangspunkten der Dienste wird die Domain
„dnssd.ti-wa.“ festgelegt.

  ---> AFO 

 ---> TABLE

### 5.6 Schnittstellen I_DNS_Name_Resolution und I_DNS_Service_Localization

Beide Schnittstellen werden durch die Standard-DNS-Funktionalität technisch
umgesetzt und daher zusammen in einem Abschnitt betrachtet.

### 5.6.1 Umsetzung

Neben den grundlegenden Funktionen zur Namensauflösung wird für Nameserver im
Namensraum der TI die Unterstützung von DNSSEC und von DNS-SD gefordert.

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

Es wird empfohlen validierende DNS Resolver so zu konfigurieren, dass DNS
Responses aus folgenden Domänen (inkl. Subdomänen) validiert werden müssen:

 ---> UL

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

Der Caching Nameserver TI erlaubt rekursive Anfragen. Er leitet die Anfragen an
die autoritativen Nameserver der TI weiter.

### 5.6.2 Nutzung

  ---> AFO 

### 5.7 Anforderungen an den Produkttyp Namensdienst

  ---> AFO 

  ---> AFO 

### 5.7.1 Schnittstellen P_DNS_Name_Entry_Announcement und P_DNS_Service_Entry_Announcement

  ---> AFO 

### 5.7.2 Schnittstelle P_DNSSEC_Key_Distribution

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

### 5.7.3 Schnittstelle P_DNS_Zone_Delegation

  ---> AFO 

### 5.7.4 Sonstige Anforderungen

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

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

  ---> AFO 

  ---> AFO 

  ---> AFO 

### 6.2 Schnittstelle I_NTP_Time_Information

### 6.2.1 Umsetzung

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

Da der Konnektor nicht immer online ist oder ggf. auch nie online ist
(Offline-Szenario), gelten hier andere Anforderungen an die Genauigkeit des
NTP-Servers.

  ---> AFO 

### 6.2.2 Nutzung

  ---> AFO 

Um auf der Clientseite Falseticker gemäß [RFC5905] erkennen zu können,
müssen alle Stratum-1-NTP-Server abgefragt werden.

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

### 6.3 Anforderungen an den Produkttyp Zeitdienst

  ---> AFO 

Die Synchronisation mit der gesetzlichen Zeit erfolgt über den Zeitsignalsender
DCF77 der Physikalisch-Technischen Bundesanstalt (PTB). Die dazugehörige
Schnittstelle wird nicht durch die TI bereitgestellt und daher nicht in diesem
Dokument beschrieben.

Die Stratum-1-NTP-Server synchronisieren sich mittels jeweils eines
Standard-DCF77-Empfängers als gesetzliche Zeitquelle.

  ---> AFO 

 ---> TABLE

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

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

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

  ---> AFO 

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
[2.2.1]:                 #221-osi-schicht-1-und-2-(physical/data-link)
[2.2.2]:                 #222-osi-schicht-3-(network)
[2.2.2.1]:               #2221-ip-version-4
[2.2.2.2]:               #2222-ip-version-6
[2.2.3]:                 #223-osi-schicht-4-(transport)
[2.2.3.1]:               #2231-transmission-control-protocol-(tcp)-und-user-datagram-protocol-(udp)
[2.2.3.2]:               #2232-udp/tcp-portbereiche
[2.2.3.3]:               #2233-transport-layer-security-(tls)
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
[3.1.1]:                 #311-sicherer-zentraler-zugangspunkt-(szzp)
[3.1.1.1]:               #3111-netzkomponente
[3.1.1.2]:               #3112-sicherheitsgateway
[3.1.1.3]:               #3113-anbindungen
[3.1.2]:                 #312-netzwerk
[3.1.2.1]:               #3121-backbone-(zentrales-transportnetz-provider)
[3.2]:                   #32-übergreifende-festlegungen
[3.3]:                   #33-funktionsmerkmale
[3.3.1]:                 #331-osi-schicht-1-und-2-(physical/data-link)
[3.3.1.1]:               #3311-schnittstelle-cpe-produkttyp
[3.3.1.2]:               #3312-hardwaremerkmale
[3.3.2]:                 #332-osi-schicht-3-(network)
[3.3.2.1]:               #3321-schnittstelle-i_ip_transport
[3.3.3]:                 #333-adressierung
[3.3.3.1]:               #3331-schnittstelle-szzp-backbone-(ce-pe)-und-szzp-intern
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
[Tbl-001]:               #Tbl-001 (&94027065694616)
[Tabelle-1]:             #Tabelle-1 (&94027066290640)
[Tbl-003]:               #Tbl-003 (&94027066427280)
[Tabelle-3]:             #Tabelle-3 (&94027066591136)
[Tabelle-4]:             #Tabelle-4 (&94027068672800)
[Tabelle-5]:             #Tabelle-5 (&94027068770960)
[Tabelle-6]:             #Tabelle-6 (&94027068913560)
[Tbl-008]:               #Tbl-008 (&94027069121536)
[Tabelle-8]:             #Tabelle-8 (&94027069347416)
[Tabelle-9]:             #Tabelle-9 (&94027069485008)
[Tabelle-10]:            #Tabelle-10 (&94027069525800)
[Tabelle-11]:            #Tabelle-11 (&94027069852336)
[Tabelle-12]:            #Tabelle-12 (&94027069878824)
[Tabelle-13]:            #Tabelle-13 (&94027069926224)
[Tbl-015]:               #Tbl-015 (&94027071670832)
[Tbl-016]:               #Tbl-016 (&94027071794200)
[Tabelle-16]:            #Tabelle-16 (&94027072524256)
[Tbl-018]:               #Tbl-018 (&94027073076664)
[Tabelle-18]:            #Tabelle-18 (&94027073102600)
[Tbl-020]:               #Tbl-020 (&94027073199360)
[Tbl-021]:               #Tbl-021 (&94027073687272)
[Tabelle-21]:            #Tabelle-21 (&94027073752232)
[Tabelle-22]:            #Tabelle-22 (&94027073789192)
[Tabelle-23]:            #Tabelle-23 (&94027073808112)
[Tbl-025]:               #Tbl-025 (&94027073878520)
[Tbl-026]:               #Tbl-026 (&94027073985072)
[Tbl-027]:               #Tbl-027 (&94027074003880)
