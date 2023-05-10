
Elektronische Gesundheitskarte und Telematikinfrastruktur

### Spezifikation<br>Implementierungsleitfaden Primärsysteme – E-Rezept

- Klassifizierung: öffentlich
- Referenzierung: gemILF_PS_eRp
- Revision: 548770
- Stand: 07.10.2021
- Status: freigegeben
- Version: 1.3.0

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
30.06.20

</td><td>
freigegeben

</td><td>
gematik

</td></tr><tr><td>
1.0.1

</td><td>
06.07.20

</td><td>
Aktualisierung Hinweis zu Dispensierinformation

</td><td>
gematik

</td></tr><tr><td>
1.1.0

</td><td>
12.11.20

</td><td>
Einarbeitung gemäß Änderungsliste P22.2 / Scope-Themen Systemdesign R4.0.1

</td><td>
gematik

</td></tr><tr><td>
1.2.0

</td><td>
19.02.21

</td><td>
Einarbeitung gemäß Änderungsliste P22.5

</td><td>
gematik

</td></tr><tr><td>
1.3.0 RC 2

</td><td>
19.05.21

</td><td>
Einarbeitung gemäß Änderungslisten  
E-Rezept_Maintenance_21.1 und  _21.2

</td><td>
gematik

</td></tr><tr><td>
1.3.0 RC 3

</td><td>
20.05.21

</td><td>
Einarbeitung gemäß Änderungseintrag C_10474, C_10718  
Übermittlung einer
URL durch eine Apotheke an einen Versicherten

</td><td>
gematik

</td></tr><tr><td>
1.3.0 RC 4

</td><td>
28.06.21

</td><td>
Kap. 5.3.7  
Kap. 5.1.3.1

</td><td>
Übermittlung url für alle Belieferungsoptionen  
Übergangsregelung für
alternative Zertifikatsprüfung

</td><td>
gematik

</td></tr><tr><td>
1.3.0

</td><td>
07.10.

.21

</td><td>
freigegeben

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
    - [1.5.1] Hinweis auf offene Punkte
- [2] Systemüberblick
- [3] Systemkontext
  - [3.1] E-Rezept Status
  - [3.2] FHIR-Ressourcen
- [4] Übergreifende Festlegungen
  - [4.1] Logging und Meldungen
  - [4.2] Namensauflösung
- [5] Funktionsmerkmale
  - [5.1] Allgemein
    - [5.1.1] Kommunikation zu den Diensten der TI
    - [5.1.2] Verschlüsselte Kommunikation zur VAU des E-Rezept-Fachdienstes
    - [5.1.3] Zertifikatsprüfung
      - [5.1.3.1] Zertifikatsprüfung von Zertifikaten der TI
      - [5.1.3.2] Zertifikatsprüfung von Internet-Zertifikaten
    - [5.1.4] Authentifizierung der LEI
      - [5.1.4.1] Übergreifende Festlegungen zur Nutzung des IDP-Dienstes
      - [5.1.4.2] Abruf von Token beim IDP-Dienst
  - [5.2] Anwendungsfälle verordnende LEI
    - [5.2.1] E-Rezept erstellen
    - [5.2.2] E-Rezept einstellen
    - [5.2.3] E-Rezept löschen
  - [5.3] Anwendungsfälle abgebende LEI
    - [5.3.1] E-Rezept abrufen
    - [5.3.2] Quittung abrufen
    - [5.3.3] Quittung erneut abrufen
    - [5.3.4] E-Rezept zurückgeben
    - [5.3.5] E-Rezept löschen
    - [5.3.6] Nachrichten von Versicherten empfangen
    - [5.3.7] Nachricht an Versicherten versenden
    - [5.3.8] Nachricht löschen
    - [5.3.9] Abgabedatensatz signieren
    - [5.3.10] 2D-Code einscannen
  - [5.4] Fehlerbehandlung
- [6] Informationsmodell
- [7] Anhang A – Verzeichnisse
  - [7.1] Abkürzungen
  - [7.2] Glossar
  - [7.3] Abbildungsverzeichnis
  - [7.4] Tabellenverzeichnis
  - [7.5] Referenzierte Dokumente
    - [7.5.1] Dokumente der gematik
    - [7.5.2] Weitere Dokumente

### 1 Einordnung des Dokumentes

### 1.1 Zielsetzung

Das Dokument beschreibt die für die Implementierung des E-Rezepts
erforderlichen Vorgaben.

### 1.2 Zielgruppe

Das Dokument richtet sich maßgeblich an Hersteller von Primärsystemen
(Praxisverwaltungssysteme, Krankenhausinformationssysteme und
Apothekenverwaltungssysteme) von Leistungserbringerinstitutionen (LEI).

### 1.3 Geltungsbereich

Die in diesem Dokument formulierten Anforderungen sind informativ für
Primärsysteme, die am Produktivbetrieb der Telematikinfrastruktur (TI)
teilnehmen. Der Gültigkeitszeitraum der vorliegenden Version und deren
Anwendung in Zulassungsverfahren wird durch die gematik GmbH in gesonderten
Dokumenten (z. B. Dokumentenlandkarte, Produkttypsteckbrief,
Leistungsbeschreibung) festgelegt und bekannt gegeben.

Die Anforderungen können für Implementierungsleitfäden bzw.
Konformitätsprofile der Sektoren verwendet werden.

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

Nicht Bestandteil des vorliegenden Dokumentes sind die Festlegungen zu den
genutzten FHIR-Ressourcen und den E-Rezept-Token. Anforderungen hierzu befinden
sich in [gemSpec_DM_eRp].

Nicht Bestandteil des vorliegenden Dokumentes sind die Festlegungen zu
Implementation des Authentisierungsmoduls. Anforderungen hierzu befinden sich
in [gemSpec_IDP_Dienst] und [gemSpec_IDP_Frontend].

### 1.5 Methodik

Anforderungen als Ausdruck normativer Festlegungen werden durch eine eindeutige
ID in eckigen Klammern sowie die dem RFC 2119 [RFC2119] entsprechenden, in
Großbuchstaben geschriebenen deutschen Schlüsselworte MUSS, DARF NICHT, SOLL,
SOLL NICHT, KANN gekennzeichnet.

Sie werden im Dokument wie folgt dargestellt:\<AFO-ID\> - \<Titel der Afo\>Text
/ Beschreibung [\<=]

Dabei umfasst die Anforderung sämtliche zwischen Afo-ID und der Textmarke [\<=]
angeführten Inhalte.

### 1.5.1 Hinweis auf offene Punkte

Themen, die noch intern geklärt werden müssen oder eine Entscheidung seitens
der Gesellschafter erfordern, sind wie folgt im Dokument gekennzeichnet:

Beispiel für einen offenen Punkt.

### 2 Systemüberblick

Die folgende Abbildung zeigt einen Systemüberblick für die Primärsysteme
verordnende LEI und abgebende LEI.

![Abbildung-1][Abbildung-1]

Die von den Primärsystemen direkt erreichbaren Produkttypen der TI sind

 ---> UL

Identity Provider

Der Identity Provider (IDP) ist ein Nutzerdienst der TI-Plattform, welcher die
Authentifizierung von Nutzern und die Bereitstellung bestätigter
Identitätsmerkmale der Nutzer als Plattformleistungen bereitstellt. Der IDP
bietet außerdem die Möglichkeit, bereits erfolgte Authentifizierungen eines
Nutzers im Sinne eines Single Sign-on nachzunutzen.

Der IDP besteht aus dem zentralen Nutzerdienst und einer dezentralen Komponente,
dem Authentisierungsmodul des IDP.

Authentisierungsmodul des IDP

Das Authentisierungsmodul ergänzt den IDP, um auf dem Gerät des Nutzers die
fachliche Logik für die Authentisierung entsprechend dem OpenID
Connect-Standard sowie das Challenge Response Verfahren mit der SMC-B
umzusetzen. Der Zugriff auf die Smart Card des Nutzers erfolgt über die
Außenschnittstellen des Konnektors.

Das Authentisierungsmodul wird durch das Primärsystem implementiert.

Konnektor

Der Konnektor bildet das Gateway zum zentralen Netz der TI, d.h. es routet die
Anfragen an den IDP und den E-Rezept-Fachdienst.

Für die Signatur des E-Rezepts bzw. des Abgabedatensatzes wird die CMS-Signatur
(CAdES) des Konnektors genutzt.

Der Konnektor kapselt die Zugriffe auf die SMC-B für die Authentisierung.

E-Rezept-Fachdienst

Der E-Rezept-Fachdienst ist ein offener fachanwendungsspezifischer Dienst in der
TI, welcher Workflow zu den E-Rezepten umsetzt.

### 3 Systemkontext

### 3.1 E-Rezept Status

Ein E-Rezept durchläuft vom Erstellen bis zum Einlösen verschiedene Status.
Abhängig vom Status sind in den Primärsystemen verschiedene Anwendungsfälle
möglich.

Der Status wird im E-Rezept-Fachdienst verwaltet. Ist ein Anwendungsfall
aufgrund des Status nicht zulässig, antwortet der E-Rezept-Fachdienst mit
einer Fehlermeldung.

TAB_ILFERP_001 listet die möglichen Status.

<table><tr><th>
E-Rezept Status

</th><th>
Task Status

</th><th>
Beschreibung

</th></tr><tr><td>
initialisiert

</td><td>
draft

</td><td>
 ---> UL

</td></tr><tr><td>
offen

</td><td>
ready

</td><td>
 ---> UL

</td></tr><tr><td>
in Abgabe (gesperrt)

</td><td>
in-progress

</td><td>
 ---> UL

</td></tr><tr><td>
quittiert

</td><td>
completed

</td><td>
 ---> UL

</td></tr><tr><td>
gelöscht

</td><td>
cancelled

</td><td>
 ---> UL

</td></tr></table>

Die AbbildungABB_ILFERP_002 zeigt die Anwendungsfälle, welche zu
Statusübergängen führen.

![Abbildung-2][Abbildung-2]

Für weitere Details zu Statusübergängen siehe [gemKPT_SysD_TI] und
[gemSysL_eRp].

### 3.2 FHIR-Ressourcen

Für die Spezifikation der Schnittstellen in dieser Anwendung wird der Standard
FHIR (Fast Healthcare Interoperability Resources) verwendet. In FHIR werden
Datenstrukturen und Elemente in "Ressourcen" beschrieben, welche über
standardisierte Schnittstellen zwischen verschiedenen Komponenten übertragen
werden können. Die Daten werden dabei in XML oder in JSON repräsentiert.

Durch die Primärsysteme werden folgende FHIR-Ressourcen in den Schnittstellen
zum E-Rezept-Fachdienst verwendet:

 ---> UL

Für eine Beschreibung der Ressourcen siehe [gemSpec_DM_eRp].

Der FHIR Standard erlaubt eine Darstellung von FHIR-Ressourcen im JSON als auch
XML Format. Fürdie FHIR-Ressourcen wird ausschließlich die XML Darstellung
genutzt.

### 4 Übergreifende Festlegungen

### 4.1 Logging und Meldungen

**A_20088 - PS: Schreiben eines Fehlerprotokolls**

Das Primärsystem SOLL alle in der Kommunikation mit den Diensten der TI
auftretenden Fehler und Warnungen in ein dediziertes Fehlerprotokoll schreiben
und diese Protokollinformationen für Supportmaßnahmen über eine Zeitraum von
mindestens 14 Tagen zur Verfügung halten. **[\<=]**

**A_20089 - PS: Anzeige von Meldungen**

Das Primärsystem SOLL alle in der Kommunikation mit den Diensten der TI
auftretenden Probleme für den Benutzer verständlich anzeigen und dabei
erkennen lassen, ob durch den Anwender oder den verantwortlichen
Leistungserbringer Maßnahmen zur Behebung eingeleitet werden müssen. **[\<=]**

**A_20884 - PS: Exponential Backoff bei Verbindungsfehlern**

Das Primärsystem SOLL bei serverseitigen Fehlermeldungen, die auf eine
Überlastung des Zielsystems schließen lassen (z.B. http-status 5xx, 429 - too
many requests, etc.), erneute Verbindungsversuche nach dem Prinzips des
Exponential Backoffs [ExpBack] durchführen. **[\<=]**

### 4.2 Namensauflösung

Der E-Rezept-Fachdienst ist für Primärsysteme gemäß den Festlegungen in
[gemSpec_FD_eRp] über die Adresse erp.zentral.erp.splitdns.ti-dienste.de
lokalisierbar. Das Redundanzkonzept sieht mehrere Instanzen vor, die über
verschiedene IP-Adressen angesprochen werden. Folglich liefert die
DNS-Namensauflösung verschiedene IP-Adressen zum FQDN zurück. Diese Adressen
werden vom DNS-Server in zufälliger Reihenfolge geschickt, sodass es legitim
ist, immer den ersten Eintrag für den folgenden Operationsaufruf zu verwenden.
Üblicherweise wird die DNS-Auflösung vom Betriebssystem gekapselt, eine
Lastverteilung am E-Rezept-Fachdienst ergibt sich aus der zufälligen
Reihenfolge der IP-Adressen der DNS-Abfrage.Unspezifiziert ist das Verhalten,
wenn die erste Zieladresse nicht erreichbar ist. Empfehlenswert ist die Nutzung
der anderen/weiteren IP-Adressen der DNS-Abfrage. Es muss aber angenommen
werden, dass bestimmte Betriebssysteme bzw. Laufzeitumgebungen des
Primärsystems diese mit der Nutzung der ersten Adresse bereits verworfen
haben. Bei Nicht-Erreichbarkeit des Zielhosts der ersten IP-Adresse wird daher
empfohlen, weitere Verbindungsversuche auf Basis einer neuen DNS-Abfrage zu
tätigen, mit dem Ziel, eine andere IP-Adresse an erster Stelle der DNS-Antwort
zu erhalten, als die des nicht erreichbaren Zielhosts.

Das Primärsystem erreicht den E-Rezept-Fachdienst und IDP über den Konnektor
geroutet. Je nach Installationsumgebung des Primärsystems ist der Konnektor
evtl. nicht das Default-Gateway. Um diese offenen Fachdienste zu erreichen,
müssen ggfs. feste Routen und eine DNS-Konfiguration für das [Split-DNS] pro
Arbeitsplatz-Computer im Rahmen der Installation festgelegt werden.

**A_21468 - PS: Handbuch-Hinweis Konnektor Default-Gateway für offene
Fachdienste**

Der Hersteller des Primärsystems MUSS in seinem Handbuch auf die verschiedenen
Installationsszenarien und Konfigurationen des Konnektors in
[gemSpec_KON#Anhang K] hinweisen, damit der Konnektor im Rahmen der
Installation und Konfiguration des PS für das E-Rezept als Default-Gateway
bzw. notwendige Routinginformationen und DNS-Konfigurationen im Gerät
festgelegt werden können. **[\<=]**

Der Hersteller des Primärsystems kann die Konfiguration zum
Installationszeitpunkt unterstützen, indem er bspw. eine Batch-Datei zum
Hinterlegen der Netzwerkeinstellungen für die verschiedenen FQDN für
E-Rezept-Fachdienst und IDP über den Konnektor als Gateway bereitstellt.

Mit dem E-Rezept wird ein Split-DNS eingeführt, um die Domainadresse
"ti-dienste.de" auch im zentralen Netz für Fachdienste nutzen zu können. Für
diesen Zweck wird "splitdns.ti-dienste.de" in die Bestandsnetzkonfiguration des
Konnektors ergänzt. Der Konnektor übernimmt dann für die Domain
splitdns.ti-dienste.de die Namensauflösung. Für lokale
Netzwerkinstallationen, die den Konnektor nicht als Nameserver und Gateway in
ihrem Netzwerk nutzen, müssen entsprechende Netzwerkkonfigurationen manuell
vorgenommen werden.

Die gematik plant, ergänzende Informationen zu Netzwerkkonfigurationen zu
veröffentlichen, bspw. auf der github-Seite https://github.com/gematik .

### 5 Funktionsmerkmale

### 5.1 Allgemein

### 5.1.1 Kommunikation zu den Diensten der TI

Das PS einer verordnenden bzw. abgebenden LEI nutzt TLS-Verbindungen für die
Kommunikation zu den Diensten der TI. Es verbindet sich mit dem
E-Rezept-Fachdienst und einem Identity Provider.

**A_19451-01 - PS: Lokalisierung E-Rezept-Fachdienst**

Das Primärsystem MUSS für die zur Kommunikation mit dem E-Rezept-Fachdienst
die FQDNs als Lokalisierungsinformationen in einer DNS-Abfrage gemäß
[gemSpec_FD_eRP#5.1 Servicelokalisierung] nutzen. **[\<=]**

Die Abfrage beim Namensdienst der TI erfolgt über einen DNS-Lookup. Hierfür
muss der Konnektor als DNS-Resolver konfiguriert sein.

**A_19744 - PS: Endpunkt Schnittstelle E-Rezept-Fachdienst**

Das Primärsystem MUSS die URL für die Kommunikation mit dem
E-Rezept-Fachdienst gemäßhttps://\<FQDN aus DNS Lookup\>:443/ bilden.
**[\<=]**

Die Informationen zu den Endpunkten des Identity Providers ermittelt das
Primärsystem aus dem Discovery Document. Siehe auch
[gemSpec_IDP_Dienst#Registrierung von Endgerät und Anwendungsfrontend]. Das
Discovery Document ist vom IDP-Dienst unter der
URL/.well-known/openid-configurationabrufbar. 

**A_19234 - PS: Kommunikation über TLS-Verbindung**

Das Primärsystem MUSS für die Anwendungsfälle der Anwendung E-Rezept mit den
Diensten der TI ausschließlich über TLS kommunizieren. **[\<=]**

Es gelten die Vorgaben aus [gemSpec_Krypt] für TLS.

**A_19235 - PS: Unzulässige TLS-Verbindungen ablehnen**

Das Primärsystem MUSS bei jedem Verbindungsaufbau den Dienst der TI anhand
seines TLS-Zertifikats authentifizieren und MUSS die Verbindungen ablehnen,
falls die Authentifizierung fehlschlägt. **[\<=]**

**A_20015-01 - PS: HTTP-Header user-agent**

Das Primärsystem MUSS in alle HTTP-Requests an Dienste der TI im äußeren
HTTP-Request den HTTP-Headeruser-agent gemäß [RFC7231] mit
\<Produktname\>/\<Produktversion\> \<Herstellername\>/\<client_id\> mit

 ---> UL

des Primärsystems befüllen. **[\<=]**

**A_21242 - PS: Unterstützung Konnektorversion**

Das Primärsystem MUSS Konnektoren ab PTV 3 für das E-Rezept unterstützen.
**[\<=]**

**A_21568 - PS: HTTP-Header X-erp-user**

Das Primärsystem MUSS in alle Anfragen an den E-Rezept-Fachdienst im äußeren
HTTP-Request den HTTP-Header "X-erp-user" mit dem Wert "l" (kleines L)
einfügen. **[\<=]**

**A_21569 - PS: HTTP-Header X-erp-resource**

Das Primärsystem MUSS in alle Anfragen an den E-Rezept-Fachdienst im äußeren
HTTP-Request den HTTP-Header "X-erp-resource" mit dem Wert gemäß der
angefragten Ressource im FHIR-Request einfügen. **[\<=]**

<table><tr><th>
Operation

</th><th>
X-erp-resource

</th></tr><tr><td>
DELETE /Communication/\<id\>

</td><td>
Communication

</td></tr><tr><td>
GET /Communication/

</td><td>
Communication 

</td></tr><tr><td>
GET /Communication/\<id\>

</td><td>
Communication 

</td></tr><tr><td>
GET /Device/

</td><td>
Device

</td></tr><tr><td>
GET /metadata/

</td><td>
metadata

</td></tr><tr><td>
POST /Communication

</td><td>
Communication 

</td></tr><tr><td>
POST /Task/$create

</td><td>
Task

</td></tr><tr><td>
POST /Task/\<id\>/$abort

</td><td>
Task

</td></tr><tr><td>
POST /Task/\<id\>/$accept

</td><td>
Task

</td></tr><tr><td>
POST /Task/\<id\>/$activate

</td><td>
Task

</td></tr><tr><td>
POST /Task/\<id\>/$close

</td><td>
Task

</td></tr><tr><td>
POST /Task/\<id\>/$reject

</td><td>
Task

</td></tr></table>

### 5.1.2 Verschlüsselte Kommunikation zur VAU des E-Rezept-Fachdienstes

Die Kommunikation zum E-Rezept-Fachdienst wird zusätzlich zu TLS über einen
sicheren Kanal (Verschlüsselung auf Http-Ebene) zwischen dem PS und der
Vertrauenswürdigen Ausführungsumgebung (VAU) im E-Rezept-Fachdienst gesichert.

**A_19741 - PS: Umsetzung sicherer Kanal zur VAU des E-Rezept-Fachdienstes**

Das Primärsystem MUSS für alle Anfragen an den E-Rezept-Fachdienst für

 ---> UL

das Kommunikationsprotokoll zwischen E-Rezept-VAU und E-Rezept-Clients in der
Rolle E-Rezept-Client nutzen **[\<=]**

Für Informationen zum Kommunikationsprotokoll zwischen E-Rezept-FdV und
der VAU des E-Rezept-Fachdienstes siehe und .

Alternativ zur Umsetzung des TUC_PKI_018 gemäß [] soll das Primärsystem für
die Prüfung des VAU-Zertifikates die VerifyCertificate Operation des
Konnektors nutzen.

Folgendes kann umgesetzt werden:

(1) Beziehen des VAU-Zertifikat von /VAUCertificate

(2) Lokales Speichern der aktuellen Zeit mit dem VAU-Zertifikat als Tupel

(3) Prüfen des VAU-Zertifikates mittels der Konnektor-Operation
VerifyCertificate

(4) Abbrechen falls INVALID

(5) if (get_current_time() \< gespeicherte Zeit + 12h) { VAU-Zertifikat wird
als gültig angesehen, Nutzen des VAU-Zertifikat }

     if (get_current_time() \>= gespeicherte Zeit + 12h) { VAU-Zertifikat
neu beziehen, siehe (1)}

Hinweis zum Fehlerhandling: Nur wenn der äußere Response der
E-Rezept-Fachdienstes den Response-Code 200 liefert, enthält der payload eine
mittels VAU-Protokoll verschlüsselte Response. Liefert der äußere Response
eine Code \>= 400, ist im VAU-Protokoll ein Fehler aufgetreten. Das PS muss
nicht versuchen, den payload zu entschlüsseln.

### 5.1.3 Zertifikatsprüfung

Das Primärsystem der verordnenden und abgebenden LEI verwendet bei den
inTAB_ILFERP_012 dargestellten Aktivitäten Zertifikate.

<table><tr><th>
Aktivität

</th><th>
Zertifikat der TI

</th><th>
Zertifikatstyp

</th><th>
Rollen-OID

</th><th>
Nutzung

</th></tr><tr><td>
TLS-Verbindungsaufbau zum E-Rezept-Fachdienst

</td><td>
nein

</td><td>
TLS Internet Zertifikat

</td><td>
n/a

</td><td>
aktiv

</td></tr><tr><td>
TLS-Verbindungsaufbau zum Verzeichnisdienst der TI

</td><td>
nein

</td><td>
TLS Internet Zertifikat

</td><td>
n/a

</td><td>
aktiv

</td></tr><tr><td>
TLS-Verbindungsaufbau zum IDP

</td><td>
nein

</td><td>
TLS Internet Zertifikat

</td><td>
n/a

</td><td>
aktiv

</td></tr><tr><td>
Aufbau sicherer Kanal zur VAU des E-Rezept-Fachdienstes

</td><td>
ja

</td><td>
C.FD.ENC

</td><td>
oid_erp-vau

</td><td>
aktiv

</td></tr><tr><td>
Nur für PS der abgebenden LEI:  
Signaturzertifikat Fachdienst

</td><td>
ja

</td><td>
C.FD.SIG

</td><td>
oid_erezept

</td><td>
aktiv

</td></tr></table>

Es gelten folgende übergreifende Festlegungen für die Prüfung aktiv durch das
E-Rezept-FdV genutzter Zertifikate.

**A_20769 - PS: verpflichtende Zertifikatsprüfung**

Das Primärsystem MUSS alle Zertifikate, die es aktiv verwendet (bspw.
TLS-Verbindungsaufbau), auf Integrität und Authentizität prüfen. Falls die
Prüfung kein positives Ergebnis ("gültig") liefert, so MUSS es die von dem
Zertifikat und den darin enthaltenen Attributen (bspw. öffentliche Schlüssel)
abhängenden Arbeitsabläufe ablehnen.Das Primärsystem MUSS alle öffentlichen
Schlüssel, die es verwenden will, auf eine positiv verlaufene
Zertifikatsprüfung zurückführen können. **[\<=]**

"Ein Zertifikat aktiv verwenden" bedeutet im Sinne von A_20769, dass ein
Primärsystem einen dort aufgeführten öffentlichen Schlüssel innerhalb einer
kryptografischen Operation (Signaturprüfung, Verschlüsselung,
Signaturprüfung von öffentlichen (EC)DH-Schlüsseln etc.) nutzt. Erhält ein
Primärsystem bspw. einen Access-Token, in dem Signaturen und Zertifikate
enthalten sind, und behandelt es diesen Token als opakes Datenobjekt, ohne die
Zertifikate darin gesondert zu betrachten, dann verwendet das Primärsystem
diese Zertifikate im Sinne von A_20769 passiv.

### 5.1.3.1 Zertifikatsprüfung von Zertifikaten der TI

**A_20764 - PS: Prüfung TI-Zertifikate**

Das Primärsystem MUSS bei der Prüfung von X.509-Zertifikaten der TI
den CertificateService des Konnektors mit der
OperationVerifyCertificategemäß [gemSpec_Kon#4.1.9.5.3] verwenden und dabei

 ---> UL

Das Primärsystem MUSS bei Prüfung eines C.FD.ENC den Rückgabewert in 

RoleList

gegen die erwartete Rollen-OID gemäß TAB_ILFERP_012 prüfen und bei
Abweichungen die Benutzung des Zertifikats für einen Verbindungsaufbau zur VAU
ablehnen. **[\<=]**

<table><tr><td>
Die Primärsysteme prüfen im Rahmen der Anwendungsfälle des E-Rezepts mittels
der Konnektor-Operation VerifyCertificate (A_20764) u.a. die folgenden
Zertifikate der TI: 

 ---> UL

Dies sind ECC-Zertifikate, deren Verwendung erst ab PTV4-Konnektor unterstützt
werden.

Für (Z)PVS wird angenommen, dass sie In den Praxen PTV4-Konnektoren vorfinden,
da zeitgleich die Anwendung ePA flächendeckend eingeführt wird, welche den
PTV4-Konnektor bedingt.

Für Apotheken kann nicht vorausgesetzt werden, dass mindestens ein
PTV4-Konnektor vorhanden ist. Hier können auch PTV3-Konnektoren genutzt werden.

Wird ein ECC-Zertifikat mittels VerifyCertificate eines PTV3-Konnektors
geprüft, dann antwortet diese Operation  mit einem Fehler (Konnektor Rise
Fehlercode=1025, KoCo + Secunet Fehlercode=1027).

Im Fall, dass bei der Prüfung der obigen Zertifikate die genannten Fehler
auftreten, muss ein AVS die alternative Zertifikatsprüfung analog zum
E-Rezept-FdV gemäß [gemSpec_Krypt#A_21218] nutzen.

Dies bedeutet, dass die AVS-Hersteller beide Prüfverfahren implementieren
müssen.

Der E-Rezept-Fachdienst stellt den Primärsystemen für die alternative
Zertifikatsprüfung die benötigten Ressourcen /CertList und /OCSPList an der
Schnittstelle im zentralen Netz der TI übergangsweise zur Verfügung.
"ee_certs" in CertList beinhaltet genau nur die oben gelisteten Zertifikate.

Dies stellt eine Übergangslösung dar, welche aufgrund der oben vorgeschlagenen
Implementierung automatisch entfällt, wenn die Apotheke einen PTV4-Konnektor
einsetzt. Das BSI hat der Übergangslösung bis zum 31.03.2022 zugestimmt. Bis
zu diesem Zeitpunkt ist ein Update von PTV3-Konnektoren vorzunehmen.

</td></tr></table>

### 5.1.3.2 Zertifikatsprüfung von Internet-Zertifikaten

Folgende Vorgaben gelten für die Prüfung von Internet-Zertifikaten.

**A_20091 - PS: Prüfung der Zertifikate für TLS-Verbindung zu
E-Rezept-Fachdienst und Identity Provider**

Das Primärsystem MUSS für die Prüfung eines Zertifikats für den
TLS-Verbindungsaufbau zum E-Rezept-Fachdienst und IDP das Zertifikat auf ein
CA-Zertifikat einer CA, die die "CA/Browser Forum Baseline Requirements for the
Issuance and Management of Publicly-Trusted Certificates"
(https://cabforum.org/baseline-requirements-documents/) erfüllt,
kryptographisch (Signaturprüfung) zurückführen können. Ansonsten MUSS es
das Zertifikat als "ungültig" bewerten.Das PS MUSS die zeitliche Gültigkeit
des Zertifikats prüfen. Falls diese Prüfung negativ ausfällt, muss es das
Zertifikat als "ungültig" bewerten.  **[\<=]**

Hinweis: Der erste Teil von A_20091 ist gleichbedeutend damit, dass das
CA-Zertifikat im Zertifikats-Truststore eines aktuellen Webbrowsers ist.

### 5.1.4 Authentifizierung der LEI

Die LEI authentisiert sich für Zugriffe auf Dienste der TI im Rahmen der
Anwendung E-Rezept gegenüber dem IDP-Dienst. 

Das Primärsystem übernimmt hierbei, wenn kein gültiger "ACCESS_TOKEN"
vorliegt, neben der Rolle der Anwendungsfrontend-Applikation auch die Aufgabe
des Authenticator-Moduls (der in [RFC6749 # section-4.1] beschriebene t), um
das zum Zugriff auf Fachdienste benötigte "ACCESS_TOKEN" zu beantragen.
Hierfür wird am Authorization-Endpunkt des IDP-Dienstes ein
"AUTHORIZATION_CODE" beantragt, der nach erfolgreicher Verifikation am
Token-Endpunkt des IDP-Dienstes gegen ein "ID_TOKEN" und ein "ACCESS_TOKEN"
getauscht wird.

Die für die Beantragung des "AUTHORIZATION_CODE" im
Challenge-Response-Verfahren notwendige elektronische Signatur mit der
AUT-Identität einer SMC-B der LEI lässt das Primärsystem über die
Schnittstellen des Konnektors generieren. Im Fall einer bereits
freigeschalteten Smartcard passiert diese Aktion ohne Interaktion mit dem
Nutzer im Hintergrund. 

Der IDP-Dienst führt die Identifikation der LEI durch, und stattet diese
anschließend mit "ID_TOKEN" gemäß [openid-connect-core 1.0 # IDToken] und
"ACCESS_TOKEN" gemäß [RFC6749 # section-1.4 & RFC6749 # section-5] aus. Dabei
wurde aus Sicherheitsaspekten der "Authorization Code Grant" gemäß [RFC6749 #
section-4.1] gewählt, welcher in identischem Ablauf auch für mobile
Endgeräte mit getrennten Komponenten für Authenticator-Modul und
Anwendungsfrontend anwendbar ist. Um dem erforderlichen Sicherheitsniveau
gerecht zu werden, wird zudem die Verwendung von PKCE (Proof Key for Code
Exchange by OAuth Public Clients) gemäß [RFC7636] vorgesehen.

Der IDP-Dienst selbst teilt sich in mehrere statisch adressierte Teildienste
auf. Diese umfassen:

 ---> UL

Für weitere Informationen zum IDP-Dienst und zum Ablauf der Authentisierung
siehe [gemSpec_IDP_Dienst] und [gemSpec_IDP_Frontend].

Die gematik wird Beispielsätze und weitere Hilfestellungen auf ihrer Webseite
in jeweils aktueller Form bereitstellen.

### 5.1.4.1 Übergreifende Festlegungen zur Nutzung des IDP-Dienstes

Zur Nutzung des IDP-Dienstes gelten einige grundlegende Voraussetzungen, welche
das PS erfüllen muss.

**A_20654 - Registrierung des Primärsystems**

Der Hersteller des Primärsystems MUSS sich über einen organisatorischen
Prozess beim Anbieter des IDP-Dienstes für die Dienste, für welche Token
abgerufen werden sollen, registrieren. Der IDP-Dienst vergibt dabei eine
"client_id". Diese "client_id" MUSS vom Primärsystem bei Nutzung des
IDP-Dienstes übertragen werden. **[\<=]**

**A_20655 - Regelmäßiges Einlesen des Discovery Document**

Das Primärsystem MUSS das Discovery Document (DD) [RFC8414] regelmäßig alle
24 Stunden einlesen und auswerten, und danach die darin aufgeführten URI zu
den benötigten öffentlichen Schlüsseln (PUKs) und Diensten verwenden. Der
Downloadpunkt wird als Teil der organisatorischen Registrierung des
Primärsystems beim IDP-Dienst übergeben. Das Primärsystem MUSS den
Downloadpunkt des Discovery Document als konfigurierbaren Parameter
speichern.    **[\<=]**

**A_20656-01 - Prüfung der Signatur des Discovery Document**

Das Primärsystem MUSS die JWS (JSON Web Signature) [RFC7515 # section-3 -
Compact Serialization] Signatur des Discovery Document auf mathematische
Korrektheit sowie über die Funktion "VerifyCertificate" des Konnektors gemäß
[gemSpec_Kon#4.1.9.5.3] bzw. [gemILF_PS#4.4.4.3] auf Gültigkeit des
ausstellenden Zertifikates innerhalb der TI prüfen. **[\<=]**

Hinweis:Der genaue Aufbau entspricht [gemSpec_IDP_Dienst#Kapitel 7.7 Aufbau des
Discovery Document].

Bei Aufruf der Funktion "VerifyDocument" an der Außenschnittstelle des
Konnektors ist es nicht möglich, direkt auch eine Prüfung des Zertifikatstyps
und der Rollen-OID durchzuführen.

**A_20657 - Prüfung der Signatur des Discovery Document**

Das Primärsystem MUSS die Signatur des Discovery Document auf ein zeitlich
gültiges C.FD.SIG-Zertifikat mit der Rollen-OID "oid_idpd" zurückführen
können. **[\<=]**

Hinweis: Zur Durchführung der Prüfungen gemäß A_20657 und ähnlicher
Anforderungen ist zu verifizieren, ob im Feld certificatePolicies (2.5.29.32)
des Zertifikates der richtige Zertifikatstyp FD.SIG (1.2.276.0.76.4.203)
gemäß [gemSpec_OID#Tabelle Tab_PKI_405] eingetragen ist und sich in der
Admission (1.3.36.8.3.3) des Zertifikats die richtige "oid_idpd"
(1.2.276.0.76.4.260) findet.

**A_20658 - Sicheres Löschen der Token**

Das Primärsystem MUSS, wenn es absichtlich gestoppt oder deaktiviert wird,
vorhandene "ACCESS_TOKEN", "ID_TOKEN" und "AUTHORIZATION_CODE"-Objekte sicher
aus dem RAM löschen. **[\<=]**

Darüber hinaus gelten für die Kommunikation mit dem IDP-Dienst die Vorgaben
aus.

**A_21337 - Löschung von TOKEN bei zeitlichem Ablauf**

Das Primärsystem MUSS vorhandene "ACCESS_TOKEN", "ID_TOKEN" und
"AUTHORIZATION_CODE"-Objekte nach Ablauf ihrer Gültigkeit sicher löschen. 
**[\<=]**

**A_21338 - Sichere Speicherung der Token**

Das Primärsystem MUSS empfangene "ACCESS_TOKEN", "ID_TOKEN" und
"AUTHORIZATION_CODE"-Objekte gegen unberechtigten Zugriff schützen.  **[\<=]**

### 5.1.4.2 Abruf von Token beim IDP-Dienst

Im Folgenden wird der Ablauf der Token-Beantragung und Ausstellung detaillierter
beschrieben und – wo für das Primärsystem notwendig – mit entsprechenden
Anforderungen hinterlegt. Im ersten Schritt erzeugt sich das Primärsystem
einen zufälligen "CODE_VERFIER" und bildet darüber den Hash "CODE_CHALLENGE".
Mit dessen Hilfe kann es sich im späteren Verlauf als valider Empfänger des
Tokens ausweisen.

**A_20659 - Erzeugen des CODE_VERIFIER**

Das Primärsystem MUSS zur Laufzeit einen "CODE_VERIFIER" (Zufallswert) gemäß
[RFC7636 # section-4.1] bilden. Der "CODE_VERIFIER" MUSS eine Länge von
mindestens 43 und maximal 128 Zeichen enthalten. Dabei sind die folgenden
Zeichen zulässig: [A-Z] / [a-z] / [0-9] / "-" / "." / "_" / "~". **[\<=]**

**A_20660 - Erzeugen des Hash-Werts des CODE_VERIFIER**

Das Primärsystem MUSS über den "CODE_VERIFIER" einen SHA256-HASH-Wert, die
sogenannte "CODE_CHALLENGE", gemäß [RFC7636 # section-4.2] bilden. 

code_challenge = BASE64URL-ENCODE(SHA256(ASCII(code_verifier))) **[\<=]**

Anschließend werden der gehashte Zufallswert und die notwendigen Angaben als
"CODE_CHALLENGE" beim Authorization-Endpunkt des IDP-Dienstes eingereicht.

**A_20661 - Anfrage des "AUTHORIZATION_CODE" für ein "ACCESS_TOKEN"**

Das Primärsystem MUSS den Antrag zum "AUTHORIZATION_CODE" für ein
"ACCESS_TOKEN" beim Authorization-Endpunkt (URI_AUTH) in Form eines HTTP/1.1
GET Request stellen und dabei die folgenden Attribute anführen: •
"response_type"• "scope"• "client_id"• "redirect_uri"• "code_challenge"
(Hashwert des "code_verifier") [RFC7636 # section-4.2]•
"code_challenge_method" HASH-Algorithmus (S256) [RFC7636 # section-4.3]
**[\<=]**

Der Authorization-Endpunkt legt nun eine "session_id" an, stellt alle nötigen
Informationen zusammen und erzeugt das "CHALLENGE_TOKEN".Darüber hinaus stellt
der Authorization-Endpunkt den im Claim des entsprechenden Fachdienstes
vereinbarten "Consent" zusammen, welcher die für dessen Funktion notwendigen
Attribute beinhaltet.

Der Authorization-Endpunkt liefert als Response zur Anfrage des
"AUTHORIZATION_CODE" einen "CHALLENGE_TOKEN", um die Identität der LEI zu
bestätigen, sowie den "consent" des im "scope" angefragten Fachdienstes.

**A_20662 - Annahme des "user_consent" und des "CHALLENGE_TOKEN"**

Das Primärsystem MUSS den "user_consent"und den "CHALLENGE_TOKEN" vom
Authorization-Endpunkt des IDP-Dienstes annehmen. Der Authorization-Endpunkt
liefert diese als Antwort auf den Authorization-Request des Primärsystems.
**[\<=]**

**A_20663-01 - Prüfung der Signatur des CHALLENGE_TOKEN**

Das Primärsystem MUSS die Signatur des "CHALLENGE_TOKEN" gegen den aktuellen
öffentlichen Schlüssel des Authorization-Endpunktes "PUK_IDP_SIG" prüfen.
Liegt dem Primärsystem der öffentliche Schlüssel des
Authorization-Endpunktes noch nicht vor, MUSS es diesen gemäß dem
"kid"-Parameter "puk_idp_sig" aus dem Discovery Document abrufen. **[\<=]**

Das Primärsystem verwendet nun die AUT-Identität der SM-B der LEI und deren
Konnektor, um das gehashte "CHALLENGE_TOKEN" des IDP-Dienstes zu signieren.
Wenn es sich um eine erstmalige Anmeldung des Benutzers bei diesem Fachdienst
handelt, werden diesem darüber hinaus die für den Zugriff übermittelten
Daten der LEI angezeigt.

**A_20664 - Bestätigung des Consent**

Das Primärsystem MUSS dem Nutzer einmalig vor der Signatur der "challenge"
anzeigen, dass ein tokenbasierter Zugriff auf den im "scope" genannten Dienst
initiiert wird. **[\<=]**

Hinweis: Die erfolgte Zustimmung des Nutzers darf gespeichert werden und weitere
Abfragen können entfallen.

**A_20665-01 - Signatur der Challenge des IdP-Dienstes**

Das Primärsystem MUSS für das Signieren des CHALLENGE_TOKEN des IdP-Dienstes
mit der Identität ID.HCI.AUT der SM-B die Operation ExternalAuthenticate des
Konnektors gemäß [gemSpec_Kon#4.1.13.4] bzw. [gemILF_PS#4.4.6.1] verwenden
und als zu signierende Daten BinaryString den SHA-256-Hashwert des
CHALLENGE_TOKEN in Base64-Codierung übergeben. **[\<=]**

Hinweis: Der Aufbau der Anfrage und der einzureichenden Objekte entspricht
[gemSpec_IDP_Dienst#Kapitel 7.3 Authentication Request].

Hinweis: Aktuell befinden sich vornehmlich SMC-B der Generation G2 im Feld. Bei
diesen ist für die Signatur, entsprechend dem Default des Konnektors, das
Verfahren RSASSA-PSS zu nutzen.Wenn eine SMC-B G2.1 Karte vorhanden ist, ist
ECDSA zu priorisieren. Beide Verfahren werden durch den IDP-Dienst unterstützt.

Für weitere Informationen siehe Kapitel "Als Nutzer gegenüber der
Telematikinfrastruktur authentisieren" in der API-Schnittstelle [E-Rezept API
Dokumentation].

**A_20666-01 - Auslesen des Authentisierungszertifikates**

Das Primärsystem MUSS das Zertifikat ID.HCI.AUT der SM-B über die Operation
ReadCardCertificate des Konnektors gemäß [gemSpec_Kon#4.1.9.5.2] bzw.
[gemILF_PS#4.4.4.2] auslesen. **[\<=]**

Hinweis: Im Rahmen der Signatur wird auf privates Schlüsselmaterial
zugegriffen. Die verwendeten Karten müssen sich daher in einem erhöhten
Sicherheitszustand befinden, der ggf. erst durch eine PIN-Eingabe hergestellt
werden muss. Das Primärsystem muss den Kartenzustand abfragen und die Karte
ggf. durch den Nutzer freischalten lassen. Mit dem (optionalen) Einblenden
eines Hinweises der Form "Bitte beachten Sie die Anzeige an Ihrem
Kartenterminal" muss das Primärsystem dafür sorgen, dass die Abfrage einer
PIN-Eingabe am Kartenterminal vom Benutzer nicht übersehen wird.

Anschließend werden die signierte "challenge" und das verwendete
Authentisierungszertifikat der Smartcard an den IDP-Dienst übermittelt.

**A_20667-01 - Response auf die Challenge des Authorization-Endpunktes**

Das Primärsystem MUSS das eingereichte "CHALLENGE_TOKEN" zusammen mit der von
der Smartcard signierten Challenge-Signatur "signed_challenge" (siehe A_20665)
und dem Authentifizierungszertifikat der Smartcard (siehe A_20666), mit dem
öffentlichen Schlüssel des Authorization-Endpunktes "PUK_IDP_ENC"
verschlüsselt, an diesen in Form eines HTTP-POST-Requests senden. **[\<=]**

Hinweis: DerAufbau der Anfrage und der einzureichenden Objekte entspricht
[gemSpec_IDP_Dienst#Kapitel 7.3 Authentication Request].

Hinweis: Das Signieren und Verschlüsseln des "CHALLENGE_TOKEN" ist durch die
Verwendung eines Nested JWT [angelehnt an den folgenden Draft:
https://tools.ietf.org/html/draft-yusef-oauth-nested-jwt-03] zu realisieren. Im
cty-Header ist "NJWT" zu setzen, um anzuzeigen, dass es sich um einen Nested
JWT handelt. Das Signieren wird dabei durch die Verwendung einer JSON Web
Signature (JWS) [RFC7515 # section-3 - Compact Serialization] gewährleistet.
Die Verschlüsselung des signierten Token wird durch die Nutzung der JSON Web
Encryption (JWE) [RFC7516 # section-3] sichergestellt. Als
Verschlüsselungsalgorithmus ist ECDH-ES (Elliptic Curve Diffie-Hellman
Ephemeral Static key agreement) vorgesehen.

Der Authorization-Endpunkt validiert nun die "session" sowie die
"signed_challenge" und prüft das Zertifikat der LEI. Anschließend verknüpft
er die "session" mit der Identität aus dem Authentisierungszertifikat und
erstellt einen "AUTHORIZATION_CODE", welchen er als Antwort zurücksendet.

Das Primärsystem empfängt nun diesen "AUTHORIZATION_CODE" vom IDP-Dienst und
reicht ihn zusammen mit dem KEY_VERIFIER beim Token-Endpunkt ein.

**A_20668 - Annahme des "AUTHORIZATION_CODE"**

Das Primärsystem MUSS den vom Authorization-Endpunkt als Antwort auf die
signierte Challenge gesendeten "AUTHORIZATION_CODE" verarbeiten. Das
Primärsystem MUSS das "AUTHORIZATION_CODE" ablehnen, wenn dieser außerhalb
der mit dem Authorization-Endpunkt etablierten TLS-Verbindung übertragen wird.
**[\<=]**

**A_21333 - Erzeugung des "Token-Key"**

Das Primärsystem MUSS vor dem Abrufen von ID_Token und ACCESS_Token einen
zufälligen 256bit-AES-Schlüssel ("Token-Key") erzeugen. **[\<=]**

**A_21334 - Erzeugung des "KEY_VERIFIER"**

Das Primärsystem MUSS den "KEY_VERIFIER" bilden, indem "Token-Key" und
"CODE_VERIFIER" in einem JSON-Objekt kodiert werden. **[\<=]**

Hinweis:Der Aufbau des "KEY_VERIFIER" entspricht [gemSpec_IDP_Dienst#Kapitel
7.5Token Request].

**A_20671-01 - Einreichen des AUTHORIZATION_CODE beim Token-Endpunkt**

Das Primärsystem MUSS den "Key_Verifier" mittels JWE und PUK_IDP_ENC
verschlüsseln und zusammen mit dem "AUTHORIZATION_CODE“ TLS-gesichert und
als HTTP/1.1 POST Request an den Token-Endpunkt senden. **[\<=]**

Hinweis: Der Aufbau der Anfrage entspricht [gemSpec_IDP_Dienst#Kapitel 7.5Token
Request].

Als Verschlüsselungsalgorithmus ist ECDH-ES (Elliptic Curve Diffie-Hellman
Ephemeral Static key agreement) vorgesehen.

Der Token-Endpunkt validiert den "CODE_VERFIER" und gleicht diesen mit der
"code_challenge" ab. Dann erzeugt er die erforderlichen Token und
verschlüsselt beide mit dem "Token-Key".

Das Primärsystem erhält nun den signierten"ID_TOKEN"und den "ACCESS_TOKEN" vom
Token-Endpunkt und prüft die Signatur des "ID_TOKEN".

**A_20672-01 - Annahme des ID_TOKEN**

Das Primärsystem MUSS das vom Token-Endpunkt ausgegebene "ID_TOKEN" als
HTTP/1.1 Statusmeldung 200 verarbeiten und mittels "Token-Key" entschlüsseln.
Das Primärsystem MUSS das "ID_TOKEN" ablehnen, wenn dieses außerhalb der mit
dem Token-Endpunkt etablierten TLS-Verbindung übertragen wird oder nicht mit
dem vorher übermittelten "Token-Key" verschlüsselt war. **[\<=]**

Hinweis: Der Aufbau der Antwort und des "ID_TOKEN" entspricht
[gemSpec_IDP_Dienst#Kapitel 7.6 Token Response].

**A_20673-01 - Annahme des "ACCESS_TOKEN"**

Das Primärsystem MUSS das vom Token-Endpunkt ausgegebene "ACCESS_TOKEN" in der
HTTP/1.1 Statusmeldung 200 verarbeiten und mittels "Token-Key" entschlüsseln.
Das Primärsystem MUSS das "ACCESS_TOKEN" ablehnen, wenn dieses außerhalb der
mit dem Token-Endpunkt etablierten TLS-Verbindung übertragen wird oder nicht
mit dem vorher übermittelten "Token-Key" verschlüsselt war. **[\<=]**

Hinweis:Der Aufbau der Antwort und des "ACCESS_TOKEN" entspricht
[gemSpec_IDP_Dienst#Kapitel 7.6 Token Response].

**A_20674 - Formale Prüfung der Signatur des ID_TOKEN**

Das Primärsystem MUSS die Signatur des ID_TOKEN mathematisch prüfen und auf
ein zeitlich gültiges C.FD.SIG-Zertifikat mit der Rollen-OID "oid_idpd"
zurückführen können. **[\<=]**

Zur Prüfung von Zertifikatstyp- und Rollen-OID siehe Hinweis zu A_20657.

**A_20675 - Gültigkeitsprüfung der Signatur des ID_TOKEN innerhalb der TI**

Das Primärsystem MUSS das zur Signatur des ID_TOKEN verwendete Zertifikat über
die Funktion „VerifyCertificate“ des Konnektors gemäß
[gemSpec_Kon#4.1.9.5.3] bzw. [gemILF_PS#4.4.4.3] auf Gültigkeit innerhalb der
TI prüfen. **[\<=]**

Im weiteren Verlauf kann der "ACCESS_TOKEN" innerhalb seiner Gültigkeitsdauer
bei verschiedenen Aufrufen des Fachdienstes eingereicht werden. Der Fachdienst
entschlüsselt das "ACCESS_TOKEN" mit seinem privaten Schlüssel, validiert es,
zieht die notwendigen Informationen entsprechend seinem Claim heraus und
verwendet diese für seine fachlichen Operationen.

### 5.2 Anwendungsfälle verordnende LEI

Folgende Anwendungsfälle werden im Primärsystem einer verordnenden LEI
umgesetzt.

### 5.2.1 E-Rezept erstellen

Mit diesem Anwendungsfall werden die Aufbewahrungspflichten der verordnenden LEI
unterstützt. Das PS der verordnenden LEI fragt für das Erstellen eines
E-Rezepts beim E-Rezept-Fachdienst eine über 11 Jahre eindeutige Rezept-ID ab,
die für das E-Rezept verwendet wird. 

**A_19274 - PS verordnende LEI: E-Rezept durch Verordnenden erstellen**

Das PS der verordnenden LEI MUSS den Anwendungsfall "UC 2.1 - E-Rezepte
erzeugen" aus [gemSysL_eRp] gemäß TAB_ILFERP_002 umsetzen. 

Tabelle4: TAB_ILFERP_002 – E-Rezept durch Verordnenden erstellen

<table><tr><td>
Name

</td><td>
E-Rezept durch Verordnenden erstellen

</td></tr><tr><td>
Auslöser

</td><td>
 ---> UL

</td></tr><tr><td>
Akteur

</td><td>
Leistungserbringer, Mitarbeiter verordnende LEI

</td></tr><tr><td>
Vorbedingung

</td><td>
 ---> UL

</td></tr><tr><td>
Nachbedingung

</td><td>
 ---> UL

</td></tr><tr><td>
Standardablauf

</td><td>
 ---> OL

</td></tr></table>

**[\<=]**

**A_19276 - PS verordnende LEI: E-Rezept einstellen - E-Rezept-ID abrufen**

Das PS der verordnenden LEI MUSS im Anwendungsfall "E-Rezept durch
Verordnenden erstellen" für das E-Rezept die HTTP-OperationPOST
/Task/$createmit

 ---> UL

ausführen. **[\<=]**

Für weitere Informationen siehe Operation "E-Rezept erstellen" aus der
API-Schnittstelle [E-Rezept API Dokumentation].

Der Value-Katalog fürFlowTypeist in [gemSpec_DM_eRp] beschrieben.

Der Response des Fachdienstes liefert

 ---> UL

**A_19275 - PS verordnende LEI: E-Rezept einstellen - E-Rezept-Bundle erstellen**

Das PS der verordnenden LEI MUSS im Anwendungsfall "E-Rezept durch
Verordnenden erstellen" eine Bundle-FHIR-Ressource gemäß
Profilierung https://fhir.kbv.de/StructureDefinition/KBV_PR_ERP_Bundle 

 ---> UL

erstellen. **[\<=]**

Dieses Bundle wird in diesem Dokument als E-Rezept-Bundle bezeichnet. Ein
E-Rezept-Bundle enthält genau eine Verordnungszeile.

**A_19559 - PS verordnende LEI: E-Rezept einstellen - E-Rezept-Bundle
kanonisieren**

Das PS der verordnenden LEI MUSS im Anwendungsfall "E-Rezept durch
Verordnenden erstellen" das E-Rezept-Bundle vor dem Signieren kanonisieren und
dazu die
Kanonisierungsregelnhttps://www.w3.org/TR/2008/REC-xml-c14n11-20080502/für
Canonical XML Version 1.1 für XML-Dokumente anwenden. **[\<=]**

Für die qualifizierte elektronische Signatur des E-Rezept Bundels wird der
Konnektor verwendet. Es wird eine CMS-Signatur (CAdES) erstellt. Die Operation
für die QES muss durch den Leistungserbringer durchgeführt werden.

**A_19281-01 - PS verordnende LEI: E-Rezept einstellen - E-Rezept-Bundle QES
signieren**

Das PS der verordnenden LEI MUSS im Anwendungsfall "E-Rezept durch
Verordnenden erstellen" für das E-Rezept die Signaturoperation des Konnektors
mit

 ---> UL

ausführen. **[\<=]**

Für weitere Informationen siehe Operation "E-Rezept qualifiziert signieren" aus
der API-Schnittstelle [E-Rezept API Dokumentation].

Für die Nutzung der Komfortsignatur siehe [gemILF_PS].

**A_21243 - PS verordnende LEI: E-Rezept-einstellen - Unterstützung
Signaturverfahren**

Das PS der verordnenden LEI MUSS muss die Erstellung der E-Rezepte mittels
Einzelsignatur, Stapelsignatur und Komfortsignatur unterstützen. **[\<=]**

Falls keine Komfortsignatur zur Verfügung steht oder die Komfortsignatur
deaktiviert ist, soll das PS der verordnenden LEI die Stapelsignatur verwenden
ist, falls mehrere E-Rezepte signiert werden sollen. 

### 5.2.2 E-Rezept einstellen

Mit diesem Anwendungsfall wird das von der verordnenden LEI erstellte E-Rezept
auf dem Fachdienst eingestellt, damit es für den Versicherten verfügbar ist.

Das erstellte E-Rezept-Bundle wird innerhalb einer PKCS#7-Datei (enveloping)
für die QES an den Task in der $activate-Operation übergeben.

**A_19272 - PS verordnende LEI: E-Rezept durch Verordnenden einstellen**

Das PS der verordnenden LEI MUSS den Anwendungsfall "UC 2.3 - E-Rezept
einstellen" aus [gemSysL_eRp] gemäß TAB_ILFERP_003 umsetzen. 

Tabelle5: TAB_ILFERP_003 – E-Rezept durch Verordnenden einstellen

<table><tr><td>
Name

</td><td>
E-Rezept durch Verordnenden einstellen

</td></tr><tr><td>
Auslöser

</td><td>
 ---> UL

</td></tr><tr><td>
Akteur

</td><td>
Leistungserbringer, Mitarbeiter verordnende LEI

</td></tr><tr><td>
Vorbedingung

</td><td>
 ---> UL

</td></tr><tr><td>
Nachbedingung

</td><td>
 ---> UL

</td></tr><tr><td>
Standardablauf

</td><td>
 ---> OL

</td></tr></table>

**[\<=]**

**A_19273-01 - PS verordnende LEI: E-Rezept einstellen - Task auf Fachdienst
aktivieren**

Das PS der verordnenden LEI MUSS im Anwendungsfall "E-Rezept durch
Verordnenden einstellen" für das E-Rezept die HTTP-OperationPOST
/Task/\<id\>/$activatemit

 ---> UL

ausführen. **[\<=]**

Für weitere Informationen siehe Operation "E-Rezept vervollständigen und Task
aktivieren" aus der API-Schnittstelle [E-Rezept API Dokumentation].

Es gelten vorrangig die Regelungen zum Ausdruck eines E-Rezepts aus den
Bundesmantelverträgen [BMV] und [BMV-Z].

**A_19279 - PS verordnende LEI: E-Rezept einstellen - E-Rezept-Token erstellen**

Das PS der verordnenden LEI MUSS im Anwendungsfall "E-Rezept durch
Verordnenden einstellen" einen E-Rezept-Token erstellen,wenn ein Ausdruck der
Einlöseinformationen des E-Rezepts erstellt werden soll. **[\<=]**

Für die Spezifikation des E-Rezept-Token siehe[gemSpec_DM_eRp#2.3].

**A_19280 - PS verordnende LEI: E-Rezept einstellen - E-Rezept ausdrucken**

Das PS der verordnenden LEI MUSS im Anwendungsfall "E-Rezept durch
Verordnenden einstellen", wenn ein Ausdruck des E-Rezepts erstellt werden
soll, den Datamatrix-Code für den E-Rezept-Token erstellen und diesen zusammen
mit Zusatzinformationen ausdrucken. **[\<=]**

Für die Spezifikation des Datamatrix-Code für E-Rezept-Token
siehe[gemSpec_DM_eRp#2.3]. 

Für Regelungen zum Inhalt des Ausdrucks siehe auch Bundesmantelverträge [BMV]
und [BMV-Z]

### 5.2.3 E-Rezept löschen

Mit diesem Anwendungsfall kann die verordnende LEI ein E-Rezept löschen,
welches sie zuvor auf den E-Rezept-Fachdienst eingestellt hat.

**A_19236 - PS verordnende LEI: E-Rezepte löschen - E-Rezept zum Löschen
auswählen**

Das PS der verordnenden LEI MUSS es dem Nutzer ermöglichen, ein E-Rezept zum
Löschen auf dem Fachdienst auszuwählen. **[\<=]**

**A_19237 - PS verordnende LEI: E-Rezept löschen - Bestätigung**

Das PS der verordnenden LEI MUSS vom Nutzer eine Bestätigung einholen, dass das
ausgewählte E-Rezept gelöscht werden soll und die Möglichkeit geben, das
Löschen abzubrechen. **[\<=]**

**A_19238 - PS verordnende LEI: E-Rezept durch Verordnenden löschen**

Das PS der verordnenden LEI MUSS den Anwendungsfall "UC 2.5 - E-Rezept durch
Verordnenden löschen" aus [gemSysL_eRp] gemäß TAB_ILFERP_004 umsetzen. 

Tabelle6: TAB_ILFERP_004 – E-Rezept durch Verordnenden löschen

<table><tr><td>
Name

</td><td>
E-Rezept durch Verordnenden löschen

</td></tr><tr><td>
Auslöser

</td><td>
 ---> UL

</td></tr><tr><td>
Akteur

</td><td>
Leistungserbringer, Mitarbeiter verordnende LEI

</td></tr><tr><td>
Vorbedingung

</td><td>
 ---> UL

</td></tr><tr><td>
Nachbedingung

</td><td>
 ---> UL

</td></tr><tr><td>
Standardablauf

</td><td>
 ---> OL

</td></tr></table>

**[\<=]**

**A_19239-01 - PS verordnende LEI: E-Rezept löschen - Löschrequest**

Das PS der verordnenden LEI MUSS im Anwendungsfall "E-Rezept durch
Verordnenden löschen" für das zu löschende E-Rezept die HTTP-OperationPOST
/TASK/\<id\>/$abortmit

 ---> UL

ausführen. **[\<=]**

Für weitere Informationen siehe Operation "Ein E-Rezept löschen" aus der
API-Schnittstelle [E-Rezept API Dokumentation].

**A_19240 - PS verordnende LEI: E-Rezept löschen - E-Rezept-Token löschen**

Das PS der verordnenden LEI MUSS im Anwendungsfall "E-Rezept durch Verordnenden
löschen" für das zu löschende E-Rezept nach erfolgreichem Aufruf der
Operation "Ein E-Rezept löschen" die Task-ID und den AccessCode im PS
löschen. **[\<=]**

### 5.3 Anwendungsfälle abgebende LEI

Folgende Anwendungsfälle werden im Primärsystem einer abgebenden LEI umgesetzt.

### 5.3.1 E-Rezept abrufen

Mit diesem Anwendungsfall kann die abgebende LEI Daten zum E-Rezept inklusive
QES zu einem vom Versicherten empfangenen E-Rezept-Token vom
E-Rezept-Fachdienst abrufen, um das E-Rezept einzulösen.Darüber hinaus wird
durch die Gültigkeit der QES sichergestellt, dass es sich um ein gegenüber
der Krankenkasse abrechenbares gültiges E-Rezept handelt.

**A_19293 - PS abgebende LEI: E-Rezept abrufen - E-Rezept-Token auswählen**

Das PS der abgebenden LEI MUSS es dem Nutzer ermöglichen, ein E-Rezept-Token
auszuwählen, zu dem das E-Rezept vom Fachdienst abgerufen werden soll.
**[\<=]**

**A_19294 - PS abgebende LEI: E-Rezept abrufen**

Das PS der abgebenden LEI MUSS den Anwendungsfall "UC 4.1 - E-Rezept
abrufen" aus [gemSysL_eRp] gemäß TAB_ILFERP_005 umsetzen. 

Tabelle7: TAB_ILFERP_005 – E-Rezept abrufen

<table><tr><td>
Name

</td><td>
E-Rezept abrufen

</td></tr><tr><td>
Auslöser

</td><td>
 ---> UL

</td></tr><tr><td>
Akteur

</td><td>
Leistungserbringer, Mitarbeiter der abgebenden LEI

</td></tr><tr><td>
Vorbedingung

</td><td>
 ---> UL

</td></tr><tr><td>
Nachbedingung

</td><td>
 ---> UL

</td></tr><tr><td>
Standardablauf

</td><td>
 ---> OL

</td></tr></table>

**[\<=]**

**A_19558-01 - PS abgebende LEI: E-Rezept abrufen - Task herunterladen**

Das PS der abgebenden LEI MUSS im Anwendungsfall "E-Rezept abrufen" zum
Herunterladen des E-Rezepts die HTTP-OperationPOST /Task/\<id\>/$acceptmit

 ---> UL

ausführen. **[\<=]**

Für weitere Informationen siehe Operation "E-Rezepte abrufen" aus der
API-Schnittstelle [E-Rezept API Dokumentation].

Der Response liefert eineTaskRessource. Für die Spezifikation derTaskRessource
siehe [gemSpec_DM_eRp]. Jeder Task enthält die folgenden fachlichen
Informationen:

 ---> UL

Für die QES-Prüfung wird die PKCS#7-Datei verwendet. Die Verordnungsdaten des
E-Rezepts sind innerhalb der PKCS#7-Datei enthalten und müssen für die
Weiterverarbeitung extrahiert werden.

**A_19745 - PS abgebende LEI: E-Rezept abrufen - QES prüfen**

Das PS der abgebenden LEI MUSS im Anwendungsfall "E-Rezept abrufen" zum Prüfen
der QES des E-Rezepts die OperationPOST //Konnektorservicemit

 ---> UL

ausführen. **[\<=]**

Für weitere Informationen siehe Operation "Qualifizierte Signatur des E-Rezepts
prüfen" aus der API-Schnittstelle [E-Rezept API Dokumentation].
Implementierungshinweise zur Signaturprüfung für Primärsysteme sind in
[gemILF_PS#4.4.2] beschrieben. Die Außenschnittstelle des Konnektors ist in
[gemSpec_Kon#TIP1-A_5034-x Operation VerifyDocument (nonQES und QES)]
beschrieben. 

Als Response liefert der Konnektor einen standardisierten Prüfbericht in einer
VerificationReport-Struktur gemäß [OASIS-VR].

Für die weitere Verarbeitung wird das E-Rezept-Bundle aus der PKCS#7-Datei
verwendet.

**A_19900 - PS abgebende LEI: E-Rezept abrufen - E-Rezept-Bundle extrahieren**

Das PS der abgebenden LEI MUSS im Anwendungsfall "E-Rezept abrufen" die Daten
zum E-Rezept-Bundle zur Weiterverarbeitung extrahieren. **[\<=]**

**A_19901 - PS abgebende LEI: E-Rezept abrufen - Daten speichern**

Das PS der abgebenden LEI MUSS im Anwendungsfall "E-Rezept abrufen" das
E-Rezept-Bundle und das Secret im PS speichern. **[\<=]**

Möchte der Versicherte die Möglichkeit einer Online-Rezepteinlösung nutzen,
kann die abgebende LEI die Belieferungs- und ggfs. Zuzahlungsmodalitäten über
ihr Warenwirtschaftssystem ("Onlineshop") abwickeln. Hierzu ist ggfs. die
Übernahme von Rezeptinformationen zur Befüllung eines Warenkorbs
erforderlich. 

**A_21372 - PS abgebende LEI: Übernahme Rezeptinformationen in
Warenwirtschaftssystem**

Das PS der abgebenden LEI MUSS bei der Übernahme von E-Rezept-Informationen in
ein Warenwirtschaftssystem die Integrität und Vertraulichkeit  der
personenbezogenen und medizinischen Daten sicherstellen und zusätzlich
sicherstellen, dass der Umfang der übertragenen Daten nur auf das unmittelbare
für die Einlösung erforderliche Maß beschränkt (Datenminimierung) ist und
keine Verwendung der Daten über die unmittelbare Rezepteinlösung hinaus
erfolgt (Zweckbindung). **[\<=]**

### 5.3.2 Quittung abrufen

Mit diesem Anwendungsfall kennzeichnet das PS der abgebenden LEI das E-Rezept
nach der Belieferung im E-Rezept-Fachdienst als abgegeben und lädt die
Quittung herunter, die für die weiteren Abrechnungsprozesse genutzt
wird.Darüber hinaus werden dem E-Rezept-Fachdienst Informationen über das
abgegebene Medikament bereitgestellt, die dann vom Versicherten auf seinem FdV
heruntergeladen werden können. 

**A_19286 - PS abgebende LEI: Quittung abrufen - E-Rezept auswählen**

Das PS der abgebenden LEI MUSS es dem Nutzer ermöglichen, ein E-Rezept als
abgegeben auszuwählen. **[\<=]**

**A_19287-01 - PS abgebende LEI: Quittung abrufen**

Das PS der abgebenden LEI MUSS den Anwendungsfall "UC 4.4 - Quittung
abrufen" aus [gemSysL_eRp] gemäß TAB_ILFERP_006 umsetzen. 

Tabelle8: TAB_ILFERP_006 – Quittung abrufen

<table><tr><td>
Name

</td><td>
Quittung abrufen

</td></tr><tr><td>
Auslöser

</td><td>
 ---> UL

</td></tr><tr><td>
Akteur

</td><td>
Leistungserbringer, Mitarbeiter der abgebenden LEI

</td></tr><tr><td>
Vorbedingung

</td><td>
 ---> UL

</td></tr><tr><td>
Nachbedingung

</td><td>
 ---> UL

</td></tr><tr><td>
Standardablauf

</td><td>
 ---> OL

</td></tr></table>

**[\<=]**

**A_19288 - PS abgebende LEI: Quittung - MedicationDispense erstellen**

Das PS der abgebenden LEI MUSS im Anwendungsfall "Quittung abrufen" eine
FHIR-RessourceMedicationDispensemit den Informationen über das abgegebene
Medikament erstellen. **[\<=]**

Für die Spezifikation der RessourceMedicationDispensesiehe [gemSpec_DM_eRp].
Die Befüllung des Medication-Objekts der MedicationDispense kann in
Abhängigkeit eines Austauschs aus der Übernahme der wesentlichen Attribute
(PZN, Wirkstoff, Darreichungsform, Dosierinformationen) aus dem
Verordnungsdatensatz und den Daten aus dem Securpharm-Scan in die
MedicationDispense und Medication kopiert werden. Weitere Informationen, die
sich aus dem Scan des Securpharm-Codes für Fertigarzneimittel ergeben (z.B.
Charge, Haltbarkeitsdatum) und im Primärsystem vorliegen, können ebenfalls
übernommen werden.

**A_21105 - PS abgebende LEI: Chargeninfo in Medication ergänzen**

Das PS der abgebenden LEI MUSS im Anwendungsfall "Quittung abrufen" die
FHIR-Ressource "Medication" der erstellten MedicationDispense um
Chargeninformation und Verfallsdatum aus dem SecurPharm-Scan [SecurPharm]
ergänzen, sofern es sich bei dem abgegebenen Arzneimittel um ein
Fertigarzneimittel handelt, das einen Data-Matrix-Code gemäß
securPharm-System besitzt.  **[\<=]**

**A_19289 - PS abgebende LEI: Quittung abrufen - Statusrequest**

Das PS der abgebenden LEI MUSS im Anwendungsfall "Quittung abrufen" für das
abgegebene E-Rezept die HTTP-OperationPOST /Task/\<id\>/$closemit

 ---> UL

ausführen. **[\<=]**

Für weitere Informationen siehe Operation "E-Rezept-Abgabe vollziehen" aus der
API-Schnittstelle [E-Rezept API Dokumentation].

Der Response enthält ein signiertes Quittungs-Bundle, welches im
Abrechnungsprozess genutzt wird.

Der E-Rezept-Fachdienst prüft regelmäßig den Status seines
Signaturzertifikats, die mandatorische Signaturprüfung der Quittung obliegt
dem Quittungsempfänger, kann aber vom AVS vor der Weitergabe in die
Abrechnungsprozesse ebenfalls geprüft werden.

Die Quittung wird als PKCS#7-Datei erstellt. Die quittierten Daten sind
innerhalb der PKCS#7-Datei enthalten.

**A_20766 - PS abgebende LEI: Quittung - Quittungssignatur prüfen**

Das PS der abgebenden LEI KANN im Anwendungsfall "Quittung abrufen" zum Prüfen
der Quittung des E-Rezepts die OperationPOST //Konnektorservicemit

 ---> UL

ausführen. **[\<=]**

Implementierungshinweise zur Signaturprüfung für Primärsysteme sind in
[gemILF_PS#4.4.2] beschrieben. Die Außenschnittstelle des Konnektors ist in
[gemSpec_Kon#TIP1-A_5034-x Operation VerifyDocument (nonQES und QES)]
beschrieben. 

Als Response liefert der Konnektor einen standardisierten Prüfbericht in einer
VerificationReport-Struktur gemäß [OASIS-VR].

Hinweis: Mit den Konnektor-Versionen PTV4, PTV4+ und PTV5 kann die Signatur der
Quittung nicht geprüft werden, da die Signaturprüfung immer eine negatives
Ergebnis liefert. Grund ist, dass für das Zertifikatsprofil des durch den
E-Rezept-Fachdienstes verwendeten Signaturzertifikates die Signaturprüfung
noch nicht spezifiziert und implementiert ist. Wenn eine Apotheke die Signatur
der Quittung prüfen möchte, dann muss dies unabhängig vom Konnektor im AVS
umgesetzt werden. Die Zertifikatsprüfung im Rahmen der Signaturprüfung kann
mittels der Konnektorfunktion VerifyCertificate erfolgen. 

### 5.3.3 Quittung erneut abrufen

Mit diesem Anwendungsfall kann die abgebende LEI die Quittung erneut abrufen,
falls bei der Übermittlung vom E-Rezept-Fachdienst ein Fehler aufgetreten ist.

Der Anwendungsfall kann bei Bedarf wiederholt werden.

**A_19290 - PS abgebende LEI: Quittung erneut abrufen - E-Rezept auswählen**

Das PS der abgebenden LEI MUSS es dem Nutzer ermöglichen, ein E-Rezept
auszuwählen, zu dem die Quittung erneut abgerufen werden soll. **[\<=]**

**A_19291 - PS abgebende LEI: Quittung erneut abrufen**

Das PS der abgebenden LEI MUSS den Anwendungsfall "UC 4.8 - Quittung erneut
abrufen" aus [gemSysL_eRp] gemäß TAB_ILFERP_007 umsetzen. 

Tabelle9: TAB_ILFERP_007 – Quittung erneut abrufen

<table><tr><td>
Name

</td><td>
Quittung erneut abrufen

</td></tr><tr><td>
Auslöser

</td><td>
 ---> UL

</td></tr><tr><td>
Akteur

</td><td>
Leistungserbringer, Mitarbeiter der abgebenden LEI

</td></tr><tr><td>
Vorbedingung

</td><td>
 ---> UL

</td></tr><tr><td>
Nachbedingung

</td><td>
 ---> UL

</td></tr><tr><td>
Standardablauf

</td><td>
 ---> OL

</td></tr></table>

**[\<=]**

**A_19292 - PS abgebende LEI: Quittung erneut abrufen - Statusrequest**

Das PS der abgebenden LEI MUSS im Anwendungsfall "Quittung erneut abrufen" für
das E-Rezept die HTTP-OperationGET /Task/\<id\>mit

 ---> UL

ausführen. **[\<=]**

Für weitere Informationen siehe Operation "Quittung erneut abrufen" aus der
API-Schnittstelle [E-Rezept API Dokumentation].

Der Response enthält ein signiertes Quittungs-Bundle, welches im
Abrechnungsprozess genutzt wird.

### 5.3.4 E-Rezept zurückgeben

Mit diesem Anwendungsfall kann die abgebende LEI ein E-Rezept, welches vom
E-Rezept-Fachdienst abgerufen wurde, wieder zurückgeben, z.B. weil das
E-Rezept nicht beliefert werden kann oder weil der Versicherte darum gebeten
hat. Nachfolgend kann es durch den Versicherten einer anderen abgebenden LEI
zugewiesen werden.

**A_19246 - PS abgebende LEI: E-Rezepte zurückgeben - E-Rezept auswählen**

Das PS der abgebenden LEI MUSS es dem Nutzer ermöglichen, ein E-Rezept zum
Zurückgeben auszuwählen. **[\<=]**

**A_19247 - PS abgebende LEI: E-Rezept zurückgeben - Bestätigung**

Das PS der abgebenden LEI MUSS vom Nutzer eine Bestätigung einholen, dass das
ausgewählte E-Rezept zurückgegeben werden soll und die Möglichkeit geben,
das Zurückgeben abzubrechen. **[\<=]**

**A_19249 - PS abgebende LEI: E-Rezept durch Abgebenden zurückgeben**

Das PS der abgebenden LEI MUSS den Anwendungsfall "UC 4.2 - E-Rezept durch
Abgebenden zurückgeben" aus [gemSysL_eRp] gemäß TAB_ILFERP_008 umsetzen. 

Tabelle10: TAB_ILFERP_008 – E-Rezept durch Abgebenden zurückgeben

<table><tr><td>
Name

</td><td>
E-Rezept durch Abgebenden zurückgeben

</td></tr><tr><td>
Auslöser

</td><td>
 ---> UL

</td></tr><tr><td>
Akteur

</td><td>
Leistungserbringer, Mitarbeiter der abgebenden LEI

</td></tr><tr><td>
Vorbedingung

</td><td>
 ---> UL

</td></tr><tr><td>
Nachbedingung

</td><td>
 ---> UL

</td></tr><tr><td>
Standardablauf

</td><td>
 ---> OL

</td></tr></table>

**[\<=]**

**A_19250 - PS abgebende LEI: E-Rezept zurückgeben - Statusrequest**

Das PS der abgebenden LEI MUSS im Anwendungsfall "E-Rezept durch Abgebenden
zurückgeben" für das zurückzugebende E-Rezept die HTTP-OperationPOST
/Task/\<id\>/$rejectmit

 ---> UL

ausführen. **[\<=]**

Für weitere Informationen siehe Operation "Ein E-Rezept zurückweisen" aus der
API-Schnittstelle [E-Rezept API Dokumentation].

**A_19251 - PS abgebende LEI: E-Rezept zurückgeben - E-Rezept löschen**

Das PS der abgebenden LEI MUSS im Anwendungsfall "E-Rezept durch Abgebenden
zurückgeben" für das zurückzugebende E-Rezept nach erfolgreichem Aufruf der
Operation "Ein E-Rezept zurückweisen" die Daten zum E-Rezept, E-Rezept-Token
und das Geheimnis im PS löschen. **[\<=]**

### 5.3.5 E-Rezept löschen

Mit diesem Anwendungsfall kann die abgebende LEI ein E-Rezept, welches auf dem
E-Rezept-Fachdienst gespeichert ist, löschen, z.B. wenn ein Fehler an der
Verordnung gefunden wurde, der sich nur durch das Ausstellen eines neuen
E-Rezepts durch die verordnende LEI beheben lässt.

**A_19241 - PS abgebende LEI: E-Rezepte löschen - E-Rezept auswählen**

Das PS der abgebenden LEI MUSS es dem Nutzer ermöglichen, ein E-Rezept zum
Löschen auf dem Fachdienst auszuwählen. **[\<=]**

**A_19242 - PS abgebende LEI: E-Rezept löschen - Bestätigung**

Das PS der abgebenden LEI MUSS vom Nutzer eine Bestätigung einholen, dass das
ausgewählte E-Rezept gelöscht werden soll, und die Möglichkeit geben, das
Löschen abzubrechen. **[\<=]**

**A_19243 - PS abgebende LEI: E-Rezept durch Abgebenden löschen**

Das PS der abgebenden LEI MUSS den Anwendungsfall "UC 4.3 - E-Rezept durch
Abgebenden löschen" aus [gemSysL_eRp] gemäß TAB_ILFERP_009 umsetzen. 

Tabelle11: TAB_ILFERP_009 – E-Rezept durch Abgebenden löschen

<table><tr><td>
Name

</td><td>
E-Rezept durch Abgebenden löschen

</td></tr><tr><td>
Auslöser

</td><td>
 ---> UL

</td></tr><tr><td>
Akteur

</td><td>
Leistungserbringer, Mitarbeiter der abgebenden LEI

</td></tr><tr><td>
Vorbedingung

</td><td>
 ---> UL

</td></tr><tr><td>
Nachbedingung

</td><td>
 ---> UL

</td></tr><tr><td>
Standardablauf

</td><td>
 ---> OL

</td></tr></table>

**[\<=]**

**A_19244 - PS abgebende LEI: E-Rezept löschen - Löschrequest**

Das PS der abgebenden LEI MUSS im Anwendungsfall "E-Rezept durch Abgebenden
löschen" für das zu löschende E-Rezept die HTTP-OperationPOST
/Task/\<id\>/$abortmit

 ---> UL

ausführen. **[\<=]**

Für weitere Informationen siehe Operation "Ein E-Rezept löschen" aus der
API-Schnittstelle [E-Rezept API Dokumentation].

**A_19245 - PS abgebende LEI: E-Rezept löschen - E-Rezept-Token löschen**

Das PS der abgebenden LEI MUSS im Anwendungsfall "E-Rezept durch Abgebenden
löschen" für das zu löschende E-Rezept nach erfolgreichem Aufruf der
Operation "Ein E-Rezept löschen" die Daten zum E-Rezept-Token und das
Geheimnis im PS löschen. **[\<=]**

### 5.3.6 Nachrichten von Versicherten empfangen

Mit diesem Anwendungsfall kann die abgebende LEI den Token eines E-Rezepts
empfangen, um es zu beliefern. Darüber hinaus kann es Nachrichten des
Versicherten, wie z.B. Anfragen zur Belieferung durch eine Apotheke,
empfangen.  

**A_21556 - PS abgebende LEI: Häufigkeit des Abrufen von Nachrichten**

Das PS der abgebenden LEI MUSS im Anwendungsfall "Nachrichten von Versicherten
empfangen" zwischen den Aufrufen der Operation GET /Communication mindestens 5
Minuten warten. Der Zeitraum zwischen den Aufrufen muss um eine zufällige
Zeitspanne zwischen 0 und 10.000 Millisekunden verlängert werden, um eine
Gleichverteilung der Anfragen am E-Rezept-Fachdienst über alle Apotheken zu
erreichen. **[\<=]**

**A_19328 - PS abgebende LEI: Nachrichten von Versicherten empfangen**

Das PS der abgebenden LEI MUSS den Anwendungsfall "UC 4.6 - Nachrichten durch
Abgebenden empfangen" aus [gemSysL_eRp] gemäß TAB_ILFERP_010 umsetzen. 

Tabelle12: TAB_ILFERP_010 – Nachrichten von Versicherten empfangen

<table><tr><td>
Name

</td><td>
Nachrichten von Versicherten empfangen

</td></tr><tr><td>
Auslöser

</td><td>
 ---> UL

</td></tr><tr><td>
Akteur

</td><td>
Leistungserbringer, Mitarbeiter der abgebenden LEI

</td></tr><tr><td>
Vorbedingung

</td><td>
 ---> UL

</td></tr><tr><td>
Nachbedingung

</td><td>
 ---> UL

</td></tr><tr><td>
Standardablauf

</td><td>
 ---> OL

</td></tr></table>

**[\<=]**

**A_19329-01 - PS abgebende LEI: Nachrichten empfangen - Abfragerequest**

Das PS der abgebenden LEI MUSS im Anwendungsfall "Nachrichten von Versicherten
empfangen" die HTTP-OperationGET /Communication mit

 ---> UL

ausführen. **[\<=]**

Für weitere Informationen siehe Operationen "Anwendungsfall auf neue
Nachrichten prüfen" und  "Anwendungsfall Alle Nachrichten vom
E-Rezept-Fachdienst abrufen" aus der API-Schnittstelle [E-Rezept API
Dokumentation].

Falls eine oder mehrere E-Rezept-Nachrichten für die abgebende LEI auf dem
Fachdienst bereitstehen, übermittelt der Fachdienst ein Bundle
vonCommunicationRessourcen. 

EineCommunicationRessource kann unterschiedlichen Typs sein und beinhaltet
typabhängige, fachliche Informationen:

 ---> UL

Wenn die Nachricht einen E-Rezept-Token enthält, dann hat der Versicherte das
E-Rezept der Apotheke zugewiesen. Mit den Informationen aus dem E-Rezept-Token
kann das E-Rezept vom Fachdienst abgerufen (Anwendungsfall "E-Rezept abrufen")
und beliefert werden.

Wenn die Nachricht Informationen zum verordneten Mittel und keinen
E-Rezept-Token enthält, dann kann die Information entsprechend der Mitteilung
des Versicherten (bspw. Anfrage zur Belieferung durch eine Apotheke)
verarbeitet werden. 

Die unverbindliche Anfrage zur Belieferung wird mit dem Start des E-Rezepts am
01.07.2021 noch nicht unterstützt.

Der verbindliche Einlöseauftrag wird mit dem Start des E-Rezepts am 01.07.2021
die optionale Mitteilung/Text als Freitext für den Versicherten nicht
unterstützt. Anstelle des im Freitext zu definierenden Belieferungswunsches
werden Informationen zum Belieferungswunsch in der folgenden JSON Struktur in
Communication.payload übermittelt.

Fürpayloadwird folgende strukturierte Übermittlung vorgesehen

{ 

"version": "1", 

"supplyOptionsType": "delivery", 

"name": "Dr. Maximilian von Muster", 

"address": [    "wohnhaft bei Emilia Fischer",    "Bundesallee 312",   
"123. OG",    "12345 Berlin"  ], 

"hint": "Bitte im Morsecode klingeln: -.-.", 

"phone": "004916094858168"

}

<table><tr><th>
Attribut

</th><th>
mandatory/optional

</th><th>
Bedeutung

</th></tr><tr><td>
version

</td><td>
mandatory

</td><td>
immer 1

</td></tr><tr><td>
supplyOptionsType

</td><td>
mandatory

</td><td>
Valide Inhalte: "onPremise", "delivery", "shipment"

</td></tr><tr><td>
name

</td><td>
mandatory

</td><td>
"onPremise": Name des Versicherten laut Rezept

"delivery"/"shipment": Name des Lieferungsempfänger

</td></tr><tr><td>
address

</td><td>
mandatory

</td><td>
"onPremise": Adresse des Versicherten laut Rezept

"delivery"/"shipment": Adresse des Lieferungsempfänger

mindestens: Strasse+Hausnummer, PLZ+Ort werden gesetzt

</td></tr><tr><td>
hint

</td><td>
optional

</td><td>
nur bei "delivery":

Hinweise zur Belieferung

Freitext, max. 90 Zeichen 

</td></tr><tr><td>
phone

</td><td>
optional

</td><td>
immer bei "delivery",

internationales Format

</td></tr></table>

Hinweis zur Bedeutung der Abhol-/Lieferoptionen:

 ---> UL

### 5.3.7 Nachricht an Versicherten versenden

Mit diesem Anwendungsfall kann die abgebende LEI auf Nachrichten eines
Versicherten antworten, z.B. um mitzuteilen, ob das E-Rezept durch die Apotheke
beliefert werden kann oder wann die Arzneimittel zur Abholung bereitstehen.

**A_19330 - PS abgebende LEI: Nachricht versenden - E-Rezept auswählen**

Das PS der abgebenden LEI MUSS es dem Nutzer ermöglichen, eine
E-Rezept-Nachricht auszuwählen, um eine Antwort zu senden. **[\<=]**

**A_19331 - PS abgebende LEI: Nachricht versenden - Mitteilung erfassen**

Das PS der abgebenden LEI MUSS es dem Nutzer ermöglichen, für eine
E-Rezept-Nachricht an einen Versicherten eine Textnachricht zu erfassen.
**[\<=]**

Wickelt die abgebende LEI ein E-Rezept über einen Onlineshop ab, kann dem
Versicherten das Weiterbearbeiten seines Warenkorbs in einer externen
Bestellplattform (z.B. Versandadresse, Zuzahlung) ermöglicht werden. Hierzu
erlaubt der E-Rezept-Fachdienst den Versand einer Warenkorb-URL in der
Nachricht an den Versicherten.

**A_21373 - PS abgebende LEI: Nachricht versenden - Externe URL ausschließlich
für Einlösung**

Das PS der abgebenden LEI MUSS sicherstellen, dass die Einbettung einer externen
URL ausschließlich für das Einlösen von E-Rezepten in einer externen
Bestellplattform genutzt wird. **[\<=]**

Für die Nutzerführung im E-Rezept-FdV ist es wichtig zu erkennen, ob es sich
um eine automatisierte Antwort oder bspw. die Bitte um Rückruf handelt.
Hierfür kann optional das Feld Communication.topic verwendet werden. Es
kommen die Werte des
Standard-Codesystems https://www.hl7.org/fhir/codesystem-communication-topic.html zur
Anwendung.

**A_19332 - PS abgebende LEI: Nachricht an Versicherten versenden**

Das PS der abgebenden LEI MUSS den Anwendungsfall "UC 4.7 - Nachricht durch
Abgebenden übermitteln" aus [gemSysL_eRp] gemäß TAB_ILFERP_011 umsetzen. 

Tabelle14: TAB_ILFERP_011 – Nachricht an Versicherten versenden

<table><tr><td>
Name

</td><td>
Nachricht an Versicherten versenden

</td></tr><tr><td>
Auslöser

</td><td>
 ---> UL

</td></tr><tr><td>
Akteur

</td><td>
Leistungserbringer, Mitarbeiter der abgebenden LEI

</td></tr><tr><td>
Vorbedingung

</td><td>
 ---> UL

</td></tr><tr><td>
Nachbedingung

</td><td>
 ---> UL

</td></tr><tr><td>
Standardablauf

</td><td>
 ---> OL

</td></tr></table>

**[\<=]**

Als ID des Empfängers wird die Versicherten-ID des Absenders aus der
empfangenen E-Rezept-Nachricht verwendet.

**A_19333-01 - PS abgebende LEI: Nachricht versenden - Communication Ressource
erstellen**

Das PS der abgebenden LEI MUSS im Anwendungsfall "Nachricht an Versicherten
versenden" eineCommunicationRessource mit

 ---> UL

erstellen. **[\<=]**

Für die Spezifikation der Communication Ressource siehe [gemSpec_DM_eRp].

Die unverbindliche Anfrage zur Belieferung wird mit dem Start des E-Rezepts am
01.07.2021 noch nicht unterstützt. Aus dem Grund wird die Attribute
verfügbare Belieferungsoptionen, Verfügbarkeitsstatus und Communication.topic
nicht durch das E-Rezept-FdV ausgewertet.

Fürpayloadwird folgende strukturierte Übermittlung vorgesehen

{

"version": "1",

"supplyOptionsType": "onPremise",

"info_text": "Wir möchten Sie informieren, dass Ihre bestellten Medikamente zur
Abholung bereitstehen. Den Abholcode finden Sie anbei.",

"pickUpCodeHR": "12341234",

"pickUpCodeDMC": "",

"url": ""

}

Es können folgende Fälle abgewickelt werden:

 ---> UL

<table><tr><th>
Attribut

</th><th>
mandatory/optional

</th><th>
Bedeutung

</th></tr><tr><td>
version

</td><td>
mandatory

</td><td>
immer 1

</td></tr><tr><td>
supplyOptionsType

</td><td>
mandatory

</td><td>
Der supplyOptionsType, der bei der Zuweisung durch den Versicherten übergeben
wurde, wird hier wiederholt.  
Valide Inhalte: "onPremise", "delivery",
"shipment".

</td></tr><tr><td>
info_text

</td><td>
optional

</td><td>
Freitext, maximal 400 Zeichen

</td></tr><tr><td>
url

</td><td>
optional

</td><td>
 Wenn gesetzt, wird dem Versicherten ein Button angezeigt, der einen Absprung
auf die hinterlegte URL in den Browser des Betriebssystems auslöst.

</td></tr><tr><td>
pickUpCodeHR

</td><td>
optional

</td><td>
menschenlesbarer Abholcode  
Nur bei supplyOptionsType "onPremise". Wenn
gesetzt, wird dem Nutzer der Inhalt des "pickUpCodeHR" optisch hervorgehoben
angezeigt. Maximale Länge 8 Zeichen.

</td></tr><tr><td>
pickUpCodeDMC

</td><td>
optional

</td><td>
maschinenlesbarer Abholcode (Data-Matrix-Code)  
Nur bei supplyOptionsType
"onPremise". Wenn gesetzt, kann sich der Nutzer den Inhalt als Data-Matrix-Code
anzeigen lassen. Der Inhalt wird gemäß ISO/IEC 16022:2006 in einen DMC
gewandelt. Fehlt die Interpretation, so wird der Code als Freitext angezeigt.

</td></tr></table>

**A_19334 - PS abgebende LEI: Nachricht versenden - Nachricht auf Fachdienst
einstellen**

Das PS der abgebenden LEI MUSS im Anwendungsfall "Nachricht an Versicherten
versenden" die HTTP-Operation POST /Communicationmit

 ---> UL

ausführen. **[\<=]**

Für weitere Informationen siehe Operationen "Anwendungsfall Nachricht als
Apotheke an einen Versicherten schicken" aus der API-Schnittstelle [E-Rezept
API Dokumentation].

### 5.3.8 Nachricht löschen

Mit diesem Anwendungsfall kann die abgebende LEI von ihr versendete Nachrichten
an einen Versicherten auf dem E-Rezept-Fachdienst löschen.

**A_21486 - PS abgebende LEI: Nachricht löschen - Nachricht auswählen**

Das PS der abgebenden LEI MUSS es dem Nutzer ermöglichen, eine Nachricht zum
Löschen auf dem Fachdienst auszuwählen. **[\<=]**

**A_21487 - PS abgebende LEI: Nachricht löschen - Bestätigung**

Das PS der abgebenden LEI MUSS vom Nutzer eine Bestätigung einholen, dass die
ausgewählte Nachricht gelöscht werden soll, und die Möglichkeit geben, das
Löschen abzubrechen. **[\<=]**

**A_21488 - PS abgebende LEI: Nachricht durch Abgebenden löschen**

Das PS der abgebenden LEI MUSS den Anwendungsfall "UC 4.9 - Nachricht durch
Abgebenden löschen" aus [gemSysL_eRp] gemäß TAB_ILFERP_013 umsetzen. 

Tabelle16: TAB_ILFERP_013 – Nachricht durch Abgebenden löschen

<table><tr><td>
Name

</td><td>
Nachricht durch Abgebenden löschen

</td></tr><tr><td>
Auslöser

</td><td>
 ---> UL

</td></tr><tr><td>
Akteur

</td><td>
Leistungserbringer, Mitarbeiter der abgebenden LEI

</td></tr><tr><td>
Vorbedingung

</td><td>
 ---> UL

</td></tr><tr><td>
Nachbedingung

</td><td>
 ---> UL

</td></tr><tr><td>
Standardablauf

</td><td>
 ---> OL

</td></tr></table>

**[\<=]**

**A_21489 - PS abgebende LEI: Nachricht löschen - Löschrequest**

Das PS der abgebenden LEI MUSS im Anwendungsfall "Nachricht durch Abgebenden
löschen" für die zu löschende Nachricht die HTTP-OperationDELETE
/Communication/\<id\>mit

 ---> UL

ausführen. **[\<=]**

Der E-Rezept-Fachdienst prüft anhand der Telematik-ID im ACCESS_TOKEN, ob die
LEI der Absender der zu löschenden Nachricht ist.

Wenn die Nachricht bereits vom Versicherten abgerufen wurde, dann wird im
Response des E-Rezept-Fachdienstes im HTTP-Header eine Warnung mit dem
Zeitpunkt des Abrufes übermittelt.

Für weitere Informationen siehe API-Schnittstelle [E-Rezept API Dokumentation].

**A_21490 - PS abgebende LEI: Nachricht löschen - Nachricht im PS löschen**

Das PS der abgebenden LEI KANN im Anwendungsfall "Nachricht durch Abgebenden
löschen" dem Nutzer ermöglichen, die Nachricht auch lokal im PS zu löschen.
**[\<=]**

Hinweis: Nachrichten an Versicherte sind immer an E-Rezept-Workflows gebunden.
Wenn ein E-Rezept-Workflow, bspw. durch den Versicherten oder aufgrund von
durch den E-Rezept-Fachdienst durchgesetzte Löschfristen, auf dem
E-Rezept-Fachdienst gelöscht wird, dann werden auch alle zugehörigen
Nachrichten gelöscht.

### 5.3.9 Abgabedatensatz signieren

Nach der Belieferung eines E-Rezepts erstellt das PS der abgebenden LEI einen
Abgabedatensatz, welcher zusammen mit dem E-Rezept-Bundle und der Quittung für
die Abrechnung des E-Rezepts verwendet wird.

Die Inhalte und die Struktur des Abgabedatensatzes werden durch DAV und GKV-SV
vorgegeben. Die Definition erfolgt in Form von FHIR-Profilen. Der Datensatz
selbst sollte zur Vereinfachung der Verarbeitung in Folgeprozessen in Analogie
der KBV-Festlegungen im XML-Format (anstelle von bspw. JSON) dargestellt sein. 

Der Abgabedatensatz dient der Abrechnung. Demgegenüber stehen die
Dispensierinformationen der MedicationDispense-Ressource für den Versicherten
(vgl. Abschnitt 5.3.2). 

Für die Signatur des Abgabedatensatzes wird der Konnektor verwendet.

**A_21619 - PS abgebende LEI: Abgabedatensatz signieren**

Das PS der abgebenden LEI MUSS beim Signieren des Abgabedatensatzes die
Signaturoperation des Konnektors mit

 ---> UL

ausführen. **[\<=]**

**A_21244-01 - PS abgebende LEI: Abgabedatensatz signieren - Signaturverfahren**

Das PS der abgebenden LEI MUSS die Signatur des Abgabedatensatzes mittels
Einzelsignatur, Stapelsignatur und Komfortsignatur unterstützen. **[\<=]**

### 5.3.10 2D-Code einscannen

Eine Alternative zur Übermittlung eines E-Rezept-Token vom Versicherten mittels
E-Rezept-Nachricht ist die persönliche Übergabe in der Apotheke vor Ort.
Hierzu übergibt der Kunde (Versicherter oder Vertreter) dem Mitarbeiter der
abgebenden LEI einen Papierausdruck mit 2D-Code oder präsentiert einen 2D-Code
auf dem Display seines mobilen Gerätes. Ebenso besteht die Möglichkeit, dass
ein Versicherter den Papierausdruck eines E-Rezept-Tokens an eine
Versandapotheke sendet. Der 2D-Code wird eingescannt.

**A_19629 - PS abgebende LEI: 2D-Code Scanner**

Das PS der abgebenden LEI MUSS einen 2D-Code Scanner für Datamatrix Code
unterstützen. **[\<=]**

**A_19630 - PS abgebende LEI: 2D-Code scannen**

Das PS der abgebenden LEI MUSS es dem Nutzer ermöglichen, einen 2D-Code für
E-Rezepte einzuscannen. **[\<=]**

**A_22078 - PS abgebende LEI: 2D-Code scannen - Gescannte Inhalte prüfen**

Das PS der abgebenden LEI MUSS die gescannten Inhalte vor einer weiteren
Verarbeitung validieren, um sich vor Schadsoftware zu schützen. **[\<=]**

Der 2D-Code auf einem durch eine verordnende LEI erstellten Ausdruck enthält
genau den E-Rezept-Token für ein E-Rezept. Der Versicherte kann in seinem
E-Rezept-FdV bis zu 3 E-Rezept-Token in einem 2D-Code zusammenfassen. Dies
dient einer besseren Usability.

**A_19631 - PS abgebende LEI: 2D-Code scannen - E-Rezept-Token extrahieren**

Das PS der abgebenden LEI MUSS den oder die E-Rezept-Token aus einem
eingescannten Datamatrix Code extrahieren. **[\<=]**

Für den Aufbau des 2D-Codes und Struktur des E-Rezept-Token siehe
[gemSpec_DM_eRp].

Mit den Informationen aus einem E-Rezept-Token kann das E-Rezept vom
E-Rezept-Fachdienst heruntergeladen werden.

### 5.4 Fehlerbehandlung

Tritt ein Fehler bei der Verarbeitung von Operationsaufrufen an einem Dienst der
TI (bspw. E-Rezept-Fachdienst) auf, dann antwortet der Dienst mit einer
Fehlermeldung. Das Format und die verwendeten Fehlercodes sind in den
Spezifikationen der Interfaces (bspw. [gemSpec_FD_eRp]) beschrieben. Weiterhin
können Fehler in der lokalen Verarbeitung auftreten.

**A_20152 - PS: Verständliche Fehlermeldung**

Das PS MUSS im Falle von Fehlern Fehlermeldungen bereitstellen, die es den
Mitarbeitern der Leistungserbringerinstitution ermöglichen, die Ursache des
Fehlers zu identifizieren und mögliche Gegenmaßnahmen zu ergreifen. **[\<=]**

### 6 Informationsmodell

Dienste der TI:

<table><tr><th>
Datenfeld

</th><th>
Herkunft

</th><th>
Beschreibung

</th></tr><tr><td>
E-Rezept-Fachdienst:

FQDN, Port

</td><td>
DNS-Abfrage am Konnektor

</td><td>
Lokalisierunginformationen

</td></tr><tr><td>
Identity Provider:

FQDN, Port, Path

</td><td>
DNS-Abfrage am Konnektor

</td><td>
Lokalisierunginformationen

</td></tr></table>

Authentisierung

<table><tr><th>
Datenfeld

</th><th>
Herkunft

</th><th>
Beschreibung

</th></tr><tr><td>
client_id

</td><td>
Organisatorischer Prozess zur Registrierung beim IDP

</td></tr><tr></tr></table>

Session-Daten

<table><tr><th>
Datenfeld

</th><th>
Herkunft

</th><th>
Beschreibung

</th></tr><tr><td>
ACCESS_TOKEN

</td><td>
IDP

</td><td>
Authentisierungs-Token für den Zugriff auf Dienste der TI

</td></tr><tr><td>
ID_TOKEN

</td><td>
IDP

</td><td>
zur Befüllung der Claims für neu ausgestellte ACCESS_TOKEN während einer
aktiven Session durch den IDP, ohne dass der IDP das Zertifikat neu
authentifizieren muss 

</td></tr><tr><td>
AUTHORIZATION_CODE 

</td><td>
IDP

</td><td>
Code für den Bezug eines ID_TOKENS und ACCESS_TOKENS nach einer erfolgreichen
Authentifizierung zwischen Authenticator-Funktion im Client und dem IDP 

</td></tr></table>

für PS verordnende LEI

E-Rezept:

<table><tr><th>
Datenfeld

</th><th>
Herkunft

</th><th>
Beschreibung

</th></tr><tr><td>
Task

</td><td>
E-Rezept-Fachdienst (

POST /Task/$create

)

</td><td>
https://simplifier.net/erezept-workflow/gemerxtask

 

</td></tr><tr><td>
E-Rezept-ID

</td><td>
Task.identifier mit NamingSystem "PrescriptionID"  
E-Rezept-ID (POST
/Task/$create)

</td><td>
https://simplifier.net/erezept-workflow/gemerxprescriptionid

  

</td></tr><tr><td>
Task-ID

</td><td>
E-Rezept-Fachdienst (

POST /Task/$create

)

</td><td>
https://hl7.org/fhir/http.html

 

</td></tr><tr><td>
AccessCode

</td><td>
E-Rezept-ID (

POST /Task/$create

)

</td><td>
https://simplifier.net/erezept-workflow/accesscode

 

</td></tr><tr><td>
E-Rezept-Bundle

</td><td>
Verordnungsdatenschnittstelle oder durch PS erstellt

</td><td>
https://simplifier.net/erezept/kbvprerpbundle

 

</td></tr></table>

für PS abgebende LEI:

E-Rezept:

<table><tr><th>
Datenfeld

</th><th>
Herkunft

</th><th>
Beschreibung

</th></tr><tr><td>
Task

</td><td>
E-Rezept-Fachdienst (

POST /Task/\<id\>/$accept

)

</td><td>
https://simplifier.net/erezept-workflow/gemerxtask 

  

</td></tr><tr><td>
E-Rezept-ID

</td><td>
E-Rezept-Fachdienst (POST /Task/\<id\>/$accept)  
Task.identifier
mit NamingSystem "PrescriptionID"

</td><td>
https://simplifier.net/erezept-workflow/gemerxprescriptionid  

  

</td></tr><tr><td>
Task-ID

</td><td>
E-Rezept-Token

2D-Code scannen oder E-Rezept-Nachricht (

GET /Communication

)

</td><td>
https://hl7.org/fhir/http.html 

 

</td></tr><tr><td>
AccessCode

</td><td>
E-Rezept-Token

2D-Code scannen oder E-Rezept-Nachricht (

GET /Communication

)

</td><td>
https://simplifier.net/erezept-workflow/accesscode 

 

</td></tr><tr><td>
Secret

</td><td>
E-Rezept-Fachdienst (

POST /Task/\<id\>/$accept

)

</td><td>
https://simplifier.net/erezept-workflow/secret

 

</td></tr><tr><td>
E-Rezept-Bundle

</td><td>
Enveloping in QES-Datensatz enthalten

E-Rezept-Fachdienst (

POST /Task/\<id\>/$accept

) 

</td><td>
https://simplifier.net/erezept/kbvprerpbundle

 

</td></tr><tr><td>
E-Rezept-Nachrichten

</td><td>
E-Rezept-Fachdienst (

GET /Communication

)

</td><td>
Anfrage Belieferung durch eine Apotheke:

https://gematik.de/fhir/StructureDefinition/erxCommunicationInfoReq

 

Einlöseauftrag:

https://gematik.de/fhir/StructureDefinition/erxCommunicationDispReq

 

Antwort der Apotheke:

https://gematik.de/fhir/StructureDefinition/erxCommunicationReply

 

https://simplifier.net/erezept-workflow/gemerxcommunication

  

</td></tr><tr><td>
Chargeninformation

</td><td>
Securpharm-Scan

</td><td>
Befüllung des Feldes

Medication.batch

im Profil 

https://fhir.kbv.de/StructureDefinition/KBV_PR_ERP_Medication_PZN

wenn Fertigarzneimittel, die einen Data-Matrix-Code gemäß securPharm-System
besitzen, dispensiert werden  

</td></tr><tr><td>
MedicationDispense

</td><td>
durch PS erstellt

</td><td>
https://simplifier.net/erezept-workflow/gemerxmedicationdispense

  

</td></tr></table>

### 7 Anhang A – Verzeichnisse

### 7.1 Abkürzungen

<table><tr><th>
Kürzel

</th><th>
Erläuterung

</th></tr><tr><td>
API

</td><td>
application programming interface

</td></tr><tr><td>
AVS

</td><td>
Apothekenverwaltungssystem

</td></tr><tr><td>
BMV

</td><td>
Bundesmantelvertrag

</td></tr><tr><td>
BSI

</td><td>
Bundesamt für Sicherheit in der Informationstechnik

</td></tr><tr><td>
DD

</td><td>
Discovery Document

</td></tr><tr><td>
DMC

</td><td>
Data-Matrix-Code

</td></tr><tr><td>
FdV

</td><td>
Frontend des Versicherten

</td></tr><tr><td>
FHIR

</td><td>
Fast Healthcare Interoperable Resources

</td></tr><tr><td>
HTTP

</td><td>
Hypertext Transfer Protocol

</td></tr><tr><td>
IDP

</td><td>
Identity Provider

</td></tr><tr><td>
JWT

</td><td>
JSON Web Token

</td></tr><tr><td>
KBV

</td><td>
Kassenärztliche Bundesvereinigung

</td></tr><tr><td>
KVNR

</td><td>
Krankenversichertennummer

</td></tr><tr><td>
LE 

</td><td>
Leistungserbringer

</td></tr><tr><td>
LEI

</td><td>
Leistungserbringerinstitution

</td></tr><tr><td>
PS

</td><td>
Primärsystem

</td></tr><tr><td>
PTV

</td><td>
Produkttypversion

</td></tr><tr><td>
PUK

</td><td>
Öffentlicher Schlüssel

</td></tr><tr><td>
QES

</td><td>
Qualifizierte Elektronische Signatur

</td></tr><tr><td>
TLS 

</td><td>
Transport Layer Security 

</td></tr><tr><td>
SMC-B

</td><td>
Security Module Card Typ B, Institutionenkarte

</td></tr><tr><td>
UC

</td><td>
Use Case

</td></tr><tr><td>
VAU

</td><td>
Vertrauenswürdige Ausführungsumgebung

</td></tr></table>

### 7.2 Glossar

<table><tr><th>
Begriff

</th><th>
Erläuterung

</th></tr><tr><td>
E-Rezept-Bundle

</td><td>
Ein E-Rezept-Bundle ist eine Bundle-FHIR-Ressource gemäß der Profilierung 

https://fhir.kbv.de/StructureDefinition/KBV_PR_ERP_Bundle

. Sie wird durch das PS der verordnenden LEI erstellt.

</td></tr><tr><td>
Funktionsmerkmal

</td><td>
Der Begriff beschreibt eine Funktion oder auch einzelne, eine logische Einheit
bildende Teilfunktionen der TI im Rahmen der funktionalen Zerlegung des Systems.

</td></tr><tr><td>
MedicationDispense

</td><td>
Ein MedicationDispense ist eine FHIR-Ressource gemäß der Profilierung 

https://gematik.de/fhir/StructureDefinition/erxMedicationDispense

 . Sie wird durch das PS der abgebenden LEI erstellt und beinhaltet
Informationen zum abgegebenen Mittel. Ein Versicherter, welcher ein
E-Rezept-FdV nutzt, kann auf die MedicationDispense-Information zu seinen
E-Rezepten zugreifen.

</td></tr><tr><td>
Task

</td><td>
Ein Task ist eine Task FHIR-Ressource gemäß der Profilierung 

https://gematik.de/fhir/StructureDefinition/erxTask

 . Sie beinhaltet die Metadaten zum Workflow eines E-Rezepts sowie die
Informationen zum E-Rezept (u.a. E-Rezept-Bundle).

</td></tr><tr><td>
Versicherten-ID

</td><td>
Die Versicherten-ID ist der 10-stellige unveränderliche Teil der
Krankenversichertennummer (KVNR).

</td></tr></table>

Das Glossar wird als eigenständiges Dokument (vgl. [gemGlossar]) zur Verfügung
gestellt.

### 7.3 Abbildungsverzeichnis

- [Abbildung-1] - ABB_ILFERP_001 – Systemzerlegung
- [Abbildung-2] - ABB_ILFERP_002 – Statusübergänge

### 7.4 Tabellenverzeichnis

- [Tabelle-1] - TAB_ILFERP_001 – E-Rezept-Status
- [Tabelle-2] - TAB_ILFERP_014 - HTTP-Header "X-erp-resource"
- [Tabelle-3] - TAB_ILFERP_012 – Zertifikatsnutzung
- [Tabelle-4] - TAB_ILFERP_002 – E-Rezept durch Verordnenden erstellen
- [Tabelle-5] - TAB_ILFERP_003 – E-Rezept durch Verordnenden einstellen
- [Tabelle-6] - TAB_ILFERP_004 – E-Rezept durch Verordnenden löschen
- [Tabelle-7] - TAB_ILFERP_005 – E-Rezept abrufen
- [Tabelle-8] - TAB_ILFERP_006 – Quittung abrufen
- [Tabelle-9] - TAB_ILFERP_007 – Quittung erneut abrufen
- [Tabelle-10] - TAB_ILFERP_008 – E-Rezept durch Abgebenden zurückgeben
- [Tabelle-11] - TAB_ILFERP_009 – E-Rezept durch Abgebenden löschen
- [Tabelle-12] - TAB_ILFERP_010 – Nachrichten von Versicherten empfangen
- [Tabelle-13] - TAB_ILFERP_015 – Nachricht von Versicherten empfangen - payload
- [Tabelle-14] - TAB_ILFERP_011 – Nachricht an Versicherten versenden
- [Tabelle-15] - TAB_ILFERP_016 – Nachricht an Versicherten versenden - payload
- [Tabelle-16] - TAB_ILFERP_013 – Nachricht durch Abgebenden löschen

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
[E-Rezept API Dokumentation]

</td><td>
gematik: 

https://github.com/gematik/api-erp

 

</td></tr><tr><td>
[gemGlossar]

</td><td>
gematik: Einführung der Gesundheitskarte – Glossar

</td></tr><tr><td>
[gemILF_PS]

</td><td>
gematik: Implementierungsleitfaden Primärsysteme - Telematikinfrastruktur (TI)

</td></tr><tr><td>
[gemKPT_eRp]

</td><td>
gematik: Konzept E-Rezept

</td></tr><tr><td>
[gemKPT_SysL_TI]

</td><td>
gematik: 

Systemdesign der Telematikinfrastruktur - Release 4.0

</td></tr><tr><td>
[gemSpec_DM_eRp]

</td><td>
gematik: Spezifikation Datenmodell E-Rezept 

</td></tr><tr><td>
[gemSpec_FD_eRp]

</td><td>
gematik: Spezifikation E-Rezept-Fachdienst

</td></tr><tr><td>
[gemSpec_IDP_Dienst]

</td><td>
gematik: 

Spezifikation Identity Provider – Dienst

</td></tr><tr><td>
[gemSpec_IDP_Frontend]

</td><td>
gematik: Spezifikation Identity Provider – Frontend

</td></tr><tr><td>
[gemSpec_Kon]

</td><td>
gematik: Spezifikation Konnektor

</td></tr><tr><td>
[gemSpec_Krypt]

</td><td>
gematik: 

Übergreifende Spezifikation Verwendung kryptographischer Algorithmen in der
Telematikinfrastruktur

</td></tr><tr><td>
[gemSpec_OID]

</td><td>
gematik: Spezifikation Festlegung von OIDs

</td></tr><tr><td>
[gemSysL_eRp]

</td><td>
gematik: Systemspezifisches Konzept E-Rezept

</td></tr></table>

### 7.5.2 Weitere Dokumente

<table><tr><th>
[Quelle]

</th><th>
Herausgeber (Erscheinungsdatum): Titel

</th></tr><tr><td>
[BMV]

</td><td>
Bundesmantelvertrag Ärzte

https://www.kbv.de/html/bundesmantelvertrag.php

 

</td></tr><tr><td>
[BMV-Z]

</td><td>
Bundesmantelvertrag - Zahnärzte

https://www.kzbv.de/bundesmantelvertrag.1223.de.html

 

</td></tr><tr><td>
[ExpBack]

</td><td>
Exponential Backoff

https://en.wikipedia.org/wiki/Exponential_backoff

 

</td></tr><tr><td>
[OASIS-VR]

</td><td>
OASIS: Profile for comprehensive multi-signature verification reports for OASIS
Digital Signature Services Version 1.0, Committee Specification 01, 12 November
2010,

http://docs.oasis-open.org/dss- x/profiles/verificationreport/oasis-dssx-1.0-
profiles-vr-cs01.pdf

 

</td></tr><tr><td>
[RFC7231]

</td><td>
Hypertext Transfer Protocol (HTTP/1.1): Semantics and Content

https://tools.ietf.org/html/rfc7231

 

</td></tr><tr><td>
[SecurPharm]

</td><td>
Inhalte und Struktur SecurPharm-Codes

http://www.securpharm.de/wp-content/uploads/2018/08/securPharm_Codierung_Regeln_DE_V2_03.pdf

 

Kapitel 5.2.3 und 5.2.4 für Chargeninformation + Verfallsdatum

</td></tr><tr><td>
[Split-DNS]

</td><td>
Split-horizon DNS

https://en.wikipedia.org/wiki/Split-horizon_DNS

 

</td></tr></table>





[Dokumentinformationen]: #dokumentinformationen
[Inhaltsverzeichnis]:    #inhaltsverzeichnis
[1]:                     #1-einordnung-des-dokumentes
[1.1]:                   #11-zielsetzung
[1.2]:                   #12-zielgruppe
[1.3]:                   #13-geltungsbereich
[1.4]:                   #14-abgrenzungen
[1.5]:                   #15-methodik
[1.5.1]:                 #151-hinweis-auf-offene-punkte
[2]:                     #2-systemüberblick
[3]:                     #3-systemkontext
[3.1]:                   #31-e-rezept-status
[3.2]:                   #32-fhir-ressourcen
[4]:                     #4-übergreifende-festlegungen
[4.1]:                   #41-logging-und-meldungen
[4.2]:                   #42-namensauflösung
[5]:                     #5-funktionsmerkmale
[5.1]:                   #51-allgemein
[5.1.1]:                 #511-kommunikation-zu-den-diensten-der-ti
[5.1.2]:                 #512-verschlüsselte-kommunikation-zur-vau-des-e-rezept-fachdienstes
[5.1.3]:                 #513-zertifikatsprüfung
[5.1.3.1]:               #5131-zertifikatsprüfung-von-zertifikaten-der-ti
[5.1.3.2]:               #5132-zertifikatsprüfung-von-internet-zertifikaten
[5.1.4]:                 #514-authentifizierung-der-lei
[5.1.4.1]:               #5141-übergreifende-festlegungen-zur-nutzung-des-idp-dienstes
[5.1.4.2]:               #5142-abruf-von-token-beim-idp-dienst
[5.2]:                   #52-anwendungsfälle-verordnende-lei
[5.2.1]:                 #521-e-rezept-erstellen
[5.2.2]:                 #522-e-rezept-einstellen
[5.2.3]:                 #523-e-rezept-löschen
[5.3]:                   #53-anwendungsfälle-abgebende-lei
[5.3.1]:                 #531-e-rezept-abrufen
[5.3.2]:                 #532-quittung-abrufen
[5.3.3]:                 #533-quittung-erneut-abrufen
[5.3.4]:                 #534-e-rezept-zurückgeben
[5.3.5]:                 #535-e-rezept-löschen
[5.3.6]:                 #536-nachrichten-von-versicherten-empfangen
[5.3.7]:                 #537-nachricht-an-versicherten-versenden
[5.3.8]:                 #538-nachricht-löschen
[5.3.9]:                 #539-abgabedatensatz-signieren
[5.3.10]:                #5310-2d-code-einscannen
[5.4]:                   #54-fehlerbehandlung
[6]:                     #6-informationsmodell
[7]:                     #7-anhang-a-–-verzeichnisse
[7.1]:                   #71-abkürzungen
[7.2]:                   #72-glossar
[7.3]:                   #73-abbildungsverzeichnis
[7.4]:                   #74-tabellenverzeichnis
[7.5]:                   #75-referenzierte-dokumente
[7.5.1]:                 #751-dokumente-der-gematik
[7.5.2]:                 #752-weitere-dokumente
[Abbildung-1]:           gemILF_PS_eRp_V1.3.0.attachments/14242908226831504654.png
[Abbildung-2]:           gemILF_PS_eRp_V1.3.0.attachments/10318857238100939551.png
[Tbl-001]:               #Tbl-001 (&93834775873520)
[Tabelle-1]:             #Tabelle-1 (&93834789488456)
[Tabelle-2]:             #Tabelle-2 (&93834789547008)
[Tabelle-3]:             #Tabelle-3 (&93834771082640)
[Tbl-005]:               #Tbl-005 (&93834810830192)
[Tabelle-4]:             #Tabelle-4 (&93834789225456)
[Tabelle-5]:             #Tabelle-5 (&93834781705536)
[Tabelle-6]:             #Tabelle-6 (&93834802317184)
[Tabelle-7]:             #Tabelle-7 (&93834802352736)
[Tabelle-8]:             #Tabelle-8 (&93834781234584)
[Tabelle-9]:             #Tabelle-9 (&93834811149272)
[Tabelle-10]:            #Tabelle-10 (&93834811181504)
[Tabelle-11]:            #Tabelle-11 (&93834767987016)
[Tabelle-12]:            #Tabelle-12 (&93834768020072)
[Tabelle-13]:            #Tabelle-13 (&93834768791344)
[Tabelle-14]:            #Tabelle-14 (&93834783498784)
[Tabelle-15]:            #Tabelle-15 (&93834799211896)
[Tabelle-16]:            #Tabelle-16 (&93834799251144)
[Tbl-019]:               #Tbl-019 (&93834802631912)
[Tbl-020]:               #Tbl-020 (&93834802642728)
[Tbl-021]:               #Tbl-021 (&93834802652096)
[Tbl-022]:               #Tbl-022 (&93834801531512)
[Tbl-023]:               #Tbl-023 (&93834800950728)
[Tbl-024]:               #Tbl-024 (&93834800997168)
[Tbl-025]:               #Tbl-025 (&93834776394368)
[Tbl-026]:               #Tbl-026 (&93834798952712)
[Tbl-027]:               #Tbl-027 (&93834798980184)
[https://github.com/gematik]: https://github.com/gematik (&93834768496488)
[https://cabforum.org/baseline-requirements-documents/]: https://cabforum.org/baseline-requirements-documents/ (&93834810845680)
[https://fhir.kbv.de/StructureDefinition/KBV_PR_ERP_Bundle]: https://fhir.kbv.de/StructureDefinition/KBV_PR_ERP_Bundle (&93834781682520)
[https://www.w3.org/TR/2008/REC-xml-c14n11-20080502/]: https://www.w3.org/TR/2008/REC-xml-c14n11-20080502/ (&93834781687344)
[https://simplifier.net/erezept-workflow/gemerxtask]: https://simplifier.net/erezept-workflow/gemerxtask (&93834801538416)
[https://simplifier.net/erezept-workflow/gemerxprescriptionid]: https://simplifier.net/erezept-workflow/gemerxprescriptionid (&93834801543400)
[https://hl7.org/fhir/http.html]: https://hl7.org/fhir/http.html (&93834801547240)
[https://simplifier.net/erezept-workflow/accesscode]: https://simplifier.net/erezept-workflow/accesscode (&93834801550896)
[https://simplifier.net/erezept/kbvprerpbundle]: https://simplifier.net/erezept/kbvprerpbundle (&93834800947256)
[https://simplifier.net/erezept-workflow/gemerxtask ]: https://simplifier.net/erezept-workflow/gemerxtask%A0 (&93834800957632)
[https://simplifier.net/erezept-workflow/gemerxprescriptionid  ]: https://simplifier.net/erezept-workflow/gemerxprescriptionid%A0%A0 (&93834800963336)
[https://hl7.org/fhir/http.html ]: https://hl7.org/fhir/http.html%A0 (&93834800967296)
[https://simplifier.net/erezept-workflow/accesscode ]: https://simplifier.net/erezept-workflow/accesscode%A0 (&93834800971256)
[https://simplifier.net/erezept-workflow/secret]: https://simplifier.net/erezept-workflow/secret (&93834800974912)
[https://simplifier.net/erezept/kbvprerpbundle]: https://simplifier.net/erezept/kbvprerpbundle (&93834800978872)
[https://gematik.de/fhir/StructureDefinition/erxCommunicationInfoReq]: https://gematik.de/fhir/StructureDefinition/erxCommunicationInfoReq (&93834800982656)
[https://gematik.de/fhir/StructureDefinition/erxCommunicationDispReq]: https://gematik.de/fhir/StructureDefinition/erxCommunicationDispReq (&93834800983912)
[https://gematik.de/fhir/StructureDefinition/erxCommunicationReply]: https://gematik.de/fhir/StructureDefinition/erxCommunicationReply (&93834800985472)
[https://simplifier.net/erezept-workflow/gemerxcommunication]: https://simplifier.net/erezept-workflow/gemerxcommunication (&93834800986912)
[https://fhir.kbv.de/StructureDefinition/KBV_PR_ERP_Medication_PZN]: https://fhir.kbv.de/StructureDefinition/KBV_PR_ERP_Medication_PZN (&93834800991296)
[https://simplifier.net/erezept-workflow/gemerxmedicationdispense]: https://simplifier.net/erezept-workflow/gemerxmedicationdispense (&93834800994536)
[https://fhir.kbv.de/StructureDefinition/KBV_PR_ERP_Bundle]: https://fhir.kbv.de/StructureDefinition/KBV_PR_ERP_Bundle (&93834776398904)
[https://gematik.de/fhir/StructureDefinition/erxMedicationDispense]: https://gematik.de/fhir/StructureDefinition/erxMedicationDispense (&93834776403104)
[https://gematik.de/fhir/StructureDefinition/erxTask]: https://gematik.de/fhir/StructureDefinition/erxTask (&93834776405680)
[https://github.com/gematik/api-erp]: https://github.com/gematik/api-erp (&93834798957224)
[https://www.kbv.de/html/bundesmantelvertrag.php]: https://www.kbv.de/html/bundesmantelvertrag.php (&93834798985064)
[https://www.kzbv.de/bundesmantelvertrag.1223.de.html]: https://www.kzbv.de/bundesmantelvertrag.1223.de.html (&93834798987944)
[https://en.wikipedia.org/wiki/Exponential_backoff]: https://en.wikipedia.org/wiki/Exponential_backoff (&93834798990824)
[http://docs.oasis-open.org/dss- x/profiles/verificationreport/oasis-dssx-1.0- profiles-vr-cs01.pdf]: http://docs.oasis-open.org/dss-x/profiles/verificationreport/oasis-dssx-1.0-profiles-vr-cs01.pdf (&93834798993400)
[https://tools.ietf.org/html/rfc7231]: https://tools.ietf.org/html/rfc7231 (&93834798996280)
[http://www.securpharm.de/wp-content/uploads/2018/08/securPharm_Codierung_Regeln_DE_V2_03.pdf]: http://www.securpharm.de/wp-content/uploads/2018/08/securPharm_Codierung_Regeln_DE_V2_03.pdf (&93834798999160)
[https://en.wikipedia.org/wiki/Split-horizon_DNS]: https://en.wikipedia.org/wiki/Split-horizon_DNS (&93834799002344)
