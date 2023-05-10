
Elektronische Gesundheitskarte und Telematikinfrastruktur

### 

- Klassifizierung: öffentlich
- Referenzierung: gemSpec_SMC-B_ObjSys_G2.1
- Revision: 548770
- Stand: 10.09.2020
- Status: freigegeben
- Version: 5.0.0

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
4.0.0

</td><td>
21.04.17

</td><td>
Einarbeitung Anpassungen Kartengeneration G2.1

</td><td>
gematik

</td></tr><tr><td>
4.1.0

</td><td>
18.12.17

</td><td>
Einarbeitung von Errata R1.6.4-2 sowie Anpassungen auf Grundlage von P 15.1

</td><td>
gematik

</td></tr><tr><td>
4.2.0

</td><td>
14.05.18

</td><td>
Anpassungen auf Grundlage von P 15.3

</td><td>
gematik

</td></tr><tr><td>
4.3.0

</td><td>
26.10.18

</td><td>
Einarbeitung P 15.9 (C_6562, C_6622)

</td><td>
gematik

</td></tr><tr><td>
4.4.0

</td><td>
15.05.19

</td><td>
Einarbeitung P18.1

</td><td>
gematik

</td></tr><tr><td>
4.5.0

</td><td>
30.06.20

</td><td>
Anpassungen gemäß Änderungsliste P22.1

</td><td>
gematik

</td></tr><tr><td>
5.0.0

</td><td>
10.09.20

</td><td>
Anpassungen gemäß C_10274 (P22.3)

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
    - [1.5.1] Nomenklatur
    - [1.5.2] Verwendung von Schüsselworten
    - [1.5.3] Komponentenspezifische Anforderungen
- [2] Optionen und Ausprägungen
  - [2.1] Option_Erstellung_von_Testkarten
  - [2.2] Ausprägung ohne Zugriff auf die eGK
  - [2.3] SMC-B mit kontaktloser Schnittstelle
- [3] Lebenszyklus von Karte und Applikation
- [4] Anwendungsübergreifende Festlegungen
  - [4.1] Mindestanzahl logischer Kanäle
  - [4.2] Unterstützung Onboard-RSA-Schlüsselgenerierung
  - [4.3] Unterstützung der kontaktlosen Schnittstelle (SMC-B CL)
  - [4.4] Attributstabellen
    - [4.4.1] Attribute eines Ordners
    - [4.4.2] Attribute einer Datei (EF)
  - [4.5] Zugriffsregeln für besondere Kommandos
  - [4.6] Attributswerte und Personalisierung
  - [4.7] Kartenadministration
- [5] Spezifikation grundlegender Applikationen
  - [5.1] Attribute des Objektsystems
    - [5.1.1] ATR-Kodierung und technische Eigenschaften
  - [5.2] Allgemeine Struktur
  - [5.3] Root, die Wurzelapplikation MF
    - [5.3.1] MF / EF.ATR
    - [5.3.2] MF / EF.DIR
    - [5.3.3] MF / EF.CardAccess (SMC-B CL)
    - [5.3.4] MF / EF.GDO
    - [5.3.5] MF / EF.Version2
    - [5.3.6] MF / EF.C.CA_SMC.CS.E256
    - [5.3.7] MF / EF.C.SMC.AUTR_CVC.E256
    - [5.3.8] MF / EF.C.SMC.AUTD_RPE_CVC.E256
    - [5.3.9] MF / PIN.SMC
    - [5.3.10] MF / PrK.SMC.AUTR_CVC.E256
    - [5.3.11] MF / PrK.SMC.AUTD_RPE_CVC.E256
    - [5.3.12] Sicherheitsanker zum Import von CV-Zertifikaten
      - [5.3.12.1] MF / PuK.RCA.CS.E256
    - [5.3.13] Asymmetrische Kartenadministration
      - [5.3.13.1] MF / PuK.RCA.ADMINCMS.CS.E256
    - [5.3.14] Symmetrische Kartenadministration
      - [5.3.14.1] MF / SK.CMS.AES128
      - [5.3.14.2] MF / SK.CMS.AES256
      - [5.3.14.3] MF / SK.CUP.AES128
      - [5.3.14.4] MF / SK.CUP.AES256
    - [5.3.15] MF / SK.CAN (SMC-B CL)
  - [5.4] Die ESIGN-Anwendung DF.ESIGN
    - [5.4.1] Dateistruktur und Dateiinhalt
    - [5.4.2] MF / DF.ESIGN (Krypto-Anwendung ESIGN)
      - [5.4.2.1] MF / DF.ESIGN / EF.C.HCI.OSIG.R2048
      - [5.4.2.2] MF / DF.ESIGN / EF.C.HCI.AUT.R2048
      - [5.4.2.3] MF / DF.ESIGN / EF.C.HCI.ENC.R2048
      - [5.4.2.4] MF / DF.ESIGN / PrK.HCI.OSIG.R2048
      - [5.4.2.5] MF / DF.ESIGN / PrK.HCI.AUT.R2048
      - [5.4.2.6] MF / DF.ESIGN / PrK.HCI.ENC.R2048
      - [5.4.2.7] MF / DF.ESIGN / EF.C.HCI.OSIG.E256
      - [5.4.2.8] MF / DF.ESIGN / EF.C.HCI.AUT.E256
      - [5.4.2.9] MF / DF.ESIGN / EF.C.HCI.ENC.E256
      - [5.4.2.10] MF / DF.ESIGN / PrK.HCI.OSIG.E256
      - [5.4.2.11] MF / DF.ESIGN / PrK.HCI.AUT.E256
      - [5.4.2.12] MF / DF.ESIGN / PrK.HCI.ENC.E256
  - [5.5] Laden neuer Anwendungen, Anlegen von EFs und Laden von Zertifikaten nach Ausgabe der SMC-B
- [6] Anhang A – Verzeichnisse
  - [6.1] Abkürzungen
  - [6.2] Glossar
  - [6.3] Abbildungsverzeichnis
  - [6.4] Tabellenverzeichnis
  - [6.5] Referenzierte Dokumente
    - [6.5.1] Dokumente der gematik
    - [6.5.2] Weitere Dokumente

### 1 Einordnung des Dokuments

### 1.1 Zielsetzung

Die vorliegende Spezifikation definiert die Anforderungen an das Objektsystem
der Sicherheitsmodulkarte SMC-B. Es beinhaltet die Definition der Anforderungen
an die Objektstruktur, die Beschreibung der Kartenschnittstelle der
Sicherheitsmodulkarte SMC-B für Institutionen im Gesundheitswesen.

Das Dokument berücksichtigt dabei:

 ---> UL

Dieses Dokument spezifiziert Anwendungen der Sicherheitsmodulkarte SMC-B unter
den folgenden, rein kartenorientierten Gesichtspunkten:

 ---> UL

Somit stellt dieses Dokument auf unterster technischer Ebene eine Reihe von
Datencontainern bereit. Zudem werden hier die Sicherheitsmechanismen für diese
Datencontainer festgelegt, d. h. es wird festgelegt, welchen Instanzen es
unter welchen Voraussetzungen möglich ist, auf Inhalte der Container
zuzugreifen. Die Semantik und die Syntax der Inhalte in Datencontainern ist
dagegen nicht Gegenstand dieses Dokumentes (siehe dazu auch Kapitel 1.4).

### 1.2 Zielgruppe

Das Dokument richtet sich an

 ---> UL

### 1.3 Geltungsbereich

Dieses Dokument enthält normative Festlegungen zur Telematikinfrastruktur des
deutschen Gesundheitswesens. Der Gültigkeitszeitraum der vorliegenden Version
und deren Anwendung in Zulassungsverfahren wird durch die gematik GmbH in
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

Die Basiskommandos, die Grundfunktionen des Betriebssystems sowie die
grundlegenden Sicherheitsfunktionen und -algorithmen (hard facts) für alle
Karten des Gesundheitswesens (eGK, HBA, SMC-B, gSMC-K, gSMC-KT) werden in der
Spezifikation des Card Operating System (COS) detailliert beschrieben
[gemSpec_COS]. Die Spezifikation [gemSpec_COS] ist Grundlage der Entwicklung
der Kommandostrukturen und Funktionen für die Chipkartenbetriebssysteme.

Die optische Gestaltung für alle SMCs und damit auch für die SMC-B wird in dem
Dokument „Gemeinsame optische Merkmale der SMC“ [gemSpec_SMC_OPT] wird
festgelegt.

### 1.5 Methodik

### 1.5.1 Nomenklatur

<table><tr><th>
‘1D’

</th><th>
Hexadezimale Zahlen und Oktettstrings werden in Hochkommata eingeschlossen.

</th></tr><tr><td>
x || y

</td><td>
Das Symbol || steht für die Konkatenierung von Oktettstrings oder
Bitstrings:    

‘1234’   ||   ‘5678’   =   ‘12345678’.

</td></tr></table>

In [gemSpec_COS] wurde ein objektorientierter Ansatz für die Beschreibung der
Funktionalität des Betriebssystems gewählt. Deshalb wurde dort der Begriff
"Passwortobjekt" verwendet, wenn Instanzen für eine Benutzerverifikation
besprochen wurden. Da in diesem Dokument lediglich numerische Ziffernfolgen als
Verifikationsdaten eines Benutzers verwendet werden, wird hier statt
Passwortobjekt vielfach der Begriff PIN gewählt, wenn keine Gefahr besteht,
dass es zu Verwechslungen kommt zwischen den Verifikationsdaten und der Instanz
des Objektes, in denen sie enthalten sind (zur Erinnerung: Ein Passwortobjekt
enthält neben den Verifikationsdaten auch einen Identifier, eine
Zugriffsregel, eine PUK, …).

Der Begriff "Wildcard" wird in diesem Dokument im Sinn eines "beliebigen,
herstellerspezifischen Wertes, der nicht anderen Vorgaben widerspricht"
verwendet.

Für die Authentisierung der Zugriffe durch ein CMS auf die dafür vorgesehenen
Objekte können entweder symmetrische Verfahren mit AES-Schlüsseln oder
alternativ asymmetrische Verfahren mit CV-Zertifikaten verwendet werden. Für
beide Verfahren sind die Schlüsselobjekte in dieser Spezifikation spezifiziert.

Die in diesem Dokument referenzierten Flaglisten cvc_FlagList_CMS und
cvc_FlagList_TI sind normativ in [gemSpec_PKI#6.7.5] und die dazugehörenden
OIDs oid_cvc_fl_cms und oid_cvc_fl_ti sind normativ in [gemSpec_OID] definiert.

Gemäß [gemSpec_COS#(N022.400)] wird die Notwendigkeit einer externen
Rollenauthentisierung für Karten der Generation 2 mit einer Flaglist wie folgt
dargestellt: AUT(OID, FlagList) wobei OID stets aus der Menge {oid_cvc_fl_cms,
oid_cvc_fl_ti} ist und FlagList ein sieben Oktett langer String, in welchem im
Rahmen dieses Dokumentes genau ein Bit gesetzt ist. Abkürzend wird deshalb in
diesem Dokument lediglich die Nummer des gesetzten Bits angegeben in Verbindung
mit der OID. Ein gesetztes Bit i in Verbindung mit der oid_cvc_fl_cms wird im
Folgenden mit flagCMS.i angegeben und ein gesetztes Bit j in Verbindung mit der
oid_cvc_fl_ti wird im Folgenden mit flagTI.j angegeben.

Beispiele:

<table><tr><th>
Langform

</th><th>
Kurzform

</th></tr><tr><td>
AUT(oid_cvc_fl_cms,’00010000000000’)

</td><td>
flagCMS.15

</td></tr><tr><td>
AUT(oid_cvc_fl_ti, ‘00010000000000’) OR AUT(oid_cvc_fl_ti,
‘00008000000000’)

</td><td>
flagTI.15 OR flagTI.16

</td></tr><tr><td>
PWD(PIN)  AND

[

    AUT(oid_cvc_fl_cms,’00010000000000’)

    OR

    AUT(oid_cvc_fl_ti, ‘00008000000000’)

]

</td><td>
PWD(PIN)   AND   [flagCMS.15 OR flagTI.16)]

</td></tr><tr><td>
SmMac(oid_cvc_fl_cms, ’00800000000000’)

</td><td>
SmMac(flagCMS.08)

</td></tr></table>

Um komplexe Zugriffsregeln für Zugriffe in den einzelnen Tabellen
übersichtlich darstellen zu können, werden folgende Abkürzungen verwendet:

<table><tr><th>
Kurzform

</th><th>
Langform

</th></tr><tr><td>
AUT_CMS

</td><td>
{            SmMac(SK.CMS.AES128)

    OR    SmMac(SK.CMS.AES256)

    OR    SmMac(flagCMS.08)  
}   

AND    SmCmdEnc   

AND    SmRspEnc

</td></tr><tr><td>
AUT_CUP

</td><td>
{            SmMac(SK.CUP.AES128)

    OR    SmMac(SK.CUP.AES256)}

    OR    SmMac(flagCMS.10)  
}    AND    SmCmdEnc   

AND    SmRspEnc

</td></tr><tr><td>
AUT_PACE

</td><td>
SmMac(SK.CAN)   

AND    SmCmdEnc   

AND    SmRspEnc

</td></tr></table>

Die Zugriffsregel AUT_CMS dient der Administration und kann nur durch den
Betreiber eines CMS  erfüllt werden.

Die Zugriffsregel AUT_CUP dient der Erneuerung von Zertifikaten und kann nur
durch den Betreiber eines CUpS erfüllt werden.

Die Zugriffsregel AUT_PACE dient der Absicherung der kontaktlosen Schnittstelle
und kann durch den Kartenverwender erfüllt werden.

In der obigen Tabelle, wie auch an anderen Stellen im Dokument werden aus
Gründen der besseren Lesbarkeit häufig mehrere Zugriffsarten zusammengefasst
und dafür eine Zugriffsbedingung angegeben. Beispielsweise (READ, UPDATE) nur,
wenn SmMac(CAN) AND SmCmdEnc AND SmRspEnc. Dabei ist folgendes zu beachten:

Dabei ist folgendes zu beachten:

 ---> OL

### 1.5.2 Verwendung von Schüsselworten

Anforderungen als Ausdruck normativer Festlegungen werden durch eine eindeutige
ID in eckigen Klammern sowie die dem RFC 2119 [RFC2119] entsprechenden, in
Großbuchstaben geschriebenen deutschen Schlüsselworte MUSS, DARF NICHT, SOLL,
SOLL NICHT, KANN gekennzeichnet

Sie werden im Dokument wie folgt dargestellt:

\<AFO-ID\> - \<Titel der Afo\>Text / Beschreibung[ \<=]

Dabei umfasst die Anforderung sämtliche innerhalb der Textmarken angeführten
Inhalte.

Abwandlungen von „MUSS“ zu „MÜSSEN“ etc. sind der Grammatik geschuldet.
Da im Beispielsatz „Eine leere Liste DARF NICHT ein Element besitzen.“ die
Phrase „DARF NICHT“ semantisch irreführend wäre (wenn nicht ein, dann
vielleicht zwei?), wird in diesem Dokument stattdessen „Eine leere Liste DARF
KEIN Element besitzen.“ verwendet.

### 1.5.3 Komponentenspezifische Anforderungen

Da es sich beim vorliegenden Dokument um die Spezifikation einer Schnittstelle
zwischen mehreren Komponenten handelt, ist es möglich, die Anforderungen aus
der Sichtweise jeder Komponente zu betrachten. Die normativen Abschnitte tragen
deshalb eine Kennzeichnung, aus wessen Sichtweise die Anforderung primär
betrachtet wird.

<table><tr><th>
Komponente

</th><th>
Beschreibung

</th></tr><tr><td>
K_Initialisierung

</td><td>
Instanz, welche eine Chipkarte im Rahmen der Initialisierung befüllt

</td></tr><tr><td>
K_Personalisierung

</td><td>
Instanz, die eine Chipkarte im Rahmen einer Produktion individualisiert

</td></tr></table>

### 2 Optionen und Ausprägungen

Dieses Unterkapitel listet Funktionspakete auf, die für eine Zulassung einer
SMC-B der Generation 2 nicht zwingend erforderlich sind.

### 2.1 Option_Erstellung_von_Testkarten

**Card-G2-A_3370 - K_Personalisierung K_Initialisierung Vorgaben für die
Option_Erstellung_von_Testkarten**

Die SMC-B KANN als Testkarte ausgestaltet werden. Soweit in dieser Spezifikation
Anforderungen an Testkarten von den Anforderungen an Produktivkarten abweichen,
wird dies an der entsprechenden Stelle aufgeführt. **[\<=]**

### 2.2 Ausprägung ohne Zugriff auf die eGK

SMC-Bs können auch in Organisationen eingesetzt werden, die an der TI
teilnehmen, aber nicht zum Zugriff auf die eGK berechtigt sind. Um zu
verhindern, dass eine solche SMC-B den Zugriff auf eine eGK freischalten kann,
wird das Rollenzertifikat EF.C.SMC.AUTR_CVC.E256 bei der Personalisierung
entweder gar nicht oder mit Nullen befüllt. Ein zugehöriger privater
Schlüssel bleibt herstellerspezifisch „unbefüllt“ oder wird mit
nicht-nutzbaren Dummy-Daten befüllt.

Dies wird in den entsprechenden Personalisierungsfestlegungen mit dem Zusatz
„Ausprägung_ORG“ gekennzeichnet.

### 2.3 SMC-B mit kontaktloser Schnittstelle

Die SMC-B kann mit der kontaktlosen Schnittstelle gemäß [gemSpec_COS] und
ISO/IEC 14443 ausgestattet sein. SMC-B mit kontaktloser Schnittstelle müssen
alle optionalen Anforderungen mit der Kennzeichnung (SMC-B CL) zusätzlich zu
den nicht gekennzeichneten Anforderungen umsetzen.

### 3 Lebenszyklus von Karte und Applikation

Diese Spezifikation gilt nicht für die Vorbereitungsphase von Applikationen
oder deren Bestandteile. Sie beschreibt lediglich den Zustand des Objektsystems
in der Nutzungsphase.

Die Nutzungsphase einer Applikation oder eines Applikationsbestandteils beginnt,
sobald sich ein derartiges Objekt, wie in der Spezifikation der Anwendung
definiert, verwenden lässt. Die Nutzungsphase einer Applikation oder eines
Applikationsbestandteils endet, wenn das entsprechende Objekt gelöscht oder
terminiert wird.

Hinweis 1: Die in diesem Kapitel verwendeten Begriffe "Vorbereitungsphase" und
"Nutzungsphase" werden in [gemSpec_COS#4] definiert.

### 4 Anwendungsübergreifende Festlegungen

Zur Umsetzung der SMC-B ist ein Betriebssystem hinreichend, welches folgende
Optionen enthält:

 ---> UL

Bei Verwendung der kontaktlosen Schnittstelle zusätzlich:

 ---> UL

### 4.1 Mindestanzahl logischer Kanäle

**Card-G2-A_2196 - K_Initialisierung: Anzahl logischer Kanäle**

Für die Anzahl logischer Kanäle, die von einer SMC-B zu unterstützen ist,
gilt:

 ---> OL

**[\<=]**

Jeder Kanal besitzt seinen eigenen unabhängigen Sicherheitsstatus, d.h., eine
externe Authentisierung der Rollenkennung in einem logischen Kanal setzt keinen
Sicherheitszustand in irgendeinem anderen Kanal.

### 4.2 Unterstützung Onboard-RSA-Schlüsselgenerierung

**Card-G2-A_3849 - K_Personalisierung und K_Initialisierung: Unterstützung
Onboard-RSA-Schlüsselgenerierung**

Das COS einer SMC-B MUSS die Option_RSA_KeyGeneration implementieren. **[\<=]**

### 4.3 Unterstützung der kontaktlosen Schnittstelle (SMC-B CL)

**A_19387 - (SMC-B CL) K_Initialisierung: Unterstützung der kontaktlosen
Schnittstelle**

Das COS einer SMC-B MUSS die Schnittstelle zur kontaktlosen Datenübertragung
gemäß ISO/IEC 14443 (siehe [gemSpec_COS]) implementieren. **[\<=]**

### 4.4 Attributstabellen

**Card-G2-A_2134 - K_Initialisierung: Änderung von Zugriffsregeln**

Die in diesem Dokument definierten Zugriffsregeln DÜRFEN in der Nutzungsphase
NICHT veränderbar sein. **[\<=]**

**Card-G2-A_2135 - K_Initialisierung: Verwendung von SE**

Alle Objekte MÜSSEN sich in SE#1 wie angegeben verwenden lassen. **[\<=]**

**Card-G2-A_3189 - K_Initialisierung: Verwendbarkeit der Objekte in anderen SEs**

Jedes Objekt KANN in SE verwendbar sein, die verschieden sind von SE#1. **[\<=]**

**Card-G2-A_3190 - K_Initialisierung: Eigenschaften der Objekte in anderen SEs**

Falls ein Objekt in einem von SE#1 verschiedenen SE verwendbar ist, dann MUSS es
dort dieselben Eigenschaften wie in SE#1 besitzen. **[\<=]**

### 4.4.1 Attribute eines Ordners

**Card-G2-A_2136-01 - K_Initialisierung: Ordnerattribute**

Enthält eine Tabelle mit Ordnerattributen einen oder
mehrereapplicationIdentifier(AID), dann MUSS sich dieser Ordner mittels aller
angegebenen AID selektieren lassen. **[\<=]**

**Card-G2-A_3647 - K_Initialisierung: Herstellerspezifischer
ApplicationIdentifier**

Enthält eine Tabelle mit Ordnerattributen keinenapplicationIdentifier(AID), so
KANN diesem Ordner herstellerspezifisch ein beliebiger AID zugeordnet werden.
**[\<=]**

**Card-G2-A_3648 - K_Initialisierung: Fehlender FileIdentifier**

Enthält eine Tabelle mit Ordnerattributen keinenfileIdentifier(FID), so DARF
dieser Ordner NICHT mittels einesfileIdentifieraus dem Intervall gemäß
[gemSpec_COS#8.1.1] selektierbar sein, es sei denn, es handelt sich um den
Ordnerroot, dessen optionalerfileIdentifierden Wert ‘3F00’ besitzen MUSS.
**[\<=]**

**Card-G2-A_3649 - K_Initialisierung: Herstellerspezifischer FileIdentifier**

Enthält eine Tabelle mit Ordnerattributen keinenfileIdentifier(FID), so KANN
diesem Ordner ein beliebigerfileIdentifieraußerhalb des Intervalls gemäß
[gemSpec_COS#8.1.1] zugeordnet werden. **[\<=]**

### 4.4.2 Attribute einer Datei (EF)

**Card-G2-A_2137 - K_Initialisierung: Dateiattribute**

Enthält eine Tabelle mit Attributen einer Datei keinenshortFileIdentifier, so
DARF sich dieses EF NICHT mittelsshortFileIdentifieraus dem Intervall gemäß
[gemSpec_COS#8.1.2] selektieren lassen. **[\<=]**

**Card-G2-A_2668 - K_Initialisierung und K_Personalisierung: Wert von
„positionLogicalEndOfFile“**

Für transparente EFs MUSS der Wert von „positionLogicalEndOfFile“, soweit
nicht anders spezifiziert, auf die Anzahl der tatsächlich belegten Bytes
gesetzt werden. **[\<=]**

### 4.5 Zugriffsregeln für besondere Kommandos

Gemäß [gemSpec_COS] gilt:

**Card-G2-A_2669 - K_Initialisierung: Zugriffsregeln für besondere Kommandos**

Die Zugriffsbedingung für die Kommandos GET CHALLENGE, LIST PUBLIC KEY, MANAGE
SECURITY ENVIRONMENT und SELECT MUSS stets ALWAYS sein, unabhängig
vomlifeCycleStatusund unabhängig vom aktuellen Security Environment.​​ **[\<=]**

### 4.6 Attributswerte und Personalisierung

Die in diesem Dokument festgelegten Attribute der Objekte berücksichtigen
lediglich fachlich motivierte Use Cases. Zum Zwecke der Personalisierung ist es
unter Umständen und je nach Personalisierungsstrategie erforderlich, von den
in diesem Dokument festgelegten Attributswerten abzuweichen.

Beispielsweise ist es denkbar, dass für die Datei EF.GDO das Attribut
lifeCycleStatus nach der Initialisierung auf dem in [gemSpec_COS] nicht
normativ geforderten Wert „Initialize“ steht und für diesen Wert die
Zugriffsregeln etwa ein Update Binary Kommando erlauben. In diesem Fall wiche
nicht nur der Wert des Attributes lifeCycleStatus, sondern auch der des
Attributes interfaceDependentAccessRules von den Vorgaben dieses Dokumentes ab.
Nach Abschluss der Personalisierung wäre dann der Wert des Attributes
lifeCycleStatus bei korrekter Personalisierung spezifikationskonform auf dem
Wert „Operational state (activated)“ aber in interfaceDependentAccessRules
fände sich für den Zustand „Initialize“ immer noch „Update Binary“.
Im Rahmen einer Sicherheitsbetrachtung wäre diese Abweichung als unkritisch
einzustufen, wenn sichergestellt ist, dass der Zustand „Initialize“
unerreichbar ist.

Denkbar wäre auch, dass die Personalisierung so genannte Ini-Tabellen und
spezielle Personalisierungskommandos nutzt, die Daten, die mit dem Kommando
übergeben werden, an durch die Ini-Tabelle vorgegebene Speicherplätze
schreibt. In dieser Variante wären die Attribute von EF.GDO auf den ersten
Blick konform zu dieser Spezifikation, obwohl durch das
Personalisierungskommando ein Zugriff auf das Attribut body bestünde, der so
eventuell nicht in den Zugriffsregeln sichtbar wird und damit gegen die
allgemeine Festlegung „andere (Kommandos) NEVER“ verstieße. Im Rahmen
einer Sicherheitsbetrachtung wäre diese Abweichung als unkritisch einzustufen,
wenn sichergestellt ist, dass die Personalisierungskommandos nach Abschluss der
Personalisierung irreversibel gesperrt sind.

Die folgende Anforderung ermöglicht herstellerspezifische
Personalisierungsprozesse:

**Card-G2-A_3375 - K_Initialisierung und K_Personalisierung: Abweichung von
Festlegungen zum Zwecke der Personalisierung**

Zur Unterstützung herstellerspezifischer Personalisierungsprozessen KÖNNEN die
Werte von Attributen eines Kartenproduktes von den Festlegungen dieses
Dokumentes abweichen. Hierbei MÜSSEN Abweichungen auf solche beschränkt sein,
die hinsichtlich ihrer Wirkung in der personalisierten Karte sowohl fachlich
wie sicherheitstechnisch der in der Spezifikation vorgegebenen Werten
entsprechen. **[\<=]**

**Card-G2-A_3527 - K_Initialisierung: Schlüsselgenerierung auf der Karte**

Die SMC-B MUSS die Generierung von asymmetrischen Schlüsselpaaren auf der Karte
ermöglichen. **[\<=]**

**Card-G2-A_3528 - K_Initialisierung: Weitere Verfahren zur Personalisierung von
Schlüsseln**

Die SMC-B KANN andere Verfahren als das in Card-G2-A_3527 genannte zur
Personalisierung asymmetrischer Schlüsselpaare unterstützen. **[\<=]**

**Card-G2-A_3524 - K_Personalisierung: Schlüsselgenerierung auf der Karte**

Wenn ein privater Schlüssel für die SMC-B zu personalisieren ist, dann MUSS
das Schlüsselpaar von der Smartcard selbst erzeugt werden. Es MUSS
sichergestellt sein, dass der private Teil des Schlüssels die Smartcard nie
verlässt. **[\<=]**

### 4.7 Kartenadministration

In den Kapiteln 5.3.15 und 5.3.16 sind die Objekte für die zwei verschiedenen
Verfahren zur Absicherung der Kommunikation zwischen einem
Kartenadministrationssystem (z.B. einem CUpS) und einer Karte beschrieben, die
bei der Ausgabe der Karte angelegt werden müssen.

**Card-G2-A_3035 - Absicherung der Kartenadministration**

Bei der Personalisierung MUSS der Schlüssel PuK.RCA.ADMINCMS.CS für die
asymmetrische Authentifizierung des Kartenadministrationssystems in die Karte
eingebracht werden. **[\<=]**

**Card-G2-A_3588 - Symmetrische Kartenadministration**

Bei der Personalisierung KÖNNEN die Schlüssel (SK.CMS und SK.CUP) für die
symmetrische Authentifizierung des Kartenadministrationssystems in die Karte
eingebracht werden. **[\<=]**

**Card-G2-A_3589 - Schlüsselspeicherung**

Der Kartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der Kartenpersonalisierer MUSS
sicherstellen, dass die Schlüssel zur Absicherung der Kartenadministration
während der gesamten Nutzungsdauer der SMC-B sicher verwahrt werden und bei
Bedarf an ein Kartenadministrationssystem (z.B. ein CUpS) übergeben werden
können. **[\<=]**

### 5 Spezifikation grundlegender Applikationen

Zu den grundlegenden Applikationen der Sicherheitsmodulkarte SMC-B zählen:

 ---> UL

### 5.1 Attribute des Objektsystems

Das Objektsystem der SMC-B enthält gemäß [gemSpec_COS#9.1] folgende Attribute:

**Card-G2-A_2139 - K_Initialisierung: Wert des Attributes root**

Der Wert des AttributesrootMUSS die Anwendung gemäß Tab_SMC-B_ObjSys_002 sein.
**[\<=]**

**Card-G2-A_2140-01 - K_Initialisierung und K_Personalisierung: Wert des
Attributes answerToReset**

Die Werte der Attribute coldAnswerToReset und warmAnswerToReset MÜSSEN den
Vorgaben der Anforderungen Card-G2-A_3340, Card-G2-A_3341-01, Card-G2-A_3650,
Card-G2-A_3342 und Card-G2-A_3343 entsprechen. **[\<=]**

**Card-G2-A_2141 - K_Personalisierung: Wert des Attributes iccsn8**

Der Wert des Attributesiccsn8MUSS identisch zu den letzten acht Oktetten
imbodyvon EF.GDO sein. **[\<=]**

**Card-G2-A_2142-01 - K_Initialisierung: Inhalt persistentPublicKeyList**

Das AttributpersistentPublicKeyListMUSS den Schlüssel PuK.RCA.CS.E256
enthalten. **[\<=]**

**Card-G2-A_3187 - K_Initialisierung: Größe persistentPublicKeyList**

Für das AttributpersistentPublicKeyList  MUSS so viel Speicherplatz
bereitgestellt werden, dass mindestens fünf weitere öffentliche
Signaturprüfschlüssel einer Root-CA mittels Linkzertifikaten persistent
importierbar sind **[\<=]**

**Card-G2-A_3267-01 - K_Initialisierung: Wert von pointInTime**

Der Hersteller des Objektsystems MUSS das AttributpointInTimeim Rahmen der
Initialisierung auf den Wert von CED (Certificate Effective Date) aus dem
selbst signierten CV-Zertifikat zu PuK.RCA.CS setzen. **[\<=]**

**Card-G2-A_3472 - K_Personalisierung: personalisierter Wert von pointInTime**

Das AttributpointInTimeMUSS im Rahmen der Personalisierung auf den Wert von CED
eines Endnutzerzertifikates gesetzt werden. Falls es mehrere
Endnutzerzertifikate gibt, so ist das CED mit dem größten Wert zu verwenden.
**[\<=]**

### 5.1.1 ATR-Kodierung und technische Eigenschaften

**Card-G2-A_3340 - K_Initialisierung und K_Personalisierung: ATR-Kodierung**

Die ATR-Kodierung MUSS die in Tab_SMC-B_ObjSys_117 dargestellten Werte besitzen.

Tabelle2: Tab_SMC-B_ObjSys_117 ATR-Kodierung (Sequenz von oben nach unten)

<table><tr><th>
Zeichen

</th><th>
Wert

</th><th>
Bedeutung

</th></tr><tr><td>
TS

</td><td>
‘3B’

</td><td>
Initial Character (direct convention)

</td></tr><tr><td>
T0

</td><td>
‘9x’

</td><td>
Format Character (TA1/TD1 indication, x = no. of HB)

</td></tr><tr><td>
TA1

</td><td>
‘xx’

</td><td>
Interface Character (FI/DI, erlaubte Werte: siehe [gemSpec_COS#N024.100])

</td></tr><tr><td>
TD1

</td><td>
‘81’

</td><td>
Interface Character, (T=1, TD2 indication)

</td></tr><tr><td>
TD2

</td><td>
‘B1’

</td><td>
Interface Character, (T=1, TA3/TB3/TD3 indication)

</td></tr><tr><td>
TA3

</td><td>
‘FE’

</td><td>
Interface Character (IFSC coding)

</td></tr><tr><td>
TB3

</td><td>
‘45’

</td><td>
Interface Character, (BWI/CWI coding)

</td></tr><tr><td>
TD3

</td><td>
‘1F’

</td><td>
Interface Character, (T=15, TA4 indication)

</td></tr><tr><td>
TA4

</td><td>
‘xx’

</td><td>
Interface Character (XI/UI coding)

</td></tr><tr><td>
Ti

</td><td>
HB

</td><td>
Historical Bytes (HB, imax. = 15)

</td></tr><tr><td>
TCK

</td><td>
XOR

</td><td>
Check Character (exclusive OR)

</td></tr></table>

**[\<=]**

**Card-G2-A_3341-01 - K_Initialisierung und K_Personalisierung: TC1 Byte im ATR**

Der ATR SOLL ein TC1 Byte mit dem Wert ‘FF’ enthalten. **[\<=]**

**Card-G2-A_3650 - K_Personalisierung und K_Initialisierung: TC1 Byte im ATR**

Wenn der ATR ein TC1 Byte mit dem Wert ‘FF’ enthält, MUSS T0 auf den Wert
‘Dx’ gesetzt werden. **[\<=]**

**Card-G2-A_3342 - K_Initialisierung und K_Personalisierung: Historical Bytes im
ATR**

Der ATR SOLL keine Historical Bytes enthalten. **[\<=]**

**Card-G2-A_3343 - K_Initialisierung und K_Personalisierung: Vorgaben für
Historical Bytes**

Falls der ATR Historical Bytes enthält, dann MÜSSEN

 ---> UL

**[\<=]**

### 5.2 Allgemeine Struktur

Abb_SMC-B_ObjSys_001 zeigt die allgemeine Struktur der Objekte einer SMC-B.

![Abbildung-1][Abbildung-1]

### 5.3 Root, die Wurzelapplikation MF

Das MF der SMC-B ist ein “Application Dedicated File” (siehe
[gemSpec_COS#8.3.1.3]) mit den in Tab_SMC-B_ObjSys_002 gezeigten Eigenschaften.

**Card-G2-A_2146 - K_Initialisierung: Initialisierte: Attribute von MF**

MF MUSS die in Tab_SMC-B_ObjSys_002 dargestellten Werte besitzen.

Tabelle3: Tab_SMC-B_ObjSys_002 Initialisierte Attribute von MF

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
Ordner

</td><td>
</td></tr><tr><td>
applicationIdentifier

</td><td>
‘D27600014606’

</td><td>
</td></tr><tr><td>
fileIdentifier

</td><td>
‘3F 00’

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td>
shareable

</td><td>
True

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
FINGERPRINT

</td><td>
Wildcard

</td><td>
</td></tr><tr><td>
GET RANDOM

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
LOAD APPLICATION

</td><td>
AUT_CMS

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr></table>

**[\<=]**

**A_19305-01 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von MF**

MF MUSS die in der folgenden Tabelle dargestellten Zugriffsregeln für die
kontaktlose Schnittstelle besitzen.

Tabelle4: Zugriffsregeln für die kontaktlose Schnittstelle von MF

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
GET RANDOM

</td><td>
AUT_PACE

</td><td>
</td></tr><tr><td>
LOAD APPLICATION

</td><td>
AUT_CMS

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr></table>

**[\<=]**

### 5.3.1 MF / EF.ATR

Die transparente Datei EF.ATR enthält Informationen zur maximalen Größe der
APDU sowie zur Identifizierung des Betriebssystems.

**Card-G2-A_2147-02 - K_Initialisierung: Initialisierte Attribute von MF /
EF.ATR**

EF.ATR MUSS die in Tab_SMC-B_ObjSys_003 dargestellten Werte besitzen.

Tabelle5: Tab_SMC-B_ObjSys_003 Initialisierte Attribute von MF / EF.ATR

<table><tr><th>
Attribute

</th><th>
Wert

</th><th colspan="2">
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
transparentes Elementary File

</td><td colspan="2">
</td></tr><tr><td>
fileIdentifier

</td><td>
‘2F 01’

</td><td colspan="2">
gemäß [ISO 7816-4]

</td></tr><tr><td>
shortFileIdentifier

</td><td>
‘1D’= 29

</td><td colspan="2">
</td></tr><tr><td>
numberOfOctet

</td><td>
Wildcard

</td><td colspan="2">
</td></tr><tr><td>
positionLogicalEndOfFile

</td><td>
Wildcard

</td><td colspan="2">
siehe Card-G2-A_2668

</td></tr><tr><td>
flagTransactionMode

</td><td>
True

</td><td colspan="2">
</td></tr><tr><td>
flagChecksum

</td><td>
True

</td><td colspan="2">
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td colspan="2">
</td></tr><tr><td>
shareable

</td><td>
True

</td><td colspan="2">
</td></tr><tr><td>
body

</td><td>
Inhalt gemäß [gemSpec_Karten_Fach_TIP_G2.1]

</td><td colspan="2">
</td></tr><tr><td colspan="4">
Kontaktbehaftete Zugriffsregel für logischen LCS „Operational state
(activated)”

</td></tr><tr><td>
Zugriffsart

</td><td colspan="2">
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
READ  BINARY  
WRITE BINARY

</td><td colspan="2">
ALWAYS

</td><td>
</td></tr></table>

**[\<=]**

**A_19307 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von EF.ATR**

EF.ATR MUSS die in der folgenden Tabelle dargestellten Zugriffsregeln für die
kontaktlose Schnittstelle besitzen.

Tabelle6: Zugriffsregeln für die kontaktlose Schnittstelle von EF.ATR

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
READ BINARY

</td><td>
ALWAYS

</td></tr><tr><td>
andere

</td><td>
NEVER

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr></table>

**[\<=]**

**Card-G2-A_3344 - K_Initialisierung: Initialisiertes Attribut numberOfOctet von
MF / EF.ATR**

Das AttributnumberOfOctetMUSS so gewählt werden, dass nach Abschluss der
Initialisierungsphase entweder

 ---> UL

**[\<=]**

### 5.3.2 MF / EF.DIR

Die Datei EF.DIR enthält eine Liste mit Anwendungs-Templates gemäß [ISO/IEC
7816-4]. Diese Liste wird dann angepasst, wenn sich die Applikationsstruktur
durch Löschen oder Anlegen von Anwendungen verändert.

**Card-G2-A_3651 - K_Initialisierung: Inhalt der Records von EF.DIR**

Für jede im Objektsystem vorhandene Anwendung MUSS die Datei einen eigenen
Record besitzen, der den ApplicationIdentifier (AID) dieser Anwendung im
Format      ´61-L\<sub\>61\</sub\>-{4F-L\<sub\>4F\</sub\>-AID}´
enthält.Zu jedem Record der Datei MUSS es auf der Karte eine Anwendung geben,
deren AID durch diesen Record beschrieben ist.Record 1 des EF.DIR MUSS den AID
des MF enthalten. **[\<=]**

**Card-G2-A_2154-01 - K_Initialisierung: Initialisierte Attribute von MF /
EF.DIR**

EF.DIR MUSS die in Tab_SMC-B_ObjSys_005 dargestellten Werte besitzen.

Tabelle7: Tab_SMC-B_ObjSys_005 Initialisierte Attribute von MF / EF.DIR

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
linear variables Elementary File

</td><td>
</td></tr><tr><td>
fileIdentifier

</td><td>
‘2F 00’

</td><td>
gemäß [ISO 7816-4]

</td></tr><tr><td>
shortFileIdentifier

</td><td>
‘1E’= 30

</td><td>
gemäß [ISO 7816-4]

</td></tr><tr><td>
numberOfOctet

</td><td>
‘00 5A’ Oktett = 90 Oktett

</td><td>
</td></tr><tr><td>
maxNumRecords

</td><td>
7 Records

</td><td>
</td></tr><tr><td>
maxRecordLength

</td><td>
19 Oktett

</td><td>
</td></tr><tr><td>
flagRecordLCS

</td><td>
False

</td><td>
</td></tr><tr><td>
flagTransactionMode

</td><td>
True

</td><td>
</td></tr><tr><td>
flagChecksum

</td><td>
True

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td>
shareable

</td><td>
True

</td><td>
</td></tr><tr><td>
recordList  
    Record 1  
    Record 2 und folgende

</td><td>
‘61- 08- (‘4F 06 D27600014606)’  
´61-L61-{4F-L4F-AID}´  
für alle
Applikationen im Objektsystem

</td><td>
AID des MF

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
APPEND RECORD

</td><td>
AUT_CMS

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
DELETE RECORD

</td><td>
AUT_CMS

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
READ RECORD

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
SEARCH RECORD

</td><td>
ALWAYS

</td></tr><tr><td>
UPDATE RECORD

</td><td>
AUT_CMS

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr></table>

**[\<=]**

**A_19304 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von EF.DIR**

EF.DIR MUSS die in der folgenden Tabelle dargestellten Zugriffsregeln für die
kontaktlose Schnittstelle besitzen.

Tabelle8: Zugriffsregeln für die kontaktlose Schnittstelle von EF.DIR

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
APPEND RECORD

</td><td>
AUT_CMS

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
DELETE RECORD

</td><td>
AUT_CMS

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
READ RECORD

</td><td>
AUT_PACE OR AUT_CMS

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
SEARCH RECORD

</td><td>
AUT_PACE OR AUT_CMS

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
UPDATE RECORD

</td><td>
AUT_CMS

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr></table>

**[\<=]**

### 5.3.3 MF / EF.CardAccess (SMC-B CL)

Der Inhalt von EF.CardAccess wird für das PACE-Protokoll zur Absicherung der
Kommunikation über die kontaktlose Schnittstelle verwendet.

**A_19352-01 - (SMC-B CL) K_Initialisierung: Initialisierte Attribute von MF /
EF.CardAccess**

EF.CardAccess MUSS die in der folgenden Tabelle dargestellten Attribute besitzen.

Tabelle9: Initialisierte  Attribute von MF / EF.CardAccess

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
transparentes Elementary File

</td><td>
</td></tr><tr><td>
fileIdentifier

</td><td>
’01 1C’

</td><td>
</td></tr><tr><td>
shortFileIdentifier

</td><td>
‘1C’= 28

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td>
flagTransactionMode

</td><td>
False

</td><td>
</td></tr><tr><td>
flagChecksum

</td><td>
True

</td><td>
</td></tr><tr><td>
numberOfOctet

</td><td>
Wildcard

</td><td>
</td></tr><tr><td>
positionLogicalEndOfFile

</td><td>
Wildcard

</td><td>
siehe Card-G2-A_2668

</td></tr><tr><td>
shareable

</td><td>
True

</td><td>
</td></tr><tr><td>
body

</td><td>
passend zu den Attributen von SK.CAN gemäß [TR-03110-3]

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregeln für die Kontaktschnittstelle

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
READ BINARY

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregeln für die kontaktlose Schnittstelle

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
READ BINARY

</td><td>
ALWAYS

</td><td>
</td></tr></table>

**[\<=]**

### 5.3.4 MF / EF.GDO

In EF.GDO wird das Datenobjekt ICCSN gespeichert, das die Kennnummer der Karte
enthält. Die Kennnummer basiert auf [Beschluss190].

**Card-G2-A_2156-01 - K_Initialisierung: Initialisierte Attribute von MF /
EF.GDO**

EF.GDO MUSS die in Tab_SMC-B_ObjSys_006 dargestellten Werte besitzen.

Tabelle10: Tab_SMC-B_ObjSys_006 Initialisierte Attribute von MF / EF.GDO

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
transparentes Elementary File

</td><td>
</td></tr><tr><td>
fileIdentifier

</td><td>
‘2F 02’

</td><td>
</td></tr><tr><td>
shortFileIdentifier

</td><td>
‘02’= 2

</td><td>
</td></tr><tr><td>
numberOfOctet

</td><td>
‘00 0C’ Oktett = 12 Oktett

</td><td>
</td></tr><tr><td>
positionLogicalEndOfFile

</td><td>
Wildcard

</td><td>
siehe Card-G2-A_2668

</td></tr><tr><td>
flagTransactionMode

</td><td>
False

</td><td>
</td></tr><tr><td>
flagChecksum

</td><td>
True

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td>
shareable

</td><td>
True

</td><td>
</td></tr><tr><td>
body

</td><td>
Wildcard

</td><td>
wird personalisiert

</td></tr><tr><td colspan="3">
Kontaktbehaftete Zugriffsregel für logischen LCS „Operational state
(activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
READ BINARY

</td><td>
ALWAYS

</td><td>
</td></tr></table>

**[\<=]**

**A_19308 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von MF / EF.GDO**

EF.GDO MUSS die in der folgenden Tabelle dargestellten Zugriffsregeln für die
kontaktlose Schnittstelle besitzen.

Tabelle11: Zugriffsregeln für die kontaktlose Schnittstelle von EF.GDO

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
READ BINARY

</td><td>
AUT_PACE

</td><td>
siehe Kapitel 1.5.1

</td></tr><tr><td>
andere

</td><td>
NEVER

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr></table>

**[\<=]**

**Card-G2-A_2157-01 - K_Personalisierung: Personalisiertes Attribut von EF.GDO**

Bei der Personalisierung von EF.GDO MÜSSEN die in Tab_SMC-B_ObjSys_107
angegebenen Attribute mit den dort angegebenen Inhalten personalisiert werden.

Tabelle12: Tab_SMC-B_ObjSys_107 Personalisierte Attribute von MF / EF.GDO

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
positionLogicalEndOfFile

</td><td>
‘00 0C’ Oktett = 12 Oktett

</td><td>
</td></tr><tr><td>
body

</td><td>
Inhalt gemäß [gemSpec_Karten_Fach_TIP_G2.1]

</td><td>
</td></tr></table>

**[\<=]**

### 5.3.5 MF / EF.Version2

Die Datei EF.Version2 enthält die Versionsnummern sowie Produktidentifikatoren
grundsätzlich veränderlicher Elemente der Karte:

 ---> UL

Die konkrete Befüllung ist in [gemSpec_Karten_Fach_TIP_G2.1] beschrieben.

Elemente, die nach Initialisierung durch Personalisierung oder reine
Kartennutzung nicht veränderlich sind, werden in EF.ATR versioniert.

**Card-G2-A_2158-02 - K_Initialisierung: Initialisierte Attribute von MF /
EF.Version2**

EF.Version2 MUSS die in Tab_SMC-B_ObjSys_007 dargestellten Werte besitzen.

Tabelle13: Tab_SMC-B_ObjSys_007 Initialisierte Attribute von MF / EF.Version2

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
transparentes Elementary File

</td><td>
</td></tr><tr><td>
fileIdentifier

</td><td>
‘2F 11’

</td><td>
</td></tr><tr><td>
shortFileIdentifier

</td><td>
‘11’= 17

</td><td>
</td></tr><tr><td>
numberOfOctet

</td><td>
‘00 3C’ Oktett = 60 Oktett

</td><td>
</td></tr><tr><td>
positionLogicalEndOfFile

</td><td>
Wildcard

</td><td>
siehe Card-G2-A_2668

</td></tr><tr><td>
flagTransactionMode

</td><td>
True

</td><td>
</td></tr><tr><td>
flagChecksum

</td><td>
True

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td>
shareable

</td><td>
True

</td><td>
</td></tr><tr><td>
body

</td><td>
Inhalt gemäß [gemSpec_Karten_Fach_TIP_G2.1]

</td><td>
</td></tr><tr><td colspan="3">
Kontaktbehaftete Zugriffsregel für logischen LCS „Operational state
(activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
READ     BINARY

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
SET LOGICAL EOF  
UPDATE BINARY

</td><td>
AUT_CMS

</td><td>
siehe Kapitel 5.5

</td></tr></table>

**[\<=]**

**A_19309 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von MF / EF.Version2**

EF.Version2 MUSS die in der folgenden Tabelle dargestellten Zugriffsregeln für
die kontaktlose Schnittstelle besitzen.

Tabelle14: Zugriffsregeln für die kontaktlose Schnittstelle von MF / EF.Version2

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
READ BINARY

</td><td>
ALWAYS

</td></tr><tr><td>
SET LOGICAL EOF

</td><td>
AUT_CMS

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
UPDATE BINARY

</td><td>
AUT_CMS

</td><td>
iehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr></table>

**[\<=]**

### 5.3.6 MF / EF.C.CA_SMC.CS.E256

Diese Datei enthält ein CV-Zertifikat für die Kryptographie mit elliptischen
Kurven gemäß [gemSpec_COS], welches den öffentlichen Schlüssel
PuK.CA_SMC.CS.E256 einer CA enthält.

**Card-G2-A_2160-02 - K_Initialisierung: Initialisierte Attribute MF /
EF.C.CA_SMC.CS.E256**

EF.C.CA_SMC.CS.E256 MUSS die in Tab_SMC-B_ObjSys_009 dargestellten Werte
besitzen.

Tabelle15: Tab_SMC-B_ObjSys_009 Initialisierte Attribute MF / EF.C.CA_SMC.CS.E256

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
transparentes Elementary File

</td><td>
</td></tr><tr><td>
fileIdentifier

</td><td>
‘2F 07’

</td><td>
</td></tr><tr><td>
shortFileIdentifier

</td><td>
‘07’= 7

</td><td>
</td></tr><tr><td>
numberOfOctet

</td><td>
‘00 DC’ Oktett = 220 Oktett

</td><td>
</td></tr><tr><td>
positionLogicalEndOfFile

</td><td>
Wildcard

</td><td>
siehe Card-G2-A_2668

</td></tr><tr><td>
flagTransactionMode

</td><td>
True

</td><td>
</td></tr><tr><td>
flagChecksum

</td><td>
False

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td>
shareable

</td><td>
True

</td><td>
</td></tr><tr><td>
body

</td><td>
kein Inhalt

</td><td>
wird personalisiert

</td></tr><tr><td colspan="3">
Kontaktbehaftete Zugriffsregel für logischen LCS „Operational state
(activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
DELETE  
UPDATE BINARY

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5 und 1.5.1

</td></tr><tr><td>
READ     BINARY

</td><td>
ALWAYS

</td><td>
</td></tr></table>

**[\<=]**

**A_19310 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von MF / EF.C.CA_SMC.CS.E256**

EF.C.CA_SMC.CS.E256 MUSS die in der folgenden Tabelle dargestellten
Zugriffsregeln für die kontaktlose Schnittstelle besitzen.

Tabelle16: Zugriffsregeln für die kontaktlose Schnittstelle von MF /
EF.C.CA_SMC.CS.E256

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
READ BINARY

</td><td>
AUT_PACE OR AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5 und 1.5.1

</td></tr><tr><td>
UPDATE BINARY

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr></table>

**[\<=]**

**Card-G2-A_3347-01 - K_Personalisierung: Personalisierte Attribute von MF /
EF.C.CA_SMC.CS.E256**

Bei der Personalisierung von MF / EF.C.CA_SMC.CS.E256 MÜSSEN die in
Tab_SMC-B_ObjSys_069 angegebenen Attribute mit den dort angegebenen Inhalten
personalisiert werden.

Tabelle17: Tab_SMC-B_ObjSys_069 Personalisierte Attribute von MF /
EF.C.CA_SMC.CS.E256

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
positionLogicalEndOfFile

</td><td>
‘00DC’ Oktett = 220 Oktett

</td><td>
</td></tr><tr><td>
body

</td><td>
C.CA_SMC.CS.E256 gemäß [gemSpec_PKI#6.7.1]

</td><td>
</td></tr><tr><td>
body (Option_Erstellung _von_Testkarten)

</td><td>
C.CA_SMC.CS.E256 gemäß [gemSpec_PKI#6.7.1] aus Test-CVC-CA

</td><td>
</td></tr></table>

**[\<=]**

### 5.3.7 MF / EF.C.SMC.AUTR_CVC.E256

EF.C.SMC.AUTR_CVC.E256 enthält das CV-Zertifikat der SMC-B für die
Kryptographie mit elliptischen Kurven für rollenbasierte C2C-Authentisierung
zwischen SMC-B und eGK. Das zugehörende private Schlüsselobjekt
PrK.SMC.AUTR_CVC.E256 ist im Kapitel 5.3.12 definiert. Für die Ausprägung
_ORG bleibt diese Datei leer oder wird mit Nullen befüllt.

**Card-G2-A_2163-01 - K_Initialisierung: Initialisierte Attribute von MF /
EF.C.SMC.AUTR_CVC.E256**

EF.C.SMC.AUTR_CVC.E256 MUSS die in Tab_SMC-B_ObjSys_012 dargestellten Werte
besitzen.

Tabelle18: (Tab_SMC-B_ObjSys_012) Initialisierte Attribute von MF /
EF.C.SMC.AUTR_CVC.E256

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
transparentes Elementary File

</td><td>
</td></tr><tr><td>
fileIdentifier

</td><td>
‘2F 06’

</td><td>
</td></tr><tr><td>
shortFileIdentifier

</td><td>
‘06’= 6

</td><td>
</td></tr><tr><td>
numberOfOctet

</td><td>
‘00DE’ Oktett = 222 Oktett

</td><td>
</td></tr><tr><td>
positionLogicalEndOfFile

</td><td>
Wildcard

</td><td>
siehe Card-G2-A_2668

</td></tr><tr><td>
flagTransactionMode

</td><td>
True

</td><td>
</td></tr><tr><td>
flagChecksum

</td><td>
False

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td>
shareable

</td><td>
True

</td><td>
</td></tr><tr><td>
body

</td><td>
kein Inhalt

</td><td>
wird personalisiert

</td></tr><tr><td colspan="3">
Kontaktbehaftete Zugriffsregel für logischen LCS „Operational state
(activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
DELETE  
UPDATE BINARY

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5 und 1.5.1

</td></tr><tr><td>
READ     BINARY

</td><td>
ALWAYS

</td><td>
</td></tr></table>

**[\<=]**

**A_19311 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von MF / EF.C.SMC.AUTR_CVC.E256**

EF.C.SMC.AUTR_CVC.E256 MUSS die in der folgenden Tabelle dargestellten
Zugriffsregeln für die kontaktlose Schnittstelle besitzen.

Tabelle19: Zugriffsregeln für die kontaktlose Schnittstelle von
EF.C.SMC.AUTR_CVC.E256

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5 und 1.5.1

</td></tr><tr><td>
READ BINARY

</td><td>
AUT_PACE OR AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5 und 1.5.1

</td></tr><tr><td>
UPDATE BINARY

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5 und 1.5.1

</td></tr><tr><td>
andere

</td><td>
NEVER

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr></table>

**[\<=]**

**Card-G2-A_3389 - K_Personalisierung: Festlegung von CHR in MF /
EF.C.SMC.AUTR_CVC.E256**

Für die CHR in diesem Zertifikat MUSS CHR = ’00 06’ || ICCSN gelten, wobei
die ICCSN denselben Wert besitzen MUSS, wie das Wertfeldbodyaus
[Card-G2-A_2157]. **[\<=]**

**Card-G2-A_3349 - K_Personalisierung: Personalisierte Attribute von MF /
EF.C.SMC.AUTR_CVC.E256**

Bei der Personalisierung von EF.C.SMC.AUTR_CVC.E256 MÜSSEN die in
Tab_SMC-B_ObjSys_072 angegebenen Attribute mit den dort angegebenen Inhalten
personalisiert werden.

Tabelle20: Tab_SMC-B_ObjSys_072 Personalisierte Attribute von MF /
EF.C.SMC.AUTR_CVC.E256

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
positionLogicalEndOfFile

</td><td>
‘00DE’ Oktett = 222 Oktett

</td><td>
</td></tr><tr><td>
positionLogicalEndOfFile (Ausprägung_ORG)

</td><td>
Wildcard

</td><td>
Entsprechend dem Verfahren des Personalisierers und passend zu body

</td></tr><tr><td>
body

</td><td>
C.SMC.AUTR_CVC.E256 gemäß [gemSpec_PKI] passend zu dem privaten Schlüssel in
PrK.SMC.AUTR_CVC.E256

</td><td>
</td></tr><tr><td>
body  
(Ausprägung_ORG)

</td><td>
Leer  
oder ’00 … 00‘

</td><td>
Entsprechend dem Verfahren des Personalisierers und passend zu
positionLogicalEndOfFile

</td></tr></table>

**[\<=]**

### 5.3.8 MF / EF.C.SMC.AUTD_RPE_CVC.E256

EF.C.SMC.AUTD_RPE_CVC.E256 enthält das CV-Zertifikat für die Kryptographie mit
elliptischen Kurven für die C2C-Geräteauthentisierung zwischen einer lokal
vorhandenen SMC-B und einer SMC-B als entferntem PIN-Empfänger. Das
zugehörende private Schlüsselobjekt PrK.SMC.AUTD_RPE_CVC.E256 ist im
Kapitel 5.3.13 definiert.

**Card-G2-A_2169-01 - K_Initialisierung: Initialisierte Attribute von MF /
EF.C.SMC.AUTD_RPE_CVC.E256**

EF.C.SMC.AUTD_RPE_CVC.E256 MUSS die in Tab_SMC-B_ObjSys_018 dargestellten Werte
besitzen.

Tabelle21: (Tab_SMC-B_ObjSys_018) Initialisierte Attribute von MF /
EF.C.SMC.AUTD_RPE_CVC.E256

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
transparentes Elementary File

</td><td>
</td></tr><tr><td>
fileIdentifier

</td><td>
‘2F 09’

</td><td>
</td></tr><tr><td>
shortFileIdentifier

</td><td>
‘09’= 9

</td><td>
</td></tr><tr><td>
numberOfOctet

</td><td>
‘00DE’ Oktett = 222 Oktett

</td><td>
</td></tr><tr><td>
positionLogicalEndOfFile

</td><td>
Wildcard

</td><td>
siehe Card-G2-A_2668

</td></tr><tr><td>
flagTransactionMode

</td><td>
True

</td><td>
</td></tr><tr><td>
flagChecksum

</td><td>
False

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td>
shareable

</td><td>
True

</td><td>
</td></tr><tr><td>
body

</td><td>
kein Inhalt

</td><td>
wird personalisiert

</td></tr><tr><td colspan="3">
Kontaktbehaftete Zugriffsregeln für LCS "Operational state (activated)"

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
DELETE  
UPDATE BINARY

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5 und 1.5.1

</td></tr><tr><td>
READ     BINARY

</td><td>
ALWAYS

</td><td>
</td></tr></table>

**[\<=]**

**A_19312 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von MF / EF.C.SMC.AUTD_RPE_CVC.E256**

EF.C.SMC.AUTD_RPE_CVC.E256 MUSS die in der folgenden Tabelle dargestellten
Zugriffsregeln für die kontaktlose Schnittstelle besitzen

Tabelle22: Zugriffsregeln für die kontaktlose Schnittstelle von MF /
EF.C.SMC.AUTD_RPE_CVC.E256

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
siehe Kapitel 5.5 und 1.5.1

</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5 und 1.5.1

</td></tr><tr><td>
READ BINARY

</td><td>
AUT_PACE OR AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5 und 1.5.1

</td></tr><tr><td>
UPDATE BINARY

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
</td></tr><tr><td>
andere

</td><td>
NEVER

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr></table>

**[\<=]**

Hinweis 16: Kommandos, die gemäß [gemSpec_COS] mit einem transparenten EF
arbeiten, sind: ACTIVATE, DEACTIVATE, DELETE, ERASE BINARY, READ BINARY,
SELECT, SET LOGICAL EOF, UPDATE BINARY, TERMINATE, WRITE BINARY

Hinweis 17: Das Kommando ist nur vom Inhaber des CMS- / CUP-Schlüssels
ausführbar, siehe Kap. 5.5.

**Card-G2-A_3390 - K_Personalisierung: Festlegung von CHR in MF /
EF.C.SMC.AUTD_RPE_CVC.E256**

Für die CHR in diesem Zertifikat MUSS CHR = ’00 09’ || ICCSN gelten, wobei
die ICCSN denselben Wert besitzen MUSS, wie das Wertfeldbodyaus
[Card-G2-A_2157]. **[\<=]**

**Card-G2-A_3350 - K_Personalisierung: Personalisierte Attribute von MF /
EF.C.SMC.AUTD_RPE_CVC.E256**

Bei der Personalisierung von EF.C.SMC.AUTD_RPE_CVC.E256 MÜSSEN die in
Tab_SMC-B_ObjSys_074 angegebenen Attribute mit den dort angegebenen Inhalten
personalisiert werden.

Tabelle23: Tab_SMC-B_ObjSys_074 Personalisierte Attribute von MF /
EF.C.SMC.AUTD_RPE_CVC.E256

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
positionLogicalEndOfFile

</td><td>
‘00DE’ Oktett = 222 Oktett

</td><td>
</td></tr><tr><td>
body

</td><td>
C.SMC.AUTD_RPE_CVC.E256 gemäß [gemSpec_PKI] passend zu dem privaten Schlüssel
in PrK.SMC.AUTD_RPE_CVC.E256

</td><td>
</td></tr></table>

**[\<=]**

### 5.3.9 MF / PIN.SMC

Dieses Passwortobjekt wird zur Freischaltung von Schlüsseln und Inhalten der
SMC-B verwendet.

**Card-G2-A_2171 - K_Initialisierung: Initialisierte Attribute von MF / PIN.SMC**

PIN.SMC MUSS die in Tab_SMC-B_ObjSys_020 dargestellten Werte besitzen.

Tabelle24: Tab_SMC-B_ObjSys_020 Initialisierte Attribute von MF / PIN.SMC

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
Reguläres Passwortobjekt

</td><td>
</td></tr><tr><td>
pwdIdentifier

</td><td>
‘01’ = 1

</td><td>
</td></tr><tr><td>
secret

</td><td>
undefiniert

</td><td>
wird personalisiert

</td></tr><tr><td>
minimumLength

</td><td>
6

</td><td>
</td></tr><tr><td>
MaximumLength

</td><td>
8

</td><td>
</td></tr><tr><td>
startRetryCounter

</td><td>
3

</td><td>
</td></tr><tr><td>
retryCounter

</td><td>
3

</td><td>
</td></tr><tr><td>
transportStatus

</td><td>
Transport-PIN

</td><td>
</td></tr><tr><td>
flagEnabled

</td><td>
True

</td><td>
</td></tr><tr><td>
startSsec

</td><td>
unendlich

</td><td>
</td></tr><tr><td>
PUK

</td><td>
undefiniert

</td><td>
wird personalisiert

</td></tr><tr><td>
pukUsage

</td><td>
10

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
CHANGE RD, P1=0

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
GET PIN STATUS

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
RESET RC. P1 AUS DER MENGE {0, 1}

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
VERIFY

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
andere

</td><td>
NEVER

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr></table>

**[\<=]**

**A_19313 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von MF / PIN.SMC**

PIN.SMC MUSS die in der folgenden Tabelle dargestellten Zugriffsregeln für die
kontaktlose Schnittstelle besitzen.

Tabelle25: Zugriffsregeln für die kontaktlose Schnittstelle von MF / PIN.SMC

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
CHANGE RD, P1=0

</td><td>
AUT_PACE

</td><td>
siehe Kapitel 1.5.1

</td></tr><tr><td>
GET PIN STATUS

</td><td>
AUT_PACE

</td><td>
siehe Kapitel 1.5.1

</td></tr><tr><td>
RESET RC, P1 AUS DER MENGE (0,1)

</td><td>
AUT_PACE

</td><td>
siehe Kapitel 1.5.1

</td></tr><tr><td>
VERIFY

</td><td>
AUT_PACE

</td><td>
siehe Kapitel 1.5.1

</td></tr><tr><td>
andere

</td><td>
NEVER

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr></table>

**[\<=]**

**Card-G2-A_3351 - K_Personalisierung: Personalisierte Attribute von MF /
PIN.SMC**

Bei der Personalisierung von PIN.SMC MÜSSEN die in Tab_SMC-B_ObjSys_076
angegebenen Attribute mit den dort angegebenen Inhalten personalisiert werden.

Tabelle26: Tab_SMC-B_ObjSys_076 Personalisierte Attribute von MF / PIN.SMC

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
secret

</td><td>
PIN-Wert gemäß [gemSpec_PINPUK_TI]

</td><td>
Transport-PIN

</td></tr><tr><td>
secretLength

</td><td>
5 Ziffern (minimumLength - 1)

</td><td>
Länge der Transport-PIN

</td></tr><tr><td>
PUK

</td><td>
PUK-Wert gemäß [gemSpec_PINPUK_TI]

</td><td>
</td></tr><tr><td>
PUKLength

</td><td>
8 Ziffern

</td><td>
</td></tr></table>

**[\<=]**

### 5.3.10 MF / PrK.SMC.AUTR_CVC.E256

PrK.SMC.AUTR_CVC.E256 ist der globale private Schlüssel für die Kryptographie
mit elliptischen Kurven für die C2C-Authentisierung zwischen SMC-B/eGK. Der
zugehörige öffentliche Schlüssel PuK.SMC.AUTR_CVC.E256 ist in
C.SMC.AUTR_CVC.E256 (siehe Kapitel 5.3.8) enthalten. Für die Ausprägung _ORG
bleibt dieser Schlüssel herstellerspezifisch „unbefüllt“ oder wird mit
Zufallswerten befüllt.

**Card-G2-A_2180-01 - K_Initialisierung: Initialisierte Attribute von MF /
PrK.SMC.AUTR_CVC.E256**

PrK.SMC.AUTR_CVC.E256 MUSS die in Tab_SMC-B_ObjSys_022 dargestellten Werte
besitzen.

Tabelle27: Tab_SMC-B_ObjSys_022 Initialisierte Attribute von MF /
PrK.SMC.AUTR_CVC.E256

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
privates Schlüsselobjekt, ELC 256

</td><td>
</td></tr><tr><td>
keyIdentifier

</td><td>
‘06’ = 6

</td><td>
</td></tr><tr><td>
privateElcKey

</td><td>
domainparameter = brainpoolP256r1

</td><td>
</td></tr><tr><td>
privateElcKey

</td><td>
keyData = AttributNotSet

</td><td>
wird personalisiert

</td></tr><tr><td>
keyAvailable

</td><td>
WildCard

</td><td>
wird personalisiert

</td></tr><tr><td>
listAlgorithmIdentifier

</td><td>
elcRoleAuthentication

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td>
accessRuleSessionkeys

</td><td>
irrelevant

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
GENERATE ASYMMETRIC KEY PAIR  
P1=‘81’

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
INTERNAL AUTHENTICATE

</td><td>
PWD(PIN.SMC)

</td><td>
</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
NEVER

</td><td>
</td></tr></table>

**[\<=]**

**A_19314 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von MF / PrK.SMC.AUTR_CVC.E256**

PrK.SMC.AUTR_CVC.E256 MUSS die in der folgenden Tabelle dargestellten
Zugriffsregeln für die kontaktlose Schnittstelle besitzen.

Tabelle28: Zugriffsregeln für die kontaktlose Schnittstelle von MF /
PrK.SMC.AUTR_CVC.E256

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
GENERATE ASYMMETRIC KEY PAIR, P1 = '81'

</td><td>
AUT_PACE

</td><td>
siehe Kapitel 1.5.1

</td></tr><tr><td>
INTERNAL AUTHENTICATE

</td><td>
AUT_PACE AND PWD(PIN.SMC)

</td><td>
siehe Kapitel 1.5.1

</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5 und 1.5.1

</td></tr><tr><td>
andere

</td><td>
NEVER

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
NEVER

</td><td>
</td></tr></table>

**[\<=]**

**Card-G2-A_3355 - K_Personalisierung: Personalisierte Attribute von MF /
PrK.SMC.AUTR_CVC.E256**

Bei der Personalisierung von PrK.SMC.AUTR_CVC.E256 MÜSSEN die in
Tab_SMC-B_ObjSys_078 angegebenen Attribute mit den dort angegebenen Inhalten
personalisiert werden.

Tabelle29: Tab_SMC-B_ObjSys_078 Personalisierte Attribute von MF /
PrK.SMC.AUTR_CVC.E256

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
keyAvailable

</td><td>
True

</td><td>
</td></tr><tr><td>
keyAvailable (Ausprägung_ORG)

</td><td>
False, ggf. True

</td><td>
Entsprechend dem Verfahren des Personalisierers

</td></tr><tr><td>
privateElcKey

</td><td>
keyData = Wildcard

</td><td>
</td></tr><tr><td>
privateElcKey (Ausprägung_ORG)

</td><td>
Herstellerspezifisch „nicht nutzbar“ (z.B. mit Zufallswerten)

</td><td>
Entsprechend dem Verfahren des Personalisierers

</td></tr></table>

**[\<=]**

### 5.3.11 MF / PrK.SMC.AUTD_RPE_CVC.E256

PrK.SMC.AUTD_RPE_CVC.E256 ist der globale private Schlüssel für die
Kryptographie mit elliptischen Kurven für die C2C-Authentisierung zwischen
einer gSMC-KT und einer SMC-B in der Funktion des PIN-Empfängers. Der
zugehörige öffentliche Schlüssel PuK.SMC.AUTD_RPE_CVC.E256 ist in
C.SMC.AUTD_RPE_CVC.E256 (siehe Kapitel 5.3.9) enthalten.

**Card-G2-A_2189 - K_Initialisierung: Initialisierte Attribute von MF /
PrK.SMC.AUTD_RPE_CVC.E256**

PrK.SMC.AUTD_RPE_CVC.E256 MUSS die in Tab_SMC-B_ObjSys_028 dargestellten Werte
besitzen.

Tabelle30: Tab_SMC-B_ObjSys_028 Initialisierte Attribute von MF /
PrK.SMC.AUTD_RPE_CVC.E256

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
privates Authentisierungsobjekt ELC 256

</td><td>
</td></tr><tr><td>
keyIdentifier

</td><td>
‘09’ = 9

</td><td>
</td></tr><tr><td>
privateKey

</td><td>
herstellerspezifisch „unbefüllt“, Speicherplatz hinreichend für einen
Schlüssel mit Domainparameter = brainpoolP256r1

</td><td>
wird personalisiert

</td></tr><tr><td>
keyAvailable

</td><td>
WildCard

</td><td>
wird personalisiert

</td></tr><tr><td>
listAlgorithmIdentifier

</td><td>
Ein Wert aus der Menge {elcSessionkey4SM, elcAsynchronAdmin}

</td><td>
</td></tr><tr><td>
numberScenarion

</td><td>
0

</td><td>
</td></tr><tr><td>
accessRuleSessionkeys

</td><td>
irrelevant

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
GENERATE ASYMMETRIC KEY PAIR  
P1=‘81’

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
GENERAL AUTHENTICATE

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
NEVER

</td><td>
</td></tr></table>

**[\<=]**

**A_19315-01 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von MF / PrK.SMC.AUTD_RPE_CVC.E256**

PrK.SMC.AUTD_RPE_CVC.E256 MUSS die in der folgenden Tabelle dargestellten
Zugriffsregeln für die kontaktlose Schnittstelle besitzen.

Tabelle31: Zugriffsregeln für die kontaktlose Schnittstelle von MF /
PrK.SMC.AUTD_RPE_CVC.E256

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
GENERATE ASYMMETRIC KEY PAIR, P1 = '81'

</td><td>
AUT_PACE

</td><td>
siehe Kapitel 1.5.1

</td></tr><tr><td>
GENERAL AUTHENTICATE

</td><td>
ALWAYS

</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr></table>

**[\<=]**

**Card-G2-A_3356 - K_Personalisierung: Personalisierte Attribute von MF /
PrK.SMC.AUTD_RPE_CVC.E256**

Bei der Personalisierung von PrK.SMC.AUTD_RPE_CVC.E256 MÜSSEN die in
Tab_SMC-B_ObjSys_080 angegebenen Attribute mit den dort angegebenen Inhalten
personalisiert werden.

Tabelle32: Tab_SMC-B_ObjSys_080 Personalisierte Attribute von MF /
PrK.SMC.AUTD_RPE_CVC.E256

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
privateKey

</td><td>
Domainparameter = brainpoolP256r1

</td><td>
</td></tr><tr><td>
keyAvailable

</td><td>
True

</td><td>
</td></tr></table>

**[\<=]**

### 5.3.12 Sicherheitsanker zum Import von CV-Zertifikaten

Der Sicherheitsanker zum Import von CV-Zertifikaten ist ein öffentliches
Signaturprüfobjekt und enthält den öffentlichen Schlüssel der Root-CA für
CV-Zertifikate der Telematikinfrastruktur.

### 5.3.12.1 MF / PuK.RCA.CS.E256

PuK.RCA.CS.E256 ist der öffentliche Schlüssel der Root-CA des
Gesundheitswesens für die Kryptographie mit elliptischen Kurven für die
Prüfung von CV-Zertifikaten, die von dieser herausgegeben werden.

**Card-G2-A_2192-01 - K_Initialisierung: Initialisierte Attribute von MF /
PuK.RCA.CS.E256**

PuK.RCA.CS.E256 MUSS die in Tab_SMC-B_ObjSys_031 dargestellten Werte besitzen.

Tabelle33: Tab_SMC-B_ObjSys_031 Initialisierte Attribute von MF / PuK.RCA.CS.E256

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
öffentliches Signaturprüfobjekt ELC 256

</td><td>
</td></tr><tr><td colspan="3">
Für Echtkarten MÜSSEN die vier folgenden Attribute mit den unten angegebenen
Werten initialisiert

werden.  
Für Option_Erstellung_von_Testkarten MÜSSEN die vier folgenden
Attribute mit Wildcard oder AttributeNotSet initialisiert werden.

</td></tr><tr><td>
keyIdentifier

</td><td>
ELC 256 Root-CA-Kennung (5 Bytes) || Erweiterung (3 Bytes)

</td><td>
</td></tr><tr><td>
expirationDate

</td><td>
Jahr Monat Tag im Format YYMMDD gemäß [gemSpec_PKI#6.7.2.6], Wert gemäß
[gemSpec_CVC_Root#5.4.2]

</td><td>
</td></tr><tr><td>
CHAT

</td><td>
OIDflags = oid_cvc_fl_ti  
flagList  = ‘FF 0084 2006 00E2’

</td><td>
siehe [gemSpec_PKI]

</td></tr><tr><td>
publicKey

</td><td>
Öffentlicher Schlüssel mit Domainparameter = brainpoolP256r1 gemäß
[gemSpec_PKI#6.7.2.3] und gemäß [gemSpec_CVC_TSP#4.5]

</td><td>
</td></tr><tr><td colspan="3">
Für Echtkarten MÜSSEN die nachfolgenden Attribute mit den unten angegebenen
Werten initialisiert werden.  
Für Option_Erstellung_von_Testkarten MÜSSEN
die nachfolgenden Attribute entweder mit den unten angegebenen

Werten oder mit Wildcard oder AttributeNotSet initialisiert werden.

</td></tr><tr><td>
oid

</td><td>
ecdsa-with-SHA256 ‘2A8648CE3D040302’ = {1.2.840.10045.4.3.2}

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td>
accessRulesPublicSignatureVerificationObject

</td><td>
Für alle relevanten Interfaces und alle relevanten Werte von lifeCycleStatus
gilt:  
DELETE  AUT_CMS OR AUT_CUP  
PSO VERIFY CERTIFICATE  ALWAYS

</td><td>
</td></tr><tr><td>
accessRulesPublicAuthenticationObject

</td><td>
Für alle relevanten Interfaces und alle relevanten Werte von lifeCycleStatus
gilt:  
DELETE  ALWAYS  
EXTERNAL AUTHENTICATE  ALWAYS

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
PSO VERIFY CERTIFICATE

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5 und 1.5.1

</td></tr><tr><td>
andere

</td><td>
NEVER

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
NEVER

</td><td>
</td></tr></table>

**[\<=]**

**A_19316 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von MF / PuK.RCA.CS.E256**

PuK.RCA.CS.E256 MUSS die in der folgenden Tabelle dargestellten Zugriffsregeln
für die kontaktlose Schnittstelle besitzen.

Tabelle34: Zugriffsregeln für die kontaktlose Schnittstelle von MF /
PuK.RCA.CS.E256

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
PSO VERIFY CERTIFICATE

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
NEVER

</td><td>
</td></tr></table>

**[\<=]**

**Card-G2-A_3374-02 - K_Personalisierung: Personalisierte Attribute von MF /
PuK.RCA.CS.E256 für Testkarten**

Bei der Personalisierung von PuK.RCA.CS.E256 für Testkarten MÜSSEN die in
Tab_SMC-B_ObjSys_119 angegebenen Attribute mit den dort angegebenen Inhalten
personalisiert werden.Wenn die restlichen Attribute von PuK.RCA.CS.E256 mit
Wildcard oder AttributeNotSet initialisiert wurden, MÜSSEN sie gemäß den
Vorgaben in der Tabelle Tab_SMC-B_ObjSys_031 personalisiert werden.

Tabelle35: Tab_SMC-B_ObjSys_119 Personalisierte Attribute von MF /
PuK.RCA.CS.E256 für Testkarten

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
publicKey

</td><td>
Öffentlicher Schlüssel mit Domainparameter = brainpoolP256r1 gemäß
[gemSpec_PKI#6.7.2.3] aus Test-CVC-CA

</td><td>
</td></tr><tr><td>
keyIdentifier

</td><td>
E 256 Root-CA-Kennung (5 Bytes) || Erweiterung (3 Bytes); Wert gemäß
keyIdentifier des personalisierten Schlüssels

</td><td>
</td></tr><tr><td>
CHAT

</td><td>
OIDflags        = oid_cvc_fl_ti  
FlagList        = ‘FF 0084
2006 00E2’

</td><td>
</td></tr><tr><td>
expirationDate

</td><td>
Jahr Monat Tag im Format YYMMDD gemäß [gemSpec_PKI#6.7.2.6], Wert gemäß CXD
des personalisierten Schlüssels

</td></tr></table>

**[\<=]**

### 5.3.13 Asymmetrische Kartenadministration

Die hier beschriebene Variante der Administration der SMC-B betrifft ein
Administrationssystem (i.A. ein Kartenmanagementsystem (CMS)) zur
Administration der SMC-B.

Die Administration einer SMC-B erfordert den Aufbau eines kryptographisch
gesicherten Kommunikationskanals (Trusted Channel). In diesem Kapitel werden
Schlüssel beschrieben, die den Aufbau eines solchen Trusted Channels mittels
asymmetrischer Verfahren ermöglichen. Die Schlüssel zum Aufbau mittels
symmetrischer Verfahren werden in 5.3.16 beschrieben.

Voraussetzung für den Aufbau mittels asymmetrischer Verfahren ist, dass sowohl
die zu administrierende Karte, als auch das administrierende System über ein
asymmetrisches Schlüsselpaar verfügen. Sei (PrK.ICC, PuK.ICC) das
Schlüsselpaar der Smartcard und (PrK.Admin, PuK.Admin) das Schlüsselpaar des
administrierenden Systems, dann ist es erforderlich, dass die Smartcard
PuK.Admin kennt und das administrierende System PuK.ICC kennt.

Während die Schlüsselpaare auf Smartcards typischerweise kartenindividuell
sind, so ist es denkbar, dass mit einem Schlüsselpaar eines administrierenden
Systems genau eine, oder mehrere oder alle Smartcards administriert werden. Das
Sicherheitskonzept des administrierenden Systems erscheint die geeignete Stelle
zu sein um eine Variante auszuwählen.

### 5.3.13.1 MF / PuK.RCA.ADMINCMS.CS.E256

Dieses Objekt enthält den öffentlichen Schlüssel der Root-CA, welcher an der
Wurzel der der CVC.E256-Hierarchie für die asymmetrische CMS-Authentisierung
steht. PuK.RCA.ADMINCMS.CS.E256 wird für den Import weiterer Schlüssel für
die elliptische Kryptographie benötigt.

**Card-G2-A_3039-01 - K_Initialisierung: Initialisierte Attribute von MF /
PuK.RCA.ADMINCMS.CS.E256**

PuK.RCA.ADMINCMS.CS.E256 MUSS die in Tab_SMC-B_ObjSys_063 dargestellten
Attribute besitzen.

Tabelle36: Tab_SMC-B_ObjSys_063 Initialisierte Attribute von MF /
PuK.RCA.ADMINCMS.CS.E256

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
öffentliches Signaturprüfobjekt, ELC 256

</td><td>
</td></tr><tr><td colspan="3">
Für Echtkarten MÜSSEN die beiden folgenden Attribute mit den unten angegebenen
Werten

initialisiert werden.  
Für Option_Erstellung_von_Testkarten MÜSSEN die beiden
folgenden Attribute mit Wildcard oder AttributeNotSet initialisiert werden.

</td></tr><tr><td>
CHAT

</td><td>
OIDflags    = oid_cvc_fl_cms

FlagList    = ‘FF AFFF FFFF FFFF’

</td><td>
</td></tr><tr><td>
expirationDate

</td><td>
Identisch zu  „expirationDate“ von PuK.RCS.CS.E256

</td><td>
</td></tr><tr><td colspan="3">
Für Echtkarten MÜSSEN die nachfolgenden Attribute mit den unten angegebenen
Werten initialisiert werden.  
Für Option_Erstellung_von_Testkarten MÜSSEN
die nachfolgenden Attribute entweder mit den unten angegebenen Werten oder mit
Wildcard oder AttributeNotSet initialisiert werden.

</td></tr><tr><td>
keyIdentifier

</td><td>
‘0000 0000 0000 0013‘

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td>
publicKey

</td><td>
herstellerspezifisch „unbefüllt“, Speicherplatz hinreichend für einen
Schlüssel

mit Domainparameter = brainpoolP256r1

</td><td>
wird personalisiert

</td></tr><tr><td>
oid

</td><td>
ecdsa-with-SHA256 ‘2A8648CE3D040302’ = {1.2.840.10045.4.3.2}

</td><td>
</td></tr><tr><td>
accessRulesPublicSignatureVerificationObject.

</td><td>
Für alle relevanten Interfaces und alle relevanten Werte von lifeCycleStatus
gilt:  
DELETE  AUT_CMS OR AUT_CUP  
PSO VERIFY CERTIFICATE



ALWAYS

</td><td>
</td></tr><tr><td>
accessRulesPublicAuthenticationObject.

</td><td>
Für alle relevanten Interfaces und alle relevanten Werte von lifeCycleStatus
gilt:  
DELETE  ALWAYS

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (activated)” 

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td></tr><tr><td>
PSO VERIFY CERTIFICATE

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td></tr><tr><td>
alle

</td><td>
NEVER

</td><td>
</td></tr></table>

**[\<=]**

**A_19317 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von MF / PuK.RCA.ADMINCMS.CS.E256**

PuK.RCA.ADMINCMS.CS.E256 MUSS die in der folgenden Tabelle dargestellten
Zugriffsregeln für die kontaktlose Schnittstelle besitzen.

Tabelle37: Zugriffsregeln für die kontaktlose Schnittstelle von MF /
PuK.RCA.ADMINCMS.CS.E256

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
PSO VERIFY CERTIFICATE

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
NEVER

</td><td>
</td></tr></table>

**[\<=]**

**Card-G2-A_3357-01 - K_Personalisierung: Personalisierte Attribute von MF /
PuK.RCA.ADMINCMS.CS.E256**

Bei der Personalisierung von PuK.RCA.ADMINCMS.CS.E256 MÜSSEN die in
Tab_SMC-B_ObjSys_083 angegebenen Attribute mit den dort angegebenen Inhalten
personalisiert werden.Wenn die restlichen Attribute von
PuK.RCA.ADMINCMS.CS.E256 mit Wildcard oder AttributeNotSet initialisiert
wurden, MÜSSEN sie gemäß den Vorgaben in der Initialisierungstabelle
Tab_SMC-B_ObjSys_063 personalisiert werden.

Tabelle38: Tab_SMC-B_ObjSys_083 Personalisierte Attribute von MF /
PuK.RCA.ADMINCMS.CS.E256

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
publicKey

</td><td>
Domainparameter = brainpoolP256r1 gemäß [gemSpec_PKI#6.7.2.3] aus
Admin-CVC-Root

</td><td>
</td></tr><tr><td>
publicKey  
(Option_Erstellung_von_Testkarten)

</td><td>
Domainparameter = brainpoolP256r1 gemäß [gemSpec_PKI#6.7.2.3] aus
Test-Admin-CVC-Root

</td><td>
</td></tr><tr><td>
CHAT

</td><td>
OIDflags   = oid_cvc_fl_cms  
FlagList    = ‘FF AFFF FFFF FFFF’

</td><td>
</td></tr><tr><td>
expirationDate  
(Option_Erstellung_von_Testkarten)

</td><td>
Identisch zu „expirationDate“ des personalisierten PuK.RCA.CS.E256

</td><td>
</td></tr></table>

**[\<=]**

### 5.3.14 Symmetrische Kartenadministration

Die hier beschriebene Variante der Administration der SMC-B betrifft ein
Administrationssystem (i.A. ein Kartenmanagementsystem (CMS)) zur
Administration der SMC-B.

Die Administration einer SMC-B erfordert den Aufbau eines kryptographisch
gesicherten Kommunikationskanals (Trusted Channel). In diesem Kapitel werden
Schlüssel beschrieben, die den Aufbau eines solchen Trusted Channels mittels
symmetrischer Verfahren ermöglichen. Die Schlüssel zum Aufbau mittels
asymmetrischer Verfahren werden in 5.3.15 beschrieben.

Voraussetzung für den Aufbau mittels symmetrischer Verfahren ist, dass sowohl
die zu administrierende Karte, als auch das administrierende System über
denselben symmetrischen Schlüssel verfügen.

Wenn die symmetrischen Schlüssel (SK.CMS und SK.CUP) für die Authentifizierung
des Kartenadministrationssystems genutzt werden, dann MÜSSEN sie
kartenindividuell  personalisiert werden, so dass mit einem Schlüssel eines
administrierenden Systems  genau eine SMC-B administriert werden kann.

Bei der Personalisierung sind nur die Schlüssel zu personalisieren, die
tatsächlich benötigt werden.

### 5.3.14.1 MF / SK.CMS.AES128

SK.CMS.AES128 (optional) ist der geheime Schlüssel für die Durchführung des
SMC-B/CMS-Authentisierungsverfahrens mit Aufbau eines Trusted Channel. Die
nachfolgende Tabelle Tab_SMC-B_ObjSys_033 zeigt die Eigenschaften des
Schlüssels.

**Card-G2-A_2194-01 - K_Initialisierung: Initialisierte Attribute von MF /
SK.CMS.AES128**

SK.CMS.AES128 MUSS die in Tab_SMC-B_ObjSys_033 dargestellten Werte besitzen.

Tabelle39: Tab_SMC-B_ObjSys_033 Initialisierte Attribute von MF / SK.CMS.AES128

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
Symmetrisches Authentisierungsobjekt

</td><td>
</td></tr><tr><td>
keyType

</td><td>
AES-128

</td><td>
</td></tr><tr><td>
keyIdentifier

</td><td>
‘14’ = 20

</td><td>
</td></tr><tr><td>
encKey

</td><td>
herstellerspezifisch „unbefüllt“, Speicherplatz hinreichend für einen
symmetrischen AES-Schlüssel mit 128 Bit

</td><td>
wird personalisiert

</td></tr><tr><td>
macKey

</td><td>
herstellerspezifisch „unbefüllt“, Speicherplatz hinreichend für einen
symmetrischen AES-Schlüssel mit 128 Bit

</td><td>
wird personalisiert

</td></tr><tr><td>
numberScenario

</td><td>
0

</td><td>
</td></tr><tr><td>
algorithmIdentifier

</td><td>
aesSessionkey4SM 

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
MUTUAL AUTHENTICATE

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
GENERAL AUTHENTICATE

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
NEVER

</td><td>
</td></tr></table>

**[\<=]**

**A_19318 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von MF / SK.CMS.AES128**

SK.CMS.AES128 MUSS die in der folgenden Tabelle dargestellten Zugriffsregeln
für die kontaktlose Schnittstelle besitzen.

Tabelle40: Zugriffsregeln für die kontaktlose Schnittstelle von MF /
SK.CMS.AES128

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
MUTUAL AUTHENTICATE

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
GENERAL AUTHENTICATE

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
NEVER

</td><td>
</td></tr></table>

**[\<=]**

**Card-G2-A_3358 - K_Personalisierung: Personalisierte Attribute von MF /
SK.CMS.AES128**

Falls das symmetrische Authentifizierungsverfahren genutzt werden soll, dann
MÜSSEN bei der Personalisierung von SK.CMS.AES128 die in Tab_SMC-B_ObjSys_086
angegebenen Attribute mit den dort angegebenen Inhalten personalisiert werden.

Tabelle41: Tab_SMC-B_ObjSys_086 Personalisierte Attribute von MF / SK.CMS.AES128

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
encKey

</td><td>
Symmetrischer Schlüssel AES.128 gemäß [gemSpec_Krypt#2.4]

</td><td>
</td></tr><tr><td>
macKey

</td><td>
Symmetrischer Schlüssel AES.128 gemäß [gemSpec_Krypt#2.4]

</td><td>
</td></tr></table>

**[\<=]**

### 5.3.14.2 MF / SK.CMS.AES256

SK.CMS.AES256 (optional) ist der geheime Schlüssel für die Durchführung des
SMC-B / CMS-Authentisierungsverfahrens mit Aufbau eines Trusted Channel.

**Card-G2-A_2195-01 - K_Initialisierung: Initialisierte Attribute von MF /
SK.CMS.AES256**

SK.CMS.AES256 MUSS die in Tab_SMC-B_ObjSys_034 dargestellten Werte besitzen.

Tabelle42: Tab_SMC-B_ObjSys_034 Initialisierte Attribute von MF / SK.CMS.AES256

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
Symmetrisches Authentisierungsobjekt

</td><td>
</td></tr><tr><td>
keyType

</td><td>
AES-256

</td><td>
</td></tr><tr><td>
keyIdentifier

</td><td>
‘18’ = 24

</td><td>
</td></tr><tr><td>
encKey

</td><td>
herstellerspezifisch „unbefüllt“, Speicherplatz hinreichend für einen
symmetrischen AES-Schlüssel mit 256 Bit

</td><td>
wird personalisiert

</td></tr><tr><td>
macKey

</td><td>
herstellerspezifisch „unbefüllt“, Speicherplatz hinreichend für einen
symmetrischen AES-Schlüssel mit 256 Bit

</td><td>
wird personalisiert

</td></tr><tr><td>
numberScenario

</td><td>
0

</td><td>
</td></tr><tr><td>
algorithmIdentifier

</td><td>
aesSessionkey4SM

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
MUTUAL AUTHENTICATE

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
GENERAL AUTHENTICATE

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
NEVER

</td><td>
</td></tr></table>

**[\<=]**

**A_19319 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von MF / SK.CMS.AES256**

SK.CMS.AES256 MUSS die in der folgenden Tabelle dargestellten Zugriffsregeln
für die kontaktlose Schnittstelle besitzen.

Tabelle43: Zugriffsregeln für die kontaktlose Schnittstelle von MF /
SK.CMS.AES256

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
MUTUAL AUTHENTICATE

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
GENERAL AUTHENTICATE

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
NEVER

</td><td>
</td></tr></table>

**[\<=]**

**Card-G2-A_3359 - K_Personalisierung: Personalisierte Attribute von MF /
SK.CMS.AES256**

Falls das symmetrische Authentifizierungsverfahren genutzt werden soll, dann
MÜSSEN bei der Personalisierung von SK.CMS.AES256 die in Tab_SMC-B_ObjSys_087
angegebenen Attribute mit den dort angegebenen Inhalten personalisiert werden.

Tabelle44: Tab_SMC-B_ObjSys_087 Personalisierte Attribute von MF / SK.CMS.AES256

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
encKey

</td><td>
Symmetrischer Schlüssel AES.256 gemäß [gemSpec_Krypt#2.4]

</td><td>
</td></tr><tr><td>
macKey

</td><td>
Symmetrischer Schlüssel AES.256 gemäß [gemSpec_Krypt#2.4]

</td><td>
</td></tr></table>

**[\<=]**

### 5.3.14.3 MF / SK.CUP.AES128

Dieser AES-Schlüssel mit 128 bit Schlüssellänge wird benötigt, um dem CUPS
administrative Zugriffe auf die SMC-B bezüglich der Zertifikate zu erlauben.

**Card-G2-A_3360-01 - K_Initialisierung: Initialisierte Attribute von MF /
SK.CUP.AES128**

SK.CUP.AES128 MUSS die in Tab_SMC-B_ObjSys_113 dargestellten Initialisierten
Attribute besitzen.

Tabelle45: Tab_SMC-B_ObjSys_113 Initialisierte Attribute von MF / SK.CUP.AES128

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
Symmetrisches Authentisierungsobjekt

</td><td>
</td></tr><tr><td>
keyType

</td><td>
AES-128

</td><td>
</td></tr><tr><td>
keyIdentifier

</td><td>
’03’ = 3

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td>
encKey

</td><td>
herstellerspezifisch „unbefüllt“, Speicherplatz hinreichend für einen
symmetrischen AES-Schlüssel mit 128 Bit

</td><td>
wird personalisiert

</td></tr><tr><td>
macKey

</td><td>
herstellerspezifisch „unbefüllt“, Speicherplatz hinreichend für einen
symmetrischen AES-Schlüssel mit 128 Bit

</td><td>
wird personalisiert

</td></tr><tr><td>
numberScenario

</td><td>
0

</td><td>
</td></tr><tr><td>
algorithmIdentifier

</td><td>
aesSessionkey4SM

</td><td>
</td></tr><tr><td>
accessRuleSessionkeys

</td><td>
irrelevant

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
MUTUAL AUTHENTICATE

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
GENERAL AUTHENTICATE

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
NEVER

</td><td>
</td></tr></table>

**[\<=]**

**A_19320 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von MF / SK.CUP.AES128**

SK.CUP.AES128 MUSS die in der folgenden Tabelle dargestellten Zugriffsregeln
für die kontaktlose Schnittstelle besitzen.

Tabelle46: Zugriffsregeln für die kontaktlose Schnittstelle von MF /
SK.CUP.AES128

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
MUTUAL AUTHENTICATE

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
GENERAL AUTHENTICATE

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
NEVER

</td><td>
</td></tr></table>

**[\<=]**

**Card-G2-A_3361 - K_Personalisierung: Personalisierte Attribute von MF /
SK.CUP.AES128**

Falls das symmetrische Authentifizierungsverfahren genutzt werden soll, dann
MÜSSEN bei der Personalisierung von SK.CUP.AES128 die in Tab_SMC-B_ObjSys_114
angegebenen Attribute mit den dort angegebenen Inhalten personalisiert werden.

Tabelle47: Tab_SMC-B_ObjSys_114 Personalisierte Attribute von MF / SK.CUP.AES128

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
encKey

</td><td>
Symmetrischer Schlüssel AES.128 gemäß [gemSpec_Krypt#2.4]

</td><td>
</td></tr><tr><td>
macKey

</td><td>
Symmetrischer Schlüssel AES.128 gemäß [gemSpec_Krypt#2.4]

</td><td>
</td></tr></table>

**[\<=]**

### 5.3.14.4 MF / SK.CUP.AES256

Dieser AES-Schlüssel mit 256 bit Schlüssellänge wird benötigt, um dem CUPS
administrative Zugriffe auf die SMC-B bezüglich der Zertifikate zu erlauben.

**Card-G2-A_3362-01 - K_Initialisierung: Initialisierte Attribute von MF /
SK.CUP.AES256**

SK.CUP.AES256 MUSS die in Tab_SMC-B_ObjSys_115 dargestellten Initialisierten
Attribute besitzen.

Tabelle48: Tab_SMC-B_ObjSys_115 Initialisierte Attribute von MF / SK.CUP.AES256

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
Symmetrisches Authentisierungsobjekt

</td><td>
</td></tr><tr><td>
keyType

</td><td>
AES-256

</td><td>
</td></tr><tr><td>
keyIdentifier

</td><td>
’04’ = 4

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td>
encKey

</td><td>
herstellerspezifisch „unbefüllt“, Speicherplatz hinreichend für einen
symmetrischen AES-Schlüssel mit 256 Bit

</td><td>
wird personalisiert

</td></tr><tr><td>
macKey

</td><td>
herstellerspezifisch „unbefüllt“, Speicherplatz hinreichend für einen
symmetrischen AES-Schlüssel mit 256 Bit

</td><td>
wird personalisiert

</td></tr><tr><td>
numberScenario

</td><td>
0

</td><td>
</td></tr><tr><td>
algorithmIdentifier

</td><td>
aesSessionkey4SM

</td><td>
</td></tr><tr><td>
accessRuleSessionkeys

</td><td>
irrelevant

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
MUTUAL AUTHENTICATE

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
GENERAL AUTHENTICATE

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
NEVER

</td><td>
</td></tr></table>

**[\<=]**

**A_19321 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von MF / SK.CUP.AES256**

SK.CUP.AES256 MUSS die in der folgenden Tabelle dargestellten Zugriffsregeln
für die kontaktlose Schnittstelle besitzen.

Tabelle49: Zugriffsregeln für die kontaktlose Schnittstelle von MF /
SK.CUP.AES256

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
MUTUAL AUTHENTICATE

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
GENERAL AUTHENTICATE

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR  AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
NEVER

</td><td>
</td></tr></table>

**[\<=]**

**Card-G2-A_3363 - K_Personalisierung: Personalisierte Attribute von MF /
SK.CUP.AES256**

Falls das symmetrische Authentifizierungsverfahren genutzt werden soll, dann
MÜSSEN bei der Personalisierung von SK.CUP.AES256 die in Tab_SMC-B_ObjSys_116
angegebenen Attribute mit den dort angegebenen Inhalten personalisiert werden.

Tabelle50: Tab_SMC-B_ObjSys_116 Personalisierte Attribute von MF / SK.CUP.AES256

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
encKey

</td><td>
Symmetrischer Schlüssel AES.256 gemäß [gemSpec_Krypt#2.4]

</td><td>
</td></tr><tr><td>
macKey

</td><td>
Symmetrischer Schlüssel AES.256 gemäß [gemSpec_Krypt#2.4]

</td><td>
</td></tr></table>

**[\<=]**

### 5.3.15 MF / SK.CAN (SMC-B CL)

Das Schlüsselobjekt SK.CAN mit der Card Access Number wird für die
kryptografische Absicherung der Kartenkommunikation über die kontaktlose
Schnittstelle verwendet.

**A_19353 - (SMC-B CL) K_Initialisierung: Initialisierte Attribute von MF /
SK.CAN**

SK.CAN MUSS die in der folgenden Tabelle dargestellten Attribute besitzen.

Tabelle51: Initialisierte Attribute von MF / SK.CAN

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
symmetrisches Kartenverbindungsobjekt

</td><td>
</td></tr><tr><td>
keyIdentifier

</td><td>
’02’ = 2

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td>
can

</td><td>
herstellerspezifisch „unbefüllt“, Speicherplatz hinreichend für ein
Schlüsselobjekt SK.CAN

</td><td>
</td></tr><tr><td>
algorithmIdentifier

</td><td>
id-PACE-ECDH-GM-AES-CBC-CMAC-128

</td><td>
</td></tr><tr><td>
accessRuleSessionkeys

</td><td>
irrelevant

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregeln für die Kontaktschnittstelle

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
GENERAL AUTHENTICATE

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
Andere

</td><td>
NEVER

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
Alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
Alle

</td><td>
NEVER

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregeln für die kontaktlose Schnittstelle

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
GENERAL AUTHENTICATE

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
Andere

</td><td>
NEVER

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
Alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
Alle

</td><td>
NEVER

</td><td>
</td></tr></table>

**[\<=]**

**A_19354 - (SMC-B CL) K_Personalisierung: Personalisierte Attribute von MF /
SK.CAN**

SK.CAN  MUSS  durch die Personalisierung die in der folgenden Tabelle
dargestellten Inhalte erhalten.

Tabelle52: Personalisierte Attribute von MF / SK.CAN

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
can

</td><td>
SK.CAN gemäß [gemSpec_CAN_TI]

</td><td>
</td></tr></table>

**[\<=]**

### 5.4 Die ESIGN-Anwendung DF.ESIGN

### 5.4.1 Dateistruktur und Dateiinhalt

Die allgemeine ESIGN-Anwendung ist in[EN14890-1]dargestellt und wird in der
SMC-B für folgende Funktionen genutzt:

 ---> UL

![Abbildung-2][Abbildung-2]

### 5.4.2 MF / DF.ESIGN (Krypto-Anwendung ESIGN)

Abbildung 3 zeigt die prinzipielle Dateistruktur der ESIGN-Anwendung gemäß
EN14890.

![Abbildung-3][Abbildung-3]

**Card-G2-A_2203 - K_Initialisierung: Initialisierte Attribute von MF /
DF.ESIGN**

DF.ESIGN MUSS die in Tab_SMC-B_ObjSys_040 dargestellten Werte besitzen.

Tabelle53: Tab_SMC-B_ObjSys_040 Initialisierte Attribute von MF / DF.ESIGN

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
Ordner

</td><td>
</td></tr><tr><td>
applicationIdentifier

</td><td>
'A000000167 455349474E’

</td><td>
gemäß [EN14890-1]

</td></tr><tr><td>
fileIdentifier

</td><td>
–

</td><td>
siehe Kapitel 4.4.1

</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td>
shareable

</td><td>
True

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
GET RANDOM

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
LOAD APPLICATION

</td><td>
AUT_CMS

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr></table>

**[\<=]**

**A_19322-01 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von MF / DF.ESIGN**

DF.ESIGN MUSS die in der folgenden Tabelle dargestellten Zugriffsregeln für die
kontaktlose Schnittstelle besitzen.

Tabelle54: Zugriffsregeln für die kontaktlose Schnittstelle von MF / DF.ESIGN

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
GET RANDOM

</td><td>
AUT_PACE

</td><td>
</td></tr><tr><td>
LOAD APPLICATION

</td><td>
AUT_CMS

</td><td>
</td></tr><tr><td>
andere

</td><td>
NEVER

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr></table>

**[\<=]**

### 5.4.2.1 MF / DF.ESIGN / EF.C.HCI.OSIG.R2048

EF.C.HCI.OSIG.R2048 enthält ein Zertifikat mit dem öffentlichen Schlüssel
PuK.HCI.OSIG.R2048 zu PrK.HCI.OSIG.R2048 (siehe Kapitel 5.4.2.4).

**Card-G2-A_2204-01 - K_Initialisierung: Initialisierte Attribute von MF /
DF.ESIGN / EF.C.HCI.OSIG.R2048**

EF.C.HCI.OSIG.R2048 MUSS die in Tab_SMC-B_ObjSys_041 dargestellten Werte
besitzen.

Tabelle55: Tab_SMC-B_ObjSys_041 Initialisierte Attribute von MF / DF.ESIGN /
EF.C.HCI.OSIG.R2048

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
transparentes Elementary File

</td><td>
</td></tr><tr><td>
fileIdentifier

</td><td>
‘C0 00’

</td><td>
</td></tr><tr><td>
shortFileIdentifier

</td><td>
‘10’= 16

</td><td>
</td></tr><tr><td>
numberOfOctet

</td><td>
‘07 6C’ Oktett = 1900 Oktett

</td><td>
</td></tr><tr><td>
positionLogicalEndOfFile

</td><td>
Wildcard

</td><td>
siehe Card-G2-A_2668

</td></tr><tr><td>
flagTransactionMode

</td><td>
True

</td><td>
</td></tr><tr><td>
flagChecksum

</td><td>
False

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td>
shareable

</td><td>
True

</td><td>
</td></tr><tr><td>
body

</td><td>
kein Inhalt

</td><td>
wird personalisiert

</td></tr><tr><td colspan="3">
Kontaktbehaftete Zugriffsregel für logischen LCS „Operational state
(activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
READ BINARY

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
DELETE  
SET LOGICAL EOF  
WRITE BINARY

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr></table>

**[\<=]**

**A_19323 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von MF / DF.ESIGN / EF.C.HCI.OSIG.R2048**

EF.C.HCI.OSIG.R2048 MUSS die in der folgenden Tabelle dargestellten
Zugriffsregeln für die kontaktlose Schnittstelle besitzen.

Tabelle56: Zugriffsregeln für die kontaktlose Schnittstelle von MF / DF.ESIGN /
EF.C.HCI.OSIG.R2048

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
READ BINARY

</td><td>
AUT_PACE OR AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5 und 1.5.1

</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
SET LOGICAL EOF

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
WRITE BINARY

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr></table>

**[\<=]**

**Card-G2-A_3371-01 - K_Personalisierung: Personalisierte Attribute von MF /
DF.ESIGN / EF.C.HCI.OSIG.R2048**

Bei der Personalisierung von EF.C.HCI.OSIG.R2048 MÜSSEN die in
Tab_SMC-B_ObjSys_092 angegebenen Attribute mit den dort angegebenen Inhalten
personalisiert werden.

Tabelle57: Tab_SMC-B_ObjSys_092 Personalisierte Attribute von MF / DF.ESIGN /
EF.C.HCI.OSIG.R2048

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
positionLogicalEndOfFile

</td><td>
Wildcard

</td><td>
siehe Card-G2-A_2668

</td></tr><tr><td>
body

</td><td>
C.HCI.OSIG.R2048 gemäß [gemSpec_PKI] passend zu dem privaten Schlüssel in
PrK.HCI.OSIG.R2048

</td><td>
</td></tr></table>

**[\<=]**

### 5.4.2.2 MF / DF.ESIGN / EF.C.HCI.AUT.R2048

Diese Datei enthält ein Zertifikat mit dem öffentlichen Schlüssel
PuK.HCI.AUT.R2048 zu PrK.HCI.AUT.R2048 (siehe Kapitel 5.4.2.5).

**Card-G2-A_2207-01 - K_Initialisierung: Initialisierte Attribute von MF /
DF.ESIGN / EF.C.HCI.AUT.R2048**

EF.C.HCI.AUT.R2048 MUSS die in Tab_SMC-B_ObjSys_042 dargestellten Werte besitzen.

Tabelle58: Tab_SMC-B_ObjSys_042 Initialisierte Attribute von MF / DF.ESIGN /
EF.C.HCI.AUT.R2048

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
transparentes Elementary File

</td><td>
</td></tr><tr><td>
fileIdentifier

</td><td>
‘C5 00’

</td><td>
</td></tr><tr><td>
shortFileIdentifier

</td><td>
‘01’= 1

</td><td>
</td></tr><tr><td>
numberOfOctet

</td><td>
‘07 6C’ Oktett = 1900 Oktett

</td><td>
</td></tr><tr><td>
positionLogicalEndOfFile

</td><td>
Wildcard

</td><td>
siehe Card-G2-A_2668

</td></tr><tr><td>
flagTransactionMode

</td><td>
True

</td><td>
</td></tr><tr><td>
flagChecksum

</td><td>
False

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td>
shareable

</td><td>
True

</td><td>
</td></tr><tr><td>
body

</td><td>
kein Inhalt

</td><td>
wird personalisiert

</td></tr><tr><td colspan="3">
Kontaktbehaftete Zugriffsregel für logischen LCS „Operational state
(activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
READ BINARY

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
DELETE  
SET LOGICAL EOF  
WRITE BINARY

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr></table>

**[\<=]**

**A_19325 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von MF / DF.ESIGN / EF.C.HCI.AUT.R2048**

EF.C.HCI.AUT.R2048 MUSS die in der folgenden Tabelle dargestellten
Zugriffsregeln für die kontaktlose Schnittstelle besitzen.

Tabelle59: Zugriffsregeln für die kontaktlose Schnittstelle von MF / DF.ESIGN /
EF.C.HCI.AUT.R2048

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
READ BINARY 

</td><td>
AUT_PACE OR AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5 und 1.5.1

</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
SET LOGICAL EOF

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
WRITE BINARY

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr></table>

**[\<=]**

**Card-G2-A_3365-01 - K_Personalisierung: Personalisierte Attribute von MF /
DF.ESIGN / EF.C.HCI.AUT.R2048**

Bei der Personalisierung von EF.C.HCI.AUT.R2048 MÜSSEN die in
Tab_SMC-B_ObjSys_094 angegebenen Attribute mit den dort angegebenen Inhalten
personalisiert werden.

Tabelle60: Tab_SMC-B_ObjSys_094 Personalisierte Attribute von MF / DF.ESIGN /
EF.C.HCI.AUT.R2048

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
positionLogicalEndOfFile

</td><td>
Wildcard

</td><td>
siehe Card-G2-A_2668

</td></tr><tr><td>
body

</td><td>
C.HCI.AUT.R2048 gemäß [gemSpec_PKI] passend zu dem privaten Schlüssel in
PrK.HCI.AUT.R2048

</td></tr></table>

**[\<=]**

### 5.4.2.3 MF / DF.ESIGN / EF.C.HCI.ENC.R2048

Diese Datei enthält ein Zertifikat mit dem öffentlichen Schlüssel
PuK.HCI.ENC.R2048. Das zugehörende private Schlüsselobjekt PrK.HCI.ENC.R2048
ist in Kapitel 5.4.2.6 definiert.

**Card-G2-A_2210-02 - K_Initialisierung: Initialisierte Attribute von MF /
DF.ESIGN / EF.C.HCI.ENC.R2048**

EF.C.HCI.ENC.R2048 MUSS die in Tab_SMC-B_ObjSys_043 dargestellten Werte besitzen.

Tabelle61: Tab_SMC-B_ObjSys_043 Initialisierte Attribute von MF / DF.ESIGN /
EF.C.HCI.ENC.R2048

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
transparentes Elementary File

</td><td>
</td></tr><tr><td>
fileIdentifier

</td><td>
‘C2 00’

</td><td>
</td></tr><tr><td>
shortFileIdentifier

</td><td>
‘02’= 2

</td><td>
</td></tr><tr><td>
numberOfOctet

</td><td>
‘07 6C’ Oktett = 1900 Oktett

</td><td>
</td></tr><tr><td>
positionLogicalEndOfFile

</td><td>
Wildcard

</td><td>
siehe Card-G2-A_2668

</td></tr><tr><td>
flagTransactionMode

</td><td>
True

</td><td>
</td></tr><tr><td>
flagChecksum

</td><td>
False

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td>
shareable

</td><td>
True

</td><td>
</td></tr><tr><td>
body

</td><td>
kein Inhalt

</td><td>
wird personalisiert

</td></tr><tr><td colspan="3">
Kontaktbehaftete Zugriffsregel für logischen LCS „Operational state
(activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
READ BINARY

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
DELETE  
SET LOGICAL EOF  
WRITE BINARY

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr></table>

**[\<=]**

**A_19326 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von MF / DF.ESIGN / EF.C.HCI.ENC.R2048**

EF.C.HCI.ENC.R2048 MUSS die in der folgenden Tabelle dargestellten
Zugriffsregeln für die kontaktlose Schnittstelle besitzen.

Tabelle62: Zugriffsregeln für die kontaktlose Schnittstelle von MF / DF.ESIGN /
EF.C.HCI.ENC.R2048

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
READ BINARY

</td><td>
AUT_PACE OR AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5 und 1.5.1

</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
SET LOGICAL EOF

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
WRITE BINARY

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr></table>

**[\<=]**

**Card-G2-A_3366-01 - K_Personalisierung: Personalisierte Attribute von MF /
DF.ESIGN / EF.C.HCI.ENC.R2048**

Bei der Personalisierung von EF.C.HCI.ENC.R2048 MÜSSEN die in
Tab_SMC-B_ObjSys_096 angegebenen Attribute mit den dort angegebenen Inhalten
personalisiert werden.

Tabelle63: Tab_SMC-B_ObjSys_096 Personalisierte Attribute von MF / DF.ESIGN /
EF.C.HCI.ENC.R2048

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
positionLogicalEndOfFile

</td><td>
Wildcard

</td><td>
siehe Card-G2-A_2668

</td></tr><tr><td>
body

</td><td>
C.HCI.ENC.R2048 gemäß [gemSpec_PKI] passend zu dem privaten Schlüssel in
PrK.HCI.ENC.R2048

</td><td>
</td></tr></table>

**[\<=]**

### 5.4.2.4 MF / DF.ESIGN / PrK.HCI.OSIG.R2048

PrK.HCI.OSIG.R2048 ist der private Schlüssel zur Berechnung einer
Organisationssignatur. Der zugehörige öffentliche Schlüssel
PuK.HCI.OSIG.R2048 ist in C.HCI.OSIG.R2048 (siehe Kapitel 5.4.2.1) enthalten.

**Card-G2-A_2217-01 - K_Initialisierung: Initialisierte Attribute von MF /
DF.ESIGN / PrK.HCI.OSIG.R2048**

PrK.HCI.OSIG.R2048 MUSS die in Tab_SMC-B_ObjSys_044 dargestellten Werte besitzen.

Tabelle64: Tab_SMC-B_ObjSys_044 Initialisierte Attribute von MF / DF.ESIGN /
PrK.HCI.OSIG.R2048

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
privates Schlüsselobjekt, RSA 2048

</td><td>
</td></tr><tr><td>
keyIdentifier

</td><td>
‘04’ = 4

</td><td>
</td></tr><tr><td>
privateKey

</td><td>
herstellerspezifisch „unbefüllt“, Speicherplatz hinreichend für einen
Schlüssel mit Moduluslänge 2048 Bit

</td><td>
wird personalisiert

</td></tr><tr><td>
keyAvailable

</td><td>
WildCard

</td><td>
wird personalisiert

</td></tr><tr><td>
listAlgorithmIdentifier

</td><td>
signPSS

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
PSO COMPUTE DIGITAL SIGNATURE

</td><td>
PWD(PIN.SMC)

</td><td>
</td></tr><tr><td>
GENERATE ASYMMETRIC KEY PAIR  
P1=‘81’

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
NEVER

</td><td>
</td></tr></table>

**[\<=]**

**A_19335 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von MF / DF.ESIGN / PrK.HCI.OSIG.R2048**

PrK.HCI.OSIG.R2048 MUSS die in der folgenden Tabelle dargestellten
Zugriffsregeln für die kontaktlose Schnittstelle besitzen.

Tabelle65: Zugriffsregeln für die kontaktlose Schnittstelle von MF / DF.ESIGN /
PrK.HCI.OSIG.R2048

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
PSO COMPUTE DIGITAL SIGNATURE

</td><td>
AUT_PACE AND PWD(PIN.SMC)

</td><td>
siehe Kapitel 1.5.1

</td></tr><tr><td>
GENERATE ASYMMETRIC KEY PAIR, P1 = '81'

</td><td>
AUT_PACE OR AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5 und 1.5.1

</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
NEVER

</td><td>
</td></tr></table>

**[\<=]**

**Card-G2-A_3367 - K_Personalisierung: Personalisierte Attribute von MF /
DF.ESIGN / PrK.HCI.OSIG.R2048**

Bei der Personalisierung von PrK.HCI.OSIG.R2048 MÜSSEN die in
Tab_SMC-B_ObjSys_100 angegebenen Attribute mit den dort angegebenen Inhalten
personalisiert werden.

Tabelle66: Tab_SMC-B_ObjSys_100 Personalisierte Attribute von MF / DF.ESIGN /
PrK.HCI.OSIG.R2048

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
privateKey

</td><td>
Moduluslänge 2048 Bit

</td><td>
</td></tr><tr><td>
keyAvailable

</td><td>
True

</td><td>
</td></tr></table>

**[\<=]**

### 5.4.2.5 MF / DF.ESIGN / PrK.HCI.AUT.R2048

PrK.HCI.AUT.R2048 ist der private Schlüssel für Client/Server-Authentisierung.
Der zugehörige öffentliche Schlüssel PuK.HCI.AUT.R2048 ist in
C.HCI.AUT.R2048 (siehe Kapitel 5.4.2.2) enthalten.

**Card-G2-A_2220-01 - K_Initialisierung: Initialisierte Attribute von MF /
DF.ESIGN / PrK.HCI.AUT.R2048**

PrK.HCI.AUT.R2048 MUSS die in Tab_SMC-B_ObjSys_047 dargestellten Werte besitzen.

Tabelle67: Tab_SMC-B_ObjSys_047 Initialisierte Attribute von MF / DF.ESIGN /
PrK.HCI.AUT.R2048

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
privates Schlüsselobjekt, RSA 2048

</td><td>
</td></tr><tr><td>
keyIdentifier

</td><td>
‘02’ = 2

</td><td>
</td></tr><tr><td>
privateKey

</td><td>
herstellerspezifisch „unbefüllt“, Speicherplatz hinreichend für einen
Schlüssel mit Moduluslänge 2048 Bit

</td><td>
wird personalisiert

</td></tr><tr><td>
keyAvailable

</td><td>
WildCard

</td><td>
wird personalisiert

</td></tr><tr><td>
listAlgorithmIdentifier

</td><td>
alle Werte aus der Menge {rsaClientAuthentication, signPKCS1_V1_5, signPSS}

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
GENERATE ASYMMETRIC KEY PAIR  
P1=‘81’

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
INTERNAL AUTHENTICATE

</td><td>
PWD(PIN.SMC)

</td><td>
</td></tr><tr><td>
PSO COMPUTE DIGITAL SIGNATURE

</td><td>
PWD(PIN.SMC)

</td><td>
</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
NEVER

</td><td>
</td></tr></table>

**[\<=]**

**A_19336 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von MF / DF.ESIGN / PrK.HCI.AUT.R2048**

PrK.HCI.AUT.R2048 MUSS die in der folgenden Tabelle dargestellten Zugriffsregeln
für die kontaktlose Schnittstelle besitzen.

Tabelle68: Zugriffsregeln für die kontaktlose Schnittstelle von MF / DF.ESIGN /
PrK.HCI.AUT.R2048

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
GENERATE ASYMMETRIC KEY PAIR, P1 = '81'

</td><td>
AUT_PACE OR AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5 und 1.5.1

</td></tr><tr><td>
INTERNAL AUTHENTICATE

</td><td>
AUT_PACE AND PWD(PIN.SMC)

</td><td>
siehe Kapitel 1.5.1

</td></tr><tr><td>
PSO COMPUTE DIGITAL SIGNATURE

</td><td>
AUT_PACE AND PWD(PIN.SMC)

</td><td>
siehe Kapitel 1.5.1

</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
NEVER

</td><td>
</td></tr></table>

**[\<=]**

**Card-G2-A_3368 - K_Personalisierung: Personalisierte Attribute von MF /
DF.ESIGN / PrK.HCI.AUT.R2048**

Bei der Personalisierung von PrK.HCI.AUT.R2048 MÜSSEN die in
Tab_SMC-B_ObjSys_103 angegebenen Attribute mit den dort angegebenen Inhalten
personalisiert werden.

belle69: Tab_SMC-B_ObjSys_103 Personalisierte Attribute von MF / DF.ESIGN /
PrK.HCI.AUT.R2048

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
privateKey

</td><td>
Moduluslänge 2048 Bit]

</td><td>
</td></tr><tr><td>
keyAvailable

</td><td>
True

</td><td>
</td></tr></table>

**[\<=]**

### 5.4.2.6 MF / DF.ESIGN / PrK.HCI.ENC.R2048

PrK.HCI.ENC.R2048 ist der private Schlüssel für den PKI-Dienst zur
Entschlüsselung und Umschlüsselung eines Dokumenten-Chiffrierungsschlüssels.
Der zugehörige öffentliche Schlüssel PuK.HCI.ENC.R2048 ist in
C.HCI.ENC.R2048 (siehe Kapitel 5.4.2.3) enthalten.

**Card-G2-A_2223 - K_Initialisierung: Initialisierte Attribute von MF / DF.ESIGN
/ PrK.HCI.ENC.R2048**

PrK.HCI.ENC.R2048 MUSS die in Tab_SMC-B_ObjSys_050 dargestellten Werte besitzen.

Tabelle70: Tab_SMC-B_ObjSys_050 Initialisierte Attribute von MF / DF.ESIGN /
PrK.HCI.ENC.R2048

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
privates RSA Entschlüsselungsobjekt

</td><td>
</td></tr><tr><td>
keyIdentifier

</td><td>
‘03’ = 3

</td><td>
</td></tr><tr><td>
privateKey

</td><td>
herstellerspezifisch „unbefüllt“, Speicherplatz hinreichend für einen
Schlüssel mit Moduluslänge 2048 Bit

</td><td>
wird personalisiert

</td></tr><tr><td>
keyAvailable

</td><td>
WildCard

</td><td>
wird personalisiert

</td></tr><tr><td>
listAlgorithmIdentifier

</td><td>
rsaDecipherOaep

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
PSO DECIPHER

</td><td>
PWD(PIN.SMC)

</td><td>
</td></tr><tr><td>
PSO TRANSCIPHER

</td><td>
PWD(PIN.SMC)

</td><td>
</td></tr><tr><td>
GENERATE ASYMMETRIC KEY PAIR  
P1=‘81’

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
ssiehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
NEVER

</td><td>
</td></tr></table>

**[\<=]**

**A_19337 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von MF / DF.ESIGN / PrK.HCI.ENC.R2048**

PrK.HCI.ENC.R2048 MUSS die in der folgenden Tabelle dargestellten Zugriffsregeln
für die kontaktlose Schnittstelle besitzen.

Tabelle71: Zugriffsregeln für die kontaktlose Schnittstelle von MF / DF.ESIGN /
PrK.HCI.ENC.R2048

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
GENERATE ASYMMETRIC KEY PAIR, P1 = '81'

</td><td>
AUT_PACE OR AUT_CMS OR AUT_CUP

</td><td>
</td></tr><tr><td>
PSO DECIPHER

</td><td>
AUT_PACE AND PWD(PIN.SMC)

</td><td>
siehe Kapitel 1.5.1

</td></tr><tr><td>
PSO TRANSCIPHER

</td><td>
AUT_PACE AND PWD(PIN.SMC)

</td><td>
siehe Kapitel 1.5.1

</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
NEVER

</td><td>
</td></tr></table>

**[\<=]**

**Card-G2-A_3369 - K_Personalisierung: Personalisierte Attribute von MF /
DF.ESIGN / PrK.HCI.ENC.R2048**

Bei der Personalisierung von PrK.HCI.ENC.R2048 MÜSSEN die in
Tab_SMC-B_ObjSys_106 angegebenen Attribute mit den dort angegebenen Inhalten
personalisiert werden.

Tabelle72: Tab_SMC-B_ObjSys_106 Personalisierte Attribute von MF / DF.ESIGN /
PrK.HCI.ENC.R2048

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
privateKey

</td><td>
Moduluslänge 2048 Bit

</td><td>
</td></tr><tr><td>
keyAvailable

</td><td>
True

</td></tr></table>

**[\<=]**

### 5.4.2.7 MF / DF.ESIGN / EF.C.HCI.OSIG.E256

Die Datei EF.C.HCI.OSIG.E256 enthält ein Zertifikat für die Kryptographie mit
elliptischen Kurven mit dem öffentlichen Schlüssel PuK.HCI.OSIG.E256. Das
zugehörende private Schlüsselobjekt PrK.HCI.OSIG.E256 ist in Kapitel 5.4.2.10
definiert.

**Card-G2-A_3652-01 - K_Initialisierung: Initialisierte Attribute von MF /
DF.ESIGN / EF.C.HCI.OSIG.E256**

EF.C.HCI.OSIG.E256 MUSS die in Tab_SMC-B_ObjSys_120  dargestellten
initialisierten Attribute besitzen.

Tabelle73: Tab_SMC-B_ObjSys_120 Initialisierte Attribute von MF / DF.ESIGN /
EF.C.HCI.OSIG.E256

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
transparentes Elementary File

</td><td>
</td></tr><tr><td>
fileIdentifier

</td><td>
‘C0 07’

</td><td>
</td></tr><tr><td>
shortFileIdentifier

</td><td>
‘07’= 7

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td>
flagTransactionMode

</td><td>
True

</td><td>
</td></tr><tr><td>
flagChecksum

</td><td>
False

</td><td>
</td></tr><tr><td>
numberOfOctet

</td><td>
‘0B B8’ Oktett = 3000 Oktett

</td><td>
</td></tr><tr><td>
positionLogicalEndOfFile

</td><td>
Wildcard

</td><td>
siehe Card-G2-A_2668

</td></tr><tr><td>
shareable

</td><td>
True

</td><td>


</td></tr><tr><td>
body

</td><td>
kein Inhalt

</td><td>
wird personalisiert

</td></tr><tr><td colspan="3">
Kontaktbehaftete Zugriffsregel für logischen LCS „Operational state
(activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
READ BINARY

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
DELETE  
SET LOGICAL EOF  
WRITE BINARY

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr></table>

**[\<=]**

**A_19338 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von MF / DF.ESIGN / EF.C.HCI.OSIG.E256**

EF.C.HCI.OSIG.E256 MUSS die in der folgenden Tabelle dargestellten
Zugriffsregeln für die kontaktlose Schnittstelle besitzen.

Tabelle74: Zugriffsregeln für die kontaktlose Schnittstelle von MF / DF.ESIGN /
EF.C.HCI.OSIG.E256

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
READ BINARY

</td><td>
AUT_PACE OR AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5 und 1.5.1

</td></tr><tr><td>
DELETE 

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
SET LOGICAL EOF

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
WRITE BINARY

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr></table>

**[\<=]**

**Card-G2-A_3653-01 - K_Personalisierung: Personalisierte Attribute von MF /
DF.ESIGN / EF.C.HCI.OSIG.E256**

Bei der Initialisierung von EF.C.HCI.OSIG.E256 MÜSSEN die in
Tab_SMC-B_ObjSys_121 angegebenen Attribute mit den dort angegebenen Inhalten
personalisiert werden.

Tabelle75: Tab_SMC-B_ObjSys_121 Personalisierte Attribute von MF / DF.ESIGN /
EF.C.HCI.OSIG.E256

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
positionLogicalEndOfFile

</td><td>
Wildcard

</td><td>
siehe Card-G2-A_2668

</td></tr><tr><td>
body

</td><td>
C.HCI.OSIG.E256 gemäß [gemSpec_PKI] passend zu dem privaten Schlüssel in
PrK.HCI.OSIG.E256

</td><td>
</td></tr></table>

**[\<=]**

### 5.4.2.8 MF / DF.ESIGN / EF.C.HCI.AUT.E256

Die Datei EF.C.HCI.AUT.E256 enthält ein Zertifikat für die Kryptographie mit
elliptischen Kurven mit dem öffentlichen Schlüssel PuK.HCI.AUT.E256. Das
zugehörende private Schlüsselobjekt PrK.HCI.AUT.E256 ist in Kapitel 5.4.2.11
definiert.

**Card-G2-A_3654-01 - K_Initialisierung: Initialisierte Attribute von MF /
DF.ESIGN / EF.C.HCI.AUT.E256**

EF.C.HCI.AUT.E256 MUSS die in Tab_SMC-B_ObjSys_122 dargestellten initialisierten
Attribute besitzen.

Tabelle76: Tab_SMC-B_ObjSys_122 Initialisierte Attribute von MF / DF.ESIGN /
EF.C.HCI.AUT.E256

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
transparentes Elementary File

</td><td>
</td></tr><tr><td>
fileIdentifier

</td><td>
‘C5 06’

</td><td>
</td></tr><tr><td>
shortFileIdentifier

</td><td>
‘06’= 6

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td>
flagTransactionMode

</td><td>
True

</td><td>
</td></tr><tr><td>
flagChecksum

</td><td>
False

</td><td>
</td></tr><tr><td>
numberOfOctet

</td><td>
‘0B B8’ Oktett = 3000 Oktett

</td><td>
</td></tr><tr><td>
positionLogicalEndOfFile

</td><td>
Wildcard

</td><td>
siehe Card-G2-A_2668

</td></tr><tr><td>
shareable

</td><td>
True

</td><td>


</td></tr><tr><td>
body

</td><td>
kein Inhalt

</td><td>
wird personalisiert

</td></tr><tr><td colspan="3">
Kontaktbehaftete Zugriffsregel für logischen LCS „Operational state
(activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
READ BINARY

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
DELETE  
SET LOGICAL EOF  
WRITE BINARY

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr></table>

**[\<=]**

**A_19339 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von MF / DF.ESIGN / EF.C.HCI.AUT.E256**

EF.C.HCI.AUT.E256 MUSS die in der folgenden Tabelle dargestellten Zugriffsregeln
für die kontaktlose Schnittstelle besitzen.

Tabelle77: Zugriffsregeln für die kontaktlose Schnittstelle von MF / DF.ESIGN /
EF.C.HCI.AUT.E256

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
READ BINARY

</td><td>
AUT_PACE OR AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5 und 1.5.1

</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
SET LOGICAL EOF

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
WRITE BINARY

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr></table>

**[\<=]**

Hinweis 53: Kommandos, die gemäß [gemSpec_COS] mit einem transparenten EF
arbeiten, sind: ACTIVATE, DEACTIVATE, DELETE, ERASE BINARY, READ BINARY,
SELECT, SET LOGICAL EOF, UPDATE BINARY, TERMINATE, WRITE BINARY

**Card-G2-A_3655-01 - K_Personalisierung: Personalisierte Attribute von MF /
DF.ESIGN / EF.C.HCI.AUT.E256**

Bei der Initialisierung von EF.C.HCI.AUT.E256 MÜSSEN die in
Tab_SMC-B_ObjSys_123 angegebenen Attribute mit den dort angegebenen Inhalten
personalisiert werden.

Tabelle78: Tab_SMC-B_ObjSys_123 Personalisierte Attribute von MF / DF.ESIGN /
EF.C.HCI.AUT.E256

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
positionLogicalEndOfFile

</td><td>
Wildcard

</td><td>
siehe Card-G2-A_2668

</td></tr><tr><td>
body

</td><td>
C.HCI.AUT.E256 gemäß [gemSpec_PKI] passend zu dem privaten Schlüssel in
PrK.HCI.AUT.E256

</td><td>
</td></tr></table>

**[\<=]**

### 5.4.2.9 MF / DF.ESIGN / EF.C.HCI.ENC.E256

Die Datei EF.C.HCI.ENC.E256 enthält ein Zertifikat für die Kryptographie mit
elliptischen Kurven mit dem öffentlichen Schlüssel PuK.HCI.ENC.E256. Das
zugehörende private Schlüsselobjekt PrK.HCI.ENC.E256 ist im Kapitel 5.4.2.12
definiert.

**Card-G2-A_3656-01 - K_Initialisierung: Initialisierte Attribute von MF /
DF.ESIGN / EF.C.HCI.ENC.E256**

EF.C.HCI.ENC.E256 MUSS die in Tab_SMC-B_ObjSys_124  dargestellten
initialisierten Attribute besitzen.

Tabelle79: Tab_SMC-B_ObjSys_124 Initialisierte Attribute von MF / DF.ESIGN/
EF.C.HCI.ENC.E256

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
transparentes Elementary File

</td><td>
</td></tr><tr><td>
fileIdentifier

</td><td>
‘C2 05’

</td><td>
</td></tr><tr><td>
shortFileIdentifier

</td><td>
‘05’= 5

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td>
flagTransactionMode

</td><td>
True

</td><td>
</td></tr><tr><td>
flagChecksum

</td><td>
False

</td><td>
</td></tr><tr><td>
numberOfOctet

</td><td>
‘0B B8’ Oktett = 3000 Oktett

</td><td>
</td></tr><tr><td>
positionLogicalEndOfFile

</td><td>
Wildcard

</td><td>
siehe Card-G2-A_2668

</td></tr><tr><td>
shareable

</td><td>
True

</td><td>


</td></tr><tr><td>
body

</td><td>
kein Inhalt

</td><td>
wird personalisiert

</td></tr><tr><td colspan="3">
Kontaktbehaftete Zugriffsregel für logischen LCS „Operational state
(activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
READ    BINARY

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
DELETE  
SET LOGICAL EOF  
WRITE BINARY

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr></table>

**[\<=]**

**A_19340 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von MF / DF.ESIGN / EF.C.HCI.ENC.E256**

EF.C.HCI.ENC.E256 MUSS die in der folgenden Tabelle dargestellten Zugriffsregeln
für die kontaktlose Schnittstelle besitzen.

Tabelle80: Zugriffsregeln für die kontaktlose Schnittstelle von MF / DF.ESIGN /
EF.C.HCI.ENC.E256

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
READ BINARY

</td><td>
AUT_PACE OR AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5 und 1.5.1

</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
SET LOGICAL EOF

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
WRITE BINARY

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr></table>

**[\<=]**

**Card-G2-A_3657-01 - K_Personalisierung: Personalisierte Attribute von MF /
DF.ESIGN / EF.C.HCI.ENC.E256**

Bei der Initialisierung von EF.C.HCI.ENC.E256 MÜSSEN die in
Tab_SMC-B_ObjSys_125 angegebenen Attribute mit den dort angegebenen Inhalten
personalisiert werden.

Tabelle81: Tab_SMC-B_ObjSys_125 Personalisierte Attribute von MF / DF.ESIGN/
EF.C.HCI.ENC.E256

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
positionLogicalEndOfFile

</td><td>
Wildcard

</td><td>
siehe Card-G2-A_2668

</td></tr><tr><td>
body

</td><td>
C.HCI.ENC.E256 gemäß [gemSpec_PKI] passend zu dem privaten Schlüssel in
PrK.HCI.ENC.E256

</td><td>
</td></tr></table>

**[\<=]**

### 5.4.2.10 MF / DF.ESIGN / PrK.HCI.OSIG.E256

PrK.HCI.OSIG.E256 ist der private Schlüssel für die Kryptographie mit
elliptischen Kurven für Client/Server-Authentisierung. Der zugehörige
öffentliche Schlüssel PuK.HCI.OSIG.E256 ist in C.HCI.OSIG.E256 (siehe Kapitel
5.5.2.7) enthalten.

**Card-G2-A_3658-01 - K_Initialisierung: Initialisierte Attribute von MF /
DF.ESIGN / PrK.HCI.OSIG.E256**

PrK.HCI.OSIG.E256  MUSS die in Tab_SMC-B_ObjSys_126 dargestellten,
initialisierten Attribute besitzen.

Tabelle82: Tab_SMC-B_ObjSys_126 Initialisierte Attribute von MF / DF.ESIGN /
PrK.HCI.OSIG.E256

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
privates Schlüsselobjekt, ELC 256

</td><td>
</td></tr><tr><td>
keyIdentifier

</td><td>
‘07’ = 7

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td>
privateElcKey

</td><td>
domainparameter = brainpoolP256r1

</td><td>
</td></tr><tr><td>
privateElcKey

</td><td>
keyData = AttributNotSet

</td><td>
wird personalisiert

</td></tr><tr><td>
keyAvailable

</td><td>
WildCard

</td><td>
wird personalisiert

</td></tr><tr><td>
listAlgorithmIdentifier

</td><td>
signECDSA

</td><td>
</td></tr><tr><td>
accessRuleSessionkeys

</td><td>
irrelevant

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
PSO COMPUTE DIGITAL SIGNATURE

</td><td>
PWD(PIN.SMC)

</td><td>
</td></tr><tr><td>
GENERATE ASYMMETRIC KEY PAIR  
P1=‘81’

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
NEVER

</td><td>
</td></tr></table>

**[\<=]**

**A_19341 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von MF / DF.ESIGN / PrK.HCI.OSIG.E256**

PrK.HCI.OSIG.E256 MUSS die in der folgenden Tabelle dargestellten Zugriffsregeln
für die kontaktlose Schnittstelle besitzen.

Tabelle83: Zugriffsregeln für die kontaktlose Schnittstelle von MF / DF.ESIGN /
PrK.HCI.OSIG.E256

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
GENERATE ASYMMETRIC KEY PAIR, P1 = '81'

</td><td>
AUT_PACE OR AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5 und 1.5.1

</td></tr><tr><td>
PSO COMPUTE DIGITAL SIGNATURE

</td><td>
AUT_PACE AND PWD(PIN.SMC)

</td><td>
siehe Kapitel 1.5.1

</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
NEVER

</td><td>
</td></tr></table>

**[\<=]**

**Card-G2-A_3659 - K_Personalisierung: Personalisierte Attribute von MF /
DF.ESIGN / PrK.HCI.OSIG.E256**

Bei der Personalisierung von PrK.HCI.OSIG.E256 MÜSSEN die in
Tab_SMC-B_ObjSys_127 angegebenen Attribute mit den dort angegebenen Inhalten
personalisiert werden.

Tabelle84: Tab_SMC-B_ObjSys_127 Personalisierte Attribute von MF / DF.ESIGN /
PrK.HCI.OSIG.E256

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
keyAvailable

</td><td>
true

</td><td>


</td></tr><tr><td>
privateElcKey

</td><td>
keyData = Wildcard

</td><td>
</td></tr></table>

**[\<=]**

### 5.4.2.11 MF / DF.ESIGN / PrK.HCI.AUT.E256

PrK.HCI.AUT.E256 ist der private Schlüssel für die Kryptographie mit
elliptischen Kurven für Client/Server-Authentisierung. Der zugehörige
öffentliche Schlüssel PuK.HCI.AUT.E256 ist in C.HCI.AUT.E256 (siehe Kapitel
5.5.2.8) enthalten.

**Card-G2-A_3660-02 - K_Initialisierung: Initialisierte Attribute von MF /
DF.ESIGN / PrK.HCI.AUT.E256**

PrK.HCI.AUT.E256 MUSS die in Tab_SMC-B_ObjSys_128 dargestellten initialisierten
Attribute besitzen.

Tabelle 70: Tab_SMC-B_ObjSys_128 Initialisierte Attribute von MF / DF.ESIGN /
PrK.HCI.AUT.E256

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
privates Schlüsselobjekt, ELC 256

</td><td>
</td></tr><tr><td>
keyIdentifier

</td><td>
‘06’ = 6

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td>
privateElcKey

</td><td>
domainparameter = brainpoolP256r1

</td><td>
</td></tr><tr><td>
privateElcKey

</td><td>
keyData = AttributNotSet

</td><td>
wird personalisiert

</td></tr><tr><td>
keyAvailable

</td><td>
WildCard

</td><td>
wird personalisiert

</td></tr><tr><td>
listAlgorithmIdentifier

</td><td>
signECDSA

</td><td>
</td></tr><tr><td>
accessRuleSessionkeys

</td><td>
irrelevant

</td><td>
</td></tr><tr><td colspan="3">
Kontaktbehaftete Zugriffsregel für logischen LCS „Operational state
(activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
GENERATE ASYMMETRIC KEY PAIR  
P1=‘81’

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
PSO Compute Digital Signature

</td><td>
PWD(PIN.SMC)

</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr></table>

**[\<=]**

**A_19342-01 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von MF / DF.ESIGN / PrK.HCI.AUT.E256**

PrK.HCI.AUT.E256 MUSS die in der folgenden Tabelle dargestellten Zugriffsregeln
für die kontaktlose Schnittstelle besitzen.

Tabelle85: Zugriffsregeln für die kontaktlose Schnittstelle von MF / DF.ESIGN /
PrK.HCI.AUT.E256

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
GENERATE ASYMMETRIC KEY PAIR, P1 = '81'

</td><td>
AUT_PACE OR AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5 und 1.5.1

</td></tr><tr><td>
PSO Compute Digital Signature

</td><td>
AUT_PACE AND PWD(PIN.SMC)

</td><td>
siehe Kapitel 1.5.1

</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr></table>

**[\<=]**

**Card-G2-A_3661 - K_Personalisierung: Personalisierte Attribute von MF /
DF.ESIGN / PrK.HCI.AUT.E256**

Bei der Personalisierung von PrK.HCI.AUT.E256 MÜSSEN die in
Tab_SMC-B_ObjSys_129 angegebenen Attribute mit den dort angegebenen Inhalten
personalisiert werden.

Tabelle 71: Tab_SMC-B_ObjSys_129 Personalisierte Attribute von MF / DF.ESIGN /
PrK.HCI.AUT.E256

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
keyAvailable

</td><td>
true

</td><td>
</td></tr><tr><td>
privateElcKey

</td><td>
keyData = Wildcard

</td><td>
</td></tr></table>

**[\<=]**

### 5.4.2.12 MF / DF.ESIGN / PrK.HCI.ENC.E256

PrK.HCI.ENC.E256 ist der private Schlüssel für die Kryptographie mit
ellptischen Kurven für das Entschlüsseln von
Dokumenten-Chiffrierungsschlüsseln. Der zugehörige öffentliche Schlüssel
PuK.HCI.ENC.E256 ist in C.HCI.ENC.E256 (siehe Kapitel 5.5.2.9) enthalten.

**Card-G2-A_3662-02 - K_Initialisierung: Initialisierte Attribute von MF /
DF.ESIGN / PrK.HCI.ENC.E256**

PrK.HCI.ENC.E256 MUSS die in Tab_SMC-B_ObjSys_139 dargestellten initialisierten
Attribute besitzen.

Tabelle 72: Tab_SMC-B_ObjSys_130 Initialisierte Attribute von MF / DF.ESIGN /
PrK.HCI.ENC.E256

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
Objekttyp

</td><td>
privates Schlüsselobjekt, ELC 256

</td><td>
</td></tr><tr><td>
keyIdentifier

</td><td>
‘05’ = 5

</td><td>
</td></tr><tr><td>
lifeCycleStatus

</td><td>
„Operational state (activated)“

</td><td>
</td></tr><tr><td>
privateElcKey

</td><td>
domainparameter = brainpoolP256r1

</td><td>
</td></tr><tr><td>
privateElcKey

</td><td>
keyData = AttributNotSet

</td><td>
wird personalisiert

</td></tr><tr><td>
keyAvailable

</td><td>
WildCard

</td><td>
wird personalisiert

</td></tr><tr><td>
listAlgorithmIdentifier

</td><td>
elcSharedSecretCalculation

</td><td>
</td></tr><tr><td>
accessRuleSessionkeys

</td><td>
irrelevant

</td><td>
</td></tr><tr><td colspan="3">
Kontaktbehaftete Zugriffsregel für logischen LCS „Operational state
(activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
PSO Decipher  
PSO Transcipher

</td><td>
PWD(PIN.SMC)

</td><td>
</td></tr><tr><td>
GENERATE ASYMMETRIC KEY PAIR  
P1=‘81’

</td><td>
ALWAYS

</td><td>
</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr></table>

**[\<=]**

**A_19343 - (SMC-B CL) K_Initialisierung: Zugriffsregeln der kontaktlosen
Schnittstelle von MF / DF.ESIGN / PrK.HCI.ENC.E256**

PrK.HCI.ENC.E256 MUSS die in der folgenden Tabelle dargestellten Zugriffsregeln
für die kontaktlose Schnittstelle besitzen.

Tabelle86: Zugriffsregeln für die kontaktlose Schnittstelle von MF / DF.ESIGN
/  PrK.HCI.ENC.E256

<table><tr><th colspan="2">
Zugriffsregeln der kontaktlosen Schnittstelle

</th><th>
Bemerkung

</th></tr><tr><td colspan="2">
Zugriffsregel für logischen LCS „Operational state (activated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
GENERATE ASYMMETRIC KEY PAIR, P1 = '81'

</td><td>
AUT_PACE OR AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5 und 1.5.1

</td></tr><tr><td>
PSO DECIPHER

</td><td>
AUT_PACE AND PWD(PIN.SMC)

</td><td>
siehe Kapitel 1.5.1

</td></tr><tr><td>
PSO TRANSCIPHER

</td><td>
AUT_PACE AND PWD(PIN.SMC)

</td><td>
siehe Kapitel 1.5.1

</td></tr><tr><td>
DELETE

</td><td>
AUT_CMS OR AUT_CUP

</td><td>
siehe Kapitel 5.5

</td></tr><tr><td>
andere

</td><td>
NEVER

</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Operational state (deactivated)”

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
herstellerspezifisch

</td><td>
</td></tr><tr><td colspan="3">
Zugriffsregel für logischen LCS „Termination state“

</td></tr><tr><td>
Zugriffsart

</td><td>
Zugriffsbedingung

</td><td>
</td></tr><tr><td>
alle

</td><td>
NEVER

</td><td>
</td></tr></table>

**[\<=]**

**Card-G2-A_3663 - K_Personalisierung: Personalisierte Attribute von MF /
DF.ESIGN / PrK.HCI.ENC.E256**

Bei der Personalisierung von PrK.HCI.ENC.E256 MÜSSEN die in
Tab_SMC-B_ObjSys_131 angegebenen Attribute mit den dort angegebenen Inhalten
personalisiert werden.

Tabelle 73: Tab_SMC-B_ObjSys_131 Personalisierte Attribute von MF / DF.ESIGN /
PrK.HCI.ENC.E256

<table><tr><th>
Attribute

</th><th>
Wert

</th><th>
Bemerkung

</th></tr><tr><td>
keyAvailable

</td><td>
true

</td><td>
</td></tr><tr><td>
privateElcKey

</td><td>
keyData = Wildcard

</td><td>
</td></tr></table>

**[\<=]**

### 5.5 Laden neuer Anwendungen, Anlegen von EFs und Laden von Zertifikaten nach Ausgabe der SMC-B

Es wird angenommen, dass das Laden neuer Anwendungen oder das Erstellen neuer
EFs auf MF-Ebene (einschließlich Aktualisieren der Dateien EF.DIR und
EF.Version2) oder das Nachladen von Zertifikaten oder das Generieren und
Sperren von Schlüsseln nach der Ausgabe der SMC-B von einem Card Management
System (CMS) durchgeführt wird. Dies ist ein optionaler Prozess.

Es wird angenommen, dass das Laden von Zertifikaten zum Austausch vorhandener
Zertifikate (beispielsweise zur Verlängerung der Laufzeit) von einem
Certificate Update Service (CUpS) durchgeführt wird. Dieses ist ein optionaler
Prozess.

Ebenso sind das CMS oder CUpS optional. Die Inhalte des Kapitels 14.2.5 in
[gemSpec_COS] sind allerdings normativ, wenn das Laden neuer Anwendungen oder
das Erstellen neuer EFs nach Ausgabe der SMC-B durchgeführt werden müssen.

### 6 Anhang A – Verzeichnisse

### 6.1 Abkürzungen

<table><tr><th>
Kürzel

</th><th>
Erläuterung

</th></tr><tr><td>
AES

</td><td>
Advanced Encryption Standard

</td></tr><tr><td>
AID

</td><td>
Application Identifier (Anwendungskennung)

</td></tr><tr><td>
APDU

</td><td>
Application Protocol Data Unit [ISO7816-3][ISO7816-3]

</td></tr><tr><td>
ATR

</td><td>
Answer-to-Reset

</td></tr><tr><td>
AUT

</td><td>
Authentisierung

</td></tr><tr><td>
AUTD

</td><td>
CV-basierte Geräteauthentisierung

</td></tr><tr><td>
AUTR

</td><td>
CV-basierte Rollenauthentisierung

</td></tr><tr><td>
C

</td><td>
Zertifikat

</td></tr><tr><td>
CA

</td><td>
Certification Authority (Zertifizierungsdiensteanbieter)

</td></tr><tr><td>
CMS

</td><td>
Card Management System

</td></tr><tr><td>
CH

</td><td>
Cardholder (Karteninhaber)

</td></tr><tr><td rowspan="2">
CHAT

</td><td>
Certificate Holder Autorisation Template

</td></tr><tr><td>
Liste von Rechten, die ein Zertifikatsinhaber besitzt

</td></tr><tr><td>
COS

</td><td>
Card Operating System (Chipkartenbetriebssystem)

</td></tr><tr><td>
CUP, CUpS

</td><td>
Certificate Update, Certificate Update Service

</td></tr><tr><td>
CV

</td><td>
Card Verifiable

</td></tr><tr><td>
CVC

</td><td>
Card Verifiable Certificate

</td></tr><tr><td>
DIR

</td><td>
Directory

</td></tr><tr><td>
DF

</td><td>
Dedicated File

</td></tr><tr><td>
ECDSA

</td><td>
Elliptic Curve Digital Signature Algorithm

</td></tr><tr><td>
EF

</td><td>
Elementary File

</td></tr><tr><td>
eGK

</td><td>
elektronische Gesundheitskarte

</td></tr><tr><td>
ELC

</td><td>
Elliptic Curve Cryptography, Kryptographie mittels elliptischer Kurven

</td></tr><tr><td>
ENC

</td><td>
Encryption

</td></tr><tr><td>
FI

</td><td>
Clock rate conversion factor

</td></tr><tr><td>
FID

</td><td>
File Identifier

</td></tr><tr><td>
GDO

</td><td>
Global Data Object

</td></tr><tr><td>
HB

</td><td>
Historical Bytes

</td></tr><tr><td>
HCI

</td><td>
Health Care Institution (Institution des Gesundheitswesens)

</td></tr><tr><td>
ICC

</td><td>
Integrated Circuit Card (Chipkarte)

</td></tr><tr><td>
ICCSN

</td><td>
ICC Serial Number (Chipkarten-Seriennummer)

</td></tr><tr><td>
ID

</td><td>
Identifier

</td></tr><tr><td>
KeyRef

</td><td>
Key Reference

</td></tr><tr><td>
LCS

</td><td>
Life Cycle Status

</td></tr><tr><td>
MAC

</td><td>
Message Authentication Code

</td></tr><tr><td>
MF

</td><td>
Master File

</td></tr><tr><td>
OID

</td><td>
Object Identifier

</td></tr><tr><td>
OSIG

</td><td>
Organisationssignatur

</td></tr><tr><td>
PIN  

</td><td>
Personal Identification Number

</td></tr><tr><td>
PK, PuK

</td><td>
Public Key

</td></tr><tr><td>
PrK

</td><td>
Private Key

</td></tr><tr><td>
PSO

</td><td>
Perform Security Operation

</td></tr><tr><td>
PUK

</td><td>
Personal Unblocking Key (Resetting Code)

</td></tr><tr><td>
P1

</td><td>
Parameter P1 einer Kommando-APDU

</td></tr><tr><td>
P2

</td><td>
Parameter P2 einer Kommando-APDU

</td></tr><tr><td>
RC

</td><td>
Retry Counter (Fehlbedienungszähler)

</td></tr><tr><td>
RCA

</td><td>
Root CA

</td></tr><tr><td>
RPE

</td><td>
Remote PIN-Empfänger

</td></tr><tr><td>
RPS

</td><td>
Remote PIN-Sender

</td></tr><tr><td>
RSA

</td><td>
Algorithmus von Rivest, Shamir, Adleman [RSA][RSA]

</td></tr><tr><td>
SE

</td><td>
Security Environment (Sicherheitsumgebung)

</td></tr><tr><td>
SK

</td><td>
Secret Key

</td></tr><tr><td>
SM

</td><td>
Secure Messaging

</td></tr><tr><td>
SMC

</td><td>
Security Module Card

</td></tr></table>

### 6.2 Glossar

Das Glossar der Telematikinfrastruktur wird als eigenständiges Dokument zur
Verfügung gestellt.

### 6.3 Abbildungsverzeichnis

- [Abbildung-1] - Abb_SMC-B_ObjSys_001 Allgemeine Struktur der SMC-B
- [Abbildung-2] - (Abb_SMC-B_ObjSys_003) Arten der digitalen Signatur
- [Abbildung-3] - (Abb_SMC-B_ObjSys_004) Allgemeine Struktur von MF / DF.ESIGN

### 6.4 Tabellenverzeichnis

- [Tabelle-1] -  Tab_SMC-B_ObjSys_001 Liste der Komponenten, an welche dieses Dokument Anforderungen stellt
- [Tabelle-2] - Tab_SMC-B_ObjSys_117 ATR-Kodierung (Sequenz von oben nach unten)
- [Tabelle-3] - Tab_SMC-B_ObjSys_002 Initialisierte Attribute von MF
- [Tabelle-4] -  Zugriffsregeln für die kontaktlose Schnittstelle von MF
- [Tabelle-5] - Tab_SMC-B_ObjSys_003 Initialisierte Attribute von MF / EF.ATR
- [Tabelle-6] - Zugriffsregeln für die kontaktlose Schnittstelle von EF.ATR
- [Tabelle-7] - Tab_SMC-B_ObjSys_005 Initialisierte Attribute von MF / EF.DIR
- [Tabelle-8] - Zugriffsregeln für die kontaktlose Schnittstelle von EF.DIR
- [Tabelle-9] - Initialisierte  Attribute von MF / EF.CardAccess
- [Tabelle-10] - Tab_SMC-B_ObjSys_006 Initialisierte Attribute von MF / EF.GDO
- [Tabelle-11] - Zugriffsregeln für die kontaktlose Schnittstelle von EF.GDO
- [Tabelle-12] - Tab_SMC-B_ObjSys_107 Personalisierte Attribute von MF / EF.GDO
- [Tabelle-13] - Tab_SMC-B_ObjSys_007 Initialisierte Attribute von MF / EF.Version2
- [Tabelle-14] - Zugriffsregeln für die kontaktlose Schnittstelle von MF / EF.Version2
- [Tabelle-15] - Tab_SMC-B_ObjSys_009 Initialisierte Attribute MF / EF.C.CA_SMC.CS.E256
- [Tabelle-16] - Zugriffsregeln für die kontaktlose Schnittstelle von MF / EF.C.CA_SMC.CS.E256
- [Tabelle-17] - Tab_SMC-B_ObjSys_069 Personalisierte Attribute von MF / EF.C.CA_SMC.CS.E256
- [Tabelle-18] - (Tab_SMC-B_ObjSys_012) Initialisierte Attribute von MF / EF.C.SMC.AUTR_CVC.E256
- [Tabelle-19] - Zugriffsregeln für die kontaktlose Schnittstelle von EF.C.SMC.AUTR_CVC.E256
- [Tabelle-20] - Tab_SMC-B_ObjSys_072 Personalisierte Attribute von MF / EF.C.SMC.AUTR_CVC.E256
- [Tabelle-21] - (Tab_SMC-B_ObjSys_018) Initialisierte Attribute von MF / EF.C.SMC.AUTD_RPE_CVC.E256
- [Tabelle-22] - Zugriffsregeln für die kontaktlose Schnittstelle von MF / EF.C.SMC.AUTD_RPE_CVC.E256
- [Tabelle-23] - Tab_SMC-B_ObjSys_074 Personalisierte Attribute von MF / EF.C.SMC.AUTD_RPE_CVC.E256
- [Tabelle-24] - Tab_SMC-B_ObjSys_020 Initialisierte Attribute von MF / PIN.SMC
- [Tabelle-25] - Zugriffsregeln für die kontaktlose Schnittstelle von MF / PIN.SMC
- [Tabelle-26] - Tab_SMC-B_ObjSys_076 Personalisierte Attribute von MF / PIN.SMC
- [Tabelle-27] - Tab_SMC-B_ObjSys_022 Initialisierte Attribute von MF / PrK.SMC.AUTR_CVC.E256
- [Tabelle-28] - Zugriffsregeln für die kontaktlose Schnittstelle von MF / PrK.SMC.AUTR_CVC.E256
- [Tabelle-29] - Tab_SMC-B_ObjSys_078 Personalisierte Attribute von MF / PrK.SMC.AUTR_CVC.E256
- [Tabelle-30] - Tab_SMC-B_ObjSys_028 Initialisierte Attribute von MF / PrK.SMC.AUTD_RPE_CVC.E256
- [Tabelle-31] - Zugriffsregeln für die kontaktlose Schnittstelle von MF / PrK.SMC.AUTD_RPE_CVC.E256
- [Tabelle-32] - Tab_SMC-B_ObjSys_080 Personalisierte Attribute von MF / PrK.SMC.AUTD_RPE_CVC.E256
- [Tabelle-33] - Tab_SMC-B_ObjSys_031 Initialisierte Attribute von MF / PuK.RCA.CS.E256
- [Tabelle-34] - Zugriffsregeln für die kontaktlose Schnittstelle von MF / PuK.RCA.CS.E256
- [Tabelle-35] - Tab_SMC-B_ObjSys_119 Personalisierte Attribute von MF / PuK.RCA.CS.E256 für Testkarten
- [Tabelle-36] - Tab_SMC-B_ObjSys_063 Initialisierte Attribute von MF / PuK.RCA.ADMINCMS.CS.E256
- [Tabelle-37] - Zugriffsregeln für die kontaktlose Schnittstelle von MF / PuK.RCA.ADMINCMS.CS.E256
- [Tabelle-38] - Tab_SMC-B_ObjSys_083 Personalisierte Attribute von MF / PuK.RCA.ADMINCMS.CS.E256
- [Tabelle-39] - Tab_SMC-B_ObjSys_033 Initialisierte Attribute von MF / SK.CMS.AES128
- [Tabelle-40] - Zugriffsregeln für die kontaktlose Schnittstelle von MF / SK.CMS.AES128
- [Tabelle-41] - Tab_SMC-B_ObjSys_086 Personalisierte Attribute von MF / SK.CMS.AES128
- [Tabelle-42] - Tab_SMC-B_ObjSys_034 Initialisierte Attribute von MF / SK.CMS.AES256
- [Tabelle-43] - Zugriffsregeln für die kontaktlose Schnittstelle von MF / SK.CMS.AES256
- [Tabelle-44] - Tab_SMC-B_ObjSys_087 Personalisierte Attribute von MF / SK.CMS.AES256
- [Tabelle-45] - Tab_SMC-B_ObjSys_113 Initialisierte Attribute von MF / SK.CUP.AES128
- [Tabelle-46] - Zugriffsregeln für die kontaktlose Schnittstelle von MF / SK.CUP.AES128
- [Tabelle-47] - Tab_SMC-B_ObjSys_114 Personalisierte Attribute von MF / SK.CUP.AES128
- [Tabelle-48] - Tab_SMC-B_ObjSys_115 Initialisierte Attribute von MF / SK.CUP.AES256
- [Tabelle-49] - Zugriffsregeln für die kontaktlose Schnittstelle von MF / SK.CUP.AES256
- [Tabelle-50] - Tab_SMC-B_ObjSys_116 Personalisierte Attribute von MF / SK.CUP.AES256
- [Tabelle-51] - Initialisierte Attribute von MF / SK.CAN
- [Tabelle-52] - Personalisierte Attribute von MF / SK.CAN
- [Tabelle-53] - Tab_SMC-B_ObjSys_040 Initialisierte Attribute von MF / DF.ESIGN
- [Tabelle-54] - Zugriffsregeln für die kontaktlose Schnittstelle von MF / DF.ESIGN
- [Tabelle-55] - Tab_SMC-B_ObjSys_041 Initialisierte Attribute von MF / DF.ESIGN / EF.C.HCI.OSIG.R2048
- [Tabelle-56] - Zugriffsregeln für die kontaktlose Schnittstelle von MF / DF.ESIGN / EF.C.HCI.OSIG.R2048
- [Tabelle-57] - Tab_SMC-B_ObjSys_092 Personalisierte Attribute von MF / DF.ESIGN / EF.C.HCI.OSIG.R2048
- [Tabelle-58] - Tab_SMC-B_ObjSys_042 Initialisierte Attribute von MF / DF.ESIGN / EF.C.HCI.AUT.R2048
- [Tabelle-59] - Zugriffsregeln für die kontaktlose Schnittstelle von MF / DF.ESIGN / EF.C.HCI.AUT.R2048
- [Tabelle-60] - Tab_SMC-B_ObjSys_094 Personalisierte Attribute von MF / DF.ESIGN / EF.C.HCI.AUT.R2048
- [Tabelle-61] - Tab_SMC-B_ObjSys_043 Initialisierte Attribute von MF / DF.ESIGN / EF.C.HCI.ENC.R2048
- [Tabelle-62] - Zugriffsregeln für die kontaktlose Schnittstelle von MF / DF.ESIGN / EF.C.HCI.ENC.R2048
- [Tabelle-63] - Tab_SMC-B_ObjSys_096 Personalisierte Attribute von MF / DF.ESIGN / EF.C.HCI.ENC.R2048
- [Tabelle-64] - Tab_SMC-B_ObjSys_044 Initialisierte Attribute von MF / DF.ESIGN / PrK.HCI.OSIG.R2048
- [Tabelle-65] - Zugriffsregeln für die kontaktlose Schnittstelle von MF / DF.ESIGN / PrK.HCI.OSIG.R2048
- [Tabelle-66] - Tab_SMC-B_ObjSys_100 Personalisierte Attribute von MF / DF.ESIGN / PrK.HCI.OSIG.R2048
- [Tabelle-67] - Tab_SMC-B_ObjSys_047 Initialisierte Attribute von MF / DF.ESIGN / PrK.HCI.AUT.R2048
- [Tabelle-68] - Zugriffsregeln für die kontaktlose Schnittstelle von MF / DF.ESIGN / PrK.HCI.AUT.R2048
- [belle-69] - Tab_SMC-B_ObjSys_103 Personalisierte Attribute von MF / DF.ESIGN / PrK.HCI.AUT.R2048
- [Tabelle-70] - Tab_SMC-B_ObjSys_050 Initialisierte Attribute von MF / DF.ESIGN / PrK.HCI.ENC.R2048
- [Tabelle-71] - Zugriffsregeln für die kontaktlose Schnittstelle von MF / DF.ESIGN / PrK.HCI.ENC.R2048
- [Tabelle-72] - Tab_SMC-B_ObjSys_106 Personalisierte Attribute von MF / DF.ESIGN / PrK.HCI.ENC.R2048
- [Tabelle-73] - Tab_SMC-B_ObjSys_120 Initialisierte Attribute von MF / DF.ESIGN / EF.C.HCI.OSIG.E256
- [Tabelle-74] - Zugriffsregeln für die kontaktlose Schnittstelle von MF / DF.ESIGN / EF.C.HCI.OSIG.E256
- [Tabelle-75] - Tab_SMC-B_ObjSys_121 Personalisierte Attribute von MF / DF.ESIGN / EF.C.HCI.OSIG.E256
- [Tabelle-76] - Tab_SMC-B_ObjSys_122 Initialisierte Attribute von MF / DF.ESIGN / EF.C.HCI.AUT.E256
- [Tabelle-77] - Zugriffsregeln für die kontaktlose Schnittstelle von MF / DF.ESIGN / EF.C.HCI.AUT.E256
- [Tabelle-78] - Tab_SMC-B_ObjSys_123 Personalisierte Attribute von MF / DF.ESIGN / EF.C.HCI.AUT.E256
- [Tabelle-79] - Tab_SMC-B_ObjSys_124 Initialisierte Attribute von MF / DF.ESIGN/ EF.C.HCI.ENC.E256
- [Tabelle-80] - Zugriffsregeln für die kontaktlose Schnittstelle von MF / DF.ESIGN / EF.C.HCI.ENC.E256
- [Tabelle-81] - Tab_SMC-B_ObjSys_125 Personalisierte Attribute von MF / DF.ESIGN/ EF.C.HCI.ENC.E256
- [Tabelle-82] - Tab_SMC-B_ObjSys_126 Initialisierte Attribute von MF / DF.ESIGN / PrK.HCI.OSIG.E256
- [Tabelle-83] - Zugriffsregeln für die kontaktlose Schnittstelle von MF / DF.ESIGN / PrK.HCI.OSIG.E256
- [Tabelle-84] - Tab_SMC-B_ObjSys_127 Personalisierte Attribute von MF / DF.ESIGN / PrK.HCI.OSIG.E256
- [Tabelle-85] - Zugriffsregeln für die kontaktlose Schnittstelle von MF / DF.ESIGN / PrK.HCI.AUT.E256
- [Tabelle-86] - Zugriffsregeln für die kontaktlose Schnittstelle von MF / DF.ESIGN /  PrK.HCI.ENC.E256

### 6.5 Referenzierte Dokumente

### 6.5.1 Dokumente der gematik

Die nachfolgende Tabelle enthält die Bezeichnung der in dem vorliegenden
Dokument referenzierten Dokumente der gematik zur Telematikinfrastruktur.
Version und Stand der referenzierten Dokumente sind daher in der nachfolgenden
Tabelle nicht aufgeführt. Deren zu diesem Dokument jeweils gültige Versionen
sind in den von der gematik veröffentlichten Produkttypsteckbriefen enthalten,
in denen die vorliegende Version aufgeführt wird.

<table><tr><th>
[Quelle]

</th><th>
Herausgeber (Erscheinungsdatum): Titel

</th></tr><tr><td>
[gemSpec_COS]

</td><td>
gematik: Spezifikation des Card Operating System (COS)

(elektrische Schnittstelle)

</td></tr><tr><td>
[gemSpec_Karten_Fach_TIP_G2.1]

</td><td>
gematik: Befüllvorschriften für die Plattformanteile der Karten der TI der
Generation G2.1

</td></tr><tr><td>
[gemSpec_PINPUK_TI]

</td><td>
gematik: Übergreifende Spezifikation PIN/PUK-Policy für Smartcards der
Telematikinfrastruktur

</td></tr><tr><td>
[gemSpec_OID]

</td><td>
gematik: Spezifikation Festlegung von OIDs

</td></tr><tr><td>
[gemSpec_PKI]

</td><td>
gematik: Übergreifende Spezifikation Spezifikation PKI

</td></tr><tr><td>
[gemSpec_CVC_Root]

</td><td>
gematik: Spezifikation CVC - Root

</td></tr><tr><td>
[gemSpec_CVC_TSP]

</td><td>
gematik: Spezifikation Trust Service Provider CVC

</td></tr><tr><td>
[gemSpec_Krypt]

</td><td>
gematik: Verwendung kryptographischer Algorithmen in der Telematikinfrastruktur

</td></tr><tr><td>
[gemSpec_SMC_OPT]

</td><td>
gematik: Gemeinsame optische Merkmale der SMC

</td></tr></table>

### 6.5.2 Weitere Dokumente

<table><tr><th>
[Quelle]

</th><th>
Herausgeber (Erscheinungsdatum): Titel

</th></tr><tr><td>
[EN14890-1]

</td><td>
EN 14890-1: 2008  
Application Interface for smart cards used as secure
signature creation devices, Part 1: Basic services

</td></tr><tr><td>
[DIN_EN_1867]

</td><td>
EN 1867:1997  
Machine readable cards – Health care applications – Numbering
system and registration procedure for issuer identifiers

</td></tr><tr><td>
[ISO3166-1]

</td><td>
ISO/IEC 3166-1: 2006  
Codes for the representations of names of countries and
their subdivisions – Part 1: Country codes

</td></tr><tr><td>
[ISO7816-3]

</td><td>
ISO/IEC 7816-3: 2006  
Identification cards - Integrated circuit cards with
contacts -  
Part 3: Electrical interface and transmission protocols

</td></tr><tr><td>
[ISO7816-4]

</td><td>
ISO/IEC 7816-4: 2005  
Identification cards - Integrated circuit cards -  
Part
4: Organization, security and commands for interchange

</td></tr><tr><td>
[ISO8825-1]

</td><td>
ISO/IEC 8825-1: 2002  
Information technology - ASN.1 encoding rules -
Specification of Basic Encoding Rules (BER), Canonical Encoding Rules (CER) and
Distinguished Encoding Rules (DER)

</td></tr><tr><td>
[ISO14443-1]

</td><td>
ISO/IEC 14443-1: 2016-03 (3

\<sup\>rd\</sup\>

edition)

Identification cards — Contactless integrated circuit cards —

Proximity cards — Part 1: Physical characteristics

</td></tr><tr><td>
[ISO14443-2]

</td><td>
ISO/IEC 14443-2: 2016-07 (3

\<sup\>rd\</sup\>

edition)

Identification cards — Contactless integrated circuit cards —

Proximity cards — Part 2: Radio frequency power and signal interface

</td></tr><tr><td>
[ISO14443-3]

</td><td>
ISO/IEC 14443-3: 2016-06 (3

\<sup\>rd\</sup\>

edition)

Identification cards — Contactless integrated circuit cards —

Proximity cards — Part 3: Initialization and anticollision

</td></tr><tr><td>
[ISO14443-4]

</td><td>
ISO/IEC 14443-4: 2016-06 (3

\<sup\>rd\</sup\>

edition)

Identification cards — Contactless integrated circuit cards —

Proximity cards — Part 4: Transmission protocol

</td></tr><tr><td>
[PKCS#1]

</td><td>
PKCS #1 RSA Cryptography Standard  
V2.1: June 14, 2002

</td></tr><tr><td>
[Beschluss190]

</td><td>
Beschluss Nr. 190 der Europäischen Union vom 18. Juni 2003 betreffend die
technischen Merkmale der europäischen Krankenversicherungskarte

</td></tr><tr><td>
[RFC2119]

</td><td>
Network Working Group, Request for Comments: 2119, S. Bradner Harvard,
University, March 1997, Category: Best Current Practice  
Key words for use in
RFCs to Indicate Requirement Levels  
http://www.apps.ietf.org/rfc/rfc2119.html

</td></tr><tr><td>
[RSA]

</td><td>
R. Rivest, A. Shamir, L. Adleman:  
A method for obtaining digital signatures
and public key cryptosystems, Communications of the ACM, Vol. 21 No. 2, 1978

</td></tr><tr><td>
[SD5]

</td><td>
ISO/IEC JTC1/SC17 STANDING DOCUMENT 5, 2006-06-19  
Register of IC manufacturers
 
http://www.pkicc.de/cms/media/pdfs/IC_manufacturer_ISO_SD5_1962006.pdf

</td></tr></table>





[Dokumentinformationen]: #dokumentinformationen
[Inhaltsverzeichnis]:    #inhaltsverzeichnis
[1]:                     #1-einordnung-des-dokuments
[1.1]:                   #11-zielsetzung
[1.2]:                   #12-zielgruppe
[1.3]:                   #13-geltungsbereich
[1.4]:                   #14-abgrenzung-des-dokuments
[1.5]:                   #15-methodik
[1.5.1]:                 #151-nomenklatur
[1.5.2]:                 #152-verwendung-von-schüsselworten
[1.5.3]:                 #153-komponentenspezifische-anforderungen
[2]:                     #2-optionen-und-ausprägungen
[2.1]:                   #21-option_erstellung_von_testkarten
[2.2]:                   #22-ausprägung-ohne-zugriff-auf-die-egk
[2.3]:                   #23-smc-b-mit-kontaktloser-schnittstelle
[3]:                     #3-lebenszyklus-von-karte-und-applikation
[4]:                     #4-anwendungsübergreifende-festlegungen
[4.1]:                   #41-mindestanzahl-logischer-kanäle
[4.2]:                   #42-unterstützung-onboard-rsa-schlüsselgenerierung
[4.3]:                   #43-unterstützung-der-kontaktlosen-schnittstelle-smc-b-cl
[4.4]:                   #44-attributstabellen
[4.4.1]:                 #441-attribute-eines-ordners
[4.4.2]:                 #442-attribute-einer-datei-ef
[4.5]:                   #45-zugriffsregeln-für-besondere-kommandos
[4.6]:                   #46-attributswerte-und-personalisierung
[4.7]:                   #47-kartenadministration
[5]:                     #5-spezifikation-grundlegender-applikationen
[5.1]:                   #51-attribute-des-objektsystems
[5.1.1]:                 #511-atr-kodierung-und-technische-eigenschaften
[5.2]:                   #52-allgemeine-struktur
[5.3]:                   #53-root-die-wurzelapplikation-mf
[5.3.1]:                 #531-mf--efatr
[5.3.2]:                 #532-mf--efdir
[5.3.3]:                 #533-mf--efcardaccess-smc-b-cl
[5.3.4]:                 #534-mf--efgdo
[5.3.5]:                 #535-mf--efversion2
[5.3.6]:                 #536-mf--efcca_smccse256
[5.3.7]:                 #537-mf--efcsmcautr_cvce256
[5.3.8]:                 #538-mf--efcsmcautd_rpe_cvce256
[5.3.9]:                 #539-mf--pinsmc
[5.3.10]:                #5310-mf--prksmcautr_cvce256
[5.3.11]:                #5311-mf--prksmcautd_rpe_cvce256
[5.3.12]:                #5312-sicherheitsanker-zum-import-von-cv-zertifikaten
[5.3.12.1]:              #53121-mf--pukrcacse256
[5.3.13]:                #5313-asymmetrische-kartenadministration
[5.3.13.1]:              #53131-mf--pukrcaadmincmscse256
[5.3.14]:                #5314-symmetrische-kartenadministration
[5.3.14.1]:              #53141-mf--skcmsaes128
[5.3.14.2]:              #53142-mf--skcmsaes256
[5.3.14.3]:              #53143-mf--skcupaes128
[5.3.14.4]:              #53144-mf--skcupaes256
[5.3.15]:                #5315-mf--skcan-smc-b-cl
[5.4]:                   #54-die-esign-anwendung-dfesign
[5.4.1]:                 #541-dateistruktur-und-dateiinhalt
[5.4.2]:                 #542-mf--dfesign-krypto-anwendung-esign
[5.4.2.1]:               #5421-mf--dfesign--efchciosigr2048
[5.4.2.2]:               #5422-mf--dfesign--efchciautr2048
[5.4.2.3]:               #5423-mf--dfesign--efchciencr2048
[5.4.2.4]:               #5424-mf--dfesign--prkhciosigr2048
[5.4.2.5]:               #5425-mf--dfesign--prkhciautr2048
[5.4.2.6]:               #5426-mf--dfesign--prkhciencr2048
[5.4.2.7]:               #5427-mf--dfesign--efchciosige256
[5.4.2.8]:               #5428-mf--dfesign--efchciaute256
[5.4.2.9]:               #5429-mf--dfesign--efchcience256
[5.4.2.10]:              #54210-mf--dfesign--prkhciosige256
[5.4.2.11]:              #54211-mf--dfesign--prkhciaute256
[5.4.2.12]:              #54212-mf--dfesign--prkhcience256
[5.5]:                   #55-laden-neuer-anwendungen-anlegen-von-efs-und-laden-von-zertifikaten-nach-ausgabe-der-smc-b
[6]:                     #6-anhang-a-–-verzeichnisse
[6.1]:                   #61-abkürzungen
[6.2]:                   #62-glossar
[6.3]:                   #63-abbildungsverzeichnis
[6.4]:                   #64-tabellenverzeichnis
[6.5]:                   #65-referenzierte-dokumente
[6.5.1]:                 #651-dokumente-der-gematik
[6.5.2]:                 #652-weitere-dokumente
[Abbildung-1]:           gemSpec_SMC-B_ObjSys_G2_1_V5.0.0.attachments/5775454977542934884.png
[Abbildung-2]:           gemSpec_SMC-B_ObjSys_G2_1_V5.0.0.attachments/16669126137634452873.wmf
[Abbildung-3]:           gemSpec_SMC-B_ObjSys_G2_1_V5.0.0.attachments/6034167424458225333.png
[Tbl-001]:               #Tbl-001 (&93834789585216)
[Tbl-002]:               #Tbl-002 (&93834768512112)
[Tbl-003]:               #Tbl-003 (&93834769383944)
[Tbl-004]:               #Tbl-004 (&93834793849208)
[Tabelle-1]:             #Tabelle-1 (&93834764151752)
[Tabelle-2]:             #Tabelle-2 (&93834771073704)
[Tabelle-3]:             #Tabelle-3 (&93834810846384)
[Tabelle-4]:             #Tabelle-4 (&93834767988000)
[Tabelle-5]:             #Tabelle-5 (&93834768029720)
[Tabelle-6]:             #Tabelle-6 (&93834768598360)
[Tabelle-7]:             #Tabelle-7 (&93834783648664)
[Tabelle-8]:             #Tabelle-8 (&93834768815000)
[Tabelle-9]:             #Tabelle-9 (&93834799234064)
[Tabelle-10]:            #Tabelle-10 (&93834801573408)
[Tabelle-11]:            #Tabelle-11 (&93834776383248)
[Tabelle-12]:            #Tabelle-12 (&93834776421776)
[Tabelle-13]:            #Tabelle-13 (&93834798964744)
[Tabelle-14]:            #Tabelle-14 (&93834785714344)
[Tabelle-15]:            #Tabelle-15 (&93834785760544)
[Tabelle-16]:            #Tabelle-16 (&93834777621136)
[Tabelle-17]:            #Tabelle-17 (&93834777666832)
[Tabelle-18]:            #Tabelle-18 (&93834777690856)
[Tabelle-19]:            #Tabelle-19 (&93834764461104)
[Tabelle-20]:            #Tabelle-20 (&93834783517032)
[Tabelle-21]:            #Tabelle-21 (&93834783547544)
[Tabelle-22]:            #Tabelle-22 (&93834774959512)
[Tabelle-23]:            #Tabelle-23 (&93834789617832)
[Tabelle-24]:            #Tabelle-24 (&93834789637592)
[Tabelle-25]:            #Tabelle-25 (&93834781627112)
[Tabelle-26]:            #Tabelle-26 (&93834783910600)
[Tabelle-27]:            #Tabelle-27 (&93834783940096)
[Tabelle-28]:            #Tabelle-28 (&93834778285864)
[Tabelle-29]:            #Tabelle-29 (&93834778331320)
[Tabelle-30]:            #Tabelle-30 (&93834768682768)
[Tabelle-31]:            #Tabelle-31 (&93834765267968)
[Tabelle-32]:            #Tabelle-32 (&93834765291000)
[Tabelle-33]:            #Tabelle-33 (&93834765311936)
[Tabelle-34]:            #Tabelle-34 (&93834775757624)
[Tabelle-35]:            #Tabelle-35 (&93834775799944)
[Tabelle-36]:            #Tabelle-36 (&93834800001624)
[Tabelle-37]:            #Tabelle-37 (&93834800091952)
[Tabelle-38]:            #Tabelle-38 (&93834783709016)
[Tabelle-39]:            #Tabelle-39 (&93834783791144)
[Tabelle-40]:            #Tabelle-40 (&93834785900008)
[Tabelle-41]:            #Tabelle-41 (&93834785945544)
[Tabelle-42]:            #Tabelle-42 (&93834785964560)
[Tabelle-43]:            #Tabelle-43 (&93834764250584)
[Tabelle-44]:            #Tabelle-44 (&93834804592128)
[Tabelle-45]:            #Tabelle-45 (&93834764283104)
[Tabelle-46]:            #Tabelle-46 (&93834769448728)
[Tabelle-47]:            #Tabelle-47 (&93834769494176)
[Tabelle-48]:            #Tabelle-48 (&93834769514128)
[Tabelle-49]:            #Tabelle-49 (&93834771268648)
[Tabelle-50]:            #Tabelle-50 (&93834771314128)
[Tabelle-51]:            #Tabelle-51 (&93834771334048)
[Tabelle-52]:            #Tabelle-52 (&93834795196192)
[Tabelle-53]:            #Tabelle-53 (&93834795223376)
[Tabelle-54]:            #Tabelle-54 (&93834776300856)
[Tabelle-55]:            #Tabelle-55 (&93834795243464)
[Tabelle-56]:            #Tabelle-56 (&93834795315512)
[Tabelle-57]:            #Tabelle-57 (&93834775471048)
[Tabelle-58]:            #Tabelle-58 (&93834775490240)
[Tabelle-59]:            #Tabelle-59 (&93834775561528)
[Tabelle-60]:            #Tabelle-60 (&93834775611040)
[Tabelle-61]:            #Tabelle-61 (&93834775630104)
[Tabelle-62]:            #Tabelle-62 (&93834781330400)
[Tabelle-63]:            #Tabelle-63 (&93834781428968)
[Tabelle-64]:            #Tabelle-64 (&93834781448216)
[Tabelle-65]:            #Tabelle-65 (&93834791293552)
[Tabelle-66]:            #Tabelle-66 (&93834791339664)
[Tabelle-67]:            #Tabelle-67 (&93834791359376)
[Tabelle-68]:            #Tabelle-68 (&93834793920016)
[belle-69]:              #belle-69 (&93834793965352)
[Tabelle-70]:            #Tabelle-70 (&93834793985176)
[Tabelle-71]:            #Tabelle-71 (&93834794071504)
[Tabelle-72]:            #Tabelle-72 (&93834794120720)
[Tabelle-73]:            #Tabelle-73 (&93834794138528)
[Tabelle-74]:            #Tabelle-74 (&93834775166320)
[Tabelle-75]:            #Tabelle-75 (&93834775215512)
[Tabelle-76]:            #Tabelle-76 (&93834775234976)
[Tabelle-77]:            #Tabelle-77 (&93834775304984)
[Tabelle-78]:            #Tabelle-78 (&93834768123144)
[Tabelle-79]:            #Tabelle-79 (&93834768142560)
[Tabelle-80]:            #Tabelle-80 (&93834768263728)
[Tabelle-81]:            #Tabelle-81 (&93834768313296)
[Tabelle-82]:            #Tabelle-82 (&93834768332664)
[Tabelle-83]:            #Tabelle-83 (&93834785428656)
[Tabelle-84]:            #Tabelle-84 (&93834785474464)
[Tbl-089]:               #Tbl-089 (&93834785492168)
[Tabelle-85]:            #Tabelle-85 (&93834785607232)
[Tbl-091]:               #Tbl-091 (&93834785630872)
[Tbl-092]:               #Tbl-092 (&93834785650376)
[Tabelle-86]:            #Tabelle-86 (&93834775954192)
[Tbl-094]:               #Tbl-094 (&93834776002272)
[Tbl-095]:               #Tbl-095 (&93834776071440)
[Tbl-096]:               #Tbl-096 (&93834764571504)
[Tbl-097]:               #Tbl-097 (&93834764653448)
