
Elektronische Gesundheitskarte und Telematikinfrastruktur

### Spezifikation<br>Service Monitoring

- Klassifizierung: öffentlich
- Referenzierung: gemSpec_ServiceMon
- Revision: 558730
- Stand: 02.03.2020
- Status: freigegeben
- Version: 1.5.0

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
14.05.18

</td><td>
</td><td>
freigegeben

</td><td>
gematik

</td></tr><tr><td>
1.1.0

</td><td>
26.10.18

</td><td>
</td><td>
Einarbeitung P15.9

</td><td>
gematik

</td></tr><tr><td>
1.2.0

</td><td>
18.12.18

</td><td>
</td><td>
Ergänzung ePA-Inhalte

</td><td>
gematik

</td></tr><tr><td>
1.3.0

</td><td>
15.05.19

</td><td>
</td><td>
Einarbeitung P18.1

</td><td>
gematik

</td></tr><tr><td>
Einarbeitung P20.1

</td><td>
gematik

</td></tr><tr><td>
1.4.0

</td><td>
02.10.19

</td><td>
</td><td>
freigegeben

</td><td>
gematik

</td></tr><tr><td>
Einarbeitung P21.1

</td><td>
gematik

</td></tr><tr><td>
1.5.0

</td><td>
02.03.20

</td><td>
freigegeben

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
- [3] Zerlegung des Produkttyps
- [4] Übergreifende Festlegungen
  - [4.1] Implementierung des Service Monitorings
    - [4.1.1] Verwendung von Standardprodukten
    - [4.1.2] Administration und Konfiguration
    - [4.1.3] Nutzeroberfläche
    - [4.1.4] Dokumentation
  - [4.2] Betrieb des Service Monitorings
    - [4.2.1] Verfügbarkeits- und Durchsatzanforderungen
    - [4.2.2] Speicherungsdauer der übermittelten Daten
  - [4.3] Zugriffs- und Berechtigungskonzept
    - [4.3.1] Zugriffskonzept
    - [4.3.2] Berechtigungskonzept
- [5] Funktionsmerkmale
  - [5.1] Schnittstelle I_View_Service_Monitoring
    - [5.1.1] Darstellung der Monitoring-Daten
    - [5.1.2] Schnittstelle View Service Monitoring API Web Service
    - [5.1.3] Umsetzung
  - [5.2] Schnittstelle I_Monitoring_Update
    - [5.2.1] Schnittstellendefinition
    - [5.2.2] Umsetzung
    - [5.2.3] Nutzung
  - [5.3] Technische Use Cases – TUCs
  - [5.4] Probes
    - [5.4.1] DNS Name Resolution
    - [5.4.2] Konnektorregistrierung*
    - [5.4.3] VPN_Tunnel*
    - [5.4.4] VPN_Tunnel SIS*
    - [5.4.5] Zeitinformation_TI
    - [5.4.6] Zeitinformation_VPN_Zugangsdienst
    - [5.4.7] CRL Download
    - [5.4.8] TSL Download
    - [5.4.9] TSL Download mit Prüfung
    - [5.4.10] TSL Download IPsecTunnel TI*
    - [5.4.11] TSL Download Internet
    - [5.4.12] BNetzA_VL Download
    - [5.4.13] BNetzA Download IPsecTunnel TI*
    - [5.4.14] OCSP
    - [5.4.15] OCSP IPsecTunnel TI*
    - [5.4.16] Fachdienste VSDM
      - [5.4.16.1] Fachdienst VSDM UFS
      - [5.4.16.2] Fachdienst VSDM_VSDD_CMS
    - [5.4.17] Intermediär VSDM*
    - [5.4.18] VSDM- Intermediär VSDM IPsecTunnel TI*
    - [5.4.19] VSDM-Intermediär VSDM Erreichbarkeit
    - [5.4.20] KSRS Upload
    - [5.4.21] KSRS Download
    - [5.4.22] KSRS Download IPsecTunnel TI*
    - [5.4.23] KSRS Download Bestandsnetze
    - [5.4.24] KSRS Download Bestandsnetze IPsecTunnel TI*
    - [5.4.25] Verzeichnisdienst Query
    - [5.4.26] Verzeichnisdienst Query IPsecTunnel TI*
    - [5.4.27] Verzeichnisdienst Application_Maintenance
    - [5.4.28] Ablauf von Server-Zertifikaten (TI)
    - [5.4.29] Ablauf von Server-Zertifikaten (Internet)
    - [5.4.30] ePA - Authentisierung TI
    - [5.4.31] ePA - Authentisierung Internet
    - [5.4.32] ePA - Autorisierung
    - [5.4.33] ePA - I_Authorization_Management::checkRecordExists
    - [5.4.34] ePA - Dokumentenverwaltung
    - [5.4.35] ePA – Verfügbarkeitsmonitoring
    - [5.4.36] ePA -Schlüsselgenerierungsdienst
    - [5.4.37] aAdG-NetG
    - [5.4.38] Erfassung von Service Monitoring-Daten in Probes
  - [5.5] Performance-Kenngrößen
- [6] Anhang A – Verzeichnisse
  - [6.1] Abkürzungen
  - [6.2] Glossar
  - [6.3] Abbildungsverzeichnis
  - [6.4] Tabellenverzeichnis
  - [6.5] Referenzierte Dokumente
    - [6.5.1] Dokumente der gematik
    - [6.5.2] Weitere Dokumente
  - [6.6] Fehlercodes
  - [6.7] Offene Punkte / Klärungsbedarf

### 1 Einordnung des Dokumentes

### 1.1 Zielsetzung

Die vorliegende Spezifikation definiert die Anforderungen zu Herstellung, Test
und Betrieb des Produkttyps Service Monitoring.

Das Service Monitoring überwacht ausgewählte Parameter, um den Betriebszustand
der Telematikinfrastruktur und der Anwendungen der Gesundheitstelematik
darzustellen. Die vorliegende Spezifikation definiert die Anforderungen zu
Herstellung, Test und Betrieb des Service Monitorings.

### 1.2 Zielgruppe

Das Dokument richtet sich an Hersteller und Anbieter des Service Monitorings
sowie Hersteller und Anbieter von Produkttypen, die hierzu eine Schnittstelle
besitzen.

### 1.3 Geltungsbereich

Dieses Dokument enthält normative Festlegungen zur Telematikinfrastruktur des
deutschen Gesundheitswesens. Der Gültigkeitszeitraum der vorliegenden Version
und deren Anwendung in Zulassungs- oder Abnahmeverfahren wird durch die gematik
GmbH in gesonderten Dokumenten (z.B. Dokumentenlandkarte,
Leistungsbeschreibung) festgelegt und bekanntgegeben.

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
Anhang A5).

Die vollständige Anforderungslage für den Produkttyp ergibt sich aus weiteren
Konzept- und Spezifikationsdokumenten, diese sind in dem Produkttypsteckbrief
des Produkttyps Service Monitoring verzeichnet.

Detailspezifikationen zu den Monitoringdaten, d. h. zu den Ziel- und Messwerten
für z. B. den Durchsatz, die Verfügbarkeit sowie für die Bearbeitungszeit
sind in diesem Dokument nicht weiter dargestellt und der [gemSpec_Perf] für
die TI-Plattform und für die Fachdienste zu entnehmen.

Weitergehende betriebliche Festlegungen sowie Details zu dem in diesem Dokument
verwendeten Begriff „Serviceeinheiten“ sind [gemKPT_Betr] zu entnehmen.

### 1.5 Methodik

Anforderungen als Ausdruck normativer Festlegungen werden durch eine eindeutige
ID sowie die dem RFC 2119 [RFC2119] entsprechenden, in Großbuchstaben
geschriebenen deutschen Schlüsselworte MUSS, DARF NICHT, SOLL, SOLL NICHT,
KANN gekennzeichnet.

Sie werden im Dokument wie folgt dargestellt:

\<AFO-ID\> - \<Titel der Afo\>Text / Beschreibung[ \<=]

Dabei umfasst die Anforderung sämtliche zwischen Afo-ID und Textmarke
angeführten Inhalte.

### 2 Systemüberblick

Die folgende Abbildung zeigt die logischen Komponenten und die Außensicht des
Service Monitorings.

![Abbildung-1][Abbildung-1]

Das Service Monitoring besteht logisch aus den Systemen Monitoring_Komponente,
Probe_Komponente (Internet) und Probe_Komponente (TI).

Über die Probe_Komponenten wird die Verfügbarkeit der Dienste der TI im
zentralen Netz der TI und im Internet mittels Probes überwacht. Die in Rot
dargestellten Kommunikationsbeziehungen benötigen einen bestehenden
IPsec-Tunnel der TI.

Die Ergebnisse der Probes-Messungen werden über eine interne Schnittstelle an
die Monitoring_Komponente zur Weiterverarbeitung übertragen.

Hinweis: ABB_ServMon_301 bildet den Stand für das Release 2.1.2 ab und kann bei
künftigen Releases Erweiterungen erfahren.

ABB_ServMon_304 zeigt eine Übersicht über die Datenquellen des Service
Monitorings.

![Abbildung-2][Abbildung-2]

Kenngrößen auf Datenebene 1 des Service Monitorings stammen aus folgenden
Quellen:

 ---> UL

Die folgende Abbildung zeigt zum besseren Verständnis des Dokuments
beispielhaft verschiedene Daten-Ebenen (es wird aber keine Anzahl von konkreten
Ebenen vorgegeben) des Service Monitorings und die entsprechenden
Aggregationen/Korrelationen und die Quellen der Daten:

![Abbildung-3][Abbildung-3]

Kenngrößen auf höheren Datenebenen werden durch Aggregation bzw. Korrelation
aus vorliegenden Kenngrößen erzeugt. Basis für die Aggregation bzw.
Korrelation können vorliegende Kenngrößen und Probe-Daten auf verschiedenen
Ebenen sein. Die Aggregation bzw. Korrelation erfolgt Anwendungsservice- bzw.
Plattformgrenzen-übergreifend.

Der Log-Datei-Analysator wird für zukünftige Fachdienste genutzt, welche noch
nicht das I_Monitoring_Update Interface nutzen.

### 3 Zerlegung des Produkttyps

Im Folgenden wird die Zerlegung des Service Monitorings dargestellt, welche für
die Übersicht der funktionalen Leistungsmerkmale in vorliegender Spezifikation
nötig ist.

![Abbildung-4][Abbildung-4]

In Abbildung 4 werden die Komponenten des Service Monitorings dargestellt.

Die Probes greifen auf die überwachten Schnittstellen analog zu den normalen
Clients dieser Schnittstellen aus dem Internet und aus der TI zu. Dafür werden
zwei Probe-Komponenten vorgesehen:

 ---> UL

Alle Probes mit Zugriff aus dem Internet auf TI Schnittstellen.

 ---> UL

Alle Probes mit Zugriff aus der TI auf TI Schnittstellen.

Die Monitoring-Komponente stellt folgende Funktionalitäten bereit:

 ---> UL

Die Probe-Komponenten stellen folgende Funktionalitäten bereit:

 ---> UL

Die Architektur des Service Monitorings sieht die Erweiterbarkeit um neue
Funktionalitäten (z. B. Aufruf zusätzlicher Probes) vor, indem die
bestehenden Schnittstellen im Komponentenmodell erweitert oder neue
Schnittstellen zu den Komponenten hinzugefügt werden.

### 4 Übergreifende Festlegungen

### 4.1 Implementierung des Service Monitorings

**TIP1-A_6739 - Service Monitoring, Festlegung der bereitzustellenden
Schnittstellen**

Das Service Monitoring MUSS die Schnittstellen I_View_Service_Monitoring und
I_Monitoring_Update implementieren und bereitstellen. **[\<=]**

Diese Schnittstellen werden in Kap. 5.1 und Kap. 5.2 näher definiert.

**TIP1-A_6740 - Erreichbarkeit des Service Monitorings**

Das Service Monitoring MUSS die Schnittstellen I_Monitoring_Update in der TI und
I_View_Service_Monitoring im Internet und der TI für Nutzer mit entsprechenden
Rechten anbieten. **[\<=]**

Diese Schnittstellen werden in Kap. 5.1 und Kap. 5.2 näher definiert.

### 4.1.1 Verwendung von Standardprodukten

**TIP1-A_6743 - Verwendung von Standardprodukten**

Der Anbieter des ServiceMonitorings SOLL IT-Monitoring-Standardprodukte für das
Service Monitoring verwenden. **[\<=]**

### 4.1.2 Administration und Konfiguration

**TIP1-A_6745 - Service Monitoring, Konfigurierbarkeit**

Das Service Monitoring MUSS so implementiert werden, dass Administratoren
Berechtigungen, Schwellwerte, Aggregationsregeln und Probes konfigurieren
können. **[\<=]**

**A_13498 - Service Monitoring, Speicherung Konfigurationsdaten**

Das Service Monitoring MUSS die Konfigurationsdaten persistent speichern sowie
deren Export und Import unterstützen. **[\<=]**

**TIP1-A_6746 - Service Monitoring, Schwellwerte**

DasService MonitoringMUSSdie Konfiguration sowie den Export und Import von
Schwellwerten fürjede einzelnePerformance-Kenngrößen erlauben.DieÜber-
bzw.Unterschreitungdieser Schwellwerte durch die Daten der dazugehörenden
Performance-KenngrößeMUSSzur Markierung (z.B. inGrün, Gelb undRot) der
entsprechenden Werte in der Darstellung führen.Für
jedePerformance-Kenngröße MUSS die Angabe mehrerer Schwellwerte mit
dazugehörender Kritikalität/Darstellungsfarbe möglich sein. **[\<=]**

**TIP1-A_6747 - Service Monitoring, Aggregationsregeln**

Das Service Monitoring MUSS mindestens folgende Aggregationsregeln für alle
Kenngrößen (übergreifend für alle Dienste und Dienstinstanzen)
unterstützen:

 ---> UL

Die Ergebnisse der Aggregation MÜSSEN als Kenngrößen in den
aggregierten  Service Monitoring Daten gespeichert werden und wie alle
anderen aggregierten Daten darstellbar und auswertbar sein. **[\<=]**

Für das Monitoring von komplexen Anwendungsfällen ist die direkte Ermittlung
von Kenngrößen für den gesamten Anwendungsfall nicht immer direkt möglich.
Deshalb besteht die Notwendigkeit der Aggregation und Darstellung von
Teilschritt-Kenngrößen auf Anwendungsfallniveau.

**TIP1-A_7084 - Service Monitoring, Konfiguration komplexer Anwendungsfälle**

Das Service Monitoring MUSS für komplexe Anwendungsfälle die folgenden
Konfigurationen durch berechtigte Nutzer unterstützen:

 ---> UL

**[\<=]**

**TIP1-A_7353 - Service Monitoring, Konfiguration Dashboard**

Das Service Monitoring MUSS jedem Nutzer die Konfiguration eines eigenen
Dashboards ermöglichen. **[\<=]**

**A_13501 - Service Monitoring, Öffentliche Dashboards**

Das Service Monitoring MUSS dem Nutzer die Veröffentlichung eines eigenen
Dashboards ermöglichen. Ein öffentliches Dashboard MUSS von allen anderen
Nutzern übernommen werden können. **[\<=]**

**TIP1-A_7085 - Service Monitoring, Wartungskalender**

DasService MonitoringMUSSfür jede Dienstinstanz einen Wartungskalender
unterstützen.Der WartungskalenderMUSS das Eintragen von Wartungszeiträumen
erlauben. Die WartungszeiträumeMÜSSENbei der Berechnungund Darstellungder
Verfügbarkeit dieser Dienstinstanz bzw. von übergreifenden Anwendungsfällen
berücksichtigt werden. **[\<=]**

**A_13502 - Service Monitoring, Wartungskalender, Berechtigungen**

Das Service Monitoring MUSS allen Nutzern mit Berechtigungen für eine
Dienstinstanz die Anzeige des Wartungskalenders dieser Dienstinstanz
ermöglichen. Die Änderung des Wartungskalenders MUSS für alle Nutzer mit der
Zusatzberechtigung "Wartungskalender ändern" möglich sein. **[\<=]**

**TIP1-A_7086 - Service Monitoring, Alarmierung**

Das Service Monitoring MUSS eine konfigurierbare Alarmierung bei Störungen
(Ausfall/Nichtverfügbarkeit, Über-/Unterschreitung von Schwellwerten) pro
Kenngröße unterstützen. Als Alarmierungsziel MÜSSEN pro Kombination aus
Kenngröße und Dienstinstanz mindestens unterstützt werden:

 ---> UL

Die Alarmierungsziele (Gruppen von E-Mail Adressen und/oder SMS Nummern) MÜSSEN
in Abhängigkeit von Tageszeit und Wochentag/Feiertag gewählt werden
können.Die Alarmierung MUSS eine Eskalation beinhalten, wenn der Alarmierte
die Bearbeitung nicht nach einer konfigurierbaren Zeit bestätigt.Die
Alarmierung MUSS wiederholte Alarmierungen zur gleichen Ursache (z.B. Ausfall
eines Dienstes wird alle 5 Minuten gemeldet) unterdrücken können (nur eine
Alarmierung wenn der Alarmierungszustand eintritt und (optional) wenn er
endet).Die Alarmierung MUSS berechtigten Nutzern eine Übersicht über die
ausgelösten Alarmierungen und den Status der Alarmierung (offen, vom
Bearbeiter bestätigt, …) in der Nutzeroberfläche darstellen können.Die
Alarmierung MUSS eine Kurzbeschreibung der auslösenden Ursache enthalten. Die
 Kurzbeschreibung  MUSS konfigurierbar für jede Alarmierung aus mindestens
folgenden Quellen wählbar sein:

 ---> UL

Die Alarmierung MUSS eine Eskalation beinhalten, wenn der Alarmierte die
Bearbeitung nicht nach einer konfigurierbaren Zeit bestätigt.Die Alarmierung
MUSS wiederholte Alarmierungen zur gleichen Ursache (z.B. Ausfall eines
Dienstes wird alle 5 Minuten gemeldet) unterdrücken können (nur eine
Alarmierung wenn der Alarmierungszustand eintritt und (optional) wenn er
endet). Die Alarmierung MUSS berechtigten Nutzern eine Übersicht über die
ausgelösten Alarmierungen und den Status der Alarmierung (offen, vom
Bearbeiter bestätigt, …) in der Nutzeroberfläche darstellen können. ​​ **[\<=]**

Die Alarmierung dient der Benachrichtigung von Service Monitoring-Nutzern über
Störungen. Zu den Nutzern gehören auch Betreiber von (Fach-) Diensten, für
welche die Alarmierungsziele durch einen Administrator entsprechend
eingerichtet werden können.

**TIP1-A_7087 - Service Monitoring, Log-Datei-Analysator**

DasService MonitoringMUSS einen Log-Datei-Analysator
bereitstellen.DieserLog-Datei-AnalysatorMUSSLog-Dateienvon Dienstenimportieren,
aus ihnenkonfigurierbar Daten extrahieren und in den Service
Monitoring-Datenbestandals Kenngrößenübernehmen können.Die Konfiguration
für konkrete Log-Dateien MUSS für Administratoren möglich sein.   **[\<=]**

**TIP1-A_7088 - Service Monitoring, Rechte der Nutzer gemäß Rolle**

DasService MonitoringMUSS sicherstellen, dass einNutzernur dieFunktionennutzen
kann, die ihm gemäß seiner Rolle zugeteilt sind. **[\<=]**

### 4.1.3 Nutzeroberfläche

**TIP1-A_7089 - Nutzeroberfläche des Service Monitorings: Nutzeroberfläche**

DasService MonitoringMUSS den Nutzerndes Service Monitoringseine
Nutzeroberfläche(I_View_Service_Monitoring)zur Verfügung stellen, welche
denZugriff auf die Betriebsstatusinformationen ermöglicht. **[\<=]**

**TIP1-A_7091 - Service Monitoring: Nutzerauthentifizierung für
Konfigurationsaufgaben**

DasService MonitoringMUSS mittels einer Authentifizierung sicherstellen, dass
nurNutzermit entsprechenden Rechtendie Konfigurationdes Service
Monitoringsändern können. **[\<=]**

**TIP1-A_7092 - Service Monitoring: Beschreibung Administrationsoberfläche**

Der Anbieter des Service Monitorings MUSS die Inhalte und  Funktionen der
Administrationsoberflächensowie deren Nutzung beschreiben. **[\<=]**

**A_13479 - Service Monitoring: Nutzeroberfläche Gebrauchstauglichkeit**

Der Anbieter des Service Monitorings SOLL die Gebrauchstauglichkeit der
Webanwendung durch Beachtung der Leitsätze gemäß [DIN EN ISO 9241#Teil11]
sicherstellen. **[\<=]**

**A_13480 - Service Monitoring: Nutzeroberfläche Dialoggestaltung**

Der Anbieter des Service Monitorings SOLL die Dialoggestaltung der Webanwendung
durch die Beachtung der Grundsätze der Dialoggestaltung gemäß [DIN EN ISO
9241#Teil110] sicherstellen. **[\<=]**

**A_13481 - Service Monitoring: Nutzeroberfläche Interaktion**

Der Anbieter des Service Monitorings SOLL bei Verwendung von Formulardialogen in
der Webanwendung die Anforderungen und Empfehlungen gemäß [DIN EN ISO
9241-143:2012-06] beachten. **[\<=]**

### 4.1.4 Dokumentation

**TIP1-A_7094 - Protokollierung Nutzerzugriffe**

DasService MonitoringMUSS alle durch die autorisierten Nutzer (inklusive
derAdministratoren) erfolgtenübergreifenden(persönliche Einstellungen für
z.B. eigene Dashboards fallen nicht darunter)Daten-,
Konfigurations-undEinstellungsänderungen chronologischin Form eines Auditlogs
protokollieren und auswertbar zur Verfügung stellen. **[\<=]**

**TIP1-A_7095 - Protokollierung Zugriffe durch autorisierte übergeordnete
Monitoring Systeme**

Das Service Monitoring MUSS alle durch die autorisierten übergeordneten
Monitoring-Systeme (I_View_Service_Monitoring) erfolgten Zugriffe und
Einstellungsänderungen chronologisch in Form eines Auditlogs protokollieren
und auswertbar zur Verfügung stellen. **[\<=]**

**A_13499 - Service Monitoring: Zugriff auf die „Auditlogs**

Das Service Monitoring MUSS den Zugriff auf die „Auditlogs“ rollenbasiert
gestalten. **[\<=]**

### 4.2 Betrieb des Service Monitorings

### 4.2.1 Verfügbarkeits- und Durchsatzanforderungen

Verfügbarkeits- und Durchsatzanforderungen für den Betrieb des Service
Monitorings sind in der [gemSpec_Perf] vorgegeben.

**TIP1-A_6742 - Monitoring des Service Monitorings**

DerBetreiber des Service MonitoringsMUSSdie Verfügbarkeit des Service
Monitorings über ein eigenes IT-Monitoring-System erfassen und die Einhaltung
der entsprechenden Anforderungen nachweisen. **[\<=]**

### 4.2.2 Speicherungsdauer der übermittelten Daten

**TIP1-A_7096 - Speicherungsdauer von übermittelten Daten an das Service
Monitoring**

Das ServiceMonitoring MUSS ermöglichen, dass die Speicherungsdauer für an
dasServiceMonitoring gelieferte Daten pro Dienst einstellbar ist.

DasService MonitoringMUSS als Ausgangswert für die Speicherungsdauer einJahr
für aggregierte Datenund 2 Monatefür Rohdaten (über Schnittstelle
I_Monitoring_Updategelieferte Daten)als Standardwert setzen und die Verkürzung
und Verlängerung derSpeicherungsdauerermöglichen.

Die Verkürzung und Verlängerung der SpeicherungsdauerMUSSmöglichsein. **[\<=]**

Die Werte für die Speicherungsdauer werden vom GTI (Gesamtverantwortlicher TI)
nach Bedarf festgelegt.

### 4.3 Zugriffs- und Berechtigungskonzept

### 4.3.1 Zugriffskonzept

**TIP1-A_7097 - Zugriffsschutz gemäß Schutzbedarf**

Der Anbieterdes Service MonitoringsMUSS entsprechend des Schutzbedarfes der
imService Monitoringdargestellten und verarbeiteten Daten entsprechende
Mechanismen zum Schutz vor unberechtigtem Zugriffumsetzen. **[\<=]**

### 4.3.2 Berechtigungskonzept

**TIP1-A_7352 - Service Monitoring, Konfiguration Berechtigungen**

DasService MonitoringMUSSAdministratoren die Verwaltung vonNutzererlaubenund –
auf Anfrage des GTI – eineAuflistung aller Nutzerkonten liefern können. **[\<=]**

**TIP1-A_7098 - Service Monitoring, Übersicht Zugriffsberechtigungen**

Das Service Monitoring MUSS ein nachvollziehbares Zugriffskonzept vorsehen,
über das zu jeder Zeit für Administratoren erkenn- und verwaltbar ist,
welcher Nutzer welche Zugriffsberechtigungen hat. Dabei MUSS es mindestens
folgende Zugriffsberechtigungen für Nutzer geben:

 ---> UL

**[\<=]**

**TIP1-A_7111 - Service Monitoring, Erteilung Einzel-Zugriffsberechtigungen**

DasService MonitoringMUSSfür Clients der Service Monitoring-Schnittstellen
(z.B. I_View_Service_Monitoring API Web Service)ebenfallsdie Definition
vonZugriffsberechtigungenerlauben. Dabei entfallen die Rechte zur Konfiguration
des Service Monitoring GUIs (Dashboards,…). Diese
ZugriffsberechtigungenMÜSSENauf die eigenen Daten des nutzenden Systems und
die Daten aller für die Serviceerbringung nötigen Dienste beschränkbar sein. **[\<=]**

**A_13574 - Service Monitoring, Zugriffsberechtigungen, Probe Ausführung**

Das Service Monitoring MUSS die Zuordnung von Zugriffsberechtigungen für
einzelne - über ihre ProbeID identifizierte - Probes für alle registrierten
Nutzer mit folgenden Randbedingungen erlauben:

 ---> UL

**[\<=]**

**TIP1-A_7099 - Service Monitoring, Verbot Gruppenberechtigungen**

Das Service Monitoring DARF Gruppenberechtigungen NICHT vorsehen oder
implementieren.Es ist nicht zulässig, dass mehrere Nutzer eine Nutzerkennung
verwenden. **[\<=]**

Hinweis: Als Gruppenberechtigung wird gewertet, wenn mehrere Nutzer die gleiche
Login/Passwort-Kombination benutzen. Das Rollenkonzept erlaubt die Zuordnung
gleicher Rechte für verschiedene Nutzer (mit verschiedenen Logins).

**TIP1-A_6741 - Service Monitoring, Zugriff gemäß Berechtigungs- und
Rollenkonzept**

Das Service Monitoring MUSS die Rechte derNutzer(Akteure) gemäß
Tab_Service_Monitoring_Akteure_und_Rollen beschränken. **[\<=]**

<table><tr><th>
Schnittstelle

</th><th>
Akteur

</th><th>
Basis-Rolle

</th><th>
Berechtigung / Beschreibung

</th></tr><tr><td>
I_Monitoring_Update  
(aus dem zentralen Netz der TI erreichbar)

</td><td>
FA_spez_Dienst, Zentraler_Dienst_TI_Plattform

</td><td>
Keine Rolle

</td><td>
Der Nutzer sendet Monitoringdaten an das Service Monitoring.  
Es erfolgt keine
Authentisierung des Nutzers.

</td></tr><tr><td>
View Service Monitoring API  
(aus dem zentralen Netz der TI und aus dem
Internet erreichbar)

</td><td>
ZIS und Monitoring Systeme (z.B. der Fachdienstbetreiber)

</td><td>
SM-MonRead

</td><td>
Der Nutzer hat lesenden Zugriff (Sichtbar sind seine eigenen Daten sowie die –
für seine Diensterbringung nötigen – TI-Plattformservices) auf
Kenngrößen, Schwellwerte und Daten der Probe-Läufe.

</td></tr><tr><td rowspan="4">
I_View_Service_Monitoring  
(im Internet und in der TI erreichbar)

</td><td>
Registrierter Nutzer  
(ohne Zusatzberechtigungen Anwendungsservices)

</td><td>
SM-TI-User

</td><td>
Der Nutzer hat lesenden Zugriff (Sichtbar sind die Daten der
TI-Plattformservices) auf Kenngrößen, Schwellwerte und Daten der Probe-Läufe.

</td></tr><tr><td>
Registrierter Nutzer  
(mit Zusatzberechtigungen für einzelne
Anwendungsservices)

</td><td>
SM-AS-User

</td><td>
Wie SM-TI-User  
Zusätzlich hat der Nutzer lesenden Zugriff auf die Daten
(Kenngrößen, Schwellwerte und Daten der Probe-Läufe) der berechtigten
Anwendungsservices. Diese Zugriff wird eingeschränkt auf die Daten von
Dienstinstanzen des Anwendungsservices, welche dem Nutzer zugeordnet sind.

</td></tr><tr><td>
Registrierter Nutzer  
(mit Administrationsberechtigungen)

</td><td>
SM-Admin

</td><td>
Wie SM-AS-User  
Zusätzlich hat der Administrator schreibenden und lesenden
Zugriff auf die Konfigurationsdaten des Service Monitorings und der Probes. 

Weiterhin kann er Kenngrößen zu Anwendungsservices oder TI-Plattformservices
zuordnen.

</td></tr><tr><td>
Registrierter Nutzer  
(mit Nutzerverwaltungsberechtigungen)

</td><td>
SM-UserAdmin

</td><td>
Der Administrator kann

 ---> UL

</td></tr></table>

**TIP1-A_7090 - Service Monitoring, Nutzeroberfläche, Nutzerauthentifizierung**

Das Service Monitoring MUSS ermöglichen, dass Nutzer eine User-ID, ein
initiales Passwort und die zur Zwei-Faktor-Authentifizierung nötigen Mittel
zur Nutzung der Schnittstellen I_View_Service_Monitoring beantragen können.Das
Passwort muss durch den Anwender änderbar sein.Die Schnittstelle darf nur nach
erfolgreicher Authentisierung (d.h. nach Nutzen von User-ID, Passwort,
Zwei-Faktor-Authentifizierung) genutzt werden können.Jedem Nutzer muss eine
Rolle gemäß Tab_Service_Monitoring_Akteure_und_Rollen zugewiesen werden.Für
Nutzer mit der Rolle SM-AS-User muss der berechtigte Anwendungsservice
festgelegt werden. **[\<=]**

### 5 Funktionsmerkmale

### 5.1 Schnittstelle I_View_Service_Monitoring

### 5.1.1 Darstellung der Monitoring-Daten

**TIP1-A_7102 - Service Monitoring, Darstellung, GUI**

DasService MonitoringMUSS über die Schnittstelle I_View_Service_Monitoring eine
grafische Darstellung der Monitoring-Datenbereitstellen. **[\<=]**

**TIP1-A_7103 - Service Monitoring, GUI, Dashboard**

DasService MonitoringMUSSin dergrafischenDarstellungein Dashboard zur
Darstellung des Status der überwachten Dienste bereitstellen. **[\<=]**

**TIP1-A_7104 - Service Monitoring, GUI, Browser**

Das Service Monitoring MUSS die aktuellen und historischen Ereignisse des
Service Monitorings wie z. B. Statusmessungen der Probes oder empfangene
Performance- und Auslastungsdaten grafisch über marktübliche Browser
(mindestens Firefoxin der aktuellen Version) darstellen können. **[\<=]**

**TIP1-A_7105 - Service Monitoring, GUI, Performance-, Auslastungs- und
Verfügbarkeitsdaten**

DasService MonitoringMUSSin dergrafischenDarstellung die
Performance-,Auslastungs- und Verfügbarkeitsdatenmitkonfigurierbaren
Zeiträumen anzeigen. Reports mit den Performance-,Auslastungs- und
Verfügbarkeitsdatenmit konfigurierbaren Zeiträumen MÜSSENüber das GUI als
Fileexportierbar sein.Das Service Monitoring MUSS eine Beschreibung von dem
File-Format bereitstellen, welche auch über das GUI abgerufen werden kann. **[\<=]**

**TIP1-A_7106 - Service Monitoring, GUI, Störungs-Dashboard**

DasService MonitoringMUSSin dergrafischenDarstellungdie Konfiguration eines
Dashboards zur Darstellung der Störungen der überwachten Dienste
bereitstellen.Unter Störungen fallen Ausfall/Nichtverfügbarkeit und
Über-/Unterschreitung von Schwellwerten. DasStörungs-Dashboardzeigt nur die
Dienste mit StörungenundkeineDienste ohne Störungen. **[\<=]**

**TIP1-A_7107 - Service Monitoring, GUI, Dokumentation**

DasService MonitoringMUSSfür diegrafische Darstellungeine
Dokumentationbereitstellen(z. B. Bedeutung der Statusfarben, Bedingungen für
Statusänderungen). Die Dokumentation MUSS für die Nutzer einsehbar sein. **[\<=]**

**TIP1-A_7108 - Service Monitoring, GUI, Details zu den Probe-Messungen**

Die grafische Darstellung SOLL Details zu den Probe-Messungen (unter anderem den
Mitschnitt derPrüfkommunikation) für eine konfigurierbare Anzahl der letzten
Messungen speichern und anzeigen können. **[\<=]**

**TIP1-A_7109 - Service Monitoring, Darstellung, Tabellen und Metriken**

Die Darstellungder Monitoring DatenSOLL–konfigurierbarfür jede
Kenngröße–in Tabellen und Metriken anzeigt werdenkönnen. **[\<=]**

**TIP1-A_7110 - Service Monitoring, Darstellung, Zeitachse mit verschiedenen
Kenngrößen**

Die Darstellungder Monitoring-DatenSOLLeinen zeitlichen Bezug
zwischenauswählbaren Kenngrößen darstellenkönnen. **[\<=]**

### 5.1.2 Schnittstelle View Service Monitoring API Web Service

Als Bestandteil der I_View_Service_Monitoring bietet der View Service Monitoring
API Web Service die Möglichkeit der automatisierten Abfrage über
HTTP-GET-Requests, die als Antwort wahlweise Performance-Daten im XML- oder
JSON-Format zurückgeben.

**TIP1-A_7112 - Service Monitoring, View Service Monitoring API**

Das Service Monitoring MUSS die Schnittstelle View Service Monitoring APIunter
einer URL im Internet und in der TIbereitstellen. **[\<=]**

**TIP1-A_7113 - Service Monitoring, I_View_Service_Monitoring, View Service
Monitoring API, Dokumentation**

Das Service Monitoring MUSS für das View Service Monitoring API

 ---> UL

**[\<=]**

**TIP1-A_7349 - Service Monitoring, View Service Monitoring API, Parameter**

Das Service Monitoring MUSS die HTTP GET-Anfragen in der Schnittstelle View
Service Monitoring API entsprechend von Parametern in der Anfrage beantworten:

 ---> UL

**[\<=]**

**TIP1-A_7350 - Service Monitoring, View Service Monitoring API, Probe
Kenngrößen**

Das Service Monitoring MUSS in der Schnittstelle View Service Monitoring API
für die – über Probes ermittelten – Daten eine Zuordnung zur
Probe-Ausführung ermöglichen. **[\<=]**

**TIP1-A_7351 - Service Monitoring, View Service Monitoring API, Kenngrößen**

Das Service Monitoring MUSSüberdie Schnittstelle View Service Monitoring
APIeinenReport mit den Kenngrößen und ihren Schwellwertenbereitstellen. **[\<=]**

**TIP1-A_7348 - Service Monitoring, I_View_Service_Monitoring, View Service
Monitoring API, Authentifizierung**

Das Service Monitoring MUSS den Aufrufer authentifizieren und den Zugriff auf
Service Monitoring-Daten entsprechend seinen Zugriffsrechten beschränken.
**[\<=]**

### 5.1.3 Umsetzung

**TIP1-A_7114 - Service Monitoring, I_View_Service_Monitoring, TLS-gesicherte
Verbindung**

Das Service Monitoring MUSS die SchnittstelleI_View_Service_Monitoringdurch
Verwendung von TLS mit serverseitiger Authentisierung sichern. **[\<=]**

### 5.2 Schnittstelle I_Monitoring_Update

Diese Schnittstelle wird aus Kompatibilität zur Schnittstelle der
Störungsampel [gemSpec_St_Ampel] unverändert übernommen. Dies erleichtert
die Migration von Diensten, welche bereits die
I_Monitoring_Update-Schnittstelle der Störungsampel nutzen.

### 5.2.1 Schnittstellendefinition

Diese Schnittstelle ermöglicht das Senden von Monitoringdaten der
fachanwendungsspezifischen Dienste und der zentralen Dienste der TI-Plattform
an das Service Monitoring.

Die zu sendenden Daten sind
inTab_gemKPT_Betr_Performance-Kenngroessen festgelegt.

**TIP1-A_7116 - Service Monitoring, Schnittstelle I_Monitoring_Update**

Das Service MonitoringMUSS die Schnittstelle I_Monitoring_Update gemäß Tabelle
Tab_Service_Monitoring_I_Monitoring_Update anbieten.

Tabelle2: Tab_Service_Monitoring_I_Monitoring_Update

<table><tr><th>
Name

</th><th colspan="2">
I_Monitoring_Update

</th></tr><tr><td>
Version

</td><td colspan="2">
Webservice: v1.1

</td></tr><tr><td rowspan="2">
Webservice Operationen

</td><td>
Name

</td><td>
Kurzbeschreibung

</td></tr><tr><td>
update

</td><td>
Die Operation ermöglicht das Senden von Monitoringdaten an das Service
Monitoring.

</td></tr><tr><td>
WSDL

</td><td colspan="2">
I_Monitoring_Update10.wsdl  
Version: 1.1.0  
TargetNamespace:

http://ws.gematik.de/tel/stoerungsampel/wsdl/v1.1

</td></tr><tr><td>
Schema

</td><td colspan="2">
I_Monitoring_Update10.xsd  
Version: 1.1.0  
TargetNamespace:

http://ws.gematik.de/tel/stoerungsampel/v1.1  
ProductInformation.xsd  
Version:
1.1.0  
TargetNamespace:

http://ws.gematik.de/tel/version/ProductInformation/v1.1  
TelematikError.xsd 

Version: 2.0.0  
TargetNamespace:

http://ws.gematik.de/tel/error/v2.0

</td></tr><tr><td>
Webservice Zugangspunkt

</td><td colspan="2">
https://monitoring-update.stampel.telematik:8443/I_Monitoring_Update10

</td></tr></table>

**[\<=]**

**TIP1-A_7117 - Service Monitoring und Client, I_Monitoring_Update, WebService**

Das Service MonitoringunddieClients MÜSSEN die Schnittstelle
I_Monitoring_Update in ihrer jeweiligen Rolle Client bzw. Server als
SOAP-Webservice über HTTPS implementieren. Der Webservice wird durch die
Dokumente I_Monitoring_Update10.wsdl und I_Monitoring_Update10.xsd sowie
Tab_Service_Monitoring_SOAP-Request und Tab_Service_Monitoring_SOAP-Response
definiert. **[\<=]**

**TIP1-A_7118 - Service Monitoring und Client, I_Monitoring_Update, eindeutige
Zuordnung**

Der Anbieter des Service Monitorings MUSS dem Anbieter des Clients der
Schnittstelle I_Monitoring_Update eine eindeutige SystemID (zur Zuordnung der
Monitoringdaten zur Instanz des Produkttyps) zuweisen, die der Anbieter des
Clients in den SOAP-Requests (tns:systemid) verwenden MUSS. **[\<=]**

**TIP1-A_7119 - Service Monitoring und Client, I_Monitoring_Update,
Servicepunkte und IP-Adressen**

Der Anbieter des Clients der Schnittstelle I_Monitoring_Update MUSS dem Anbieter
des Service Monitorings die IP-Adressen mitteilen, von denen Daten an das
Service Monitoring gesendet werden.Der Anbieter des Clients MUSS mit dem
Anbieter des Service Monitorings die gültigen Servicepunkte (Host, Port und
URL) verifizieren. **[\<=]**

In einer Nachricht können mehrere Performancewerte oder Auslastungswerte
übertragen werden.

**TIP1-A_7120 - Service Monitoring und Client, I_Monitoring_Update, maximale
Zeitabweichung zwischen Berichtszeitraum und Nachrichtenübermittelung**

Der Client der Schnittstelle I_Monitoring_Update MUSS die Übertragung der in
[gemSpec_Perf] geforderten Monitoringdaten innerhalb von 120 Sekunden nach
Ablauf eines Reportzeitraumes an das Service Monitoring beginnen. Eine
Kennzeichnung des Report-Zeitraumes erfolgt durch eine Zeitbereichsangabe
(Startzeit und Endzeit) in der übermittelten Nachricht.​​ **[\<=]**

**TIP1-A_7125 - Service Monitoring, I_Monitoring_Update, keine Daten für
Berichtszeitraum**

Das Service Monitoring MUSS Berichtszeiträume – für die nach der maximalen
Zeitabweichung zwischen Berichtszeitraum und Nachrichtenübermittelung keine
Monitoringdaten über die Schnittstelle I_Monitoring_Update geliefert wurden
– im GUI bzw. Dashboard hervorheben. **[\<=]**

**TIP1-A_6744 - Service Monitoring, I_Monitoring_Update, Datenverarbeitung**

Das Service Monitoring MUSS über die Schnittstelle I_Monitoring_Update
gelieferte Daten in den Service Monitoring-Datenbestand als Kenngrößen
entsprechend [gemSpec_Perf] übernehmen. Diese Kenngrößen MÜSSEN analog zu
den durch Probes ermittelten Kenngrößen und den im Service Monitoring durch
Aggregation/Korrelation ermittelten Kenngrößen

 ---> UL

**[\<=]**

### 5.2.2 Umsetzung

Die Schnittstelle ist aus dem zentralen Netz der TI-Plattform erreichbar.

**TIP1-A_7121 - Service Monitoring, I_Monitoring_Update, TLS-gesicherte
Verbindung**

Das Service Monitoring MUSS die Schnittstelle I_Monitoring_Update durch
Verwendung von TLS mit serverseitiger Authentisierung sichern.

Das Service MonitoringMUSSsich mit der Identität ID.ZD.TLS-S und der
enthaltenen Admission-OID „oid_stamp“ gegenüber den nutzenden Systemen
authentisieren. **[\<=]**

**TIP1-A_7122 - Service Monitoring, Datenerhebung**

Der Anbieter des Service Monitorings MUSS die Voraussetzungen dafür schaffen,
dass die in der [gemSpec_Perf] unter GS-A_4147 festgelegten Daten und
Informationen an das Service Monitoring übermittelt werden können.Hierfür
sind durch den Anbieter des Service Monitorings mindestens zu leisten:

 ---> UL

**[\<=]**

**TIP1-A_7123 - Service Monitoring, I_Monitoring_Update, Fehlermeldungen**

Das Service Monitoring MUSS fehlerhafte Zugriffe auf die
Webservice-Schnittstelle I_Monitoring_Update

 ---> UL

beantworten. **[\<=]**

**TIP1-A_7124 - Service Monitoring, I_Monitoring_Update, Rückmeldung der
Nachrichten-ID**

Das Service Monitoring MUSS jeden akzeptierten SOAP-Request mit einem SOAP-Reply
beantworten, der eine eindeutige Nachrichten-ID enthält, die als Referenz für
Rückfragen beim Anbieter des Service Monitorings genutzt werden kann. **[\<=]**

### 5.2.3 Nutzung

**TIP1-A_7126 - Nutzer des Service Monitorings I_Monitoring_Update, Zeitstempel
bei Ausfall/Wiederherstellung**

Der Nutzer der Schnittstelle I_Monitoring_Update MUSS beim Versenden von
Verfügbarkeitsdaten im Alarm-Nachrichtenelement/Nachrichtenobjekt einen
Zeitstempel übermitteln, der die Startzeit oder Endzeit des Alarms angibt. **[\<=]**

**TIP1-A_7127 - Nutzer des Service Monitorings I_Monitoring_Update, eindeutige
Zuordnung des Messwertes**

Der Nutzer der Schnittstelle I_Monitoring_Update MUSS durch die Verwendung von
Attributen gemäßder TabelleTab_Service_Monitoring_Attribute jede
übermittelte Performance-Kenngröße und jeden übermittelten
Alarm-Status-Wert eindeutig kennzeichnen.

Optionale Attribute dürfen nur verwendet werden, wenn sie zur eindeutigen
Zuordnung benötigt werden. **[\<=]**

<table><tr><th>
Attribut / Objekt

</th><th>
Beschreibung

</th></tr><tr><td>
pdt

</td><td>
Produkttyp-ID lt. [gemKPT_Betr]

</td></tr><tr><td>
perftype

</td><td>
Performance-Kenngrößen-ID lt. [gemKPT_Betr]

</td></tr><tr><td>
interface

</td><td>
Schnittstellenoperationen-ID lt. [gemKPT_Betr]

</td></tr><tr><td>
certtype

</td><td>
Zertifkats-Typen-ID lt. [gemKPT_Betr]

</td></tr><tr><td>
querysource

</td><td>
Aufrufquellen-ID lt. [gemKPT_Betr]

</td></tr><tr><td>
connect

</td><td>
Eindeutige ID zur Identifikation bei Ende-zu-Ende-Messungen im Netzwerk-Bereich

</td></tr></table>

Für die Übermittlung von Monitoringdaten wird der SOAP-Request der Operation
„update“ verwendet.

Die folgende Abbildung zeigt die Datenstruktur des SOAP-Requests.

![Abbildung-5][Abbildung-5]

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
tns:request

</td><td>
definiert den SOAP-Request, der über die Operation update an das Service
Monitoring gesendet wird.

</td></tr><tr><td>
tns:systemid

</td><td>
ermöglicht eine eindeutige Identifikation des sendenden Systems/Dienstes. Diese
ID MUSS eindeutig sein und deren Vergabe erfolgt in Abstimmung zwischen dem
Anbieter Service Monitoring und dem Dienstanbieter.

</td></tr><tr><td>
tns:selfdisclosure

</td><td>
enthält Informationen zur Selbstauskunft eines meldenden Systems, siehe
[gemSpec_OM].

</td></tr><tr><td>
tns:message

</td><td>
beinhaltet die in [gemSpec_Perf] für den Dienst geforderten Verfügbarkeits-,
Performance- und Auslastungsdaten.

</td></tr><tr><td>
tns:performance

</td><td>
beinhaltet die in [gemSpec_Perf] für den Dienst geforderten Performance- und
Auslastungsdaten.

</td></tr><tr><td>
tns:alarms

</td><td>
beinhaltet die in [gemSpec_Perf] für den Dienst geforderten
Verfügbarkeitsdaten.

</td></tr><tr><td>
tns:starttime, tns:endtime

</td><td>
definieren das zugrundeliegende Zeitintervall für Performance- und
Auslastungswerte.

</td></tr><tr><td>
tns:value_list

</td><td>
enthält die Liste der Performance-Kenngrößen vom Typ t_dat_update.  
Dieses
Element muss die folgenden Attribute enthalten.  
tns:interface:
Schnittstellenoperationen-ID lt. [gemKPT_Betr]  
tns:pdt: Produkttyp-ID lt.
[gemKPT_Betr]  
tns:perftype: Performance-Kenngrößen-ID lt. [gemKPT_Betr] 

Dieses Element kann die folgenden Attribute enthalten.  
tns:certtype:
Zertifkats-Typen-ID lt. [gemKPT_Betr]  
tns:connect: Eindeutige ID zur
Identifikation bei Ende-zu-Ende-Messungen im Netzwerk-Bereich 

tns:querysource: Aufrufquellen-ID lt. [gemKPT_Betr]  
Mit einer SOAP-Nachricht
können mehrere Werte für gleiche Zeitintervalle übergeben werden.

</td></tr><tr><td>
tns:value

</td><td>
Wert der Performance-Kenngröße

</td></tr><tr><td>
tns:alarm_list

</td><td>
enthält die Alarmstatus-Informationen.  
Dieses Element muss die folgenden
Attribute enthalten.  
tns:interface: Schnittstellenoperationen-ID lt.
[gemKPT_Betr]  
tns:pdt: Produkttyp-ID lt. [gemKPT_Betr]  
tns:perftype:
Performance-Kenngrößen-ID lt. [gemKPT_Betr]  
Dieses Element kann die
folgenden Attribute enthalten.  
tns:certtype: Zertifkats-Typen-ID lt.
[gemKPT_Betr]  
tns:connect: Eindeutige ID zur Identifikation bei
Ende-zu-Ende-Messungen im Netzwerk-Bereich  
tns:querysource: Aufrufquellen-ID
lt. [gemKPT_Betr]

</td></tr><tr><td>
tns:status

</td><td>
enthält den Alarm-Status.  
open: Alarmstatus gesetzt  
close: Alarmstatus
gelöscht  
warn: nicht benutzt  
grace: nicht genutzt

</td></tr><tr><td>
tns:systemtime

</td><td>
Alarmzeit des sendenden Systems zur Erkennung von Inkonsistenzen (z.B. Alarme
aus historischen Daten).

</td></tr></table>

Die Rückgabe enthält die Elemente gemäß der Tabelle
Tab_Service_Monitoring_SOAP-Response.

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
tns:request

</td><td>
definiert die SOAP-Response, die als Antwort auf den SOAP-Request an den Nutzer
gesendet wird.

</td></tr><tr><td>
tns:result

</td><td>
beinhaltet Abnahmebestätigung der Nachricht.  
true | 1: Die Nachricht wurde
vom Service Monitoring angenommen und zur Analyse der Messwerte weitergeleitet.
 
false | 0: Die Nachricht konnte nicht an das Auswertesystem weitergeleitet
werden.

</td></tr><tr><td>
tns:id

</td><td>
ermöglicht eine eindeutige Quittungs-ID für gesendete Nachricht (relevant für
Fehleranalyse).

</td></tr><tr><td>
tns:selfdisclosure

</td><td>
enthält Informationen zur Selbstauskunft des Service Monitorings, siehe
[gemSpec_OM].

</td></tr></table>

Für den Fehlerfall ist das Nachrichtenelement err:Error (gematik-SOAP-Fault,
definiert in Schemadatei TelematikError.xsd gemäß [gemSpec_OM]) verfügbar.

**TIP1-A_7128 - Nutzer des Service Monitorings I_Monitoring_Update, maximale
HTTP-Nachrichtenlänge**

Der Nutzer der Schnittstelle I_Monitoring_Update MUSS beachten,
dassbeiMonitoringnachrichten die maximale HTTP-Nachrichtenlänge
(Headerinformationen und Daten) von 16.000 Bytes nicht überschritten wird.
Größere Nachrichten werden verworfen. **[\<=]**

Nachrichten mit fehlenden oder inkonsistenten Informationen werden akzeptiert,
der Dateninhalt jedoch verworfen.

Das sendende System erhält als Rückmeldung eine Nachrichten-ID, die für
Rückfragen beim Anbieter des Service Monitorings als Referenz genutzt werden
kann. Eine Referenzierung von übermittelten Nachrichten ist nur im Rahmen der
genutzten Datenaufbewahrungsrichtlinie möglich.

**TIP1-A_7129 - Nutzer des Service Monitorings I_Monitoring_Update,
Selbstauskunft als Bestandteil jeder SOAP-Nachricht**

Der Nutzer der Schnittstelle I_Monitoring_Update MUSS in jeder SOAP-Nachricht
das Element selfdisclosure (Selbstauskunft) befüllen. Die Selbstauskunft
basiert auf dem Schema [ProductInformation.xsd] gemäß [gemSpec_OM]. **[\<=]**

**A_15166 - Nutzer der Schnittstelle I_Monitoring_Update, Zertifikatsprüfung**

Der Nutzer der Schnittstelle I_Monitoring_Update SOLL die Vertrauenswürdigkeit
der Verbindung durch die Auswertung des Serverzertifikats überprüfen.Die
Prüfung SOLL gemäß gemSpec_PKI# TUC_PKI_018 mit  - PolicyList:
oid_zd_tls_s (gemäß gemSpec_OID) - KeyUsage: digitalSignature (Prüfung auf
Vorhandensein des Bits) - ExtendedKeyUsages: serverAuth (1.3.6.1.5.5.7.3.1) -
OCSP-Graceperiod: 0 - Offlinemodus: nein - TOLERATE_OCSP_FAILURE: false -
Prüfmodus: OCSP erfolgen. Alternativ ist die Prüfung gemäß
GS-A_5581 zulässig. **[\<=]**

### 5.3 Technische Use Cases – TUCs

Die hier beschriebenen TUCs werden in Probes für wiederkehrende Abläufe
genutzt.

**TIP1-A_7147 - Service Monitoring, TUC_SM_001_DNS_Name_Resolution**

Das Service Monitoring MUSS TUC_SM_001_DNS_Name_Resolution entsprechend
Tab_Service_Monitoring_TUC_SM_001_DNS_Name_Resolutionbereitstellen. Dieser TUC
MUSS in allen Probes zur DNS-Namensauflösung genutzt werden.

Tabelle6: Tab_Service_Monitoring_TUC_SM_001_DNS_Name_Resolution

<table><tr><th>
Name

</th><th colspan="2">
TUC_SM_001_DNS_Name_Resolution

</th></tr><tr><td>
Beschreibung

</td><td colspan="2">
Dieser TUC führt die Auflösung eines FQDN in eine IP-Adresse durch.

</td></tr><tr><td>
Vorbedingungen

</td><td colspan="2">
 ---> UL

</td></tr><tr><td>
Eingangsdaten

</td><td colspan="2">
 ---> UL

</td></tr><tr><td>
Komponenten

</td><td colspan="2">
 ---> UL

</td></tr><tr><td>
Ausgangsdaten

</td><td colspan="2">
 ---> UL

</td></tr><tr><td>
Standardablauf

</td><td>
Aktion

</td><td>
Beschreibung

</td></tr><tr><td>


</td><td>
IP-Adresse der Schnittstelle ermitteln

</td><td>
Durch eine DNS-Anfrage (I_DNS_Name_Resolution:: get_IP_Address.) wird der FQDN
in eine IP-Adresse aufgelöst.

</td></tr><tr><td>


</td><td>
Falls bei der DNS-Anfrage keine Antwort (und kein DNS-Fehler) ermittelt werden
konnte

</td><td>
Prüfung der Erreichbarkeit des DNS-Nameserver über
TUC_SM_002_Erreichbarkeitsprüfung.Der Service Monitoring Datensatz für die
DNS-Namensauflösung wird in diesem Fall in TUC_SM_002_Erreichbarkeitsprüfung
erstellt.

</td></tr><tr><td>


</td><td>
Falls bei der DNS-Anfrage eine Antwort oder ein DNS-Fehler ermittelt werden
konnte

</td><td>
Die Service Monitoring-Daten (aus den Eingangsdaten) werden entsprechend der
durchgeführten Aktionen, Tab_Service_Monitoring_Probe_Daten und um die
Performance-Kenngröße „Bearbeitungszeit“ergänzt.Dabei wird das
„Probe-Ergebnis“ dieses Datensatzes

 ---> UL

</td></tr><tr><td>


</td><td>
Rückgabe der Daten

</td><td>
Rückgabe der Ausgangsdaten

</td></tr></table>

​​ **[\<=]**

**TIP1-A_7148 - Service Monitoring, TUC_SM_002_Erreichbarkeitsprüfung**

Das Service Monitoring MUSS TUC_SM_002_Erreichbarkeitsprüfung entsprechend
Tab_Service_Monitoring_TUC_SM_002_Erreichbarkeitsprüfungbereitstellen. Dieser
TUC MUSS in Probes genutzt werden wenn

 ---> UL

Tabelle7: Tab_Service_Monitoring_TUC_SM_002_Erreichbarkeitsprüfung

<table><tr><th>
Name

</th><th colspan="2">
TUC_SM_002_Erreichbarkeitsprüfung

</th></tr><tr><td>
Beschreibung

</td><td colspan="2">
Dieser TUC prüft die Erreichbarkeit einer Schnittstelle/Dienstes.

</td></tr><tr><td>
Vorbedingungen

</td><td colspan="2">
 ---> UL

</td></tr><tr><td>
Eingangsdaten

</td><td colspan="2">
 ---> UL

</td></tr><tr><td>
Komponenten

</td><td colspan="2">
Service Monitoring Probe, jeweiliger Dienst

</td></tr><tr><td>
Ausgangsdaten

</td><td colspan="2">
 ---> UL

</td></tr><tr><td>
Standardablauf

</td><td>
Aktion

</td><td>
Beschreibung

</td></tr><tr><td>
</td><td>
Prüfung ob Port(s) offen sind

</td><td>
Für die übergebenen Ports/IP-Adresse wird je nach Eingangsparametern ein
TCP-SYN-Scan oder ein UDP-Scan durchgeführt.

</td></tr><tr><td>
</td><td>
Ergänzen der Service Monitoring-Daten

</td><td>
Die Service Monitoring-Daten (aus den Eingangsdaten) werden entsprechend der
durchgeführten Aktionen bzw. deren Ergebnis ergänzt.

Falls

 ---> UL

</td></tr><tr><td>
</td><td>
Rückgabe der Daten

</td><td>
Rückgabe der Ausgangsdaten

</td></tr></table>

**[\<=]**

### 5.4 Probes

Die Probes werden im Normalfall in allen Umgebungen (RU (Referenzumgebung), TU
(Testumgebung) und PU (Produktivumgebung)) eingesetzt. Eine Ausnahme stellen
Probes dar, welche sich mit SMC-B-Zertifikaten authentifizieren müssen.Offener
Punkt: Die Verfügbarkeit von SMC-B-Zertifikaten für die PU befindet sich noch
in der Klärung. Deshalb werden diese Probes derzeit nur für die
Testumgebungen RU und PU TU gefordert. Diese Probes werden im Titel des
entsprechenden Unterkapitels mit "*" gekennzeichnet.

**TIP1-A_7130 - Service Monitoring, Probes, Installation**

DasService MonitoringMUSSAdministratorendas Einbringen/InstallierenvonProbesin
daslaufende Service Monitoring-System erlauben. **[\<=]**

**TIP1-A_7131 - Service Monitoring, Probes, Entwicklung eigener Probes**

DasService MonitoringMUSSdie Entwicklung eigener Probes erlauben.Falls für die
Probe EntwicklungToolsvorgegeben sind,MÜSSENdiesebenanntwerden.
NötigeRandbedingungen (z.B. Schnittstelle zwischen Probes und dem Service
Monitoring System)MÜSSENdokumentiert werden. **[\<=]**

**TIP1-A_7132 - Service Monitoring, Monitoring der Verfügbarkeit mittels
Probes**

Das Service Monitoring MUSS die Verfügbarkeit der Schnittstellen der
fachanwendungsspezifischen Dienste und der zentralen Dienste der TI-Plattform
sowie der Dienste sicherer Übermittlungsverfahren (sowohl im zentralen Netz
der TI als auch im Internet) durch Abfrage der Schnittstellen mit Systemen, die
das Verhalten der echten Nutzer der Schnittstellen simulieren (den sogenannten
Probes) ermitteln.Die Probes senden spezifikationskonforme Abfragen – welche
den Abfragen der echten Nutzer möglichst nahekommen – an die Schnittstellen
und vergleichen die Antworten mit dem erwarteten Ergebnis. Wenn die Antwort dem
erwarteten Ergebnis entspricht, wird die Schnittstelle als verfügbar gewertet.
Bei Abweichungen vom erwarteten Ergebnis MUSS die Schnittstelle – optional in
Abhängigkeit von Regeln – als nicht verfügbar gewertet werden. **[\<=]**

**A_13496 - Service Monitoring, Auswertung der Antworten von Diensten**

Das Service Monitoring MUSS die Antworten von überwachten Diensten analysieren
und daraus den Status von dem Dienst ableiten. Für diese Analyse MUSS
mindestens die Prüfung auf das Vorhandensein bzw. Nichtvorhandensein von
konfigurierbaren Textteilen in der Antwort möglich sein. Die Analyse MUSS für
jede Probe/Fachdienst-Kombination individuell konfigurierbar sein. **[\<=]**

**TIP1-A_7115 - Service Monitoring, Monitoring der Verfügbarkeit, mehrere
Probe-Läufe**

DasService MonitoringMUSSfür das Monitoring der Verfügbarkeit dieErgebnisse
verschiedener Probe-Läufe (z.B. beiredundanten Knoten oderwenn die
Verfügbarkeit eines Anwendungsfalls aus der Verfügbarkeit von beteiligten
Diensten abgeleitet wird)kombinieren können. **[\<=]**

**TIP1-A_7134 - Service Monitoring, Probes, Abstimmung**

Die von den Probes ausgeführten Operationen und das
AusführungsintervallMÜSSEN vom Anbieter des ServiceMonitoringsmit den
Betreibern der überwachten Dienste im Rahmen der gematik-Vorgaben abgestimmt
werden. **[\<=]**

**TIP1-A_7135 - Service Monitoring, keine Beeinträchtigung der Dienste durch
Probes**

DasService MonitoringDARF die mittels Probes überwachten Dienste
NICHTnegativbeeinflussen. **[\<=]**

**TIP1-A_7136 - Service Monitoring, Probes, Konfigurationsdatensätze**

DasService MonitoringMUSSberechtigten Nutzern die Eingabe bzw. Änderung von
Konfigurationsdaten von Probes erlauben. Für jede Probe MÜSSEN mehrere
Konfigurationsdatensätze unterstützt werden. **[\<=]**

**TIP1-A_7137 - Service Monitoring, Probes, Konfiguration von erwarteten
Ergebnissen**

DasService MonitoringMUSSin Probes die Konfiguration der erwarteten Antworten
von aufgerufenen Operationen erlauben. EsMUSSmöglich sein – neben der
normalen fachlichen Antwort–die Fehlermeldung oder ausbleibende Antwort einer
Operation als positivesProbe-Ergebniszu werten. **[\<=]**

**TIP1-A_7138 - Service Monitoring, Probes, Konfiguration von Kenngrößen**

DasService MonitoringMUSSin Probes die Konfiguration von Kenngrößen für die
ermittelten Werte (z. B. Bearbeitungszeit von aufgerufenen Operationen)
erlauben. Diese Kenngrößen und die überdieSchnittstelle I_Monitoring_Update
gelieferten Performance-Kenngrößensowie alle anderen vorhandenen Kenngrößen
imService Monitoring(z.B. durchdenLog-Datei-Analysatorimportierte
Kenngrößen)MÜSSENin den Aggregationsregeln
undSchnittstelleI_View_Service_Monitoring  (DarstellungundView Service
Monitoring API Web Service)verwendet werden können. **[\<=]**

**TIP1-A_7328 - Service Monitoring, Probes, Konfigurationsvariante**

Das Service Monitoring MUSS in Probes die Konfiguration der
Konfigurationsvariante erlauben. Die Konfigurationsvariante identifiziert den
Satz von Konfigurationsdaten, welche für diese Probe-Ausführung genutzt
werden. Die Konfigurationsvariante MUSS für jede Probe-Ausführung in dem
Service Monitoring-Datensatz abgelegt werden. Die Konfigurationsvariante MUSS
zusammen mit den dazugehörigen Konfigurationsdaten bei der Darstellung der
Probe im GUI einsehbar sein. **[\<=]**

**TIP1-A_7139 - Service Monitoring, Probes, Ausführungszeitpunkt**

Das Service Monitoring MUSS berechtigten Nutzern die vorhandenen Probes anzeigen
und für jede Probe in Kombination mit einem Konfigurationsdatensatz den
Ausführungszeitpunkt wählen lassen:

 ---> UL

Jede Probe MUSS mehrfach mit unterschiedlichen Konfigurationsdatensätzen zum
gleichen und zu verschiedenen Ausführungszeitpunkt(en) ausführbar sein. **[\<=]**

**A_13500 - Service Monitoring, Probes, Einsicht in Ausführungszeitpunkte**

Das Service Monitoring MUSS Nutzern entsprechend ihren Berechtigungen auf
Dienstinstanzen für die vorhandenen Probes Einsicht in die konfigurierten
Ausführungszeitpunkte gewährleisten. **[\<=]**

**A_13497 - Service Monitoring, Probes, Ausführungszeitpunkt pro Dienst**

Das Service Monitoring MUSS berechtigten Nutzern die vorhandenen Probes anzeigen
und für jede Probe in Kombination mit einem Konfigurationsdatensatz den/die
Ausführungszeitpunkt(e) für jede Dienstinstanz individuell wählen lassen.
**[\<=]**

**TIP1-A_7140 - Service Monitoring, Probes, parallele Ausführung**

Das Service Monitoring MUSS die parallele Ausführung von Probes erlauben. Auch
eine einzelne Probe MUSS mehrfach parallel (z.B. für verschiedene
Dienstinstanzen) ausführbar sein. **[\<=]**

**TIP1-A_7141 - Service Monitoring, Probes, Übersicht über active Probes**

Das Service Monitoring MUSS berechtigten Nutzern eine Übersicht über die
aktiven Probes mit ihren Ausführungszeitpunkten anzeigen können. Aktive
Probes sind Probes mit Ausführungszeitpunkten in der Zukunft.Das Service
Monitoring MUSS den berechtigten Nutzern die Änderung und Stornierung der
Ausführungszeitpunkte der Probes erlauben. **[\<=]**

**TIP1-A_7142 - Service Monitoring, Probes, Details zu den Probe-Messungen**

Das Service Monitoring MUSS für alle Probe Ausführungen folgende Daten erfassen

 ---> UL

Die durch Probes erfassten Daten MÜSSEN von den durch Betreiber gelieferten
Daten im Service Monitoring unterscheidbar (bei der Aggregation und in der
Darstellung) sein. **[\<=]**

**TIP1-A_7143 - Service Monitoring, Probes, Ergebnis bei komplexen Probes**

DasService MonitoringMUSSfür Probes,welche sich aus Aufrufen mehrerer
Operationen zusammensetzen, das Probe-Ergebnis folgendermaßen bilden:

Probe-Ergebnis der gesamten Probe:

 ---> UL

**[\<=]**

**TIP1-A_7144 - Service Monitoring, Probes, Unabhängige parallele Ausführung
von mehreren Probes**

DasService MonitoringMUSSdieparallele Ausführung von mehreren Probes
unterstützen. Die gegenseitige Beeinflussung vonProbesMUSS vermieden
werden(ist eine Probeblockiert oder verlangsamt,dürfen andere Probes nicht
davon beeinflusst sein). **[\<=]**

**TIP1-A_7145 - Service Monitoring, Probes, Timeouts**

Das Service Monitoring MUSS in Probes die Konfiguration von Timeouts für
aufgerufene Operationen erlauben. Für das Timeout MUSS die Angabe eines
Probe-Ergebnisses, einer Aktion  oder eines alternativen Pfades im
Probe-Ablauf möglich sein. **[\<=]**

**TIP1-A_7093 - Service Monitoring, Probes, Kartenterminals**

Das Service Monitoring MUSS für Probes den Einsatz von Smartcards ermöglichen
und dafür Kartenterminals vorsehen. **[\<=]**

In vorliegender Spezifikation müssen für alle Probes, die mit
SMC-B-Zertifikaten (OSIG und AUT) arbeiten, Kartenterminals nutzbar sein.

### 5.4.1 DNS Name Resolution

**TIP1-A_7149 - Service Monitoring, Probe DNS_Name_Resolution**

Das Service Monitoring MUSS die Probe DNS_Name_Resolution entsprechend
Tab_Service_Monitoring_Probes_DNS_Name_Resolution bereitstellen.

Tabelle8: Tab_Service_Monitoring_Probes_DNS_Name_Resolution

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
Benennung der Probe

</td><td>
DNS_Name_Resolution

</td></tr><tr><td>
Dienst

</td><td>
Namensdienst

</td></tr><tr><td>
Schnittstelle

</td><td>
I_DNS_Name_Resolution

</td></tr><tr><td>
Operation

</td><td>
get_IP_Address

</td></tr><tr><td>
Netzwerk

</td><td>
Internet  
zentrales Netz der TI

</td></tr><tr><td>
Beschreibung

</td><td>
Diese Probe wird ausgeführt für

 ---> UL

</td></tr><tr><td>
Vorbedingung

</td><td>
Für die Probe müssen folgende Informationen konfigurierbar sein:

 ---> UL

</td></tr><tr><td>
Nachbedingung

</td><td>
Im Service Monitoring müssen für die Teilschritte des Probe-Ablaufs die dort
definierten Daten für jeden DNS-Nameserver verfügbar sein.

</td></tr><tr><td rowspan="2">
Standardablauf

</td><td>
1. Die Probe ruft für jeden DNS-Nameserver TUC_SM_001_DNS_Name_Resolution mit
der FQDN, dem Flag für die DNS-Record Validierung und den Service Monitoring
Daten für diese Operation auf.

</td></tr><tr><td>
2. Rückgabe der ermittelten Daten an das Service Monitoring.  
Alternativ
können die Daten auch nach jeden Teilschritt an das Service Monitoring
übergeben werden.

</td></tr></table>

**[\<=]**

### 5.4.2 Konnektorregistrierung*

**TIP1-A_7150 - Service Monitoring, Probe Konnektorregistrierung**

Das Service Monitoring MUSS die Probe Konnektorregistrierung entsprechend
Tab_Service_Monitoring_Probes_Konnektorregistrierung bereitstellen.

Tabelle9: Tab_Service_Monitoring_Probes_Konnektorregistrierung

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
Benennung der Probe

</td><td>
Konnektorregistrierung

</td></tr><tr><td>
Dienst

</td><td>
Registrierungsserver

</td></tr><tr><td>
Schnittstelle

</td><td>
I_Registration_Service

</td></tr><tr><td>
Operation

</td><td>
registerKonnektorderegisterKonnektor

</td></tr><tr><td>
Netzwerk

</td><td>
Internet

</td></tr><tr><td>
Beschreibung

</td><td>
Diese Probe wird ausgeführt für alle Standorte des VPN-ZugD, inkl. der
Schnittstelle I_DNS_Name_Resolution (implizit für Namensraum Internet).Es wird
ein Konnektor registriert und gleich wieder deregistriert.Dieser Konnektor bzw.
die ContractID wird nur für diese Probe genutzt. In anderen Probes benötigte
VPN-Kanäle werden mit separaten Konnektorregistrierungen/ContractIDs
realisiert.

</td></tr><tr><td>
Vorbedingung

</td><td>
Der Betreiber des Registrierungsservers muss informiert sein, dass für eine
festgelegte Contract-ID durch die Probes häufig eine Registrierung und
Deregistrierung erfolgt.Der Konnektor (den die Probe simuliert) muss für alle
VPN-Zugangsdienste registriert sein.In der Probe müssen für jeden
VPN-Zugangsdienstanbieter folgende Daten konfigurierbar sein:- DNS_SERVERS_INT
(DNS-Server im Internet)- DNS_DOMAIN_VPN_ZUGD_INT (alle DNS-Domainnamen für
die Service Discovery der VPN-Konzentratoren)- ContractIDDas ZertifikatC.NK.VPN
(SMC-K) muss vorliegen (für die Erstellung des registerKonnektor Requests
nötig).Sie SMC-B muss für die Signatur des Registrierungsrequests
freigeschaltet sein.

</td></tr><tr><td>
Nachbedingung

</td><td>
Im Service Monitoring müssen die definierten Daten für jeden VPN-Konzentrator
des entsprechenden VPN-Zugangsdienstes verfügbar sein:

 ---> UL

</td></tr><tr><td rowspan="11">
Standardablauf

</td><td>
1. Ermittlung der URI aller Registrierungsservers für alle DNS-Domänen (siehe
auch TIP1-A_4825 [gemSpec_Kon]).

 ---> UL

beendet.

 ---> UL

</td></tr><tr><td>
2. Für jeden ermittelten Registrierungsservers:

</td></tr><tr><td>
2.1. Erstellung eines registerKonnektor-Requests inklusive Signatur durch SM-B
/C.HCI.OSIG mit passender ContractID für die DNS Domäne (siehe auch
TIP1-A_4390 [gemSpec_VPN_ZugD] bzw. TIP1-A_4825 [gemSpec_Kon]).

</td></tr><tr><td>
2.2. Aufruf Operation I_Registration_Service::registerKonnektor (siehe auch
TIP1-A_4390 [gemSpec_VPN_ZugD] bzw. TIP1-A_4825 [gemSpec_Kon]).

</td></tr><tr><td>
2.3. Ermittlung der Service Monitoring-Daten für Operation registerKonnektor
entsprechend Tab_Service_Monitoring_Probe_Daten und Erfassung der
Performance-Kenngröße „Bearbeitungszeit“.

</td></tr><tr><td>
2.4. Auf- und Abbau eines TI-/SIS-Tunnels entsprechend Probe „ VPN Tunnel“
als Nachweis, dass der gerade registrierte Konnektor bzw. seine Zertifikate
durch das ZugD-Netz korrekt propagiert wurden, und für die TI-Verbindungen
verwendet werden können.

</td></tr><tr><td>
2.5. Erstellung einer deRegisterKonnektorRequest-Struktur inklusive Signatur
durch SM-B /C.HCI.OSIG (siehe auch TIP1-A_4391 [gemSpec_VPN_ZugD] bzw.
TIP1-A_4827 [gemSpec_Kon])

</td></tr><tr><td>
2.6. Aufruf Operation I_Registration_Service::deRegisterKonnektor (siehe auch
TIP1-A_4827 [gemSpec_Kon]) mit der URI des Registrierungsservers.Auch wenn die
Operation registerKonnektor fehlschlägt, weil der Konnektor schon registriert
ist, muss die Operation deRegisterKonnektor ausgeführt werden (um wieder den
Ausgangszustand für die Probe herzustellen).

</td></tr><tr><td>
2.7. Ermittlung der Service Monitoring-Daten für Operation deRegisterKonnektor
entsprechend Tab_Service_Monitoring_Probe_Daten und Erfassung der
Performance-Kenngröße „Bearbeitungszeit“.

</td></tr><tr><td>
2.8. Ermittlung der Service Monitoring-Daten für die gesamte Probe entsprechend
Tab_Service_Monitoring_Probe_Daten.

</td></tr><tr><td>
3. Rückgabe der ermittelten Daten an das Service Monitoring.Alternativ können
die Daten auch nach jeden Teilschritt an das Service Monitoring übergeben
werden.

</td></tr><tr><td>
Ursachen-Analyse im Fehlerfall

</td><td>
Falls im Standardablauf bei den Aufrufen des Registrierungsservers Fehler
auftreten (es wird keine erwartete Antwort und keine Fehlermeldung geliefert),
muss die Erreichbarkeit des Dienstes mit TUC_SM_002_Erreichbarkeitsprüfung
geprüft und die Probe mit dem nächsten Registrierungsserver fortgesetzt
werden. Das „Probe-Ergebnis“ für den Aufruf dieses Registrierungsservers
wird auf

 ---> UL

gesetzt.

</td></tr></table>

**[\<=]**

### 5.4.3 VPN_Tunnel*

**TIP1-A_7151 - Service Monitoring, Probe VPN Tunnel**

Das Service Monitoring MUSS die Probe VPN-Tunnel entsprechend
Tab_Service_Monitoring_Probes_VPN_Tunnelbereitstellen.

Tabelle10: Tab_Service_Monitoring_Probes_VPN_Tunnel

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
Benennung der Probe

</td><td>
VPN Tunnel

</td></tr><tr><td>
Dienst

</td><td>
VPN-Zugangsdienst

</td></tr><tr><td>
Schnittstelle

</td><td>
I_Secure_Channel_TunnelI_IP_Transport

</td></tr><tr><td>
Operation

</td><td>
I_Secure_Channel_Tunnel::connectI_Secure_Channel_Tunnel::send_secure_IP_PacketI_Secure_Channel_Tunnel::disconnect

</td></tr><tr><td>
Netzwerk

</td><td>
Internet

</td></tr><tr><td>
Beschreibung

</td><td>
Diese Probe wird ausgeführt für alle VPN-Konzentratoren aller Standorte des
VPN-ZugD, inkl. der Schnittstelle I_DNS_Name_Resolution (implizit für
Namensraum Internet und TI).Die Probe wird für jeden VPN-Konzentrator
ausgeführt.Es wird ein VPN-Tunnel auf- und – nach Senden von Datenpaketen
– wieder abgebaut.Bei dem VPN-Tunnel-Aufbau wird die Gültigkeitsdauer der
VPN-Konzentrator-Zertifikate ermittelt und in den Service-Monitoring-Daten
gespeichert. 

</td></tr><tr><td>
Vorbedingung

</td><td>
Der Konnektor (den die Probe simuliert) muss für alle VPN-Zugangsdienste
registriert sein.Die Probe muss für jeden VPN-Zugangsdienstanbieter mit
folgenden Daten konfigurierbar sein:

 ---> UL

</td></tr><tr><td>
Nachbedingung

</td><td>
Im Service Monitoring müssen die definierten Daten den VPN-Konzentrator
verfügbar sein:

 ---> UL

In den Service-Monitoring-Daten werden die Gültigkeitsdauern der
VPN-Konzentrator-Zertifikate aktualisiert. Für jeden geprüften
VPN-Konzentrator  müssen mindestens folgende Daten erfasst werden: 

 ---> UL

Diese Daten müssen im Service Monitoring GUI in Tabellenform –
mindestens sortierbar nach Gültigkeitsende des Zertifikats und IssuerDN –
darstellbar sein. Generierung einer Warnung oder eines Alarms falls ein
Zertifikat in x Tagen (entsprechend Konfiguration) ausläuft. 

</td></tr><tr><td rowspan="10">
Standardablauf

</td><td>
1. Liste der VPN-Konzentratoren über  DNS-SRV ermitteln (siehe auch
TIP1-A_4373 [gemSpec_VPN_ZugD]).

 ---> UL

beendet.

 ---> UL

</td></tr><tr><td>
2. Für jeden ermittelten VPN-Konzentrator muss die Probe mit den folgenden
Unterpunkten einen Tunnelaufbau-Test durchführen.

</td></tr><tr><td>
2.1. Aufbau einer Verbindung zum VPN-Konzentrator (siehe auch TUC_VPN-ZD_0001
[gemSpec_VPN_ZugD] bzw. TIP1-A_4783 [gemSpec_Kon]).

</td></tr><tr><td>
2.2. Ermittlung der Service Monitoring-Daten für den Verbindungsaufbau
entsprechend Tab_Service_Monitoring_Probe_Daten und Erfassung der
Performance-Kenngröße „Bearbeitungszeit“.Analyse Server-Zertifikat 

 ---> UL

Ablage der ermittelten Daten (siehe Nachbedingungen). 

</td></tr><tr><td>
2.3. Senden eines Datenpakets über den VPN Tunnel und Empfang eines
Antwortpakets (siehe auch [gemSpec_VPN_ZugD#5.1.3]).Das kann z.B. ein Ping
(ICMP-„Echo-Request“) zu einem zentralen Dienst der TI sein.Das Senden des
Datenpakets muss mit dem Betreiber des zentralen Dienstes abgestimmt sein.

</td></tr><tr><td>
2.4. Ermittlung der Service Monitoring-Daten für die Übertragung des
Datenpakets entsprechend Tab_Service_Monitoring_Probe_Daten und Erfassung der
Performance-Kenngröße „Bearbeitungszeit“.

</td></tr><tr><td>
2.5. Abbau der Verbindung zum VPN-Konzentrator (siehe auch TIP1-A_4389
[gemSpec_VPN_ZugD]) nach der konfigurierten Zeit (Dauer der IPSec-Verbindung).
Falls die Verbindung vor der konfigurierten Zeit abbricht, MUSS dies in den
Service Monitoring-Daten erfasst werden.Auch wenn der Verbindungsaufbau zum
VPN-Konzentrator fehlgeschlagen ist, weil der Konnektor bzw. die Probe schon
eine Verbindung aufgebaut hat, muss die Operation
I_Secure_Channel_Tunnel::disconnect ausgeführt werden (um wieder den
Ausgangszustand für die Probe herzustellen).

</td></tr><tr><td>
2.6. Ermittlung der Service Monitoring-Daten für den Verbindungsabbau
entsprechend Tab_Service_Monitoring_Probe_Daten und Erfassung der
Performance-Kenngröße „Bearbeitungszeit“.

</td></tr><tr><td>
2.7. Ermittlung der Service Monitoring-Daten für den gesamtenDurchlauf derProbe
entsprechend Tab_Service_Monitoring_Probe_Daten.

</td></tr><tr><td>
3. Rückgabe der ermittelten Daten an das Service Monitoring.Alternativ können
die Daten auch nach jeden Teilschritt an das Service Monitoring übergeben
werden.

</td></tr><tr><td>
Ursachen-Analyse im Fehlerfall

</td><td>
Falls im Standardablauf bei den Aufrufen des VPN-Konzentrators Fehler auftreten
(es wird keine erwartete Antwort und keine Fehlermeldung geliefert), muss die
Erreichbarkeit des Dienstes mit TUC_SM_002_Erreichbarkeitsprüfung (TCP Ports
500 und 4500) geprüft und die Probe mit dem nächsten VPN-Konzentrator
fortgesetzt werden. Das „Probe-Ergebnis“ für diesen VPN-Konzentrator wird
auf

 ---> UL

gesetzt.

</td></tr></table>

**[\<=]**

### 5.4.4 VPN_Tunnel SIS*

**TIP1-A_7152 - Service Monitoring, Probe VPN Tunnel SIS**

Das Service Monitoring MUSS die Probe VPN Tunnel SIS entsprechend
Tab_Service_Monitoring_Probes_VPN_Tunnel mit folgenden Änderungen für
denVPN-Konzentrator SIS realisieren:

 ---> UL

 ---> UL

 ---> UL

**[\<=]**

### 5.4.5 Zeitinformation_TI

**TIP1-A_7153 - Service Monitoring, Probe Zeitinformation TI**

Das Service Monitoring MUSS die Probe Zeitinformation TI entsprechend
Tab_Service_Monitoring_Probes_Zeitinformation_TI bereitstellen.

Tabelle11: Tab_Service_Monitoring_Probes_Zeitinformation_TI

<table><tr><td colspan="2">
Element

</td><td>
Beschreibung

</td></tr><tr><td>
Benennung der Probe

</td><td colspan="2">
Zeitinformation TI

</td></tr><tr><td>
Dienst

</td><td colspan="2">
Zeitdienst

</td></tr><tr><td>
Schnittstelle

</td><td colspan="2">
I_NTP_Time_Information

</td></tr><tr><td>
Operation

</td><td colspan="2">
sync_Time

</td></tr><tr><td>
Netzwerk

</td><td colspan="2">
zentrales Netz der TI

</td></tr><tr><td>
Beschreibung

</td><td colspan="2">
Diese Probe wird ausgeführt für alle Stratum-1-NTP-Server der TI.

</td></tr><tr><td>
Vorbedingung

</td><td colspan="2">
Die NTP-Server der TI müssen für die Probe konfigurierbar sein.

</td></tr><tr><td>
Nachbedingung

</td><td colspan="2">
Im Service Monitoring müssen für die Teilschritte des Probe-Ablaufs die dort
definierten Daten für jeden NTP-Server verfügbar sein.

</td></tr><tr><td rowspan="5">
Standardablauf

</td><td colspan="2">
1. Die Probe führt für jeden NTP-Server die folgenden Schritte durch:

</td></tr><tr><td colspan="2">
1.1. Ermittlung der IP-Adresse des NTP-Servers durch eine DNS-Anfrage mit
TUC_SM_001_DNS_Name_Resolution.

</td></tr><tr><td colspan="2">
1.2. Die Probe ermittelt von dem NTP-Server die Zeit über das NTPv4 Protokoll
(siehe auch GS-A_3934 [gemSpec_Net]).

</td></tr><tr><td colspan="2">
1.3. Ermittlung der Service Monitoring-Daten für den NTP-Server entsprechend
Tab_Service_Monitoring_Probe_Daten und Erfassung der Performance-Kenngröße
„Bearbeitungszeit“

</td></tr><tr><td colspan="2">
2. Rückgabe der ermittelten Daten an das Service Monitoring.  
Alternativ
können die Daten auch nach jeden Teilschritt an das Service Monitoring
übergeben werden.

</td></tr><tr><td>
Ursachen-Analyse im Fehlerfall

</td><td colspan="2">
Falls im Standardablauf bei den Aufrufen des NTP-Servers Fehler auftreten (es
wird keine erwartete Antwort und keine Fehlermeldung geliefert), muss die
Erreichbarkeit des Dienstes mit TUC_SM_002_Erreichbarkeitsprüfung geprüft und
die Probe mit dem nächsten NTP-Server fortgesetzt werden. Das
„Probe-Ergebnis“ für diesen NTP-Server wird auf

 ---> UL

gesetzt.

</td></tr></table>

**[\<=]**

### 5.4.6 Zeitinformation_VPN_Zugangsdienst

**TIP1-A_7154 - Service Monitoring, Probe Zeitinformation VPN Zugangsdienst**

Das Service Monitoring MUSS die Probe Zeitinformation VPN-Zugangsdienst
entsprechend Tab_Service_Monitoring_Probes_Zeitinformation_TIfür die
Stratum-2-NTP-Servermit folgenden Änderungen für dieZeitinformation
VPN-Zugangsdienstrealisieren:

 ---> UL

 ---> UL

**[\<=]**

### 5.4.7 CRL Download

**TIP1-A_7155 - Service Monitoring, Probe CRL Download**

Das Service Monitoring MUSS die Probe CRL Download entsprechend
Tab_Service_Monitoring_Probes_CRL_Downloadbereitstellen.

Tabelle12: Tab_Service_Monitoring_Probes_CRL_Download

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
Benennung der Probe

</td><td>
CRL Download

</td></tr><tr><td>
Dienst

</td><td>
Trust Service Provider X.509 nonQES

</td></tr><tr><td>
Schnittstelle

</td><td>
I_CRL_Download

</td></tr><tr><td>
Operation

</td><td>
download_CRL

</td></tr><tr><td>
Netzwerk

</td><td>
Internet

</td></tr><tr><td>
Beschreibung

</td><td>
Diese Probe wird ausgeführt für alle CRL Distribution Points (CDP).

</td></tr><tr><td>
Vorbedingung

</td><td>
Die CRL Distribution Points (CDP) müssen für die Probe konfigurierbar sein. 

Die minimale zeitliche Gültigkeit der CRL (KONF_ZG_CRL) muss konfigurierbar
sein (in Minuten oder Sekunden).

</td></tr><tr><td>
Nachbedingung

</td><td>
Im Service Monitoring müssen für die Teilschritte des Probe-Ablaufs die dort
definierten Daten für jeden CRL Distribution Point (CDP) verfügbar sein.

</td></tr><tr><td rowspan="6">
Standardablauf

</td><td>
1. Die Probe führt für jeden CRL Distribution Point (CDP) die folgenden
Schritte durch:

</td></tr><tr><td>
1.1. Ermittlung der IP-Adresse des CRL Distribution Points durch
TUC_SM_001_DNS_Name_ResolutionResolution ohne DNS-Record Validierung (DNSSEC).

</td></tr><tr><td>
1.2. Die Probe lädt die CRL vom CRL Distribution Point (siehe auch TIP1-A_4248
[gemSpec_X.509_TSP]).  
Falls die CRL nicht auf dem CRL Distribution Point
vorliegt wird der gelieferte Fehlercode in den Service Monitoring Daten

erfasst.

</td></tr><tr><td>
1.3 Prüfung der CRL-Signatur

 ---> UL

</td></tr><tr><td>
1.4. Ermittlung der Service Monitoring-Daten für den CRL Distribution Point
entsprechend Tab_Service_Monitoring_Probe_Daten und Erfassung der
Performance-Kenngröße „Bearbeitungszeit“.

</td></tr><tr><td>
2. Rückgabe der ermittelten Daten an das Service Monitoring.  
Alternativ
können die Daten auch nach jeden Teilschritt an das Service Monitoring
übergeben werden.

</td></tr><tr><td>
Ursachen-Analyse im Fehlerfall

</td><td>
Falls im Standardablauf (Punkt 1.2) beim Laden der CRL Fehler auftreten (es wird
keine erwartete Antwort und keine Fehlermeldung geliefert), muss die
Erreichbarkeit des Dienstes mit TUC_SM_002_Erreichbarkeitsprüfung geprüft und
die Probe mit dem nächsten CRL Distribution Point fortgesetzt werden. Das
„Probe-Ergebnis“ für diesen CRL Distribution Point wird auf

 ---> UL

gesetzt.  
Falls im Standardablauf (Punkt 1.3) bei der CRL-Signaturprüfung
Fehler auftreten, muss das „Probe-Ergebnis“ für diesen CRL Distribution
Point auf

 ---> UL

gesetzt werden.

</td></tr></table>

**[\<=]**

### 5.4.8 TSL Download

**TIP1-A_7156 - Service Monitoring, Probe TSL Download**

Das Service Monitoring MUSS die Probe TSL Download entsprechend
Tab_Service_Monitoring_Probes_TSL_Downloadbereitstellen.

Tabelle13: Tab_Service_Monitoring_Probes_TSL_Download

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
Benennung der Probe

</td><td>
TSL Download

</td></tr><tr><td>
Dienst

</td><td>
TSL-Dienst

</td></tr><tr><td>
Schnittstelle

</td><td>
I_TSL_Download

</td></tr><tr><td>
Operation

</td><td>
download_TSL

</td></tr><tr><td>
Netzwerk

</td><td>
zentrales Netz der TI

</td></tr><tr><td>
Beschreibung

</td><td>
Diese Probe wird ausgeführt für den TSL Dienst.

</td></tr><tr><td>
Vorbedingung

</td><td>
Die URL(s) für den Download der TSL vom TSL-Dienst muss für die Probe
konfigurierbar sein.

</td></tr><tr><td>
Nachbedingung

</td><td>
Im Service Monitoring müssen für die Teilschritte des Probe-Ablaufs die dort
definierten Daten für den TSL Dienst verfügbar sein.

</td></tr><tr><td>
Standardablauf

</td><td>
1.

Die Probe führt für jede TSL-Download-Adresse die folgenden Schritte durch:

</td></tr><tr><td rowspan="4">
</td><td>
1.1.

Ermittlung der IP-Adresse des TSL-Dienstes durch TUC_SM_001_DNS_Name_Resolution.

</td></tr><tr><td>
1.2.

Die Probe lädt die TSL (siehe auch  [gemSpec_TSL#6.3.1]).

</td></tr><tr><td>
1.3. Ermittlung der Service Monitoring-Daten für den Download entsprechend
Tab_Service_Monitoring_Probe_Daten und Erfassung der Performance-Kenngröße
„Bearbeitungszeit“.

</td></tr><tr><td>
2. Rückgabe der ermittelten Daten an das Service Monitoring.

Alternativ können die Daten auch nach jeden Teilschritt an das Service
Monitoring übergeben werden.

</td></tr><tr><td>
Ursachen-Analyse im Fehlerfall

</td><td>
Falls im Standardablauf beim Laden der TSL Fehler auftreten (es wird keine
erwartete Antwort und keine Fehlermeldung geliefert), muss die Erreichbarkeit
des Dienstes mit TUC_SM_002_Erreichbarkeitsprüfung geprüft und die Probe mit
der nächsten TSL-Download-Adresse fortgesetzt werden. Das „Probe-Ergebnis“
wird für diesen TSL Download-Punkt auf

 ---> UL

gesetzt.

</td></tr></table>

**[\<=]**

### 5.4.9 TSL Download mit Prüfung

**TIP1-A_7157 - Service Monitoring, Probe TSL Download mit Prüfung**

Das Service Monitoring MUSS die Probe TSL Download mit Prüfung entsprechend
Tab_Service_Monitoring_Probes_TSL_Download bereitstellen.Folgende Abweichungen
von Tab_Service_Monitoring_Probes_TSL_Download MÜSSEN beachtet werden:

 ---> UL

**[\<=]**

### 5.4.10 TSL Download IPsecTunnel TI*

**TIP1-A_7158 - Service Monitoring, Probe TSL Download IPsecTunnel TI**

Das Service Monitoring MUSS die Probe TSL Download IPsecTunnel TI entsprechend
Tab_Service_Monitoring_Probes_TSL_Download bereitstellen. Die Probe TSL
Download IPsecTunnel TI MUSS sich wie ein Konnektor verhalten und für die
Verbindung zur TI einen IPsecTunnel nutzen.Folgende Abweichungen von
Tab_Service_Monitoring_Probes_TSL_Download MÜSSEN beachtet werden:

 ---> UL

**[\<=]**

### 5.4.11 TSL Download Internet

**TIP1-A_7159 - Service Monitoring, Probe TSL Download Internet**

Das Service Monitoring MUSS die Probe TSL Download Internet entsprechend
Tab_Service_Monitoring_Probes_TSL_Download bereitstellen. Die Probe TSL
Download Internet MUSS die TSL vom TSL-Dienst im Internet laden.Folgende
Abweichungen von Tab_Service_Monitoring_Probes_TSL_Download MÜSSEN beachtet
werden:

 ---> UL

**[\<=]**

### 5.4.12 BNetzA_VL Download

**TIP1-A_7160 - Service Monitoring, Probe BNetzA Download**

Das Service Monitoring MUSS die Probe BNetzA Download entsprechend
Tab_Service_Monitoring_Probes_BNetzA_Downloadbereitstellen.

Tabelle14: Tab_Service_Monitoring_Probes_BNetzA_Download

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
Benennung der Probe

</td><td>
BNetzA Download

</td></tr><tr><td>
Dienst

</td><td>
TSL-Dienst

</td></tr><tr><td>
Schnittstelle

</td><td>
I_BNetzA_VL_Download

</td></tr><tr><td>
Operation

</td><td>
download_VL

</td></tr><tr><td>
Netzwerk

</td><td>
zentrales Netz der TI

</td></tr><tr><td>
Beschreibung

</td><td>
Diese Probe wird ausgeführt für alle ServiceSupplyPoints für die BNetzA-VL.

</td></tr><tr><td>
Vorbedingung

</td><td>
Die Download-Adressen der BNetzA-VL müssen konfigurierbar sein.

</td></tr><tr><td>
Nachbedingung

</td><td>
Im Service Monitoring müssen für die Teilschritte des Probe-Ablaufs die dort
definierten Daten verfügbar sein.

</td></tr><tr><td rowspan="5">
Standardablauf

</td><td>
1. Die Probe führt für jede Download-Adresse der BNetzA-VL die folgenden
Schritte durch:

</td></tr><tr><td>
1.1. Ermittlung der IP-Adresse der BNetzA-VL Download-Adresse durch
TUC_SM_001_DNS_Name_Resolution.

</td></tr><tr><td>
1.2. Die Probe lädt die BNetzA-VL vom Download-Adresse (siehe auch

GS-A_5484 

[gemSpec_PKI]).

</td></tr><tr><td>
1.3. Ermittlung der Service Monitoring-Daten für den BNetzA-VL Download
entsprechend Tab_Service_Monitoring_Probe_Daten und Erfassung der
Performance-Kenngröße „Bearbeitungszeit“.

</td></tr><tr><td>
2. Rückgabe der ermittelten Daten an das Service Monitoring.

Alternativ können die Daten auch nach jeden Teilschritt an das Service
Monitoring übergeben werden.

</td></tr><tr><td>
Ursachen-Analyse im Fehlerfall

</td><td>
Falls im Standardablauf beim Laden der BNetzA-VL Fehler auftreten (es wird keine
erwartete Antwort und keine Fehlermeldung geliefert), muss die Erreichbarkeit
des Dienstes mit TUC_SM_002_Erreichbarkeitsprüfung geprüft und die Probe mit
der nächsten BNetzA-VL Adresse fortgesetzt werden. Das „Probe-Ergebnis“
wird für diese Download-Punkt der BNetzA-VL auf

 ---> UL

gesetzt.

</td></tr></table>

**[\<=]**

### 5.4.13 BNetzA Download IPsecTunnel TI*

**TIP1-A_7310 - Service Monitoring, Probe BNetzA Download IPsecTunnel TI**

Das Service Monitoring MUSS die Probe BNetzA Download IPsecTunnel TI
entsprechend Tab_Service_Monitoring_Probes_BNetzA_Downloadbereitstellen. Die
Probe BNetzA Download IPsecTunnel TI MUSS sich wie ein Konnektor verhalten und
für die Verbindung zur TI einen IPsec-Tunnel nutzen.Folgende Abweichungen von
Tab_Service_Monitoring_Probes_BNetzA_Downloadsind zu beachteten:

 ---> UL

**[\<=]**

### 5.4.14 OCSP

**TIP1-A_7311 - Service Monitoring, Probe OCSP**

Das Service Monitoring MUSS die Probe OCSP entsprechend
Tab_Service_Monitoring_Probes_OCSP bereitstellen.

Tabelle15: Tab_Service_Monitoring_Probes_OCSP

<table><tr><td colspan="2">
Element

</td><td>
Beschreibung

</td></tr><tr><td>
Benennung der Probe

</td><td colspan="2">
OCSP

</td></tr><tr><td>
Dienst

</td><td colspan="2">
TSL-Dienst

</td></tr><tr><td>
Schnittstelle

</td><td colspan="2">
I_OCSP_Status_Information

</td></tr><tr><td>
Operation

</td><td colspan="2">
check_Revocation_Status

</td></tr><tr><td>
Netzwerk

</td><td colspan="2">
zentrales Netz der TI

</td></tr><tr><td>
Beschreibung

</td><td colspan="2">
Diese Probe wird ausgeführt für alle ServiceSupplyPoints in der TSL (inkl.
alle ServiceSupplyPoints in der VL über den OCSP-Responder Proxy).

</td></tr><tr><td>
Vorbedingung

</td><td colspan="2">
In der Probe müssen folgende Daten konfigurierbar sein:

 ---> UL

Die OCSP-Responder Adressen können optional auch aus der TSL ermittelt werden.
Die manuelle Konfiguration der OCSP-Adressen muss auch in diesem Fall
alternativ möglich sein.

</td></tr><tr><td>
Nachbedingung

</td><td colspan="2">
Im Service Monitoring müssen für die Teilschritte des Probe-Ablaufs die dort
definierten Daten verfügbar sein.

</td></tr><tr><td rowspan="5">
Standardablauf

</td><td colspan="2">
1. Die Probe führt für jeden OCSP-Responder die folgenden Schritte durch:

</td></tr><tr><td colspan="2">
1.1. Ermittlung der IP-Adresse des OCSP-Responder ServiceSupplyPoints durch
TUC_SM_001_DNS_Name_Resolution.

</td></tr><tr><td colspan="2">
1.2. Die Probe führt eine OCSP-Abfrage entsprechend GS-A_4657 TUC_PKI_006
[gemSpec_PKI] durch.

</td></tr><tr><td colspan="2">
1.3. Ermittlung der Service Monitoring-Daten für die OCSP-Abfrage entsprechend
Tab_Service_Monitoring_Probe_Daten und Erfassung der Performance-Kenngröße
„Bearbeitungszeit“.

</td></tr><tr><td colspan="2">
2. Rückgabe der ermittelten Daten an das Service Monitoring.  
Alternativ
können die Daten auch nach jeden Teilschritt an das Service Monitoring
übergeben werden.

</td></tr><tr><td>
Ursachen-Analyse im Fehlerfall

</td><td colspan="2">
Falls im Standardablauf bei den OCSP Abfragen Fehler auftreten (es wird keine
erwartete Antwort und keine Fehlermeldung geliefert), muss die Erreichbarkeit
des Dienstes mit TUC_SM_002_Erreichbarkeitsprüfung geprüft und die Probe mit
dem nächsten OCSP-Responder fortgesetzt werden. Das „Probe-Ergebnis“ wird
für diesen OCSP auf

 ---> UL

gesetzt.

</td></tr></table>

**[\<=]**

### 5.4.15 OCSP IPsecTunnel TI*

**TIP1-A_7312 - Service Monitoring, Probe OCSP IPsecTunnel TI**

Das Service Monitoring MUSS die Probe OCSP IPsecTunnel TI entsprechend
Tab_Service_Monitoring_Probes_OCSP bereitstellen. Die Probe BNetzA Download
IPsecTunnel TI MUSS sich wie ein Konnektor verhalten und für die Verbindung
zur TI einen IPsecTunnel nutzen.Folgende Abweichungen von
Tab_Service_Monitoring_Probes_OCSP sind zu beachteten:

 ---> UL

 ---> UL

 ---> UL

**[\<=]**

### 5.4.16 Fachdienste VSDM

**TIP1-A_7313 - Service Monitoring, Probe Fachdienste VSDM**

DasService MonitoringMUSSdie Konfiguration derFachdiensteVSDMProbes mit jedem
Fachdienstbetreiber abstimmenund individuell fürjedenFachdienst konfigurieren. **[\<=]**

### 5.4.16.1 Fachdienst VSDM UFS

**TIP1-A_7314 - Service Monitoring, Probe UFS**

Das Service Monitoring MUSS die Probe UFS entsprechend
Tab_Service_Monitoring_Probes_UFS bereitstellen.

Tabelle16: Tab_Service Monitoring_Probes_UFS

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
Benennung der Probe

</td><td>
UFS

</td></tr><tr><td>
Dienst

</td><td>
Update Flag Service

</td></tr><tr><td>
Schnittstelle

</td><td>
I_UFS

</td></tr><tr><td>
Operation

</td><td>
GetUpdateFlags

</td></tr><tr><td>
Netzwerk

</td><td>
zentrales Netz der TI

</td></tr><tr><td>
Beschreibung

</td><td>
Diese Probe wird ausgeführt für alle UFS-Fachdienste.

</td></tr><tr><td>
Vorbedingung

</td><td>
Die Daten für alle UFS-Fachdienste – welche durch die Probe aufgerufen werden
– müssen konfigurierbar sein.  
Für den Aufruf von Operation
I_UFS::GetUpdateFlags müssen folgende Werte in der Probe für den jeweiligen
UFS konfigurierbar sein:

 ---> UL

 ---> UL

Die Probe muss sowohl eine korrekte Fachdienst-Antwort (mit UpdateID oder
ServiceReceipt) wie auch einen SOAP-Fehler mit Fehlercode (z.B. 11101) als
erwartete Antwort akzeptieren können.  
Die Probe muss über ein
TLS-Client-Zertifikat (C.FD.TLS-C) für den Verbindungsaufbau zum UFS verfügen.

</td></tr><tr><td>
Nachbedingung

</td><td>
Im Service Monitoring müssen für

die gesamte Probe und für die Teilschritte des Probe-Ablaufs die dort
definierten Daten für den UFS verfügbar sein.  
Falls der Fachdienst UFS eine
UpdateID liefert, muss sie in einem folgenden Aufruf des VSDD- oder
CMS-Fachdienstes als Eingangsparameter nutzbar sein.

</td></tr><tr><td>
Standardablauf

</td><td>
1. Für jeden Fachdienst:

</td></tr><tr><td rowspan="6">
</td><td>
1.1.

Ermittlung der IP-Adresse des UFS durch eine DNS-Anfrage (DNS-SRV Fachdienst)
mit TUC_SM_001_DNS_Name_Resolution.

</td></tr><tr><td>
1.2. Verbindungsaufbau zum UFS unter Nutzung des TLS-Client-Zertifikats.

</td></tr><tr><td>
1.3.

Senden des GetUpdateFlags Requests zum UFS unter Nutzung der
Konfigurationsparameter ICCSN und Provider ID [gemSpec_SST_FD_VSDM#3.1].

</td></tr><tr><td>
1.4. Das vom Fachdienst gelieferte Ergebnis wird mit der erwarteten
Fachdienstantwort/Fehlercode verglichen.  
Das Fachdienstergebnis ist von den
Konfigurationsparametern ProviderId  und  ICCSN abhängig.  
Für eine
nicht existierende ICCSN wird als Ergebnis ein Gematik SOAP Fault mit
Fehlercode 11101 (für die eGK mit der angegebenen ICCSN ist der aufgerufene
Dienst nicht zuständig) erwartet.  
Für eine existierende ICCSN wird eine
korrekte Fachdienst Antwort (mit UpdateID oder ServiceReceipt) erwartet.

</td></tr><tr><td>
1.5. Ermittlung der Service Monitoring-Daten für Operation GetUpdateFlags
entsprechend Tab_Service_Monitoring_Probe_Daten und Erfassung der
Performance-Kenngröße „Bearbeitungszeit“.

</td></tr><tr><td>
2. Ermittlung der Service Monitoring-Daten für die gesamte Probe und Rückgabe
aller Datensätze an das Service Monitoring entsprechend
Tab_Service_Monitoring_Probe_Daten.

</td></tr><tr><td>
Ursachen-Analyse im Fehlerfall

</td><td>
Falls im Standardablauf bei den Aufrufen des Fachdienstes Fehler auftreten (es
wird keine erwartete Antwort und keine Fehlermeldung geliefert), muss die
Erreichbarkeit des Dienstes mit TUC_SM_002_Erreichbarkeitsprüfung geprüft und
die Probe mit dem nächsten Fachdienst fortgesetzt werden. Das
„Probe-Ergebnis“ wird für diesen Fachdienst auf

 ---> UL

gesetzt.

</td></tr></table>

**[\<=]**

### 5.4.16.2 Fachdienst VSDM_VSDD_CMS

**TIP1-A_7315 - Service Monitoring, Probe VSDD_CMS**

Das Service Monitoring MUSS die Probe VSDD_CMS entsprechend
Tab_Service_Monitoring_Probes_VSDD_CMS bereitstellen.

Tabelle17: Tab_Service_Monitoring_Probes_VSDD_CMS

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
Benennung der Probe

</td><td>
VSDD_CMS

</td></tr><tr><td>
Dienst

</td><td>
VSDD- und CMS-Fachdienste

</td></tr><tr><td>
Schnittstelle

</td><td>
I_CCS

</td></tr><tr><td>
Operation

</td><td>
PerformUpdates

</td></tr><tr><td>
Netzwerk

</td><td>
zentrales Netz der TI

</td></tr><tr><td>
Beschreibung

</td><td>
Diese Probe wird ausgeführt für alle VSDD- und CMS-Fachdienste.

</td></tr><tr><td>
Vorbedingung

</td><td>
Die Daten für alle VSDD- und CMS-Fachdienste – welche durch die Probe
aufgerufen werden – müssen konfigurierbar sein.Für den Aufruf der
Operationen PerformUpdates müssen folgende Werte in der Probe individuell für
den jeweiligen Fachdienst konfigurierbar sein:

 ---> UL

 ---> UL

Die UpdateID muss konfigurierbar und aus der vorangehenden Operation
GetUpdateFlags übernehmbar sein.

 ---> UL

Die Probe muss sowohl korrekte Fachdienst-Antworten  wie auch einen
SOAP-Fehler mit Fehlercode (z.B. 12101) oder den Abbruch der Kommunikation beim
Aufbau des sicheren Kanals vom Fachdienst zur eGK als erwartete Antwort
akzeptieren.Die Probe muss über ein TLS-Client-Zertifikat (C.FD.TLS-C) für
den Verbindungsaufbau zum Fachdienst verfügen.

</td></tr><tr><td>
Nachbedingung

</td><td>
Im Service Monitoring müssen für die gesamte Probe und für die Teilschritte
des Probe-Ablaufs die dort definierten Daten verfügbar sein.

</td></tr><tr><td rowspan="7">
Standardablauf

</td><td>
1. Für jeden Fachdienst:

</td></tr><tr><td>
1.1.Ermittlung der IP-Adresse des Fachdienstes durch eine DNS-Anfrage
(DNS-SRV-Fachdienst) mit TUC_SM_001_DNS_Name_Resolution.

</td></tr><tr><td>
1.2. Verbindungsaufbau zum Fachdienst unter Nutzung des TLS-Client-Zertifikats.

</td></tr><tr><td>
1.3 Durchführung einer komplette Aktualisierung der eGK mit den SOAP-Requests
PerformUpdates und GetNextCommandPackage gemäß [gemSpec_SST_FD_VSDM#4] unter
Nutzung der Konfigurationsparameter.Abhängig von den Konfigurationsparametern
kann der Fachdienst mit einem SOAP-Fehler antworten wenn z.B. keine „echte“
ICCSN genutzt wird oder kein Update vorliegt.Falls der kartenindividuelle
symmetrische Schlüssel für die ICCSN nicht vorliegt, wird nach Senden des
PerformUpdates an den Fachdienst die Probe für diesen Fachdienst mit einem
Fehler beendet.Falls Konfigurationsparameter „Update Flag verbrauchen“ auf
„nein“ gesetzt ist, muss die Aktualisierung bei dem letzten
GetNextCommandPackage mittels dem Element Abort abgebrochen werden, so dass das
Update-Flag nach dem Aktualisierungsversuch nicht im Fachdienst UFS gelöscht
wird und erneut für eine Aktualisierung verwendet werden kann.

</td></tr><tr><td>
1.4. Das vom Fachdienst gelieferte Ergebnis wird mit der erwarteten
Fachdienstantwort/Fehlercode verglichen.Das Fachdienstergebnis ist von den
Konfigurationsparametern ServiceType, ProviderId, UpdateId und ICCSN
abhängig.Die Probe prüft, ob die Fachdienstantwort den Erwartungen (siehe
Vorbedingungen) entspricht.Falls die Fachdienstantwort von dem erwarteten
Ergebnis abweicht, wird das in den Daten für das Service Monitoring
erfasst.Zum Beispiel wird für eine nicht existierende ICCSN und UpdateId  als
Ergebnis ein gematik-SOAP-Fault mit Fehlercode 12101 (Für die angegebene
Kombination aus ICCSN und Update-Identifier liegt kein Update vor) erwartet.

</td></tr><tr><td>
1.5. Ermittlung der Service Monitoring-Daten für Operation PerformUpdates
entsprechend Tab_Service_Monitoring_Probe_Daten und Erfassung der
Performance-Kenngröße „Bearbeitungszeit“.

</td></tr><tr><td>
2. Ermittlung der Service Monitoring-Daten für die gesamte Probe und Rückgabe
aller Datensätze an das Service Monitoring entsprechend
Tab_Service_Monitoring_Probe_Daten.

</td></tr><tr><td>
Ursachen-Analyse im Fehlerfall

</td><td>
Falls im Standardablauf bei den Aufrufen des Fachdienstes Fehler auftreten (es
wird keine erwartete Antwort und keine Fehlermeldung geliefert), muss die
Erreichbarkeit des Dienstes mit TUC_SM_002_Erreichbarkeitsprüfung geprüft und
die Probe mit dem nächsten Fachdienst fortgesetzt werden. Das
„Probe-Ergebnis“ wird für diesen Fachdienst auf

 ---> UL

gesetzt.

</td></tr></table>

**[\<=]**

### 5.4.17 Intermediär VSDM*

**TIP1-A_7316 - Service Monitoring, Probe Intermediär VSDM**

Das Service Monitoring MUSS die Probe Intermediär VSDM entsprechend Tab_Service
Monitoring_Probes_Intermediär_VSDM bereitstellen.

Tabelle18: Tab_Service_Monitoring_Probes_ Intermediär_VSDM

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
Benennung der Probe

</td><td>
Intermediär VSDM

</td></tr><tr><td>
Dienst

</td><td>
Intermediär VSDM

</td></tr><tr><td>
Schnittstelle

</td><td>
I_TLS Intermediär

</td></tr><tr><td>
Operation

</td><td>
GetUpdateFlags via Intermediär

</td></tr><tr><td>
Netzwerk

</td><td>
zentrales Netz der TI

</td></tr><tr><td>
Beschreibung

</td><td>
Diese Probe wird ausgeführt für jeden Intermediär.

</td></tr><tr><td>
Vorbedingung

</td><td>
Für den Aufruf von Operation I_UFS::GetUpdateFlags via Intermediär müssen
folgende Werte in der Probe für den jeden Intermediär individuell
konfigurierbar sein.

 ---> UL

 ---> UL

Die Probe muss über eine SM-B-Prüfkarte (bzw. das AUT-Zertifikat dieser Karte
entsprechend [gemSpec_SST_VSDM#2.4.1]) für den Verbindungsaufbau zum
Intermediär verfügen.Die SM-B muss freigeschaltet sein.Weiterhin muss für
die Probe mit einem Fachdienstbetreiber die Verwendung von einem Fachdienst UFS
abgesprochen sein.

</td></tr><tr><td>
Nachbedingung

</td><td>
Im Service Monitoring müssen für die Teilschritte des Probe-Ablaufs die dort
definierten Daten verfügbar sein.

</td></tr><tr><td rowspan="7">
Standardablauf

</td><td>
1. Für jeden Intermediär:

</td></tr><tr><td>
1.1.Ermittlung der IP-Adresse des Intermediär VSDM durch eine DNS-Anfrage
(DNS-SRV Intermediär) mit TUC_SM_001_DNS_Name_Resolution.

</td></tr><tr><td>
1.2. Verbindungsaufbau zum Intermediär VSDM unterNutzung des
TLS-Client-Zertifikats (SM-B AUT Zertifikat).

</td></tr><tr><td>
1.3. Senden des GetUpdateFlags Requests zum Intermediär VSDM unter Nutzung der
Konfigurationsparameter [gemSpec_SST_FD_VSDM#3.1].

</td></tr><tr><td>
1.4. Als Ergebnis wird ein Gematik SOAP Fault mit Fehlercode 11101 (Für die eGK
mit der angegebenen ICCSN ist der aufgerufene Dienst nicht zuständig) erwartet.

</td></tr><tr><td>
1.5. Ermittlung der Service Monitoring-Daten für Operation GetUpdateFlags
entsprechend Tab_Service_Monitoring_Probe_Daten und Erfassung der
Performance-Kenngröße „Bearbeitungszeit“.

</td></tr><tr><td>
2. Ermittlung der Service Monitoring-Daten für die gesamte Probe und Rückgabe
aller Datensätze an das Service Monitoring entsprechend
Tab_Service_Monitoring_Probe_Daten.

</td></tr><tr><td>
Ursachen-Analyse im Fehlerfall

</td><td>
Falls im Standardablauf bei den Aufrufen des Intermediärs Fehler auftreten (es
wird keine erwartete Antwort und keine Fehlermeldung geliefert), muss die
Erreichbarkeit des Dienstes mit TUC_SM_002_Erreichbarkeitsprüfung geprüft und
die Probe mit dem nächsten Intermediär fortgesetzt werden. Das
„Probe-Ergebnis“ wird für diesen Intermediär auf

 ---> UL

gesetzt.

</td></tr></table>

**[\<=]**

### 5.4.18 VSDM- Intermediär VSDM IPsecTunnel TI*

**TIP1-A_7317 - Service Monitoring, Probe Intermediär VSDM IPsecTunnel TI**

Das Service Monitoring MUSS die Probe Intermediär VSDM IPsecTunnel TI
entsprechend Tab_Service_Monitoring_Probes_Intermediär_VSDM bereitstellen. Die
Probe Intermediär VSDM IPsecTunnel TI MUSS sich wie ein Konnektor verhalten
und für die Verbindung zur TI/Intermediär VSDM einen IPsecTunnel zum VPN-ZugD
nutzen.Folgende Abweichungen von
Tab_Service_Monitoring_Probes_Intermediär_VSDM müssen beachtet werden:

 ---> UL

**[\<=]**

### 5.4.19 VSDM-Intermediär VSDM Erreichbarkeit

**TIP1-A_7318 - Service Monitoring, Probe Intermediär VSDM Erreichbarkeit**

Das Service Monitoring MUSS die Probe Intermediär Erreichbarkeit entsprechend
Tab_Service_Monitoring_Probes_Intermediär_VSDM bereitstellen. Mit dieser Probe
wird die Erreichbarkeit des Intermediär VSDM geprüft. Mit einer fehlerhaften
„Provider ID“ wird die Weiterleitung der UFS Anfrage an den Fachdienst
verhindert.Folgende Abweichungen von
Tab_Service_Monitoring_Probes_Intermediär_VSDM MÜSSEN beachtet werden:

 ---> UL

 ---> UL

 ---> UL

**[\<=]**

### 5.4.20 KSRS Upload

**TIP1-A_7319 - Service Monitoring, Probe KSRS Upload**

Das Service Monitoring MUSS die Probe KSRS Upload entsprechend
Tab_Service_Monitoring_Probes_KSRS_Upload bereitstellen.

Tabelle19: Tab_Service Monitoring_Probes_KSRS_Upload

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
Benennung der Probe

</td><td>
KSRS Upload

</td></tr><tr><td>
Dienst

</td><td>
KSR

</td></tr><tr><td>
Schnittstelle

</td><td>
P_KSRS_Upload

</td></tr><tr><td>
Operation

</td><td>
Erreichbarkeit KSRS-Upload-Schnittstelle

</td></tr><tr><td>
Netzwerk

</td><td>
Internet

</td></tr><tr><td>
Beschreibung

</td><td>
Diese Probe wird ausgeführt für den KSR.

</td></tr><tr><td>
Vorbedingung

</td><td>
Für die Prüfung der Erreichbarkeit der KSRS-Upload-Schnittstelle müssen
folgende Werte in der Probe konfigurierbar sein.

 ---> UL

</td></tr><tr><td>
Nachbedingung

</td><td>
Im Service Monitoring müssen für die Teilschritte des Probe-Ablaufs die dort
definierten Daten verfügbar sein.

</td></tr><tr><td rowspan="4">
Standardablauf

</td><td>
1.

Ermittlung der IP-Adresse der KSRS-Upload-Schnittstelle durch eine DNS-Anfrage
mit

TUC_SM_001_DNS_Name_Resolution.

</td></tr><tr><td>
2. Prüfung ob die KSRS-Upload-Webseite erreichbar ist.  
Die Prüfung kann z.B.
mit einem HTTP HEAD Request [

RFC 7231#4.3.2] auf die URL der KSRS-Upload-Schnittstelle erfolgen.

</td></tr><tr><td>
3. Falls die KSRS-Upload-Webseite nicht erreichbar ist: Prüfung der
Erreichbarkeit des Dienstes mit TUC_SM_002_Erreichbarkeitsprüfung.

</td></tr><tr><td>
5. Rückgabe der ermittelten Daten für die Erreichbarkeit der
KSRS-Upload-Schnittstelle an das Service Monitoring entsprechend
Tab_Service_Monitoring_Probe_Daten und Erfassung der Kenngröße
„Verfügbarkeit“.

</td></tr></table>

**[\<=]**

### 5.4.21 KSRS Download

**TIP1-A_7320 - Service Monitoring, Probe KSRS Download**

Das Service Monitoring MUSS die Probe KSRS Download entsprechend
Tab_Service_Monitoring_Probes_KSRS_Download bereitstellen.

Tabelle20: Tab_Service_Monitoring_Probes_KSRS_Download

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
Benennung der Probe

</td><td>
KSRS Download

</td></tr><tr><td>
Dienst

</td><td>
KSR

</td></tr><tr><td>
Schnittstelle

</td><td>
I_KSRS_Download

</td></tr><tr><td>
Operation

</td><td>
I_KSRS_Download::list_UpdatesI_KSRS_Download::get_Updates

</td></tr><tr><td>
Netzwerk

</td><td>
zentrales Netz der TI

</td></tr><tr><td>
Beschreibung

</td><td>
Diese Probe wird ausgeführt für den KSR.

</td></tr><tr><td>
Vorbedingung

</td><td>
Für die Operationen von Schnittstelle I_KSRS_Download müssen folgende Werte in
der Probe konfigurierbar sein.

 ---> UL

</td></tr><tr><td>
Nachbedingung

</td><td>
Im Service Monitoring müssen für die Teilschritte des Probe-Ablaufs die dort
definierten Daten verfügbar sein.

</td></tr><tr><td rowspan="7">
Standardablauf

</td><td>
1.Ermittlung der IP-Adresse der KSRS-Download-Schnittstelle durch eine
DNS-Anfrage mit TUC_SM_001_DNS_Name_Resolution.

</td></tr><tr><td>
2. TLS Verbindungsaufbau zum Konfigurationsdienst.

</td></tr><tr><td>
3. Senden von Request I_KSRS_Download::listUpdates gemäß[gemSpec_KSR] an den
Konfigurationsdienst

</td></tr><tr><td>
4. Auswerten des Response gemäß I_KSRS_Download::get_Updates und Ermittlung
der Service Monitoring-Daten für diese Operation entsprechend
Tab_Service_Monitoring_Probe_Daten und Erfassung der Performance-Kenngröße
„Bearbeitungszeit“.

</td></tr><tr><td>
5. Download des Files „Bestandsnetze.xml“ mit I_KSRS_Download::get_Updates
gemäß[gemSpec_KSR] vom Konfigurationsdienst.Dieses File wird hier verwendet,
weil es immer auf dem KSR vorhanden ist und über die gleiche unterliegende
Operation [gemSpec_KSR#TUC_KSR_001] bereitgestellt wird.Siehe
I_KSRS_Download::get_Ext_Net_Config [gemSpec_KSR] für den Download dieses
Files.

</td></tr><tr><td>
6. Auswerten des Downloads gemäß I_KSRS_Download::get_Updates und Ermittlung
der Service Monitoring-Daten für diese Operation entsprechend
Tab_Service_Monitoring_Probe_Daten und Erfassung der Performance-Kenngröße
„Bearbeitungszeit“.

</td></tr><tr><td>
7. Speicherung der ermittelten Daten für die KSRS-Download-Schnittstelle im
Service Monitoring entsprechend Tab_Service_Monitoring_Probe_Daten.

</td></tr><tr><td>
Ursachen-Analyse im Fehlerfall

</td><td>
Falls im Standardablauf bei den Aufrufen des KSR Fehler auftreten (es wird keine
erwartete Antwort und keine Fehlermeldung geliefert), muss die Erreichbarkeit
des Dienstes mit TUC_SM_002_Erreichbarkeitsprüfung geprüft werden. Das
„Probe-Ergebnis“ wird für die jeweilige KSR Operation auf

 ---> UL

gesetzt.

</td></tr></table>

**[\<=]**

### 5.4.22 KSRS Download IPsecTunnel TI*

**TIP1-A_7321 - Service Monitoring, Probe KSRS Download IPsecTunnel TI**

Das Service Monitoring MUSS die Probe KSRS Download IPsecTunnel TI entsprechend
Tab_Service_Monitoring_Probes_KSRS_Download bereitstellen. Die Probe KSRS
Download IPsecTunnel TI MUSS sich wie ein Konnektor verhalten und für die
Verbindung zur TI/Intermediär einen IPsecTunnel nutzen.Folgende Abweichungen
von Tab_Service_Monitoring_Probes_KSRS_Download sind zu beachten:

 ---> UL

**[\<=]**

### 5.4.23 KSRS Download Bestandsnetze

**TIP1-A_7322 - Service Monitoring, Probe KSRS Download Bestandsnetze**

Das Service Monitoring MUSS die Probe KSRS Download Bestandsnetze entsprechend
Tab_Service_Monitoring_Probes_KSRS_Download_Bestandsnetze bereitstellen.

Tabelle21: Tab_Service_Monitoring_Probes_KSRS_Download_Bestandsnetze

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
Benennung der Probe

</td><td>
KSRS Download Bestandsnetze

</td></tr><tr><td>
Dienst

</td><td>
KSR

</td></tr><tr><td>
Schnittstelle

</td><td>
I_KSRS_Net_Config

</td></tr><tr><td>
Operation

</td><td>
I_KSRS_Net_Config::get_Ext_Net_Config

</td></tr><tr><td>
Netzwerk

</td><td>
zentrales Netz der TI

</td></tr><tr><td>
Beschreibung

</td><td>
Diese Probe wird ausgeführt für den KSR.

</td></tr><tr><td>
Vorbedingung

</td><td>
Für die Operationen von Schnittstelle I_KSRS_Net_Config müssen folgende Werte
in der Probe konfigurierbar sein:

 ---> UL

</td></tr><tr><td>
Nachbedingung

</td><td>
Im Service Monitoring müssen für die Teilschritte des Probe-Ablaufs die dort
definierten Daten verfügbar sein.

</td></tr><tr><td rowspan="5">
Standardablauf

</td><td>
1.Ermittlung der IP-Adresse der KSRS-Download-Schnittstelle durch eine
DNS-Anfrage mit TUC_SM_001_DNS_Name_Resolution.

</td></tr><tr><td>
2. TLS Verbindungsaufbau zum Konfigurationsdienst.

</td></tr><tr><td>
3. Download des Files „Bestandsnetze.xml“ mit
I_KSRS_Net_Config::get_Ext_Net_Config Updates gemäß[gemSpec_KSR] vom
Konfigurationsdienst.

</td></tr><tr><td>
4. Auswerten des Downloads gemäß I_KSRS_Net_Config::get_Ext_Net_Config und
Ermittlung der Service Monitoring-Daten für diese Operation entsprechend
Tab_Service_Monitoring_Probe_Daten und Erfassung der Performance-Kenngröße
„Bearbeitungszeit“.

</td></tr><tr><td>
5. Speicherung der ermittelten Daten für die KSRS-Download-Schnittstelle im
Service Monitoring entsprechend Tab_Service_Monitoring_Probe_Daten.

</td></tr><tr><td>
Ursachen-Analyse im Fehlerfall

</td><td>
Falls im Standardablauf bei den Aufrufen des KSR Fehler auftreten (es wird keine
erwartete Antwort und keine Fehlermeldung geliefert), muss die Erreichbarkeit
des Dienstes mit TUC_SM_002_Erreichbarkeitsprüfung geprüft werden. Das
„Probe-Ergebnis“ wird auf

 ---> UL

gesetzt.

</td></tr></table>

**[\<=]**

### 5.4.24 KSRS Download Bestandsnetze IPsecTunnel TI*

**TIP1-A_7323 - Service Monitoring, Probe KSRS Download Bestandsnetze
IPsecTunnel TI**

Das Service Monitoring MUSS die Probe KSRS Download Bestandsnetze IPsecTunnel TI
entsprechend Tab_Service_Monitoring_Probes_KSRS_Download_Bestandsnetze
bereitstellen. Die Probe KSRS Download IPsecTunnel TI MUSS sich wie ein
Konnektor verhalten und für die Verbindung zur TI/Intermediär einen
IPsecTunnel nutzen.Folgende Abweichungen von
Tab_Service_Monitoring_Probes_KSRS_Download_Bestandsnetze MÜSSEN beachtet
werden:

 ---> UL

**[\<=]**

### 5.4.25 Verzeichnisdienst Query

**TIP1-A_7324 - Service Monitoring, Probe Verzeichnisdienst Query**

Das Service Monitoring MUSS die Probe Verzeichnisdienst Query entsprechend
Tab_Service_Monitoring_Probes_Verzeichnisdienst_Query bereitstellen.

Tabelle22: Tab_Service_Monitoring_Probes_Verzeichnisdienst_Query

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
Benennung der Probe

</td><td>
Verzeichnisdienst Query

</td></tr><tr><td>
Dienst

</td><td>
Verzeichnisdienst

</td></tr><tr><td>
Schnittstelle

</td><td>
I_Directory_Query

</td></tr><tr><td>
Operation

</td><td>
I_Directory_Query::search_Directory

</td></tr><tr><td>
Netzwerk

</td><td>
zentrales Netz der TI

</td></tr><tr><td>
Beschreibung

</td><td>
Diese Probe wird ausgeführt für den Verzeichnisdienst.

</td></tr><tr><td>
Vorbedingung

</td><td>
Für die Operation I_Directory_Query::search_Directory müssen folgende Werte in
der Probe konfigurierbar sein:

 ---> UL

</td></tr><tr><td>
Nachbedingung

</td><td>
Im Service Monitoring müssen für die Teilschritte des Probe-Ablaufs die dort
definierten Daten verfügbar sein.

</td></tr><tr><td rowspan="6">
Standardablauf

</td><td>
1.

Ermittlung FQDN und Port des Verzeichnisdienstes analog zu TIP1-A_5517
[gemSpec_Kon#4.1.12.4.1] entsprechend Tab_Service_Monitoring_Probes_

DNS_Name_Resolution

.

</td></tr><tr><td>
2. LDAPS-Verbindungsaufbau zum Verzeichnisdienst (analog zu A_5517
[gemSpec_Kon#4.1.12.4.1]).

</td></tr><tr><td>
3. Abfrage des Verzeichnisdienstes mit den konfigurierten Eingangsdaten analog
zu TIP1-A_5518 [gemSpec_Kon#4.1.12.4.2].

</td></tr><tr><td>
4. Auswerten der Verzeichnisdienst-Antwort und Ermittlung der Service
Monitoring-Daten für diese Operation entsprechend
Tab_Service_Monitoring_Probe_Daten und Erfassung der Performance-Kenngröße
„Bearbeitungszeit“.

</td></tr><tr><td>
5. Die Probe beendet die Verbindung zum Verzeichnisdienst (analog zu A_5519
[gemSpec_Kon#4.1.12.4.3]).

</td></tr><tr><td>
6. Speicherung der ermittelten Daten für die Verzeichnisdienst I_Directory_Query

Schnittstelle im Service Monitoring entsprechend
Tab_Service_Monitoring_Probe_Daten.

</td></tr><tr><td>
Ursachen-Analyse im Fehlerfall

</td><td>
Falls im Standardablauf bei den Aufrufen des Verzeichnisdienstes Fehler
auftreten (es wird keine erwartete Antwort und keine Fehlermeldung

geliefert), muss die Erreichbarkeit des Dienstes mit
TUC_SM_002_Erreichbarkeitsprüfung geprüft werden. Das „Probe-Ergebnis“
wird für diese Verzeichnisdienst Operation auf

 ---> UL

gesetzt.

</td></tr></table>

**[\<=]**

### 5.4.26 Verzeichnisdienst Query IPsecTunnel TI*

**TIP1-A_7325 - Service Monitoring, Probe Verzeichnisdienst Query IPsecTunnel
TI**

Das Service Monitoring MUSS die Probe Verzeichnisdienst Query IPsecTunnel TI
entsprechend Tab_Service_Monitoring_Probes_Verzeichnisdienst_Query
bereitstellen. Die Probe Verzeichnisdienst Query IPsecTunnel TI MUSS sich wie
ein Konnektor verhalten und für die Verbindung zur TI/-Verzeichnisdienst einen
IPsecTunnel nutzen.Folgende Abweichungen von
Tab_Service_Monitoring_Probes_Verzeichnisdienst_Query MÜSSEN beachtet werden:

 ---> UL

**[\<=]**

### 5.4.27 Verzeichnisdienst Application_Maintenance

**TIP1-A_7326 - Service Monitoring, Probe Verzeichnisdienst Application
Maintenance**

Das Service Monitoring MUSS die Probe Verzeichnisdienst Application Maintenance
entsprechend
Tab_Service_Monitoring_Probes_Verzeichnisdienst_Application_Maintenance
bereitstellen.

Tabelle23:
Tab_Service_Monitoring_Probes_Verzeichnisdienst_Application_Maintenance

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
Benennung der Probe

</td><td>
Verzeichnisdienst Application Maintenance

</td></tr><tr><td>
Dienst

</td><td>
Verzeichnisdienst

</td></tr><tr><td>
Schnittstelle

</td><td>
I_Directory_Application_Maintenance

</td></tr><tr><td>
Operation

</td><td>
I_Directory_Application_Maintenance::add_Directory_FA-Attributes

</td></tr><tr><td>
Netzwerk

</td><td>
zentrales Netz der TI

</td></tr><tr><td>
Beschreibung

</td><td>
Diese Probe wird ausgeführt für den Verzeichnisdienst.Es wird die Webservice
(SOAP) Ausprägung der Operationen genutzt.

</td></tr><tr><td>
Vorbedingung

</td><td>
Die Probe muss beim Verzeichnisdienst für die Nutzung der Schnittstelle
registriert sein (TIP1-A_5604 [gemSpec_VZD]).Für den Aufbau einer TLS
Verbindung muss die Probe über ein C.FD.TLS-C Zertifikat verfügen
(TIP1-A_5585 [gemSpec_VZD]).Für diese Probe muss im Verzeichnisdienst ein
Basisdatensatz verfügbar sein, dem ein Fachdatensatz hinzugefügt (bzw. ein
existierender Fachdatensatz überschrieben) wird.Der Basisdatensatz muss mit
dem Verzeichnisdienst-Betreiber abgestimmt sein.Für diese Probe müssen
folgende Werte konfigurierbar sein:

 ---> UL

</td></tr><tr><td>
Nachbedingung

</td><td>
Im Service Monitoring müssen für die Teilschritte des Probe-Ablaufs die dort
definierten Daten verfügbar sein.

</td></tr><tr><td rowspan="7">
Standardablauf

</td><td>
1.Ermittlung FQDN und Port der Schnittstelle I_Directory_Application_Maintenance
vom Verzeichnisdienst entsprechend
Tab_Service_Monitoring_Probes_DNS_Name_Resolution.

</td></tr><tr><td>
2.Ermittlung der IP-Adresse des Verzeichnisdienstes durch eine DNS-Anfrage mit
TUC_SM_001_DNS_Name_Resolution.

</td></tr><tr><td>
3. TLS-Verbindungsaufbau zum Verzeichnisdienst. Die Probe muss sich mit dem
Client Zertifikat C.FD.TLS-C authentisieren (TIP1-A_5585 [gemSpec_VZD]).

</td></tr><tr><td>
4. Senden des add_Directory_FA-Attributes Requests an den Verzeichnisdienst mit
den konfigurierten Eingangsdaten.

</td></tr><tr><td>
5. Auswerten der Verzeichnisdienst Antwort und Ermittlung der Service
Monitoring-Daten für diese Operation entsprechend
Tab_Service_Monitoring_Probe_Daten und Erfassung der Performance-Kenngröße
„Bearbeitungszeit“.

</td></tr><tr><td>
6. Die Probe beendet die TLS-Verbindung zum Verzeichnisdienst.

</td></tr><tr><td>
7. Speicherung der ermittelten Daten für die Verzeichnisdienst Schnittstelle
_Directory_Application_Maintenance im Service Monitoring entsprechend
Tab_Service_Monitoring_Probe_Daten.

</td></tr><tr><td>
Ursachen-Analyse im Fehlerfall

</td><td>
Falls im Standardablauf bei den Aufrufen des Verzeichnisdienstes Fehler
auftreten (es wird keine erwartete Antwort und keine Fehlermeldung geliefert),
muss die Erreichbarkeit des Dienstes mit TUC_SM_002_Erreichbarkeitsprüfung
geprüft werden. Das „Probe-Ergebnis“ wird für diese Verzeichnisdienst
Operation auf

 ---> UL

gesetzt.

</td></tr></table>

**[\<=]**

### 5.4.28 Ablauf von Server-Zertifikaten (TI)

**A_15579 - Service Monitoring, Probe Ablauf von Server-Zertifikaten (TI)**

Das Service Monitoring MUSS die Probe Ablauf von Server-Zertifikaten (TI)
entsprechend Tab_Service_Monitoring_Probes_Ablauf_von_Server_Zertifikaten
bereitstellen.

Tabelle24: Tab_Service_Monitoring_Probes_Ablauf_von_Server_Zertifikaten

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
Benennung der Probe

</td><td>
Ablauf von Server-Zertifikaten

</td></tr><tr><td>
Dienst

</td><td>
Alle in der Probe konfigurierten Server

</td></tr><tr><td>
Schnittstelle

</td><td>
TLS

</td></tr><tr><td>
Operation

</td><td>
TLS-Verbindungsaufbau

</td></tr><tr><td>
Netzwerk

</td><td>
zentrales Netz der TI

</td></tr><tr><td>
Beschreibung

</td><td>
Diese Probe wird ausgeführt für alle in der Probe konfigurierten Server.

</td></tr><tr><td>
Vorbedingung

</td><td>
Für diese Probe müssen folgende Werte konfigurierbar sein:

 ---> UL

</td></tr><tr><td>
Nachbedingung

</td><td>
In den Service-Monitoring-Daten werden die Gültigkeitsdauern der
Server-Zertifikate aktualisiert. Für jeden geprüften Server müssen
mindestens folgende Daten erfasst werden:

 ---> UL

Diese Daten müssen im Service-Monitoring-GUI in Tabellenform – mindestens
sortierbar nach Gültigkeitsende des Zertifikats und IssuerDN – darstellbar
sein.Generierung einer Warnung oder eines Alarms falls ein Zertifikat in x
Tagen (entsprechend Konfiguration) ausläuft.Die ermittelten Daten entsprechend
Tab_Service_Monitoring_Probe_Daten  sind für die Probe im Service Monitoring
gespeichert.

</td></tr><tr><td rowspan="4">
Standardablauf

</td><td>
1. Ermittlung der IP-Adresse des Servers durch eine DNS-Anfrage mit
TUC_SM_001_DNS_Name_Resolution.

</td></tr><tr><td>
2. Für jeden konfigurierten Server:

 ---> UL

</td></tr><tr><td>
3. Analyse Server-Zertifikat

 ---> UL

</td></tr><tr><td>
4. Speicherung der ermittelten Daten für die Probe im Service Monitoring
entsprechend Tab_Service_Monitoring_Probe_Daten.

</td></tr><tr><td>
Ursachen-Analyse im Fehlerfall

</td><td>
Falls im Standardablauf bei den Aufrufen der Server Fehler auftreten (es wird
keine erwartete Antwort und keine Fehlermeldung geliefert), muss die
Erreichbarkeit des Servers mit TUC_SM_002_Erreichbarkeitsprüfung geprüft
werden. Das „Probe-Ergebnis“ wird für diesen TLS-Verbindungsaufbau auf

 ---> UL

gesetzt.

</td></tr></table>

**[\<=]**

### 5.4.29 Ablauf von Server-Zertifikaten (Internet)

**A_15580 - Service Monitoring, Probe Ablauf von Server-Zertifikaten (Internet)**

Das Service Monitoring MUSS die Probe Ablauf von Server-Zertifikaten (Internet)
entsprechend Tab_Service_Monitoring_Probes_Ablauf_von_Server_Zertifikaten
bereitstellen.Folgende Abweichungen von
Tab_Service_Monitoring_Probes_TSL_Download MÜSSEN beachtet werden:

 ---> UL

**[\<=]**

### 5.4.30 ePA - Authentisierung TI

**A_15662 - Service Monitoring, Probe ePA-Authentisierung TI**

Das Service Monitoring MUSS die Probe ePA-Authentisierung TI entsprechend
Tab_Service_Monitoring_Probes_ePA- Authentisierung_TI bereitstellen.

Tabelle25: Tab_Service_Monitoring_Probes_ePA- Authentisierung_TI

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
Benennung der Probe

</td><td>
ePA-Authentisierung TI

</td></tr><tr><td>
Dienst

</td><td>
ePA

</td></tr><tr><td>
Schnittstelle

</td><td>
I_Authentication_Insurant

</td></tr><tr><td>
Operation

</td><td>
I_Authentication_Insurant::LoginCreateChallenge

</td></tr><tr><td>
Netzwerk

</td><td>
zentrales Netz der TI

</td></tr><tr><td>
Beschreibung

</td><td>
Diese Probe wird ausgeführt für jede ePA-Instanz.

</td></tr><tr><td>
Vorbedingung

</td><td>
ePA DNS Service Records sind konfiguriert.

</td></tr><tr><td>
Nachbedingung

</td><td>
Im Service Monitoring müssen für die Teilschritte des Probe-Ablaufs die dort
definierten Daten verfügbar sein.

</td></tr><tr><td rowspan="7">
Standardablauf

</td><td>
1. Ermittlung I_Authentication_Insurant FQDN aller ePA-Aktensysteme  
Das Probe
muss die zur Kommunikation mit der Komponente Zugangsgateway für Versicherte
aller ePA-Aktensysteme notwendigen Lokalisierungsinformationen per DNS-Abfrage
nach den in [gemSpec_Aktensystem#Tab_ePA_Service Discovery] und
[gemSpec_Aktensystem#Tab_ePA_FQDN] dargestellten Parametern ermitteln.

</td></tr><tr><td>
2. Ermittlung der IP-Adresse aller Zugangsgateways durch eine DNS-Anfrage mit
TUC_SM_001_DNS_Name_Resolution.

</td></tr><tr><td>
3. TLS-Verbindungsaufbau mit Serverauthentisierung zu jedem Zugangsgateway.

</td></tr><tr><td>
4. Senden des RequestSecurityToken an jeden Zugangsgateway.

</td></tr><tr><td>
5. Auswerten der RequestSecurityTokenResponse und Ermittlung der
Service-Monitoring-Daten für diese Operation entsprechend
Tab_Service_Monitoring_Probe_Daten und Erfassung der Performance-Kenngröße
„Bearbeitungszeit“.

</td></tr><tr><td>
6. Die Probe beendet die TLS-Verbindung zum Zugangsgateway.

</td></tr><tr><td>
7. Speicherung der ermittelten Daten für die Schnittstelle
I_Authentication_Insurant im Service Monitoring entsprechend
Tab_Service_Monitoring_Probe_Daten.

</td></tr><tr><td>
Ursachen-Analyse im Fehlerfall

</td><td>
Falls im Standardablauf bei den Aufrufen des Zugangsgateways Fehler auftreten
(es wird keine erwartete Antwort und keine Fehlermeldung geliefert), muss die
Erreichbarkeit des Dienstes mit TUC_SM_002_Erreichbarkeitsprüfung geprüft
werden. Das „Probe-Ergebnis“ wird für diese ePA-Aktensystem-Operation auf

 ---> UL

gesetzt werden.

</td></tr></table>

**[\<=]**

### 5.4.31 ePA - Authentisierung Internet

**A_15694 - Service Monitoring, Probe ePA-Authentisierung Internet**

Das Service Monitoring MUSS die Probe ePA-Authentisierung Internet entsprechend
Tab_Service_Monitoring_Probes_ePA- Authentisierung bereitstellen. Die Probe
ePA-Authentisierung Internet MUSS sich wie ein ePA-Frontend des Versicherten
verhalten.Folgende Abweichungen von
Tab_Service_Monitoring_Probes_Verzeichnisdienst_Query MÜSSEN beachtet werden:

 ---> UL

**[\<=]**

### 5.4.32 ePA - Autorisierung

**A_15669 - Service Monitoring, Probe ePA-Autorisierung**

Das Service Monitoring MUSS die Probe ePA-Autorisierung entsprechend
Tab_Service_Monitoring_Probes_ePA-Autorisierung bereitstellen.

Tabelle26: Tab_Service_Monitoring_Probes_ePA-Autorisierung

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
Benennung der Probe

</td><td>
ePA-Autorisierung

</td></tr><tr><td>
Dienst

</td><td>
ePA

</td></tr><tr><td>
Schnittstelle

</td><td>
I_Authorization

</td></tr><tr><td>
Operation

</td><td>
I_Authorization::getAuthorizationKey

</td></tr><tr><td>
Netzwerk

</td><td>
zentrales Netz der TI

</td></tr><tr><td>
Beschreibung

</td><td>
Diese Probe wird ausgeführt für jede ePA-Instanz.

</td></tr><tr><td>
Vorbedingung

</td><td>
ePA DNS Service Records sind konfiguriert.Für diese Probe müssen folgende
Werte für Operation getAuthorizationKey pro ePA-Anbieter (identifiziert durch
homeCommunityID) konfigurierbar sein:

 ---> UL

</td></tr><tr><td>
Nachbedingung

</td><td>
Im Service Monitoring müssen für die Teilschritte des Probe-Ablaufs die dort
definierten Daten für jede ePA-Instanz verfügbar sein.

</td></tr><tr><td rowspan="7">
Standardablauf

</td><td>
1. Ermittlung aller ePA-Autorisierungs-DiensteDas Probe muss die zur
Kommunikation mit der Komponente Autorisierungs-Dienste aller ePA-Aktensysteme
notwendigen Lokalisierungsinformationen per DNS-Abfrage nach den in
[gemSpec_Aktensystem#Tab_ePA_Service Discovery] und
[gemSpec_Aktensystem#Tab_ePA_FQDN] dargestellten Parametern ermitteln.

</td></tr><tr><td>
2. Ermittlung der IP-Adresse aller Autorisierungs-Dienste durch eine DNS-Anfrage
mit TUC_SM_001_DNS_Name_Resolution.

</td></tr><tr><td>
3. TLS-Verbindungsaufbau mit Serverauthentisierung zu jedem
Autorisierungs-Dienst.

</td></tr><tr><td>
4. Senden des getAuthorizationKey (mit den Konfigurationsparametern für diese
homeCommunityID) an jeden Autorisierungs-Dienst.Falls für einen ePA-Anbieter
keine Konfigurationsdaten vorhanden sind, wird das „Probe-Ergebnis“ für
diesen ePA-Anbieter auf

 ---> UL

gesetzt.

</td></tr><tr><td>
5. Auswerten der GetAuthorizationKeyResponse und Ermittlung der
Service-Monitoring-Daten für diese Operation entsprechend
Tab_Service_Monitoring_Probe_Daten und Erfassung der Performance-Kenngröße
„Bearbeitungszeit“.

</td></tr><tr><td>
6. Die Probe beendet die TLS-Verbindung zum Autorisierungs-Dienst.

</td></tr><tr><td>
7. Speicherung der ermittelten Daten für die Schnittstelle I_Authorization im
Service Monitoring entsprechend Tab_Service_Monitoring_Probe_Daten.

</td></tr><tr><td>
Ursachen-Analyse im Fehlerfall

</td><td>
Falls im Standardablauf bei den Aufrufen des-ePA Autorisierungs-Dienstes Fehler
auftreten (es wird keine erwartete Antwort und keine Fehlermeldung geliefert),
muss die Erreichbarkeit des Dienstes mit TUC_SM_002_Erreichbarkeitsprüfung
geprüft werden. Das „Probe-Ergebnis“ wird für diese
ePA-Aktensystem-Operation auf

 ---> UL

gesetzt werden.

</td></tr></table>

**[\<=]**

### 5.4.33 ePA - I_Authorization_Management::checkRecordExists

**A_16186 - Service Monitoring, Probe ePA -
I_Authorization_Management::checkRecordExists**

Das Service Monitoring MUSS die Probe ePA -
I_Authorization_Management::checkRecordExists entsprechend
Tab_Service_Monitoring_Probes_ePA-I_Authorization_Management::checkRecordExists
bereitstellen.

Tabelle27:
Tab_Service_Monitoring_Probes_ePA-I_Authorization_Management::checkRecordExists

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
Benennung der Probe

</td><td>
ePA - I_Authorization_Management::checkRecordExists

</td></tr><tr><td>
Dienst

</td><td>
ePA

</td></tr><tr><td>
Schnittstelle

</td><td>
I_Authorization_Management

</td></tr><tr><td>
Operation

</td><td>
I_Authorization_Management::checkRecordExists

</td></tr><tr><td>
Netzwerk

</td><td>
zentrales Netz der TI

</td></tr><tr><td>
Beschreibung

</td><td>
Diese Probewird ausgeführt für jede ePA-Instanz.

</td></tr><tr><td>
Vorbedingung

</td><td>
ePA DNS Service Records sind konfiguriert.Für diese Probe müssen folgende
Werte für Operation checkRecordExists pro ePA-Anbieter (identifiziert durch
homeCommunityID) konfigurierbar sein:

 ---> UL

</td></tr><tr><td>
Nachbedingung

</td><td>
Im Service Monitoring müssen für die Teilschritte des Probe-Ablaufs die dort
definierten Daten für jede ePA-Instanz verfügbar sein.

</td></tr><tr><td rowspan="7">
Standardablauf

</td><td>
1. Ermittlung aller ePA-Autorisierungs-DiensteDas Probe muss die zur
Kommunikation mit der Komponente Autorisierungs-Dienste aller ePA-Aktensysteme
notwendigen Lokalisierungsinformationen perDNS-Abfrage nach den in
[gemSpec_Aktensystem#Tab_ePA_Service Discovery] und
[gemSpec_Aktensystem#Tab_ePA_FQDN] dargestellten Parametern ermitteln.

</td></tr><tr><td>
2. Ermittlung der IP-Adresse aller Autorisierungs-Dienste durch eine DNS-Anfrage
mit TUC_SM_001_DNS_Name_Resolution.

</td></tr><tr><td>
3. TLS-Verbindungsaufbau mit Serverauthentisierung zu jedem
Autorisierungs-Dienst.

</td></tr><tr><td>
4. Senden des checkRecordExists (mit den Konfigurationsparametern für diese
homeCommunityID) an jeden Autorisierungs-Dienst.Falls für einen ePA-Anbieter
keine Konfigurationsdaten vorhanden sind, wird das „Probe-Ergebnis“ für
diesen ePA-Anbieter auf

 ---> UL

gesetzt.

</td></tr><tr><td>
5. Auswerten der checkRecordExistsResponse und Ermittlung der
Service-Monitoring-Daten für diese Operation entsprechend
Tab_Service_Monitoring_Probe_Daten und Erfassung der Performance-Kenngröße
„Bearbeitungszeit“.

</td></tr><tr><td>
6. Die Probe beendet die TLS-Verbindung zum Autorisierungs-Dienst.

</td></tr><tr><td>
7. Speicherung der ermittelten Daten für die Schnittstelle I_Authorization im
Service Monitoring entsprechend Tab_Service_Monitoring_Probe_Daten.

</td></tr><tr><td>
Ursachen-Analyse im Fehlerfall

</td><td>
Falls im Standardablauf bei den Aufrufen des ePA-Autorisierungs-Dienstes Fehler
auftreten (es wird keine erwartete Antwort und keine Fehlermeldung geliefert),
muss die Erreichbarkeit des Dienstes mit TUC_SM_002_Erreichbarkeitsprüfung
geprüft werden. Das „Probe-Ergebnis“ wird für diese
ePA-Aktensystem-Operation auf

 ---> UL

gesetzt werden.

</td></tr></table>

**[\<=]**

### 5.4.34 ePA - Dokumentenverwaltung

**A_15672 - Service Monitoring, Probe ePA-Dokumentenverwaltung**

Das Service Monitoring MUSS die Probe ePA-Dokumentenverwaltung ePA-Autorisierung
entsprechend Tab_Service_Monitoring_Probes_ePA-Dokumentenverwaltung
Autorisierung bereitstellen.

Tabelle28: Tab_Service_Monitoring_Probes_ePA_Dokumentenverwaltung

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
Benennung

der Probe

</td><td>
ePA-Dokumentenverwaltung

</td></tr><tr><td>
Dienst

</td><td>
ePA

</td></tr><tr><td>
Schnittstelle

</td><td>
I_Account_Management

</td></tr><tr><td>
Operation

</td><td>
I_Account_Management - Aufbau eines sicheren Kanals auf Anwendungsebene

</td></tr><tr><td>
Netzwerk

</td><td>
zentrales Netz der TI

</td></tr><tr><td>
Beschreibung

</td><td>
Diese Probe wird ausgeführt für jede ePA-Instanz.

</td></tr><tr><td>
Vorbedingung

</td><td>
ePA DNS Service Records sind konfiguriert.  
Für diese Probe müssen folgende
Werte für den Aufbau eines sicheren Kanals auf Anwendungsebene pro
ePA-Anbieter (identifiziert durch homeCommunityID) konfigurierbar sein:

 ---> UL

</td></tr><tr><td>
Nachbedingung

</td><td>
Im Service Monitoring müssen für die Teilschritte des Probe-Ablaufs die dort
definierten Daten verfügbar sein.

</td></tr><tr><td rowspan="7">
Standardablauf

</td><td>
1. Ermittlung aller ePA-Dokumentenverwaltungs-Dienste  
Das Probe muss die zur
Kommunikation mit der Komponente Dokumentenverwaltung-Dienste aller
ePA-Aktensysteme notwendigen Lokalisierungsinformationen per DNS-Abfrage nach
den in [gemSpec_Aktensystem#Tab_ePA_Service Discovery] und
[gemSpec_Aktensystem#Tab_ePA_FQDN] dargestellten Parametern ermitteln.

</td></tr><tr><td>
2. Ermittlung der IP-Adresse aller Dokumentenverwaltungs-Dienste durch eine
DNS-Anfrage mit TUC_SM_001_DNS_Name_Resolution.

</td></tr><tr><td>
3. TLS-Verbindungsaufbau mit Serverauthentisierung zu jedem
Dokumentenverwaltungs-Dienst.

</td></tr><tr><td>
4. Aufbau eines sicheren Kanals auf Anwendungsebene (mit den
Konfigurationsparametern für diese homeCommunityID) zu jedem
Dokumentenverwaltungs-Dienst analog zu Anforderungen A_15199 und A_15200. 

Falls für einen ePA-Anbieter keine Konfigurationsdaten vorhanden sind, wird
das „Probe-Ergebnis“ für diesen ePA-Anbieter auf

 ---> UL

gesetzt.

</td></tr><tr><td>
5. Auswerten der Antwort auf den Verbindungsaufbau und Ermittlung der
Service-Monitoring-Daten für diese Operation entsprechend
Tab_Service_Monitoring_Probe_Daten und Erfassung der Performance-Kenngröße
„Bearbeitungszeit“.  
Falls der sichere Kanal erfolgreich aufgebaut wurde,
wird er wieder abgebaut.

</td></tr><tr><td>
6. Die Probe beendet die TLS-Verbindung zum ePA-Dokumentenverwaltungs-Dienst.

</td></tr><tr><td>
7. Speicherung der ermittelten Daten für die Schnittstelle I_Account_Management
im Service Monitoring entsprechend Tab_Service_Monitoring_Probe_Daten.

</td></tr><tr><td>
Ursachen-Analyse im Fehlerfall

</td><td>
Falls im Standardablauf bei den Aufrufen des ePA-Dokumentenverwaltungs-Dienstes
Fehler auftreten (es wird keine erwartete Antwort und keine Fehlermeldung
geliefert), muss die Erreichbarkeit des Dienstes mit
TUC_SM_002_Erreichbarkeitsprüfung geprüft werden. Das „Probe-Ergebnis“
wird für diese ePA-Aktensystem-Operation auf

 ---> UL

gesetzt.

</td></tr></table>

**[\<=]**

### 5.4.35 ePA – Verfügbarkeitsmonitoring

**A_18381 - Service Monitoring, Probe ePA-Verfügbarkeitsmonitoring**

Das Service Monitoring MUSS die Probe ePA-Verfügbarkeitsmonitoring entsprechend
Tab_Service_Monitoring_Probes_ePA-Verfügbarkeitsmonitoring bereitstellen.

Tabelle29: Tab_Service_Monitoring_Probes_ePA-Verfügbarkeitsmonitoring

<table><tr><td>
Element

</td><td>
Beschreibung

</td></tr><tr><td>
Benennung der Probe

</td><td>
ePA-Verfügbarkeitsmonitoring

</td></tr><tr><td>
Dienst

</td><td>
ePA

</td></tr><tr><td>
Netzwerk

</td><td>
Internet

</td></tr><tr><td>
Beschreibung

</td><td>
Diese Probe wird ausgeführt für jede ePA-Instanz.

</td></tr><tr><td>
Vorbedingung

</td><td>
Kartenterminal mit eGK-Prüfkarten.

eGK MRPIN.home muss nötigen Sicherheitszustand haben.

ePA DNS Service Records sind konfiguriert.

Für jedes ePA-Aktensystem ist ein RecordIdentifier konfiguriert.

In jedem ePA-Aktensystem ist ein abrufbares Dokument eingestellt.

</td></tr><tr><td>
Nachbedingung

</td><td>
Im Service Monitoring müssen für die Teilschritte des Probe-Ablaufs die dort
definierten Daten verfügbar sein.

</td></tr><tr><td rowspan="6">
Standardablauf

</td><td>
1. Ermittlung I_Authentication_Insurant FQDN aller ePA-Aktensysteme  
Das Probe
muss die zur Kommunikation mit der Komponente Zugangsgateway für Versicherte
aller ePA-Aktensysteme notwendigen Lokalisierungsinformationen per DNS-Abfrage
nach den in [gemSpec_Aktensystem#Tab_ePA_Service Discovery] und
[gemSpec_Aktensystem#Tab_ePA_FQDN] dargestellten Parametern ermitteln.

</td></tr><tr><td>
2. Das Login erfolgt entsprechend Anwendungsfall "UC 1.1 - Login durch einen
Versicherten" aus [gemSysL_ePA].

 

Aktivitäten im Ablauf

 ---> OL

Die Authentisierung erfolgt mittels Prüfkarte im Kartenterminal. Falls die
MRPIN.home nicht den nötigen Sicherheitszustand hat, wird die Probe mit Fehl

er 7111 been

det.

Wenn nach der Aktivität "Autorisieren des Nutzers" ein Autorisierungstoken mit
RecordState = REGISTERED oder REGISTERED_FOR_MIGRATION vorliegt, dann wird die
Probe mit Fehler 7107 abgebrochen und der Anwendungsfall "Logout Aktensession"
gestartet.

</td></tr><tr><td>
3. Das Suchen des konfigurierten Dokuments aus dem Aktenkonto erfolgt
entsprechend Anwendungsfall "UC 4.10 - Dokumente durch einen Versicherten
anzeigen" aus [gemSysL_ePA].

 

4. Das Herunterladen des konfigurierten Dokuments aus dem Aktenkonto erfolgt
entsprechend Anwendungsfall "UC 4.10 - Dokumente durch einen Versicherten
anzeigen" aus [gemSysL_ePA].

</td></tr><tr><td>
5. Das Logout aus der Aktensession erfolgt entsprechend Anwendungsfall "UC 1.3 -
Logout durch einen Nutzer" aus [gemSysL_ePA].

 

Aktivitäten im Ablauf

 ---> OL

</td></tr><tr><td>
6. Auswerten der RequestSecurityTokenResponse und Ermittlung der
Service-Monitoring-Daten für diese Operation entsprechend
Tab_Service_Monitoring_Probe_Daten und Erfassung der Performance-Kenngröße
„Bearbeitungszeit“.

</td></tr><tr><td>
7. Speicherung der ermittelten Daten für jede ePA-Instanz und Schnittstelle im
Service Monitoring entsprechend Tab_Service_Monitoring_Probe_Daten.

</td></tr><tr><td>
Ursachen-Analyse im Fehlerfall

</td><td>
Falls im Standardablauf bei den Aufrufen des Zugangsgateways Fehler auftreten
(es wird keine erwartete Antwort und keine Fehlermeldung geliefert), muss die
Erreichbarkeit des Dienstes mit TUC_SM_002_Erreichbarkeitsprüfung geprüft
werden. Das „Probe-Ergebnis“ muss für diese ePA-Aktensystem-Operation auf

 ---> UL

gesetzt werden.

</td></tr></table>

**[\<=]**

### 5.4.36 ePA -Schlüsselgenerierungsdienst

**A_17849 - Service Monitoring, Probe ePA-Schlüsselgenerierungsdienst**

Das Service Monitoring MUSS die Probe ePA-Schlüsselgenerierungsdienst
entsprechend Tab_Service_Monitoring_Probes_ePA-Schlüsselgenerierungsdienst
bereitstellen.

Tabelle30: Tab_Service_Monitoring_Probes_ePA_Schlüsselgenerierungsdienst

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
Benennung der Probe

</td><td>
ePA-Schlüsselgenerierungsdienst

</td></tr><tr><td>
Dienst

</td><td>
ePA-Schlüsselgenerierungsdienst

</td></tr><tr><td>
Schnittstelle

</td><td>
I_GetPublicKey  
I_KeyDerivation  
I_GetEventLog

</td></tr><tr><td>
Operation

</td><td>
GetPublicKey - Lesen des öffentlichen ECDH-Schlüssels  
KeyDerivation -
Schlüsselableitung  
GetEventLog - Auslesen des Ereignisprotokolls des
Versicherten

</td></tr><tr><td>
Netzwerk

</td><td>
zentrales Netz der TI

</td></tr><tr><td>
Beschreibung

</td><td>
Diese Probe wird ausgeführt für jede Instanz des
ePA-Schlüsselgenerierungsdienstes.

</td></tr><tr><td>
Vorbedingung

</td><td>
ePA DNS Service Records sind konfiguriert.  
Für diese Probe müssen folgende
Werte für den Aufbau eines sicheren Kanals auf Anwendungsebene pro
ePA-Schlüsselgenerierungsdienst konfigurierbar sein:

 ---> UL

{ "Command"      : "GetPublicKey",  
  "Certificate"  : "",  
 
"OCSPResponse" : ""  }  
oder  
{ "Command"       : "KeyDerivation",  
 
"PublicKeyECDH" : "",  
  "Signature"     : "",  
  "Certificate"   :
"",  
  "OCSPResponse"  : "",     
  "Message"       : "" }  
oder  
{
"Command"       : "GetEventLog",  
  "PublicKeyECDH" : "",  
 
"Signature"     : "",  
  "Certificate"   : "",  
  "OCSPResponse"  :
"",     
  "Message"       : "" }

 ---> UL

{ "Status" : "certificate not valid" }  
  oder  
{ "Status" : "request not
valid" }

</td></tr><tr><td>
Nachbedingung

</td><td>
Im Service Monitoring müssen für die Teilschritte des Probe-Ablaufs die dort
definierten Daten verfügbar sein.

</td></tr><tr><td rowspan="7">
Standardablauf

</td><td>
1. Ermittlung aller ePA-Schlüsselgenerierungsdienste  
Die Probe muss alle die
zur Kommunikation mit der Komponente Schlüsselgenerierungsdienst notwendigen
Lokalisierungsinformationen per DNS-Abfrage nach den in
[gemSpec_Aktensystem#Tab_ePA_Service Discovery] und
[gemSpec_Aktensystem#Tab_ePA_FQDN] dargestellten Parametern ermitteln.

</td></tr><tr><td>
2. Ermittlung der IP-Adresse allerSchlüsselgenerierungsdienste durch eine
DNS-Anfrage mit TUC_SM_001_DNS_Name_Resolution.

</td></tr><tr><td>
3. TLS-Verbindungsaufbau mit Serverauthentisierung zu jedem
Schlüsselgenerierungsdienst.

</td></tr><tr><td>
4. Senden des GetPublicKey  
Es wird ein HTTP POST mit dem konfigurierten Body
für Operation GetPublicKey gesendet.

</td></tr><tr><td>
5. Auswerten der Antwort auf den Request und Ermittlung der
Service-Monitoring-Daten für diese Operation entsprechend
Tab_Service_Monitoring_Probe_Daten und Erfassung der Performance-Kenngröße
„Bearbeitungszeit“.

</td></tr><tr><td>
6. Die Probe beendet die TLS-Verbindung zum ePA Schlüsselgenerierungsdienst.

</td></tr><tr><td>
7. Speicherung der ermittelten Daten für die Schnittstelle I_GetPublicKey im
Service Monitoring entsprechend Tab_Service_Monitoring_Probe_Daten.

</td></tr><tr><td>
Ursachen-Analyse im Fehlerfall

</td><td>
Falls im Standardablauf bei den Aufrufen des ePA -Schlüsselgenerierungsdienst
Fehler auftreten (es wird keine erwartete Antwort und keine Fehlermeldung
geliefert), muss die Erreichbarkeit des Dienstes mit
TUC_SM_002_Erreichbarkeitsprüfung geprüft werden. Das „Probe-Ergebnis“
wird für diese ePA Schlüsselgenerierungsdienst Operation auf

 ---> UL

gesetzt.

</td></tr></table>

**[\<=]**

### 5.4.37 aAdG-NetG

Die TI agiert für die aAdG-NetG-Kommunikation als Transportnetz. Die
Überwachung dieser Transportnetz-Funktionalität ist Aufgabe der Probe
"aAdG-NetG Erreichbarkeit".

Für  diese  Prüfung  wird  die  Probe "aAdG-NetG Erreichbarkeit" für
das aAdG-NetG-Netz konfiguriert und periodisch ausgeführt. Für
jedes aAdG-NetG-Netz wird ein  –  vom jeweiligen Netzanbieter genannter 
–  Endpunkt (IP-Adresse oder URL) in der Probe konfiguriert.

Es obliegt dem Betreiber des aAdG-NetG-Netzes, ob dieser eine Probe zur
Erreichbarkeit möchte.

Zudem soll bei der Etablierung neuer Kommunikationsziele im aAdG-NetG-Netz die
Verbindung im Rahmen der Einrichtung überprüft werden können.

**A_18400 - Service Monitoring, Probe aAdG-NetG Erreichbarkeit**

Das Service Monitoring MUSS die Probe aAdG-NetG Erreichbarkeit entsprechend
Tab_Service_Monitoring_Probes_aAdG-NetG_Erreichbarkeit bereitstellen, sofern
eine Probe durch den Betreiber des aAdG-NetG-Netzes gewünscht und dieser einen
Endpunkt für die Probe benannt hat.

Tabelle31: Tab_Service_Monitoring_Probes_aAdG-NetG_Erreichbarkeit

<table><tr><th>
Element

</th><th>
Beschreibung

</th></tr><tr><td>
Benennung der Probe

</td><td>
aAdG-NetG Erreichbarkeit

</td></tr><tr><td>
Dienst

</td><td>
aAdG-NetG

</td></tr><tr><td>
Schnittstelle

</td><td>
I_IP_Transport

</td></tr><tr><td>
Operation

</td><td>
ICMP Request

HTTPS GET

</td></tr><tr><td>
Netzwerk

</td><td>
zentrales Netz der TI

</td></tr><tr><td>
Beschreibung

</td><td>
Diese Probe wird ausgeführt für alle aAdG-NetG-Netze.

</td></tr><tr><td>
Vorbedingung

</td><td>
IP-Adressen bzw. URLs aus dem aAdG-NetG müssen für die Probe konfiguriert sein.

</td></tr><tr><td>
Nachbedingung

</td><td>
Im Service Monitoring müssen für die Teilschritte des Probe-Ablaufs die dort
definierten Daten für jedes aAdG-NetG verfügbar sein.

</td></tr><tr><td rowspan="5">
Standardablauf

</td><td>
1. Die Probe führt für jedes konfigurierte aAdG-NetG die folgenden Schritte
durch:

</td></tr><tr><td>
1.1. Für alle konfigurierten URLs:

·        

TUC_SM_001_DNS_Name_ResolutionResolution ohne DNS-Record Validierung (DNSSEC)
für die URL.

·        

Aufruf der URL und Auswertung der Response (Laufzeit und Erhalt werden erfasst)

</td></tr><tr><td>
1.2 Für alle konfigurierten IP-Adressen: ICMP Request auf die IP-Adresse und
Auswertung der Response (Laufzeit und Erhalt werden erfasst)

</td></tr><tr><td>
1.3. Ermittlung der Service-Monitoring-Daten für alle konfigurierten
IP-Adressen und URLs entsprechend Tab_Service_Monitoring_Probe_Daten und
Erfassung der Performance-Kenngröße „Bearbeitungszeit“.

</td></tr><tr><td>
2. Rückgabe der ermittelten Daten an das Service Monitoring.  
Alternativ
können die Daten auch nach jeden Teilschritt an das Service Monitoring
übergeben werden.

</td></tr><tr><td>
Ursachen-Analyse im Fehlerfall

</td><td>
Falls im Standardablauf (Punkt 1 inklusive Unterpunkte) Fehler auftreten (es
wird keine erwartete Antwort und keine Fehlermeldung geliefert), muss die
Erreichbarkeit des Dienstes mit TUC_SM_002_Erreichbarkeitsprüfung geprüft und
die Probe mit der nächsten konfigurierten IP-Adresse oder URL fortgesetzt
werden. Das „Probe-Ergebnis“ wird auf

 ---> UL

gesetzt.

</td></tr></table>

**[\<=]**

### 5.4.38 Erfassung von Service Monitoring-Daten in Probes

**TIP1-A_7327 - Service Monitoring, Probes, Datenerfassung**

Das Service Monitoring MUSS die in Probes ermittelten Daten im Service
Monitoring ablegen. Im Service Monitoring MÜSSEN für

 ---> UL

erfasst werden.

In den internen Service Monitoring Daten MUSS die Zugehörigkeit aller
geschriebenen Datensätze zu Probe -Ausführungszeitpunkten erfasst und für
Aggregationsregeln auswertbar sein. **[\<=]**

<table><tr><th>
Monitoring Daten

</th><th>
Datensatz

</th><th>
Einheit

</th><th>
Erläuterung

</th></tr><tr><td>
ProbeID

</td><td>
P & O

</td><td>
 

</td><td>
Identifikation der Probe  
Wird bei Erstellung der Probe vergeben und muss
eindeutig sein.  
Probe-Datensatz: Dient der Identifikation der Probe 

Operation-Datensatz: Zeigt, durch welche Probe die Daten ermittelt wurden.
Falls nicht vorhanden, wurden die Daten nicht durch eine Probe ermittelt.

</td></tr><tr><td>
ProbeBeschreibung

</td><td>
</td><td>
 

</td><td>
Beschreibung der Probe  
Wird bei Erstellung der Probe erstellt.  
Ist im GUI
anzeigbar.

</td></tr><tr><td>
Betriebsumgebung

</td><td>
P & O

</td><td>
 

</td><td>
RU/TU/PU  
Die Umgebung muss nicht in jedem Datensatz enthalten sein. Die
Datensätze müssen aber der Umgebung zuordenbar sein.

</td></tr><tr><td>
TeilnehmerID

</td><td>
O

</td><td>
 

</td><td>
ID des Teilnehmers wie in TI-ITSM für den diese Operation aufgerufen wurde

</td></tr><tr><td>
Dienstinstanz

</td><td>
O

</td><td>
 

</td><td>
Operation-Datensatz: Instanz des Dienstes für den die Operation ausgeführt
wird.

</td></tr><tr><td>
ProductType

</td><td>
O

</td><td>
 

</td><td>
ID zu Eintrag aus Tab_gemKPT_Betr_Produkttypen

</td></tr><tr><td>
Schnittstelle

</td><td>
O

</td><td>
 

</td><td>
ID zu Eintrag aus Tab_gemKPT_Betr_Schnittstellenoperationen

</td></tr><tr><td>
Zertifikatstyp

</td><td>
O

</td><td>
 

</td><td>
ID zu Eintrag aus Tab_gemKPT_Betr_Zertifikatstypen

</td></tr><tr><td>
AnfrageQuelle

</td><td>
O

</td><td>
 

</td><td>
Angabe, ob die Schnittstelle, zu der reportet wird, in der TI oder im Internet
bereitgestellt wird. Werte aus Tab_gemKPT_Betr_Aufrufquelle

</td></tr><tr><td>
</td><td>
</td><td>
</td><td>
</td></tr><tr><td>
Zeitstempel

</td><td>
P & O

</td><td>
ms

</td><td>
Probe-Datensatz: Zeitpunkt der Probe-Ausführung  
Operation-Datensatz: Zeigt
zusammen mit der ProbeID durch welche Probe-Ausführung die Daten ermittelt
wurden

</td></tr><tr><td>
Bearbeitungszeit

</td><td>
P & O

</td><td>
ms

</td><td>
Probe Datensatz: Ausführungsdauer der Probe  
Operation-Datensatz:
Ausführungsdauer der Operation. Wird als Performance-Kenngröße erfasst.

</td></tr><tr><td>
Ergebnis

</td><td>
P & O

</td><td>
 

</td><td>
Probe-Datensatz: Ergebnis der Probe-Ausführung  
Operation Datensatz: Ergebnis
der Operation  
Das Ergebnis kann auch „Erfolgreich“ sein, wenn das
erwartete Ergebnis einer Einzeloperation ein Fehler war.

</td></tr><tr><td>
Mitschnitt der Kommunikation

</td><td>
P

</td><td>
 

</td><td>
Aufzeichnung der gesamten Kommunikation der Probe mit den Diensten für die
Probe-Ausführung,  
im Fehlerfall auch für die Ursachen-Analyse.  
Die
Operation-Datensätze enthalten keinen Mitschnitt der Kommunikation, verweisen
aber auf die aufrufende ProbeAusführung (wo diese Daten zu finden sind).

</td></tr></table>

Legende:

 ---> UL

### 5.5 Performance-Kenngrößen

Performance-Kenngrößen werden

 ---> UL

**TIP1-A_7329 - Service Monitoring, Performance-Kenngrößen**

DasService MonitoringMUSSPerformance-Kenngrößenanhand einer eindeutigen
Identifikation (ID im XML-Schema) identifizieren. Für gleiche
Performance-Kenngrößen (z.B. Bearbeitungszeit)MUSSder gleiche Identifikator
über Produkttypgrenzen hinaus nutzbar sein. Eindeutig identifiziert wird ein
Wert über

 ---> UL

**[\<=]**

Die Identifikatoren für Performance-Kenngrößen werden in [gemKPT_Betr]
definiert. Bei Notwendigkeit werden in [gemKPT_Betr] neue
Performance-Kenngrößen Identifikatoren aufgenommen.

### 6 Anhang A – Verzeichnisse

### 6.1 Abkürzungen

<table><tr><th>
Kürzel

</th><th>
Erläuterung

</th></tr><tr><td>
eGK

</td><td>
elektronische Gesundheitskarte

</td></tr><tr><td>
FQDN

</td><td>
Fully Qualified Domain Name

</td></tr><tr><td>
GUI

</td><td>
Graphical User Interface – Grafische Benutzeroberfläche

</td></tr><tr><td>
GTI

</td><td>
Gesamtverantwortlicher TI

</td></tr><tr><td>
HBA

</td><td>
Heilberufsausweis

</td></tr><tr><td>
PU

</td><td>
Produktivumgebung

</td></tr><tr><td>
RU

</td><td>
Referenzumgebung

</td></tr><tr><td>
SMC-B

</td><td>
Security Module Card Typ B

</td></tr><tr><td>
TI

</td><td>
Telematikinfrastruktur

</td></tr><tr><td>
TLS

</td><td>
Transport Layer Security

</td></tr><tr><td>
TU

</td><td>
Testumgebung

</td></tr><tr><td>
VSDM

</td><td>
Versichertenstammdatenmanagement

</td></tr></table>

### 6.2 Glossar

Das Glossar wird als eigenständiges Dokument (vgl. [gemGlossar]) zur Verfügung
gestellt.

### 6.3 Abbildungsverzeichnis

- [Abbildung-1] - ABB_ServMon_301 Komponenten und Außensicht des Service Monitorings
- [Abbildung-2] - ABB_ServMon_304 Übersicht Service Monitoring-Datenquellen
- [Abbildung-3] - ABB_ServMon_303 Datenfluss Service Monitoring
- [Abbildung-4] - ABB_ServMon_300 – Komponentendiagramm des Service Monitorings
- [Abbildung-5] - Abb_Service_Monitoring_SOAP-Request

### 6.4 Tabellenverzeichnis

- [Tabelle-1] - Tab_Service_Monitoring_Akteure_und_Rollen
- [Tabelle-2] - Tab_Service_Monitoring_I_Monitoring_Update
- [Tabelle-3] - Tab_Service_Monitoring_Attribute
- [Tabelle-4] - Tab_Service_Monitoring_SOAP-Request, Beschreibung der Elemente
- [Tabelle-5] - Tab_Service_Monitoring_SOAP-Response, Beschreibung der Elemente
- [Tabelle-7] - Tab_Service_Monitoring_TUC_SM_002_Erreichbarkeitsprüfung
- [Tabelle-8] - Tab_Service_Monitoring_Probes_DNS_Name_Resolution
- [Tabelle-11] - Tab_Service_Monitoring_Probes_Zeitinformation_TI
- [Tabelle-12] - Tab_Service_Monitoring_Probes_CRL_Download
- [Tabelle-13] - Tab_Service_Monitoring_Probes_TSL_Download
- [Tabelle-14] - Tab_Service_Monitoring_Probes_BNetzA_Download
- [Tabelle-15] - Tab_Service_Monitoring_Probes_OCSP
- [Tabelle-16] - Tab_Service Monitoring_Probes_UFS
- [Tabelle-19] - Tab_Service Monitoring_Probes_KSRS_Upload
- [Tabelle-22] - Tab_Service_Monitoring_Probes_Verzeichnisdienst_Query
- [Tabelle-25] - Tab_Service_Monitoring_Probes_ePA- Authentisierung_TI
- [Tabelle-28] - Tab_Service_Monitoring_Probes_ePA_Dokumentenverwaltung
- [Tabelle-29] - Tab_Service_Monitoring_Probes_ePA-Verfügbarkeitsmonitoring
- [Tabelle-31] - Tab_Service_Monitoring_Probes_aAdG-NetG_Erreichbarkeit
- [Tabelle-32] - Tab_Service_Monitoring_Probe_Daten
- [Tabelle-33] - Tab_Service_Monitoring_Fehlercodes

### 6.5 Referenzierte Dokumente

### 6.5.1 Dokumente der gematik

Die nachfolgende Tabelle enthält die Bezeichnung der in dem vorliegenden
Dokument referenzierten Dokumente der gematik zur Telematikinfrastruktur. Der
mit der vorliegenden Version korrelierende Entwicklungsstand dieser Konzepte
und Spezifikationen wird pro Release in einer Dokumentenlandkarte definiert,
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
[gemKPT_Arch_TIP]

</td><td>
gematik: Konzept Architektur der TI-Plattform

</td></tr><tr><td>
[gemKPT_Betr]

</td><td>
gematik: Spezifisches Betriebskonzept

</td></tr><tr><td>
[gemSpec_Intermediär_VSDM]

</td><td>
gematik: Spezifikation Intermediär VSDM

</td></tr><tr><td>
[gemSpec_Kon]

</td><td>
gematik: Spezifikation Konnektor

</td></tr><tr><td>
[gemSpec_Krypt]

</td><td>
gematik: Übergreifende Spezifikation – Verwendung kryptographischer
Algorithmen in der Telematikinfrastruktur

</td></tr><tr><td>
[gemSpec_KSR]

</td><td>
gematik: Spezifikation Konfigurationsdienst

</td></tr><tr><td>
[gemSpec_Net]

</td><td>
gematik: Übergreifenden Spezifikation Netzwerk

</td></tr><tr><td>
[gemSpec_OM]

</td><td>
gematik: Übergreifenden Spezifikation Operations und Maintenance

</td></tr><tr><td>
[gemSpec_Perf]

</td><td>
gematik: Performancespezifikation TI-Plattform

</td></tr><tr><td>
[gemSpec_PKI]

</td><td>
gematik: Spezifikation PKI

</td></tr><tr><td>
[gemSpec_SST_FD_VSDM]

</td><td>
gematik: Schnittstellenspezifikation Fachdienste (UFS/VSDD/CMS)

</td></tr><tr><td>
[gemSpec_St_Ampel]

</td><td>
gematik: Spezifikation Störungsampel

</td></tr><tr><td>
[gemSpec_TSL]

</td><td>
gematik: Spezifikation TSL-Dienst

</td></tr><tr><td>
[gemSpec_VPN_ZugD]

</td><td>
gematik: Spezifikation VPN-Zugangsdienst

</td></tr><tr><td>
[gemSpec_VZD]

</td><td>
gematik: Spezifikation Verzeichnisdienst

</td></tr><tr><td>
[gemSpec_X.509_TSP]

</td><td>
gematik: Spezifikation Trust Service Provider X.509

</td></tr></table>

### 6.5.2 Weitere Dokumente

<table><tr><th>
[Quelle]

</th><th>
Herausgeber (Erscheinungsdatum): Titel

</th></tr><tr><td>
[DIN EN ISO 9241]

</td><td>
Ergonomie der Mensch-System-Interaktion - Teil 110: Grundsätze der
Dialoggestaltung (ISO 9241-110:2006); Deutsche Fassung EN ISO 9241-110:2006 

Ausgabe 2008-09

</td></tr><tr><td>
[RFC2119]

</td><td>
RFC 2119 (März 1997): Key words for use in RFCs to Indicate  
Requirement
Levels S. Bradner  
http://tools.ietf.org/html/rfc2119

</td></tr><tr><td>
[RFC7159]

</td><td>
The JavaScript Object Notation (JSON) Data Interchange Format

</td></tr><tr><td>
[RFC7231]

</td><td>
Hypertext Transfer Protocol (HTTP/1.1): Semantics and Content

</td></tr></table>

### 6.6 Fehlercodes

<table><tr><th>
Fehlercode

</th><th>
ErrorType

</th><th>
Severity

</th><th>
Fehlertext

</th></tr><tr><td>
7100

</td><td>
Technical

</td><td>
Fatal

</td><td>
Dienst ist nicht erreichbar

</td></tr><tr><td>
7101

</td><td>
Technical

</td><td>
Fatal

</td><td>
Ein oder mehrere Port(s) vom Dienst sind geschlossen

</td></tr><tr><td>
7102

</td><td>
Technical

</td><td>
Fatal

</td><td>
Zu einem DNS Namen konnte keine IP-Adresse gefunden werden

</td></tr><tr><td>
7103

</td><td>
Technical

</td><td>
Fatal

</td><td>
Aufruf mit Fehler beendet

</td></tr><tr><td>
7104

</td><td>
Technical

</td><td>
Fatal

</td><td>
Werte können nicht über DNS Service Discovery ermittelt werden

</td></tr><tr><td>
7105

</td><td>
Technical

</td><td>
Fatal

</td><td>
Fehler beim Aufruf des Registrierungsservers

</td></tr><tr><td>
7106

</td><td>
Technical

</td><td>
Fatal

</td><td>
TSL nicht valide

</td></tr><tr><td>
7107

</td><td>
Technical

</td><td>
Fatal

</td><td>
In der Probe ist ein Fehler aufgetreten

</td></tr><tr><td>
7108

</td><td>
Technical

</td><td>
Fatal

</td><td>
DNS-Record Validierung fehlgeschlagen (DNSSEC)

</td></tr><tr><td>
7109

</td><td>
Technical

</td><td>
Fatal

</td><td>
Minimale zeitliche Gültigkeit der CRL unterschritten

</td></tr><tr><td>
7110

</td><td>
Technical

</td><td>
Fatal

</td><td>
CRL Signaturprüfung fehlgeschlagen

</td></tr><tr><td>
7111

</td><td>
Technical

</td><td>
Fatal

</td><td>
eGK MRPIN.home hat nicht den nötigen Sicherheitszustand

</td></tr></table>

### 6.7 Offene Punkte / Klärungsbedarf

<table><tr><th>
Kap.

</th><th>
Offener Punkt

</th><th>
Zuständig

</th></tr><tr><td>
  5.4

</td><td>
Die Verfügbarkeit von SMC-B-Karten bzw. -Zertifikaten für die PU befindet sich
noch in der Klärung. Bis zur Klärung werden in der PU keine Probes genutzt
welche SMC-B-Zertifikate benötigen.

</td><td>
  gematik

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
[3]:                     #3-zerlegung-des-produkttyps
[4]:                     #4-übergreifende-festlegungen
[4.1]:                   #41-implementierung-des-service-monitorings
[4.1.1]:                 #411-verwendung-von-standardprodukten
[4.1.2]:                 #412-administration-und-konfiguration
[4.1.3]:                 #413-nutzeroberfläche
[4.1.4]:                 #414-dokumentation
[4.2]:                   #42-betrieb-des-service-monitorings
[4.2.1]:                 #421-verfügbarkeits--und-durchsatzanforderungen
[4.2.2]:                 #422-speicherungsdauer-der-übermittelten-daten
[4.3]:                   #43-zugriffs--und-berechtigungskonzept
[4.3.1]:                 #431-zugriffskonzept
[4.3.2]:                 #432-berechtigungskonzept
[5]:                     #5-funktionsmerkmale
[5.1]:                   #51-schnittstelle-i_view_service_monitoring
[5.1.1]:                 #511-darstellung-der-monitoring-daten
[5.1.2]:                 #512-schnittstelle-view-service-monitoring-api-web-service
[5.1.3]:                 #513-umsetzung
[5.2]:                   #52-schnittstelle-i_monitoring_update
[5.2.1]:                 #521-schnittstellendefinition
[5.2.2]:                 #522-umsetzung
[5.2.3]:                 #523-nutzung
[5.3]:                   #53-technische-use-cases-–-tucs
[5.4]:                   #54-probes
[5.4.1]:                 #541-dns-name-resolution
[5.4.2]:                 #542-konnektorregistrierung
[5.4.3]:                 #543-vpn_tunnel
[5.4.4]:                 #544-vpn_tunnel-sis
[5.4.5]:                 #545-zeitinformation_ti
[5.4.6]:                 #546-zeitinformation_vpn_zugangsdienst
[5.4.7]:                 #547-crl-download
[5.4.8]:                 #548-tsl-download
[5.4.9]:                 #549-tsl-download-mit-prüfung
[5.4.10]:                #5410-tsl-download-ipsectunnel-ti
[5.4.11]:                #5411-tsl-download-internet
[5.4.12]:                #5412-bnetza_vl-download
[5.4.13]:                #5413-bnetza-download-ipsectunnel-ti
[5.4.14]:                #5414-ocsp
[5.4.15]:                #5415-ocsp-ipsectunnel-ti
[5.4.16]:                #5416-fachdienste-vsdm
[5.4.16.1]:              #54161-fachdienst-vsdm-ufs
[5.4.16.2]:              #54162-fachdienst-vsdm_vsdd_cms
[5.4.17]:                #5417-intermediär-vsdm
[5.4.18]:                #5418-vsdm--intermediär-vsdm-ipsectunnel-ti
[5.4.19]:                #5419-vsdm-intermediär-vsdm-erreichbarkeit
[5.4.20]:                #5420-ksrs-upload
[5.4.21]:                #5421-ksrs-download
[5.4.22]:                #5422-ksrs-download-ipsectunnel-ti
[5.4.23]:                #5423-ksrs-download-bestandsnetze
[5.4.24]:                #5424-ksrs-download-bestandsnetze-ipsectunnel-ti
[5.4.25]:                #5425-verzeichnisdienst-query
[5.4.26]:                #5426-verzeichnisdienst-query-ipsectunnel-ti
[5.4.27]:                #5427-verzeichnisdienst-application_maintenance
[5.4.28]:                #5428-ablauf-von-server-zertifikaten-ti
[5.4.29]:                #5429-ablauf-von-server-zertifikaten-internet
[5.4.30]:                #5430-epa---authentisierung-ti
[5.4.31]:                #5431-epa---authentisierung-internet
[5.4.32]:                #5432-epa---autorisierung
[5.4.33]:                #5433-epa---i_authorization_managementcheckrecordexists
[5.4.34]:                #5434-epa---dokumentenverwaltung
[5.4.35]:                #5435-epa-–-verfügbarkeitsmonitoring
[5.4.36]:                #5436-epa--schlüsselgenerierungsdienst
[5.4.37]:                #5437-aadg-netg
[5.4.38]:                #5438-erfassung-von-service-monitoring-daten-in-probes
[5.5]:                   #55-performance-kenngrößen
[6]:                     #6-anhang-a-–-verzeichnisse
[6.1]:                   #61-abkürzungen
[6.2]:                   #62-glossar
[6.3]:                   #63-abbildungsverzeichnis
[6.4]:                   #64-tabellenverzeichnis
[6.5]:                   #65-referenzierte-dokumente
[6.5.1]:                 #651-dokumente-der-gematik
[6.5.2]:                 #652-weitere-dokumente
[6.6]:                   #66-fehlercodes
[6.7]:                   #67-offene-punkte--klärungsbedarf
[Abbildung-1]:           gemSpec_ServiceMon_V1.5.0.attachments/18187159648614223387.emf
[Abbildung-2]:           gemSpec_ServiceMon_V1.5.0.attachments/12422785690422370962.png
[Abbildung-3]:           gemSpec_ServiceMon_V1.5.0.attachments/3614776289696959476.png
[Abbildung-4]:           gemSpec_ServiceMon_V1.5.0.attachments/10471764381621478801.emf
[Abbildung-5]:           gemSpec_ServiceMon_V1.5.0.attachments/690845079118879069.emf
[Tbl-001]:               #Tbl-001 (&93834811903456)
[Tabelle-1]:             #Tabelle-1 (&93834810820296)
[Tabelle-2]:             #Tabelle-2 (&93834801654456)
[Tabelle-3]:             #Tabelle-3 (&93834811144600)
[Tabelle-4]:             #Tabelle-4 (&93834811174088)
[Tabelle-5]:             #Tabelle-5 (&93834783610448)
[Tbl-007]:               #Tbl-007 (&93834783649176)
[Tabelle-7]:             #Tabelle-7 (&93834768024080)
[Tabelle-8]:             #Tabelle-8 (&93834783500648)
[Tbl-010]:               #Tbl-010 (&93834799211384)
[Tbl-011]:               #Tbl-011 (&93834801552816)
[Tabelle-11]:            #Tabelle-11 (&93834776408848)
[Tabelle-12]:            #Tabelle-12 (&93834798995024)
[Tabelle-13]:            #Tabelle-13 (&93834777657488)
[Tabelle-14]:            #Tabelle-14 (&93834800915728)
[Tabelle-15]:            #Tabelle-15 (&93834781790896)
[Tabelle-16]:            #Tabelle-16 (&93834764436880)
[Tbl-018]:               #Tbl-018 (&93834764504664)
[Tbl-019]:               #Tbl-019 (&93834785698320)
[Tabelle-19]:            #Tabelle-19 (&93834785774096)
[Tbl-021]:               #Tbl-021 (&93834783894680)
[Tbl-022]:               #Tbl-022 (&93834776270280)
[Tabelle-22]:            #Tabelle-22 (&93834776326952)
[Tbl-024]:               #Tbl-024 (&93834778276528)
[Tbl-025]:               #Tbl-025 (&93834802494392)
[Tabelle-25]:            #Tabelle-25 (&93834802566344)
[Tbl-027]:               #Tbl-027 (&93834765284624)
[Tbl-028]:               #Tbl-028 (&93834799081048)
[Tabelle-28]:            #Tabelle-28 (&93834799150112)
[Tabelle-29]:            #Tabelle-29 (&93834775695960)
[Tbl-031]:               #Tbl-031 (&93834783683960)
[Tabelle-31]:            #Tabelle-31 (&93834783763120)
[Tabelle-32]:            #Tabelle-32 (&93834799985152)
[Tbl-034]:               #Tbl-034 (&93834809673104)
[Tbl-035]:               #Tbl-035 (&93834809752616)
[Tbl-036]:               #Tbl-036 (&93834809808264)
[Tabelle-33]:            #Tabelle-33 (&93834811311080)
[Tbl-038]:               #Tbl-038 (&93834811432680)
