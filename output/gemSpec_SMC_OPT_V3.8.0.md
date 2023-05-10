
Elektronische Gesundheitskarte und Telematikinfrastruktur

### Gemeinsame optische<br>Merkmale der SMC

- Klassifizierung: öffentlich
- Referenzierung: gemSpec_SMC_OPT
- Revision: 591017
- Stand: 30.06.2020
- Status: freigegeben
- Version: 3.8.0

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
22.08.08

</td><td>
</td><td>
freigegeben  
Die Version 1.0.0 wurde im Rahmen der Testmaßnahmen zu Rel. 2.3.4
erstellt.

</td><td>
gematik

</td></tr><tr><td>
3.0.0

</td><td>
19.09.12

</td><td>
</td><td>
freigegeben

</td><td>
gematik

</td></tr><tr><td>
3.0.1

</td><td>
28.11.13

</td><td>
</td><td>
Einfügen Kapitel 2.4.4 mit AFO zu elektrophysikalischen Eigenschaften

</td><td>
gematik

</td></tr><tr><td>
23.01.14

</td><td>
Ergänzungen zu elektro-physikalischen Eigenschaften

</td><td>
gematik

</td></tr><tr><td>
3.2.0

</td><td>
21.02.14

</td><td>
</td><td>
freigegeben

</td><td>
gematik

</td></tr><tr><td>
3.2.1

</td><td>
06.05.14

</td><td>
</td><td>
Streichen der Vorgabe für die Bedruckung der Rückseite

</td><td>
gematik

</td></tr><tr><td>
3.3.0

</td><td>
06.06.14

</td><td>
</td><td>
Einarbeitung Änderungen Iteration 3

</td><td>
gematik

</td></tr><tr><td>
3.4.0

</td><td>
16.10.16

</td><td>
</td><td>
Aufnahme SMC-B für Organisationen der Gesellschafter, Anpassungen gemäß
Änderungsliste

</td><td>
gematik

</td></tr><tr><td>
3.5.0

</td><td>
06.02.17

</td><td>
</td><td>
Einarbeitung gemäß Änderungsliste

</td><td>
gematik

</td></tr><tr><td>
3.6.0

</td><td>
18.12.18

</td><td>
</td><td>
freigegeben

</td><td>
gematik

</td></tr><tr><td>
3.7.0

</td><td>
15.05.19

</td><td>
</td><td>
freigegeben

</td><td>
gematik

</td></tr><tr><td>
3.8.0

</td><td>
30.06.20

</td><td>
Anpassungen gemäß Scope-Themen aus Systemdesign R4.0.0 

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
  - [1.4] Abgrenzung des Dokuments
  - [1.5] Methodik
- [2] Gestaltungsmerkmale der (g)SMC der Generation 2
  - [2.1] SMC-B
    - [2.1.1] Formfaktor der SMC-B der Generation 2
    - [2.1.2] Vorderseite der SMC-B der Generation 2
  - [2.2] gSMC-K
    - [2.2.1] Vorderseite der gSMC-K der Generation 2
  - [2.3] gSMC-KT
    - [2.3.1] Formfaktor der gSMC-KT der Generation 2
    - [2.3.2] Vorderseite der gSMC-KT der Generation 2
  - [2.4] Sonstige optische Merkmale der (g)SMC
  - [2.5] Elektrophysikalische Eigenschaften der (g)SMC
- [3] Anhang A – Verzeichnisse
  - [3.1] Abkürzungen
  - [3.2] Glossar
  - [3.3] Abbildungsverzeichnis
  - [3.4] Referenzierte Dokumente
    - [3.4.1] Dokumente der gematik
    - [3.4.2] Weitere Dokumente

### 1 Einordnung des Dokumentes

### 1.1 Zielsetzung

Dieses Dokument beschreibt die gemeinsamen Merkmale bezüglich der optischen
Gestaltung von (g)SMCs, die im Rahmen der Einführung der elektronischen
Gesundheitskarte von verschiedenen Herausgebern ausgegeben werden.

Eine (g)SMC im Sinne dieses Dokumentes ist eine Chipkarte, die

 ---> UL

existiert. Sollte ein bestimmter Typ der (g)SMC gemeint sein, dann wird dieser
nachfolgend immer explizit angegeben.

### 1.2 Zielgruppe

Dieses Dokument richtet sich an Herausgeber und Produzenten von (g)SMCs.

### 1.3 Geltungsbereich

Dieses Dokument enthält normative Festlegungen zur Telematikinfrastruktur des
deutschen Gesundheitswesens für die Gestaltung der Karten der Generation 2.
Der Gültigkeitszeitraum der vorliegenden Version und deren Anwendung in
Zulassungsverfahren werden durch die gematik GmbH in gesonderten Dokumenten (z.
B. Dokumentenlandkarte, Produkttypsteckbrief, Leistungsbeschreibung) festgelegt
und bekannt gegeben.

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

Dieses Dokument beschreibt nur die sektorübergreifend festgelegten
Gestaltungsmerkmale. Die einzelnen Sektoren bzw. Herausgeber können weitere
Vorgaben für die übrige Gestaltung der von ihnen herausgegebenen (g)SMC
festlegen.

Ferner werden keinerlei Vorgaben über die Verfahren zur Bedruckung der (g)SMC
getroffen.

### 1.5 Methodik

Anforderungen als Ausdruck normativer Festlegungen werden durch eine eindeutige
ID sowie die dem RFC 2119 [RFC2119] entsprechenden, in Großbuchstaben
geschriebenen deutschen Schlüsselworte MUSS, DARF NICHT, SOLL, SOLL NICHT,
KANN gekennzeichnet.

Sie werden im Dokument wie folgt dargestellt:

\<AFO-ID\> - \<Titel der Afo\>Text / Beschreibung[ \<=]

Dabei umfasst die Anforderung sämtliche zwischen Afo-ID und der Textmarke [\<=]
angeführten Inhalte.

### 2 Gestaltungsmerkmale der (g)SMC der Generation 2

### 2.1 SMC-B

Die Gestaltung der SMC-B richtet sich nach dem vorgesehenen Einsatzbereich. Die
hauptsächliche Verwendung einer SMC-B ist der dauerhafte und rein
kontaktbehaftete Einsatz in einem Kartenterminal. Darüber hinaus können SMC-B
mit kontaktlosen Eigenschaften für die Verwendung mit kontaktlosen
Kartenlesern erforderlich sein.SMC-B, deren COS/Objektsystem keine kontaktlose
Schnittstelle realisiert, sind grundsätzlich im ID-1-Format mit
herausbrechbarem ID-000-Teil auszuführen.

SMC-B, deren COS/Objektsystem die Option kontaktlose Schnittstelle gemäß
Option (SMC-B CL) aus [gemSpec_SMC-B_ObjSys_G2.1] realisiert, können durch
Verwendung eines Kartenkörpers im Format ID-1 mit geeigneter Antenne für den
kontaktlosen Einsatz vorgesehen sein. Werden diese kontaktlosen Eigenschaften
niemals benötigt, kann das Format ID-1 ohne Antenne, jedoch mit
herausbrechbarem ID-000-Teil verwendet werden.

### 2.1.1 Formfaktor der SMC-B der Generation 2

**Card-G2-A_2008-01 - Formfaktor SMC-B**

Eine SMC-B, die nicht für die Verwendung der kontaktlosen Schnittstelle
vorgesehen ist, MUSS im Format ID-1mit herausbrechbarem ID-000-Teil geliefert
werden. **[\<=]**

**A_19492 - Formfaktor der SMC-B zur kontaktlosen Verwendung**

Eine SMC-B, die für die Verwendung der kontaktlosen Schnittstelle vorgesehen
ist, MUSS im ID-1-Format geliefert werden. **[\<=]**

### 2.1.2 Vorderseite der SMC-B der Generation 2

**Card-G2-A_2009-01 - Layout Vorderseite SMC-B**

Die Vorderseite einer SMC-B, die nicht für die Verwendung der kontaktlosen
Schnittstelle vorgesehen ist, MUSS das Basis-Layoutgemäß Abbildung
Abb_SMCOPT_01 verwenden.![Img-001][Img-001]

Abbildung1: Abb_SMCOPT_01 – Basis-Layout der SMC-B mit beispielhafter
Kennzeichnung zur Abfallentsorgung **[\<=]**

**A_19493 - Layout Vorderseite SMC-B zur kontaktlosen Verwendung**

Die Vorderseite einer SMC-B, die für die Verwendung der kontaktlosen
Schnittstelle vorgesehen ist, MUSS das Basis-Layoutgemäß Abbildung
Abb_SMCOPT_12 verwenden.

![Img-002][Img-002]

Abbildung2: Abb_SMCOPT_12 – Basis-Layout der SMC-B  zur kontaktlosen
Verwendung mit beispielhafter Kennzeichnung zur Abfallentsorgung **[\<=]**

Um die Beschreibung zu erleichtern, werden die Kartenregionen folgendermaßen
bezeichnet (Zahl in den roten Kreisen):

![Abbildung-3][Abbildung-3]

![Abbildung-4][Abbildung-4]

**Card-G2-A_2010 - Layout Vorderseite SMC-B, Ausweisnummer**

Auf die Vorderseite der SMC-BMUSSgemäß AbbildungAbb_SMCOPT_02, Region 1,das
Wort „Ausweisnummer“ und darüber linksbündig die Ausweisnummer
aufgedruckt werden. Die Ausweisnummer ist zehnstellig und besteht aus
denletzten zehn Ziffern der ICCSN. **[\<=]**

**Card-G2-A_2011 - Layout Vorderseite SMC-B, Gültigkeitszeitraum**

Auf die Vorderseite derSMC-BSOLLgemäß AbbildungAbb_SMCOPT_02, Region 2,das
Wort „Gültigkeitszeitraum“ und darüber linksbündig der
Gültigkeitszeitraum aufgedruckt werden.

Der Gültigkeitszeitraum ist der Gültigkeitszeitraum der X.509-Zertifikate der
SMC-B und setzt sich wie folgt zusammen:

 ---> UL

**[\<=]**

**Card-G2-A_2012 - Layout Vorderseite SMC-B, Profil**

Auf die Vorderseite der SMC-BMUSSgemäß AbbildungAbb_SMCOPT_02, Region 3,das
Wort „Profil“ und rechtsbündig darüber dieProfilbezeichnungdes
organisationsbezogenen Profils aufgedruckt werden.SMC-Bs, die keinem
Profilzugeordnet werden und damit keine Rechte zum Zugriff auf die eGK
besitzen, MÜSSEN anstelle derProfilbezeichnungden Aufdruck „-“ erhalten.

Die Profilbezeichnung ist die auf den Text „CHA.“ folgende Zeichenkette in
der Spalte Zugriffsprofil der Tabelle „Tab_PKI_254 Zugriffsprofile für eine
Rollenauthentisierung“. **[\<=]**

**Card-G2-A_2013 - Ausrichtung Text Regionen 1-3 SMC-B**

Die Angaben aus den Regionen 1 bis 3gemäß AbbildungAbb_SMCOPT_02MÜSSEN
einheitlich an einer waagerechten Linie im unteren Bereich der SMC-B
ausgerichtet werden. **[\<=]**

**Card-G2-A_2014 - Layout Vorderseite SMC-B, ID-000-Bereich**

Rechts vom Chip MÜSSEN gemäß Abbildung Abb_SMCOPT_02, Region 4, folgende
Werte rechtsbündig und um 90° nach links gedreht auf den ID-000-Bereich der
SMC-B aufgedruckt werden:

 ---> UL

 ---> UL

**[\<=]**

**Card-G2-A_2015 - Schriftgröße ID-000 SMC-B**

Für die Bedruckung des ID-000-Bereichsder Vorderseite der SMC-BMUSS
einenichtproportionale Schriftart (z.B. Courier) in einer Größe verwendet
werden, die den zur Verfügung stehenden Platz optimal ausnutzt. **[\<=]**

**A_19494 - Layout Vorderseite SMC-B, CAN**

Auf der Vorderseite der SMC-B, die für die Verwendung der kontaktlosen
Schnittstelle vorgesehen ist, MUSS gemäß AbbildungAbb_SMCOPT_13, Region 1,
das Wort "CAN" und linksbündig darüber der Wert der CAN aufgedruckt werden.
Dieser MUSS mit dem Attributcandes Objekts SK.CAN übereinstimmen.Die
Platzierung erfolgt oberhalb und linksbündig zu den Angaben zur Ausweisnummer.
**[\<=]**

**A_19963 - Layout Vorderseite SMC-B, Angabe der Generation**

Auf der Vorderseite der SMC-B, die für die Verwendung der kontaktlosen
Schnittstelle vorgesehen ist, MUSS gemäßAbbildung Abb_SMCOPT_13, Region 3,
das Wort "Generation" und rechtsbündig darüber ein "G" gefolgt von der
Generationsnummer aufgedruckt werden. **[\<=]**

Die Wahl der Schriftart, der Schriftgröße und des Schnitts für die Bedruckung
des ID-1-Bereichs der SMC-B obliegt jedem SMC-Herausgeber.

### 2.2 gSMC-K

### 2.2.1 Vorderseite der gSMC-K der Generation 2

**Card-G2-A_2017 - Layout Vorderseite gSMC-K**

Für die Vorderseite der gSMC-K der Generation 2 MUSS das Basis-Layout gemäß
Abbildung Abb_SMCOPT_03 verwendet werden:

![Abbildung-5][Abbildung-5]

Abbildung5: Abb_SMCOPT_03 – Gemeinsames Basis-Layout der gSMC-K Generation 2
mit beispielhafter Kennzeichnung zur Abfallentsorgung **[\<=]**

Um die Beschreibung zu erleichtern, werden die Kartenregionen folgendermaßen
bezeichnet (Zahl in den roten Kreisen):

![Abbildung-6][Abbildung-6]

Für die einzelnen Merkmale der gSMC-K gelten folgende Festlegungen:

**Card-G2-A_2018 - Layout Vorderseite gSMC-K, Kartennummer**

Auf die Vorderseite der gSMC-KMUSSgemäß AbbildungAbb_SMCOPT_04, Region 1,das
Wort „Kartennummer“ und darüber linksbündig die Kartennummer aufgedruckt
werden. Die Kartennummer ist zehnstellig und besteht aus den letzten zehn
Ziffern der ICCSN. **[\<=]**

Für Region 2 gibt es keine Vorgaben.

**Card-G2-A_2019 - Layout Vorderseite gSMC-K, Profilnummern**

SoferndiegSMC-K im ID-1-Format geliefert wird,DÜRFEN auf die Vorderseite des
ID-1-Formats der gSMC-KProfilnummern NICHT aufgedruckt werden. **[\<=]**

**Card-G2-A_2020 - Layout Vorderseite gSMC-K, ID-000-Bereich**

Rechts vom Chip MÜSSENgemäß AbbildungAbb_SMCOPT_04, Region 4,folgende Werte
rechtsbündig und um 90° nach links gedrehtauf den ID-000-Bereich der
gSMC-Kaufgedruckt werden:

 ---> UL

**[\<=]**

**Card-G2-A_2021 - Schriftgröße ID-000 gSMC-K**

Für die Bedruckung des ID-000-Bereichsder Vorderseite der SMC-K MUSS
einenichtproportionale Schriftart (z.B. Courier) in einer Größe verwendet
werden, die den zur Verfügung stehenden Platz optimal ausnutzt. **[\<=]**

Die Wahl der Schriftart, der Schriftgröße und des Schnitts für die Bedruckung
des ID-1-Bereichs der gSMC-K obliegt jedem gSMC-Herausgeber.

### 2.3 gSMC-KT

### 2.3.1 Formfaktor der gSMC-KT der Generation 2

**Card-G2-A_2022 - Formfaktor (g)SMC-KT**

Die gSMC-KT MUSS im Format ID1 mit herausbrechbarem ID-000-Teil geliefert
werden. **[\<=]**

### 2.3.2 Vorderseite der gSMC-KT der Generation 2

**Card-G2-A_2023 - Layout Vorderseite gSMC-KT**

Für die Vorderseite der gSMC-KT der Generation 2 MUSS das Basis-Layout gemäß
Abbildung Abb_SMCOPT_05 verwendet werden.![Img-007][Img-007]

Abbildung7: Abb_SMCOPT_05 – Gemeinsames Basis-Layout der gSMC-KT Generation 2
mit beispielhafter Kennzeichnung zur Abfallentsorgung **[\<=]**

Um die Beschreibung zu erleichtern, werden die Kartenregionen folgendermaßen
bezeichnet (Zahl in den roten Kreisen):

![Abbildung-8][Abbildung-8]

![Abbildung-9][Abbildung-9]

![Abbildung-10][Abbildung-10]

Für die einzelnen Merkmale der gSMC-KT gelten folgende Festlegungen:

**Card-G2-A_2024 - Layout Vorderseite gSMC-KT, Kartennummer**

Auf die Vorderseite der gSMC-KT MUSS gemäß AbbildungAbb_SMCOPT_06, Region
1,das Wort „Kartennummer“ und darüber linksbündig die Kartennummer
aufgedruckt werden. Die Kartennummer ist zehnstellig und besteht aus den
letzten zehn Ziffern der ICCSN. **[\<=]**

Für Region 2 gibt es keine Vorgaben.

**Card-G2-A_2025 - Layout Vorderseite gSMC-KT, Profilnummer**

SoferndiegSMC-KT im ID-1-Format geliefert wird,DÜRFEN auf die Vorderseite des
ID-1-Formats der gSMC-KT Profilnummern NICHT aufgedruckt werden. **[\<=]**

**Card-G2-A_3209 - Layout Vorderseite gSMC-KT der Generation G2, Hashwert des
AUT-Zertifikats**

Falls die gSMC-KT als ID1-Karte mit herausbrechbarem ID-000-Teil geliefert
wird,MUSS im freien Bereich der Vorderseite (Region 6) gemäß Abbildung
Abb_SMCOPT_09 der Hashwert (Fingerprint) des Zertifikats C.SMKT.AUT.R2048 ,
welcher gemäß [gemSpec_Krypt#GS-A_4393] gebildet wird, in einer
nichtproportionalen Schrift gut lesbar aufgedruckt werden.​​ **[\<=]**

**Card-G2-A_3239 - Bereitstellung des Hashwerts des AUT-Zertifikats der gSMC-KT
der Generation G2**

Falls die gSMC-KT als ID-000-Karte geliefert wird,MUSS der Hashwert
(Fingerprint) des Zertifikats C.SMKT.AUT.R2048, welcher gemäß
[gemSpec_Krypt#GS-A_4393] gebildet wird, in Papierform (z.B. in einem
Begleitschreiben) an den Empfänger der gSMC-KT übermittelt werden.​​ **[\<=]**

**A_16189 - Layout Vorderseite gSMC-KT Generation G2.1, Hashwerte der
AUT-Zertifikate**

Falls die gSMC-KT der Generation G2.1 als ID1-Karte mit herausbrechbarem
ID-000-Teil geliefert wird,  MUSS im freien Bereich der Vorderseite (Region
6) gemäß Abbildung Abb_SMCOPT_10 der Hashwert (Fingerprint) des Zertifikats
C.SMKT.AUT.R2048 und des Zertifikats C.SMKT.AUT.E256, welcher gemäß
[gemSpec_Krypt#GS-A_4393] gebildet wird, in einer nichtproportionalen Schrift
gut lesbar aufgedruckt werden.Die aufgedruckten Hashwerte MÜSSEN zur
Unterscheidung und Zuordnung eindeutig gekennzeichnet sein, beispielsweise
durch die Angabe der Zertifikatsnamen. **[\<=]**

**A_16190 - Bereitstellung der Hashwerte der AUT-Zertifikate der gSMC-KT der
Generation G2.1**

Falls die gSMC-KT als ID-000-Karte geliefert wird,MÜSSEN die Hashwerte
(Fingerprint) der Zertifikate C.SMKT.AUT.R2048 und C-SMKT.AUT.E256, welche
gemäß [gemSpec_Krypt#GS-A_4393] gebildet werden, in Papierform (z.B. in einem
Begleitschreiben) an den Empfänger der gSMC-KT übermittelt werden.​​ **[\<=]**

**Card-G2-A_2026 - Layout Vorderseite gSMC-KT, ID-000-Bereich**

Rechts vom Chip der SMC-KT MÜSSEN gemäß Abbildung Abb_SMCOPT_06, Region 4,
folgende Werte rechtsbündig und um 90° nach links gedreht auf den
ID-000-Bereich der gSMC-KT aufgedruckt werden:

 ---> UL

**[\<=]**

**Card-G2-A_2027 - Schriftgröße ID-000 gSMC-KT**

Für die Bedruckung des ID-000 Bereichs der Vorderseite dergSMC-KT MUSS
einenichtproportionale Schriftart (z.B. Courier) in einer Größe verwendet
werden, die den zur Verfügung stehenden Platz optimal ausnutzt. **[\<=]**

Die Wahl der Schriftart, der Schriftgröße und des Schnitts für die Bedruckung
des ID-1-Bereichs der gSMC-KT obliegt jedem gSMC-Herausgeber.

### 2.4 Sonstige optische Merkmale der (g)SMC

Zur Darstellung der Konformität der (g)SMC zu kennzeichnungspflichtigen
Richtlinien oder gesetzlichen Vorgaben, beispielsweise die Kennzeichnung
gemäß des Gesetzes über das Inverkehrbringen, die Rücknahme und die
umweltverträgliche Entsorgung von Elektro- und Elektronikgeräten [ElektroG]
oder die CE-Kennzeichnung der Europäischen Union, können geeignete
Kennzeichen (beispielsweise Symbole) auf die SMC aufgebracht werden.

Die Kennzeichnung ist Bestandteil des Aufdrucks der Kartenkörper im
ID-1-Bereich oder eines Aufdrucks auf der Rückseite des herausbrechbaren
ID-000-Teils.

![Abbildung-11][Abbildung-11]

**Card-G2-A_2031 - Sonstige optische Merkmale für die (g)SMCs**

Auf den (g)SMCs KÖNNEN zusätzliche optische Merkmale aufgedruckt werden. Die
Ausgestaltung obliegt dem jeweiligen (g)SMC-Herausgeber und ist nicht normiert. **[\<=]**

Beispiele hierfür sind:

 ---> UL

**A_16191 - Aufdruck der kennzeichnungspflichtigen Angaben**

Wenn der Kartenhersteller Kennzeichen (Symbole oder weitere Angaben) zur
Kennzeichnung der Konformität der Karte zu kennzeichnungspflichtigen
Richtlinien oder gesetzlichen Vorgaben auf den Kartenkörper aufbringen muss,
dann KANN dieses innerhalb der als Region 56 gekennzeichneten schraffierten
Fläche erfolgen.  **[\<=]**

**A_16999 - Gestaltung der kennzeichnungspflichtigen Angaben**

Wenn kennzeichnungspflichtige Angaben auf den Kartenkörper aufgebracht werden,
dann MUSS der Kartenhersteller sicherstellen, dass die jeweiligen Vorgaben zur
Kennzeichnungspflicht in Bezug auf die zu verwendenden Symbole, sowie die
Größe und Lesbarkeit der jeweiligen Kennzeichen eingehalten werden. **[\<=]**

### 2.5 Elektrophysikalische Eigenschaften der (g)SMC

**Card-G2-A_3478 - Elektrophysikalische Eigenschaften des Kartenkörpers der
(g)SMC**

Der Kartenkörper der (g)SMC MUSS konform zu [ISO 7810], [ISO_IEC 7810-1 AMD],
[ISO 7816-1], [ISO/IEC 10373-1] und [ISO/IEC 10373-1 AMD1] sein. Im Einzelnen
gelten folgende Kapitel der jeweiligen Spezifikationen:a) ISO 7810:

Alle Kapitel, die alle Kartenformate betreffen und zusätzlich alle Kapitel, die
explizit das ID-000-Format betreffen.

b) ISO_IEC 7810-1 AMD

Kapitel 9.1, 9.2, 9.3, 9.4.1, 9.5

c) ISO 7816-1

Kapitel 4.2, 4.3 und 4.4

d) ISO/IEC 10373-1

Es gelten die allgemein für alle Kartentypen gültigen Kapitel und in Kapitel 5
„Test Methods“ folgende Kapitel:

5.2 Dimensions of cards

5.3 Peel strength

5.4 Resistance to chemicals

5.5 Card dimensional stability and warpage with temperature and humidity

5.12 X-rays

5.13 Static magnetic fields

5.16 Surface distortions and raised areas

e) ISO/IEC 10373-1 AMENDMENT

Es gelten die allgemein für alle Kartentypen gültigen Kapitel, angepasst an
die Belange des ID-000-Kartentyps, und zusätzlich die folgenden Kapitel:

5.17 Dimension and Location of Contacts for ICCs with contacts (location of

        contacts as defined in Card-G2-A_xxxx instead of ISO 7816-2)

5.18 Static electricity test for ICCs with contacts

5.20 Electrical surface resistance of contacts of ICCs with contacts

5.21 Surface profile of contacts of ICCs with contacts **[\<=]**

**Card-G2-A_3513 - Bemaßung der Kontakte der (g)SMC**

Die Maße des Kartenkörpers und der Kontakte der (g)SMC MÜSSEN den Vorgaben
derAbb_SMCOPT_08entsprechen (Quelle [ETSI TS 100 977#Annex A]). **[\<=]**

![Abbildung-12][Abbildung-12]

### 3 Anhang A – Verzeichnisse

### 3.1 Abkürzungen

<table><tr><th>
Kürzel

</th><th>
Erläuterung

</th></tr><tr><td>
CMYK

</td><td>
System

zur Definition einer Farbe; CMYK steht für Cyan (Türkis), Magenta
(Fuchsinrot), Yellow (Gelb) und Key/blacK (schwarz)

</td></tr><tr><td>
CVC

</td><td>
Card Verifiable Certificate

</td></tr><tr><td>
gSMC

</td><td>
gerätebezogene Security Module Card

</td></tr><tr><td>
gSMC-K

</td><td>
gerätebezogene Security Module Card für den Konnektor

</td></tr><tr><td>
gSMC-KT

</td><td>
gerätebezogene Security Module Card für das Kartenterminal

</td></tr><tr><td>
SMC

</td><td>
Security Module Card

</td></tr><tr><td>
SMC-B

</td><td>
Security Module Card für eine Organisation des Gesundheitswesens

</td></tr><tr><td>
ZDA

</td><td>
Zertifizierungsdiensteanbieter

</td></tr></table>

### 3.2 Glossar

Das Glossar der Telematikinfrastruktur wird als eigenständiges Dokument (vgl.
[gemGlossar]) zur Verfügung gestellt.

### 3.3 Abbildungsverzeichnis

- [Abbildung-3] - Abb_SMCOPT_02 – Basis-Layout der SMC-B mit Kennzeichnung der Kartenregionen
- [Abbildung-4] -  Abb_SMCOPT_13 – Basis-Layout der SMC-B zur kontaktlosen Verwendung mit Kennzeichnung der Kartenregionen
- [Abbildung-5] - Abb_SMCOPT_03 – Gemeinsames Basis-Layout der gSMC-K Generation 2 mit beispielhafter Kennzeichnung zur Abfallentsorgung
- [Abbildung-6] - Abb_SMCOPT_04 – Gemeinsames Basis-Layout der gSMC-K Generation 2 mit Kennzeichnung der Kartenregionen
- [Abbildung-8] - Abb_SMCOPT_06 – Gemeinsames Basis-Layout der gSMC-KT Generation 2 mit Kennzeichnung der Kartenregionen
- [Abbildung-9] - Abb_SMCOPT_09 – Gemeinsames Basis-Layout der gSMC-KT Generation 2 mit beispielhafter Kennzeichnung zur Abfallentsorgung
- [Abbildung-10] - Abb_SMCOPT_10 – Gemeinsames Basis-Layout der gSMC-KT Generation G2.1 mit Hashwerten (beispielhaft)
- [Abbildung-11] - Abb_SMCOPT_11 - Druckbereich der ID-000-Rückseite zum Aufdruck kennzeichnungspflichtiger Angaben  
- [Abbildung-12] - Abb_SMCOPT_08 – Bemaßung der (g)SMC

### 3.4 Referenzierte Dokumente

### 3.4.1 Dokumente der gematik

Die nachfolgende Tabelle enthält die Bezeichnung der in dem vorliegenden
Dokument referenzierten Dokumente der gematik zur Telematikinfrastruktur. Der
mit der vorliegenden Version korrelierende Entwicklungsstand dieser Konzepte
und Spezifikationen wird pro Release in einer Dokumentenlandkarte definiert;
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
gematik: Glossar der Telematikinfrastruktur

</td></tr><tr><td>
[gemSpec_SMC-B_ObjSys]

</td><td>
gematik: Spezifikation des elektronischen Heilberufsausweises SMC-B -
Objektsystem (Generation G2.1)

</td></tr><tr><td>
[gemSpec_SMC-K_ObjSys]

</td><td>
gematik: Spezifikation der elektronischen Secure Module Card des Konnektors
(gSMC-K) - Objektsystem

</td></tr><tr><td>
[gemSpec_SMC-KT_ObjSys]

</td><td>
gematik: Spezifikation der elektronischen Secure Module Card des Kartenterminals
(gSMC-KT) - Objektsystem (Generation G2.1)

</td></tr></table>

### 3.4.2 Weitere Dokumente

<table><tr><th>
[Quelle]

</th><th>
Herausgeber (Erscheinungsdatum): Titel

</th></tr><tr><td>
[RFC2119]

</td><td>
RFC 2119 (März 1997): Key words for use in RFCs to Indicate Requirement Levels
S. Bradner,  
http://tools.ietf.org/html/rfc2109

</td></tr><tr><td>
ISO/IEC 7810

</td><td>
Identification cards -- Physical characteristics  
Third edition 2003-11-01

</td></tr><tr><td>
ISO/IEC 7810, AMENDMENT

</td><td>
Identification cards - Physical characteristics - Amendment 1: Criteria for
cards containing integrated circuits, Third edition 2003-11-01, AMENDMENT 1,
2009-12-15

</td></tr><tr><td>
ISO/IEC 7816-1

</td><td>
Physical Charcteristics of Integrated Circuit Cards  
2011

</td></tr><tr><td>
ISO/IEC 10373-1

</td><td>
Identification cards -- Test methods -- Part 1: General characteristics  
Second
edition 2006-05-01

</td></tr><tr><td>
ISO/IEC 10373-1 AMENDMENT 1

</td><td>
Identification cards - Test methods - Part 1: General characteristics; Second
edition 2006-05-01,  
Amendment 1, 2012-11-01AMD1

</td></tr><tr><td>
[ElektroG]

</td><td>
Gesetz über das Inverkehrbringen, die Rücknahme und die umweltverträgliche
Entsorgung von Elektro- und Elektronikgeräten (Elektro- und
Elektronikgerätegesetz - ElektroG), 20.10.2015

</td></tr><tr><td>
[ETSI TS 100 977]

</td><td>
Digital cellular telecommunications system (Phase 2+);  
Specification of the
Subscriber Identity Module -  
Mobile Equipment (SIM-ME) Interface  
(3GPP TS
11.11) V8.14.0 (2007-06)

</td></tr></table>





[Dokumentinformationen]: #dokumentinformationen
[Inhaltsverzeichnis]:    #inhaltsverzeichnis
[1]:                     #1-einordnung-des-dokumentes
[1.1]:                   #11-zielsetzung
[1.2]:                   #12-zielgruppe
[1.3]:                   #13-geltungsbereich
[1.4]:                   #14-abgrenzung-des-dokuments
[1.5]:                   #15-methodik
[2]:                     #2-gestaltungsmerkmale-der-gsmc-der-generation-2
[2.1]:                   #21-smc-b
[2.1.1]:                 #211-formfaktor-der-smc-b-der-generation-2
[2.1.2]:                 #212-vorderseite-der-smc-b-der-generation-2
[2.2]:                   #22-gsmc-k
[2.2.1]:                 #221-vorderseite-der-gsmc-k-der-generation-2
[2.3]:                   #23-gsmc-kt
[2.3.1]:                 #231-formfaktor-der-gsmc-kt-der-generation-2
[2.3.2]:                 #232-vorderseite-der-gsmc-kt-der-generation-2
[2.4]:                   #24-sonstige-optische-merkmale-der-gsmc
[2.5]:                   #25-elektrophysikalische-eigenschaften-der-gsmc
[3]:                     #3-anhang-a-–-verzeichnisse
[3.1]:                   #31-abkürzungen
[3.2]:                   #32-glossar
[3.3]:                   #33-abbildungsverzeichnis
[3.4]:                   #34-referenzierte-dokumente
[3.4.1]:                 #341-dokumente-der-gematik
[3.4.2]:                 #342-weitere-dokumente
[Img-001]:               gemSpec_SMC_OPT_V3.8.0.attachments/13066816828895861801.png
[Img-002]:               gemSpec_SMC_OPT_V3.8.0.attachments/18019545009382237756.png
[Abbildung-3]:           gemSpec_SMC_OPT_V3.8.0.attachments/9021124037250734740.png
[Abbildung-4]:           gemSpec_SMC_OPT_V3.8.0.attachments/10046564981150972255.png
[Abbildung-5]:           gemSpec_SMC_OPT_V3.8.0.attachments/4880816034241447709.png
[Abbildung-6]:           gemSpec_SMC_OPT_V3.8.0.attachments/5540140646352868126.jpg
[Img-007]:               gemSpec_SMC_OPT_V3.8.0.attachments/6899918646041867010.png
[Abbildung-8]:           gemSpec_SMC_OPT_V3.8.0.attachments/12237971105258056575.png
[Abbildung-9]:           gemSpec_SMC_OPT_V3.8.0.attachments/2881327315724409122.png
[Abbildung-10]:          gemSpec_SMC_OPT_V3.8.0.attachments/5441542574656025292.png
[Abbildung-11]:          gemSpec_SMC_OPT_V3.8.0.attachments/7662163933419559304.png
[Abbildung-12]:          gemSpec_SMC_OPT_V3.8.0.attachments/16258033424518333966.png
[Tbl-001]:               #Tbl-001 (&93834765174784)
[Tbl-002]:               #Tbl-002 (&93834781672840)
[Tbl-003]:               #Tbl-003 (&93834768355056)
[Tbl-004]:               #Tbl-004 (&93834768372096)
