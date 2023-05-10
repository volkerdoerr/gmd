
Elektronische Gesundheitskarte und Telematikinfrastruktur

### Schnittstellenspezifikation<br>Fachdienste (UFS/VSDD/CMS)

- Klassifizierung: öffentlich
- Referenzierung: gemSpec_SST_FD_VSDM
- Revision: 591080
- Stand: 12.08.2016
- Status: freigegeben
- Version: 1.6.0

### Dokumentinformationen

Änderung zur Vorversion

Überarbeitung der Dokumente für den Online-Produktivbetrieb (Stufe 1), als
Grundlage für Produktivzulassungen und den bundesweiten Rollout.

Die Änderungen zur letzten freigegebenen Version zum Online-Rollout (Stufe 1)
sind gelb markiert.

Dokumentenhistorie

<table><tr><th>
Version

</th><th>
Stand

</th><th>
Kap./  
Seite

</th><th>
Grund der Änderung, besondere Hinweise

</th><th>
Bearbeitung

</th></tr><tr><td>
0.9.0

</td><td>
29.03.12

</td><td>
zur Abstimmung freigegeben

</td><td>
gematik

</td></tr><tr><td>
0.9.5

</td><td>
17.07.12

</td><td>
zur Freigabe empfohlen PL

</td><td>
PL P72

</td></tr><tr><td>
1.0.0

</td><td>
25.07.12

</td><td>
freigegeben

</td><td>
gematik

</td></tr><tr><td>
1.1.0

</td><td>
15.10.12

</td><td>
Änderung der Kapitelstruktur Kap. 1 und 2

Aktualisierung des Anforderungshaushaltes

</td><td>
PL P72

</td></tr><tr><td>
1.2.0

</td><td>
12.11.12

</td><td>
Einarbeitung Kommentare aus der übergreifenden Konsistenzprüfung

</td><td>
P72

</td></tr><tr><td>
1.3.0

</td><td>
06.06.13

</td><td>
Einarbeitung Kommentare aus Workshop „sicheres CMS“, Kommentare LA

</td><td>
P72

</td></tr><tr><td>
1.4.0

</td><td>
21.02.14

</td><td>
Losübergreifende Synchronisation

</td><td>
PL P72

</td></tr><tr><td>
1.5.0

</td><td>
17.06.14

</td><td>
Neue Afo: VSDM-A_3009 Reaktion auf Abort-Element - CLOSE Element – gemäß
P11-Änderungsliste.

</td><td>
PL P72

</td></tr><tr><td>
1.5.9

</td><td>
18.12.15

</td><td>
Anpassungen zum Online-Produktivbetrieb (Stufe 1)

</td><td>
gematik

</td></tr><tr><td>
1.6.0

</td><td>
12.08.16

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
  - [1.5] Bestandsschutz
  - [1.6] Methodik
- [2] Allgemeine Festlegungen
  - [2.1] Bezeichnung der Request-Elemente
  - [2.2] Bezeichnung der Response-Elemente
  - [2.3] Header-Elemente
  - [2.4] Visualisierung der XML-Schemata
- [3] Update Flag Service
  - [3.1] Operation GetUpdateFlags
    - [3.1.1] Request
    - [3.1.2] Request-Header
    - [3.1.3] Response
  - [3.2] Fehlerbehandlung
- [4] Card Communication Service
  - [4.1] Operation PerformUpdates
    - [4.1.1] Request
    - [4.1.2] Request-Header
    - [4.1.3] Response
    - [4.1.4] Response-Header
  - [4.2] Operation GetNextCommandPackage
    - [4.2.1] Request
    - [4.2.2] Request-Header
    - [4.2.3] Response
  - [4.3] Fehlerbehandlung
- [5] Kommandosequenzen (informativ)
  - [5.1] Ablauf
  - [5.2] Kartenkommunikation
- [6] Anhang A - Verzeichnisse
  - [6.1] Abkürzungen
  - [6.2] Glossar
  - [6.3] Abbildungsverzeichnis
  - [6.4] Tabellenverzeichnis
  - [6.5] Referenzierte Dokumente
    - [6.5.1] Dokumente der gematik
    - [6.5.2] Weitere Dokumente
- [7] Anhang B - Anforderungshaushalt
  - [7.1] Eingangsanforderungen
  - [7.2] Ausgangsanforderungen

### 1 Einordnung des Dokuments

### 1.1 Zielsetzung

Das vorliegende Dokument spezifiziert die Schnittstelle zwischen den
Fachdiensten VSDM und dem Fachmodul VSDM auf Anwendungsebene. Die Fachdienste
VSDM sind in der jetzigen Version der Update Flag Service (UFS), das
Kartenmanagementsystem (CMS) und der Versichertenstammdatendienst (VSDD). Die
Dienste CMS und VSDD werden in Bezug auf ihre Schnittstelle als "Card
Communication Service" (CCS) zusammengefasst.

Die Systemlösung der Fachanwendung VSDM ist im systemspezifischen Konzept
[gemSysL_VSDM] beschrieben. Es setzt die fachlichen Anforderungen des
Lastenheftes auf Systemebene um, zerlegt die Fachanwendung VSDM in die
zugehörigen Produkttypen und definiert die Schnittstellen zwischen den
einzelnen Produkttypen. Für das Verständnis dieser Spezifikation wird die
Kenntnis von [gemSysL_VSDM] vorausgesetzt.

Die Anforderungen an die Transportschnittstelle auf Nachrichtenebene werden
separat in dem Dokument Schnittstellenspezifikation Transport VSDM
[gemSpec_SST_VSDM] behandelt.

Die Abbildung 1 zeigt schematisch die Dokumentenhierarchie im Projekt VSDM, in
welcher die Schnittstellenspezifikation Fachdienste innerhalb der Konzepte und
Spezifikationen der Design-Phase eingeordnet ist. Die Abbildung stellt nicht
die vollständige Dokumentenhierarchie des Projekts Online-Produktivbetrieb
(Stufe 1) oder den Trace der Anforderungen dar.

![Abbildung-1][Abbildung-1]

In der Schnittstellenspezifikation Fachdienste werden einleitend in Kapitel 1
die Zielsetzung des Dokumentes, die notwendigen Grundlagen und die gewählten
Methoden dargestellt.

Kapitel 2 enthält eine Zusammenfassung der allgemeinen Festlegungen zu den in
diesem Dokument spezifizierten Schnittstellen.

Die Spezifikation der Operation der UFS-Schnittstelle erfolgt in Kapitel 3 und
in Kapitel 4 erfolgt die Spezifikation für die Operationen der
CCS-Schnittstelle.

Zur Verdeutlichung der Kommunikation im Rahmen der Aktualisierung einer eGK wird
in Kapitel 5 der prinzipielle Ablauf einmal dargestellt und die
Kartenkommandos, die für eine Aktualisierung notwendig sind werden beschrieben.

Die Ausgangsanforderungen dieser Spezifikation und deren Zusammenhang zu den
Anforderungen aus dem übergeordneten Konzepten und Spezifikationen werden
tabellarisch in Anhang B dargestellt.

### 1.2 Zielgruppe

Das Dokument richtet sich an Hersteller und Anbieter der VSDM-Fachdienste und
Fachmodule sowie an Hersteller und Anbieter von Produkttypen, die hierzu eine
Schnittstelle besitzen.

### 1.3 Geltungsbereich

Dieses Dokument enthält normative Festlegungen zur Telematikinfrastruktur des
Deutschen Gesundheitswesens. Der Gültigkeitszeitraum der vorliegenden Version
und deren Anwendung im Zulassungsverfahren wird durch die gematik GmbH in
gesonderten Dokumenten (z.B. Dokumentenlandkarte, Produkttypsteckbrief,
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

### 1.4 Abgrenzung des Dokuments

Die Transportschnittstelle zwischen den Fachdiensten VSDM (UFS, VSDD, CMS) und
dem Fachmodul VSDM befindet sich nach dem OSI-Schichtenmodell in der
Anwendungsschicht. Die Transportschnittstelle selbst wird dabei in die zwei
Ebenen Nachrichtenebene und Anwendungsebene unterteilt. Zur Anwendungsebene,
die in diesem Dokument behandelt wird, zählen die fachdienstespezifischen
Daten (SOAP-Body).

Das Dokument [gemSpec_SST_VSDM] spezifiziert die Schnittstelle zwischen den
Fachdiensten VSDM und dem Fachmodul VSDM auf Nachrichtenebene und bezieht sich
auf die Header-Information in der SOAP-Nachricht.

Festlegungen zu tiefer liegenden Schichten im OSI-Modell und übergreifenden
Themen, wie Prüfung von Zertifikaten, zulässige Algorithmen und Details der
sicheren Kommunikation, werden durch Spezifikationen der Basis-TI getroffen.

Festlegungen zur Ausführung von Anwendungsfällen und Vorgaben zum Betrieb der
Fachdienste sind nicht Bestandteil dieser Spezifikation.

### 1.5 Bestandsschutz

Für die Schnittstellen der Fachdienste der Kostenträger besteht
Bestandsschutz. Nur in begründeten Fällen darf in Abstimmung mit den
Kostenträgern davon abgewichen werden. Daher werden die Festlegungen
bezüglich der Fehlerstruktur und Transport der fachlichen Inhalte aus dem
Releasestand 4.0.0 in die Dokumente der Pflichtenheftphase übernommen.

Das Transportprotokoll Telematik Transport Details (TTD) ist gemäß
Entscheidung der Basis-TI kein übergreifendes Protokoll, das von allen
Fachanwendungen der TI zwingend zu verwenden ist. Zukünftig verantworten die
Fachanwendungen das Kommunikationsprotokoll selbst. Um die Komplexität zu
reduzieren, wird in Abstimmung mit den Kostenträgern in der Fachanwendung VSDM
auf die TTD als Transportprotokoll verzichtet.

Stattdessen werden für die Fachdienste VSDM nur die Elemente zur Lokalisierung
und Sessioninformation übernommen sowie die Standard SOAP-Struktur verwendet.

### 1.6 Methodik

Anforderungen als Ausdruck normativer Festlegungen werden durch eine eindeutige
ID in eckigen Klammern sowie die dem RFC 2119 [RFC2119] entsprechenden, in
Großbuchstaben geschriebenen deutschen Schlüsselworte MUSS, DARF NICHT, SOLL,
SOLL NICHT, KANN gekennzeichnet.

Sofern im Text des systemspezifischen Konzepts auf die Ausgangsanforderungen
verwiesen wird, erfolgt dies in eckigen Klammern, z.B. [VSDM-A_2093]. Dies
tritt häufig bei Modellen und Tabellen auf, da viele Umsetzungsanforderungen
genau auf eine dieser methodischen Beschreibungen verweisen. Wird auf
Eingangsanforderungen verwiesen, erfolgt dies in runden Klammern, z.B.
(VSDM-A_303).

In Anhang B1 dieses Dokuments werden die Lastenheftanforderungen aufgelistet,
die in diesem Ergebnisdokument berücksichtigt sind. In der Spalte "umgesetzt
durch" befinden sich die eindeutigen Referenzen auf die dazu erarbeiteten
Umsetzungsanforderungen. In Anhang B2 stehen die Umsetzungsanforderungen mit
ihrer Beschreibung und dem entsprechenden Vorgänger.

Die zu einer Eingangsanforderung referenzierte Umsetzungsanforderung spiegelt
die erste Ebene des Anforderungsbaumes wieder. Die Verfeinerung dieser
Anforderungen zu einem vollständigen Anforderungsbaum erfolgt in einem
Anforderungsmanagement-Tool und nicht im vorliegenden Dokument.

### 2 Allgemeine Festlegungen

Das vorliegende Dokument spezifiziert die Schnittstelle zwischen den
Fachdiensten VSDM und dem Fachmodul VSDM. Zu den Fachdiensten VSDM zählen der
Update Flag Service (UFS), das Kartenmanagementsystem (CMS) und der
Versichertenstammdatendienst (VSDD). Die Fachdienste CMS und VSDD werden in
Bezug auf ihre Schnittstelle als "Card Communication Service" (CCS)
zusammengefasst.

Die Spezifikation der Schnittstelle des "Update Flag Service" und des "Card
Communication Service" umfasst die Definition mehrerer Operationen. Ein Dienst,
der eine dieser Schnittstellen anbietet, muss diese spezifizierten Operationen
vollständig implementieren.

In Kapitel 3 und Kapitel 4 sind die Operationen der Schnittstellen detailliert
beschrieben. Zu jeder Operation gibt es ein Request- und ein Response-Element.
Die Request- und Response-Nachrichten, der von den Diensten implementierten
Operationen, müssen zu den definierten Schemas konform sein.

Zusätzlich zu den hier getroffenen Festlegungen gelten für die hier
beschriebenen Schnittstellen alle übergreifenden Festlegungen aus der
Spezifikation [gemSpec_SST_VSDM].

### 2.1 Bezeichnung der Request-Elemente

Der Name eines Request-Elementes kann eindeutig einer Operation zugeordnet
werden, die bei dem Dienst ausgeführt werden soll.

### 2.2 Bezeichnung der Response-Elemente

Ein Response-Element besteht aus dem Namen des zugehörigen Request-Elementes
und dem SuffixResponse.

### 2.3 Header-Elemente

In dieser Spezifikation werden keine eigenen Header-Elemente definiert. Es
werden die Header-Elemente entsprechend der Spezifikation [gemSpec_SST_VSDM]
verwendet. Für jeden Request, als auch für die Response, sind
operationsspezifisch Header-Elemente festgelegt.

### 2.4 Visualisierung der XML-Schemata

Zur besseren Verständlichkeit werden in den folgenden Kapiteln XML-Schemas oder
Teile hieraus grafisch dargestellt. Die Visualisierungen wurden aus den
zugrunde liegenden Schemas generiert. Maßgeblich für die exakte Definition
eines Elementes ist nicht die Visualisierung, sondern jeweils das zugrunde
liegende Schema [UFS.wsdl] [CCS.wsdl].

### 3 Update Flag Service

Der Update Flag Service (UFS) bündelt den ggf. vorliegenden
Aktualisierungsbedarf mehrerer Dienste (CMS und VSDD) und gibt über die
UFS-Schnittstelle Auskunft zum Aktualisierungsbedarf. Damit entfällt der
Aufwand, bei jedem Kontakt der eGK mit der Telematikinfrastruktur jeden
Fachdienst, der potentiell auf die eGK zugreifen möchte, explizit nach einer
Aktualisierung zu fragen. Der UFS optimiert somit diesen Ablauf.

![Abbildung-2][Abbildung-2]

Wenn ein Fachdienst eine Aktualisierung der eGK beabsichtigt, setzt dieser
Fachdienst ein entsprechendes Update Flag im UFS. Sobald die eGK anschließend,
z. B. im Rahmen eines Arztbesuches mit dem UFS in Kontakt tritt, zeigt dieser
den Aktualisierungsbedarf an und es wird ggf. die Aktualisierung initiiert.

Wenn eine Optimierung von Aktualisierungen möglich ist, indem
mehrereAktualisierungenzusammen in einem Vorgang durchgeführt werden, nimmt
der Fachdienst diese Optimierung vor, indem er die Änderungen zu einem
Aktualisierungsvorgang zusammenführt. Fallen zum Beispiel mehrere Änderungen
der VSD an, sollen die Änderungen in einer Aktualisierung mit dem ServiceType
VSD zusammenfasst werden. [VSDM-A_2751]

Die Schnittstelle zum Hinzufügen und Entfernen eines Update Flags am UFS durch
einen Fachdienst ist nicht Teil der Fachanwendung VSDM. Die Schnittstelle liegt
in der Verantwortung der Fachdienstbetreiber und kann von diesen
eigenverantwortlich implementiert werden.

In der Tabelle 1 sind die allgemeinen Werte der Schnittstelle aufgeführt. Diese
Werte werden unter anderem für die Kodierung der Endpunkt-Adresse der
Schnittstelle verwendet.

<table><tr><th>
Element

</th><th>
Wert

</th></tr><tr><td>
Provider-Kennung

</td><td>
Kostenträgerkennung

</td></tr><tr><td>
ServiceType

</td><td>
UFS

</td></tr><tr><td>
Schnittstellen-Version

</td><td>
2.0

</td></tr></table>

### 3.1 Operation GetUpdateFlags

Mit der Operation GetUpdateFlags können Update Flags zu einer bestimmten ICCSN
ausgelesen werden. Ein vorhandenes Update Flag muss eindeutig über das Tupel
ICCSN, Service-Localization und Update-Identifier identifiziert werden können.
[VSDM-A_2280] [VSDM-A_2281]

Die Antwortnachricht der Operation enthält die Prüfziffer, wenn kein
Aktualisierungsauftrag für den VSDD vorliegt, damit das Fachmodul den
Prüfungsnachweis erstellen kann. Der Prüfungsnachweis dient als Nachweis
einer durchgeführten Aktualisierungsanfrage der VSD. Das bedeutet, dass der
UFS auch eine Prüfziffer sendet, wenn nur Aktualisierungsaufträge für das
CMS vorliegen, z.B. zum Aktivieren der Gesundheitsanwendung. [VSDM-A_2287]

### 3.1.1 Request

![Abbildung-3][Abbildung-3]

<table><tr><td>
Bezeichnung

</td><td>
GetUpdateFlags

</td></tr><tr><td>
Beschreibung

</td><td>
Operations-Element des Request der Operation GetUpdateFlags.

</td></tr><tr><td>
Datentyp

</td><td>
complexType

</td></tr></table>

<table><tr><td>
Bezeichnung

</td><td>
Iccsn

</td></tr><tr><td>
Beschreibung

</td><td>
Der Inhalt des Elements ICCSN ist das Suchkriterium, für das alle zugehörigen
Update Flags ausgelesen werden sollen.

</td></tr><tr><td>
Datentyp

</td><td>
string

</td></tr><tr><td>
Feldlänge

</td><td>
20

</td></tr><tr><td>
Wertebereich

</td><td>
80276[0-9]{15}

</td></tr></table>

### 3.1.2 Request-Header

Damit ein Intermediär auf Nachrichtenebene eine Lokalisation des Fachdienstes
vornehmen und der Fachdienst die Lokalisation prüfen kann, wird zusätzlich zu
den fachlichen Daten das ServiceLocalization-Element gemäß [gemSpec_SST_VSDM]
als SOAP-Header übertragen. Die Elemente des ServiceLocalization-Header
müssen vom Fachmodul entsprechend der Tabelle 4 gesetzt werden. Die Werte des
ServiceLocalization-Header müssen auf Korrektheit geprüft werden, damit von
dem Intermediär fehlgeleitete Nachrichten erkannt und abgewiesen werden.

<table><tr><th>
Element

</th><th>
Wert

</th></tr><tr><td>
ServiceType

</td><td>
„UFS“

</td></tr><tr><td>
ProviderId

</td><td>
Die 9-stellige Kostenträgerkennung. Der Wert wird aus dem Feld
organizationalUnitName im Subject Distinguished Name des C.CH.AUTZertifikates
des Versicherten auf der eGK ermittelt. Der Wert erlaubt die eindeutige
Zuordnung des Kostenträgers des Versicherten zu einem von diesem Kostenträger
betriebenen Dienst.

</td></tr></table>

### 3.1.3 Response

Diese Response liefert eine Liste aller Update Flags zu einer bestimmten ICCSN.
Die Reihenfolge der Update Flags in dieser Liste gibt die Reihenfolge vor, in
der die zugehörigen Vorgänge angestoßen werden müssen.

Optionale Aktualisierungen sind derzeit nicht vorgesehen. Falls in der jetzigen
Version optionale Aktualisierungen eingestellt werden, sollen diese ausgelassen
werden (siehe hierzu das Element UpdatePriority). Für die tatsächlich
angestoßenen, nicht optionalen Aktualisierungen ist die Reihenfolge aber
bindend. [VSDM-A_2285] [VSDM-A_2286]

Alle in dieser Liste direkt hintereinander stehenden Update Flags zur gleichen
Service-Localization müssen einzeln durch Aufrufe der Operation PerformUpdates
durchgeführt werden.

![Abbildung-4][Abbildung-4]

<table><tr><td>
Bezeichnung

</td><td>
GetUpdateFlagsResponse

</td></tr><tr><td>
Beschreibung

</td><td>
Operations-Element der Response der Operation GetUpdateFlags.

</td></tr><tr><td>
Datentyp

</td><td>
complexType

</td></tr></table>

<table><tr><td>
Bezeichnung

</td><td>
UpdateFlag

</td></tr><tr><td>
Beschreibung

</td><td>
Ein UpdateFlag-Element inklusive seiner Unterelemente entspricht jeweils einem
Aktualisierungsauftrag.

</td></tr><tr><td>
Datentyp

</td><td>
complexType

</td></tr></table>

<table><tr><td>
Bezeichnung

</td><td>
ServiceReceipt

</td></tr><tr><td>
Beschreibung

</td><td>
Ein ServiceReceipt-Element ist angegeben, wenn kein Aktualisierungsauftrag für
den VSDD vorliegt.

</td></tr><tr><td>
Datentyp

</td><td>
complexType

</td></tr></table>

![Abbildung-5][Abbildung-5]

<table><tr><td>
Bezeichnung

</td><td>
ServiceLocalization

</td></tr><tr><td>
Beschreibung

</td><td>
Mit dem Element ServiceLocalization wird angegeben, bei welchem Fachdienst ein
zugehöriger Vorgang angestoßen werden soll. Die Unterelemente von
ServiceLocalization müssen die gleichen Werte besitzen, mit denen der
Fachdienst registriert ist.

</td></tr><tr><td>
Datentyp

</td><td>
complexType

</td></tr></table>

<table><tr><td>
Bezeichnung

</td><td>
UpdateId

</td></tr><tr><td>
Beschreibung

</td><td>
Das Element UpdateId ist ein Identifier (Update-Identifier), mit dem mehrere
Update Flags unterschieden werden können, die zur gleichen ICCSN gehören und
die gleiche ServiceLocalization besitzen. Der Update-Identifier wird dem
Fachdienst bei der Initiierung der Kommunikation zwischen eGK und Fachdienst
(Operation PerformUpdates) übergeben, so dass der Fachdienst den
durchzuführenden Vorgang identifizieren kann.

</td></tr><tr><td>
Datentyp

</td><td>
hexBinary

</td></tr><tr><td>
Feldlänge

</td><td>
20

</td></tr></table>

<table><tr><td>
Bezeichnung

</td><td>
UpdatePriority

</td></tr><tr><td>
Beschreibung

</td><td>
Das Element UpdatePriority (Update-Priorität) gibt an, ob der zum Update Flag
zugehörige Vorgang zwingend angestoßen werden muss (MANDATORY) oder ob der
Anstoß optional ist (OPTIONAL).

Die Auswahl, ob für ein einzelnes Update Flag mit der Priorität OPTIONAL das
Update tatsächlich durchgeführt oder ausgelassen wird, erfolgt durch das
aufrufende System.

</td></tr><tr><td>
Datentyp

</td><td>
string

</td></tr><tr><td>
Wertebereich

</td><td>
MANDATORY | OPTIONAL

</td></tr></table>

<table><tr><td>
Bezeichnung

</td><td>
ShortDescription

</td></tr><tr><td>
Beschreibung

</td><td>
Das Element ShortDescription enthält einen kurzen Text, der den vom Fachdienst
durchzuführenden Vorgang beschreibt. Diese Beschreibung soll für die Anzeige
des Vorganges im Primärsystem verwendet werden. Für die drei Pflicht-Updates
VSD aktualisieren, eGK sperren und entsperren sollen diese Texte genutzt werden:

 ---> UL

</td></tr><tr><td>
Datentyp

</td><td>
string

</td></tr><tr><td>
Feldlänge

</td><td>
120

</td></tr></table>

![Abbildung-6][Abbildung-6]

<table><tr><td>
Bezeichnung

</td><td>
Type

</td></tr><tr><td>
Beschreibung

</td><td>
Für ein UpdateFlag-Element enthält das Element Type den Typ des Fachdienstes,
an den eine Anfrage gerichtet ist.

Für ein ServiceReceipt-Element enthält das Element Type den Typ des
Fachdienstes, der die Prüfziffer generiert.

Jede Fachanwendung definiert das für die Dienste gültige Kürzel.

</td></tr><tr><td>
Datentyp

</td><td>
string

</td></tr><tr><td>
Wertebereich

</td><td>
VSD | CMS   für UpdateFlag-Element

UFS   für ServiceReceipt-Element

</td></tr></table>

<table><tr><td>
Bezeichnung

</td><td>
Provider

</td></tr><tr><td>
Beschreibung

</td><td>
Das Feld Provider dient der Servicelokalisierung und identifiziert den Provider.
Für die Fachanwendung VSDM wird die Kostenträgerkennung des Zertifikats des
Versicherten auf der eGK genutzt.

Der angegebene Wertebereich wird nicht über das Schema festgelegt, sondern der
Empfänger muss bei der Verarbeitung die Lokalisierung prüfen.

</td></tr><tr><td>
Datentyp

</td><td>
string

</td></tr><tr><td>
Feldlänge

</td><td>
9

</td></tr><tr><td>
Wertebereich

</td><td>
[0-9]

</td></tr></table>

![Abbildung-7][Abbildung-7]

<table><tr><td>
Bezeichnung

</td><td>
ServiceLocalization

</td></tr><tr><td>
Beschreibung

</td><td>
Mit dem Element ServiceLocalization wird angegeben, zu welchem Fachdienst die
zugehöriger fachdienstspezifische Prüfziffer gehört.

</td></tr><tr><td>
Datentyp

</td><td>
complexType

</td></tr></table>

Die Unterelemente Type und Provider sind bereits im Zusammenhang mit dem Element
UpdateFlag beschrieben.

<table><tr><td>
Bezeichnung

</td><td>
Receipt

</td></tr><tr><td>
Beschreibung

</td><td>
Dieses Element beinhaltet die Prüfziffer des Fachdienstes als eine
Base64Binary-kodierte Folge von bis zu 65 Bytes.

Das Format der Prüfziffer ist gemäß Lastenheft aufgebaut und auf den
verwendeten Zeichensatz und –länge beschränkt. Der Aufbau der Prüfziffer
ist kassenübergreifend vorgegeben. Dieser setzt sich aus zwei Teilen zusammen:

Prüfziffer = Kryptographische Funktion (z. B. HMAC mit SHA-256) [Teil 1:
Vorgangskennung | Teil 2: Kryptographisches Material]key

Es erfolgt keine Auswertung des Receipts durch das Fachmodul.

</td></tr><tr><td>
Datentyp

</td><td>
base64Binary

</td></tr></table>

### 3.2 Fehlerbehandlung

Die Beschreibung der Fehlerbehandlung und Struktur der gematik SOAP Faults
erfolgt in der Spezifikation „Schnittstellenspezifikation Transport VSDM“
[gemSpec_SST_VSDM]. Für die hier beschriebene Schnittstelle der
Anwendungsebene erfolgt lediglich die Festlegung der Fehlercodes auf
Anwendungsebene (s. Tabelle 16).

Der ComponentType ist für alle an dieser Schnittstelle auftretenden, auch
übergreifenden Fehlercodes gemäß [gemSpec_SST_VSDM], Fehler „UFS“. Da er
für alle aufgeführten Fehlercodes gilt, wird er nicht extra pro Fehlercode
angegeben. [VSDM-A_2329]

<table><tr><th>
Code

</th><th>
ErrorType

</th><th>
Severity

</th><th>
ErrorText

</th><th>
Befüllung  
Detail

</th><th>
Auslösende Bedingung

</th></tr><tr><td>
11101

</td><td>
Technical

</td><td>
Fatal

</td><td>
Für die eGK  
mit der  
angegebenen  
ICCSN ist der  
aufgerufene  
Dienst
nicht  
zuständig.

</td><td>
DARF NICHT  
verwendet  
werden

</td><td>
Für die eGK mit der  
angegebenen ICCSN  
ist dieser UFS nicht  
zuständig.

Es muss  
die, in der ICCSN  
enthaltene, Issuer  
Identification Number  
(IIN)
geprüft werden.  
Eine IIN ist dann falsch,  
wenn sie nicht den/die  
Issuer
(Kartenherausgeber)  
bezeichnet, für den/die  
dieser UFS betrieben wird.

Eine darüber hinausgehende  
Überprüfung der ICCSN ist  
optional, um auch
(einfache)  
UFS-Implementierungen zu  
ermöglichen, bei denen der  
UFS nur
genau diejenigen  
ICCSN kennt, für die Update  
Flags existieren.

</td></tr><tr><td>
11999

</td><td>
nicht vorgegeben

</td><td>
nicht vorgegeben

</td><td>
Ein nicht  
spezifizierter  
Fehler ist  
aufgetreten, zu  
dem weitere 

Details im  
Dienst  
protokolliert  
worden sind.

</td><td>
Kurzbeschrei-  
bung des  
Fehlers

</td><td>
Der aufgetretene Fehler  
ist keinem spezifizierten  
Fehlercode zuzuordnen. 

Weitere Details zum Fehler  
sind vom Dienst  
protokolliert worden.

</td></tr></table>

Für einen Fehler, der keinem bereits spezifizierten Fehlercode zugeordnet ist,
soll der Fehlercode 11999 angegeben werden. Dieser Fehlercode soll nur in
Ausnahmefällen verwendet werden.

Neben den in der Tabelle 16 aufgeführten Fehlercodes können die in der Tabelle
17 aufgeführten Fehlercodes vom Fachdienst verwendet werden, sofern das
eingesetzte Webservice-Framework diesen Fehler nicht bereits erkennt und mit
einem SOAP Fault darauf reagiert.

<table><tr><th>
Code

</th><th>
ErrorType

</th><th>
Severity

</th><th>
ErrorText

</th><th>
Befüllung  
Detail

</th><th>
Auslösende  
Bedingung

</th></tr><tr><td>
11148

</td><td>
Technical

</td><td>
Fatal

</td><td>
Die Payload  
ist nicht  
konform zum  
XML-Schema.

</td><td>
DARF  
NICHT  
verwendet  
werden

</td><td>
Im Payload  
ist kein zum  
XML-Schema  
konformer  
Request  
GetUpdateFlags 

angegeben.

</td></tr></table>

### 4 Card Communication Service

Erhält das Fachmodul ein oder mehrere Aktualisierungsaufträge (Update Flags),
kann das Fachmodul diese Aktualisierungen über die Operation PerformUpdates
der Schnittstelle CCS initiieren und durchführen. Beim ersten Aufruf übergibt
das Fachmodul dem Dienst einen Update-Identifier (Bestandteil der Update
Flags). Der Fachdienst ordnet den Update-Identifier dem durchzuführenden
Vorgang zu. [VSDM-A_2294] [VSDM-A_2295]

![Abbildung-8][Abbildung-8]

Damit der Fachdienst die folgenden Nachrichten nach dem initiierenden Aufruf
zuordnen kann, wird vom Dienst eine Sessioninformation erstellt und in der
ersten Antwortnachricht an das Fachmodul übergeben. Diese Sessioninformation
wird in den Aufrufen der Folgenachrichten angegeben. [VSDM-A_2297] [VSDM-A_2298]

Die Schnittstelle ermöglicht den Fachdiensten beliebige Kartenkommandos zur eGK
zu senden. Zwischen dem Fachdiensten und der eGK wird ein Trusted Channel
aufgebaut, über den die eigentliche Aktualisierung erfolgt. Aus diesem Grund
wird für den Auf- und Abbau des Trusted Channels sowie für alle Aktionen
innerhalb des Trusted Channels auf die Anwendung von zusätzlichen
nachrichtenbasierten Sicherheitsmechanismen verzichtet. Der Ablauf zur
Aktualisierung einer eGK wird in Kapitel 5 verdeutlicht. [VSDM-A_2302]
[VSDM-A_2999]

Prinzipiell sollen die Fachdienste aus Performancegründen bei einer
Aktualisierung der Stammdaten immer nur die VSD-Container aktualisieren, für
die auch Änderungen vorliegen. Eine Ausnahme diesbezüglich besteht dann, wenn
für die Aktualisierung des zu ändernden Containers eine neue Schemaversion
verwendet wird. In diesem Fall müssen alle VSD-Container aktualisiert werden,
um sicherzustellen, dass immer in allen drei VSD-Containern (PD, VD und GVD)
die Daten in derselben Schemaversion vorliegen. [VSDM-A_2546]

Zum Abschluss einer erfolgreichen Aktualisierung der VSD erstellt der Fachdienst
VSDD eine Prüfziffer, die vom Fachmodul in den Prüfungsnachweis aufgenommen
wird. Der Prüfungsnachweis dient als Nachweis einer durchgeführten
Aktualisierungsanfrage der VSD. Der Fachdienst CMS hingegen soll keine
Prüfziffer erstellen, da das Fachmodul die Prüfziffer des CMS nicht nutzt.
[VSDM-A_2341] [VSDM-A_2342]

Bei Änderung von Versichertenstammdaten muss der Fachdienst mit einem
vorhergehenden Kommando den Transaktionsstatus auf der eGK auf ‚1’ setzen.
Nach den Kommandos zum Ändern der Daten muss ein Kommando zum Zurücksetzen
des Transaktionsstatus auf ‚0’ folgen. [VSDM-A_2961]

In der Tabelle 18 sind die allgemeinen Werte der Schnittstelle aufgeführt.
Diese Werte werden unter anderem für die Kodierung der Endpunkt-Adresse der
Schnittstelle verwendet.

<table><tr><th>
Element

</th><th>
Wert

</th></tr><tr><td>
Provider-Kennung

</td><td>
Kostenträgerkennung

</td></tr><tr><td>
ServiceType

</td><td>
VSD | CMS

</td></tr><tr><td>
Schnittstellen-Version

</td><td>
2.0

</td></tr></table>

### 4.1 Operation PerformUpdates

Die Operation PerformUpdates initiiert die Kommunikation zwischen Dienst und
eGK. Durch die Übermittlung eines oder mehrerer Update-Identifier an den
Dienst, wird beim Dienst der durchzuführende Vorgang angestoßen. In der
Response zu dieser Operation wird vom Dienst bereits das erste Kommando-Paket
angegeben. Die Chipkarten-Kommandos werden von dieser Spezifikation nicht
beschränkt. Allerdings sind derzeit nur VSD-Aktualisierungen und die Sperrung
der Gesundheitsanwendung vorgesehen (s. Kapitel 5).

### 4.1.1 Request

![Abbildung-9][Abbildung-9]

<table><tr><td>
Bezeichnung

</td><td>
PerformUpdates

</td></tr><tr><td>
Beschreibung

</td><td>
Operations-Element des Request der Operation PerformUpdates.

</td></tr><tr><td>
Datentyp

</td><td>
complexType

</td></tr></table>

<table><tr><td>
Bezeichnung

</td><td>
Iccsn

</td></tr><tr><td>
Beschreibung

</td><td>
Das Element Iccsn enthält die ICCSN der eGK, für die Aktualisierungen
durchgeführt werden sollen.

Die Feldlänge und der Wertebereich des Elements ist im Kapitel 3.1.1
spezifiziert.

</td></tr><tr><td>
Datentyp

</td><td>
string

</td></tr><tr><td>
Feldlänge

</td><td>
20

</td></tr><tr><td>
Wertebereich

</td><td>
80276[0-9]{15}

</td></tr></table>

<table><tr><td>
Bezeichnung

</td><td>
UpdateId

</td></tr><tr><td>
Beschreibung

</td><td>
Der Spezifikation des Elements erfolgt im Kapitel 3.1.3.

</td></tr><tr><td>
Datentyp

</td><td>
hexBinary

</td></tr><tr><td>
Feldlänge

</td><td>
20

</td></tr></table>

<table><tr><td>
Bezeichnung

</td><td>
AdditionalInfo

</td></tr><tr><td>
Beschreibung

</td><td>
In der jetzigen Version darf das Element nicht verwendet werden.

Mit dem optionalen Element AdditionalInfo könnten zukünftig zusätzliche
fachdienstspezifische Informationen übergeben werden, die für die Ausführung
der Operation PerformUpdates erforderlich sind.

</td></tr><tr><td>
Datentyp

</td><td>
-

</td></tr></table>

### 4.1.2 Request-Header

Damit  der Fachdienst die Lokalisierung durchden Intermediär prüfen kann,
wird das ServiceLocalization-Element gemäß [gemSpec_SST_VSDM] im SOAP-Header
übertragen. Die Elemente des ServiceLocalization-Header müssen entsprechend
der Tabelle 23 gesetzt werden.

<table><tr><th>
Element

</th><th>
Wert

</th></tr><tr><td>
ServiceType

</td><td>
Der Wert muss aus dem zugehörigen Update Flag entnommen werden.

</td></tr><tr><td>
ProviderId

</td><td>
Der Wert muss aus dem zugehörigen Update Flag entnommen werden.

</td></tr></table>

### 4.1.3 Response

Die Response enthält für alle abgeschlossenen Aktualisierungsvorgänge eine
Liste von UpdatePerformed-Elementen, welche die erfolgreiche Durchführung der
Updates bestätigen, und das Element CommandPackage mit Chipkartenbefehlen zur
Durchführung einer weiteren Aktualisierung der eGK. Sind alle Aktualisierungen
abgeschlossen, enthält die Response anstelle des Elements CommandPackage das
Element Close. [VSDM-A_2317]

![Abbildung-10][Abbildung-10]

<table><tr><td>
Bezeichnung

</td><td>
PerformUpdatesResponse

</td></tr><tr><td>
Beschreibung

</td><td>
Operations-Element der Response der Operation PerformUpdates.

</td></tr><tr><td>
Datentyp

</td><td>
complexType

</td></tr></table>

<table><tr><td>
Bezeichnung

</td><td>
UpdatePerformed

</td></tr><tr><td>
Beschreibung

</td><td>
Für jede erfolgreich durchgeführte Aktualisierung wird ein
UpdatePerformed-Element mit den zugehörigen Elementen angegeben.

</td></tr><tr><td>
Datentyp

</td><td>
complexType

</td></tr></table>

<table><tr><td>
Bezeichnung

</td><td>
CommandPackage

</td></tr><tr><td>
Beschreibung

</td><td>
Im Element CommandPackage können ein oder mehrere Kommandos für die
Aktualisierung der eGK als Paket übertragen werden.

Es dürfen nur Kommandos zur Aktualisierung der VSD und zum Sperren/Entsperren
der DF.HCA durchgeführt werden.

Eine maximale Kommando-Gesamtgröße eines Paketes ist nicht vorgegeben.

</td></tr><tr><td>
Datentyp

</td><td>
complexType

</td></tr></table>

<table><tr><td>
Bezeichnung

</td><td>
Close

</td></tr><tr><td>
Beschreibung

</td><td>
Das Element Close wird angegeben, wenn kein (weiteres) Kommando-Paket für die
eGK ausgeführt werden soll. Das Element Close hat keinen Inhalt.

</td></tr><tr><td>
Datentyp

</td><td>
-

</td></tr></table>

![Abbildung-11][Abbildung-11]

<table><tr><td>
Bezeichnung

</td><td>
UpdateId

</td></tr><tr><td>
Beschreibung

</td><td>
Das Element UpdateId enthält den Update-Identifier des Vorganges, der
abgeschlossen wurde.

Die weitere Beschreibung des Elements erfolgt in dem Kapitel 3.1.3.

</td></tr><tr><td>
Datentyp

</td><td>
hexBinary

</td></tr><tr><td>
Feldlänge

</td><td>
20

</td></tr></table>

<table><tr><td>
Bezeichnung

</td><td>
Receipt

</td></tr><tr><td>
Beschreibung

</td><td>
Im Element Receipt wird die servicespezifische Prüfziffer für den erfolgreich
durchgeführten Vorgang mitgeliefert.

Die weitere Beschreibung des Elements erfolgt in dem Kapitel 3.1.3.

</td></tr><tr><td>
Datentyp

</td><td>
base64Binary

</td></tr></table>

<table><tr><td>
Bezeichnung

</td><td>
AdditionalInfo

</td></tr><tr><td>
Beschreibung

</td><td>
In der jetzigen Version darf das Element nicht verwendet werden.

Analog zum gleichnamigen Element im Request umfasst das optionale Element
AdditionalInfo-Elemente, mit denen zukünftig zusätzliche
fachdienstspezifische Informationen übergeben werden könnten.

</td></tr><tr><td>
Datentyp

</td><td>
-

</td></tr></table>

![Abbildung-12][Abbildung-12]

<table><tr><td>
Bezeichnung

</td><td>
LastIfOk

</td></tr><tr><td>
Beschreibung

</td><td>
Das optionale Attribut LastIfOk soll mit dem Wert „true“ angegeben werden,
wenn die folgende Bedingung erfüllt ist: Dies ist das letzte vom Fachdienst
versendete CommandPackage, falls alle Statuscodes, die die eGK zurückliefern
wird, mit den in diesem CommandPackage angegebenen erwarteten Statuscodes
übereinstimmen.

Das Attribut LastIfOk beendet nicht die Kommunikationssequenz, d. h. das
Absenden des folgenden Requestes „GetNextCommandPackageRequest“ kann zwar
parallelisiert werden, darf aber nicht entfallen.

</td></tr><tr><td>
Datentyp

</td><td>
boolean

</td></tr></table>

<table><tr><td>
Bezeichnung

</td><td>
CommandItem

</td></tr><tr><td>
Beschreibung

</td><td>
Das Element CommandItem enthält jeweils das auszuführende Kartenkommando und
die erwartete Antwort der eGK auf das Kartenkommando.

</td></tr><tr><td>
Datentyp

</td><td>
complexType

</td></tr></table>

![Abbildung-13][Abbildung-13]

<table><tr><td>
Bezeichnung

</td><td>
Command

</td></tr><tr><td>
Beschreibung

</td><td>
Das Element Command enthält in hexadezimaler Form eine vollständige
Command-APDU für die eGK. Dieses Kommando wird unverändert an die eGK
weitergeleitet. Der Aufbau und die Struktur der Kommando-APDUs sind für die
Standard-Betriebssystemkommandos in [gemSpec_COS] beschrieben. Durch die
Schnittstelle sind die Chipkarten-Kommandos jedoch nicht beschränkt. Eine
Übersicht, der für die vorgesehen Aktualisierungen notwendigen Kommandos, ist
im Kapitel 5 enthalten.

Die im Element Command angegebene Byte-Sequenz darf nicht mehr als 3082 Bytes
enthalten.

</td></tr><tr><td>
Datentyp

</td><td>
hexBinary

</td></tr></table>

<table><tr><td>
Bezeichnung

</td><td>
StatusCodeExpected

</td></tr><tr><td>
Beschreibung

</td><td>
Das Element StatusCodeExpected gibt den Statuscode an, der in der Antwort der
eGK erwartet wird. Durch einen Vergleich mit dem tatsächlich von der eGK
zurückgelieferten Statuscode kann hiermit vom Fachmodul eine unerwartete
Abweichung erkannt werden (s. 4.2.1).

</td></tr><tr><td>
Datentyp

</td><td>
CommandStatusCodeType

</td></tr><tr><td>
Feldlänge

</td><td>
2

</td></tr></table>

### 4.1.4 Response-Header

In der Response ist die Sessioninformation gemäß [gemSpec_SST_VSDM] im
SOAP-Header zu übertragen. Das Element des SessionIdentifier-Headers muss
entsprechend der Tabelle 35 gesetzt werden.

<table><tr><th>
Element

</th><th>
Wert

</th></tr><tr><td>
ConversationID

</td><td>
Die Vergabe der ConversationID erfolgt durch den Fachdienst. Erfolgt für einen
Aktualisierungsauftrag der Aufruf der Operation PerformUpdates erneut, erzeugt
der Fachdienst eine neue ConversationID und behandelt die vorhergehende
ConversationID als abgelaufen.

</td></tr></table>

### 4.2 Operation GetNextCommandPackage

Das Fachmodul fordert mit der Operation GetNextCommandPackage ein weiteres
Kommando-Paket für die eGK an. Vor der ersten Ausführung dieser Operation
MUSS die Operation PerformUpdates ausgeführt worden sein.

Im Request für diese Operation werden dem Fachdienst die letzten Antworten der
Chipkarte mitgeliefert. Diese Operation MUSS solange wiederholt abgesetzt
werden bis vom Dienst durch die Übermittlung des Elements Close in der
Response bestätigt wird, dass alle Aktualisierungen beendet sind.

### 4.2.1 Request

Im Request werden alle Antworten der eGK zu allen ausgeführten Kommandos aus
dem letzten Kommando-Paket sequentiell aufgelistet. Liefert die eGK bei der
Ausführung der Kommandos eines Kommando-Paketes einen unerwarteten Status-Code
zurück, werden keine weiteren Kommandos aus dem Kommando-Paket ausgeführt. In
einem solchen Fall, werden alle Antworten, der bis dahin erfolgreich
ausgeführten Kommandos einschließlich des Kommandos, bei dem der Statuscode
ungleich dem erwarteten Statuscode war, zurückgeliefert. [VSDM-A_2552]
[VSDM-A_2553]

Ein Sonderfall bildet hier der Response-Code "63 Cx". Er ist für die
Abarbeitung durch das Fachmodul wie ein "90 00" zu betrachten, sollte aber in
der Response an den Fachdienst zurückgegeben werden. Die Abarbeitung der
Kommando-Pakete wird hier nicht abgebrochen. [VSDM-A_2552]

Wenn die Verbindung zur eGK abbricht, wird hinter dem letzten Element
CommandResponse das Element Abort angegeben. Konnte vorher kein Kommando
ausgeführt werden, wird nur das Element Abort angegeben. [VSDM-A_3008]

![Abbildung-14][Abbildung-14]

<table><tr><td>
Bezeichnung

</td><td>
GetNextCommandPackage

</td></tr><tr><td>
Beschreibung

</td><td>
Operations-Element des Request der Operation GetNextCommandPackage.

</td></tr><tr><td>
Datentyp

</td><td>
complexType

</td></tr></table>

<table><tr><td>
Bezeichnung

</td><td>
CommandResponsePackage

</td></tr><tr><td>
Beschreibung

</td><td>
Im Element CommandResponsePackage können ein oder mehrere Antworten der eGK zu
den ausgeführten Kommandos aus dem letzten Kommando-Paket als Paket
übertragen werden.

Eine maximale Kommando-Gesamtgröße eines Paketes ist nicht vorgegeben

</td></tr><tr><td>
Datentyp

</td><td>
complexType

</td></tr></table>

![Abbildung-15][Abbildung-15]

<table><tr><td>
Bezeichnung

</td><td>
CommandResponse

</td></tr><tr><td>
Beschreibung

</td><td>
Das Element CommandResponse enthält in hexadezimaler Form eine vollständige
Response-APDU der eGK. Eine Beschreibung zum Aufbau der Response-APDU ist in
[gemSpec_COS] zu finden.

</td></tr><tr><td>
Datentyp

</td><td>
hexBinary

</td></tr></table>

<table><tr><td>
Bezeichnung

</td><td>
Abort

</td></tr><tr><td>
Beschreibung

</td><td>
Wenn die Verbindung zur eGK abbricht, wird dieses Element angegeben. Die Angabe
des Elements beendet die Kommunikationssequenz, d. h. in der zu diesem Request
nachfolgende Response darf der Fachdienst keine weiteren Kommandos an die eGK
übermitteln, sondern muss die Kommunikation mit dem Element Close beenden.

Das Abort Element hat keinen Inhalt.

</td></tr><tr><td>
Datentyp

</td><td>
complexType

</td></tr></table>

![Abbildung-16][Abbildung-16]

<table><tr><td>
Bezeichnung

</td><td>
CommandSentToCard

</td></tr><tr><td>
Beschreibung

</td><td>
Das Attribut CommandSentToCard gibt an, ob das Kommando bereits in Richtung eGK
abgeschickt wurde und erst danach die Verbindung abgebrochen ist
(CommandSentToCard = true) oder ob die Verbindung abgebrochen ist noch bevor
das Kommando in Richtung eGK abgeschickt werden konnte (CommandSentToCard =
false).

</td></tr><tr><td>
Datentyp

</td><td>
boolean

</td></tr></table>

### 4.2.2 Request-Header

Damit ein Intermediär auf Nachrichtenebene eine Lokalisierung des Fachdienstes
vornehmen und der Fachdienst die Lokalisierung prüfen kann, wird zusätzlich
zu den fachlichen Daten das ServiceLocalization-Element gemäß
[gemSpec_SST_VSDM] als SOAP-Header übertragen. Die Elemente des
ServiceLocalization-Header müssen entsprechend der Tabelle 41 gesetzt werden.

<table><tr><th>
Element

</th><th>
Wert

</th></tr><tr><td>
ServiceType

</td><td>
Der Wert muss aus der zugehörigen Update Flag entnommen werden.

</td></tr><tr><td>
ProviderId

</td><td>
Der Wert muss aus der zugehörigen Update Flag entnommen werden.

</td></tr></table>

Ebenfalls in dem Request muss das SessionInformation-Element gemäß
[gemSpec_SST_VSDM] als SOAP-Header übertragen werden. Das Element des
SessionInformation-Header müssen entsprechend der Tabelle 42 gesetzt werden.

<table><tr><th>
Element

</th><th>
Wert

</th></tr><tr><td>
ConversationID

</td><td>
Die ConversationID muss der ConversationID aus dem SOAP-Header der Response der
Operation PerformUpdates entsprechen.

</td></tr></table>

### 4.2.3 Response

![Abbildung-17][Abbildung-17]

Die Response entspricht der Response der Operation PerformUpdates. Die
Beschreibung der Response-Elemente erfolgt in dem Kapitel 4.1.3. [VSDM-A_2334]

### 4.3 Fehlerbehandlung

Die genaue Beschreibung der Fehlerbehandlung erfolgt in dem Dokument
„Schnittstellenspezifikation Transport VSDM“ [gemSpec_SST_VSDM]. Für die
hier beschriebene Schnittstelle erfolgt lediglich die Festlegung der sich aus
der Schnittstelle ergebenen Fehlercodes (s. Tabelle 43).

Der ComponentType ist für alle an dieser Schnittstelle auftretenden, auch
übergreifenden Fehlercodes gemäß [gemSpec_SST_VSDM], Fehler „CCS“. Da er
für alle aufgeführten Fehlercodes gilt, wird er nicht extra pro Fehlercode
angegeben. [VSDM-A_2328]

<table><tr><th>
Code

</th><th>
Error  
Type

</th><th>
Severity

</th><th>
ErrorText

</th><th>
Befüllung  
Detail

</th><th>
Auslösende  
Bedingung

</th></tr><tr><td>
12101

</td><td>
Tech  
nical

</td><td>
Fatal

</td><td>
Für die  
angegebene  
Kombination  
aus ICCSN  
und Update-  
Identifier 

liegt kein  
Update vor.

</td><td>
Beschreibung  
des Fehlers  
mit Angabe  
des Update-Identifier

</td><td>
Die Kombination  
(ICCSN, Update-Identifier)  
ist dem Dienst nicht bekannt, 

d. h. der Dienst kann hierzu  
keinen Vorgang zuordnen,  
den er durchführen
soll.

</td></tr><tr><td>
12102

</td><td>
Tech  
nical

</td><td>
Fatal

</td><td>
Für das  
angefragte  
Update ist die  
Durchführung  
eines anderen  
Updates
eine  
Vorbedingung.

</td><td>
Beschreibung  
des Fehlers  
mit Angabe  
des Update-Identifier

</td><td>
Der zum Update-Identifier  
zugehörige Vorgang kann  
nicht durchgeführt
werden,  
da die Durchführung eines  
anderen Updates eine  
Vorbedingung ist.
Dieser  
Fehler kann zum Beispiel  
auftreten, wenn das  
Client-System eine 

vorgegebene Reihenfolge  
von Update-Identifier nicht  
einhält.

</td></tr><tr><td>
12103

</td><td>
Security

</td><td>
Fatal

</td><td>
Die  
Authentifizierung  
zwischen  
Fachdienst und  
eGK mittels des 

fachdienst-  
spezifischen, kartenindividuellen symmetrischen  
Schlüssels
ist  
fehlgeschlagen.

</td><td>
Beschreibung  
des Fehlers  
mit Angabe  
des Update-Identifier

</td><td>
Der zum Update-Identifier  
zugehörige Vorgang konnte  
nicht erfolgreich
durchgeführt  
werden, da eine  
Authentifizierung  
zwischen Fachdienst und 

eGK mittels des  
fachdienstspezifischen  
kartenindividuellen  
symmetrischen
Schlüssels  
nicht erfolgreich durchgeführt  
werden konnte.

</td></tr><tr><td>
12105

</td><td>
Technical

</td><td>
Fatal

</td><td>
Die eGK ist  
defekt.

</td><td>
Beschreibung  
des Fehlers  
mit Angabe  
des Update-Identifier

</td><td>
Der zum Update-Identifier  
zugehörige Vorgang konnte  
nicht erfolgreich
durchgeführt  
werden, da die Chipkarte  
defekt ist. Dieser Fehler  
darf nur
dann gemeldet  
werden, wenn der Fachdienst  
anhand der zurückgemeldeten 

Statuscodes der Chipkarte  
einen Defekt festgestellt hat,  
z. B. einen
Speicherfehler.  
Dieser Fehler darf nicht  
zurückgemeldet werden,  
wenn
lediglich die  
Kommunikation vom  
Client-System mit dem  
Element Abort
(siehe 4.1.3)  
abgebrochen wurde.

</td></tr><tr><td>
12999

</td><td>
nicht  
vorgegeben

</td><td>
nicht  
vorge-  
geben

</td><td>
Ein nicht  
spezifizierter  
Fehler ist  
aufgetreten, zu  
dem weitere 

Details im Dienst  
protokolliert  
worden sind.

</td><td>
Beschreibung  
des Fehlers

</td><td>
Der aufgetretene Fehler  
ist keinem spezifizierten  
Fehlercode zuzuordnen. 

Weitere Details zum Fehler  
sind vom Dienst protokolliert  
worden.

</td></tr></table>

Ist für die Befüllung des Details-Elements die Angabe des Update-Identifier
gefordert, muss das Element Detail eine Fehlermeldung im Format „plain“
enthalten, in der dieser Update-Identifier angegeben ist. Dieser
Update-Identifier muss derjenige sein, zu dem der zugehörige
Aktualisierungsvorgang nicht erfolgreich abgeschlossen werden konnte.
[VSDM-A_2331]

Für einen Fehler, der keinem bereits spezifizierten Fehlercode zugeordnet ist,
muss der Fehlercode 12999 angegeben werden. Dieser Fehlercode soll nur in
Ausnahmefällen verwendet werden.

Bei "Fehlern", die mittels weiterer Command-Packages behoben werden können,
darf keine Fehlermeldung vom Fachdienst erzeugt werden, sondern es müssen
stattdessen die entsprechenden weiteren CommandPackage-Elemente übertragen
werden. [VSDM-A_2332]

Neben den in der Tabelle 43 aufgeführten Fehlercodes können die in der Tabelle
44 aufgeführten Fehlercodes vom Fachdienst verwendet werden, sofern das
eingesetzte Webservice-Framework diesen Fehler nicht bereits erkennt und mit
einem SOAP Fault darauf reagiert.

<table><tr><th>
Code

</th><th>
Error  
Type

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
12148

</td><td>
Technical

</td><td>
Fatal

</td><td>
Die Payload  
ist nicht  
konform zum  
XML-Schema.

</td><td>
DARF  
NICHT  
verwendet  
werden

</td><td>
Im Payload ist kein zum  
XML-Schema konformer  
Request PerformUpdates  
oder 

GetNextCommandpackage  
angegeben.

</td></tr></table>

### 5 Kommandosequenzen (informativ)

Die Fachdienste steuern mittels der Kommandopakete, die innerhalb der
Operationen PerformUpdates und GetNextCommandPackage übermittelt werden, die
Verarbeitung von Aktualisierungen durch die eGK. Dem Fachmodul fällt nur die
Aufgabe zu, die jeweiligen Kartenkommandos vom Fachdienst abzufragen, sie an
die eGK weiterzuleiten und die jeweiligen Ergebnisse der Kartenkommandos an den
Fachdienst zurückzuliefern. Der Fachdienst organisiert hierbei sowohl den
Aufbau des Trusted Channels als auch das Schreiben auf die eGK.

In diesem Kapitel werden exemplarisch die notwendigen Kommandosequenzen für
eine Aktualisierung der eGK aufgeführt. Dabei werden sowohl die
Kommandosequenz zum Aktualisieren der VSD als auch zum Sperren der
Gesundheitsanwendung betrachtet.

Es sollen so wenig wie möglich Kommandopakete pro Aktualisierung entsprechend
den Möglichkeiten der Kartensysteme gesendet werden. Die hier angegebenen
Sequenzen soll keine Implementierungsvorschrift darstellen. So ist es durchaus
vorstellbar, die Anzahl der Kartenbefehle durch eine andere Gruppierung der
Kommandopakete zu minimieren.

### 5.1 Ablauf

![Abbildung-18][Abbildung-18]

In der Tabelle 45 sind die in der Abbildung 18 dargestellten Schritte während
der Aktualisierung der eGK weiter erläutert. Sofern in den jeweiligen
Schritten Kartenbefehle bzw. die Antworten relevant sind, ist in der Spalte
APDUs eine Referenz zu der Tabelle aufgeführt, die die Kartenbefehle bzw.
Antworten enthält.

Wenn in der Beschreibung eines Schrittes auf einen fachdienstspezifischen
Schlüssel verwiesen wird, so wird für diesen die allgemeine Abkürzung
„CM“ verwendet. Die Abkürzung „CM“ umfasst dabei jeweils die drei
verschiedenen Schlüssel CMS, VSD und VSDCMS. Somit umfasst z.B. die
Bezeichnung SK.CM die Schlüssel SK.CMS, SK.VSD und SK.VSDCMS. Welcher dieser
Schlüssel konkret in dem Ablauf eingesetzt wird hängt vom jeweiligen Kontext
ab.

<table><tr><th>
Schritt

</th><th>
Funktion

</th><th>
Beschreibung

</th><th>
APDUs

</th></tr><tr><td>
1

</td><td>
PerformUpdates

</td><td>
Initial wird dem Fachdienst die ICCSN der zu aktualisierenden eGK und die
UpdateId als Kennzeichen der durchzuführenden Aktualisierung übermittelt.

</td><td>
</td></tr><tr><td>
2

</td><td>
PerformUpdates-Response (ManageSecurity-Environment)

</td><td>
Als Antwort auf den Operationsaufruf PerformUpdates bereitet der Fachdienst das
erste Kommandopaket auf. Dieses Kommandopaket beinhaltet den Befehl zum
Einstellen des Security Environment (ManageSecurityEnvironment) sowie dem
Befehle zum Generieren und Ausgeben einer Zufallszahl (GetChallenge).

</td><td>
s. Tabelle 46

</td></tr><tr><td>
3

</td><td>
GetNextCommand Package

</td><td>
Nachdem die im vorherigen Schritt empfangenen Kartenbefehle von der eGK
verarbeitet wurden und der von der eGK erhaltenen Statuscode mit dem vom
Fachdienst übermittelten Erwartungswert übereinstimmt, wird eine neue Anfrage
an den Fachdienst gesandt. Diese Anfrage beinhaltet alle empfangen Antworten
der eGK.

</td><td>
s. Tabelle 47

</td></tr><tr><td>
4

</td><td>
InternalAuthenticate

</td><td>
Der Fachdienst führt eine interne Authentifikation durch.

Dazu berechnet der Fachdienst mit Hilfe seines Master Keys und den letzten 8
Stellen der ICCSN der eGK den geheimen Schlüssel SK.VSD, SK.CMS oder SK.VSDCMS
bestehend aus den Teilschlüsseln SK.CM.ENC und SK.CM.MAC für die weiteren
Operationen.

Mit Hilfe des Teilschlüssels SK.CM.ENC wird die gerade erhaltene Zufallszahl
RND_eGK, eine selbst generierte weitere Zufallszahl RND_CM, die letzten 8
Stellen der ICCSN der eGK sowie der ICCSN des Sicherheitsmoduls des
Fachdienstes und weitere Daten (KeyDerivationData) verschlüsselt. Über die
verschlüsselten Daten (CG_CM) wird zudem ein MAC (CC_CM) unter Nutzung des
Schlüssels SK.CM.MAC gebildet.

</td><td>
</td></tr><tr><td>
5

</td><td>
GetNextCommand PackageResponse (MutualAuthenticate)

</td><td>
Unter Verwendung der im vorherigen Schritt gebildeten Daten von CG_CM und CC_CM
bereitet der Fachdienst den Kartenbefehl MutualAuthenticate auf. Dieser
Kartenbefehl wird als einziger Befehl in der Antwort zurückgegeben.

</td><td>
s. Tabelle 48

</td></tr><tr><td>
6

</td><td>
GetNextCommand Package

</td><td>
Nachdem der im vorherigen Schritt empfangene Kartenbefehl von der eGK
verarbeitet wurde und der von der eGK erhaltene Statuscode mit dem vom
Fachdienst übermittelten Erwartungswert übereinstimmt, wird eine neue Anfrage
an den Fachdienst gesandt. Diese Anfrage beinhaltet die empfangene Antwort der
eGK.

Zur Verdeutlichung der Abläufe in der eGK:

Die eGK prüft zunächst die Echtheit der Prüfsumme (CC_CM) mit Hilfe des
Schlüssels SK.CM.MAC und entschlüsselt anschließend die erhaltenen Daten
(CG_CM) unter Nutzung von SK.CM.ENC. Über einen Vergleich der selbst
berechneten Zufallszahl RND_eGK mit der gerade entschlüsselten Zufallszahl
prüft die eGK die Echtheit des Fachdienstes.

Anschließend erzeugt die eGK mit Hilfe der entschlüsselten Daten und
zusätzlichen, in der eGK gespeicherten Daten (KeyDerivationData_eGK), einen
Session Key, welcher als Grundlage für das nachfolgende Secure Messaging gilt.

Entsprechend der in Schritt 4 beschrieben Vorgehensweise berechnet nun auch die
Karte ein Datenpaket CG_eGK und stellt diesem eine Prüfsumme CC_eGK nach.
CG_eGK und CC_eGK werden im Rahmen der Antwortdaten an den Fachdienst
übermittelt.

</td><td>
s. Tabelle 49

</td></tr><tr><td>
7

</td><td>
ExternelAuthenticate

</td><td>
Der Fachdienst prüft zunächst die Echtheit der Prüfsumme (CC_eGK) mit Hilfe
des Schlüssels SK.CM.MAC und entschlüsselt anschließend die erhaltenen Daten
(CG_eGK) unter Nutzung von SK.CM.ENC. Über einen Vergleich der selbst
berechneten Zufallszahl RND_CM mit der gerade entschlüsselten Zufallszahl
prüft der Fachdienst die Echtheit der eGK.

Anschließend erzeugt der Fachdienst mit Hilfe der entschlüsselten Daten und
zusätzlichen mit den im Fachdienst vorliegenden Daten (KeyDerivationData_CM)
einen Session Key, welcher als Grundlage für das nachfolgende Secure Messaging
gilt.

</td><td>
</td></tr><tr><td>
8

</td><td>
GetNextCommand PackageResponse (Secure Messaging)

</td><td>
Nach der gegenseitigen Authentifizierung und der durchgeführten
Schlüsselvereinbarung können vom Fachdienst mittels Secure Messaging weitere
Kartenbefehle sicher übermittelt werden.

Handelt es sich bei der Aktualisierung um ein VSD-Update, so werden Befehle zum
Setzen des Transaktionsstatus, zur Aktualisierung der Daten und zum
Zurücksetzen des Transaktionsstatus gesendet. Für das Sperren bzw. Entsperren
der Gesundheitsanwendung wird nur ein entsprechender Befehl benötigt.

</td><td>
s. Tabelle 50,

Tabelle 51,

oder

Tabelle 53

</td></tr><tr><td>
9

</td><td>
GetNextCommand Package (Aktualisierung beendet)

</td><td>
Die Aktualisierung der eGK ist beendet, sofern die im vorherigen Schritt
empfangenen Kartenbefehle von der eGK verarbeitet wurden und der von der eGK
erhaltene Statuscode mit dem vom Fachdienst übermittelten Erwartungswert
übereinstimmt.

Sofern in der letzten Antwort des Fachdienstes das Flag „LastIfOK“ gesetzt
war, ist dem Fachmodul somit bekannt, dass keine weiteren Kartenbefehle folgen
und es kann bereits jetzt im Ablauf mit weiteren Kartenbefehlen fortfahren
(z.B. durchführen eines C2C).

Trotz eines Fortfahrens im Ablauf werden die empfangenen Antworten der eGK an
den Fachdienst gesandt.

</td><td>
Tabelle 52

oder

Tabelle 54

</td></tr><tr><td>
10

</td><td>
GetNextCommand PackageResponse

(Prüfziffer)

</td><td>
Durch den Erhalt der letzten Antworten der eGK kann auch der Fachdienst eine
erfolgreiche Aktualisierung der eGK feststellen. Daraufhin übermittelt der
Fachdienst dem Fachmodul ein UpdatePerformed-Element (enthält die Prüfziffer)
und schließt die Aktualisierung somit ab.

</td><td>
</td></tr></table>

### 5.2 Kartenkommunikation

In den nachfolgenden Tabellen ist beispielhaft die direkte Kartenkommunikation
bei einer Aktualisierung der eGK zwischen Fachdienst und eGK aufgeführt. Die
kursiv dargestellten Kommandos sind optional.

<table><tr><th>
Nr.

</th><th>
APDU

</th><th>
Name

</th><th>
Zweck

</th></tr><tr><td>
RP1_01

</td><td>
00A4040C

</td><td>
Select Root

</td><td>
Initialisierung

</td></tr><tr><td>
RP1_02

</td><td>
00B09D0000

</td><td>
ReadBinary EF.ATR

</td><td>
APDUBuffer

</td></tr><tr><td>
RP1_03

</td><td>
00A4040C06D27600000102

</td><td>
Select DF.HCA

</td><td>
Selektion DF.HCA

</td></tr><tr><td>
RP1_04

</td><td>
002281A406830112800154

</td><td>
ManageSecurity  
Environment

</td><td>
MSE mit SK.VSD

</td></tr><tr><td>
RP1_05

</td><td>
0084000008

</td><td>
GetChallenge

</td><td>
Erzeuge Zufallszahl

</td></tr></table>

Das Kommando RP1_01 ist optional, da diese Initialisierung schon beim
Zurücksetzen der Karte vorgenommen werden muss.

Das Kommando RP1_02 ist ebenfalls optional. Es ist nicht notwendig, wenn dem
Fachdienst der Inhalt von EF.ATR schon bekannt ist. Anderenfalls jedoch ist es
notwendig.

Wenn die eGK-Fähigkeiten um Extended Length und Größe des APDU Buffer bekannt
sind, können auch die Kommandos RP1_03ff bereits unter Verwendung dieser
Informationen codiert sein.

Anmerkungen:

Ein Auslesen der ICCSN (ReadBinary EF.GDO) ist nicht notwendig, da die ICCSN dem
Fachdienst in der Anfrage mitgeteilt wird. Eine von der gesteckten eGK
abweichende ICCSN deutet auf einen Fehler der dezentralen TI oder einen Angriff
hin. Entsprechend selten tritt dieser Fall ein. Wenn er eintritt, wird dies
jedoch beim Aufbau des Secure Messaging bemerkt, da die ICCSN in EF.GDO zur
Berechnung der Schlüssel herangezogen wird, welche deshalb nicht zu den im
Fachdienst hinterlegten Schlüsseln passen. (Dabei gilt die Annahme, dass die
symmetrischen Schlüssel eGK-spezifisch sind)

Ein Auslesen des Transaktions-Flag (ReadBinary EF.StatusVD) ist nicht notwendig,
da der VSDD den Status der VSD-Aktualisierung aus den Response-APDUs der eGK
ermittelt.

<table><tr><th>
Nr.

</th><th>
Result

</th><th>
Name

</th><th>
Zweck

</th></tr><tr><td>
RQ2_01

</td><td>
´XX…YY || 9000´

</td><td>
Inhalt EF.ATR

</td><td>
APDU Buffer?

</td></tr><tr><td>
RQ2_02

</td><td>
9000

</td><td>
Ergebnis Select DF.HCA

</td><td>
</td></tr><tr><td>
RQ2_03

</td><td>
9000

</td><td>
Ergebnis MSE

</td><td>
</td></tr><tr><td>
RQ2_04

</td><td>
´YY…XX || 9000´

</td><td>
Zufallszahl

</td><td>
Aufbau SessionKey

</td></tr></table>

Die Antwort RQ2_01 ist optional. Sie wird nur erwartet, wenn das Kommando RP1_01
gesendet wurde (s. Tabelle 46).

<table><tr><th>
Nr.

</th><th>
APDU

</th><th>
Name

</th><th>
Zweck

</th></tr><tr><td>
RP2_01

</td><td>
´0082000068 || XX…XX || 00´

</td><td>
MutualAuthenticate

</td><td>
Aufbau SessionKey

</td></tr></table>

<table><tr><th>
Nr.

</th><th>
Result

</th><th>
Name

</th><th>
Zweck

</th></tr><tr><td>
RQ3_01

</td><td>
´XX…XX || 9000´

</td><td>
Ergebnis MutualAuthenticate

</td><td>
Aufbau SessionKey

</td></tr></table>

<table><tr><th>
Nr.

</th><th>
APDU

</th><th>
Name

</th><th>
Zweck

</th></tr><tr><td>
RP3_01

</td><td>
´0CA4040C

…

´

</td><td>
Select DF.HCA

</td><td>
Selektion DF.HCA

</td></tr><tr><td>
RP3_02

</td><td>
´0C440000

…

´

</td><td>
ACTIVATE

</td><td>
Aktivieren DF.HCA

</td></tr></table>

<table><tr><th>
Nr.

</th><th>
APDU

</th><th>
Name

</th><th>
Zweck

</th></tr><tr><td>
RP3_01

</td><td>
´0CA4040C

…

´

</td><td>
Select DF.HCA

</td><td>
Selektion DF.HCA

</td></tr><tr><td>
RP3_02

</td><td>
´0C040000

…

´

</td><td>
DEACTIVATE

</td><td>
Deaktivieren DF.HCA

</td></tr></table>

<table><tr><th>
Nr.

</th><th>
Result

</th><th>
Name

</th><th>
Zweck

</th></tr><tr><td>
RQ4_01

</td><td>
´990290008E08…9000´

</td><td>
Ergebnis Select DF.HCA

</td><td>
</td></tr><tr><td>
RQ4_02

</td><td>
´990290008E08…9000´

</td><td>
Ergebnis De-/Aktivierung

</td><td>
</td></tr></table>

<table><tr><th>
Nr.

</th><th>
APDU

</th><th>
Name

</th><th>
Zweck

</th></tr><tr><td>
RP3_01

</td><td>
´0CD68C

…´

</td><td>
UpdateBinary EF.StatusVD

</td><td>
Setzen Transaktions-Flag (,1’)

</td></tr><tr><td>
RP3_02.1  
RP3_02.2  
…  
RP3_02.i

</td><td>
´0CD68100…´  
´0CD600XX…´  
…  
´0CD6XXYY…´

</td><td>
UpdateBinary EF.PD

</td><td>
EF.PD aktualisieren

</td></tr><tr><td>
RP3_03.1  
RP3_03.2  
…  
RP3_03.i

</td><td>
´0CD68200…´  
´0CD600XX…´  
…  
´0CD6XXYY…´

</td><td>
UpdateBinary EF.VD

</td><td>
EF.VD aktualisieren

</td></tr><tr><td>
RP3_04

</td><td>
´0CD68300…´´

</td><td>
UpdateBinary EF.GVD

</td><td>
EF.GVD aktualisieren

</td></tr><tr><td>
RP3_05

</td><td>
´0CD68C…´

</td><td>
UpdateBinary EF.StatusVD

</td><td>
Rücksetzen Transaktions-Flag (,0’)

</td></tr></table>

Anmerkung:

Im ersten Kommando RP3_01 muss das Transaktions-Flag gesetzt werden. Im letzten
Kommando RP3_05 muss das Transaktions-Flag zurückgesetzt werden. Die Anzahl
und Reihenfolge der dazwischen stattfindenden Update-Kommandos ist abhängig
vom jeweiligen Update. Es sollen auch nur die geänderten Dateien aktualisiert
werden. Die Dateigröße von EF.GVD ist so gering, dass es möglich ist, den
gesamten Dateiinhalt mit einem Kommando zu beschreiben.

<table><tr><th>
Nr.

</th><th>
Result

</th><th>
Name

</th><th>
Zweck

</th></tr><tr><td>
RQ4_01

</td><td>
´990290008E08…9000´

</td><td>
Transaktions-Flag gesetzt (‚1’)

</td><td>
Beginn der Transaktion

</td></tr><tr><td>
RQ4_02.1  
RQ4_02.2  
…  
RQ4_02.i

</td><td>
´990290008E08…9000´  
´990290008E08…9000´  
…  
´990290008E08…9000´

</td><td>
Update EF.PD

</td><td>
EF.PD aktualisiert

</td></tr><tr><td>
RQ4_03.1  
RQ4_03.2  
…  
RQ4_03.i

</td><td>
´990290008E08…9000´  
´990290008E08…9000´  
…  
´990290008E08…9000´

</td><td>
Update EF.VD

</td><td>
EF.VD aktualisiert

</td></tr><tr><td>
RQ4_04

</td><td>
´990290008E08…9000´

</td><td>
Update EF.GVD

</td><td>
EF.GVD aktualisiert

</td></tr><tr><td>
RQ4_05

</td><td>
´990290008E08…9000´

</td><td>
Transaktions-Flag gesetzt (‚0’)

</td><td>
Ende der Transaktion

</td></tr></table>

Anmerkung:

Am Ende eines erfolgreichen Updates ist das Transaktions-Flag zurückgesetzt
(‚0’).

### 6 Anhang A - Verzeichnisse

### 6.1 Abkürzungen

<table><tr><th>
Abkürzung

</th><th>
Bedeutung

</th></tr><tr><td>
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
Healthcareapplication

</td></tr><tr><td>
HTTP

</td><td>
Hypertext Transfer Protocols

</td></tr><tr><td>
ICCSN

</td><td>
Integrated Circuit Card Serial Number

</td></tr><tr><td>
ID

</td><td>
Identification

</td></tr><tr><td>
IIN

</td><td>
Issuer Identification Number

</td></tr><tr><td>
ISO

</td><td>
International Organization for Standardization

</td></tr><tr><td>
KVNR

</td><td>
Krankenversicherungsnummer

</td></tr><tr><td>
KVK

</td><td>
Krankenversichertenkarte

</td></tr><tr><td>
OCSP

</td><td>
Online Certificate Status Protocol

</td></tr><tr><td>
PD

</td><td>
Persönliche Versichertendaten

</td></tr><tr><td>
SMC (B/A/KTR)

</td><td>
Security Module Card

</td></tr><tr><td>
SSL

</td><td>
Secure Sockets Layer

</td></tr><tr><td>
TI

</td><td>
Telematikinfrastruktur

</td></tr><tr><td>
TLS

</td><td>
Transport Layer Security, die Vorgängerbezeichnung ist SSL

</td></tr><tr><td>
TTD

</td><td>
Telematik Transport Details

</td></tr><tr><td>
UFS

</td><td>
Update Flag Service

</td></tr><tr><td>
SOAP

</td><td>
Simple Object Access Protocol

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
WSDL

</td><td>
Web Services Description Language

</td></tr><tr><td>
XML

</td><td>
Extensible Markup Language

</td></tr></table>

### 6.2 Glossar

Das Glossar wird als eigenständiges Dokument, vgl. [gemGlossar_TI] zur
Verfügung gestellt.

### 6.3 Abbildungsverzeichnis

- [Abbildung-1] - – Dokumentenhierarchie im Projekt VSDM
- [Abbildung-2] - – Darstellung der UFS-WSDL
- [Abbildung-3] - – Element GetUpdateFlags
- [Abbildung-4] - – Element GetUpdateFlagsResponse
- [Abbildung-5] - – Element UpdateFlag
- [Abbildung-6] - – Element ServiceLocalization
- [Abbildung-7] - – Element ServiceReceipt-Element
- [Abbildung-8] - – Darstellung der CCS-WSDL
- [Abbildung-9] - – Element PerformUpdates
- [Abbildung-10] - – Element PerformUpdatesResponse
- [Abbildung-11] - – Element UpdatePerformed
- [Abbildung-12] - – Element CommandPackage
- [Abbildung-13] - – Element CommandItem
- [Abbildung-14] - – Element GetNextCommandPackage
- [Abbildung-15] - – Element CommandResponsePackage
- [Abbildung-16] - – Element Abort
- [Abbildung-17] - – Element GetNextCommandPackageResponse
- [Abbildung-18] - - Ablauf "Aktualisierung der eGK"

### 6.4 Tabellenverzeichnis

- [Tabelle-1] - Tab_SST_FD_01 – Allgemeine Werte der UFS Schnittstelle
- [Tabelle-2] - Tab_SST_FD_52 – Element GetUpdateFlags [VSDM-A_2310]
- [Tabelle-3] - Tab_SST_FD_53 – Element Iccsn [VSDM-A_2310]
- [Tabelle-4] - Tab_SST_FD_02 – Elemente des ServiceLocalization-Header für die Operation GetUpdateFlags [VSDM-A_2282] [VSDM-A_2283]
- [Tabelle-5] - Tab_SST_FD_03 – Element GetUpdateFlagsResponse
- [Tabelle-6] - Tab_SST_FD_04 - Element UpdateFlag
- [Tabelle-7] - Tab_SST_FD_05 - Element ServiceReceipt
- [Tabelle-8] - Tab_SST_FD_06 – Element ServiceLocalization [VSDM-A_2288]
- [Tabelle-9] - Tab_SST_FD_07 – Element UpdateId
- [Tabelle-10] - Tab_SST_FD_08 – Element UpdatePriority
- [Tabelle-11] - Tab_SST_FD_09 – Element ShortDescription
- [Tabelle-12] - Tab_SST_FD_10 – Element Type [VSDM-A_2288]
- [Tabelle-13] - Tab_SST_FD_11 – Element Provider [VSDM-A_2288]
- [Tabelle-14] - Tab_SST_FD_13 – Element ServiceLocalization [VSDM-A_2288]
- [Tabelle-15] - Tab_SST_FD_14 – Element Receipt [VSDM-A_2287]
- [Tabelle-16] - Tab_SST_FD_15 – Fehlercodes der UFS-Schnittstelle [VSDM-A_2290] [VSDM-A_2291] [VSDM-A_2292]
- [Tabelle-17] - Tab_SST_FD_16 – Optionale Fehlercodes der UFS-Schnittstelle [VSDM-A_2293]
- [Tabelle-18] - Tab_SST_FD_17 – Allgemeine Werte der CCS Schnittstelle
- [Tabelle-19] - Tab_SST_FD_18 – Element PerformUpdates [VSDM-A_2308]
- [Tabelle-20] - Tab_SST_FD_19 – Element Iccsn [VSDM-A_2308]
- [Tabelle-21] - Tab_SST_FD_20 – Element UpdateId [VSDM-A_2308]
- [Tabelle-22] - Tab_SST_FD_21 – Element AdditionalInfo [VSDM-A_2308] [VSDM-A_2335] [VSDM-A_2314]
- [Tabelle-23] - Tab_SST_FD_22 – Elemente des ServiceLocalization-Header der Operation PerformUpdates [VSDM-A_2303] [VSDM-A_2305]
- [Tabelle-24] - Tab_SST_FD_23 – Element PerformUpdatesResponse
- [Tabelle-25] - Tab_SST_FD_24 – Element UpdatePerformed [VSDM-A_2315]
- [Tabelle-26] - Tab_SST_FD_25 – Element CommandPackage [VSDM-A_2316]
- [Tabelle-27] - Tab_SST_FD_26 – Element Close
- [Tabelle-28] - Tab_SST_FD_27 – Element UpdateId [VSDM-A_2315]
- [Tabelle-29] - Tab_SST_FD_50 – Element Receipt [VSDM-A_2341] [VSDM-A_2315]
- [Tabelle-30] - Tab_SST_FD_28 – Element AdditionalInfo [VSDM-A_2315]
- [Tabelle-31] - Tab_SST_FD_29 – Attribut LastIfOk [VSDM-A_2339] [VSDM-A_2316]
- [Tabelle-32] - Tab_SST_FD_30 – Element CommandItem [VSDM-A_2316]
- [Tabelle-33] - Tab_SST_FD_31 – Element Command [VSDM-A_2318] [VSDM-A_2316]
- [Tabelle-34] - Tab_SST_FD_32 – Element StatusCodeExpected [VSDM-A_2316]
- [Tabelle-35] - Tab_SST_FD_33 – Elemente des SessionIdentifier-Header der Operation PerformUpdates
- [Tabelle-36] - Tab_SST_FD_34 – Element GetNextCommandPackage [VSDM-A_2311]
- [Tabelle-37] - Tab_SST_FD_35 – Element CommandResponsePackage [VSDM-A_2311]
- [Tabelle-38] - Tab_SST_FD_36 – Element CommandResponse [VSDM-A_2311]
- [Tabelle-39] - Tab_SST_FD_37 – Element Abort [VSDM-A_2311] [VSDM-A_3009]
- [Tabelle-40] - Tab_SST_FD_38 – Attribut CommandSentToCard [VSDM-A_2311]
- [Tabelle-41] - Tab_SST_FD_39 – Elemente des ServiceLocalization-Header der Operation GetNextCommandPackage [VSDM-A_2321] [VSDM-A_2305]
- [Tabelle-42] - Tab_SST_FD_40 – Elemente des SessionInformation-Header der Operation GetNextCommandPackage [VSDM-A_2321] [VSDM-A_2322]
- [Tabelle-43] - Tab_SST_FD_41 – Fehlercodes der CCS-Schnittstelle [VSDM-A_2323] [VSDM-A_2324] [VSDM-A_2325] [VSDM-A_2326] [VSDM-A_2327]
- [Tabelle-44] - Tab_SST_FD_42 – Optionale Fehlercodes der CCS-Schnittstelle [VSDM-A_2333]
- [Tabelle-45] - Ablauf „Aktualisierung der eGK“
- [Tabelle-46] - PerformUpdatesResponse (ManageSecurityEnvironment)
- [Tabelle-47] - GetNextCommandPackage 1
- [Tabelle-48] - GetNextCommandPackageResponse (MutualAuthenticate)
- [Tabelle-49] - GetNextCommandPackage 2
- [Tabelle-50] - GetNextCommandPackageResponse (Gesundheitsanwendung entsperren)
- [Tabelle-51] - GetNextCommandPackageResponse (Gesundheitsanwendung sperren)
- [Tabelle-52] - GetNextCommand Package (Gesundheitsanwendung ent-/sperren beendet)
- [Tabelle-53] - GetNextCommandPackageResponse (Stammdaten aktualisieren)
- [Tabelle-54] - GetNextCommand Package (Stammdaten Aktualisierung beendet)
- [Tabelle-55] - Eingangsanforderungen mit Nachweis der Abdeckung

### 6.5 Referenzierte Dokumente

### 6.5.1 Dokumente der gematik

Die nachfolgende Tabelle enthält die Bezeichnung der in dem vorliegenden
Dokument referenzierten Dokumente der gematik zur Telematikinfrastruktur. Der
mit der vorliegenden Version korrelierende Entwicklungsstand dieser Konzepte
und Spezifikationen wird pro Release in einer Dokumentenlandkarte definiert,
Version und Stand der referenzierten Dokumente sind daher in der nachfolgenden
Tabelle nicht aufgeführt. Deren zu diesem Dokument passende jeweils gültige
Versionsnummer entnehmen Sie bitte der aktuellsten, auf der Internetseite der
gematik veröffentlichten Dokumentenlandkarte, in der die vorliegende Version
aufgeführt wird.

<table><tr><th>
[Quelle]

</th><th>
Herausgeber (Erscheinungsdatum): Titel

</th></tr><tr><td>
[gemGlossar_TI]

</td><td>
gematik: Glossar der TI

</td></tr><tr><td>
[gemSpec_COS]

</td><td>
gematik: Spezifikation des Card Operating System (COS) – Elektrische
Schnittstelle

</td></tr><tr><td>
[gemSpec_SST_VSDM]

</td><td>
gematik: Schnittstellenspezifikation Transport VSDM

</td></tr><tr><td>
[gemSysL_VSDM]

</td><td>
gematik: Systemspezifisches Konzept Versichertenstammdatenmanagement

</td></tr></table>

### 6.5.2 Weitere Dokumente

<table><tr><th>
[Quelle]

</th><th>
Herausgeber (Erscheinungsdatum): Titel

</th></tr><tr><td>
[CCS.wsdl]

</td><td>
Schnittstellendefinition der CCS-Schnittstellen

</td></tr><tr><td>
[RFC2119]

</td><td>
RFC 2119 (März 1997): Key words for use in RFCs to Indicate Requirement Levels
S. Bradner,

http://tools.ietf.org/html/rfc2109

</td></tr><tr><td>
[UFS.wsdl]

</td><td>
Schnittstellendefinition der UFS-Schnittstellen

</td></tr></table>

### 7 Anhang B - Anforderungshaushalt

### 7.1 Eingangsanforderungen

<table><tr><td>
AFO-ID

</td><td>
Quelle

</td><td>
Beschreibung

</td><td>
Umgesetzt durch

</td></tr><tr><td>
VSDM-A_2101

</td><td>
[gemSysL_VSDM]

</td><td>
Der Fachdienst UFS MUSS eine SOAP-Schnittstelle mit der Operation GetUpdateFlags
für das Fachmodul VSDM bereitstellen.

</td><td>
VSDM-A_2280  
VSDM-A_2751

</td></tr><tr><td>
VSDM-A_2102

</td><td>
[gemSysL_VSDM]

</td><td>
Das Fachmodul VSDM MUSS die Aktualisierungsaufträge durch die Operation
GetUpdateFlags ermitteln.

</td><td>
VSDM-A_2285  
VSDM-A_2310

</td></tr><tr><td>
VSDM-A_2106

</td><td>
[gemSysL_VSDM]

</td><td>
Die Operation GetUpdateFlags der Schnittstelle des UFS MUSS die Ein- und
Ausgangsparameter der Tabelle "Tab_VSDM_SysL_31 Parameter der Operation
GetUpdateFlags" nutzen.

</td><td>
VSDM-A_2281  
VSDM-A_2285  
VSDM-A_2286  
VSDM-A_2287  
VSDM-A_2288 

VSDM-A_2290  
VSDM-A_2291  
VSDM-A_2341  
VSDM-A_2342

</td></tr><tr><td>
VSDM-A_2107

</td><td>
[gemSysL_VSDM]

</td><td>
Die Operation PerformUpdates MUSS die Ein- und Ausgangsparameter der Tabelle
"Tab_VSDM_SysL_32 Parameter der Operation PerformUpdates" nutzen.

</td><td>
VSDM-A_2308  
VSDM-A_2314  
VSDM-A_2315  
VSDM-A_2316  
VSDM-A_2317 

VSDM-A_2318  
VSDM-A_2324  
VSDM-A_2335  
VSDM-A_2339  
VSDM-A_2552 

VSDM-A_2553

</td></tr><tr><td>
VSDM-A_2108

</td><td>
[gemSysL_VSDM]

</td><td>
Die Operation GetNextCommandPackage MUSS die Ein- und Ausgangsparameter der
Tabelle "Tab_VSDM_SysL_33 Parameter der Operation GetNextCommandPackage" nutzen.

</td><td>
VSDM-A_2311  
VSDM-A_2314  
VSDM-A_2315  
VSDM-A_2316  
VSDM-A_2317 

VSDM-A_2318  
VSDM-A_2335  
VSDM-A_2339  
VSDM-A_2552  
VSDM-A_2553 

VSDM-A_3008

</td></tr><tr><td>
VSDM-A_2109

</td><td>
[gemSysL_VSDM]

</td><td>
Das Fachmodul VSDM MUSS der Aufrufnachricht der Operation GetUpdateFlags die
Lokalisierungsinformationen Servicetype und Provider-Kennung hinzufügen.

</td><td>
VSDM-A_2282  
VSDM-A_2283

</td></tr><tr><td>
VSDM-A_2111

</td><td>
[gemSysL_VSDM]

</td><td>
Das Fachmodul VSDM MUSS der Aufrufnachricht der Operation PerformUpdates die
Lokalisierungsinformationen Servicetype und Provider-Kennung hinzufügen.

</td><td>
VSDM-A_2303

</td></tr><tr><td>
VSDM-A_2112

</td><td>
[gemSysL_VSDM]

</td><td>
Das Fachmodul VSDM MUSS der Aufrufnachricht der Operation GetNextCommandPackage
die Lokalisierungsinformationen Servicetype und Provider-Kennung hinzufügen.

</td><td>
VSDM-A_2321

</td></tr><tr><td>
VSDM-A_2113

</td><td>
[gemSysL_VSDM]

</td><td>
Das Fachmodul VSDM MUSS die Lokalisierungsinformationen für den VSDD und CMS
aus den Rückgabewerten des UFS entnehmen.

</td><td>
VSDM-A_2288  
VSDM-A_2303

</td></tr><tr><td>
VSDM-A_2114

</td><td>
[gemSysL_VSDM]

</td><td>
Die Fachdienst VSDD MUSS der Antwort der Operation PerformUpdates die Kennung
zur Zuordnung der Folgenachrichten (Sessioninformation) hinzufügen.

</td><td>
VSDM-A_2297

</td></tr><tr><td>
VSDM-A_2115

</td><td>
[gemSysL_VSDM]

</td><td>
Das Fachmodul VSDM MUSS der Aufrufnachricht der Operation GetNextCommandPackage
die Kennung zur Zuordnung der Folgenachrichten (Sessioninformation) hinzufügen.

</td><td>
VSDM-A_2298

</td></tr><tr><td>
VSDM-A_2116

</td><td>
[gemSysL_VSDM]

</td><td>
Das Fachmodul VSDM MUSS die Sessioninformation aus der Antwort der Operation
PerformUpdates in die Folgenachrichten (GetNextCommandPackage) übernehmen.

</td><td>
VSDM-A_2298  
VSDM-A_2321

</td></tr><tr><td>
VSDM-A_2117

</td><td>
[gemSysL_VSDM]

</td><td>
Der Fachdienst VSDD MUSS die Sessioninformation der Antwort der Operation
PerformUpdates für die interne Zuordnung der Folgenachrichten
(GetNextCommandPackage) nutzen.

</td><td>
VSDM-A_2322  
VSDM-A_2334

</td></tr><tr><td>
VSDM-A_2120

</td><td>
[gemSysL_VSDM]

</td><td>
Die Fachanwendung VSDM MUSS für die Schnittstellen Fehlermeldungen mit einer
einheitlichen Fehlerstruktur für die nachnutzenden Systeme definieren.

</td><td>
VSDM-A_2283  
VSDM-A_2290  
VSDM-A_2291  
VSDM-A_2292  
VSDM-A_2293 

VSDM-A_2305  
VSDM-A_2322  
VSDM-A_2323  
VSDM-A_2324  
VSDM-A_2325 

VSDM-A_2326  
VSDM-A_2327

</td></tr><tr><td>
VSDM-A_2121

</td><td>
[gemSysL_VSDM]

</td><td>
Die Operation PerformUpdates MUSS ohne Nachrichtensignatur ausführbar sein.

</td><td>
VSDM-A_2294  
VSDM-A_2295

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
VSDM-A_2328  
VSDM-A_2329  
VSDM-A_2331  
VSDM-A_2332  
VSDM-A_2333

</td></tr><tr><td>
VSDM-A_2157

</td><td>
[gemSysL_VSDM]

</td><td>
Der Fachdienst VSDD MUSS vor dem Aktualisieren der eGK den Aufbau eines Trusted
Channel zwischen der eGK und dem Fachdienst steuern.

</td><td>
VSDM-A_2302  
VSDM-A_2326

</td></tr><tr><td>
VSDM-A_2175

</td><td>
[gemSysL_VSDM]

</td><td>
Der Fachdienst VSDD MUSS beim Aktualisieren der Versichertenstammdaten den
Transaktionsstatus auf der eGK speichern.

</td><td>
VSDM-A_2961

</td></tr><tr><td>
VSDM-A_2178

</td><td>
[gemSysL_VSDM]

</td><td>
Der Fachdienst VSDD MUSS VSD-Aktualisierungen durchführen.

</td><td>
VSDM-A_2294  
VSDM-A_2546

</td></tr><tr><td>
VSDM-A_2179

</td><td>
[gemSysL_VSDM]

</td><td>
Der Fachdienst CMS MUSS Kartenaktualisierungen durchführen.

</td><td>
VSDM-A_2295

</td></tr><tr><td>
VSDM-A_2180

</td><td>
[gemSysL_VSDM]

</td><td>
Der Fachdienst UFS MUSS auf Anfragen des Fachmoduls VSDM Informationen zu
vorhandenen Aktualisierungsaufträge zurückgeben.

</td><td>
VSDM-A_2280  
VSDM-A_2286  
VSDM-A_2751

</td></tr><tr><td>
VSDM-A_2181

</td><td>
[gemSysL_VSDM]

</td><td>
Der Fachdienst CMS MUSS die Sessioninformation der Antwort der Operation
PerformUpdates für die interne Zuordnung der Folgenachrichten
(GetNextCommandPackage) nutzen.

</td><td>
VSDM-A_2322

</td></tr><tr><td>
VSDM-A_2182

</td><td>
[gemSysL_VSDM]

</td><td>
Der Fachdienst CMS MUSS der Antwort der Operation PerformUpdates die Kennung zur
Zuordnung der Folgenachrichten (Sessioninformation) hinzufügen.

</td><td>
VSDM-A_2297  
VSDM-A_2334

</td></tr><tr><td>
VSDM-A_2184

</td><td>
[gemSysL_VSDM]

</td><td>
Der Fachdienst CMS MUSS vor dem Aktualisieren der eGK den Aufbau eines Trusted
Channel zwischen der eGK und dem Fachdienst steuern.

</td><td>
VSDM-A_2302  
VSDM-A_2326

</td></tr><tr><td>
VSDM-A_2243

</td><td>
[gemSpec_SST_VSDM]

</td><td>
Die Fachanwendung VSDM MUSS in den WSDLs die Kodierungsmethode für der
SOAP-Nachrichten "wrapped document/literal" verwenden.

</td><td>
VSDM-A_2280  
VSDM-A_2294  
VSDM-A_2295

</td></tr><tr><td>
VSDM-A_2340

</td><td>
[gemSysL_VSDM]

</td><td>
Die Fachanwendung VSDM MUSS sicherstellen, dass eine Prüfziffer für das
Fachmodul im Ablauf der Aktualisierungsanfrage entweder vom UFS oder VSDD
erstellt wird.

</td><td>
VSDM-A_2287  
VSDM-A_2341  
VSDM-A_2342

</td></tr><tr><td>
VSDM-A_2130

</td><td>
[gemSysL_VSDM]

</td><td>
Der Fachdienst VSDD MUSS Log-Einträge zur Analyse von Abläufen, Performance
und Fehlerzuständen schreiben.

</td><td>
VSDM-A_2999

</td></tr><tr><td>
VSDM-A_2131

</td><td>
[gemSysL_VSDM]

</td><td>
Der Fachdienst CMS MUSS Log-Einträge zur Analyse von Abläufen, Performance und
Fehlerzuständen schreiben.

</td><td>
VSDM-A_2999

</td></tr><tr><td>
VSDM-A_2134

</td><td>
[gemSysL_VSDM]

</td><td>
Der Fachdienst VSDD MUSS dem berechtigten Akteur das Auslesen der eigenen
Log-Einträge ermöglichen

</td><td>
VSDM-A_2999

</td></tr><tr><td>
VSDM-A_2135

</td><td>
[gemSysL_VSDM]

</td><td>
Der Fachdienst CMS MUSS dem berechtigten Akteur das Auslesen der eigenen
Log-Einträge ermöglichen.

</td><td>
VSDM-A_2999

</td></tr></table>

### 7.2 Ausgangsanforderungen

**VSDM-A_2280 - Fachdienst UFS: GetUpdateFlags gemäß UFS.wsdl implementieren.**

Die UFS-Schnittstelle des Fachdienstes MUSS die Operation GetUpdateFlags gemäß
der Syntax der UFS.wsdl implementieren. **[\<=]**

**VSDM-A_2281 - Fachdienst UFS: Aktualisierungsauftrag eindeutig
identifizierbar**

Die UFS-Schnittstelle des Fachdienstes MUSS sicherstellen, dass ein
Aktualisierungsauftrag eindeutig durch das Tupel bestehend aus ICCSN,
Service-Localization und Update-Identifier identifizierbar ist. **[\<=]**

**VSDM-A_2282 - Fachmodul VSDM: RequestHeader bei Aufruf GetUpdateFlags**

Das Fachmodul VSDM MUSS bei Aufruf der Operation GetUpdateFlags den
Request-Header mit den Werten in Tabelle Tab_SST_FD_02 bilden. **[\<=]**

**VSDM-A_2283 - Fachdienst UFS: fehlgeleitete Nachrichten abweisen**

Die UFS-Schnittstelle des Fachdienstes MUSS bei fehlgeleiteten Nachrichten, die
nicht den Werten der Tabelle Tab_SST_FD_02 entsprechen, mit einem SOAP Fault
mit gematik Fehlerstruktur und dem Fehlercode 01006 (s. gemSpec_SST_VSDM)
antworten. **[\<=]**

**VSDM-A_2285 - Fachmodul VSDM: optionale Updates nicht ausführen**

Das Fachmodul VSDM MUSS UpdateFlags mit dem Wert OPTIONAL im Element
UpdatePriority ignorieren und für diese UpdateFlags keine Aktualisierung
durchführen. **[\<=]**

**VSDM-A_2286 - Fachdienst UFS: optionale UpdateFlags nicht senden**

Die UFS-Schnittstelle des Fachdienstes SOLL NICHT UpdateFlags mit dem Wert
OPTIONAL im Element UpdatePriority senden. **[\<=]**

**VSDM-A_2287 - Fachdienst UFS: Prüfziffer übermitteln**

Die UFS-Schnittstelle des Fachdienstes MUSS die Prüfziffer gemäß den
Festlegungen der Tabelle Tab_SST_FD_14 in die Antwortnachricht aufnehmen, wenn
kein Aktualisierungsauftrag für den VSDD vorliegt. **[\<=]**

**VSDM-A_2288 - Fachdienst UFS: Lokalisierungsinformation bilden**

Der Fachdienst UFS MUSS die Lokalisierungsinformation gemäß der Festlegungen
in den Tabellen Tab_SST_FD_06, Tab_SST_FD_10, Tab_SST_FD_11 und Tab_SST_FD_13
in dieAntwortnachricht aufnehmen. **[\<=]**

**VSDM-A_2290 - Fachdienst UFS: IIN der ICCSN unbekannt**

Die UFS-Schnittstelle des Fachdienstes MUSS die Issuer Identification Number in
der ICCSN des Requests prüfen und bei unbekannter Issuer Identification Number
mit einem SOAP Fault mit gematik Fehlerstruktur und dem Fehlercode 11101
gemäß den Festlegungen der Tabelle Tab_SST_FD_15 antworten. **[\<=]**

**VSDM-A_2291 - Fachdienst UFS: ICCSN unbekannt**

Die UFS-Schnittstelle des Fachdienstes MUSS, falls sie die optionale Validierung
der ICCSN ausführt, mit einem SOAP Fault mit gematik Fehlerstruktur und dem
Fehlercode 11101 gemäß den Festlegungen der Tabelle Tab_SST_FD_15 antworten,
wenn die ICCSN unbekannt ist. **[\<=]**

**VSDM-A_2292 - Fachdienst UFS: nicht spezifizierter Fehler**

Die UFS-Schnittstelle des Fachdienstes MUSS bei Fehlern auf Anwendungsebene,
denen kein anderer Fehlercode zugeordnet ist, mit einem SOAP Fault mit gematik
Fehlerstruktur und dem Fehlercode 11999 gemäß den Festlegungen der Tabelle
Tab_SST_FD_15 antworten. **[\<=]**

**VSDM-A_2293 - Fachdienst UFS: schema-invalide Requests**

Die UFS-Schnittstelle des Fachdienstes KANN bei schema-invaliden SOAP Body mit
einem SOAP Fault mit gematik Fehlerstruktur und dem Fehlercode 11148 gemäß
den Festlegungen der Tabelle Tab_SST_FD_16 antworten. **[\<=]**

**VSDM-A_2294 - Fachdienst VSDD: PerformUpdates und GetNextCommandPackage
gemäß der Syntax der CCS.wsdl implementieren**

Der Fachdienst VSDD MUSS die Operationen PerformUpdates und
GetNextCommandPackage gemäß der Syntax der CCS.wsdl implementieren. **[\<=]**

**VSDM-A_2295 - Fachdienst CMS: PerformUpdates und GetNextCommandPackage gemäß
der Syntax der CCS.wsdl implementieren**

Der Fachdienst CMS MUSS die Operationen PerformUpdates und GetNextCommandPackage
gemäß der Syntax der CCS.wsdl implementieren. **[\<=]**

**VSDM-A_2297 - CCS-Schnittstelle: Sessioninformation bilden**

Die CCS-Schnittstelle der Fachdienste MUSS die Sessioninformation erstellen und
in die Antwortnachricht aufnehmen, wenn die Operation PerformUpdates durch das
Fachmodul aufgerufen wird. **[\<=]**

**VSDM-A_2298 - Fachmodul VSDM: Sessioninformation für GetNextCommandPackage
übernehmen**

Das Fachmodul VSDM MUSS die Sessioninformation aus der Antwortnachricht der
Operation PerformUpdates entnehmen und für die folgenden Aufrufe der Operation
GetNextCommandPackage übernehmen. **[\<=]**

**VSDM-A_2302 - CCS-Schnittstelle: Trusted Channel aufbauen**

Die CCS-Schnittstelle der Fachdienste MUSS einen Trusted Channel mit der eGK
aufbauen, über den die Aktualisierung der eGK erfolgt. **[\<=]**

**VSDM-A_2303 - Fachmodul VSDM: Request-Header bei Aufruf PerformUpdates**

Das Fachmodul VSDM MUSS bei Aufruf der Operation PerformUpdates den
Request-Header mit den Werten aus Tab_SST_FD_22 bilden. **[\<=]**

**VSDM-A_2305 - CCS-Schnittstelle: fehlgeleitete Nachrichten abweisen**

Die CCS-Schnittstelle des Fachdienstes MUSS bei fehlgeleitetenNachrichten, die
nicht den Werten der Tabelle Tab_SST_FD_22 und Tab_SST_FD_39 entsprechen, mit
einem SOAP Fault mit gematik Fehlerstruktur und dem Fehlercode 01006 (s.
gemSpec_SST_VSDM) antworten. **[\<=]**

**VSDM-A_2308 - Fachmodul VSDM: Operation PerformUpdates aufrufen**

Das Fachmodul VSDM MUSS die Operation PerformUpdates gemäß den Festlegungen
der Tabellen Tab_SST_FD_18, Tab_SST_FD_19, Tab_SST_FD_20 und Tab_SST_FD_21
aufrufen. **[\<=]**

**VSDM-A_2310 - Fachmodul VSDM: Operation GetUpdateFlags aufrufen**

Das Fachmodul VSDM MUSS die Operation GetUpdateFlags gemäß den Festlegungen in
den Tabelle Tab_SST_FD_52 und Tab_SST_FD_53 aufrufen. **[\<=]**

**VSDM-A_2311 - Fachmodul VSDM: Operation GetNextCommandPackage aufrufen**

Das Fachmodul VSDM MUSS die Operation GetNextCommandPackage gemäß den
Festlegungen der Tabellen Tab_SST_FD_34, Tab_SST_FD_35, Tab_SST_FD_36,
Tab_SST_FD_37 und Tab_SST_FD_38 aufrufen. **[\<=]**

**VSDM-A_2314 - CCS-Schnittstelle: AdditionalInfo tolerieren**

Die CCS-Schnittstelle der Fachdienste SOLL das Element AdditionalInfo in der
Aufrufnachricht ignorieren, falls es in der Anfragenachricht enthalten ist. **[\<=]**

**VSDM-A_2315 - CCS-Schnittstelle: UpdatePerformed nutzen**

Die CCS-Schnittstelle der Fachdienste MUSS das Element UpdatePerformed gemäß
den Festlegungen der Tabellen Tab_SST_FD_24, Tab_SST_FD_27, Tab_SST_FD_50 und
Tab_SST_FD_28 in die Antwortnachricht aufnehmen, wenn der zum Update-Identifier
zugehörige Update-Vorgang beendet ist. **[\<=]**

**VSDM-A_2316 - CCS-Schnittstelle: CommandPackage nutzen**

Die CCS-Schnittstelle der Fachdienste MUSS das Element CommandPackage gemäß
den Festlegungen der Tabellen Tab_SST_FD_25, Tab_SST_FD_29, Tab_SST_FD_30,
Tab_SST_FD_31 und Tab_SST_FD_32 in die Antwortnachricht aufnehmen, um
Chipkartenbefehle zur Aktualisierung der eGK zu übermitteln. **[\<=]**

**VSDM-A_2317 - CCS-Schnittstelle: Close nutzen**

Die CCS-Schnittstelle der Fachdienste MUSS das Element Close in die
Antwortnachricht aufnehmen, wenn alle Aktualisierungen abgeschlossen sind. **[\<=]**

**VSDM-A_2318 - Fachmodul VSDM: Kommando-APDUs unverändert durchreichen**

Das Fachmodul VSDM MUSS die Kommando-APDUs gemäß Tabelle Tab_SST_FD_31
unverändert an die eGK durchreichen. **[\<=]**

**VSDM-A_2321 - Fachmodul VSDM: Request-Header bei Aufruf GetNextCommandPackage**

Das Fachmodul VSDM MUSS bei Aufruf der Operation GetNextCommandPackage die
Request-Header mit den Werten der Tabellen Tab_SST_FD_39 und Tab_SST_FD_40
bilden. **[\<=]**

**VSDM-A_2322 - CCS-Schnittstelle: Nachrichten mit abgelaufener Session
abweisen**

Die CCS-Schnittstelle der Fachdienste MUSS die Sessioninformationen bei Aufruf
der Operation GetNextCommandPackage anhand der Werte der Tabelle Tab_SST_FD_40
prüfen und bei abgelaufener oder unbekannter Session mit einem SOAP Fault mit
gematik Fehlerstruktur und dem Fehlercode 01014 (s. [gemSpec_SST_VSDM])
antworten. **[\<=]**

**VSDM-A_2323 - CCS-Schnittstelle: Aktualisierung in falscher Reihenfolge
abweisen**

Die CCS-Schnittstelle der Fachdienste MUSS mit einem SOAPFault mit gematik
Fehlerstruktur und dem Fehlercode 12102 gemäß den Festlegungen der Tabelle
Tab_SST_FD_41 antworten, wenn das Fachmodul die vorgegebene Reihenfolge bei
mehreren Aktualisierungen für denselben Fachdienst nicht einhält und die
Durchführung eines anderen Updates eine Vorbedingung ist. **[\<=]**

**VSDM-A_2324 - CCS-Schnittstelle: falsche Kombination ICCSN und
Update-Identifier abweisen**

Die CCS-Schnittstelle der Fachdienste MUSS mit einem SOAP Fault mit gematik
Fehlerstruktur und dem Fehlercode 12101 gemäß den Festlegungen der Tabelle
Tab_SST_FD_41 antworten, wenn die Kombination aus ICCSN und Update-Identifier
nicht bekannt ist. **[\<=]**

**VSDM-A_2325 - CCS-Schnittstelle: nicht spezifizierter Fehler**

Die CCS-Schnittstelle der Fachdienste MUSS bei Fehlern auf Anwendungsebene,
denen kein anderer Fehlercode zugeordnet ist, mit einem SOAP Fault mit gematik
Fehlerstruktur und dem Fehlercode 12999 gemäß den Festlegungen der Tabelle
Tab_SST_FD_41 antworten. **[\<=]**

**VSDM-A_2326 - CCS-Schnittstelle: Trusted Channel nicht aufgebaut**

Die CCS-Schnittstelle der Fachdienste MUSS, wenn die Authentifizierung beim
Aufbau des Trusted Channel nicht erfolgreich ist, mit einem SOAP Fault mit
gematik Fehlerstruktur und dem Fehlercode 12103 gemäß den Festlegungen der
Tabelle Tab_SST_FD_41 antworten. **[\<=]**

**VSDM-A_2327 - CCS-Schnittstelle: eGK defekt**

Die CCS-Schnittstelle der Fachdienste MUSS, mit einem SOAP Fault mit gematik
Fehlerstruktur und dem Fehlercode 12105 gemäß den Ergänzungen der Tabelle
Tab_SST_FD_41 antworten, wenn die eGK offensichtlich defekt ist, da die
zurückgelieferten Statuscodes nicht mit den erwarteten Werten übereinstimmen. **[\<=]**

**VSDM-A_2328 - CCS-Schnittstelle: ComponentType "CCS" verwenden**

Die CCS-Schnittstelle der Fachdienste MUSS für alle SOAP Faults mit gematik
Fehlerstruktur als ComponentType "CCS" verwenden. **[\<=]**

**VSDM-A_2329 - Fachdienst UFS: ComponentType "UFS" verwenden**

Die UFS-Schnittstelle des Fachdienstes MUSS für alle SOAP Faults mit gematik
Fehlerstruktur als ComponentType "UFS" verwenden. **[\<=]**

**VSDM-A_2331 - CCS-Schnittstelle: Detail-Element mit Update-Identifier**

Die CCS-Schnittstelle der Fachdienste MUSS einen Fehlertext mit dem
Update-Identifier der fehlgeschlagene Aktualisierung und dem Attribut Encoding
mit dem Wert "plain" erstellen, wenn ein SOAP Fault mit der Angabe des
Update-Identifier im Detail-Element gefordert ist. **[\<=]**

**VSDM-A_2332 - CCS-Schnittstelle: Fehler mit weiteren Command-Packages beheben**

Die CCS-Schnittstelle der Fachdienste SOLL keine Fehlermeldung erzeugen, wenn
die eGK während der Aktualisierung unerwartete Statuscodes meldet, die mittels
weiterer Command Packages behoben werden können. **[\<=]**

**VSDM-A_2333 - CCS-Schnittstelle: schema-invalide Anfragenachrichten**

Die CCS-Schnittstelle der Fachdienste KANN bei schema-invaliden
Anfragenachrichten auf Anwendungsebene mit einem SOAP Fault mit gematik
Fehlerstruktur mit Fehlercode 12148 antworten, falls die fehlerhafte
Aufrufnachricht nicht bereits durch das Webservice Framework zurückgewiesen
wurde. **[\<=]**

**VSDM-A_2334 - CCS-Schnittstelle: Sessioninformation bilden**

Die CCS-Schnittstelle der Fachdienste MUSS die Sessioninformation aus der
Anfragenachricht in dieAntwortnachricht übernehmen, wenn die Operation
GetNextCommandPackage vom Fachmodul aufgerufen wird. **[\<=]**

**VSDM-A_2335 - Fachmodul VSDM: AdditionalInfo nicht nutzen**

Das Fachmodul VSDM DARF NICHT das Element AdditionalInfo bei Aufruf der
Operationen der Schnittstelle CCS nutzen. **[\<=]**

**VSDM-A_2339 - CCS-Schnittstelle: LastIfOk nutzen**

Die CCS-Schnittstelle der Fachdienste SOLL das Attribut LastIfOk gemäß der
Tabelle Tab_SST_FD_29 mit dem Wert true in die Antwortnachricht aufnehmen, wenn
das CommandPackage das letzte vom Fachdienst versendete CommandPackage ist. **[\<=]**

**VSDM-A_2341 - Fachdienst VSDD: Prüfziffer übermitteln**

Der Fachdienst VSDD MUSS eine Prüfziffer gemäß den Festlegungen der Tabelle
Tab_SST_FD_50 in die Antwortnachricht aufnehmen. **[\<=]**

**VSDM-A_2342 - Fachdienst CMS: Prüfziffer nicht übermitteln**

Der Fachdienst CMS SOLL eine Prüfziffer für das Fachmodul VSDM NICHT
übermitteln. **[\<=]**

**VSDM-A_2546 - Fachdienst VSDD: Aktualisierung aller VSD-Container bei
Änderung der Schemaversion**

Der Fachdienst VSDD MUSS sofern für die Aktualisierung eines VSD-Containers auf
der eGK eine neue Schemaversion verwendet wird, auch die anderen VSD-Container
aktualisieren um sicherzustellen, dass in den drei VSD-Containern (PD, VD und
GVD) die Daten in derselben Schemaversion vorliegen. **[\<=]**

**VSDM-A_2552 - Fachmodul VSDM: Abbruch bei unerwarteten Statuscode**

Das Fachmodul VSDM MUSS die Ausführung der Karten-Kommandos aus der Antwort des
Fachdienstes VSDD bzw. CMS bei einer Aktualisierung abbrechen, wenn der von der
eGK zurückgelieferte Statuscode nicht dem vom Fachdienst erwarteten Statuscode
(Element StatusCodeExpected) oder „63 Cx“ entspricht. **[\<=]**

**VSDM-A_2553 - Fachmodul VSDM: Response bei unerwarteten Statuscode**

Das Fachmodul VSDM MUSS, wenn die eGK bei der Ausführung eines Karten-Kommandos
einen unerwarteten Statuscode zurückliefert, alle Antworten der bis dahin
ausgeführten Karten-Kommandos in den folgenden Request an den Fachdienst
aufnehmen. **[\<=]**

**VSDM-A_2751 - Fachdienst UFS: Aktualisierungsaufträge zusammenführen**

Der Fachdienst UFS SOLL, falls mehrere Aktualisierungen vorliegen, diese
Aktualisierungen in einen Aktualisierungsauftrag zusammenführen, um den
Vorgang zu optimieren. **[\<=]**

**VSDM-A_2961 - Fachdienst VSDD: Transaktionsstatus setzen**

Der Fachdienst VSDD MUSS bei Änderung von Versichertenstammdaten mit einem
vorhergehenden Kommando den Transaktionsstatus auf der eGK auf ‚1’ setzen
und nach den Kommandos zum Ändern der Daten muss ein Kommando zum
Zurücksetzen des Transaktionsstatus auf ‚0’ folgen **[\<=]**

**VSDM-A_2999 - Fachdienst VSDD CMS: Logging von Fehlerzuständen**

Die Fachdienste VSDD und CMS MÜSSEN Log-Einträge der Anfragen aus der TI zur
Analyse von Abläufen und Fehlerzuständen schreiben. Die Fachdienste VSDD und
CMS MÜSSEN dem berechtigten Akteur das Auslesen der eigenen Log-Einträge
ermöglichen. **[\<=]**

**VSDM-A_3008 - Fachmodul VSDM: Response bei Abbruch**

Das Fachmodul VSDM MUSS, wenn die Verbindung zur eGK abbricht, das Element Abort
hinter dem letzten Element CommandResponse in den folgenden Request an den
Fachdienst aufnehmen, bzw. nur das Element Abort falls kein Kommando
ausgeführt werden konnte. **[\<=]**

**VSDM-A_3009 - CCS-Schnittstelle: Reaktion auf Abort-Element - CLOSE Element**

Die CCS-Schnittstelle der Fachdienste MUSS bei Empfang einer Nachricht, die das
Element Abort enthält, im folgenden Response mit einem CLOSE-Element antworten. **[\<=]**





[Dokumentinformationen]: #dokumentinformationen
[Inhaltsverzeichnis]:    #inhaltsverzeichnis
[1]:                     #1-einordnung-des-dokuments
[1.1]:                   #11-zielsetzung
[1.2]:                   #12-zielgruppe
[1.3]:                   #13-geltungsbereich
[1.4]:                   #14-abgrenzung-des-dokuments
[1.5]:                   #15-bestandsschutz
[1.6]:                   #16-methodik
[2]:                     #2-allgemeine-festlegungen
[2.1]:                   #21-bezeichnung-der-request-elemente
[2.2]:                   #22-bezeichnung-der-response-elemente
[2.3]:                   #23-header-elemente
[2.4]:                   #24-visualisierung-der-xml-schemata
[3]:                     #3-update-flag-service
[3.1]:                   #31-operation-getupdateflags
[3.1.1]:                 #311-request
[3.1.2]:                 #312-request-header
[3.1.3]:                 #313-response
[3.2]:                   #32-fehlerbehandlung
[4]:                     #4-card-communication-service
[4.1]:                   #41-operation-performupdates
[4.1.1]:                 #411-request
[4.1.2]:                 #412-request-header
[4.1.3]:                 #413-response
[4.1.4]:                 #414-response-header
[4.2]:                   #42-operation-getnextcommandpackage
[4.2.1]:                 #421-request
[4.2.2]:                 #422-request-header
[4.2.3]:                 #423-response
[4.3]:                   #43-fehlerbehandlung
[5]:                     #5-kommandosequenzen-informativ
[5.1]:                   #51-ablauf
[5.2]:                   #52-kartenkommunikation
[6]:                     #6-anhang-a---verzeichnisse
[6.1]:                   #61-abkürzungen
[6.2]:                   #62-glossar
[6.3]:                   #63-abbildungsverzeichnis
[6.4]:                   #64-tabellenverzeichnis
[6.5]:                   #65-referenzierte-dokumente
[6.5.1]:                 #651-dokumente-der-gematik
[6.5.2]:                 #652-weitere-dokumente
[7]:                     #7-anhang-b---anforderungshaushalt
[7.1]:                   #71-eingangsanforderungen
[7.2]:                   #72-ausgangsanforderungen
[Abbildung-1]:           gemSpec_SST_FD_VSDM_V1.6.0.attachments/10137944713365387744.emf
[Abbildung-2]:           gemSpec_SST_FD_VSDM_V1.6.0.attachments/11912994526820556438.png
[Abbildung-3]:           gemSpec_SST_FD_VSDM_V1.6.0.attachments/14097059134549592343.png
[Abbildung-4]:           gemSpec_SST_FD_VSDM_V1.6.0.attachments/16515779820881092919.png
[Abbildung-5]:           gemSpec_SST_FD_VSDM_V1.6.0.attachments/2876690802949125868.png
[Abbildung-6]:           gemSpec_SST_FD_VSDM_V1.6.0.attachments/13921751001356595786.png
[Abbildung-7]:           gemSpec_SST_FD_VSDM_V1.6.0.attachments/9864174634026694722.png
[Abbildung-8]:           gemSpec_SST_FD_VSDM_V1.6.0.attachments/5705801334878283335.png
[Abbildung-9]:           gemSpec_SST_FD_VSDM_V1.6.0.attachments/10677090256036285044.png
[Abbildung-10]:          gemSpec_SST_FD_VSDM_V1.6.0.attachments/13076019558537773885.png
[Abbildung-11]:          gemSpec_SST_FD_VSDM_V1.6.0.attachments/10397295658720834343.png
[Abbildung-12]:          gemSpec_SST_FD_VSDM_V1.6.0.attachments/15653356867906002241.png
[Abbildung-13]:          gemSpec_SST_FD_VSDM_V1.6.0.attachments/12252038578525715915.png
[Abbildung-14]:          gemSpec_SST_FD_VSDM_V1.6.0.attachments/12142829197515919672.png
[Abbildung-15]:          gemSpec_SST_FD_VSDM_V1.6.0.attachments/7469689486126541172.png
[Abbildung-16]:          gemSpec_SST_FD_VSDM_V1.6.0.attachments/4134859043505118611.png
[Abbildung-17]:          gemSpec_SST_FD_VSDM_V1.6.0.attachments/7073713217169264199.png
[Abbildung-18]:          gemSpec_SST_FD_VSDM_V1.6.0.attachments/15549923772817802376.png
[Tbl-001]:               #Tbl-001 (&93834799934808)
[Tabelle-1]:             #Tabelle-1 (&93834775730000)
[Tabelle-2]:             #Tabelle-2 (&93834810734216)
[Tabelle-3]:             #Tabelle-3 (&93834810746656)
[Tabelle-4]:             #Tabelle-4 (&93834801638032)
[Tabelle-5]:             #Tabelle-5 (&93834801656344)
[Tabelle-6]:             #Tabelle-6 (&93834775091368)
[Tabelle-7]:             #Tabelle-7 (&93834775103632)
[Tabelle-8]:             #Tabelle-8 (&93834777021280)
[Tabelle-9]:             #Tabelle-9 (&93834777033544)
[Tabelle-10]:            #Tabelle-10 (&93834775754248)
[Tabelle-11]:            #Tabelle-11 (&93834775770248)
[Tabelle-12]:            #Tabelle-12 (&93834771057264)
[Tabelle-13]:            #Tabelle-13 (&93834771074832)
[Tabelle-14]:            #Tabelle-14 (&93834775029776)
[Tabelle-15]:            #Tabelle-15 (&93834775042640)
[Tabelle-16]:            #Tabelle-16 (&93834775060056)
[Tabelle-17]:            #Tabelle-17 (&93834810806728)
[Tabelle-18]:            #Tabelle-18 (&93834810839832)
[Tabelle-19]:            #Tabelle-19 (&93834801694408)
[Tabelle-20]:            #Tabelle-20 (&93834801706672)
[Tabelle-21]:            #Tabelle-21 (&93834801726112)
[Tabelle-22]:            #Tabelle-22 (&93834801741328)
[Tabelle-23]:            #Tabelle-23 (&93834780405568)
[Tabelle-24]:            #Tabelle-24 (&93834780422984)
[Tabelle-25]:            #Tabelle-25 (&93834780435328)
[Tabelle-26]:            #Tabelle-26 (&93834780447592)
[Tabelle-27]:            #Tabelle-27 (&93834780461424)
[Tabelle-28]:            #Tabelle-28 (&93834767992128)
[Tabelle-29]:            #Tabelle-29 (&93834768008432)
[Tabelle-30]:            #Tabelle-30 (&93834768022176)
[Tabelle-31]:            #Tabelle-31 (&93834768038872)
[Tabelle-32]:            #Tabelle-32 (&93834781671368)
[Tabelle-33]:            #Tabelle-33 (&93834781687280)
[Tabelle-34]:            #Tabelle-34 (&93834783649456)
[Tabelle-35]:            #Tabelle-35 (&93834783665872)
[Tabelle-36]:            #Tabelle-36 (&93834781703224)
[Tabelle-37]:            #Tabelle-37 (&93834781715488)
[Tabelle-38]:            #Tabelle-38 (&93834801525456)
[Tabelle-39]:            #Tabelle-39 (&93834801537896)
[Tabelle-40]:            #Tabelle-40 (&93834801555760)
[Tabelle-41]:            #Tabelle-41 (&93834801569400)
[Tabelle-42]:            #Tabelle-42 (&93834801582440)
[Tabelle-43]:            #Tabelle-43 (&93834774923464)
[Tabelle-44]:            #Tabelle-44 (&93834799228408)
[Tabelle-45]:            #Tabelle-45 (&93834798979232)
[Tabelle-46]:            #Tabelle-46 (&93834764450304)
[Tabelle-47]:            #Tabelle-47 (&93834764492488)
[Tabelle-48]:            #Tabelle-48 (&93834798402624)
[Tabelle-49]:            #Tabelle-49 (&93834798416992)
[Tabelle-50]:            #Tabelle-50 (&93834798431376)
[Tabelle-51]:            #Tabelle-51 (&93834798453856)
[Tabelle-52]:            #Tabelle-52 (&93834798476216)
[Tabelle-53]:            #Tabelle-53 (&93834777621784)
[Tabelle-54]:            #Tabelle-54 (&93834772247856)
[Tbl-056]:               #Tbl-056 (&93834772290072)
[Tbl-057]:               #Tbl-057 (&93834783491104)
[Tbl-058]:               #Tbl-058 (&93834783507968)
[Tabelle-55]:            #Tabelle-55 (&93834783525288)
