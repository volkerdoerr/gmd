
Elektronische Gesundheitskarte und Telematikinfrastruktur

### Spezifikation<br>Verzeichnisdienst FHIR-Directory

- Klassifizierung: öffentlich
- Referenzierung: gemSpec_VZD_FHIR_Directory
- Revision: 557497
- Stand: 29.07.2022
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
1.0.0 

</td><td>
01.10.2021

</td><td>
Erstversion des Dokumentes  

</td><td>
gematik

</td></tr><tr><td>
1.1.0

</td><td>
29.07.2022

</td><td>
Fortschreibung und insbesondere Anpassungen gemäß TI-Messenger-Spezifikation
Version 1.1.0

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
  - [2.1] Nutzer und Rollen
  - [2.2] Nachbarsysteme
- [3] Zerlegung des Produkttyps
- [4] Funktionsmerkmale
  - [4.1] FHIR-Directory
    - [4.1.1] Datenmodell
    - [4.1.2] Mapping von LDAP auf FHIR-Ressourcen
    - [4.1.3] FHIR RESTful API
  - [4.2] FHIR-Proxy
    - [4.2.1] Schnittstellen
      - [4.2.1.1] TLS-Verbindungsaufbau
      - [4.2.1.2] FHIR Schnittstelle für TI-Messenger-Nutzer
      - [4.2.1.3] FHIR-Schnittstelle für Besitzer
      - [4.2.1.4] Schnittstelle I_VZD_TIM_Provider_Services
    - [4.2.2] Aktualisierung der Basiseinträge
    - [4.2.3] Erzeugung und Bereitstellung der Föderationsliste
    - [4.2.4] Lokalisierung einer MXID (Operation whereIs)
  - [4.3] Übergreifende Vorgaben
    - [4.3.1] Sicherheit
    - [4.3.2] Betrieb
- [5] Anwendungsfälle
  - [5.1] TI-Messenger-Nutzer sucht Einträge im FHIR-Directory
  - [5.2] Eigentümer ändert seinen Eintrag im FHIR-Directory
  - [5.3] Anwendungsfälle der TI-Messenger-Anbieter im VZD-FHIR-Directory
  - [5.4] Einträge mit dem VZD-LDAP-Directory abgleichen
- [6] Verteilungssicht
- [7] Anhang A – Verzeichnisse
  - [7.1] Abkürzungen
  - [7.2] Glossar
  - [7.3] Abbildungsverzeichnis
  - [7.4] Tabellenverzeichnis
  - [7.5] Referenzierte Dokumente
    - [7.5.1] Dokumente der gematik
    - [7.5.2] Weitere Dokumente
  - [7.6] Versionierung Datenmodell
- [8] Anhang B - Beispiele
  - [8.1] FHIR Operationen
    - [8.1.1] Abfrage von OrganizationDirectory Einträgen
      - [8.1.1.1] Client Code
      - [8.1.1.2] Request
      - [8.1.1.3] Request Headers
      - [8.1.1.4] Response
      - [8.1.1.5] Response Headers
      - [8.1.1.6] Response Body

### 1 Einordnung des Dokumentes

Dieses Dokument beschreibt das FHIR-Directory des Verzeichnisdienstes der TI.
Die Spezifikation umfasst Schnittstellen zum Abruf von Informationen der im
FHIR-Directory eingetragenen Organization-FHIR-Ressourcen und der
Practitioner-FHIR-Ressourcen durch Clientsysteme sowie Schnittstellen und
Prozesse zur Pflege der Informationen innerhalb des VZD-FHIR-Directories.

### 1.1 Zielsetzung

Die Spezifikation soll die Entwicklung und den Betrieb eines
VZD-FHIR-Directories für die Telematikinfrastruktur unterstützen, indem die
funktionalen und nicht-funktionalen Anforderungen sowie die
Sicherheits-Anforderungen an den Dienst festgelegt werden. 

### 1.2 Zielgruppe

Das Dokument richtet sich zwecks der Realisierung an den Hersteller des
VZD-FHIR-Directories sowie an den Anbieter, welcher dieses Produkt betreibt
[gemKPT_Betr]. Alle Hersteller und Anbieter von TI-Anwendungen, die das
VZD-FHIR-Directory nutzen,  müssen dieses Dokument ebenso berücksichtigen.
Gleichfalls ist das Dokument auch für die Nutzer relevant welche die Daten im
VZD-FHIR-Directory eintragen, abfragen, ändern und löschen wollen.

### 1.3 Geltungsbereich

Dieses Dokument enthält normative Festlegungen zur Telematikinfrastruktur des
deutschen Gesundheitswesens. Der Gültigkeitszeitraum der vorliegenden Version
und deren Anwendung in Zulassungs- oder Abnahmeverfahren wird durch die gematik
GmbH in gesonderten Dokumenten (z. B. gemPTV_ATV_Festlegungen,
Produkttypsteckbrief, Anbietertypsteckbrief, u.a.) oder Webplattformen (z.B.
gitHub, u.a.) festgelegt und bekanntgegeben.

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

Spezifiziert werden in dem Dokument nur die mit dem VZD-FHIR-Directory neu
eingeführten Komponenten und Schnittstellen des Verzeichnisdienstes der
TI. Das VZD-LDAP-Directory ist in [gemSpec_VZD] spezifiziert. 

Benutzte Schnittstellen werden in der Spezifikation desjenigen Produkttypen
beschrieben, der diese Schnittstelle bereitstellt. Auf die entsprechenden
Dokumente wird referenziert (siehe auch Anhang, Kapitel ).

Die vollständige Anforderungslage für den Produkttyp ergibt sich aus weiteren
Konzept- und Spezifikationsdokumenten, diese sind in dem Produkttypsteckbrief
des Produkttyps VZD-FHIR-Directory verzeichnet.

### 1.5 Methodik

Die Spezifikation ist im Stil einer RFC-Spezifikation verfasst. Dies bedeutet: 

 ---> UL

Anwendungsfälle und Akzeptanzkriterien als Ausdruck normativer Festlegungen
werden als Grundlage für Erlangung der Zulassung durch Tests geprüft und
nachgewiesen. Sie besitzen eine eindeutige, permanente ID, welche als Referenz
verwendet werden SOLL. Die Tests werden gegen eine von der gematik gestellte
Referenz-Implementierung durchgeführt. 

Anwendungsfälle und Akzeptanzkriterien werden im Dokument wie folgt
dargestellt:\<ID\> - \<Titel des Anwendungsfalles / Akzeptanzkriteriums\>Text /
Beschreibung [\<=]

Die einzelnen Elemente beschreiben:

 ---> UL

Dabei umfasst der Anwendungsfall bzw. das Akzeptanzkriterium sämtliche zwischen
ID und Textmarke [\<=] angeführten Inhalte.

Der für die Erlangung einer Zulassung notwendige  Nachweis der Erfüllung des
Anwendungsfalls wird in den jeweiligen  Steckbriefen festgelegt, in denen
jeweils der Anwendungsfall gelistet ist. Akzeptanzkriterien werden in der Regel
nicht im Steckbrief gelistet.

Hinweis auf offene Punkte

<table><tr><td>
Offener Punkt: Das Kapitel wird in einer späteren Version des Dokumentes
ergänzt.

</td></tr></table>

### 2 Systemüberblick

Das VZD-FHIR-Directory ist eine Erweiterung des bisherigen Verzeichnisdienstes
der TI. Im VZD-FHIR-Directory werden Einträge von Organisationen und
Leistungserbringern gespeichert. Die  VZD-LDAP-Directory Einträge werden in
das VZD-FHIR-Verzeichnis synchronisiert. Bei diesem Vorgang erfolgt eine
Umsetzung von der LDAP-Datenstruktur auf die Datenstruktur der FHIR-Ressourcen.
Personeneinträge der Leistungserbringer werden auf die
PractitionerDirectory-Ressource und Organisations-Einträge auf die
OrganizationDirectory-Ressource abgebildet. Die synchronisierten Einträge
bilden die Basis-Einträge, die durch die Besitzer um zusätzliche Daten
ergänzt bzw. erweitert werden können. PractitionerDirectory und
TIOrganization sind Profilierungen der FHIR-Ressourcen Practitioner und
Organization. Die Anbieter von Fachanwendungen werden ebenfalls als
TIOrganization-Einträge im FHIR-Directory eingetragen um Daten der
Fachanwendung zu dieser Organisation zuordnen zu können.

Der Besitzer einer Telematik-ID erhält das Recht seinen Eintrag zu erweitern
(um z. B. Unterstrukturen für eine Organisation einzutragen) und Fachdaten zu
ergänzen (z. B. TI-Messenger-Adressen). Die von den Kartenherausgebern
eingetragenen Daten dürfen durch die Besitzer nicht verändert
werden. Zusätzliche FHIR-Ressourcen (wie z. B. Location und
HealthcareService) können durch die Besitzer ergänzt werden, um den Komfort
bei der Suche nach Einträgen zu erhöhen.

Alle vom VZD-FHIR-Directory bereitgestellten Schnittstellen sind über das
Internet erreichbar und TLS-gesichert. Die Authentisierung erfolgt mit:

 ---> UL

Eine Nutzung der Schnittstellen des VZD-FHIR-Directory ohne Authentisierung der
Nutzer MUSS durch das VZD-FHIR-Directory verhindert werden.

Als erste Anwendung wird der TI-Messenger-Dienst das VZD-FHIR-Directory nutzen.

![Abbildung-1][Abbildung-1]

Das FHIR-Directory ist eine Implementierung der FHIR-Spezifikation
(http://hl7.org/fhir/summary.html ).

### 2.1 Nutzer und Rollen

<table><tr><th>
Nutzer und Rolle

</th><th>
Beschreibung

</th></tr><tr><td>
Nutzer

</td><td>
Alle Nutzer können im FHIR-Directory über die Schnittstelle (1) nach
Einträgen im Organisationsverzeichnis und im Personenverzeichnis suchen.

 

</td></tr><tr><td>
Org-Admin oder LE

</td><td>
Administratoren der Organisationen und LE können im FHIR-Directory über die
Schnittstelle (2) ihren Eintrag im Organisationsverzeichnis ändern und um
zusätzliche Ressourcen erweitern.

</td></tr></table>

<table><tr><th>
IT-Systeme

</th><th>
Beschreibung

</th></tr><tr><td>
Kartenherausgeber

</td><td>
Die Kartenherausgeber nutzen die Schnittstelle (3) um die Einträge ihrer
Mitglieder im LDAP-Directory und zukünftig im FHIR-Directory zu pflegen.

</td></tr><tr><td>
TI-Messenger-Anbieter

</td><td>
Die TI-Messenger-Anbieter nutzen die Schnittstelle (4) um die Föderationsliste
des TI-Messengers abzufragen und um die Domains der von ihnen betriebenen
Messenger-Services als Teil der TI-Messenger Föderation zu verwalten.

</td></tr><tr><td>
gematik

</td><td>
Die gematik kann über die Schnittstelle (5) lesend auf die Einträge im
FHIR-Directory und im LDAP-Directory zugreifen um die Daten-Qualität der
Einträge zu prüfen und um Fehler zu analysieren.

</td></tr><tr><td>
LDAP-Directory

</td><td>
Die Schnittstelle (6) zwischen FHIR-Directory und LDAP-Directory wird vom
Verzeichnisdienst genutzt, um die Einträge zu synchronisieren.

</td></tr></table>

Alle Schnittstellen mit Ausnahme (6) sind über das Internet erreichbar. Die
Schnittstellen stellen folgende Funktionen bereit:

 ---> OL

### 2.2 Nachbarsysteme

Die Nachbarsysteme des VZD-FHIR-Directory sind Client- und Serverkomponenten des
TI-Messenger-Dienstes, das VZD-LDAP-Directory, die IDPs aus der
TI-IDP-Föderation und die Betriebsdatenerfassung der gematik. 

**ML-123876 - Test gegen die Referenzimplementierung der Nachbarsysteme
(VZD-FHIR-Directory)**

Es MÜSSEN alle Anwendungsfälle des VZD-FHIR-Directories erfolgreich gegen die
Referenzimplementierung der Nachbarsysteme getestet sein. **[\<=]**

### 3 Zerlegung des Produkttyps

Die folgende Abbildung zeigt die Teilkomponenten des bisherigen
VZD-LDAP-Directory und die rot dargestellten neuen Komponenten des
VZD-FHIR-Directory.

![Abbildung-2][Abbildung-2]

Das VZD-FHIR-Directory besteht aus den Komponenten FHIR-Proxy und FHIR-Directory
sowie Auth-Service.

Die vom VZD-FHIR-Directory zu liefernden Rohdaten zur Ermittlung der Auslastung
und Performance werden in den bereits vorhandenen
Betriebsdaten-Erfassungs-Client (BDE-Client) des Verzeichnisdienstes integriert.

### 4 Funktionsmerkmale

In diesem Kapitel werden die Komponenten des VZD-FHIR-Directories beschrieben.

### 4.1 FHIR-Directory

Das FHIR-Directory ist eine Implementierung der HL7-FHIR-Spezifikation Release
4.0.1 (https://www.hl7.org/fhir/http.html ).

Das FHIR-Directory ist nur über den FHIR-Proxy erreichbar.

### 4.1.1 Datenmodell

Es werden die FHIR-Ressourcen nach folgender Tabelle verwendet.

Alle Änderungen und Erweiterungen der FHIR Ressourcen sind
in https://simplifier.net/vzd-fhir-directory veröffentlicht.

<table><tr><th>
FHIR-Ressource

</th><th>
Beschreibung

</th></tr><tr><td>
Organization in gematik Directory

 (

OrganizationDirectory)

</td><td>
Profil der Organization Ressource.

(

https://simplifier.net/vzd-fhir-directory/organizationdirectory

)

Das Element Identifier wurde so geändert, dass Telematik-IDs als Identifier
verwendet werden können.

Im Element type wird der Typ der Organisation eingetragen. Dafür werden die
CodeSysteme 

https://simplifier.net/vzd-fhir-directory/organizationprofessionoid

   und 

https://simplifier.net/vzd-fhir-directory/practitionerprofessionoid

  sowie das ValueSet 

https://simplifier.net/vzd-fhir-directory/organizationtypevs

  verwendet.

Wenn das Element type den Wert "TI-Messenger-Provider" hat, dann handelt es sich
um eine Organisation, die einen TI-Messenger-Dienst innerhalb der
Telematikinfrastruktur bereitstellt. In endpoint-Referenzen der Organisation
werden die Domainnamen der TI-Messenger-Service-Instanzen eingetragen. Dazu
wird im Elem

ent connectionType d

as Codesystem

https://simplifier.net/vzd-fhir-directory/endpointconnectiontype

   mit

  verwendet. Im Element "name" wird der TI-Messenger Domainname eingetragen.
In "managingOrganization" wird die OrganizationDirectory eingetragen, für die
die TI-Messenger-Domain eingerichtet wurde.

</td></tr><tr><td>
Practitioner in gematik Directory (PractitionerDirectory)

</td><td>
Profil der Practitioner Ressource. Lediglich das Element Identifier wurde so
geändert, dass Telematik-IDs als Identifier verwendet werden können. (

https://simplifier.net/vzd-fhir-directory/practitionerdirectory

)

</td></tr><tr><td>
Endpoint in gematik Directory

 (

EndpointDirectory)

</td><td>
Endpoint Ressource (

https://simplifier.net/vzd-fhir-directory/endpointdirectory

)

</td></tr><tr><td>
Location in gematik Directory

 (

LocationDirectory)

</td><td>
Location (

https://simplifier.net/vzd-fhir-directory/locationdirectory

)

</td></tr><tr><td>
HealthcareService in gematik Directory

 (

HealthcareServiceDirectory

)

</td><td>
HealthcareService (

https://simplifier.net/vzd-fhir-directory/healthcareservicedirectory

)

</td></tr><tr><td>
PractitionerRole in gematik Directory (PractitionerRoleDirectory)

</td><td>
PractitionerRole (

https://simplifier.net/vzd-fhir-directory/practitionerroledirectory

)

</td></tr></table>

**ML-123880 - Einschränkung der nutzbaren FHIR-Ressourcen (VZD-FHIR-Directory)**

Nur die in Tabelle "VZD-FHIR-Directory, FHIR-Ressourcen" angegebenen Ressourcen
dürfen im VZD-FHIR-Directory erzeugt werden. **[\<=]**

### 4.1.2 Mapping von LDAP auf FHIR-Ressourcen

Die OrganizationDirectory- und PractitionerDirectory-Basiseinträge werden durch
den FHIR Proxy mit den Daten aus dem VZD-LDAP-Directory initial erzeugt und
anschließend fortlaufend aktualisiert. Die synchronisierten Daten können
nicht durch die Besitzer (Leistungserbringer und Organisationen) geändert
werden.

Die Daten aus dem VZD-LDAP-Directory werden wie folgt den FHIR-Ressourcen
zugeordnet: https://github.com/gematik/api-vzd/blob/master/docs/LDAP2FHIR_Sync.adoc 

### 4.1.3 FHIR RESTful API

Die Operationen der FHIR-Schnittstelle sind durch die FHIR-Spezifikation
festgelegt (https://www.hl7.org/fhir/http.html ).

Die Anzahl der mittels /search Operation gefundenen und zurückgegebenen
Einträge wird initial auf 100 begrenzt. Dieser Wert MUSS konfigurierbar
sein. Die zurückgegebenen Einträge werden in einem FHIR-Ressource-Bundle
zusammengefasst. Im Attribut Bundle.total MUSS die Gesamtanzahl der gefundenen
Einträge (total number of matches) zurück gegeben werden. 

Zusätzlich MUSS konfigurierbar sein, ob Paging eingesetzt wird und wie groß
die page_size ist. Paging ist initial eingeschaltet mit page_size = 10. Wenn
eine Suche mehr Treffer enthält, als in page_size angegeben, dann enthält die
Response ein bundle mit den gefundenen Einträgen gemäß page_size und einen
Link auf die nächste page.

### 4.2 FHIR-Proxy

### 4.2.1 Schnittstellen

### 4.2.1.1 TLS-Verbindungsaufbau

Der FHIR-Proxy MUSS sich beim TLS-Verbindungsaufbau an den Endpunkten gegenüber
Clients mit einem Extended Validation TLS-Zertifikat eines Herausgebers gemäß
[CAB-Forum] authentisieren. Das Zertifikat MUSS an die Schnittstelle des
Eingangspunkts für Clientsysteme gebunden werden, damit Clientsysteme beim
TLS-Verbindungsaufbau eine vereinfachte Zertifikatsprüfung mit
TLS-Standardbibliotheken durchführen können.

### 4.2.1.2 FHIR Schnittstelle für TI-Messenger-Nutzer

Endpunkte für die Suche von Einträgen im VZD-FHIR-Directory durch
TI-Messenger-Clients

In der Produktionsumgebung ist die
URL: https://fhir-directory.vzd.ti-dienste.de/search   

In der Referenzumgebung ist die
URL:https://fhir-directory-ref.vzd.ti-dienste.de/search  

In der Testumgebung ist die
URL: https://fhir-directory-test.vzd.ti-dienste.de/search 

Authentisierung

Um die Schnittstelle nutzen zu können MÜSSEN sich die Clients mit einem
gültigen Token authentisieren, das von einem Matrix-Homeserver aus der
TI-Messenger-Föderation ausgestellt wurde. Im Folgenden werden diese
AccesstokenMatrix-OpenID-Token genannt. Nach erfolgreicher Prüfung
des Matrix-OpenID-Token stellt der FHIR-Proxy dem TI-Messenger-Client ein
neues OAuth Accesstoken aus (tim-accesstoken), dass für Suchanfragen
des TI-Messenger-Clients verwendet wird. Die Gültigkeitsdauer ist 24 Stunden.

Das Accesstoken enthält folgende Attribute:

<table><tr><td>
{  
  "iss": "https://fhir-directory.vzd.ti-dienste.de/tim-authenticate",  
 
"aud": [ "https://fhir-directory.vzd.ti-dienste.de/search" ],  
  "iat":
1630306800,  
  "exp": 1630393200  
}

</td></tr></table>

Das Attribut "iss" enthält die URL des Endpunktes für die Authentisierung in
der jeweiligen Umgebung RU, TU oder PU.

Das Attribut "aud" enthält die URL des Endpunktes in der jeweiligen Umgebung
RU, TU oder PU.

Endpunkte für die Authentisierung

In der Produktionsumgebung ist die
URL: https://fhir-directory.vzd.ti-dienste.de/tim-authenticate   

In der Referenzumgebung ist die
URL: https://fhir-directory-ref.vzd.ti-dienste.de/tim-authenticate 

In der Testumgebung ist die
URL: https://fhir-directory-test.vzd.ti-dienste.de/tim-authenticate  

Operationen

Die FHIROperationen für die Suche nach Einträgen im VZD-FHIR-Directory sind
in der HL7 FHIR Spezifikation (https://www.hl7.org/fhir/http.html ) festgelegt.

### 4.2.1.3 FHIR-Schnittstelle für Besitzer

Die Schnittstelle ermöglicht es den Besitzern einer Telematik-ID, ihren Eintrag
im VZD-FHIR-Directory zu ändern. Im bei der Authentifizierung verwendeten
Accesstoken ist die Telematik-ID des Nutzers enthalten. Nur der Eintrag
(PractitionerDirectory oder OrganizationDirectory)mit der eigenen
Telematik-ID darf verändert werden. Dabei dürfen nur die Attribute
verändert werden, die nicht vom VZD-LDAP-Directory synchronisiert werden.

Endpunkte für das Ändern von eigenen Einträgen im VZD-FHIR-Directory durch
TI-Messenger Clients und Org-Admin-Clients

In der Produktionsumgebung ist die
URL: https://fhir-directory.vzd.ti-dienste.de/owner  

In der Referenzumgebung ist die
URL: https://fhir-directory-ref.vzd.ti-dienste.de/owner 

In der Testumgebung ist die
URL: https://fhir-directory-test.vzd.ti-dienste.de/owner   

Authentisierung

Um die Schnittstelle nutzen zu können, MÜSSEN sich die Clients mit einem
gültigen Accesstoken authentisieren, das vom FHIR-Proxy ausgestellt wurde.
Wenn kein gültiges Accesstoken im Client vorhanden ist, dann muss sich der
Client an einem IDP der TI-IDP-Föderation authentisieren.

Nur der eigene Eintrag mit einem Identifier passend zur Telematik-ID aus dem
Accesstoken KANN bearbeitet werden. Für einen eigenen
OrganizationDirectory-Eintrag KÖNNEN weitere OrganizationDirectory-Einträge
erstellt und mit dem eigenen Eintrag verlinkt werden.

Das Accesstoken enthält folgende Attribute:

<table><tr><td>
{  
  "iss": "https://vzd-fhir-directory.vzd.ti-dienste.de/owner-authenticate",
 
  "sub": "\<telematikID\>",  
  "aud": [
"https://vzd-fhir-directory.vzd.ti-dienste.de/owner" ],  
  "iat": 1630306800,
 
  "exp": 1630393200  
}

</td></tr></table>

Das Attribut "iss" enthält die URL des Endpunktes für die Authentisierung in
der jeweiligen Umgebung RU, TU oder PU.

Das Attribut "aud" enthält die URL des Endpunktes in der jeweiligen Umgebung
RU, TU oder PU.

Endpunkte für die Authentisierung

In der Produktionsumgebung ist die
URL: https://fhir-directory.vzd.ti-dienste.de/owner-authenticate  

In der Referenzumgebung ist die
URL: https://vzd-fhir-directory-ref.vzd.ti-dienste.de/owner-authenticate   

In der Testumgebung ist die
URL: https://vzd-fhir-directory-test.vzd.ti-dienste.de/owner-authenticate  

Operationen

Die FHIR-Operationen für das Ändern von eigenen Einträgen im
VZD-FHIR-Directory sind in der HL7-FHIR-Spezifikation
(https://www.hl7.org/fhir/http.html ) festgelegt.

### 4.2.1.4 Schnittstelle I_VZD_TIM_Provider_Services

Endpunkte

In der Produktionsumgebung ist die
URL: https://fhir-directory.vzd.ti-dienste.de/tim-provider-services 

In der Referenzumgebung ist die
URL: https://fhir-directory-ref.vzd.ti-dienste.de/tim-provider-services 

In der Testumgebung ist die
URL: https://fhir-directory-test.vzd.ti-dienste.de/tim-provider-services 

Authentisierung

Um die Schnittstelle nutzen zu können muss sich der Registrierungsdienst des
TI-Messenger-Anbieters mit einem Accesstoken authentisieren, das vom
OAuth-Server des VZD-Anbieters ausgestellt wurde. Das Accesstoken hat eine
Gültigkeitsdauer von 30 Minuten.

Das Accesstoken enthält folgende Attribute:

<table><tr><td>
{  
  "iss": "https://oauth.vzd.ti-dienste.de/authenticate",  
  "sub":
"\<client_id\>",  
  "aud": [
"https://vzd-fhir-directory.vzd.ti-dienste.de/tim-provider-services" ],  
 
"iat": 1630306800,  
  "exp":

1630308600

,  
  "scope": "tim-provider-services"  
}

</td></tr></table>

Das Attribut "iss" enthält die URL des Endpunktes für die Authentisierung in
der jeweiligen Umgebung RU, TU oder PU.

Das Attribut "aud" enthält die URL des Endpunktes in der jeweiligen Umgebung
RU, TU oder PU.

Endpunkte für die Authentisierung

In der Produktionsumgebung ist die
URL: https://oauth.vzd.ti-dienste.de/authenticate   

In der Referenzumgebung ist die
URL: https://ru-oauth-test.vzd.ti-dienste.de/authenticate 

In der Testumgebung ist die
URL: https://tu-oauth-test.vzd.ti-dienste.de/authenticate 

Registrierung

Für den Zugriff auf den OAuth-Server MUSS der TI-Messenger-Anbieter für seinen
Registrierungsdienst beim VZD-Anbieter Client-Credentials beantragen. Die
Beantragung erfolgt über einen genehmigungspflichtigen Service-Request im
TI-ITSM-System.

Die Registrierung und Vergabe der Credentials erfolgt dabei auf Anbieterebene.

Der Antrag MUSS folgende Informationen enthalten um weiter bearbeitet werden zu
können:

 ---> UL

Nach Prüfung der Angaben, werden die Zugangsdaten direkt vom Anbieter Zentrale
Plattformdienste (vgl. gemKPT_Betr) an die gewünschte E-Mail-Adresse
übermittelt.

Es ist zu beachten, dass dieser Prozess ausschließlich für Neuanlagen und
Löschungen vorgesehen ist. Änderungen oder der Neuversand von Zugangsdaten
können nicht bearbeitet werden.

Operationen

Die Schnittstelle ist in I_VZD_TIM_Provider_Services.yaml als OpenAPI RESTful
Service spezifiziert.

https://github.com/gematik/api-vzd/blob/main/src/openapi/I_VZD_TIM_Provider_Services.yaml 

<table><tr><th>
Operation

</th><th>
Beschreibung

</th></tr><tr><td>
GET /

"

getInfo"

</td><td>
Mit dieser Operation können Metadaten (insbesondere auch die Version und das
verwendete yaml-File) dieser Schnittstelle abgefragt werden.

</td></tr><tr><td>
GET 

/FederationList/federationList.json

</td><td>
Mit dieser Operation wird die Liste der an der TI-Messenger-Föderation
beteiligten Matrix-Domainnamen abgefragt (Föderationsliste). 

</td></tr><tr><td>
GET 

/localization  
"whereIs"

</td><td>
Gibt für den übergebenen Hash einer MXID den Teil des Directories zurück, in
dem die MXID enthalten ist.

</td></tr><tr><td>
POST /federation

"addTiMessengerDomain"

</td><td>
Eine Domaine zur Föderation hinzufügen.

</td></tr><tr><td>
GET /federation

"getTiMessengerDomain"

</td><td>
Lesen einer oder aller eigener Domains.

</td></tr><tr><td>
PUT /federation

"updateTiMessengerDomain"

</td><td>
Aktualisierung einer Domaine.

</td></tr><tr><td>
DELETE /federation

"deleteTiMessengerDomain"

</td><td>
Löschen einer Domaine.

</td></tr><tr><td>
GET /federationCheck

"checkTiMessengerDomains"

</td><td>
Prüft, ob alle eigenen Domains (durch Token ermittelbar) zu aktiven
Organisationen gehören. Gibt die eigenen Domains zurück, die zu inaktiven
Organisationen gehören.

</td></tr></table>

Im Attribut "sub" des Accesstoken ist die client_id des
TI-Messenger-Registrierungsdienstes enthalten. Wenn der
TI-Messenger-Registrierungsdienst einen OrganizationDirectory-Eintrag erzeugt,
dann MUSS die client_id im Element alias des Eintrags enthalten sein

### 4.2.2 Aktualisierung der Basiseinträge

Der FHIR-Proxy aktualisiert regelmäßig die Basiseinträge im
VZD-FHIR-Directory mit den geänderten Daten des VZD-LDAP-Directories (siehe
AF_10047 Einträge mit dem VZD-LDAP-Directory abgleichen). Das Intervall für
die regelmäßige Aktualisierung MUSS konfigurierbar sein und wird initial auf
2 Stunden festgelegt. 

Es MUSS (analog dem Background-Sync-Verfahren in die LDAP flache Liste) eine
weitere Synchronisation mittels PUSH in den FHIR VZD möglich sein.

Zukünftig ist vorgesehen, dass Kartenherausgeber direkt die Basiseinträge
ihrer Mitglieder im VZD-FHIR-Directory über eine FHIR-Schnittstelle verwalten
können.

### 4.2.3 Erzeugung und Bereitstellung der Föderationsliste

Die Föderationsliste MUSS bei Änderung der Domains durch TI-Messenger-Anbieter
oder regelmäßig (7 Tage vor Ablauf der Gültigkeit) neu erzeugt und zum
Download über die Schnittstelle I_VZD_TIM_Provider_Services bereitgestellt
werden.

Die Föderationsliste hat folgende Struktur:

<table><tr><td>
{

  "iat": \<Unix Timestamp, Zeitpunkt der Erzeugung == Beginn der Gültigkeit\>,

  "exp": \<Unix Timestamp, Beginn der Gültigkeit + 30 Tage\>,

  "hashAlgorithm": "sha256",

  "domainList": [

    {

      "domain": "hash der Domain",

      "isInsurance": false

    }

  ]

}

</td></tr></table>

Die Föderationsliste MUSS mit einer JWS gemäß RFC7515 signiert werden. Der zu
verwendende Signatur-Algorithmus MUSS "ES256" sein. Dazu MUSS ein
Signatur-Zertifikat der Komponenten-PKI der TI (C.FD.SIG) verwendet werden. Das
Signatur-Zertifikat und das ausstellende CA-Zertifikat MÜSSEN im
Signatur-Header enthalten sein.

Der Signatur-Header hat folgende Struktur:

<table><tr><td>
{

  "alg": "ES256",

  "x5c": [

    "\<X.509 Sig-Cert, base64-encoded DER\>",

    "\<X.509 CA-Cert, base64-encoded DER\>"

  ]

}

</td></tr></table>

Die signierte Föderationsliste hat gemäß RFC7515 folgende Struktur:

<table><tr><td>
{

  "payload": "\<Föderationsliste, BASE64URL\>",

  "signatures": [

    {

      "header":\<Signatur-Header\>,

      "signature":"\<signature, BASE64URL\>"

    }

  ]

}

</td></tr></table>

**ML-123677 - Maßnahmen gegen die Manipulation der Föderationsliste
(VZD-FHIR-Directory, Sicherheitsgutachten)**

Im Sicherheitsgutachten des VZD-FHIR-Directories sind geeignete Maßnahmen gegen
die Manipulation der Föderationsliste beschrieben. **[\<=]**

### 4.2.4 Lokalisierung einer MXID (Operation whereIs)

Der FHIR-Proxy MUSS die Lokalisierung einer MXID über Operation whereIs
performant bereitstellen. Dazu MUSS der FHIR-Proxy bei jeder Änderung an den
Endpoint-Einträgen (der MXID darin) die benötigten Daten für die
performante Antwort der whereIs Operation aktualisieren. Der FHIR-Proxy DARF
NICHT die originalen FHIR-Daten für die Ausführung der whereIs Operation
durchsuchen.

### 4.3 Übergreifende Vorgaben

### 4.3.1 Sicherheit

Schutz vor Sicherheits-Risiken

Das VZD-FHIR-Directory MUSS Maßnahmen zum Schutz vor Sicherheits-Risiken
gemäß der aktuellen Version der OWASP-Top-10 umsetzen
(https://owasp.org/www-project-top-ten/ ).

Es gelten die Anforderungen an TLS-Verbindungen gemäß [gemSpec_Krypt#3.3.2]
TLS-Verbindungen.

**ML-123682 - Maßnahmen zum Schutz vor Sicherheits-Risiken (VZD-FHIR-Directory,
Sicherheitsgutachten)**

Im Sicherheitsgutachten des VZD-FHIR-Directories sind geeignete Maßnahmen zum
Schutz vor Sicherheits-Risiken gemäß der aktuellen Version der OWASP-Top-10
beschrieben. **[\<=]**

### 4.3.2 Betrieb

Das VZD-FHIR-Directory wird betrieblich als eine weitere Servicekomponente im
Sinne der Weiterentwicklung des Verzeichnisdienstes betrachtet. Diese
Servicekomponente kann, bis auf die Schnittstellen, unabhängig vom
VZD-LDAP-Directory entwickelt und deployt werden. Aus Nutzersicht ist weniger
die interne, logische Struktur der Verzeichnisdienste relevant, sondern die
Verfügbarkeit der Schnittstellen und die im Verzeichnis enthaltenen Daten.

Das VZD-FHIR-Directory MUSS die Bearbeitungszeitvorgaben unter Last aus
Tab_VZD_FHIR_Perf unter der für alle Funktionen parallel anliegenden
Spitzenlast erfüllen.

<table><tr><th>
Schnittstellenoperation

</th><th>
Lastvorgaben

Spitzenlast

[1/sec]

</th><th>
Bearbeitungszeitvorgaben

Mittelwert

[msec]

</th><th>
Bearbeitungszeitvorgaben

99%-Quantil

[msec]

</th></tr><tr><td>
FHIR Schnittstelle für TI-Messenger-Nutzer (/search)

</td><td>
1000

</td><td>
1000

</td><td>
1250

</td></tr><tr><td>
FHIR-Schnittstelle für Besitzer (/owner)

</td><td>
20

</td><td>
1000

</td><td>
1250

</td></tr><tr><td>
Schnittstelle I_VZD_TIM_Provider_Services (/tim-provider-services)

</td></tr><tr><td>
   - getFederationList

</td><td>
1

</td><td>
1000

</td><td>
1250

</td></tr><tr><td>
   - whereIs

</td><td>
50

</td><td>
1000

</td><td>
1250

</td></tr><tr><td>
   - addTiMessengerDomain

</td><td>
1

</td><td>
1000

</td><td>
1250

</td></tr><tr><td>
   - getTiMessengerDomain

</td><td>
1

</td><td>
1000

</td><td>
1250

</td></tr><tr><td>
   - updateTiMessengerDomain

</td><td>
1

</td><td>
1000

</td><td>
1250

</td></tr><tr><td>
   - deleteTiMessengerDomain

</td><td>
1

</td><td>
1000

</td><td>
1250

</td></tr><tr><td>
   - checkTiMessengerDomains

</td><td>
1

</td><td>
1000

</td><td>
1250

</td></tr></table>

### 5 Anwendungsfälle

### 5.1 TI-Messenger-Nutzer sucht Einträge im FHIR-Directory

**AF_10036 - Nutzer sucht Einträge im FHIR-Directory**

![Abbildung-3][Abbildung-3]

Abbildung3: Sequence diagram /search **[\<=]**

Akzeptanzkriterien für den Anwendungsfall AF_10036 Nutzer sucht
OrganizationDirectory- und PractitionerDirectory-Einträge im VZD-FHIR-Directory

**ML-123485 - Authentifizierung am Endpunkt /search (VZD-FHIR-Directory,
Sicherheitsgutachten)**

Am Endpunkt /search des FHIR-Proxy darf die Authentifizierung nur für Requests
erfolgreich sein, die ein gültiges search-accesstoken im Authentication Header
enthalten, dass vom Auth-Service ausgestellt wurde. **[\<=]**

### 5.2 Eigentümer ändert seinen Eintrag im FHIR-Directory

**AF_10037 - Einträge im VZD-FHIR-Directory ändern**

![Img-004][Img-004]

Abbildung4: Sequenzdiagramm VZD-FHIR-Directory Änderung von eigenen
OrganizationDirectory- oder PractitionerDirectory-Einträgen **[\<=]**

Akzeptanzkriterien für den Anwendungsfall
AF_10037 OrganizationDirectory-Einträge im VZD-FHIR-Directory ändern

**ML-123873 - Authentifizierung am Endpunkt /owner (VZD-FHIR-Directory,
Sicherheitsgutachten)**

Am Endpunkt /owner des FHIR-Proxy darf die Authentifizierung nur für Nutzer
erfolgreich sein, die ein gültiges Accesstoken vom VZD-FHIR-Directory
vorweisen. **[\<=]**

**ML-123874 - Nur Einträge mit eigener Telematik-ID verändern
(VZD-FHIR-Directory)**

Im, bei der Authentifizierung verwendeten, Accesstoken ist die Telematik-ID des
Nutzers enthalten. Nur der Eintrag (PractitionerDirectory oder
OrganizationDirectory)mit der eigenen Telematik-ID darf verändert
werden.Dabei dürfen nur die Attribute verändert werden, die nicht vom
VZD-LDAP-Directory synchronisiert werden. **[\<=]**

**ML-123482 - Selbst angelegte OrganizationDirectory-Einträge MÜSSEN mit dem
eigenen Basiseintrag verlinkt sein (VZD-FHIR-Directory)**

Alle selbst durch den Besitzer angelegten FHIR-Einträge MÜSSEN mit dem eigenen
Basiseintrag mittels partOf verlinkt sein. Wenn keine korrekte Verlinkung
angegeben ist, dann MUSS der FHIR-Proxy das Erzeugen oder die Änderung des
OrganizationDirectory-Eintrags mit der Fehlermeldung (HTTP 422 Unprocessable
Entity) ablehnen. **[\<=]**

### 5.3 Anwendungsfälle der TI-Messenger-Anbieter im VZD-FHIR-Directory

**AF_10048 - Anwendungsfälle der TI-Messenger-Anbieter im VZD-FHIR-Directory**

![Abbildung-5][Abbildung-5]

Abbildung5: VZD-FHIR-Directory_Sequenzdiagramm_TI-Messenger-Provider-Services **[\<=]**

**ML-123881 - Authentifizierung an der Schnittstelle I_VZD_TIM_Provider_Services
(VZD-FHIR-Directory, Sicherheitsgutachten)**

An der Schnittstelle I_VZD_TIM_Provider_Services darf die Authentifizierung nur
für Clients erfolgreich sein, die ein gültiges provider-accesstoken vom
OAuth-Server des VZD-Anbieters vorweisen. **[\<=]**

### 5.4 Einträge mit dem VZD-LDAP-Directory abgleichen

**AF_10047 - Einträge mit dem VZD-LDAP-Directory abgleichen**

![Img-006][Img-006]

Abbildung6: VZD-FHIR-Directory, Aktualisierung der Basiseinträge **[\<=]**

### 6 Verteilungssicht

Das VZD-FHIR-Directory unterstützt initial die Anwendung TI-Messenger; wird
zukünftig aber auch die anderen Anwendungen wie ePA und KIM in deren
Folgeversionen sowie bisher unbekannte Fachanwendungen und neue Nutzergruppen
unterstützen. Es ist daher erforderlich, dass das VZD-FHIR-Directory mit der
Anzahl der Nutzerzugriffe skalieren und anwendungsspezifische Ressourcen
speichern kann.

Der FHIR-Proxy MUSS in mehreren Instanzen betrieben werden können, die die
Schnittstellen Richtung Internet für Abfragen der TI-Messenger-Nutzer und
Änderungen durch die Besitzer implementieren. Das Load-Balancing der
Client-Requests erfolgt per DNS, indem für jede Instanz des FHIR-Proxy ein A
und ein AAAA Resource Record für die RU, TU und PU FQDNs der Schnittstellen im
DNS eingetragen wird. Instanzen des FHIR-Proxies werden je nach Last
hinzugefügt oder entfernt.

Die FHIR-Proxy sind auch die HTTP-Load-Balancer für die Lesezugriffe auf
FHIR-Directory-Instanzen. Für den Schreibzugriff wird eine Instanz
implementiert. Die Datenbanken der Instanzen für den Lesezugriff werden mit
der Datenbank für den Schreibzugriff synchronisiert.

Eine weitere Komponente setzt die Aktualisierung der Basiseinträge im
FHIR-Directory mit den geänderten Daten aus dem VZD-LDAP-Directory um.
Zusätzlich implementiert diese Komponente die
Schnittstelle I_VZD_TIM_Provider_Services.

![Abbildung-7][Abbildung-7]

### 7 Anhang A – Verzeichnisse

### 7.1 Abkürzungen

<table><tr><th>
Kürzel

</th><th>
Erläuterung

</th></tr><tr><td>
AF

</td><td>
Anwendungsfall

</td></tr><tr><td>
DNS

</td><td>
Domain Name System

</td></tr><tr><td>
FHIR

</td><td>
Fast Healthcare Interoperable Resources

</td></tr><tr><td>
FQDN

</td><td>
Fully Qualified Domain Name

</td></tr><tr><td>
LDAP

</td><td>
Lightweight Directory Access Protocol

</td></tr><tr><td>
OWASP

</td><td>
Open Web Application Security Project

</td></tr><tr><td>
PU

</td><td>
Produktivumgebung

</td></tr><tr><td>
RU

</td><td>
Referenzumgebung

</td></tr><tr><td>
SHA

</td><td>
Secure Hash Algorithm

</td></tr><tr><td>
TLS

</td><td>
Transport Layer Security

</td></tr><tr><td>
TI

</td><td>
Telematikinfrastruktur

</td></tr><tr><td>
TIM

</td><td>
TI-Messenger (ausschließliche Verwendung der Abkürzung in Attributen,
Parametern oder URLs)

</td></tr><tr><td>
TU

</td><td>
Testumgebung

</td></tr><tr><td>
VZD

</td><td>
Verzeichnisdienst

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

</td></tr><tr></tr></table>

Das Glossar wird als eigenständiges Dokument (vgl. [gemGlossar]) zur Verfügung
gestellt.

### 7.3 Abbildungsverzeichnis

- [Abbildung-1] - Systemüberblick VZD-FHIR-Directory
- [Abbildung-2] - Zerlegung des VZD
- [Abbildung-3] -  Sequence diagram /search
- [Abbildung-5] -  VZD-FHIR-Directory_Sequenzdiagramm_TI-Messenger-Provider-Services
- [Abbildung-7] - VZD-FHIR-Directory, Verteilungssicht  

### 7.4 Tabellenverzeichnis

- [Tabelle-1] - Nutzer und Rollen 
- [Tabelle-2] - Kommunikationsbeziehungen zu IT-Systemen
- [Tabelle-3] - VZD-FHIR-Directory, FHIR-Ressourcen
- [Tabelle -4] - Tab_VZD_TIM-Provider-Services_Operations
- [Tabelle -5] - Tab_VZD_FHIR_Perf

### 7.5 Referenzierte Dokumente

### 7.5.1 Dokumente der gematik

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
gematik: Einführung der Gesundheitskarte – Glossar

</td></tr><tr><td>
[gemSpec_VZD]

</td><td>
g

ematik: Spezifikation Verzeichnisdienst

</td></tr><tr><td>
[gemSpec_Krypt]

</td><td>
gematik: Übergreifende Spezifikation Verwendung kryptographischer Algorithmen
in der Telematikinfrastruktur

</td></tr><tr><td>
[gemKPT_Betr]

</td><td>
gematik: Betriebskonzept Online-Produktivbetrieb

</td></tr></table>

### 7.5.2 Weitere Dokumente

<table><tr><th>
[Quelle]

</th><th>
Herausgeber (Erscheinungsdatum): Titel

</th></tr><tr><td>
[CAB-Forum]

</td><td>
Liste vertrauenswürdiger Zertifikatsherausgeber (Root-CAs) für Anwendungen im
Internet

https://cabforum.org/members/

</td></tr></table>

### 7.6 Versionierung Datenmodell

Folgende Versionen der Datenmodell Ressourcen
(https://simplifier.net/vzd-fhir-directory/ ) sind für die vorliegende
Spezifikation relevant:

 ---> UL

### 8 Anhang B - Beispiele

### 8.1 FHIR Operationen

### 8.1.1 Abfrage von OrganizationDirectory Einträgen

### 8.1.1.1 Client Code

// Create a client (only needed once)FhirContext ctx = new
FhirContext();IGenericClient client =
ctx.newRestfulGenericClient("http://hapi.fhir.org/baseR4");// Invoke the
clientBundle bundle =
client.search().forResource(HealthcareService.class).where(new
StringClientParam("location.address").matches().value("10117"))  
.include(new
Include("Organization"))  
.prettyPrint()  
.execute();

### 8.1.1.2 Request

GET http://hapi.fhir.org/baseR4/HealthcareService?location.address=10117&_include=Organization&_pretty=true 

### 8.1.1.3 Request Headers

Accept-Charset: utf-8  
Accept: application/fhir+xml;q=1.0,
application/fhir+json;q=1.0, application/xml+fhir;q=0.9,
application/json+fhir;q=0.9  
User-Agent: HAPI-FHIR/5.5.0-PRE1-SNAPSHOT (FHIR
Client; FHIR 4.0.1/R4; apache)  
Accept-Encoding: gzip

### 8.1.1.4 Response

HTTP 200 OK

### 8.1.1.5 Response Headers

x-request-id: hr3p6Pi0jorUblN7  
date: Fri, 06 Aug 2021 10:22:24 GMT 

last-modified: Fri, 06 Aug 2021 10:22:23 GMT  
server: nginx/1.18.0 (Ubuntu)
 
transfer-encoding: chunked  
x-powered-by: HAPI FHIR
5.5.0-PRE1-SNAPSHOT/1703568840/2021-05-28 REST Server (FHIR Server; FHIR
4.0.1/R4)  
connection: keep-alive 

content-type: application/fhir+json;charset=utf-8

### 8.1.1.6 Response Body

{  
  "resourceType": "Bundle",  
  "id":
"ec8a4846-5719-4760-833f-606f01ea6055",  
  "meta": {  
    "lastUpdated":
"2021-08-06T06:56:44.620+00:00"  
  },  
  "type": "searchset",  
  "total":
2,  
  "link": [ {  
    "relation": "self",  
    "url":
"http://hapi.fhir.org/baseR4/TIOrganization?_include=TIOrganization%3Aendpoint 

&_pretty=true&address=10117"  
  } ],  
  "entry": [ {  
    "fullUrl":
"http://hapi.fhir.org/baseR4/TIOrganization/2500949",  
    "resource": { 

      "resourceType": "TIOrganization",  
      "id": "2500949",  
   
  "meta": {  
        "versionId": "1",  
        "lastUpdated":
"2021-08-04T15:51:20.261+00:00",  
        "source": "#0j3wXiC80VNH7wON" 

      },  
      "name": "Test Organisation der TI",  
     
"telecom": [ {  
        "system": "url",  
        "value":
"matrix:u/testorg:gematik.de"  
      } ],  
      "address": [ {  
   
    "line": [ "Friedrichstr. 136" ],  
        "city": "Berlin",  
   
    "state": "Berlin",  
        "postalCode": "10117",  
       
"country": "Germany"  
      } ]  
    },  
    "search": {  
     
"mode": "match"  
    }  
  }, {  
    "fullUrl":
"http://hapi.fhir.org/baseR4/TIOrganization/2500973",  
    "resource": { 

      "resourceType": "TIOrganization",  
      "id": "2500973",  
   
  "meta": {  
        "versionId": "1",  
        "lastUpdated":
"2021-08-04T16:55:16.931+00:00",  
        "source": "#q5G1swl1SHzfbbjj" 

      },  
      "name": "Test Organisation 2 der TI",  
     
"telecom": [ {  
        "system": "url",  
        "value":
"matrix:u/testorg2:gematik.de"  
      } ],  
      "address": [ {  
 
      "line": [ "Friedrichstr. 136" ],  
        "city": "Berlin",  
 
      "state": "Berlin",  
        "postalCode": "10117",  
       
"country": "Germany"  
      } ],  
      "endpoint": [ {  
       
"reference": "Endpoint/2500968"  
      } ]  
    },  
    "search": { 

      "mode": "match"  
    }  
  }, {  
    "fullUrl":
"http://hapi.fhir.org/baseR4/Endpoint/2500968",  
    "resource": {  
   
  "resourceType": "Endpoint",  
      "id": "2500968",  
      "meta": {
 
        "versionId": "1",  
        "lastUpdated":
"2021-08-04T16:27:54.228+00:00",  
        "source": "#bsfK2WXBApjsoYj8" 

      },  
      "connectionType": {  
        "system":
"https://gematik.de/fhir/VZD-FHIR-Directory/CodeSystem/TIMessengerCS",  
   
    "code": "tim-domain"  
      },  
      "name": "gematik.de",  
 
    "managingOrganization": {  
        "reference":
"TIOrganization/2500949"  
      }  
    },  
    "search": {  
     
"mode": "include"  
    }  
  } ]  
}





[Dokumentinformationen]: #dokumentinformationen
[Inhaltsverzeichnis]:    #inhaltsverzeichnis
[1]:                     #1-einordnung-des-dokumentes
[1.1]:                   #11-zielsetzung
[1.2]:                   #12-zielgruppe
[1.3]:                   #13-geltungsbereich
[1.4]:                   #14-abgrenzungen
[1.5]:                   #15-methodik
[2]:                     #2-systemüberblick
[2.1]:                   #21-nutzer-und-rollen
[2.2]:                   #22-nachbarsysteme
[3]:                     #3-zerlegung-des-produkttyps
[4]:                     #4-funktionsmerkmale
[4.1]:                   #41-fhir-directory
[4.1.1]:                 #411-datenmodell
[4.1.2]:                 #412-mapping-von-ldap-auf-fhir-ressourcen
[4.1.3]:                 #413-fhir-restful-api
[4.2]:                   #42-fhir-proxy
[4.2.1]:                 #421-schnittstellen
[4.2.1.1]:               #4211-tls-verbindungsaufbau
[4.2.1.2]:               #4212-fhir-schnittstelle-für-ti-messenger-nutzer
[4.2.1.3]:               #4213-fhir-schnittstelle-für-besitzer
[4.2.1.4]:               #4214-schnittstelle-i_vzd_tim_provider_services
[4.2.2]:                 #422-aktualisierung-der-basiseinträge
[4.2.3]:                 #423-erzeugung-und-bereitstellung-der-föderationsliste
[4.2.4]:                 #424-lokalisierung-einer-mxid-operation-whereis
[4.3]:                   #43-übergreifende-vorgaben
[4.3.1]:                 #431-sicherheit
[4.3.2]:                 #432-betrieb
[5]:                     #5-anwendungsfälle
[5.1]:                   #51-ti-messenger-nutzer-sucht-einträge-im-fhir-directory
[5.2]:                   #52-eigentümer-ändert-seinen-eintrag-im-fhir-directory
[5.3]:                   #53-anwendungsfälle-der-ti-messenger-anbieter-im-vzd-fhir-directory
[5.4]:                   #54-einträge-mit-dem-vzd-ldap-directory-abgleichen
[6]:                     #6-verteilungssicht
[7]:                     #7-anhang-a-–-verzeichnisse
[7.1]:                   #71-abkürzungen
[7.2]:                   #72-glossar
[7.3]:                   #73-abbildungsverzeichnis
[7.4]:                   #74-tabellenverzeichnis
[7.5]:                   #75-referenzierte-dokumente
[7.5.1]:                 #751-dokumente-der-gematik
[7.5.2]:                 #752-weitere-dokumente
[7.6]:                   #76-versionierung-datenmodell
[8]:                     #8-anhang-b---beispiele
[8.1]:                   #81-fhir-operationen
[8.1.1]:                 #811-abfrage-von-organizationdirectory-einträgen
[8.1.1.1]:               #8111-client-code
[8.1.1.2]:               #8112-request
[8.1.1.3]:               #8113-request-headers
[8.1.1.4]:               #8114-response
[8.1.1.5]:               #8115-response-headers
[8.1.1.6]:               #8116-response-body
[Abbildung-1]:           gemSpec_VZD_FHIR_Directory_V1.1.0.attachments/3487542842298011336.png
[Abbildung-2]:           gemSpec_VZD_FHIR_Directory_V1.1.0.attachments/11283030060405967466.png
[Abbildung-3]:           gemSpec_VZD_FHIR_Directory_V1.1.0.attachments/14243104084904649518.png
[Img-004]:               gemSpec_VZD_FHIR_Directory_V1.1.0.attachments/4338925173979829955.png
[Abbildung-5]:           gemSpec_VZD_FHIR_Directory_V1.1.0.attachments/3593576910348582271.png
[Img-006]:               gemSpec_VZD_FHIR_Directory_V1.1.0.attachments/11705194599738530532.png
[Abbildung-7]:           gemSpec_VZD_FHIR_Directory_V1.1.0.attachments/6867044630018266293.png
[Tbl-001]:               #Tbl-001 (&93834775696304)
[Tbl-002]:               #Tbl-002 (&93834808903608)
[Tabelle-1]:             #Tabelle-1 (&93834801627888)
[Tabelle-2]:             #Tabelle-2 (&93834801637544)
[Tabelle-3]:             #Tabelle-3 (&93834764165664)
[Tbl-006]:               #Tbl-006 (&93834799914240)
[Tbl-007]:               #Tbl-007 (&93834771060600)
[Tbl-008]:               #Tbl-008 (&93834810794672)
[Tabelle -4]:            #Tabelle -4 (&93834810831672)
[Tbl-010]:               #Tbl-010 (&93834770985488)
[Tbl-011]:               #Tbl-011 (&93834770992608)
[Tbl-012]:               #Tbl-012 (&93834770997912)
[Tabelle -5]:            #Tabelle -5 (&93834771020072)
[Tbl-014]:               #Tbl-014 (&93834775084856)
[Tbl-015]:               #Tbl-015 (&93834775112280)
[Tbl-016]:               #Tbl-016 (&93834775137104)
[Tbl-017]:               #Tbl-017 (&93834783645568)
[http://hl7.org/fhir/summary.html]: http://hl7.org/fhir/summary.html (&93834801623656)
[https://www.hl7.org/fhir/http.html]: https://www.hl7.org/fhir/http.html (&93834764159688)
[https://simplifier.net/vzd-fhir-directory]: https://simplifier.net/vzd-fhir-directory (&93834764163040)
[https://simplifier.net/vzd-fhir-directory/organizationdirectory]: https://simplifier.net/vzd-fhir-directory/organizationdirectory (&93834764171072)
[https://simplifier.net/vzd-fhir-directory/organizationprofessionoid]: https://simplifier.net/vzd-fhir-directory/organizationprofessionoid (&93834764172632)
[https://simplifier.net/vzd-fhir-directory/practitionerprofessionoid]: https://simplifier.net/vzd-fhir-directory/practitionerprofessionoid (&93834764173584)
[https://simplifier.net/vzd-fhir-directory/organizationtypevs]: https://simplifier.net/vzd-fhir-directory/organizationtypevs (&93834764174536)
[https://simplifier.net/vzd-fhir-directory/endpointconnectiontype]: https://simplifier.net/vzd-fhir-directory/endpointconnectiontype (&93834764176576)
[https://simplifier.net/vzd-fhir-directory/practitionerdirectory]: https://simplifier.net/vzd-fhir-directory/practitionerdirectory (&93834799836576)
[https://simplifier.net/vzd-fhir-directory/endpointdirectory]: https://simplifier.net/vzd-fhir-directory/endpointdirectory (&93834799840112)
[https://simplifier.net/vzd-fhir-directory/locationdirectory]: https://simplifier.net/vzd-fhir-directory/locationdirectory (&93834799843648)
[https://simplifier.net/vzd-fhir-directory/healthcareservicedirectory]: https://simplifier.net/vzd-fhir-directory/healthcareservicedirectory (&93834799847304)
[https://simplifier.net/vzd-fhir-directory/practitionerroledirectory]: https://simplifier.net/vzd-fhir-directory/practitionerroledirectory (&93834799850240)
[https://github.com/gematik/api-vzd/blob/master/docs/LDAP2FHIR_Sync.adoc]: https://github.com/gematik/api-vzd/blob/master/docs/LDAP2FHIR_Sync.adoc (&93834799855768)
[https://www.hl7.org/fhir/http.html]: https://www.hl7.org/fhir/http.html (&93834799857920)
[https://fhir-directory.vzd.ti-dienste.de/search]: https://fhir-directory.vzd.ti-dienste.de/search (&93834799907304)
[https://fhir-directory-ref.vzd.ti-dienste.de/search]: https://fhir-directory-ref.vzd.ti-dienste.de/search (&93834799908856)
[https://fhir-directory-test.vzd.ti-dienste.de/search]: https://fhir-directory-test.vzd.ti-dienste.de/search (&93834799910408)
[https://fhir-directory.vzd.ti-dienste.de/tim-authenticate]: https://fhir-directory.vzd.ti-dienste.de/tim-authenticate (&93834799930040)
[https://fhir-directory-ref.vzd.ti-dienste.de/tim-authenticate]: https://fhir-directory-ref.vzd.ti-dienste.de/tim-authenticate (&93834799931592)
[https://fhir-directory-test.vzd.ti-dienste.de/tim-authenticate]: https://fhir-directory-test.vzd.ti-dienste.de/tim-authenticate (&93834799933144)
[https://fhir-directory.vzd.ti-dienste.de/owner]: https://fhir-directory.vzd.ti-dienste.de/owner (&93834771053664)
[https://fhir-directory-ref.vzd.ti-dienste.de/owner]: https://fhir-directory-ref.vzd.ti-dienste.de/owner (&93834771055216)
[https://fhir-directory-test.vzd.ti-dienste.de/owner ]: https://fhir-directory-test.vzd.ti-dienste.de/owner%A0 (&93834771056768)
[https://fhir-directory.vzd.ti-dienste.de/owner-authenticate]: https://fhir-directory.vzd.ti-dienste.de/owner-authenticate (&93834771077424)
[https://vzd-fhir-directory-ref.vzd.ti-dienste.de/owner-authenticate ]: https://vzd-fhir-directory-ref.vzd.ti-dienste.de/owner-authenticate%A0 (&93834771078976)
[https://vzd-fhir-directory-test.vzd.ti-dienste.de/owner-authenticate]: https://vzd-fhir-directory-test.vzd.ti-dienste.de/owner-authenticate (&93834771080528)
[https://fhir-directory-ref.vzd.ti-dienste.de/tim-provider-services]: https://fhir-directory-ref.vzd.ti-dienste.de/tim-provider-services (&93834810789888)
[https://fhir-directory-test.vzd.ti-dienste.de/tim-provider-services]: https://fhir-directory-test.vzd.ti-dienste.de/tim-provider-services (&93834810791440)
[https://oauth.vzd.ti-dienste.de/authenticate ]: https://oauth.vzd.ti-dienste.de/authenticate%A0 (&93834810813840)
[https://ru-oauth-test.vzd.ti-dienste.de/authenticate]: https://ru-oauth-test.vzd.ti-dienste.de/authenticate (&93834810815392)
[https://tu-oauth-test.vzd.ti-dienste.de/authenticate]: https://tu-oauth-test.vzd.ti-dienste.de/authenticate (&93834810816944)
[https://github.com/gematik/api-vzd/blob/main/src/openapi/I_VZD_TIM_Provider_Services.yaml]: https://github.com/gematik/api-vzd/blob/main/src/openapi/I_VZD_TIM_Provider_Services.yaml (&93834810829048)
[https://owasp.org/www-project-top-ten/]: https://owasp.org/www-project-top-ten/ (&93834771010736)
[https://simplifier.net/vzd-fhir-directory/]: https://simplifier.net/vzd-fhir-directory/ (&93834783651944)
[de.gematik.fhir.directory 0.6.1]: https://simplifier.net/packages/de.gematik.fhir.directory/0.6.1 (&93834783653680)
[http://hapi.fhir.org/baseR4/HealthcareService?location.address=10117&_include=Organization&_pretty=true]: http://hapi.fhir.org/baseR4/HealthcareService?location.address=10117&_include=Organization&_pretty=true (&93834783665088)
