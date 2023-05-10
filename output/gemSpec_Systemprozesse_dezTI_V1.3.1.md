
Elektronische Gesundheitskarte und Telematikinfrastruktur

### Spezifikation<br>Systemprozesse der dezentralen TI

- Klassifizierung: öffentlich
- Referenzierung: gemSpec_Systemprozesse_dezTI
- Revision: 548770
- Stand: 31.01.2022
- Status: freigegeben
- Version: 1.3.1

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
14.12.18

</td><td>
freigegeben

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
Einarbeitung P19.1

</td><td>
gematik

</td></tr><tr><td>
1.3.0

</td><td>
10.09.20

</td><td>
Einarbeitung Änderungsliste P22.3

</td><td>
gematik

</td></tr><tr><td>
1.3.1

</td><td>
31.01.22

</td><td>
2.5.1

</td><td>
Einarbeitung CI_Maintenance_21.2

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
- [2] Leistungen
  - [2.1] Systemprozesse für den Zugriff auf Smartcards der TI
    - [2.1.1] Die Realisierungsumgebung des CardProxy
      - [2.1.1.1] ENV_TUC_CARD_SECRET_INPUT – Realisierung Eingabe PIN-Geheimnis
      - [2.1.1.2] ENV_TUC_CARD_TO_CARD – Realisierung Card-2-Card
      - [2.1.1.3] ENV_TUC_CARD_APDU_TRANSPORT – Realisierung APDU-Transport
    - [2.1.2] Konfiguration und Statusinformationen
      - [2.1.2.1] Konfiguration des CardProxy
      - [2.1.2.2] Initialisierung CardProxy für eGK
      - [2.1.2.3] Initialisierung CardProxy für SM-B
      - [2.1.2.4] PL_TUC_CARD_INFORMATION – Gesammelte Statusinformationen zu einer Karte
      - [2.1.2.5] PL_TUC_EGK_STATUS – Gültigkeit der eGK prüfen
      - [2.1.2.6] PL_TUC_CARD_RESET – Rücksetzen einer Karte
    - [2.1.3] Zugriff auf Smartcards der TI
      - [2.1.3.1] PL_TUC_CARD_CHANGE_PIN – PIN Ändern
      - [2.1.3.2] PL_TUC_CARD_ENABLE_PIN – PIN-Schutz einschalten
      - [2.1.3.3] PL_TUC_CARD_DISABLE_PIN – PIN-Schutz abschalten
      - [2.1.3.4] PL_TUC_CARD_UNBLOCK_PIN – PIN mit PUK entsperren
      - [2.1.3.5] PL_TUC_CARD_VERIFY_PIN – Benutzer verifizieren
      - [2.1.3.6] PL_TUC_CARD_ACTIVATE_APPLICATION – Anwendung aktivieren
      - [2.1.3.7] PL_TUC_CARD_DEACTIVATE_APPLICATION – Anwendung deaktivieren
      - [2.1.3.8] PL_TUC_CARD_GET_CHALLENGE – Auslesen einer Zufallszahl
      - [2.1.3.9] PL_TUC_CARD_READ_FILE – Lesen von Daten aus einer SmartCard
      - [2.1.3.10] PL_TUC_CARD_WRITE_FILE – Schreiben von Daten auf eine SmartCard
      - [2.1.3.11] PL_TUC_CARD_UPDATE_FILE – Aktualisieren von Daten in einer transparenten Datei einer SmartCard
      - [2.1.3.12] PL_TUC_CARD_DELETE_FILE – Löschen von Daten auf einer SmartCard
      - [2.1.3.13] PL_TUC_CARD_ERASE_FILE – Rücksetzen des Inhalts einer transparenten Datei
      - [2.1.3.14] PL_TUC_CARD_READ_RECORD – Lesen von Daten aus einer strukturierten Datei
      - [2.1.3.15] PL_TUC_EGK_READ_PROTOCOL – Auslesen des Zugriffprotokolls der eGK
      - [2.1.3.16] PL_TUC_CARD_WRITE_RECORD – Schreiben von Daten in eine strukturierte Datei
      - [2.1.3.17] PL_TUC_CARD_APPEND_RECORD – Anfügen von Daten an eine strukturierte Datei
      - [2.1.3.18] PL_TUC_EGK_APPEND_PROTOCOL – Zugriff auf der eGK protokollieren
      - [2.1.3.19] PL_TUC_CARD_DELETE_RECORD – Löschen von Daten in einer strukturierten Datei
      - [2.1.3.20] PL_TUC_CARD_ERASE_RECORD – Rücksetzen eines Datensatzes in einer strukturierten Datei
    - [2.1.4] Transparenter Zugriff auf eine SmartCard
      - [2.1.4.1] PL_TUC_CARD_TC_OPEN
      - [2.1.4.2] PL_TUC_CARD_TC_SEND
      - [2.1.4.3] PL_TUC_CARD_TC_CLOSE
  - [2.2] Kommunikation und Vernetzung
    - [2.2.1] PL_TUC_TLS_SECURE_CHANNEL – TLS-Verbindung mit gegenseitiger Authentisierung
    - [2.2.2] PL_TUC_NET_NAME_RESOLUTION
    - [2.2.3] PL_TUC_NET_SYNC_TIME
  - [2.3] Zugriffe auf den Verzeichnisdienst
    - [2.3.1] PL_TUC_VZD_BIND - Verbindung aufbauen
    - [2.3.2] PL_TUC_VZD_SEARCH - Verzeichnis abfragen
    - [2.3.3] PL_TUC_VZD_UNBIND - Verbindung trennen
    - [2.3.4] PL_TUC_VZD_ABANDON - Verzeichnisabfrage abbrechen
  - [2.4] Vertraulichkeit, Authentizität, Integrität
    - [2.4.1] PL_TUC_SIGN_HASH_nonQES – mit TI-Identität nonQES signieren
    - [2.4.2] PL_TUC_HYBRID_ENCIPHER – Hybrid verschlüsseln
    - [2.4.3] PL_TUC_HYBRID_DECIPHER – Hybrid entschlüsseln
    - [2.4.4] PL_TUC_SYMM_ENCIPHER – Symmetrisch verschlüsseln
    - [2.4.5] PL_TUC_SYMM_DECIPHER – Symmetrisch entschlüsseln
    - [2.4.6] PL_TUC_SIGN_DOCUMENT_nonQES – Dokument nonQES signieren
    - [2.4.7] PL_TUC_VERIFY_DOCUMENT_nonQES - nonQES Dokumentensignatur verifizieren
  - [2.5] Leistungen der PKI
    - [2.5.1] PL_TUC_PKI_VERIFY_CERTIFICATE – Prüfung eines Zertifikats der TI
- [3] Anhang A – Verzeichnisse
  - [3.1] Abkürzungen
  - [3.2] Glossar
  - [3.3] Abbildungsverzeichnis
  - [3.4] Tabellenverzeichnis
  - [3.5] Referenzierte Dokumente
    - [3.5.1] Dokumente der gematik
    - [3.5.2] Weitere Dokumente

### 1 Einordnung des Dokuments

### 1.1 Zielsetzung

In der Spezifikation Systemprozesse der dezentralen TI werden Leistungen der
TI-Plattform beschrieben und als Systemprozesse deklariert. Diese
Systemprozesse beschreiben wie mit Produkttypen der TI zu verfahren ist, um
eine Plattformleistung für Fachanwendungen der TI zu erbringen. Diese Lösung
hat das Ziel, Basisleistungen der TI-Plattform einheitlich und
produkttypunabhängig zu definieren.

### 1.2 Zielgruppe

Das Dokument richtet sich an Hersteller von Produkten der TI, welche
fachanwendungsspezifische Funktionalitäten implementieren dafür auf
dezentrale Komponenten der TI-Plattform bzw. Dienste der TI-Plattform zugreifen
und zu deren Umsetzung die Systemprozesse dezentrale TI nutzen.

### 1.3 Geltungsbereich

Dieses Dokument enthält normative Festlegungen zur Telematikinfrastruktur des
Deutschen Gesundheitswesens. Der Gültigkeitszeitraum der vorliegenden Version
und deren Anwendung in Zulassungs- oder Abnahmeverfahren wird durch die gematik
GmbH in gesonderten Dokumenten (z.B. Dokumentenlandkarte, Produkttypsteckbrief,
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

Die Nutzung der Systemprozesse dezentrale TI wird produkttypspezifisch
festgelegt. Bspw. haben die Produkttypen Konnektor, eHealth-KT und Mob-KT
individuelle Spezifikationen und nutzen die Systemprozesse dezentrale TI nicht.

### 1.5 Methodik

Anforderungen als Ausdruck normativer Festlegungen werden durch eine eindeutige
ID sowie die dem RFC 2119 [RFC2119] entsprechenden, in Großbuchstaben
geschriebenen deutschen Schlüsselworte MUSS, DARF NICHT, SOLL, SOLL NICHT,
KANN gekennzeichnet.

Anforderungen werden im Dokument wie folgt dargestellt:\<AFO-ID\> - \<Titel der
Afo\>Text / Beschreibung [\<=]

Dabei umfasst die Anforderung sämtliche zwischen Afo-ID und Textmarke [\<=]
angeführten Inhalte.

### 2 Leistungen

Produkttypen der dezentralen TI, welche Anwendungsfälle der Fachanwendungen
umsetzen, nutzen dafür Komponenten der TI-Plattform, bspw. beim Zugriff auf
Sicherheitsmodule wie Smartcards (eGK, SMC-B, …) oder ein HSM, Verwendung von
Zertifikaten der TI oder Nutzung von Signatur-, Verzeichnis-, Zeit- und
Namensdienst im zentralen Netz. In dieser Spezifikation werden die Leistungen
der TI-Plattform einheitlich und produkttypunabhängig beschrieben und als
Systemprozesse der dezentralen TI deklariert.

Durch das Zusammenschalten von Operationen und Bausteinen der verschiedenen
Fachdomänen der TI-Plattform (Kartenzugriff, PKI, Kryptografische Verfahren)
entstehen höherwertige Plattformbausteine mit einer vereinheitlichten Syntax
für den Zugriff auf produkttypübergreifende Plattformleistungen
(„PL_TUC_*“). Den Zusammenhang der verschiedenen Domänen und den damit
komponierten höherwertigen Systemprozessen verdeutlicht die folgende Abbildung
alstechnische Dokumentenlandkarte(in der Darstellunggrünmarkiert).

![Abbildung-1][Abbildung-1]

Die Beschreibung dieser Systemprozesse der TI erfolgt normativ, es wird jedoch
auf eine prozedurale Ablaufbeschreibung verzichtet. Es erfolgt eine Festlegung,
was zu tun ist, um eine vorgegebene Plattformleistung zu erbringen. Die
konkrete Realisierung dieser Leistung eines Systemprozesses ist abhängig von
Umgebungsannahmen und muss unter bestimmten Bedingungen um umgebungsspezifische
Operationen und Festlegungen ergänzt werden. Sie sorgen für einen
umgebungsspezifischen Zuschnitt (tayloring) der Systemprozesse, um eine
TI-übergreifend spezifizierte Leistung in einer konkreten Ablaufumgebung von
einem konkreten Produkttypen oder Dienst einer Fachanwendung zu erbringen.

Die umgebungsspezifischen Operationen, Umgebungsannahmen oder -parameter müssen
von der Realisierungsumgebung („ENV_TUC_*“) normativ festgelegt werden. Der
Produkttyp, der die hier spezifizierten Plattformleistungen nutzt, muss
Festlegungen treffen, wie diese umgebungsabhängigen Schnittstellen zu
implementieren sind. Damit ergibt sich für die Realisierung der Systemprozesse
in einer konkreten Fachanwendung für eine konkrete Realisierungsumgebung ein
Spezifikationsanteil, der in der folgenden Abbildungorangegekennzeichnet ist.

![Abbildung-2][Abbildung-2]

### 2.1 Systemprozesse für den Zugriff auf Smartcards der TI

Der Zugriff auf Smartcards der TI wird in verschiedenen Produkttypen der TI
durch einen CardProxy gemäß [gemSpec_CardProxy] gekapselt. Der CardProxy
kommuniziert pro Instanz mit einer einzelnen eGK, SM-B, mit einem HBA oder
einer anderen entsprechenden Karte. Der CardProxy stellt Anwendungen eine
höherwertige Schnittstelle für den Zugriff auf eine Karte zur Verfügung und
übersetzt die parametrisierbaren Operationen in kartenverständliche
APDU-Sequenzen. Der CardProxy verwaltet intern den Freischaltstatus der Karte
und organisiert bei technischer Notwendigkeit einer PIN-Eingabe oder
Freischaltung durch eine weitere Karte auf Basis von Zugriffsregeln und dem
aktuellen Freischaltzustand eines Artefakts auf der Karte.

Die Kommunikation mit dem CardProxy wird durch die hier beschriebenen
Plattformbausteine gekapselt. Die Plattformbausteine leiten die Aufrufe an den
CardProxy weiter der zum einen eine höherwertige Kartenoperationen
alscardOperationbereitstellt und zum anderen eine direkte, bei Bedarf auf eine
verschlüsselte, Kommunikation mit der Karte überAPDU-Sequenzen erlaubt. In
der Schnittstelle zur cardOperation sind sämtliche kartenspezifischen Aspekte
gekapselt, jede Aktion auf und mit der Karte wird auf die jeweils angegebenen
Rückgabewerte abgebildet. In der direkten Kommunikation über einen
transparenten Kanal erfolgt keine Auswertung der zur und von der Karte
übertragenen APDU-Kommandos.

### 2.1.1 Die Realisierungsumgebung des CardProxy

Der CardProxy benötigt einen Zugriff auf Umgebungsschnittstellen, die je nach
Einsatzumgebung der Karten unterschiedlich ausgeprägt sind. Der CardProxy
benötigt eine Transportschnittstelle der physischen Anbindung zur Karte, einen
Kommunikationskanal zu einem Remote-CardProxy mit einer zweiten Karte für eine
Freischaltung nach dem Zwei-Schlüssel-Prinzip (Card-2-Card) und eine
Schnittstelle zur Eingabe eines PIN-Geheimnisses.

### 2.1.1.1 ENV_TUC_CARD_SECRET_INPUT – Realisierung Eingabe PIN-Geheimnis

Das System zur Umsetzung der Plattformleistungen zur Anbindung der Karte muss
für seine konkrete Realisierungsumgebung festlegen, wie PIN- bzw.
PUK-Geheimnisse von einem Benutzerinterface an die Karte gelangen.

**TIP1-A_6889 - Eingabeschnittstelle für PIN**

Das System zur Umsetzung der Plattformleistungen PL_TUC_CARD_* MUSS eine
Eingabeschnittstelle definieren, mittels der die Eingabe eines PIN-Geheimnisses
an der Schnittstelle CardProxy und Kartenterminal gemäß
[gemSpec_CardProxy#Schnittstelle CardProxy und Kartenleser] übergeben wird.
**[\<=]**

**TIP1-A_6890 - Eingabeschnittstelle für PUK**

Das System zur Umsetzung der Plattformleistungen PL_TUC_CARD_* MUSS eine
Eingabeschnittstelle definieren, mittels der die Eingabe eines PUK-Geheimnisses
an der Schnittstelle CardProxy und Kartenterminal gemäß
[gemSpec_CardProxy#Schnittstelle CardProxy und Kartenleser] übergeben wird.
**[\<=]**

**TIP1-A_6891 - Eingabeschnittstelle für newPIN**

Das System zur Umsetzung der Plattformleistungen PL_TUC_CARD_* MUSS eine
Eingabeschnittstelle definieren, mittels der die Eingabe eines neuen
PIN-Geheimnisses an der Schnittstelle CardProxy und Kartenterminal gemäß
[gemSpec_CardProxy#Schnittstelle CardProxy und Kartenleser] übergeben wird.
**[\<=]**

**TIP1-A_7017 - Statusinformationen im Rahmen der PIN-Verifikation**

Produkttypen und Dienste der TI die eine PIN/PUK-Eingabe mittels
ENV_TUC_CARD_SECRET_INPUT umsetzen, MÜSSEN das Ergebnis gemäß
[gemSpec_CardProxy#Sicherheitszustand] zurückmelden:

 ---> OL

**[\<=]**

### 2.1.1.2 ENV_TUC_CARD_TO_CARD – Realisierung Card-2-Card

Das System zur Umsetzung der Plattformleistungen zur Anbindung der Karte muss
für seine konkrete Realisierungsumgebung festlegen, wie der Datentransport
innerhalb einer Card-2-Card-Freischaltung zwischen zwei beteiligten Karten
erfolgt.

**TIP1-A_6892 - Umgebungsschnittstelle für Card-2-Card**

Das System zur Umsetzung der Plattformleistungen PL_TUC_CARD_* MUSS eine
Transportschnittstelle „Umgebung“ definieren, mittels welcher der
Datenaustausch von Challenge und Response im Card-2-Card-Verfahren zwischen
zwei CardProxy-Instanzen von CardProxy_A an CardProxy_B gemäß
[gemSpec_CardProxy#Sicherheitszustand#Card-2-Card] realisiert wird. **[\<=]**

**TIP1-A_7018 - Statusinformationen im Rahmen von Card-2-Card**

Produkttypen und Dienste der TI die eine Card-2-Card-Freischaltung mittels
ENV_TUC_CARD_TO_CARD umsetzen, MÜSSEN das Ergebnis gemäß
[gemSpec_CardProxy#Sicherheitszustand] zurückmelden:

 ---> OL

**[\<=]**

### 2.1.1.3 ENV_TUC_CARD_APDU_TRANSPORT – Realisierung APDU-Transport

Das System zur Umsetzung der Plattformleistungen zur Anbindung der Karte muss
für seine konkrete Realisierungsumgebung festlegen, wie die elektrische
Schnittstelle zwischen CardProxy und Karte als Kartenkontaktiereinheit IFD
realisiert wird.

**TIP1-A_6893 - Umgebungsschnittstelle für Kartenkommandos**

Das System zur Umsetzung der Plattformleistungen PL_TUC_CARD_* MUSS eine
Schnittstelle realisieren, mittels welcher der Transport der APDU-Kommandos
zwischen CardProxy und Karte gemäß [gemSpec_CardProxy Konzept der Komponente
Kartenterminal Proxy] über eine Kartenkontaktiereinheit gemäß [ISO7816-3]
realisiert wird. **[\<=]**

### 2.1.2 Konfiguration und Statusinformationen

Um die korrekte Funktionsweise einer CardProxy-Instanz in einer konkreten
Realisierungsumgebung sicherzustellen, ist eine Konfiguration und
Initialisierung des CardProxies erforderlich. Es muss festgelegt werden,
welchen Kartentyp eine jeweilige CardProxy-Instanz unterstützen soll und
welche Operation auf welchen Objekten der jeweiligen Karte in einer Anwendung
zulässig sind.

### 2.1.2.1 Konfiguration des CardProxy

**TIP1-A_6894 - Konfiguration des Kartenzugriffs**

Das System zur Umsetzung der Kartenzugriffe mittels CardProxy MUSS für seine
Realisierungsumgebung eine Konfigurationstabelle gemäß
[gemSpec_CardProxy#Konfigurationstabelle CardProxy] für jeden unterstützten
Kartentyp einer SmartCard der TI definieren. **[\<=]**

Die Konfigurationstabelle legt die zulässigen Operationen für jeden
unterstützten Kartentyp in einer konkreten Realisierungsumgebung fest. Um eine
Eindeutigkeit in der Auswahl einer passenden Zugriffsregel eines Objektes auf
der Karte zu erhalten, muss der Nutzer der Plattformleistung festlegen, in
welchen Rollen ein Akteur in Anwendungsfällen mit Bezug zu einer Karte der TI
interagieren kann.

**TIP1-A_7019 - Konfiguration der Rollen des Benutzers einer Karte**

Das System zur Umsetzung der Plattformleistungen für Systemprozesse der
TI-Plattform MUSS für seine Realisierungsumgebung festlegen, welche Rollen ein
Benutzer in Anwendungsfällen mit Bezug auf eine Karte der TI einnehmen darf.
**[\<=]**

**TIP1-A_6895 - Festlegung des Zugriffsprofils zur Rollenauthentisierung
gegenüber einer eGK**

Das System zur Umsetzung der Plattformleistungen für Systemprozesse der
TI-Plattform MUSS festlegen, welche Zugriffe eine SmartCard (HBA, SM-B) bei der
Rollenauthentisierung gegenüber einer eGK in seiner konkreten
Realisierungsumgebung freischalten darf. **[\<=]**

Mit dieser Anforderung wird sichergestellt, dass die zum Einsatz kommenden
Karten über die entsprechenden Zertifikate zur Rollenauthentisierung
gegenüber einer eGK verfügen. Diese Rollen bilden Zugriffsrechte auf der eGK
ab, die in der Konfigurationstabelle für den CardProxy verzeichnet sind.

### 2.1.2.2 Initialisierung CardProxy für eGK

Bei der Initialisierung des CardProxy in dessen Zugriff sich eine eGK befindet,
soll die komplette CV-Zertifikatskette einer in der Realisierungsumgebung
vorgehaltenen SM-B, die für die Freischaltung der eGK vorgesehen ist,
übergeben werden. Daraus ergibt sich, dass die in der Realisierungsumgebung
eingesetzte SM-B bereits über einen initialisierten CardProxy adressiert
werden kann. Die Instanz des CardProxy mit eGK muss mit der Referenz der SM-B
der übergebenen SM-B-CV-Zertifikatskette und dem bei der Initialisierung des
SM-B-CardProxy ausgelesenen X.509-AUT-Zertifikats assoziiert werden.

**TIP1-A_6896 - Initialisierung CardProxy für eGK**

Das System zur Umsetzung der Plattformleistungen für Systemprozesse der
TI-Plattform MUSS bei der Initialisierung des CardProxies mit Zugriff auf eine
eGK

 ---> UL

**[\<=]**

### 2.1.2.3 Initialisierung CardProxy für SM-B

Bei der Initialisierung des CardProxy in dessen Zugriff sich eine SM-B befindet,
soll die SM-B mittels PIN-Eingabe freigeschaltet werden sowie das CV- und das
X.509-AUT-Zertifikat ausgelesen werden.

**TIP1-A_6897 - Initialisierung CardProxy für SM-B**

Das System zur Umsetzung der Plattformleistungen für Systemprozesse der
TI-Plattform MUSS bei der Initialisierung des CardProxies mit Zugriff auf eine
SM-B

 ---> UL

**[\<=]**

### 2.1.2.4 PL_TUC_CARD_INFORMATION – Gesammelte Statusinformationen zu einer Karte

Der Systemprozess PL_TUC_CARD_INFORMATION sammelt Statusinformationen zu einer
SmartCard, die über eine umgebungsspezifische Schnittstelle an das System
angebunden wird und stellt diese zum Abruf durch andere Systemprozesse bereit.
Die Informationen umfassen zum einen Auskünfte über Kartentyp und
Kartengeneration bzw. -version und zum anderen Statusinformationen über auf
der Karte vorhandene Anwendungen und PINs.

**TIP1-A_6898 - Leistung zu Statusinformationen zu einer Karte**

Produkttypen und Dienste der TI mit Zugriff auf Smartcards der TI MÜSSEN eine
Plattformleistung PL_TUC_CARD_INFORMATION realisieren und mit
Statusinformationen einer SmartCard befüllen, die über die
Umgebungsschnittstelle ENV_TUC_CARD_APDU_TRANSPORT mit dem System verbunden
wird. **[\<=]**

**TIP1-A_6899 - Liste verfügbarer Informationen zu einer SmartCard**

Produkttypen und Dienste der TI die eine Plattformleistung
PL_TUC_CARD_INFORMATION umsetzen, MÜSSEN die folgenden Informationen zum
Status einer angebundenen SmartCard sammeln, bei Änderung aktualisieren und
für die Dauer der Verbindung zu dieser SmartCard zum Abruf bereitstellen.
**[\<=]**

### 2.1.2.5 PL_TUC_EGK_STATUS – Gültigkeit der eGK prüfen

Der Systemprozess PL_TUC_EGK_STATUS fasst Leistungen verschiedener Domänen
unter Einbeziehung einer elektronischen Gesundheitskarte zu einer
höherwertigen Plattformleistung zusammen. Mit dieser wird eine
Gültigkeitsprüfung der eGK durchgeführt, die zum einen Prüfschritte direkt
auf der Karte durchführt und andererseits die Legitimität der Karte mittels
Onlineabfrage beim Kartenherausgeber prüft.

**TIP1-A_6901 - Prüfkriterien der Gültigkeit der eGK**

Produkttypen und Dienste der TI mit Zugriff auf eine elektronische
Gesundheitskarte mittels CardProxy MÜSSEN eine Plattformleistung
PL_TUC_EGK_STATUS zur Prüfung des Status einer eGK umsetzen, die die eGK den
folgenden Prüfkriterien unterzieht:

<table><tr><th>
Prüfkriterium

</th><th>
Prüfergebnis

</th></tr><tr><td>
Abbildung des Werts zur Echtheit der Karte
inPL_TUC_CARD_INFORMATION.Echtheitaufden Wahrheitswertjawenn die Karte für
echt befunden wurde, sonstnein.

</td><td>
Echtheit:ja / nein

</td></tr><tr><td>
Abbildung des Status der Gesundheitsanwendung auf der eGK
inPL_TUC_CARD_INFORMATION.DF.HCAauf den Wert„aktiv“, wenn Status =
AVAILABLE„nicht aktiv“,     wenn Status ungleich AVAILABLE

</td><td>
Gesundheits-anwendung:aktiv / nicht aktiv / Prüffehler

</td></tr><tr><td>
Prüfung der Gültigkeit des Zertifikats der Karteninhaberidentität C.CH.AUTN
der eGK aus PL_TUC_CARD_INFORMATION mittels PL_TUC_PKI_VERIFY_CERTIFICATE unter
Verwendung der folgenden Parameter:

 ---> UL

</td><td>
Gültigkeit zu Referenzzeitpunkt:„zeitlich gültig / ungültig“ /
PrüffehlerMathematische Gültigkeit:„mathematisch gültig / ungültig“ /
PrüffehlerOCSP-Prüfung:„Online gültig / Online gesperrt / nicht geprüft /
Prüffehler“

</td></tr></table>

**[\<=]**

**TIP1-A_6902 - Prüfergebnis der Echtheit_und_Gültigkeit der eGK**

Produkttypen und Dienste der TI MÜSSEN zur Realisierung von PL_EGK_STATUS über
das Ergebnis jedes Prüfkriteriums der Echtheit- und Gültigkeitsprüfung der
eGK informieren und mit einem Status die erfolgreiche Prüfung aller Kriterien
mitteilen.

 ---> OL

**[\<=]**

### 2.1.2.6 PL_TUC_CARD_RESET – Rücksetzen einer Karte

Mit dem Systemprozess PL_TUC_CARD_RESET soll der logische Kanal einer im Zugriff
eines CardProxy befindlichen SmartCard der TI auf den Initialisierungsstand
zurückgesetzt werden.

**TIP1-A_7020 - Leistung zum Rücksetzen einer Karte**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN das
Rücksetzen des logischen Kanals einer SmartCard als Plattformleistung
PL_TUC_CARD_RESET gemäß [gemSpec_CardProxy]cardOperationmit dem
AktionsparameterRESETCHANNELund dem IDENTIFIKATOR „*“ (Wildcard) umsetzen
und das Abschließen dieser Aktion mit dem RückgabewertOKbestätigen. **[\<=]**

### 2.1.3 Zugriff auf Smartcards der TI

Der folgende Abschnitt definiert Systemprozesse für den Zugriff auf Smartcards
der TI als funktionale Abläufe. Voraussetzung für die korrekte Funktionsweise
sind zum einen umgebungsspezifische Abläufe an den Außenschnittstellen, die
von der jeweiligen Realisierungsumgebung festgelegt werden müssen. Zum anderen
muss für die jeweils durch einen CardProxy adressierbaren Karten eine
Konfigurationstabelle der zulässigen Kartenoperationen definiert werden.

### 2.1.3.1 PL_TUC_CARD_CHANGE_PIN – PIN Ändern

**TIP1-A_6903 - Leistung zur Änderung einer PIN**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN das
Ändern einer PIN auf einer SmartCard als Plattformleistung
PL_TUC_CARD_CHANGE_PIN gemäß [gemSpec_CardProxy]cardOperation für
Passwortobjektemit dem AktionsparameterCHANGEumsetzen. **[\<=]**

**TIP1-A_6904 - Aufrufparameter zum Ändern einer PIN**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_CARD_CHANGE_PIN umsetzen, MÜSSEN vom Nutzenden denIDENTIFIKATORdes
Passwortobjektes gemäß [gemSpec_CardProxy#Konfigurationstabelle CardProxy]
entgegennehmen und in der Umsetzung voncardOperationverwenden. **[\<=]**

**TIP1-A_6905-01 - Ergebnis der Änderung einer PIN**

Produkttypen und Dienste der TI die eine Plattformleistung
PL_TUC_CARD_CHANGE_PIN umsetzen, MÜSSEN das Ergebnis gemäß
[gemSpec_CardProxy]cardOperationzurückmelden:

 ---> OL

**[\<=]**

Durch den Systemprozess PL_TUC_CARD_CHANGE_PIN wird das PIN-Geheimnis einer
referenzierten PIN auf einer SmartCard der TI geändert.

### 2.1.3.2 PL_TUC_CARD_ENABLE_PIN – PIN-Schutz einschalten

Mit dem Systemprozess PL_TUC_CARD_ENABLE_PIN wird die PIN-Verifikation der
referenzierten PIN eingeschaltet.

**TIP1-A_6906 - Leistung zum Einschalten einer PIN**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN das
Einschalten einer PIN auf einer SmartCard als Plattformleistung
PL_TUC_CARD_ENABLE_PIN gemäß [gemSpec_CardProxy]cardOperation für
Passwortobjektemit dem AktionsparameterENABLEumsetzen. **[\<=]**

**TIP1-A_6907 - Aufrufparameter zum Einschalten einer PIN**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_CARD_ENABLE_PIN umsetzen, MÜSSEN vom Nutzenden denIDENTIFIKATORdes
Passwortobjektes gemäß [gemSpec_CardProxy#Konfigurationstabelle CardProxy]
entgegennehmen und in der Umsetzung voncardOperationverwenden. **[\<=]**

**TIP1-A_6908 - Ergebnis des Einschaltens einer PIN**

Produkttypen und Dienste der TI die eine Plattformleistung
PL_TUC_CARD_ENABLE_PIN umsetzen, MÜSSEN das Ergebnis gemäß
[gemSpec_CardProxy]cardOperationzurückmelden:

 ---> OL

**[\<=]**

### 2.1.3.3 PL_TUC_CARD_DISABLE_PIN – PIN-Schutz abschalten

**TIP1-A_6909 - Leistung zum Abschalten einer PIN**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN das
Abschalten einer PIN auf einer SmartCard als Plattformleistung
PL_TUC_CARD_DISABLE_PIN gemäß [gemSpec_CardProxy]cardOperation für
Passwortobjektemit dem AktionsparameterDISABLEumsetzen. **[\<=]**

**TIP1-A_6910 - Aufrufparameter zum Abschalten einer PIN**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_CARD_DISABLE_PIN umsetzen, MÜSSEN vom Nutzenden denIDENTIFIKATORdes
Passwortobjektes gemäß [gemSpec_CardProxy#Konfigurationstabelle CardProxy]
entgegennehmen und in der Umsetzung voncardOperationverwenden. **[\<=]**

**TIP1-A_6911 - Ergebnis des Abschaltens einer PIN**

Produkttypen und Dienste der TI die eine Plattformleistung
PL_TUC_CARD_DISABLE_PIN umsetzen, MÜSSEN das Ergebnis gemäß
[gemSpec_CardProxy]cardOperationzurückmelden:

 ---> OL

**[\<=]**

Mit dem Systemprozess PL_TUC_CARD_DISABLE_PIN wird die PIN-Verifikation einer
referenzierten PIN abgeschaltet. Objekte auf einer SmartCard mit
Zugriffsbedingungen, die die referenzierte PIN enthalten, sind bei
abgeschalteter PIN weniger geschützt.

### 2.1.3.4 PL_TUC_CARD_UNBLOCK_PIN – PIN mit PUK entsperren

**TIP1-A_6912 - Leistung zum Entsperren einer PIN mittels PUK**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN das
Entsperren einer PIN auf einer SmartCard als Plattformleistung
PL_TUC_CARD_UNBLOCK_PIN gemäß [gemSpec_CardProxy]cardOperation für
Passwortobjektemit dem AktionsparameterUNBLOCKumsetzen. **[\<=]**

**TIP1-A_6913 - Aufrufparameter zum Entsperren einer PIN mittels PUK**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_CARD_UNBLOCK_PIN umsetzen, MÜSSEN vom Nutzenden denIDENTIFIKATORdes
Passwortobjektes gemäß [gemSpec_CardProxy#Konfigurationstabelle CardProxy]
entgegennehmen und in der Umsetzung voncardOperationverwenden. **[\<=]**

**TIP1-A_6914 - Ergebnis der Entsperrung einer PIN mittels PUK**

Produkttypen und Dienste der TI die eine Plattformleistung
PL_TUC_CARD_UNBLOCK_PIN umsetzen, MÜSSEN das Ergebnis gemäß
[gemSpec_CardProxy]cardOperationzurückmelden:

 ---> OL

**[\<=]**

Mit dem Systemprozess PL_TUC_CARD_UNBLOCK_PIN wird eine gesperrte PIN entsperrt.
Das Entsperren kann mit gleichzeitigem Setzen einer neuen PIN oder ohne das
setzen einer neuen PIN erfolgen. Der Modus der Entsperrung erfolgt auf
Grundlage der Festlegungen in der Konfiguration des CardProxies für einen
bestimmten Kartentypen.

### 2.1.3.5 PL_TUC_CARD_VERIFY_PIN – Benutzer verifizieren

**TIP1-A_6915 - Leistung zur Benutzerverifikation**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN eine
Benutzerverifikation mittels PIN als Plattformleistung PL_TUC_CARD_VERIFY_PIN
gemäß [gemSpec_CardProxy]cardOperation für Passwortobjektemit dem
AktionsparameterVERIFYumsetzen. **[\<=]**

**TIP1-A_6916 - Aufrufparameter der Benutzerverifikation**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_CARD_VERIFY_PIN umsetzen, MÜSSEN vom Nutzenden denIDENTIFIKATORdes
Passwortobjektes gemäß [gemSpec_CardProxy#Konfigurationstabelle CardProxy]
entgegennehmen und in der Umsetzung voncardOperationverwenden. **[\<=]**

**TIP1-A_6917 - Ergebnis der Leistung zur Eingabe einer PIN**

Produkttypen und Dienste der TI die eine Plattformleistung
PL_TUC_CARD_VERIFY_PIN umsetzen, MÜSSEN das Ergebnis gemäß
[gemSpec_CardProxy]cardOperationzurückmelden:

 ---> OL

**[\<=]**

Der Systemprozess PL_TUC_CARD_VERIFY_PIN führt eine kartenbasierte
Benutzerverifikation durch. Dazu wird auf einer SmartCard der TI eine
PIN-Eingabe angestoßen, über die sich ein Benutzer als Besitzer des
Kartengeheimnisses authentifiziert.

### 2.1.3.6 PL_TUC_CARD_ACTIVATE_APPLICATION – Anwendung aktivieren

**TIP1-A_6918 - Leistung zum Aktivieren einer Anwendung**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN das
Sichtbarmachen einer Anwendung auf einer SmartCard als Plattformleistung
PL_TUC_CARD_ACTIVATE_APPLICATION gemäß [gemSpec_CardProxy]cardOperation für
Ordnermit dem AktionsparameterACTIVATEumsetzen. **[\<=]**

**TIP1-A_6919 - Aufrufparameter zum Aktivieren einer Anwendung**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_CARD_ACTIVATE_APPLICATION umsetzen, MÜSSEN vom Nutzenden
denIDENTIFIKATORder Anwendung gemäß [gemSpec_CardProxy#Konfigurationstabelle
CardProxy] entgegennehmen und in der Umsetzung voncardOperationverwenden.
**[\<=]**

**TIP1-A_6920 - Ergebnis der Leistung zur Aktivieren einer Anwendung**

Produkttypen und Dienste der TI die eine Plattformleistung
PL_TUC_CARD_ACTIVATE_APPLICATION umsetzen, MÜSSEN das Ergebnis gemäß
[gemSpec_CardProxy]cardOperationzurückmelden:

 ---> OL

**[\<=]**

Der Systemprozess PL_TUC_CARD_ACTIVATE_APPLICATION schaltet eine verborgene
Anwendung auf einer SmartCard sichtbar.

### 2.1.3.7 PL_TUC_CARD_DEACTIVATE_APPLICATION – Anwendung deaktivieren

**TIP1-A_6921 - Leistung zum Deaktivieren einer Anwendung**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN das
Verbergen einer Anwendung auf einer SmartCard als Plattformleistung
PL_TUC_CARD_DEACTIVATE_APPLICATION gemäß [gemSpec_CardProxy]cardOperation
für Ordnermit dem Aktionsparameter DEACTIVATEumsetzen. **[\<=]**

**TIP1-A_6922 - Aufrufparameter zum Deaktivieren einer Anwendung**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_CARD_DEACTIVATE_APPLICATION umsetzen, MÜSSEN vom Nutzenden
denIDENTIFIKATORder Anwendung gemäß [gemSpec_CardProxy#Konfigurationstabelle
CardProxy] entgegennehmen und in der Umsetzung voncardOperationverwenden.
**[\<=]**

**TIP1-A_6923 - Ergebnis der Leistung zur Deaktivieren einer Anwendung**

Produkttypen und Dienste der TI die eine Plattformleistung
PL_TUC_CARD_DEACTIVATE_APPLICATION umsetzen, MÜSSEN das Ergebnis gemäß
[gemSpec_CardProxy]cardOperationzurückmelden:

 ---> OL

**[\<=]**

Mit dem Systemprozess PL_CAR_DEACTIVATE_APPLICATION wird eine Anwendung auf
einer SmartCard verborgen.

### 2.1.3.8 PL_TUC_CARD_GET_CHALLENGE – Auslesen einer Zufallszahl

**TIP1-A_6924 - Leistung zum Auslesen einer Zufallszahl**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN das
Auslesen einer Zufallszahl gemäß [gemSpec_Krypt#2.2
Zufallszahlengeneratoren]als Plattformleistung
PL_TUC_GET_CHALLENGE umsetzen. Bei Verwendung einer SmartCard MUSS dies
gemäß [gemSpec_CardProxy] mittels cardOperation für Ordnermit dem
AktionsparameterGETRANDOMund dem IDENTIFIKATOR„*“(Wildcard) erfolgen. Bei
Verwendung eines HSM MUSS dies unter Verwendung der durch das HSM
bereitgestellten Zufallszahlengenerierung erfolgen. **[\<=]**

**TIP1-A_6925 - Aufrufparameter für das Auslesen einer Zufallszahl**

Produkttypen und Dienste der TI, die eine Plattformleistung PL_TUC_GET_CHALLENGE
unter Verwendung einer SmartCard umsetzen, MÜSSEN vom Nutzer die
LängenangabeLENGTHder auszulesenden Zufallszahl gemäß [gemSpec_CardProxy]
entgegennehmen und in der Umsetzung voncardOperationverwenden. **[\<=]**

**TIP1-A_6926 - Ergebnis des Auslesens einer Zufallszahl**

Produkttypen und Dienste der TI die eine Plattformleistung PL_TUC_GET_CHALLENGE
umsetzen, MÜSSEN das Ergebnis gemäß
[gemSpec_CardProxy]cardOperationzurückmelden:

 ---> OL

**[\<=]**

Mit dem Systemprozess PL_TUC_GET_CHALLENGE kann eine Zufallszahl ausgelesen
werden. Bei Verwendung einer elektronischen Gesundheitskarte genügt die
Qualität der Zufallszahl zur Ableitung ephemerer Schlüsselparameter.

### 2.1.3.9 PL_TUC_CARD_READ_FILE – Lesen von Daten aus einer SmartCard

**TIP1-A_6927 - Leistung zum Lesen einer Datei**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN das
Lesen des Inhalts einer Datei auf einer SmartCard als Plattformleistung
PL_TUC_CARD_READ_FILE gemäß [gemSpec_CardProxy]cardOperation für
transparente Elementary Filesmit dem AktionsparameterREADumsetzen. **[\<=]**

**TIP1-A_6928 - Aufrufparameter für das Lesen einer Datei**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_CARD_READ_FILE umsetzen, MÜSSEN vom Nutzer denIDENTIFIKATORder zu
lesenden Datei gemäß [gemSpec_CardProxy#Konfigurationstabelle CardProxy]
entgegennehmen und in der Umsetzung voncardOperationverwenden. **[\<=]**

**TIP1-A_6929 - Optionale Parameter für das Lesen einer Datei**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_CARD_READ_FILE umsetzen, MÜSSEN die vom Nutzer optional
bereitgestellten ParameterOFFSETundLENGTHbei Vorhandensein entgegennehmen und
diese in der Umsetzung von [gemSpec_CardProxy]cardOperationverwenden, um die zu
lesende Datenmenge zu beschränken. **[\<=]**

**TIP1-A_6930 - Ergebnis des Lesens des Inhalts einer Datei**

Produkttypen und Dienste der TI die eine Plattformleistung PL_TUC_CARD_READ_FILE
umsetzen, MÜSSEN das Ergebnis gemäß
[gemSpec_CardProxy]cardOperationzurückmelden:

 ---> OL

**[\<=]**

Mit dem Systemprozess PL_TUC_CARD_READ_FILE werden Daten aus einer transparenten
Datei einer SmartCard gelesen. Über die Parameter Offset und Length kann
gesteuert werden, ab welcher Position in der Datei eine festgelegte Anzahl
Bytes gelesen werden. Fehlen diese Parameter, wird der komplette Dateiinhalt
ausgelesen.

### 2.1.3.10 PL_TUC_CARD_WRITE_FILE – Schreiben von Daten auf eine SmartCard

**TIP1-A_6931 - Leistung zum Schreiben von Daten in eine transparente Datei**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN das
Schreiben von Daten in eine transparente Datei auf einer SmartCard als
Plattformleistung PL_TUC_CARD_WRITE_FILE gemäß
[gemSpec_CardProxy]cardOperation für transparente Elementary Filesmit dem
AktionsparameterUPDATEund demOFFSET = 0umsetzen. **[\<=]**

**TIP1-A_6932 - Aufrufparameter für das Schreiben einer transparenten Datei**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_CARD_WRITE_FILE umsetzen, MÜSSEN vom Nutzenden denIDENTIFIKATORder zu
schreibenden Datei gemäß [gemSpec_CardProxy#Konfigurationstabelle CardProxy]
sowieNEWDATAentgegennehmen und in der Umsetzung voncardOperationverwenden.
**[\<=]**

**TIP1-A_6933 - Ergebnis des Schreibens von Datei in eine transparente Datei**

Produkttypen und Dienste der TI die eine Plattformleistung
PL_TUC_CARD_WRITE_FILE umsetzen, MÜSSEN das Ergebnis gemäß
[gemSpec_CardProxy]cardOperationzurückmelden:

 ---> OL

**[\<=]**

Mit dem Systemprozess PL_TUC_CARD_WRITE_FILE werden Binärdaten in eine
transparente Datei einer SmartCard geschrieben. Die Schreiboperation fügt die
neuen Daten an eventuell vorhandene Daten an.

### 2.1.3.11 PL_TUC_CARD_UPDATE_FILE – Aktualisieren von Daten in einer transparenten Datei einer SmartCard

**TIP1-A_6934 - Leistung zum Aktualisieren von Daten in einer transparenten
Datei**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN das
Aktualisieren von Daten in einer transparenten Datei auf einer SmartCard als
Plattformleistung PL_TUC_CARD_UPDATE_FILE gemäß
[gemSpec_CardProxy]cardOperation für transparente Elementary Filesmit dem
AktionsparameterUPDATEumsetzen. **[\<=]**

**TIP1-A_6935 - Aufrufparameter zum Aktualisieren von Daten in einer
transparenten Datei**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_CARD_UPDATE_FILE umsetzen, MÜSSEN vom Nutzenden denIDENTIFIKATORder zu
aktualisierenden Datei gemäß [gemSpec_CardProxy#Konfigurationstabelle
CardProxy] sowieNEWDATAentgegennehmen und in der Umsetzung
voncardOperationverwenden. **[\<=]**

**TIP1-A_6936 - Optionaler Parameter für das Aktualisieren von Datei in einer
transparenten Datei**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_CARD_READ_FILE umsetzen, MÜSSEN den vom Nutzenden optional
bereitgestellten ParameterOFFSETbei Vorhandensein entgegennehmen und diesen in
der Umsetzung von [gemSpec_CardProxy]cardOperationverwenden, um die
Startposition der Schreiboperation innerhalb der Datei festzulegen. **[\<=]**

**TIP1-A_6937 - Ergebnis der Aktualisierung von Daten einer transparenten Datei**

Produkttypen und Dienste der TI die eine Plattformleistung
PL_TUC_CARD_UDPATE_FILE umsetzen, MÜSSEN das Ergebnis gemäß
[gemSpec_CardProxy]cardOperationzurückmelden:

 ---> OL

**[\<=]**

Mit dem Systemprozess PL_TUC_CARD_UPDATE_FILE werden Binärdaten in eine
transparente Datei einer SmartCard geschrieben, so dass vorhandene Daten
überschrieben werden. Über den Parameter Offset kann gesteuert werden, ab
welcher Position in der Datei die neuen Daten geschrieben werden. Fehlt dieser
Parameter, beginnt die Schreiboperation am Anfang der Datei.

### 2.1.3.12 PL_TUC_CARD_DELETE_FILE – Löschen von Daten auf einer SmartCard

**TIP1-A_6938 - Leistung des Löschens einer transparenten Datei**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN das
Löschen einer transparenten Datei auf einer SmartCard als Plattformleistung
PL_TUC_CARD_DELETE_FILE gemäß [gemSpec_CardProxy]cardOperation für
transparente Elementary Filesmit dem AktionsparameterDELETEumsetzen. **[\<=]**

**TIP1-A_6939 - Aufrufparameter zum Löschen einer transparenten Datei**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_CARD_DELETE_FILE umsetzen, MÜSSEN vom Nutzenden denIDENTIFIKATORder zu
löschenden Datei gemäß [gemSpec_CardProxy#Konfigurationstabelle CardProxy]
entgegennehmen und in der Umsetzung voncardOperationverwenden. **[\<=]**

**TIP1-A_6940 - Ergebnis der Löschoperation einer transparenten Datei**

Produkttypen und Dienste der TI die eine Plattformleistung
PL_TUC_CARD_DELETE_FILE umsetzen, MÜSSEN das Ergebnis gemäß
[gemSpec_CardProxy]cardOperationzurückmelden:

 ---> OL

**[\<=]**

Der Systemprozess PL_TUC_CARD_DELETE_FILE entfernt eine transparente Datei auf
einer SmartCard samt Dateiinhalt. Die gelöschte Datei ist im Anschluss nicht
mehr adressierbar.

### 2.1.3.13 PL_TUC_CARD_ERASE_FILE – Rücksetzen des Inhalts einer transparenten Datei

Der Systemprozess PL_TUC_CARD_ERASE_FILE entfernt den Inhalt einer transparenten
Datei. Die adressierte Datei ist weiterhin verwendbar.

**TIP1-A_6941 - Leistung zum Rücksetzen einer transparenten Datei**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN das
Rücksetzen des Dateiinhalts einer transparenten Datei auf einer SmartCard als
Plattformleistung PL_TUC_CARD_ERASE_FILE gemäß
[gemSpec_CardProxy]cardOperation für transparente Elementary Filesmit dem
AktionsparameterERASEumsetzen. **[\<=]**

**TIP1-A_6942 - Aufrufparameter zum Rücksetzen einer transparenten Datei**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_CARD_ERASE_FILE umsetzen, MÜSSEN vom Nutzenden denIDENTIFIKATORder
zurückzusetzenden Datei gemäß [gemSpec_CardProxy#Konfigurationstabelle
CardProxy] entgegennehmen und in der Umsetzung voncardOperationverwenden.
**[\<=]**

**TIP1-A_6943 - Optionaler Parameter für das Rücksetzen des Inhalts einer
transparenten Datei**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_CARD_ERASE_FILE umsetzen, MÜSSEN den vom Nutzenden optional
bereitgestellten ParameterOFFSETbei Vorhandensein entgegennehmen und dieses in
der Umsetzung von [gemSpec_CardProxy]cardOperationverwenden, um die
Startposition der Operation innerhalb der Datei festzulegen. **[\<=]**

**TIP1-A_6944 - Ergebnis des Rücksetzens einer transparenten Datei**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_CARD_ERASE_FILE umsetzen, MÜSSEN das Ergebnis gemäß
[gemSpec_CardProxy]cardOperationzurückmelden:

 ---> OL

**[\<=]**

### 2.1.3.14 PL_TUC_CARD_READ_RECORD – Lesen von Daten aus einer strukturierten Datei

Mit dem Systemprozess PL_TUC_CARD_READ_RECORD werden Daten aus einer
strukturierten Datei auf einer SmartCard ausgelesen. Über die optionale Angabe
der recordNumber wird gesteuert, ob nur ein einzelner Record oder alle Records
der strukturierten Datei gelesen werden sollen.

**TIP1-A_6945 - Leistung zum Lesen einer strukturierten Datei**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN das
Lesen einer strukturierten Datei auf einer SmartCard als Plattformleistung
PL_TUC_CARD_READ_RECORD gemäß [gemSpec_CardProxy]cardOperation für
strukturierte Elementary Filesmit dem AktionsparameterREADumsetzen. **[\<=]**

**TIP1-A_6946 - Aufrufparameter für das Lesen einer strukturierten Datei**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_CARD_READ_RECORD umsetzen, MÜSSEN vom Nutzenden denIDENTIFIKATORder zu
lesenden Datei gemäß [gemSpec_CardProxy#Konfigurationstabelle CardProxy]
entgegennehmen und in der Umsetzung voncardOperationverwenden. **[\<=]**

**TIP1-A_6947 - Optionale Parameter für das Lesen einer strukturierten Datei**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_CARD_READ_RECORD umsetzen, MÜSSEN den vom Nutzenden optional
bereitgestellten ParameterRECORDNUMBERbei Vorhandensein entgegennehmen und
diese in der Umsetzung von [gemSpec_CardProxy]cardOperationverwenden, um die zu
lesende Datenmenge zu beschränken. **[\<=]**

**TIP1-A_6948 - Ergebnis des Lesens einer strukturierten Datei**

Produkttypen und Dienste der TI die die Plattformleistung
PL_TUC_CARD_READ_RECORD umsetzen, MÜSSEN das Ergebnis gemäß
[gemSpec_CardProxy]cardOperationzurückmelden:

 ---> OL

**[\<=]**

### 2.1.3.15 PL_TUC_EGK_READ_PROTOCOL – Auslesen des Zugriffprotokolls der eGK

Mit dem Systemprozess PL_TUC_EGK_READ_PROTOCOL wird das gesamte
Zugriffsprotokoll auf der elektronischen Gesundheitskarte ausgelesen. Im
Gegensatz zur generischen Leseoperation eines strukturierten Elementary Files
wird in diesem Baustein der Zugriff auf die Karte durch die
Kartenzugriffsschicht CardProxy optimiert und es werden alle Log-Einträge
(maximal 50) in einer Liste zurückgegeben. 

**TIP1-A_6949 - Leistung zum Lesen des Zugriffprotokolls auf der eGK**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN das
Auslesen des Zugriffprotokolls auf der eGK als Plattformleistung
PL_TUC_EGK_READ_PROTOCOL gemäß [gemSpec_CardProxy]cardOperation für
strukturiertes Elementary Filemit dem AktionsparameterREADund dem
IDENTIFIKATOREF.Logginggemäß [gemSpec_CardProxy#Konfigurationstabelle
CardProxy eGK G2] umsetzen. **[\<=]**

**TIP1-A_6996 - Aufbereitung Zugriffsprotokolleinträge**

Produkttypen und Dienste der TI, die die Plattformleistung
PL_TUC_EGK_READ_PROTOCOL umsetzen, MÜSSEN alle aus der Karte gelesenen,
binär-codierten Zugriffsprotokolleinträge gemäß
[gemSpec_Karten_Fach_TIP#Tab_Karten_Fach_TIP_010_StrukturEF.Logging] in ein
strukturiertes Format überführen und die Werte entsprechend des angegeben
Datentyps decodieren. **[\<=]**

**TIP1-A_6950 - Ergebnis des Auslesens des Zugriffprotokolls der eGK**

Produkttypen und Dienste der TI, die die Plattformleistung
PL_TUC_EGK_READ_PROTOCOL umsetzen, MÜSSEN das Ergebnis gemäß
[gemSpec_CardProxy]cardOperationzurückmelden:

 ---> OL

**[\<=]**

### 2.1.3.16 PL_TUC_CARD_WRITE_RECORD – Schreiben von Daten in eine strukturierte Datei

Der Systemprozess PL_TUC_CARD_WRITE_RECORD schreibt einen Datensatz in einen
Record einer strukturierten Datei auf einer SmartCard. Enthält der zu
schreibende Record bereits Daten, wird der alte Datensatz mit dem neuen Wert
überschrieben.

**TIP1-A_6951 - Leistung zum Schreiben von Daten in eine strukturierte Datei**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN das
Schreiben eines Records einer strukturierten Datei auf einer SmartCard als
Plattformleistung PL_TUC_CARD_WRITE_RECORD gemäß
[gemSpec_CardProxy]cardOperation für strukturierte Elementary Filesmit dem
AktionsparameterUPDATEumsetzen. **[\<=]**

**TIP1-A_6952 - Aufrufparameter zum Schreiben von Daten in eine strukturierte
Datei**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_CARD_WRITE_RECORD umsetzen, MÜSSEN vom Nutzenden denIDENTIFIKATORder zu
aktualisierenden Datei gemäß [gemSpec_CardProxy#Konfigurationstabelle
CardProxy], dieRECORDNUMBERsowie NEWDATA entgegennehmen und in der Umsetzung
voncardOperationverwenden. **[\<=]**

**TIP1-A_6953 - Ergebnis der Schreiboperation in einer strukturierten Datei**

Produkttypen und Dienste der TI die die Plattformleistung
PL_TUC_CARD_WRITE_RECORD umsetzen, MÜSSEN das Ergebnis gemäß
[gemSpec_CardProxy]cardOperationzurückmelden:

 ---> OL

**[\<=]**

### 2.1.3.17 PL_TUC_CARD_APPEND_RECORD – Anfügen von Daten an eine strukturierte Datei

Mit dem Systemprozess PL_TUC_CARD_APPEND_RECORD wird ein Datensatz als neuer
Record in einer strukturierten Datei an das Ende angefügt.

**TIP1-A_6954 - Leistung zum Anfügen von Daten in einer strukturierten Datei**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN das
Anfügen eines Records in einer strukturierten Datei auf einer SmartCard als
Plattformleistung PL_TUC_CARD_APPEND_RECORD gemäß
[gemSpec_CardProxy]cardOperation für strukturierte Elementary Filesmit dem
AktionsparameterAPPENDumsetzen. **[\<=]**

**TIP1-A_6955 - Aufrufparameter zum Anfügen von Daten in einer strukturierten
Datei**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_CARD_APPEND_RECORD umsetzen, MÜSSEN vom Nutzenden denIDENTIFIKATORder
zu aktualisierenden Datei gemäß [gemSpec_CardProxy#Konfigurationstabelle
CardProxy] sowieRECORDDATAentgegennehmen und in der Umsetzung
voncardOperationverwenden. **[\<=]**

**TIP1-A_6956 - Ergebnis der Anfügeoperation in einer strukturierten Datei**

Produkttypen und Dienste der TI, die die Plattformleistung
PL_TUC_CARD_APPEND_RECORD umsetzen, MÜSSEN das Ergebnis gemäß
[gemSpec_CardProxy]cardOperationzurückmelden:

 ---> OL

**[\<=]**

### 2.1.3.18 PL_TUC_EGK_APPEND_PROTOCOL – Zugriff auf der eGK protokollieren

Mit dem Systemprozess PL_TUC_EGK_APPEND_PROTOCOL wird ein höherwertiger
Baustein für das Schreiben eines Zugriffsprotokoll-Eintrags auf die eGK
definiert. Nutzern dieser Plattformleistung genügt es, beim Aufruf den
Identifikator der zu protokollierenden Fachanwendung mit der Art des durch die
Fachanwendung erfolgten Zugriffs mitzuteilen. Der Systemprozess erzeugt aus
diesen Daten zusammen mit den Angaben des Karteninhabers der
SM-B-AUT-Identität, der diese eGK in einem Card-2-Card-Verfahren mit einem
CV-Zertifikat freigeschaltet hat, einen Protokolldatensatz. Für das
Protokollieren auf der eGK nutzt der Systemprozess die Schreiboperation des
CardProxy der eGK.

**TIP1-A_6957 - Leistung zum Protokollieren des eGK-Zugriffs**

Produkttypen und Dienste, welche Systemprozesse der TI mit Zugriff auf die eGK
realisieren, MÜSSEN das Hinzufügen eines Protokolleintrags auf der eGK als
Plattformleistung PL_TUC_EGK_APPEND_PROTOCOL umsetzen. **[\<=]**

**TIP1-A_6958 - Aufrufparameter der Zugriffsprotokollierung**

Produkttypen und Dienste der TI, die die Plattformleistung
PL_TUC_EGK_APPEND_PROTOCOL umsetzen, MÜSSEN vom Nutzenden die
Protokollparameter

 ---> OL

entgegennehmen. **[\<=]**

**TIP1-A_6959 - Hinzufügen eines Protokolleintrags auf die eGK**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_EGK_APPEND_PROTOCOL umsetzen, MÜSSEN die Schritte zum Hinzufügen eines
Protokolleintrags auf der eGK in der angegebenen Reihenfolge durchführen:
**[\<=]**

### 2.1.3.19 PL_TUC_CARD_DELETE_RECORD – Löschen von Daten in einer strukturierten Datei

Mit dem Systemprozess PL_TUC_CARD_DELETE_RECORD wird ein einzelner Record einer
strukturierten Datei oder werden alle Records einer strukturierten Datei auf
einer SmartCard gelöscht. Beim Löschen eines einzelnen Records reduziert sich
die Anzahl der Records in der strukturierten Datei um eins. Werden alle Records
gelöscht, ist die Anzahl der Records nach erfolgreichem Abschluss der
Operation null. Die strukturierte Datei ist weiterhin adressierbar.

**TIP1-A_6960 - Leistung zum Löschen von Daten in einer strukturierten Datei**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN das
Löschen von Daten einer strukturierten Datei auf einer SmartCard als
Plattformleistung PL_TUC_CARD_DELETE_RECORD gemäß
[gemSpec_CardProxy]cardOperation für strukturierte Elementary Filesmit dem
AktionsparameterDELETERECORDumsetzen. **[\<=]**

**TIP1-A_6961 - Aufrufparameter zum Löschen von Daten in einer strukturierten
Datei**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_CARD_DELETE_RECORD umsetzen, MÜSSEN vom Nutzenden denIDENTIFIKATORder
betroffenen Datei gemäß [gemSpec_CardProxy#Konfigurationstabelle CardProxy]
entgegennehmen und in der Umsetzung voncardOperationverwenden. **[\<=]**

**TIP1-A_6962 - Optionale Parameter für das Löschen von Daten einer
strukturierten Datei**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_CARD_DELETE_RECORD umsetzen, MÜSSEN den vom Nutzenden optional
bereitgestellten ParameterRECORDNUMBERbei Vorhandensein entgegennehmen und
diese in der Umsetzung von [gemSpec_CardProxy]cardOperationverwenden, um die zu
löschende Datenmenge auf einen einzelnen Record zu beschränken. **[\<=]**

**TIP1-A_6963 - Ergebnis der Löschoperation in einer strukturierten Datei**

Produkttypen und Dienste der TI, die die Plattformleistung
PL_TUC_CARD_DELETE_RECORD umsetzen, MÜSSEN das Ergebnis gemäß
[gemSpec_CardProxy]cardOperationzurückmelden:

 ---> OL

**[\<=]**

### 2.1.3.20 PL_TUC_CARD_ERASE_RECORD – Rücksetzen eines Datensatzes in einer strukturierten Datei

Der Systemprozess PL_TUC_CARD_ERASE_RECORD löscht den Inhalt eines einzelnen
der strukturierten Datei auf einer SmartCard. Der Record sowie die gesamte
strukturierte Datei bleiben dabei erhalten. Der zurückgesetzte Record sowie
die strukturierte Datei sind weiterhin adressierbar.

**TIP1-A_6964 - Leistung zum Rücksetzen eines Datensatzes in einer
strukturierten Datei**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN das
Rücksetzen eines Records einer strukturierten Datei auf einer SmartCard als
Plattformleistung PL_TUC_CARD_ERASE_RECORD gemäß
[gemSpec_CardProxy]cardOperation für strukturierte Elementary Filesmit dem
AktionsparameterERASEumsetzen. **[\<=]**

**TIP1-A_6965 - Aufrufparameter zum Rücksetzen eines Datensatzes in einer
strukturierten Datei**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_CARD_ERASE_RECORD umsetzen, MÜSSEN vom Nutzenden denIDENTIFIKATORder zu
betroffenen strukturierten Datei gemäß
[gemSpec_CardProxy#Konfigurationstabelle CardProxy] sowie dieRECORDNUMBERdes
zurückzusetzenden Datensatzes entgegennehmen und in der Umsetzung
voncardOperationverwenden. **[\<=]**

**TIP1-A_6966 - Ergebnis des Rücksetzens eines Datensatzes in einer
strukturierten Datei**

Produkttypen und Dienste der TI die die Plattformleistung
PL_TUC_CARD_DELETE_RECORD umsetzen, MÜSSEN das Ergebnis gemäß
[gemSpec_CardProxy]cardOperationzurückmelden:

 ---> OL

**[\<=]**

### 2.1.4 Transparenter Zugriff auf eine SmartCard

Mit dem Zugriff auf eine SmartCard über einen transparenten Kanal ist es
möglich, von entfernter Stelle mit der Karte zu interagieren. Über den
CardProxy werden Kartenkommandos direkt an die Karte weitergeleitet und deren
Antwort-APDU zurückgegeben. Weder die kapselnden Systemprozesse noch CardProxy
werten den Inhalt der an die Karte gesendeten und von dort empfangenen APDUs
aus. Im speziellen Fall einer verschlüsselten Kommunikation (trusted channel)
zwischen der Karte und einem Server in Card-to-Server-Kommunikation ist dies
ohnehin nicht möglich.

### 2.1.4.1 PL_TUC_CARD_TC_OPEN

Der Systemprozess PL_TUC_CARD_TC_OPEN öffnet einen transparenten
Kommunikationskanal zu einer SmartCard. Mit der Nutzung dieses
Plattformbausteins findet kein direkter Zugriff auf die Karte statt, es
aktiviert in der Kartenzugriffsschicht eine exklusive Nutzung der Karte für
diesen transparenten Kanal. Während dieser geöffnet ist, sind ausschließlich
Aktionen mit den Systemprozessen PL_TUC_CARD_TC_SEND und _CLOSE möglich.

**TIP1-A_6967 - Leistung zum Öffnen eines transparenten Kanals**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN das
Öffnen eines transparenten Kanals zu einer SmartCard als Plattformleistung
PL_TUC_CARD_TC_OPEN gemäß [gemSpec_CardProxy]Funktion transparentChannelmit
dem AktionsparameterOPENumsetzen. **[\<=]**

**TIP1-A_6968 - Ergebnis des Öffnens eines transparenten Kanals**

Produkttypen und Dienste der TI, die eine Plattformleistung PL_TUC_CARD_TC_OPEN
umsetzen, MÜSSEN das Ergebnis gemäß [gemSpec_CardProxy]Funktion
transparentChannelzurückmelden:

 ---> OL

**[\<=]**

### 2.1.4.2 PL_TUC_CARD_TC_SEND

Mittels des Systemprozesses PL_TUC_CARD_TC_SEND wird ein Kartenkommando zu einer
Karte weitergeleitet, ohne den Inhalt auszuwerten. Gelangt das Kartenkommando
erfolgreich zur Karte wird immer das Response-Kommando der Karte zurückgegeben.

**TIP1-A_6969 - Leistung der transparenten Kommunikation zur Karte**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN das
Senden von transparenten Kartenkommandos an eine SmartCard als
Plattformleistung PL_TUC_CARD_TC_SEND gemäß [gemSpec_CardProxy]Funktion
transparentChannelmit dem AktionsparameterSENDAPDUumsetzen. **[\<=]**

**TIP1-A_6970 - Aufrufparameter zur transparenten Kommunikation zur Karte**

Produkttypen und Dienste der TI, die eine Plattformleistung PL_TUC_CARD_TC_SEND
umsetzen, MÜSSEN vom Nutzenden dieCOMMANDAPDU, welche an die Karte
weitergeleitet werden soll, entgegennehmen und in der Umsetzung derFunktion
transparentChannelverwenden. **[\<=]**

**TIP1-A_6971 - Ergebnis der transparenten Kommunikation zur Karte**

Produkttypen und Dienste der TI die eine Plattformleistung PL_TUC_CARD_TC_SEND
umsetzen, MÜSSEN das Ergebnis gemäß [gemSpec_CardProxy]Funktion
transparentChannelzurückmelden:

 ---> OL

**[\<=]**

### 2.1.4.3 PL_TUC_CARD_TC_CLOSE

Der Systemprozess PL_TUC_CARD_TC_CLOSE schließt einen transparenten
Kommunikationskanal zu einer SmartCard und gibt diese als Ressource für andere
Plattformleistungen wieder frei. Mit der Nutzung dieses Plattformbausteins
findet kein direkter Zugriff auf die Karte statt, es deaktiviert in der
Kartenzugriffsschicht die exklusive Nutzung der Karte für diesen transparenten
Kanal.

**TIP1-A_6972 - Leistung zum Schließen eines transparenten Kanals**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN das
Schließen eines transparenten Kanals zu einer SmartCard als Plattformleistung
PL_TUC_CARD_TC_CLOSE gemäß [gemSpec_CardProxy]Funktion transparentChannelmit
dem AktionsparameterCLOSEumsetzen. **[\<=]**

**TIP1-A_6973 - Ergebnis des Schließens eines transparenten Kanals**

Produkttypen und Dienste der TI die eine Plattformleistung PL_TUC_CARD_TC_CLOSE
umsetzen, MÜSSEN das Ergebnis gemäß [gemSpec_CardProxy]Funktion
transparentChannelzurückmelden:

 ---> OL

**[\<=]**

### 2.2 Kommunikation und Vernetzung

### 2.2.1 PL_TUC_TLS_SECURE_CHANNEL – TLS-Verbindung mit gegenseitiger Authentisierung

Der Systemprozess PL_TUC_TLS_SECURE_CHANNEL baut eine verschlüsselte Verbindung
von einem Clientsystem auf Basis einer in einem Sicherheitsmodul (z.B. HSM,
SmartCard) gespeicherten Identität der TI zu einem Zielsystem her. Dazu
erfolgt einegegenseitige Authentisierungzwischen dem Zielsystem und dem
verwendeten Sicherheitsmodul und es werden symmetrische Sitzungsschlüssel,
für die verschlüsselte Kommunikation zwischen Client- und Zielsystem,
ausgehandelt.

**TIP1-A_6974 - Leistung zur TLS-Verbindung mit gegenseitiger Authentisierung**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN eine
Plattformleistung PL_TUC_TLS_SECURE_CHANNEL für den Aufbau einer
TLS-Verbindung auf Basis einer in einem Sicherheitsmodul gespeicherten
Identität umsetzen. **[\<=]**

**TIP1-A_6975 - Aufrufparameter zur TLS-Verbindung mit gegenseitiger
Authentisierung**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_TLS_SECURE_CHANNEL umsetzen, MÜSSEN vom Nutzer denURIdes Zielsystems
und denROLLENBEZEICHNERder erwarteten Rolle des Zielsystems als Parameter
entgegennehmen und diese im Verbindungsaufbau verwenden. **[\<=]**

**TIP1-A_6976 - Aufbau der TLS-Verbindung mit gegenseitiger Authentisierung**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_TLS_SECURE_CHANNEL umsetzen, MÜSSEN die Schritte zum Aufbau einer
TLS-Verbindung auf Basis einer in einem Sicherheitsmodul gespeicherten
Identität in der angegebenen Reihenfolge durchführen: **[\<=]**

### 2.2.2 PL_TUC_NET_NAME_RESOLUTION

Mit dem Systemprozess PL_TUC_NET_NAME_RESOLUTION wird ein URI einer
Netzwerkkomponente der TI mittels des Namensdienstes der zentralen TI-Plattform
in eine IP-Adresse aufgelöst.

**TIP1-A_6977 - Auflösen von URI in IP-Adresse**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, SOLLEN eine
Auflösung von Netzwerk-URI in IP-Adresse als Plattformleistung
PL_TUC_NET_NAME_RESOLUTION über die Schnittstelle I_DNS_Name_Resolution zum
TI-Namensdienst gemäß [gemSpec_Net#Namensdienst] anbieten. **[\<=]**

### 2.2.3 PL_TUC_NET_SYNC_TIME

Über den Systemprozess PL_TUC_NET_SYNC_TIME können sich Dienste und
Komponenten der Telematikinfrastruktur mit dem Zeitserver der zentralen
TI-Plattform synchronisieren.

**TIP1-A_6978 - Synchronisierung mit Zeitdienst**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN eine
Zeitsynchronisation als Plattformleistung PL_TUC_NET_SYNC_TIME über die
Schnittstelle I_NTP_Time_Informationen zum Zeitdienst der
Telematikinfrastruktur gemäß [gemSpec_Net#Zeitdienst] umsetzen und diese
TI-Zeit als gültige, gesetzliche Zeit betrachten. **[\<=]**

### 2.3 Zugriffe auf den Verzeichnisdienst

Über die im Folgenden beschriebenen Systemprozesse können Zugriffe auf den
Verzeichnisdienst der zentralen TI-Plattform durchgeführt werden.

### 2.3.1 PL_TUC_VZD_BIND - Verbindung aufbauen

**A_17431 - Leistung zum Verbindungsaufbau zum VZD**

Produkttypen und Dienste der TI, welche Systemprozesse der TI realisieren,
MÜSSEN eine Plattformleistung PL_TUC_VZD_BIND für den Aufbau einer Verbindung
zum Verzeichnisdienst der zentralen TI-Plattform umsetzen. **[\<=]**

**A_17445 - Aufbau der Verbindung zum VZD**

Produkttypen und Dienste der TI, die eine Plattformleistung PL_TUC_VZD_BIND
umsetzen, MÜSSEN die Schritte zum Aufbau einer Verbindung zum
Verzeichnisdienst der zentralen TI-Plattform in der angegebenen Reihenfolge
durchführen: **[\<=]**

### 2.3.2 PL_TUC_VZD_SEARCH - Verzeichnis abfragen

**A_17432 - Leistung zur Abfrage des VZD**

Produkttypen und Dienste der TI, welche Systemprozesse der TI realisieren,
MÜSSEN eine Plattformleistung PL_TUC_VZD_SEARCH für die Abfrage des
Verzeichnisdienst der zentralen TI-Plattform gemäß [gemSpec_VZD#Schnittstelle
I_Directory_Query] umsetzen. **[\<=]**

**A_17448 - Aufrufparameter der Verzeichnisabfrage**

Produkttypen und Dienste der TI, die eine Plattformleistung PL_TUC_VZD_SEARCH
umsetzen, MÜSSEN vom Nutzer denSEARCH_REQUESTals Aufrufparameter
entgegennehmen und in der Umsetzung als LDAPv3 Search Request gemäß
[RFC-4511#4.5.1] über die SchnittstelleI_Directory_Queryan den
Verzeichnisdienst der zentralen TI-Plattform senden. **[\<=]**

**A_17449 - Ergebnis der Verzeichnisabfrage**

Produkttypen und Dienste der TI, die eine Plattformleistung PL_TUC_VZD_SEARCH
umsetzen, MÜSSEN die LDAPv3 Search Response gemäß [RFC-4511#4.5.2] vom
Verzeichnisdienst empfangen und alsSEARCH_RESPONSEan den Nutzer übergeben.
Fehler MÜSSEN ggf. gemäß [RFC-4511#Appendix A] alsERRORan den Nutzer
übergeben und behandelt werden. **[\<=]**

### 2.3.3 PL_TUC_VZD_UNBIND - Verbindung trennen

**A_17446 - Leistung zur Verbindungstrennung zum VZD**

Produkttypen und Dienste der TI, welche Systemprozesse der TI realisieren,
MÜSSEN eine Plattformleistung PL_TUC_VZD_UNBIND für die Trennung einer
Verbindung zum Verzeichnisdienst der zentralen TI-Plattform umsetzen. **[\<=]**

**A_17465 - Trennen der Verbindung zum VZD**

Produkttypen und Dienste der TI, die eine Plattformleistung PL_TUC_VZD_UNBIND
umsetzen, MÜSSEN in der Umsetzung einen LDAPv3 Unbind Request gemäß
[RFC-4511#4.3] an den Verzeichnisdienst der zentralen TI-Plattform
senden. Fehler MÜSSEN ggf. gemäß [RFC-4511# Appendix A] alsERRORan den
Nutzer übergeben und behandelt werden. **[\<=]**

### 2.3.4 PL_TUC_VZD_ABANDON - Verzeichnisabfrage abbrechen

**A_17447 - Leistung zum Abbrechen einer Verzeichnisabfrage**

Produkttypen und Dienste der TI, welche Systemprozesse der TI realisieren,
MÜSSEN eine Plattformleistung PL_TUC_VZD_ABANDON für den Abbruch einer
Abfrage des Verzeichnisdienstes der zentralen TI-Plattform umsetzen. **[\<=]**

**A_17468 - Abbrechen einer Verzeichnisabfrage**

Produkttypen und Dienste der TI, die eine Plattformleistung PL_TUC_VZD_ABANDON
umsetzen, MÜSSEN in der Umsetzung einen LDAPv3 Abandon Request gemäß
[RFC-4511#4.11] an den Verzeichnisdienst der zentralen TI-Plattform senden.
Fehler MÜSSEN ggf. gemäß [RFC-4511# Appendix A] alsERRORan den Nutzer
übergeben und behandelt werden. **[\<=]**

### 2.4 Vertraulichkeit, Authentizität, Integrität

### 2.4.1 PL_TUC_SIGN_HASH_nonQES – mit TI-Identität nonQES signieren

Der Systemprozess PL_TUC_SIGN_HASH_nonQES versieht einen übergebenen Hash-Wert
mit einer auf einer TI-Identität basierenden digitalen nonQES Signatur. Dazu
wird unter Verwendung eines Sicherheitsmoduls (SmartCard, HSM) oder
Signaturdienstes und einer auf dem Sicherheitsmodul bzw. dem Signaturdienst
gespeicherten Identitätder TI ein Binärwert signiert.

**TIP1-A_6979 - Leistung der nonQES-Signatur**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN das
Signieren eines Hashwertes mit einer TI-Identität als Plattformleistung
PL_TUC_SIGN_HASH_nonQES umsetzen. Bei Verwendung einer SmartCard MUSS dies
gemäß [gemSpec_CardProxy]cardOperation für private Schlüsselobjekte 
erfolgen. Bei Verwendung eines HSMs oder eines Signaturdienstes MUSS dies
gemäß [gemSpec_HSMProxy#logische Operationsignfür Signaturen] bzw.
[gemSpec_SigD#Operationsdefinition I_Remote_Sign_Operations::sign_Data]
erfolgen. **[\<=]**

**TIP1-A_6980 - Aufrufparameter der nonQES-Signatur**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_SIGN_HASH_nonQES umsetzen, MÜSSEN vom Nutzer denIDENTIFIKATORdes
privaten Schlüssels der TI-Identität, dasSIGNATURVERFAHREN
gemäß[gemSpec_Krypt#3.7 Signatur binärer Inhaltsdaten (Dokumente)/5.7.2
ECDSA-Signaturen im CMS-Format]  sowie den zu signierendenHASHWERTals
Aufrufparameter entgegennehmen und in der Umsetzung verwenden.Bei Nutzung einer
SmartCard MUSS derIDENTIFIKATORgemäß [gemSpecCardProxy#Konfigurationstabelle
CardProxy] verwendet werden,SIGNATURVERFAHRENundHASHWERTMÜSSEN als
Aktionsparameter bzw. Eingangsparameter voncardOperationgemäß
[gemSpec_CardProxy] verwendet werden.Bei Nutzung eines Signaturdienstes oder
eines HSM MÜSSENIDENTIFIKATORund derHASHWERTals Aufrufparameter Identifier
bzw. Data gemäß [gemSpec_SigD#Operationsdefinition
I_Remote_Sign_Operations::sign_Data] bzw. Identity und Data gemäß
[gemSpec_HSMProxy#logische Operationsignfür Signaturen] übergeben werden.
**[\<=]**

**TIP1-A_6981 - Ergebnis der nonQES-Signatur**

Produkttypen und Dienste der TI die eine Plattformleistung
PL_TUC_SIGN_HASH_nonQES umsetzen, MÜSSEN das Ergebnis und ggf. Fehler an die
nutzende Komponente zurückmelden:- bei Verwendung einer Karte gemäß
[gemSpec_CardProxy]cardOperation:

 ---> OL

- bei Verwendung eines Signaturdienstes gemäß
[gemSpec_SigD#Operationsdefinition I_Remote_Sign_Operations::sign_Data]:

 ---> OL

- bei Verwendung eines HSM gemäß [gemSpec_HSMProxy]:

 ---> UL

**[\<=]**

### 2.4.2 PL_TUC_HYBRID_ENCIPHER – Hybrid verschlüsseln

Der Systemprozess PL_TUC_HYBRID_ENCIPHER führt eine hybride Verschlüsselung
eines Dokuments für ein oder mehrere Empfängerzertifikate durch. Dazu muss
zunächst ein symmetrischer Schlüssel erzeugt werden, mit dem das
Eingabedokument verschlüsselt wird. Dieser symmetrische Schlüssel wird
anschließend mit dem öffentlichen Schlüsselmaterial der Dokumentenempfänger
(bereitgestellt über X.509v3-Zertifikate) verschlüsselt und an das Dokument
angefügt.

**TIP1-A_6982 - Leistung zum hybriden Verschlüsseln**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN eine
Plattformleistung PL_TUC_HYBRID_ENCIPHER zum hybriden Verschlüsseln eines
Dokuments umsetzen. **[\<=]**

**TIP1-A_6983-01 - Aufrufparameter zum hybriden Verschlüsseln**

Produkttypen und Dienste der TI, die die Plattformleistung
PL_TUC_HYBRID_ENCIPHER umsetzen, MÜSSEN vom Nutzer die Aufrufparameter

 ---> OL

entgegennehmen. **[\<=]**

**TIP1-A_6984-02 - Ablauf der hybriden Verschlüsselung eines Dokuments**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_HYBRID_ENCYPHER umsetzen, MÜSSEN die Schritte zum Verschlüsseln eines
gegebenen Dokuments in der angegebenen Reihenfolge durchführen: **[\<=]**

### 2.4.3 PL_TUC_HYBRID_DECIPHER – Hybrid entschlüsseln

Der Systemprozess PL_TUC_HYBRID_DECIPHER entschlüsselt ein hybrid
verschlüsseltes Dokument. Dazu wird zunächst der verschlüsselte
Dokumentenschlüssel aus dem Eingabedokument extrahiert und mit einem privaten
Schlüssel des Empfängers entschlüsselt. Die Speicherung und Nutzung des
privaten Schlüssels ist dabei bevorzugt unter Verwendung eines
Sicherheitsmoduls (SmartCard, HSM) durchzuführen. Mit dem wiederhergestellten
Dokumentenschlüssel wird anschließend das Dokument in einem symmetrischen
Verfahren entschlüsselt.

**TIP1-A_6985 - Leistung zum hybriden Entschlüsseln**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN eine
Plattformleistung PL_TUC_HYBRID_DECIPHER zum hybriden Entschlüsseln eines
Dokuments umsetzen. **[\<=]**

**TIP1-A_6986 - Aufrufparameter zum hybriden Entschlüsseln**

Produkttypen und Dienste der TI, die die Plattformleistung
PL_TUC_HYBRID_DECIPHER umsetzen, MÜSSEN vom Nutzer die Aufrufparameter

 ---> OL

entgegennehmen. **[\<=]**

**TIP1-A_6987 - Ablauf der hybriden Entschlüsselung eines Dokuments**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_HYBRID_DECYPHER umsetzen, MÜSSEN die Schritte zum Entschlüsseln eines
verschlüsselten Dokuments in der angegebenen Reihenfolge durchführen:
**[\<=]**

### 2.4.4 PL_TUC_SYMM_ENCIPHER – Symmetrisch verschlüsseln

Der Systemprozess PL_TUC_SYMM_ENCIPHER führt eine symmetrische Verschlüsselung
eines Dokuments durch. Dazu können zusammen mit dem Dokument ein Schlüssel
und associatedData (beide optional) übergeben werden. Falls kein Schlüssel
übergeben wird, wird ein symmetrischer Schlüssel erzeugt.

**A_14970 - Leistung zum symmetrischen Verschlüsseln**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN eine
Plattformleistung PL_TUC_SYMM_ENCIPHER zum symmetrischen Verschlüsseln eines
Dokuments umsetzen. **[\<=]**

**A_14971 - Aufrufparameter zum symmetrischen Verschlüsseln**

Produkttypen und Dienste der TI, die die Plattformleistung PL_TUC_SYMM_ENCIPHER
umsetzen, MÜSSEN vom Nutzer die Aufrufparameter

 ---> OL

entgegennehmen. **[\<=]**

**A_14972 - Ablauf des symmetrischen Verschlüsseln eines Dokuments**

Produkttypen und Dienste der TI, die eine Plattformleistung PL_TUC_SYMM_ENCYPHER
umsetzen, MÜSSEN die Schritte zum Verschlüsseln eines gegebenen Dokuments in
der angegebenen Reihenfolge durchführen: **[\<=]**

### 2.4.5 PL_TUC_SYMM_DECIPHER – Symmetrisch entschlüsseln

Der Systemprozess PL_TUC_SYMM_DECIPHER entschlüsselt ein symmetrisch
verschlüsseltes Dokument.

**A_14982 - Leistung zum symmetrischen Entschlüsseln**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN eine
Plattformleistung PL_TUC_SYMM_DECIPHER zum symmetrischen Entschlüsseln eines
Dokuments umsetzen. **[\<=]**

**A_14983 - Aufrufparameter zum symmetrischen Entschlüsseln**

Produkttypen und Dienste der TI, die die Plattformleistung PL_TUC_SYMM_DECIPHER
umsetzen, MÜSSEN vom Nutzer die Aufrufparameter

 ---> OL

entgegennehmen. **[\<=]**

**A_14984 - Ablauf des symmetrischen Entschlüsselns eines Dokuments**

Produkttypen und Dienste der TI, die eine Plattformleistung PL_TUC_SYMM_DECYPHER
umsetzen, MÜSSEN die Schritte zum Entschlüsseln eines verschlüsselten
Dokuments in der angegebenen Reihenfolge durchführen: **[\<=]**

### 2.4.6 PL_TUC_SIGN_DOCUMENT_nonQES – Dokument nonQES signieren

Der Systemprozess PL_TUC_SIGN_DOCUMENT_nonQES versieht ein übergebenes Dokument
mit einer auf einer TI-Identität basierenden digitalen nonQES Signatur. Dazu
wird unter Verwendung eines Sicherheitsmoduls (SmartCard, HSM) und einer darauf
gespeicherten Identität der TI ein Dokument signiert.

**A_17376 - Leistung der nonQES Dokumenten-Signatur**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN das
Signieren eines Dokuments mit einer TI-Identität als Plattformleistung
PL_TUC_SIGN_DOCUMENT_nonQES umsetzen. Bei Verwendung einer SmartCard MUSS dies
gemäß [gemSpec_CardProxy] cardOperation für private Schlüsselobjekte
erfolgen. Bei Verwendung eines HSMs MUSS dies gemäß
[gemSpec_HSMProxy#logische Operation sign für Signaturen] erfolgen. **[\<=]**

**A_17377 - Aufrufparameter der nonQES Dokumenten-Signatur**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_SIGN_DOCUMENT_nonQES umsetzen, MÜSSEN vom Nutzer denIDENTIFIKATORdes
privaten Schlüssels der TI-Identität, dasSIGNATURVERFAHRENgemäß
[gemSpec_Krypt#3.1.1 XML-Signaturen für nicht-qualifizierte Signaturen, 3.7
Signatur binärer Inhaltsdaten (Dokumente)] (RSA) bzw. [gemSpec_Krypt#5.7.1
ECDSA-Signaturen im XML-Format, 5.7.2 ECDSA-Signaturen im CMS-Format] (ECC)
sowie das zu signierendeDOKUMENTund denDOKUMENTENTYP(XML, CMS) als
Aufrufparameter entgegennehmen und in der Umsetzung verwenden. Das DOKUMENT
MUSS gemäß DOKUMENTENTYP für die Signatur vorbereitet werden, dabei ist der
zu signierende HASHWERT zu ermitteln.Bei Nutzung einer SmartCard MUSS
derIDENTIFIKATORgemäß [gemSpecCardProxy#Konfigurationstabelle CardProxy]
verwendet werden, das SIGNATURVERFAHREN sowie der HASHWERT MÜSSEN als
Aktionsparameter bzw. Eingangsparameter voncardOperationgemäß
[gemSpec_CardProxy] verwendet werden.Bei Nutzung eines HSMs MUSS die Verwendung
der genannten Aufrufparameter für Identity und Data gemäß
[gemSpec_HSMProxy#logische Operationsignfür Signaturen] erfolgen. **[\<=]**

**A_17380 - Ergebnis der nonQES Dokumenten-Signatur**

Produkttypen und Dienste der TI die eine Plattformleistung
PL_TUC_SIGN_DOCUMENT_nonQES umsetzen, MÜSSEN das Ergebnis und ggf. Fehler an
die nutzende Komponente zurückmelden:- bei Verwendung einer Karte gemäß
[gemSpec_CardProxy]cardOperation:

 ---> OL

- bei Verwendung eines HSM gemäß [gemSpec_HSMProxy]

 ---> UL

**[\<=]**

### 2.4.7 PL_TUC_VERIFY_DOCUMENT_nonQES - nonQES Dokumentensignatur verifizieren

Der Systemprozess PL_TUC_VERIFY_DOCUMENT_nonQES überprüft die nonQES Signatur
eines gegebenen Dokuments im Format XML oder CMS, unter Verwendung eines
zusammen mit dem Dokument gegebenen X.509-Zertifikates der PKI der
Telematikinfrastruktur.

**A_17559 - Leistung zur Prüfung der nonQES Dokumentensignatur**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN eine
nonQES Signaturprüfung eines Dokumentes im Format XML oder CMS als
Plattformleistung PL_TUC_PKI_VERIFY_DOCUMENT_nonQES umsetzen. **[\<=]**

**A_17561 - Aufrufparameter zur Prüfung der nonQES Dokumentensignatur**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_PKI_VERIFY_DOCUMENT_nonQES umsetzen, MÜSSEN vom Nutzer die folgenden
Parameter entgegennehmen und in der Umsetzung verwenden:

 ---> OL

**[\<=]**

**A_17562 - Ablauf der Prüfung der nonQES Dokumentensignatur**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_PKI_VERIFY_DOCUMENT_nonQES umsetzen, MÜSSEN die Schritte zur Prüfung
der Signatur eines Dokuments in der angegebenen Reihenfolge durchführen:
**[\<=]**

### 2.5 Leistungen der PKI

### 2.5.1 PL_TUC_PKI_VERIFY_CERTIFICATE – Prüfung eines Zertifikats der TI

Der Systemprozess PL_TUC_PKI_VERIFY_CERTIFICATE kapselt die Prüfung eines
X.509-Zertifikats der PKI der Telematikinfrastruktur. Es wird die zeitliche
Gültigkeit zu einem Referenzzeitpunktes sowie die mathematische Gültigkeit
geprüft. Zusätzlich kann via Parameter eine Online-Prüfung des Sperrstatus
des Zertifikats verlangt werden.

**TIP1-A_6991 - Leistung zur Prüfung eines Zertifikats in der TI**

Produkttypen und Dienste, welche Systemprozesse der TI realisieren, MÜSSEN eine
Zertifikatsprüfung als Plattformleistung PL_TUC_PKI_VERIFY_CERTIFICATE
umsetzen. **[\<=]**

**TIP1-A_6992-01 - Aufrufparameter der Zertifikatsprüfung in der TI**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_PKI_VERIFY_CERTIFICATE umsetzen, MÜSSEN vom Nutzer die folgenden
Parameter entgegennehmen und in der Zertifikatsprüfung verwenden:

 ---> OL

nur relevant, wenn EECertificateContainedInTSL=false:

 ---> OL

**[\<=]**

**A_18072 - Ablauf der Zertifikatsprüfung in der TI**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_PKI_VERIFY_CERTIFICATE umsetzen, MÜSSEN die Schritte zur Prüfung eines
Zertifikats in der angegebenen Reihenfolge durchführen: **[\<=]**

**TIP1-A_6993 - Ergebnis der Zertifikatsprüfung in der TI**

Produkttypen und Dienste der TI, die eine Plattformleistung
PL_TUC_PKI_VERIFY_CERTIFICATE umsetzen, MÜSSEN das Ergebnis jedes
Prüfkriteriums und Fehler in der Zertifikatsprüfung zurückmelden:Fehler in
der Verarbeitung beeinflussen die Prüfergebnisse wie folgt:

 ---> OL

Nur relevant bei EECertificateContainedInTSL = false:

 ---> OL

Nur relevant bei EECertificateContainedInTSL = true:

 ---> OL

**[\<=]**

### 3 Anhang A – Verzeichnisse

### 3.1 Abkürzungen

<table><tr><th>
Kürzel

</th><th>
Erläuterung

</th></tr><tr><td>
APDU

</td><td>
Application Protocol Data Unit

</td></tr><tr><td>
eGK

</td><td>
elektronische Gesundheitskarte

</td></tr><tr><td>
HBA

</td><td>
Heilberufsausweis

</td></tr><tr><td>
NTP

</td><td>
Network Time Protocol

</td></tr><tr><td>
OCSP

</td><td>
Online Certificate Status Protocol

</td></tr><tr><td>
PIN

</td><td>
Personal Identification Number

</td></tr><tr><td>
PKI

</td><td>
Public Key Infrastructure

</td></tr><tr><td>
PL

</td><td>
Plattformleistung

</td></tr><tr><td>
PUK

</td><td>
Personal Unblocking Key

</td></tr><tr><td>
QES

</td><td>
qualifizierte elektronische Signatur

</td></tr><tr><td>
SM-B

</td><td>
Security Module B, Sammelbegriff für SMC-B und HSM-B

</td></tr><tr><td>
TI

</td><td>
Telematikinfrastruktur

</td></tr><tr><td>
TUC

</td><td>
Technical Use Case

</td></tr></table>

### 3.2 Glossar

<table><tr><th>
Begriff

</th><th>
Erläuterung

</th></tr><tr><td>
Funktionsmerkmal

</td><td>
Der Begriff beschreibt eine Funktion oder auch einzelne, eine logische Einheit
bildende Teilfunktionen der TI im Rahmen der funktionalen Zerlegung des Systems.

</td></tr><tr><td>
Sicherheitsmodul  
(Engl. Security Module)

</td><td>
Physikalischer Träger kryptographischer Geheimnisse, insbesondere zu
Identitäten (z.B. zugehörige Schlüssel).

</td></tr></table>

Das Glossar wird als eigenständiges Dokument (vgl. [gemGlossar]) zur Verfügung
gestellt.

### 3.3 Abbildungsverzeichnis

- [Abbildung-1] - Systemprozesse der Basis-TI
- [Abbildung-2] - Umgebungsspezifische Operationen

### 3.4 Tabellenverzeichnis



### 3.5 Referenzierte Dokumente

### 3.5.1 Dokumente der gematik

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
gematik: Glossar der Telematikinfrastruktur

</td></tr><tr><td>
[gemSpec_CardProxy]

</td><td>
gematik: Übergreifende Spezifikation Card Proxy

</td></tr><tr><td>
[gemSpec_SigD]

</td><td>
gematik: Spezifikation Signaturdienst

</td></tr><tr><td>
[gemSpec_HSMProxy]

</td><td>
gematik: Übergreifende Spezifikation HSM-Proxy

</td></tr><tr><td>
[gemSpec_Karten_Fach_TIP]

</td><td>
gematik: Befüllvorschriften für die Plattformanteile der Karten der TI

</td></tr><tr><td>
[gemSpec_Krypt]

</td><td>
gematik: Übergreifende Spezifikation

Verwendung kryptographischer Algorithmen in der Telematikinfrastruktur

</td></tr><tr><td>
[gemSpec_Net]

</td><td>
gematik: Übergreifende Spezifikation Netzwerk

</td></tr><tr><td>
[gemSpec_OID]

</td><td>
gematik: Spezifikation Festlegung von OIDs

</td></tr><tr><td>
[gemSpec_PKI]

</td><td>
gematik: Spezifikation PKI

</td></tr><tr><td>
[gemSpec_VZD]

</td><td>
gematik: Spezifikation Verzeichnisdienst

</td></tr></table>

### 3.5.2 Weitere Dokumente

<table><tr><th>
[Quelle]

</th><th>
Herausgeber (Erscheinungsdatum): Titel

</th></tr><tr><td>
[CAdES]

</td><td>
ETSI: Electronic Signature Formats, Electronic Signatures and Infrastructures
(ESI) – Technical Specification, ETSI TS 101 733 V2.2.1, 2008-07, via
http://www.etsi.org

</td></tr><tr><td>
[RFC-4511]

</td><td>
Network Working Group (Juni 2006): Lightweight Directory Access Protocol
(LDAP): The Protocol,  https://tools.ietf.org/html/rfc4511 

</td></tr><tr><td>
[RFC-5083]

</td><td>
Network Working Group (November 2007): Cryptographic Message Syntax (CMS)
Authenticated-Enveloped-Data Content Type, 
https://tools.ietf.org/html/rfc5083 

</td></tr><tr><td>
[RFC-5084]

</td><td>
Network Working Group (November 2007): Using AES-CCM and AES-GCM Authenticated
Encryption in the Cryptographic Message Syntax (CMS), 
https://tools.ietf.org/html/rfc5084 

</td></tr><tr><td>
[RFC-5246]

</td><td>
Network Working Group (August 2008): The Transport Layer Security (TLS)
Protocol  
Version 1.2,  https://tools.ietf.org/html/rfc5246 

</td></tr><tr><td>
[RFC-5652]

</td><td>
Network Working Group (September 2009): Cryptographic Message Syntax (CMS), 
https://tools.ietf.org/html/rfc5652 

</td></tr><tr><td>
[RFC-6763]

</td><td>
Internet Engineering Task Force (Februar 2013): DNS-Based Service Discovery, 
https://tools.ietf.org/html/rfc6763 

</td></tr><tr><td>
[XAdES]

</td><td>
European Telecommunications Standards Institute (ETSI): Technical Specication
XML Advanced Electronic Signatures (XAdES). ETSI Technical Specication TS 101
903, Version 1.4.2, 2010

</td></tr><tr><td>
[XMLDSig]

</td><td>
W3C Recommendation (06.2008): XML-Signature Syntax and Processing
http://www.w3.org/TR/2008/REC-xmldsig-core-20080610/

</td></tr><tr><td>
[XMLEnc-1.1]

</td><td>
XML Encryption Syntax and Processing, W3C Recommendation  
11 April 2013,
http://www.w3.org/TR/xmlenc-core1/

</td></tr></table>





[Dokumentinformationen]: #dokumentinformationen
[Inhaltsverzeichnis]:    #inhaltsverzeichnis
[1]:                     #1-einordnung-des-dokuments
[1.1]:                   #11-zielsetzung
[1.2]:                   #12-zielgruppe
[1.3]:                   #13-geltungsbereich
[1.4]:                   #14-abgrenzungen
[1.5]:                   #15-methodik
[2]:                     #2-leistungen
[2.1]:                   #21-systemprozesse-für-den-zugriff-auf-smartcards-der-ti
[2.1.1]:                 #211-die-realisierungsumgebung-des-cardproxy
[2.1.1.1]:               #2111-env_tuc_card_secret_input-–-realisierung-eingabe-pin-geheimnis
[2.1.1.2]:               #2112-env_tuc_card_to_card-–-realisierung-card-2-card
[2.1.1.3]:               #2113-env_tuc_card_apdu_transport-–-realisierung-apdu-transport
[2.1.2]:                 #212-konfiguration-und-statusinformationen
[2.1.2.1]:               #2121-konfiguration-des-cardproxy
[2.1.2.2]:               #2122-initialisierung-cardproxy-für-egk
[2.1.2.3]:               #2123-initialisierung-cardproxy-für-sm-b
[2.1.2.4]:               #2124-pl_tuc_card_information-–-gesammelte-statusinformationen-zu-einer-karte
[2.1.2.5]:               #2125-pl_tuc_egk_status-–-gültigkeit-der-egk-prüfen
[2.1.2.6]:               #2126-pl_tuc_card_reset-–-rücksetzen-einer-karte
[2.1.3]:                 #213-zugriff-auf-smartcards-der-ti
[2.1.3.1]:               #2131-pl_tuc_card_change_pin-–-pin-ändern
[2.1.3.2]:               #2132-pl_tuc_card_enable_pin-–-pin-schutz-einschalten
[2.1.3.3]:               #2133-pl_tuc_card_disable_pin-–-pin-schutz-abschalten
[2.1.3.4]:               #2134-pl_tuc_card_unblock_pin-–-pin-mit-puk-entsperren
[2.1.3.5]:               #2135-pl_tuc_card_verify_pin-–-benutzer-verifizieren
[2.1.3.6]:               #2136-pl_tuc_card_activate_application-–-anwendung-aktivieren
[2.1.3.7]:               #2137-pl_tuc_card_deactivate_application-–-anwendung-deaktivieren
[2.1.3.8]:               #2138-pl_tuc_card_get_challenge-–-auslesen-einer-zufallszahl
[2.1.3.9]:               #2139-pl_tuc_card_read_file-–-lesen-von-daten-aus-einer-smartcard
[2.1.3.10]:              #21310-pl_tuc_card_write_file-–-schreiben-von-daten-auf-eine-smartcard
[2.1.3.11]:              #21311-pl_tuc_card_update_file-–-aktualisieren-von-daten-in-einer-transparenten-datei-einer-smartcard
[2.1.3.12]:              #21312-pl_tuc_card_delete_file-–-löschen-von-daten-auf-einer-smartcard
[2.1.3.13]:              #21313-pl_tuc_card_erase_file-–-rücksetzen-des-inhalts-einer-transparenten-datei
[2.1.3.14]:              #21314-pl_tuc_card_read_record-–-lesen-von-daten-aus-einer-strukturierten-datei
[2.1.3.15]:              #21315-pl_tuc_egk_read_protocol-–-auslesen-des-zugriffprotokolls-der-egk
[2.1.3.16]:              #21316-pl_tuc_card_write_record-–-schreiben-von-daten-in-eine-strukturierte-datei
[2.1.3.17]:              #21317-pl_tuc_card_append_record-–-anfügen-von-daten-an-eine-strukturierte-datei
[2.1.3.18]:              #21318-pl_tuc_egk_append_protocol-–-zugriff-auf-der-egk-protokollieren
[2.1.3.19]:              #21319-pl_tuc_card_delete_record-–-löschen-von-daten-in-einer-strukturierten-datei
[2.1.3.20]:              #21320-pl_tuc_card_erase_record-–-rücksetzen-eines-datensatzes-in-einer-strukturierten-datei
[2.1.4]:                 #214-transparenter-zugriff-auf-eine-smartcard
[2.1.4.1]:               #2141-pl_tuc_card_tc_open
[2.1.4.2]:               #2142-pl_tuc_card_tc_send
[2.1.4.3]:               #2143-pl_tuc_card_tc_close
[2.2]:                   #22-kommunikation-und-vernetzung
[2.2.1]:                 #221-pl_tuc_tls_secure_channel-–-tls-verbindung-mit-gegenseitiger-authentisierung
[2.2.2]:                 #222-pl_tuc_net_name_resolution
[2.2.3]:                 #223-pl_tuc_net_sync_time
[2.3]:                   #23-zugriffe-auf-den-verzeichnisdienst
[2.3.1]:                 #231-pl_tuc_vzd_bind---verbindung-aufbauen
[2.3.2]:                 #232-pl_tuc_vzd_search---verzeichnis-abfragen
[2.3.3]:                 #233-pl_tuc_vzd_unbind---verbindung-trennen
[2.3.4]:                 #234-pl_tuc_vzd_abandon---verzeichnisabfrage-abbrechen
[2.4]:                   #24-vertraulichkeit-authentizität-integrität
[2.4.1]:                 #241-pl_tuc_sign_hash_nonqes-–-mit-ti-identität-nonqes-signieren
[2.4.2]:                 #242-pl_tuc_hybrid_encipher-–-hybrid-verschlüsseln
[2.4.3]:                 #243-pl_tuc_hybrid_decipher-–-hybrid-entschlüsseln
[2.4.4]:                 #244-pl_tuc_symm_encipher-–-symmetrisch-verschlüsseln
[2.4.5]:                 #245-pl_tuc_symm_decipher-–-symmetrisch-entschlüsseln
[2.4.6]:                 #246-pl_tuc_sign_document_nonqes-–-dokument-nonqes-signieren
[2.4.7]:                 #247-pl_tuc_verify_document_nonqes---nonqes-dokumentensignatur-verifizieren
[2.5]:                   #25-leistungen-der-pki
[2.5.1]:                 #251-pl_tuc_pki_verify_certificate-–-prüfung-eines-zertifikats-der-ti
[3]:                     #3-anhang-a-–-verzeichnisse
[3.1]:                   #31-abkürzungen
[3.2]:                   #32-glossar
[3.3]:                   #33-abbildungsverzeichnis
[3.4]:                   #34-tabellenverzeichnis
[3.5]:                   #35-referenzierte-dokumente
[3.5.1]:                 #351-dokumente-der-gematik
[3.5.2]:                 #352-weitere-dokumente
[Abbildung-1]:           gemSpec_Systemprozesse_dezTI_V1.3.1.attachments/2148329178677835239.png
[Abbildung-2]:           gemSpec_Systemprozesse_dezTI_V1.3.1.attachments/7905817830305171484.png
[Tbl-001]:               #Tbl-001 (&93834775698216)
[Tbl-002]:               #Tbl-002 (&93834810809032)
[Tbl-003]:               #Tbl-003 (&93834775579440)
[Tbl-004]:               #Tbl-004 (&93834775622584)
[Tbl-005]:               #Tbl-005 (&93834775641720)
[Tbl-006]:               #Tbl-006 (&93834775724392)
