
Elektronische Gesundheitskarte und Telematikinfrastruktur

### Übergreifende Spezifikation PIN/PUK-Policy für Smartcards der Telematikinfrastruktur

- Klassifizierung: öffentlich
- Referenzierung: gemSpec_PINPUK_TI
- Revision: 591017
- Stand: 14.05.2018
- Status: freigegeben
- Version: 1.3.0

### Dokumentinformationen

Änderungen zur Vorversion

Änderungen gemäß Änderungsliste P15.2 sind gelb markiert.

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
0.0.1

</td><td>
22.02.12

</td><td>
</td><td>
Ableitung des Dokumentes aus [gemSiko#AnhE]

</td><td>
ITS/SI

</td></tr><tr><td>
</td><td>
24.02.12

</td><td>
</td><td>
Redaktionelle Überarbeitung im Rahmen des Projektes Online-Rollout Stufe 1,
insbesondere die Umnummerierung der Anforderungsnummern entsprechend der
Vorgaben des Projektes.

Ergänzen des Anhangs A (Eingangsanforderungen) und Anhangs B
(Ausgangsanforderungen)

</td><td>
ITS/SI

</td></tr><tr><td>
0.9.0

</td><td>
27.02.12

</td><td>
</td><td>
formale QS

</td><td>
QM

</td></tr><tr><td>
0.10.0

</td><td>
20.04.12

</td><td>
Kap. 2.1,

Kap. 4

</td><td>
Ergänzung Kapitel 2.1 und Einführung von Kapitel 4.

</td><td>
ITS/SI

</td></tr><tr><td>
0.15.0

</td><td>
11.01.13

</td><td>
</td><td>
Anpassung an die Inhalte und Struktur der vergaberelevanten Dokumente

</td><td>
ITS/SI

</td></tr><tr><td>
0.19.0

</td><td>
22.04.13

</td><td>
</td><td>
Einarbeitung Gesellschafterkommentare

</td><td>
P77

</td></tr><tr><td>
1.0.0

</td><td>
06.06.13

</td><td>
</td><td>
freigegeben

</td><td>
gematik

</td></tr><tr><td>
1.1.0

</td><td>
21.02.14

</td><td>
</td><td>
Losübergreifende Synchronisation

</td><td>
P77

</td></tr><tr><td>
1.2.0

</td><td>
28.10.16

</td><td>
</td><td>
Einarbeitung lt. Änderungsliste

</td><td>
gematik

</td></tr><tr><td>
1.3.0

</td><td>
14.05.18

</td><td>
</td><td>
freigegeben

</td><td>
gematik

</td></tr><tr></tr></table>

### Inhaltsverzeichnis

- [Dokumentinformationen]
- [Inhaltsverzeichnis]
- [1] Einordnung des Dokumentes
  - [1.1] Zielsetzung
  - [1.2] Zielgruppe
  - [1.3] Geltungsbereich
  - [1.4] Abgrenzung
  - [1.5] Methodik
- [2] Mindestanforderungen und Sicherheits-Policies für die Behandlung von PIN/PUK
  - [2.1] PIN/PUK-Erzeugung
  - [2.2] PIN/PUK-Speicherung
  - [2.3] PIN/PUK-Transport
  - [2.4] PIN/PUK-Verwendung
  - [2.5] PIN -Änderung
  - [2.6] PIN/PUK-Löschung
- [3] Mindestanforderungen und Sicherheits-Policies für die Behandlung der Schlüssel zum Schutz der PIN/PUK
- [4] Anhang A – Verzeichnisse
  - [4.1] Abkürzungen
  - [4.2] Glossar
  - [4.3] Referenzierte Dokumente
    - [4.3.1] Dokumente der gematik
    - [4.3.2] Weitere Dokumente

### 1 Einordnung des Dokumentes

### 1.1 Zielsetzung

Die übergreifende PIN/PUK-Policy für Smartcards der TI gilt für den
Gesamtbereich Kartenproduktion, Kartenausgabe, Karteneinzug der eGK und der
HBA/SMC sowie für die Verwendung von deren PINs und den zugehörigen PUKs an
allen betroffenen Komponenten der Telematikinfrastruktur. Die PINs für die
qualifizierte elektronische Signatur eines HBA werden von der BNetzA geregelt
und sind nicht Gegenstand dieses Dokumentes. Falls die eGK eine qualifizierte
elektronische Signatur besitzt, so wird die PIN für diese qualifizierte
elektronische Signatur von der BNetzA geregelt und ist ebenfalls nicht
Gegenstand dieses Dokumentes.

Die Anforderungen der übergreifenden PIN/PUK-Policy für Smartcards der TI
stellen sicher, dass die PINs und zugehörige PUKs in der TI in jedem
Verarbeitungsschritt und zu jedem Zeitpunkt auf einem einheitlichen
Mindestniveau geschützt werden. Dadurch werden auch die Daten der TI auf einem
adäquaten Sicherheitsniveau geschützt, auf die nach erfolgreicher Eingabe der
PIN/PUK zugegriffen werden kann.

Durch die übergreifende PIN/PUK-Policy für Smartcards der TI wird auch
sichergestellt, dass die PIN/PUK für in der TI hinzukommende Smartcards mit
einem einheitlichen Mindestniveau geschützt werden.

### 1.2 Zielgruppe

Das Dokument richtet sich an Kartenherausgeber von eGK und HBA/SMC.
Kartenherausgeber können Dritte mit der Kartenpersonalisierung beauftragen. In
diesem Fall, in dem der Kartenherausgeber operative Aufgaben durch einen
Dritten wahrnehmen lässt, muss der beauftragte Auftragnehmer die Anforderungen
einhalten. Es bleibt jedoch in der Verantwortung des Kartenherausgebers
sicherzustellen, dass der Beauftragte die Anforderungen umsetzt. Bei der
Auswahl des Auftragnehmers ist hierauf zu achten.

### 1.3 Geltungsbereich

Dieses Dokument enthält normative Festlegungen zur Telematikinfrastruktur des
Deutschen Gesundheitswesens. Der Gültigkeitszeitraum der vorliegenden Version
und deren Anwendung in Zulassungsverfahren wird durch die gematik GmbH in
gesonderten Dokumenten (z.B. Dokumentenlandkarte, Produkttypsteckbrief,
Leistungsbeschreibung) festgelegt und bekannt gegeben.

Wichtiger Schutzrechts-/Patentrechtshinweis:

Das vorliegende Sicherheitskonzept ist von der gematik allein unter technischen
Gesichtspunkten erstellt worden. Im Einzelfall kann nicht ausgeschlossen
werden, dass die Implementierung der Spezifikation in technische Schutzrechte
Dritter eingreift. Es ist allein Sache des Anbieters oder Herstellers, durch
geeignete Maßnahmen dafür Sorge zu tragen, dass von ihm aufgrund der
Spezifikation angebotene Produkte und/oder Leistungen nicht gegen Schutzrechte
Dritter verstoßen und sich ggf. die erforderlichen Erlaubnisse/Lizenzen von
den betroffenen Schutzrechtsinhabern einzuholen. Die gematik übernimmt
insofern keinerlei Gewährleistungen

### 1.4 Abgrenzung

Das Dokument definiert Anforderungen an Produkte und Verfahren, stellt jedoch
keine Lösungsbeschreibungen dar.

### 1.5 Methodik

Für die genauere Unterscheidung zwischen normativen und informativen Inhalten
werden die dem RFC 2119 [RFC2119] entsprechenden in Großbuchstaben
geschriebenen, deutschen Schlüsselworte (MUSS, DARF NICHT, SOLL, SOLL NICHT,
KANN) verwendet.

Sie werden im Dokument wie folgt dargestellt:

\<AFO-ID\> - \<Titel der Afo\>Text / Beschreibung[ \<=]

Dabei umfasst die Anforderung sämtliche innerhalb der Textmarken angeführten
Inhalte.

### 2 Mindestanforderungen und Sicherheits-Policies für die Behandlung von PIN/PUK

Der Zugriff auf personenbezogene und medizinische Daten der
Telematikinfrastruktur (TI) ist unter anderem durch kryptographische Schlüssel
geschützt, die auf Smartcards gespeichert sind und durch die Eingabe von PINs
freigeschaltet werden. Um die Daten der TI auf einem adäquaten
Sicherheitsniveau zu schützen, sind daher auch diese PINs der Smartcards in
der TI in jedem Verarbeitungsschritt und zu jedem Zeitpunkt auf einem
einheitlichen Mindestniveau zu schützen. Diese Mindestanforderungen gelten in
gleicher Weise für PUKs, die für PIN-Änderungen bzw. für das Zurücksetzen
des Fehlbedienungszählers einer PIN benötigt werden. Die Kartenherausgeber
oder, falls der Kartenherausgeber einen Dritten mit der Kartenpersonalisierung
beauftragt, die Kartenpersonalisierer müssen bei der Auslieferung der Karten
auch für die geschützte Übermittlung der benötigten PINs und PUKs sorgen.

Dieses Kapitel beschreibt die Mindestanforderungen an die Behandlung von
PIN/PUK, damit unabhängig von der jeweils gewählten Verfahrensvariante zur
Aushändigung der PIN/PUK-Briefe und der Karten (z.B. Transport-PIN-Verfahren
oder Echt-PIN-Verfahren) ein einheitliches Sicherheitsniveau für die PIN/PUK
in der Telematikinfrastruktur gewährleistet werden kann.

**GS-A_2229 - Prozesse und Maßnahmen zur Aushändigung von Karte und
PIN/PUK-Brief**

Die Erreichung der Schutzziele Vertraulichkeit, Integrität, Authentizität,
Verfügbarkeit und Nichtabstreitbarkeit sowie die Wirksamkeit und Konsistenz
der gewählten Maßnahmen und Prozesse zur Aushändigung der PIN/PUK-Briefe
sowie der Karten MUSS vom Kartenherausgeber bewertet und gewährleistet werden. **[\<=]**

Es ist vorgesehen, dass der Karteninhaber seinen persönlichen Willen durch
Besitz (der Karte) und Wissen (der PIN) ausdrücken kann. Mit diesen PINs zur
Authentifizierung werden kryptographische Schlüssel zugänglich, die einen
Zugriff auf personenbezogene und medizinische Daten ermöglichen. Daraus
resultieren u. A. die Anforderungen:

**GS-A_2227 - Keine Kartendubletten**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS technisch
kontrollieren und zusichern, dass jede Karte mit der zugehörigen PIN/PUK nur
einmal existiert (keine Kartendubletten) und auch nur einmal an den
Karteninhaber sicher ausgegeben wird. **[\<=]**

**GS-A_2228 - Trennung von Karte und PIN/PUK-Brief**

Der Kartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der Kartenpersonalisierer MUSS
organisatorisch sicherstellen, dass Karte und PIN/PUK-Brief bis zur Übergabe
an den Karteninhaber nie gemeinsam an einer Stelle beim Kartenherausgeber bzw.
Kartenpersonalisierer vorhanden sind, z. B. durch den getrennten Versand mit
einem Mindestabstand von drei Tagen mit unterschiedlichen Rücksendeadressen.
**[\<=]**

**GS-A_5387 - Beachten von Vorgaben bei der Kartenpersonalisierung**

Der Kartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der Kartenpersonalisierer MUSS die Vorgaben
und Empfehlungen von Kartenherstellern (bspw. Personalisierungsguides) beachten
und umsetzen. **[\<=]**

In den nachfolgenden Unterkapiteln werden die für HBA, SMC und eGK mindest
einzuhaltenden Sicherheitsanforderungen und -policies über den gesamten
Lebenszyklus beschrieben. Es werden dabei die folgenden Phasen unterschieden:

 ---> UL

### 2.1 PIN/PUK-Erzeugung

Grundsätzlich sind für die PIN-Erzeugung Verfahren möglich, bei denen die
Auswahl einer PIN durch den Karteninhaber erfolgt oder bei dem die PIN dem
Karteninhaber durch den Kartenherausgeber bzw. Kartenpersonalisierer zugewiesen
wird.

**GS-A_2232 - PIN/PUK-Erzeugung: Verfahren für PIN/PUK-Auswahl**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS sicherstellen,
dass die PIN/PUK-Auswahl gemäß einer der folgenden Techniken erfolgt:

 ---> UL

Festlegungen in den Spezifikationen eines Kartentyps können die erlaubten
Verfahren weiter einschränken. **[\<=]**

**GS-A_2239 - PIN/PUK-Erzeugung: Ableitung von PIN im Sicherheitsmodul**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS die PIN/PUK in
einem Sicherheitsmodul mit geprüften Algorithmen gemäß
derMindeststandardsder gematikentsprechend [gemSpec_Krypt]erzeugen oder
ableiten, so dass sie nicht von Unbefugten ausgelesen oder manipuliert werden
können. **[\<=]**

Die Mindestanforderungen der gematik an kryptographische Algorithmen sind in
[gemSpec_Krypt] beschrieben.

Falls der Kartenherausgeber bzw. der Kartenpersonalisierer die PINs zuweist, so
können die PINs/PUKs entweder (pseudo-)zufällig erzeugt oder aus Kartendaten
abgeleitet werden.

**GS-A_2234 - PIN/PUK-Erzeugung: Zufallsgenerator für PIN/PUK**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS sicherstellen,
dass, falls die PIN/PUK zufällig oder pseudozufällig erzeugt wird, der dabei
verwendete Zufalls- oder Pseudozufallsgenerator die vorgegebenen
Mindestanforderungen der gematikentsprechend [gemSpec_Krypt]erfüllt. **[\<=]**

Die Mindestanforderungen der gematik an einen Zufalls- oder
Pseudozufallsgenerator sind in [gemSpec_Krypt] beschrieben.

**GS-A_2235 - PIN/PUK-Erzeugung: Ableitung von PIN**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS sicherstellen,
dass, falls die PIN/PUK aus Kartendaten abgeleitet wird, die abgeleitete
PIN/PUK ohne Kenntnis des benutzten Schlüssels nicht einfacher bestimmt werden
kann alseine zufällig erzeugte PIN/PUK. **[\<=]**

Der Kartenherausgeber bzw. Kartenpersonalisierer muss bei der Ableitung der PIN
also insbesondere verhindern, dass der Ableitungsprozess spezielle Werte
bevorzugt erzeugt und dass zugewiesene PIN/PUK gleich verteilt sind, um das
Erraten einer PIN/PUK zu erschweren.

**GS-A_2236 - PIN/PUK-Erzeugung: Ableitung der PIN aus eindeutig dem
Versicherten zugeordneten Daten**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS sicherstellen,
dass, falls die PIN/PUK aus Kartendaten abgeleitet wird, sie kryptographisch
von vollständigen Kartenidentifikationsdaten, die eineindeutig dem
Versicherten zugeordnet sind, abgeleitet wird. **[\<=]**

**GS-A_2237 - PIN/PUK-Erzeugung: kein Rückschluss von PIN/PUK auf Schlüssel**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS sicherstellen,
dass, falls die PIN/PUK aus Kartendaten abgeleitet wird, aus der Kenntnis der
PIN/PUK und der Inputdaten keine Informationen über den benutzten Schlüssel
desKartenherausgebersbzw.Kartenpersonalisierersabgeleitet werden können.
DerKartenherausgeberbzw.KartenpersonalisiererMUSS sicherstellen, dass die
Mindestanforderungen der gematik für die kryptographischen
Algorithmenentsprechend [gemSpec_Krypt]erfüllt werden. **[\<=]**

Die Mindestanforderungen der gematik an kryptographische Algorithmen sind in
[gemSpec_Krypt] beschrieben.

Falls die PIN vom Karteninhaber gewählt wird, ist dieser über die
Anforderungen an die PIN-Auswahl zu informieren.

**GS-A_2230 - PIN/PUK-Erzeugung: Länge PIN/PUK (Kartenherausgeber)**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS den
Karteninhaber bei einer durch den Karteninhaber selbst zu wählenden PIN, über
die Länge der PIN informieren. **[\<=]**

**GS-A_2238 - PIN/PUK-Erzeugung: Informationen an Karteninhaber bei
selbstständiger Wahl der PIN**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS, falls die PIN
durch die Karteninhaber gewählt wird, dem Karteninhaber entsprechende
AuswahlanweisungensowieWarnungen geben und dem Karteninhaber bei
derKartenausgabezusenden. **[\<=]**

### 2.2 PIN/PUK-Speicherung

Eine Speicherung von PINs/PUKs beim Herausgeber für die Nutzung im
Produktionsprozess erfolgt nur so lange, bis PIN und PUK auf die Karte und den
PIN/PUK-Brief übertragen wurden.

**GS-A_5209 - PIN/PUK-Speicherung: PIN/PUK unverzüglich löschen**

Der Kartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der Kartenpersonalisierer MUSS die PIN/PUK
einer Karte in seinen Systemen unverzüglich löschen, nachdem PIN und PUK auf
die Karte übertragen und der PIN/PUK-Brief an den Karteninhaber erstellt
wurden. **[\<=]**

Die gespeicherte PIN darf nicht abgehört oder unbemerkt manipuliert werden
können. PINs dürfen nur innerhalb von Sicherheitsmodulen (Chip, HSM) und
Sicherheitsobjekten (inkl. PIN/PUK-Briefe) im Klartext vorliegen.

**GS-A_2240 - PIN/PUK-Speicherung: Verschlüsselung der PIN außerhalb von
Sicherheitsmodulen**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS die PIN/PUK
verschlüsseln, falls die PIN/PUK außerhalb eines Sicherheitsmoduls
gespeichert wird. DerKartenherausgeberbzw.KartenpersonalisiererMUSS
sicherstellen, dass die dabei verwendeten kryptographischen Algorithmen die
aktuellen Mindestanforderungen der gematikentsprechend [gemSpec_Krypt]erfüllen. **[\<=]**

**GS-A_2242 - PIN/PUK-Speicherung: Integrität der PIN außerhalb von
Sicherheitsmodulen**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS die
Integrität der PIN/PUK schützen, falls die PIN/PUK außerhalb eines
Sicherheitsmoduls gespeichert wird.
DerKartenherausgeberbzw.KartenpersonalisiererMUSS sicherstellen, dass die dabei
verwendeten kryptographischen Algorithmen die aktuellen Mindestanforderungen
der gematikentsprechend [gemSpec_Krypt]erfüllen. **[\<=]**

Die Mindestanforderungen der gematik an kryptographische Algorithmen sind in
[gemSpec_Krypt] beschrieben.

**GS-A_2244 - PIN/PUK-Speicherung: Verschlüsselung unterschiedlicher PINs mit
unterschiedlichen Schlüsseln**

Falls PINs bzw. PUKs außerhalb der Karte gespeichert werden, dann MUSS
derKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der Kartenpersonalisiererfür den Schutz
unterschiedlicher PINs und der PUK einer Karte während der Speicherung
verschiedene Verschlüsselungsschlüssel verwenden. **[\<=]**

**GS-A_2246 - PIN/PUK-Speicherung: Verschlüsselung gleicher PINs führt zu
unterschiedlichen verschlüsselten Werten**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS sicherstellen,
dass falls zwei PINs zufällig den gleichen Wert aufweisen, diese bei der
Verschlüsselung zur Speicherung
beimKartenherausgeberbzw.Kartenpersonalisierernicht auf den gleichen
verschlüsselten Wert abgebildet werden. **[\<=]**

**GS-A_2247 - PIN/PUK-Speicherung: Wiederholte Verschlüsselung der PIN führt
zu unterschiedlichen Werten**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS sicherstellen,
dass, falls dieselbe PIN wiederholt verschlüsselt wird, die entsprechenden
verschlüsselten Werte unterschiedlich sind. **[\<=]**

**GS-A_2248 - PIN/PUK-Speicherung: unterschiedliche Schlüssel für
unterschiedliche Zwecke**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS sicherstellen,
dass für das Verschlüsseln der PIN zur Speicherung je Verwendungszweck bzw.
Empfänger (u. a. PIN-Druck, Chip-Personalisierung, Speicherung)
unterschiedliche Schlüssel verwendet werden. **[\<=]**

**GS-A_2249 - PIN/PUK-Speicherung: Dokumentation der Zwecke**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS sicherstellen,
dass für die Schlüssel die entsprechenden Verwendungszwecke bzw. Empfänger
dokumentiert werden. **[\<=]**

Die Dokumentation dient zum Nachweis der korrekten Schlüsselverwendung und kann
u.a. im Falle von Audits herangezogen werden.

**GS-A_2250 - PIN/PUK-Speicherung: Entschlüsselung nur durch berechtigten
Empfänger**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS durch
geeignete organisatorische und technische Maßnahmen (z. B. Schlüsseltrennung,
getrennte HSMs) sicherstellen, dass nur innerhalb der Sicherheitsmodule
berechtigter Empfänger und Komponenten die PIN entschlüsselt und im Klartext
vorliegen kann. **[\<=]**

### 2.3 PIN/PUK-Transport

Ein Transport der PIN/PUK innerhalb des Systems ist zu verschiedenen Zwecken
notwendig. Dazu gehört z. B. die Mitteilung der PIN durch den
Kartenherausgeber bzw. Kartenpersonalisierer an den Karteninhaber oder der
Druck des PIN/PUK-Briefes. Die nachfolgenden Mindestanforderungen für den
PIN/PUK-Transport müssen für jeden Transport eingehalten werden.

Dieses Unterkapitel betrifft nicht die Verteilung öffentlicher Transport-PINs
bzw. Einmal-PINs, die nach der Eingabe durch den Karteninhaber zu ändern sind.

**GS-A_2253 - PIN/PUK-Transport: Sicherer PIN-Transport beim Kartenherausgeber
bzw. Kartenpersonalisierer**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS sicherstellen,
dass die PIN/PUK in Transport und Speicherung vor nicht autorisierter
Aufdeckung und Weitergabe geschützt wird. **[\<=]**

**GS-A_2254 - PIN/PUK-Transport: Schutz außerhalb geschützter Hardware beim
Kartenherausgeber bzw. Kartenpersonalisierer**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS sicherstellen,
dass PINs/PUKs außerhalb geschützter Hardware nicht unverschlüsselt
auftreten. Ausnahme ist der einmalige Ausdruck des PIN/PUK-Briefes, der durch
gesonderte organisatorische Maßnahmen gesichert ist. **[\<=]**

**GS-A_2255 - PIN/PUK-Transport: Verteilung beschränken**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS sicherstellen,
dass die Verteilung der PIN/PUK auf das absolut notwendige Maß eingeschränkt
wird, um die Möglichkeiten zur Kompromittierung der PIN/PUK zu minimieren und
potentielle Schäden zu beschränken. **[\<=]**

**GS-A_2256 - PIN/PUK-Transport: einmalige PIN-Erstellung beim Kartenherausgeber
bzw. Kartenpersonalisierer**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS sicherstellen,
dass eine PIN/PUKfür den Transport nur erstellt wird, wenn dies erforderlich
ist und direkt dem Karteninhaber übermittelt wird. **[\<=]**

**GS-A_2260 - PIN/PUK-Transport: Transport außerhalb eines Sicherheitsmoduls**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS sicherstellen,
dass während des elektronischen PIN/PUK-Transports außerhalb einer sicheren
Umgebung oder eines Sicherheitsmoduls, die PIN verschlüsselt ist.
DerKartenherausgeberbzw.KartenpersonalisiererMUSS sicherstellen, dass die dabei
verwendeten kryptographischen Algorithmen die aktuellen Mindestanforderungen
der gematikentsprechend [gemSpec_Krypt]erfüllen. **[\<=]**

**GS-A_2261 - PIN/PUK-Transport: Transport außerhalb eines Sicherheitsmoduls -
kein Klartext**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS sicherstellen,
dass eine PIN/PUK außerhalb einer sicheren Umgebung oder eines
Sicherheitsmoduls nicht im Klartext erscheint.Ausnahme ist der Ausdruck des
PIN/PUK-Briefes, der durch gesonderte organisatorische Maßnahmenzu sichernist. **[\<=]**

**GS-A_2264 - PIN/PUK-Transport: elektronische PIN-Verteilung**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS sicherstellen,
dass während der elektronischen PIN/PUK-Verteilung außerhalb einer sicheren
Umgebung oder eines Sicherheitsmoduls die Integrität der PIN/PUK geschützt
wird. DerKartenherausgeberbzw.KartenpersonalisiererMUSS sicherstellen, dass die
dabei verwendeten kryptographischen Algorithmen die aktuellen
Mindestanforderungen der gematikentsprechend [gemSpec_Krypt]erfüllen. **[\<=]**

**GS-A_2266 - PIN/PUK-Transport: Verschlüsselung gleicher PINs muss zu
unterschiedlichen Werten führen**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS sicherstellen,
dass, falls zwei PINs einer Karte zufällig den gleichen Wert aufweisen, sie
bei der Verschlüsselung zum Transport auf verschiedene verschlüsselte Werte
abgebildet werden. **[\<=]**

**GS-A_2270 - PIN/PUK-Transport: Unterschiedliche verschlüsselte Werte auch bei
gleichen PINs**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS sicherstellen,
dass falls zwei PINs unterschiedlicher Karten zufällig den gleichen Wert
aufweisen, sie bei der Verschlüsselung zum Transport auf verschiedene
verschlüsselte Werte abgebildet werden. **[\<=]**

**GS-A_2271 - PIN/PUK-Transport: kein Rückschluss auf vorher benutzte
Schlüssel**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS sicherstellen,
dassdie WahlderSchlüsselzum Schutz der PIN/PUK während der
Verteilungsoerfolgt, dass es nicht möglich ist, bei Kenntnis aller ab einem
Zeitpunkt benutzten Schlüssel die vorher benutzten Schlüssel abzuleiten. **[\<=]**

**GS-A_2274 - PIN/PUK-Transport: Löschung der PIN nach Transport**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS sicherstellen,
dass die PIN/PUK nach der Übertragung in den bei der Übertragung beteiligten
und in seiner Verantwortung befindlichen Komponenten sicher gelöscht werden. **[\<=]**

Im BSI-Grundschutzbaustein M 2.167 „Auswahl geeigneter Verfahren zur Löschung
oder Vernichtung von Daten“ oder in der Technischen Leitlinie des BSI
"Richtlinien für das Löschen und Vernichten von schutzbedürftigen
Informationen auf analogen und digitalen Datenträgern" sind
Maßnahmenempfehlungen für sicheres Löschen beschrieben.

**GS-A_2276 - PIN/PUK-Transport: Aktivitäten im Vier-Augen-Prinzip bei der
Zuordnung einer PIN/PUK zu einer Karte**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS sicherstellen,
dass alle Aktivitäten und die unterstützenden Systemfunktionen der
PIN/PUK-Herausgabe, die die Zuordnung einer PIN/PUKzu einer Karte oder zu einem
Karteninhaber betreffen und die Personal des Herausgebers bzw. Personal des
vomKartenherausgeberbeauftragtenKartenpersonalisierersbenötigen, dem
Vier-Augen-Prinzip gehorchen. **[\<=]**

**GS-A_2277 - PIN/PUK-Transport: Aktivitäten im Vier-Augen-Prinzip beim
Rücksetzen des Fehlbedienungszählers**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS sicherstellen,
dass alle Funktionen, die das Rücksetzen des Fehlbedienungszählers bzw. der
(De)Aktivierung einer Karte oder Kartenanwendung betreffen und die Personal
desKartenherausgebersbzw.Kartenpersonalisiererbenötigen, dem
Vier-Augen-Prinzip gehorchen. **[\<=]**

### 2.4 PIN/PUK-Verwendung

An den Kartenherausgeber und den Kartenpersonalisierer werden bzgl. der
Verwendung der PIN/PUK keine Anforderungen gestellt.

### 2.5 PIN -Änderung

Eine Änderung einer PIN kann aus mehreren Gründen notwendig sein:

 ---> UL

Für die Prozesse beim Kartenherausgeber bzw. Kartenpersonalisierer ergeben sich
hieraus folgende Anforderungen:

**GS-A_2284 - PIN/PUK-Änderung: Änderungen durch Kartenpersonalisierer im
Vier-Augen-Prinzip**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS
sicherstellen,dass alleProzesse einerPIN-Änderung, die Personal
desKartenherausgebersbzw.Kartenpersonalisierersbenötigen, dem
Vier-Augen-Prinzip gehorchen. **[\<=]**

**GS-A_2285 - PIN/PUK-Änderung: Prozess bei Kompromittierung beim
Kartenherausgeber bzw. Kartenpersonalisierer**

Falls der Kartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit
der Kartenpersonalisierung beauftragt, der Kartenpersonalisierer eine PIN/PUK
von Kartendaten ableiten kann oder in anderer Weise zur Verfügung hat, MUSS er
sicherstellen, dass, falls eine PIN/PUK beim Kartenherausgeber bzw.
Kartenpersonalisierer kompromittiert wurde, die PIN/PUK beim Kartenherausgeber
bzw. Kartenpersonalisierer so schnell wie möglich deaktiviert bzw. gesperrt
wird. Der Kartenherausgeber bzw. Kartenpersonalisierer MUSS sicherstellen, dass
es einen praktikablen Prozess gibt, um kompromittierte PIN/PUK beim
Kartenherausgeber bzw. Kartenpersonalisierer zu sperren. Der Kartenherausgeber
bzw. Kartenpersonalisierer MUSS den Karteninhaber über die Kompromittierung
informieren. **[\<=]**

**GS-A_5085 - PIN/PUK-Änderung: Prozess bei Kompromittierungsmeldung durch
Karteninhaber**

Falls derKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit
der Kartenpersonalisierung beauftragt, der Kartenpersonalisierereine PIN/PUKvon
Kartendaten ableiten kann oder in anderer Weise zur Verfügung hat, MUSS er
sicherstellen,dass,fallseinePIN/PUKvom Karteninhaber als kompromittiert
gemeldet wurde, die PIN/PUKbeimKartenherausgeber bzw.Kartenpersonalisierer so
schnell wiemöglich deaktiviert bzw. gesperrt wird.DerKartenherausgeber
bzw.KartenpersonalisiererMUSSsicherstellen,dasseseinen praktikablen Prozess
gibt, um kompromittierte PIN/PUKbeimKartenherausgeber bzw.Kartenpersonalisierer
zu sperren. DerKartenherausgeber
bzw.KartenpersonalisiererMUSSdenKarteninhaberüber die Prozesse zur Sperrung
von kompromittierten PIN/PUKinformieren **[\<=]**

### 2.6 PIN/PUK-Löschung

Die PIN/PUK darf nur für den vorgesehenen Zweck verwendet werden. Um
missbräuchliche Verwendung und Kompromittierungsmöglichkeiten zu verringern,
muss eine nicht mehr benötigte PIN/PUK daher in allen Komponenten
unverzüglich sicher gelöscht werden. In der Regel sind die PINs/PUKs nach dem
einmaligen Gebrauch unverzüglich zu löschen.

Für die ggf. notwendige Speicherung in zentralen Systemen in der Verantwortung
des Kartenherausgebers bzw. des von ihm beauftragten Kartenpersonalisierers
sind die folgenden Anforderungen mindestens einzuhalten.

**GS-A_2287 - PIN/PUK-Löschung: Nachweis der Löschung nicht mehr gebrauchter
PIN beim Kartenherausgeber bzw. Kartenpersonalisierer**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS sicherstellen,
dass die unverzügliche sichere Löschung von nicht mehr benötigten
elektronischen PINs/PUKsbzw. zugeordnetenSchlüsseln in den Komponenten und
Diensten, die in seiner Verantwortung sind, in seinem Sicherheitskonzept
nachgewiesen wird. **[\<=]**

**GS-A_2252 - PIN/PUK-Löschung: Löschung von PIN/PUK nach Ablauf der
Speicherdauer**

Der Kartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der Kartenpersonalisierer MUSS
sicherstellen, dass die PIN/PUK nach Ablauf der Speicherdauer in den
Komponenten und Diensten, die in seiner Verantwortung sind, sicher gelöscht
wird. **[\<=]**

**GS-A_2291 - PIN/PUK-Löschung: Löschen von nicht mehr benötigten
Klartext-PIN**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS Vorkehrungen
treffen, um die nicht mehr benötigte Klartext-PIN/PUK so zerstören zu
können, dass es nicht mehr möglich ist, die PIN/PUK ganz oder teilweise zu
rekonstruieren. Insbesondere MÜSSEN
dieKartenherausgeberbzw.Kartenpersonalisierergeeignete Sicherheitsmaßnahmen
treffen in Bezug auf die interne Handhabung und Beseitigung von
zurückgesendeten PIN/PUK-Briefen und Material, das mit dem ursprünglichen
Druck der PIN/PUK-Briefe verbunden ist. Dabei MUSS
derKartenherausgeberbzw.Kartenpersonalisierersicherstellen, dass die Behandlung
zurückgesandter PIN/PUK-Briefe von der Behandlung der zurückgesandten Karten
organisatorisch getrennt ist. **[\<=]**

**GS-A_2292 - PIN/PUK-Löschung: Außerbetriebnahme der PIN und Karte**

Der Kartenherausgeber MUSS die sichere Außerbetriebnahme der PIN und der damit
verbundenen Karten regeln. Der Kartenherausgeber MUSS entsprechende
praxistaugliche Verfahrenfestlegen. **[\<=]**

Hinweis: Auch abgelaufene Karten bergen Risiken z. B. auf der eGK vorhandene
medizinische Daten wie etwa Notfalldaten sowie im HBA noch verwendbare
C2C-Authentisierungsschlüssel, die einen Offline-Zugriff auf geschützte
medizinische Daten ermöglichen.

### 3 Mindestanforderungen und Sicherheits-Policies für die Behandlung der Schlüssel zum Schutz der PIN/PUK

Das sichere Management der Schlüssel für die Behandlung der PIN/PUK ist
entscheidend für die Einhaltung der Mindestanforderungen für PIN/PUK. Die
Schlüsselverwendung und die nachfolgenden Bereiche des Schlüsselmanagements
müssen die Mindestanforderungen der gematik erfüllen: Der Lebenszyklus der
Schlüssel umfasst nach [ISO11770] die Schlüsselerzeugung (generation) mit
Registrierung des Schlüssels bzw. des Zertifikats, die Schlüsselableitung,
die Schlüsselaktivierung (activation) mit der Installation, jeweils optional
die Zertifikatserzeugung, die Schlüsselverteilung, die Schlüsselspeicherung
sowie die Schlüsseldeaktivierung (deactivation), die Reaktivierung
(reactivation) und die Schlüsselzerstörung (destruction).

**GS-A_2295 - Schutz der Schlüssel für PIN/PUK gemäß Hierarchiestufe 4**

DerKartenherausgeber oder, falls der Kartenherausgeber einen Dritten mit der
Kartenpersonalisierung beauftragt, der KartenpersonalisiererMUSS sicherstellen,
dass für die Schlüssel zum Schutz der PIN/PUK, die bei der Kartenproduktion
verwendet werden, die organisatorischen und technischen Maßnahmen eingesetzt
werden, die sicherstellen, dass

 ---> UL

**[\<=]**

### 4 Anhang A – Verzeichnisse

### 4.1 Abkürzungen

<table><tr><th>
Kürzel

</th><th>
Erläuterung

</th></tr><tr><td>
C2C

</td><td>
Card to Card

</td></tr><tr><td>
CA

</td><td>
Certification Authority

</td></tr><tr><td>
eGK

</td><td>
elektronische Gesundheitskarte

</td></tr><tr><td>
HBA

</td><td>
(elektronischer) Heilberufsausweis

</td></tr><tr><td>
HSM

</td><td>
Hardware Sicherheits Modul

</td></tr><tr><td>
ISO

</td><td>
International Organization for Standardization

</td></tr><tr><td>
PIN

</td><td>
Persönliche Identifikationsnummer

</td></tr><tr><td>
PUK

</td><td>
Personal Unblocking Key

</td></tr><tr><td>
SMC

</td><td>
Security Module Card

</td></tr><tr><td>
TI

</td><td>
Telematikinfrastruktur

</td></tr></table>

### 4.2 Glossar

Das Projektglossar wird als eigenständiges Dokument zur Verfügung gestellt.

### 4.3 Referenzierte Dokumente

### 4.3.1 Dokumente der gematik

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
[gemSpec_Krypt]

</td><td>
gematik: Verwendung kryptographischer Algorithmen in der Telematikinfrastruktur

</td></tr></table>

### 4.3.2 Weitere Dokumente

<table><tr><th>
[Quelle]

</th><th>
Herausgeber (Erscheinungsdatum): Titel

</th></tr><tr><td>
[ISO11770]

</td><td>
ISO/IEC 11770: 1996  
Information technology - Security techniques - Key
management  
Part 3: Mechanisms using asymmetric techniques

</td></tr><tr><td>
[RFC2119]

</td><td>
RFC 2119 (März 1997): Key words for use in RFCs to Indicate Requirement Levels
S. Bradner,

http://tools.ietf.org/html/rfc2119

</td></tr></table>





[Dokumentinformationen]: #dokumentinformationen
[Inhaltsverzeichnis]:    #inhaltsverzeichnis
[1]:                     #1-einordnung-des-dokumentes
[1.1]:                   #11-zielsetzung
[1.2]:                   #12-zielgruppe
[1.3]:                   #13-geltungsbereich
[1.4]:                   #14-abgrenzung
[1.5]:                   #15-methodik
[2]:                     #2-mindestanforderungen-und-sicherheits-policies-für-die-behandlung-von-pinpuk
[2.1]:                   #21-pinpuk-erzeugung
[2.2]:                   #22-pinpuk-speicherung
[2.3]:                   #23-pinpuk-transport
[2.4]:                   #24-pinpuk-verwendung
[2.5]:                   #25-pin--änderung
[2.6]:                   #26-pinpuk-löschung
[3]:                     #3-mindestanforderungen-und-sicherheits-policies-für-die-behandlung-der-schlüssel-zum-schutz-der-pinpuk
[4]:                     #4-anhang-a-–-verzeichnisse
[4.1]:                   #41-abkürzungen
[4.2]:                   #42-glossar
[4.3]:                   #43-referenzierte-dokumente
[4.3.1]:                 #431-dokumente-der-gematik
[4.3.2]:                 #432-weitere-dokumente
[Tbl-001]:               #Tbl-001 (&93834775878104)
[Tbl-002]:               #Tbl-002 (&93834778123248)
[Tbl-003]:               #Tbl-003 (&93834776739040)
[Tbl-004]:               #Tbl-004 (&93834776746376)
[http://tools.ietf.org/html/rfc2119]: http://tools.ietf.org/html/rfc2119 (&93834776755728)
