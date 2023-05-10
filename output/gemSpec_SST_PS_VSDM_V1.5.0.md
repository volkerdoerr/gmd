
Elektronische Gesundheitskarte und Telematikinfrastruktur

### Schnittstellenspezifikation Primärsysteme VSDM

- Klassifizierung: öffentlich
- Referenzierung: gemSpec_SST_PS_VSDM
- Revision: 591017
- Stand: 14.05.2018
- Status: freigegeben
- Version: 1.5.0

### Dokumentinformationen

Änderungen zur Vorversion

Anpassungen lt. Änderungsliste P15.2

Dokumentenhistorie

<table><tr><th>
Version

</th><th>
Datum

</th><th>
Kap./ Seite

</th><th>
Grund der Änderung, besondere Hinweise

</th><th>
Bearbeitung

</th></tr><tr><td>
0.1.0

</td><td>
Oktober 11

</td><td>
</td><td>
Ersterstellung

</td><td>
gematik

</td></tr><tr><td>
0.7.0

</td><td>
04.06.12

</td><td>
</td><td>
Stand zur Abstimmung

</td><td>
gematik

</td></tr><tr><td>
1.0.0

</td><td>
15.10.12

</td><td>
</td><td>
Einarbeitung Gesellschafterkommentare

</td><td>
gematik

</td></tr><tr><td>
1.1.0

</td><td>
12.11.12

</td><td>
</td><td>
Einarbeitung Kommentare aus der übergreifenden Konsistenzprüfung

</td><td>
gematik

</td></tr><tr><td>
1.2.0

</td><td>
15.08.13

</td><td>
</td><td>
Einarbeitung lt. Änderungsliste vom 08.08.13

</td><td>
gematik

</td></tr><tr><td>
1.3.0

</td><td>
21.02.14

</td><td>
</td><td>
Losübergreifende Synchronisation

</td><td>
gematik

</td></tr><tr><td>
1.4.0

</td><td>
12.08.16

</td><td>
</td><td>
Anpassungen zum Online-Produktivbetrieb (Stufe 1)

</td><td>
gematik

</td></tr><tr><td>
</td><td>
Einarbeitung lt. Änderungsliste P15.2

</td><td>
gematik

</td></tr><tr><td>
 1.5.0

</td><td>
14.05.18 

</td><td>
freigegeben

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
  - [1.4] Abgrenzung des Dokuments
  - [1.5] Methodik
- [2] Übergreifende Festlegungen
  - [2.1] Eingesetzte Standards
  - [2.2] Transportsicherung
  - [2.3] Nachrichtenerzeugung
  - [2.4] Nachrichtverarbeitung
  - [2.5] Umfang der Schnittstellen
- [3] Schnittstelle I_VSDService
  - [3.1] Übersicht
  - [3.2] Operation ReadVSD
    - [3.2.1] Eingangsbedingungen
    - [3.2.2] Request
    - [3.2.3] Response
    - [3.2.4] Zeichenkodierung
    - [3.2.5] Statusverarbeitung mittels Prüfungsnachweis
- [4] Schnittstelle I_KVKService
  - [4.1] Übersicht
  - [4.2] Operation ReadKVK
    - [4.2.1] Eingangsbedingungen
    - [4.2.2] Request
    - [4.2.3] Response
- [5] Fehlerbehandlung
  - [5.1] Übersicht
  - [5.2] Struktur
  - [5.3] Fehlercodes
- [6] Anhang A – Verzeichnisse
  - [6.1] Abkürzungen
  - [6.2] Glossar
  - [6.3] Abbildungsverzeichnis
  - [6.4] Tabellenverzeichnis
  - [6.5] Referenzierte Dokumente
    - [6.5.1] Dokumente der gematik
    - [6.5.2] Weitere Dokumente
- [7] Anhang B – Anforderungshaushalt
  - [7.1] Eingangsanforderungen
  - [7.2] Ausgangsanforderungen

### 1 Einordnung des Dokuments

### 1.1 Zielsetzung

Eindeutig spezifizierte Schnittstellen an den Außengrenzen der
Telematikinfrastruktur (TI) sind Grundlage für die Interoperabilität zwischen
der TI und angeschlossenen Systemen. Produkte verschiedener Hersteller und
Anbieter müssen die spezifizierten Schnittstellen nutzen, um die geforderte
Funktionalität und Interoperabilität zu gewährleisten.

Dieses Dokument spezifiziert die Schnittstellen des Fachmoduls VSDM, die von
Clientsystemen zum Lesen der Versichertenstammdaten genutzt werden. Die
Schnittstellen werden in diesem Dokument in der für die Entwicklung und Test
benötigten Tiefe spezifiziert. Das Dokument richtet neben anderen
Spezifikationen Blattanforderungen an das Fachmodul VSDM. Blattanforderungen
sind detaillierte Anforderungen, die direkt Grundlagen der Implementierung sind
(im Gegensatz zu allgemeineren Umsetzungsanforderungen). Die
Schnittstellenspezifikation ist aus der Fachmodulspezifikation herausgelöst,
da sie sich neben den Entwicklern von Fachmodulen auch an Entwickler von
Primärsystemen richtet.

Clientsysteme sind Primärsysteme der Leistungserbringer oder Anwendungen in den
Geschäftsstellen der Kostenträger. Primärsysteme der Leistungserbringer sind
Praxisverwaltungssysteme (PVS), Krankenhausinformationssysteme (KIS) und
Apothekenverwaltungssysteme (AVS). In diesem Dokument werden die Begriffe
Primärsystem und Clientsystem synonym verwendet.

Ziel des Dokumentes ist die Umsetzung der Anforderungen aus dem
systemspezifischem Konzept VSDM, die sich auf die Schnittstellen des Fachmoduls
VSDM für die Clientsysteme beziehen.

Grundlagen für die Ausführungen dieses Dokumentes sind

 ---> UL

Die Abbildung zeigt schematisch die Dokumentenhierarchie im Projekt VSDM, in
welcher die Schnittstellenspezifikation Primärsysteme und die Konzepte und
Spezifikationen eingeordnet sind. Die Abbildung stellt nicht die vollständige
Dokumentenhierarchie des Projekts Online-Produktivbetrieb (Stufe 1) oder den
Trace der Anforderungen dar.

### 1.2 Zielgruppe

Dieses Dokument richtet sich an:

 ---> UL

### 1.3 Geltungsbereich

Dieses Dokument enthält normative Festlegungen zur Telematikinfrastruktur des
deutschen Gesundheitswesens. Der Gültigkeitszeitraum der vorliegenden Version
und deren Anwendung in Zulassungsverfahren wird durch die gematik GmbH in
gesonderten Dokumenten (z. B. Dokumentenlandkarte, Produkttypsteckbrief,
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

### 1.4 Abgrenzung des Dokuments

Innerhalb dieses Dokuments wird auf die technische Umsetzung der Schnittstelle
des Fachmoduls VSDM für Clientsysteme eingegangen. Anforderungen an andere
Produkttypen sind nicht Bestandteil des Dokuments. Für die Beschreibung der
Anwendungsfälle und Abläufe der Fachanwendung VSDM wird auf das
systemspezifische Konzept VSDM [gemSysL_VSDM] verwiesen.

Dieses Dokument fokussiert auf das sichtbare Außenverhalten der Schnittstelle
selbst und damit auf die Eingangs- und Ausgangsparameter der entsprechenden
Operationen. Anforderungen zu den internen Abläufen im Fachmodul finden sich
in [gemSpec_FM_VSDM].

Ebenfalls in [gemSpec_FM_VSDM] enthalten und damit nicht Bestandteil dieses
Dokuments ist die Beschreibung der durch das Fachmodul für das Primärsystem
erzeugten Benachrichtigungen (Events).

Nicht beschrieben sind Konfigurationen, Abläufe und die Verarbeitung der Daten
im Primärsystem. Diese finden sich im Implementierungsleitfaden Primärsysteme
[gemILF_PS]. Insbesondere Entwickler von Primärsystemen sollten für die
Schnittstellenimplementierung dieses Dokument als Grundlage gelesen haben.

### 1.5 Methodik

Für die genauere Unterscheidung zwischen normativen und informativen Inhalten
werden die dem RFC 2119 [RFC2119] entsprechenden in Großbuchstaben
geschriebenen, deutschen Schlüsselworte (MUSS, DARF NICHT, SOLL, SOLL NICHT,
KANN) verwendet.

In Anhang B dieses Dokuments werden in der Tabelle 8 die Eingangsanforderungen
aufgelistet, die in diesem Ergebnisdokument berücksichtigt sind. In der Spalte
"umgesetzt durch" finden sich die eindeutigen Referenzen auf die dazu
erarbeiteten Blattanforderungen. In Anhang B2 stehen die Blattanforderungen mit
ihrem Text und dem entsprechenden Vorgänger.

Sofern im Dokument auf die Ausgangsanforderungen verwiesen wird, erfolgt dies in
eckigen Klammern, z. B. [VSDM-A_2093]. Wird auf Eingangsanforderungen
verwiesen, erfolgt dies in runden Klammern, z. B. (VSDM-A_303).

Die Ausgangsanforderungen und deren Zusammenhang zu den Anforderungen aus den
anderen Dokumenten bezüglich der Fachanwendung VSDM werden tabellarisch in
Anhang B dargestellt.

Die Darstellung der Schemadaten mittels Klassendiagramm erfolgt in UML.

Listing, Bezeichner, Variablen oder XML-Elemente werden in Courier dargestellt.

### 2 Übergreifende Festlegungen

### 2.1 Eingesetzte Standards

Als Schnittstellentechnologie wird SOAP verwendet. Um Interoperabilität
zwischen verschiedenen SOAP-Implementierungen [SOAP1.1] zu gewährleisten,
erfolgt die technische Umsetzung der Schnittstellen konform zum WS-I Basic
Profile in der Version 1.2 [BasicProfile1.2] [VSDM-A_2658].

Die Schnittstellen des Fachmoduls VSDM werden in Form von WSDL [WSDL1.1] und
XML-Schemas definiert. Gemäß dem WS-I Basic Profile muss für die Definition
die Web Services Description Language (WSDL) in der Version 1.1 verwendet
werden. Die aus der WSDL resultierende Nachricht muss dem Simple Object Access
Protocol (SOAP) in der Version 1.1 entsprechen und die Übertragung erfolgt
mittels des Hypertext Transfer Protocols (HTTP) in der Version 1.1.

Die WSDL-Dateien und XML-Schemadateien müssen mit dieser
Schnittstellenspezifikation zur Verfügung gestellt werden, um eine einfache
Implementierung zu gewährleisten und eine maschinelle Prüfung der
spezifizierten Elemente zu ermöglichen. Die in den WSDLs verwendete
Kodierungsmethode der SOAP-Nachrichten muss „wrapped document/literal“
sein, um Interoperabilität zu gewährleisten.

### 2.2 Transportsicherung

Es ist bei Leistungserbringern aufgrund gesetzlicher Vorschriften bzw.
sektorspezifischer Regelungen von einer sicheren Umgebung auszugehen. Demnach
ist eine unverschlüsselte Kommunikation zwischen Primärsystem und Fachmodul
des Konnektors ausreichend.

Die Notwendigkeit der Absicherung der Kommunikation zwischen Fachmodul VSDM und
Clientsystem hängt allerdings von dem Angriffsrisiko im konkreten
Einsatzumfeld ab. Die Verantwortung für die Beurteilung der Sicherheit der
Einsatzumgebung haben der Leistungserbringer bzw. die Verantwortlichen in den
Geschäftsstellen der Kostenträger. Ein Ergebnis dieser Bewertung kann sein,
dass die Kommunikation zwischen Clientsystem und Konnektor durch
Verschlüsselung zusätzlich abzusichern ist, um die Kommunikation ausreichend
vor Abhören zu schützen.

Das Fachmodul VSDM muss daher dem Clientsystem die Verschlüsselung der
Kommunikation anbieten, indem es die durch den Konnektor bereitgestellte
Funktionalität zur Transportsicherung an der Primärsystemschnittstelle nutzt.
[VSDM-A_2678]

Verschlüsselte Kommunikation mittels TLS ist weit verbreitete industrielle
Praxis und stellt keinen nennenswerten Implementierungsaufwand dar. Daher wird
zur allgemeinen Erhöhung des Schutzniveaus an der Schnittstelle des
Primärsystems zum Konnektor die standardmäßige Verschlüsselung der
Kommunikation mit serverseitiger Authentisierung empfohlen.

Zusätzlich kann vom Konnektor eine Client-Authentisierung erzwungen werden.
Dies ist entweder eine Basic Authentication mittels Benutzername und Passwort
oder eine Client Authentication mittels Software-Zertifikat. Bei der Basic
Authentication müssen Benutzername und Passwort in der
Schnittstellenkonfiguration des PS hinterlegt und mit der Konfiguration des
Konnektors abgestimmt sein. Im Fall der zertifikatsbasierten Client
Authentication wird im Konnektor ein Zertifikat generiert und exportiert.
Dieses ist anschließend für die Nutzung im Primärsystem zu importieren.
Weitere Festlegungen (z. B. Format der Zertifikatsdatei) finden sich in
[gemSpec_Kon] sowie Anwendungshinweise in [gemILF_PS].

### 2.3 Nachrichtenerzeugung

Der Sender muss gültige SOAP-Nachrichten konform der WSDL bzw. der XSDs der
aufgerufenen SOAP-Schnittstelle erzeugen. Es sind nur die in der Spezifikation
genannten Header-Elemente erlaubt. [VSDM-A_2703]

### 2.4 Nachrichtverarbeitung

Das Fachmodul VSDM validiert eingehende Nachrichten gegen das entsprechende
Schema (XSD). Nicht valide Nachrichten müssen mit einer Fehlermeldung
zurückgewiesen werden. Neben der Schemavalidierung muss das Fachmodul auch die
Inhalte aller zur Verarbeitung benötigten Elemente auf zulässige Werte
validieren. [VSDM-A_2675][VSDM-A_2689]

Das Fachmodul als Empfänger einer Nachricht muss nicht auf zusätzliche
Header-Elemente prüfen. Enthält eine Nachricht zusätzliche Header-Elemente
soll das Fachmodul diese ignorieren und die Verarbeitung fortsetzen.
[VSDM-A_2676]

### 2.5 Umfang der Schnittstellen

Die externen SchnittstellenI_VSDServiceundI_KVKServicezum Primärsystem müssen,
wie in der Systemlösung VSDM dargestellt, umgesetzt werden. [VSDM-A_2596]
[VSDM-A_2608]

Die Schnittstellen müssen dabei gleichartig die verschiedenen
Konfigurationsvarianten der Leistungserbringerumgebung unterstützen
(Online-Szenario und Standalone-Szenario), welche detailliert im
Implementierungsleitfaden Primärsysteme beschrieben sind.

Die BezeichnerI_VSDServiceundI_KVKServicesind die logischen Bezeichnungen der
Schnittstellen. Die konkreten OperationenReadVSDundReadKVKwerden in
entsprechenden WSDL-Dateien spezifiziert.

### 3 Schnittstelle I_VSDService

### 3.1 Übersicht

Das Fachmodul VSDM muss die SchnittstelleI_VSDServicemit der
OperationReadVSDrealisieren, die mehrfach parallel aufgerufen werden kann. Die
SOAP-Schnittstelle ist in [VSDService.wsdl] gemäß Abbildung
Abb_SST_PS_VSDM_03 spezifiziert, die Ein- und Ausgangsparameter der
SOAP-Anfrage sind in [VSDService.xsd] definiert. [VSDM-A_2633]

### 3.2 Operation ReadVSD

### 3.2.1 Eingangsbedingungen

Die Eingangsbedingungen für die Durchführung der OperationenReadVSDsind im
Anwendungsfall in Tab_VSDM_SysL_01 von [gemSysL_VSDM] beschrieben: Alle lokalen
Komponenten sind betriebsbereit, z. B. die zu lesende eGK sowie der HBA bzw.
die SMC sind gesteckt, funktionsfähig und durch vorangegangene Operationen
bereits eindeutig durch Karten-Handles identifiziert.

Die OperationReadVSDwird sowohl im Online-Szenario als auch im
Standalone-Szenario am Offline-Konnektor genutzt.

Online-Szenario

Im Online-Szenario ist der Konnektor sowohl über das lokale Netzwerk direkt mit
dem Primärsystem als auch mit der Telematikinfrastruktur (TI) verbunden. Beim
Aufruf der OperationReadVSDkann die Prüfung auf Aktualisierung durch das
Fachmodul online vorgenommen werden.

Standalone-Szenario

Im Standalone-Szenario ist das Primärsystem im lokalen Netzwerk mit dem
Offline-Konnektor verbunden. In diesem Fall ist die Prüfung und ggf.
Aktualisierung der eGK durch den Online-Konnektor inkl. Erstellen des
Prüfungsnachweises bereits erfolgt und der Aufruf der OperationReadVSDliest
den Prüfungsnachweis von der eGK.

Die zwei Szenarien Standalone und Online sind im systemspezifischen Konzept
[gemSysL_VSDM] sowie ausführlich im Implementierungsleitfaden Primärsysteme
erläutert [gemILF_PS].

### 3.2.2 Request

Die Tabelle Tab_SST_PS_VSDM_01 beschreibt die Eingangsparameter der
OperationReadVSD.

<table><tr><th>
Parameter

</th><th>
Beschreibung

</th></tr><tr><td>
EhcHandle

</td><td>
Karten-Handle der eGK: Merkmal zur Identifizierung der eGK, von der die Daten
gelesen werden sollen.

</td></tr><tr><td>
HpcHandle

</td><td>
Karten-Handle der SMC-B bzw. der HBA: Merkmal zur Identifizierung der SMC-B /
HBA, die zur Durchführung der Echtheitsprüfung (Card-to-Card-Authentisierung)
verwendet werden soll.

</td></tr><tr><td>
PerformOnlineCheck

</td><td>
Online-Prüfung durchführen: Gibt an, ob eine Onlineprüfung und ggf. ein
Update durchgeführt werden soll.  
(

true/false

).

</td></tr><tr><td>
ReadOnlineReceipt

</td><td>
Prüfungsnachweis lesen: Gibt an, ob der Prüfungsnachweis in der Antwort
enthalten sein soll.  
(

true/false

)

</td></tr><tr><td>
Context

</td><td>
Aufrufkontext der Operation, bestehend aus Mandanten-ID, Primärsystem-ID,
Arbeitsplatz-ID und User-ID. Dieser dient zur Prüfung, ob die angegebenen
Karten im gegebenen Kontext verwendet werden dürfen.

</td></tr></table>

Damit das Clientsystem steuern kann, ob eine Online-Prüfung durchgeführt
werden soll, besitzt die Operation den ParameterPerformOnlineCheck. Ist der
Parameter auftruegesetzt, führt das Fachmodul eine Aktualisierungsanfrage
durch. Ist der Parameter auffalsegesetzt, führt das Fachmodul nur aus
fachlichen Gründen gemäß Aktivitätsdiagramm des UC VSDM-UC_01 eine
Aktualisierungsanfrage durch, z. B. wenn die Gesundheitsanwendung der eGK
bereits gesperrt ist. Da im Standalone-Szenario keine Online-Verbindung genutzt
werden kann (Primärsystem am Offline-Konnektor), ist in diesem Fall der
ParameterPerformOnlineCheckmit dem Wertfalsezu verwenden, da die Aktualisierung
immer scheitern würde.

Das Clientsystem steuert mittels des ParametersReadOnlineReceipt, ob ein
Prüfungsnachweis zurückgegeben wird. Ist der
ParameterReadOnlineReceiptauftruegesetzt, wird ein Prüfungsnachweis
zurückgegeben, andernfalls enthält die Antwort keinen Prüfungsnachweis.
Falls Leistungserbringer grundsätzlich nicht zum Auslesen und Verwenden des
Prüfungsnachweises verpflichtet sind (z. B. Krankenhäuser), kann der
ParameterReadOnlineReceiptimmer auffalsegesetzt sein.

Im Online-Szenario ist die
ParametrierungPerformOnlineCheck=falseundReadOnlineReceipt=truegrundsätzlich
zulässig, aber im normalen Ablauf nicht sinnvoll, da versucht würde einen
bestehenden, verschlüsselten Prüfungsnachweis von der eGK zu lesen. Dieser
Prüfungsnachweis wäre aber bei einem vorherigen Besuch in einer anderen
Praxis erstellt worden und nicht nutzbar oder aus der eigenen Praxis und
veraltet.

Das Element Context enthält notwendige und optionale Angaben zum Aufrufkontext.

<table><tr><th>
Parameter

</th><th>
Beschreibung

</th></tr><tr><td>
MandantId

</td><td>
Eine alphanumerische ID des Mandanten, die in der Konnektorkonfiguration
festgelegt und im Clientsystem entsprechend hinterlegt sein muss.

Die ID ist immer anzugeben. In Mehrmandantenumgebungen muss sie entsprechend dem
Aufrufkontext gefüllt sein

</td></tr><tr><td>
ClientSystemId

</td><td>
Eine alphanumerische ID des Primärsystems, die in der Konnektorkonfiguration
festgelegt und im Primärsystem entsprechend hinterlegt sein muss.

</td></tr><tr><td>
WorkplaceId

</td><td>
Eine alphanumerische ID des Arbeitsplatzes, aus dessen Kontext der Aufruf
erfolgt. Diese muss in der Konnektorkonfiguration festgelegt und im
Primärsystem entsprechend hinterlegt sein. Sie ist im Rahmen der
VSDM-Schnittstelle (abweichend vom Schema) immer anzugeben.        

</td></tr><tr><td>
UserId

</td><td>
Die ID des Nutzers im Primärsystem, die auch im Konnektor hinterlegt ist. Sie
ist nur dann erforderlich, falls ein HBA verwendet wird.

</td></tr></table>

Weiterführende Beschreibungen zu Anwendung und Kombination der
Eingangsparameter in verschiedenen Szenarien sind im Implementierungsleitfaden
zu finden [gemILF_PS].

### 3.2.3 Response

Die Tabelle Tab_SST_PS_VSDM_02 beschreibt die Ausgangsparameter der
OperationReadVSD.

<table><tr><th>
Parameter

</th><th>
Beschreibung

</th></tr><tr><td>
VSD_Status

</td><td>
Inhalt Status-Container der eGK

(XML-Element

VSD_Status

)

</td></tr><tr><td>
PersoenlicheVersichertendaten (PD)

</td><td>
Inhalt des PD-Containers der eGK  
(XML-Element

UC_PersoenlicheVersicherungsdatenXML

)

</td></tr><tr><td>
AllgemeineVersicherungsdaten (VD)

</td><td>
Inhalt des VD-Containers der eGK

(XML-Element

UC_AllgemeineVersicherungsdatenXML

)

</td></tr><tr><td>
GeschuetzteVersichertendaten (GVD)

</td><td>
Inhalt des GVD-Containers der eGK

(XML-Element

UC_GeschützteVersicherungsdatenXML

)

</td></tr><tr><td>
Pruefungsnachweis

</td><td>
Von der eGK gelesene Prüfungsnachweis bzw. der innerhalb des Ablaufs erstellte
Prüfungsnachweis.

(XML-Element

Pruefungsnachweis

)

</td></tr></table>

Die SOAP-Antwort enthält immer den Statuscontainer, die ungeschützten VSD (PD,
VD) sowie - abhängig von der Parametrierung des Aufrufs und dem Verlauf der
Verarbeitung - die geschützten Versichertendaten (GVD) und den
Prüfungsnachweis.

Die XML-Struktur findet sich in der zugehörigen Schemadatei
[Versichertenstammdaten.xsd]. Die Beschreibung dazu findet sich im Anhang von
[gemSysL_VSDM]. Das Fachmodul VSDM des Konnektors führt keine Validierung der
XML-Dateien der eGK durch und gibt sie ohne Modifikation an die Schnittstelle
zurück.

Die geschützten Daten sind nur Bestandteil der SOAP-Response, wenn der
Leistungserbringer zum Zugriff berechtigt ist. Können die GVD aufgrund
fehlender Berechtigungen nicht gelesen werden, werden trotzdem die PD und VD
zurückgegeben [VSDM-A_2647].

Prüfungsnachweis

Sofern durch das Clientsystem angefordert, enthält die Antwort einen
Prüfungsnachweis. Dieser enthält neben der Fachdienstquittung sowohl im
Erfolgsfall (Aktualisierung erfolgt bzw. nicht notwendig) als auch im Falle von
Warnungen entsprechenden Statusinformationen. [VSDM-A_2631] [VSDM-A_2676].

Die XML-Struktur findet sich in der zugehörigen Schemadatei
[Pruefungsnachweis.xsd]. Die zulässigen Werte für das Element Ergebnis sind
in [gemSysL_VSDM#Tab_VSDM_SysL_35] definiert.

Container VSD_Status

Der Container VSD_Status ist ein XML-Element von TypVSD_StatusTypeund enthält
die Statusinformationen der Versichertenstammdaten der eGK.
(Aktualisierungsstatus, Version und Zeitstempel der letzten Aktualisierung der
Karte).

### 3.2.4 Zeichenkodierung

Festlegungen zur Zeichenkodierung der Datenstrukturen (ISO8859-15, UTF-8) und
Kompression finden sich in [gemSysL_VSDM], in [gemSpec_eGK_Fach_VSDM] sowie in
Beschreibungen im Implementierungsleitfaden Primärsysteme [gemILF_PS].

Die Operation ReadVSD liefert die Container PD, VD, GVD sowie den
Prüfungsnachweis gzip-komprimiert und Base64-kodiert [VSDM-A_2691].

### 3.2.5 Statusverarbeitung mittels Prüfungsnachweis

Bei Fehlern, die bei der Kommunikation zwischen Fachmodul und Fachdienst
auftreten, wird die Verarbeitung nicht abgebrochen, sondern das Fachmodul
versucht trotzdem die Versichertenstammdaten zu lesen und den Aufruf für das
Clientsystem zu beantworten. Dem Clientsystem sind damit Probleme bei der
Online-Kommunikation nicht direkt ersichtlich.

In Fällen, bei denen durch das Primärsystem ein Prüfungsnachweis angefordert
worden ist, kann anhand von Ergebnis und ErrorCode im Prüfungsnachweis eine
weitergehende Verarbeitung im Primärsystem erfolgen. Durch das Ergebnis im
Prüfungsnachweis (3-6) kann ein Problem bei der Kommunikation erkannt werden.
Aus Sicht des Primärsystems stellt dieser Fall eine Warnung dar. Die
Verarbeitung bezüglich VSD war trotzdem erfolgreich, sofern die VSD von der
eGK gelesen werden konnten [VSDM-A_2631].

Im speziellen Fall des Ergebnis=3 im Prüfungsnachweis sind Fehlercodes
Bestandteil des Prüfungsnachweises. Dies ist dann der Fall, wenn die
VSDM-Fachdienste mit einem SOAP-Fault geantwortet haben. Die entsprechenden
Fehlercodes finden sich in der Gesamtübersicht im Implementierungsleitfaden
Primärsystem [gemILF_PS].

<table><tr><th>
Kategorie

</th><th>
Beschreibung

</th><th>
Übermittlung des Status / Fehlers

</th></tr><tr><td>
OK

</td><td>
Kein Fehler, Verarbeitung vollständig

</td><td>
PN.Ergebnis (1-2)

(sofern PN erzeugt/gelesen)

</td></tr><tr><td>
Warnung  
(*)

</td><td>
Kartendaten gelesen und gültig, z.B. Probleme bei Online-Aktualisierung

</td><td>
PN.Ergebnis (3-6)  
PN.ErrorCode

(sofern PN erzeugt/gelesen)

</td></tr><tr><td>
Fehler

</td><td>
Fehler, Verarbeitung abgebrochen, anstelle von ReadVSDResponse wird ein
SOAP-Fault zurückgeliefert

</td><td>
SOAP-Fault  
(

siehe Fehlerbehandlung 5)

</td></tr></table>

(*) Für alle Anwendungsfälle, bei denen kein Prüfungsnachweis durch das
Primärsystem angefordert worden ist, ist immer von einer erfolgreichen und
fehlerfreien Verarbeitung auszugehen, wenn die Operation nicht mit einem
SOAP-Fault antwortet.

DerWert 4für das Ergebnis im Prüfungsnachweis ist nur im Standalone-Szenario
möglich. Nur in diesem Szenario wird dieser Wert im Zuge der automatischen
Online-Aktualisierung durch den Online-Konnektor auf die eGK geschrieben,
sofern im Ergebnis der Online-Prüfung das AUTH-Zertifikat der eGK ungültig
ist. Im Online-Szenario würde anstelle dessen die Operation abgebrochen und
ein SOAP-Fault geliefert werden.

DerWert 6für das Ergebnis im Prüfungsnachweis sollte eine spezielle
Verarbeitung im Primärsystem auslösen. Dieser Wert wird erzeugt, wenn die
Bedingung „Aktualisierung VSD auf eGK technisch nicht möglich und maximaler
Offline-Zeitraum überschritten“ eingetreten ist. Der Benutzer kann dadurch
in hervorgehobener Art und Weise über diesen länger anhaltenden Fehlerzustand
informiert werden.

### 4 Schnittstelle I_KVKService

### 4.1 Übersicht

Das Fachmodul VSDM muss die SchnittstelleI_KVKServicemit der
OperationReadKVKrealisieren. Die SOAP-Schnittstelle ist in [KVKService.wsdl]
gemäß Abbildung Abb_SST_PS_VSDM_07 spezifiziert, die Ein- und
Ausgangsparameter der SOAP-Anfrage sind in [KVKService.xsd] definiert.
[VSDM-A_2677]

### 4.2 Operation ReadKVK

### 4.2.1 Eingangsbedingungen

Die Eingangsbedingungen für die Durchführung der
SchnittstellenoperationenReadKVKsind in der Erläuterung des Anwendungsfalls in
Tabelle [gemSysL_VSDM#Tab_VSDM_SysL_07] normativ beschrieben: Alle lokalen
Komponenten sind betriebsbereit, z. B. die zu lesende KVK ist gesteckt und
funktionsfähig.

### 4.2.2 Request

Die Tabelle Tab_SST_PS_VSDM_09 beschreibt die Eingangsparameter der
OperationReadKVK.

<table><tr><th>
Parameter

</th><th>
Beschreibung

</th></tr><tr><td>
KVKHandle

</td><td>
Merkmal zur Identifizierung der KVK, von der die Daten gelesen werden sollen.

</td></tr><tr><td>
Context

</td><td>
Aufrufkontext der Operation, bestehend aus Mandanten-ID, Primärsystem-ID,
Arbeitsplatz-ID. Dieser dient zur Prüfung, ob die angegebene Karte im
gegebenen Kontext verwendet werden darf (siehe Abbildung 5: Abb_SST_PS_VSDM_12
– Schema des Aufrufkontextes).

</td></tr></table>

### 4.2.3 Response

Die Tabelle Tab_SST_PS_VSDM_14 beschreibt die Ausgangsparameter der
OperationReadVSD

<table><tr><th>
Parameter

</th><th>
Beschreibung

</th></tr><tr><td>
KVK

</td><td>
Die base64-kodierte ASN.1 Struktur der KVK [G04].

</td></tr></table>

Der Datensatz ist anhand der bestehenden Regeln geprüft und mit Hilfe der
Prüfsumme auf Integrität verifiziert (siehe [gemSpec_FM_VSDM] und [G04]).

Ist die Verifikation fehlgeschlagen, wird mit einem SOAP-Fault mit
entsprechendem Fehlercode geantwortet.

### 5 Fehlerbehandlung

### 5.1 Übersicht

Tritt ein Fehler in der Verarbeitung auf, der dazu führt, dass die aufgerufene
Operation abgebrochen wird, gibt das Fachmodul VSDM einen SOAP-Fault mit der
gematik Fehlerstruktur zurück. Tritt der Fehler nicht auf Nachrichtenebene,
sondern auf einer tieferen Ebene des OSI-Schichtenmodells auf (z. B. HTTP oder
TLS), erfolgt die Fehlerbehandlung auf der entsprechenden OSI-Schicht.

Bei Fehlern in der Kommunikation zwischen Fachmodul und Clientsystem, die
bereits durch das eingesetzte Webservice-Framework erkannt werden, soll mit
einem normalen SOAP-Fault reagiert werden. Zu diesen Fehlerzuständen zählen:
Verletzung des Schemas, Abweichungen von der technischen
Schnittstellenbeschreibung (WSDL), fehlerhaftes Encoding oder unerwartet große
Nachrichten. Das Fachmodul muss sicherstellen, dass der SOAP-Fault keine
sicherheitsrelevanten Informationen (z. B. Stacktraces) enthält. [VSDM-A_2682]

### 5.2 Struktur

Bei der anzuwendenden Fehlermeldung handelt es sich um eine standardkonforme
Erweiterung des SOAP-Faults gemäß [SOAP1.1] und [BasicProfile1.2], deren
Vorgaben zu SOAP-Faults normativ gelten. Die Struktur eines SOAP-Faults und die
Inhalte der Datenelemente sind in [gemSpec_OM#Kap3.2.3] beschrieben.

Die Struktur des Error-Elements entspricht dem Schema in [TelematikError.xsd].
Die Struktur des Error-Elements und die Inhalte der Datenelemente sind in der
[gemSpec_OM#Kap3.2.1] beschrieben. Auch wenn das Schema mehrere Trace-Elemente
zulässt, ist nur ein Trace-Element pro Fehlermeldung erlaubt.

Das Ereignis, dass einen Fehler verursacht, wird eindeutig
durchEventIDundLogReferencebeschrieben, wobei letztere durch eine InstanceID
verfeinert werden kann.

Die Werte für das Element Severity sind in [gemSpec_OM] beschrieben. Von der
Fachanwendung VSDM wird nur der WertFatalgenutzt.

### 5.3 Fehlercodes

In Tab_SST_PS_VSDM_10 sind die Fehlercodes aufgeführt, die vom Fachmodul VSDM
erzeugt werden und von der Schnittstelle als Bestandteil des
SOAP-Fault-Elements zurückgegeben werden. Allgemeine Fehlercodes des
Konnektors sind nicht in der Tabelle enthalten.

Das Fachmodul VSDM muss mit einer generischen Fehlermeldung gemäß [gemSpec_OM]
antworten, wenn die Gesundheitsanwendung DF.HCA auf der eGK gesperrt ist.

<table><tr><th>
Comp  
Type

</th><th>
Code

</th><th>
ErrorType

</th><th>
Severity

</th><th>
ErrorText

</th><th>
Befüllung Detail

</th><th>
Auslösende  
Bedingung

</th></tr><tr><td>
FM_  
VSDM

</td><td>
3001

</td><td>
Technical

</td><td>
Error

</td><td>
VSD nicht  
konsistent

</td><td>
Der Detailtext kann leer sein oder soll den Fehler in geeigneter Form näher
beschreiben.

</td><td>
Status-Flag des  
StatusVD Con-  
tainers ist ’1’.

</td></tr><tr><td>
FM_  
VSDM

</td><td>
3011

</td><td>
Technical

</td><td>
Error

</td><td>
Verarbeiten  
der Versicher-  
tendaten ge-  
scheitert

</td><td>
Der Detailtext soll den Fehler in geeigneter Form näher beschreiben, z.B. den
betroffenen Container (PD, VD, GVD) identifizieren.

</td><td>
Lesen der VSD  
(PD, VD oder  
GVD) von der  
eGK gescheitert.

</td></tr><tr><td>
FM_  
VSDM

</td><td>
3020

</td><td>
Technical

</td><td>
Error

</td><td>
Lesen KVK  
gescheitert

</td><td>
Der Detailtext soll den Fehler in geeigneter Form näher beschreiben.

</td><td>
KVK-Datensatz  
konnte nicht  
gelesen werden.

</td></tr><tr><td>
FM_  
VSDM

</td><td>
3021

</td><td>
Technical

</td><td>
Error

</td><td>
KVK-Prüfsumme  
falsch, Daten  
korrupt

</td><td>
Der Detailtext kann leer sein oder soll den Fehler in geeigneter Form näher
beschreiben.

</td><td>
Die Überprüfung  
der Prüfsumme  
des KVK-Satzes  
ergab einen Feh-  
ler.

</td></tr><tr><td>
FM_  
VSDM

</td><td>
3039

</td><td>
Technical

</td><td>
Error

</td><td>
Prüfungsnach-  
weis nicht ent-  
schlüsselbar

</td><td>
Der Detailtext soll den Fehler in geeigneter Form näher beschreiben, z.B. Der
Prüfungsnachweis kann nicht entschlüsselt werden.

</td><td>
Die Integritäts-  
prüfung bei der Entschlüsselung  
des Prüfungs- 

nachweises  
schlägt fehl.

</td></tr><tr><td>
FM_  
VSDM

</td><td>
3040

</td><td>
Technical

</td><td>
Error

</td><td>
Es ist kein Prü-  
fungsnachweis  
auf der eGK vor-  
handen

</td><td>
Der Detailtext soll den Fehler in geeigneter Form näher beschreiben, z.B. Kein
Prüfungsnachweis auf der eGK vorhanden.

</td><td>
Es ist kein Prü-  
fungsnachweis  
auf der eGK  
vorhanden.

</td></tr><tr><td>
FM_  
VSDM

</td><td>
3041

</td><td>
Technical

</td><td>
Error

</td><td>
SM-B nicht  
freigeschaltet

</td><td>
Der Detailtext muss das CardHandle der betroffenen SM-B enthalten.

</td><td>
SMC-B oder  
HSM-Sicher-  
heitszustand  
ist nicht aus-  
reichend, z. B. 

für C2C oder für TLS-Verbin-  
dungsaufbau  
zum Intermediär

</td></tr><tr><td>
FM_  
VSDM

</td><td>
3042

</td><td>
Technical

</td><td>
Error

</td><td>
HBA nicht  
freigeschaltet

</td><td>
Der Detailtext kann leer sein oder soll den Fehler in geeigneter Form näher
beschreiben.

</td><td>
HBA-Sicher-  
heitszustand ist  
nicht ausreichend,  
z. B. für C2C

</td></tr></table>

### 6 Anhang A – Verzeichnisse

### 6.1 Abkürzungen

<table><tr><th>
Abkürzung

</th><th>
Bedeutung

</th></tr><tr><td>
AVS

</td><td>
Apothekenverwaltungssystem

</td></tr><tr><td>
C2C

</td><td>
Card to Card

</td></tr><tr><td>
CCS

</td><td>
Card Communication Service

</td></tr><tr><td>
CMP

</td><td>
Komponentendiagramm

</td></tr><tr><td>
CMS

</td><td>
Card Management System

</td></tr><tr><td>
eGK

</td><td>
elektronische Gesundheitskarte

</td></tr><tr><td>
GVD

</td><td>
Geschützte Versichertendaten

</td></tr><tr><td>
HBA

</td><td>
Heilberufsausweis

</td></tr><tr><td>
HCA

</td><td>
Healthcare Application

</td></tr><tr><td>
ICCSN

</td><td>
Integrated Circuit Card Serial Number

</td></tr><tr><td>
ID

</td><td>
Identification

</td></tr><tr><td>
IP

</td><td>
Internet Protocol

</td></tr><tr><td>
ISO

</td><td>
International Organization for Standardization

</td></tr><tr><td>
KIS

</td><td>
Krankenhausinformationssystem

</td></tr><tr><td>
KVNR

</td><td>
Krankenversicherungsnummer

</td></tr><tr><td>
KVK

</td><td>
Krankenversichertenkarte

</td></tr><tr><td>
NTP

</td><td>
Network Time Protocol

</td></tr><tr><td>
OCSP

</td><td>
Online Certificate Status Protocol

</td></tr><tr><td>
PD

</td><td>
Persönliche Versichertendaten

</td></tr><tr><td>
PN

</td><td>
Prüfungsnachweis

</td></tr><tr><td>
PVS

</td><td>
Praxisverwaltungssystem

</td></tr><tr><td>
RFC

</td><td>
Request for Comments

</td></tr><tr><td>
SAB

</td><td>
Sicherer Ausführungsbereich

</td></tr><tr><td>
SD

</td><td>
Sequenzdiagramm

</td></tr><tr><td>
SMC (B/A/KTR)

</td><td>
Security Module Card

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
UC

</td><td>
Use Case, Use-Case-Diagramm

</td></tr><tr><td>
UML

</td><td>
Unified Modeling Language

</td></tr><tr><td>
VD

</td><td>
Allgemeine Versicherungsdaten

</td></tr><tr><td>
VSD

</td><td>
Versichertenstammdaten

</td></tr><tr><td>
VSDD

</td><td>
Versichertenstammdatendienst

</td></tr><tr><td>
VSDM

</td><td>
Versichertenstammdatenmanagement

</td></tr><tr><td>
XML

</td><td>
Extensible Markup Language

</td></tr></table>

### 6.2 Glossar

Das Glossar wird als eigenständiges Dokument, vgl. [gemGlossar] zur Verfügung
gestellt.

### 6.3 Abbildungsverzeichnis



### 6.4 Tabellenverzeichnis

- [Tabelle-1] - Tab_SST_PS_VSDM_01 - Eingangsparameter ReadVSD [VSDM-A_2693]
- [Tabelle-2] - Tab_SST_PS_VSDM_13: Eingangsparameter ReadVSD, Aufrufkontext [VSDM-A_2693]
- [Tabelle-3] - Tab_SST_PS_VSDM_02 - Ausgangsparameter ReadVSD [VSDM-A_2634]
- [Tabelle-4] - Tab_SST_PS_VSDM_03 - Kategorien von Status- und Fehlermeldungen
- [Tabelle-5] - Tab_SST_PS_VSDM_09 - Eingangsparameter der Operation ReadKVK [VSDM-A_2710]
- [Tabelle-6] - Tab_SST_PS_VSDM_14 - Ausgangsparameter der Operation ReadKVK [VSDM-A_2711]
- [Tabelle-7] - Tab_SST_PS_VSDM_10 - Fehlercodes des Fachmoduls VSDM [VSDM-A_2690] [VSDM-A_2692] [VSDM-A_2695] [VSDM-A_2696] [VSDM-A_2936] [VSDM-A_2937] [VSDM-A_2982] [VSDM-A_2983]
- [Tabelle-8] - Tab_SST_PS_VSDM_11 - Eingangsanforderungen mit Nachweis der Abdeckung

### 6.5 Referenzierte Dokumente

### 6.5.1 Dokumente der gematik

Die nachfolgende Tabelle enthält die Bezeichnungen der im vorliegenden Dokument
referenzierten Dokumente der gematik zur Telematikinfrastruktur. Der mit der
vorliegenden Version korrelierende Entwicklungsstand dieser Konzepte und
Spezifikationen wird pro Release in einer Dokumentenlandkarte definiert,
Version und Stand der referenzierten Dokumente sind daher in der nachfolgenden
Tabelle nicht aufgeführt. Deren zu diesem Dokument passende jeweils gültige
Versionsnummer entnehmen Sie bitte der aktuellsten, auf der Internetseite der
gematik veröffentlichten Dokumentenlandkarte, in der die vorliegende Version
aufgeführt wird.

<table><tr><th>
Quelle

</th><th>
Herausgeber (Erscheinungsdatum): Titel

</th></tr><tr><td>
[gemeGK_Fach]

</td><td>
gematik: Speicherstrukturen der eGK für Gesundheitsanwendungen

</td></tr><tr><td>
[gemGlossar]

</td><td>
gematik: Glossar der Telematikinfrastruktur

</td></tr><tr><td>
[gemKPT_Arch_TIP]

</td><td>
gematik: Konzept Architektur der TI-Plattform

</td></tr><tr><td>
[gemSpec_FM_VSDM]

</td><td>
gematik: Spezifikation Fachmodul VSDM

</td></tr><tr><td>
[gemSpec_OM]

</td><td>
gematik: Übergreifende Spezifikation Operations und Maintenance

</td></tr><tr><td>
[gemSysL_VSDM]

</td><td>
gematik: Systemspezifisches Konzept Versichertenstammdatenmanagement (VSDM)

</td></tr><tr><td>
[gemILF_PS]

</td><td>
gematik: Implementierungsleitfaden Primärsysteme

</td></tr><tr><td>
[gemSpec_Kon]

</td><td>
gematik: Konnektorspezifikation

</td></tr></table>

### 6.5.2 Weitere Dokumente

<table><tr><th>
Quelle

</th><th>
Herausgeber (Erscheinungsdatum): Titel

</th></tr><tr><td>
[BasicProfile1.2]

</td><td>
Basic Profile Version 1.2, 2006-11-09

http://ws-i.org/profiles/BasicProfile-1.2-2010-11-09.html

</td></tr><tr><td>
[G04]

</td><td>
Spitzenverbände der Krankenkassen, Kassenärztliche Bundesvereinigung und
Kassenzahnärztlichen Bundesvereinigung (gültig ab 01.November 2003): 

Technische Spezifikation der Arztausstattung – Lesegeräte, Version: 2.00

</td></tr><tr><td>
[RFC2119]

</td><td>
RFC 2119 (März 1997): Key words for use in RFCs to Indicate Requirement Levels
S. Bradner,

http://tools.ietf.org/html/rfc2109

</td></tr><tr><td>
[SOAP1.1]

</td><td>
Simple Object Access Protocol (SOAP) 1.1, W3C Note 08 May 2000

http://www.w3.org/TR/2000/NOTE-SOAP-20000508/

</td></tr><tr><td>
[WSDL1.1]

</td><td>
Web Services Description Language (WSDL) 1.1, W3C Note 15 March 2001

http://www.w3.org/TR/wsdl

</td></tr><tr><td>
[XML Datatypes]

</td><td>
XML Schema Part 2: Datatypes Second Edition W3C Recommendation 28 October 2004

http://www.w3.org/TR/2004/REC-xmlschema-2-20041028/

</td></tr></table>

### 7 Anhang B – Anforderungshaushalt

### 7.1 Eingangsanforderungen

<table><tr><th>
AFO-ID

</th><th>
Quelle

</th><th>
Beschreibung

</th><th>
Umgesetzt durch

</th></tr><tr><td>
CR-A_9

</td><td>
Ä_2; 1012705

</td><td>
Die nachrichtenbasierte Middleware der TI-Plattform MUSS Interoperabilität
durch einfache und, sofern verfügbar, standardbasierte Mechanismen
sicherstellen. Entscheidend für die Eignung eines Standards ist dabei
vorrangig die Reife und Akzeptanz in der Industrie und nachrangig der Status
des Standards.

</td><td>
VSDM-A_2658  
VSDM-A_2675  
VSDM-A_2676  
VSDM-A_2678  
VSDM-A_2689  
VSDM-A_2703

</td></tr><tr><td>
VSDM-A_2002

</td><td>
[gemSysL_VSDM]

</td><td>
Die Fachanwendung VSDM MUSS das Aktivitätsdiagramm "Aktivitätsdiagramm:
VSDM-UC_01 - VSD von eGK lesen" erfüllen.

</td><td>
VSDM-A_2596

</td></tr><tr><td>
VSDM-A_2017

</td><td>
[gemSysL_VSDM]

</td><td>
Die Fachanwendung VSDM MUSS den primären Anwendungsfall "VSDM-UC_01: VSD von
eGK lesen" abbilden.

</td><td>
VSDM-A_2596

</td></tr><tr><td>
VSDM-A_2018

</td><td>
[gemSysL_VSDM]

</td><td>
Die Fachanwendung VSDM MUSS den primären Anwendungsfall "VSDM-UC_03:
Versichertendaten von KVK lesen" abbilden.

</td><td>
VSDM-A_2608

</td></tr><tr><td>
VSDM-A_2055

</td><td>
[gemSysL_VSDM]

</td><td>
Die Fachanwendung VSDM MUSS im Anwendungsfall "VSDM-UC_01 VSD von eGK lesen" die
funktionalen Ergänzungen der Tabelle "Tab_VSDM_SysL_01 - VSD von eGK lesen"
erfüllen.

</td><td>
VSDM-A_2596

</td></tr><tr><td>
VSDM-A_2061

</td><td>
[gemSysL_VSDM]

</td><td>
Die Fachanwendung VSDM MUSS im Anwendungsfall "VSDM-UC_03 Versichertendaten von
KVK lesen" die funktionalen Ergänzungen der Tabelle "Tab_VSDM_SysL_07 –
Versichertendaten von KVK lesen" erfüllen.

</td><td>
VSDM-A_2608

</td></tr><tr><td>
VSDM-A_2094

</td><td>
[gemSysL_VSDM]

</td><td>
Das Fachmodul VSDM MUSS für das Primärsystem die Operation ReadVSD an der
I_VSDService Schnittstelle bereitstellen.

</td><td>
VSDM-A_2596

</td></tr><tr><td>
VSDM-A_2097

</td><td>
[gemSysL_VSDM]

</td><td>
Die Operation ReadVSD der Schnittstelle I_VSDService MUSS die Ein- und
Ausgangsparameter der Tabelle "Tab_VSDM_SysL_29 Parameter der Operation
ReadVSD" nutzen.

</td><td>
VSDM-A_2596  
VSDM-A_2634  
VSDM-A_2691  
VSDM-A_2693

</td></tr><tr><td>
VSDM-A_2099

</td><td>
[gemSysL_VSDM]

</td><td>
Die Operation ReadKVK der Schnittstelle I_KVKService MUSS die Ein- und
Ausgangsparameter der Tabelle "Tab_VSDM_SysL_30 Parameter der Operation
ReadKVK" nutzen.

</td><td>
VSDM-A_2608  
VSDM-A_2710  
VSDM-A_2711

</td></tr><tr><td>
VSDM-A_2120

</td><td>
[gemSysL_VSDM]

</td><td>
Die Fachanwendung VSDM MUSS für die Schnittstellen Fehlermeldungen mit einer
einheitlichen Fehlerstruktur für die nachnutzenden Systeme definieren.

</td><td>
VSDM-A_2682  
VSDM-A_2690  
VSDM-A_2692  
VSDM-A_2695  
VSDM-A_2696 

VSDM-A_2698  
VSDM-A_2699  
VSDM-A_2700  
VSDM-A_2701  
VSDM-A_2702

VSDM-A_2936

VSDM-A_2937

VSDM-A_2982

VSDM-A_2983

</td></tr><tr><td>
VSDM-A_2142

</td><td>
[gemSysL_VSDM]

</td><td>
Die Fachanwendung VSDM MUSS im Falle eines Abbruchs einer Aktivität bzw. eines
Anwendungsfalles eine Fehlermeldung für alle nachnutzenden Systeme erzeugen,
die Produkttyp, Betreiber und Fehlerursache eindeutig identifiziert und
Referenzen zu Details des Fehlers enthält.

</td><td>
VSDM-A_2631

</td></tr><tr><td>
VSDM-A_2154

</td><td>
[gemSysL_VSDM]

</td><td>
Die Fachanwendung VSDM MUSS das fachliche Infomodell zum Prüfungsnachweis aus
dem Lastenheft VSDM im technischen Infomodell umsetzen.

</td><td>
VSDM-A_2633  
VSDM-A_2677

</td></tr><tr><td>
VSDM-A_2156

</td><td>
[gemSysL_VSDM]

</td><td>
Die Fachanwendung VSDM MUSS das Teilmodell geschützte Versichertendaten aus dem
technischen Informationsmodell VSDM umsetzen.

</td><td>
VSDM-A_2633  
VSDM-A_2647  
VSDM-A_2677

</td></tr><tr><td>
VSDM-A_2158

</td><td>
[gemSysL_VSDM]

</td><td>
Die Fachanwendung VSDM MUSS das Teilmodell persönliche Versichertendaten aus
dem technischen Informationsmodell VSDM umsetzen.

</td><td>
VSDM-A_2633  
VSDM-A_2677

</td></tr><tr><td>
VSDM-A_2159

</td><td>
[gemSysL_VSDM]

</td><td>
Die Fachanwendung VSDM MUSS das Teilmodell allgemeine Versicherungsdaten aus dem
technischen Informationsmodell VSDM umsetzen.

</td><td>
VSDM-A_2633  
VSDM-A_2677

</td></tr><tr><td>
VSDM-A_2170

</td><td>
[gemSysL_VSDM]

</td><td>
Das Fachmodul VSDM MUSS für das Primärsystem die Operation ReadKVK an der
I_KVKService Schnittstelle bereitstellen.

</td><td>
VSDM-A_2608

</td></tr><tr><td>
VSDM-A_2709

</td><td>
[gemSysL_VSDM]

</td><td>
Das Fachmodul VSDM KANN die Kommunikation mit dem Clientsystem absichern, um
sicherzustellen, dass nur Anfragen aus Umgebungen von berechtigten Akteuren
stammen.

</td><td>
VSDM-A_2678

</td></tr></table>

### 7.2 Ausgangsanforderungen

**VSDM-A_2596 - ReadVSD: Umsetzung des Anwendungsfalls "VSDM-UC_01: VSD von eGK
lesen"**

Die Operation ReadVSD des Fachmoduls VSDM MUSS das Außenverhalten des
Anwendungsfalls "VSDM-UC_01: VSD von eGK lesen" abbilden. **[\<=]**

**VSDM-A_2608 - ReadKVK: Umsetzung des Anwendungsfalls "VSDM-UC_03:
Versichertendaten von KVK lesen"**

Die Operation ReadKVK des Fachmoduls VSDM MUSS das Außenverhalten des
Anwendungsfalls "VSDM-UC_03: Versichertendaten von KVK lesen" abbilden.
**[\<=]**

**VSDM-A_2631 - ReadVSD: ErrorCode im Prüfungsnachweis**

Die Operation ReadVSD des Fachmoduls VSDM MUSS den ErrorCode eines SOAP-Faults
des Fachdienstes in das Feld ErrorCode des Prüfungsnachweises übernehmen,
wenn das Fachmodul in der Verarbeitung von einem Fachdienst einen gematik
SOAP-Fault erhält. **[\<=]**

**VSDM-A_2633 - I_VSDService: Implementierung ReadVSD gemäß WSDL**

Die Schnittstelle I_VSDService des Fachmoduls VSDM MUSS die Operation ReadVSD
gemäß der Syntax der VSDService.wsdl implementieren. **[\<=]**

**VSDM-A_2634 - ReadVSD: Ausgangsparameter**

Die Operation ReadVSD des Fachmoduls VSDM MUSS in der Antwortnachricht die
Ausgangsparameter gemäß Tab_SST_PS_VSDM_02 enthalten.  **[\<=]**

**VSDM-A_2647 - ReadVSD: GVD in Antwort optional**

Die Operation ReadVSD des Fachmoduls VSDM MUSS in der Antwortnachricht das
Element GeschuetzteVersichertendaten enthalten, wenn der Leistungserbringer zum
Lesen berechtigt ist. **[\<=]**

**VSDM-A_2658 - Schnittstelle Primärsystem: BasicProfile 1.2**

Das Fachmodul VSDM MUSS die Primärsystemschnittstellen I_VSDService und
I_KVKService konform zu WS-I Basic-Profile 1.2 implementieren. **[\<=]**

**VSDM-A_2675 - Schnittstelle Primärsystem: invalide Anfragenachrichten
erkennen**

Das Fachmodul VSDM MUSS schema-invalide XML-Request-Root-Elemente in der
Anfragenachricht des Clientsystems erkennen und die Verarbeitung mit einer
Fehlermeldung abbrechen. **[\<=]**

**VSDM-A_2676 - Schnittstelle Primärsystem: zusätzliche Headerelemente**

Das Fachmodul VSDM SOLL an den Primärsystemschnittstellen beim Aufruf
zusätzliche Headerelemente ignorieren und die Verarbeitung fortsetzen.
**[\<=]**

**VSDM-A_2677 - I_KVKService: Implementierung ReadKVK gemäß WSDL**

Die Schnittstelle I_KVKService des Fachmoduls MUSS die Operation ReadKVK gemäß
der Syntax der KVKService.wsdl implementieren. **[\<=]**

**VSDM-A_2678 - Schnittstelle Primärsystem: Transportsicherung**

Das Fachmodul VSDM MUSS dem Clientsystem die Verschlüsselung der Kommunikation
anbieten, indem es die durch den Konnektor bereitgestellte Funktionalität zur
Transportsicherung an der Primärsystemschnittstelle nutzt. **[\<=]**

**VSDM-A_2682 - Fachmodul VSDM: Keine sicherheitsreleveanten Informationen im
Fehlermeldungen**

Das Fachmodul VSDM DARF sicherheitsrelevante Informationen (geheimes
Schlüsselmaterial, personenbezogene Daten) beim Abbruch der Verarbeitung in
der Fehlermeldung NICHT übermitteln (z.B. in Stacktraces). **[\<=]**

**VSDM-A_2689 - Schnittstelle Primärsystem: auf zulässige Werte prüfen**

Das Fachmodul VSDM MUSS alle zur Verarbeitung benötigten Elemente der
Anfragenachricht auf zulässige Werte validieren. **[\<=]**

**VSDM-A_2690 - Fachmodul VSDM: Fehlercode bei nicht konsistenten VSD**

Das Fachmodul VSDM MUSS mit einem gematik SOAP-Fault und dem Fehlercode 3001
gemäß den Festlegungen in Tab_SST_PS_VSDM_10 antworten, wenn der
Status-Container im Feld Status den Wert '1' enthält. **[\<=]**

**VSDM-A_2691 - ReadVSD: Format der Ausgangsparameter**

Die Schnittstelle I_VSDService des Fachmoduls VSDM MUSS die Elemente
PersoenlicheVersichertendaten, AllgemeineVersicherungsdaten,
GeschuetzteVersichertendaten und Pruefungsnachweis gzip-komprimiert und
anschließend Base64-kodiert liefern. **[\<=]**

**VSDM-A_2692 - Fachmodul VSDM: Lesen oder Dekomprimieren der VSD von der eGK
scheitert**

Das Fachmodul VSDM MUSS mit einem gematik SOAP-Fault und dem Fehlercode 3011
gemäß den Festlegungen in Tab_SST_PS_VSDM_10 antworten, wenn das Lesen der
VSD von der eGK scheitert. **[\<=]**

**VSDM-A_2693 - ReadVSD: Eingangsparameter**

Die Operation ReadVSD des Fachmoduls VSDM MUSS im Request die Eingangsparameter
gemäß Tab_SST_PS_VSDM_01 und Tab_SST_PS_VSDM_13 enthalten.  **[\<=]**

**VSDM-A_2695 - Fachmodul VSDM: Lesen der Daten von der KVK scheitert**

Das Fachmodul VSDM MUSS mit einem gematik SOAP-Fault und dem Fehlercode 3020
gemäß den Festlegungen in Tab_SST_PS_VSDM_10 antworten, wenn das Lesen des
KVK-Datensatzes scheitert. **[\<=]**

**VSDM-A_2696 - Fachmodul VSDM: Prüfsumme des KVK-Satzes falsch**

Das Fachmodul VSDM MUSS mit einem gematik SOAP-Fault und dem Fehlercode 3021
gemäß den Festlegungen in Tab_SST_PS_VSDM_10 antworten, wenn die
Überprüfung der Prüfsumme des KVK-Datensatzes einen Fehler ergibt. **[\<=]**

**VSDM-A_2703 - Schnittstelle Primärsystem: nur erlaubte Header in
Antwortnachricht**

Das Fachmodul VSDM MUSS Antwortnachrichten erstellen, die nur die in der
Spezifikation genannten Header-Elemente der aufgerufenen Schnittstelle
enthalten. **[\<=]**

**VSDM-A_2710 - ReadKVK: Eingangsparameter**

Die Operation ReadKVK des Fachmoduls VSDM MUSS im Request die Eingangsparameter
gemäß Tab_SST_PS_VSDM_09 enthalten.  **[\<=]**

**VSDM-A_2711 - ReadKVK: Ausgangsparameter**

Die Operation ReadKVK des Fachmoduls VSDM MUSS in der Antwortnachricht die
Ausgangsparameter gemäß Tab_SST_PS_VSDM_14 enthalten.  **[\<=]**

**VSDM-A_2936 - Fachmodul VSDM: Prüfungsnachweis nicht entschlüsselbar**

Das Fachmodul VSDM MUSS mit einem gematik SOAP-Fault und dem Fehlercode 3039
gemäß den Festlegungen in Tab_SST_PS_VSDM_10 antworten, wenn der
Prüfungsnachweis mit dem konfigurierten Schlüssel nicht entschlüsselbar ist.
**[\<=]**

**VSDM-A_2937 - Fachmodul VSDM: Es ist kein Prüfungsnachweis auf der eGK
vorhanden**

Das Fachmodul VSDM MUSS mit einem gematik SOAP-Fault und dem Fehlercode 3040
gemäß den Festlegungen in Tab_SST_PS_VSDM_10 antworten, wenn der
Prüfungsnachweis angefordert worden ist und dieser auf der eGK nicht vorhanden
ist. **[\<=]**

**VSDM-A_2982 - Fachmodul VSDM: Fehlermeldung: SM-B nicht freigeschaltet**

Das Fachmodul VSDM MUSS mit einem gematik SOAP-Fault und dem Fehlercode 3041
gemäß den Festlegungen in Tab_SST_PS_VSDM_10 antworten, wenn der SMC-B- oder
HSM-Sicherheitszustand für entsprechende Operationen nicht ausreichend ist.
**[\<=]**

**VSDM-A_2983 - Fachmodul VSDM: Fehlermeldung: HBA nicht freigeschaltet**

Das Fachmodul VSDM MUSS mit einem gematik SOAP-Fault und dem Fehlercode 3042
gemäß den Festlegungen in Tab_SST_PS_VSDM_10 antworten, wenn der
HBA-Sicherheitszustand für entsprechende Operationen nicht ausreichend ist (z.
B. C2C). **[\<=]**





[Dokumentinformationen]: #dokumentinformationen
[Inhaltsverzeichnis]:    #inhaltsverzeichnis
[1]:                     #1-einordnung-des-dokuments
[1.1]:                   #11-zielsetzung
[1.2]:                   #12-zielgruppe
[1.3]:                   #13-geltungsbereich
[1.4]:                   #14-abgrenzung-des-dokuments
[1.5]:                   #15-methodik
[2]:                     #2-übergreifende-festlegungen
[2.1]:                   #21-eingesetzte-standards
[2.2]:                   #22-transportsicherung
[2.3]:                   #23-nachrichtenerzeugung
[2.4]:                   #24-nachrichtverarbeitung
[2.5]:                   #25-umfang-der-schnittstellen
[3]:                     #3-schnittstelle-i_vsdservice
[3.1]:                   #31-übersicht
[3.2]:                   #32-operation-readvsd
[3.2.1]:                 #321-eingangsbedingungen
[3.2.2]:                 #322-request
[3.2.3]:                 #323-response
[3.2.4]:                 #324-zeichenkodierung
[3.2.5]:                 #325-statusverarbeitung-mittels-prüfungsnachweis
[4]:                     #4-schnittstelle-i_kvkservice
[4.1]:                   #41-übersicht
[4.2]:                   #42-operation-readkvk
[4.2.1]:                 #421-eingangsbedingungen
[4.2.2]:                 #422-request
[4.2.3]:                 #423-response
[5]:                     #5-fehlerbehandlung
[5.1]:                   #51-übersicht
[5.2]:                   #52-struktur
[5.3]:                   #53-fehlercodes
[6]:                     #6-anhang-a-–-verzeichnisse
[6.1]:                   #61-abkürzungen
[6.2]:                   #62-glossar
[6.3]:                   #63-abbildungsverzeichnis
[6.4]:                   #64-tabellenverzeichnis
[6.5]:                   #65-referenzierte-dokumente
[6.5.1]:                 #651-dokumente-der-gematik
[6.5.2]:                 #652-weitere-dokumente
[7]:                     #7-anhang-b-–-anforderungshaushalt
[7.1]:                   #71-eingangsanforderungen
[7.2]:                   #72-ausgangsanforderungen
[Tbl-001]:               #Tbl-001 (&93834801500120)
[Tabelle-1]:             #Tabelle-1 (&93834799837680)
[Tabelle-2]:             #Tabelle-2 (&93834777030816)
[Tabelle-3]:             #Tabelle-3 (&93834799915384)
[Tabelle-4]:             #Tabelle-4 (&93834771077904)
[Tabelle-5]:             #Tabelle-5 (&93834810821928)
[Tabelle-6]:             #Tabelle-6 (&93834810841792)
[Tabelle-7]:             #Tabelle-7 (&93834781674824)
[Tbl-009]:               #Tbl-009 (&93834775130816)
[Tbl-010]:               #Tbl-010 (&93834799247680)
[Tbl-011]:               #Tbl-011 (&93834768040888)
[Tabelle-8]:             #Tabelle-8 (&93834774923632)
[http://tools.ietf.org/html/rfc2109]: http://tools.ietf.org/html/rfc2109 (&93834768055512)
[http://www.w3.org/TR/2000/NOTE-SOAP-20000508/]: http://www.w3.org/TR/2000/NOTE-SOAP-20000508/ (&93834774911112)
[http://www.w3.org/TR/wsdl]: http://www.w3.org/TR/wsdl (&93834774915176)
[http://www.w3.org/TR/2004/REC-xmlschema-2-20041028/]: http://www.w3.org/TR/2004/REC-xmlschema-2-20041028/ (&93834774919264)
