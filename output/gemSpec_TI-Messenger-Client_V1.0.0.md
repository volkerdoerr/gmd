
Elektronische Gesundheitskarte und Telematikinfrastruktur

### 

- Klassifizierung: öffentlich
- Referenzierung: gemSpec_TI-Messenger-Client
- Revision: 408371
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
  - [3.1] Nachbarsysteme
  - [3.2] TI-Messenger-Clients für unterschiedliche Nutzergruppen
  - [3.3] TI-Messenger-Clients für unterschiedliche Plattformen
- [4] Übergreifende Festlegungen
  - [4.1] Datenschutz und Sicherheit
  - [4.2] Benutzerführung
  - [4.3] Konfiguration des TI-Messenger-Clients
  - [4.4] Test
  - [4.5] Betriebliche Aspekte
- [5] Funktionsmerkmale
  - [5.1] Authentisierung
  - [5.2] Matrix-Client-Server-API
  - [5.3] Instant Messaging
  - [5.4] Direct Messaging
  - [5.5] Group Messaging
  - [5.6] Push-Benachrichtigungen
    - [5.6.1] Allgemein
    - [5.6.2] Push-Anbieter
    - [5.6.3] Push-Gateway
    - [5.6.4] Push-Regel
    - [5.6.5] Push-Regelsatz
    - [5.6.6] Opt-In
  - [5.7] Weitere Funktionen
- [6] Anhang A – Verzeichnisse
  - [6.1] Abkürzungen
  - [6.2] Glossar
  - [6.3] Abbildungsverzeichnis
  - [6.4] Tabellenverzeichnis
  - [6.5] Referenzierte Dokumente
    - [6.5.1] Dokumente der gematik
    - [6.5.2] Weitere Dokumente

### 1 Einordnung des Dokumentes

### 1.1 Zielsetzung

Beim vorliegenden Dokument handelt es sich um die Festlegungen zur ersten
Ausbaustufe des TI-Messengers. Diese Ausbaustufe ist definiert durch die
Ad-hoc-Kommunikation zwischen Organisationen des Gesundheitswesens. Dabei wird
insbesondere die Ad-hoc-Kommunikation zwischen Leistungserbringern bzw.
zwischen Leistungserbringerinstitutionen betrachtet. Festlegungen zur
Nutzergruppe der Versicherten und Anforderungen an Kassenorganisationen werden
in der zweiten Ausbaustufe des TI-Messengers Berücksichtigung finden und daher
im vorliegenden Dokument nicht weiter betrachtet. 

Die vorliegende Spezifikation definiert die Anforderungen zu Herstellung, Test
und Betrieb des Produkttyps TI-Messenger-Client. Der TI-Messenger-Client
stellt dem Nutzer die benötigte Funktionalität zur sicheren
Ad-hoc-Kommunikation mit anderen Teilnehmern bereit. Aus den
Kommunikationsbeziehungen mit dem TI-Messenger-Fachdienst und dem
VZD-FHIR-Directory resultieren vom TI-Messenger-Client zu nutzende
Schnittstellen. In vorliegendem Dokument wird die Nutzung dieser Schnittstellen
zur zur sicheren Ad-hoc-Kommunikation und die dafür benötigten
Funktionalitäten beschrieben. Vom TI-Messenger-Client genutzte Schnittstellen
werden in den entsprechenden Produkttypspezifikationen definiert.

### 1.2 Zielgruppe

Das Dokument richtet sich zwecks der Realisierung an Hersteller des Produkttypen
TI-Messenger-Client sowie an Anbieter, welche diesen Produkttypen betreiben
[gemKPT_Betr]. Alle Hersteller und Anbieter von TI-Anwendungen, die
Schnittstellen der Komponente nutzen, oder Daten mit dem Produkttypen
TI-Messenger-Client austauschen oder solche Daten verarbeiten, müssen dieses
Dokument ebenso berücksichtigen.

### 1.3 Geltungsbereich

Dieses Dokument enthält normative Festlegungen zur Telematikinfrastruktur des
deutschen Gesundheitswesens. Der Gültigkeitszeitraum der vorliegenden Version
und deren Anwendung in Zulassungs- oder Abnahmeverfahren wird durch die gematik
GmbH in gesonderten Dokumenten (z. B. gemPTV_ATV_Festlegungen,
Produkttypsteckbrief, Anbietertypsteckbrief, u.a.) oder Webplattformen (z. B.
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

Spezifiziert werden in dem Dokument die von dem Produkttyp bereitgestellten
(angebotenen) Schnittstellen. Benutzte Schnittstellen werden hingegen in der
Spezifikation desjenigen Produkttypen beschrieben, der diese Schnittstelle
bereitstellt. Auf die entsprechenden Dokumente wird referenziert (siehe auch
Anhang, Kap. ).

Die vollständige Anforderungslage für den Produkttyp ergibt sich aus weiteren
Konzept- und Spezifikationsdokumenten, diese sind in dem Produkttypsteckbrief
des Produkttyps TI-Messenger verzeichnet.

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

Der TI-Messenger-Client wird als eine Anwendung (oder eingebettet in bestehende
Anwendungen) auf dem Endgerät eines Nutzers installiert und ermöglicht eine
sichere, chatbasierte Kommunikation mit anderen Teilnehmern des
TI-Messenger-Dienstes. Der TI-Messenger-Client folgt den offenen Standards des
Kommunikationsprotokolls Matrix und synchronisiert, durch die Matrix Foundation
festgelegte, JSON-Objekte mit Matrix-Homeservern, welche als Teil der
TI-Messenger-Fachdienste bereitgestellt werden.

Die Kommunikation zwischen Teilnehmern des TI-Messenger-Dienstes erfolgt
Ende-zu-Ende verschlüsselt in Räumen. Die Nachrichten werden auf dem
jeweiligen TI-Messenger-Client erstellt und Ende-zu-Ende verschlüsselt
versendet. Die Schlüssel zur Entschlüsselung werden nur mit verifizierten
Geräten innerhalb des jeweiligen Raumes geteilt. Die Nachrichten werden
verschlüsselt auf dem jeweiligen Matrix-Homeserver gespeichert. Die
beteiligten Homeserver können die Nachrichten nicht entschlüsseln.

Die Kommunikation zwischen einem TI-Messenger-Client und einem
TI-Messenger-Fachdienst erfolgt über die Messenger-Proxies. Auf den
Messenger-Proxies findet die TLS-Terminierung der Verbindungen von den
TI-Messenger-Clients statt. Die TI-Messenger-Proxies erlauben nur das Anmelden
eines Nutzers durch zugelassene TI-Messenger-Clients. Dies wird ermöglicht,
indem während des Logins ein auf dem Client hinterlegtes Zertifikat für den
Login verwendet wird. Ein TI-Messenger-Client überprüft während des 
Logins, ob es sich um einen zugelassenen Matrix-Homeserver handelt.

Die folgende Abbildung "Systemüberblick (Vereinfachte Darstellung)" zeigt einen
Systemüberblick aller am TI-Messenger beteiligten Teilkomponenten in
vereinfachter Form.

![Img-001][Img-001]

### 3 Systemkontext

Der folgende Abschnitt setzt den TI-Messenger-Client in den Systemkontext des
TI-Messenger-Dienstes.

### 3.1 Nachbarsysteme

Die folgende Abbildung zeigt die benachbarten Komponenten des
TI-Messenger-Clients:

![Abbildung-2][Abbildung-2]

Die im Folgenden benannten Nachbarsysteme des TI-Messenger-Clients werden in der
[gemSpec_TI-Messenger-Dienst] und [gemSpec_TI-Messenger-FD] hinreichend
beschrieben. Die in diesem Dokument zum jeweiligen Nachbarsystem genannten
Punkte sollen an dieser Stelle die für das Funktionieren des
TI-Messenger-Clients benötigten Funktionen benennen.

<table><tr><th>
Komponente

</th><th>
Funktion

</th></tr><tr><td>
Push-Gateway

</td><td>
 ---> UL

</td></tr><tr><td>
Messenger-Service

</td><td>
 ---> UL

</td></tr><tr><td>
Registrierungs-Dienst

</td><td>
Der TI-Messenger-Client benötigt für diverse Aktionen eine Verbindung zum
Registrierungs-Dienst. Dazu gehören:

 ---> UL

</td></tr><tr><td>
IDP-Dienst

</td><td>
 ---> UL

</td></tr><tr><td>
VZD-FHIR-Directory

</td><td>
 ---> UL

</td></tr><tr><td>
TI-Messenger-Client

</td><td>
Für den Aufbau einer Kommunikation ohne das VZD-FHIR-Directory kann der
TI-Messenger-Client eine direkte Verbindung zu einem anderen
TI-Messenger-Client aufbauen. Ziel dieser Verbindung ist der Austausch der MXID
und PASSporT, damit ein

Invite Request

durch die jeweiligen Messenger-Services validiert werden kann.

</td></tr><tr><td>
Push-Dienst 

</td><td>
Push-Dienste sind Services von Push-Anbietern und werden für die native
Unterstützung von Push-Benachrichtigungen auf der Mehrzahl mobiler Geräte
benötigt.

</td></tr></table>

### 3.2 TI-Messenger-Clients für unterschiedliche Nutzergruppen

Gemäß der Architektur des TI-Messenger-Dienstes wird zwischen zwei Arten von
TI-Messenger-Clients unterschieden. Die Unterscheidung ergibt sich
ausschließlich aus der Sicht der Nutzer. Jeder Anbieter eines
TI-Messenger-Fachdienstes MUSS für seine Nutzergruppen TI-Messenger-Clients in
unterschiedlicher Ausprägung anbieten.  Im Folgenden werden die beiden
Ausprägungen beschrieben:

TI-Messenger-Client mit Administrationsfunktionen

Der TI-Messenger-Client mit Administrationsfunktionen ist ein Client für
Administratoren einer Organisation. Dieser Client dient zur komfortablen
Verwaltung der jeweiligen Messenger-Services bei einem TI-Messenger-Fachdienst
sowie der Organisationseinträge auf dem VZD-FHIR-Directory. Mit dem
Org-Admin-Client besteht die Möglichkeit mittels SMC-B Schreibzugriffe auf das
VZD-FHIR-Directory zu erhalten und im Namen der Organisation FHIR-Ressourcen
zur Verfügung zu stellen oder zu bearbeiten. Administratoren einer
Organisation haben die Möglichkeit mittels des TI-Messenger-Clients mit
Administrationsfunktionen Benutzer und Geräte auf dem jeweiligen
Messenger-Service zu verwalten. Es besteht ebenfalls die Möglichkeit über den
Org-Admin-Client Sessions von angemeldeten Geräten auf dem Messenger-Service
zu invalidieren oder zu verifizieren.

TI-Messenger-Client für Nutzer

Der TI-Messenger-Client für Nutzer unterstützt die meisten aller, durch die
Matrix-Spezifikation festgelegten Funktionalitäten eines Matrix-Messengers.
Nutzer können mit Hilfe des TI-Messenger-Clients Ende-zu-Ende-verschlüsselte
Chatnachrichten senden und empfangen. Innerhalb der Chaträume erfolgt der
Zugriff auf Chatverläufe, oder das Austauschen von Medien. Ebenfalls besteht
für Nutzer die Möglichkeit eigene Geräte und Geräte von Gesprächspartnern
zu verifizieren und das VZD-FHIR-Directory nach Organisationen zu durchsuchen,
um eine neue Chatkonversation mit einer Organisation zu starten. Es ist den
Herstellern freigestellt wie die Oberfläche gestaltet wird. So besteht
beispielsweise die Möglichkeit Chaträume nach unterschiedlichen
Verwendungszwecken zu organisieren. HBA-Inhaber haben zusätzlich die
Möglichkeit, die eigene MXID als Kontaktadresse des bereits vorhandenen
Practitoner-Eintrages zu setzen. Das Eintragen der MXID gewährt die Suche nach
anderen, auf dem VZD-FHIR-Directory eingetragenen HBA-Inhabern und ermöglicht
das Auffinden durch andere HBA-Inhaber. 

### 3.3 TI-Messenger-Clients für unterschiedliche Plattformen

Anbieter eines TI-Messenger-Clients MÜSSEN einen mobilen- und einen
desktopfähigen TI-Messenger-Client zur Verfügung stellen.
TI-Messenger-Clients haben je nach Installationsort (Mobil/Stationär)
unterschiedliche Anforderungen an Sicherheit, Datenschutz und Funktionen. Im
Folgenden werden die zu unterstützenden Plattformen beschrieben:

Mobil

Es handelt sich hierbei um einen TI-Messenger-Client, der speziell für die
Nutzung auf mobilen Geräten entwickelt wurde. Dabei handelt es sich um eine
native mobile Anwendung oder eine Integration in eine bestehende native
Anwendung. Die mobile Anwendung MUSS die betriebssystemseitigen Funktionen in
Bezug auf Sicherheit nutzen und sicherstellen, dass die Speicherung von Daten
getrennt und verschlüsselt vom Dateisystem erfolgt. Ein unerlaubter Zugriff
durch Dritte MUSS aktiv verhindert werden. 

Web

Der TI-Messenger-Client KANN als Web-Frontend für den stationären Einsatzzur
Verfügung gestelltwerden. Es MUSS sichergestellt werden, dass die
Web-Applikation vor unerlaubten Zugriff durch andere Nutzer geschützt wird. Es
MUSS sichergestellt werden, dass bei Aufruf des Web-Frontends durch Nutzer auf
dem Mobilgerät ein entsprechender Nutzungshinweis angezeigt wird.

Desktop

Der TI-Messenger-Client KANN als native- oder Web-Applikation für
Desktop-Geräte zur Verfügung gestellt werden.

Integriert

Für die Nutzung des TI-Messenger-Dienstes KANN die Integration eines
TI-Messenger-Clients in existierende Primärsysteme erfolgen. Diese
Primärsysteme können sowohl mobile als auch stationäre Anwendungen sein.

### 4 Übergreifende Festlegungen

### 4.1 Datenschutz und Sicherheit

Für die datenschutzrechtlichen Anforderungen an den TI-Messenger wird auf die
Stellungnahme der Konferenz der unabhängigen Datenschutzaufsichtsbehörden des
Bundes und der Länder vom 29. April 2021 zum Thema "Technische
Datenschutzanforderungen an Messenger-Dienste im Krankenhausbereich" verwiesen.
Die Inhalte der Stellungnahme werden hier zusammenfassend und vereinfachend als
Akzeptanzkriterium an den TI-Messenger-Client dargestellt. Anforderungen, die
durch andere Systemkomponenten sichergestellt werden, sind hier nicht
dargestellt.

**ML-124880 - Anforderungen aus der Konferenz der unabhängigen
Datenschutzaufsichtsbehörden**

 ---> UL

 ---> UL

 ---> UL

 ---> UL

 ---> UL

 ---> UL

 ---> UL

 ---> UL

 ---> UL

 ---> UL

 ---> UL

 ---> UL

 ---> UL

 ---> UL

 ---> UL

**[\<=]**

**ML-123584 - Authentisierung des Nutzers gegenüber dem TI-Messenger-Client**

Der TI-Messenger-Client MUSS über ein 2-Faktor-Authentisierungsverfahren
verfügen, um sich zu authentisieren gibtder Nutzer bei jedem Start der
Applikation eine sechsstellige PIN ein, um die Applikation zu entsperren. Nach
jeder Abmeldung, jedem Benutzerwechsel, jedem Schließen der Applikation, oder
spätestens 12Stunden nach letzter Entsperrung MUSS diese Authentisierung
erneut vorgenommen werden. Alternativ zum Authentisierungsmittel PIN sind auch
die Mittel Biometrie, starke Passphrase oder Fido-Token zulässig. Falls das
Merkmal Biomentrie gewählt wird, MUSS es den Vorgaben von [BSI-TR-03166] Kap.
2.3.1.5 oder 2.3.1.6 genügen. Als zweiten Faktor MUSS der TI-Messenger-Client
prüfen, ob er auf dem Gerät gestartet wurde, an welches er gebunden ist. Für
Webclients entfällt diese Authentisierung.Diese Funktionen DÜRFEN NICHT
abschaltbar sein und MÜSSEN unabhängig von den Entsperrfunktionen der
Endgeräte sein.Der Hersteller SOLL eine Sperre implementieren, die nach
längerer Inaktivität an Webclients die weitere Nutzung verhindert, bis sich
erneut wie zuvor beschrieben authentisiert wird. Die nötige Dauer der
Inaktivität MUSS durch den Nutzer konfigurierbar und auf eine Stunde
voreingestellt sein.Der TI-Messenger-Client MUSS den Nutzer bei Erstverwendung
des TI-Messenger-Clients, falls das Merkmal PIN oder Passphrase gewählt wurde,
dazu zwingen eine solche festzulegen. Dabei ist technisch zu prüfen, dass ein
PIN oder Passphrase entsprechend sicher ist. Dies kann beispielsweise durch das
Anzeigen von Fortschrittbalken dem Nutzer dargestellt werden. Dieser wird erst
grün, sobald eine entsprechende Güte erreicht wurde.Der Hersteller KANN eine
Funktion implementieren, die zufallsgenerierte Vorschläge für PIN oder
Passphrase erstellt. Diese Vorschläge MÜSSEN auf sichere Erzeugung von
Zufallszahlen gemäß [gemSpec_Krypt] basieren. **[\<=]**

**ML-123585 - Verhinderung der Erstellung von Screenshots**

Mobile TI-Messenger-Clients MÜSSENScreenshots und Screencapturing verhindern,
sofern das Betriebssystem dies zulässt, oder Nutzer nach Aufnahme eines
Screenshots klar darauf hinweisen, dass dieser nicht durch den TI-Messenger
geschützt werden kann. **[\<=]**

**ML-123589 - Mandantenfähigkeit von Clients**

Hersteller des TI-Messenger-Clients MÜSSEN sicherstellen, dass
TI-Messenger-Clients eine geeignete Mandantentrennung unterstützen, die
verhindert, dass bei geteilten Endgeräten ein Nutzer des TI-Messenger-Clients
auf Daten oder Funktionen der TI-Messenger-Client-Devices eines anderen Nutzers
auf diesem Gerät zugreifen kann. **[\<=]**

**ML-123610 - Datenschutzfreundliche MXIDs**

Der TI-Messenger-Client MUSS sicherstellen, dass MXIDs so generiert werden,
dass sie keine personenbezogenen Daten als Klarinformation beinhalten. Nutzer
des TI-Messenger haben keinen Einfluss auf die Bildung der MXID. **[\<=]**

**ML-123583 - Informationspflicht bzgl. Gefahren unsicherer Endgeräte**

Der TI-Messenger-Client MUSS den Nutzer in einem Hinweistext auf die Gefahren
hinweisen, die bei einem Betrieb des Clients auf Hardware, die nicht unter der
Kontrolle des Nutzern steht, gegeben sind. Das betrifft neben geteilten
Endgeräten ohne IT-Security-Überwachung insbesondere öffentlich zugängliche
Endgeräte. Der Nutzer MUSS die Empfehlung erhalten auf solchen Geräten den
TI-Messenger-Client nicht zu nutzen. **[\<=]**

**ML-123586 - Key-Sharing zwischen Geräten eines Nutzers**

Um Synchronisation von Nachrichteninhalten zwischen mehreren Devices eines
Nutzers zu ermöglichen, verfügt Matrix über vorgesehene
Key-Sharing-Funktionalität. Der Hersteller MUSS die Matrix Vorgabe SHOULD
"Key-Sharing nur für verifizierte Geräte" als MUST umsetzen. **[\<=]**

**ML-124004 - Key-Sharing zwischen Geräten innerhalb eines Chatraums**

Herstellerdes TI-Messenger-Clients MÜSSEN sicherstellen, dass
TI-Messenger-Clients über eine Funktion verfügen innerhalb eines Chatraums
Key-Sharing Anfragen an andere Geräte zu stellen und Key-Sharing Anfragen von
anderen Geräten anzunehmen oder abzulehnen. **[\<=]**

**ML-123587 - Versand von Dateien mittels Matrix**

Für den Versand von Dateien gemäß der Matrix-Spezifikation über den
TI-Messenger gilt:

 ---> UL

Sofern der Hersteller eine Funktion implementiert, Dokumente direkt über den
TI-Messenger-Client ohne Nutzung von Third-party software anzuzeigen, MUSS
diese die Ausführung von aktiven Inhalten verhindern. Ebenfalls MUSS diese
Funktion es ermöglichen zugehörige Metadaten auch ohne Öffnen oder
Herunterladen der Datei selbst einzusehen.

Der Nutzer MUSS darüber informiert werden, dass Dokumente Schadsoftware
enthalten können und welche Maßnahmen der Nutzer zum Selbstschutz vornehmen
kann.

Der TI-Messenger-Client MUSS, wenn er Dokumenteninhalte direkt anzeigt,
Maßnahmen zum Schutz vor Schadsoftware in den Dokumenten umsetzen. **[\<=]**

Maßnahmenvorschläge:

 ---> UL

**ML-123588 - Abschottung der TI-Messengerinhalte**

Mobile TI-Messenger-Clients MÜSSEN sicherstellen, dass Daten, die lokal
gespeichert werden, nicht im allgemeinen Speicher des Geräts abgelegt werden,
sondern in einem TI-Messenger-Client spezifischen Speicherbereich auf dem
Endgerät.Mobile TI-Messenger-Clients MÜSSEN sicherstellen, dass andere
Applikationen auf den Endgeräten nicht auf Inhalte des TI-Messengers zugreifen
können. Hierzu SOLL der Hersteller eine Abschottung des Speichers, den der
TI-Messenger für Nutzerdaten belegt, implementieren. Hierzu genügen die vom
Betriebssystem i.d.R. zur Verfügung gestellten Mittel.Webclients MÜSSEN
sicherstellen, dass sensible Daten im Browser (z. B. OLM-Keys, ACCESS_TOKEN)
nicht durch andere Applikationen ausgelesen werden können.TI-Messenger-Clients
MÜSSEN ein Öffnen von über den TI-Messenger empfangenen Dateien durch
Drittprogramme ermöglich. Hierbei MUSS er sicherstellen, dass eine solche
Ausleitung von Daten nur ausgelöst durch den TI-Messenger-Client erfolgt. Der
TI-Messenger-Client KANN eine Funktion enthalten, mittels derer empfangene
Dateien außerhalb des dedizierten Speichers im Gerätespeicher abgelegt
werden. Der TI-Messenger-Client MUSS sicherstellen, dass Nutzer bei Verwenden
einer solchen Funktion geeignet darüber informiert werden, dass sie Daten aus
dem geschützten Bereich des TI-Messengers hinausbewegen. **[\<=]**

**ML-123590 - Sicherheitskritische Updates**

Anbieter des TI-Messenger-Clients MÜSSEN sicherstellen, dass Nutzer über die
Veröffentlichung von Updates für ihre TI-Messenger-Clientsoftware informiert
werden. Bei sicherheitskritischen Updates MÜSSEN sie sicherstellen, dass nach
einer geeigneten Frist eine weitere Nutzung des TI-Messenger-Clients ohne
vorheriges Sicherheitsupdate nicht möglich ist. Hierzu genügt eine
clientseitige Sperre im Gegensatz zu einem Nachweis gegenüber dem
Homeserver. Die Möglichkeit weiter Updates einzuspielen MUSS in diesem Fall
weiterhin gegeben sein.Nutzer MÜSSEN geeignet darüber informiert werden, dass
sie sicherheitskritische Updates installieren müssen um den
TI-Messenger-Client weiterhin zu nutzen.Der Hersteller des TI-Messenger-Clients
MUSS die gematik bei Veröffentlichung einer neuen Produktversion informieren
und eine Erklärung zur sicherheitstechnischen Eignungliefern. **[\<=]**

**ML-124867 - Resilienz von Clients**

Hersteller MÜSSEN sicherstellen, dass TI-Messenger-Clients resilient auf
unerwartete Eingaben reagieren. **[\<=]**

**ML-123591 - Zusatzfunktionen für TI-Messenger-Clients**

Hersteller des TI-Messenger-Clients MÜSSEN sicherstellen, dass alle
implementierten Funktionen, die über den gewöhnlichen Funktionsumfang eines
TI-Messenger-Clients hinausgehen die Sicherheit des Produkts nicht gefährden
und die Interoperabilität mit anderen TI-Messenger-Produkten erhalten.Der
Hersteller MUSS sicherstellen, dass alle Zusatzfunktionen des
TI-Messenger-Clients von den Basisfunktionen unterscheidbar sind. **[\<=]**

Zusatzfunktionen sind Funktionen des TI-Messenger-Clients und verwenden den
gleichen Speicherbereich, sofern es sich nicht um Drittprogramm konzipierte
Zusatzfunktionen handelt.

**ML-123629 - Device Verification, Cross-Signing und SSSS für
TI-Messenger-Clients**

Hersteller MÜSSEN sicherstellen, dass die Funktionen Cross-Signing und Secure
Secret Storage and Sharing (SSSS) zur Device Verification unterstützt
werden. Es MUSS die Spezifikation 12.11.2
(https://spec.matrix.org/unstable/client-server-api/#device-verification) und
12.11.3
(https://spec.matrix.org/unstable/client-server-api/#sharing-keys-between-devices)
vollständig befolgt werden. **[\<=]**

**ML-123861 - Ende-zu-Ende-Verschlüsselung**

Hersteller MÜSSEN sicherstellen, dass eine vollständige
Ende-zu-Ende-Verschlüsselung auf Basis von OLM/MEGOLM unterstützt wird. Dazu
MUSS der Spezifikation 12.11
(https://spec.matrix.org/unstable/client-server-api/#end-to-end-encryption )
und 12.12 (https://spec.matrix.org/unstable/client-server-api/#secrets )
gefolgt werden. **[\<=]**

**ML-124006 - Explizites Verbot von Profiling für TI-Messenger-Clients**

Hersteller und Anbieter von TI-Messenger-Komponenten DÜRFEN NICHT Daten zu
Profiling-Zwecken sammeln. Dies betrifft insbesondere eine Überwachung welche
Akteure mit welchen anderen Akteuren kommunizieren.  
Die gematik kann nach §
331 Abs. 2 SGB V Daten festlegen, die Anbieter von Komponenten und Dienste der
gematik offenzulegen bzw. zu übermitteln haben, sofern diese erforderlich
sind, um den gesetzlichen Auftrag der gematik zur Überwachung des Betriebs zur
Gewährleistung der Sicherheit, Verfügbarkeit und Nutzbarkeit der
Telematikinfrastruktur zu erfüllen. Nur die hierfür erforderlichen
personenbezogenen Daten dürfen von den Anbietern und Herstellern als Ausnahme
vom Profilingverbot erhoben und ausschließlich für den genannten Zweck
verwendet werden. **[\<=]**

**ML-123593 - Einbringung und Speicherung von Schlüsseln und Token**

Hersteller von TI-Messenger-Clients MÜSSEN sicherstellen, dass Schlüssel und
Token sicher in den Client eingebracht werden. Hierzu genügt eine Prüfung des
Prozesses.Herstellervon TI-Messenger-Clients MÜSSEN technisch sicherstellen,
dass Schlüssel und Token nicht in andere Speicher ausgelagert werden können,
als die dafür vorgesehenen Speicher der TI-Messenger-Clients oder dem SSSS des
beteiligten Homeservers. **[\<=]**

**ML-123596 - Verwendung von TLS zur Kommunikation mit Fachdienst und
VZD-FHIR-Directory**

Der Hersteller MUSS sicherstellen, dass der TI-Messenger-Client in der Lage ist
Verbindungen zu anderen Bestandteilen des TI-Messengers über TLS aufzubauen.
Hierzu gelten die Festlegungen der [gemSpec_Krypt]. Entsprechende Anforderungen
werden dem Produkttypsteckbrief zugeordnet. **[\<=]**

**ML-123597 - Löschfunktionen für TI-Messenger-Inhalte**

Der Hersteller von TI-Messenger-Clients MUSS eine automatisierte Löschfunktion
für TI-Messenger-Client-Nachrichten implementieren. Diese MUSS eine zumutbare
voreingestellte Löschfrist enthalten, welche für Nutzer konfigurierbar ist.
Die Löschfrist MUSS hierbei auf den minimal einstellbaren Wert initialisiert
sein.Nach Verstreichen der eingestellten Löschfrist MÜSSEN Gesprächsinhalte
aus dem TI-Messenger-Client sicher gelöscht werden. Der Hersteller MUSS
zusätzlich eine nachrichtenbasierte Löschfunktion vorsehen, die es Nutzern
erlaubt ihre eigenen Nachrichten händisch nicht nur vom eigenen
TI-Messenger-Client, sondern auch aus dem Room State zu löschen. **[\<=]**

**ML-123607 - Privacy by Default**

Der Hersteller eines TI-Messenger-Clients MUSS für die Standardeinstellungen
des TI-Messenger-Clients stets die datenschutzfreundlichste Voreinstellung
konfigurieren. **[\<=]**

**ML-123608 - Verwendung von OWASP Mobile**

Der Hersteller eines mobilenTI-Messenger-Clients MUSS bei der Entwicklung von
TI-Messenger-Clients die Maßnahmen und Vorgaben der aktuellen Version der
OWASP-Top-10-Mobile-Risiken [OWASPMobileTop10] umsetzen. Hierbei SOLLEN die
Vorgaben der Prüfvorschrift für den Produktgutachter des „ePA-Frontend des
Versicherten“ analog für den TI-Messenger-Client umgesetzt werden, mit
Ausnahme folgender Punkte:Darüber hinaus sind folgende Punkte der
OWASP-Top-10-Mobile-Risiken nur für eingeschränkte Clients relevant. Andere
Client-Typen KÖNNEN auf die Umsetzung dieser Punkte verzichten: **[\<=]**

**ML-123630 - Sicherheitsrisiken von Software Bibliotheken minimieren**

Der TI-Messenger-Client MUSS Maßnahmen umsetzen, um die Auswirkung von
unentdeckten Schwachstellen in benutzten Software-Bibliotheken zu
minimieren.Hinweis:  Beispielmaßnahmen sind in [OWASP Proactive Control#C2]
zu finden. Das gewählte Verfahren muss die gleiche Wirksamkeit aufweisen, wie
die Kapselung gemäß [OWASP Proactive Control#C2 Punkt 4]. **[\<=]**

**ML-123606 - Ausführung nur von begutachtetem Code**

Der Hersteller des TI-Messenger-Clients MUSS technisch sicherstellen, dass nur
im Rahmen eines Produktgutachtens begutachteter Code ausgeführt wird oder
Code-Änderungen nach Vorgaben der gematik durch den Hersteller als nicht
zulassungsrelevant bewertet wurden.Der Hersteller MUSS die Software-Komponenten
des TI-Messenger-Clients, die nicht vom Hersteller selbst entwickelt oder zur
Entwicklung beauftragt werden (z.B. TLS-Bibliotheken oder
Matrix-Implementierungen), aus bekannten und vertrauenswürdigen Quellen
beziehen. **[\<=]**

**ML-123600 - Sichere Softwareverteilung**

Der Hersteller eines TI-Messenger-Clients MUSS Nutzer über die
vertrauenswürdigen Quellen informieren, von denen Nutzer den
TI-Messenger-Client beziehen können und wie sie die Vertrauenswürdigkeit der
Quelle erkennen können. Der Hersteller MUSS sicherstellen, dass der Nutzer bei
Erstbezug eines TI-Messenger-Clients die Authentizität der vertrauenswürdigen
Bezugsquelle verifizieren kann. Der TI-Messenger-Client MUSS sicherstellen,
dass Updates nur von bekannten und vertrauenswürdigen Quellen bezogen werden,
nachdem die Authentizität der Quelle technisch erfolgreich verifiziert wurde.
**[\<=]**

**ML-123602 - Lokale Ausführung des TI-Messenger-Clients**

Der TI-Messenger-Client MUSS sicherstellen, dass alle
TI-Messenger-Clientspezifischen Anteile lokal auf dem Gerät des Nutzers
ausgeführt werden, sofern die Betriebsumgebung des Clients dies zulässt.
**[\<=]**

**ML-123605 - Datenschutzkonformes Tracking**

Der TI-Messenger-Client DARF NICHT Werbe-Tracking verwenden.Im Folgenden wird
unter Tracking Usability-Tracking sowie Crash-Reporting verstanden.Der
TI-Messenger-Client MUSS sicherstellen, falls er Tracking-Funktionen
implementiert, dass in den übermittelten Tracking-Informationen keine
Sicherheitsmerkmale, wie Device-ID oder Daten mit Sicherheitsbezug, enthalten
sind.Der Datenschutzrechtlich-Verantwortliche für
denTI-Messenger-Clients MUSS die Verarbeitung und Auswertung etwaiger
gesammelten Tracking-Daten des TI-Messenger-Clients selbst durchführen und
nicht von einem Drittanbieter durchführen lassen.Der TI-Messenger-Client MUSS
sicherstellen, falls er Tracking-Funktionen nutzt, dass die Tracking-Daten
keine Daten enthalten, die natürliche Personen direkt identifizieren.Der
TI-Messenger-Client MUSS, falls er Tracking-Funktionen ohne Einwilligung des
Nutzersnutzt, sicherstellen, dass die Tracking-Daten

 ---> UL

Der TI-Messenger-Client MUSS, falls er Tracking-Funktionen ohne Einwilligung des
Nutzers nutzt, den Nutzer über das Tracking im TI-Messenger-Client in
verständlicher und leicht zugänglicher Form sowie in einer klaren und
einfachen Sprache informieren, bevor die Trackingdaten erhoben werden.

Der TI-Messenger-Client MUSS, falls er Tracking-Funktionen ohne Einwilligung des
Nutzers nutzt, für jede Clientnutzung neue Nutzungsidentifier zufällig
generieren. Der Nutzer MUSS in der Lage sein jederzeit die Neugenerierung
dieser Identifier zu erzwingen.

Der TI-Messenger-Client MUSS, falls er Tracking-Funktionen mit Verknüpfung der
Tracking-Daten mehrerer Clientnutzungen implementiert, technisch sicherstellen,
dass diese Tracking-Funktionen bei der Installation des TI-Messenger-Clients
standardmäßig deaktiviert sind und nur nach expliziter Einwilligung durch den
Nutzer aktiviert werden (Opt-in). Die Ablehnung der Nutzung solcher Funktionen
darf die Standardfunktionen des TI-Messenger-Clients nicht einschränken.

 

Falls solche Funktionen implementiert werden, MUSS den Nutzern vor der
Einwilligung in die Aktivierung dieser Tracking-Funktionen in verständlicher
und leicht zugänglicher Form sowie in einer klaren und einfachen Sprache
folgende Einwilligungsinformationen angezeigt werden:

 ---> UL

Diese Funktionen DÜRFEN NICHT aktiviert werden, bis eine explizite Einwilligung
durch den Nutzer erfolgt ist und MUSS jederzeit durch diese deaktivierbar sein.

Ein Verweis auf AGBs oder Nutzungsbedingungen des TI-Messengers ist hierzu NICHT
ausreichend. Unter verständlicher und leicht zugänglicher Form wird explizit
eine kurze Erklärung in einfacher und nicht juristischer Sprache verstanden,
die direkt im TI-Messenger-Client angezeigt wird.

Der Hersteller DARF NICHT wiederholt beim Nutzer anfragen um eine Einwilligung
durch Belästigung zu erzwingen. Nach einmaliger Ablehnung durch den Nutzer
MUSS jede Anzeige des Dialogs explizit durch den Nutzer initiiert werden. **[\<=]**

**ML-123632 - CC-Evaluierung als Ersatz für Gutachten**

Falls der Hersteller entscheidet, eine CC-Zertifizierung statt eines
Produktgutachtens durchzuführen, MUSS der Herstellerbei der Einreichung eines
CC-Zertifizierungsantrags sein Security Target Dokument der gematik zur
Verfügung stellen. In diesem müssen mindestens beschrieben sein:

 ---> UL

**[\<=]**

**ML-123631 - Sichere Produktentwicklung und Nachweise**

Der Hersteller MUSS innerhalb des Produktlebenszyklus (Entwicklung, Betrieb,
Außerbetriebnahme) seines Produktes Sicherheitsaktivitäten integrieren und
anwenden, d. h. in einschlägigen Fachkreisen anerkannte, erprobte und
bewährte Regeln anwenden.Der Hersteller MUSS die Sicherheits- und
Datenschutzmaßnahmen für sein Produkt in einem Sicherheits- und
Datenschutzkonzept dokumentieren und auf Verlangen der gematik zur Verfügung
stellen.Der Hersteller MUSS einen Testplan für Sicherheitstests erstellen und
auf Verlangen der gematik zur Verfügung stellen. Dieser MUSS umgesetzt werden
und der gematik bei jeder Veröffentlichung einer Produktversion als neuer
Bericht vorgelegt werden.Der Hersteller des TI-Messenger-Clients desNutzersMUSS
während der Entwicklung des Produktes implementierungsspezifische
Sicherheitsanforderungen dokumentieren und umsetzen.Der Hersteller MUSS ein
sicherheitsrelevantes Softwarearchitektur-Review durchführen und
identifizierte Architekturschwachstellen beheben. Dieses Review MUSS nach jeder
Architekturänderung mit Sicherheitsrelevanz wiederholt werden.Der Hersteller
MUSS eine Bedrohungsanalyse durchführen und Maßnahmen gegen die
identifizierten Bedrohungen implementieren.Der Hersteller MUSS während der
Entwicklung des Produktes sicherheitsrelevante Quellcode-Reviews oder
automatisierte sicherheitsrelevante Quellcode-Scans durchführen.Der Hersteller
MUSS während der Entwicklung des Produktes automatisierte
Sicherheitstests durchführen.Der Hersteller MUSS einen Schulungsplan zur
regelmäßigen Schulung von Entwicklern in sicherer Entwicklung und
Secure-Coding-Techniken dokumentieren und umsetzen.Der Hersteller MUSS alle
Entwickler des Produktes in sicherer Entwicklung und Secure-Coding-Techniken
schulen. Hierzu MUSS der Hersteller sicherstellen, dass alle Entwickler zu
Beginn der Entwicklung geschult sind. Er SOLL für diese anschließend auch
laufende Weiterbildung durchführen.Der Hersteller MUSS den verwendeten
sicheren Produktlebenszyklus und deren Teilprozesse dokumentieren und auf
Nachfrage der gematik zur Verfügung stellen. Die Dokumentation soll mindestens
die folgenden Sicherheitsaktivitäten beschreiben:

 ---> UL

Der Hersteller MUSS während der Entwicklung des Produktes einen Änderungs- und
Konfigurationsmanagementprozess verwenden. Das Änderungsmanagement umfasst
mindestens den Entscheidungsprozess über vorgeschlagene Änderungen und die
Autorisierung der Änderungen. Das Konfigurationsmanagement liefert mindestens
zu jedem Zeitpunkt die eindeutige Zusammensetzung des Produktes bezüglich
seiner eindeutigen Komponenten (Dritt-Software wie Bibliotheken und Frameworks)
und den vorgenommenen Änderungen an eigenen Komponenten.

Der Hersteller MUSS bei Veröffentlichung einer neuen Produktversion des
Produktes die Einhaltung der Herstellererklärung sicherheitstechnische Eignung
durch seinen Datenschutzbeauftragten verifizieren. **[\<=]**

**ML-124881 - Kein Schreibzugriff für Clients auf Room-States**

TI-Messenger-Clients MÜSSEN verhindern, dass Nutzer mittels Nutzereingaben
Informationen in Room-States bringen. Sobald durch die geplante
Matrix-Spec-Changes (MSCs) die Möglichkeit geschaffen wurde, vertrauliche
Informationen sicher im Room-State zu speichern, wird dies direkt durch die
Matrix-Spezifikation abgedeckt. **[\<=]**

### 4.2 Benutzerführung

Mittels einer geeigneten Benutzerführung wird eine hohe Akzeptanz des Nutzers
erreicht. Hierzu zählt eine einfache und selbsterklärende Bedienung der
Oberfläche, die sich an gängige auf dem Markt zu findenden
App-Design-Empfehlungen orientiert. Ebenfalls MÜSSEN alle infrage kommenden
Zielgruppen betrachtet werden. Es MÜSSEN folgende interoperablen Funktionen
durch den Hersteller bereitgestellt werden, um ein Mindestmaß an
Nutzererfahrung zu erreichen. 

Präsenzanzeige

Für eine Echtzeitnutzererfahrung, MÜSSEN TI-Messenger-Clients gemäß
[Präsenzanzeige] eine Präsenzanzeige für andere Gesprächspartner zur
Verfügung stellen. Die Präsenzanzeige MUSS an- und abschaltbar sein und MUSS
gemäß Privacy-by-default (Art. 25 Abs. 2 DSGVO und nachgelagert ML-123607)
standardmäßig deaktiviert sein.

Erwähnungen

TI-Messenger-Clients MÜSSEN es ermöglichen, dass über das Eingabefeld andere
Nutzer gemäß [Erwähnung] im jeweiligen Chatraum erwähnt werden können.
Dazu MUSS der TI-Messenger-Client eine entsprechende Nutzerliste anzeigen,
sobald der Nutzer ein neues Wort mit "@" startet, oder einen entsprechenden "@"
Knopf im Chatraum anbieten. TI-Messenger-Clients MÜSSEN Nutzererwähnungen
entsprechend als "Pile" in dem Chatraum anzeigen. Handelt es sich um einen
TI-Messenger-Client für mobile Geräte, oder Geräte mit Push-Funktionalität,
MUSS der Client eine entsprechende Push-Benachrichtigung anzeigen, wenn der
Nutzer die entsprechenden Push-Regeln eingestellt hat.

Lesebestätigungen

Lesebestätigungen dienen dem Ziel einen Aufschluss darüber zu geben, wann, ob
und von wem eine Nachricht innerhalb eines Chatraums gelesen wurde. Aus diesem
Grund MÜSSEN mobile TI-Messenger-Clients die Matrix-Spezifikation gemäß
[Lesebestätigungen] vollständig implementieren. TI-Messenger-Clients für
Nutzer MÜSSEN diese Funktion des Anzeigens und Sendens von
Lesebestätigungen vollständig implementieren. Der TI-Messenger-Client
MUSSFully-Readmarkersunterstützen. Lesebestätigungen MÜSSEN an- und
abschaltbar sein und MÜSSEN gemäß Privacy-by-default (Art. 25 Abs. 2 DSGVO
und nachgelagert ML-123607) standardmäßig deaktiviert sein.

Eingabebenachrichtigungen

Mobile TI-Messenger-Clients MÜSSEN die Matrix-Spezifikation gemäß
[Eingabebenachrichtigungen] vollständig implementieren. TI-Messenger-Clients
SOLLEN Nutzern anzeigen, wenn die Gegenseite eine Nachricht in einem Chatraum
schreibt. Die Eingabebenachrichtigungen MÜSSEN an- und abschaltbar sein und
MÜSSEN gemäß Privacy-by-default (Art. 25 Abs. 2 DSGVO und nachgelagert
ML-123607) standardmäßig deaktiviert sein. 

Barrierefreiheit

**ML-123582 - Standards zur Barrierefreiheit**

Hersteller eines TI-Messenger-Clients SOLLEN die in [ISO 9241] aufgeführten
Qualitätsrichtlinien zur Sicherstellung der Ergonomie interaktiver Systeme und
Anforderungen aus der Verordnung zur Schaffung barrierefreier
Informationstechnik nach dem Behindertengleichstellungsgesetz
(Barrierefreie-Informationstechnik-Verordnung – [BITV 2.0]) beachten.
**[\<=]**

### 4.3 Konfiguration des TI-Messenger-Clients

Im folgenden Kapitel werden alle zu konfigurierenden Funktionen beschrieben, die
im TI-Messenger-Client durch den Nutzer konfigurierbar sein müssen.

Einstellung von Push-Benachrichtigungen

TI-Messenger-Clients MÜSSEN über eine Funktion verfügen, um
Push-Benachrichtigungen auf einem Gerät konfigurieren zu können. Dazu MÜSSEN
neben [Push-Rules] auch geräteseitige Einstellungsmöglichkeiten den Nutzern
zur Verfügung gestellt werden.

Nutzer ignorieren

TI-Messenger-Clients MÜSSEN über eine Funktion verfügen, um Nachrichten
anderer Nutzer zu ignorieren. Daher MÜSSEN mobile TI-Messenger-Clients die
Matrix-Spezifikation gemäß [Nutzer ignorieren] vollständig implementieren.

TI-Messenger-Clients MÜSSEN eine Liste aller ignorierten Nutzer anzeigen und
die Möglichkeit bieten das Ignorieren von Nutzern rückgängig zu machen.

Raum-Historie

Mobile TI-Messenger-Clients MÜSSEN die Matrix-Spezifikation gemäß [Raum
Historie] vollständig implementieren.

TI-Messenger-Clients MÜSSEN Einstellungen zur Verfügung stellen, um die
Sichtbarkeit der Raum-Historie festlegen zu können. Als Standard SOLLTE die
Raum-Historie ab dem Zeitpunkt des Beitritts sichtbar sein.

### 4.4 Test

Produkttests zur Sicherstellung der Konformität mit der Spezifikation sind
vollständig in der Verantwortung der Anbieter/Hersteller des
TI-Messenger-Clients. Die gematik konzentriert sich bei der Zulassung auf das
Zusammenspiel der Produkte durch E2E- und IOP Tests.

Die eigenverantwortlichen Produkttests bei den Industriepartnern umfassen:

 ---> UL

Die Hersteller der TI-Messenger-Fachdienste MÜSSEN zusichern, dass die gematik
die Produkttests der Industriepartner in Form von Reviews der Testkonzepte,
Testspezifikationen, Testfälle sowie mit dem Review der Testprotokolle (Log-
und Trace-Daten) überprüfen kann.

Die gematik fördert eine enge Zusammenarbeit und unterstützt Industriepartner
dabei, die Qualität der Produkte zu verbessern. Dies erfolgt durch die
Organisation früher IOP-Tests, die Synchronisierung von Meilensteinen und
regelmäßige industriepartnerübergreifenden Test-Sessions. Die Test-Sessions
umfassen gegenseitige IOP- und E2E Tests.

Die gematik stellt eine TI-Messenger-Fachdienst Referenzimplementierung zur
Verfügung. Zur Sicherstellung der Interoperabilität zwischen verschiedenen
TI-Messenger-Fachdiensten innerhalb des TI-Messenger-Dienstes MUSS der
TI-Messenger-Fachdienst eines TI-Messenger-Anbieters gegen die
Referenzimplementierung (TI-Messenger-Client und TI-Messenger Fachdienst)
getestet werden.

**ML-124204 - Test des TI-Messenger-Clients gegen die Referenzimplementierung**

Der TI-Messenger-Client MUSS gegen die Referenzimplementierung erfolgreich
getestet werden. Die Testergebnisse sind der gematik vorzulegen. **[\<=]**

Die gematik testet in den Zulassungsverfahren auf Basis von Anwendungsfällen.
Dabei werden die Anwendungsfälle durchgespielt und es wird versucht viele
Funktionsbereiche und Teile der Anwendung mit einzubeziehen. Anschließend wird
mit den IOP Tests die Interoperabilität zwischen den verschiedenen Anbieter
nachgewiesen. Für das Zulassungsverfahren des TI-Messenger-Dienst müssen die
TI-Messenger-Clients und TI-Messenger FD bereitgestellt werden. Um einen
automatisierten Test für den TI-Messenger-Dienst zu ermöglichen, muss die
Test-App des TI-Messenger-Clients zusätzlich ein Testtreiber-Modul beinhalten,
welcher die Funktionalitäten der produktspezifischen Schnittstelle des
TI-Messenger-Clients über eine standardisierte Schnittstelle von außen
zugänglich macht und einen Fernzugriff ermöglicht.

![Abbildung-3][Abbildung-3]

**ML-124877 - Test-App des TI-Messenger-Clients und Testtreiber-Modul**

Die Test-App des TI-Messenger-Clients MUSS ein Testtreiber-Modul beinhalten,
welches eine Schnittstelle für automatisierte Tests anbietet. Diese
Schnittstelle wird durch die gematik spezifiziert und bereitgestellt. Das
Testtreiber-Modul MUSS die durch den TI-Messenger-Client – dem
Zulassungsgegenstand – über eine produktspezifische Schnittstelle angebotene
Funktionalität nutzen, um die Operationen der Schnittstellen umzusetzen.
**[\<=]**

Das Testtreiber-Modul darf die Ausgaben des TI-Messenger-Clients gemäß der
technischen Schnittstelle aufarbeiten, aber darf die Inhalte nicht
verfälschen. Die konkrete Ausgestaltung der Schnittstellen wird im Fachportal
der gematik und in GitHub zur Verfügung gestellt.

**ML-124878 - Beschränkung Einsatz Testtreiber-Modul**

Der produktive TI-Messenger-Client DARF ein Testtreiber-Modul NICHT enthalten.
**[\<=]**

Der Einsatz des Testtreiber-Moduls ist auf das Zulassungsverfahren in Test-Apps
beschränkt und darf nicht in Wirkbetriebs-Apps genutzt werden.

**ML-124879 - Keine Fachlogik in Testtreiber-Modul**

Das Testtreiber-Modul DARF NICHT die fachliche Logik des TI-Messenger-Clients
umsetzen.  **[\<=]**

### 4.5 Betriebliche Aspekte

Die Betriebsbereitschaft des bzw. der Clients vom TI-Messenger Anbieter bezieht
sich in diesem Kapitel auf serverseitige Systeme welche notwendig sind, damit
der Client vom Nutzer sicher-funktional betrieben werden kann. Der sichere
Betrieb im Sinne der Nutzung auf ihren Endgeräten des TI-Messenger-Clients
liegt letztendlich in der Verantwortung bei den Nutzern des TI-Messengers.

Der TI-Messenger-Anbieter MUSS seine Nutzer dabei unterstützen, einen sicheren
und funktionalen Betrieb der TI-Messenger-Clients zu ermöglichen.

Der TI-Messenger-Client MUSS mit einer vollumfänglich-funktionalen
Verfügbarkeit von 98 % betreibbar sein. 

Der Anbieter TI-Messenger MUSS sein Produkt TI-Messenger-Client mit einer
vollumfänglich-funktionalen Verfügbarkeit von 98% seinen Nutzern anbieten.

### 5 Funktionsmerkmale

Die Funktionen des TI-Messenger-Clients ergeben sich aus den Funktionen der
Matrix-Spezifikation. Die hier beschriebenen Funktionen MÜSSEN durch den
jeweiligen TI-Messenger-Client unterstützt werden. Funktionen, welche durch
Matrix bereitgestellt wurden, aber nicht Teil dieser Spezifikation sind und
keine Fallbacks bieten, DÜRFEN NICHT implementiert werden, um die
Interoperabilität zu gewährleisten.

### 5.1 Authentisierung

SSO Login

TI-Messenger-Clients MÜSSEN die Matrix-Spezifikation gemäß [SSO Login]
vollständig implementieren.

OpenID

TI-Messenger-Clients MÜSSEN die Matrix-Spezifikation gemäß [OpenID]
vollständig implementieren.

Gäste Accounts

Der Hersteller eines TI-Messenger-Client MUSS sicherstellen, dass eine
Erstellung von Gäste-Accounts verhindert wird.

### 5.2 Matrix-Client-Server-API

Die Kernbestandteile des TI-Messenger-Clients basieren auf der
Matrix-Client-Server-API. Diese umfasst neben dem eigentlichen Funktionsumfang
für einen Ad-hoc-Nachrichtendienst auch die Verwaltung der Sessions,
Benachrichtigungen etc., worauf in dieser Spezifikation nicht weiter
eingegangen wird. TI-Messenger-Clients MÜSSEN die Matrix-Client-Server-API
gemäß [Matrix Foundation#Client_Server API] umsetzen.

Room Upgrades

TI-Messenger-Clients MÜSSEN die Matrix-Spezifikation gemäß [Room Upgrades]
vollständig implementieren. TI-Messenger-Clients MÜSSEN mit Raum Upgrades
umgehen können. Der Nutzer SOLLTE NICHT bemerken, dass eine neue Raumversion
vorliegt.

Send-to-Device messaging

TI-Messenger-Clients MÜSSEN die Matrix-Spezifikation gemäß [Send-to-Device
messaging] vollständig implementieren und umsetzen.

Geräteverwaltung

TI-Messenger-Clients MÜSSEN eine Geräteverwaltung für die eigenen Geräte
eines Nutzers, für die Geräte anderer Nutzer in einem Chatraum, sowie für
die Geräte aller Nutzer eines Messenger-Services in der Rolle
desOrg-Adminunterstützen. Daher MÜSSEN TI-Messenger-Clients die
Matrix-Spezifikation gemäß [Geräteverwaltung] vollständig implementieren.

Ende-zu-Ende-Verschlüsselung

TI-Messenger-Clients MÜSSEN die Matrix-Spezifikation gemäß
[Ende-zu-Ende-Verschlüsselung] vollständig implementieren.
TI-Messenger-Clients MÜSSEN eine Ende-zu-End-Verschlüsselung entsprechend der
Matrix-Spezifikation unterstützen. Der Hersteller von TI-Messenger-Clients
MUSS verhindern, dass nicht Ende-zu-Ende verschlüsselten Nachrichten versendet
werden.

Reporting von Inhalten

TI-Messenger-Clients MÜSSEN die Matrix-Spezifikation gemäß
[Reporting-content] implementieren und den Nutzern die Möglichkeit geben,
unerwünschten Inhalt an Nutzer in der RolleOrg-Adminzu melden.

### 5.3 Instant Messaging

Instant Messaging MUSS von einem TI-Messenger-Client vollständig nach der
Matrix-Spezifikation gemäß [Instant Messaging] implementiert werden. Ein
TI-Messenger-Client MUSS sicherstellen, dass alle eingehenden und ausgehenden
Events in der richtigen chronologischen  Reihenfolge dem Nutzer angezeigt
werden. Ein TI-Messenger-Client MUSS eine Wiederholungslogik für das Senden
von Nachrichten unterstützen. TI-Messenger-Clients SOLLEN die MXID eines
Nutzers verstecken und SOLLEN den Displaynamen anzeigen. TI-Messenger-Clients
MÜSSEN Nutzer informieren, falls ein Event nicht oder fehlerhaft versendet
wurde.

Folgende Events und Msgtypes MÜSSEN unterstützt werden:

<table><tr><th>
Events

</th><th>
Msgtypes

</th></tr><tr><td>
m.room.message

</td><td>
m.text

</td></tr><tr><td>
m.room.name

</td><td>
m.emote

</td></tr><tr><td>
m.room.topic

</td><td>
m.notice

</td></tr><tr><td>
m.room.avatar

</td><td>
m.image

</td></tr><tr><td>
m.file

</td></tr><tr><td>
m.audio

</td></tr><tr><td>
m.location

</td></tr><tr><td>
m.video

</td></tr></table>

Nachrichten in Matrix können sowohl im Plaintext als auch in HTML-formatierter
Form versendet werden. Für den Fall, dass ein Client keine formatierten
Nachrichten unterstützt, ist ein Fallback im Plaintext für beispielsweise
Replies spezifiziert:

https://spec.matrix.org/unstable/client-server-api/#fallbacks-for-rich-replies 

TI-Messenger-Clients MÜSSEN Fallbacks für folgende Events unterstützen:

 ---> UL

Hinweis: Unter einem Fallback versteht man, dass der TI-Messenger-Client neben
dem formatierten Body auch einen unformatierten Body sendet, welcher von
TI-Messenger-Clients ohne die jeweilige Formatierung genutzt werden kann.

### 5.4 Direct Messaging

TI-Messenger-Clients MÜSSEN eine Funktion anbieten, um Direktnachrichten
gemäß [Direct Messaging] mit anderen Nutzern des TI-Messenger-Dienstes
auszutauschen. Direktnachrichten bedeutet, dass ein Chatraum nur zwischen zwei
Personen erstellt wird. Dieser Chatraum kann nicht um weitere Teilnehmer
erweitert werden. Soll ein Chatraum für mehr als zwei Teilnehmer erstellt
werden, ist Group Messaging zu verwenden . Chaträume, die mit einer
Organisation geführt werden sollen, unterliegen grundsätzlich dem Group
Messaging. Die folgenden Möglichkeiten MÜSSEN dabei vom TI-Messenger-Client
angeboten werden:

<table><tr><td colspan="2" rowspan="1">
Direktnachrichten innerhalb eines Messenger-Services

</td></tr><tr><td>
Userstory

</td><td>
 ---> OL

</td></tr><tr><td colspan="2" rowspan="1">
Direktnachrichten zwischen verschiedenen Messenger-Services

</td></tr><tr><td>
Userstory mittels VZD-FHIR-Directory

</td><td>
 ---> OL

Client zeigt an, dass es sich um einen Direktchat handelt. Eine Umwandlung in
Gruppe ist nicht möglich.

</td></tr><tr><td>
Userstory mittels QR-Scan

</td><td>
 ---> OL

</td></tr></table>

### 5.5 Group Messaging

TI-Messenger-Clients MÜSSEN eine Funktion anbieten, um Gruppenunterhaltungen zu
starten und Nachrichten innerhalb einer Chatgruppe mit unbegrenzt vielen
Nutzern des TI-Messenger-Dienstes auszutauschen. TI-Messenger-Clients MÜSSEN
alle Teilnehmer einer Chatgruppe anzeigen. Darüberhinaus MÜSSEN
TI-Messenger-Clients alle Teilnehmer einer Gruppe benachrichtigen, wenn ein
weiterer Teilnehmer in die Chatgruppe hinzugefügt wurde. Teilnehmer dürfen
nur mittels Einladung in eine Chatgruppe hinzugefügt werden.

<table><tr><td colspan="2" rowspan="1">
Gruppenunterhaltungen innerhalb eines Messenger-Services

</td></tr><tr><td>
Neue Gruppenunterhaltung

</td><td>
 ---> OL

</td></tr><tr><td colspan="2" rowspan="1">
Gruppenunterhaltungen zwischen verschiedenen Messenger-Services

</td></tr><tr><td>
Nachricht an Organisation

</td><td>
 ---> OL

</td></tr><tr><td>
Einladen weiterer Personen

</td><td>
 ---> OL

</td></tr><tr><td>
Einladen weiterer Organisationen

</td><td>
 ---> OL

</td></tr></table>

### 5.6 Push-Benachrichtigungen

Mobile TI-Messenger-Clients MÜSSEN die Matrix-Spezifikation gemäß
[Push-Benachrichtigungen] vollständig implementieren.

### 5.6.1 Allgemein

![Abbildung-4][Abbildung-4]

Die Abbildung "Push-Benachrichtigung für Mobilgeräte" zeigt den Fluss von
Push-Benachrichtigungen, die an ein Mobiltelefon gesendet werden, bei dem die
Push-Benachrichtigungen über den Anbieter des Mobiltelefons übermittelt
werden . Dies geschieht wie folgt:

 ---> OL

### 5.6.2 Push-Anbieter

Ein Push-Anbieter ist ein vom Gerätehersteller verwalteter Dienst, der
Benachrichtigungen direkt an das Gerät senden kann. Ein mobiler
TI-Messenger-Client MUSS den jeweiligen Push-Anbieter des Systems unterstützen.

### 5.6.3 Push-Gateway

Ein Push-Gateway wird vom TI-Messenger-Anbieter zur Verfügung gestellt und ist
ein Server, der Ereignisbenachrichtigungen von Matrix-Homeservern empfängt
und  diese an andere Dienste weiterleitet. Die TI-Messenger-Clients erhalten
organisatorisch ein Routing-Token durch den TI-Messenger-Anbieter und teilen
dem Matrix-Homeserver mit, an welches Push-Gateway die Benachrichtigungen
gesendet werden sollen. Ein mobiler TI-Messenger-Client MUSS organisatorisch
mit dem Push-Gateway des TI-Messenger-Anbieters verknüpft sein. Der
TI-Messenger-Client MUSS sicherstellen, dass das Routing-Token sicher auf dem
Endgerät verwahrt wird.

### 5.6.4 Push-Regel

Eine Push-Regel ist eine einzelne Regel, die festlegt, unter welchen Bedingungen
ein Ereignis an ein Push-Gateway weitergeleitet werden soll und wie die
Benachrichtigung präsentiert werden soll. Diese Regeln werden auf dem
Matrix-Homeserver des Benutzers gespeichert. Der TI-Messenger-Client MUSS
Nutzern die Möglichkeit geben, Push-Regeln für jeden Raum zu erstellen und
anzuzeigen.

### 5.6.5 Push-Regelsatz

Ein Push-Regelsatz deckt einen Satz von Regeln nach bestimmten Kriterien ab.
Beispielsweise können einige Regeln nur für Nachrichten von einem bestimmten
Absender, einem bestimmten Raum oder standardmäßig angewendet werden. Der
Push-Regelsatz enthält den gesamten Satz an Geltungsbereichen und Regeln. Ein
mobiler TI-Messenger-Client MUSS dem Nutzer Möglichkeiten anbieten
Push-Regelsätze zu verwalten.

### 5.6.6 Opt-In

Der Hersteller eines TI-Messenger-Clients MUSS ein Opt-In Verfahren für
Push-Benachrichtigungen durch Nutzer bereitstellen. Das Opt-In Verfahren MUSS
jeweils pro Endgerät bereitgestellt werden.

### 5.7 Weitere Funktionen

Erstellung des Localparts

Der TI-Messenger-Client MUSS bei der Erstellung des Localparts der MXID eines
Nutzers sicherstellen, dass keine personenbezogenen Daten entstehen. Dazu MUSS
der TI-Messenger-Clientden local-Part der verwendeten MXID des Nutzers als
Base32 SHA256 Hash berechnen.

Beispiel einer MXID

@74c1fecc710ce4c8a8bbe310fbc5954c2a5e1e9ef5f70d651da1bfc4c9abe43f:\<domain\>.de

**ML-124045 - Base32 SHA256 Hash**

Der Client MUSS für die MXID einen Hash-Wert mittels Base32 SHA256 zu
berechnen. **[\<=]**

Displayname

Der TI-Messenger-Client MUSS sicherstellen, dass nur Nutzer in der
RolleOrg-Adminden Displaynamen von Nutzern bearbeiten können. Es MUSS
sichergestellt werden, dass Nutzer den eigenen Displaynamen nicht ändern
können. 

Server Administration

Mobile TI-Messenger-Clients MÜSSEN die Matrix-Spezifikation gemäß [Server
Administration] vollständig implementieren.

TI-Messenger-Clients MÜSSEN entsprechende Administrationsfunktionen für einen
Messenger-Service zur Verfügung stellen. Dazu gehören:

 ---> UL

Hinweis: Die Funktionen der Server Administration können in einen separaten
Administrations-Client ausgelagert werden. Sofern reguläre Nutzerfunktionen
und Administrationsfunktionen in derselben Applikation angeboten werden, so
sollte auf eine klar erkennbare Unterscheidung zwischen Nutzer- und
Administrationsfunktionen geachtet werden. Es MUSS sichergestellt werden, dass
nur Akteure in der Rolle Org-Admin die Administrationsfunktionen nutzen
können. 

Third Party Networks / Bridging

Das Bridging zu Drittsystemen zur Zwecken der Kommunikation (Austausch von
Matrix-Events) ist nicht erlaubt. Das Bridging zu Drittsystemen ist nur zum
Archivieren von Chatinhalten erlaubt. Es MUSS sichergestellt werden, dass eine
Ende-zu-Ende Verschlüsselung mittels OLM/MEGOLM zu jeder Zeit erfolgt. 

Nutzerverzeichnis eines Messenger-Services

Der TI-Messenger-Client KANN eine Funktion bereitstellen, dass Nutzer auf dem
jeweiligen Messenger-Service ein Verzeichnis von Nutzern aufrufen oder
durchsuchen können.

Suchabfragen VZD-FHIR-Directory

Der TI-Messenger-Client MUSS eine Funktion bereitstellen, dass Nutzer das
VZD-FHIR-Directory nach Ressourcen durchsuchen können. Der TI-Messenger-Client
MUSS eine Funktion bereitstellen, um Detailinformationen der auf dem
VZD-FHIR-Directory gespeicherten Ressourcen anzuzeigen. Weitere Spezifikationen
finden sich in [gemSpec_VZD_FHIR_Directory].

Verbindung nur mit in der Föderation vorhandenen Messenger-Services

Der TI-Messenger-Client MUSS sicherstellen, dass eine Nutzung nur mit
Matrix-Homeservern möglich ist die Teil der Föderation sind. Verbindet sich
der TI-Messenger-Client mit einem Matrix-Homeserver, welcher nicht Teil der
Föderation ist, MUSS der Nutzer direkt ausgeloggt werden.

Ende-zu-Ende Verschlüsselung

Der TI-Messenger-Client MUSS sicherstellen, dass sämtliche Nachrichteninhalte
Ende-zu-Ende [Ende-zu-Ende Verschlüsselung] verschlüsselt werden. Das Senden
von Nachrichten ohne Ende-zu-Ende Verschlüsselung MUSS technisch unterbunden
werden.

Archivierung von Gesprächsinhalten mittels Chatbot-Clients

<table><tr><td>
Zur Archivierung von Gesprächsinhalten ist eine Lösung auf Basis
automatisierter Matrix-Clients in der Leistungserbringerumgebung geplant. Die
hier vorhandene Beschreibung ist für die Erstveröffentlichung der
Spezifikation noch als informell zu betrachten und wird im ersten geplanten
Hotfix konkretisiert und formalisiert.

</td></tr></table>

Für eine echtzeitnahe und automatische Archivierung von Gesprächsinhalten zu
Nachweiszwecken werden vom Anbieter des TI-Messenger-Homeservers sog.
Archivbots bereitgestellt, bei welchen es sich um funktional eingeschränkte
Matrix-Clients handelt. Diese können entweder von Leistungserbringern zu
Gesprächen eingeladen werden oder sind für bestimmte Gesprächsraumtypen
automatisch bei der Raumerstellung eingeladen (konfigurierbar durch
LE-Organisation).

Der einzige Zweck des Archivbots besteht darin, eine Unterhaltung oder Teile
dieser zu entschlüsseln und zu archivieren. Hierzu betritt der Archivbot den
Gesprächsraum, in den er eingeladen wurde und kann somit darin versandte
Nachrichten entschlüsseln und als FHIR-Ressource archivieren. Der Archivbot
liegt in der Leistungserbringerumgebung und kommuniziert zum Ablegen
archivierter Nachrichten mittels TLS mit einem Endpunkt, z.B. des PVS/KIS oder
einem LE-Archivierungs-Backend.

Der Archivbot ist als Gesprächsteilnehmer für alle anderen Teilnehmer sichtbar
und klar als rein funktionaler Archivbot benannt. Es wird empfohlen, dass der
Archivbot bei Betreten eines Gesprächsraums ein kurzes Statement zu seiner
Funktion abgibt, um Missverständnisse zu vermeiden.

Es ist vorgesehen, dass auch Gespräche ohne Archivbot geführt werden können,
welche dementsprechend nicht archiviert werden. Bei Archivbots handelt es sich
nicht um vollwertige TI-Messenger-Clients, weswegen sie bezüglich der
Client-Anforderungen gesondert betrachtet werden müssen.

### 6 Anhang A – Verzeichnisse

### 6.1 Abkürzungen

<table><tr><th>
Kürzel

</th><th>
Erläuterung

</th></tr><tr><td>
CC

</td><td>
Common Criteria

</td></tr><tr><td>
FHIR

</td><td>
Fast Healthcare Interoperable Resources

</td></tr><tr><td>
IDP

</td><td>
Identity Provider

</td></tr><tr><td>
JSON

</td><td>
JavaScript Object Notation

</td></tr><tr><td>
MXID

</td><td>
Matrix-ID

</td></tr><tr><td>
OAuth

</td><td>
Open Authorization

</td></tr><tr><td>
PASSporT

</td><td>
Personal Assertion Token

</td></tr><tr><td>
SMC-B

</td><td>
Institutionenkarte (Security Module Card Typ B)

</td></tr><tr><td>
SSO

</td><td>
Single Sign-on

</td></tr><tr><td>
SSSS

</td><td>
Secure Secret Storage and Sharing

</td></tr><tr><td>
TI

</td><td>
Telematikinfrastruktur

</td></tr><tr><td>
TLS

</td><td>
Transport Layer Security

</td></tr><tr><td>
VZD

</td><td>
Verzeichnisdienst

</td></tr></table>

### 6.2 Glossar

<table><tr><th>
Begriff

</th><th>
Erläuterung

</th></tr><tr><td>
</td></tr><tr><td>
MXID

</td><td>
Eindeutige Identifikation eines TI-Messenger-Nutzers

</td></tr></table>

Das Glossar wird als eigenständiges Dokument (vgl. [gemGlossar]) zur Verfügung
gestellt.

### 6.3 Abbildungsverzeichnis

- [Abbildung-2] - Benachbarte Komponenten des TI-Messenger-Clients
- [Abbildung-3] - Testtreiberschnittstelle
- [Abbildung-4] - Push-Benachrichtigung für Mobilgeräte

### 6.4 Tabellenverzeichnis

- [Tabelle-1] - Übersicht der Komponenten und deren Funktionen
- [Tabelle-2] - Events und Msgtypes

### 6.5 Referenzierte Dokumente

### 6.5.1 Dokumente der gematik

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
[gemSpec_TI-Messenger-Dienst]

</td><td>
gematik: Spezifikation TI-Messenger-Dienst

</td></tr><tr><td>
[gemSpec_TI-Messenger-FD]

</td><td>
gematik: Spezifikation TI-Messenger-Fachdienst

</td></tr><tr><td>
[gemSpec_Krypt]

</td><td>
gematik: Übergreifende Spezifikation - Verwendung kryptographischer Algorithmen
in der Telematikinfrastruktur

</td></tr><tr><td>
[gemSpec_VZD_FHIR_Directory]

</td><td>
gematik: Spezifikation Verzeichnisdienst FHIR-Directory

</td></tr><tr><td>
[gemKPT_Betr]

</td><td>
gematik: Betriebskonzept Online-Produktivbetrieb

</td></tr></table>

### 6.5.2 Weitere Dokumente

<table><tr><th>
[Quelle]

</th><th>
Herausgeber (Erscheinungsdatum): Titel

</th></tr><tr><td>
[Matrix Foundation]

</td><td>
Matrix Foundation 

https://matrix.org/docs/spec/

 

</td></tr><tr><td>
[Instant Messaging]

</td><td>
Matrix Foundation

https://matrix.org/docs/spec/client_server/r0.6.1#id42

 

</td></tr><tr><td>
[Direct Messaging]

</td><td>
Matrix Foundation

https://matrix.org/docs/spec/client_server/r0.6.1#id140

 

</td></tr><tr><td>
[Erwähnung]

</td><td>
Matrix Foundation

https://matrix.org/docs/spec/client_server/r0.6.1#user-room-and-group-mentions

 

</td></tr><tr><td>
[Präsenzanzeige]

</td><td>
Matrix Foundation

https://matrix.org/docs/spec/client_server/r0.6.1#id62

 

</td></tr><tr><td>
[Push Benachrichtigungen]

</td><td>
Matrix Foundation

https://matrix.org/docs/spec/client_server/r0.6.1#id89

 

</td></tr><tr><td>
[Push-Rules]

</td><td>
Matrix Fundation

https://matrix.org/docs/spec/client_server/r0.6.1#id89

 

</td></tr><tr><td>
[Lesebestätigungen]

</td><td>
Matrix Foundation

https://matrix.org/docs/spec/client_server/r0.6.1#id53

 

</td></tr><tr><td>
[Eingabebenachrichtigungen]

</td><td>
Matrix Foundation

https://matrix.org/docs/spec/client_server/r0.6.1#id49

 

</td></tr><tr><td>
[Nutzer ignorieren]

</td><td>
Matrix Foundation

https://matrix.org/docs/spec/client_server/r0.6.1#id144

 

</td></tr><tr><td>
[Raum Historie]

</td><td>
Matrix Foundation

https://matrix.org/docs/spec/client_server/r0.6.1#room-history-visibility

 

</td></tr><tr><td>
[Room Upgrades]

</td><td>
Matrix Foundation

https://matrix.org/docs/spec/client_server/r0.6.1#id160

 

</td></tr><tr><td>
[Server Administration]

</td><td>
Matrix Foundation

https://matrix.org/docs/spec/client_server/r0.6.1#id129

 

</td></tr><tr><td>
[Send-to-Device messaging]

</td><td>
Matrix Foundation

https://matrix.org/docs/spec/client_server/r0.6.1#id70

 

</td></tr><tr><td>
[Geräteverwaltung]

</td><td>
Matrix Foundation

https://matrix.org/docs/spec/client_server/r0.6.1#id73

 

</td></tr><tr><td>
[Reporting-content]

</td><td>
Matrix-Foundation

https://matrix.org/docs/spec/client_server/r0.6.1#id150

 

</td></tr><tr><td>
[Ende-zu-Ende Verschlüsselung]

</td><td>
Matrix Foundation

https://matrix.org/docs/spec/client_server/r0.6.1#id76

 

</td></tr><tr><td>
[SSO Login]

</td><td>
Matrix Foundation

https://matrix.org/docs/spec/client_server/r0.6.1#sso-client-login

 

</td></tr><tr><td>
[OpenID]

</td><td>
Matrix Foundation

https://matrix.org/docs/spec/client_server/r0.6.1#id154

 

</td></tr><tr><td>
[OWASPMobileTop10]

</td><td>
OWASP Mobile Top 10

https://owasp.org/www-project-mobile-top-10/

 

</td></tr><tr><td>
[OWASP Proactive Control] 

</td><td>
OWASP Proactive Controls

https://owasp.org/www-project-proactive-controls/

 

</td></tr><tr><td>
[ISO 9241]

</td><td>
Ergonomics of human-system interaction

https://www.iso.org

</td></tr><tr><td>
[BITV 2.0]

</td><td>
Verordnung zur Schaffung barrierefreier Informationstechnik nach dem
Behindertengleichstellungsgesetz (Barrierefreie-Informationstechnik-Verordnung
- BITV 2.0)

https://www.gesetze-im-internet.de/bitv_2_0/BJNR184300011.html

 

</td></tr><tr><td>
[BSI-TR-03166]

</td><td>
BSI TR-03166 - Technical Guideline for Biometric Authentication Components in
Devices for Authentication 

https://www.bsi.bund.de/SharedDocs/Downloads/EN/BSI/Publications/TechGuidelines/TR03166/BSI-TR-03166.pdf

 

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
[3.1]:                   #31-nachbarsysteme
[3.2]:                   #32-ti-messenger-clients-für-unterschiedliche-nutzergruppen
[3.3]:                   #33-ti-messenger-clients-für-unterschiedliche-plattformen
[4]:                     #4-übergreifende-festlegungen
[4.1]:                   #41-datenschutz-und-sicherheit
[4.2]:                   #42-benutzerführung
[4.3]:                   #43-konfiguration-des-ti-messenger-clients
[4.4]:                   #44-test
[4.5]:                   #45-betriebliche-aspekte
[5]:                     #5-funktionsmerkmale
[5.1]:                   #51-authentisierung
[5.2]:                   #52-matrix-client-server-api
[5.3]:                   #53-instant-messaging
[5.4]:                   #54-direct-messaging
[5.5]:                   #55-group-messaging
[5.6]:                   #56-push-benachrichtigungen
[5.6.1]:                 #561-allgemein
[5.6.2]:                 #562-push-anbieter
[5.6.3]:                 #563-push-gateway
[5.6.4]:                 #564-push-regel
[5.6.5]:                 #565-push-regelsatz
[5.6.6]:                 #566-opt-in
[5.7]:                   #57-weitere-funktionen
[6]:                     #6-anhang-a-–-verzeichnisse
[6.1]:                   #61-abkürzungen
[6.2]:                   #62-glossar
[6.3]:                   #63-abbildungsverzeichnis
[6.4]:                   #64-tabellenverzeichnis
[6.5]:                   #65-referenzierte-dokumente
[6.5.1]:                 #651-dokumente-der-gematik
[6.5.2]:                 #652-weitere-dokumente
[Img-001]:               gemSpec_TI-Messenger-Client_V1.0.0.attachments/14647692903745499075.png
[Abbildung-2]:           gemSpec_TI-Messenger-Client_V1.0.0.attachments/1083322672245794402.jpg
[Abbildung-3]:           gemSpec_TI-Messenger-Client_V1.0.0.attachments/15715377702803687840.png
[Abbildung-4]:           gemSpec_TI-Messenger-Client_V1.0.0.attachments/3277742052805261512.jpg
[Tbl-001]:               #Tbl-001 (&93834801498976)
[Tbl-002]:               #Tbl-002 (&93834764162504)
[Tabelle-1]:             #Tabelle-1 (&93834799909264)
[Tabelle-2]:             #Tabelle-2 (&93834781681640)
[Tbl-005]:               #Tbl-005 (&93834781710976)
[Tbl-006]:               #Tbl-006 (&93834775085136)
[Tbl-007]:               #Tbl-007 (&93834804528328)
[Tbl-008]:               #Tbl-008 (&93834804537448)
[Tbl-009]:               #Tbl-009 (&93834804563256)
[Tbl-010]:               #Tbl-010 (&93834767978464)
[Tbl-011]:               #Tbl-011 (&93834767993568)
[https://spec.matrix.org/unstable/client-server-api/#device-verification]: https://spec.matrix.org/unstable/client-server-api/#device-verification (&93834810786624)
[https://spec.matrix.org/unstable/client-server-api/#sharing-keys-between-devices]: https://spec.matrix.org/unstable/client-server-api/#sharing-keys-between-devices (&93834810787576)
[https://spec.matrix.org/unstable/client-server-api/#end-to-end-encryption]: https://spec.matrix.org/unstable/client-server-api/#end-to-end-encryption (&93834810791248)
[https://spec.matrix.org/unstable/client-server-api/#secrets]: https://spec.matrix.org/unstable/client-server-api/#secrets (&93834810792200)
[https://spec.matrix.org/unstable/client-server-api/#fallbacks-for-rich-replies]: https://spec.matrix.org/unstable/client-server-api/#fallbacks-for-rich-replies (&93834781703296)
[https://matrix.org/docs/spec/]: https://matrix.org/docs/spec/ (&93834767998384)
[https://matrix.org/docs/spec/client_server/r0.6.1#id42]: https://matrix.org/docs/spec/client_server/r0.6.1#id42 (&93834768001264)
[https://matrix.org/docs/spec/client_server/r0.6.1#id140]: https://matrix.org/docs/spec/client_server/r0.6.1#id140 (&93834768004144)
[https://matrix.org/docs/spec/client_server/r0.6.1#user-room-and-group-mentions]: https://matrix.org/docs/spec/client_server/r0.6.1#user-room-and-group-mentions (&93834768007024)
[https://matrix.org/docs/spec/client_server/r0.6.1#id62]: https://matrix.org/docs/spec/client_server/r0.6.1#id62 (&93834768010088)
[https://matrix.org/docs/spec/client_server/r0.6.1#id89]: https://matrix.org/docs/spec/client_server/r0.6.1#id89 (&93834768013344)
[https://matrix.org/docs/spec/client_server/r0.6.1#id89]: https://matrix.org/docs/spec/client_server/r0.6.1#id89 (&93834768016408)
[https://matrix.org/docs/spec/client_server/r0.6.1#id53]: https://matrix.org/docs/spec/client_server/r0.6.1#id53 (&93834768019288)
[https://matrix.org/docs/spec/client_server/r0.6.1#id49]: https://matrix.org/docs/spec/client_server/r0.6.1#id49 (&93834768022168)
[https://matrix.org/docs/spec/client_server/r0.6.1#id144]: https://matrix.org/docs/spec/client_server/r0.6.1#id144 (&93834768025048)
[https://matrix.org/docs/spec/client_server/r0.6.1#room-history-visibility]: https://matrix.org/docs/spec/client_server/r0.6.1#room-history-visibility (&93834768027928)
[https://matrix.org/docs/spec/client_server/r0.6.1#id160]: https://matrix.org/docs/spec/client_server/r0.6.1#id160 (&93834768030808)
[https://matrix.org/docs/spec/client_server/r0.6.1#id129]: https://matrix.org/docs/spec/client_server/r0.6.1#id129 (&93834768033688)
[https://matrix.org/docs/spec/client_server/r0.6.1#id70]: https://matrix.org/docs/spec/client_server/r0.6.1#id70 (&93834768036568)
[https://matrix.org/docs/spec/client_server/r0.6.1#id73]: https://matrix.org/docs/spec/client_server/r0.6.1#id73 (&93834768039448)
[https://matrix.org/docs/spec/client_server/r0.6.1#id150]: https://matrix.org/docs/spec/client_server/r0.6.1#id150 (&93834768042328)
[https://matrix.org/docs/spec/client_server/r0.6.1#id76]: https://matrix.org/docs/spec/client_server/r0.6.1#id76 (&93834799199120)
[https://matrix.org/docs/spec/client_server/r0.6.1#sso-client-login]: https://matrix.org/docs/spec/client_server/r0.6.1#sso-client-login (&93834799202000)
[https://matrix.org/docs/spec/client_server/r0.6.1#id154]: https://matrix.org/docs/spec/client_server/r0.6.1#id154 (&93834799204880)
[https://owasp.org/www-project-mobile-top-10/]: https://owasp.org/www-project-mobile-top-10/ (&93834799207760)
[https://owasp.org/www-project-proactive-controls/]: https://owasp.org/www-project-proactive-controls/ (&93834799210640)
[https://www.iso.org]:   https://www.iso.org (&93834799213520)
[https://www.gesetze-im-internet.de/bitv_2_0/BJNR184300011.html]: https://www.gesetze-im-internet.de/bitv_2_0/BJNR184300011.html (&93834799216280)
[https://www.bsi.bund.de/SharedDocs/Downloads/EN/BSI/Publications/TechGuidelines/TR03166/BSI-TR-03166.pdf]: https://www.bsi.bund.de/SharedDocs/Downloads/EN/BSI/Publications/TechGuidelines/TR03166/BSI-TR-03166.pdf (&93834799219160)
