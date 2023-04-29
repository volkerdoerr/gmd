
Elektronische Gesundheitskarte und Telematikinfrastruktur

### Spezifikation<br>Konnektor

- Klassifizierung: öffentlich
- Referenzierung: gemSpec_Kon
- Revision: 571788
- Stand: 28.11.2022
- Status: freigegeben
- Version: 5.18.0

### Dokumentinformationen

Änderungen zur Vorversion

Anpassungen des vorliegenden Dokumentes im Vergleich zur Vorversion können Sie
der nachfolgenden Tabelle entnehmen.

Dokumentenhistorie

 ---> TABLE

### Inhaltsverzeichnis

- [Dokumentinformationen]
- [Inhaltsverzeichnis]
- [1] Einordnung des Dokumentes
  - [1.1] Zielsetzung
  - [1.2] Zielgruppe
  - [1.3] Geltungsbereich
  - [1.4] Abgrenzung des Dokuments
  - [1.5] Methodik
    - [1.5.1] Anforderungen
    - [1.5.2] Offene Punkte
    - [1.5.3] Erläuterungen zur Spezifikation des Außenverhaltens
    - [1.5.4] Erläuterungen zur Dokumentenstruktur und „Dokumentenmechanismen“
      - [1.5.4.1] Modulare Spezifikation über Funktionsmerkmale
      - [1.5.4.2] Technische Use Cases - TUCs
      - [1.5.4.3] Event-Mechanismus
      - [1.5.4.4] Konfigurationsparameter und Zustandswerte
- [2] Systemüberblick
  - [2.1] Logische Struktur
  - [2.2] Sicherer Datenspeicher
  - [2.3] Überblick Konnektoridentität
  - [2.4] Mandantenfähigkeit
  - [2.5] Versionierung
  - [2.6] Fachanwendungen
  - [2.7] Netzseitige Einsatzszenarien
    - [2.7.1] Parameter ANLW_ANBINDUNGS_MODUS
    - [2.7.2] Parameter ANLW_INTERNET_MODUS
  - [2.8] Lokale und entfernte Kartenterminals
  - [2.9] Standalone-Szenario
- [3] Übergreifende Festlegungen
  - [3.1] Allgemeine übergreifende Festlegungen
    - [3.1.1] Dokumentformate
    - [3.1.2] Kartentypen
    - [3.1.3] Übergreifende Festlegungen zum Aufbau von sicheren Verbindungen
  - [3.2] Konnektoridentität und gSMC-K
    - [3.2.1] Organisatorische Anforderungen und Sperrprozesse
  - [3.3] Bootup-Phase
  - [3.4] Betriebszustand
    - [3.4.1] Betriebsaspekte
  - [3.5] Fachliche Anbindung der Clientsysteme
    - [3.5.1] Betriebsaspekte
  - [3.6] Clientsystemschnittstelle
    - [3.6.1] SOAP-Schnittstelle
    - [3.6.2] Statusrückmeldung und Fehlerbehandlung
    - [3.6.3] Transport großer Dokumente
  - [3.7] Verwendung manuell importierter CA-Zertifikate
  - [3.8] Testunterstützung
- [4] Funktionsmerkmale
  - [4.1] Anwendungskonnektor
    - [4.1.1] Zugriffsberechtigungsdienst
      - [4.1.1.1] Funktionsmerkmalweite Aspekte
      - [4.1.1.2] Durch Ereignisse ausgelöste Reaktionen
      - [4.1.1.3] Interne TUCs, nicht durch Fachmodule nutzbar
      - [4.1.1.4] Interne TUCs, auch durch Fachmodule nutzbar
        - [4.1.1.4.1] TUC_KON_000 „Prüfe Zugriffsberechtigung“
      - [4.1.1.5] Operationen an der Außenschnittstelle
      - [4.1.1.6] Betriebsaspekte
    - [4.1.2] Dokumentvalidierungsdienst
      - [4.1.2.1] Funktionsmerkmalweite Aspekte
      - [4.1.2.2] Durch Ereignisse ausgelöste Reaktionen
      - [4.1.2.3] Interne TUCs, nicht durch Fachmodule nutzbar
      - [4.1.2.4] Interne TUCs, auch durch Fachmodule nutzbar
        - [4.1.2.4.1] TUC_KON_080 „Dokument validieren”
      - [4.1.2.5] Operationen an der Außenschnittstelle
      - [4.1.2.6] Betriebsaspekte
    - [4.1.3] Dienstverzeichnisdienst
      - [4.1.3.1] Funktionsmerkmalweite Aspekte
      - [4.1.3.2] Durch Ereignisse ausgelöste Reaktionen
      - [4.1.3.3] Interne TUCs, nicht durch Fachmodule nutzbar
      - [4.1.3.4] Interne TUCs, auch durch Fachmodule nutzbar
        - [4.1.3.4.1] TUC_KON_041 „Einbringen der Endpunktinformationen während der Bootup-Phase“
      - [4.1.3.5] Operationen an der Außenschnittstelle
      - [4.1.3.6] Betriebsaspekte
    - [4.1.4] Kartenterminaldienst
      - [4.1.4.1] Funktionsmerkmalweite Aspekte
      - [4.1.4.2] Durch Ereignisse ausgelöste Reaktionen
      - [4.1.4.3] Interne TUCs, nicht durch Fachmodule nutzbar
        - [4.1.4.3.1] TUC_KON_050 „Beginne Kartenterminalsitzung“
        - [4.1.4.3.2] TUC_KON_054 „Kartenterminal hinzufügen“
        - [4.1.4.3.3] TUC_KON_053 „Paire Kartenterminal“
        - [4.1.4.3.4] TUC_KON_055 „Befülle CT-Object“
      - [4.1.4.4] Interne TUCs, auch durch Fachmodule nutzbar
        - [4.1.4.4.1] TUC_KON_051 „Mit Anwender über Kartenterminal interagieren“
        - [4.1.4.4.2] TUC_KON_056 „Karte anfordern“
        - [4.1.4.4.3] TUC_KON_057 „Karte auswerfen“
        - [4.1.4.4.4] TUC_KON_058 „Displaygröße ermitteln“
      - [4.1.4.5] Operationen an der Außenschnittstelle
        - [4.1.4.5.1] RequestCard
        - [4.1.4.5.2] EjectCard
      - [4.1.4.6] Betriebsaspekte
        - [4.1.4.6.1] Allgemeine Betriebsaspekte
        - [4.1.4.6.2] Kartenterminals pflegen
        - [4.1.4.6.3] Import der Kartenterminal-Informationen
    - [4.1.5] Kartendienst
      - [4.1.5.1] Funktionsmerkmalweite Aspekte
      - [4.1.5.2] Durch Ereignisse ausgelöste Reaktionen
      - [4.1.5.3] Interne TUCs, nicht durch Fachmodule nutzbar
        - [4.1.5.3.1] TUC_KON_001 „Karte öffnen“
      - [4.1.5.4] Interne TUCs, auch durch Fachmodule nutzbar
        - [4.1.5.4.1] TUC_KON_026 „Liefere CardSession“
        - [4.1.5.4.2] TUC_KON_012 „PIN verifizieren“
        - [4.1.5.4.3] TUC_KON_019 „PIN ändern“
        - [4.1.5.4.4] TUC_KON_021 „PIN entsperren“
        - [4.1.5.4.5] TUC_KON_022 „Liefere PIN-Status“
        - [4.1.5.4.6] TUC_KON_027 „PIN-Schutz ein-/ausschalten“
        - [4.1.5.4.7] TUC_KON_023 „Karte reservieren“
        - [4.1.5.4.8] TUC_KON_005 „Card-to-Card authentisieren“
        - [4.1.5.4.9] TUC_KON_202 „LeseDatei“
        - [4.1.5.4.10] TUC_KON_203 „SchreibeDatei“
        - [4.1.5.4.11] TUC_KON_204 „LöscheDateiInhalt“
        - [4.1.5.4.12] TUC_KON_209 „LeseRecord“
        - [4.1.5.4.13] TUC_KON_210 „SchreibeRecord“
        - [4.1.5.4.14] TUC_KON_211 „LöscheRecordInhalt“
        - [4.1.5.4.15] TUC_KON_214 „FügeHinzuRecord“
        - [4.1.5.4.16] TUC_KON_215 „SucheRecord“
        - [4.1.5.4.17] TUC_KON_018 „eGK-Sperrung prüfen“
        - [4.1.5.4.18] TUC_KON_006 „Datenzugriffsaudit eGK schreiben“
        - [4.1.5.4.19] TUC_KON_218 „Signiere“
        - [4.1.5.4.20] TUC_KON_219 „Entschlüssele“
        - [4.1.5.4.21] TUC_KON_200 „SendeAPDU“
        - [4.1.5.4.22] TUC_KON_024 „Karte zurücksetzen“
        - [4.1.5.4.23] TUC_KON_216 „LeseZertifikat“
        - [4.1.5.4.24] TUC_KON_036 „LiefereFachlicheRolle“
      - [4.1.5.5] Operationen an der Außenschnittstelle
        - [4.1.5.5.1] VerifyPin
        - [4.1.5.5.2] ChangePin
        - [4.1.5.5.3] GetPinStatus
        - [4.1.5.5.4] UnblockPin
        - [4.1.5.5.5] EnablePin
        - [4.1.5.5.6] DisablePin
      - [4.1.5.6] Betriebsaspekte
        - [4.1.5.6.1] TUC_KON_025 "Initialisierung Kartendienst"
        - [4.1.5.6.2] Kartenübersicht und PIN-Management
    - [4.1.6] Systeminformationsdienst
      - [4.1.6.1] Funktionsmerkmalweite Aspekte
      - [4.1.6.2] Durch Ereignisse ausgelöste Reaktionen
      - [4.1.6.3] Interne TUCs, nicht durch Fachmodule nutzbar
      - [4.1.6.4] Interne TUCs, auch durch Fachmodule nutzbar
        - [4.1.6.4.1] TUC_KON_256 „Systemereignis absetzen“
        - [4.1.6.4.2] TUC_KON_252 „Liefere KT_Liste“
        - [4.1.6.4.3] TUC_KON_253 „Liefere Karten_Liste“
        - [4.1.6.4.4] TUC_KON_254 „Liefere Ressourcendetails“
      - [4.1.6.5] Operationen an der Außenschnittstelle
        - [4.1.6.5.1] GetCardTerminals
        - [4.1.6.5.2] GetCards
        - [4.1.6.5.3] GetResourceInformation
        - [4.1.6.5.4] Subscribe
        - [4.1.6.5.5] Unsubscribe
        - [4.1.6.5.6] RenewSubscriptions
        - [4.1.6.5.7] GetSubscription
      - [4.1.6.6] Betriebsaspekte
    - [4.1.7] Verschlüsselungsdienst
      - [4.1.7.1] Funktionsmerkmalweite Aspekte
      - [4.1.7.2] Durch Ereignisse ausgelöste Reaktionen
      - [4.1.7.3] Interne TUCs, nicht durch Fachmodule nutzbar
      - [4.1.7.4] Interne TUCs, auch durch Fachmodule nutzbar
        - [4.1.7.4.1] TUC_KON_070 „Daten hybrid verschlüsseln”
        - [4.1.7.4.2] TUC_KON_071 „Daten hybrid entschlüsseln”
        - [4.1.7.4.3] TUC_KON_072 „Daten symmetrisch verschlüsseln”
        - [4.1.7.4.4] TUC_KON_073 „Daten symmetrisch entschlüsseln”
        - [4.1.7.4.5] TUC_KON_075 „Symmetrisch verschlüsseln“
        - [4.1.7.4.6] TUC_KON_076 „Symmetrisch entschlüsseln“
      - [4.1.7.5] Operationen an der Außenschnittstelle
        - [4.1.7.5.1] EncryptDocument
        - [4.1.7.5.2] DecryptDocument
      - [4.1.7.6] Betriebsaspekte
    - [4.1.8] Signaturdienst
      - [4.1.8.1] Funktionsmerkmalweite Aspekte
        - [4.1.8.1.1] Dokumentensignatur
        - [4.1.8.1.2] Signaturrichtlinien
        - [4.1.8.1.3] Signaturzeitpunkt
        - [4.1.8.1.4] Jobnummer
        - [4.1.8.1.5] Komfortsignatur
      - [4.1.8.2] Durch Ereignisse ausgelöste Reaktionen
      - [4.1.8.3] Interne TUCs, nicht durch Fachmodule nutzbar
        - [4.1.8.3.1] TUC_KON_155 „Dokumente zur Signatur vorbereiten”
        - [4.1.8.3.2] TUC_KON_165 „Signaturvoraussetzungen für nonQES prüfen“
        - [4.1.8.3.3] TUC_KON_166 „nonQES Signaturen erstellen“
        - [4.1.8.3.4] TUC_KON_152 "Signaturvoraussetzungen für QES prüfen"
        - [4.1.8.3.5] TUC_KON_154 "QES Signaturen erstellen"
        - [4.1.8.3.6] TUC_KON_168 „Einzelsignatur QES erstellen“
        - [4.1.8.3.7] TUC_KON_158 "Komfortsignaturen erstellen"
      - [4.1.8.4] Interne TUCs, auch durch Fachmodule nutzbar
        - [4.1.8.4.1] TUC_KON_160 „Dokumente nonQES signieren”
        - [4.1.8.4.2] TUC_KON_161 „nonQES Dokumentsignatur prüfen”
        - [4.1.8.4.3] TUC_KON_162 „Kryptographische Prüfung der XML-Dokumentensignatur”
        - [4.1.8.4.4] TUC_KON_150 „Dokumente QES signieren”
        - [4.1.8.4.5] Anforderungen an die Stapelsignatur
        - [4.1.8.4.6] TUC_KON_151 „QES Dokumentensignatur prüfen“
        - [4.1.8.4.7] TUC_KON_170 „Dokumente mit Komfort signieren”
        - [4.1.8.4.8] TUC_KON_171 „Komfortsignatur einschalten”
        - [4.1.8.4.9] TUC_KON_172 „Komfortsignatur ausschalten”
        - [4.1.8.4.10] TUC_KON_173 „Liefere Signaturmodus”
      - [4.1.8.5] Operationen an der Außenschnittstelle
        - [4.1.8.5.1] SignDocument (nonQES und QES)
        - [4.1.8.5.2] VerifyDocument (nonQES und QES)
        - [4.1.8.5.3] StopSignature
        - [4.1.8.5.4] GetJobNumber
        - [4.1.8.5.5] ActivateComfortSignature
        - [4.1.8.5.6] DeactivateComfortSignature
        - [4.1.8.5.7] GetSignatureMode
      - [4.1.8.6] Betriebsaspekte
    - [4.1.9] Zertifikatsdienst
      - [4.1.9.1] Funktionsmerkmalweite Aspekte
      - [4.1.9.2] Durch Ereignisse ausgelöste Reaktionen
      - [4.1.9.3] Interne TUCs, nicht durch Fachmodule nutzbar
        - [4.1.9.3.1] TUC_KON_032 „TSL aktualisieren“
        - [4.1.9.3.2] TUC_KON_031 „BNetzA-VL aktualisieren“
        - [4.1.9.3.3] TUC_KON_040 „CRL aktualisieren“
        - [4.1.9.3.4] TUC_KON_033 „Zertifikatsablauf prüfen“
      - [4.1.9.4] Interne TUCs, auch durch Fachmodule nutzbar
        - [4.1.9.4.1] TUC_KON_037 „Zertifikat prüfen"
        - [4.1.9.4.2] TUC_KON_042 „CV-Zertifikat prüfen“
        - [4.1.9.4.3] TUC_KON_034 „Zertifikatsinformationen extrahieren“
      - [4.1.9.5] Operationen an der Außenschnittstelle
        - [4.1.9.5.1] CheckCertificateExpiration
        - [4.1.9.5.2] ReadCardCertificate
        - [4.1.9.5.3] VerifyCertificate
      - [4.1.9.6] Betriebsaspekte
        - [4.1.9.6.1] TUC_KON_035 „Zertifikatsdienst initialisieren“
    - [4.1.10] Protokollierungsdienst
      - [4.1.10.1] Funktionsmerkmalweite Aspekte
      - [4.1.10.2] Durch Ereignisse ausgelöste Reaktionen
      - [4.1.10.3] Interne TUCs, nicht durch Fachmodule nutzbar
      - [4.1.10.4] Interne TUCs, auch durch Fachmodule nutzbar
        - [4.1.10.4.1] TUC_KON_271 „Schreibe Protokolleintrag“
      - [4.1.10.5] Operationen an der Außenschnittstelle
      - [4.1.10.6] Betriebsaspekte
        - [4.1.10.6.1] TUC_KON_272 „Initialisierung Protokollierungsdienst
    - [4.1.11] TLS-Dienst
      - [4.1.11.1] Funktionsmerkmalweite Aspekte
      - [4.1.11.2] Durch Ereignisse ausgelöste Reaktionen
      - [4.1.11.3] Interne TUCs, nicht durch Fachmodule nutzbar
      - [4.1.11.4] Interne TUCs, auch durch Fachmodule nutzbar
        - [4.1.11.4.1] TUC_KON_110 „Kartenbasierte TLS-Verbindung aufbauen“
        - [4.1.11.4.2] TUC_KON_111 „Kartenbasierte TLS-Verbindung abbauen“
      - [4.1.11.5] Operationen an der Außenschnittstelle
      - [4.1.11.6] Betriebsaspekte
    - [4.1.12] LDAP-Proxy
      - [4.1.12.1] Funktionsmerkmalweite Aspekte
      - [4.1.12.2] Durch Ereignisse ausgelöste Reaktionen
      - [4.1.12.3] Interne TUCs, nicht durch Fachmodule nutzbar
      - [4.1.12.4] Interne TUCs, auch durch Fachmodule nutzbar
        - [4.1.12.4.1] TUC_KON_290 „LDAP-Verbindung aufbauen“
        - [4.1.12.4.2] TUC_KON_291 „Verzeichnis abfragen“
        - [4.1.12.4.3] TUC_KON_292 „LDAP-Verbindung trennen"
        - [4.1.12.4.4] TUC_KON_293 „Verzeichnisabfrage abbrechen"
      - [4.1.12.5] Operationen an der Außenschnittstelle
        - [4.1.12.5.1] Unterstützte LDAPv3 Operationen
      - [4.1.12.6] Betriebsaspekte
    - [4.1.13] Authentifizierungsdienst
      - [4.1.13.1] Funktionsmerkmalweite Aspekte
        - [4.1.13.1.1] Externe Authentisierung
      - [4.1.13.2] Durch Ereignisse ausgelöste Reaktionen
      - [4.1.13.3] Interne TUCs
      - [4.1.13.4] Operationen an der Außenschnittstelle
        - [4.1.13.4.1] ExternalAuthenticate
      - [4.1.13.5] Betriebsaspekte
    - [4.1.14] Betriebsdatenmeldedienst
  - [4.2] Netzkonnektor
    - [4.2.1] Anbindung LAN/WAN
      - [4.2.1.1] Funktionsmerkmalweite Aspekte
        - [4.2.1.1.1] Netzwerksegmentierung
        - [4.2.1.1.2] Routing und Firewall
      - [4.2.1.2] Durch Ereignisse ausgelöste Reaktionen
      - [4.2.1.3] Interne TUCs, nicht durch Fachmodule nutzbar
        - [4.2.1.3.1] TUC_KON_305 „LAN-Adapter initialisieren“
        - [4.2.1.3.2] TUC_KON_306 „WAN-Adapter initialisieren“
        - [4.2.1.3.3] TUC_KON_304 „Netzwerk-Routen einrichten“
      - [4.2.1.4] Interne TUCs, auch durch Fachmodule nutzbar
      - [4.2.1.5] Operationen an der Außenschnittstelle
      - [4.2.1.6] Betriebsaspekte
    - [4.2.2] DHCP-Server
      - [4.2.2.1] Funktionsmerkmalweite Aspekte
      - [4.2.2.2] Durch Ereignisse ausgelöste Reaktionen
      - [4.2.2.3] Interne TUCs, nicht durch Fachmodule nutzbar
      - [4.2.2.4] Interne TUCs, auch durch Fachmodule nutzbar
      - [4.2.2.5] Operationen an der Außenschnittstelle
        - [4.2.2.5.1] Liefere Netzwerkinformationen über DHCP
      - [4.2.2.6] Betriebsaspekte
        - [4.2.2.6.1] TUC_KON_343 „Initialisierung DHCP-Server“
    - [4.2.3] DHCP-Client
      - [4.2.3.1] Funktionsmerkmalweite Aspekte
      - [4.2.3.2] Durch Ereignisse ausgelöste Reaktionen
      - [4.2.3.3] Interne TUCs, nicht durch Fachmodule nutzbar
        - [4.2.3.3.1] TUC_KON_341 „DHCP-Informationen beziehen“
      - [4.2.3.4] Interne TUCs, auch durch Fachmodule nutzbar
      - [4.2.3.5] Operationen an der Außenschnittstelle
      - [4.2.3.6] Betriebsaspekte
    - [4.2.4] VPN-Client
      - [4.2.4.1] Funktionsmerkmalweite Aspekte
      - [4.2.4.2] Durch Ereignisse ausgelöste Reaktionen
      - [4.2.4.3] Interne TUCs, nicht durch Fachmodule nutzbar
        - [4.2.4.3.1] TUC_KON_321 „Verbindung zu dem VPN-Konzentrator der TI aufbauen“
        - [4.2.4.3.2] TUC_KON_322 „Verbindung zu dem VPN-Konzentrator des SIS aufbauen“
      - [4.2.4.4] Interne TUCs, auch durch Fachmodule nutzbar
      - [4.2.4.5] Operationen an der Außenschnittstelle
      - [4.2.4.6] Betriebsaspekte
    - [4.2.5] Zeitdienst
      - [4.2.5.1] Funktionsmerkmalweite Aspekte
      - [4.2.5.2] Durch Ereignisse ausgelöste Reaktionen
      - [4.2.5.3] Interne TUCs, nicht durch Fachmodule nutzbar
      - [4.2.5.4] Interne TUCs, auch durch Fachmodule nutzbar
        - [4.2.5.4.1] TUC_KON_351 “Liefere Systemzeit”
      - [4.2.5.5] Operationen an der Außenschnittstelle
        - [4.2.5.5.1] Sync_Time
      - [4.2.5.6] Betriebsaspekte
        - [4.2.5.6.1] TUC_KON_352 Initialisierung Zeitdienst
    - [4.2.6] Namensdienst und Dienstlokalisierung
      - [4.2.6.1] Funktionsmerkmalweite Aspekte
      - [4.2.6.2] Durch Ereignisse ausgelöste Reaktionen
      - [4.2.6.3] Interne TUCs, nicht durch Fachmodule nutzbar
      - [4.2.6.4] Interne TUCs, auch durch Fachmodule nutzbar
        - [4.2.6.4.1] TUC_KON_361 „DNS-Namen auflösen“
        - [4.2.6.4.2] TUC_KON_362 „Liste der Dienste abrufen“
        - [4.2.6.4.3] TUC_KON_363 „Dienstdetails abrufen“
      - [4.2.6.5] Operationen an der Außenschnittstelle
        - [4.2.6.5.1] GetIPAddress
      - [4.2.6.6] Betriebsaspekte
    - [4.2.7] Optionale Verwendung von IPv6
  - [4.3] Konnektormanagement
    - [4.3.1] Zugang und Benutzerverwaltung des Konnektormanagements
    - [4.3.2] Konnektorname und Versionsinformationen
    - [4.3.3] Konfigurationsdaten: Persistieren sowie Export-Import
    - [4.3.4] Administration von Fachmodulen
    - [4.3.5] Neustart und Werksreset
    - [4.3.6] Leistungsumfänge und Standalone-Szenarios
    - [4.3.7] Online-Anbindung verwalten
    - [4.3.8] Re-Registrierung des Konnektors mit weiterem NK-Zertifikat
    - [4.3.9] Remote Management (Optional)
    - [4.3.10] Software- und Konfigurationsaktualisierung (KSR-Client)
      - [4.3.10.1] Funktionsmerkmalweite Aspekte
      - [4.3.10.2] Durch Ereignisse ausgelöste Reaktionen
      - [4.3.10.3] Interne TUCs, nicht durch Fachmodule nutzbar
        - [4.3.10.3.1] TUC_KON_280 „Konnektoraktualisierung durchführen“
        - [4.3.10.3.2] TUC_KON_281 „Kartenterminalaktualisierung anstoßen“
        - [4.3.10.3.3] TUC_KON_282 „UpdateInformationen beziehen“
        - [4.3.10.3.4] TUC_KON_283 „Infrastruktur Konfiguration aktualisieren“
      - [4.3.10.4] Interne TUCs, auch durch Fachmodule nutzbar
        - [4.3.10.4.1] TUC_KON_285 „UpdateInformationen für Fachmodul beziehen“
        - [4.3.10.4.2] TUC_KON_286 „Paket für Fachmodul laden“
      - [4.3.10.5] Operationen an der Außenschnittstelle
      - [4.3.10.6] Betriebsaspekte
        - [4.3.10.6.1] TUC_KON_284 KSR-Client initialisieren
    - [4.3.11] Konnektorstatus
  - [4.4] Hardware-Merkmale des Konnektors
- [5] Anhang A – Verzeichnisse
  - [5.1] Abkürzungen
  - [5.2] Glossar
  - [5.3] Abbildungsverzeichnis
  - [5.4] Tabellenverzeichnis
  - [5.5] Referenzierte Dokumente
    - [5.5.1] Dokumente der gematik
    - [5.5.2] Weitere Dokumente
- [6] Anhang B – Profilierung der Signatur- und Verschlüsselungsformate (normativ)
  - [6.1] Profilierung der Verschlüsselungsformate
  - [6.2] Profilierung der Signaturformate
  - [6.3] Profilierung VerificationReport
  - [6.4] Profilierung der Dokumentenformate und Nachrichten
- [7] Anhang F – Übersicht Events
- [8] Anhang H – Mapping von „Architektur der TI-Plattform“ auf Konnektorspezifikation
- [9] Anhang I – Umsetzungshinweise (informativ)
  - [9.1] Systemüberblick
    - [9.1.1] – Hinweise zur Sicherheitsevaluierung nach Common Criteria
      - [9.1.1.1] Separationsmechanismen des Konnektors
      - [9.1.1.2] Granularität der TSF
  - [9.2] Übergreifende Festlegungen
    - [9.2.1] Interne Mechanismen
      - [9.2.1.1] Zufallszahlen und Schlüssel
  - [9.3] Funktionsmerkmale
    - [9.3.1] Anwendungskonnektor
      - [9.3.1.1] Administration des Informationsmodells
      - [9.3.1.2] Vorgehensvariante für das Handling von CardSessions
      - [9.3.1.3] Darstellung von Terminal-Anzeigen auf einem Kartenterminal
- [10] Anhang K – Szenarien im dezentralen Umfeld
  - [10.1] Szenario 1: Einfache Installation ohne spezielle Anforderungen und ohne bestehende Infrastruktur
    - [10.1.1] Beschreibung des Szenarios
    - [10.1.2] Voraussetzungen
    - [10.1.3] Auswirkungen
  - [10.2] Szenario 2: Installation mit mehreren Behandlungsräumen
    - [10.2.1] Beschreibung des Szenarios
    - [10.2.2] Voraussetzungen
    - [10.2.3] Auswirkungen
  - [10.3] Szenario 3: Integration in bestehende Infrastruktur ohne Netzsegmentierung
    - [10.3.1] Beschreibung des Szenarios
    - [10.3.2] Voraussetzungen
    - [10.3.3] Auswirkungen
  - [10.4] Szenario 4: Integration in bestehende Infrastruktur mit Netzsegmentierung
    - [10.4.1] Beschreibung des Szenarios
    - [10.4.2] Voraussetzungen
    - [10.4.3] Auswirkungen
  - [10.5] Szenario 5: Zentral gesteckter HBA
    - [10.5.1] Beschreibung des Szenarios
    - [10.5.2] Voraussetzungen
    - [10.5.3] Auswirkung
  - [10.6] Szenario 6: Installation mit zentralem PS
    - [10.6.1] Beschreibung des Szenarios
    - [10.6.2] Voraussetzungen
    - [10.6.3] Auswirkungen
  - [10.7] Szenario 7: Mehrere Mandanten
    - [10.7.1] Beschreibung des Szenarios
    - [10.7.2] Voraussetzungen
    - [10.7.3] Auswirkungen
  - [10.8] Szenario 9: Standalone Konnektor - Physische Trennung
    - [10.8.1] Beschreibung des Szenarios
    - [10.8.2] Voraussetzungen
    - [10.8.3] Auswirkung
- [11] Anhang L – Datentypen von Eingangs- und Ausgangsdaten

### 1 Einordnung des Dokumentes

### 1.1 Zielsetzung

Die vorliegende Spezifikation definiert die Anforderungen zu Herstellung, Test
und Betrieb des Produkttyps Konnektor.

Dieses Dokument beschreibt die dezentrale Komponente zur sicheren Anbindung von
Clientsystemen der Institutionen und Organisationen des Gesundheitswesens an
die Telematikinfrastruktur – den Konnektor. Der Konnektor ist einerseits
verantwortlich für den Zugriff auf die in der Einsatzumgebung befindlichen
Kartenterminals sowie Karten und andererseits für die Kommunikation mit den
zentralen Diensten der TI-Plattform und fachanwendungsspezifischen Diensten.
Aus den Kommunikationsbeziehungen mit Clientsystem, Kartenterminals, Karten und
zentralen Diensten der TI-Plattform und fachanwendungsspezifischen Diensten
resultieren vom Konnektor anzubietende Schnittstellen, die gemeinsam in diesem
Dokument sowie den fachanwendungsspezifischen Fachmodulspezifikationen normativ
geregelt werden. Vom Konnektor genutzte Schnittstellen liegen zumeist in
anderen Verantwortungsbereichen (zentrale TI-Plattform aber auch Schnittstellen
der Kartenterminals und Karten). Diese werden in den übergreifenden
Spezifikationen der TI sowie den Produkttypspezifikationen definiert.

Dieses Dokument regelt somit nur einen Teil des Konnektors (wenngleich auch den
Wesentlichen). Für die Implementierung eines Konnektors ist entsprechend die
Kenntnis aller weiteren Spezifikationen erforderlich. Die Gesamtheit aller für
den Konnektor relevanten Dokumente wird im Produkttypsteckbrief des Konnektors
erhoben.

### 1.2 Zielgruppe

Das Dokument richtet sich an Konnektorhersteller sowie Hersteller und Anbieter
von Produkttypen (dies beinhaltet auch die Anbieter zur G2-Ausschreibung), die
hierzu eine Schnittstelle besitzen.

### 1.3 Geltungsbereich

Dieses Dokument enthält normative Festlegungen zur Telematikinfrastruktur des
Deutschen Gesundheitswesens. Der Gültigkeitszeitraum der vorliegenden Version
und deren Anwendung in Zulassungsverfahren werden durch die gematik GmbH in
gesonderten Dokumenten (z. B. Dokumentenlandkarte, Produkttypsteckbrief,
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

Spezifiziert werden in dem Dokument die von dem Produkttyp bereitgestellten
(angebotenen) Schnittstellen. Benutzte Schnittstellen werden hingegen in der
Spezifikation desjenigen Produkttypen beschrieben, der diese Schnittstelle
bereitstellt. Auf die entsprechenden Dokumente wird referenziert.

Die vollständige Anforderungslage für den Produkttyp ergibt sich aus weiteren
Konzept- und Spezifikationsdokumenten, diese sind in dem Produkttypsteckbrief
des Produkttyps Konnektor verzeichnet.

### 1.5 Methodik

### 1.5.1 Anforderungen

Anforderungen als Ausdruck normativer Festlegungen werden durch eine eindeutige
ID sowie die dem RFC 2119 [RFC2119] entsprechenden, in Großbuchstaben
geschriebenen deutschen Schlüsselworte MUSS, DARF NICHT, SOLL, SOLL NICHT,
KANN gekennzeichnet.

Sie werden im Dokument wie folgt dargestellt:

\<AFO-ID\> - \<Titel der Afo\>Text / Beschreibung[ \<=]Dabei umfasst die
Anforderung sämtliche innerhalb der Afo-ID und der Textmarke angeführten
Inhalte.

\<AFO-ID\> - *

Das Zeichen '*' steht hierbei für den Suffix der Anforderung. Es gilt der im
Dokumentenpaket gültige Suffix.

### 1.5.2 Offene Punkte

Zum Zeitpunkt der Spezifikationserstellung konnten nicht alle Details
abschließend geklärt werden, insbesondere, da Abstimmungsbedarf mit der
umsetzenden Industrie besteht. Details, die keine produkttypübergreifenden
Auswirkungen haben und die im Rahmen des Verhandlungsverfahrens mit der
Industrie besprochen werden müssen, werden als „Offene Punkte“ ausgewiesen
und wie folgt im Dokument kenntlich gemacht:

 ---> TABLE

### 1.5.3 Erläuterungen zur Spezifikation des Außenverhaltens

Der Konnektor stellt einen vergleichsweise komplexen Produkttyp dar, dessen
Beschreibung eine Herausforderung darstellt und somit in vielen verschiedenen
Varianten möglich wäre. An dieser Stelle folgen daher wesentliche
Informationen, die das korrekte Verstehen der Spezifikation fördern:

Die Spezifikation des Konnektors ist eine Black-Box-Spezifikation, das heißt
alle Festlegungen dienen ausschließlich der Beschreibung des von der
Komponente verlangten Verhaltens an der Außenschnittstelle.

Normative Festlegungen, die eine Festlegung des inneren Verhalten vermuten
lassen (beispielsweise die Definitionen der Technischen Use Cases - TUCs) sind
nur in so weit normativ, wie ihre Festlegungen auf die Außenschnittstelle
wirken. Sie legen explizit nicht die intern zu verwendende Implementierung
fest. Die Notwendigkeit für diese Art der „scheinbaren internen
Beschreibung“ ergibt sich aus der Komplexität der Gesamtkomponente, sowie
dem Bedarf, wiederholt ähnlich Verhaltensweisen in Außenschnittstellen
darstellen zu müssen. In diesem Fall werden die sich wiederholenden
Verhaltensanteile in internen TUCs zur editoriellen Wiederverwendung gekapselt.
Die konkrete konnektorinterne Modularisierung bleibt dem Hersteller
freigestellt. Insbesondere bleibt es dem Hersteller freigestellt, intern
bereits Mechanismen für kommende Releases zu realisieren, sofern diese an der
Außenschnittstelle keine Auswirkung zeigen.

Die einzige Abweichung von dieser Vorgehensweise ergibt sich für
Sicherheitsaspekte. Hier können interne Vorgänge normativ gefordert sein, die
sich an der Außenschnittstelle nicht manifestieren (Beispiel „Verpflichtung
auf sicheres Löschen eines temporären Schlüssels nach Gebrauch“). In
diesem Fall erfolgt die Überprüfung der Einhaltung dieser Anforderungen im
Rahmen der CC-Evaluierung.

### 1.5.4 Erläuterungen zur Dokumentenstruktur und „Dokumentenmechanismen“

### 1.5.4.1 Modulare Spezifikation über Funktionsmerkmale

Die Beschreibung des Konnektors erfolgt soweit wie möglich modular, d. h. alle
Aspekte, die für einen logischen Bereich relevant sind, werden in einem
Kapitel beschrieben. Diese logischen Bereiche werden als Funktionsmerkmal
bezeichnet.

Funktionsmerkmale kennzeichnet ein eigener Verantwortungsbereich. In diesen
Verantwortungsbereich greifen keine anderen Funktionsmerkmale ein. So kann ein
logischer Bereich vollständig durchdrungen werden, ohne dass in anderen
Kapiteln Anforderungen zu erwarten wären, die das Verhalten des
Funktionsmerkmals beeinflussen. Da zwischen Funktionsmerkmalen Wechselwirkungen
bestehen (Die Erkennung einer gesteckten Karte im Kartenterminaldienst löst
eine Reaktion im Kartendienst aus), wurden zur „dokumententechnischen
Interaktion“ zwischen Funktionsmerkmalen ein interner Event-Mechanismus sowie
Konfigurationsparameter und Zustandswerte eingeführt (siehe Folgekapitel).

Funktionsmerkmale bestehen (bis auf wenige Ausnahmen) immer aus folgenden
Unterkapiteln:

 ---> OL

Die Unterkapitel 1-5 dienen der funktionalen Beschreibung des Funktionsmerkmals.

Punkte, die zum Funktionieren des Funktionsmerkmals relevant sind:
Initialisierungsaspekte, durch den Administrator festzulegenden
Konfigurationsparameter etc., werden im Unterkapitel Betriebsaspekte erfasst.

In jedem Funktionsmerkmal sind immer alle Unterkapitel enthalten, auch wenn es
im konkreten Einzelfall dort keine Inhalte gibt. Diese feste Struktur innerhalb
der Funktionsmerkmale erleichtert die Orientierung und erhöht somit die
Lesbarkeit.

### 1.5.4.2 Technische Use Cases - TUCs

Innerhalb der Funktionsmerkmale in Kapitel 4 erfolgt eine Unterscheidung der
TUCs in solche, die nur durch die Basisdienste des Konnektors aufgerufen werden
dürfen (rein interne TUCs) und solche die neben den Basisdiensten auch durch
Fachmodule genutzt werden dürfen. Diese Unterteilung ergibt sich
ausschließlich aus dem Bedarf der editoriellen Steuerung der verschiedenen
Spezifikationen (Konnektor- und Fachmodulspezifikationen). Es besteht im Rahmen
der Implementierung des Konnektors keine Anforderung diese Trennung intern
durchzusetzen.

Die Beschreibung der TUCs erfolgt nach folgendem Muster:

 ---> UL

Dabei wird innerhalb der TUC-Tabelle in der Zeile „Standardablauf“
ausschließlich der Gut-Durchlauf beschrieben. Fehler, die innerhalb dieses
Ablaufs auftreten können, werden in der Zeile „Fehlerfälle“ erhoben.
Dabei wird auf die jeweilige Schrittnummer innerhalb des Ablaufs referenziert.
In dieser Tabellenzeile werden nur Fehlercodes erhoben, die im jeweiligen
Fehlerfall geworfen werden müssen. Die genauen Festlegungen zu den Fehlern,
neben Fehlercode auch: ErrorType, Severity und Fehlertext, werden in der
Fehlercodetabelle festgelegt.    

Die Spezifikation, in der ein TUC definiert wird, ist an den mittleren drei
Buchstaben der TUC-Referenz zu erkennen:

 ---> UL

Festlegungen zur Schreibweise von Eingangs- und Ausgangsdaten von TUCs

a) Eingangs- und Ausgangsparameter werden in TUC-Tabellen wie folgt beschrieben:

Name des Eingangs- bzw. Ausgangsparameters

gefolgt von(falls definiert):[Datentyp]

gefolgt von(falls zutreffend):

-optional; default: \<Defaultwert\>bzw.

-optional;/\<erklärender Text\>  

Hierbei bedeuten:- optional;kennzeichnet optionale Ein- und Ausgangsparameter

default: \<Defaultwert\>definiert den Defaultwert für den Fall, dass der
Eingangsparameter leer ist bzw. nicht übergeben wurde

/\<erklärender Text\>beschreibt Bedingungen, unter denen der Eingangsparameter
optional ist

    gefolgt von(falls vorhanden):(\<erklärender Text\>)

b) Namen mit kleinem Anfangsbuchstaben bezeichnen Ein- und Ausgangsparameter;
Namen mit großem Anfangsbuchstaben bezeichnen Datentypen.

Beispiel:

 ---> TABLE

Die im Dokument verwendeten Datentypen sind definiert in [Anhang L –
Datentypen von Eingangs- und Ausgangsdaten].

Festlegungen zur Schreibweise des Aufrufs von TUCs

Ein TUC-Aufruf erfolgt nach folgendem Muster:

\<TUC-Bezeichner\> {

   \<TUC-Eingangsparameter Name\> = \<TUC Eingangsparameter Wert\>;

   … }

Beispiel:

TUC_KON_256 {    topic = „CT/DISCONNECTED“;    eventType =
Op;    severity = Info;    parameters = („CtID=$CT.CTID,
Hostname=$CT.HOSTNAME“) }

Vereinfachung:

Ist \<TUC-Eingangsparameter Name\> des aufzurufenden TUCs gleich der Variablen,
die als \< TUC Eingangsparameter Wert\> gesetzt wird, so kann dieser Bezeichner
ohne Zuweisung geschrieben werden.

Beispiel: (cardSession und pinRef sind Eingangsdaten des aufrufenden TUCs):

TUC_KON_022 „Liefere PIN-Status“ {cardSession=cardSession; pinRef=pinRef}

vereinfachte Schreibweise:

TUC_KON_022 „Liefere PIN-Status“ {cardSession; pinRef}

### 1.5.4.3 Event-Mechanismus

Der in Kapitel 4.1.6 spezifizierte Event-Mechanismus zur Unterrichtung von
Clientsystemen wird innerhalb dieser Spezifikation auch zur internen Verzahnung
der einzelnen Funktionsmerkmale eingesetzt. So wird ein Ereignis, das in der
Managementschnittstelle durch Änderung eines Konfigurationsparameters
ausgelöst wird, innerhalb des DHCP-Kapitels als Trigger für eine
Lease-Erneuerung verwendet. Dies bedeutet nicht, dass im Rahmen der
Implementierung intern ein Event-Mechanismus zwischen den Modulen verwendet
werden muss. Auch hier dient die Form der Darstellung (Events) lediglich der
editoriellen Kopplung verschiedener Verhaltensbeschreibungen.

Um den Ursprung eines Events erkennen zu können, verwenden alle Events ein
Haupt-Topic passend zum Funktionsmerkmal: „DHCP/LAN_CLIENT/RENEW” wird im
Funktionsmerkmal DHCP ausgelöst, „CARD/INSERTED” wird im Funktionsmerkmal
Kartendienst ausgelöst usw.     

### 1.5.4.4 Konfigurationsparameter und Zustandswerte

Werte die der Administrator des Konnektors einsehen oder verändern können
muss, werden zusätzlich zu den Festlegungen in Kapitel 4.3 Konnektormanagement
auch pro Funktionsmerkmal in den jeweiligen Unterkapiteln „Betriebsaspekte“
erhoben. DieseKonfigurationsparameterwerden über eine ReferenzID definiert.
Definierte Konfigurationsparameter können in allen Kapiteln der Spezifikation
referenziert werden. Den Ort, an welchem ein solcher Konfigurationsparameter
definiert/erhoben und somit dessen Bedeutung beschrieben wird, lässt sich
über den Präfix der ReferenzID erkennen:CERT_CRL_DOWNLOAD_ADDRESS(also
„Cert“) wird im Zertifikatsdienst definiert,MGM_LU_ONLINE(also „MGM“)
wird im Konnektormanagement definiert usw.

Die ReferenzIDs der Konfigurationsparameter besitzen in ihrer Schreibweise nur
innerhalb des Dokuments Gültigkeit. In der Umsetzung können für die
Konfigurationswerte herstellerspezifische Beschreibungen und Labels verwendet
werden.

Vergleichbar zu diesen Konfigurationsparametern, sindZustandswerte.Auch diese
werden über ReferenzIDs definiert, nur können sie nicht durch den
Administrator verändert oder eingesehen werden. Sie finden nur konnektorintern
Verwendung und sind für die Beschreibung der Verhaltensweise notwendig,
Beispiele sindCTM_CT_LISTfür die Liste der durch den Konnektor verwalteten
Kartenterminals oderCM_CARD_LISTfür die Liste der aktuell erreichbaren Karten.
Zustandswerte verwenden die gleichen Präfixe wie Konfigurationsparameter.

### 2 Systemüberblick

Der Konnektor ist ein Produkttyp der TI gemäß [gemKPT_Arch_TIP#5.3.9].

Er bietet seine Basisdienste sowohl intern den in ihm laufenden Fachmodulen an,
als auch externen Clientsystemen über die Konnektoraußenschnittstellen.

Im lokalen Netz der Einsatzumgebung kommuniziert das Clientsystem mit dem
Konnektor über dessen LAN-seitiges Ethernet-Interface. Alleinig der Konnektor
kommuniziert mit den in lokalen Netzen angeschlossenen Kartenterminals und
Karten. Auch die Kommunikation mit den zentralen Diensten der TI-Plattform und
fachanwendungsspezifischen Diensten erfolgt ausschließlich über den Konnektor
über dessen WAN-seitiges Ethernet-Interface.

Abbildung PIC_KON_116 stellt die Schnittstellen im Umfeld des Konnektors dar.

![Abbildung-1][Abbildung-1]

Die logischen Außenschnittstellen aus [gemKPT_Arch_TIP] werden im Konnektor
technisch vorrangig als SOAP-Schnittstellen ausgeprägt. Von dieser Regel wird
insbesondere bei Netzwerkschnittstellen abgewichen, wenn bereits etablierte
Schnittstellenstandards für Basisdienste existieren (IPsec, TLS, NTP, DNS
etc.). Eine Übersicht der Zuordnung „logische Schnittstellentechnische
Schnittstellen“ findet sich in Anhang H.

Zum Nachweis der Sicherheit müssen Konnektoren im Rahmen der Zulassung nach
Common Criteria gegen die Schutzprofile [PP_NK] und [PP_KON] evaluiert und
zertifiziert werden.

Die zu verwendenden kryptographischen Verfahren und zugehörige Parameter
(z. B. Schlüssellängen) für alle kryptographischen Operationen innerhalb
der Telematikinfrastruktur, werden durch das Dokument „Verwendung
kryptographischer Algorithmen in der Telematikinfrastruktur“ [gemSpec_Krypt]
normativ geregelt.

### 2.1 Logische Struktur

Der Produkttyp Konnektor besitzt eine Vielzahl verschiedenster Operationen und
Verhaltensweisen an seiner Außenschnittstelle. Um sein komplexes
Gesamtverhalten sinnvoll beschreiben zu können, wird der Konnektor innerhalb
dieser Spezifikation logisch unterteilt und strukturiert. Es wird primär
zwischen Anwendungs- und Netzkonnektor unterschieden, begleitet von
Mechanismen, die blockübergreifend beschrieben werden.

Der logische Aufbau des Konnektors ist in Abbildung PIC_KON_117 dargestellt.

 ---> UL

![Abbildung-2][Abbildung-2]

Diese logische Unterteilung schreibt in keiner Art und Weise die spätere
Implementierung durch den Hersteller vor. Der Hersteller kann seine interne
Modularisierung des Konnektors frei wählen. Normativ wirksam ist
ausschließlich das durch die Detailfestlegungen in Summe beschriebene
Verhalten an den Außenschnittstellen des Konnektors als Ganzes.

### 2.2 Sicherer Datenspeicher

Wie im vorherigen Kapitel dargestellt, wird für den Konnektor ein Datenspeicher
angenommen, in welchem der Konnektor alle sicherheitskritischen,
veränderlichen Daten dauerhaft speichert, die für seinen Betrieb relevant
sind. Dieser Datenspeicher sichert die Integrität, Authentizität und
Vertraulichkeit der in ihm hinterlegten Daten bzw. der aus ihm entnommenen
Daten. Alleinig der Konnektor hat auf diesen Datenspeicher Zugriff. Für
folgende, im weiteren Verlauf der Spezifikation anfallende Daten wird
angenommen, dass diese im Sicheren Datenspeicher persistiert werden:

 ---> UL

Ferner stellt der Konnektor den in ihm laufenden Fachmodulen ebenfalls eine
Nutzung dieses Datenspeichers für ihre sensiblen Daten zur Verfügung.

Da es sich bei dem Sicheren Datenspeicher um ein internes Modul handelt, welches
an der Außenschnittstelle nicht testbar ist, werden an dieses Modul im Rahmen
dieser Spezifikation keine Anforderungen erhoben. Da dieses logische Modul aber
essenzielle Sicherheitsfunktionen bietet, ohne die ein Konnektor nicht sicher
betrieben werden kann, werden die Funktionen, die ein Hersteller für sein
Konnektormodell real umsetzt, um die notwendigen sicheren Speicherfunktionen zu
realisieren, im Rahmen der CC-Evaluierung geprüft werden. Näheres hierzu
regeln die Schutzprofile des Konnektors.

### 2.3 Überblick Konnektoridentität

Die Geräteidentität des Konnektors (Konnektoridentität) teilt sich in drei
Identitäten auf:

 ---> UL

In der Regel ergibt sich aus dem Kontext, welche Identität gemeint ist, sodass
in diesen Fällen nur kurz von der Konnektoridentität geschrieben wird.

Die Geräteidentitäten werden durch asymmetrische Schlüssel und
X.509-Zertifikate umgesetzt. In Abhängigkeit vom gewählten kryptographischen
Verfahren werden RSA-Schlüssel bzw. ECC-Schlüssel verwendet.

### 2.4 Mandantenfähigkeit

Den Anforderungen aus [gemKPT_Arch_TIP#TIP1-A_2200] folgend, wird die
Mandantenfähigkeit innerhalb des Konnektors nicht durch eine einzelne
Funktion, sondern durch Berücksichtigung in einer Reihe von Funktionsmerkmalen
umgesetzt.

Die Mandantenfähigkeit wirkt dabei auf:

 ---> UL

### 2.5 Versionierung

Gemäß [gemSpec_OM] müssen Konnektor und Kartenterminals über eine
Versionierung verfügen. Die relevanten Versionsinformationen sind durch das
O&M-Schema ProductInformation.xsd definiert. Ferner definiert [gemSpec_OM],
dass Konnektor und Kartenterminal das Konzept der Firmware-Gruppe verwenden
müssen. Daher verfügen die beiden Produkttypen auch über eine aktuelle
Firmware-Gruppenversion.

Versionsinformationen werden innerhalb des Konnektor an folgenden Stellen ver-
und bearbeitet:

 ---> UL

### 2.6 Fachanwendungen

Der Konnektor ist als Plattformkomponente der TI für die Erbringung von
Basisdiensten verantwortlich. Fachliche Funktionalitäten werden über die
Fachmodule bereitgestellt.

Das Fachmodul wird dabei als integraler Bestandteil des Konnektors verstanden
(Konnektor als Monolith), d. h., die Spezifikationen zu Konnektor (als
Plattformkomponente) und dem Fachmodul sind zwar getrennt, werden aber von
einem Hersteller in einer Gesamtkomponente umgesetzt. Die inneren
Schnittstellen zwischen Fachmodul und Konnektor sind von außen nicht erkennbar.

In dieser Ausbaustufe unterstützt der Konnektor die Fachanwendungen VSDM,
AMTS, NFDM und ePA über jeweils ein Fachmodul.

Neben Fachanwendungen, die über ihr Fachmodul mit einem gesicherten Fachdienst
kommunizieren, unterstützt der Konnektor einen Zugriff von Clientsystemen auf
offene Fachdienste.

### 2.7 Netzseitige Einsatzszenarien

Der Konnektor unterstützt unterschiedliche netzseitige Einsatzszenarien, die in
Anhang K beispielhaft dargestellt sind.

Der Konnektor bietet hierzu Konfigurations-Parameter, die je nach netzseitigem
Einsatzszenario konfiguriert werden müssen.

### 2.7.1 Parameter ANLW_ANBINDUNGS_MODUS

Konfiguration 1: Konnektor als Gateway (ANLW_ANBINDUNGS_MODUS = InReihe):Diese
Konfiguration ist geeignet für Szenarien, in denen der Konnektor zwischen das
lokale Netz und das Internet Access Gateway (IAG) (z. B. Router mit
DSL-/Kabelmodem) geschaltet wird. (vgl. Anhang K, Szenario 1)

Konfiguration 2: Konnektor eingebettet in existierende Infrastruktur
(ANLW_ANBINDUNGS_MODUS = Parallel):Diese Konfiguration ist geeignet für
Szenarien, in denen der Konnektor als weiteres Gerät in die bestehende
Netzwerkinfrastruktur integriert wird. (vgl. Anhang K, Szenario 3)

Aus Sicherheitsgründen soll die Kommunikation der Clientsysteme mit dem
Konnektor hierbei verschlüsselt erfolgen (ANCL_TLS_MANDATORY=Enabled). Falls
diese Kommunikation unverschlüsselt erfolgt (ANCL_TLS_MANDATORY=Disabled),
übernimmt der Nutzer die Verantwortung für die Sicherstellung der
vertraulichen Übertragung.

Für den Einsatz und die Nutzung von DHCP gibt es im Zusammenhang mit diesem
Konfigurationsparameter folgende Möglichkeiten:

 ---> UL

Die DHCP-Konfiguration ist in Konfiguration 1 in aller Regel die folgende: Die
WAN-Seite des Konnektors verwendet den DHCP-Server des bestehenden IAG. An der
LAN-Seite stellt der Konnektor einen DHCP-Server für alle Clients zur
Verfügung.

### 2.7.2 Parameter ANLW_INTERNET_MODUS

Grundsätzlich routet der Konnektor im Modus ANLW_INTERNET_MODUS=SIS alle für
das Internet bestimmten Pakete von Clients, die ihn als Default Gateway
verwenden, in den VPN-Tunnel zum SIS, während er im Modus
ANLW_INTERNET_MODUS=Keiner diese Pakete verwirft.

Im Unterschied zu (ANLW_ANBINDUNGS_MODUS = InReihe) ist die Nutzung des SIS bei
(ANLW_ANBINDUNGS_MODUS = Parallel) optional. Alternativ können auch die
Clients, die den Konnektor als Default Gateway verwenden, per Redirect direkt
ins Internet verwiesen werden (ANLW_INTERNET_MODUS=IAG).

### 2.8 Lokale und entfernte Kartenterminals

Gemäß [gemKPT_Arch_TIP] ermöglicht die Telematikinfrastruktur dem Anwender
die PIN-Eingabe zur Freischaltung eines HBAs oder einer SMC-B wahlweise lokal
oder über das Remote-PIN-Eingabeverfahren durchzuführen. Deshalb
unterscheidet auch der Konnektor zwischen einem lokalen Kartenterminal –
räumlich („in Sichtweite“) dem Arbeitsplatz zugeordnet – und einem
entfernten Kartenterminal.

Ein lokales Kartenterminal befindet sich lokal an einem Arbeitsplatz und kann
von diesem aus genutzt werden. Hingegen ist das entfernte Kartenterminal einem
entfernten oder auch – für zentral steckende Karten – keinem Arbeitsplatz
fest zugewiesen. Ein lokales Kartenterminal kann als sogenanntes Remote-PIN-KT
verwendet werden, um die PIN für eine in einem entfernten Kartenterminal
steckende Karte einzugeben.

### 2.9 Standalone-Szenario

Gemäß § 291 Absatz 2b SGB V müssen „Diese Dienste [zur
Online-Aktualisierung der Versichertendaten auf der eGK] […] auch ohne
Netzanbindung an die Praxisverwaltungssysteme der Leistungserbringer online
genutzt werden können.“

Dies bedeutet, dass der Konnektor ohne ein steuerndes Clientsystem
ereignisgetrieben Fachanwendungen ausführen können muss. Aus Fachsicht
„steht der Konnektor alleine“, ohne Clientsysteme. Die konkreten Aktionen,
die Fachanwendungen in diesen Fällen ausführen, sowie deren Auslöser werden
in den jeweiligen Fachmodulspezifikationen beschrieben.

Ein solcher alleinstehender Konnektor mit Zugang zur TI muss zur Durchführung
der Fachanwendungen durch einen weiteren Konnektor unterstützt werden, der in
direkter Verbindung zum Clientsystem steht, selbst aber keine Online-Anbindung
besitzt.

### 3 Übergreifende Festlegungen

Für die folgenden Inhalte bitte die Hinweise in Kapitel 1.5.3 „Erläuterungen
zur Spezifikation des Außenverhaltens" sowie Kapitel 1.5.4 Erläuterungen zur
Dokumentenstruktur und „Dokumentenmechanismen“ beachten.

In diesem Kapitel werden die Aspekte des Konnektors behandelt, die
Funktionsmerkmalübergreifend geregelt werden müssen.

Die Managementschnittelle/Administrationsoberfläche des Konnektors wird dabei
nicht als übergreifender Aspekt, sondern als eigenes Funktionsmerkmal
gewertet. Die Festlegungen hierzu finden sich entsprechend in Kapitel 4.3.

### 3.1 Allgemeine übergreifende Festlegungen

### 3.1.1 Dokumentformate

Mit dem Aufruf einer Operation, die Dokumente verarbeitet, muss durch den
Aufrufer festgelegt werden können, um welches Dokumentenformat es sich
handelt, damit die unterschiedlichen Formate zur Verarbeitung und etwaigen
Anzeige unterschieden werden können. Die nicht-XML-Formate werden dabei nach
MIME-Typ-Klassen unterschieden:

 ---> UL

Folgende Bezeichner werden verwendet:

Alle_DocFormate:      XML, PDF/A, Text, TIFF, Binär

nonQES_DocFormate:    XML, PDF/A, Text, TIFF, Binär

QES_DocFormate:        XML, PDF/A, Text, TIFF

Für nonQES_DocFormate wird, trotz Gleichheit zu Alle_DocFormate, ein eigener
Referenzbezeichner verwendet, da sich diese Liste noch ändern könnte. TIFF
wird durch [gemKPT_Arch_TIP] nicht für die nonQES verlangt. Die Unterstützung
dieses Formats für nonQES bedeutet jedoch keinen Mehraufwand, da die Routinen
durch QES bereits implementiert sind und nachgenutzt werden können.

##### TIP1-A_4500-02

Der Konnektor MUSS für alle Außenschnittstellen, in denen ein Dokument
verarbeitet wird, Dokumente mit einer Größe \<= 25 MB (26.214.400 Byte)
unterstützen. Der Konnektor DARF NICHT Dokumente mit einer Größe \> 25
MB (26.214.400 Byte) unterstützen. **[\<=]**

##### A_19052-01

Der Konnektor MUSS bei der Verarbeitung von Dokumenten und Nachrichten die
Mindestanforderungen aus TAB_KON_775erfüllen. Wenn vom Aufrufer übergebene
Dokumente oder Nachrichten die vom Konnektor unterstützte Dimensionierung
überschreiten, MUSS der Konnektor die Verarbeitung mit Fehler 4280 abweisen.

Tabelle1Fehlercodes TAB_KON_890 Mindestanforderungen an Dokumente und
Nachrichten

 ---> TABLE

**[\<=]**

##### A_22673

Der Konnektor MUSS bei der Verarbeitung von Dokumenten und Nachrichten die
Einhaltung der Vorgaben aus TAB_KON_889sicherstellen. Wenn vom Aufrufer an den
Konnektor übergebene Dokumente oder Nachrichten gegen Vorgaben aus
TAB_KON_778 verstoßen, MUSS der Konnektor die Verarbeitung mit Fehler 4281
abbrechen.

Tabelle2Fehlercodes TAB_KON_891 Unerlaubte Inhalte in Dokumenten und Nachrichten

 ---> TABLE

**[\<=]**

##### A_22923

Der Konnektor DARF in XML-Dokumenten- und Nachrichten enthaltene Attribute
schemaLocation und noNamespaceSchemaLocation NICHT auswerten. **[\<=]**

##### TIP1-A_4502

Der Konnektor MUSS bei der Verarbeitung von Dokumenten der Formate XML und Text
die Zeichensatzkodierungen UTF-8 und ISO-8859-15 unterstützen. Das
verarbeitete Dokument MUSS der Konnektor mit demselben Zeichensatz kodieren, in
dem das Eingangsdokument kodiert war. **[\<=]**

##### TIP1-A_5541-01

Der Konnektor DARF in Dokumenten eventuell vorhandene Referenzen auf externe
Ressourcen NICHT auflösen, es sei denn es sind Verweise auf im Konnektor
sicher eingebrachte vorliegende Schemata oder dies wird im Einzelfall
normativ gefordert. **[\<=]**

### 3.1.2 Kartentypen

Der Konnektor unterstützt eine Reihe von Kartentypen. Die folgende Tabelle
enthält die Liste der Referenzbezeichner für die verschiedenen Kartentypen,
wie sie im weiteren Verlauf verwendet werden. Die Unterstützung von Karten der
Generation 2 (G2.x: G2.0, G2.1 und höher) beschränkt sich bei diesen auf die
Datenstrukturen und Schlüssel, die aus Gründen der Abwärtskompatibilität zu
den Karten der Generation 1+ vorhanden sind. Eine Ausnahme hiervon bilden die
Geräte-CVCs, die bereits für dieses Release basierend auf ECC verwendet
werden.

 ---> TABLE

### 3.1.3 Übergreifende Festlegungen zum Aufbau von sicheren Verbindungen

##### TIP1-A_7254

Der Konnektor MUSS beim Aufbau von TLS-gesicherten Verbindungen zu einem
zentralen Dienst der TI-Plattform oder zu einem fachanwendungsspezifischen
Dienst, bei denen eine OCSP-Abfrage des Serverzertifikats nach TUC_PKI_006
erfolgt, neben Fehlerfällen bei folgenden Warnungen gemäß
[gemSpec_PKI#Tab_PKI_274]

 ---> UL

mit Abbruch des Verbindungsaufbaus reagieren. **[\<=]**

In [gemSpec_Krypt#6] wird das Kommunikationsprotokoll zwischen einem Client und
einer Vertrauenswürdigen Ausführungsumgebung (VAU) spezifiziert. Dabei wird
ein sicherer Kanal auf HTTP-Anwendungsschicht zwischen dem Client und der VAU
(Server) aufgebaut. Der Client ist hier ein Fachmodul des Konnektors; der
Server ist ein Fachdienst.

##### A_17225-01

Der Konnektor MUSS für Fachmodule den Aufbau einer sicheren Verbindung zur
Vertrauenswürdigen Ausführungsumgebung (VAU) gemäß Kommunikationsprotokoll
[gemSpec_Krypt#6] unterstützen und das vom Server übergebene Zertifikat wie
folgt prüfen:TUC_KON_037 „Zertifikat prüfen“  {       certificate
= C.FD.AUT;       qualifiedCheck = not_required;     
 offlineAllowNoCheck = false;       policyList  = oid_fd_aut;    
  intendedKeyUsage= intendedKeyUsage(C.FD.AUT);     
 validationMode  = OCSP}Der Konnektor MUSS die vom Fachmodul übergebene
Rolle gegen die aus dem Zertifikat ermittelte Rolle prüfen.   **[\<=]**

##### A_17777

Der Konnektor MUSS für Fachmodule für die Nutzung der
Schlüsselableitungsfunktionalität die sicherheitstechnischen Festlegungen
gemäß [gemSpec_Krypt#3.15.5 Schlüsselableitungsfunktionalität ePA] und
[gemSpec_SGD] bereitstellen. **[\<=]**

Der Gesamtablauf der Schlüsselableitungsfunktionalität gemäß
[gemSpec_SGD#2.3] für den Konnektor als Client ist aufgeteilt zwischen
Basiskonnektor und Fachmodul. Die kryptographischen Vorgaben (u.a.
Durchführung des ECDH, Schlüsselerzeugung, Ver- und Entschlüsselung,
Signaturerzeugung und -prüfung) werden dabei durch den Basiskonnektor
realisiert.

### 3.2 Konnektoridentität und gSMC-K

##### TIP1-A_4503

Der Konnektor MUSSdas geheime Schlüsselmaterial zur
Geräteidentität(ID.NK.VPN, ID.AK.AUT, ID.SAK.AUT)und der Rolle
SAK(C.SAK.AUTD_CVC) über Smartcards des Typs gSMC-Kgemäß
[gemSpec_gSMC-K_ObjSys]nutzen.Der Konnektor MUSS mit einer gSMC-K bestückt
sein. Er KANN mit mehr als einer gSMC-K bestückt sein. **[\<=]**

Die Notwendigkeit, den Konnektor mit mehr als einer gSMC-K zu bestücken, kann
sich aus den Lastanforderungen aus [gemSpec_Perf#4.1.2] ergeben.

##### TIP1-A_4504

Verwendet der Konnektor mehrere gSMC-Ks, DARF eine Administratorinteraktion für
diese Belange NICHT erforderlich sein. **[\<=]**

##### TIP1-A_5543

Der Konnektor DARF Anwender und Administratoren außer bei der Inbetriebnahme
(erstmalig oder nach Werksreset) NICHT auffordern, eine PIN für eine gSMC-K
einzugeben. **[\<=]**

##### TIP1-A_4505

Die gSMC-Kdes Konnektors MÜSSENdurch den Einsatz physikalischer Sperren oder
manipulationssicherer Siegelso mit dem Konnektor verbunden sein,
dassphysischerMissbrauch oder physische Manipulationerkennbar ist. **[\<=]**

gSMC-Ks gemäß [gemSpec_gSMC-K_ObjSys] verfügen über die Möglichkeit zur
nachträglichen Generierung von Schlüsselpaaren und dem Nachladen der
zugehörigen Zertifikate. Dieser Mechanismus wird erst in kommenden Releases
durch den Konnektor unterstützt. Initial sind alle Identitäten bereits einmal
auf der gSMC-K vorhanden.

##### TIP1-A_4506

In Abhängigkeit vom kryptographischen Verfahren MUSSder Konnektor folgende
Objekte der gSMC-K als Quelle seiner Identitäten verwenden:

Tabelle4: TAB_KON_856: Identitäten des Konnektors auf der gSMC-K

 ---> TABLE

**[\<=]**

##### A_21849

Der Konnektor MUSS dem Administrator anzeigen, welche Zertifikate aktuell
verwendet werden. Dies gilt für diese Strecken bzw. Anwendungsfälle:
VPN-Tunnel (C.NK.VPN), TLS zum PS (C.AK.AUT oder lokales Zertifikat), TLS zum
KT (C.SAK.AUT) und C2C für SUK (C.SAK.AUTD_CVC und C.CA_SAK.CS). **[\<=]**

### 3.2.1 Organisatorische Anforderungen und Sperrprozesse

##### TIP1-A_5392

Der Hersteller des Konnektors MUSS die Rolle des Kartenherausgebers für in
seinen Konnektoren verbauten gSMC-Ks einnehmen.

Der Hersteller des Konnektors KANN die von ihm verantwortete Personalisierung
der gSMC-K durch einen von ihm zu beauftragenden Dienstleister in seinem Namen
vornehmen lassen. **[\<=]**

##### TIP1-A_5696

Der Hersteller des Konnektors MUSS sich von der korrekten Personalisierung der
herausgegebenen gSMC-K überzeugen. **[\<=]**

##### A_18928

Der Hersteller des Konnektors MUSS die Konnektoren mit einer gSMC-K mit
personalisierten RSA- und ECC-Zertifikaten gemäß TAB_KON_856 ausstatten.
**[\<=]**

##### A_18930

Der Konnektor MUSS unterschiedliche gSMC-K-Personalisierungsvarianten sowohl mit
als auch ohne ECC-Zertifikate für ID.NK.VPN, ID.AK.AUT und ID.SAK.AUT
unterstützen. **[\<=]**

Die Anforderung ist für die Anwendungsfälle Registrierung,
IPsec-Authentisierung und Autorisierung beim VPN-Zugangsdienst,
TLS-Authentisierung zum eHealth-Kartenterminal, TLS-Authentisierung zum
Primärsystem nachzuweisen. Wenn RSA-2048 in der TI abgekündigt wird,
entfällt dadurch die Anforderung.

##### TIP1-A_5393

Der Hersteller des Konnektors MUSS die Zuordnung von Konnektor und jeweils
eingebrachtem C.NK.VPN-Zertifikat mit dem Ziel dokumentieren, anhand eines
Sperrauftrages für einen Konnektor, das zu sperrende C.NK.VPN-Zertifikat
identifizieren zu können. **[\<=]**

Das bedeutet, dass der Konnektorhersteller je Konnektor die für die
Identifikation des C.NK.VPN-Zertifikates relevanten Daten wie z. B.
Seriennummer des Konnektors und Art der verbauten Komponenten, Seriennummer der
gSMC-K, etc. für seinen Sperrprozesse dokumentieren muss.

##### TIP1-A_5394

Der Hersteller des Konnektors MUSS für die von ihm verantworteten Konnektoren
einen Sperrprozess etablieren, unterhalten und der gematik zugänglich machen.

Der Hersteller des Konnektors KANN die operative Durchführung des
Sperrprozesses an Dritte delegieren. **[\<=]**

Sperrberechtigt ist die gematik im Rahmen des Change-Verfahrens (siehe
[gemRL_Betr_TI#5.4).

##### TIP1-A_5395

Der Hersteller des Konnektors MUSS im Rahmen der Change-Durchführung erteilte
Sperraufträge der gematik fristgemäß (gemäß Change-Auftrag) bei dem TSP
X.509 nonQES (Zertifikatsaussteller) umsetzen. **[\<=]**

Dazu bedient er die standardmäßige Schnittstelle zum TSP (siehe
[gemSpec_X.509_TSP#TIP1-A_3643]).

##### TIP1-A_5396

Der Hersteller des Konnektors MUSS vor der Umsetzung des Sperrauftrages für
einen Konnektor die Sperrberechtigung des Beauftragenden prüfen und
verhindern, dass Konnektoren missbräuchlich gesperrt werden. **[\<=]**

##### TIP1-A_5397

Der Hersteller des Konnektors MUSS nach erfolgreicher Prüfung der
Sperrberechtigung des Beauftragenden die Sperrung der entsprechenden
C.NK.VPN-Zertifikate unverzüglich bei dem TSP X.509 nonQES
(Zertifikatsaussteller) beauftragen. **[\<=]**

##### TIP1-A_5398

Der Hersteller des Konnektors DARF NICHT die Sperrung von C.NK.VPN-Zertifikaten
bei dem TSP X.509 nonQES (Zertifikatsaussteller) beauftragen, wenn er nicht
durch einen für den Konnektor Sperrberechtigten dazu beauftragt wurde. **[\<=]**

##### TIP1-A_5399

Der Hersteller des Konnektors MUSS die Durchführung der Sperrung eines
Konnektors protokollieren und der gematik auf Anfrage übermitteln.Dabei
MÜSSEN folgende Informationen protokolliert werden:

 ---> UL

**[\<=]**

Der Hersteller des Konnektors übernimmt im Rahmen der organisatorischen
Sperrung die Aufgabe der Anwenderkommunikation gegenüber den betroffenen
Anwendern. Die Eckpunkte zur Kommunikation sind Bestandteil des Beschlusses zur
Außerbetriebnahme einer Konnektor-Baureihe und im Rahmen des Change-Verfahrens
zwischen den Beteiligten abgestimmt.

##### TIP1-A_5400

Der Hersteller des Konnektors MUSS die Fortführung des Sperrprozesses über die
Einstellung seiner Geschäftstätigkeit hinaus gewährleisten. **[\<=]**

Dies kann bspw. durch Übertragung der Aufgabe an einen Dritten realisiert
werden. Dabei sind die Zuordnungen Konnektor zu Zertifikat gemäß Anforderung
„Dokumentation der Konnektorzertifikatszuordnungen“ zur Verfügung zu
stellen.

Bei der Schlüsselerzeugung für die gSMC-K muss insbesondere auch mit
technischen Maßnahmen die Vertraulichkeit der relevanten Schlüssel
sichergestellt werden:

##### TIP1-A_7225

Der Hersteller des Konnektors, der Schlüssel für die gSMC-K erzeugt, MUSS
diese Schlüssel mittels eines technischen Sicherheitsmoduls (HSM, Chipkarte,
TPM etc.) erzeugen, welches

 ---> OL

Wird für die Schlüsselerzeugung eine Schlüsselableitung verwendet, so MUSS
die Schlüsselableitung die fachlichen Anforderungen aus GS-A_5386 erfüllen.

Es ist zulässig, dass asymmetrische Schlüssel bei der Personalisierung auf der
gSMC-K selbst erzeugt werden und symmetrische Schlüssel mittels einer
Schlüsselableitung erzeugt werden, bei dem sich der Ableitungsschlüssel
(Masterkey) innerhalb eines nach 3. zulässigen Hardwaresicherheitsmoduls
befindet.

Es ist zulässig, sicherheitstechnisch geeignete Maßnahmen zur Sicherstellung
der Verfügbarkeit der Ableitungsschlüssel (Masterkey) umzusetzen (bspw.
Shamir Secret-Sharing-Verfahren).

Der Hersteller des Konnektors MUSS die Schlüsselerzeugung und die
Schlüsselverwaltung in einem Konzept darstellen, das die technischen und
organisatorischen Maßnahmen beschreibt, die den Schutzbedarf der verarbeiteten
Informationsobjekte befriedigen. Der Hersteller des Konnektors MUSS dieses
Konzept der gematik zur Verfügung stellen. **[\<=]**

##### TIP1-A_5703

Der Hersteller des Konnektors, der Daten für die gSMC-K erzeugt (bspw.
Schlüssel), MUSS diese Daten bei der Übertragung zum Kartenpersonalisierer
hinsichtlich Vertraulichkeit, Authentizität und Integrität mit einem
Verfahren nach [gemSpec_Krypt] schützen. **[\<=]**

### 3.3 Bootup-Phase

##### TIP1-A_4507

Da während der Bootup-Phase des Konnektors noch nicht alle
Sicherheitsmechanismen ihre Leistung erbringen können, DÜRFEN die Dienste des
Konnektorswährend dem Bootup über physikalische Schnittstellen von außen
NICHT erreichbar sein. **[\<=]**

##### TIP1-A_4508

Der Konnektor MUSS nach Beendigung der Bootup-Phase die Initialisierung der
Funktionsmerkmale durchlaufen haben. Die Startreihenfolge der Funktionsmerkmale
kann unter Berücksichtigung von TIP1-A_4507 herstellerspezifisch gestaltet
werden.Im Rahmen der Bootup-Phase MÜSSEN folgende TUCs ausgeführt werden:
TUC_KON_025, TUC_KON_035, TUC_KON_272, TUC_KON_341, TUC_KON_343, TUC_KON_352
(die Reihenfolge der TUC-Ausführung ist herstellerspezifisch).Treten während
der Bootup-Phase Fehler auf, so MUSS die Bootup-Phase, sofern möglich,
abgeschlossen werden.Sobald die Bootup-Phase abgeschlossen ist, MUSS
TUC_KON_256 „Systemereignis absetzen“ mit folgenden Parameter aufgerufen
werden:TUC_KON_256 {    topic = "BOOTUP/BOOTUP_COMPLETE";    eventType
= Op;    severity = Info;    } **[\<=]**

Die hier gelisteten TUCs bilden nicht die abschließende Menge der während der
Bootup-Phase zu erfüllenden Anforderungen. In den einzelnen Funktionsmerkmalen
werden weitere Einzelanforderungen erhoben, die als Ausführungszeitpunkt die
Bootup-Phase benennen (siehe Unterkapitel „Betriebsaspekte“ der einzelnen
Funktionsmerkmal-Kapiteln, sowie Kapitel 4.3 Konnektormanagement).

### 3.4 Betriebszustand

##### TIP1-A_4509

Der Konnektor MUSS seinen Betriebszustand gemäß Tabelle TAB_KON_503
Betriebszustand_Fehlerzustandsliste über Fehlerzustände $EC erfassen.

Tritt die in Spalte „Beschreibung“ charakterisierte Fehlersituation eines
Fehlerzustandes $EC ein, wird sein Wert $EC.value = true. Sobald die
Fehlersituation beendet ist, springt der Wert auf $EC.value = false. Die
Fehlerzustände müssen dabei innerhalb der „max. Feststellungszeit“
(Tabellenspalte) erfasst werden. Eine maximale Feststellungszeit von einen Tag
(1 day) verlangt, dass einmal am Tag der Zustand geprüft werden muss,
unabhängig davon, welche TUCs aufgerufen werden. Eine maximale
Feststellungszeit von 1 sec, 10 sec, 1 min und 300 sec verlangt, dass nach der
Feststellung einer Fehlfunktion innerhalb eines TUCs die Zustandsänderung
innerhalb der angegebenen Zeit stattfinden muss.

Nach Abschluss des Boot-Vorgangs müssen sämtliche Fehlerzustände mit einer
„max. Feststellungszeit“ von „1 day“ erfasst worden sein. **[\<=]**

##### TIP1-A_4597

Der Konnektor MUSS zur Unterstützung von Missbrauchserkennungen für alle
Operationen, die in EVT_MONITOR_OPERATIONS gelistet sind und deren Alarmwert \>
0 ist, kontinuierlich folgende Aktivitäten durchlaufen:

 ---> OL

**[\<=]**

Erklärung „Minütlich gleitende 10-Minuten-Summe“: Für die jeweilige
Operation wird die Summe aller OK_Val und NOK_Val der letzten 10 Minuten
gebildet. Diese Summe wird jede Minute neu berechnet.

##### TIP1-A_4512-04

Der Konnektor MUSS per Ereignisdienst TUC_KON_256 über Änderungen des
Betriebszustandes (Tabelle TAB_KON_503 Betriebszustand_Fehlerzustandsliste)
informieren.Der Konnektor muss dazu für jeden Fehlerzustand $EC mit Error
Condition $EC.errorcondition mit verändertem Wert $EC.value den technischen
Anwendungsfall TUC_KON_256 „Systemereignis absetzen“ mit folgenden
Parametern aufrufen:TUC_KON_256 {        topic =
"OPERATIONAL_STATE/$EC.errorcondition";    eventType =
$EC.type;    severity = $EC.severity;    parameters =
(„Value=$EC.value, $EC.parameterlist”)}

Tabelle5: TAB_KON_503 Betriebszustand_Fehlerzustandsliste

 ---> TABLE

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

Unter „kartenbasiert“ sind nicht nur Lösungen mit Smartcards sondern auch
solche mit HSMs (Hardware Security Modules) zu verstehen.

##### A_17085

Wenn MGM_LU_ONLINE=Enabled nicht erfüllt ist, DARF der Konnektor den
Zustand EC_No_VPN_TI_Connection NICHT annehmen. **[\<=]**

##### A_17086

Wenn MGM_LU_ONLINE=Enabled oder ANLW_INTERNET_MODUS=SIS nicht erfüllt ist, DARF
der Konnektor den Zustand EC_No_VPN_SIS_Connection NICHT annehmen. **[\<=]**

##### A_17087

Wenn MGM_LU_ONLINE=Enabled nicht erfüllt ist, DARF der Konnektor den
Zustand EC_No_Online_Connection NICHT annehmen. **[\<=]**

##### A_22970

Der Konnektor MUSS 180 Tage vor Ablauf des aktuell verwendeten
C.NK.VPN-Zertifikats in den Zustand EC_NK_Certificate_Expiring wechseln.
**[\<=]**

##### A_22971

Der Konnektor MUSS mit dem Ablauf des aktuell verwendeten C.NK.VPN-Zertifikats
in den Zustand EC_NK_Certificate_Expired wechseln. **[\<=]**

 ---> TABLE

In den kritischen Fehlerzuständen, in denen keine TLS-Verbindung ins LAN
aufgebaut werden (EC_Random_Generator_Not_Reliable,
EC_Software_Integrity_Check_Failed, EC_Security_Log_Not_Writable,
EC_Time_Sync_Pending_Critical, EC_Time_Difference_Intolerable,
EC_NK_Certificate_Expired), kann keine Verbindung zu den Kartenterminals
aufgebaut werden. Infolge sind hier keine Kartenoperationen zugelassen.

Wenn keine Verbindung zum VPN-Konzentrator des SIS aufgebaut werden kann, ist
dadurch das Internet nicht über den Konnektor erreichbar. Wenn keine
Verbindung zum VPN-Konzentrator der TI aufgebaut werden kann, sind
Bestandsnetze nicht erreichbar.

Bezüglich der Administration des Konnektors im Zustand EC_FIREWALL_NOT_RELIABLE
ist eine Abstimmung mit der Prüfstelle und der Zertifizierungsstelle notwendig.

##### A_16203

Im Zustand EC_Firewall_Not_Reliable DARF der Konnektor NICHT nutzbar sein.
Möglichkeiten zur Behebung des Zustandes EC_Firewall_Not_Reliable sind mit dem
CC - Evaluierer und Zertifizierer abzustimmen. **[\<=]**

Die Architektur der TI ist so angelegt, dass die Fehlerzustände mit
Severity=Fatal in den Tabellen TAB_KON_504 und TAB_KON_503 mit
vernachlässigbarer Wahrscheinlichkeit von externen Einflüssen abhängen. Die
SLAs für Dienste der zentralen TI-Plattform sind so gefasst, dass diese
schwerwiegend verletzt werden müssten, um dadurch einen Konnektor in einen
solchen kritischen Zustand zu bringen (externer Fehler aus Sicht des
Konnektors). Dass beispielsweise der TSL-Dienst über den Zeitraum der
Grace-Period-TSL (typisch: 7 Tage) nicht erreichbar ist (ErrorCondition
EC_TSL_Out_Of_Date _Beyond_Grace_Period), kann nur bei massiver Verletzung der
für zentrale Dienste festgelegten SLAs eintreten.

Um die konnektorinternen Fehlerquellen zu erfassen, die dazu führen, dass ein
Fehlerzustand mit Severity=Fatal eintritt oder ein anderer Zustand, in dem der
Konnektor nicht verwendbar ist, wird Folgendes gefordert:

##### TIP1-A_5148

Der Konnektorhersteller MUSS den mittleren Zeitabstand zwischen Ausfällen
(MTBF) als Produkteigenschaft ausweisen. Der Konnektor soll einen mittleren
Zeitabstand zwischen Ausfällen (MTBF) von mindestens 50 Jahren haben.

Ein „Ausfall“gilt dann als eingetreten, wenn

 ---> UL

**[\<=]**

Bei einem mittleren Zeitabstand zwischen Ausfällen (MTBF) von 50 Jahren ist die
Wahrscheinlichkeit, dass ein Fehlerzustand mit Severity=Fatal auftritt, kleiner
2 % pro Jahr.

##### TIP1-A_4510-04

Der Konnektor MUSS bei eingetretenem Fehlerzustand aus Tabelle Tab_ Kon_503
Betriebszustand_Fehlerzustandsliste mit Severity=Fatal dafür sorgen, dass von
den Operationen der Basisdienste und Technische Use Cases (TUCs) der
Basisdienste, die relevant für Fachanwendungen sind, nur erlaubte Operationen
und TUCs gestartet und ausgeführt werden.Welche Operationen und TUCs je
eingetretenem Fehlerzustand ausgeführt werden dürfen, legt Tabelle
„TAB_KON_504 Ausführungserlaubnis für Dienste in kritischen
Fehlerzuständen“ fest: Jede Erlaubnis ist dort durch ein „x“
definiert.Abweichend zu Angaben in der Tabelle TAB_KON_504 DÜRFEN folgende
Operationen und TUCs NICHT im Zustand EC_Firewall_Not_Reliable ausgeführt
werden:

 ---> UL

Sind mehrere Fehlerzustände gleichzeitig eingetreten, dürfen nur die
Operationen und TUCs ausgeführt werden, die für alle eingetretenen
Fehlerzustände erlaubt sind. Der Konnektor MUSS Anfragen, die auf Grund eines
kritischen Fehlerzustandes nicht ausgeführt oder abgebrochen werden, mit einem
Fehler (Fehlercode 4002) beantworten.

Tabelle7: TAB_KON_502 Fehlercodes „Betriebszustand“

 ---> TABLE

**[\<=]**

### 3.4.1 Betriebsaspekte

Der Konnektor soll per Signaleinrichtung am Konnektor die Fehlerzustände mit
Severity „Error“ und „Fatal“ anzeigen (siehe [TIP1-A_4843]).

##### TIP1-A_4513

Der Konnektor MUSS es dem Administrator ermöglichen, den aktuellen
Betriebszustand einzusehen und Fehlerzustände zurückzusetzen, soweit diese
Möglichkeit in Tabelle „TAB_KON_503 Betriebszustand_Fehlerzustandsliste“
für den jeweiligen Fehlerzustand festgelegt ist.

Ferner MUSS es die Managementschnittstelle dem Administrator ermöglichen,
Konfigurationsänderungen gemäß Tabelle TAB_KON_505 vorzunehmen:

Tabelle8:TAB_KON_505 Konfigurationswerte Missbrauchserkennung

 ---> TABLE

**[\<=]**

### 3.5 Fachliche Anbindung der Clientsysteme

Für die Schnittstellen des Konnektors zu den Clientsystemen kann gesteuert
werden:

 ---> UL

Dabei werden die folgenden zwei Nutzungsszenariennichtunterschieden:

 ---> UL

Sowohl die Anbindung zur Administration des Konnektors, als auch die Anbindung
zur Nutzung von Bestandsnetzen oder dem gesicherten Internetzugang sind nicht
Gegenstand dieser Schnittstellenfestlegungen. Für die Anbindung zu
Administration wird diese im Kapitel Konnektormanagement beschrieben, für die
Anbindung von Bestandsnetzen bzw. dem gesicherten Internetzugang ist diese Art
der Regelung nicht erforderlich, da es sich dort um Routing-Funktionen handelt.

Die seitens des Administrators einstellbaren Werte und Listen sind, der
allgemeinen Struktur dieses Dokuments folgend, im Unterkapitel 3.4.1
Betriebsaspekte beschrieben.

##### TIP1-A_4514

Der Konnektor MUSS TLS in Richtung der Clientsysteme für alle
Außenschnittstellen der Basisdienste:

 ---> UL

unterstützen.

Ferner MUSS der Konnektor für die SOAP-Endpunkte der Fachmodule TLS
unterstützen.

Der Konnektor MUSS sich mittels ID.AK.AUT gegenüber dem Client authentisieren. **[\<=]**

##### TIP1-A_4515

Der Konnektor MUSS immer TLS-Verbindungsanfragen von Clientsystemen annehmen.

Der Konnektor MUSS bei gesetzter Variable ANCL_TLS_MANDATORY = Enabled den
Verbindungsversuch von Clientsystemen ohne TLS ablehnen. Ausgenommen hiervon
sind Anfragen an den Dienstverzeichnisdienst bei gesetzter Variable
ANCL_DVD_OPEN = Enabled. **[\<=]**

##### TIP1-A_4516

Der Konnektor MUSS zur Client-Authentifizierung die Verfahren Basic
Authentication (Username/Password) [RFC2617] über HTTP/TLS [RFC2818] und
zertifikatsbasierte Client-Authentifizierung (X.509) [gemSpec_PKI#8.3.1.4]
über TLS anbieten.Dabei MUSS für eine erfolgreiche Prüfung bei Basic
Authentication:

 ---> UL

Für eine erfolgreiche Prüfung mit zertifikatsbasierter
Client-Authentifizierung MUSS:

 ---> UL

Schlägt die Prüfung fehl, MUSS der Verbindungsversuch des Clientsystem
abgelehnt werden. **[\<=]**

Bei der Authentisierung des Clientsystems geht es um eine Authentisierung in
zwei Richtungen:

 ---> OL

Für beide Richtungen kann das Clientsystem dasselbe Zertifikat verwenden.

##### TIP1-A_5009

Der Konnektor MUSS für Verbindungen zu Clientsystemen als
Authentifizierungsmethode ausschließlich folgende Varianten erlauben:

 ---> OL

 ---> OL

Alle anderen Verbindungsversuche von Clientsystemen MÜSSEN vom Konnektor
abgelehnt werden. **[\<=]**

Für die Anbindung der Clientsysteme ergeben sich verschiedene
Konfigurationsvarianten bezüglich der Absicherung der Verbindungen zwischen
Konnektor und Clientsystemen. Tabelle TAB_KON_852 listet die Varianten für die
Verbindungen zum Aufruf der WebService-Schnittstellen (Varianten SOAP1 bis
SOAP4), für die Verbindungen zum Senden von Events (Varianten CETP1 und CETP2)
und für Verbindungen zum Abruf des Dienstverzeichnisses (Varianten DVD1, DVD2
und DVD3).

 ---> TABLE

Client-Authentisierung bei Nutzung des LDAP-Proxy

Für die Nutzung des LDAP-Proxy gelten abweichende Festlegungen, da viele
Standard LDAP- / Mail-Clients grundsätzlich keine Funktion zur
Client-Authentisierung anbieten. Um die Nutzung des LDAP-Proxy und somit des
VZD der TI dennoch zu ermöglichen, ohne dabei auf eine verpflichtende
Client-Authentisierung für SOAP-Aufrufe zu verzichten, werden für LDAP
gesonderte Regelungen getroffen.

##### A_21224-01

Bei der Verwendung  des LDAP-Proxies im Konnektor, MUSS sich
der Konnektor abhängig von der Stellung der Schalter ANCL_TLS_MANDATORY,
ANCL_CAUT_MANDATORY, ANCL_CAUT_MODE und ANCL_CAUT_LDAP gemäß der Tabelle
TAB_KON_860 verhalten.

Tabelle10: TAB_KON_865-01 Konfigurationsvarianten der Verbindungen zwischen
Konnektor und Clientsystemen bei LDAP

 ---> TABLE

**[\<=]**

Aus A_21224 resultiert direkt, dass als Client-Authentisierung für LDAPS nur
Client-Zertifikate unterstützt werden müssen.Die Authentisierung mit
Username/Passwort wird bei LDAPS nicht unterstützt.

Es sei noch einmal betont, dass TIP1-A_5009 sich nur auf SOAP und CETP
beziehtund TIP1-A_4516 das Basic-Authentication Verfahren nur für HTTP fordert.

### 3.5.1 Betriebsaspekte

Damit sich ein Clientsystem mittels X.509 authentisieren kann, muss es über ein
entsprechendes Zertifikat verfügen. Diese Zertifikate kann der Administrator
entweder mit seinen lokalen Mitteln selbst oder mittels des Konnektors
erzeugen. In beiden Fällen müssen diese Zertifikate sowohl im Clientsystemen
(hier zusammen mit ihren privaten Schlüsseln), als auch im Konnektor vorhanden
sein.

Da es sich um eine lokal begrenzte Authentisierung im Verantwortungsbereich des
Betreibers des lokalen Netzes handelt, werden keine weiteren Vorgaben zu den
Schlüsselspeichern auf Clientsystemseite erhoben. Auch hinsichtlich der
außerhalb des Konnektors erzeugten Zertifikate gelten keine weiteren Vorgaben.
Ferner ist eine Online-Prüfung dieser Zertifikate nicht erforderlich.

##### TIP1-A_4517

Der Konnektor MUSS die Erstellung und den Export von X.509-Zertifikaten für
Clientsysteme und der zugehörigen privaten Schlüssel durch den Administrator
über das Managementinterface ermöglichen. Hierbei MUSS der Konnektor dem
Administrator die Möglichkeit geben, das kryptographische Verfahren RSA-2048
oder ECC-256 auszuwählen. Als Exportformat MUSS PKCS#12 verwendet werden. Die
so erstellten Zertifikate werden zu ANCL_CCERT_LIST angefügt. Der Konnektor
MUSS dem Administrator ferner den Import von konnektorfremden
X.509-Zertifikaten für Clientsysteme über das Managementinterface
ermöglichen. Die so importierten Zertifikate werden zu ANCL_CCERT_LIST
angefügt. **[\<=]**

##### TIP1-A_4518-02

Der Administrator MUSS in der Managementoberfläche die in TAB_KON_506 genannten
Parameter im Managementinterface konfigurieren können.Wird ANCL_TLS_MANDATORY
auf ENABLED gewechselt, MÜSSEN alle nicht per TLS gesicherten
http-Verbindungen geschlossen werden, sobald die in den Verbindungen jeweils
aktuell laufenden Außenschnittstelle-Operationen abgeschlossen wurden, mit
Ausnahme von http-Verbindungen zum Dienstverzeichnisdienst.Der Konnektor MUSS
den Administrator geeignet und verständlich auf seine Verantwortung für die
Sicherung der Kommunikation hinweisen.

Tabelle11: TAB_KON_506-01 Konfigurationsparameter der
Clientsystem-Authentisierung

 ---> TABLE

**[\<=]**

Damit sich der Konnektor mittels X.509 gegenüber Clientsystemen authentisieren
kann, muss er über ein entsprechendes Zertifikat und dazu passendes
Schlüsselmaterial verfügen. Dieses Zertifikat und Schlüsselmaterial befinden
sich auf der gSMC-K (ID.AK.AUT). Der Administrator hat neben der Konfiguration
zur Nutzung des erneuerten C.AK.AUT , welches vom Konnektor heruntergeladen
wurde, auch mehrere Möglichkeiten, die ID.AK.AUT von der gSMC-K für die
Authentisierung gegenüber den Clientsystemen zu ersetzen:

 ---> UL

Da es sich um eine lokal begrenzte Authentisierung im Verantwortungsbereich des
Betreibers des lokalen Netzes handelt, werden keine weiteren Vorgaben zur
Erstellung und Handhabung in der LE-Umgebung der außerhalb des Konnektors
erzeugten Zertifikate und Schlüssel erhoben. Eine Online-Status-Prüfung
dieser Zertifikate ist nicht erforderlich und nicht vorgesehen.

##### A_21811-01

Der Konnektor MUSS bezüglich selbst generierter und importierter Schlüssel und
Zertifikate für die TLS-Authentisierung gegenüber Primärsystemen die
kryptographischen Vorgaben aus gemSpec_Krypt durchsetzen und bezüglich ECC
sowohl Brainpool- als auch NIST-Kurven unterstützen. **[\<=]**

##### A_21697

Der Konnektor MUSS dem Administrator den Import eines extern generierten
Schlüsselpaars und des dazugehörigen X.509-Zertifikats für die
Authentisierung des Konnektors im Rahmen von TLS-Verbindungen gegenüber
Clientsystemen über das Managementinterface ermöglichen. **[\<=]**

##### A_21698

Der Konnektor MUSS dem Administrator das Einschalten der Verwendung von
importiertem Schlüsselpaar und dazugehörigem X.509-Zertifikat für die
Authentisierung des Konnektors gegenüber Clientsystemen über das
Managementinterface ermöglichen. **[\<=]**

##### A_21699-01

Der Konnektor MUSS die Erstellung eines Schlüsselpaars und eines dazugehörigen
X.509-Zertifikats für die Authentisierung des Konnektors im Rahmen von
TLS-Verbindungen gegenüber den Clientsystemen durch den Administrator über
das Managementinterface ermöglichen. Hierbei MUSS der Konnektor dem
Administrator die Möglichkeit geben, das kryptographische Verfahren
RSA-2048, RSA-3072oder ECC-256 auszuwählen. Ferner MUSS der Konnektor dem
Administrator die Möglichkeit geben, den Hostnamen des Konnektors im
Zertifikat zu vergeben. **[\<=]**

##### A_21701

Der Konnektor MUSS dem Administrator den Export von intern generierten
X.509-Zertifikaten, die für die Authentisierung des Konnektors im Rahmen von
TLS-Verbindungen gegenüber den Clientsystemen verwendet werden,  über das
Managementinterface ermöglichen. Der private Schlüssel verbleibt im
Konnektor. **[\<=]**

##### A_21702

Der Konnektor MUSS dem Administrator das Einschalten der Verwendung von intern
generierten Schlüsseln und X.509-Zertifikaten für die Authentisierung des
Konnektors gegenüber den Clientsystemen über das Managementinterface
ermöglichen. **[\<=]**

##### A_21760-01

Der Konnektor MUSS dem Administrator das Einschalten der Verwendung von
ID.AK.AUTauf der gSMC-K für die Authentisierung des Konnektors gegenüber den
Clientsystemen über das Managementinterface ermöglichen.Der Konnektor MUSS
dabei zur Auswahl das RSA-Zertifikat C.AK.AUT.R2048 und (falls personalisiert)
das ECC-Zertifikat C.AK.AUT2.XXXX anbieten. Das ausgewählte Zertifikat MUSS
sowohl für die Serveridentität an der SOAP-Schnittstelle als auch für die
Clientidentität an der CETP-Schnittstelle verwendet werden. **[\<=]**

##### A_22894

DerHersteller des Konnektors MUSS im Administratorhandbuch erläutern, welche
Abhängigkeiten die unterschiedlichen Konfigurationen zur Authentifizierung
gegenüber den Clientsystemen zu beachten sind.  **[\<=]**

### 3.6 Clientsystemschnittstelle

##### TIP1-A_5401

Alle Schnittstellen, die der Konnektor den Clientsystemen zur Verfügung stellt,
MÜSSEN parallel durch mehrere Aufrufer nutzbar sein. **[\<=]**

### 3.6.1 SOAP-Schnittstelle

Für die Beschreibung der SOAP-Schnittstelle zum Clientsystem wird in dieser
Spezifikation WSDL Version 1.1 [WSDL1.1] eingesetzt. Die Interoperabilität
zwischen verschiedenen SOAP-Implementierungen wird durch die Vorgaben des WS-I
Basic Profile erreicht.

##### A_15601

Der Konnektor MUSS für die an der Clientsystemschnittstelle definierten
Web-Services der Basisdienste [SOAP1.1] verwenden. **[\<=]**

##### TIP1-A_4519

Der Konnektor MUSS die für die Clientsystemschnittstelle definierten
Web-Services konform zu [BasicProfile1.2] anbieten.

Abweichend von R1012 in [BasicProfile1.2] MUSS der Konnektor nur das Character
Encoding UTF-8 unterstützen. Andere Kodierungen MUSS der Konnektor mit einem
Fehler beantworten. **[\<=]**

##### TIP1-A_4519-01

Der Konnektor MUSS die für die Clientsystemschnittstelle definierten
Web-Services der Basisdienste konform zu [BasicProfile1.2] anbieten. **[\<=]**

##### A_15606

Abweichend von R1012 in [BasicProfile1.2] und [BasicProfile2.0] MUSS der
Konnektor nur das Character Encoding UTF-8 unterstützen. Andere Kodierungen
MUSS der Konnektor mit einem Fehler beantworten. **[\<=]**

Da der Konnektor UTF-16 nicht unterstützt, muss das Clientsystem den Request in
UTF-8 kodieren. Diese Festlegungen gelten nur für die eigentliche
SOAP-Nachricht. Sind in der SOAP-Nachricht base64-encodierte XML-Elemente
vorhanden, so können diese XML-Elemente andere Zeichencodierungen aufweisen.

Fachmodule

Fachmodule können für Web-Services, die Clientsystemen bereitgestellt werden,
entweder [SOAP1.1] mit [BasicProfile1.2] oder [SOAP1.2] mit [BasicProfile2.0]
verwenden. Die genaue Ausprägung erfolgt in der jeweiligen
Interfacebeschreibung des Web-Services für das Fachmodul.

##### A_15607

Der Konnektor MUSS für die an der Clientsystemschnittstelle definierten
Web-Services der Fachmodule [SOAP1.1] und [SOAP1.2] unterstützen. Die
SOAP-Version pro Web-Service Endpunkt wird durch die WSDL des jeweiligen
Web-Service definiert. **[\<=]**

##### A_15608

Der Konnektor MUSS für die an der Clientsystemschnittstelle definierten
Web-Services der Fachmodule bei [SOAP1.1] die Profilierung konform zu
[BasicProfile1.2] anbieten. **[\<=]**

##### A_15609

Der Konnektor MUSS für die an der Clientsystemschnittstelle definierten
Web-Services der Fachmodule bei [SOAP1.2] die Profilierung konform zu
[BasicProfile2.0]  anbieten. **[\<=]**

### 3.6.2 Statusrückmeldung und Fehlerbehandlung

Der Konnektor bietet Operationen an der Außenschnittstelle über
SOAP-Webservices an. Treten bei der Ausführung einer Operation Fehler auf, so
werden diese an das aufrufende System gemeldet. Die von den Basisdiensten des
Konnektors angebotenen SOAP-Webservices melden Fehler, die bei der Ausführung
einer Operation auftreten, über eine SOAP-Fault-Nachricht (siehe auch
[gemSpec_OM#3.2.3]).

##### TIP1-A_5058

Der Konnektor MUSS Fehlermeldungen, die im Rahmen einer über die
Außenschnittstelle aufgerufenen Operation auftreten, an das Clientsystem
mittels gematik-SOAP-Faults melden. **[\<=]**

##### TIP1-A_5058-01

Der Konnektor MUSS Fehlermeldungen, die im Rahmen einer über die
Außenschnittstelle aufgerufenen Operation eines Basisdienst-SOAP-Webservices
auftreten, an das Clientsystem mittels gematik-SOAP-Faults melden. **[\<=]**

Treten bei konnektorinternen Operationen (TUCs) Fehler auf, so werden diese an
den Aufrufer (aufrufender TUC oder aufrufende Operation) zurückgegeben. Der
Aufrufer kann den aufgetretenen Fehler in seinem Kontext neu interpretieren.
Das bedeutet insbesondere, dass ein Error eines aufgerufenen TUCs nicht
zwingend zum Abbruch des aufrufenden TUCs bzw. der aufrufenden Operation
führen muss. So ist es dem Aufrufer möglich, einen Error als Warnung zu
interpretieren und an den eigenen internen oder externen Aufrufer
zurückzumelden. Diese dabei erzeugte Fehlerkette wird in Form einer
Fehler-Trace-Struktur abgebildet, um eine Nachverfolgung von Fehlern zu
ermöglichen.

Operationen an der Außenschnittstelle können die Fehlerkette zu
Informationszwecken in der SOAP-Antwort an das Clientsystem senden. Dazu
enthält jede SOAP-Antwort das Element Status, dass gemäß dem XML-Schema
[ConnectorCommon.xsd] aufgebaut ist (siehe auch Abbildung PIC_KON_107
XML-Struktur des Status-Elements einer SOAP-Antwort).

![Abbildung-3][Abbildung-3]

Schlägt eine Operation fehl, so wird eine SOAP-Fault-Meldung an das
Clientsystem versendet. Im Erfolgsfall wird das Status-Element in die
Antwortnachricht an das Clientsystem aufgenommen. Ist der Fehler-Trace leer
(Element GERROR:Error ist nicht vorhanden), so wird CONN:Result auf OK gesetzt.
Andernfalls, d. h. wenn in GERROR:Trace Fehler der Schwere Info oder Warning
(zu Informationszwecken) enthalten sind, wird CONN:Result auf Warning gesetzt.

##### TIP1-A_4521

Der Konnektor MUSS Fehler protokollieren, die in fachlichen und technischen
Abläufen von der gematik spezifiziert oder herstellerspezifisch definiert
sind und den Schweregrad (Severity) Warning, Error oder Fatal haben. Zur
Nachvollziehbarkeit des Fehlers MÜSSEN Fehlerursache, fachliche und technische
Auslöser des Fehlverhaltens aus den Protokolleinträgen erkennbar sein. 
**[\<=]**

##### A_14159

Der Konnektor MUSS bei der Rückgabe von Fehlermeldungen an der
Außenschnittstelle sicherstellen, dass im letzten“ GERROR:Trace“-Element
der GERROR-Struktur ein von der gematik spezifizierter Fehler steht. Die
GERROR-Struktur kann weitere gematik- und herstellerspezifische Fehler
enthalten. **[\<=]**

In der Regel ist es ausreichend, wenn die GERROR-Struktur an der
Außenschnittstelle nur ein Element „GERROR:Trace“ mit einem gematik-Fehler
enthält.

Wenn für eine Fehlersituation kein Fehlercode spezifiziert ist, kann ein
herstellerspezifischer Fehler zur Detaillierung verwendet werden. In diesem
Fall muss ein passender gematik-Fehler als letztes GERROR:Trace-Element
gewählt werden.  Bei Fehlern in technischen Abläufen kann Fehlercode 4001
als letztes GERROR:Trace-Element verwendet werden. Die Wahl des letzten
GERROR:Trace-Elements ist mit der gematik abzustimmen.

Zur Struktur von Fehlermeldungen siehe auch [gemSpec_OM#GS-A_3856-*].

### 3.6.3 Transport großer Dokumente

SOAP Message Transmission Optimization Mechanism (MTOM) ermöglicht den direkten
Transport von binären Daten in Webservices, d.h. ohne dass eine zur Laufzeit
aufwändige Verpackung der binären Daten in ein Base64-XML-Element notwendig
wird. Auf die Definition der Webservices und ihre Funktionalität hat dieser
Optimierungsmechanismus keinen Einfluss. Der Einsatz von MTOM dient der
Verbesserung des Performance-Verhaltens für große Dokumente.

Das Clientsystem kann die Optimierung des Transports großer Dokumente per SOAP
Message Transmission Optimization Mechanism (MTOM) anstoßen. In den
WSDL-Dateien werden keine MTOM Serialization Policy Assertion [WS-MTOMPolicy]
eingebettet.

##### TIP1-A_5694

Der Konnektor KANN SOAP Message Transmission Optimization Mechanism (MTOM)
gemäß [MTOM] unterstützen.

Wenn der Konnektor MTOM unterstützt, MUSS er MTOM für Signatur- und
Verschlüsselungsdienst unterstützen, DARF aber NICHT MTOM für andere Dienste
unterstützen.

Wenn der Konnektor MTOM unterstützt, MUSS er, vergleichbar dem Einsatz des
Attributs wsp:Optional="true" einer MTOM Serialization Policy Assertion
[WS-MTOMPolicy], genau dann MTOM für die Antwortnachricht verwenden, wenn
entweder

 ---> UL

**[\<=]**

##### TIP1-A_5694-02

Der Konnektor KANN SOAP Message Transmission Optimization Mechanism (MTOM)
gemäß [MTOM-SOAP1.1] für Basisdienste unterstützen. **[\<=]**

##### TIP1-A_5694-03

Der Konnektor MUSS SOAP Message Transmission Optimization Mechanism (MTOM)
gemäß [MTOM-SOAP1.1] für Basisdienste unterstützen. **[\<=]**

##### A_15786

Wenn der Konnektor MTOM für Basisdienste unterstützt, MUSS er MTOM für
Signatur- und Verschlüsselungsdienst unterstützen, DARF aber NICHT MTOM für
andere Dienste unterstützen. **[\<=]**

##### A_15610

Wenn der Konnektor MTOM unterstützt, MUSS er, vergleichbar dem Einsatz des
Attributs wsp:Optional="true" einer MTOM Serialization Policy Assertion
[WS-MTOMPolicy], genau dann MTOM für die Antwortnachricht verwenden, wenn
entweder

 ---> UL

**[\<=]**

##### A_15611

Der Konnektor MUSS SOAP Message Transmission Optimization Mechanism (MTOM)
gemäß [MTOM] für Fachmodule unterstützen, wenn es in der
Schnittstellenbeschreibung des Fachmodules explizit gefordert wird. **[\<=]**

### 3.7 Verwendung manuell importierter CA-Zertifikate

TI-fremde X.509-Zertifikate werden im Rahmen des Verschlüsselungsdienstes
verwendet. Um den Vertrauensraum für diese Zertifikate abzubilden, erlaubt der
Konnektor, X.509-CA-Zertifikate zu diesen TI-fremden X.509-Zertifikaten in eine
interne Liste (CERT_IMPORTED_CA_LIST) zu importieren.

Der Konnektor kann dann im Rahmen der Hybridverschlüsselung den symmetrischen
Schlüssel empfängerspezifisch mit dessem TI-fremden X.509-Zertifikat
verschlüsseln. Die TI-fremden Zertifikate dürfen nicht zu einem anderen Zweck
als diesem eingesetzt werden.

##### TIP1-A_5433

Der Konnektor DARF End-Entity-Zertifikate, die lediglich gegen manuell
importierte X.509-CA-Zertifikate geprüft werden, die von CAs außerhalb der TI
stammen (CERT_IMPORTED_CA_LIST), NICHT für andere Zwecke als zur hybriden
Verschlüsselung von Dokumenten verwenden. **[\<=]**

Die Berücksichtigung der CA-Zertifikate aus CERT_IMPORTED_CA_LIST muss auf
folgende Anwendungsfälle beschränkt werden:

1. Prüfung eines Zertifikates im Rahmen der hybriden Verschlüsselung

2. Prüfung eines Zertifikates im Rahmen eines Aufrufes der Operation
"VerifyCertificate"

##### TIP1-A_5660

Das Handbuch des Konnektors MUSS sinngemäß folgende Hinweise enthalten:

 ---> UL

**[\<=]**

### 3.8 Testunterstützung

Gemäß Testkonzept der TI [gemKPT_Test#TIP1-A_6526] muss ein Hersteller eines
Konnektors seine Modelle in verschiedenen Ausführungen vorsehen: für
Testumgebung, für die Referenzumgebung und für die Produktivumgebung.Damit
trotz dieser Forderung die Firmware je Konnektorversion für alle Umgebungen
identisch ist, wird die Erkennung der Umgebung an die gSMC-K gebunden. Die
Konnektor-Firmware muss zwischen den Umgebungen PU und RU/TU unterscheiden. Die
gSMC-K besitzt hierzu den Datencontainer MF/EF.EnvironmentSettings, der die
jeweilige Umgebungskennung enthält (PU bzw. TU/RU). Die Umgebungskennung wird
read-only auf der gSMC-K gespeichert.

##### TIP1-A_4981

Der Produkttyp Konnektor MUSS sowohl in der Testumgebung (TU), der
Referenzumgebung (RU) wie auch der Produktivumgebung (PU) betreibbar sein.Die
Information, ob eine Konnektorinstanz in der TU/RU oder PU betrieben wird, MUSS
der Konnektor dem File MF/EF.EnvironmentSettings der gSMC-K entnehmen.Abhängig
von der ermittelten Betriebsumgebung MÜSSEN die Konfigurationswerte gemäß
Tabelle TAB_KON_812 verwendet werden.

Tabelle12: TAB_KON_812 Umgebungsabhängige Konfigurationsparameter

 ---> TABLE

**[\<=]**

##### TIP1-A_4707

Der Produkttyp Konnektor MUSS auch in der Test- und Referenzumgebung betrieben
werden können. Dafür MUSS der Vertrauensanker des Konnektors für diese
Umgebung ausgetauscht werden können. Dies KANN durch Lieferung eines neuen
Konnektors oder durch Austausch der gSMC-K durch den Hersteller ermöglicht
werden. Der Hersteller MUSS sicherstellen, dass Konnektoren ausschließlich mit
den zu ihrer Einsatzumgebung gehörenden Vertrauensankern ausgestattet werden. **[\<=]**

##### TIP1-A_4982

Die Administrationsoberfläche MUSS, wenn der Konnektor in der Testumgebung (TU)
oder Referenzumgebung (RU) betrieben wird, die Umgebungsbezeichnung zu jeder
Zeit erkennbar in der Managementschnittstelle anzeigen.

Die Anzeige eines Betriebs in der Produktivumgebung DARF NICHT explizit
angezeigt werden. **[\<=]**

### 4 Funktionsmerkmale

Für die folgenden Inhalte bitte die Hinweise in Kapitel 1.5.3 „Erläuterungen
zur Spezifikation des Außenverhaltens„ sowie Kapitel 1.5.4 Erläuterungen
zur Dokumentenstruktur und „Dokumentenmechanismen“ beachten.

### 4.1 Anwendungskonnektor

### 4.1.1 Zugriffsberechtigungsdienst

Der Zugriffsberechtigungsdienst ist ein interner Dienst. Er ermöglicht es
Operationen eine Prüfung auf Zugriffsberechtigung für die von ihnen
benötigten Ressourcen durchzuführen. Die Prüfung erfolgt direkt nach Aufruf
einer Operation des Konnektors durch das Clientsystem und basiert auf den im
Clientaufruf enthaltenen Parametern.

Der Zugriffsberechtigungsdienst definiert über ein Informationsmodell die
erlaubten Zugriffsmöglichkeiten. Um dies zu erreichen, modelliert es Mandanten
und ordnet ihnen Clientsysteme sowie die vom Konnektor verwalteten externen
Ressourcen (Kartenterminal mit Slots, Arbeitsplatz mit SMC-Bs) zu. Diese durch
einen Administrator persistent zu modellierenden Entitäten und Beziehungen
beinhalten die erlaubten Zugriffswege vom Clientsystem über Arbeitsplatz zum
Kartenterminal und dessen Slots. Sie werden im Konnektor administrativ
konfiguriert.

Neben diesen persistenten Entitäten und Beziehungen bildet das Modell auch die
in den Slots temporär gesteckten Karten und die zugehörigen Kartensitzungen
als transiente Entitäten und Beziehungen ab.

Abbildung PIC_Kon_100 stellt das Informationsmodell dar. Die persistenten
Entitäten haben einen grünen Hintergrund, die transienten einen weißen.

Tabelle TAB_KON_507 beschreibt die Entitäten und legt ihren
Identitätsschlüssel fest. Tabelle TAB_KON_508 beschreibt die Attribute.
Tabelle TAB_KON_509 beschreibt die Entitätsbeziehungen und referenziert dabei
die in Abbildung PIC_Kon_100 durch Zahlen in eckigen Klammern markierten
Beziehungen. Tabelle TAB_KON_510 definiert Constraints, die zusätzlich zu den
in Abbildung PIC_Kon_100 definierten Kardinalitäten gelten. Die Constraints
werden mittels Object Constraint Language (OCL) definiert.

### 4.1.1.1 Funktionsmerkmalweite Aspekte

##### TIP1-A_4522

Der KonnektorMUSS die Entitäten, Attribute und Beziehungen des
Informationsmodells intern vorhalten, dabei für die Einhaltung der definierten
Constraints sorgen und die persistenten Entitäten und Beziehungen dauerhaft
speichern. Der Konnektor MUSS dabei eine Mindestanzahl von 999 Mandanten
unterstützen.

Das Informationsmodell ist definiert durch das UML-Diagramm „PIC_Kon_100
Informationsmodell des Konnektors„ und die Tabelle „TAB_KON_510
Informationsmodell Constraints“. Der Konnektor darf nur Daten in sein
Informationsmodell übernehmen, die alle Eigenschaften des Informationsmodells,
insbesondere die Constraints, erfüllen.

Die Entitäten werden in Tabelle „TAB_KON_507 Informationsmodell
Entitäten“beschrieben, die Attribute in Tabelle „TAB_KON_508
Informationsmodell Attribute“und die Beziehungen in Tabelle „TAB_KON_509
Informationsmodell Entitätenbeziehungen“. **[\<=]**

Hinweis zu den Bezeichnern der Entitäten und ihrer Attribute: Im Folgenden
beginnen Entitäten mit einem Großbuchstaben, Attribute mit einem
Kleinbuchstaben. Werden die Entitäten und Attribute in XML-Dokumenten
verwendet, so beginnen die zugeordneten XML-Elementbezeichner grundsätzlich
mit einem Großbuchstaben und verwenden den englischen Begriff, der im
Folgenden in Klammern angegeben ist, wenn zur besseren Lesbarkeit im Modell ein
deutscher Begriff verwendet wird.

![Abbildung-4][Abbildung-4]

 ---> TABLE

 ---> TABLE

 ---> TABLE

 ---> TABLE

Hinweis zur Remote-PIN-Eingabe: Constraints C14 und C15 legen fest, dass auch im
Fall mehrerer lokaler Kartenterminals an einem Arbeitsplatz nur eines (oder
keines) dieser Kartenterminals pro Mandant für die Remote-PIN-Eingabe im
Informationsmodell konfiguriert wird.

##### TIP1-A_4523

Der Konnektor MUSS seine Entscheidungen zur Zugriffsberechtigung basierend auf
den aktuellen, realen statischen wie transienten Entitäten und Beziehungen des
Informationsmodells treffen. Veränderungen an der statischen Definition (durch
den Administrator), sowie Veränderungen an den Entitäten (Änderung der
Verfügbarkeit und Zustandsänderung von Karten, Kartenterminals und
Clientsystemen) MÜSSEN bei Zugriffsanfragen unmittelbare Auswirkung auf die
Entscheidung des Zugriffsberechtigungsdienstes zur Folge haben. **[\<=]**

### 4.1.1.2 Durch Ereignisse ausgelöste Reaktionen

Keine.

### 4.1.1.3 Interne TUCs, nicht durch Fachmodule nutzbar

Keine.

### 4.1.1.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.1.1.4.1 TUC_KON_000 „Prüfe Zugriffsberechtigung“

Vor Ausführung jeder Operation an der Außenschnittstelle muss der Konnektor
prüfen, ob die Operation ausgeführt werden darf (Autorisierung). Diese
Prüfung auf Zugriffsberechtigung wird in TUC_KON_000 „Prüfe
Zugriffsberechtigung“ gekapselt.

TUC_KON_000 „Prüfe Zugriffsberechtigung“ hat als Aufrufparameter den
Aufrufkontext der Operation (siehe Abbildung PIC_KON_101), optional das
cardHandle einer Karte, optional eine Kartenterminal-ID ctId und optional die
Steuerungsparameter „needCardSession“ sowie „allWorkplaces“. Über den
Steuerungsparameter „needCardSession“ wird festgelegt, ob zu den
CardHandles im Rahmen der Operationsausführung eine Kartensitzung benötigt
wird. Über den Steuerungsparameter „allWorkplaces“. wird festgelegt, ob
die Auswertung im Rahmen der Operation arbeitsplatzübergreifend für alle vom
Mandanten für das angegebene Clientsystem erreichbaren Kartenterminals
erfolgen soll.

![Abbildung-5][Abbildung-5]

##### TIP1-A_4524-03

Der Konnektor MUSS den technischen Use Case TUC_KON_000 „Prüfe
Zugriffsberechtigung“ umsetzen.

Tabelle17: TAB_KON_511-01 – TUC_KON_000 „Prüfe Zugriffsberechtigung“

 ---> TABLE

**[\<=]**

Eine Beschreibung aller Zugriffsregeln gibt Tabelle TAB_KON_512.

 ---> TABLE

![Abbildung-6][Abbildung-6]

Welche Zugriffsregel für einen gegebenen Satz an Aufrufparametern anzuwenden
ist, wird in Tabelle TAB_KON_513 ermittelt. Die Pflichtfelder mandantId,
clientSystemId und workplaceId und das optionale Feld userId sind zwar für die
Auswertung der Regeln wichtig, tragen aber nicht zur Auswahl der Regel bei und
sind daher in der Tabelle nicht vorhanden. Zur Auswahl einer Regel ist relevant,

 ---> UL

 ---> TABLE

Tabelle TAB_KON_514 definiert einzelne Bedingungen, ordnet sie den Regeln zu und
definiert ErrorCodes für den Fall, dass eine Bedingung nicht erfüllt ist.

Die Bedingungen in Tabelle TAB_KON_514 sind wie folgt gruppiert:

 ---> UL

Die Fehlercodes mit Beschreibung, ErrorType und Severity Tabelle TAB_KON_515.

 ---> TABLE

Erläuterungen zu TAB_KON_514-01:

Hinweis 1:Jede Bedingung ist als Constraint mittels OCL definiert, ist einzeln
prüfbar und hat als Eingangsparameter mandantId, clientSystemId, workplaceId,
ctId, cardHandle und userId.

Hinweis 2:Zur Bezeichnung einer Objektinstanz, die im Informationsmodell
vorhanden ist, wird die Notation \<\<Entitätsbezeichner\>\>(\<\<Komma
separierte Liste der Identitätsschlüssel\>\> verwendet.

Hinweis 3:  
Bei manchen Bedingungen gibt es unterschiedliche Fehlermeldungen
für die Außenschnittstelle und für die interne Protokollierung. Dann wird
folgende Notation in Spalte "Error Code" verwendet:

"\<\<Fehlercode\>\> an der Außenschnittstelle" für den Fehlercode, der über
die Außenschnittstelle zurückgegeben werden muss

"\<\<Fehlercode\>\> im Protokoll" für den Fehlercode, der für die interne
Protokollierung verwendet werden muss. 

 ---> TABLE

Hinweis zu Fehler 4018: Sicherheitszustand wird bei PIN-Eingabe erhöht.

### 4.1.1.5 Operationen an der Außenschnittstelle

Keine

### 4.1.1.6 Betriebsaspekte

##### TIP1-A_4525

Der Konnektor MUSS mit Abschluss der Bootup-Phase den Ist-Zustand transienter
Entitäten und Beziehungen des Informationsmodells erfasst haben. **[\<=]**

##### TIP1-A_4526

Für die Administration MUSS der Konnektor eine Administrationsoberfläche zur
Pflege des Informationsmodells zur Verfügung stellen. Die Oberfläche muss es
ermöglichen, sämtliche persistente Entitäten undBeziehungen des durch
Abbildung„PIC_Kon_100 Informationsmodell des Konnektors“und Tabelle
„TAB_KON_510Informationsmodell Constraints“ definierten Informationsmodells
initial anzulegen, zu ändern und zu löschen. **[\<=]**

Im Anhang I „Umsetzungshinweise“ werden Empfehlungen zur Umsetzung der
Administration des Informationsmodells gegeben.

### 4.1.2 Dokumentvalidierungsdienst

Der Dokumentvalidierungsdienst ist ein Dienst, der nur intern genutzt wird,
d. h., dass dessen definierte Verhaltensweisen nur in anderen TUCs des
Konnektors nachgenutzt werden. Er bietet Schnittstellen zum Validieren von
Dokumenten an. Dabei werden diejenigen spezifischen Dokumentformate
unterstützt, die an den Außenschnittstellen anderer Dienste wie Signatur- und
Verschlüsselungsdienst auftreten können (Alle_DocFormategemäß Kapitel 3).

Die jeweils gültigen XML-Schemas der Fachmodule werden den Herstellern von der
gematik bereitgestellt.

### 4.1.2.1 Funktionsmerkmalweite Aspekte

##### A_18780

Der Konnektor DARF Dokumente im PDF/A-3 Format NICHT unterstützen. **[\<=]**

### 4.1.2.2 Durch Ereignisse ausgelöste Reaktionen

Keine.

### 4.1.2.3 Interne TUCs, nicht durch Fachmodule nutzbar

Keine

### 4.1.2.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.1.2.4.1 TUC_KON_080 „Dokument validieren”

##### TIP1-A_4527-04

Der Konnektor MUSS den technischen Use Case TUC_KON_080 „Dokument
validieren” umsetzen.

Tabelle22: TAB_KON_143 – TUC_KON_080 „Dokument validieren“

 ---> TABLE

Tabelle23: TAB_KON_144 Fehlercodes TUC_KON_080 „Dokument validieren“

 ---> TABLE

**[\<=]**

### 4.1.2.5 Operationen an der Außenschnittstelle

Keine

### 4.1.2.6 Betriebsaspekte

Keine

### 4.1.3 Dienstverzeichnisdienst

Der Dienstverzeichnisdienst liefert dem aufrufenden Clientsystem sowohl
Informationen über die Version und Produktkenndaten des Konnektors, als auch
die SOAP-Endpunkte, über die das Clientsystem die einzelnen Dienstoperationen
erreichen kann.

### 4.1.3.1 Funktionsmerkmalweite Aspekte

Die Endpunkte der Basisdienste werden in WSDL spezifiziert. Diese Endpunkte und
weitere konnektormodellspezifische Informationen werden dem Clientsystem in
Form eines Dienstverzeichnisdienstes gesammelt angeboten.

Der prinzipielle Ablauf sieht dabei folgendermaßen aus:

Das Clientsystem ruft beim Initialisieren des Systems mit HTTP-GET die
vordefinierte URL:     https://\<ANLW_LAN_IP_ADDRESS oder    
MGM_KONN_HOSTNAME\>/connector.sds oderhttp://\<ANLW_LAN_IP_ADDRESS oder
MGM_KONN_HOSTNAME\>/connector.sdsdes Konnektors auf.

Der Konnektor stellt die Liste der Dienste, der Versionen und die Endpunkte der
Dienste in einem XML-Dokument zusammen. Jeder über SOAP erreichbare
Basisdienst des Konnektors wird in dieser Liste geführt. Ferner können
Fachmodule ihre eigenen Endpunkte über TUC_KON_041 „Einbringen der
Endpunktinformationenwährend der Bootup-Phase“ einbringen. Die so erstellte
Liste der Dienste wird als Antwort an das Clientsystem übergeben.

Das Clientsystem prüft, ob die gewünschten Dienste und Versionen unterstützt
werden und merkt sich die Endpunkte der Dienste für die späteren Aufrufe.
Danach kann das Clientsystem diese Dienstendpunkte nach Bedarf aufrufen.

##### TIP1-A_4528

Der Konnektor MUSS den Dienstverzeichnisdienst anbieten. Dieser Dienst
veröffentlicht
auf:    https://$ANLW_LAN_IP_ADDRESS oder $MGM_KONN_HOSTNAME\>/connector.sds
oder    
http://$ANLW_LAN_IP_ADDRESS oder $MGM_KONN_HOSTNAME\>/connector.sds.

Die Datei MUSS über https erreichbar sein.

Wenn (ANCL_DVD_OPEN = Enabled) oder (ANCL_TLS_MANDATORY = Disabled) MUSS die
Datei auch über http erreichbar sein. **[\<=]**

##### TIP1-A_4529-02

Das XML-Dokument, welches als „connector.sds“ dem Aufrufer zurückgeliefert
wird, MUSS gemäß dem Schema „conn/ServiceDirectory.xsd“ formatiert
sein.conn/ServiceDirectory.xsdreferenziert die Schemata
„tel/version/ProductInformation.xsd“ (siehe [gemSpec_OM]) und
„conn/ServiceInformation.xsd“.TAB_KON_516, TAB_KON_517 und TAB_KON_518
beschreiben die Elemente der zu verwendenden Schemastruktur.

Tabelle24: TAB_KON_516 Basisanwendung Dienstverzeichnisdienst

 ---> TABLE

Tabelle25: TAB_KON_517 Schemabeschreibung Produktinformation
(ProductInformation.xsd)

![Img-007][Img-007]

 ---> TABLE

Tabelle26: TAB_KON_518 Schemabeschreibung Serviceinformation
(Serviceinformation.xsd)

 ---> TABLE

**[\<=]**

##### TIP1-A_4530

Die URLs der Dienste KÖNNEN herstellerspezifisch aufgebaut werden. **[\<=]**

### 4.1.3.2 Durch Ereignisse ausgelöste Reaktionen

Keine.

### 4.1.3.3 Interne TUCs, nicht durch Fachmodule nutzbar

Keine

### 4.1.3.4 Interne TUCs, auch durch Fachmodule nutzbar

Da der Konnektor als Black-Box mit inkludierten Fachmodulen ohne erkennbare
Innenschnittstellen spezifiziert wird, stellt der folgende TUC lediglich einen
Mechanismus zur editoriellen Kopplung der Fachmodulspezifikationen mit der
Konnektorspezifikation dar:

### 4.1.3.4.1 TUC_KON_041 „Einbringen der Endpunktinformationen während der Bootup-Phase“

##### TIP1-A_4531

Der Dienstverzeichnisdienst des Konnektors MUSS es den Fachmodulen ermöglichen,
die zum jeweiligen Fachmodul gehörenden Endpunkte während der Bootup-Phase
des Konnektors in den Dienstverzeichnisdienst einzubringen.

Tabelle27: TAB_KON_519 - TUC_KON_041 „Einbringen der Endpunktinformationen
während der Bootup-Phase“

 ---> TABLE

Tabelle28: TAB_KON_520 Fehlercodes TUC_KON_041 „Einbringen der
Endpunktinformationen während der Bootup-Phase“

 ---> TABLE

**[\<=]**

### 4.1.3.5 Operationen an der Außenschnittstelle

##### TIP1-A_4532

Der Dienstverzeichnisdienst des Konnektors MUSS die in Tabelle TAB_KON_521
Schnittstelle der Basisanwendung Dienstverzeichnisdienst beschriebene
Schnittstelle anbieten.

Tabelle29: TAB_KON_521 Schnittstelle der Basisanwendung Dienstverzeichnisdienst

 ---> TABLE

​​ **[\<=]**

### 4.1.3.6 Betriebsaspekte

##### TIP1-A_4533

Mit Abschluss der Bootup-Phase MUSS der Dienstverzeichnisdienst an der
Außenschnittstelle die vollständige Liste aller Services bereitstellen, die
der Anwendungskonnektor den Clientsystemen anbietet, inklusive der Services der
Fachmodule. **[\<=]**

### 4.1.4 Kartenterminaldienst

Die Aufgabe des Kartenterminaldienstes ist das Management aller vom Konnektor
adressierbaren Kartenterminals. Dies umfasst alle administrativen Prozesse
(insbesondere das Pairing, vgl. [gemSpec_KT#2.5.2]). Ferner kapselt der
Kartenterminaldienst die Zugriffe auf Kartenterminals durch Basisdienste und
Fachmodule.

Für die TLS-Verbindungen zu den Kartenterminals muss der Konnektor die Vorgaben
aus [gemSpec_Krypt#3.3.2] und hinsichtlich ECC-Migration die Vorgaben aus
[gemSpec_Krypt#5] befolgen.

Innerhalb des Kartenterminaldienstes werden folgende Präfixe für Bezeichner
verwendet:

 ---> UL

Der Kartenterminaldienst verwaltet hinsichtlich der Kartenterminals mindestens
die in der informativen Tabelle TAB_KON_522 Parameterübersicht des
Kartenterminaldienstes ausgewiesenen Parameter, weitere herstellerspezifische
Parameter sind möglich. Die normative Festlegung wann welche Parameter mit
welchen Werten belegt werden, erfolgt in den folgenden Abschnitten und
Unterkapiteln.

Dabei beschrieben CTM_xyz-Bezeichner Parameter, die den Dienst als Ganzes
betreffen. Zu jedem Kartenterminal selbst werden dessen Parameter in einem
CT-Object gekapselt. Die folgende Tabelle zeigt die Attribute der jeweiligen
CT-Objekte über Punktschreibweise.

 ---> TABLE

Zum besseren Verständnis sind die Zustände, die ein Kartenterminal einnehmen
kann, im nachfolgenden Zustandsdiagramm PIC_KON_071 dargestellt.

![Abbildung-7][Abbildung-7]

### 4.1.4.1 Funktionsmerkmalweite Aspekte

##### TIP1-A_4534

Der Kartenterminaldienst MUSS Kartenterminals nach der
eHealth-KartenterminalSpezifikation [gemSpec_KT] unterstützen. **[\<=]**

Zur Unterstützung von HSM-Bs benötigt der Konnektor virtuelle Kartenterminals
(CT.IS_PHYSICAL=Nein), in denen virtuelle SMC-Bs „stecken“ können (siehe
Kapitel 4.1.4). Diese Kartenterminals werden innerhalb des
Zugriffsberechtigungsdienstes sowie des Systeminformationsdienstes wie normale
Kartenterminals berücksichtigt. Weitere Details zu den logischen
Kartenterminals finden sich im Kapitel Betriebsaspekte.

##### TIP1-A_4535

DerKartenterminaldienst MUSS logische Kartenterminals mit logischen Slots
unterstützen. Zu jedem verwalteten HSM (siehe Kartendienst) MUSS der Konnektor
ein oder mehrere logische Kartenterminal mit folgenden Bedingungen vorhalten:

 ---> UL

**[\<=]**

##### TIP1-A_4536

Der Kartenterminaldienst MUSS jede mit einem Kartenterminal etablierte
Verbindung durch Nutzung des in [SICCT#6.1.4.5] definierten Keep-Alive
Mechanismus halten.Der Konnektor MUSS für das Heartbeat-Interval gemäß
[SICCT#6.1.4.5] den Wert CTM_KEEP_ALIVE_INTERVAL verwenden und beim Ausbleiben
von Terminal-Antworten eines Kartenterminals nach der Anzahl
von  CTM_KEEP_ALIVE_TRY_COUNT Versuchen die Netzwerkverbindung zu diesem
Kartenterminal beenden. **[\<=]**

##### TIP1-A_6725

Der Konnektor MUSS steuern, dass Textanzeigen am Kartenterminal nur so lange
angezeigt werden, wie sie im jeweiligen Anwendungskontext benötigt werden. **[\<=]**

Ziel der Textanzeigen am Kartenterminal ist die Kommunikation mit dem Benutzer
zur Unterstützung der Anwendungsfälle. Die Anzeige am Kartenterminal muss
daher einen engen zeitlichen Bezug zum jeweiligen Anwendungskontext haben.

Nachrichten, deren Anwendungskontext mit einem Event beendet werden, wie etwa
die Aufforderung zum Stecken der Karte im Kontext von TUC_KON_056, deren
inhaltliche Berechtigung mit dem Stecken der Karte erlischt, (ebenso zum Ziehen
der Karte im Rahmen von TUC_KON_057) müssen sofort gelöscht werden, wenn das
Event eintritt.  

Nachrichten, deren Lebensdauer nicht durch ein natürliches Event beendet wird,
müssen eine vordefinierte Lebensdauer erhalten, die per Konfiguration an die
Bedürfnisse der Leistungserbringer anpassbar sein sollte. Das gilt für
Ergebnisanzeigen oder Anzeigen von Fehlern.

##### TIP1-A_4537

Tritt ein Timeout ein oder wird eine Netzwerkverbindung zu einem
Kartenterminal(oder zu einem HSM, welches einem logischen Kartenterminal
zugeordnet ist) beendet oder zurückgesetzt und ist CT.CONNECTED = Ja, so MUSS
der Konnektor:

 ---> UL

**[\<=]**

##### TIP1-A_4538

Sind in CTM_CT_LIST Kartenterminals mit CT.CONNECTED=Nein und CT.VALID_VERSION =
True und CT.CORRELATION = „aktiv“ und istCTM_SERVICE_DISCOVERY_CYCLE\>0,
MUSS der Konnektor im ZeitabstandCTM_SERVICE_DISCOVERY_CYCLE-Minutenentweder
eine Service Discovery-Nachricht an alle KTs als Broadcast oderan jedes
einzelne dieser unverbundenen KTs als Unicast senden. **[\<=]**

##### TIP1-A_4538-02

Sind in CTM_CT_LIST Kartenterminals mit CT.CONNECTED=Nein und CT.VALID_VERSION =
True und CT.CORRELATION = „aktiv“ und istCTM_SERVICE_DISCOVERY_CYCLE\>0,
MUSS der Konnektor im ZeitabstandCTM_SERVICE_DISCOVERY_CYCLE-Minuten an jedes
einzelne dieser unverbundenen KTs eine Service-Discovery-Nachricht als Unicast
senden. **[\<=]**

##### TIP1-A_6478

Der Kartenterminaldienst DARF SICCT-bzw. EHEALTH-Kommandos NICHT an ein
Kartenterminal senden, wenn für dieses Kartenterminal CT.CONNECTED=Nein
gesetzt ist. Ausgenommen hiervon sind die in TAB_KON_785 gelisteten EHEALTH-
bzw. SICCT-Kommandos. **[\<=]**

 ---> TABLE

##### TIP1-A_4539

Das Ziehen einer Karte während einer Kartenaktion DARF NICHT dazu führen, dass
das verwaltete Kartenterminal im Anschluss durch den Konnektor nicht weiter
genutzt werden kann.Die entsprechende Ressource MUSS nach Erkennung der
Fehlersituation freigegeben werden. Ein manuelles Eingreifen DARF NICHT
erforderlich sein. **[\<=]**

##### TIP1-A_5408

Der Konnektor MUSS beim Anfordern und Auswerfen von Karten die folgenden
Display-Nachrichten für die Anzeige im Kartenterminal verwenden, wenn der
Aufrufer keine konkrete Display-Nachricht übergeben hat. Der Verweis auf den
Kartenterminal-Slot SOLL in der Display-Nachricht entfallen, wenn es keine
Slot-Auswahl am Kartenterminal gibt.

Tabelle32: TAB_KON_727 Terminalanzeigen beim Anfordern und Auswerfen von Karten

 ---> TABLE

**[\<=]**

### 4.1.4.2 Durch Ereignisse ausgelöste Reaktionen

##### TIP1-A_4540

Der Konnektor MUSS Service Announcement für das Auffinden von Kartenterminals
entsprechend [SICCT] und [gemSpec_KT] unterstützen. Der Konnektor MUSS
Dienstbeschreibungspakete auf UDP
PortCTM_SERVICE_ANNOUNCEMENT_PORTentgegennehmen.

Erhält er ein solchesDienstbeschreibungspaket, MUSS er

 ---> UL

**[\<=]**

##### TIP1-A_4541

Der Kartenterminaldienst MUSS auf SICCT-Ereignisnachrichten „Slot-Ereignis –
Karte eingesteckt“ ([SICCT#6.1.4.4], TAG ‚84’) wie folgt reagieren:

 ---> UL

**[\<=]**

##### TIP1-A_4542

Der Kartenterminaldienst MUSSauf SICCT-Ereignisnachrichten „Slot-Ereignis –
Karte entfernt“ ([SICCT#6.1.4.4], TAG ‚85’) wie folgt reagieren:

 ---> UL

**[\<=]**

##### TIP1-A_4543

Tritt der Event"KSR/UPDATE/START"mit „Target=KT“ ein, MUSS der Konnektor:

 ---> UL

**[\<=]**

##### TIP1-A_4544

Tritt der Event "KSR/UPDATE/END"mit „Target=KT“ ein, MUSS der Konnektor:

 ---> UL

**[\<=]**

### 4.1.4.3 Interne TUCs, nicht durch Fachmodule nutzbar

### 4.1.4.3.1 TUC_KON_050 „Beginne Kartenterminalsitzung“

##### TIP1-A_4545-03

Der Konnektor MUSS den technischen Use Case „Beginne Kartenterminalsitzung”
gemäß TUC_KON_050 umsetzen.

Tabelle33: TAB_KON_039 – TUC_KON_050 „Beginne Kartenterminalsitzung“

 ---> TABLE

![Img-009][Img-009]

Abbildung8: PIC_KON_110 Aktivitätsdiagramm zu „Beginne
Kartenterminalsitzung“

Tabelle34: TAB_KON_523 Fehlercodes TUC_KON_050 „Beginne
Kartenterminalsitzung“

 ---> TABLE

**[\<=]**

### 4.1.4.3.2 TUC_KON_054 „Kartenterminal hinzufügen“

##### TIP1-A_4546

Der Konnektor MUSS den technischen Use Case TUC_KON_054 „Kartenterminal
hinzufügen“ umsetzen.

Tabelle35: TAB_KON_524 – TUC_KON_054 „Kartenterminal hinzufügen“

 ---> TABLE

Tabelle36: TAB_KON_525 Fehlercodes TUC_KON_054 „Kartenterminal hinzufügen“

 ---> TABLE

**[\<=]**

### 4.1.4.3.3 TUC_KON_053 „Paire Kartenterminal“

##### TIP1-A_4548-02

DerKonnektor MUSS den technischen Use Case „Paire Kartenterminal” gemäß
TUC_KON_053 umsetzen.

Tabelle37: TAB_KON_041 – TUC_KON_053 „Paire Kartenterminal“

 ---> TABLE

Tabelle38: TAB_KON_113 Fehlercodes TUC_KON_053 „Paire Kartenterminal“

 ---> TABLE

Hinweis zu Fehler 4041:

Nur wenn dieser Fehler wegen eines Fehlers auf der SICCT-Schnittstelle auftritt,
ist der SICCT-Fehlercode mit anzugeben.

![Abbildung-9][Abbildung-9]

Abbildung9: PIC_KON_057 Aktivitätsdiagramm zu „PaireKartenterminal“ **[\<=]**

### 4.1.4.3.4 TUC_KON_055 „Befülle CT-Object“

##### TIP1-A_4985

Der Konnektor MUSS den technischen Use Case TUC_KON_055 „Befülle CT-Object“
umsetzen.

Tabelle39: TAB_KON_526 – TUC_KON_055 „Befülle CT-Object“

 ---> TABLE

**[\<=]**

### 4.1.4.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.1.4.4.1 TUC_KON_051 „Mit Anwender über Kartenterminal interagieren“

##### TIP1-A_4547

Der Konnektor MUSS den technischen Use Case „Mit Anwender über Kartenterminal
interagieren” gemäß TUC_KON_051 umsetzen.

Tabelle40: TAB_KON_112 – TUC_KON_051 „Mit Anwender über Kartenterminal
interagieren“

 ---> TABLE

Tabelle41: TAB_KON_114 Fehlercodes TUC_KON_051 „Mit Anwender über
Kartenterminal interagieren“

 ---> TABLE

**[\<=]**

### 4.1.4.4.2 TUC_KON_056 „Karte anfordern“

##### TIP1-A_5409

Der Konnektor MUSS den technischen Use Case „Karte anfordern” gemäß
TUC_KON_056 umsetzen.

Tabelle42: TAB_KON_723 - TUC_KON_056 „Karte anfordern“

 ---> TABLE

Tabelle43: TAB_KON_724 Fehlercodes TUC_KON_056 „Karte anfordern“

 ---> TABLE

**[\<=]**

### 4.1.4.4.3 TUC_KON_057 „Karte auswerfen“

##### TIP1-A_5410

Der Konnektor MUSS den technischen Use Case „Karte auswerfen” gemäß
TUC_KON_057 umsetzen.

Tabelle44: TAB_KON_725 – TUC_KON_057 „Karte auswerfen“

 ---> TABLE

Tabelle45: TAB_KON_796 Fehlercodes TUC_KON_057 „Karte auswerfen“

 ---> TABLE

**[\<=]**

### 4.1.4.4.4 TUC_KON_058 „Displaygröße ermitteln“

##### A_17473

Der Konnektor MUSS den technischen Use Case „Displaygröße ermitteln“
gemäß TUC_KON_058 umsetzen.

Tabelle46: TAB_KON_854 – TUC_KON_058 „Displaygröße ermitteln“

 ---> TABLE

Tabelle47: TAB_KON_855 Fehlercodes TUC_KON_058 „Displaygröße ermitteln“

 ---> TABLE

**[\<=]**

### 4.1.4.5 Operationen an der Außenschnittstelle

##### TIP1-A_5411-02

Der Konnektor MUSS Clientsystemen den Basisdienst Kartenterminaldienst anbieten.

Tabelle48: TAB_KON_722 Basisdienst Kartenterminaldienst

 ---> TABLE

**[\<=]**

### 4.1.4.5.1 RequestCard

##### TIP1-A_5412

Der Konnektor MUSS an der Außenschnittstelle eine Operation RequestCard, wie in
Tabelle TAB_KON_716 Operation RequestCard beschrieben, anbieten.

Tabelle49: TAB_KON_716 Operation RequestCard

 ---> TABLE

Der Ablauf der Operation RequestCard ist in Tabelle TAB_KON_717 Ablauf
RequestCard beschrieben.

Tabelle50: TAB_KON_717 Ablauf RequestCard

 ---> TABLE

Tabelle51: TAB_KON_718 Fehlercodes „RequestCard“

 ---> TABLE

**[\<=]**

### 4.1.4.5.2 EjectCard

##### TIP1-A_5413

Der Konnektor MUSS an der Außenschnittstelle eine Operation EjectCard, wie in
Tabelle TAB_KON_719 Operation EjectCard beschrieben, anbieten.

Tabelle52: TAB_KON_719 Operation EjectCard

 ---> TABLE

Der Ablauf der Operation EjectCard ist in Tabelle TAB_KON_720 Ablauf EjectCard
beschrieben.

Tabelle53: TAB_KON_720 Ablauf EjectCard

 ---> TABLE

Tabelle54: TAB_KON_721 Fehlercodes Operation „EjectCard“

 ---> TABLE

**[\<=]**

### 4.1.4.6 Betriebsaspekte

### 4.1.4.6.1 Allgemeine Betriebsaspekte

##### TIP1-A_4549

Während des Bootvorgangs, nach dem Einlesen der persistierten Informationen des
Kartenterminaldienstes MUSS der Konnektor für jedes Kartenterminal CT in
CTM_CT_LIST:

 ---> UL

**[\<=]**

Hinweis: Bei der Initialiserung des Kartenterminaldienstes liest der Konnektor
noch nicht die Karten, um zu ermitteln, welche Karten gesteckt sind. Dies
erfolgt erst bei Initialisierung des Kartendienstes.

##### TIP1-A_4550

Die Managementschnittstelle MUSS es einem Administrator ermöglichen
Konfigurationsänderungen gemäß Tabelle TAB_KON_527 vorzunehmen:

Tabelle55: TAB_KON_527 Konfigurationswerte eines Kartenterminalobjekts

 ---> TABLE

**[\<=]**

##### TIP1-A_4986

Die Managementschnittstelle MUSS es einem Administrator ermöglichen die
Informationsparameter gemäß Tabelle TAB_KON_528 einzusehen:

Tabelle56: TAB_KON_528 Informationsparamter des Kartenterminaldienstes

 ---> TABLE

**[\<=]**

### 4.1.4.6.2 Kartenterminals pflegen

Im Folgenden werden die Administratorinteraktionen beschrieben, die zum
Hinzufügen, Pairen, Bearbeiten und Löschen von Kartenterminals innerhalb der
CTM_CT_LIST angeboten werden müssen. Eine Aktualisierung der Kartenterminals
mit neuer Firmware wird in Kapitel 4.3.9 beschrieben.

##### TIP1-A_4551

Die Managementschnittstelle MUSS es einem Administrator ermöglichen die Liste
der verwalteten und neu entdeckten Kartenterminals einzusehen (CTM_CT_LIST). **[\<=]**

##### TIP1-A_4552

Die Managementschnittstelle MUSS es einem Administrator ermöglichen zu jedem
CT-Object-Eintrag in CTM_CT_LIST mit CT.CONNECTED=Nein und CT.CORRELATION=aktiv
einen manuellen Verbindungsaufbau
überTUC_KON_050 {ctId=CtID;role=„User“}auszulösen. **[\<=]**

##### TIP1-A_4553

Die Managementschnittstelle MUSS es einem Administrator ermöglichen zu jedem
CT-Object-Eintrag in CTM_CT_LIST die Werte gemäß Tabelle TAB_KON_529 einsehen
zu können:Zu jedem Eintrag MUSS der Administrator TUC_KON_055 „Befülle
CT-Object“ auslösen können.

Tabelle57: TAB_KON_529 Anzeigewerte zu einem Kartenterminalobjekt

 ---> TABLE

**[\<=]**

##### TIP1-A_4554

Die Managementschnittstelle MUSS es einem Administrator ermöglichen zu jedem
CT-Object-Eintrag in CTM_CT_LIST die Werte gemäß Tabelle TAB_KON_530 ändern
zu können:Zur Überprüfung der veränderten Parameter auf Korrektheit MUSS
nach Änderung von CT.IP_ADRESS, TCP_PORT oder HOSTNAME TUC_KON_054 mit Mode=
ManuallyModified und allen vorhandenen CT-Parametern aufgerufen werden. Endet
der Aufruf von TUC_KON_054 mit einem Fehler, MUSS der Konnektor die geänderten
Konfigurationswerte auf ihren Ausgangswert zurücksetzen.

Tabelle58: TAB_KON_530 Konfigurationswerte eines Kartenterminalobjekts

 ---> TABLE

**[\<=]**

##### TIP1-A_6477

Die Managementschnittstelle MUSS es einem Administrator ermöglichen, ein
Service Discovery entsprechend [SICCT] auszulösen, um neue Kartenterminals
hinzuzufügen. **[\<=]**

##### TIP1-A_4555

Die Managementschnittstelle MUSS es einem Administrator ermöglichen für neue
Kartenterminals CT-Objects manuell in CTM_CT_LIST aufzunehmen.Hierzu MUSS der
Administrator für das neue Kartenterminal folgende Werte eingeben können:

 ---> UL

Bestätigt der Administrator seine Eingaben, MUSS TUC_KON_054 mit
Mode=ManuallyAdded und allen eingegebenen Parametern aufgerufen werden. **[\<=]**

Als Sicherung gegen den unbemerkten Austausch von Kartenterminals oder deren
Identitäten wird das gSMC-KT über den Konnektor logisch an das
eHealth-Kartenterminal gebunden. Dieser Vorgang wird als Pairing von
Kartenterminal und gSMC-KT bezeichnet und ist ausführlich in [gemSpec_KT]
beschrieben.

##### TIP1-A_4556

Die Managementschnittstelle MUSS es einem Administrator ermöglichen alle
Kartenterminals mitCT.CORRELATION= „zugewiesen“ in einer Liste einzusehen
und für einen ausgewählten Eintrag mit CT.VALID_VERSION=True TUC_KON_053
auslösen zu können. **[\<=]**

##### TIP1-A_4557

Die Managementschnittstelle MUSS es einem Administrator ermöglichen zu einem
Kartenterminal aus CTM_CT_LIST für KTs mit CT.IS_PHYSICAL=Ja den Wert für
CT.CORRELATION nach folgenden Mustern zu ändern:

 ---> UL

**[\<=]**

##### TIP1-A_5698

Die Managementschnittstelle MUSS einem Administrator die Möglichkeit bieten,
Kartenterminals aus der Liste der Kartenterminals (CTM_CT_LIST) zu entfernen.
**[\<=]**

### 4.1.4.6.3 Import der Kartenterminal-Informationen

Im Rahmen des Konnektormanagements müssen die Konfigurationsdaten des
Konnektors ex- und importiert werden können (siehe Kapitel 4.3.3). Eine
Sonderstellung nimmt dabei der Import von Kartenterminalinformationen ein, da
hier im Rahmen des Imports folgende Interaktion mit dem Administrator
erforderlich ist:

##### TIP1-A_5011

Der Konnektor MUSS vor der endgültigen Aktivierung der importierten
Kartenterminalkonfiguration folgende zusätzliche Schritte ausführen:

 ---> OL

**[\<=]**

### 4.1.5 Kartendienst

Innerhalb des Kartendienstes werden folgende Präfixe für Bezeichner verwendet:

 ---> UL

Der Konnektor verwaltet eine Liste aller Karten (CM_CARD_LIST), die in die vom
Konnektor verwalteten Kartenterminals gesteckt sind (CTM_CT_LIST). Alle
Ereignisse und Operationen, die sich auf Karten beziehen, werden durch diesen
Basisdienst gekapselt.

Für jede gesteckte Karte vergibt er einen eindeutigen Identifikator (im
weiteren Text CardHandle bezeichnet), mit dem diese Karte adressiert werden
kann, um zu diesen oder mit diesen Karten Operationen auszuführen. Dieses
Handle ist gültig bis zum Entfernen der Karte aus dem Kartenterminal.

Um die in [gemSpec_Perf] geforderten Zeiten für kartenbezogene Operationen
erreichen zu können, kann es erforderlich sein, dass der Konnektor möglichst
viele Informationen der Karten cached. Hierzu gehören Steuerdaten wie Extended
Length, Version etc. aber auch Zertifikate der Karte (X.509 und CVC). Da es
sich bei Caching um einen internen Mechanismus handelt, der sich nicht auf das
funktionale Außenverhalten von TUCs oder Operationen auswirkt, wird das
Caching nicht weiter beschrieben oder explizit gefordert. Es kann aber
Anforderungen aus Sicherheitssicht bezüglich des Cachings geben (insbesondere
hinsichtlich der erlaubten Caching-Dauer). Die Einhaltung dieser Vorgaben wird
im Rahmen der CC-Evaluierung geprüft werden.

Der Kartendienst verwaltet mindestens die in der informativen Tabelle
TAB_KON_531 ausgewiesenen Parameter, weitere herstellerspezifische Parameter
sind möglich. Die normative Festlegung wann welche Parameter wie belegt
werden, erfolgt in den folgenden Abschnitten und Unterkapiteln.

 ---> TABLE

### 4.1.5.1 Funktionsmerkmalweite Aspekte

##### TIP1-A_4988-02

Der Konnektor MUSS für eGK, HBA, SMC-B, gSMC-KT und gSMC-K Karten der
Generation 2 unterstützen. Karten der Generation 2 sind alle Karten, deren
Version des dem aktiven Objektsystem zugrundeliegenden Produkttyps (Tag
‘C1‘ in EF.Version2) den Wert 4.x.y hat, wobei x,y in {0, …, 255}.Der
Konnektor DARF eGKs der Generation \< 2 (also 1 und 1+) NICHT unterstützen.
eGKs der Generation \< 2 werden im Konnektor als CARD.TYPE = UNKNOWN
geführt.Bei Karten der Generation 2

 ---> UL

**[\<=]**

Es kann notwendig sein, Karten der Generation 2 (G2) näher zu bezeichnen. In
diesem Fall wird in G2.0- und G2.1-Karten unterschieden. Wird von Karten der
Generation 2 gesprochen, so gilt die Festlegung für G2.x (G2.0, G2.1 und
höher) des betrachteten Kartentyps.

##### TIP1-A_4558

Sofern der Konnektor Daten gesteckter Karten cached, so DÜRFEN diese Daten von
HBAx und SM-B NICHT länger als 24 Stunden gecached werden.

Der Konnektor DARF Daten der eGK NICHT über den Steckzyklus der Karte
hinauscachen.Ausnahme: Eine Cachingdauer über den Steckzyklus der eGK hinaus
wird voneiner Fachanwendung gefordert und durch die Fachmodulspezifikation
dieser Fachanwendung definiert. **[\<=]**

##### TIP1-A_6031

Der Konnektor DARF NICHT selbsttätig die SM-B und deren Sicherheitszustände
zurücksetzen, auch nicht, wenn die Daten der SM-B nach Ablauf der
24-Stunden-Frist neu in den Cache eingelesen werden. **[\<=]**

##### TIP1-A_4559

Der Konnektor DARF NICHT auf das DF.KT einer gSMC-KT zugreifen. **[\<=]**

##### TIP1-A_4560

Der Konnektor MUSS alle Zugriffe auf Karten ausCM_CARD_LIST,die den
Sicherheitszustand der Karte erhöhen können oder einen erhöhten
Sicherheitszustand der Karte voraussetzen, im Kontext einer Kartensitzung zu
dieser Karte durchführen (CARD.CARDSESSION). Ausgenommen hiervon ist der
Zugriff durch das CMS(bzw. VSDD)auf die eGK.

Der Konnektor MUSS sicherstellen, dass in einer Kartensitzung nur dann auf einen
erhöhten Sicherheitszustand einer Karte zugegriffen werden kann, wenn die zur
Erreichung dieses Sicherheitszustandes erforderlichen Authentisierungen
(PIN-Verifikation, C2C-Rollen-Authentisierung etc.) in dieser verwendeten
Kartensitzung erfolgreich durchgeführt wurden.

Der Konnektor MUSS Authentisierungen in einer Kartensitzung so durchführen,
dass in anderen KartensitzungenvorhandeneSicherheitszustände nicht beeinflusst
werden. (Eine falsche PIN-Eingabe in einer Kartensitzung darf
denerhöhtenSicherheitszustand einer anderen Sitzung nicht zurücksetzen etc.).

Der Konnektor SOLL die Verwaltung der Sicherheitsstatus der Kartensitzungen so
über die Nutzung logischer Kartenkanäle umsetzen, dass PIN-Verifikationen,
die für die Dauer der Kartensitzung Gültigkeit haben, nicht unnötig
wiederholt werden müssen. **[\<=]**

Für die TUCs zur PIN-Eingabe, Änderung und Entsperrung sind Festlegungen
hinsichtlich der auf dem Kartenterminal anzuzeigenden Meldungen erforderlich.
Die folgende Tabelle definiert diese Terminalanzeigen gemäß [SICCT#5.5.10.19].

##### TIP1-A_4561-02

Der Konnektor MUSS im Rahmen des interaktiven PIN-Handlings die folgenden
Displaymessages für die Anzeige im Kartenterminal verwenden:

Tabelle60: TAB_KON_090 Terminalanzeigen beim Eingeben der PIN am Kartenterminal

 ---> TABLE

**[\<=]**

Hinweise zu den Terminalanzeigen bei PIN-Eingaben und zu obiger Tabelle:

 ---> UL

In den Technischen Use Cases TUC_KON_012 „PIN verifizieren“, TUC_KON_019
„PIN ändern“, TUC_KON_021 „PIN entsperren“ wird das
Remote-PIN-Verfahren verwendet, sofern die Zielkarte in einem als für den
Arbeitsplatz entfernt definiertem Kartenterminal steckt (siehe Kap. 4.1.1.1,
Relation [7]). In diesem Fall erfolgt die Nutzerinteraktion am Remote-PIN-KT
von workplaceId (PinInputKT). Dabei wendet der Konnektor das folgende Verfahren
an:

##### TIP1-A_5012

Der Konnektor MUSS das Remote-PIN Verfahren im Sinne der BSI TR-03114
unterstützen. Abweichend von der TR-03114 MUSS statt der SMC-A eine gSMC-KT
verwendet werden.Der Konnektor MUSS für die PIN-Objekte: HBA.PIN.CH,
HBA.PUK.CH, HBA.PIN.QES, HBA.PUK.QES, SM-B.PIN.SMC und SM-B.PUK.SMC das
Remote-PIN Verfahren unterstützen. Für alle anderen Karten und PIN-Objekte
DARF das Verfahren NICHT verwendet werden.Für die Interaktion mit dem Anwender
MÜSSEN die Display Messages entsprechend TAB_KON_090 Terminalanzeigen beim
Eingeben der PIN am Kartenterminal verwendet werden.Der Ablauf für eine
PIN-Operation gegen eine Zielkarte MUSS in diesen logischen Schritten erfolgen:

 ---> OL

Fehlermeldung: Ein Fehler in der Verarbeitung führt zum Abbruch mit Fehlercode
4053 „Remote-PIN nicht möglich“ (Security, Error). **[\<=]**

Hinweis: Derzeit schlägt die Freischaltung der SMC-B durch
Card-2-Card-Authentisierung ohne Fehlermeldung fehl. Der Sicherheitszustand der
SMC-B wird nicht verändert. Diese Einschränkung betrifft TUC_KON_005
„Card-to-Card authentisieren“ (TAB_KON_096).

### 4.1.5.2 Durch Ereignisse ausgelöste Reaktionen

##### TIP1-A_4562

Empfängt der Kartendienst das Ereignis „CT/SLOT_FREE“, so MUSS der
Konnektor:

 ---> UL

**[\<=]**

##### TIP1-A_4563

Empfängt der Kartendienst das Ereignis „CT/SLOT_IN_USE“, so MUSS der
Konnektor für die Karte, die über dieim Ereignis gemeldeten ParameterCtID und
SlotNo adressiert ist, über TUC_KON_001 ein neues CardObject in CM_CARD_LIST
anlegen. **[\<=]**

### 4.1.5.3 Interne TUCs, nicht durch Fachmodule nutzbar

### 4.1.5.3.1 TUC_KON_001 „Karte öffnen“

##### TIP1-A_4565

Der Konnektor MUSS den technischen Use Case „Karte öffnen“ gemäß
TUC_KON_001 umsetzen.

Tabelle61: TAB_KON_734 – TUC_KON_001 „Karte öffnen“

 ---> TABLE

**[\<=]**

### 4.1.5.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.1.5.4.1 TUC_KON_026 „Liefere CardSession“

##### TIP1-A_4566

Der Konnektor MUSS den technischen Use Case „Liefere CardSession“ gemäß
TUC_KON_26 umsetzen.

Tabelle62: TAB_KON_735 - TUC_KON_026

 ---> TABLE

Tabelle63: TAB_KON_824 Fehlercodes TUC_KON_026 „Liefere CardSession“

 ---> TABLE

**[\<=]**

Hinweis zu TAB_KON_735 - TUC_KON_026: Die WorkplaceId wird als
Eingangsparameter nicht benötigt. Bereits TUC_KON_000 stellt sicher, dass eine
eGK jeweils nur von einem einzigen Arbeitsplatz aus angesprochen werden kann.

### 4.1.5.4.2 TUC_KON_012 „PIN verifizieren“

##### TIP1-A_4567

Der Konnektor MUSS den technischen Use Case „PIN verifizieren“ gemäß
TUC_KON_012 umsetzen.

Tabelle64: TAB_KON_087 – TUC_KON_012 „PIN verifizieren“

 ---> TABLE

![Img-011][Img-011]

Abbildung10: PIC_KON_111 Aktivitätsdiagramm zu „PIN verifizieren“

Tabelle65: TAB_KON_089 Fehlercodes TUC_KON_012 „PIN verifizieren“

 ---> TABLE

**[\<=]**

### 4.1.5.4.3 TUC_KON_019 „PIN ändern“

##### TIP1-A_4568

Der Konnektor MUSS den technischen Use Case „PIN ändern“ gemäß
TUC_KON_019 umsetzen.

Tabelle66: TAB_KON_736 – TUC_KON_019 „PIN ändern“

 ---> TABLE

Tabelle67: TAB_KON_093 Fehlercodes TUC_KON_019 „PIN ändern“

 ---> TABLE

**[\<=]**

### 4.1.5.4.4 TUC_KON_021 „PIN entsperren“

##### TIP1-A_4569-02

Der Konnektor MUSS den technischen Use Case „PIN entsperren“ gemäß
TUC_KON_021 umsetzen.

Tabelle68: TAB_KON_236 – TUC_KON_021 „PIN entsperren“

 ---> TABLE

Tabelle69: TAB_KON_193 Fehlercodes TUC_KON_021 „PIN entsperren“

 ---> TABLE

**[\<=]**

### 4.1.5.4.5 TUC_KON_022 „Liefere PIN-Status“

##### TIP1-A_4570

Der Konnektor MUSS den technischen Use Case „Liefere PIN-Status“ gemäß
TUC_KON_022 umsetzen.

Tabelle70TAB_KON_532 – TUC_KON_022 „Liefere PIN-Status“

 ---> TABLE

Tabelle71: TAB_KON_091 Fehlercodes TUC_KON_022 „Liefere PIN-Status“

 ---> TABLE

**[\<=]**

### 4.1.5.4.6 TUC_KON_027 „PIN-Schutz ein-/ausschalten“

##### TIP1-A_5486

Der Konnektor MUSS den technischen Use Case TUC_KON_027 „PIN-Schutz
ein-/ausschalten“ umsetzen.

Tabelle72: TAB_KON_240 - TUC_KON_027 „PIN-Schutz ein-/ausschalten”

 ---> TABLE

Tabelle73: TAB_KON_838 Mapping von pinRef auf ANW

 ---> TABLE

Hinweis zu TAB_KON_838: Leerzeichen werden als "•" dargestellt.

Tabelle74: TAB_KON_241 Fehlercodes TUC_KON_027 „PIN-Schutz ein/ausschalten“

 ---> TABLE

**[\<=]**

### 4.1.5.4.7 TUC_KON_023 „Karte reservieren“

##### TIP1-A_4571

Der Konnektor MUSS den technischen Use Case „Karte reservieren“ gemäß
TUC_KON_023 umsetzen.

Tabelle75: TAB_KON_533 - TUC_KON_023 „Karte reservieren”

 ---> TABLE

Tabelle76: TAB_KON_534 Fehlercodes TUC_KON_023 „Karte reservieren“

 ---> TABLE

**[\<=]**

### 4.1.5.4.8 TUC_KON_005 „Card-to-Card authentisieren“

Die C2C-Authentisierung erfolgt konform zu den in [gemSpec_COS#15] festgelegten
Authentisierungsprotokollen.

Definition Quellkarte/Zielkarte:

Bei einseitiger Card-to-Card-Authentisierung ohne Aushandlung eines Session Key
ist die Quellkarte diejenige, die die Rolle des Karteninhabers bzw. der
Organisation gemäß [gemSpec_PKI_TI#Tab_PKI_254] gegenüber der anderen Karte
nachweist, z. B. der HBA bei der Freischaltung einer eGK.

Bei gegenseitiger Card-to-Card-Authentisierung ohne Aushandlung eines Session
Key erfolgen nach einander zwei einseitige Card-to-Card-Authentisierungen mit
vertauschten Rollen. Quell- und Zielkarte habe daher für den Gesamtablauf
keine nähere Bedeutung.

Bei Card-to-Card-Authentisierung mit Aushandlung eines Session Key ist die
Quellkarte diejenige, die die SM-APDUs produzieren kann, also die SMC (-KT oder
-K).

Die Zielkarte ist jeweils die Karte, die nicht die Quellkarte ist.

##### TIP1-A_4572

Der Konnektor MUSS den technischen Use Case „Card-to-Card authentisieren“
gemäß TUC_KON_005 umsetzen.

Die Card-to-Card-Authentisierung zwischen zwei Karten, bei der eine Karte der
Generation 1+ angehört MUSS das RSA-Verfahren verwenden.

Die Card-to-Card-Authentisierung zwischen zwei Karten der Generation 2 MUSS das
Verfahren der elliptischen Kurven verwenden.

Tabelle77: TAB_KON_096 – TUC_KON_005 „Card-to-Card authentisieren”

 ---> TABLE

Tabelle78: TAB_KON_673 AuthMode für C2C

 ---> TABLE

Tabelle79: TAB_KON_674 Erlaubte Parameterkombinationen und resultierende
CV-Zertifikate für C2C

 ---> TABLE

Tabelle80: TAB_KON_535 Fehlercodes TUC_KON_005 „Card-to-Card authentisieren“

 ---> TABLE

**[\<=]**

### 4.1.5.4.9 TUC_KON_202 „LeseDatei“

##### TIP1-A_4573

Der Konnektor MUSS den technischen Use Case „LeseDatei“ gemäß TUC_KON_202
umsetzen.

Tabelle81: TAB_KON_218 – TUC_KON_202 „LeseDatei“

 ---> TABLE

Tabelle82: TAB_KON_536 Fehlercodes TUC_KON_202 „LeseDatei“

 ---> TABLE

**[\<=]**

### 4.1.5.4.10 TUC_KON_203 „SchreibeDatei“

##### TIP1-A_4574

Der Konnektor MUSS den technischen Use Case „SchreibeDatei“ gemäß
TUC_KON_203 umsetzen.

Tabelle83: TAB_KON_219 – TUC_KON_203 „SchreibeDatei“

 ---> TABLE

Tabelle84: TAB_KON_537 Fehlercodes TUC_KON_203 „Schreibe Datei“

 ---> TABLE

**[\<=]**

### 4.1.5.4.11 TUC_KON_204 „LöscheDateiInhalt“

##### TIP1-A_5476

Der Konnektor MUSS den technischen Use Case „LöscheDateiInhalt“ gemäß
TUC_KON_204 umsetzen.

Tabelle85: TAB_KON_204 – TUC_KON_204 „LöscheDateiInhalt“

 ---> TABLE

Tabelle86: TAB_KON_785 Fehlercodes TUC_KON_204 „LöscheDateiInhalt“

 ---> TABLE

**[\<=]**

### 4.1.5.4.12 TUC_KON_209 „LeseRecord“

##### TIP1-A_4575

Der Konnektor MUSS den technischen Use Case „LeseRecord“ gemäß TUC_KON_209
umsetzen.

Tabelle87: TAB_KON_538 – TUC_KON_209 „LeseRecord“

 ---> TABLE

Tabelle88: TAB_KON_539 Fehlercodes TUC_KON_209 „LeseRecord“

 ---> TABLE

**[\<=]**

### 4.1.5.4.13 TUC_KON_210 „SchreibeRecord“

##### TIP1-A_4576

Der Konnektor MUSS den technischen Use Case „SchreibeRecord“ gemäß
TUC_KON_210 umsetzen.

Tabelle89: TAB_KON_224 – TUC_KON_210 „SchreibeRecord“

 ---> TABLE

Tabelle90: TAB_KON_540 Fehlercodes TUC_KON_210 „SchreibeRecord“

 ---> TABLE

**[\<=]**

### 4.1.5.4.14 TUC_KON_211 „LöscheRecordInhalt“

##### TIP1-A_5477

Der Konnektor MUSS den technischen Use Case „LöscheRecordInhalt“ gemäß
TUC_KON_211 umsetzen.

Tabelle91: TAB_KON_211 – TUC_KON_211 „LöscheRecordInhalt“

 ---> TABLE

Tabelle92: TAB_KON_786 Fehlercodes TUC_KON_211 „LöscheRecordInhalt“

 ---> TABLE

**[\<=]**

### 4.1.5.4.15 TUC_KON_214 „FügeHinzuRecord“

##### TIP1-A_4577

Der Konnektor MUSS den technischen Use Case „FügeHinzuRecord“ gemäß
TUC_KON_214 umsetzen.

Tabelle93: TAB_KON_228 – TUC_KON_214 „FügeHinzuRecord“

 ---> TABLE

Tabelle94: TAB_KON_541 Fehlercodes TUC_KON_214 „FügeHinzuRecord“

 ---> TABLE

**[\<=]**

### 4.1.5.4.16 TUC_KON_215 „SucheRecord“

##### TIP1-A_4578

Der Konnektor MUSS den technischen Use Case „SucheRecord“ gemäß
TUC_KON_215 umsetzen.

Tabelle95: TAB_KON_229 – TUC_KON_215 „SucheRecord“

 ---> TABLE

Tabelle96: TAB_KON_542 Fehlercodes TUC_KON_215 „SucheRecord“

 ---> TABLE

**[\<=]**

### 4.1.5.4.17 TUC_KON_018 „eGK-Sperrung prüfen“

##### TIP1-A_4579

Der Konnektor MUSS den technischen Use Case „eGK-Sperrung prüfen“ gemäß
TUC_KON_018 umsetzen.

Tabelle97: TAB_KON_110 - TUC_KON_018 „eGK-Sperrung prüfen“

 ---> TABLE

Tabelle98: TAB_KON_239 Fehlercodes TUC_KON_018 „eGK-Sperrung prüfen“

 ---> TABLE

**[\<=]**

### 4.1.5.4.18 TUC_KON_006 „Datenzugriffsaudit eGK schreiben“

##### TIP1-A_4580

Der Konnektor MUSS den technischen Use Case „Datenzugriffsaudit eGK
schreiben“ gemäß TUC_KON_006 umsetzen.

Tabelle99: TAB_KON_108 - TUC_KON_006 „Datenzugriffsaudit eGK schreiben“

 ---> TABLE

Tabelle100: TAB_KON_238 Fehlercodes TUC_KON_006 „Datenzugriffsaudit eGK
schreiben“

 ---> TABLE

**[\<=]**

### 4.1.5.4.19 TUC_KON_218 „Signiere“

##### TIP1-A_4581

Der Konnektor MUSS den technischen Use Case „Signiere“ gemäß TUC_KON_218
umsetzen.

Tabelle101: TAB_KON_231 – TUC_KON_218 „Signiere“

 ---> TABLE

Tabelle102: TAB_KON_543 Fehlercodes TUC_KON_218 „Signiere“

 ---> TABLE

**[\<=]**

### 4.1.5.4.20 TUC_KON_219 „Entschlüssele“

##### TIP1-A_4582

Der Konnektor MUSS den technischen Use Case „Entschlüssele“ gemäß
TUC_KON_219 umsetzen.

Tabelle103: TAB_KON_232 – TUC_KON_219 „Entschlüssele“

 ---> TABLE

Tabelle104: TAB_KON_210 Fehlercodes TUC_KON_219 „Entschlüssele“

 ---> TABLE

**[\<=]**

### 4.1.5.4.21 TUC_KON_200 „SendeAPDU“

##### TIP1-A_4583

Der Konnektor MUSS den technischen Use Case „SendeAPDU“ gemäß TUC_KON_200
umsetzen.

Tabelle105: TAB_KON_215 TUC_KON_200 „SendeAPDU“

 ---> TABLE

Tabelle106: TAB_KON_216 Fehlercodes TUC_KON_200 „SendeAPDU“

 ---> TABLE

**[\<=]**

### 4.1.5.4.22 TUC_KON_024 „Karte zurücksetzen“

##### TIP1-A_4584

Der Konnektor MUSS den technischen Use Case „Karte zurücksetzen“ gemäß
TUC_KON_024 umsetzen.

Tabelle107: TAB_KON_737 – TUC_KON_024 „Karte zurücksetzen“

 ---> TABLE

Tabelle108: TAB_KON_544 Fehlercodes TUC_KON_024 „Karte zurücksetzen“

 ---> TABLE

**[\<=]**

### 4.1.5.4.23 TUC_KON_216 „LeseZertifikat“

##### TIP1-A_4585

Der Konnektor MUSS den technischen Use Case „LeseZertifikat“ gemäß
TUC_KON_216 umsetzen.

Tabelle109: TAB_KON_230 – TUC_KON_216 „LeseZertifikat“

 ---> TABLE

Tabelle110: TAB_KON_209 Fehlercodes TUC_KON_216 „LeseZertifikat“

 ---> TABLE

**[\<=]**

### 4.1.5.4.24 TUC_KON_036 „LiefereFachlicheRolle“

##### TIP1-A_5478

Der Konnektor MUSS den technischen Use Case TUC_KON_036
„LiefereFachlicheRolle” umsetzen.

Tabelle111: TAB_KON_827 TUC_KON_036 „LiefereFachlicheRolle“

 ---> TABLE

Tabelle112: TAB_KON_829 Fehlercodes TUC_KON_036 „LiefereFachlicheRolle“

 ---> TABLE

**[\<=]**

### 4.1.5.5 Operationen an der Außenschnittstelle

##### TIP1-A_4586-03

Der Konnektor MUSS für Clients eine Basisanwendung Kartendienst mit den
Operationen VerifyPin, ChangePin, UnblockPin, GetPinStatus an der
Außenschnittstelle anbieten.

Tabelle113: TAB_KON_038 Basisanwendung Karten- und Kartenterminaldienst

 ---> TABLE

**[\<=]**

### 4.1.5.5.1 VerifyPin

##### TIP1-A_4587

Der Konnektor MUSS an der Außenschnittstelle eine Operation VerifyPin, wie in
Tabelle TAB_KON_047 Operation VerifyPin beschrieben, anbieten.

Tabelle114: TAB_KON_047 Operation VerifyPin

 ---> TABLE

Der Ablauf der Operation VerifyPin ist in Tabelle TAB_KON_738 Ablauf VerifyPin
beschrieben.

Tabelle115: TAB_KON_738 Ablauf VerifyPin

 ---> TABLE

Tabelle116: TAB_KON_545 Fehlercodes „VerifyPin“

 ---> TABLE

**[\<=]**

### 4.1.5.5.2 ChangePin

##### TIP1-A_4588

Der Konnektor MUSS an der Außenschnittstelle eine Operation ChangePin, wie in
Tabelle TAB_KON_049 Operation ChangePin beschrieben, anbieten.

Tabelle117: TAB_KON_049 Operation ChangePin

 ---> TABLE

Tabelle118: TAB_KON_546 Ablauf ChangePin

 ---> TABLE

Tabelle119: TAB_KON_547 Fehlercodes „ChangePin“

 ---> TABLE

**[\<=]**

### 4.1.5.5.3 GetPinStatus

##### TIP1-A_4589

Der Konnektor MUSS an der Außenschnittstelle eine Operation GetPinStatus, wie
in Tabelle TAB_KON_051 Operation GetPinStatus beschrieben, anbieten.

Tabelle120: TAB_KON_051 Operation GetPinStatus

 ---> TABLE

Tabelle121: TAB_KON_548 Ablauf GetPinStatus

 ---> TABLE

Tabelle122: TAB_KON_549 Fehlercodes „GetPinStatus“

 ---> TABLE

**[\<=]**

### 4.1.5.5.4 UnblockPin

##### TIP1-A_4590

Der Konnektor MUSS an der Außenschnittstelle eine Operation UnblockPin, wie in
Tabelle TAB_KON_053 Operation UnblockPin beschrieben, anbieten.

Tabelle123: TAB_KON_053 Operation UnblockPin

 ---> TABLE

Tabelle124: TAB_KON_550 Ablauf UnblockPIN

 ---> TABLE

Tabelle125: TAB_KON_551 Fehlercodes „UnblockPin“

 ---> TABLE

**[\<=]**

### 4.1.5.5.5 EnablePin

##### TIP1-A_5487

Der Konnektor MUSS an der Außenschnittstelle eine Operation EnablePin, wie in
Tabelle TAB_KON_242 Operation EnablePin beschrieben, anbieten.

Tabelle126: TAB_KON_242 Operation EnablePin

 ---> TABLE

Tabelle127: TAB_KON_243 Ablauf EnablePin

 ---> TABLE

Tabelle128: TAB_KON_244 Fehlercodes „EnablePin“

 ---> TABLE

**[\<=]**

### 4.1.5.5.6 DisablePin

##### TIP1-A_5488

Der Konnektor MUSS an der Außenschnittstelle eine Operation DisablePin, wie in
Tabelle TAB_KON_245 Operation DisablePin beschrieben, anbieten.

Tabelle129: TAB_KON_245 Operation DisablePin

 ---> TABLE

Tabelle130: TAB_KON_246 Ablauf DisablePin

 ---> TABLE

Tabelle131: TAB_KON_247 Fehlercodes „DisablePin“

 ---> TABLE

**[\<=]**

### 4.1.5.6 Betriebsaspekte

##### TIP1-A_4592

Der Konnektor MUSS es einem Administrator ermöglichen,
Konfigurationsänderungen gemäß Tabelle TAB_KON_554 vorzunehmen.

Tabelle132: TAB_KON_554 Konfiguration des Kartendienstes

 ---> TABLE

**[\<=]**

### 4.1.5.6.1 TUC_KON_025 "Initialisierung Kartendienst"

##### TIP1-A_4593

Der Konnektor MUSS den technischen Use Case „Initialisierung Kartendienst“
gemäß TUC_KON_025 umsetzen.

Tabelle133: TAB_KON_555 - TUC_KON_025 „Initialisierung Kartendienst“

 ---> TABLE

**[\<=]**

### 4.1.5.6.2 Kartenübersicht und PIN-Management

##### TIP1-A_5110

Die Administrationsoberfläche MUSS dem Administrator eine Übersichtsseite
anbieten, die alle in CM_CARD_LIST enthaltenen Karten listet.In dieser
Übersichtsseite muss zu jeder Karte dargestellt werden:

 ---> UL

Ferner MÜSSEN auf Verlangen des Administrators zu jeder Karte neben den obigen
Informationen auch folgende Details angezeigt werden:

 ---> UL

**[\<=]**

##### TIP1-A_5111

Über die Administrationsoberfläche MUSS der Administrator für jede in der
Übersichtsseite angezeigte Karte vom Typ SM-B die folgenden TUCs für die
PIN.SMC auslösen können.Für diese MUSS er einen der gemäß Kapitel 4.1.1.6
[TIP1-A_4526] definierten Mandanten auswählen können:

 ---> UL

Die Eingabe der PIN SOLL von jedem vom Informationsmodell her zulässigen
Kartenterminal aus möglich sein. **[\<=]**

Der Konnektor kann den Administrator zur Laufzeit entscheiden lassen, an welchem
Kartenterminal die PIN eingegeben werden soll, indem er ihn wählen lässt, ob
er die PIN am Kartenterminal eingibt, in dem die betroffene SM-B steckt, oder
ihn den Arbeitsplatz wählen lässt, von dem aus er die Remote-PIN eingibt.

### 4.1.6 Systeminformationsdienst

Der Systeminformationsdienst stellt Basisdiensten, Fachmodulen und
Clientsystemen sowohl aktiv (Push-Mechanismus) wie passiv (Pull-Mechanismus)
Informationen zur Verfügung. Dabei erhebt er selbst keine Daten, sondern dient
nur als zentraler Mechanismus, der von anderen Basisdiensten und Fachmodulen
zur Verteilung und Bereitstellung derer Informationen verwendet werden kann.

Innerhalb des Systeminformationsdienstes werden folgende Präfixe für
Bezeichner verwendet:

 ---> UL

Push-Mechanismus

Der Push-Mechanismus des Systeminformationsdienstes hat die Aufgabe, Ereignisse
von internen Ereignisquellen im Konnektor (z. B. von anderen Basisdiensten wie
Kartendienst, Kartenterminaldienst oder Fachmodulen) an alle Basisdienste und
Fachmodule sowie an die bei ihm registrierten Ereignisempfänger
(Clientsysteme) weiterzuleiten.

Die Namen der Ereignisse, die Topics, sind als Baumstruktur organisiert und
werden mittels „/“-getrennter Liste angegeben (z. B.
„Auslöser/Ereigniskategorie1/…/Ereignis1“). Die konkreten Topics werden
innerhalb der einzelnen Funktionsmerkmale kontextbezogen definiert und im
Anhang in einer zentralen Liste übersichtlich dargestellt.

Clientsysteme können sich für den Empfang bestimmter Ereigniskategorien
(Topics) anmelden. Der Systeminformationsdienst übernimmt dementsprechend bei
der Verteilung der Ereignisse auch eine Filterfunktion für die
weiterzuleitenden Ereignisse.

Die Zustellung der Ereignisse erfolgt unidirektional über eine
Netzschnittstelle, deren Kommunikationsendpunkt („Ereignissenke“) vom
Clientsystem realisiert werden muss. Zur Übertragung der Daten wird ein
konnektoreigenes Protokoll cetp (Connector Event Transport Protocol) verwendet.

Pull-Mechanismus

Der Pull-Mechanismus des Systeminformationsdienstes hat die Aufgabe sowohl
Zustandswerte als auch statische Informationen des Konnektors selbst als auch
von den über ihn verwalteten Ressourcen durch Fachmodule und Clientsysteme
abrufbar zu machen. Dabei können entweder Listen von Ressourcen oder Details
zu einzelnen Ressourcen abgerufen werden.

Die folgenden Unterkapitel regeln:

 ---> UL

### 4.1.6.1 Funktionsmerkmalweite Aspekte

##### TIP1-A_4594

DerKonnektorsMUSS zur Übertragung von Ereignissen einecetp-Verbindung zuder
Ereignissenke des Clientsystemsaufbauen, die das Clientsystem beim
Operationsaufruf Subscribe perEventToangegeben hatte. **[\<=]**

##### TIP1-A_5536

Der Konnektor MUSS das Anwendungsprotokoll cetp (Connector Event Transport
Protocol) ausschließlich über das Transportprotokoll TCP (gebenenfalls TLS
gesichert) anbieten. **[\<=]**

##### TIP1-A_4595

Der Konnektor MUSS zur Übertragung der Ereignisse eine gesicherte Verbindung
(TLS) verwenden, die vom Konnektor als TLS-Client initiiert wurde, wenn
ANCL_TLS_MANDATORY=Enabled.Der Konnektor muss sich beim Aufbau der TLS-Sitzung
gegenüber dem Clientsystem authentisieren, wenn dieses eine Authentisierung im
Rahmen des TLS-Handshakes anfordert.Die Schalter ANCL_CAUT_MODE und
ANCL_CAUT_MANDATORY wirken für die Übertragung der Ereignisse nicht. **[\<=]**

Für die Übermittlung der Ereignisse wurde ein leichtgewichtiges Protokoll
gewählt, da vom Clientsystem keine Antwort auf Anwendungsebene erwartet wird.

##### TIP1-A_4596

Der Konnektors MUSS Ereignisse an Ereignissenken mittels Nachrichten verteilen,
die gemäß TAB_KON_030 „Ereignisnachricht“ aufgebaut sind. Der Konnektor
MUSS die Nachrichten mit der Zeichenkette „CETP“ beginnen, gefolgt von der
Länge der folgenden Ereignisnachricht in Anzahl Bytes. Das vier Byte lange
Längenfeld MUSS in der Byte-Reihenfolge Big-Endian codiert werden (das
hochwertigste Byte wird als erstes übertragen).

Abbildung11: PIC_KON_022 Grundsätzlicher Aufbau der Ereignisnachricht

Tabelle134: TAB_KON_030 Ereignisnachricht

 ---> TABLE

​​ **[\<=]**

### 4.1.6.2 Durch Ereignisse ausgelöste Reaktionen

Keine.

### 4.1.6.3 Interne TUCs, nicht durch Fachmodule nutzbar

Keine.

### 4.1.6.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.1.6.4.1 TUC_KON_256 „Systemereignis absetzen“

##### TIP1-A_4598-02

Der Konnektor MUSS für den PUSH-Mechanismus des Systeminformationsdienstes den
technischen Use Case TUC_KON_256 „Systemereignis absetzen” umsetzen.

Tabelle135: TAB_KON_556 - TUC_KON_256 „Systemereignis absetzen“

 ---> TABLE

![Img-012][Img-012]

Abbildung12: PIC_KON_112 Aktivitätsdiagramm zu „Systemereignis absetzen“

Tabelle136: TAB_KON_557 Fehlercodes TUC_KON_256 „Systemereignis absetzen“

 ---> TABLE

**[\<=]**

### 4.1.6.4.2 TUC_KON_252 „Liefere KT_Liste“

##### TIP1-A_4599

Der Konnektor MUSS den technischen Use Case TUC_KON_252 „Liefere KT_Liste”
umsetzen.

Tabelle137: TAB_KON_558 – TUC_KON_252 „Liefere KT_Liste“

 ---> TABLE

**[\<=]**

### 4.1.6.4.3 TUC_KON_253 „Liefere Karten_Liste“

##### TIP1-A_4600

Der Konnektor MUSS den technischen Use Case TUC_KON_253 „Liefere
Karten_Liste” umsetzen.

Tabelle138: TAB_KON_559 – TUC_KON_253 „Liefere Karten_Liste“

 ---> TABLE

Tabelle139: TAB_KON_560 Fehlercodes TUC_KON_253 „Liefere Karten_Liste“

 ---> TABLE

**[\<=]**

### 4.1.6.4.4 TUC_KON_254 „Liefere Ressourcendetails“

##### TIP1-A_4602

Der Konnektor MUSS den technischen Use Case TUC_KON_254 „Liefere
Ressourcendetails” umsetzen.

Tabelle140: TAB_KON_561 - TUC_KON_254 „Liefere Ressourcendetails“

 ---> TABLE

Tabelle141: TAB_KON_562 Fehlercodes TUC_KON_254 „Liefere Ressourcendetails“

 ---> TABLE

**[\<=]**

### 4.1.6.5 Operationen an der Außenschnittstelle

##### TIP1-A_4603-02

Der Konnektor MUSS für Clients eine Basisanwendung Systeminformationsdienst
anbieten.

Tabelle142TAB_KON_029 Basisanwendung Systeminformationsdienst

 ---> TABLE

**[\<=]**

### 4.1.6.5.1 GetCardTerminals

##### TIP1-A_4604

Der Konnektors MUSS an der Außenschnittstelle eine Operation GetCardTerminals,
wie in Tabelle TAB_KON_563 „Operation GetCardTerminals“ beschrieben,
anbieten.

Tabelle143: TAB_KON_563 Operation GetCardTerminals

 ---> TABLE

Der Ablauf der Operation GetCardTerminals ist in Tabelle TAB_KON_564 Ablauf
GetCardTerminals beschrieben:

Tabelle144: TAB_KON_564 Ablauf GetCardTerminals

 ---> TABLE

Tabelle145: TAB_KON_823 Fehlercodes „GetCardTerminals“

 ---> TABLE

​​ **[\<=]**

### 4.1.6.5.2 GetCards

##### TIP1-A_4605

Der Konnektors MUSS an der Außenschnittstelle eine Operation GetCards, wie in
Tabelle TAB_KON_565 „Operation GetCards“ beschrieben, anbieten und MUSS
dabei Kartentypen aus Tabelle TAB_KON_500 Wertetabelle Kartentypen
unterscheiden.

Tabelle146: TAB_KON_565 Operation GetCards

 ---> TABLE

Der Ablauf der Operation GetCards ist in Tabelle TAB_KON_566 Ablauf GetCards
beschrieben:

Tabelle147: TAB_KON_566 Ablauf GetCards

 ---> TABLE

Die Fehlerfälle der Operation GetCards sind in Tabelle TAB_KON_567 Fehlercodes
„GetCards dargestellt:

Tabelle148: TAB_KON_567 Fehlercodes „GetCards“

 ---> TABLE

**[\<=]**

### 4.1.6.5.3 GetResourceInformation

##### TIP1-A_4607

Der Konnektors MUSS an der Außenschnittstelle eine Operation
GetResourceInformation, wie in Tabelle TAB_KON_568 „Operation
GetResourceInformation“ beschrieben, anbieten.

Tabelle149: TAB_KON_568 Operation GetResourceInformation

 ---> TABLE

Der Ablauf der Operation GetResourceInformation ist in Tabelle TAB_KON_569
Ablauf GetResourceInformation beschrieben:

Tabelle150: TAB_KON_569 Ablauf GetResourceInformation

 ---> TABLE

Die Fehlerfälle der Operation GetResourceInformation sind in Tabelle
TAB_KON_570 Fehlercodes „GetResourceInformation dargestellt:

Tabelle151: TAB_KON_570 Fehlercodes „GetResourceInformation“

 ---> TABLE

**[\<=]**

### 4.1.6.5.4 Subscribe

##### TIP1-A_4608

Der Konnektors MUSS an der Außenschnittstelle eine Operation Subscribe, wie in
Tabelle TAB_KON_571 Operation Subscribe beschrieben, anbieten.

Tabelle152: TAB_KON_571 Operation Subscribe

 ---> TABLE

Der Ablauf der Operation Subscribe ist in Tabelle TAB_KON_572 Ablauf Subscribe
beschrieben:

Tabelle153: TAB_KON_572 Ablauf Subscribe

 ---> TABLE

Die Fehlerfälle der Operation Subscribe sind in Tabelle TAB_KON_573 Fehlercodes
„Subscribe dargestellt:

Tabelle154TAB_KON_573 Fehlercodes „Subscribe“

 ---> TABLE

​​ **[\<=]**

### 4.1.6.5.5 Unsubscribe

##### TIP1-A_4609

Der Konnektors MUSS an der Außenschnittstelle eine Operation Unsubscribe, wie
in Tabelle TAB_KON_574 Operation Unsubscribe beschrieben, anbieten.

Tabelle155: TAB_KON_574 Operation Unsubscribe

 ---> TABLE

Der Ablauf der Operation Unsubscribe ist in Tabelle TAB_KON_575 Ablauf
Unsubscribe beschrieben:

Tabelle156: TAB_KON_575 Ablauf Unsubscribe

 ---> TABLE

Die Fehlerfälle der Operation Unsubscribe sind in Tabelle TAB_KON_576
Fehlercodes „Unsubscribe dargestellt:

Tabelle157: TAB_KON_576 Fehlercodes „Unsubscribe“

 ---> TABLE

​​ **[\<=]**

### 4.1.6.5.6 RenewSubscriptions

##### TIP1-A_5112

Der Konnektors MUSS an der Außenschnittstelle eine Operation
RenewSubscriptions, wie in Tabelle TAB_KON_792 Operation RenewSubscriptions
beschrieben, anbieten.

Tabelle158: TAB_KON_792 Operation RenewSubscriptions

 ---> TABLE

Der Ablauf der Operation RenewSubscriptions ist in Tabelle TAB_KON_793 Ablauf
RenewSubscriptions beschrieben:

Tabelle159: TAB_KON_793 Ablauf RenewSubscriptions

 ---> TABLE

Die Fehlerfälle der Operation RenewSubscriptions sind in Tabelle TAB_KON_794
Fehlercodes „RenewSubscriptions dargestellt:

Tabelle160: TAB_KON_794 Fehlercodes „RenewSubscriptions“

 ---> TABLE

​​ **[\<=]**

### 4.1.6.5.7 GetSubscription

##### TIP1-A_4610

Der Konnektor MUSS an der Außenschnittstelle eine Operation GetSubscription,
wie in Tabelle TAB_KON_577 Operation GetSubscription beschrieben, anbieten.

Tabelle161: TAB_KON_577 Operation GetSubscription

 ---> TABLE

Der Ablauf der Operation GetSubscription ist in Tabelle TAB_KON_578 Ablauf
GetSubscription beschrieben:

Tabelle162: TAB_KON_578 Ablauf GetSubscription

 ---> TABLE

Die Fehlerfälle der Operation GetSubscription sind in Tabelle TAB_KON_579
Fehlercodes „GetSubscription dargestellt:

Tabelle163: TAB_KON_579 Fehlercodes „GetSubscription“

 ---> TABLE

​​ **[\<=]**

### 4.1.6.6 Betriebsaspekte

##### TIP1-A_4611

Die Managementschnittstelle MUSS es einem Administrator ermöglichen
Konfigurationsänderungen gemäß Tabelle TAB_KON_580vorzunehmen:

Tabelle164: TAB_KON_580 Konfigurationswerte des Systeminformationsdienstes
(Administrator)

 ---> TABLE

**[\<=]**

##### TIP1-A_4612

Der Konnektor MUSS eine Mindestmenge von 999 Subscriptions insgesamt
unterstützen. Der Konnektorhersteller kann jedoch die Anzahl der maximal
möglichen Subscriptions (insgesamt und/oder pro Ziel) festlegen. **[\<=]**

##### TIP1-A_4613

Der Konnektor MUSS beim Bootupmit einer leeren Liste an Subscriptions starten. **[\<=]**

### 4.1.7 Verschlüsselungsdienst

Der Verschlüsselungsdienst bietet Schnittstellen zum hybriden und symmetrischen
Ver- und Entschlüsseln von Dokumenten an.

Der Verschlüsselungsdienst bietet für alleAlle_DocFormatedie hybride und
symmetrische Ver- und Entschlüsselung nach dem Cryptographic Message Syntax
(CMS) Standard an [RFC5652].

Darüber hinaus werden folgende formaterhaltende
Ver-/Entschlüsselungsmechanismen unterstützt:

 ---> UL

Der Konnektor kann optional folgende formaterhaltende
Ver-/Entschlüsselungsmechanismen unterstützen:

 ---> UL

Dabei soll der Konnektor, wenn er die S/MIME-Verschlüsselung unterstützt, auch
die S/MIME-Entschlüsselung unterstützen.

Der Konnektor muss bezüglich der zur Ver- und Entschlüsselung von Dokumenten
verwendeten Verfahren und Algorithmen die Vorgaben in [gemSpec_Krypt#3.1.4]
sowie in [gemSpec_Krypt#3.1.5] und hinsichtlich ECC-Migration die Vorgaben aus
[gemSpec_Krypt#5] erfüllen.

### 4.1.7.1 Funktionsmerkmalweite Aspekte

##### TIP1-A_4614

DerKonnektorsMUSS zur Unterstützung von Missbrauchserkennungen die in Tabelle
TAB_KON_581 gelisteten Operationen als Einträge in EVT_MONITOR_OPERATIONS
berücksichtigen.

Tabelle165:TAB_KON_581Verschlüsselungsdienst-Operationen
fürEVT_MONITOR_OPERATIONS

 ---> TABLE

**[\<=]**

##### TIP1-A_5434

Der Konnektor MUSS das Operationspaar Verschlüsselung/Entschlüsselung so
implementieren, dass Dokumente vom Typ XML unverändert bleiben, wobei zwei
XML-Dokumente als identisch zu betrachten sind, wenn sie gemäß Canonical XML
1.1 gleich sind [CanonXML1.1]. **[\<=]**

##### A_17746

Der Konnektor MUSS für die kartenbasierte Ver- und Entschlüsselung die
Zertifikate und Schlüssel in Abhängigkeit vom kryptographischen Verfahren
unter Berücksichtigung des Einsatzbereiches aus TAB_KON_747 ermitteln.
**[\<=]**

 ---> TABLE

 ---> TABLE

### 4.1.7.2 Durch Ereignisse ausgelöste Reaktionen

Keine.

### 4.1.7.3 Interne TUCs, nicht durch Fachmodule nutzbar

Keine.

### 4.1.7.4 Interne TUCs, auch durch Fachmodule nutzbar

Die in diesem Kapitel beschriebenen TUCs zur hybriden Ver- und Entschlüsselung
werden den Fachmodulen und Außenoperationen angeboten. Die TUCs zur
symmetrischen Ver-/Entschlüsselung werden den Fachmodulen angeboten. Es gibt
keine Aufrufhierarchie innerhalb der hier beschriebenen TUCs zur hybriden und
symmetrischen Ver-/Entschlüsselung.

### 4.1.7.4.1 TUC_KON_070 „Daten hybrid verschlüsseln”

##### TIP1-A_4616-03

Der Konnektor MUSS den technischen Use Case TUC_KON_070 „Daten hybrid
verschlüsseln” umsetzen.

Tabelle168: TAB_KON_739 - TUC_KON_070 „Daten hybrid verschlüsseln“

 ---> TABLE

![Abbildung-13][Abbildung-13]

Abbildung13: PIC_KON_058 Aktivitätsdiagramm „Daten hybrid verschlüsseln“

Tabelle169: TAB_KON_073 Vorgaben zum Format verschlüsselter XML-Dokumente

 ---> TABLE

Tabelle170: TAB_KON_740 Fehlercodes TUC_KON_070 „Daten hybrid verschlüsseln“

 ---> TABLE

**[\<=]**

### 4.1.7.4.2 TUC_KON_071 „Daten hybrid entschlüsseln”

##### TIP1-A_4617-02

Der Konnektor MUSS den technischen Use Case TUC_KON_071 „Daten hybrid
entschlüsseln” umsetzen.

Tabelle171: TAB_KON_140 – TUC_KON_071 „Daten hybrid entschlüsseln“

 ---> TABLE

![Img-014][Img-014]

Abbildung14: PIC_KON_059 Aktivitätsdiagramm „Daten hybrid entschlüsseln“

Tabelle172: TAB_KON_142 Fehlercodes TUC_KON_071 „Daten hybrid entschlüsseln“

 ---> TABLE

**[\<=]**

### 4.1.7.4.3 TUC_KON_072 „Daten symmetrisch verschlüsseln”

##### TIP1-A_4618

Der Konnektor MUSS den technischen Use Case TUC_KON_072 „Daten symmetrisch
verschlüsseln“ umsetzen.

Tabelle173: TAB_KON_741 – TUC_KON_072 „Daten symmetrisch verschlüsseln“

 ---> TABLE

Tabelle174: TAB_KON_742 Fehlercodes TUC_KON_072 „Daten symmetrisch
verschlüsseln“

 ---> TABLE

**[\<=]**

### 4.1.7.4.4 TUC_KON_073 „Daten symmetrisch entschlüsseln”

##### TIP1-A_4619

Der Konnektor MUSS den technischen Use Case TUC_KON_073 „Daten symmetrisch
entschlüsseln“ umsetzen.

Tabelle175: TAB_KON_743 - TUC_KON_073 „Daten symmetrisch entschlüsseln“

 ---> TABLE

Tabelle176: TAB_KON_744 Fehlercodes TUC_KON_073 „Daten symmetrisch
entschlüsseln“

 ---> TABLE

**[\<=]**

### 4.1.7.4.5 TUC_KON_075 „Symmetrisch verschlüsseln“

##### A_18001

Der Konnektor MUSS den technischen Use Case TUC_KON_075 „Symmetrisch
verschlüsseln“ umsetzen.

Tabelle177: TAB_KON_860 – TUC_KON_075 „Symmetrisch verschlüsseln“

 ---> TABLE

**[\<=]**

### 4.1.7.4.6 TUC_KON_076 „Symmetrisch entschlüsseln“

##### A_18002

Der Konnektor MUSS den technischen Use Case TUC_KON_076 „Symmetrisch
entschlüsseln“ umsetzen.

Tabelle178: TAB_KON_861 - TUC_KON_076 „Symmetrisch entschlüsseln“

 ---> TABLE

**[\<=]**

### 4.1.7.5 Operationen an der Außenschnittstelle

##### TIP1-A_4620-03

Der Konnektor MUSS für Clients einen Basisdienst Verschlüsselungsdienst
anbieten.

Tabelle179: TAB_KON_745 Basisdienst Verschlüsselungsdienst

 ---> TABLE

**[\<=]**

### 4.1.7.5.1 EncryptDocument

##### TIP1-A_4621-05

Der Basisdienst Verschlüsselungsdienst des Konnektors MUSS an der
Clientschnittstelle eine Operation EncryptDocument anbieten.

Tabelle180: TAB_KON_071 Operation EncryptDocument

 ---> TABLE

Der Ablauf der Operation EncryptDocument ist in Tabelle TAB_KON_746 Ablauf
EncryptDocument beschrieben:

Tabelle181: TAB_KON_746 Ablauf EncryptDocument

 ---> TABLE

Tabelle182: TAB_KON_141 Fehlercodes „EncryptDocument“

 ---> TABLE

**[\<=]**

### 4.1.7.5.2 DecryptDocument

##### TIP1-A_4622-05

Der Basisdienst Verschlüsselungsdienst des Konnektors MUSS an der
Clientschnittstelle eine Operation DecryptDocument anbieten.

Tabelle183: TAB_KON_075 Operation DecryptDocument

 ---> TABLE

Der Ablauf der Operation DecryptDocument ist in Tabelle TAB_KON_076 Ablauf
DecryptDocument beschrieben:

Tabelle184: TAB_KON_076 Ablauf DecryptDocument

 ---> TABLE

Tabelle185: TAB_KON_145 Fehlercodes „DecryptDocument“

 ---> TABLE

**[\<=]**

### 4.1.7.6 Betriebsaspekte

keine

### 4.1.8 Signaturdienst

Der Signaturdienst bietet Clientsystemen und Fachmodulen eine Schnittstelle zum
Signieren von Dokumenten und Prüfen von Dokumentensignaturen

Innerhalb des Signaturdienstes werden folgende Präfixe für Bezeichner
verwendet:

 ---> UL

### 4.1.8.1 Funktionsmerkmalweite Aspekte

### 4.1.8.1.1 Dokumentensignatur

Der Signaturdienst umfasst die Funktionalität der nicht-qualifizierten
elektronischen Signatur (nonQES) mit der SM-B, sowie die qualifizierte
elektronische Signatur (QES) mit dem HBA und den HBA-Vorläuferkarten HBA-qSig
und ZOD_2.0 (=HBAx).

In der Abbildung fachlicher Abläufe kann es nötig sein, ein Dokument mehrfach
parallel zu signieren, oder existierende Signaturen gegenzusignieren. Der
Konnektor unterstütztparallele Signaturen(QES und nonQES). Ebenso unterstützt
er Gegensignaturen (QES und nonQES), die jeweils alle bestehenden Signaturen
gegensignieren. Die angebotene Möglichkeit des Gegensignierens bezieht sich
dabei auf das Signieren aller vorhandenen parallelen Signaturen, während ein
Gegensignieren von Gegensignaturen nicht angeboten wird. Der Konnektor
unterstützt ausschließlich eine dokumentexkludierende Gegensignatur, bei der
alle Signaturen gegensigniert werden, aber nicht der fachliche Inhalt des
Dokumentes selbst.

##### TIP1-A_4623-02

Der Signaturdienst MUSS für die Erstellung und Prüfung von
nicht-qualifizierten elektronischen Signaturen (nonQES) für
dienonQES_DocFormatedie Signaturverfahren entsprechend Tabelle TAB_KON_582 –
Signaturverfahren unterstützen. **[\<=]**

##### TIP1-A_4627

Der Signaturdienst MUSS für die Erstellung und Prüfung von qualifizierten
elektronischen Signaturen (QES) für dieQES_DocFormatedie Signaturverfahren
entsprechend Tabelle TAB_KON_582 – Signaturverfahren unterstützen. **[\<=]**

 ---> TABLE

Zu den Begriffen detached, enveloping und enveloped Signaturen siehe
beispielsweise auch [HüKo06#Abs. 4.3.3. und 4.3.1.5].

##### TIP1-A_5447

Der Signaturdienst MUSS für die Erstellung und Prüfung von
nicht-qualifizierten elektronischen Signaturen (nonQES) und qualifizierten
elektronischen Signaturen (QES) die Vorgaben zum Einsatzbereich gemäß Tabelle
TAB_KON_778 umsetzen.

Tabelle187: TAB_KON_778 – Einsatzbereich der Signaturvarianten für XAdES,
CAdES und PAdES

 ---> TABLE

Legende:

Ja: Die Signaturvariante ist für den Einsatzbereich erlaubt.

Nein: Die Signaturvariante ist für den Einsatzbereich nicht erlaubt.

Bedingt: Die Signaturvariante ist für den Einsatzbereich nicht erlaubt, es sei
denn es wird durch eine im Konnektor integrierte Signaturrichtlinie explizit
gefordert.

Die Spalten mit gelber Kopfzeile definieren die Signaturvarianten, die mit
grauer, den Einsatzbereich. Beim Einsatzbereich wird zwischen nonQES und QES
unterschieden und im Fall QES nach der Bereitstellung an der
Außenschnittstelle oder intern für Fachmodule.

Die benötigten Signaturvarianten werden für XAdES über die Aufrufparameter
IncludeObject und SignaturePlacement gemäß [OASIS-DSS] gesteuert.

Für CAdES erfolgt die Steuerung welche Signaturvariante gewählt wird, über
den Aufrufparameter IncludeEContent. **[\<=]**

##### A_18756

Der Konnektor KANN alle Aufrufe zu Signaturerstellung einer nonQES-XAdES
Signatur mit Fehler 4111 und alle Aufrufe zur Signaturprüfung einer
nonQES-XAdES Signatur mit Fehler 4112 beantworten. Die Signaturvarianten aus
TAB_KON_778 werden damit weiter eingeschränkt. Wird die nonQES-XAdES Signatur
umgesetzt, so ist diese in der Sicherheitszertifizierung zu betrachten.
**[\<=]**

##### TIP1-A_5402

Der Konnektor MUSS von den AdES-Profilen die AdES-EPES-Profile umsetzen,
ergänzt um

 ---> UL

Dabei MUSS der Konnektor die Baseline-Profilierung gemäß Kapitel 6 in [XAdES
Baseline Profile] für XAdES, Kapitel 6 in [CAdES Baseline Profile] für CAdES
und Kapitel 6 in [PAdES Baseline Profile] für PAdES umsetzen. **[\<=]**

Durch die Baseline-Profilierung der AdES-BES-Profile wird festgelegt, wie der
Signaturzeitpunkt, gemessen als Systemzeit des Konnektors, in die Signatur
eingebracht wird.

##### TIP1-A_5403

Der Konnektor SOLL die signierten Dokumente konform zu [COMMON_PKI#Part 3] und
[COMMON_PKI#Part 8] erstellen. **[\<=]**

##### TIP1-A_4624

Bei fehlender expliziter Angabe durch den Aufrufer MUSS der Signaturdienst bei
der Erstellung von nicht-qualifizierten elektronischen Signaturen (nonQES) die
Default-Signaturverfahren entsprechend TAB_KON_583 Default-Signaturverfahren
wählen. **[\<=]**

##### TIP1-A_4628

Bei fehlender expliziter Angabe durch den Aufrufer MUSSder Signaturdienst bei
derErstellung vonqualifizierten elektronischen Signaturen (QES)die
Default-Signaturverfahren entsprechendTAB_KON_583 –
Default-Signaturverfahrenwählen. **[\<=]**

 ---> TABLE

##### TIP1-A_5387

Der Konnektor MUSS auf eine vollständige Nutzung der AdES-Profile erweiterbar
sein. **[\<=]**

##### TIP1-A_5033

Der Konnektor MUSS zur Unterstützung von Missbrauchserkennungen die in Tabelle
TAB_KON_584 gelisteten Operationen als Einträge in EVT_MONITOR_OPERATIONS
berücksichtigen.

Tabelle189: TAB_KON_584 nonQES-Operationen für EVT_MONITOR_OPERATIONS

 ---> TABLE

**[\<=]**

##### TIP1-A_4629

Der Signaturdienst MUSS für die QES-Erstellung die Kartentypen HBA, HBA-qSig
und ZOD_2.0 unterstützen. **[\<=]**

##### TIP1-A_5436

Der Konnektor MUSS die Operation SignDocument für XML-Dokumente so
implementieren, dass das Dokument nach Entfernen der Signatur, insbesondere
auch einer Teilsignatur, als Ganzes unverändert ist, wobei zwei XML-Dokumente
als identisch zu betrachten sind, wenn sie gemäß Canonical XML 1.1 gleich
sind [CanonXML1.1]. **[\<=]**

##### TIP1-A_5682

Der Konnektor MUSS im VerificationReport einer QES-Signaturprüfung ausweisen,
wenn die für die Signatur verwendeten Algorithmen nach dem Algorithmenkatalog
[ALGCAT] als nicht geeignet eingestuft werden. **[\<=]**

##### A_17768

Der Konnektor MUSS bei der Signaturerstellung und Signaturprüfung (QES und
nonQES) die Zertifikate und Schlüssel gemäß den Vorgaben in TAB_KON_900
ermitteln.

Tabelle190: TAB_KON_900 Zertifikate und private Schlüssel für
Signaturerstellung und Signaturprüfung (QES und nonQES)

 ---> TABLE

**[\<=]**

 ---> TABLE

 ---> TABLE

### 4.1.8.1.2 Signaturrichtlinien

Signaturrichtlinien dienen der Profilierung von Signaturerstellung und
-prüfung. Beim Aufruf der Operation SignDocument kann eine URI übergeben
werden, die eine im Konnektor hinterlegte Signaturrichtlinie referenziert. Die
Plattform des Konnektors stellt selbst keine Signaturrichtlinien bereit.
Fachanwendungen, die Signaturrichtlinien erfordern, definieren diese im
Fachmodul des Konnektors. Für XML-Dokumentenformate aus der Menge
vonQES_DocFormatekönnen die nachfolgenden Aspekte über eine
Signaturrichtlinie gekapselt festgelegt werden:

 ---> UL

##### TIP1-A_5538

Der Konnektor MUSS Signaturrichtlinien fürXML-Dokumentenformateausder Menge
vonQES_DocFormatebeidieSignaturerstellung und -prüfungumsetzen.

Der Konnektor MUSS den für jede Signaturrichtlinie definierten Bezeichner (URI)
bei der Signatur als SigPolicyId im Feld SignaturePolicyIdentifier einbetten.
Bei der Signaturprüfung MUSS der Konnektor über eine etwaig vorhandene
SigPolicyId die Signaturrrichtlinie identifizieren.

Die gemäß AdES erforderliche Hash-Referenz über die Policy (SigPolicyHash)
MUSS Schema-konform leer gelassen werden. Bei der Signaturprüfung DARF die
Hash-Referenz über die Policy NICHT geprüft werden. **[\<=]**

### 4.1.8.1.3 Signaturzeitpunkt

Bezogen auf den vom Konnektor für die Signaturprüfung anzunehmenden
Signaturerstellungszeitpunkt werden in dieser Spezifikation die Bezeichner
Ermittelter_Signaturzeitpunkt und Benutzerdefinierter_Zeitpunkt verwendet.

Ermittelter_Signaturzeitpunkt:Vom Konnektor ermittelter Zeitpunkt, zu dem eine
Signatur geprüft wird. Es werden folgende Signaturzeitpunkte ermittelt:

 ---> OL

Anmerkung: Bei vom Konnektor selbst erstellten Signaturen ist immer ein in der
Signatur eingebetteter Zeitpunkt vorhanden, jedoch kein qualifizierter
Zeitstempel, da in der TI keine qualifizierten Zeitstempel ausgestellt
werden. Sollte ein Dokument mit einem qualifizierten Zeitstempel versehen
sein, so wird dieser nicht für die Ermittlung des Signaturzeitpunktes
herangezogen.

Benutzerdefinierter_Zeitpunkt:Vom Benutzer beim Aufruf der
Signaturprüfoperation als Parameter an den Konnektor übergebener Zeitpunkt,
zu dem eine Signatur geprüft werden soll.

### 4.1.8.1.4 Jobnummer

Da die eHealth-Kartenterminals dezentral über eine Netzwerkschnittstelle am
Konnektor betrieben werden, fehlt die Möglichkeit zur direkten physischen und
vom Anwender kontrollierbaren Zuordnung eines solchen Terminals zu einem
Arbeitsplatz, auf dem sich das Clientsystem befindet.

Daher ist es bei einer fehlerhaften Zuordnung eines eHealth-Kartenterminals zu
einem Arbeitsplatz möglich, dass die PIN-Eingabeaufforderung –
beispielsweise zu einem Signaturauftrag – an ein entferntes Kartenterminal
weitergeleitet wird. Diese fehlerhafte Zuordnung kann durch einen Fehler des
Clientsystems oder den Versuch eines Angriffes hervorgerufen werden.

Die Jobnummern werden vom Konnektor erzeugt und können durch Clientsystem
abgerufen werden. Der Konnektor stellt jedoch keine Verbindung zwischen
erzeugten und verwendeten Jobnummern her. Es wird also nicht geprüft, ob nur
Jobnummern verwendet werden, die vorher vom Konnektor erzeugt wurden, oder ob
alle Jobnummern verwendet werden, die vom Konnektor erzeugt wurden.

##### TIP1-A_4639

Um Fehler- und Angriffsmöglichkeiten auszuschließen, MUSS der Konnektor bei
bestimmten PIN-Verifikationen vor der Aufforderung zur PIN-Eingabe an einem
eHealth-Kartenterminal eine hinreichend eindeutige Nummer – die Jobnummer –
generieren, welche den Auftrag kennzeichnet, für dessen Verarbeitung die
PIN-Eingabe erfolgen soll. Bei welchen PIN-Verifikationen dies der Fall ist,
kann den PIN-Prompts in TAB_KON_090 Terminalanzeigen beim Eingeben der PIN am
Kartenterminalentnommen werden. **[\<=]**

##### TIP1-A_4640

Diese Jobnummer MUSS vom Konnektor im Display des eHealth-Kartenterminals neben
der PIN-Eingabeaufforderung angezeigt werden. **[\<=]**

##### TIP1-A_4992-02

Das Handbuch des Konnektors MUSS den Benutzer über den korrekten Gebrauch der
Jobnummer informieren. Es MUSS ihm verdeutlichen, dass er seine PIN über die
Tastatur des eHealth-Kartenterminals nur eingeben darf, wenn am Primärsystem
und am Display des Kartenterminals die gleiche Jobnummer angezeigt wird.
Stimmen die beiden Nummern nicht überein, so soll der Benutzer seine PIN nicht
eingeben und stattdessen weitergehende Schritte zur Klärung des aufgetretenen
Fehlverhaltens einleiten. **[\<=]**

##### TIP1-A_4642

Zur hinreichend eindeutigen Kennzeichnung des Vorganges MUSS eine Jobnummer von
einem Zufallswert abgeleitet sein, wobei die Vorgaben an einen solchen
Zufallswert beachtet werden MÜSSEN[gemSpec_Krypt#2.2]. **[\<=]**

##### TIP1-A_4643

Zur Wahrung der Benutzerfreundlichkeit MUSS eine Reduzierung der Jobnummer auf
eine Länge von sechs Zeichen erfolgen. Diese sechs Zeichen MÜSSEN in zwei
Zeichengruppen mit je drei Zeichen, getrennt durch einen Bindestrich (0x2D),
dargestellt werden. Die erste Zeichengruppe MUSS ausschließlich die Zeichen
"A-Z" beinhalten, die zweite Zeichengruppe MUSS aus Ziffern "0-9" bestehen. Die
Länge der resultierenden, reduzierten Jobnummer ist sieben und wird durch den
Umfang der darstellbaren Zeichen auf dem Display des eHealth-Kartenterminals
beschränkt. **[\<=]**

##### TIP1-A_4644

Der Konnektor MUSS die Eindeutigkeit einer Jobnummer sicherstellen:

 ---> UL

**[\<=]**

##### TIP1-A_4645

Die einzelnen Zeichen der Jobnummer MÜSSEN für die Anzeige am Kartenterminal
gemäß dem Zeichensatz ISO 646DE/DIN66003, bzw. ISO 646 US codiert werden. Aus
diesem Zeichensatz dürfen nur die Zeichen „A-Z“ (0x41 bis 0x5A) und die
Ziffern „0-9“ (0x30 bis 0x39) für die Anzeige der Jobnummer verwendet
werden. **[\<=]**

Beispiele für eine Jobnummer sind ABC-475 und HZF-696.

Die Einbettung der Jobnummer in den Nachrichtentext für den Bildschirm des
Kartenlesers wird in TAB_KON_090 Terminalanzeigen beim Eingeben der PIN am
Kartenterminal beschrieben.

### 4.1.8.1.5 Komfortsignatur

Für die QES unterstützt der Konnektor die Komfortsignaturfunktion. In diesem
Modus können für ein- und denselben HBA mehrere vom Clientsystem initiierte
Signaturaufträge (Einzel- oder Stapelsignatur) abgearbeitet werden, ohne dass
der Inhaber des HBA für jeden einzelnen dieser Signaturaufträge die PIN.QES
am Kartenterminal eingegeben muss.

Im Auslieferungszustand ist die Komfortsignaturfunktion ausgeschaltet
(SAK_COMFORT_SIGNATURE = Disabled), d. h. mit dem Konnektor können zunächst
keine Komfortsignaturen durchgeführt werden. Die Komfortsignaturfunktion kann
vom Administrator eingeschaltet werden. Dies ist nur möglich, wenn an der
Clientsystemschnittstelle des Konnektors verpflichtend TLS mit
Clientauthentisierung (Konfigurationsvariante SOAP1 und SOAP2 in TAB_KON_852)
konfiguriert ist. Das Einschalten der Komfortsignaturfunktion im Konnektor hat
zur Folge, dass alle Operationen an der Clientsystemschnittstelle nur über TLS
mit Clientauthentisierung angesprochen werden können (außer ggf.
Dienstverzeichnisdienst).

Bei eingeschalteter Komfortsignaturfunktion können potentiell alle HBAs in der
Umgebung, in der der Konnektor eingesetzt ist, Komfortsignaturen durchführen.
Die eigentliche Aktivierung der Komfortsignatur muss separat für jede einzelne
HBA-CardSession erfolgen.

Durch Aufruf der Operation ActivateComfortSignature des Konnektors durch das
Primärsystem wird die Nutzung der Komfortsignatur für eine HBA-CardSession
(Komfortsignaturmodus) aktiviert. Dazu muss der HBA-Inhaber diePIN.QESeingeben.

Der Konnektor merkt sich für die Cardsession des HBA, dass die Komfortsignatur
aktiviert wurde. Bei den folgenden Aufrufen vonSignDocumentwerden dann
Komfortsignaturen ausgeführt, solange bis eines der folgenden Abbruchkriterien
eintritt:

·      Die vom HBA (entsprechend Personalisierung) oder die vom Konnektor
(entsprechend KonfigurationSAK_COMFORT_SIGNATURE_MAX) durchgesetzte maximale
Anzahl von Signaturen wurde erreicht.

·      Das konfigurierte Zeitintervall für die Komfortsignatur
(entsprechend KonfigurationSAK_COMFORT_SIGNATURE_TIMER) ist für die
Cardsession abgelaufen.

·      Der Komfortsignaturmodus wurde für die betroffene Cardsession
deaktiviert.

·      Der HBA wurde gezogen.

·      Der Sicherheitszustand des HBA wurde zurückgesetzt.

·      Die Komfortsignaturfunktion wurde für den Konnektor durch den
Administrator deaktiviert.

##### A_19945

Der Signaturdienst MUSS bei der Komfortsignatur die Signaturvarianten für die
QES gemäß TAB_KON_778 unterstützen. **[\<=]**

##### A_18597

Bei der Komfortsignatur DARF der Konnektor den Sicherheitszustand
derPIN.QES NICHT selbsttätig zurücksetzen, außer wenn dies explizit
spezifikatorisch gefordert wird. **[\<=]**

A_18597 kann z. B. umgesetzt werden, indem

·       ein dedizierter logischer Kanal des HBA für die Komfortsignatur
verwendet wird und

·      im dedizierten logischen Kanal des HBA die Selektion
vonDF.QESsolange beibehalten wird, bis ein Verlassen vonDF.QESdurch die
Spezifikation explizit gefordert wird.

##### A_18686-01

Der Konnektor MUSS für jede HBA-Kartensitzung mit eingeschalteter
Komfortsignatur einen Komfortsignatur-Timer gemäß konfiguriertem
ZeitintervallSAK_COMFORT_SIGNATURE_TIMER einrichten.  
Der Konnektor DARF nach
Erreichen des Maximalwerts des Timers NICHT weitere Signaturaufträge annehmen.
 
Der Konnektor MUSS den Sicherheitszustand des HBA nach Erreichen des
Maximalwertes des Timers zurücksetzen, nachdem Signaturaufträge, die bis zu
diesem Zeitpunkt bereits zur Bearbeitung angenommen wurden, vollständig
abgearbeitet wurden. **[\<=]**

##### A_19100-01

Der Konnektor MUSS für jede HBA-Kartensitzung mit eingeschalteter
Komfortsignatur die an die Karte gesendeten Signaturaufträge zählen und nach
Erreichen von SAK_COMFORT_SIGNATURE_MAX den Sicherheitszustand des HBA
zurücksetzen. **[\<=]**

##### A_19258

Bei der Komfortsignatur MUSS der Signaturdienst die zu signierenden Daten (DTBS)
über Secure Messaging vom Konnektor zum HBA übertragen. Dieser Secure
Messaging-Kanal MUSS über die gSMC-K zum HBA mittels C.SAK.AUTD_CVC aufgebaut
werden. **[\<=]**

##### A_20073-01

Der Konnektor MUSS die beim Aktivieren des Komfortsignaturmodus vom PS
übermittelte UserId für die Kartensitzung des HBA, für den der Modus
aktiviert wird, auf die ausreichende Länge von 128 Bit im Format einer UUID
nach RFC4122 prüfen und die Aktivierung mit Fehler 4272 ablehnen, wenn die
UserId nicht ausreichend lang ist. **[\<=]**

##### A_20074

Der Konnektor MUSS die Eindeutigkeit der UserId sicherstellen. Wird die
Operation ActivateComfortSignature mit einer UserId im Aufrufkontext
aufgerufen, die innerhalb der vorangegangenen 1.000 Vorgänge bereits verwendet
wurde, so MUSS der Konnektor die Bearbeitung mit dem Fehler 4270 abbrechen. Die
Zählung der Aufrufe erfolgt dabei unabhängig vom Aufrufkontext. **[\<=]**

##### A_19101

Das Handbuch des Konnektors MUSS einen Hinweis enthalten, dass die
Authentifizierung des HBA-Inhabers für die Komfortsignatur vom Clientsystem
vorgenommen wird und dass die Authentifizierung des Nutzers am Clientsystem
einen unverzichtbaren Beitrag zur Sicherheit der Lösung leistet. **[\<=]**

##### A_22344

Der Konnektor MUSS mindestens zwei parallele Komfortsignatursessions für ein-
und denselben HBA unterstützen. **[\<=]**

Es kann davon ausgegangen werden, dass in den Einsatzumgebungen des Konnektors
fachlicher Bedarf an mehr als zwei parallelen Komfortsignatursessions
besteht. Daher wird empfohlen, mehr als zwei Sessions zu unterstützen.

Um pro Session die maximal erlaubte Anzahl von Signaturen
(SAK_COMFORT_SIGNATURE_MAX) ausschöpfen zu können, sollen für parallele
Komfortsignatursessions nach Möglichkeit mehrere logische Kanäle des
HBA verwendet werden.

Der Konnektor soll sich robust verhalten, wenn zu einem HBA Signaturaufträge
von unterschiedlichen Clientsystemen aus eintreffen, während vorherige
Signaturaufträge noch nicht vollständig abgearbeitet sind. Nach Möglichkeit
sollen gleichzeitig eintreffende Signaturaufträge angenommen und abgearbeitet
werden.

##### A_22352

Der Konnektor SOLL die Komfortsignatur-Timer paralleler Komfortsignatursessions
für ein- und denselben HBA so umsetzen, dass diese unabhängig voneinander
wirken. **[\<=]**

##### A_22459

Der Konnektor SOLL die Komfortsignatur-Zähler paralleler
Komfortsignatursessions für ein- und denselben HBA so umsetzen, dass diese
unter Berücksichtigung der Limitierungen der Karte unabhängig voneinander
wirken. **[\<=]**

### 4.1.8.2 Durch Ereignisse ausgelöste Reaktionen

keine

### 4.1.8.3 Interne TUCs, nicht durch Fachmodule nutzbar

Abbildung PIC_KON_103 Use Case Diagramm Signaturdienst (nonQES) beschreibt die
Aufrufbeziehungen der nonQES-TUCs des Signaturdienstes. Die TUCs des
Signaturdienstes sind weiß dargestellt. Genutzte TUCs anderer Basisdienste
sind grau hinterlegt.

![Abbildung-15][Abbildung-15]

Abbildung PIC_KON_104 Use Case Diagramm Signaturdienst (QES) beschreibt die
Aufrufbeziehungen der QES-TUCs des Signaturdienstes.

![Abbildung-16][Abbildung-16]

Abbildung PIC_KON_102 Use Case Diagramm Signaturdienst (Komfortsignatur)
beschreibt die Aufrufbeziehungen der TUCs des Signaturdienstes für die
Komfortsignatur.

![Abbildung-17][Abbildung-17]

### 4.1.8.3.1 TUC_KON_155 „Dokumente zur Signatur vorbereiten”

##### TIP1-A_4646-04

Der Konnektor MUSS den technischen Use Case TUC_KON_155 „Dokumente zur
Signatur vorbereiten” umsetzen.

Tabelle193: TAB_KON_748 - TUC_KON_155 „Dokumente zur Signatur vorbereiten“

 ---> TABLE

Tabelle194: TAB_KON_586 Fehlercodes TUC_KON_155 „Dokumente zur Signatur
vorbereiten“

 ---> TABLE

**[\<=]**

### 4.1.8.3.2 TUC_KON_165 „Signaturvoraussetzungen für nonQES prüfen“

##### TIP1-A_4647-02

Der Konnektor MUSS den technischen Use Case „Signaturvoraussetzungen für
nonQES prüfen” umsetzen.

Tabelle195: TAB_KON_749 – TUC_KON_165 „Signaturvoraussetzungen für nonQES
prüfen“

 ---> TABLE

Tabelle196: TAB_KON_587 Fehlercodes TUC_KON_165 „Signaturvoraussetzungen für
nonQES prüfen“

 ---> TABLE

**[\<=]**

### 4.1.8.3.3 TUC_KON_166 „nonQES Signaturen erstellen“

##### TIP1-A_4648

Der Konnektor MUSS den technischen Use Case TUC_KON_166 „nonQES Signaturen
erstellen” umsetzen.

Tabelle197: TAB_KON_750 – TUC_KON_166 „nonQES Signaturen erstellen“

 ---> TABLE

Tabelle198: TAB_KON_120 Fehlercodes TUC_KON_166 „nonQES Signaturen erstellen“

 ---> TABLE

**[\<=]**

### 4.1.8.3.4 TUC_KON_152 "Signaturvoraussetzungen für QES prüfen"

##### TIP1-A_4649

Der Konnektor MUSS den technischen Use Case TUC_KON_152
„Signaturvoraussetzungen für QES prüfen” umsetzen.

Tabelle199: TAB_KON_751 – TUC_KON_152 „Signaturvoraussetzungen für QES
prüfen“

 ---> TABLE

Tabelle200: TAB_KON_588 Fehlercodes TUC_KON_152 „Signaturvoraussetzungen für
QES prüfen“

 ---> TABLE

**[\<=]**

### 4.1.8.3.5 TUC_KON_154 "QES Signaturen erstellen"

Der TUC_KON_154 stellt den Standardsignaturfall in der TI, die Stapelsignatur
dar (auch für Stapel der Größe 1). Da die Stapelsignatur auf der Zielkarte
passende CVC voraussetzt, die auf den HBA-Vorläuferkarten nicht vorhanden
sind, kann dieser TUC nur den HBA unterstützen. Für HBA-Vorläuferkarten kann
TUC_KON_168 verwendet werden.

##### TIP1-A_4651-02

Der Konnektor MUSS den technischen Use Case TUC_KON_154 „QES Signaturen
erstellen” umsetzen.

Tabelle201: TAB_KON_752 – TUC_KON_154 „QES Signaturen erstellen"

 ---> TABLE

![Img-018][Img-018]

Abbildung18: PIC_KON_113 Aktivitätsdiagramm zu „QES Signaturen erstellen“

Tabelle202: TAB_KON_126 Fehlercodes TUC_KON_154 „QES Signaturen erstellen“

 ---> TABLE

**[\<=]**

### 4.1.8.3.6 TUC_KON_168 „Einzelsignatur QES erstellen“

##### TIP1-A_4652-02

Der Konnektor MUSS den technischen Use Case TUC_KON_168 „Einzelsignatur QES
erstellen“ umsetzen.

Tabelle203: TAB_KON_293 - TUC_KON_168 „Einzelsignatur QES erstellen“

 ---> TABLE

Tabelle204: TAB_KON_590 Fehlercodes TUC_KON_168 „Einzelsignatur QES
erstellen“

 ---> TABLE

**[\<=]**

### 4.1.8.3.7 TUC_KON_158 "Komfortsignaturen erstellen"

Der TUC_KON_158 führt die Komfortsignatur für ein Dokument oder mehrere
Dokumente eines Stapels aus. Da die Komfortsignatur auf der Zielkarte passende
CVC voraussetzt, die auf den HBA-Vorläuferkarten nicht vorhanden sind,
unterstützt dieser TUC nur den HBA.

##### A_19102-04

Der Konnektor MUSS den technischen Use Case TUC_KON_158 „Komfortsignaturen
erstellen” umsetzen.

Tabelle205: TAB_KON_870 – TUC_KON_158 „Komfortsignaturen erstellen"

 ---> TABLE

Tabelle206: TAB_KON_873 Fehlercodes TUC_KON_158 „Komfortsignaturen erstellen“

 ---> TABLE

**[\<=]**

### 4.1.8.4 Interne TUCs, auch durch Fachmodule nutzbar

##### A_20478

Der Konnektor KANN für die nonQES-Signaturerstellung an der Schnittstelle zu
Fachmodulen zusätzliche Dokumentformate unterstützen. **[\<=]**

Die in der obigen Anforderung benannten Signaturen von Dokumentenformaten
umfassen beispielsweise die Signatur von Token nach SAML2 für das Fachmodul
ePA entsprechend [gemSpec_FM_ePA#A_14927].

### 4.1.8.4.1 TUC_KON_160 „Dokumente nonQES signieren”

##### TIP1-A_4653

Der Konnektor MUSS den technischen Use Case TUC_KON_160 „Dokumente nonQES
signieren” umsetzen.

Tabelle207: TAB_KON_753 – TUC_KON_160 „Dokumente nonQES signieren“

 ---> TABLE

Tabelle208: TAB_KON_127 Fehlercodes TUC_KON_160 „Dokumente nonQES signieren“

 ---> TABLE

**[\<=]**

##### TIP1-A_4653-02

Der Konnektor MUSS den technischen Use Case TUC_KON_160 „Dokumente nonQES
signieren” umsetzen.

Tabelle209: TAB_KON_753 – TUC_KON_160 „Dokumente nonQES signieren“

 ---> TABLE

Tabelle210: TAB_KON_127 Fehlercodes TUC_KON_160 „Dokumente nonQES signieren“

 ---> TABLE

Die zulässigen Zertifikate und Schlüssel sind in TAB_KON_900 aufgelistet. **[\<=]**

### 4.1.8.4.2 TUC_KON_161 „nonQES Dokumentsignatur prüfen”

##### TIP1-A_4654-04

Der Konnektor MUSS den technischen Use Case TUC_KON_161 „nonQES
Dokumentsignatur prüfen” umsetzen.

Tabelle211: TAB_KON_121 - TUC_KON_161 „nonQES Dokumentsignatur prüfen“

 ---> TABLE

Tabelle212: TAB_KON_124 Fehlercodes TUC_KON_161 „nonQES Dokumentensignatur
prüfen“

 ---> TABLE

Das Gesamtergebnis (VerificationResult) für die Prüfung einer
Dokumentensignatur fasst die Ergebnisse aller Prüfungsschritte in einem
einzelnen Statuswert zusammen.

Tabelle213: TAB_KON_754 Übersicht Status für Prüfung einer Dokumentensignatur

 ---> TABLE

Tabelle214: TAB_KON_786 Übersicht unterstützte Zertifikatstyp-OIDs

 ---> TABLE

**[\<=]**

##### TIP1-A_5545

Der Konnektor MUSS zur nonQES-Signaturprüfung ein Prüfergebnis das sich auf
genau einen angenommenen Signaturzeitpunkt bezieht, an den Aufrufer
zurückgeben.Die Auswahl des angenommenen Signaturzeitpunkts, auf den sich das
Signaturergebnis bezieht, erfolgt hierarchisch:

 ---> UL

**[\<=]**

### 4.1.8.4.3 TUC_KON_162 „Kryptographische Prüfung der XML-Dokumentensignatur”

##### TIP1-A_5505

Der Konnektor MUSS den technischen Use Case TUC_KON_162 „Kryptographische
Prüfung der XML-Dokumentensignatur” umsetzen.

Tabelle215: TAB_KON_430 – TUC_KON_162 „Kryptographische Prüfung der
XML-Dokumentensignatur“

 ---> TABLE

Tabelle216: TAB_KON_431 Fehlercodes TUC_KON_162 „Kryptographische Prüfung der
XML-Dokumentensignatur“

 ---> TABLE

**[\<=]**

### 4.1.8.4.4 TUC_KON_150 „Dokumente QES signieren”

##### TIP1-A_4655-02

Der Konnektor MUSS den technischen Use Case TUC_KON_150 „Dokumente QES
signieren” umsetzen.

Tabelle217: TAB_KON_755 – TUC_KON_150 „Dokumente QES signieren“

 ---> TABLE

![Img-019][Img-019]

Abbildung19: PIC_KON_114 Aktivitätsdiagramm zu „Dokument QES signieren“

Tabelle218: TAB_KON_128 Fehlercodes TUC_KON_150 „Dokument QES signieren“

 ---> TABLE

**[\<=]**

### 4.1.8.4.5 Anforderungen an die Stapelsignatur

Eine Stapelsignatur definiert sich als „Erstellung einer begrenzten Anzahl
Signaturen nach den zeitlich unmittelbar aufeinander folgenden Prozessen der
Anzeige der zu signierenden Daten und der einmaligen Authentisierung des
Signaturschlüssel-Inhabers gegenüber der qualifizierten elektronischen
Signaturerstellungseinheit“ (siehe [BSI-TR03114]).

##### TIP1-A_4669

Der Signaturdienst MUSS die Möglichkeit bieten, Dokumente eines Stapels einzeln
qualifiziert elektronisch zu signieren. Der Signaturdienst MUSS als
qualifizierte elektronische Signaturerstellungseinheit für die Stapelsignatur
den HBA unterstützen. **[\<=]**

##### TIP1-A_5664

Die zu signierenden Dokumente einer Stapelsignatur MÜSSEN vom Signaturdienst im
Konnektor in derselben Reihenfolge signiert, in der sie im Signaturauftrag vom
Clientsystem geschickt werden. **[\<=]**

##### TIP1-A_4670

Bei der Stapelsignatur MUSS der Signaturdienst die zu signierenden Daten
(DTBS)über Secure Messaging vom Konnektor zum HBA übertragen. Dieser Secure
Messaging-Kanal MUSS über die gSMC-K zum HBA mittels C.SAK.AUTD_CVC aufgebaut
werden. **[\<=]**

##### TIP1-A_4671

Der Signaturdienst MUSS dem Benutzer während und nach einer PIN-Eingabe die
Möglichkeit zum Abbruch einer Stapelsignatur anbieten.Das geforderte Verhalten
des Konnektors beim Abbruch einer Stapelsignatur wird in der folgenden Tabelle
beschrieben. Hierbei werden die beiden Punkte „Abbruch, während die erneute
PIN-Eingabe angefordert wird“ (Nummer 1 bis 4) und „Abbruch, während der
Vorgang der Signaturerstellung läuft“ (Nummer 5 bis 6) unterschieden. Zeile
Nummer 7 beschreibt alle sonstigen Fehlerfälle.Ein Teilstapel einer
Stapelsignatur ist durch die maximale Anzahl der Dokumente definiert, welche
nach der Eingabe der Signatur-PIN durch den Signaturschlüssel-Inhaber signiert
werden kann.

Tabelle219: TAB_KON_192 Verhalten des Konnektors beim Abbruch einer
Stapelsignatur

 ---> TABLE

**[\<=]**

### 4.1.8.4.6 TUC_KON_151 „QES Dokumentensignatur prüfen“

##### TIP1-A_4672-04

Der Konnektor MUSS den technischen Use Case TUC_KON_151
„QES-Dokumentensignatur prüfen” umsetzen.

Tabelle220: TAB_KON_591 - TUC_KON_151 „QES-Dokumentensignatur prüfen“

 ---> TABLE

Tabelle221: TAB_KON_592 Fehlercodes TUC_KON_151 „QES Dokumentensignatur
prüfen“

 ---> TABLE

Das Gesamtergebnis (VerificationResult) für die Prüfung einer
Dokumentensignatur fasst die Ergebnisse

aller Prüfungsschritte in einem einzelnen Statuswert zusammen. 

Tabelle222: TAB_KON_593 Übersicht Status für Prüfung einer Dokumentensignatur

 ---> TABLE

**[\<=]**

##### TIP1-A_5540-01

Der Konnektor MUSS zur QES-Signaturprüfung ein Prüfergebnis, das sich auf
genau einen angenommenen Signaturzeitpunkt bezieht, an den Aufrufer
zurückgeben.  Die Auswahl des angenommenen Signaturzeitpunkts, auf den sich
das Signaturergebnis bezieht, erfolgt hierarchisch:

 ---> UL

**[\<=]**

### 4.1.8.4.7 TUC_KON_170 „Dokumente mit Komfort signieren”

##### A_19103-06

Der Konnektor MUSS den technischen Use Case TUC_KON_170 „Dokumente mit Komfort
signieren” umsetzen.

Tabelle223: TAB_KON_871 – TUC_KON_170 „Dokumente mit Komfort signieren“

 ---> TABLE

Tabelle224: TAB_KON_872 Fehlercodes TUC_KON_170 „Dokumente mit Komfort
signieren“

 ---> TABLE

**[\<=]**

### 4.1.8.4.8 TUC_KON_171 „Komfortsignatur einschalten”

##### A_19104-04

Der Konnektor MUSS den technischen Use Case TUC_KON_171 „Komfortsignatur
einschalten“ umsetzen.

Tabelle225: TAB_KON_883 – TUC_KON_171 „Komfortsignatur einschalten“

 ---> TABLE

Tabelle226: TAB_KON_886 Fehlercodes TUC_KON_171 „Komfortsignatur einschalten“

 ---> TABLE

**[\<=]**

### 4.1.8.4.9 TUC_KON_172 „Komfortsignatur ausschalten”

##### A_19105

Der Konnektor MUSS den technischen Use Case TUC_KON_172 „Komfortsignatur
ausschalten“ umsetzen.

Tabelle227: TAB_KON_884 – TUC_KON_172 „Komfortsignatur ausschalten“

 ---> TABLE

 

Tabelle228: TAB_KON_887 Fehlercodes TUC_KON_172 „Komfortsignatur ausschalten“

 ---> TABLE

**[\<=]**

### 4.1.8.4.10 TUC_KON_173 „Liefere Signaturmodus”

##### A_19106-02

Der Konnektor MUSS den technischen Use Case TUC_KON_173 „Liefere
Signaturmodus“ umsetzen.

Tabelle229: TAB_KON_885 – TUC_KON_173 „Liefere Signaturmodus“

 ---> TABLE

 

Tabelle230: TAB_KON_888 Fehlercodes TUC_KON_173 „Liefere Signaturmodus“

 ---> TABLE

**[\<=]**

### 4.1.8.5 Operationen an der Außenschnittstelle

##### TIP1-A_4676-08

Der Konnektor MUSS Clientsystemen den Basisdienst Signaturdienst (nonQES und
QES) anbieten.

Tabelle231: TAB_KON_197 Basisdienst Signaturdienst (nonQES und QES)

 ---> TABLE

**[\<=]**

### 4.1.8.5.1 SignDocument (nonQES und QES)

##### TIP1-A_5010-09

Der Signaturdienst des Konnektors MUSS an der Clientschnittstelle eine an
[OASIS-DSS] angelehnte Operation SignDocument anbieten.

Tabelle232: TAB_KON_065 Operation SignDocument (nonQES und QES)

 ---> TABLE

Der Ablauf der Operation SignDocument ist in Tabelle TAB_KON_756 Ablauf
Operation SignDocument (nonQES und QES) beschrieben:

Tabelle233: TAB_KON_756 Ablauf Operation SignDocument (nonQES und QES)

 ---> TABLE

Tabelle234: TAB_KON_757 Fehlercodes „SignDocument (nonQES und QES)“

 ---> TABLE

Die zulässigen Zertifikate und Schlüssel sind in TAB_KON_900 aufgelistet. **[\<=]**

### 4.1.8.5.2 VerifyDocument (nonQES und QES)

##### TIP1-A_5034-06

Der Signaturdienst des Konnektors MUSS an der Clientschnittstelle eine an
[OASIS-DSS] angelehnte Operation VerifyDocument (nonQES und QES) anbieten.

Tabelle235: TAB_KON_066 Operation VerifyDocument (nonQES und QES)

 ---> TABLE

Tabelle236: TAB_KON_760 Ablauf Operation VerifyDocument (nonQES und QES)

 ---> TABLE

Tabelle237: TAB_KON_761 Fehlercodes „VerifyDocument (nonQES und QES)“

 ---> TABLE

**[\<=]**

### 4.1.8.5.3 StopSignature

##### TIP1-A_5666-02

Der Signaturdienst des Konnektors MUSS an der Clientschnittstelle eine Operation
StopSignature anbieten.

Tabelle238: TAB_KON_840 Operation StopSignature

 ---> TABLE

Tabelle239: TAB_KON_841 Ablauf Operation StopSignature

 ---> TABLE

Tabelle240: TAB_KON_842 Fehlercodes „StopSignature“

 ---> TABLE

**[\<=]**

### 4.1.8.5.4 GetJobNumber

##### TIP1-A_5667

Der Signaturdienst des Konnektors MUSS an der Clientschnittstelle eine Operation
GetJobNumber anbieten.

Tabelle241: TAB_KON_843 Operation GetJobNumber

 ---> TABLE

Tabelle242: TAB_KON_844 Ablauf Operation GetJobNumber

 ---> TABLE

Tabelle243: TAB_KON_845 Fehlercodes „GetJobNumber“

 ---> TABLE

**[\<=]**

### 4.1.8.5.5 ActivateComfortSignature

##### A_19107

Der Signaturdienst des Konnektors MUSS an der Clientschnittstelle eine Operation
ActivateComfortSignature anbieten.

Tabelle244: TAB_KON_874 ActivateComfortSignature

 ---> TABLE

Tabelle245: TAB_KON_877 Ablauf ActivateComfortSignature

 ---> TABLE

 

Tabelle246: TAB_KON_879 Fehlercodes ActivateComfortSignature

 ---> TABLE

**[\<=]**

### 4.1.8.5.6 DeactivateComfortSignature

##### A_19108

Der Signaturdienst des Konnektors MUSS an der Clientschnittstelle eine Operation
DeactivateComfortSignature anbieten.

Tabelle247: TAB_KON_875 DeactivateComfortSignature

 ---> TABLE

Tabelle248: TAB_KON_878 Ablauf DeactivateComfortSignature

 ---> TABLE

 

Tabelle249: TAB_KON_880 Fehlercodes DeactivateComfortSignature

 ---> TABLE

**[\<=]**

### 4.1.8.5.7 GetSignatureMode

##### A_19109-02

Der Signaturdienst des Konnektors MUSS an der Clientschnittstelle eine Operation
GetSignatureMode anbieten.

Tabelle250: TAB_KON_876 GetSignatureMode

 ---> TABLE

Tabelle251: TAB_KON_882 Ablauf GetSignatureMode

 ---> TABLE

 

Tabelle252: TAB_KON_881 Fehlercodes GetSignatureMode

 ---> TABLE

**[\<=]**

### 4.1.8.6 Betriebsaspekte

##### TIP1-A_4680-03

Die Managementschnittstelle MUSS es einem Administrator ermöglichen
Konfigurationsänderungen gemäß Tabelle TAB_KON_596 vorzunehmen:

Tabelle253: TAB_KON_596 Konfigurationswerte des Signaturdienstes (Administrator)

 ---> TABLE

**[\<=]**

### 4.1.9 Zertifikatsdienst

Der Zertifikatsdienst bietet eine Schnittstelle zur Überprüfung der
Gültigkeit von Zertifikaten an. Dies geschieht auf Grundlage des durch den
Vertrauensanker (TSL-CA-Signer-Zertifikat und eine aktuelle, gültige TSL
aufgespannten Vertrauensraums sowie unter Berücksichtigung von aktuellen
Statusinformationen (OCSP, CRL). Die Zertifikatsprüfung wird sowohl für
nonQES- als auch für QES-Zertifikate unterstützt.

Die für die QES-Zertifikatsprüfung notwendigen QES-Signer-Zertifikate werden
durch die Vertrauensliste der Bundesnetzagentur (BNetzA-VL) bereitgestellt. Das
Signer-Zertifikat der BNetzA-VL ist in der TSL enthalten.

Im Rahmen der ECC-Migration muss der Konnektor neben RSA auch ECC unterstützen.
Hierfür wird eine TSL bereitgestellt, die sowohl die neuen ECC-basierten
Zertifikate als auch aus Rückwärtskompatibilitätsgründen die weiterhin
benötigten RSA-basierten Zertifikate enthält. Diese neue TSL wird auch als
„TSL(ECC-RSA)“ bezeichnet. In dieser Spezifikation wird außerhalb der
Regelungen zur ECC-Migration  nicht zwischen „TSL(ECC-RSA)"
und „TSL(RSA)" unterschieden, da die Anforderungslage keine Unterscheidung
erfordert.

Innerhalb des Zertifikatsdienstes werden folgende Präfixe für Bezeichner
verwendet:

 ---> UL

### 4.1.9.1 Funktionsmerkmalweite Aspekte

Bei der Zertifikatsprüfung wird im Rahmen eines Anwendungsfalls u.a. auch der
Verwendungszweck des Zertifikats geprüft. Der Verwendungszweck
(intendedKeyUsage) wird als Parameter an TUC_KON_037 übergeben. Der konkrete
Wert von intendedKeyUsage ist abhängig vom kryptographischen Verfahren, auf
welchem das Zertifikat basiert. Die Parametrisierung von intendedKeyUsage wird
in TAB_KON_853 in Abhängigkeit vom zu prüfenden Zertifikat, dem
Anwendungsfall und dem kryptographischen Verfahren definiert.

##### A_17295-01

Der Konnektor MUSS bei der Zertifikatsprüfung die intendedKeyUsage in
Abhängigkeit vom zu prüfenden Zertifikat, dem Anwendungsfall und dem
kryptographischen Verfahren gemäßTAB_KON_853prüfen.

Tabelle254: TAB_KON_853- intendedKeyUsage bei Zertifikatsprüfung

 ---> TABLE

**[\<=]**

Bei der Zertifikatsprüfung wird ein übergebenes Zertifikat oder ein Zertifikat
einer referenzierten Karte geprüft. Das konkrete Zertifikatsobjekt einer Karte
ist abhängig vom Kartentyp und dem gewählten kryptographischen Verfahren. Die
folgende Tabelle führt auf, welche Zertifikatsobjekte einer Karte in
Abhängigkeit vom kryptographischen Verfahren für die jeweilige
Zertifikatsreferenz ausgewählt werden.

 ---> TABLE

##### TIP1-A_4682

DerVertrauensankerder TI MUSSzum Auslieferungszeitpunkt des
Konnektorsintegritätsgeschützt im Konnektor hinterlegt sein. Zur
Sicherstellung dieser IntegritätMUSSdie Dateiablage EF.C.TSL.CA_1 der
Anwendung DF.Sicherheitsanker der gSMC-K [gemSpec_gSMC-K_ObjSys#5.7.2]
verwendet werden. **[\<=]**

##### TIP1-A_4684

Falls Parameter MGM_LU_ONLINE=Enabled,MUSS der Zertifikatsdienst einmal täglich
die Aktualisierung der TSL durch Aufruf von TUC_KON_032 „TSL aktualisieren“
durchführen und anschließend TUC_KON_040 „CRL aktualisieren“ aufrufen.
**[\<=]**

##### TIP1-A_4685

Der KonnektorMUSS Spitzenlasten durch paralleles Herunterladen der TSL und der
CRL vermeiden. Dazu MÜSSEN die imEinsatz befindlichen Konnektoren eines
Herstellers ihre Download-Versuche gleichmäßig über den Tag verteilen. **[\<=]**

Dadurch wird gleichzeitig die Spitzenlast bei OCSP-Anfragen begrenzt.

##### A_17572

Falls die TSL(ECC-RSA) verwendet wird, MUSS der Konnektor vor deren
Aktualisierung mit TUC_KON_032 „TSL aktualisieren“ die Hash-Datei der
TSL(ECC-RSA) herunterladen, um zu prüfen, ob die am TSL-Downloadpunkt
verfügbare TSL(ECC-RSA) eine andere ist, als die schon zuvor heruntergeladene
und bereits ausgewertete TSL(ECC-RSA). Entspricht der Hash-Wert am
Download-Punkt der bereits heruntergeladenen und ausgewerteten TSL(ECC-RSA),
MUSS der Konnektor auf den Download verzichten. **[\<=]**

##### A_17661

Der Konnektor MUSS für den Download der Hash-Datei der TSL(ECC-RSA) die
Verbindung zum TSL-Dienst durch TLS absichern. Der Konnektor MUSS das vom
TSL-Dienst beim TLS-Verbindungsaufbau präsentierte Zertifikat C.ZD.TLS-S
prüfen. Die Prüfung erfolgt durch Aufruf von TUC_KON_037 „Zertifikat
prüfen“ {

certificate = C.ZD.TLS-S;

qualifiedCheck = not_required;

offlineAllowNoCheck = true;

policyList  = oid_zd_tls_s;

intendedKeyUsage  = intendedKeyUsage(C.ZD.TLS-S);

intendedExtendedKeyUsage = id-kp-serverAuth;

validationMode  = OCSP } .

Falls Fehler im TLS-Verbindungsaufbau bzw. bei der Zertifikatsprüfung auftreten
MUSS der Konnektor den TLS-Verbindungsaufbau mit Fehlercode 4235 gemäß
TAB_KON_825 abbrechen. **[\<=]**

##### A_17781

Falls im Rahmen der TSL-Aktualisierung beim Download der Hash-Datei der
TSL(ECC-RSA) ein Fehler auftritt MUSS der Konnektor die Aktualisierung der TSL
mit TUC_KON_032 „TSL aktualisieren“ ohne einen ermittelten Hashwert
aufrufen. **[\<=]**

##### TIP1-A_6730

Falls Parameter MGM_LU_ONLINE=Enabled,MUSS der Zertifikatsdienst die
Aktualisierung der BNetzA-VL im
Zeitintervall  CERT_BNETZA_VL_UPDATE_INTERVALdurch Aufruf von TUC_KON_031
„BNetzA-VL aktualisieren“durchführen. **[\<=]**

##### TIP1-A_6731

Der Zertifikatsdienst MUSS einmal täglich die zeitliche Gültigkeitder
BNetzA-VL prüfen. Wenn das Element NextUpdate in der Vergangenheit liegt MUSS
der Konnektor den Betriebszustand EC_ BNetzA_VL_not_valid auslösen. **[\<=]**

##### TIP1-A_6732

Der Konnektor MUSS Spitzenlasten durch Herunterladen der BNetzA-VL vermeiden.
Dazu MÜSSEN die imEinsatz befindlichen Konnektoren den Zeitpunkt für den
Download zufällig wählen unter Beachtung des konfigurierten
ZeitintervallsCERT_BNETZA_VL_UPDATE_INTERVAL. **[\<=]**

##### TIP1-A_5662

Der Konnektor MUSS für den Download der BNetzA-VL und deren Hashwert die
Verbindung zum TSL-Dienst durch TLS absichern. Der Konnektor MUSS  das vom
TSL-Dienst beim TLS-Verbindungsaufbau präsentierte Zertifikat ID.ZD.TLS_S
prüfen. Die Prüfung erfolgt durch Aufruf von TUC_KON_037 „Zertifikat
prüfen“ {

certificate = ID.ZD.TLS_S;

qualifiedCheck = not_required;

offlineAllowNoCheck = true;

policyList  = oid_zd_tls_s;

intendedKeyUsage  = intendedKeyUsage(C.ZD.TLS-S);

intendedExtendedKeyUsage = id-kp-serverAuth;

validationMode  = OCSP } .

Fehler im TLS-Verbindungsaufbau bzw. bei der Zertifikatsprüfung führen zum
Abbruch des TLS-Verbindungsaufbaus mit Fehlercode 4235 gemäß TAB_KON_825.

Tabelle256: TAB_KON_825 Fehlercodes „TLS-Verbindungsaufbau zum TSL-Dienst“

 ---> TABLE

**[\<=]**

##### TIP1-A_5663

Der Konnektor MUSS beim TLS-Verbindungsaufbau zum TSL-Dienst prüfen, dass die
vom TSL-Dienst in ID.ZD.TLS_S übergebene technische Rolle gemäß
[gemSpec_OID#GS-A_4446] dem Wert „oid_tsl_ti“entspricht.

Ein Fehler bei der Prüfung der techischen Rolle führt zum Abbruch des
TLS-Verbindungsaufbaus mit Fehlercode 4236 gemäß TAB_KON_826.

Tabelle257: TAB_KON_826 Fehlercodes„TLS-Verbindungsaufbau zum TSL-Dienst bei
Prüfung der technischen Rolle“

 ---> TABLE

**[\<=]**

##### TIP1-A_4686

Steht der Ablauf der TSL innerhalb von 7 Tagen an, MUSS der Konnektor den
Betriebszustand EC_TSL_Expiring annehmen.

Mit Ablauf der Gültigkeit der TSL MUSS der Konnektor den Betriebszustand
EC_TSL_Out_Of_Date_Within_Grace_Period annehmen.

Mit Ablauf der Graceperiod der TSL MUSS der Konnektor den kritischen
Betriebszustand EC_TSL_Out_Of_Date_Beyond_Grace_Period annehmen. **[\<=]**

##### TIP1-A_4687

Steht der Ablauf der Gültigkeit des TI-Vertrauensankers innerhalb von 30 Tagen
an, MUSS der Konnektor den Betriebszustand EC_TSL_Trust_Anchor_Expiring
annehmen.

Mit Ablauf der Gültigkeit des Vertrauensankers MUSS der Konnektor den
kritischen Betriebszustand EC_TSL_Trust_Anchor_Out_Of_Date annehmen. **[\<=]**

##### TIP1-A_4994

Steht der Ablauf der Gültigkeit der CRL innerhalb von 3 Tagen an, MUSS der
Konnektor den Betriebszustand EC_CRL_Expiringannehmen.

Mit Ablauf der Gültigkeit der CRL MUSS der Konnektor den kritischen
BetriebszustandEC_CRL_Out_Of_Dateannehmen. **[\<=]**

##### TIP1-A_4688

DerKonnektorMUSS alle OCSP-Anfragen über den OCSP-Forwarder (HTTP-Proxy) des
Zugangsdienst-Providers schicken, der durch die Konfigurationswerte
(CERT_OCSP_FORWARDER_ADDRESS, CERT_OCSP_FORWARDER_PORT) festgelegt ist. **[\<=]**

##### TIP1-A_4689

Der Zertifikatsdienst MUSS erhaltene OCSP-Antworten für eine
durchCERT_OCSP_DEFAULT_GRACE_PERIOD_NONQESangegebene Anzahl an Minuten
(nonQES-Zertifikate) zwischenspeichern. **[\<=]**

##### TIP1-A_4690

Bei Ausführung von TUC_PKI_006 „OCSP-Abfrage“ [gemSpec_PKI#8.3.2.2] MÜSSEN
folgende Parameter verwendet werden:OCSP-Graceperiod =
    CERT_OCSP_DEFAULT_GRACE_PERIOD_NONQES

 ---> UL

**[\<=]**

##### TIP1-A_4691

Für die gSMC-K sowie für jede gesteckte Karte außer eGK MUSS der Konnektor im
IntervallCERT_EXPIRATION_CARD_CHECK_DAYSgenau einmal TUC_KON_033 aufrufen.Der
Konnektor MUSS die Gültigkeitsdauer der Zertifikate prüfen mittels Aufruf
von:für gSMC-KTUC_KON_033{checkSMCK; doInformClients=Ja; crypt =
ECC}TUC_KON_033{checkSMCK; doInformClients=Ja; crypt = RSA}für jede
gesteckte G2.0 Karte außer eGK und außer
gSMC-KTUC_KON_033{cardSession; doInformClients=Ja; crypt = RSA}für jede
gesteckte ab G2.1 Karte außer
eGKTUC_KON_033{cardSession; doInformClients=Ja; crypt =
ECC}TUC_KON_033{cardSession; doInformClients=Ja; crypt = RSA} **[\<=]**

##### TIP1-A_4692

Der Konnektor MUSS zur Unterstützung von Missbrauchserkennungen die in Tabelle
TAB_KON_597 gelisteten Operationen als Einträge in EVT_MONITOR_OPERATIONS
berücksichtigen.

Tabelle258: TAB_KON_597 Operationen in EVT_MONITOR_OPERATIONS

 ---> TABLE

**[\<=]**

##### A_23274

Der Konnektor SOLL dem Administrator an der Management-Oberfläche die
Aktualisierung der TSL und CRL per Download ermöglichen. Dabei wird
TUC_KON_032 „TSL aktualisieren“ und anschließend TUC_KON_040 „CRL
aktualisieren“ aufgerufen. **[\<=]**

### 4.1.9.2 Durch Ereignisse ausgelöste Reaktionen

Keine.

### 4.1.9.3 Interne TUCs, nicht durch Fachmodule nutzbar

### 4.1.9.3.1 TUC_KON_032 „TSL aktualisieren“

##### TIP1-A_4693-02

Der Konnektor MUSS den technischen Use Case TUC_KON_032 „TSL aktualisieren“
umsetzen.

Tabelle259: TAB_KON_766 TUC_KON_032 „TSL aktualisieren“

 ---> TABLE

Tabelle260: TAB_KON_598 Fehlercodes TUC_KON_032 „TSL aktualisieren“

 ---> TABLE

**[\<=]**

Für den Download der TSL über einen HTTP-Server im Internet wird zusätzlich
zu der bereits mit einer XML-Signatur versehenen TSL eine detached-Signatur
als separate Datei auf dem Download-Punkt zur Verfügung gestellt. Diese
detached-Signatur umfasst die TSL in ihrerer Gänze, das heißt die
TSL-XML-Datei wird inkl. der dort bereits enthaltenen XML-Signatur nochmal
durch den TSL-Signer signiert. Ein Konnektor verwendet dann bei der
Signaturprüfung einer TSL, die über das Internet bezogen wurde, die
detached-Signatur für die Signaturprüfung. Hintergrund ist die aus
Sicherheitsperspektive einfachere, im Sinne von sicherer prüfbare
detached-Signatur. Das heißt, die TSL muss nicht als XML-File verarbeitet und
die relativ komplexe XML-Signatur - die potentiell von einem Angreifer
modifiziert sein könnte - nicht ausgewertet werden. Deshalb wird der Weg
gewählt, der auch für die Signatur von X.509-Zertifikaten und OCSP-Responses
verwendet wird.

##### A_21185

Der Konnektor MUSS beim Download der TSL aus dem Internet ebenfalls deren
detached-Signatur (vgl. [gemSpec_TSL#A_21182]) mit herunterladen und immer
zunächst folgende Prüfungen durchführen:

 ---> OL

Schlägt eine der Prüfungen fehl, MUSS der Import abgebrochen werden.

Ist die Prüfung erfolgreich, KANN die Prüfung der XML-Signatur der TSL im
weiteren fachlichen Ablauf der TSL-Aktualisierung entfallen. **[\<=]**

Eine erweiterte Übersicht zum Aufbau der detached-Signatur-Datei inkl. Beispiel
finden sie unter [gemGitHub_tslSig].

##### A_20750

Der Hersteller des Konnektors MUSS den Betreiber des Konnektors in geeigneter
Weise (mindestens per Handbuch-Eintrag und per Hinweis innerhalb der
UpdateInformation eines FirmwareUpdates am KSR) darüber informieren, dass im
Fall, dass eine TSL-Aktualisierung innerhalb der TI fehlschlägt, automatisch
versucht wird, eine TSL-Aktualisierung aus dem Internet vorzunehmen. **[\<=]**

### 4.1.9.3.2 TUC_KON_031 „BNetzA-VL aktualisieren“

##### TIP1-A_6729

Der Konnektor MUSS den technischen Use Case TUC_KON_031 „BNetzA-VL
aktualisieren“ umsetzen.

Tabelle261: TAB_KON_618 TUC_KON_031 „BNetzA-VL aktualisieren“

 ---> TABLE

Tabelle262: TAB_KON_619 Fehlercodes TUC_KON_031 „BNetzA-VL aktualisieren“

 ---> TABLE

**[\<=]**

### 4.1.9.3.3 TUC_KON_040 „CRL aktualisieren“

##### TIP1-A_4694

Der Konnektor MUSS den technischen Use Case TUC_KON_040 „CRL aktualisieren“
umsetzen.

Tabelle263: TAB_KON_767 TUC_KON_040 „CRL aktualisieren“

 ---> TABLE

Tabelle264: TAB_KON_599 Fehlercodes TUC_KON_040 „CRL aktualisieren“

 ---> TABLE

**[\<=]**

### 4.1.9.3.4 TUC_KON_033 „Zertifikatsablauf prüfen“

##### TIP1-A_4695

Der Konnektor MUSS den technischen Use Case TUC_KON_033 „Zertifikatsablauf
prüfen” umsetzen.

Tabelle265: TAB_KON_768 TUC_KON_033 „Zertifikatsablauf prüfen“

 ---> TABLE

Tabelle266: TAB_KON_600 Fehlercodes TUC_KON_033 „Zertifikatsablauf prüfen“

 ---> TABLE

**[\<=]**

### 4.1.9.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.1.9.4.1 TUC_KON_037 „Zertifikat prüfen"

##### TIP1-A_4696-02

Der Konnektor MUSS den technischen Use Case „Zertifikat prüfen“ gemäß
TUC_KON_037 „Zertifikat prüfen“ umsetzen.

Tabelle267: TAB_KON_769 TUC_KON_037 „Zertifikat prüfen“

 ---> TABLE

Tabelle268: TAB_KON_601 Fehlercodes TUC_KON_037 „Zertifikat prüfen“

 ---> TABLE

**[\<=]**

### 4.1.9.4.2 TUC_KON_042 „CV-Zertifikat prüfen“

##### TIP1-A_5482-01

Der Konnektor MUSS den technischen Use Case „CV-Zertifikat prüfen“ gemäß
TUC_KON_042 „CV-Zertifikat prüfen“ umsetzen.

Tabelle269: TAB_KON_818 TUC_KON_042 „CV-Zertifikat prüfen“ 

 ---> TABLE

Tabelle270: TAB_KON_819 Fehlercodes TUC_KON_042 „CV-Zertifikat prüfen“

 ---> TABLE

**[\<=]**

### 4.1.9.4.3 TUC_KON_034 „Zertifikatsinformationen extrahieren“

##### TIP1-A_4697

Der Konnektor MUSS den technischen Use Case TUC_KON_034
„Zertifikatsinformationen extrahieren” umsetzen.

Tabelle271: TAB_KON_770 TUC_KON_034 „Zertifikatsinformationen extrahieren“

 ---> TABLE

Tabelle272: TAB_KON_602 Fehlercodes TUC_KON_034 „Zertifikatsinformationen
extrahieren“

 ---> TABLE

**[\<=]**

### 4.1.9.5 Operationen an der Außenschnittstelle

##### TIP1-A_4698-03

Der Konnektor MUSS Clientsystemen eine Basisanwendung Zertifikatsdienst zur
Verfügung stellen

Tabelle273: TAB_KON_771 Basisanwendung Zertifikatsdienst

 ---> TABLE

**[\<=]**

### 4.1.9.5.1 CheckCertificateExpiration

##### TIP1-A_4699-03

Die Basisanwendung Zertifikatsdienst des Konnektors MUSS an der
Clientschnittstelle eine Operation CheckCertificateExpiration anbieten.

Tabelle274: TAB_KON_676 Operation CheckCertificateExpiration

 ---> TABLE

Der Ablauf der Operation CheckCertificateExpiration ist in Tabelle TAB_KON_677
beschrieben:

Tabelle275: TAB_KON_677 Ablauf CheckCertificateExpiration

 ---> TABLE

Tabelle276: TAB_KON_603 Fehlercodes „CheckCertificateExpiration“

 ---> TABLE

**[\<=]**

### 4.1.9.5.2 ReadCardCertificate

##### TIP1-A_4700

Die Basisanwendung Zertifikatsdienst des Konnektors MUSS an der
Clientschnittstelle eine Operation ReadCardCertificate wie in Tabelle
TAB_KON_678 Operation ReadCardCertificate beschrieben anbieten.

Tabelle277: TAB_KON_678 Operation ReadCardCertificate

 ---> TABLE

Der Ablauf der Operation ReadCardCertificate ist in Tabelle TAB_KON_679 Ablauf
ReadCardCertificate beschrieben:

Tabelle278: TAB_KON_679 Ablauf ReadCardCertificate

 ---> TABLE

Tabelle279: TAB_KON_604 Fehlercodes „ReadCardCertificate“

 ---> TABLE

**[\<=]**

### 4.1.9.5.3 VerifyCertificate

##### TIP1-A_5449

Die Basisanwendung Zertifikatsdienst des Konnektors MUSS an der
Clientschnittstelle eine Operation VerifyCertificate wie in Tabelle TAB_KON_795
Operation VerifyCertificate beschrieben anbieten.

Tabelle280: TAB_KON_795 Operation VerifyCertificate

 ---> TABLE

Der Ablauf der Operation VerifyCertificate ist in Tabelle TAB_KON_797 Ablauf
VerifyCertificate beschrieben:

Tabelle281: TAB_KON_797 Ablauf VerifyCertificate

 ---> TABLE

Tabelle282: TAB_KON_800 Fehlercodes „VerifyCertificate“

 ---> TABLE

​​ **[\<=]**

### 4.1.9.6 Betriebsaspekte

### 4.1.9.6.1 TUC_KON_035 „Zertifikatsdienst initialisieren“

##### TIP1-A_4701

In der Bootup-Phase MUSS der Konnektor den Zertifikatsdienst durch Aufruf des
TUC_KON_035 „Zertifikatsdienst initialisieren“ initialisieren.

Tabelle283: TAB_KON_772 TUC_KON_035 „Zertifikatsdienst initialisieren“

 ---> TABLE

Tabelle284: TAB_KON_605 Fehlercodes TUC_KON_035 „Zertifikatsdienst
initialisieren“

 ---> TABLE

**[\<=]**

##### TIP1-A_4702-04

Der Administrator MUSS die in TAB_KON_606 aufgelisteten Parameter über die
Managementschnittstelle konfigurieren und die in TAB_KON_733 aufgelisteten
Parameter ausschließlich einsehen können.

Tabelle285: TAB_KON_606 Konfiguration des Zertifikatsdienstes

 ---> TABLE

Tabelle286: TAB_KON_733 Einsehbare Konfigurationsparameter des
Zertifikatsdienstes

 ---> TABLE

**[\<=]**

##### TIP1-A_4703-01

Das Managementinterface des Konnektors MUSS einem authentisierten Administrator
die Anzeige des Status des Vertrauensraums in Form folgender Daten anbieten:
Sequenznummer der aktuellen TSL, StatusStartingTime (des TSPService
(TSL-Signer-CA-Dienst) zum aktuell gültigen, aktiven TI-Vertrauensanker),
NextUpdate, Gültigkeit der TSL, Typ der TSL (RSA oder ECC-RSA)) sowie optional
für den Administrator einsehbar der Fingerprint des TSL-Signer-Zertifikats.
**[\<=]**

Der Typ der TSL liefert dem Administrator die Information, ob es sich um eine
TSL handelt, die den TI-Vertrauensraum ausschließlich für Zertifikate mit
kryptographischen Verfahren nach RSA-2048 (TSL(RSA)) oder für Zertifikate mit
kryptographischen Verfahren nach RSA-2048 und ECC-256 (TSL(ECC-RSA))
bereitstellt. Die Information kann aus der Signatur der TSL ermittelt werden.

##### TIP1-A_6733

Das Managementinterface des Konnektors MUSS einem authentisierten Administrator
die Anzeige des Status der BNetzA-VL in Form folgender Daten anbieten:
Sequenznummer, NextUpdate, Gültigkeitsstatus und Zeitpunkt der letzten
Prüfung der Aktualität durch TUC_KON_031. **[\<=]**

##### TIP1-A_4704

Der Administrator MUSS einen Prüflauf auf den innerhalb von
CERT_EXPIRATION_WARN_DAYS Tagen bevorstehenden Ablauf von Zertifikaten aller
für den Konnektor erreichbaren Karten (inkl. gSMC-K) an zentraler Stelle in
der Managementschnittstelle auslösen können und das Ergebnis angezeigt
bekommen.Der Konnektor MUSS die Gültigkeitsdauer der Zertifikate aller
gesteckten Karten (inkl. gSMC-K) prüfen mittels Aufruf von:für
gSMC-KTUC_KON_033{checkSMCK; doInformClients=Nein; crypt =
ECC}TUC_KON_033{checkSMCK; doInformClients=Nein; crypt = RSA}für jede
gesteckte G2.0 Karte
außer gSMC-KTUC_KON_033{cardSession; doInformClients=Nein; crypt = RSA}für
jede gesteckte ab G2.1 Karte
außer gSMC-KTUC_KON_033{cardSession; doInformClients=Nein; crypt =
ECC}TUC_KON_033{cardSession; doInformClients=Nein; crypt = RSA} **[\<=]**

##### A_18931

Der Konnektor MUSS dem Administrator die X.509-Zertifikate der verbauten gSMC-Ks
 gemäß TIP1-A_4506 anzeigen. Aus der Anzeige MUSS der
Personalisierungs-Status der X.509-Zertifikate ersichtlich sein (dual RSA- und
ECC-personalisiert oder nur RSA-personalisiert). **[\<=]**

##### TIP1-A_4705

Der Konnektor MUSS es dem Administrator ermöglichen, eine TSL manuell von
lokaler Datenquelle einzuspielen. Dabei MUSS der Konnektor
TUC_KON_032{TSL-Datei} mit der manuell importierten TSL aufrufen.

Der Konnektor MUSS den manuellen Import einer TSL auch ermöglichen, wenn er
sich im kritischen Betriebszustand EC_TSL_Out_Of_Date_Beyond_Grace_Period
befindet.

Der Konnektor MUSS den manuellen Import einer zeitlich abgelaufenen TSL
zulassen.  **[\<=]**

Auch im Fall des automatischen Imports der TSL muss dies im kritischen
BetriebszustandEC_TSL_Out_Of_Date_Beyond_Grace_Periodunterstützt werden.

##### A_20536

Der Konnektor MUSS den automatischen Import einer TSL auch ermöglichen, wenn er
sich im kritischen
BetriebszustandEC_TSL_Out_Of_Date_Beyond_Grace_Periodbefindet.  **[\<=]**

##### A_20748

Falls der Konnektor im kritischen
Betriebszustand EC_TSL_Out_Of_Date_Beyond_Grace_Period ist, und
falls onlineMode = ENABLED ist, MUSS der Konnektor periodisch und in der
BootUp Phase die TSL aktualisieren. **[\<=]**

##### TIP1-A_6728

Der Konnektor MUSS es dem Administrator ermöglichen, die BNetzA-VL manuell von
lokaler Datenquelle einzuspielen. Dabei MUSS der Konnektor
TUC_KON_031{BNetzA-VL-Datei} mit der manuell importierten BNetzA-VL-Datei
aufrufen. **[\<=]**

##### TIP1-A_4706

Der Konnektor SOLL es dem Administrator ermöglichen, eine CRL manuell von einer
lokalen Datenquelle einzuspielen. In dem Fall MUSS der Konnektor
TUC_KON_040{CRL-Datei} mit der manuell importierten CRL aufrufen. **[\<=]**

Für die ECC-Migration ist es notwendig den ECC-RSA-Vertrauensraum zu
etablieren. Dies erfolgt durch das Einspielen eines TSL-Signer-CA
Cross-Zertifikats und das neue TSL-Signer-CA-Zertifikat, wodurch der
ECC-Vertrauensanker im Konnektor im sicheren Datenspeicher gespeichert wird.
Die Prüfung des Cross-Zertifikats erfolgt durch A_17821 - Wechsel des
Vertrauensraumes mittels Cross-Zertifikaten (ECC-Migration). Danach kann die
TSL(ECC-RSA) importiert werden. Das Ergebnis ist ein etablierter
TI-Vertrauensraum für ECC und RSA.Konnektoren müssen den ECC-Vertrauensraum
automatisiert und im Rahmen des Upgrades auf PTV4 etablieren. Manuelle Schritte
durch den Administrator sind für den Regelfall zu vermeiden und sollten nur im
Fehlerfall nötig werden. Als Fallback-Lösung muss das manuelle Verfahren
dennoch unterstützt werden.

##### A_20469-02

In der BootUp-Phase MUSS ein Konnektor, der den RSA-Vertrauensraum (RSA)
verwendet, überprüfen, ob die TSL(ECC-RSA) und die entsprechenden
TSL-Signer-CA Cross-Zertifikate sowie TSL-Signer-CA-Zertifikate verfügbar
sind und MUSS sie im positiven Fall automatisiert herunterladen, nach
erfolgreicher Prüfung verwenden und dadurch den ECC-Vertrauensraum (ECC-RSA)
etablieren.Der Konnektor MUSS hierzu die Downloadpunkte, die mit A_17680-01 in
[gemSpec_TSL#6.3.1.2] definiert sind, verwenden.Falls beim Wechsel auf den 
ECC-RSA Vertrauensraum ein Fehler auftritt, MUSS der Konnektor weiterhin den
RSA-Vertrauensraum (RSA) verwenden. **[\<=]**

##### A_20508-01

Der Konnektor MUSS alle Schritte, die er zur Etablierung des
ECC-RSA-Vertrauensraums durchläuft, im Systemprotokoll des Konnektors mit dem
Log-Level "Warning" protokollieren. **[\<=]**

##### A_17345

Der Konnektor MUSS es dem Administrator ermöglichen, ein TSL-Signer-CA
Cross-Zertifikat und das TSL-Signer-CA-Zertifikat für den neuen
TI-Vertrauensanker manuell von lokaler Datenquelle einzuspielen.    **[\<=]**

##### A_17837-01

Um auf Basis des bereits etablierten Vertrauensankers (RSA) in den
Vertrauensraum (ECC-RSA) zu wechseln MUSS der Konnektor bei der Initialisierung
des neuen Vertrauensankers (ECC-RSA) Cross-Zertifikate verwenden. Das Ergebnis
ist ein neuer etablierter TI-Vertrauensanker (ECC-RSA). **[\<=]**

##### A_17548-01

Der Konnektor MUSS den neuen TI-Vertrauensanker im sicheren Datenspeicher
speichern. **[\<=]**

##### A_17549-01

Der Konnektor MUSS den Import des TSL-Signer-CA Cross-Zertifikats auch
ermöglichen, wenn er sich im kritischen Betriebszustand
EC_TSL_Out_Of_Date_Beyond_Grace_Period befindet.  **[\<=]**

##### A_17550-01

Falls der Import des TSL-Signer-CA Cross-Zertifikats nicht erfolgreich
durchgeführt werden konnte, MUSS der Konnektor den Vorgang abbrechen und einen
Fehler gemäß TAB_KON_857 dem Administrator zur Anzeige bringen und
protokollieren.

Tabelle287: TAB_KON_857 - Fehlercodes beim Import des Cross-Zertifikats für
TI-Vertrauensanker ECC

 ---> TABLE

**[\<=]**

##### TIP1-A_5700

Beim Auftreten des Events NETWORK/VPN_TI/UP MUSS der Konnektor über DNS die
Adressen des http-Forwarders des VPN-Zugangsdienststandortes ermitteln (SRV-RR
mit Bezeichner "_ocsp._tcp.\<DOMAIN_SRVZONE_TI\>). **[\<=]**

##### A_21158

Der Konnektor MUSS mindestens 20 CV-Crosszertifikate verwalten und verarbeiten
können. **[\<=]**

### 4.1.10 Protokollierungsdienst

Der Protokollierungsdienst protokolliert system- und sicherheitsrelevante
Ereignisse, sowie Ereignisse im Kontext der Performancemessung (siehe
[gemSpec_Perf#4.1.2), innerhalb des Konnektors. Auch Ereignisse von Fachmodulen
können protokolliert werden. Im Sicherheitsprotokoll werden alle Ereignisse
eingetragen, die Auswirkungen auf Sicherheitsmerkmale des Konnektors haben
können (Änderungen an der Firewall-Konfiguration, Authentisierungsfehler
etc.). Ereignisse im Kontext der Performancemessung innerhalb des Konnektors
werden in das Konnektor-Performanceprotokoll geschrieben. Ereignisse im Kontext
der Performancemessung von Fachmodulen werden in das
Fachmodul-Performanceprotokoll geschrieben. Alle anderen Ereignisse werden in
das Systemprotokoll oder die Fachmodulprotokolle geschrieben (grundsätzlich
trifft die Entscheidung über den zu verwendenden Protokollspeicher der
Aufrufer des Protokolldienstes).

Die Protokolle werden persistiert.

Hinweis:Ereignisse im Protokollierungsdienst adressieren nicht nur zu
protokollierende Events im Sinne des Systeminformationsdienstes sondern alles,
was zu einem Protokolleintrag führen soll (z.B. Fehler, Informationen zu
Ablauf, Debug, Performance).

Innerhalb des Protokollierungsdienstes werden folgende Präfixe für Bezeichner
verwendet:

 ---> UL

### 4.1.10.1 Funktionsmerkmalweite Aspekte

##### TIP1-A_4708

Der Konnektor MUSS einen Protokollierungsdienst anbieten. Dabei MUSS der
Konnektor zwischen System- und Sicherheitsprotokoll, sowie Fachmodulprotokollen
unterscheiden. Je Fachmodul MUSS ein getrenntes Protokoll vorhanden sein.

Die Protokolleinträge MÜSSEN durch den Konnektor lokal persistiert werden. **[\<=]**

##### TIP1-A_5654

Der Konnektor MUSS herstellerspezifische Fehler, die Auswirkungen auf
Sicherheitsmerkmale des Konnektors haben, in das Sicherheitsprotokoll schreiben. **[\<=]**

##### TIP1-A_4709

Der Konnektor MUSS sicherstellen, dass Einträge in das Sicherheitsprotokoll
nicht von außen und nicht durch den Administrator verändert und gelöscht
werden können. **[\<=]**

##### TIP1-A_4710

Der Konnektor DARF medizinische Daten NICHT in die Protokolldateien
schreiben.Personenbezogene Daten DÜRFEN NICHT in Protokolleinträgen
gespeichert werden.KVNR, ICCSN und CardHolderName MÜSSEN als personenbezogene
Daten behandelt werden.Die ICCSN DARF Im Fehlerfall durch Fachmodule in
Protokolleinträgen gespeichert werden. Die ICCSN DARF NICHT im
Sicherheitsprotokoll gespeichert werden. **[\<=]**

##### TIP1-A_6479

Der Konnektor DARF vertrauliche Daten NICHT in die Protokolldateien schreiben. **[\<=]**

##### TIP1-A_4711

Der Konnektor MUSS über eine Speichergröße für
Protokolldateienverfügen,sodass Einträge (protokollierte Ereignisse ab der
Schwere „Warning“) über einen Zeitraum von bis zu einem Jahr darin
vorgehalten werden können. **[\<=]**

Da sich die Menge an Einträgen nach der Größe der Einsatzumgebung richtet,
ist die Speichergröße nach den in [gemSpec_Perf#3.1.1] beschriebenen
Einsatzumgebungen (LE-Ux, x=1,2,3,4) ausreichend zu wählen.

##### TIP1-A_4712

WennLOG_SUCCESSFUL_CRYPTO_OPS= Enabled MUSS der Konnektor die folgenden
erfolgreich durchlaufenen Außenoperationen protokollieren: - SignDocument, -
VerifyDocument, - ExternalAuthenticate, - EncryptDocument, -
DecryptDocument.Dazu MUSS erTUC_KON_256 {     topic =
„LOG/CRYPTO_OP“;     eventType = Sec;     severity = Info;    
parameters =
(„Operation=$Operationsname,                          
\<für alle betroffenen
Schlüssel:\>                                
Karte=$ICCSN,                                
Keyref=\<Referenz auf den
Schlüssel\>,                                
CARD_HANDLE=$CardHandle,                                
CardHolderName=$CardHolderName“);                                
doDisp = false}aufrufen. **[\<=]**

##### TIP1-A_4713

WennLOG_LEVEL_SYSLOG= Info MUSS der Konnektor herstellerspezifische
Informationen über den laufenden Betrieb in das Systemprotokoll eintragen, um
im Bedarfsfall das Verhalten des Konnektors analysieren zu können
(Unterstützung der Fehlersuche etc.).

Die Häufigkeit und der Inhalt der protokollierten Informationen sind
herstellerspezifisch. **[\<=]**

##### TIP1-A_4714

Der Konnektor MUSS Protokolleinträge so anlegen, dass eine Analyse der
Einträge unterstützt wird:

 ---> UL

**[\<=]**

### 4.1.10.2 Durch Ereignisse ausgelöste Reaktionen

Keine.

### 4.1.10.3 Interne TUCs, nicht durch Fachmodule nutzbar

Keine.

### 4.1.10.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.1.10.4.1 TUC_KON_271 „Schreibe Protokolleintrag“

##### TIP1-A_4715

Der Konnektor MUSS den technischen Use Case TUC_KON_271 „Schreibe
Protokolleintrag” umsetzen.

Tabelle288: TAB_KON_607 – TUC_KON_271 „Schreibe Protokolleintrag“

 ---> TABLE

Tabelle289: TAB_KON_608 Fehlercodes TUC_KON_271 „Schreibe Protokolleintrag“

 ---> TABLE

**[\<=]**

Die Darstellung PIC_KON_118 veranschaulicht den Aufbau der Protokolle für
Plattform und Fachmodule und die Steuerung der Protokolleinträge in
TUC_KON_271 „Schreibe Protokolleintrag“.

![Abbildung-20][Abbildung-20]

### 4.1.10.5 Operationen an der Außenschnittstelle

Keine

### 4.1.10.6 Betriebsaspekte

##### TIP1-A_4716

Der Administrator MUSS die durch den Protokollierungsdienst geschriebenen
Protokolle über die Managementschnittstelle einsehen können.

Eine Veränderung des Sicherheitsprotokolls DARF für den Administrator NICHT
möglich sein.

Das Löschen folgender Protokolle MUSS für den Administrator möglich sein:

 ---> UL

Der Konnektor MUSS den Export von Protokolleinträgen oder ganzen
Protokolldateien unterstützen.

Der Konnektor SOLL das Sortieren und Filtern der Protokolleinträge sowie das
Suchen in den Protokolleinträgen unterstützen. **[\<=]**

##### TIP1-A_4996

Nachdem sich der Administrator an der Managementschnittstelle angemeldet hat,
MUSS der Konnektor ihn automatisch auf Sicherheitsprotokolleinträge hinweisen,
die seit dem Ausloggen dieses Administrator aufgelaufen sind. **[\<=]**

##### TIP1-A_4717

Die Managementschnittstelle MUSS es einem Administrator ermöglichen
Konfigurationsänderungen gemäß Tabelle TAB_KON_609 vorzunehmen:

Tabelle290: TAB_KON_609 Konfigurationswerte des Protokollierungsdienstes
(Administrator)

 ---> TABLE

**[\<=]**

### 4.1.10.6.1 TUC_KON_272 „Initialisierung Protokollierungsdienst

##### TIP1-A_4718

Der Konnektor MUSS den technischen Use Case TUC_KON_272 „Initialisierung
Protokollierungsdienst” umsetzen.

Tabelle291: TAB_KON_610 – TUC_KON_272 „Initialisierung
Protokollierungsdienst“

 ---> TABLE

Tabelle292: TAB_KON_611 Fehlercodes TUC_KON_272 „Initialisiere
Protokollierungsdienst“

 ---> TABLE

**[\<=]**

### 4.1.11 TLS-Dienst

Fachmodule müssen gesicherte Verbindungen zu Fachdiensten in der TI aufbauen
können. Dabei sollen sie sich mit einer Organisationsidentität (einer SM-B)
authentisieren können. Der TLS-Dienst stellt hierfür TUCs für einen
TLS-Verbindungsaufbau und -Verbindungsabbau zur Verfügung. Die gesicherte
Kommunikation selbst erfolgt dann durch das Fachmodul unter Nutzung der
etablierten Verbindung.

Die Funktionalität steht nur zur Verfügung, wenn MGM_LU_ONLINE aktiv ist
(siehe Kapitel 4.3.6)

### 4.1.11.1 Funktionsmerkmalweite Aspekte

### 4.1.11.2 Durch Ereignisse ausgelöste Reaktionen

##### TIP1-A_4719

Tritt das Ereignis „MGM/LU_CHANGED/LU_ONLINE“ ein, so MUSS

 ---> UL

**[\<=]**

### 4.1.11.3 Interne TUCs, nicht durch Fachmodule nutzbar

Keine.

### 4.1.11.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.1.11.4.1 TUC_KON_110 „Kartenbasierte TLS-Verbindung aufbauen“

##### TIP1-A_4720-02

Der Konnektor MUSS den technischen Use Case "Kartenbasierte TLS-Verbindung
aufbauen" gemäß TUC_KON_110 umsetzen.

Tabelle293: TAB_KON_773 – TUC_KON_110 „Kartenbasierte TLS-Verbindung
aufbauen“

 ---> TABLE

Tabelle294: TAB_KON_612 Fehlercodes TUC_KON_110 „Kartenbasierte TLS-Verbindung
aufbauen“

 ---> TABLE

**[\<=]**

### 4.1.11.4.2 TUC_KON_111 „Kartenbasierte TLS-Verbindung abbauen“

##### TIP1-A_4721

Der Konnektor MUSS den technischen Use Case "Kartenbasierte TLS-Verbindung
abbauen" gemäß TUC_KON_111 umsetzen.

Tabelle295: TAB_KON_774 - TUC_KON_111 „Kartenbasierte TLS-Verbindung abbauen“

 ---> TABLE

Tabelle296: TAB_KON_613 Fehlercodes TUC_KON_111 „Kartenbasierte TLS-Verbindung
abbauen“

 ---> TABLE

**[\<=]**

### 4.1.11.5 Operationen an der Außenschnittstelle

Keine.

### 4.1.11.6 Betriebsaspekte

##### TIP1-A_4722

Wenn MGM_LU_ONLINE =„Enabled“, MUSS der Basisdienst TLS-Dienst nach dem
Bootup zur Nutzung zur Verfügung stehen.

Wenn MGM_LU_ONLINE =„Disabled“, DARF der Basisdienst TLS-Dienst nach dem
Bootup NICHT zur Nutzung zur Verfügung stehen. **[\<=]**

### 4.1.12 LDAP-Proxy

Der Konnektor ermöglicht es Clientsystemen und Fachmodulen durch Nutzung des
LDAP-Proxies Daten aus dem Verzeichnisdienst der TI-Plattform (VZD) abzufragen.
Die Kommunikation erfolgt über das LDAPv3 Protokoll.

Die Funktionalität steht nur zur Verfügung, wenn MGM_LU_ONLINE=Enabled ist
(siehe Kapitel 4.3.6)

### 4.1.12.1 Funktionsmerkmalweite Aspekte

Keine.

### 4.1.12.2 Durch Ereignisse ausgelöste Reaktionen

##### TIP1-A_5516

Tritt das Ereignis „MGM/LU_CHANGED/LU_ONLINE“ ein, so MUSS

 ---> UL

**[\<=]**

### 4.1.12.3 Interne TUCs, nicht durch Fachmodule nutzbar

Keine.

### 4.1.12.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.1.12.4.1 TUC_KON_290 „LDAP-Verbindung aufbauen“

##### TIP1-A_5517-02

Der Konnektor MUSS den technischen Use Case TUC_KON_290 „LDAP-Verbindung
aufbauen“ gemäß TAB_KON_805 umsetzen.

Tabelle297: TAB_KON_805 - TUC_KON_290 „LDAP-Verbindung aufbauen“

 ---> TABLE

**[\<=]**

### 4.1.12.4.2 TUC_KON_291 „Verzeichnis abfragen“

##### TIP1-A_5518

Der Konnektor MUSS den technischen Use Case TUC_KON_291 „Verzeichnis
abfragen“ gemäß TAB_KON_815 umsetzen.

Tabelle298: TAB_KON_815 – TUC_KON_291 „Verzeichnis abfragen“

 ---> TABLE

**[\<=]**

### 4.1.12.4.3 TUC_KON_292 „LDAP-Verbindung trennen"

##### TIP1-A_5519

Der Konnektor MUSS den technischen Use Case „LDAP-Verbindung trennen" gemäß
TAB_KON_816 umsetzen.

Tabelle299: TAB_KON_816 – TUC_KON_292 „LDAP-Verbindung trennen"

 ---> TABLE

**[\<=]**

### 4.1.12.4.4 TUC_KON_293 „Verzeichnisabfrage abbrechen"

##### TIP1-A_5520

Der Konnektor MUSS den technischen Use Case TUC_KON_293 „Verzeichnisabfrage
abbrechen" gemäß TAB_KON_817 umsetzen.

Tabelle300: TAB_KON_817 – TUC_KON_293 „Verzeichnisabfrage abbrechen“

 ---> TABLE

**[\<=]**

### 4.1.12.5 Operationen an der Außenschnittstelle

### 4.1.12.5.1 Unterstützte LDAPv3 Operationen

##### TIP1-A_5521

Der Konnektor MUSS an der Client-Schnittstelle die folgenden LDAPv3 Operationen
gemäß [RFC4511] anbieten.

 ---> UL

Andere LDAPv3 Operationen werden mit dem LDAP-Fehler unwillingToPerform (53)
beantwort.

Wenn ANCL_TLS_MANDATORY=Enabled, muss der Konnektor sicherstellen, dass nur
über eine LDAPS-Verbindung (Voreinstellung TCP Port 636) Daten abgefragt
werden können.

Wenn ANCL_TLS_MANDATORY=Disabled, muss der Konnektor sicherstellen, dass über
eine LDAP-Verbindung (Voreinstellung TCP Port 389) und über eine
LDAPS-Verbindung (Voreinstellung TCP Port 636) Daten abgefragt werden können.

Fehler müssen gemäß [RFC4511]#Appendix A behandelt werden. **[\<=]**

### 4.1.12.6 Betriebsaspekte

keine

### 4.1.13 Authentifizierungsdienst

Der Authentifizierungsdienst bietet Clientsystemen und Fachmodulen eine
Schnittstelle zum Signieren von Binärstrings zum Zweck der externen
Authentisierung.

Innerhalb des Authentifizierungsdienstes werden folgende Präfixe für
Bezeichner verwendet:

 ---> UL

Eine Prüfung der Signatur bietet der Konnektor nicht an.

### 4.1.13.1 Funktionsmerkmalweite Aspekte

### 4.1.13.1.1 Externe Authentisierung

##### TIP1-A_5437-02

Der Signaturdienst MUSS für die Operation ExternalAuthenticate die
Signaturverfahren entsprechend TAB_KON_780 – Signaturverfahren Externe
Authentisierung unterstützen.

Tabelle301: TAB_KON_780 – Signaturverfahren Externe Authentisierung

 ---> TABLE

     **[\<=]**

##### TIP1-A_5149-01

Der Hersteller des Konnektors MUSS den Anwender (Clientsystem) im Handbuch des
Konnektors geeignet und ausreichend darüber informieren, dass die Operation
ExternalAuthenticate nur zu Authentisierungszwecken mit dem
Authentisierungsschlüssel des HBAx und des SM-B verwendet werden darf.
**[\<=]**

### 4.1.13.2 Durch Ereignisse ausgelöste Reaktionen

keine

### 4.1.13.3 Interne TUCs

keine

### 4.1.13.4 Operationen an der Außenschnittstelle

##### TIP1-A_5665-03

Der Konnektor MUSS Clientsystemen den Basisdienst Authentifizierungsdienst
anbieten.

Tabelle302: TAB_KON_839 Basisdienst Authentifizierungsdienst

 ---> TABLE

**[\<=]**

### 4.1.13.4.1 ExternalAuthenticate

##### TIP1-A_5439

Der Authentifizierungsdienst des Konnektors MUSS an der Clientschnittstelle eine
Operation ExternalAuthenticate anbieten.

Tabelle303: TAB_KON_781 Operation ExternalAuthenticate

 ---> TABLE

Der Ablauf der Operation ExternalAuthenticate ist in Tabelle TAB_KON_782
beschrieben:

Tabelle304: TAB_KON_782 Ablauf Operation ExternalAuthenticate

 ---> TABLE

Tabelle305: TAB_KON_783 Übersicht Fehler Operation ExternalAuthenticate

 ---> TABLE

Die folgende Tabelle führt die zulässigen privaten Schlüssel für die
Operation ExternalAuthenticate auf:

Tabelle306: TAB_KON_784 Privater Schlüssel je Karte für ExternalAuthenticate

 ---> TABLE

**[\<=]**

### 4.1.13.5 Betriebsaspekte

Keine

### 4.1.14 Betriebsdatenmeldedienst

##### A_21136

Der Konnektor MUSS die Operation I_Registration_Service#sendData benutzen, um
die Betriebsdaten täglich zu versenden. **[\<=]**

##### A_21137

Der Konnektor MUSS die Betriebsdaten als XML-Dokument gemäß dem Schema
„conn/OperatingData.xsd“ mit

 ---> UL

senden. **[\<=]**

##### A_21225

Der Konnektor MUSS die XML Elemente der Betriebsdaten gemäß der Annotations im
Schema OperatingData.xsd befüllen. **[\<=]**

##### A_21138

Liefert I_Registration_Service einen Fehler, MUSS der Konnektor das Senden der
Betriebsdaten 3 Mal im Abstand von 5 Minuten erneut versuchen. **[\<=]**

##### A_21139

Meldet I_Registration_Service, dass die Soap Operation sendData nicht vorhanden
ist, DARF der Konnektor die Operation NICHT sofort wiederholen. Erst zum
nächsten regulären Termin soll wieder gesendet werden. **[\<=]**

##### A_21140

Der Konnektor DARF NICHT personenbezogene, personenbeziehbare oder medizinische
Daten senden. **[\<=]**

##### A_23275

Der Konnektor SOLL dem Administrator an der Management-Oberfläche ein manuelles
Versenden der Betriebsdaten ermöglichen. Dabei wird die Operation
I_Registration_Service#sendData aufgerufen. **[\<=]**

### 4.2 Netzkonnektor

### 4.2.1 Anbindung LAN/WAN

Unter Anbindung LAN/WAN werden die Mechanismen beschrieben, mit denen der
Konnektor auf der einen Seite in das lokale Netz der Einsatzumgebung, auf der
anderen Seite in die TI bzw. die Bestandsnetze angebunden wird. Diese
wesentlichen Aspekte betreffen Routing und Firewall.

Innerhalb des Kapitels Anbindung LAN/WAN werden folgende Präfixe für
Bezeichner verwendet:

 ---> UL

### 4.2.1.1 Funktionsmerkmalweite Aspekte

##### TIP1-A_4723

Der Konnektor MUSS sich nach den in [RFC1812#1.1.3] definierten
Rahmenbedingungen als IP Version 4 (IPv4) Router verhalten.Hiervon ausgenommen
sind die in den folgenden Kapiteln aufgeführten Anforderungen des [RFC1812]:

 ---> UL

Die in [RFC2644] geforderten Aktualisierungen zum [RFC1812] müssen vom
Konnektor umgesetzt werden. **[\<=]**

##### TIP1-A_5406

Der Konnektor DARF NICHT IP-Pakete mitgesetzter Source Route Option gemäß
[RFC791] erzeugen oder weiterleiten. **[\<=]**

In der folgenden Anforderung wird die Terminologie gemäß [RFC2663] verwendet.

##### TIP1-A_5407

Der Konnektor MUSS für die Kommunikation aus den Adressbereichen
NET_LEKTR-Umgebung mit den Adressbereichen NET_TI_OFFENE_FD und
ANLW_BESTANDSNETZE eine Network Address Port Translation (NAPT) gemäß
[RFC3022#2.2, 3, 4.1-4.3] vornehmen.Für die Umsetzung der Private Local
Address aus den Adressbereichen der Einsatzumgebung MUSS die IP-Adresse
VPN_TUNNEL_TI_INNER_IP als Global Address genutzt werden.Der Konnektor MUSS
für die Kommunikation aus den Adressbereichen der NET_LEKTR-Umgebung mit dem
Internet über den VPN-Tunnel SIS eine Network Address Port Translation (NAPT)
gemäß RFC3022#2.2, 3, 4.1-4.3 vornehmen. Für die Umsetzung der Local Address
MUSS die IP-Adresse VPN_TUNNEL_SIS_INNER_IP als Global Address genutzt werden.
**[\<=]**

##### TIP1-A_4724

Der Konnektor MUSS sicherstellen, dass nur über den LAN-Adapter (Adressen aus
ANLW_LAN_NETWORK_SEGMENT oder Adressen aus einem der Netzwerksegmente in
ANLW_LEKTR_INTRANET_ROUTES) mit den Clientsystemen und den
Kartenterminalskommuniziert werden kann. **[\<=]**

##### TIP1-A_4725

Für den Betrieb in Reihe (ANLW_ANBINDUNGS_MODUS=InReihe) MUSS der Konnektor den
WAN-Adapter für den Zugang zumInternet über das IAGder
Einsatzumgebungverwenden. **[\<=]**

##### TIP1-A_4726

Der Hersteller des Konnektors MUSS sicherstellen, dass eine Anbindung an das
Transportnetz/Internet nur möglich ist, wenn (MGM_LU_ONLINE=Enabled) gesetzt
ist. **[\<=]**

##### TIP1-A_4728

Der Konnektor MUSS IP Version 4 (IPv4) für alle seine IP-Schnittstellen
unterstützen.Die Hardware des Konnektors MUSS für den Einsatz von IPv4 und
IPv6 im Dual-Stack-Mode geeignet sein.Bis zu einer Migration von IPv4 auf IPv6
MUSS der Konnektor sämtliche empfangene IP-Pakete der Version 6 (IPv6)
verwerfen. **[\<=]**

##### TIP1-A_4728-01

Der Konnektor MUSS IP Version 4 (IPv4) und IP Version 6 (IPv6) für alle seine
physikalischen Adapter unterstützen.Die Hardware des Konnektors MUSS für den
Einsatz von IPv4 und IPv6 im Dual-Stack-Mode geeignet sein. **[\<=]**

##### TIP1-A_4729

Dynamische Routing-Protokolle dürfen vom Konnektor nicht eingesetzt werden.
Wird in einem der an den Konnektor angeschlossenen Netzwerke ein
dynamischesRouting genutzt, so DÜRFEN Routing Updates vom Konnektor NICHT
akzeptiert werden und keine Routen eingetragen werden. **[\<=]**

##### TIP1-A_5152

Falls Parameter MGM_LU_ONLINE=Enabled,MUSS der Konnektor einmal täglich
TUC_KON_283 „Infrastruktur Konfiguration aktualisieren“aufrufen. **[\<=]**

### 4.2.1.1.1 Netzwerksegmentierung

In Anlehnung an die in der [gemSpec_Net#2.3.3] definierten Netzwerksegmente
werden in der Konnektorspezifikation die folgenden Bezeichner verwendet:

 ---> TABLE

 ---> TABLE

 ---> TABLE

### 4.2.1.1.2 Routing und Firewall

Darstellung der Kommunikationsregeln des Konnektors

Diese Abbildung dient der Veranschaulichung der im Konnektor verwendeten
Kommunikationsregeln welche in den nachfolgenden Afo definiert werden.

![Abbildung-21][Abbildung-21]

##### TIP1-A_4730

Der Konnektor MUSS sicherstellen, dass IP-Pakete mit einer Absenderadresse aus
dem Adressbereich NET_TI_GESICHERTE_FD verworfen werden, wenn sie nicht aus dem
VPN-Tunnel der TI (VPN_TI) stammen.Der Konnektor MUSS die Kommunikation mit
Systemen des Netzwerksegments NET_TI_GESICHERTE_FD für folgende Fälle
unterstützen:

 ---> UL

Der Konnektor MUSS insbesondere die Kommunikation an seinen Außenschnittstellen
mit Systemen des Netzwerksegments NET_TI_GESICHERTE_FD für folgende Fälle
blockieren:

 ---> UL

Der Konnektor MUSS sicherstellen, dass die aus einer unterstützten
Kommunikation mit Systemen aus dem Netzwerksegment NET_TI_GESICHERTE_FD
bestimmten IP-Pakete ausschließlich in den VPN-Tunnel der TI (VPN_TI) geleitet
werden. **[\<=]**

##### TIP1-A_5530

Der Konnektor MUSS sicherstellen, dass IP-Pakete mit einer Absenderadresse aus
dem Adressbereich NET_TI_OFFENE_FD verworfen werden, wenn sie nicht aus dem
VPN-Tunnel der TI (VPN_TI) stammen.Der Konnektor MUSS die Kommunikation mit
Systemen des Netzwerksegments NET_TI_OFFENE_FD für folgende Fälle
unterstützen:

 ---> UL

Der Konnektor MUSS insbesondere die Kommunikation an seinen Außenschnittstellen
mit Systemen des Netzwerksegments NET_TI_OFFENE_FD für folgende Fälle
blockieren:

 ---> UL

Der Konnektor MUSS sicherstellen, dass die aus einer unterstützten
Kommunikation mit Systemen aus dem Netzwerksegment NET_TI_OFFENE_FD bestimmten
IP-Pakete ausschließlich in den VPN-Tunnel der TI (VPN_TI) geleitet werden. **[\<=]**

##### TIP1-A_4731

Der Konnektor MUSS sicherstellen, dassIP-Paketemit einer Absenderadresse aus dem
Adressbereich NET_TI_ZENTRAL verworfen werden, wenn sie nicht aus dem
VPN-Tunnel der TI (VPN_TI) stammen.

Der Konnektor MUSS die Kommunikationmit Systemen
desNetzwerksegmentsNET_TI_ZENTRAL für folgende Fälle unterstützen:

 ---> UL

Der Konnektor MUSSinsbesonderedie Kommunikation an seinen
Außenschnittstellenmit Systemen des NetzwerksegmentsNET_TI_ZENTRAL für
folgende Fälle blockieren:

 ---> UL

Der Konnektor MUSS sicherstellen, dass die aus einer unterstützten
Kommunikation mit Systemen aus dem Netzwerksegment NET_TI_ZENTRAL
bestimmtenIP-Paketeausschließlich in den VPN-Tunnel der TI (VPN_TI) geleitet
werden. **[\<=]**

##### TIP1-A_4732

Der Konnektor MUSS sicherstellen, dass die Adressen aus dem Adressbereich
NET_TI_DEZENTRAL nur für die Kommunikation mit der TI/den weiteren Anwendungen
des Gesundheitswesens in Form der inner IP (VPN_TUNNEL_TI_INNER_IP) des
VPN-Tunnel der TI (VPN_TI) verwendet wird.Der Konnektor MUSS die Kommunikation
mit Systemen des Netzwerksegments NET_TI_DEZENTRAL für folgende Fälle
unterstützen:

 ---> UL

Der Konnektor MUSS insbesondere die Kommunikation an seinen Außenschnittstellen
mit Systemen des Netzwerksegments NET_TI_DEZENTRAL für folgende Fälle
blockieren:

 ---> UL

**[\<=]**

##### TIP1-A_4733

Der Konnektor MUSS sicherstellen, dass IP-Pakete mit einer Absenderadresse aus
dem Adressbereich ANLW_AKTIVE_BESTANDSNETZE verworfen werden, wenn sie nicht
aus dem VPN-Tunnel der TI (VPN_TI) stammen.Der Konnektor MUSS die Kommunikation
mit Systemen des Netzwerksegments ANLW_AKTIVE_BESTANDSNETZE für folgende
Fälle unterstützen:

 ---> UL

Der Konnektor MUSS insbesondere die Kommunikation an seinen Außenschnittstellen
mit Systemen des Netzwerksegments ANLW_AKTIVE_BESTANDSNETZE für folgende
Fälle blockieren:

 ---> UL

Der Konnektor MUSS sicherstellen, dass die aus einer unterstützten
Kommunikation mit Systemen aus dem Netzwerksegment ANLW_AKTIVE_BESTANDSNETZE
bestimmten IP-Pakete ausschließlich in den VPN-Tunnel der TI (VPN_TI) geleitet
werden. **[\<=]**

##### TIP1-A_4734

Der Konnektor MUSS sicherstellen, dasseineAdresse aus dem Adressbereich NET_SIS
nur für die Kommunikation mit dem Internet (via SIS) in Form der inner IP
(VPN_TUNNEL_SIS_INNER_IP) des VPN-Tunnel der SIS (VPN_SIS) verwendet wird.

Der Konnektor MUSSinsbesonderedie Kommunikationmit Systemen des
NetzwerksegmentsNET_SIS für folgende Fälle unterstützen:

 ---> UL

Der Konnektor MUSS die Kommunikation an seinen Außenschnittstellen mit NET_SIS
für folgende Fälle blockieren:

 ---> UL

**[\<=]**

##### TIP1-A_4735

Der Konnektor MUSS sicherstellen, dass IP-Pakete mit einer Absenderadresse aus
dem Adressbereich NET_TI_ZENTRAL, NET_TI_GESICHERTE_FD; NET_TI_OFFENE_FD,
NET_TI_DEZENTRAL, ANLW_AKTIVE_BESTANDSNETZE, ANLW_LAN_ADDRESS_SEGMENT, aus
einem der Netzwerksegmente in ANLW_LEKTR_INTRANET_ROUTES oder
ANLW_WAN_NETWORK_SEGMENT verworfen werden, wenn sie aus dem VPN-Tunnel der SIS
(VPN_SIS) stammen.

Der Konnektor MUSS die Kommunikation mit Systemendes NetzwerksegmentsInternet
(via SIS) für folgende Fälle unterstützen:

 ---> UL

Der Konnektor MUSS insbesondere die Kommunikation anseinenAußenschnittstellen
mit Internet (via SIS) für folgende Fälle blockieren oder umleiten:

 ---> UL

Der Konnektor MUSS sicherstellen, dass die für die Kommunikation mit dem
Internet (via SIS) bestimmten IP-Pakete ausschließlich in den VPN-Tunnel des
SIS (VPN_SIS) geleitet werden. **[\<=]**

##### TIP1-A_4736-02

Der Konnektor MUSS sicherstellen, dass eingehende IP-Pakete von der
Kommunikation mit dem Internet mit der Empfängeradresse ungleich
(ANLW_LAN_IP_ADDRESS oder aus einem der Netzwerksegmente in
ANLW_LEKTR_INTRANET_ROUTES wenn ANLW_WAN_ADAPTER_MODUS=DISABLED) oder
(ANLW_WAN_IP_ADDRESS wenn ANLW_WAN_ADAPTER_MODUS=ENABLED) verworfen werden.Der
Konnektor MUSS sicherstellen, dass ausgehende IP-Pakete für die Kommunikation
mit dem Internet mit der Absenderadresse ungleich (ANLW_LAN_IP_ADDRESS oder aus
einem der Netzwerksegmente in ANLW_LEKTR_INTRANET_ROUTES wenn
ANLW_WAN_ADAPTER_MODUS=DISABLED) oder (ANLW_WAN_IP_ADDRESS wenn
ANLW_WAN_ADAPTER_MODUS=ENABLED) verworfen werden.Der Konnektor MUSS die
Kommunikation mit Systemen des Netzwerksegments Internet (via IAG) für
folgende Fälle unterstützen:

 ---> UL

Der Konnektor MUSS insbesondere die Kommunikation an seinen Außenschnittstellen
mit Internet (via IAG) für folgende Fälle blockieren oder umleiten:

 ---> UL

**[\<=]**

##### TIP1-A_4737

Der Konnektor MUSS sicherstellen, dass ausgehendeIP-Paketefür die Kommunikation
mit „AktiveKomponenten“mit einer Absenderadresse ungleich
ANLW_LAN_IP_ADDRESS, einer Adresse aus einem Netzwerksegment
inANLW_LEKTR_INTRANET_ROUTESoder 0.0.0.0 verworfenwerden.

Der Konnektor MUSS die Kommunikation mit „Aktive Komponenten“für folgende
Fälle unterstützen:

 ---> UL

Der Konnektor MUSS insbesondere die Kommunikation anseinen Außenschnittstellen
mit „Aktive Komponenten“für folgende Fälle blockieren:

 ---> UL

**[\<=]**

##### TIP1-A_4738

Der Konnektor MUSS die Kommunikation mit dem IAGder Einsatzumgebungfür folgende
Fälle unterstützen:

 ---> UL

Der Konnektor MUSS insbesondere die Kommunikation an seinen Außenschnittstellen
mit dem IAGder Einsatzumgebungfür folgende Fälle blockieren:

 ---> UL

**[\<=]**

##### TIP1-A_4740

Die Firewall des Konnektor MUSS alle vom Administrator in
ANLW_FW_SIS_ADMIN_RULES definierten Firewall-Regeln als zusätzliche
Einschränkung übernehmen. **[\<=]**

##### TIP1-A_4741

Der KonnektorMUSS die Kommunikation mit Systemen aus einem Intranet-VPN (einem
der Netzwerksegmente ANLW_LEKTR_INTRANET_ROUTES) für folgende
Fälleunterstützen:

 ---> UL

**[\<=]**

##### TIP1-A_4742

Der Konnektor MUSS die Kommunikation mit den Fachmodulen für folgende Fälle
unterstützen:

 ---> UL

Der Konnektor MUSS insbesondere die Kommunikation an seinen Außenschnittstellen
mit den Fachmodulen für folgende Fälle blockieren:

 ---> UL

**[\<=]**

##### TIP1-A_4744

Die Firewall des Konnektor MUSS alle abgelehnten IP-Pakete verwerfen (DROP) ohne
ein ICMP-Destination-Unreachable (Type 3) zu schicken. **[\<=]**

##### TIP1-A_4746

Der Konnektor MUSS geeignete technische Funktionen zur Abwehr von IP-Spoofing
und DoS/DDoS-Angriffen implementieren.

Der Konnektor MUSS Martian Packets (Absender– oder Empfängeradressen aus den
von der IETF als Special-Purpose definierten Netzbereichen), mindestens jedoch
aus folgenden Netzbereichen 0.0.0.0/8, 127.0.0.0/8, 169.254.0.0/16,
192.0.0.0/24, 192.0.2.0/24, 198.18.0.0/15, 198.51.100.0/24, 203.0.113.0/24,
224.0.0.0/4, 240.0.0.0/4 verwerfen. Die in [RFC1918] und [RFC 6598] definierten
Netzbereiche sind hiervonausgenommen. **[\<=]**

##### TIP1-A_4745

Die Firewall des Konnektor MUSS TCP-Port-7(Echo)-Pakete verwerfen.Die Firewall
des Konnektor MUSS ICMP-Echo-Request (Typ 8) und ICMP-Echo-Response (Typ 0)
ausschließlich für die folgenden Kommunikationen zulassen:

 ---> UL

Die Firewall des Konnektors MUSS für alle anderen Kommunikationen ein
ICMP-Echo-Request (Typ 8) verwerfen. **[\<=]**

##### TIP1-A_4747

Der Konnektor MUSS alle IP-Protokolle außer 1 (ICMP), 4 (IP in IP
(encapsulation)), 17 (UDP), 6 (TCP), 50 (ESP) und 108 (IPComp) für alle ein-
oder ausgehenden Pakete an allen seinen Adaptern verwerfen. **[\<=]**

##### TIP1-A_4748

Der Konnektor DARF seine Routing-Regeln NICHT durch IP-Kommunikation
beeinflussen lassen, weder mittels eines Routing-Protokolls (wie BGP oder RIP)
noch mittels ICMP-Kommandos (wie Redirect (5), Router Advertisement (9/10) oder
auch Mobile Host Redirect (32)) sondern MUSS diese ausschließlich
durchTUC_KON_304 „Netzwerk-Routen einrichten“setzen.

Die Firewall des Konnektor MUSS alle aus einem der Tunnel (VPN_TI oder VPN_SIS)
kommenden DHCP-Pakete verwerfen.

Die Firewall des Konnektors MUSS an den Konnektor gerichtete IPsec-Pakete (IKE,
ESP und IPsec NAT-T) verwerfen, sofern sie nicht einer vom Konnektor
initiierten IPsec-Verbindung (VPN_TI und VPN_SIS) zugeordnet werden können. **[\<=]**

##### TIP1-A_4749

Der Konnektor MUSS gewährleisten, dass unmittelbar nach einer Änderung der
Parameter eines Adapters (LAN-Adapter, WAN-Adapter, virtueller Adapter VPN_TI
oder virtueller Adapter VPN_SIS) die Firewall des Konnektor neu erstellt und
geladen wird.

Wenn der WAN-Adapter verwendet wird (ANLW_WAN_ADAPTER_MODUS=ENABLED) DARF die
Firewall des Konnektor bei einer Änderung der ANLW_WAN_IP_ADDRESS NICHT die
Verbindungen über den LAN-Adapter durch einen Restart der Firewall
beeinflussen.

Wenn der WAN-Adapter verwendet wird (ANLW_WAN_ADAPTER_MODUS=ENABLED), DARF die
Firewall des Konnektor bei einer Änderung derANLW_LAN_IP_ADDRESS NICHT die
Verbindungen über die Adapter WAN, VPN_TI oder VPN_SIS durch einen Restart der
Firewall beeinflussen. **[\<=]**

Umsetzungshinweis für den Hersteller: Es können zwei getrennten
Firewall-Regelsets für den LAN- bzw. für den WAN-Adapter verwendet werden.

##### TIP1-A_4750

Der Konnektor MUSS bei Start und Stopp der Firewall einen Protokolleintrag mit
der Schwere „Warning“und dem Typ „Operations“sowie mindestens folgenden
Informationen generieren:

 ---> UL

Der Konnektor MUSS bei Konfigurationsänderungen der Firewall einen
Protokolleintrag mit der Schwere „Warning“und dem Typ „Operations“sowie
mindestens folgenden Informationen generieren:

 ---> UL

Der Konnektor MUSS für alle vom Konnektor ausgehenden, nicht zugelassenen
Kommunikationsversuche einen Protokolleintrag mit der Schwere „Warning“und
dem Typ „Security“sowie mindestens folgenden Informationen generieren:

 ---> UL

Der Konnektor MUSS für alleverworfenenIP-Spoofing- und Martian-Packets einen
Protokolleintrag mit der Schwere „Warning“und dem Typ „Security“sowie
mindestens folgenden Informationen generieren:

 ---> UL

Der Konnektor MUSS für alle von der Firewall verworfenen IP-Pakete einen
Protokolleintrag mit der Schwere „Info“und dem Typ „Security“sowie
mindestens folgenden Informationengenerieren, wobei Layer 3 Broadcasts von der
Protokollierung ausgenommen werden können:

 ---> UL

Der Konnektor MUSS für die Firewall-Protokollierung den TUC_KON_271 „Schreibe
Protokolleintrag“nutzen. **[\<=]**

### 4.2.1.2 Durch Ereignisse ausgelöste Reaktionen

##### TIP1-A_4751

Beim Auftreten eines dernachfolgenden Events MUSS der Konnektor denTUC_KON_305
„LAN-Adapter initialisieren“starten.

 ---> UL

**[\<=]**

##### TIP1-A_4752

Beim Auftreten eines der nachfolgenden Events MUSS der Konnektor TUC_KON_306
„WAN-Adapter initialisieren“ starten.

 ---> UL

**[\<=]**

##### TIP1-A_4753

Beim Auftreten einesder nachfolgenden Events MUSS der Konnektor denTUC_KON_304
„Netzwerk-Routen einrichten“aufrufen.

 ---> UL

**[\<=]**

### 4.2.1.3 Interne TUCs, nicht durch Fachmodule nutzbar

### 4.2.1.3.1 TUC_KON_305 „LAN-Adapter initialisieren“

##### TIP1-A_4754

Der Konnektor MUSS den technischen Use Case TUC_KON_305 „LAN-Adapter
initialisieren“ umsetzen.

Tabelle310: TAB_KON_614 - TUC_KON_305 „LAN-Adapter initialisieren“

 ---> TABLE

Tabelle311: TAB_KON_615 Fehlercodes TUC_KON_305 „LAN-Adapter initialisieren“

 ---> TABLE

**[\<=]**

### 4.2.1.3.2 TUC_KON_306 „WAN-Adapter initialisieren“

##### TIP1-A_4755

Der Konnektor MUSS den technischen Use Case TUC_KON_306 „WAN-Adapter
initialisieren“ umsetzen.

Tabelle312: TAB_KON_616 - TUC_KON_306 „WAN-Adapter initialisieren“

 ---> TABLE

Tabelle313: TAB_KON_617 Fehlercodes TUC_KON_306 „WAN-Adapter initialisieren“

 ---> TABLE

**[\<=]**

### 4.2.1.3.3 TUC_KON_304 „Netzwerk-Routen einrichten“

##### TIP1-A_4758

Der Konnektor MUSS den technischen Use Case TUC_KON_304 „Netzwerk-Routen
einrichten“ umsetzen.

Tabelle314: TAB_KON_622 - TUC_KON_304 „Netzwerk-Routen einrichten“

 ---> TABLE

Tabelle315: TAB_KON_623 Fehlercodes TUC_KON_304 „Netzwerk-Routen einrichten“

 ---> TABLE

**[\<=]**

### 4.2.1.4 Interne TUCs, auch durch Fachmodule nutzbar

Keine.

### 4.2.1.5 Operationen an der Außenschnittstelle

Keine

### 4.2.1.6 Betriebsaspekte

##### TIP1-A_5414

Der KonnektorMUSS in der Bootup-Phase zur Initialisierung des Funktionsmerkmals
„Anbindung LAN/WAN“:

 ---> UL

**[\<=]**

##### TIP1-A_4759

Der Konnektor MUSS gewährleisten, dass die Konfiguration nur dann gespeichert
wird, wenn alle Parameter der nachfolgenden Tabellen den dazugehörigen
Bedingungen entsprechen, sowie grundsätzlich zulässige Werte darstellen
(gemäß RFCs).Wenn die Konfiguration per Managementschnittstelle geändert
wurde, MUSS das folgende Systemereignis ausgelöst
werden:TUC_KON_256 {      topic =
"ANLW/LAN/IP_CHANGED";      eventType = Op;      severity =
Info;      parameters = („IP=$dieNeueIP”);      doDisp =
false}Wenn (DHCP_CLIENT_LAN_STATE=Disabled) gesetzt ist, MUSS der Administrator
des Konnektor die Werte der folgenden Tabelle über die Managementschnittstelle
setzen können.Wenn (DHCP_CLIENT_LAN_STATE=Enabled) gesetzt ist, MUSS der
Administrator des Konnektor die Werte der folgenden Tabelle angezeigt bekommen,
kann diese jedoch nicht ändern.

Tabelle316: TAB_KON_683 LAN-Adapter IP-Konfiguration

 ---> TABLE

Der Administrator des Konnektor MUSS die Werte der folgenden Tabelle über die
Managementschnittstelle setzen können.

Tabelle317: TAB_KON_684 LAN-Adapter Erweiterte Parameter

 ---> TABLE

**[\<=]**

##### TIP1-A_4760

Der Konnektor MUSS gewährleisten, dass die Konfiguration nur dann gespeichert
wird, wenn alle Parameter der nachfolgenden Tabellen den dazugehörigen
Bedingungen entsprechen.Wenn die Konfiguration per Managementschnittstelle
geändert wurde, MUSS das folgende Systemereignis ausgelöst
werden:    TUC_KON_256 {topic = "ANLW/WAN/IP_CHANGED";eventType =
Op;severity = Info;parameters = („IP=$dieNeueIP“);doDisp = false}Wenn
(DHCP_CLIENT_WAN_STATE=Disabled) gesetzt ist, MUSS der Administrator des
Konnektors die Werte der folgenden Tabelle über die Managementschnittstelle
setzen können.Wenn (DHCP_CLIENT_WAN_STATE=Enabled) gesetzt ist, MUSS der
Administrator des Konnektors die Werte der folgenden Tabelle angezeigt
bekommen, kann diese jedoch nicht ändern.

Tabelle318: TAB_KON_685 WAN-Adapter IP-Konfiguration

 ---> TABLE

Der Administrator des Konnektor MUSS die Werte der folgenden Tabelle über die
Managementschnittstelle setzen können.

Tabelle319: TAB_KON_686 WAN-Adapter Erweiterte Parameter

 ---> TABLE

**[\<=]**

##### TIP1-A_4761

Die Managementschnittstelle MUSS es einem Administrator ermöglichen
Konfigurationsänderungen gemäß Tabelle TAB_KON_624 –
„Konfigurationsparameter der Anbindung LAN/WAN vorzunehmen.Wenn
(ANLW_INTRANET_ROUTES_MODUS = REDIRECT) gesetzt ist, MUSS der Konnektor jedes
Paket aus einem konfigurierten Intranet mit einem ICMP-Redirect mit dem
hinterlegten Next Hop beantworten und der Konnektor MUSS gewährleisten, dass
keine IP-Pakete in eines oder mehrere der konfigurierten Intranet geroutet
werden.Wenn (ANLW_INTRANET_ROUTES_MODUS = BLOCK) gesetzt ist, MUSS der
Konnektor alle IP-Pakete für ein Intranet (gemäß ANLW_LEKTR_INTRANET_ROUTES)
ablehnen.

Tabelle320: TAB_KON_624 – „Konfigurationsparameter der Anbindung LAN/WAN“

 ---> TABLE

**[\<=]**

##### TIP1-A_5537

Der Konnektor MUSS über die Managmentschnittstelle die konfigurierten IP-Routen
und die aktuelle IP-Routingtabelle mit mindestens folgenden Informationen
anzeigen:

 ---> UL

**[\<=]**

##### TIP1-A_4762

Im Anschluss an eine Anpassung der ANLW_FW_SIS_ADMIN_RULES MUSS der Konnektor
die Firewall neu erstellen und laden.

Tabelle321: TAB_KON_625 - Konfigurationsparameter Firewall-Schnittstelle

 ---> TABLE

**[\<=]**

### 4.2.2 DHCP-Server

Innerhalb des Kapitels DHCP-Servers werden folgende Präfixe für Bezeichner
verwendet:

 ---> UL

### 4.2.2.1 Funktionsmerkmalweite Aspekte

##### TIP1-A_4763

Der Konnektor MUSS an seiner LAN-Schnittstelle einen DHCP-Server
gemäß[RFC2131] und [RFC2132] anbieten. **[\<=]**

### 4.2.2.2 Durch Ereignisse ausgelöste Reaktionen

Keine.

### 4.2.2.3 Interne TUCs, nicht durch Fachmodule nutzbar

Keine.

### 4.2.2.4 Interne TUCs, auch durch Fachmodule nutzbar

Keine.

### 4.2.2.5 Operationen an der Außenschnittstelle

### 4.2.2.5.1 Liefere Netzwerkinformationen über DHCP

##### TIP1-A_4765

Der DHCP-Server des Konnektors MUSS an der Client-Schnittstelle eine Operation
zur Lieferung von Netzwerkinformationen über DHCP anbieten.

Tabelle322: TAB_KON_626 „Liefere Netzwerkinformationen über DHCP“

 ---> TABLE

**[\<=]**

### 4.2.2.6 Betriebsaspekte

##### TIP1-A_4766

Der DHCP- Server des KonnektorsMUSSdurch den Administrator über die
Managementschnittstelle aktivierbar und deaktivierbarsein(gemäß
TAB_KON_627).Der DHCP-ServerMUSSbei der Auslieferung deaktiviert sein.

Bei der Aktivierung MUSS der Konnektor
denTUC_KON_343"InitialisierungDHCP-Server"durchlaufen.

Sobald DHCP_SERVER_STATE geändert wurde,
mussTUC_KON_256{"DHCP/SERVER/STATECHANGED"; Op; Info;
"STATE=$DHCP_SERVER_STATE"} aufgerufen werden.

Tabelle323: TAB_KON_627„Aktivierung des DHCP-Servers“

 ---> TABLE

**[\<=]**

##### TIP1-A_4767

Der Konnektor MUSS die Möglichkeit bieten die in Tabelle TAB_KON_628 und
Tabelle TAB_KON_629 beschriebenen Parameter des DHCP-Servers über die
Managementschnittstelle zu konfigurieren.

Tabelle324: TAB_KON_628 „Basiskonfiguration des DHCP-Servers“

 ---> TABLE

Tabelle325: TAB_KON_629 „Client-Gruppenspezifische Konfigurationsoptionen des
Konnektor-DHCP-Servers“

 ---> TABLE

**[\<=]**

### 4.2.2.6.1 TUC_KON_343 „Initialisierung DHCP-Server“

##### TIP1-A_4768

Der Konnektor MUSS in der Bootup-Phase TUC_KON_343 "Initialisierung DHCP-Server"
durchlaufen.

Tabelle326: TAB_KON_630 - TUC_KON_343 „Initialisierung DHCP-Server“

 ---> TABLE

Tabelle327: TAB_KON_631 Fehlercodes TUC_KON_343 „Initialisierung DHCP-Server“

 ---> TABLE

**[\<=]**

### 4.2.3 DHCP-Client

Innerhalb des Kapitels DHCP-Client werden folgende Präfixe für Bezeichner
verwendet:

 ---> UL

### 4.2.3.1 Funktionsmerkmalweite Aspekte

##### TIP1-A_4769

Der Konnektor MUSS an seiner LAN- und WAN-Schnittstelle die Möglichkeit bieten
jeweils DHCP zu nutzen.Der DHCP-Client des Konnektors MUSS die empfangenen
Parameter wie folgt verwenden:

 ---> UL

Weitere DHCP-Parameter DÜRFEN nicht übernommen werden. **[\<=]**

### 4.2.3.2 Durch Ereignisse ausgelöste Reaktionen

##### TIP1-A_4771

Wenn das Ereignis DHCP/LAN_CLIENT/STATECHANGED
oderDHCP/WAN_CLIENT/STATECHANGEDempfangenwird, MUSS
TUC_KON_341„DHCP-Informationen beziehen“aufgerufenwerden. **[\<=]**

### 4.2.3.3 Interne TUCs, nicht durch Fachmodule nutzbar

### 4.2.3.3.1 TUC_KON_341 „DHCP-Informationen beziehen“

##### TIP1-A_4772

Der Konnektor MUSS den technischen Use Case TUC_KON_341 „DHCP-Informationen
beziehen“ umsetzen.

Tabelle328: TAB_KON_632 – TUC_KON_341 „DHCP Informationen beziehen“

 ---> TABLE

Tabelle329: TAB_KON_633 Fehlercodes TUC_KON_341 „DHCP-Informationen beziehen“

 ---> TABLE

**[\<=]**

### 4.2.3.4 Interne TUCs, auch durch Fachmodule nutzbar

Keine.

### 4.2.3.5 Operationen an der Außenschnittstelle

Keine.

### 4.2.3.6 Betriebsaspekte

##### TIP1-A_4773

Die DHCP-Client Funktionalität MUSS für LAN- und WAN-Interface vom
Administrator getrennt aktivierbar und deaktivierbar sein (gemäß
TAB_KON_634). Falls der DHCP-Client nicht verwendet wird MUSS sichergestellt
werden, dass eine statische Konfiguration, für den LAN-Adapter gemäß Tabelle
TAB_KON_683 LAN-Adapter IP-Konfiguration bzw. für den WAN-Adapter gemäß
Tabelle TAB_KON_685 WAN-Adapter IP-Konfiguration, existiert bevor die
Netzwerkeinstellungen übernommen werden.Sobald Parameter geändert wurden,
MUSS TUC_KON_256 „Systemereignis absetzen“ je nachdem auf welchem Interface
der Client aktiviert oder deaktiviert wurde mit folgenden Parameter aufgerufen
werden:TUC_KON_256{"DHCP/LAN_CLIENT/STATECHANGED"; Op;
Info;    "STATE=$DHCP_CLIENT_LAN_STATE"; doDisp =
false}oderTUC_KON_256{"DHCP/WAN_CLIENT/STATECHANGED "; Op;
Info;    "STATE=$DHCP_CLIENT_WAN_STATE "; doDisp = false}

Tabelle330: TAB_KON_634 „Konfiguration des DHCP-Clients“

 ---> TABLE

**[\<=]**

##### TIP1-A_4774

Der Administrator MUSS die Möglichkeit haben die DHCP-Lease des Konnektors für
jedes Interface getrennt zu erneuern. **[\<=]**

##### TIP1-A_4776

Falls der DHCP-Client auf der LAN-Seite nach einem Timeout von 30s keine
IP-Adresse bezogen hat, MUSS gemäß [RFC3927] eine Default-Adresse aus
169.254/16 vergeben werden. **[\<=]**

### 4.2.4 VPN-Client

Der VPN-Client beschreibt die Absicherung der Anbindung des Konnektors an die TI
und die Bestandsnetze. Während der technische Kern dieser Funktion, der Aufbau
der VPN- Kanäle zu den Konzentratoren, in [gemSpec_VPN_ZugD#TUC_VPN-ZD_0001]
und [gemSpec_VPN_ZugD#TUC_VPN-ZD_0002] beschrieben wird, regelt dieses Kapitel
die Interaktion, sowie die Konfiguration des VPN-Clients innerhalb des
Konnektors.

Innerhalb des Kapitels VPN-Client werden folgende Präfixe für Bezeichner
verwendet:

 ---> UL

### 4.2.4.1 Funktionsmerkmalweite Aspekte

##### TIP1-A_4778

Der Konnektor MUSS sich im Rahmen des IPsec-Verbindungsaufbaus gegenüber den
VPN-Konzentratoren mit seiner Identität ID.NK.VPN ausweisen.

Der VPN-Client im Konnektor MUSS das folgendeEvent generieren, sobald der
VPN-Tunnel zur TI nicht mehr zur Verfügung steht:

Rufe TUC_KON_256 {"NETWORK/VPN_TI/DOWN"; Op; Warning;}

Der VPN-Client im Konnektor MUSS das folgende Event generieren, sobald der
VPN-Tunnel zum SIS nicht mehr zur Verfügung steht:

Rufe TUC_KON_256 {"NETWORKVPN_SIS/DOWN"; Op; Warning;}

Der Hersteller des Konnektor MUSS sicherstellen, dass eine Anbindung an einen
Konzentrator ausschließlich dann möglich ist, wenn (MGM_LU_ONLINE = Enabled)
gesetzt ist.

Der Administrator des Konnektor MUSS durchdieManagementschnittstelle manuell
einen Verbindungsaufbau und einen Verbindungsabbau eines VPN-Tunnelzur TI
(VPN_TI) oder zu den SIS (VPN_SIS) initiieren können. **[\<=]**

##### TIP1-A_4779

Der Konnektor MUSS gewährleisten, dass nach einem Fehler beim
VPN-Verbindungsaufbau nicht unmittelbar ein weiterer Versuch des
Verbindungsaufbaus durchgeführt wird.

Hierzu MUSS der Hersteller ein inkrementelles (schrittweise anwachsend)Verfahren
wählen, welcher den zeitlichen Abstand zwischen einzelnen Versuchen des
VPN-Verbindungsaufbau definiert. Dieser Abstand MUSS maximal fünf
Minutenbetragen.(Diese Pausesolles dem Konnektor ermöglichen, noch ausreichend
Ressourcen für die verbleibenden Services zur Verfügung zu stellen). **[\<=]**

### 4.2.4.2 Durch Ereignisse ausgelöste Reaktionen

##### TIP1-A_4780

Beim Auftreten einer der nachfolgenden Events MUSS der Konnektor denTUC_KON_321
„Verbindung zu dem VPN-Konzentrator der TI aufbauen“starten, sofern auch
MGM_LU_ONLINE = Enabled.

 ---> UL

**[\<=]**

##### TIP1-A_4781

Beim Auftreten einer der nachfolgenden Events MUSS der Konnektor denTUC_KON_322
„Verbindung zu dem VPN-Konzentrator des SIS aufbauen“starten, sofern
ANLW_INTERNET_MODUS = SIS, MGM_LU_ONLINE = Enabled und die Verbindung
VPN-Konzentrator TI aufgebaut ist:

 ---> UL

**[\<=]**

##### TIP1-A_5417

Beim Auftreten einer der nachfolgenden Events MUSS der Konnektor den VPN-Tunnel
zur TI beenden:

 ---> UL

**[\<=]**

##### TIP1-A_4782

Beim Auftreten einer der nachfolgenden Events MUSS der Konnektor den VPN-Tunnel
zum SIS beenden:

 ---> UL

**[\<=]**

Hinweis: Wenn der IPsec-Tunnel VPN_SIS aufgebaut ist, zeigt die Default Route im
Konnektor auf die innere Tunnel-IP-Adresse des VPN-Konzentrators SIS. Dies ist
bei einer Trennung und dem Wiederaufbau der Verbindung VPN_TI zu beachten.

### 4.2.4.3 Interne TUCs, nicht durch Fachmodule nutzbar

### 4.2.4.3.1 TUC_KON_321 „Verbindung zu dem VPN-Konzentrator der TI aufbauen“

##### TIP1-A_4783

Der Konnektor MUSS den technischen Use Case TUC_KON_321 „Verbindung zu dem
VPN-Konzentrator der TI aufbauen“ umsetzen.

Tabelle331: TAB_KON_635 – TUC_KON_321 „Verbindung zu dem VPN-Konzentrator
der TI aufbauen“

 ---> TABLE

Tabelle332: TAB_KON_636 Fehlercodes TUC_KON_321 „Verbindung zu dem
VPN-Konzentrator der TI aufbauen“

 ---> TABLE

**[\<=]**

### 4.2.4.3.2 TUC_KON_322 „Verbindung zu dem VPN-Konzentrator des SIS aufbauen“

##### TIP1-A_4784

Der Konnektor MUSS den technischen Use Case TUC_KON_322 „Verbindung zu dem
VPN-Konzentrator der SIS aufbauen“ umsetzen.

Tabelle333: TAB_KON_637 – TUC_KON_322 „Verbindung zu dem VPN-Konzentrator
der SIS aufbauen“

 ---> TABLE

Tabelle334: TAB_KON_638 Fehlercodes TUC_KON_322 „Verbindung zu dem
VPN-Konzentrator der SIS aufbauen“

 ---> TABLE

**[\<=]**

### 4.2.4.4 Interne TUCs, auch durch Fachmodule nutzbar

Keine

### 4.2.4.5 Operationen an der Außenschnittstelle

Keine

### 4.2.4.6 Betriebsaspekte

##### TIP1-A_5415

Der KonnektorMUSS in der Bootup-Phase zur Initialisierung des Funktionsmerkmals
„VPN-Client“:

 ---> UL

**[\<=]**

##### TIP1-A_4785-03

Die Managementschnittstelle MUSS es einem Administrator ermöglichen
Konfigurationsänderungen am VPN-Client gemäß Tabelle TAB_KON_639
vorzunehmen.Der Konnektor MUSS bei einer Änderung der Konfigurationswerte den
folgenden Event auslösen:Rufe TUC_KON_256 {"NETWORK/VPN/CONFIG_CHANGED"; Op;
Info;; doDisp = false}

Tabelle335: TAB_KON_639 – Konfigurationsparameter VPN-Client

 ---> TABLE

**[\<=]**

### 4.2.5 Zeitdienst

Der Zeitdienst schafft die Grundlage einer gleichen Systemzeit für alle in der
TI einzusetzenden Produkttypen. Grundsätzlich ist ein NTP-Server der
Stratum-3-Ebene innerhalb des Konnektors erforderlich, welcher die Zeitangaben
eines NTP-Servers Stratum-2-Ebene abfragt (GS-A_3942). Die in [gemSpec_Net#5.1]
„NTP-Topologie“ getroffenen Anforderungen werden durch dieses Kapitel
erweitert.

Innerhalb des Zeitdienstes werden folgende Präfixe für Bezeichner verwendet:

 ---> UL

### 4.2.5.1 Funktionsmerkmalweite Aspekte

##### TIP1-A_4786

Falls der Leistungsumfang Online nicht aktiviert ist (MGM_LU_ONLINE=Disabled),
MUSS sichergestellt werden, dass der maximale zulässige Fehler von +/-
20ppm(part per million) gegenüber einer Referenzuhr nicht überschritten wird.
Dies entspricht einer maximalen Abweichung im Freilauf von +/- 34,56 Sekunden
über 20 Tage. **[\<=]**

##### TIP1-A_4787

Der NTP-Server des Konnektors MUSS deaktiviert sein, falls der Konnektor
Leistungsumfang Online nicht aktiviert ist (MGM_LU_ONLINE=Disabled. **[\<=]**

Falls die Systemzeit des Konnektors zu stark von der Zeit der zentralen
TI-Plattform abweicht, deutet dies auf ein schwerwiegendes Problem im Konnektor
oder der Umgebung hin, da dies im ordnungsgemäßen Betrieb nicht auftreten
sollte.

##### TIP1-A_4788

Der KonnektorDARF die im Konnektor vorgehaltene Systemzeit im Rahmen einer
automatisierten Synchronisation NICHT aktualisieren, wenn die lokaleZeit von
der im Rahmen der Synchronisation erhaltenen Zeit um mehr
alsNTP_MAX_TIMEDIFFERENCEabweicht.Dies betrifft NICHT Änderungen in der
Darstellung der Systemzeit, die zeitzonenbedingt sind (MEZ -\> MESZ -\> MEZ),
da die Zeitsynchronisation grundsätzlich UTC berücksichtigt.Bei einer
erstmaligen Synchronisierung nach dem Boot-Vorgang oder bei einer erstmaligen
Synchronisierung bei der Inbetriebnahme des Konnektors darf eine
Synchronisation trotz einer Zeitabweichung größer einer Stunde durchgeführt
werden.Daher MUSS der Konnektor bei einer Abweichung von mehr als einer Stunde
indenkritischen BetriebszustandEC_TIME_DIFFERENCE_INTOLERABLEübergehen, ein
weiterer fachlicher Betrieb des Konnektors DARF NICHT mehr erfolgen. **[\<=]**

Der kritische Betriebszustand kann anschließend über einen manuellen Eingriff
(z. B. Reboot) behoben werden (siehe 3.3 Betriebszustand).

##### TIP1-A_4789

TAB_KON_640 listet die zu verwendenden Zustandsvariablen des Konnektor
NTP-Servers. Diese Werte DÜRFEN NICHT durch den Administrator geändert werden.

Tabelle336: TAB_KON_640 Zustandswerte für Konnektor NTP-Server

 ---> TABLE

**[\<=]**

### 4.2.5.2 Durch Ereignisse ausgelöste Reaktionen

Keine.

### 4.2.5.3 Interne TUCs, nicht durch Fachmodule nutzbar

Keine.

### 4.2.5.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.2.5.4.1 TUC_KON_351 “Liefere Systemzeit”

##### TIP1-A_4790

Der Konnektor MUSS den technischen Use Case TUC_KON_351 „Liefere Systemzeit“
umsetzen.

Tabelle337: TAB_KON_776 TUC_KON_351 „Liefere Systemzeit“

 ---> TABLE

Tabelle338: TAB_KON_641 Fehlercodes TUC_KON_351 „Liefere Systemzeit“

 ---> TABLE

**[\<=]**

### 4.2.5.5 Operationen an der Außenschnittstelle

### 4.2.5.5.1 Sync_Time

##### TIP1-A_4791

Der NTP-Server des Konnektors MUSS an der Client-Schnittstelle eine Operation
sync_Time anbieten.

Tabelle339: TAB_KON_642 Operation sync_Time

 ---> TABLE

**[\<=]**

### 4.2.5.6 Betriebsaspekte

##### TIP1-A_4792

Der KonnektorMUSSdemAdministrator die Möglichkeit bieten, eine Synchronisation
mit dem zentralen Zeitdienst explizit anzustoßen. **[\<=]**

##### TIP1-A_4793

Der Administrator MUSS die in TAB_KON_643 aufgelisteten Parameter über die
Managementschnittstelle konfigurieren und die in TAB_KON_730 aufgelisteten
Parameter ausschließlich einsehen können.

Tabelle340: TAB_KON_643 Konfiguration des Konnektor NTP-Servers

 ---> TABLE

Tabelle341: TAB_KON_730 Einsehbare Konfigurationsparameter des Konnektor
NTP-Servers

 ---> TABLE

**[\<=]**

##### TIP1-A_4794

Befindet sich der Konnektor im Zustand EC_TIME_SYNC_PENDING_CRITICAL oder
EC_Time_Difference_Intolerable, MUSS der Administrator eine Korrektur oder
Bestätigung der Systemzeit vornehmen können. Anschließend MUSS der Konnektor
wie nach einer erfolgreichen Zeitsynchronisation verfahren, d. h. der
Tagezähler wird auf 0 zurückgesetzt. **[\<=]**

### 4.2.5.6.1 TUC_KON_352 Initialisierung Zeitdienst

##### TIP1-A_4795

Der Konnektor MUSS in der Bootup-Phase TUC_KON_352 "Initialisierung Zeitdienst"
durchlaufen.

Tabelle342: TAB_KON_644 – TUC_KON_352 „Initialisierung Zeitdienst“

 ---> TABLE

Tabelle343: TAB_KON_645 Fehlercodes TUC_KON_352 „Initialisierung Zeitdienst“

 ---> TABLE

**[\<=]**

### 4.2.6 Namensdienst und Dienstlokalisierung

Innerhalb des Namensdienstes werden folgende Präfixe für Bezeichner verwendet:

 ---> UL

### 4.2.6.1 Funktionsmerkmalweite Aspekte

##### TIP1-A_4796

Der Konnektor MUSS einen Recursive Caching Nameserver zur Auflösung von
DNS-Anfragen sowie einen autoritativen Nameserver zur Verwaltung der Zone
„konlan.“ bereitstellen.Der Caching-Nameserver des Konnektors MUSS für
Clientsysteme aus dem lokalen Netzwerk (ANLW_LAN_NETWORK_SEGMENT oder
ANLW_LEKTR_INTRANET_ROUTES) erreichbar sein.Der Caching-Nameserver des
Konnektors MUSS einen Timeout für die Bearbeitung von DNS-Abfragen beachten.
Konnte eine DNS-Abfrage nicht durchgeführt werden, MUSS die Bearbeitung
abgebrochen werden. **[\<=]**

##### TIP1-A_6480

Der Konnektor MUSS in der Zone „konlan.“ die folgenden Resource Records
bereitstellen:

 ---> UL

Die in spitzen Klammern angegebenen Werte müssen implementierungs- und
konfigurationsabhängig vergeben werden. **[\<=]**

##### TIP1-A_4797

Der DNS-Server des Konnektors MUSS die folgenden DNS-Forwards durchführen:

Tabelle344: TAB_KON_687 DNS-Forwards des DNS-Servers

 ---> TABLE

**[\<=]**

##### TIP1-A_4798

Der Stub-Resolver im Konnektor MUSS von alleninternenDiensten zur
Namensauflösung genutzt werden.

Der Stub-Resolver im Konnektor MUSS immer denCaching-Nameserverim Konnektor
anfragen. **[\<=]**

##### TIP1-A_4799

Der Konnektor,der einen Caching Nameserver als Validating Resolver umsetzt, MUSS
den DNSSEC-Vertrauensanker der TI aus dem Zertifikatspeicher in den
Caching-Nameserver übernehmen, wenn ein Fehler bei der Validierung der
Namensauflösung der TI aufgetreten ist. **[\<=]**

### 4.2.6.2 Durch Ereignisse ausgelöste Reaktionen

Keine.

### 4.2.6.3 Interne TUCs, nicht durch Fachmodule nutzbar

Keine.

### 4.2.6.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.2.6.4.1 TUC_KON_361 „DNS-Namen auflösen“

##### TIP1-A_4801

Der Konnektor MUSS den technischen Use Case TUC_KON_361 „DNS-Namen
auflösen“ umsetzen.

Tabelle345: TAB_KON_646 – TUC_KON_361 „DNS-Namen auflösen“

 ---> TABLE

Tabelle346: TAB_KON_647 Fehlercodes TUC_KON_361 „DNS Namen auflösen“

 ---> TABLE

**[\<=]**

##### TIP1-A_4801-02

Der Konnektor MUSS den technischen Use Case TUC_KON_361 „DNS-Namen
auflösen“ umsetzen.

Tabelle347: TAB_KON_646 – TUC_KON_361 „DNS-Namen auflösen“

 ---> TABLE

Tabelle348: TAB_KON_647 Fehlercodes TUC_KON_361 „DNS Namen auflösen“

 ---> TABLE

**[\<=]**

### 4.2.6.4.2 TUC_KON_362 „Liste der Dienste abrufen“

##### TIP1-A_4802

Der Konnektor MUSS den technischen Use Case TUC_KON_362 „Liste der Dienste
abrufen“ umsetzen.

Tabelle349: TAB_KON_648 – TUC_KON_362 „Liste der Dienste abrufen“

 ---> TABLE

Tabelle350: TAB_KON_649 Fehlercodes TUC_KON_362 „Liste der Dienste abrufen“

 ---> TABLE

**[\<=]**

### 4.2.6.4.3 TUC_KON_363 „Dienstdetails abrufen“

##### TIP1-A_4803

Der Konnektor MUSS den technischen Use Case TUC_KON_363 „Dienstdetails
abrufen“ umsetzen.

Tabelle351: TAB_KON_650 - TUC_KON_363 „Dienstdetails abrufen“

 ---> TABLE

Tabelle352: TAB_KON_651 Fehlercodes TUC_KON_363 „Dienstdetails abrufen“

 ---> TABLE

**[\<=]**

### 4.2.6.5 Operationen an der Außenschnittstelle

##### TIP1-A_4804

Der Konnektor MUSS für Clients eine Basisanwendung Namensdienst anbieten.

Tabelle353: TAB_KON_652 Basisanwendung Namensdienst

 ---> TABLE

**[\<=]**

### 4.2.6.5.1 GetIPAddress

##### TIP1-A_5035

Der Namensdienst des Konnektors MUSS an der Client-Schnittstelle eine Operation
GetIPAddress anbieten.

Tabelle354: TAB_KON_653 Operation GetIPAddress

 ---> TABLE

**[\<=]**

### 4.2.6.6 Betriebsaspekte

##### TIP1-A_5416

Der KonnektorMUSS in der Bootup-Phase zur Initialisierung des Funktionsmerkmals
„Namensdienst und Dienstlokalisierung“:

 ---> UL

**[\<=]**

##### TIP1-A_4805

Der Administrator MUSS die in TAB_KON_654 aufgelisteten Parameter über die
Managementschnittstelle konfigurieren und die in TAB_KON_731 aufgelisteten
Parameter ausschließlich einsehen können.Nach jeder Änderung MUSS
sichergestellt werden, dass die Änderungen sofort am autoritativen bzw. am
Caching-Nameserver zur Verfügung stehen.

Tabelle355: TAB_KON_654 - Konfigurationsparameter Namensdienst

 ---> TABLE

Tabelle356: TAB_KON_731 Einsehbare Konfigurationsparameter Namensdienst

 ---> TABLE

**[\<=]**

### 4.2.7 Optionale Verwendung von IPv6

Der Konnektor kann zusätzlich eine IPv6-Adresse an den Netzwerkschnittstellen
zum Transportnetz implementieren. Entscheidet sich der Hersteller für den
parallelen Einsatz von IPv4 und IPv6 (Dual-Stack-Mode), sind die nachfolgenden
Anforderungen dieses Kapitels umzusetzen. Einhergehend mit der Entscheidung,
IPv6 an diesem Interface zu konfigurieren, ist der spätere VPN-Tunnelaufbau
zur TI und SIS über das IPv6 Interface möglich. Die durch den jeweiligen
IPv6-Tunnel zu transportierenden IP-Pakete sind IPv4 adressierte Pakete.

##### A_17199

Der Konnektor MUSS bei Verwendung von IPv6 für den VPN-Tunnelaufbau zur TI und
SIS auf geeignete Weise (z.B. DHCP vom IAG) mit einer IPv6-Adresse auf dem
physikalischen Interface in Richtung Internet konfiguriert werden
(Dual-Stack-Mode). **[\<=]**

##### A_17200

Der Konnektor MUSS bei Verwendung von IPv6 für den VPN-Tunnelaufbau zur TI und
SIS die Fragmentierung von IKEv2 Nachrichten gemäß [RFC7383] unterstützen.
**[\<=]**

##### A_17201

Der Konnektor MUSS bei Verwendung von IPv6 für den VPN-Tunnelaufbau zur TI und
SIS die notwendige Route für das Erreichen des Internets bereitstellen.
**[\<=]**

### 4.3 Konnektormanagement

Das Konnektormanagement dient ausschließlich Betriebsaspekten des Konnektors.
Daher wird in diesem Kapitel weitestgehend auf die übliche Strukturierung nach
TUCs (intern/für Fachmodule), Außenoperationen und Betriebsaspekten
verzichtet. Lediglich der KSR-Client verwendet diese Kapitelstruktur.

Innerhalb des Konnektormanagements werden vorrangig folgende Präfixe für
Bezeichner verwendet:

 ---> UL

Eine Ausnahme hiervon bildet der Anteil der Software-Aktualisierung
(KSR-Client). Dieser verwendet folgende Präfixe für Bezeichner:

 ---> UL

##### TIP1-A_4806

Der Konnektor MUSS LAN-seitig über eine Managementschnittstelle für
Konfiguration und Diagnose verfügen.Die Ausführung der Schnittstelle ist
herstellerspezifisch, MUSS aber entweder als Konfigurations-Frontend im Sinne
einer eigenständigen Client-Applikation oder als Web-Oberfläche ausgeprägt
sein.Wenn die Schnittstelle als Web-Oberfläche ausgeprägt ist, MUSS im
Handbuch beschrieben sein, wo angegeben ist, welche Browser-Versionen für
welche Betriebssysteme unterstützt werden (bspw. im Handbuch selbst oder über
einen Link auf eine Web-Seite des Herstellers), und wo diese als
installierbares Softwarepaket oder direkt ausführbare Datei bezogen werden
können.Die Verbindung zur Managementschnittstelle MUSS zur Sicherung der
Vertraulichkeit, Integrität und Authentizität durch Nutzung eines
kryptographischen Verfahrens gemäß [gemSpec_Krypt] abgesichert werden, falls
die Sicherheit der übertragenen Daten nicht auf andere Weise erreicht wird.
Die Absicherung der Daten kann z. B. durch Nutzung von TLS unter
Berücksichtigung der in [gemSpec_Krypt] angegebenen Algorithmen und
Schlüssellängen geschehen.Die Managementschnittstelle MUSS in thematisch
gegliederte Konfigurationsbereiche unterteilt sein. Die konkrete Gliederung
selbst ist herstellerspezifisch.Die Managementschnittstelle KANN einen
Managementbereich aufweisen, der nur für autorisierte Techniker des
Herstellers zugänglich ist. Ein Zugriff auf diesen Bereich MUSS durch eine
eigene Authentisierungsfunktion geschützt werden (z. B. durch
Passwortschutz). **[\<=]**

Die über die Managementschnittstelle zu erreichenden und zu verändernden
Inhalte werden erhoben in:

 ---> UL

Eine Ergänzung um weitere, herstellerspezifische Konfigurationsinhalte ist
möglich.

##### TIP1-A_5661

Der Konnektor MUSS für die Automatisierung von Konnektor-Tests alle Funktionen,
die über die Managementschnittstelle bereitgestellt werden,über
eineLAN-seitigeSchnittstelle ohne graphische Benutzerführung bereitstellen.

Der Konnektorhersteller MUSS eine Dokumentation der Schnittstelle bereitstellen,
welche die Nutzung so beschreibt, dass die Schnittstelle von der gematik in
vollem Umfang genutzt werden kann. Die Dokumentation MUSS der gematik im
Regelfall zwei Wochen vor Einreichung des Zulassungsobjekts bereitgestellt
werden. Von diesem Regelfall KANN in Abstimmung mit der gematik abgewichen
werden.

Die Schnittstelle SOLL mittels JSON [RFC7159] bereitgestellt werden. Wenn die
Bereitstellung nicht mittels JSON erfolgt, MUSS sie über eine vergleichbare
Technologie erfolgen.

Der Zugriff auf die Schnittstelle MUSS in RU/TU erlaubt sein. Falls der Zugriff
in der PU erlaubt ist, MUSS er dort ebenso wie die Managementschnittstelle
abgesichert sein:

 ---> UL

Ansonsten DARF der Zugriff in der PU NICHT möglich sein. **[\<=]**

##### TIP1-A_4807

Das Management des Konnektors MUSS über die Managementschnittstelle
mandantenübergreifend erfolgen. Dies bedeutet insbesondere, dass ein
Administrator(gemäß seiner Zugriffsberechtigungen) in einer
Management-Session alle Einstellungen einsehen und verändern können MUSS,
egal welchem Mandanten diese Werte zugeordnet sind. **[\<=]**

##### TIP1-A_5658

Der Konnektor MUSS die Managementschnittstelle mit zwei getrennten Endpunkten
implementieren. Der Konnektor MUSS sicherstellen, dass auf den einen Endpunkt
nur Nutzer mit der Rolle Lokaler-Administrator oder Super-Administrator
zugreifen können, und auf den anderen Endpunkt nur Nutzer mit der Rolle
Remote-Administrator. **[\<=]**

##### TIP1-A_5005

Jede Änderung, die ein Administrator vornimmt, MUSS protokolliert werden durch
TUC_KON_271 „Schreibe Protokolleintrag“
{    topic=„MGM/ADMINCHANGES“;    eventType=Op;    severity=Info;    parameters
=(„User=$AdminUsername,                          
RefID=$ReferenzID,                          
NewVal=$NeuEingestellterWert“)}Der hier geforderte Logging-Level gilt, wenn
nicht an anderer Stelle eine abweichende Regelung spezifiziert ist.Wenn die
Änderung über ein Remote-Management-System durchgeführt wird, ohne dass ein
Remote-Administrator im Konnektor konfiguriert ist, so MUSS als User eine
Referenz auf das Remote-Management-System verwendet werden.Passwörter DÜRFEN
NICHT in den Protokolleinträgen geschrieben werden. **[\<=]**

### 4.3.1 Zugang und Benutzerverwaltung des Konnektormanagements

Der Konnektor verfügt über keine Verwaltung der fachlichen Nutzer, wohl aber
über eine Verwaltung der Nutzer, die in der Rolle eines Administrators den
Konnektor konfigurieren und die Protokolle einsehen dürfen. Dabei werden drei
Administrator-Rollen unterschieden:

 ---> OL

##### TIP1-A_4808-01

Der Konnektor MUSS sicherstellen, dass die Managementschnittstelle vor
unberechtigtem Zugang geschützt ist. Die Managementschnittstelle MUSS durch
eine Kombination aus Benutzername und Passwort oder einen mindestens gleich
starken Mechanismus vor unberechtigtem Zugang geschützt sein.Für die
Passworterstellung MUSS der Konnektor mindestens folgende Aspekte
berücksichtigen:

 ---> UL

Für die Passwortverarbeitung MUSS der Konnektor mindestens folgende Aspekte
berücksichtigen:

 ---> UL **[\<=]**

Näheres hierzu regeln die Schutzprofile des Konnektors.

##### TIP1-A_4810

Der Konnektor MUSS eine Benutzerverwaltung für die Managementschnittstelle
enthalten, in der anmeldeberechtigte Administratoren-Benutzer definiert werden
können.Die Benutzerverwaltung MUSS die Administrator-Rollen
Lokaler-Administrator, Remote-Administrator und Super-Administrator
unterstützen.Den Administrator-Rollen MÜSSEN folgende Rechte zugewiesen sein:

 ---> UL

Tabelle357: TAB_KON_655 Konfigurationen der Benutzerverwaltung
(Super-Administrator)

 ---> TABLE

Die Benutzerverwaltung MUSS es jedem Benutzer ermöglichen
Konfigurationsänderungen gemäß Tabelle TAB_KON_656 vorzunehmen:

Tabelle358: TAB_KON_656 Konfigurationen der Benutzerverwaltung

 ---> TABLE

**[\<=]**

### 4.3.2 Konnektorname und Versionsinformationen

##### TIP1-A_4811

Der Konnektor MUSS die Konfiguration und Nutzung eines sprechenden
Konnektornamens unterstützen, der identisch zum Hostnamen des Konnektors ist.
Der Konnektorname MUSS dauerhaft an der Managementschnittstelle angezeigt
werden.Die Managementschnittstelle MUSS es einem Administrator ermöglichen
Konfigurationsänderungen gemäß Tabelle TAB_KON_657 vorzunehmen:

Tabelle359: TAB_KON_657 Konfigurationsparameter des Konnektornamens

 ---> TABLE

Optional KANN ein Hersteller zusätzlich zum Konnektor- bzw. Hostnamen die
Konfiguration eines DNS-Suffixes vorsehen. Der DNS-Suffix DARF NICHT
Bestandteil des Konnektornamens sein. **[\<=]**

##### TIP1-A_4812

Der Administrator MUSS die Versionsinformationen des Konnektors einsehen
können. Dabei MÜSSEN alle über ProductInformation.xsd definierten Elemente
verständlich angezeigt werden.

Ferner MUSS der Administrator dabei die aktuelle Firmware-Gruppenversion des
Konnektors einsehen können. **[\<=]**

##### A_18929

Der Hersteller MUSS die ECC-Vorbereitung der gSMC-K durch die Bezeichnung
„ECC-Vorbereitet“ zusammen mit den Versionsinformationen des Konnektors an
der Managementschnittstelle sichtbar machen. **[\<=]**

##### TIP1-A_7255

Der Administrator MUSS die Versionen der in der Firmware des Konnektors
enthaltenen Fachmodule einsehen können. **[\<=]**

Fachmodulversionsinformationen sind nicht Bestandteil der Selbstauskunft gemäß
ProductInformation.xsd.

### 4.3.3 Konfigurationsdaten: Persistieren sowie Export-Import

##### TIP1-A_4813

Der Konnektor MUSS die Konfigurationsdaten nach Änderung persistieren. Dabei
MÜSSEN Integrität, Authentizität und Vertraulichkeit der Konfigurationsdaten
gewährt sein. Der Mechanismus hierfür ist herstellerspezifisch.

Der Konnektor MUSS sicherstellen, dass immer ein integerer Konfigurationssatz
persistiert ist.

Bei der Konnektorinitialisierung MÜSSEN die persistierten Konfigurationsdaten
eingelesen werden.

Die Verpflichtung zur Persistierung gilt für alle innerhalb der Konnektor- und
Fachmodul-Spezifikationen erhobenen Konfigurationsdaten. **[\<=]**

##### TIP1-A_4814

Der Administrator MUSS die gesamten Konfigurationsdaten des Konnektors ex- und
importieren können. Dazu gehören die Konfigurationsparameter des Konnektors,
die persistenten Daten wie im Informationsmodell des Konnektors (Tabelle
TAB_KON_507 Informationsmodell Entitäten) definiert  und die Pairing
Informationen der Kartenterminals.Die Konfigurationsdaten des Anwendungs- und
Netzkonnektors KÖNNEN gemeinsam oder getrennt exportiert bzw. importiert
werden. Das Format der Konfigurationsdaten ist herstellerspezifisch.Auf
hardwareseitig baugleichen Geräten:

 ---> UL

Der Import von Konfigurationsdateien, die von einem Konnektor mit anderer
Hardwareversion exportiert wurden, KANN ermöglicht werden.

(für Fachmodule siehe Kapitel 4.3.4)

Der Konnektor MUSS sicherstellen, dass der Exportvorgang nur von einem am
Konnektor angemeldeten User mit mindestens der Rolle Administrator ausgelöst
werden kann.

Der Konnektor MUSS sicherstellen, dass der Importvorgang nur von einem am
Konnektor angemeldeten User mit der Rolle Super-Administrator ausgelöst werden
kann.

Sowohl Ex- als auch Import MÜSSEN protokolliert werden durch TUC_KON_271
„Schreibe Protokolleintrag“ {    

    topic = „MGM/CONFIG_EXIMPORT“;

    eventType = Op;

    severity = Info;

    parameters = („User=$AdminUsername,

                            Mode=[Export/Import]“)}. **[\<=]**

##### A_19738

DerKonnektor KANN einem am Konnektor angemeldeten User mit der Rolle
Lokaler-Administrator erlauben, den Importvorgang von Konfigurationsdateien
auszulösen, wennin den Konfigurationsdaten keine Benutzerdatengemäß Tabelle
TAB_KON_655 enthalten sind. **[\<=]**

Nähere Vorgaben zum Ablauf des Imports der Kartenterminalinformationen finden
sich im Kapitel 4.1.4.6.3.

##### TIP1-A_4815

DieIntegrität, Authentizität und Nichtabstreitbarkeitder exportierten Daten
MUSS sichergestellt werden. Dies MUSS durch eine Signatur mit der
OSIG-Identität der SM-B oder mit einem herstellerspezifischenSchlüsselpaar
realisiert werden. In die zu signierenden Daten MUSS eine Zeitangabe zum
Signaturzeitpunkt integriert werden. Beim Import MUSS die Signatur vor der
Übernahme der Daten erfolgreich verifiziert worden sein. Im Laufe des
Importvorgangs MUSS dem Administrator das zur Signatur zugehörige Zertifikat
(oder der herstellerspezifische öffentliche Schlüssel) sowie die Zeitangabe
zum Signaturzeitpunkt der exportierten Konfiguration angezeigt werden, undder
Administrator MUSS explizit bestätigen, dass er die zu dem angezeigten
Zeitpunkt gehörige Konfiguration importieren will.

Wird die SM-B zur Signatur eingesetzt, so MUSS die Prüfung des genutzten
Signaturzertifikats anhand von TUC_KON_037 erfolgen. Das Zertifikat der
OSIG-Identität, mit dem die Daten signiert wurden, MUSS zusammen mit den
exportierten Daten gespeichert werden, um eine Verifikation der Signatur auf
neuen Konnektoren auch ohne Zugriff auf die entsprechende SM-B zu ermöglichen.

DaKonfigurationsdaten mit einem Schutzbedarf von mindestens „Hoch“für
Authentizität und Nichtabstreitbarkeit exportiertwerden(z. B.
Pairing-Geheimnisse (ShS.KT.AUT) der Kartenterminals), MUSS durch geeignete
Maßnahmen sichergestellt werden, dass der Zugriff auf die Daten auf eine
natürliche Person rückführbar ist. Dies kann organisatorisch(durch Einträge
des Administrators in ein Betriebsführungs-HandbuchbeimNutzer)technisch (durch
eine personenbezogene Administratorenverwaltung) oder äquivalent
herstellerspezifischerreicht werden. **[\<=]**

##### TIP1-A_4816

Zum Schutz derVertraulichkeitder exportierten Daten MÜSSEN die Daten vor dem
Export verschlüsselt werden. Dies kann durch asymmetrische oder symmetrische
Verschlüsselungsverfahrennach [gemSpec_Krypt]realisiert werden.

Wird ein rein symmetrisches Verfahren eingesetzt, so MUSS als Mindestanforderung
eine Passphrase einer Mindestlänge von16Zeichen(Groß- und Kleinbuchstaben,
Ziffern und Sonderzeichen)zur Verschlüsselung der Daten eingesetzt werden.
Diese Passphrase MUSS dabei vom Konnektor zufällig generiert werdenund aus
einer Kombination von Buchstaben und Ziffern bestehen.Diese Passphrase MUSS dem
Administrator anschließend angezeigt werden. **[\<=]**

### 4.3.4 Administration von Fachmodulen

Die Konfiguration von Fachmodulen ist innerhalb der Managementschnittstelle des
Konnektors von der Konfiguration der Plattformanteile des Konnektors logisch
entkoppelt. Die Festlegungen, welche Konfigurationsparameter und welche
zusätzlichen administrativen Funktionen für ein Fachmodul benötigt werden,
werden in den jeweiligen Fachmodulspezifikationen getroffen. Der Konnektor muss
aber für jedes Fachmodul hinsichtlich der Administrierbarkeit des Fachmoduls
die folgende Basisfunktionalität zur Verfügung stellen:

##### TIP1-A_4818

Neben den Konfigurationsbereichen der Plattformanteile des Konnektors, MUSS die
Managementschnittstelle auch die Konfiguration der im Konnektor enthaltenen
Fachmodule unterstützen.

Ein Administrator MUSS die in den Fachmodulspezifikationen enthaltenen
Konfigurationsparameter ändern und die dort definierten Informationen einsehen
können.

Der Konnektor MUSS die Konfigurationsdaten von Fachmodulen nach deren Änderung
persistieren, sowie bei einem Neustart eines Fachmoduls die
Fachmodul-Konfigurationsdaten vor der Initialisierung des Fachmoduls einlesen.

Die persistierten Fachmodulkonfigurationsdaten MÜSSEN ebenso wie die
plattformeigenen Konfigurationsdaten hinsichtlich ihrer Integrität und
Authentizität sowie ihrer Vertraulichkeit geschützt werden.

Der Ex- und Import von Fachmodulkonfigurationen MUSS äquivalent zum Ex- und
Import der Plattformanteile für den Administrator möglich sein (siehe4.3.3).
Die Konfigurationsdaten der Fachmodule KÖNNEN dabei in der Gesamt
Export-Dateides Konnektors enthalten sein oder separat exportiert und
importiert werden. **[\<=]**

##### TIP1-A_5484

Der Konnektor MUSS den Fachmodulen die Möglichkeit bereitstellen, die in den
Fachmodulspezifikationen gekennzeichneten Konfigurationsdaten persistent zu
speichern, auszulesen und zu löschen. Je Fachmodul muss ein exklusiv durch das
Fachmodul nutzbarer Speicherbereich verwendet werden.Namenskonvention zur
Kennzeichnung der Konfigurationsdaten der Fachmodule für persistent zu
speichernde Daten:FM_\<fmName\>_\<fmDataName\>

Tabelle360: TAB_KON_833 Bezeichner für persistente Konfigurationsdaten für
Fachmodule

 ---> TABLE

**[\<=]**

### 4.3.5 Neustart und Werksreset

##### TIP1-A_4819

Der Administrator MUSS einen Neustart des Konnektors auslösen können. **[\<=]**

##### TIP1-A_4820

Ein Administrator mit USER_RESET_PERMISSION MUSS einen Werksreset des Konnektors
auslösen können.Zur Durchführung des Werksreset MUSS der Administrator nach
Funktionsaufruf per Sicherheitsabfrage zur Bestätigung des Werksresets
aufgefordert werden. Nach bestätigter Sicherheitsabfrage MUSS der Konnektor
die gesamte Konfiguration des Konnektors und alle internen Speicher, mit
Ausnahme des aktuellen Vertrauensraums sowie der Sicherheitsprotokolle und der
installierten Firmware, auf den Auslieferungszustand zurücksetzen. Die in
CERT_IMPORTED_CA_LIST enthaltenen Zertifikate MÜSSEN aus dem aktuellen
Vertrauensraum gelöscht werden.Die Durchführung des Werksresets MUSS
protokolliert werden durch TUC_KON_271 „Schreibe Protokolleintrag“
{    topic = „MGM/FACTORYSETTINGS“;    eventType =
Op;    severity = Info;    parameters =
„User=$AdminUsername“}.Dieser Protokolleintrag DARF NICHT durch einen
erfolgreichen Werksreset verloren gehen.Der Hersteller MUSS ferner einen
alternativen, herstellerspezifischen Weg zum Auslösen des Werksresets
vorsehen, welcher die Arbeitsabläufe beim Nutzer nur minimal unterbricht. Auch
für diesen zusätzlichen Weg MUSS zuvor eine Authentisierung durch eine
Kombination aus Benutzername und Passwort oder einem mindestens gleich starken
Mechanismus erfolgen. Der Mechanismus MUSS auch dann funktionieren, wenn sich
keiner der in der Benutzerverwaltung definierten Administratoren mehr
erfolgreichen anmelden kann. **[\<=]**

### 4.3.6 Leistungsumfänge und Standalone-Szenarios

Obgleich der Konnektor in seinem Auslieferungszustand alle Leistungsmerkmale
aufweisen muss, die gemäß Produkttypssteckbrief gefordert werden, so soll es
dem Administrator doch ermöglicht werden grundsätzliche Leistungsumfänge
gezielt deaktivieren zu können, um den Konnektor so besser in die
organisatorische/technische Struktur der Betriebsstätte eingliedern zu können.

##### TIP1-A_4821-02

Die Managementschnittstelle MUSS es einem Administrator ermöglichen
Konfigurationsänderungen gemäß Tabelle TAB_KON_658 vorzunehmen:

Tabelle361: TAB_KON_658 Aktivieren/Deaktivieren von Leistungsumfängen

 ---> TABLE

**[\<=]**

Der Konfigurationsparameter MGM_LU_SAK wirkt hauptsächlich in dem
Funktionsmerkmal „Signaturdienst“ (siehe Kapitel 4.1.8).

Ist MGM_LU_ONLINE Disabled, so baut der Konnektor grundsätzlich keine
Online-Verbindungen auf (weder zur TI, noch zum SIS). Der Parameter wirkt
hauptsächlich in den Funktionsmerkmalen:

 ---> UL

Ob es sich bei einem Konnektor um den losgelöst (stand alone) vom Netz der
Einsatzumgebung betriebenen handelt, also einen Konnektor, auf welchen kein
Clientsystem zugreift, muss diesem mitgeteilt werden:

##### TIP1-A_4822

Die Managementschnittstelle MUSS es einem Administrator ermöglichen
Konfigurationsänderungen gemäß Tabelle TAB_KON_659 vorzunehmen:

Tabelle362: TAB_KON_659 Konnektor Standalone einsetzen

 ---> TABLE

​​ **[\<=]**

Das Setzen von MGM_STANDALONE_KON auf Enabled dient dem Konnektor als Anzeige,
dass dieser ohne angeschlossenes Clientsystem (Primärsystem) betrieben wird.
Diese Information kann seitens der Fachmodule verwendet werden, damit diese
sich im Standalone-Fall anders als im Normalfall verhalten.

### 4.3.7 Online-Anbindung verwalten

Um Zugang zur TI erlangen zu können, muss der Betriebsstättenverantwortliche
einen Vertrag mit einem Zugangsdienstprovider (ZGDP) abgeschlossen haben. Von
diesem erhält er eine ContractID. Der Administrator muss den Konnektor
(genauer das NK-Zertifikat C.NK.VPN) mit dieser Information unter Nutzung einer
SM-B über den Registrierungsdienst des ZGDP bei diesem freischalten.

Die Berechtigung zur Einwahl in die TI ist von der Gültigkeit derbeidenbei der
Freischaltung übermittelten Zertifikate abhängig (C.NK.VPN und C.HCI.OSIG).
Die Berechtigung zur Einwahl in die TI wird verweigert, bzw. eine bestehende
Verbindung zur TI wird beendet, wenn ein Zertifikat abgelaufen oder gesperrt
ist. Aus diesem Grund muss der Administrator vor Ablauf eines der beiden
Zertifikate eine wiederholte Registrierung mit neuem Netzkonnektorzertifikat
bzw. neuer SM-B beim ZGDP durchführen. (Hinweis: neue NK-Zertifikate werden
erst mit Etablierung der Nachladefunktionalität für gSMC-K verfügbar sein.)

Soll ein Konnektor außer Betrieb genommen werden oder wird der Vertrag mit
einem ZGDP gekündigt, muss der Administrator den Konnektor über den
Registrierungsdienst des ZGDP abmelden.

##### TIP1-A_4824

Der Administrator MUSS die in TAB_KON_661 aufgelisteten Parameter über die
Managementschnittstelle konfigurieren und die in TAB_KON_732 aufgelisteten
Parameter ausschließlich einsehen können.

Tabelle363: TAB_KON_661 Konfigurationsparameter der Konnektorfreischaltung

 ---> TABLE

Tabelle364: TAB_KON_732 Einsehbare Konfigurationsparameter der
Konnektorfreischaltung

 ---> TABLE

Den Zustand der Freischaltung verwaltet der Konnektor gemäß Tabelle
TAB_KON_662 Zustandswerte der Konnektorfreischaltung.Im Auslieferungszustand
MUSS MGM_TI_ACCESS_GRANTED=Disabled belegt sein.

Tabelle365: TAB_KON_662 Zustandswerte der Konnektorfreischaltung

 ---> TABLE

​​ **[\<=]**

##### TIP1-A_4825

Der Administrator MUSS den Konnektor über folgenden Mechanismus zur Nutzung
freischalten bzw. eine vorhandene Freischaltung mit einer neuen SM-B
aktualisieren können (Voraussetzung ist eine korrekte Konfiguration aller für
einen Online-Zugang erforderlicher Parameter):

 ---> OL

Tritt während der Verarbeitungskette ein Fehler auf, so bricht die weitere
Verarbeitung ab und der Administrator MUSS darüber geeignet informiert werden
(u.a. Klartextanzeige des vom Registrierungsdienst gemeldeten Fehlers).

Wenn eine Reregistrierung mit einer neuen SMC-B fehlschlägt (Request wird mit
einem SOAP-Error beantwortet ) dann ist der Konnektor nicht registriert
(MGM_TI_ACCESS_GRANTED = Disabled). **[\<=]**

##### TIP1-A_4826-01

Der Administrator MUSS über die Managementschnittstelle den aktuellen
Freischaltstatus einsehen können (MGM_TI_ACCESS_GRANTED). Ist der Konnektor
aktuell freigeschaltet, so MÜSSEN der VPN:ContractStatus, die für die
Freischaltung verwendete(n) SMC-B und die verwendeten C.NK.VPN-Zertifikate
angezeigt werden (RSA und/oder ECC). **[\<=]**

Möchte ein Konnektoreigentümer das Gerät weiterveräußern oder vollständig
außer Betrieb nehmen, so sollte er eine vorhandene Freischaltung zuvor
rückgängig machen.

##### TIP1-A_4827

Ist MGM_TI_ACCESS_GRANTED=Enabled, dann MUSS der Administrator über die
Managementschnittstelle des Konnektors die Freischaltung über den folgenden
Mechanismus zurücknehmen können:

 ---> OL

Tritt während der Verarbeitungskette ein Fehler auf, so bricht die weitere
Verarbeitung ab und der Administrator MUSS darüber geeignet informiert werden
(u.a. Klartextanzeige des vom Registrierungsdienst gemeldeten Fehlers).

Wenn eine Deregistrierung mit einer neuen SMC-B fehlschlägt (Request wird mit
einem SOAP-Error beantwortet) dann ist der Konnektor weiterhin registriert
(MGM_TI_ACCESS_GRANTED = Enabled). **[\<=]**

##### TIP1-A_5655

Der Hersteller des Konnektors MUSS im Handbuch den Administrator darüber
informieren, dass der Konnektor bei dauerhafter Außerbetriebnahme (z. B.
Verkauf, Schenkung, Entsorgung) beim Zugangsdienstprovider deregistriert werden
muss. **[\<=]**

##### A_23120

Der Konnektor DARF die automatische Re-Registrierung mit seinem
ECC-NK-Zertifikat NICHT öfter als einmal am Tag versuchen. **[\<=]**

##### A_23150

Der Konnektor MUSS dem Administrator über den Mechanismus in TUC_KON_411
ermöglichen, den Konnektor zu registrieren bzw. eine vorhandene Registrierung
zu aktualisieren. Dabei MUSS der Administrator das für die Registrierung zu
verwendende NK-Zertifikat (RSA oder ECC) und die zu verwendende SMC-B
auswählen können. **[\<=]**

##### A_23122

Der Konnektor MUSS dem Administrator ermöglichen, die automatische
Re-Registrierung mit dem ECC-NK-Zertifikat ein- und auszuschalten. Im
Auslieferungszustand muss die automatische Re-Registrierung eingeschaltet sein.
**[\<=]**

##### A_23121

Der Konnektor MUSS dem Administrator ermöglichen, die Verwendung von ECC bei
IPsec/IKE-Verbindungen ein- und auszuschalten. Die Verwendung von ECC darf nur
eingeschaltet werden, wenn der Konnektor mit seinem ECC-NK-Zertifikat beim
VPN-Zugangsdienst registriert ist. Die Verwendung von ECC darf nur
ausgeschaltet werden, wenn der Konnektor mit seinem RSA-NK-Zertifikat beim
VPN-Zugangsdienst registriert ist.Im eingeschalteten Zustand MUSS der Konnektor
die Vorgaben in A_17125 umsetzen. Im ausgeschalteten Zustand MUSS der Konnektor
die Vorgaben in GS-A_4382 umsetzen. **[\<=]**

##### A_23149

Der Konnektor MUSS dem Administrator ermöglichen, die Verwendung von
ECDSA-basierten Ciphersuiten bei TLS-Verbindungen ein- und auszuschalten. Im
ausgeschalteten Zustand DARF der Konnektor ECDSA-basierte Ciphersuiten NICHT
anbieten (Rolle TLS-Client) und NICHT auswählen (Rolle TLS-Server). Ebenfalls
DARF der Konnektor dann NICHT während des TLS-Verbindungsaufbaus (genauer bei
der Signatur der ephemeren (EC)DH-Schlüssel) mit ECDSA-basierten Zertifikaten
bzw. deren privaten ECC-Schlüsselmaterial Daten authentisieren. **[\<=]**

Es können separate Konfigurationsschalter für einzelne TLS-Strecken umgesetzt
werden.

Es gelten darüber hinaus:

 ---> UL

### 4.3.8 Re-Registrierung des Konnektors mit weiterem NK-Zertifikat

Eine Re-Registrierung eines Konnektors am VPN-Zugangsdienst mit einem neuen
NK-Zertifikat wird im Rahmen der ECC-Migration der IPsec-Kommunikation zum
VPN-Zugangsdienst mit einem ECC-Zertifikat notwendig

##### A_22332-01

Solange der Konnektor nur mit einem RSA-Zertifikat am VPN-Zugangsdienst
registriert ist, MUSS er mindestens einmal wöchentlich die Re-Registrierung
mit seinem ECC-NK-Zertifikat beim Registrierungsdienst durchführen. **[\<=]**

##### A_21758-05

Der Konnektor MUSS den technischen Use Case TUC_KON_411 "Konnektor mit neuem
NK-Zertifikat registrieren"umsetzen.

Tabelle 366: TAB_KON_932 – TUC_KON_411 „Konnektor mit neuem NK-Zertifikat
registrieren“

 ---> TABLE

Tabelle 367: Tab_Kon_933 Fehlercodes TUC_KON_411"Konnektor mit neuem
NK-Zertifikat registrieren"

 ---> TABLE

**[\<=]**

##### A_21781

Der Hersteller des Konnektors MUSS in seinem Handbuch den Nutzer/Administrator
darauf hinweisen, dass das Ereignis mit dem Topic=SMC_K/REGISTER/ERROR dringend
durch das Primärsystem abonniert werden sollte. Bei Auftreten des Fehlers mit
Fail=No_Smcb muss in der Leistungserbringerumgebung dafür gesorgt werden, dass
eine freigeschaltete SMC-B verfügbar ist, die der Konnektor beim nächsten
Re-Registrierungsversuch verwenden kann. **[\<=]**

### 4.3.9 Remote Management (Optional)

Im Betreibermodell der TI wird unter Remote Management ein delegierter Betrieb
dezentraler Produkte durch einen durch den Anwender beauftragten Servicepartner
verstanden. Der Servicepartner stellt als Vertragsbestandteil bevollmächtigte
Personen zur Verfügung, die sich ständig um die Betriebs- und Datensicherheit
der dezentralen Produkte im Rahmen eines Remote Managements kümmern.

Voraussetzung für die Etablierung dieses Bestandteils des Betreibermodells der
TI ist, dass ein dezentrales Produkt ein Remote Management technisch
unterstützt. Die nachfolgend aufgeführten Anforderungen bilden die Grundlage
für die Nutzung von Remote Management am Konnektor.

Zum Remote Management gehören die Verwaltung von Konfigurationsdaten und die
Durchführung weiterer Administratoraktionen wie z. B. die Aktualisierung der
Software des Konnektors. Im Rahmen des Remote Managements kann der Konnektor
Remote Monitoring unterstützen. Dazu übermittelt der Konnektor
Betriebszustandsdaten an das Remote- Management-System.

##### TIP1-A_7276-01

Der Konnektor KANN Remote Management technisch unterstützen.Falls der Konnektor
das Remote Management technisch unterstützt, MUSS der Konnektor
alle Anforderungen, die das Remote Management (z.B. auch Remote-Administrator)
betreffen, umsetzen.Andernfalls sind die Anforderungen, die das Remote
Management (z.B. auch Remote-Administrator) betreffen, für den Konnektor nicht
relevant. **[\<=]**

##### TIP1-A_5647

Der Konnektor DARF über die Remote-Managementschnittstelle KEINE
personenbezogenen Daten übertragen oder darstellen. **[\<=]**

##### TIP1-A_5648

Der Hersteller des Konnektors MUSS die zur Nutzung der
Remote-Managemenschnittstelle notwendigen Informationen offenlegen. Der
Hersteller des Konnektors MUSS die Remote-Managementschnittstelle so
spezifizieren und implementieren, dass diese auch für Dritte (z.B. einen durch
den Anwender beauftragten Servicepartner) nutzbar ist. **[\<=]**

##### TIP1-A_5649

Der Hersteller des Konnektors SOLL für die Implementierung der
Remote-Managementschnittstelle standardbasierte Verfahren und Protokolle
einsetzen. **[\<=]**

##### TIP1-A_5650

Der Konnektor MUSS sicherstellen, dass die Initiierung einer
Remote-Managementverbindung im Sinne des Verbindungsaufbaus immer vom Konnektor
ausgeht. **[\<=]**

##### TIP1-A_5651

Der Konnektor MUSS die Remote-Management-Verbindung durch Nutzung eines
kryptographischen Verfahrens gemäß [gemSpec_Krypt] hinsichtlich
Vertraulichkeit, Integrität und Authentizität absichern. **[\<=]**

Das Remote-Management-System authentisiert sich auf Transportebene
zertifikatsbasiert gegenüber dem Konnektor.

##### TIP1-A_7277

Der Konnektor MUSS eine zertifikatsbasierte Authentifizierung des
Remote-Management-Systems auf Transportebene durchführen. **[\<=]**

##### TIP1-A_7278

Der Konnektor MUSS sich gegenüber dem Remote-Management-System
zertifikatsbasiert oder mittels Username/Password authentisieren. **[\<=]**

##### TIP1-A_7281

Das Remote-Management-System MUSS eine Authentifizierung des Konnektors
durchführen. **[\<=]**

Die Authentifizierung des Remote-Management-Systems durch den Konnektor auf
Transportebene ist verpflichtend gefordert.

Darüber hinaus können optional Remote-Administratoren in der
Benutzerverwaltung des Konnektors konfiguriert werden. Wenn
Remote-Administratoren in der Benutzerverwaltung konfiguriert sind, muss der
Konnektor diese verpflichtend auf Anwendungsebene authentifizieren.  

Wenn kein Remote-Administrator konfiguriert ist, vertraut der Konnektor der
Benutzerverwaltung des Remote-Management-Systems. Auch wenn die Verwaltung von
Remote-Administratoren an das Remote-Management-System delegiert ist, werden
alle Zugriffe über das Remote-Management-System auf den Konnektor mit der
Rolle Remote-Administrator ausgeführt. Das Remote-Management-System muss die
Authentisierung der Remote-Administratoren und die Nachvollziehbarkeit der
Zugriffe sicherstellen.

##### TIP1-A_7279

Wenn in der Benutzerverwaltung des Konnektors Administratoren mit der
Administrator-Rolle Remote-Administrator konfiguriert sind, MUSS der Konnektor
diese gemäß TIP1-A_4808 authentifizieren. **[\<=]**

##### TIP1-A_7280

Der Konnektor DARF Remote-Administratoren Rechte gemäß TAB_KON_851 und
TAB_KON_655 NICHT gewähren. **[\<=]**

 ---> TABLE

##### TIP1-A_5652

Der Konnektor MUSS sicherstellen, dass es ausschließlich einem Administrator
mit einer der Rollen {Lokaler Administrator; Super-Administrator} und dem Recht
USER_INIT_REMOTESESSION möglich ist, Konfigurationsänderungen gemäß
TAB_KON_663 vorzunehmen.

Tabelle369: TAB_KON_663 Konfigurationen des Remote Managements

 ---> TABLE

​​ **[\<=]**

##### TIP1-A_5653

Der Konnektor MUSS im Rahmen des Remote-Managements folgende Aktionen
protokollieren:

 ---> UL

**[\<=]**

Ein Softwareupdate gemäß TIP1-A_5657 kann auch über das Remote Management
initiiert, aktiviert und freigeschaltet werden.

### 4.3.10 Software- und Konfigurationsaktualisierung (KSR-Client)

Die Umsetzung des KSR-Clients bezüglich des Mechanismus zur Durchführung der
Aktualisierungen, sowie die Art der Darstellung an der Managementschnittstelle
sind herstellerspezifisch.

Innerhalb der Software- und Konfigurationsaktualisierung (KSR-Client) werden
folgende Präfixe für Bezeichner verwendet:

 ---> UL

### 4.3.10.1 Funktionsmerkmalweite Aspekte

Der Konnektor muss einen KSR-Client bereitstellen, über den der Administrator
sowohl den Konnektor selbst als auch die vom Konnektor verwalteten
Kartenterminals (CT-Objects in CTM_CT_LIST mit CT.CORRELATION\>=„gepairt“
und CT.VALID_VERSION=True und CT.IS_PHYSICAL = Ja) softwareseitig aktualisieren
kann.

Weiterhin muss über den KSR-Client eine Aktualisierung von ausgewählten
Konfigurationsdaten möglich sein.

##### TIP1-A_4829

DieSoftware-AktualisierungdesKonnektor SOLL sicherstellen, dass alle
Software-Bestandteile des Konnektors aktualisiert werden können, damit eine
ungehinderte Nachnutzung der Hardware-Basis im Feld mit neuen Funktionalitäten
nicht durch nichtaktualisierbare Software-Bestandteile gefährdet wird. Weicht
ein Hersteller für sein Konnektormodell von dieser Forderung in Teilen ab, so
MUSS er im Rahmender Zulassung nachweisen, dass dies auf Grund von
Sicherheitsaspekten für sein eingereichtes Konnektormodell zwingend
erforderlich ist. **[\<=]**

##### TIP1-A_5657-02

Der Konnektor MUSS die Möglichkeit bieten, dass Softwareupdates durch den
Nutzer bzw. einen von ihm beauftragten Administrator einzeln freigeschaltet
werden. **[\<=]**

##### A_18387

Der Konnektor MUSS die Möglichkeit bieten, die automatische Installation von
Softwareupdates pro Gerät (Konnektor und Kartenterminals) ein- und
auszuschalten. **[\<=]**

##### A_18389

Der Hersteller des Konnektors MUSS in seinem Handbuch den Nutzer darauf
hinweisen, dass er sich bei der Arbeit mit dem Konnektor vergewissern muss,
dass er mit einer zugelassenen Version arbeitet und beschreiben, wie der Nutzer
diese Information mittels seines Primärsystems erhalten kann. **[\<=]**

##### TIP1-A_6476

Der Hersteller des Konnektors MUSS jede zugelassene Firmware-Version umgehend
als Update-Paket über die in [gemSpec_KSR] definierte Schnittstelle
P_KSRS_Upload im Konfigurationsdienst (KSR) ablegen.

Der Hersteller des Konnektors MUSS in den jeweiligen
UpdateInformation/Firmware/FirmwareReleaseNotes eine Internet-URL zum Download
des FW-Updates bereitstellen. **[\<=]**

##### TIP1-A_6026

Das Managementinterface des Konnektors MUSS einem authentisierten Administrator
die Internet-URL zum Download des FW-Updates anzeigen. **[\<=]**

### 4.3.10.2 Durch Ereignisse ausgelöste Reaktionen

##### TIP1-A_4831

Wenn aus (TIP1-A_4840 Auslösen der durchzuführenden Updates) heraus für ein
Kartenterminal noch ein ausstehendes Updates vorhanden ist, dessen
Ausführungszeitpunkt nicht gesetzt oder überschritten ist, und für dieses
Kartenterminal das Ereignis „CT/CONNECTED“eintritt, so MUSS TUC_KON_281
„Kartenterminalaktualisierung anstoßen“für dieses KT gerufen werden. **[\<=]**

### 4.3.10.3 Interne TUCs, nicht durch Fachmodule nutzbar

### 4.3.10.3.1 TUC_KON_280 „Konnektoraktualisierung durchführen“

##### TIP1-A_4832-02

Der Konnektor MUSS den technischen Use Case TUC_KON_280
„Konnektoraktualisierung durchführen“ umsetzen.

Tabelle370: TAB_KON_664 – TUC_KON_280 „Konnektoraktualisierung
durchführen“

 ---> TABLE

Tabelle371: TAB_KON_665 Fehlercodes TUC_KON_280 „Konnektoraktualisierung
durchführen“

 ---> TABLE

![Img-022][Img-022]

Abbildung22: PIC_KON_105 Aktivitätsdiagramm Konnektoraktualisierung
durchführen   **[\<=]**

### 4.3.10.3.2 TUC_KON_281 „Kartenterminalaktualisierung anstoßen“

Im Vergleich zur Durchführung des Konnektor-Update (TUC_KON_280), werden die
Updates der Kartenterminals nur durch den Konnektor initiiert. Der Konnektor
liefert dem Kartenterminal das Updatefile, der eigentliche Updatevorgang
(inklusive der Prüfung des Updatepakets auf Integrität und Authentizität)
erfolgt ausschließlich und eigenverantwortlich auf Seiten des Kartenterminals.

##### TIP1-A_4833-02

Der Konnektor MUSS den technischen Use Case TUC_KON_281
„Kartenterminalaktualisierung anstoßen“ umsetzen.

Tabelle372: TAB_KON_666 – TUC_KON_281 „Kartenterminalaktualisierung
anstoßen“

 ---> TABLE

Tabelle373: TAB_KON_667 Fehlercodes TUC_KON_281 „Kartenterminalaktualisierung
anstoßen“

 ---> TABLE

**[\<=]**

### 4.3.10.3.3 TUC_KON_282 „UpdateInformationen beziehen“

##### TIP1-A_4834

Der Konnektor MUSS den technischen Use Case TUC_KON_282 „UpdateInformationen
beziehen“ umsetzen.

Tabelle374: TAB_KON_668 – TUC_KON_282 „UpdateInformationen beziehen“

 ---> TABLE

Tabelle375: TAB_KON_669 Fehlercodes TUC_KON_282 „UpdateInformationen
beziehen“

 ---> TABLE

**[\<=]**

### 4.3.10.3.4 TUC_KON_283 „Infrastruktur Konfiguration aktualisieren“

##### TIP1-A_5153

Der Konnektor MUSS den technischen Use Case TUC_Kon_283 „Infrastruktur
Konfiguration aktualisieren“ umsetzen.

Tabelle376: TAB_KON_799 – TUC_KON_283 „Infrastruktur Konfiguration
aktualisieren“

 ---> TABLE

Tabelle377: Tab_Kon_726 Fehlercodes TUC_KON_283 „Infrastruktur Konfiguration
aktualisieren“

 ---> TABLE

**[\<=]**

### 4.3.10.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.3.10.4.1 TUC_KON_285 „UpdateInformationen für Fachmodul beziehen“

##### TIP1-A_6018

Der Konnektor MUSS den technischen Use Case TUC_KON_285 „UpdateInformationen
für Fachmodul beziehen“ umsetzen.

Tabelle378: TAB_KON_833 – TUC_KON_285 „UpdateInformationen für Fachmodul
beziehen“

 ---> TABLE

Tabelle379: TAB_KON_834 Fehlercodes TUC_KON_285 „UpdateInformationen für
Fachmodul beziehen“

 ---> TABLE

**[\<=]**

### 4.3.10.4.2 TUC_KON_286 „Paket für Fachmodul laden“

##### TIP1-A_6019

Der Konnektor MUSS den technischen Use Case TUC_KON_286 „Paket für Fachmodul
laden“ umsetzen.

Tabelle380: TAB_KON_835 – TUC_KON_286 „Paket für Fachmodul laden“

 ---> TABLE

Tabelle381: TAB_KON_836 Fehlercodes TUC_KON_286 „Paket für Fachmodul laden“

 ---> TABLE

**[\<=]**

### 4.3.10.5 Operationen an der Außenschnittstelle

Keine.

### 4.3.10.6 Betriebsaspekte

##### A_21899

Der Konnektor DARF NICHT nach einer Aktualisierung der Datei Bestandsnetze.xml
einen Restart durchführen. **[\<=]**

##### A_21900

Der Konnektor MUSS die Anzahl der Reboots minimieren. **[\<=]**

### 4.3.10.6.1 TUC_KON_284 KSR-Client initialisieren

##### TIP1-A_5938

Der Konnektor MUSS in der Bootup-Phase TUC_KON_284 „KSR-Client
initialisieren“ durchlaufen.

Tabelle382: TAB_KON_864 – TUC_KON_284 „KSR-Client initialisieren“

 ---> TABLE

Tabelle383: TAB_KON_822 Fehlercodes TUC_KON_284 „KSR-Client initialisieren“

 ---> TABLE

**[\<=]**

##### TIP1-A_4835-02

Der Administrator MUSS die in TAB_KON_670 aufgelisteten Parameter über die
Managementschnittstelle konfigurieren und die in TAB_KON_820 aufgelisteten
Parameter ausschließlich einsehen können.

Tabelle384: TAB_KON_670 Konfigurationsparameter der Software-Aktualisierung

 ---> TABLE

Tabelle385: TAB_KON_820 Einsehbare Konfigurationsparameter der
Software-Aktualisierung

 ---> TABLE

**[\<=]**

Hinweis: Die Adressen des Konfigurationsdienstes werden im Rahmen des
VPN-Verbindungsaufbaus ermittelt (siehe [gemSpec_VPN_ZugD#5.1.1.2
TUC_VPN-ZD_0001])

##### TIP1-A_6025

Der Konnektor MUSS täglich überprüfen, ob unter den auf die aktuelle
Konnektor-Firmware anwendbaren Updates  ein Update mit FWPriority =
„Kritisch“ ist, dessen Deadline
(entsprichtUpdateInformation/DeploymentInformation/Deadline) abgelaufen ist,
d.h. Deadline \<= Systemzeit. In diesem Fall MUSS der Konnektor den
Verbindungsaufbau zur TI Plattform verhindern, bestehende Verbindungen in die
TI abbauen und den kritischen Betriebszustand EC_FW_Not_Valid_Status_Blocked
annehmen. **[\<=]**

##### TIP1-A_4836

Der Konnektor MUSS täglich die folgenden Schritte durchführen:

 ---> OL

TUC_KON_256 „Systemereignis absetzen“ {

        topic = „KSR/UPDATE/KONNEKTOR_DOWNLOAD_END“;

        eventType = Op;     

        severity = Info;     

        parameters  = (\<Param\>)}    

informieren. Je heruntergeladenem FW-Paket MUSS \<Param\> mit folgenden Werten
belegt sein:    

\<Param\> =     „ProductVendorID= $UpdateInformation/ProductVendorID;

                     ProductCode=
$UpdateInformation/ProductCode;

                    
ProductName=$UpdateInformation/ProductName;

                    
FirmwareVersion=$UpdateInformation/Firmware/FWVersion;

                    
Deadline=$UpdateInformation/DeploymentInformation/Deadline;

                    

FWPriority

=$UpdateInformation/Firmware/

FWPriority;

                     F

irmwareReleaseNotes

                                    
=$UpdateInformation/Firmware/FirmwareReleaseNotes“

 ---> OL

Der Konnektor MUSS immer nur die neusten Update-Pakete für eine Nutzung
vorhalten. Eventuell vorhandene ältere, nicht genutzte Update-Pakete KÖNNEN
überschrieben werden. **[\<=]**

##### TIP1-A_4836-02

Der Konnektor MUSS täglich die folgenden Schritte durchführen:

 ---> OL

TUC_KON_256 „Systemereignis absetzen“ {

        topic = „KSR/UPDATE/KONNEKTOR_DOWNLOAD_END“;

        eventType = Op;     

        severity = Info;     

        parameters  = (\<Param\>)}    

informieren. Je heruntergeladenem FW-Paket MUSS \<Param\> mit folgenden Werten
belegt sein:    

\<Param\> =     „ProductVendorID= $UpdateInformation/ProductVendorID;

                     ProductCode=
$UpdateInformation/ProductCode;

                    
ProductName=$UpdateInformation/ProductName;

                    
FirmwareVersion=$UpdateInformation/Firmware/FWVersion;

                    
Deadline=$UpdateInformation/DeploymentInformation/Deadline;

                    
FWPriority=$UpdateInformation/Firmware/FWPriority;

                     FirmwareReleaseNotes

                                    
=$UpdateInformation/Firmware/FirmwareReleaseNotes“

 ---> OL

Der Konnektor MUSS immer nur die neusten Update-Pakete für eine Nutzung
vorhalten. Eventuell vorhandene ältere, nicht genutzte Update-Pakete KÖNNEN
überschrieben werden.

Nach einem erfolgreichen Download DÜRFEN die Namen der Dateien eines
Update-Paketes beim Abspeichern NICHT verändert werden. **[\<=]**

##### TIP1-A_7220

Der Konnektor KANN für den Download von Update-Paketen über
I_KSRS_Download::get_Updates die Option Range Requests [RFC7233#3.1] zur
Fortsetzung von unterbrochenen Transfers nutzen. **[\<=]**

##### TIP1-A_4837

Die Administrationsoberfläche desKSR-Clients MUSS dem Administrator eine
Übersichtseite anbieten, die einen Geräteeintrag für den Konnektor selbst,
sowie eine Liste von Geräteeinträgen für jedes Kartenterminal (CT) aus
CTM_CT_LIST mit CT.IS_PHYSICAL=Ja und CT.CORRELATION\>=„gepairt“enthält.

Der Administrator MUSS die Liste der Kartenterminals nach Kartenterminalmodellen
gruppieren können (gleiche Werte für ProductVendorID,ProductCode,
HardwareVersion und FirmwareVersion).

Je Geräteeintrag MÜSSEN die über „Automatische Prüfung und Download
vonUpdate-Paketen“ ermittelten listUpdatesResponse bereitstehen.

Je Geräteeintrag MUSS die Version der aktuell installierten Software
dargestellt werden. Sind Bestandteile der installierten Software unabhängig
aktualisierbar, so MUSS für jedes der Bestandteile die Version angezeigt
werden.

Der Administrator MUSS eine Aktualisierung aller listUpdatesResponse über
TUC_KON_282 „UpdateInformationen beziehen“ auslösen können.

Geräteeinträge, die über listUpdatesResponse mit neuerer Firmwareversion als
das zugehörige Gerät verfügen, MÜSSEN hervorgehoben werden.

Je Geräteeintrag MUSS die Zugehörigkeit der installierten Software und der
Software-Updates zum Online-Produktivbetrieb oder zu einer Erprobung (inklusive
Name der Erprobung) dargestellt werden. **[\<=]**

##### TIP1-A_4838

Für alle Geräteeinträge MUSS der Administrator zu den listUpdatesResponse
sowohl die FirmwareGroupReleaseNotes als auch jedes enthaltene
UpdateInformation-Element einsehen können. Dazu MUSS der Konnektor

 ---> UL

**[\<=]**

##### TIP1-A_4839-01

Der Administrator MUSS in der Übersichtsliste einzelne Geräteeinträge bzw.
Gruppen mit der jeweils anzuwendenden UpdateInformation für die Durchführung
eines Updates markieren können.Alternativ MUSS der Administrator neben der
Markierung je Geräteeintrag bzw. Gruppe Update-Pakete lokal einspielen können
(etwa durch ein Upload- bzw. Download-Interface in der
Administrationsoberfläche).Je Geräteeintrag MUSS der Administrator einen
individuellen Ausführungszeitpunkt für die Durchführung des Updates
einstellen können.Der Administrator MUSS für den Geräteeintrag Konnektor
festlegen können, ob dieses Update erst gestartet werden darf, wenn zuvor alle
festgelegten KT-Updates erfolgreich durchlaufen wurden.Der Administrator MUSS
zu jeder Zeit die gerätebezogene Festlegung für ein Update ändern bzw.
löschen können, sofern dieses konkrete Update noch nicht begonnen wurde.Je
Geräteeintrag MUSS der Administrator automatische Softwareupdates aktivieren
und deaktivieren können. **[\<=]**

##### TIP1-A_4840-01

Der Administrator MUSS für die Liste der markierten Geräteeinträge ein
gesammeltes Update auslösen können. Dieses MUSS nach folgendem Muster
ablaufen:

 ---> OL

 ---> UL

 ---> OL

 ---> UL

Wenn der Administrator ein Erprobungs-Update zur Installation auswählt, MUSS er
über einen Warnhinweis darüber informiert werden,

 ---> UL

dass, falls die Institution oder Organisation des Gesundheitswesens nicht an der
Erprobung teilnimmt und dennoch das Update installiert wird, es zu funktionalen
Einschränkungen des Konnektors kommen kann. **[\<=]**

##### A_18390

Wenn für mindestens ein Gerät das automatische Softwareupdate aktiviert ist,
MUSS der Konnektor zur MGM_KSR_AUTO_UPDATE_TIME die Updates nach folgendem
Muster durchführen:

 ---> UL

**[\<=]**

##### A_18391

Sofern der Konnektor zu MGM_KSR_AUTO_UPDATE_TIME nicht in Betrieb war, DÜRFEN
die automatischen Updates später NICHT nachgeholt werden. **[\<=]**

##### A_18779

Wenn mit einem Update erstmalig MGM_KSR_AUTO_UPDATE=Enabled aktiv wird, MUSS der
Konnektorhersteller über das entsprechende KSR-Paket den Admin an der
Konnektor Oberfläche darauf hinweisen, dass mit diesem Update der automatische
Softwareupdate aktiv wird. **[\<=]**

##### A_20531

Der Konnektor MUSS eine Bestandsnetze.xml mit einer Größe von mindestens 3
MByte und 2000 Netzen (XML Element \<Network\>) verarbeiten können. **[\<=]**

### 4.3.11 Konnektorstatus

##### TIP1-A_5542

Der Konnektor MUSS an der Managementschnittstelle eine Funktion anbieten, die es
ermöglicht die Erreichbarkeit von Systemen durch Eingabe der IP-Adresse oder
des FQDN zu prüfen. Das Ergebnis des Tests MUSS angezeigt werden. **[\<=]**

##### A_23276

Der Konnektor MUSS dem Administrator an der Management-Oberfläche automatisch
die Erreichbarkeit und die FQDNs von folgenden Systemen und ggf. ihren
Backupservern anzeigen:

 ---> UL

**[\<=]**

### 4.4 Hardware-Merkmale des Konnektors

##### TIP1-A_4841

Der Konnektor MUSS sowohl in seiner Stromversorgung als auch in seinen
restlichen Hardwarekomponenten auf einen 24x7-Dauerbetrieb ausgelegt sein.

Der Hersteller DARF NICHT davon ausgehen oder gar in seiner Guidance darauf
verweisen, dass der Konnektor mehrere Stunden am Tag nicht betrieben wird. **[\<=]**

Diese Anforderung verlangt keinen Schutz gegen Stromausfall in den
Betriebsräumen.

##### TIP1-A_4842

Jeder Konnektor, der als Appliance (dezidierte, geschlossene Kombination aus
spezifischer Hard- und Software) ausgeprägt ist,MUSS über eine
fälschungssichere Gehäuseversiegelung verfügen. Die Versiegelung MUSS so
angebracht werden, dass eine Öffnung des Gehäuses nicht ohne Beschädigung
des Siegels erfolgen kann.

Der Konnektor MUSS die Umsetzung entsprechend der Festlegungen für das
Kartenterminal nach der TR-03120 [BSI TR-03120], Kapitel bzgl.
Gehäuseversiegelung 9 vornehmen.

Die optische Gestaltung der Siegel ist herstellerspezifisch. **[\<=]**

Die Prüfung auf Einhaltung der Versiegelungsvorgaben erfolgt nicht im Rahmen
der CC-Evaluierung, sondern im Zuge der Prüfung auf funktionale Eignung.

##### TIP1-A_4843

Im Betrieb MUSS der Zustand des Konnektors erkennbar sein. Zur Anzeige des
Betriebszustandes des Konnektors SOLL es eine Signaleinrichtung (z. B. über
Status-LEDs) am Konnektor geben. Falls keine Signalvorrichtung am
Konnektorgehäuse verwendet wird MUSS es eine softwareseitige Lösung über das
Managementinterface geben. Bei verbauter Hardware-Signalgebung KANN eine
softwareseitige Lösung zusätzlich angeboten werden.Es MÜSSEN mindestens
folgende angezeigt werden:

 ---> UL

Es SOLLEN folgende Zustände angezeigt werden:

 ---> UL

**[\<=]**

##### TIP1-A_4844-02

Der Konnektor MUSS mindestens zwei Ethernetinterfaces nach [IEEE802.3] als
physikalische Schnittstellen zur Verfügung stellen. **[\<=]**

##### TIP1-A_4845

Als normaler Einsatzort wird für den Konnektor ein Büroraum angenommen. Der
Konnektor MUSS die in Tabelle TAB_KON_671 aufgeführten Anforderungen
erfüllen, welche unter der Annahme des normalen Einsatzortes erhoben werden.

Tabelle386: TAB_KON_671 Anforderungen Klima

 ---> TABLE

**[\<=]**

##### TIP1-A_4846

Die durch Vibrationen und mechanische Schockbelastungen auftretenden Belastungen
MÜSSEN vom Konnektor schadensfrei gemäß IEC 68-2 Methode nach den
Anforderungen aus TAB_KON_672 absolviert, geprüft und nachgewiesen werden.

Tabelle387: TAB_KON_672 Anforderungen Vibration

 ---> TABLE

**[\<=]**

##### TIP1-A_4846-02

Die durch Vibrationen und mechanische Schockbelastungen auftretenden Belastungen
MÜSSEN vom Konnektor schadensfrei gemäß IEC 68-2 Methode nach den
Anforderungen aus TAB_KON_672 absolviert, geprüft und nachgewiesen werden.

Tabelle388: TAB_KON_672 Anforderungen Vibration

 ---> TABLE

**[\<=]**

### 5 Anhang A – Verzeichnisse

### 5.1 Abkürzungen

 ---> TABLE

### 5.2 Glossar

 ---> TABLE

Das Glossar wird als eigenständiges Dokument, vgl. [gemGlossar] zur Verfügung
gestellt.

### 5.3 Abbildungsverzeichnis

- [Abbildung-1] - PIC_KON_116 Schnittstellen des Konnektors von und zu anderen Produkttypen
- [Abbildung-2] - PIC_KON_117 Logische Zerlegung des Konnektors in Anwendungs- und Netzkonnektor
- [Abbildung-3] - PIC_KON_107 XML-Struktur des Status-Elements einer SOAP-Antwort
- [Abbildung-4] - PIC_Kon_100 Informationsmodell des Konnektors
- [Abbildung-5] - PIC_KON_101 Aufrufkontext der Operation
- [Abbildung-6] - PIC_KON_118 Aktivitätsdiagramm zu „TUC_KON_000 Prüfe Zugriffsberechtigung“
- [Abbildung-7] - PIC_KON_071 Korrelationszustände eines eHealth-KT
- [Abbildung-9] - PIC_KON_057 Aktivitätsdiagramm zu „PaireKartenterminal“
- [Abbildung-13] - PIC_KON_058 Aktivitätsdiagramm „Daten hybrid verschlüsseln“
- [Abbildung-15] - PIC_KON_103 Use Case Diagramm Signaturdienst (nonQES)
- [Abbildung-16] - PIC_KON_104 Use Case Diagramm Signaturdienst (QES)
- [Abbildung-17] - PIC_KON_102
- [Abbildung-20] - PIC_KON_118 Aufbau und Struktur der Protokolldateien für Plattform und Fachmodule
- [Abbildung-21] - PIC_KON_115 Kommunikationsregeln Konnektor
- [Abbildung-23] - PIC_KON_120 Abbildung von CardSessions auf logische Kanäle
- [Abbildung-24] -  Szenario einer einfachen Installation
- [Abbildung-25] - Szenario einer Installation mit mehreren Behandlungsräumen
- [Abbildung-26] - Szenario einer Integration der TI Produkte in eine bestehende Infrastruktur
- [Abbildung-27] - Szenario einer Integration der TI Produkte in eine bestehende Infrastruktur mit existierendem Router
- [Abbildung-28] - Szenario mit zentral gesteckten HBA und SMC-B
- [Abbildung-29] - Szenario mit zentralem Primärsystem als Clientsystem
- [Abbildung-30] - Szenario für den Zugriff
- [Abbildung-31] -   Standalone-Szenario mit physischer Trennung im Konnektor

### 5.4 Tabellenverzeichnis

- [Tabelle-1] - Fehlercodes TAB_KON_890 Mindestanforderungen an Dokumente und Nachrichten
- [Tabelle-2] - Fehlercodes TAB_KON_891 Unerlaubte Inhalte in Dokumenten und Nachrichten
- [Tabelle-3] - TAB_KON_500 Wertetabelle Kartentypen
- [Tabelle-4] - TAB_KON_856: Identitäten des Konnektors auf der gSMC-K
- [Tabelle-5] - TAB_KON_503 Betriebszustand_Fehlerzustandsliste
- [Tabelle-6] - TAB_KON_504 Ausführungserlaubnis für Dienste in kritischen Fehlerzuständen
- [Tabelle-7] - TAB_KON_502 Fehlercodes „Betriebszustand“
- [Tabelle-9] - TAB_KON_852 Konfigurationsvarianten der Verbindungen zwischen Konnektor und Clientsystemen
- [Tabelle-10] - TAB_KON_865-01 Konfigurationsvarianten der Verbindungen zwischen Konnektor und Clientsystemen bei LDAP
- [Tabelle-11] - TAB_KON_506-01 Konfigurationsparameter der Clientsystem-Authentisierung
- [Tabelle-12] - TAB_KON_812 Umgebungsabhängige Konfigurationsparameter
- [Tabelle-13] - TAB_KON_507 Informationsmodell Entitäten
- [Tabelle-14] - TAB_KON_508 Informationsmodell Attribute
- [Tabelle-15] - TAB_KON_509 Informationsmodell Entitätenbeziehungen
- [Tabelle-16] - TAB_KON_510 Informationsmodell Constraints
- [Tabelle-17] - TAB_KON_511-01 – TUC_KON_000 „Prüfe Zugriffsberechtigung“
- [Tabelle-18] - TAB_KON_512 Zugriffsregeln Beschreibung
- [Tabelle-19] - TAB_KON_513 Zugriffsregeln Regelzuordnung
- [Tabelle-20] - TAB_KON_514-01 Zugriffsregeln Definition
- [Tabelle-21] - TAB_KON_515 Fehlercodes TUC_KON_000 „Prüfe Zugriffsberechtigung“
- [Tabelle-22] - TAB_KON_143 – TUC_KON_080 „Dokument validieren“
- [Tabelle-23] - TAB_KON_144 Fehlercodes TUC_KON_080 „Dokument validieren“
- [Tabelle-24] - TAB_KON_516 Basisanwendung Dienstverzeichnisdienst
- [Tabelle-26] - TAB_KON_518 Schemabeschreibung Serviceinformation (Serviceinformation.xsd)
- [Tabelle-27] - TAB_KON_519 - TUC_KON_041 „Einbringen der Endpunktinformationen während der Bootup-Phase“
- [Tabelle-28] - TAB_KON_520 Fehlercodes TUC_KON_041 „Einbringen der Endpunktinformationen während der Bootup-Phase“
- [Tabelle-30] - TAB_KON_522 Parameterübersicht des Kartenterminaldienstes
- [Tabelle-31] - TAB_KON_785 Erlaubte SICCT-Kommandos bei CT.CONNECTED=Nein
- [Tabelle-32] - TAB_KON_727 Terminalanzeigen beim Anfordern und Auswerfen von Karten
- [Tabelle-33] - TAB_KON_039 – TUC_KON_050 „Beginne Kartenterminalsitzung“
- [Tabelle-34] - TAB_KON_523 Fehlercodes TUC_KON_050 „Beginne Kartenterminalsitzung“
- [Tabelle-35] - TAB_KON_524 – TUC_KON_054 „Kartenterminal hinzufügen“
- [Tabelle-36] - TAB_KON_525 Fehlercodes TUC_KON_054 „Kartenterminal hinzufügen“
- [Tabelle-37] - TAB_KON_041 – TUC_KON_053 „Paire Kartenterminal“
- [Tabelle-38] - TAB_KON_113 Fehlercodes TUC_KON_053 „Paire Kartenterminal“
- [Tabelle-39] - TAB_KON_526 – TUC_KON_055 „Befülle CT-Object“
- [Tabelle-40] - TAB_KON_112 – TUC_KON_051 „Mit Anwender über Kartenterminal interagieren“
- [Tabelle-41] - TAB_KON_114 Fehlercodes TUC_KON_051 „Mit Anwender über Kartenterminal interagieren“
- [Tabelle-42] - TAB_KON_723 - TUC_KON_056 „Karte anfordern“
- [Tabelle-43] - TAB_KON_724 Fehlercodes TUC_KON_056 „Karte anfordern“
- [Tabelle-44] - TAB_KON_725 – TUC_KON_057 „Karte auswerfen“
- [Tabelle-45] - TAB_KON_796 Fehlercodes TUC_KON_057 „Karte auswerfen“
- [Tabelle-46] - TAB_KON_854 – TUC_KON_058 „Displaygröße ermitteln“
- [Tabelle-47] - TAB_KON_855 Fehlercodes TUC_KON_058 „Displaygröße ermitteln“
- [Tabelle-48] - TAB_KON_722 Basisdienst Kartenterminaldienst
- [Tabelle-49] - TAB_KON_716 Operation RequestCard
- [Tabelle-50] - TAB_KON_717 Ablauf RequestCard
- [Tabelle-51] - TAB_KON_718 Fehlercodes „RequestCard“
- [Tabelle-52] - TAB_KON_719 Operation EjectCard
- [Tabelle-53] - TAB_KON_720 Ablauf EjectCard
- [Tabelle-54] - TAB_KON_721 Fehlercodes Operation „EjectCard“
- [Tabelle-55] - TAB_KON_527 Konfigurationswerte eines Kartenterminalobjekts
- [Tabelle-56] - TAB_KON_528 Informationsparamter des Kartenterminaldienstes
- [Tabelle-57] - TAB_KON_529 Anzeigewerte zu einem Kartenterminalobjekt
- [Tabelle-58] - TAB_KON_530 Konfigurationswerte eines Kartenterminalobjekts
- [Tabelle-59] - TAB_KON_531 Parameterübersicht des Kartendienstes
- [Tabelle-60] - TAB_KON_090 Terminalanzeigen beim Eingeben der PIN am Kartenterminal
- [Tabelle-61] - TAB_KON_734 – TUC_KON_001 „Karte öffnen“
- [Tabelle-62] - TAB_KON_735 - TUC_KON_026
- [Tabelle-63] - TAB_KON_824 Fehlercodes TUC_KON_026 „Liefere CardSession“
- [Tabelle-64] - TAB_KON_087 – TUC_KON_012 „PIN verifizieren“
- [Tabelle-65] - TAB_KON_089 Fehlercodes TUC_KON_012 „PIN verifizieren“
- [Tabelle-66] - TAB_KON_736 – TUC_KON_019 „PIN ändern“
- [Tabelle-67] - TAB_KON_093 Fehlercodes TUC_KON_019 „PIN ändern“
- [Tabelle-68] - TAB_KON_236 – TUC_KON_021 „PIN entsperren“
- [Tabelle-69] - TAB_KON_193 Fehlercodes TUC_KON_021 „PIN entsperren“
- [Tabelle-70] - TAB_KON_532 – TUC_KON_022 „Liefere PIN-Status“
- [Tabelle-71] - TAB_KON_091 Fehlercodes TUC_KON_022 „Liefere PIN-Status“
- [Tabelle-72] - TAB_KON_240 - TUC_KON_027 „PIN-Schutz ein-/ausschalten”
- [Tabelle-73] - TAB_KON_838 Mapping von pinRef auf ANW
- [Tabelle-74] - TAB_KON_241 Fehlercodes TUC_KON_027 „PIN-Schutz ein/ausschalten“
- [Tabelle-75] - TAB_KON_533 - TUC_KON_023 „Karte reservieren”
- [Tabelle-76] - TAB_KON_534 Fehlercodes TUC_KON_023 „Karte reservieren“
- [Tabelle-77] - TAB_KON_096 – TUC_KON_005 „Card-to-Card authentisieren”
- [Tabelle-78] - TAB_KON_673 AuthMode für C2C
- [Tabelle-79] - TAB_KON_674 Erlaubte Parameterkombinationen und resultierende CV-Zertifikate für C2C
- [Tabelle-80] - TAB_KON_535 Fehlercodes TUC_KON_005 „Card-to-Card authentisieren“
- [Tabelle-81] - TAB_KON_218 – TUC_KON_202 „LeseDatei“
- [Tabelle-82] - TAB_KON_536 Fehlercodes TUC_KON_202 „LeseDatei“
- [Tabelle-83] - TAB_KON_219 – TUC_KON_203 „SchreibeDatei“
- [Tabelle-84] - TAB_KON_537 Fehlercodes TUC_KON_203 „Schreibe Datei“
- [Tabelle-85] - TAB_KON_204 – TUC_KON_204 „LöscheDateiInhalt“
- [Tabelle-86] - TAB_KON_785 Fehlercodes TUC_KON_204 „LöscheDateiInhalt“
- [Tabelle-87] - TAB_KON_538 – TUC_KON_209 „LeseRecord“
- [Tabelle-88] - TAB_KON_539 Fehlercodes TUC_KON_209 „LeseRecord“
- [Tabelle-89] - TAB_KON_224 – TUC_KON_210 „SchreibeRecord“
- [Tabelle-90] - TAB_KON_540 Fehlercodes TUC_KON_210 „SchreibeRecord“
- [Tabelle-91] - TAB_KON_211 – TUC_KON_211 „LöscheRecordInhalt“
- [Tabelle-92] - TAB_KON_786 Fehlercodes TUC_KON_211 „LöscheRecordInhalt“
- [Tabelle-93] - TAB_KON_228 – TUC_KON_214 „FügeHinzuRecord“
- [Tabelle-94] - TAB_KON_541 Fehlercodes TUC_KON_214 „FügeHinzuRecord“
- [Tabelle-95] - TAB_KON_229 – TUC_KON_215 „SucheRecord“
- [Tabelle-96] - TAB_KON_542 Fehlercodes TUC_KON_215 „SucheRecord“
- [Tabelle-97] - TAB_KON_110 - TUC_KON_018 „eGK-Sperrung prüfen“
- [Tabelle-98] - TAB_KON_239 Fehlercodes TUC_KON_018 „eGK-Sperrung prüfen“
- [Tabelle-99] - TAB_KON_108 - TUC_KON_006 „Datenzugriffsaudit eGK schreiben“
- [Tabelle-100] - TAB_KON_238 Fehlercodes TUC_KON_006 „Datenzugriffsaudit eGK schreiben“
- [Tabelle-101] - TAB_KON_231 – TUC_KON_218 „Signiere“
- [Tabelle-102] - TAB_KON_543 Fehlercodes TUC_KON_218 „Signiere“
- [Tabelle-103] - TAB_KON_232 – TUC_KON_219 „Entschlüssele“
- [Tabelle-104] - TAB_KON_210 Fehlercodes TUC_KON_219 „Entschlüssele“
- [Tabelle-105] - TAB_KON_215 TUC_KON_200 „SendeAPDU“
- [Tabelle-106] - TAB_KON_216 Fehlercodes TUC_KON_200 „SendeAPDU“
- [Tabelle-107] - TAB_KON_737 – TUC_KON_024 „Karte zurücksetzen“
- [Tabelle-108] - TAB_KON_544 Fehlercodes TUC_KON_024 „Karte zurücksetzen“
- [Tabelle-109] - TAB_KON_230 – TUC_KON_216 „LeseZertifikat“
- [Tabelle-110] - TAB_KON_209 Fehlercodes TUC_KON_216 „LeseZertifikat“
- [Tabelle-111] - TAB_KON_827 TUC_KON_036 „LiefereFachlicheRolle“
- [Tabelle-112] - TAB_KON_829 Fehlercodes TUC_KON_036 „LiefereFachlicheRolle“
- [Tabelle-113] - TAB_KON_038 Basisanwendung Karten- und Kartenterminaldienst
- [Tabelle-114] - TAB_KON_047 Operation VerifyPin
- [Tabelle-115] - TAB_KON_738 Ablauf VerifyPin
- [Tabelle-116] - TAB_KON_545 Fehlercodes „VerifyPin“
- [Tabelle-117] - TAB_KON_049 Operation ChangePin
- [Tabelle-118] - TAB_KON_546 Ablauf ChangePin
- [Tabelle-119] - TAB_KON_547 Fehlercodes „ChangePin“
- [Tabelle-120] - TAB_KON_051 Operation GetPinStatus
- [Tabelle-121] - TAB_KON_548 Ablauf GetPinStatus
- [Tabelle-122] - TAB_KON_549 Fehlercodes „GetPinStatus“
- [Tabelle-123] - TAB_KON_053 Operation UnblockPin
- [Tabelle-124] - TAB_KON_550 Ablauf UnblockPIN
- [Tabelle-125] - TAB_KON_551 Fehlercodes „UnblockPin“
- [Tabelle-126] - TAB_KON_242 Operation EnablePin
- [Tabelle-127] - TAB_KON_243 Ablauf EnablePin
- [Tabelle-128] - TAB_KON_244 Fehlercodes „EnablePin“
- [Tabelle-129] - TAB_KON_245 Operation DisablePin
- [Tabelle-130] - TAB_KON_246 Ablauf DisablePin
- [Tabelle-131] - TAB_KON_247 Fehlercodes „DisablePin“
- [Tabelle-132] - TAB_KON_554 Konfiguration des Kartendienstes
- [Tabelle-133] - TAB_KON_555 - TUC_KON_025 „Initialisierung Kartendienst“
- [Tabelle-135] - TAB_KON_556 - TUC_KON_256 „Systemereignis absetzen“
- [Tabelle-136] - TAB_KON_557 Fehlercodes TUC_KON_256 „Systemereignis absetzen“
- [Tabelle-137] - TAB_KON_558 – TUC_KON_252 „Liefere KT_Liste“
- [Tabelle-138] - TAB_KON_559 – TUC_KON_253 „Liefere Karten_Liste“
- [Tabelle-139] - TAB_KON_560 Fehlercodes TUC_KON_253 „Liefere Karten_Liste“
- [Tabelle-140] - TAB_KON_561 - TUC_KON_254 „Liefere Ressourcendetails“
- [Tabelle-141] - TAB_KON_562 Fehlercodes TUC_KON_254 „Liefere Ressourcendetails“
- [Tabelle-142] - TAB_KON_029 Basisanwendung Systeminformationsdienst
- [Tabelle-146] - TAB_KON_565 Operation GetCards
- [Tabelle-147] - TAB_KON_566 Ablauf GetCards
- [Tabelle-148] - TAB_KON_567 Fehlercodes „GetCards“
- [Tabelle-149] - TAB_KON_568 Operation GetResourceInformation
- [Tabelle-150] - TAB_KON_569 Ablauf GetResourceInformation
- [Tabelle-151] - TAB_KON_570 Fehlercodes „GetResourceInformation“
- [Tabelle-166] - TAB_KON_747 KeyReference für Encrypt-/DecryptDocument
- [Tabelle-167] - TAB_KON_859 Werteliste und Defaultwert des Parameters crypt bei hybrider Verschlüsselung
- [Tabelle-168] - TAB_KON_739 - TUC_KON_070 „Daten hybrid verschlüsseln“
- [Tabelle-169] - TAB_KON_073 Vorgaben zum Format verschlüsselter XML-Dokumente
- [Tabelle-170] - TAB_KON_740 Fehlercodes TUC_KON_070 „Daten hybrid verschlüsseln“
- [Tabelle-171] - TAB_KON_140 – TUC_KON_071 „Daten hybrid entschlüsseln“
- [Tabelle-172] - TAB_KON_142 Fehlercodes TUC_KON_071 „Daten hybrid entschlüsseln“
- [Tabelle-173] - TAB_KON_741 – TUC_KON_072 „Daten symmetrisch verschlüsseln“
- [Tabelle-174] - TAB_KON_742 Fehlercodes TUC_KON_072 „Daten symmetrisch verschlüsseln“
- [Tabelle-175] - TAB_KON_743 - TUC_KON_073 „Daten symmetrisch entschlüsseln“
- [Tabelle-176] - TAB_KON_744 Fehlercodes TUC_KON_073 „Daten symmetrisch entschlüsseln“
- [Tabelle-177] - TAB_KON_860 – TUC_KON_075 „Symmetrisch verschlüsseln“
- [Tabelle-178] - TAB_KON_861 - TUC_KON_076 „Symmetrisch entschlüsseln“
- [Tabelle-179] - TAB_KON_745 Basisdienst Verschlüsselungsdienst
- [Tabelle-180] - TAB_KON_071 Operation EncryptDocument
- [Tabelle-181] - TAB_KON_746 Ablauf EncryptDocument
- [Tabelle-182] - TAB_KON_141 Fehlercodes „EncryptDocument“
- [Tabelle-183] - TAB_KON_075 Operation DecryptDocument
- [Tabelle-184] - TAB_KON_076 Ablauf DecryptDocument
- [Tabelle-185] - TAB_KON_145 Fehlercodes „DecryptDocument“
- [Tabelle-186] - TAB_KON_582 – Signaturverfahren Dokumentensignatur
- [Tabelle-187] - TAB_KON_778 – Einsatzbereich der Signaturvarianten für XAdES, CAdES und PAdES
- [Tabelle-188] - TAB_KON_583 – Default-Signaturverfahren
- [Tabelle-189] - TAB_KON_584 nonQES-Operationen für EVT_MONITOR_OPERATIONS
- [Tabelle-191] - TAB_KON_862-01 Werteliste und Defaultwert des Parameters crypt bei QES-Erzeugung
- [Tabelle-192] - TAB_KON_863 Werteliste und Defaultwert des Parameters crypt bei nonQES-Erzeugung
- [Tabelle-193] - TAB_KON_748 - TUC_KON_155 „Dokumente zur Signatur vorbereiten“
- [Tabelle-194] - TAB_KON_586 Fehlercodes TUC_KON_155 „Dokumente zur Signatur vorbereiten“
- [Tabelle-195] - TAB_KON_749 – TUC_KON_165 „Signaturvoraussetzungen für nonQES prüfen“
- [Tabelle-196] - TAB_KON_587 Fehlercodes TUC_KON_165 „Signaturvoraussetzungen für nonQES prüfen“
- [Tabelle-197] - TAB_KON_750 – TUC_KON_166 „nonQES Signaturen erstellen“
- [Tabelle-198] - TAB_KON_120 Fehlercodes TUC_KON_166 „nonQES Signaturen erstellen“
- [Tabelle-199] - TAB_KON_751 – TUC_KON_152 „Signaturvoraussetzungen für QES prüfen“
- [Tabelle-200] - TAB_KON_588 Fehlercodes TUC_KON_152 „Signaturvoraussetzungen für QES prüfen“
- [Tabelle-201] - TAB_KON_752 – TUC_KON_154 „QES Signaturen erstellen"
- [Tabelle-202] - TAB_KON_126 Fehlercodes TUC_KON_154 „QES Signaturen erstellen“
- [Tabelle-203] - TAB_KON_293 - TUC_KON_168 „Einzelsignatur QES erstellen“
- [Tabelle-204] - TAB_KON_590 Fehlercodes TUC_KON_168 „Einzelsignatur QES erstellen“
- [Tabelle-205] - TAB_KON_870 – TUC_KON_158 „Komfortsignaturen erstellen"
- [Tabelle-206] - TAB_KON_873 Fehlercodes TUC_KON_158 „Komfortsignaturen erstellen“
- [Tabelle-207] - TAB_KON_753 – TUC_KON_160 „Dokumente nonQES signieren“
- [Tabelle-208] - TAB_KON_127 Fehlercodes TUC_KON_160 „Dokumente nonQES signieren“
- [Tabelle-209] - TAB_KON_753 – TUC_KON_160 „Dokumente nonQES signieren“
- [Tabelle-210] - TAB_KON_127 Fehlercodes TUC_KON_160 „Dokumente nonQES signieren“
- [Tabelle-211] - TAB_KON_121 - TUC_KON_161 „nonQES Dokumentsignatur prüfen“
- [Tabelle-212] - TAB_KON_124 Fehlercodes TUC_KON_161 „nonQES Dokumentensignatur prüfen“
- [Tabelle-213] - TAB_KON_754 Übersicht Status für Prüfung einer Dokumentensignatur
- [Tabelle-214] - TAB_KON_786 Übersicht unterstützte Zertifikatstyp-OIDs
- [Tabelle-215] - TAB_KON_430 – TUC_KON_162 „Kryptographische Prüfung der XML-Dokumentensignatur“
- [Tabelle-216] - TAB_KON_431 Fehlercodes TUC_KON_162 „Kryptographische Prüfung der XML-Dokumentensignatur“
- [Tabelle-217] - TAB_KON_755 – TUC_KON_150 „Dokumente QES signieren“
- [Tabelle-218] - TAB_KON_128 Fehlercodes TUC_KON_150 „Dokument QES signieren“
- [Tabelle-219] - TAB_KON_192 Verhalten des Konnektors beim Abbruch einer Stapelsignatur
- [Tabelle-220] - TAB_KON_591 - TUC_KON_151 „QES-Dokumentensignatur prüfen“
- [Tabelle-221] - TAB_KON_592 Fehlercodes TUC_KON_151 „QES Dokumentensignatur prüfen“
- [Tabelle-222] - TAB_KON_593 Übersicht Status für Prüfung einer Dokumentensignatur
- [Tabelle-223] - TAB_KON_871 – TUC_KON_170 „Dokumente mit Komfort signieren“
- [Tabelle-224] - TAB_KON_872 Fehlercodes TUC_KON_170 „Dokumente mit Komfort signieren“
- [Tabelle-225] - TAB_KON_883 – TUC_KON_171 „Komfortsignatur einschalten“
- [Tabelle-226] - TAB_KON_886 Fehlercodes TUC_KON_171 „Komfortsignatur einschalten“
- [Tabelle-227] - TAB_KON_884 – TUC_KON_172 „Komfortsignatur ausschalten“
- [Tabelle-228] - TAB_KON_887 Fehlercodes TUC_KON_172 „Komfortsignatur ausschalten“
- [Tabelle-229] - TAB_KON_885 – TUC_KON_173 „Liefere Signaturmodus“
- [Tabelle-230] - TAB_KON_888 Fehlercodes TUC_KON_173 „Liefere Signaturmodus“
- [Tabelle-231] - TAB_KON_197 Basisdienst Signaturdienst (nonQES und QES)
- [Tabelle-232] - TAB_KON_065 Operation SignDocument (nonQES und QES)
- [Tabelle-233] - TAB_KON_756 Ablauf Operation SignDocument (nonQES und QES)
- [Tabelle-234] - TAB_KON_757 Fehlercodes „SignDocument (nonQES und QES)“
- [Tabelle-235] - TAB_KON_066 Operation VerifyDocument (nonQES und QES)
- [Tabelle-236] - TAB_KON_760 Ablauf Operation VerifyDocument (nonQES und QES)
- [Tabelle-237] - TAB_KON_761 Fehlercodes „VerifyDocument (nonQES und QES)“
- [Tabelle-238] - TAB_KON_840 Operation StopSignature
- [Tabelle-239] - TAB_KON_841 Ablauf Operation StopSignature
- [Tabelle-240] - TAB_KON_842 Fehlercodes „StopSignature“
- [Tabelle-241] - TAB_KON_843 Operation GetJobNumber
- [Tabelle-242] - TAB_KON_844 Ablauf Operation GetJobNumber
- [Tabelle-243] - TAB_KON_845 Fehlercodes „GetJobNumber“
- [Tabelle-244] - TAB_KON_874 ActivateComfortSignature
- [Tabelle-245] - TAB_KON_877 Ablauf ActivateComfortSignature
- [Tabelle-246] - TAB_KON_879 Fehlercodes ActivateComfortSignature
- [Tabelle-247] - TAB_KON_875 DeactivateComfortSignature
- [Tabelle-248] - TAB_KON_878 Ablauf DeactivateComfortSignature
- [Tabelle-249] - TAB_KON_880 Fehlercodes DeactivateComfortSignature
- [Tabelle-250] - TAB_KON_876 GetSignatureMode
- [Tabelle-251] - TAB_KON_882 Ablauf GetSignatureMode
- [Tabelle-252] - TAB_KON_881 Fehlercodes GetSignatureMode
- [Tabelle-253] - TAB_KON_596 Konfigurationswerte des Signaturdienstes (Administrator)
- [Tabelle-254] - TAB_KON_853- intendedKeyUsage bei Zertifikatsprüfung
- [Tabelle-255] - TAB_KON_858 Kartenobjekt in Abhängigkeit vom kryptographischen Verfahren
- [Tabelle-256] - TAB_KON_825 Fehlercodes „TLS-Verbindungsaufbau zum TSL-Dienst“
- [Tabelle-258] - TAB_KON_597 Operationen in EVT_MONITOR_OPERATIONS
- [Tabelle-259] - TAB_KON_766 TUC_KON_032 „TSL aktualisieren“
- [Tabelle-260] - TAB_KON_598 Fehlercodes TUC_KON_032 „TSL aktualisieren“
- [Tabelle-261] - TAB_KON_618 TUC_KON_031 „BNetzA-VL aktualisieren“
- [Tabelle-262] - TAB_KON_619 Fehlercodes TUC_KON_031 „BNetzA-VL aktualisieren“
- [Tabelle-263] - TAB_KON_767 TUC_KON_040 „CRL aktualisieren“
- [Tabelle-264] - TAB_KON_599 Fehlercodes TUC_KON_040 „CRL aktualisieren“
- [Tabelle-265] - TAB_KON_768 TUC_KON_033 „Zertifikatsablauf prüfen“
- [Tabelle-266] - TAB_KON_600 Fehlercodes TUC_KON_033 „Zertifikatsablauf prüfen“
- [Tabelle-267] - TAB_KON_769 TUC_KON_037 „Zertifikat prüfen“
- [Tabelle-268] - TAB_KON_601 Fehlercodes TUC_KON_037 „Zertifikat prüfen“
- [Tabelle-269] -  TAB_KON_818 TUC_KON_042 „CV-Zertifikat prüfen“ 
- [Tabelle-270] - TAB_KON_819 Fehlercodes TUC_KON_042 „CV-Zertifikat prüfen“
- [Tabelle-271] - TAB_KON_770 TUC_KON_034 „Zertifikatsinformationen extrahieren“
- [Tabelle-272] - TAB_KON_602 Fehlercodes TUC_KON_034 „Zertifikatsinformationen extrahieren“
- [Tabelle-273] - TAB_KON_771 Basisanwendung Zertifikatsdienst
- [Tabelle-274] - TAB_KON_676 Operation CheckCertificateExpiration
- [Tabelle-275] - TAB_KON_677 Ablauf CheckCertificateExpiration
- [Tabelle-276] - TAB_KON_603 Fehlercodes „CheckCertificateExpiration“
- [Tabelle-277] - TAB_KON_678 Operation ReadCardCertificate
- [Tabelle-278] - TAB_KON_679 Ablauf ReadCardCertificate
- [Tabelle-279] - TAB_KON_604 Fehlercodes „ReadCardCertificate“
- [Tabelle-283] - TAB_KON_772 TUC_KON_035 „Zertifikatsdienst initialisieren“
- [Tabelle-284] - TAB_KON_605 Fehlercodes TUC_KON_035 „Zertifikatsdienst initialisieren“
- [Tabelle-285] - TAB_KON_606 Konfiguration des Zertifikatsdienstes
- [Tabelle-286] - TAB_KON_733 Einsehbare Konfigurationsparameter des Zertifikatsdienstes
- [Tabelle-287] - TAB_KON_857 - Fehlercodes beim Import des Cross-Zertifikats für TI-Vertrauensanker ECC
- [Tabelle-288] - TAB_KON_607 – TUC_KON_271 „Schreibe Protokolleintrag“
- [Tabelle-289] - TAB_KON_608 Fehlercodes TUC_KON_271 „Schreibe Protokolleintrag“
- [Tabelle-290] - TAB_KON_609 Konfigurationswerte des Protokollierungsdienstes (Administrator)
- [Tabelle-291] - TAB_KON_610 – TUC_KON_272 „Initialisierung Protokollierungsdienst“
- [Tabelle-292] - TAB_KON_611 Fehlercodes TUC_KON_272 „Initialisiere Protokollierungsdienst“
- [Tabelle-293] - TAB_KON_773 – TUC_KON_110 „Kartenbasierte TLS-Verbindung aufbauen“
- [Tabelle-294] - TAB_KON_612 Fehlercodes TUC_KON_110 „Kartenbasierte TLS-Verbindung aufbauen“
- [Tabelle-295] - TAB_KON_774 - TUC_KON_111 „Kartenbasierte TLS-Verbindung abbauen“
- [Tabelle-296] - TAB_KON_613 Fehlercodes TUC_KON_111 „Kartenbasierte TLS-Verbindung abbauen“
- [Tabelle-297] - TAB_KON_805 - TUC_KON_290 „LDAP-Verbindung aufbauen“
- [Tabelle-298] - TAB_KON_815 – TUC_KON_291 „Verzeichnis abfragen“
- [Tabelle-299] - TAB_KON_816 – TUC_KON_292 „LDAP-Verbindung trennen"
- [Tabelle-300] - TAB_KON_817 – TUC_KON_293 „Verzeichnisabfrage abbrechen“
- [Tabelle-301] - TAB_KON_780 – Signaturverfahren Externe Authentisierung
- [Tabelle-302] - TAB_KON_839 Basisdienst Authentifizierungsdienst
- [Tabelle-303] - TAB_KON_781 Operation ExternalAuthenticate
- [Tabelle-304] - TAB_KON_782 Ablauf Operation ExternalAuthenticate
- [Tabelle-305] - TAB_KON_783 Übersicht Fehler Operation ExternalAuthenticate
- [Tabelle-306] - TAB_KON_784 Privater Schlüssel je Karte für ExternalAuthenticate
- [Tabelle-307] - TAB_KON_680 Mapping der Netzwerksegmente
- [Tabelle-308] - TAB_KON_681 Definition der vom Konnektor verwendeten VPN-Tunnel
- [Tabelle-309] - TAB_KON_682 Definition der Konnektor IP-Adressen
- [Tabelle-310] - TAB_KON_614 - TUC_KON_305 „LAN-Adapter initialisieren“
- [Tabelle-311] - TAB_KON_615 Fehlercodes TUC_KON_305 „LAN-Adapter initialisieren“
- [Tabelle-312] - TAB_KON_616 - TUC_KON_306 „WAN-Adapter initialisieren“
- [Tabelle-313] - TAB_KON_617 Fehlercodes TUC_KON_306 „WAN-Adapter initialisieren“
- [Tabelle-314] - TAB_KON_622 - TUC_KON_304 „Netzwerk-Routen einrichten“
- [Tabelle-315] - TAB_KON_623 Fehlercodes TUC_KON_304 „Netzwerk-Routen einrichten“
- [Tabelle-316] - TAB_KON_683 LAN-Adapter IP-Konfiguration
- [Tabelle-317] - TAB_KON_684 LAN-Adapter Erweiterte Parameter
- [Tabelle-318] - TAB_KON_685 WAN-Adapter IP-Konfiguration
- [Tabelle-319] - TAB_KON_686 WAN-Adapter Erweiterte Parameter
- [Tabelle-320] - TAB_KON_624 – „Konfigurationsparameter der Anbindung LAN/WAN“
- [Tabelle-321] - TAB_KON_625 - Konfigurationsparameter Firewall-Schnittstelle
- [Tabelle-322] - TAB_KON_626 „Liefere Netzwerkinformationen über DHCP“
- [Tabelle-324] - TAB_KON_628 „Basiskonfiguration des DHCP-Servers“
- [Tabelle-325] - TAB_KON_629 „Client-Gruppenspezifische Konfigurationsoptionen des Konnektor-DHCP-Servers“
- [Tabelle-326] - TAB_KON_630 - TUC_KON_343 „Initialisierung DHCP-Server“
- [Tabelle-327] - TAB_KON_631 Fehlercodes TUC_KON_343 „Initialisierung DHCP-Server“
- [Tabelle-328] - TAB_KON_632 – TUC_KON_341 „DHCP Informationen beziehen“
- [Tabelle-329] - TAB_KON_633 Fehlercodes TUC_KON_341 „DHCP-Informationen beziehen“
- [Tabelle-330] - TAB_KON_634 „Konfiguration des DHCP-Clients“
- [Tabelle-331] - TAB_KON_635 – TUC_KON_321 „Verbindung zu dem VPN-Konzentrator der TI aufbauen“
- [Tabelle-332] - TAB_KON_636 Fehlercodes TUC_KON_321 „Verbindung zu dem VPN-Konzentrator der TI aufbauen“
- [Tabelle-333] - TAB_KON_637 – TUC_KON_322 „Verbindung zu dem VPN-Konzentrator der SIS aufbauen“
- [Tabelle-334] - TAB_KON_638 Fehlercodes TUC_KON_322 „Verbindung zu dem VPN-Konzentrator der SIS aufbauen“
- [Tabelle-335] - TAB_KON_639 – Konfigurationsparameter VPN-Client
- [Tabelle-336] - TAB_KON_640 Zustandswerte für Konnektor NTP-Server
- [Tabelle-337] - TAB_KON_776 TUC_KON_351 „Liefere Systemzeit“
- [Tabelle-338] - TAB_KON_641 Fehlercodes TUC_KON_351 „Liefere Systemzeit“
- [Tabelle-339] - TAB_KON_642 Operation sync_Time
- [Tabelle-340] - TAB_KON_643 Konfiguration des Konnektor NTP-Servers
- [Tabelle-341] - TAB_KON_730 Einsehbare Konfigurationsparameter des Konnektor NTP-Servers
- [Tabelle-342] - TAB_KON_644 – TUC_KON_352 „Initialisierung Zeitdienst“
- [Tabelle-343] - TAB_KON_645 Fehlercodes TUC_KON_352 „Initialisierung Zeitdienst“
- [Tabelle-344] - TAB_KON_687 DNS-Forwards des DNS-Servers
- [Tabelle-345] - TAB_KON_646 – TUC_KON_361 „DNS-Namen auflösen“
- [Tabelle-346] - TAB_KON_647 Fehlercodes TUC_KON_361 „DNS Namen auflösen“
- [Tabelle-347] - TAB_KON_646 – TUC_KON_361 „DNS-Namen auflösen“
- [Tabelle-348] - TAB_KON_647 Fehlercodes TUC_KON_361 „DNS Namen auflösen“
- [Tabelle-349] - TAB_KON_648 – TUC_KON_362 „Liste der Dienste abrufen“
- [Tabelle-350] - TAB_KON_649 Fehlercodes TUC_KON_362 „Liste der Dienste abrufen“
- [Tabelle-351] - TAB_KON_650 - TUC_KON_363 „Dienstdetails abrufen“
- [Tabelle-352] - TAB_KON_651 Fehlercodes TUC_KON_363 „Dienstdetails abrufen“
- [Tabelle-353] - TAB_KON_652 Basisanwendung Namensdienst
- [Tabelle-354] - TAB_KON_653 Operation GetIPAddress
- [Tabelle-355] - TAB_KON_654 - Konfigurationsparameter Namensdienst
- [Tabelle-356] - TAB_KON_731 Einsehbare Konfigurationsparameter Namensdienst
- [Tabelle-357] - TAB_KON_655 Konfigurationen der Benutzerverwaltung (Super-Administrator)
- [Tabelle-358] - TAB_KON_656 Konfigurationen der Benutzerverwaltung
- [Tabelle-359] - TAB_KON_657 Konfigurationsparameter des Konnektornamens
- [Tabelle-360] - TAB_KON_833 Bezeichner für persistente Konfigurationsdaten für Fachmodule
- [Tabelle-361] - TAB_KON_658 Aktivieren/Deaktivieren von Leistungsumfängen
- [Tabelle -366] - TAB_KON_932 – TUC_KON_411 „Konnektor mit neuem NK-Zertifikat registrieren“
- [Tabelle-368] - TAB_KON_851 Einschränkung der Rechte des Remote-Administrators (Denylist)
- [Tabelle-370] - TAB_KON_664 – TUC_KON_280 „Konnektoraktualisierung durchführen“
- [Tabelle-371] - TAB_KON_665 Fehlercodes TUC_KON_280 „Konnektoraktualisierung durchführen“
- [Tabelle-372] - TAB_KON_666 – TUC_KON_281 „Kartenterminalaktualisierung anstoßen“
- [Tabelle-373] - TAB_KON_667 Fehlercodes TUC_KON_281 „Kartenterminalaktualisierung anstoßen“
- [Tabelle-374] - TAB_KON_668 – TUC_KON_282 „UpdateInformationen beziehen“
- [Tabelle-375] - TAB_KON_669 Fehlercodes TUC_KON_282 „UpdateInformationen beziehen“
- [Tabelle-376] - TAB_KON_799 – TUC_KON_283 „Infrastruktur Konfiguration aktualisieren“
- [Tabelle-377] - Tab_Kon_726 Fehlercodes TUC_KON_283 „Infrastruktur Konfiguration aktualisieren“
- [Tabelle-378] - TAB_KON_833 – TUC_KON_285 „UpdateInformationen für Fachmodul beziehen“
- [Tabelle-379] - TAB_KON_834 Fehlercodes TUC_KON_285 „UpdateInformationen für Fachmodul beziehen“
- [Tabelle-380] - TAB_KON_835 – TUC_KON_286 „Paket für Fachmodul laden“
- [Tabelle-381] - TAB_KON_836 Fehlercodes TUC_KON_286 „Paket für Fachmodul laden“
- [Tabelle-382] - TAB_KON_864 – TUC_KON_284 „KSR-Client initialisieren“
- [Tabelle-383] - TAB_KON_822 Fehlercodes TUC_KON_284 „KSR-Client initialisieren“
- [Tabelle-384] - TAB_KON_670 Konfigurationsparameter der Software-Aktualisierung
- [Tabelle-385] - TAB_KON_820 Einsehbare Konfigurationsparameter der Software-Aktualisierung
- [Tabelle-386] - TAB_KON_671 Anforderungen Klima
- [Tabelle-387] - TAB_KON_672 Anforderungen Vibration
- [Tabelle-388] - TAB_KON_672 Anforderungen Vibration
- [Tabelle-389] - TAB_KON_779-01 „Profilierung der Signaturformate“
- [Tabelle-390] - TAB_KON_775 „Mindestanforderungen an Dimensionierung von Dokumenten und Nachrichten“
- [Tabelle-391] - TAB_KON_889 „Unerlaubte Inhalte in Dokumenten und Nachrichten“
- [Tabelle-392] - TAB_KON_777 Events Interne Mechanismen
- [Tabelle-393] - TAB_KON_711 Architektur der TI-Plattform, Berechtigt Fachmodule
- [Tabelle-394] - TAB_KON_712 Architektur der TI-Plattform, Berechtigt Clientsysteme
- [Tabelle-395] - TAB_KON_713 Architektur der TI-Plattform, Berechtigt eHealth-KT
- [Tabelle-396] - TAB_KON_714 Architektur der TI-Plattform, Berechtigt Administrator
- [Tabelle-397] - Aufzähltypen

### 5.5 Referenzierte Dokumente

### 5.5.1 Dokumente der gematik

Die nachfolgende Tabelle enthält die Bezeichnung der in dem vorliegenden
Dokument referenzierten Dokumente der gematik zur Telematikinfrastruktur. Der
mit der vorliegenden Version korrelierende Entwicklungsstand dieser Konzepte
und Spezifikationen wird pro Release in einer Dokumentenlandkarte definiert,
Version und Stand der referenzierten Dokumente sind daher in der nachfolgenden
Tabelle nicht aufgeführt. Deren zu diesem Dokument passende jeweils gültige
Versionsnummer sind in der aktuellsten, von der gematik veröffentlichten
Dokumentenlandkarte enthalten, in der die vorliegende Version aufgeführt wird.

 ---> TABLE

### 5.5.2 Weitere Dokumente

 ---> TABLE

### 6 Anhang B – Profilierung der Signatur- und Verschlüsselungsformate (normativ)

### 6.1 Profilierung der Verschlüsselungsformate

### 6.2 Profilierung der Signaturformate

 ---> TABLE

### 6.3 Profilierung VerificationReport

Anforderung eines ausführlichen Prüfberichts

Folgende Aufrufparameter müssen unterstützt werden:

\<ReturnVerificationReport

xmlns="urn:oasis:names:tc:dss-x:1.0:profiles:verificationreport:schema#"
xmlns:xsi=http://www.w3.org/2001/XMLSchema-instance

xsi:schemaLocation="urn:oasis:names:tc:dss-x:1.0:profiles:verificationreport:schema#

oasis-dssx-1.0-profiles-vr-cd1.xsd"\>

\<IncludeVerifier\>false\</IncludeVerifier\>

\<IncludeCertificateValues\>true\</IncludeCertificateValues\>

\<IncludeRevocationValues\>true\</IncludeRevocationValues\>

\<ExpandBinaryValues\>false\</ExpandBinaryValues\>  

\<ReportDetailLevel\>

urn:oasis:names:tc:dss-x:1.0:profiles:verificationreport:reportdetail:allDetails

\</ReportDetailLevel\>

\</ReturnVerificationReport\>

Verwendung des erzeugten VerificationReport

Für die folgenden Inhalte müssen die angegebenen Strukturen benutzt werden. Im
Standard angegebene Pflichtfelder von erzeugten Strukturen müssen ggf.
zusätzlich gefüllt werden:

 ---> OL

/VerificationReport/

    dss:VerificationTimeInfo/    

        dss:VerificationTime

 ---> OL

/VerificationReport/

    IndividualReport/

        SignedObjectIdentifier/

            SignedProperties/

                SignedSignatureProperties/

                    XAdES:SigningTime

Die Signierzeit SigningTime ist nicht nur für XAdES-Signaturen, sondern
allgemein für Signaturen gemäß AdES-Baseline-Profilierung, also auch für
CAdES und PAdES zu füllen.

 ---> OL

/VerificationReport/    IndividualReport/  
        Details/            dss:VerificationTimeInfo/                dss:VerificationTime

 ---> OL

/VerificationReport/

    IndividualReport/

        SignedObjectIdentifier/

            SignatureValue

 ---> OL

Der signierte Kurztext wird in folgendem XML-Element zurückgegeben:

/VerificationReport/

      IndividualReport/

             SignedObjectIdentifier/

                   SignedProperties/

                        Other/                            SIG:ShortText

Die ungültigen Zeichen müssen aus dem ShortText entfern werden und der
ShortText wird gekürzt, wenn er nicht den Längenvorgaben des Schemas
entspricht. 

 ---> OL

/VerificationReport/

      IndividualReport/

             SignedObjectIdentifier/

                   SignedProperties/

                        Other/                               
SIG:ReferenceToSignerCertificate

 ---> OL

/VerificationReport/

      IndividualReport/

             SignedObjectIdentifier/

                   SignedProperties/

                        Other/                               
SIG:DisplayableAttributes

 ---> OL

/VerificationReport/

    IndividualReport/

        Result

 ---> OL

Properties/

UnsignedProperties/

    Other/

        SIG:CounterSignatureMarker    

und mit

/DetailedSignatureReport/

Properties/

UnsignedProperties/

    Other/

        SIG:CounterSignatureMarker/

SignatureValueReference/

        @IdRef        

auf jede (eine oder mehrere) gegensignierte Signaturen verwiesen.  Dabei
zeigt  IdRef auf den jeweiligen gegensignierten
Signaturwert/VerificationReport/

    IndividualReport/

        SignedObjectIdentifier/

            ds:SignatureValue/

                @Id

 ---> OL

/VerificationReport/

    IndividualReport/

        Details/

            DetailedSignatureReport/

                CertificatePathValidity/

                    PathValiditySummary/

                        ResultMajor

 ---> OL

/VerificationReport/

    IndividualReport/

        Details/

            DetailedSignatureReport/

                CertificatePathValidity/

                    PathValidityDetail/

                        CertificateValidity/

                            CertificateValue

 ---> OL

/VerificationReport/

    IndividualReport/

        Details/

            DetailedSignatureReport/

                SignatureOK/    

                    SignatureAlgorithm    

                        

 ---> OL

Für alle geprüften Zertifikate:

../

vr:CertificateValidity/

        vr:SignatureOK/

            vr:SignatureAlgorithm/

                vr:Suitability/

./ResultMajor= urn:oasis:names:tc:dss:1.0:detail:invalid

./ResultMessage=“Algorithmen seit \<Jahr\> als unsicher eingestuft“

 ---> OL

//CertificateValidity/ChainingOK/ResultMajor (ab dem zweiten Zertifikat in der
Kette)

//CertificateValidity/CertificateStatus/CertStatusOK/ResultMajor

//CertificateValidity/CertificateValue

Für das Feld TrustAnchor ist

“urn:oasis:names:tc:dss-x:1.0:profiles:verificationreport:trustanchor:certDataBase”

zu verwenden.

 ---> OL

/VerificationReport/

    IndividualReport/

        Details/

            DetailedSignatureReport/

                CertificatePathValidity/

                    PathValidityDetail/

                        CertificateValidity/

                            ValidityPeriodOK/

                                ResultMajor

 ---> OL

/VerificationReport/

    IndividualReport/

        Details/

            DetailedSignatureReport/

                CertificatePathValidity/

                    PathValidityDetail/

                        CertificateValidity/

                            ExtensionsOK/

                                ResultMajor

 ---> OL

/VerificationReport/

    IndividualReport/

        Details/

            DetailedSignatureReport/

                CertificatePathValidity/

                        PathValidityDetail/

                            CertificateValidity/

                                CertificateStatus/

                                    RevocationEvidence/

                                        OCSPValidity/

                                            OCSPIdentifier/

            ./XAdES:ResponderID/XAdES:ByName

            ./XAdES:ProducedAt

 ---> OL

/VerificationReport/

    IndividualReport/

        Details/

            /vr:DetailedSignatureReport/

                vr:CertificatePathValidity/

                    vr:PathValidityDetail/

                        vr:CertificateValidity/

                            vr:CertificateStatus/

                                vr:RevocationEvidence/

                                    vr:OCSPValidity/

                                        vr:OCSPValue

Sonderfälle:

Dokument mit parallelen Signaturen

    Für jede Signatur wird ein IndividualReport erzeugt.

Dokument mit Signatur und Gegensignatur

    Für jede Signatur wird ein IndividualReport erzeugt.    

### 6.4 Profilierung der Dokumentenformate und Nachrichten

 ---> TABLE

 ---> TABLE

### 7 Anhang F – Übersicht Events

 ---> TABLE

Die Abbildungsvorschrift von Fehler- auf Event-Type lautet:

 ---> UL

### 8 Anhang H – Mapping von „Architektur der TI-Plattform“ auf Konnektorspezifikation

 ---> TABLE

 ---> TABLE

 ---> TABLE

 ---> TABLE

### 9 Anhang I – Umsetzungshinweise (informativ)

In diesem Anhang finden sich Darstellungen und Informationen, die ein
Konnektorhersteller zur Umsetzung der normativen Anforderungen in ein konkretes
Produkt berücksichtigen kann. Sie wurden im Rahmen der Erhebung der normativen
Anforderungen erarbeitet, um die Umsetzbarkeit der Anforderungen zu bestätigen.

Dieser Anhang soll als Unterstützung für eine Umsetzung verstanden werden und
erhebt keinen Anspruch auf Korrektheit und Vollständigkeit.

### 9.1 Systemüberblick

### 9.1.1 – Hinweise zur Sicherheitsevaluierung nach Common Criteria

Gemäß dem Sicherheitskonzept des Konnektors [gemKPT_Sich_Kon] muss die
Software des Konnektors nach Common Criteria (CC) evaluiert und geprüft werden.

Diese Software erbringt Sicherheitsleistungen in zwei wesentlichen
Funktionsblöcken. Durch diese Aufteilung ist es möglich, dass die einzelnen
Funktionsblöcke zeitlich voneinander unabhängig bzw. sogar von
unterschiedlichen Herstellern implementiert, evaluiert und geprüft werden
können. Es werden zwei Schutzprofile (Protection Profile) für die
Funktionsblöcke des Konnektors erstellt. Es handelt sich dabei um die
Schutzprofile des Netzkonnektors (KONN.NK) sowie des Anwendungskonnektors
(KONN.AK) inklusive der Signaturanwendungskomponente. Das Schutzprofil des
Sicherheitsmoduls für den Konnektor (SM-K) wird in diesem Kapitel nicht
betrachtet.

Diese Schutzprofile definieren eine implementierungsunabhängige Menge von
Sicherheitsanforderungen für die einzelnen Konnektorfunktionsblöcke bzw.
Konnektorbestandteile. Anhand dieser Schutzprofile werden von den Herstellern
der Konnektoren die Sicherheitsvorgaben (Security Targets) für die konkreten
Umgebungen erstellt, welche als Eingangsdokumente für den
Zertifizierungsprozess der jeweiligen konkreten Komponenten eingesetzt werden.
Diese zu evaluierenden Komponenten werden als Evaluierungsgegenstand (EVG)
bezeichnet.

### 9.1.1.1 Separationsmechanismen des Konnektors

Damit es nach einer erfolgreichen Evaluierung eines Konnektors auch weiterhin
möglich bleibt, Software oder Daten, die keinen direkten Einfluss auf
Sicherheitsfunktionen der EVGs aufweisen, ohne eine Re-Evaluierung definiert
auszutauschen, hinzuzufügen oder zu erweitern, ist eine Separation der
Komponenten des EVG dringend anzuraten.

Implementiert der Hersteller keine bzw. nicht ausreichende
Separationsmechanismen, so ist bei bestimmten Update-Arten von einer
aufwändigen Re-Evaluierung des entsprechenden EVGs auszugehen. Die Separation
dient also der Trennung zwischen ausführbarem Code des EVG, welcher
Sicherheitsfunktionen umsetzt, und zusätzlichem ausführbarem Code auf dem
Konnektor, welcher keine Sicherheitsfunktionen umsetzt.

Die Wahl der Separationsmechanismen steht dem Hersteller frei und muss in den
Sicherheitsvorgaben für den EVG beschrieben und als solcher evaluiert werden.
Aus diesen Sicherheitsvorgaben ergibt sich auch, welche Update-Arten bei
welchen Separationsmechanismen eine Re-Evaluierung des EVG erfordern und wie
aufwendig diese Re-Evaluierung ausfällt.

Unter diese Update-Arten können beispielsweise – je nach
Konnektorarchitektur, CC-Dokumentation oder Konnektorimplementierung –
Bestandteile des unter dem Konnektor arbeitenden Betriebsystems, die
Installation dezentraler Komponenten von Fachlogik oder Konfigurationsdaten des
Konnektors fallen.

Als Beispiel für Separationsmechanismen sei auf die folgende informative
Aufzählung verwiesen, welche jedoch keinen Anspruch auf Vollständigkeit
besitzen kann und nur mögliche Alternativen aufzeigt:

 ---> UL

Je nach gewähltem Architekturansatz des Herstellers sind nicht alle hier
genannten Alternativen für die Separation des EVG auf dem Konnektor anwendbar.

Insbesondere sollte der Hersteller den eigentlichen Update-Prozess und die
dafür verantwortliche Komponente mit besonderer Sorgfalt beschreiben,
spezifizieren und implementieren. Bei einer fehlerhaften Implementierung dieser
Komponente besteht die Gefahr einer Schwächung oder des Ausschaltens von
Sicherheitsfunktionen des EVG. Die Update-Komponente muss eine sichere
Zuweisung der Updates zu den separierten Bestandteilen des EVGs gewährleisten.
Auch ist zu betonen, dass der EVG immer die Integrität der Daten des Updates
und die Authentizität des Absenders prüfen muss, bevor ein Update akzeptiert
wird. Der Update-Komponente muss somit besondere Beachtung geschenkt werden.

### 9.1.1.2 Granularität der TSF

Die TSF (TOE Security Functionality) eines EVG besteht aus Subsystemen und
Modulen, wobei ein Modul die genaueste Beschreibung einer Funktionalität
darstellt und unterhalb der Subsysteme angesiedelt ist. Subsysteme beschreiben
das Design des EVG und können wiederum – je nach Komplexität eines EVGs –
aus weiteren Subsystemen bestehen. Ein Entwickler sollte außer der
Modulbeschreibung keine weiteren Informationen zur Implementierung der dort
beschriebenen Funktionalität benötigen.

Die Subsysteme und Module der TSF gliedern sich in drei Klassen:

   (a) SFR-Enforcing Subsysteme und Module. Hierunter fallen die Subsysteme und

        Module, welche eine funktionale Sicherheitsanforderung direkt
durchsetzen.

   (b) SFR-Supporting Subsysteme und Module. Hierunter fallen die Subsysteme
und

        Module, welche bei der Durchsetzung einer funktionalen
Sicherheitsanforderung

        unterstützend wirken.

   (c) SFR-Non-Interfering Subsysteme und Module. Hierunter fallen die
Subsysteme

        und Module, welche keine Leistung bei der Erfüllung einer
funktionalen

        Sicherheitsanforderung erbringen.

Sollte nach einer erfolgreichen CC-Evaluierung eines Konnektors die
Notwendigkeit zur Änderung der Software des Konnektors gegeben sein, so ist
unter Umständen eine Re-Evaluierung des EVG erforderlich. Diese Notwendigkeit
kann sich aus der Behebung von nachträglich erkannten Fehlern, aufgetretenen
Sicherheitslücken, Schwächen eines Standardverfahrens oder einer
erforderlichen Erweiterung der Funktionalität ergeben.

Im Rahmen der Aufzählung der Anforderungen an die Beschreibung des EVG-Design
(ADV_TDS) wird bereits die Aufteilung der TSF auf Subsysteme und Module
beschrieben. Trotzdem soll hiermit ausdrücklich geraten werden, die Aufteilung
der TSF auf die Subsysteme und Module selbst und die Aufteilung der Subsysteme
und Module auf die drei o. g. Klassen möglichst feingranular durchzuführen.

Denn so

 ---> OL

### 9.2 Übergreifende Festlegungen

### 9.2.1 Interne Mechanismen

### 9.2.1.1 Zufallszahlen und Schlüssel

Der Konnektor kann zur Erzeugung von Zufallszahlen und Einmalschlüsseln einen
Hardware- oder Software-Generator verwenden. Als Quelle für Zufallszahlen kann
der Konnektor die gSMC-K verwenden.

### 9.3 Funktionsmerkmale

### 9.3.1 Anwendungskonnektor

### 9.3.1.1 Administration des Informationsmodells

Wie die Administration der persistenten Entitäten und Beziehungen des
Informationsmodells im Detail über die bereitzustellende
Administrationsoberfläche erfolgt, entscheidet der Hersteller.

Es wird folgende Reihenfolge für die Pflege des Informationsmodells empfohlen.

 ---> OL

### 9.3.1.2 Vorgehensvariante für das Handling von CardSessions

Das in der [TIP1-A_4560] „Rahmenbedingungen für Kartensitzungen“ geforderte
Verhalten, ließe sich über folgenden Mechanismus umsetzen:

Verschiedene Clientsystem (oder verschiedene Nutzer an einem Clientsystem)
möchten auf Daten der über CardHandle adressierten Smartcard zugreifen.

Für die Zugriffe müssen, je nach Definition der Zugriffsbedingung in der
Zielkarte, bestimmte Sicherheitszustände erreicht werden (durch Verifikation
einer PIN oder durch C2C). Diese erreichten Sicherheitszustände werden
innerhalb einer Karte jeweils an einen logischen Kanäle (bzw. den Basiskanal)
gebunden, d. h., das Erhöhen oder Absenken eines Sicherheitszustands wirkt
nicht außerhalb des logischen Kanals, in dem die Veränderung verursacht wurde.

Finden nun Clientsystemzugriffe in unterschiedlichen Kontexten (Mandant,
Clientsystem, Arbeitsplatz und Nutzer verschieden) auf die gleiche Karte statt,
so muss sichergestellt sein, dass PIN-Eingaben und durchgeführte C2C nur für
den Kontext wirksam sind, in welchem sie durchgeführt wurden. Dies ließe sich
erreichen, wenn jeder Kontext auf einen eigenen logischen Kanal der Karte
abgebildet würde. Leider unterstützen der HBA und die SMC-B nur vier, die eGK
nur einen logischen Kanal. Mehrere gleichzeitige unterschiedliche Kontexte
wären somit nicht möglich.

Eine mögliche Lösung für beliebig viele gleichzeitige Kontexte:

![Abbildung-23][Abbildung-23]

Der Kartendienst fungiert als Multiplexer. Er spiegelt die Zugriffsrechte der
Karte und wendet deren Regeln selbständig gegen die unterschiedlichen Zugriffe
durch Clientsysteme an.

Für jedes Card-Objekt wird „in Richtung Clientsystem“ pro Kontext genau
eine CardSession erzeugt und verwaltet. Zugriffe des Clientsystems erfolgen
somit „im Kontext“ einer CardSession.

In Richtung Karte verwendet das Card-Object genau zwei Kanäle (zwei logische
oder einen logischen und einen Basiskanal):

 ---> UL

In jeder CardSession werden die in ihrem Kontext erreichten Sicherheitszustände
vermerkt. Das Vorgehen für die Durchführung der Verifikationen und des
Vermerkens der erreichten Sicherheitszustände, sowie der Datenzugriffe folgt
folgenden Regeln (hier für PIN-Verifikation, sinngleich auch für C2C):

 ---> UL

Diese Regeln führen dazu, dass eine durch CardSession Y fehlgeschlagene
Verifikation für PinRef_A die zuvor erfolgreich durch CardSession X
durchgeführt Verifikation nicht beeinflusst. Kartenzugriffe auf dem Datenkanal
sind für CardSession X weiterhin möglich, da der Verlust des erhöhten
Sicherheitszustands durch fehlerhafte Verifikation immer nur im
Verifikationskanal erfolgt.

Dieser Mechanismus funktioniert mit zwei Kanälen zu einer Karte für beliebig
viele CardSessions.

### 9.3.1.3 Darstellung von Terminal-Anzeigen auf einem Kartenterminal

Hiweise für die korrekte Verwendung der zur Verfügung stehenden Datenobjekte
(DO) zur Darstellung von Terminal-Anzeigen an einem Kartenterminal finden sich
in SICCT- (insbesondere in [SICCT#5.5.10.19] und [SICCT#5.5.10.21]) und
eHealth-Kartenterminal-Spezifikationen.

### 10 Anhang K – Szenarien im dezentralen Umfeld

Die folgenden Szenarien für den Einsatz der Produkte der Telematikinfrastruktur
beschreiben informativ Varianten und Optionen, die durch die Spezifikationen
abgedeckt werden.

Die vorliegenden Abbildungen in diesem Anhang fokussieren auf das dezentrale
Umfeld und verzichten daher auf die Darstellung der zentralen Anteile, wie das
zentrale Netzwerk der Telematikinfrastruktur, welches über den
„VPN-Konzentrator TI“ erreichbar ist.

Der Konnektor, sowie die Netzwerkkomponenten Switch und IAG (Internet Access
Gateway) sind in den folgenden Szenarien zum Schutz vor unerlaubtem Zugriff
gemäß den Annahmen des Sicherheitskonzeptes vor unbefugten physischen
Zugriffen geschützt installiert.

Die folgenden Abschnitte stellen jeweils ein Szenario in der Übersicht als
Diagramm, eine Beschreibung sowie eine kurze Auflistung der Voraussetzungen und
Auswirkungen dar.

### 10.1 Szenario 1: Einfache Installation ohne spezielle Anforderungen und ohne bestehende Infrastruktur

![Abbildung-24][Abbildung-24]

### 10.1.1 Beschreibung des Szenarios

Abbildung 25 zeigt ein einfaches Szenario für das dezentrale Umfeld. Es wird
der Konnektor als Default-Gateway für jegliche IP-Kommunikation aus dem LAN in
das WAN eingesetzt. Dabei übernimmt der Konnektor das Routing der
Kommunikation in das Internet über den SIS (Secure Internet Service) und in
die an die TI angeschlossenen Bestandsnetze. Die Bezeichnung IAG (Internet
Access Gateway) steht für die Geräte, die den Internetzugang ermöglichen und
typischerweise vom Internet Service Provider (ISP) zur Verfügung gestellt
werden (z.B. DSL Router und DSL Modem).

Ein oder mehrere Clientsysteme können über den Konnektor Anwendungsfälle der
Telematikinfrastruktur initiieren und über den Konnektor und die zentrale
TI-Plattform in Bestandsnetze kommunizieren (rote gestrichelte Linie). Dabei
ist die Nutzung der Anwendungsfälle der Telematikinfrastruktur je nach
Konfiguration des Konnektors entweder nur authentifizierten Clients möglich
oder beliebigen Clients.

In diesem einfachen Szenario werden über ein einziges Kartenterminal die SMC-B,
der HBA und auch die eGK des Versicherten gelesen, es können dazu alternativ
auch mehrere Kartenterminals genutzt werden.

Darüber hinaus können die Clientsysteme über den SIS (Secure Internet
Service) auf Dienste des Internets zugreifen.

### 10.1.2 Voraussetzungen

 ---> UL

### 10.1.3 Auswirkungen

 ---> UL

### 10.2 Szenario 2: Installation mit mehreren Behandlungsräumen

![Abbildung-25][Abbildung-25]

### 10.2.1 Beschreibung des Szenarios

Mit der in Szenario 1 skizzierten Topologie kann auch ein Szenario bedient
werden, bei dem mehrere Behandlungsräume unterstützt werden (siehe Abbildung
26). Dabei ist in jedem Behandlungsraum mindestens ein Kartenterminal
vorzusehen, so dass die eGK gelesen werden kann.

Auf die Darstellung der Kommunikationswege in zentrale Netze wurde in Abbildung
26 verzichtet, da sich hier keine Änderung gegenüber Szenario 1 ergibt.

Durch die Ressourcenverwaltung des Konnektors wird sichergestellt, dass bei
Anwendungsfällen diejenigen Kartenterminals angesprochen werden, welche dem
Arbeitsplatz zugeordnet sind, von dem aus der Anwendungsfall initiiert wurde.

### 10.2.2 Voraussetzungen

 ---> UL

### 10.2.3 Auswirkungen

 ---> UL

### 10.3 Szenario 3: Integration in bestehende Infrastruktur ohne Netzsegmentierung

![Abbildung-26][Abbildung-26]

### 10.3.1 Beschreibung des Szenarios

Im Falle einer bereits vorhandenen Infrastruktur im dezentralen Bereich können
die Produkte der TI, insbesondere der Konnektor, so in die Infrastruktur
integriert werden, dass Bestandsanwendungen bereits erprobte Kommunikationswege
weiter nutzen können.

Wie in Abbildung 27 beispielhaft dargestellt, existiert bereits eine
Infrastruktur, die sowohl einen Internetzugang für die Arbeitsplätze
ermöglicht (gestrichelte Linie in türkis), als auch eine Nebenstelle über
VPN anbindet (gestrichelte Linie in blau). In diesem Fall wird der Konnektor
als zusätzliches Gerät an das bestehende Netzwerk angeschlossen und nutzt den
bereits vorhandenen Internetanschluss zur Kommunikation in die TI.

Für die Clientsysteme muss in diesem Szenario je nach individuellem
Anforderungsprofil entschieden werden, ob das jeweilige Clientsystem über die
Telematikinfrastruktur kommunizieren können soll und den gesicherten
Internetzugang (SIS) nutzen soll oder nicht.

Soll ein Clientsysteme nicht über die Telematikinfrastruktur kommunizieren,
bleibt der IAG als Default-Gateway dieses Clientsystems konfiguriert. In diesem
Fall routet der IAG die eingehenden IP-Pakete mit öffentlichen Zieladressen
weiter in das Internet. Die gestrichelte Linie in türkis zeigt beispielhaft
einen Zugriff in das Internet.

Soll ein Clientsystem über die Telematikinfrastruktur kommunizieren oder den
gesicherten Internetzugang (SIS) nutzen, muss der Konnektor als Default-Gateway
konfiguriert werden. In diesem Fall routet der Konnektor die eingehenden
IP-Pakete, die nicht für ihn bestimmt sind, entweder durch den VPN-Tunnel der
TI über die Telematikinfrastruktur in ein angeschlossenes Bestandsnetz,
(gestrichelte Linie in rot) oder durch den VPN-Tunnel zum SIS (Secure Internet
Service) in das Internet (gestrichelte Linie in grün). Sollte kein sicherer
Internetzugang konfiguriert sein, so würde der Konnektor den Traffic verwerfen
und ggf. per ICMP dem Client eine anderes Gateway (IAG) vorschlagen. Alternativ
können die von den Clients benötigten Routing-Informationen manuell oder per
DHCP konfiguriert werden.

### 10.3.2 Voraussetzungen

 ---> UL

### 10.3.3 Auswirkungen

 ---> UL

### 10.4 Szenario 4: Integration in bestehende Infrastruktur mit Netzsegmentierung

![Abbildung-27][Abbildung-27]

### 10.4.1 Beschreibung des Szenarios

Das vorliegende Szenario skizziert eine etwas komplexere dezentrale Umgebung, in
der das Netzwerk segmentiert ist und dedizierte Router als Default-Gateway für
die Clientsysteme genutzt werden. In diesem Fall kann die Konfiguration der
Clients unverändert bleiben und der Konnektor wird als zusätzliches Gerät in
das Netzwerk integriert und dem Router bekanntgemacht als Gateway für den
sicheren Internetzugang und den Zugang zu den an die Telematikinfrastruktur
angeschlossenen Bestandsnetze.

### 10.4.2 Voraussetzungen

 ---> UL

### 10.4.3 Auswirkungen

 ---> UL

### 10.5 Szenario 5: Zentral gesteckter HBA

![Abbildung-28][Abbildung-28]

### 10.5.1 Beschreibung des Szenarios

Dieses Szenario zeichnet sich dadurch aus dass ein HBA nicht durch seinen
Inhaber mitgeführt und am Arbeitsplatz gesteckt wird, sondern zentral und
geschützt vor unbefugten physischen Zugriffen gesteckt bleibt.

Der HBA-Inhaber greift über jeden konfigurierten Arbeitsplatz auf seinen HBA
zu. Die Remote-PIN-Eingabe erfolgt unter Verwendung des lokal am Arbeitsplatz
vorhandenen eHealth-Kartenterminals.

Die Mechanismen zum Zugriff auf eine zentral gesteckte SMC-B funktionieren
analog zum HBA.

### 10.5.2 Voraussetzungen

Folgende zusätzliche Punkte müssen erfüllt sein, um dieses Szenario
umzusetzen:

 ---> UL

### 10.5.3 Auswirkung

 ---> UL

### 10.6 Szenario 6: Installation mit zentralem PS

![Abbildung-29][Abbildung-29]

### 10.6.1 Beschreibung des Szenarios

Das Szenario skizziert eine dezentrale Konfiguration, bei der das Primärsystem
aus einem Serveranteil „PS Server“ und mehreren Clientanteilen „PS
Client“ besteht. Die Anbindung zwischen dem „PS Server“ und den „PS
Clients“ ist herstellerspezifisch. Der „PS Server“ fungiert als ein
einziges Clientsystem gegenüber der TI bzw. dem Konnektor (z.B. als
Terminalserver). Die Clientsystemschnittstelle des Konnektors wird
ausschließlich vom „PS Server“ genutzt. Der „PS Server“ muss bei der
Kommunikation mit dem Konnektor eine Übersetzung der zugreifenden „PS
Clients“ auf die entsprechende Entität „Arbeitsplatz“ des Konnektors
durchführen

Beispielhaft zeigt das Szenario zwei Arbeitsplätze mit jeweils einem
Kartenterminal für die eGK sowie zentral gesteckte SMC-B und HBAs. Alternativ
sind auch lokal am Arbeitsplatz gesteckte HBAs möglich.

### 10.6.2 Voraussetzungen

 ---> UL

### 10.6.3 Auswirkungen

 ---> UL

### 10.7 Szenario 7: Mehrere Mandanten

![Abbildung-30][Abbildung-30]

### 10.7.1 Beschreibung des Szenarios

Das Szenario skizziert eine dezentrale Konfiguration, bei der mehrere Mandanten
vorhanden sind, wobei jedem Mandant eine eigene SMC-B zugeordnet ist. Die
SMC-Bs sind zentral zusammen mit dem Konnektor geschützt vor unbefugten
physischen Zugriffen installiert. Die Komponenten Arbeitplätze, Clientsysteme
und Kartenterminals müssen eine Zuordnung zum Mandanten haben, wobei
Zuordnungen zu mehreren Mandaten möglich sind. Das Beispiel zeigt einen
Arbeitplatz mit „Clientsystem 1“ und „KT 1“, der zu unterschiedlichen
Zeiten durch verschiedene Mandaten verwendet wird. Zum Zeitpunkt T=t1 greift
ein Anwender 1 mit HBA 1 über einen Anwendungsfall im Kontext Mandat 1 auf die
TI zu, wobei der Versicherte 1 mit eGK 1 am Anwendungsfall beteiligt ist. Zum
Zeitpunkt T=t2 wird ein anderer Anwendungsfall im Kontext von Mandat 2 durch
einen Anwender 2 ohne HBA initiiert, wobei der Versicherte 2 mit eGK 2 am
Anwendungsfall beteiligt ist. Das Clientsystem stellt hierbei den
Mandantenbezug sowie die Nutzer Authentisierung sicher. Als Variante können
auch mehrere Mandanten eine Zuordnung zu einer einzelnen SMC-B haben. Weiterhin
können auch in diesem Szenario HBAs zentral gesteckt werden.

### 10.7.2 Voraussetzungen

 ---> UL

### 10.7.3 Auswirkungen

 ---> UL

### 10.8 Szenario 9: Standalone Konnektor - Physische Trennung

![Abbildung-31][Abbildung-31]

### 10.8.1 Beschreibung des Szenarios

Dieses Szenario stellt eine Variante des Standalone-Szenarios dar, bei dem eine
physische Trennung der Konnektoren eingesetzt wurde.

Im Standalone-Szenario besteht eine Trennung zwischen den Praxissystemen der
dezentralen Umgebung, welche offline (also, ohne Anbindung an die zentrale
TI-Plattform) betrieben werden und den für das Update der eGK durch die
Fachanwendung VSDM notwendigen Komponenten, welche online (also, mit Verbindung
in die zentrale TI-Plattform) betrieben werden.

Die physische Trennung im Standalone-Szenario zeichnet sich dadurch aus, dass
getrennte Komponenten zum Einsatz kommen. Der Online-Konnektor ist mit der
zentralen TI-Plattform verbunden und ermöglicht das VSDM Update der eGKs. Ein
am Online-Konnektor angebundener Kommunikations-PC kann darüber hinaus über
den sicheren Internetzugang der TI auf das Internet und über den
VPN-Konzentrator TI auf Bestandsnetze zugreifen.

Sollten die Online-/Offline-Systeme nicht netztechnisch voneinander getrennt
sein, so obliegt es dem Administrator der Praxissysteme sicherzustellen, dass
die netztechnische Verbindung keine Gefährdung für die Praxissysteme zur
Folge hat.

Im Offline-Konnektor sind einzelne Funktionen nicht verfügbar, andere haben
einen eingeschränkten Funktionsumfang. So kann z.B. eine QES erzeugt oder
geprüft aber dabei keine aktuelle Statusauskunft (OCSP-Response) für die
eingesetzten Zertifikate eingeholt werden. Dies hat zur Folge, dass bei
Erzeugung einer QES keine Statusauskunft für das Signaturzertifikat in die
Signatur eingebettet werden kann und bei einer Prüfung der QES nur eine
eventuell in die Signatur eingebettet Statusauskunft des Zertifikats
berücksichtigt werden kann.

Der Nutzer muss in diesem Fall selber entscheiden ob der gebotene
Funktionsumfang für seinen Anwendungsfall ausreichend ist.

### 10.8.2 Voraussetzungen

Folgende zusätzliche Punkte müssen erfüllt sein, um dieses Szenario
umzusetzen:

 ---> UL

### 10.8.3 Auswirkung

 ---> UL

### 11 Anhang L – Datentypen von Eingangs- und Ausgangsdaten

 ---> TABLE





[Dokumentinformationen]: #dokumentinformationen
[Inhaltsverzeichnis]:    #inhaltsverzeichnis
[1]:                     #1-einordnung-des-dokumentes
[1.1]:                   #11-zielsetzung
[1.2]:                   #12-zielgruppe
[1.3]:                   #13-geltungsbereich
[1.4]:                   #14-abgrenzung-des-dokuments
[1.5]:                   #15-methodik
[1.5.1]:                 #151-anforderungen
[1.5.2]:                 #152-offene-punkte
[1.5.3]:                 #153-erläuterungen-zur-spezifikation-des-außenverhaltens
[1.5.4]:                 #154-erläuterungen-zur-dokumentenstruktur-und-dokumentenmechanismen
[1.5.4.1]:               #1541-modulare-spezifikation-über-funktionsmerkmale
[1.5.4.2]:               #1542-technische-use-cases---tucs
[1.5.4.3]:               #1543-event-mechanismus
[1.5.4.4]:               #1544-konfigurationsparameter-und-zustandswerte
[2]:                     #2-systemüberblick
[2.1]:                   #21-logische-struktur
[2.2]:                   #22-sicherer-datenspeicher
[2.3]:                   #23-überblick-konnektoridentität
[2.4]:                   #24-mandantenfähigkeit
[2.5]:                   #25-versionierung
[2.6]:                   #26-fachanwendungen
[2.7]:                   #27-netzseitige-einsatzszenarien
[2.7.1]:                 #271-parameter-anlw_anbindungs_modus
[2.7.2]:                 #272-parameter-anlw_internet_modus
[2.8]:                   #28-lokale-und-entfernte-kartenterminals
[2.9]:                   #29-standalone-szenario
[3]:                     #3-übergreifende-festlegungen
[3.1]:                   #31-allgemeine-übergreifende-festlegungen
[3.1.1]:                 #311-dokumentformate
[3.1.2]:                 #312-kartentypen
[3.1.3]:                 #313-übergreifende-festlegungen-zum-aufbau-von-sicheren-verbindungen
[3.2]:                   #32-konnektoridentität-und-gsmc-k
[3.2.1]:                 #321-organisatorische-anforderungen-und-sperrprozesse
[3.3]:                   #33-bootup-phase
[3.4]:                   #34-betriebszustand
[3.4.1]:                 #341-betriebsaspekte
[3.5]:                   #35-fachliche-anbindung-der-clientsysteme
[3.5.1]:                 #351-betriebsaspekte
[3.6]:                   #36-clientsystemschnittstelle
[3.6.1]:                 #361-soap-schnittstelle
[3.6.2]:                 #362-statusrückmeldung-und-fehlerbehandlung
[3.6.3]:                 #363-transport-großer-dokumente
[3.7]:                   #37-verwendung-manuell-importierter-ca-zertifikate
[3.8]:                   #38-testunterstützung
[4]:                     #4-funktionsmerkmale
[4.1]:                   #41-anwendungskonnektor
[4.1.1]:                 #411-zugriffsberechtigungsdienst
[4.1.1.1]:               #4111-funktionsmerkmalweite-aspekte
[4.1.1.2]:               #4112-durch-ereignisse-ausgelöste-reaktionen
[4.1.1.3]:               #4113-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.1.1.4]:               #4114-interne-tucs-auch-durch-fachmodule-nutzbar
[4.1.1.4.1]:             #41141-tuc_kon_000-prüfe-zugriffsberechtigung
[4.1.1.5]:               #4115-operationen-an-der-außenschnittstelle
[4.1.1.6]:               #4116-betriebsaspekte
[4.1.2]:                 #412-dokumentvalidierungsdienst
[4.1.2.1]:               #4121-funktionsmerkmalweite-aspekte
[4.1.2.2]:               #4122-durch-ereignisse-ausgelöste-reaktionen
[4.1.2.3]:               #4123-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.1.2.4]:               #4124-interne-tucs-auch-durch-fachmodule-nutzbar
[4.1.2.4.1]:             #41241-tuc_kon_080-dokument-validieren”
[4.1.2.5]:               #4125-operationen-an-der-außenschnittstelle
[4.1.2.6]:               #4126-betriebsaspekte
[4.1.3]:                 #413-dienstverzeichnisdienst
[4.1.3.1]:               #4131-funktionsmerkmalweite-aspekte
[4.1.3.2]:               #4132-durch-ereignisse-ausgelöste-reaktionen
[4.1.3.3]:               #4133-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.1.3.4]:               #4134-interne-tucs-auch-durch-fachmodule-nutzbar
[4.1.3.4.1]:             #41341-tuc_kon_041-einbringen-der-endpunktinformationen-während-der-bootup-phase
[4.1.3.5]:               #4135-operationen-an-der-außenschnittstelle
[4.1.3.6]:               #4136-betriebsaspekte
[4.1.4]:                 #414-kartenterminaldienst
[4.1.4.1]:               #4141-funktionsmerkmalweite-aspekte
[4.1.4.2]:               #4142-durch-ereignisse-ausgelöste-reaktionen
[4.1.4.3]:               #4143-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.1.4.3.1]:             #41431-tuc_kon_050-beginne-kartenterminalsitzung
[4.1.4.3.2]:             #41432-tuc_kon_054-kartenterminal-hinzufügen
[4.1.4.3.3]:             #41433-tuc_kon_053-paire-kartenterminal
[4.1.4.3.4]:             #41434-tuc_kon_055-befülle-ct-object
[4.1.4.4]:               #4144-interne-tucs-auch-durch-fachmodule-nutzbar
[4.1.4.4.1]:             #41441-tuc_kon_051-mit-anwender-über-kartenterminal-interagieren
[4.1.4.4.2]:             #41442-tuc_kon_056-karte-anfordern
[4.1.4.4.3]:             #41443-tuc_kon_057-karte-auswerfen
[4.1.4.4.4]:             #41444-tuc_kon_058-displaygröße-ermitteln
[4.1.4.5]:               #4145-operationen-an-der-außenschnittstelle
[4.1.4.5.1]:             #41451-requestcard
[4.1.4.5.2]:             #41452-ejectcard
[4.1.4.6]:               #4146-betriebsaspekte
[4.1.4.6.1]:             #41461-allgemeine-betriebsaspekte
[4.1.4.6.2]:             #41462-kartenterminals-pflegen
[4.1.4.6.3]:             #41463-import-der-kartenterminal-informationen
[4.1.5]:                 #415-kartendienst
[4.1.5.1]:               #4151-funktionsmerkmalweite-aspekte
[4.1.5.2]:               #4152-durch-ereignisse-ausgelöste-reaktionen
[4.1.5.3]:               #4153-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.1.5.3.1]:             #41531-tuc_kon_001-karte-öffnen
[4.1.5.4]:               #4154-interne-tucs-auch-durch-fachmodule-nutzbar
[4.1.5.4.1]:             #41541-tuc_kon_026-liefere-cardsession
[4.1.5.4.2]:             #41542-tuc_kon_012-pin-verifizieren
[4.1.5.4.3]:             #41543-tuc_kon_019-pin-ändern
[4.1.5.4.4]:             #41544-tuc_kon_021-pin-entsperren
[4.1.5.4.5]:             #41545-tuc_kon_022-liefere-pin-status
[4.1.5.4.6]:             #41546-tuc_kon_027-pin-schutz-ein-/ausschalten
[4.1.5.4.7]:             #41547-tuc_kon_023-karte-reservieren
[4.1.5.4.8]:             #41548-tuc_kon_005-card-to-card-authentisieren
[4.1.5.4.9]:             #41549-tuc_kon_202-lesedatei
[4.1.5.4.10]:            #415410-tuc_kon_203-schreibedatei
[4.1.5.4.11]:            #415411-tuc_kon_204-löschedateiinhalt
[4.1.5.4.12]:            #415412-tuc_kon_209-leserecord
[4.1.5.4.13]:            #415413-tuc_kon_210-schreiberecord
[4.1.5.4.14]:            #415414-tuc_kon_211-löscherecordinhalt
[4.1.5.4.15]:            #415415-tuc_kon_214-fügehinzurecord
[4.1.5.4.16]:            #415416-tuc_kon_215-sucherecord
[4.1.5.4.17]:            #415417-tuc_kon_018-egk-sperrung-prüfen
[4.1.5.4.18]:            #415418-tuc_kon_006-datenzugriffsaudit-egk-schreiben
[4.1.5.4.19]:            #415419-tuc_kon_218-signiere
[4.1.5.4.20]:            #415420-tuc_kon_219-entschlüssele
[4.1.5.4.21]:            #415421-tuc_kon_200-sendeapdu
[4.1.5.4.22]:            #415422-tuc_kon_024-karte-zurücksetzen
[4.1.5.4.23]:            #415423-tuc_kon_216-lesezertifikat
[4.1.5.4.24]:            #415424-tuc_kon_036-lieferefachlicherolle
[4.1.5.5]:               #4155-operationen-an-der-außenschnittstelle
[4.1.5.5.1]:             #41551-verifypin
[4.1.5.5.2]:             #41552-changepin
[4.1.5.5.3]:             #41553-getpinstatus
[4.1.5.5.4]:             #41554-unblockpin
[4.1.5.5.5]:             #41555-enablepin
[4.1.5.5.6]:             #41556-disablepin
[4.1.5.6]:               #4156-betriebsaspekte
[4.1.5.6.1]:             #41561-tuc_kon_025-initialisierung-kartendienst
[4.1.5.6.2]:             #41562-kartenübersicht-und-pin-management
[4.1.6]:                 #416-systeminformationsdienst
[4.1.6.1]:               #4161-funktionsmerkmalweite-aspekte
[4.1.6.2]:               #4162-durch-ereignisse-ausgelöste-reaktionen
[4.1.6.3]:               #4163-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.1.6.4]:               #4164-interne-tucs-auch-durch-fachmodule-nutzbar
[4.1.6.4.1]:             #41641-tuc_kon_256-systemereignis-absetzen
[4.1.6.4.2]:             #41642-tuc_kon_252-liefere-kt_liste
[4.1.6.4.3]:             #41643-tuc_kon_253-liefere-karten_liste
[4.1.6.4.4]:             #41644-tuc_kon_254-liefere-ressourcendetails
[4.1.6.5]:               #4165-operationen-an-der-außenschnittstelle
[4.1.6.5.1]:             #41651-getcardterminals
[4.1.6.5.2]:             #41652-getcards
[4.1.6.5.3]:             #41653-getresourceinformation
[4.1.6.5.4]:             #41654-subscribe
[4.1.6.5.5]:             #41655-unsubscribe
[4.1.6.5.6]:             #41656-renewsubscriptions
[4.1.6.5.7]:             #41657-getsubscription
[4.1.6.6]:               #4166-betriebsaspekte
[4.1.7]:                 #417-verschlüsselungsdienst
[4.1.7.1]:               #4171-funktionsmerkmalweite-aspekte
[4.1.7.2]:               #4172-durch-ereignisse-ausgelöste-reaktionen
[4.1.7.3]:               #4173-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.1.7.4]:               #4174-interne-tucs-auch-durch-fachmodule-nutzbar
[4.1.7.4.1]:             #41741-tuc_kon_070-daten-hybrid-verschlüsseln”
[4.1.7.4.2]:             #41742-tuc_kon_071-daten-hybrid-entschlüsseln”
[4.1.7.4.3]:             #41743-tuc_kon_072-daten-symmetrisch-verschlüsseln”
[4.1.7.4.4]:             #41744-tuc_kon_073-daten-symmetrisch-entschlüsseln”
[4.1.7.4.5]:             #41745-tuc_kon_075-symmetrisch-verschlüsseln
[4.1.7.4.6]:             #41746-tuc_kon_076-symmetrisch-entschlüsseln
[4.1.7.5]:               #4175-operationen-an-der-außenschnittstelle
[4.1.7.5.1]:             #41751-encryptdocument
[4.1.7.5.2]:             #41752-decryptdocument
[4.1.7.6]:               #4176-betriebsaspekte
[4.1.8]:                 #418-signaturdienst
[4.1.8.1]:               #4181-funktionsmerkmalweite-aspekte
[4.1.8.1.1]:             #41811-dokumentensignatur
[4.1.8.1.2]:             #41812-signaturrichtlinien
[4.1.8.1.3]:             #41813-signaturzeitpunkt
[4.1.8.1.4]:             #41814-jobnummer
[4.1.8.1.5]:             #41815-komfortsignatur
[4.1.8.2]:               #4182-durch-ereignisse-ausgelöste-reaktionen
[4.1.8.3]:               #4183-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.1.8.3.1]:             #41831-tuc_kon_155-dokumente-zur-signatur-vorbereiten”
[4.1.8.3.2]:             #41832-tuc_kon_165-signaturvoraussetzungen-für-nonqes-prüfen
[4.1.8.3.3]:             #41833-tuc_kon_166-nonqes-signaturen-erstellen
[4.1.8.3.4]:             #41834-tuc_kon_152-signaturvoraussetzungen-für-qes-prüfen
[4.1.8.3.5]:             #41835-tuc_kon_154-qes-signaturen-erstellen
[4.1.8.3.6]:             #41836-tuc_kon_168-einzelsignatur-qes-erstellen
[4.1.8.3.7]:             #41837-tuc_kon_158-komfortsignaturen-erstellen
[4.1.8.4]:               #4184-interne-tucs-auch-durch-fachmodule-nutzbar
[4.1.8.4.1]:             #41841-tuc_kon_160-dokumente-nonqes-signieren”
[4.1.8.4.2]:             #41842-tuc_kon_161-nonqes-dokumentsignatur-prüfen”
[4.1.8.4.3]:             #41843-tuc_kon_162-kryptographische-prüfung-der-xml-dokumentensignatur”
[4.1.8.4.4]:             #41844-tuc_kon_150-dokumente-qes-signieren”
[4.1.8.4.5]:             #41845-anforderungen-an-die-stapelsignatur
[4.1.8.4.6]:             #41846-tuc_kon_151-qes-dokumentensignatur-prüfen
[4.1.8.4.7]:             #41847-tuc_kon_170-dokumente-mit-komfort-signieren”
[4.1.8.4.8]:             #41848-tuc_kon_171-komfortsignatur-einschalten”
[4.1.8.4.9]:             #41849-tuc_kon_172-komfortsignatur-ausschalten”
[4.1.8.4.10]:            #418410-tuc_kon_173-liefere-signaturmodus”
[4.1.8.5]:               #4185-operationen-an-der-außenschnittstelle
[4.1.8.5.1]:             #41851-signdocument-nonqes-und-qes
[4.1.8.5.2]:             #41852-verifydocument-nonqes-und-qes
[4.1.8.5.3]:             #41853-stopsignature
[4.1.8.5.4]:             #41854-getjobnumber
[4.1.8.5.5]:             #41855-activatecomfortsignature
[4.1.8.5.6]:             #41856-deactivatecomfortsignature
[4.1.8.5.7]:             #41857-getsignaturemode
[4.1.8.6]:               #4186-betriebsaspekte
[4.1.9]:                 #419-zertifikatsdienst
[4.1.9.1]:               #4191-funktionsmerkmalweite-aspekte
[4.1.9.2]:               #4192-durch-ereignisse-ausgelöste-reaktionen
[4.1.9.3]:               #4193-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.1.9.3.1]:             #41931-tuc_kon_032-tsl-aktualisieren
[4.1.9.3.2]:             #41932-tuc_kon_031-bnetza-vl-aktualisieren
[4.1.9.3.3]:             #41933-tuc_kon_040-crl-aktualisieren
[4.1.9.3.4]:             #41934-tuc_kon_033-zertifikatsablauf-prüfen
[4.1.9.4]:               #4194-interne-tucs-auch-durch-fachmodule-nutzbar
[4.1.9.4.1]:             #41941-tuc_kon_037-zertifikat-prüfen
[4.1.9.4.2]:             #41942-tuc_kon_042-cv-zertifikat-prüfen
[4.1.9.4.3]:             #41943-tuc_kon_034-zertifikatsinformationen-extrahieren
[4.1.9.5]:               #4195-operationen-an-der-außenschnittstelle
[4.1.9.5.1]:             #41951-checkcertificateexpiration
[4.1.9.5.2]:             #41952-readcardcertificate
[4.1.9.5.3]:             #41953-verifycertificate
[4.1.9.6]:               #4196-betriebsaspekte
[4.1.9.6.1]:             #41961-tuc_kon_035-zertifikatsdienst-initialisieren
[4.1.10]:                #4110-protokollierungsdienst
[4.1.10.1]:              #41101-funktionsmerkmalweite-aspekte
[4.1.10.2]:              #41102-durch-ereignisse-ausgelöste-reaktionen
[4.1.10.3]:              #41103-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.1.10.4]:              #41104-interne-tucs-auch-durch-fachmodule-nutzbar
[4.1.10.4.1]:            #411041-tuc_kon_271-schreibe-protokolleintrag
[4.1.10.5]:              #41105-operationen-an-der-außenschnittstelle
[4.1.10.6]:              #41106-betriebsaspekte
[4.1.10.6.1]:            #411061-tuc_kon_272-initialisierung-protokollierungsdienst
[4.1.11]:                #4111-tls-dienst
[4.1.11.1]:              #41111-funktionsmerkmalweite-aspekte
[4.1.11.2]:              #41112-durch-ereignisse-ausgelöste-reaktionen
[4.1.11.3]:              #41113-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.1.11.4]:              #41114-interne-tucs-auch-durch-fachmodule-nutzbar
[4.1.11.4.1]:            #411141-tuc_kon_110-kartenbasierte-tls-verbindung-aufbauen
[4.1.11.4.2]:            #411142-tuc_kon_111-kartenbasierte-tls-verbindung-abbauen
[4.1.11.5]:              #41115-operationen-an-der-außenschnittstelle
[4.1.11.6]:              #41116-betriebsaspekte
[4.1.12]:                #4112-ldap-proxy
[4.1.12.1]:              #41121-funktionsmerkmalweite-aspekte
[4.1.12.2]:              #41122-durch-ereignisse-ausgelöste-reaktionen
[4.1.12.3]:              #41123-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.1.12.4]:              #41124-interne-tucs-auch-durch-fachmodule-nutzbar
[4.1.12.4.1]:            #411241-tuc_kon_290-ldap-verbindung-aufbauen
[4.1.12.4.2]:            #411242-tuc_kon_291-verzeichnis-abfragen
[4.1.12.4.3]:            #411243-tuc_kon_292-ldap-verbindung-trennen
[4.1.12.4.4]:            #411244-tuc_kon_293-verzeichnisabfrage-abbrechen
[4.1.12.5]:              #41125-operationen-an-der-außenschnittstelle
[4.1.12.5.1]:            #411251-unterstützte-ldapv3-operationen
[4.1.12.6]:              #41126-betriebsaspekte
[4.1.13]:                #4113-authentifizierungsdienst
[4.1.13.1]:              #41131-funktionsmerkmalweite-aspekte
[4.1.13.1.1]:            #411311-externe-authentisierung
[4.1.13.2]:              #41132-durch-ereignisse-ausgelöste-reaktionen
[4.1.13.3]:              #41133-interne-tucs
[4.1.13.4]:              #41134-operationen-an-der-außenschnittstelle
[4.1.13.4.1]:            #411341-externalauthenticate
[4.1.13.5]:              #41135-betriebsaspekte
[4.1.14]:                #4114-betriebsdatenmeldedienst
[4.2]:                   #42-netzkonnektor
[4.2.1]:                 #421-anbindung-lan/wan
[4.2.1.1]:               #4211-funktionsmerkmalweite-aspekte
[4.2.1.1.1]:             #42111-netzwerksegmentierung
[4.2.1.1.2]:             #42112-routing-und-firewall
[4.2.1.2]:               #4212-durch-ereignisse-ausgelöste-reaktionen
[4.2.1.3]:               #4213-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.2.1.3.1]:             #42131-tuc_kon_305-lan-adapter-initialisieren
[4.2.1.3.2]:             #42132-tuc_kon_306-wan-adapter-initialisieren
[4.2.1.3.3]:             #42133-tuc_kon_304-netzwerk-routen-einrichten
[4.2.1.4]:               #4214-interne-tucs-auch-durch-fachmodule-nutzbar
[4.2.1.5]:               #4215-operationen-an-der-außenschnittstelle
[4.2.1.6]:               #4216-betriebsaspekte
[4.2.2]:                 #422-dhcp-server
[4.2.2.1]:               #4221-funktionsmerkmalweite-aspekte
[4.2.2.2]:               #4222-durch-ereignisse-ausgelöste-reaktionen
[4.2.2.3]:               #4223-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.2.2.4]:               #4224-interne-tucs-auch-durch-fachmodule-nutzbar
[4.2.2.5]:               #4225-operationen-an-der-außenschnittstelle
[4.2.2.5.1]:             #42251-liefere-netzwerkinformationen-über-dhcp
[4.2.2.6]:               #4226-betriebsaspekte
[4.2.2.6.1]:             #42261-tuc_kon_343-initialisierung-dhcp-server
[4.2.3]:                 #423-dhcp-client
[4.2.3.1]:               #4231-funktionsmerkmalweite-aspekte
[4.2.3.2]:               #4232-durch-ereignisse-ausgelöste-reaktionen
[4.2.3.3]:               #4233-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.2.3.3.1]:             #42331-tuc_kon_341-dhcp-informationen-beziehen
[4.2.3.4]:               #4234-interne-tucs-auch-durch-fachmodule-nutzbar
[4.2.3.5]:               #4235-operationen-an-der-außenschnittstelle
[4.2.3.6]:               #4236-betriebsaspekte
[4.2.4]:                 #424-vpn-client
[4.2.4.1]:               #4241-funktionsmerkmalweite-aspekte
[4.2.4.2]:               #4242-durch-ereignisse-ausgelöste-reaktionen
[4.2.4.3]:               #4243-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.2.4.3.1]:             #42431-tuc_kon_321-verbindung-zu-dem-vpn-konzentrator-der-ti-aufbauen
[4.2.4.3.2]:             #42432-tuc_kon_322-verbindung-zu-dem-vpn-konzentrator-des-sis-aufbauen
[4.2.4.4]:               #4244-interne-tucs-auch-durch-fachmodule-nutzbar
[4.2.4.5]:               #4245-operationen-an-der-außenschnittstelle
[4.2.4.6]:               #4246-betriebsaspekte
[4.2.5]:                 #425-zeitdienst
[4.2.5.1]:               #4251-funktionsmerkmalweite-aspekte
[4.2.5.2]:               #4252-durch-ereignisse-ausgelöste-reaktionen
[4.2.5.3]:               #4253-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.2.5.4]:               #4254-interne-tucs-auch-durch-fachmodule-nutzbar
[4.2.5.4.1]:             #42541-tuc_kon_351-liefere-systemzeit”
[4.2.5.5]:               #4255-operationen-an-der-außenschnittstelle
[4.2.5.5.1]:             #42551-sync_time
[4.2.5.6]:               #4256-betriebsaspekte
[4.2.5.6.1]:             #42561-tuc_kon_352-initialisierung-zeitdienst
[4.2.6]:                 #426-namensdienst-und-dienstlokalisierung
[4.2.6.1]:               #4261-funktionsmerkmalweite-aspekte
[4.2.6.2]:               #4262-durch-ereignisse-ausgelöste-reaktionen
[4.2.6.3]:               #4263-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.2.6.4]:               #4264-interne-tucs-auch-durch-fachmodule-nutzbar
[4.2.6.4.1]:             #42641-tuc_kon_361-dns-namen-auflösen
[4.2.6.4.2]:             #42642-tuc_kon_362-liste-der-dienste-abrufen
[4.2.6.4.3]:             #42643-tuc_kon_363-dienstdetails-abrufen
[4.2.6.5]:               #4265-operationen-an-der-außenschnittstelle
[4.2.6.5.1]:             #42651-getipaddress
[4.2.6.6]:               #4266-betriebsaspekte
[4.2.7]:                 #427-optionale-verwendung-von-ipv6
[4.3]:                   #43-konnektormanagement
[4.3.1]:                 #431-zugang-und-benutzerverwaltung-des-konnektormanagements
[4.3.2]:                 #432-konnektorname-und-versionsinformationen
[4.3.3]:                 #433-konfigurationsdaten-persistieren-sowie-export-import
[4.3.4]:                 #434-administration-von-fachmodulen
[4.3.5]:                 #435-neustart-und-werksreset
[4.3.6]:                 #436-leistungsumfänge-und-standalone-szenarios
[4.3.7]:                 #437-online-anbindung-verwalten
[4.3.8]:                 #438-re-registrierung-des-konnektors-mit-weiterem-nk-zertifikat
[4.3.9]:                 #439-remote-management-optional
[4.3.10]:                #4310-software--und-konfigurationsaktualisierung-ksr-client
[4.3.10.1]:              #43101-funktionsmerkmalweite-aspekte
[4.3.10.2]:              #43102-durch-ereignisse-ausgelöste-reaktionen
[4.3.10.3]:              #43103-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.3.10.3.1]:            #431031-tuc_kon_280-konnektoraktualisierung-durchführen
[4.3.10.3.2]:            #431032-tuc_kon_281-kartenterminalaktualisierung-anstoßen
[4.3.10.3.3]:            #431033-tuc_kon_282-updateinformationen-beziehen
[4.3.10.3.4]:            #431034-tuc_kon_283-infrastruktur-konfiguration-aktualisieren
[4.3.10.4]:              #43104-interne-tucs-auch-durch-fachmodule-nutzbar
[4.3.10.4.1]:            #431041-tuc_kon_285-updateinformationen-für-fachmodul-beziehen
[4.3.10.4.2]:            #431042-tuc_kon_286-paket-für-fachmodul-laden
[4.3.10.5]:              #43105-operationen-an-der-außenschnittstelle
[4.3.10.6]:              #43106-betriebsaspekte
[4.3.10.6.1]:            #431061-tuc_kon_284-ksr-client-initialisieren
[4.3.11]:                #4311-konnektorstatus
[4.4]:                   #44-hardware-merkmale-des-konnektors
[5]:                     #5-anhang-a-–-verzeichnisse
[5.1]:                   #51-abkürzungen
[5.2]:                   #52-glossar
[5.3]:                   #53-abbildungsverzeichnis
[5.4]:                   #54-tabellenverzeichnis
[5.5]:                   #55-referenzierte-dokumente
[5.5.1]:                 #551-dokumente-der-gematik
[5.5.2]:                 #552-weitere-dokumente
[6]:                     #6-anhang-b-–-profilierung-der-signatur--und-verschlüsselungsformate-normativ
[6.1]:                   #61-profilierung-der-verschlüsselungsformate
[6.2]:                   #62-profilierung-der-signaturformate
[6.3]:                   #63-profilierung-verificationreport
[6.4]:                   #64-profilierung-der-dokumentenformate-und-nachrichten
[7]:                     #7-anhang-f-–-übersicht-events
[8]:                     #8-anhang-h-–-mapping-von-architektur-der-ti-plattform-auf-konnektorspezifikation
[9]:                     #9-anhang-i-–-umsetzungshinweise-informativ
[9.1]:                   #91-systemüberblick
[9.1.1]:                 #911-–-hinweise-zur-sicherheitsevaluierung-nach-common-criteria
[9.1.1.1]:               #9111-separationsmechanismen-des-konnektors
[9.1.1.2]:               #9112-granularität-der-tsf
[9.2]:                   #92-übergreifende-festlegungen
[9.2.1]:                 #921-interne-mechanismen
[9.2.1.1]:               #9211-zufallszahlen-und-schlüssel
[9.3]:                   #93-funktionsmerkmale
[9.3.1]:                 #931-anwendungskonnektor
[9.3.1.1]:               #9311-administration-des-informationsmodells
[9.3.1.2]:               #9312-vorgehensvariante-für-das-handling-von-cardsessions
[9.3.1.3]:               #9313-darstellung-von-terminal-anzeigen-auf-einem-kartenterminal
[10]:                    #10-anhang-k-–-szenarien-im-dezentralen-umfeld
[10.1]:                  #101-szenario-1-einfache-installation-ohne-spezielle-anforderungen-und-ohne-bestehende-infrastruktur
[10.1.1]:                #1011-beschreibung-des-szenarios
[10.1.2]:                #1012-voraussetzungen
[10.1.3]:                #1013-auswirkungen
[10.2]:                  #102-szenario-2-installation-mit-mehreren-behandlungsräumen
[10.2.1]:                #1021-beschreibung-des-szenarios
[10.2.2]:                #1022-voraussetzungen
[10.2.3]:                #1023-auswirkungen
[10.3]:                  #103-szenario-3-integration-in-bestehende-infrastruktur-ohne-netzsegmentierung
[10.3.1]:                #1031-beschreibung-des-szenarios
[10.3.2]:                #1032-voraussetzungen
[10.3.3]:                #1033-auswirkungen
[10.4]:                  #104-szenario-4-integration-in-bestehende-infrastruktur-mit-netzsegmentierung
[10.4.1]:                #1041-beschreibung-des-szenarios
[10.4.2]:                #1042-voraussetzungen
[10.4.3]:                #1043-auswirkungen
[10.5]:                  #105-szenario-5-zentral-gesteckter-hba
[10.5.1]:                #1051-beschreibung-des-szenarios
[10.5.2]:                #1052-voraussetzungen
[10.5.3]:                #1053-auswirkung
[10.6]:                  #106-szenario-6-installation-mit-zentralem-ps
[10.6.1]:                #1061-beschreibung-des-szenarios
[10.6.2]:                #1062-voraussetzungen
[10.6.3]:                #1063-auswirkungen
[10.7]:                  #107-szenario-7-mehrere-mandanten
[10.7.1]:                #1071-beschreibung-des-szenarios
[10.7.2]:                #1072-voraussetzungen
[10.7.3]:                #1073-auswirkungen
[10.8]:                  #108-szenario-9-standalone-konnektor---physische-trennung
[10.8.1]:                #1081-beschreibung-des-szenarios
[10.8.2]:                #1082-voraussetzungen
[10.8.3]:                #1083-auswirkung
[11]:                    #11-anhang-l-–-datentypen-von-eingangs--und-ausgangsdaten
[Abbildung-1]:           gemSpec_Kon_V5.18.0.attachments/11372500556585029303.png
[Abbildung-2]:           gemSpec_Kon_V5.18.0.attachments/597812103449717399.png
[Abbildung-3]:           gemSpec_Kon_V5.18.0.attachments/452543610749890073.png
[Abbildung-4]:           gemSpec_Kon_V5.18.0.attachments/3253016863505255554.emf
[Abbildung-5]:           gemSpec_Kon_V5.18.0.attachments/5885552658699712675.png
[Abbildung-6]:           gemSpec_Kon_V5.18.0.attachments/2737851721132666970.emf
[Img-007]:               gemSpec_Kon_V5.18.0.attachments/5446061706879125634.png
[Abbildung-7]:           gemSpec_Kon_V5.18.0.attachments/8656477943409294784.emf
[Img-009]:               gemSpec_Kon_V5.18.0.attachments/4238673678557912379.emf
[Abbildung-9]:           gemSpec_Kon_V5.18.0.attachments/5553279804750508008.emf
[Img-011]:               gemSpec_Kon_V5.18.0.attachments/16835580620461563295.emf
[Img-012]:               gemSpec_Kon_V5.18.0.attachments/560025191717672503.emf
[Abbildung-13]:          gemSpec_Kon_V5.18.0.attachments/293107814685344665.png
[Img-014]:               gemSpec_Kon_V5.18.0.attachments/4935412250355692970.emf
[Abbildung-15]:          gemSpec_Kon_V5.18.0.attachments/1166144241643877153.png
[Abbildung-16]:          gemSpec_Kon_V5.18.0.attachments/15903632354578786558.emf
[Abbildung-17]:          gemSpec_Kon_V5.18.0.attachments/13571335905733562869.png
[Img-018]:               gemSpec_Kon_V5.18.0.attachments/4615707335606718182.emf
[Img-019]:               gemSpec_Kon_V5.18.0.attachments/1777103963067446278.emf
[Abbildung-20]:          gemSpec_Kon_V5.18.0.attachments/4679305598564690814.emf
[Abbildung-21]:          gemSpec_Kon_V5.18.0.attachments/377569428305567874.png
[Img-022]:               gemSpec_Kon_V5.18.0.attachments/8792316216455315176.png
[Abbildung-23]:          gemSpec_Kon_V5.18.0.attachments/1680130296516442956.emf
[Abbildung-24]:          gemSpec_Kon_V5.18.0.attachments/17762408187233769204.emf
[Abbildung-25]:          gemSpec_Kon_V5.18.0.attachments/11140954224183461378.emf
[Abbildung-26]:          gemSpec_Kon_V5.18.0.attachments/14159813432999277364.emf
[Abbildung-27]:          gemSpec_Kon_V5.18.0.attachments/5644381610894428272.emf
[Abbildung-28]:          gemSpec_Kon_V5.18.0.attachments/17364015577677169346.emf
[Abbildung-29]:          gemSpec_Kon_V5.18.0.attachments/7972339229766263266.emf
[Abbildung-30]:          gemSpec_Kon_V5.18.0.attachments/3336173011312695993.png
[Abbildung-31]:          gemSpec_Kon_V5.18.0.attachments/7031299863855507289.emf
[Tbl-001]:               #Tbl-001 (&94498804047752)
[Tbl-002]:               #Tbl-002 (&94498804829848)
[Tbl-003]:               #Tbl-003 (&94498804871104)
[Tabelle-1]:             #Tabelle-1 (&94498804912760)
[Tabelle-2]:             #Tabelle-2 (&94498804925080)
[Tabelle-3]:             #Tabelle-3 (&94498804943144)
[Tabelle-4]:             #Tabelle-4 (&94498794786456)
[Tabelle-5]:             #Tabelle-5 (&94498794950256)
[Tabelle-6]:             #Tabelle-6 (&94498805821440)
[Tabelle-7]:             #Tabelle-7 (&94498806897120)
[Tbl-011]:               #Tbl-011 (&94498806916968)
[Tabelle-9]:             #Tabelle-9 (&94498806974424)
[Tabelle-10]:            #Tabelle-10 (&94498796059840)
[Tabelle-11]:            #Tabelle-11 (&94498796119184)
[Tabelle-12]:            #Tabelle-12 (&94498796316816)
[Tabelle-13]:            #Tabelle-13 (&94498796462856)
[Tabelle-14]:            #Tabelle-14 (&94498794445560)
[Tabelle-15]:            #Tabelle-15 (&94498794494864)
[Tabelle-16]:            #Tabelle-16 (&94498797870608)
[Tabelle-17]:            #Tabelle-17 (&94498798069720)
[Tabelle-18]:            #Tabelle-18 (&94498798145280)
[Tabelle-19]:            #Tabelle-19 (&94498798561288)
[Tabelle-20]:            #Tabelle-20 (&94498799247120)
[Tabelle-21]:            #Tabelle-21 (&94498799691344)
[Tabelle-22]:            #Tabelle-22 (&94498799885896)
[Tabelle-23]:            #Tabelle-23 (&94498799973792)
[Tabelle-24]:            #Tabelle-24 (&94498800030016)
[Tbl-028]:               #Tbl-028 (&94498800103944)
[Tabelle-26]:            #Tabelle-26 (&94498800332016)
[Tabelle-27]:            #Tabelle-27 (&94498800384464)
[Tabelle-28]:            #Tabelle-28 (&94498800475440)
[Tbl-032]:               #Tbl-032 (&94498800494752)
[Tabelle-30]:            #Tabelle-30 (&94498800746832)
[Tabelle-31]:            #Tabelle-31 (&94498801562104)
[Tabelle-32]:            #Tabelle-32 (&94498801588344)
[Tabelle-33]:            #Tabelle-33 (&94498801723888)
[Tabelle-34]:            #Tabelle-34 (&94498801936872)
[Tabelle-35]:            #Tabelle-35 (&94498802738016)
[Tabelle-36]:            #Tabelle-36 (&94498802827936)
[Tabelle-37]:            #Tabelle-37 (&94498802863184)
[Tabelle-38]:            #Tabelle-38 (&94498803032712)
[Tabelle-39]:            #Tabelle-39 (&94498803069152)
[Tabelle-40]:            #Tabelle-40 (&94498803720400)
[Tabelle-41]:            #Tabelle-41 (&94498803812728)
[Tabelle-42]:            #Tabelle-42 (&94498803832128)
[Tabelle-43]:            #Tabelle-43 (&94498807111672)
[Tabelle-44]:            #Tabelle-44 (&94498807218792)
[Tabelle-45]:            #Tabelle-45 (&94498807292920)
[Tabelle-46]:            #Tabelle-46 (&94498807350712)
[Tabelle-47]:            #Tabelle-47 (&94498807458456)
[Tabelle-48]:            #Tabelle-48 (&94498807478072)
[Tabelle-49]:            #Tabelle-49 (&94498807513232)
[Tabelle-50]:            #Tabelle-50 (&94498807571848)
[Tabelle-51]:            #Tabelle-51 (&94498807606000)
[Tabelle-52]:            #Tabelle-52 (&94498807679680)
[Tabelle-53]:            #Tabelle-53 (&94498807730256)
[Tabelle-54]:            #Tabelle-54 (&94498807767064)
[Tabelle-55]:            #Tabelle-55 (&94498807804680)
[Tabelle-56]:            #Tabelle-56 (&94498807858624)
[Tabelle-57]:            #Tabelle-57 (&94498807932320)
[Tabelle-58]:            #Tabelle-58 (&94498808037064)
[Tabelle-59]:            #Tabelle-59 (&94498808170920)
[Tabelle-60]:            #Tabelle-60 (&94498808654808)
[Tabelle-61]:            #Tabelle-61 (&94498809155568)
[Tabelle-62]:            #Tabelle-62 (&94498809225328)
[Tabelle-63]:            #Tabelle-63 (&94498809281992)
[Tabelle-64]:            #Tabelle-64 (&94498809301016)
[Tabelle-65]:            #Tabelle-65 (&94498809470960)
[Tabelle-66]:            #Tabelle-66 (&94498810295720)
[Tabelle-67]:            #Tabelle-67 (&94498810428272)
[Tabelle-68]:            #Tabelle-68 (&94498810562872)
[Tabelle-69]:            #Tabelle-69 (&94498810703168)
[Tabelle-70]:            #Tabelle-70 (&94498810831344)
[Tabelle-71]:            #Tabelle-71 (&94498810891256)
[Tabelle-72]:            #Tabelle-72 (&94498810915512)
[Tabelle-73]:            #Tabelle-73 (&94498811107408)
[Tabelle-74]:            #Tabelle-74 (&94498811124984)
[Tabelle-75]:            #Tabelle-75 (&94498811172920)
[Tabelle-76]:            #Tabelle-76 (&94498811237184)
[Tabelle-77]:            #Tabelle-77 (&94498811268112)
[Tabelle-78]:            #Tabelle-78 (&94498811408064)
[Tabelle-79]:            #Tabelle-79 (&94498811423064)
[Tabelle-80]:            #Tabelle-80 (&94498811502560)
[Tabelle-81]:            #Tabelle-81 (&94498811560232)
[Tabelle-82]:            #Tabelle-82 (&94498811680848)
[Tabelle-83]:            #Tabelle-83 (&94498811716816)
[Tabelle-84]:            #Tabelle-84 (&94498811797896)
[Tabelle-85]:            #Tabelle-85 (&94498811850120)
[Tabelle-86]:            #Tabelle-86 (&94498811969928)
[Tabelle-87]:            #Tabelle-87 (&94498812022448)
[Tabelle-88]:            #Tabelle-88 (&94498812092472)
[Tabelle-89]:            #Tabelle-89 (&94498812139544)
[Tabelle-90]:            #Tabelle-90 (&94498812259456)
[Tabelle-91]:            #Tabelle-91 (&94498812306288)
[Tabelle-92]:            #Tabelle-92 (&94498812378200)
[Tabelle-93]:            #Tabelle-93 (&94498812430064)
[Tabelle-94]:            #Tabelle-94 (&94498812549416)
[Tabelle-95]:            #Tabelle-95 (&94498812590256)
[Tabelle-96]:            #Tabelle-96 (&94498812662920)
[Tabelle-97]:            #Tabelle-97 (&94498812704560)
[Tabelle-98]:            #Tabelle-98 (&94498812822552)
[Tabelle-99]:            #Tabelle-99 (&94498812842328)
[Tabelle-100]:           #Tabelle-100 (&94498812904504)
[Tabelle-101]:           #Tabelle-101 (&94498812929216)
[Tabelle-102]:           #Tabelle-102 (&94498812994416)
[Tabelle-103]:           #Tabelle-103 (&94498813400936)
[Tabelle-104]:           #Tabelle-104 (&94498813473360)
[Tabelle-105]:           #Tabelle-105 (&94498813514424)
[Tabelle-106]:           #Tabelle-106 (&94498813581376)
[Tabelle-107]:           #Tabelle-107 (&94498813660896)
[Tabelle-108]:           #Tabelle-108 (&94498813722024)
[Tabelle-109]:           #Tabelle-109 (&94498813746896)
[Tabelle-110]:           #Tabelle-110 (&94498813802512)
[Tabelle-111]:           #Tabelle-111 (&94498813827608)
[Tabelle-112]:           #Tabelle-112 (&94498813946496)
[Tabelle-113]:           #Tabelle-113 (&94498813977240)
[Tabelle-114]:           #Tabelle-114 (&94498814026808)
[Tabelle-115]:           #Tabelle-115 (&94498814157560)
[Tabelle-116]:           #Tabelle-116 (&94498814209704)
[Tabelle-117]:           #Tabelle-117 (&94498814239920)
[Tabelle-118]:           #Tabelle-118 (&94498814472096)
[Tabelle-119]:           #Tabelle-119 (&94498814518528)
[Tabelle-120]:           #Tabelle-120 (&94498814549608)
[Tabelle-121]:           #Tabelle-121 (&94498814794816)
[Tabelle-122]:           #Tabelle-122 (&94498814835680)
[Tabelle-123]:           #Tabelle-123 (&94498814872328)
[Tabelle-124]:           #Tabelle-124 (&94498815001072)
[Tabelle-125]:           #Tabelle-125 (&94498815048864)
[Tabelle-126]:           #Tabelle-126 (&94498815073576)
[Tabelle-127]:           #Tabelle-127 (&94498815200904)
[Tabelle-128]:           #Tabelle-128 (&94498815249816)
[Tabelle-129]:           #Tabelle-129 (&94498815280608)
[Tabelle-130]:           #Tabelle-130 (&94498815357776)
[Tabelle-131]:           #Tabelle-131 (&94498815457040)
[Tabelle-132]:           #Tabelle-132 (&94498815488208)
[Tabelle-133]:           #Tabelle-133 (&94498815503760)
[Tbl-137]:               #Tbl-137 (&94498815602320)
[Tabelle-135]:           #Tabelle-135 (&94498815927024)
[Tabelle-136]:           #Tabelle-136 (&94498816809712)
[Tabelle-137]:           #Tabelle-137 (&94498816828792)
[Tabelle-138]:           #Tabelle-138 (&94498816893000)
[Tabelle-139]:           #Tabelle-139 (&94498816970832)
[Tabelle-140]:           #Tabelle-140 (&94498816990704)
[Tabelle-141]:           #Tabelle-141 (&94498817123144)
[Tabelle-142]:           #Tabelle-142 (&94498817164488)
[Tbl-146]:               #Tbl-146 (&94498817216824)
[Tbl-147]:               #Tbl-147 (&94498817347168)
[Tbl-148]:               #Tbl-148 (&94498817388688)
[Tabelle-146]:           #Tabelle-146 (&94498817406936)
[Tabelle-147]:           #Tabelle-147 (&94498817617800)
[Tabelle-148]:           #Tabelle-148 (&94498817710544)
[Tabelle-149]:           #Tabelle-149 (&94498817729448)
[Tabelle-150]:           #Tabelle-150 (&94498817899848)
[Tabelle-151]:           #Tabelle-151 (&94498817952256)
[Tbl-155]:               #Tbl-155 (&94498817973760)
[Tbl-156]:               #Tbl-156 (&94498818047504)
[Tbl-157]:               #Tbl-157 (&94498818143560)
[Tbl-158]:               #Tbl-158 (&94498818164176)
[Tbl-159]:               #Tbl-159 (&94498818217016)
[Tbl-160]:               #Tbl-160 (&94498818575144)
[Tbl-161]:               #Tbl-161 (&94498818600776)
[Tbl-162]:               #Tbl-162 (&94498818708056)
[Tbl-163]:               #Tbl-163 (&94498818751888)
[Tbl-164]:               #Tbl-164 (&94498818777520)
[Tbl-165]:               #Tbl-165 (&94498818899112)
[Tbl-166]:               #Tbl-166 (&94498818935320)
[Tbl-167]:               #Tbl-167 (&94498818962784)
[Tbl-168]:               #Tbl-168 (&94498819002200)
[Tabelle-166]:           #Tabelle-166 (&94498819029504)
[Tabelle-167]:           #Tabelle-167 (&94498819172936)
[Tabelle-168]:           #Tabelle-168 (&94498819196216)
[Tabelle-169]:           #Tabelle-169 (&94498819331792)
[Tabelle-170]:           #Tabelle-170 (&94498819470392)
[Tabelle-171]:           #Tabelle-171 (&94498819514936)
[Tabelle-172]:           #Tabelle-172 (&94498819581392)
[Tabelle-173]:           #Tabelle-173 (&94498820350216)
[Tabelle-174]:           #Tabelle-174 (&94498820406200)
[Tabelle-175]:           #Tabelle-175 (&94498820425680)
[Tabelle-176]:           #Tabelle-176 (&94498820472560)
[Tabelle-177]:           #Tabelle-177 (&94498820491784)
[Tabelle-178]:           #Tabelle-178 (&94498820600200)
[Tabelle-179]:           #Tabelle-179 (&94498820654952)
[Tabelle-180]:           #Tabelle-180 (&94498820688920)
[Tabelle-181]:           #Tabelle-181 (&94498820868784)
[Tabelle-182]:           #Tabelle-182 (&94498820904736)
[Tabelle-183]:           #Tabelle-183 (&94498820988472)
[Tabelle-184]:           #Tabelle-184 (&94498821055056)
[Tabelle-185]:           #Tabelle-185 (&94498821086496)
[Tabelle-186]:           #Tabelle-186 (&94498821181360)
[Tabelle-187]:           #Tabelle-187 (&94498821231616)
[Tabelle-188]:           #Tabelle-188 (&94498821379320)
[Tabelle-189]:           #Tabelle-189 (&94498821472560)
[Tbl-193]:               #Tbl-193 (&94498821504200)
[Tabelle-191]:           #Tabelle-191 (&94498821600248)
[Tabelle-192]:           #Tabelle-192 (&94498821618808)
[Tabelle-193]:           #Tabelle-193 (&94498821817808)
[Tabelle-194]:           #Tabelle-194 (&94498822563944)
[Tabelle-195]:           #Tabelle-195 (&94498822581696)
[Tabelle-196]:           #Tabelle-196 (&94498822644416)
[Tabelle-197]:           #Tabelle-197 (&94498822657840)
[Tabelle-198]:           #Tabelle-198 (&94498822765544)
[Tabelle-199]:           #Tabelle-199 (&94498822784800)
[Tabelle-200]:           #Tabelle-200 (&94498822842832)
[Tabelle-201]:           #Tabelle-201 (&94498822857520)
[Tabelle-202]:           #Tabelle-202 (&94498822928728)
[Tabelle-203]:           #Tabelle-203 (&94498823484328)
[Tabelle-204]:           #Tabelle-204 (&94498823538968)
[Tabelle-205]:           #Tabelle-205 (&94498823558960)
[Tabelle-206]:           #Tabelle-206 (&94498823642536)
[Tabelle-207]:           #Tabelle-207 (&94498823671784)
[Tabelle-208]:           #Tabelle-208 (&94498823790712)
[Tabelle-209]:           #Tabelle-209 (&94498823821056)
[Tabelle-210]:           #Tabelle-210 (&94498823894032)
[Tabelle-211]:           #Tabelle-211 (&94498823925912)
[Tabelle-212]:           #Tabelle-212 (&94498824454584)
[Tabelle-213]:           #Tabelle-213 (&94498824497856)
[Tabelle-214]:           #Tabelle-214 (&94498824552256)
[Tabelle-215]:           #Tabelle-215 (&94498824586560)
[Tabelle-216]:           #Tabelle-216 (&94498824693760)
[Tabelle-217]:           #Tabelle-217 (&94498824713328)
[Tabelle-218]:           #Tabelle-218 (&94498824813608)
[Tabelle-219]:           #Tabelle-219 (&94498825506496)
[Tabelle-220]:           #Tabelle-220 (&94498825566264)
[Tabelle-221]:           #Tabelle-221 (&94498825687424)
[Tabelle-222]:           #Tabelle-222 (&94498825783984)
[Tabelle-223]:           #Tabelle-223 (&94498825842992)
[Tabelle-224]:           #Tabelle-224 (&94498825946808)
[Tabelle-225]:           #Tabelle-225 (&94498826050040)
[Tabelle-226]:           #Tabelle-226 (&94498826114336)
[Tabelle-227]:           #Tabelle-227 (&94498826160144)
[Tabelle-228]:           #Tabelle-228 (&94498826235696)
[Tabelle-229]:           #Tabelle-229 (&94498826319552)
[Tabelle-230]:           #Tabelle-230 (&94498826383256)
[Tabelle-231]:           #Tabelle-231 (&94498826399384)
[Tabelle-232]:           #Tabelle-232 (&94498826449184)
[Tabelle-233]:           #Tabelle-233 (&94498826802816)
[Tabelle-234]:           #Tabelle-234 (&94498826845168)
[Tabelle-235]:           #Tabelle-235 (&94498826943616)
[Tabelle-236]:           #Tabelle-236 (&94498827172464)
[Tabelle-237]:           #Tabelle-237 (&94498827263736)
[Tabelle-238]:           #Tabelle-238 (&94498827296552)
[Tabelle-239]:           #Tabelle-239 (&94498827330984)
[Tabelle-240]:           #Tabelle-240 (&94498827346200)
[Tabelle-241]:           #Tabelle-241 (&94498827370248)
[Tabelle-242]:           #Tabelle-242 (&94498827454072)
[Tabelle-243]:           #Tabelle-243 (&94498827471160)
[Tabelle-244]:           #Tabelle-244 (&94498827491336)
[Tabelle-245]:           #Tabelle-245 (&94498827531208)
[Tabelle-246]:           #Tabelle-246 (&94498827563664)
[Tabelle-247]:           #Tabelle-247 (&94498827593152)
[Tabelle-248]:           #Tabelle-248 (&94498827680640)
[Tabelle-249]:           #Tabelle-249 (&94498827698712)
[Tabelle-250]:           #Tabelle-250 (&94498827718696)
[Tabelle-251]:           #Tabelle-251 (&94498827780128)
[Tabelle-252]:           #Tabelle-252 (&94498827810920)
[Tabelle-253]:           #Tabelle-253 (&94498827877992)
[Tabelle-254]:           #Tabelle-254 (&94498827920704)
[Tabelle-255]:           #Tabelle-255 (&94498827978656)
[Tabelle-256]:           #Tabelle-256 (&94498828081456)
[Tbl-260]:               #Tbl-260 (&94498828153112)
[Tabelle-258]:           #Tabelle-258 (&94498828203792)
[Tabelle-259]:           #Tabelle-259 (&94498828225856)
[Tabelle-260]:           #Tabelle-260 (&94498828303896)
[Tabelle-261]:           #Tabelle-261 (&94498828358152)
[Tabelle-262]:           #Tabelle-262 (&94498828469512)
[Tabelle-263]:           #Tabelle-263 (&94498828494272)
[Tabelle-264]:           #Tabelle-264 (&94498828891176)
[Tabelle-265]:           #Tabelle-265 (&94498828909184)
[Tabelle-266]:           #Tabelle-266 (&94498829009968)
[Tabelle-267]:           #Tabelle-267 (&94498829089832)
[Tabelle-268]:           #Tabelle-268 (&94498829202632)
[Tabelle-269]:           #Tabelle-269 (&94498829225976)
[Tabelle-270]:           #Tabelle-270 (&94498829343016)
[Tabelle-271]:           #Tabelle-271 (&94498829365840)
[Tabelle-272]:           #Tabelle-272 (&94498829446288)
[Tabelle-273]:           #Tabelle-273 (&94498829482176)
[Tabelle-274]:           #Tabelle-274 (&94498829522432)
[Tabelle-275]:           #Tabelle-275 (&94498829614976)
[Tabelle-276]:           #Tabelle-276 (&94498829657664)
[Tabelle-277]:           #Tabelle-277 (&94498829687128)
[Tabelle-278]:           #Tabelle-278 (&94498829868672)
[Tabelle-279]:           #Tabelle-279 (&94498829910360)
[Tbl-283]:               #Tbl-283 (&94498829946968)
[Tbl-284]:               #Tbl-284 (&94498830052512)
[Tbl-285]:               #Tbl-285 (&94498830125168)
[Tabelle-283]:           #Tabelle-283 (&94498830144168)
[Tabelle-284]:           #Tabelle-284 (&94498830250576)
[Tabelle-285]:           #Tabelle-285 (&94498830263704)
[Tabelle-286]:           #Tabelle-286 (&94498830323328)
[Tabelle-287]:           #Tabelle-287 (&94498830394488)
[Tabelle-288]:           #Tabelle-288 (&94498830516328)
[Tabelle-289]:           #Tabelle-289 (&94498830606024)
[Tabelle-290]:           #Tabelle-290 (&94498831080856)
[Tabelle-291]:           #Tabelle-291 (&94498831129728)
[Tabelle-292]:           #Tabelle-292 (&94498831189600)
[Tabelle-293]:           #Tabelle-293 (&94498831240296)
[Tabelle-294]:           #Tabelle-294 (&94498831361936)
[Tabelle-295]:           #Tabelle-295 (&94498831389984)
[Tabelle-296]:           #Tabelle-296 (&94498831437336)
[Tabelle-297]:           #Tabelle-297 (&94498831474264)
[Tabelle-298]:           #Tabelle-298 (&94498831518912)
[Tabelle-299]:           #Tabelle-299 (&94498831569264)
[Tabelle-300]:           #Tabelle-300 (&94498831671528)
[Tabelle-301]:           #Tabelle-301 (&94498831735448)
[Tabelle-302]:           #Tabelle-302 (&94498831765224)
[Tabelle-303]:           #Tabelle-303 (&94498831798832)
[Tabelle-304]:           #Tabelle-304 (&94498831965592)
[Tabelle-305]:           #Tabelle-305 (&94498831999432)
[Tabelle-306]:           #Tabelle-306 (&94498832020816)
[Tabelle-307]:           #Tabelle-307 (&94498832146752)
[Tabelle-308]:           #Tabelle-308 (&94498832199016)
[Tabelle-309]:           #Tabelle-309 (&94498832211280)
[Tabelle-310]:           #Tabelle-310 (&94498832697336)
[Tabelle-311]:           #Tabelle-311 (&94498832755400)
[Tabelle-312]:           #Tabelle-312 (&94498832779808)
[Tabelle-313]:           #Tabelle-313 (&94498832876928)
[Tabelle-314]:           #Tabelle-314 (&94498832901336)
[Tabelle-315]:           #Tabelle-315 (&94498832998032)
[Tabelle-316]:           #Tabelle-316 (&94498833037424)
[Tabelle-317]:           #Tabelle-317 (&94498833067712)
[Tabelle-318]:           #Tabelle-318 (&94498833090920)
[Tabelle-319]:           #Tabelle-319 (&94498833173752)
[Tabelle-320]:           #Tabelle-320 (&94498833194376)
[Tabelle-321]:           #Tabelle-321 (&94498833310232)
[Tabelle-322]:           #Tabelle-322 (&94498833337480)
[Tbl-326]:               #Tbl-326 (&94498833416128)
[Tabelle-324]:           #Tabelle-324 (&94498833480608)
[Tabelle-325]:           #Tabelle-325 (&94498833838192)
[Tabelle-326]:           #Tabelle-326 (&94498833920736)
[Tabelle-327]:           #Tabelle-327 (&94498833966616)
[Tabelle-328]:           #Tabelle-328 (&94498834002920)
[Tabelle-329]:           #Tabelle-329 (&94498834107072)
[Tabelle-330]:           #Tabelle-330 (&94498834134568)
[Tabelle-331]:           #Tabelle-331 (&94498834200056)
[Tabelle-332]:           #Tabelle-332 (&94498834263416)
[Tabelle-333]:           #Tabelle-333 (&94498834299744)
[Tabelle-334]:           #Tabelle-334 (&94498834410616)
[Tabelle-335]:           #Tabelle-335 (&94498834455528)
[Tabelle-336]:           #Tabelle-336 (&94498834547504)
[Tabelle-337]:           #Tabelle-337 (&94498834575472)
[Tabelle-338]:           #Tabelle-338 (&94498834669152)
[Tabelle-339]:           #Tabelle-339 (&94498834687400)
[Tabelle-340]:           #Tabelle-340 (&94498834721288)
[Tabelle-341]:           #Tabelle-341 (&94498834737784)
[Tabelle-342]:           #Tabelle-342 (&94498834757336)
[Tabelle-343]:           #Tabelle-343 (&94498834815832)
[Tabelle-344]:           #Tabelle-344 (&94498834844808)
[Tabelle-345]:           #Tabelle-345 (&94498834951848)
[Tabelle-346]:           #Tabelle-346 (&94498834993008)
[Tabelle-347]:           #Tabelle-347 (&94498835016048)
[Tabelle-348]:           #Tabelle-348 (&94498835063088)
[Tabelle-349]:           #Tabelle-349 (&94498835087632)
[Tabelle-350]:           #Tabelle-350 (&94498835131968)
[Tabelle-351]:           #Tabelle-351 (&94498835206648)
[Tabelle-352]:           #Tabelle-352 (&94498835257160)
[Tabelle-353]:           #Tabelle-353 (&94498835283136)
[Tabelle-354]:           #Tabelle-354 (&94498835315488)
[Tabelle-355]:           #Tabelle-355 (&94498835353536)
[Tabelle-356]:           #Tabelle-356 (&94498835441024)
[Tabelle-357]:           #Tabelle-357 (&94498835550664)
[Tabelle-358]:           #Tabelle-358 (&94498835575016)
[Tabelle-359]:           #Tabelle-359 (&94498835590136)
[Tabelle-360]:           #Tabelle-360 (&94498835729424)
[Tabelle-361]:           #Tabelle-361 (&94498835763936)
[Tbl-365]:               #Tbl-365 (&94498835797016)
[Tbl-366]:               #Tbl-366 (&94498835822600)
[Tbl-367]:               #Tbl-367 (&94498835838984)
[Tbl-368]:               #Tbl-368 (&94498835852016)
[Tabelle -366]:          #Tabelle -366 (&94498835924912)
[Tbl-370]:               #Tbl-370 (&94498836026208)
[Tabelle-368]:           #Tabelle-368 (&94498836077232)
[Tbl-372]:               #Tbl-372 (&94498836127592)
[Tabelle-370]:           #Tabelle-370 (&94498836201016)
[Tabelle-371]:           #Tabelle-371 (&94498836343256)
[Tabelle-372]:           #Tabelle-372 (&94498836385424)
[Tabelle-373]:           #Tabelle-373 (&94498836577272)
[Tabelle-374]:           #Tabelle-374 (&94498836602160)
[Tabelle-375]:           #Tabelle-375 (&94498836669048)
[Tabelle-376]:           #Tabelle-376 (&94498836699248)
[Tabelle-377]:           #Tabelle-377 (&94498836829904)
[Tabelle-378]:           #Tabelle-378 (&94498836851104)
[Tabelle-379]:           #Tabelle-379 (&94498836924752)
[Tabelle-380]:           #Tabelle-380 (&94498836955000)
[Tabelle-381]:           #Tabelle-381 (&94498837067448)
[Tabelle-382]:           #Tabelle-382 (&94498837109096)
[Tabelle-383]:           #Tabelle-383 (&94498837156600)
[Tabelle-384]:           #Tabelle-384 (&94498837169424)
[Tabelle-385]:           #Tabelle-385 (&94498837201760)
[Tabelle-386]:           #Tabelle-386 (&94498837407872)
[Tabelle-387]:           #Tabelle-387 (&94498837422872)
[Tabelle-388]:           #Tabelle-388 (&94498837437480)
[Tbl-392]:               #Tbl-392 (&94498837450200)
[Tbl-393]:               #Tbl-393 (&94498837652176)
[Tbl-394]:               #Tbl-394 (&94498838380096)
[Tbl-395]:               #Tbl-395 (&94498838459984)
[Tabelle-389]:           #Tabelle-389 (&94498838908872)
[Tabelle-390]:           #Tabelle-390 (&94498839115760)
[Tabelle-391]:           #Tabelle-391 (&94498839129824)
[Tabelle-392]:           #Tabelle-392 (&94498839142112)
[Tabelle-393]:           #Tabelle-393 (&94498841085640)
[Tabelle-394]:           #Tabelle-394 (&94498841901232)
[Tabelle-395]:           #Tabelle-395 (&94498842133616)
[Tabelle-396]:           #Tabelle-396 (&94498842157080)
[Tabelle-397]:           #Tabelle-397 (&94498846324216)
