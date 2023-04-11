
Elektronische Gesundheitskarte und Telematikinfrastruktur

### Übergreifende Spezifikation <br> Netzwerk

Klassifizierung: öffentlich  
Referenzierung: gemSpec_Net  
Revision: 566842  
Stand: 16.12.22  
Status: freigegeben  
Version: 1.23.0

### Dokumentinformationen

--> P

--> P

--> P

--> P

--> P

--> P

--> TABLE

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

--> P

--> P

--> UL

### 1.2 Zielgruppe

--> P

### 1.3 Geltungsbereich

--> P

--> P

--> P

--> P

### 1.4 Abgrenzung des Dokuments

--> P

--> P

### 1.5 Methodik

--> P

--> P

--> P

--> P

### 2 Übergreifende Netzwerk-Festlegungen

### 2.1 Netztopologie

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

### 2.2 Netzwerkprotokolle

### 2.2.1 OSI-Schicht 1 und 2 (Physical/Data Link)

--> DIV

### 2.2.2 OSI-Schicht 3 (Network)

--> P

### 2.2.2.1 IP-Version 4

--> DIV

--> DIV

### 2.2.2.2 IP-Version 6

--> DIV

--> DIV

--> DIV

--> DIV

--> P

### 2.2.3 OSI-Schicht 4 (Transport)

### 2.2.3.1 Transmission Control Protocol (TCP) und User Datagram Protocol (UDP)

--> P

### 2.2.3.2 UDP/TCP-Portbereiche

--> P

--> P

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

### 2.2.3.3 Transport Layer Security (TLS)

--> P

--> P

### 2.3 IP-Adresskonzept der TI

--> P

### 2.3.1 Adressblöcke

--> P

--> P

--> P

--> UL

--> P

--> UL

--> P

--> UL

--> P

### 2.3.2 Prozesse zur IP-Adressvergabe

--> P

--> P

--> P

--> P

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

### 2.3.3 Adresskonzept IPv4

--> P

--> P

--> DIV

--> P

--> P

--> P

--> DIV

--> P

--> P

--> P

--> P

--> P

--> DIV

--> P

--> P

--> TABLE

--> P

--> DIV

### 2.3.4 Adresskonzept IPv6

--> P

--> P

--> P

--> DIV

--> DIV

--> DIV

--> DIV

### 2.3.5 Adressen SIS-Systeme

--> P

### 2.4 IP-Routingkonzept

--> P

--> DIV

--> DIV

--> DIV

### 2.5 Priorisierung auf Netzwerkebene

--> P

--> P

### 2.5.1 Architektur

--> P

--> UL

--> P

--> DIV

### 2.5.2 Definition und Zuordnung von Dienstklassen

--> P

--> P

--> P

--> TABLE

--> P

### 2.5.3 Markierung

--> P

--> P

--> P

--> TABLE

--> P

--> P

--> P

--> P

--> TABLE

--> P

--> P

--> P

--> DIV

--> P

--> P

--> P

--> P

--> P

### 2.5.3.1 DSCP-Markierung Netzkonnektor

--> DIV

--> DIV

### 2.5.3.2 DSCP-Markierung Zentrales Netz TI

--> DIV

--> DIV

--> DIV

### 2.5.3.3 DSCP-Markierung Fremdnetze

--> P

--> OL

--> P

--> DIV

--> DIV

--> DIV

### 2.5.4 Priorisierung des markierten Datenverkehrs

--> P

--> P

--> P

--> DIV

--> P

--> P

--> TABLE

--> P

--> P

--> TABLE

--> P

--> P

--> TABLE

--> P

--> DIV

--> DIV

--> DIV

### 2.5.4.1 Zentrales Netz

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

### 2.5.4.2 Konnektor

--> P

--> P

--> P

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

### 2.5.4.3 VPN-Zugangsdienst

--> P

--> DIV

--> DIV

### 2.6 Sicherheitskomponenten im Netzwerk

--> P

### 2.6.1 Typen von Sicherheitskomponenten

--> P

--> P

--> P

--> P

### 2.6.2 Anforderungen an Sicherheitskomponenten

--> P

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

### 2.6.3 Platzierung von Sicherheitskomponenten

--> P

--> DIV

--> DIV

--> P

--> DIV

--> P

--> P

--> P

--> P

--> DIV

--> DIV

--> P

### 2.6.4 Prozesse zu Regeln für Sicherheitsgateways

--> P

--> P

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

### 2.6.5 Erlaubter Verkehr

--> DIV

--> DIV

--> DIV

--> DIV

### 2.7 IP-Configuration-Management

--> P

--> P

--> P

--> P

--> DIV

--> DIV

--> P

--> P

--> P

--> P

--> P

--> DIV

--> DIV

--> P

### 3 Zentrales Netz der TI

### 3.1 Zerlegung des Produkttyps

--> P

--> P

--> UL

--> P

--> UL

--> P

--> UL

--> P

--> P

--> P

--> P

### 3.1.1 Sicherer Zentraler Zugangspunkt (SZZP)

--> P

--> P

--> DIV

--> DIV

--> DIV

--> DIV

### 3.1.1.1 Netzkomponente

--> P

--> P

--> OL

### 3.1.1.2 Sicherheitsgateway

--> P

--> P

--> DIV

### 3.1.1.3 Anbindungen

--> P

--> P

--> P

--> P

--> P

--> UL

--> P

--> P

--> P

--> DIV

--> DIV

--> P

--> P

--> DIV

--> DIV

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> DIV

--> DIV

--> DIV

--> P

--> DIV

--> P

--> P

--> DIV

--> P

--> DIV

--> P

--> P

--> DIV

--> P

--> DIV

--> P

--> P

### 3.1.2 Netzwerk

### 3.1.2.1 Backbone (zentrales Transportnetz Provider)

--> DIV

--> P

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

### 3.2 Übergreifende Festlegungen

--> P

--> DIV

--> DIV

--> DIV

--> P

--> DIV

### 3.3 Funktionsmerkmale

--> DIV

### 3.3.1 OSI-Schicht 1 und 2 (Physical/Data Link)

### 3.3.1.1 Schnittstelle CPE-Produkttyp

--> DIV

### 3.3.1.2 Hardwaremerkmale

--> DIV

### 3.3.2 OSI-Schicht 3 (Network)

### 3.3.2.1 Schnittstelle I_IP_Transport

--> DIV

### 3.3.3 Adressierung

### 3.3.3.1 Schnittstelle SZZP-Backbone (CE-PE) und SZZP intern

--> P

--> DIV

--> DIV

### 3.3.4 Routing

--> DIV

--> P

--> DIV

### 3.3.5 Abstimmung mit angeschlossenen Produkttypen

--> DIV

--> DIV

--> DIV

### 3.4 Verteilungssicht

### 3.4.1 Zugangsstellen

--> P

--> DIV

--> DIV

### 4 Anforderungen an das Sicherheitsgateway Bestandsnetze

### 4.1 Zerlegung des Produkttyps

--> P

--> UL

--> P

--> P

--> P

--> P

--> DIV

--> P

--> P

--> P

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> P

--> DIV

--> DIV

--> P

--> P

--> DIV

--> P

--> P

--> DIV

### 5 Namensdienst

--> P

--> P

### 5.1 Hostnamen

--> DIV

### 5.2 Namensräume

--> DIV

--> P

--> DIV

--> P

--> P

--> DIV

### 5.3 Domainnamen- und Hierarchie

--> DIV

--> P

--> DIV

--> DIV

--> DIV

--> P

### 5.4 DNS-Topologie

--> P

--> P

--> P

--> P

--> TABLE

--> P

--> P

--> P

--> P

--> P

--> DIV

--> DIV

### 5.5 Dienstlokalisierung

--> P

--> DIV

--> P

--> DIV

--> P

--> P

--> TABLE

--> P

### 5.6 Schnittstellen I_DNS_Name_Resolution und I_DNS_Service_Localization

--> P

### 5.6.1 Umsetzung

--> P

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> P

--> UL

--> P

--> DIV

--> DIV

--> DIV

--> DIV

--> P

--> P

### 5.6.2 Nutzung

--> DIV

### 5.7 Anforderungen an den Produkttyp Namensdienst

--> DIV

--> DIV

### 5.7.1 Schnittstellen P_DNS_Name_Entry_Announcement und P_DNS_Service_Entry_Announcement

--> DIV

### 5.7.2 Schnittstelle P_DNSSEC_Key_Distribution

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

### 5.7.3 Schnittstelle P_DNS_Zone_Delegation

--> DIV

### 5.7.4 Sonstige Anforderungen

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

### 6 Zeitdienst

--> P

--> P

### 6.1 NTP-Topologie

--> P

--> P

--> P

--> P

--> DIV

--> DIV

--> DIV

### 6.2 Schnittstelle I_NTP_Time_Information

### 6.2.1 Umsetzung

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> P

--> DIV

### 6.2.2 Nutzung

--> DIV

--> P

--> DIV

--> DIV

--> DIV

--> DIV

### 6.3 Anforderungen an den Produkttyp Zeitdienst

--> DIV

--> P

--> P

--> DIV

--> P

--> P

--> TABLE

--> P

--> DIV

--> DIV

--> DIV

--> DIV

### 7 Hosting

--> P

--> P

--> P

--> P

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> P

### 8 Anhang A – Verzeichnisse

### 8.1 Abkürzungen

--> TABLE

### 8.2 Glossar

--> P

### 8.3 Abbildungsverzeichnis

--> DIV

--> DIV

### 8.4 Tabellenverzeichnis

--> DIV

--> DIV

### 8.5 Referenzierte Dokumente

### 8.5.1 Dokumente der gematik

--> P

--> P

--> TABLE

--> P

### 8.5.2 Weitere Dokumente

--> TABLE

--> P

--> P

--> P

[Dokumentinformationen]: #dokumentinformationen
[Inhaltsverzeichnis]: #inhaltsverzeichnis
[1]: #1-einordnung-des-dokuments
[1.1]: #11-zielsetzung
[1.2]: #12-zielgruppe
[1.3]: #13-geltungsbereich
[1.4]: #14-abgrenzung-des-dokuments
[1.5]: #15-methodik
[2]: #2-Übergreifende-netzwerkfestlegungen
[2.1]: #21-netztopologie
[2.2]: #22-netzwerkprotokolle
[2.2.1]: #221-osischicht-1-und-2-physicaldata-link
[2.2.2]: #222-osischicht-3-network
[2.2.2.1]: #2221-ipversion-4
[2.2.2.2]: #2222-ipversion-6
[2.2.3]: #223-osischicht-4-transport
[2.2.3.1]: #2231-transmission-control-protocol-tcp-und-user-datagram-protocol-udp
[2.2.3.2]: #2232-udptcpportbereiche
[2.2.3.3]: #2233-transport-layer-security-tls
[2.3]: #23-ipadresskonzept-der-ti
[2.3.1]: #231-adressblöcke
[2.3.2]: #232-prozesse-zur-ipadressvergabe
[2.3.3]: #233-adresskonzept-ipv4
[2.3.4]: #234-adresskonzept-ipv6
[2.3.5]: #235-adressen-sissysteme
[2.4]: #24-iproutingkonzept
[2.5]: #25-priorisierung-auf-netzwerkebene
[2.5.1]: #251-architektur
[2.5.2]: #252-definition-und-zuordnung-von-dienstklassen
[2.5.3]: #253-markierung
[2.5.3.1]: #2531-dscpmarkierung-netzkonnektor
[2.5.3.2]: #2532-dscpmarkierung-zentrales-netz-ti
[2.5.3.3]: #2533-dscpmarkierung-fremdnetze
[2.5.4]: #254-priorisierung-des-markierten-datenverkehrs
[2.5.4.1]: #2541-zentrales-netz
[2.5.4.2]: #2542-konnektor
[2.5.4.3]: #2543-vpnzugangsdienst
[2.6]: #26-sicherheitskomponenten-im-netzwerk
[2.6.1]: #261-typen-von-sicherheitskomponenten
[2.6.2]: #262-anforderungen-an-sicherheitskomponenten
[2.6.3]: #263-platzierung-von-sicherheitskomponenten
[2.6.4]: #264-prozesse-zu-regeln-für-sicherheitsgateways
[2.6.5]: #265-erlaubter-verkehr
[2.7]: #27-ipconfigurationmanagement
[3]: #3-zentrales-netz-der-ti
[3.1]: #31-zerlegung-des-produkttyps
[3.1.1]: #311-sicherer-zentraler-zugangspunkt-szzp
[3.1.1.1]: #3111-netzkomponente
[3.1.1.2]: #3112-sicherheitsgateway
[3.1.1.3]: #3113-anbindungen
[3.1.2]: #312-netzwerk
[3.1.2.1]: #3121-backbone-zentrales-transportnetz-provider
[3.2]: #32-Übergreifende-festlegungen
[3.3]: #33-funktionsmerkmale
[3.3.1]: #331-osischicht-1-und-2-physicaldata-link
[3.3.1.1]: #3311-schnittstelle-cpeprodukttyp
[3.3.1.2]: #3312-hardwaremerkmale
[3.3.2]: #332-osischicht-3-network
[3.3.2.1]: #3321-schnittstelle-iiptransport
[3.3.3]: #333-adressierung
[3.3.3.1]: #3331-schnittstelle-szzpbackbone-cepe-und-szzp-intern
[3.3.4]: #334-routing
[3.3.5]: #335-abstimmung-mit-angeschlossenen-produkttypen
[3.4]: #34-verteilungssicht
[3.4.1]: #341-zugangsstellen
[4]: #4-anforderungen-an-das-sicherheitsgateway-bestandsnetze
[4.1]: #41-zerlegung-des-produkttyps
[5]: #5-namensdienst
[5.1]: #51-hostnamen
[5.2]: #52-namensräume
[5.3]: #53-domainnamen-und-hierarchie
[5.4]: #54-dnstopologie
[5.5]: #55-dienstlokalisierung
[5.6]: #56-schnittstellen-idnsnameresolution-und-idnsservicelocalization
[5.6.1]: #561-umsetzung
[5.6.2]: #562-nutzung
[5.7]: #57-anforderungen-an-den-produkttyp-namensdienst
[5.7.1]: #571-schnittstellen-pdnsnameentryannouncement-und-pdnsserviceentryannouncement
[5.7.2]: #572-schnittstelle-pdnsseckeydistribution
[5.7.3]: #573-schnittstelle-pdnszonedelegation
[5.7.4]: #574-sonstige-anforderungen
[6]: #6-zeitdienst
[6.1]: #61-ntptopologie
[6.2]: #62-schnittstelle-intptimeinformation
[6.2.1]: #621-umsetzung
[6.2.2]: #622-nutzung
[6.3]: #63-anforderungen-an-den-produkttyp-zeitdienst
[7]: #7-hosting
[8]: #8-anhang-a-–-verzeichnisse
[8.1]: #81-abkürzungen
[8.2]: #82-glossar
[8.3]: #83-abbildungsverzeichnis
[8.4]: #84-tabellenverzeichnis
[8.5]: #85-referenzierte-dokumente
[8.5.1]: #851-dokumente-der-gematik
[8.5.2]: #852-weitere-dokumente

