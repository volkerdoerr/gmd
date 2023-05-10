
Elektronische Gesundheitskarte und Telematikinfrastruktur

### Spezifikation<br>KOM-LE-Clientmodul<br>Abbildung 4: Administrationsmodul für die Kommunikation mit dem Account Manager

- Klassifizierung: öffentlich
- Referenzierung: gemSpec_CM_KOMLE
- Revision: 548770
- Stand: 31.01.2022
- Status: freigegeben
- Version: 1.13.0

### Dokumentinformationen

<table><tr><td>
Seit März 2020 verwendet die gematik die Bezeichnung „KIM – Kommunikation
im Medizinwesen“ für die Anwendung KOM-LE. Diese neue Benennung findet sich
insbesondere in Informationsmaterialien für die Zielgruppe Leistungserbringer
sowie in Presseveröffentlichungen. Eine Umbenennung in den
technisch-normativen Dokumenten wie Spezifikationen, Konzepten,
Zulassungsdokumenten etc. mit Ausnahme von Angaben zu Domänen,
E-Mail-Adressen, technischen Schnittstellen, Parametern u.ä. ist mit Stand
Release 4.0.0 nicht geplant.

</td></tr></table>

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
0.5.0

</td><td>
19.11.13

</td><td>
</td><td>
zur Abstimmung freigegeben

</td><td>
gematik

</td></tr><tr><td>
1.0.0

</td><td>
27.01.14

</td><td>
</td><td>
Einarbeitung Kommentare

</td><td>
gematik

</td></tr><tr><td>
1.1.0

</td><td>
28.02.14

</td><td>
4.1.2

</td><td>
XP-Verweis entfernt

</td><td>
gematik

</td></tr><tr><td>
1.2.0

</td><td>
25.07.14

</td><td>
3.1  
4.1.2/4.1.4

</td><td>
Zeitsynchronisation Konnektor ergänzt Formulierungsanpassungen

</td><td>
gematik

</td></tr><tr><td>
1.3.0

</td><td>
24.07.15

</td><td>
</td><td>
Begriff Betreiber durch Anbieter ersetzt

</td><td>
gematik

</td></tr><tr><td>
1.4.0

</td><td>
16.10.16

</td><td>
Anpassungen gemäß Änderungsliste

</td><td>
gematik

</td></tr><tr><td>
1.5.0

</td><td>
14.05.18

</td><td>
</td><td>
Einarbeitung P15.4

</td><td>
gematik

</td></tr><tr><td>
1.6.0

</td><td>
15.05.2019

</td><td>
</td><td>
Einarbeitung P18.1

</td><td>
gematik

</td></tr><tr><td>
1.7.0

</td><td>
02.03.20

</td><td>
Einarbeitung P21.1

</td><td>
gematik

</td></tr><tr><td>
1.8.0 

</td><td>
30.06.20

</td><td>
</td><td>
Anpassungen gemäß Änderungsliste P22.1 und Scope-Themen aus Systemdesign
R4.0.0

</td><td>
gematik

</td></tr><tr><td>
1.9.0 

</td><td>
12.11.20

</td><td>
Anpassungen gemäß Änderungsliste P22.2 und Scope-Themen aus Systemdesign
R4.0.1

</td><td>
gematik

</td></tr><tr><td>
1.9.1

</td><td>
18.12.20

</td><td>
Anpassungen gemäß Änderungsliste P22.4

</td><td>
gematik

</td></tr><tr><td>
1.10.0

</td><td>
19.02.21

</td><td>
Anpassungen gemäß Änderungsliste P22.5 

</td><td>
gematik

</td></tr><tr><td>
1.11.0

</td><td>
06.04.21

</td><td>
Anpassungen gemäß Änderungsliste KIM_Maintenance_21.1/  
KIM 1.5.1

</td><td>
gematik

</td></tr><tr><td>
1.11.1

</td><td>
20.04.21

</td><td>
Anpassung C_10247 aus KIM_Maintenance_21.1 vervollständigt (A_21247 entfernt)

</td><td>
gematik

</td></tr><tr><td>
1.12.0

</td><td>
04.08.21

</td><td>
Einarbeitung gemäß KIM Maintenance 21.2 /KIM 1.5.1-3

</td><td>
gematik

</td></tr><tr><td>
1.13.0

</td><td>
31.01.22

</td><td>
Einarbeitung gemäß KIM Maintenance 21.3 /KIM 1.5.2

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
  - [1.4] Arbeitsgrundlagen
  - [1.5] Abgrenzung des Dokuments
  - [1.6] Methodik
    - [1.6.1] Anforderungen
    - [1.6.2] Diagramme
    - [1.6.3] Nomenklatur
- [2] Systemüberblick
- [3] Produktfunktionen
  - [3.1] Allgemeine Anforderungen
  - [3.2] Umgang mit großen Anhängen
    - [3.2.1] Senden von Nachrichten mit großen Anhängen
    - [3.2.2] Empfangen von Nachrichten mit großen Anhängen
  - [3.3] Senden von Nachrichten
    - [3.3.1] Übersicht
    - [3.3.2] CONNECT-Zustand
      - [3.3.2.1] Initialisierung
      - [3.3.2.2] Verbindungsaufbau mit MTA
    - [3.3.3] PROXY-Zustand
    - [3.3.4] PROCESS-Zustand
      - [3.3.4.1] Empfang und Weiterleitung einer Nachricht
        - [3.3.4.1.1] Bearbeitung einer ungeschützten Nachricht
        - [3.3.4.1.2] Bearbeitung einer geschützten KOM-LE-Nachricht
    - [3.3.5] Beispiele
  - [3.4] Empfangen von Nachrichten
    - [3.4.1] Übersicht
    - [3.4.2] CONNECT-Zustand
      - [3.4.2.1] Initialisierung
      - [3.4.2.2] Verbindungsaufbau mit dem POP3-Server
    - [3.4.3] PROXY-Zustand
    - [3.4.4] PROCESS-Zustand
      - [3.4.4.1] Empfang und Weiterleitung einer Nachricht
      - [3.4.4.2] Aufbereitung einer Nachricht
        - [3.4.4.2.1] Entschlüsselung
        - [3.4.4.2.2] Integritätsprüfung
    - [3.4.5] Beispiele
  - [3.5] Übermittlung von Kontaktdaten
  - [3.6] Übermittlung von E-Mail-Kategorien
  - [3.7] Administrationsmodul
    - [3.7.1] Allgemeine Anforderungen
    - [3.7.2] Registrierung KOM-LE-Teilnehmer
    - [3.7.3] Deregistrierung KOM-LE-Teilnehmer
    - [3.7.4] Download PKCS#12 KOM-LE-Teilnehmer
  - [3.8] Kryptographischen Schnittstellen des Konnektors
    - [3.8.1] Erstellung der digitalen Signatur einer Nachricht mit einer SM-B
    - [3.8.2] Prüfung der digitalen Signatur einer Nachricht
    - [3.8.3] Verschlüsselung einer Nachricht
    - [3.8.4] Entschlüsselung einer Nachricht mit einer SM-B bzw. einem HBA
- [4] Nichtfunktionale Anforderungen
  - [4.1] Transportsicherung
    - [4.1.1] Allgemeine Festlegungen
    - [4.1.2] Transportsicherung zwischen Clientsystem und Clientmodul
    - [4.1.3] Transportsicherung zwischen Clientmodul und Konnektor
    - [4.1.4] Transportsicherung zwischen Clientmodul und Fachdienst
  - [4.2] Nutzung von Webservice-Schnittstellen des Konnektors
  - [4.3] Protokollierung/Logging
    - [4.3.1] Ablaufprotokoll
    - [4.3.2] Performance
    - [4.3.3] Fehler
  - [4.4] Konfiguration
  - [4.5] Update-Mechanismen
  - [4.6] Produktleistungen
    - [4.6.1] Performance
    - [4.6.2] Skalierbarkeit
- [5] Anhang A – Verzeichnisse
  - [5.1] Abkürzungen
  - [5.2] Glossar
  - [5.3] Abbildungsverzeichnis
  - [5.4] Tabellenverzeichnis
  - [5.5] Referenzierte Dokumente
    - [5.5.1] Dokumente der gematik
    - [5.5.2] Weitere Dokumente

### 1 Einordnung des Dokumentes

### 1.1 Zielsetzung

Das vorliegende Dokument spezifiziert die Anforderungen an den Produkttyp
KOM-LE-Clientmodul. Das Clientmodul ist verantwortlich für das Signieren und
Verschlüsseln von KOM-LE-Nachrichten beim Versenden sowie für die
Entschlüsselung und Signaturprüfung beim Abholen von KOM-LE-Nachrichten.

Aus den Kommunikationsbeziehungen mit Clientsystem, Konnektor, Verzeichnisdienst
und KOM-LE-Fachdienst resultieren vom Clientmodul anzubietende Schnittstellen,
die in diesem Dokument normativ beschrieben werden. Vom Clientmodul genutzte
Schnittstellen liegen zumeist in anderen Verantwortungsbereichen (Konnektor,
Verzeichnisdienst). Diese werden in den entsprechenden
Produkttypspezifikationen definiert.

### 1.2 Zielgruppe

Dieses Dokument richtet sich an

 ---> UL

### 1.3 Geltungsbereich

Dieses Dokument enthält normative Festlegungen zur Telematikinfrastruktur des
deutschen Gesundheitswesens. Der Gültigkeitszeitraum der vorliegenden Version
und deren Anwendung in Zulassungsverfahren werden durch die gematik GmbH in
gesonderten Dokumenten (z.B. Dokumentenlandkarte, Produkttypsteckbrief,
Leistungsbeschreibung) festgelegt und bekannt gegeben.

### 1.4 Arbeitsgrundlagen

Grundlagen für die Ausführungen dieses Dokumentes sind

 ---> UL

### 1.5 Abgrenzung des Dokuments

Spezifiziert werden in dem Dokument die vom Produkttyp bereitgestellten
(angebotenen) Schnittstellen. Benutzte Schnittstellen werden hingegen in der
Spezifikation desjenigen Produkttypen beschrieben, der diese Schnittstelle
bereitstellt. Auf die entsprechenden Dokumente wird referenziert.

Die Systemlösung der Fachanwendung KOM-LE ist im systemspezifischen Konzept
[gemSysL_KOMLE] beschrieben. Dieses Konzept setzt die fachlichen Anforderungen
des Lastenheftes auf Systemebene um, zerlegt die Fachanwendung KOM-LE in die
zugehörigen Produkttypen, darunter das KOM-LE-Clientmodul und der
KOM-LE-Fachdienst. Ferner definiert es die Schnittstellen zwischen den
einzelnen Produkttypen. Für das Verständnis dieser Spezifikation wird die
Kenntnis von [gemSysL_KOMLE] vorausgesetzt.

Die Anforderungen am Fachdienst werden separat in der Spezifikationen Fachdienst
KOM-LE [gemSpec_FD_KOMLE] beschrieben.

Die Anforderungen an das Format der KOM-LE-Nachrichten, die zwischen dem
Clientmodul und dem Fachdienst übermittelt werden, werden separat im
KOM-LE-S/MIME-Profil [gemSMIME_KOMLE] beschrieben.

Abbildung 1 zeigt schematisch die Einbettung des vorliegenden Dokuments in die
Dokumentenlandschaft der Lastenheft- und Pflichtenheftphase in Form einer
Dokumentenhierarchie.

![Abbildung-1][Abbildung-1]

### 1.6 Methodik

### 1.6.1 Anforderungen

Anforderungen als Ausdruck normativer Festlegungen werden durch eine eindeutige
ID sowie die dem RFC 2119 [RFC2119] entsprechenden, in Großbuchstaben
geschriebenen deutschen Schlüsselworte MUSS, DARF NICHT, SOLL, SOLL NICHT,
KANN gekennzeichnet.

Sie werden im Dokument wie folgt dargestellt:

\<AFO-ID\> - \<Titel der Afo\>Text / Beschreibung[ \<=]

Dabei umfasst die Anforderung sämtliche innerhalb der Afo-ID und der Textmarke
angeführten Inhalte.

### 1.6.2 Diagramme

Die Darstellung der Spezifikationen von Komponenten erfolgt auf der Grundlage
einer durchgängigen Use-Case-Modellierung als

 ---> UL

### 1.6.3 Nomenklatur

Sofern im Text dieser Spezifikation auf die Ausgangsanforderungen verwiesen
wird, erfolgt dies in eckigen Klammern, z.B. [KOMLE-A_2015]. Wird auf
Eingangsanforderungen verwiesen, erfolgt dies in runden Klammern, z.B.
(KOMLE-A_202).

### 2 Systemüberblick

Das Clientmodul bietet die Funktionalität, die für Anwendungsfälle
KOM-LE_AF_1 „Nachricht senden“ und KOM-LE_AF_2 „Nachricht empfangen“
(siehe [gemSysL_KOMLE]) relevant ist. Die Aufgabe des Clientmoduls ist das
Aufbringen und Aufheben des Schutzes der Integrität und Vertraulichkeit der
zwischen den KOM-LE-Teilnehmern ausgetauschten E-Mail-Nachrichten. Dabei
kommuniziert das Clientmodul mit dem Clientsystem, dem KOM-LE-Fachdienst und
nutzt mehrere Dienste der TI-Plattform. Optional kann das Clientmodul in das
Clientsystem integriert werden. Abbildung 2 stellt die grundlegenden Elemente
der KOM-LE-Architektur dar.

![Abbildung-2][Abbildung-2]

Die im Clientmodul bearbeitende E-Mail-Nachrichten von kleiner oder gleich 25 MB
werden beim Senden entsprechend dem KOM-LE-S/MIME-Profil [gemSMIME_KOMLE]
digital signiert und verschlüsselt und beim Empfangen entschlüsselt und deren
Signatur geprüft. Bei E-Mail-Nachrichten größer als 25 MB wird der Anhang
aus der E-Mail extrahiert und auf einemseparaten Speicherort (Fachdienst)
verschlüsselt abgelegt. Das KOM-LE-S/MIME-Profil konkretisiert die
S/MIME-Spezifikation und stellt sicher, dass die Interoperabilität zwischen
den verschiedenen KOM-LE-Komponenten sowie der Schutz von Integrität und
Vertraulichkeit für alle personenbezogenen medizinischen Daten gewährleistet
werden.

Jede dem KOM-LE-S/MIME-Profil entsprechende Nachricht hat die in Abbildung 3
dargestellte Struktur. Die äußere Nachricht ist eine entsprechend dem
S/MIME-Standard signierte und verschlüsselte E-Mail-Nachricht. Die innere
Nachricht ist eine im Clientsystem erzeugte E-Mail-Nachricht, die Nutzdaten
enthält und alsmessage/rfc822Anhang in die äußere Nachricht verpackt ist.

![Abbildung-3][Abbildung-3]

Die durch das Clientmodul versendeten Nachrichten können vom Client optional
gekennzeichnet werden. Es wird empfohlen eine Dienstkennung zu setzen.
Andernfalls werden Nachrichten mit einer standardisierten Dienstkennung
versehen. Das hierfür notwendiges Attribut im Header der
Mail(X-KIM-Dienstkennung)wird im Kapitel 3.6 beschrieben. Erfolgte durch den
Client keine Belegung dieses Attributes, wird durch das Clientmodul eine
Default-Kennung gesetzt. Um die Abholung der auf dem Mail-Server ankommenden
Nachrichten inhaltsabhängig durchführen zu können, wird das Header-Feld
"X-KIM-Dienstkennung" aus der inneren Nachricht, die signiert und
verschlüsselt ist, in den äußeren Header der Nachricht übernommen.

Zusätzlich wird das Clientmodul um das Administrationsmodul erweitert (siehe
auch Kap. 3.7). Mit Hilfe des Administrationsmoduls kann sich der
KOM-LE-Teilnehmer beim Fachdienst registrieren oder eine Deregistrierung
vornehmen. Zugleich kann über das Administrationsmodul das benötigte
Clientzertifikat (PKCS#12 - Datei) heruntergeladen werden.

![Abbildung-4][Abbildung-4]

Der Funktionsumfang des Clientmodules kann optional in das Clientsystem
integriert werden. Somit ist kein separates Clientmodul mehr notwendig.

Wenn das Clientmodul in das Clientsystem (PVS) integriert wird, richten sich die
Anforderungen des Clientmodul an das Clientsystem (PVS). Durch die optionale
Integration entfallen alle Anforderungen an die Schnittstelle zwischen
Clientsystem und Clientmodul, da diese nicht mehr existiert.

In diesem Szenario gilt für Anforderungen, die nur Anteile auf die
Schnittstelle zwischen Clientsystem und dem Clientmodul enthalten (z.B. "vom
Clientsystem erhaltene E-Mail-Nachrichten"), dass diese Anteile entfallen und
die restliche Anforderung umgesetzt werden muss. Abzüglich der Tests der
weggefallenen Schnittstelle ändert sich also das Zulassungsverfahren nicht.

### 3 Produktfunktionen

### 3.1 Allgemeine Anforderungen

**KOM-LE-A_2003 - Unterstützung von E-Mail-Clients**

Das KOM-LE-Clientmodul MUSS das Senden und Empfangen von Nachrichten
mitmarktüblichen SMTP/POP3 Desktop-E-Mail-Clients unterstützen. **[\<=]**

**KOM-LE-A_2004 - Größe einer E-Mail-Nachricht bis zu 25 MB**

Das KOM-LE-Clientmodul MUSS Nachrichten mit einer Nettogröße von bis zu 25 MB
bearbeiten können. Dabei ist zu beachten, dass sich durch die base64-Kodierung
der Nachricht die zu verarbeitende Bruttogröße um den Faktor 1,37 erhöht.
**[\<=]**

**A_19366-02 - Größe einer E-Mail-Nachricht größer 25 MB**

Das KOM-LE-Clientmodul MUSS Nachrichten (ohne oder nach dem entfernen aller
Anhänge), die eine Nettogröße von bis zu 25 MB haben, verarbeiten
können.Ist der E-Mail-Body (ohne Anhänge) größer als 25 MB (netto), dann
MUSS das KOM-LE-Clientmodul an den Mail-Client den Fehlercode X.3.4  (Message
too big for system) gemäß [RFC3463] zurückgeben. **[\<=]**

Durch die Limitierung des Konnektors sind E-Mail-Nachrichten bis zu einer
Größe von 25 MB möglich.Wenn der Empfänger einen KOM-LE-Client ab Version
1.5 nutzt, können mit der in Kap. 3.2 beschriebenen Vorgehensweise auch große
Mails mit  Anhängen von über 25 MB versendet werden. Die Nachricht darf,
nach Extraktion der Anhänge, weiterhin die Größe von 25 MB nicht
übersteigen und muss durch das KOM-LE-Clientmodul und den KOM-LE-Fachdienst
verarbeitet werden.

**A_19513 - Bereitstellung Zertifikate aus PKCS#12-Datei**

Das KOM-LE-Clientmodul MUSS die Zertifikate aus der PKCS#12-Datei entpacken und
zur Verfügung stellen. **[\<=]**

Die PKCS#12-Datei wird für die Registrierung eines KOM-LE-Teilnehmers sowie bei
Ablauf des Clientzertifikates benötigt.

**KOM-LE-A_2005 - Keine persistente Speicherung von Nachrichten**

DasKOM-LE-Clientmodul DARF NICHT die Inhalte von Nachrichten länger als es für
die Aufbereitung und Übermittlungnötig ist, speichern. **[\<=]**

**KOM-LE-A_2230 - Synchronisation mit der Systemzeit des Konnektors**

Das KOM-LE-Clientmodul MUSS sich unter Verwendung der Operation sync_Time mit
der Systemzeit des Konnektors synchronisieren. **[\<=]**

**KOM-LE-A_2006 - Einzuhaltende Standards beim Senden und Empfangen**

Das KOM-LE-Clientmodul MUSS sich beim Senden und Empfangen von Nachrichten
konform zu folgenden Standards verhalten:

 ---> UL

**[\<=]**

Diese Spezifikation erläutert nicht alle Schritte und Einzelheiten der SMTP-
und POP3-Kommunikation zwischen dem Clientsystem, dem KOM-LE-Clientmodul und
dem KOM-LE-Fachdienst. Es setzt voraus, dass das Format einer E-Mail, MIME,
SMTP und POP3 dem Leser bekannt sind.

**A_20189-02 - Übermittlung der benötigten KOM-LE Version des Clientmoduls**

Der Anbieter des KOM-LE-Fachdienstes MUSS seinem KOM-LE Teilnehmer bei der
Erstellung des Accounts sowie bei einem  relevanten Update des Fachdienstes,
die nötige KOM-LE-Version des Clientmoduls mitteilen. **[\<=]**

Die KOM-LE-Version des Clientmodules muss mitgeteilt werden, damit der Nutzer
weiß, welche Clientmodul-Version zu verwenden ist. Bei Nutzung eines
Clientmodules in der KOM-LE-Version 1.0 ist eine Registrierung durch den
Teilnehmer über die KOM-LE-1.5-Schnittstelle am KOM-LE-Fachdienst nicht
möglich.

Die Übermittlung der KOM-LE-Version vom Anbieter kann hierbei in geeigneter
Form erfolgen. Die jeweilige Client-Version kann aus dem LDAP-Directory
Attribut:komLeDatavom VZD entnommen werden. Geltende KOM-LE-Versionen
sind1.0und1.5und werden in der Form in das
Header-ElementX-KOM-LE-Versioneingetragen.

**A_20650-03 - Übermittlung von Fehlernachrichten**

Das KOM-LE-Clientmodul MUSS bei der Übertragung von Fehlernachrichten ein
Mail-Header-AttributX-KIM-Fehlermeldung mit dem Wert aus der Tabelle
Tab_Fehlercodes_KOMLE-Clientmodule befüllen. **[\<=]**

<table><tr><th>
Fehler

</th><th>
Wert

</th></tr><tr><td colspan="2">
Fehlermeldungen beim Senden einer KIM-Nachricht

</td></tr><tr><td>
Empfänger entfernt, wegen falscher KIM-Version

</td><td>
4001

</td></tr><tr><td>
Anhang konnte nicht zum KOM-LE-Attachment-Service übertragen werden

</td><td>
4002

</td></tr><tr><td>
keine eindeutige Telematik-ID mit Verschlüsselungszertifikat gefunden

</td><td>
4003

</td></tr><tr><td>
Nachricht nicht für alle Empfänger verschlüsselbar

</td><td>
4004

</td></tr><tr><td>
Für einen Empfänger existieren mehrere Verschlüsselungszertifikate mit
unterschiedlichen Telematik-IDs

</td><td>
4005

</td></tr><tr><td colspan="2">
Fehlermeldungen beim Empfangen einer KIM-Nachricht

</td></tr><tr><td>
Anhang konnte nicht vom KOM-LE-Attachment-Service geladen werden

</td><td>
4006

</td></tr><tr><td>
beim Entschlüsseln eines Anhangs ist ein Fehler aufgetreten

</td><td>
4007

</td></tr><tr><td>
Das verwendete Client-Modul unterstützt die in der Mail verwendete Version nicht

</td><td>
4008

</td></tr><tr><td>
Die KIM-Nachricht konnte auf Grund eines nicht verfügbaren Schlüssels nicht
entschlüsselt werden

</td><td>
4009

</td></tr><tr><td>
Die KIM-Nachricht konnte aufgrund des falschen Formats nicht entschlüsselt
werden

</td><td>
4010

</td></tr><tr><td>
Der Konnektor steht für die Entschlüsselung nicht zur Verfügung

</td><td>
4011

</td></tr><tr><td>
Die Prüfsumme des Anhangs stimmt nicht mit der dem Anhang beigefügten
Prüfsumme überein. Der empfangene Anhang entspricht eventuell nicht dem
originalen Anhang

</td><td>
4012

</td></tr><tr><td>
Anhang konnte nicht heruntergeladen werden, da durch zu häufigen Zugriff der
KOM-LE-Attachment-Service den Abruf verweigert.

</td><td>
4013

</td></tr><tr><td>
Die Prüfung der Nachricht hat ergeben, dass die Nachricht nach dem
Verschlüsseln manipuliert wurde. Möglicherweise wurde die verschlüsselte
Nachricht auch an einen nicht empfangsberechtigten Personenkreis versendet.

</td><td>
4014

</td></tr><tr><td>
Die Prüfung der Signatur der Nachricht hat ergeben, dass die Nachricht
manipuliert wurde, um einem anderen Nutzer das Entschlüsseln der Nachricht mit
einem Schlüssel, der nicht in seinem Besitz ist, zu ermöglichen.

</td><td>
4015

</td></tr><tr><td colspan="2">
Sonnstige Fehlermeldungen

</td></tr><tr><td>
Bei der Aktualisierung der PKCS#12-Datei ist ein Fehler aufgetreten

</td><td>
4016

</td></tr><tr><td>
Die KIM-Version des Client-Moduls ist kleiner als die im Verzeichnisdienst zu
seinem Eintrag hinterlegte Version

</td><td>
4017

</td></tr><tr><td>
Übernahme der Fehlercodes und Vermerke aus der Tabelle 

Tab_Verm_Sig_Prüf

</td><td>
[Fehlercode]

</td></tr></table>

Die Fehlermeldungen beim Senden einer KIM-Mail werden über den Fachdienst
zurück an den Sender übermittelt, da eine direkte Rückgabe der
Fehlernachricht zum Client nicht vorgesehen ist. Das Clientmodul befüllt im
Fehlerfall dasX-KIM-Fehlermeldung-Attribut und sendet dies anschließend über
den Fachdienst an den Sender zurück. Die Fehlermeldungen beim Empfang einer
KIM-Mail werden auf direkten Weg dem Empfänger zugestellt. Der Client (z. B.
PVS) muss die Fehlercodes aus der Tabelle Tab_Fehlercodes_KOMLE-Clientmodule
auswerten.

Die folgende Anforderung bezweckt, dass bei Einsatz mehrerer Clientmodule in
unterschiedlichen Versionen, der KIM-Teilnehmer bei Verwendung eines
Clientmoduls in einer kleineren Version darüber informiert wird, dieses zu
updaten.

**A_21387-01 - Prüfung der verwendeten Clientmodul-Version beim Senden**

Das KOM-LE-Clientmodul MUSS vor dem Versenden einer Nachricht die KOM-LE-Version
des Absenders mittels des LDAP-Directory Attributs:komLeDataaus dem
Verzeichnisdienst [gemSpec_VZD#5] abfragen. Ist die KOM-LE-Version des
Clientmoduls kleiner als die im Verzeichnisdienst eingetragene, so MUSS das
Clientmodul den Absender mit einer E-Mail darüber informieren. Aus dem Inhalt
der E-Mail MUSS hervorgehen, dass die verwendete Clientmodul Version veraltet
ist. Die E-Mail ist weder zu signieren noch zu verschlüsseln und entsprichtder
Delivery Status Notification gemäß [RFC3461-3464]. Ist die KOM-LE-Version des
Clientmoduls größer als die im Verzeichnisdienst abgefragte Version MUSS das
Clientmodul das LDAP-Directory Attribut:komLeDatafür den Absender mit der
neuen Versionen überschreiben. **[\<=]**

**A_22416 - Anfragen von technischen Konfigurationsdaten**

Das KOM-LE Clientmodul MUSS beim Versenden einer E-Mail die OperationgetLimitsam
Account Manager aufrufen, um alle technischen Konfigurationsdaten eines Nutzers
(dataTimeToLive, maxMailSize, quota, remainQuota) zu erhalten. Das Clientmodul
KANN für jeden Nutzer-Account die abgerufenen Daten 24 Stunden
zwischenspeichern (cachen). **[\<=]**

**A_22417 - Einfügen des Ablaufdatums in den äußeren Mail-Header**

Das Clientmodul MUSS beim Versand-Vorgang der verschlüsselten Mail einen Header
"Expires" in den Header der äußeren Nachricht aufnehmen. Der Wert ermittelt
sich aus Versandzeitpunkt (TI-Zeit) + TTL(dataTimeToLive) als offset. **[\<=]**

**A_22412 - Behandlung von Zugriffs-Limitierung**

Das Clientmodul MUSS bei Aufruf der Operation read_Attachment() bei der
Rückgabe des HTTP-Fehlercodes 429, das
Mail-Header-AttributX-KIM-Fehlermeldungmit dem Wert gemäß Tabelle
„Tab_Fehlercodes_KOMLE-Clientmodule“4017befüllen und an der Position des
Anhangs ein MIME-Element mitContent-Type: text/plain;
charset=utf-8undContent-Disposition: attachment;
filename=\<Original-Filename\>_Fehlermeldung.txtsowie folgende Informationen
als Inhalt des Anhangs einfügen: Der Anhang { "name": "Dateiname des Anhangs",
"size": Größe des Anhangs in Byte, "type": "MIME-Type des Anhangs" } konnte
nicht abgerufen werden. Als Betreff ist Folgendes zu verwenden:Subject:[Fehler
beim Abruf eines Anhangs *_Fehlermeldung.txt] \<Original-Subject\>. **[\<=]**

**A_21388-01 - Übermittlung der Clientmodul- und Produkttypversion**

Das Clientmodul MUSS im Header ElementX-KIM-CMVersionder äußeren Nachricht die
VendorID, sowie die Produktversion des verwendeten Clientmoduls gemäß des
Formates:"[a-zA-Z0-9_]{1,5}_[0-9]{1,2}\.[0-9]{1,2}\.[0-9]{1,2}(-25[0-5]|-2[0-4][0-9]|-[0-1]?[0-9]?[0-9]){0,1}"
eintragen.Zusätzlich MUSS das Clientmodul im Header ElementX-KIM-PTVersionder
äußeren Nachricht die Produkttypversion des Clientmoduls gemäß des
Formates:"[0-9]{1,2}\.[0-9]{1,2}\.[0-9]{1,2}(-25[0-5]|-2[0-4][0-9]|-[0-1]?[0-9]?[0-9]){0,1}"eintragen.Zusätzlich
MUSS das Clientmodul im Header-Element X-KIM-KONVersion der äußeren
Nachricht die Version des verwendeten Konnektors
gemäß seiner Produktversion im Format
"\<Productname\>\<ProductType\>\<ProductTypeVersion\>\<HWVersion\>\<FWVersion\>  eintragen.
**[\<=]**

Beispiel:X-KIM-CMVersion: [VendorID]_2.1.2-8X-KIM-PTVersion: 1.5.0-2 

X-KIM-KONVersion: \<secunet konnektor 2.0.0\>\<Konnektor
PTV4Plus\>\<4.80.3\>\<2.0.0\>\<4.10.1\>

Die Produkttypversion entspricht dabei der Produkttypversion aus dem
Produkttypsteckbrief. Die Clientmodulversion entspricht dabei der zugelassenen
Produktversion, die im TI-ITSM-System hinterlegt und gepflegt wird.

**A_21389 - Übermittlung der Clientmodul- und Produkttypversion an die gematik**

Der KIM-Anbieter MUSS der gematik auf Anfrage eine nicht-personenbezogene
Gesamtübersicht, der sich im Feld befindenden aktiven KIM-Clientmodule, zur
Verfügung stellen. **[\<=]**

### 3.2 Umgang mit großen Anhängen

Dieses Kapitel beschreibt die Verarbeitung von Mails, welche die Nettogröße
von 25 MB überschreiten. Die Größenbeschränkung auf 25 MB basiert auf den
Konnektoroperationen zum Signieren und Verschlüsseln. Für
dieseOperationen existiert eine Größenbeschränkung auf 25 MB.

E-Mails mit einer Gesamtgröße bis zu 25 MB werden entsprechend den
Festlegungen im KOM-LE 1.0 behandelt. Übersteigt die Größe einer Mail die
25-MB-Grenze, werden alle Anhänge durch das KOM-LE-Clientmodul aus der Mail
entnommen und auf einem Speicher des KOM-LE-Fachdiensts (KAS) abgelegt. Das
KOM-LE-Clientmodul ergänzt die Mail um die Links auf die Anhänge und
versendet sie als KOM-LE-Mail. Das KOM-LE-Clientmodul des Empfängers erkennt
die Links der entfernten Anhänge in der Mail, lädt die Anhänge vom
KOM-LE-Fachdienst (KAS) und setzt sie wieder in die Mail ein. 

In [gemSpec_FD_KOMLE]  Kapitel "Schnittstelle I_Attachment_Services" wird der
Umgang mit großen Anhängen in einem Sequenzdiagramm erläutert.

### 3.2.1 Senden von Nachrichten mit großen Anhängen

In diesem Kapitel werden Anforderungen an das Clientmodul formuliert, die es
erlauben, Nachrichten von über 25MB inklusiver Anhänge zu versenden.

**A_19355-01 - Prüfen der Nachrichtengröße**

Das KOM-LE-Clientmodul MUSS die Größe der vom KOM-LE-Client erhaltenen
Nachricht (gegen den Wert maxMailSize aus der
Operation I_AccountLimit_Service::getLimits) prüfen. Im Fehlerfall wird dem
KOM-LE-Client der Fehlercode X.3.4 [RFC3463] zurückgegeben. **[\<=]**

**A_19356-04 - Prüfen der Version des Empfängers**

Das KOM-LE-Clientmodul MUSS die vom Empfänger verwendete KOM-LE-Version
prüfen. Das KOM-LE-Clientmodul MUSS dazu die KOM-LE-Version mittels des
LDAP-Directory Attributs:komLeDataaus dem Verzeichnisdienst [gemSpec_VZD#5]
abfragen. Ist das LDAP-Directory Attribut:komLeDatafür den Empfänger
undefiniert, dann muss ein KOM-LE-Clientmodul mit einer Version 1.0 angenommen
werden.Wenn eine Mail größer als 25 MB an einen Empfänger mit KOM-LE-Version
\< 1.5 versendet werden soll, MUSS das KOM-LE-Clientmodul diesen Empfänger aus
der Mail entfernen. Beim Entfernen eines Empfängers MUSS das
KOM-LE-Clientmodul den Absender mit einer E-Mail über den Fehlerfall
informieren. Aus dem Inhalt der Fehlernachricht müssen alle aus der Mail
entfernten Empfänger hervorgehen. Die Fehlernachricht ist weder zu signieren
noch zu verschlüsseln und entsprichtder Delivery Status Notification gemäß
[RFC3461-3464].Kann die Mail für keinen der Empfänger versendet werden, wird
das Senden der Nachricht abgebrochen. Dabei wird dem MTA das RSET-Kommando
gesendet und das Clientsystem wird mit dem SMTP-Antwortcode 451über den
Fehlerfall informiert. **[\<=]**

**A_22340 - Cachen vom KOM-LE-Versionen**

Das Clientmodul MUSS das Cachen von KOM-LE-Versionen der Mail-Empfänger nach
der Abfrage am VZD für eine maximale Zeitdauer von 24 Stunden unterstützen.
**[\<=]**

**A_19357-01 - Extrahieren des Anhanges**

Das KOM-LE-Clientmodul MUSS gewährleisten, dass die Nachrichtengröße nicht 25
MB überschreitet. Hierzu MUSS das KOM-LE-Clientmodul alle Anhänge aus der
Mail extrahieren. Die Anhänge müssen inklusive ihrer Content-Header aus dem
Mail-Body extrahiert werden. **[\<=]**

**A_19358 - Erzeugung symmetrischer Schlüssel**

Das KOM-LE-Clientmodul MUSS für die Verschlüsselung der Anhänge einen
symmetrischen Schlüssel generieren. Hierbei MUSS das KOM-LE-Clientmodul die
Kriterien gemäß [gemSpec_Krypt] einhalten. **[\<=]**

**A_19364-01 - Freigabelink in die Mail aufnehmen**

Das KOM-LE-Clientmodul MUSS das Ergebnis der Operation add_Attachment
[gemSpec_FD_KOMLE] prüfen. Bei einem HTTP-Status 201 MUSS das
KOM-LE-Clientmodul den zurückgelieferten Freigabelink in die
KIM-Attachment-Datenstruktur des Anhangs im Mail-Body aufnehmen. **[\<=]**

Mit der folgenden Anforderung wird sichergestellt, dass ein Client nicht bereits
unerwünschten Kontent (über die Attachment Datenstruktur) in die an das
Clientmodul übergebene KIM-Mail eingefügt hat.

**A_22341 - Prüfen der Nachrichtenanhänge**

Das KOM-LE-Clientmodul MUSS die vom KOM-LE-Client erhaltene Nachricht auf
Vorhandensein von MIME konformen Content-Headern mit Content-Type: text/plain;
charset=utf-8 sowie ein Content-Disposition: x-kas prüfen. Ist mindestens ein
derartiger Content-Header in der Nachricht enthalten, wird dem KOM-LE-Client
der SMTP-Antwortcode 451zurückgegeben. **[\<=]**

**A_19359-06 - Einbetten von Informationen großer Anhänge**

Das KOM-LE-Clientmodul MUSS für jeden auf dem KAS abgelegten Anhang die
folgende KIM-Attachment-Datenstruktur gemäß [Attachment_Schema] - an der
Position des extrahierten Anhanges im Mail-Body -  einfügen:

Tabelle1KIM-Attachment-Datenstruktur

<table><tr><th>
Attribut in KIM-Attachment-Datenstruktur

</th><th>
Wert

</th></tr><tr><td>
name

</td><td>
Dateiname des Anhangs

</td></tr><tr><td>
link

</td><td>
Freigabelink des Anhangs

</td></tr><tr><td>
k

</td><td>
AES-GCM Key des Anhangs (symmetrischer Schlüssel) im Base64 Format 

</td></tr><tr><td>
hash

</td><td>
Hashwert des Anhangs (entsprechend A_19644 [gemSpec_Krypt] zu bilden) im Base64
Format

</td></tr><tr><td>
type

</td><td>
MIME-Type des Anhanges

</td></tr><tr><td>
size

</td><td>
Größe des Anhangs in Byte

</td></tr></table>

Vor der KIM-Attachment-Datenstruktur MUSS ein MIME konformer Content Header mit

Content-Type: text/plain

;

charset=utf-8

 sowie ein

Content-Disposition: x-kas

eingefügt werden. **[\<=]**

Beispiel für eine Mail mit zwei Anhängen vor der Entnahme der Anhänge:

From: "Sender" \<sender@maildomain.de\>  
To: \<empfaenger@maildomain.de\> 

Subject: Mail mit zwei Anhängen  
Mime-Version: 1.0

X-KIM-Dienstkennung: KIM-Mail;Default;V1.0

Content-Type: multipart/mixed; boundary="body_part_boundary"

--body_part_boundary  
Content-Type: text/plain; charset=utf-8 

Content-Transfer-Encoding: quoted-printable  
Content-Disposition: inline 

Ein Dokument und eine Aufnahme im Anhang.  
--body_part_boundary 

Content-Type: application/msword; name="MR-2020-04-01-xyz.doc" 

Content-Transfer-Encoding: base64  
Content-Disposition: attachment;
filename="MR-2020-04-01-xyz.doc" 

ABCDABCDABCDABCDABCDABCDABCDABCDABCDABCDABCDABCDABCDABCDABCDABCDABCDABCDABCD 

[Anhang gekürzt] 

ABCDABCDABCDABCDABCDABCDABCDABCDABCDABCDABCDABCDABCDABCDABCDABCDABCDABCDABCD 

ABCDABCDABCDABCDABCDABCDABCD==  
--body_part_boundary  
Content-Type:
image/jpeg; name="Roentgenbild-375632378.jpg"  
Content-Transfer-Encoding:
base64  
Content-Disposition: attachment; filename="Roentgenbild-375632378.jpg"
 
/9j/4AAQSkZJRgABAQEASSBIAAD/2wBDAAEBAQEBAQEBAQEBAQEBAQEDAQEBAQEBAQEBAEEBAQEB 

[Anhang gekürzt] 

RAQFRBcwRD8H6y8B+voDMoSa1I4Md6+UMzwKVdT3W/fz4cotgwwoZDa1sbvrwU1QcEyNlI3KwKwZ 

uiFj1Ka6BVAM2WU4rCh+xfXS1/p573//2Q==  
--body_part_boundary--

Die gleiche Mail nach Entnahme der Anhänge:

From: "Sender" \<sender@maildomain.de\>  
To: \<empfaenger@maildomain.de\> 

Subject: Mail mit zwei Anhängen  
Mime-Version: 1.0  
Content-Type:
multipart/mixed; boundary="body_part_boundary"  
--body_part_boundary 

Content-Type: text/plain; charset=utf-8  
Content-Transfer-Encoding:
quoted-printable  
Content-Disposition: inline  
Ein Dokument und eine Aufnahme
im Anhang.  
--body_part_boundary  
Content-Type: text/plain; charset=utf-8 

Content-Disposition: x-kas

  {  
    "name":     "MR-2020-04-01-xyz.doc",  
    "link":   
 "HTTPS://KIM-FD1.telematik.de/CXFDTE82346dfzwr7634dfs76sd76sdtzq376e3tzsd", 

    "k":       
"RzVEY3M0MzkmNGZkc2RneCVoX2tkdFQlNXczZnZDdDM2ZGZ2eGZzJDYxITJndmR1VWpzKGk=", 

    "hash":     "Z6A65Z2dasI2I00mM7uxtQjLsEwwl+WLMnDw8eLntaA=",  
   
"size":     143271,  
    "type":     "application/msword"  
   } 

--body_part_boundary  
Content-Type: text/plain; charset=utf-8 

Content-Disposition: x-kas

  {  
    "name":     "Roentgenbild-375632378.jpg",  
    "link":   
 "HTTPS://KIM-FD1.telematik.de/Cduiz763478dfjkdfjhgow4784JHKZsdtq376e3t478d", 

    "k":       
"Ry80ZmRpdWhjczQzOSY0ZmRzZGd4JWhfa2R0VCU1dzNmdkzZkYXNlcmZnODkzNDV1aXNyZg==", 

    "hash":     "Hp30Rx6T9aX8PUmyuASDDIAJ2lPAwbPdc5OSAMK49I=",  
   
"size":     32573,  
    "type":     "image/jpeg"  
   } 

--body_part_boundary--

**A_19360-01 - Verschlüsselung des Anhanges**

Das KOM-LE-Clientmodul MUSS den Anhang mit dem erzeugten symmetrischen
Schlüssel gemäß GS-A_5016 [gemSpec_Krypt] verschlüsseln. **[\<=]**

**A_19361-01 - Lokalisierung des KIM Fachdienstes**

Das KOM-LE-Clientmodul MUSS mittels DNS Service Discovery den FQDN vom KIM
Fachdienst und dessen zugehörigen KAS des Senders ermitteln. **[\<=]**

Die für die Lokalisierung  benötigten DNS Service-Records werden in der
[gemSpec_FD_KOMLE] im Kapitel 3.4 Service Lokalisierung beschrieben.

**A_19362 - Client Authentifizierung**

Das KOM-LE-Clientmodul MUSS eine beidseitige gesicherte TLS-Verbindung zum KAS
des Fachdienstes aufbauen. **[\<=]**

Der KAS ist ein Bestandteil des Fachdiensts. Deshalb gelten für die
TLS-Verbindungen (inklusive genutzter Zertifikate) zum KAS ebenfalls die
Festlegungen von Kap. 4.1.4.

**A_19363-02 - Übertragung von Anhängen**

Das KOM-LE-Clientmodul MUSS für die Übertragung des Anhanges, die vom KAS des
Fachdienstes bereitgestellte Operation add_Attachment aufrufen.  
Im Fehlerfall
MUSS das KOM-LE-Clientmodul den Absender mit einer E-Mail über den Fehlerfall
informieren. Aus dem Inhalt der Fehlernachricht MUSS hervorgehen, welcher
Anhang nicht an den KAS übermittelt werden konnte. Die Fehlernachricht ist
weder zu signieren noch zu verschlüsseln und entspricht der Delivery Status
Notification gemäß [RFC3461-3464]. Zusätzlich muss der vom KAS gemeldete
Fehlertext wie folgt eingefügt werden: Fehlertext: \<message\>. Die
ursprüngliche KOM-LE-Nachricht darf im Fehlerfall nicht versendet werden .
**[\<=]**

**A_19365-01 - Senden der Nachricht**

Das KOM-LE-Clientmodul MUSS die – um die großen Anhänge reduzierte –
E-Mail-Nachricht entsprechend den Festlegungen für Mails kleiner oder gleich
25 MB senden. **[\<=]**

**A_22419 - Behandlung von Quota-Überschreitung**

Wenn das Clientmodul beim Versand eines E-Mail-Anhanges vom KAS einen Fehlercode
507 erhält, MUSS es den Mailversand abbrechen und dem KOM-LE-Client den
SMTP-Fehlercode 521 gemäß [RFC3463] zurückgeben und die existierende
SMTP-Verbindung zum Mail Server abbauen. **[\<=]**

**A_22427 - I_Attachment_Services - Content-Length**

Das KOM-LE-Clientmodul MUSS bei der Übertragung des Anhanges das
HTTP-Header-Element "Content-Length" immer mit der Gesamt-Länge des Bodys
befüllen. **[\<=]**

### 3.2.2 Empfangen von Nachrichten mit großen Anhängen

In diesem Kapitel werden Anforderungen an das Clientmodul formuliert, die es
erlauben, große Anhänge zu empfangen.

**A_19367 - Empfangen der Nachricht**

Das KOM-LE-Clientmodul MUSS die E-Mail-Nachricht empfangen. **[\<=]**

Eine KOM-LE 1.0 E-Mail ist maximal 25 MB groß (netto). Hierbei ist zu beachten,
dass durch die Base64-Kodierung der Nachricht die zu verarbeitende
Bruttogröße um den Faktor 1,37 erhöht wird (brutto).

**A_19368 - Client Authentifizierung**

Das KOM-LE-Clientmodul MUSS eine beidseitige gesicherte TLS-Verbindung  zum KAS
des Fachdienstes aufbauen. **[\<=]**

Die Anforderungen an die TLS Authentifizierung und die Zertifikate entsprechen
den Anforderungen von dem Fachdienst.

**A_19369-01 - Ermittlung der Informationen über die Anhänge**

Das KOM-LE-Clientmodul MUSS die Dateinamen, Hash-Werte und die Freigabelinks
der extrahierten Anhänge sowie den symmetrischen Schlüssel aus der
KIM-Attachment-Datenstruktur der Anhänge im Mail-Body entnehmen. **[\<=]**

**A_19370-03 - Download von Anhängen**

Das KOM-LE-Clientmodul MUSS die Anhänge zu den entnommenen Freigabelinks via
der Operation read_Attachment am KAS des Fachdienstes herunterladen.  
Wenn
beim Herunterladen eines Anhangs ein Fehler auftritt, dann MUSS das
KOM-LE-Clientmodul die empfangene, dem KOM-LE-S/MIME-Profil entsprechende
Nachricht, als eine message/rfc822 MIME-Einheit in einer neuen multipart/mixed
MIME-Nachricht dem Clientsystem übermitteln. Zusätzlich muss diese neue
multipart/mixed MIME-Nachricht eine text/plain MIME-Einheit mit dem Fehlertext
[Tab_Fehlertext_Download] enthalten. Die orig-date, from, sender, reply-to, to
und cc Header-Elemente der neuen multipart/mixed Nachricht werden aus der
empfangenen Nachricht übernommen. Das subject Header-Element der neuen
multipart/mixed Nachricht erhält den Wert „Mindestens ein Anhang der
Nachricht konnte nicht heruntergeladen werden“. **[\<=]**

Bei einer Nachricht mit dem Subject „Mindestens ein Anhang der Nachricht
konnte nicht heruntergeladen werden“ gibt es folgende Optionen:

 ---> UL

Tabelle "Tab_Fehlertext_Download Fehlertext beim Download von Anlagen" enthält
den Fehlertext, der in die Nachricht eingeführt wird, wenn der Download von
Anhängen nicht durchgeführt werden konnte.

<table><tr><th>
Bedingung

</th><th>
Fehlertext

</th></tr><tr><td>
Mindestens ein Anhang der Nachricht konnte nicht heruntergeladen werden.

</td><td>
Nicht alle Anhänge dieser Nachricht konnten heruntergeladen werden. Bitte
leiten Sie diese Nachricht nach einer angemessenen Zeit an Ihre eigene
E-Mail-Adresse (\<Email Adresse\>) weiter. Beim nächsten Abholen wird der
Download wiederholt.

</td></tr></table>

**A_19371-03 - Entschlüsselung der Anhänge**

Das KOM-LE-Clientmodul MUSS die heruntergeladenen Anhänge mit dem symmetrischen
Schlüssel entschlüsseln.  
Wenn beim Entschlüsseln eines Anhangs ein Fehler
auftritt, dann MUSS das KOM-LE-Clientmodul an der Position des Anhangs ein
MIME-Element mit Content-Type: text/plain;
charset=utf-8, Content-Transfer-Encoding: quoted-printable
und Content-Disposition: attachment;
filename=\<Original-Filename\>_Fehlermeldung.txt sowie folgende Informationen
als Inhalt des Anhangs einfügen: Der Anhang { "name":  "Dateiname des
Anhangs",  "size":  Größe des Anhangs in Byte,  "type":  "MIME-Type des
Anhangs" } konnte nicht entschlüsselt werden. Im Betreff der entschlüsselten
Nachricht ist Folgendes anzugeben: [Fehler beim Entschlüsseln eines Anhangs
*_Fehlermeldung.txt] \<Original-Subject\>. **[\<=]**

**A_19372-02 - Prüfen des Anhanges**

Das KOM-LE-Clientmodul MUSS den Hash-Wert des entschlüsselten Anhanges
entsprechend [A_19644] bilden und mit dem aus dem Content-Header des Anhangs im
Mail-Body entnommenen Hash-Wert vergleichen. Bei einer Nichtübereinstimmung
MUSS das KOM-LE-Clientmodul die Nachricht dem Clientsystem mit dem Anhang und
einem entsprechenden Vermerk zum Anhang übergeben.  
Das KOM-LE-Clientmodul
MUSS den Vermerk mit der folgenden Bildungsregel an den Text der Nachricht
anhängen:  
"Die Prüfsumme des name(gemäß [A_19359]) stimmt nicht überein.
Der empfangene Anhang entspricht eventuell nicht dem originalen Anhang." Es ist
dabei das Format des TextParts zu beachten (mediatype text/html oder
text/plain) und der Vermerk diesem Format anzupassen. **[\<=]**

**A_19374-02 - Zusammensetzen der Mail**

Das KOM-LE-Clientmodul MUSS alle entschlüsselten Anhänge in die Mail an ihrer
ursprünglichen Position integrieren, welche den MIME-Part mit den
Informationen zu diesem Anhang enthältund die eingefügten
KIM-Attachment-Datenstrukturen - inklusive der eingefügten MIME Content
Header -  entfernen.  **[\<=]**

### 3.3 Senden von Nachrichten

### 3.3.1 Übersicht

Beim Senden von KOM-LE-Nachrichten sorgt das Clientmodul dafür, dass die
gesendeten E-Mail-Nachrichten digital signiert und verschlüsselt
dem MailTransfer Agent des KOM-LE-Fachdienstes (weiter im Text als MTA
bezeichnet), bei dem der Sender registriert ist, übermittelt werden. Bei
E-Mail-Nachrichten größer 25 MB werden alle zur E-Mail-Nachricht gehörenden
Anhänge vor der Durchführung der kryptographischen Operationen extrahiert und
symmetrisch verschlüsselt auf dem Fachdienst abgespeichert.

Abbildung 5 stellt die Interaktionen zwischen den am Senden von
KOM-LE-Nachrichten beteiligten Komponenten dar. Aus der Sicht des Clientsystems
agiert das Clientmodul als ein MTA und aus der Sicht des MTAs des Fachdienstes
agiert das Clientmodul als MUA. Für Funktionen wie Datentransport,
kryptographische Operationen und Kommunikation mit dem Verzeichnisdienst
verwendet das Clientmodul entsprechende Dienste der TI-Plattform.

![Abbildung-5][Abbildung-5]

Beim Senden von Nachrichten findet die Kommunikation zwischen dem Clientsystem,
dem Clientmodul und dem MTA über SMTP statt. Das Clientmodul fungiert als SMTP
Proxy, der das Clientsystem mit dem MTA verbindet, die Integrität und
Vertraulichkeit der vom Clientsystem gesendeten Nachricht schützt und die
Nachricht an den MTA übermittelt.

Sobald die Nachricht komplett dem MTA übertragen wurde und der MTA das Ankommen
der Nachricht bestätigt, übergibt das Clientmodul die Verantwortung für die
Nachricht an den MTA. Die Übermittlung von Nachrichten zwischen MTAs ist nicht
Bestandteil dieser Spezifikation.

Es liegt in der Verantwortung des Clientmoduls sicher zu stellen, dass die
Nachricht erfolgreich dem MTA übertragen wird. Falls die Übermittlung einer
Nachricht an den MTA fehlschlägt (z.B. bei Verbindungsaufbau mit dem MTA,
Authentifizierung gegenüber dem MTA, Verschlüsselung oder Signieren der
Nachricht), benachrichtigt das Clientmodul das Clientsystem unter Verwendung
entsprechenden SMTP-Antwortcodes über den Fehler.

Beispiel: Verwendet das Clientsystem beim Senden von Nachrichten falsche
Anmeldungsdaten, erhält es vom Clientmodul „535 5.7.8 Der Nutzer konnte
nicht authentifiziert werden“ als Antwort auf sein AUTH-Kommando.

Das Verhalten des Clientmoduls beim Senden von Nachrichten wird mit Hilfe der in
Abbildung 6 dargestellten Zustandsmuster beschrieben. Die im Dokument
dargestellten Zustände haben nur illustrativen und keinen normativen
Charakter. Die Umsetzung kann sich unterscheiden, solange das Ergebnis das
Gleiche ist. Die den Zuständen zugeordnete Anforderungen sind normativ,
können aber außerhalb des Kontexts dieser Zustände umgesetzt werden.

![Abbildung-6][Abbildung-6]

Das Clientmodul lauscht auf einem TCP Port und wartet bis ein Clientsystem mit
ihm eine Verbindung aufbaut. Sobald dies passiert, geht das Clientmodul in den
CONNECT-Zustand über und betrachtet die SMTP-Verbindung als geöffnet. Die
Verbindung zwischen dem Clientsystem und dem Clientmodul muss mit TLS
geschützt werden.

Im CONNECT-Zustand führt das Clientmodul einen SMTP-Dialog mit dem
Clientsystem, in dem ihm die Anmeldedaten des Nutzers sowie die Adresse und die
Portnummer des MTAs mitgeteilt werden. Sobald die Anmeldedaten und die Adresse
des MTAs übermittelt sind, baut das Clientmodul eine über TLS geschützte
SMTP-Verbindung mit dem MTA auf, authentifiziert sich und geht in den
PROXY-Zustand über.

Im PROXY-Zustand leitet das Clientmodul SMTP-Kommandos und SMTP-Antwortcodes
zwischen dem Clientsystem und dem MTA weiter, bis das Clientsystem mit dem
DATA-Kommando die Übertragung einer Nachricht initiiert. Sobald das
Clientsystem anfängt, Inhalte einer Nachricht zu übertragen, geht das
Clientmodul in den PROCESS-Zustand über.

In PROCESS-Zustand wird die Nachricht entsprechend dem KOM-LE-S/MIME-Profile
[gemSMIME_KOMLE] geschützt und anschließend an den MTA übermittelt. Sobald
die Nachricht erfolgreich an den MTA übertragen wurde oder im Fehlerfall, geht
das Clientmodul in den PROXY-Zustand zurück.

Nachdem die Verbindungen zwischen dem Clientsystem, dem Clientmodul und dem MTA
aufgebaut wurden, übermittelt das Clientmodul die SMTP-Meldungen zwischen dem
Clientsystem und dem MTA so lange die beiden Verbindungen bestehen.

### 3.3.2 CONNECT-Zustand

Sobald die TCP-Verbindung zwischen dem Clientsystem und dem Clientmodul
aufgebaut ist, geht das Clientmodul in den CONNECT-Zustand über.

### 3.3.2.1 Initialisierung

**KOM-LE-A_2007 - SMTP Begrüßung**

Nachdemdie SMTP-Verbindung zwischen dem Clientsystem und dem Clientmodul
aufgebaut ist, MUSS das Clientmodul dem Clientsystem die SMTP-Begrüßung
senden. Um zu signalisieren, dass Extended SMTP unterstützt wird, muss die
Begrüßung „ESMTP“ enthalten. **[\<=]**

Beispiel einer solchen Begrüßung:220 KOM-LE-Clientmodul ESMTP

Das Clientmodul führt einen SMTP-Dialog mit dem Clientsystem bis zum Punkt, an
dem das Clientsystem ihm die Adresse und die Portnummer des MTAs als einen Teil
des während des Authentifizierungsverfahrens übertragenen Benutzernamens
mitteilt (siehe Kapitel 3.2.2.2).

Tabelle Tab_SMTP_Ant_Init beschreibt Antworten, die das Clientmodul dem
Clientsystem im CONNECT-Zustand sendet.

<table><tr><th>
SMTP-Kommando

(Clientsystem -\> Clientmodul)

</th><th>
SMTP-Antwortcode

(Clientmodul -\> Clientsystem)

</th></tr><tr><td>
HELO

</td><td>
“250 OK” Antwortcode

</td></tr><tr><td>
EHLO

</td><td>
“250 OK” Antwortcode mit folgenden EHLO Kennworten:

SIZE \<size\>

AUTH LOGIN PLAIN

8BITMIME

ENCHANCEDSTATUSCODES

DSN

und \<size\> gleich oder großer als 35882577

</td></tr><tr><td>
AUTH

</td><td>
Anmeldungsdaten erhalten und Verbindungsaufbau mit dem MTA beginnen (siehe
Kapitel 3.2.2.2)

</td></tr><tr><td>
RSET, NOOP

</td><td>
„250 OK“ Antwortcode

</td></tr><tr><td>
MAIL, RCPT, DATA

</td><td>
„530 5.7.0“ Antwortcode (Authentication required)

</td></tr><tr><td>
QUIT

</td><td>
„221 OK“ Antwortcode senden und die Verbindung mit dem Clientsystem
schließen

</td></tr><tr><td>
Andere Meldungen

</td><td>
„502  5.5.1“ Antwortcode (Invalid command)

</td></tr></table>

**KOM-LE-A_2008 - Initialer SMTP-Dialog**

Das Clientmodul MUSS, nachdem die SMTP-Verbindung zwischen dem Clientsystem und
dem Clientmodul aufgebautwird und bis zum Punkt an dem das Clientsystem die
Bestätigung des Erfolgs oder Misserfolgs seiner Authentifizierung erwartet,
einen SMTP-Dialog entsprechend der Tabelle Tab_SMTP_Ant_Init mit dem
Clientsystem führen. **[\<=]**

### 3.3.2.2 Verbindungsaufbau mit MTA

Das Clientmodul kann die Verbindung mit dem MTA nur dann aufbauen, wenn ihm das
Clientsystem die Adresse des MTAs und die Portnummer des SMTP-Dienstes
übermittelt. Das Clientmodul erwartet, dass ihm der Domain Name oder die
IP-Adresse und die Portnummer während des Authentifizierungsverfahrens als
Teil des Benutzernamens mitgeteilt werden.

Das Clientmodul führt das Authentifizierungsverfahren mit dem Clientsystem bis
zu dem Punkt, an dem es mit dem entsprechenden Antwortcode die
Authentifizierung akzeptieren oder ablehnen muss. Das Clientmodul allein kann
das Clientsystem nicht authentifizieren. Die Authentizität der Zugangsdaten
kann nur vom MTA überprüft werden. Dazu authentifiziert sich das Clientmodul
im Auftrag vom Clientsystem gegenüber dem MTA.

Die MTA-Adresse und die Portnummer des SMTP-Dienstes sind als Teil des
SMTP-Benutzernamens vom Clientsystem zu übergeben. Sie sind vom eigentlichen
Benutzernamen durch das Zeichen ’#’ getrennt und als adresse:port String
formatiert.

Um mit der SM-B über den Konnektor kommunizieren zu können, werden dem
KOM-LE-Clientmodul ebenfalls als Teil des SMTP-Benutzernamens, die Parameter

 ---> UL

übergeben (siehe Kapitel 3.5 und [gemSpec_Kon] für Details zu MandantId,
ClientSystemId und WorkplaceId). Der optionale Parameter KonnektorID, als
Bestandteil des Aufrufkontext für SM-B, ermöglicht die Unterstützung von
Multikonnektor-Umgebungen. Die Parameter entsprechen denen des aufrufenden
Clients und werden voneinander durch das Zeichen ’#’ getrennt.

Der Aufbau des SMTP-Benutzernamens entspricht somit dem folgenden Muster und
hat der den Parametern vorangestellten Nummer in der Reihenfolge zu entsprechen:

[0] Benutzername[1] \<Domain Adresse des SMTP-Servers\>:\<Port\>[2] MandantId[3]
ClientsystemId[4] WorkplaceId— \<optional\> —[5] KonnektorId[...]

![Abbildung-7][Abbildung-7]

Beispiel:

Bei folgenden Informationen

 ---> UL

erwartet das Clientmodul, dass das Clientsystem ihm folgenden SMTP-Benutzernamen
als String überträgt:

erik.mustermann@hrst_domain.kim.telematik#hrst_domain.kim.telematik:465#1#KOM_LE#7#Konn_1

Das KOM-LE-Clientmodul bricht die Kommunikation mit dem entsprechende
SMTP-Antwortcode ab (siehe Tabelle Tab_SMTP_Verbindung), wenn der erhaltene
SMTP-Benutzername nicht alle erforderlichen Parameter enthält. Beinhaltet der
SMTP-Benutzername zusätzliche optionale durch ‚#’ abgegrenzte Parameter
(z. B. #KonnektorId), dann müssen diese Parameter vom Clientmodul ausgewertet
werden und der Sendevorgang wird fortgesetzt.

Für SMTP-Authentifizierung existieren sowohl Mechanismen für die Übertragung
von Nutzername und Passwort im Klartext (PLAIN und LOGIN) als auch
Challenge-Response-Mechanismen. Die auf Challenge-Response (DIGEST-MD5,
CRAM-MD5, NTLM) basierenden Mechanismen machen das Extrahieren des Passworts
aus der Challenge-basierten Response für das Clientmodul unmöglich. Deshalb
werden für die SMTP-Authentifizierung nur die PLAIN oder LOGIN-Mechanismen
verwendet.

Sobald das Clientmodul die Anmeldedaten des Nutzers erhält, extrahiert es die
Adresse des MTAs und die Portnummer des SMTP-Dienstes aus dem Nutzernamen und
baut damit  die Verbindung zum MTA auf. Die Verbindung wird über TLS
geschützt. Details zum Aufbau der TLS-Verbindung werden in Kapitel 4.1.3
beschrieben.

Tabelle Tab_SMTP_Verbindung enthält SMTP-Antwortcodes, die das Clientmodul dem
Clientsystem bei einem Verbindungsaufbau mit dem MTA übermittelt.

<table><tr><th>
Bedingung

</th><th>
SMTP-Antwortcode

(Clientmodul -\> Clientsystem)

</th></tr><tr><td>
Das Clientmodul hat sich erfolgreich gegenüber dem MTA mit den vom Clientsystem
erhaltenen Anmeldungsdaten authentifiziert.

</td><td>
235 2.7.0 (Authentication successful)

</td></tr><tr><td>
Das Clientsystem verwendet für die SMTP-Authentifizierung einen anderen
Mechanismus als PLAIN oder LOGIN.

</td><td>
504 5.7.4 (Security features not supported)

</td></tr><tr><td>
Die vom Clientsystem erhaltene SMTP-Authentifizierungsidentität ist nicht
vollständig oder  falsch formatiert (MTA-Adresse, MandantId, ClientSystemId,
WorkplaceID oder Platzhalter fehlt – siehe Abbildung 6 "Abb_MTA_Nutzername
Format des SMTP- Benutzernamens")

</td><td>
501 5.5.4 (Invalid command arguments)

</td></tr><tr><td>
Bei Übergabe der Parameter für den Aufrufkontext für SM-B (MandantID,
ClientSystemID oder WorkplaceID) antwortet der Konnektor mit einem SOAP Fault
(Code: 4004 - 4006)

</td><td>
501 (Syntax error in parameters or arguments)

</td></tr><tr><td>
Die Verbindung zwischen dem Clientmodul und dem MTA kann nicht aufgebaut werden.

</td><td>
454 4.7.0 (Temporary authentication failure)

</td></tr><tr><td>
Die Authentifizierung gegenüber dem MTA schlägt fehl.

</td><td>
535 5.7.8 (Authentication credentials invalid)

</td></tr></table>

**KOM-LE-A_2015-01 - Ergebnis des Verbindungsaufbaus mit dem MTA**

Das Clientmodul MUSS das Clientsystem über das Ergebnis des Verbindungsaufbaus
mit dem MTA mit den in Tabelle Tab_SMTP_Verbindung beschriebenen
SMTP-Antwortcodes informieren. **[\<=]**

Die Verbindungen zwischen dem Clientsystem und dem Clientmodul sowie zwischen
dem Clientmodul und dem MTA bleiben solange offen, bis eine von beiden
geschlossen oder abgebrochen wird. Sobald eine der beiden Verbindungen
geschlossen oder abgebrochen wird, übermittelt das Clientmodul die
ausstehenden SMTP-Meldungen und schließt die andere Verbindung. Die
SMTP-Sitzung wird damit für den MTA, das Clientsystem und das Clientmodul
beendet.

Beispiel: Nachdem das Clientmodul das QUIT-Kommando vom Clientsystem erhalten
und dem MTA übermittelt hat, bestätigt der MTA das Ankommen des Kommandos mit
dem „221“ Antwortcode und schließt die Verbindung mit dem Clientmodul. Das
Clientmodul übermittelt den „221“ Antwortcode dem Clientsystem und
schließt die Verbindung mit dem Clientsystem.

**KOM-LE-A_2009 - Unterstützung der Serverteile der Mechanismen PLAIN und
LOGIN**

Das Clientmodul MUSS fürdieSMTP-Authentifizierung des
Clientsystemsausschließlichdie Serverteile der SASL-Mechanismen PLAIN und
LOGIN unterstützen. **[\<=]**

**KOM-LE-A_2010 - Extrahieren von MTA-Adresse, Portnummer und
Kartenaufrufkontext**

Das Clientmodul MUSS den Benutzernamen, die MTA-Adresse, die zugehörige
Portnummer und den Kartenaufrufkontext ausdemvom Clientsystem
erhaltenenSMTP-Benutzernamen entsprechend Abbildung Abb_MTA_Nutzer_Name
extrahieren. **[\<=]**

**A_21457 - Extrahieren der KonnektorId für Multikonnekor-Umgebungen**

Das Clientmodul MUSS, wenn der Parameter KonnektorId im erhaltenen
SMTP-Benutzernamen erhalten ist, diesen extrahieren und auswerten, um während
der SMTP-Verbindung, mit einem definierten Konnektor, Nachrichten
weiterzuleiten. **[\<=]**

Der Parameter KonnektorId ist eine Referenz auf eine URI oder eine IP-Adresse
eines Konnektors, um in einer Umgebung mit mehreren Konnektoren einen
bestimmten Konnektor ansprechen zu können. Diese kann beispielweise in einer
Konfigurations-Datei im Clientmodul hinterlegt sein.

**A_21519-02 - Überprüfung des SMTP-Benutzernames**

Das Clientmodul MUSS die übergebene SMTP-Benutzername-Zeichenkette auf
Vollständigkeit überprüfen. Werden optionale Bestandteile des
SMTP-Benutzernamens nicht genutzt, MUSS sichergestellt werden, dass später
folgende optionale Bestandteile in ihrer vorgegebenen Position platziert
werden. Als Platzhalter ist in so einem Fall "*" zu verwenden. Wenn die
SMTP-Benutzername-Zeichenkette nicht vollständig ist, MUSS das Clientmodul den
SMTP Fehlercode gemäß Tabelle "Tab_SMTP_Verbindung SMTP-Antwortcodes für
MTA-Verbindungsaufbau" an das Clientsystem senden und den Vorgang abbrechen.
**[\<=]**

Beispiel einer vollständigen SMTP-Benutzername-Zeichenkette:

 ---> UL

erik.mustermann@hrst_domain.kim.telematik#hrst_domain.kim.telematik:465#1#KOM_LE#7

 ---> UL

erik.mustermann@hrst_domain.kim.telematik#hrst_domain.kim.telematik:465#1#KOM_LE#7#Konn_1

Erfolgt die Einbindung von KIM in ein bestehendes Mail-System, kann ein
übergebener Delimiter ":" zwischen dem Serveranteil und dem Port (z.
B.hrst_domain.kim.telematik:465) des SMTP-Benutzernamens zu Fehlern bei der
Interpretation im Bestandsystem führen. Es werden daher weitere Delimiter im
Benutzernamen unterstützt, sofern die Funktionalität gemäß der
Bestandsanforderungen zu den Benutzernamen, in semantischer Abgrenzung,
uneingeschränkt erhalten bleiben. Es gilt, dass die Bestandteile des
SMTP-Benutzernames in ihrem semantischen Bezug gemäß [RFC1123, RFC2822]
einhalten müssen.

**KOM-LE-A_2011 - Verbindungsaufbau mit dem MTA über MTA-Adresse und
Portnummer**

Das Clientmodul MUSSdie MTA-Adresse und die Portnummer, dieausdemvom
Clientsystem erhaltenenSMTP-Benutzernamenextrahiert wurden (sieheAbbildung
Abb_MTA_Nutzer_Name), für den Verbindungsaufbau mit dem MTA verwenden. **[\<=]**

**KOM-LE-A_2012 - Authentisierung gegenüber dem MTA mit Benutzernamen und
Passwort**

DasClientmodul MUSSden Benutzernamen, derausdemvom Clientsystem
erhaltenenSMTP-Benutzernamenextrahiert wurde (sieheAbbildung
Abb_MTA_Nutzer_Name) sowie das vom Clientsystem erhaltene Passwortfür die
Authentisierung gegenüber den MTA verwenden. **[\<=]**

**KOM-LE-A_2013 - Unterstützung der Clientteile der Mechanismen PLAIN und
LOGIN**

Das Clientmodul MUSS fürdieSMTP-Authentifizierung mit dem
MTAdieClientteilederder SASL-Mechanismen PLAIN und LOGIN unterstützen. **[\<=]**

**KOM-LE-A_2014 - Authentifizierung gegenüber MTA mit anderen Mechanismen als
PLAIN und LOGIN**

Das Clientmodul KANN fürdieAuthentifizierunggegenüberdem MTA andere
Authentifizierungsmechanismen als PLAIN oder LOGIN benutzen. **[\<=]**

**KOM-LE-A_2016 - Schließen der SMTP-Verbindung mit dem Clientsystem**

Das Clientmodul MUSS die SMTP-Verbindung mit dem Clientsystem aufrechterhalten.
Das Schließen der Verbindung ist nur bei folgenden Ausnahmen zulässig:

 ---> UL

**[\<=]**

**KOM-LE-A_2017 - Schließen der SMTP-Verbindung mit dem MTA**

Das Clientmodul MUSS die SMTP-Verbindung mit dem MTA aufrechterhalten. Das
Schließen der Verbindung ist nur zulässig:

 ---> UL

**[\<=]**

Nachdem sich das Clientsystem gegenüber dem MTA erfolgreich authentifiziert
hat, geht das Clientmodul in den PROXY-Zustand über. Anderenfalls bleibt das
Clientmodul im CONNECT-Zustand.

### 3.3.3 PROXY-Zustand

Im PROXY-Zustand vermittelt das Clientmodul SMTP-Meldungen und Antwortcodes
zwischen dem Clientsystem und dem MTA. Das Clientmodul bleibt in diesem Zustand
bis das Clientmodul das DATA-Kommando bekommt und der MTA das Erhalten von
diesem Kommando mit dem Antwortcode „354“ bestätigt. Das Clientmodul
leitet den Antwortcode „354“ an das Clientsystem weiter und geht in den
PROCESS-Zustand über.

**KOM-LE-A_2018 - Weiterleitung von SMTP-Meldungen und Antwortcodes**

Nach erfolgreicher Beendigung des Authentifizierungsverfahrens mit dem MTA
MUSSdasClientmodulallevom Clientsystem erhaltenen SMTP-Meldungen,mit Ausnahme
des RCPT-Kommandos und der Inhalte von E-Mail-Nachrichten(inklusive dem
DATA-Kommando)sowie alle vom MTA erhaltenen Antwortcodes ohne Veränderung dem
MTA bzw. dem Clientsystem unverzüglich übermitteln. **[\<=]**

**KOM-LE-A_2176 - Prüfen auf gültiges ENC-Zertifikat für den Empfänger im
RCPT-Kommando**

Das Clientmodul MUSS, wenn es vom Clientsystem ein RCPT TO:\<recipient-address\>
Kommando erhält, prüfen, ob für den im Kommando aufgeführten Empfänger
mindestens ein gültiges ENC-Zertifikat existiert. Da die Nachricht nur an
Empfänger, die ein gültiges ENC-Zertifikat besitzen weitergeleitet werden
darf, MUSS das Clientmodul im Negativfall das Kommando verwerfen und dem
Clientsystem den Antwortcode „550“ senden . Im Positivfall MUSS das
Clientmodul das Kommando an den MTA weiterleiten. **[\<=]**

### 3.3.4 PROCESS-Zustand

Im PROZESS-Zustand nimmt das Clientmodul die Inhalte der vom Clientsystem
gesendeten Nachricht entgegen. Mit Hilfe von Diensten der TI-Plattform schützt
es die Vertraulichkeit und Integrität der Nachricht entsprechend dem
KOM-LE-S/MIME-Profil [gemSMIME_KOMLE]. Anschließend leitet das Clientmodul die
geschützte Nachricht an den MTA, bei dem der Nutzer registriert ist, weiter.
Im Erfolgsfall wird das Clientsystem über das Versenden der Nachricht
informiert. Im Fehlerfall wird das Clientsystem mit dem entsprechenden
Antwortcode über den Fehler benachrichtigt. Im folgenden Text wird eine
entsprechend dem KOM-LE-S/MIME-Profil geschützte Nachricht auch als
KOM-LE-S/MIME-Nachricht bezeichnet.

### 3.3.4.1 Empfang und Weiterleitung einer Nachricht

Nachdem die Bereitschaft zum Empfangen der Nachricht dem Clientsystem mit dem
Antwortcode „354“ bestätigt wurde, erwartet das Clientmodul, dass das
Clientsystem mit der Übertragung der Nachricht fortfährt. Die Inhalte der
Nachricht werden im Clientmodul zwischengespeichert und sobald das Clientsystem
durch die „\<CRLF\>.\<CRLF\>“ Zeichensequenz das Ende der Nachricht
markiert, werden die Inhalte der Nachricht im Clientmodul durch digitale
Signatur und die Verschlüsselung geschützt. Die Details werden im Kapitel
3.3.4.1.1 beschrieben.

KOM-LE bietet die Möglichkeit Nachrichten, die beim Abholen nicht
entschlüsselt wurden (z.B. auf Grund eines fehlenden HBA mit dem
entsprechenden privaten Schlüssel), nachträglich zu entschlüsseln. Um die
nachträgliche Entschlüsselung einer verschlüsselten KOM-LE-Nachricht
durchführen zu können, schickt der Empfänger die verschlüsselte Nachricht
als einmessage/rfc822Anhang in einer neuen Nachricht an seine eigene
E-Mail-Adresse. Beim nächsten Abholvorgang kann diese Nachricht, sofern die
erforderliche Karte vorhanden ist, durch das Clientmodul entschlüsselt werden.
Werden solche Nachrichten im Clientmodul erkannt, werden sie weder signiert
noch verschlüsselt. Stattdessen wird die verschlüsselte KOM-LE-Nachricht aus
demmessage/rfc822Anhang extrahiert und diefromHeader-Elemente werden durch
dasfromHeader-Element (E-Mail-Adresse des Absenders) der
angekommenenmultipartMIME-Nachricht ersetzt. Anschließend wird die Nachricht
dem MTA übermittelt. Die Details werden im Kapitel 3.3.4.1.2 beschrieben.

Die Benachrichtigung des Clientsystems über den Erfolg des Sendens einer
Nachricht findet nur dann statt, wenn der MTA die Übernahme der Verantwortung
für die Nachricht mit positiven Erledigungsstatus über den „250“
Antwortcode bestätigt. Ab diesem Moment gilt die Nachricht für das
Clientsystem als versendet und der MTA hat sich zu ihrer Lieferung oder
Benachrichtigung des Senders über einen Fehlerfall verpflichtet.

Nachdem das Clientsystem über das erfolgreiche Senden der Nachricht oder über
einen Fehlerfall mit entsprechendem Antwortcode benachrichtigt wurde, löscht
das Clientmodul die zwischengespeicherten Inhalte der Nachricht und geht
zurück in den PROXY-Zustand.

**KOM-LE-A_2019 - Signatur und Verschlüsselung entsprechend
KOM-LE-S/MiME-Profil**

Das Clientmodul MUSS die vom Clientsystem erhaltene KOM-LE-Nachricht
entsprechend demKOM-LE-S/MIME-Profil[gemSMIME_KOMLE]signieren und
verschlüsseln und anschließend dem MTA übermitteln. **[\<=]**

### 3.3.4.1.1 Bearbeitung einer ungeschützten Nachricht

Um die Vertraulichkeit und die Integrität einer Nachricht zu schützen wird die
Nachricht entsprechend dem KOM-LE-S/MIME-Profil signiert und verschlüsselt.
Für das Signieren und die Verschlüsselung nutzt das Clientmodul die Dienste
der TI-Plattform. Die folgende Abbildung stellt den prinzipiellen Ablauf und
die Aktivitäten des Clientmoduls beim Erzeugen einer dem KOM-LE-S/MIME-Profil
entsprechenden Nachricht dar. Hierbei wird von einer E-Mail-Nachricht Größe
von kleiner oder gleich 25 MB ausgegangen.

![Abbildung-8][Abbildung-8]

Für das digitale Signieren einer Nachricht verwendet das Clientmodul den
privaten PrK.HCI.OSIG-Schlüssel der SM-B. Der Zugriff auf die entsprechende
Karte und die Erstellung der Signatur erfolgt über die Aufrufe der
entsprechenden Operationen der Außenschnittstelle des Konnektors. Eine
detaillierte Beschreibung erfolgt im Kapitel 3.8.1.

Wenn das Signieren fehlschlägt, wird das Senden der Nachricht abgebrochen indem
dem MTA das RSET-Kommando übermittelt wird und das Clientsystem mit dem
Antwortcode „451“ inklusive der entsprechenden Fehlermeldung über den
Fehlerfall informiert wird.

**KOM-LE-A_2177 - Verwenden von SignDocument und EncryptDocument**

Das Clientmodul MUSS für das Signieren und Verschlüsseln der Nachrichten die
Operationen SignDocument und EncryptDocument der Außenschnittstelle des
Konnektors verwenden. **[\<=]**

**KOM-LE-A_2299-01 - Vorgehen bei Signatur und Verschlüsselung einer KOM-LE
Nachricht**

Zur Signatur und Verschlüsselung von KOM-LE Nachrichten MUSS das folgende
Vorgehen umgesetzt werden:

 ---> OL

**[\<=]**

Ein Beispiel einer diesem Profil konformen Nachricht für den Aufbau
des binären CMS-Container ist in [gemSMIME_KOMLE] enthalten. Insbesondere
wird auf die Aufnahme des „Content Headers“ hingewiesen.

**KOM-LE-A_2190 - Übergabe des recipient-emails Attributs beim Signieren**

DasClientmodulMUSSbeimAufrufder OperationSignDocumentdesKonnektorsdas
recipient-emailsAttributalsAufrufparameterin der ASN.1-Form    Attribute
::= SEQUENCE {            attrTypeOBJECT IDENTIFIER,       
    attrValuesSET OFAttributeValue}übergeben.Das ASN.1-Atribut MUSS
DER-kodiertund
base64verpacktimRequest-Element\<SIG:SignDocument\>/\<SIG:SignRequest\>/\<SIG:OptionalInputs\>/\<dss:Properties\>/\<dss:SignedProperties\>/\<dss:Property\>/\<dss:Value\>/\<CMSAttribute\>übergebenwerden.​​ **[\<=]**

Folgend ein Beispiel für den SOAP-Request beim Signieren:

\<?xml version="1.0" encoding="UTF-8" ?\>

\<SIG:SignDocument
xmlns:CERTCMN="http://ws.gematik.de/conn/CertificateServiceCommon/v2.0"
xmlns:CONN="http://ws.gematik.de/conn/ConnectorCommon/v5.0"
xmlns:CCTX="http://ws.gematik.de/conn/ConnectorContext/v2.0"
xmlns:SIG="http://ws.gematik.de/conn/SignatureService/v7.0"
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:dss="urn:oasis:names:tc:dss:1.0:core:schema"\>

  \<CONN:CardHandle\>zDgq6V5EsA\</CONN:CardHandle\>

  \<SIG:Crypt\>RSA\</SIG:Crypt\>

  \<CCTX:Context\>

  \<CONN:MandantId\>Praxis Dr. Mustermann\</CONN:MandantId\>

  \<CONN:ClientSystemId\>Mediakom-PVS-3000\</CONN:ClientSystemId\>

  \<CONN:WorkplaceId\>Arztzimmer2\</CONN:WorkplaceId\>

  \</CCTX:Context\>

  \<SIG:TvMode\>NONE\</SIG:TvMode\>

  \<SIG:SignRequest RequestID="SignRequestNo_001"\>

  \<SIG:OptionalInputs\>

  \<dss:SignatureType\>urn:ietf:rfc:5652\</dss:SignatureType\>

  \<dss:Properties\>

  \<dss:SignedProperties\>

  \<dss:Property\>

  \<dss:Identifier\>RecipientEmailsAttribute\</dss:Identifier\>

  \<dss:Value\>

\<CMSAttribute\>QnNVakJzUjA5RWJHaGpaMGRUUVV4TlVqQnNSMDlFYkdoalowZFRRVXhOUVVGQlVRVU

ZCVVVOQlJVMXRRMXAwZFUxR1VYaEVVemhp\</CMSAttribute\>

  \</dss:Value\>

  \</dss:Property\>

  \</dss:SignedProperties\>

  \</dss:Properties\>

  \<SIG:IncludeEContent\>true\</SIG:IncludeEContent\>

  \</SIG:OptionalInputs\>

  \<SIG:Document ShortText="none"\>

\<dss:Base64Data\>TUlNRS1WZXJzaW9uOiAxLjANCkNvbnRlbnQtdHlwZTogdGV4dC9wbGFpbjsgY2hh

cnNldD1pc28tODg1OS0xNQ0KQ29udGVudC1UcmFuc2Zlci1FbmNvZGluZzogOGJpdA0KRnJvbTogPGhh

bnMubXVzdGVyYXJ6dEBwcmF4aXNBLmRlPg0KVG86IDxldmEubXVzdGVyYXJ6dEBwcmF4aXNCLmRlPg0K

U3ViamVjdDog3GJlcndlaXN1bmcgSHIuIE0uIFBhdGllbnRCDQpEYXRlOiBNb24sIDExIE5vdiAyMDEz

IDE0OjM0OjI3ICswMTAwDQoNClNlaHIgZ2VlaHJ0ZSBGcmF1IEtvbGxlZ2luIERyLiBNdXN0ZXJhcnp0

LA0KDQpoaWVybWl0IPxiZXJ3ZWlzZSBpY2ggSWhuZW4gSHIuIE0uIFBhdGllbnRCIGF1ZiBHcnVuZCAu

Li4uDQoNCk1pdCBmcmV1bmRsaWNoZW4gR3L832VuLA0KDQpEci4gSGFucyBNdXN0ZXJhcnp0\</dss:Ba

se64Data\>

  \</SIG:Document\>

  \<SIG:IncludeRevocationInfo\>false\</SIG:IncludeRevocationInfo\>

  \</SIG:SignRequest\>

\</SIG:SignDocument\>

Da der Versand einer Nachricht an mehrere Empfänger erfolgen kann und das
Clientmodul nicht erkennt, ob alle Empfänger ECC beherrschen, muss das
Signieren einer Nachricht immer mit dem RSA-Schlüssel der SM-B erfolgen.

**KOM-LE-A_2020 - Signieren der Nachricht mit dem Schlüssel Prk.HCI.OSIG**

Das Clientmodul MUSS für das Signieren einer KOM-LE-Nachricht den privaten
Schlüssel PrK.HCI.OSIG.R2048 der SM-B der medizinischen Institution verwenden.
**[\<=]**

**KOM-LE-A_2021 - Verhalten, wenn Nachricht nicht signiert werden kann**

Das Clientmodul MUSSdem MTA das Kommando RSET senden unddas Clientsystem
mitdemAntwortcode„451“benachrichtigen,wenn das Clientmodul die vom
Clientsystem erhaltene Nachricht nicht digitalsignieren kann. **[\<=]**

Die Verschlüsselung erfolgt sowohl für den Sender als auch für alle
Empfänger. Die erforderlichen Verschlüsselungszertifikate C.HCI.ENC für
Institutionen und C.HP.ENC für Leistungserbringer werden im Verzeichnisdienst
zur Verfügung gestellt. Für die Suche nach den passenden Einträgen im
Verzeichnisdienst wird die KOM-LE-E-Mail-Adresse als Suchschlüssel verwendet.
Wenn der Sender bzw. ein Empfänger mehrere Verschlüsslungszertifikate hat
(z.B. wenn dem Empfänger ein neuer HBA  ausgegeben wurde und der alte noch
gültig ist), wird die Nachricht mit allen vorhandenen
Verschlüsselungszertifikaten verschlüsselt.

**KOM-LE-A_2191 - Übergabe des recipient-emails Attributs beim Verschlüsseln**

Das Clientmodul MUSS beim Aufruf der Operation EncryptDocument des Konnektors
das recipient-emails Attribut als Aufrufparameter in der
ASN.1-Form    Attribute ::= SEQUENCE {            attrTypeOBJECT
IDENTIFIER,            attrValuesSET OFAttributeValue}übergeben.
Das ASN.1-Atribut MUSS DER-kodiert und base64 verpackt im
Request-Element\<CRYPT:EncryptDocument\>/\<CRYPT:OptionalInputs\>/\<CRYPT:UnprotectedProperties\>/\<dss:Property\>/\<dss:Value\>/\<CMSAttribulte\>übergeben
werden. **[\<=]**

Folgend ein Beispiel für den SOAP-Request beim Verschlüsseln:

\<?xml version="1.0" encoding="UTF-8" ?\>

\<CRYPT:EncryptDocument
xmlns:CONN="http://ws.gematik.de/conn/ConnectorCommon/v5.0"
xmlns:CCTX="http://ws.gematik.de/conn/ConnectorContext/v2.0"
xmlns:CRYPT="http://ws.gematik.de/conn/EncryptionService/v6.0"
xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xmlns:dss="urn:oasis:names:tc:dss:1.0:core:schema"\>

  \<CCTX:Context\>

  \<CONN:MandantId\>Praxis Dr. Mustermann\</CONN:MandantId\>

  \<CONN:ClientSystemId\>Mediakom-PVS-3000\</CONN:ClientSystemId\>

  \<CONN:WorkplaceId\>Arztzimmer2\</CONN:WorkplaceId\>

  \</CCTX:Context\>

  \<CRYPT:RecipientKeys\>

  \<CRYPT:CertificateOnCard\>

  \<CONN:CardHandle\>zDgq6V5EsA\</CONN:CardHandle\>

  \<CRYPT:Crypt\> ECC \</CRYPT:KeyReference\>

  \</CRYPT:CertificateOnCard\>
\<CRYPT:Certificate\>UjBsR09EbGhjZ0dTQUxNQUFBUUNBRU1tQ1p0dU1GUXhEUzhi\</CRYPT:Certificate\>

  \</CRYPT:RecipientKeys\>

  \<CONN:Document\>

\<dss:Base64Data\>QnNVakJzUjA5RWJHaGpaMGRUUVV4TlVqQnNSMDlFYkdoalowZFRRVXhOUV

VGQlVRVUZCVVVOQlJVMXRRMXAwZFUxR1VYaEVVemhp\</dss:Base64Data\>

  \</CONN:Document\>

  \<CRYPT:OptionalInputs\>

  \<CRYPT:EncryptionType\>urn:ietf:rfc:5652\</CRYPT:EncryptionType\>

  \<CRYPT:UnprotectedProperties\>

  \<dss:Property\>

  \<dss:Identifier\>RecipientEmailsAttribute\</dss:Identifier\>

  \<dss:Value\>

\<CMSAttribute\>QnNVakJzUjA5RWJHaGpaMGRUUVV4TlVqQnNSMDlFYkdoalowZFRRVXhOUVVG

QlVRVUZCVVVOQlJVMXRRMXAwZFUxR1VYaEVVemhp\</CMSAttribute\>

  \</dss:Value\>

  \</dss:Property\>

  \</CRYPT:UnprotectedProperties\>

  \</CRYPT:OptionalInputs\>

\</CRYPT:EncryptDocument\>

Zum Verschlüsseln der Nachricht bezieht das Clientmodul die erforderlichen
Zertifikate aus dem Verzeichnisdienst der TI. Vor der Verwendung der
Zertifikate für die Verschlüsselung muss das Clientmodul prüfen, ob der
verwendete Konnektor die ECC-Kryptographie unterstützt. Ist dies nicht der
Fall, dürfen im Verzeichnisdienst gefundene ECC-Zertifikate nicht für die
Verschlüsselung benutzt werden. Unterstützt der Konnektor ECC, sind sowohl
die RSA- als auch die ECC-Zertifikate für die Verschlüsselung zu verwenden.
Durch diese Herangehensweise wird sichergestellt, dass auch Empfänger, die
noch kein ECC beherrschen, die Nachricht entschlüsseln können. Dieses Prinzip
gilt solange, bis alle TI-Beteiligten ECC beherrschen und somit die
RSA-Zertifikate gesperrt sind.

**A_17464 - ECC-Migration, Prüfung der ECC-Fähigkeit des Konnektors**

Das Clientmodul MUSS über eine Abfrage des Dienstverzeichnisdienstes des
Konnektors prüfen, ob der verwendete Konnektor ECC-Kryptographie unterstützt.
Ein Konnektor unterstützt ECC, wenn die Konnektordienstversionen des
Signaturdienstes mindestens 7.4.1 und des Verschlüsselungsdienstes mindestens
6.1.1 sind. **[\<=]**

**KOM-LE-A_2022 - Verschlüsseln der Nachricht mit den
Verschlüsselungszertifikaten C.HCI.ENC bzw. C.HP.ENC**

Das Clientmodul MUSS vom Clientsystem erhaltene E-Mail-Nachrichten sowohl für
jeden in den RCPT-Kommandos angegeben Empfänger als auch für den Sender aus
demfrombzw.senderHeader-Element der Nachricht mit allen dem Sender bzw.
Empfängern zugeordneten Verschlüsselungszertifikaten (C.HCI.ENC für eine
Institution oder C.HP.ENC für einen Leistungserbringer) verschlüsseln.
**[\<=]**

**A_17472 - ECC-Migration, Keine Verwendung von
ECC-Verschlüsselungszertifikaten bei Konnektoren ohne ECC-Unterstützung**

Verwendet das Clientmodul einen Konnektor, der die ECC-Kryptographie nicht
unterstützt, DARF das Clientmodul ECC-Verschlüsselungszertifikate NICHT für
die Verschlüsselung der Nachricht verwenden. **[\<=]**

**KOM-LE-A_2178 - Kein Versenden an Empfänger mit unterschiedlichen
Telematik-IDs in den Verschlüsselungszertifikaten**

Existieren für einen Empfänger mehrere Verschlüsselungszertifikate mit
unterschiedlichen Telematik-IDs DARF das Clientmodul die Nachricht NICHT an
diesen Empfänger versenden. **[\<=]**

**KOM-LE-A_2192-01 - Fehlernachricht bei Empfänger mit unterschiedlichen
Telematik-IDs in den Verschlüsselungszertifikaten**

Existieren für einen Empfänger mehrere Verschlüsselungszertifikate mit
unterschiedlichen Telematik-IDs MUSS das Clientmodul den Absender der Nachricht
mit einer Fehlernachrichtinformieren. Die Fehlernachricht ist weder zu
signieren noch zu verschlüsseln und entspricht der Delivery Status
Notification gemäß [RFC3461-3464]. **[\<=]**

**KOM-LE-A_2023 - Verschlüsselungszertifikate aus dem Verzeichnisdienst**

Das Clientmodul MUSS in der Lage sein,die Verschlüsselungszertifikate aus
demVerzeichnisdienstder TI mit Hilfe der E-Mail-Adresse zu ermitteln. **[\<=]**

Nachdem die Nachricht erfolgreich signiert wurde und die entsprechenden
Verschlüsselungszertifikate zur Verfügung stehen, führt das Clientmodul die
Verschlüsselung der Nachricht für alle Empfänger bzw. Sender durch. Die
Empfänger werden über die E-Mail-Adressen aus den RCPT-Kommandos
identifiziert. Die Sender werden über die E-Mail-Adressen
imsenderHeader-Element identifiziert. Wenn der Header der Nachricht
keinsenderElement enthält, werden die E-Mail-Adressen des Senders aus
demfromHeader-Element übernommen.

Beim Verschlüsselungsvorgang sind die folgenden Szenarien möglich:

 ---> UL

Die Verschlüsselung erfolgt über die Aufrufe der entsprechenden Operationen
der Außenschnittstelle des Konnektors. Eine detaillierte Beschreibung erfolgt
in Kapitel 3.5.3.

**KOM-LE-A_2024-01 - Information des Absenders über Empfänger, für die nicht
verschlüsselt werden kann**

Kann eine Nachricht auf Grund von fehlenden oder ungültigen Zertifikaten nicht
für alle Empfänger verschlüsselt werden, MUSS das Clientmodul den Absender
mit einer E-Mail über den Fehlerfall informieren. Aus dem Inhalt der
Fehlernachricht müssen alle Empfänger, für die nicht verschlüsselt werden
konnte, hervorgehen. Die Fehlernachricht ist weder zu signieren noch zu
verschlüsseln und entspricht der Delivery Status Notification gemäß
[RFC3461-3464]. Die Originalnachricht darf an die Empfänger, für die nicht
verschlüsselt werden konnte, nicht versendet werden. **[\<=]**

**KOM-LE-A_2025 - Abbruch des Sendens, wenn keine Verschlüsselung möglich**

Das Clientmodul MUSS das Clientsystem mitdemAntwortcode„451“benachrichtigen
und den Senden-VorgangzumMTA mitdem RSET-Kommando abbrechen, wenn das
Clientmodul die vom Clientsystem erhaltene Nachricht für keinen Empfänger
verschlüsseln kann. **[\<=]**

Das KOM-LE-S/MIME-Profil fordert, dass jede entsprechend dem Profil
verschlüsselte Nachricht dasrecipient-emailsAttribut enthält. In diesem
Attribut werden  Zusammenhänge zwischen den für die Verschlüsselung
verwendeten Zertifikaten und den E-Mail-Adressen der Empfänger bzw. des
Senders angegeben. Das Clientmodul befüllt dieses Attribut nur mit den
E-Mail-Adressen für die die Nachricht erfolgreich verschlüsselt werden konnte.

Um die Anzahl von Anfragen an den Verzeichnisdienst und die Bearbeitungszeiten
zu reduzieren werden die für die Verschlüsselung verwendeten Zertifikate für
eine konfigurierbare Zeitdauer im Clientmodul gecached.

**KOM-LE-A_2026 - Cachen von Verschlüsselungszertifikaten**

Das Clientmodul MUSS dasmanipulationssichereCachen von
Verschlüsselungszertifikatenfür eine konfigurierbare Zeitdauerunterstützen. **[\<=]**

Die folgenden Schritte stellen den Schutzvorgang für eine Nachricht im
Clientmodul dar. Die Schritte haben einen beschreibenden und nicht normativen
Charakter. Die Umsetzung kann sich unterscheiden, solange die Anforderungen des
Dokuments erfüllt sind.

 ---> OL

 ---> OL

![Abbildung-9][Abbildung-9]

Abbildung 9 stellt die oben beschriebenen Schritte als Aktivitätsdiagramm dar.

**KOM-LE-A_2027 - Befüllung des recipient-emails Attributs**

Das Clientmodul MUSS für die E-Mail-Adressen,für die die Nachricht erfolgreich
verschlüsselt werden konnte,einen Wert in dasrecipient-emails Attribut
entsprechend dem KOM-LE-S/MIME-Profil einfügen.​​ **[\<=]**

**KOM-LE-A_2028 - Entfernen von Empfängern aus dem Header der Nachricht**

Das Clientmodul MUSS die Empfänger bzw. Senderfür die die Verschlüsselung der
Nachricht nicht durchgeführt werden konnte,
austo,ccbzw.from,senderHeader-Elementen der Nachricht entfernen, um
sicherzustellen, dass die ursprüngliche Nachricht nicht an solche Empfänger
gesendet wird. **[\<=]**

Nachdem die Verschlüsselung durchgeführt wurde, verpackt das Clientmodul das
vom Konnektor verschlüsselte CMS-Objekt in eine äußere Nachricht
entsprechend KOM-LE-S/MIME-Profil und überträgt die geschützte Nachricht an
den MTA.

**KOM-LE-A_2193 - Verpacken des verschlüsselten CMS-Objektes**

Das Clientmodul MUSS das signierte und verschlüsselte CMS-Objekt in eine
äußere Nachricht entsprechend den Anforderungen KOM-LE-A_2097, KOM-LE-A_2098,
KOM-LE-A_2099, KOM-LE-A_2100, KOM-LE-A_2101, KOM-LE-A_2102 des KOM-LE S/MIME
Profils verpacken. **[\<=]**

### 3.3.4.1.2 Bearbeitung einer geschützten KOM-LE-Nachricht

Wenn während eines Abholvorgangs eine KOM-LE-Nachricht nicht im Clientmodul
entschlüsselt werden konnte, wird sie dem Clientsystem als
einemessage/rfc822Einheit mit einem Fehlertext geliefert (siehe das Beispiel im
Kapitel 3.3.4.1.2). Um die Nachricht im Anhang nachträglich zu entschlüsseln
und ihre Signatur prüfen zu können, muss der Nutzer die erhaltene Nachricht
an seine eigene E-Mail-Adresse senden. Beim nächsten Abholvorgang wird diese
Nachricht dann nochmalig im Clientmodul aufbereitet.

**KOM-LE-A_2029 - Aufbereitung einer vom Clientsystem erhaltenen
KOM-LE-S/MIME-Nachricht**

Das Clientmodul MUSS die vom Clientsystem empfangene Nachricht, deren Body
einemessage/rfc822MIME Einheit mit einer dem KOM-LE-Profil entsprechenden
Nachricht (KOM-LE-S/MIME-Nachricht) enthält, in den folgenden Schritten
aufbereiten:

 ---> OL

**[\<=]**

Beispiel für die oben beschriebene Transformation:

MIME-Version: 1.0

Content-Type: multipart/mixed; boundary="unique-boundary-1"

Subject: WG: Signed and encrypted in attachment

Date: Fri, 10 Feb 2012 14:29:21 +0100

From: musterfrau@komle.de

To: musterfrau@komle.de

This is a multi-part message in MIME format.

--unique-boundary-1

Content-Type: text/plain;    charset="iso-8859-1"

Content-Transfer-Encoding: quoted-printable

Der f=FCr die Entschl=FCsselung der Nachricht ben=F6tigte Schl=FCssel =

wurde nicht gefunden. =DCberpr=FCfen Sie ob die entsprechende Karte =

gesteckt ist und leiten Sie diese Nachricht an Ihre eigene Email Adresse =

(musterfrau@komle.de) weiter. Beim n=E4chsten Abholen der Nachricht =

wird der Entschl=FCsselungsvorgang wiederholt.

--unique-boundary-1

Content-Type: message/rfc822    

X-KOM-LE-Version: 1.0

MIME-Version: 1.0

Content-Type: application/pkcs7-mime; smime-type=enveloped-data;name="smime.p7m";

Content-Transfer-Encoding: base64

Content-Disposition: attachment;    filename="smime.p7m"

Subject: KOM-LE Nachricht

Date: Fri, 9 Feb 2012 12:07:17 +0100

From: mustermann@komle.de

To: musterfrau@komle.de

Cc: mustermann2@komle.de

\<verschlüsselter Inhalt\>

--unique-boundary-1

Im Clientmodul wird diese Nachricht entsprechend der Anforderung [KOM-LE-A_2029]
aufbereitet:

X-KOM-LE-Version: 1.0

MIME-Version: 1.0

Content-Type: application/pkcs7-mime;

smime-type=enveloped-data; name="smime.p7m"

Content-Transfer-Encoding: base64

Content-Disposition: attachment;    filename="smime.p7m"

Subject: KOM-LE Nachricht

Date: Fri, 9 Feb 2012 12:07:17 +0100

From: mustermann@komle.de

To:musterfrau@komle.de

Cc: mustermann2@komle.de

\<Verschlüsselter Inhalt\>

### 3.3.5 Beispiele

Das Clientsystem (C) verbindet sich mit dem Clientmodul (M) und sendet dem
MTA-Server (S) eine Nachricht (im Beispiel werden auch die Zustände des
Clientmoduls dargestellt):

C:     \<das Clientsystem öffnet eine mit TLS geschützte Verbindung mit
dem Clientmodul\>

M:    \<CONNECT Zustand\>

M-\>C: 220 KOM-LE Clientmodul ESMTP

C-\>M: EHLO [192.168.1.5]

M-\>C: 250 – SIZE 35882577

M-\>C: 250 - AUTH LOGIN PLAIN

M-\>C: 250 – 8BITMIME

M-\>C: 250 ENCHANCEDSTATUSCODES

C-\>M: AUTH LOGIN

M-\>C: 334 VXNlcm5hbWU6

C-\>M: bXVzdGVybWFubkBrb21sZS5kZSNtYWlsLmtvbWxlLmRlOjU4NyMxI0tPTS1MRSM3==

M-\>C: 334 UGFzc3dvcmQ6

C-\>M: lkajsdfvlj

M:    \<das Clientmodul öffnet eine mit TLS geschützte Verbindung mit dem
MTA\>

S-\>M: 220 SMTP Server ESMTP

M-\>S: EHLO [192.168.1.5]

S-\>M: 250 – SIZE 35882577

S-\>M: 250 - AUTH LOGIN PLAIN

S-\>M: 250 – 8BITMIME

S-\>M: 250 ENCHANCEDSTATUSCODES

M-\>S: AUTH LOGIN

S-\>M: 334 VXNlcm5hbWU6

M-\>S: bXVzdGVybWFubkBrb21sZS5kZQ==

S-\>M: 334 UGFzc3dvcmQ6

M-\>S: lkajsdfvlj

S-\>M: 235 2.7.0 Authentication successful

M:     \<PROXY Zustand\>

M-\>C: 235 2.7.0 Authentication successful

C-\>M: MAIL FROM:\<mustermann@komle.de\>

M-\>S: MAIL FROM:\<mustermann@komle.de\>

S-\>M: 250 OK

M-\>C: 250 OK

C-\>M: RCPT TO:\<musterfrau@komle.de\>

M-\>S: RCPT TO:\<musterfrau@komle.de\>

S-\>M: 250 OK

M-\>C: 250 OK

C-\>M: DATA

M-\>C: 354 Start mail input; end with \<CRLF\>.\<CRLF\>

M:    \<PROCESS Zustand\>

C-\>M: From: "Max Mustermann" \<mustermann@komle.de\>

C-\>M: To: "Erika Musterfrau" \<musterfrau@komle.de\>

C-\>M: Subject: Biopsie Ergebnisse für Frau S. Muster

C-\>M: Date: Mon, 30 Jan 2012 13:14:12 +0100

C-\>M:

C-\>M: \<Inhalt der KOM-LE Nachricht\>

C-\>M: .

M:    \<Die Nachricht wird im Clientmodul aufbereitet\>

M-\>S: DATA

S-\>M: 354 Start mail input; end with \<CRLF\>.\<CRLF\>

M-\>S: X-KOM-LE-Version: 1.0

M-\>S: MIME-Version: 1.0

M-\>S: From: "Max Mustermann" \<mustermann@komle.de\>

M-\>S: To: "Erika Musterfrau" \<musterfrau@komle.de\>

M-\>S: Subject: KOM-LE Nachricht

M-\>S: Date: Mon, 30 Jan 2012 13:14:12 +0100

M-\>S: Content-Type: application/pkcs7-mime;
mime-type=enveloped-data;name=smime.p7m

M-\>S: Content-Transfer-Encoding: base64

M-\>S: Content-Disposition: attachment; filename=smime.p7m

M-\>S:

M-\>S: \<verschlüsselter Inhalt der KOM-LE Nachricht\>

M-\>S: .

M:    \<PROXY Zustand\>

S-\>M: 250 Ok

M-\>C: 250 Ok

C-\>M: QUIT

M-\>S: QUIT

S-\>M: 221 Bye

S:    \<der MTA schließt die Verbindung mit dem Clientmodul\>

M-\>C: 221 Bye

M:    \<das Clientmodul schließt die Verbindung mit dem Clientsystem\>

Das Senden einer Nachricht wird abgebrochen, weil die Anmeldedaten keine
MTA-Adresse erhalten:

C:     \<das Clientsystem öffnet eine mit TLS geschützte Verbindung mit
dem Clientmodul\>

M:     \<CONNECT Zustand\>

M-\>C: 220 KOM-LE Clientmodul ESMTP

C-\>M: EHLO [192.168.1.5]

M-\>C: 250 – SIZE 35882577

M-\>C: 250 - AUTH LOGIN PLAIN

M-\>C: 250 – 8BITMIME

M-\>C: 250 ENCHANCEDSTATUSCODES

C-\>M: AUTH LOGIN

M-\>C: 334 VXNlcm5hbWU6

C-\>M: bXVzdGVybWFubkBrb21sZS5kZQ==

M-\>C: 334 UGFzc3dvcmQ6

C-\>M: lkajsdfvlj

M-\>C: 501 5.5.4 Benutzername muss die Adresse und die Portnummer des SMTP
Servers

Enthalten

M:    \<das Clientmodul schließt die Verbindung mit dem Clientsystem\>

Das Senden einer Nachricht wird abgebrochen, weil Verschlüsselungszertifikate
weder für mustermann@komle.de noch für musterfrau@komle.de gefunden werden
konnten:

...

C-\>M: DATA

M-\>C: 354 Start mail input; end with \<CRLF\>.\<CRLF\>

M:    \<PROCESS Zustand\>

C-\>M: From: "Max Mustermann" \<mustermann@komle.de\>

C-\>M: To: "Erika Musterfrau" \<musterfrau@komle.de\>

C-\>M: Subject: Biopsie Ergebnisse für Frau S. Muster

C-\>M: Date: Mon, 30 Jan 2012 13:14:12 +0100

C-\>M:

C-\>M: \<Inhalt der KOM-LE Nachricht\>

C-\>M: .

M:    \<Das Clientmodul konnte die Verschlüsselungszertifikate nicht
finden\>

M-\>C: 451 Die Nachricht konnte nicht verschlüsselt werden, weil

Verschlüsselungszertifikate für mustermann@komle.de,musterfrau@komle.denicht
zugänglich sind

M-\>S: RSET

S-\>M: 250 2.0.0 Flushed

C-\>M: QUIT

M-\>S: QUIT

S-\>M: 221 Bye

S:    \<der MTA schließt die Verbindung mit dem Clientmodul\>

M-\>C: 221 Bye

M:    \<das Clientmodul schließt die Verbindung mit dem Clientsystem\>

Das Senden einer Nachricht wird abgebrochen, weil die Verbindung zwischen dem
Clientmodul und dem Clientsystem abgebrochen wird:

...

M-\>C: 235 2.7.0 Authentifizierung erfolgreich

C-\>M: MAIL FROM:\<mustermann@komle.de\>

M-\>S: MAIL FROM:\<mustermann@komle.de\>

S-\>M: 250 OK

M-\>C: 250 OK

C-\>M: RCPT TO:\<musterfrau@komle.de\>

C:     \<das Clientsystem bricht die Verbindung mit dem Clientmodul ab\>

M-\>S: RCPT TO:\<musterfrau@komle.de\>

M:     \<das Clientmodul schließt die Verbindung mit dem MTA\>

### 3.4 Empfangen von Nachrichten

In diesem Kapitel werden Anforderungen an das Clientmodul formuliert, die für
den Anwendungsfall „KOM-LE_AF_2 Nachricht empfangen“ [gemSysL_KOMLE]
spezifisch sind.

### 3.4.1 Übersicht

Beim Empfangen von KOM-LE-Nachrichten sorgt das Clientmodul dafür, dass für
abgeholte Nachrichten vor der Weiterleitung an das Clientsystem der
Vertraulichkeitsschutz aufgehoben und die Integrität geprüft werden.
Abbildung 10 stellt die Interaktionen zwischen den am Abholen von
KOM-LE-Nachrichten beteiligten Komponenten dar. Aus Sicht des Clientsystems
agiert das Clientmodul als POP3-Server, und aus Sicht des POP3-Servers des
Fachdienstes (weiter im Text auch als POP3-Server bezeichnet) agiert das
Clientmodul als E-Mail-Client. Für Funktionen wie Datentransport,
kryptographische Operationen, Kommunikation mit dem Verzeichnisdienst verwendet
das Clientmodul entsprechende Dienste der TI-Plattform.

![Abbildung-10][Abbildung-10]

Beim Abholen von Nachrichten findet die Kommunikation zwischen dem Clientsystem,
dem Clientmodul und dem POP3-Server über POP3 statt. Das Clientmodul fungiert
als POP3-Proxy, der das Clientsystem mit dem POP3-Server verbindet, die
Entschlüsselung und Signaturprüfung für die abgeholten Nachrichten
durchführt und die entschlüsselten Nachrichten an das Clientsystem liefert.
Die Ergebnisse der Signaturprüfung werden dem Nutzer als Vermerk, der in den
Inhalt der Nachricht integriert wird, sowie als ein detaillierter Bericht in
Form einer angehängten PDF-Datei mitgeteilt. Die Integritätsprüfung einer
empfangenen KOM-LE-Mail wird im Kapitel 3.4.4.2.2 beschrieben.

Dieses Dokument spezifiziert nicht alle Schritte und Einzelheiten der
POP3-Kommunikation zwischen dem Clientsystem, dem Clientmodul und dem
POP3-Server. Es setzt voraus, dass POP3 und dessen Erweiterungen dem Leser
bekannt sind.

Das Clientmodul benachrichtigt den Nutzer über Fehler, die während der
Nachrichtenübertragung zwischen dem POP3-Server und dem Clientmodul oder bei
der Bearbeitung der Nachrichten im Clientmodul auftreten. In den meisten
Fällen wird das Clientsystem durch POP3-Meldungen über Fehler informiert. Das
Clientsystem entscheidet anschließend über das weitere Vorgehen (weitermachen
oder abbrechen und den Nutzer über den Fehler informieren).

Beispiel: Verwendet das Clientsystem beim Empfangen von Nachrichten falsche
Anmeldungsdaten, bekommt es vom Clientmodul „-ERR Der Nutzer konnte nicht
authentifiziert werden“ als Antwort auf sein PASS-Kommando.

Fehler, die bei der Entschlüsselung oder Signaturprüfung einer Nachricht
auftreten, werden anders behandelt:

 ---> UL

Das Verhalten des Clientmoduls beim Abholen von Nachrichten kann mit Hilfe der
in Abbildung 11 dargestellten Zustandsmuster beschrieben werden und haben
illustrativen und nicht normativen Charakter. Die Umsetzung kann sich
unterscheiden, solange das Ergebnis das gleiche ist. Die den Zuständen
zugeordnete Anforderungen sind normativ, können aber außerhalb des Kontexts
dieser Zustände umgesetzt werden.

![Abbildung-11][Abbildung-11]

Das Clientmodul lauscht auf einem TCP-Port und wartet bis ein Clientsystem mit
ihm eine Verbindung aufbaut. Sobald dies passiert, geht das Clientmodul in den
CONNECT-Zustand über und betrachtet die POP3-Verbindung als geöffnet. Die
POP3-Verbindung zwischen dem Clientmodul und dem Clientsystem muss mit TLS
erfolgen.

Im CONNECT-Zustand führt das Clientmodul einen POP3-Dialog mit dem
Clientsystem, in dem ihm die Anmeldedaten des Nutzers sowie die Adresse und die
Portnummer des POP3-Servers mitgeteilt werden. Sobald die Anmeldedaten und die
Adresse des POP3-Servers übermittelt sind, baut das Clientmodul eine über TLS
geschützte POP3-Verbindung mit dem POP3-Server auf, authentifiziert sich und
geht in den PROXY-Zustand über.

Im PROXY-Zustand leitet das Clientmodul POP3-Meldungen und POP3-Antwortcodes
zwischen dem Clientsystem und dem POP3-Server hin und her, bis das Clientsystem
mit dem RETR-Kommando das Abholen einer Nachricht initiiert. Sobald der
POP3-Server beginnt, Inhalte einer Nachricht zu übertragen, geht das
Clientmodul in den PROCESS-Zustand über.

Im PROCESS-Zustand wird die Nachricht entschlüsselt, ihre Signatur geprüft und
die aufbereitete Nachricht dem Clientsystem übermittelt. Sobald die Nachricht
erfolgreich an das Clientsystem übermittelt wurde oder im Fehlerfall, geht das
Clientmodul in den PROXY-Zustand zurück.

### 3.4.2 CONNECT-Zustand

Sobald die TCP-Verbindung zwischen dem Clientsystem und dem Clientmodul
aufgebaut wurde, geht das Clientmodul in den CONNECT-Zustand über.

### 3.4.2.1 Initialisierung

Nachdem die POP3-Verbindung zwischen dem Clientsystem und dem Clientmodul
aufgebaut wurde, sendet das Clientmodul dem Clientsystem die POP3-Begrüßung.

Beispiel einer solchen Begrüßung:+OK KOM-LE Clientmodul POP3

Das Clientmodul führt einen POP3-Dialog mit dem Clientsystem bis ihm das
Clientsystem die Adresse und die Portnummer des POP3-Servers als einen Teil des
während des Authentifizierungsverfahrens übertragenen Benutzernamens mitteilt.

Tabelle Tab_POP3_Ant_Init beschreibt die Antworten, die das Clientmodul dem
Clientsystem im CONNECT-Zustand sendet.

<table><tr><th>
Clientsystem -\> Clientmodul

</th><th>
Clientmodul -\> Clientsystem

</th></tr><tr><td>
CAPA

</td><td>
“+OK” Antwortcode mit folgenden CAPA Kennworten:

TOP

USER

SASL PLAIN

UIDL

</td></tr><tr><td>
USER, AUTH

</td><td>
Anmeldungsdaten erhalten und Verbindungsaufbau mit dem POP3-Server fortsetzen
(siehe Kapitel 3.3.2.2)

</td></tr><tr><td>
QUIT

</td><td>
„+ OK“ Antwortcode senden und die Verbindung mit dem Clientsystem schließen

</td></tr><tr><td>
Andere Meldungen

</td><td>
„-ERR“ Antwortcode

</td></tr></table>

**KOM-LE-A_2030 - POP3-Dialog zur Authentifizierung**

Das Clientmodul MUSS, nachdem die POP3-Verbindung zwischen dem Clientsystemund
dem Clientmodul aufgebaut wurdeund bis zudem Punkt an dem das Clientsystem die
Bestätigungdes Erfolgs oder Misserfolgs seiner Authentifizierung erwartet,
einen POP3-Dialog entsprechend Tabelle Tab_POP3_Ant_Init mit dem Clientsystem
führen. **[\<=]**

### 3.4.2.2 Verbindungsaufbau mit dem POP3-Server

Das Clientmodul kann die Verbindung mit dem POP3-Server nur dann aufbauen, wenn
ihm das Clientsystem die Adresse des POP3-Servers und die Portnummer des
POP3-Dienstes übermittelt. Das Clientmodul erwartet, dass der Domain Name oder
die IP-Adresse und die Portnummer während des Authentifizierungsverfahrens als
Teil des Benutzernamens übergeben werden.

Das Clientmodul führt das Authentifizierungsverfahren mit dem Clientsystem bis
zu dem Punkt, an dem es mit dem entsprechenden Antwortcode die
Authentifizierung akzeptieren oder ablehnen muss. Das Clientmodul allein kann
das Clientsystem nicht authentifizieren. Die Authentizität der Zugangsdaten
kann nur vom POP3-Server überprüft werden. Dazu authentisiert sich das
Clientmodul im Auftrag vom Clientsystem gegenüber dem POP3-Server.

Die Server Adresse und die Portnummer des POP3-Dienstes sind als Teil des
POP3-Benutzernamens vom Clientsystem zu übergeben. Sie sind vom eigentlichen
Benutzernamen durch das Zeichen ’#’ getrennt und als adresse:port String
formatiert.

Um mit SM-B/HBA über den Konnektor kommunizieren zu können, werden dem
KOM-LE-Clientmodul ebenfalls als Teil des POP3-Benutzernamens, die

 ---> UL

übergeben (siehe Kapitel 3.5 und [gemSpec_Kon] für Details zu MandantId,
ClientSystemId, WorkplaceId und UserId). Der optionale Parameter KonnektorId,
als Bestandteil des Aufrufkontext für SM-B, ermöglicht die Unterstützung von
Multikonnektor-Umgebungen. Die Parameter entsprechen denen des aufrufenden
Clients und werden voneinander durch das Zeichen ’#’ getrennt. Der
Parameter UserId wird nur für den Zugriff auf einen HBA benötigt und kann
entfallen wenn kein HBA erforderlich ist (z.B. wenn die Entschlüsselung der
empfangenen Nachrichten ausschließlich mit SM-B durchgeführt wird). Der
optionale Parameter KonnektorId kann ebenfalls entfallen, wenn das Clientmodul
nicht mit mehreren Konnektoren kommunizieren muss.

Die Reihenfolge der Parameter entspricht dem folgenden Muster und hat der den
Parametern vorangestellten Nummer in der Reihenfolge zu entsprechen:

[0] Benutzername[1] \<Domain Adresse des POP3-Servers\>:\<Port\>[2] MandantId[3]
ClientsystemId[4] WorkplaceId— \<optional\> —[5] UserId[6] KonnektorId[...]

![Abbildung-12][Abbildung-12]

Beispiel:

Bei folgenden Informationen

 ---> UL

erwartet das Clientmodul, dass das Clientsystem ihm den folgenden
POP3-Benutzernamen als String überträgt:

erik.mustermann@hrst_domain.kim.telematik#hrst_domain.kim.telematik:995#1#KOM_LE#7#13#Konn_1

Enthält der POP3-Benutzername nicht alle erforderlichen Parameter, bricht das
KOM-LE-Clientmodul den Empfangsvorgang mit dem -ERR Antwortcode ab. Wenn der
erhaltene POP3-Benutzername zusätzliche optionale durch das Zeichen ‚#’
abgegrenzte Parameter enthält (z.B. #UserId#KonnektorId), dann müssen diese
Parameter vom Clientmodul ausgewertet werden und der Empfangsvorgang wird
fortgesetzt.

Es gibt mehrere Benutzername/Password-basierte
POP3-Authentifizierungsmechanismen:

 ---> UL

Die auf Challenge-Response basierten Mechanismen machen das Extrahieren des
Passworts aus der Challenge-basierten Response für das Clientmodul
unpraktikabel. Deshalb werden für die
Clientsystem-Clientmodul-Authentifizierung die PLAIN oder USER/PASS-Mechanismen
verwendet.

Sobald das Clientmodul die Anmeldedaten des Nutzers erhält, extrahiert es die
Adresse des POP3-Servers und die Portnummer des POP3-Dienstes aus dem
Nutzernamen und baut damit die Verbindung zum POP3-Server auf. Die Verbindung
wird über TLS geschützt. Details zum Aufbau der TLS-Verbindung werden in
Kapitel 4.1.3 beschrieben.

Tabelle Tab_POP3_Verbindung enthält POP3-Antwortcodes, die das Clientmodul dem
Clientsystem bei einem Verbindungsaufbau mit dem POP3-Server übermittelt.

<table><tr><th>
Bedingung

</th><th>
POP3 Antwortcode

(Clientmodul -\> Clientsystem)

</th></tr><tr><td>
Das Clientsystem hat sich erfolgreich gegenüber dem POP3-Server mit den vom
Clientsystem erhaltenen Anmeldungsdaten authentifiziert.

</td><td>
+OK

</td></tr><tr><td>
Das Clientsystem verwendet für die POP3-Authentifizierung einen anderen
Mechanismus als USER/PASS oder PLAIN.

</td><td>
-ERR

</td></tr><tr><td>
Die vom Clientsystem erhaltene POP3-Authentifizierungsidentität ist nicht
vollständig oder  falsch formatiert (POP3 Server Adresse, MandantId,
ClientSystemId, WorkplaceID oder Platzhalter fehlt – siehe Abbildung
"Abb_POP3_Nutzer_Name Format des POP3- Benutzernamens").

</td><td>
-ERR

</td></tr><tr><td>
Bei Übergabe der Parameter für den Aufrufkontext für SM-B (MandantID,
ClientSystemID oder WorkplaceID) antwortet der Konnektor mit einem SOAP Fault
(Code: 4004 - 4006)

</td><td>
-ERR

</td></tr><tr><td>
Die Verbindung zwischen dem Clientmodul und dem POP3-Server kann nicht aufgebaut
werden.

</td><td>
-ERR

</td></tr><tr><td>
Die Authentifizierung gegenüber dem MTA schlägt fehl.

</td><td>
-ERR

</td></tr></table>

**KOM-LE-A_2037-01 - Antwortcodes des Verbindungsaufbaus mit dem POP3-Server**

Das Clientmodul MUSS das Clientsystem über das Ergebnis des Verbindungsaufbaus
mit dem POP3-Server mit den in der Tabelle Tab_POP3_Verbindung beschriebenen
POP3-Antwortcodes informieren. **[\<=]**

Die Verbindungen zwischen dem Clientsystem und dem Clientmodul sowie zwischen
dem Clientmodul und dem POP3-Server bleiben solange offen, bis eine der beiden
geschlossen oder abgebrochen wird. Sobald eine der beiden Verbindungen
geschlossen oder abgebrochen wird, übermittelt das Clientmodul die
ausstehenden POP3-Meldungen und schließt die andere Verbindung. Die
POP3-Sitzung wird damit für den POP3-Server, das Clientsystem und das
Clientmodul beendet.

Beispiel:

Nachdem das Clientmodul das QUIT-Kommando vom Clientsystem erhält und dem
POP3-Server übermittelt, bestätigt der POP3-Server das Ankommen des Kommandos
mit dem Antwortcode „+OK“ und schließt die Verbindung mit dem Clientmodul.
Das Clientmodul übermittelt den Antwortcode „+OK“ an das Clientsystem und
schließt die Verbindung mit dem Clientsystem.

**KOM-LE-A_2031 - Unterstützung der Serverteile der Mechanismen USER/PASS und
SASL PLAIN**

Das Clientmodul MUSS fürdiePOP3-Authentifizierung des Clientsystems die
ServerteilederUSER/PASS und SASL-PLAIN-Mechanismen unterstützen. **[\<=]**

**KOM-LE-A_2032 - Extrahieren der Zugangsdaten des POP3-Servers und des
Kartenaufrufkontextes**

Das Clientmodul MUSS die Zugangsdaten für den POP3-Server und den
Kartenaufrufcontext aus dem vom Clientsystem erhaltenen POP3-Benutzernamen
entsprechend AbbildungAbb_POP3_Nutzer_Nameextrahieren. **[\<=]**

**A_21517 - POP3 - Extrahieren der KonnektorId für Multikonnekor-Umgebungen**

Das Clientmodul MUSS, wenn der Parameter KonnektorId im erhaltenen
POP3-Benutzernamen erhalten ist, diesen extrahieren und auswerten, um während
der POP3-Verbindung, mit einem definierten Konnektor, Nachrichten
weiterzuleiten. **[\<=]**

Der Parameter KonnektorId ist eine Referenz auf eine URI oder eine IP-Adresse
eines Konnektors, um in einer Umgebung mit mehreren Konnektoren einen
bestimmten Konnektor ansprechen zu können. Diese kann beispielweise in einer
Konfigurations-Datei im Clientmodul hinterlegt sein.

**A_21518-02 - Überprüfung des POP3-Benutzernames**

Das Clientmodul MUSS die übergebene POP3-Benutzername-Zeichenkette auf
Vollständigkeit überprüfen. Werden optionale Bestandteile des
POP3-Benutzernamens nicht genutzt, MUSS sichergestellt werden das später
folgende optionale Bestandteile in ihrer vorgegebenen Position platziert
werden. Als Platzhalter ist in so einem Fall "*" zu verwenden. Wenn die
POP3-Benutzername-Zeichenkette nicht vollständig ist, MUSS das Clientmodul den
POP3 Fehlercode gemäß Tabelle "Tab_POP3_Verbindung Antwortcodes für
POP3-Server-Verbindungsaufbau" an das Clientsystem senden und den Vorgang
abbrechen. **[\<=]**

Beispiel einer vollständigen POP3-Benutzername-Zeichenkette:

 ---> UL

erik.mustermann@hrst_domain.kim.telematik#hrst_domain.kim.telematik:995#1#KOM_LE#7

 ---> UL

erik.mustermann@hrst_domain.kim.telematik#hrst_domain.kim.telematik:995#1#KOM_LE#7#13

 ---> UL

erik.mustermann@hrst_domain.kim.telematik#hrst_domain.kim.telematik:995#1#KOM_LE#7#*#Konn_1

 ---> UL

erik.mustermann@hrst_domain.kim.telematik#hrst_domain.kim.telematik:995#1#KOM_LE#7#13#Konn_1

Erfolgt die Einbindung von KIM in ein bestehendes Mail-System, kann ein
übergebener Delimiter ":" zwischen dem Serveranteil und dem Port (z.
B.hrst_domain.kim.telematik:995) des POP3-Benutzernamens zu Fehlern bei der
Interpretation im Bestandsystem führen. Es werden daher weitere Delimiter im
Benutzernamen unterstützt, sofern die Funktionalität gemäß der
Bestandsanforderungen zu den Benutzernamen, in semantischer Abgrenzung,
uneingeschränkt erhalten bleiben. Es gilt, dass die Bestandteile des
POP3-Benutzernames in ihrem semantischen Bezug gemäß [RFC1123, RFC2822]
einhalten müssen.

**KOM-LE-A_2033-01 - Verbindungsaufbau mit POP3-Server über Adresse und
Portnummer**

Das Clientmodul MUSS die POP3-Adresse und die Portnummer, die aus dem vom
Clientsystem erhaltenen POP3-Benutzernamen extrahiert wurden (siehe Abbildung
Abb_POP3_Nutzer_Name), für den Verbindungsaufbau mit dem POP3-Server
verwenden. **[\<=]**

**KOM-LE-A_2034 - Authentifizierung gegenüber POP3-Server mit Benutzernamen und
Passwort**

Das Clientmodul MUSS den Benutzernamen, der aus dem vom Clientsystem erhaltenen
POP3-Benutzernamen extrahiert wurde(sieheAbbildung Abb_POP3_Nutzer_Name)sowie
das vom Clientsystem erhaltene Passwort für die Authentifizierung gegenüber
den POP3-Server verwenden. **[\<=]**

**KOM-LE-A_2035 - Unterstützung der Clientteile der Mechanismen USER/PASS und
SASL PLAIN**

Das Clientmodul MUSS für das Authentifizierungsverfahren mit dem POP3-Server
den ClientteilderUSER/PASS und SASL-PLAIN-Mechanismen für
POP3-Authentifizierung unterstützen. **[\<=]**

**KOM-LE-A_2036 - Authentifizierung gegenüber POP3-Server mit anderen
Mechanismen als USER/PASS oder SASL PLAIN**

Das Clientmodul KANN für das Authentifizierungsverfahren mit dem
POP3-Serverandere als USER/PASS oder SASL-PLAIN-Authentifizierungsmechanismen
benutzen. **[\<=]**

**KOM-LE-A_2038 - Schließen der POP3-Verbindung mit dem Clientsystem**

Das Clientmodul MUSS die POP3-Verbindung mit dem Clientsystem aufrechterhalten.
Das Schließen der Verbindung ist nur bei folgenden Ausnahmen zulässig:

 ---> UL

**[\<=]**

**KOM-LE-A_2039 - Schließen der POP3-Verbindung mit dem POP3-Server**

Das Clientmodul MUSS die POP3-Verbindung mit dem POP3-Server aufrechterhalten.
Das Schließen der Verbindung ist nur zulässig:

 ---> UL

**[\<=]**

Nachdem das Clientsystem sich gegenüber dem POP3-Server erfolgreich
authentifiziert hat, geht das Clientmodul in den PROXY-Zustand über.
Anderenfalls bleibt das Clientmodul im CONNECT-Zustand.

### 3.4.3 PROXY-Zustand

Im PROXY-Zustand vermittelt das Clientmodul POP3-Meldungen und Antwortcodes
zwischen dem Clientsystem und dem POP3-Server. Das Clientmodul bleibt in diesem
Zustand bis das Clientsystem das RETR-Kommando sendet und der POP3-Server das
Erhalten dieses Kommandos mit dem Antwortcode „+OK“ bestätigt. Das
Clientmodul leitet den Antwortcode „+OK“ an das Clientsystem weiter und
geht in den PROCESS-Zustand über.

In diesem Zustand kann das Clientmodul vom Clientsystem das TOP-Kommando
erhalten, das \<MsgID\>und \<N\>als Parameter hat. Es fordert den POP3-Server
zur Übertragung des Headers und von \<N\>Nachrichtenzeilen der durch
\<MsgID\>identifizierten Nachricht auf. Um sicherzustellen, dass das
Clientmodul keine Teile einer verschlüsselten S/MIME-Nachricht bekommt, wird
der Parameter \<N\>vom Clientmodul immer auf 0 gesetzt.

**KOM-LE-A_2040 - Übermittlung von POP3-Kommandos und -Meldungen nach
erfolgreicher Authentifizierung**

Das Clientmodul MUSS, nachdem das Authentifizierungsverfahren mit dem
Clientsystem erfolgreich beendet ist, alle vom Clientsystem
erhaltenenPOP3-Kommandos, mit Ausnahmedes TOP-Kommandos, bzw. alle vom
POP3-Server erhaltenen POP3-Meldungen, mit Ausnahme von Inhalten vom
E-Mail-Nachrichten, ohne jegliche Veränderungen demPOP3-Server bzw. dem
Clientsystem übermitteln. **[\<=]**

**KOM-LE-A_2041 - Setzen des Parameters 
     
       des TOP-Kommandos auf
Null
     **

Das Clientmodul MUSS, wennesvom ClientsystemeinTOP \<MsgID\>
\<N\>Kommandomiteinemvon Nullabweichenden Parameter\<N\>erhält, den Wert des
Parameters\<N\>auf Null setzen, bevor das Kommando dem POP3-Server übermittelt
wird. **[\<=]**

Hinweis für Implementierung

Wegen eines Thunderbird bugs:

Das getrennte Laden von Header und Body ist in Thunderbird nicht korrekt
implementiert. Möglicher Bugfix im CM: Bei TOP 0 den Msg Header ändern: MIME
Element(MIME-Version: 1.0) aus Header entfernen, dann klappt das nachladen.

### 3.4.4 PROCESS-Zustand

Im PROZESS-Zustand nimmt das Clientmodul die Inhalte der vom POP3-Server
abgerufenen Nachricht entgegen, entschlüsselt die Nachricht, prüft deren
Integrität, fügt einen Vermerk sowie einen PDF-Anhang mit dem Ergebnis der
Signaturprüfung in die Nachricht ein und leitet die aufbereitete Nachricht dem
Clientsystem weiter. Im Erfolgsfall wird das Clientsystem über das
erfolgreiche Abholen der Nachricht informiert. Im Fehlerfall wird das
Clientsystem mit dem entsprechenden Antwortcode über den Fehler informiert.

### 3.4.4.1 Empfang und Weiterleitung einer Nachricht

Nachdem der POP3-Server das Erhalten des RETR-Kommandos mit dem Antwortcode
„+OK“ bestätigt, erwartet das Clientmodul, dass der POP3-Server mit der
Übertragung der Nachricht beginnt. Die Inhalte der Nachricht werden im
Clientmodul zwischengespeichert. Wenn die Nachricht eine entsprechend dem
KOM-LE-S/MIME-Profil geschützte Nachricht ist, bereitet das Clientmodul die
erhaltene Nachricht auf und übermittelt sie anschließend dem Clientsystem.
Wenn es keine KOM-LE-S/MIME-Nachricht ist, wird sie ohne jegliche Änderungen
dem Clientsystem übermittelt.

Nachdem die Nachricht dem Clientsystem übermittelt wurde, löscht das
Clientmodul die zwischengespeicherten Nachrichtinhalte und geht in den
PROXY-Zustand zurück.

**A_21236 - Headerfeld „Return-Path“ der äußeren Nachricht**

Das Clientmodul MUSS, nach dem Empfang der E-Mail vom Fachdienst, das im Header
der äußeren Nachricht enthaltene Header-ElementReturn-Path,vor der
Weiterleitung an den E-Mail-Client des Empfängers, in den Header der
entschlüsselten Mail an den Empfänger übernehmen. **[\<=]**

### 3.4.4.2 Aufbereitung einer Nachricht

Das Clientmodul soll zwischen den KOM-LE S/MIME und anderen Nachrichten
unterscheiden. Wenn die angekommene Nachricht eine KOM-LE-S/MIME-Nachricht ist,
entschlüsselt das Clientmodul ihre Inhalte und führt die Prüfung ihrer
Signatur durch. Die KOM-LE-S/MIME-Nachrichten sind anhand
desX-KOM-LE-VersionHeader-Elements erkennbar. Wenn die ankommende Nachricht
keine KOM-LE-S/MIME-Nachricht ist (z.B. nicht signierte und nicht
verschlüsselte Fehlernachrichten), soll sie ohne weitere Veränderungen dem
Clientsystem übermittelt werden.

**A_21390 - Prüfung auf eine KOM-LE-S/MIME-Nachricht**

Zur Unterscheidung einer KOM-LE-S/MIME-Nachricht von einer anderen Nachricht
MUSS das Clientmodul prüfen, ob das Header-ElementX-KOM-LE-Versionin der
äußeren Nachricht vorhanden ist. Wenn das Header-Element nicht gesetzt ist,
MUSS das Clientmodul die Nachricht ohne weitere Veränderungen an das
Clientsystem übermitteln. Wenn das Header-Element gesetzt ist, MUSS das
Clientmodul die Nachricht wie eine KOM-LE-S/MIME-Nachricht behandeln. **[\<=]**

**A_21391-02 - Auswertung des X-KOM-LE-Version Header Elements**

Das Clientmodul MUSS prüfen, ob das Header-Element X-KOM-LE-Version in der
äußeren Nachricht eine vom Clientmodul unterstützte Version enthält. Wenn
das nicht der Fall ist, MUSS das Clientmodul den Nutzer mit einer E-Mail über
den Fehlerfall informieren. Die Fehlernachricht entspricht einer
multipart/mixed MIME-Nachricht. Die Originalnachricht MUSS als message/rfc822
MIME-Einheit in die Fehlernachricht eingepackt werden. Zusätzlich muss diese
neue multipart/mixed MIME-Nachricht eine text/plain MIME-Einheit mit dem
Fehlertext, "Das verwendete Clientmodul unterstützt die in der empfangenen
Nachricht angegebene KIM-Version \<KIMVersion\> nicht." enthalten. Die
orig-date, from, sender, reply-to, to und cc Header-Elemente der neuen
multipart/mixed Nachricht werden aus der empfangenen Nachricht übernommen. Das
subject Header-Element der neuen multipart/mixed Nachricht erhält den Wert
„Die KIM-Version der empfangenen Nachricht wird nicht unterstützt“.
**[\<=]**

Bei einer Nachricht mit dem Subject „Die KIM-Version der empfangenen Nachricht
wird nicht unterstützt“ gibt es folgende Optionen:

 ---> UL

Für die Entschlüsselung und die Signaturprüfung verwendet das Clientmodul die
Dienste der TI-Plattform, die dem Clientmodul über Schnittstellen des
Konnektors zur Verfügung gestellt werden.

Für die vereinfachte Darstellung wird im Folgenden ein Beispiel einer
Fehlernachricht ohne die Originalnachricht dargestellt:

From: "Sender" \<sender@maildomain.de\>  
To: \<empfaenger@maildomain.de\> 

Message-Id: \<II8HEDLEUEU4.EG0B98QUZNPM2@STST-TEST\>  
Subject: Die
KIM-Version der empfangenen Nachricht wird nicht unterstützt  
MIME-Version:
1.0  
Content-Type: multipart/mixed; boundary="=-hDUtypluINBWKuVpu2reTw==" 

X-KIM-Fehlermeldung: 4008  
--=-hDUtypluINBWKuVpu2reTw==  
Content-Type:
text/plain; charset=utf-8  
Content-Transfer-Encoding: quoted-printable  
Das
verwendete Clientmodul unterstützt die in der empfangenen  
Nachricht
angegebene KIM-Version [1.5] nicht.  
Das verwendete Clientmodul unterstützt
nur Nachrichten einer KIM-  
Version [1.0].  
Es wird empfohlen, das verwendete
Clientmodul zu aktualisieren!  
Leiten Sie diese Mail an Ihre eigene
KIM-E-Mail-Adresse weiter, um die  
Nachrichtenverarbeitung beim nächsten
Abruf der Nachricht zu  
wiederholen.

### 3.4.4.2.1 Entschlüsselung

Für die Entschlüsselung der ankommenden Nachricht wird der private Schlüssel
PrK.HCI.ENC bzw. Prk.HP.ENC verwendet, der dem Verschlüsselungszertifikat der
Institution bzw. des Leistungserbringers zugeordnet ist. Der Zugriff auf die
entsprechende Karte und die Entschlüsselung erfolgen über die Aufrufe der
entsprechenden Operationen der Außenschnittstelle des Konnektors. Eine
detaillierte Beschreibung erfolgt im Kapitel 3.8.4.

Wenn die Nachricht für mehrere Empfänger verschlüsselt wurde, liegt es in der
Verantwortung des Clientmoduls sicherzustellen, dass die Nachricht mit dem
Schlüssel des den Abholvorgang auslösenden Nutzers entschlüsselt wird. Der
erforderliche Schlüssel kann mit Hilfe des im KOM-LE-S/MIME-Profil
beschriebenenrecipient-emailsAttributs imEnvelopedDataCMS-Objekt identifiziert
werden. DasEnvelopedDataCMS-Objekt enthält die verschlüsselten Inhalte und
imrecipient-emailsAttribut werden die Zusammenhänge zwischen den
E-Mail-Adressen der Empfänger und den verwendeten
Verschlüsselungszertifikaten definiert. Das ermöglicht die Identifizierung
des erforderlichen Verschlüsselungszertifikats, dessen zugehöriger privater
Schlüssel für die Entschlüsselung verwendet werden soll. Dadurch kann
vermieden werden, dass die Nachricht mit dem freigeschalteten Schlüssel eines
Empfängers entschlüsselt wird, der nicht derjenige ist, der den Abholvorgang
ausgelöst hat. Das Clientmodul geht davon aus, dass der Nutzername, der für
die POP3-Authentifizierung verwendet wurde, der E-Mail-Adresse des Empfängers
entspricht und benutzt ihn, um den entsprechendenRecipientIdentifieraus
demrecipient-emailsAttribut auszulesen. Wenn es keinenRecipientIdentifiergibt,
der dem POP3-Nutzernamen des Empfängers entspricht, wird die Entschlüsselung
als fehlgeschlagen betrachtet.

Wenn die Entschlüsselung fehlschlägt, wird dem Clientsystem die
verschlüsselte Nachricht im Anhang einer Fehlernachricht übermittelt. Hierzu
wird die angekommene KOM-LE-S/MIME-Nachricht als einemessage/rfc822MIME-Einheit
in einemultipart/mixedMIME-Nachricht verpackt, die zusätzlich
einetext/plainMIME-Einheit mit der Fehlermeldung enthält.
Dieorig-date,from,sender,reply-to,toundccHeader-Elemente der neuen Nachricht
werden aus der ursprünglichen Nachricht übernommen. Der Betreff der neuen
Nachricht enthält die Zeichenkette „Die Nachricht konnte nicht
entschlüsselt werden“.

Beispiel:

Kann eine Nachricht auf Grund des fehlenden HBA mit dem erforderlichen privaten
Schlüssel nicht im Clientmodul entschlüsselt werden, wird die Nachricht wie
folgt dem Clientsystem übermittelt:

MIME-Version: 1.0

Content-Type: multipart/mixed; boundary="unique-boundary-1"

Subject: Die Nachricht konnte nicht entschlüsselt werden

Date: Fri, 9 Feb 2012 12:07:17 +0100

From: mustermann@komle.de

To: musterfrau@komle.de

X-KIM-Fehlermeldung: cmgerr_4

This is a multi-part message in MIME format.

--unique-boundary-1

Content-Type: text/plain;    charset="iso-8859-1"

Content-Transfer-Encoding: quoted-printable

Der f=FCr die Entschl=FCsselung der Nachricht ben=F6tigte Schl=FCssel =

wurde nicht gefunden. =DCberpr=FCfen Sie ob die entsprechende Karte =

gesteckt ist und leiten Sie diese Nachricht an Ihre eigene Email Adresse =

(musterfrau@komle.de) weiter. Beim n=E4chsten Abholen wird der =

Entschl=FCsselungsvorgang wiederholt.

--unique-boundary-1

Content-Type: message/rfc822    

X-KOM-LE-Version: 1.0

MIME-Version: 1.0

Content-Type: application/pkcs7-mime; name="smime.p7m"; name="smime.p7m"

Content-Transfer-Encoding: base64

Content-Disposition: attachment;    filename="smime.p7m"

Subject: KOM-LE Nachricht

Date: Fri, 9 Feb 2012 12:07:17 +0100

From: mustermann@komle.de

To:musterfrau@komle.de

567GhIGfHfYT6ghyHhHUujpfyF4f8HHGTrfvhJhjH776tbB9HG4VQbnj7

77n8HHGT9HG4VQpfyF467GhIGfHfYT6rfvbnj756tbBghyHhHUujhJhjH

HUujhJh4VQpfyF467GhIGfHfYGTrfvbnjT6jH7756tbB9H7n8HHGghyHh

...

9efmAAAAAAAAAAAAAA==

--unique-boundary-1--

**KOM-LE-A_2042 - Entschlüsselung einer KOM-LE-SMIME-Nachricht**

Das Clientmodul MUSS eine vomPOP3-Server erhalteneunddem KOM-LE-S/MIME-Profil
entsprechende E-Mail entschlüsseln.Nachrichten, die nicht dem
KOM-LE-S/MIME-Profil entsprechen, sind ohne Veränderung an das
Clientsystem  weiterzuleiten. **[\<=]**

**KOM-LE-A_2043 - Beachtung des recipient-emails Attributs bei der
Entschlüsselung**

Das Clientmodul MUSS bei der Entschlüsselung dasrecipient-emailsAttribut
desEnvelopedData-CMS-Objekts beachten, umdie Nachricht mit dem Schlüssel des
Nutzers, derdenAbholvorgang ausgelöst hat,zu entschlüsseln. **[\<=]**

**A_20628 - Beachtung des received-Header-Attributs bei der Entschlüsselung**

Das Clientmodul MUSS nach erfolgreicher Entschlüsselung des
EnvelopedData-CMS-Objekts dasreceived-Header-Attributin den Header der
entschlüsselten Nachricht übernehmen. **[\<=]**

**KOM-LE-A_2044 - E-Mail-Adresse des den Abholvorgang auslösenden Nutzers**

Das Clientmodul MUSS den vom Clientsystem erhaltenen POP3-Usernamen(ohne den
#server:port#... Teil) als die E-Mail-Adresse des den Abholvorgang auslösenden
Nutzersbetrachten. **[\<=]**

**KOM-LE-A_2045 - Entschlüsselung nur mit Schlüsseln des abholenden Nutzers**

Das Clientmodul DARFfür die Entschlüsselung einer NachrichtSchlüssel
NICHTverwenden, wenn sie von anderenNutzern stammen als von dem der
denAbholvorgangausgelöst hat. **[\<=]**

**KOM-LE-A_2179-01 - Vermerk in der Nachricht bei erfolgreicher
Entschlüsselung**

Das Clientmodul MUSS bei erfolgreicher Entschlüsselung der KOM-LE-Nachricht den
Vermerk „Die Nachricht wurde entschlüsselt.“ an den Text der Nachricht
anhängen. Es ist dabei das Format des TextParts zu beachten (mediatype
text/html oder text/plain) und der Vermerk diesem Format anzupassen. **[\<=]**

**KOM-LE-A_2046 - Aufbau der Fehlernachricht bei fehlgeschlagener
Entschlüsselung**

Das Clientmodul MUSS eine empfangene, dem KOM-LE-S/MIME-Profil entsprechende
Nachricht, diez.B.aufGrund desfehlenden Schlüsselsnicht entschlüsselt
werdenkann, als einemessage/rfc822MIME-Einheit in
einerneuenmultipart/mixedMIME-Nachrichtdem Clientsystem übermitteln.
Zusätzlich muss diese
neuemultipart/mixedMIME-Nachrichteinetext/plainMIME-Einheit mit dem
Fehlertextenthalten.
Dieorig-date,from,sender,reply-to,toundccHeader-Elementeder neuenmultipart/mixedNachricht
werden ausderempfangenenNachricht übernommen.DassubjectHeader-Element der
neuenmultipart/mixedNachrichterhältdenWert„Die Nachricht konnte nicht
entschlüsselt werden“. **[\<=]**

Bei einer Nachricht mit dem Subject „Die Nachricht konnte nicht entschlüsselt
werden“ gibt es folgende Optionen:

 ---> UL

Tabelle Tab_Fehlertext_Entschl enthält die Fehlertexte, die in die Nachricht
eingeführt werden, wenn die Entschlüsselung nicht durchgeführt werden konnte.

<table><tr><th>
ID*

</th><th>
Bedingung

</th><th>
Fehlertexte

</th></tr><tr><td>
01

</td><td>
Die KOM-LE-Nachricht konnte auf Grund eines nicht verfügbaren Schlüssels nicht
entschlüsselt werden.

</td><td>
Der für die Entschlüsselung der Nachricht benötigte Schlüssel wurde nicht
gefunden. Überprüfen Sie ob die entsprechende Karte gesteckt ist und leiten
Sie diese Nachricht an Ihre eigene E-Mail-Adresse (\<Email Adresse\>) weiter.
Beim nächsten Abholen wird der Entschlüsselungsvorgang wiederholt.

</td></tr><tr><td>
02

</td><td>
Die KOM-LE-Nachricht konnte aufgrund des falschen Formats nicht entschlüsselt
werden (z.B. enthält die Nachricht das X-KOM-LE-Version Header-Element,
entspricht aber nicht dem KOM-LE-S/MIME-Profil).

</td><td>
Die Nachricht wurde als eine verschlüsselte KIM-Nachricht gekennzeichnet,
konnte aber auf Grund des falschen Formats nicht entschlüsselt werden. Die
Verschlüsselte Nachricht befindet sich im Anhang.

</td></tr><tr><td>
03

</td><td>
Der Konnektor steht für die Entschlüsselung nicht zur Verfügung.

</td><td>
Die Entschlüsselung konnte nicht erfolgen, weil der Konnektor nicht antwortet.
Stellen Sie sicher, dass der Konnektor wieder zur Verfügung steht und leiten
Sie diese Nachricht an Ihre eigene E-Mail-Adresse (\<Email Adresse\>) weiter.
Beim nächsten Abholen wird der Entschlüsselungsvorgang wiederholt.

</td></tr></table>

*) Hinweis: Die in der Tabelle enthaltene ID des jeweiligen Prüfvermerks kann
gemäß [KOM-LE-A_2047] als ID dem Fehlertext der MIME Fehlernachricht
hinzugefügt werden und muss in das X-KIM-DecryptionResult Header-Element
aufgenommen werden, um damit eine spätere automatische Auswertung zu
ermöglichen.

**KOM-LE-A_2047-01 - Fehlertexte bei fehlgeschlagener Entschlüsselung**

Das Clientmodul MUSS bei fehlgeschlagener Entschlüsselung entsprechend der
jeweiligen Bedingung die in Tabelle Tab_Fehlertext_Entschl definierten
Fehlertexte in dietext/plainMIME-Einheit der multipart/mixed
MIME-Fehlernachricht aufnehmen.Zusätzlich MUSS das Clientmodul ein
Mail-Header-Attribut X-KIM-DecryptionResult mit der dazugehörigen ID aus der
Tabelle Tab_Verm_Sig_Prüf Fehlercode befüllen. **[\<=]**

### 3.4.4.2.2 Integritätsprüfung

Nachdem die angekommene Nachricht erfolgreich entschlüsselt wurde, prüft das
Clientmodul ihre Integrität. Dabei werden die digitale Signatur der Nachricht,
der Zertifizierungspfad für das Signaturzertifikat und die Integrität
desrecipient-emailsAttributs geprüft. Für die Signaturprüfung der Nachricht
wird das im CMS-Objekt mitgelieferte C.HCI.OSIG-Institutionszertifikat benutzt.
Die Prüfung der Signatur erfolgt über die Aufrufe der entsprechenden
Operationen der Außenschnittstelle des Konnektors. Eine detaillierte
Beschreibung erfolgt in Kapitel 3.8.2. Das Ergebnis der Signaturprüfung des
Konnektors und des Abgleichs desrecipient-emailsAttributs wird als Vermerk, der
den Text der Nachricht ergänzt, dem Empfänger mitgeteilt.

Die Tabelle "Tab_Verm_Sig_Prüf Vermerke mit Ergebnissen der Signaturprüfung"
stellt die einzufügenden Vermerke entsprechend den Ergebnissen der
Signaturprüfung des Konnektors dar.In dieser Tabelle werden die
Prüfergebnisse mit den entsprechenden Fehlercodes sowie die Vermerke
zusammengefasst. Die Prüfergebnisse entsprechen dem Gesamtergebnis für die
Prüfung einer nicht qualifizierten Dokumentensignatur (nonQES) für die
Operation VerifyDocument des Konnektors gemäß [gemSpec_KON#TAB_KON_754] und
[gemSpec_KON#TAB_KON_124].

<table><tr><th>
ID*

</th><th>
Prüfergebnis

</th><th>
Fehlercode

</th><th>
Ergebnis

</th><th>
Vermerk

</th></tr><tr><td>
01

</td><td>
VALID

</td><td>
-

</td><td>
Die Signatur der Nachricht wurde erfolgreich geprüft.

</td><td>
Die Signatur wurde erfolgreich geprüft.

</td></tr><tr><td>
02

</td><td>
INVALID

</td><td>
4115

</td><td>
Die Integrität der Nachricht wurde verletzt.

</td><td>
Die Prüfung der Signatur hat ergeben, dass die Nachricht manipuliert wurde.

</td></tr><tr><td>
03

</td><td>
INVALID

</td><td>
4253

</td><td>
Die digitale Signatur ist nicht vorhanden.

</td><td>
Die Nachricht ist nicht signiert. Die Nachricht ist deshalb eventuell
manipuliert worden.

</td></tr><tr><td>
04

</td><td>
INVALID

</td><td>
4112

</td><td>
Die digitale Signatur konnte aufgrund des falschen Formats nicht geprüft werden.

</td><td>
Die Signatur der Nachricht konnte aufgrund eines falschen Formats nicht geprüft
werden. Die Nachricht ist deshalb eventuell manipuliert worden.

</td></tr><tr><td>
05

</td><td>
INVALID

</td><td>
4206

</td><td>
Der Zertifizierungspfad des Signaturzertifikats kann nicht validiert werden
(abgelaufenes Zertifikat, der Zertifizierungspfad konnte nicht aufgebaut werden
usw.).

</td><td>
Die Signatur der Nachricht wurde geprüft. Die dabei durchgeführte
Integritätsprüfung der Nachricht war erfolgreich. Der Status des zur Signatur
verwendeten Zertifikats konnte nicht vollständig durchgeführt werden, weil
nicht alle am Signaturprozess beteiligten Zertifikate validiert werden konnten.

</td></tr><tr><td>
06

</td><td>
INVALID

</td><td>
[Fehlercode]

</td><td>
Die digitale Signatur konnte aufgrund eines nicht zuordenbaren Fehlercodes des
Konnektors nicht geprüft werden.

</td><td>
Bei der Prüfung der digitalen Signatur ist ein unerwarteter Fehler aufgetreten.

</td></tr><tr><td>
07

</td><td>
INCONCLUSIVE

</td><td>
4264

</td><td>
Die digitale Signatur ist mathematisch korrekt, der Zertifikatsstatus des
Signaturzertifikats konnte aber nicht geprüft werden.

</td><td>
Die Signatur der Nachricht wurde geprüft. Die dabei durchgeführte
Integritätsprüfung der Nachricht war erfolgreich. Der Status des zur Signatur
verwendeten Zertifikats konnte nicht vollständig geprüft werden, weil zum
Prüfungszeitpunkt nicht alle erforderlichen technischen Ressourcen verfügbar
waren.

</td></tr><tr><td>
08

</td><td>
VALID

</td><td>
-

</td><td>
Die digitale Signatur ist mathematisch korrekt und der Zertifikatsstatus des
Signaturzertifikats konnte erfolgreich geprüft werden, aber beim Vergleich der
Header-Elemente from, sender, reply-to, to und cc der äußeren Nachricht mit
denen der inneren Nachricht wurden Abweichungen festgestellt.

</td><td>
Die Signatur der Nachricht wurde geprüft. Die Prüfung hat ergeben, dass die
Nachricht nach dem Verschlüsseln manipuliert wurde. Möglicherweise wurde die
verschlüsselte Nachricht auch an einen nicht empfangsberechtigten
Personenkreis versendet.

</td></tr><tr><td>
09

</td><td>
VALID

</td><td>
-

</td><td>
Die digitale Signatur ist mathematisch korrekt und der Zertifikatsstatus des
Signaturzertifikats konnte erfolgreich geprüft werden, aber das
recipient-emails-Attribut aus signerInfos enthält nicht die gleichen Werte wie
das recipient-emails-Attribut aus dem enveloped-data CMS-Objekt.

</td><td>
Die Signatur der Nachricht wurde geprüft. Die Prüfung hat ergeben, dass die
Nachricht manipuliert wurde, um einem anderen Nutzer das Entschlüsseln der
Nachricht mit einem Schlüssel, der nicht in seinem Besitz ist, zu ermöglichen.

</td></tr></table>

*) Hinweis: Die in der Tabelle enthaltene ID des jeweiligen Prüfvermerks kann
gemäß [KOM-LE-A_2050] als ID dem Vermerk hinzugefügt werden und muss in das
X-KIM-IntegrityCheckResult Header-Element aufgenommen  werden, um damit eine
spätere automatische Auswertung zu ermöglichen.

Falls der Zertifikatstatus des Signaturzertifikates nicht geprüft werden kann
(z.B. der OCSP-Responder ist unerreichbar), die mathematische Prüfung der
Signatur aber erfolgreich durchgeführt wurde, wird ein entsprechender Vermerk
in den Body der Nachricht eingetragen.

Es folgt ein Beispiel einer entschlüsseltenmultipart/mixedNachricht deren
Signatur erfolgreich geprüft wurde. Die Nachricht enthält
einetext/plainEinheit im Nachrichtentext und einen Arztbrief als PDF-Anhang.

Date: Fri, 9 Feb 2012 12:07:17 +0100

MIME-Version: 1.0

From: mustermann@komle.de

To: musterfrau@komle.de

Subject: Arztbrief

Content-Type: multipart/mixed;

X-KIM-Dienstkennung: Arztbrief;VHitG-Versand;V1.2

X-KIM-Sendersystem: Beispiel-PVS;V2.81

boundary="unique-boundary-1"

This is a multi-part message in MIME format.

--unique-boundary-1

Content-Type: text/plain;    charset="iso-8859-1"

Content-Transfer-Encoding: 8bit

Sehr Geehrte Frau Dr. Musterfrau,

hiermit sende ich Ihnen den Arztbrief f=FCr Herrn H. Muster.

Mit Freundlichen Gr=FC=DFen

Dr. med. Mustermann

Arzt f=FCr Allgemeinmedizin

---------------------------------------------

Die Nachricht wurde entschl=FCsselt

Die Signatur wurde erfolgreich gepr=FCft.

--unique-boundary-1

Content-Type: application/pdf;

name="Arztbrief_Muster.pdf"

Content-Transfer-Encoding: base64

Content-Disposition: attachment;

Content-Description: eAB-PDF-signed

filename="Arztbrief_Muster.pdf"

JVBERi0xLjQNCiXDpMO8w7bDnw0KMiAwIG9iag0KPDwgL0xlbmd0aCAzIDAgUg0KICAgL0Zp

bHRlciAvRmxhdGVEZWNvZGUNCj4+DQpzdHJlYW0NCnicrVhda1sxDH0P5D/4uQ+3lvxxfaEM

...

OEJCQUExQzY0NDU+IF0NCj4+DQpzdGFydHhyZWYNCjIyNDU3Mg0KJSVFT0YNCg==

--unique-boundary-1--

**KOM-LE-A_2048-01 - Prüfung der Signatur und Integrität einer
KOM-LE-Nachricht**

Das Clientmodul MUSS die Integrität der KOM-LE-Nachricht prüfen. Dabei müssen
die digitale Signatur selbst, der Zertifizierungspfad für das verwendete
Signaturzertifikat, die Integrität des Headers der äußeren Nachricht und die
Integrität desrecipient-emailsAttributs geprüft werden.Bei der Prüfung der
Integrität des Headers der äußeren Nachricht sind die
Header-Elementefrom,sender,reply-to,toundccmit denen der signierten inneren
Nachricht zu vergleichen.Bei der Prüfung der Integrität
desrecipient-emailsAttributs sind die Werte dieses Attributs aussignerInfosund
aus demenveloped-dataCMS-Objekt miteinander zu vergleichen. **[\<=]**

Hinweis: Für lange Header-Elemente (z. B. bei reply-to) muss "folding" gemäß
[RFC822] unterstützt werden.

**KOM-LE-A_2050-04 - Vermerke des Ergebnisses der Signaturprüfung einer
KOM-LE-Nachricht**

Das Clientmodul MUSS abhängig vom Ergebnis der Signaturprüfung einer
KOM-LE-Nachricht die in Tabelle Tab_Verm_Sig_Prüf definierten Vermerke an den
Nachrichtentext der KOM-LE-Nachricht anfügen. Es ist dabei das Format des
TextParts zu beachten (mediatype text/html oder text/plain) und der Vermerk
diesem Format anzupassen. Zusätzlich MUSS das Clientmodul ein
Mail-Header-Attribut X-KIM-IntegrityCheckResult mit der dazugehörigen ID aus
der Tabelle Tab_Verm_Sig_Prüf Fehlercode befüllen. **[\<=]**

### 3.4.5 Beispiele

Das Clientsystem (C) verbindet sich mit dem Clientmodul (M) und holt vom
POP3-Server (S) eine Nachricht (im Beispiel werden auch die Zustände des
Clientmoduls dargestellt):

C:    \<das Clientsystem öffnet eine mit TLS geschützte Verbindung mit dem
Clientmodul\>

M:    \<CONNECT Zustand\>

M-\>C: +OK KOM-LE Clientmodul POP3

C-\>M: CAPA

M-\>C: +OK Capability list follows

M-\>C: TOP

M-\>C: USER

M-\>C: SASL PLAIN

M-\>C: UIDL

M-\>C: .

C-\>M: USERmustermann@komle.de#pop.komle.de:110#1#KOM-LE#7

M-\>C: +OK

C-\>M: PASS password

M:    \<das Clientmodul öffnet eine mit TLS geschützte Verbindung mit dem
POP3 Server\>

S-\>M: +OK POP Server Ready

M-\>S: CAPA

S-\>M: +OK Capability list follows

S-\>M: TOP

S-\>M: USER

S-\>M: SASL PLAIN CRAM-MD5

S-\>M: UIDL

S-\>M: RESP-CODES

S-\>M: .

M-\>S: USERmustermann@komle.de

S-\>M: +OK

M-\>S: PASS password

S-\>M: +OK Maildrop ready

M:    \<PROXY Zustand\>

M-\>C: +OK Maildrop ready

C-\>M: STAT

M-\>S: STAT

S-\>M: +OK 1 13950

M-\>C: +OK 1 13950

C-\>M: LIST

M-\>S: LIST

S-\>M: +OK

M-\>C: +OK

S-\>M: 1 13950

M-\>C: 1 13950

S-\>M: .

M-\>C: .

C-\>M: UIDL

M-\>S: UIDL

S-\>M: +OK

M-\>C: +OK

S-\>M: 1 01SDF8-1RiSd50vfv-00FGJN

M-\>C: 1 01SDF8-1RiSd50vfv-00FGJN

S-\>M: .

M-\>C: .

C-\>M: RETR 1

M-\>S: RETR 1

S-\>M: +OK

M-\>C: +OK

M:    \<PROCESS Zustand\>

S-\>M: \<Inhalt der verschlüsselten KOM-LE Nachricht\>

S-\>M: .

M:    \<die Nachricht wird im Clientmodul aufbereitet\>

M-\>C: \<Inhalt der KOM-LE Nachricht\>

M-\>C: .

M:    \<PROXY Zustand\>

C-\>M: QUIT

M-\>S: QUIT

S-\>M: +OK

S:    \<der POP3 Server schließt die Verbindung mit dem Clientmodul\>

M-\>S: +OK

M:    \<das Clientmodul schließt die Verbindung mit dem Clientsystem\>

Während des Löschens einer Nachricht wird die Verbindung zwischen dem
Clientmodul und dem POP3-Server abgebrochen:

...

C-\>M: UIDL

M-\>S: UIDL

S-\>M: +OK

M-\>C: +OK

S-\>M: 1 01SDF8-1RiSd50vfv-00FGJN

M-\>C: 1 01SDF8-1RiSd50vfv-00FGJN

S-\>M: .

M-\>C: .

C-\>M: DELE 1

C:    \<die Verbindung zwischen dem Clientmodul und dem Clientsystem wird
abgebrochen\>

M-\>S: DELE 1

M:    \<die Verbindung zwischen dem Clientmodul und dem POP3 Server wird
geschlossen\>

### 3.5 Übermittlung von Kontaktdaten

Ein KOM-LE-Nutzer soll die Möglichkeit haben in seinem Clientsystem die Suche
nach den E-Mail-Adressen der Empfänger seiner KOM-LE-Nachrichten
durchzuführen. Die TI-Plattform stellt einen Verzeichnisdienst zur Verfügung,
der unter anderem Einträge mit Kontaktdaten von KOM-LE-Nutzern enthält. Der
Verzeichnisdienst kann über LDAP abgefragt werden und kann somit als
Adressbuch für KOM-LE benutzt werden. Eine detaillierte Beschreibung des
Verzeichnisdienstes der TI-Plattform befindet sich in [gemSpec_VZD]. Um
LDAP-Anfragen gegenüber dem Verzeichnisdienst durchzuführen, fungiert der
Konnektor als LDAP-Proxy wie in [gemSpec_Kon] beschrieben.

Der Verzeichnisdienst kann direkt von Clientsystemen, die die entsprechenden
LDAP-Suchanfragen generieren, angefragt werden. Das LDAP-Schema des
Verzeichnisdienstes wird in [gemSpec_VZD] beschrieben.

### 3.6 Übermittlung von E-Mail-Kategorien

Das Clientmodul soll die Kategorisierung von versendeten E-Mails ermöglichen.
Zusätzlich zu den für den Versand einer gültigen E-Mail notwendigen
Header-Feldern wird ein weiteres Attribut im Header eingefügt und mit der
Information befüllt, welche der verwendete E-Mail-Client liefert.

**A_19488-02 - E-Mail-Kategorisierung**

Das KOM-LE-Clientmodul MUSS die ihm im Mail-Header gemäß der Tabelle
"Tab_Header_Kat Header-Feld Kategorie" bereitgestellte Information zur
Kategorisierung einer zu übertragenden E-Mail weiterleiten. Die Benennung
dieses zusätzlichen E-Mail-Header-Feldes erfolgt wie in Tabelle
"Tab_Header_Kat festgelegt". Wenn vom Mail-Client keine Informationen
übergeben werden können, wird durch das KOM-LE-Clientmodul der Default-Wert
aus der X-KIM-Dienstkennung gesetzt. **[\<=]**

<table><tr><th>
Header-Feld

</th><th>
Name

</th><th>
Verpflichtend

</th><th>
Beschreibung

</th></tr><tr><td>
X-KIM-Dienstkennung

</td><td>
E-Mail-Kategorie

</td><td>
optional

</td><td>
Zusätzliches E-Mail-Header-Feld, enthält die auf die E-Mail bezogene
Dienstkennung mit Bezug auf deren Inhalt.

Wenn vom Mail-Client keine Informationen übergeben werden können, wird durch
das KOM-LE-Clientmodul der Default-Wert aus der X-KIM-Dienstkennung gesetzt.

</td></tr></table>

Die zu verwendenden Dienstkennungen werden durch die gematik festgelegt und sind
über das Fachportal der gematik im Bereich "Toolkit" abrufbar. Die dort durch
die gematik auf der Seite "Dienstkennung" administrierte Übersicht liefert bei
Bedarf die Default-Dienstkennung. Diese wird durch das Clientmodul vor der
weiteren Verarbeitung in das Headerfeld X-KIM-Dienstkennung der ursprünglichen
E-Mail eingetragen, wenn keine Dienstkennung durch den Mail-Client des Senders
eingetragen wurde.

Das Header-FeldX-KIM-Dienstkennungwird im unverschlüsselten Header der E-Mail
enthalten sein, um eine eventuelle Verarbeitung der E-Mail auf Seiten des
Empfängers zu ermöglichen. Eine entsprechende Festlegung erfolgt in der
[gemSMIME_KOMLE] im Kapitel 2.1.1.1.

### 3.7 Administrationsmodul

Das Administrationsmodul ist Bestandteil des KOM-LE-Clientmoduls. Das Modul
ermöglicht die Verwaltung des Accounts des KOM-LE-Teilnehmers. Dazu
kommuniziert das Administrationsmodul über eine TLS-Verbindung mit dem Account
Manager des KOM-LE-Fachdienstes. Zum Funktionsumfang des Modules gehören:

 ---> UL

Im ersten Schritt konfiguriert der KOM-LE-Teilnehmer einmalig die Domain des
KOM-LE-Fachdienstes im Administrationsmodul. Dadurch ist das
Administrationsmodul in der Lage, den Account Manager über DNS Service
Discovery zu lokalisieren. Danach können sich neue KOM-LE-Teilnehmer über das
Administrationsmodul bei ihrem KOM-LE-Fachdienst registrieren und die
benötigte PKCS#12 Dateien für das Clientmodul herunterladen.

Die konzeptionelle Betrachtung für das Administrationsmodul sieht wie folgt aus:

 ---> OL

### 3.7.1 Allgemeine Anforderungen

**A_19453 - Aktualisierung PKCS#12-Datei Administrationsmodul**

Das Administrationsmodul MUSS die PKCS#12-Datei dem Clientmodul für die
Weiterverarbeitung übergeben. **[\<=]**

**A_19454 - Dialoggestaltung Administrationsmodul**

Das Administrationsmodul SOLL die Dialoggestaltung gemäß [EN ISO 9241#Teil110]
sicherstellen. **[\<=]**

**A_19455 - Formulardialoge Administrationsmodul**

Das Administrationsmodul SOLL bei Verwendung von Formulardialogen die
Anforderungen und Empfehlungen gemäß [DIN EN ISO 9241-143:2012-06] beachten.
**[\<=]**

**A_19456-02 - Domain Fachdienst Administrationsmodul**

Das Administrationsmodul MUSS die Auswahl der genutzten Fachdienste
ermöglichen.  **[\<=]**

Die Domain des Anbieters kann z.B. die folgende Ausprägung haben:

hrst.kim.telematik

**A_19523 - Service-Discovery Administrationsmodul**

Das Administrationsmodul MUSS die zur Kommunikation mit dem Account Manager des
Fachdienstes notwendigen Informationen durch DNS Service Discovery nach den in
[gemSpec_FD_KOMLE#Tab_KOMLE_Service Discovery] und
[gemSpec_FD_KOMLE#Tab_KOMLE_FQDN] ermitteln. **[\<=]**

**A_19457-02 - Client Authentisierung Administrationsmodul**

Das Administrationsmodul MUSS bei der initialen Registrierung eine serverseitig
gesicherte TLS-Verbindung zum Account Managers des Fachdienstes aufbauen.Für
die Authentisierung am Account Manager MUSS das Administrationsmodul ein
JSON-Web-Token gemäß [RFC7519] mit den Elementen aus der folgenden Tabelle
erzeugen und zusammen mit dem Passwort des Nutzers an den Account Manager
übergeben. **[\<=]**

Der Parameter "alg": "PS256" ist informativ. Anstatt einer üblichen Signatur
bildet er den Hash gemäß [gemSpec_Krypt#A_19644]. Dieser wird mittels der
externalAuthenticate-Funktion des Konnektors mit dem AUT-Zertifikat des HBA
bzw. der SMC-B signiert. Als Signature Type muss RSASSA-PSS verwendet werden.
Diese Signatur wird anstatt des Signaturteils des Tokens angehängt.

Der Account Manager ist Bestandteil des Fachdiensts und deshalb gelten für die
TLS-Verbindungen (inklusive genutzter Zertifikate) zum Account Manager
ebenfalls die Festlegungen von Kap. 4.1.4.

**A_20773 - I_AccountManager_Service Zeichensatz Clientmodul**

Das Administrationsmodul  MUSS für die Inhalte aller Operationen (Request und
Response) der Schnittstelle  I_AccountManager_Service den UTF-8-Zeichensatz
unterstützen. **[\<=]**

Abweichung außerhalb der Leistungserbringerumgebung

Für Umgebungen außerhalb der Leistungserbringerumgebung (z. B. im
Rechenzentrum) können von den Anforderungen zur Dialogsteuerung abgewichen
werden.

**A_20188 - Formulardialoge Administrationsmodul - außerhalb der
Leistungserbringerumgebung**

Das Administrationsmodul KANN bei Verwendung außerhalb der
Leistungserbringerumgebung von der Dialogsteuerung abweichen. **[\<=]**

**A_21396 - Darstellung von Ereignissen**

Das Administrationsmodul MUSS bei Aufruf der Operationen am Account Manager die
Ergebnisse der Operationen sowie Fehlernachrichten darstellen. **[\<=]**

**A_21380 - Verwaltung von Abwesenheitsnotizen**

Das Clientmodul MUSS es dem Nutzer ermöglichen, Abwesenheitsnotizen über die
Schnittstelle I_AccountManager_Service am Account Manager verwalten zu
können. **[\<=]**

### 3.7.2 Registrierung KOM-LE-Teilnehmer

**A_19458-01 - Initiale Anmeldung KOM-LE-Teilnehmer Administrationsmodul**

Das Administrationsmodul MUSS sich bei der initialen Anmeldung mit der
referenceID und dem initialen Passwort am Account Manager authentifizieren.
**[\<=]**

**A_19459 - Registrierung Aufruf KOM-LE-Teilnehmer Administrationsmodul**

Das Administrationsmodul MUSS die Registrierung des neuen KOM-LE-Teilnehmers
am Account Manager ermöglichen. **[\<=]**

**A_19460 - Registrierungsdialog KOM-LE-Teilnehmer Administrationsmodul**

Das Administrationsmodul MUSS die Registrierung des neuen KOM-LE-Teilnehmers
im Dialog durchführen. **[\<=]**

**A_19462 - Registrierungsfehler KOM-LE-Teilnehmer Administrationsmodul**

Das Administrationsmodul MUSS Fehler bei der Registrierung verständlich
anzeigen und dem Anwender Handlungsoptionen anbieten. **[\<=]**

### 3.7.3 Deregistrierung KOM-LE-Teilnehmer

**A_19463 - Deregistrierung Aufruf KOM-LE-Teilnehmer Administrationsmodul**

Das Administrationsmodul MUSS die Deregistrierung des KOM-LE-Teilnehmers am
Account Manager ermöglichen. **[\<=]**

**A_19464-02 - Deregistrierungsdialog KOM-LE-Teilnehmer Administrationsmodul**

Das Administrationsmodul MUSS die Deregistrierung  des KOM-LE-Teilnehmers im
Dialog durchführen. Im Verlauf der Deregistrierung MUSS der KOM-LE-Teilnehmer
in geeigneter Form informiert werden, dass nach der Deregistrierung kein
weiterer Zugriff auf das E-Mail-Konto möglich ist, das gelöschte Konto nicht
wiederhergestellt werden und die damit verbundene E-Mail-Adresse nicht neu
vergeben werden kann.   **[\<=]**

### 3.7.4 Download PKCS#12 KOM-LE-Teilnehmer

**A_19468-02 - Beantragen und Herunterladen der PKCS#12 Datei**

Das Administrationsmodul MUSS die PKCS#12-Datei über die
OperationcreateCert()am Account Manager beantragen und vom Account Manager
herunterladen. Nach dem Herunterladen der PKCS#12-Datei MUSS das
Administrationsmodul diese mit dem vom Administrationsmodul erzeugten
symmetrischen Schlüssel entschlüsseln. **[\<=]**

**A_21381 - Automatischer Abruf der PKCS#12-Datei**

Das Administrationsmodul MUSS einen Monat vor Ablauf des TLS-Zertifikates
automatisch ein neues Zertifikat über die OperationcreateCert()beantragen und
herunterladen. Die zeitliche Gültigkeit des Zertifikats muss vom Clientmodul
beim TLS-Verbindungsaufbau geprüft werden.Wenn während der Aktualisierung ein
Fehler auftritt, dann MUSS das KOM-LE-Clientmodul den Absender mit einer E-Mail
über den Fehlerfall informieren. Aus dem Inhalt der Fehlernachricht MUSS
hervorgehen, dass bei der Aktualisierung der PKCS#12-Datei ein Fehler
aufgetreten ist. Die Fehlernachricht ist weder zu signieren noch zu
verschlüsseln und entsprichtder Delivery Status Notification gemäß
[RFC3461-3464]. Zusätzlich muss der vom Account Manager gemeldeter Fehlertext
wie folgt eingefügt werden: Fehlertext:\<message\>. **[\<=]**

**A_21382 - Generierung eines symmetrischen Schlüssels für die PKCS#12-Datei**

Das Administrationsmodul MUSS bei Aufruf der OperationcreateCert()einen
symmetrischen Schlüssel gemäß den Kriterien [gemSpec_Kryp] generieren und
als Parameter CertPassword übergeben. **[\<=]**

### 3.8 Kryptographischen Schnittstellen des Konnektors

Das digitale Signieren und die Verschlüsselung von Nachrichten sowie deren
Entschlüsselung und die Prüfung ihrer digitalen Signaturen beinhalten den
Zugriff auf die SOAP-Schnittstellen des Konnektors, die die folgenden
Operationen zu Verfügung stellen:

 ---> UL

Die Verschlüsselung und das digitale Signieren erfordern dabei den Zugriff auf
eine SM-B und/oder einen HBA mit dem erforderlichen Schlüsselmaterial. Zur
Erstellung einer digitalen Signatur ist der Zugriff auf den geheimen Schlüssel
PrK.HCI.OSIG einer SM-B erforderlich. Für die Verschlüsselung ist der Zugriff
auf den geheimen Schlüssel Prk.HCI.ENC einer SM-B oder Prk.HP.ENC eines HBA
notwendig.

Der Zugriff auf den entsprechenden geheimen Schlüssel erfolgt während der
Durchführung derSignDocumentundDecryptDocumentOperationen. Die
Eingangsparameter der beiden Operationen beinhalten dasContextElement
(Aufrufkontext). Der Aufrufkontext umfasst die Angaben zu Mandanten
(MandantId), Arbeitsplatz (WorkplaceId), Anwendung (ClientSystemId) und
Identifikation des Benutzers (UserId). Die Angaben zur Identifikation des
Benutzers (UserId) sind optional und nur für Aufrufe, die einen Zugriff auf
den HBA brauchen, erforderlich. Die Elemente des Aufrufkontexts werden dem
Clientmodul als Teile des MTA- bzw. POP3-Benutzernamens übertragen (siehe
Kapitel 3.2.2.2, 3.3.2.2).

Zur Identifikation der Karte benötigen die Operationen zusätzlich den
ParametercardHandle. DascardHandlegilt für die Dauer des Steckzyklus einer
Karte und wird beim Stecken einer Karte vom Konnektor generiert. Um eine Karte
über mehreren Steckzyklen zu identifizieren kann die Seriennummer der Karte
(ICCSN) verwendet werden.

Die über den Konnektor verfügbaren SM-Bs und HBAs, ihre Handles und ICCSNs
können über dieGetCardsOperation des Konnektors ermittelt werden.

### 3.8.1 Erstellung der digitalen Signatur einer Nachricht mit einer SM-B

Das Signieren von ausgehenden Nachrichten erfolgt mit dem Schlüssel
PrK.HCI.OSIG der SM-B, die der Institution des Senders entspricht. Ein
Konnektor kann von mehreren Institutionen (Mandaten) gleichzeitig benutzt
werden und dementsprechend mit mehreren SM-Bs, die den unterschiedlichen
Identitäten entsprechen, ausgestattet sein. Die Ermittlung der SM-B, die für
die Erstellung der Nachrichtensignatur verwendet werden soll, kann entsprechend
dem in der Abbildung "Abb_Zugriff_SMB SM-B-Zugriff zur Erstellung der
Nachrichtensignatur" dargestellten Aktivitätsdiagramm erfolgen. Die
Aktivitäten und deren Reihenfolge haben illustrativen und nicht normativen
Charakter. Die konkrete Umsetzung kann sich unterscheiden, solange das Ergebnis
das Gleiche ist.

![Abbildung-13][Abbildung-13]

Es folgt die Beschreibung der einzelnen Aktivitäten des Diagramms:

 ---> OL

 ---> UL

 ---> OL

 ---> UL

 ---> OL

**KOM-LE-A_2052 - Quellen zur Ermittlung der SM-B des Senders beim Signieren**

Das Clientmodul MUSS die Menge der verfügbaren Karten, die über die
OperationGetCardsdes Konnektors anhand des Aufrufkontexts des Senders ermittelt
werden, nach einer verfügbaren SM-B durchsuchen. **[\<=]**

**KOM-LE-A_2057 - Abbrechen des Signierens, wenn keine SM-B verfügbar ist**

Das Clientmodul MUSS das Signieren einer Nachricht abbrechen, wenn für die
Erstellung der Signatur keine SM-B verfügbar/gesteckt ist. **[\<=]**

**KOM-LE-A_2058 - Abbrechen des Signierens, wenn Freischaltung der
erforderlichen SM-B fehlschlägt**

Das Clientmodul MUSS das Signieren einer Nachricht abbrechen, wenn die
Freischaltung der für die Erstellung der Signatur erforderlichen SM-B
fehlschlägt. **[\<=]**

### 3.8.2 Prüfung der digitalen Signatur einer Nachricht

Die Prüfung der digitalen Signatur einer Nachricht erfolgt mittels
derVerifyDocumentOperation des Konnektors. Dabei werden die
ParameterContext(dem Empfänger entsprechender Aufrufkontext)
undDocument(signierte Daten) verwendet.

### 3.8.3 Verschlüsselung einer Nachricht

Die Verschlüsselung einer Nachricht erfolgt mittels derEncryptDocumentOperation
des Konnektors. Dabei werden die ParameterContext(dem Empfänger entsprechender
Aufrufkontext),Document(zu verschlüsselnde Daten) undCertificate (alle
Zertifikate mit denen die Nachricht verschlüsselt werden soll) verwendet.

### 3.8.4 Entschlüsselung einer Nachricht mit einer SM-B bzw. einem HBA

Für die Entschlüsselung von empfangenen Nachrichten verwendet das Clientmodul
den privaten Schlüssel PrK.HP.ENC eines HBA bzw. den privaten Schlüssel
PrK.HCI.ENC einer SM-B. Die Zuordnung von den für die Verschlüsselung
verwendeten Zertifikaten und den E-Mail-Adressen der Empfänger wird
imrecipient-emailsAttribut des CMS-Objektes mit den verschlüsselten Daten
abgebildet (siehe [gemSMIME_KOMLE]). Die Ermittlung des HBAs bzw. der SM-B, die
für die Entschlüsselung der empfangenen Nachricht verwendet wird, kann
entsprechend dem in Abbildung 14 dargestellten Aktivitätsdiagramm
durchgeführt werden. Die Aktivitäten und deren Reihenfolge haben
illustrativen und nicht normativen Charakter. Die konkrete Umsetzung kann sich
unterscheiden, solange das Ergebnis das Gleiche ist.

![Abbildung-14][Abbildung-14]

Es folgt die Beschreibung der einzelnen Aktivitäten des Diagramms:

 ---> OL

 ---> UL

 ---> OL

 ---> UL

 ---> OL

 ---> UL

 ---> OL

**KOM-LE-A_2059 - Verwendung des recipient-emails Attributs beim Entschlüsseln**

Das Clientmodul MUSS die Suche nach der zur Entschlüsselung erforderlichen
Karte anhand der E-Mail-Adresse des Empfängers und der zugehörigen
Zertifikats-IDs aus demrecipient-emailsAttribut des CMS-Objektes der
KOM-LE-Nachricht durchführen. **[\<=]**

**KOM-LE-A_2060 - Quellen zur Ermittlung der erforderlichen Karte beim
Entschlüsseln**

Das Clientmodul MUSS für die Ermittlung der zur Entschlüsselung einer
Nachricht erforderlichen Karte primär seinen Cache durchsuchen. Wird die
erforderliche Karte nicht über den Cache gefunden, MUSS das Clientmodul die
Menge der verfügbaren Karten (wird über die OperationGetCardsdes
Konnektorsermittelt) nach der Karte mit dem passenden
Verschlüsselungszertifikat (unter Verwendung der
OperationReadCardCertificatedes Konnektors) durchsuchen. **[\<=]**

**KOM-LE-A_2061 - Speichern von Zuordnungen im Cache beim Entschlüsseln**

Wird beim Entschlüsseln die erforderliche Karte (SM-B bzw. HBA) unter
Verwendung der OperationReadCardCertificatedes Konnektors ermittelt, MUSS das
Clientmodul die zu dieser Karte korrespondierende Zuordnung von E-Mail-Adresse
des Empfängers, Zertifikats-ID und ICCSN im Cache speichern. **[\<=]**

**KOM-LE-A_2062 - Abbrechen des Entschlüsseln, wenn die erforderliche Karte
nicht verfügbar ist**

Das Clientmodul MUSS die Entschlüsselung einer Nachricht abbrechen, wenn die
für die Entschlüsselung erforderliche Karte (SM-B bzw. HBA) nicht verfügbar
ist. **[\<=]**

**KOM-LE-A_2063 - Abbrechen des Entschlüsseln, wenn Freischaltung der
erforderlichen Karte fehlschlägt**

Das Clientmodul MUSS die Entschlüsselung einer Nachricht abbrechen, wenn die
Freischaltung der für die Entschlüsselung erforderlichen Karte fehlschlägt. **[\<=]**

### 4 Nichtfunktionale Anforderungen

In diesem Kapitel werden nichtfunktionale Anforderungen an das
KOM-LE-Clientmodul definiert.

### 4.1 Transportsicherung

Beim Senden bzw. Empfangen von Nachrichten baut das Clientmodul mit folgenden
Systemen Verbindungen auf:

 ---> UL

In diesem Kapitel werden die Anforderungen an den Aufbau der TLS-Verbindungen
mit diesen Systemen definiert.

### 4.1.1 Allgemeine Festlegungen

Die Vorgaben zu X.509-Identitäten für die TLS/SSL-Authentifizierung,
unterstützten TLS-Versionen und TLS Cipher Suites werden aus [gemSpec_Krypt]
übernommen.

**KOM-LE-A_2064-02 - Verwendung von X.509-Identitäten bei der
TLS-Authentifizierung**

Das Clientmodul KOM-LE MUSS bei der Verwendung von X.509-Identitäten für die
TLS-Authentifizierung sowie dem Aufbau von TLS-Verbindungen die Vorgaben aus
[gemSpec_Krypt] beachten. Hierbei sind zusätzlich auch Cipher-Suites und
Kurven aus [BSI-TR-02102-2]  Kapitel 3.3 akzeptabel um Kompatibilität mit
gängigen Clientsystemen und PVSen bzw. Mailclients, sowie gängigen
Plattformen für Fachdienste sicherzustellen. **[\<=]**

Der Aufbau von TLS-Verbindungen mit Clientsystemen oder die zertifikatsbasierte
clientseitige Authentisierung beim Aufbau von TLS-Verbindungen mit dem
Konnektor oder den Fachdiensten erfordert das Vorhandensein des entsprechenden
Schlüsselmaterials.

Üblicherweise liegt ein Zertifikat zusammen mit dem zugehörigen geheimen
Schlüssel in einem standardisierten und passwortgeschützten Format (p12)
[PKCS#12] vor. Das Clientmodul kann ein Zertifikat und den zugehörigen
geheimen Schlüssel auf mindestens zwei Arten nutzen:

 ---> OL

**A_17239 - ECC-Migration, Unterstützung verschiedener kryptografischer
Verfahren bei der TLS-Verwendung**

Das Clientmodul KOM-LE MUSS parallel RSA und ECC unterstützen. Als TLS-Client
MUSS das Clientmodul KOM-LE  bevorzugt ECC verwenden, falls es auf einen
TLS-Server, der beide Verfahren unterstützt, trifft. **[\<=]**

**KOM-LE-A_2065 - Schutz des Schlüsselspeichers für TLS-Verbindungen**

Das Clientmodul MUSS das für den Aufbau von TLS-Verbindungen mit dem
Fachdienst, dem Konnektor und Clientsystemen benötigte Schlüsselmaterial in
einem mindestens durch Passwort geschützten sicheren Schlüsselspeicher
ablegen. **[\<=]**

Lösungen die Zertifikat und Schlüsselmaterial in der ausgelieferten Software
des Clientmoduls enthalten und Lösungen bei denen derselbe Schlüssel für
mehrere Clientmodule verwendet wird, sind aus Sicherheitsgründen nicht
zulässig.

**KOM-LE-A_2300 - Import des Schlüsselmaterial für TLS-Verbindungen**

Das Clientmodul DARF Schlüsselmaterial für den Aufbau von TLS-Verbindungen
NICHT im Auslieferungszustand in der Software enthalten, sondern muss dieses
nach Installation importieren. **[\<=]**

**KOM-LE-A_2301-02 - Individuelles Schlüsselmaterial für TLS-Verbindungen**

Das Clientmodul MUSS das vom KOM-LE-Anbieter bereitgestellte Schlüsselmaterial
in Form der PKCS#12 Datei für jeden Aufbau von TLS-Verbindungen nutzen. Das
Clientmodul MUSS das notwendige Schlüsselmaterial über die Schnittstelle
I_AccountManager_Service vom KOM-LE-Fachdienst beziehen. **[\<=]**

**A_18783 - Import Schlüssel und Zertifikat als PKCS#12 Datei**

Das Clientmodul KOM-LE MUSS das Schlüsselmaterial und das Zertifikat für die
TLS-Verbindungen als passwortgeschützte PKCS#12 Datei importieren können.
**[\<=]**

### 4.1.2 Transportsicherung zwischen Clientsystem und Clientmodul

Die SMTP- und POP3-Verbindungen zwischen dem Clientmodul und den Clientsystemen
müssen über TLS geschützt werden, sofern Clientmodul und E-Mail-Client nicht
auf demselben PC laufen.

**KOM-LE-A_2066 - Verwendung von TLS für SMTP-Verbindungen mit Clientsystemen**

Für SMTP-Verbindungen zwischen Clientsystem und Clientmodul MUSS TLS verwendet
werden, wenn das Clientmodul nicht auf demselben Gerät läuft wie das
Clientsystem. **[\<=]**

**KOM-LE-A_2067 - Verwendung von TLS für POP3-Verbindungen mit Clientsystemen**

Für POP3-Verbindungen zwischen Clientsystem und Clientmodul MUSS TLS verwendet
werden, wenn das Clientmodul nicht auf demselben Gerät läuft wie das
Clientsystem. **[\<=]**

**KOM-LE-A_2181 - Authentifizierung von Clientsystemen gegenüber dem
Clientmodul**

DasClientmodul MUSSfür den Aufbau von TLS-Verbindungen mit den Clientsystemen
sowohl die Möglichkeit, die zertifikatsbasierte Clientauthentifizierung zu
verwenden, als auch ohne Clientauthentifizierung zu arbeiten, unterstützen. **[\<=]**

Die Server-Authentisierung erfolgt mit einem Zertifikat, das im gemäß
KOM-LE_2065 geschützten Schlüsselspeicher gespeichert wird.

### 4.1.3 Transportsicherung zwischen Clientmodul und Konnektor

Die Kommunikation zwischen Clientmodul und Konnektor basiert auf HTTP. Der
Konnektor bietet vier Varianten der HTTP(S)-Verbindung an:

 ---> OL

Für die Basic-Authentifizierung (auch “Basic Access Authentication”, ein
Standard der HTTP-Authentifizierung) soll dabei das Clientmodul die notwendigen
Parameter „Benutzername“ und „Passwort“ verwalten. Das Clientmodul muss
über entsprechende Konfigurationsparameter verfügen. Diese müssen mit den
gleichen Werten für Benutzername und Passwort befüllt werden, wie an der
Managementschnittstelle des Konnektors.

Die zertifikatsbasierte Client-Authentifizierung erfolgt mit einem Zertifikat,
das im gemäß KOM-LE-A_2065 passwortgeschützten Schlüsselspeicher
gespeichert wird.

**KOM-LE-A_2070 - Verbindungsaufbau mit dem Konnektor mit TLS**

Das Clientmodul MUSS für Verbindungen mit dem Konnektor immer TLS verwenden. **[\<=]**

**KOM-LE-A_2071 - TLS-Verbindung mit dem Konnektor mit oder ohne
zertifikatsbasierter Client-Authentifizierung**

Das Clientmodul MUSSkonfigurierbardie Verwendung von TLS mit oder
ohnezertifikatsbasierter Client-Authentifizierung für Verbindungen
mitdemKonnektorermöglichen.Standardmäßig muss die zertifikatsbasierte
Client-Authentifizierungaktiviert sein. **[\<=]**

**KOM-LE-A_2072 - Verwendung von HTTP-Basic-Authentifizierung für
TLS-Verbindungen mit dem Konnektor**

Das Clientmodul MUSSkonfigurierbardie Verwendung von
HTTP-Basic-Authentifizierungin einemTLS-Kanalfür Verbindungen mitdemKonnektor
ermöglichen. **[\<=]**

**A_21223-01 - Verbindungen mit dem Konnektor bei LDAP**

Bei der Verwendung des LDAP-Proxies im Konnektor MUSS das Clientmodul die
Vorgaben aus [gemSpec_Kon#3.4] erfüllen.Die folgenden Vorgaben sind
einzuhalten:

 ---> OL

**[\<=]**

### 4.1.4 Transportsicherung zwischen Clientmodul und Fachdienst

Die Verbindungen zwischen KOM-LE-Clientmodul und KOM-LE-Fachdiensten (inklusive
KAS) erfolgen immer über TLS. Der TLS Handshake zwischen dem Clientmodul und
dem MTA sowie POP3-Server findet unmittelbar nach dem Aufbau der entsprechenden
TCP-Verbindung statt. Damit wird sichergestellt, dass die Anmeldungsdaten des
Nutzers immer über die mit TLS geschützte Verbindung transportiert werden.

Während des Aufbaus der TLS-Verbindung authentifizieren sich die
KOM-LE-Fachdienste bzw. der Verzeichnisdienst  gegenüber dem Clientmodul mit
X.509 TLS-Server-Zertifikaten. Zur Überprüfung dieser Zertifikate verwendet
das Clientmodul die OperationVerifyCertificatedes Konnektors.

Das Clientmodul wiederum authentisiert sich gegenüber den KOM-LE-Fachdiensten
mit dem vom KOM-LE-Anbieter zur Verfügung gestellten TLS-Client-Zertifikat und
dem entsprechenden privaten Schlüssel (KOM-LE-A_2065, KOM-LE-A_2300 und
KOM-LE-A_2301 sind zu beachten).

**KOM-LE-A_2074 - Verbindung zu KOM-LE-Fachdiensten immer über TLS**

Das Clientmodul MUSS immer TLSmit beidseitiger Authentifizierung über
X.509-Zertifikate aus der PKI der TI-Plattformfür die Verbindung mit
denKOM-LE-Fachdiensten verwenden.Das TLS-HandshakeMUSSunmittelbar nach dem
Aufbau der TCP-Verbindung initiiertwerden. **[\<=]**

**KOM-LE-A_2075-01 - Prüfung von TLS-Server-Zertifikaten**

Das Clientmodul MUSS für die Prüfung von TLS-Server-Zertifikaten der
KOM-LE-Fachdienste die Operation VerifyCertificate des Konnektors benutzen.
Wird durch die Operation ein Prüfergebnis "INVALID" zurückgegeben, MUSS der
beabsichtigte Verbindungsaufbau abgebrochen werden. **[\<=]**

**A_22348 - Caching der Prüfergebnisse der TLS-Server-Zertifikate**

Das Clientmodul KANN das Ergebnisse der Zertifikatsprüfung für eine definierte
Zeitdauer (Tabelle 15: Tab_Konf_Param Standardkonfiguration allgemeine
Parameter) temporär und manipulationssicher speichern. Für die Zuordnung sind
eindeutige Identifikatoren, wie bspw. der Zertifikats-Fingerabdruck, zu
verwenden. Bei erneuter Prüfung eines gleichen Zertifikats kann das
vorangegangene Verifikations-Ergebnis dieses Zertifikats genutzt werden. Die
Speicherdauer ist an die zeitliche Gültigkeit ("notAfter") des Zertifikats
anzupassen. **[\<=]**

**KOM-LE-A_2182-01 - Verwendung des vom KOM-LE-Anbieter zur Verfügung
gestellten Zertifikats für die clientseitige TLS-Authentifizierung**

Das Clientmodul MUSS sich mit dem vom KOM-LE-Anbieter zur Verfügung gestellten
TLS-Client-Zertifikat C.CM.TLS-CS gegenüber den KOM-LE-Fachdienst-Komponenten
authentifizieren. **[\<=]**

### 4.2 Nutzung von Webservice-Schnittstellen des Konnektors

Aus der Herstellerdokumentation des Konnektors ist der FQDN zu entnehmen, unter
dem der Konnektor seinen Dienstverzeichnisdienst anbietet. Innerhalb des FQDN
können Hostname und Domain-Name je nach Konfiguration der LE-Umgebung
individuell konfiguriert sein. Der resultierende FQDN des
Dienstverzeichnisdienstes muss in die Konfiguration des Clientmoduls
übernommen werden.

Durch das Auslesen des Dienstverzeichnisdienstes erhält das Clientmodul
Webservice-Endpunkte von Diensten des Konnektors. Die Dienste des Konnektors
sind versioniert. Es ist möglich, dass ein Konnektor mehrere Versionen eines
Dienstes gleichzeitig anbietet. Die Versionierung der Dienste hilft dem
Clientmodul dabei, genau die Dienstversionen zu nutzen, die es clientseitig
implementiert hat.

Da nicht davon ausgegangen werden kann, dass die Inhalte des
Dienstverzeichnisdienstes statisch sind, sollte das Lesen des Verzeichnisses
beim Programmstart und in Fehlersituationen erfolgen, um den
Dienstverzeichnis-Cache zu erneuern. Die weitere Kommunikation mit den Diensten
des Konnektors erfolgt dann über die im Dienstverzeichnis-Cache propagierten
Dienstendpunkte.

**KOM-LE-A_2076 - Ermittlung der Serviceendpunkte des Konnektors**

Das Clientmodul MUSS die Endpunkte der Services, die der Konnektor anbietet, aus
dem Dienstverzeichnisdienst (DVD)ermittelnund die Endpunktinformationen der
Dienste lokal cachen.Der DVD istunter einem FQDN,derim Clientmodul konfiguriert
ist, erreichbar.Wenn ein Verbindungsproblem auftritt (Dienst nicht
erreichbar),MUSSdas Clientmodul einen Refresh auf die Endpunktinformationen des
Dienstverzeichnisdienstes durchführen. **[\<=]**

**KOM-LE-A_2077 - Auswahl der unterstützten Version einer Dienstschnittstelle
des Konnektors**

Das Clientmodul MUSS in der Lage sein, die von ihm unterstützte Dienstversion
unter mehreren vom Konnektor angebotenen Dienstschnittstellen auszuwählen. **[\<=]**

### 4.3 Protokollierung/Logging

Das Clientmodul soll Protokolldateien schreiben, die eine Analyse technischer
Vorgänge erlauben. Diese Protokolldateien sind dafür vorgesehen, aufgetretene
Fehler zu identifizieren, die Performance zu analysieren und interne Abläufe
zu beobachten. Um die Anforderungen an den Datenschutz zu gewährleisten,
dürfen keine medizinischen und personenbezogenen Daten protokolliert werden.
Geheimes Schlüsselmaterial darf ebenfalls nicht protokolliert werden.

**KOM-LE-A_2079 - Protokolldateien für Ablauf, Performance und Fehler**

Das Clientmodul MUSS das Protokollieren von Abläufen, Performanceinformationen
und Fehlern ermöglichen. **[\<=]**

**KOM-LE-A_2080 - Keine Protokollierung sensibler Daten**

Das Clientmodul DARF medizinischeundpersonenbezogene Datensowie geheimes
Schlüsselmaterialund PasswörterNICHT protokollieren. **[\<=]**

Die Protokolldateien folgen einem einheitlichen Format, das vom Hersteller
festgelegt wird. Es muss geeignet sein, automatische Auswertungen mit wenig
Aufwand durch Dritte zu ermöglichen. Ein Vorbild ist das Weblog des Apache
Webservers.

**KOM-LE-A_2081 - Format der Protokolldateien**

DasKOM-LE-ClientmodulMUSS Protokolldateien in einem einheitlichenFormat
erstellen, um eine automatisierte Auswertung zu ermöglichen. **[\<=]**

Der Zugriff auf Protokolldateien muss auf autorisierte Personen durch
angemessene technische oder organisatorische Maßnahmen eingeschränkt werden.
Die Logdateien können auf ein separates Speichermedium kopiert werden. Zudem
soll der Administrator das Protokollieren für die Performanceanalyse und der
internen Abläufe einzeln deaktivieren und wieder aktivieren können. Für den
Produktivbetrieb soll das Protokollieren der internen Abläufe grundsätzlich
deaktiviert sein. Damit die Protokolldateien nur begrenzten Speicherplatz
belegen, werden sie automatisch nach einem konfigurierbaren Zeitraum gelöscht
bzw. überschrieben.

**KOM-LE-A_2082 - Zugriff auf Protokolldateien einschränken**

DasKOM-LE-ClientmodulMUSS den Zugriff auf Protokolldateien auf autorisierte
Personen durch angemessene technische oder organisatorische Maßnahmen
einschränken. **[\<=]**

**KOM-LE-A_2083 - Kopien der Protokolldateien**

DasKOM-LE-Clientmodul MUSS autorisiertemPersonal das Anfertigen von Kopien der
Protokolldateien auf separatenSpeichermedien ermöglichen. **[\<=]**

**KOM-LE-A_2084 - Aktivierung und Deaktivierung der Protokollierung von
Performanceinformationen**

DasKOM-LE-ClientmodulMUSS das Aktivieren und Deaktivierender Protokollierung von
Performanceinformationen ermöglichen. **[\<=]**

**KOM-LE-A_2085 - Begrenzung des Speicherplatzes für Protokolldateien**

DasKOM-LE-ClientmodulMUSS den verwendeten Speicherplatz für die
Protokolldateien begrenzen, indem diese automatisch nach einem konfigurierbaren
Zeitraum gelöscht oder überschrieben werden. **[\<=]**

Um mehrere Protokolleinträge zu korrelieren, soll beim Aufruf einer Operation
eine Vorgangsnummer gebildet werden. Diese Vorgangsnummer wird in allen
Protokolleinträgen dieses Operationsaufrufs genutzt. Die Vorgangsnummer wird
vom KOM-LE-Clientmodul pseudozufällig gebildet.

**KOM-LE-A_2086 - Vorgangsnummer für Protokolleinträge**

DasKOM-LE-ClientmodulMUSS eine Vorgangsnummer beimAufruf einer
Operationpseudozufälligbilden, um alle zugehörigen Protokolleinträge zum
Operationsaufruf zu korrelieren. **[\<=]**

### 4.3.1 Ablaufprotokoll

Die Protokolleinträge im Ablaufprotokoll enthalten mindestens die in Tabelle
Tab_Felder_Ablauf_Prot aufgezählten Felder.

<table><tr><th>
Feld

</th><th>
Beschreibung

</th></tr><tr><td>
Vorgangsnummer

</td><td>
Pseudo-zufällige Zeichenkette zur Korrelation der Protokolleinträge

</td></tr><tr><td>
Zeitpunkt

</td><td>
Zeitpunkt der Erstellung des Protokolleintrags

</td></tr><tr><td>
Beschreibung

</td><td>
Details zum Ausführungsschritt

</td></tr></table>

Das Ablaufprotokoll soll die Ausführungsschritte enthalten, die einen Einblick
in den internen Ablauf für Administratoren, Anbieter und Tester ermöglichen
und die Analyse von Fehlersituationen erleichtern.

**KOM-LE-A_2087 - Felder zur Protokollierung des Ablaufs**

Das KOM-LE-Clientmodul MUSS die Protokollierung des Ablaufs mit mindestens
folgenden Feldern ermöglichen:

 ---> UL

**[\<=]**

### 4.3.2 Performance

Die Protokolleinträge im Performanceprotokoll enthalten mindestens die in
Tabelle Tab_Felder_Perf_Prot aufgezählten Felder und müssen geeignet sein, um
die tatsächlichen Ausführungszeiten des KOM-LE-Clientmoduls mit den Vorgaben
in Kapitel 4.6.1 zu vergleichen. Für jeden Aufruf einer Schnittstelle des
Clientmoduls KOM-LE werden ein oder mehrere Protokolleinträge geschrieben.

<table><tr><th>
Feld

</th><th>
Beschreibung

</th></tr><tr><td>
Vorgangsnummer

</td><td>
Pseudozufällige Zeichenkette zur Korrelation der Protokolleinträge

</td></tr><tr><td>
Name der Aktion

</td><td>
Name der Aktion für Protokolleintrag

</td></tr><tr><td>
Startzeitpunk

</td><td>
Startzeitpunkt der Aktion

</td></tr><tr><td>
Endezeitpunkt

</td><td>
Endezeitpunkt der Aktion

</td></tr><tr><td>
Dauer in ms

</td><td>
Dauer in ms

</td></tr></table>

**KOM-LE-A_2088 - Felder zur Protokollierung der Performance**

Das KOM-LE-Clientmodul MUSS die Protokollierung der Performance mit mindestens
folgenden Feldern ermöglichen:

 ---> UL

**[\<=]**

Jede der in Tabelle Tab_Auslöser_Prot_Entry aufgelisteten Aktionen führt zu
einem Eintrag im Performanceprotokoll. Diese Durchlaufzeiten sollen separat
protokolliert werden, damit die Ausführungszeit des Clientmoduls ohne Zeiten
anderer Komponenten ermittelbar ist.

<table><tr><th>
Auslöser

</th><th>
Name der Aktion für Protokolleintrag

</th><th>
Beschreibung

</th></tr><tr><td>
Ankommen einer SMTP bzw. POP3-Meldung

</td><td>
SMTP bzw. POP3-Meldung

</td><td>
Wird beim Ankommen einer SMTP bzw. POP3-Meldung ausgelöst und endet mit der
Weiterleitung an den Fachdienst oder der Antwort an das Clientsystem.

</td></tr><tr><td>
Aufruf einer Operation des Konnektors

</td><td>
Name der Operation

</td><td>
Wird durch den Aufruf einer Operation des Konnektors ausgelöst und endet mit
der Rückkehr der Aktion

</td></tr></table>

**KOM-LE-A_2089 - Aktionen zur Protokollierung der Performance**

Das KOM-LE-Clientmodul MUSS für die folgenden Aktionen Einträge in das
Performanceprotokoll schreiben:

 ---> UL

**[\<=]**

### 4.3.3 Fehler

Tritt innerhalb einer Operation ein Fehler auf bzw. wird eine Operation nicht
beendet, soll trotzdem ein Protokolleintrag erstellt werden, in dem eindeutig
auswertbar ist, dass die Ausführung der Operation fehlerhaft war.

Die Protokolleinträge im Fehlerprotokoll enthalten mindestens die in Tabelle
Tab_Felder_Fehler_Prot aufgezählten Felder.

<table><tr><th>
Feld

</th><th>
Beschreibung

</th></tr><tr><td>
Vorgangsnummer

</td><td>
Pseudozufällige Zeichenkette zur Korrelation der Protokolleinträge

</td></tr><tr><td>
Zeitpunkt

</td><td>
Zeitpunkt der Erstellung des Protokolleintrags

</td></tr><tr><td>
Fehlerdetails

</td><td>
Weiterführende Details zur Fehlermeldung

</td></tr></table>

**KOM-LE-A_2090 - Felder zur Protokollierung der Fehler**

Das KOM-LE-Clientmodul MUSS die Protokollierung von Fehlern mit mindestens
folgenden Feldern ermöglichen:

 ---> UL

**[\<=]**

### 4.4 Konfiguration

Die in der Tabelle Tab_Konf_Param aufgeführten Parameter müssen über eine
Managementoberfläche oder eine Konfigurationsdatei für das KOM-LE-Clientmodul
konfigurierbar sein.

<table><tr><th>
Parameter

</th><th>
Beschreibung des Parameters

</th><th>
Defaultwert

</th></tr><tr><td>
TLS_AUTH_KONNEKTOR

</td><td>
Authentifizierung des Clientmoduls gegenüber dem Konnektor bei aktivierter
TLS-Verbindung (zertifikatsbasiert, Basic-Authentifizierung, ohne)

</td><td>
zertifikats-basiert

</td></tr><tr><td>
KONNEKTOR_TIMEOUT

</td><td>
Timeout für Aufrufe von  Schnittstellen des Konnektors

</td><td>
1 Minute    

</td></tr><tr><td>
SMTP_TIMEOUT_SERVER

</td><td>
Timeout für Antworten vom SMTP-Server auf SMTP-Kommandos

</td><td>
5 Minuten

</td></tr><tr><td>
SMTP_TIMEOUT_CLIENT

</td><td>
Timeout für das Warten auf neue SMTP-Kommandos vom Clientsystem

</td><td>
5 Minuten

</td></tr><tr><td>
POP3_TIMEOUT_SERVER

</td><td>
Timeout für Antworten vom POP3-Server auf POP3-Kommandos

</td><td>
5 Minuten

</td></tr><tr><td>
POP3_TIMEOUT_CLIENT

</td><td>
Timeout für das Warten auf neue POP3-Kommandos vom Clientsystem

</td><td>
5 Minuten

</td></tr><tr><td>
TTL_ENC_CERT

</td><td>
Time to Live für gecachte Verschlüsselungs-zertifikate und Prüfergebnisse

</td><td>
12 Stunden

</td></tr><tr><td>
TTL_EMAIL_ICCSN

</td><td>
Time to Live für gecachte Zuordnungen von E-Mail-Adressen der Sender bzw.
Empfänger zu ICCSNs von deren HBAs/SM-Bs

</td><td>
30 Tage

</td></tr><tr><td>
TTL_PROTS

</td><td>
Time to Live für Protokolldateien.

</td><td>
30 Tage

</td></tr><tr><td>
PROT_PERF

</td><td>
Protokolldatei für Performance

</td><td>
JA

</td></tr><tr><td>
KONNEKTOR_URI

</td><td>
URI des DVD des Konnektors

</td><td>
-

</td></tr><tr><td>
CM_KAS_TIMEOUT

</td><td>
Timeout bei Inaktivität der Kommunikation zwischen Clientmodul und KAS

</td><td>
30 Sekunden

</td></tr></table>

**KOM-LE-A_2091-01 - Konfigurationsparameter**

Das KOM-LE-Clientmodul MUSS die in Tabelle Tab_Konf_Param aufgelisteten
Parameter ausschließlich dem berechtigten Akteur über eine
Managementoberfläche oder eine Konfigurationsdatei zur Konfiguration anbieten.
**[\<=]**

**KOM-LE-A_2184 - Standardwerte der Konfigurationsparameter**

Die Konfiguration des Clientmoduls MUSS mit den in TabelleTab_Konf_Param
Standardkonfiguration allgemeine Parameterdefinierten Defaultwerten
ausgeliefert werden. **[\<=]**

### 4.5 Update-Mechanismen

**KOM-LE-A_2225 - Update-Mechanismen**

Der Hersteller des Clientmoduls MUSS Mechanismen für das Updaten des
Clientmoduls zur Verfügung stellen. Diese Mechanismen MÜSSEN es auch
ermöglichen, dass die TLS-Zertifikate und das zugehörige Schlüsselmaterial
des Clientmoduls auf sichere Art und Weise erneuert werden können. **[\<=]**

### 4.6 Produktleistungen

### 4.6.1 Performance

Die durch das Clientmodul einzuhaltenden Performanceanforderungen werden in
diesem Dokument nicht betrachtet sondern in [gemSpec_Perf] aufgeführt.

### 4.6.2 Skalierbarkeit

Das Clientmodul kann in Einzelpraxen, Praxisgemeinschaften, Gemeinschaftspraxen
oder in medizinischen Versorgungszentren (MVZ) eingesetzt werden. Zusätzlich
ist der Einsatz in Krankenhäusern und Umgebungen der Kostenträger vorgesehen.
In diesen Umgebungen sind gleichzeitige Sende- und Abholvorgänge möglich. Das
Clientmodul muss in der Lage sein, solche Vorgänge parallel bearbeiten zu
können.

Im Rahmen dieser Spezifikation wird gefordert, dass ein KOM-LE-Clientmodul
grundsätzlich beliebig viele parallele Sende- und Abholvorgänge unterstützt.
Die Anzahl der tatsächlich unterstützten parallelen Aufrufe wird durch die
eingesetzte Hardware und Beschränkungen des Herstellers begrenzt.

**KOM-LE-A_2094 - Skalierbarkeit**

Das Clientmodul MUSS gleichzeitig für mehrere Clientsysteme nutzbar sein, wobei
die Anzahl der tatsächlich unterstützten parallelen Aufrufe dem Hersteller
überlassen ist. **[\<=]**

### 5 Anhang A – Verzeichnisse

### 5.1 Abkürzungen

<table><tr><th>
Kürzel

</th><th>
Erläuterung

</th></tr><tr><td>
AUTH

</td><td>
Authentisierung

</td></tr><tr><td>
CMS

</td><td>
Cryptographic Message Syntax

</td></tr><tr><td>
DER

</td><td>
Distinguished Encoding Rules

</td></tr><tr><td>
DVD

</td><td>
Dienstverzeichnisdienst

</td></tr><tr><td>
FQDN

</td><td>
Fully Qualified Domain Name

</td></tr><tr><td>
HBA

</td><td>
Heilberufsausweis

</td></tr><tr><td>
ICCSN

</td><td>
Integrated Circuit Card Serial Number

</td></tr><tr><td>
ID

</td><td>
Identifier

</td></tr><tr><td>
KAS

</td><td>
KOM-LE Attachment Service

</td></tr><tr><td>
KOM-LE

</td><td>
Kommunikation für Leistungserbringer

</td></tr><tr><td>
LDAP

</td><td>
Leightweight Directory Access Protocol

</td></tr><tr><td>
LE

</td><td>
Leistungserbringer

</td></tr><tr><td>
MTA

</td><td>
Mail Transfer Agent

</td></tr><tr><td>
MUA

</td><td>
Mail User Agent

</td></tr><tr><td>
OCSP

</td><td>
Online Certificate Status Protocol

</td></tr><tr><td>
PIN

</td><td>
Personal Identification Number

</td></tr><tr><td>
POP3

</td><td>
Post Office Protocol Version 3

</td></tr><tr><td>
S/MIME

</td><td>
Secure/Multipurpose Internet Mail Extensions

</td></tr><tr><td>
SMTP

</td><td>
Simple Mail Transfer Protocol

</td></tr><tr><td>
SSL

</td><td>
Secure Socket Layer

</td></tr><tr><td>
TCP

</td><td>
Transmission Control Protocol

</td></tr><tr><td>
TI

</td><td>
Telematikinfrastruktur

</td></tr><tr><td>
TLS

</td><td>
Transport Layer Security

</td></tr><tr><td>
URL

</td><td>
Uniform Resource Locator

</td></tr><tr><td>
VZD

</td><td>
Verzeichnisdienst

</td></tr></table>

### 5.2 Glossar

Das Glossar wird als eigenständiges Dokument (vgl. [gemGlossar]) zur Verfügung
gestellt.

### 5.3 Abbildungsverzeichnis

- [Abbildung-1] - Abb_Dok_Hierarchie Dokumentenhierarchie KOM-LE
- [Abbildung-2] - Abb_KOMLE_Komp KOM-LE-Komponenten
- [Abbildung-3] - Abb_Struk_KOMLE_Msg Struktur einer KOM-LE-Nachricht
- [Abbildung-4] - Administrationsmodul für die Kommunikation mit dem Account Manager
- [Abbildung-5] - Abb_Send_Msg Senden von Nachrichten
- [Abbildung-6] - Abb_State_CM_Send Zustände Clientmodul beim Senden von Nachrichten
- [Abbildung-7] - Abb_MTA_Nutzername Format des SMTP- Benutzernamens
- [Abbildung-8] - Abb_Sig_Verschl Signieren und Verschlüsseln entsprechend S/MIME Profil
- [Abbildung-9] - Abb_Verschl_Msg Verschlüsselung einer Nachricht
- [Abbildung-10] - Abb_Empfangen_Msg Empfangen von Nachrichten
- [Abbildung-11] - Abb_Status_CM_Empfang Zustände Clientmodul beim Nachrichtenempfang
- [Abbildung-12] - Abb_POP3_Nutzer_Name Format des POP3- Benutzernamens
- [Abbildung-13] - Abb_Zugriff_SMB SM-B-Zugriff zur Erstellung der Nachrichtensignatur
- [Abbildung-14] - Abb_Zugriff_SMB_HBA SM-B/HBA-Zugriff zur Nachrichtentschlüsselung

### 5.4 Tabellenverzeichnis

- [Tabelle-#] - Tab_Fehlercodes_KOMLE-Clientmodule
- [Tabelle-1] - KIM-Attachment-Datenstruktur
- [Tabelle-2] - Tab_Fehlertext_Download Fehlertext beim Download von Anlagen
- [Tabelle-3] - Tab_SMTP_Ant_Init Antworten Clientmodul im CONNECT-Zustand
- [Tabelle-4] - Tab_SMTP_Verbindung SMTP-Antwortcodes für MTA-Verbindungsaufbau
- [Tabelle-5] - Tab_POP3_Ant_Init Antworten Clientmodul im CONNECT-Zustand
- [Tabelle-6] - Tab_POP3_Verbindung Antwortcodes für POP3-Server-Verbindungsaufbau
- [Tabelle-#] - Tab_Fehlertext_Entschl Fehlertexte für Entschlüsselungsfehler
- [Tabelle-7] - Tab_Verm_Sig_Prüf Vermerke mit Ergebnissen der Signaturprüfung
- [Tabelle-8] -  Tab_Header_Kat Header-Feld Kategorie
- [Tabelle-9] - Tab_Felder_Ablauf_Prot Felder im Ablaufprotokoll
- [Tabelle-10] - Tab_Felder_Perf_Prot Felder im Performance-Protokoll
- [Tabelle-11] - Tab_Auslöser_Prot_Entry Auslöser Protokolleinträge im Performanceprotokoll
- [Tabelle-12] - Tab_Felder_Fehler_Prot Felder im Fehlerprotokoll
- [Tabelle-13] - Tab_Konf_Param Standardkonfiguration allgemeine Parameter

### 5.5 Referenzierte Dokumente

### 5.5.1 Dokumente der gematik

Die nachfolgende Tabelle enthält die Bezeichnung der in dem vorliegenden
Dokument referenzierten Dokumente der gematik zur Telematikinfrastruktur. Der
mit der vorliegenden Version korrelierende Entwicklungsstand dieser Konzepte
und Spezifikationen wird pro Release in einer Dokumentenlandkarte definiert;
Version und Stand der referenzierten Dokumente sind daher in der nachfolgenden
Tabelle nicht aufgeführt. Deren zu diesem Dokument jeweils gültige
Versionsnummer entnehmen Sie bitte der aktuellen, auf der Internetseite der
gematik veröffentlichten Dokumentenlandkarte, in der die vorliegende Version
aufgeführt wird.

<table><tr><th>
[Quelle]

</th><th>
Herausgeber: Titel

</th></tr><tr><td>
[gemGlossar]

</td><td>
gematik: Glossar der Telematikinfrastruktur

</td></tr><tr><td>
[gemLH_KOM-LE]

</td><td>
gematik: Lastenheft Adressierte Kommunikation Leistungserbringer

</td></tr><tr><td>
[gemSpec_FD_KOMLE]

</td><td>
gematik: Spezifikation Fachdienst KOM-LE

</td></tr><tr><td>
[gemSpec_Kon]

</td><td>
gematik: Spezifikation Konnektor

</td></tr><tr><td>
[gemSpec_Krypt]

</td><td>
gematik: Verwendung kryptographischer Algorithmen in der Telematikinfrastruktur

</td></tr><tr><td>
[gemSpec_PKI]

</td><td>
gematik: Spezifikation PKI

</td></tr><tr><td>
[gemSMIME_KOMLE]

</td><td>
gematik: KOM-LE S/MIME Profil 1.0

</td></tr><tr><td>
[gemSysL_KOMLE]

</td><td>
gematik: Systemspezifisches Konzept KOM-LE

</td></tr><tr><td>
[AccountManager.yaml]

</td><td>
gematik: https://github.com/gematik/api-kim/blob/master/src/openapi/AccountManager.yaml 

</td></tr><tr><td>
[Attachment_Schema]

</td><td>
gematik:

https://github.com/gematik/api-kim/blob/master/src/schema/Attachment_schema.json

</td></tr></table>

### 5.5.2 Weitere Dokumente

<table><tr><th>
[Quelle]

</th><th>
Herausgeber (Erscheinungsdatum): Titel

</th></tr><tr><td>
[RFC1123]

</td><td>
RFC: Requirements for Internet Hosts -- Application and Support

</td></tr><tr><td>
[RFC1939]

</td><td>
RFC 1939: Post Office Protocol – Version 3, J. Myers, M. Rose, Mai 1996

</td></tr><tr><td>
[RFC2045]

</td><td>
RFC 2045: Multipurpose Internet Mail Extension (MIME) Part One: Format of
Internet Message Bodies, N. Freed, N. Borenstein, November 1996

</td></tr><tr><td>
[RFC2046]

</td><td>
RFC 2046: Multipurpose Internet Mail Extension (MIME) Part Two: Media Types, N.
Feed, N. Borenstein, November 1996

</td></tr><tr><td>
[RFC2449]

</td><td>
RFC 2449: POP3 Extension Mechanism, R. Gellens, C. Newman, L. Lundblade,
November 1998

</td></tr><tr><td>
[RFC2822]

</td><td>
RFC 2822: Internet Message Format

</td></tr><tr><td>
[RFC3463]

</td><td>
RFC 3463: Enhanced Mail System Status Codes, G. Vaudreuil, Januar 2003

</td></tr><tr><td>
[RFC4616]

</td><td>
RFC 4616: The PLAIN Simple Authentication and Security Layer (SASL) Mechanism,
K. Zeilenga, August 2006

</td></tr><tr><td>
[RFC4954]

</td><td>
RFC 4954: SMTP Service Extension for Authentication, R. Siemborski, A. Melnikov,
März 2007

</td></tr><tr><td>
[RFC5321]

</td><td>
RFC 5321: Simple Mail Transfer Protocol, J. Klensin, Oktober 2008

</td></tr><tr><td>
[RFC5322]

</td><td>
RFC 5322: Internet Message Format, P. Resnick, Ed., Oktober 2008

</td></tr><tr><td>
[RFC5750]

</td><td>
RFC 5750: Secure/Multipurpose Internet Mail Extensions (S/MIME) Version 3.2
Certificate Handiling, B. Ramsdell, S. Turner, Januar 2010

</td></tr><tr><td>
[RFC5751]

</td><td>
RFC 5751: Secure/Multipurpose Internet Mail Extensions (S/MIME) Version 3.2
Message Specification, B. Ramsdell, S. Turner, Januar 2010

</td></tr></table>





[Dokumentinformationen]: #dokumentinformationen
[Inhaltsverzeichnis]:    #inhaltsverzeichnis
[1]:                     #1-einordnung-des-dokumentes
[1.1]:                   #11-zielsetzung
[1.2]:                   #12-zielgruppe
[1.3]:                   #13-geltungsbereich
[1.4]:                   #14-arbeitsgrundlagen
[1.5]:                   #15-abgrenzung-des-dokuments
[1.6]:                   #16-methodik
[1.6.1]:                 #161-anforderungen
[1.6.2]:                 #162-diagramme
[1.6.3]:                 #163-nomenklatur
[2]:                     #2-systemüberblick
[3]:                     #3-produktfunktionen
[3.1]:                   #31-allgemeine-anforderungen
[3.2]:                   #32-umgang-mit-großen-anhängen
[3.2.1]:                 #321-senden-von-nachrichten-mit-großen-anhängen
[3.2.2]:                 #322-empfangen-von-nachrichten-mit-großen-anhängen
[3.3]:                   #33-senden-von-nachrichten
[3.3.1]:                 #331-übersicht
[3.3.2]:                 #332-connect-zustand
[3.3.2.1]:               #3321-initialisierung
[3.3.2.2]:               #3322-verbindungsaufbau-mit-mta
[3.3.3]:                 #333-proxy-zustand
[3.3.4]:                 #334-process-zustand
[3.3.4.1]:               #3341-empfang-und-weiterleitung-einer-nachricht
[3.3.4.1.1]:             #33411-bearbeitung-einer-ungeschützten-nachricht
[3.3.4.1.2]:             #33412-bearbeitung-einer-geschützten-kom-le-nachricht
[3.3.5]:                 #335-beispiele
[3.4]:                   #34-empfangen-von-nachrichten
[3.4.1]:                 #341-übersicht
[3.4.2]:                 #342-connect-zustand
[3.4.2.1]:               #3421-initialisierung
[3.4.2.2]:               #3422-verbindungsaufbau-mit-dem-pop3-server
[3.4.3]:                 #343-proxy-zustand
[3.4.4]:                 #344-process-zustand
[3.4.4.1]:               #3441-empfang-und-weiterleitung-einer-nachricht
[3.4.4.2]:               #3442-aufbereitung-einer-nachricht
[3.4.4.2.1]:             #34421-entschlüsselung
[3.4.4.2.2]:             #34422-integritätsprüfung
[3.4.5]:                 #345-beispiele
[3.5]:                   #35-übermittlung-von-kontaktdaten
[3.6]:                   #36-übermittlung-von-e-mail-kategorien
[3.7]:                   #37-administrationsmodul
[3.7.1]:                 #371-allgemeine-anforderungen
[3.7.2]:                 #372-registrierung-kom-le-teilnehmer
[3.7.3]:                 #373-deregistrierung-kom-le-teilnehmer
[3.7.4]:                 #374-download-pkcs#12-kom-le-teilnehmer
[3.8]:                   #38-kryptographischen-schnittstellen-des-konnektors
[3.8.1]:                 #381-erstellung-der-digitalen-signatur-einer-nachricht-mit-einer-sm-b
[3.8.2]:                 #382-prüfung-der-digitalen-signatur-einer-nachricht
[3.8.3]:                 #383-verschlüsselung-einer-nachricht
[3.8.4]:                 #384-entschlüsselung-einer-nachricht-mit-einer-sm-b-bzw-einem-hba
[4]:                     #4-nichtfunktionale-anforderungen
[4.1]:                   #41-transportsicherung
[4.1.1]:                 #411-allgemeine-festlegungen
[4.1.2]:                 #412-transportsicherung-zwischen-clientsystem-und-clientmodul
[4.1.3]:                 #413-transportsicherung-zwischen-clientmodul-und-konnektor
[4.1.4]:                 #414-transportsicherung-zwischen-clientmodul-und-fachdienst
[4.2]:                   #42-nutzung-von-webservice-schnittstellen-des-konnektors
[4.3]:                   #43-protokollierunglogging
[4.3.1]:                 #431-ablaufprotokoll
[4.3.2]:                 #432-performance
[4.3.3]:                 #433-fehler
[4.4]:                   #44-konfiguration
[4.5]:                   #45-update-mechanismen
[4.6]:                   #46-produktleistungen
[4.6.1]:                 #461-performance
[4.6.2]:                 #462-skalierbarkeit
[5]:                     #5-anhang-a-–-verzeichnisse
[5.1]:                   #51-abkürzungen
[5.2]:                   #52-glossar
[5.3]:                   #53-abbildungsverzeichnis
[5.4]:                   #54-tabellenverzeichnis
[5.5]:                   #55-referenzierte-dokumente
[5.5.1]:                 #551-dokumente-der-gematik
[5.5.2]:                 #552-weitere-dokumente
[Abbildung-1]:           gemSpec_CM_KOMLE_V1.13.0.attachments/12530168495840135892.png
[Abbildung-2]:           gemSpec_CM_KOMLE_V1.13.0.attachments/7100822428860025400.png
[Abbildung-3]:           gemSpec_CM_KOMLE_V1.13.0.attachments/6843201451921357209.jpeg
[Abbildung-4]:           gemSpec_CM_KOMLE_V1.13.0.attachments/1080796885240025719.png
[Abbildung-5]:           gemSpec_CM_KOMLE_V1.13.0.attachments/10047724992998041337.emf
[Abbildung-6]:           gemSpec_CM_KOMLE_V1.13.0.attachments/1247252452270032696.emf
[Abbildung-7]:           gemSpec_CM_KOMLE_V1.13.0.attachments/16777837172002567704.png
[Abbildung-8]:           gemSpec_CM_KOMLE_V1.13.0.attachments/526343025665164694.jpeg
[Abbildung-9]:           gemSpec_CM_KOMLE_V1.13.0.attachments/9055980938555232690.emf
[Abbildung-10]:          gemSpec_CM_KOMLE_V1.13.0.attachments/8848582674007134219.png
[Abbildung-11]:          gemSpec_CM_KOMLE_V1.13.0.attachments/12287274127072086798.emf
[Abbildung-12]:          gemSpec_CM_KOMLE_V1.13.0.attachments/677856746205699043.png
[Abbildung-13]:          gemSpec_CM_KOMLE_V1.13.0.attachments/5925077707692217005.emf
[Abbildung-14]:          gemSpec_CM_KOMLE_V1.13.0.attachments/4691757431674851972.emf
[Tbl-001]:               #Tbl-001 (&93834802417840)
[Tbl-002]:               #Tbl-002 (&93834811875464)
[Tabelle-#]:             #Tabelle-# (&93834772234760)
[Tabelle-1]:             #Tabelle-1 (&93834811205896)
[Tabelle-2]:             #Tabelle-2 (&93834781691280)
[Tabelle-3]:             #Tabelle-3 (&93834767994456)
[Tabelle-4]:             #Tabelle-4 (&93834802304240)
[Tabelle-5]:             #Tabelle-5 (&93834798980616)
[Tabelle-6]:             #Tabelle-6 (&93834777667024)
[Tabelle-#]:             #Tabelle-# (&93834781617776)
[Tabelle-7]:             #Tabelle-7 (&93834785709824)
[Tabelle-8]:             #Tabelle-8 (&93834778274600)
[Tabelle-9]:             #Tabelle-9 (&93834799120360)
[Tabelle-10]:            #Tabelle-10 (&93834799145136)
[Tabelle-11]:            #Tabelle-11 (&93834799176928)
[Tabelle-12]:            #Tabelle-12 (&93834775682152)
[Tabelle-13]:            #Tabelle-13 (&93834775755680)
[Tbl-018]:               #Tbl-018 (&93834799985384)
[Tbl-019]:               #Tbl-019 (&93834800092168)
[Tbl-020]:               #Tbl-020 (&93834809688312)
[musterfrau@komle.de]:   mailto:mustermann@komle.de (&93834801559728)
[mustermann@komle.de]:   mailto:mustermann@komle.de (&93834800962624)
[musterfrau@komle.de]:   mailto:musterfrau@komle.de (&93834800967536)
[musterfrau@komle.de]:   mailto:musterfrau@komle.de (&93834800970048)
[musterfrau@komle.de]:   mailto:musterfrau@komle.de (&93834800980288)
[musterfrau@komle.de]:   mailto:musterfrau@komle.de (&93834776404048)
[mustermann@komle.de]:   mailto:mustermann@komle.de (&93834776419280)
[mustermann@komle.de]:   mailto:mustermann@komle.de (&93834776421792)
[musterfrau@komle.de]:   mailto:musterfrau@komle.de (&93834776426704)
[musterfrau@komle.de]:   mailto:musterfrau@komle.de (&93834798951992)
[musterfrau@komle.de]:   mailto:musterfrau@komle.de (&93834781549288)
[mustermann@komle.de#pop.komle.de:110]: mailto:mustermann@komle.de#pop.komle.de:110 (&93834776297776)
[mustermann@komle.de]:   mailto:mustermann@komle.de (&93834776314912)
[https://github.com/gematik/api-kim/blob/master/src/schema/Attachment_schema.json]: https://github.com/gematik/api-kim/blob/master/src/schema/Attachment_schema.json (&93834809685920)
