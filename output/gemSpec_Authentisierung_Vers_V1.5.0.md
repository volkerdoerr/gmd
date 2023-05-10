
Elektronische Gesundheitskarte und Telematikinfrastruktur

### Spezifikation Authentisierung des Versicherten ePA

- Klassifizierung: öffentlich
- Referenzierung: gemSpec_Authentisierung_Vers
- Revision: 548770
- Stand: 31.01.2022
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
18.12.18

</td><td>
</td><td>
initiale Erstellung

</td><td>
gematik

</td></tr><tr><td>
1.1.0

</td><td>
15.05.19

</td><td>
</td><td>
Einarbeitung Änderungsliste P18.1

</td><td>
gematik

</td></tr><tr><td>
1.2.0

</td><td>
02.03.20

</td><td>
Einarbeitung Änderungsliste P21.1

</td><td>
gematik

</td></tr><tr><td>
1.2.1

</td><td>
26.05.20

</td><td>
Einarbeitung Änderungsliste P21.3

</td><td>
gematik

</td></tr><tr><td>
Einarbeitung offener Punkte für Release 4.0.0

</td></tr><tr><td>
1.3.0.

</td><td>
30.06.20

</td><td>
freigegeben

</td><td>
gematik

</td></tr><tr><td>
1.4.0

</td><td>
19.02.21

</td><td>
Einarbeitung Änderungsliste P22.5

</td><td>
gematik

</td></tr><tr><td>
1.4.1

</td><td>
02.06.21

</td><td>
Einarbeitung Änderungsliste ePA_Maintenance_21.1

</td><td>
gematik

</td></tr><tr><td>
1.5.0

</td><td>
31.01.22

</td><td>
Einarbeitung Änderungsliste ePA_Maintenance_21.4 und ePA_Maintenance_21.5

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
- [2] Systemkontext
- [3] Zerlegung der Komponente
- [4] Übergreifende Festlegungen
  - [4.1] Datenschutz und Datensicherheit
  - [4.2] Verwendete Standards
  - [4.3] Fehlerbehandlung
  - [4.4] Protokollierung
  - [4.5] Nicht-Funktionale Anforderungen
  - [4.6] Identifikation der Akteure
- [5] Funktionsmerkmale
  - [5.1] Authentisierung
    - [5.1.1] Schnittstellen
      - [5.1.1.1] Schnittstelle I_Authentication_Insurant
        - [5.1.1.1.1] Operation login
        - [5.1.1.1.2] Operation renew
        - [5.1.1.1.3] Operation logout
        - [5.1.1.1.4] Operation getAuditEvents
        - [5.1.1.1.5] Operation getSignedAuditEvents
    - [5.1.2] Umsetzung
      - [5.1.2.1] Schnittstelle I_Authentication_Insurant
        - [5.1.2.1.1] Operation login
        - [5.1.2.1.2] Operation Renew
        - [5.1.2.1.3] Operation Logout
        - [5.1.2.1.4] Operation getAuditEvents
        - [5.1.2.1.5] Operation getSignedAuditEvents
    - [5.1.3] Lebensdauer der Authentifizierungsbestätigung
- [6] Informationsmodell
- [7] Verteilungssicht
- [8] Anhang A – Verzeichnisse
  - [8.1] Abkürzungen
  - [8.2] Glossar
  - [8.3] Abbildungsverzeichnis
  - [8.4] Tabellenverzeichnis
  - [8.5] Referenzierte Dokumente
    - [8.5.1] Dokumente der gematik
    - [8.5.2] Weitere Dokumente

### 1 Einordnung des Dokumentes

### 1.1 Zielsetzung

Die vorliegende Spezifikation definiert die Anforderungen an die Teilkomponente
"Authentisierung Versicherter" der Komponente "Zugangsgateway" (s.a.
[gemSpec_Zugangsgateway_Vers]) des Produkttyps ePA-Aktensystem (s.a.
[gemSpec_Aktensystem]).

Die Teilkomponente "Authentisierung Versicherter" ist zuständig für die
Authentisierung von Versicherten und deren Vertretern innerhalb der
Fachanwendung ePA (s.a. [gemSysL_ePA]).

### 1.2 Zielgruppe

Das Dokument ist maßgeblich für Anbieter und Hersteller des Produkttyps
ePA-Aktensystem sowie für Anbieter und Hersteller von Produkten, die die
Schnittstellen der Teilkomponente "Authentisierung Versicherter" nutzen.

### 1.3 Geltungsbereich

Dieses Dokument enthält normative Festlegungen zur Telematikinfrastruktur des
Deutschen Gesundheitswesens. Der Gültigkeitszeitraum der vorliegenden Version
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

Spezifiziert werden in dem Dokument die von dem Produkttyp bereitgestellten
(angebotenen) Schnittstellen. Benutzte Schnittstellen werden hingegen in der
Spezifikation desjenigen Produkttypen beschrieben, der diese Schnittstelle
bereitstellt. Auf die entsprechenden Dokumente wird referenziert (siehe auch
Kapitel 8.5).

Die vollständige Anforderungslage für den Produkttyp ergibt sich aus weiteren
Konzept- und Spezifikationsdokumenten, diese sind in dem Produkttypsteckbrief
des Produkttyps ePA-Aktensystem verzeichnet.

### 1.5 Methodik

Anforderungen als Ausdruck normativer Festlegungen werden durch eine eindeutige
ID sowie die dem RFC 2119 [RFC2119] entsprechenden, in Großbuchstaben
geschriebenen deutschen Schlüsselworte MUSS, DARF NICHT, SOLL, SOLL NICHT,
KANN gekennzeichnet.

Anforderungen werden im Dokument wie folgt dargestellt:\<AFO-ID\> - \<Titel der
Afo\>Text / Beschreibung [\<=]

Dabei umfasst die Anforderung sämtliche zwischen Afo-ID und Textmarke [\<=] 
angeführten Inhalte.

### 2 Systemkontext

Die Teilkomponente "Authentisierung Versicherter" der Komponente
"Zugangsgateway" des ePA-Aktensystems ist Teil des Produkttyps ePA. Der
Systemüberblick ist in [gemSysL_ePA] dargestellt.

Von der dezentralen Fachlogik im "ePA-Frontend des Versicherten" und dem
Fachmodul ePA wird die Komponente verwendet, um die Authentifizierung von
Versicherten und deren berechtigten Vertretern zu bestätigen.

Auf Anwendungsebene findet dabei ein Dialog zwischen aufrufendem Client (C) und
der Komponente "Authentisierung Versicherter" (S) statt:

 ---> UL

Um Prüfungen durchzuführen, greift die Komponente auf Dienste der TI-Plattform
zentral zurück.

### 3 Zerlegung der Komponente

Eine weitere Untergliederung der Aufbaustruktur der Komponente ist nicht
erforderlich.

### 4 Übergreifende Festlegungen

Die Komponente "Authentisierung Versicherter" stellt eine X-User Assertion
(XUA) gemäß [IHE#ITI-40] aus.

### 4.1 Datenschutz und Datensicherheit

**A_14773 - Komponente Authentisierung Versicherter -
Authentisierungsschlüssel**

Die Komponente "Authentisierung Versicherter" MUSS die erstellten
Authentifizierungsbestätigungen mit dem privaten Schlüssel der
Ausstelleridentität ID.FD.SIG signieren. Das zugehörige Zertifikat C.FD.SIG
MUSS die Rolle "oid_epa_authn" enthalten. **[\<=]**

Hinweis: Da die Identität ID.FD.SIG nur durch das Aktensystem selbst verwendet
wird ist dafür die Schlüsselgeneration ECDSA zu verwenden (s.
[gemSpec_Krypt]).

**A_15091 - Komponente Authentisierung Versicherter - Verwendung eines HSM**

Die Komponente "Authentisierung Versicherter" MUSS das private
Schlüsselmaterial der Ausstelleridentität C.FD.SIG und der
TLS-Server-Identität C.FD.TLS-S in einem HSM speichern. **[\<=]**

Zur Absicherung der Schnittstelle muss der Transport der SOAP-Nachrichten
mittels HTTPS erfolgen. Dabei sind die Vorgaben zu TLS gem.
[gemSpec_Krypt#3.3.2] und [gemSpec_PKI#8.4.1] umzusetzen.

Die Verbindung zum ePA-Frontend des Versicherten wird auf Transportebene mit TLS
abgesichert. Auf dieser Ebene erfolgt eine serverseitige Authentisierung durch
die Komponente "Authentisierung Versicherter" wie in
[gemSpec_Zugangsgateway_Vers#Kapitel4.2] beschrieben.

Verbindungen innerhalb der TI werden ebenfalls auf Transportebene mit TLS
abgesichert. Dabei werden Zertifikate der TI verwendet.

**A_14227 - Komponente Authentisierung Versicherter - TLS-Authentisierung
innerhalb der TI**

Die Komponente "Authentisierung Versicherter" MUSS für alle innerhalb der TI
zur Verfügung gestellten Schnittstellen ausschließlich Verbindungen mit TLS
akzeptieren und dabei die einseitige Serverauthentisierung unter Nutzung des
X.509-Komponentenzertifikats für TLS C.FD.TLS-S  und der Rolle
"oid_epa_authn" umsetzen. **[\<=]**

**A_14801 - Komponente Authentisierung Versicherter - XML Schema-Validierung
für SOAP-Eingangsnachrichten**

Die Komponente "Authentisierung Versicherter" MUSS vor einer Weiterverarbeitung
sämtliche SOAP 1.2-Eingangsnachrichten einer XML Schema-Validierung
unterziehen und gemäß [SOAP] verarbeiten. Sind Nachrichten nicht wohlgeformt
oder gültig, MUSS die Komponente "Authentisierung Versicherter" die Nachricht
mit einem HTTP-Statuscode 400 gemäß [RFC7231] quittieren. **[\<=]**

**A_14777 - Komponente Authentisierung Versicherter - Prüfung des
Signaturzertifikats von Authentifizierungsbestätigungen**

Die Komponente "Authentisierung Versicherter" MUSS sicherstellen, dass
Authentifizierungsbestätigungen nur akzeptiert werden, wenn das zugehörige
Signaturzertifikat zeitlich gültig ist, nicht gesperrt wurde und nach dem
Zertifikatsprofil C.FD.SIG für  die Identität der Komponente Authentisierung
Versicherter selbst ausgestellt wurde.  Dies kann durch eine aktuell gehaltene
Konfiguration vertrauenswürdiger Zertifikate umgesetzt werden und ersetzt eine
detaillierte Prüfung des Signaturzertifikats gem. [gemSpec_TBAuth#A_15557].
**[\<=]**

**A_14780 - Komponente Authentisierung Versicherter - Aussteller von
Authentifizierungsbestätigungen**

Die Komponente "Authentisierung Versicherter" MUSS sicherstellen, dass die
Authentifizierungsbestätigung von der Komponente "Authentisierung
Versicherter" selbst ausgestellt wurde (s.a. [gemSpec_TBAuth#GS-A_5494]). 
**[\<=]**

**A_15605-01 - Komponente Authentisierung Versicherter - Ablehnung von SOAP
1.2-Nachrichten ohne UTF-8 Enkodierung**

Die Komponente "Authentisierung Versicherter" MUSS SOAP 1.2-Nachrichten mit
einem HTTP-Statuscode 415 gemäß [RFC7231] quittieren, sofern die
Zeichenkodierung im HTTP Header nicht UTF-8 benennt
(Content-Type: charset=utf-8). **[\<=]**

Diese Festlegungen zur UTF-8-Enkodierung überschreibt die Festlegungen aus
[WSIBP].

**A_15613 - Komponente Authentisierung Versicherter – Erkennung von
Denial-of-Service-Angriffen hinsichtlich dem Parsen von SOAP 1.2-Nachricht**

Die Komponente "Authentisierung Versicherter" MUSS die folgenden Angriffstypen
in eingehenden SOAP 1.2-Nachrichten erkennen und mit einem HTTP-Statuscode 400
gemäß [RFC7231] quittieren:

 ---> UL

**[\<=]**

### 4.2 Verwendete Standards

Für die Übertragung von Nachrichten an den Schnittstellen der Komponente
"Authentisierung Versicherter" wird SOAP in Verbindung mit HTTP verwendet.

**A_14352-01 - Komponente Authentisierung Versicherter - Grundlegende Standards**

Die Komponente "Authentisierung Versicherter" MUSS folgende Standards umsetzen,
soweit diese im Rahmen der zu implementierenden Operationen verwendet werden
und sofern sie nicht durch konkrete Anforderungen überschrieben werden: 

 ---> UL

**[\<=]**

Generell ist [gemSpec_Krypt] für alle Algorithmen und sonstigen
kryptographischen Vorgaben zu beachten.

Für die Schnittstellen der Komponente "Authentisierung Versicherter" werden die
in der folgenden Tabelle definierten XML-Präfixe verwendet.

<table><tr><th>
Präfix

</th><th>
Namensraum

</th><th>
Referenz

</th></tr><tr><td>
phra

</td><td>
http://ws.gematik.de/fd/phrs/

I_Authentication_Insurant/v1.1

</td><td>
</td></tr><tr><td>
phr

</td><td>
http://ws.gematik.de/fa/phr/v1.0

</td><td>
</td></tr><tr><td>
xs

</td><td>
http://www.w3.org/2001/XMLSchema

</td><td>
</td></tr><tr><td>
saml

</td><td>
urn:oasis:names:tc:SAML:2.0:assertion

</td><td>
SAML 2.0 [SAML2.0]

</td></tr><tr><td>
soap

</td><td>
http://www.w3.org/2003/05/soap-envelope

</td><td>
SOAP 1.2 [SOAP]

</td></tr><tr><td>
wsoap12

</td><td>
http://schemas.xmlsoap.org/wsdl/soap12/

</td><td>
[WSDL11SOAP12]

</td></tr><tr><td>
wsdl

</td><td>
http://schemas.xmlsoap.org/wsdl/

</td><td>
WSDL 1.1 [WSDL]

</td></tr><tr><td>
ds

</td><td>
http://www.w3.org/2000/09/xmldsig#

</td><td>
</td></tr><tr><td>
xenc

</td><td>
http://www.w3.org/2001/04/xmlenc# 

</td><td>
</td></tr><tr><td>
wst

</td><td>
http://docs.oasis-open.org/ws-sx/ws-trust/200512

</td><td>
WS-Trust 1.4 [WS-Trust]

</td></tr><tr><td>
wsu

</td><td>
http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd

</td><td>
</td></tr><tr><td>
wsaw

</td><td>
http://www.w3.org/2006/05/addressing/wsdl

</td><td>
</td></tr><tr><td>
tel

</td><td>
http://ws.gematik.de/tel/error/v2.0

</td><td>
</td></tr></table>

**A_15604 - Komponente Authentisierung Versicherter - Kodierung in UTF-8**

Die Komponente "Authentisierung Versicherter" MUSS bei der Erstellung von
XML-Fragmenten das Encoding UTF-8 verwenden. **[\<=]**

### 4.3 Fehlerbehandlung

Bei Fehlern in der internen Verarbeitung oder bei fachlichen Fehlern in der
Nutzung der bereitgestellten Schnittstellen liefert die Komponente
"Authentisierung Versicherter" Fehlermeldungen zurück. Deren Struktur hängt
davon ab, ob der Meldungsablauf auf [WS-Trust] basiert oder nicht.

Aufrufe mit Meldungen nach [WS-Trust] werden entsprechend auch mit
Fehlermeldungen gemäß dem Standard beantwortet.

Andere Aufrufe werden als SOAP-Fault gemäß [gemSpec_OM] strukturiert und
enthalten die in den Schnittstellendefinitionen angegebenen
Fehlermeldungsinhalte innerhalb einer GERROR-Struktur gemäß
[TelematikError.xsd].

**A_14415 - Komponente Authentisierung Versicherter - Verwendung von
Webservice-Fehlern**

Die Komponente "Authentisierung Versicherter" MUSS an der Schnittstelle 
I_Authentication_Insurant:login den in [WS-Trust#Kapitel11] festgelegten
SOAP-Fault-Mechanismus umsetzen. **[\<=]**

**A_15138 - Komponente Authentisierung Versicherter - Inhalte der
Fehlermeldungen**

Die Komponente "Authentisierung Versicherter" MUSS in einer GERROR-Fehlermeldung
gemäß [TelematikError.xsd] die Felder wie folgt mit den
Fehlermeldungsinhalten der Schnittstellenbeschreibung befüllen:

 ---> UL

Tabelle2:  Tab_Auth_Vers_003 - Zuordnung Fehlercodes zu Fehlernamen

Name 
        Fehlercode 
        
        
        INTERNAL_ERROR 
        7720

        
        
        SYNTAX_ERROR 
        7730 
        
        
      
 ASSERTION_INVALID 
        7740 **[\<=]**

### 4.4 Protokollierung

Die Anforderungen an die Protokollierung für die Komponente leiten sich
aus [gemSysL_ePA#2.5.5] ab.

**A_13877-01 - Komponente Authentisierung Versicherter -
Verwaltungsprotokollierung**

Die Komponente "Authentisierung Versicherter" MUSS beim Aufruf einer der in []
aufgelisteten Operationen der Schnittstelle I_Authentication_Insurant unter
der Voraussetzung, dass der Aufruf erfolgreich war, je einen Eintrag im
Verwaltungsprotokoll für den Versicherten gemäß [] vornehmen und die
Parameterwerte dabei wie folgt setzen:

Tabelle3: Tab_Auth_Vers_004 - Operationsabhängige Parameter des
Verwaltungsprotokolls

<table><tr><th>
Protokoll-parameter

</th><th colspan="2">
Parameterwerte gemäß aufgerufener Operation

</th></tr><tr><td>
UserID

</td><td colspan="2">
KVNR;  
Ermittlung für Operation  
I_Authentication_Insurant::getAuditEvents, 

I_Authentication_Insurant::getSignedAuditEvents, 

I_Authentication_Insurant::logoutToken  
über den folgenden XPath-Ausdruck
zur "Subject ID" der im Operationsaufruf übergebenen Authentication Assertion:
 
//*[local-name()='Assertion' and namespace-uri() =
'urn:oasis:names:tc:SAML:2.0:assertion']//*[local-name()='Attribute' and
namespace-uri() = 'urn:oasis:names:tc:SAML:2.0:assertion'][@Name=
'urn:gematik:subject:subject-id']/*[local-name()='AttributeValue']/*[local-name()='InstanceIdentifier']/data(@extension)

Ermittlung für die Operation I_Authentication_Insurant::loginCreateToken aus
dem Inhalt des Elements

SubjectDN des bestätigten C.CH.AUT bzw. C.CH.AUT_ALT Zertifikats, siehe Kap.
 ).

</td></tr><tr><td>
UserName

</td><td colspan="2">
Name des Nutzers;  
Ermittlung für Operation 

I_Authentication_Insurant::getAuditEvents, 

I_Authentication_Insurant::getSignedAuditEvents, 

I_Authentication_Insurant::logoutToken über den folgenden XPath-Ausdruck zur
Behauptung "name" , der im Operationsaufruf übergebenen Authentication
Assertion:  
//*[local-name()='Assertion' and namespace-uri() =
'urn:oasis:names:tc:SAML:2.0:assertion']//*[local-name()='Attribute' and
namespace-uri() =
'urn:oasis:names:tc:SAML:2.0:assertion'][@Name='http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name']/*[local-name()='AttributeValue']

Ermittlung für die Operation I_Authentication_Insurant::loginCreateToken aus
dem Inhalt des Elements

commonName

aus

subjectDN 

des übergebenen

C.CH.AUT bzw. C.CH.AUT_ALT Zertifikats.

</td></tr><tr><td>
ObjectID

</td><td colspan="2">
[nicht belegt]

</td></tr><tr><td>
ObjectName

</td><td colspan="2">
[nicht belegt]

</td></tr><tr><td>
DeviceID

</td><td colspan="2">
[nicht belegt]

</td></tr><tr><td rowspan="3">
ObjectDetail

</td><td colspan="2">
gilt nur bei Operation I_Authentication_Insurant::loginCreateToken:

</td></tr><tr><td>
type

</td><td>
value

</td></tr><tr><td>
AuthenticationType

</td><td>
"eGK", wenn policyIdentifier = \<oid_egk_aut\>

"alternative Authentisierung", wenn policyIdentifier = \<oid_egk_aut_alt\>

policyIdentifier ist enthalten in Element Extensions/CertificatePolicies des
übergebenen C.CH.AUT bzw. C.CH.AUT_ALT Zertifikats

</td></tr><tr><td>
übrige Protokolldaten

</td><td colspan="2">
s. []

</td></tr></table>

Die nicht in [

] aufgelisteten Operationen der Schnittstelle I_Authentication_Insurant werden
nicht protokolliert. **[\<=]**

Zur Protokollierung sind auch die Vorgaben in [gemSpec_Aktensystem#5.2] zu
beachten.

**A_21104-01 - Komponente Authentisierung Versicherter -
Verwaltungsprotokollierung, wenn loginCreateToken fehlschlägt**

Fallsder Aufruf der Operation loginCreateToken fehl schlägt, MUSS die
Komponente "Authentisierung Versicherter" einen Eintrag im Verwaltungsprotokoll
für den Versicherten bzw. seinen Vertreter gemäß [] vornehmen und
zusätzlich zu den Vorgaben vonA_13877 die Parameterwerte wie
in Tab_Auth_Vers_0016 setzen. Es wird die Gesamtanzahl der fehlgeschlagenen
Aufrufe der Operation loginCreateToken jeweils für eGK und al.vi gezählt und
genau ein Protokolleintrag je Datumstag geschrieben.

Tabelle4: Tab_Auth_Vers_0016- Operationsabhängige Parameter des
Verwaltungsprotokolls bei fehlerhaftem Aufruf der Operation loginCreateToken

<table><tr><th>
Protokoll-parameter

</th><th colspan="2">
Parameterwerte gemäß aufgerufener Operation

</th></tr><tr><td colspan="1" rowspan="5">
ObjectDetail

</td><td colspan="1" rowspan="2">
type

</td><td colspan="1" rowspan="2">
value

</td></tr><tr></tr><tr><td>
ErrorCounter_eGK

</td><td>
Anzahl der fehlgeschlagenen Aufrufe der Operation loginCreateToken mit eGK
(policyIdentifier = \<oid_egk_aut\>) für diesen Tag korrespondierend
zu phr:AuditMessage/phr:EventIdentification/@EventDateTime

</td></tr><tr><td>
ErrorCounter_alvi

</td><td>
Anzahl der fehlgeschlagenen Aufrufe der Operation loginCreateToken mit al.vi
(policyIdentifier = \<oid_egk_aut_alt\>)für diesen Tag korrespondierend
zu phr:AuditMessage/phr:EventIdentification/@EventDateTime

</td></tr><tr><td>
ErrorCounter_unknown

</td><td>
Anzahl der fehlgeschlagenen Aufrufe der Operation loginCreateToken mit
unbekanntem policyIdentifier (keine Rolle oder nur eine unbekannte Rollen-OID)
für diesen Tag korrespondierend zu

phr:AuditMessage/phr:EventIdentification/@EventDateTime

</td></tr></table>

**[\<=]**

### 4.5 Nicht-Funktionale Anforderungen

Die die Komponente "Authentisierung Versicherter" betreffenden Anforderungen
zu Skalierbarkeit, Performance und Mengengerüst sind in [gemSpec_Perf] zu
finden.

### 4.6 Identifikation der Akteure

Der Versicherte bzw. der von ihm berechtigte Vertreter im Sinne der
Fachanwendung ePA werden über ihre Krankenversichertennummer (KVNR) eindeutig
identifiziert (vgl. [gemSysL_ePA#2.4.1]. Die KVNR besteht aus einem
unveränderlichen Teil (Versicherten-ID) und einem veränderlichen Teil. In
diesem Dokument ist mit der Abkürzung KVNR immer nur der unveränderliche Teil
(Versicherten-ID) gemeint.

In den Zertifikaten einer eGK bzw. einer alternativen Versichertenidentität ist
der unveränderliche Teil der KVNR in einem Feld organizationalUnitName des
SubjectDN enthalten (s. [gemSpec_PKI#5.1]). Dabei ist zu beachten, dass das
Feld organizationalUnitName im SubjectDN in zwei Ausprägungen auftritt (s.
[gemSpec_PKI#4.2]):

 ---> UL

Demzufolge muss für Versicherte bzw. deren berechtigte Vertreter der
unveränderliche Teil der KVNR aus dem zehnstelligen alphanumerischen Feld
organizationalUnitName von den Zertifikaten entnommen und zur Identifikation
herangezogen werden.

### 5 Funktionsmerkmale

Die Komponente Authentisierung Versicherter realisiert ein Funktionsmerkmal
über eine Schnittstelle:

<table><tr><th>
Schnittstelle

</th><th colspan="2">
Beschreibung und Operationen

</th></tr><tr><td colspan="1" rowspan="7">
I_Authentication_Insurant

</td><td colspan="2">
Schnittstelle zur Authentifizierung eines Versicherten

</td></tr><tr><td>
Logische Operation

</td><td>
Beschreibung

</td></tr><tr><td>
login

</td><td>
Authentifizierung eines Versicherten

</td></tr><tr><td>
renew

</td><td>
Erneuern der Authentifizierungsbestätigung für einen Versicherten auf Basis
einer vorliegenden Authentifizierungsbestätigung

</td></tr><tr><td>
logout

</td><td>
Beenden der Erneuerbarkeit der Authentifizierungsbestätigung für einen
Versicherten

</td></tr><tr><td>
getAuditEvents

</td><td>
Abruf der Verwaltungsprotokolleinträge

</td></tr><tr><td>
getSignedAuditEvents

</td><td>
Abruf der signierten Liste des Verwaltungsprotokolls

</td></tr></table>

Die Operation 'login' wird sowohl zur initialen Erstellung der
Authentifizierungsbestätigung als auch nach Ablauf der Gültigkeit der
ursprünglichen Authentifizierungsbestätigung zur Erstellung einer neuen
Authentifizierungsbestätigung aufgerufen.Die Operation 'renew' erstellt eine
neue Authentifizierungsbestätigung, wenn eine gültige
Authentifizierungsbestätigung vorgelegt wird, zu der noch kein 'logout'
stattgefunden hat.Die Operation 'logout' beendet die Erneuerbarkeit einer
Authentifizierungsbestätigung.

Die Komponente "Authentisierung Versicherter" nutzt die in der folgenden Tabelle
aufgeführten Schnittstellen der Telematikinfrastruktur.

<table><tr><th>
Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td>
I_IP_Transport

</td><td>
Definition in [gemSpec_Net]

</td></tr><tr><td>
I_DNS_Name_Resolution

</td><td>
Definition in [gemSpec_Net]

</td></tr><tr><td>
I_NTP_Time_Information

</td><td>
Definition in [gemSpec_Net]

</td></tr><tr><td>
I_OCSP_Status_Information

</td><td>
Definition in [gemSpec_PKI]

</td></tr><tr><td>
I_TSL_Download

</td><td>
Definition in [gemSpec_TSL]

</td></tr><tr><td>
I_Cert_provisioning

</td><td>
Definition in [gemSpec_X.509_TSP]

</td></tr><tr><td>
I_Cert_Revocation

</td><td>
Definition in [gemSpec_X.509_TSP]

</td></tr></table>

### 5.1 Authentisierung

### 5.1.1 Schnittstellen

### 5.1.1.1 Schnittstelle I_Authentication_Insurant

Das Interface I_Authentication_Insurant stellt die in [gemSysL_ePA] definierte
Schnittstelle bereit.

**A_14228-01 - Komponente Authentisierung Versicherter -
I_Authentication_Insurant**

Die Komponente "Authentisierung Versicherter" MUSS einen
Webservice-EndpunktI_Authentication_Insurant bereitstellen, welcher
die logischen Schnittstellen
I_Authentication_Insurant:login, I_Authentication_Insurant:renew
und I_Authentication_Insurant:logout nach WS-Trust und die Schnittstellen
I_Authentication_Insurant:getAuditEvents
und I_Authentication_Insurant:getSignedAuditEvents zum Abruf von
Protokolldaten durch die folgenden angebotenen Operationen realisiert:

Tabelle7: Tab_Auth_Vers_007 - Schnittstellenübersicht der Authentisierung des
Versicherten

<table><tr><th>
Name

</th><th colspan="2">
I_Authentication_Insurant

</th></tr><tr><td>
Version

</td><td colspan="2">
1.2

</td></tr><tr><td>
Namensraum

</td><td colspan="2">
http://docs.oasis-open.org/ws-sx/ws-trust/200512

</td></tr><tr><td colspan="1" rowspan="7">
Operationen

</td><td>
Name

</td><td>
Kurzbeschreibung

</td></tr><tr><td>
LoginCreateChallenge

</td><td>
Login Teil 1  
Request: RequestSecurityToken  
Response:
RequestSecurityTokenResponse mit einer SignChallenge

</td></tr><tr><td>
LoginCreateToken

</td><td>
Login Teil 2  
Request: RequestSecurityTokenResponse mit einer
SignChallengeResponse  
Response: RequestSecurityTokenResponseCollection

</td></tr><tr><td>
RenewToken

</td><td>
Renew  
Request: RequestSecurityToken  
Response: RequestSecurityTokenResponse

</td></tr><tr><td>
LogoutToken

</td><td>
Logout  
Request: RequestSecurityToken  
Response: RequestSecurityTokenResponse

</td></tr><tr><td>
getAuditEvents

</td><td>
getAuditEvents - Abruf Verwaltungsprotokoll

Request:

GetAuditEvents

Response: 

GetAuditEventsResponse

</td></tr><tr><td>
getSignedAuditEvents

</td><td>
getSignedAuditEvents - Abruf  signiertes Verwaltungsprotokoll

Request:

GetSignedAuditEvents

Response: 

GetSignedAuditEventsResponse

</td></tr><tr><td>
WSDL

</td><td colspan="2">
AuthenticationService.wsdl

</td></tr></table>

Die als SAML-Assertion zurückgelieferte Authentifizierungsbestätigung ist zur
Vorlage bei den im Element

Audience

(s. Kap. 5.1.2.1.1) angegeben Webservices bestimmt und kann durch den Aufrufer
als opakes Token behandelt werden. Es ist mit der Identität der Komponente
"Authentisierung Versicherter" signiert. **[\<=]**

### 5.1.1.1.1 Operation login

Die Operation dient der Ausstellung von Authentifizierungsbestätigungen für
Versicherte auf der Basis des Zertifikats C.CH.AUT oder C.CH.AUT_ALT des
Versicherten.

Die Authentifizierungsbestätigung hat folgende wesentlichen Eigenschaften:

 ---> UL

Voraussetzung für den Dialog auf Anwendungsebene ist eine etablierte
TLS-Verbindung auf Transportebene.

Analog zu [WS-Trust#8] wird auf Anwendungsebene ein Signature Challenge Dialog
implementiert. Abweichend von  [WS-Trust#8.2] bzw. [WS-Trust#Appendix B]
liegt der Endpunkt auch für den Austausch der Signaturchallenge auf der Seite
der Komponente "Authentisierung Versicherter", d.h. der Meldungsablauf ist in
zwei durch den Aufrufer initiierte Meldungspaare aufgeteilt, deren Inhalte
gemäß [WS-Trust] strukturiert sind.

Die logische Operation Login setzt sich daher auf Ebene der Webservices aus
einer Abfolge der zwei Operationen LoginCreateChallenge und LoginCreateToken
zusammen.

Die Fehlerbehandlung für diese beiden Operationen wird gemäß [WS-Trust#11]
durchgeführt (vgl. Kap. 4.3).

Im Request zur Operation LoginCreateToken wird die Signatur des Versicherten
über die von der Komponente "Authentisierung Versicherter" erstellten
Challenge übertragen. Diese Übertragung erfolgt per WS-Security im
SOAP-Header.

Die Bestückung der Nachrichtenfelder wird an einem Beispiel illustriert und
dann normativ festgelegt.Beispiel Dialog

LoginCreateChallenge, Request:

\<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope"\> 
\<soap:Header\>    \<Action
xmlns="http://www.w3.org/2005/08/addressing"\>http://docs.oasis-open.org/ws-sx/ws-trust/200512/RST/Issue\</Action\> 
  \<To
xmlns="http://www.w3.org/2005/08/addressing"\>https://localhost:9094/authn\</To\> 
\</soap:Header\>  \<soap:Body\>    \<RequestSecurityToken
xmlns="http://docs.oasis-open.org/ws-sx/ws-trust/200512"\>     
\<TokenType\>http://docs.oasis-open.org/wss/oasis-wss-saml-token-profile-1.1#SAMLV2.0\</TokenType\> 
   
\<RequestType\>http://docs.oasis-open.org/ws-sx/ws-trust/200512/Issue\</RequestType\> 
  \</RequestSecurityToken\>  \</soap:Body\>\</soap:Envelope\>

LoginCreateChallenge, Response:

\<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope"\> 
\<soap:Header\>    \<Action
xmlns="http://www.w3.org/2005/08/addressing"\>http://docs.oasis-open.org/ws-sx/ws-trust/200512/RSTR/Challenge\</Action\> 
  \<To
xmlns="http://www.w3.org/2005/08/addressing"\>http://www.w3.org/2005/08/addressing/anonymous\</To\> 
\</soap:Header\>

  \<soap:Body\>    \<RequestSecurityTokenResponse
xmlns="http://docs.oasis-open.org/ws-sx/ws-trust/200512"\>     
\<SignChallenge\>        \<Challenge\>JemuBWS...\</Challenge\>     
\</SignChallenge\>    \</RequestSecurityTokenResponse\> 
\</soap:Body\>\</soap:Envelope\>

LoginCreateToken, Request:

\<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope"\> 
\<soap:Header\>    \<wsse:Security
xmlns:wsse="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd"
xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd"
soap:mustUnderstand="true"\>      \<wsse:BinarySecurityToken
EncodingType="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-soap-message-security-1.0#Base64Binary"
ValueType="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-x509-token-profile-1.0#X509v3"
wsu:Id="X509-c3b3a51c-a22b-4682-85a2-5537d56ba5e2"\>MIIEzTCCA7WgA...\</wsse:BinarySecurityToken\> 
    \<ds:Signature xmlns:ds="http://www.w3.org/2000/09/xmldsig#"
Id="SIG-f1f0472f-2f0d-468d-b425-0b1f5c78cc5a"\>        \<ds:SignedInfo\> 
        \<ds:CanonicalizationMethod
Algorithm="http://www.w3.org/2001/10/xml-exc-c14n#"\>           
\<ec:InclusiveNamespaces xmlns:ec="http://www.w3.org/2001/10/xml-exc-c14n#"
PrefixList="soap"/\>          \</ds:CanonicalizationMethod\>         
\<ds:SignatureMethod
Algorithm="http://www.w3.org/2007/05/xmldsig-more#sha256-rsa-MGF1"/\>     
    \<ds:Reference URI="#id-6c68f4bd-153d-42fb-a640-890c5cc14771"\>     
      \<ds:Transforms\>              \<ds:Transform
Algorithm="http://www.w3.org/2001/10/xml-exc-c14n#"/\>           
\</ds:Transforms\>            \<ds:DigestMethod
Algorithm="http://www.w3.org/2001/04/xmlenc#sha256"/\>           
\<ds:DigestValue\>9Et/DvvJ1Sb0Z1SEequKHmOYTEizKYCKZlAEiDILGFU=\</ds:DigestValue\> 
        \</ds:Reference\>        \</ds:SignedInfo\>       
\<ds:SignatureValue\>P21t+FT2tA...\</ds:SignatureValue\>       
\<ds:KeyInfo Id="KI-bd93fc63-8828-46ad-8a6c-df08acabe5ce"\>         
\<wsse:SecurityTokenReference
xmlns:wsse="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd"
xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd"
wsu:Id="STR-d16144ef-1a31-45b8-b061-537a93fbd515"\>           
\<wsse:Reference URI="#X509-c3b3a51c-a22b-4682-85a2-5537d56ba5e2"
ValueType="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-x509-token-profile-1.0#X509v3"/\> 
        \</wsse:SecurityTokenReference\>        \</ds:KeyInfo\>     
\</ds:Signature\>    \</wsse:Security\>

    \<Action
xmlns="http://www.w3.org/2005/08/addressing"\>http://docs.oasis-open.org/ws-sx/ws-trust/200512/RSTR/ChallengeFinal\</Action\> 
  \<To
xmlns="http://www.w3.org/2005/08/addressing"\>https://localhost:9094/authn\</To\> 
\</soap:Header\>  \<soap:Body
xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd"
wsu:Id="id-6c68f4bd-153d-42fb-a640-890c5cc14771"\> 

    \<RequestSecurityTokenResponse
xmlns="http://docs.oasis-open.org/ws-sx/ws-trust/200512"\>     
\<SignChallengeResponse\>        \<Challenge\>JemuBWS-...\</Challenge\> 
    \</SignChallengeResponse\>    \</RequestSecurityTokenResponse\> 
\</soap:Body\>\</soap:Envelope\>

LoginCreateToken, Response:

\<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope"\> 
\<soap:Header\>    \<Action
xmlns="http://www.w3.org/2005/08/addressing"\>http://docs.oasis-open.org/ws-sx/ws-trust/200512/RSTRC/IssueFinal\</Action\> 
  \<To
xmlns="http://www.w3.org/2005/08/addressing"\>http://www.w3.org/2005/08/addressing/anonymous\</To\> 
\</soap:Header\>

  \<soap:Body\>    \<RequestSecurityTokenResponseCollection
xmlns="http://docs.oasis-open.org/ws-sx/ws-trust/200512"\>     
\<RequestSecurityTokenResponse\>        \<RequestedSecurityToken\>     
    \<saml2:Assertion ...\> ...                 
\</saml2:Assertion\>        \</RequestedSecurityToken\>     
\</RequestSecurityTokenResponse\>   
\</RequestSecurityTokenResponseCollection\>  \</soap:Body\>\</soap:Envelope\>

Normative Festlegung zum Dialog

**A_14053 - Komponente Authentisierung Versicherter -
I_Authentication_Insurant:login nach WS-Trust, LoginCreateChallenge**

Die Komponente "Authentisierung Versicherter" MUSS die
OperationLoginCreateChallengewie folgt anbieten:

Tabelle8: Tab_Auth_Vers_008 - Signatur der Schnittstelle
I_Authentication_Insurant:loginCreateChallenge

<table><tr><th>
Operation

</th><th colspan="3">
loginCreateChallenge

</th></tr><tr><td>
Beschreibung

</td><td colspan="3">
Login Teil 1 (Erzeugen der Challenge)

Request: RequestSecurityToken

Response: RequestSecurityTokenResponse mit einer SignChallenge

</td></tr><tr><td colspan="4">
Eingangsparameter

</td></tr><tr><td>
 Name

</td><td>
 Beschreibung

</td><td>
Typ

</td><td>
opt.

</td></tr><tr><td>
/RequestSecurityToken

</td><td>
Request Security Token

</td><td>
n

</td></tr><tr><td>
/RequestSecurityToken

/TokenType

</td><td>
Typ des Security Tokens.

Wert:

http://docs.oasis-open.org/wss/oasis-wss-saml-token-profile-1.1#SAMLV2.0

 

</td><td>
</td><td>
n

</td></tr><tr><td>
/RequestSecurityToken

/RequestType

</td><td>
Angeforderte Funktion des Requests.

Wert:

http://docs.oasis-open.org/ws-sx/ws-trust/200512/Issue

 

</td><td>
</td><td>
n

</td></tr><tr><td colspan="4">
Ausgangsparameter

</td></tr><tr><td>
 Name

</td><td>
Beschreibung

</td><td>
Typ

</td><td>
opt.

</td></tr><tr><td>
/RequestSecurityToken

Response

</td><td>
</td><td>
</td><td>
n

</td></tr><tr><td>
/RequestSecurityToken

Response

/SignChallenge

</td><td>
n

</td></tr><tr><td>
/RequestSecurityToken

Response

/SignChallenge

/Challenge

</td><td>
Enthält einen Zufallswert.

Der Inhalt wird vom Aufrufer nicht ausgewertet.

</td><td>
String

</td><td>
n

</td></tr><tr><td colspan="4">
Fehlermeldungen 

</td></tr><tr><td>
Fault/Code/Subcode/Value

</td><td>
Fault/Reason/Text

</td><td colspan="2">
Details

</td></tr><tr><td>
wst:RequestFailed

</td><td>
The specified request failed

</td><td colspan="2">
Interner Fehler in der Verarbeitungslogik

</td></tr><tr><td>
wst:InvalidRequest

</td><td>
The request was invalid or malformed 

</td><td colspan="2">
Es wurde ein fehlerhafter Aufrufparameter übergeben.

</td></tr></table>

**[\<=]**

**A_14059 - Komponente Authentisierung Versicherter -
I_Authentication_Insurant:login nach WS-Trust, LoginCreateToken**

Die Komponente "Authentisierung Versicherter" MUSS die
OperationLoginCreateTokenwie folgt anbieten:

Tabelle9:  Tab_Auth_Vers_009 - Signatur der Schnittstelle
I_Authentication_Insurant:loginCreateToken

<table><tr><th>
Operation

</th><th colspan="3">
loginCreateToken

</th></tr><tr><td>
Beschreibung

</td><td colspan="3">
Login Teil 2

Request: RequestSecurityTokenResponse mit einer SignChallengeResponse

Response: RequestSecurityTokenResponseCollection

</td></tr><tr><td colspan="4">
Eingangsparameter

</td></tr><tr><td>
 Name

</td><td>
Beschreibung

</td><td>
Typ

</td><td>
opt.

</td></tr><tr><td>
/wsse:Security

</td><td>
Der WSSE SOAP Header enthält die Signatur über den Body

sowie das zugehörige Zertifikat.

</td><td>
</td><td>
n

</td></tr><tr><td>
/wsse:Security

/wsse:BinarySecurityToken

</td><td>
Zertifikat C.CH.AUT

oder C.CH.AUT_ALT

als BinarySecurityToken (s. [WSS#Kapitel6.3])

Hinweis: dabei kann es sich um ein Zertifikat der Schlüsselgeneration RSA oder
ECDSA handeln (vgl. [gemSpec_Krypt]).

</td><td>
</td><td>
n

</td></tr><tr><td>
/wsse:Security

/ds:Signature

</td><td>
Signatur über den SOAP Body durch die Identität ID.CH.AUT

bzw. ID.CH.AUT_ALT  und Referenz auf das Zertifikat (s. [WSS#Kapitel8] und
[WSS-X509#Kapitel3.2]) 

</td><td>
</td><td>
n

</td></tr><tr><td>
/RequestSecurityTokenResponse

</td><td>
</td><td>
</td><td>
n

</td></tr><tr><td>
/RequestSecurityTokenResponse

/SignChallengeResponse

/Challenge

</td><td>
Unveränderter Wert der vom Aufrufer in der Meldung zuvor empfangenen Challenge.

</td><td>
</td><td>
n

</td></tr><tr><td colspan="4">
Ausgangsparameter

</td></tr><tr><td>
 Name

</td><td>
Beschreibung

</td><td>
Typ

</td><td>
opt.

</td></tr><tr></tr><tr><td>
/RequestSecurityTokenResponseCollection

</td><td>
</td><td>
</td><td>
</td></tr><tr><td>
/RequestSecurityToken

ResponseCollection

/RequestSecurityToken

Response

</td><td>
</td><td>
</td><td>
</td></tr><tr><td>
/RequestSecurityToken

ResponseCollection

/RequestSecurityToken

Response

/RequestedSecurityToken

</td><td>
Dieser Parameter MUSS die in Kap. 5.1.2.1.1 definierte SAML Assertion enthalten

Die Signatur der Komponente Authentisierung

Versicherter

ist in der SAML Assertion enthalten.

</td><td>
</td><td>
</td></tr><tr><td>
/RequestSecurityToken

ResponseCollection

/RequestSecurityToken

Response

/RequestedSecurityToken

/saml2:Assertion

</td><td>
Angeforderte AuthenticationAssertion als SAML Assertion

</td><td>
</td><td>
</td></tr><tr><td colspan="4">
Fehlermeldungen 

</td></tr><tr><td>
Fault/Code/Subcode/Value

</td><td>
Fault/Reason/Text

</td><td colspan="2">
Details

</td></tr><tr><td>
wst:RequestFailed

</td><td>
The specified request failed  

</td><td colspan="2">
Interner Fehler in der Verarbeitungslogik

</td></tr><tr><td>
wst:InvalidRequest

</td><td>
The request was invalid or malformed

</td><td colspan="2">
Es wurde ein fehlerhafter Aufrufparameter übergeben oder die Signatur der
Eingangsnachricht ist nicht korrekt.

</td></tr><tr><td>
wst:InvalidSecurityToken

</td><td>
Security token has been revoked

</td><td colspan="2">
Das als BinarySecurityToken übergebene Zertifikat ist ungültig oder gesperrt.

</td></tr></table>

**[\<=]**

**A_14350 - Komponente Authentisierung Versicherter -
I_Authentication_Insurant:login, Challenge Response Prüfung**

Die Komponente "Authentisierung Versicherter" MUSS sicherstellen, dass die in
der SignChallengeResponseverwendeteChallengefolgende Eigenschaften hat:

 ---> UL

**[\<=]**

**A_18985-03 - ePA-Client: Prüfen der AuthenticationAssertion**

Ein ePA-Client (ePA-Frontend des Versicherten, ePA FM etc.) MUSS beim Erhalt
des Authenticationtokens (AuthenticationAssertion) vergleichen, ob sich die
KVNR als eineindeutiges Merkmal des Nutzers, welcher sich gegenüber dem
Aktensystem authentifiziert hat, in den Behauptungen mit saml2:Attribute
Name="urn:gematik:subject:subject-id" wiederfindet (vgl. A_18985-Beispiel-1).

Falls die Prüfung ein negatives Ergebnis liefert, so MUSS der ePA-Client den
Vorgang (Einloggen ins Aktensystem) abbrechen. **[\<=]**

A_18985-Beispiel-1:

\<saml2:Assertion xmlns:saml2="urn:oasis:names:tc:SAML:2.0:assertion"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
ID="_3886aa57-deb8-422d-b0f8-54ff207d089a"
IssueInstant="2020-05-11T16:59:53.420Z" Version="2.0"
xsi:type="saml2:AssertionType"\>  
   
\<saml2:Issuer\>https://aktor-gateway.gematik.de/authn\</saml2:Issuer\>  
   
\<ds:Signature xmlns:ds="http://www.w3.org/2000/09/xmldsig#"\>  
      … 

    \</ds:Signature\>  
    \<saml2:Subject\>  
        \<saml2:NameID
Format="urn:oasis:names:tc:SAML:1.1:nameid-format:X509SubjectName"\>CN=Dr.
Emilio von BurgundTEST-ONLY, T=Dr., GIVENNAME=Emilio von, SURNAME=Burgund,
OU=109500969, OU=X110474929, O=Test GKV-SVNOT-VALID, C=DE\</saml2:NameID\>  
 
      \<saml2:SubjectConfirmation
Method="urn:oasis:names:tc:SAML:2.0:cm:bearer"/\>  
    \</saml2:Subject\> 

    \<saml2:Conditions NotBefore="2020-05-11T16:59:53.420Z"
NotOnOrAfter="2020-05-11T17:04:53.420Z"\>  
       
\<saml2:AudienceRestriction\>  
           
\<saml2:Audience\>https://aktor-gateway.gematik.de\</saml2:Audience\>  
   
    \</saml2:AudienceRestriction\>  
    \</saml2:Conditions\>  
   
\<saml2:AuthnStatement AuthnInstant="2020-05-11T16:53:53.322Z"\>  
       
\<saml2:AuthnContext\>  
           
\<saml2:AuthnContextClassRef\>urn:oasis:names:tc:SAML:2.0:ac:classes:SmartcardPKI\</saml2:AuthnContextClassRef\>
 
        \</saml2:AuthnContext\>  
    \</saml2:AuthnStatement\>  
   
\<saml2:AttributeStatement\>  
        \<saml2:Attribute
Name="http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name"
NameFormat="urn:oasis:names:tc:SAML:2.0:attrname-format:uri"\>  
         
  \<saml2:AttributeValue xsi:type="xsd:string"\>Dr. Emilio von
BurgundTEST-ONLY\</saml2:AttributeValue\>  
        \</saml2:Attribute\> 

        \<saml2:Attribute
Name="http://schemas.xmlsoap.org/ws/2005/05/identity/claims/givenname"
NameFormat="urn:oasis:names:tc:SAML:2.0:attrname-format:uri"\>  
         
  \<saml2:AttributeValue xsi:type="xsd:string"\>Emilio
von\</saml2:AttributeValue\>  
        \</saml2:Attribute\>  
       
\<saml2:Attribute
Name="http://schemas.xmlsoap.org/ws/2005/05/identity/claims/surname"
NameFormat="urn:oasis:names:tc:SAML:2.0:attrname-format:uri"\>  
         
  \<saml2:AttributeValue
xsi:type="xsd:string"\>Burgund\</saml2:AttributeValue\>  
       
\</saml2:Attribute\>  
        \<saml2:Attribute
Name="http://schemas.xmlsoap.org/ws/2005/05/identity/claims/country"
NameFormat="urn:oasis:names:tc:SAML:2.0:attrname-format:uri"\>  
         
  \<saml2:AttributeValue xsi:type="xsd:string"\>DE\</saml2:AttributeValue\> 

        \</saml2:Attribute\>  
        \<saml2:Attribute
Name="http://schemas.xmlsoap.org/ws/2005/05/identity/claims/nameidentifier"
NameFormat="urn:oasis:names:tc:SAML:2.0:attrname-format:uri"\>  
         
  \<saml2:AttributeValue
xsi:type="xsd:string"\>X110474929\</saml2:AttributeValue\>  
       
\</saml2:Attribute\>  
        \<saml2:Attribute
Name="urn:gematik:subject:subject-id"
NameFormat="urn:oasis:names:tc:SAML:2.0:attrname-format:uri"\>  
         
  \<saml2:AttributeValue\>  
                \<InstanceIdentifier
xmlns="urn:hl7-org:v3" extension="X110474929" root="1.2.276.0.76.4.8"/\>  
 
          \</saml2:AttributeValue\>  
        \</saml2:Attribute\> 

    \</saml2:AttributeStatement\>  
\</saml2:Assertion\>

### 5.1.1.1.2 Operation renew

Die Operation dient der Erneuerung einer Authentifizierungsbestätigung.

Die Bestückung der Nachrichtenfelder wird an einem Beispiel illustriert und
dann normativ festgelegt.Beispiel Dialog

RenewToken, Request:

\<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope"\> 
\<soap:Header\>    \<Action
xmlns="http://www.w3.org/2005/08/addressing"\>http://docs.oasis-open.org/ws-sx/ws-trust/200512/RST/Renew\</Action\> 
  \<To xmlns="http://www.w3.org/2005/08/addressing"\>...\</To\> 
\</soap:Header\>

\<soap:Body\>    \<RequestSecurityToken
xmlns="http://docs.oasis-open.org/ws-sx/ws-trust/200512"\>     
\<TokenType\>http://docs.oasis-open.org/wss/oasis-wss-saml-token-profile-1.1#SAMLV2.0\</TokenType\> 
   
\<RequestType\>http://docs.oasis-open.org/ws-sx/ws-trust/200512/Renew\</RequestType\> 
    \<RenewTarget\>... the token to be renewed ...\</RenewTarget\>   
\</RequestSecurityToken\>  \</soap:Body\>\</soap:Envelope\>

RenewToken, Response:

\<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope"\>

  \<soap:Header\>    \<Action
xmlns="http://www.w3.org/2005/08/addressing"\>http://docs.oasis-open.org/ws-sx/ws-trust/200512/RSTR/RenewFinal\</Action\> 
  \<To xmlns="http://www.w3.org/2005/08/addressing"\>...\</To\> 
\</soap:Header\>

  \<soap:Body\>    \<RequestSecurityTokenResponse
xmlns="http://docs.oasis-open.org/ws-sx/ws-trust/200512"\>     
\<RequestedSecurityToken\> ... the new token ... \</RequestedSecurityToken\> 
  \</RequestSecurityTokenResponse\>  \</soap:Body\>\</soap:Envelope\>

**A_17392-01 - Komponente Authentisierung Versicherter -
I_Authentication_Insurant:renew nach WS-Trust, RenewToken**

Die Komponente "Authentisierung Versicherter" MUSS die Operation renew wie folgt
anbieten: **[\<=]**

### 5.1.1.1.3 Operation logout

Die Operation beendet die Erneuerbarkeit einer Authentifizierungsbestätigung.

Die Bestückung der Nachrichtenfelder wird an einem Beispiel illustriert und
dann normativ festgelegt.Beispiel Dialog

LogoutToken, Request:

\<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope"\> 
\<soap:Header\>    \<Action
xmlns="http://www.w3.org/2005/08/addressing"\>http://docs.oasis-open.org/ws-sx/ws-trust/200512/RST/Cancel\</Action\> 
  \<To xmlns="http://www.w3.org/2005/08/addressing"\>...\</To\> 
\</soap:Header\>

  \<soap:Body\>    \<RequestSecurityToken
xmlns="http://docs.oasis-open.org/ws-sx/ws-trust/200512"\>     
\<RequestType\>http://docs.oasis-open.org/ws-sx/ws-trust/200512/Cancel\</RequestType\> 
    \<CancelTarget\>... the token to be cancelled ...\</CancelTarget\>   
\</RequestSecurityToken\>  \</soap:Body\>\</soap:Envelope\>

LogoutToken, Response:

\<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope"\>

  \<soap:Header\>    \<Action
xmlns="http://www.w3.org/2005/08/addressing"\>...\</Action\>    \<To
xmlns="http://www.w3.org/2005/08/addressing"\>http://docs.oasis-open.org/ws-sx/ws-trust/200512/RSTR/CancelFinal\</To\> 
\</soap:Header\>

  \<soap:Body\>    \<RequestSecurityTokenResponse
xmlns="http://docs.oasis-open.org/ws-sx/ws-trust/200512"\>     
\<RequestedTokenCancelled/\>    \</RequestSecurityTokenResponse\> 
\</soap:Body\>\</soap:Envelope\>

**A_17393-01 - Komponente Authentisierung Versicherter -
I_Authentication_Insurant:Logout nach WS-Trust, LogoutToken**

Die Komponente "Authentisierung Versicherter" MUSS die Operation Logout wie
folgt anbieten: **[\<=]**

### 5.1.1.1.4 Operation getAuditEvents

**A_14477-02 - Komponente Authentisierung Versicherter -
I_Authentication_Insurant::getAuditEvents**

Die Komponente "Authentisierung Versicherter" MUSS die
OperationI_Authentication_Insurant::getAuditEventsgemäß der folgenden Tabelle
implementieren:

Tabelle10: Tab_Auth_Vers_010 - Signatur der Schnittstelle
I_Authentication_Insurant::getAuditEvents

<table><tr><th>
Operation

</th><th colspan="3">
I_Authentication_Insurant::getAuditEvents

</th></tr><tr><td>
Beschreibung

</td><td colspan="3">
Mit dieser Operation kann ein authentifizierter Versicherter bzw. ein
berechtigter Vertreter das Verwaltungsprotokoll der Komponente "Authentisierung
Versicherter" auslesen. Es werden nur Protokolleinträge zurückgegeben, die
der authentifizierten Person zuzuordnen sind.

</td></tr><tr><td>
Formatvorgaben

</td><td colspan="3">
Die Definition der Ein- und Ausgabeparameter erfolgt in
[AuthenticationService.xsd ].

</td></tr><tr><td colspan="4">
Eingangsparameter

</td></tr><tr><td>
 Name

</td><td>
Beschreibung

</td><td>
Typ

</td><td>
opt.

</td></tr><tr><td>
AuthenticationAssertion

</td><td>
Die

AuthenticationAssertion

ist eine zuvor von der Komponente "Authentisierung Versicherter" ausgestellte
Authentifizierungsbestätigung.

</td><td>
SAML Assertion(im WSSE SOAP Header gem. [WSS-SAML#3.3])

</td><td>
-

</td></tr><tr><td>
PageSize

</td><td>
Umsetzung gemäß [gemSpecAktensystem#

]

</td><td>
Integer (\> 0)

</td><td>
y

</td></tr><tr><td>
PageNumber

</td><td>
Umsetzung gemäß [gemSpecAktensystem#

]

</td><td>
Integer (\> 0)

</td><td>
y

</td></tr><tr><td>
LastDay

</td><td>
Umsetzung gemäß [gemSpecAktensystem#

]

</td><td>
YYYY-MM-DD

 

</td><td>
y

</td></tr><tr><td colspan="4">
Ausgangsparameter

</td></tr><tr><td>
 Name

</td><td>
Beschreibung

</td><td>
Typ

</td><td>
opt.

</td></tr><tr><td>
AuditMessage

</td><td>
Liste der Verwaltungsprotokolleinträge, die sich auf die KVNR beziehen, die in
dem zugehörigen Attribut der übergebenen Authentication-Assertion enthalten
ist.

</td><td>
AuditMessage[0..*]

</td><td>
-

</td></tr><tr><td>
PageSize

</td><td>
Umsetzung gemäß [gemSpecAktensystem#

]

</td><td>
Integer (\> 0)

</td><td>
y

</td></tr><tr><td>
PageNumber

</td><td>
Umsetzung gemäß [gemSpecAktensystem#

]

</td><td>
Integer (\> 0)

</td><td>
y

</td></tr><tr><td>
TotalPages

</td><td>
Umsetzung gemäß [gemSpecAktensystem#

]

</td><td>
Integer (\>= 0)

</td><td>
y

</td></tr><tr><td>
TotalEntries

</td><td>
Umsetzung gemäß [gemSpecAktensystem#

]

</td><td>
Integer (\>= 0)

</td><td>
y

</td></tr><tr><td colspan="4">
Fehlermeldungen 

</td></tr><tr><td>
Name

</td><td>
Fehlertext

</td><td colspan="2">
Details

</td></tr><tr><td>
INTERNAL_ERROR

</td><td>
Es ist ein interner Fehler aufgetreten.

</td><td colspan="2">
Interner Fehler in der Verarbeitungslogik.

</td></tr><tr><td>
ASSERTION_INVALID

</td><td>
Die übergebene AuthenticationAssertion ist ungültig.

</td><td colspan="2">
z. B abgelaufen oder ungültige Signatur des Tokens.

</td></tr><tr><td>
SYNTAX_ERROR

</td><td>
Fehlerhafte Aufrufparameter.

</td><td colspan="2">
Es wurde ein fehlerhafter Aufrufparameter übergeben.

</td></tr></table>

**[\<=]**

### 5.1.1.1.5 Operation getSignedAuditEvents

**A_21162-02 - Komponente Authentisierung Versicherter -
I_Authentication_Insurant::getSignedAuditEvents**

Die Komponente "Authentisierung Versicherter" MUSS die
OperationI_Authentication_Insurant::getSignedAuditEventsgemäß der folgenden
Tabelle implementieren:

Tabelle11: Tab_Auth_Vers_016 - Signatur der Schnittstelle
I_Authentication_Insurant::getSignedAuditEvents

<table><tr><th>
Operation

</th><th colspan="3">
I_Authentication_Insurant::getSignedAuditEvents

</th></tr><tr><td>
Beschreibung

</td><td colspan="3">
Mit dieser Operation kann ein authentifizierter Versicherter das signierte
Verwaltungsprotokoll der Komponente "Authentisierung Versicherter" auslesen.

Das signierte Verwaltungsprotokoll enthält alle Protokolleinträge, die der
authentifizierten Person zuzuordnen sind.

</td></tr><tr><td>
Formatvorgaben

</td><td colspan="3">
Die Definition der Ein- und Ausgabeparameter erfolgt in
[AuthenticationService.xsd ].

</td></tr><tr><td colspan="4">
Eingangsparameter

</td></tr><tr><td>
 Name

</td><td>
Beschreibung

</td><td>
Typ

</td><td>
opt.

</td></tr><tr><td>
AuthenticationAssertion

</td><td>
Die

AuthenticationAssertion

ist eine zuvor von der Komponente "Authentisierung Versicherter" ausgestellte
Authentifizierungsbestätigung.

</td><td>
SAML Assertion(im WSSE SOAP Header gem. [WSS-SAML#3.3])

</td><td>
-

</td></tr><tr><td>
PageSize

</td><td>
Umsetzung gemäß [gemSpecAktensystem#

]

</td><td>
Integer (\> 0)

</td><td>
y

</td></tr><tr><td>
PageNumber

</td><td>
Umsetzung gemäß [gemSpecAktensystem#

]

</td><td>
Integer (\> 0)

</td><td>
y

</td></tr><tr><td>
LastDay

</td><td>
Umsetzung gemäß [gemSpecAktensystem#

]

</td><td>
YYYY-MM-DD

 

</td><td>
y

</td></tr><tr><td colspan="4">
Ausgangsparameter

</td></tr><tr><td>
 Name

</td><td>
Beschreibung

</td><td>
Typ

</td><td>
opt.

</td></tr><tr><td>
SignedAuditEventList

</td><td>
Signierte Liste (Teilliste bei Verwendung der Paging-Parameter) der
Verwaltungsprotokolleinträge, die sich auf die KVNR beziehen, die in dem
zugehörigen Attribut der übergebenen Authentication-Assertion enthalten ist. 

</td><td>
Signiertes Dokument

</td><td>
-

</td></tr><tr><td>
PageSize

</td><td>
Umsetzung gemäß [gemSpecAktensystem#

]

</td><td>
Integer (\> 0)

</td><td>
y

</td></tr><tr><td>
PageNumber

</td><td>
Umsetzung gemäß [gemSpecAktensystem#

]

</td><td>
Integer (\> 0)

</td><td>
y

</td></tr><tr><td>
TotalPages

</td><td>
Umsetzung gemäß [gemSpecAktensystem#

]

</td><td>
Integer (\>= 0)

</td><td>
y

</td></tr><tr><td>
TotalEntries

</td><td>
Umsetzung gemäß [gemSpecAktensystem#

]

</td><td>
Integer (\>= 0)

</td><td>
y

</td></tr><tr><td colspan="4">
Fehlermeldungen 

</td></tr><tr><td>
Name

</td><td>
Fehlertext

</td><td colspan="2">
Details

</td></tr><tr><td>
INTERNAL_ERROR

</td><td>
Es ist ein interner Fehler aufgetreten.

</td><td colspan="2">
Interner Fehler in der Verarbeitungslogik.

</td></tr><tr><td>
ASSERTION_INVALID

</td><td>
Die übergebene AuthenticationAssertion ist ungültig.

</td><td colspan="2">
z. B abgelaufen oder ungültige Signatur des Tokens.

</td></tr><tr><td>
SYNTAX_ERROR

</td><td>
Fehlerhafte Aufrufparameter.

</td><td colspan="2">
Es wurde ein fehlerhafter Aufrufparameter übergeben.

</td></tr></table>

**[\<=]**

### 5.1.2 Umsetzung

### 5.1.2.1 Schnittstelle I_Authentication_Insurant

### 5.1.2.1.1 Operation login

**A_15052 - Komponente Authentisierung Versicherter - loginCreateChallenge,
Ablauf**

Die Komponente "Authentisierung Versicherter" MUSS beim Aufruf der
OperationloginCreateChallengedie folgenden Aktionen ausführen und bei den
genannten Fehlerbedingungen die Fehlermeldungen (vgl. Kap. 5.1.1.1.1)
entsprechend setzen:

Tabelle12: Tab_Auth_Vers_011 - Ablauf von loginCreateChallenge

<table><tr><th>
Aktion

</th><th>
Fehlerbedingung

</th><th>
Fehlermeldung

</th></tr><tr><td>
Validierung der Eingangsnachricht gegen die WSDL und die zugehörigen
Schemadateien 

</td><td>
Fehler bei der Validierung.

</td><td>
wst:InvalidRequestoder allgemeiner SOAP-Fault

</td></tr><tr><td>
Eingangsparameter entsprechend A_14053 prüfen

</td><td>
Fehlende Elemente oder falsche Inhalte oder andere Fehler im empfangenen Request.

</td><td>
wst:InvalidRequest

</td></tr><tr><td>
Zufallswert für die Responsemessage gem. [gemSpec_Krypt#GS-A_4367] erzeugen

</td><td>
Zufallswert nicht verfügbar oder andere interne Verarbeitungsfehler.

</td><td>
wst:RequestFailed

</td></tr></table>

**[\<=]**

**A_14229 - Komponente Authentisierung Versicherter - loginCreateToken, Ablauf**

Das Komponente "Authentisierung Versicherter" MUSS beim Aufruf der
OperationloginCreateTokendie folgenden Aktionen ausführen und bei den
genannten Fehlerbedingungen die Fehlermeldungen (vgl. Kap. 5.1.1.1.1)
entsprechend setzen:

Tabelle13: Tab_Auth_Vers_012 - Ablauf von loginCreateToken

<table><tr><th>
Aktion

</th><th>
Fehlerbedingung

</th><th>
Fehlermeldung

</th></tr><tr><td>
Validierung der Eingangsnachricht gegen die WSDL und die zugehörigen
Schemadateien 

</td><td>
Fehler bei der Validierung.

</td><td>
wst:InvalidRequest

oder allgemeiner SOAP Fault

</td></tr><tr><td>
Prüfung WS-Security Header

</td><td>
Das Signaturzertifikat ist nicht vorhanden oder das Signaturverfahren entspricht
nicht den Vorgaben von [gemSpec_Krypt].

</td><td>
wst:InvalidRequest

</td></tr><tr><td>
Prüfung mathematische Korrektheit der Signatur

</td><td>
Signatur nicht korrekt.

</td><td>
wst:InvalidRequest

</td></tr><tr><td>
Das Signaturzertifikat muss gemäß [gemSpec_PKI#TUC_PKI_018] geprüft werden.
Parameter:

 ---> UL

Eine Prüfung der vom TUC zurückgelieferten Rollen-OID ist nicht erforderlich.

</td><td>
Fehlermeldung des aufgerufenen TUC.

</td><td>
wst:InvalidSecurityToken

</td></tr><tr><td>
Eingangsparameter des SOAP Body entsprechend A_14059 prüfen

</td><td>
Fehlende Elemente oder falsche Inhalte oder andere Fehler.

</td><td>
wst:InvalidRequest

</td></tr><tr><td>
Challenge

Element mit abgesendeter

Challenge

in Response zu

loginCreateChallenge

vergleichen

</td><td>
Challenges verschieden.

</td><td>
wst:InvalidRequest

</td></tr><tr><td>
AuthenticationAssertion (Token) gem. A_14109 erstellen und in Whitelist für
Erneuerung aufnehmen (s. Kap. 5.1.3#A_17395)

</td><td>
Fehler in der  internen Verarbeitung.

</td><td>
wst:RequestFailed

</td></tr></table>

**[\<=]**

Die Bestückung der Authentifizierungsbestätigung wird an einem Beispiel
illustriert und dann normativ festgelegt.Beispiel Authentifizierungsbestätigung

\<?xml version="1.0" encoding="UTF-8"?\>\<saml2:Assertion
xmlns:saml2="urn:oasis:names:tc:SAML:2.0:assertion"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
ID="_108c30ac-bbcb-42c9-b306-a61c39a6d890"
IssueInstant="2018-09-20T11:29:19.858Z" Version="2.0"
xsi:type="saml2:AssertionType"\>   
\<saml2:Issuer\>https://[ePA_TI_FQDN]/authn\</saml2:Issuer\>   
\<ds:Signature xmlns:ds="http://www.w3.org/2000/09/xmldsig#"\>       
\<ds:SignedInfo\>            \<ds:CanonicalizationMethod
Algorithm="http://www.w3.org/2001/10/xml-exc-c14n#"/\>           
\<ds:SignatureMethod
Algorithm="http://www.w3.org/2007/05/xmldsig-more#sha256-rsa-MGF1"/\>     
      \<ds:Reference URI="#_108c30ac-bbcb-42c9-b306-a61c39a6d890"\>     
          \<ds:Transforms\>                    \<ds:Transform
Algorithm="http://www.w3.org/2000/09/xmldsig#enveloped-signature"/\>       
            \<ds:Transform
Algorithm="http://www.w3.org/2001/10/xml-exc-c14n#"\>                 
      \<ec:InclusiveNamespaces
xmlns:ec="http://www.w3.org/2001/10/xml-exc-c14n#" PrefixList="xsd"/\>     
              \</ds:Transform\>               
\</ds:Transforms\>                \<ds:DigestMethod
Algorithm="http://www.w3.org/2001/04/xmlenc#sha256"/\>               
\<ds:DigestValue\>TDtN2nJ05NUB1n18GL7AalUyuMVvrIHlEklGKXLho2o=\</ds:DigestValue\> 
          \</ds:Reference\>        \</ds:SignedInfo\>       
\<ds:SignatureValue\>aA4mAz3W2j7YWTKZmSXH2erR5MtfzzOroWRLsy0wVwZdSsaK3MXW5pTnVjXE87Wq2dYJ3OFhu1QGGPWwz1qNxnmynBiWlfu21UZNuroQycQCIojHqw+wguYkZJQAA7exfyDAQYG8lgQbg4YiaIHWvy7l/VPu8fKaU/BgGObbnYyLuXwg2DrTilD1XbunBpj25Hps4z6cS5zJZPPIIx8ZqOQ/keyz4Z+gcykj9Djv87lb/UZciBqtNR7nWv9PhDwvFti9VvD3KbNixgoyNozGbgAdlc9qo4gLgmDXuMhZLrOADzVwDOlmdx3/6rp+4vyMODdZGtIMA97EqPAm+QF0DQ==\</ds:SignatureValue\> 
      \<ds:KeyInfo\>            \<ds:X509Data\>               
\<ds:X509Certificate\>MIID...zA==\</ds:X509Certificate\>           
\</ds:X509Data\>        \</ds:KeyInfo\>    \</ds:Signature\>   
\<saml2:Subject\>        \<saml2:NameID
Format="urn:oasis:names:tc:SAML:1.1:nameid-format:X509SubjectName"
NameQualifier="http://cxf.apache.org/sts"\>CN=Harald Graf
HünschTEST-ONLY,2.5.4.42=#0c0b486172616c642047726166,2.5.4.4=#0c0748c3bc6e736368,OU=999567890,OU=X110446869,O=gematik
Musterkasse1GKVNOT-VALID,C=DE\</saml2:NameID\>       
\<saml2:SubjectConfirmation Method="urn:oasis:names:tc:SAML:2.0:cm:bearer"/\> 
  \</saml2:Subject\>    \<saml2:Conditions
NotBefore="2018-09-20T11:29:19.884Z"
NotOnOrAfter="2018-09-20T11:44:19.884Z"\>       
\<saml2:AudienceRestriction\>           
\<saml2:Audience\>[ePA_TI_FQDN_autn]\</saml2:Audience\>  
           
\<saml2:Audience\>[ePA_TI_FQDN_autz]\</saml2:Audience\>           
\<saml2:Audience\>[ePA_TI_FQDN_dokv]\</saml2:Audience\>       
\</saml2:AudienceRestriction\>    \</saml2:Conditions\>   
\<saml2:AuthnStatement AuthnInstant="2018-09-20T11:29:19.878Z"\>       
\<saml2:AuthnContext\>

            \<saml2:AuthnContextClassRef\>

                urn:oasis:names:tc:SAML:2.0:ac:classes:SmartcardPKI

            \</saml2:AuthnContextClassRef\>       
\</saml2:AuthnContext\>    \</saml2:AuthnStatement\>   
\<saml2:AttributeStatement\>

                  ...        \<saml2:Attribute
Name="urn:gematik:subject:subject-id"
NameFormat="urn:oasis:names:tc:SAML:2.0:attrname-format:uri"\>           
\<saml2:AttributeValue\>

               \<InstanceIdentifier xmlns="urn:hl7-org:v3"
extension="G995030566" root="1.2.276.0.76.4.8"/\>

            \</saml2:AttributeValue\>        \</saml2:Attribute\>   
\</saml2:AttributeStatement\>\</saml2:Assertion\>

**A_14109-02 - Komponente Authentisierung Versicherter - Befüllung der
Authentifizierungsbestätigung bei Login**

Die Komponente "Authentisierung Versicherter" MUSS die für die Operation
loginCreateToken erzeugteAuthentifizierungsbestätigung  als SAML2-Assertion
gemäß [gemSpec_TBAuth#TAB_TBAuth_03] umsetzen und dabei folgende Vorgaben
beachten:

 ---> UL

**[\<=]**

**A_15631 - Komponente Authentisierung Versicherter - Behauptungen in der
Authentifizierungsbestätigung**

Die Komponente "Authentisierung Versicherter" MUSS die für die Operation
loginCreateToken erzeugte Authentifizierungsbestätigung im
ElementAttributeStatementmit den Behauptungen gemäß
[gemSpec_TBAuth#TAB_TBAuth_02_2] befüllen und dabei folgende Vorgaben beachten:

 ---> UL

**[\<=]**

### 5.1.2.1.2 Operation Renew

**A_17398 - Komponente Authentisierung Versicherter - RenewToken**

Die Komponente "Authentisierung Versicherter" MUSS beim Aufruf der
OperationRenewTokendie folgenden Aktionen ausführen und bei den genannten
Fehlerbedingungen die Fehlermeldungen (vgl. Kap. 5.1.1.1.2) entsprechend setzen:

Tabelle14: Tab_Auth_Vers_015 - Ablauf von RenewToken

<table><tr><th>
Aktion

</th><th>
Fehlerbedingung

</th><th>
Fehlermeldung

</th></tr><tr><td>
Validierung der Eingangsnachricht gegen die WSDL und die zugehörigen
Schemadateien 

</td><td>
Fehler bei der Validierung.

</td><td>
wst:InvalidRequest

oder allgemeiner SOAP-Fault

</td></tr><tr><td>
Eingangsparameter entsprechend A_17392 prüfen

</td><td>
Fehlende Elemente oder falsche Inhalte oder andere Fehler im empfangenen Request.

</td><td>
wst:InvalidRequest

</td></tr><tr><td>
Prüfung gegen WhiteList entsprechend A_17395 und Entfernen des Tokens aus der
Whitelist

</td><td>
Token nicht in Whitelist vorhanden

</td><td>
wst:UnableToRenew

</td></tr><tr><td>
Erstellung der neuen Authenfizierungsbestätigung gemäß A_17793 und ggf.
Aufnahme in Whitelist für Erneuerung (gem. Kap. 5.1.3#A_17395) 

</td><td>
Fehler in der  internen Verarbeitung.

</td><td>
wst:RequestFailed

</td></tr></table>

**[\<=]**

**A_17793 - Komponente Authentisierung Versicherter - Befüllung der
Authentifizierungsbestätigung bei Renew**

Die Komponente "Authentisierung Versicherter" MUSS die für die Operation
RenewToken erzeugte Authentifizierungsbestätigung  als SAML2-Assertion
gemäß [gemSpec_TBAuth#TAB_TBAuth_03] umsetzen und dabei folgende Vorgaben
beachten:

 ---> UL

**[\<=]**

### 5.1.2.1.3 Operation Logout

**A_17412 - Komponente Authentisierung Versicherter - LogoutToken**

Die Komponente "Authentisierung Versicherter" MUSS beim Aufruf der
OperationLogoutTokendie folgenden Aktionen ausführen und bei den genannten
Fehlerbedingungen die Fehlermeldungen (vgl. Kap. 5.1.1.1.3) entsprechend setzen:

Tabelle15: Tab_Auth_Vers_015 - Ablauf von RenewToken

<table><tr><th>
Aktion

</th><th>
Fehlerbedingung

</th><th>
Fehlermeldung

</th></tr><tr><td>
Validierung der Eingangsnachricht gegen die WSDL und die zugehörigen
Schemadateien 

</td><td>
Fehler bei der Validierung.

</td><td>
wst:InvalidRequest

oder allgemeiner SOAP-Fault

</td></tr><tr><td>
Eingangsparameter entsprechend A_17393 prüfen

</td><td>
Fehlende Elemente oder falsche Inhalte oder andere Fehler im empfangenen Request.

</td><td>
wst:InvalidRequest

</td></tr><tr><td>
Authentifizierungsbestätigung (Token) aus Whitelist für Erneuerung entfernen

</td><td>
Authentifizierungsbestätigung nicht in Whitelist vorhanden

</td><td>
(keine Fehlermeldung)

</td></tr></table>

**[\<=]**

### 5.1.2.1.4 Operation getAuditEvents

Die Vorgaben zur Erstellung der Protokolleinträge sind in Kap. 4.4 beschrieben.
Zur Prüfung der Berechtigung des Abrufs des Protokolls wird die übergebene
Authentifizierungsbestätigung geprüft.

**A_14781 - Komponente Authentisierung Versicherter - getAuditEvents,
Prüfschritte**

Die Komponente "Authentisierung Versicherter" MUSS beim Aufruf der
OperationgetAuditEventsdie Prüfschritte
fürAuthentifizierungsbestätigungengem. Kap. 4.2 mit der als Eingangsparameter
übergebenen Authentifizierungsbestätigungausführen und die Fehlermeldung
(vgl. Kap. 5.1.1.1.2) wie folgt setzen:

Tabelle16: Tab_Auth_Vers_013 - Prüfschritte bei getAuditEvents

<table><tr><th>
Fehlerbedingung

</th><th>
Fehlermeldung

</th></tr><tr><td>
Fehler bei Validierung der Eingangsnachricht gegen die WSDL oder die
zugehörigen Schemadateien

</td><td>
SYNTAX_ERROR oder allgemeiner SOAP Fault

</td></tr><tr><td>
Fehler im empfangenen Request

</td><td>
SYNTAX_ERROR

</td></tr><tr><td>
Interner Fehler in der Verarbeitungslogik

</td><td>
INTERNAL_ERROR

</td></tr><tr><td>
Ein Prüfschritt der Signaturprüfung gem. [gemSpec_TBAuth#A_15556] bzw.

[gemSpec_Authentisierung_Vers#A_14777] liefert einen Fehler.

</td><td>
ASSERTION_INVALID

</td></tr><tr><td>
Ein Prüfschritt der Inhaltsprüfung gem.
[gemSpec_TBAuth#A_15558]/[gemSpec_Authentisierung_Vers#A_14780] bzw.
[gemSpec_TBAuth#A_15637] liefert einen Fehler.

</td><td>
ASSERTION_INVALID

</td></tr></table>

**[\<=]**

**A_14803 - Komponente Authentisierung Versicherter - Umsetzung getAuditEvents**

Die Komponente "Authentisierung Versicherter" MUSS beim Aufruf der
OperationgetAuditEventsdie Liste aller Verwaltungsprotokolleinträge gemäß
[] zurückliefern, die der Identität in der
übergebenenAuthentifizierungsbestätigungentsprechen.​​ **[\<=]**

### 5.1.2.1.5 Operation getSignedAuditEvents

Die Vorgaben zur Erstellung der Protokolleinträge sind in Kap. 4.4 beschrieben.
Zur Prüfung der Berechtigung des Abrufs des Protokolls wird die übergebene
Authentifizierungsbestätigung geprüft.

**A_21163 - Komponente Authentisierung Versicherter - getSignedAuditEvents,
Prüfschritte**

Die Komponente "Authentisierung Versicherter" MUSS beim Aufruf der
OperationgetSignedAuditEventsdie Prüfschritte
fürAuthentifizierungsbestätigungengem. Kap. 4.2 mit der als Eingangsparameter
übergebenen Authentifizierungsbestätigungausführen und die Fehlermeldung
(vgl. Kap. 5.1.1.1.2) wie folgt setzen:

Tabelle17: Tab_Auth_Vers_017 - Prüfschritte bei getSignedAuditEvents

<table><tr><th>
Fehlerbedingung

</th><th>
Fehlermeldung

</th></tr><tr><td>
Fehler bei Validierung der Eingangsnachricht gegen die WSDL oder die
zugehörigen Schemadateien

</td><td>
SYNTAX_ERROR oder allgemeiner SOAP Fault

</td></tr><tr><td>
Fehler im empfangenen Request

</td><td>
SYNTAX_ERROR

</td></tr><tr><td>
Interner Fehler in der Verarbeitungslogik

</td><td>
INTERNAL_ERROR

</td></tr><tr><td>
Ein Prüfschritt der Signaturprüfung gem. [gemSpec_TBAuth#A_15556] bzw.
[gemSpec_Authentisierung_Vers#A_14777] liefert einen Fehler.

</td><td>
ASSERTION_INVALID

</td></tr><tr><td>
Ein Prüfschritt der Inhaltsprüfung gem.
[gemSpec_TBAuth#A_15558]/[gemSpec_Authentisierung_Vers#A_14780] bzw.
[gemSpec_TBAuth#A_15637] liefert einen Fehler.

</td><td>
ASSERTION_INVALID

</td></tr></table>

**[\<=]**

**A_21164-02 - Komponente Authentisierung Versicherter - Umsetzung
getSignedAuditEvents**

Die Komponente "Authentisierung Versicherter" MUSS beim Aufruf der
OperationgetSignedAuditEventsein signiertes Dokument  zurückliefern, welches
alle Verwaltungsprotokolleinträge gemäß [gemSpec_DM_ePA#A_14471] enthält,
die der Identität in der übergebenen Authentifizierungsbestätigung
entsprechen, wobei für die Signatur der Liste der private Schlüssel der
Ausstelleridentität ID.FD.SIG genutzt wird, dessen zugehöriges Zertifikat
C.FD.SIG die Rolle "oid_epa_logging" enthält. **[\<=]**

Es wird das gesamte Dokument bzw. Dokumente signiert. Das Format soll dem der
AuditEvents entsprechen.

### 5.1.3 Lebensdauer der Authentifizierungsbestätigung

Die Authentifizierungsbestätigung (Token) wird mit einer kurzen Lebensdauer
erstellt. Innerhalb dieser Lebensdauer kann über die Operation Renew ein neuer
Token wieder mit einer kurzen Lebensdauer ausgestellt werden. Durch Aufruf der
Logout Operation wird die Möglichkeit eines erneuten Renew unterbunden. Die
Gesamtlebensdauer, über die ein Renew erfolgen kann, wird beschränkt.

**A_17395 - Komponente Authentisierung Versicherter - Whitelist**

Die Komponente "Authentisierung Versicherter" MUSS eine Whitelist der aktiven
Authentifizierungsbestätigungen (Token) mit folgenden Eigenschaften führen:

 ---> UL

**[\<=]**

Die Whitelist wirkt somit ausschließlich als Einschränkung für die Operation
Renew:

 ---> UL

Für die konkrete Ausgestaltung der Aktualisierung der Whitelist werden keine
Vorgaben gemacht. Die Anforderungen in dieser Spezifikation stellen nur das
logische Modell des Verhaltens der Whitelist dar. Umsetzungen sind
spezifikationskonform, sofern dieses Verhalten an der Schnittstelle der
Komponente reproduziert wird.

### 6 Informationsmodell

Ein gesondertes Informationsmodell der durch den Produkttypen verarbeiteten
Daten wird nicht benötigt.

### 7 Verteilungssicht

Eine Darstellung der hardwareseitigen Verteilung des Produkttyps bzw. seiner
Teilsysteme und der Einbettung in die physikalische Umgebung wird nicht
benötigt.

### 8 Anhang A – Verzeichnisse

### 8.1 Abkürzungen

<table><tr><th>
Kürzel

</th><th>
Erläuterung

</th></tr><tr><td>
CDA

</td><td>
Clinical Document Architecture

</td></tr><tr><td>
eGK

</td><td>
elektronische Gesundheitskarte

</td></tr><tr><td>
ePA

</td><td>
elektronische Patientenakte

</td></tr><tr><td>
FdV

</td><td>
ePA-Frontend des Versicherten

</td></tr><tr><td>
FQDN

</td><td>
Fully-Qualified Domain Name

</td></tr><tr><td>
HSM

</td><td>
Hardware Security Module

</td></tr><tr><td>
HTTP

</td><td>
Hypertext Transfer Protocol

</td></tr><tr><td>
IHE

</td><td>
Integrating the Healthcare Enterprise

</td></tr><tr><td>
KVNR

</td><td>
Krankenversichertennummer (vgl. Kap. 4.6)

</td></tr><tr><td>
OID

</td><td>
Object Identifier

</td></tr><tr><td>
SAML

</td><td>
Security Assertion Markup Language

</td></tr><tr><td>
SOAP

</td><td>
Simple Object Access Protocol

</td></tr><tr><td>
TI

</td><td>
Telematikinfrastruktur

</td></tr><tr><td>
TLS

</td><td>
Transport Layer Security

</td></tr><tr><td>
TUC

</td><td>
Technical Use Case

</td></tr><tr><td>
VAU

</td><td>
Vertrauenswürdige Ausführungsumgebung

</td></tr><tr><td>
W3C

</td><td>
World Wide Web Consortium

</td></tr><tr><td>
WS-I

</td><td>
Web-Services Interoperability Consortium

</td></tr><tr><td>
WSDL

</td><td>
Web Services Description Language

</td></tr><tr><td>
XACML

</td><td>
eXtensible Access Control Markup Language

</td></tr><tr><td>
XSPA

</td><td>
Cross-Enterprise Security and Privacy Authorization Profile

</td></tr><tr><td>
XUA

</td><td>
Cross-Enterprise User Assertion Profile 

</td></tr></table>

### 8.2 Glossar

Das Glossar wird als eigenständiges Dokument (vgl. [gemGlossar]) zur Verfügung
gestellt.

### 8.3 Abbildungsverzeichnis



### 8.4 Tabellenverzeichnis

- [Tabelle-1] - Tab_Auth_Vers_002 - Verwendete Namensräume und Präfixe
- [Tabelle-3] - Tab_Auth_Vers_004 - Operationsabhängige Parameter des Verwaltungsprotokolls
- [Tabelle-4] - Tab_Auth_Vers_0016- Operationsabhängige Parameter des Verwaltungsprotokolls bei fehlerhaftem Aufruf der Operation loginCreateToken
- [Tabelle-5] - Tab_Auth_Vers_005 - Schnittstellenübersicht der Komponente Authentisierung des Versicherten
- [Tabelle-6] - Tab_Auth_Vers_006 - Benutzte Schnittstellen der TI
- [Tabelle-8] - Tab_Auth_Vers_008 - Signatur der Schnittstelle I_Authentication_Insurant:loginCreateChallenge
- [Tabelle-9] -   Tab_Auth_Vers_009 - Signatur der Schnittstelle I_Authentication_Insurant:loginCreateToken
- [Tabelle-10] - Tab_Auth_Vers_010 - Signatur der Schnittstelle I_Authentication_Insurant::getAuditEvents
- [Tabelle-11] - Tab_Auth_Vers_016 - Signatur der Schnittstelle I_Authentication_Insurant::getSignedAuditEvents
- [Tabelle-13] - Tab_Auth_Vers_012 - Ablauf von loginCreateToken
- [Tabelle-14] - Tab_Auth_Vers_015 - Ablauf von RenewToken
- [Tabelle-15] - Tab_Auth_Vers_015 - Ablauf von RenewToken
- [Tabelle-16] - Tab_Auth_Vers_013 - Prüfschritte bei getAuditEvents
- [Tabelle-17] - Tab_Auth_Vers_017 - Prüfschritte bei getSignedAuditEvents

### 8.5 Referenzierte Dokumente

### 8.5.1 Dokumente der gematik

Die nachfolgende Tabelle enthält die Bezeichnung der in dem vorliegenden
Dokument referenzierten Dokumente der gematik zur Telematikinfrastruktur.

<table><tr><th>
[Quelle]

</th><th>
Herausgeber: Titel

</th></tr><tr><td>
[gemGlossar]

</td><td>
gematik: Glossar der Telematikinfrastruktur

</td></tr><tr><td>
[gemSysL_ePA]

</td><td>
gematik: Systemspezifisches Konzept ePA

</td></tr><tr><td>
[gemSpec_Aktensystem]

</td><td>
gematik: Spezifikation Aktensystem ePA

</td></tr><tr><td>
[gemSpec_DM_ePA]

</td><td>
gematik: Datenmodell ePA

</td></tr><tr><td>
[gemSpec_Zugangsgateway_Vers]

</td><td>
gematik: Spezifikation Zugangsgateway des Versicherten ePA

</td></tr><tr><td>
[gemSpec_Autorisierung]

</td><td>
gematik: Spezifikation Autorisierung ePA

</td></tr><tr><td>
[gemSpec_FM_ePA]

</td><td>
gematik: Spezifikation Fachmodul ePA

</td></tr><tr><td>
[gemSpec_ePA_FdV]

</td><td>
gematik: Spezifikation Frontend des Versicherten ePA

</td></tr><tr><td>
[gemKPT_Arch_TIP]

</td><td>
gematik: Konzept Architektur der TI-Plattform

</td></tr><tr><td>
[gemKPT_PKI_TIP]

</td><td>
gematik: Konzept PKI der TI-Plattform

</td></tr><tr><td>
[gemSpec_Net]

</td><td>
gematik: Übergreifenden Spezifikation Netzwerk

</td></tr><tr><td>
[gemSpec_Perf]

</td><td>
gematik: Spezifikation Performancevorgaben und Mengengerüst

</td></tr><tr><td>
[gemSpec_OID]

</td><td>
gematik: Spezifikation Festlegung von OIDs

</td></tr><tr><td>
[gemSpec_OM]

</td><td>
gematik: Übergreifende Spezifikation Operations und Maintenance

</td></tr><tr><td>
[gemSpec_PKI]

</td><td>
gematik: Spezifikation PKI

</td></tr><tr><td>
[gemSpec_Krypt]

</td><td>
gematik: Übergreifende Spezifikation - Verwendung kryptographischer Algorithmen
in der Telematikinfrastruktur

</td></tr><tr><td>
[gemSpec_X.509_TSP]

</td><td>
gematik: PKI für X.509-Zertifikate: Spezifikation Trust Service Provider X.509

</td></tr><tr><td>
[gemSpec_TSL]

</td><td>
gematik: Spezifikation TSL-Dienst

</td></tr></table>

### 8.5.2 Weitere Dokumente

<table><tr><th>
[Quelle]

</th><th>
Herausgeber (Erscheinungsdatum): Titel

</th></tr><tr><td>
[RFC2119]

</td><td>
IETF (1997): Key words for use in RFCs to Indicate Requirement Levels, RFC 2119,

http://tools.ietf.org/html/rfc2119

</td></tr><tr><td>
[RFC7231]

</td><td>
IETF (2014): Hypertext Transfer Protocol (HTTP/1.1): Semantics and Content, RFC
7231, 

https://tools.ietf.org/html/rfc7231

 

</td></tr><tr><td>
[SOAP]

</td><td>
W3C (2007): SOAP Version 1.2 Part 1: Messaging Framework (Second Edition), 

https://www.w3.org/TR/soap12-part1/

 

</td></tr><tr><td>
[SAML2.0]

</td><td>
Assertions and Protocols for the OASIS Security Assertion Markup Language (SAML)
V2.0

http://docs.oasis-open.org/security/saml/v2.0/

</td></tr><tr><td>
[WSDL]

</td><td>
W3C: Web Services Description Language (WSDL) 1.1

https://www.w3.org/TR/wsdl.html

 

</td></tr><tr><td>
[WSDL11SOAP12]

</td><td>
W3C (2006): WSDL 1.1Binding Extension for SOAP 1.2, 

https://www.w3.org/Submission/wsdl11soap12/

 

</td></tr><tr><td>
[WSIBP]

</td><td>
Web-Services Interoperability Consortium (2010): WS-I Basic Profile V2.0 (final
material), 

http://ws-i.org/Profiles/BasicProfile-2.0-2010-11-09.html

</td></tr><tr><td>
[WSS]

</td><td>
OASIS (2006): Web Services Security: SOAP Message Security 1.1 (WS-Security
2004), 

http://www.oasis-open.org/committees/download.php/16790/wss-v1.1-spec-os-SOAPMessageSecurity.pdf

 

</td></tr><tr><td>
[WSS-SAML]

</td><td>
OASIS (2006): Web Services Security: SAML Token Profile 1.1, 

https://www.oasis-open.org/committees/download.php/16768/wss-v1.1-spec-os-SAMLTokenProfile.pdf

 

</td></tr><tr><td>
[WS-Trust]

</td><td>
WS-Trust 1.4

OASIS Standard incorporating Approved Errata01

25.04.2012

http://docs.oasis-open.org/ws-sx/ws-trust/v1.4/errata01/os/ws-trust-1.4-errata01-os-complete.doc

 

</td></tr><tr><td>
[XSPA-SAML]

</td><td>
OASIS:  Cross-Enterprise Security and Privacy Authorization (XSPA) Profile of
Security Assertion Markup Language (SAML) for Healthcare Version 2.0

http://docs.oasis-open.org/xspa/saml-xspa/v2.0/saml-xspa-v2.0.html

</td></tr><tr><td>
[IHE#ITI-40]

</td><td>
IHE IT Infrastructure Technical Framework

Volume 2b (ITI TF-2b) – Transactions Part B, Revision 15.0, Section 3.40
Provide X-User Assertion [ITI-40]

http://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2b.pdf

 

</td></tr></table>





[Dokumentinformationen]: #dokumentinformationen
[Inhaltsverzeichnis]:    #inhaltsverzeichnis
[1]:                     #1-einordnung-des-dokumentes
[1.1]:                   #11-zielsetzung
[1.2]:                   #12-zielgruppe
[1.3]:                   #13-geltungsbereich
[1.4]:                   #14-abgrenzungen
[1.5]:                   #15-methodik
[2]:                     #2-systemkontext
[3]:                     #3-zerlegung-der-komponente
[4]:                     #4-übergreifende-festlegungen
[4.1]:                   #41-datenschutz-und-datensicherheit
[4.2]:                   #42-verwendete-standards
[4.3]:                   #43-fehlerbehandlung
[4.4]:                   #44-protokollierung
[4.5]:                   #45-nicht-funktionale-anforderungen
[4.6]:                   #46-identifikation-der-akteure
[5]:                     #5-funktionsmerkmale
[5.1]:                   #51-authentisierung
[5.1.1]:                 #511-schnittstellen
[5.1.1.1]:               #5111-schnittstelle-i_authentication_insurant
[5.1.1.1.1]:             #51111-operation-login
[5.1.1.1.2]:             #51112-operation-renew
[5.1.1.1.3]:             #51113-operation-logout
[5.1.1.1.4]:             #51114-operation-getauditevents
[5.1.1.1.5]:             #51115-operation-getsignedauditevents
[5.1.2]:                 #512-umsetzung
[5.1.2.1]:               #5121-schnittstelle-i_authentication_insurant
[5.1.2.1.1]:             #51211-operation-login
[5.1.2.1.2]:             #51212-operation-renew
[5.1.2.1.3]:             #51213-operation-logout
[5.1.2.1.4]:             #51214-operation-getauditevents
[5.1.2.1.5]:             #51215-operation-getsignedauditevents
[5.1.3]:                 #513-lebensdauer-der-authentifizierungsbestätigung
[6]:                     #6-informationsmodell
[7]:                     #7-verteilungssicht
[8]:                     #8-anhang-a-–-verzeichnisse
[8.1]:                   #81-abkürzungen
[8.2]:                   #82-glossar
[8.3]:                   #83-abbildungsverzeichnis
[8.4]:                   #84-tabellenverzeichnis
[8.5]:                   #85-referenzierte-dokumente
[8.5.1]:                 #851-dokumente-der-gematik
[8.5.2]:                 #852-weitere-dokumente
[Tbl-001]:               #Tbl-001 (&93834801499568)
[Tabelle-1]:             #Tabelle-1 (&93834799842040)
[Tabelle-3]:             #Tabelle-3 (&93834783604824)
[Tabelle-4]:             #Tabelle-4 (&93834783653680)
[Tabelle-5]:             #Tabelle-5 (&93834770996664)
[Tabelle-6]:             #Tabelle-6 (&93834771024416)
[Tbl-007]:               #Tbl-007 (&93834775023552)
[Tabelle-8]:             #Tabelle-8 (&93834799205312)
[Tabelle-9]:             #Tabelle-9 (&93834804545872)
[Tabelle-10]:            #Tabelle-10 (&93834798469080)
[Tabelle-11]:            #Tabelle-11 (&93834764450864)
[Tbl-012]:               #Tbl-012 (&93834781750832)
[Tabelle-13]:            #Tabelle-13 (&93834781773000)
[Tabelle-14]:            #Tabelle-14 (&93834781586816)
[Tabelle-15]:            #Tabelle-15 (&93834781621472)
[Tabelle-16]:            #Tabelle-16 (&93834783931048)
[Tabelle-17]:            #Tabelle-17 (&93834783966480)
[Tbl-018]:               #Tbl-018 (&93834783491512)
[Tbl-019]:               #Tbl-019 (&93834785709816)
[Tbl-020]:               #Tbl-020 (&93834778224392)
[http://www.w3.org/2006/05/addressing/wsdl]: http://www.w3.org/2006/05/addressing/wsdl (&93834771080160)
[http://docs.oasis-open.org/wss/oasis-wss-saml-token-profile-1.1#SAMLV2.0]: http://docs.oasis-open.org/wss/oasis-wss-saml-token-profile-1.1#SAMLV2.0 (&93834799229688)
[http://docs.oasis-open.org/ws-sx/ws-trust/200512/Issue]: http://docs.oasis-open.org/ws-sx/ws-trust/200512/Issue (&93834799238920)
[http://docs.oasis-open.org/ws-sx/ws-trust/200512/RST/Renew]: http://docs.oasis-open.org/ws-sx/ws-trust/200512/RST/Renew (&93834774927920)
[http://docs.oasis-open.org/ws-sx/ws-trust/200512/RSTR/RenewFinal]: http://docs.oasis-open.org/ws-sx/ws-trust/200512/RSTR/RenewFinal (&93834774941456)
[http://docs.oasis-open.org/ws-sx/ws-trust/200512/RST/Cancel]: http://docs.oasis-open.org/ws-sx/ws-trust/200512/RST/Cancel (&93834799004512)
[http://docs.oasis-open.org/ws-sx/ws-trust/200512/RSTR/CancelFinal]: http://docs.oasis-open.org/ws-sx/ws-trust/200512/RSTR/CancelFinal (&93834798391944)
[http://tools.ietf.org/html/rfc2119]: http://tools.ietf.org/html/rfc2119 (&93834778230712)
[https://tools.ietf.org/html/rfc7231]: https://tools.ietf.org/html/rfc7231 (&93834778234496)
[https://www.w3.org/TR/soap12-part1/]: https://www.w3.org/TR/soap12-part1/ (&93834778238760)
[http://docs.oasis-open.org/security/saml/v2.0/]: http://docs.oasis-open.org/security/saml/v2.0/ (&93834778243328)
[https://www.w3.org/TR/wsdl.html]: https://www.w3.org/TR/wsdl.html (&93834778247504)
[https://www.w3.org/Submission/wsdl11soap12/]: https://www.w3.org/Submission/wsdl11soap12/ (&93834778251744)
[http://ws-i.org/Profiles/BasicProfile-2.0-2010-11-09.html]: http://ws-i.org/Profiles/BasicProfile-2.0-2010-11-09.html (&93834778256008)
[http://www.oasis-open.org/committees/download.php/16790/wss-v1.1-spec-os-SOAPMessageSecurity.pdf]: http://www.oasis-open.org/committees/download.php/16790/wss-v1.1-spec-os-SOAPMessageSecurity.pdf (&93834778259792)
[https://www.oasis-open.org/committees/download.php/16768/wss-v1.1-spec-os-SAMLTokenProfile.pdf]: https://www.oasis-open.org/committees/download.php/16768/wss-v1.1-spec-os-SAMLTokenProfile.pdf (&93834778264056)
[http://docs.oasis-open.org/ws-sx/ws-trust/v1.4/errata01/os/ws-trust-1.4-errata01-os-complete.doc]: http://docs.oasis-open.org/ws-sx/ws-trust/v1.4/errata01/os/ws-trust-1.4-errata01-os-complete.doc (&93834778270192)
[http://docs.oasis-open.org/xspa/saml-xspa/v2.0/saml-xspa-v2.0.html]: http://docs.oasis-open.org/xspa/saml-xspa/v2.0/saml-xspa-v2.0.html (&93834778275240)
[http://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2b.pdf]: http://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2b.pdf (&93834778280168)
