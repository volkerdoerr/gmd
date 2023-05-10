
Elektronische Gesundheitskarte und Telematikinfrastruktur

### 

- Klassifizierung: öffentlich
- Referenzierung: gemF_Laufzeitverlängerung_gSMC-K
- Revision: 548770
- Stand: 06.12.2022
- Status: freigegeben
- Version: 1.1.0

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
0.9.0

</td><td>
20.05.21

</td><td>
Vorabversion zur Prüfung

</td><td>
gematik

</td></tr><tr><td>
1.0.0 CC

</td><td>
07.06.21

</td><td>
zur Abstimmung freigegeben

</td><td>
gematik

</td></tr><tr><td>
1.0.0 RC

</td><td>
21.06.21

</td><td>
Einarbeitung Kommentierung

</td><td>
gematik

</td></tr><tr><td>
1.0.0

</td><td>
30.06.21

</td><td>
freigegeben

</td><td>
gematik

</td></tr><tr><td>
1.1.0 CC

</td><td>
25.10.22

</td><td>
Einarbeitung als Option, Anpassung Zeitraum

</td><td>
gematik

</td></tr><tr><td>
1.1.0 CC2

</td><td>
11.11.22

</td><td>
Einarbeitung Kommentierung

</td><td>
gematik

</td></tr></table>

### Inhaltsverzeichnis

- [Dokumentinformationen]
- [Inhaltsverzeichnis]
- [1] Einordnung des Dokuments
  - [1.1] Zielsetzung
  - [1.2] Zielgruppe
  - [1.3] Abgrenzungen
  - [1.4] Methodik
    - [1.4.1] Anforderungen
    - [1.4.2] Hinweise auf offene Punkte
- [2] Technisches Konzept Laufzeitverlängerung gSMC-K
  - [2.1] Zusammenfassung
    - [2.1.1] Betroffene Komponenten und Zertifikate
    - [2.1.2] Lösung
    - [2.1.3] Wiederholbarkeit der Aktion
    - [2.1.4] Zusammenspiel mit der ECC-Migration der Konnektoren
    - [2.1.5] Bedeutung der Laufzeitverlängerung der gSMC-K für Robustheit, Akzeptanz und Zukunftsfähigkeit der TI
  - [2.2] Identität ID.NK.VPN relevant für Konnektor - VPN-Zugangsdienst
  - [2.3] Identität ID.AK.AUT relevant für Konnektor - PS
  - [2.4] Identität SAK.AUTD_CVC relevant für C2C mit HBA
  - [2.5] Identität ID.SAK.AUT relevant für eHealth-Kartenterminal
- [3] Operative Umsetzung
  - [3.1] Bereitstellung des Zertifikats-Downloads
  - [3.2] Bereitstellung der Zertifikate
  - [3.3] Sperrprozesse
  - [3.4] Offline Konnektoren
- [4] Spezifikation
  - [4.1] Änderungen in gemSpec_Kon
    - [4.1.1] (3.1) Konnektoridentität und gSMC-K
    - [4.1.2] (3.1.1) Erneuerung der Zertifikate der gSMC-K
    - [4.1.3] (3.3) Betriebszustand
    - [4.1.4] (4.3.5 ) Neustart und Werksreset
    - [4.1.5] Identität ID.NK.VPN relevant für Konnektor - VPN-Zugangsdienst
      - [4.1.5.1] (4.3.7) Re-Registrierung des Konnektors mit neuem NK-Zertifikat
    - [4.1.6] (3.5.1) Identität ID.AK.AUT relevant für Konnektor - PS (3.5.1 Betriebsaspekte)
    - [4.1.7] (7 Anhang F) Events
  - [4.2] Änderungen in gemSpec_X.509_TSP
    - [4.2.1] (6.6) Erneuerung von Zertifikaten der gSMC-K
  - [4.3] Änderungen in gemSpec_CVC_TSP
    - [4.3.1] (5.2) Erneuerung von CV-Zertifikaten der gSMC-K
  - [4.4] (4.1.1.2) Änderungen in gemILF_PS -"ServerAuthentisierung"
- [5] Anhang A – Verzeichnisse
  - [5.1] Abkürzungen
  - [5.2] Referenzierte Dokumente
    - [5.2.1] Dokumente der gematik
    - [5.2.2] Weitere Dokumente

### 1 Einordnung des Dokuments

Dieses Dokument beschreibt das Feature "Laufzeitverlängerung gSMC-K" mit dem
die spezifikatorische Grundlage für eine sichere verlängerte Nutzung von
Konnektor-Identitäten der gSMC-K gelegt wird.Das Feature ist bereits fachlich
freigegeben und wird für den Produkttyp Konnektor bereitgestellt.Die
Umsetzung der Option Laufzeitverlängerung ist ab sofort verpflichtend.

### 1.1 Zielsetzung

Die in Konnektoren verbauten gSMC-K werden zum Zeitpunkt der Hardware-Produktion
mit TI-Zertifikaten personalisiert. Gemäß gematik- und BSI-Vorgaben dürfen
die Komponentenzertifikate ab dem Zeitpunkt des Abrufs maximal 5 Jahre gültig
sein. Dadurch haben die Konnektoren - ohne Maßnahmen zur
Verlängerung/Aktualisierung von Zertifikaten - eine maximal mögliche
Lebensdauer von 5 Jahren. Unter Berücksichtigung der Lager- und Lieferzeiten
fordert die gematik, dass die Konnektoren zum Zeitpunkt der Installation beim
Leistungserbringer eine Restlaufzeit von mindestens 4 Jahren aufweisen
müssen.Die ersten Konnektoren für den Online-Produktivbetrieb wurden in der
zweiten Jahreshälfte 2017 produziert. Somit laufen deren Zertifikate bis Ende
2022 ab und werden dadurch ungültig.Nach Ablauf der Zertifikate im Konnektor
stehen die Funktionen des Konnektors nicht mehr zur Verfügung. Stand heute
muss das Gerät rechtzeitig vor Ablauf der Zertifikate getauscht werden, um
eine unterbrechungsfreie TI-Nutzung für die Leistungserbringer zu
gewährleisten.

Das Feature "Laufzeitverlängerung gSMC-K" beschreibt eine technische
Alternative zu einem Austausch der betroffenen Geräte.

### 1.2 Zielgruppe

Das Dokument richtet sich an Konnektor-Hersteller, die das Feature
"Laufzeitverlängerung gSMC-K" in ihrem Konnektor-Produkt umsetzen wollen.

### 1.3 Abgrenzungen

In diesem Dokument sind die Festlegungen und Erläuterungen zum optionalen
Feature "Laufzeitverlängerung gSMC-K" für den Produkttyp Konnektor enthalten,
die die [gemSpec_Kon] ergänzen.

### 1.4 Methodik

### 1.4.1 Anforderungen

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

### 1.4.2 Hinweise auf offene Punkte

Themen, die noch intern geklärt werden müssen oder eine Entscheidung seitens
der Gesellschafter erfordern, sind wie folgt im Dokument gekennzeichnet:

Beispiel für einen offenen Punkt.

### 2 Technisches Konzept Laufzeitverlängerung gSMC-K

### 2.1 Zusammenfassung

Die Abbildung 1 zeigt die vom Laufzeitende der gSMC-K-Zertifikate betroffenen
Handlungsfelder im Überblick.

![Abbildung-1][Abbildung-1]

Für die Lösung gelten übergreifende Rahmenbedingungen:

 ---> UL

### 2.1.1 Betroffene Komponenten und Zertifikate

Die gSMC-K enthält Schlüsselmaterial und Zertifikate für verschiedene
Identitäten. Ein Teil davon sind die Geräteidentitäten des Konnektors, die
von der gematik spezifiziert und im TI-Kontext gefordert sind; nur diese
werden vom gematik-Konzept zur Laufzeitverlängerung der gSMC-K
erfasst.Darüber hinaus gibt es herstellerspezifisch genutzte Identitäten, die
hier nicht Gegenstand der Betrachtung sind. Ob und wie herstellerspezifische
Anteile der gSMC-K betroffen sind, und die Entscheidung, ob und welche
Maßnahmen hierbei ergriffen werden, obliegt dem Konnektor-Hersteller.

Die Geräteidentität des Konnektors (Konnektoridentität) teilt sich in drei
Identitäten auf:

 ---> OL

Nach Ablauf der gSMC-K-Zertifikate im Konnektor stehen wichtige Funktionen des
Konnektors nicht mehr zur Verfügung:

 ---> UL

### 2.1.2 Lösung

Die im Feld befindlichen Konnektoren werden per Firmware-Update in die Lage
versetzt, neue TI-Zertifikate für ihre alten Schlüssel der gSMC-K zu erhalten
und zu verwenden. Der TSP X.509 nonQES für Komponenten stellt Zertifikate in
der TI für den Abruf durch die Konnektoren bereit.

 ---> UL

![Abbildung-2][Abbildung-2]

### 2.1.3 Wiederholbarkeit der Aktion

Die Spezifikationen und die Implementierungen der Hersteller werden so
gestaltet, dass die Aktion der Laufzeitverlängerung auch wiederholt werden
kann.Eine zweite Laufzeitverlängerung darf nur nach Einwilligung  durch das
BSI erfolgen. 

### 2.1.4 Zusammenspiel mit der ECC-Migration der Konnektoren

Die ECC-Migration der Konnektoren erfolgt unabhängig von der
Laufzeitverlängerung der gSMC-K:

 ---> UL

### 2.1.5 Bedeutung der Laufzeitverlängerung der gSMC-K für Robustheit, Akzeptanz und Zukunftsfähigkeit der TI

Mit dem Feature "Laufzeitverlängerung der gSMC-K" sollein großflächiger
Konnektortausch vor der Verfügbarkeit einer Zukunftskonnektorlösung vermieden
werden. Die Lösung wurde so gestaltet, dass möglichst geringe Aufwände für
die Umsetzung und Zertifizierung anfallen.

Im folgenden werden erst die jeweiligen Detailkonzepte der betroffenen
Handlungsfelder beschrieben, bevor in Kapitel 4 die Spezifikations-Änderungen
ausformuliert werden.

### 2.2 Identität ID.NK.VPN relevant für Konnektor - VPN-Zugangsdienst

Entsprechend der Lösungsbeschreibung in Kapitel 3.1 werden neue
C.NK.VPN-Zertifikate vom TSP X.509 Komponenten erzeugt und gemeinsam mit den
anderen zur gleichen ICCSN gehörigen Zertifikaten abgelegt.Der Konnektor
beginnt ab einem definierten Zeitpunkt vor Ablauf der gSMC-K-Zertifikate mit
der Prüfung, ob neue Zertifikate für die ICCSN seiner gSMC-Ks vorhanden
sind.Der Konnektor lädt die bereitgestellten neuen Zertifikate herunter und
legt sie in seinem sicheren Speicher ab. Die neuen Zertifikate müssen ab
diesem Zeitpunkt verwendet werden. Dazu muss die Registrierung mit dem neuen
C.NK.VPN-Zertifikat erfolgen.

### 2.3 Identität ID.AK.AUT relevant für Konnektor - PS

Beim Verbindungsaufbau zwischen PSund Konnektor präsentiert der Konnektor dem
PS das Zertifikat der Identität ID.AK.AUT von der gSMC-K. Dieses Zertifikat
ist 5 Jahre gültig und wird nach Erreichen des Ablaufdatums vom Primärsystem
nicht mehr akzeptiert. Ein PS wird dann keine gesicherte Verbindung zu solch
einem Konnektor aufbauen können. 

Bei einer erfolgreichen zentralen Erneuerung der Zertifikate der gSMC-K wird das
erneuerte C.AK.AUT zur Verwendung vorgemerkt (siehe TUC_KON_410, Schritt 4).
Das neue AK.AUT-Zertifikat wird vom Konnektor nicht automatisch verwendet,
sondern dies wird vom Administrator manuell gesteuert (siehe A_21759). Bei
Bedarf kann der Administrator alternativ nicht-TI-Zertifikate am Konnektor
generieren und exportieren bzw. extern generieren und in den Konnektor
importieren, so wie deren Verwendungsstartzeitpunkt definieren.

### 2.4 Identität SAK.AUTD_CVC relevant für C2C mit HBA

Für die Verwendung von Stapel- und Komfortsignatur (SUK) bei der QES wird im
Rahmen der CardToCard-Authentisierung (C2C) zwischen HBA und dem Konnektor die
Identität SAK.AUTD_CVC der gSMC-K verwendet. Die vom HBA verwendete
Identität ist HPC.AUTD_SUK_CVC.

Bei HBA-G2.0-Karten wird für die mehrfache QES-Signatur mit einer einzigen
PIN-Eingabe (also SUK) eine Freischaltung des HBA mittels C2C und Aufbau eines
Trusted Channel (SE#2) zwischen gSMC-K und HBA für die Übertragung der zu
signierenden Daten gefordert.Die technische Notwendigkeit der C2C und des
Trusted Channel für die SUK entfällt bei HBA G2.1. Um das Sicherheitsniveau
für QES zu erfüllen, wird jedoch weiterhin ein Trusted Channel für die
QES-Stapel- und Komfortsignatur gefordert. 

![Img-003][Img-003]

Durch die „Innere Uhr“ der Karten (ParameterpointInTimedes COS) ergibt sich
bei einer längeren Nutzung von CV-Zertifikaten über deren
Gültigkeitszeitraum hinaus das Risiko, dass in bestimmten Szenarien das C2C
fehlschlägt. Im konkreten Szenario könnte ein HBA ein zu altes
gSMC-K-Zertifikat ablehnen und somit wäre dann keine Stapel- und
Komfortsignatur mehr möglich. Daher muss das Zertifikat nach 5 Jahren ersetzt
werden.

Entsprechend der Lösungsbeschreibung in Kapitel 3.1 werden neue
SAK.AUTD_CVC-Zertifikate vom TSP CVC Komponenten erzeugt und gemeinsam mit den
anderen zur gleichen ICCSN gehörigen Zertifikaten abgelegt. Der Konnektor
beginnt ab einem definierten Zeitpunkt vor Ablauf der gSMC-K-Zertifikate mit
der Prüfung, ob neue Zertifikate für die ICCSN seiner gSMC-Ks vorhanden
sind.Der Konnektor lädt die bereitgestellten neuen Zertifikate herunter und
legt sie in seinem sicheren Speicher ab. Die neuen Zertifikate müssen ab
diesem Zeitpunkt verwendet werden.

### 2.5 Identität ID.SAK.AUT relevant für eHealth-Kartenterminal

Die Identität ID.SAK.AUT auf der gSMC-K ist die im Anwendungskonnektor (AK)
genutzte Identität für die Signaturanwendungskomponente (SAK) des
Konnektors. Sie dient zur Authentisierung gegenüber den
Kartenterminals.Bisher haben die eHealth-Kartenterminals keine Uhr, gegen die
ein Zertifikats-Ende-Datum geprüft werden könnte. Daher wird für das
Kartenterminal beim Verifizieren des Konnektor-SAK-Zertifikats momentan auch
keine Prüfung des Laufzeitendes gefordert.

Das Zertifikat C.SAK.AUT der gSMC-K wird dennoch erneuert und verwendet. Dies
soll zur Absicherung der Robustheit dienen, falls Kartenterminals mit Uhren
zukünftig zugelassen werden. (Zukunftsfähigkeit). Da die Kartenterminals für
die Pairing-Informationen genau nur den öffentlichen Schlüssel des
Konnektor-Zertifikats speichern und sich dieser nicht unterscheidet zwischen
alten und erneuertem C.SAK.AUT, ist die automatische Nutzung des neuen
Zertifikats im Feld problemlos möglich.

### 3 Operative Umsetzung

### 3.1 Bereitstellung des Zertifikats-Downloads

Arvato als TSP Komponenten (für x.509 und CVC) ist von der gematik beauftragt,
den Zertifikats-Download zur Benutzung durch die Konnektoren, bereitzustellen.
Neben der Bereitstellung des Downloadpunkts mit den Zertifikatspaketen, müssen
auch alle operativen Bedingungen gegeben sein, wie beispielsweise
Firewall-Freischaltungen.

### 3.2 Bereitstellung der Zertifikate

Die gematik wird Arvato als TSP Komponenten (für x.509 und CVC) beauftragen,
neue Zertifikate für alle gSMC-K Zertifikate, die vor dem 01.01.2021 erstellt
worden sind, auf Kosten der gematik zu erzeugen.

### 3.3 Sperrprozesse

Für alle ausgestellten Zertifikate (auch für die erneuerten) werden
Sperr-Informationen vom OCSP-Responder der Komponenten-PKI bereitgestellt. Dies
ist in TIP1-A_3627 für die Zertifikats-Typen der gSMC-K festgelegt und gilt
somit auch für die erneuerten Zertifikate.Zur Zeit erfolgt der Sperrprozess
über die Zertifikats-Seriennummer, daher benötigen die Konnektor-Hersteller
die Info zur Seriennummer. Es ist geplant, folgenden Prozess zwischen dem TSP
Komponenten (Arvato) und den Konnektor-Herstellern zu etablieren:

 ---> UL

### 3.4 Offline Konnektoren

Es kann vorkommen, dass Konnektoren dauerhaft offline sind (z.B. Reserve
insbesondere in Krankenhäusern). Für diese Konnektoren ist die skizzierte
Lösung nur geeignet, wenn sie rechtzeitig vor Ablauf der Zertifikate online
genommen werden.

Dafür wurde die Möglichkeit geschaffen, dass ein Administrator manuell neue
gSMC-K-Zertifikate einbringt, ggf. auch nach Ablauf der ursprünglichen
Zertifikate.  

### 4 Spezifikation

### 4.1 Änderungen in gemSpec_Kon

### 4.1.1 (3.1) Konnektoridentität und gSMC-K

### 4.1.2 (3.1.1) Erneuerung der Zertifikate der gSMC-K

**A_21736 - Verwendung erneuerter Zertifikate**

Nach erfolgreicher Zertifikatserneuerung MUSS der Konnektor vor Ablauf der alten
Zertifikate an allen Stellen, wo er die Zertifikate C.NK.VPN,
C.AK.AUT, C.SAK.AUT, C.SAK.AUTD_CVC und C.CA_SAK.CS verarbeitet, die neuen
Zertifikate verwenden, es sei denn die Spezifikation trifft andere
Festlegungen. **[\<=]**

**A_21744 - Zertifikate regelmäßig erneuern**

Der Konnektor MUSS die Zertifikate C.NK.VPN, C.AK.AUT, C.SAK.AUT,
C.SAK.AUTD_CVC und C.CA_SAK.CS regelmäßig erneuern. Der Konnektor MUSS 180
Tage vor Ablauf des aktuell verwendeten C.NK.VPN-Zertifikats den
Zertifikatserneuerungsprozess anstoßen. Solange die Zertifikate noch nicht
vollständig erfolgreich erneuert wurden, MUSS der Konnektor genau einmal
täglich durch Aufruf von TUC_KON_410 neue Zertifikate beziehen. **[\<=]**

Es werden keine expliziten Festlegungen zu herstellerspezifisch verwendetem
Material auf der gSMC-K getroffen. Es liegt in der Verantwortung des
Konnektor-Herstellers, dafür zu sorgen, dass der Konnektor nach Erneuerung
und Aktivierung der spezifizierten Zertifikate insgesamt fehlerfrei lauffähig
ist.

**A_21879 - Erneuerte Zertifikate der gSMC-K manuell importieren**

Der Konnektor MUSS es dem Administrator ermöglichen, erneuerte
Zertifikate C.NK.VPN, C.AK.AUT, C.SAK.AUT, C.SAK.AUTD_CVC
und C.CA_SAK.CS manuell von lokaler Datenquelle einzuspielen.Der Konnektor
MUSS dies auch im kritischen
BetriebszustandEC_NK_Certificate_Expiredermöglichen. **[\<=]**

**A_21749-01 - TUC_KON_410 „gSMC-K-Zertifikate aktualisieren“**

Der Konnektor MUSS den technischen Use Case TUC_KON_410 „gSMC-K-Zertifikate
aktualisieren“ umsetzen.

Tabelle 1: TAB_KON_930 – TUC_KON_410 „Zertifikate aktualisieren“

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
Name

</td><td>
TUC_KON_410 "gSMC-K-Zertifikate aktualisieren"

</td></tr><tr><td>
Beschreibung

</td><td>
Dieser TUC bezieht neue gSMC-K-Zertifikate vom Downloadpunkt des TSP X.509
nonQES für Komponenten, oder diese werden vom Administrator übergeben.

</td></tr><tr><td>
Auslöser

</td><td>
A_21744, Administrator

</td></tr><tr><td>
Vorbedingungen

</td><td>
Automatische Aktualisierung:

 ---> UL

</td></tr><tr><td>
Eingangsdaten

</td><td>
Manuelle Aktualisierung: 

 ---> UL

</td></tr><tr><td>
Komponenten

</td><td>
Konnektor, TSP Komponenten

</td></tr><tr><td>
Ausgangsdaten

</td><td>
Keine

</td></tr><tr><td>
Standardablauf

</td><td>
Automatische Aktualisierung:

 ---> OL

       topic = „SMC_K/UPDATE/SUCCESS“;  
       eventType = Op; 

       severity = Info;  
       parameters = „$Parameters“; 

       doLog = true;  
       doDisp = true }

</td></tr><tr><td>
Varianten/Alternativen

</td><td>
Manuelle Aktualisierung:

 ---> OL

</td></tr><tr><td>
Fehlerfälle

</td><td>
(-\>1) Fehler beim Download:

TUC_KON_256 {

       topic = „SMC_K

/DOWNLOAD/ERROR

“;

       eventType = Op;

       severity = Error;

       parameters = „$Parameters“;

       doLog = true;

       doDisp = true }

(-\>3) Wenn eine der folgenden Prüfungen fehlschlägt, wird das bezogene
Zertifikat verworfen und mit dem nächsten fortgesetzt:

(-\> 3a) ICCSN nicht gleich: Fail=Iccsn

(-\> 3b) Neues Ablaufdatum nicht später als altes Ablaufdatum: Fail=Date

(-\> 3c) Öffentlicher Schlüssel passt nicht zum privaten Schlüssel: Fail=Crypt

(-\> 3e) Zertifikat gesperrt oder unknown: Fail=Ocsp

Automatische Aktualisierung: TUC_KON_256 {

       topic = „SMC_K/UPDATE/ERROR“;

       eventType = Op;

       severity = Error;

       parameters = „$Parameters“;

       doLog = true;

       doDisp = true }

(-\>3) Wenn eine der folgenden Prüfungen fehlschlägt, wird das bezogene
Zertifikat trotzdem zur Verwendung vorgemerkt:

(-\> 3d) Zertifikatsseriennummer identisch: Fail=Serial

Warnung wird protokolliert

</td></tr><tr><td>
Nichtfunktionale Anforderungen

</td><td>
Keine

</td></tr><tr><td>
Zugehörige Diagramme

</td><td>
Keine

</td></tr></table>

Tabelle 2: Tab_Kon_931 Fehlercodes TUC_KON_410 „gSMC-K-Zertifikate
aktualisieren“

<table><tr><th>
Fehlercode

</th><th>
ErrorType

</th><th>
Severity

</th><th>
Fehlertext

</th></tr><tr><td colspan="4">
Neben den Fehlercodes der aufgerufenen technischen Use Cases können folgende
weitere Fehlercodes auftreten:

</td></tr><tr><td colspan="4" rowspan="1">
herstellerspezifisch

</td></tr></table>

**[\<=]**

**A_21780 - Nutzerhinweis bezüglich Fehler bei Zertifikatserneuerung**

Der Hersteller des Konnektors MUSS in seinem Handbuch den Nutzer/Administrator
darauf hinweisen, dass die Ereignisse mit dem Topic=SMC_K/UPDATE/ERROR und dem
Topic=SMC_K/DOWNLOAD/ERROR dringend durch das Primärsystem abonniert werden
sollten und dass der Nutzer/Administrator sich bei Auftreten des Fehlers
unverzüglich mit dem Hersteller in Verbindung setzen muss. **[\<=]**

### 4.1.3 (3.3) Betriebszustand

**TIP1-A_4512-03 - Ereignis bei Änderung des Betriebszustandes**

Der Konnektor MUSS per Ereignisdienst TUC_KON_256 über Änderungen des
Betriebszustandes (Tabelle TAB_KON_503 Betriebszustand_Fehlerzustandsliste)
informieren.Der Konnektor muss dazu für jeden Fehlerzustand $EC mit Error
Condition $EC.errorcondition mit verändertem Wert $EC.value den technischen
Anwendungsfall TUC_KON_256 „Systemereignis absetzen“ mit folgenden
Parametern aufrufen:TUC_KON_256 {        topic =
"OPERATIONAL_STATE/$EC.errorcondition";    eventType =
$EC.type;    severity = $EC.severity;    parameters =
(„Value=$EC.value, $EC.parameterlist”)}

Tabelle3: TAB_KON_503 Betriebszustand_Fehlerzustandsliste

<table><tr><th>
 ErrorCondition

(siehe Hinweis 1)

</th><th>
 Beschreibung

</th><th>
Type

</th><th>
Seve

rity

</th><th>
max.

Fest

stell

ungs-

zeit

</th><th>
Parameterlist

(siehe Hinweis 2)

</th></tr><tr><td>
EC_CardTerminal_

Software_Out_Of_

Date ($ctId)

</td><td>
Software auf

Kartenterminal($ctId)

ist nicht aktuell

</td><td>
Op

</td><td>
Info

</td><td>
1 day

</td><td>
CtID=$ctId;

Bedeutung=

$EC.description

</td></tr><tr><td>
EC_CardTerminal_

gSMC-KT_Certificate_ Expires_Soon ($ctId)

</td><td>
Das Zertifikat der gSMC-KT im

Kartenterminal($ctId)

läuft in weniger als 5 Wochen ab

</td><td>
Op

</td><td>
Info

</td><td>
7 days

</td><td>
CtID=$ctId;

Bedeutung=

$EC.description

</td></tr><tr><td>
EC_Connector_

Software_Out_

Of_Date

</td><td>
I_KSRS_Download::list_

Updates

liefert mindestens eine

UpdateInformation mit einer UpdateInformation/Firmware/

FWVersion \> aktuelle Version

der Konnektorsoftware, deren

UpdateInformation/Firmware/

FWPriority = „Kritisch“

</td><td>
Op

</td><td>
Info

</td><td>
1 day

</td><td>
Bedeutung=

$EC.description

</td></tr><tr><td>
EC_FW_Update_Available

</td><td>
I_KSRS_Download::list_

Updates

liefert mindestens eine

UpdateInformation mit einer UpdateInformation/Firmware/

FWVersion \> aktuelle Version

der Konnektor- oder Kartenterminalsoftware

</td><td>
Op

</td><td>
Info

</td><td>
1 day

</td><td>
Bedeutung=

$EC.description

</td></tr><tr><td>
EC_FW_Not_

Valid_Status_

Blocked

</td><td>
Konnektor Firmware muss

aktualisiert werden. Zugang zur

TI momentan nicht erlaubt.

</td><td>
Sec

</td><td>
Fatal

</td><td>
1 day

</td><td>
Bedeutung=

$EC.description

</td></tr><tr><td>
EC_Time_Sync_

Not_Successful

</td><td>
der letzte

Synchronisationsversuch

der Systemzeit war nicht

erfolgreich.

</td><td>
Op

</td><td>
Info

</td><td>
1 sec

</td><td>
LastSyncAttempt=

$lastSyncAttempt

Timestamp;

LastSyncSuccess

=$lastSyncSuccess

Timestamp;

Bedeutung=

$EC.description

</td></tr><tr><td>
EC_TSL_Update_

Not_Successful

</td><td>
das letzte Update der TSL

war nicht erfolgreich.

</td><td>
Op

</td><td>
Info

</td><td>
1 sec

</td><td>
Bedeutung=

$EC.description;

LastUpdateTSL=

$lastUpdateTSL

Timestamp

</td></tr><tr><td>
EC_TSL_Expiring

</td><td>
Systemzeit t mit

t \> NextUpdate-Element der

TSL – 7 Tage und

t \<= NextUpdate-Element

der TSL

</td><td>
Sec

</td><td>
Info

</td><td>
1 day

</td><td>
NextUpdateTSL

=$NextUpdate-

Element der TSL;

Bedeutung=

$EC.description

</td></tr><tr><td>
EC_BNetzA_VL_

Update_

Not_Successful

</td><td>
Das letzte Update der

BNetzA-VL war nicht erfolgreich

</td><td>
Op

</td><td>
Info

</td><td>
1 sec

</td><td>
LastUpdateBNetz

AVL=

$lastUpdateBNetz

AVLTimestamp;

Bedeutung=

$EC.description

</td></tr><tr><td>
EC_ BNetzA_VL_

not_valid

</td><td>
Systemzeit t mit

t \> NextUpdate-Element der

BNetzA-VL

</td><td>
Sec

</td><td>
War

ning

</td><td>
1 day

</td><td>
NextUpdateBNetz

AVL

=$NextUpdate-

Element

der BNetzA-VL;

Bedeutung=

$EC.description

</td></tr><tr><td>
EC_TSL_Trust_

Anchor_Expiring

</td><td>
Gültigkeit des Vertrauensankers

ist noch nicht abgelaufen, läuft

aber innerhalb von 30 Tagen ab.

</td><td>
Sec

</td><td>
Info

</td><td>
1 day

</td><td>
ExpiringDateTrust

Anchor=

Ablaufdatum der

Vertrauensanker

gültigkeit;

Bedeutung=

$EC.description

</td></tr><tr><td>
EC_LOG_

OVERFLOW

</td><td>
Wenn im Rahmen der Regeln

für die rollierende Speicherung

von Logging-Einträgen Einträge

gelöscht werden, die nicht älter

als

SECURITY_LOG_DAYS

,

 

LOG_DAYS bzw. FM_

\<fmName\>_LOG_DAYS sind,

tritt der Fehlerzustand ein.

Der Fehlerzustand kann nur

durch einen Administrator

wieder zurückgesetzt werden.

Unter Protokoll wird die Liste der auslösenden Protokolle angegeben.

</td><td>
Op

</td><td>
War

ning

</td><td>
1 sec

</td><td>
Protokoll=$Protokoll;

Bedeutung=

$EC.description

</td></tr><tr><td>
EC_CRL_Expiring

</td><td>
Systemzeit t \> NextUpdate

der CRL – 3 Tage

</td><td>
Sec

</td><td>
War

ning

</td><td>
1 day

</td><td>
ExpiringDateCRL=

NextUpdate der

CRL;

Bedeutung=

$EC.description

</td></tr><tr><td>
EC_Time_Sync_

Pending_Warning

</td><td>
MGM_LU_ONLINE=Enabled und

keine erfolgreiche

Synchronisation

der Systemzeit seit d Tagen und

d \> NTP_WARN_PERIOD und

d \<= NTP_GRACE_PERIOD.

Nach einer Korrektur oder

Bestätigung der Systemzeit

durch einen Administrator muss

der Konnektor wie nach einer

erfolgreichen Zeitsynchronisation

verfahren, d.h., der Tagezähler

wird auf 0 zurückgesetzt.

</td><td>
Sec

</td><td>
War

ning

</td><td>
1 day

</td><td>
LastSyncSuccess=

$lastSyncSuccess

Timestamp;

Bedeutung=

$EC.description

</td></tr><tr><td>
EC_TSL_Out_

Of_Date_Within_

Grace_Period

</td><td>
Systemzeit t mit

t \> NextUpdate-Element der TSL

und

t \<= NextUpdate-Element

der TSL + CERT_TSL_

DEFAULT_GRACE_

PERIOD_DAYS

und eine neue TSL ist nicht

verfügbar

</td><td>
Sec

</td><td>
War

ning

</td><td>
1 day

</td><td>
NextUpdateTSL

=$NextUpdate-

Element der TSL;

GracePeriodTSL

=CERT_TSL_

DEFAULT_

GRACE_PERIOD_

DAYS;

Bedeutung=

$EC.description

</td></tr><tr><td>
EC_CardTerminal_

Not_Available

($ctId)

</td><td>
Kartenterminal($ctId) ist nicht

verfügbar. Dieser

Betriebszustand

bezieht sich auf die als „aktiv“

gekennzeichneten KTs.  

</td><td>
Op

</td><td>
Error

</td><td>
1 sec

</td><td>
CtID=$ctId;

Bedeutung=

$EC.description

</td></tr><tr><td>
EC_No_VPN_TI_

Connection

</td><td>
Kein sicherer Kanal (VPN) in die Telematikinfrastruktur aufgebaut.

Der Wert 300 sec ist abgeleitet

aus der maximalen

Verbindungsaufbauzeit bei

einem Standortausfall des

VPN-Zugangsdienstes.

</td><td>
Op

</td><td>
Error

</td><td>
300 sec

</td><td>
Bedeutung=

$EC.description

</td></tr><tr><td>
EC_No_VPN_

SIS_Connection

</td><td>
Kein sicherer Kanal (VPN) zu

den Sicheren Internet Services

aufgebaut.

Der Wert 300 sec ist abgeleitet

aus der maximalen

Verbindungsaufbauzeit

bei einem

Standortausfall des

VPN-Zugangsdienstes.

</td><td>
Op

</td><td>
Error

</td><td>
300 sec

</td><td>
Bedeutung=

$EC.description

</td></tr><tr><td>
EC_No_Online_

Connection

</td><td>
Konnektor kann Dienste im

Transportnetz nicht erreichen.

</td><td>
Op

</td><td>
Error

</td><td>
10 sec

</td><td>
Bedeutung=

$EC.description

</td></tr><tr><td>
EC_IP_Adresses_

Not_Available

</td><td>
Die IP-Adressen des

Netzkonnektors sind nicht oder

falsch gesetzt.

</td><td>
Sec

</td><td>
Error

</td><td>
1 sec

</td><td>
Bedeutung=

$EC.description

</td></tr><tr><td>
EC_CRL_Out_Of_

Date

</td><td>
Systemzeit t \> Next Update

der CRL

</td><td>
Sec

</td><td>
Fatal

</td><td>
1 day

</td><td>
NextUpdateCRL=

$NextUpdate der

CRL;

Bedeutung=

$EC.description

</td></tr><tr><td>
EC_Firewall_Not_

Reliable

</td><td>
Firewall-Regeln konnten nicht

fehlerfrei generiert werden oder

beim Laden der Firewall-Regeln

ist ein Fehler aufgetreten.

</td><td>
Sec

</td><td>
Fatal

</td><td>
1 sec

</td><td>
Bedeutung=

$EC.description

</td></tr><tr><td>
EC_Random_

Generator_

Not_Reliable

</td><td>
Der Zufallszahlengenerator kann

die Anforderungen an die zu

erzeugende Entropie

nicht erfüllen.

</td><td>
Sec

</td><td>
Fatal

</td><td>
1 sec

</td><td>
Bedeutung=

$EC.description

</td></tr><tr><td>
EC_Secure_

KeyStore_

Not_Available

</td><td>
Sicherer Zertifikats- und

Schlüsselspeicher des

Konnektors

(gSMC-K oder Truststore)

nicht verfügbar

</td><td>
Sec

</td><td>
Fatal

</td><td>
1 sec

</td><td>
Bedeutung=

$EC.description

</td></tr><tr><td>
EC_Security_

Log_

Not_Writable

</td><td>
Das Sicherheitslog kann nicht

geschrieben werden.

</td><td>
Op

</td><td>
Fatal

</td><td>
1 sec

</td><td>
Bedeutung=

$EC.description

</td></tr><tr><td>
EC_Software_

Integrity_

Check_Failed

</td><td>
Eine oder mehrere

konnektorinterne

Integritätsprüfungen der aktiven Konnektorbestandteile

sind fehlgeschlagen.

</td><td>
Sec

</td><td>
Fatal

</td><td>
1 day

</td><td>
Bedeutung=

$EC.description

</td></tr><tr><td>
EC_Time_

Difference_

Intolerable

</td><td>
Abweichung zwischen

der lokalen Zeit und der

per NTP empfangenen

Zeit bei der

Zeitsynchronisation

größer als NTP_MAX_

TIMEDIFFERENCE.

Nach einer Korrektur oder

Bestätigung der Systemzeit

durch einen Administrator

muss der Konnektor den

Fehlerzustand zurücksetzen.

</td><td>
Sec

</td><td>
Fatal

</td><td>
1 sec

</td><td>
NtpTimedifference=

Zeitabweichung;

NtpMaxAllowed

Timedifference

=NTP_MAX_

TIMEDIFFERENCE;

Bedeutung=

$EC.description

</td></tr><tr><td>
EC_Time_Sync_

Pending_Critical

</td><td>
MGM_LU_ONLINE=

Enabled und

keine erfolgreiche

Synchronisation

der Systemzeit seit d Tagen

und

d \> NTP_GRACE_PERIOD

Nach einer Korrektur oder

Bestätigung der Systemzeit

durch einen Administrator muss

der Konnektor wie nach einer

erfolgreichen

Zeitsynchronisation

verfahren, d.h., der Tagezähler

wird auf 0 zurückgesetzt.

</td><td>
Sec

</td><td>
Fatal

</td><td>
1 day

</td><td>
LastSyncSuccess

=$lastSync

SuccessTimestamp;

NtpGracePeriod=

NTP_GRACE_

PERIOD;

Bedeutung=

$EC.description

</td></tr><tr><td>
EC_TSL_Trust_

Anchor_

Out_Of_Date

</td><td>
Gültigkeit des Vertrauensankers

ist abgelaufen

</td><td>
Sec

</td><td>
Fatal

</td><td>
1 day

</td><td>
ExpiringDateTrust

Anchor=

Ablaufdatum der

Vertrauensanker

gültigkeit;

Bedeutung=

$EC.description

</td></tr><tr><td>
EC_TSL_Out_

Of_Date_

Beyond_Grace_

Period

</td><td>
Systemzeit t mit

t \> NextUpdate-Element

der TSL +

CERT_TSL_DEFAULT_

GRACE_ PERIOD_DAYS

und eine neue TSL ist

nicht verfügbar

</td><td>
Sec

</td><td>
Fatal

</td><td>
1 day

</td><td>
NextUpdateTSL

=$NextUpdate-

Element der TSL;

GracePeriodTSL

=CERT_TSL_

DEFAULT_

GRACE_PERIOD_

DAYS;

Bedeutung=

$EC.description

</td></tr><tr><td>
EC_

CRYPTOP

ERATION_

ALARM

</td><td>
Gemäß TIP1-A_4597 wurde ein

potentieller Missbrauch einer

Kryptooperation erkannt.

Nur der Administrator kann die

Alarmmeldung zurücksetzen.

</td><td>
Sec

</td><td>
War

ning

</td><td>
1 min

</td><td>
Operation=

$Operationsname;

Count=$Summenwert;

Arbeitsplatz=

$\<Liste

operationsaufrufenden workplaceIDs\>;    

Meldung=

’Auffällige Häufung von

Operationsaufrufen

in den

letzten 10 Minuten’

</td></tr><tr><td>
EC_OTHER_

ERROR_

STATE($no)

</td><td>
Herstellerspezifische

Fehlerzustände, die per $no

(von 1 aufsteigend nummeriert)

identifiziert werden.

$Type, $Severity und

$ParameterList legt

der Hersteller

nach Bedarf fest.

</td><td>
$Type

</td><td>
$Sev

erity

</td><td>
\<= 1 day

</td><td>
Bedeutung=

$EC.description

</td></tr><tr><td>
EC_NK_Certificate_Expiring

</td><td>
Das C.NK.VPN-Zertifikat läuft bald ab. 

Systemzeit t \> (Ablaufdatum von C.NK.VPN – 180 Tage)

</td><td>
Sec

</td><td>
Warning

</td><td>
1 day

</td><td>
Iccsn=$Iccsn;

Serial=$Serialnumber;

Bedeutung=

$EC.description

</td></tr><tr><td>
EC_NK_Certificate_Expired

</td><td>
Das C.NK.VPN-Zertifikat ist abgelaufen.

Systemzeit t \> Ablaufdatum von C.NK.VPN 

</td><td>
Sec 

</td><td>
Fatal

</td><td>
1 day

</td><td>
Iccsn=$Iccsn;

Serial=$Serialnumber;

Bedeutung=

$EC.description

</td></tr></table>

Erläuterungen zu TAB_KON_503:

Hinweis 1:

Jeder Fehlerzustand wird durch einen eindeutigen ErrorCondition identifiziert.
Dieser kann einen Parameter enthalten. Sind etwa die Kartenterminals mit
ctId=47 und das mit ctId=93 nicht erreichbar, so lauten die ErrorCondition
„EC_CardTerminal_Not_Available(47)“ und
„EC_CardTerminal_Not_Available(93)“.

Hinweis 2:

EC.description referenziert den Text, der in der Spalte „Beschreibung“ des
Zustandes spezifiziert wurde. **[\<=]**

**TIP1-A_4510-05 - Sicherheitskritische Fehlerzustände**

Der Konnektor MUSS bei eingetretenem Fehlerzustand aus Tabelle Tab_ Kon_503
Betriebszustand_Fehlerzustandsliste mit Severity=Fatal dafür sorgen, dass von
den Operationen der Basisdienste und Technische Use Cases (TUCs) der
Basisdienste, die relevant für Fachanwendungen sind, nur erlaubte Operationen
und TUCs gestartet und ausgeführt werden.Welche Operationen und TUCs je
eingetretenem Fehlerzustand ausgeführt werden dürfen, legt Tabelle
„TAB_KON_504-01 Ausführungserlaubnis für Dienste in kritischen
Fehlerzuständen“ fest: Jede Erlaubnis ist dort durch ein „x“
definiert.Abweichend zu Angaben in der Tabelle TAB_KON_504-01 DÜRFEN folgende
Operationen und TUCs NICHT im Zustand EC_Firewall_Not_Reliable ausgeführt
werden:

 ---> UL

Sind mehrere Fehlerzustände gleichzeitig eingetreten, dürfen nur die
Operationen und TUCs ausgeführt werden, die für alle eingetretenen
Fehlerzustände erlaubt sind. Der Konnektor MUSS Anfragen, die auf Grund eines
kritischen Fehlerzustandes nicht ausgeführt oder abgebrochen werden, mit einem
Fehler (Fehlercode 4002) beantworten.

Tabelle4: TAB_KON_502 Fehlercodes „Betriebszustand“

<table><tr><th>
Fehlercode

</th><th>
ErrorType

</th><th>
Severity

</th><th>
Fehlertext

</th></tr><tr><td>
4002

</td><td>
Security

</td><td>
Fatal

</td><td>
Der Konnektor befindet sich in einem kritischen Betriebszustand

</td></tr></table>

**[\<=]**

<table><tr><td>
EC_ Software_ Integrity_ Check_ Failed

</td><td>
EC_ Random_ Generator_ Not_ Reliable

</td><td>
EC_ Security_ Log_ Not_ Writable

</td><td>
EC_ Time_ Sync_ Pending_ Critical

</td><td>
EC_ Time_ Diffe rence_ Intoler able

</td><td>
EC_ CRL_ Out_ Of_ Date

</td><td>
EC_ TSL_ Out_ Of_ Date_ Beyond_ Grace_ Period

</td><td>
EC_ TSL_ Trust_

Anchor_

Out_

Of_

Date

</td><td>
EC_ Secure_ KeyStore_ Not_ Available

</td><td>
EC_ FW_ Not_ Valid_ Status_ Blocked

</td><td>
EC_

NK_

Certificate_

Expired 

</td></tr><tr><td colspan="12">
Technische Use Cases (TUCs) der Basisdienste  
relevant für Fachanwendung und
die Kommunikation mit Weiteren Anwendungen und SIS

</td></tr><tr><td colspan="2">
Zugriffsberechtigungsdienst

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td></tr><tr><td>
TUC_KON_000 Prüfe Zugriffsberechtigung

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td></tr><tr><td colspan="2">
Dienstverzeichnisdienst

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td></tr><tr><td>
 

</td><td>
TUC_KON_041 Einbringen der Endpunktinformationen während der Bootup-Phase

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td></tr><tr><td colspan="2">
Kartenterminaldienst

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td></tr><tr><td>
TUC_KON_051 Mit Anwender über Kartenterminal interagieren

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td><td>
x

</td><td>
-

</td></tr><tr><td colspan="2">
Kartendienst

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td></tr><tr><td>
TUC_KON_005 Card-to-Card authentisieren

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td><td>
x

</td><td>
-

</td></tr><tr><td>
TUC_KON_006 Datenzugriffsaudit eGK schreiben

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td><td>
x

</td><td>
-

</td></tr><tr><td>
TUC_KON_018 eGK-Sperrung prüfen

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td><td>
x

</td><td>
-

</td></tr><tr><td>
TUC_KON_024 Karte zurücksetzen

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td><td>
x

</td><td>
-

</td></tr><tr><td>
TUC_kON_026 Liefere

CardSession

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
-

</td><td>
x

</td><td>
-

</td><td>
-

</td><td>
-

</td></tr><tr><td>
TUC_KON_200 SendeAPDU

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td><td>
x

</td><td>
-

</td></tr><tr><td>
TUC_KON_202 LeseDatei

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td><td>
x

</td><td>
-

</td></tr><tr><td>
TUC_KON_203 SchreibeDatei

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td><td>
x

</td><td>
-

</td></tr><tr><td>
TUC_KON_209 LeseRecord

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td><td>
x

</td><td>
-

</td></tr><tr><td colspan="12">
Systeminformationsdienst

</td></tr><tr><td>
TUC_KON_256 Systemereignis absetzen

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td></tr><tr><td colspan="2">
Verschlüsselungsdienst

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td></tr><tr><td>
TUC_KON_072 Daten symmetrisch verschlüsseln

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td><td>
x

</td><td>
-

</td></tr><tr><td>
TUC_KON_073 Daten symmetrisch entschlüsseln

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td><td>
x

</td><td>
-

</td></tr><tr><td colspan="2">
Zertifikatsdienst

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td></tr><tr><td>
 

</td><td>
TUC_KON_034 Zertifikatsinformationen extrahieren

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td><td>
x

</td><td>
x

</td></tr><tr><td colspan="2">
Protokollierungsdienst

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td></tr><tr><td>
TUC_KON_271 Schreibe Protokolleintrag

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td></tr><tr><td colspan="2">
TLS-Dienst 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td></tr><tr><td>
TUC_KON_110 Kartenbasierte TLS-Verbindung aufbauen

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td></tr><tr><td colspan="2">
Verbindung zum VPN-Konzentrator

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td></tr><tr><td rowspan="2">
 

</td><td>
TUC_VPN-ZD_0001 „IPsec Tunnel TI aufbauen”

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td></tr><tr><td>
TUC_VPN-ZD_0002 „IPsec Tunnel SIS aufbauen”

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td></tr><tr><td colspan="2">
Feature Laufzeitverlängerung gSMC-K)

</td></tr><tr><td>
TUC_KON_410 „gSMC-K-Zertifikate aktualisieren (automatisch)

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td></tr><tr><td>
TUC_KON_410 „gSMC-K-Zertifikate aktualisieren (manuell)

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td></tr><tr><td>
TUC_KON_411 „Konnektor mit neuem NK-Zertifikat registrieren (automatisch)

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td></tr><tr><td>
TUC_KON_411 „Konnektor mit neuem NK-Zertifikat registrieren (manuell)

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td></tr><tr><td colspan="12">
Operationen der Basisdienste

</td></tr><tr><td colspan="2">
Kartendienst

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td></tr><tr><td>
VerifyPin  

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td><td>
x

</td><td>
-

</td></tr><tr><td>
UnblockPin  

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td><td>
x

</td><td>
-

</td></tr><tr><td>
ChangePin 

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td><td>
x

</td><td>
-

</td></tr><tr><td>
GetPinStatus  

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td><td>
x

</td><td>
-

</td></tr><tr><td colspan="2">
Systeminformationsdienst

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td></tr><tr><td>
Schnittstelle der Ereignissenke

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td></tr><tr><td>
GetCardTerminals

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td></tr><tr><td>
GetCards

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td></tr><tr><td>
GetResourceInformation

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td></tr><tr><td>
Subscribe

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td></tr><tr><td>
RenewSubscription

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td></tr><tr><td>
Unsubscribe

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td></tr><tr><td>
GetSubscription

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td></tr><tr><td colspan="2">
Verschlüsselungsdienst

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td></tr><tr><td>
EncryptDocument

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td><td>
x

</td><td>
-

</td></tr><tr><td>
DecryptDocument

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td><td>
x

</td><td>
-

</td></tr><tr><td colspan="2">
 Signaturdienst

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td></tr><tr><td>
SignDocument

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td><td>
x

</td><td>
-

</td></tr><tr><td>
VerifyDocument

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td><td>
x

</td><td>
-

</td></tr><tr><td>
GetJobNumber

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td><td>
x

</td><td>
-

</td></tr><tr><td>
StopSignature

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td><td>
x

</td><td>
-

</td></tr><tr><td>
ActivateComfortSignature

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td><td>
x

</td><td>
-

</td></tr><tr><td>
DeactivateComfortSignature

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td><td>
x

</td><td>
-

</td></tr><tr><td>
GetSignatureMode

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td><td>
x

</td><td>
-

</td></tr><tr><td colspan="12">
Authentifizierungsdienst   

</td></tr><tr><td>
ExternalAuthenticate

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td><td>
x

</td><td>
-

</td></tr><tr><td colspan="2">
Zertifikatsdienst

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td></tr><tr><td>
ReadCardCertificate

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td></tr><tr><td>
CheckCertificateExpiration

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td></tr><tr><td>
VerifyCertificate

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td></tr><tr><td colspan="2">
Zeitdienst

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td></tr><tr><td>
I_NTP_Time_Information

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
-

</td><td>
-

</td></tr><tr><td colspan="2">
Konnektormanagement

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td><td>
 

</td></tr><tr><td>
Softwareaktualisierung

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td></tr><tr><td>
Protokolleinsicht

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td></tr><tr><td>
Werksreset

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td></tr><tr><td>
Sonstiges

</td><td>
-

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td><td>
x

</td></tr></table>

### 4.1.4 (4.3.5 ) Neustart und Werksreset

folgende Anforderung wird im Kapitel 4.3.5 ergänzt

**A_21743 - Laufzeitverlängerung gSMC-K: Erneuerte Zertifikate nach Werksreset
verwenden**

Der Konnektor, dessen gSMC-K-Zertifikate erneuert wurden, MUSS auch nach einem
Werksreset die erneuerten Zertifikate verwenden. **[\<=]**

### 4.1.5 Identität ID.NK.VPN relevant für Konnektor - VPN-Zugangsdienst

### 4.1.5.1 (4.3.7) Re-Registrierung des Konnektors mit neuem NK-Zertifikat

**A_21745-01 - Re-Registrierung mit neuem NK-Zertifikat automatisch
durchführen**

Nach einer vollständigen erfolgreichen automatischen Zertifikatserneuerung
über TUC_KON_410 MUSS der Konnektor eine Re-Registrierung mit dem neuen
Zertifikat beim Registrierungsdienst des VPN-Zugangsdienstes durchführen.
Solange nach Bezug eines neuen C.NK.VPN-Zertifikats noch keine erfolgreiche
Re-Registrierung durchgeführt wurde, MUSS der Konnektor genau einmal täglich
TUC_KON_411 aufrufen. **[\<=]**

**A_21881 - Re-Registrierung mit neuem NK-Zertifikat manuell durchführen**

Der Konnektor MUSS die manuelle Re-Registrierung mittels TUC_KON_411 durch den
Administrator auch im kritischen
BetriebszustandEC_NK_Certificate_Expiredermöglichen. **[\<=]**

**A_21758-06 - TUC_KON_411 „Konnektor mit neuem NK-Zertifikat registrieren“**

Der Konnektor MUSS den technischen Use Case TUC_KON_411 "Konnektor mit neuem
NK-Zertifikat registrieren"umsetzen.

Tabelle 6: TAB_KON_932 – TUC_KON_411 „Konnektor mit neuem NK-Zertifikat
registrieren“

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
Name

</td><td>
TUC_KON_411 "Konnektor mit neuem NK-Zertifikat registrieren"

</td></tr><tr><td>
Beschreibung

</td><td>
Dieser TUC führt eine Neuregistrierung mit einem neuen (ECC) NK-Zertifikat
durch.

</td></tr><tr><td>
Auslöser

</td><td>
A_

22332, A_21745, Administrator

</td></tr><tr><td>
Vorbedingungen

</td><td>
Keine

</td></tr><tr><td>
Eingangsdaten

</td><td>
Keine

</td></tr><tr><td>
Komponenten

</td><td>
Konnektor, VPN-ZugD

</td></tr><tr><td>
Ausgangsdaten

</td><td>
Keine

</td></tr><tr><td>
Standardablauf

</td><td>
 ---> OL

</td></tr><tr><td>
Varianten/Alternativen

</td><td>
Manuelle Registrierung:  
(-\>2) Der Administrator soll die zu verwendende SM-B
auswählen können.

</td></tr><tr><td>
Fehlerfälle

</td><td>
(



 2

) Es konnte keine freigeschaltete SM-B ausgewählt werden:  
     
Fail=No_Smcb  
(-\>2,3) Im Fehlerfall  
       TUC_KON_256 {  
       
    topic = „SMC_K/REGISTER/ERROR“;  
            eventType = Op; 

            severity = Error;  
            parameters =
„$Parameters“;  
            doLog = true;  
            doDisp
= true }  
Die Registrierung soll herstellerspezifisch erneut mehrmals versucht
werden.  
Bei allen Fehlerfällen, die zum Abbruch führen:  
TUC_KON_256 { 

       topic = „SMC_K/REGISTER/ERROR“;  
       eventType =
Op;  
       severity = Error;  
       parameters =
„$Parameters“;  
       doLog = true;  
       doDisp = true }

</td></tr><tr><td>
Nichtfunktionale Anforderungen

</td><td>
Keine

</td></tr><tr><td>
Zugehörige Diagramme

</td><td>
Keine

</td></tr></table>

Tabelle 7: Tab_Kon_933 Fehlercodes TUC_KON_411"Konnektor mit neuem
NK-Zertifikat registrieren"

<table><tr><th>
Fehlercode

</th><th>
ErrorType

</th><th>
Severity

</th><th>
Fehlertext

</th></tr><tr><td colspan="4">
Neben den Fehlercodes der aufgerufenen technischen Use Cases können folgende
weitere Fehlercodes auftreten:

</td></tr><tr><td colspan="4" rowspan="1">
herstellerspezifisch

</td></tr></table>

**[\<=]**

### 4.1.6 (3.5.1) Identität ID.AK.AUT relevant für Konnektor - PS (3.5.1 Betriebsaspekte)

**A_21759 - Erneuerte ID.AK.AUT für Authentisierung des Konnektors gegenüber
Clientsystemen verwenden**

Der Konnektor MUSS dem Administrator das Einschalten der Verwendung von
erneuerten C.AK.AUT für die Authentisierung des Konnektors gegenüber den
Clientsystemen über das Managementinterface ermöglichen. Der Konnektor DARF
ein erneuertes C.AK.AUT NICHT automatisch verwenden. **[\<=]**

### 4.1.7 (7 Anhang F) Events

<table><tr><th>
Topic Ebene1

/Topic Ebene2

/Topic Ebene3

</th><th>
Typ

</th><th>
Schw

ere

</th><th>
Pr

ot

</th><th>
An

Cli

en

ts

</th><th>
Parameter

</th><th>
Bedeutung

</th><th>
Auslöser

(TUC/Op)

</th></tr><tr><td>
SMC_K/UPDATE/SUCCESS

</td><td>
Op

</td><td>
Info

</td><td>
x

</td><td>
x

</td><td>
Zertifikate erfolgreich erneuert

</td><td>
TUC_KON_410

</td></tr><tr><td>
SMC_K/DOWNLOAD/ERROR

</td><td>
Op

</td><td>
Error

</td><td>
x

</td><td>
x

</td><td>
Fehler beim Zertifikatsdownload

</td><td>
TUC_KON_410

</td></tr><tr><td>
SMC_K/UPDATE/ERROR

</td><td>
Op

</td><td>
Error

</td><td>
x

</td><td>
x

</td><td>
Iccsn=$Iccsn;

Profile=$CertProfile; Serial=$Serialnumber;

Fail=Iccsn | Date | Crypt | Serial | Ocsp

</td><td>
Prüffehler bei Zertifikatsupdate

</td><td>
TUC_KON_410

</td></tr><tr></tr></table>

### 4.2 Änderungen in gemSpec_X.509_TSP

### 4.2.1 (6.6) Erneuerung von Zertifikaten der gSMC-K

A_21765-01 ersetzt A_21765:

**A_21765-01 - Erneuerung von gSMC-K-Zertifikaten: Zeitliche Vorgabe**

Ein TSP-X.509 nonQES für Komponenten MUSS zur Erneuerung von Zertifikaten der
gSMC-K (C.NK.VPN, C.AK.AUT und C.SAK.AUT) den Erneuerungsprozess auf Antrag der
gematik einleiten und dabei alle gSMC-K Zertifikate erneuern, die vor dem
01.01.2021 ausgegeben wurden. Das Laufzeitende der erneuerten Zertifikate MUSS
jeweils auf 31.12.2025 gesetzt werden. **[\<=]**

### 4.3 Änderungen in gemSpec_CVC_TSP

### 4.3.1 (5.2) Erneuerung von CV-Zertifikaten der gSMC-K

A_21774-01 ersetzt A_21774:

**A_21774-01 - Erneuerung von CV-Zertifikaten der gSMC-K: Profile, CHR und CXD**

Ein TSP-CVC für Komponenten MUSS bei der Erneuerung der CV-Zertifikate der
gSMC-K (C.SMC.AUT_CVC und C.SAK.AUTD_CVC) dieselben Zugriffsprofile (0 und 51)
und vor allem denselben CHR (inkl. ICCSN-Bezug) verwenden. Als Certificate
Expiration Date (CXD) MUSS dabei der 31.12.2025 angesetzt werden. **[\<=]**

### 4.4 (4.1.1.2) Änderungen in gemILF_PS -"ServerAuthentisierung"

Der Konnektor verwendet als TLS-Server-Zertifikat die auf der gSMC-K
gespeicherte\<PTV5\>bzw. vom Konnektor über die TI
erneuerte\</PTV5\>Identität ID.AK.AUT. Der CommonName dieses Zertifikats ist
mit der ICCSN und dem Herausgabedatum befüllt und nicht mit dem Hostnamen des
Konnektors. Eine optional durchzuführende Hostnamenprüfung durch das
Primärsystem kann daher ggf. nur daraufhin erfolgen, ob der Konnektor in der
LEI unter dem inSubject.AltNamesfestgelegtenDNSName="konnektor.konlan"
erreichbar ist.

\<PTV5\>Nach einer erfolgreichen Erneuerung der Identität ID.AK.AUT kann der
Zeitpunkt der Verwendung von dieser erneuerten Identität vom Administrator
frei gewählt werden. 

Der Konnektor sendet nach erfolgreicher automatischer Erneuerung der Zertifikate
ein Ereignis mit dem Topic SMC_K/UPDATE/SUCCESS. Das Primärsystem sollte diese
Information beziehen, den Anwender geeignet über den erfolgreichen
Zertifikatsupdate informieren und eine Warnung ausgeben, dass bei Verwendung
der ID.AK.AUT für die Server-Authentisierung eine Umstellung auf das neue
AK.AUT-Zertifikat manuell vom Administrator vorgenommen werden muss.

Darüber hinaus kann der Konnektor intern oder extern generierte Identitäten
als TLS-Server-Zertifikat verwenden. Der Administrator hat zwei Möglichkeiten,
die ID.AK.AUT für die Authentisierung gegenüber den Clientsystemen zu
ersetzen:

 ---> UL

Der CommonName dieser Zertifikate kann mit einem frei wählbaren Hostnamen des
Konnektors befüllt werden. Eine optional durchzuführende Hostnamenprüfung
durch das Primärsystem kann dann vollumfänglich erfolgen.

Der Zeitpunkt der Verwendung von generierten oder importierten Zertifikaten kann
vom Administrator frei gewählt werden und ist unabhängig vom Zeitpunkt der
Generierung oder des Imports. Der Administrator kann jederzeit zwischen der
Verwendung von generierten, importierten, erneuerten oder
ursprünglichen Zertifikaten der gSMC-K hin- und herschalten.\</PTV5\>

Für eine Prüfung des TLS-Server-Zertifikates des Konnektors durch das
Primärsystem sind verschiedene auch kombinierbare Umsetzungsvarianten möglich.

\<PTV5\>Die Prüfung der generierten oder importierten Zertifikate durch das
Primärsystem kann nicht gegen die TI-TSL oder die
TI-Komponenten-CA-Zertifikate erfolgen, da es sich um rein lokale Identitäten
außerhalb des TI-Vertrauensraums handelt.\</PTV5\>

Variante Prüfung gegen TI-Komponenten-SubCAs

Im Falle einer Prüfung der TLS-Server-Zertifikate des Konnektors gegen die
produktive Komponenten-SubCA der TI (z.B. am PS gespeichert in einer PEM-Datei)
ist der Lebenszyklus der in der TSL veröffentlichten TI-Komponenten-SubCA zu
beachten. Die SubCA ist 8 Jahre gültig und wird über diesen Zeitraum in der
TSL veröffentlicht. Nach spätestens drei Jahren werden jedoch
End-Entity-Komponenten-Zertifikate von einer neu hinzugefügten SubCA
abgeleitet, damit diese noch 5 Jahre gültig sind. Das PS muss also damit
rechnen, TLS-Server-Zertifikate von Konnektoren gegen mindestens drei
produktive SubCAs validieren zu können, weil es im Feld
End-Entity-Konnektorzertifikate geben kann, die aus unterschiedlichen SubCAs
abgeleitet sind. Am Laufzeitende einer TI-Komponenten-SubCA verliert diese ihre
Gültigkeit und wird aus der TSL entfernt. Die aktuelle TSL  ist
unterhttps://download.tsl.ti-dienste.de/verfügbar.

Darin befinden sich Zertifikate mit dem Namen GEM.KOMP-CA*, also z.B.
GEM.KOMP-CA1, GEM.KOMP-CA3, o.ä. Diese Zertifikate sind auch separat im
Verzeichnishttps://download.tsl.ti-dienste.de/verfügbar, um sie als Trusted CA
in der LE-Umgebung zu verwalten.  

\<PTV4\> Parallel dazu wird für die Einführung von elliptischen Kurven eine
zweite TSL () sowie entsprechende ECC verwendende Komponenten-CA-Zertifikate ()
von der gematik zur Verfügung gestellt. Diese neue TSL beruht auf ECC als
kryptografisches Verfahren, enthält jedoch zusätzlich alle für den
parallelen Einsatz von RSA und ECC erforderlichen RSA-Anteile. \</PTV4\>

Variante Etablierung Vertrauensbeziehung zwischen Konnektor und PS

Falls ein Administrator am Primärsystem das TLS-Server-Zertifikat des
Konnektors im Rahmen der Inbetriebnahme des Konnektors dem Zertifikatsspeicher
des lokalen PS-Rechners hinzufügen will (zur Etablierung einer
Vertrauensbeziehung zwischen einer Konnektor-Instanz und einer PS-Instanz in
einer einzelnen LE-Umgebung), wird an PS-Arbeitsplätzen das
Konnektor-TLS-Server-Zertifikat beim ersten TLS-Handshake mit dem Konnektor
einmalig akzeptiert und vom Primärsystem-Arbeitsplatz persistent gespeichert,
um die gesamte nachfolgende TLS-Kommunikation zwischen PS und Konnektor
abzusichern (so wie an einem Browser eine Ausnahmeregelung für CAs einer
Webseite gespeichert werden kann). 

Das Konnektor-TLS-Server-Zertifikat muss im Falle der Etablierung der
Vertrauensbeziehung zwischen Konnektor und Primärsystem-Arbeitsplatz nicht
durch das Primärsystem gegen die Komponenten-SubCAs aus der TSL geprüft
werden. Im Falle eines Konnektorwechsels muss dieses Pairing mit dem neuen
Konnektor erneut durchgeführt werden. Beim Austausch konnektoreigener
Zertifikate, z. B. im Zuge eines Wechsels der TLS-Server-Zertifikate des
Konnektors \<PTV4\>aufgrund der Umstellung auf Zertifikate, die ECC
verwenden,\</PTV4\>  muss die Vertrauensbeziehung erneut mit den neu
erstellten End-Entity-Zertifikaten hergestellt werden.

\<PTV5\>Falls ein Administrator ein konnektorextern generiertes und in den
Konnektor importiertes Zertifikat, ein im Konnektor generiertes Zertifikat oder
die erneuerte ID.AK.AUT für die Server-Authentisierung verwendet, so ist das
Zertifikat am Primärsystem entweder bereits bekannt (z.B. durch die Verwendung
einer PKI), oder es wird im Rahmen der Inbetriebnahme des Konnektors dem
Zertifikatsspeicher des lokalen PS-Rechners wie oben beschrieben
hinzugefügt.\</PTV5\>

Änderung in Absatz 4.1.4: Neuer Absatz:

\<PTV5\>  
4.1.4.7 Informationen zu Fehlern bei der Zertifikatserneuerung
(Laufzeitverlängerung gSMC-K)  
Der Konnektor stellt Informationen über ggf.
aufgetretene Fehler bei der Erneuerung der Zertifikate der gSMC-K über den
Systeminformationsdienst zur Verfügung, insbesondere über den Topic
SMC_K/DOWNLOAD/ERROR und SMC_K/UPDATE/ERROR.

Diese Informationen sollten gemäß den Betriebsprozessen des Primärsystems
beim Leistungserbringer sorgfältig berücksichtigt werden, da eine fehlerhafte
oder unvollständige Erneuerung der Zertifikate der gSMC-K zu einem Ausfall der
TI-Anwendungsfälle führen und einen Konnektor-Tausch notwendig machen
kann. Das Primärsystem sollte diese Informationen daher beziehen (siehe Kap.
4.1.4.3) und den Anwender geeignet informieren.

Ebenso stellt der Konnektor Informationen über aufgetretene Fehler bei der
Reregistrierung mit erneuertem Zertifikat zur Verfügung, insbesondere über
den Topic SMC_K/REGISTER/ERROR. Bei Auftreten des Fehlers mit Parameter
Fail=No_Smcb muss in der Leistungserbringerumgebung dafür gesorgt werden, dass
eine freigeschaltete SMC-B verfügbar ist, die der Konnektor für die
Re-Registrierung verwenden kann.\</PTV5\>

### 5 Anhang A – Verzeichnisse

### 5.1 Abkürzungen

<table><tr><th>
Kürzel

</th><th>
Erläuterung

</th></tr><tr></tr><tr></tr><tr></tr><tr></tr><tr></tr></table>

### 5.2 Referenzierte Dokumente

### 5.2.1 Dokumente der gematik

Die nachfolgende Tabelle enthält die Bezeichnung der in dem vorliegenden
Dokument referenzierten Dokumente der gematik zur Telematikinfrastruktur. Der
mit der vorliegenden Version korrelierende Entwicklungsstand dieser Konzepte
und Spezifikationen wird pro Release in einer Dokumentenlandkarte definiert;
Version und Stand der referenzierten Dokumente sind daher in der nachfolgenden
Tabelle nicht aufgeführt. Deren zu diesem Dokument jeweils gültige
Versionsnummern sind in der aktuellen, von der gematik veröffentlichten
Dokumentenlandkarte enthalten, in der die vorliegende Version aufgeführt wird.

<table><tr><td>
[Quelle]

</td><td>
Herausgeber: Titel

</td></tr><tr><td>
[gemGlossar]

</td><td>
gematik: Glossar der Telematikinfrastruktur

</td></tr><tr><td>
</td><td>
</td></tr></table>

### 5.2.2 Weitere Dokumente

<table><tr><td>
[Quelle]

</td><td>
Herausgeber (Erscheinungsdatum): Titel

</td></tr><tr><td>
</td><td>
</td></tr><tr><td>
</td><td>
</td></tr></table>





[Dokumentinformationen]: #dokumentinformationen
[Inhaltsverzeichnis]:    #inhaltsverzeichnis
[1]:                     #1-einordnung-des-dokuments
[1.1]:                   #11-zielsetzung
[1.2]:                   #12-zielgruppe
[1.3]:                   #13-abgrenzungen
[1.4]:                   #14-methodik
[1.4.1]:                 #141-anforderungen
[1.4.2]:                 #142-hinweise-auf-offene-punkte
[2]:                     #2-technisches-konzept-laufzeitverlängerung-gsmc-k
[2.1]:                   #21-zusammenfassung
[2.1.1]:                 #211-betroffene-komponenten-und-zertifikate
[2.1.2]:                 #212-lösung
[2.1.3]:                 #213-wiederholbarkeit-der-aktion
[2.1.4]:                 #214-zusammenspiel-mit-der-ecc-migration-der-konnektoren
[2.1.5]:                 #215-bedeutung-der-laufzeitverlängerung-der-gsmc-k-für-robustheit-akzeptanz-und-zukunftsfähigkeit-der-ti
[2.2]:                   #22-identität-idnkvpn-relevant-für-konnektor---vpn-zugangsdienst
[2.3]:                   #23-identität-idakaut-relevant-für-konnektor---ps
[2.4]:                   #24-identität-sakautd_cvc-relevant-für-c2c-mit-hba
[2.5]:                   #25-identität-idsakaut-relevant-für-ehealth-kartenterminal
[3]:                     #3-operative-umsetzung
[3.1]:                   #31-bereitstellung-des-zertifikats-downloads
[3.2]:                   #32-bereitstellung-der-zertifikate
[3.3]:                   #33-sperrprozesse
[3.4]:                   #34-offline-konnektoren
[4]:                     #4-spezifikation
[4.1]:                   #41-änderungen-in-gemspec_kon
[4.1.1]:                 #411-31-konnektoridentität-und-gsmc-k
[4.1.2]:                 #412-311-erneuerung-der-zertifikate-der-gsmc-k
[4.1.3]:                 #413-33-betriebszustand
[4.1.4]:                 #414-435--neustart-und-werksreset
[4.1.5]:                 #415-identität-idnkvpn-relevant-für-konnektor---vpn-zugangsdienst
[4.1.5.1]:               #4151-437-re-registrierung-des-konnektors-mit-neuem-nk-zertifikat
[4.1.6]:                 #416-351-identität-idakaut-relevant-für-konnektor---ps-351-betriebsaspekte
[4.1.7]:                 #417-7-anhang-f-events
[4.2]:                   #42-änderungen-in-gemspec_x509_tsp
[4.2.1]:                 #421-66-erneuerung-von-zertifikaten-der-gsmc-k
[4.3]:                   #43-änderungen-in-gemspec_cvc_tsp
[4.3.1]:                 #431-52-erneuerung-von-cv-zertifikaten-der-gsmc-k
[4.4]:                   #44-4112-änderungen-in-gemilf_ps--serverauthentisierung
[5]:                     #5-anhang-a-–-verzeichnisse
[5.1]:                   #51-abkürzungen
[5.2]:                   #52-referenzierte-dokumente
[5.2.1]:                 #521-dokumente-der-gematik
[5.2.2]:                 #522-weitere-dokumente
[Abbildung-1]:           gemF_Laufzeitverlangerung_gSMC-K_V1.1.0.attachments/16325900127099767966.png
[Abbildung-2]:           gemF_Laufzeitverlangerung_gSMC-K_V1.1.0.attachments/10565454007505814899.png
[Img-003]:               gemF_Laufzeitverlangerung_gSMC-K_V1.1.0.attachments/16325900127099767966.png
[Tbl-001]:               #Tbl-001 (&93834810721720)
[Tabelle -1]:            #Tabelle -1 (&93834781493752)
[Tbl-003]:               #Tbl-003 (&93834771053336)
[Tabelle-3]:             #Tabelle-3 (&93834771073544)
[Tabelle-4]:             #Tabelle-4 (&93834774918320)
[Tabelle-5]:             #Tabelle-5 (&93834774933064)
[Tabelle -6]:            #Tabelle -6 (&93834785733488)
[Tbl-008]:               #Tbl-008 (&93834785788160)
[Tabelle-8]:             #Tabelle-8 (&93834785806632)
[Tbl-010]:               #Tbl-010 (&93834778322392)
[Tbl-011]:               #Tbl-011 (&93834775429712)
[Tbl-012]:               #Tbl-012 (&93834775438864)
[https://download.tsl.ti-dienste.de/]: https://download.tsl.ti-dienste.de/ (&93834778308000)
[https://download.tsl.ti-dienste.de/]: https://download.tsl.ti-dienste.de/ (&93834778309552)
