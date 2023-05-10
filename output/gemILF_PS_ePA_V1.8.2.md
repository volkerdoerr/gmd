
Elektronische Gesundheitskarte und Telematikinfrastruktur

### Abbildung 1: ILF_ePA_Element_Context

- Klassifizierung: öffentlich
- Referenzierung: gemILF_PS_ePA
- Revision: 548770
- Stand: 30.09.2021
- Status: freigegeben
- Version: 1.8.2

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
Einarbeitung P 18.1

</td><td>
gematik

</td></tr><tr><td>
1.2.0

</td><td>
28.06.19

</td><td>
Einarbeitung P 19.1

</td><td>
gematik

</td></tr><tr><td>
1.3.0

</td><td>
02.10.19

</td><td>
Einarbeitung P 20.1/2

</td><td>
gematik

</td></tr><tr><td>
1.4.0

</td><td>
02.03.20

</td><td>
Einarbeitung P 21.1

</td><td>
gematik

</td></tr><tr><td>
1.5.0

</td><td>
30.06.20

</td><td>
Anpassungen gemäß Änderungsliste P22.1 und Scope-Themen aus Systemdesign
R4.0.0 

</td><td>
gematik

</td></tr><tr><td>
1.6.0

</td><td>
12.10.20

</td><td>
Einarbeitung P22.2

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
Einarbeitung ePA_Maintenance_21.1

</td><td>
gematik

</td></tr><tr><td>
1.8.1

</td><td>
09.07.21

</td><td>
Einarbeitung ePA_Maintenance_21.2

</td><td>
gematik

</td></tr><tr><td>
1.8.2

</td><td>
30.09.21

</td><td>
Einarbeitung ePA_Maintenance_21.3

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
  - [2.1] Relevante Integrationsprofile
- [3] Systemkontext
  - [3.1] Akteure und Rollen
  - [3.2] Nachbarsysteme
- [4] Übergreifende Festlegungen
  - [4.1] Webservice-Kommunikation
  - [4.2] Dienstverzeichnisdienst
  - [4.3] Ereignisdienst
  - [4.4] Zugriffssteuerung
    - [4.4.1] Aufrufkontext
    - [4.4.2] RecordIdentifier
    - [4.4.3] Status Aktenzugriff
- [5] Funktionsmerkmale
  - [5.1] ePA-Administration
    - [5.1.1] Aktenanbieter ermitteln
      - [5.1.1.1] Schnittstelle
      - [5.1.1.2] Umsetzung
      - [5.1.1.3] Nutzung
    - [5.1.2] Aktenkonto aktivieren
      - [5.1.2.1] Schnittstelle
      - [5.1.2.2] Umsetzung
      - [5.1.2.3] Nutzung
    - [5.1.3] Ad-hoc-Berechtigung erteilen
      - [5.1.3.1] Schnittstelle
      - [5.1.3.2] Umsetzung
      - [5.1.3.3] Nutzung
  - [5.2] Dokumentenmanagement
    - [5.2.1] Dokumente einstellen
      - [5.2.1.1] Schnittstelle
      - [5.2.1.2] Umsetzung
      - [5.2.1.3] Nutzung
    - [5.2.2] Dokumente suchen
      - [5.2.2.1] Schnittstelle
      - [5.2.2.2] Umsetzung
      - [5.2.2.3] Nutzung
    - [5.2.3] Dokumente laden
      - [5.2.3.1] Schnittstelle
      - [5.2.3.2] Umsetzung
      - [5.2.3.3] Nutzung
    - [5.2.4] Dokumente löschen
      - [5.2.4.1] Schnittstelle
      - [5.2.4.2] Umsetzung
      - [5.2.4.3] Nutzung
    - [5.2.5] Artefakte
      - [5.2.5.1] Namensräume
      - [5.2.5.2] WSDLs und Schemata
    - [5.2.6] Testunterstützung
  - [5.3] Protokolle und Benachrichtigungen
    - [5.3.1] Benachrichtigungen erhalten
      - [5.3.1.1] Info-Quelle ePA-Administration
      - [5.3.1.2] Info-Quelle Berechtigungs-Abfrage
      - [5.3.1.3] Info-Quelle Dokumentensuche
      - [5.3.1.4] Info-Quelle Systeminformationsdienst
      - [5.3.1.5] Info-Quelle Fehlermeldung
      - [5.3.1.6] Umsetzung
      - [5.3.1.7] Nutzung
    - [5.3.2] Übertragungsprotokolle speichern
  - [5.4] Status- und Fehlermeldungen
    - [5.4.1] Statusinformationen
    - [5.4.2] Fehlerbehandlung
      - [5.4.2.1] TelematikError
      - [5.4.2.2] IHE-Error
    - [5.4.3] Handlungs-Empfehlungen in Fehlerfällen
    - [5.4.4] Übersicht möglicher Fehlermeldungen
      - [5.4.4.1] Fehlermeldungen aus dem Fachmodul ePA
      - [5.4.4.2] Fehlermeldungen aus dem Aktensystem ePA
- [6] Informationsmodell
  - [6.1] Metadaten
  - [6.2] Selbstauskunft
  - [6.3] Wertebereiche
  - [6.4] Dokumentenformate der ePA
    - [6.4.1] ContentProfile Notfalldatensatz und Datensatz Persönliche Erklärungen
    - [6.4.2] ContentProfile elektronischer Medikationsplan
    - [6.4.3] ContentProfile Arztbrief nach § 291f
    - [6.4.4] Strukturierte Dokumente
      - [6.4.4.1] Signatur für strukturierte Dokumentenformate der ePA
- [7] Ergänzende Funktionalitäten
  - [7.1] Empfehlung zur Archivierung
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

Die vorliegende Spezifikation definiert Anforderungen zu Erstellung, Test und
Betrieb derjenigen Anteile eines Primärsystems, die zur Nutzung der
elektronischen Patientenakte erforderlich sind. Die gematik erstellt auch in
Hinsicht auf die ePA eine Bestätigung über die Konformität des
Primärsystems zur Konnektorschnittstelle aus. Bei Umsetzung der Anforderungen
dieses Dokumentes erfüllt der PS-Hersteller die Anforderungen des
Bestätigungsverfahrens.

Die Anforderungen des Dokumentes sind für Primärsystemhersteller, die keine
Bestätigung auf Konformität der Konnektorschnittstelle durch die gematik
benötigen informativ.

Technische Standards werden in der ePA verwendet,um Interoperabilität zu
steigern und die technischen Voraussetzungen zur Nutzung der Anwendung zu
legen. Auf Seiten der Primärsystemhersteller eröffnet die Verwendung von
Standards die Chance, wiederverwendbare Schnittstellen zu entwickeln bzw. zu
nutzen und einzelne Module austauschbar zu gestalten.

Zum Zweck der Implementierungshilfe werden grundlegende Konzepte und
Anwendungsfälle der ePA aus der Sicht der PS-Hersteller erläutert. Dabei
werden nicht nur Anwendungsfälle der ePA erläutert, sondern auch praktische
Umsetzungshinweise sowie Beispiele gegeben. 

### 1.2 Zielgruppe

Das Dokument ist maßgeblich für Hersteller von Primärsystemen, welche die
Fachmodul-ePA-Schnittstelle des Konnektors nutzen.

Falls ein Primärsystem bisher das technische Framework von IHE noch nicht
verwendet, wird es durch diesen Implementierungsleitfaden in die Lage versetzt,
die ePA-Schnittstellen IHE-konform zu verwenden.

Falls ein Primärsystem das technische Framework von IHE bereits verwendet,
schildert der Implementierungsleitfaden ihm die relevanten Einschränkungen des
IHE-Frameworks, die für die ePA der Telematikinfrastruktur von Relevanz sind.
Die IHE-Konformität dieser Schnittstellen ermöglicht ihm die Anbindung
weiterer Gegenstandsbereiche.

### 1.3 Geltungsbereich

Dieses Dokument enthält normative Festlegungen zur Telematikinfrastruktur des
deutschen Gesundheitswesens. Der Gültigkeitszeitraum der vorliegenden Version
und deren Anwendung in Bestätigungs- Zulassungs- oder Abnahmeverfahren wird
durch die gematik GmbH in gesonderten Dokumenten (z.B. Dokumentenlandkarte,
Produkttypsteckbrief, Leistungsbeschreibung) fest­gelegt und bekannt gegeben.

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

Benutzte Schnittstellen werden in der Spezifikation desjenigen Produkttypen
normativ beschrieben, der diese Schnittstelle bereitstellt. Auf die
entsprechenden Dokumente wird referenziert (siehe auch Anhang 8.5).

Nicht Bestandteil des vorliegenden Dokumentes sind:

 ---> UL

Die ePA fungiert als Sekundärdokumentation von Daten der Versicherten. Die
Primärdokumentation der Versichertendaten im PS wird nur insoweit
thematisiert, wie es für die Anbindung der ePA an das PS erforderlich ist.

### 1.5 Methodik

Anforderungen als Ausdruck normativer Festlegungen werden durch eine eindeutige
ID sowie die dem RFC 2119 [RFC2119] entsprechenden, in Großbuchstaben
geschriebenen deutschen Schlüsselworte MUSS, DARF NICHT, SOLL, SOLL NICHT,
KANN gekennzeichnet.

Anforderungen werden im Dokument wie folgt dargestellt:\<AFO-ID\> - \<Titel der
Afo\>Text / Beschreibung [\<=]

Dabei umfasst die Anforderung sämtliche zwischen Afo-ID und Textmarke
[\<=] angeführten Inhalte.

### 2 Systemüberblick

Einem Leistungserbringer als Nutzer seines Primärsystems bietet ein
ePA-fähiger Konnektor den Zugang zur elektronischen Patientenakte des
gesetzlich Versicherten an. Leistungserbringer und Primärsystem greifen in der
ConsumerZone der TI primär auf die lokalen bzw. dezentralen TI-Komponenten der
LE-Institution zu. Zugriffe auf elektronische Patientenakten erfolgen
ausschließlich gekapselt über den Konnektor.

Zu diesem Zweck nutzt das Primärsystem IHE-Schnittstellen, die das Fachmodul
ePA des Konnektors bereitstellt.  Eine Übersicht über die Fachanwendung ePA
im Ganzen liefert [gemSysL_ePA]. Einen Überblick über die ePA-Profilierung
des Frameworks von IHE (Integrating the Healthcare Enterprise) liefert
[gemSpec_Dokumentenverwaltung].

Wenn von der "Akte" im Folgenden gesprochen wird, ist die ePA als Sekundärakte
des Versicherten gemeint, nicht die "Primärakte" für den Versicherten im
Primärsystem. Mit "Aktenanbieter" ist im Folgenden immer der Anbieter des
ePA-Aktensystems gemeint.

### 2.1 Relevante Integrationsprofile

Für das aktennutzende PS sind mehrere IHE-Integrationsprofile für das
Primärsystem relevant:

<table><tr><th>
Kürzel

</th><th>
Dokument

</th><th>
Transaktion

</th></tr><tr><td>
[ITI-41]

</td><td>
[ITI TF-2b#3.41]

</td><td>
Provide and Register Document Set-b

</td></tr><tr><td>
[ITI-18]

</td><td>
[ITI TF-

2a#3

.18]

</td><td>
Registry Stored Query

</td></tr><tr><td>
[ITI-43]

</td><td>
[ITI TF-2b#3.43]

</td><td>
Retrieve Document Set

</td></tr><tr><td>
[ITI-62]

</td><td>
[IHE-ITI-RMD]

</td><td>
Remove Metadata

</td></tr></table>

### 3 Systemkontext

Die Nutzer der Primärsysteme der Leistungserbringer teilen sich die technische
Infrastruktur der ePA in der Telematikinfrastruktur, folgen dabei den hier
geschilderten Regeln der TI und bilden in diesem Sinne eine IHE-Affinity
Domain, um ePA-Daten gesteuert durch die Berechtigungsvergabe des
Versicherten auszutauschen. Dieser Datenaustausch erfolgt in vielerlei
Hinsicht gemäß Festlegungen von IHE.

Die technische Infrastruktur der ePA besteht beim Leistungserbringer vor allem
aus dem Konnektor mit dem Fachmodul ePA, welches die Kommunikation mit dem
ePA-Aktensystem ermöglicht.  Mit dem Konnektor stehen auch die Komponenten
der Basis-TI, die zentrale TI und der Fach- und Basisdienste der TI zur
Verfügung, deren Nutzung durch das PS in [gemILF_PS], [gemILF_PS_NFDM]
und [gemILF_PS_AMTS] beschrieben sind.

### 3.1 Akteure und Rollen

Leistungserbringer agieren in zwei ePA-Szenarien: 

 ---> UL

Das PS tritt somit in der Consumer Zone der TI sowohl als Document Consumer als
auch als Document Source auf, beim Löschen auch als Document Administrator.

Gemäß [gemILF_PS#3.1.3]  können Heilberufler ihren SM-B selbst nutzen oder
ihre Gehilfen im Allgemeinen dafür autorisieren, auf die Anwendungen der eGK
mit ebendiesen Rechten zuzugreifen. Dies gilt für das SM-B der
TI-Rollenprofile 2, 3, 4 (SM-B Leistungserbringer). Eine Ausnahme hierzu bilden
ausschließlich die Gehilfen der nichtärztlichen Psychotherapeuten. Das PS
darf die berufsmäßigen Gehilfen der nichtärztlichen Psychotherapeuten nicht
mit denjenigen Zugriffsberechtigungen auf die ePA ausstatten, über die
der nichtärztliche Psychotherapeut verfügt. 

Die Versicherten agieren in der Rolle des Akteninhabers und in der Rolle des
Vertreters des Akteninhabers. 

### 3.2 Nachbarsysteme

Leistungserbringer erhalten über ihr ePA-fähiges Primärsystem Zugriff auf die
ePA des Versicherten ausschließlich über den Konnektor. Der Konnektor macht
zusätzlich die zentralen und dezentralen Komponenten der TI für das PS
zugänglich, für Details siehe die Übersicht in [gemKPT_Arch_TIP]. Weitere
Nachbarsysteme oder an das PS angebundene Softwaremodule werden in diesem
Dokument nicht betrachtet.

Das vorliegende Dokument bezieht sich mit den referenzierten
Konnektorschnittstellen auf den Leistungsumfang der ePA-Komponenten, die in der
dazugehörigen Dokumentenlandkarte aufgelistet sind. Die hier beschriebene
Funktionalität wird als ePA Stufe 2 (und höher) beschrieben, um zu
kennzeichnen, dass die vorliegenden Primärsystemschnittstellen der ePA einige
nur beschränkt abwärtskompatible Änderungen zur ePA-Stufe 1 enthält. Das
betrifft insbesondere die Erteilung von Berechtigungen. In ePA 1 erstellte
Berechtigungen werden vom Aktensystem in Berechtigungen für ePA 2
transformiert. ePA 2 - Berechtigungen können jedoch nicht in ePA 1 -
Berechtigungen zurück transformiert werden. Das Upgrade von ePA 1 auf ePA 2
kann nicht rückgängig gemacht werden. In einer früheren Version des
vorliegenden Dokumentes ist die Nutzung der ePA Stufe 1 beschrieben, zuletzt
für das Release 3.1.3.

Das Upgrade des Primärsystems auf Stufe 2 ist abhängig von der Verfügbarkeit
des ePA 2 - Konnektorfachmoduls im Konnektor des Leistungserbringers. Falls der
PS-Hersteller die Verfügbarkeit des Konnektor PTV5 (mit der ePA 2 -
Funktionalität) bei den Leistungserbringern nicht durchgängig sicher stellen
kann, kann es für das Ausrollen des ePA 2 - Primärsystems erforderlich sein,
die Schnittstellenversion des Konnektors über den Dienstverzeichnisdienst zu
ermitteln und die Inbetriebnahme des ePA 2 - Upgrades vom Vorliegen der
passenden Schnittstellenversion im Dienstverzeichnisdienst abhängig zu
machen (PHRService V2.x und PHRServiceManagement V2.x sind erreichbar). Dieses
Feature ("Dualmode" des Primärsystems) unterstützt die Migration von ePA 1
nach ePA2 und darf nicht dazu verwendet werden zwischen den Interfaces von ePA
1 und ePA 2 beliebig zu wechseln. Dies würde dazu führen, dass bei manchen
PS-Installation ePA 1 genutzt wird, bei anderen ePA 2, je nach Version des
Konnektors in der konkreten LE-Institution. Dieser "Dualmode" erlaubt
PS-Herstellern ein einheitliches Release-Management für unterschiedliche
Praxiskonstellationen im Migrationszeitraum der ePA Stufe 1 auf die ePA Stufe
2. 

### 4 Übergreifende Festlegungen

Das Primärsystem verarbeitet die primäre Behandlungsdokumentation der
Versicherten. Die ePA ist ein potentiell lebenslanger Speicherort für eine
sekundäre Behandlungsdokumentation der Versicherten.

Die Anbindung und Nutzung dezentraler TI-Komponenten, die in [gemILF_PS]
beschrieben wird, ermöglicht unter anderem den Aufbau von Kartensitzungen, die
an verschiedenen Stellen vorausgesetzt werden, insbesondere zur Nutzung der eGK
des Versicherten.

Das Fachmodul ePA wird vom Konnektor ab Produkttyp Version 4 (PTV4) zur
Verfügung gestellt.

Die Inbetriebnahme des Konnektors in die LE-Umgebung [gemILF_PS#4.1] und die
Unterstützung des VSDM durch das PS für eine Gültigkeitsprüfung der
eGK [gemILF_PS#4.3] MUSS erfolgt sein, um die ePA nutzen zu können.

Für die Anwendungsfälle der ePA MUSS eine SM-B in PS und Konnektor verwaltet
werden und freigeschaltet sein [gemILF_PS#4.2.3]. Das PIN-Handling von eGK und
SM-B wird in [gemILF_PS#4.1.5] beschrieben. 

Das PS muss eine Arbeitsplatz-Konfiguration in der LE-Institution ermöglichen,
in der Versicherte auf ein Kartenterminal zugreifen können, in dem sie ihre
eGK freischalten können. Dazu gehört ein KT, dessen PIN-Pad dem Versicherten
zur Eingabe seiner PIN.CH zugänglich ist. Die Konfiguration eines
Arbeitsplatzes, an dem ein Kartenterminal für den Versicherten zur
PIN-Eingabe zugänglich ist, insbesondere am Empfangstresen, wird in
[gemILF_PS#9.1] beschrieben. 

### 4.1 Webservice-Kommunikation

Die Webservice-Konnektorschnittstellen werden nachrichtenbasiert
angesprochen über

 ---> UL

Die Bildung der SOAP-Nachrichten durch das Primärsystem wird in diesem Dokument
technologie-neutral geschildert. Dabei werden die Voraussetzungen für
unterschiedliche Strategien zur Nachrichtenerzeugung geliefert, darunter:

 ---> UL

Die ePA nutzt bei bestimmten Operationen den SOAP-Header, um Informationen über
Aufruf- und Aktenkontext zu erhalten (s. Kap. 4.4).

**A_14510 - Setzen erforderlicher Parameter im SOAP-Header**

Das PS MUSS Parameter im SOAP-Header setzen, wenn diese in der jeweiligen
Signatur der Operation gefordert sind. **[\<=]**

**A_14511 - Leere oder fehlende SOAP-Header im Falle fehlender Parametern**

Das PS KANN einen leeren SOAP-Header an den Konnektor senden oder eine Nachricht
ohne SOAP-Header versenden, wenn keine SOAP-Header-Parameter in der jeweiligen
Signatur der Operation gefordert sind. **[\<=]**

**A_15569 - Verwendung von Byte Order Mark in SOAP-Nachrichten**

Das PS KANN einen UTF-8 Unicode Byte Order Mark (BOM) gemäß
[BasicProfile1.2#3.1.2] setzen. **[\<=]**

**A_15570 - Content-Type und Charset im http-Header**

Das PS MUSS abweichend von R1012 in [BasicProfile1.2] und [BasicProfile2.0]
ausschließlich das Character Encoding UTF-8 in der Nachricht benutzen und das
charset im http-Header auf UTF-8 setzen. Beispiel einer korrekten Angabe im
http-Header: Content-Type: text/xml; charset=utf-8. **[\<=]**

### 4.2 Dienstverzeichnisdienst

**A_15573 - Nutzung DVD zur Ermittlung der Webservice-Endpunkte der ePA am
Konnektor**

Das PS MUSS ausschließlich den Dienstverzeichnisdienst des Konnektors nutzen,
um die Webservice-Endpunkte für die ePA-Dienste des Fachmoduls zu ermitteln.
Die URL des Webservice-Endpunktes, die aus WSDL-Abfragen wieGET
/ws/CertificateService?wsdl ermittelt werden kann, ist nicht zu verwenden.
**[\<=]**

Das PS soll auch mit Konnektoren kompatibel sein, die eine Produkttypversion
kleiner als PTV4 nutzen. Der PS-Hersteller kann es erreichen, dass sein
Primärsystem mit Konnektoren unterschiedlicher Produkttypversion zusammen
arbeitet, um darauf vorbereitet zu sein, dass seine Kunden Konnektoren älterer
Produkttypversionen (kleiner PTV4) nutzen, indem er die Versionsinformationen
des Dienstverzeichnisdienstes beachtet:

 ---> UL

Es kann vorkommen, dass PS und Konnektor vom selben Webservice unterschiedliche
Dienstversionsnummern unterstützen. Der Umgang mit Abweichungen zwischen
produktiven PS und Konnektor in Bezug auf unterstützte Dienstversionen wird in
[gemILF_PS#4.1.2] beschrieben. 

### 4.3 Ereignisdienst

Falls das PS den Eventservice des Konnektors abonniert, kann es
Komfortfunktionen der Kartenverwaltung wie Benachrichtigungen über gesteckte
und gezogene Karten und Informationen über den Betriebszustand des Konnektors
nutzen.

**A_15577 - Abonnierung von Ereignissen**

Das PS SOLL Benachrichtigung über Konnektor-Ereignisse gemäß
[gemILF_PS#4.1.4] Eventservice abonnieren, insbesondereFM_EPA/POLICY_LEI (Kap.
5.4.1) undFM_EPA/ ACTIVATE_ACCOUNT/START(Kap. 5.1.2). **[\<=]**

### 4.4 Zugriffssteuerung

Der ePA-Client übergibt je nach Signatur der Operation eines ePA-Webservices
Informationen über

 ---> OL

Viele Funktionsmerkmale erfordern die Kenntnis des Status der
Zugriffsberechtigung auf die ePA eines Versicherten, um

 ---> UL

**A_14413 - Primärdokumentation als Voraussetzung der ePA als
Sekundärdokumentation**

Das PS MUSS für einen Versicherten Daten in seiner Primärdokumentation
verwalten, falls er für ihn Funktionsmerkmale des ePA-Dokumentenmanagements
zur Sekundärdokumentation nutzen will, und dort folgende Informationen
hinterlegen können: RecordIdentifier inklusive Versicherten-ID (Die
Versicherten-ID ist der 10-stellige unveränderliche Teil der 30-stelligen
Krankenversicherungsnummer), Status Zugriffsberechtigung. **[\<=]**

### 4.4.1 Aufrufkontext

Das Bilden des Aufrufkontextes erfolgt wie schon im PTV1-Konnektor. Die nur für
den HBA verwendete User-ID muss im Rahmen der ePA nicht gesetzt werden, da der
Zugriff auf die ePA mittels HBA in den Stufen 1 und 1.1 nicht möglich ist. 

![Abbildung-1][Abbildung-1]

Der Konnektor ermittelt unter Verwendung von Konfigurationsdaten am Konnektor
und der Context-Informationen die zur Laufzeit verfügbaren SM-Bs, die für den
Aktenzugriff vom Konnektor herangezogen werden können. Voraussetzung für die
Nutzung vieler Funktionsmerkmale ist daher das Vorliegen mindestens einer
freigeschalteten SM-B.

Beispiel#: Bsp_ILF_ePA_Context 

<table><tr><th>
         \<m0:Context\>

             \<m1:MandantId\>m0001\</m1:MandantId\>

             \<m1:ClientSystemId\>csid0001\</m1:ClientSystemId\>

             \<m1:WorkplaceId\>wpid007\</m1:WorkplaceId\>

         \</m0:Context\>

</th></tr></table>

**A_14442 - Freischaltung von SM-Bs garantieren**

Das PS MUSS mindestens einmal täglich den Sicherheitszustand aller SM-Bs
prüfen, die in der LE-Institution verfügbar sind. Im Falle nicht
freigeschalteter SM-Bs MUSS das PS den Nutzer auffordern, die Freischaltung
der SM-Bs durchzuführen. **[\<=]**

Die Liste der gesteckten SM-Bs liefert der Systeminformationsdienst (siehe
[gemILF_PS#4.1.4]). Der erhöhte Sicherheitszustand bzw. die Freischaltung
einer SM-B ist mittelsGetPinStatusam Rückgabewertverifiederkennbar (siehe
[gemILF_PS#4.1.5.4]).

Eine Eins-zu-Eins-Beziehung zwischen MandantID und TelematikID wird von der
gematik nicht anwendungsübergreifend festgeschrieben. Für die Anwendung ePA
ist die 1:1-Beziehung zwischen MandantID und TelematikID jedoch fachlich
erforderlich.Das PS kann die 1:1-Beziehung zwischen MandantID und TelematikID
technisch verifzieren, indem es (Schritt 1) potentiell mehrere
SMC-B-Cardhandles der für die ePA im Kontext verwendeten MandantID ermittelt,
(Schritt 2) für jede dieser CardHandle per ReadCardCertificate aus der SMC-B
das C.HCI.AUT – Zertifikat ausliest, die Telematik-ID extrahiert und (Schritt
3) eine Fehlermeldung anzeigt, falls die ermittelten TelematikIDs pro MandantID
nicht identisch sind.

### 4.4.2 RecordIdentifier

Für die ePA eines Versicherten werden identifizierende Merkmale in
unterschiedlicher Form verwendet:

<table><tr><th>
Datentyp

</th><th>
Bestandteile

</th><th>
Format

</th><th>
Beschreibung

</th></tr><tr><td rowspan="2">
RecordIdentifier

</td><td>
InsurantId

</td><td>
 Strukturierter Datentyp, s. Abb_ILF_ePA_RecordIdentifier mit der
Versicherten-ID als @extension in Verbindung mit der OID für KVNRs als @root

</td><td>
Kennung des Versicherten, eindeutig über alle verfügbaren
Aktensysteme (Verwendung im Kontext der ePA-Administration)

</td></tr><tr><td>
HomeCommunityId

</td><td>
String, gebildet als OID mit 64 Zeichen nach [IHE-ITI-TF3#4.2.3.2.12]
[gemSpec_DM_ePA#2.1.4.6]

</td><td>
Kennung des Aktenanbieters, eindeutig über alle verfügbaren Aktensysteme

</td></tr><tr><td colspan="2">
patientID

</td><td>
String, gebildet aus Versicherten-ID und ihrer OID gemäß
[gemSpec_DM_ePA#2.1.4.5]

</td><td>
Kennung des Versicherten, eindeutig über alle verfügbaren Aktensysteme
(Verwendung im Kontext der Dokumentenverwaltung)

</td></tr></table>

An den Konnektor-Schnittstellen werden jeweils entweder derRecordIdentifieroder
seine Bestandteile verwendet.

![Abbildung-2][Abbildung-2]

**A_15640 - Transformationen InsurantId und patientId**

Das PS MUSS in der Lage sein, aus derVersicherten-IDgemäß
[gemSpec_DM_ePA#2.1.4.5] eineInsurantIdund einepatientIdzu erzeugen, sowie die
inhaltsgleichen InsurantIdund patientIdwechselseitig ineinander zu
transformieren.  **[\<=]**

### 4.4.3 Status Aktenzugriff

Die LEI wird vom Primärsystem darin unterstützt, die Metadaten für die
Aktenzugriffe mit möglichst wenig Pflegeaufwand zu befüllen, und zwar
insbesondere durch die

 ---> UL

Der lokal hinterlegbare Status des Aktenzugriffs umfasst für einzelne
Versicherte in Tab_ILF_ePA_Zugriffsberechtigungsstatus pro RecordIdentifier
aufgeführte Informationen. Kap. 5.4.1 (Benachrichtigungen verwalten)
beschreibt, wie sich diese Informationen akkumulieren und aktualisieren lassen.

<table><tr><th>
Information pro RecordIdentifier

</th><th>
Wert

</th><th>
Quellen für Aktualisierungen

</th></tr><tr><td>
Kennung des Versicherten (Versicherten-ID)

</td><td>
RecordIdentifier/InsurantId/@extension

</td><td>
 ---> UL

</td></tr><tr><td>
Kennung des Aktenanbieters

</td><td>
HomeCommunityId

</td><td>
Anwendungsfall

Aktenanbieter ermitteln

</td></tr><tr><td>
Vorliegen der Berechtigung, auf seine Akte zuzugreifen;

Ablaufdatum Zugriffsberechtigung

</td><td>
ExpirationDate

: Datum, an dem die Zugriffsberechtigung abläuft

</td><td>
Anwendungsfälle:

 ---> UL

</td></tr><tr><td>
Dokumentenliste

</td><td>
 ---> UL

</td><td>
Anwendungsfälle Kapitel 5.2.6, 5.3.1

</td></tr><tr><td>
Zugriffsberechtigung

(Typ der Dokumente im Zugriff)

</td><td>
Einer der Werte der Tabelle Tab_ILF_ePA_Zugriffsberechtigungen)

</td><td>
Anwendungsfälle Kapitel 5.1.3

</td></tr></table>

Die LEI erhält Zugriff auf ePA-Dokumente je nach erteilter Kombination von
Zugriffsberechtigungen. Folgende einander ergänzende Zugriffsberechtigungen
sind in der ePA möglich:

<table><tr><th>
Technischer Identifier Zugriffsberechtigung

</th><th>
Anmerkung

</th></tr><tr><td>
DocumentCategory:

Liste von Identifiern für Dokumentenkategorien gemäß
[gemSpec_DM_ePA#Tab_DM_Dokumentenkategorien]

</td><td>
LEI erhält Zugriffsrecht auf alle aufgelisteten Dokumentenkategorien, soweit
es der Festlegung in der AuthorizationConfidentiality, sowie den
Zugriffsunterbindungsregeln aus A_19303 nicht widerspricht.

</td></tr><tr><td>
AuthorizationConfidentiality="N"

</td><td>
LEI erhält "Einfaches Zugriffsrecht", auf: Dokumente vom Typ
CondidentialityCode normal,  falls es nicht den Zugriffsunterbindungsregeln
aus A_19303 nicht widerspricht.

</td></tr><tr><td>
AuthorizationConfidentiality="R"

</td><td>
LEI erhält "Erweitertes Zugriffsrecht", auf: Dokumente vom Typ
CondidentialityCode normal und restricted,  falls es nicht den
Zugriffsunterbindungsregeln aus A_19303 nicht widerspricht. Die umfasst auch
durch ihn selbst später in der Vertraulichkeitsstufe restricted
("vertraulich") eingestellte Dokumente. 

</td></tr></table>

### 5 Funktionsmerkmale

Das Aktenkonto eines Versicherten kann sowohl beim LE, als auch am ePA-Frontend
des Versicherten aktiviert werden (Kap. 5.2.1).

Das PS nutzt die Berechtigungsverwaltung des ePA-Aktensystems über seine
Schnittstellen zum Fachmodul ePA.

Leistungserbringerinstitutionen haben zwei Möglichkeiten, vom Versicherten
eine Berechtigung zum Aktenzugriff zu erhalten:

 ---> OL

Die Berechtigung kann sowohl vom Versicherten selbst stammen, als auch vom
Vertreter des Versicherten. Sie ist auf Leistungserbringer (inkl. deren
berufsmäßigen Gehilfen oder zur Vorbereitung auf den Beruf Tätige, jedoch
nicht die Gehilfen der nichtärztlichen Psychotherapeuten) eingeschränkt, s.
[gemSpec_PKI#Tab_PKI_254 Zugriffsprofile für eine Rollenauthentisierung] und
[gemKPT_Arch_TIP#Tabelle Zugriffsberechtigter Personenkreis (PK) nach §291a
SGB V].

Die Laufzeit von Zugriffsberechtigungen ist begrenzt. Falls eine
Zugriffsberechtigung aufgrund in der Vergangenheit liegendemexpirationDateoder
Berechtigungsentzug am ePA-Frontend des Versicherten nicht mehr existiert, ist
eine erneute Berechtigungsvergabe erforderlich, s. [gemSysL_ePA#2.5.2]. 

Im Falle vorliegender Berechtigung kann das PS denRecordIdentifierdes
Versicherten ermitteln (Kap. 5.1.5).

Für ein bereits aktiviertes Aktenkonto kann sich eine Kombination der
Anwendungsfälle bis hin zu einem lesenden Aktenzugriff beispielhaft
folgendermaßen darstellen:

![Abbildung-3][Abbildung-3]

In technische Abläufe wird der Versicherte oder sein Vertreter über die
PIN-Eingabe integriert.

<table><tr><th>
Obligatorische Beteiligung des Versicherten oder seines Vertreters (eGK-Nutzung
erforderlich)

</th><th>
Fakultative Beteiligung des Versicherten oder seines Vertreters (keine
eGK-Nutzung)

</th></tr><tr><td>
Aktenkonto aktivieren

 (Kap. 5.1.2) (Nur durch den Versicherten, nicht durch den Vertreter)

</td><td>
Aktenanbieter

der Versicherten

ermitteln

(Kap. 5.1.1)

</td></tr><tr><td>
Ad-hoc-Berechtigung erteilen

(Kap. 5.1.3)

</td><td>
Management von Dokumenten: 

 ---> UL

</td></tr><tr><td>
Benachrichtigungen über Änderungen innerhalb einer Akte erhalten

(Kap. 5.3.1) 

</td></tr></table>

Der Vertreter hat seine Vertretungsberechtigung am ePA-Frontend des Versicherten
erhalten, wo auch die eGK des Vertreters der ePA des Vertretenen bekannt
gemacht wurde. Im Gegensatz dazu benutzt der gesetzlich bevollmächtigte
Vertreter die eGK desjenigen, den er vertritt.

Falls ein Vertreter das Aktenkonto aktivieren möchte, kann er dies nur dann
tun, falls er ein gesetzlich bevollmächtigter Vertreter ist, der über eGK und
PIN des Versicherten verfügt, den er vertritt. Für das Aktivieren des
Aktenkontos kann der Vertreter seine eigene eGK nicht verwenden, anders als
beim Erteilen der Ad-hoc-Berechtigung

Für die Durchführung der Aktenkonto-Aktivierung oder der Erteilung der
Ad-hoc-Berechtigung durch einen gesetzlich bevollmächtigten Vertreter ist
keine darüber hinaus gehende zusätzliche Implementierung am PS erforderlich.

Das komplette Berechtigungskonzept inklusive der Berechtigungsverwaltung am
ePA-Frontend des Versicherten liefert [gemSysL_ePA#3.6].

**A_15090 - Protokollierung Dokumententransfer im Übertragungsprotokoll**

Jeder Dokumententransfer (Dokumente einstellen, laden, löschen) MUSS im
Übertragungsprotokoll vermerkt werden. **[\<=]**

### 5.1 ePA-Administration

Das Aktenmanagement der Leistungserbringer (PHRManagementService) erfolgt
weitgehend über das Fachmodul ePA und dort gekapselte Funktionalitäten.

<table><tr><th>
Name

</th><th colspan="2">
PHRManagementService [gemSpec_FM_ePA

#7.2

]

</th></tr><tr><td>
Version

</td><td colspan="2">
2.0

</td></tr><tr><td>
Namensraum

</td><td colspan="2">
http://ws.gematik.de/conn/WSDL/PHRManagementService/v2.0

</td></tr><tr><td>
Abkürzung Namensraum

</td><td colspan="2">
phr_management

</td></tr><tr><td rowspan="4">
Operationen

</td><td>
Name

</td><td>
Implementierungshinweise

</td></tr><tr><td>
GetHomeCommunityID

</td><td>
[gemSpec_FM_ePA#7.2.1.4]

</td></tr><tr><td>
ActivateAccount

</td><td>
[gemSpec_FM_ePA#7.2.1.1]

</td></tr><tr><td>
RequestFacilityAuthorization

</td><td>
[gemSpec_FM_ePA#7.2.1.2] 

</td></tr><tr><td>
WSDL

</td><td>
PHRManagementService.wsdl

</td></tr><tr><td>
XML-Schema

</td><td>
PHRManagementService.xsd

</td></tr></table>

InActivateAccountund RequestFacilityAuthorizationwerden eGK und SM-B im
freigeschaltetem Zustand verwendet, inGetHomeCommunityIDnur die SM-B. 

### 5.1.1 Aktenanbieter ermitteln

Frau Gundlach ist Patientin bei Herrn Dr. Weber und teilt ihm bei einem
vergangenen Arzttermin mit, dass sie seit kurzem ein Aktenkonto bei einem ePA -
Provider eingerichtet hat. Dr. Weber ermittelt daraufhin dessen Identifier
über eine Funktion seines Primärsystems, und speichert den Identifier des
Aktenanbieters von Frau Gundlach daraufhin persistent in der
Primärdokumentation des Primärsystems ab. 

Zur Ermittlung der HomeCommunityID des Versicherten wird die
Operation GetHomeCommunityID desPHRManagementService genutzt.

Für die Nutzung der ePA durch das Primärsystem ist das Vorliegen eines
Identifikators für das Aktenkonto des Versicherten (RecordIdentifier)
erforderlich. 

Fachliche Grundlage der Aktenzuordnung ist die Versicherten-ID des Versicherten.
Jeder Versicherte hat zur selben Zeit nur ein einzelnes Aktenkonto.
Unterschiedliche Versicherte können bei jeweils unterschiedlichen
Aktenanbietern ihre Patientenakte hosten lassen. Die Abfrage der verschiedenen
möglichen Anbieter übernimmt das Fachmodul für das PS.
Die HomeCommunityId kann pro Versicherten über das Fachmodul ePA ermittelt
werden. 

Jeder Versicherte verfügt über genau eine aktive Akte, auch während er ggf.
den Aktenanbieter wechselt.

Wenn die Aktenzuordnung für einen Vertreter durchgeführt wird, muss der
Vertreter der LEI hinreichend genau mitteilen, für welchen Versicherten er
vertretungsberechtigt ist, damit für den Vertretenen der Aktenanbieter
ermittelt werden kann. Aufgrund der vom Vertreter mitgeteilten
Patientenidentifikationsmerkmale ermittelt die LEI die betroffene Primärakte
und ermittelt den Aktenanbieter aus dieser Primärakte heraus. Durch das
Starten des Anwendungsfalles aus dem Aktenkonto desjenigen heraus, der
vertreten wird, wird dessenKVNRalsInsurantIDverwendet. Die Ermittlung
desjenigen, der vertreten wird, kann nicht über die eGK des Vertreters
erfolgen und muss vielmehr im Dialog mit dem Vertreter durchgeführt werden.

**A_15581 - Anwendungsfall Aktenanbieter ermitteln**

Das PS MUSS es dem Leistungserbringer ermöglichen, für einen Versicherten,
über dessen Versicherten-ID er in der Primärdokumentation seines PS verfügt,
mittelsGetHomeCommunityID dieHomeCommunityId des Aktenanbieters zu ermitteln.
**[\<=]**

Das Resultat vonAktenanbieter ermitteln,die HomeCommunityId, wird als Teil
des RecordIdentifiersverwendet, sowie separat als Wert bestimmter
Metadatenfelder. Aufgrund der vielfachen Verwendung ist eine persistente
Speicherung in der Primärdokumentation des Versicherten erforderlich. 

### 5.1.1.1 Schnittstelle

**A_15582 - Identifikation des Versicherten mittels Versicherten-ID**

Das PS MUSS die Versicherten-ID benutzen, um den Versicherten in seiner
Primärdokumentation seiner ePA durch Bildung eines RecordIdentifiers
zuzuordnen.  **[\<=]**

<table><tr><th>
Operationsname

</th><th colspan="2">
GetHomeCommunityID [gemSpec_FM_ePA#7.2.1.1]

</th></tr><tr><td rowspan="3">
Aufrufparameter

</td><td>
Name

</td><td>
Implementierung

</td></tr><tr><td>
Context

</td><td>
 Aufrufkontext gemäß [ConnectorContext.xsd], s. [gemILF_PS#3.3.1]

</td></tr><tr><td>
InsurantID 

</td><td>
InsurantIdType

, s. Kap. 4.4.2

</td></tr><tr><td rowspan="3">
Rückgabeparameter

</td><td>
Name

</td><td>
Implementierung

</td></tr><tr><td>
Status

</td><td>
Status nach [gemSpec_Kon#3.5.2] zur Information im PS

</td></tr><tr><td>
HomeCommunityId

</td><td>
Anbieterkennung gemäß [gemSpec_DM_ePA#2.1.4.7]

</td></tr></table>

![Abbildung-4][Abbildung-4]

![Abbildung-5][Abbildung-5]

### 5.1.1.2 Umsetzung

Die Aktivitäten des AnwendungsfallesAktenanbieter ermittelnsind:

Vorbedingung:

 ---> UL

Auslöser:

 ---> UL

Aktivitäten:

 ---> UL

Resultat:

 ---> UL

### 5.1.1.3 Nutzung

Das erfolgreiche Ermitteln einer HomeCommunityId ist kein Beleg für das
Vorliegen einer Zugriffsberechtigung auf die Akte des Versicherten. Daher ist
die Nutzung der OperationGetHomeCommunityID vor allem im Kontext der
Ad-hoc-Berechtigung sinnvoll, oder nach einer Kenntnisnahme davon,
dass Leistungserbringer eine Berechtigung über das ePA-Frontend des
Versicherten erhalten haben. 

Beispiel#: Bsp_ILF_ePA_Request_getHomeCommunityID

<table><tr><th>
\<?xml version="1.0" encoding="UTF-8"?\>  
\<SOAP-ENV:Envelope
xmlns:m1="http://ws.gematik.de/conn/ConnectorCommon/v5.0"
xmlns:m0="http://ws.gematik.de/conn/ConnectorContext/v2.0"
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:SOAP-ENC="http://www.w3.org/2003/05/soap-encoding"
xmlns:SOAP-ENV="http://www.w3.org/2003/05/soap-envelope"\> 

\<SOAP-ENV:Header\>  
 \<Action SOAP-ENV:mustunderstand="true"
xmlns="http://www.w3.org/2005/08/addressing"\>http://ws.gematik.de/conn/phrs/PHRManagementService/v1.3/GetHomeCommunityID\</Action\>
 
 \<To SOAP-ENV:mustunderstand="1"
xmlns="http://www.w3.org/2005/08/addressing"\>http://10.11.218.161:80/fm/phrmanagementservice\</To\>
 
 \<MessageID SOAP-ENV:mustunderstand="true"
xmlns="http://www.w3.org/2005/08/addressing"\>5d3f0445-1c9c-4c0f-a246-57816bc99cab\</MessageID\>
 
 \<ReplyTo SOAP-ENV:mustunderstand="1"
xmlns="http://www.w3.org/2005/08/addressing"\>  
 
\<Address\>http://www.w3.org/2005/08/addressing/anonymous\</Address\> 

 \</ReplyTo\>  
\</SOAP-ENV:Header\>  
\<SOAP-ENV:Body\> 

 \<m:GetHomeCommunityID
xmlns:m="http://ws.gematik.de/conn/phrs/PHRManagementService/v1.3"\>  
  
\<m0:Context\>  
     \<m1:MandantId\>Mandant1\</m1:MandantId\>  
   
 \<m1:ClientSystemId\>ClientID1\</m1:ClientSystemId\>  
   
 \<m1:WorkplaceId\>CATS\</m1:WorkplaceId\>  
   \</m0:Context\>  
 
\<m:InsurantID extension="X110411319" root="1.2.276.0.76.4.8"/\> 

 \</m:GetHomeCommunityID\>  
\</SOAP-ENV:Body\>  
\</SOAP-ENV:Envelope\>

</th></tr></table>

Wenn das Primärsystem durch eine VSDM-Prüfung von einem Wechsel der
Haupt-IK-Nummer an den Daten des Versicherten informiert wird, soll im Falle
einer bestehenden Zugriffsberechtigung auf eine Akte der
Operation GetHomeCommunityID aufgerufen werden, da ein Wechsel des
Aktenanbieters nicht unwahrscheinlich ist.

**A_14660 - Eingeschränkte Speicherung der HomeCommunityId**

Das PS SOLL die HomeCommunityId nur im Falle festgestellter
Zugriffsberechtigungen in die Primärdokumentation des Versicherten
speichern: 

 ---> UL

**[\<=]**

### 5.1.2 Aktenkonto aktivieren

Frau Gundlach hat bei einem Aktenanbieter einen Vertrag über die Nutzung einer
elektronischen Patientenakte abgeschlossen. Sie bittet Dr. Weber darum, für
sie das Aktenkonto zu aktivieren. Dr. Weber ermittelt den Aktenanbieter von
Frau Gundlachdurch Aufruf einer entsprechenden Funktion im PVS und aktiviert
dort für Sie ihre Akte. Dabei gibt Frau Weber die PIN ihrer eGK ein.

Zur Umsetzung des "Schritt 2 - Aktivierung in der Umgebung des
Leistungserbringers" im Anwendungsfall Aktenkonto einrichtenaus
[gemSysL_ePA#3.5.1, UC 2.1 - Aktenkonto einrichten, Schritt 2 - Aktivierung in
der Umgebung des Leistungserbringers] wird die
OperationActivateAccountdesPHRManagementService genutzt.

**A_14191 - Anwendungsfall Aktivierung Aktenkonto des Versicherten**

Das PS MUSS es dem Leistungserbringer ermöglichen,
mittelsActivateAccountdas Aktenkonto des Versicherten zu aktivieren. **[\<=]**

Das Aktivieren des Aktenkontos wird entweder vom PS-Nutzer über das
Userinterface aktiv gestartet oder es wird implizit aus anderen
Anwendungsfällen heraus gestartet, in denen das Fachmodul am Status der Akte
erkennt, dass die Akte eines Versicherten noch zu aktivieren ist. Das implizite
Starten des Anwendungsfalles führt ebenso wie das vom PS angestoßene Starten
des Aktenkonto-Aktivierens zu einer Interaktion des Versicherten mit dem
Kartenterminal, worüber das PS durch das Event FM_EPA/
ACTIVATE_ACCOUNT/STARTinformiert wird.

### 5.1.2.1 Schnittstelle

Durch seine PIN bestätigt der Versicherte seine Einwilligung dazu, das
Aktenkonto in der in den Vertragsunterlagen ausgewählten Konfiguration zu
aktivieren.

<table><tr><th>
Operationsname

</th><th colspan="2">
ActivateAccount [gemSpec_FM_ePA#7.2.1.1]

</th></tr><tr><td rowspan="4">
Aufrufparameter

</td><td>
Name

</td><td>
Implementierung

</td></tr><tr><td>
Context

</td><td>
 Aufrufkontext gemäß [ConnectorContext.xsd], s. [gemILF_PS#3.3.1]

</td></tr><tr><td>
EhcHandle

</td><td>
Aufbau einer Kartensitzung gemäß [gemILF_PS#4.2] ergibt 

CardHandle

der eGK des Versicherten

</td></tr><tr><td>
RecordIdentifier

</td><td>
RecordIdentifier gemäß [gemSpec_DM_ePA#3.1.2], s. Kapitel 5.1.1

</td></tr><tr><td rowspan="2">
Rückgabeparameter

</td><td>
Name

</td><td>
Implementierung

</td></tr><tr><td>
Status

</td><td>
Status nach [gemSpec_Kon#3.5.2] zur Information im PS

</td></tr></table>

![Abbildung-6][Abbildung-6]

### 5.1.2.2 Umsetzung

Die Aktivitäten des AnwendungsfallesAktenkonto aktivierensind:

Vorbedingung:

 ---> UL

Auslöser:

 ---> UL

Aktivitäten:

 ---> UL

Resultat:

 ---> UL

### 5.1.2.3 Nutzung

**A_17204 - Informieren aufgrund Event FM_EPA/ ACTIVATE_ACCOUNT/START**

Das PS MUSS bei Erhalt der EventsFM_EPA/ ACTIVATE_ACCOUNT/STARTeine Information
an den Nutzer des PS weiterleiten, dass der Versicherte aktuell mit dem
Anwendungsfall beschäftigt ist, das Aktenkonto zu aktivieren. **[\<=]**

Der Versicherte kann so vom Nutzer des PS darauf aufmerksam gemacht werden, dass
der Versicherte am Kartenterminal dazu aufgefordert wird, seine PIN einzugeben.

Der Anwendungsfall startet mit der Information des Versicherten, die
Aktenaktivierung bereits vorbereitet zu haben, mit einem expliziten Auslösen
über das Userinterface des Primärsystems.

Das implizite Aktivieren startet die Aktenkontoaktivierung beispielsweise beim
Erteilen einer Ad-hoc-Berechtigung, sofern das Aktenkonto sich in dem Zustand
befindet, die ausstehende Aktivierung durchführen zu können. Dabei wird das
Event FM_EPA/ ACTIVATE_ACCOUNT/STARTausgelöst.

Wenn die Aktivierung des Aktenkontos erfolgreich beendet wurde und sich das
Aktenkonto des Versicherten im aktivierten Zustand befindet, löst das
ePA-Fachmodul das EventFM_EPA/ ACTIVATE_ACCOUNT/FINISHEDaus, das für eine
Erfolgsmeldung am Primärsystem genutzt werden kann, um den Versicherten über
den Erfolg des Anwendungsfalles zu unterrichten.

### 5.1.3 Ad-hoc-Berechtigung erteilen

Frau Gundlach möchte Herrn Dr. Weber und seiner Hausarztpraxis Zugriff auf ihre
ePA erteilen. Im Gespräch mit der . Medizinischen Fachangestellte (MFA) von
Dr. Weber am Empfangstresen, Frau Kunze, wird besprochen, dass der Zugriff auf
alle normalen von Leistungserbringern eingestellte Dokumente erfolgen soll,
nicht aber auf die vertraulichen Dokumente von Frau Gundlach. Sie überreicht
ihre eGK Frau Kunze. Frau Kunze wählt die besprochene Option am PS. Frau
Kunze fordert die Ad-hoc-Berechtigung am PS an und dreht das Kartenterminal
mit dem Eingabefeld für die PIN-Eingabe zu Frau Weber. Auf dem Display des
Kartenterminals sieht Frau Weber die Aufforderung zur PIN-Eingabe für die
Ad-hoc-Berechtigung mit den abgesprochenen Optionen, sowie Dauer der
Gültigkeit der Zugriffsberechtigung für die Arztpraxis Dr. Weber. Das PS am
Empfangstresen fügt der lokalen Primärdokumentation von Frau Gundlach ein
ePA-Kennzeichen als Markierung einer bestehenden Zugriffsberechtigung hinzu. 

Zur Umsetzung des AnwendungsfallesAd-hoc-Berechtigung durch einen
Leistungserbringer anfordernaus [gemSysL_ePA#3.6.7, UC 3.7 -
Ad-hoc-Berechtigung durch einen Leistungserbringer anfordern] wird die
Operation RequestFacilityAuthorization desPHRManagementService verwendet.

**A_14200-05 - Anwendungsfall Ad-hoc-Berechtigung erteilen**

Das PS MUSS es Leistungserbringern ermöglichen,
mittelsRequestFacilityAuthorization vom Versicherten oder seinem Vertreter
eine Ad-hoc-Zugriffsberechtigung auf seine Akte erteilen zu lassen. Dabei wird
die Art des gewährten Zugriffs in der AuthorizationConfiguration angegeben,
sowie die Dauer der Zugriffsberechtigung im ExpirationDate(heute+6 Tage als
Defaultwert).DieAuthorizationConfigurationenthält die vom Versicherten
getroffene Festlegung zu folgenden Auswahlmöglichkeiten
(AuthorizationConfidentiality): a) Vertraulichkeitsstufenormaloder vertraulich
(restricted), b) die Auflistung der DokumentenkategorienDocumentCategorygemäß
[gemSpec_DM#Tab_DM_Dokumentenkategorien], auf die eine Berechtigung erteilt
wird. **[\<=]**

Die Vertraulichkeitsstufe vertraulich (restricted) betrifft Dokumente, die der
Versicherte an seinem FdV als vertraulich gekennzeichnet hat, sowie Dokumente,
die von Leistungserbringern auf Wunsch des Versicherten als vertraulich
eingestellt wurden. Falls eine Freigabe auf Dokumente der
Vertraulichkeitsstuferestricted erfolgt, ist damit eine Freigabe auf Dokumente
der Vertraulichkeitsstufenormalverbunden.

**A_19408 - Auswahlmöglichkeit AuthorizationConfiguration.DocumentCategory**

Das PS MUSS ihren Nutzern geeignete Auswahlmöglichkeiten bieten, um die
Optionen der AuthorizationConfiguration.DocumentCategoryauszuwählen,
insbesondere die Kombination der mit dem Versicherten besprochenen
Dokumentenkategorien gemäß [gemSpec_DM#Tab_DM_Dokumentenkategorien], für die
eine Freigabe erfolgt. Das Primärsystem MUSS dem Leistungserbringer je nach
dem Sektor, in dem er arbeitet, einen konfigurierbaren Defaultwert anbieten,
der die Summe aller Kategorien umfasst, die ihm die Zugriffsunterbindungsregeln
erlauben. Die Summe der für den Sektor des Primärsystems möglichen
Zugriffsrechte ist aus der Tabelle [gemSpec_Dokumentenverwaltung#Tab_Dokv_030 -
Zugriffsunterbindungsregeln] abzuleiten.  **[\<=]**

**A_19497 - Auswahlmöglichkeit
AuthorizationConfiguration.AuthorizationConfidentiality**

Das PS MUSS dem LE eine Auswahl an Optionen anzubieten, die dem Wunsch des
Versicherten entsprechen, eine
ZugriffsberechtigungAuthorizationConfigurationaus der Tabelle
Tab_ILF_ePA_Zugriffsberechtigungen zu erteilen. Eine leere Auswahl ist nicht
zulässig. Erfolgt keine anders lautende Auswahl, MUSS das PS
fürAuthorizationConfiguration.AuthorizationConfidentialityden Default-Wertnormalsetzen.
Das PS MUSS die ausgewählte Kombination aus Zugriffsberechtigungen im
ElementAuthorizationConfigurationsetzen.   **[\<=]**

**A_19498 - Speicherung RecordIdentifier in der lokalen Primärdokumentation des
PS**

Das PS MUSS den RecordIdentifier an der lokalen Patientenakte
(Primärdokumentation) persistent speichern, falls die Ad-hoc-Autorisierung
erfolgreich verlaufen ist. Zusätzlich MUSS
die RequestFacilityAuthorization.AuthorizationConfigurationgespeichert werden,
um für denselben Versicherten bei der nächsten Adhoc-Autorisierung dem
Versicherten die Option anbieten zu können, dieselben Optionen wie beim
letzten Mal zu setzen.  **[\<=]**

Am Aktensystem werden Zugriffe auf Dokumente unterbunden, die nicht den
gesetzlich festgelegten berufsgruppenspezifischen Regeln entsprechen. Manche
Berufsgruppen verfügen nur über eingeschränkte Zugriffsrechte auf bestimmte
Typen von Dokumenten. Die Auswahl von Dokumentenkategorien durch den
Versicherten kann diese Zugriffsmöglichkeiten weiter einschränken, nicht
jedoch über die gesetzlich festgelegten Rahmenbedingungen hinaus erweitern.

**A_19386 - Respektieren der berufsgruppenspezifischen
Zugriffsunterbindungsregeln**

Das PS MUSS die in [gemSpec_Dokumentenverwaltung#Tab_Dokv -
Zugriffsunterbindungsregeln] aufgeführten Zugriffsunterbindungsregeln
beachten, um nicht unnötige Fehlermeldungen zu provozieren. Das PS darf nur
solche Dokumentenkategorien zur Auswahl bringen, die der Berufsgruppe der SMC-B
entsprechen, die für die Ad-hoc-Berechtigung verwendet wird.  **[\<=]**

Über die OperationReadCardCertificatekann das PS  die Berufsgruppederjenigen
SMC-B ermitteln, die für die ePA-Zugriffe benutzt wird. Im
Authentisierungszertifikat C.AUTbefindet
sich die Berufsgruppe ProfessionOID in der ZertifikatsExtensionAdmission,
s. [gemSpec_PKI#Anhang A]. 

Die Rolle des Versicherten kann teilweise auch vom Vertreter übernommen werden.
In diesem Fall übergibt der Vertreter seine eigene eGK, um eine
Ad-hoc-Berechtigung für den Versicherten zu erstellen, für den die Vertretung
wahrgenommen wird (identifiziert durch dessen RecordIdentifier, aufgerufen aus
der PS-Dokumentation des Vertretenen). 

Durch das Starten des Anwendungsfalles aus dem Aktenkonto desjenigen heraus, der
vertreten wird, wird dessenRecordIdentifierverwendet. Die Ermittlung
desjenigen, der vertreten wird, kann nicht über die eGK des Vertreters
erfolgen und muss vielmehr im Dialog mit dem Vertreter durchgeführt werden.
 Falls für den Vertreter die Vertretungsrechte nicht (mehr) vorliegen
sollten, scheitert der Anwendungsfall Ad-hoc-Berechtigung durch den Vertreter
erteilen. Dabei wird der Fehler 7209 (Keine Berechtigung für das Aktenkonto
vorhanden) geworfen. 

### 5.1.3.1 Schnittstelle

<table><tr><th>
Operationsname

</th><th colspan="2">
RequestFacilityAuthorization [gemSpec_FM_ePA#7.2.1.1]

</th></tr><tr><td rowspan="7">
Aufrufparameter

</td><td>
Name

</td><td>
Implementierung

</td></tr><tr><td>
Context

</td><td>
Aufrufkontext gemäß [ConnectorContext.xsd], s. [gemILF_PS#3.3.1]

</td></tr><tr><td>
EhcHandle

</td><td>
Aufbau einer Kartensitzung gemäß [gemILF_PS#4.2] ergibt 

CardHandle

der eGK des Versicherten oder seines Vertreters

</td></tr><tr><td>
AuthorizationConfiguration

</td><td>
Art und Gültigkeitsendedatum des Zugriffs, den der Versicherte auf seine Akte
gewährt.  

</td></tr><tr><td>
RecordIdentifier

</td><td>
RecordIdentifier mit den Elementen 

InsurantId 

und

HomeCommunityID

</td></tr><tr><td>
OrganizationName

</td><td>
Name der LE-Organisation gemäß Selbstbeschreibung Kap.
6.2, Tab_ILF_ePA_Datenfelder_Selbstauskunft für die Anzeige am Kartenterminal

</td></tr><tr><td>
InsurantName

</td><td>
Vor- und Nachname aus der Primärakte des Versicherten, für den eine
Berechtigung erteilt wird, für die Anzeige am Kartenterminal.

</td></tr><tr><td rowspan="2">
Rückgabeparameter

</td><td>
Name

</td><td>
Implementierung

</td></tr><tr><td>
Status

</td><td>
Status nach [gemSpec_Kon#3.5.2] zur Information im PS

</td></tr></table>

![Abbildung-7][Abbildung-7]

Der EingabeparameterAuthorizationConfiguration beschreibt 

 ---> UL

**A_15633-06 - Setzen des Elementes ExpirationDate**

Das PS MUSS dem LE eine Konfigurationsauswahl gemäß Tabelle
Tab_ILF_ePA_Zugriffsberechtigungs-Endedatum anbieten, in der ein Versicherter
bestimmt, wie lange er dem LE eine Zugriffsberechtigung erteilt. Außerdem
MUSS zusätzlich eine flexible Festlegung möglich sein. Erfolgt keine
Festlegung, gilt der Default-Wert. Für die erteilte Berechtigung setzt das PS
ein Zugriffsberechtigungs-Endedatum im ElementExpirationDateaufgrund der 
Berechnung des Datums des letzten Datums ab heute, zu dem die
Zugriffsberechtigung noch besteht. 

Tabelle10: Tab_ILF_ePA_Zugriffsberechtigungs-Endedatum

<table><tr><th>
Werte zur Auswahl

</th><th>
Erläuterung der Berechnung des ExpirationDate

</th><th>
Default-Wert

</th></tr><tr><td>
1 Tag

</td><td>
ExpirationDate = heutiges Datum

</td></tr><tr><td>
7 Tage

</td><td>
ExpirationDate = heutiges Datum + 6 Kalendertage

</td><td>
ja

</td></tr><tr><td>
18 Monate

</td><td>
ExpirationDate = heutiges Datum + 18 Kalendermonate

</td></tr><tr><td>
flexibel

</td><td>
ExpirationDate =  beliebiges Datum (heutiges Datum bis 100 Jahre)

</td></tr><tr><td>
unbefristet

</td><td>
ExpirationDate =  31.12.9999

</td></tr></table>

**[\<=]**

Der Versicherte oder ein von ihm berechtigter Vertreter stimmt der Berechtigung
auf Aktenzugriff durch PIN-Eingabe am Kartenterminal, in dem die eGK (des
Versicherten bzw. des Vertreters) steckt, zu.

### 5.1.3.2 Umsetzung

Das Primärsystem nutzt beim Erteilen einer Ad-hoc-Berechtigung die Festlegungen
zur Vertraulichkeitsstufe (AuthorizationConfidentiality) und die
kategoriebasierte Berechtigung (DocumentCategoryList). Dokumentenspezifische
Berechtigungen, d.h. Zugriffsberechtigungen, die sich auf einzelne ausgewählte
Dokumente beziehen, können am PS nicht gesetzt werden.
Dokumentenspezifische Berechtigungen erteilen kann nur der Versicherte an
seinem Frontend.

Falls schon eine Berechtigung vorliegt, wird diese durch die Operation
überschrieben.

Die Aktivitäten des AnwendungsfallesAd-hoc-Berechtigung erteilensind:

Vorbedingung:

 ---> UL

Auslöser:

 ---> UL

Aktivitäten:

 ---> UL

Resultat:

 ---> UL

![Abbildung-8][Abbildung-8]

### 5.1.3.3 Nutzung

**A_14517 - Speicherung RecordIdentifier in der lokalen Primärdokumentation des
PS**

Das PS MUSS den RecordIdentifier an der lokalen Patientenakte
(Primärdokumentation) persistent speichern, falls die Ad-hoc-Autorisierung
erfolgreich verlaufen ist. Zusätzlich MUSS das
Zugriffsberechtigungs-EndedatumExpirationDateaus RequestFacilityAuthorization.AuthorizationConfiguration.ExpirationDateals
Ablaufdatum der Zugriffsberechtigung in der Primärakte des Versicherten
gespeichert werden.  **[\<=]**

Die Ad-hoc-Berechtigung ermöglicht eine Abfrage der Metadaten der ePA-Dokumente
und das Anlegen eines lokalen Metadaten-Index für die Dokumente, auf die
prinzipiell Zugriffsrechte bestehen, als Vorbereitung von
Dokumentenmanagement-Zugriffen. 

### 5.2 Dokumentenmanagement

Der Konnektor bietet dem PS mit dem DienstDocumentRepositoryeine
Dokumentenverwaltung auf  Basis einer Profilierung der IHE-Spezifikationen
rund um das KernprofilXDS.b(Cross-Enterprise Document Sharing) an.

<table><tr><th>
Name

</th><th colspan="2">
PHRService [gemSpec_FM_ePA#7.1]

</th></tr><tr><td>
Version

</td><td colspan="2">
2.0.1

</td></tr><tr><td>
SOAP-Header

</td><td colspan="2">
![Img-009][Img-009]

</td></tr><tr><td>
Namensraum

</td><td colspan="2">
urn:ihe:iti:xds-b:2007 

</td></tr><tr><td>
Abkürzung Namensraum

</td><td colspan="2">
ihe

</td></tr><tr><td rowspan="5">
Operationen

</td><td>
Name

</td><td>
Implementierungshinweise

</td></tr><tr><td>
DocumentRepository_ProvideAndRegisterDocumentSet-b

</td><td>
Profilierung von [ITI-41], s. Kap. 5.2.1

</td></tr><tr><td>
DocumentRegistry_RegistryStoredQuery  

</td><td>
Profilierung von [ITI-18], s. Kap. 5.2.2

</td></tr><tr><td>
DocumentRepository_RetrieveDocumentSet

</td><td>
Profilierung von [ITI-43], s. Kap. 5.2.3

</td></tr><tr><td>
DocumentRegistry_RemoveMetadata 

</td><td>
Profilierung von [ITI-62], s. Kap. 5.2.5

</td></tr><tr><td>
WSDL

</td><td colspan="2">
gemäß:

 ---> UL

</td></tr><tr><td>
XML-Schema

</td><td colspan="2">
PHRService.xsd

</td></tr></table>

<table><tr><th colspan="2">
Profilierungen des Kernprofiles XDS.b

</th></tr><tr><td>
Anwendungsfall

</td><td>
IHE-Schnittstelle

</td></tr><tr><td>
Dokumente einstellen

</td><td>
DocumentRepository_ProvideAndRegisterDocumentSet-b  [ITI-41]

</td></tr><tr><td>
Dokumente suchen

</td><td>
Registry Stored Query [ITI-18]

</td></tr><tr><td>
Dokumente laden

</td><td>
Retrieve Document Set [ITI-43]

</td></tr><tr><td>
Dokument löschen (auch in Ordnern)

</td><td>
Remove Metadata [ITI-62] 

</td></tr></table>

<table><tr><th>
Einschränkungen von XDS.b im Rahmen der IHE-Profilierung

</th><th>
Referenz

</th></tr><tr><td>
Kein asynchrones Kommunikationsmuster

</td><td>
nicht umgesetzt: [ITI TF-1#10.2.5]

</td></tr><tr><td>
Beschränkung der Dokumentenformate je nach Ausbaustufe

</td><td>
Kap.  6.3, [gemSpec_DM_ePA#A_14760]

</td></tr><tr><td>
Beschränkung auf RPLC (replace) analog zu Document Replacement Option

</td><td>
[gemSpec_Dokumentenverwaltung#A_14941]

</td></tr></table>

**A_14418 - MTOM-Pflicht bei [ITI-41]**

Das PS MUSS bei der Umsetzung der IHE XDS-Transaktion [ITI-41] zur Übertragung
von Dokumenten eine Kodierung mittels MTOM/XOP [MTOM]
gemäß [IHE-ITI-TF2x#V.3.6.] verwenden.  **[\<=]**

**A_15084 - SOAP-Header nach [SOAP 1.2]**

Das PS MUSS in der Dokumentenverwaltung die SOAP-Nachricht konform zu [SOAP
1.2] bilden.  **[\<=]**

Die Anwendungsfälle des Dokumentenmanagements der Akte erfordern, dass der
Nutzer die Berechtigung hat, auf mindestens eine SM-B zuzugreifen, die für die
LE-Institution vorliegt und dass eine durch eine Telematik-ID identifizierte
Institution oder ein durch eine Telematik-ID identifizierter Teil einer
Institution eine Berechtigung erhalten hat. Um diese Berechtigung durchzusetzen
ist eine Konfiguration am Konnektor administrativ zu pflegen und vom PS zu
nutzen.

Drei Elemente des Aufrufkontextes eines SOAP-Clients geben bei einem Zugriff des
Dokumentenmanagements im SOAP-Header darüber Auskunft, von welchem
Clientsystem-Arbeitsplatz ein Aufruf auf welche Akte erfolgt: 

<table><tr><th>
Name SOAP-Header-Element 

</th><th>
Quelle

</th><th>
optional, falls Defaultwert genutzt wird

</th></tr><tr><td>
MandantID

</td><td>
Context/MandantId

</td><td>
ja

</td></tr><tr><td>
ClientSystemID

</td><td>
Context/ClientSystemId

</td><td>
ja

</td></tr><tr><td>
WorkplaceID

</td><td>
Context/WorkplaceId

</td><td>
ja

</td></tr><tr><td>
RecordIdentifier 

</td><td>
RecordIdentifier

</td><td>
nein

</td></tr></table>

Die interne Mandantenverwaltung des PS SOLL auf die WS-Kommunikation der ePA
über die Nutzung derMandantIDabgebildet werden. DieMandantIDsteht für die
Kennung der PS-Mandanten. Die Konfiguration von PS-Mandanten, SM-Bs und
Arbeitsplätzen wird in [gemILF_PS] geschildert, die Konfiguration für
größere LE-Institutionen mit mehreren SM-Bs oder Mandanten in Kapitel 3.3.3.

Der Nutzer ist durch die lokale Mandantenverwaltung seines Primärsystems
berechtigt auf die Primärdokumentation des Versicherten zuzugreifen und wird
durch die Konfiguration der Mandantenverwaltung im Konnektor derjenigen SM-B
zugeordnet, die er für den Zugriff auf die Akte benötigt. 

In der Administrationsoberfläche des Konnektors wird gemäß
[gemSpec_Kon#10.3.1.1] im Informationsmodell der LE-Institution die
Default-SM-B der Arbeitsplätze, Clientsysteme und Kartenterminals für den
Zugriff auf die ePA konfiguriert. Für die Administration des
Default-Aufrufkontextes s. [gemSpec_FM_ePA#6.4]. 

Ad-hoc-Berechtigung erteilen ist nicht davon abhängig, ob für eine LEI eine
oder mehrere SM-Bs im Verzeichnisdienst eingepflegt sind. Falls mehrere 
SM-Bs in einer LEI verwendet werden, sind die unterschiedlichen
Primärsystem-Arbeitsplätze erst dann zugriffsberechtigt, wenn der
Aufrufkontext oder der Default-Aufrufkontext SMC-Bs mit derjenigen Telematik-ID
zugeordnet sind, für die eine Berechtigung erteilt wurde.

**A_14475 - SOAP-Header-Clientparameter bei gesamthaft berechtigten
LE-Institutionen**

Falls der LE-Institution nur eine einzelne Telematik-ID zugeordnet ist, KANN
das PS die in Tab_ILF_ePA_ClientInformationen aufgeführten Parameter des
SOAP-Headers in jedem Zugriff des Dokumentenmanagements verwenden. **[\<=]**

Wenn der Parameter nicht gesetzt wird, verwendet das Fachmodul ePA den in der
Konnektorkonfiguration hinterlegten Default-Wert.

**A_14476 - SOAP-Header-Clientparameter bei unterschiedlich berechtigten Teilen
von LE-Institutionen**

Falls der LE-Institution mehrere Telematik-ID zugeordnet sind, MUSS das PS die
in Tab_ILF_ePA_ClientInformationen aufgeführten Parameter des SOAP-Headers in
jedem Zugriff des Dokumentenmanagements verwenden. **[\<=]**

**A_14698 - Einstellen von Zugriffsinformationen in Metadaten**

Für die Weiterverarbeitung auf Dokumentenebene MÜSSEN Zugriffsinformationen
gemäß Tab_ILF_ePA_Zugriffsinformation_Werte zusätzlich in die Metadaten der
Dokumentenmanagement-Zugriffe eingestellt werden:

Tabelle15: Tab_ILF_ePA_Zugriffsinformation_Werte

<table><tr><th>
Zugriffsinformationen

</th><th>
IHE-Schnittstellen

</th><th>
Wertgleiches Request-Attribut

</th></tr><tr><td rowspan="3">
InsurantId 

</td><td>
[ITI-41], [ITI-18]

</td><td>
XDSSubmissionSet.patientID

</td></tr><tr><td>
[ITI-41], [ITI-18]

</td><td>
XDSDocumentEntry.patientID

</td></tr><tr><td>
[ITI-41], [ITI-18]

</td><td>
XDSDocumentEntry.sourcePatientId

</td></tr><tr><td rowspan="3">
HomeCommunityID

</td><td>
[ITI-43]

</td><td>
XDSDocumentEntry.repositoryUniqueID

</td></tr><tr><td>
[ITI-43]

</td><td>
XDSDocumentEntry.HomeCommunityID

</td></tr><tr><td>
[ITI-86]

</td><td>
DocumentRequest.RepositoryUniqueID

</td></tr></table>

**[\<=]**

Das Ersetzen eines Dokumentes ist als Kombination mehrerer Anwendungsfälle
umzusetzen: Nach dem Ermitteln (Suchen, Kap. 5.2.2) und Löschen des zu
ersetzenden Dokumentes (Kap. 5.2.5) nach Rücksprache mit dem Versicherten wird
das ersetzende Dokument (als "Original"-Dokument, s. A_14250) in die ePA
eingestellt (Kap. 5.2.1).

### 5.2.1 Dokumente einstellen

Herr Dr. Weber hatte für Frau Gundlach vor einigen Monaten einen
Notfalldatensatz auf ihre eGK geschrieben. Dr. Weber bespricht mit Frau
Gundlach, ihren Notfalldatensatz auch in ihre ePA einzustellen. Frau Gundlach
erteilt eine Ad-hoc-Berechtigung für diesen Zugriff. Bei Auswahl der
entsprechenden Funktion nutzt Dr. Weber die Möglichkeit, die Metadaten zu
kontrollieren, mit denen der Notfalldatensatz automatisch für die Akte von
Frau Gundlach konnotiert werden. Dr. Weber nimmt kurz Notiz von der
Bestätigungsmeldung über den Erfolg des Einstellens.

**A_15653 - Funktionsmerkmal Dokumente Einstellen**

Das PS MUSS es dem Leistungserbringer ermöglichen, ePA-Dokumente in die Akte
eines Versicherten einstellen zu können. Dafür MUSS das PS die
Konnektorschnittstellenoperation ProvideAndRegisterDocumentSet-b verwenden.
**[\<=]**

Zur Umsetzung des AnwendungsfallesDokumente durch einen Leistungserbringer
Einstellenaus  [gemSysL_ePA#3.7.1, UC 4.1 - Dokumente durch einen
Leistungserbringer einstellen]  wird Provide & Register Document Set-b
[ITI-41] gemäß Cross-Enterprise Document Reliable Interchange (XDR) Profile
profiliert. 

<table><tr><th>
IHE-Konzept

</th><th>
Wert

</th><th>
Referenz

</th></tr><tr><td>
PS als IHE Akteur

</td><td>
XDR Document Source

</td><td>
[IHE ITI-41]

</td></tr><tr><td>
XDR Document Source Options

</td><td>
keine

</td><td>
[IHE ITI-41#3.41.4.1.2.1] 

</td></tr><tr><td>
Document Relationships

[ITI TF-3#Table4.2.2.2-1]

</td><td>
RPLC (replace) analog zu Document Replacement Option einer XDS.b Document Source

</td><td>
[ITI TF-1#10.2.2] und  
[ITI TF-1#10.2.3]

</td></tr><tr><td>
SOAP-Action

</td><td>
urn:ihe:iti:2007:ProvideAndRegisterDocumentSet-b 

</td><td>
[IHE ITI-41#3.41.4.1.2]

</td></tr></table>

Die Unterstützung für RPLC (replace) hat zur Folge, dass Dokumente ersetzt
werden können durch eine neue Version des gleichen Dokuments. Das hat zur
Folge, dass das alte Dokument in den Status (DocumentEntry.availabilityStatus)
"Deprecated" wechselt und mit dem neuen Dokument (Status "Approved") über eine
"RPLC"-Association verbunden wird. Der AvailabilityStatus wird beim Dokumente
einstellen ausschließlich vom Aktensystem automatisiert gesetzt bzw. geändert.

### 5.2.1.1 Schnittstelle

Das Fachmodul ePA bietet zur logischen Schnittstelle I_PHR_Management am
WebservicePHR_Service (analog IHE-DienstDocumentRepository) die
OperationDocumentRepository_ProvideAndRegisterDocumentSet-b an, und übernimmt
gemäß [ITI-41] die Rolle eines IHEDocumentRepositorygegenüber dem PS.

<table><tr><th>
Operationsname

</th><th colspan="2">
DocumentRepository_ProvideAndRegisterDocumentSet-b [gemSpec_FM_ePA#7.1.1.1]

</th></tr><tr><td rowspan="2">
Aufrufparameter

</td><td>
Name

</td><td>
Implementierung

</td></tr><tr><td>
ProvideAndRegisterDocumentSetRequest 

</td><td>
[ITI-41#3.41.4.1.2] 

</td></tr><tr><td rowspan="2">
Rückgabeparameter

</td><td>
Name

</td><td>
Implementierung

</td></tr><tr><td>
RegistryResponse 

</td><td>
[ITI-41#3.41.4.2] 

</td></tr></table>

**A_14201 - Anwendungsfall Dokumente einstellen**

Das PS MUSS bei vorliegender Berechtigung Dokumente in die Akte eines
Versicherten einstellen können. Das Primärsystem MUSS im
DienstDocumentRepositorydes Konnektor-Fachmoduls die
OperationDocumentRepository_ProvideAndRegisterDocumentSet-bnutzen
[gemSpec_FM_ePA#7.1.1.1] und dazu schemakonforme SOAP-Nachrichten erstellen
können. **[\<=]**

**A_14253 - Metadaten-Pflicht für Dokumente**

Das PS MUSS Metadaten ausschließlich aus der im [gemSpec_DM_ePA] aufgeführten
Menge von Metadaten entnehmen. Das Primärsystem MUSS Dokumente, denen es keine
passenden Metadaten zuweisen kann, von der Auswahl der einzustellenden
Dokumente ausschließen. Das PS MUSS das
MetadatenobjektXDSDocumentEntry entsprechend den Vorgaben aus dem Datenmodell
[gemSpec_DM_ePA#Tabelle Nutzungsvorgaben für Metadatenattribute XDS.b]
befüllen. Das PS MUSS alle als R=requiredmarkierten Metadatenfelder setzen.
**[\<=]**

Die Auswahl der Metadaten soll möglichst weitgehend automatisiert werden.

**A_16194 - Änderbarkeit der Metadaten - Auswahllisten**

Bei der Auswahl der Metadaten zum Zwecke des Einstellens von Dokumenten MUSS das
PS insbesondere im Falle erforderlicher Auswahldialoge beachten:

 ---> UL

**[\<=]**

**A_20179-01 - Setzen der Vertraulichkeitsstufe**

Beim Einstellen von Dokumenten MUSS das PS für jedes Dokument eine
Vertraulichkeitsstufe wählen, die dem Wunsch des Versicherten entspricht, d.h.
entweder "streng vertraulich" (very restricted),  "vertraulich" (restricted)
oder "normal" (normal). **[\<=]**

Eine entsprechende Absprache zwischen LEI und Versichertem muss nicht
zwangsläufig explizit für jedes einzelne Dokument getroffen werden, sondern
kann auch im Vorfeld stattfinden, z. B. über eine Vereinbarung über die
Vertraulichkeitsstufe von bestimmten Dokumententypen oder ähnliche
Mechanismen. 

**A_20517-02 - Exklusivität der Dokumentenkategorien**

Das PS MUSS beim Einstellen von Dokumenten die Kategorien beachten, zu denen
Dokumente gehören. Dabei werden Kategorien durch zwei Arten von Foldern
umgesetzt:

 ---> UL

**[\<=]**

Dokumente werden statischen Ordnern automatisch am Aktensystem aufgrund der
vergebenen Metadaten zugeordnet. Dokumente werden dynamischer Ordnern
(mothersrecord und childsrecord) hingegen durch das PS zugeordnet. Der
Leistungserbringer legt bei Bedarf dynamische Ordner an:

 ---> UL

**A_20180-02 - Für Mutterpass und U-Heft dynamische Ordner auswählen**

Falls das hochzuladende Dokument in die Kategorien mit dynamischen Ordnern
fällt (mothersrecord und childsrecord, siehe
[gemSpec_DM_ePA#Tab_DM_Dokumentenkategorien]), MUSS das PS das hochzuladende
Dokument genau einem der dynamischen Ordner zuweisen, indem es das Dokument in
den entsprechenden Ordner hochlädt. Dazu MUSS das PS beim Einstellen im
SubmissionSet mit demDocumentEntryeine zusätzliche Association
(FD-DE-HasMember) hinterlegen, die denDocumentEntrymit dem für die gewünschte
Unterkategorie bereits existierenden Ordner über ihre
jeweiligeuniqueIdverbindet, vgl. u.a. [IHE-ITI-TF3#4.2.1.3]. **[\<=]**

DieuniqueIddes Ordners kann z. B. über die Suche FindFoldersmit entsprechendem
Filter aufFolder.codeListermittelt werden.

**A_14932 - Bildung und Verwendung einer UUID für Dokumente**

Das PS MUSS eineDocumentEntry.UniqueIDgemäß [ITI-TF-3#4.2.3.2.26] erstellen.
Für die Dokumentenverwaltung im ePA-Aktensystem wird
dieDocumentEntry.UniqueIDin die Metadaten der IHE-Nachrichten eingestellt: 

 ---> UL

**[\<=]**

Das PS soll die DocumentEntry.UniqueID gemäß [ITI-TF-3#4.2.3.2.26] nicht nur
für das Laden von Dokumenten, sondern auch in der Primärakte
verwenden. Eine aktenweit eindeutigeDocumentEntry.UniqueIDermöglicht dem PS
eine zuverlässige Benachrichtigungsverwaltung (s. Kap. 5.3.1 und Kap. 5.2.3).

### 5.2.1.2 Umsetzung

Die Aktivitäten des AnwendungsfallesDokumente einstellensind:

Vorbedingung:

 ---> UL

Auslöser:

 ---> UL

Aktivitäten:

 ---> UL

Resultat:

 ---> UL

Beispiel#: Bsp_ILF_ePA_ProvideAndRegisterDocumentSetRequest

<table><tr><th>
\<?xml version="1.0" encoding="UTF-8"?\>  
\<soap:Envelope
xmlns:m2="http://ws.gematik.de/fa/phr/v1.1"
xmlns:m1="http://ws.gematik.de/conn/ConnectorCommon/v5.0"
xmlns:m0="http://ws.gematik.de/conn/ConnectorContext/v2.0"
xmlns:soap="http://www.w3.org/2003/05/soap-envelope"
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"\>  
\<soap:Header\> 

\<m:ContextHeader xmlns:m="http://ws.gematik.de/conn/phrs/PHRService/v1.3"\> 

\<m0:Context\>  
\<m1:MandantId\>Mandant1\</m1:MandantId\> 

\<m1:ClientSystemId\>ClientID1\</m1:ClientSystemId\> 

\<m1:WorkplaceId\>CATS\</m1:WorkplaceId\>  
\</m0:Context\> 

\<m:RecordIdentifier\>  
\<m2:InsurantId extension="X110411319"
root="1.2.276.0.76.4.8"/\> 

\<m2:HomeCommunityId\>urn:oid:1.2.276.0.76.3.1.315.3.2.1.1\</m2:HomeCommunityId\>
 
\</m:RecordIdentifier\>  
\</m:ContextHeader\>  
\<Action
xmlns="http://www.w3.org/2005/08/addressing"\>urn:ihe:iti:2007:ProvideAndRegisterDocumentSet-b\</Action\>
 
\<MessageID
xmlns="http://www.w3.org/2005/08/addressing"\>cc7f3acb-d210-4ca0-9d9e-7143f1b95ee3\</MessageID\>
 
\<To
xmlns="http://www.w3.org/2005/08/addressing"\>http://10.11.217.160:80/ws/PHRService\</To\>
 
\<ReplyTo xmlns="http://www.w3.org/2005/08/addressing"\> 

\<Address\>http://www.w3.org/2005/08/addressing/anonymous\</Address\> 

\</ReplyTo\>  
\<xdr:homeCommunityBlock xmlns:xdr="urn:ihe:iti:xdr:2014"\> 

\<xdr:homeCommunityId\>urn:oid:1.2.276.0.76.3.1.315.3.2.1.1\</xdr:homeCommunityId\>
 
\</xdr:homeCommunityBlock\>  
\</soap:Header\>  
\<soap:Body\> 

\<ProvideAndRegisterDocumentSetRequest xmlns="urn:ihe:iti:xds-b:2007"
xmlns:lcm="urn:oasis:names:tc:ebxml-regrep:xsd:lcm:3.0"
xmlns:rs="urn:oasis:names:tc:ebxml-regrep:xsd:rs:3.0"
xmlns:rim="urn:oasis:names:tc:ebxml-regrep:xsd:rim:3.0"\> 

\<lcm:SubmitObjectsRequest\>  
\<rs:RequestSlotList\>  
\<rim:Slot
name="homeCommunityId"\>  
\<rim:ValueList\> 

\<rim:Value\>urn:oid:1.2.276.0.76.3.1.315.3.2.1.1\</rim:Value\> 

\</rim:ValueList\>  
\</rim:Slot\>  
\</rs:RequestSlotList\> 

\<rim:RegistryObjectList\>  
\<!-- SubmissionSet --\>  
\<rim:RegistryPackage
home="urn:oid:1.2.276.0.76.3.1.315.3.2.1.1"
objectType="urn:oasis:names:tc:ebxml-regrep:ObjectType:RegistryObject:RegistryPackage"
id="submissionset"\>  
\<!-- SubmissionSet.submissionTime --\>  
\<rim:Slot
name="submissionTime"\>  
\<rim:ValueList\> 

\<rim:Value\>20201218172143\</rim:Value\>  
\</rim:ValueList\>  
\</rim:Slot\>
 
\<!-- SubmissionSet.author --\>  
\<rim:Classification
objectType="urn:oasis:names:tc:ebxml-regrep:ObjectType:RegistryObject:Classification"
id="author" classifiedObject="submissionset"
classificationScheme="urn:uuid:a7058bb9-b4e4-4307-ba5b-e3f0ab85e12d"\> 

\<rim:Slot name="authorRole"\>  
\<rim:ValueList\> 

\<rim:Value\>11^^^&1.3.6.1.4.1.19376.3.276.1.5.13&ISO\</rim:Value\> 

\</rim:ValueList\>  
\</rim:Slot\>  
\<rim:Slot name="authorPerson"\> 

\<rim:ValueList\>  
\<rim:Value\>^Münchhausen^David^^^Prof.
Dr.^^^\</rim:Value\>  
\</rim:ValueList\>  
\</rim:Slot\>  
\<rim:Slot
name="authorInstitution"\>  
\<rim:ValueList\>  
\<rim:Value\>Praxis David Graf
MünchhausenNOT-VALID^^^^^&1.2.276.0.76.4.188&ISO^^^^1-SMC-B-Testkarte-783110000092399\</rim:Value\>
 
\</rim:ValueList\>  
\</rim:Slot\>  
\</rim:Classification\>  
\<!--
SubmissionSet.contentTypeCode --\>  
\<rim:Classification
objectType="urn:oasis:names:tc:ebxml-regrep:ObjectType:RegistryObject:Classification"
id="contentType" classifiedObject="submissionset"
classificationScheme="urn:uuid:aa543740-bdda-424e-8c96-df4873be8500"
nodeRepresentation="8"\>  
\<rim:Slot name="codingScheme"\>  
\<rim:ValueList\>
 
\<rim:Value\>1.3.6.1.4.1.19376.3.276.1.5.12\</rim:Value\> 

\</rim:ValueList\>  
\</rim:Slot\>  
\<rim:Name\>  
\<rim:LocalizedString
xml:lang="de-DE" value="Veranlassung durch Patient"/\>  
\</rim:Name\> 

\</rim:Classification\>  
\<!-- SubmissionSet Classification of
RegistryPackage --\>  
\<rim:Classification
objectType="urn:oasis:names:tc:ebxml-regrep:ObjectType:RegistryObject:Classification"
id="SubmissionSetClassification" classifiedObject="submissionset"
classificationNode="urn:uuid:a54d6aa5-d40d-43f9-88c5-b4633d873bdd"/\>  
\<!--
SubmissionSet.patientId --\>  
-\<rim:ExternalIdentifier
objectType="urn:oasis:names:tc:ebxml-regrep:ObjectType:RegistryObject:ExternalIdentifier"
id="patientId" value="X110411319^^^&1.2.276.0.76.4.8&ISO"
registryObject="submissionset"
identificationScheme="urn:uuid:6b5aea1a-874d-4603-a4bc-96a0a7b38446"\> 

-\<rim:Name\>  
\<rim:LocalizedString value="XDSSubmissionSet.patientId"/\> 

\</rim:Name\>  
\</rim:ExternalIdentifier\>  
\<!-- SubmissionSet.uniqueId
--\>  
-\<rim:ExternalIdentifier
objectType="urn:oasis:names:tc:ebxml-regrep:ObjectType:RegistryObject:ExternalIdentifier"
id="uniqueId"
value="1.2.840.113556.1.8000.2554.35589.34102.63238.18691.36463.16560801.3400984"
registryObject="submissionset"
identificationScheme="urn:uuid:96fdda7c-d067-4183-912e-bf5ee74998a8"\> 

\<rim:Name\>  
\<rim:LocalizedString value="XDSSubmissionSet.uniqueId"/\> 

\</rim:Name\>  
\</rim:ExternalIdentifier\>  
\</rim:RegistryPackage\> 

\<rim:Association id="association-0" targetObject="DocumentEntry-0"
sourceObject="submissionset"
associationType="urn:oasis:names:tc:ebxml-regrep:AssociationType:HasMember"\> 

\<rim:Slot name="SubmissionSetStatus"\>  
\<rim:ValueList\> 

\<rim:Value\>Original\</rim:Value\>  
\</rim:ValueList\>  
\</rim:Slot\> 

\</rim:Association\>  
\<rim:ExtrinsicObject
home="urn:oid:1.2.276.0.76.3.1.315.3.2.1.1"
objectType="urn:uuid:7edca82f-054d-47f2-a032-9b2a5b5186c1" id="DocumentEntry-0"
mimeType="application/xml"\>  
\<!-- DocumentEntry.creationTime --\> 

\<rim:Slot name="creationTime"\>  
\<rim:ValueList\> 

\<rim:Value\>20191209124919\</rim:Value\>  
\</rim:ValueList\>  
\</rim:Slot\>
 
\<!-- DocumentEntry.languageCode --\>  
\<rim:Slot name="languageCode"\> 

\<rim:ValueList\>  
\<rim:Value\>de-DE\</rim:Value\>  
\</rim:ValueList\> 

\</rim:Slot\>  
\<rim:Slot name="URI"\>  
\<rim:ValueList\> 

\<rim:Value\>pssim_nfd.xml\</rim:Value\>  
\</rim:ValueList\>  
\</rim:Slot\> 

\<!-- DocumentEntry.Title --\>  
\<rim:Name\>  
\<rim:LocalizedString
xml:lang="de-DE" value="PsSim: Notfalldaten"/\>  
\</rim:Name\>  
\<!--
DocumentEntry.classCode --\>  
\<rim:Classification
objectType="urn:oasis:names:tc:ebxml-regrep:ObjectType:RegistryObject:Classification"
id="class-0" classifiedObject="DocumentEntry-0"
classificationScheme="urn:uuid:41a5887f-8865-4c09-adf7-e362475b143a"
nodeRepresentation="AUS"\>  
\<rim:Slot name="codingScheme"\> 

\<rim:ValueList\>  
\<rim:Value\>1.3.6.1.4.1.19376.3.276.1.5.8\</rim:Value\> 

\</rim:ValueList\>  
\</rim:Slot\>  
\<rim:Name\>  
\<rim:LocalizedString
xml:lang="de-DE" value="Medizinischer Ausweis"/\>  
\</rim:Name\> 

\</rim:Classification\>  
\<!-- DocumentEntry.confidentialityCode --\> 

\<rim:Classification
objectType="urn:oasis:names:tc:ebxml-regrep:ObjectType:RegistryObject:Classification"
id="confidentiality-0" classifiedObject="DocumentEntry-0"
classificationScheme="urn:uuid:f4f85eac-e6cb-4883-b524-f2705394840f"
nodeRepresentation="LEI"\>  
\<rim:Slot name="codingScheme"\> 

\<rim:ValueList\>  
\<rim:Value\>1.2.276.0.76.5.491\</rim:Value\> 

\</rim:ValueList\>  
\</rim:Slot\>  
\<rim:Name\>  
\<rim:LocalizedString
xml:lang="de-DE" value="Dokument einer Leistungserbringerinstitution"/\> 

\</rim:Name\>  
\</rim:Classification\>  
\<!-- DocumentEntry.formatCode --\> 

\<rim:Classification
objectType="urn:oasis:names:tc:ebxml-regrep:ObjectType:RegistryObject:Classification"
id="formatCode-0" classifiedObject="DocumentEntry-0"
classificationScheme="urn:uuid:a09d5840-386c-46f2-b5ad-9c3699a4309d"
nodeRepresentation="urn:gematik:ig:Notfalldatensatz:r3.1"\>  
\<rim:Slot
name="codingScheme"\>  
\<rim:ValueList\> 

\<rim:Value\>1.3.6.1.4.1.19376.3.276.1.5.6\</rim:Value\>  
\</rim:ValueList\> 

\</rim:Slot\>  
\<rim:Name\>  
\<rim:LocalizedString xml:lang="de-DE"
value="Notfalldatensatz"/\>  
\</rim:Name\>  
\</rim:Classification\>  
\<!--
DocumentEntry.healthCareFacilityTypeCode --\>  
\<rim:Classification
objectType="urn:oasis:names:tc:ebxml-regrep:ObjectType:RegistryObject:Classification"
id="healthCare-0" classifiedObject="DocumentEntry-0"
classificationScheme="urn:uuid:f33fb8ac-18af-42cc-ae0e-ed0b0bdb91e1"
nodeRepresentation="PRA"\>  
\<rim:Slot name="codingScheme"\> 

\<rim:ValueList\>  
\<rim:Value\>1.3.6.1.4.1.19376.3.276.1.5.2\</rim:Value\> 

\</rim:ValueList\>  
\</rim:Slot\>  
\<rim:Name\>  
\<rim:LocalizedString
xml:lang="de-DE" value="Arztpraxis"/\>  
\</rim:Name\> 

\</rim:Classification\>  
\<!-- DocumentEntry.authorPerson and
DocumentEntry.authorRole --\>  
\<rim:Classification
objectType="urn:oasis:names:tc:ebxml-regrep:ObjectType:RegistryObject:Classification"
id="author-0" classifiedObject="DocumentEntry-0"
classificationScheme="urn:uuid:93606bcf-9494-43ec-9b4e-a7748d1a838d"\> 

\<rim:Slot name="authorRole"\>  
\<rim:ValueList\> 

\<rim:Value\>11^^^&1.3.6.1.4.1.19376.3.276.1.5.13&ISO\</rim:Value\> 

\</rim:ValueList\>  
\</rim:Slot\>  
\<rim:Slot name="authorPerson"\> 

\<rim:ValueList\> 

\<rim:Value\>^Müller-Holzscheit^Marcello-Bernhardino^^^Dr.^^^\</rim:Value\> 

\</rim:ValueList\>  
\</rim:Slot\>  
\</rim:Classification\>  
\<!--
DocumentEntry.practiceSettingCode --\>  
\<rim:Classification
objectType="urn:oasis:names:tc:ebxml-regrep:ObjectType:RegistryObject:Classification"
id="practiceSettingCode-0" classifiedObject="DocumentEntry-0"
classificationScheme="urn:uuid:cccf5598-8b07-4b77-a05e-ae952c785ead"
nodeRepresentation="ALLG"\>  
\<rim:Slot name="codingScheme"\> 

\<rim:ValueList\>  
\<rim:Value\>1.3.6.1.4.1.19376.3.276.1.5.4\</rim:Value\> 

\</rim:ValueList\>  
\</rim:Slot\>  
\<rim:Name\>  
\<rim:LocalizedString
xml:lang="de-DE" value="Allgemeinmedizin"/\>  
\</rim:Name\> 

\</rim:Classification\>  
\<!-- DocumentEntry.typeCode --\> 

\<rim:Classification
objectType="urn:oasis:names:tc:ebxml-regrep:ObjectType:RegistryObject:Classification"
id="typeCode-0" classifiedObject="DocumentEntry-0"
classificationScheme="urn:uuid:f0306f51-975f-434e-a61c-c59651d33983"
nodeRepresentation="BESC"\>  
\<rim:Slot name="codingScheme"\> 

\<rim:ValueList\>  
\<rim:Value\>1.3.6.1.4.1.19376.3.276.1.5.9\</rim:Value\> 

\</rim:ValueList\>  
\</rim:Slot\>  
\<rim:Name\>  
\<rim:LocalizedString
xml:lang="de-DE" value="Ärztliche Bescheinigungen"/\>  
\</rim:Name\> 

\</rim:Classification\>  
\<rim:ExternalIdentifier
objectType="urn:oasis:names:tc:ebxml-regrep:ObjectType:RegistryObject:ExternalIdentifier"
id="patientId-0" value="X110411319^^^&1.2.276.0.76.4.8&ISO"
registryObject="DocumentEntry-0"
identificationScheme="urn:uuid:58a6f841-87b3-4a3e-92fd-a8ffeff98427"\> 

\<rim:Name\>  
\<rim:LocalizedString value="XDSDocumentEntry.patientId"/\> 

\</rim:Name\>  
\</rim:ExternalIdentifier\>  
\<rim:ExternalIdentifier
objectType="urn:oasis:names:tc:ebxml-regrep:ObjectType:RegistryObject:ExternalIdentifier"
id="uniqueId-0"
value="1.2.840.113556.1.8000.2554.20502.5074.39693.19397.40947.3962341.16685811"
registryObject="DocumentEntry-0"
identificationScheme="urn:uuid:2e82c1f6-a085-4c72-9da3-8640a32e42ab"\> 

\<rim:Name\>  
\<rim:LocalizedString value="XDSDocumentEntry.uniqueId"/\> 

\</rim:Name\>  
\</rim:ExternalIdentifier\>  
\</rim:ExtrinsicObject\> 

\</rim:RegistryObjectList\>  
\</lcm:SubmitObjectsRequest\>  
\<Document
id="DocumentEntry-0"\>  
\<Include
xmlns="http://www.w3.org/2004/08/xop/include" href="cid:Document0@PHRService.konlan"/\>
 
\</Document\>  
\</ProvideAndRegisterDocumentSetRequest\>  
\</soap:Body\> 

\</soap:Envelope\>

</th></tr></table>

XDS-Option „Document Replacement“ - Ersetzen eines existierenden Dokuments

Ein eingestelltes Dokument kann auch ein existierendes Dokument ersetzen. Dies
erfolgt durch Verwendung der „Document Replacement“-Option. Dazu wird das
gleiche Dokument (mit geändertem Inhalt und nebst ggf. geänderten
DocumentEntry-Metadaten) erneut hochgeladen. Das neue Dokument erhält den
Status „Approved“. Das alte Dokument geht in den Status „Deprecated“.
 Beide Dokumente werden über eine „Replace“-Assoziation miteinander
verbunden, so dass nach dem Einstellen erkennbar ist, dass das neue Dokument
das alte ersetzt. Lädt man erneut eine neue Fassung hoch, erhält man analog
zwei Dokumente im Status "Deprecated" und das neueste im Status "Approved".Alle
alten Dokumente (Status "Deprecated") können nach wie vor gefunden und
heruntergeladen werden. Einige Suchen erlauben das Filtern nach Status bzw.
zeigen per Default auch nur Dokumente im Status „Approved“ an.Eingestellt
(im „Submission Set“) wird das neue Dokument inkl. DocumentEntry-Metadaten,
ein Verweis auf das alte Dokument und die verbindende „Replace“-Association
(urn:ihe:iti:2007:AssociationType:RPLC).

### 5.2.1.3 Nutzung

Dokumente, die Leistungserbringer einstellen, werden unabhängig vom Inhalt des
Dokumentes als LE-Dokumente (Kennzeichnung über entsprechende Auswahl
aus SubmissionSet.AuthorRole, siehe [gemSpec_DM_ePA#2.1.4.1],und dem
konfiguriertenXDSDocumentEntry.healthcareFacilityTypeCode) kategorisiert, um
sie von Dokumenten zu unterscheiden, die vom Versicherten selbst
(SubmissionSet.AuthorRole="102") oder von Kostenträgern
(SubmissionSet.AuthorRole="105") eingestellt wurden. Das heißt u.a., dass die
Codes für Versicherte und Kostenträger ("102" und "105") dabei explizit nicht
verwendet werden dürfen.

**A_15621-02 - Kategorisierung der vom LE eingestellten Dokumente**

Das PS MUSS die von der LEI eingestellten Dokumente kategorisieren:

 ---> UL

DocumentEntry und SubmissionSet enthalten übereinstimmende Werte, wenn der
Autor des Dokumentes aus der das Dokument einstellenden Institution stammt.
Falls eine LEI ein Dokument hochlädt, das einer Quelle außerhalb der
hochladenden LEI entstammt, können diese Wert voneinander abweichen.  **[\<=]**

**A_14251 - Vom LE in die Akten einstellbare Dokumententypen**

Das Primärsystem MUSS die in die ePA einstellbaren
Dokumententypenaus[gemSpec_DM_ePA#A_14760] in die ePA einstellen können. **[\<=]**

Beispiel#: Bsp_ILF_ePA_ProvideAndRegisterDocumentSetResponse

<table><tr><th>
\<?xml version="1.0" encoding="UTF-8"?\>  
\<soap:Envelope
xmlns:soap="http://www.w3.org/2003/05/soap-envelope"\>  
\<soap:Header\> 

\<Action xmlns="http://www.w3.org/2005/08/addressing"/\>  
\<MessageID
xmlns="http://www.w3.org/2005/08/addressing"\>urn:uuid:48d9984a-eaa9-4b54-b968-216e98a13e3b\</MessageID\>
 
\<To
xmlns="http://www.w3.org/2005/08/addressing"\>http://www.w3.org/2005/08/addressing/anonymous\</To\>
 
\<RelatesTo
xmlns="http://www.w3.org/2005/08/addressing"\>6e2fa9e2-18fb-4071-b796-a49c5fe9a303\</RelatesTo\>
 
\</soap:Header\>  
\<soap:Body\>  
\<ns8:RegistryResponse
status="urn:oasis:names:tc:ebxml-regrep:ResponseStatusType:Success"
xmlns:ns2="http://ws.gematik.de/conn/ConnectorCommon/v5.0"
xmlns:ns3="http://ws.gematik.de/conn/ConnectorContext/v2.0"
xmlns:ns4="http://ws.gematik.de/fa/phr/v1.1"
xmlns:ns5="http://ws.gematik.de/conn/phrs/PHRService/v1.3"
xmlns:ns6="urn:ihe:iti:xds-b:2007"
xmlns:ns7="urn:oasis:names:tc:ebxml-regrep:xsd:rim:3.0"
xmlns:ns8="urn:oasis:names:tc:ebxml-regrep:xsd:rs:3.0"
xmlns:ns9="urn:oasis:names:tc:ebxml-regrep:xsd:query:3.0"
xmlns:ns10="urn:oasis:names:tc:ebxml-regrep:xsd:lcm:3.0"
xmlns:ns11="http://ws.gematik.de/fa/vsdm/vsd/v5.2"
xmlns:ns12="http://www.w3.org/2006/05/addressing/wsdl"
xmlns:ns13="http://ws.gematik.de/tel/error/v2.0"
xmlns:ns14="urn:oasis:names:tc:dss:1.0:core:schema"
xmlns:ns15="http://www.w3.org/2000/09/xmldsig#" xmlns:ns16="urn:hl7-org:v3"
xmlns:ns17="urn:oasis:names:tc:SAML:1.0:assertion"
xmlns:ns18="urn:ihe:iti:rmd:2017"/\>  
\</soap:Body\>  
\</soap:Envelope\>

</th></tr><tr><th>
                       

</th></tr></table>

In [gemSpec_DM_ePA#A_14760] ist beschrieben, bei Einhaltung welcher Vorgaben
konsistente Metadaten für das Einstellen des Dokumentes erzeugt werden
können. 

**A_16187 - Maximalgröße des Dokumentes**

Das PS MUSS sicherstellen, dass jedes einzelne einzustellende Dokument nicht
größer als 25 MB ist, und dass ein Satz der in einem einzelnen Request
einzustellenden Dokumente insgesamt nicht größer als 250 MB ist. **[\<=]**

**A_16188 - MTOM-Pflicht bei [ITI-43]**

Das PS MUSS bei der Umsetzung der IHE XDS-Transaktion [ITI-43] die Übertragung
von Dokumenten mit MTOM/XOP [MTOM] umsetzen. **[\<=]**

<table><tr><th>
Fehlercode

</th><th>
Beschreibung

</th><th>
Handlungsanweisung

</th></tr><tr><td>
7211  

</td><td>
Dokument überschreitet maximal zulässige Größe von 25 MB 

</td><td>
Den Versicherten bei Bedarf über das Fehlen der Möglichkeit zum Einstellen des
übergroßen Dokumentes informieren.

</td></tr><tr><td>
7212

</td><td>
Summe der Dokumente überschreitet maximal zulässige Größe von 250 MB

</td><td>
Dokumentenpaket verkleinern (etwa durch Aufteilung) und ein kleineres
Dokumentenpaket einstellen.

</td></tr></table>

### 5.2.2 Dokumente suchen

Frau Gundlach berichtet Dr. Weber über den Arztbrief, den ihr Radiologe vor
wenigen Tagen in ihre Patientenakte geschrieben hat. Dr. Weber sieht in seiner
lokalen Akte, dass die 7 Tage lang gültige Berechtigung auf die elektronische
Akte zuzugreifen, noch nicht abgelaufen ist. Er sucht nach dem Arztbrief des
Radiologen über dessen Namen in der ePA-Suchmaske des PVS. Sein PVS zeigt ihm
Metadaten zum Arztbrief des Kollegen an.

Zur Umsetzung des AnwendungsfallesDokumente durch einen Leistungserbringer
suchenaus [gemSysL_ePA#3.7.3, UC 4.3 - Dokumente durch einen Leistungserbringer
suchen] wird Registry Stored Query [ITI-18] profiliert.

**A_15652 - Funktionsmerkmal Dokumente Suchen**

Das PS MUSS es dem Leistungserbringer ermöglichen, ePA-Dokumente in der Akte
eines Versicherten suchen zu können. Dafür MUSS das PS
dieKonnektorschnittstellenoperationRegistryStoredQuery verwenden. **[\<=]**

<table><tr><th>
IHE-Konzept

</th><th>
Wert

</th><th>
Referenz

</th></tr><tr><td>
PS als IHE Akteur

</td><td>
Document Consumer

</td><td>
Registry Stored Query [ITI-18] (ITI TF-2a: 3.18)

</td></tr><tr><td>
Document Relationships

[ITI TF-3#Table4.2.2.2-1]

</td><td>
RPLC (replace) analog zu Document Replacement Option einer XDS.b Document Source

</td><td>
[ITI TF-1#10.2.2] und

[ITI TF-1#10.2.3]

</td></tr><tr><td>
Stored Queries

</td><td>
FindDocuments, FindDocumentsByTitle, FindSubmissionSets,
FindDocumentsByReferenceID,  
GetSubmissionSets,
GetSubmissionSetsAndContents, GetAll und
GetDocuments, GetAssociations, GetDocumentsAndAssociations,  

GetRelatedDocuments, FindFolders,
GetFolders, GetFoldersForDocument, GetFolderAndContents

</td><td>
Registry Stored Query [ITI-18]

</td></tr><tr><td>
SOAP-Action

</td><td>
urn:ihe:iti:2007:RegistryStoredQuery

</td><td>
[ITI-18#3.18.4.1]

</td></tr></table>

Das Suchen nach Dokumenten erfolgt auf den Metadaten des Dokumentes, nicht auf
den Inhalten des Dokumentes selbst. Die Suche kann zur Anzeigen der Metadaten
eines Dokumentes verwendet werden. 

UmDokumente suchenzu können, brauchen Leistungserbringer nicht zu wissen,
welche Art Berechtigung sie erhalten haben (Zugriffsberechtigung auf
LE-Dokumente, Versicherten-Dokumente oder mehrere dieser Dokumententypen). Die
Suche erfolgt immer ausschließlich auf den berechtigungsgemäß tatsächlich
zugänglichen Dokumenten, nie auf Dokumenten, für die keine
Zugriffsberechtigung besteht. 

Zur Suche nach Dokumenten zu einem RecordIdentifier sind u.a. folgende
Filterfunktionen möglich:

 ---> UL

Weitere für Suchstrategien geeignete Metadaten von Dokumenten (Metadaten)
können [gemSpec_DM_ePA] entnommen werden. Sie beziehen sich vor allem auf
Informationen der Dokumentenverwaltung, weniger auf den (medizinischen) Inhalt
der Dokumente.

**A_16336-01 - Eingrenzung von Suchergebnissen**

Das PS SOLL verschiedene Strategien nutzen können, um die Menge der
ePA-Dokumente einer Akte auf die für den LE relevanten Dokumente zu reduzieren:

 ---> UL

**[\<=]**

Das Ergebnis der Suche in der Dokumenten-Registry sind Mengen eindeutiger
Dokumenten-Identifier als UUID.

**A_21133 - Identifizierung unscharfer Ergebnisse**

Das PS SOLL etwaige unscharfe Suchergebnisse (siehe
gemSpec_Dokumentenverwaltung#A_21131) in der Ergebnismenge als solche
kennzeichnen können. **[\<=]**

### 5.2.2.1 Schnittstelle

Das Fachmodul ePA bietet zur logischen Schnittstelle I_PHR_Managementam
WebservicePHR_Service(analog IHE-DienstDocumentRegistry)die
OperationDocumentRegistry_RegistryStoredQueryan, die in ihrem Außenverhalten
der Schnittstellendefinition des [ITI-18] folgt und die Rolle eines
IHEDocumentRegistrygegenüber dem PS übernimmt.

<table><tr><th>
Operationsname

</th><th colspan="2">
DocumentRegistry_RegistryStoredQuery [gemSpec_FM_ePA#7.1.1.2]

</th></tr><tr><td rowspan="2">
Aufrufparameter

</td><td>
Name

</td><td>
Implementierung

</td></tr><tr><td>
AdhocQueryRequest 

</td><td>
Stored Query aus  Tab_ILF_ePA_StoredQueries

</td></tr><tr><td rowspan="2">
Rückgabeparameter

</td><td>
Name

</td><td>
Implementierung

</td></tr><tr><td>
AdhocQueryResponse

</td><td>
ebXML version 3 [ebRS] gemäß

[ITI-18]#3.18.4.1.2.6

</td></tr></table>

**A_17198-01 - Nutzung des um XDSDocumentEntryTitle erweiterten Registry Stored
Query FindDocuments**

Das PS MUSS den in [ITI-18] nicht enthaltenen zusätzlichen
Anfragetyp FindDocumentsByTitlemit der Query-ID
"urn:uuid:ab474085-82b5-402d-8115-3f37cb1e2405" und denselben
Parameternutzungsvorgaben der Registry Stored QueryFindDocumentsgemäß
[IHE-ITI-TF2a#3.18.4.1.2.3.7.1] in Verbindung mit dem zusätzlich zu [ITI-18]
eingeführten Suchparameter$XDSDocumentEntryTitlenutzen können. Der
zusätzliche Parameter $XDSDocumentEntryTitle ist verpflichtend und filtert
die Suchergebnismenge über das AttributXDSDocumentEntry.title, siehe auch
[gemSpec_Dokumentenverwaltung#A_17184]. **[\<=]**

**A_18197 - Suche nach Institutionen im Anfragetyp "FindDocumentsByTitle"**

Das PS KANN im Anfragetyp FindDocumentsByTitle den optionalen Parameter
$XDSDocumentEntryAuthorInstitution setzen, um eine Suchanfrage nach
Institutionen durchzuführen, bei denen die Ergebnismenge auf  Einträge
eingeschränkt wird, die im XDSDocumentEntry.author-Slot über ein
zutreffendes authorInstitution-Sub-Attribut verfügen.          
**[\<=]**

Für die Suche über beiden Parameter

 ---> UL

ist eine Ähnlichkeitssuche möglich, wie auch beim Parameter
$XDSDocumentEntryAuthorPerson. Diese Ähnlichkeitssuche beruht auf dem
SQL-Suchmuster LIKE,in dem mit einer Kombination aus dem SQL-Wildcard-Zeichen
"%" und dem SQL-Platzhalterzeichen "_" Suchanfragen zusammengestellt werden, in
denen nach einer Kombination aus bestimmten und beliebigen Zeichen gesucht
wird.

Zudem können bei Verwendung der folgenden Suchparameter auch auf diese
Suchparameter bezogen unscharfe, d.h. leicht abweichende, Suchergebnisse
zurückgegeben werden:

 ---> UL

Ob und inwieweit unscharfe Ergebnisse für diese Parameter zurückgegeben
werden, kann das PS nicht steuern.

### 5.2.2.2 Umsetzung

Die Umsetzung der Suchen von Dokumenten über Metadaten ist in vielfältiger
Form möglich, insbesondere als

 ---> OL

<table><tr><th>
Parametername

</th><th>
Attribut

</th><th>
Befüllung

</th></tr><tr><td>
$XDSDocumentEntryPatientId 

</td><td>
XDSDocumentEntry.patientId 

</td><td>
patientID

</td></tr><tr><td>
$XDSDocumentEntryStatus 

</td><td>
XDSDocumentEntry.availabilityStatus 

</td><td>
urn:oasis:names:tc:ebxml-regrep:StatusType:Approved

 

</td></tr></table>

Je nachdem, obreturnTypeauf LeafClassoder ObjectRefgesetzt wird, enthält die
Response der Suche eine Objektliste im Result (LeafClass) oder eine Liste von
Objektidentifiern (ObjectRef), s. [ITI-18#3.18.4.1.2.6].

Die Aktivitäten des AnwendungsfallesDokumente suchensind:

Vorbedingung:

 ---> UL

Auslöser:

 ---> UL

Aktivitäten:

 ---> UL

Resultat:

 ---> UL

### 5.2.2.3 Nutzung

**A_14907 - Setzen des Message-Identifiers im Dokumentensuche-Request**

Die WS-Requests der Dokumentensuche werden alsAdhocQuerymit der Stored Query ID
aus [ITI-18#3.18.4.1.2.4] an die ePA-Aktensysteme versendet. Dabei MUSS das PS
die wsa:MessageIDalsUUIDgemäß PHR_Common.xsd im SOAP-Header des Requests
setzen. **[\<=]**

Beispiel#: Bsp_ILF_ePA_Request_AdhocQuery

<table><tr><th>
\<query:AdhocQueryRequest xmlns="urn:ihe:iti:xds-b:2007"
xmlns:query="urn:oasis:names:tc:ebxml-regrep:xsd:query:3.0"
xmlns:rim="urn:oasis:names:tc:ebxml-regrep:xsd:rim:3.0"\> 

\<query:ResponseOption returnComposedObjects="true" returnType="LeafClass"/\> 

\<rim:AdhocQuery home="urn:oid:1.2.276.0.76.3.1.405"
id="urn:uuid:14d4debf-8f97-4251-9a74-a90016b0af0d"\>  
\<rim:Slot
name="$XDSDocumentEntryPatientId"\>  
\<rim:ValueList\> 

\<rim:Value\>'X110473550^^^&1.2.276.0.76.4.8&ISO'\</rim:Value\> 

\</rim:ValueList\>  
\</rim:Slot\>  
\<rim:Slot
name="$XDSDocumentEntryStatus"\>  
\<rim:ValueList\> 

\<rim:Value\>('urn:oasis:names:tc:ebxml-regrep:StatusType:Approved')\</rim:Value\>
 
\</rim:ValueList\>  
\</rim:Slot\>  
\</rim:AdhocQuery\> 

\</query:AdhocQueryRequest\>

</th></tr></table>

Das PS soll Stored Query IDs der Tab_ILF_ePA_StoredQueries gemäß
[ITI-18#3.18.4.1.2.4] verwenden.

<table><tr><th>
Stored Queries

</th><th>
Implementierungshinweis (beispielhaft)

</th></tr><tr><td>
FindDocuments

</td><td>
Query verwendet id des AdhocQuery-Elements, weil nur zu einem einzelnen
Versicherten aus ihrer lokalen Patientenakte der Query durchgeführt wird. 

Für die Suche nach Arztbriefen allgemein: Angabe von

 classCode=BRI.

Für die Suche speziell nach Arztbriefen gemäß Kap. 6.3.3: Angabe von 

formatCode=

urn:gematik:ig:Arztbrief:r3.1.

</td></tr><tr><td>
FindSubmissionSets

</td><td>
$XDSSubmissionSetSubmissionTimeFrom

und 

$XDSSubmissionSetSubmissionTimeTo

schränken einen Zeitraum ein, in dem Ergebnisse der

SubmissionSet

-Suche hochgeladen wurden. Nutzbar für eine Delta-Suche in der
Benachrichtigungsverwaltung: Es wird nach aktuell eingestellten SubmissionSets
gesucht.

</td></tr><tr><td>
FindDocumentsByReferenceID

</td><td>
Semantisch identisch zum

FindDocuments Stored Query

</td></tr><tr><td>
GetSubmissionSets

</td><td>
Parameter $uuid mit 

XDSDocumentEntry.entryUUID 

ermittelt den

SubmissionSet

zu einem Dokument, z.B. zu einem eArztbrief, um verknüpfte Dokumente zu finden.

</td></tr><tr><td>
GetSubmissionSetsAndContents

</td><td>
Unter Angabe z.B. des formatCode für den eArztbrief werden

DocumentEntries

gefunden, die zum selben

SubmissionSet

eine

HasMember

Association aufweisen. 

</td></tr><tr><td>
GetAll

</td><td>
Für die Benachrichtigungsverwaltung (Kap. 5.4.1) können Metadaten aller
Dokumente einer Akte erhalten werden, für die eine Zugriffsberechtigung
besteht. 

</td></tr><tr><td>
GetDocuments

</td><td>
$homeCommunityId

erforderlich

</td></tr><tr><td>
FindFolders

</td></tr></table>

**A_15088-01 - LE-Dokumente suchen**

Das PS SOLL
mittels RegistryStoredQueryüber SubmissionSet.authorPerson Dokumente
herausfiltern können, die von Leistungserbringern eingestellt wurden. **[\<=]**

Beispiel#: Bsp_ILF_ePA_Request_getDocuments

<table><tr><th>
\<soapenv:Body\>  
    \<query:AdhocQueryRequest
xmlns:query="urn:oasis:names:tc:ebxml-regrep:xsd:query:3.0"\>  
     
\<query:ResponseOption returnComposedObjects="true" returnType="LeafClass"/\> 

      \<AdhocQuery xmlns="urn:oasis:names:tc:ebxml-regrep:xsd:rim:3.0"
id="urn:uuid:5c4f972b-d56b-40ac-a5fc-c8ca9b40b9d4"\>  
        \<Slot
name="$MetadataLevel"\>  
          \<ValueList\>  
           
\<Value\>  
              1  
            \</Value\>  
       
  \</ValueList\>  
        \</Slot\>  
        \<Slot
name="$XDSDocumentEntryEntryUUID"\>  
          \<ValueList\>  
     
      \<Value\>  
             
('urn:uuid:744e9ad5-bc2d-453d-b20e-a91c6e33eaf1')  
           
\</Value\>  
          \</ValueList\>  
        \</Slot\>  
     
\</AdhocQuery\>  
    \</query:AdhocQueryRequest\>  
  \</soapenv:Body\>

</th></tr></table>

Beispiel#: Bsp_ILF_ePA_Response_getDocuments

<table><tr><th>
\<S:Envelope xmlns:S="http://www.w3.org/2003/05/soap-envelope"\>  
 
\<S:Header\>  
...  
  \</S:Header\>  
  \<S:Body\>  
   
\<query:AdhocQueryResponse
xmlns:query="urn:oasis:names:tc:ebxml-regrep:xsd:query:3.0"
status="urn:oasis:names:tc:ebxml-regrep:ResponseStatusType:Success"\>  
   
  \<rim:RegistryObjectList
xmlns:rim="urn:oasis:names:tc:ebxml-regrep:xsd:rim:3.0"\>  
       
\<rim:ExtrinsicObject id="urn:uuid:744e9ad5-bc2d-453d-b20e-a91c6e33eaf1"
mimeType="application/pdf"
objectType="urn:uuid:7edca82f-054d-47f2-a032-9b2a5b5186c1"
lid="urn:uuid:744e9ad5-bc2d-453d-b20e-a91c6e33eaf1"
status="urn:oasis:names:tc:ebxml-regrep:StatusType:Approved"\>  
(...)  
   
      \<rim:Slot name="sourcePatientId"\>  
           
\<rim:ValueList\>  
              \<rim:Value\>  
             
  89765a87b^^^&1.2.3.4.5&ISO  
              \</rim:Value\>  
     
      \</rim:ValueList\>  
          \</rim:Slot\>  
(...)  
     
   \<rim:ExternalIdentifier
identificationScheme="urn:uuid:2e82c1f6-a085-4c72-9da3-8640a32e42ab"
value="1.2.42.20180828094414.4"
objectType="urn:oasis:names:tc:ebxml-regrep:ObjectType:RegistryObject:ExternalIdentifier"
id="urn:uuid:96e39549-887b-444d-9e10-a58708d63e71"
registryObject="urn:uuid:744e9ad5-bc2d-453d-b20e-a91c6e33eaf1"\>  
       
    \<rim:Name\>  
              \<rim:LocalizedString
value="XDSDocumentEntry.uniqueId"/\>  
            \</rim:Name\>  
   
        \<rim:VersionInfo versionName="-1"/\>  
         
\</rim:ExternalIdentifier\>  
        \</rim:ExtrinsicObject\>  
     
\</rim:RegistryObjectList\>  
    \</query:AdhocQueryResponse\>  
 
\</S:Body\>  
\</S:Envelope\>

</th></tr></table>

<table><tr><th>
Fehlercode

</th><th>
Beschreibung

</th><th>
Handlungsanweisung

</th></tr><tr><td>
XDSTooManyResults

</td><td>
Die Ergebnismenge der Suche ist zu groß. 

</td><td>
Die Suche verfeinern und neu durchführen bis das Aktensystem den Fehler nicht
mehr wirft. Die Reduktion von Metadaten-Suchergebnissen erfolgt gemäß A_16336.

</td></tr></table>

Durch die Einführung der Folder für jede Kategorie, also auch für solche der
Kategorie patientdoc, kann eine Suche mittels FindFolders auf
Dokumentenkategorie erfolgen, die in Folder.Codelist angegeben sind. 

Filtern

Die Metadaten der StoredQuery-Response sind geeignet, dem Nutzer weitere
Filtermöglichkeiten zu geben, um die Ergebnismenge der Dokumenten-Anzeige
einzuschränken. 

**A_15030 - Filteroptionen für den Nutzer**

Das PS MUSS mittels der Metadaten aus der StoredQuery-Response Filteroptionen
anbieten, mit denen Leistungserbringer die Ergebnismenge für die Anzeige von
Dokumenten einschränken können. **[\<=]**

**A_15087 - Identifizierung von LE-Dokumente in Ergebnismengen**

Eine metadatengestützte Sortierfunktion unterstützt das Filtern von
Dokumenten. Das PS SOLL eine Ergebnismenge unter Identifizierung der
LE-Dokumente einschränken können. **[\<=]**

### 5.2.3 Dokumente laden

Dr. Weber erkennt anhand der Metadaten aus seiner Dokumentensuche, dass in der
Akte von Frau Gundlach ein Arztbrief im eArztbrief-Format enthalten ist. Das
PVS zeigt Dr. Weber an, dass dieses Dokumentenformat strukturiert in die lokale
Patientenakte übernommen und dort verarbeitet werden kann. Dr. Weber wählt
dieses Dokument aus den Suchergebnissen aus, lässt es sich anzeigen und
speichert es in seine lokale Patientenakte.

Zur Umsetzung des AnwendungsfallesDokumente durch einen Leistungserbringer
anzeigenaus [gemSysL_ePA#3.7.9, UC 4.9 - Dokumente durch einen
Leistungserbringer anzeigen] wird Retrieve Document Set [ITI-43] profiliert.

**A_15651 - Funktionsmerkmal Dokumente laden**

Das PS MUSS es dem Leistungserbringer ermöglichen, ePA-Dokumente aus der Akte
in das PS laden zu können. Dafür MUSS das PS die
Konnektorschnittstellenoperation RetrieveDocumentSet verwenden. **[\<=]**

<table><tr><th>
IHE-Konzept

</th><th>
Wert

</th><th>
Referenz

</th></tr><tr><td>
PS als IHE Akteur

</td><td>
Document Consumer

</td><td>
Retrieve Document Set [ITI-43]

</td></tr><tr><td>
Format Ergebnis-Dokument(e)

</td><td>
XOP-Infoset

</td><td>
[IHE-ITI-TF2x#Appendix v.8]

</td></tr></table>

Das Fachmodul stellt kein Integrated Document Source/Repository und keine
On-Demand Document Source dar.

Das Anzeigen von Dokumenten beinhaltet auch das Anzeigen der Metadaten des
Dokumentes.

Das Anzeigen ist nicht zwingend mit dem persistenten Abspeichern des Dokumentes
verbunden.

Falls das anzuzeigende Dokument nicht schon mit seiner Dokumenten-ID bekannt
ist, und eine Liste vorliegt, soll das PS die Auswahl des anzuzeigenden
Dokumentes unter Auswertung von Metadaten ermöglichen.

Es lassen sich nur solche Dokumente laden, für welche die LEI über eine
Berechtigung verfügt.

### 5.2.3.1 Schnittstelle

Das Fachmodul ePA bietet zur logischen Schnittstelle I_PHR_Management am
WebservicePHR_Service(analog
IHE-DienstDocumentRepository)die OperationRetrieveDocumentSetan, die in ihrem
Außenverhalten der Schnittstellendefinition des [ITI-43] folgt und die Rolle
eines IHE ITIDocumentRepositorygegenüber dem PS übernimmt.

<table><tr><th>
Operationsname

</th><th colspan="2">
DocumentRepository_RetrieveDocumentSet [gemSpec_FM_ePA#7.1.1.3]

</th></tr><tr><td rowspan="2">
Aufrufparameter

</td><td>
Name

</td><td>
Implementierung

</td></tr><tr><td>
RetrieveDocumentSetRequest 

</td><td>
[ITI-43#3.43.4.1]

</td></tr><tr><td rowspan="2">
Rückgabeparameter

</td><td>
Name

</td><td>
Implementierung

</td></tr><tr><td>
RetrieveDocumentSetResponse 

</td><td>
[ITI-43#3.43.4.2] 

</td></tr></table>

### 5.2.3.2 Umsetzung

Die Aktivitäten des Anwendungsfalles Dokumente anzeigen sind:

Vorbedingung:

 ---> UL

Auslöser:

 ---> UL

Aktivitäten:

 ---> UL

Resultat:

 ---> UL

Beispiel#: Bsp_ILF_ePA_RetrieveDocumentSetRequest

<table><tr><th>
\<RetrieveDocumentSetRequest xmlns="urn:ihe:iti:xds-b:2007"\> 

\<DocumentRequest xmlns="urn:ihe:iti:xds-b:2007"\> 

\<HomeCommunityId\>urn:oid:1.2.276.0.76.3.1.315.3.2.1.1\</HomeCommunityId\> 

\<RepositoryUniqueId\>1.2.276.0.76.3.1.315.3.2.1.1\</RepositoryUniqueId\> 

\<DocumentUniqueId\>1.2.840.113556.1.8000.2554.17930.51373.54354.20040.33122.16728266.12168687\</DocumentUniqueId\>
 
\</DocumentRequest\>  
\</RetrieveDocumentSetRequest\>

</th></tr></table>

Beispiel#: Bsp_ILF_ePA_RetrieveDocumentSetResponse

<table><tr><th>
\<ns9:RetrieveDocumentSetResponse xmlns:ns9="urn:ihe:iti:xds-b:2007"
xmlns:ns8="urn:oasis:names:tc:ebxml-regrep:xsd:rs:3.0"
xmlns:ns7="urn:oasis:names:tc:ebxml-regrep:xsd:rim:3.0"
xmlns:ns6="http://ws.gematik.de/conn/ConnectorContext/v2.0"
xmlns:ns5="http://ws.gematik.de/conn/phrs/PHRManagementService/v1.3"
xmlns:ns4="http://ws.gematik.de/fa/phr/v1.1"
xmlns:ns3="http://ws.gematik.de/tel/error/v2.0"
xmlns:ns2="http://ws.gematik.de/conn/ConnectorCommon/v5.0"
xmlns:ns11="urn:oasis:names:tc:ebxml-regrep:xsd:lcm:3.0"
xmlns:ns10="urn:oasis:names:tc:ebxml-regrep:xsd:query:3.0"\> 

\<ns8:RegistryResponse
status="urn:oasis:names:tc:ebxml-regrep:ResponseStatusType:Success"/\> 

\<ns9:DocumentResponse\> 

\<ns9:HomeCommunityId\>urn:oid:1.2.276.0.76.3.1.315.3.2.1.1\</ns9:HomeCommunityId\>


\<ns9:RepositoryUniqueId\>1.2.276.0.76.3.1.315.3.2.1.1\</ns9:RepositoryUniqueId\>


\<ns9:DocumentUniqueId\>1.2.840.113556.1.8000.2554.17930.51373.54354.20040.33122.16728266.12168687\</ns9:DocumentUniqueId\>
 
\<ns9:mimeType\>application/xml\</ns9:mimeType\>  
\<ns9:Document\> 

\<xop:Include href="cid:85130d97-672a-4000-b09c-43a4ac630403%40null"
xmlns:xop="http://www.w3.org/2004/08/xop/include"/\>  
\</ns9:Document\> 

\</ns9:DocumentResponse\>  
\</ns9:RetrieveDocumentSetResponse\>

</th></tr></table>

### 5.2.3.3 Nutzung

Die Retrieve Document Set Request Message muss mindestens
eineDocumentUniqueIDenthalten.

Ein http-Request im MTOM/XOP - Format (type="application/xop+xml") führt zu
einer MTOM-Response.

**A_16519 - Größenbeschränkung beim Laden von Dokumentensätzen**

DasDokumente Ladenunterliegt der Beschränkung der Gesamtgröße einer
Dokumentenmenge, die mit einem einzelnen Aufruf geladen werden können. Das PS
MUSS beachten, dass die in den Dokument-Metadatensizeaufgeführte Größe der
Dokumente, die in der Response der Nachricht zu erwarten sind, in Summe 250 MB
nicht überschreiten darf, um eine Fehlermeldung des Fachmodules oder des
Aktensystems zuverlässig zu vermeiden.  **[\<=]**

Dokumente werden in das ePA-Aktensystem Ende-zu-Ende verschlüsselt eingestellt.
Dadurch können die Dokumente nicht an zentraler Stelle auf mögliche
Schadsoftware geprüft werden. Eine Absicherung gegen mögliche Schadsoftware
in heruntergeladenen Dokumenten muss im Primärsystem erfolgen.

**A_17769 - Schutzmaßnahmen nach Plausibilitätsprüfungen an heruntergeladenen
Dokumenten**

Das PS SOLL Maßnahmen zur Absicherung gegen mögliche Schadsoftware in
heruntergeladenen Dokumenten ergreifen, falls:

 ---> UL

**[\<=]**

**A_17770 - Maßnahmen zum Schutz vor heruntergeladenen Dokumenten**

Das PS MUSS bei Anzeige oder persistenter Speicherung eines heruntergeladenen
Dokumentes sicherstellen, dass geeignete Maßnahmen zum Schutz von PS und
LE-Umgebung durchgeführt werden.  **[\<=]**

Geeignet wären insbesondere folgende Maßnahmen:

 ---> UL

**A_15089 - Protokollierung einer Dokumentenanzeige im Übertragungsprotokoll**

Das Anzeigen von Dokumenten MUSS als Übertragung eines Dokumentes aus der ePA
in das PS im Übertragungsprotokoll vermerkt werden. **[\<=]**

**A_16198 - Prüfung der Zuordnung von Dokument zu Akte**

DiePatientIdenthält die Versicherten-ID und SOLL vom PS zur Überprüfung
verwendet werden, ob das angezeigte Dokument vor einem möglichen Abspeichern
dem richtigen Versicherten bzw. der richtigen lokalen Patientenakte zugeordnet
ist.  **[\<=]**

**A_16196 - Verarbeitung strukturierter Inhalte**

Das PS SOLL nach Möglichkeit in der Lage sein, aus ePA-Dokumenten, deren
Inhalte strukturiert vorliegen, die strukturierten Inhalte in die
Primärdokumentation des Versicherten zu übernehmen.  **[\<=]**

### 5.2.4 Dokumente löschen

Dr. Weber stellt fest, dass Frau Gundlach keine Medikamente mehr benötigt,
setzt diese ab und löscht in Absprache mit ihr den elektronischen
Medikationsplan aus ihrer Akte. Frau Gundlach hat kein Interesse daran,
überholte Versionen des eMP in der ePA zu archivieren. 

Zur Umsetzung des Anwendungsfalles Dokumente durch einen Leistungserbringer
löschenaus [gemSysL_ePA#3.7.7, UC 4.7 - Dokumente durch einen
Leistungserbringer löschen] wird Remove Metadata [ITI-62] profiliert.

**A_14247-04 - Funktionsmerkmal Dokumente Löschen**

Das PS MUSS es dem LE ermöglichen, dem Wunsch des Versicherten nach Löschung
von Dokumenten entsprechen zu können. Dafür MUSS das PS die
Konnektorschnittstellenoperation RemoveMetadataverwenden. Technische Dokumente
der ePA (Policy-Dateien) können nicht vom LE gelöscht werden.  **[\<=]**

Das Löschen eines Dokumentes aus einer ePA wird als ein strukturierter
Anwendungsfall realisiert, dem unmittelbar ein Suchen des Dokumentes
vorhergeht, so dass vom Fachmodul eine Aktensession eröffnet wurde, die vom
Löschen nachgenutzt wird. 

<table><tr><th>
IHE-Konzept

</th><th>
Wert

</th><th>
Referenz

</th></tr><tr><td>
PS als IHE Akteur

</td><td>
Document Administrator

</td><td>
Remove Metadata [ITI-62]

</td></tr></table>

Ein LE kann alle Dokumente in Rücksprache mit dem Versicherten löschen, für
die er Zugriffsrechte gemäß Tab_ILF_ePA_Zugriffsberechtigungen erhalten hat.

Der Aktenanbieter löscht mit den Dokumenten auch die Metadaten des Dokumentes.

Für das nach der Löschung des Dokumentes in der ePA gegebenenfalls in der
Primärdokumentation des Leistungserbringers verbleibende Dokument sind die in
Kap. 7.1 aufgeführten Empfehlungen zur Archivierung zu beachten.

Das direkte Löschen von Ordnern für den Versicherten ist keine UseCase für
das PS.

### 5.2.4.1 Schnittstelle

Das Fachmodul ePA bietet zur logischen Schnittstelle I_PHR_Management am
WebservicePHR_Service(analog IHE-DienstDocumentRegistry)die
OperationRemoveMetadata an, die in ihrem Außenverhalten der
Schnittstellendefinition des [ITI-62] folgt und die Rolle einer
IHEDocumentAdministratorgegenüber dem PS übernimmt.

<table><tr><th>
Operationsname

</th><th colspan="2">
DocumentRegistry_RemoveMetadata [gemSpec_FM_ePA#7.1.1.6]

</th></tr><tr><td rowspan="2">
Aufrufparameter

</td><td>
Name

</td><td>
Implementierung

</td></tr><tr><td>
RemoveObjectsRequest 

</td><td>
[IHE-ITI-RMD#3.62.4.1]

</td></tr><tr><td rowspan="2">
Rückgabeparameter

</td><td>
Name

</td><td>
Implementierung

</td></tr><tr><td>
RegistryResponse

</td><td>
[IHE-ITI-RMD#3.62.4.2]

</td></tr></table>

### 5.2.4.2 Umsetzung

Die Aktivitäten des Anwendungsfalles Dokumente löschen sind:

Vorbedingung:

 ---> UL

Auslöser:

 ---> UL

Aktivitäten:

 ---> UL

Resultat:

 ---> UL

### 5.2.4.3 Nutzung

Der RMD-Request MUSS enthalten:

 ---> UL

### 5.2.5 Artefakte

### 5.2.5.1 Namensräume

<table><tr><th>
Präfix

</th><th>
Namensraum

</th></tr><tr><td>
ds

</td><td>
http://www.w3.org/2000/09/xmldsig

</td></tr><tr><td>
ec

</td><td>
http://www.w3.org/2001/10/xml-exc-c14n#

</td></tr><tr><td>
wst

</td><td>
http://docs.oasis-open.org/ws-sx/ws-trust/200512

</td></tr><tr><td>
wsu

</td><td>
http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd 

</td></tr><tr><td>
xsi

</td><td>
http://www.w3.org/2001/XMLSchema-instance   

</td></tr><tr><td>
fed

</td><td>
http://docs.oasis-open.org/wsfed/federation/200706

</td></tr><tr><td>
wsp

</td><td>
http://schemas.xmlsoap.org/ws/2004/09/policy 

</td></tr><tr><td>
wsa

</td><td>
http://www.w3.org/2005/08/addressing

</td></tr><tr><td>
xds

</td><td>
urn:ihe:iti:xds-b:2007  

</td></tr><tr><td>
rmd

</td><td>
urn:ihe:iti:rmd:2017 

</td></tr><tr><td>
rim

</td><td>
urn:oasis:names:tc:ebxml-regrep:xsd:rim:3.0 

</td></tr><tr><td>
lcm

</td><td>
urn:oasis:names:tc:ebxml-regrep:xsd:lcm:3.0 

</td></tr><tr><td>
query

</td><td>
urn:oasis:names:tc:ebxml-regrep:xsd:query:3.0 

</td></tr><tr><td>
soap12 

</td><td>
http://www.w3.org/2003/05/soap-envelope  

</td></tr></table>

### 5.2.5.2 WSDLs und Schemata

Die normativen WSDLs und Schemata der ePA werden von der gematik zur Verfügung
gestellt.

Für den Fall, dass es sich dabei um IHE-Artefakte handelt, gilt, dass diese
Artefakte denjenigen entsprechen, die von IHE im entsprechenden Zeitraum
bereitstellt. 

### 5.2.6 Testunterstützung

Zur Unterstützung von Tests im Zusammenhang mit den oben geschilderten
Funktionsmerkmalen dürfen keine Echtdaten verwendet werden.

### 5.3 Protokolle und Benachrichtigungen

### 5.3.1 Benachrichtigungen erhalten

Frau Gundlach hat Herrn Dr. Weber angekündigt, sie werde ihm in Kürze eine
Zugriffsberechtigung von ihremePA-Frontend des Versicherten aus erteilen (ihre
eGK führte sie für die Ad-hoc-Berechtigung nicht mit sich). Am folgenden Tag
findet sie am Frontend des Versicherten ihren Hausarzt Dr. Weber über den
Verzeichnisdienst und erteilt ihm eine Berechtigung für einen 7-Tage-Zugriff
(Default-Zeitraum) auf ihre ePA. Ein Mitarbeiter von Dr. Weber öffnet die
Primärakte von Frau Gundlach und erhält dabei die Benachrichtigung, dass Dr.
Weber eine Zugriffsberechtigung erhalten hat und dass der Facharzt, zu dem er
Frau Gundlach überwiesen hatte, einen eArztbrief in die Patientenakte
eingestellt hat.

Zur Umsetzung des UseCases "Benachrichtigungen durch einen LE verwalten" aus
[gemSysL_ePA#3.8.1] gibt es keine dedizierte Konnektorschnittstelle, auch nicht
zur dedizierten Abfrage der Zugriffsrechte, über die ein LE verfügt.
Stattdessen setzt sich das Funktionsmerkmal aus einer Reihe von
Informationsquellen zusammen, die gesamthaft eine zuverlässige
Informationsgrundlage bieten können, die jedoch keine Vollständigkeit
beanspruchen kann. 

Die Benachrichtigungsverwaltung kann aus dem Vergleich der Werte des
Zugriffsberechtigungsstatus und der Info-Quellen einen Vergleich über
Änderungen ziehen und über diese Änderungen den LE geeignet informieren.

Benachrichtigungen über Änderungen an der ePA eines Versicherten können aus
folgenden Quellen stammen:

<table><tr><th>
Kürzel

</th><th>
Beschreibung

</th><th>
Verweis

</th></tr><tr><td>
Quelle_Ad-hoc

</td><td>
Ausstellen von Ad-hoc-Berechtigungen zu einem Versicherten

</td><td>
Kap. 5.1.3

</td></tr><tr><td>
Quelle_GetAuthorizationList

</td><td>
Aufruf der Operation

GetAuthorizationList

()

</td><td>
Kap. 5.3.1.2

</td></tr><tr><td>
Quelle_getAll

</td><td>
Register Stored Query

GetAll

in

Dokumente suchen

</td><td>
Kap. 5.2.2

</td></tr><tr><td>
Quelle_Event

</td><td>
Info/Event im Systeminformationsdienst

</td><td>
Kap. 5.3.1.3

</td></tr><tr><td>
Quelle_Fehler

</td><td>
Spezielle Fehler melden den Entzug einer Berechtigung

</td><td>
Kap. 5.3.1.4

</td></tr></table>

Die Dokumentation durchgeführter Ad-hoc-Berechtigungen ergibt kein
vollständiges Bild der erteilten Zugriffsberechtigungen, da
Zugriffsberechtigungen für die LEI auch vom ePA-Frontend des Versicherten
heraus erteilt werden können.

**A_14351 - Benachrichtigung über ePA-Änderungen bei Auswahl des Versicherten**

Falls die Benachrichtigungsfunktion aktiviert ist, MUSS das PS
Leistungserbringer (sowie ihre Gehilfen) bei Auswahl einer Ansicht mit
Versichertenbezug in Bezug auf diesen Versicherten in folgenden Konstellationen
(ein- und abschaltbar, mit Einstellbarkeit der Frequenz der
Benachrichtigung) informieren können: 

 ---> OL

Tabelle30: Tab_ILF_ePA_Benachrichtigungs_InfoModell

<table><tr><th>
Kürzel

</th><th>
Beschreibung

</th><th>
Benachrichtigungsquellen

</th><th>
Datentyp

</th></tr><tr><td>
Info_Neu_Zugriff

</td><td>
Info über (neu) erhaltene Akten-Zugriffsberechtigungen

</td><td>
Quelle_Ad-hoc, Quelle_GetAuthorizationList, Quelle_getAll, Quelle_Event

</td><td>
RecordIdentifier

</td></tr><tr><td>
Info_Ende_Zugriff

</td><td>
Info über das Ende der Zugriffsberechtigung auf eine Akte (

ExpirationDate

\< heute)

</td><td>
Quelle_Ad-hoc, Quelle_GetAuthorizationList, Quelle_getAll,
Quelle_Event, Quelle_Fehler 

</td><td>
date

</td></tr><tr><td>
Info_Neu_Doc

</td><td>
Info über neu in eine Akte eingestellte Dokumente

</td><td>
Quelle_getAll, Quelle_Event

</td><td>
DocumentUniqueId

</td></tr><tr><td>
Info_Lösch_Doc

</td><td>
Info über gelöschte Dokumente

</td><td>
Quelle_getAll, Quelle_Fehler

</td><td>
DocumentUniqueId

</td></tr></table>

**[\<=]**

Handlungsanweisungen auf Basis der Informationen von
Tab_ILF_ePA_Benachrichtigungs_InfoModell:

 ---> UL

Das Erhalten von Berechtigung ist die Nachbedingung der Anwendungsfälle
"Berechtigung durch einen Versicherten vergeben" aus [gemSysL_ePA#3.6.1] und
"Bestehende Berechtigungen durch einen Versicherten verwalten"
[gemSysL_ePA#3.6.6].

### 5.3.1.1 Info-Quelle ePA-Administration

Im Rahmen der Ad-hoc-Berechtigung wird derRecordIdentifierbekannt, für den eine
Zugriffsberechtigung erteilt wird, und dasExpirationDateder
Zugriffsberechtigung (Quelle_Ad-hoc). Als alleinige Quelle dieser
Informationen ist die Ad-hoc-Berechtigung u.a. deswegen nicht geeignet, weil
der Versicherte vom ePA- Frontend des Versicherten ebenfalls
Zugriffsberechtigungen erteilen kann.

**A_15656 - Nutzung Ad-hoc-Berechtigung Erteilen für die
Benachrichtigungsverwaltung**

Das PS MUSS das FunktionsmerkmalAktenkonto Aktivierennutzen, um für die  im
Erfolgsfalle zu einem RecordIdentifierdasExpirationDate für die
Benachrichtigungsfunktion zu erhalten. **[\<=]**

### 5.3.1.2 Info-Quelle Berechtigungs-Abfrage

Durch Aufruf der Operation PHRManagementService::GetAuthorizationListerhält
das PS eine Liste sämtlicher zum Zeitpunkt der Abfrage vorliegenden
RecordIdentifier, auf die die LEI zugriffsberechtigt ist, sowie das jeweilige
Ablaufdatum der Zugriffsberechtigung. 

Der LE erhält über die Schnittstelle nicht nur Kenntnis über
Zugriffsberechtigungen, die in der Ad-hoc-Autorisierung in seiner LEI erteilt
wurden, sondern auch über Zugriffsberechtigungen, die vom ePA-Frontend des
Versicherten aus erteilt oder geändert wurden.

Nutzungsvoraussetzungen:

 ---> UL

<table><tr><th>
Operationsname

</th><th colspan="2">
GetAuthorizationList [gemSpec_FM_ePA#7.2.1.5]

</th></tr><tr><td rowspan="2">
Aufrufparameter

</td><td>
Name

</td><td>
Implementierung

</td></tr><tr><td>
Context

</td><td>
 Aufrufkontext gemäß [ConnectorContext.xsd], s. [gemILF_PS#3.3.1]

</td></tr><tr><td rowspan="3">
Rückgabeparameter

</td><td>
Name

</td><td>
Implementierung

</td></tr><tr><td>
AuthorizationList

</td><td>
Liste aller Zugriffsberechtigungen für die LEI

</td></tr><tr><td>
Status

</td><td>
Status nach [gemSpec_Kon#3.5.2] zur Information im PS.

</td></tr></table>

![Abbildung-9][Abbildung-9]

DieAuthorizationListals Liste von Tupeln ausRecordIdentifierund Ablaufdatum der
Zugriffsberechtigung erlaubt die Aktualisierung vonInfo_Neu_Zugriff(über
denRecordIdentifier) und Info_Ende_Zugriff(über dasvalidTo-Element), indem
die Liste derAuthorizationEntry-Elemente mit der Liste der bisher schon
bekannten Berechtigungen auf Aktenzugriff verglichen wird.

![Abbildung-10][Abbildung-10]

**A_17143 - Nutzung von GetAuthorizationList für die
Benachrichtigungsverwaltung**

Das PS MUSS regelmäßige Änderungsabfragen
mit GetAuthorizationList initiieren, um  die Liste der Tupel
aus RecordIdentifierundExpirationDate seiner Berechtigungen zu erhalten, mit
denen die zur Verwaltung der Benachrichtigungen aktualisiert wird.  **[\<=]**

**A_19008 - Einschränkung der Häufigkeit der Abfrage getAuthorizationList**

Das PS DARF den Request getAuthorizationList NICHT öfter als einmal in 10
Minuten stellen. Häufigere Abfragen werden mit dem Fehler 7231 abgewiesen. Die
Häufigkeit der Abfrage sollte durch den Nutzer konfigurierbar sein, falls sie
automatisiert in einem festen Intervall erfolgt. **[\<=]**

Falls dieAuthorizationListVersicherten-IDs enthält, die dem Primärsystem nicht
bekannt sind, so dass sie keiner Primärdokumentation und keinem bestehenden
oder vergangenen Behandlungskontext entsprechen, so soll
dieserRecordIdentifier verworfen werden. Falls dieser noch unbekannte
Versicherte zu einem späteren Zeitpunkt eine neue Primärakte im PS erhält,
kann sein RecordIdentifier mitgetHomeCommunityIDermittelt werden. Die
Informationen der Tab_ILF_ePA_Benachrichtigungs_InfoModell werden dann wie
beiQuelle_getAllbeschrieben ermittelt, wo implizit auchQuelle_Eventausgewertet
werden kann, um die Benachrichtigungsinformationen zu vervollständigen. 

 

Das PS erhält Kenntnis vom Aktenanbieterwechsel eines Versicherten
überGetAuthorizationList. Sobald ein Versicherter den Aktenanbieter gewechselt
hat, wird der alteRecordIdentifier(zum alten Aktenanbieter) aus
derAuthorizationEntry-Liste entfernt. Beim Aktenanbieterwechsel wird die
Berechtigung der LEI in die neue Akte transferiert, so dass ein
neuerRecordIdentifierin derAuthorizationEntry-Liste erscheint. Anhand der
bekanntenInsurantIdkann das PS feststellen, dass der bekannte Versicherte die
Akte gewechselt hat, so dass der in der Primärakte für den Versicherten
dokumentierte RecordIdentifierim PS aktualisiert werden kann. 

### 5.3.1.3 Info-Quelle Dokumentensuche

Die Dokumentensuche mitGetAll(Quelle_getAll) liefert die umfangreichsten
Informationen für die Benachrichtigungsverwaltung, sollte aber aus
Performancegründen nicht zu oft für Änderungsabfragen verwendet werden.

Das PS erhält nur Kenntnis von solchen Dokumenten, für die es berechtigt ist.
Bei einer Änderung des Berechtigungstyps aus
Tab_ILF_ePA_Zugriffsberechtigungen kann sich auch die Ergebnismenge des Querys
ändern.

**A_14708 - Nutzung StoredQuery [ITI-18] für die Benachrichtigungsverwaltung**

Das PS MUSS dem Leistungserbringer die Möglichkeit geben, zur Verwaltung von
Benachrichtigungen gemäß dem in Kapitel 5.3.2 profilierten [ITI-18] die
StoredQueriesGetALL oder GetDocumentszu verwenden, um regelmäßige
Änderungsabfragen zu initiieren. **[\<=]**

**A_15654 - Keine regelmäßige Änderungsabfrage über sämtliche Versicherten
eines LE**

Das PS MUSS seine regelmäßigen Änderungsabfragen beschränken auf Akten zu
Primärdokumentationen, in denen Leistungserbringer aktiv arbeiten.
Eine regelmäßige Änderungsabfrage mittels StoredQuery über sämtliche
Versicherte einer LE-Umgebung DARF NICHT erfolgen.  **[\<=]**

### 5.3.1.4 Info-Quelle Systeminformationsdienst

Wenn das Fachmodul ePA den Leistungserbringer gegenüber der Akte eines
Versicherten erfolgreich autorisiert, erzeugt das Fachmodul ePA unter
Verwendung des Systeminformationsdienstes des Konnektors ein Event mit dem in
[gemSpec_FM_ePA#6.5.4] aufgeführten Inhalt ("Zugriffspolicy-Event"). Das
Zugriffspolicy-Event gibt Auskunft über den RecordIdentifier, für den eine
Zugriffsberechtigung erteilt wird, sowie über
dasExpirationDate(Quelle_Event). 

Das Zugriffspolicy-Event liefert zum aktuellen Zeitpunkt korrekte Informationen
und informiert somit über Aktualisierungen über Zugriffsberechtigungen, auch
solche, die der Versicherte am ePA-Frontend des Versicherten vorgenommen hat. 

Das Zugriffspolicy-Event wird implizit bei jedem Aktenzugriff am Fachmodul ePA
geworfen, der einen Zugriff auf den Berechtigungsschlüssel des LE erfordert,
z.B. wie beiQuelle_getAll beschrieben. 

**A_15655 - Nutzung Systeminformationsdienst für die
Benachrichtigungsverwaltung**

Das PS MUSS den Systeminformationsdienst des Konnektors nutzen, um zum
Topic FM_EPA/POLICY_LEIund derTelematikIDder Leistungserbringerinstitution das
Ablaufdatum der Zugriffsberechtigung für einenRecordIdentifierim
ElementvalidTo für die Benachrichtigungsfunktion zu erhalten.  **[\<=]**

### 5.3.1.5 Info-Quelle Fehlermeldung

**A_15657 - Nutzung von Fehlermeldungen für die Benachrichtigungsverwaltung**

Bei Auftreten der in Tab_ILF_ePA_Infoquelle_Fehlermeldung aufgelisteten
Fehlercodes MUSS das PS die geschilderten Handlungsweisen umsetzen. 

Tabelle32: Tab_ILF_ePA_Infoquelle_Fehlermeldung

<table><tr><th>
Fehlercode

</th><th>
Beschreibung

</th><th>
Handlungsanweisung

</th></tr><tr><td>
7209

</td><td>
Keine Berechtigung für das Aktenkonto vorhanden

</td><td>
Das PS MUSS den Ablauf der Zugriffsberechtigung bzw. die nicht vorliegende
Zugriffsberechtigung in der betroffenen lokalen Patientenakte für die
Benachrichtigungsfunktion kenntlich machen.

</td></tr><tr><td>
InvalidDocumentContent 

</td><td>
Dokument oder seine Metadaten sind fehlerhaft, daher ist das Dokument nicht
verfügbar

</td><td colspan="1" rowspan="2">
Dokument ist nicht verfügbar und in dieser Hinsicht als gelöscht anzusehen.
Als Info über gelöschte Dokumente in der Benachrichtigungsfunktion
verwenden.  

</td></tr><tr><td>
XDSDocumentUniqueIdError 

</td><td>
Dokument zur DokumentID ist nicht verfügbar. 

</td></tr></table>

**[\<=]**

### 5.3.1.6 Umsetzung

Die auch kombinierbaren Aktivitäten des Anwendungsfalles Benachrichtigungen
erhalten sind:

Vorbedingung:

 ---> UL

Auslöser:

 ---> UL

Aktivitäten:

 ---> UL

Resultat:

 ---> UL

![Abbildung-11][Abbildung-11]

### 5.3.1.7 Nutzung

**A_14659 - Speicherung RecordIdentifier in der lokalen Primärdokumentation des
PS**

Das PS MUSS den RecordIdentifier an der lokalen Patientenakte
(Primärdokumentation) persistent speichern, falls eine neu vergebene
Berechtigung für den LE ermittelt wurde.  **[\<=]**

**A_15100 - Auswahloptionen der Benachrichtigungsverwaltung**

Das PS SOLL dem LE Auswahloptionen für die Benachrichtigungsverwaltung
anbieten. **[\<=]**

Der StoredQueryGetDocumentsliefert aktuelle Metadaten für Dokumente, auf die
ein LE zugriffsberechtigt ist. Durch Nutzung
vonGetALL[ITI-18#3.18.4.1.2.3.7.4] werden die Metadaten aller XDSSubmissionSets
und XDSDocumentEntries eines Versicherten in einer Akte erfragt.

Suchstrategien aus der SchnittstelleRegistry Stored Querykönnen
Info_Neu_Zugriff und Info_Ende_Zugriff aktualisieren helfen, beispielsweise:

 ---> UL

Die Suche erfolgt auf den Metadaten von Dokumenten, nicht auf den
Dokumenteninhalten.

### 5.3.2 Übertragungsprotokolle speichern

Das Primärsystem von Dr. Weber speichert die Übertragungsprotokolle zwischen
dem Primärsystem und dem Konnektor, die darüber Auskunft geben, welche
Aktenzugriffe er auf Frau Gundlachs ePA vollzogen hat.

Das PS benutzt "Übertragungsprotokolle", um insbesondere die vorgeschriebenen
Nachweispflichten von Leistungserbringern bei der Übertragung von Dokumenten
zwischen PS und Aktensystem zu erfüllen, bei denen Patientendaten betroffen
sind. Das Erstellen, Speichern, Durchsuchbar machen und Anzeigen der
Übertragungsprotokolle zwischen PS und Aktensystem ist eine Aufgabe des PS,
nicht jedoch des Fachmoduls ePA oder anderer Komponenten der TI. Die
Übertragungsprotokolle geben Auskunft über die Aktivität des PS bei der
Nutzung der Akte, nicht aber über die Datenverarbeitung im Aktensystem des
Versicherten.

**A_16434 - Übertragungsprotokolle durchsuchbar und einsehbar speichern**

Das PS MUSS Übertragungsprotokolle der Kommunikation mit dem Fachmodul ePA des
Konnektors speichern, durchsuchbar und einsehbar machen. **[\<=]**

Das Format der Speicherung und die Schnittstellen zu den
Übertragungsprotokollen können herstellerspezifisch sein. Das PS kann zur
Speicherung zum Speichern Record Audit Event [ITI-20] verwenden, und darauf
aufbauende Filtermechanismen zur Anzeige der Übertragungsprotokolle verwenden.

Durch das Loggen der SOAP-Parameter aus  Tab_ILF_ePA_ClientInformationen bei
Dokumentenmanagementzugriffen werden für das Einsehen von
Übertragungsprotokollen erforderliche Zugriffsinformationen bereit gestellt.

Details zur Nutzung der Übertragungsprotokolle obliegen dem PS.

### 5.4 Status- und Fehlermeldungen

### 5.4.1 Statusinformationen

**A_14691 - Meldung über partielle Erfolgsmeldungen**

Das PS MUSS im Falle einer partiellen Erfolgsmeldung (oder eines vorliegenden
Warning-Elementes) eine Warnung bereitstellen, die es den Mitarbeitern der
Leistungserbringerinstitution ermöglichen, die Ursache des (partiellen)
Fehlers zu identifizieren und mögliche Gegenmaßnahmen zu ergreifen und die
partiellen Fehler vom partiellen Erfolg unterscheiden helfen.  **[\<=]**

<table><tr><th>
Wert

</th><th>
Beschreibung

</th><th>
Erläuterung

</th><th>
Beispiel Anzeigetext

</th></tr><tr><td>
W

</td><td>
Warning

</td><td>
Transaktion erfolgreich, jedoch gibt es Abweichungen

</td><td>
7402: Das Aktenkonto ist bereits eingerichtet

</td></tr><tr><td>
E

</td><td>
Error

</td><td>
Transaktion gescheitert

</td><td>
7409: Das Aktenkonto wurde aktiviert, aber die Wiederherstellungsschlüssel
konnten nicht am Aktensystem hinterlegt werden.

</td></tr></table>

[IHE-ITT-TF3] definiert, insbes. Table 4.2.4.2-3 und Table 4.2.4.2-4.

Bei IHE-Operationen stellt der in Im rs:RegistryResponse/@status Attribut den
Verarbeitungsstatus der Anfrage dar:

<table><tr><th>
Wert

</th><th>
Beschreibung

</th><th>
Erläuterung

</th><th>
Beispiel Anzeigetext

</th></tr><tr><td>
urn:oasis:names:tc:ebxml-regrep:ResponseStatusType:Success

</td><td>
[IHE-ITT-TF3]#Table 4.2.4.2-1, 4.2.4.2-3,4.2.4.2-4

</td><td>
Transaktion erfolgreich

</td><td>
Transaktion erfolgreich

</td></tr><tr><td>
urn:ihe:iti:2007:ResponseStatusType:PartialSuccess

</td><td>
[IHE-ITT-TF3]#Table 4.2.4.2-3,  4.2.4.2-4.

</td><td>
In der Response einer Transaktion sind Error-Elemente enthalten, mindestens
eines davon hat die Error Severity. Andere Teile der Transaktion sind
erfolgreich verlaufen.

</td><td>
Transaktion in Teilen erfolgreich

</td></tr><tr><td>
urn:oasis:names:tc:ebxml-regrep:ResponseStatusType:Failure

</td><td>
[IHE-ITT-TF3#Table 4.2.4.2-1, 4.2.4.2-3,4.2.4.2-4]

</td><td>
Transaktion gescheitert

</td><td>
Der ePA-Anwendungsfall konnte nicht erfolgreich beendet werden.

</td></tr></table>

### 5.4.2 Fehlerbehandlung

Auftretende Fehlertypen unterscheiden sich je nach Architekturebene:

 ---> UL

<table><tr><th>
Aspekt

</th><th>
TelematikError

</th><th>
IHE-Error

</th></tr><tr><td>
Fehlercodes

</td><td>
als Nummer

</td><td>
als String mit Kurzbeschreibung

</td></tr><tr><td>
Fehlerlisten

</td><td>
Fehler als Einzelobjekte ohne Trace

</td><td>
RegistryErrorList 

</td></tr><tr><td>
Kritikalität Warning

</td><td>
GERROR:Severity

 = "Warning"

</td><td>
RegistryErrorList.highestSeverity

="Warning"

</td></tr><tr><td>
Kritikalität Error

</td><td>
GERROR:Severity

 = "Error", "Fatal" 

</td><td>
RegistryErrorList.highestSeverit

y="Error"

</td></tr><tr><td>
SOAP-Fehlertyp

</td><td>
SOAP 1.1

</td><td>
SOAP 1.2

</td></tr></table>

**A_14179 - Verständliche Fehlermeldung**

Das PS MUSS im Falle von Fehlern Fehlermeldungen bereitstellen, die es den
Mitarbeitern der Leistungserbringerinstitution ermöglichen, die Ursache des
Fehlers zu identifizieren und mögliche Gegenmaßnahmen zu ergreifen. **[\<=]**

Der Stacktrace der Fehler wird nicht an das PS weitergegeben.

### 5.4.2.1 TelematikError

Im Falle von Nicht-IHE-Fehlern erhält das PS vom Fachmodul ePA einen Fehler
gemäß [gemSpec_OM#3.2.3], das ein einzelnesGERROR:Trace-Element enthält,
das in derGERROR-Struktur im Element GERROR:Trace einen von der gematik
spezifizierten Fehler enthält. 

Es gibt keinen Fehlertrace bei SOAP-Fehlern. Die Fehlerbehandlung durch das PS
MUSS auf Basis der Fehlerstruktur erfolgen. Herstellerspezifische
ePA-SOAP-Fehler sind nicht zulässig. Anforderungen an das PS
zum Fehlerhandling bei SOAP-Fehlern finden sich in [gemILF_PS#6].

Die vom FM geworfenen Fehler sind gelistet in Tab_ILF_ePA_Fehlermeldungen des
Fachmoduls ePA.

Daneben kann es Fehler des Basiskonnektors geben gemäß [gemSpec_Kon], s.
Übersicht in [gemILF_PS#6.6]

**A_16205 - Fehlertexte aus dem TelematikError zur Anzeige von Fehlertexten**

Das PS SOLL bei Auftreten einesTelematikErrorsdenCodeund den ErrorText zur
Anzeige der Fehlermeldungen verwenden.  **[\<=]**

### 5.4.2.2 IHE-Error

In der Response der IHE-Schnittstellen-Aufrufe können [ITI-TF-3#Table
4.2.4.1-2]: Error Codes auftreten, die drei ResponseStatusType aufweisen
können.

Das Vorhandensein eine Error-List ist prinzipiell vereinbar mit einer teilweise
erfolgreichen Verarbeitung. Falls die ErrorList nur Warnings enthält
(RegistryError elements mit warning severity, aber ohne error severity), kann
die Verarbeitung als erfolgreich angesehen werden.

Fehler aus Aufrufen des Dokumentenmanagements haben das in [ITI TF Vol 3#4.2.4]
"Success and Error Reporting" beschriebene Format. Es wird im Fehlerfall ggf.
eine Fehlerliste (RegistryErrorList) und darin Fehler (RegistryError) mit den
AttributenerrorCode,errorContextundseverityzurückgegeben. 

**A_14920 - Fehlertexte aus der RegistryErrorList zur Anzeige von Fehlertexten**

Das PS SOLL für Fehler aus derRegistryErrorList eine deutschsprachige
Fehlermeldung erstellen. **[\<=]**

**A_15092 - Eigene Übersetzungen von Fehlertexten**

Das PS KANN die IHE-Error-Fehlertexte mit eigenen Übersetzungen zur Anzeige
bringen. Andernfalls KANN der Fehlertext für Fehler, bei denen keine
Handlungsanweisung besteht, mit dem generischen Fehlertext "Der
ePA-Anwendungsfall konnte nicht erfolgreich beendet werden." zur Anzeige
gebracht werden. **[\<=]**

### 5.4.3 Handlungs-Empfehlungen in Fehlerfällen

**A_15632-04 - Empfehlungen zur Fehlerbehandlung**

Bei Auftreten der in Tab_ILF_ePA_Handlungsanweisung_im_Fehlerfall aufgelisteten
Fehlercodes SOLL das PS die geschilderten Handlungsweisen unterstützen.

Tabelle36: Tab_ILF_ePA_Handlungsanweisung_im_Fehlerfall

<table><tr><th>
Fehler-code

</th><th>
Fehlertext

</th><th>
Handlungsanweisung

</th></tr><tr><td>
7207

</td><td>
PIN Verifikation gescheitert

</td><td colspan="1">
Das PS soll den LE darüber informieren, dass der Versicherte seine PIN-Eingabe
wiederholen soll.   
Wenn die PIN-Eingabe ein weiteres Mal scheitert, sollte
darauf hingewiesen werde, dass nach dem dritten fehlerhaften Versuch die PIN
gesperrt wird und nur über die PUK am

ePA-

Frontend des Versicherten freigeschaltet werden kann.

</td></tr><tr><td>
4063

</td><td>
PIN gesperrt

</td><td>
Das PS soll den LE darüber informieren, dass der Versicherte die PIN mit seiner
PUK am

ePA-

Frontend des Versicherten entsperren sol. 

</td></tr><tr><td>
7231

</td><td>
Die Abfrage getAuthorizationList wurde zu häufig gestellt

</td><td>
Das PS soll den Nutzer auffordern, die Anfrage nicht zu häufig zustellen oder
den Administrator auffordern, das Anfrage-Intervall zu verlängern. 

</td></tr><tr><td>
7403

</td><td>
Das Aktenkonto kann noch nicht verwendet werden.

</td><td>
Das PS soll das Aktenkonto des Versicherten aktivieren (s. Kap. 5.1.2).

</td></tr><tr><td>
7209

</td><td>
Keine Berechtigung für das Aktenkonto vorhanden

</td><td>
Wenn ein ePA-Zugriff ausgeführt werden soll, und der Versicherte ist
einverstanden, eine Ad-hoc-Berechtigung auszuführen, soll die
Ad-hoc-Berechtigung beim ihm eingeholt werden. 

</td></tr><tr><td>
7205

</td><td>
Es konnte kein freigeschaltetes SM-B gefunden werden.

</td><td>
Das PS soll den Konnektoradministrator auffordern zu prüfen, ob eine SM-B im
Konnektor konfiguriert ist, diese ggf. konfigurieren, freischalten (lassen) und
Anwendungsfall wiederholen (lassen).

</td></tr><tr><td>
7401  
7403, 7404, 7405 

</td><td>
s. Tab_ILF_ePA_Fehlermeldungen des Fachmoduls ePA

</td><td>
Das PS soll den LE darüber informieren, dass der Versicherte den Anwendungsfall
zu einem späteren Zeitpunkt wiederholen soll. 

</td></tr></table>

**[\<=]**

**A_15632-02 - Empfehlungen zur Fehlerbehandlung**

Bei Auftreten der in Tab_ILF_ePA_Handlungsanweisung_im_Fehlerfall aufgelisteten
Fehlercodes SOLL das PS die geschilderten Handlungsweisen unterstützen.

Tabelle37: Tab_ILF_ePA_Handlungsanweisung_im_Fehlerfall

<table><tr><th>
Fehler-code

</th><th>
Fehlertext

</th><th>
Handlungsanweisung

</th></tr><tr><td>
7207

</td><td>
PIN Verifikation gescheitert

</td><td colspan="1">
Das PS soll den LE darüber informieren, dass der Versicherte seine PIN-Eingabe
wiederholen soll.   
Wenn die PIN-Eingabe ein weiteres Mal scheitert, sollte
darauf hingewiesen werde, dass nach dem dritten fehlerhaften Versuch die PIN
gesperrt wird und nur über die PUK am

ePA-

Frontend des Versicherten freigeschaltet werden kann.

</td></tr><tr><td>
4063

</td><td>
PIN gesperrt

</td><td>
Das PS soll den LE darüber informieren, dass der Versicherte die PIN mit seiner
PUK am

ePA-

Frontend des Versicherten entsperren sol. 

</td></tr><tr><td>
7231

</td><td>
Die Abfrage getAuthorizationList wurde zu häufig gestellt

</td><td>
Das PS soll den Nutzer auffordern, die Anfrage nicht zu häufig zustellen oder
den Administrator auffordern, das Anfrage-Intervall zu verlängern. 

</td></tr><tr><td>
7403

</td><td>
Das Aktenkonto kann noch nicht verwendet werden.

</td><td>
Das PS soll das Aktenkonto des Versicherten aktivieren (s. Kap. 5.1.2).

</td></tr><tr><td>
7209

</td><td>
Keine Berechtigung für das Aktenkonto vorhanden

</td><td>
Aufruf von getHomeCommunityID zur Prüfung, ob die persistent im PS gespeicherte
HomeCommunityID aktualisiert werden muss, weil der Versicherte seinen
Aktenanbieter gewechselt hat.  
Falls bei Aktualisierung der HomeCommunityID
die erneut aufgerufene Operation dennoch scheitert, gilt für Anwendungsfälle
außer Ad-hoc-Berechtigung erteilen:  
Das PS soll den Ablauf der
Zugriffsberechtigung in der betroffenen lokalen Patientenakte kenntlich machen.
 
Wenn ein ePA-Zugriff ausgeführt werden soll, und der Versicherte ist
einverstanden, eine Ad-hoc-Berechtigung auszuführen, soll die
Ad-hoc-Berechtigung beim ihm eingeholt werden. 

</td></tr><tr><td>
7205

</td><td>
Es konnte kein freigeschaltetes SM-B gefunden werden.

</td><td>
Das PS soll den Konnektoradministrator auffordern zu prüfen, ob eine SM-B im
Konnektor konfiguriert ist, diese ggf. konfigurieren, freischalten (lassen) und
Anwendungsfall wiederholen (lassen).

</td></tr><tr><td>
7401  
7403, 7404, 7405 

</td><td>
s. Tab_ILF_ePA_Fehlermeldungen des Fachmoduls ePA

</td><td>
Das PS soll den LE darüber informieren, dass der Versicherte den Anwendungsfall
zu einem späteren Zeitpunkt wiederholen soll. 

</td></tr></table>

**[\<=]**

### 5.4.4 Übersicht möglicher Fehlermeldungen

### 5.4.4.1 Fehlermeldungen aus dem Fachmodul ePA

Das Primärsystem können neben Fehlermeldungen des Basiskonnektors auch solche
des Fachmoduls ePA erreichen:

<table><tr><th>
Code

</th><th>
Fehlertext

</th><th>
Referenz

</th></tr><tr><td>
106

</td><td>
Zertifikat ungültig

</td><td>
[gemSpec_OM#Tab_Gen_Fehler]

</td></tr><tr><td>
114

</td><td>
DF.HCA gesperrt

</td><td>
[gemSpec_OM#Tab_Gen_Fehler]

</td></tr><tr><td>
4000

</td><td>
Syntaxfehler beim Aufruf einer Operation

</td><td>
[gemSpec_Kon#TAB_KON_567]

</td></tr><tr><td>
4008

</td><td>
Karte nicht gesteckt

</td><td>
[gemSpec_Kon#TAB_KON_515]

</td></tr><tr><td>
4063

</td><td>
PIN gesperrt

</td><td>
[gemSpec_Kon#TAB_KON_089], 

Tab_ILF_ePA_Handlungsanweisung_im_Fehlerfall

</td></tr><tr><td>
4065

</td><td>
PIN transportgeschützt

</td><td>
[gemSpec_Kon#TAB_KON_089]

</td></tr><tr><td>
4093

</td><td>
Karte bereits exklusiv verwendet

</td><td>
[gemSpec_Kon#TAB_KON_824]

</td></tr><tr><td>
7200

</td><td>
Lokalisierung des Aktensystems fehlgeschlagen

</td><td>
</td></tr><tr><td>
7202

</td><td>
Verbindung zum Aktensystem fehlgeschlagen

</td><td>
</td></tr><tr><td>
7203

</td><td>
Die gegenseitige Authentisierung von eGK und SMC-B
(Card-to-Card-Authentisierung) ist gescheitert.

</td><td>
</td></tr><tr><td>
</td><td>
</td><td>
Tab_ILF_ePA_Handlungsanweisung_im_Fehlerfall

</td></tr><tr><td>
7205

</td><td>
Es konnte kein freigeschaltetes SM-B gefunden werden.

</td><td>
Tab_ILF_ePA_Handlungsanweisung_im_Fehlerfall

</td></tr><tr><td>
7206

</td><td>
Prüfung der Zugriffsberechtigung fehlgeschlagen

</td><td>
</td></tr><tr><td>
7207

</td><td>
PIN-Verifikation gescheitert 

</td><td>
Tab_ILF_ePA_Handlungsanweisung_im_Fehlerfall

</td></tr><tr><td>
7209

</td><td>
Keine Berechtigung für das Aktenkonto vorhanden

</td><td>
Tab_ILF_ePA_Handlungsanweisung_im_Fehlerfall

</td></tr><tr><td>
7211

</td><td>
Dokument überschreitet maximal zulässige Größe von 25 MB

</td><td>
</td></tr><tr><td>
7212

</td><td>
Summe der Dokumente überschreitet maximal zulässige Größe von 250 MB

</td><td>
</td></tr><tr><td>
7213

</td><td>
Sperrstatus des Zertifikats der eGK nicht ermittelbar

</td><td>
</td></tr><tr><td>
7214

</td><td>
Das Schlüsselmaterial der Akte entspricht nicht den Sicherheitsanforderungen.

</td><td>
</td></tr><tr><td>
7215

</td><td>
Fehler im Aktensystem - Die Operation konnte nicht durchgeführt werden.

</td><td>
</td></tr><tr><td>
7217

</td><td>
Die Operation wurde am Kartenterminal abgebrochen.

</td><td>
</td></tr><tr><td>
7220

</td><td>
Aktensystem nicht erreichbar

</td><td>
</td></tr><tr><td>
7290

</td><td>
Die Patientenakte konnte nicht gefunden werden

</td><td>
Operation GetHomeCommunityID

</td></tr><tr><td>
7291

</td><td>
Die Patientenakte konnte nicht eindeutig identifiziert werden.

</td><td>
Operation GetHomeCommunityID

</td></tr><tr><td>
7231

</td><td>
Die Abfrage getAuthorizationList wurde zu häufig gestellt.

</td><td>
Info-Quelle Berechtigungs-Abfrage, Tab_ILF_ePA_Handlungsanweisung_im_Fehlerfall 

</td></tr><tr><td>
7400

</td><td>
Fehler - Die Operation konnte nicht durchgeführt werden.

</td><td>
</td></tr><tr><td>
7401

</td><td>
Operation konnte nicht durchgeführt werden - Akte vorübergehend nicht
verfügbar.

</td><td>
Tab_ILF_ePA_Handlungsanweisung_im_Fehlerfall

</td></tr><tr><td>
7402

</td><td>
Das Aktenkonto ist bereits eingerichtet

</td><td>
Operation ActivateAccount

</td></tr><tr><td>
7403

</td><td>
Das Aktenkonto kann noch nicht verwendet werden.

</td><td>
Tab_ILF_ePA_Handlungsanweisung_im_Fehlerfall

</td></tr><tr><td>
7404

</td><td>
Das Aktenkonto existiert nicht (mehr) in diesem ePA-Aktensystem.

</td><td>
Tab_ILF_ePA_Handlungsanweisung_im_Fehlerfall

</td></tr><tr><td>
7405

</td><td>
Das Aktenkonto wurde bei diesem ePA-Aktensystem gekündigt, kann aber aktuell
noch benutzt werden.

</td><td>
Tab_ILF_ePA_Handlungsanweisung_im_Fehlerfall

</td></tr><tr><td>
7406

</td><td>
Das Aktenkonto wurde bei diesem ePA-Aktensystem gekündigt und ist nur noch für
einen Kontowechsel lesend zugreifbar.

</td><td>
</td></tr></table>

### 5.4.4.2 Fehlermeldungen aus dem Aktensystem ePA

Das Aktensystem kann mindestens die Fehler der Tabelle
Tab_ILF_ePA_IHE-Fehlermeldungen_Aktensystem werfen, die an das PS durchgereicht
werden.

<table><tr><th>
Code

</th><th>
Hinweis

</th><th>
Referenz

</th></tr><tr><td>
InvalidDocumentContent

</td><td>
Dokument passt nicht zu Metadaten

</td><td>
[IHE-ITI-TF3#4.2.4]

</td></tr><tr><td>
UnresolvedReferenceException

</td><td>
entryUUID kann nicht aufgelöst werden 

</td><td>
[IHE-ITI-TF3#4.2.4]

</td></tr><tr><td>
XDSDocumentUniqueIdError

</td><td>
uniqueId kann nicht aufgelöst werden 

</td><td>
[IHE-ITI-TF3#4.2.4]

</td></tr><tr><td>
XDSDuplicateUniqueIdInRegistry

</td><td>
uniqueId ist nicht eindeutig

</td><td>
[IHE-ITI-TF3#4.2.4]

</td></tr><tr><td>
XDSMissingDocument

</td><td>
Dokument zu den Metadaten fehlt

</td><td>
[IHE-ITI-TF3#4.2.4]

</td></tr><tr><td>
XDSMissingDocumentMetadata

</td><td>
Metadaten zum Dokument fehlen

</td><td>
[IHE-ITI-TF3#4.2.4]

</td></tr><tr><td>
XDSPatientIdDoesNotMatch

</td><td>
PatientID fehlt

</td><td>
[IHE-ITI-TF3#4.2.4]

</td></tr><tr><td>
XDSRegistryBusy 

</td><td>
Zu viele Aktivitäten in der Registry

</td><td>
[IHE-ITI-TF3#4.2.4]

</td></tr><tr><td>
XDSRepositoryBusy 

</td><td>
Zu viele Aktivitäten

</td><td>
[IHE-ITI-TF3#4.2.4]

</td></tr><tr><td>
XDSRegistryError 

</td><td>
interner Fehler

</td><td>
[IHE-ITI-TF3#4.2.4]

</td></tr><tr><td>
XDSRepositoryError 

</td><td>
interner Fehler

</td><td>
[IHE-ITI-TF3#4.2.4]

</td></tr><tr><td>
XDSRegistryMetadataError 

</td><td>
Fehlerhafte Metadaten

</td><td>
[IHE-ITI-TF3#4.2.4]

</td></tr><tr><td>
XDSRepositoryMetadataError 

</td><td>
Fehlerhafte Metadaten

</td><td>
[IHE-ITI-TF3#4.2.4]

</td></tr><tr><td>
XDSRegistryNotAvailable 

</td><td>
Fehler Zugriff Registry 

</td><td>
[IHE-ITI-TF3#4.2.4]

</td></tr><tr><td>
XDSRegistryOutOfResources 

</td><td>
Resourcenengpass

</td><td>
[IHE-ITI-TF3#4.2.4]

</td></tr><tr><td>
XDSRepositoryOutOfResources 

</td><td>
Resourcenengpass

</td><td>
[IHE-ITI-TF3#4.2.4]

</td></tr><tr><td>
XDSStoredQueryMissingParam 

</td><td>
Parameterfehler Stored Query

</td><td>
[IHE-ITI-TF3#4.2.4]

</td></tr><tr><td>
XDSStoredQueryParamNumber 

</td><td>
Parameterfehler Stored Query

</td><td>
[IHE-ITI-TF3#4.2.4]

</td></tr><tr><td>
XDSTooManyResults

</td><td>
</td><td>
Tab_ILF_ePA_Fehlerbehandlung_Dokumente_Suchen

</td></tr><tr><td>
XDSUnknownStoredQuery 

</td><td>
Fehlerhafte Stored Query

</td><td>
[IHE-ITI-TF3#4.2.]

</td></tr><tr><td>
MAX_DOC_SIZE_EXCEEDED

</td><td>
Die max. Dokumentengröße wurde überschritten.

</td><td>
Bei Verletzung von A_16197, vgl. auch [gemSpec_Dokumentenverwaltung#Operation
Cross-Gateway Document Provide#Technische Fehlermeldungen] 

</td></tr><tr><td>
ACCESS_DENIED

</td><td>
Der Zugriff für diese Operation konnte nicht gewährt werden.

</td><td>
Der Nutzer hat nicht die erforderliche Berechtigung für die Operationen der
[gemSpec_Dokumentenverwaltung]: 

 ---> UL

</td></tr><tr><td>
MAX_PKG_SIZE_EXCEEDED

</td><td>
Die max. Paketgröße wurde überschritten.

</td><td>
Bei Verletzung von A_16519, vgl. auch
[gemSpec_Dokumentenverwaltung#OperationCross-Gateway Retrieve#Technische
Fehlermeldungen] 

</td></tr></table>

### 6 Informationsmodell

### 6.1 Metadaten

Beim Einstellen von Dokumenten in die ePA werden die dazu genutzten
SubmissionSets und die Dokumente selbst, durch Metadaten angereichert die für
Such- und Filterfunktionen nachgenutzt werden können. Metadaten liegen sowohl
am SubmissionSet, als auch am ePA-Dokument selbst vor. 

Das PS MUSS Metadaten unter Beachtung von [gemSpec_DM_ePA] möglichst
automatisiert aus den Primärdaten der Versicherten übernehmen und erzeugen,
ohne dass eine händische Eingabe von Metadaten zwingend erforderlich ist. Die
manuelle Auszeichnung der Werte von Metadaten sollte auf ein Minimum begrenzt
werden. 

Als Codierung wird UTF-8 verwendet.

**A_14940 - Festlegungen zu Metadaten im Datenmodells der ePA-Dokumente**

Das PS MUSS dieDokumententypen aus [gemSpec_DM_ePA#A_14760] betreffenden
Festlegungen zur Verwendung von Metadaten gemäß [gemSpec_DM_ePA#3.3]
beachten. **[\<=]**

### 6.2 Selbstauskunft

**A_15086-04 - Selbstauskunft der LE-Institution**

Das PS MUSS dem LE die Möglichkeit zur Konfiguration von Metadaten geben, in
denen Leistungserbringer ihre LE-Institution und sich selbst als Akteure
beschreiben. Diese LE-Selbstbeschreibungen MUSS zur Befüllung der Metadaten
automatisiert herangezogen werden können und die in
Tabelle Tab_ILF_ePA_Datenfelder_Selbstauskunft aufgeführten Felder gemäß
[gemSpec_DM_ePA#A_14760] umfassen. SubmissionSet.authorPersonMUSS mit Werten
des Einstellers belegt werden. Für den Fall, dass der LE eigene Dokumente
einstellt, MUSS die Selbstauskunft zusätzlich auch für die Belegung
vonDocumentEntry.authorPersonherangezogen werden. Da bei manchen
einzustellenden Dokumenten auch mehrere Autoren angegeben werden, MUSS die
Selbstauskunft mindestens mehrere Mitarbeiter der eigenen Institution umfassen
können.DieFachrichtung der erstellenden EinrichtungMUSS in der Selbstauskunft
im FeldpracticeSettingCode gespeichert werden mit einem zutreffenden Wert aus
[IHE-ITI-VS].Die Selbstauskunft MUSS einen einzelnen Code aus [Tab_DM_112:Codes
in ValueSet für Folder.codeList] setzen, um eine Voreinstellung für die
fachrichtungsspezifische ePA-Berechtigung vorzunehmen. Dieser
fachrichtungsspezifische Code beschreibt Daten zu Befunden, Diagnosen,
durchgeführten und geplanten Therapiemaßnahmen,
Früherkennungsuntersuchungen, zu Behandlungsberichten und sonstige
untersuchungs- und behandlungsbezogene medizinische Informationen.

Tabelle40: Tab_ILF_ePA_Datenfelder_Selbstauskunft

<table><tr><th>
Metadatum (Dokumentenmanagement)

</th><th>
Schnittstellenparameter (ePA-Administration)

</th><th>
Mult.

</th></tr><tr><td>
DocumentEntry.authorPerson

</td><td>
[1..*] 

</td></tr><tr><td>
DocumentEntry.authorInstitution

</td><td>
gemäß A_21209:  OrganizationName und Telematik-ID der Institution

</td><td>
1

</td></tr><tr><td>
DocumentEntry.authorRole

</td><td>
[0..*] 

</td></tr><tr><td>
DocumentEntry.authorSpecialty

</td><td>
[0..*] 

</td></tr><tr><td>
DocumentEntry.authorTelecommunication

</td><td>
[0..*] 

</td></tr><tr><td>
DocumentEntry.healthcareFacilityTypeCode

</td><td>
1

</td></tr><tr><td>
DocumentEntry.practiceSettingCode

</td><td>
[1..*] 

</td></tr><tr><td>
DocumentEntry.legalAuthenticator

</td><td>
 [0..*] 

</td></tr><tr><td>
DocumentEntry.languageCode

</td><td>
[1..*]

</td></tr><tr><td>
Folder.codeList

</td><td>
1

</td></tr></table>

**[\<=]**

Die Telematik-ID der Leistungserbringerinstitution muss in vielen Nachrichten
angegeben werden. Sie sollte aus der SMC-B ausgelesen werden. Die Telematik-ID
ist von den Kartenherausgebern der SM-B festgelegt und immer im Attribut
"registrationNumber" im Admission-Element der Extension der SMC-B-Zertifikate
(C.HCI.AUT, C.HCI.ENC,C.HCI.OSIG) eingetragen. Wenn nicht explizit vom
Antragsteller eine neue Telematik-ID angefordert wird, wird bei Ausgabe von
Folge- und Ersatzkarten die bisherige Telematik-ID wiederverwendet. Eine
generelle Vorgehensweise kann die gematik hierfür nicht geben, da die
Personalisierung der SMC-B sektoral unterschiedlich ist (siehe gemSpec_PKI,
Anhang A). Zum Auslesen der Zertifikate kann die Operation ReadCardCertificate
gemäß [gemSpec_Kon#4.1.9.5.2] verwendet werden. Die Telematik-ID ist in allen
Zertifikaten in der Admissionstruktur als "registrationNumber" im ASN.1-Format
gespeichert. 

### 6.3 Wertebereiche

Erforderliche Wertebereiche (Value Sets) für ePA-Dokumente werden je nach
Festlegung von [gemSpec_DM_ePA] in [IHE-ITI-VS] angegeben. 

Einstellen von Dokumenten

Auf die Auszeichnung von in die ePA einzustellenden Dokumenten durch Metadaten
kann das PS spezifische Einschränkungen und Vorbelegungen umsetzen:

 ---> UL

**A_15748-03 - Metadaten-Vorbelegungen bei Dokumenten, die nicht aus der eigenen
LEI stammen**

Für den Fall, dass LE der eigenen LE-Institution nicht die Autoren der
einzustellenden Dokumente sind, KANN das PS in seinen Dialogen zur Beschreibung
des Dokumenten-Autors und seiner Institution Auswahllisten von Wertebereiche
der Metadaten author, authorSpecialty, healthcareFacilityTypeCodeundpracticeSettingCodein
einer gemäß [gemSpec_DM#4.1] verkürzten Form zur Auswahl bringen. **[\<=]**

**A_16206-02 - Empfehlungen zur sektorspezifischen Reduktion von Auswahllisten**

Beim Einstellen von Dokumenten SOLLEN sektorspezifische Empfehlungen zur
Reduktion von Auswahllisten mögliche Werte für die
Metadaten authorRoleund typeCode beim Einstellen von Dokumenten gemäß
[gemSpec_DM_ePA#5.2.3] beachtet werden.  **[\<=]**

Auslesen von Dokumenten

Insoweit Metadaten zur Anzeige gebracht werden, muss das PS die Anzeigenamen der
Metadaten in eine lesbare Form bringen. Die Anzeige von Metadaten ist
insbesondere zu dem Zwecke des Filterns großer Ergebnismengen erforderlich
sowie zur Auswahl der gegebenenfalls herunterzuladenden Dokumente. Zum Filtern
über Dokumentenmengen kann es nützlich sein, nicht nur Metadaten
derDocumentEntries, sondern auch Metadaten derSubmissionSetsanzuzeigen, um ein
Ausblenden bestimmter Suchergebnisse zu ermöglichen. 

### 6.4 Dokumentenformate der ePA

**A_14245-01 - Unterstützung der Verarbeitung von Dokumentenformaten der ePA
durch das PS**

Das PS KANN über die Liste der in ePA definierten strukturierten Dokumente
gemäß [gemSpec_DM_ePA#A_14761] hinaus zusätzliche Dokumentenformate gemäß
[gemSpec_DM_ePA#A_14760] unterstützen, um sie zu verwalten.  **[\<=]**

Falls Word- oder Openoffice-Dokumente in die ePA eingestellt werden sollen,
müssen diese Dokumente vor ihrem Upload in ein PDF umgewandelt werden.

Das DPE-XML der eGK ist ein Beispiel eines XML-Dokumentes, dessen Metadaten
gemäß [gemSpec_DM_ePA] in [IHE-ITI-VS] angereichert werden. 

Ein ContentProfile zu einem einzelnen Dokumentenformat bzw. Inhaltstypen eines
Dokumentenformates beschreibt die Befüllung der Metadaten im Sinne einer Best
Practice zur Vermeidung von Interoperabilitätsproblemen. 

DerDocumentEntry.formatCode von Dokumenten, bei denen es kein Contentprofile
gibt, kann mit dem Wert  "urn:ihe:iti:xds:2017:mimeTypeSufficient" automatisch
vorbelegt werden. Eine manuelle Auswahl des formatCodessoll vermieden
werden.  

**A_21651 - Verarbeitung strukturierter Dokumente der gesetzlich vorgegebenen
Kategorien**

Das Primärsystem MUSS strukturierte Dokumente der Kategorien aus
Tab_DM_Dokumentenkategorien in gemSpec_DM_ePA#A_19388-* nicht nur anzeigen,
sondern auch verarbeiten können, d.h. anlegen und bearbeiten können.
Strukturierte Dokumente sind Dokumente, für die in gemSpec_DM
Strukturdefinitionen aufgeführt werden oder aber Definitionen als Medizinische
Informationsobjekte vorliegen. **[\<=]**

**A_14246 - Verarbeitbarkeit ausgelesener Dokumente und Formate**

Das Primärsystem MUSS anhand der Metadaten eines durch Dokumente
Suchenaufgefundenen  Dokumentes erkennen, ob es in der Lage ist, diese zu
verarbeiten, insbesondere anhand vonmimeType, formatCode,
classCodeundtypeCodedesDocumentEntry.  **[\<=]**

### 6.4.1 ContentProfile Notfalldatensatz und Datensatz Persönliche Erklärungen

Der Notfalldatensatz, der in die ePA eingestellt werden soll, wird vom PS
entweder zuvor gemäß [gemILF_PS_NFDM#5.1.2] von der eGK gelesen oder er wird
gemäß den im XML-Schema des Infomodells NFDM festgelegten Regeln und den
darüber hinaus gehenden in [gemSpec_InfoNFDM] definierten Integritätsregeln
erstellt, so dass der NFD gemäß [gemRL_QES_NFDM] signiert werden kann. 

Ein Datensatz persönliche Erklärungen (DPE), der in die ePA eingestellt werden
soll, wird vom PS entweder zuvor gemäß [gemILF_PS_NFDM#5.2.2] von der eGK
gelesen oder er wird  gemäß  den  im XML-Schema  des  Infomodells 
NFDM  festgelegten Regeln  und  den darüber hinaus gehenden in
[gemSpec_InfoNFDM] definierten Integritätsregeln erstellt. 

Im \<lcm:SubmitObjectsRequest\> des \<ProvideAndRegisterDocumentSetRequest\>
referenziert das \<rim:ExtrinsicObject\> die \<rim:RegistryObjectList\> die ID
des angehängten NFD-Objektes bzw. DPE-Objektes.

**A_18690 - DPE-spezifische Metadatenbefüllung**

Das PS KANN die Werte derSubmissionSet-Metadaten für den  Datensatz 
persönliche Erklärungen gemäß [gemSpec_DM_ePA] für das
Dokumentenmanagement der ePA automatisiert befüllen und dabei die
DPE-spezifischen Implementierungshinweise aus Tab_ILF_ePA_Nutzungsvorgaben
für Metadaten NFD/DPE beachten. Datenquellen sind Daten des Einstellers und
der DPE der eGK. **[\<=]**

**A_14504-01 - NFD-spezifische Metadatenbefüllung**

Das PS MUSS die Werte derSubmissionSet-Metadaten für den
Notfalldatensatz gemäß [gemSpec_DM_ePA] für das Dokumentenmanagement der
ePA automatisiert befüllen und dabei die
NFD-spezifischen Implementierungshinweise aus Tab_ILF_ePA_Nutzungsvorgaben
für Metadaten NFD/DPE beachten. Datenquellen sind Daten des Einstellers und
die NFD der eGK.

Tabelle41: Tab_ILF_ePA_Nutzungsvorgaben für Metadaten NFD/DPE

<table><tr><th colspan="2">
Metadatum XDS.b

</th><th>
Opt

</th><th>
Nutzungsvorgabe  
(Wertvorgabe oder Implementierungsanweisung)

</th></tr><tr><td colspan="4">
Metadatenelement DocumentEntry

</td></tr><tr><td colspan="2">
author

</td><td>
R

</td><td>
% 

</td></tr><tr><td>
authorPerson

</td><td>
O

</td><td>
Mögliche Quellen:

 ---> UL

</td></tr><tr><td>
authorInstitution

</td><td>
O

</td><td>
SubmissionSet.authorInstitution, falls Autor identisch mit Einsteller des
Dokumentes

</td></tr><tr><td>
authorRole

</td><td>
O

</td><td>
Einsteller des Dokumentes   
Verwendung gemäß [IHE-ITI-VS]  

</td></tr><tr><td>
authorSpecialty 

</td><td>
O

</td><td>
Einsteller des Dokumentes   
Verwendung gemäß [IHE-ITI-VS]   

</td></tr><tr><td>
authorTelecommunication

</td><td>
O

</td><td>
Einsteller des Dokumentes = SubmissionSet.authorTelecommunication 

</td></tr><tr><td colspan="2">
classCode

</td><td>
R

</td><td>
Codesystem, ID=1.2.276.0.76.11.32

 ---> UL

</td></tr><tr><td colspan="2">
creationTime

</td><td>
R

</td><td>
Mögliche Quellen (Mehrfachnutzung möglich):

 ---> UL

</td></tr><tr><td colspan="2">
formatCode

</td><td>
R

</td><td>
Codesystem= 1.3.6.1.4.1.19376.3.276.1.5.6 

Code=urn:gematik:ig:Notfalldatensatz:r3.1

</td></tr><tr><td colspan="2">
healthcareFacilityTypeCode

</td><td>
R

</td><td>
Einsteller des Dokumentes   
Der Wert MUSS aus [IHE-ITI-VS], Value Set
IHEXDShealthcareFacilityTypeCode gewählt werden.

</td></tr><tr><td colspan="2" rowspan="1">
mimeType

</td><td>
R

</td><td>
application/xml  

</td></tr><tr><td colspan="2">
practiceSettingCode

</td><td>
R

</td><td>
Einsteller des Dokumentes  
Der Wert MUSS aus [IHE-ITI-VS], Value
Set practiceSettingCode gewählt werden. 

</td></tr><tr><td colspan="2">
sourcePatientId

</td><td>
R

</td><td>
NFD signed NFD_Document.Versicherter.Versicherten_ID, falls diese mit der
Versicherten-ID der Primärdokumentation übereinstimmt, zur Übernahme gemäß
[gemSpec_DM_ePA]#2.1.4.6

</td></tr><tr><td colspan="2">
title

</td><td>
O

</td><td>
Notfalldatensatz (Nur für NFD)   
Datensatz persönliche Erklärungen (Nur
für DPE) 

</td></tr><tr><td colspan="2">
typeCode

</td><td>
R

</td><td>
Codesystem-ID=1.3.6.1.4.1.19376.3.276.1.5.9 

 ---> UL

</td></tr><tr><td colspan="4">
Metadatenelement SubmissionSet 

</td></tr><tr><td colspan="2">
contentTypeCode

</td><td>
R

</td><td>
Klinische Aktivität, die zum Einstellen des SubmissionSet geführt hat gemäß
[IHE-ITI-VS].  
Codesystem=1.3.6.1.4.1.19376.3.276.1.5.12  
Code=8

</td></tr></table>

**[\<=]**

Der Notfalldatensatz wird im Base64-Format, wie er aus der eGK ausgelesen wird,
in das Element \<xds:Document\> eingefügt, das ein Attribut @id enthält, das
dem rim:ExtrinsicObject/@id übereinstimmt.

**A_15058 - Anzeige (Rendering) ContentProfile NFD/DPE**

Das PS MUSS ePA-Daten im ContentProfile NFD/DPE in geeigneter Form zur Anzeige
bringen können. Für die Anzeige der Inhaltsdaten SOLL die Anzeigefunktion
der Notfalldaten bzw. des DPE nachgenutzt werden, die beim Auslesen der
NFD/DPE von der eGK gemäß [gemILF_PS_NFDM] verwendet wird, sofern die
Anzeigefunktion über die Anwendung NFDM verfügbar ist.  **[\<=]**

### 6.4.2 ContentProfile elektronischer Medikationsplan

Der elektronische Medikationsplan, der in die ePA eingestellt werden soll, wird
vom PS entweder zuvor gemäß [gemILF_PS_AMTS] von der eGK gelesen oder er wird
gemäß den im XML-Schema des Infomodells eMP/AMTS festgelegten Regeln und den
darüber hinaus gehenden in [gemSpec_Info_AMTS] definierten Integritätsregeln
erstellt, so dass der eMP durch das PS gemäß [gemILF_PS_AMTS] zum
Einstellen des eMP in die ePA vorbereitet ist. 

**A_21103 - Einstellen von eMP-Daten inklusive der Einwilligung**

Das PS MUSS dafür Sorge tragen, dass für den elektronischen Medikationsplan
der eGK sowohl das XML-Artefakt zum Medikationsplan, als auch das XML-Artefakt
zur Einwilligung des Versicherten gemäß [gemSpec_Info_AMTS#2.1] in einer
aktuellen Fassung in die ePA hochgeladen wird, falls die genannten Artefakte
dort fehlen oder nicht in einer aktuellen Version vorliegen.  **[\<=]**

**A_21102-01 - eMP-spezifische Metadatenbefüllung**

Das PS MUSS die Werte der Metadaten für den elektronischen Medikationsplan und
die zugehörige Einwilligung gemäß [gemSpec_DM_ePA] für das
Dokumentenmanagement der ePA automatisiert befüllen und dabei die
eMP-spezifischen Implementierungshinweise aus Tab_ILF_ePA_Nutzungsvorgaben
für Metadaten eMP sowie die ValueSetDefinition aus
 [IHE-ITI-VS] beachten. Datenquellen sind Daten des Einstellers oder
eMP-Daten der eGK.  **[\<=]**

<table><tr><th colspan="2">
Metadatum XDS.b

</th><th>
Opt

</th><th>
Nutzungsvorgabe  
(Wertvorgabe oder Implementierungsanweisung)

</th></tr><tr><td colspan="4">
Metadatenelement DocumentEntry

</td></tr><tr><td colspan="2">
classCode

</td><td>
R

</td><td>
Codesystem, ID: 1.2.276.0.76.11.32  
Code: PLA

</td></tr><tr><td colspan="2">
creationTime

</td><td>
R

</td><td>
element MP/A   
attribute MP/A/@t  

</td></tr><tr><td colspan="2">
healthcareFacilityTypeCode

</td><td>
R

</td><td>
Author des Dokumentes   
Der Wert MUSS aus [IHE-ITI-VS], Value Set
IHEXDShealthcareFacilityTypeCode gewählt werden. 

</td></tr><tr><td colspan="2">
practiceSettingCode

</td><td>
R

</td><td>
Author des Dokumentes   
Der Wert MUSS aus [IHE-ITI-VS], Value Set
practiceSettingCode gewählt werden. 

</td></tr><tr><td colspan="2">
sourcePatientId

</td><td>
R

</td><td>
Mögliche Quellen:  
KVNR des Versicherten =  
element MP/P   
attribute
MP/P/@egk 

</td></tr><tr><td colspan="4">
Metadatenelement SubmissionSet 

</td></tr><tr><td colspan="2">
contentTypeCode

</td><td>
R

</td><td>
Klinische Aktivität, die zum Einstellen des SubmissionSet geführt hat. 

Codesystem=1.3.6.1.4.1.19376.3.276.1.5.12  
Code=8 

</td></tr></table>

**A_15059-01 - Anzeige (Rendering) ContentProfile eMP**

Das PS MUSS ePA-Daten im ContentProfile elektronischer Medikationsplan in
geeigneter Form zur Anzeige bringen können. Für die Anzeige der Inhaltsdaten
SOLL die Anzeigefunktion des Medikationsplans und der zugehörigen Einwilligung
nachgenutzt werden, die beim Auslesen des eMP von der eGK gemäß
[gemILF_PS_AMTS] verwendet wird, sofern die Anzeigefunktion über die Anwendung
eMP/AMTS verfügbar ist. **[\<=]**

### 6.4.3 ContentProfile Arztbrief nach § 291f

Falls ein Arztbrief im Format als HL7 CDA R2-Dokument vorliegt, ohne dass der
Arztbrief eine PDF-Darstellung hat, soll er direkt im
Format  mimeType= application/xmlin der Dokumentenverwaltung der ePA
verwaltet werden. 

Ein Arztbrief, der als reines PDF-Dokument in die ePA eingestellt werden
soll, soll direkt im Format  mimeType = application/pdf  in der
Dokumentenverwaltung der ePA verwaltet werden.

Der Arztbrief nach § 291f SGB V hat gemäß [Richtlinie eArztbrief] die
verpflichtenden Teile PDF-Dokument und CDA-XML (nur der CDA-Header ist
verpflichtend).  Um diesen Arztbrief in die ePA einzustellen und wieder
auszulesen, wird auf das XML-ContainerformatDischargeLetterContainer(s.
Abb_ILF_ePA_eAB-XML-Containerformat aus  PHRManagementService.xsd)
zurückgegriffen. 

![Abbildung-12][Abbildung-12]

**A_14244 - ePA-Einstellung Verarbeitungsvorschrift für Arztbrief nach § 291f
mit XML- und PDF-Anteil**

Falls der Arztbrief nach § 291f in zwei Anteilen vorliegt (einem CDA-Anteil und
einem PDF-Anteil), MUSS das PS beide Teile gemeinsam in eine
XML-Container-Struktur gemäß [gemSpec_DM_ePA#4.2] einstellen und diesen
in eine gemeinsamen SubmissionSet in die ePA einstellen. In diesem
SubmissionSet MUSS dasMetadatenelement
SubmissionSet.formatCode aufCodesystem= 1.3.6.1.4.1.19376.3.276.1.5.6 und Code=urn:gematik:ig:Arztbrief:r3.1 gesetzt
werden. **[\<=]**

**A_14556 - eAB-spezifische Metadatenbefüllung**

Das PS MUSS die Werte derSubmissionSet-Metadaten für den elektronischen
Arztbrief gemäß [gemSpec_DM_ePA] für das Dokumentenmanagement der ePA
automatisiert befüllen und dabei die
eAB-spezifischen Implementierungshinweise aus Tab_ILF_ePA_Nutzungsvorgaben
für Metadaten eAB beachten.  

Tabelle43: Tab_ILF_ePA_Nutzungsvorgaben für Metadaten eAB

<table><tr><th colspan="2">
Metadatum XDS.b

</th><th>
Opt

</th><th>
Nutzungsvorgabe  
(Wertvorgabe oder Implementierungsanweisung)

</th></tr><tr><td colspan="4">
Metadatenelement DocumentEntry

</td></tr><tr><td colspan="2">
author

</td><td>
R

</td><td>
%

</td></tr><tr><td>
authorPerson

</td><td>
O

</td><td>
Mögliche Quellen :

 ---> UL

</td></tr><tr><td>
authorInstitution

</td><td>
O

</td><td>
Mögliche Quellen :

 ---> UL

</td></tr><tr><td>
authorRole

</td><td>
O

</td><td>
Einsteller des Dokumentes   
Verwendung gemäß [IHE-ITI-VS] 

</td></tr><tr><td>
authorSpecialty 

</td><td>
O

</td><td>
Einsteller des Dokumentes   
Verwendung gemäß [IHE-ITI-VS]  

</td></tr><tr><td>
authorTelecommunication

</td><td>
O

</td><td>
Telekommunikationsdaten des Autors

</td></tr><tr><td colspan="2">
classCode

</td><td>
R

</td><td>
Codesystem, ID: 1.2.276.0.76.11.32  
Code: BRI

</td></tr><tr><td colspan="2">
creationTime

</td><td>
R

</td><td>
Mögliche Quellen:

 ---> UL

</td></tr><tr><td colspan="2">
formatCode

</td><td>
R

</td><td>
Codesystem=

 1.3.6.1.4.1.19376.3.276.1.5.6

Code=urn:gematik:ig:Arztbrief:r3.1

</td></tr><tr><td colspan="2">
healthcareFacilityTypeCode

</td><td>
R

</td><td>
Der Wert MUSS aus [IHE-ITI-VS], Value Set IHEXDShealthcareFacilityTypeCode
gewählt werden. Wert des Einstellers

</td></tr><tr><td colspan="2" rowspan="1">
mimeType

</td><td>
R

</td><td>
Für den eAB als XML: application/xml    
Für den eAB als PDF:
application/pdf 

</td></tr><tr><td colspan="2">
practiceSettingCode

</td><td>
R

</td><td>
Der Wert MUSS aus [IHE-ITI-VS], Value Set practiceSettingCode gewählt
werden.  Wert des Einstellers

</td></tr><tr><td colspan="2">
sourcePatientId

</td><td>
R

</td><td>
 eAB Patient.id, falls vorhanden und eine Versicherten-ID, mit Versicherten-ID
des Versicherten abgleichen. Falls die IDs nicht matchen, muss eine Warnung
ausgeben werden. 

</td></tr><tr><td colspan="2">
title

</td><td>
O

</td><td>
eAB ClinicalDocument.title 

</td></tr><tr><td colspan="2">
typeCode

</td><td>
R

</td><td>
Codesystem-ID=1.3.6.1.4.1.19376.3.276.1.5.9   
Code=BERI

</td></tr><tr><td colspan="4">
Metadatenelement SubmissionSet 

</td></tr><tr><td colspan="2">
contentTypeCode

</td><td>
R

</td><td>
Klinische Aktivität, die zum Einstellen des SubmissionSet geführt hat. 

Codesystem=1.3.6.1.4.1.19376.3.276.1.5.12  
Code=2,3,4,8,9
gemäß [IHE-ITI-VS] 

</td></tr></table>

**[\<=]**

**A_16246 - Auslesen des eArztbriefes nach § 291f SGB V**

Beim Auslesen eines eArztbriefes
mitformatCode="Code=urn:gematik:ig:Arztbrief:r3.1" MUSS das PS die zwei Anteile
(den CDA-Anteil und den PDF-Anteil) aus der
XML-Container-Struktur DischargeLetterContainergemäß [gemSpec_DM_ePA#4.2]
aus der ePA herauslesen und als eArztbrief nach § 291f SGB V gemäß
[Richtlinie eArztbrief] weiterverarbeiten und den PDF-Anteil zur Anzeige
bringen können.  **[\<=]**

### 6.4.4 Strukturierte Dokumente

In der ePA können strukturierte Dokumente verarbeitet werden. Strukturierte
Dokumente und deren Zuordnung zu Sammlung und Sammlungstypen sind in
[gemSpec_DM_ePA# ] beschrieben.

Zum Laden, Suchen und Einstellen von strukturierten Dokumenten gelten die
Anwendungsfälle zum Laden, Suchen, Einstellen und Löschen von Dokumenten. Es
kommen gemäß [gemSpec_DM] weitere Kriterien zur Aufbereitung einer
Sammlung hinzu. Besteht der Bedarf nach mehreren Sammlungen des gleichen Typs
(Beispiel Mutterpass) so wird jeweils ein dynamischer Ordner (je
Schwangerschaft) angelegt. Beim erstmaligen Erstellen einer dynamischen
Sammlung muss vom Primärsystem für diese Sammlung ein Ordner angelegt werden.
Es wird empfohlen für den Titel des Ordners einen sprechenden Namen zu finden.
Dadurch kann bei der Suche nach Sammlungen bereits durch den Titel auf deren
Inhalt geschlossen werden. Da das Aktensystem dynamisch angelegte  Ordner
löscht, wenn diese keine Dokumente mehr enthalten, ist das Löschen der Ordner
durch das Primärsystem nicht erforderlich.

Die Erteilung der Berechtigung für eine Sammlung kann im Primärsystem im
Rahmen der Berechtigung für eine Dokumentenkategorie (soweit für Pass
definiert) erfolgen.

Die Liste der strukturierten Dokumente wird sich im Laufe der Zeit erweitern.
Die KBV liefert zu neu entwickelten MIOs Informationen über die interne
Datenstruktur und fachliche Hintergründe, die gematik veröffentlicht
Informationen darüber, um welchen Sammlungstyp es sich bei dem neuen
strukturierten Dokument handelt, und welche Metadaten dieses strukturierte
Dokument identifizieren.

Die Berechtigung zukünftiger strukturierter Dokumente wird über das Freigeben
gemäß Vertraulichkeitsstufe geregelt, d.h. wenn ein neues, bisher noch nicht
bekanntes strukturiertes Dokument vom Versicherten mit der
Vertraulichkeitsstufe "normal" eingestellt wird, kann es über die genannte
Vertraulichkeitsstufe für einen LE freigegeben werden.

**A_19548 - Elektronischer Impfpass**

Das PS MUSS die Werte derDocumentEntry- und SubmissionSet-Metadaten für den
elektronischen Impfpass gemäß [gemSpec_DM_ePA] für das Dokumentenmanagement
der ePA automatisiert befüllen. **[\<=]**

**A_19549 - Elektronischer Mutterpass**

Das PS MUSS die Werte derDocumentEntry- und SubmissionSet-Metadaten für den
elektronischen Mutterpass gemäß [gemSpec_DM_ePA] für das
Dokumentenmanagement der ePA automatisiert befüllen. **[\<=]**

**A_19550 - Elektronisches Untersuchungsheft für Kinder**

Das PS MUSS die Werte derDocumentEntry- und SubmissionSet-Metadaten für das
elektronische Untersuchungsheft für Kinder gemäß [gemSpec_DM_ePA] für das
Dokumentenmanagement der ePA automatisiert befüllen. **[\<=]**

**A_19551 - Elektronisches Zahnbonusheft**

Das PS MUSS die Werte der DocumentEntry- und SubmissionSet-Metadaten für das
elektronische Zahnbonusheft gemäß [gemSpec_DM_ePA] für das
Dokumentenmanagement der ePA automatisiert befüllen. **[\<=]**

**A_19552 - Elektronische Verordnungen/Verordnungsdatensatz**

Das PS MUSS die Werte derDocumentEntry- und SubmissionSet-Metadaten für
elektronische Verordnungen/den Verordnungsdatensatz gemäß [gemSpec_DM_ePA]
für das Dokumentenmanagement der ePA automatisiert befüllen.  **[\<=]**

**A_20197-01 - Arbeitsunfähigkeitsbescheinigung**

Das PS MUSS die Werte derDocumentEntry- und SubmissionSet-Metadaten für
elektronische Arbeitsunfähigkeitsbescheinigungen gemäß [gemSpec_DM_ePA] für
das Dokumentenmanagement der ePA automatisiert befüllen.  **[\<=]**

### 6.4.4.1 Signatur für strukturierte Dokumentenformate der ePA

Ob eine Signatur und welche Art der Signatur (QES oder nonQES) erforderlich
ist, wird durch den Anwendungsfall für das jeweilige strukturierte
Dokumentenformat festgelegt und außerhalb dieser Spezifikation veröffentlicht.

Im Folgenden wird das Vorgehen beschrieben, für den Fall, dass ein
strukturiertes Dokumentenformat signiert wird. 

Im Primärsystem liegt ein strukturiertes Dokumentenformat der ePA als
FHIR-XML-Darstellung oder FHIR-JSON-Darstellung vor. Im Sinne der
Signaturerstellung wird dies als Data to be Signed (DTBS) bezeichnet.

Vor dem Einstellen des Dokuments wird dieses elektronisch signiert (QES oder
nonQES). Das Primärsystem nutzt dafür die Schnittstelle des Konnektors und
dieser den HBA für QES bzw. SM-B für nonQES des einstellenden LE. 

Bei der Signaturerstellung ist folgender Ablauf im Primärsystem erforderlich:

 ---> OL

**A_19742 - strukturiertes Dokument - QES signieren**

Falls eine QES-Signatur für ein strukturiertes Dokument gefordert wird, MUSS
das PS vor dem Einstellen eines strukturierten Dokumentes in die Akte des
Versicherten eine QES-Signatur als CADES Enveloping Signaturfür das
strukturierte Dokument durch Aufruf der OperationSignDocumenterstellen.
**[\<=]**

**A_19957 - strukturiertes Dokument - nonQES signieren**

Falls eine nonQES-Signatur für ein strukturiertes Dokument gefordert wird, MUSS
das PS vor dem Einstellen eines strukturierten Dokumentes in die Akte des
Versicherten eine nonQES Signatur als CADES Enveloping Signaturfür das
strukturierte Dokument durch Aufruf der OperationSignDocumenterstellen.
**[\<=]**

Bei der Signaturprüfung ist folgender Ablauf im Primärsystem erforderlich:

 ---> OL

**A_19743 - strukturiertes Dokument - QES-Signatur prüfen**

Falls eine QES-Signatur für ein strukturiertes Dokument gefordert wird MUSS das
PS nach dem Laden eines strukturierten Dokumentes aus der Akte des
Versicherten die QES des Dokumentes durch Aufruf der
OperationVerifyDocumentprüfen und das Prüfergebnis zur Anzeige bringen.
**[\<=]**

**A_19958 - strukturiertes Dokument - nonQES Signatur prüfen**

Falls eine nonQES-Signatur für ein strukturiertes Dokument gefordert wird, MUSS
das PS nach dem Laden eines strukturierten Dokumentes aus der Akte des
Versicherten die nonQES des Dokumentes durch Aufruf der
OperationVerifyDocumentprüfen und das Prüfergebnis zur Anzeige bringen.
**[\<=]**

Ein vom Arzt mit QES-signiertes E-Rezept darf nicht in den Besitz des
Versicherten gelangen und wird ausschließlich im E-Rezept-Server gespeichert.
Deshalb wird begrifflich unterschieden zwischen E-Rezept und Elektronische
Verordnungen/Verordnungsdatensatz. Elektronische
Verordnungen/Verordnungsdatensatz ist nicht QES signiert und kann in die Akte
des Versicherten eingestellt werden.

**A_19974 - Elektronische Verordnungen/Verordnungsdatensatz ohne QES**

Ein Primärsystem DARF NICHT Elektronische Verordnungen/Verordnungsdatensatz
mit QES in die Akte des Versicherten einstellen.   **[\<=]**

### 7 Ergänzende Funktionalitäten

### 7.1 Empfehlung zur Archivierung

Auf der Grundlage gesetzlicher Regelungen besteht eine Archivierungspflicht für
die medizinischen Dokumente und für die Übertragungsprotokolle des
Versicherten. Die Archivierung ist korrekt, verständlich, vollständig,
nachvollziehbar und zeitnah durchzuführen. Je nach gesetzlicher Regelung sind
damit dokumentierte Inhalte mit Aufbewahrungszeiträumen verbunden. 

Zur Aufbewahrungsfrist wird auf die jeweils aktuelle Fassung der „Empfehlungen
zur ärztlichen Schweigepflicht, Datenschutz und Datenverarbeitung in der
Arztpraxis“ der BÄK und KBV, siehe [BÄK_KBV], und auf die einschlägigen
gesetzlichen Normen verwiesen.  Im Umfang der Archivierung sollen
zusätzlich zu den aus der ePA heruntergeladenen und persistent im PS
gespeicherten ePA-Dokumenten des Versicherten auch die zu diesen Dokumenten
gehörigen Metadaten enthalten sein, die in [gemSpec_DM_ePA#Tabelle
Nutzungsvorgaben für Metadatenattribute XDS.b] aufgelistet sind, soweit sie
für den Verarbeitungskontext relevant sind.

### 8 Anhang A – Verzeichnisse

### 8.1 Abkürzungen

<table><tr><th>
Kürzel

</th><th>
Erläuterung

</th></tr><tr><td>
Versicherten-ID

</td><td>
10-stelliger unveränderlicher Teil der 30-stelligen Krankenversicherungsnummer.

</td></tr><tr><td>
BAG

</td><td>
Berufsausübungsgemeinschaft

</td></tr><tr><td>
DTBS

</td><td>
Data To Be Signed - zu signierende Daten

</td></tr><tr><td>
DTBSR

</td><td>
Data to be Signed Representation - maschinenlesbare Repräsentation der zu
signierenden Daten

</td></tr><tr><td>
KT

</td><td>
Kartenterminal

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

</td></tr><tr><td>
ePA-Frontend des Versicherten 

</td><td>
Softwareprogramm in der Verfügung des Versicherten, ausgestattet mit einer
grafischen Benutzeroberfläche zum Starten fachlicher Anwendungsfälle der ePA
und Darstellung des Ergebnisses der Anwendungsfälle.

</td></tr></table>

Das Glossar wird als eigenständiges Dokument, vgl. [gemGlossar] zur Verfügung
gestellt.

### 8.3 Abbildungsverzeichnis

- [Abbildung-1] - ILF_ePA_Element_Context
- [Abbildung-2] - Abb_ILF_ePA_RecordIdentifier
- [Abbildung-3] - Abb_ILF_ePA_Kombinierte_Anwendungsfälle_für_bereits_aktiviertes_Aktenkonto
- [Abbildung-4] - Abb_ILF_ePA_getHomeCommunityRequest
- [Abbildung-5] - Abb_ILF_PS_ePA_getHomeCommunityResponse
- [Abbildung-6] - Abb_ILF_ePA_Eingabeparameter_ActivateAccount
- [Abbildung-7] - Abb_ILF_ePA_RequestFacilityAuthorization
- [Abbildung-8] - Abb_ILF_ePA_Ad-hoc-Berechtigung_erteilen
- [Abbildung-9] - Abb_ILF_ePA_Eingabeparameter_GetAuthorizationList
- [Abbildung-10] - Abb_ILF_ePA_GetAuthorizationListResponse
- [Abbildung-11] - Abb_ILF_ePA_Benachrichtigungen_GetAll_mit_Zugriffspolicy-Event
- [Abbildung-12] - Abb_ILF_ePA_eAB-XML-Containerformat

### 8.4 Tabellenverzeichnis

- [Tabelle-1] - Tab_ILF_ePA_IHE-TransaktionenProfile
- [Tabelle-2] - Tab_ILF_ePA_Identifier_für_Versicherte_und_Akten
- [Tabelle-3] - Tab_ILF_ePA_Zugriffsberechtigungsstatus pro RecordIdentifier
- [Tabelle-4] - Tab_ILF_ePA_Zugriffsberechtigungen  
- [Tabelle-5] - Tab_ILF_ePA_Funktionsmerkmale_Beteiligung_Versicherter
- [Tabelle-6] - Tab_ILF_ePA_PHRManagementService
- [Tabelle-7] -  Tab_ILF_ePA_Operation_getHomeCommunityID
- [Tabelle-8] - Tab_ILF_ePA_Operation_ActivateAccount
- [Tabelle-9] -  Tab_ILF_ePA_Operation_RequestFacilityAuthorization
- [Tabelle-10] - Tab_ILF_ePA_Zugriffsberechtigungs-Endedatum
- [Tabelle-11] - Tab_ILF_ePA_PHRService
- [Tabelle-12] - Tab_ILF_ePA_DM_Profilierung
- [Tabelle-13] - Tab_ILF_ePA_Einschränkungen_auf_XDS.b
- [Tabelle-14] - Tab_ILF_ePA_ClientInformationen
- [Tabelle-15] - Tab_ILF_ePA_Zugriffsinformation_Werte
- [Tabelle-16] - Tab_ILF_ePA_IHE-Profilierung_ITI41
- [Tabelle-17] - Tab_ILF_ePA_Operation_Dokument_einstellen
- [Tabelle-18] -  Tab_ILF_ePA_Fehlerbehandlung_Dokumente_einstellen
- [Tabelle-19] - Tab_ILF_ePA_IHE-Profilierung_ITI18
- [Tabelle -20] - Tab_ILF_ePA_Operation_Dokument_suchen
- [Tabelle-21] - Tab_ILF_ePA_FindDocuments_Pflichtfelder
- [Tabelle-22] - Tab_ILF_ePA_StoredQueries
- [Tabelle-23] - Tab_ILF_ePA_Fehlerbehandlung_Dokumente_Suchen
- [Tabelle-24] - Tab_ILF_ePA_IHE-Profilierung_ITI43
- [Tabelle-25] - Tab_ILF_ePA_Operation_Dokumente_anzeigen
- [Tabelle-26] - Tab_ILF_ePA_IHE-Profilierung_ITI86
- [Tabelle-27] - Tab_ILF_ePA_Operation_Dokumente_löschen
- [Tabelle-28] - Tab_ILF_ePA_Namensräume
- [Tabelle-29] - Tab_ILF_ePA_Benachrichtigungsquellen
- [Tabelle-30] - Tab_ILF_ePA_Benachrichtigungs_InfoModell
- [Tabelle-31] -  Tab_ILF_ePA_Operation_GetAuthorizationList
- [Tabelle-32] - Tab_ILF_ePA_Infoquelle_Fehlermeldung
- [Tabelle-33] - Tab_ILF_ePA_ErrorSeverity
- [Tabelle-34] - Tab_ILF_ePA_IHE_Success_and_Error_Reporting
- [Tabelle-35] - Tab_ILF_ePA_DifferenzFehlerhandling
- [Tabelle-36] - Tab_ILF_ePA_Handlungsanweisung_im_Fehlerfall
- [Tabelle-37] - Tab_ILF_ePA_Handlungsanweisung_im_Fehlerfall
- [Tabelle-38] - Tab_ILF_ePA_Fehlermeldungen des Fachmoduls ePA
- [Tabelle-39] - Tab_ILF_ePA_IHE-Fehlermeldungen_Aktensystem
- [Tabelle-40] - Tab_ILF_ePA_Datenfelder_Selbstauskunft
- [Tabelle-41] - Tab_ILF_ePA_Nutzungsvorgaben für Metadaten NFD/DPE
- [Tabelle-42] - Tab_ILF_ePA_Nutzungsvorgaben für Metadaten eMP
- [Tabelle-43] - Tab_ILF_ePA_Nutzungsvorgaben für Metadaten eAB

### 8.5 Referenzierte Dokumente

### 8.5.1 Dokumente der gematik

Die nachfolgende Tabelle enthält die Bezeichnung der in dem vorliegenden
Dokument referenzierten Dokumente der gematik zur Telematikinfrastruktur. Der
mit der vorliegenden Version korrelierende Entwicklungsstand dieser Konzepte
und Spezifikationen wird pro Release in einer Dokumentenlandkarte definiert,
Version und Stand der referenzierten Dokumente sind daher in der nachfolgenden
Tabelle nicht aufgeführt. Deren zu diesem Dokument passende jeweils gültige
Versionsnummer sind in der aktuellsten, von der gematik veröffentlichten
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
[gemSpec_FM_ePA]

</td><td>
gematik: Spezifikation Fachmodul ePA

</td></tr><tr><td>
[gemSpec_DM_ePA]

</td><td>
gematik: Datenmodell ePA

</td></tr><tr><td>
[gemSpec_OM]

</td><td>
gematik: Übergreifende Spezifikation Operations und Maintenance

</td></tr><tr><td>
[gemSysL_ePA]

</td><td>
gematik: Systemspezifisches Konzept ePA

</td></tr><tr><td>
[gemILF_PS_NFDM]

</td><td>
gematik: Implementierungsleitfaden Primärsysteme – Notfalldaten-Management
(NFDM)

</td></tr><tr><td>
[gemSpec_InfoNFDM]

</td><td>
gematik: Informationsmodell Notfalldaten-Management (NFDM)

</td></tr><tr><td>
[gemRL_QES_NFDM]

</td><td>
gematik: Signaturrichtlinie QES Notfalldaten-Management  (NFDM) 

</td></tr><tr><td>
[gemSpec_Info_AMTS]

</td><td>
gematik: Informationsmodell eMP/AMTS-Datenmanagement

</td></tr><tr><td>
[gemILF_PS_AMTS]

</td><td>
gematik: Implementierungsleitfaden Primärsysteme
–  elektronischer Medikationsplan/AMTS-

Datenmanagement (Stufe A)

</td></tr><tr><td>
[gemKPT_Arch_TIP] 

</td><td>
gematik: Konzept Architektur der TI-Plattform

</td></tr><tr><td>
[gemSpec_PKI]

</td><td>
gematik: Spezifikation PKI

</td></tr></table>

### 8.5.2 Weitere Dokumente

<table><tr><th>
[Quelle]

</th><th>
Herausgeber (Erscheinungsdatum): Titel

</th></tr><tr><td>
[BasicProfile1.2] 

</td><td>
Basic Profile Version 1.2  

http://www.ws-i.org/Profiles/BasicProfile-1.2-2010-11-09.html 

</td></tr><tr><td>
[BasicProfile2.0]

</td><td>
Basic Profile Version 2.0 

http://ws-i.org/Profiles/BasicProfile-2.0-2010-11-09.html 

</td></tr><tr><td>
[WSDL11]

</td><td>
W3C (2006): WSDL 1.1 Binding Extension for SOAP 1.2,   

https://www.w3.org/Submission/wsdl11soap12/  

</td></tr><tr><td>
[SOAP12]

</td><td>
W3C (2007): SOAP Version 1.2 Part 1: Messaging Framework (Second Edition), 

https://www.w3.org/TR/soap12-part1/ 

</td></tr><tr><td>
[ebRS]

</td><td>
ebXML Registry Services Specification Version 3.0 

https://docs.oasis-open.org/regrep/regrep-rs/v3.0/regrep-rs-3.0-os.pdf  

</td></tr><tr><td>
[IHE-ITI-TF2a], enthält [ITI-18]

</td><td>
IHE International (2018): IHE IT Infrastructure (ITI) Technical Framework,
Volume 2a (ITI TF-2a) - Transactions Part A, Revision 15.0, 
http://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2a.pdf

</td></tr><tr><td>
[IHE-ITI-TF2b], enthält [ITI-41], [ITI-43], [ITI-45]

</td><td>
IHE International (2017): IHE IT Infrastructure (ITI) Technical Framework,
Volume 2b (ITI TF-2b) - Transactions Part B, Revision 14.0, 
http://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2b.pdf

</td></tr><tr><td>
[IHE-ITI-TF2x]

</td><td>
IHE International (2018): IHE IT Infrastructure (ITI) Technical Framework,
Volume 2x (ITI TF-2x) – Volume 2 Appendices, Revision 15.1,  

http://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2x.pdf

</td></tr><tr><td>
[IHE-ITI-TF3]

</td><td>
IHE International (2018): IHE IT Infrastructure (ITI) Technical Framework,
Volume 3 (ITI TF-3) - Cross-Transaction Specifications and Content
Specifications, Revision 15.0, 

http://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol3.pdf

</td></tr><tr><td>
[IHE-ITI-RMD], enthält [ITI-86]

</td><td>
IHE International (2018): IHE IT Infrastructure (ITI) Technical Framework
Supplement, Remove Metadata and Documents (RMD), Revision 1.2 – Trial
Implementation, 
http://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_Suppl_RMD.pdf

</td></tr><tr><td>
[IHE-ITI-XCDR]

</td><td>
IHE International (2017): IHE IT Infrastructure (ITI) Technical Framework
Supplement, Cross-Community Document Reliable Interchange (XCDR), Revision 1.4
– Trial Implementation, 

http://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_Suppl_XCDR.pdf

</td></tr><tr><td>
[IHE-ITI-TF1]

</td><td>
IHE International (2018): IHE IT Infrastructure (ITI)  Technical Framework,
Volume 1    
(ITI TF-1) Integration Profiles  

http://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol1.pdf 

</td></tr><tr><td>
[ITI TF Supplement]

</td><td>
IHE IT Infrastructure  5 Technical Framework Supplement   
Remove Metadata
and Documents  10 (RMD) 

</td></tr><tr><td>
[MTOM]

</td><td>
W3C (2005): SOAP Message Transmission Optimization Mechanism,
https://www.w3.org/TR/soap12-mtom/ 

</td></tr><tr><td>
[Richtlinie eArztbrief]

</td><td>
Kassenärztliche Bundesvereinigung (2017): Richtlinie über die Übermittlung
elektronischer Briefe in der vertragsärztlichen Versorgung gemäß § 291f SGB
V, Richtlinie Elektronischer Brief, Version: 10.0,  

https://www.kbv.de/media/sp/RL-eArztbrief.pdf 

</td></tr><tr><td>
[KBV Portal]

</td><td>
Portal der Kassenärztliche Bundesvereinigung

https://kbv.de

 

</td></tr><tr><td>
[XPATH]

</td><td>
XML Path Language (XPath) Version 1.0  
http://www.w3.org/TR/xpath

</td></tr><tr><td>
[IHE-ITI-VS]

</td><td>
IHE Deutschland (2018): Value Sets für Aktenprojekte im deutschen
Gesundheitswesen, Implementierungsleitfaden, Version 2.0  

http://www.ihe-d.de/projekte/xds-value-sets-fuer-deutschland/ 

</td></tr><tr><td>
[OWASP Top 10]

</td><td>
OWASP (2017): OWASP Top 10 -- 2017 - The Ten Most Critical Web Application
Security Risks 

https://github.com/OWASP/Top10/raw/master/2017/OWASP%20Top%2010-2017%20(en).pdf 

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
[2.1]:                   #21-relevante-integrationsprofile
[3]:                     #3-systemkontext
[3.1]:                   #31-akteure-und-rollen
[3.2]:                   #32-nachbarsysteme
[4]:                     #4-übergreifende-festlegungen
[4.1]:                   #41-webservice-kommunikation
[4.2]:                   #42-dienstverzeichnisdienst
[4.3]:                   #43-ereignisdienst
[4.4]:                   #44-zugriffssteuerung
[4.4.1]:                 #441-aufrufkontext
[4.4.2]:                 #442-recordidentifier
[4.4.3]:                 #443-status-aktenzugriff
[5]:                     #5-funktionsmerkmale
[5.1]:                   #51-epa-administration
[5.1.1]:                 #511-aktenanbieter-ermitteln
[5.1.1.1]:               #5111-schnittstelle
[5.1.1.2]:               #5112-umsetzung
[5.1.1.3]:               #5113-nutzung
[5.1.2]:                 #512-aktenkonto-aktivieren
[5.1.2.1]:               #5121-schnittstelle
[5.1.2.2]:               #5122-umsetzung
[5.1.2.3]:               #5123-nutzung
[5.1.3]:                 #513-ad-hoc-berechtigung-erteilen
[5.1.3.1]:               #5131-schnittstelle
[5.1.3.2]:               #5132-umsetzung
[5.1.3.3]:               #5133-nutzung
[5.2]:                   #52-dokumentenmanagement
[5.2.1]:                 #521-dokumente-einstellen
[5.2.1.1]:               #5211-schnittstelle
[5.2.1.2]:               #5212-umsetzung
[5.2.1.3]:               #5213-nutzung
[5.2.2]:                 #522-dokumente-suchen
[5.2.2.1]:               #5221-schnittstelle
[5.2.2.2]:               #5222-umsetzung
[5.2.2.3]:               #5223-nutzung
[5.2.3]:                 #523-dokumente-laden
[5.2.3.1]:               #5231-schnittstelle
[5.2.3.2]:               #5232-umsetzung
[5.2.3.3]:               #5233-nutzung
[5.2.4]:                 #524-dokumente-löschen
[5.2.4.1]:               #5241-schnittstelle
[5.2.4.2]:               #5242-umsetzung
[5.2.4.3]:               #5243-nutzung
[5.2.5]:                 #525-artefakte
[5.2.5.1]:               #5251-namensräume
[5.2.5.2]:               #5252-wsdls-und-schemata
[5.2.6]:                 #526-testunterstützung
[5.3]:                   #53-protokolle-und-benachrichtigungen
[5.3.1]:                 #531-benachrichtigungen-erhalten
[5.3.1.1]:               #5311-info-quelle-epa-administration
[5.3.1.2]:               #5312-info-quelle-berechtigungs-abfrage
[5.3.1.3]:               #5313-info-quelle-dokumentensuche
[5.3.1.4]:               #5314-info-quelle-systeminformationsdienst
[5.3.1.5]:               #5315-info-quelle-fehlermeldung
[5.3.1.6]:               #5316-umsetzung
[5.3.1.7]:               #5317-nutzung
[5.3.2]:                 #532-übertragungsprotokolle-speichern
[5.4]:                   #54-status--und-fehlermeldungen
[5.4.1]:                 #541-statusinformationen
[5.4.2]:                 #542-fehlerbehandlung
[5.4.2.1]:               #5421-telematikerror
[5.4.2.2]:               #5422-ihe-error
[5.4.3]:                 #543-handlungs-empfehlungen-in-fehlerfällen
[5.4.4]:                 #544-übersicht-möglicher-fehlermeldungen
[5.4.4.1]:               #5441-fehlermeldungen-aus-dem-fachmodul-epa
[5.4.4.2]:               #5442-fehlermeldungen-aus-dem-aktensystem-epa
[6]:                     #6-informationsmodell
[6.1]:                   #61-metadaten
[6.2]:                   #62-selbstauskunft
[6.3]:                   #63-wertebereiche
[6.4]:                   #64-dokumentenformate-der-epa
[6.4.1]:                 #641-contentprofile-notfalldatensatz-und-datensatz-persönliche-erklärungen
[6.4.2]:                 #642-contentprofile-elektronischer-medikationsplan
[6.4.3]:                 #643-contentprofile-arztbrief-nach-§-291f
[6.4.4]:                 #644-strukturierte-dokumente
[6.4.4.1]:               #6441-signatur-für-strukturierte-dokumentenformate-der-epa
[7]:                     #7-ergänzende-funktionalitäten
[7.1]:                   #71-empfehlung-zur-archivierung
[8]:                     #8-anhang-a-–-verzeichnisse
[8.1]:                   #81-abkürzungen
[8.2]:                   #82-glossar
[8.3]:                   #83-abbildungsverzeichnis
[8.4]:                   #84-tabellenverzeichnis
[8.5]:                   #85-referenzierte-dokumente
[8.5.1]:                 #851-dokumente-der-gematik
[8.5.2]:                 #852-weitere-dokumente
[Abbildung-1]:           gemILF_PS_ePA_V1.8.2.attachments/10658844976499636160.png
[Abbildung-2]:           gemILF_PS_ePA_V1.8.2.attachments/3763235049232573412.png
[Abbildung-3]:           gemILF_PS_ePA_V1.8.2.attachments/7394674084710412507.png
[Abbildung-4]:           gemILF_PS_ePA_V1.8.2.attachments/7617311717081102059.png
[Abbildung-5]:           gemILF_PS_ePA_V1.8.2.attachments/2427030114978174737.png
[Abbildung-6]:           gemILF_PS_ePA_V1.8.2.attachments/16004476117784056897.png
[Abbildung-7]:           gemILF_PS_ePA_V1.8.2.attachments/3901828183472372682.png
[Abbildung-8]:           gemILF_PS_ePA_V1.8.2.attachments/1795910573159626875.png
[Img-009]:               gemILF_PS_ePA_V1.8.2.attachments/5654566259053092633.png
[Abbildung-9]:           gemILF_PS_ePA_V1.8.2.attachments/4361177934131753633.png
[Abbildung-10]:          gemILF_PS_ePA_V1.8.2.attachments/13890405362866839461.png
[Abbildung-11]:          gemILF_PS_ePA_V1.8.2.attachments/3608420212588913930.png
[Abbildung-12]:          gemILF_PS_ePA_V1.8.2.attachments/995364908173244191.png
[Tbl-001]:               #Tbl-001 (&93834801498000)
[Tabelle-1]:             #Tabelle-1 (&93834799846496)
[Tbl-003]:               #Tbl-003 (&93834801628032)
[Tabelle-2]:             #Tabelle-2 (&93834801640184)
[Tabelle-3]:             #Tabelle-3 (&93834771010736)
[Tabelle-4]:             #Tabelle-4 (&93834781667744)
[Tabelle-5]:             #Tabelle-5 (&93834781698968)
[Tabelle-6]:             #Tabelle-6 (&93834781727288)
[Tabelle-7]:             #Tabelle-7 (&93834783647648)
[Tbl-010]:               #Tbl-010 (&93834804571120)
[Tabelle-8]:             #Tabelle-8 (&93834768032280)
[Tabelle-9]:             #Tabelle-9 (&93834799229168)
[Tabelle-10]:            #Tabelle-10 (&93834801532864)
[Tabelle-11]:            #Tabelle-11 (&93834774944136)
[Tabelle-12]:            #Tabelle-12 (&93834798958048)
[Tabelle-13]:            #Tabelle-13 (&93834798976760)
[Tabelle-14]:            #Tabelle-14 (&93834798996584)
[Tabelle-15]:            #Tabelle-15 (&93834798406872)
[Tabelle-16]:            #Tabelle-16 (&93834798436448)
[Tabelle-17]:            #Tabelle-17 (&93834798465224)
[Tbl-021]:               #Tbl-021 (&93834764427512)
[Tbl-022]:               #Tbl-022 (&93834781756608)
[Tabelle-18]:            #Tabelle-18 (&93834781778408)
[Tabelle-19]:            #Tabelle-19 (&93834781802600)
[Tabelle -20]:           #Tabelle -20 (&93834785757240)
[Tabelle-21]:            #Tabelle-21 (&93834785794952)
[Tbl-027]:               #Tbl-027 (&93834778238832)
[Tabelle-22]:            #Tabelle-22 (&93834778256200)
[Tbl-029]:               #Tbl-029 (&93834778299888)
[Tbl-030]:               #Tbl-030 (&93834778311120)
[Tabelle-23]:            #Tabelle-23 (&93834778325224)
[Tabelle-24]:            #Tabelle-24 (&93834775719840)
[Tabelle-25]:            #Tabelle-25 (&93834775743512)
[Tbl-034]:               #Tbl-034 (&93834775779952)
[Tbl-035]:               #Tbl-035 (&93834775789392)
[Tabelle-26]:            #Tabelle-26 (&93834799066032)
[Tabelle-27]:            #Tabelle-27 (&93834799084472)
[Tabelle-28]:            #Tabelle-28 (&93834799128320)
[Tabelle-29]:            #Tabelle-29 (&93834765228272)
[Tabelle-30]:            #Tabelle-30 (&93834765315064)
[Tabelle-31]:            #Tabelle-31 (&93834765363624)
[Tabelle-32]:            #Tabelle-32 (&93834800038256)
[Tabelle-33]:            #Tabelle-33 (&93834783795888)
[Tabelle-34]:            #Tabelle-34 (&93834783815504)
[Tabelle-35]:            #Tabelle-35 (&93834783844088)
[Tabelle-36]:            #Tabelle-36 (&93834764257376)
[Tabelle-37]:            #Tabelle-37 (&93834764291456)
[Tabelle-38]:            #Tabelle-38 (&93834764327760)
[Tabelle-39]:            #Tabelle-39 (&93834775294584)
[Tabelle-40]:            #Tabelle-40 (&93834771282192)
[Tabelle-41]:            #Tabelle-41 (&93834771407720)
[Tabelle-42]:            #Tabelle-42 (&93834775492696)
[Tabelle-43]:            #Tabelle-43 (&93834775546368)
[Tbl-054]:               #Tbl-054 (&93834781415296)
[Tbl-055]:               #Tbl-055 (&93834781432088)
[Tbl-056]:               #Tbl-056 (&93834778090096)
[Tbl-057]:               #Tbl-057 (&93834778128656)
[https://kbv.de]:        https://kbv.de (&93834768143464)
