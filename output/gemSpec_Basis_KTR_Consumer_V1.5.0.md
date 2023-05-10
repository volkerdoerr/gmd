
Elektronische Gesundheitskarte und Telematikinfrastruktur

### Spezifikation<br>Basis- und KTR-Consumer

- Klassifizierung: öffentlich
- Referenzierung: gemSpec_Basis_KTR_Consumer
- Revision: 591017
- Stand: 13.05.2022
- Status: freigegeben
- Version: 1.5.0

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
1.0.0

</td><td>
15.05.19

</td><td>
initiale Erstellung des Dokuments

</td><td>
gematik

</td></tr><tr><td>
1.1.0

</td><td>
28.06.19

</td><td>
Einarbeitung P19.1

</td><td>
gematik

</td></tr><tr><td>
1.2.0

</td><td>
30.06.20

</td><td>
Einarbeitung P22.1

</td><td>
gematik

</td></tr><tr><td>
1.3.0

</td><td>
10.09.20

</td><td>
Einarbeitung P22.3

</td><td>
gematik

</td></tr><tr><td>
1.3.1

</td><td>
19.02.21

</td><td>
Clientmodul KOM-LE ist für den KTR-Consumer nicht verpflichtend

</td><td>
gematik

</td></tr><tr><td>
1.3.2

</td><td>
06.08.21

</td><td>
Einarbeitung Consumer_Maintenance_21.3

</td><td>
gematik

</td></tr><tr><td>
1.4.0

</td><td>
17.02.22

</td><td>
Einarbeitung Consumer_Maintenance_21.4 und CI_Maintenance_21.2,

</td><td>
gematik

</td></tr><tr><td>
1.5.0

</td><td>
13.05.22

</td><td>
6.5.1

</td><td>
Einarbeitung Consumer_Maintenance_22.1

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
  - [1.4] Abgrenzungen
  - [1.5] Methodik
- [2] Systemüberblick
- [3] Systemkontext
- [4] Zerlegung der Produkttypen
  - [4.1] Basisfunktionen
  - [4.2] LDAP-Proxy
  - [4.3] Clientmodul KOM-LE
- [5] Übergreifende Festlegungen
  - [5.1] Anschluss an die TI
    - [5.1.1] Anbindung per LAN/WAN
      - [5.1.1.1] Funktionsmerkmalweite Aspekte
        - [5.1.1.1.1] Netzwerksegmentierung
      - [5.1.1.2] Durch Ereignisse ausgelöste Reaktionen
    - [5.1.2] Zeitdienst
    - [5.1.3] Namensdienst und Dienstlokalisierung
      - [5.1.3.1] Funktionsmerkmalweite Aspekte
      - [5.1.3.2] Interne TUCs, auch durch Fachmodule nutzbar
        - [5.1.3.2.1] TUC_CON_362 „Liste der Dienste abrufen“
      - [5.1.3.3] Operationen an der Außenschnittstelle
      - [5.1.3.4] Betriebsaspekte
  - [5.2] Sicherheit
  - [5.3] Identitäten
  - [5.4] Schnittstellen
- [6] Funktionsmerkmale
  - [6.1] Verschlüsselungsdienst
    - [6.1.1] Durch Module nutzbare TUCs
    - [6.1.2] Operationen an der Clientschnittstelle
      - [6.1.2.1] EncryptDocument
      - [6.1.2.2] DecryptDocument
  - [6.2] Signaturdienst
    - [6.2.1] Durch Module nutzbare TUCs
    - [6.2.2] Operationen an der Clientschnittstelle
      - [6.2.2.1] SignDocument
      - [6.2.2.2] VerifyDocument
      - [6.2.2.3] ExternalAuthenticate
  - [6.3] Zertifikatsdienst
    - [6.3.1] Durch Module nutzbare TUCs
    - [6.3.2] Operationen an der Clientschnittstelle
      - [6.3.2.1] VerifyCertificate
  - [6.4] LDAP-Proxy
    - [6.4.1] Durch Module nutzbare TUCs
    - [6.4.2] Unterstützte LDAPv3-Operationen an der Clientschnittstelle
  - [6.5] Clientmodul KOM-LE
    - [6.5.1] Allgemeine Anforderungen
    - [6.5.2] Senden von Nachrichten
    - [6.5.3] Empfangen von Nachrichten
  - [6.6] Realisierung der Leistungen der TI-Plattform
    - [6.6.1] Transportschnittstelle für Kartenkommandos
    - [6.6.2] Schnittstelle für PIN-Operationen und Anbindung der Karten der TI
- [7] Anhang A - Verzeichnisse
  - [7.1] Abkürzungen
  - [7.2] Glossar
  - [7.3] Abbildungsverzeichnis
  - [7.4] Tabellenverzeichnis
  - [7.5] Referenzierte Dokumente
    - [7.5.1] Dokumente der gematik
    - [7.5.2] Weitere Dokumente
- [8] Anhang B – Übersicht über die verwendeten Versionen
- [9] Anhang C – Übersicht der genutzten Systemprozesse

### 1 Einordnung des Dokumentes

### 1.1 Zielsetzung

Die vorliegende Spezifikation definiert die Anforderungen an Herstellung, Test
und Betrieb der beiden Produkttypen Basis-Consumer und KTR-Consumer.

Der Basis-Consumer und der KTR-Consumer sind Produkttypen der TI-Plattform, die
in der Rolle eines Consumers mit der Telematikinfrastruktur (TI) interagieren
und dabei sowohl Anteile der TI-Plattform als auch Anteile des sicheren
Übermittlungsverfahrens KOM-LE (beim Basis-Consumer) enthalten. Der
KTR-Consumer enthält darüber hinaus auch Fachmodule, die einem Nutzerkreis
„Kostenträger“ die Teilnahme an den dafür vorgesehenen Fachanwendungen
der Telematikinfrastruktur ermöglichen.

### 1.2 Zielgruppe

Das Dokument ist maßgeblich für Anbieter und Hersteller des Produkttyps Basis-
und KTR-Consumer sowie für Anbieter und Hersteller von Produkten, die die
Schnittstellen des Produkttyps Basis- und KTR-Consumer nutzen.

### 1.3 Geltungsbereich

Dieses Dokument enthält normative Festlegungen zur Telematikinfrastruktur des
deutschen Gesundheitswesens. Der Gültigkeitszeitraum der vorliegenden Version
und deren Anwendung in Zulassungs- oder Abnahmeverfahren wird durch die gematik
GmbH in gesonderten Dokumenten (z.B. Dokumentenlandkarte, Produkttypsteckbrief,
Leistungsbeschreibung) fest­gelegt und bekannt gegeben.

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

### 1.4 Abgrenzungen

Spezifiziert werden in dem Dokument die von den Produkttypen Basis- und
KTR-Consumer  bereitgestellten (angebotenen) Schnittstellen. Benutzte
Schnittstellen werden hingegen in der Spezifikation desjenigen Produkttypen
beschrieben, der diese Schnittstelle bereitstellt. Auf die entsprechenden
Dokumente wird referenziert (siehe auch Anhang A5).

Die vollständige Anforderungslage für die Produkttypen ergibt sich aus
weiteren Konzept- und Spezifikationsdokumenten, diese sind in den
Produkttypsteckbriefen des Produkttyps Basis- bzw. KTR-Consumer verzeichnet.

### 1.5 Methodik

Anforderungen als Ausdruck normativer Festlegungen werden durch eine eindeutige
ID sowie die dem RFC 2119 [RFC2119] entsprechenden, in Großbuchstaben
geschriebenen deutschen Schlüsselworte MUSS, DARF NICHT, SOLL, SOLL NICHT,
KANN gekennzeichnet.

Sie werden im Dokument wie folgt dargestellt:\<AFO-ID\> - \<Titel der Afo\>Text
/ Beschreibung [\<=]

Dabei umfasst die Anforderung sämtliche zwischen der ID und der Textmarke
angeführten Inhalte.

### 2 Systemüberblick

Die Produkttypen Basis- und KTR-Consumer sind beides Realisierungen des
konzeptionellen Konstrukts „RZ-Consumer“ aus [gemKPT_Arch_TIP]. D.h., sie
agieren als Consumer in der Telematikinfrastruktur (TI), nutzen dabei zentrale
Dienste, die Dienste des sicheren Übermittlungsverfahrens und ggf.
fachanwendungsspezifische Dienste und werden in einem Rechenzentrum
entsprechend den Vorgaben der TI betrieben. Beide Produkttypen bieten für
externe Clients eine Menge von Basisfunktionen (z.B. kryptographische
Operationen), ermöglichen den Zugriff auf weitere Anwendungen des
Gesundheitswesens und die Nutzung des sicheren Übermittlungsverfahrens KOM-LE
(beim Basis-Consumer).

Der Basis-Consumer ermöglicht es den Gesellschaftern der gematik sowie den
durch sie vertretenen Organisationen, als Nutzer an der TI teilzunehmen. Der
Zugriff auf Fachanwendungen der TI ist dieser Nutzergruppe nicht gestattet. Der
Produkttyp enthält demnach zwar keine Fachmodule, aber ein Clientmodul KOM-LE
zur Nutzung des sicheren Übermittlungsverfahrens. Auf technischer Ebene wird
die jeweilige Nutzergruppe durch die kryptographische Identität der SMC-B Org
oder SMC-B KTR (jeweils auf Basis oid_kostenträger) identifiziert, die in
einem HSM oder auf einer Karte gespeichert wird.

Der KTR-Consumer ermöglicht es Kostenträgern, als Nutzer an der TI
teilzunehmen. Durch enthaltene Fachmodule können dabei Fachanwendungen, bei
der die Kostenträger als berechtigte Nutzer festgelegt sind (mit Ausnahme von
VSDM), und die weiteren Anwendungen des Gesundheitswesens genutzt werden. Auf
technischer Ebene wird die Nutzergruppe durch kryptographische Identitäten der
SMC-B KTR (auf Basis oid_kostenträger und oid_epa_ktr) identifiziert, die in
einem HSM gespeichert werden.

### 3 Systemkontext

Nachfolgend wird angelehnt an den Systemüberblick aus [gemKPT_Arch_TIP] die
Einbettung der Produkttypen Basis-Consumer und KTR-Consumer in das System der
TI dargestellt. Die Darstellung ist reduziert auf die Produkttypen der TI sowie
Clients und Anwendungen außerhalb der TI, mit denen potentiell eine
Interaktion stattfindet. Die Festlegungen des vorliegenden Dokuments beziehen
sich auf die Produkttypen Basis-Consumer und KTR-Consumer als Ganzes und das
logische Konstrukt des Consumer-Adapters aus [gemKPT_Arch_TIP], das den Umfang
der Basisfunktionen der Produkttypen festlegt.

![Abbildung-1][Abbildung-1]

### 4 Zerlegung der Produkttypen

Der ProdukttypBasis-Consumer teilt sich in die folgenden Bestandteile auf:

 ---> UL

Der ProdukttypKTR-Consumer teilt sich in die folgenden Bestandteile auf:

 ---> UL

Die Festlegungen der vorliegenden Dokuments beziehen sich auf die Produkttypen
Basis-Consumer und KTR-Consumer als Ganzes sowie deren oben aufgeführten
Bestandteile, mit Ausnahme des Fachmoduls ePA und des Clientmoduls KOM-LE,
welche in [gemSpec_FM_ePA_KTR_Consumer], bzw. [gemSpec_CM_KOMLE], beschrieben
sind. Das logische Konstrukt des Consumer-Adapters aus [gemKPT_Arch_TIP], wird
durch die Basisfunktionen und den LDAP-Proxy in dem für die Produkttypen
benötigten Umfang umgesetzt.

Einige Anforderungen des vorliegenden Dokuments, sowie der Spezifikationen des
Clientmoduls und des Fachmoduls, sind nur in Abhängigkeit einer konkreten
Produktausprägung verpflichtend umzusetzen. Die Kennzeichnung dieser
Anforderungen ist Bestandteil der jeweiligen Produtkttypsteckbriefe des Basis-
oder KTR-Consumers.

### 4.1 Basisfunktionen

Die Basisfunktionen enthalten:

 ---> UL

### 4.2 LDAP-Proxy

Der Basis- und KTR-Consumer ermöglicht es Clientsystemen und Clientmodulen
durch Nutzung des LDAP-Proxies Daten aus dem Verzeichnisdienst der TI-Plattform
(VZD) abzufragen. Die Kommunikation erfolgt über das LDAPv3-Protokoll.

### 4.3 Clientmodul KOM-LE

Der Basis-Consumer enthält ein Clientmodul KOM-LE, um das sichere
Übermittlungsverfahren KOM-LE nutzen zu können. Es werden die
Anwendungsfälle „Senden und Empfangen von Nachrichten“ unterstützt. Die
Spezifikation [gemSpec_CM_KOMLE] gilt in großen Teilen auch für den
Basis-Consumer. Es gibt aber verschiedene Bereiche, in denen eine Anpassung
für den Basis-Consumer erforderlich ist. Für diese Bereiche werden neue
Anforderungen aufgenommen, die statt der bestehenden Anforderungen aus
[gemSpec_CM_KOMLE] zu verwenden sind. Die Bereiche sind:

 ---> UL

### 5 Übergreifende Festlegungen

### 5.1 Anschluss an die TI

### 5.1.1 Anbindung per LAN/WAN

Unter Anbindung per LAN/WAN werden die Mechanismen beschrieben, mit denen der
Basis- und KTR-Consumer auf der einen Seite in das lokale Netz der
Einsatzumgebung und auf der anderen Seite in die zentrale TI sowie WANDA
Basic und die WANDA Smart angebunden wird. Diese wesentlichen Aspekte
betreffen Routing und Firewall.

### 5.1.1.1 Funktionsmerkmalweite Aspekte

**A_17396 - Verhalten als IPv4-Router**

Der Basis- und KTR-Consumer MUSS sich nach den in [RFC1812#1.1.3] definierten
Rahmenbedingungen als IP-Version-4-(IPv4)-Router verhalten. Die in [RFC2644]
geforderten Aktualisierungen zum [RFC1812] MÜSSEN umgesetzt werden. **[\<=]**

**A_17397 - IP-Pakete mit Source Route Option**

Der Basis- und KTR-Consumer DARF NICHT IP-Pakete mit gesetzter Source Route
Option gemäß [RFC791] erzeugen oder weiterleiten. **[\<=]**

**A_17400-01 - NAT-Umsetzung**

DerBasis- und KTR-Consumer MUSS für die Kommunikation mit Adressbereichen der
TI sowie WANDA Basic und WANDA Smart eine Network Address Translation (NAT)
gemäß [RFC3022#2.2, 3, 4.1-4.3] vornehmen.Für die Umsetzung der Private
Local Address aus den Adressbereichen der Einsatzumgebung MUSS die verwendete
IP-Adresse aus dem vom Anbieter Zentrale Plattform Dienste (AZPD)
bereitgestellten Adress-Pool entnommen werden und als Global Address genutzt
werden. **[\<=]**

**A_17405 - Nur IPv4. IPv6 nur hardwareseitig vorbereitet**

Der Basis- und KTR-Consumer MUSS die IP Version 4 (IPv4) für alle seine
IP-Schnittstellen unterstützen.Die Hardware des Basis- und KTR-Consumer MUSS
für den Einsatz von IPv4 und IPv6 im Dual-Stack-Mode geeignet sein.Bis zu
einer Migration von IPv4 auf IPv6 MUSS der Basis- und KTR-Consumer sämtliche
empfangenen IP-Pakete der Version 6 (IPv6) verwerfen. **[\<=]**

Die Anbindung des Basis- und KTR-Consumers an die zentrale TI erfolgt über
einen Sicheren Zentralen Zugangspunkt (SZZP), siehe [gemSpec_Net#3.1.1]. Dieser
Produkttyp unterstützt kein dynamisches Routing.

**A_17406 - Kein dynamisches Routing**

Basis- und KTR-Consumer DÜRFEN NICHT Dynamische Routing-Protokolle einsetzen.
**[\<=]**

### 5.1.1.1.1 Netzwerksegmentierung

In Anlehnung an die in der [gemSpec_Net#2.3.3] definierten Netzwerksegmente
werden in der Basis- und KTR-Consumerspezifikation die folgenden Bezeichner
verwendet:

<table><tr><th>
ReferenzID im  
Basis- und KTR-Consumer

</th><th>
Adressbereich für die TI-Produktivumgebung

</th><th>
Adressbereich für die TI-Testumgebung

</th><th>
Adressbereich für die TI-Referenzumgebung

</th></tr><tr><td>
NET_TI_  
ZENTRAL

</td><td>
TI_Zentral  
- Zentrale Dienste

</td><td>
TI_Test_Zentral  
- Zentrale Dienste

</td><td>
Ist durch den Testbetriebsverantwortlichen zu definieren.

</td></tr><tr><td>
NET_TI_  
GESICHERTE_  
FD

</td><td>
TI_Fachdienste  
- Gesicherte Fachdienste

</td><td>
TI_Test_Fachdienste  
- Gesicherte Fachdienste

</td><td>
Ist durch den Testbetriebsverantwortlichen zu definieren.

</td></tr><tr><td>
NET_TI_OFFENE_FD

</td><td>
TI_Fachdienste  
- Offene Fachdienste

</td><td>
TI_Test_Fachdienste  
- Offene Fachdienste

</td><td>
Ist durch den Testbetriebsverantwortlichen zu definieren.

</td></tr><tr><td>
NET_WANDA_Smart

</td><td>
WANDA Smart

</td><td>
WANDA Smart

</td><td>
WANDA Smart

</td></tr><tr><td>
NET_CONSUMER

</td><td colspan="3">
Liste der Netzwerke die in der Einsatzumgebung über den Basis- und KTR-Consumer
erreichbar sind. Ein Eintrag der Liste enthält die Netzwerkadresse und den
Netzwerkpräfix.

</td></tr><tr><td>
NET_WANDA_Basic

</td><td>
WANDA Basic

</td><td>
WANDA Basic

</td><td>
WANDA Basic

</td></tr></table>

**A_17411 - Kommunikation mit NET_TI_Offene_FD**

Der Basis- und KTR-Consumer MUSS sicherstellen, dass IP-Pakete mit dem Ziel
NET_TI_Offene_FD und NET_WANDA_Smart weitergeleitet werden. **[\<=]**

**A_17514 - Kommunikation mit NET_TI_Gesicherte_FD**

Der KTR-Consumer MUSS sicherstellen, dass IP-Pakete mit dem Ziel
NET_TI_Gesicherte_FD nur durch das im KTR-Consumer vorhandene jeweilige
Fachmodul in Richtung TI mit dem Ziel NET_TI_Gesicherte_FD weitergeleitet
werden. **[\<=]**

**A_17415 - Kommunikation mit NET_TI_ZENTRAL**

Der Basis- und KTR-Consumer MUSS sicherstellen, dass IP-Pakete in Richtung
NET_TI_ZENTRAL mit dem Ziel TI-Namens- und Zeitdienst nur vom Basis- und
KTR-Consumer weitergeleitet werden. **[\<=]**

**A_21998 - Kommunikation mit NET_WANDA_Basic**

Der Basis- und KTR-Consumer MUSS sicherstellen, dass IP-Pakete mit dem Ziel
NET_WANDA_Basic weitergeleitet werden. **[\<=]**

**A_17417 - Einschränkung von nicht genehmigten Traffic**

Der Basis- und KTR-Consumer MUSS nicht genehmigten Traffic blockieren. **[\<=]**

**A_17418 - Drop statt Reject**

Der Basis- und KTR-Consumer MUSS alle abgelehnten IP-Pakete verwerfen (DROP),
ohne ein ICMP-Destination-Unreachable (Type 3) zu schicken. **[\<=]**

**A_17419 - Abwehr von IP-Spoofing, DoS/DDoS-Angriffe und Martian Packets**

Der Basis- und KTR-Consumer MUSS geeignete technische Funktionen zur Abwehr von
IP-Spoofing und DoS/DDoS-Angriffen implementieren.Der Basis- und KTR-Consumer
MUSS Martian Packets (Absender- oder Empfängeradressen aus den von der IETF
als Special-Purpose definierten Netzbereichen), mindestens jedoch aus folgenden
Netzbereichen 0.0.0.0/8, 127.0.0.0/8, 169.254.0.0/16, 192.0.0.0/24,
192.0.2.0/24, 198.18.0.0/15, 198.51.100.0/24, 203.0.113.0/24, 224.0.0.0/4,
240.0.0.0/4, verwerfen. Die in [RFC1918] und [RFC 6598] definierten
Netzbereiche sind hiervon ausgenommen. **[\<=]**

**A_17420 - Eingeschränkte Nutzung von „Ping“**

Der Basis- und KTR-Consumer MUSS TCP-Port-7(Echo)-Pakete verwerfen.Der Basis-
und KTR-Consumer MUSS ICMP-Echo-Request (Typ 8) und ICMP-Echo-Response (Typ 0)
ausschließlich für, per Anforderung genehmigten, Traffic weiterleiten.
**[\<=]**

**A_17421 - Einschränkungen der IP-Protokolle**

Der Basis- und KTR-Consumer MUSS alle IP-Protokolle außer 1 (ICMP), 17 (UDP)
und 6 (TCP) für alle ein- oder ausgehenden Pakete an allen seinen Adaptern
verwerfen. **[\<=]**

**A_17423 - Firewall Restart**

Der Basis- und KTR-Consumer MUSS gewährleisten, dass unmittelbar nach einer
Änderung der Parameter eines Adapters (LAN-Adapter, WAN-Adapter) die Firewall
des Basis- und KTR-Consumer neu erstellt und geladen wird. **[\<=]**

Umsetzungshinweis für den Hersteller: Es können zwei getrennten
Firewall-Regelsets für den LAN- bzw. für den WAN-Adapter verwendet werden.

**A_17424 - Firewall-Protokollierung**

Der Basis- und KTR-Consumer MUSS bei Konfigurationsänderungen der Firewall
einen Protokolleintrag mit der Schwere „Warning“ und dem Typ
„Operations“ sowie mindestens folgenden Informationen generieren:

 ---> UL

Der Basis- und KTR-Consumer MUSS für alle vom Basis- und KTR-Consumer
ausgehenden, nicht zugelassenen Kommunikationsversuche einen Protokolleintrag
mit der Schwere „Warning“ und dem Typ „Security“ sowie mindestens
folgenden Informationen generieren:

 ---> UL

Der Basis- und KTR-Consumer MUSS für alle verworfenen IP-Spoofing- und
Martian-Packets einen Protokolleintrag mit der Schwere „Warning“ und dem
Typ „Security“ sowie mindestens folgenden Informationen generieren:

 ---> UL

Der Basis- und KTR-Consumer MUSS für alle weiteren von der Firewall verworfenen
IP-Pakete einen Protokolleintrag mit der Schwere „Info“ und dem Typ
„Security“ sowie mindestens folgenden Informationen generieren, wobei Layer
3 Broadcasts von der Protokollierung ausgenommen werden können:

 ---> UL

**[\<=]**

### 5.1.1.2 Durch Ereignisse ausgelöste Reaktionen

**A_17425 - Reagiere auf LAN_IP_Changed**

Wurde die IP Adresse des LAN Interfaces geändert oder hat, bei aktiven DHCP
Client, ein erfolgreiches DHCP_RENEW stattgefunden MUSS der Basis- und
KTR-Consumer den LAN-Adapter initialisieren. **[\<=]**

**A_17426 - Reagiere auf WAN_IP_Changed**

Wurde die IP Adresse des WAN Interfaces geändert oder hat, bei aktiven DHCP
Client, ein erfolgreiches DHCP_RENEW stattgefunden MUSS der Basis- und
KTR-Consumer den WAN-Adapter initialisieren. **[\<=]**

**A_17430 - Netzwerk-Routen einrichten**

Der Basis- und KTR-Consumer MUSS die Konfiguration aller notwendigen
Netzwerk-Routen ermöglichen. **[\<=]**

**A_17474 - Anzeige IP-Routinginformationen**

Der Basis- und KTR-Consumer MUSS über die Managementschnittstelle die
konfigurierten IP-Routen und die aktuelle IP-Routingtabelle mit mindestens
folgenden Informationen anzeigen:

 ---> UL

**[\<=]**

Zur Bekanntmachung von Änderungen und Neuanschlüssen zu den, an die TI
angeschlossenen, weiteren Anwendungen des Gesundheitswesens für den
Datenaustausch (WANDA Smart) wird tagesaktuell eine Datei mit dem Namen
"Bestandsnetze.xml" bereitgestellt (siehe dazu [gemSpec_KSR#9/Anhang C]). Die
Datei liefert für alle angeschlossenen WANDA Smart einen Namen/ID,
Netzwerkinformationen (IP-Adressen) und den für dieses Netz zu verwendenden
DNS Server welcher dem DNS Forwarder des Basis- und KTR-Konsumer übergeben
wird.

**A_17576 - KSR lokalisieren**

Der Basis- und KTR-Consumer MUSS für die Lokalisierung des
Konfigurationsdienstes der TI (KSR) die Möglichkeit der Lokalisierung des KSR
durch DNS-Anfragen an den DNS-Forwarder DNS_SERVERS_TI zur Auflösung der
SRV-RR und TXT-RR mit den
Bezeichnern „_ksrkonfig._tcp.ksr.\<TOP_LEVEL_DOMAIN_TI\>“ vorsehen.Der
Basis- und KTR-Consumer erhält damit URLs der Downloadpunkte des KSR
für Konfigurationsdaten (MGM_KSR_KONFIG_URL). **[\<=]**

**A_17574 - Infrastruktur Konfiguration aktualisieren**

Der Basis- und KTR-Consumer MUSS täglich seine Infrastruktur Konfiguration
aktualisieren.Der Basis- und KTR-Consumer MUSS dazu eine TLS-Verbindung zum
Konfigurationsdienst der TI aufbauen. Dabei MUSS er das durch den Server
präsentierte Zertifikat prüfen.Das Herunterladen der Konfigurationsdaten
erfolgt mittels I_KSRS_Download::get_Ext_Net_Config (MGM_KSR_KONFIG_URL,
„Bestandsnetze.xml“.) **[\<=]**

### 5.1.2 Zeitdienst

Der Zeitdienst schafft die Grundlage einer gleichen Systemzeit für alle in der
TI einzusetzenden Produkttypen.Innerhalb des Basis- und KTR-Consumers ist
dafür ein NTP-Client erforderlich, welcher die Zeitangaben des Zeitdienstes
der zentralen TI abfragt und verwendet. Die in [gemSpec_Net#6.2.2]
„Nutzung“ getroffenen Anforderungen werden durch dieses Kapitel erweitert.

**A_17485 - Maximale Zeitabweichung**

Der Basis- und KTR-Consumer MUSS sicherstellen, dass der maximale zulässige
Fehler von +/- 20ppm (part per million) gegenüber einer Referenzuhr nicht
überschritten wird. Dies entspricht einer maximalen Abweichung im Freilauf von
+/- 34,56 Sekunden über 20 Tage. **[\<=]**

### 5.1.3 Namensdienst und Dienstlokalisierung

### 5.1.3.1 Funktionsmerkmalweite Aspekte

**A_17498 - Grundlagen des Namensdienstes**

Der Basis- und KTR-Consumer MUSS die Funktion eines Recursive Caching
Nameservers zur Auflösung von DNS-Anfragen anbieten. (Im Folgenden kurz
DNS-Server genannt).Der Caching-Nameserver des Basis- und KTR-Consumer MUSS
für Clientsysteme aus dem lokalen Netzwerk der Einsatzumgebung erreichbar
sein.Der Caching Nameserver des Basis- und KTR-Consumer MUSS einen sinnvollen
Timeout für die Bearbeitung von DNS-Abfragen beachten. Konnte eine DNS-Abfrage
nicht durchgeführt werden, MUSS die Bearbeitung abgebrochen werden.  **[\<=]**

**A_17499 - DNS-Forwards des DNS-Servers**

Der DNS-Server des Basis- und KTR-Consumer MUSS die folgenden DNS-Forwards
durchführen: 

Tabelle2: TAB_CONS_687 DNS-Forwards des DNS-Servers

<table><tr><th>
Domain

</th><th>
Forwarders

</th><th>
Bemerkungen

</th></tr><tr><td>
Namensraum

TI (*.DNS_TOP_  
LEVEL_DOMAIN_TI)

</td><td>
DNS_SERVERS_TI

</td><td>
DNS Forward

Rule

zur Auflösung aller DNS-Namen innerhalb des Namensraums der TI.

</td></tr><tr><td>
Namensraum angeschlossene Netze des Gesundheitswesens mit

WANDA Basic  
(Domainnamen  
von angeschlossenen Netzen des

Gesundheitswesens mit

WANDA Basic

gemäß  
Bestandsnetze.xml) 

</td><td>
DNS_SERVERS_BESTANDSNETZE  
(Je Domainnamen eines angeschlossenen Netzes des
Gesundheitswesens mit

WANDA Basic

alle zugehörigen DNS-Server IP-Adressen gemäß Bestandsnetze.xml) 

</td><td>
Je angeschlossenem Netz des Gesundheitswesens mit

WANDA Basic

in NLW_AKTIVE_BESTANDSNETZE wird eine DNS Forward

Rule

zur Auflösung von DNS-Namen innerhalb dieses Netzes verwendet. 

</td></tr><tr><td>
Namensraum lokale Einsatzumgebung

</td><td>
DNS_SERVERS_CONSUMER

</td><td>
DNS Forward

Rule

zur Auflösung aller DNS-Namen innerhalb der DNS-Domain im LAN des Consumer

</td></tr></table>

**[\<=]**

**A_17500 - DNS Stub-Resolver**

Der Basis- und KTR-Consumer MUSS von allen internen Diensten zur
Namensauflösung genutzt werden.Der Stub-Resolver im Basis- und KTR-Consumer
MUSS immer den Caching Nameserver im Basis- und KTR-Consumer anfragen. **[\<=]**

### 5.1.3.2 Interne TUCs, auch durch Fachmodule nutzbar

### 5.1.3.2.1 TUC_CON_362 „Liste der Dienste abrufen“

**A_17502 - TUC_CON_362 „Liste der Dienste abrufen“**

Der Basis- und KTR-Consumer MUSS den technischen Use Case TUC_CONS_362 „Liste
der Dienste abrufen“ umsetzen.

Tabelle3: TAB_CONS_648 – TUC_CONS_362 „Liste der Dienste abrufen“

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
Name

</td><td>
TUC „Liste der Dienste abrufen“

</td></tr><tr><td>
Beschreibung

</td><td>
Ermittlung aller zu einer DNS-SD-Gruppe gehörenden DNS-Namen.

</td></tr><tr><td>
Auslöser

</td><td>
interne Anfrage (Basisdienst oder Fachmodul)

</td></tr><tr><td>
Vorbedingungen

</td><td>
Die vom Basis- und KTR-Consumer zu verwendenden DNS-Server müssen konfiguriert
sein.

</td></tr><tr><td>
Eingangsdaten

</td><td>
FQDN des PTR Resource Records

</td></tr><tr><td>
Komponenten

</td><td>
Basis- und KTR-Consumer

</td></tr><tr><td>
Ausgangsdaten

</td><td>
LIST_OF_SRV_ENTITIES

</td></tr><tr><td>
Standardablauf

</td><td>
Mit dem FQDN wird eine Typ „PTR“ Anfrage an den Stub-Resolver des Basis- und
KTR-Consumer gestellt.

</td></tr></table>

**[\<=]**

### 5.1.3.3 Operationen an der Außenschnittstelle

**A_17509 - Basisanwendung Namensdienst**

Der Basis- und KTR-Consumer MUSS für Clients  in der Einsatzumgebung und den
Fachmodulen im jeweiligen Consumer eine Basisanwendung Namensdienst, mit der
Funktion Namensauflösung und Dienstlokalisierung anbieten.

Tabelle4: Basisanwendung Namensdienst

<table><tr><th>
Name

</th><th colspan="2">
Namensdienst

</th></tr><tr><td>
Version

</td><td colspan="2">
wird im Produktsteckbrief des Basis- und KTR-Consumer definiert

</td></tr><tr><td>
Namensraum

</td><td colspan="2">
Keiner

</td></tr><tr><td>
Namensraum-Kürzel

</td><td colspan="2">
Keiner

</td></tr><tr><td rowspan="2">
Operationen

</td><td>
Name

</td><td>
Kurzbeschreibung

</td></tr><tr><td>
GetIPAddress

</td><td>
Diese Operation ermöglicht die Auflösung von FQDNs in IP-Adressen

</td></tr><tr><td>
WSDL

</td><td colspan="2">
Keines

</td></tr><tr><td>
Schema

</td><td colspan="2">
Keines

</td></tr></table>

**[\<=]**

### 5.1.3.4 Betriebsaspekte

**A_17512-01 - Initialisierung „Namensdienst und Dienstlokalisierung“**

DerBasis- und KTR-Consumer MUSS in der Bootup-Phase zur Initialisierung des
Funktionsmerkmals „Namensdienst und Dienstlokalisierung“
den Caching-Nameserver starten. **[\<=]**

**A_17513 - Konfigurationsparameter Namensdienst und Dienstlokalisierung**

Der Administrator des Basis- und KTR-Consumer MUSS die aufgelisteten Parameter
in Tabelle 5 über die Managementschnittstelle konfigurieren und die
aufgelisteten Parameter in Tabelle 6 ausschließlich einsehen können.Nach
jeder Änderung MUSS sichergestellt werden, dass die Änderungen sofort am
autoritativen bzw. am Caching Nameserver zur Verfügung stehen.

Tabelle5: Konfigurationsparameter Namensdienst

<table><tr><th>
ReferenzID

</th><th>
Belegung

</th><th>
Bedeutung und Administrator-Interaktion

</th></tr><tr><td>
DNS_SERVERS_  
CONSUMER

</td><td>
Liste von IP-Adressen der DNS-Server

</td><td>
Liste von DNS-Servern, die zur Namensauflösung von Namensräumen in der
Einsatzumgebung verwendet werden.  
Der Administrator MUSS die Liste von
DNS-Servern, die die DNS_DOMAIN_CONSUMER auflösen, bearbeiten können.  
Die
IP-Adressen der DNS-Server KÖNNEN auf den Adressbereich der
ANLW_LAN_IP_ADDRESS eingeschränkt sein.

</td></tr><tr><td>
DNS_DOMAIN_  
CONSUMER

</td><td>
DNS Domainname

</td><td>
DNS Domainname, der von einem DNS-Server der Einsatzumgebung aufgelöst wird.
Der Name DARF NICHT mit einem „.“ beginnen.

</td></tr></table>

Tabelle6: Einsehbare Konfigurationsparameter Namensdienst

<table><tr><th>
ReferenzID

</th><th>
Belegung

</th><th>
Bedeutung

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

**[\<=]**

### 5.2 Sicherheit

Die Sicherheits- und Datenschutzanforderungen sind abgedeckt durch die
übergreifenden Sicherheits- und Datenschutzanforderungen an Hersteller und
Anbieter [gemSpec_DS_Hersteller], [gemSpec_DS_Anbieter], die spezifischen
Sicherheits- und Datenschutzanforderungen des Clientmoduls KOM-LE im
Basis-Consumer [gemSpec_CM_KOMLE] und des Fachmoduls ePA im KTR-Consumer
[gemSpec_FM_ePA_KTR_Consumer] sowie die spezifischen Sicherheits- und
Datenschutzanforderungen der Systemprozesse der dezentralen TI
[gemSpec_Systemprozesse_dezTI].

### 5.3 Identitäten

In diesem Dokument werden kryptographische Identitäten entsprechend ihrer
Bezeichner im Objektsystem der SMC-B referenziert. Dies dient der Eindeutigkeit
der Referenz und bedeutet nicht, dass die Strukturen des Objektsystems der
SMC-B in einem HSM nachgebildet werden müssen.

Im KTR-Consumer werden private Schlüssel der SMC-B in einem HSM gespeichert. Im
Basis-Consumer werden private Schlüssel der SMC-B in einem HSM oder auf einer
SMC-B in Kartenform gespeichert. Das Schlüsselmaterial des KOM-LE-Clientmoduls
hingegen wird auch hier in einem HSM gespeichert.

Nachfolgend wird festgelegt, welche Qualitäten dabei erreicht werden müssen
und was bei der Personalisierung zu beachten ist.

**A_17598 - Qualität des HSM**

Die Basis- und KTR-Consumer MÜSSEN privates Schlüsselmaterial zu Zertifikaten
der Telematikinfrastruktur in einem HSM, dessen Eignung durch eine
erfolgreiche Evaluierung nachgewiesen wurde, integritätsgeschützt und
vertraulich speichern. Als Evaluierungsschema kommen dabei Common Criteria oder
Federal Information Processing Standard (FIPS) in Frage. Die Prüftiefe MUSS
mindestens (a) FIPS 140-2 Level 3, oder (b) Common Criteria EAL 4 entsprechen.
**[\<=]**

**A_18195 - Basis-Consumer mit SMC-B**

Der Basis-Consumer KANN privates Schlüsselmaterial einer SMC-B in Kartenform
nutzen. **[\<=]**

<table><tr><th>
Aspekt

</th><th>
Beschreibung

</th></tr><tr><td>
Schlüsselmaterial der SMC-B

</td><td>
Das Schlüsselmaterial wird sicher im HSM erzeugt.  
Das private
Schlüsselmaterial verlässt das HSM nicht oder nur zum Zwecke eines Backups
auf einem Backup-HSM, wobei die Übertragung hinsichtlich Vertraulichkeit
geschützt sein muss.

</td></tr><tr><td>
Zertifikatsrequest

</td><td>
Die benötigten Zertifikatsrequests werden im HSM erzeugt und exportiert.  
Die
Zertifikatsrequests werden unter Wahrung der Authentizität und Integrität dem
TSP übermittelt.

</td></tr><tr><td>
Zertifikat

</td><td>
Das Zertifikat wird vom TSP zum Betreiber übermittelt.

</td></tr><tr><td>
TLS-Schlüsselmaterial des KOM-LE-Clientmoduls

</td><td>
Der KOM-LE-Anbieter erzeugt die Schlüsselpaare für die Zertifikate des
KOM-LE-Clientmoduls und bezieht aus der Komponenten-PKI der TI die
C.CM.TLS-CS-Zertifikate. Das Schlüsselpaar muss zur sicheren Speicherung ins
HSM eingebracht werden.

</td></tr></table>

Hinweis:

 ---> UL

**A_17599 - Personalisierung des HSM**

Der Anbieter des Basis- oder KTR-Consumers MUSS einen sicheren Prozess zur
Personalisierung des HSMs definieren und etablieren, der die in
Tab_Personalisierung_HSM genannten Aspekte beinhaltet. **[\<=]**

**A_18196 - Personalisierung des HSM beim Basis-Consumer**

Der Anbieter eines Basis-Consumers, der ausschließlich mit SMC-Bs in Kartenform
arbeitet, KANN auf einen Prozess zur Personalisierung der Identitäten der
SMC-B im HSM verzichten. **[\<=]**

### 5.4 Schnittstellen

Für den Basis- und KTR-Consumer werden einheitliche Schnittstellen definiert
und im Rahmen des Zulassungstests genutzt. Für eine bessere
Integrationsfähigkeit ist es aber erlaubt, dass zusätzlich zu den definierten
Schnittstellen auch weitere Schnittstellentechnologien genutzt werden können,
über welche die festgelegten Operationen angesprochen werden können.

**A_17712 - Zusätzlich alternative Schnittstellentechnologien**

Der Basis- und KTR-Consumer KANN zusätzlich zu den in den Spezifikationen
festgelegten Schnittstellen zusätzlich weitere Schnittstellentechnologien
anbieten, über welche die festgelegten Operationen angesprochen werden
können. **[\<=]**

### 6 Funktionsmerkmale

### 6.1 Verschlüsselungsdienst

### 6.1.1 Durch Module nutzbare TUCs

**A_17466 - Systemprozess PL_TUC_HYBRID_ENCIPHER**

Der Basis- und KTR-Consumer MUSS den Systemprozess PL_TUC_HYBRID_ENCIPHER
implementieren und bereitstellen. **[\<=]**

**A_17467 - Systemprozess PL_TUC_HYBRID_DECIPHER**

Der Basis- und KTR-Consumer MUSS den Systemprozess PL_TUC_HYBRID_DECIPHER
implementieren und bereitstellen. **[\<=]**

### 6.1.2 Operationen an der Clientschnittstelle

**A_17477 - Basisdienst Verschlüsselungsdienst**

Der Basis- und KTR-Consumer MUSS für Clients einen Basisdienst
Verschlüsselungsdienst anbieten.

Tabelle8: Tab_Verschlüsselungsdienst

<table><tr><th>
Name

</th><th colspan="2">
EncryptionService

</th></tr><tr><td>
Version

</td><td colspan="2">
Siehe Anhang

</td></tr><tr><td>
Namensraum

</td><td colspan="2">
Siehe Anhang

</td></tr><tr><td>
Namensraum-Kürzel

</td><td colspan="2">
CRYPT für Schema und CRYPTW für WSDL

</td></tr><tr><td rowspan="3">
Operationen

</td><td>
Name

</td><td>
Kurzbeschreibung

</td></tr><tr><td>
EncryptDocument

</td><td>
Dokument hybrid verschlüsseln

</td></tr><tr><td>
DecryptDocument

</td><td>
Dokument hybrid entschlüsseln

</td></tr><tr><td>
WSDL

</td><td colspan="2">
EncryptionService.wsdl

</td></tr><tr><td>
Schema

</td><td colspan="2">
EncryptionService.xsd

</td></tr></table>

**[\<=]**

### 6.1.2.1 EncryptDocument

**A_17510-03 - Basis- und KTR-Consumer, Operation EncryptDocument**

Der Verschlüsselungsdienst des Basis- und KTR-Consumer MUSS an der
Clientschnittstelle eine Operation EncryptDocument anbieten.

Tabelle9: Tab_Operation_EncryptDocument

<table><tr><th>
Name

</th><th colspan="3">
EncryptDocument

</th></tr><tr><td>
Beschreibung

</td><td colspan="3">
Diese Operation verschlüsselt ein übergebenes Dokument hybrid.  
Der
Dokumententyp XML wird gesondert behandelt. Alle anderen Dokumententypen nutzen
die binäre Verschlüsselung

Für die hybride Verschlüsselung wird ein asymmetrischer Schlüssel aus einem
X.509v3-Zertifikat genutzt. Dieses Zertifikat wird als Parameter übergeben
oder auf dem HSM referenziert. Pro Operationsaufruf können mehrere
Hybridschlüssel erzeugt werden.  
Durch das Zertifikat wird festgelegt, ob RSA
oder ECC basierte Hybridschlüssel erzeugt werden. Bei Angabe der Zertifikate
über CertificateOnCard (Referenz auf HSM) wird das Verschüsselungsverfahren
durch die Angabe in Crypt bestimmt. Es können Hybridschlüssel für RSA oder
ECC oder beide Verfahren erzeugt werden.  
Für alle Dokumententypen wird immer
das gesamte Dokument verschlüsselt.

</td></tr><tr><td rowspan="9">
Aufrufparameter

</td><td colspan="3">
![Img-002][Img-002]

</td></tr><tr><td colspan="3">
![Img-003][Img-003]

</td></tr><tr><td>
RecipientKeys

</td><td colspan="2">
Identifiziert die Empfänger der zu verschlüsselnden Nachricht über
X.509-Zertifikate (öffentliche Schlüssel). Quelle für die Zertifikate kann
eine Karte sein, die per CertificateOnCard-Element referenziert wird, oder der
Aufrufer, der X.509-Zertifikate im Certificate-Element übergibt.

</td></tr><tr><td>
CardHandle

</td><td colspan="2">
Identifiziert die zu verwendende Karte mit dem (öffentlichen) Schlüssel.  
Ist
das Element nicht vorhanden, so werden nur Zertifikate per Element

Certificate

übergeben.

</td></tr><tr><td>
Crypt

</td><td colspan="2">
Der Wert dieses Parameters ist in Tabelle Tab_KeyReference_für_Encrypt/Decrypt
spezifiziert und gibt den Typ von Zertifikaten und dadurch das Verfahren für
die Erzeugung der Hybridschlüssel vor. (Default-Wert ist RSA) 

</td></tr><tr><td>
Certificate

</td><td colspan="2">
Certificate

ist ein Base64-kodiertes XML-Element, in dem das Zertifikat, das den
asymmetrischen Schlüssel enthält (öffentlicher Schlüssel), DER-kodiert
übergeben wird.  
Es kann eine Liste von Zertifikaten übergeben werden. 

Dieses Element kann leer sein, wenn ausschließlich Zertifikate verwendet
werden sollen, die über CertificateOnCard angegeben werden.

</td></tr><tr><td>
CONSUMER:

Document

</td><td colspan="2">
Dieses entsprechend [OASIS-DSS] Section 2.4.2 spezifizierte Element enthält das
zu verschlüsselnde Dokument, wobei das Kindelement

dss:Base64Data

 oder 

CONSUMER:Base64XML 

verwendet wird.  
Das zugeordnete Verschlüsselungsverfahren ist

 ---> UL

</td></tr><tr><td colspan="3">
![Img-004][Img-004]

</td></tr><tr><td>
CRYPT:

Optional

Inputs

</td><td colspan="2">
Enthält die optionalen Parameter CRYPT:UnprotectedProperties und
CRYPT:EncryptionType.

</td></tr><tr><td>
Encryption

Type

</td><td colspan="2" rowspan="1">
Dieses optionale Element bestimmt das Verschlüsselungsverfahren.

Es MUSS das Verfahren XMLEnc:
„http://www.w3.org/TR/xmlenc-core/" unterstützt werden, wenn das Dokument in

CONSUMER:Base64XML

übergeben wird und  CMS: „urn:ietf:rfc:5652“, wenn das Dokument in

dss:Base64Data

 übergeben wird.

Die Verwendung dieses Elements ist aufgrund der impliziten Zuordnung der
Verschlüsselungsverfahren zur Methode der Dokumentübergabe nicht erforderlich.

</td></tr><tr><td>
</td><td colspan="2">
CRYPT:

Unprotected

Properties

</td><td>
Dieses optionale Element wird nur für das Verschlüsselungsverfahren CMS
ausgewertet (zu verschlüsselndes Dokument ist in dss:Base64Data vorhanden).

Die Elemente

./UnprotectedProperties/Property/Value/CMSAttribute

müssen base64/DER-kodiert ein vollständiges ASN.1-

Attribute

enthalten, definiert in [CMS# 9.1.AuthenticatedData Type]. Es muss bei der
Erstellung des CMS-Containers unter

"unauthAttrs"

aufgenommen werden. Das zugehörige Element

./UnprotectedProperties/Property/Identifier

wird nicht ausgewertet.

</td></tr><tr><td rowspan="3">
Rückgabe

</td><td colspan="3">
![Img-005][Img-005]

</td></tr><tr><td>
Status

</td><td colspan="2">
Enthält den Ausführungsstatus der Operation.

</td></tr><tr><td>
Document

</td><td colspan="2">
Enthält das verschlüsselte Dokument in Base64-codierter Form, wenn die
Verschlüsselung erfolgreich durchgeführt wurde.  
Im Fall XMLEnc wird das
verschlüsselte XML-Dokument in CONSUMER:Document/CONSUMER:Base64XML
zurückgegeben.  
Im Fall CMS wird das verschlüsselte Dokument in
CONSUMER:Docum  
ent/dss:Base64data zurückgegeben.

</td></tr><tr><td>
Vorbe-dingungen

</td><td colspan="3">
Keine

</td></tr><tr><td>
Nachbe-dingungen

</td><td colspan="3">
Keine

</td></tr></table>

Vor der Verwendung für die Verschlüsselung MÜSSEN Zertifikate durch den
Aufruf von PL_TUC_PKI_VERIFY_CERTIFICATE auf ihre Gültigkeit geprüft werden.

Abgelaufene oder gesperrte Zertifikate MÜSSEN von der Verwendung ausgeschlossen
werden.

Das Verschlüsseln erfolgt durch Aufruf von PL_TUC_HYBRID_ENCIPHER {

   Doc, das zu verschlüsselnde Dokument =

CONSUMER:Document;

   {Cert(i)}, „Menge der Empfänger-/Ziel-Zertifikate“ =

RecipientKeys;

    Attribute,

optionale, zusätzliche Attribute = UnprotectedProperties;

}

Wird ein Zertifikat per CertificateOnCard-Element referenziert, ist dieses
vorher durch den HSMProxy zu extrahieren **[\<=]**

### 6.1.2.2 DecryptDocument

**A_17515-02 - Basis- und KTR-Consumer, Operation DecryptDocument**

Der Verschlüsselungsdienst des Basis- und KTR-Consumer MUSS an der
Clientschnittstelle eine OperationDecryptDocumentanbieten.

Tabelle10: Tab_Operation_DecryptDocument

<table><tr><th>
Name

</th><th colspan="2">
DecryptDocument

</th></tr><tr><td>
Beschreibung

</td><td colspan="2">
Diese Operation entschlüsselt ein hybrid verschlüsseltes Dokument.  
Es werden
die Dokumententypen XML und Andere (Binär) unterstützt.

Für die Entschlüsselung wird ein asymmetrischer Schlüssel zu einem
X.509v3-Zertifikat genutzt.  
Das Kryptoverfahren (RSA oder ECC) wird durch den
Hybridschlüssel des verschlüsselten Dokuments bestimmt. Liegt eine
Verschlüsselung sowohl für RSA, als auch ECC vor, erfolgt vorrangig eine
Entschlüsselung mittels des ECC-Schlüssels.

</td></tr><tr><td rowspan="6">
Aufrufparameter

</td><td colspan="2">
![Img-006][Img-006]

</td></tr><tr><td colspan="2">
![Img-007][Img-007]

</td></tr><tr><td>
PrivateKey

OnCard

</td><td>
Identifiziert die zu verwendende Karte mit dem (privaten) Schlüssel.

</td></tr><tr><td>
CardHandle

</td><td>
Identifiziert die Karte.

</td></tr><tr><td>
Crypt

</td><td>
Wird nicht verwendet. Die Auswahl des Kryptoverfahrens erfolgt anhand des
Hybridschlüssels des verschlüsselten Dokuments..

</td></tr><tr><td>
CONSUMER:

Document

</td><td>
Enthält das base64-codierte Dokument, das entschlüsselt werden soll.

</td></tr><tr><td rowspan="3">
Rückgabe

</td><td colspan="2">
![Img-008][Img-008]

</td></tr><tr><td>
Status

</td><td>
Enthält den Ausführungsstatus der Operation.

</td></tr><tr><td>
Document

</td><td>
Enthält das entschlüsselte Dokument in Base64-codierter Form.  
Im Fall der
Verschlüsselung mit XMLEnc wird das entschlüsselte XML-Dokument in
CONSUMER:Document/CONSUMER:Base64XML zurückgegeben.  
Im Fall der
Verschlüsselung mit CMS wird das entschlüsselte Dokument in
CONSUMER:Document/dss:Base64data zurückgegeben.

</td></tr><tr><td>
Vorbedingungen

</td><td colspan="2">
Keine

</td></tr><tr><td>
Nachbedingungen

</td><td colspan="2">
Keine

</td></tr></table>

Das Entschlüsseln erfolgt durch Aufruf von PL_TUC_HYBRID_DECIPHER {

   D, "das verschlüsselte Dokument =

CONSUMER:Document;

   Id, "(Identität des) Empfänger" =

PrivateKeyOnCard;

} **[\<=]**

<table><tr><th>
Karte

</th><th>
Crypt (Wert)

</th><th>
KeyReference (Encrypt)

</th><th>
KeyReference (Decrypt)

</th></tr><tr><td>
In DF.ESIGN

</td><td>
In DF.ESIGN

</td></tr><tr><td colspan="1" rowspan="3">
SM-B  
(HSM)

</td><td>
RSA

</td><td>
EF.C.HCI.ENC.R2048

</td><td>
PrK.HCI.ENC.R2048

</td></tr><tr><td>
ECC

</td><td>
EF.C.HCI.ENC.E256

</td><td>
PrK.HP.ENC.E256

</td></tr><tr><td>
RSA_ECC

</td><td>
EF.C.HCI.ENC.R2048  
EF.C.HCI.ENC.E256

</td><td>
PrK.HCI.ENC.R2048

PrK.HP.ENC.E256

</td></tr></table>

### 6.2 Signaturdienst

### 6.2.1 Durch Module nutzbare TUCs

**A_17517 - Systemprozess PL_TUC_SIGN_DOCUMENT_nonQES**

Der Basis- und KTR-Consumer MUSS den Systemprozess PL_TUC_SIGN_DOCUMENT_nonQES
implementieren und bereitstellen. **[\<=]**

**A_17518 - Systemprozess PL_TUC_SIGN_HASH_nonQES**

Der Basis- und KTR-Consumer MUSS den Systemprozess PL_TUC_SIGN_HASH_nonQES
implementieren und bereitstellen. **[\<=]**

**A_17577 - Systemprozess PL_TUC_VERIFY_DOCUMENT_nonQES**

Der Basis- und KTR-Consumer MUSS den Systemprozess PL_TUC_VERIFY_DOCUMENT_nonQES
implementieren und bereitstellen. **[\<=]**

### 6.2.2 Operationen an der Clientschnittstelle

**A_17523 - Basisdienst Signaturdienst**

Der Basis- und KTR-Consumer MUSS Clientsystemen einen Basisdienst Signaturdienst
(nonQES) anbieten.

Tabelle12: Tab_Signaturdienst

<table><tr><th>
Name

</th><th colspan="2">
SignatureService

</th></tr><tr><td>
Version

</td><td colspan="2">
Siehe Anhang

</td></tr><tr><td>
Namensraum

</td><td colspan="2">
Siehe Anhang

</td></tr><tr><td>
Namensraum-Kürzel

</td><td colspan="2">
SIG für Schema und SIGW für WSDL

</td></tr><tr><td rowspan="4">
Operationen

</td><td>
Name

</td><td>
Kurzbeschreibung

</td></tr><tr><td>
SignDocument

</td><td>
Dokument signieren

</td></tr><tr><td>
VerifyDocument

</td><td>
Signatur verifizieren

</td></tr><tr><td>
ExternalAuthenticate

</td><td>
Binärstring signieren

</td></tr><tr><td>
WSDL

</td><td colspan="2">
SignatureService.wsdl

</td></tr><tr><td>
Schema

</td><td colspan="2">
SignatureService.xsd

</td></tr></table>

**[\<=]**

### 6.2.2.1 SignDocument

**A_17525-02 - Basis- und KTR-Consumer, Operation SignDocument**

Der Signaturdienst des Basis- und KTR-Consumer MUSS an der Clientschnittstelle
eine an [OASIS-DSS] angelehnte OperationSignDocumentwie in Tabelle
Tab_Operation_SignDocument beschrieben anbieten.

Tabelle13: Tab_Operation_SignDocument

<table><tr><th>
Name

</th><th colspan="2">
SignDocument

</th></tr><tr><td>
Beschreibung

</td><td colspan="2">
Diese Operation lehnt sich an [OASIS-DSS] an. Sie enthält voneinander
unabhängige SignRequests. Jeder SignRequest erzeugt eine Signatur für ein
Dokument.

Zur Signaturerzeugung werden Schlüssel und Zertifikate eines HSM benutzt. Es
wird ausschließlich der Signaturtyp "CMS-Signatur" gemäß [RFC 5652] (URI
urn:ietf:rfc:5652) und das Profil CAdES-BES gemäß[CAdES] verwendet.

</td></tr><tr><td rowspan="10">
Aufruf-parameter

</td><td colspan="2">
![Img-009][Img-009]

</td></tr><tr><td>
PrivateKeyOnCard

</td><td>
Identifiziert die zu verwendende Karte mit dem (privaten) Schlüssel.

</td></tr><tr><td>
CardHandle

</td><td>
Identifiziert die zu verwendende Signaturkarte.

</td></tr><tr><td>
Crypt

</td><td>
Dieser Parameter steuert die Auswahl der Zertifikate und Schlüssel für die
Signaturerstellung. Die Werte sind in der Tabelle
Tab_Zertifikate_für_Sign/VerifyDocument vorgegeben.  
(Default-Wert ist RSA)

</td></tr><tr><td>
SIG:SignRequest

</td><td>
Ein

SignRequest

kapselt den Signaturauftrag für ein Dokument.

Das verpflichtende XML-Attribut

RequestID

identifiziert einen

SignRequest

innerhalb eines Stapels von

SignRequests

eindeutig. Es dient der Zuordnung der

SignResponse

zum jeweiligen

SignRequest

.

</td></tr><tr><td>
SIG:OptionalInputs

</td><td>
Enthält optionale Eingangsparameter (angelehnt an

dss:OptionalInputs

gemäß [OASIS-DSS] Section 2.7):

![Img-010][Img-010]

</td></tr><tr><td>
SIG:Document

</td><td>
![Img-011][Img-011]

Dieses an das

dss:Document

Element aus [OASIS-DSS] Section 2.4.2 angelehnte Element enthält das zu
signierende Dokument in dss:Base64Data.

</td></tr><tr><td>
dss:SignatureType

</td><td>
Durch dieses in [OASIS-DSS] (Abschnitt 3.5.1) beschriebene Element kann der
generelle Typ der zu erzeugenden Signaturen angegeben werden.  
Es muss der
Signaturtyp CMS-Signatur (URI urn:ietf:rfc:5652) unterstützt werden.  
Fehlt
dieses Element, so muss der Signaturtyp CMS-Signatur (URI urn:ietf:rfc:5652)
implizit verwendet werden.

</td></tr><tr><td>
dss:Properties

</td><td>
Durch dieses in [OASIS-DSS] (Abschnitt 3.5.5) definierte Element können
zusätzliche signierte und unsignierte Eigenschaften (Properties) bzw.
Attribute in die Signatur eingefügt werden  
.  
Es dürfen genau die
folgenden Attribute 

./SignedProperties/Property/Value/CMSAttribute

und

./UnsignedProperties/Property/Value/CMSAttribute

enthalten sein.  
Ein solches XML-Element

CMSAttribute

muss ein vollständiges, base64/DER-kodiertes ASN.1-

Attribute

enthalten, definiert in [CMS#5.3.SignerInfo Type]. Es muss bei der Erstellung
des CMS-Containers unverändert unter

SignedAttributes bzw. UnsignedAttributes

aufgenommen werden.

</td></tr><tr><td>
SIG:IncludeEContent

</td><td>
Durch dieses in [OASIS-DSS] (Abschnitt 3.5.7), definierte Element kann bei einer
CMS-basierten Signatur das Einfügen des signierten Dokumentes in die Signatur
angefordert werden.  
Fehlt dieses Element oder ist der Wert = "'false', wird
die Signaturvariante "detached" verwendet, ansonsten "enveloping".

</td></tr><tr><td rowspan="7">
Rückgabe

</td><td colspan="2">
![Img-012][Img-012]

</td></tr><tr><td>
SIG:SignResponse

</td><td>
Eine

SignResponse

kapselt den ausgeführten Signaturauftrag pro Dokument. Die Zuordnung zwischen

SignRequest

und

SignResponse

erfolgt über die RequestID.

</td></tr><tr><td>
CONSUMER:Status

</td><td>
Enthält den Status der ausgeführten Operation pro SignRequest.

</td></tr><tr><td>
SIG:OptionalOutputs

</td><td>
Enthält optionale Ausgangsparameter.  
Dieses Element wird durch den Basis-
und KTR-Consumer nicht befüllt.

![Img-013][Img-013]

</td></tr><tr><td>
SIG:DocumentWith

Signature

</td><td>
Dieses Element wird durch den Basis- und KTR-Consumer nicht befüllt.

</td></tr><tr><td>
vr:VerificationReport

</td><td>
Dieses Element wird durch den Basis- und KTR-Consumer nicht befüllt.

</td></tr><tr><td>
dss:SignatureObject

</td><td>
Enthält im Erfolgsfall die erzeugte Signatur in Form eines

dss:SignatureObject

-Elements gemäß [OASIS-DSS] (Abschnitt 3.2).

Der Signaturwert wird im XML-Element

dss:SignatureObject/dss:Base64Signature

übergeben.  
Der Signatur-Typ (CMS Signatur) in

dss:SignatureObject/dss:Base64Signature/@Type

Die XML-Elemente

dss:SignatureObject/ds:Signature

dss:SignatureObject/dss:Timestamp

dss:SignatureObject/dss:SignaturePtr

dss:SignatureObject/dss:Other

werden nicht verwendet.

</td></tr><tr><td>
Vorbe-dingungen

</td><td colspan="2">
Keine

</td></tr><tr><td>
Nachbe-dingungen

</td><td colspan="2">
Keine

</td></tr></table>

Das Signieren erfolgt durch Aufruf von PL_TUC_SIGN_DOCUMENT_nonQES {

   IDENTIFIKATOR =

PrivateKeyOnCard;

   DOKUMENT =

SIG:Document

;

   DOKUMENTTYPE =

dss:SignatureType;

}

Die folgende Tabelle führt die zulässigen Zertifikate und Schlüssel für die
nonQES auf:

Tabelle14: Tab_Zertifikate_für_Sign/VerifyDocument(nonQeS)

<table><tr><th>
Karte

</th><th>
Crypt (Wert)

</th><th>
KeyReference (Verify)

</th><th>
KeyReference (Sign)

</th></tr><tr><td>
in DF.ESIGN

</td><td>
in DF.ESIGN

</td></tr><tr><td colspan="1" rowspan="3">
SM-B  
(KTR/Org)  
(HSM)

</td><td>
RSA

</td><td>
EF.C.HCI.OSIG.R2048

</td><td>
PrK.HCI.OSIG.R2048

</td></tr><tr><td>
ECC

</td><td>
EF.C.HCI.OSIG.E256

</td><td>
PrK.HCI.OSIG.E256

</td></tr><tr><td>
RSA_ECC

</td><td>
EF.C.HCI.OSIG.R2048

EF.C.HCI.OSIG.E256

</td><td>
PrK.HCI.OSIG.R2048

PrK.HCI.OSIG.E256

</td></tr></table>

**[\<=]**

### 6.2.2.2 VerifyDocument

**A_17526-02 - Basis- und KTR-Consumer, Operation VerifyDocument**

Der Signaturdienst des Basis- und KTR-Consumer MUSS an der Clientschnittstelle
eine OperationVerifyDocumentwie in Tabelle Tab_Operation_VerifyDocument
beschrieben anbieten.

Tabelle15: Tab_Operation_VerifyDocument

<table><tr><th>
Name

</th><th colspan="3">
VerifyDocument

</th></tr><tr><td>
Beschreibung

</td><td colspan="3">
Diese Operation verifiziert die Signatur eines Dokumentes.

Der Basis- und KTR-Consumer MUSS jede konform zur Clientschnittstelle
SignDocument erzeugte Signatur durch VerifyDocument prüfen können.

Das Ergebnis der Prüfung wird, wenn gefordert, in Form eines standardisierten
Prüfberichts in einer

VerificationReport

-Struktur gemäß [OASIS-VR] zurückgeliefert.

</td></tr><tr><td colspan="1" rowspan="11">
Aufruf-parameter

</td><td colspan="3">
![Img-014][Img-014]

            

</td></tr><tr><td colspan="2">
SIG:

OptionalInputs

</td><td>
Enthält optionale Eingabeparameter (angelehnt an dss:OptionalInputs gemäß
[OASIS-DSS] Section 2.7):

Die zulässigen optionalen Eingabeparameter sind unten erläutert.

</td></tr><tr><td colspan="2">
SIG:

Document

</td><td>
Enthält im Fall der Prüfung von detached oder enveloped Signaturen das zur
Signatur gehörende bzw. das diese umschließende Dokument (siehe [OASIS-DSS]
Section 2.4.2 und oben).

</td></tr><tr><td colspan="2">
dss:

SignatureObject

</td><td>
Enthält die zu prüfende Signatur, wenn sie nicht im Dokument selbst
eingebettet ist ([OASIS-DSS] Kapitel 4.1).  
Die Signatur wird in 

ss:Base64Signature

mit entsprechend gesetztem

Type

-Attribut (siehe

SignatureType

) übergeben, wobei der nachfolgende Werte unterstützt werden muss:

 ---> UL

</td></tr><tr><td colspan="3">
![Img-015][Img-015]

</td></tr><tr><td colspan="2">
SIG:

VerifyManifests

</td><td>
Dieses Element wird durch den Basis-/KTR-Consumer nicht verwendet.

</td></tr><tr><td colspan="3">
![Img-016][Img-016]

</td></tr><tr><td colspan="2">
SIG:

UseVerification

Time

</td><td>
Durch das in [OASIS-DSS] (Abschnitt 4.5.2) spezifizierte Element kann die
Prüfung der Signatur bezüglich eines durch den Aufrufer bestimmten
Zeitpunktes (

Benutzerdefinierter_Zeitpunkt

) erfolgen.

</td></tr><tr><td colspan="2">
dss:

AdditionalKeyInfo

</td><td>
Dieses Element wird durch den Basis-/KTR-Consumer nicht verwendet.

</td></tr><tr><td colspan="2">
vr:

Return

VerificationReport

</td><td>
Durch dieses in [OASIS-VR] spezifizierte Element kann die Erstellung eines
ausführlichen Prüfberichtes angefordert werden.

</td></tr><tr><td colspan="2" rowspan="1">
dss:Schemas

</td><td>
Dieses Element wird durch den Basis-/KTR-Consumer nicht verwendet.

</td></tr><tr><td rowspan="9">
Rückgabe

</td><td colspan="3">
![Img-017][Img-017]

</td></tr><tr><td>
Status

</td><td colspan="2">
Enthält den Ausführungsstatus der Operation.

</td></tr><tr><td>
SIG:

Verifi

cation

Result

</td><td colspan="2">
![Img-018][Img-018]

Das Element

Sig:VerificationResult

enthält das Ergebnis der Prüfung als Ampel, den Typ des zugehörigen
angenommenen Signaturzeitpunkts und der angenommene Signaturzeitpunkt selbst.

</td></tr><tr><td>
SIG:

High

Level

Result

</td><td colspan="2">
Das Ergebnis der Prüfung (Ampelschaltung) mit folgenden Werten:

 ---> UL

</td></tr><tr><td>
SIG:

Time

stamp

Type

</td><td colspan="2">
Der Typ des angenommenen Signaturzeitpunkts mit folgenden Werten:

 ---> UL

Als Format darf jedes zum XML-Typ "dateTime" konforme Format verwendet werden
(\<element name="Timestamp" type="dateTime"/\>). Wenn mehrere Signaturen im
Dokument vorhanden sind, wird hier der angenommene Signaturzeitpunkt der
jüngsten Signatur angegeben.

</td></tr><tr><td>
SIG:

Timestamp

</td><td colspan="2">
Im Element SIG:Timestamp wird der zu SIG:TimestampType gehörende Zeitstempel
zurückgegeben.

</td></tr><tr><td>
SIG:

Optional

Outputs

</td><td colspan="2">
Enthält (angelehnt an dss:OptionalOutputs, wie in Abschnitt 2.7 von [OASIS-DSS]
beschrieben) optionale Ausgangselemente:

![Img-019][Img-019]

</td></tr><tr><td>
dss:

Verify

Manifest

Results

</td><td colspan="2">
Dieses Element wird durch den Basis-/KTR-Consumer nicht verwendet.

</td></tr><tr><td>
vr:

Verification

Report

</td><td colspan="2">
Dieses in [OASIS-VR] spezifizierte Element wird zurückgeliefert, falls das

ReturnVerificationReport

-Element als Eingabeparameter verwendet wurde.

</td></tr><tr><td>
Vorbe-dingungen

</td><td colspan="3">
Keine

</td></tr><tr><td>
Nachbe-dingungen

</td><td colspan="3">
Keine

</td></tr></table>

SigningTime

ist der zu prüfende Signaturzeitpunkt. Dieser ergibt sich wie folgt:

 ---> OL

Das Verifizieren erfolgt durch Aufruf von PL_TUC_VERIFY_DOCUMENT_nonQES {

   SIGNED_DOCUMENT = 

SIG:Document;

  CERTIFICATE = extrahiert aus 

SIG:Document;

  SIGNATURE = 

dss: SignatureObject ;

  TIME_REFERENCE =

SigningTime;

}

. **[\<=]**

### 6.2.2.3 ExternalAuthenticate

**A_17578-01 - Basis- und KTR-Consumer, Operation ExternalAuthenticate**

Der Signaturdienst des Basis- und KTR-Consumer MUSS an der Clientschnittstelle
die OperationExternalAuthenticatewie in Tabelle
Tab_Operation_ExternalAuthenticate beschrieben anbieten.

Tabelle16: Tab_Operation_ExternalAuthenticate

<table><tr><th>
Name

</th><th colspan="3">
ExternalAuthenticate

</th></tr><tr><td>
Beschrei

bung

</td><td colspan="3">
Diese Operation versieht einen Binärstring der maximalen Länge 512 Bit mit
einer nicht-qualifizierten elektronischen Signatur (nonQES).

Dazu wird das Signaturverfahren PKCS#1 oder ECDSA verwendet.

</td></tr><tr><td rowspan="7">
Aufruf

parameter

</td><td colspan="3">
![Img-020][Img-020]

</td></tr><tr><td colspan="2">
Name

</td><td>
Beschreibung

</td></tr><tr><td colspan="2">
CONSUMER:

CardHandle

</td><td>
Identifiziert die zu verwendende Signaturkarte.

</td></tr><tr><td colspan="2">
SIG:

Optional

Inputs

</td><td>
Enthält optionale Eingangsparameter:

![Img-021][Img-021]

</td></tr><tr><td colspan="2">
SIG:

Binary

String

</td><td>
Dieses Element enthält im Kindelement

dss:Base64Data

den zu signierenden Binärstring.

Das XML Attribut

SIG:BinaryString/dss:Base64Data/@MimeType

MUSS den Wert "application/octet-stream" haben.

Die maximale Länge des Binärstrings beträgt 512 Bit entsprechend der maximal
zu erwartenden Hash-Größe.  
Aus der Länge des Binärstrings wird auf das
verwendete Hashverfahren geschlossen. Es werden folgende Längen
unterstützt:  

 ---> UL

Im Falle des Signaturverfahrens RSASSA-PKCS1-v1_5 werden SHA-256, SHA-384 und
SHA-512 unterstützt.

Im Falle des Signaturverfahrens RSASSA-PSS wird SHA-256 unterstützt.

Im Falle des Signaturverfahrens ECDSA wird SHA-256 unterstützt.

Für die Signaturerstellung gilt:

 ---> UL

</td></tr><tr><td colspan="2">
dss:

Signature

Type

</td><td>
Durch dieses in [OASIS-DSS] (Abschnitt 3.5.1) beschriebene Element wird der Typ
der zu erzeugenden Signatur bestimmt. Als Signaturtyp wird unterstützt :

 ---> UL

Andere

SignatureType

-Angaben führen zu einer Fehlermeldung.

Fehlt dieses Element, so wird ebenfalls der Signaturtyp PKCS#1-Signatur
verwendet.

</td></tr><tr><td colspan="2">
SIG:

Signature

Schemes

</td><td>
Durch dieses Element wird für PKCS#1-Signaturen zwischen den folgenden
SignatureScheme-Optionen unterschieden:

 ---> UL

Fehlt dieses Element, so wird als Default-SignatureScheme RSASSA-PSS gewählt.

</td></tr><tr><td rowspan="3">
Rückgabe

</td><td colspan="3">
![Img-022][Img-022]

</td></tr><tr><td>
CONSUMER:

Status

</td><td colspan="2">
Enthält den Status der ausgeführten Operation.

</td></tr><tr><td>
dss:

Signature

Object

</td><td colspan="2">
Enthält im Erfolgsfall die erzeugte Signatur in Form eines

dss:SignatureObject

-Elements gemäß [OASIS-DSS] (Abschnitt 3.2).

Der Signaturwert wird im XML-Element

dss:SignatureObject/dss:Base64Signature

übergeben. Das XML-Attribut

dss:SignatureObject/dss:Base64Signature/@Type

kennzeichnet durch den Wert:

 ---> UL

bzw.

 ---> UL

Die XML-Elemente

dss:SignatureObject/ds:Signature

dss:SignatureObject/dss:Timestamp

dss:SignatureObject/dss:SignaturePtr

dss:SignatureObject/dss:Other

werden nicht verwendet.

</td></tr><tr><td>
Vorbeding

ungen

</td><td colspan="3">
Keine

</td></tr><tr><td>
Nachbeding

ungen

</td><td colspan="3">
Keine

</td></tr></table>

Das Signieren erfolgt durch Aufruf von PL_TUC_SIGN_HASH_nonQES {

   IDENTIFIKATOR =

CardHandle;

   SIGNATURVERFAHREN =

SIG:SignatureSchemes

;

   HASHWERT =

SIG:BinaryString;

} **[\<=]**

### 6.3 Zertifikatsdienst

### 6.3.1 Durch Module nutzbare TUCs

**A_17401 - Systemprozess PL_TUC_PKI_VERIFY_CERTIFICATE**

Der Basis- und KTR-Consumer MUSS den Systemprozess PL_TUC_PKI_VERIFY_CERTIFICATE
implementieren und bereitstellen. **[\<=]**

### 6.3.2 Operationen an der Clientschnittstelle

**A_17408 - Basisdienst Zertifikatsdienst**

Der Basis- und KTR-Consumer MUSS Clientsystemen einen Basisdienst
Zertifikatsdienst zur Verfügung stellen.

Tabelle17: Tab_Zertifikatsdienst

<table><tr><th>
Name

</th><th colspan="2">
CertificateService

</th></tr><tr><td>
Version

</td><td colspan="2">
Siehe Anhang B

</td></tr><tr><td>
Namensraum

</td><td colspan="2">
Siehe Anhang B

</td></tr><tr><td>
Namensraum-Kürzel

</td><td colspan="2">
CERT für Schema und CERTW für WSDL

</td></tr><tr><td rowspan="2">
Operationen

</td><td>
Name

</td><td>
Kurzbeschreibung

</td></tr><tr><td>
VerifyCertificate

</td><td>
Prüfung des Status eines Zertifikats

</td></tr><tr><td>
WSDL

</td><td colspan="2">
CertificateService.wsdl

</td></tr><tr><td>
Schema

</td><td colspan="2">
CertificateService.xsd

</td></tr></table>

**[\<=]**

### 6.3.2.1 VerifyCertificate

**A_17429-01 - Basis- und KTR-Consumer, Operation VerifyCertificate**

Der Zertifikatsdienst des Basis- und KTR-Consumer MUSS an der
Clientschnittstelle eine OperationVerifyCertificatewie in Tabelle
Tab_Operation_VerifyCertificate beschrieben anbieten.

Tabelle18: Tab_Operation_VerifyCertificate

<table><tr><th>
Name

</th><th colspan="3">
VerifyCertificate

</th></tr><tr><td>
Beschreibung

</td><td colspan="3">
Prüft den Status eines Zertifikats.

</td></tr><tr><td rowspan="4">
Aufruf-parameter

</td><td colspan="3">
![Img-023][Img-023]

</td></tr><tr><td>
Name

</td><td colspan="2">
Beschreibung

</td></tr><tr><td>
CERTCMN:

X509Certificate

</td><td colspan="2">
Enthält das base64-codierte Zertifikat, dessen Binärstruktur wiederum
ASN.1-codiert (gemäß [gemSpec_PKI]) vorliegt.

</td></tr><tr><td>
CERT:

VerificationTime

</td><td colspan="2">
Der für die Prüfung zu verwendende Referenzzeitpunkt. Falls der Parameter
nicht angegeben ist, wird als Referenzzeitpunkt die Systemzeit verwendet.

</td></tr><tr><td rowspan="4">
Rückgabe

</td><td colspan="3">
![Img-024][Img-024]

</td></tr><tr><td colspan="2">
Status

</td><td>
Enthält den Ausführungsstatus der Operation.

</td></tr><tr><td colspan="2">
CERT:VerificationStatus

</td><td>
Enthält eines der drei möglichen Prüfungsergebnisse in CERT:VerificationResult

 ---> UL

sowie weiter Details zu den Zuständen „INCONCLUSIVE“ und „INVALID“ in
GERROR:Error.

</td></tr><tr><td colspan="2">
CERT:RoleList

</td><td>
OIDs der im Zertifikat gespeicherten Rollen.

</td></tr><tr><td>
Vorbe-dingungen

</td><td colspan="3">
Keine

</td></tr><tr><td>
Nachbe-dingungen

</td><td colspan="3">
Keine

</td></tr></table>

Der Ablauf der Operation

VerifyCertificate

ist in Tabelle Tab_Ablauf_VerifyCertificate beschrieben:

Tabelle19: Tab_Ablauf_VerifyCertificate

<table><tr><th>
Nr.

</th><th>
Aufruf Technischer Use Case oder Interne Operation

</th><th>
Beschreibung

</th></tr><tr><td>
1.

</td><td>
PL_TUC_PKI_

VERIFY_CERTIFICATE

</td><td>
Die Zertifikatsprüfung erfolgt durch Aufruf von PL_TUC_PKI_VERIFY_CERTIFICATE
{ 

   Zu prüfendes Zertifikat = 

CERTCMN:X509Certificate;

   Referenzzeitpunkt = 

CERT:VerificationTime;

   PolicyList = keine Einschränkung;

   KeyUsage = empty;

   ExtendedKeyUsage = empty;

   OCSP-Graceperiod = empty;

   Offline-Modus = nein;

   OCSP-Response =

empty ;

  Timeout = empty;

  TOLERATE_OCSP_FAILURE = ja;

}

</td></tr><tr><td>
2.

</td><td>
</td><td>
Wenn der Prüfprozess fehlerhaft war und nicht zu einem Ergebnis im Sinne eines
VerificationResult führt, wird eine FaultMessage erzeugt.

War der Prüfprozess erfolgreich, wird eine VerifyCertificateResponse mit

 ---> UL

Ein Prüfergebnis „INCONCLUSIVE“ bzw. „INVALID“ wird in
CERT:VerificationStatus/GERROR:Error mit den zugehörigen Fehlermeldungen
detailliert (in diesem Fall kann CONSUMER:Status/CONSUMER:Result=OK oder
CONSUMER:Status/CONSUMER:Result=Warning gesetzt sein).

</td></tr></table>

Tabelle20: Tab_Übersicht_VerificationResult_VerifyCertificate

<table><tr><th>
CERT:VerificationResult 

</th><th>
Bedeutung

</th></tr><tr><td>
VALID

</td><td>
Wenn  
Gültigkeit zu Referenzzeitpunkt: "gültig"  
Mathematische
Gültigkeit:"gültig"  
OCSP-Prüfung: Online gültig

</td></tr><tr><td>
INVALID

</td><td>
Wenn mindestens ein Wert von (Gültigkeit zu Referenzzeitpunkt, Mathematische
Gültigkeit, OCSP-Prüfung) „ungültig“,„Prüffehler“ oder „gesperrt"
ist.

</td></tr><tr><td>
INCONCLUSIVE

</td><td>
Wenn OCSP-Prüfung „unbekannt“ und die andere Werte „gültig“ sind.

</td></tr></table>

**[\<=]**

### 6.4 LDAP-Proxy

### 6.4.1 Durch Module nutzbare TUCs

**A_17343 - Basis- und KTR-Consumer, LDAPv3 Operationen für interne Module**

Der Basis- und KTR-Consumer MUSS für die in Tab_Ldap_TUC_Mapping aufgelisteten
Systemprozesse die entsprechenden LDAP-Operationen implementieren und zur
Nutzung durch interne Module zur Verfügung stellen.

Tabelle21: Tab_Ldap_TUC_Mapping

<table><tr><th>
LDAPv3-Operation

</th><th>
Systemprozess

</th></tr><tr><td>
Bind

</td><td>
PL_TUC_VZD_BIND

</td></tr><tr><td>
Unbind

</td><td>
PL_TUC_VZD_UNBIND

</td></tr><tr><td>
Search

</td><td>
PL_TUC_VZD_SEARCH

</td></tr><tr><td>
Abandon

</td><td>
PL_TUC_VZD_ABANDON

</td></tr></table>

**[\<=]**

### 6.4.2 Unterstützte LDAPv3-Operationen an der Clientschnittstelle

**A_17341 - Basis- und KTR-Consumer, LDAPv3-Operationen an der
Clientschnittstelle**

Der Basis- und KTR-Consumer MUSS an der Client-Schnittstelle die folgenden
LDAPv3-Operationen für den Zugriff auf den Verzeichnisdienst der TI gemäß
[RFC4511] anbieten.

 ---> UL

Andere LDAPv3-Operationen MÜSSEN mit dem LDAP-Fehler unwillingToPerform (53)
beantwortet werden.

Fehler MÜSSEN gemäß [RFC4511]#Appendix A behandelt werden. **[\<=]**

### 6.5 Clientmodul KOM-LE

### 6.5.1 Allgemeine Anforderungen

**A_17298 - Synchronisation mit der Systemzeit der zentralen TI-Plattform**

Das KOM-LE-Clientmodul MUSS sich unter Verwendung des Systemprozesses
PL_TUC_NET_SYNC_TIME mit der Systemzeit des Zeitservers der zentralen
TI-Plattform synchronisieren. **[\<=]**

**A_17299-01 - Konfigurationsparameter**

Das KOM-LE-Clientmodul MUSS die in Tabelle Tab_Konf_Param aufgelisteten
Parameter über eine Managementoberfläche oder eine Konfigurationsdatei
konfigurierbar gestalten und mit einer Standardkonfiguration entsprechend den
Defaultwerten ausliefern.

Tabelle22: Tab_Konf_Param Standardkonfiguration

<table><tr><th>
Parameter

</th><th>
Beschreibung des Parameters

</th><th>
Defaultwert

</th></tr><tr><td>
ADDRESS_SMTP

</td><td>
URI SMTP-Server

</td><td>
-

</td></tr><tr><td>
ADDRESS POP3

</td><td>
URI POP3-Server

</td><td>
-

</td></tr><tr><td>
PORT_SMTP

</td><td>
SMTP-Port für Clientsysteme

</td><td>
Der Wert muss den Rahmenbedingungen des Herstellers entsprechend gewählt
werden, z.B. als einer der folgenden Werte:

 ---> UL

</td></tr><tr><td>
PORT_POP3

</td><td>
POP3-Port für Clientsysteme

</td><td>
995

</td></tr><tr><td>
SMTP_TIMEOUT_SERVER

</td><td>
Timeout für Antworten vom SMTP-Server auf SMTP-Kommandos

</td><td>
5 Minuten

</td></tr><tr><td>
SMTP_TIMEOUT_CLIENT

</td><td>
Timeout für das Warten auf neue SMTP-Kommandos vom Clientsystem

</td><td>
5 Minuten

</td></tr><tr><td>
POP3_TIMEOUT_SERVER

</td><td>
Timeout für Antworten vom POP3-Server auf POP3-Kommandos

</td><td>
5 Minuten

</td></tr><tr><td>
POP3_TIMEOUT_CLIENT

</td><td>
Timeout für das Warten auf neue POP3-Kommandos vom Clientsystem

</td><td>
5 Minuten

</td></tr><tr><td>
TTL_ENC_CERT

</td><td>
Time to Live für gecachte Verschlüsselungs-zertifikate

</td><td>
24 Stunden

</td></tr><tr><td>
TTL_EMAIL_ICCSN

</td><td>
Time to Live für gecachte Zuordnungen von E-Mail-Adressen der Sender bzw.
Empfänger zu ICCSNs von deren HBAs/SM-Bs

</td><td>
30 Tage

</td></tr><tr><td>
TTL_PROTS

</td><td>
Time to Live für Protokolldateien.

</td><td>
30 Tage

</td></tr><tr><td>
PROT_PERF

</td><td>
Protokolldatei für Performance

</td><td>
JA

</td></tr></table>

**[\<=]**

**A_17503 - Prüfung von TLS-Server-Zertifikaten**

Das KOM-LE-Clientmodul MUSS für die Prüfung von TLS-Server-Zertifikaten der
KOM-LE-Fachdienste den Systemprozess PL_TUC_PKI_VERIFY_CERTIFICATEdes Basis-
und KTR-Consumer benutzen.  **[\<=]**

**A_22664 - Basis-Consumer - Prüfung der verwendeten Clientmodul-Version beim
Senden**

Das KIM-Clientmodul des Basis-Consumers MUSS vor dem Versenden einer Nachricht
die KIM-Version des Absenders mittels des LDAP-Directory
Attributs: komLeData aus dem Verzeichnisdienst [gemSpec_VZD#5] abfragen. Ist
die KIM-Version des Clientmoduls kleiner als die im Verzeichnisdienst
eingetragene, so MUSS das Clientmodul den Absender mit einer E-Mail darüber
informieren. Aus dem Inhalt der E-Mail MUSS hervorgehen, dass die verwendete
Clientmodul-Version veraltet ist. Die E-Mail ist weder zu signieren noch zu
verschlüsseln und entspricht der Delivery Status Notification gemäß
[RFC3461-3464]. Ist die KIM-Version des Clientmoduls größer als die im
Verzeichnisdienst abgefragte Version KANN das Clientmodul des Basis-Consumers
das LDAP-Directory Attribut: komLeData für den Absender mit der neuen
Versionen überschreiben. **[\<=]**

Es wird dem Empfänger von E-Mails die Entscheidung ermöglicht, ob er sich
mitkomLeData 1.5 im Verzeichnisdienst einträgt, oder es bei der 1.0 belässt
und damit keine E-Mails mit Anhängen \> 25 MB empfangen kann.

### 6.5.2 Senden von Nachrichten

**A_17300 - Initialer SMTP-Dialog**

Das KOM-LE-Clientmodul MUSS, nachdem die SMTP-Verbindung zwischen dem
Clientsystem und dem Clientmodul aufgebaut wird und bis zum Punkt an dem das
Clientsystem die Bestätigung des Erfolgs oder Misserfolgs seiner
Authentifizierung erwartet, einen SMTP-Dialog entsprechend der Tabelle
Tab_SMTP_Ant_Init mit dem Clientsystem führen.

Tabelle23: Tab_SMTP_Ant_Init Antworten Clientmodul im CONNECT-Zustand

<table><tr><th>
SMTP-Kommando

(Clientsystem -\> Clientmodul)

</th><th>
SMTP-Antwortcode

(Clientmodul -\> Clientsystem)

</th></tr><tr><td>
HELO

</td><td>
“250 OK” Antwortcode

</td></tr><tr><td>
EHLO

</td><td>
“250 OK” Antwortcode mit folgenden EHLO-Kennworten:

SIZE \<size\>

AUTH LOGIN PLAIN

8BITMIME

ENHANCEDSTATUSCODES

DSN

und \<size\> gleich oder großer als 35882577

</td></tr><tr><td>
AUTH

</td><td>
Anmeldungsdaten erhalten und Verbindungsaufbau mit dem MTA beginnen

</td></tr><tr><td>
RSET, NOOP

</td><td>
„250 OK“ Antwortcode

</td></tr><tr><td>
MAIL, RCPT, DATA

</td><td>
„530 5.7.0“ Antwortcode (Authentication required)

</td></tr><tr><td>
QUIT

</td><td>
„221 OK“ Antwortcode senden und die Verbindung mit dem Clientsystem
schließen

</td></tr><tr><td>
Andere Meldungen

</td><td>
„502  5.5.1“ Antwortcode (Invalid command)

</td></tr></table>

**[\<=]**

**A_17301 - Verbindungsaufbau mit dem SMTP-Servers**

Das KOM-LE-Clientmodul MUSS für den Verbindungsaufbau mit dem SMTP-Server die
Werte der Konfigurationsparameter ADDRESS_SMTP und PORT_SMTP verwenden.
**[\<=]**

**A_17302 - Authentisierung gegenüber dem SMTP-Server mit Benutzernamen und
Passwort**

Das KOM-LE-Clientmodul MUSS den Benutzernamen und das Passwort, die es vom
Clientsystem erhalten hat, für die Authentisierung gegenüber dem SMTP-Server
verwenden. **[\<=]**

**A_17303 - Ergebnis des Verbindungsaufbaus mit dem SMTP-Server**

Das KOM-LE-Clientmodul MUSS das Clientsystem über das Ergebnis des
Verbindungsaufbaus mit dem MTA mit den in Tabelle Tab_SMTP_Verbindung
beschriebenen SMTP-Antwortcodes informieren.

Tabelle24: Tab_SMTP_Verbindung SMTP-Antwortcodes für MTA-Verbindungsaufbau

<table><tr><th>
Bedingung

</th><th>
SMTP-Antwortcode

(Clientmodul -\> Clientsystem)

</th></tr><tr><td>
Das Clientmodul hat sich erfolgreich gegenüber dem MTA mit den vom Clientsystem
erhaltenen Anmeldungsdaten authentifiziert.

</td><td>
235 2.7.0 (Authentication successful)

</td></tr><tr><td>
Das Clientsystem verwendet für die SMTP-Authentifizierung einen anderen
Mechanismus als PLAIN oder LOGIN.

</td><td>
504 5.7.4 (Security features not supported)

</td></tr><tr><td>
Die Verbindung zwischen dem Clientmodul und dem MTA kann nicht aufgebaut werden.

</td><td>
454 4.7.0 (Temporary authentication failure)

</td></tr><tr><td>
Die Authentifizierung gegenüber dem MTA schlägt fehl.

</td><td>
535 5.7.8 (Authentication credentials invalid)

</td></tr></table>

**[\<=]**

**A_17305 - Verwenden von PL_TUC_SIGN_DOCUMENT_nonQES und
PL_TUC_HYBRID_ENCIPHER**

Das KOM-LE-Clientmodul MUSS für das Signieren und Verschlüsseln der
Nachrichten entsprechend dem KOM-LE-S/MIME-Profil die
Systemprozesse PL_TUC_SIGN_DOCUMENT_nonQES und PL_TUC_HYBRID_ENCIPHER des
Basis- und KTR-Consumers verwenden. **[\<=]**

**A_17306 - Vorgehen bei Signatur und Verschlüsselung einer KOM-LE Nachricht**

Das KOM-LE-Clientmodul MUSS zur Signatur und Verschlüsselung von KOM-LE
Nachrichten das folgende Vorgehen umsetzen:

 ---> OL

**[\<=]**

**A_17327 - Signieren der Nachricht mit dem Schlüssel Prk.HCI.OSIG**

Das KOM-LE-Clientmodul MUSS für das Signieren einer KOM-LE-Nachricht den
privaten Schlüssel PrK.HCI.OSIG.R2048der SM-B der jeweiligen Organisation
(Kostenträger oder Leistungserbringerorganisation) verwenden. **[\<=]**

### 6.5.3 Empfangen von Nachrichten

**A_17328 - POP3-Dialog zur Authentifizierung**

Das KOM-LE-Clientmodul MUSS, nachdem die POP3-Verbindung zwischen dem
Clientsystem und dem Clientmodul aufgebaut wurde und bis zu dem Punkt an dem
das Clientsystem die Bestätigung des Erfolgs oder Misserfolgs seiner
Authentifizierung erwartet, einen POP3-Dialog entsprechend Tabelle
Tab_POP3_Ant_Init mit dem Clientsystem führen.

Tabelle25: Tab_POP3_Ant_Init Antworten Clientmodul im CONNECT-Zustand

<table><tr><th>
Clientsystem -\> Clientmodul

</th><th>
Clientmodul -\> Clientsystem

</th></tr><tr><td>
CAPA

</td><td>
“+OK” Antwortcode mit folgenden CAPA Kennworten:

TOP

USER

SASL PLAIN

UIDL

</td></tr><tr><td>
USER, AUTH

</td><td>
Anmeldungsdaten erhalten und Verbindungsaufbau mit dem POP3-Server fortsetzen

</td></tr><tr><td>
QUIT

</td><td>
„+ OK“ Antwortcode senden und die Verbindung mit dem Clientsystem schließen

</td></tr><tr><td>
Andere Meldungen

</td><td>
„-ERR“ Antwortcode

</td></tr></table>

**[\<=]**

**A_17329 - Verbindungsaufbau mit dem POP3-Servers**

Das KOM-LE-Clientmodul MUSS für den Verbindungsaufbau mit dem POP3-Server die
Werte der Konfigurationsparameter ADDRESS_POP3 und PORT_POP3 verwenden.
**[\<=]**

**A_17330 - Authentifizierung gegenüber POP3-Server mit Benutzernamen und
Passwort**

Das KOM-LE-Clientmodul MUSS den Benutzernamen und das Passwort,die es vom
Clientsystem erhalten hat, für die Authentifizierung gegenüber dem
POP3-Server verwenden. **[\<=]**

**A_17331 - Ergebnis des Verbindungsaufbaus mit dem POP3-Server**

Das KOM-LE-Clientmodul MUSS das Clientsystem über das Ergebnis des
Verbindungsaufbaus mit dem POP3-Server mit den in der Tabelle
Tab_POP3_Verbindung beschriebenen POP3-Antwortcodes informieren.

Tabelle26: Tab_POP3_Verbindung Antwortcodes für POP3-Server-Verbindungsaufbau

<table><tr><th>
Bedingung

</th><th>
POP3 Antwortcode

(Clientmodul -\> Clientsystem)

</th></tr><tr><td>
Das Clientsystem hat sich erfolgreich gegenüber dem POP3-Server mit den vom
Clientsystem erhaltenen Anmeldungsdaten authentifiziert.

</td><td>
+OK

</td></tr><tr><td>
Das Clientsystem verwendet für die POP3-Authentifizierung einen anderen
Mechanismus als USER/PASS oder PLAIN.

</td><td>
-ERR

</td></tr><tr><td>
Die Verbindung zwischen dem Clientmodul und dem POP3-Server kann nicht aufgebaut
werden.

</td><td>
-ERR

</td></tr><tr><td>
Die Authentifizierung gegenüber dem MTA schlägt fehl.

</td><td>
-ERR

</td></tr></table>

**[\<=]**

**A_17333 - E-Mail-Adresse des den Abholvorgang auslösenden Nutzers**

Das KOM-LE-Clientmodul MUSS den vom Clientsystem erhaltenen POP3-Usernamen als
die E-Mail-Adresse des den Abholvorgang auslösenden Nutzers betrachten.
**[\<=]**

**A_17504 - Verwenden von PL_TUC_VERIFY_DOCUMENT_nonQES und
PL_TUC_HYBRID_DECIPHER**

Das KOM-LE-Clientmodul MUSS für das Entschlüsseln und die Signaturprüfung der
Nachrichten die Systemprozesse PL_TUC_VERIFY_DOCUMENT_nonQES und
PL_TUC_HYBRID_DECIPHER des Basis- und KTR-Consumers verwenden. **[\<=]**

**A_17337 - Abbrechen des Entschlüsseln, wenn die erforderliche SM-B nicht
verfügbar ist**

Das KOM-LE-Clientmodul MUSS die Entschlüsselung einer Nachricht abbrechen, wenn
die für die Entschlüsselung erforderliche SM-B nicht verfügbar ist. **[\<=]**

**A_17338 - Abbrechen des Entschlüsseln, wenn Freischaltung der erforderlichen
SM-B fehlschlägt**

Das KOM-LE-Clientmodul MUSS die Entschlüsselung einer Nachricht abbrechen, wenn
die Freischaltung der für die Entschlüsselung erforderlichen SM-B
fehlschlägt. **[\<=]**

### 6.6 Realisierung der Leistungen der TI-Plattform

**A_18130 - Nutzung von PL_TUC_CARD Systemprozessen**

Der Basis-Consumer MUSS für den Zugriff auf Smartcards die in
TAB_Systemprozesse mit PL_TUC_CARD_* bezeichneten Systemprozesse benutzen.
**[\<=]**

### 6.6.1 Transportschnittstelle für Kartenkommandos

Wenn der Basis-Consumer Smartcards unterstützt, muss er eine Schnittstelle zu
Karten der TI über ein Kartenterminal herstellen. Diese Schnittstelle muss die
von den Plattformprozessen erzeugten, kartenverständlichen APDUs an die Karte
übertragen. Neben proprietären Schnittstellentreibern von
Kartenterminalherstellern existiert eine Reihe standardisierter Schnittstellen,
die auch von verschiedenen Betriebssystemen zur Anbindung handelsüblicher
Kartenterminals unterstützt werden.

Die folgenden Anforderungen betreffen die gemäß
[gemSpec_Systemprozesse_dezTI#ENV_TUC_CARD_APDU_TRANSPORT] zu beschreibende
Transportschnittstelle.

**A_18166 - Vertrauliche und integritätsgeschützte Kommunikation mit KT**

Wenn der Basis-Consumer Smartcards unterstützt, MUSS der Basis-Consumer mit dem
Kartenterminal ausschließlich über eine vertrauliche, integritätsgeschützte
Verbindung kommunizieren. **[\<=]**

**A_18097 - Transportschnittstelle für Kartenkommandos**

Wenn der Basis-Consumer Smartcards unterstützt, MUSS er eine sichere
Transportschnittstelle für die Übertragung von Smartcard-APDUs gemäß
[CT-API] implementieren. **[\<=]**

**A_18100 - Ergänzende Standards für Transportschnittstelle**

Der Basis-Consumer KANN eine Transportschnittstelle für die Übertragung von
SmartCard-APDUs auf Basis des SICCT-Protokolls gemäß [CCID] und unter
Verwendung der vom Hersteller des Kartenterminals ggf. bereitgestellten
Hardwaretreiber implementieren. **[\<=]**

**A_18163 - Kartenterminal für Basis-Consumer**

Wenn der Basis-Consumer Smartcards unterstützt, MUSS er mindestens ein
Kartenterminal enthalten. **[\<=]**

**A_18102 - PIN-Eingabe nicht speichern**

Der Basis-Consumer DARF ein eingegebenes PIN-Geheimnis NICHT speichern. **[\<=]**

**A_18103 - PIN-Geheimnis ausschließlich an Karte übermitteln**

Der Basis-Consumer MUSS sicherstellen, dass das eingegebene PIN-Geheimnis
ausschließlich an die Karte und nicht an andere Adressaten übermittelt wird.
**[\<=]**

### 6.6.2 Schnittstelle für PIN-Operationen und Anbindung der Karten der TI

Anwendungsfälle zur PIN-Verwaltung, zur Kartenfreischaltung oder weiterer
Fachanwendungen können die Eingabe eines PIN- oder PUK-Geheimnisses erfordern.
Der Zugriff auf Karten der TI erfolgt über die Systemprozesse PL_TUC_CARD_*.
Der Basis-Consumer als Realisierungsumgebung der Systemprozesse muss
seinerseits die von der Plattform geforderten Schnittstellen gemäß
[gemSpec_Systemprozesse_dezTI#ENV_TUC_CARD_SECRET_INPUT] implementieren, um die
Kommunikation der Plattform mit dem Benutzer zu ermöglichen.

Die Kommunikationsschnittstelle ist in Kapitel 6.6.1 Transportschnittstelle für
Kartenkommandos beschrieben und umfasst das Kartenterminal, Eingabemedium und
Hinweistexte an den Benutzer. Diese kann je nach Konfiguration an einem Gerät
als Kartenterminal oder auch eine Kombination aus Bildschirmausgabe,
Kartenterminal-PIN-Pad und/oder Tastatureingabe erfolgen.

**A_18107 - Übergabeschnittstelle PIN/PUK-Geheimnis**

Wenn der Basis-Consumer Smartcards unterstützt, MUSS er eine Operation gemäß
[gemSpec_Systemprozesse_dezTI#ENV_TUC_CARD_SECRET_INPUT] zur Eingabe eines
PIN/PUK-Geheimnisses und Weiterleitung an eine Smartcard mit folgenden
Parametern implementieren:Eingabeparameter:

 ---> UL

Rückgabewerte

 ---> UL

**[\<=]**

**A_18108 - Umsetzung ENV_TUC_CARD_SECRET_INPUT**

Wenn der Basis-Consumer Smartcards unterstützt, MUSS er die Abbildung der
Eingabeparameter auf die Rückgabewerte der Operation ENV_TUC_SECRET_INPUT
derart umsetzen, dass

 ---> UL

und die Antwortnachricht der Karte als responseApdu an den Aufrufer zur
Auswertung zurückgegeben wird. **[\<=]**

**A_18109 - Minimalprinzip Karteninteraktion**

Der Basis-Consumer DARF ein Kartenkommando NICHT an eine angebundene Karte
weiterleiten, wenn dies nicht explizit im Kontext eines Anwendungsfalls
(intendierte Kartenoperationen und Erhöhen des Sicherheitszustands der Karte,
falls erforderlich) erforderlich ist. **[\<=]**

### 7 Anhang A - Verzeichnisse

### 7.1 Abkürzungen

Abkürzungen

<table><tr><th>
Kürzel

</th><th>
Erläuterung

</th></tr><tr><td>
AZPD 

</td><td>
Anbieter Zentrale Plattform Dienste

</td></tr><tr><td>
CMS

</td><td>
Cryptographic Message Syntax

</td></tr><tr><td>
HSM

</td><td>
Hardware Security Module

</td></tr><tr><td>
IPv4

</td><td>
Internet Protokoll Version 4

</td></tr><tr><td>
IPv6

</td><td>
Internet Protokoll Version 6

</td></tr><tr><td>
KOM-LE

</td><td>
Kommunikation für Leistungserbringer

</td></tr><tr><td>
LDAP

</td><td>
Leightweight Directory Access Protocol

</td></tr><tr><td>
MIME

</td><td>
Multipurpose Internet Mail Extensions

</td></tr><tr><td>
MTA

</td><td>
Mail Transfer Agent

</td></tr><tr><td>
POP3

</td><td>
Post Office Protocol Version 3

</td></tr><tr><td>
S/MIME

</td><td>
Secure/Multipurpose Internet Mail Extensions

</td></tr><tr><td>
SM-B

</td><td>
Security Module Typ B

</td></tr><tr><td>
SMTP

</td><td>
Simple Mail Transfer Protocol

</td></tr><tr><td>
TI

</td><td>
Telematikinfrastruktur

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

</td></tr></table>

### 7.2 Glossar

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

Das Glossar wird als eigenständiges Dokument, vgl. [gemGlossar] zur Verfügung
gestellt.

### 7.3 Abbildungsverzeichnis

- [Abbildung-1] - Systemkontext für Basis- und KTR-Consumer

### 7.4 Tabellenverzeichnis

- [Tabelle-1] - Mapping der Netzwerksegmente
- [Tabelle-2] - TAB_CONS_687 DNS-Forwards des DNS-Servers
- [Tabelle-3] -  TAB_CONS_648 – TUC_CONS_362 „Liste der Dienste abrufen“
- [Tabelle-4] -  Basisanwendung Namensdienst
- [Tabelle-5] - Konfigurationsparameter Namensdienst
- [Tabelle-6] - Einsehbare Konfigurationsparameter Namensdienst
- [Tabelle-7] - Tab_Personalisierung_HSM – Personalisierung des HSM
- [Tabelle-8] - Tab_Verschlüsselungsdienst
- [Tabelle-9] - Tab_Operation_EncryptDocument
- [Tabelle-10] - Tab_Operation_DecryptDocument
- [Tabelle-11] - Tab_KeyReference_für_Encrypt/Decrypt
- [Tabelle-12] - Tab_Signaturdienst
- [Tabelle-13] - Tab_Operation_SignDocument
- [Tabelle-14] - Tab_Zertifikate_für_Sign/VerifyDocument(nonQeS)
- [Tabelle-15] - Tab_Operation_VerifyDocument
- [Tabelle-16] - Tab_Operation_ExternalAuthenticate
- [Tabelle-17] - Tab_Zertifikatsdienst
- [Tabelle-18] - Tab_Operation_VerifyCertificate
- [Tabelle-19] - Tab_Ablauf_VerifyCertificate
- [Tabelle-20] - Tab_Übersicht_VerificationResult_VerifyCertificate
- [Tabelle-21] - Tab_Ldap_TUC_Mapping
- [Tabelle-22] - Tab_Konf_Param Standardkonfiguration
- [Tabelle-23] - Tab_SMTP_Ant_Init Antworten Clientmodul im CONNECT-Zustand
- [Tabelle-24] - Tab_SMTP_Verbindung SMTP-Antwortcodes für MTA-Verbindungsaufbau
- [Tabelle-25] - Tab_POP3_Ant_Init Antworten Clientmodul im CONNECT-Zustand
- [Tabelle-26] - Tab_POP3_Verbindung Antwortcodes für POP3-Server-Verbindungsaufbau
- [Tabelle-27] - Tab_Schema_Versionen Versionen der Schemas aus dem Namensraum des Basis- und KTR-Consumers
- [Tabelle-28] - TAB_Systemprozesse – Verwendete Plattformleistungen

### 7.5 Referenzierte Dokumente

### 7.5.1 Dokumente der gematik

Die nachfolgende Tabelle enthält die Bezeichnung der in dem vorliegenden
Dokument referenzierten Dokumente der gematik zur Telematikinfrastruktur. Der
mit der vorliegenden Version korrelierende Entwicklungsstand dieser Konzepte
und Spezifikationen wird pro Release in einer Dokumentenlandkarte definiert,
Version und Stand der referenzierten Dokumente sind daher in der nachfolgenden
Tabelle nicht aufgeführt. Deren zu diesem Dokument passende jeweils gültige
Versionsnummer sind in der aktuellsten, von der gematik veröffentlichten
Dokumentenlandkarte enthalten, in der die vorliegende Version aufgeführt wird.

<table><tr><th>
[Quelle]

</th><th>
Herausgeber: Titel

</th></tr><tr><td>
[gemGlossar]

</td><td>
gematik: Einführung der Gesundheitskarte - Glossar

</td></tr><tr><td>
[gemSMIME_KOMLE]

</td><td>
gematik: S/MIME-Profil Kommunikation Leistungserbringer(KOM-LE)

</td></tr><tr><td>
[gemSpec_CM_KOMLE]

</td><td>
gematic: Spezifikation KOM-LE-Clientmodul

</td></tr><tr><td>
[gemSpec_Systemprozesse_dezTI]

</td><td>
gematik: Spezifikation der Systemprozesse der dezentralen TI

</td></tr><tr><td>
[gemSpec_VZD]

</td><td>
gematik: Spezifikation Verzeichnisdienst

</td></tr><tr><td>
[gemKPT_Arch_TIP]

</td><td>
gematik: Konzept Architektur der TI-Plattform

</td></tr><tr><td>
[gemSpec_FM_ePA_KTR_Consumer]

</td><td>
gematik: Spezifikation Fachmodul ePA im KTR-Consumer

</td></tr><tr><td>
[gemSpec_PKI]

</td><td>
gematik: Übergreifende Spezifikation PKI

</td></tr><tr><td>
[gemSpec_Net]

</td><td>
gematik: Übergreifende Spezifikation Netzwerk

</td></tr></table>

### 7.5.2 Weitere Dokumente

<table><tr><th>
[Quelle]

</th><th>
Herausgeber (Erscheinungsdatum): Titel

</th></tr><tr><td>
[BSI-TR-03111]

</td><td>
BSI TR-31111: Elliptic Curve Cryptography, Version 2.10, Juni 2018 

</td></tr><tr><td>
[RFC1939]

</td><td>
RFC 1939: Post Office Protocol – Version 3, J. Myers, M. Rose, Mai 1996

</td></tr><tr><td>
[RFC2045]

</td><td>
RFC 2045: Multipurpose Internet Mail Extension (MIME) Part One: Format of
Internet Message Bodies, N. Freed, N. Borenstein, November 1996

</td></tr><tr><td>
[RFC2119]

</td><td>
RFC 2119 (März 1997): Key words for use in RFCs to Indicate Requirement Levels
S. Bradner

</td></tr><tr><td>
[RFC4511]

</td><td>
RFC 4511: Lightweight Directory Access Protocol (LDAP), J. Sermersheim, Juni
2006

</td></tr><tr><td>
[RFC4954]

</td><td>
RFC 4954: SMTP Service Extension for Authentication, R. Siemborski, A. Melnikov,
März 2007

</td></tr><tr><td>
[RFC5083]

</td><td>
RFC 5083: Authenticated-Enveloped-Data Content Type, R.Housley, November 2007

</td></tr><tr><td>
[RFC5321]

</td><td>
RFC 5321: Simple Mail Transfer Protocol, J. Klensin, Oktober 2008

</td></tr><tr><td>
[RFC5652]

</td><td>
RFC 5652: Cryptographic Message Syntax (CMS), R. Housley, September 2009

</td></tr><tr><td>
[RFC5751]

</td><td>
RFC 5751: Secure/Multipurpose Internet Mail Extensions (S/MIME) Version 3.2
Message Specification, B. Ramsdell, S. Turner, Januar 2010

</td></tr><tr><td>
[RFC1812]

</td><td>
RFC 1812: Requirements for IP Version 4 Routers, Juni 1995

</td></tr><tr><td>
[RFC2644]

</td><td>
RFC 2644: Changing the Default for Directed Broadcasts in Routers, August 1999

</td></tr><tr><td>
[RFC791]

</td><td>
RFC 791: Internet Protocol, September 1981

</td></tr><tr><td>
[RFC3022]

</td><td>
RFC 3022: Traditional IP Network Address Translator (Traditional NAT), Januar
2001

</td></tr><tr><td>
[RFC1918]

</td><td>
RFC 1918: Address Allocation for Private Internets, Februar 1996

</td></tr><tr><td>
[RFC6598]

</td><td>
RFC 6598: IANA-Reserved IPv4 Prefix for Shared Address Spac, April 2012

</td></tr><tr><td>
[OASIS-DSS]

</td><td>
OASIS: Digital Signature Service Core Protocols, Elements, and Bindings, Version
1.0, OASIS Standard, via
http://docs.oasis-open.org/dss/v1.0/oasis-dss-core-spec-v1.0-os.pdf

</td></tr><tr><td>
[OASIS-SP]

</td><td>
OASIS: Signature Policy Profile of the OASIS Digital Signature Services Version
1.0, Committee Draft 01, 18 May 2009,
http://docs.oasis-open.org/dss-x/profiles/sigpolicy/oasis-dssx-1.0-profiles-sigpolicy-cd01.pdf

</td></tr><tr><td>
[OASIS-VR]

</td><td>
OASIS: Profile for comprehensive multi-signature verification reports for OASIS
Digital Signature Services Version 1.0, Committee Specification 01, 12 November
2010,
http://docs.oasis-open.org/dss-x/profiles/verificationreport/oasis-dssx-1.0-profiles-vr-cs01.pdf

</td></tr><tr><td>
[XMLEnc]

</td><td>
XML Encryption Syntax and Processing  
W3C Recommendation 11 April 2013 

http://www.w3.org/TR/xmlenc-core1/

</td></tr><tr><td>
[XPATH]

</td><td>
W3C Recommendation (14 December 2010)  
XML Path Language (XPath) 2.0 (Second
Edition)  
http://www.w3.org/TR/2010/REC-xpath20-20101214/

</td></tr><tr><td>
[CMS]

</td><td>
Cryptographic Message Syntax (CMS), September 2009 

http://tools.ietf.org/html/rfc5652

</td></tr><tr><td>
[Canon XML1.1]

</td><td>
Canonical XML Version 1.1  
http://www.w3.org/TR/2008/REC-xml-c14n11-20080502/

</td></tr><tr><td>
[CAdES]

</td><td>
ETSI: Electronic Signature Formats, Electronic Signatures and Infrastructures
(ESI) – Technical Specification, ETSI TS 101 733 V2.2.1, 2008-07, via
http://www.etsi.org 

</td></tr><tr><td>
[CT-API]

</td><td>
https://www.tuvit.de/de/aktuelles/beitraege-white-paper/card-terminal-application-programing-interface-fuer-chipkartenanwendungen// 

</td></tr><tr><td>
[CCID]

</td><td>
https://usb.org.10-1-108-210.causewaynow.com/sites/default/files/DWG_Smart-Card_CCID_Rev110.pdf 

</td></tr></table>

### 8 Anhang B – Übersicht über die verwendeten Versionen

Für den Fall, dass Schnittstellenversionen unterstützt werden müssen, die den
gleichen TargetNamespace nutzen, kann der Basis- und KTR-Consumer zu diesen
Schnittstellenversionen einheitlich einen SOAP-Endpunkt anbieten, der die
höchste der Schnittstellenversionen implementiert.

<table><tr><th colspan="3">
Schemas aus dem Namensraum des Basis- und KTR-Consumer
„http://ws.gematik.de/consumer“

</th></tr><tr><td>
Name

</td><td>
Version

</td><td>
TargetNamespace

</td></tr><tr><td>
CertificateService.wsdl

</td><td>
2.0.0

</td><td>
http://ws.gematik.de/consumer/CertificateService/WSDL/v2.0  

</td></tr><tr><td>
CertificateService.xsd

</td><td>
2.0.0

</td><td>
http://ws.gematik.de/consumer/CertificateService/v2.0 

</td></tr><tr><td>
CertificateServiceCommon.xsd

</td><td>
1.0.0

</td><td>
http://ws.gematik.de/consumer/CertificateServiceCommon/v1.0 

</td></tr><tr><td>
ConsumerCommon.xsd

</td><td>
2.0.0

</td><td>
http://ws.gematik.de/consumer/ConsumerCommon/v2.0 

</td></tr><tr><td>
EncryptionService.wsdl

</td><td>
2.0.0

</td><td>
http://ws.gematik.de/consumer/EncryptionService/WSDL/v2.0 

</td></tr><tr><td>
EncryptionService.xsd

</td><td>
2.0.0

</td><td>
http://ws.gematik.de/consumer/EncryptionServiceCommon/v2.0 

</td></tr><tr><td>
SignatureService.wsdl

</td><td>
2.0.0

</td><td>
http://ws.gematik.de/consumer/SignatureService/WSDL/v2.0 

</td></tr><tr><td>
SignatureService.xsd

</td><td>
2.0.0

</td><td>
http://ws.gematik.de/consumer/SignatureServiceCommon/v2.0 

</td></tr></table>

### 9 Anhang C – Übersicht der genutzten Systemprozesse

Der Basis- und KTR-Consumer verwendet u.a. die in Tabelle TAB_Systemprozesse
dargestellten Plattformleistungen aus [gemSpec_Systemprozesse_dezTI].

<table><tr><th>
Kürzel

</th><th>
Bezeichnung

</th></tr><tr><td>
PL_TUC_HYBRID_DECIPHER

</td><td>
Hybrid entschlüsseln

</td></tr><tr><td>
PL_TUC_HYBRID_ENCIPHER

</td><td>
Hybrid verschlüsseln

</td></tr><tr><td>
PL_TUC_SIGN_DOCUMENT_nonQES

</td><td>
Dokument nonQES signieren

</td></tr><tr><td>
PL_TUC_SIGN_HASH_nonQES

</td><td>
mit Karten-Identität signieren

</td></tr><tr><td>
PL_TUC_VERIFY_DOCUMENT_nonQES

</td><td>
nonQES Dokumentensignatur verifizieren

</td></tr><tr><td>
PL_TUC_PKI_VERIFY_CERTIFICATE

</td><td>
Prüfung eines Zertifikats der TI

</td></tr><tr><td>
PL_TUC_VZD_BIND

</td><td>
Verbindung aufbauen

</td></tr><tr><td>
PL_TUC_VZD_UNBIND

</td><td>
Verbindung trennen

</td></tr><tr><td>
PL_TUC_VZD_SEARCH

</td><td>
Verzeichnis abfragen

</td></tr><tr><td>
PL_TUC_VZD_ABANDON

</td><td>
Verzeichnisabfrage abbrechen

</td></tr><tr><td>
PL_TUC_NET_SYNC_TIME

</td><td>
Zeit synchronisieren

</td></tr><tr><td>
PL_TUC_CARD_INFORMATION

</td><td>
gesammelte Statusinformationen zu einer Karte

</td></tr><tr><td>
PL_TUC_CARD_RESET

</td><td>
Rücksetzen einer Karte

</td></tr><tr><td>
PL_TUC_CARD_CHANGE_PIN

</td><td>
PIN ändern

</td></tr><tr><td>
PL_TUC_CARD_ENABLE_PIN

</td><td>
PIN-Schutz einschalten

</td></tr><tr><td>
PL_TUC_CARD_DISABLE_PIN

</td><td>
PIN-Schutz abschalten

</td></tr><tr><td>
PL_TUC_CARD_VERIFY_PIN

</td><td>
Benutzer verifizieren

</td></tr><tr><td>
PL_TUC_CARD_ACTIVATE_APPLICATION

</td><td>
Anwendung aktivieren

</td></tr><tr><td>
PL_TUC_CARD_DEACTIVATE_APPLICATION

</td><td>
Anwendung deaktivieren

</td></tr><tr><td>
PL_TUC_CARD_GET_CHALLENGE

</td><td>
Auslesen einer Zufallszahl

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
[3]:                     #3-systemkontext
[4]:                     #4-zerlegung-der-produkttypen
[4.1]:                   #41-basisfunktionen
[4.2]:                   #42-ldap-proxy
[4.3]:                   #43-clientmodul-kom-le
[5]:                     #5-übergreifende-festlegungen
[5.1]:                   #51-anschluss-an-die-ti
[5.1.1]:                 #511-anbindung-per-lanwan
[5.1.1.1]:               #5111-funktionsmerkmalweite-aspekte
[5.1.1.1.1]:             #51111-netzwerksegmentierung
[5.1.1.2]:               #5112-durch-ereignisse-ausgelöste-reaktionen
[5.1.2]:                 #512-zeitdienst
[5.1.3]:                 #513-namensdienst-und-dienstlokalisierung
[5.1.3.1]:               #5131-funktionsmerkmalweite-aspekte
[5.1.3.2]:               #5132-interne-tucs-auch-durch-fachmodule-nutzbar
[5.1.3.2.1]:             #51321-tuc_con_362-liste-der-dienste-abrufen
[5.1.3.3]:               #5133-operationen-an-der-außenschnittstelle
[5.1.3.4]:               #5134-betriebsaspekte
[5.2]:                   #52-sicherheit
[5.3]:                   #53-identitäten
[5.4]:                   #54-schnittstellen
[6]:                     #6-funktionsmerkmale
[6.1]:                   #61-verschlüsselungsdienst
[6.1.1]:                 #611-durch-module-nutzbare-tucs
[6.1.2]:                 #612-operationen-an-der-clientschnittstelle
[6.1.2.1]:               #6121-encryptdocument
[6.1.2.2]:               #6122-decryptdocument
[6.2]:                   #62-signaturdienst
[6.2.1]:                 #621-durch-module-nutzbare-tucs
[6.2.2]:                 #622-operationen-an-der-clientschnittstelle
[6.2.2.1]:               #6221-signdocument
[6.2.2.2]:               #6222-verifydocument
[6.2.2.3]:               #6223-externalauthenticate
[6.3]:                   #63-zertifikatsdienst
[6.3.1]:                 #631-durch-module-nutzbare-tucs
[6.3.2]:                 #632-operationen-an-der-clientschnittstelle
[6.3.2.1]:               #6321-verifycertificate
[6.4]:                   #64-ldap-proxy
[6.4.1]:                 #641-durch-module-nutzbare-tucs
[6.4.2]:                 #642-unterstützte-ldapv3-operationen-an-der-clientschnittstelle
[6.5]:                   #65-clientmodul-kom-le
[6.5.1]:                 #651-allgemeine-anforderungen
[6.5.2]:                 #652-senden-von-nachrichten
[6.5.3]:                 #653-empfangen-von-nachrichten
[6.6]:                   #66-realisierung-der-leistungen-der-ti-plattform
[6.6.1]:                 #661-transportschnittstelle-für-kartenkommandos
[6.6.2]:                 #662-schnittstelle-für-pin-operationen-und-anbindung-der-karten-der-ti
[7]:                     #7-anhang-a---verzeichnisse
[7.1]:                   #71-abkürzungen
[7.2]:                   #72-glossar
[7.3]:                   #73-abbildungsverzeichnis
[7.4]:                   #74-tabellenverzeichnis
[7.5]:                   #75-referenzierte-dokumente
[7.5.1]:                 #751-dokumente-der-gematik
[7.5.2]:                 #752-weitere-dokumente
[8]:                     #8-anhang-b-–-übersicht-über-die-verwendeten-versionen
[9]:                     #9-anhang-c-–-übersicht-der-genutzten-systemprozesse
[Abbildung-1]:           gemSpec_Basis_KTR_Consumer_V1.5.0.attachments/18445073441336388534.png
[Img-002]:               gemSpec_Basis_KTR_Consumer_V1.5.0.attachments/16621404060534927350.png
[Img-003]:               gemSpec_Basis_KTR_Consumer_V1.5.0.attachments/10905502372898110443.png
[Img-004]:               gemSpec_Basis_KTR_Consumer_V1.5.0.attachments/9211249275986351283.png
[Img-005]:               gemSpec_Basis_KTR_Consumer_V1.5.0.attachments/13305078831658311783.png
[Img-006]:               gemSpec_Basis_KTR_Consumer_V1.5.0.attachments/17668465197856016356.png
[Img-007]:               gemSpec_Basis_KTR_Consumer_V1.5.0.attachments/3110557969022182157.png
[Img-008]:               gemSpec_Basis_KTR_Consumer_V1.5.0.attachments/240588376863411668.png
[Img-009]:               gemSpec_Basis_KTR_Consumer_V1.5.0.attachments/10485345170604926526.png
[Img-010]:               gemSpec_Basis_KTR_Consumer_V1.5.0.attachments/497428918559136001.png
[Img-011]:               gemSpec_Basis_KTR_Consumer_V1.5.0.attachments/654340862499539967.png
[Img-012]:               gemSpec_Basis_KTR_Consumer_V1.5.0.attachments/5591054957365209502.png
[Img-013]:               gemSpec_Basis_KTR_Consumer_V1.5.0.attachments/16418325756727644132.png
[Img-014]:               gemSpec_Basis_KTR_Consumer_V1.5.0.attachments/8747151615322488883.png
[Img-015]:               gemSpec_Basis_KTR_Consumer_V1.5.0.attachments/7212896267878518057.png
[Img-016]:               gemSpec_Basis_KTR_Consumer_V1.5.0.attachments/13883905178538230263.png
[Img-017]:               gemSpec_Basis_KTR_Consumer_V1.5.0.attachments/6350483296715844335.png
[Img-018]:               gemSpec_Basis_KTR_Consumer_V1.5.0.attachments/6428807695314848769.png
[Img-019]:               gemSpec_Basis_KTR_Consumer_V1.5.0.attachments/12587326460955289142.png
[Img-020]:               gemSpec_Basis_KTR_Consumer_V1.5.0.attachments/12981934522493971086.png
[Img-021]:               gemSpec_Basis_KTR_Consumer_V1.5.0.attachments/10821174516087157775.png
[Img-022]:               gemSpec_Basis_KTR_Consumer_V1.5.0.attachments/11624870121609237196.png
[Img-023]:               gemSpec_Basis_KTR_Consumer_V1.5.0.attachments/16099814150706486231.png
[Img-024]:               gemSpec_Basis_KTR_Consumer_V1.5.0.attachments/8614804184070861435.png
[Tbl-001]:               #Tbl-001 (&93834775876760)
[Tabelle-1]:             #Tabelle-1 (&93834783636920)
[Tabelle-2]:             #Tabelle-2 (&93834781723856)
[Tabelle-3]:             #Tabelle-3 (&93834768010344)
[Tabelle-4]:             #Tabelle-4 (&93834768041872)
[Tabelle-5]:             #Tabelle-5 (&93834772261608)
[Tabelle-6]:             #Tabelle-6 (&93834772276944)
[Tabelle-7]:             #Tabelle-7 (&93834764476816)
[Tabelle-8]:             #Tabelle-8 (&93834781755848)
[Tabelle-9]:             #Tabelle-9 (&93834781791088)
[Tabelle-10]:            #Tabelle-10 (&93834783789288)
[Tabelle-11]:            #Tabelle-11 (&93834783835960)
[Tabelle-12]:            #Tabelle-12 (&93834785396624)
[Tabelle-13]:            #Tabelle-13 (&93834785433008)
[Tabelle-14]:            #Tabelle-14 (&93834785776672)
[Tabelle-15]:            #Tabelle-15 (&93834785802368)
[Tabelle-16]:            #Tabelle-16 (&93834764277392)
[Tabelle-17]:            #Tabelle-17 (&93834781389616)
[Tabelle-18]:            #Tabelle-18 (&93834781422688)
[Tabelle-19]:            #Tabelle-19 (&93834776842512)
[Tabelle-20]:            #Tabelle-20 (&93834776874672)
[Tabelle-21]:            #Tabelle-21 (&93834776893088)
[Tabelle-22]:            #Tabelle-22 (&93834776922048)
[Tabelle-23]:            #Tabelle-23 (&93834777043736)
[Tabelle-24]:            #Tabelle-24 (&93834768110528)
[Tabelle-25]:            #Tabelle-25 (&93834768141488)
[Tabelle-26]:            #Tabelle-26 (&93834768167144)
[Tbl-028]:               #Tbl-028 (&93834768232944)
[Tbl-029]:               #Tbl-029 (&93834768331632)
[Tbl-030]:               #Tbl-030 (&93834768369464)
[Tbl-031]:               #Tbl-031 (&93834764550152)
[Tabelle-27]:            #Tabelle-27 (&93834764641152)
[Tabelle-28]:            #Tabelle-28 (&93834764692792)
