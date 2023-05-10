
Elektronische Gesundheitskarte und Telematikinfrastruktur

### Spezifikation Autorisierung ePA<br>Abbildung 1: Anwendungsfälle der Schlüsselverwaltung nach Umgebung

- Klassifizierung: öffentlich
- Referenzierung: gemSpec_Autorisierung
- Revision: 588744
- Stand: 11.04.2022
- Status: freigegeben
- Version: 1.9.2

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
initiale Erstellung des Dokuments

</td><td>
gematik

</td></tr><tr><td>
1.1.0

</td><td>
15.05.19

</td><td>
Einarbeitung Änderungsliste P18.1

</td><td>
gematik

</td></tr><tr><td>
1.2.0

</td><td>
28.06.19

</td><td>
Einarbeitung Änderungsliste P19.1

</td><td>
gematik

</td></tr><tr><td>
 1.3.0

</td><td>
02.10.19

</td><td>
Einarbeitung Änderungsliste P20.1/2

</td><td>
gematik

</td></tr><tr><td>
1.4.0

</td><td>
02.03.20

</td><td>
Einarbeitung Änderungsliste P21.1

</td><td>
gematik

</td></tr><tr><td>
1.4.1

</td><td>
26.06.20

</td><td>
Einarbeitung Änderungsliste P21.3

</td><td>
gematik

</td></tr><tr><td>
1.5.0

</td><td>
30.06.20

</td><td>
Anpassungen gemäß Änderungsliste P22.1 und Scope-Themen aus Systemdesign
R4.0.0, Einarbeitung offener Punkte

</td><td>
gematik

</td></tr><tr><td>
1.6.0

</td><td>
12.10.20

</td><td>
Einarbeitung der Scope-Themen aus R4.0.1

</td><td>
gematik

</td></tr><tr><td>
1.7.0

</td><td>
19.02.21

</td><td>
Einarbeitung Änderungsliste P22.5

</td><td>
gematik

</td></tr><tr><td>
1.8.0

</td><td>
02.06.21

</td><td>
Einarbeitung Änderungsliste ePA_Maintenance_21.1

</td><td>
gematik

</td></tr><tr><td>
1.8.1

</td><td>
09.07.21

</td><td>
Einarbeitung Anpassung IOP-WS (ePA_Maintenance_21.2) 

</td><td>
gematik

</td></tr><tr><td>
1.8.2

</td><td>
30.09.21

</td><td>
Einarbeitung ePA_Maintenance_21.3 und red. Anpassung (Pfad auf github)

</td><td>
gematik

</td></tr><tr><td>
1.9.0

</td><td>
31.01.22

</td><td>
Einarbeitung ePA_Maintenance_21.4 und ePA_Maintenance_21.5

</td><td>
gematik

</td></tr><tr><td>
1.9.1

</td><td>
31.03.22

</td><td>
Einarbeitung ePA_Maintenance_22.1

</td><td>
gematik

</td></tr><tr><td>
1.9.2

</td><td>
11.04.22

</td><td>
Einarbeitung Kommentierung 

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
  - [3.1] Akteure und Rollen
  - [3.2] Nachbarsysteme
  - [3.3] Tokenbasierte Autorisierung
- [4] Zerlegung der Komponente Autorisierung
- [5] Übergreifende Festlegungen
  - [5.1] Datenschutz und Datensicherheit
  - [5.2] Verwendete Standards
  - [5.3] Protokollierung
  - [5.4] Fehlerbehandlung in Schnittstellenoperationen
  - [5.5] Nicht-Funktionale Anforderungen
    - [5.5.1] Skalierbarkeit
    - [5.5.2] Performance
    - [5.5.3] Mengengerüst
- [6] Funktionsmerkmale
  - [6.1] Übergreifende Festlegungen
  - [6.2] Schnittstellen der Komponente Autorisierung
    - [6.2.1] Schnittstelle I_Authorization
      - [6.2.1.1] Operationsdefinition I_Authorization::getAuthorizationKey
      - [6.2.1.2] Umsetzung I_Authorization::getAuthorizationKey
    - [6.2.2] Schnittstelle I_Authorization_Insurant
      - [6.2.2.1] Operationsdefinition I_Authorization_Insurant::getAuthorizationKey
      - [6.2.2.2] Umsetzung I_Authorization_Insurant::getAuthorizationKey
    - [6.2.3] Schnittstelle I_Authorization_Management
      - [6.2.3.1] Operationsdefinition I_Authorization_Management::putAuthorizationKey
      - [6.2.3.2] Umsetzung I_Authorization_Management::putAuthorizationKey
      - [6.2.3.3] Operationsdefinition I_Authorization_Management::checkRecordExists
      - [6.2.3.4] Umsetzung I_Authorization_Management::checkRecordExists
      - [6.2.3.5] Operationsdefinition I_Authorization_Management::getAuthorizationList
      - [6.2.3.6] Umsetzung I_Authorization_Management::getAuthorizationList
      - [6.2.3.7] Operationsdefinition I_Authorization_Management::getAuthorizationState
      - [6.2.3.8] Umsetzung I_Authorization_Management::getAuthorizationState
    - [6.2.4] Schnittstelle I_Authorization_Management_Insurant
      - [6.2.4.1] Operationsdefinition I_Authorization_Management_Insurant::putAuthorizationKey
      - [6.2.4.2] Umsetzung I_Authorization_Management_Insurant::putAuthorizationKey
      - [6.2.4.3] Operationsdefinition I_Authorization_Management_Insurant::deleteAuthorizationKey
      - [6.2.4.4] Umsetzung I_Authorization_Management_Insurant::deleteAuthorizationKey
      - [6.2.4.5] Operationsdefinition I_Authorization_Management_Insurant::replaceAuthorizationKey
      - [6.2.4.6] Umsetzung I_Authorization_Management_Insurant::replaceAuthorizationKey
      - [6.2.4.7] Operationsdefinition I_Authorization_Management_Insurant::getAuditEvents
      - [6.2.4.8] Umsetzung I_Authorization_Management_Insurant::getAuditEvents
      - [6.2.4.9] Operationsdefinition I_Authorization_Management_Insurant::getSignedAuditEvents
      - [6.2.4.10] Umsetzung I_Authorization_Management_Insurant::getSignedAuditEvents
      - [6.2.4.11] Operationsdefinition I_Authorization_Management_Insurant::putNotificationInfo
      - [6.2.4.12] Umsetzung I_Authorization_Management_Insurant::putNotificationInfo
      - [6.2.4.13] Operationsdefinition I_Authorization_Management_Insurant::getNotificationInfo
      - [6.2.4.14] Umsetzung I_Authorization_Management_Insurant::getNotificationInfo
      - [6.2.4.15] Operationsdefinition I_Authorization_Management_Insurant::getKtrTelematikID
      - [6.2.4.16] Umsetzung I_Authorization_Management_Insurant::getKtrTelematikID
      - [6.2.4.17] Operationsdefinition I_Authorization_Management_Insurant::getAuthorizationList
      - [6.2.4.18] Umsetzung I_Authorization_Management_Insurant::getAuthorizationList
      - [6.2.4.19] Operationsdefinition I_Authorization_Management_Insurant::startKeyChange
      - [6.2.4.20] Umsetzung I_Authorization_Management_Insurant::startKeyChange
      - [6.2.4.21] Operationsdefinition I_Authorization_Management_Insurant::putForReplacement
      - [6.2.4.22] Umsetzung I_Authorization_Management_Insurant::putForReplacement
      - [6.2.4.23] Operationsdefinition I_Authorization_Management_Insurant::finishKeyChange
      - [6.2.4.24] Umsetzung I_Authorization_Management_Insurant::finishKeyChange
      - [6.2.4.25] Fehlerbehandlung I_Authorization_Management_Insurant
  - [6.3] Berechtigungstypen der Autorisierung
  - [6.4] Hardware-Merkmal der Komponente Autorisierung
  - [6.5] Geräteverwaltung
    - [6.5.1] Freischaltprozess neuer Geräte
    - [6.5.2] Geräteadministration
  - [6.6] Freischaltprozess Vertretereinrichtung
- [7] Informationsmodell
  - [7.1] Namensräume
  - [7.2] SAML-Profil und Tokeninhalte
- [8] Verteilungssicht
- [9] Anhang A – Verzeichnisse
  - [9.1] Abkürzungen
  - [9.2] Glossar
  - [9.3] Abbildungsverzeichnis
  - [9.4] Tabellenverzeichnis
  - [9.5] Referenzierte Dokumente
    - [9.5.1] Dokumente der gematik
    - [9.5.2] Weitere Dokumente

### 1 Einordnung des Dokumentes

### 1.1 Zielsetzung

Das vorliegende Dokument spezifiziert die Anforderungen an die Komponente
"Autorisierung" des Produkttyps ePA-Aktensystem. Die Komponente Autorisierung
ist verantwortlich für die zentrale Verwaltung des empfängerbezogenen
verschlüsselten Schlüsselmaterials.

### 1.2 Zielgruppe

Das Dokument richtet sich an Hersteller und Anbieter der Komponente
"Autorisierung" für die Nutzung in einem ePA-Aktensystem sowie an Hersteller
und Anbieter von Produkttypen ePA, die Schnittstellen der Komponente
"Autorisierung" nutzen.

### 1.3 Geltungsbereich

Dieses Dokument enthält normative Festlegungen zur Telematikinfrastruktur des
deutschen Gesundheitswesens. Der Gültigkeitszeitraum der vorliegenden Version
und deren Anwendung in Zulassungs- oder Abnahmeverfahren wird durch die gematik
GmbH in gesonderten Dokumenten (z.B. Dokumentenlandkarte, Produkttypsteckbrief,
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

### 1.4 Abgrenzungen

Spezifiziert werden in dem Dokument die von der Komponente bereitgestellten
(angebotenen) Schnittstellen. Benutzte Schnittstellen werden hingegen in der
Spezifikation desjenigen Produkttypen beschrieben, der diese Schnittstelle
bereitstellt. Auf die entsprechenden Dokumente wird referenziert (siehe auch
Anhang A5).

Die vollständige Anforderungslage für den Produkttyp ergibt sich aus weiteren
Konzept- und Spezifikationsdokumenten. Diese sind in dem Produkttypsteckbrief
des Produkttyps \<ePA-Aktensystem\> verzeichnet.

Nicht Bestandteil des vorliegenden Dokumentes sind die Festlegungen zum
Themenbereich Betrieb.

### 1.5 Methodik

Anforderungen als Ausdruck normativer Festlegungen werden durch eine eindeutige
ID sowie die dem RFC 2119 [RFC2119] entsprechenden, in Großbuchstaben
geschriebenen deutschen Schlüsselworte MUSS, DARF NICHT, SOLL, SOLL NICHT,
KANN gekennzeichnet.

Da in dem Beispielsatz „Eine leere Liste DARF NICHT ein Element besitzen.“
die Phrase „DARF NICHT“ semantisch irreführend wäre (wenn nicht ein, dann
vielleicht zwei?), wird in diesem Dokument stattdessen „Eine leere Liste DARF
KEIN Element besitzen.“ verwendet. Die Schlüsselworte werden außerdem um
Pronomen in Großbuchstaben ergänzt, wenn dies den Sprachfluss verbessert oder
die Semantik verdeutlicht.

Anforderungen werden im Dokument wie folgt dargestellt:\<AFO-ID\> - \<Titel der
Afo\>Text / Beschreibung [\<=]

Dabei umfasst die Anforderung sämtliche zwischen Afo-ID und Textmarke [\<=]
angeführten Inhalte.

### 2 Systemüberblick

Der Autorisierungsdienst ePA ist eine Komponente des Produkttyps
ePA-Aktensystem. Die Systemzerlegung der Fachanwendung ePA in Komponenten und
Produkttypen sowie die Verteilung der Komponenten auf Produkttypen der
Telematikinfrastruktur (TI) ist in [gemSysL_ePA#2.1] und in [gemSysL_ePA#4.1]
definiert.

Die Komponente Autorisierungsdienst ePA verwaltet das empfängerverschlüsselte
Schlüsselmaterial der Nutzer eines Aktenkontos eines Versicherten
(kryptografische Autorisierung). Mit dem Vorhandensein einer kryptografischen
Berechtigung ist ein Nutzer in der Lage, auf den symmetrischen Aktenschlüssel
sowie den Kontextschlüssel zuzugreifen. Um dieses Schlüsselmaterial für den
Zugriff auf medizinische Daten und Dokumente eines Versicherten zu nutzen,
benötigt ein Nutzer ggfs. zusätzlich Berechtigungen auf Objektebene in
anderen Komponente und Produkttypen, die die Daten und Dokumente des
Versicherten verwalten.

### 3 Systemkontext

Der folgende Abschnitt setzt die Komponente Autorisierung in den Systemkontext
der Fachanwendung ePA.

### 3.1 Akteure und Rollen

Die Komponente Autorisierung wird als Provider technischer Schnittstellen von
weiteren technischen Komponenten und Produkttypen der Fachanwendung ePA
aufgerufen. Diese weiteren Komponenten und Produkttypen nutzen die
Schnittstellen der Komponente Autorisierung im Zusammenhang von fachlichen
Anwendungsfällen der Nutzer der Fachanwendung ePA.

Die Nutzer sind dabei gesetzlich Versicherte, Leistungserbringerinstitutionen
und Kostenträger, welche durch ihre jeweilige Karte der TI repräsentiert
werden. Über eine kartenbasierte Authentifizierungsbestätigung authentisieren
sie sich gegenüber der Komponente Autorisierung. Ein Spezialfall des
gesetzlichen Versicherten ist der berechtigte Vertreter.

Für die oben genannten Nutzer verwaltet die Komponente Autorisierung
empfängerbezogen verschlüsseltes Schlüsselmaterial

 ---> UL

Die Komponente Autorisierung wird je nach Erfordernis zur Laufzeit von einem
Administrator administriert. Gemäß der Festlegungen des Rollenmodells
"Personenkreise der Telematikinfrastruktur" in [gemKPT_Arch_TIP] haben
Anbieter, Betreiber und Administratoren keinen Zugriff auf medizinische Daten
der Anwendungen des §291a SGB V [SGB V]. Die Komponente Autorisierung
speichert personenbezogene Informationen, jedoch keine medizinischen Daten im
Sinne des § 291a SGB V [SGB V].

Das folgende Bild gibt eine Übersicht der durch die Schnittstellen realisierten
Anwendungsfälle zur Schlüsselverwaltung der Komponente Autorisierung. Zur
Vereinfachung sind die Anwendungsfälle der Protokollierung und
Geräteverwaltung nicht dargestellt.

![Abbildung-1][Abbildung-1]

Die Berechtigung für Anwendungsfälle der Schlüsselverwaltung durch einen
Nutzer unterscheidet sich nach Umgebung. Dem Versicherten stehen in der
Umgebung der Leistungserbringer keine Anwendungsfälle zum Löschen bestehender
Berechtigungen zur Verfügung, da ihm dort kein geeignetes Benutzerinterface
zur Verfügung steht. Ein Ersetzen des Schlüsselmaterials erfolgt bei Vergabe
einer Änderungsberechtigung für eine Leistungserbringerinstitution, wenn
bspw. die Gültigkeitsdauer der Berechtigung angepasst wird.

Eine Leistungserbringerinstitution kann auf das für sie hinterlegte
Schlüsselmaterial lesend zugreifen. Analog kann ein  Kostenträger nur auf
das für ihn hinterlegte Schlüsselmaterial lesend zugreifen.

In der Umgebung des Versicherten hat ein Versicherter vollen Zugriff auf das
hinterlegte Schlüsselmaterial mit folgender Ausnahme - ein Versicherter darf
das eigene Schlüsselmaterial für die eGK des Versicherten nicht löschen.
Ebenso darf der Vertreter nicht das Schlüsselmaterial des Versicherten
löschen und auch nicht Schlüsselmaterial für andere eGK-Inhaber hinzufügen
(kein Einrichten weiterer Vertretungen durch einen Vertreter).

Ergänzende Informationen zu Bezeichnern und Datentypen finden sich im
Informationsmodell in Abschnitt 7. 

<table><tr><th>
Assoziation

</th><th>
Actor

</th><th>
Regel zur Identifikation des Nutzers*

</th></tr><tr><td>
A

</td><td rowspan="3">
Versicherter  
   
 

</td><td rowspan="3">
subject-id == OwnerKVNR == ActorID  
   
 

</td></tr><tr><td>
B

</td></tr><tr><td>
C

</td></tr><tr><td>
D

</td><td>
Leistungserbringer-institution

</td><td>
subject-id == ActorID != OwnerKVNR (für HBA – erst in Folgestufe) 

organization-id == ActorID != OwnerKVNR (für SMC-B)

</td></tr><tr><td>
E

</td><td>
Versicherter

</td><td>
subject-id == OwnerKVNR

</td></tr><tr><td>
F

</td><td>
Vertreter

</td><td>
subject-id == ActorID != OwnerKVNR (beim Verwalten des Vertretungsschlüssels) 

subject-id != ActorID != OwnerKVNR (beim Verwalten aller übrigen Schlüssel)

</td></tr><tr><td>
G

</td><td>
Kostenträger

</td><td>
organization-id == ActorID != OwnerKVNR (für SMC-B KTR)

</td></tr></table>

*subject-id/organization-id ist Teil der Authentication- bzw.
AuthorizationAssertion (als Behauptung gemäß
[gemSpec_TBAuth#TAB_TBAuth_02_1/2]),OwnerKVNRist ein Attribut der KeyChain
(vgl. Kap. 7 Informationsmodell), der mehrere AuthorizationKeys untergeordnet
werden,ActorIDmeint hier den Teil des AuthorizationKeys der dessen Besitzer
identifiziert, (einige Schnittstellenoperationen verfügen über einen
ParameterActorID, dieser ist hier jedoch nicht Gegenstand der Betrachtung)

Der Versicherte wird beim Einsatz der eGK in der Umgebung der Leistungserbringer
(Anwendungsfälle A und B) und in Anwendungsfällen aus der Umgebung des
Versicherten (Anwendungsfälle zu E) anhand der KVNR als subject-id eines
AuthenticationTokens erkannt. Diese stimmt gleichzeitig mit der OwnerKVNR des
Eigentümers der Akte überein. Im Regelfall existiert für den Versicherten
ein AuthorizationKey mit der KVNR des Versicherten als ActorID. Im Zustand der
Kontoeröffnung und bei Anbieterwechsel wird das Schlüsselmaterial für den
Versicherten extern erzeugt. Ein Nicht-Vorhandensein eines AuthorizationKeys
für den Versicherten wird nicht als Fehler behandelt, sondern als
Autorisierung im Zusammenhang mit Anwendungsfällen der Kontoverwaltung. 

Eine Leistungserbringerinstitution wird bei Einsatz einer SMC-B
(Anwendungsfälle C und D) anhand ihrer Telematik-ID aus der 
organization-id eines AuthenticationTokens erkannt. Für diese Telematik-ID
muss ein AuthorizationKey mit gleichlautender ActorID vorhanden sein,
andernfalls ist diese Leistungserbringerinstitution nicht autorisiert. Das
gleiche gilt für die Kostenträger  (Anwendungsfälle G und H).

Der Vertreter wird zunächst als Versicherter mit eigener eGK anhand der KVNR
als subject-id eines AuthenticationTokens erkannt. In der Wahrnehmung einer
Vertretung (Anwendungsfälle F)  ist seine KVNR ungleich der OwnerKVNR des
Eigentümers der Akte. Für seine KVNR muss ein AuthorizationKey mit
gleichlautender ActorID vorhanden sein, andernfalls ist der Vertreter für den
Zugriff nicht autorisiert.

### 3.2 Nachbarsysteme

Der folgende Abschnitt beschreibt die Positionierung der Komponente
Autorisierung im Kontext der Fachanwendung ePA. 

Die folgende Abbildung zeigt die Beziehung zu benachbarten Produkttypen
innerhalb der Fachanwendung mit den von der Komponente Autorisierung
bereitgestellten Schnittstellen.

![Abbildung-2][Abbildung-2]

Die Komponente Autorisierung stellt die
SchnittstellenI_AuthorizationundI_Authorization_Managementzur Nutzung aus der
Umgebung der Leistungserbringer und Kostenträger bereit. Von dort werden sie
aus der Secure Consumer Zone aufgerufen.

Die
SchnittstellenI_Authorization_InsurantundI_Authorization_Management_Insurantwerden
aus der Personal Zone in der Umgebung des Versicherten aufgerufen. In dieser
Umgebung nutzt der Versicherte das ePA-Frontend des Versicherten auf einem
Gerät des Versicherten.

Die Komponente Autorisierung wird als Teil des Produkttyps ePA-Aktensystem in
der Provider Zone der Telematikinfrastruktur betrieben. Sie verfügt über
einen logischen, internen Speicher, an den in diesem Dokument keine
Umsetzungsanforderungen gestellt werden. Er dient der Persistierung der im
Informationsmodell (siehe ) strukturierten Inhalte.

**A_13956 - Komponente Autorisierung -Separierung der Schnittstellen für
verschiedene Umgebungen**

Die Komponente Autorisierung MUSS die Bereitstellungspunkte der Schnittstellen
für die Nutzung durch benachbarte Komponenten und Produkttypen aus
verschiedenen Einsatzumgebungen voneinander separieren.  **[\<=]**

Diese Separierung kann beispielsweise umgesetzt werden durch die Erreichbarkeit
der Schnittstellen über verschiedene Netzwerkadressen. 

### 3.3 Tokenbasierte Autorisierung

Die Komponente Autorisierung bietet eine Single-Sign-On (SSO)-Lösung an, um
einem zuvor authentifizierten Nutzer den Zugriff auf weitere Ressourcen zu
ermöglichen. Hierbei wird nach einer erfolgreichen Autorisierung eine
Autorisierungsbestätigung (AuthorizationAssertion gemäß SAML 2.0 Assertions
[SAML2.0]) ausgestellt.

Für die Initialisierung sowie für den Zugriff auf den Aktenkontext eines
Versicherten erwartet die Komponente Dokumentenverwaltung eine gültige
Assertion von der Komponente Autorisierung. Die Assertion wird ungültig, wenn
der Aktenkontext eines Versicherten geschlossen wird oder der
Gültigkeitszeitraum der Assertion abgelaufen ist.

### 4 Zerlegung der Komponente Autorisierung

Eine detaillierte Zerlegung der Komponente Autorisierung wird nicht vorgegeben.
Gleichwohl muss die Komponente Autorisierung privates Schlüsselmaterial in
einem HSM speichern, das den Anforderungen einer bestimmten Prüftiefe
entspricht. Auf eine grafische Darstellung wird an dieser Stelle verzichtet.

### 5 Übergreifende Festlegungen

### 5.1 Datenschutz und Datensicherheit

Im folgenden Abschnitt werden die für die Komponente Autorisierung notwendigen
Anforderungen für den Schutz personenbezogener Daten bzw. Anforderungen für
den Schutz von Daten beschrieben, um beispielsweise vor Datenmanipulation oder
Datenverlust zu schützen.

**A_14417 - Komponente Autorisierung - Akzeptieren von
Identitätsbestätigungen**

Die Komponente Autorisierung MUSS Identitätsbestätigungen
(AuthenticationAssertion) als ungültig mit dem Fehler ASSERTION_INVALID
ablehnen, wenn die Identität des Ausstellers (Issuer) nicht als
vertrauenswürdiger Dienst für die Durchführung einer Authentifizierung
konfiguriert ist oder dessen X.509-Signatur-Zertifkat nicht zu der Signatur der
Identitätsbestätigung passt. **[\<=]**

**A_13990 - Komponente Autorisierung - Vorgaben für Identitätsbestätigung**

Die Komponente Autorisierung MUSS eine übergebene Identitätsbestätigung
(AuthenticationAssertion) als ungültig mit dem Fehler ASSERTION_INVALID
ablehnen, wenn diese nicht konform zu den Vorgaben der Tabelle
[gemSpec_TBAuth#TAB_TBAuth_03 Identitätsbestätigung] ist. **[\<=]**

**A_14688-01 - Komponente Autorisierung - Prüfung einer
Identitätsbestätigung**

Die Komponente Autorisierung MUSS eine übergebene Identitätsbestätigung
(AuthenticationAssertion) als ungültig mit dem Fehler ASSERTION_INVALID
ablehnen, die nach einer Prüfung gemäß [gemSpec_TBAuth#A_15557](vgl. auch
gemSpec_TBAuth#3.2 Prüfen von Identitätsbestätigungen) als nicht gültig
betrachtet wird. Insbesondere MUSS die Komponente Autorisierung das
Signaturzertifikat der Ausstelleridentität eines Vertrauensraums außerhalb
des Vertrauensraums der Komponente Autorisierung mittels
[gemSpec_PKI#TUC_PKI_018] mit den folgenden Parametern prüfen:Das
Signaturzertifikat muss anhand der Zertifikatsprüfung für [mathematisch
gültig UND zeitlich gültig UND online gültig ] befunden werden. Die
Telematik-ID im Signaturzertifikat muss identisch mit der Telematik-ID in der
Identitätsbestätigung sein. **[\<=]**

**A_18989 - Komponente Autorisierung – Beschränkung gültiger
Identitätsbestätigungen**

Die Komponente Autorisierung DARF in Aufrufen aus Richtung der Komponente
Zugangsgateway KEINE Identitätsbestätigung akzeptieren, die nicht durch die
Komponente Authentisierung (Versicherter) erstellt wurde. **[\<=]**

**A_17839-03 - Komponente Autorisierung - Prüfung der Empfänger-Rolle**

Die Komponente Autorisierung MUSS beim Aufruf einer der Operation

 ---> UL

den übergebenen Parameter 

AuthenticationAssertion

  dahingehend prüfen, ob mindestens eine 

ProfessionOID

 der ZertifikatsExtension

Admission

 gemäß [gemSpec_PKI#Tab_PKI_226] im Signaturzertifikat C.HCI.OSIG

/saml2:Assertion/ds:Signature/ds:KeyInfo/ds:X509Data/ds:X509Certificate

 

in der Liste der zulässigen Autorisierungsempfänger-Rollen gemäß
[gemSpec_OID#Tab_PKI_403]

 ---> UL

enthalten ist und sofern nicht, die Operation mit dem Fehler AUTHORIZATION_ERROR
abbrechen. **[\<=]**

Ist die AuthenticationAssertion vom Aktensystem selbst erstellt worden
(/saml2:Assertion/ds:Signature/ds:KeyInfo/ds:X509Data/ds:X509Certificateenthält
das Signaturzertifikat C.FD.SIG des Aktensystems), entfällt die
Rollenprüfung, da die Rolle des Versicherten bereits durch Komponente
Authentisierung Versicherter geprüft wurde.

**A_17840 - Komponente Autorisierung Vers. - Prüfung Identitätswechsel des
Versicherten**

Die Komponente Autorisierung MUSS eine
übergebene AuthenticationAssertion für einen Versicherten (Das
SAML:Assertion/SAML:AttributeStatement/SAML:Attribute urn:gematik:subject:subject-identhält
eine KVNR) dahingehend prüfen, ob die in der
Behauptung urn:gematik:subject:authreference mit derserialNumberdes zur
Authentifizierung verwendeten AUT- bzw. AUT_ALT-Zertifikats in der Liste der
bekannten AUT-Referenzen an der KeyChain des im RecordIdentifier benannten
Aktenkontos ist und falls nicht,MUSS die Komponente Autorisierung
den Versicherten sowie im Vertretungsfall zusätzlich den Vertreter über die
Nutzung eines neuen Authentisierungsmittels in einer E-Mail-Nachricht an die
hinterlegte E-Mailadresse NotificationInfodes Versicherten bzw. des Vertreters
informieren. Anschließend MUSS die benannteserialNumberin die WhiteList der
AUT-Referenzen an der KeyChain des im RecordIdentifier benannten
Aktenkontos übernommen werden.​​ **[\<=]**

Nutzt der Versicherte ein im Aktensystem bisher unbekanntes
Authentisierungsmittel (z.B. eine Folge-eGK) erhält er eine
E-Mailbenachrichtigung, der Anwendungsfall wird nicht unterbrochen. Es obliegt
dem Versicherten die Legitimität des Zugriffs bzw. des Authentisierungsmittels
zu prüfen und sich gegebenenfalls mit dem ePA-Aktenanbieter und seiner Kasse
in Verbindung zu setzen.

Nutzt der Vertreter des Versicherten ein bisher unbekanntes
Authentisierungsmittel, erhalten sowohl der Versicherte als auch der Vertreter
eine Benachrichtigung.

**A_17655 - Komponente Autorisierung – Prüfung von Identitätsbestätigungen
des Aktensystems**

Die Komponente Autorisierung MUSS sicherstellen, dass Identitätsbestätigungen
für Versicherte nur akzeptiert werden, wenn das zugehörige 
Signaturzertifikat zeitlich gültig ist, nicht gesperrt wurde und nach dem
Zertifikatsprofil C.FD.SIG auf die Identität der Komponente Authentisierung
Versicherter ausgestellt wurde. **[\<=]**

Dies kann durch eine aktuell gehaltene Konfiguration vertrauenswürdiger
Zertifikate umgesetzt werden und ersetzt eine detaillierte Prüfung des
Signaturzertifikats gemäß [gemSpec_TBAuth#A_15557], um die Prüfung solcher
vom ePA-Aktensystem selbst ausgestellten Identitätsbestätigungen zu
vereinfachen.

Eine Prüfung von Identitätsbestätigungen gemäß den Festlegungen für TBAuth
bezieht sich auf Identitätsbestätigungen für Leistungserbringerinstitutionen
und Kostenträger.

**A_14270 - Komponente Autorisierung - Zugriff aus der Umgebung des
Versicherten**

Die Komponente Autorisierung MUSS Zugriffe auf Daten eines Versicherten aus der
Personal Zone heraus verhindern, wenn das verwendete Gerät des Versicherten
nicht in der Liste der bekannten/freigeschalteten Geräte vorhanden ist.
**[\<=]**

Bei Zugriffen aus der Umgebung des Versicherten wird ein Identitätsmerkmal des
verwendeten Geräts abgefragt (DeviceID). Bei Zugriffen aus der Umgebung der
Leistungserbringer erfolgt dies nicht, da hier als zugreifende Geräte
ausschließlich zugelassene Konnektoren mit geprüfter Fachlogik zum Einsatz
kommen. Ebenso wird keine Geräteidentität für den Zugang der Kostenträger
über ihr jeweiliges Rechenzentrum geprüft, da auch hier ausschließlich
zugelassene Produkttypen in einer kontrollierten Betriebsumgebung zum Einsatz
kommen.

**A_14402 - Komponente Autorisierung - Integritätsschutz für
Autorisierungsbestätigungen**

Die Komponente Autorisierung MUSS jede ausgestellte Autorisierungsbestätigung
mit dem privaten Schlüssel der Ausstelleridentität C.FD.SIG in seiner
fachlichen Rolle oid_epa_authz gemäß [gemSpec_OID] signieren. **[\<=]**

**A_14740 - Komponente Autorisierung - TLS-Identität innerhalb der TI**

Die Komponente Autorisierung MUSS sich beim TLS-Verbindungsaufbau an den
Schnittstellen innerhalb der TI mit der technischen Rolle oid_epa_authz
der TLS-Identität C.FD.TLS-S authentisieren. **[\<=]**

Hinweis zu A_14740:Die Komponente Autorisierung soll für seine serverseitigen
TLS-Endpunkte in der TI die Server TLS-Identität C.FD.TLS-S verwenden.

**A_14529 - Komponente Autorisierung - Absicherung gegenüber dem Internet**

Die Komponente Autorisierung MUSS alle Operationsaufrufe der Schnittstellen
I_Authorization_Insurant und I_Authorization_Management_Insurant auf
Wohlgeformtheit und Zulässigkeit gemäß Protokoll SOAP 1.2 prüfen und bei
Schema-, Semantik- oder Protokollverletzungen eine aufgerufene Operation mit
dem HTTP-Statuscode 400 gemäß [RFC-7231]  abbrechen. **[\<=]**

Die Prüfung der eingehenden Nachrichten auf Syntax-, Semantik- und
Protokollverletzungen soll insbesondere den Angriffstypen XML
Injection, XPath Query Tamperingund XML External Entity
Injection entgegenwirken.

Im Fall der Sperrung der Signaturidentität der Komponente Autorisierung, darf
diese nicht für die Ausstellung einer Autorisierungsbestätigung genutzt
werden. Da diese Identität aus dem gleichen Vertrauensraum stammt wie die
Signaturidentität der Identitätsbestätigung eines Authentisierungsdienstes
im gleichen Aktensystem, dürfen in diesem Fall auch keine
Identitätsbestätigungen des gleichen Vertrauensraums mehr akzeptiert werden.

**A_16260 - Komponente Autorisierung - Periodische Prüfung Signaturidentität**

Die Komponente Autorisierung MUSS den Sperrstatus der eigenen Signaturidentität
C.FD.SIG mittels [gemSpec_PKI#TUC_PKI_018] periodisch (einmal täglich)
prüfen:Das Signaturzertifikat muss anhand der Zertifikatsprüfung für
[mathematisch gültig UND zeitlich gültig UND online gültig] befunden werden.
**[\<=]**

**A_16261 - Komponente Autorisierung - Keine Autorisierung bei gesperrter
Signaturidentität**

Die Komponente Autorisierung MUSS das Ausstellen einer
Autorisierungsbestätigung mit dem Fehler INTERNAL_ERROR abbrechen, wenn das
Signaturzertifikat der Komponente Autorisierung gemäß einer Statusprüfung
nach [A_16260] nicht gültig ist. **[\<=]**

**A_16262 - Komponente Autorisierung - Keine Identitätsbestätigung bei
gesperrter Signaturidentität**

Die Komponente Autorisierung MUSS alle Identitätsbestätigungen aller Issuer
des gleichen Vertrauensraums der Signaturidentität C.FD.SIG der Komponente
Autorisierung mit dem Fehler INTERNAL_ERROR als ungültig ablehnen, wenn das
Signaturzertifikat der Komponente Autorisierung gemäß einer
Statusprüfung nach [A_16260] nicht gültig ist. **[\<=]**

**A_22570 - Komponente Autorisierung – Kein Zugriff auf gesperrte Akten**

Die Komponente Autorisierung MUSS eine aufgerufene Operation mit dem
Standardfehler ACCESS_DENIED abbrechen, wenn die Akte gemäß
[gemSpec_Aktensystem#A_22569]gesperrt wurde. **[\<=]**

### 5.2 Verwendete Standards

Für die Sicherstellung der Interoperabilität wird auf verwendete Standards
zurückgegriffen.Durch die Verwendung des IHE-Frameworks (Integrating the
Healthcare Enterprise) zum einheitlichen Datenaustausch im Gesundheitssystem
ist die Verwendung von SAML zum Austausch von Authentisierungsinformationen
notwendig.

Für die Übertragung von Nachrichten zwischen dem Fachmodul und den
Teilkomponenten von ePA wird das vom W3C standardisierte Protokoll SOAP 1.2 in
Verbindung mit HTTP verwendet.

**A_13801 - Komponente Autorisierung - Verwendung von SAML 2.0**

Die Komponente Autorisierung MUSS Authentisierungsbestätigung im Format SAML
2.0 Assertions [SAML2.0] unterstützen. **[\<=]**

**A_13802 - Komponente Autorisierung - Ausstellung im Format SAML 2.0**

Die Komponente Autorisierung MUSS Autorisierungsbestätigungen im Format SAML
2.0 Assertions [SAML2.0] ausstellen. **[\<=]**

**A_14969 - Komponente Autorisierung - Kodierung in UTF-8**

Die Komponente Autorisierung MUSS bei der Erstellung von XML-Fragmenten das
Encoding UTF-8 verwenden. **[\<=]**

**A_17760 - Komponente Autorisierung - AuthenticationAssertion im SOAP-Header**

Die Komponente Autorisierung MUSS die Identitätsbestätigungen eines Nutzers
(AuthenticationAssertion) im Header eines eingehenden SOAP-Requests
akzeptieren. **[\<=]**

**A_17761 - Komponente Autorisierung - Verwendung des SAML Token Profile 1.1
für Web Services Security bei SAML 2.0 Assertions**

Die Komponente Autorisierung MUSS die Anforderungen aus [WSS-SAML] umsetzen,
wenn eine SAML 2.0 Assertion Teil einer SOAP 1.2-Eingangsnachricht ist.
**[\<=]**

**A_17762 - Komponente Autorisierung - Verwendung von SOAP Message Security 1.1**

Die Komponente Autorisierung MUSS die Sicherheitsanforderungen aus SOAP Message
Security 1.1 [WSS] für die Verarbeitung von SOAP 1.2-Nachrichten umsetzen.
**[\<=]**

**A_17763 - Komponente Autorisierung - Unterstützung von Profilen der Web
Services Interoperability Organization (WS-I)**

Die Komponente Autorisierung MUSS das WS-I Basic Profile V2.0 [WSIBP],
das WS-I Basic Security Profile Version V1.1 [WSIBSP] sowie das WS-I
Attachment Profile V1.0 [WSIAP] für die Kommunikation über Web Services
berücksichtigen. **[\<=]**

### 5.3 Protokollierung

Die Anforderungen an die Protokollierung für die Komponente Autorisierung
leiten sich aus dem Konzept der Protokollierung aus [gemSysL_ePA#2.5.5] ab.

**A_14403-02 - Komponente Autorisierung - Verwaltungsprotokollierung
Autorisierung**

Die Komponente Autorisierung MUSS beim Aufruf einer der folgenden Operationen:

 ---> UL

je einen Eintrag im Verwaltungsprotokoll für den Versicherten
gemäß [gemSpec_DM_ePA#A_14471-*] mit folgenden vom Operationsaufruf
abhängigen Parameterwerten vornehmen:

UserID, UserName, ObjectID, ObjectName, DeviceID, ObjectDetail

. **[\<=]**

**A_20514 - Komponente Autorisierung - Verwaltungsprotokollierung Rollback
Umschlüsselung**

Die Komponente Autorisierung MUSS beim Rollback, der bei einer abgebrochenen
Umschlüsselung erfolgt, einen Eintragim Verwaltungsprotokoll für den
Versicherten mit PHR-850 vornehmen. **[\<=]**

**A_15753-01 - Komponente Autorisierung - Verwaltungsprotokollierung
E-Mail-Adresse ändern**

Die Komponente Autorisierung MUSS das manuelle Ändern der
Benachrichtigungsadresse (z.B. durch den Anbieter im Supportfall)im
Verwaltungsprotokoll des Versicherten mit PHR-451 protokollieren. **[\<=]**

**A_14427-01 - Komponente Autorisierung - Verwaltungsprotokollierung Gerät
hinzufügen**

Die Komponente Autorisierung MUSS beim Hinzufügen eines Geräts in die Liste
der registrierten Geräte einen Eintragim Verwaltungsprotokoll für den
Versicherten mit PHR-470 vornehmen. **[\<=]**

**A_14188-03 - Komponente Autorisierung - Umfang Verwaltungsprotokoll**

Die Komponente Autorisierung MUSS dem Versicherten oder berechtigten Vertreter
die Einträge des Verwaltungsprotokolls gemäß der Festlegung
in [gemSpec_DM_ePA#A_14471-*] übergeben:

Tabelle 2: Parameter des Verwaltungsprotokolls

<table><tr><th>
Protokoll-parameter

</th><th colspan="2" rowspan="1">
Parameterwerte gemäß aufgerufener Operation

</th></tr><tr><td>
UserID

</td><td colspan="2" rowspan="1">
Wert des AttributeStatements der übergebenen übergebenen
AuthenticationAssertion in  
SAML:Assertion/SAML:AttributeStatement  
Variante
a: Akteur des Aufrufs ist Versicherter bzw. Vertreter   
(unveränderbare
Anteil der KVNR des aufrufenden Versicherten bzw. Vertreters)  
XPath-Ausdruck
zur "Subject-ID" der im Operationsaufruf übergebenen Authentication Assertion:
 
//*[local-name()='Assertion' and namespace-uri() =
'urn:oasis:names:tc:SAML:2.0:assertion']//*[local-name()='Attribute' and
namespace-uri() = 'urn:oasis:names:tc:SAML:2.0:assertion'][@Name=
'urn:gematik:subject:subject-id']/*[local-name()='AttributeValue']/*[local-name()='InstanceIdentifier']/data(@extension)
 
 Hinweis: Bei Aufrufen der Fälle PHR-451 sowie PHR-470 (via Webseite) kann
der Wert für die UserID nicht aus der AuthenticationAssertion bezogen werden,
sondern es MUSS die actorID aus dem AuthorizationKey des Betroffenen
(Versicherter oder Vertreter) entnommen werden.   
  
Variante b: Akteur des
Aufrufs ist LEI oder Kostenträger  
(Telematik-ID der aufrufenden LEI oder
Kostenträgers)  
XPath-Ausdruck zur "Organization-ID" der im Operationsaufruf
übergebenen Authentication Assertion:  
//*[local-name()='Assertion' and
namespace-uri() =
'urn:oasis:names:tc:SAML:2.0:assertion']//*[local-name()='Attribute' and
namespace-uri() = 'urn:oasis:names:tc:SAML:2.0:assertion'][@Name= 'urn:gematik
: subject:organization-id']/*[local-name()='AttributeValue']/*[local-name()='InstanceIdentifier']/data(@extension)

</td></tr><tr><td>
UserName

</td><td colspan="2" rowspan="1">
XPath-Ausdruck zur Behauptung "name" (beinhaltet commonName aus dem
X.509-Zertifikat), der im Operationsaufruf übergebenen Authentication
Assertion:  
//*[local-name()='Assertion' and namespace-uri() =
'urn:oasis:names:tc:SAML:2.0:assertion']//*[local-name()='Attribute' and
namespace-uri() =
'urn:oasis:names:tc:SAML:2.0:assertion'][@Name='http://schemas.xmlsoap.org/ws/2005/05/identity/claims/name']/*[local-name()='AttributeValue']
 
 Hinweis: Bei Aufrufen der Fälle PHR-451 sowie PHR-470 (via Webseite) kann
der Wert für den UserName nicht aus der AuthenticationAssertion bezogen werden
sondern es MUSS der DisplayName aus dem AuthorizationKey des Betroffenen
(Versicherter oder Vertreter) entnommen werden.

</td></tr><tr><td>
ObjectID

</td><td colspan="2" rowspan="1">
ActorID

des im Operationsaufruf gelesenen, gespeicherten oder geänderten
AuthorizationKey

Hinweis: Bei Aufruf von Operationen ohne Bezug zu einem AuthorizationKey wird
der Wert im Protokolleintrag nicht belegt (z.B. getAuditEvents).

</td></tr><tr><td>
ObjectName

</td><td colspan="2" rowspan="1">
DisplayName

des AuthorizationKeys

Hinweis: Bei Aufruf von Operationen ohne DisplayName wird der Wert im
Protokolleintrag nicht belegt.

</td></tr><tr><td>
DeviceID

</td><td colspan="2" rowspan="1">
DeviceID

-Parameter

DeviceIdType::Displayname

  des Operationsaufrufs

Hinweis: Bei Aufruf der Operationen der
Schnittstelle I_Authorization_Management gibt es den Parameter nicht, DeviceID
wird  im Protokolleintrag demzufolge nicht belegt.

</td></tr><tr><td colspan="1" rowspan="3">
ObjectDetail

</td><td colspan="2" rowspan="1">
Falls die Operation mit einem Fehler ASSERTION_INVALID aufgrund einer
ungültigen übergebenen Authentication Assertion abbricht, MUSS
ParticipantObjectDetail

mit folgenden Wertepaaren (

type/value

) belegt werden

:

</td></tr><tr><td>
type

</td><td>
value

</td></tr><tr><td>
ErrorInformation

</td><td>
"fehlgeschlagene Authentifizierung des Zugreifenden"

</td></tr></table>

**[\<=]**

**A_14189 - Komponente Autorisierung - Protokollierung Schutz vor Manipulation**

Die Komponente Autorisierung MUSS sicherstellen, dass die
Verwaltungsprotokolldaten gegen Veränderung und unberechtigtes Löschen
geschützt sind. **[\<=]**

### 5.4 Fehlerbehandlung in Schnittstellenoperationen

Bei Fehlern in der internen Verarbeitung oder fachlichen Fehlern in der Nutzung
der von der Komponente Autorisierung bereitgestellten Schnittstellen werden
Operationsaufrufe mit gematik-Fehlermeldungen gemäß der Definition in
[gemSpec_OM] beantwortet. Die Fehlermeldungen werden als SOAP-Fault gemäß
[TelematikError.xsd] strukturiert. Abweichend von den Festlegungen in
[gemSpec_OM] sind zu meldende Fehler wie folgt mit Informationen zu füllen.

**A_15068 - Komponente Autorisierung - Fehlername**

Die Komponente Autorisierung MUSS in einer GERROR-Fehlermeldung gemäß
[TelematikError.xsd] den in der Operationsdefinition festgelegten
FehlernamenNameim Feld tel:Error/tel:Trace/tel:EventIDverwenden. **[\<=]**

Die folgende Abbildung illustriert das Schema der GERROR-Struktur in
TelematikError.xsd:

![Abbildung-3][Abbildung-3]

**A_15069 - Komponente Autorisierung - Fehlertext**

Die Komponente Autorisierung MUSS in einer GERROR-Fehlermeldung gemäß
[TelematikError.xsd] den in der Operationsdefinition festgelegten
Fehlerdetailtext Fehlertext im
Feld tel:Error/tel:Trace/tel:ErrorTextverwenden. **[\<=]**

**A_15101-06 - Komponente Autorisierung - Fehlernummer**

Die Komponente Autorisierung MUSS in einer GERROR-Fehlermeldung gemäß
[TelematikError.xsd] die folgenden Fehlercodes im
Feld tel:Error/tel:Trace/tel:Codeverwenden:

Tabelle3: Fehlercodes zu Fehlern gemäß Operationsdefinition

<table><tr><th>
Name

</th><th>
Fehlercode

</th></tr><tr><td>
TECHNICAL_ERROR

</td><td>
7900

</td></tr><tr><td>
KEY_ERROR

</td><td>
7910

</td></tr><tr><td>
SYNTAX_ERROR

</td><td>
7930

</td></tr><tr><td>
ASSERTION_INVALID

</td><td>
7940

</td></tr><tr><td>
DEVICE_UNKNOWN

</td><td>
7950

</td></tr><tr><td>
ACCESS_DENIED

</td><td>
7960

</td></tr><tr><td>
AUTHORIZATION_ERROR

</td><td>
7970

</td></tr><tr><td>
REPRESENTATIVE_ PENDING

</td><td>
7980

</td></tr><tr><td>
INTERNAL_ERROR

</td><td>
7990

</td></tr><tr><td>
KEY_LOCKED

</td><td>
8000

</td></tr><tr><td>
KEY_CORRUPT

</td><td>
8010

</td></tr><tr><td>
ACTOR_UNKNOWN

</td><td>
8020

</td></tr><tr><td>
DEVICE_LOCKED

</td><td>
8030

</td></tr></table>

**[\<=]**

Die Operationsdefinitionen der Schnittstellen der Komponente Autorisierung
beschränken die Liste möglicher Fehler auf fachliche Fehler. Daneben sind
weitere, technische Gründe für Fehler anderer Art denkbar. Für diese kann
der Hersteller der Komponente einen generischen Fehler für den Transport
geeigneter Fehlerinformationen (z.B. für Supportzwecke) verwenden.

**A_15102 - Komponente Autorisierung - Herstellerspezifische Fehlermeldungen**

Die Komponente Autorisierung MUSS komponenteninterne und 
 herstellerspezifische Fehlermeldungen in einer GERROR-Fehlermeldung gemäß
[TelematikError.xsd] mit folgender Festlegung transportieren:

Tabelle4: Herstellerspezifische Fehlerdefinition

<table><tr><th>
GERROR-Element

</th><th>
Herstellerspezifisch zu belegen

</th></tr><tr><td>
tel:Error/tel:Trace/tel:Code

</td><td>
Fester Wert: "

7900"

</td></tr><tr><td>
tel:Error/tel:Trace/tel:EventID

</td><td>
Fester Wert:

"TECHNICAL_ERROR"

</td></tr><tr><td>
tel:Error/tel:Trace/tel:ErrorText

</td><td>
Je Fehlerfall zufällig gewählte Fehlernummer

</td></tr></table>

**[\<=]**

**A_15249 - Komponente Autorisierung - Herstellerspezifische Fehlermeldungen
Detailtext**

Die Komponente Autorisierung MUSS Details zu herstellerspezifischen
Fehlermeldungen ausschließlich in einem internen Fehlerprotokoll und zusammen
mit der zum Zeitpunkt des Fehlers gewählten zufälligen Fehlernummer
speichern. **[\<=]**

Die herstellerspezifische und je Fehlerfall zufällig gewählte Fehlernummer
dient der Kapselung von Implementierungs- und Fehlerbehebungsdetails und zum
Auffinden der Fehlermeldungsdetails in einem internen Fehlerprotokoll im
Supportfall.

### 5.5 Nicht-Funktionale Anforderungen

### 5.5.1 Skalierbarkeit

Die für die Komponente Autorisierung relevanten Informationen zur
Skalierbarkeit sind in [gemSpec_Perf] zu entnehmen.

### 5.5.2 Performance

Die durch die Komponente Autorisierung zu erfüllende Performance-Anforderung
befinden sich in [gemSpec_Perf].

### 5.5.3 Mengengerüst

Das für die Komponente Autorisierung relevante Mengengerüst befindet sich in
[gemSpec_Perf].

### 6 Funktionsmerkmale

Die Komponente Autorisierung realisiert die Funktionsmerkmale der
kryptografischen Autorisierung und eine Geräteverwaltung. Das Funktionsmerkmal
der Autorisierung wird über die Implementierung der
Schnittstellen I_Authorization, I_Authorization_Management, I_Authorization_Insurantund I_Authorization_Management_Insurantrealisiert.

Die Nutzung des Funktionsmerkmals der Geräteverwaltung durch den Versicherten
erfolgt über einen separaten Verwaltungszugang abseits
derI_Authorization*-Schnittstellen. Dieser Zugang ist für den Versicherten
über das Internet erreichbar.

### 6.1 Übergreifende Festlegungen

Im Folgenden werden übergreifende Festlegungen formuliert, die in allen
Operationen umgesetzt werden.

Wenn im Folgenden die KVNR als ActorID, OwnerKVNR oder subject-id referenziert
wird ist immer der unveränderliche Anteil als 10-stellige Kennung gemeint.

**A_14469 - Komponente Autorisierung - Identifizierung des Versicherten anhand
einer AuthenticationAssertion**

Die Komponente Autorisierung MUSS jeden Versicherten anhand des
unveränderlichen Teils der KVNR
als   urn:gematik:subject:subject-idinSAML:Assertion/SAML:AttributeStatement/SAML:Attribute/@Nameeiner
übergebenen, gültigen AuthenticationAssertion eindeutig identifizieren, wenn
die subject-idmit der OwnerKVNR zu einem im Operationsaufruf angegebenen
RecordIdentifier übereinstimmt. **[\<=]**

**A_14499 - Komponente Autorisierung - Identifizierung einer Institution anhand
einer AuthenticationAssertion**

Die Komponente Autorisierung MUSS jede Leistungserbringerinstitution und jeden
Kostenträger anhand der Telematik-ID
als   urn:gematik:subject:organization-idinSAML:Assertion/SAML:AttributeStatement/SAML:Attribute/@Nameeiner
übergebenen, gültigen AuthenticationAssertion eindeutig identifizieren, wenn
für diese ein AuthorizationKey zu einem im Operationsaufruf angegebenen
RecordIdentifier existiert. **[\<=]**

**A_14500 - Komponente Autorisierung - Identifizierung eines Vertreters anhand
einer AuthenticationAssertion**

Die Komponente Autorisierung MUSS einen berechtigten Vertreter anhand seiner
KVNR als  
 urn:gematik:subject:subject-idinSAML:Assertion/SAML:AttributeStatement/SAML:Attribute/@Nameeiner
übergebenen, gültigen AuthenticationAssertion eindeutig identifizieren, wenn
die subject-idungleich der OwnerKVNR zu einem im Operationsaufruf angegebenen
RecordIdentifier ist und für die KVNR der AuthenticationAssertion ein
AuthorizationKey zu der im Operationsaufruf angegebenen RecordIdentifier
existiert. **[\<=]**

**A_14434 - Komponente Autorisierung - Prüfung der Schnittstellenparameter**

Die Komponente Autorisierung MUSS in jeder Operation alle übergebenen
Eingangsparameter auf Konformität zum Schema AuthorizationService.xsd prüfen
und bei Nichtkonformität die jeweilige Operation mit dem Fehler
TECHNICAL_ERROR gemäß den Festlegungen zur  abbrechen. **[\<=]**

**A_14369-02 - Komponente Autorisierung - Prüfung des Geräts des Versicherten**

Die Komponente Autorisierung MUSS in allen Operationen der
Schnittstellen I_Authorization_Insurant und I_Authorization_Management_Insurantanhand
des Wertes DeviceID::Deviceprüfen, ob das vom Nutzer verwendete Gerät in der
Geräteliste des AuthorizationKeys des Nutzers bekannt/freigeschaltet ist und
andernfalls die Operation mit dem Fehler DEVICE_UNKNOWN abbrechen, in dessen
SOAP-Error in tel:Error/tel:Trace/tel:ErrorTexteine
gemäß generiertephr:DeviceID::Deviceeinfügen und den Freischaltprozess
neuer Geräte auslösen. Wenn das Gerät bekannt und gesperrt ist, MUSS die
Operation mit dem Fehler DEVICE_LOCKED abgebrochen werden. Eine neue Geräte-ID
DARF in diesem Fall NICHT generiert und an das FdV übergeben werden. **[\<=]**

Greift ein Nutzer mit einem Gerät erstmalig auf die in A_14369-* genannten
Schnittstellen zu, sind die Elemente phr:DeviceID@ und phr:DeviceID::Device in
den aufgerufenen Operationen ggfs. leer bzw. enthalten eine Zeichenkette der
Länge 0 ("").

**A_14634 - Komponente Autorisierung - Prüfung auf vorhandenen
AuthorizationKey**

Die Komponente Autorisierung MUSS eine aufgerufene Operationen mit dem
Standardfehler KEY_ERROR abbrechen, wenn es zu fachlichen Fehlern in Lese- oder
Schreiboperationen eines AuthorizationKey kommt oder dieser für einen in der
ActorID benannten Nutzer in der KeyChain eines benannten RecordIdentifier
nicht vorhanden ist. **[\<=]**

**A_14768 - Komponente Autorisierung - Prüfung auf Berechtigung**

Die Komponente Autorisierung MUSS eine aufgerufene Operation mit dem
Standardfehler ACCESS_DENIED abbrechen, wenn ein über
diesubject-idbzw.organization-ideiner AuthenticationAssertion identifizierter
Nutzer eine Operation auf einem im RecordIdentifier benannten Datensatz
aufruft, für den kein AuthorizationKey hinterlegt und er nicht der Eigentümer
ist, d.h. OwnerKVNR != subject-idbzw.organization-idund es
existiertkeinAuthorizationKey mitActorID == subject-idbzw.organization-id.
**[\<=]**

Der Fehler ACCESS_DENIED wird ebenso erwartet, wenn im jeweiligen
Aufrufparameter ein RecordIdentifier mit einer falschen HomeCommunityID
übergeben wird.  Eine leere HomeCommunityID führt hingegen nicht zu einem
Fehler.

**A_16487 - Komponente Autorisierung - Prüfung auf Tokenherkunft**

Die Komponente Autorisierung MUSS jeden Aufruf an den
SchnittstellenI_Authorization_Insurantund I_Authorization_Management_Insurant mit
dem Fehler ACCESS_DENIED ablehnen, der mittels einer AuthenticationAssertion
erfolgt, die nicht aus dem Vertrauensraum der Komponente Autorisierung erfolgt.
**[\<=]**

**A_17102 - Komponente Autorisierung - Maximale Berechtigungsstufe für
Konto-Eigentümer**

Die Komponente Autorisierung MUSS sicherstellen, dass der AuthorizationType am
hinterlegten AuthorizationKey des Versicherten immer "DOCUMENT_AUTHORIZATION"
lautet. **[\<=]**

### 6.2 Schnittstellen der Komponente Autorisierung

Das Funktionsmerkmal 'Autorisierung' der Komponente Autorisierung wird durch die
in der folgenden Tabelle beschriebenen Schnittstellen mit den jeweiligen
Operationen umgesetzt.

<table><tr><th colspan="2">
Schnittstellen der Komponente Autorisierung

</th></tr><tr><td colspan="2">
I_Authorization

</td></tr><tr><td>
getAuthorizationKey

</td><td>
Mit der Operation

getAuthorizationKey

wird das für einen Berechtigten verschlüsselte Schlüsselmaterial für ein
konkretes Aktenkonto eines Versicherten in der

Leistungserbringer-Umgebung

und durch den Kostenträger heruntergeladen.

</td></tr><tr><td colspan="2">
I_Authorization_Management

</td></tr><tr><td>
putAuthorizationKey

</td><td>
Mit der Operation

putAuthorizationKey

wird das für einen Berechtigten verschlüsselte Schlüsselmaterial für ein
konkretes Aktenkonto  eines Versicherten im Aktensystem ePA gespeichert.

</td></tr><tr><td>
checkRecordExists

</td><td>
Mit der Operation

checkRecordExists

kann ein anderer Anbieter bei einem Anbieter einer Aktenlösung den Status und
die Existenz eines Aktenkontos über die KVNR eines Versicherten abfragen.

</td></tr><tr><td>
getAuthorizationList

</td><td>
Die Operation

getAuthorizationList

liefert die Liste aller OwnerKVNRs des Aktensystems, in denen für die
anfragende Institution ein AuthorizationKey hinterlegt ist. 

(horizontale Abfrage) 

</td></tr><tr><td>
getAuthorizationState

</td><td>
Die Operation

getAuthorizationState

liefert für das Aktenkonto der im Aufruf übergebenen KVNR, ob Berechtigungen
für die anfragende Identität vorliegen und gibt bei existierender
Berechtigung das Tupel Fachanwendung und das Endedatum der Berechtigung zurück.

</td></tr><tr><td colspan="2">
I_Authorization_Insurant

</td></tr><tr><td>
getAuthorizationKey

</td><td>
Mit der Operation

getAuthorizationKey

wird das für einen Berechtigten verschlüsselte Schlüsselmaterial
(kryptografische Berechtigung) für ein konkretes Aktenkonto eines Versicherten
in der Personal-Zone heruntergeladen.

</td></tr><tr><td colspan="2">
I_Authorization_Management_Insurant

</td></tr><tr><td>
putAuthorizationKey

</td><td>
Mit der Operation

putAuthorizationKey

wird das für einen Berechtigten verschlüsselte Schlüsselmaterial
AuthorizationKey für ein konkretes Aktenkonto eines Versicherten im
ePA-Aktensystem gespeichert.

</td></tr><tr><td>
deleteAuthorizationKey

</td><td>
Mit der Operation

deleteAuthorizationKey

kann ein authentifizierter Versicherter bzw. ein berechtigter Vertreter die
kryptografische Berechtigung für einen Nutzer innerhalb seines Aktenkontos
löschen.

</td></tr><tr><td>
replaceAuthorizationKey

</td><td>
Mit der Operation replaceAuthorizationKey kann ein authentifizierter
Versicherter bzw. ein berechtigter Vertreter das im Aktenkonto für einen
benannten Nutzer hinterlegte kryptografische Schlüsselmaterial  ersetzen. Die
Operation kann insbesondere dazu benutzt werden, den Berechtigungszeitraum für
einen AuthorizationKey anzupassen. 

</td></tr><tr><td>
getAuditEvents

</td><td>
Mit der Operation

getAuditEvents

kann ein authentifizierter Versicherter bzw. ein berechtigter Vertreter das
Verwaltungsprotokoll der Komponente Autorisierung auslesen.

</td></tr><tr><td>
getSignedAuditEvents

</td><td>
Die Operation

getSignedAuditEvents

liefert für einen authentifizierten Versicherten bzw. einen berechtigten
Vertreter eine signierte Liste (SignedAuditEventList) der Verwaltungsprotokolle
des Versicherten der Komponente Autorisierung.

</td></tr><tr><td>
putNotificationInfo

</td><td>
Mit der Operation

putNotificationInfo

kann ein authentifizierter Versicherter bzw. ein berechtigter Vertreter die
eigene, im Benachrichtigungskanal hinterlegten Daten aktualisieren.

</td></tr><tr><td>
getNotificationInfo

</td><td>
Mit der Operation

getNotificationInfo

kann ein authentifizierter Versicherter Email-Adressen abfragen, die für
zugriffsberechtige Versicherten bzw. ihre Vertreter im Benachrichtigungskanal
seines Aktenkontos hinterlegt sind.

</td></tr><tr><td>
getKtrTelematikID

</td><td>
Die Operation liefert die TelematikID des Kostenträgers, der das Kontos
im Aktensystems anbietet.

</td></tr><tr><td>
getRecordProviderList

</td><td>
Die Operation liefert eine Liste

der Internet-FQDN aller ePA-Aktensysteme.

</td></tr><tr><td>
getAuthorizationList

</td><td>
Die Operation

getAuthorizationList

liefert die Liste aller AuthorizationKeys zu einer angefragten Akte eines
Versicherten. 

(vertikale Abfrage)

</td></tr><tr><td>
startKeyChange

</td><td>
Mit dieser Operation kann der Versicherte den Prozess der Umschlüsselung an der
Komponente Autorisierung initiieren und die Autorisierungskomponente bis zur
Beendigung der Verarbeitung für andere Aktivitäten sperren.

</td></tr><tr><td>
putForReplacement

</td><td>
Mit dieser Operation übergibt der Versicherte die für die Umschlüsselung an
der Komponente Autorisierung erforderlichen verschlüsselten AuthorizationKeys,
damit diese die bisher verwendeten AuthorizationKeys ersetzen können.

</td></tr><tr><td>
finishKeyChange

</td><td>
Mit dieser Operation beendet der Versicherte die Umschlüsselung an der
Komponente Autorisierung und hebt die Sperre der Autorisierungskomponente für
anderweitige Autorisierungsaktivitäten auf.

</td></tr></table>

### 6.2.1 Schnittstelle I_Authorization

Diese Schnittstelle setzt die in [gemSysL_ePA#4.2.2.2] definierte
SchnittstelleI_Authorizationtechnisch um.

Die Schnittstelle stellt dem Fachmodul eine Operation zum Bezug eines
Autorisierungs-Tokens für bereits authentifizierte Leistungserbringer und
Kostenträger bereit, um die ePA-Komponente Dokumentenverwaltung verwenden zu
können.

### 6.2.1.1 Operationsdefinition I_Authorization::getAuthorizationKey

**A_14045-01 - Komponente Autorisierung - I_Authorization::getAuthorizationKey**

Die Komponente Autorisierung MUSS die
OperationI_Authorization::getAuthorizationKeygemäß der folgenden Signatur
implementieren:

Tabelle6: I_Authorization::getAuthorizationKey Definition

<table><tr><th>
Operation

</th><th colspan="3">
I_Authorization::getAuthorizationKey 

</th></tr><tr><td>
Beschreibung

</td><td colspan="3">
Mit dieser Operation wird für einen authentifizierten Nutzer eine Autorisierung
des Zugriffs auf Daten eines Versicherten geprüft.

</td></tr><tr><td>
Formatvorgaben

</td><td colspan="3">
Die Definition der Ein- und Ausgabeparameter erfolgt in
[AuthorizationService.xsd].

Diejenigen Parameter, die im XSD-Schema optional gekennzeichnet, aber hier nicht
aufgeführt sind, werden in der Operation an dieser Schnittstelle nicht
verwendet.

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

ist eine von einem Identitiy Provider ausgestellte
Authentifizierungsbestätigung für einen Nutzer.

</td><td>
SAML Assertion im SOAP-Header des Requests

</td><td>
-

</td></tr><tr><td>
RecordIdentifier

</td><td>
Der

RecordIdentifier

referenziert ein konkretes Aktenkonto eines Versicherten bei einem Anbieter. Mit
diesem wird der Datensatz der kryptografischen Autorisierung in der Komponente
Autorisierung für den anfragenden Nutzer lokalisiert.

</td><td>
RecordIdentifierType

</td><td>
-

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
AuthorizationAssertion

</td><td>
Die

AuthorizationAssertion

ist eine signierte Autorisierungsbestätigung für einen Nutzer und enthält
Informationen über die Art und den Umfang der in der Komponente Autorisierung
hinterlegten Autorisierung.

</td><td>
SAML Assertion

base64-codiert

</td><td>
-

</td></tr><tr><td>
AuthorizationKey

</td><td>
Die kryptografische Autorisierung eines Nutzers. 

</td><td>
AuthorizationKeyType

</td><td>
ja

</td></tr><tr><td colspan="4">
Fehlermeldungen 

</td></tr><tr><td>
Name

</td><td>
Fehlertext

</td><td colspan="2">
Details

</td></tr><tr><td>
TECHNICAL_ERROR

</td><td>
Zufallszahl

</td></tr><tr><td>
ASSERTION_INVALID

</td><td>
Authentifizierungsbestätigung ungültig

</td><td colspan="2">
Die Authentifizierungsbestätigung des aufrufenden Nutzers wird nicht akzeptiert.

</td></tr><tr><td>
ACCESS_DENIED

</td><td>
Zugriff verweigert

</td><td colspan="2">
Die Operation ist mit den angegebenen Parametern nicht zulässig.

</td></tr><tr><td>
KEY_ERROR

</td><td>
Fehler im Schlüsseldatensatz

</td><td colspan="2">
Kein Datensatz für diesen Nutzer für den benannten RecordIdentifier vorhanden.

</td></tr><tr><td>
REPRESENTATIVE_PENDING

</td><td>
Vertretungsberechtigung erfordert Freischaltung

</td><td colspan="2">
Die Vertretung kann erst wahrgenommen werden, wenn diese über den
Freischaltprozess autorisiert wurde.

</td></tr><tr><td>
AUTHORIZATION_ERROR

</td><td>
Autorisierung nicht zulässig

</td><td colspan="2">
Die zu hinterlegte Berechtigtenrolle ist nicht zulässig.

</td></tr></table>

Sollte bei der Autorisierung für einen Versicherten kein zugehöriger Datensatz
gefunden werden, darf dies nicht mit einer technischen Fehlermeldung behandelt
werden. Hierfür MUSS eine sprechende Information (fachliches Ereignis)
geliefert werden. **[\<=]**

### 6.2.1.2 Umsetzung I_Authorization::getAuthorizationKey

Die folgenden Anforderungen beschreiben die Umsetzung der
OperationI_Authorization::getAuthorizationKey. Dabei gelten die übergreifenden
Festlegungen zur Prüfung der Eingangsparameter.

**A_17790 - Komponente Autorisierung LE - Vertretung wahrnehmen
Freischaltprüfung**

Die Komponente Autorisierung MUSS bei Wahrnehmung einer Vertretung für einen
Versicherten mittels I_Authorization::getAuthorizationKey(subject-idder
AuthenticationAssertion !=OwnerKVNR) vor der Herausgabe prüfen, ob ein
wartender Vertreter-Freischaltprozess für [OwnerKVNR des benannten
RecordIdentifiers, subject-id als ActorID] aktiv ist und falls ja, die
Operation mit dem Fehler REPRESENTATIVE_PENDING abbrechen. **[\<=]**

**A_13917 - Komponente Autorisierung LE - Ausstellen einer
Autorisierungsbestätigung**

Die Komponente Autorisierung MUSS inder
OperationI_Authorization::getAuthorizationKey bei Vorhandensein
einesAuthorizationKey in derKeyChaindes benanntenRecordIdentifierfür den
mittelsAuthenticationAssertionauthentifizierten Nutzer
(subject-IDbzw.organization-id == ActorID) eineAuthorizationAssertiongemäß
der Festlegung in [A_14491-*] ausstellen und diese in der Ausgangsnachricht
der Operation zurückgeben.Der Wert für [AuthorizationType] in der
AuthorizationAssertion MUSS dem Wert des hinterlegten AuthorizationKey genau
dieses authentifizierten Nutzers entsprechen. **[\<=]**

**A_17662 - Komponente Autorisierung LE - Codierung der
Autorisierungsbestätigung**

Die Komponente Autorisierung MUSS die erstellte und signierte
Autorisierungsbestätigung in der Response der
Operation I_Authorization::getAuthorizationKeyBase64-codiert zurückgeben.
**[\<=]**

**A_13692 - Komponente Autorisierung LE - Herausgabe kryptografischer
Berechtigung des Nutzers**

Die Komponente Autorisierung MUSS in der
OperationI_Authorization::getAuthorizationKey bei Vorhandensein
einesAuthorizationKey in derKeyChaindes benanntenRecordIdentifier für den
mittelsAuthenticationAssertionauthentifizierten Nutzer
(subject-IDbzw.organization-id == ActorID) denAuthorizationKeyin der
Ausgangsnachricht der Operation zurückgeben. **[\<=]**

**A_14643 - Komponente Autorisierung LE - Aktivierung bei Kontoeröffnung in der
Umgebung der Leistungserbringer**

Die Komponente Autorisierung MUSS dem authentifizierten Versicherten als
Eigentümer der Akte (subject-ID == OwnerKVNRfür den
benanntenRecordIdentifier) eine Autorisierungsbestätigung mit
AuthorizationType = ACCOUNT_AUTHORIZATION gemäß [A_14491-*] ausstellen,
wenn für seine OwnerKVNR kein Schlüsseldatensatz AuthorizationKey in der
KeyChain vorhanden ist. **[\<=]**

**A_15618-01 - Komponente Autorisierung LE - keine Autorisierung bei
suspendiertem Konto**

Die Komponente Autorisierung MUSS bei Aufruf der
OperationI_Authorization::getAuthorizationKeymit der
FehlermeldungACCESS_DENIEDabbrechen, wenn derRecordState derKeyChaindes
benanntenRecordIdentifier den ZustandSUSPENDED oder START_MIGRATIONaufweist.
**[\<=]**

**A_21741 - Komponente Autorisierung LE - keine Autorisierung vor Beendigung der
Datenübernahme**

Die Komponente Autorisierung MUSS bei Aufruf der
OperationI_Authorization::getAuthorizationKeymit der
FehlermeldungACCESS_DENIEDabbrechen, wenn derRecordState derKeyChaindes
benanntenRecordIdentifier den ZustandREGISTERED_FOR_MIGRATION, DL_IN_PROGRESS
oder READY_FOR_IMPORTaufweist. **[\<=]**

### 6.2.2 Schnittstelle I_Authorization_Insurant

Diese Schnittstelle setzt die in [gemSysL_ePA] definierte
SchnittstelleI_Authorization_Insuranttechnisch um.

Die SchnittstelleI_Authorization_Insurantstellt Operationen zur
Autorisierungsprüfung auf das Vorhandensein von kryptografischem
Schlüsselmaterial für einen Nutzer des Aktenkontos eines Versicherten bereit.
Sie stellt dem Frontend des Versicherten eine Schnittstelle zum Abruf eines
Autorisierungs-Tokens für bereits authentifizierte Versicherte bereit.

### 6.2.2.1 Operationsdefinition I_Authorization_Insurant::getAuthorizationKey

**A_14042-01 - Komponente Autorisierung -
I_Authorization_Insurant::getAuthorizationKey**

Die Komponente Autorisierung MUSS die
OperationI_Authorization_Insurant::getAuthorizationKeygemäß der folgenden
Signatur implementieren:

Tabelle7: I_Authorization_Insurant::getAuthorizationKey Definition

<table><tr><th>
Operation

</th><th colspan="3">
I_Authorization_Insurant::getAuthorizationKey 

</th></tr><tr><td>
Beschreibung

</td><td colspan="3">
Mit dieser Operation wird für einen authentifizierten Nutzer eine Autorisierung
des Zugriffs auf Daten eines Versicherten geprüft.

</td></tr><tr><td>
Formatvorgaben

</td><td colspan="3">
Die Definition der Ein- und Ausgabeparameter erfolgt in
[AuthorizationService.xsd].

Diejenigen Parameter, die im XSD-Schema optional gekennzeichnet, aber hier nicht
aufgeführt sind, werden in der Operation an dieser Schnittstelle nicht
verwendet.

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

ist eine von einem Identitiy Provider ausgestellte
Authentifizierungsbestätigung für einen Nutzer.

</td><td>
SAML Assertion im SOAP-Header des Requests

</td><td>
-

</td></tr><tr><td>
RecordIdentifier

</td><td>
Der

RecordIdentifier

referenziert ein konkretes Aktenkonto eines Versicherten bei einem Anbieter. Mit
diesem wird der Datensatz der Autorisierung in der Komponente Autorisierung
für den anfragenden Nutzer lokalisiert.

</td><td>
RecordIdentifierType

</td><td>
-

</td></tr><tr><td>
DeviceID

</td><td>
Die

DeviceID

enthält die Gerätekennung eines vom Nutzer verwendeten Geräts.

</td><td>
DeviceIdType

</td><td>
-

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
AuthorizationAssertion

</td><td>
Die

AuthorizationAssertion

ist eine signierte Autorisierungsbestätigung für einen Nutzer und enthält
Informationen über die Art und den Umfang der in der Komponente Autorisierung
hinterlegten Autorisierung.

</td><td>
SAML Assertion mit

AuthorizationDecision Statement

base 64-codiert

</td><td>
-

</td></tr><tr><td>
AuthorizationKey

</td><td>
Die kryptografische Autorisierung eines Nutzers.

</td><td>
AuthorizationKeyType

</td><td>
ja

</td></tr><tr><td colspan="4">
Fehlermeldungen 

</td></tr><tr><td>
Name

</td><td>
Fehlertext

</td><td colspan="2">
Details

</td></tr><tr><td>
TECHNICAL_ERROR

</td><td>
Zufallszahl  

</td></tr><tr><td>
ASSERTION_INVALID

</td><td>
Authentifizierungsbestätigung ungültig

</td><td colspan="2">
Die Authentifizierungsbestätigung des aufrufenden Nutzers wird nicht akzeptiert.

</td></tr><tr><td>
ACCESS_DENIED

</td><td>
Zugriff verweigert

</td><td colspan="2">
Die Operation ist mit den angegebenen Parametern nicht zulässig.

</td></tr><tr><td>
KEY_ERROR

</td><td>
Fehler im Schlüsseldatensatz

</td><td colspan="2">
Kein Datensatz für diesen Nutzer für den benannten RecordIdentifier vorhanden.

</td></tr><tr><td>
DEVICE_UNKOWN

</td><td>
generierte

phr:DeviceID::Device

</td><td colspan="2">
Das vom Nutzer verwendete Gerät des Versicherten ist nicht bekannt und muss
freigeschaltet werden.

</td></tr><tr><td>
REPRESENTATIVE_PENDING

</td><td>
Vertretungsberechtigung erfordert Freischaltung

</td><td colspan="2">
Die Vertretung kann erst wahrgenommen werden, wenn diese über den
Freischaltprozess autorisiert wurde.

</td></tr></table>

Sollte bei der Autorisierung für einen Versicherten kein zugehöriger Datensatz
gefunden werden, darf dies nicht mit einer technischen Fehlermeldung behandelt
werden. Hierfür MUSS eine sprechende Information (fachliches Ereignis)
geliefert werden. **[\<=]**

### 6.2.2.2 Umsetzung I_Authorization_Insurant::getAuthorizationKey

Die folgenden Anforderungen beschreiben die Umsetzung der
OperationI_Authorization_Insurant::getAuthorizationKey. Dabei gelten die
übergreifenden Festlegungen zur Prüfung der Eingangsparameter.

**A_22232 - Komponente Autorisierung Vers. - Fehler REPRESENTATIVE_PENDING**

Die Komponente Autorisierung MUSS, solange der Vertreter noch nicht
freigeschaltet ist, die Operation mit dem Fehler REPRESENTATIVE_PENDING
abbrechen. (Siehe auch A_17674, A_17789) **[\<=]**

**A_17789 - Komponente Autorisierung Vers. - Vertretung wahrnehmen
Freischaltprüfung**

Die Komponente Autorisierung MUSS bei Wahrnehmung einer Vertretung für einen
Versicherten
mittels I_Authorization_Insurant::getAuthorizationKey(subject-idder
AuthenticationAssertion !=OwnerKVNR) vor der Herausgabe prüfen, ob ein
wartender Vertreter-Freischaltprozess für [OwnerKVNR des benannten
RecordIdentifiers, subject-id als ActorID] aktiv ist und falls ja, die
Operation mit dem Fehler REPRESENTATIVE_PENDING abbrechen. **[\<=]**

**A_14436 - Komponente Autorisierung Vers. - Ausstellen einer
Autorisierungsbestätigung**

Die Komponente Autorisierung MUSS in der
OperationI_Authorization_Insurant::getAuthorizationKey bei Vorhandensein
einesAuthorizationKey in derKeyChaindes benanntenRecordIdentifier für den
mittelsAuthenticationAssertion authentifizierten Nutzer [subject-id der
AuthenticationAssertion == ActorID des vorhandenen AuthorizationKey]
eineAuthorizationAssertiongemäß der Festlegung in [A_14491-*] ausstellen und
diese in der Ausgangsnachricht der Operation zurückgeben.Der Wert für
[AuthorizationType] in der AuthorizationAssertion MUSS dem Wert des
hinterlegten AuthorizationKey genau dieses authentifizierten Nutzers
entsprechen. **[\<=]**

**A_17663 - Komponente Autorisierung Vers. - Codierung der
Autorisierungsbestätigung**

Die Komponente Autorisierung MUSS die erstellte und signierte
Autorisierungsbestätigung in der Response der
Operation I_Authorization_Insurant::getAuthorizationKeyBase64-codiert
zurückgeben. **[\<=]**

**A_14439 - Komponente Autorisierung Vers. - Herausgabe kryptografischer
Berechtigung des Nutzers**

Die Komponente Autorisierung MUSS in der
OperationI_Authorization_Insurant::getAuthorizationKey bei Vorhandensein
einesAuthorizationKey in derKeyChaindes benanntenRecordIdentifier für den
mittelsAuthenticationAssertionauthentifizierten Versicherten oder Vertreter
(subject-id == ActorID) denAuthorizationKey  des authentifizierten Nutzers in
der Ausgangsnachricht der Operation zurückgeben. **[\<=]**

**A_14644 - Komponente Autorisierung Vers. - Aktivierung bei Kontoeröffnung in
der Umgebung des Versicherten**

Die Komponente Autorisierung MUSS bei Aufruf der
OperationI_Authorization_Insurant::getAuthorizationKey dem authentifizierten
Versicherten als Eigentümer der Akte (subject-ID == OwnerKVNRfür den
benanntenRecordIdentifier) eine Autorisierungsbestätigung mit
AuthorizationType = ACCOUNT_AUTHORIZATION gemäß [A_14491-*] ausstellen, wenn
für seine OwnerKVNR kein Schlüsseldatensatz AuthorizationKey in der KeyChain
vorhanden ist. **[\<=]**

**A_21742-02 - Komponente Autorisierung Vers. - ACCOUNT_AUTHORIZATION bei
Datenübernahme**

Die Komponente Autorisierung MUSS bei Aufruf der
Operation I_Authorization_Insurant::getAuthorizationKey  in
der KeyChain des benannten RecordIdentifier für den
mittels AuthenticationAssertion authentifizierten Nutzer
(subject-id = OwnerKVNR) eine Autorisierungsbestätigung mit
AuthorizationType = ACCOUNT_AUTHORIZATION gemäß [A_14491-*] ausstellen, wenn
der RecordState der KeyChain des benannten RecordIdentifier den Zustand
SUSPENDED, START_MIGRATION, REGISTERED_FOR_MIGRATION, DL_IN_PROGRESS oder
READY_FOR_IMPORT aufweist. Sofern der benannte Nutzer nicht der Versicherte
selbst ist (subject-id != OwnerKVNR) , MUSS die Komponente Autorisierung den
Aufruf mit der Fehlermeldung ACCESS_DENIED abbrechen. **[\<=]**

**A_21810-01 - Komponente Autorisierung Vers. - Zulässige Operationen bei
START_MIGRATION und SUSPENDED**

Die Komponente Autorisierung MUSS bei einer AuthenticationAssertion des
authentifizierten Nutzers mit subject-id = OwnerKVNR und wenn der RecordState
der KeyChain des benannten RecordIdentifier den Zustand SUSPENDED oder
START_MIGRATION aufweist nur den Aufruf
derOperationen I_Authorization_Insurant::getAuthorizationKey, 
I_Authorization_Management_Insurant::getNotificationInfo
und I_Authorization_Management_Insurant::getAuthorizationList  zulassen. Ist
der Nutzer nicht der Versicherte (subject-id != OwnerKVNR) oder werden andere
Operationen als die aufgeführten aufgerufen, MUSS der entsprechende
Aufruf mit der Fehlermeldung ACCESS_DENIED beendet werden. **[\<=]**

### 6.2.3 Schnittstelle I_Authorization_Management

Diese Schnittstelle setzt die in [gemSysL_ePA] definierte
SchnittstelleI_Authorization_Managementtechnisch um.

Die SchnittstelleI_Authorization_Managementdient dazu, kryptografische
Berechtigungen im Autorisierungsdienst eines Aktensystems zu verwalten.

### 6.2.3.1 Operationsdefinition I_Authorization_Management::putAuthorizationKey

**A_14180-01 - Komponente Autorisierung -
I_Authorization_Management::putAuthorizationKey**

Die Komponente Autorisierung MUSS die
OperationI_Authorization_Management::putAuthorizationKeygemäß der folgenden
Signatur implementieren:

Tabelle8: I_Authorization_Management::putAuthorizationKey - Definition

<table><tr><th>
Operation

</th><th colspan="3">
I_Authorization_Management::putAuthorizationKey 

</th></tr><tr><td>
Beschreibung

</td><td colspan="3">
Mit der Operation wird das für einen Berechtigten verschlüsselte
Schlüsselmaterial für ein konkretes Akt

enkonto

eines Versicherten im ePA-Aktensystem gespeichert.

</td></tr><tr><td>
Formatvorgaben

</td><td colspan="3">
Die Definition der Ein- und Ausgabeparameter erfolgt in
[AuthorizationService.xsd].

Diejenigen Parameter, die im XSD-Schema optional gekennzeichnet, aber hier nicht
aufgeführt sind, werden in der Operation an dieser Schnittstelle nicht
verwendet.

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

ist eine von einem Identitiy Provider ausgestellte
Authentifizierungsbestätigung für einen Nutzer.

</td><td>
SAML Assertion  im SOAP-Header des Requests

</td><td>
-

</td></tr><tr><td>
RecordIdentifier

</td><td>
Der

RecordIdentifier

referenziert ein konkretes Aktenkonto eines Versicherten bei einem Anbieter. Mit
diesem wird der Datensatz der Autorisierung in der Komponente Autorisierung
für den anfragenden Nutzer lokalisiert.

</td><td>
RecordIdentifierType

</td><td>
-

</td></tr><tr><td>
AuthorizationKey

</td><td>
Die kryptografische Autorisierung eines Nutzers, bestehend aus Listen von
verschlüsselten Schlüsseln. Details zur Struktur finden sich im Kapitel 7
zum Informationsmodell.

</td><td>
AuthorizationKeyType 

</td><td>
-

</td></tr><tr><td colspan="4">
Fehlermeldungen 

</td></tr><tr><td>
Name

</td><td>
Fehlertext

</td><td colspan="2">
Details

</td></tr><tr><td>
TECHNICAL_ERROR

</td><td>
Zufallszahl

</td></tr><tr><td>
ASSERTION_INVALID

</td><td>
Authentifizierungsbestätigung ungültig

</td><td colspan="2">
Die Authentifizierungsbestätigung des aufrufenden Nutzers wird nicht akzeptiert.

</td></tr><tr><td>
ACCESS_DENIED

</td><td>
Zugriff verweigert

</td><td colspan="2">
Die Operation ist mit den angegebenen Parametern nicht zulässig.

</td></tr></table>

**[\<=]**

### 6.2.3.2 Umsetzung I_Authorization_Management::putAuthorizationKey

Die folgenden Anforderungen beschreiben die Umsetzung der
OperationI_Authorization_Management::putAuthorizationKey. Dabei gelten die
übergreifenden Festlegungen zur Prüfung der Eingangsparameter.

**A_14212 - Komponente Autorisierung LE - Speicherung kryptografische
Berechtigung des Nutzers**

Die Komponente Autorisierung MUSS in der
OperationI_Authorization_Management::putAuthorizationKey den im
Eingangsparameter übergebenenAuthorizationKey als AuthorizationKey der
KeyChain des im Eingangsparameter benannten RecordIdentifier speichern bzw.
ersetzen, falls für die im AuthorizationKeybenannte ActorID bereits
einAuthorizationKey in der KeyChain des benanntenRecordIdentifier existiert.
**[\<=]**

**A_14441 - Komponente Autorisierung LE - Berechtigungsprüfung
Schlüsselhinterlegung**

Die Komponente Autorisierung MUSS beim Aufruf der
Operation I_Authorization_Management::putAuthorizationKey anhand der KVNR
der AuthenticationAssertion und des RecordIdentifierprüfen, ob für den
aufrufenden Nutzer ein AuthorizationKey mitActorID == subject-ID hinterlegt
ist, und falls nicht, die Operation mit dem Fehler ACCESS_DENIED abbrechen.
**[\<=]**

Mit dieser Prüfung wird sichergestellt, dass nur Versicherte bzw. Vertreter
einen Schlüssel für einen Berechtigten hinterlegen können. Eine Berechtigung
wird nicht von einer Leistungserbringerinstitution oder von einem Kostenträger
hinterlegt.

**A_14587 - Komponente Autorisierung LE - Initiale Schlüsselhinterlegung
Kontoeröffnung**

Die Komponente Autorisierung MUSS die Operation
 I_Authorization_Management::putAuthorizationKey mit dem Fehler ACCESS_DENIED
abbrechen, sofern für den Eigentümer der Akte noch kein AuthorizationKey
vorhanden ist und der zu speicherndeAuthorizationKeydes Aufrufparameters für
einen anderen Nutzer als den Eigentümer desRecordIdentifier (ActorID !=
OwnerKVNR) gespeichert werden soll. **[\<=]**

Mit dieser Anforderung soll verhindert werden, dass die Akte genutzt wird, bevor
das Schlüsselmaterial für den Versicherten erzeugt und hinterlegt wurde. Die
benannte Konstellation liegt im Rahmen der Kontoeröffnung und bei einem
Aktenumzug vor. Das Schlüsselmaterial für den Versicherten wird im Schritt
der Kontoaktivierung erzeugt, welcher auf den Schritt der Kontoinitialisierung
folgt.

**A_14737-01 - Komponente Autorisierung LE - Initiale Schlüsselhinterlegung
für den Versicherten**

Die Komponente Autorisierung MUSS bei Aufruf der
Operation I_Authorization_Management::putAuthorizationKeydurch den
Versicherten (subject-id (KVNR) der AuthenticationAssertion == OwnerKVNR) im
Rahmen der initialen Schlüsselhinterlegung während der Kontoaktivierung
dasvalidTo-Datum des übergebenenAuthorizationKeyvor der Speicherung mit einem
technischen Datum gleichbedeutend mit "unendlich" (31.12.9999) ersetzen.
**[\<=]**

**A_21880 - Komponente Autorisierung LE - Keine Berechtigung von Vertretern bei
I_Authorization_Management::putAuthorizationKey**

Die Komponente Autorisierung MUSS bei Aufruf der
Operation I_Authorization_Management::putAuthorizationKeyprüfen, ob die im
AuthorizationKey benannte ActorID == OwnerKVNR oder eine TelematikID ist und
falls nicht, die Operation mit dem Fehler ACCESS_DENIED abbrechen. **[\<=]**

**A_14999 - Komponente Autorisierung LE - Zustandswechsel bei
Schlüsselhinterlegung für den Versicherten**

Die Komponente Autorisierung MUSS bei Aufruf der
Operation I_Authorization_Management::putAuthorizationKeydurch den
Versicherten (subject-id (KVNR) der AuthenticationAssertion == OwnerKVNR) bei
erfolgreichem Abschluss der initialen Schlüsselhinterlegung für den
Versicherten während der Kontoaktivierung den ZustandRecordStateder KeyChain
des Versicherten vonREGISTEREDauf den WertACTIVATEDsetzen. **[\<=]**

**A_21869 - Komponente Autorisierung LE - Keine Ausführung von
I_Authorization_Management::putAuthorizationKey bei SUSPENDED oder
START_MIGRATION**

Im ZustandRecordStateder KeyChain des Versicherten vonSUSPENDED oder
START_MIGRATION MUSS die
Operation I_Authorization_Management::putAuthorizationKey mit der
Fehlermeldung ACCESS_DENIED abgebrochen werden. **[\<=]**

### 6.2.3.3 Operationsdefinition I_Authorization_Management::checkRecordExists

**A_14965-01 - Komponente Autorisierung -
I_Authorization_Management::checkRecordExists**

Die Komponente Autorisierung MUSS die
Operation I_Authorization_Management::checkRecordExistsgemäß der folgenden
Signatur implementieren:

Tabelle9: I_Authorization_Management::checkRecordExists - Definition

<table><tr><th>
Operation

</th><th colspan="3">
I_Authorization_Management::checkRecordExists

</th></tr><tr><td>
Beschreibung

</td><td colspan="3">
Die Operation liefert den Status eines Aktenkontos eines via KVNR benannten
Versicherten. 

</td></tr><tr><td>
Formatvorgaben

</td><td colspan="3">
Die Definition der Ein- und Ausgabeparameter erfolgt in
[AuthorizationService.xsd].

Diejenigen Parameter, die im XSD-Schema optional gekennzeichnet, aber hier nicht
aufgeführt sind, werden in der Operation an dieser Schnittstelle nicht
verwendet.

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
KVNR

</td><td>
Der unveränderliche Teil der Krankenversicherungsnummer eines gesetzlich
Versicherten

</td><td>
String

</td><td>
-

</td></tr><tr><td>
AllMandators

</td><td>
 ---> UL

 ---> UL

</td><td>
boolean

</td><td>
ja

</td></tr><tr><td colspan="4">
Ausgangsparameter

</td></tr><tr><td>
Name 

</td><td>
Beschreibung 

</td><td>
Typ 

</td><td>
opt 

</td></tr><tr><td>
RecordState

 

</td><td>
Statuswert zur Existenz eines Aktenkontos in der Komponente Autorisierung zu
einer angefragten KVNR

</td><td>
RecordStateType

</td><td>
-

</td></tr><tr><td>
HomeCommunityId

</td><td>
HomeCommunityId des Aktensystem-Mandanten, in dem eine Akte zur KVNR vorliegt,
die sich im Zustand REGISTERED, ACTIVATED oder DISMISSED befindet. Wird bei
keinem Aktensystem-Mandanten eine solche Akte gefunden, wird keine
HomeCommunityId zurück gegeben.

</td><td>
HomeCommunityIdType

</td><td>
ja

</td></tr><tr><td colspan="4">
Fehlermeldungen

</td></tr><tr><td>
Name

</td><td>
Fehlertext

</td><td colspan="2">
Details

</td></tr><tr><td>
TECHNICAL_ERROR

</td><td>
Zufallszahl

</td></tr></table>

**[\<=]**

### 6.2.3.4 Umsetzung I_Authorization_Management::checkRecordExists

Die folgenden Anforderungen beschreiben die Umsetzung der
OperationI_Authorization_Management::checkRecordExists. Dabei gelten die
übergreifenden Festlegungen zur Prüfung der Eingangsparameter.

**A_14966-01 - Komponente Autorisierung LE - Abfrage Aktenexistenz bei
AllMandators=false oder leer**

Falls der Parameter AllMandators=false gesetzt ist oder fehlt, MUSS
die Komponente Autorisierung bei Aufruf der Operation
I_Authorization_Management::checkRecordExists den Wert RecordState
des Datensatzes KeyChain eines Konto zurückliefern, wenn zu einer
angefragten KVNR ein Datensatz KeyChain mit OwnerKVNR == KVNR existiert und
andernfalls den Statuswert UNKNOWN zurückgeben. Bei fehlendem
Parameter AllMandators oder bei RecordState mit dem Wert UNKNOWN entfällt der
Rückgabeparameter HomeCommunityId. **[\<=]**

**A_22465 - Komponente Autorisierung – Abfrage Aktenexistenz bei
AllMandators=true**

Falls der ParameterAllMandators=truegesetzt ist MUSS die
Operation  I_Authorization_Management:: checkRecordExistsüber alle
Aktensystem-Mandanten zur angefragten KVNR alle Aktenkonten ermitteln
(DatensatzKeyChainmitOwnerKVNR == KVNRexistiert). Zur Konsolidierung des
Auswertungsergebnisses MUSS für alle ermittelten Aktenkonten der
StatusREGISTERED, ACTIVATED, DISMISSEDgesucht werden. Sobald der erste dieser
Status gefunden wird, MUSS der gefundene Status des Aktenkontos und
dieHomeCommunityIddes betreffenden Aktensystem-Mandanten als Response in den
AusgangsparameternRecordStateundHomeCommunityIdzurückgegeben werden.
Andernfalls wird derRecordState mit dem Wert UNKNOWNzurückgegeben und der
RückgabeparameterHomeCommunityId entfällt. **[\<=]**

Für die Abarbeitung der Operation checkRecordExistsmit
ParameterAllMandators=truekann das Aktensystem für die
eigenen Aktensystem-Mandanten checkRecordExistsmit
ParameterAllMandators=falsenutzen.

### 6.2.3.5 Operationsdefinition I_Authorization_Management::getAuthorizationList

**A_17110 - Komponente Autorisierung -
I_Authorization_Management::getAuthorizationList**

Die Komponente Autorisierung MUSS die
Operation I_Authorization_Management::getAuthorizationListgemäß der
folgenden Signatur implementieren:

Tabelle10: I_Authorization_Management::getAuthorizationList - Definition

<table><tr><th>
Operation

</th><th colspan="3">
I_Authorization_Management::getAuthorizationList

</th></tr><tr><td>
Beschreibung

</td><td colspan="3">
Die Operation liefert eine Liste der OwnerKVNRs von Konten im Aktensystem, in
denen die anfragende Identität berechtigt ist.

</td></tr><tr><td>
Formatvorgaben

</td><td colspan="3">
Die Definition der Ein- und Ausgabeparameter erfolgt in
[AuthorizationService.xsd].

Diejenigen Parameter, die im XSD-Schema optional gekennzeichnet, aber hier nicht
aufgeführt sind, werden in der Operation an dieser Schnittstelle nicht
verwendet.

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

 ist eine von einem Identitiy Provider ausgestellte
Authentifizierungsbestätigung für einen Nutzer.

</td><td>
SAML Assertion im SOAP-Header des Requests

</td><td>
-

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
AuthorizationInfoList

 

</td><td>
Liste der OwnerKVNRs von Konten im Aktensystem, in denen für die Telematik-ID
der anfragenden Leistungserbringerinstitution bzw. der Kostenträger ein
AuthorizationKey aktuell vorhanden ist.

</td><td>
AuthorizationInfo[0..*]

</td><td>
-

</td></tr><tr><td colspan="4">
Fehlermeldungen

</td></tr><tr><td>
Name

</td><td>
Fehlertext

</td><td colspan="2">
Details

</td></tr><tr><td>
ASSERTION_INVALID

</td><td>
Die übergebene AuthenticationAssertion ist ungültig.

</td><td colspan="2">
z.B. abgelaufen oder Misstrauen in Signatur des Tokens

</td></tr><tr><td>
T

ECHNICAL_ERROR

</td><td>
Zufallszahl

</td></tr></table>

**[\<=]**

### 6.2.3.6 Umsetzung I_Authorization_Management::getAuthorizationList

Die folgenden Anforderungen beschreiben die Umsetzung der
OperationI_Authorization_Management::getAuthorizationList. Dabei gelten die
übergreifenden Festlegungen zur Prüfung der Eingangsparameter.

**A_17111 - Komponente Autorisierung LE - Abfrage Berechtigungsliste**

Die Komponente Autorisierung MUSS bei Aufruf
der OperationI_Authorization_Management::getAuthorizationListdie Liste aller
OwnerKVNRs ermitteln, in deren KeyChain für dieorganization-idder gültigen
AuthenticationAssertion ein AuthorizationKey vorhanden ist
(organization-id==ActorID) und diese Liste als AuthorizationInformation
[OwnerKVNR+ validToam jeweiligen AuthorizationKey der ActorID je KeyChain]
zurückgeben. **[\<=]**

**A_19007 - Komponente Autorisierung - Einschränkung der Häufigkeit der
Abfrage getAuthorizationList**

Das Aktensystem KANN getAuthorizationList-Anfragen mit dem Fehler
TOO_MANY_REQUESTS zurückweisen, wenn sie von derselben LEI (bei Gleichheit der
organization-id) innerhalb eines Zeitraumes von 10 Minuten wiederholt gestellt
werden.  **[\<=]**

**A_22382 - Komponente Autorisierung LE - Erstellung der Berechtigungsliste nur
bei ACTIVATED und DISMISSED**

Die Komponente Autorisierung MUSS bei Aufruf der
OperationI_Authorization_Management::getAuthorizationListausschließlich
Aktenkonten berücksichtigen, die sich im Zustand ACTIVATED oder DISMISSED
befinden. **[\<=]**

### 6.2.3.7 Operationsdefinition I_Authorization_Management::getAuthorizationState

**A_22447 - Komponente Autorisierung -
I_Authorization_Management::getAuthorizationState**

Die Komponente Autorisierung MUSS die
Operation I_Authorization_Management::getAuthorizationStategemäß der
folgenden Signatur implementieren:

Tabelle11: I_Authorization_Management::getAuthorizationState - Definition

<table><tr><th>
Operation

</th><th colspan="3">
I_Authorization_Management::getAuthorizationState

</th></tr><tr><td>
Beschreibung

</td><td colspan="3">
Die Operation prüft für das Aktenkonto der im Aufruf übergebenen KVNR, ob
eine Berechtigung für die anfragende Identität vorliegt und gibt bei
existierender Berechtigung das Endedatum der Berechtigung zurück.

</td></tr><tr><td>
Formatvorgaben

</td><td colspan="3">
Die Definition der Ein- und Ausgabeparameter erfolgt in
[AuthorizationService.xsd].

Diejenigen Parameter, die im XSD-Schema optional gekennzeichnet, aber hier nicht
aufgeführt sind, werden in der Operation an dieser Schnittstelle nicht
verwendet.

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

 ist eine von einem Identitiy Provider ausgestellte
Authentifizierungsbestätigung für einen Nutzer.

</td><td>
SAML Assertion im SOAP-Header des Requests

</td><td>
-

</td></tr><tr><td>
UserAgents

</td><td>
Liste der UserAgent Clients.

UserAgent dient bei der Performance-Rohdatenerfassung der Erkennung der
UserAgents.

Bildungsvorschrift für UserAgent siehe A_22470.

</td><td>
UserAgentsType

(LIste von Strings; Gesamtlänge von 17 bis maximal 65 Zeichen)

</td><td>
-

</td></tr><tr><td>
InsurantId

</td><td>
InsurantId

referenziert ein konkretes Aktenkonto eines Versicherten. Mit diesem wird der
Datensatz der Autorisierung in der Komponente Autorisierung für den
anfragenden Nutzer lokalisiert.

 

</td><td>
InsurantId

Type 

</td><td>
-

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
AuthorizationStatusList

</td><td>
Liste aller Berechtigungen für das durch InsurantId adressierte Aktenkonto
im Aktensystem, in denen für die Telematik-ID der anfragenden
Leistungserbringerinstitution bzw. der Kostenträger ein AuthorizationKey
aktuell vorhanden ist.  
Falls eine Berechtigung für die Anwendung vorliegt
wird ein Eintrag in der Liste für die berechtigte Anwendung und das Endedatum
der Berechtigung übergeben. Liegt keine einzige Berechtigung vor so
entfällt AuthorizationStatusList.

</td><td>
AuthorizedApplication[0..*]

</td><td>
ja

</td></tr><tr><td colspan="4">
Fehlermeldungen

</td></tr><tr><td>
Name

</td><td>
Fehlertext

</td><td colspan="2">
Details

</td></tr><tr><td>
ASSERTION_INVALID

</td><td>
Die übergebene AuthenticationAssertion ist ungültig.

</td><td colspan="2">
z.B. abgelaufen oder Misstrauen in Signatur des Tokens

</td></tr><tr><td>
TECHNICAL_ERROR

</td><td>
Zufallszahl

</td></tr><tr><td>
TOO_MANY_REQUESTS

(HTTP-Fehler)

</td><td>
Http 429 Too many Requests

</td></tr></table>

**[\<=]**

### 6.2.3.8 Umsetzung I_Authorization_Management::getAuthorizationState

Die folgenden Anforderungen beschreiben die Umsetzung der
OperationI_Authorization_Management::getAuthorizationState. Dabei gelten die
übergreifenden Festlegungen zur Prüfung der Eingangsparameter.

**A_22448 - Komponente Autorisierung LE - Abfrage Berechtigungsliste**

Die Komponente Autorisierung MUSS bei Aufruf
der OperationI_Authorization_Management::getAuthorizationStatefür das durch
dieInsurantIdadressierte Aktenkonto die Berechtigung für die Fachanwendungen
ermitteln, in deren KeyChain für dieorganization-idder gültigen
AuthenticationAssertion ein AuthorizationKey vorhanden ist
(organization-id==ActorID) und bei vorhandener Berechtigung einen Eintrag in
AuthorizationStatusList mitApplicationNameund dem Endedatum validToder
ermittelten Berechtigung zurückgeben. **[\<=]**

**A_22449 - Komponente Autorisierung - Einschränkung der Häufigkeit der
Abfrage getAuthorizationState**

Das Aktensystem KANN getAuthorizationState-Anfragen mit dem Fehler
TOO_MANY_REQUESTS zurückweisen, wenn sie von derselben LEI (bei Gleichheit der
organization-id) und derselben InsurantId innerhalb eines Zeitraumes von 10
Minuten wiederholt gestellt werden.  **[\<=]**

**A_22568 - Komponente Autorisierung LE - Erstellung der Berechtigungsliste in
getAuthorizationState nur bei ACTIVATED und DISMISSED**

DieKomponente Autorisierung MUSS bei Aufruf der
OperationI_Authorization_Management::getAuthorizationStateausschließlich
Aktenkonten berücksichtigen, die sich im Zustand ACTIVATED oder DISMISSED
befinden. **[\<=]**

### 6.2.4 Schnittstelle I_Authorization_Management_Insurant

Diese Schnittstelle setzt die in [gemSysL_ePA] definierte
SchnittstelleI_Authorization_Management_Insuranttechnisch um.

Die SchnittstelleI_Authorization_Management_Insurantstellt Operationen zur
Verwaltung von kryptografischen Berechtigungen im Autorisierungsdienst eines
Aktensystems bereit.

### 6.2.4.1 Operationsdefinition I_Authorization_Management_Insurant::putAuthorizationKey

**A_14672-01 - Komponente Autorisierung -
I_Authorization_Management_Insurant::putAuthorizationKey**

Die Komponente Autorisierung MUSS die
Operation I_Authorization_Management_Insurant::putAuthorizationKeygemäß der
folgenden Signatur implementieren:

Tabelle12: I_Authorization_Management_Insurant::putAuthorizationKey - Definition

<table><tr><th>
Operation

</th><th colspan="3">
I_Authorization_Management_Insurant::putAuthorizationKey

</th></tr><tr><td>
Beschreibung

</td><td colspan="3">
Mit dieser Operation wird für einen Berechtigten verschlüsseltes
Schlüsselmaterial für ein konkretes Aktenkonto eines Versicherten im
Aktensystem gespeichert. 

</td></tr><tr><td>
Formatvorgaben

</td><td colspan="3">
Die Definition der Ein- und Ausgabeparameter erfolgt in
[AuthorizationService.xsd].

Diejenigen Parameter, die im XSD-Schema optional gekennzeichnet, aber hier nicht
aufgeführt sind, werden in der Operation an dieser Schnittstelle nicht
verwendet.

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

 ist eine von einem Identitiy Provider ausgestellte
Authentifizierungsbestätigung für einen Nutzer.

</td><td>
SAML Assertion im SOAP-Header des Requests

</td><td>
-

</td></tr><tr><td>
RecordIdentifier

</td><td>
Der

RecordIdentifier

referenziert ein konkretes Aktenkonto eines Versicherten bei einem Anbieter. Mit
diesem wird der Datensatz der Autorisierung in der Komponente Autorisierung
für den anfragenden Nutzer lokalisiert.

</td><td>
RecordIdentifierType

</td><td>
-

</td></tr><tr><td>
AuthorizationKey

</td><td>
Die kryptografische Autorisierung eines Nutzers,  bestehend aus Listen von
verschlüsselten Schlüsseln. Details zur Struktur finden sich im Kapitel 7
zum Informationsmodell.

</td><td>
AuthorizationKeyType

</td><td>
-

</td></tr><tr><td>
DeviceID

</td><td>
Die

DeviceID

enthält die Gerätekennung eines vom Nutzer verwendeten Gerätes.

</td><td>
DeviceIdType 

</td><td>
-

</td></tr><tr><td>
NotificationInfoRepresentative

</td><td>
Mit diesem Parameterhinterlegt der Versicherte eine Benachrichtigungsadresse
der Geräteverwaltung des mittels AuthorizationKey berechtigten Vertreters.

</td><td>
String

</td><td>
ja

</td></tr><tr><td colspan="4">
Fehlermeldungen

</td></tr><tr><td>
Name

</td><td>
Fehlertext

</td><td colspan="2">
Details

</td></tr><tr><td>
TECHNICAL_ERROR

</td><td>
Zufallszahl

</td><td colspan="2">
</td></tr><tr><td>
ASSERTION_INVALID

</td><td>
Authentifizierungsbestätigung ungültig 

</td><td colspan="2">
Die Authentifizierungsbestätigung des aufrufenden Nutzers wird nicht akzeptiert.

</td></tr><tr><td>
KEY_ERROR

</td><td>
Fehler im Schlüsseldatensatz

</td><td colspan="2">
Es ist bereits ein Datensatz vorhanden.

</td></tr><tr><td>
SYNTAX_ERROR

</td><td>
Fehlerhafte Aufrufparameter

</td><td colspan="2">
Es wurde ein fehlerhafter Aufrufparameter übergeben.

</td></tr><tr><td>
DEVICE_UNKNOWN

</td><td>
generierte

phr:DeviceID::Device

</td><td colspan="2">
Das vom Nutzer verwendete Gerät des Versicherten ist nicht bekannt und muss
freigeschaltet werden.

</td></tr></table>

**[\<=]**

### 6.2.4.2 Umsetzung I_Authorization_Management_Insurant::putAuthorizationKey

Die folgenden Anforderungen beschreiben die Umsetzung der
OperationI_Authorization_Management_Insurant::putAuthorizationKey. Dabei
gelten die übergreifenden Festlegungen zur Prüfung der Eingangsparameter.

**A_14446 - Komponente Autorisierung Vers. - Speicherung kryptografische
Berechtigung des Nutzers**

Die Komponente Autorisierung MUSS in
der OperationI_Authorization_Management_Insurant::putAuthorizationKeyden im
Eingangsparameter übergebenen AuthorizationKey alsAuthorizationKeyder
KeyChain des im Eingangsparameter benannten RecordIdentifier speichern,
sofern keinAuthorizationKeyfür die ActorID zu diesem RecordIdentifier bereits
vorhanden ist, und andernfalls die Operation mit der Fehlermeldung  KEY_ERROR
abbrechen. **[\<=]**

**A_14447 - Komponente Autorisierung Vers. - Berechtigungsprüfung
Schlüsselhinterlegung**

Die Komponente Autorisierung MUSS beim Aufruf der
Operation I_Authorization_Management_Insurant::putAuthorizationKey anhand der
subject-id (KVNR)der AuthenticationAssertion und
des RecordIdentifierprüfen, ob für den aufrufenden Nutzer ein
AuthorizationKey mit ActorID = KVNR hinterlegt ist und falls nicht, die
Operation mit dem Fehler ACCESS_DENIED abbrechen. **[\<=]**

Mit dieser Prüfung wird sichergestellt, dass nur Versicherte sowie berechtigte
Vertreter Schlüsselmaterial für Versicherte, 
Leistungserbringerinstitutionen und Kostenträger hinterlegen können, die
selbst bereits über einen AuthorizationKey verfügen.

**A_21541 - Komponente Autorisierung Vers. – Einrichten
Vertretungsberechtigung nicht durch einen Vertreter**

Die Komponente Autorisierung MUSS das Einrichten einer Vertretungsberechtigung
durch den Aufruf der
Operation I_Authorization_Management_Insurant::putAuthorizationKey mit
(subject-id der AuthenticationAssertion != ActorID des Übergabeparameters
AuthorizationKey und ActorID des Übergabeparameters AuthorizationKey !=
OwnerKVNR) ablehnen, wenn die subject-id der AuthenticationAssertion nicht der
OwnerKVNR des benannten RecordIdentifiers entspricht und die Operation mit dem
Fehler ACCESS_DENIED beenden. Mit dieser Prüfung wird verhindert, dass ein
Vertreter weitere Vertreter einrichten kann. **[\<=]**

**A_18184-01 - Komponente Autorisierung Vers. - Prüfung auf
Vertretungsberechtigung für Validierungsidentität**

Die Komponente Autorisierung MUSS bei einer Vertretungsberechtigung
sicherstellen, dass der Vertreter für ein Aktenkonto genau dann eine
Validierungsidentität gemäß [gemSpec_PK_eGK#Card-G2-A_3820] besitzt, wenn es
sich um ein Validierungsaktenkonto handelt. Ansonsten ist mit dem Fehler
TECHNICAL_ERROR abzubrechen. **[\<=]**

Hinweis: Das stellt sicher, dass auf „echte“ Konten ausschließlich
„echte“ Vertreter berechtigt werden und auf Validierungskonten
ausschließlich „Validierungs-Vertreter“. Die Erkennung auf eine
Validierungsidentität kann über die Auswertung der ActorID des zu
berechtigenden Vertreters erfolgen, wobei diese als Prüf-KVNR anhand der
Bildungsregel "4 oder mehr gleiche aufeinander folgende Ziffern" eindeutig zu
erkennen ist.

**A_17670 - Komponente Autorisierung Vers. - Freischaltprozess
Vertreterberechtigung**

Die Komponente Autorisierung MUSS bei Hinterlegung einer Vertretungsberechtigung
durch Aufruf der
Operation I_Authorization_Management_Insurant::putAuthorizationKeymit
(subject-id der AuthenticationAssertion != ActorID des Übergabeparameters
AuthorizationKey und ActorID des Übergabeparameters AuthorizationKey !=
OwnerKVNR) die Operation abschließen, sofern kein technischer oder fachlicher
Fehler dies verhindert und anschließend den Freischaltprozess für
Vertretereinrichtung starten ( ), sofern für die im Übergabeparameter
AuthorizationKey  benannte ActorID noch kein AuthorizationKey in der
Komponente Autorisierung für die im RecordIdentifierbenannte OwnerKVNR
vorhanden ist.  **[\<=]**

**A_18750 - Komponente Autorisierung Vers. - Begrenzung zu registrierender
Vertreter**

Die Komponente Autorisierung MUSS bei Hinterlegung einer Vertretungsberechtigung
durch Aufruf der
OperationI_Authorization_Management_Insurant::putAuthorizationKey(vgl. A_17670)
prüfen, ob die maximale Anzahl von fünf Vertretern erreicht wurde. Trifft
dies zu, MUSS der Anwendungsfall mit dem Fehler TECHNICAL_ERROR abgebrochen
werden. Eine Prüfung MUSS berücksichtigen, ob zum Zeitpunkt der
Vertretungsregistrierung Freischaltprozesse gestartet wurden bzw. im Gange
sind. Diese Prozesse sind in der maximalen Anzahl an Vertretern zu
berücksichtigen. **[\<=]**

**A_15752 - Komponente Autorisierung Vers. - Benachrichtigungskanal für
Geräteverwaltung E-Mail-Format**

Die Komponente Autorisierung MUSS die
OperationI_Authorization_Management_Insurant::putAuthorizationKeymit dem Fehler
SYNTAX_ERROR abbrechen, wenn der Parameter NotificationInfoRepresentativenicht
leer und nicht gemäß [RFC-5322]formatiert ist. **[\<=]**

**A_14318-01 - Komponente Autorisierung Vers. - Benachrichtigungskanal für
Geräteverwaltung**

Die Komponente Autorisierung MUSS einen in der
OperationI_Authorization_Management_Insurant::putAuthorizationKey übergebenen
optionalen Parameter NotificationInfoRepresentative als
Benachrichtigungsadresse der Geräteverwaltung für den im
ParameterAuthorizationKeydurch ActorID benannten Nutzer übernehmen, sofern
ActorID eine KVNR enthält, die nicht der OwnerKVNR entspricht, anderenfalls
ist der Parameter zu ignorieren. Für die Berechtigung eines Vertreters MUSS
dieser Parameter immer gesetzt sein und falls nicht, ist die Operation mit dem
Fehler SYNTAX_ERROR zu beenden. **[\<=]**

**A_14615 - Komponente Autorisierung Vers. - Initiale Schlüsselhinterlegung
Kontoeröffnung**

Die Komponente Autorisierung MUSS die
OperationI_Authorization_Management_Insurant::putAuthorizationKey mit dem
Fehler ACCESS_DENIED abbrechen, sofern für den Eigentümer der Akte noch kein
AuthorizationKey vorhanden ist, und der zu speicherndeAuthorizationKeydes
Aufrufparameters für einen anderen Nutzer als den Eigentümer
desRecordIdentifier (ActorID != OwnerKVNR) gespeichert werden soll. **[\<=]**

Mit dieser Anforderung soll verhindert werden, dass die Akte genutzt wird, bevor
das Schlüsselmaterial für den Versicherten erzeugt und hinterlegt wurde. Die
benannte Konstellation liegt im Rahmen der Kontoeröffnung und bei einem
Aktenumzug vor. Das Schlüsselmaterial für den Versicherten wird im Schritt
der Kontoaktivierung erzeugt, welcher auf den Schritt der Kontoinitialisierung
folgt.

**A_14736 - Komponente Autorisierung Vers. - Initiale Schlüsselhinterlegung
für den Versicherten**

Die Komponente Autorisierung MUSS bei Aufruf der
Operation I_Authorization_Management_Insurant::putAuthorizationKeydurch den
Versicherten (subject-id (KVNR) der AuthenticationAssertion == OwnerKVNR) im
Rahmen der initialen Schlüsselhinterlegung während der Kontoaktivierung
dasvalidTo-Datum des übergebenenAuthorizationKeyvor der Speicherung mit einem
technischen Datum gleichbedeutend mit "unendlich" (z.B.31.12.9999) ersetzen.
**[\<=]**

**A_15000-03 - Komponente Autorisierung Vers. - Zustandswechsel bei
Schlüsselhinterlegung für den Versicherten**

Die Komponente Autorisierung MUSS bei Aufruf der
Operation I_Authorization_Management_Insurant::putAuthorizationKeydurch den
Versicherten (subject-id (KVNR) der AuthenticationAssertion == OwnerKVNR) bei
erfolgreichem Abschluss der initialen Schlüsselhinterlegung für den
Versicherten während der Kontoaktivierung den ZustandRecordStateder KeyChain
des Versicherten vonREGISTEREDauf den WertACTIVATEDsetzen. **[\<=]**

### 6.2.4.3 Operationsdefinition I_Authorization_Management_Insurant::deleteAuthorizationKey

**A_14674-01 - Komponente Autorisierung -
I_Authorization_Management_Insurant::deleteAuthorizationKey**

Die Komponente Autorisierung MUSS die
Operation  I_Authorization_Management_Insurant::deleteAuthorizationKeygemäß
der folgenden Signatur implementieren:

Tabelle13: I_Authorization_Management_Insurant::deleteAuthorizationKey -
Definition

<table><tr><th>
Operation

</th><th colspan="3">
I_Authorization_Management_Insurant::deleteAuthorizationKey

</th></tr><tr><td>
Beschreibung

</td><td colspan="3">
Mit dieser Operation kann ein authentifizierter Nutzer bzw. ein berechtigter
Vertreter das im Aktenkonto hinterlegte kryptografische Schlüsselmaterial für
einen benannten Nutzer löschen.

</td></tr><tr><td>
Formatvorgaben

</td><td colspan="3">
Die Definition der Ein- und Ausgabeparameter erfolgt in
[AuthorizationService.xsd].

Diejenigen Parameter, die im XSD-Schema optional gekennzeichnet, aber hier nicht
aufgeführt sind, werden in der Operation an dieser Schnittstelle nicht
verwendet.

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

 ist eine von einem Identitiy Provider ausgestellte
Authentifizierungsbestätigung für einen Nutzer.

</td><td>
SAML Assertion  im SOAP-Header des Requests

</td><td>
-

</td></tr><tr><td>
RecordIdentifier

</td><td>
Der

RecordIdentifier

referenziert ein konkretes Aktenkonto eines Versicherten bei einem Anbieter. Mit
diesem wird der Datensatz der Autorisierung in der Komponente Autorisierung
für den anfragenden Nutzer lokalisiert.

</td><td>
RecordIdentifierType

</td><td>
-

</td></tr><tr><td>
ActorID

</td><td>
Identifikator des Nutzers, für den der hinterlegte Datensatz

AuthorizationKey

gelöscht werden soll.

</td><td>
String

</td><td>
-

</td></tr><tr><td>
DeviceID

</td><td>
Die DeviceID enthält die Gerätekennung eines vom Nutzer verwendeten Gerätes.

</td><td>
DeviceIdType

</td><td>
-

</td></tr><tr><td colspan="4">
Fehlermeldungen

</td></tr><tr><td>
Name

</td><td>
Fehlertext

</td><td colspan="2">
Details

</td></tr><tr><td>
TECHNICAL_ERROR

</td><td>
Zufallszahl

</td></tr><tr><td>
ASSERTION_INVALID

</td><td>
Authentifizierungsbestätigung ungültig 

</td><td colspan="2">
Die Authentifizierungsbestätigung des aufrufenden Nutzers wird nicht akzeptiert.

</td></tr><tr><td>
KEY_ERROR

</td><td>
Fehler im Schlüsseldatensatz

</td><td colspan="2">
Kein Datensatz vorhanden

</td></tr><tr><td>
ACCESS_DENIED

</td><td>
Zugriff verweigert

</td><td colspan="2">
Die Operation ist mit den angegebenen Parametern nicht zulässig.

</td></tr><tr><td>
DEVICE_UNKNOWN

</td><td>
generierte

phr:DeviceID::Device

</td><td colspan="2">
Das vom Nutzer verwendete Gerät des Versicherten ist nicht bekannt und muss
freigeschaltet werden.

</td></tr></table>

**[\<=]**

### 6.2.4.4 Umsetzung I_Authorization_Management_Insurant::deleteAuthorizationKey

Die folgenden Anforderungen beschreiben die Umsetzung der
OperationI_Authorization_Management_Insurant::deleteAuthorizationKey. Dabei
gelten die übergreifenden Festlegungen zur Prüfung der Eingangsparameter.

**A_14451 - Komponente Autorisierung Vers. - Prüfen Löschberechtigung**

Die Komponente Autorisierung MUSS bei Aufruf der
OperationI_Authorization_Management_Insurant::deleteAuthorizationKey prüfen,
ob der in derAuthenticationAssertionbenannte Nutzer über
einenAuthorizationKeymit AuthorizationType = DOCUMENT_AUTHORIZATION für den
benanntenRecordIdentifierverfügt, und andernfalls die Operation mit der
Fehlermeldung ACCESS_DENIED abbrechen. **[\<=]**

**A_21542 - Komponente Autorisierung Vers. – Löschen Vertretungsberechtigung
nicht durch einen Vertreter**

Die Komponente Autorisierung MUSS das Löschen einer Vertretungsberechtigung
durch den Aufruf der
Operation I_Authorization_Management_Insurant::deleteAuthorizationKeymit
(subject-id der AuthenticationAssertion != Übergabeparameter ActorID und
Übergabeparameter ActorID != OwnerKVNR) ablehnen, wenn die subject-id der
AuthenticationAssertion nicht der OwnerKVNR des benannten RecordIdentifiers
entspricht und die Operation mit dem Fehler ACCESS_DENIED beenden. Mit dieser
Prüfung wird verhindert, dass ein Vertreter Berechtigungen anderer Vertreter
löschen kann. **[\<=]**

**A_14452 - Komponente Autorisierung Vers. - Löschen des AuthorizationKeys**

Die Komponente Autorisierung MUSS bei Aufruf der
OperationI_Authorization_Management_Insurant::deleteAuthorizationKeyden
Datensatz AuthorizationKey des Nutzers löschen, der im Aufrufparameter
alsActorID (Telematik-ID oder KVNR für Vertreter) benannt wurde. **[\<=]**

**A_21704 - Komponente Autorisierung Vers. - Benachrichtigung des Versicherten
bei Löschen Vertreterschlüssel**

Löscht ein Vertreter seine eigene Vertreterberechtigung MUSS der Versicherte
darüber, mittels seiner hinterlegten E-Mail-Adresse, informiert werden.
**[\<=]**

**A_14453 - Komponente Autorisierung Vers. - Löschverbot für
Versichertenschlüssel**

Die Komponente Autorisierung MUSS bei Aufrufder
OperationI_Authorization_Management_Insurant::deleteAuthorizationKeydas
Löschen verhindern, wenn der im Aufrufparameter alsActorIDbenannte Datensatz
gleich derOwnerKVNRdes Versicherten als Eigentümer der Akte ist, und die
Operation mit der Fehlermeldung ACCESS_DENIED abbrechen. **[\<=]**

**A_14552-02 - Komponente Autorisierung Vers. - Löschen veralteter Schlüssel**

Die Komponente Autorisierung MUSS alle AuthorizationKey unverzüglich
löschen, derenvalidTo-Datum älter als die aktuelle Systemzeit der Komponente
Autorisierung sind unddas Löschen mit den folgenden Parametern als PHR-421
protokollieren:

 ---> UL

**[\<=]**

### 6.2.4.5 Operationsdefinition I_Authorization_Management_Insurant::replaceAuthorizationKey

**A_14325-02 - Komponente Autorisierung -
I_Authorization_Management_Insurant::replaceAuthorizationKey**

Die Komponente Autorisierung MUSS die
OperationI_Authorization_Management_Insurant::replaceAuthorizationKeygemäß
der folgenden Signatur implementieren:

Tabelle14: I_Authorization_Management_Insurant::replaceAuthorizationKey -
Definition

<table><tr><th>
Operation

</th><th colspan="3">
I_Authorization_Management_Insurant::replaceAuthorizationKey 

</th></tr><tr><td>
Beschreibung

</td><td colspan="3">
Mit dieser Operation kann ein authentifizierter Nutzer bzw. ein berechtigter
Vertreter das im Aktenkonto für einen benannten Nutzer hinterlegte
kryptografische Schlüsselmaterial  ersetzen. Die Operation kann insbesondere
dazu benutzt werden, den Berechtigungszeitraum für einen AuthorizationKey
anzupassen.

</td></tr><tr><td>
Formatvorgaben

</td><td colspan="3">
Die Definition der Ein- und Ausgabeparameter erfolgt in
[AuthorizationService.xsd].

Diejenigen Parameter, die im XSD-Schema optional gekennzeichnet, aber hier nicht
aufgeführt sind, werden in der Operation an dieser Schnittstelle nicht
verwendet.

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

ist eine von einem Identitiy Provider ausgestellte
Authentifizierungsbestätigung für einen Nutzer.

</td><td>
SAML Assertion  im SOAP-Header des Requests

</td><td>
-

</td></tr><tr><td>
RecordIdentifier

</td><td>
Der

RecordIdentifier

referenziert ein konkretes Aktenkonto eines Versicherten bei einem Anbieter. Mit
diesem wird der Datensatz der Autorisierung in der Komponente Autorisierung
für den anfragenden Nutzer lokalisiert.

</td><td>
RecordIdentifierType

</td><td>
-

</td></tr><tr><td>
NewAuthorizationKey

</td><td>
Die kryptografische Autorisierung eines Nutzers, bestehend aus Listen von
verschlüsselten Schlüsseln. Details zur Struktur finden sich im Kapitel 7
zum Informationsmodell.

</td><td>
AuthorizationKeyType

</td><td>
-

</td></tr><tr><td>
DeviceID

</td><td>
Die

DeviceID

enthält die Gerätekennung eines vom Nutzer verwendeten Gerätes.

</td><td>
DeviceIdType

</td><td>
-

</td></tr><tr><td colspan="4">
Fehlermeldungen 

</td></tr><tr><td>
Name

</td><td>
Fehlertext

</td><td colspan="2">
Details

</td></tr><tr><td>
TECHNICAL_ERROR

</td><td>
Zufallszahl

</td></tr><tr><td>
KEY_E

RROR

</td><td>
Fehler im Schlüsseldatensatz

</td><td colspan="2">
Kein Datensatz vorhanden.

</td></tr><tr><td>
ASSERTION_INVALID

</td><td>
Authentifizierungsbestätigung ungültig

</td><td colspan="2">
Die Authentifizierungsbestätigung des aufrufenden Nutzers wird nicht akzeptiert.

</td></tr><tr><td>
DEVICE_UNKNOWN

</td><td>
generierte

phr:DeviceID::Device

</td><td colspan="2">
Das vom Nutzer verwendete Gerät des Versicherten ist nicht bekannt und muss
freigeschaltet werden.

</td></tr><tr><td>
ACCESS_DEN

IED

</td><td>
Zugriff verweigert

</td><td colspan="2">
Die Operation ist mit den angegebenen Parametern nicht zulässig.

</td></tr></table>

**[\<=]**

### 6.2.4.6 Umsetzung I_Authorization_Management_Insurant::replaceAuthorizationKey

Die folgenden Anforderungen beschreiben die Umsetzung der
OperationI_Authorization_Management_Insurant::replaceAuthorizationKey. Dabei
gelten die übergreifenden Festlegungen zur Prüfung der Eingangsparameter.

**A_14454 - Komponente Autorisierung Vers. - Prüfung Datensatz für bestehenden
AuthorizationKey**

Die Komponente Autorisierung MUSS für die
OperationI_Authorization_Management_Insurant::replaceAuthorizationKeyprüfen,
ob einAuthorizationKeyfür den benannten RecordIdentifier und den in
derAuthenticationAssertionbenannten Nutzer (subject-id == ActorID des
vorhandenen AuthorizationKey) hinterlegt ist, und andernfalls die Operation mit
der Fehlermeldung ACCESS_DENIED abbrechen. **[\<=]**

**A_21543 - Komponente Autorisierung Vers. – Ändern Vertretungsberechtigung
nicht durch einen Vertreter**

Die Komponente Autorisierung MUSS das Ändern einer Vertretungsberechtigung
durch den Aufruf der
Operation I_Authorization_Management_Insurant::replaceAuthorizationKeymit
(subject-id der AuthenticationAssertion != ActorID des Übergabeparameters
NewAuthorizationKey und ActorID des Übergabeparameters NewAuthorizationKey !=
OwnerKVNR) ablehnen, wenn die subject-id der AuthenticationAssertion nicht der
OwnerKVNR des benannten RecordIdentifiers entspricht und die Operation mit dem
Fehler ACCESS_DENIED beenden. Mit dieser Prüfung wird verhindert, dass ein
Vertreter Berechtigungen anderer Vertreter ändern kann. **[\<=]**

**A_21544 - Komponente Autorisierung Vers. - Änderung des Schlüsselmaterials
des Versicherten nur durch den Versicherten selbst**

Die Komponente Autorisierung MUSS das Ändern des Schlüsselmaterial des
Versicherten durch den Aufruf der
Operation I_Authorization_Management_Insurant::replaceAuthorizationKey ablehnen
und die Operation mit dem Fehler ACCESS_DENIED beenden, wenn (subject-id der
AuthenticationAssertion != OwnerKVNR und ActorID des Übergabeparameters
NewAuthorizationKey == OwnerKVNR) gilt. **[\<=]**

**A_14455 - Komponente Autorisierung Vers. - Ersetzen des AuthorizationKeys**

Die Komponente Autorisierung MUSS bei Aufruf der
OperationI_Authorization_Management_Insurant::replaceAuthorizationKeyden
DatensatzAuthorizationKeydesjenigen Nutzers durch den
übergebenenNewAuthorizationKeyersetzen, der im Aufrufparameter
alsActorID (Telematik-ID oder KVNR) benannt wurde und für den
ein AuthorizationKeyvorhanden ist. **[\<=]**

### 6.2.4.7 Operationsdefinition I_Authorization_Management_Insurant::getAuditEvents

**A_14676-05 - Komponente Autorisierung -
I_Authorization_Management_Insurant::getAuditEvents**

Die Komponente Autorisierung MUSS die
Operation I_Authorization_Management_Insurant::getAuditEventsgemäß der
folgenden Signatur implementieren:

Tabelle15: I_Authorization_Management_Insurant::getAuditEvents - Definition

<table><tr><th>
Operation

</th><th colspan="3">
I_Authorization_Management_Insurant::getAuditEvents

</th></tr><tr><td>
Beschreibung

</td><td colspan="3">
Mit dieser Operation kann ein authentifizierter Versicherter bzw. ein
berechtigter Vertreter das Verwaltungsprotokoll der Autorisierungskomponente
auslesen. 

</td></tr><tr><td>
Formatvorgaben

</td><td colspan="3">
Die Definition der Ein- und Ausgabeparameter erfolgt in
[AuthorizationService.xsd].

Diejenigen Parameter, die im XSD-Schema optional gekennzeichnet, aber hier nicht
aufgeführt sind, werden in der Operation an dieser Schnittstelle nicht
verwendet.

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

 ist eine von einem Identitiy Provider ausgestellte
Authentifizierungsbestätigung für einen Nutzer.

</td><td>
SAML Assertion im SOAP-Header des Requests

</td><td>
-

</td></tr><tr><td>
RecordIdentifier

</td><td>
Der

RecordIdentifier

referenziert ein konkretes Aktenkonto eines Versicherten bei einem Anbieter. Mit
diesem wird der Datensatz der Autorisierung in der Komponente Autorisierung
für den anfragenden Nutzer lokalisiert.

</td><td>
RecordIdentifierType

</td><td>
-

</td></tr><tr><td>
DeviceID

</td><td>
Die DeviceID enthält die Gerätekennung eines vom Nutzer verwendeten Gerätes.

</td><td>
DeviceIdType 

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

 oder

YYYY-MM-DDThh:mm:ss

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
Liste der Verwaltungsprotokolleinträge des im RecordIdentifier referenzierten
Aktenkontos

</td><td>
AuditMessage [0..*]

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
TECHNICAL_ERROR

</td><td>
Zufallszahl

</td></tr><tr><td>
ASSERTION_INVALID

</td><td>
Authentifizierungsbestätigung ungültig 

</td><td colspan="2">
Die Authentifizierungsbestätigung des aufrufenden Nutzers wird nicht akzeptiert.

</td></tr><tr><td>
DEVICE_UNKNOWN

</td><td>
generierte

phr:DeviceID::Device

</td><td colspan="2">
Das vom Nutzer verwendete Gerät des Versicherten ist nicht bekannt und muss
freigeschaltet werden.

</td></tr><tr><td>
SYNTAX_ERROR

</td><td>
Fehlerhafte Aufrufparameter.

</td><td colspan="2" rowspan="1">
Es wurde ein fehlerhafter Aufrufparameter übergeben.

</td></tr></table>

**[\<=]**

### 6.2.4.8 Umsetzung I_Authorization_Management_Insurant::getAuditEvents

Die folgenden Anforderungen beschreiben die Umsetzung der
OperationI_Authorization_Management_Insurant::getAuditEvents. Dabei gelten die
übergreifenden Festlegungen zur Prüfung der Eingangsparameter.

**A_14394-01 - Komponente Autorisierung Vers. - Auslesen Verwaltungsprotokoll**

Die Komponente Autorisierung MUSS beim Aufruf der
OperationI_Authorization_Management_Insurant::getAuditEvents dem anhand
einerAuthenticationAssertionauthentifizierten Nutzer die Liste aller zum
angefragtenRecordIdentifierverfügbaren Verwaltungsprotokolleinträge gemäß
[gemSpec_DM_ePA#A_14471-*] zurückliefern, wenn der Wert
von DeviceID::Devicedes Aufrufparameters gleich dem Wert
"urn:gematik:fa:phr:1.0:device:device-id" einer für diesen Nutzer
ausgestellten Autorisierungsbestätigungist. **[\<=]**

Damit wird sichergestellt, dass das Auslesen des Verwaltungsprotokolls nur
gestattet wird, wenn zuvor eine Autorisierungsbestätigung für diesen Nutzer
ausgestellt wurde.

### 6.2.4.9 Operationsdefinition I_Authorization_Management_Insurant::getSignedAuditEvents

**A_21165-04 - Komponente Autorisierung -
I_Authorization_Management_Insurant::getSignedAuditEvents**

Die Komponente Autorisierung MUSS die
Operation I_Authorization_Management_Insurant::getSignedAuditEventsgemäß der
folgenden Signatur implementieren:

Tabelle16: I_Authorization_Management_Insurant::getSignedAuditEvents - Definition

<table><tr><th>
Operation

</th><th colspan="3">
I_Authorization_Management_Insurant::getSignedAuditEvents

</th></tr><tr><td>
Beschreibung

</td><td colspan="3">
Mit dieser Operation kann ein authentifizierter Versicherter bzw. ein be

rechtigter Vertreter eine signierte Liste der Verwaltungsprotokolle des
Versicherten aus de

r Autorisierungskomponente auslesen. 

</td></tr><tr><td>
Formatvorgaben

</td><td colspan="3">
Die Definition der Ein- und Ausgabeparameter erfolgt in
[AuthorizationService.xsd].

Diejenigen Parameter, die im XSD-Schema optional gekennzeichnet, aber hier nicht
aufgeführt sind, werden in der Operation an dieser Schnittstelle nicht
verwendet.

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

 ist eine von einem Identitiy Provider ausgestellte
Authentifizierungsbestätigung für einen Nutzer.

</td><td>
SAML Assertion im SOAP-Header des Requests

</td><td>
-

</td></tr><tr><td>
RecordIdentifier

</td><td>
Der

RecordIdentifier

referenziert ein konkretes Aktenkonto eines Versicherten bei einem Anbieter. Mit
diesem wird der Datensatz der Autorisierung in der Komponente Autorisierung
für den anfragenden Nutzer lokalisiert.

</td><td>
RecordIdentifierType

</td><td>
-

</td></tr><tr><td>
DeviceID

</td><td>
Die DeviceID enthält die Gerätekennung eines vom Nutzer verwendeten Gerätes.

</td><td>
DeviceIdType 

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

 oder

YYYY-MM-DDThh:mm:ss

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
 

 

Signed

AuditEventList

</td><td>
Signierte Liste (Teilliste bei Verwendung der Paging-Parameter) der
Verwaltungsprotokolleinträge des im RecordIdentifier referenzierten Aktenkontos

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
TECHNICAL_ERROR

</td><td>
Zufallszahl

</td></tr><tr><td>
ASSERTION_INVALID

</td><td>
Authentifizierungsbestätigung ungültig 

</td><td colspan="2">
Die Authentifizierungsbestätigung des aufrufenden Nutzers wird nicht akzeptiert.

</td></tr><tr><td>
DEVICE_UNKNOWN

</td><td>
generierte

phr:DeviceID::Device

</td><td colspan="2">
Das vom Nutzer verwendete Gerät des Versicherten ist nicht bekannt und muss
freigeschaltet werden.

</td></tr><tr><td>
SYNTAX_ERROR

</td><td>
Fehlerhafte Aufrufparameter.

</td><td colspan="2" rowspan="1">
Es wurde ein fehlerhafter Aufrufparameter übergeben.

</td></tr></table>

**[\<=]**

### 6.2.4.10 Umsetzung I_Authorization_Management_Insurant::getSignedAuditEvents

Die folgenden Anforderungen beschreiben die Umsetzung der
OperationI_Authorization_Management_Insurant::getSignedAuditEvents. Dabei
gelten die übergreifenden Festlegungen zur Prüfung der Eingangsparameter.

**A_21166-01 - Komponente Autorisierung - signiertes Verwaltungsprotokoll
erstellen**

Die Komponente Autorisierung MUSS beim Aufruf der Operation
I_Authorization_Management_Insurant::getSignedAuditEvents dem anhand einer
AuthenticationAssertion authentifizierten Nutzer ein signiertes Dokument
zurückliefern,

 ---> UL

wenn der Wert von DeviceID::Device des Aufrufparameters gleich dem Wert
"urn:gematik:fa:phr:1.0:device:device-id" einer für diesen Nutzer
ausgestellten Autorisierungsbestätigung ist.  Hinweis: Es ist zulässig die
Verwaltungsprotokolleinträge auf mehrere Dokumente aufzuteilen **[\<=]**

Damit wird sichergestellt, dass das Auslesen des Verwaltungsprotokolls nur
gestattet wird, wenn zuvor eine Autorisierungsbestätigung für diesen Nutzer
ausgestellt wurde.

Es wird das gesamte Dokument bzw. Dokumente signiert. Das Format soll dem von
Audit Events entsprechen.

### 6.2.4.11 Operationsdefinition I_Authorization_Management_Insurant::putNotificationInfo

**A_14344-01 - Komponente Autorisierung -
I_Authorization_Management_Insurant::putNotificationInfo**

Die Komponente Autorisierung MUSS die
Operation I_Authorization_Management_Insurant::putNotificationInfogemäß der
folgenden Signatur implementieren:

Tabelle17: I_Authorization_Management_Insurant::putNotificationInfo - Definition

<table><tr><th>
Operation

</th><th colspan="3">
I_Authorization_Management_Insurant::putNotificationInfo

</th></tr><tr><td>
Beschreibung

</td><td colspan="3">
Mit dieser Operation kann ein authentifizierter Versicherter bzw. ein
berechtigter Vertreter seine im Benachrichtigungskanal hinterlegte Adresse
aktualisieren.

</td></tr><tr><td>
Formatvorgaben

</td><td colspan="3">
Die Definition der Ein- und Ausgabeparameter erfolgt in
[AuthorizationService.xsd].

Diejenigen Parameter, die im XSD-Schema optional gekennzeichnet, aber hier nicht
aufgeführt sind, werden in der Operation an dieser Schnittstelle nicht
verwendet.

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

ist eine von einem Identitiy Provider ausgestellte
Authentifizierungsbestätigung für einen Nutzer.

</td><td>
SAML Assertion im SOAP-Header des Requests

</td><td>
-

</td></tr><tr><td>
RecordIdentifier

</td><td>
Der

RecordIdentifier

referenziert ein konkretes Aktenkonto eines Versicherten bei einem Anbieter. Mit
diesem wird der Datensatz der Autorisierung in der Komponente Autorisierung
für den anfragenden Nutzer lokalisiert.

</td><td>
RecordIdentifierType

</td><td>
-

</td></tr><tr><td>
DeviceID

</td><td>
Die

DeviceID

enthält die Gerätekennung eines vom Nutzer verwendeten Gerätes.

</td><td>
DeviceIdType 

</td><td>
-

</td></tr><tr><td>
NewNotificationInfo

</td><td>
NewNotificationInfo

beinhaltet die neue Benachrichtigungsadresse, die für den authentifizierten
Nutzer gespeichert werden soll.

</td><td>
String

</td><td>
-

</td></tr><tr><td colspan="4">
Fehlermeldungen 

</td></tr><tr><td>
Name

</td><td>
Fehlertext

</td><td colspan="2">
Details

</td></tr><tr><td>
TECHNICAL_ERROR

</td><td>
Zufallszahl

</td><td colspan="2">
</td></tr><tr><td>
SYNTAX_ERROR

</td><td>
Fehlerhafte Aufrufparameter

</td><td colspan="2">
Es wurde ein fehlerhafter Aufrufparameter übergeben.

</td></tr><tr><td>
DEVICE_UNKNOWN

</td><td>
generierte

phr:DeviceID::Device

</td><td colspan="2">
Das vom Nutzer verwendete Gerät des Versicherten ist nicht bekannt und muss
freigeschaltet werden.

</td></tr><tr><td>
ACCESS_DE

NIED

</td><td>
Zugriff verweigert

</td><td colspan="2">
Die Operation ist mit den angegebenen Parametern nicht zulässig.

</td></tr></table>

**[\<=]**

### 6.2.4.12 Umsetzung I_Authorization_Management_Insurant::putNotificationInfo

Die folgenden Anforderungen beschreiben die Umsetzung der
OperationI_Authorization_Management_Insurant::putNotificationInfo. Dabei gelten
die übergreifenden Festlegungen zur Prüfung der Eingangsparameter.

**A_14715-02 - Komponente Autorisierung Vers. - Aktualisierung
Benachrichtigungsadresse**

Die Komponente Autorisierung MUSS bei Aufruf der Operation
I_Authorization_Management_Insurant::putNotificationInfo den Wert des
Parameters NewNotificationInfo als Benachrichtigungsadresse des in
derAuthenticationAssertionbenannten Nutzers für den hinterlegten
AuthorizationKey des Nutzers(subject-idder AuthenticationAssertion== ActorIDdes
AuthorizationKey) speichern. **[\<=]**

**A_14716 - Komponente Autorisierung Vers. - E-Mail-Format**

Die Komponente Autorisierung MUSS die
Operation I_Authorization_Management_Insurant::putNotificationInfomit dem
Fehler SYNTAX_ERROR abbrechen, wenn der Parameter NewNotificationInfonicht
gemäß [RFC-5322] formatiert ist. **[\<=]**

Mit dieser Funktion kann ein Versicherter oder ein berechtigter Vertreter seine
persönliche Benachrichtigungsadresse zur Gerätefreischaltung ändern. Sowohl
für Versicherte als auch deren berechtigte Vertreter sind vor deren jeweiligem
Zugriff Benachrichtigungsadressen vorhanden, da diese Operation ohne
Gerätefreischaltung über ihre Adresse nicht aufrufbar ist.

Für Versicherte wird die Benachrichtigungsadresse initial im Rahmen der
Kontoeröffnung hinterlegt. Für Vertreter erfolgt die initiale Hinterlegung
der Benachrichtigungsadresse durch den Versicherten
mittelsI_Authorization_Management_Insurant::putAuthorizationKeywährend der
Vergabe der Zugriffsberechtigung.

### 6.2.4.13 Operationsdefinition I_Authorization_Management_Insurant::getNotificationInfo

Mit dieser Operation kann ein Versicherter die Email-Adressen einsehen, die
Nutzern zugeordnet sind, die über eine Zugriffsberechtigung für das Konto des
Versicherten (Akteninhabers) verfügen, also die eigene Email-Adresse und die
seiner Vertreter.

**A_21250-01 - Komponente Autorisierung -
I_Authorization_Management_Insurant::getNotificationInfo**

Die Komponente Autorisierung MUSS die
Operation I_Authorization_Management_Insurant::getNotificationInfo gemäß
der folgenden Signatur implementieren:

Tabelle18:  I_Authorization_Management_Insurant::getNotificationInfo -
Definition

<table><tr><td>
Operation

</td><td colspan="3">
I

_Authorization_Management_Insurant::getNotificationInfo

</td></tr><tr><td>
Beschreibung

</td><td colspan="3">
Mit dieser Operation kann ein authentifizierter Versicherter die an seinem Konto
hinterlegten Benachrichtigungskanal - Adressen  abfragen.

</td></tr><tr><td>
Formatvorgaben

</td><td colspan="3">
Die Definition der Ein- und Ausgabeparameter erfolgt in
[AuthorizationService.xsd].

Diejenigen Parameter, die im XSD-Schema optional gekennzeichnet, aber hier nicht
aufgeführt sind, werden in der Operation an dieser Schnittstelle nicht
verwendet.

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

ist eine von einem Identitiy Provider ausgestellte
Authentifizierungsbestätigung für einen Nutzer (Akteninhaber).

</td><td>
SAML Assertion im SOAP-Header des Requests

</td><td>
-

</td></tr><tr><td>
RecordIdentifier

</td><td>
Der

RecordIdentifier

referenziert ein konkretes Aktenkonto eines Versicherten bei einem Anbieter. Mit
diesem wird der Datensatz der Autorisierung in der Komponente Autorisierung
für den anfragenden Nutzer lokalisiert.

</td><td>
 RecordIdentifierType

</td><td>
 -

</td></tr><tr><td>
DeviceID

</td><td>
Die

DeviceID

enthält die Gerätekennung eines vom Nutzer verwendeten Gerätes.

</td><td>
DeviceIdType 

</td><td>
-

</td></tr><tr><td>
ActorID

</td><td>
Identifikator des Nutzers (Vertreter oder Akteninhaber), dessen
Benachrichtigungsadresse ausgegeben werden soll. Soll die Liste aller
Benachrichtigungskanäle zurückgegeben werden, wird ActorID leer gelassen.

</td><td>
String 

</td><td>
ja

</td></tr><tr><td colspan="4">
Ausgangsparameter

</td></tr><tr><td>
NotificationInfoList

</td><td>
NotificationInfoList

beinhaltet die Benachrichtigungskanäle (ActorID und Benachrichtigungsadresse),
die entweder zur angefragten ActorID oder aber im Aktenkonto insgesamt
hinterlegt sind.

</td><td>
NotificationInfoListType

</td><td>
-

</td></tr><tr><td colspan="4">
Fehlermeldungen 

</td></tr><tr><td>
Name

</td><td>
Fehlertext

</td><td colspan="2">
Details

</td></tr><tr><td>
TECHNICAL_ERROR

</td><td>
Zufallszahl

</td></tr><tr><td>
SYNTAX_ERROR

</td><td>
Fehlerhafte Aufrufparameter

</td><td colspan="2">
Es wurde ein fehlerhafter Aufrufparameter übergeben.

</td></tr><tr><td>
ACTOR_UNKNOWN

</td><td>
unbekannte ActorID

</td><td colspan="2">
Die ActorID ist im angegebenen Aktenkonto nicht bekannt.

</td></tr><tr><td>
DEVICE_UNKNOWN

</td><td>
generierte

phr:DeviceID::Device

</td><td colspan="2" rowspan="1">
Das vom Nutzer verwendete Gerät des Versicherten ist nicht bekannt und muss
freigeschaltet werden.

</td></tr><tr><td>
ACCESS_DENIED

</td><td>
Zugriff verweigert

</td><td colspan="2">
Die Operation ist mit den angegebenen Parametern nicht zulässig.

</td></tr></table>

**[\<=]**

### 6.2.4.14 Umsetzung I_Authorization_Management_Insurant::getNotificationInfo

Bei der Umsetzung der
OperationI_Authorization_Management_Insurant::getNotificationInfo gelten die
übergreifenden Festlegungen zur Prüfung der Eingangsparameter.

**A_21722 - Komponente Autorisierung Vers. - Berechtigung für
getNotificationInfo**

Die Komponente Autorisierung MUSS bei Aufruf der
OperationI_Authorization_Management_Insurant::getNotificationInfo prüfen, ob
für den in der AuthenticationAssertion benannten User ein AuthorizationKey in
der Keychain der mittels RecordIdentifier benannten Akte vorhanden ist und
andernfalls die Operation mit ACCESS_DENIED abbrechen.  **[\<=]**

**A_21252-01 - Komponente Autorisierung – Abfrage Benachrichtigungsadresse**

Die Komponente Autorisierung MUSS bei Aufruf der
OperationI_Authorization_Management_Insurant::getNotificationInfo für das
über RecordIdentifier referenzierte Aktenkontoentweder alle
Benachrichtigungskanäle oder aber den im Parameter ActorID angefragten
Benachrichtigungskanal zurück geben. Ist der in der AuthenticationAssertion
benannte Nutzer nicht Eigentümer der Akte, also ein Vertreter, MUSS immer
ausschließlich der Benachrichtigungskanal dieses Nutzers zurück gegeben
werden.  **[\<=]**

### 6.2.4.15 Operationsdefinition I_Authorization_Management_Insurant::getKtrTelematikID

**A_21559 - Komponente Autorisierung -
I_Authorization_Management_Insurant::getKtrTelematikID**

Die Komponente Autorisierung MUSS die
Operation I_Authorization_Management_Insurant::getKtrTelematikIDgemäß der
folgenden Signatur implementieren:

Tabelle19: I_Authorization_Management_Insurant::getAuthorizationList - Definition

<table><tr><th>
Operation

</th><th colspan="3">
I_Authorization_Management_Insurant::getKtrTelematikID

</th></tr><tr><td>
Beschreibung

</td><td colspan="3">
Die Operation liefert die TelematikID des Kostenträgers, der das Kontos
im Aktensystems anbietet.

</td></tr><tr><td>
Formatvorgaben

</td><td colspan="3">
Die Definition der Ein- und Ausgabeparameter erfolgt in
[AuthorizationService.xsd].

Diejenigen Parameter, die im XSD-Schema optional gekennzeichnet, aber hier nicht
aufgeführt sind, werden in der Operation an dieser Schnittstelle nicht
verwendet.

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

 ist eine von einem Identitiy Provider ausgestellte
Authentifizierungsbestätigung für einen Nutzer.

</td><td>
SAML Assertion im SOAP-Header des Requests

</td><td>
-

</td></tr><tr><td>
RecordIdentifier

</td><td>
Der

RecordIdentifier

referenziert ein konkretes Aktenkonto eines Versicherten bei einem Anbieter. Mit
diesem wird der Datensatz der Autorisierung in der Komponente Autorisierung
für den anfragenden Nutzer lokalisiert.

</td><td>
RecordIdentifierType

</td><td>
-

</td></tr><tr><td>
DeviceID

</td><td>
Die

DeviceID

enthält die Gerätekennung eines vom Nutzer verwendeten Gerätes.

</td><td>
DeviceIdType 

</td><td>
-

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
KtrTelematikID

 

</td><td>
Telematik-ID des Kostenträgers, der das Aktenkonto anbietet.

</td><td>
String

</td><td>
-

</td></tr><tr><td colspan="4">
Fehlermeldungen

</td></tr><tr><td>
Name

</td><td>
Fehlertext

</td><td colspan="2">
Details

</td></tr><tr><td>
TECHNICAL_ERROR

</td><td>
Zufallszahl

</td></tr><tr><td>
DEVICE_UNKNOWN

</td><td>
generierte

phr:DeviceID::Device

</td><td colspan="2">
Das vom Nutzer verwendete Gerät des Versicherten ist nicht bekannt und muss
freigeschaltet werden.

</td></tr><tr><td>
ACCESS_DENIED

</td><td>
Zugriff verweigert

</td><td colspan="2">
Die Operation ist mit den angegebenen Parametern nicht zulässig.

</td></tr></table>

**[\<=]**

### 6.2.4.16 Umsetzung I_Authorization_Management_Insurant::getKtrTelematikID

**A_21560 - Komponente Autorisierung Vers. - Berechtigung für
getKtrTelematikID**

Die Komponente Autorisierung MUSS bei Aufruf der
Operation I_Authorization_Management_Insurant::getKtrTelematikID prüfen, ob
für den in der AuthenticationAssertion benannten User ein AuthorizationKey in
der Keychain der mittels RecordIdentifier benannten Akte vorhanden ist
(subject-id==ActorID) und andernfalls die Operation mit ACCESS_DENIED
abbrechen.  **[\<=]**

### 6.2.4.17 Operationsdefinition I_Authorization_Management_Insurant::getAuthorizationList

**A_17113-01 - Komponente Autorisierung -
I_Authorization_Management_Insurant::getAuthorizationList**

Die Komponente Autorisierung MUSS die
Operation I_Authorization_Management_Insurant::getAuthorizationListgemäß der
folgenden Signatur implementieren:

Tabelle20: I_Authorization_Management_Insurant::getAuthorizationList - Definition

<table><tr><th>
Operation

</th><th colspan="3">
I_Authorization_Management_Insurant::getAuthorizationList

</th></tr><tr><td>
Beschreibung

</td><td colspan="3">
Die Operation liefert eine Liste aller AuthorizationKeys eines Kontos
im Aktensystems, als Liste aller Berechtigten in einem Aktenkonto.

</td></tr><tr><td>
Formatvorgaben

</td><td colspan="3">
Die Definition der Ein- und Ausgabeparameter erfolgt in
[AuthorizationService.xsd].

Diejenigen Parameter, die im XSD-Schema optional gekennzeichnet, aber hier nicht
aufgeführt sind, werden in der Operation an dieser Schnittstelle nicht
verwendet.

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

 ist eine von einem Identitiy Provider ausgestellte
Authentifizierungsbestätigung für einen Nutzer.

</td><td>
SAML Assertion im SOAP-Header des Requests

</td><td>
-

</td></tr><tr><td>
RecordIdentifier

</td><td>
Der

RecordIdentifier

referenziert ein konkretes Aktenkonto eines Versicherten bei einem Anbieter. Mit
diesem wird der Datensatz der Autorisierung in der Komponente Autorisierung
für den anfragenden Nutzer lokalisiert.

</td><td>
RecordIdentifierType

</td><td>
-

</td></tr><tr><td>
DeviceID

</td><td>
Die

DeviceID

enthält die Gerätekennung eines vom Nutzer verwendeten Gerätes.

</td><td>
DeviceIdType 

</td><td>
-

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
AuthorizationKeyList

 

</td><td>
Liste der AuthorizationKeys des per RecordIdentifier identifizierten Kontos.

</td><td>
AuthorizationKeyType[0..*]

</td><td>
-

</td></tr><tr><td colspan="4">
Fehlermeldungen

</td></tr><tr><td>
Name

</td><td>
Fehlertext

</td><td colspan="2">
Details

</td></tr><tr><td>
TECHNICAL_ERROR

</td><td>
Zufallszahl

</td><td colspan="2">
</td></tr><tr><td>
DEVICE_UNKNOWN

</td><td>
generierte

phr:DeviceID::Device

</td><td colspan="2">
Das vom Nutzer verwendete Gerät des Versicherten ist nicht bekannt und muss
freigeschaltet werden.

</td></tr><tr><td>
ACCESS_DENIED

</td><td>
Zugriff verweigert

</td><td colspan="2">
Die Operation ist mit den angegebenen Parametern nicht zulässig.

</td></tr></table>

**[\<=]**

### 6.2.4.18 Umsetzung I_Authorization_Management_Insurant::getAuthorizationList

**A_17115 - Komponente Autorisierung Vers. - Berechtigung für
Berechtigungsliste**

Die Komponente Autorisierung MUSS bei Aufruf der
OperationI_Authorization_Management_Insurant::getAuthorizationListprüfen, ob
für den in der AuthenticationAssertion benannten User ein AuthorizationKey in
der Keychain der mittels RecordIdentifier benannten Akte vorhanden ist
(subject-id==ActorID) und andernfalls die Operation mit ACCESS_DENIED
abbrechen.  **[\<=]**

**A_17114-01 - Komponente Autorisierung Vers. - Abfrage Berechtigungsliste**

Die Komponente Autorisierung MUSS bei Aufruf
der OperationI_Authorization_Management_Insurant::getAuthorizationListdie
Liste aller AuthorizationKey in der KeyChain der im RecordIdentifier benannten
Akte mit Ausnahme des AuthorizationKey des Eigentümers der Akte (für alle
zurückgegebenen AuthorizationKey MUSS gelten: ActorID!=OwnerKVNR) in der
folgenden Struktur zurückgebenDie Elemente Ciphertext und AssociatedData
innerhalb des Elements EncryptedKeyContainer MÜSSEN mit einem Leer-String
belegt werden. **[\<=]**

### 6.2.4.19 Operationsdefinition I_Authorization_Management_Insurant::startKeyChange

**A_20480-02 - Komponente Autorisierung -
I_Authorization_Management_Insurant::startKeyChange**

Die Komponente Autorisierung MUSS die
Operation I_Authorization_Management_Insurant::startKeyChangegemäß der
folgenden Signatur implementieren:

Tabelle21: Tab_Autorisierung -
Operation I_Authorization_Management_Insurant::startKeyChange Definition

<table><tr><th colspan="2">
Operation

</th><th colspan="4">
I_Authorization_Management_Insurant::startKeyChange

</th></tr><tr><td colspan="2">
Beschreibung

</td><td colspan="4">
Mit dieser Operation kann der Versicherte den Prozess der Umschlüsselung an der
Komponente Autorisierung initiieren und die Autorisierungskomponente bis zur
Beendigung der Verarbeitung sperren.

</td></tr><tr><td colspan="2">
Formatvorgaben

</td><td colspan="4">
Die Definition der Ein- und Ausgabeparameter erfolgt in
[AuthorizationService.xsd].

Diejenigen Parameter, die im XSD-Schema optional gekennzeichnet, aber hier nicht
aufgeführt sind, werden in der Operation an dieser Schnittstelle nicht
verwendet.

</td></tr><tr><td colspan="6">
Eingangsparameter

</td></tr><tr><td colspan="2">
 Name

</td><td colspan="2">
 Beschreibung

</td><td>
Typ

</td><td>
opt.

</td></tr><tr><td colspan="2" rowspan="1">
AuthenticationAssertion

</td><td colspan="2" rowspan="1">
Die AuthenticationAssertion ist eine von einem Identitiy Provider ausgestellte
Authentifizierungsbestätigung für einen Nutzer.

</td><td>
SAML Assertion im SOAP-Header des Requests

</td><td>
-

</td></tr><tr><td colspan="2" rowspan="1">
RecordIdentifier

</td><td colspan="2" rowspan="1">
Der

RecordIdentifier

referenziert ein konkretes Aktenkonto eines Versicherten bei einem Anbieter. Mit
diesem wird der Datensatz der Autorisierung in der Komponente Autorisierung
für den anfragenden Nutzer lokalisiert.

 

</td><td>
RecordIdentifierType

</td><td>
-

</td></tr><tr><td colspan="6">
Technische Fehlermeldungen 

</td></tr><tr><td colspan="2" rowspan="1">
Name

</td><td colspan="2">
Fehlertext

</td><td colspan="2">
Details

</td></tr><tr><td colspan="2" rowspan="1">
TECHNICAL_ERROR

</td><td colspan="2">
Zufallszahl

</td><td colspan="2">
Interner Fehler in der Verarbeitungslogik

</td></tr><tr><td colspan="2" rowspan="1">
ASSERTION_INVALID

</td><td colspan="2">
Die übergebene Authentication Assertion ist ungültig

</td><td colspan="2">
Die Authentifizierungsbestätigung des aufrufenden Nutzers wird nicht akzeptiert.

</td></tr><tr><td colspan="2" rowspan="1">
ACCESS_DENIED

</td><td colspan="2" rowspan="1">
Der Zugriff für diese Operation konnte nicht gewährt werden.

</td><td colspan="2" rowspan="1">
Die Operation ist mit den angegebenen Parametern nicht zulässig.

</td></tr></table>

**[\<=]**

### 6.2.4.20 Umsetzung I_Authorization_Management_Insurant::startKeyChange

**A_21670-01 - Komponente Autorisierung - Aufruf startKeyChange nur durch die
Dokumentenverwaltung**

Die OperationI_Authorization_Management_Insurant::startKeyChange DARF NICHT
durch das FdV aufgerufen werden. Der Aufruf der Operation darf nur innerhalb
des Aktensystems durch die Komponente Dokumentenverwaltung
erfolgen.Anmerkung:Die Beschreibung der Operation ist als “logische”
Definition zu verstehen. Die technische Umsetzung innerhalb des Aktensystems
kann vom Hersteller frei gewählt (so das z.b. auch REST möglich ist). Die
Operation verbleibt in der WSDL,  falls ein Hersteller diese nutzen möchte.
Es besteht keine Pflicht die SOAP Schnittstellen zu implementieren. **[\<=]**

Die folgenden Anforderungen beschreiben die Umsetzung der
OperationI_Authorization_Management_Insurant::startKeyChange. Dabei gelten die
übergreifenden Festlegungen zur Prüfung der Eingangsparameter.

**A_20481-01 - Komponente Autorisierung - Prüfen Umschlüsselungsberechtigung
startKeyChange**

Die Komponente Autorisierung MUSS bei Aufruf der
OperationI_Authorization_Management_Insurant::startKeyChangedurch den
Versicherten als Eigentümer der Akte (subject-id == ActorIDdes
übergebenenAuthorizationKey == OwnerKVNRfür den benanntenRecordIdentifier)
mit der Fehlermeldung ACCESS_DENIED abbrechen, wenn der unveränderliche Teil
der KVNR des Versichertenin der übergebenen AuthenticationAssertionnicht
übereinstimmt mit dem unveränderlichen Teil der KVNR des Versicherten im
bereits gespeicherten AuthorizationKey. **[\<=]**

**A_20482-02 - Komponente Autorisierung - Sperren für
Autorisierungsoperationen**

Die Komponente Autorisierung MUSS für den ersten berechtigten Aufruf von
startKeyChange in einem Umschlüsselungsvorgang denRecordStatederKeyChain auf
den Zustand KEY_CHANGEsetzen und Operationsaufrufe
(ausgenommencheckRecordExists, putNotificationInfo, getAuthorizationList,
getAuthorizationState, PutForReplacementund FinishKeyChange) solange mit dem
Fehler  KEY_LOCKEDbeantworten, bis die KeyChainnicht mehr auf dem
WertKEY_CHANGEsteht. Ein Operationsaufruf vongetAuthorizationKeydarf nur durch
den Versicherten selbst möglich sein und MUSS andernfalls mit dem
FehlerACCESS_DENIEDbeantwortet werden.

Tabelle22Tab_Autorisierung -Technische Fehlermeldung KEY_LOCKED

<table><tr><th>
Name

</th><th>
Fehlertext

</th><th>
Details

</th></tr><tr><td>
KEY_LOCKED

</td><td>
Die Akte ist während des Schlüsselwechsels gesperrt

</td><td>
Die Akte ist während des Schlüsselwechsels gesperrt

</td></tr></table>

**[\<=]**

**A_20496 - Komponente Autorisierung - Umschlüsselung nur für aktive
Aktenkonten**

Die Komponente Autorisierung MUSS die OperationstartKeyChangemit dem
Fehler ACCESS_DENIEDbeenden, wenn sich das Aktenkonto des benannten Nutzers
nicht im ZustandACTIVATEDbefindet oderKeyChainsich bereits im
Zustand KEY_CHANGEbefindet. **[\<=]**

### 6.2.4.21 Operationsdefinition I_Authorization_Management_Insurant::putForReplacement

**A_20484-02 - Komponente Autorisierung -
I_Authorization_Management_Insurant::putForReplacement**

Die Komponente Autorisierung MUSS die
Operation I_Authorization_Management_Insurant::putForReplacementgemäß der
folgenden Signatur implementieren:

Tabelle23: Tab_Autorisierung -
Operation I_Authorization_Management_Insurant::putForReplacement Definition

<table><tr><th colspan="2">
Operation

</th><th colspan="4">
I_Authorization_Management_Insurant::putForReplacement

</th></tr><tr><td colspan="2">
Beschreibung

</td><td colspan="4">
Mit dieser Operation übergibt der Versicherte die für die Umschlüsselung an
der Komponente Autorisierung erforderlichen verschlüsselten AuthorizationKeys,
damit diese die bisher verwendeten AuthorizationKeys ersetzen können.

</td></tr><tr><td colspan="2">
Formatvorgaben

</td><td colspan="4">
Die Definition der Ein- und Ausgabeparameter erfolgt in
[AuthorizationService.xsd].

Diejenigen Parameter, die im XSD-Schema optional gekennzeichnet, aber hier nicht
aufgeführt sind, werden in der Operation an dieser Schnittstelle nicht
verwendet.

</td></tr><tr><td colspan="6">
Eingangsparameter

</td></tr><tr><td colspan="2">
 Name

</td><td colspan="2">
 Beschreibung

</td><td>
Typ

</td><td>
opt.

</td></tr><tr><td colspan="2" rowspan="1">
AuthenticationAssertion

</td><td colspan="2" rowspan="1">
Die AuthenticationAssertion ist eine von einem Identitiy Provider ausgestellte
Authentifizierungsbestätigung für einen Nutzer.

</td><td>
SAML Assertion im SOAP-Header des Requests

</td><td>
-

</td></tr><tr><td colspan="2" rowspan="1">
RecordIdentifier

</td><td colspan="2" rowspan="1">
Der

RecordIdentifier

referenziert ein konkretes Aktenkonto eines Versicherten bei einem Anbieter. Mit
diesem wird der Datensatz der Autorisierung in der Komponente Autorisierung
für den anfragenden Nutzer lokalisiert.

 

</td><td>
RecordIdentifierType

</td><td>
-

</td></tr><tr><td colspan="2" rowspan="1">
DeviceID

</td><td colspan="2" rowspan="1">
Die

DeviceID

enthält die Gerätekennung eines vom Nutzer verwendeten Gerätes.

</td><td>
DeviceIdType

</td><td>
-

</td></tr><tr><td colspan="2" rowspan="1">
AllEncryptedKeys

</td><td colspan="2" rowspan="1">
Die Liste der neuen Autorisierungsschlüssel soll die bisherigen Schlüssel
komplett ersetzen.

</td><td>
AuthorizationKeyType[0..*]

</td><td>
-

</td></tr><tr><td colspan="5" rowspan="1">
Ausgangsparameter

</td></tr><tr><td colspan="2" rowspan="1">
Name

</td><td colspan="2" rowspan="1">
Beschreibung

</td><td>
Typ

</td><td>
opt.

</td></tr><tr><td colspan="2" rowspan="1">
OkDate

</td><td colspan="2" rowspan="1">
Zeitpunkt der erfolgreichen Umsetzung

</td><td>
signierte dateTime, 

base64-codiert

</td><td>
-

</td></tr><tr><td colspan="6">
Technische Fehlermeldungen 

</td></tr><tr><td colspan="2" rowspan="1">
Name

</td><td colspan="2">
Fehlertext

</td><td colspan="2">
Details

</td></tr><tr><td colspan="2" rowspan="1">
TECHNICAL_ERROR

</td><td colspan="2">
Zufallszahl

</td><td colspan="2">
Interner Fehler in der Verarbeitungslogik

</td></tr><tr><td colspan="2" rowspan="1">
ASSERTION_INVALID

</td><td colspan="2">
Die übergebene Authentication Assertion ist ungültig

</td><td colspan="2">
Die Authentifizierungsbestätigung des aufrufenden Nutzers wird nicht akzeptiert.

</td></tr><tr><td colspan="2" rowspan="1">
DEVICE_UNKNOWN

</td><td colspan="2" rowspan="1">
generierte

phr:DeviceID::Device

</td><td colspan="2" rowspan="1">
Das vom Nutzer verwendete Gerät des Versicherten ist nicht bekannt und muss
freigeschaltet werden.

</td></tr><tr><td colspan="2" rowspan="1">
ACCESS_DENIED

</td><td colspan="2" rowspan="1">
Der Zugriff für diese Operation konnte nicht gewährt werden.

</td><td colspan="2" rowspan="1">
Die Operation ist mit den angegebenen Parametern nicht zulässig.

</td></tr><tr><td colspan="2" rowspan="1">
KEY_CORRUPT

</td><td colspan="2" rowspan="1">
Schlüssel in

AllEncryptedKeys

sind korrupt

</td><td colspan="2" rowspan="1">
Ein oder mehrere der übergebenen AuthorizationKeys lassen sich nicht
verarbeiten.

</td></tr></table>

**[\<=]**

### 6.2.4.22 Umsetzung I_Authorization_Management_Insurant::putForReplacement

**A_20493-01 - Komponente Autorisierung - Prüfen Umschlüsselungsberechtigung
putForReplacement**

Die Komponente Autorisierung MUSS für die
OperationI_Authorization_Management_Insurant::putForReplacementdurch den
Versicherten als Eigentümer der Akte (subject-id == ActorIDdes
übergebenenAuthorizationKey == OwnerKVNRfür den benanntenRecordIdentifier)
mit der FehlermeldungACCESS_DENIEDabbrechen, wenn der unveränderliche Teil der
KVNR des Versichertenin der übergebenen AuthenticationAssertionnicht
übereinstimmt mit dem unveränderlichen Teil der KVNR des Versicherten im
bereits gespeichertenAuthorizationKey. Wenn dieKEY_CHAIN sich nicht auf dem
WertKEY_CHANGEbefindet, MUSS die Operation mit der
FehlermeldungACCESS_DENIEDabbrechen. **[\<=]**

**A_20485 - Komponente Autorisierung - Markieren der bisherigen
AuthorizationKeys als veraltet**

Bei Aufruf der OperationputForReplacementMUSS die Komponente Autorisierung
sämtliche bestehenden AuthorizationKeys des betroffenen Aktenkontos als
veraltet markieren und in einem Zwischenspeicher von der Verwendung als
produktives Schlüsselmaterial ausschließen. Die Zwischenspeicherung muss im
Falle eines Rollbacks geeignet sein, das Schlüsselmaterial wieder vollständig
als produktives Schlüsselmaterial herzustellen.  **[\<=]**

**A_20486 - Komponente Autorisierung - Einbringen des neuen Schlüsselmaterials
als produktive Schlüssel**

Die Komponente Autorisierung MUSS die in der
OperationputForReplacementübergebene Liste AllEncryptedKeys(nach der
Markierung der bisherigen AuthorizationKeys als veraltet) als produktive
AuthorizationKeys in das betroffene Aktenkonto einbringen und benutzen.
**[\<=]**

**A_20544 - Komponente Autorisierung Vers. - Codierung der
putForReplacement-Response**

Die Komponente Autorisierung MUSS den Zeitpunkt des Einbringens des neuen
Schlüsselmaterials mit dem privaten Schlüssel der Ausstelleridentität
C.FD.SIG in seiner fachlichen Rolle oid_epa_authz gemäß [gemSpec_OID]  in
der Response der
Operation I_Authorization_Management_Insurant::putForReplacement signieren
und Base64-codiert inOkDatezurückgeben. **[\<=]**

**A_20488 - Komponente Autorisierung - Rollback bei Scheitern der
Schlüsselersetzung**

Die Komponente Autorisierung MUSS bei Scheitern des Einbringens neuen
Schlüsselmaterials als produktive Schlüssel

 ---> UL

**[\<=]**

### 6.2.4.23 Operationsdefinition I_Authorization_Management_Insurant::finishKeyChange

**A_20487-04 - Komponente Autorisierung -
I_Authorization_Management_Insurant::finishKeyChange**

Die Komponente Autorisierung MUSS die
Operation I_Authorization_Management_Insurant::finishKeyChangegemäß der
folgenden Signatur implementieren:

Tabelle24: Tab_Autorisierung -
Operation I_Authorization_Management_Insurant::finishKeyChange Definition

<table><tr><th colspan="2">
Operation

</th><th colspan="4">
I_Authorization_Management_Insurant::finishKeyChange

</th></tr><tr><td colspan="2">
Beschreibung

</td><td colspan="4">
Mit dieser Operation beendet der Versicherte die Umschlüsselung an der
Komponente Autorisierung und hebt die Sperre der Autorisierungskomponente für
anderweitige Autorisierungsaktivitäten auf.

</td></tr><tr><td colspan="2">
Formatvorgaben

</td><td colspan="4">
Die Definition der Ein- und Ausgabeparameter erfolgt in
[AuthorizationService.xsd].

Diejenigen Parameter, die im XSD-Schema optional gekennzeichnet, aber hier nicht
aufgeführt sind, werden in der Operation an dieser Schnittstelle nicht
verwendet.

</td></tr><tr><td colspan="6">
Eingangsparameter

</td></tr><tr><td colspan="2">
 Name

</td><td colspan="2">
 Beschreibung

</td><td>
Typ

</td><td>
opt.

</td></tr><tr><td colspan="2" rowspan="1">
AuthenticationAssertion

</td><td colspan="2" rowspan="1">
Die AuthenticationAssertion ist eine von einem Identitiy Provider ausgestellte
Authentifizierungsbestätigung für einen Nutzer.

</td><td>
SAML Assertion im SOAP-Header des Requests

</td><td>
-

</td></tr><tr><td colspan="2" rowspan="1">
RecordIdentifier

</td><td colspan="2" rowspan="1">
Der

RecordIdentifier

referenziert ein konkretes Aktenkonto eines Versicherten bei einem Anbieter. Mit
diesem wird der Datensatz der Autorisierung in der Komponente Autorisierung
für den anfragenden Nutzer lokalisiert.

 

</td><td>
RecordIdentifierType

</td><td>
-

</td></tr><tr><td colspan="2" rowspan="1">
Success

</td><td colspan="2" rowspan="1">
Der Erfolgszustand zeigt an, ob die Umschlüsselung erfolgreich abgeschlossen
werden kann, oder ob ein Rollback des alten Schlüsselmaterials erforderlich
ist.

</td><td>
Boolean

</td><td>
-

</td></tr><tr><td colspan="6">
Technische Fehlermeldungen 

</td></tr><tr><td colspan="2" rowspan="1">
Name

</td><td colspan="2">
Fehlertext

</td><td colspan="2">
Details

</td></tr><tr><td colspan="2" rowspan="1">
TECHNICAL_ERROR

</td><td colspan="2">
Zufallszahl

</td><td colspan="2">
Interner Fehler in der Verarbeitungslogik

</td></tr><tr><td colspan="2" rowspan="1">
ASSERTION_INVALID

</td><td colspan="2">
Die übergebene Authentication Assertion ist ungültig

</td><td colspan="2">
Die Authentifizierungsbestätigung des aufrufenden Nutzers wird nicht akzeptiert.

</td></tr><tr><td colspan="2" rowspan="1">
ACCESS_DENIED

</td><td colspan="2" rowspan="1">
Der Zugriff für diese Operation konnte nicht gewährt werden.

</td><td colspan="2" rowspan="1">
Die Operation ist mit den angegebenen Parametern nicht zulässig.

</td></tr></table>

**[\<=]**

### 6.2.4.24 Umsetzung I_Authorization_Management_Insurant::finishKeyChange

**A_21668-01 - Komponente Autorisierung - Aufruf finishKeyChange nur durch die
Dokumentenverwaltung**

Die OperationI_Authorization_Management_Insurant::finishKeyChange DARF NICHT
durch das FdV aufgerufen werden. Der Aufruf der Operation darf nur innerhalb
des Aktensystems durch die Komponente Dokumentenverwaltung erfolgen.Anmerkung: 

Die Beschreibung der Operation ist als “logische” Definition zu verstehen.
Die technische Umsetzung innerhalb des Aktensystems kann vom Hersteller frei
gewählt (so das z.b. auch REST möglich ist). Die Operation verbleibt in der
WSDL,  falls ein Hersteller diese nutzen möchte. Es besteht keine Pflicht die
SOAP Schnittstellen zu implementieren. **[\<=]**

**A_20494-01 - Komponente Autorisierung - Prüfen Umschlüsselungsberechtigung
finishKeyChange**

Die Komponente Autorisierung MUSS für die
OperationI_Authorization_Management_Insurant::finishKeyChange durch den
Versicherten als Eigentümer der Akte (subject-id == ActorIDdes
übergebenenAuthorizationKey == OwnerKVNRfür den benanntenRecordIdentifier)
mit der FehlermeldungACCESS_DENIEDabbrechen, wenn der unveränderliche Teil der
KVNR des Versicherten in der übergebenenAuthenticationAssertion nicht
übereinstimmt mit dem unveränderlichen Teil der KVNR des Versicherten im
bereits gespeichertenAuthorizationKey. Wenn dieKEY_CHAIN sich nicht auf dem
WertKEY_CHANGEbefindet, MUSS die Operation mit der
FehlermeldungACCESS_DENIEDabbrechen. **[\<=]**

**A_20489 - Komponente Autorisierung - Erfolgreicher Abschluss der
Umschlüsselung**

Die Komponente Autorisierung MUSS bei Übergabe des Wertestrueim
ParameterSuccessam RecordStatederKeyChainden ZustandKEY_CHANGEverlassen und
stattdessen den Zustand ACTIVATEDsetzen. **[\<=]**

**A_20490 - Komponente Autorisierung - Rollback bei fehlgeschlagener
Umschlüsselung**

Die Komponente Autorisierung MUSS bei Übergabe des Wertesfalse im
ParameterSuccess einen Rollback der als veraltet markierten AuthorizationKeys
durchführen und am RecordStatederKeyChainden Zustand KEY_CHANGEverlassen und
stattdessen den Zustand ACTIVATEDsetzen. **[\<=]**

**A_21150 - Komponente Autorisierung - Protokollierungszusatz für
Verwaltungsprotokolleintrag für Aufruf der Operation FinishKeyChange**

Die Komponente Autorisierung MUSS im Falle des Aufrufs von FinishKeyChange bei
der Protokollierung gemäß [gemSpec_DM_ePA#A_14505-*] einen Protokolleintrag
(Event.code=PHR-482) hinzufügen und dabei den folgenden Parameter hinzufügen:

Tabelle 25: Tab_Autorisierung_43 - Zusätzliche Parameter des §
291a-Protokolls für ein Rollback im Rahmen der Umschlüsselung

<table><tr><th>
Protokoll-parameter

</th><th colspan="2">
Parameterwerte gemäß aufgerufener Operation

</th></tr><tr><td rowspan="3">
O

bjectDetail

</td><td colspan="2">
Das Element

ParticipantObjectDetail

muss zusätzlich mit folgendem Wertepaar (

type/value

) belegt werden

:

</td></tr><tr><td>
type

</td><td>
value

</td></tr><tr><td>
Details

</td><td>
Der Wert ist abhängig vom Aufrufparameter 

Success

der Operation

FinishKeyChange

.

Success = 1:

"Umschlüsselung erfolgreich beenden"

Success = 0:

"Umschlüsselung abbrechen"

</td></tr></table>

**[\<=]**

### 6.2.4.25 Fehlerbehandlung I_Authorization_Management_Insurant

**A_22401 - Komponente Autorisierung Vers. - Freischaltprüfung Vertreter an der
Schnittstelle I_Authorization_Management_Insurant**

Die Komponente Autorisierung MUSS bei Wahrnehmung einer Vertretung für einen
Versicherten bei Aufrufen von Operationen an der
Schnittstelle I_Authorization_Management_Insurantprüfen, ob ein wartender
Vertreter-Freischaltprozess für [OwnerKVNR des benannten RecordIdentifiers,
subject-id als ActorID] aktiv ist und falls ja, die Operation mit dem
Fehler REPRESENTATIVE_PENDING abbrechen. **[\<=]**

### 6.3 Berechtigungstypen der Autorisierung

Der Berechtigungstyp (AuthorizationType) steuert den Zugriff auf weitere
Ressourcen für einen authentisierten Nutzer. Der Berechtigungstyp wird beim
Hinzufügen des Schlüsselmaterials für einen Nutzer in der
Autorisierungskomponente hinterlegt.

Es wird zwischen drei Typen unterschieden, die in der folgenden Tabelle
beschrieben sind:

<table><tr><th>
AuthorizationType

</th><th>
Beschreibung

</th></tr><tr><td>
DOCUMENT_AUTHORIZATION

(Dokumentenautorisierung)

</td><td>
Es wird für einen authentisierten Nutzer eine Autorisierungsbestätigung
ausgestellt, die für den Zugang zur Dokumentenverwaltung notwendig ist.

</td></tr><tr><td>
ACCOUNT_AUTHORIZATION

(Betreiberwechselautorisierung)

</td><td>
Es wird dem authentisierten Nutzer eine Autorisierungsbestätigung ausgestellt,
mit dem in der Komponente Dokumentenverwaltung nur ein eingeschränkter
Zugriff  auf Daten des Versicherten möglich ist.

</td></tr></table>

### 6.4 Hardware-Merkmal der Komponente Autorisierung

Es müssen die privaten Schlüssel der Ausstelleridentität für
Autorisierungsbestätigungen sowie der TLS-Server-Identität sicher gespeichert
werden.

**A_14366 - Komponente Autorisierung - Verwendung eines HSM**

Die Komponente Autorisierung MUSS das private Schlüsselmaterial der
Ausstelleridentität C.FD.SIG und der TLS-Server-Identität C.FD.TLS-S in einem
HSM speichern. **[\<=]**

### 6.5 Geräteverwaltung

Die Komponente Autorisierung setzt zusätzlich zur kryptografischen
Autorisierung eine Geräteautorisierung um. Dazu wird bei Zugriffen aus der
Umgebung des Versicherten (über das Internet) geprüft, ob ein Versicherter
bzw. berechtigter Vertreter ein bekanntes Gerät für den Zugriff nutzt. Ist
das Gerät unbekannt, wird ein Freischaltprozess über einen separaten
Benachrichtigungskanal gestartet. Die Erkennung erfolgt auf Basis einer im
Gerät des Versicherten gebildeten DeviceID, welche in den Operationsaufrufen
mitgeschickt werden muss. Die DeviceId alsDeviceIdTypegemäß
[PHR_Common.xsd] enthält neben der eigentlichen GerätekennungDevice, welche
für den Abgleich bekannter Geräte verwendet wird, einenDisplayName, der dem
Nutzer die Verwaltung seiner genutzten Geräte erleichtert.

Die Umsetzung erfolgt in der Komponente Autorisierung, da eine vorgelagerte
zustandslose Komponente der Authentifizierung von Nutzern, ggfs. nicht über
einen Speicher zur Verwaltung von Gerätekennungen je Benutzerkonto verfügt
bzw. dieser für diesen Zweck erst geschaffen werden müsste.

Die Prüfung auf ein autorisiertes Gerät erfolgt vor der Herausgabe des in der
Komponente Autorisierung gespeicherten Schlüsselmaterials.

Für die Benachrichtigung mit anschließender Freischaltung werden E-Mails mit
generierten URLs auf generierte HTML-Webseiten verwendet, da E-Mail aus
Usability-Sicht am komfortabelsten erscheint und diese Methoden in
verschiedensten Diensten im Internet etabliert und den Versicherten sehr
wahrscheinlich bekannt sind.

### 6.5.1 Freischaltprozess neuer Geräte

Der Freischaltprozess dient dazu, ein Endgerät des Versicherten in der
Komponente Autorisierung zu registrieren. Der folgende Ablauf zeigt informativ
einen möglichen Ablauf des Freischaltprozesses.

![Abbildung-4][Abbildung-4]

Die Komponente Autorisierung startet den Freischaltprozess für jedes
überDeviceID::Deviceidentifizierte Gerät, das für den AuthorizationKey eines
per KVNR identifizierten Versicherten bzw. Vertreter zu einer genannten
RecordID als unbekannt gilt. D.h. ein vom Vertreter im eigenen Aktenkonto
verwendetes Gerät kann dort bereits registriert sein, im Rahmen der Vertretung
eines anderen Versicherten kann das gleiche Gerät am Vertretungsschlüssel
unbekannt sein. In diesem Fall ist der Freischaltprozess für die Wahrnehmung
der Vertretung erforderlich.

Die Komponente Autorisierung generiert zu einem Freischaltprozess einen
eindeutigen Link auf Basis von Zufallszahlen und verschickt ihn an die vom
Nutzer hinterlegte Benachrichtigungs-E-Mail-Adresse. Durch Klicken auf diesen
Link erhält der Versicherte bzw. Vertreter eine Webseite, mit der Bitte um
Bestätigung der Freischaltung des genutzten Geräts. Nach Erhalt der
Freischaltbestätigung fügt die Komponente Autorisierung das per DeviceID
identifizierte Gerät zum AuthorizationKey des Versicherten bzw. Vertreters
hinzu.

**A_17866 - Komponente Autorisierung - Generierung Device-Kennung für
unbekanntes Gerät des Versicherten**

Die Komponente Autorisierung MUSS bei Aufruf einer Operation der
SchnittstellenI_Authorization_Insurant und I_Authorization_Management_Insurantmit
einem für den aufrufenden Nutzer im benanntenRecordIdentifierunbekanntem
Parameterphr:DeviceID::Deviceeine  256 Bit Zufallszahl (base64-kodiert) mit
einer Mindestentropie von 120 Bit  und Erzeugung gemäß
[gemSpec_Krypt#GS-A_4367] erzeugen, diese als phr:DeviceID::Devicefür den
aufrufenden Nutzer im benannten RecordIdentifier konfigurieren und den
Freischaltprozess gemäß starten. **[\<=]**

Mit der Generierung der Device-Kennung auf Basis einer Zufallszahl je Konto
ergibt sich, dass die Verwendung eines Geräts in verschiedenen Konten (z.B.
eigenes Konto + Vertretungsberechtigung in einem anderen Konto) zur Erzeugung
zweier verschiedener Device-IDs führt, die im jeweiligen Aufrufkontext zu
verwenden sind.

**A_17947 - Komponente Autorisierung - Gültigkeitszeitraum und Löschung der
Devicekennung**

Die Komponente Autorisierung MUSS jede generierte und in einem Aktenkonto
gespeicherte Device-Kennungphr:DeviceID::Device nach 2 Jahren löschen und
darf Nutzeranfragen mit dieser Device-Kennung nach diesem Zeitpunkt nicht mehr
akzeptieren. **[\<=]**

Daraus folgt, dass nach zwei Jahren eine Neuregistrierung des verwendeten
Geräts erforderlich ist. Ein möglicher Zeitraum der Inaktivität des Geräts
ist dabei irrelevant

**A_14515 - Komponente Autorisierung - Freischaltprozess Freischalt-URL**

Die Komponente Autorisierung MUSS im Freischaltprozess eine Freischalt-URL
erzeugen, die einzig aus dem FQDN der Komponente Autorisierung und einer
Zufallszahl (base64-kodiert) mit mindestens 120 Bit Entropie und Erzeugung
gemäß [gemSpec_Krypt#GS-A_4367] besteht und diese Freischalt-URL an die
E-Mail-Adresse amAuthorizationKeydes
viaKVNReinerAuthenticationAssertionreferenzierten Nutzers zum
angefragtenRecordIdentifierverschicken. **[\<=]**

**A_14518 - Komponente Autorisierung - Freischaltprozess Freischalt-URL
Transportsicherheit**

Die Komponente Autorisierung MUSS in der generierten Freischalt-URL das
https-Protokoll verwenden. **[\<=]**

**A_14520 - Komponente Autorisierung - Freischaltprozess Webseite zu
Freischalt-URL**

Die Komponente Autorisierung MUSS bei Aufruf einer generierten Freischalt-URL
durch einen Versicherten bzw. Vertreter mit einer HTML-Seite mit folgendem
Inhalt über den transportverschlüsselten Kanal der https-Freischalt-URL
antworten:

 ---> UL

**[\<=]**

**A_14521 - Komponente Autorisierung - Freischaltprozess DeviceID hinzufügen**

Die Komponente Autorisierung MUSS bei Abruf des Bestätigungslinks eines aktiven
Freischaltprozesses die generierte phr:DeviceID::Device 
zumAuthorizationKeyeinesRecordIdentifiersdes
überKVNReinerAuthenticationAssertionidentifizierten Versicherten bzw.
Vertreters hinzufügen und den Freischaltprozess für den Vorgang zu DeviceID,
KVNR und RecordIdentifier beenden. **[\<=]**

**A_14522 - Komponente Autorisierung - Freischaltprozess beenden**

Die Komponente Autorisierung MUSS den Vorgang eines Freischaltprozesses
zuDeviceID, KVNRundRecordIdentifiernach6 Stunden Wartezeit beenden. **[\<=]**

**A_14523 - Komponente Autorisierung - Freischaltprozess Löschen nach
Beendigung**

Die Komponente Autorisierung MUSS beim Beenden des Vorgangs eines
Freischaltprozesses die generierte Freischalt-URL und alle dazugehörigen
temporären Daten löschen. **[\<=]**

### 6.5.2 Geräteadministration

Mit der Geräteadministration wird dem Nutzer die Möglichkeit gegeben, seine
Endgeräte zu verwalten.

**A_14364 - Komponente Autorisierung - Geräteverwaltung**

Die Komponente Autorisierung MUSS dem authentifizierten Versicherten über eine
Web-Schnittstelle folgende Funktionen zur Verfügung stellen:

 ---> UL

**[\<=]**

**A_15438 - Komponente Autorisierung - Keine negative Beeinflussung des
Aktensystems durch die Geräteverwaltung**

Die Komponente Autorisierung MUSS sicherstellen, dass das Web-Frontend zur
Geräteverwaltung der Komponente Autorisierung so geschützt wird, dass keine
negative Beeinflussung des Aktensystems über diese Schnittstelle möglich ist.
**[\<=]**

**A_21709 - Komponente Autorisierung - Definition Schnittstelle
Geräteverwaltung**

Die Schnittstelle zur Geräteverwaltung ist als REST-Service definiert und als
[DeviceManagement] veröffentlicht. Sie MUSS wie dort definiert umgesetzt
werden. **[\<=]**

**A_21711 - Komponente Autorisierung - Verwaltung eigener Geräte in der
Geräteverwaltung**

Die Komponente Autorisierung MUSS sicherstellen, dass der jeweilige Nutzer
(Versicherter, Vertreter) über die Schnittstelle zur Geräteverwaltung
ausschließlich seine eigenen Geräte verwalten kann. **[\<=]**

**A_21712-01 - Komponente Autorisierung - Löschen der Informationen zur
Geräteverwaltung für einen Vertreter**

Die Komponente Autorisierung MUSS sicherstellen, dass beim Löschen einer
Vertreterberechtigung auch die Daten zu den Geräten des Vertreters in der
Geräteverwaltung gelöscht werden. **[\<=]**

**A_14595 - Komponente Autorisierung - Pflegeprozess Geräteverwaltung**

Die Komponente Autorisierung MUSS die interne Liste aller bekannten Geräte
derart pflegen, dass ein Gerät nach spätestens einem Jahr nach der letzten
Nutzung des Gerätes automatisch aus der Liste der registrierten Geräte
gelöscht wird, und bei anschließender Verwendung durch einen Versicherten als
unbekanntes Gerät über den Freischaltprozess neu freizuschalten ist. **[\<=]**

**A_15551 - Komponente Autorisierung - Deregistrierung in fremden Konten**

Die Komponente Autorisierung MUSS sicherstellen, dass der Versicherte nur
diejenigen registrierten Geräte verwalten kann, die der Versicherte oder ein
Vertreter in seinem Konto verwendet. Eine Deregistrierung eines Gerätes in
einem Konto DARF NICHT automatisch zu einer Deregistrierung in einem anderen
Konto führen (z.B. im Konto eines anderen Versicherten, für das der
Versicherte Vertretungsrechte besitzt). **[\<=]**

**A_15755-01 - Komponente Autorisierung - Protokollierung Geräteverwaltung**

Die Komponente Autorisierung MUSS alle Vorgänge der Geräteverwaltung im
Verwaltungsprotokoll des Versicherten mit PHR-470 protokollieren. **[\<=]**

### 6.6 Freischaltprozess Vertretereinrichtung

Die Komponente Autorisierung führt eine zusätzliche Autorisierung durch den
Versicherten bei Einrichtung einer Vertretung für einen Vertreter durch. Der
Versicherte wird aufgefordert, auf einen Link in einer E-Mail zu klicken, um
die Speicherung eines AuthorizationKey für einen Vertreter zu autorisieren,
den er über I_Authorization_Management_Insurant::putAuthorizationKey für
diesen Vertreter hinterlegt. Die E-Mail mit dem Link zur Freischaltung wird an
die E-Mail-Adresse des Versicherten geschickt, die auch für die
Gerätefreischaltung des Versicherten verwendet wurde. Der folgende Ablauf
zeigt informativ einen möglichen Ablauf des Freischaltprozesses.

![Abbildung-5][Abbildung-5]

Die Komponente Autorisierung startet den Freischaltprozess wenn der Versicherte
mittelsI_Authorization_Management_Insurant::putAuthorizationKeyfür einen
konkreten mittels KVNR identifizierten Vertreter (alsActorIDam
AuthorizationKey) erstmalig eine Berechtigung hinterlegen möchte.  Die
Operation wird zunächst erfolgreich abgeschlossen, sofern kein fachlicher oder
technischer Fehler dies verhindert. Dem Vertreter wird der Zugriff auf diesen
Schlüssel jedoch solange verwehrt, wie der Versicherte noch nicht auf einen
Freischaltlink in einer generierten Freischalt-E-Mail klickt. Die Komponente
Autorisierung generiert zum Freischaltprozess der Vertretung einen eindeutigen
Link auf Basis von Zufallszahlen und verschickt ihn an die vom Versicherten
hinterlegte Benachrichtigungs-E-Mail-Adresse.

Durch Klicken auf diesen Link signalisiert der Versicherte der Komponente
Autorisierung, dass die Hinterlegung eines AuthorizationKey für die KVNR
d.h.ActorIDdes Vertreters rechtmäßig ist. Die Komponente Autorisierung
speichert diesen Freischaltzustand für dieActorIDdes Vertreters und teilt dem
Versicherten über die mittels Freischaltlink abgerufene Webseite mit, dass der
UseCase des Schlüsselabrufs
mittelsI_Authorization_Insurant::getAuthorizationKey durch den Vertreter nun
autorisiert ist. Der Vertreter kann nun den hinterlegten Schlüssel abrufen
und eine Vertretung wahrnehmen.

**A_17672 - Komponente Autorisierung - Freischaltprozess Vertretung
Freischalt-URL**

Die Komponente Autorisierung MUSS im Freischaltprozess Vertretereinrichtung eine
Freischalt-URL erzeugen, die einzig aus dem FQDN der Komponente Autorisierung
und einer Zufallszahl (base64-kodiert) mit mindestens 120 Bit Entropie und
Erzeugung gemäß [gemSpec_Krypt#GS-A_4367] besteht und diese Freischalt-URL an
die E-Mail-Adresse des viaOwnerKVNRreferenzierten Versicherten verschicken. **[\<=]**

**A_17673 - Komponente Autorisierung - Freischaltprozess Vertretung
Freischalt-URL Transportsicherheit**

Die Komponente Autorisierung MUSS in der generierten Freischalt-URL das
https-Protokoll verwenden. **[\<=]**

**A_17674 - Komponente Autorisierung - Freischaltprozess Vertretung
getAuthorizationKey erlauben**

Die Komponente Autorisierung MUSS bei Abruf des Bestätigungslinks eines aktiven
Freischaltprozesses zurOwnerKVNRund ActorIddes zukünftigen Vertreters die
Operation I_Authorization_Insurant::getAuthorizationKeyfür das Abrufen eines
AuthorizationKey durch den Vertreter (ActorId = KVNR des zukünftigen
Vertreters) erlauben und den Freischaltprozess für den Vorgang
zuOwnerKVNRundActorIDbeenden. **[\<=]**

Damit wird die Operation I_Authorization_Insurant::getAuthorizationKey bei
zukünftigen Aufrufen durch den Vertreter für die freigeschalteteActorIDnicht
mehr mit Fehler REPRESENTATIVE_PENDING abgebrochen.

**A_17677 - Komponente Autorisierung - Freischaltprozess Vertretung Information**

Die Komponente Autorisierung KANN in der HTTP-Response zum URL-Aufruf der
Vertreterfreischaltung eine Meldung über die erfolgreiche Freischaltung an den
aufrufenden Versicherten zurückgeben. **[\<=]**

**A_17675 - Komponente Autorisierung - Freischaltprozess Vertretung beenden**

Die Komponente Autorisierung MUSS den Vorgang eines Freischaltprozesses
Vertretung zur OwnerKVNR undActorID nach 6 StundenWartezeit beenden. **[\<=]**

**A_17676 - Komponente Autorisierung - Freischaltprozess Vertretung Löschen
nach Beendigung**

Die Komponente Autorisierung MUSS beim Beenden des Vorgangs eines
Freischaltprozesses die generierte Freischalt-URL und alle dazugehörigen
temporären Daten löschen. **[\<=]**

### 7 Informationsmodell

Das folgende Informationsmodell der Autorisierung gibt eine Übersicht über die
verwendeten Objekte mit ihren Eigenschaften und Beziehungen zueinander.

![Abbildung-6][Abbildung-6]

Das blau dargestellte Element bildet den verwaltetenAuthorizationKey, der vom
Versicherten für jeden berechtigten Nutzer in der Komponente Autorisierung
hinterlegt wird, das ElementEncryptedKeyContainerenthält dabei das mit dem
Empfängerschlüssel individuell verschlüsselte Schlüsselmaterial der Akte
(Akten- und Kontextschlüssel). Die Summe aller AuthorizationKeys zu einem
über denRecordIdentifieridentifizierten Konto eines über
dieOwnerKVNRidentifizierten Versicherten bildet das logische Element des
"Schlüsselrings" KeyChain. Zu einem überActorIDidentifizierten Nutzer wird
eine Liste autorisierterGeräte(grün dargestellt) geführt, die bei Zugriffen
aus der Umgebung des Versicherten die Zulässigkeit des genutztenGerätsprüfen
lässt. Für den Fall eines unbekannten und somit nicht in der Liste
zulässiger Geräte enthaltenen Geräts wird ein Freischaltprozess über
einenBenachrichtigungskanalgestartet. Die Zuordnung der
Benachrichtigungsadressen zum jeweiligen Nutzer ist im Bild gelb dargestellt.

Für Versicherte und deren Vertreter wird der unveränderliche Teil
derKVNR(VersichertenID) der eGK alsActorIDverwendet. Für den Versicherten
wird genau diese ID auch als OwnerKVNR genutzt, um den jeweiligen Versicherten
als Eigentümer einer Akte zu identifizieren. Für
Leistungserbringerinstitutionen und Kostenträger wird die Telematik-ID als
ActorID verwendet. Für Leistungserbringerinstitutionen sowie für die
Kostenträger wird keine Liste autorisierter Geräte und keine Liste von
Benachrichtigungskanälen geführt. Die Eigenschaft validTo bezeichnet ein
Gültigkeitsende-Datum, nach welchem (darauffolgender Tag) ein AuthorizationKey
systemseitig automatisch gelöscht wird. Für den Versicherten als Eigentümer
der Akte wird ein technisches Ende-Datum gleichbedeutend mit "unendlich"
automatisch gesetzt. Für alle anderen AuthorizationKeys wird das Datum
clientseitig belegt und definiert das Ende der vom Versicherten vergebenen
Berechtigung. Mit dem optionalen Displaynameje AuthorizationKey kann vom
Versicherten ein lesbarer Name für eine Berechtigung vergeben werden, auf
LE-Seite und den Abruf durch Kostenträger wird das Feld vollständig ignoriert.

Mittels der Angabe desRecordIdentifiersund derActorID(Telematik-ID/KVNR)kann der
zugehörigeAuthorizationKeyeines Berechtigten gefunden
werden. DerAuthorizationKeyenthält eine Liste
verschlüsselter Akten-undKontextschlüssel.

Das Element AUT-Referenz speichert in einer WhiteList die serialNumber der zur
Authentisierung durch Versicherte in einer Akte verwendeten AUT- bzw.
AUT_ALT-Zertifikate. Über diese Liste wird die Verwendung einer bisher
unbekannten kryptografischen Identität erkannt und der Versicherte bzw. der
Vertreter über den Benachrichtigungskanal informiert.

### 7.1 Namensräume

Für die Schnittstellen der Komponente Autorisierung werden die in der folgenden
Tabelle definierten XML-Präfixe verwendet, um den Namensraum des
XML-Dokumentes zu beschreiben.

<table><tr><th>
Präfix

</th><th>
Namensraum

</th></tr><tr><td>
xmlns:phrs

</td><td>
http://ws.gematik.de/fd/phrs/AuthorizationService/v1.1

</td></tr><tr><td>
xmlns:SAML

</td><td>
urn:oasis:names:tc:SAML:2.0:assertion

</td></tr><tr><td>
xmlns:ds

</td><td>
http://www.w3.org/2000/09/xmldsig#

</td></tr><tr><td>
xmlns:xenc

</td><td>
http://www.w3.org/2001/04/xmlenc# 

</td></tr></table>

### 7.2 SAML-Profil und Tokeninhalte

In diesem Abschnitt werden die Inhalte der auszustellenden
AuthorizationAssertion festgelegt. Eine AuthorizationAssertion wird für einen
mittels AuthenticationAssertion authentifizierten Nutzer ausgestellt. Aus
dessen AuthenticationAssertion werden identifizierende Attribute in die
AuthorizationAssertion übernommen.

**A_14491-05 - Komponente Autorisierung - Inhalte AuthorizationAssertion**

Die Komponente Autorisierung MUSS Autorisierungsbestätigungen als
SAML2-Assertion gemäß den Festlegungen der folgenden Tabelle ausstellen:

Tabelle28: Inhalte Autorisierungsbestätigung

<table><tr><th colspan="3">
Assertion Element

</th><th>
Usage Convention

</th><th>
Beschreibung

</th></tr><tr><td colspan="3">
Issuer

</td><td>
[FQDN des authz Service der TI]

</td><td>
Aussteller des Tokens

</td></tr><tr><td colspan="3">
Signature

</td><td>
[nonQES-Signatur des SAML-Tokens]

</td><td>
nonQES-Signatur des SAML-Tokens gemäß [SAML 2.0], die mit dem privaten
Schlüssel der Ausstelleridentität C.FD.SIG der Komponente Autorisierung
gemäß [ gemSpec_Krypt#A_17206] erstellt wird.

Das Element

ds:Signature/ds:KeyInfo/ds:X509

Data/ds:X509Certificate

 muss das zugehörige C.FD.SIG Zertifikat enthalten

</td></tr><tr><td colspan="3">
Subject

</td><td>
</td><td>
</td></tr><tr><td>
</td><td colspan="2">
NameID

</td><td>
[SubjectDN der SMC-B] oder [SubjectDN der eGK]

</td><td>
wird übernommen aus der übergebenen

AuthenticationAssertion

</td></tr><tr><td>
</td><td colspan="2">
SubjectConfirmation 

</td><td>
</td><td>
</td></tr><tr><td>
</td><td>
</td><td>
@Method

</td><td>
urn:oasis:names:tc:SAML:2.0:cm:bearer

</td><td>
Protokoll zur Authentisierung

</td></tr><tr><td colspan="3">
Conditions

</td><td>
</td><td>
</td></tr><tr><td>
</td><td colspan="2">
@NotBefore

</td><td>
[Systemzeit der Komponente Autorisierung]

</td><td>
Zeitpunkt, ab wann die Assertion nutzbar ist.

</td></tr><tr><td>
</td><td colspan="2">
@NotOnOrAfter

</td><td>
[Systemzeit der Komponente Autorisierung + 15 Minuten]

</td><td>
Zeitpunkt, zu dem die Gültigkeit der Assertion endet.

</td></tr><tr><td>
</td><td colspan="2">
AudienceRestriction

</td><td>
</td><td>
Liste der Server, für die das Token ausgestellt wird.

</td></tr><tr><td>
</td><td>
</td><td>
 Audience

</td><td>
 [FQDN des ePA-Aktensystems gemäß gemSpec_Aktensystem Kapitel  ]

</td><td>
Empfänger des Tokens

</td></tr><tr><td colspan="3">
AuthnStatement

</td><td>
</td><td>
</td></tr><tr><td>
</td><td colspan="2">
@AuthnInstant

</td><td>
[Systemzeit der Komponente Autorisierung]

</td><td>
Systemzeitpunkt bei Erstellung des Tokens  
Hinweis: UTC

</td></tr><tr><td colspan="3" rowspan="1">
AuthnContext

</td></tr><tr><td colspan="2" rowspan="1">
@ AuthnContextClassRef

</td><td>
[Art der Authentifizierung]

</td><td>
wird übernommen aus der übergebenen

AuthenticationAssertion

; 

</td></tr><tr><td colspan="3">
AuthzDecisionStatement

</td><td>
</td><td>
</td></tr><tr><td>
</td><td colspan="2">
@Resource

</td><td>
[Telematik-ID] oder [10-stelliger, unveränderlicher Teil der KVNR]

</td><td>
wird übernommen aus der AuthenticationAssertion  
Hinweis: Informationen und
Beispiele zur AuthenticationAssertion finden sich in A_14927, A_15638 und
A_18985-*

</td></tr><tr><td>
</td><td colspan="2">
@Decision

</td><td>
Permit

</td><td>
</td></tr><tr><td>
</td><td colspan="2">
Action

</td><td>
[AuthorizationType]

</td><td>
String gemäß der Autorisierungsentscheidung über den authentifizierten Nutzer

</td></tr><tr><td>
</td><td>
</td><td>
@Namespace

</td><td>
"http://ws.gematik.de/fa/phr/v1.0"

</td><td>
</td></tr><tr><td colspan="3">
AttributeStatement

</td><td>
</td><td>
</td></tr><tr><td>
</td><td colspan="2">
Attribute

</td><td>
</td><td>
</td></tr><tr><td>
</td><td>
</td><td>
@Name

</td><td>
Resource ID

"urn:oasis:names:tc:xacml:1.0:resource:resource-id"

</td><td>
</td></tr><tr><td>
</td><td>
</td><td>
AttributeValue

</td><td>
[RecordIdentifier]

</td><td>
RecordIdentifier der Akte, für die eine Autorisierungsbestätigung für den
Nutzer ausgestellt wird.

</td></tr><tr><td>
</td><td colspan="2">
Attribute

</td><td>
</td><td>
</td></tr><tr><td>
</td><td>
</td><td>
@Name

</td><td>
Gerätekennung 

"urn:gematik:fa:phr:1.0:device:device-id"

</td><td>
Nur bei mittels ActorID authentifizierten Versicherten, bei Abruf durch
Leistungserbringer und Kostenträger entfällt dieses Attribut.

</td></tr><tr><td>
</td><td>
</td><td>
AttributeValue

</td><td>
[DeviceID::Device]

</td><td>
Die DeviceID::Device ist über die ActorID des AuthorizationKey referenziert,
der über die KVNR des Versicherten einer übergebenen AuthenticationAssertion
gefunden wird.

</td></tr><tr><td>
</td><td colspan="2">
Attribute

</td><td>
</td><td>
</td></tr><tr><td>
</td><td>
</td><td>
@Name

</td><td>
Zustand des Kontos

"urn:gematik:fa:phr:1.0:status:status-id"

</td><td>
</td></tr><tr><td>
</td><td>
</td><td>
AttributeValue

</td><td>
[RecordState]

</td><td>
Wert der Eigenschaft RecordState der KeyChain des via RecordIdentifier benannten
Kontos.

</td></tr><tr><td>
</td><td colspan="2">
Attribute

</td><td>
</td><td>
</td></tr><tr><td>
</td><td>
</td><td>
@Name

</td><td>
VersichertenID

"urn:gematik:subject:subject-id"

oder

Telematik-ID

"urn:gematik:subject:organization-id"

</td><td>
Benutzerkennung für den die AuthorizationAssertion ausgestellt wird.

</td></tr><tr><td>
</td><td>
</td><td>
AttributeValue

</td><td>
[Telematik-ID] oder [10-stelliger, unveränderlicher Teil der KVNR]

</td><td>
wird übernommen aus der AuthenticationAssertion

</td></tr></table>

**[\<=]**

### 8 Verteilungssicht

Eine Darstellung der hardwareseitigen Verteilung des Produkttyps bzw. seiner
Teilsysteme und der Einbettung in die physikalische Umgebung wird nicht
benötigt.

### 9 Anhang A – Verzeichnisse

### 9.1 Abkürzungen

<table><tr><th>
Kürzel

</th><th>
Erläuterung

</th></tr><tr><td>
SAML

</td><td>
Security Assertion Markup Language

</td></tr><tr><td>
WS

</td><td>
Web Services

</td></tr><tr><td>
PKCS

</td><td>
Public-Key Cryptography Standards

</td></tr><tr><td>
ePA-FdV

</td><td>
ePA-Frontend des Versicherten, welches das das ePA-Modul FdV inkludiert

</td></tr><tr><td>
IHE

</td><td>
Integrating the Healthcare Enterprise

</td></tr><tr><td>
WSDL

</td><td>
Web Services Description Language

</td></tr><tr><td>
KVNR

</td><td>
Krankenversichertennummer

</td></tr></table>

### 9.2 Glossar

<table><tr><th>
Begriff

</th><th>
Erläuterung

</th></tr><tr><td>
HSM

</td><td>
Hardware Security Module, Gerät zur sicheren Speicherung kryptografischen
Schlüsselmaterials

</td></tr><tr><td>
ePA-Modul FdV

</td><td>
Modul der dezentralen ePA-Fachlogik zur Nutzung durch den Versicherten in einem
ePA-Frontend des Versicherten

</td></tr></table>

Das Glossar wird als eigenständiges Dokument (vgl. [gemGlossar]) zur Verfügung
gestellt.

### 9.3 Abbildungsverzeichnis

- [Abbildung-1] - Anwendungsfälle der Schlüsselverwaltung nach Umgebung
- [Abbildung-2] - Komponente Autorisierung, benachbarte Komponenten und Produkttypen
- [Abbildung-3] - GERROR-Struktur zur Rückgabe einer Fehlermeldung
- [Abbildung-4] - Informativer Ablauf des Geräte-Freischaltprozesses
- [Abbildung-5] - Informativer Ablauf des Freischaltprozesses für Vertretung
- [Abbildung-6] - Informationsmodell der intern verwalteten Daten

### 9.4 Tabellenverzeichnis

- [Tabelle-1] - Anwendungsfälle der Schlüsselverwaltung nach Umgebung
- [Tabelle -2] - Parameter des Verwaltungsprotokolls
- [Tabelle-3] - Fehlercodes zu Fehlern gemäß Operationsdefinition
- [Tabelle-4] - Herstellerspezifische Fehlerdefinition
- [Tabelle-5] - Schnittstellen der Komponente Autorisierung
- [Tabelle-6] - I_Authorization::getAuthorizationKey Definition
- [Tabelle-7] - I_Authorization_Insurant::getAuthorizationKey Definition
- [Tabelle-8] - I_Authorization_Management::putAuthorizationKey - Definition
- [Tabelle-9] - I_Authorization_Management::checkRecordExists - Definition
- [Tabelle-10] - I_Authorization_Management::getAuthorizationList - Definition
- [Tabelle-11] - I_Authorization_Management::getAuthorizationState - Definition
- [Tabelle-12] - I_Authorization_Management_Insurant::putAuthorizationKey - Definition
- [Tabelle-13] - I_Authorization_Management_Insurant::deleteAuthorizationKey - Definition
- [Tabelle-14] - I_Authorization_Management_Insurant::replaceAuthorizationKey - Definition
- [Tabelle-15] - I_Authorization_Management_Insurant::getAuditEvents - Definition
- [Tabelle-16] - I_Authorization_Management_Insurant::getSignedAuditEvents - Definition
- [Tabelle-17] - I_Authorization_Management_Insurant::putNotificationInfo - Definition
- [Tabelle-18] -   I_Authorization_Management_Insurant::getNotificationInfo - Definition
- [Tabelle-19] - I_Authorization_Management_Insurant::getAuthorizationList - Definition
- [Tabelle-20] - I_Authorization_Management_Insurant::getAuthorizationList - Definition
- [Tabelle-21] - Tab_Autorisierung - Operation I_Authorization_Management_Insurant::startKeyChange Definition
- [Tabelle-22] - Tab_Autorisierung -Technische Fehlermeldung KEY_LOCKED
- [Tabelle-23] - Tab_Autorisierung - Operation I_Authorization_Management_Insurant::putForReplacement Definition
- [Tabelle-24] - Tab_Autorisierung - Operation I_Authorization_Management_Insurant::finishKeyChange Definition
- [Tabelle -25] - Tab_Autorisierung_43 - Zusätzliche Parameter des § 291a-Protokolls für ein Rollback im Rahmen der Umschlüsselung
- [Tabelle-26] - Berechtigungstypen für AuthorizationType
- [Tabelle-27] - Namensräume
- [Tabelle-28] - Inhalte Autorisierungsbestätigung
- [Tabelle-29] - Referenzierte Dokumente der gematik
- [Tabelle-30] - Referenzierte externe Dokumente

### 9.5 Referenzierte Dokumente

### 9.5.1 Dokumente der gematik

Die nachfolgende Tabelle enthält die Bezeichnung der in dem vorliegenden
Dokument referenzierten Dokumente der gematik zur Telematikinfrastruktur. Der
mit der vorliegenden Version korrelierende Entwicklungsstand dieser Konzepte
und Spezifikationen wird pro Release in einer Dokumentenlandkarte definiert.
Version und Stand der referenzierten Dokumente sind daher in der nachfolgenden
Tabelle nicht aufgeführt. Deren zu diesem Dokument jeweils gültige
Versionsnummer ist in der aktuellen, von der gematik veröffentlichten
Dokumentenlandkarte enthalten, in der die vorliegende Version aufgeführt wird.

<table><tr><th>
[Quelle]

</th><th>
Herausgeber: Titel

</th></tr><tr><td>
[gemGlossar]

</td><td>
Glossar der Telematikinfrastruktur

</td></tr><tr><td>
[gemSysL_ePA]

</td><td>
Systemspezifisches Konzept ePA

</td></tr><tr><td>
[AuthorizationService.wsdl]

</td><td>
Schnittstellendefinition Komponente Autorisierung 

(src/schema/fd/phr/AuthorizationService.wsdl),
https://github.com/gematik/api-ePA 

</td></tr><tr><td>
[AuthorizationService.xsd]

</td><td>
Schemadefinition der Schnittstellen der Komponente Autorisierung 

(src/schema/fd/phr/AuthorizationService.xsd),
https://github.com/gematik/api-ePA

</td></tr><tr><td>
[TelematikError.xsd]

</td><td>
Schemadefinition Fehlermeldungen TelematikError 

(src/schema/tel/error/TelematikError.xsd), https://github.com/gematik/api-ePA

</td></tr><tr><td>
[PHR_Common.xsd]

</td><td>
Schemadefinition für übergreifende ePA-Datentypen 

(src/schema/fd/phr/PHR_Common.xsd), https://github.com/gematik/api-ePA

</td></tr><tr><td>
[gemKPT_Arch_TIP]

</td><td>
Konzept Architektur der TI-Plattform

</td></tr><tr><td>
[gemSpec_Perf]

</td><td>
Spezifikation Performancevorgaben und Mengengerüst

</td></tr><tr><td>
[gemSpec_Krypt]

</td><td>
Spezifikation der in der TI zulässigen kryptografischen Verfahren

</td></tr><tr><td>
[gemSpec_OID]

</td><td>
Spezifikation Festlegung von OIDs

</td></tr><tr><td>
[gemSpec_OM]

</td><td>
Spezifikation Operation und Maintenance

</td></tr><tr><td>
[gemSpec_PKI]

</td><td>
Übergreifende Spezifikation PKI

</td></tr><tr><td>
[gemSpec_TB_Auth]

</td><td>
Übergreifende Spezifikation Tokenbasierte Authentisierung

</td></tr><tr><td>
[gemSpec_TSL]

</td><td>
Spezifikation der Schnittstelle des TSL-Dienstes

</td></tr><tr><td>
[DeviceManagement]

</td><td>
Schnittstelle zur Geräteverwaltung

(src/openapi/device_management.yaml),

https://github.com/gematik/api-ePA

 

</td></tr></table>

### 9.5.2 Weitere Dokumente

<table><tr><th>
[Quelle]

</th><th>
Herausgeber (Erscheinungsdatum): Titel

</th></tr><tr><td>
[SAML2.0]

</td><td>
Assertions and Protocols for the OASIS Security Assertion Markup Language (SAML)
V2.0

http://docs.oasis-open.org/security/saml/v2.0/

</td></tr><tr><td>
[SOAP]

</td><td>
W3C (2007): SOAP Version 1.2 Part 1: Messaging Framework (Second Edition), 

https://www.w3.org/TR/soap12-part1/

 

</td></tr><tr><td>
[WSDL]

</td><td>
W3C: Web Services Description Language (WSDL) 1.1

https://www.w3.org/TR/wsdl.html

 

</td></tr><tr><td>
[WSDL11SOAP12]

</td><td>
W3C (2006): WSDL 1.1 Binding Extension for SOAP 1.2, 

https://www.w3.org/Submission/wsdl11soap12/

 

</td></tr><tr><td>
[WSIBP]

</td><td>
Web-Services Interoperability Consortium (2010): WS-I Basic Profile V2.0 (final
material),

http://ws-i.org/Profiles/BasicProfile-2.0-2010-11-09.html

</td></tr><tr><td>
[WS-Trust1.4]

</td><td>
WS-Trust 1.4

http://docs.oasis-open.org/ws-sx/ws-trust/v1.4/errata01/os/ws-trust-1.4-errata01-os-complete.pdf

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
[XSPA]

</td><td>
OASIS:  Cross-Enterprise Security and Privacy Authorization (XSPA) Profile of
Security Assertion Markup Language (SAML) for Healthcare Version 2.0

http://docs.oasis-open.org/xspa/saml-xspa/v2.0/saml-xspa-v2.0.html

 

</td></tr><tr><td>
[SGB V]

</td><td>
BGBl. I S.2477 (20.12.1988):  
Sozialgesetzbuch, Fünftes Buch  
Zuletzt
geändert durch Art. 4 G v. 14.4.2010 I 410  
Gesetzliche Krankenversicherung

</td></tr><tr><td>
[RFC-5322]

</td><td>
Internet Message Format - Format für E-Mail-Adressen

https://tools.ietf.org/html/rfc5322

 

</td></tr><tr><td>
[RFC5280]

</td><td>
Internet X.509 Public Key Infrastructure Certificate  
Prüfung von Zertifikaten
entlang einer Zertifikatskette (inkl. Cross-Zertifikaten) bis zu einem
Vertrauensanker (Root-CA)

https://tools.ietf.org/html/rfc5280#page-71

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
[3.1]:                   #31-akteure-und-rollen
[3.2]:                   #32-nachbarsysteme
[3.3]:                   #33-tokenbasierte-autorisierung
[4]:                     #4-zerlegung-der-komponente-autorisierung
[5]:                     #5-übergreifende-festlegungen
[5.1]:                   #51-datenschutz-und-datensicherheit
[5.2]:                   #52-verwendete-standards
[5.3]:                   #53-protokollierung
[5.4]:                   #54-fehlerbehandlung-in-schnittstellenoperationen
[5.5]:                   #55-nicht-funktionale-anforderungen
[5.5.1]:                 #551-skalierbarkeit
[5.5.2]:                 #552-performance
[5.5.3]:                 #553-mengengerüst
[6]:                     #6-funktionsmerkmale
[6.1]:                   #61-übergreifende-festlegungen
[6.2]:                   #62-schnittstellen-der-komponente-autorisierung
[6.2.1]:                 #621-schnittstelle-i_authorization
[6.2.1.1]:               #6211-operationsdefinition-i_authorizationgetauthorizationkey
[6.2.1.2]:               #6212-umsetzung-i_authorizationgetauthorizationkey
[6.2.2]:                 #622-schnittstelle-i_authorization_insurant
[6.2.2.1]:               #6221-operationsdefinition-i_authorization_insurantgetauthorizationkey
[6.2.2.2]:               #6222-umsetzung-i_authorization_insurantgetauthorizationkey
[6.2.3]:                 #623-schnittstelle-i_authorization_management
[6.2.3.1]:               #6231-operationsdefinition-i_authorization_managementputauthorizationkey
[6.2.3.2]:               #6232-umsetzung-i_authorization_managementputauthorizationkey
[6.2.3.3]:               #6233-operationsdefinition-i_authorization_managementcheckrecordexists
[6.2.3.4]:               #6234-umsetzung-i_authorization_managementcheckrecordexists
[6.2.3.5]:               #6235-operationsdefinition-i_authorization_managementgetauthorizationlist
[6.2.3.6]:               #6236-umsetzung-i_authorization_managementgetauthorizationlist
[6.2.3.7]:               #6237-operationsdefinition-i_authorization_managementgetauthorizationstate
[6.2.3.8]:               #6238-umsetzung-i_authorization_managementgetauthorizationstate
[6.2.4]:                 #624-schnittstelle-i_authorization_management_insurant
[6.2.4.1]:               #6241-operationsdefinition-i_authorization_management_insurantputauthorizationkey
[6.2.4.2]:               #6242-umsetzung-i_authorization_management_insurantputauthorizationkey
[6.2.4.3]:               #6243-operationsdefinition-i_authorization_management_insurantdeleteauthorizationkey
[6.2.4.4]:               #6244-umsetzung-i_authorization_management_insurantdeleteauthorizationkey
[6.2.4.5]:               #6245-operationsdefinition-i_authorization_management_insurantreplaceauthorizationkey
[6.2.4.6]:               #6246-umsetzung-i_authorization_management_insurantreplaceauthorizationkey
[6.2.4.7]:               #6247-operationsdefinition-i_authorization_management_insurantgetauditevents
[6.2.4.8]:               #6248-umsetzung-i_authorization_management_insurantgetauditevents
[6.2.4.9]:               #6249-operationsdefinition-i_authorization_management_insurantgetsignedauditevents
[6.2.4.10]:              #62410-umsetzung-i_authorization_management_insurantgetsignedauditevents
[6.2.4.11]:              #62411-operationsdefinition-i_authorization_management_insurantputnotificationinfo
[6.2.4.12]:              #62412-umsetzung-i_authorization_management_insurantputnotificationinfo
[6.2.4.13]:              #62413-operationsdefinition-i_authorization_management_insurantgetnotificationinfo
[6.2.4.14]:              #62414-umsetzung-i_authorization_management_insurantgetnotificationinfo
[6.2.4.15]:              #62415-operationsdefinition-i_authorization_management_insurantgetktrtelematikid
[6.2.4.16]:              #62416-umsetzung-i_authorization_management_insurantgetktrtelematikid
[6.2.4.17]:              #62417-operationsdefinition-i_authorization_management_insurantgetauthorizationlist
[6.2.4.18]:              #62418-umsetzung-i_authorization_management_insurantgetauthorizationlist
[6.2.4.19]:              #62419-operationsdefinition-i_authorization_management_insurantstartkeychange
[6.2.4.20]:              #62420-umsetzung-i_authorization_management_insurantstartkeychange
[6.2.4.21]:              #62421-operationsdefinition-i_authorization_management_insurantputforreplacement
[6.2.4.22]:              #62422-umsetzung-i_authorization_management_insurantputforreplacement
[6.2.4.23]:              #62423-operationsdefinition-i_authorization_management_insurantfinishkeychange
[6.2.4.24]:              #62424-umsetzung-i_authorization_management_insurantfinishkeychange
[6.2.4.25]:              #62425-fehlerbehandlung-i_authorization_management_insurant
[6.3]:                   #63-berechtigungstypen-der-autorisierung
[6.4]:                   #64-hardware-merkmal-der-komponente-autorisierung
[6.5]:                   #65-geräteverwaltung
[6.5.1]:                 #651-freischaltprozess-neuer-geräte
[6.5.2]:                 #652-geräteadministration
[6.6]:                   #66-freischaltprozess-vertretereinrichtung
[7]:                     #7-informationsmodell
[7.1]:                   #71-namensräume
[7.2]:                   #72-saml-profil-und-tokeninhalte
[8]:                     #8-verteilungssicht
[9]:                     #9-anhang-a-–-verzeichnisse
[9.1]:                   #91-abkürzungen
[9.2]:                   #92-glossar
[9.3]:                   #93-abbildungsverzeichnis
[9.4]:                   #94-tabellenverzeichnis
[9.5]:                   #95-referenzierte-dokumente
[9.5.1]:                 #951-dokumente-der-gematik
[9.5.2]:                 #952-weitere-dokumente
[Abbildung-1]:           gemSpec_Autorisierung_V1.9.2.attachments/15719297084117273851.bmp
[Abbildung-2]:           gemSpec_Autorisierung_V1.9.2.attachments/12032052280740721834.png
[Abbildung-3]:           gemSpec_Autorisierung_V1.9.2.attachments/16997383745116635923.png
[Abbildung-4]:           gemSpec_Autorisierung_V1.9.2.attachments/11133527811203100159.png
[Abbildung-5]:           gemSpec_Autorisierung_V1.9.2.attachments/5333311913823548744.png
[Abbildung-6]:           gemSpec_Autorisierung_V1.9.2.attachments/10285420410116400334.png
[Tbl-001]:               #Tbl-001 (&93834801632112)
[Tabelle-1]:             #Tabelle-1 (&93834768504944)
[Tabelle -2]:            #Tabelle -2 (&93834781669032)
[Tabelle-3]:             #Tabelle-3 (&93834772236080)
[Tabelle-4]:             #Tabelle-4 (&93834772278008)
[Tabelle-5]:             #Tabelle-5 (&93834768030848)
[Tabelle-6]:             #Tabelle-6 (&93834776366592)
[Tabelle-7]:             #Tabelle-7 (&93834801577160)
[Tabelle-8]:             #Tabelle-8 (&93834799002032)
[Tabelle-9]:             #Tabelle-9 (&93834785762472)
[Tabelle-10]:            #Tabelle-10 (&93834777672600)
[Tabelle-11]:            #Tabelle-11 (&93834781774200)
[Tabelle-12]:            #Tabelle-12 (&93834764482576)
[Tabelle-13]:            #Tabelle-13 (&93834774917608)
[Tabelle-14]:            #Tabelle-14 (&93834789679000)
[Tabelle-15]:            #Tabelle-15 (&93834776292400)
[Tabelle-16]:            #Tabelle-16 (&93834783877232)
[Tabelle-17]:            #Tabelle-17 (&93834778252008)
[Tabelle-18]:            #Tabelle-18 (&93834768667528)
[Tabelle-19]:            #Tabelle-19 (&93834799063080)
[Tabelle-20]:            #Tabelle-20 (&93834799139056)
[Tabelle-21]:            #Tabelle-21 (&93834765321360)
[Tabelle-22]:            #Tabelle-22 (&93834775678728)
[Tabelle-23]:            #Tabelle-23 (&93834775695392)
[Tabelle-24]:            #Tabelle-24 (&93834800037744)
[Tabelle -25]:           #Tabelle -25 (&93834800118088)
[Tabelle-26]:            #Tabelle-26 (&93834783702544)
[Tabelle-27]:            #Tabelle-27 (&93834764335856)
[Tabelle-28]:            #Tabelle-28 (&93834764355744)
[Tbl-030]:               #Tbl-030 (&93834769499712)
[Tbl-031]:               #Tbl-031 (&93834769523280)
[Tabelle-29]:            #Tabelle-29 (&93834771224104)
[Tabelle-30]:            #Tabelle-30 (&93834771276400)
[https://github.com/gematik/api-ePA]: https://github.com/gematik/api-ePA (&93834771272160)
[http://docs.oasis-open.org/security/saml/v2.0/]: http://docs.oasis-open.org/security/saml/v2.0/ (&93834771282664)
[https://www.w3.org/TR/soap12-part1/]: https://www.w3.org/TR/soap12-part1/ (&93834771286328)
[https://www.w3.org/TR/wsdl.html]: https://www.w3.org/TR/wsdl.html (&93834771290704)
[https://www.w3.org/Submission/wsdl11soap12/]: https://www.w3.org/Submission/wsdl11soap12/ (&93834771294848)
[http://ws-i.org/Profiles/BasicProfile-2.0-2010-11-09.html]: http://ws-i.org/Profiles/BasicProfile-2.0-2010-11-09.html (&93834771299176)
[http://docs.oasis-open.org/ws-sx/ws-trust/v1.4/errata01/os/ws-trust-1.4-errata01-os-complete.pdf]: http://docs.oasis-open.org/ws-sx/ws-trust/v1.4/errata01/os/ws-trust-1.4-errata01-os-complete.pdf (&93834771303024)
[http://www.oasis-open.org/committees/download.php/16790/wss-v1.1-spec-os-SOAPMessageSecurity.pdf]: http://www.oasis-open.org/committees/download.php/16790/wss-v1.1-spec-os-SOAPMessageSecurity.pdf (&93834771306688)
[https://www.oasis-open.org/committees/download.php/16768/wss-v1.1-spec-os-SAMLTokenProfile.pdf]: https://www.oasis-open.org/committees/download.php/16768/wss-v1.1-spec-os-SAMLTokenProfile.pdf (&93834771310832)
[http://docs.oasis-open.org/xspa/saml-xspa/v2.0/saml-xspa-v2.0.html]: http://docs.oasis-open.org/xspa/saml-xspa/v2.0/saml-xspa-v2.0.html (&93834771315160)
[https://tools.ietf.org/html/rfc5322]: https://tools.ietf.org/html/rfc5322 (&93834771323176)
[https://tools.ietf.org/html/rfc5280#page-71]: https://tools.ietf.org/html/rfc5280#page-71 (&93834771327808)
