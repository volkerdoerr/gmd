
Elektronische Gesundheitskarte und Telematikinfrastruktur

### Produkttypsteckbrief<br>Prüfvorschrift<br>Identity Provider - Dienst

- Klassifizierung: öffentlich
- Produkttyp Status: freigegeben
- Produkttyp Version: 2.3.1-0
- Referenzierung: gemProdT_IDP-Dienst_PTV_2.3.1-0
- Revision: 548770
- Stand: 14.02.2022
- Status: freigegeben
- Version: 1.0.0

### Historie Produkttypversion und Produkttypsteckbrief

Historie Produkttypversion

Die Produkttypversion ändert sich, wenn sich die normativen Festlegungen für
den Produkttyp ändern und die Umsetzung durch Produktentwicklungen ebenfalls
betroffen ist.

<table><tr><th>
Produkttypversion

</th><th>
Beschreibung der Änderung

</th><th>
Referenz

</th></tr><tr><td>
1.0.0-0

</td><td>
Initiale Version auf Dokumentenebene

</td><td>
gemProdT_IDP-Dienst_PTV_1.0.0-0

</td></tr><tr><td>
2.0.0-0

</td><td>
Anpassung auf Releasestand 4.0.1

</td><td>
gemProdT_IDP-Dienst_PTV_2.0.0-0

</td></tr><tr><td>
2.1.0-0

</td><td>
Anpassung auf Releasestand 4.0.1 Hotfix 1

</td><td>
gemProdT_IDP-Dienst_PTV_2.1.0-0

</td></tr><tr><td>
2.2.0-0

</td><td>
Anpassung auf Releasestand IDP 2.2.0 (inkl. entsprechender Anteile aus
gemF_Tokenverschlüsselung & gemF_Biometrie) und der Änderungsliste
IdP_Maintenance_21.1  

</td><td>
gemProdT_IDP-Dienst_PTV_2.2.0-0

</td></tr><tr><td>
2.3.0-0

</td><td>
Anpassung bzgl. Nutzung der Anmeldung durch sektorale Identity Provider

und Anpassungen aufgrund Änderungsliste IDP_CR_Q4

zus.: fehlerhafte Anforderungszuordnungen korrigiert

(Prüfverfahrenszuweisungen sind nun gemäß IdP_Maintenance_21.1 korrekt
angepasst)

</td><td>
gemProdT_IDP-Dienst_PTV_2.3.0-0

</td></tr><tr><td>
2.3.1-0

</td><td>
Anpassung aufgrund der Einarbeitung der Änderungen aus Betr_Maintenance_21.3
sowie Anpassungen aus [gemSpec_Krypt], [gemSpec_SST_LD_BD] und redaktionellen
Anpassungen

</td><td>
gemProdT_IDP-Dienst_PTV_2.3.1-0

</td></tr></table>

Historie Produkttypsteckbrief

Die Dokumentenversion des Produkttypsteckbriefs ändert sich mit jeder
inhaltlichen oder redaktionellen Änderung des Produkttypsteckbriefs und seinen
referenzierten Dokumenten. Redaktionelle Änderungen haben keine Auswirkung auf
die Produkttypversion.

<table><tr><th>
Version

</th><th>
Stand

</th><th>
Kap.

</th><th>
Grund der Änderung, besondere Hinweise

</th><th>
Bearbeiter

</th></tr><tr><td>
1.0.0

</td><td>
14.02.22

</td><td>
freigegeben

</td><td>
gematik

</td></tr></table>

### Inhaltsverzeichnis

- [Historie] Produkttypversion und Produkttypsteckbrief
- [Inhaltsverzeichnis]
- [1] Einführung
  - [1.1] Zielsetzung und Einordnung des Dokumentes
  - [1.2] Zielgruppe
  - [1.3] Geltungsbereich
  - [1.4] Abgrenzung des Dokumentes
  - [1.5] Methodik
- [2] Dokumente
- [3] Normative Festlegungen
  - [3.1] Festlegungen zur funktionalen Eignung
    - [3.1.1] Produkttest/Produktübergreifender Test
    - [3.1.2] Herstellererklärung funktionale Eignung
  - [3.2] Festlegungen zur sicherheitstechnischen Eignung
    - [3.2.1] Herstellererklärung sicherheitstechnische Eignung
    - [3.2.2] Sicherheitsgutachten
    - [3.2.3] Produktgutachten
- [4] Anhang – Verzeichnisse
  - [4.1] Abkürzungen
  - [4.2] Tabellenverzeichnis
  - [4.3] Referenzierte Dokumente

### 1 Einführung

### 1.1 Zielsetzung und Einordnung des Dokumentes

Dieser Produkttypsteckbrief verzeichnet verbindlich die normativen Festlegungen
der gematik an Herstellung und Betrieb von Produkten des Produkttyps oder
verweist auf Dokumente, in denen verbindliche Festlegungen mit ggf. anderer
Notation zu finden sind. Die normativen Festlegungen bilden die Grundlage für
die Erteilung von Zulassungen, Zertifizierungen bzw. Bestätigungen durch die
gematik. (Wenn im weiteren Dokument vereinfachend der Begriff „Zulassung“
verwendet wird, so ist dies der besseren Lesbarkeit geschuldet und umfasst
übergreifend neben dem Verfahren der Zulassung auch Zertifizierungen und
Bestätigungen der gematik-Zulassungsstelle.)

Die normativen Festlegungen werden über ihren Identifier, ihren Titel sowie die
Dokumentenquelle referenziert. Die normativen Festlegungen mit ihrem
vollständigen, normativen Inhalt sind dem jeweils referenzierten Dokument zu
entnehmen.

### 1.2 Zielgruppe

Der Produkttypsteckbrief richtet sich an Hersteller des Identity Provider
Dienstes (IDP-Dienst) sowie Hersteller und Anbieter von Produkttypen, die
hierzu eine Schnittstelle besitzen.

Das Dokument ist außerdem zu verwenden von:

 ---> UL

Bei zentralen Diensten der TI-Plattform und fachanwendungsspezifischen Diensten
beziehen sich normativen Festlegungen, die sowohl an Anbieter als auch
Hersteller gerichtet sind, jeweils auf den Anbieter als Zulassungsnehmer, bei
dezentralen Produkten auf den Hersteller.

### 1.3 Geltungsbereich

Dieses Dokument enthält normative Festlegungen zur Telematikinfrastruktur des
deutschen Gesundheitswesens. Der Gültigkeitszeitraum der vorliegenden Version
und deren Anwendung in Zulassungsverfahren werden durch die gematik GmbH in
gesonderten Dokumenten (z.B. gemPTV_ATV_Festlegungen, Leistungsbeschreibung)
festgelegt und bekannt gegeben.

### 1.4 Abgrenzung des Dokumentes

Dieses Dokument macht keine Aussagen zur Aufteilung der Produktentwicklung bzw.
Produktherstellung auf verschiedene Hersteller und Anbieter.

Dokumente zu den Zulassungsverfahren für den Produkttyp sind nicht aufgeführt.
Die geltenden Verfahren und Regelungen zur Beantragung und Durchführung von
Zulassungsverfahren können der Homepage der gematik entnommen werden.

### 1.5 Methodik

Die im Dokument verzeichneten normativen Festlegungen werden tabellarisch
dargestellt. Die Tabellenspalten haben die folgende Bedeutung:

ID:Identifiziert die normative Festlegung eindeutig im Gesamtbestand aller
Festlegungen der gematik.

Bezeichnung:Gibt den Titel einer normativen Festlegung informativ wieder, um die
thematische Einordnung zu erleichtern. Der vollständige Inhalt der normativen
Festlegung ist dem Dokument zu entnehmen, auf das die Quellenangabe verweist.

Quelle (Referenz):Verweist auf das Dokument, das die normative Festlegung
definiert.

### 2 Dokumente

Die nachfolgenden Dokumente enthalten alle für den Produkttyp normativen
Festlegungen.

<table><tr><th>
Dokumentenkürzel

</th><th>
Bezeichnung des Dokumentes

</th><th>
Version

</th></tr><tr><td>
gemSpec_OM

</td><td>
Übergreifende Spezifikation Operations und Maintenance

</td><td>
1.14.0

</td></tr><tr><td>
gemKPT_Test

</td><td>
Testkonzept der TI

</td><td>
2.8.5

</td></tr><tr><td>
gemSpec_IDP_Frontend

</td><td>
Spezifikation Identity Provider - Frontend

</td><td>
1.3.0

</td></tr><tr><td>
gemSpec_DS_Hersteller

</td><td>
Spezifikation Datenschutz- und Sicherheitsanforderungen der TI an Hersteller

</td><td>
1.3.0

</td></tr><tr><td>
gemSpec_Net

</td><td>
Übergreifende Spezifikation Netzwerk

</td><td>
1.21.0

</td></tr><tr><td>
gemSpec_PKI

</td><td>
Übergreifende Spezifikation – Spezifikation PKI

</td><td>
2.11.1

</td></tr><tr><td>
gemSpec_Perf

</td><td>
Übergreifende Spezifikation Performance und Mengengerüst TI-Plattform

</td><td>
2.17.0

</td></tr><tr><td>
gemSpec_IDP_Dienst

</td><td>
Spezifikation Identity Provider - Dienst

</td><td>
1.4.0

</td></tr><tr><td>
gemSpec_SST_LD_BD

</td><td>
Spezifikation Logdaten und Betriebsdatenerfassung

</td><td>
1.2.0

</td></tr><tr><td>
gemSpec_Krypt

</td><td>
Übergreifende Spezifikation Verwendung kryptographischer Algorithmen in der
Telematikinfrastruktur

</td><td>
2.21.0

</td></tr></table>

Errata

Neben den vorgenannten Dokumenten werden auf der Internetseite der gematik bei
Bedarf Errata-Dokumente mit normativen Ergänzungen bzw. Korrekturen zu den
Spezifikationsdokumenten veröffentlicht. Sofern in den Errata der vorliegende
Produkttyp benannt wird, sind diese bei der Umsetzung des Produkttyps
entsprechend der Vorgabe in der Dokumentenlandkarte zu berücksichtigen. Dabei
kann eine abweichende Produkttypversion festgelegt werden.

### 3 Normative Festlegungen

Die folgenden Abschnitte verzeichnen alle für den Produkttypen normativen
Festlegungen, die für die Herstellung und den Betrieb von Produkten des
Produkttyps notwendig sind. Die Festlegungen sind gruppiert nach der Art der
Nachweisführung ihrer Erfüllung als Grundlage der Zulassung, Zertifizierung
bzw. Bestätigung.

### 3.1 Festlegungen zur funktionalen Eignung

### 3.1.1 Produkttest/Produktübergreifender Test

In diesem Abschnitt sind alle funktionalen und nichtfunktionalen Festlegungen an
den technischen Teil des Produkttyps verzeichnet, deren Umsetzung im Zuge von
Zulassungstests durch die gematik geprüft wird.

<table><tr><th>
ID

</th><th>
Bezeichnung

</th><th>
Quelle (Referenz)

</th></tr><tr><td>
A_20313-01

</td><td>
Inhalte des Claims

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20314-01

</td><td>
Maximale Gültigkeitsdauer des "AUTHORIZATION_CODE" und des "CHALLENGE_TOKEN"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20315-01

</td><td>
"AUTHORIZATION_CODE" nach Gültigkeitsende nicht mehr verwenden

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20318

</td><td>
Keine Token für widerrufene Entitäten

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20321-01

</td><td>
Annahme und Prüfung von "AUTHORIZATION_CODE" und "KEY_VERIFIER"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20323

</td><td>
TOKEN-Ausgabe Protokollierung in allen Fällen

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20327-02

</td><td>
Signatur des "ID_TOKEN" und "ACCESS_TOKEN"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20376

</td><td>
Verwendung des Attributes "state"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20377

</td><td>
Verwendung des Attributes "state"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20434

</td><td>
Einhaltung der Standards bei der Realisierung des Authorization-Endpunkts

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20439

</td><td>
Das Discovery Document enthält statische Adressen

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20440-01

</td><td>
Schematische Prüfung des Consent

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20458-02

</td><td>
Inhalte des Discovery Document

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20459

</td><td>
Das Attribut AUTH_TIME muss in allen Token unverändert bleiben

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20462

</td><td>
Maximale Gültigkeitsdauer des "ID_TOKEN"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20463

</td><td>
Maximale Gültigkeitsdauer des "ACCESS_TOKEN"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20464

</td><td>
Token-Endpunkt (Datensparsamkeit)

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20465

</td><td>
Zertifikatsprüfung gegen OCSP-Responder

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20521-02

</td><td>
Inhalt des CHALLENGE_TOKEN an das Authenticator-Modul

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20522

</td><td>
Erstellen einer "SESSION_ID"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20523

</td><td>
Zusammenstellung der Claims zum "user_consent"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20524-04

</td><td>
Befüllen der Claims "given_name", "family_name", "organizationName",
"professionOID", "idNummer", "acr" und "amr"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20588-01

</td><td>
IdP-Dienst - Erkennung Clientsystem User-Agent

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20589

</td><td>
IdP-Dienst – Ausschluss bestimmter Clientsystem-Versionsnummern von der
Kommunikation

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20591-01

</td><td>
Festlegungen zur Signatur der Discovery Documents

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20687-01

</td><td>
Bereitstellung der öffentlichen Schlüsselteile

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20688

</td><td>
Discovery Document interne und externe Adressierung

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20691-01

</td><td>
Das Discovery Document ist maximal 24 Stunden alt

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20692-01

</td><td>
Maximale Gültigkeitsdauer eines SSO_TOKEN

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20693-01

</td><td>
Senden des "AUTHORIZATION_CODE" und "SSO_TOKEN" an die "REDIRECT_URI"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20694

</td><td>
Zusammenstellung des "SSO_TOKEN"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20695-01

</td><td>
Signieren des "SSO_TOKEN"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20696

</td><td>
Verschlüsselung des "SSO_TOKEN"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20697

</td><td>
Zusammenstellung des "AUTHORIZATION_CODE"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20698

</td><td>
Annahme des Authorization Request

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20699-03

</td><td>
Annahme von CHALLENGE_TOKEN: Authentication_Data-Struktur

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20731

</td><td>
Verwendung des Attributes "auth_time"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20732

</td><td>
Aufnahme der öffentlichen Schlüssel in das Discovery Document

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20946-01

</td><td>
Annahme eines "SSO_TOKEN"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20947

</td><td>
Entschlüsselung des "SSO_TOKEN"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20948-01

</td><td>
Validierung des "SSO_TOKEN"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20949

</td><td>
Anforderung einer Authentisierung bei negativer Validierung des "SSO_TOKEN"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20950-01

</td><td>
Positive Validierung des "SSO_TOKEN"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20951-01

</td><td>
Validierung der Signatur und des Zertifikats des CHALLENGE_TOKEN

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20952

</td><td>
Claim "aud" im Token setzen

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21315-01

</td><td>
Bereitstellung einer URI zum Einreichen von SSO_TOKEN

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21317

</td><td>
Verschlüsselung des "AUTHORIZATION_CODE"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21318

</td><td>
Prüfung des "AUTHORIZATION_CODE“

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21319

</td><td>
Prüfung des "CODE_VERIFIER"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21320

</td><td>
Entschlüsseln des "Token-Key"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21321

</td><td>
Verschlüsselung von "ACCESS_TOKEN" und "ID_TOKEN"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21330

</td><td>
Ablaufzeitpunkt von "AUTHORIZATION_CODE" und "SSO_TOKEN"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21411

</td><td>
Registrierungsfunktion des IdP-Dienstes: Fehlermeldungen

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21412

</td><td>
Registrierungsfunktion des IdP-Dienstes: Registrierung

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21413

</td><td>
Registrierungsfunktion des IdP-Dienstes: Prüfung des Scope

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21415

</td><td>
Registrierungsfunktion des IdP-Dienstes: Datenformate und Syntax zur
Kommunikation mit dem Authenticator-Modul

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21419

</td><td>
Registrierungsfunktion des IdP-Dienstes: Anforderung an die Authentifizierung
des Nutzers

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21420

</td><td>
Registrierungsfunktion des IdP-Dienstes: Entschlüsselung der Registrierungsdaten

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21421

</td><td>
Registrierungsfunktion des IdP-Dienstes: Validierung der signierten Pairing-Daten

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21422

</td><td>
Registrierungsfunktion des IdP-Dienstes: Validierung des Zusammenhangs von
ACCESS_TOKEN und Pairing-Daten

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21423

</td><td>
Registrierungsfunktion des IdP-Dienstes: Bewertung des Gerätetyps

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21424

</td><td>
Registrierungsfunktion des IdP-Dienstes: Speicherung der Pairing-Daten

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21425

</td><td>
Registrierungsfunktion des IdP-Dienstes: Validierung des übermittelten
ACCESS_TOKENS

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21427

</td><td>
Registrierungsfunktion des IdP-Dienstes: Rückmeldung an den Nutzer

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21428

</td><td>
Erweiterung des Authorization-Endpunkts: Fehlermeldungen

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21429-02

</td><td>
Erweiterung des Authorization-Endpunkts: Realisierung verschiedener
Authentifizierungsmethoden

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21432

</td><td>
Erweiterung des Authorization-Endpunkts: Prüfung der vorliegenden Gerätedaten

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21433

</td><td>
Erweiterung des Authorization-Endpunkts: Validierung des
Authentifizierungszertifikats

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21434

</td><td>
Erweiterung des Authorization-Endpunkts: Auslesen der gespeicherten Pairing-Daten

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21435

</td><td>
Erweiterung des Authorization-Endpunkts: Validierung der mathematischen
Integrität der gespeicherten Pairing-Daten

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21437

</td><td>
Erweiterung des Authorization-Endpunkts: Bewertung der Gültigkeit des
öffentlichen Schlüssels in den Pairing-Daten

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21438

</td><td>
Erweiterung des Authorization-Endpunkts: Validierung der mathematischen
Integrität der signierten Authentication_Data-Struktur

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21439

</td><td>
Erweiterung des Authorization-Endpunkts: Zu unterstützende Algorithmen zur
Prüfung der mathematischen Integrität der signierten
Authentication_Data-Struktur

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21440

</td><td>
Erweiterung des Authorization-Endpunkts: Produktion des Authorization Code und
eines SSO_TOKEN

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21441

</td><td>
Inspektions- und Deregistrierungsfunktion des IDP-Dienstes: Fehlermeldungen

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21445

</td><td>
Inspektions- und Deregistrierungsfunktion des IdP-Dienstes: Validierung und
Verarbeitung des ACCESS_TOKEN

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21447

</td><td>
Inspektions- und Deregistrierungsfunktion des IdP-Dienstes: Annahme des
Kommandos zur Deaktivierung des Pairings

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21448

</td><td>
Inspektions- und Deregistrierungsfunktion des IdP-Dienstes: Deaktivierung des
identifizierten Pairing-Datensatzes

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21449

</td><td>
Erweiterung des Authorization-Endpunkts: Datenmodell und Syntax zur
Kommunikation mit dem Authenticator-Modul

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21450

</td><td>
Inspektions- und Deregistrierungsfunktion des IdP-Dienstes: Datenmodell und
Syntax zur Kommunikation mit dem Authenticator-Modul

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21452

</td><td>
Inspektions- und Deregistrierungsfunktion des IdP-Dienstes: Rückgabe der
Pairing-Daten

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21470

</td><td>
Registrierungsfunktion des IdP-Dienstes: Prüfung des Zusammenhangs zwischen
Pairing-Daten und übermittelten Authentifizierungszertifikat

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21472

</td><td>
SSO_TOKEN nur für Mobile Endgeräte und nicht für Primärsysteme

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_22262

</td><td>
Bereitstellung eines Third-Party Authorization Endpoint

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_22263

</td><td>
Sitzungsmanagement des IDP-Dienstes zu einem sektoralen Identity Provider

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_22264

</td><td>
Authorization-Request des IDP-Dienstes an sektorale Identity Provider

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_22265

</td><td>
Token Request des IDP-Dienstes an sektorale Identity Provider

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_22266

</td><td>
Authentisierung des IDP-Dienstes gegenüber den sektoralen Identity Providern

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_22269

</td><td>
Produktion eines Authorization Code nach Bestätigung des sektoralen Identity
Provider

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_22271

</td><td>
Befüllen der Claims "given_name", "family_name", "organizationName",
"professionOID", "idNummer", "acr" und "amr" nach Bestätigung durch einen
sektoralen Identity Provider

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_22282

</td><td>
Periodisches Einlesen der Discovery Documents und Schlüssel der sektoralen
Identity Provider

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_22283

</td><td>
Bereitstellung einer Liste der registrierten Authenticator-Module von sektoralen
Identity Providern

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_22286

</td><td>
Erweiterung des Discovery Document des IDP-Dienstes

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_22287

</td><td>
Veröffentlichung des Third-Party Authorization Endpoint

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_22290

</td><td>
Zwischenspeichern (Caching) von Smartcard-basierten OCSP-Antworten

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_22328

</td><td>
IDP-Dienst: Überprüfung der korrekten keyUsage des AUT-Zertifikats

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21442

</td><td>
Inspektions- und Deregistrierungsfunktion des IdP-Dienstes: Authentisierung des
Nutzers

</td><td>
gemSpec_IDP_Frontend

</td></tr><tr><td>
A_17124

</td><td>
TLS-Verbindungen (ECC-Migration)

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
A_18464

</td><td>
TLS-Verbindungen, nicht Version 1.1

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
GS-A_4359

</td><td>
X.509-Identitäten für die Durchführung einer TLS-Authentifizierung

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
GS-A_4384

</td><td>
TLS-Verbindungen

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
GS-A_4385

</td><td>
TLS-Verbindungen, Version 1.2

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
GS-A_4387

</td><td>
TLS-Verbindungen, nicht Version 1.0

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
GS-A_5035

</td><td>
Nichtverwendung des SSL-Protokolls

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
GS-A_5322

</td><td>
Weitere Vorgaben für TLS-Verbindungen

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
GS-A_5526

</td><td>
TLS-Renegotiation-Indication-Extension

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
GS-A_3702

</td><td>
Inhalt der Selbstauskunft von Produkten außer Karten

</td><td>
gemSpec_OM

</td></tr><tr><td>
GS-A_5025

</td><td>
Versionierung von Produkten auf Basis von zentralen Produkttypen der
TI-Plattform und fachanwendungsspezifischen Diensten durch die
Produktidentifikation

</td><td>
gemSpec_OM

</td></tr><tr><td>
A_17688

</td><td>
Nutzung des ECC-RSA-Vertrauensraumes (ECC-Migration)

</td><td>
gemSpec_PKI

</td></tr><tr><td>
A_17690

</td><td>
Nutzung der Hash-Datei für TSL (ECC-Migration)

</td><td>
gemSpec_PKI

</td></tr><tr><td>
A_17700

</td><td>
TSL-Auswertung ServiceTypeIdentifier "unspecified"

</td><td>
gemSpec_PKI

</td></tr><tr><td>
GS-A_4637

</td><td>
TUCs, Durchführung Fehlerüberprüfung

</td><td>
gemSpec_PKI

</td></tr><tr><td>
GS-A_4642

</td><td>
TUC_PKI_001: Periodische Aktualisierung TI-Vertrauensraum

</td><td>
gemSpec_PKI

</td></tr><tr><td>
GS-A_4643

</td><td>
TUC_PKI_013: Import TI-Vertrauensanker aus TSL

</td><td>
gemSpec_PKI

</td></tr><tr><td>
GS-A_4646

</td><td>
TUC_PKI_017: Lokalisierung TSL Download-Adressen

</td><td>
gemSpec_PKI

</td></tr><tr><td>
GS-A_4647

</td><td>
TUC_PKI_016: Download der TSL-Datei

</td><td>
gemSpec_PKI

</td></tr><tr><td>
GS-A_4648

</td><td>
TUC_PKI_019: Prüfung der Aktualität der TSL

</td><td>
gemSpec_PKI

</td></tr><tr><td>
GS-A_4649

</td><td>
TUC_PKI_020: XML-Dokument validieren

</td><td>
gemSpec_PKI

</td></tr><tr><td>
GS-A_4650

</td><td>
TUC_PKI_011: Prüfung des TSL-Signer-Zertifikates

</td><td>
gemSpec_PKI

</td></tr><tr><td>
GS-A_4651

</td><td>
TUC_PKI_012: XML-Signatur-Prüfung

</td><td>
gemSpec_PKI

</td></tr><tr><td>
GS-A_4652-01

</td><td>
TUC_PKI_018: Zertifikatsprüfung in der TI

</td><td>
gemSpec_PKI

</td></tr><tr><td>
GS-A_4653-01

</td><td>
TUC_PKI_002: Gültigkeitsprüfung des Zertifikats

</td><td>
gemSpec_PKI

</td></tr><tr><td>
GS-A_4654-01

</td><td>
TUC_PKI_003: CA-Zertifikat finden

</td><td>
gemSpec_PKI

</td></tr><tr><td>
GS-A_4655-01

</td><td>
TUC_PKI_004: Mathematische Prüfung der Zertifikatssignatur

</td><td>
gemSpec_PKI

</td></tr><tr><td>
GS-A_4656

</td><td>
TUC_PKI_005: Adresse für Status- und Sperrprüfung ermitteln

</td><td>
gemSpec_PKI

</td></tr><tr><td>
GS-A_4657-03

</td><td>
TUC_PKI_006: OCSP-Abfrage

</td><td>
gemSpec_PKI

</td></tr><tr><td>
GS-A_4660-02

</td><td>
TUC_PKI_009: Rollenermittlung

</td><td>
gemSpec_PKI

</td></tr><tr><td>
GS-A_4661-01

</td><td>
kritische Erweiterungen in Zertifikaten

</td><td>
gemSpec_PKI

</td></tr><tr><td>
GS-A_4662

</td><td>
Bedingungen für TLS-Handshake

</td><td>
gemSpec_PKI

</td></tr><tr><td>
GS-A_4663

</td><td>
Zertifikats-Prüfparameter für den TLS-Handshake

</td><td>
gemSpec_PKI

</td></tr><tr><td>
GS-A_4749-01

</td><td>
TUC_PKI_007: Prüfung Zertifikatstyp

</td><td>
gemSpec_PKI

</td></tr><tr><td>
GS-A_4751

</td><td>
Fehlercodes bei TSL- und Zertifikatsprüfung

</td><td>
gemSpec_PKI

</td></tr><tr><td>
GS-A_4829

</td><td>
TUCs, Fehlerbehandlung

</td><td>
gemSpec_PKI

</td></tr><tr><td>
GS-A_4898

</td><td>
TSL-Grace-Period einer TSL

</td><td>
gemSpec_PKI

</td></tr><tr><td>
GS-A_4899

</td><td>
TSL Update-Prüfintervall

</td><td>
gemSpec_PKI

</td></tr><tr><td>
GS-A_4943

</td><td>
Alter der OCSP-Responses für eGK-Zertifikate

</td><td>
gemSpec_PKI

</td></tr><tr><td>
GS-A_4957-01

</td><td>
Beschränkungen OCSP-Request

</td><td>
gemSpec_PKI

</td></tr><tr><td>
GS-A_5077

</td><td>
FQDN-Prüfung beim TLS-Handshake

</td><td>
gemSpec_PKI

</td></tr><tr><td>
GS-A_5215

</td><td>
Festlegung der zeitlichen Toleranzen in einer OCSP-Response

</td><td>
gemSpec_PKI

</td></tr><tr><td>
GS-A_5336

</td><td>
Zertifikatsprüfung nach Ablauf TSL-Graceperiod

</td><td>
gemSpec_PKI

</td></tr><tr><td>
A_20243

</td><td>
Performance - IdP-Dienst - Robustheit gegenüber Lastspitzen

</td><td>
gemSpec_Perf

</td></tr><tr><td>
A_20247

</td><td>
Performance - Erfassung von Rohdaten - IdP-Dienst

</td><td>
gemSpec_Perf

</td></tr><tr><td>
A_21340-01

</td><td>
IDP- Abbruch bei OCSP-Timeout

</td><td>
gemSpec_Perf

</td></tr><tr><td>
A_21980

</td><td>
Performance - Rohdaten - Leerlieferung (Rohdatenerfassung v.02)

</td><td>
gemSpec_Perf

</td></tr><tr><td>
A_21981-01

</td><td>
Performance - Rohdaten - Format des Rohdaten-Performance-Berichtes
(Rohdatenerfassung v.02)

</td><td>
gemSpec_Perf

</td></tr><tr><td>
A_21982

</td><td>
Performance - Rohdaten - Message-Block (Rohdatenerfassung v.02)

</td><td>
gemSpec_Perf

</td></tr><tr><td>
A_22000

</td><td>
Performance - Rohdaten - zu liefernde Dateien (Rohdatenerfassung v.02)

</td><td>
gemSpec_Perf

</td></tr><tr><td>
A_22001

</td><td>
Performance - Rohdaten - Name der Berichte (Rohdatenerfassung v.02)

</td><td>
gemSpec_Perf

</td></tr><tr><td>
A_22002

</td><td>
Performance - Rohdaten - Übermittlung (Rohdatenerfassung v.02)

</td><td>
gemSpec_Perf

</td></tr><tr><td>
A_22004

</td><td>
Performance - Rohdaten - Korrektheit (Rohdatenerfassung v.02)

</td><td>
gemSpec_Perf

</td></tr><tr><td>
A_22012-01

</td><td>
Performance - Rohdaten - Spezifika IDP - Duration (Rohdatenerfassung v.02)

</td><td>
gemSpec_Perf

</td></tr><tr><td>
A_22013-01

</td><td>
Performance - Rohdaten - Spezifika IDP - Operation (Rohdatenerfassung v.02)

</td><td>
gemSpec_Perf

</td></tr><tr><td>
A_22015-01

</td><td>
Performance - Rohdaten - Spezifika IDP - Status (Rohdatenerfassung v.02)

</td><td>
gemSpec_Perf

</td></tr><tr><td>
A_22381

</td><td>
Performance - Rohdaten - Size-Block - Ausnahme (Rohdatenerfassung v.02)

</td><td>
gemSpec_Perf

</td></tr><tr><td>
A_22429

</td><td>
Performance - Rohdaten - Inhalt der Selbstauskunft (Rohdatenerfassung v.02)

</td><td>
gemSpec_Perf

</td></tr><tr><td>
A_17416-01

</td><td>
Schnittstelle Betriebsdatenerfassung Prüfung des TLS-Server-Zertifikats durch
Fach- und zentrale Dienste

</td><td>
gemSpec_SST_LD_BD

</td></tr></table>

### 3.1.2 Herstellererklärung funktionale Eignung

In diesem Abschnitt sind alle funktionalen und nichtfunktionalen Festlegungen an
den technischen Teil des Produkttyps verzeichnet, deren durchgeführte bzw.
geplante Umsetzung und Beachtung der Hersteller bzw. der Anbieter durch eine
Herstellererklärung bestätigt bzw. zusagt.

<table><tr><th>
ID

</th><th>
Bezeichnung

</th><th>
Quelle (Referenz)

</th></tr><tr><td>
GS-A_2162

</td><td>
Kryptographisches Material in Entwicklungs- und Testumgebungen

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_2720

</td><td>
RU/TU: Funktionales Abbild der Produktivumgebung

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_2722-01

</td><td>
TBI integriert die Produkttypen in seine Systemumgebung

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_2724

</td><td>
TBI verantwortet Betrieb RU und TU

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_2726

</td><td>
Bestandteile RU und TU

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_2738

</td><td>
Exklusiver Zugriff organisatorisch

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_2775

</td><td>
Performance in RU

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_2803-01

</td><td>
Nachstellen von PU-Fehlern in der TU

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_2805

</td><td>
Zeitnahe Anpassung von Produktkonfigurationen

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_2806

</td><td>
Zeitnahe Anpassung der Konfiguration der Testumgebung

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_3017

</td><td>
Systemumgebungsmanagement RU sowie TU

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_3361

</td><td>
Dokumentation für den Betrieb in der RU und TU bereitstellen

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_3363

</td><td>
Nutzung von Produkt-Schnittstellen in der TU

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_4191

</td><td>
Keine Echtdaten in RU und TU

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_4192

</td><td>
Dimensionierung TU für PU-Fehlernachstellung

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_4923

</td><td>
Dauerhafte Verfügbarkeit RU und TU

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_4930

</td><td>
Automatisierung von Tests

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_5052

</td><td>
Dauerhafte Verfügbarkeit in der RU

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_6079

</td><td>
Updates von Referenzobjekten

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_6080

</td><td>
Softwarestand von Referenzobjekten

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_6081

</td><td>
Bereitstellung der Referenzobjekte

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_6086

</td><td>
Unterstützung bei Anbindung eines Produktes

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_6088

</td><td>
Unterstützung bei Fehlernachstellung

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_6093

</td><td>
Ausprägung der Referenzobjekte

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_6517-01

</td><td>
Eigenverantwortlicher Test: TBI

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_6518

</td><td>
Eigenverantwortlicher Test: TDI

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_6519

</td><td>
Eigenverantwortlicher Test: Hersteller und Anbieter

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_6521

</td><td>
Zulassungstest: TBI

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_6523

</td><td>
Zulassungstest: Hersteller und Anbieter

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_6524-01

</td><td>
Testdokumentation gemäß Vorlagen

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_6526

</td><td>
Produkttypen: Bereitstellung

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_6527

</td><td>
Testkarten

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_6529

</td><td>
Produkttypen: Mindestumfang der Interoperabilitätsprüfung

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_6532

</td><td>
Zulassung eines neuen Produkts: Aufgaben der TDI

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_6533

</td><td>
Zulassung eines neuen Produkts: Aufgaben der Hersteller und Anbieter

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_6536

</td><td>
Zulassung eines geänderten Produkts: Aufgaben der TDI

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_6537

</td><td>
Zulassung eines geänderten Produkts: Aufgaben der Hersteller und Anbieter

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_6772

</td><td>
Partnerprodukte bei Interoperabilitätstests

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_7330

</td><td>
Tracedaten von echten Außenschnittstellen

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_7331

</td><td>
Bereitstellung von Tracedaten an Außenschnittstelle

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_7333

</td><td>
Parallelbetrieb von Release oder Produkttypversion

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_7334

</td><td>
Risikoabschätzung bezüglich der Interoperabilität

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_7335

</td><td>
Bereitstellung der Testdokumentation

</td><td>
gemKPT_Test

</td></tr><tr><td>
TIP1-A_7358

</td><td>
Qualität des Produktmusters

</td><td>
gemKPT_Test

</td></tr><tr><td>
A_19874-05

</td><td>
Bereitstellung des internen Discovery Documents innerhalb der TI

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_19877-04

</td><td>
Bereitstellung des externen Discovery Documents im Internet

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20319-01

</td><td>
Signatur des "AUTHORIZATION_CODE"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20320-01

</td><td>
Sichere Übertragung des "AUTHORIZATION_CODE"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20329-01

</td><td>
Sichere Übertragung von "ID_TOKEN" und "ACCESS_TOKEN"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20457

</td><td>
Verwendung eindeutiger URI

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20680

</td><td>
Format der Fehlermeldungen

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20681

</td><td>
Nutzung von eindeutigen Error-Codes bei der Erstellung von Fehlermeldungen

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20682-01

</td><td>
Verwendung eines einheitlichen Schemas für die Aufbereitung von Fehlermeldungen

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20683

</td><td>
Formulierung der Fehlermeldungen

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20684

</td><td>
Nutzung einer eindeutigen Beschreibung beim Aufbau von Fehlermeldungen

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20685

</td><td>
Ausgabe der Fehlermeldungen in umgekehrter Reihenfolge des Auftretens

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20686

</td><td>
Erweiterte Nutzung von Schlüsseln

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21404

</td><td>
Bewertung von Typen mobiler Endgeräte durch den IdP-Dienst

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21406

</td><td>
Anforderungen an Transaktionalität der Freischaltung der Einstufung von
Gerätetypen

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21407

</td><td>
Vorhalten von Backup-Daten zur Einstufung von Gerätetypen

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21410

</td><td>
Registrierung des Pairing-Endpunkts und des Authenticator-Moduls am IdP-Dienst

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_22288

</td><td>
Weitere Informationen zu registrierten sektoralen Authenticator-Modulen

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_22326

</td><td>
IDP-Dienst: Setzen des korrekten Issuer Claims

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_17124

</td><td>
TLS-Verbindungen (ECC-Migration)

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
A_17205

</td><td>
Signatur der TSL: Signieren und Prüfen (ECC-Migration)

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
A_17322

</td><td>
TLS-Verbindungen nur zulässige Ciphersuiten und TLS-Versionen (ECC-Migration)

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
A_17775

</td><td>
TLS-Verbindungen Reihenfolge Ciphersuiten (ECC-Migration)

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
A_18986

</td><td>
Fachdienst-interne TLS-Verbindungen

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
GS-A_4367

</td><td>
Zufallszahlengenerator

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
GS-A_4368

</td><td>
Schlüsselerzeugung

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
GS-A_4384

</td><td>
TLS-Verbindungen

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
GS-A_4385

</td><td>
TLS-Verbindungen, Version 1.2

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
GS-A_4387

</td><td>
TLS-Verbindungen, nicht Version 1.0

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
GS-A_5035

</td><td>
Nichtverwendung des SSL-Protokolls

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
GS-A_5339

</td><td>
TLS-Verbindungen, erweiterte Webbrowser-Interoperabilität

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
GS-A_4009

</td><td>
Übertragungstechnologie auf OSI-Schicht LAN

</td><td>
gemSpec_Net

</td></tr><tr><td>
GS-A_4831

</td><td>
Standards für IPv4

</td><td>
gemSpec_Net

</td></tr><tr><td>
GS-A_3695

</td><td>
Grundlegender Aufbau Versionsnummern

</td><td>
gemSpec_OM

</td></tr><tr><td>
GS-A_3696

</td><td>
Zeitpunkt der Erzeugung neuer Versionsnummern

</td><td>
gemSpec_OM

</td></tr><tr><td>
GS-A_3697

</td><td>
Anlass der Erhöhung von Versionsnummern

</td><td>
gemSpec_OM

</td></tr><tr><td>
GS-A_3806

</td><td>
Loglevel in der Referenz- und Testumgebung

</td><td>
gemSpec_OM

</td></tr><tr><td>
GS-A_4541

</td><td>
Nutzung der Produkttypversion zur Kompatibilitätsprüfung

</td><td>
gemSpec_OM

</td></tr><tr><td>
GS-A_4542

</td><td>
Spezifikationsgrundlage für Produkte

</td><td>
gemSpec_OM

</td></tr><tr><td>
GS-A_4864

</td><td>
Logging-Vorgaben nach dem Übergang zum Produktivbetrieb

</td><td>
gemSpec_OM

</td></tr><tr><td>
GS-A_5025

</td><td>
Versionierung von Produkten auf Basis von zentralen Produkttypen der
TI-Plattform und fachanwendungsspezifischen Diensten durch die
Produktidentifikation

</td><td>
gemSpec_OM

</td></tr><tr><td>
GS-A_5038

</td><td>
Festlegungen zur Vergabe einer Produktversion

</td><td>
gemSpec_OM

</td></tr><tr><td>
GS-A_5039

</td><td>
Änderung der Produktversion bei Änderungen der Produkttypversion

</td><td>
gemSpec_OM

</td></tr><tr><td>
GS-A_5054

</td><td>
Versionierung von Produkten durch die Produktidentifikation erweitert um
Klartextnamen

</td><td>
gemSpec_OM

</td></tr><tr><td>
GS-A_4640

</td><td>
Identifizierung/Validierung des TI-Vertrauensankers bei der initialen Einbringung

</td><td>
gemSpec_PKI

</td></tr><tr><td>
A_19718-01

</td><td>
Performance – IdP-Dienst – Verfügbarkeit

</td><td>
gemSpec_Perf

</td></tr><tr><td>
A_21976

</td><td>
Performance - Rohdaten - Konfigurierbarkeit der Lieferintervalle
(Rohdatenerfassung v.02)

</td><td>
gemSpec_Perf

</td></tr><tr><td>
A_21978

</td><td>
Performance - Rohdaten - Trennung der Lieferintervalle (Rohdatenerfassung v.02)

</td><td>
gemSpec_Perf

</td></tr><tr><td>
A_21979

</td><td>
Performance - Rohdaten - Bezug der Lieferverpflichtung (Rohdatenerfassung v.02)

</td><td>
gemSpec_Perf

</td></tr><tr><td>
A_21983-01

</td><td>
Performance - Rohdaten - Message-Block im Fehlerfall - ID (Rohdatenerfassung
v.02)

</td><td>
gemSpec_Perf

</td></tr><tr><td>
A_21984

</td><td>
Performance - Rohdaten - Size-Block (Rohdatenerfassung v.02)

</td><td>
gemSpec_Perf

</td></tr><tr><td>
A_22005

</td><td>
Performance - Rohdaten - Frist für Nachlieferung (Rohdatenerfassung v.02)

</td><td>
gemSpec_Perf

</td></tr><tr><td>
A_22016-01

</td><td>
Performance - Rohdaten - Spezifika IDP - Message (Rohdatenerfassung v.02)

</td><td>
gemSpec_Perf

</td></tr><tr><td>
A_22047

</td><td>
Performance - Rohdaten - Änderung der Konfiguration der Lieferintervalle
(Rohdatenerfassung v.02)

</td><td>
gemSpec_Perf

</td></tr><tr><td>
A_22227

</td><td>
Performance – IDP-Dienst – Bearbeitungszeit unter Last

</td><td>
gemSpec_Perf

</td></tr><tr><td>
A_22500

</td><td>
Performance - Rohdaten - Status-Block (Rohdatenerfassung v.02)

</td><td>
gemSpec_Perf

</td></tr><tr><td>
A_22504

</td><td>
Performance - Rohdaten - Spezifika IDP - Feldtrennzeichen im Useragent
(Rohdatenerfassung v.02)

</td><td>
gemSpec_Perf

</td></tr><tr><td>
A_22513

</td><td>
Performance - Rohdaten - Message-Block im Fehlerfall - JSON (Rohdatenerfassung
v.02)

</td><td>
gemSpec_Perf

</td></tr><tr><td>
A_17733-01

</td><td>
Schnittstelle Betriebsdatenerfassung Datei-Upload

</td><td>
gemSpec_SST_LD_BD

</td></tr></table>

### 3.2 Festlegungen zur sicherheitstechnischen Eignung

### 3.2.1 Herstellererklärung sicherheitstechnische Eignung

Sofern in diesem Abschnitt Festlegungen verzeichnet sind, muss der Hersteller
bzw. der Anbieter deren Umsetzung und Beachtung zum Nachweis der
sicherheitstechnischen Eignung durch eine Herstellererklärung bestätigen bzw.
zusagen.

<table><tr><th>
ID

</th><th>
Bezeichnung

</th><th>
Quelle (Referenz)

</th></tr><tr><td>
A_17178

</td><td>
Produktentwicklung: Basisschutz gegen OWASP Top 10 Risiken

</td><td>
gemSpec_DS_Hersteller

</td></tr><tr><td>
A_17179

</td><td>
Auslieferung aktueller zusätzlicher Softwarekomponenten

</td><td>
gemSpec_DS_Hersteller

</td></tr><tr><td>
A_19163

</td><td>
Rechte der gematik zur sicherheitstechnischen Prüfung des Produktes

</td><td>
gemSpec_DS_Hersteller

</td></tr><tr><td>
A_19164

</td><td>
Mitwirkungspflicht bei Sicherheitsprüfung

</td><td>
gemSpec_DS_Hersteller

</td></tr><tr><td>
A_19165

</td><td>
Auditrechte der gematik zur Prüfung der Herstellerbestätigung

</td><td>
gemSpec_DS_Hersteller

</td></tr><tr><td>
GS-A_4944-01

</td><td>
Produktentwicklung: Behebung von Sicherheitsmängeln

</td><td>
gemSpec_DS_Hersteller

</td></tr><tr><td>
GS-A_4945-01

</td><td>
Produktentwicklung: Qualitätssicherung

</td><td>
gemSpec_DS_Hersteller

</td></tr><tr><td>
GS-A_4946-01

</td><td>
Produktentwicklung: sichere Programmierung

</td><td>
gemSpec_DS_Hersteller

</td></tr><tr><td>
GS-A_4947-01

</td><td>
Produktentwicklung: Schutz der Vertraulichkeit und Integrität

</td><td>
gemSpec_DS_Hersteller

</td></tr><tr><td>
A_19874-05

</td><td>
Bereitstellung des internen Discovery Documents innerhalb der TI

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_19877-04

</td><td>
Bereitstellung des externen Discovery Documents im Internet

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20319-01

</td><td>
Signatur des "AUTHORIZATION_CODE"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20320-01

</td><td>
Sichere Übertragung des "AUTHORIZATION_CODE"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20329-01

</td><td>
Sichere Übertragung von "ID_TOKEN" und "ACCESS_TOKEN"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20680

</td><td>
Format der Fehlermeldungen

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20681

</td><td>
Nutzung von eindeutigen Error-Codes bei der Erstellung von Fehlermeldungen

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20682-01

</td><td>
Verwendung eines einheitlichen Schemas für die Aufbereitung von Fehlermeldungen

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20683

</td><td>
Formulierung der Fehlermeldungen

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20684

</td><td>
Nutzung einer eindeutigen Beschreibung beim Aufbau von Fehlermeldungen

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20685

</td><td>
Ausgabe der Fehlermeldungen in umgekehrter Reihenfolge des Auftretens

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20688

</td><td>
Discovery Document interne und externe Adressierung

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21309

</td><td>
Prüfung der Verwendung des Authorization Codes

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21404

</td><td>
Bewertung von Typen mobiler Endgeräte durch den IdP-Dienst

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_22270

</td><td>
Löschung der Sitzungsdaten zum sektoralen Identity Provider

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_22326

</td><td>
IDP-Dienst: Setzen des korrekten Issuer Claims

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_17205

</td><td>
Signatur der TSL: Signieren und Prüfen (ECC-Migration)

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
A_17322

</td><td>
TLS-Verbindungen nur zulässige Ciphersuiten und TLS-Versionen (ECC-Migration)

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
A_17775

</td><td>
TLS-Verbindungen Reihenfolge Ciphersuiten (ECC-Migration)

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
A_18464

</td><td>
TLS-Verbindungen, nicht Version 1.1

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
A_18467

</td><td>
TLS-Verbindungen, Version 1.3

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
GS-A_4362

</td><td>
X.509-Identitäten für Verschlüsselungszertifikate

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
GS-A_5541

</td><td>
TLS-Verbindungen als TLS-Klient zur Störungsampel oder SM

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
GS-A_5542

</td><td>
TLS-Verbindungen (fatal Alert bei Abbrüchen)

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
GS-A_5580-01

</td><td>
TLS-Klient für betriebsunterstützende Dienste

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
GS-A_5581

</td><td>
"TUC vereinfachte Zertifikatsprüfung“ (Komponenten-PKI)

</td><td>
gemSpec_Krypt

</td></tr></table>

### 3.2.2 Sicherheitsgutachten

Die in diesem Abschnitt verzeichneten Festlegungen sind Gegenstand der Prüfung
der Sicherheitseignung gemäß [gemRL_PruefSichEig]. Das entsprechende
Sicherheitsgutachten ist der gematik vorzulegen.

<table><tr><th>
ID

</th><th>
Bezeichnung

</th><th>
Quelle (Referenz)

</th></tr><tr><td>
A_19147

</td><td>
Sicherheitstestplan

</td><td>
gemSpec_DS_Hersteller

</td></tr><tr><td>
A_19148

</td><td>
Sicherheits- und Datenschutzkonzept

</td><td>
gemSpec_DS_Hersteller

</td></tr><tr><td>
A_19150

</td><td>
Umsetzung Sicherheitstestplan

</td><td>
gemSpec_DS_Hersteller

</td></tr><tr><td>
A_19151

</td><td>
Implementierungsspezifische Sicherheitsanforderungen

</td><td>
gemSpec_DS_Hersteller

</td></tr><tr><td>
A_19152

</td><td>
Verwendung eines sicheren Produktlebenszyklus

</td><td>
gemSpec_DS_Hersteller

</td></tr><tr><td>
A_19153

</td><td>
Sicherheitsrelevanter Softwarearchitektur-Review

</td><td>
gemSpec_DS_Hersteller

</td></tr><tr><td>
A_19154

</td><td>
Durchführung einer Bedrohungsanalyse

</td><td>
gemSpec_DS_Hersteller

</td></tr><tr><td>
A_19155

</td><td>
Durchführung sicherheitsrelevanter Quellcode-Reviews

</td><td>
gemSpec_DS_Hersteller

</td></tr><tr><td>
A_19156

</td><td>
Durchführung automatisierter Sicherheitstests

</td><td>
gemSpec_DS_Hersteller

</td></tr><tr><td>
A_19157

</td><td>
Dokumentierter Plan zur Sicherheitsschulung für Entwickler

</td><td>
gemSpec_DS_Hersteller

</td></tr><tr><td>
A_19158

</td><td>
Sicherheitsschulung für Entwickler

</td><td>
gemSpec_DS_Hersteller

</td></tr><tr><td>
A_19159

</td><td>
Dokumentation des sicheren Produktlebenszyklus

</td><td>
gemSpec_DS_Hersteller

</td></tr><tr><td>
A_19160

</td><td>
Änderungs- und Konfigurationsmanagementprozess

</td><td>
gemSpec_DS_Hersteller

</td></tr><tr><td>
A_19161

</td><td>
Verifizierung der Einhaltung sicherheitstechnische Eignung durch
Datenschutzbeauftragten

</td><td>
gemSpec_DS_Hersteller

</td></tr><tr><td>
A_19162

</td><td>
Informationspflicht bei Veröffentlichung neue Produktversion

</td><td>
gemSpec_DS_Hersteller

</td></tr></table>

### 3.2.3 Produktgutachten

Die in diesem Abschnitt verzeichneten Festlegungen sind Gegenstand der Prüfung
der Sicherheitseignung gemäß [gemRL_PruefSichEig]. Das entsprechende
Produktgutachten ist der gematik vorzulegen.

<table><tr><th>
ID

</th><th>
Bezeichnung

</th><th>
Quelle (Referenz)

</th></tr><tr><td>
A_20313-01

</td><td>
Inhalte des Claims

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20314-01

</td><td>
Maximale Gültigkeitsdauer des "AUTHORIZATION_CODE" und des "CHALLENGE_TOKEN"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20315-01

</td><td>
"AUTHORIZATION_CODE" nach Gültigkeitsende nicht mehr verwenden

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20318

</td><td>
Keine Token für widerrufene Entitäten

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20323

</td><td>
TOKEN-Ausgabe Protokollierung in allen Fällen

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20327-02

</td><td>
Signatur des "ID_TOKEN" und "ACCESS_TOKEN"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20434

</td><td>
Einhaltung der Standards bei der Realisierung des Authorization-Endpunkts

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20440-01

</td><td>
Schematische Prüfung des Consent

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20459

</td><td>
Das Attribut AUTH_TIME muss in allen Token unverändert bleiben

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20462

</td><td>
Maximale Gültigkeitsdauer des "ID_TOKEN"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20463

</td><td>
Maximale Gültigkeitsdauer des "ACCESS_TOKEN"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20464

</td><td>
Token-Endpunkt (Datensparsamkeit)

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20465

</td><td>
Zertifikatsprüfung gegen OCSP-Responder

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20521-02

</td><td>
Inhalt des CHALLENGE_TOKEN an das Authenticator-Modul

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20522

</td><td>
Erstellen einer "SESSION_ID"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20582-01

</td><td>
IdP-Dienst - Berücksichtigung OWASP-Top-10-Risiken

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20591-01

</td><td>
Festlegungen zur Signatur der Discovery Documents

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20691-01

</td><td>
Das Discovery Document ist maximal 24 Stunden alt

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20692-01

</td><td>
Maximale Gültigkeitsdauer eines SSO_TOKEN

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20695-01

</td><td>
Signieren des "SSO_TOKEN"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20696

</td><td>
Verschlüsselung des "SSO_TOKEN"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20697

</td><td>
Zusammenstellung des "AUTHORIZATION_CODE"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20731

</td><td>
Verwendung des Attributes "auth_time"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20947

</td><td>
Entschlüsselung des "SSO_TOKEN"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20948-01

</td><td>
Validierung des "SSO_TOKEN"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20949

</td><td>
Anforderung einer Authentisierung bei negativer Validierung des "SSO_TOKEN"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20950-01

</td><td>
Positive Validierung des "SSO_TOKEN"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_20951-01

</td><td>
Validierung der Signatur und des Zertifikats des CHALLENGE_TOKEN

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21317

</td><td>
Verschlüsselung des "AUTHORIZATION_CODE"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21318

</td><td>
Prüfung des "AUTHORIZATION_CODE“

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21319

</td><td>
Prüfung des "CODE_VERIFIER"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21321

</td><td>
Verschlüsselung von "ACCESS_TOKEN" und "ID_TOKEN"

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21413

</td><td>
Registrierungsfunktion des IdP-Dienstes: Prüfung des Scope

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21419

</td><td>
Registrierungsfunktion des IdP-Dienstes: Anforderung an die Authentifizierung
des Nutzers

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21420

</td><td>
Registrierungsfunktion des IdP-Dienstes: Entschlüsselung der Registrierungsdaten

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21421

</td><td>
Registrierungsfunktion des IdP-Dienstes: Validierung der signierten Pairing-Daten

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21422

</td><td>
Registrierungsfunktion des IdP-Dienstes: Validierung des Zusammenhangs von
ACCESS_TOKEN und Pairing-Daten

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21423

</td><td>
Registrierungsfunktion des IdP-Dienstes: Bewertung des Gerätetyps

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21424

</td><td>
Registrierungsfunktion des IdP-Dienstes: Speicherung der Pairing-Daten

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21425

</td><td>
Registrierungsfunktion des IdP-Dienstes: Validierung des übermittelten
ACCESS_TOKENS

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21426

</td><td>
Registrierungsfunktion des IdP-Dienstes: Nicht-Speicherung des übermittelten
Authentifizierungszertifikats

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21432

</td><td>
Erweiterung des Authorization-Endpunkts: Prüfung der vorliegenden Gerätedaten

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21433

</td><td>
Erweiterung des Authorization-Endpunkts: Validierung des
Authentifizierungszertifikats

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21434

</td><td>
Erweiterung des Authorization-Endpunkts: Auslesen der gespeicherten Pairing-Daten

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21435

</td><td>
Erweiterung des Authorization-Endpunkts: Validierung der mathematischen
Integrität der gespeicherten Pairing-Daten

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21437

</td><td>
Erweiterung des Authorization-Endpunkts: Bewertung der Gültigkeit des
öffentlichen Schlüssels in den Pairing-Daten

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21438

</td><td>
Erweiterung des Authorization-Endpunkts: Validierung der mathematischen
Integrität der signierten Authentication_Data-Struktur

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21439

</td><td>
Erweiterung des Authorization-Endpunkts: Zu unterstützende Algorithmen zur
Prüfung der mathematischen Integrität der signierten
Authentication_Data-Struktur

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21440

</td><td>
Erweiterung des Authorization-Endpunkts: Produktion des Authorization Code und
eines SSO_TOKEN

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21445

</td><td>
Inspektions- und Deregistrierungsfunktion des IdP-Dienstes: Validierung und
Verarbeitung des ACCESS_TOKEN

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21447

</td><td>
Inspektions- und Deregistrierungsfunktion des IdP-Dienstes: Annahme des
Kommandos zur Deaktivierung des Pairings

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21448

</td><td>
Inspektions- und Deregistrierungsfunktion des IdP-Dienstes: Deaktivierung des
identifizierten Pairing-Datensatzes

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21452

</td><td>
Inspektions- und Deregistrierungsfunktion des IdP-Dienstes: Rückgabe der
Pairing-Daten

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21470

</td><td>
Registrierungsfunktion des IdP-Dienstes: Prüfung des Zusammenhangs zwischen
Pairing-Daten und übermittelten Authentifizierungszertifikat

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_22264

</td><td>
Authorization-Request des IDP-Dienstes an sektorale Identity Provider

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_22265

</td><td>
Token Request des IDP-Dienstes an sektorale Identity Provider

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_22266

</td><td>
Authentisierung des IDP-Dienstes gegenüber den sektoralen Identity Providern

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_22268

</td><td>
Prüfung des ID-Token eines sektoralen Identity Provider

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_22284

</td><td>
Festlegungen zur Signatur der Liste der registrierten Authenticator-Module von
sektoralen Identity Providern

</td><td>
gemSpec_IDP_Dienst

</td></tr><tr><td>
A_21442

</td><td>
Inspektions- und Deregistrierungsfunktion des IdP-Dienstes: Authentisierung des
Nutzers

</td><td>
gemSpec_IDP_Frontend

</td></tr><tr><td>
A_17207

</td><td>
Signaturen binärer Daten (ECC-Migration)

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
GS-A_4357

</td><td>
X.509-Identitäten für die Erstellung und Prüfung digitaler
nicht-qualifizierter elektronischer Signaturen

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
GS-A_4359

</td><td>
X.509-Identitäten für die Durchführung einer TLS-Authentifizierung

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
GS-A_4367

</td><td>
Zufallszahlengenerator

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
GS-A_4368

</td><td>
Schlüsselerzeugung

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
GS-A_4389

</td><td>
Symmetrischer Anteil der hybriden Verschlüsselung binärer Daten

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
GS-A_4390

</td><td>
Asymmetrischer Anteil der hybriden Verschlüsselung binärer Daten

</td><td>
gemSpec_Krypt

</td></tr><tr><td>
GS-A_5016

</td><td>
Symmetrische Verschlüsselung binärer Daten

</td><td>
gemSpec_Krypt

</td></tr></table>

### 4 Anhang – Verzeichnisse

### 4.1 Abkürzungen

<table><tr><th>
Kürzel

</th><th>
Erläuterung

</th></tr><tr><td>
ID

</td><td>
Identifikation

</td></tr><tr><td>
CC

</td><td>
Common Criteria

</td></tr><tr><td>
ST

</td><td>
Security Target

</td></tr></table>

### 4.2 Tabellenverzeichnis

- [Tabelle-1] - Dokumente mit Festlegungen zu der Produkttypversion
- [Tabelle-2] - Festlegungen zur funktionalen Eignung "Produkttest/Produktübergreifender Test"
- [Tabelle-3] - Festlegungen zur funktionalen Eignung "Herstellererklärung"
- [Tabelle-4] - Festlegungen zur sicherheitstechnischen Eignung "Herstellererklärung"
- [Tabelle-5] - Festlegungen zur sicherheitstechnischen Eignung "Sicherheitsgutachten"
- [Tabelle-6] - Festlegungen zur sicherheitstechnischen Eignung "Produktgutachten"

### 4.3 Referenzierte Dokumente

Neben den in Kapitel 2 angeführten Dokumenten werden referenziert:

<table><tr><th>
[Quelle]

</th><th>
Herausgeber: Titel, Version

</th></tr><tr><td>
[CC]

</td><td>
Internationaler Standard: Common Criteria for Information Technology Security
Evaluation  
https://www.commoncriteriaportal.org/cc/ 

</td></tr><tr><td>
[gemRL_PruefSichEig]

</td><td>
gematik: Richtlinie zur Prüfung der Sicherheitseignung

</td></tr></table>

**ML-126528 - gemProdT_IDP-Dienst_PTV_2.3.1-0** **[\<=]**





[Historie]:              #historie-produkttypversion-und-produkttypsteckbrief
[Inhaltsverzeichnis]:    #inhaltsverzeichnis
[1]:                     #1-einführung
[1.1]:                   #11-zielsetzung-und-einordnung-des-dokumentes
[1.2]:                   #12-zielgruppe
[1.3]:                   #13-geltungsbereich
[1.4]:                   #14-abgrenzung-des-dokumentes
[1.5]:                   #15-methodik
[2]:                     #2-dokumente
[3]:                     #3-normative-festlegungen
[3.1]:                   #31-festlegungen-zur-funktionalen-eignung
[3.1.1]:                 #311-produkttestproduktübergreifender-test
[3.1.2]:                 #312-herstellererklärung-funktionale-eignung
[3.2]:                   #32-festlegungen-zur-sicherheitstechnischen-eignung
[3.2.1]:                 #321-herstellererklärung-sicherheitstechnische-eignung
[3.2.2]:                 #322-sicherheitsgutachten
[3.2.3]:                 #323-produktgutachten
[4]:                     #4-anhang-–-verzeichnisse
[4.1]:                   #41-abkürzungen
[4.2]:                   #42-tabellenverzeichnis
[4.3]:                   #43-referenzierte-dokumente
[Tbl-001]:               #Tbl-001 (&93834775846072)
[Tbl-002]:               #Tbl-002 (&93834775866512)
[Tabelle-1]:             #Tabelle-1 (&93834778135928)
[Tabelle-2]:             #Tabelle-2 (&93834777759080)
[Tabelle-3]:             #Tabelle-3 (&93834772291848)
[Tabelle-4]:             #Tabelle-4 (&93834783908184)
[Tabelle-5]:             #Tabelle-5 (&93834781580552)
[Tabelle-6]:             #Tabelle-6 (&93834781628376)
[Tbl-009]:               #Tbl-009 (&93834778228984)
[Tbl-010]:               #Tbl-010 (&93834778248376)
[gemSpec_OM]:            ../gemSpec_OM/gemSpec_OM_V1.14.0.html (&93834778140560)
[gemKPT_Test]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html (&93834778143144)
[gemSpec_IDP_Frontend]:  ../gemSpec_IDP_Frontend/gemSpec_IDP_Frontend_V1.3.0.html (&93834778145728)
[gemSpec_DS_Hersteller]: ../gemSpec_DS_Hersteller/gemSpec_DS_Hersteller_V1.3.0.html (&93834778148312)
[gemSpec_Net]:           ../gemSpec_Net/gemSpec_Net_V1.21.0.html (&93834778150896)
[gemSpec_PKI]:           ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html (&93834778153480)
[gemSpec_Perf]:          ../gemSpec_Perf/gemSpec_Perf_V2.17.0.html (&93834778156064)
[gemSpec_IDP_Dienst]:    ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html (&93834778158648)
[gemSpec_SST_LD_BD]:     ../gemSpec_SST_LD_BD/gemSpec_SST_LD_BD_V1.2.0.html (&93834778161232)
[gemSpec_Krypt]:         ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html (&93834778163816)
[A_20313-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20313-01 (&93834777763712)
[A_20314-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20314-01 (&93834777766296)
[A_20315-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20315-01 (&93834777768880)
[A_20318]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20318 (&93834777771464)
[A_20321-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20321-01 (&93834777774048)
[A_20323]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20323 (&93834777776632)
[A_20327-02]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20327-02 (&93834777779216)
[A_20376]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20376 (&93834810793560)
[A_20377]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20377 (&93834810796144)
[A_20434]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20434 (&93834810798728)
[A_20439]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20439 (&93834810801312)
[A_20440-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20440-01 (&93834810803896)
[A_20458-02]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20458-02 (&93834810806480)
[A_20459]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20459 (&93834810809064)
[A_20462]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20462 (&93834810811648)
[A_20463]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20463 (&93834810814232)
[A_20464]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20464 (&93834810816816)
[A_20465]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20465 (&93834810819400)
[A_20521-02]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20521-02 (&93834810821984)
[A_20522]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20522 (&93834810824568)
[A_20523]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20523 (&93834771051600)
[A_20524-04]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20524-04 (&93834771054184)
[A_20588-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20588-01 (&93834771056768)
[A_20589]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20589 (&93834771059352)
[A_20591-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20591-01 (&93834771061936)
[A_20687-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20687-01 (&93834771064520)
[A_20688]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20688 (&93834771067104)
[A_20691-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20691-01 (&93834771069688)
[A_20692-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20692-01 (&93834771072272)
[A_20693-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20693-01 (&93834771074856)
[A_20694]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20694 (&93834771077440)
[A_20695-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20695-01 (&93834771080024)
[A_20696]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20696 (&93834771082608)
[A_20697]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20697 (&93834767980248)
[A_20698]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20698 (&93834767982832)
[A_20699-03]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20699-03 (&93834767985416)
[A_20731]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20731 (&93834767988000)
[A_20732]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20732 (&93834767990584)
[A_20946-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20946-01 (&93834767993168)
[A_20947]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20947 (&93834767995752)
[A_20948-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20948-01 (&93834767998336)
[A_20949]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20949 (&93834768000920)
[A_20950-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20950-01 (&93834768003504)
[A_20951-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20951-01 (&93834768006088)
[A_20952]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20952 (&93834768008672)
[A_21315-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21315-01 (&93834768011288)
[A_21317]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21317 (&93834768013872)
[A_21318]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21318 (&93834768016456)
[A_21319]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21319 (&93834768019040)
[A_21320]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21320 (&93834768021624)
[A_21321]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21321 (&93834768024208)
[A_21330]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21330 (&93834768026792)
[A_21411]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21411 (&93834768029376)
[A_21412]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21412 (&93834768031960)
[A_21413]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21413 (&93834768034544)
[A_21415]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21415 (&93834768037128)
[A_21419]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21419 (&93834768039712)
[A_21420]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21420 (&93834768042296)
[A_21421]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21421 (&93834783608304)
[A_21422]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21422 (&93834783610888)
[A_21423]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21423 (&93834783613472)
[A_21424]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21424 (&93834783616056)
[A_21425]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21425 (&93834783618640)
[A_21427]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21427 (&93834783621224)
[A_21428]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21428 (&93834783623808)
[A_21429-02]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21429-02 (&93834783626392)
[A_21432]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21432 (&93834783628976)
[A_21433]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21433 (&93834783631560)
[A_21434]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21434 (&93834783634144)
[A_21435]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21435 (&93834783636728)
[A_21437]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21437 (&93834783639312)
[A_21438]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21438 (&93834783641992)
[A_21439]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21439 (&93834783644576)
[A_21440]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21440 (&93834783647160)
[A_21441]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21441 (&93834783649744)
[A_21445]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21445 (&93834783652328)
[A_21447]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21447 (&93834783654912)
[A_21448]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21448 (&93834783657496)
[A_21449]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21449 (&93834783660080)
[A_21450]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21450 (&93834783662664)
[A_21452]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21452 (&93834783665248)
[A_21470]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21470 (&93834783667832)
[A_21472]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21472 (&93834783670416)
[A_22262]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_22262 (&93834781663432)
[A_22263]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_22263 (&93834781666016)
[A_22264]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_22264 (&93834781668600)
[A_22265]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_22265 (&93834781671184)
[A_22266]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_22266 (&93834781673768)
[A_22269]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_22269 (&93834781676352)
[A_22271]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_22271 (&93834781678936)
[A_22282]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_22282 (&93834781681520)
[A_22283]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_22283 (&93834781684104)
[A_22286]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_22286 (&93834781686688)
[A_22287]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_22287 (&93834781689272)
[A_22290]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_22290 (&93834781691856)
[A_22328]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_22328 (&93834781694440)
[A_21442]:               ../gemSpec_IDP_Frontend/gemSpec_IDP_Frontend_V1.3.0.html#A_21442 (&93834781697056)
[A_17124]:               ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#A_17124 (&93834781699640)
[A_18464]:               ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#A_18464 (&93834781702224)
[GS-A_4359]:             ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#GS-A_4359 (&93834781704808)
[GS-A_4384]:             ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#GS-A_4384 (&93834781707392)
[GS-A_4385]:             ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#GS-A_4385 (&93834781709976)
[GS-A_4387]:             ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#GS-A_4387 (&93834781712560)
[GS-A_5035]:             ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#GS-A_5035 (&93834781715144)
[GS-A_5322]:             ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#GS-A_5322 (&93834781717728)
[GS-A_5526]:             ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#GS-A_5526 (&93834781720312)
[GS-A_3702]:             ../gemSpec_OM/gemSpec_OM_V1.14.0.html#GS-A_3702 (&93834781722896)
[GS-A_5025]:             ../gemSpec_OM/gemSpec_OM_V1.14.0.html#GS-A_5025 (&93834781725480)
[A_17688]:               ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#A_17688 (&93834781728064)
[A_17690]:               ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#A_17690 (&93834808791720)
[A_17700]:               ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#A_17700 (&93834808794304)
[GS-A_4637]:             ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_4637 (&93834808796888)
[GS-A_4642]:             ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_4642 (&93834808799472)
[GS-A_4643]:             ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_4643 (&93834808802056)
[GS-A_4646]:             ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_4646 (&93834808804640)
[GS-A_4647]:             ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_4647 (&93834808807224)
[GS-A_4648]:             ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_4648 (&93834808809808)
[GS-A_4649]:             ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_4649 (&93834808812392)
[GS-A_4650]:             ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_4650 (&93834808814976)
[GS-A_4651]:             ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_4651 (&93834808817560)
[GS-A_4652-01]:          ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_4652-01 (&93834808820144)
[GS-A_4653-01]:          ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_4653-01 (&93834808822760)
[GS-A_4654-01]:          ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_4654-01 (&93834808825344)
[GS-A_4655-01]:          ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_4655-01 (&93834808827928)
[GS-A_4656]:             ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_4656 (&93834808830512)
[GS-A_4657-03]:          ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_4657-03 (&93834808833096)
[GS-A_4660-02]:          ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_4660-02 (&93834808835680)
[GS-A_4661-01]:          ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_4661-01 (&93834808838264)
[GS-A_4662]:             ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_4662 (&93834808840848)
[GS-A_4663]:             ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_4663 (&93834808843432)
[GS-A_4749-01]:          ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_4749-01 (&93834808846016)
[GS-A_4751]:             ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_4751 (&93834808848600)
[GS-A_4829]:             ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_4829 (&93834808851184)
[GS-A_4898]:             ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_4898 (&93834808853768)
[GS-A_4899]:             ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_4899 (&93834772230480)
[GS-A_4943]:             ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_4943 (&93834772233064)
[GS-A_4957-01]:          ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_4957-01 (&93834772235648)
[GS-A_5077]:             ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_5077 (&93834772238232)
[GS-A_5215]:             ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_5215 (&93834772240816)
[GS-A_5336]:             ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_5336 (&93834772243400)
[A_20243]:               ../gemSpec_Perf/gemSpec_Perf_V2.17.0.html#A_20243 (&93834772245984)
[A_20247]:               ../gemSpec_Perf/gemSpec_Perf_V2.17.0.html#A_20247 (&93834772248568)
[A_21340-01]:            ../gemSpec_Perf/gemSpec_Perf_V2.17.0.html#A_21340-01 (&93834772251152)
[A_21980]:               ../gemSpec_Perf/gemSpec_Perf_V2.17.0.html#A_21980 (&93834772253736)
[A_21981-01]:            ../gemSpec_Perf/gemSpec_Perf_V2.17.0.html#A_21981-01 (&93834772256320)
[A_21982]:               ../gemSpec_Perf/gemSpec_Perf_V2.17.0.html#A_21982 (&93834772258904)
[A_22000]:               ../gemSpec_Perf/gemSpec_Perf_V2.17.0.html#A_22000 (&93834772261488)
[A_22001]:               ../gemSpec_Perf/gemSpec_Perf_V2.17.0.html#A_22001 (&93834772264168)
[A_22002]:               ../gemSpec_Perf/gemSpec_Perf_V2.17.0.html#A_22002 (&93834772266752)
[A_22004]:               ../gemSpec_Perf/gemSpec_Perf_V2.17.0.html#A_22004 (&93834772269336)
[A_22012-01]:            ../gemSpec_Perf/gemSpec_Perf_V2.17.0.html#A_22012-01 (&93834772271920)
[A_22013-01]:            ../gemSpec_Perf/gemSpec_Perf_V2.17.0.html#A_22013-01 (&93834772274504)
[A_22015-01]:            ../gemSpec_Perf/gemSpec_Perf_V2.17.0.html#A_22015-01 (&93834772277088)
[A_22381]:               ../gemSpec_Perf/gemSpec_Perf_V2.17.0.html#A_22381 (&93834772279672)
[A_22429]:               ../gemSpec_Perf/gemSpec_Perf_V2.17.0.html#A_22429 (&93834772282256)
[A_17416-01]:            ../gemSpec_SST_LD_BD/gemSpec_SST_LD_BD_V1.2.0.html#A_17416-01 (&93834772284840)
[GS-A_2162]:             ../gemKPT_Test/gemKPT_Test_V2.8.5.html#GS-A_2162 (&93834777619408)
[TIP1-A_2720]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_2720 (&93834777621992)
[TIP1-A_2722-01]:        ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_2722-01 (&93834777624576)
[TIP1-A_2724]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_2724 (&93834777627160)
[TIP1-A_2726]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_2726 (&93834777629744)
[TIP1-A_2738]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_2738 (&93834777632328)
[TIP1-A_2775]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_2775 (&93834777634912)
[TIP1-A_2803-01]:        ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_2803-01 (&93834777637496)
[TIP1-A_2805]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_2805 (&93834777640080)
[TIP1-A_2806]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_2806 (&93834777642664)
[TIP1-A_3017]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_3017 (&93834777645248)
[TIP1-A_3361]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_3361 (&93834777647832)
[TIP1-A_3363]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_3363 (&93834777650472)
[TIP1-A_4191]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_4191 (&93834777653032)
[TIP1-A_4192]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_4192 (&93834777655616)
[TIP1-A_4923]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_4923 (&93834777658200)
[TIP1-A_4930]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_4930 (&93834777660784)
[TIP1-A_5052]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_5052 (&93834777663368)
[TIP1-A_6079]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_6079 (&93834777665952)
[TIP1-A_6080]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_6080 (&93834777668536)
[TIP1-A_6081]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_6081 (&93834777671120)
[TIP1-A_6086]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_6086 (&93834777673704)
[TIP1-A_6088]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_6088 (&93834777676288)
[TIP1-A_6093]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_6093 (&93834777678872)
[TIP1-A_6517-01]:        ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_6517-01 (&93834777681456)
[TIP1-A_6518]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_6518 (&93834777684136)
[TIP1-A_6519]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_6519 (&93834777686720)
[TIP1-A_6521]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_6521 (&93834777689304)
[TIP1-A_6523]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_6523 (&93834777691888)
[TIP1-A_6524-01]:        ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_6524-01 (&93834777694472)
[TIP1-A_6526]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_6526 (&93834777697056)
[TIP1-A_6527]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_6527 (&93834777699640)
[TIP1-A_6529]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_6529 (&93834777702224)
[TIP1-A_6532]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_6532 (&93834777704808)
[TIP1-A_6533]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_6533 (&93834777707392)
[TIP1-A_6536]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_6536 (&93834777709976)
[TIP1-A_6537]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_6537 (&93834777712560)
[TIP1-A_6772]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_6772 (&93834777715144)
[TIP1-A_7330]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_7330 (&93834781791848)
[TIP1-A_7331]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_7331 (&93834781794432)
[TIP1-A_7333]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_7333 (&93834781797016)
[TIP1-A_7334]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_7334 (&93834781799600)
[TIP1-A_7335]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_7335 (&93834781802184)
[TIP1-A_7358]:           ../gemKPT_Test/gemKPT_Test_V2.8.5.html#TIP1-A_7358 (&93834781804768)
[A_19874-05]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_19874-05 (&93834781807352)
[A_19877-04]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_19877-04 (&93834781809936)
[A_20319-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20319-01 (&93834781812520)
[A_20320-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20320-01 (&93834781815104)
[A_20329-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20329-01 (&93834781817688)
[A_20457]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20457 (&93834781820272)
[A_20680]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20680 (&93834764410544)
[A_20681]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20681 (&93834764413128)
[A_20682-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20682-01 (&93834764415712)
[A_20683]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20683 (&93834764418296)
[A_20684]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20684 (&93834764420880)
[A_20685]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20685 (&93834764423464)
[A_20686]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20686 (&93834764426048)
[A_21404]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21404 (&93834764428632)
[A_21406]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21406 (&93834764431216)
[A_21407]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21407 (&93834764433800)
[A_21410]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21410 (&93834764436384)
[A_22288]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_22288 (&93834764438968)
[A_22326]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_22326 (&93834764441552)
[A_17124]:               ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#A_17124 (&93834764444184)
[A_17205]:               ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#A_17205 (&93834764446768)
[A_17322]:               ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#A_17322 (&93834764449352)
[A_17775]:               ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#A_17775 (&93834764451936)
[A_18986]:               ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#A_18986 (&93834764454520)
[GS-A_4367]:             ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#GS-A_4367 (&93834764457104)
[GS-A_4368]:             ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#GS-A_4368 (&93834764459688)
[GS-A_4384]:             ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#GS-A_4384 (&93834764462272)
[GS-A_4385]:             ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#GS-A_4385 (&93834764464856)
[GS-A_4387]:             ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#GS-A_4387 (&93834764467440)
[GS-A_5035]:             ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#GS-A_5035 (&93834764470024)
[GS-A_5339]:             ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#GS-A_5339 (&93834764472608)
[GS-A_4009]:             ../gemSpec_Net/gemSpec_Net_V1.21.0.html#GS-A_4009 (&93834764475192)
[GS-A_4831]:             ../gemSpec_Net/gemSpec_Net_V1.21.0.html#GS-A_4831 (&93834764477864)
[GS-A_3695]:             ../gemSpec_OM/gemSpec_OM_V1.14.0.html#GS-A_3695 (&93834764480448)
[GS-A_3696]:             ../gemSpec_OM/gemSpec_OM_V1.14.0.html#GS-A_3696 (&93834764483032)
[GS-A_3697]:             ../gemSpec_OM/gemSpec_OM_V1.14.0.html#GS-A_3697 (&93834764485616)
[GS-A_3806]:             ../gemSpec_OM/gemSpec_OM_V1.14.0.html#GS-A_3806 (&93834764488200)
[GS-A_4541]:             ../gemSpec_OM/gemSpec_OM_V1.14.0.html#GS-A_4541 (&93834764490784)
[GS-A_4542]:             ../gemSpec_OM/gemSpec_OM_V1.14.0.html#GS-A_4542 (&93834764493368)
[GS-A_4864]:             ../gemSpec_OM/gemSpec_OM_V1.14.0.html#GS-A_4864 (&93834764495952)
[GS-A_5025]:             ../gemSpec_OM/gemSpec_OM_V1.14.0.html#GS-A_5025 (&93834764498536)
[GS-A_5038]:             ../gemSpec_OM/gemSpec_OM_V1.14.0.html#GS-A_5038 (&93834764501120)
[GS-A_5039]:             ../gemSpec_OM/gemSpec_OM_V1.14.0.html#GS-A_5039 (&93834764503704)
[GS-A_5054]:             ../gemSpec_OM/gemSpec_OM_V1.14.0.html#GS-A_5054 (&93834764506288)
[GS-A_4640]:             ../gemSpec_PKI/gemSpec_PKI_V2.11.1.html#GS-A_4640 (&93834783863872)
[A_19718-01]:            ../gemSpec_Perf/gemSpec_Perf_V2.17.0.html#A_19718-01 (&93834783866456)
[A_21976]:               ../gemSpec_Perf/gemSpec_Perf_V2.17.0.html#A_21976 (&93834783869040)
[A_21978]:               ../gemSpec_Perf/gemSpec_Perf_V2.17.0.html#A_21978 (&93834783871624)
[A_21979]:               ../gemSpec_Perf/gemSpec_Perf_V2.17.0.html#A_21979 (&93834783874208)
[A_21983-01]:            ../gemSpec_Perf/gemSpec_Perf_V2.17.0.html#A_21983-01 (&93834783876792)
[A_21984]:               ../gemSpec_Perf/gemSpec_Perf_V2.17.0.html#A_21984 (&93834783879376)
[A_22005]:               ../gemSpec_Perf/gemSpec_Perf_V2.17.0.html#A_22005 (&93834783881960)
[A_22016-01]:            ../gemSpec_Perf/gemSpec_Perf_V2.17.0.html#A_22016-01 (&93834783884544)
[A_22047]:               ../gemSpec_Perf/gemSpec_Perf_V2.17.0.html#A_22047 (&93834783887128)
[A_22227]:               ../gemSpec_Perf/gemSpec_Perf_V2.17.0.html#A_22227 (&93834783889712)
[A_22500]:               ../gemSpec_Perf/gemSpec_Perf_V2.17.0.html#A_22500 (&93834783892296)
[A_22504]:               ../gemSpec_Perf/gemSpec_Perf_V2.17.0.html#A_22504 (&93834783894880)
[A_22513]:               ../gemSpec_Perf/gemSpec_Perf_V2.17.0.html#A_22513 (&93834783897512)
[A_17733-01]:            ../gemSpec_SST_LD_BD/gemSpec_SST_LD_BD_V1.2.0.html#A_17733-01 (&93834783900096)
[A_17178]:               ../gemSpec_DS_Hersteller/gemSpec_DS_Hersteller_V1.3.0.html#A_17178 (&93834783912816)
[A_17179]:               ../gemSpec_DS_Hersteller/gemSpec_DS_Hersteller_V1.3.0.html#A_17179 (&93834783915400)
[A_19163]:               ../gemSpec_DS_Hersteller/gemSpec_DS_Hersteller_V1.3.0.html#A_19163 (&93834783917984)
[A_19164]:               ../gemSpec_DS_Hersteller/gemSpec_DS_Hersteller_V1.3.0.html#A_19164 (&93834783920568)
[A_19165]:               ../gemSpec_DS_Hersteller/gemSpec_DS_Hersteller_V1.3.0.html#A_19165 (&93834783923152)
[GS-A_4944-01]:          ../gemSpec_DS_Hersteller/gemSpec_DS_Hersteller_V1.3.0.html#GS-A_4944-01 (&93834783925736)
[GS-A_4945-01]:          ../gemSpec_DS_Hersteller/gemSpec_DS_Hersteller_V1.3.0.html#GS-A_4945-01 (&93834783928320)
[GS-A_4946-01]:          ../gemSpec_DS_Hersteller/gemSpec_DS_Hersteller_V1.3.0.html#GS-A_4946-01 (&93834783930920)
[GS-A_4947-01]:          ../gemSpec_DS_Hersteller/gemSpec_DS_Hersteller_V1.3.0.html#GS-A_4947-01 (&93834783933504)
[A_19874-05]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_19874-05 (&93834783936088)
[A_19877-04]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_19877-04 (&93834783938672)
[A_20319-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20319-01 (&93834783941256)
[A_20320-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20320-01 (&93834783943840)
[A_20329-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20329-01 (&93834783946424)
[A_20680]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20680 (&93834783949008)
[A_20681]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20681 (&93834783951592)
[A_20682-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20682-01 (&93834783954176)
[A_20683]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20683 (&93834783956760)
[A_20684]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20684 (&93834783959344)
[A_20685]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20685 (&93834783961928)
[A_20688]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20688 (&93834781537328)
[A_21309]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21309 (&93834781539912)
[A_21404]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21404 (&93834781542496)
[A_22270]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_22270 (&93834781545080)
[A_22326]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_22326 (&93834781547664)
[A_17205]:               ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#A_17205 (&93834781550248)
[A_17322]:               ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#A_17322 (&93834781552832)
[A_17775]:               ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#A_17775 (&93834781555416)
[A_18464]:               ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#A_18464 (&93834781558000)
[A_18467]:               ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#A_18467 (&93834781560584)
[GS-A_4362]:             ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#GS-A_4362 (&93834781563168)
[GS-A_5541]:             ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#GS-A_5541 (&93834781565752)
[GS-A_5542]:             ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#GS-A_5542 (&93834781568376)
[GS-A_5580-01]:          ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#GS-A_5580-01 (&93834781570960)
[GS-A_5581]:             ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#GS-A_5581 (&93834781573544)
[A_19147]:               ../gemSpec_DS_Hersteller/gemSpec_DS_Hersteller_V1.3.0.html#A_19147 (&93834781585184)
[A_19148]:               ../gemSpec_DS_Hersteller/gemSpec_DS_Hersteller_V1.3.0.html#A_19148 (&93834781587768)
[A_19150]:               ../gemSpec_DS_Hersteller/gemSpec_DS_Hersteller_V1.3.0.html#A_19150 (&93834781590352)
[A_19151]:               ../gemSpec_DS_Hersteller/gemSpec_DS_Hersteller_V1.3.0.html#A_19151 (&93834781592936)
[A_19152]:               ../gemSpec_DS_Hersteller/gemSpec_DS_Hersteller_V1.3.0.html#A_19152 (&93834781595520)
[A_19153]:               ../gemSpec_DS_Hersteller/gemSpec_DS_Hersteller_V1.3.0.html#A_19153 (&93834781598104)
[A_19154]:               ../gemSpec_DS_Hersteller/gemSpec_DS_Hersteller_V1.3.0.html#A_19154 (&93834781600696)
[A_19155]:               ../gemSpec_DS_Hersteller/gemSpec_DS_Hersteller_V1.3.0.html#A_19155 (&93834781603280)
[A_19156]:               ../gemSpec_DS_Hersteller/gemSpec_DS_Hersteller_V1.3.0.html#A_19156 (&93834781605864)
[A_19157]:               ../gemSpec_DS_Hersteller/gemSpec_DS_Hersteller_V1.3.0.html#A_19157 (&93834781608448)
[A_19158]:               ../gemSpec_DS_Hersteller/gemSpec_DS_Hersteller_V1.3.0.html#A_19158 (&93834781611032)
[A_19159]:               ../gemSpec_DS_Hersteller/gemSpec_DS_Hersteller_V1.3.0.html#A_19159 (&93834781613616)
[A_19160]:               ../gemSpec_DS_Hersteller/gemSpec_DS_Hersteller_V1.3.0.html#A_19160 (&93834781616200)
[A_19161]:               ../gemSpec_DS_Hersteller/gemSpec_DS_Hersteller_V1.3.0.html#A_19161 (&93834781618784)
[A_19162]:               ../gemSpec_DS_Hersteller/gemSpec_DS_Hersteller_V1.3.0.html#A_19162 (&93834781621368)
[A_20313-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20313-01 (&93834781633008)
[A_20314-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20314-01 (&93834783470000)
[A_20315-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20315-01 (&93834783472584)
[A_20318]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20318 (&93834783475168)
[A_20323]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20323 (&93834783477752)
[A_20327-02]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20327-02 (&93834783480336)
[A_20434]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20434 (&93834783482920)
[A_20440-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20440-01 (&93834783485504)
[A_20459]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20459 (&93834783488088)
[A_20462]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20462 (&93834783490672)
[A_20463]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20463 (&93834783493256)
[A_20464]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20464 (&93834783495840)
[A_20465]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20465 (&93834783498424)
[A_20521-02]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20521-02 (&93834783550216)
[A_20522]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20522 (&93834783552800)
[A_20582-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20582-01 (&93834783555384)
[A_20591-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20591-01 (&93834783557968)
[A_20691-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20691-01 (&93834783560552)
[A_20692-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20692-01 (&93834783563136)
[A_20695-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20695-01 (&93834783565720)
[A_20696]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20696 (&93834783568304)
[A_20697]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20697 (&93834783570888)
[A_20731]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20731 (&93834783573472)
[A_20947]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20947 (&93834783576056)
[A_20948-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20948-01 (&93834783578640)
[A_20949]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20949 (&93834783581224)
[A_20950-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20950-01 (&93834785694624)
[A_20951-01]:            ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_20951-01 (&93834785697208)
[A_21317]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21317 (&93834785699792)
[A_21318]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21318 (&93834785702376)
[A_21319]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21319 (&93834785704960)
[A_21321]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21321 (&93834785707544)
[A_21413]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21413 (&93834785710128)
[A_21419]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21419 (&93834785712712)
[A_21420]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21420 (&93834785715296)
[A_21421]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21421 (&93834785717880)
[A_21422]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21422 (&93834785720464)
[A_21423]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21423 (&93834785723048)
[A_21424]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21424 (&93834785725632)
[A_21425]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21425 (&93834785728304)
[A_21426]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21426 (&93834785730888)
[A_21432]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21432 (&93834785733472)
[A_21433]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21433 (&93834785736056)
[A_21434]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21434 (&93834785738640)
[A_21435]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21435 (&93834785741224)
[A_21437]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21437 (&93834785743808)
[A_21438]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21438 (&93834785746392)
[A_21439]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21439 (&93834785748976)
[A_21440]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21440 (&93834785751560)
[A_21445]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21445 (&93834785754144)
[A_21447]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21447 (&93834785756728)
[A_21448]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21448 (&93834785759352)
[A_21452]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21452 (&93834785761936)
[A_21470]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_21470 (&93834785764520)
[A_22264]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_22264 (&93834785767104)
[A_22265]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_22265 (&93834785769688)
[A_22266]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_22266 (&93834785772272)
[A_22268]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_22268 (&93834785774856)
[A_22284]:               ../gemSpec_IDP_Dienst/gemSpec_IDP_Dienst_V1.4.0.html#A_22284 (&93834785777440)
[A_21442]:               ../gemSpec_IDP_Frontend/gemSpec_IDP_Frontend_V1.3.0.html#A_21442 (&93834785780024)
[A_17207]:               ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#A_17207 (&93834785782608)
[GS-A_4357]:             ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#GS-A_4357 (&93834785785192)
[GS-A_4359]:             ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#GS-A_4359 (&93834785787776)
[GS-A_4367]:             ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#GS-A_4367 (&93834785790360)
[GS-A_4368]:             ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#GS-A_4368 (&93834778216080)
[GS-A_4389]:             ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#GS-A_4389 (&93834778218664)
[GS-A_4390]:             ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#GS-A_4390 (&93834778221248)
[GS-A_5016]:             ../gemSpec_Krypt/gemSpec_Krypt_V2.21.0.html#GS-A_5016 (&93834778223832)
