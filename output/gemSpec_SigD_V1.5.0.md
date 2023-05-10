
Elektronische Gesundheitskarte und Telematikinfrastruktur

### Spezifikation<br>Signaturdienst

- Klassifizierung: öffentlich
- Referenzierung: gemSpec_SigD
- Revision: 567442
- Stand: 06.02.23
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
30.04.19

</td><td>
freigegeben

</td><td>
gematik

</td></tr><tr><td>
1.1.0

</td><td>
28.06.19

</td><td>
Einarbeitung Änderungsliste P19.1

</td><td>
gematik

</td></tr><tr><td>
1.2.0

</td><td>
02.10.19

</td><td>
Einarbeitung Änderungsliste P20.2

</td><td>
gematik

</td></tr><tr><td>
Einarbeitung Änderungsliste P21.1

</td><td>
gematik

</td></tr><tr><td>
1.3.0

</td><td>
02.03.20

</td><td>
freigegeben

</td><td>
gematik

</td></tr><tr><td>
1.4.0

</td><td>
12.10.20

</td><td>
Einarbeitung Scope-Themen zu R4.0.1

</td><td>
gematik

</td></tr><tr><td>
1.5.0

</td><td>
06.02.23

</td><td>
Einarbeitung IDP_Maintenance_22.2

</td><td>
gematik

</td></tr></table>

### Inhaltsverzeichnis

- [Dokumentinformationen]
- [Inhaltsverzeichnis]
- [1] Einordnung des Dokuments
  - [1.1] Zielsetzung
  - [1.2] Zielgruppe
  - [1.3] Geltungsbereich
  - [1.4] Abgrenzungen
  - [1.5] Methodik
- [2] Systemüberblick
- [3] Systemkontext
  - [3.1] Akteure und Rollen
  - [3.2] Nachbarsysteme
  - [3.3] Sicherheitsanforderungen für den operativen Betrieb
- [4] Zerlegung des Signaturdienstes
- [5] Übergreifende Festlegungen
- [6] Funktionsmerkmale
  - [6.1] Schnittstelle I_Remote_Sign_Operations
    - [6.1.1] Operationsdefinition I_Remote_Sign_Operations::sign_Data
    - [6.1.2] Umsetzung I_Remote_Sign_Operations::sign_Data
  - [6.2] Schnittstelle P_Create_Identity
  - [6.3] Schnittstelle P_Delete_Identity
- [7] Anhang – Verzeichnisse
  - [7.1] Abkürzungen
  - [7.2] Glossar
  - [7.3] Abbildungsverzeichnis
  - [7.4] Tabellenverzeichnis
  - [7.5] Referenzierte Dokumente
    - [7.5.1] – Dokumente der gematik
    - [7.5.2] – Weitere Dokumente

### 1 Einordnung des Dokuments

### 1.1 Zielsetzung

Die vorliegende Spezifikation definiert die Anforderungen an den Produkttyp
Signaturdienst einschließlich der durch ihn bereitgestellten Schnittstellen.

### 1.2 Zielgruppe

Das Dokument richtet sich an Hersteller des Signaturdienstes und Anbieter von
Signaturdiensten.

### 1.3 Geltungsbereich

Dieses Dokument enthält normative Festlegungen zur Telematikinfrastruktur des
deutschen Gesundheitswesens für den Online-Produktivbetrieb. Der
Gültigkeitszeitraum der vorliegenden Version und deren Anwendung in
Zulassungs- oder Abnahmeverfahren wird durch die gematik GmbH in gesonderten
Do­kumenten (z.B. Dokumentenlandkarte, Produkttypsteckbrief,
Leistungsbeschreibung) festgelegt und bekannt gegeben.

Wichtiger Schutzrechts-/Patentrechtshinweis

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

Spezifiziert werden in diesem Dokument die vom Signaturdienst bereitgestellten
(angebotenen) Schnittstellen. Benutzte Schnittstellen werden in der
Spezifikation desjenigen Produkttypen beschrieben, der diese Schnittstelle
bereitstellt. Auf die entsprechenden Dokumente wird referenziert (siehe auch
Anhang, Kap. ).

Die vollständige Anforderungslage für den Produkttyp ergibt sich aus weiteren
Konzept- und Spezifikationsdokumenten. Diese sind in dem Produkttypsteckbrief
des Signaturdienstes verzeichnet.

Nicht Bestandteil des vorliegenden Dokumentes sind die Festlegungen zum
Themenbereich Betrieb. Die betrieblichen Anforderungen sind im
Anbietertypsteckbrief zum TSP X.509 nonQES eGK mit Option Signaturdienst
verzeichnet.

### 1.5 Methodik

Anforderungen als Ausdruck normativer Festlegungen werden durch eine eindeutige
ID sowie die dem RFC 2119 [RFC2119] entsprechenden, in Großbuchstaben
geschriebenen deutschen Schlüsselworte MUSS, DARF NICHT, SOLL, SOLL NICHT,
KANN gekennzeichnet.Sie werden im Dokument wie folgt dargestellt:\<AFO-ID\> -
\<Titel der Afo\>Text / Beschreibung [\<=]Dabei umfasst die Anforderung
sämtliche zwischen Afo-ID und der Textmarke [\<=] angeführten Inhalte.

### 2 Systemüberblick

Der Signaturdienst erzeugt elektronische Identifizierungsmittel
für Versicherte in der Umgebung des Anbieters des Signaturdienstes. Ein
elektronisches Identifizierungsmittel ist gemäß Verordnung (EU) Nr. 910/2014
[eIDAS] eine materielle und/oder immaterielle Einheit, die
Personenidentifizierungsdaten enthält und zur
Authentifizierung bei Online-Diensten verwendet wird. Die vom Signaturdienst
ausgestellten elektronischen Identifizierungsmittel sind kryptographische
Identitäten basierend auf asymmetrischer Kryptographie und Teil des
Vertrauensraums für X.509 nonQES-Identitäten der Telematikinfrastruktur. Die
vom Signaturdienst erstellten elektronischen Identifizierungsmittel
(Zertifikate) nutzen Versicherte zur Authentisierung an den Diensten der
elektronischen Patientenakte.

Versicherte können elektronische Signaturen, mittels Authentisierung durch
einen sektoralen Identity Provider, in der vom Anbieter des Signaturdienstes
geführten Umgebung erstellen lassen. Die elektronischen Signaturen des
Signaturdienstes sind eine Alternative zur elektronischen Signatur mittels der
Identität ID.CH.AUT der eGK.

Der Signaturdienst erstellt elektronische Identifizierungsmittel für
Versicherte ausschließlich über korrespondierende Identitäten bzw.
Personenidentifizierungsdaten eines sektoralen Identity Provider gemäß
[gemSpec_IDP_Sek] im Auftrag des Kartenherausgebers der eGK des Versicherten.
Personenidentifizierungsdaten sind ein Datensatz, der es ermöglicht, die
Identität des Versicherten mitsamt der Herkunft der erhobenen Daten
abzubilden. Die von einem sektoralen Identity Provider bereitgestellten
Personenidentifizierungsdaten entsprechen den Personenidentifizierungsdaten im
Zertifikat C.CH.AUT der eGK des Versicherten. Das Zertifikatsprofil
C.CH.AUT_ALT für die vom Signaturdienst ausgestellten elektronischen
Identifizierungsmittel ist in [gemSpec_PKI] festgelegt.

### 3 Systemkontext

### 3.1 Akteure und Rollen

Im Kontext des Signaturdienstes treten folgende Akteure auf:

Anbieterdes Signaturdienstes:Anbieter eines Signaturdienstes setzen die in
dieser Spezifikation beschriebenen Aufgaben des Signaturdienstes um.

Kartenherausgeber eGKKartenherausgeber der eGK beauftragen den Anbieter eines
Signaturdienstes, um für ihre Versicherten auf deren Wunsch hin elektronische
Identifizierungsmittel ausstellen zu lassen, die alternativ zur Identität
ID.CH.AUT der eGK genutzt werden können. Falls sich ein Versicherter
gegenüber dem Kartenherausgeber seiner eGK für ein elektronisches
Identifizierungsmittel entscheidet, beauftragt der Kartenherausgeber eGK für
diesen Versicherten beim Anbieter des Signaturdienstes das elektronische
Identifizierungsmittel. Der Kartenherausgeber eGK übermittelt hierzu die für
das elektronische Identifizierungsmittel notwendigen
Personenidentifikationsdaten des Versicherten (u.a. Name, KVNR) an den Anbieter
des Signaturdienstes.Der Kartenherausgeber eGK veranlasst die Sperrung von
elektronischen Identifizierungsmitteln bzgl. seiner Versicherten beim TSP
X.509 nonQES eGK, der das Zertifikat für das elektronische
Identifizierungsmittel erstellt hat. 

VersicherteVersicherte nutzen mittels eigener Client-Systeme den Signaturdienst,
um mittels der elektronischen Identifizierungsmittel anderen Diensten ihre
Identität zu bestätigen.Versicherte richten sich an den Kartenherausgeber
ihrer eGK, falls sie ihr elektronisches Identifizierungsmittel sperren lassen
möchten.

Sektoraler Identity Provider

Ein sektoraler Identity Provider einer autoritativen Stelle (z. B. eine
Krankenversicherung) gibt für ihre Versicherten eine digitale Identität aus.
Diese Versicherten-ID wird über Standards der OpenID Foundation Anwendungen
der TI zur Verfügung gestellt. Zu den Aufgaben einer autoritativen Stelle
gehören:

 ---> UL

Der sektorale Identity Provider übernimmt aus diesen Aufgaben die
Identitätsfeststellung und Authentifizierung von Versicherten sowie die
Bestätigung ihrer Attribute. Die verschiedenen Dienste und sektoralen Identity
Provider sind über den Federation Master [gemSpec_IDP_FedMaster] in einem
Vertrauensraum organisiert. Jedoch ist es aufgrund der
direktenBeziehungen zwischen Karteherausgeber der eGK, sektoralem Identity
Provider, Signaturdienst und ePA-FdV nicht notwendig, dass der Signaturdienst
die Funktionen der Föderation verwendet. Es besteht im Fall einer Anmeldung
für den Zugriff auf eine elektronische Patientenakte eine klare Verbindung
zwischen ePA-FdV, Signaturdienst und sektoralem Identity Provider, sodass die
Vertrauensbeziehungen hier nicht über die Mechanismen der Föderation
aufgebaut werden müssen.

### 3.2 Nachbarsysteme

Die folgende Abbildung zeigt die Beziehung zu benachbarten Systemen mit den vom
Signaturdienst bereitgestellten und genutzten Schnittstellen.

![Abbildung-1][Abbildung-1]

Der Signaturdienst wird als Provider einer technischen Schnittstelle zum
Erstellen elektronischer Signaturen für Clients und einer Prozessschnittstelle
für Kartenherausgeber eGK zum Beauftragen und Löschen von elektronischen
Identifizierungsmitteln für Versicherte aufgerufen.

Der Signaturdienst nutzt die Schnittstellen desTSP X.509 nonQES - eGK zum
Erstellen von Zertifikaten.

### 3.3 Sicherheitsanforderungen für den operativen Betrieb

Der Anbieter Signaturdienst muss die folgenden Anforderungen erfüllen:

**A_19033 - Schützenswerte Objekte**

Der Anbieter Signaturdienst MUSS die folgenden kryptographischen Objekte als
schützenswerte Objekte in seinem Sicherheitskonzept berücksichtigen: (a)
Private Schlüssel, (b) Öffentlicher Schlüssel, (c) Öffentlicher Schlüssel
von Antragstellern, (d) Anträge zur Ausstellung von X.509-Zertifikaten, (e)
Authentisierungsinformationen von Sperrberechtigten, (f) Dokumentation über
beauftragte und durchgeführte Sperrungen, (g) Statusinformationen, (h)
Zulassungsdokumente, (i) Registrierungsdokumente, (j)
Authentisierungsinformationen zur Authentisierung von internen Akteuren bzw.
Rollen, (k) Protokolldaten, (l) Konfigurationsdaten. **[\<=]**

**A_19037 - Gesicherte interne Schnittstellen des Anbieters Signaturdienst**

Der Anbieter Signaturdienst MUSS für den internen Datenaustausch einen
Mechanismus zur Sicherung der Datenintegrität, der Authentizität und zur
Vertraulichkeit der Daten zur Verfügung stellen. **[\<=]**

**A_19038 - Datenaustausch zwischen gematik und Anbieter Signaturdienst**

Der Anbieter Signaturdienst MUSS für den Datenaustausch zur gematik einen
Mechanismus zur Sicherung der Datenintegrität, der Authentizität und zur
Vertraulichkeit der Daten zur Verfügung stellen. **[\<=]**

**A_19039 - Gesicherte externe Schnittstellen des Anbieters Signaturdienst**

Der Anbieter Signaturdienst MUSS für den Datenaustausch mit anderen Rollen und
Diensten einen Mechanismus zur Sicherung der Datenintegrität, der
Authentizität und zur Vertraulichkeit der Daten zur Verfügung stellen. Hierzu
gehören die Schnittstellen vona) Anbieter Signaturdienst zum berechtigten
Zertifikatsantragsteller zur Beantragung und Ausstellung von
Zertifikaten,    b) Anbieter Signaturdienst zum Sperrantragsteller für die
Sperrung von Zertifikaten. **[\<=]**

**A_19040 - Eindeutige Verbindung Zertifikatsnehmer und privater Schlüssel**

Der Anbieter Signaturdienst MUSS sicherstellen, dass der öffentliche
Schlüssel, dem die Attribute des Zertifikatsnehmers in einem Zertifikat
zugeordnet werden, und der private Schlüssel des Zertifikatsnehmers
zusammengehören. **[\<=]**

**A_19041-01 - Umsetzung Signaturdienst für Zertifikate**

Der Anbieter Signaturdienst MUSS nach erfolgreicher erster Authentifizierung des
Antragstellers die erforderlichen Angaben zur Zertifikatserstellung an den
Erstellungsdienst des TSP X.509 nonQES - eGK weiterleiten. **[\<=]**

**A_19042 - Trennung der Signaturdienst-Betriebsumgebungen**

Der Anbieter Signaturdienst MUSS sicherstellen, dass das Testsystem von dem
Produktivsystem technisch, organisatorisch und betrieblich so getrennt werden,
dass keine gegenseitige Beeinflussung und keine Verwechslung möglich sind.
**[\<=]**

**A_19043 - Datenschutzgerechte Antrags- und Sperrprozesse**

Der Anbieter Signaturdienst MUSS die Antrags- und Sperrprozesse
datenschutzgerecht ausgestalten, d.h. insbesondere sind für die Verarbeitung
der Antrags- und Sperrauftragsdaten die Datenschutzgrundsätze gemäß Art. 5
DSGVO zu berücksichtigen sowie die technischen und organisatorischen
Maßnahmen nach Art. 25 und Art. 32 DSGVO zu treffen. **[\<=]**

**A_19044 - Löschung von Signaturdienst-Zertifikatstatusinformationen,
Zertifikats- und Sperranträgen**

Der Anbieter Signaturdienst MUSS die Zertifikatsanträge und die Sperraufträge
zu einem X.509-Zertifikat unverzüglich löschen, sobald die gesetzlichen oder
vertraglichen Aufbewahrungsfristen erreicht sind. **[\<=]**

**A_19045 - Fehlerprotokollierung**

Falls es erforderlich sein sollte, dass der Anbieter Signaturdienst eine
Protokollierung zum Zwecke der Fehler- bzw. Störungsbehebung durchführt,
MÜSSEN die Protokolldaten entsprechend des Datenschutzgrundsatzes der
Datenminimierung gemäß Art. 5 Abs. 1 Satz 1 lit.c) DSGVO unter
Berücksichtigung der Art. 25, 32 DSGVO derart gestaltet sein, dass nur
personenbezogene Daten in der Art und dem Umfang enthalten sind, wie sie zur
Behebung erforderlich sind. **[\<=]**

### 4 Zerlegung des Signaturdienstes

Eine Zerlegung des Produkttyps Signaturdienst wird nicht vorgegeben.

### 5 Übergreifende Festlegungen

Der Signaturdienst muss die folgenden übergreifenden Anforderungen erfüllen.

**A_17373-01 - Signaturdienst - Produkt erfordert Authentisierung auf dem
Vertrauensniveau "hoch"**

Der Hersteller des Signaturdienstes MUSS sein Produkt so implementieren, dass
dieses die Freischaltung nach einer Authentisierung des Nutzers über einen
sektoralen Identity Provider auf dem Vertrauensniveau
"gematik-ehealth-loa-high" vorsieht.  **[\<=]**

**A_17336-01 - Signaturdienst - Sicherheitsniveau der Authentisierung auf dem
Vertrauensniveau "hoch"**

Der Anbieter des Signaturdienstes MUSS für den angebotenen Signaturdienst
sicherstellen, dass die Nutzung nur nach Authentisierung des Nutzers über
einenzugelassenen sektoralen Identity Provider auf dem Vertrauensniveau
"gematik-ehealth-loa-high" erfolgt. **[\<=]**

Die Anmeldung des elektronischen Identifizierungsmittels inklusive
Identitätsnachweis und -überprüfung des Versicherten erfolgt durch den
Kartenherausgeber eGK auf Grundlage der GKV-SV Richtlinie "Kontakt mit
Versicherten" nach § 217f Abs. 4b SGB V.

Eine Notifizierung des elektronischen Identifizierungssystems, welches die
elektronischen Identifizierungsmittel ausstellt, ist nicht gefordert. Ebenso
ist nicht gefordert, dass der Anbieter ein qualifizierter oder
nichtqualifizierter Vertrauensdiensteanbieter gemäß Verordnung (EU) Nr.
910/2014 ist.

Zur Erstellung der Signatur kann eine nach eIDAS zertifizierte qualifizierte
Signatur/Siegelerstellungseinheit (QSEE) eingesetzt werden.

**A_17369 - Signaturdienst - Elektronische Identifizierungsmittel sind
kryptographische Identitäten der TI**

Der Signaturdienst MUSS als elektronische Identifizierungsmittel
kryptographische Identitäten ausstellen, die aus einem privaten und einem
öffentlichen Schlüssel mit dazugehörigem Zertifikat des
TypsC.CH.AUT_ALT aus dem Vertrauensraum der TI bestehen.  **[\<=]**

**A_17370 - Signaturdienst - ECC-Verfahren für elektronische
Identifizierungsmittel**

Der Signaturdienst MUSS elektronische Identifizierungsmittel auf der Grundlage
von ECC-Verfahren erstellen. **[\<=]**

Für die Erzeugung von ECC-Schlüsseln sind die Vorgaben in [gemSpec_Krypt]
einzuhalten.

**A_17371 - Signaturdienst - Keine RSA-Verfahren für elektronische
Identifizierungsmittel**

Der Signaturdienst DARF elektronische Identifizierungsmittel NICHT auf der
Grundlage von RSA-Verfahren erstellen. **[\<=]**

**A_17339 - Signaturdienst - Speicherung privater Schlüssel mit einem HSM**

Der Anbieter des Signaturdienstes MUSS die privaten Schlüssel der
elektronischen Identifizierungsmittel mit einem HSM  speichern und
sicherstellen, dass die Eignung des HSM durch eine erfolgreiche Evaluierung
nachgewiesen wurde. Als Evaluierungsschemata kommen dabei Federal Information
Processing Standard (FIPS) oder Common Criteria mit mindestens folgender
Prüftiefe in Frage:  

 ---> OL

**[\<=]**

**A_17853-01 - Signaturdienst - Auskunft an Versicherten**

Der Anbieter des Signaturdienstes MUSS dem Versicherten auf dessen Verlangen
Auskunft geben über erfolgte Zugriffe auf das elektronische
Identifizierungsmittel des Versicherten. **[\<=]**

Hinweis: Die Auskunft des Versicherten kann auch über den Kartenherausgeber
erfolgen, der den Anbieter des Signaturdienstes mit der Erstellung des
elektronischen Identifizierungsmittels beauftragt hat.

**A_17864 - Signaturdienst - Anbieter des Signaturdienstes ist kein Anbieter
eines ePA-Aktensystems**

Der Anbieter des Signaturdienstes MUSS unabhängig von Anbietern von
ePA-Aktensystemen sein, d.h. es sind mindestens jeweils eigenständige
Rechtspersönlichkeiten mit eigenständigen operativen Geschäfts- und
Betriebsführungen und es ist eine strikte Vermeidung von
Personenidentitäten bzw.
Doppelrollen in den Funktionen Geschäftsführung, leitende Mitarbeiter und
Zugangsberechtigte zum Betriebsort des Signaturdienstes bzw. ePA-Aktensystems
gewährleistet. **[\<=]**

Hinweis: Die Anforderung schließt nicht aus, dass die Anbieter verbundene
Unternehmen im Sinne des § 15 AktG sind.

**A_18957 - Darstellen der Voraussetzungen für sicheren Betrieb des Produkts im
Handbuch**

Der Hersteller des Signaturdienstes MUSS für sein Produkt im dazugehörigen
Handbuch leicht ersichtlich darstellen, welche Voraussetzungen vom Betreiber
und der Betriebsumgebung erfüllt werden müssen, damit ein sicherer Betrieb
des Produktes gewährleistet werden kann. **[\<=]**

**A_18958 - Sicherer Betrieb des Produkts nach Handbuch**

Der Anbieter eines Signaturdienstes MUSS die im Handbuch des eingesetzten
Signaturdienstes beschriebenen Voraussetzungen für den sicheren Betrieb des
Produktes gewährleisten. **[\<=]**

### 6 Funktionsmerkmale

Der Signaturdienst realisiert die Funktionsmerkmale zur Erstellung
elektronischer Identifizierungsmittel und deren Nutzung für elektronische
Signaturen. Das Funktionsmerkmal wird über die Implementierung der
Schnittstellen I_Remote_Sign_Operation,P_Create_IdentityundP_Delete_Identityrealisiert.

### 6.1 Schnittstelle I_Remote_Sign_Operations

Die in diesem Abschnitt beschriebene logische
SchnittstelleI_Remote_Sign_Operationssetzt die gleichnamige Schnittstelle aus
[gemKPT_Arch_TIP] um.

**A_17383 - Signaturdienst - I_Remote_Sign_Operations im Internet**

Der Signaturdienst MUSS die SchnittstelleI_Remote_Sign_Operationsim Internet
anbieten. **[\<=]**

**A_17382 - Signaturdienst - Schutz gegen OWASP Top 10-Risiken**

Der Anbieter des Signaturdienstes MUSS sicherstellen, dass die
Internet-Schnittstelle I_Remote_Sign_Operationsresistent bezüglich der im
aktuellen und den beiden vorherigen OWASP Top 10 Report(s) ausgewiesenen
Risiken ist. **[\<=]**

Hinweis: Die Nichtanwendbarkeit eines OWASP Top 10-Risikos ist zu begründen.
Für Informationen zum Umgang mit den OWASP Top 10-Risiken wird auf den
aktuellen [OWASP Top 10 Report] und die darin enthaltenen Vorgehensweisen für
z. B. Entwickler und Tester verwiesen.

**A_17528 - Signaturdienst - Schutz der Verbindung zum Signaturdienst**

Der Anbieter des Signaturdienstes MUSS sicherstellen, dass die
SchnittstelleI_Remote_Sign_Operationsvon Klienten nur über eine gegen
Abhören, Manipulation und Replay-Angriffe geschützte Verbindung genutzt
werden kann. **[\<=]**

### 6.1.1 Operationsdefinition I_Remote_Sign_Operations::sign_Data

**A_17238-01 - Signaturdienst - Logische Schnittstelle I_Remote_Sign_Operations**

Der Signaturdienst MUSS die
SchnittstelleI_Remote_Sign_Operations::sign_Datagemäß dem folgenden logischen
Ablauf implementieren:

Tabelle1: Tab_SigD_01 -  I_Remote_Sign_Operations::sign_Data - Definition

<table><tr><th colspan="2">
Operation

</th><th colspan="3">
I_Remote_Sign_Operations::sign_Data

</th></tr><tr><td colspan="2">
Beschreibung

</td><td colspan="3">
Die Operation erzeugt eine ECDSA-Signatur unter Einhaltung der Vorgaben in
[gemSpec_Krypt] des übergebenen Datum (Data) mittels des privaten Schlüssels
des elektronischen Identifizierungsmittels ID.CH.AUT_ALT des aufrufenden
Nutzers (Identifier).  
Das signierte Datum (SignedData) und das Zertifikat des
elektronischen Identifizierungsmittels C.CH.AUT_ALT der Identität, für die
signiert wurde, werden als Ergebnis der Operation zurückgeliefert.

</td></tr><tr><td colspan="5">
Eingangsparameter

</td></tr><tr><td colspan="2">
Name

</td><td colspan="2">
Beschreibung

</td><td>
Typ

</td></tr><tr><td colspan="2">
Data

</td><td colspan="2">
Die zu signierenden Daten.

</td><td>
Binary

</td></tr><tr><td colspan="2">
Identifier

</td><td colspan="2">
Identifiziert, welches elektronisches Identifizierungsmittel ID.CH.AUT_ALT zur
Signatur des Datums genutzt werden soll.  
Der Identifier ergibt sich aus den
Attributen nach Authentisierung des Nutzers an einem sektoralen Identity
Provider.

</td><td>
String

</td></tr><tr><td colspan="5">
Ausgangsparameter

</td></tr><tr><td colspan="2">
Name

</td><td colspan="2">
Beschreibung

</td><td>
Typ

</td></tr><tr><td colspan="2">
SignedData

</td><td colspan="2">
Das mit dem privaten Schlüssel des elektronischen Identifizierungsmittels
ID.CH.AUT_ALT signierte Datum.

</td><td>
Binary

</td></tr><tr><td colspan="2">
Certificate

</td><td colspan="2">
Zertifikat C.CH.AUT_ALT des elektronischen

Identifizierungsmittels,

mit dessen zugehörigem privaten Schlüssel signiert wurde.

</td><td>
Certificate X.509

</td></tr></table>

**[\<=]**

### 6.1.2 Umsetzung I_Remote_Sign_Operations::sign_Data

Die folgenden Anforderungen beschreiben die Umsetzung der
Operation I_Remote_Sign_Operations::sign_Data.

**A_17527 - Signaturdienst - Aufruf der Operation nur über geschützte
Verbindung**

Der Signaturdienst MUSS sicherstellen, dass die Operation
I_Remote_Sign_Operations::sign_Data von Klienten nur über eine gegen
Abhören, Manipulation und Replay-Angriffe geschützte Verbindung aufgerufen
werden kann. **[\<=]**

**A_17741 - Signaturdienst - Freischaltung vorzeitig beenden**

Der Signaturdienst MUSS sicherstellen, dass der Client die Freischaltung der
OperationI_Remote_Sign_Operations::sign_Data  bzgl. eines Nutzers explizit
beenden kann und somit beim nächsten Aufruf der Operation durch diesen Nutzer
eineerneute Authentifizierung erforderlich ist. **[\<=]**

**A_18710 - Maximale Gültigkeit einer Authentifizierung**

Der Signaturdienst und der Anbieter des Signaturdienstes MÜSSEN sicherstellen,
dass eine erfolgreiche Authentifizierung des Nutzers für maximal 1 Stunde
gültig ist, um die Operation I_Remote_Sign_Operations::sign_Data von dem
Client, von dem sich der Nutzer authentisiert hat, aufzurufen. **[\<=]**

**A_18711 - Signaturdienst – Nutzung einer erfolgreichen Authentifizierung**

Der Signaturdienst und der Anbieter des Signaturdienstes MÜSSEN sicherstellen,
dass eine erfolgreiche Authentifizierung des Nutzers maximal einmal genutzt
werden kann, um die Operation I_Remote_Sign_Operations::sign_Data für maximal
5 Minuten ohne erneute Authentifizierung des Nutzers von dem Client (auch
mehrmals) aufzurufen, von dem sich der Nutzer authentisiert hat, und nach
Ablauf der 5 Minuten die Operation I_Remote_Sign_Operations::sign_Data nur nach
erneuter erfolgreicher Authentifizierung des Nutzers wieder genutzt werden
kann. **[\<=]**

### 6.2 Schnittstelle P_Create_Identity

**A_17375-01 - Signaturdienst - P_Create_Identity**

Der Anbieter des Signaturdienstes MUSS eine Prozess-Schnittstelle umsetzen,
mittels derer Kartenherausgeber dem Signaturdienst einen Auftrag zur
Ausstellung eines elektronischen Identifizierungsmittels für einen
Versicherten erteilen können. Der Auftrag MUSS die für das
elektronische Identifizierungsmittel notwendigen Personenidentifikationsdaten
für das ZertifikatC.CH.AUT_ALTenthalten.Die Zuordnung des elektronischen
Identifizierungsmittels zu einem Nutzer erfolgt über die Identifikationsdaten
des sektoralen Identity Provider. **[\<=]**

**A_17372 - Signaturdienst - Schutz des Auftrags der Krankenkasse während des
Transports**

Der Anbieter des Signaturdienstes MUSS sicherstellen, dass die im Auftrag der
Krankenkasse enthaltenen personenbezogenen oder sensiblen Daten während des
Transports von der Krankenkasse zum Signaturdienst gegen Abhören, Manipulation
und Replay-Angriffe geschützt werden. **[\<=]**

**A_17379 - Signaturdienst - Zertifikatsabruf beim TSP X.509 nonQES eGK**

Der Signaturdienst MUSS das Zertifikat des TypsC.CH.AUT_ALTüber die
Schnittstelle I_Cert_Provisioning zum Zertifikatabruf beim TSP X.509 nonQES eGK
mit den vom Kartenherausgeber übermittelten Personenidentifikationsdaten aus
dem Auftrag anfordern. **[\<=]**

### 6.3 Schnittstelle P_Delete_Identity

**A_17808 - Signaturdienst - P_Delete_Identity**

Der Anbieter des Signaturdienstes MUSS eine Prozess-Schnittstelle umsetzen,
mittels derer Kartenherausgeber die Löschung genau derjenigen elektronischen
Identifizierungsmittel beim Signaturdienst veranlassen können, deren
Ausstellung sie zuvor beauftragt haben. **[\<=]**

### 7 Anhang – Verzeichnisse

### 7.1 Abkürzungen

<table><tr><th>
Kürzel

</th><th>
Erläuterung

</th></tr><tr><td>
eGK

</td><td>
elektronische Gesundheitskarte

</td></tr><tr><td>
ePA

</td><td>
elektronische Patientenakte

</td></tr><tr><td>
HSM

</td><td>
Hardware Security Module

</td></tr><tr><td>
QES

</td><td>
Qualifizierte Elektronische Signatur

</td></tr><tr><td>
RSA

</td><td>
kryptographischer Algorithmus (nach Rivest, Shamir, Adleman)

</td></tr><tr><td>
TSP

</td><td>
Trust Service Provider

</td></tr></table>

### 7.2 Glossar

Das Glossar wird als eigenständiges Dokument, vgl. [gemGlossar] zur Verfügung
gestellt.

### 7.3 Abbildungsverzeichnis

- [Abbildung-1] - Benachbarte Systeme des Signaturdienstes mit bereitgestellten und genutzten Schnittstellen

### 7.4 Tabellenverzeichnis

- [Tabelle-1] - Tab_SigD_01 -  I_Remote_Sign_Operations::sign_Data - Definition

### 7.5 Referenzierte Dokumente

### 7.5.1 – Dokumente der gematik

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
gematik: Einführung der Gesundheitskarte - Glossar

</td></tr><tr><td>
[gemKPT_Arch_TIP]

</td><td>
gematik: Konzept Architektur der TI-Plattform

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
[GVO_IOPVZ]

</td><td>
gematik: Geschäfts- und Verfahrensordnung für das
Interoperabilitätsverzeichnis vesta: (Verzeichnis elektronischer Standards und
Anwendungen im Gesundheitswesen)

</td></tr></table>

### 7.5.2 – Weitere Dokumente

<table><tr><th>
[Quelle]

</th><th>
Herausgeber (Erscheinungsdatum): Titel

</th></tr><tr><td>
[BSI-TR-03111]

</td><td>
Technical Guideline BSI TR-03111  
Elliptic Curve Cryptography, Version 2.10,
Date: 2018-06-01 

https://www.bsi.bund.de/SharedDocs/Downloads/EN/BSI/Publications/TechGuidelines/TR03111/BSI-TR-03111_pdf.pdf?__blob=publicationFile&v=2

</td></tr><tr><td>
[eIDAS 910/2014]

</td><td>
Verordnung (EU) Nr. 910/2014 des Europäischen Parlaments und des Rates vom
23. Juli 2014 über elektronische Identifizierung und Vertrauensdienste für
elektronische Transaktionen im Binnenmarkt und zur Aufhebung der Richtlinie
1999/93/EG

</td></tr><tr><td>
[eIDAS 2015/1502]

</td><td>
DURCHFÜHRUNGSVERORDNUNG (EU) 2015/1502 DER KOMMISSION  
vom 8. September 2015
zur  Festlegung  von  Mindestanforderungen  an  technische 
Spezifikationen  und  Verfahren  für Sicherheitsniveaus elektronischer
Identifizierungsmittel gemäß Artikel 8 Absatz 3 der Verordnung (EU)  Nr. 
910/2014  des  Europäischen  Parlaments  und  des  Rates  über 
elektronische  Identifizierung und Vertrauensdienste für elektronische
Transaktionen im Binnenmarkt

</td></tr><tr><td>
[OWASP Top 10 Report]

</td><td>
OWASP Foundation, OWASP Top Ten Project: “OWASP Top 10 The Ten Most Critical
Web Application Security Risks“, 
https://www.owasp.org/index.php/Category:OWASP_Top_Ten_Project 

</td></tr><tr><td>
[RFC2119]

</td><td>
IETF (1997): Key words for use in RFCs to Indicate Requirement Levels, RFC 2119,
http://tools.ietf.org/html/rfc2119

</td></tr></table>





[Dokumentinformationen]: #dokumentinformationen
[Inhaltsverzeichnis]:    #inhaltsverzeichnis
[1]:                     #1-einordnung-des-dokuments
[1.1]:                   #11-zielsetzung
[1.2]:                   #12-zielgruppe
[1.3]:                   #13-geltungsbereich
[1.4]:                   #14-abgrenzungen
[1.5]:                   #15-methodik
[2]:                     #2-systemüberblick
[3]:                     #3-systemkontext
[3.1]:                   #31-akteure-und-rollen
[3.2]:                   #32-nachbarsysteme
[3.3]:                   #33-sicherheitsanforderungen-für-den-operativen-betrieb
[4]:                     #4-zerlegung-des-signaturdienstes
[5]:                     #5-übergreifende-festlegungen
[6]:                     #6-funktionsmerkmale
[6.1]:                   #61-schnittstelle-i_remote_sign_operations
[6.1.1]:                 #611-operationsdefinition-i_remote_sign_operationssign_data
[6.1.2]:                 #612-umsetzung-i_remote_sign_operationssign_data
[6.2]:                   #62-schnittstelle-p_create_identity
[6.3]:                   #63-schnittstelle-p_delete_identity
[7]:                     #7-anhang-–-verzeichnisse
[7.1]:                   #71-abkürzungen
[7.2]:                   #72-glossar
[7.3]:                   #73-abbildungsverzeichnis
[7.4]:                   #74-tabellenverzeichnis
[7.5]:                   #75-referenzierte-dokumente
[7.5.1]:                 #751-–-dokumente-der-gematik
[7.5.2]:                 #752-–-weitere-dokumente
[Abbildung-1]:           gemSpec_SigD_V1.5.0.attachments/6426316276783116570.png
[Tbl-001]:               #Tbl-001 (&93834811901240)
[Tabelle-1]:             #Tabelle-1 (&93834765162208)
[Tbl-003]:               #Tbl-003 (&93834764168528)
[Tbl-004]:               #Tbl-004 (&93834768495192)
[Tbl-005]:               #Tbl-005 (&93834799837264)
