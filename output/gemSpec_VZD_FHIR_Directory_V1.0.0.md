
Elektronische Gesundheitskarte und Telematikinfrastruktur

### Spezifikation<br>Verzeichnisdienst FHIR-Directory

- Klassifizierung: öffentlich
- Referenzierung: gemSpec_VZD_FHIR_Directory
- Revision: 408162
- Stand: 01.10.2021
- Status: freigegeben
- Version: 1.0.0

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

</td></tr><tr></tr><tr><td>
</td><td>
</td><td>
</td><td>
</td><td>
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
  - [3.1] Akteure und Rollen
  - [3.2] User Stories
  - [3.3] Nachbarsysteme
- [4] Zerlegung des Produkttyps
- [5] Funktionsmerkmale
  - [5.1] FHIR-Directory
    - [5.1.1] Datenmodell
    - [5.1.2] Mapping von LDAP auf FHIR-Ressourcen
    - [5.1.3] FHIR RESTful API
  - [5.2] FHIR-Proxy und PASSporT-Service
    - [5.2.1] Schnittstellen
      - [5.2.1.1] TLS-Verbindungsaufbau
      - [5.2.1.2] FHIR Schnittstelle für TI-Messenger-Nutzer
      - [5.2.1.3] FHIR-Schnittstelle für Besitzer
      - [5.2.1.4] Schnittstelle I_VZD_TIM_Provider_Services
    - [5.2.2] Aktualisierung der Basiseinträge
    - [5.2.3] Erzeugung und Verteilung der Föderationsliste
  - [5.3] Übergreifende Vorgaben
    - [5.3.1] Sicherheit
    - [5.3.2] Betrieb
- [6] Anwendungsfälle
  - [6.1] TI-Messenger-Nutzer sucht TIOrganization- und TIPractitioner-Einträge im VZD-FHIR-Directory
  - [6.2] TIOrganization-Einträge oder TIPractitioner-Einträge im VZD-FHIR-Directory ändern
  - [6.3] Anwendungsfälle der TI-Messenger-Anbieter im VZD-FHIR-Directory
  - [6.4] Einträge mit dem VZD-LDAP-Directory abgleichen
- [7] Verteilungssicht
- [8] Anhang A – Verzeichnisse
  - [8.1] Abkürzungen
  - [8.2] Glossar
  - [8.3] Abbildungsverzeichnis
  - [8.4] Tabellenverzeichnis
  - [8.5] Referenzierte Dokumente
    - [8.5.1] Dokumente der gematik
    - [8.5.2] Weitere Dokumente
- [9] Anhang B - Beispiele
  - [9.1] FHIR Operationen
    - [9.1.1] Abfrage von TIOrganisation Einträgen
      - [9.1.1.1] Client Code
      - [9.1.1.2] Request
      - [9.1.1.3] Request Headers
      - [9.1.1.4] Response
      - [9.1.1.5] Response Headers
      - [9.1.1.6] Response Body

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
Leistungserbringern gespeichert. Die Einträge werden mit den Einträgen im
VZD-LDAP-Directory synchronisiert. Bei diesem Vorgang erfolgt eine Umsetzung
von der LDAP-Datenstruktur auf die Datenstruktur der FHIR-Ressourcen.
Personeneinträge der Leistungserbringer werden auf die
TIPractitioner-Ressource und Organisations-Einträge auf die
TIOrganization-Ressource abgebildet. Die synchronisierten Einträge bilden die
Basis-Einträge, die durch die Besitzer um zusätzliche Daten ergänzt bzw.
erweitert werden können. TIPractitioner und TIOrganization sind Profilierungen
der FHIR-Ressourcen Practitioner und Organization. Die Anbieter von
Fachanwendungen werden ebenfalls als TIOrganization-Einträge im FHIR-Directory
eingetragen um Daten der Fachanwendung zu dieser Organisation zuordnen zu
können.

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
Nutzer ist nicht zulässig.

Als erste Anwendung wird der TI-Messenger das VZD-FHIR-Directory nutzen.

![Abbildung-1][Abbildung-1]

Das VZD-FHIR-Directory besteht aus den logischen Komponenten FHIR-Directory,
FHIR-Proxy und PASSporT-Service.

Das FHIR-Directory ist eine Implementierung der FHIR-Spezifikation
(http://hl7.org/fhir/summary.html ).

Der FHIR-Proxy terminiert die TLS-Verbindungen, prüft die Zugriffsberechtigung
der Nutzer und verteilt die Anfragen der Nutzer auf die Instanzen des
FHIR-Directory sowie des PASSporT-Service. Zusätzlich übernimmt und
aktualisiert der FHIR-Proxy die Basiseinträge im VZD-FHIR-Directory mit den
geänderten Daten des VZD-LDAP-Directories.

Der PASSporT-Service ist eine Komponente, die Personal Assertion Token gemäß
[RFC8225] ausstellt. Die Token bestätigen, dass ein Leistungserbringer oder
eine Organisation durch die Eintragung der TI-Messenger-Adresse im
VZD-FHIR-Directory damit einverstanden ist, dass eine
TI-Messenger-Kommunikation zu dieser Adresse aufgebaut werden darf. Für die
Signatur des PASSporT wird ein Zertifikat aus der Komponenten PKI der TI
verwendet.

### 3 Systemkontext

### 3.1 Akteure und Rollen

Das VZD-FHIR-Directory ist ein Dienst der Telematikinfrastruktur und kann von
allen Nutzern der TI abgefragt werden. Zusätzlich ist es erforderlich, dass
die Einträge gepflegt werden. Dies erfolgt durch die Kartenherausgeber, die
Fachanwendungen, falls spezifische Fachdaten den Einträgen zugeordnet sind,
und optional durch die Besitzer der Einträge.

<table><tr><th>
Akteur

</th><th>
Rolle

</th><th>
Beschreibung

</th></tr><tr><td>
TI-Messenger-Nutzer

</td><td>
User

</td><td>
TI-Messenger-Nutzer sind Leistungserbringer, Mitarbeiter in Organisationen des
Gesundheitswesens und Versicherte. Sie können im Rahmen der Fachanwendung
TI-Messenger Einträge im VZD-FHIR-Directory lesen.

</td></tr><tr><td>
Besitzer 

</td><td>
Admin_Owner

</td><td>
Ein Besitzer ist der Leistungserbringer oder die Organisation des
Gesundheitswesens dessen bzw. deren Daten im Eintrag gespeichert sind.

Ein Besitzer eines Eintrags im VZD-FHIR-Directory ist berechtigt, ihm
zugeordnete Attribute in eigenen Eintrag anzulegen, zu ändern, zu löschen
und zu lesen.

</td></tr><tr><td>
Kartenherausgeber

</td><td>
Admin_Base_Entry

</td><td>
Kartenherausgeber sind berechtigt, Basiseinträge für von ihnen mit
Telematik-IDs ausgestattete Leistungserbringer und Organisationen des
Gesundheitswesens anzulegen, zu bearbeiten, zu lesen und zu löschen.

</td></tr><tr><td>
Fachanwendung

</td><td>
Admin_Application_Data

</td><td>
Die Fachanwendung ist ein generischer Akteur.

Fachanwendungen sind berechtigt, ihnen zugeordnete Attribute von Einträgen im
Directory anzulegen, zu ändern und zu löschen. Sie sind im Rahmen ihrer
Aufgabe berechtigt, die Einträge zu lesen.

</td></tr><tr><td>
TI-Messenger-Registrierungsdienst

</td><td>
Admin_TI_Messenger_Data

</td><td>
Der TI-Messenger-Registrierungsdienst ist berechtigt, einen
TIOrganization-Eintrag anzulegen. Der Admin_TI_Messenger_Data KANN
Endpoint-Einträge anlegen, in denen die von ihm verwalteten
TI-Messenger-Domains eingetragen sind. Die Endpoint-Einträge MÜSSEN mit dem
eigenen TIOrganization-Eintrag verlinkt sein.

</td></tr><tr><td>
Gesamtverantwortlicher TI

</td><td>
GTI

</td><td>
Die gematik als Gesamtverantwortlicher TI und damit für den sicheren,
funktionalen und interoperablen Betrieb der Anwendungen und Komponenten erhält
im Rahmen des Monitorings und Reporting sowohl Informationen über die
technischen Vorgänge als auch über die Datenbestände innerhalb des Dienstes.

</td></tr></table>

### 3.2 User Stories

 ---> UL

 ---> UL

 ---> UL

 ---> UL

 ---> UL

### 3.3 Nachbarsysteme

Die Nachbarsysteme des VZD-FHIR-Directory sind Client- und Serverkomponenten des
TI-Messengers, das VZD-LDAP-Directory, die IDPs aus der TI-IDP-Föderation und
die Betriebsdatenerfassung der gematik. 

**ML-123876 - Test gegen die Referenzimplementierung der Nachbarsysteme
(VZD-FHIR-Directory)**

Es MÜSSEN alle Anwendungsfälle des VZD-FHIR-Directories erfolgreich gegen die
Referenzimplementierung der Nachbarsysteme getestet sein. **[\<=]**

### 4 Zerlegung des Produkttyps

Die folgende Abbildung zeigt die Teilkomponenten des bisherigen
VZD-LDAP-Directory und die rot dargestellten neuen Komponenten des
VZD-FHIR-Directory.

![Img-002][Img-002]

Das VZD-FHIR-Directory besteht aus den Komponenten FHIR-Proxy und FHIR-Directory
sowie PASSPorT-Service. Die Schnittstelle zwischen FHIR-Proxy und
PASSporT-Service wird nicht vorgegeben.

Die vom VZD-FHIR-Directory zu liefernden Rohdaten zur Ermittlung der Auslastung
und Performance werden in den bereits vorhandenen
Betriebsdaten-Erfassungs-Client (BDE-Client) des Verzeichnisdienstes integriert.

### 5 Funktionsmerkmale

In diesem Kapitel werden die Komponenten des VZD-FHIR-Directories beschrieben.

### 5.1 FHIR-Directory

Das FHIR-Directory ist eine Implementierung der HL7-FHIR-Spezifikation Release
4.0.1 (https://www.hl7.org/fhir/http.html ).

Das FHIR-Directory ist nur über den FHIR-Proxy erreichbar.

### 5.1.1 Datenmodell

Es werden die FHIR-Ressourcen nach folgender Tabelle verwendet.

Alle Änderungen und Erweiterungen der FHIR Ressourcen sind
in https://simplifier.net/vzd-fhir-directory veröffentlicht.

<table><tr><th>
FHIR-Ressource

</th><th>
Beschreibung

</th></tr><tr><td>
TIOrganization

</td><td>
Profil der Organization Ressource.

(

https://simplifier.net/vzd-fhir-directory/tiorganization

)

Das Element Identifier wurde so geändert, dass Telematik-IDs als Identifier
verwendet werden können (

https://gematik.de/fhir/VZD-FHIR-Directory/NamingSystem/TelematikID

).

Im Element type wird der Typ der Organisation eingetragen. Dafür werden die
CodeSysteme 

https://gematik.de/fhir/VZD-FHIR-Directory/CodeSystem/TIOrganizationTypeCS

 und

https://gematik.de/fhir/VZD-FHIR-Directory/CodeSystem/TIProfessionOidCS

 sowie das ValueSet 

https://gematik.de/fhir/VZD-FHIR-Directory/ValueSet/TIOrganizationTypeVS

  verwendet.

Im Element telecom KANN der Besitzer eines TIOrganisation Eintrags oder eines
TIPractitioner Eintrags TI-Messenger-Adressen (MXID) in url-Notation speichern
(telecom.system = url; telecom.value = MXID in url Notation
matrix:u/localpart:tim-domain).

Mit telecom.period.end lässt sich steuern, ob der Besitzer einverstanden ist,
dass andere TI-Messenger-Nutzer mit der in telecom.value gespeicherten MXID
Kontakt aufnehmen dürfen.

telecom.period.end = leer oder Datum in der Zukunft bedeutet: Kontaktaufnahme
ist erlaubt

telecom.period.end = Datum in der Vergangenheit bedeutet: Kontaktaufnahme ist
nicht erlaubt (gilt nur, wenn die MXID im VZD-FHIR-Directory gesucht wurde).

Durch den Besitzer erstellte TIOrganisations-Einträge MÜSSEN mit seinem
TIOrganisations-Eintrag über eine partOf-Referenz verlinkt sein.

Wenn das Element type den Wert "TI-Messenger-Provider" hat, dann handelt es sich
um eine Organisation, die einen TI-Messenger-Dienst innerhalb der
Telematikinfrastruktur bereitstellt. In endpoint-Referenzen der Organisation
werden die Domainnamen der TI-Messenger-Service-Instanzen eingetragen. Dazu
wird im Elem

ent connectionType d

as Codesystem

https://gematik.de/fhir/VZD-FHIR-Directory/CodeSystem/TIMessengerCS

mit

  verwendet. Im Element "name" wird der TI-Messenger Domainname eingetragen.
In "managingOrganization" wird die TIOrganization eingetragen, für die die
TI-Messenger-Domain eingerichtet wurde.

</td></tr><tr><td>
TIPractitioner

</td><td>
Profil der Practitioner Ressource. Lediglich das Element Identifier wurde so
geändert, dass Telematik-IDs als Identifier verwendet werden können. (

https://simplifier.net/vzd-fhir-directory/tipractitioner

 )

</td></tr><tr><td>
Endpoint

</td><td>
Endpoint Ressource (

https://www.hl7.org/fhir/endpoint.html

 )

</td></tr><tr><td>
Location

</td><td>
Location (

https://www.hl7.org/fhir/location.html

 )

</td></tr><tr><td>
HealthcareService 

</td><td>
HealthcareService (

https://www.hl7.org/fhir/healthcareservice.html

 )

</td></tr><tr><td>
PractitionerRole

</td><td>
PractitionerRole (

https://www.hl7.org/fhir/practitionerrole.html

)

</td></tr></table>

**ML-123880 - Einschränkung der nutzbaren FHIR-Ressourcen (VZD-FHIR-Directory)**

Nur die in Tabelle "VZD-FHIR-Directory, FHIR-Ressourcen" angegebenen Ressourcen
dürfen im VZD-FHIR-Directory erzeugt werden. **[\<=]**

### 5.1.2 Mapping von LDAP auf FHIR-Ressourcen

Die TIOrganization- und TIPractitioner-Basiseinträge werden durch den FHIR
Proxy mit den Daten aus dem VZD-LDAP-Directory initial erzeugt und
anschließend fortlaufend aktualisiert. Die Daten können nicht durch die
Besitzer (Leistungserbringer und Organisationen) geändert werden.

Die Daten aus dem VZD-LDAP-Directory werden wie folgt den FHIR-Ressourcen
zugeordnet.

<table><tr><th>
LDAP-Eintragstyp 

</th><th>
LDAP-Attribut

</th><th>
FHIR-Ressource

</th><th>
FHIR-Element

</th></tr><tr><td>
HBA und SMC-B 

</td><td>
givenName

</td><td>
–

</td><td>
–

</td></tr><tr><td>
HBA und SMC-B 

</td><td>
sn

</td><td>
–

</td><td>
–

</td></tr><tr><td>
HBA und SMC-B 

</td><td>
cn

</td><td>
–

</td><td>
–

</td></tr><tr><td>
HBA und SMC-B 

</td><td>
displayName

</td><td>
TIPractitioner

TIOrganization

</td><td>
name = displayName

</td></tr><tr><td>
HBA und SMC-B

</td><td>
streetAddress,

postalCode,

countryCode,

localityName,

stateOrProvinceName

</td><td>
TIPractitioner

TIOrganization

</td><td>
address. use = work

address.type = postal

address.text = "streetAddress

&#13;&#10;

postalCode

&#13;&#10;

localityName

&#13;&#10;

stateOrProvinceName

&#13;&#10;

countryCode"

address.line="streetAddress"

address.city = localityName

address.state = stateOrProvinceName

address.postalCode = postalCode

address.country = countryCode

</td></tr><tr><td>
title

</td></tr><tr><td>
SMC-B

</td><td>
organization

</td><td>
TIOrganization

</td><td>
alias = organization

</td></tr><tr><td>
HBA

</td><td>
organization

</td><td>
–

</td><td>
–

</td></tr><tr><td>
HBA und SMC-B

</td><td>
otherName

</td><td>
–

</td><td>
–

</td></tr><tr><td>
SMC-B

</td><td>
specialization

Format

urn:psc:\<OID Codesystem:Code\>

</td><td>
HealthcareService

</td><td>
specialty.coding.system

= Codesystem  
specialty.coding.code = Code  
specialty.coding.display = \<added
by FHIR-Proxy\>

</td></tr><tr><td>
HBA

</td><td>
specialization

Format

urn:as:\<OID Codesystem:Code\>

</td><td>
TIPractitioner

</td><td>
qualification.code.coding.system = Codesystem

qualification.code.coding.code = Code

qualification.code.coding.display = \<added by FHIR-Proxy\>

</td></tr><tr><td>
HBA und SMC-B

</td><td>
domainID

</td><td>
–

</td><td>
–

</td></tr><tr><td>
HBA und SMC-B

</td><td>
holder

</td><td>
–

</td><td>
–

</td></tr><tr><td>
HBA und SMC-B

</td><td>
maxKOMLEadr

</td><td>
– 

</td><td>
–

</td></tr><tr><td>
HBA und SMC-B

</td><td>
personalEntry

</td><td>
–

</td><td>
–

</td></tr><tr><td>
HBA und SMC-B

</td><td>
dataFromAuthority

</td><td>
–

</td><td>
–

</td></tr><tr><td>
HBA und SMC-B

</td><td>
userCertificate

</td><td>
TIPractitioner

TIOrganization

</td><td>
telecom.system = other

telecom.value = userCertificate (im PEM Format)

</td></tr><tr><td>
HBA und SMC-B

</td><td>
entryType

</td><td>
–

</td><td>
–

</td></tr><tr><td>
HBA und SMC-B

</td><td>
telematikID

</td><td>
TIPractitioner

TIOrganization

</td><td>
identifier.value = telematikID

</td></tr><tr><td>
SMC-B

</td><td>
professionOID

</td><td>
TIOrganization

</td><td>
type.coding.system = 

https://gematik.de/fhir/VZD-FHIR-Directory/CodeSystem/TIProfessionOidCS

 

type.coding.code = professionOID

type.coding.display = display aus

https://gematik.de/fhir/VZD-FHIR-Directory/ValueSet/TIOrganizationTypeVS

 

</td></tr><tr><td>
HBA und SMC-B

</td><td>
usage

</td><td>
–

</td><td>
–

</td></tr><tr><td>
HBA und SMC-B

</td><td>
description

</td><td>
–

</td><td>
–

</td></tr><tr><td>
HBA und SMC-B

</td><td>
mail

</td><td>
–

</td><td>
–  

</td></tr><tr><td>
HBA und SMC-B

</td><td>
KOM-LE-Version

</td><td>
– 

</td><td>
–

</td></tr><tr><td>
HBA und SMC-B

</td><td>
changeDateTime

</td><td>
–

</td><td>
–

</td></tr></table>

### 5.1.3 FHIR RESTful API

Die Operationen der FHIR-Schnittstelle sind durch die FHIR-Spezifikation
festgelegt (https://www.hl7.org/fhir/http.html ).

### 5.2 FHIR-Proxy und PASSporT-Service

### 5.2.1 Schnittstellen

### 5.2.1.1 TLS-Verbindungsaufbau

Der FHIR-Proxy MUSS sich beim TLS-Verbindungsaufbau an den Endpunkten gegenüber
Clients mit einem Extended Validation TLS-Zertifikat eines Herausgebers gemäß
[CAB-Forum] authentisieren. Das Zertifikat MUSS an die Schnittstelle des
Eingangspunkts für Clientsysteme gebunden werden, damit Clientsysteme beim
TLS-Verbindungsaufbau eine vereinfachte Zertifikatsprüfung mit
TLS-Standardbibliotheken durchführen können.

### 5.2.1.2 FHIR Schnittstelle für TI-Messenger-Nutzer

Endpunkte für die Suche von Einträgen im VZD-FHIR-Directory durch
TI-Messenger-Clients

In der Produktionsumgebung ist die
URL: https://vzd-fhir-directory.vzd.ti-dienste.de/tim-search  

In der Referenzumgebung ist die
URL: https://ru-vzd-fhir-directory-test.vzd.ti-dienste.de/tim-search 

In der Testumgebung ist die
URL: https://tu-vzd-fhir-directory-test.vzd.ti-dienste.de/tim-search 

Authentisierung

Um die Schnittstelle nutzen zu können MÜSSEN sich die Clients mit einem
gültigen Accesstoken authentisieren, das von einem Matrix-Homeserver aus der
TI-Messenger-Föderation ausgestellt wurde. Im folgenden werden diese
AccesstokenMatrix-OpenID-Token genannt. Nach erfolgreicher Prüfung
des Matrix-OpenID-Token stellt der FHIR-Proxy dem TI-Messenger-Client ein
neues OAuth Accesstoken aus, dass für Suchanfragen des TI-Messenger-Clients
verwendet wird. Die Gültigkeitsdauer ist 24 Stunden.

Das Accesstoken enthält folgende Attribute:

<table><tr><td>
{  
  "iss": "https://vzd-fhir-directory.vzd.ti-dienste.de/tim-authenticate", 

  "sub": "\<MXID des TI-Messenger-Nutzers in url Notation\>",  
  "aud": [
"https://vzd-fhir-directory.vzd.ti-dienste.de/tim-search" ],  
  "iat":
1630306800,  
  "exp": 1630393200,  
  "scope": "tim-search"  
}

</td></tr></table>

Das Attribut "iss" enthält die URL des Endpunktes für die Authentisierung in
der jeweiligen Umgebung RU, TU oder PU.

Das Attribut "aud" enthält die URL des Endpunktes in der jeweiligen Umgebung
RU, TU oder PU.

Endpunkte für die Authentisierung

In der Produktionsumgebung ist die
URL: https://vzd-fhir-directory.vzd.ti-dienste.de/tim-authenticate  

In der Referenzumgebung ist die
URL: https://ru-vzd-fhir-directory-test.vzd.ti-dienste.de/tim-authenticate 

In der Testumgebung ist die
URL: https://tu-vzd-fhir-directory-test.vzd.ti-dienste.de/tim-authenticate 

Operationen

Die FHIROperationen für die Suche nach Einträgen im VZD-FHIR-Directory sind
in der HL7 FHIR Spezifikation (https://www.hl7.org/fhir/http.html ) festgelegt.

PASSporT-Service

Das VZD-FHIR-Directory MUSS für alle gefundenen MXIDs PASSporT erzeugen und in
die Response einfügen (siehe AF_10036).

Der Aufbau des PASSporT MUSS wie im RFC[8225] beschrieben erfolgen. Die
Befüllung der gezeigten Header Elemente MUSS wie im RFC[8225] gefordert
erfolgen und wie folgt aufgebaut sein:

<table><tr><th>
Header:  
   {  
      "typ":"passport",  
      "alg":"ES256",  
   
  "x5u":"https://cert.example.org/passport.cer"  
   }

</th></tr></table>

Die TI-Messenger spezifischen PASSporT-Claims sind durch den PASSporT-Service
wie folgt zu befüllen. Der Claim mit dem Bezeichner "orig" ist die MXID des
Nutzers der den GET /tim_search Request ausgeführt hat. Der Claim "dest" wird
mit der MXID des gefundenen Eintrags befüllt. Die MXIDs werden in url Notation
angegeben. Das folgende Beispiel zeigt eine solche Struktur.

<table><tr><th>
Claims:  
  {  
      "orig": {  
          "uri":
"matrix:u/me:example.org"  
      },  
      "dest": { 

          "uri": [  
            
"matrix:u/you:example.org"  
          ]  
      }  
  }

</th></tr></table>

Dieses erzeugte PASSporT wird dann durch den PASSporT-Service signiert und
anschließend an die gefundene MXID angefügt
(matrix:u/you:example.org/?PASSporT=[PASSporT-String]).

Die ausgestellten PASSporT werden mit einem Zertifikat aus der Komponenten PKI
der TI signiert. Die Zertifikate haben die keyUsage = digitalSignature.

### 5.2.1.3 FHIR-Schnittstelle für Besitzer

Die Schnittstelle ermöglicht es den Besitzern einer Telematik-ID ihren Eintrag
im VZD-FHIR-Directory zu ändern. Im, bei der Authentifizierung, verwendeten
Accesstoken ist die Telematik-ID des Nutzers enthalten. Nur der Eintrag
(TIPractitioner oder TIOrganization)mit der eigenen Telematik-ID darf
verändert werden. Dabei dürfen nur die Attribute verändert werden, die nicht
vom VZD-LDAP-Directory synchronisiert werden.

Endpunkte für das Ändern von eigenen Einträgen im VZD-FHIR-Directory durch
TI-Messenger Clients und Org-Admin-Clients

In der Produktionsumgebung ist die
URL: https://vzd-fhir-directory.vzd.ti-dienste.de/owner 

In der Referenzumgebung ist die
URL: https://ru-vzd-fhir-directory-test.vzd.ti-dienste.de/owner

In der Testumgebung ist die
URL: https://tu-vzd-fhir-directory-test.vzd.ti-dienste.de/owner 

Authentisierung

Um die Schnittstelle nutzen zu können, MÜSSEN sich die Clients mit einem
gültigen Accesstoken authentisieren, das vom FHIR-Proxy ausgestellt wurde.
Wenn kein gültiges Accesstoken im Client vorhanden ist, dann muss sich der
Client an einem IDP der TI-IDP-Föderation authentisieren.

Nur der eigene Eintrag mit einem Identifier passend zur Telematik-ID aus dem
Accesstoken KANN bearbeitet werden. Für einen eigenen TIOrganization-Eintrag
KÖNNEN weitere TIOrganization-Einträge erstellt und mit dem eigenen Eintrag
verlinkt werden.

Das Accesstoken enthält folgende Attribute:

<table><tr><td>
{  
  "iss": "https://vzd-fhir-directory.vzd.ti-dienste.de/owner-authenticate",
 
  "sub": "\<telematikID\>",  
  "aud": [
"https://vzd-fhir-directory.vzd.ti-dienste.de/owner" ],  
  "iat": 1630306800,
 
  "exp": 1630393200,  
  "scope": "owner"  
}

</td></tr></table>

Das Attribut "iss" enthält die URL des Endpunktes für die Authentisierung in
der jeweiligen Umgebung RU, TU oder PU.

Das Attribut "aud" enthält die URL des Endpunktes in der jeweiligen Umgebung
RU, TU oder PU.

Endpunkte für die Authentisierung

In der Produktionsumgebung ist die
URL: https://vzd-fhir-directory.vzd.ti-dienste.de/owner-authenticate   

In der Referenzumgebung ist die
URL: https://ru-vzd-fhir-directory-test.vzd.ti-dienste.de/owner-authenticate 

In der Testumgebung ist die
URL: https://tu-vzd-fhir-directory-test.vzd.ti-dienste.de/owner-authenticate 

Operationen

Die FHIR-Operationen für das Ändern von eigenen Einträgen im
VZD-FHIR-Directory sind in der HL7-FHIR-Spezifikation
(https://www.hl7.org/fhir/http.html ) festgelegt.

### 5.2.1.4 Schnittstelle I_VZD_TIM_Provider_Services

Endpunkte

In der Produktionsumgebung ist die
URL: https://vzd-fhir-directory.vzd.ti-dienste.de/tim-provider-services  

In der Referenzumgebung ist die
URL: https://ru-vzd-fhir-directory-test.vzd.ti-dienste.de/tim-provider-services 

In der Testumgebung ist die
URL: https://tu-vzd-fhir-directory-test.vzd.ti-dienste.de/tim-provider-services 

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

Für die Zugriff auf den OAuth-Server MUSS der TI-Messenger-Anbieter für seinen
Registrierungsdienst beim VZD-Anbieter Client-Credentials beantragen. Die
Beantragung erfolgt über einen Service-Request an betrieb@gematik.de mit dem
Betreff "VZD-FHIR-Directory (De-)/Registrierung" notwendig.

Die Registrierung und Vergabe der Credentials erfolgt dabei auf
Organisationsebene.

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

https://github.com/gematik/api-vzd/blob/master/src/I_VZD_TIM_Provider_Services.yaml 

<table><tr><th>
Operation

</th><th>
Beschreibung

</th></tr><tr><td>
GET /

</td><td>
Mit dieser Operation können Metadaten (insbesondere auch die Version und das
verwendete yaml-File) dieser Schnittstelle abgefragt werden.

</td></tr><tr><td>
GET 

/FederationList

</td><td>
Mit dieser Operation wird die Liste der an der TI-Messenger-Föderation
beteiligten Matrix-Domainnamen abgefragt (Föderationsliste). 

</td></tr><tr><td>
GET 

/PASSporTCertificates

</td><td>
Mit dieser Operat

ion werden die PASSporT-Signatur-Zertifikate abg

efragt.

</td></tr><tr><td>
GET, POST, PUT, DELETE /FHIR

</td><td>
Die FHIR-

Operationen für das Ändern von eigenen TIOrganization-Einträgen und von
Endpoint-Einträgen im VZD-FHIR-Directory sind in der HL7-FHIR-Spezifikation
(https://www.hl7.org/fhir/http.html) festgelegt.

</td></tr></table>

Im Attribut "sub" des Accesstoken ist die client_id des
TI-Messenger-Registrierungsdienstes enthalten. Wenn der
TI-Messenger-Registrierungsdienst einen TIOrganization-Eintrag erzeugt, dann
MUSS die client_id im Element alias des Eintrage enthalten sein

### 5.2.2 Aktualisierung der Basiseinträge

Der FHIR-Proxy aktualisiert regelmäßig die Basiseinträge im
VZD-FHIR-Directory mit den geänderten Daten des VZD-LDAP-Directories (siehe
AF_10047 Einträge mit dem VZD-LDAP-Directory abgleichen). Das Intervall für
die regelmäßige Aktualisierung MUSS konfigurierbar sein und wird initial auf
2 Stunden festgelegt.

Zukünftig ist vorgesehen, dass Kartenherausgeber direkt die Basiseinträge
ihrer Mitglieder im VZD-FHIR-Directory über eine FHIR-Schnittstelle verwalten
können.

### 5.2.3 Erzeugung und Verteilung der Föderationsliste

Der FHIR-Proxy MUSS bei jeder Änderung an den Endpoint-Einträgen der
TIM-Anbieter über die Schnittstelle I_VZD_TIM_Provider_Services die
Föderationsliste aktualisieren und dabei die Versionsnummer erhöhen und
anschließend über ein internes Netzwerk des Anbieters auf alle
FHIR-Proxy-Instanzen verteilen sowie für die Abfrage über die Schnittstelle
I_VZD_TIM_Provider_Services bereithalten.

Die Föderationsliste wird vollständig erzeugt, indem alle Endpoint Einträge
abgefragt werden, die das CodeSystem connectionType.System
= https://gematik.de/fhir/VZD-FHIR-Directory/CodeSystem/TIMessengerCS 

und den connectionType.code == "tim-domain" haben.

Für jeden Endpoint-Eintrag wird aus dem Wert des Elements "name" mit dem
Hash-Algorithmus "SHA-256" ein hash gebildet und in die Föderationsliste
eingetragen. In der Föderationsliste MUSS das Element hashAlgorithm den Wert
"SHA-256" haben

(siehe I_VZD_TIM_Provider_Services.yaml).

Die Aktualisierung der Föderationsliste KANN so implementiert werden, dass nur
die geänderten Endpoint-Einträge in der Föderationsliste aktualisiert werden
(z. B. über FHIR R4.5.1 Subscriptions; siehe
https://build.fhir.org/subscription.html ).

Der Anbieter des VZD-FHIR-Directories MUSS geeignete Maßnahmen vorsehen, die
verhindern, dass die Föderationsliste manipuliert werden kann.

**ML-123677 - Maßnahmen gegen die Manipulation der Föderationsliste
(VZD-FHIR-Directory, Sicherheitsgutachten)**

Im Sicherheitsgutachten des VZD-FHIR-Directories sind geeignete Maßnahmen gegen
die Manipulation der Föderationsliste beschrieben. **[\<=]**

### 5.3 Übergreifende Vorgaben

### 5.3.1 Sicherheit

Schutz vor Sicherheits-Risiken

Das VZD-FHIR-Directory MUSS Maßnahmen zum Schutz vor Sicherheits-Risiken
gemäß der aktuellen Version der OWASP-Top-10 umsetzen
(https://owasp.org/www-project-top-ten/ ).

Es gelten Die Anforderungen an TLS-Verbindungen gemäß [gemSpec_Krypt#3.3.2]
TLS-Verbindungen.

**ML-123682 - Maßnahmen zum Schutz vor Sicherheits-Risiken (VZD-FHIR-Directory,
Sicherheitsgutachten)**

Im Sicherheitsgutachten des VZD-FHIR-Directories sind geeignete Maßnahmen zum
Schutz vor Sicherheits-Risiken gemäß der aktuellen Version der OWASP-Top-10
beschrieben. **[\<=]**

### 5.3.2 Betrieb

Das VZD-FHIR-Directory wird betrieblich als eine weitere Servicekomponente im
Sinne der Weiterentwicklung des Verzeichnisdienstes betrachtet. Diese
Servicekomponente kann, bis auf die Schnittstellen, unabhängig vom
VZD-LDAP-Directory entwickelt und deployt werden. Aus Nutzersicht ist weniger
die interne, logische Struktur der Verzeichnisdienste relevant sondern die
Verfügbarkeit der Schnittstellen und die im Verzeichnis enthaltenen Daten.

Das VZD-FHIR-Directory MUSS mit einer vollumfänglich-funktionalen
Verfügbarkeit von 99,8 % zur Hauptzeit und 99 % zur Nebenzeit betreibbar sein.

Der Anbieter des VZD-FHIR-Directorys MUSS sein Produkt VZD-FHIR-Directory mit
einer vollumfänglich-funktionalen Verfügbarkeit von 99,8 % zur Hauptzeit und
99 % zur Nebenzeit betreiben.

### 6 Anwendungsfälle

### 6.1 TI-Messenger-Nutzer sucht TIOrganization- und TIPractitioner-Einträge im VZD-FHIR-Directory

**AF_10036 - TI-Messenger-Nutzer sucht TIOrganization- und
TIPractitioner-Einträge im VZD-FHIR-Directory**

![Img-003][Img-003]

Abbildung3: Sequence diagram /tim-search **[\<=]**

Akzeptanzkriterien für den Anwendungsfall AF_10036 Nutzer sucht TIOrganization-
und TIPractitioner-Einträge im VZD-FHIR-Directory

**ML-123485 - Authentifizierung am Endpunkt /tim-search (VZD-FHIR-Directory,
Sicherheitsgutachten)**

Am Endpunkt /tim-search des FHIR-Proxy darf die Authentifizierung nur für
Nutzer erfolgreich sein, die an einem Homeserver der TI-Messenger Föderation
registriert sind. **[\<=]**

**ML-123483 - PASSporT Erzeugung (VZD-FHIR-Directory, Sicherheitsgutachten)**

Der FHIR-Proxy darf nur PASSporT ausstellen, wenn im telecom Element des
Eintrags eine MXID in url-Form vorhanden ist und das period.endDate nicht in
der Vergangenheit liegt. **[\<=]**

### 6.2 TIOrganization-Einträge oder TIPractitioner-Einträge im VZD-FHIR-Directory ändern

**AF_10037 - TIOrganization-Einträge oder TIPractitioner-Einträge im
VZD-FHIR-Directory ändern**

![Img-004][Img-004]

Abbildung4: Sequenzdiagramm VZD-FHIR-Directory Änderung von eigenen
TIOrganization- oder TIPractitioner-Einträgen **[\<=]**

Akzeptanzkriterien für den Anwendungsfall AF_10037 TIOrganization-Einträge im
VZD-FHIR-Directory ändern

**ML-123873 - Authentifizierung am Endpunkt /owner (VZD-FHIR-Directory,
Sicherheitsgutachten)**

Am Endpunkt /owner des FHIR-Proxy darf die Authentifizierung nur für Nutzer
erfolgreich sein, die ein gültiges Accesstoken vom VZD-FHIR-Directory
vorweisen. **[\<=]**

**ML-123874 - Nur Einträge mit eigener Telematik-ID verändern
(VZD-FHIR-Directory)**

Im, bei der Authentifizierung verwendeten, Accesstoken ist die Telematik-ID des
Nutzers enthalten. Nur der Eintrag (TIPractitioner oder TIOrganization)mit der
eigenen Telematik-ID darf verändert werden.Dabei dürfen nur die Attribute
verändert werden, die nicht vom VZD-LDAP-Directory synchronisiert werden.
**[\<=]**

**ML-123482 - Selbst angelegte TIOrganisation-Einträge MÜSSEN mit dem eigenen
Basiseintrag verlinkt sein (VZD-FHIR-Directory)**

Alle selbst durch den Besitzer angelegten FHIR-Einträge MÜSSEN mit dem eigenen
Basiseintrag mittels partOf verlinkt sein. Wenn keine korrekte Verlinkung
angegeben ist, dann MUSS der FHIR-Proxy das Erzeugen oder die Änderung des
TIOrganisation-Eintrags mit der Fehlermeldung (HTTP 422 Unprocessable Entity)
ablehnen. **[\<=]**

### 6.3 Anwendungsfälle der TI-Messenger-Anbieter im VZD-FHIR-Directory

**AF_10048 - Anwendungsfälle der TI-Messenger-Anbieter im VZD-FHIR-Directory**

![Img-005][Img-005]

Abbildung5: VZD-FHIR-Directory_Sequenzdiagramm_TI-Messenger-Provider-Services **[\<=]**

**ML-123881 - Authentifizierung an der Schnittstelle I_VZD_TIM_Provider_Services
(VZD-FHIR-Directory, Sicherheitsgutachten)**

An der Schnittstelle I_VZD_TIM_Provider_Services darf die Authentifizierung nur
für Clients erfolgreich sein, die ein gültiges Accesstoken vom OAuth-Server
des VZD-Anbieters vorweisen. **[\<=]**

### 6.4 Einträge mit dem VZD-LDAP-Directory abgleichen

**AF_10047 - Einträge mit dem VZD-LDAP-Directory abgleichen**

![Img-006][Img-006]

Abbildung6: VZD-FHIR-Directory, Aktualisierung der Basiseinträge **[\<=]**

### 7 Verteilungssicht

Das VZD-FHIR-Directory unterstützt initial die Anwendung TI-Messenger; wird
zukünftig aber auch die anderen Anwendungen wie ePA und KIM in deren
Folgeversionen sowie bisher unbekannte Fachanwendungen unterstützen. Es ist
daher erforderlich, dass das VZD-FHIR-Directory mit der Anzahl der
Nutzerzugriffe skalieren und anwendungsspezifische Ressourcen speichern kann.

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

### 8 Anhang A – Verzeichnisse

### 8.1 Abkürzungen

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
PASSporT

</td><td>
Personal Assertion Token

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

### 8.2 Glossar

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

### 8.3 Abbildungsverzeichnis

- [Abbildung-1] - Systemüberblick VZD-FHIR-Directory
- [Abbildung-7] - VZD-FHIR-Directory, Verteilungssicht

### 8.4 Tabellenverzeichnis

- [Tabelle-1] - VZD_FHIR_Directory_Akteure_und_Rollen
- [Tabelle-2] - VZD-FHIR-Directory, FHIR-Ressourcen
- [Tabelle-3] - VZD-FHIR-Directory_Mapping_LDAP_to_FHIR
- [Tabelle -4] - Tab_VZD_TIM-Provider-Services_Operations

### 8.5 Referenzierte Dokumente

### 8.5.1 Dokumente der gematik

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

### 8.5.2 Weitere Dokumente

<table><tr><th>
[Quelle]

</th><th>
Herausgeber (Erscheinungsdatum): Titel

</th></tr><tr></tr></table>

### 9 Anhang B - Beispiele

### 9.1 FHIR Operationen

### 9.1.1 Abfrage von TIOrganisation Einträgen

### 9.1.1.1 Client Code

// Create a client (only needed once)FhirContext ctx = new
FhirContext();IGenericClient client =
ctx.newRestfulGenericClient("http://hapi.fhir.org/baseR4");// Invoke the
clientBundle bundle =
client.search().forResource(TIOrganization.class).where(new
StringClientParam("address").matches().value("10117"))  
.include(new
Include("TIOrganization:endpoint"))  
.prettyPrint()  
.execute();

### 9.1.1.2 Request

GET http://hapi.fhir.org/baseR4

### 9.1.1.3 Request Headers

Accept-Charset: utf-8  
Accept: application/fhir+xml;q=1.0,
application/fhir+json;q=1.0, application/xml+fhir;q=0.9,
application/json+fhir;q=0.9  
User-Agent: HAPI-FHIR/5.5.0-PRE1-SNAPSHOT (FHIR
Client; FHIR 4.0.1/R4; apache)  
Accept-Encoding: gzip

### 9.1.1.4 Response

HTTP 200 OK

### 9.1.1.5 Response Headers

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

### 9.1.1.6 Response Body

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
[3]:                     #3-systemkontext
[3.1]:                   #31-akteure-und-rollen
[3.2]:                   #32-user-stories
[3.3]:                   #33-nachbarsysteme
[4]:                     #4-zerlegung-des-produkttyps
[5]:                     #5-funktionsmerkmale
[5.1]:                   #51-fhir-directory
[5.1.1]:                 #511-datenmodell
[5.1.2]:                 #512-mapping-von-ldap-auf-fhir-ressourcen
[5.1.3]:                 #513-fhir-restful-api
[5.2]:                   #52-fhir-proxy-und-passport-service
[5.2.1]:                 #521-schnittstellen
[5.2.1.1]:               #5211-tls-verbindungsaufbau
[5.2.1.2]:               #5212-fhir-schnittstelle-für-ti-messenger-nutzer
[5.2.1.3]:               #5213-fhir-schnittstelle-für-besitzer
[5.2.1.4]:               #5214-schnittstelle-i_vzd_tim_provider_services
[5.2.2]:                 #522-aktualisierung-der-basiseinträge
[5.2.3]:                 #523-erzeugung-und-verteilung-der-föderationsliste
[5.3]:                   #53-übergreifende-vorgaben
[5.3.1]:                 #531-sicherheit
[5.3.2]:                 #532-betrieb
[6]:                     #6-anwendungsfälle
[6.1]:                   #61-ti-messenger-nutzer-sucht-tiorganization--und-tipractitioner-einträge-im-vzd-fhir-directory
[6.2]:                   #62-tiorganization-einträge-oder-tipractitioner-einträge-im-vzd-fhir-directory-ändern
[6.3]:                   #63-anwendungsfälle-der-ti-messenger-anbieter-im-vzd-fhir-directory
[6.4]:                   #64-einträge-mit-dem-vzd-ldap-directory-abgleichen
[7]:                     #7-verteilungssicht
[8]:                     #8-anhang-a-–-verzeichnisse
[8.1]:                   #81-abkürzungen
[8.2]:                   #82-glossar
[8.3]:                   #83-abbildungsverzeichnis
[8.4]:                   #84-tabellenverzeichnis
[8.5]:                   #85-referenzierte-dokumente
[8.5.1]:                 #851-dokumente-der-gematik
[8.5.2]:                 #852-weitere-dokumente
[9]:                     #9-anhang-b---beispiele
[9.1]:                   #91-fhir-operationen
[9.1.1]:                 #911-abfrage-von-tiorganisation-einträgen
[9.1.1.1]:               #9111-client-code
[9.1.1.2]:               #9112-request
[9.1.1.3]:               #9113-request-headers
[9.1.1.4]:               #9114-response
[9.1.1.5]:               #9115-response-headers
[9.1.1.6]:               #9116-response-body
[Abbildung-1]:           gemSpec_VZD_FHIR_Directory_V1.0.0.attachments/8113109558214208944.png
[Img-002]:               gemSpec_VZD_FHIR_Directory_V1.0.0.attachments/12227914605283840879.png
[Img-003]:               gemSpec_VZD_FHIR_Directory_V1.0.0.attachments/12438437665341644804.png
[Img-004]:               gemSpec_VZD_FHIR_Directory_V1.0.0.attachments/13419995141599807919.png
[Img-005]:               gemSpec_VZD_FHIR_Directory_V1.0.0.attachments/16596192902717392488.png
[Img-006]:               gemSpec_VZD_FHIR_Directory_V1.0.0.attachments/11705194599738530532.png
[Abbildung-7]:           gemSpec_VZD_FHIR_Directory_V1.0.0.attachments/10304338528505342833.png
[Tbl-001]:               #Tbl-001 (&93834794179920)
[Tbl-002]:               #Tbl-002 (&93834789480480)
[Tabelle-1]:             #Tabelle-1 (&93834765146760)
[Tabelle-2]:             #Tabelle-2 (&93834804588480)
[Tabelle-3]:             #Tabelle-3 (&93834764154232)
[Tbl-006]:               #Tbl-006 (&93834799840696)
[Tbl-007]:               #Tbl-007 (&93834771057992)
[Tbl-008]:               #Tbl-008 (&93834771066776)
[Tbl-009]:               #Tbl-009 (&93834772231080)
[Tbl-010]:               #Tbl-010 (&93834772265440)
[Tabelle -4]:            #Tabelle -4 (&93834801614752)
[Tbl-012]:               #Tbl-012 (&93834781672592)
[Tbl-013]:               #Tbl-013 (&93834781700936)
[Tbl-014]:               #Tbl-014 (&93834781724224)
[Tbl-015]:               #Tbl-015 (&93834801454848)
[http://hl7.org/fhir/summary.html]: http://hl7.org/fhir/summary.html (&93834765140304)
[https://www.hl7.org/fhir/http.html]: https://www.hl7.org/fhir/http.html (&93834804582504)
[https://simplifier.net/vzd-fhir-directory]: https://simplifier.net/vzd-fhir-directory (&93834804585856)
[https://simplifier.net/vzd-fhir-directory/tiorganization]: https://simplifier.net/vzd-fhir-directory/tiorganization (&93834775008952)
[https://gematik.de/fhir/VZD-FHIR-Directory/NamingSystem/TelematikID]: https://gematik.de/fhir/VZD-FHIR-Directory/NamingSystem/TelematikID (&93834775010208)
[https://gematik.de/fhir/VZD-FHIR-Directory/CodeSystem/TIOrganizationTypeCS]: https://gematik.de/fhir/VZD-FHIR-Directory/CodeSystem/TIOrganizationTypeCS (&93834775011464)
[https://gematik.de/fhir/VZD-FHIR-Directory/CodeSystem/TIProfessionOidCS]: https://gematik.de/fhir/VZD-FHIR-Directory/CodeSystem/TIProfessionOidCS (&93834775012416)
[https://gematik.de/fhir/VZD-FHIR-Directory/ValueSet/TIOrganizationTypeVS]: https://gematik.de/fhir/VZD-FHIR-Directory/ValueSet/TIOrganizationTypeVS (&93834775013368)
[https://gematik.de/fhir/VZD-FHIR-Directory/CodeSystem/TIMessengerCS]: https://gematik.de/fhir/VZD-FHIR-Directory/CodeSystem/TIMessengerCS (&93834775017416)
[https://simplifier.net/vzd-fhir-directory/tipractitioner]: https://simplifier.net/vzd-fhir-directory/tipractitioner (&93834775027480)
[https://www.hl7.org/fhir/endpoint.html]: https://www.hl7.org/fhir/endpoint.html (&93834775030056)
[https://www.hl7.org/fhir/location.html]: https://www.hl7.org/fhir/location.html (&93834775032632)
[https://www.hl7.org/fhir/healthcareservice.html]: https://www.hl7.org/fhir/healthcareservice.html (&93834775035208)
[https://www.hl7.org/fhir/practitionerrole.html]: https://www.hl7.org/fhir/practitionerrole.html (&93834775038144)
[https://gematik.de/fhir/VZD-FHIR-Directory/CodeSystem/TIProfessionOidCS]: https://gematik.de/fhir/VZD-FHIR-Directory/CodeSystem/TIProfessionOidCS (&93834799917232)
[https://gematik.de/fhir/VZD-FHIR-Directory/ValueSet/TIOrganizationTypeVS]: https://gematik.de/fhir/VZD-FHIR-Directory/ValueSet/TIOrganizationTypeVS (&93834799918792)
[https://www.hl7.org/fhir/http.html]: https://www.hl7.org/fhir/http.html (&93834799936256)
[https://vzd-fhir-directory.vzd.ti-dienste.de/tim-search]: https://vzd-fhir-directory.vzd.ti-dienste.de/tim-search (&93834799833760)
[https://ru-vzd-fhir-directory-test.vzd.ti-dienste.de/tim-search]: https://ru-vzd-fhir-directory-test.vzd.ti-dienste.de/tim-search (&93834799835312)
[https://tu-vzd-fhir-directory-test.vzd.ti-dienste.de/tim-search]: https://tu-vzd-fhir-directory-test.vzd.ti-dienste.de/tim-search (&93834799836864)
[https://vzd-fhir-directory.vzd.ti-dienste.de/tim-authenticate]: https://vzd-fhir-directory.vzd.ti-dienste.de/tim-authenticate (&93834799860464)
[https://ru-vzd-fhir-directory-test.vzd.ti-dienste.de/tim-authenticate]: https://ru-vzd-fhir-directory-test.vzd.ti-dienste.de/tim-authenticate (&93834799862016)
[https://tu-vzd-fhir-directory-test.vzd.ti-dienste.de/tim-authenticate]: https://tu-vzd-fhir-directory-test.vzd.ti-dienste.de/tim-authenticate (&93834771051288)
[https://vzd-fhir-directory.vzd.ti-dienste.de/owner]: https://vzd-fhir-directory.vzd.ti-dienste.de/owner (&93834771078096)
[https://ru-vzd-fhir-directory-test.vzd.ti-dienste.de/owner]: https://ru-vzd-fhir-directory-test.vzd.ti-dienste.de/owner (&93834771079648)
[https://tu-vzd-fhir-directory-test.vzd.ti-dienste.de/owner]: https://tu-vzd-fhir-directory-test.vzd.ti-dienste.de/owner (&93834771081080)
[https://vzd-fhir-directory.vzd.ti-dienste.de/owner-authenticate]: https://vzd-fhir-directory.vzd.ti-dienste.de/owner-authenticate (&93834772249888)
[https://ru-vzd-fhir-directory-test.vzd.ti-dienste.de/owner-authenticate]: https://ru-vzd-fhir-directory-test.vzd.ti-dienste.de/owner-authenticate (&93834772251440)
[https://tu-vzd-fhir-directory-test.vzd.ti-dienste.de/owner-authenticate]: https://tu-vzd-fhir-directory-test.vzd.ti-dienste.de/owner-authenticate (&93834772252992)
[https://vzd-fhir-directory.vzd.ti-dienste.de/tim-provider-services]: https://vzd-fhir-directory.vzd.ti-dienste.de/tim-provider-services (&93834772259096)
[https://ru-vzd-fhir-directory-test.vzd.ti-dienste.de/tim-provider-services]: https://ru-vzd-fhir-directory-test.vzd.ti-dienste.de/tim-provider-services (&93834772260648)
[https://tu-vzd-fhir-directory-test.vzd.ti-dienste.de/tim-provider-services]: https://tu-vzd-fhir-directory-test.vzd.ti-dienste.de/tim-provider-services (&93834772262208)
[https://oauth.vzd.ti-dienste.de/authenticate ]: https://oauth.vzd.ti-dienste.de/authenticate%A0 (&93834772284608)
[https://ru-oauth-test.vzd.ti-dienste.de/authenticate]: https://ru-oauth-test.vzd.ti-dienste.de/authenticate (&93834772286160)
[https://tu-oauth-test.vzd.ti-dienste.de/authenticate]: https://tu-oauth-test.vzd.ti-dienste.de/authenticate (&93834772287712)
[https://gematik.de/fhir/VZD-FHIR-Directory/CodeSystem/TIMessengerCS]: https://gematik.de/fhir/VZD-FHIR-Directory/CodeSystem/TIMessengerCS (&93834801632160)
[https://owasp.org/www-project-top-ten/]: https://owasp.org/www-project-top-ten/ (&93834801645096)
[http://hapi.fhir.org/baseR4]: http://hapi.fhir.org/baseR4/Organization?address=10117&_include=Organization%3Aendpoint&_include=Organization%3Apartof&_pretty=true (&93834801470112)
