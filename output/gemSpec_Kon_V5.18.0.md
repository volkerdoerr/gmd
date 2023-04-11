
Elektronische Gesundheitskarte und Telematikinfrastruktur

### Spezifikation<br>Konnektor

Klassifizierung: öffentlich  
Referenzierung: gemSpec_Kon  
Revision: 571788  
Stand: 28.11.2022  
Status: freigegeben  
Version: 5.18.0

### Dokumentinformationen

--> P

--> P

--> P

--> P

--> TABLE

--> P

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

--> P

--> P

--> P

### 1.2 Zielgruppe

--> P

### 1.3 Geltungsbereich

--> P

--> P

--> P

### 1.4 Abgrenzung des Dokuments

--> P

--> P

### 1.5 Methodik

### 1.5.1 Anforderungen

--> P

--> P

--> P

--> P

--> P

### 1.5.2 Offene Punkte

--> P

--> TABLE

### 1.5.3 Erläuterungen zur Spezifikation des Außenverhaltens

--> P

--> P

--> P

--> P

### 1.5.4 Erläuterungen zur Dokumentenstruktur und „Dokumentenmechanismen“

### 1.5.4.1 Modulare Spezifikation über Funktionsmerkmale

--> P

--> P

--> P

--> OL

--> P

--> P

--> P

### 1.5.4.2 Technische Use Cases - TUCs

--> P

--> P

--> UL

--> P

--> P

--> UL

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> TABLE

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

### 1.5.4.3 Event-Mechanismus

--> P

--> P

### 1.5.4.4 Konfigurationsparameter und Zustandswerte

--> P

--> P

--> P

### 2 Systemüberblick

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

### 2.1 Logische Struktur

--> P

--> P

--> UL

--> P

--> P

--> P

--> P

### 2.2 Sicherer Datenspeicher

--> P

--> UL

--> P

--> P

### 2.3 Überblick Konnektoridentität

--> P

--> UL

--> P

--> P

### 2.4 Mandantenfähigkeit

--> P

--> P

--> UL

### 2.5 Versionierung

--> P

--> P

--> UL

### 2.6 Fachanwendungen

--> P

--> P

--> P

--> P

### 2.7 Netzseitige Einsatzszenarien

--> P

--> P

### 2.7.1 Parameter ANLW_ANBINDUNGS_MODUS

--> P

--> P

--> P

--> P

--> UL

--> P

### 2.7.2 Parameter ANLW_INTERNET_MODUS

--> P

--> P

### 2.8 Lokale und entfernte Kartenterminals

--> P

--> P

### 2.9 Standalone-Szenario

--> P

--> P

--> P

### 3 Übergreifende Festlegungen

--> P

--> P

--> P

### 3.1 Allgemeine übergreifende Festlegungen

### 3.1.1 Dokumentformate

--> P

--> UL

--> P

--> P

--> P

--> P

--> P

--> DIV

--> P

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

### 3.1.2 Kartentypen

--> P

--> P

--> TABLE

--> P

### 3.1.3 Übergreifende Festlegungen zum Aufbau von sicheren Verbindungen

--> DIV

--> P

--> DIV

--> DIV

--> P

### 3.2 Konnektoridentität und gSMC-K

--> DIV

--> P

--> DIV

--> DIV

--> DIV

--> P

--> DIV

--> DIV

### 3.2.1 Organisatorische Anforderungen und Sperrprozesse

--> DIV

--> DIV

--> DIV

--> P

--> DIV

--> P

--> DIV

--> P

--> DIV

--> P

--> DIV

--> P

--> DIV

--> DIV

--> DIV

--> DIV

--> P

--> DIV

--> P

--> P

--> DIV

--> DIV

### 3.3 Bootup-Phase

--> DIV

--> DIV

--> P

### 3.4 Betriebszustand

--> DIV

--> DIV

--> P

--> P

--> DIV

--> P

--> P

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> P

--> P

--> TABLE

--> P

--> P

--> P

--> DIV

--> P

--> P

--> DIV

--> P

--> DIV

### 3.4.1 Betriebsaspekte

--> P

--> DIV

### 3.5 Fachliche Anbindung der Clientsysteme

--> P

--> UL

--> P

--> UL

--> P

--> P

--> DIV

--> DIV

--> DIV

--> P

--> OL

--> P

--> DIV

--> P

--> P

--> TABLE

--> P

--> P

--> P

--> DIV

--> P

--> P

### 3.5.1 Betriebsaspekte

--> P

--> P

--> DIV

--> DIV

--> P

--> UL

--> P

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

### 3.6 Clientsystemschnittstelle

--> DIV

### 3.6.1 SOAP-Schnittstelle

--> P

--> DIV

--> DIV

--> DIV

--> DIV

--> P

--> P

--> P

--> DIV

--> DIV

--> DIV

--> P

### 3.6.2 Statusrückmeldung und Fehlerbehandlung

--> P

--> DIV

--> DIV

--> P

--> P

--> P

--> P

--> P

--> DIV

--> DIV

--> P

--> P

--> P

### 3.6.3 Transport großer Dokumente

--> P

--> P

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

### 3.7 Verwendung manuell importierter CA-Zertifikate

--> P

--> P

--> DIV

--> P

--> P

--> P

--> P

--> DIV

### 3.8 Testunterstützung

--> P

--> DIV

--> DIV

--> DIV

### 4 Funktionsmerkmale

--> P

### 4.1 Anwendungskonnektor

### 4.1.1 Zugriffsberechtigungsdienst

--> P

--> P

--> P

--> P

--> P

### 4.1.1.1 Funktionsmerkmalweite Aspekte

--> DIV

--> P

--> P

--> P

--> P

--> P

--> TABLE

--> P

--> P

--> TABLE

--> P

--> P

--> TABLE

--> P

--> P

--> TABLE

--> P

--> DIV

### 4.1.1.2 Durch Ereignisse ausgelöste Reaktionen

--> P

### 4.1.1.3 Interne TUCs, nicht durch Fachmodule nutzbar

--> P

### 4.1.1.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.1.1.4.1 TUC_KON_000 „Prüfe Zugriffsberechtigung“

--> P

--> P

--> P

--> P

--> P

--> DIV

--> P

--> P

--> P

--> TABLE

--> P

--> P

--> P

--> UL

--> P

--> P

--> TABLE

--> P

--> P

--> P

--> UL

--> P

--> P

--> TABLE

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> TABLE

--> P

### 4.1.1.5 Operationen an der Außenschnittstelle

--> P

### 4.1.1.6 Betriebsaspekte

--> DIV

--> P

--> DIV

--> P

### 4.1.2 Dokumentvalidierungsdienst

--> P

--> P

### 4.1.2.1 Funktionsmerkmalweite Aspekte

--> DIV

### 4.1.2.2 Durch Ereignisse ausgelöste Reaktionen

--> P

### 4.1.2.3 Interne TUCs, nicht durch Fachmodule nutzbar

--> P

### 4.1.2.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.1.2.4.1 TUC_KON_080 „Dokument validieren”

--> DIV

### 4.1.2.5 Operationen an der Außenschnittstelle

--> P

### 4.1.2.6 Betriebsaspekte

--> P

### 4.1.3 Dienstverzeichnisdienst

--> P

### 4.1.3.1 Funktionsmerkmalweite Aspekte

--> P

--> P

--> P

--> P

--> P

--> DIV

--> DIV

--> DIV

### 4.1.3.2 Durch Ereignisse ausgelöste Reaktionen

--> P

### 4.1.3.3 Interne TUCs, nicht durch Fachmodule nutzbar

--> P

### 4.1.3.4 Interne TUCs, auch durch Fachmodule nutzbar

--> P

### 4.1.3.4.1 TUC_KON_041 „Einbringen der Endpunktinformationen während der Bootup-Phase“

--> DIV

### 4.1.3.5 Operationen an der Außenschnittstelle

--> DIV

### 4.1.3.6 Betriebsaspekte

--> DIV

### 4.1.4 Kartenterminaldienst

--> P

--> P

--> P

--> UL

--> P

--> P

--> P

--> TABLE

--> P

--> P

--> P

--> P

### 4.1.4.1 Funktionsmerkmalweite Aspekte

--> DIV

--> P

--> DIV

--> DIV

--> DIV

--> P

--> P

--> P

--> DIV

--> DIV

--> DIV

--> DIV

--> P

--> TABLE

--> DIV

--> DIV

### 4.1.4.2 Durch Ereignisse ausgelöste Reaktionen

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

### 4.1.4.3 Interne TUCs, nicht durch Fachmodule nutzbar

### 4.1.4.3.1 TUC_KON_050 „Beginne Kartenterminalsitzung“

--> DIV

--> P

### 4.1.4.3.2 TUC_KON_054 „Kartenterminal hinzufügen“

--> DIV

### 4.1.4.3.3 TUC_KON_053 „Paire Kartenterminal“

--> DIV

--> P

### 4.1.4.3.4 TUC_KON_055 „Befülle CT-Object“

--> DIV

### 4.1.4.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.1.4.4.1 TUC_KON_051 „Mit Anwender über Kartenterminal interagieren“

--> DIV

### 4.1.4.4.2 TUC_KON_056 „Karte anfordern“

--> DIV

### 4.1.4.4.3 TUC_KON_057 „Karte auswerfen“

--> DIV

### 4.1.4.4.4 TUC_KON_058 „Displaygröße ermitteln“

--> DIV

### 4.1.4.5 Operationen an der Außenschnittstelle

--> DIV

### 4.1.4.5.1 RequestCard

--> DIV

### 4.1.4.5.2 EjectCard

--> DIV

### 4.1.4.6 Betriebsaspekte

### 4.1.4.6.1 Allgemeine Betriebsaspekte

--> DIV

--> P

--> DIV

--> DIV

### 4.1.4.6.2 Kartenterminals pflegen

--> P

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> P

--> DIV

--> DIV

--> DIV

### 4.1.4.6.3 Import der Kartenterminal-Informationen

--> P

--> DIV

### 4.1.5 Kartendienst

--> P

--> UL

--> P

--> P

--> P

--> P

--> P

--> TABLE

### 4.1.5.1 Funktionsmerkmalweite Aspekte

--> DIV

--> P

--> DIV

--> DIV

--> DIV

--> DIV

--> P

--> DIV

--> P

--> UL

--> P

--> DIV

--> P

### 4.1.5.2 Durch Ereignisse ausgelöste Reaktionen

--> DIV

--> DIV

### 4.1.5.3 Interne TUCs, nicht durch Fachmodule nutzbar

### 4.1.5.3.1 TUC_KON_001 „Karte öffnen“

--> DIV

### 4.1.5.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.1.5.4.1 TUC_KON_026 „Liefere CardSession“

--> DIV

--> P

### 4.1.5.4.2 TUC_KON_012 „PIN verifizieren“

--> DIV

### 4.1.5.4.3 TUC_KON_019 „PIN ändern“

--> DIV

### 4.1.5.4.4 TUC_KON_021 „PIN entsperren“

--> DIV

--> P

### 4.1.5.4.5 TUC_KON_022 „Liefere PIN-Status“

--> DIV

### 4.1.5.4.6 TUC_KON_027 „PIN-Schutz ein-/ausschalten“

--> DIV

### 4.1.5.4.7 TUC_KON_023 „Karte reservieren“

--> DIV

### 4.1.5.4.8 TUC_KON_005 „Card-to-Card authentisieren“

--> P

--> P

--> P

--> P

--> P

--> P

--> DIV

### 4.1.5.4.9 TUC_KON_202 „LeseDatei“

--> DIV

### 4.1.5.4.10 TUC_KON_203 „SchreibeDatei“

--> DIV

### 4.1.5.4.11 TUC_KON_204 „LöscheDateiInhalt“

--> DIV

### 4.1.5.4.12 TUC_KON_209 „LeseRecord“

--> DIV

### 4.1.5.4.13 TUC_KON_210 „SchreibeRecord“

--> DIV

### 4.1.5.4.14 TUC_KON_211 „LöscheRecordInhalt“

--> DIV

### 4.1.5.4.15 TUC_KON_214 „FügeHinzuRecord“

--> DIV

### 4.1.5.4.16 TUC_KON_215 „SucheRecord“

--> DIV

### 4.1.5.4.17 TUC_KON_018 „eGK-Sperrung prüfen“

--> DIV

### 4.1.5.4.18 TUC_KON_006 „Datenzugriffsaudit eGK schreiben“

--> DIV

### 4.1.5.4.19 TUC_KON_218 „Signiere“

--> DIV

### 4.1.5.4.20 TUC_KON_219 „Entschlüssele“

--> DIV

### 4.1.5.4.21 TUC_KON_200 „SendeAPDU“

--> DIV

### 4.1.5.4.22 TUC_KON_024 „Karte zurücksetzen“

--> DIV

### 4.1.5.4.23 TUC_KON_216 „LeseZertifikat“

--> DIV

### 4.1.5.4.24 TUC_KON_036 „LiefereFachlicheRolle“

--> DIV

### 4.1.5.5 Operationen an der Außenschnittstelle

--> DIV

### 4.1.5.5.1 VerifyPin

--> DIV

### 4.1.5.5.2 ChangePin

--> DIV

### 4.1.5.5.3 GetPinStatus

--> DIV

### 4.1.5.5.4 UnblockPin

--> DIV

### 4.1.5.5.5 EnablePin

--> DIV

### 4.1.5.5.6 DisablePin

--> DIV

### 4.1.5.6 Betriebsaspekte

--> DIV

### 4.1.5.6.1 TUC_KON_025 "Initialisierung Kartendienst"

--> DIV

### 4.1.5.6.2 Kartenübersicht und PIN-Management

--> DIV

--> DIV

--> P

### 4.1.6 Systeminformationsdienst

--> P

--> P

--> UL

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> UL

### 4.1.6.1 Funktionsmerkmalweite Aspekte

--> DIV

--> DIV

--> DIV

--> P

--> DIV

### 4.1.6.2 Durch Ereignisse ausgelöste Reaktionen

--> P

### 4.1.6.3 Interne TUCs, nicht durch Fachmodule nutzbar

--> P

### 4.1.6.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.1.6.4.1 TUC_KON_256 „Systemereignis absetzen“

--> DIV

### 4.1.6.4.2 TUC_KON_252 „Liefere KT_Liste“

--> DIV

### 4.1.6.4.3 TUC_KON_253 „Liefere Karten_Liste“

--> DIV

### 4.1.6.4.4 TUC_KON_254 „Liefere Ressourcendetails“

--> DIV

### 4.1.6.5 Operationen an der Außenschnittstelle

--> DIV

### 4.1.6.5.1 GetCardTerminals

--> DIV

### 4.1.6.5.2 GetCards

--> DIV

### 4.1.6.5.3 GetResourceInformation

--> DIV

### 4.1.6.5.4 Subscribe

--> DIV

### 4.1.6.5.5 Unsubscribe

--> DIV

### 4.1.6.5.6 RenewSubscriptions

--> DIV

### 4.1.6.5.7 GetSubscription

--> DIV

--> P

### 4.1.6.6 Betriebsaspekte

--> DIV

--> DIV

--> DIV

### 4.1.7 Verschlüsselungsdienst

--> P

--> P

--> P

--> UL

--> P

--> UL

--> P

--> P

### 4.1.7.1 Funktionsmerkmalweite Aspekte

--> DIV

--> DIV

--> P

--> DIV

--> P

--> P

--> TABLE

--> P

--> P

--> TABLE

### 4.1.7.2 Durch Ereignisse ausgelöste Reaktionen

--> P

### 4.1.7.3 Interne TUCs, nicht durch Fachmodule nutzbar

--> P

### 4.1.7.4 Interne TUCs, auch durch Fachmodule nutzbar

--> P

### 4.1.7.4.1 TUC_KON_070 „Daten hybrid verschlüsseln”

--> DIV

### 4.1.7.4.2 TUC_KON_071 „Daten hybrid entschlüsseln”

--> DIV

### 4.1.7.4.3 TUC_KON_072 „Daten symmetrisch verschlüsseln”

--> DIV

### 4.1.7.4.4 TUC_KON_073 „Daten symmetrisch entschlüsseln”

--> DIV

### 4.1.7.4.5 TUC_KON_075 „Symmetrisch verschlüsseln“

--> DIV

### 4.1.7.4.6 TUC_KON_076 „Symmetrisch entschlüsseln“

--> DIV

--> P

### 4.1.7.5 Operationen an der Außenschnittstelle

--> DIV

### 4.1.7.5.1 EncryptDocument

--> DIV

### 4.1.7.5.2 DecryptDocument

--> DIV

--> P

### 4.1.7.6 Betriebsaspekte

--> P

### 4.1.8 Signaturdienst

--> P

--> P

--> UL

### 4.1.8.1 Funktionsmerkmalweite Aspekte

### 4.1.8.1.1 Dokumentensignatur

--> P

--> P

--> DIV

--> DIV

--> P

--> TABLE

--> P

--> DIV

--> DIV

--> P

--> DIV

--> P

--> DIV

--> DIV

--> DIV

--> P

--> P

--> TABLE

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> P

--> P

--> TABLE

--> P

--> P

--> TABLE

--> P

### 4.1.8.1.2 Signaturrichtlinien

--> P

--> UL

--> DIV

### 4.1.8.1.3 Signaturzeitpunkt

--> P

--> P

--> OL

--> P

--> P

### 4.1.8.1.4 Jobnummer

--> P

--> P

--> P

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> P

--> P

### 4.1.8.1.5 Komfortsignatur

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> DIV

--> DIV

--> P

--> P

--> P

--> DIV

--> DIV

--> P

--> DIV

--> DIV

--> P

--> DIV

--> DIV

--> DIV

--> P

--> DIV

--> P

--> P

--> P

--> P

--> DIV

--> DIV

--> P

### 4.1.8.2 Durch Ereignisse ausgelöste Reaktionen

--> P

### 4.1.8.3 Interne TUCs, nicht durch Fachmodule nutzbar

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

### 4.1.8.3.1 TUC_KON_155 „Dokumente zur Signatur vorbereiten”

--> DIV

### 4.1.8.3.2 TUC_KON_165 „Signaturvoraussetzungen für nonQES prüfen“

--> DIV

### 4.1.8.3.3 TUC_KON_166 „nonQES Signaturen erstellen“

--> DIV

### 4.1.8.3.4 TUC_KON_152 "Signaturvoraussetzungen für QES prüfen"

--> DIV

### 4.1.8.3.5 TUC_KON_154 "QES Signaturen erstellen"

--> P

--> DIV

--> P

--> P

### 4.1.8.3.6 TUC_KON_168 „Einzelsignatur QES erstellen“

--> DIV

### 4.1.8.3.7 TUC_KON_158 "Komfortsignaturen erstellen"

--> P

--> DIV

### 4.1.8.4 Interne TUCs, auch durch Fachmodule nutzbar

--> DIV

--> P

### 4.1.8.4.1 TUC_KON_160 „Dokumente nonQES signieren”

--> DIV

--> DIV

--> P

### 4.1.8.4.2 TUC_KON_161 „nonQES Dokumentsignatur prüfen”

--> DIV

--> P

--> DIV

### 4.1.8.4.3 TUC_KON_162 „Kryptographische Prüfung der XML-Dokumentensignatur”

--> DIV

### 4.1.8.4.4 TUC_KON_150 „Dokumente QES signieren”

--> DIV

--> P

--> P

### 4.1.8.4.5 Anforderungen an die Stapelsignatur

--> P

--> DIV

--> DIV

--> DIV

--> DIV

### 4.1.8.4.6 TUC_KON_151 „QES Dokumentensignatur prüfen“

--> DIV

--> P

--> DIV

### 4.1.8.4.7 TUC_KON_170 „Dokumente mit Komfort signieren”

--> DIV

### 4.1.8.4.8 TUC_KON_171 „Komfortsignatur einschalten”

--> DIV

### 4.1.8.4.9 TUC_KON_172 „Komfortsignatur ausschalten”

--> DIV

--> P

### 4.1.8.4.10 TUC_KON_173 „Liefere Signaturmodus”

--> DIV

### 4.1.8.5 Operationen an der Außenschnittstelle

--> DIV

--> P

### 4.1.8.5.1 SignDocument (nonQES und QES)

--> DIV

### 4.1.8.5.2 VerifyDocument (nonQES und QES)

--> DIV

### 4.1.8.5.3 StopSignature

--> DIV

### 4.1.8.5.4 GetJobNumber

--> DIV

### 4.1.8.5.5 ActivateComfortSignature

--> DIV

--> P

### 4.1.8.5.6 DeactivateComfortSignature

--> DIV

--> P

### 4.1.8.5.7 GetSignatureMode

--> DIV

### 4.1.8.6 Betriebsaspekte

--> DIV

--> P

### 4.1.9 Zertifikatsdienst

--> P

--> P

--> P

--> P

--> UL

### 4.1.9.1 Funktionsmerkmalweite Aspekte

--> P

--> DIV

--> P

--> P

--> P

--> TABLE

--> P

--> DIV

--> DIV

--> DIV

--> P

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

### 4.1.9.2 Durch Ereignisse ausgelöste Reaktionen

--> P

### 4.1.9.3 Interne TUCs, nicht durch Fachmodule nutzbar

### 4.1.9.3.1 TUC_KON_032 „TSL aktualisieren“

--> DIV

--> P

--> DIV

--> P

--> P

--> DIV

### 4.1.9.3.2 TUC_KON_031 „BNetzA-VL aktualisieren“

--> DIV

### 4.1.9.3.3 TUC_KON_040 „CRL aktualisieren“

--> DIV

### 4.1.9.3.4 TUC_KON_033 „Zertifikatsablauf prüfen“

--> DIV

### 4.1.9.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.1.9.4.1 TUC_KON_037 „Zertifikat prüfen"

--> DIV

### 4.1.9.4.2 TUC_KON_042 „CV-Zertifikat prüfen“

--> DIV

### 4.1.9.4.3 TUC_KON_034 „Zertifikatsinformationen extrahieren“

--> DIV

### 4.1.9.5 Operationen an der Außenschnittstelle

--> DIV

### 4.1.9.5.1 CheckCertificateExpiration

--> DIV

### 4.1.9.5.2 ReadCardCertificate

--> DIV

### 4.1.9.5.3 VerifyCertificate

--> DIV

### 4.1.9.6 Betriebsaspekte

### 4.1.9.6.1 TUC_KON_035 „Zertifikatsdienst initialisieren“

--> DIV

--> DIV

--> DIV

--> P

--> DIV

--> DIV

--> DIV

--> DIV

--> P

--> DIV

--> DIV

--> P

--> DIV

--> DIV

--> P

--> DIV

--> P

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

### 4.1.10 Protokollierungsdienst

--> P

--> P

--> P

--> P

--> UL

### 4.1.10.1 Funktionsmerkmalweite Aspekte

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> P

--> DIV

--> DIV

--> DIV

### 4.1.10.2 Durch Ereignisse ausgelöste Reaktionen

--> P

### 4.1.10.3 Interne TUCs, nicht durch Fachmodule nutzbar

--> P

### 4.1.10.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.1.10.4.1 TUC_KON_271 „Schreibe Protokolleintrag“

--> DIV

--> P

--> P

--> P

### 4.1.10.5 Operationen an der Außenschnittstelle

--> P

### 4.1.10.6 Betriebsaspekte

--> DIV

--> DIV

--> DIV

### 4.1.10.6.1 TUC_KON_272 „Initialisierung Protokollierungsdienst

--> DIV

### 4.1.11 TLS-Dienst

--> P

--> P

### 4.1.11.1 Funktionsmerkmalweite Aspekte

### 4.1.11.2 Durch Ereignisse ausgelöste Reaktionen

--> DIV

### 4.1.11.3 Interne TUCs, nicht durch Fachmodule nutzbar

--> P

### 4.1.11.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.1.11.4.1 TUC_KON_110 „Kartenbasierte TLS-Verbindung aufbauen“

--> DIV

### 4.1.11.4.2 TUC_KON_111 „Kartenbasierte TLS-Verbindung abbauen“

--> DIV

### 4.1.11.5 Operationen an der Außenschnittstelle

--> P

### 4.1.11.6 Betriebsaspekte

--> DIV

### 4.1.12 LDAP-Proxy

--> P

--> P

### 4.1.12.1 Funktionsmerkmalweite Aspekte

--> P

### 4.1.12.2 Durch Ereignisse ausgelöste Reaktionen

--> DIV

### 4.1.12.3 Interne TUCs, nicht durch Fachmodule nutzbar

--> P

### 4.1.12.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.1.12.4.1 TUC_KON_290 „LDAP-Verbindung aufbauen“

--> DIV

--> P

### 4.1.12.4.2 TUC_KON_291 „Verzeichnis abfragen“

--> DIV

### 4.1.12.4.3 TUC_KON_292 „LDAP-Verbindung trennen"

--> DIV

### 4.1.12.4.4 TUC_KON_293 „Verzeichnisabfrage abbrechen"

--> DIV

### 4.1.12.5 Operationen an der Außenschnittstelle

### 4.1.12.5.1 Unterstützte LDAPv3 Operationen

--> DIV

### 4.1.12.6 Betriebsaspekte

--> P

### 4.1.13 Authentifizierungsdienst

--> P

--> P

--> UL

--> P

### 4.1.13.1 Funktionsmerkmalweite Aspekte

### 4.1.13.1.1 Externe Authentisierung

--> DIV

--> DIV

--> P

### 4.1.13.2 Durch Ereignisse ausgelöste Reaktionen

--> P

### 4.1.13.3 Interne TUCs

--> P

### 4.1.13.4 Operationen an der Außenschnittstelle

--> DIV

### 4.1.13.4.1 ExternalAuthenticate

--> DIV

### 4.1.13.5 Betriebsaspekte

--> P

### 4.1.14 Betriebsdatenmeldedienst

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

### 4.2 Netzkonnektor

### 4.2.1 Anbindung LAN/WAN

--> P

--> P

--> UL

### 4.2.1.1 Funktionsmerkmalweite Aspekte

--> DIV

--> DIV

--> P

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

### 4.2.1.1.1 Netzwerksegmentierung

--> P

--> P

--> P

--> TABLE

--> P

--> P

--> TABLE

--> P

--> P

--> TABLE

### 4.2.1.1.2 Routing und Firewall

--> P

--> P

--> P

--> P

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> P

--> DIV

### 4.2.1.2 Durch Ereignisse ausgelöste Reaktionen

--> DIV

--> DIV

--> DIV

### 4.2.1.3 Interne TUCs, nicht durch Fachmodule nutzbar

### 4.2.1.3.1 TUC_KON_305 „LAN-Adapter initialisieren“

--> DIV

### 4.2.1.3.2 TUC_KON_306 „WAN-Adapter initialisieren“

--> DIV

### 4.2.1.3.3 TUC_KON_304 „Netzwerk-Routen einrichten“

--> DIV

### 4.2.1.4 Interne TUCs, auch durch Fachmodule nutzbar

--> P

### 4.2.1.5 Operationen an der Außenschnittstelle

--> P

### 4.2.1.6 Betriebsaspekte

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

### 4.2.2 DHCP-Server

--> P

--> UL

### 4.2.2.1 Funktionsmerkmalweite Aspekte

--> DIV

### 4.2.2.2 Durch Ereignisse ausgelöste Reaktionen

--> P

### 4.2.2.3 Interne TUCs, nicht durch Fachmodule nutzbar

--> P

### 4.2.2.4 Interne TUCs, auch durch Fachmodule nutzbar

--> P

### 4.2.2.5 Operationen an der Außenschnittstelle

### 4.2.2.5.1 Liefere Netzwerkinformationen über DHCP

--> DIV

### 4.2.2.6 Betriebsaspekte

--> DIV

--> DIV

### 4.2.2.6.1 TUC_KON_343 „Initialisierung DHCP-Server“

--> DIV

### 4.2.3 DHCP-Client

--> P

--> UL

### 4.2.3.1 Funktionsmerkmalweite Aspekte

--> DIV

### 4.2.3.2 Durch Ereignisse ausgelöste Reaktionen

--> DIV

### 4.2.3.3 Interne TUCs, nicht durch Fachmodule nutzbar

### 4.2.3.3.1 TUC_KON_341 „DHCP-Informationen beziehen“

--> DIV

### 4.2.3.4 Interne TUCs, auch durch Fachmodule nutzbar

--> P

### 4.2.3.5 Operationen an der Außenschnittstelle

--> P

### 4.2.3.6 Betriebsaspekte

--> DIV

--> DIV

--> DIV

### 4.2.4 VPN-Client

--> P

--> P

--> UL

### 4.2.4.1 Funktionsmerkmalweite Aspekte

--> DIV

--> DIV

### 4.2.4.2 Durch Ereignisse ausgelöste Reaktionen

--> DIV

--> DIV

--> DIV

--> DIV

--> P

### 4.2.4.3 Interne TUCs, nicht durch Fachmodule nutzbar

### 4.2.4.3.1 TUC_KON_321 „Verbindung zu dem VPN-Konzentrator der TI aufbauen“

--> DIV

### 4.2.4.3.2 TUC_KON_322 „Verbindung zu dem VPN-Konzentrator des SIS aufbauen“

--> DIV

### 4.2.4.4 Interne TUCs, auch durch Fachmodule nutzbar

--> P

### 4.2.4.5 Operationen an der Außenschnittstelle

--> P

### 4.2.4.6 Betriebsaspekte

--> DIV

--> DIV

--> P

### 4.2.5 Zeitdienst

--> P

--> P

--> UL

### 4.2.5.1 Funktionsmerkmalweite Aspekte

--> DIV

--> DIV

--> P

--> DIV

--> P

--> DIV

### 4.2.5.2 Durch Ereignisse ausgelöste Reaktionen

--> P

### 4.2.5.3 Interne TUCs, nicht durch Fachmodule nutzbar

--> P

### 4.2.5.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.2.5.4.1 TUC_KON_351 “Liefere Systemzeit”

--> DIV

### 4.2.5.5 Operationen an der Außenschnittstelle

### 4.2.5.5.1 Sync_Time

--> DIV

### 4.2.5.6 Betriebsaspekte

--> DIV

--> DIV

--> DIV

### 4.2.5.6.1 TUC_KON_352 Initialisierung Zeitdienst

--> DIV

### 4.2.6 Namensdienst und Dienstlokalisierung

--> P

--> UL

### 4.2.6.1 Funktionsmerkmalweite Aspekte

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> P

### 4.2.6.2 Durch Ereignisse ausgelöste Reaktionen

--> P

### 4.2.6.3 Interne TUCs, nicht durch Fachmodule nutzbar

--> P

### 4.2.6.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.2.6.4.1 TUC_KON_361 „DNS-Namen auflösen“

--> DIV

--> DIV

### 4.2.6.4.2 TUC_KON_362 „Liste der Dienste abrufen“

--> DIV

### 4.2.6.4.3 TUC_KON_363 „Dienstdetails abrufen“

--> DIV

### 4.2.6.5 Operationen an der Außenschnittstelle

--> DIV

### 4.2.6.5.1 GetIPAddress

--> DIV

### 4.2.6.6 Betriebsaspekte

--> DIV

--> DIV

### 4.2.7 Optionale Verwendung von IPv6

--> P

--> DIV

--> DIV

--> P

--> DIV

### 4.3 Konnektormanagement

--> P

--> P

--> UL

--> P

--> UL

--> DIV

--> P

--> UL

--> P

--> DIV

--> DIV

--> DIV

--> DIV

### 4.3.1 Zugang und Benutzerverwaltung des Konnektormanagements

--> P

--> OL

--> DIV

--> P

--> DIV

### 4.3.2 Konnektorname und Versionsinformationen

--> DIV

--> DIV

--> DIV

--> DIV

--> P

### 4.3.3 Konfigurationsdaten: Persistieren sowie Export-Import

--> DIV

--> DIV

--> DIV

--> P

--> DIV

--> DIV

### 4.3.4 Administration von Fachmodulen

--> P

--> DIV

--> DIV

### 4.3.5 Neustart und Werksreset

--> DIV

--> DIV

--> P

### 4.3.6 Leistungsumfänge und Standalone-Szenarios

--> P

--> DIV

--> P

--> P

--> UL

--> P

--> DIV

--> P

### 4.3.7 Online-Anbindung verwalten

--> P

--> P

--> P

--> DIV

--> DIV

--> DIV

--> P

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> P

--> P

--> UL

### 4.3.8 Re-Registrierung des Konnektors mit weiterem NK-Zertifikat

--> P

--> DIV

--> DIV

--> DIV

### 4.3.9 Remote Management (Optional)

--> P

--> P

--> P

--> DIV

--> P

--> DIV

--> DIV

--> DIV

--> DIV

--> P

--> DIV

--> P

--> DIV

--> DIV

--> DIV

--> P

--> P

--> P

--> DIV

--> DIV

--> P

--> P

--> TABLE

--> P

--> DIV

--> DIV

--> P

### 4.3.10 Software- und Konfigurationsaktualisierung (KSR-Client)

--> P

--> P

--> UL

### 4.3.10.1 Funktionsmerkmalweite Aspekte

--> P

--> P

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

### 4.3.10.2 Durch Ereignisse ausgelöste Reaktionen

--> DIV

### 4.3.10.3 Interne TUCs, nicht durch Fachmodule nutzbar

### 4.3.10.3.1 TUC_KON_280 „Konnektoraktualisierung durchführen“

--> DIV

--> P

### 4.3.10.3.2 TUC_KON_281 „Kartenterminalaktualisierung anstoßen“

--> P

--> DIV

--> P

### 4.3.10.3.3 TUC_KON_282 „UpdateInformationen beziehen“

--> DIV

### 4.3.10.3.4 TUC_KON_283 „Infrastruktur Konfiguration aktualisieren“

--> DIV

### 4.3.10.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.3.10.4.1 TUC_KON_285 „UpdateInformationen für Fachmodul beziehen“

--> DIV

### 4.3.10.4.2 TUC_KON_286 „Paket für Fachmodul laden“

--> DIV

### 4.3.10.5 Operationen an der Außenschnittstelle

--> P

### 4.3.10.6 Betriebsaspekte

--> DIV

--> DIV

### 4.3.10.6.1 TUC_KON_284 KSR-Client initialisieren

--> DIV

--> DIV

--> P

--> P

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> DIV

--> P

--> DIV

--> DIV

--> DIV

--> DIV

### 4.3.11 Konnektorstatus

--> DIV

--> DIV

### 4.4 Hardware-Merkmale des Konnektors

--> DIV

--> P

--> DIV

--> P

--> DIV

--> DIV

--> P

--> DIV

--> DIV

--> DIV

--> P

### 5 Anhang A – Verzeichnisse

### 5.1 Abkürzungen

--> TABLE

### 5.2 Glossar

--> TABLE

--> P

### 5.3 Abbildungsverzeichnis

--> DIV

--> DIV

### 5.4 Tabellenverzeichnis

--> DIV

--> DIV

### 5.5 Referenzierte Dokumente

### 5.5.1 Dokumente der gematik

--> P

--> TABLE

### 5.5.2 Weitere Dokumente

--> TABLE

--> P

### 6 Anhang B – Profilierung der Signatur- und Verschlüsselungsformate (normativ)

### 6.1 Profilierung der Verschlüsselungsformate

### 6.2 Profilierung der Signaturformate

--> P

--> TABLE

### 6.3 Profilierung VerificationReport

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> OL

--> P

--> P

--> P

--> OL

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> OL

--> P

--> OL

--> P

--> P

--> P

--> P

--> OL

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> OL

--> P

--> P

--> P

--> P

--> P

--> OL

--> P

--> P

--> P

--> P

--> P

--> OL

--> P

--> P

--> P

--> OL

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> OL

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> OL

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> OL

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> OL

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> OL

--> P

--> P

--> P

--> P

--> P

--> P

--> OL

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> OL

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> OL

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> OL

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

### 6.4 Profilierung der Dokumentenformate und Nachrichten

--> P

--> TABLE

--> P

--> TABLE

--> P

### 7 Anhang F – Übersicht Events

--> P

--> TABLE

--> P

--> P

--> UL

### 8 Anhang H – Mapping von „Architektur der TI-Plattform“ auf Konnektorspezifikation

--> P

--> TABLE

--> P

--> P

--> TABLE

--> P

--> P

--> TABLE

--> P

--> P

--> TABLE

### 9 Anhang I – Umsetzungshinweise (informativ)

--> P

--> P

### 9.1 Systemüberblick

### 9.1.1 – Hinweise zur Sicherheitsevaluierung nach Common Criteria

--> P

--> P

--> P

### 9.1.1.1 Separationsmechanismen des Konnektors

--> P

--> P

--> P

--> P

--> P

--> UL

--> P

--> P

### 9.1.1.2 Granularität der TSF

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> OL

### 9.2 Übergreifende Festlegungen

### 9.2.1 Interne Mechanismen

### 9.2.1.1 Zufallszahlen und Schlüssel

--> P

### 9.3 Funktionsmerkmale

### 9.3.1 Anwendungskonnektor

### 9.3.1.1 Administration des Informationsmodells

--> P

--> P

--> OL

### 9.3.1.2 Vorgehensvariante für das Handling von CardSessions

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> P

--> UL

--> P

--> UL

--> P

--> P

### 9.3.1.3 Darstellung von Terminal-Anzeigen auf einem Kartenterminal

--> P

### 10 Anhang K – Szenarien im dezentralen Umfeld

--> P

--> P

--> P

--> P

### 10.1 Szenario 1: Einfache Installation ohne spezielle Anforderungen und ohne bestehende Infrastruktur

--> P

--> P

### 10.1.1 Beschreibung des Szenarios

--> P

--> P

--> P

--> P

### 10.1.2 Voraussetzungen

--> UL

### 10.1.3 Auswirkungen

--> UL

### 10.2 Szenario 2: Installation mit mehreren Behandlungsräumen

--> P

--> P

### 10.2.1 Beschreibung des Szenarios

--> P

--> P

--> P

### 10.2.2 Voraussetzungen

--> UL

### 10.2.3 Auswirkungen

--> UL

### 10.3 Szenario 3: Integration in bestehende Infrastruktur ohne Netzsegmentierung

--> P

--> P

### 10.3.1 Beschreibung des Szenarios

--> P

--> P

--> P

--> P

--> P

### 10.3.2 Voraussetzungen

--> UL

### 10.3.3 Auswirkungen

--> UL

### 10.4 Szenario 4: Integration in bestehende Infrastruktur mit Netzsegmentierung

--> P

--> P

### 10.4.1 Beschreibung des Szenarios

--> P

### 10.4.2 Voraussetzungen

--> UL

### 10.4.3 Auswirkungen

--> UL

### 10.5 Szenario 5: Zentral gesteckter HBA

--> P

--> P

### 10.5.1 Beschreibung des Szenarios

--> P

--> P

--> P

### 10.5.2 Voraussetzungen

--> P

--> UL

### 10.5.3 Auswirkung

--> UL

### 10.6 Szenario 6: Installation mit zentralem PS

--> P

--> P

### 10.6.1 Beschreibung des Szenarios

--> P

--> P

### 10.6.2 Voraussetzungen

--> UL

### 10.6.3 Auswirkungen

--> UL

### 10.7 Szenario 7: Mehrere Mandanten

--> P

--> P

### 10.7.1 Beschreibung des Szenarios

--> P

### 10.7.2 Voraussetzungen

--> UL

### 10.7.3 Auswirkungen

--> UL

### 10.8 Szenario 9: Standalone Konnektor - Physische Trennung

--> P

--> P

### 10.8.1 Beschreibung des Szenarios

--> P

--> P

--> P

--> P

--> P

--> P

### 10.8.2 Voraussetzungen

--> P

--> UL

### 10.8.3 Auswirkung

--> UL

### 11 Anhang L – Datentypen von Eingangs- und Ausgangsdaten

--> P

--> TABLE

--> P

[Dokumentinformationen]: #dokumentinformationen
[Inhaltsverzeichnis]: #inhaltsverzeichnis
[1]: #1-einordnung-des-dokumentes
[1.1]: #11-zielsetzung
[1.2]: #12-zielgruppe
[1.3]: #13-geltungsbereich
[1.4]: #14-abgrenzung-des-dokuments
[1.5]: #15-methodik
[1.5.1]: #151-anforderungen
[1.5.2]: #152-offene-punkte
[1.5.3]: #153-erläuterungen-zur-spezifikation-des-außenverhaltens
[1.5.4]: #154-erläuterungen-zur-dokumentenstruktur-und-dokumentenmechanismen
[1.5.4.1]: #1541-modulare-spezifikation-über-funktionsmerkmale
[1.5.4.2]: #1542-technische-use-cases--tucs
[1.5.4.3]: #1543-eventmechanismus
[1.5.4.4]: #1544-konfigurationsparameter-und-zustandswerte
[2]: #2-systemüberblick
[2.1]: #21-logische-struktur
[2.2]: #22-sicherer-datenspeicher
[2.3]: #23-Überblick-konnektoridentität
[2.4]: #24-mandantenfähigkeit
[2.5]: #25-versionierung
[2.6]: #26-fachanwendungen
[2.7]: #27-netzseitige-einsatzszenarien
[2.7.1]: #271-parameter-anlwanbindungsmodus
[2.7.2]: #272-parameter-anlwinternetmodus
[2.8]: #28-lokale-und-entfernte-kartenterminals
[2.9]: #29-standaloneszenario
[3]: #3-Übergreifende-festlegungen
[3.1]: #31-allgemeine-übergreifende-festlegungen
[3.1.1]: #311-dokumentformate
[3.1.2]: #312-kartentypen
[3.1.3]: #313-Übergreifende-festlegungen-zum-aufbau-von-sicheren-verbindungen
[3.2]: #32-konnektoridentität-und-gsmck
[3.2.1]: #321-organisatorische-anforderungen-und-sperrprozesse
[3.3]: #33-bootupphase
[3.4]: #34-betriebszustand
[3.4.1]: #341-betriebsaspekte
[3.5]: #35-fachliche-anbindung-der-clientsysteme
[3.5.1]: #351-betriebsaspekte
[3.6]: #36-clientsystemschnittstelle
[3.6.1]: #361-soapschnittstelle
[3.6.2]: #362-statusrückmeldung-und-fehlerbehandlung
[3.6.3]: #363-transport-großer-dokumente
[3.7]: #37-verwendung-manuell-importierter-cazertifikate
[3.8]: #38-testunterstützung
[4]: #4-funktionsmerkmale
[4.1]: #41-anwendungskonnektor
[4.1.1]: #411-zugriffsberechtigungsdienst
[4.1.1.1]: #4111-funktionsmerkmalweite-aspekte
[4.1.1.2]: #4112-durch-ereignisse-ausgelöste-reaktionen
[4.1.1.3]: #4113-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.1.1.4]: #4114-interne-tucs-auch-durch-fachmodule-nutzbar
[4.1.1.4.1]: #41141-tuckon000-prüfe-zugriffsberechtigung
[4.1.1.5]: #4115-operationen-an-der-außenschnittstelle
[4.1.1.6]: #4116-betriebsaspekte
[4.1.2]: #412-dokumentvalidierungsdienst
[4.1.2.1]: #4121-funktionsmerkmalweite-aspekte
[4.1.2.2]: #4122-durch-ereignisse-ausgelöste-reaktionen
[4.1.2.3]: #4123-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.1.2.4]: #4124-interne-tucs-auch-durch-fachmodule-nutzbar
[4.1.2.4.1]: #41241-tuckon080-dokument-validieren”
[4.1.2.5]: #4125-operationen-an-der-außenschnittstelle
[4.1.2.6]: #4126-betriebsaspekte
[4.1.3]: #413-dienstverzeichnisdienst
[4.1.3.1]: #4131-funktionsmerkmalweite-aspekte
[4.1.3.2]: #4132-durch-ereignisse-ausgelöste-reaktionen
[4.1.3.3]: #4133-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.1.3.4]: #4134-interne-tucs-auch-durch-fachmodule-nutzbar
[4.1.3.4.1]: #41341-tuckon041-einbringen-der-endpunktinformationen-während-der-bootupphase
[4.1.3.5]: #4135-operationen-an-der-außenschnittstelle
[4.1.3.6]: #4136-betriebsaspekte
[4.1.4]: #414-kartenterminaldienst
[4.1.4.1]: #4141-funktionsmerkmalweite-aspekte
[4.1.4.2]: #4142-durch-ereignisse-ausgelöste-reaktionen
[4.1.4.3]: #4143-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.1.4.3.1]: #41431-tuckon050-beginne-kartenterminalsitzung
[4.1.4.3.2]: #41432-tuckon054-kartenterminal-hinzufügen
[4.1.4.3.3]: #41433-tuckon053-paire-kartenterminal
[4.1.4.3.4]: #41434-tuckon055-befülle-ctobject
[4.1.4.4]: #4144-interne-tucs-auch-durch-fachmodule-nutzbar
[4.1.4.4.1]: #41441-tuckon051-mit-anwender-über-kartenterminal-interagieren
[4.1.4.4.2]: #41442-tuckon056-karte-anfordern
[4.1.4.4.3]: #41443-tuckon057-karte-auswerfen
[4.1.4.4.4]: #41444-tuckon058-displaygröße-ermitteln
[4.1.4.5]: #4145-operationen-an-der-außenschnittstelle
[4.1.4.5.1]: #41451-requestcard
[4.1.4.5.2]: #41452-ejectcard
[4.1.4.6]: #4146-betriebsaspekte
[4.1.4.6.1]: #41461-allgemeine-betriebsaspekte
[4.1.4.6.2]: #41462-kartenterminals-pflegen
[4.1.4.6.3]: #41463-import-der-kartenterminalinformationen
[4.1.5]: #415-kartendienst
[4.1.5.1]: #4151-funktionsmerkmalweite-aspekte
[4.1.5.2]: #4152-durch-ereignisse-ausgelöste-reaktionen
[4.1.5.3]: #4153-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.1.5.3.1]: #41531-tuckon001-karte-öffnen
[4.1.5.4]: #4154-interne-tucs-auch-durch-fachmodule-nutzbar
[4.1.5.4.1]: #41541-tuckon026-liefere-cardsession
[4.1.5.4.2]: #41542-tuckon012-pin-verifizieren
[4.1.5.4.3]: #41543-tuckon019-pin-ändern
[4.1.5.4.4]: #41544-tuckon021-pin-entsperren
[4.1.5.4.5]: #41545-tuckon022-liefere-pinstatus
[4.1.5.4.6]: #41546-tuckon027-pinschutz-einausschalten
[4.1.5.4.7]: #41547-tuckon023-karte-reservieren
[4.1.5.4.8]: #41548-tuckon005-cardtocard-authentisieren
[4.1.5.4.9]: #41549-tuckon202-lesedatei
[4.1.5.4.10]: #415410-tuckon203-schreibedatei
[4.1.5.4.11]: #415411-tuckon204-löschedateiinhalt
[4.1.5.4.12]: #415412-tuckon209-leserecord
[4.1.5.4.13]: #415413-tuckon210-schreiberecord
[4.1.5.4.14]: #415414-tuckon211-löscherecordinhalt
[4.1.5.4.15]: #415415-tuckon214-fügehinzurecord
[4.1.5.4.16]: #415416-tuckon215-sucherecord
[4.1.5.4.17]: #415417-tuckon018-egksperrung-prüfen
[4.1.5.4.18]: #415418-tuckon006-datenzugriffsaudit-egk-schreiben
[4.1.5.4.19]: #415419-tuckon218-signiere
[4.1.5.4.20]: #415420-tuckon219-entschlüssele
[4.1.5.4.21]: #415421-tuckon200-sendeapdu
[4.1.5.4.22]: #415422-tuckon024-karte-zurücksetzen
[4.1.5.4.23]: #415423-tuckon216-lesezertifikat
[4.1.5.4.24]: #415424-tuckon036-lieferefachlicherolle
[4.1.5.5]: #4155-operationen-an-der-außenschnittstelle
[4.1.5.5.1]: #41551-verifypin
[4.1.5.5.2]: #41552-changepin
[4.1.5.5.3]: #41553-getpinstatus
[4.1.5.5.4]: #41554-unblockpin
[4.1.5.5.5]: #41555-enablepin
[4.1.5.5.6]: #41556-disablepin
[4.1.5.6]: #4156-betriebsaspekte
[4.1.5.6.1]: #41561-tuckon025-initialisierung-kartendienst
[4.1.5.6.2]: #41562-kartenübersicht-und-pinmanagement
[4.1.6]: #416-systeminformationsdienst
[4.1.6.1]: #4161-funktionsmerkmalweite-aspekte
[4.1.6.2]: #4162-durch-ereignisse-ausgelöste-reaktionen
[4.1.6.3]: #4163-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.1.6.4]: #4164-interne-tucs-auch-durch-fachmodule-nutzbar
[4.1.6.4.1]: #41641-tuckon256-systemereignis-absetzen
[4.1.6.4.2]: #41642-tuckon252-liefere-ktliste
[4.1.6.4.3]: #41643-tuckon253-liefere-kartenliste
[4.1.6.4.4]: #41644-tuckon254-liefere-ressourcendetails
[4.1.6.5]: #4165-operationen-an-der-außenschnittstelle
[4.1.6.5.1]: #41651-getcardterminals
[4.1.6.5.2]: #41652-getcards
[4.1.6.5.3]: #41653-getresourceinformation
[4.1.6.5.4]: #41654-subscribe
[4.1.6.5.5]: #41655-unsubscribe
[4.1.6.5.6]: #41656-renewsubscriptions
[4.1.6.5.7]: #41657-getsubscription
[4.1.6.6]: #4166-betriebsaspekte
[4.1.7]: #417-verschlüsselungsdienst
[4.1.7.1]: #4171-funktionsmerkmalweite-aspekte
[4.1.7.2]: #4172-durch-ereignisse-ausgelöste-reaktionen
[4.1.7.3]: #4173-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.1.7.4]: #4174-interne-tucs-auch-durch-fachmodule-nutzbar
[4.1.7.4.1]: #41741-tuckon070-daten-hybrid-verschlüsseln”
[4.1.7.4.2]: #41742-tuckon071-daten-hybrid-entschlüsseln”
[4.1.7.4.3]: #41743-tuckon072-daten-symmetrisch-verschlüsseln”
[4.1.7.4.4]: #41744-tuckon073-daten-symmetrisch-entschlüsseln”
[4.1.7.4.5]: #41745-tuckon075-symmetrisch-verschlüsseln
[4.1.7.4.6]: #41746-tuckon076-symmetrisch-entschlüsseln
[4.1.7.5]: #4175-operationen-an-der-außenschnittstelle
[4.1.7.5.1]: #41751-encryptdocument
[4.1.7.5.2]: #41752-decryptdocument
[4.1.7.6]: #4176-betriebsaspekte
[4.1.8]: #418-signaturdienst
[4.1.8.1]: #4181-funktionsmerkmalweite-aspekte
[4.1.8.1.1]: #41811-dokumentensignatur
[4.1.8.1.2]: #41812-signaturrichtlinien
[4.1.8.1.3]: #41813-signaturzeitpunkt
[4.1.8.1.4]: #41814-jobnummer
[4.1.8.1.5]: #41815-komfortsignatur
[4.1.8.2]: #4182-durch-ereignisse-ausgelöste-reaktionen
[4.1.8.3]: #4183-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.1.8.3.1]: #41831-tuckon155-dokumente-zur-signatur-vorbereiten”
[4.1.8.3.2]: #41832-tuckon165-signaturvoraussetzungen-für-nonqes-prüfen
[4.1.8.3.3]: #41833-tuckon166-nonqes-signaturen-erstellen
[4.1.8.3.4]: #41834-tuckon152-signaturvoraussetzungen-für-qes-prüfen
[4.1.8.3.5]: #41835-tuckon154-qes-signaturen-erstellen
[4.1.8.3.6]: #41836-tuckon168-einzelsignatur-qes-erstellen
[4.1.8.3.7]: #41837-tuckon158-komfortsignaturen-erstellen
[4.1.8.4]: #4184-interne-tucs-auch-durch-fachmodule-nutzbar
[4.1.8.4.1]: #41841-tuckon160-dokumente-nonqes-signieren”
[4.1.8.4.2]: #41842-tuckon161-nonqes-dokumentsignatur-prüfen”
[4.1.8.4.3]: #41843-tuckon162-kryptographische-prüfung-der-xmldokumentensignatur”
[4.1.8.4.4]: #41844-tuckon150-dokumente-qes-signieren”
[4.1.8.4.5]: #41845-anforderungen-an-die-stapelsignatur
[4.1.8.4.6]: #41846-tuckon151-qes-dokumentensignatur-prüfen
[4.1.8.4.7]: #41847-tuckon170-dokumente-mit-komfort-signieren”
[4.1.8.4.8]: #41848-tuckon171-komfortsignatur-einschalten”
[4.1.8.4.9]: #41849-tuckon172-komfortsignatur-ausschalten”
[4.1.8.4.10]: #418410-tuckon173-liefere-signaturmodus”
[4.1.8.5]: #4185-operationen-an-der-außenschnittstelle
[4.1.8.5.1]: #41851-signdocument-nonqes-und-qes
[4.1.8.5.2]: #41852-verifydocument-nonqes-und-qes
[4.1.8.5.3]: #41853-stopsignature
[4.1.8.5.4]: #41854-getjobnumber
[4.1.8.5.5]: #41855-activatecomfortsignature
[4.1.8.5.6]: #41856-deactivatecomfortsignature
[4.1.8.5.7]: #41857-getsignaturemode
[4.1.8.6]: #4186-betriebsaspekte
[4.1.9]: #419-zertifikatsdienst
[4.1.9.1]: #4191-funktionsmerkmalweite-aspekte
[4.1.9.2]: #4192-durch-ereignisse-ausgelöste-reaktionen
[4.1.9.3]: #4193-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.1.9.3.1]: #41931-tuckon032-tsl-aktualisieren
[4.1.9.3.2]: #41932-tuckon031-bnetzavl-aktualisieren
[4.1.9.3.3]: #41933-tuckon040-crl-aktualisieren
[4.1.9.3.4]: #41934-tuckon033-zertifikatsablauf-prüfen
[4.1.9.4]: #4194-interne-tucs-auch-durch-fachmodule-nutzbar
[4.1.9.4.1]: #41941-tuckon037-zertifikat-prüfen
[4.1.9.4.2]: #41942-tuckon042-cvzertifikat-prüfen
[4.1.9.4.3]: #41943-tuckon034-zertifikatsinformationen-extrahieren
[4.1.9.5]: #4195-operationen-an-der-außenschnittstelle
[4.1.9.5.1]: #41951-checkcertificateexpiration
[4.1.9.5.2]: #41952-readcardcertificate
[4.1.9.5.3]: #41953-verifycertificate
[4.1.9.6]: #4196-betriebsaspekte
[4.1.9.6.1]: #41961-tuckon035-zertifikatsdienst-initialisieren
[4.1.10]: #4110-protokollierungsdienst
[4.1.10.1]: #41101-funktionsmerkmalweite-aspekte
[4.1.10.2]: #41102-durch-ereignisse-ausgelöste-reaktionen
[4.1.10.3]: #41103-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.1.10.4]: #41104-interne-tucs-auch-durch-fachmodule-nutzbar
[4.1.10.4.1]: #411041-tuckon271-schreibe-protokolleintrag
[4.1.10.5]: #41105-operationen-an-der-außenschnittstelle
[4.1.10.6]: #41106-betriebsaspekte
[4.1.10.6.1]: #411061-tuckon272-initialisierung-protokollierungsdienst
[4.1.11]: #4111-tlsdienst
[4.1.11.1]: #41111-funktionsmerkmalweite-aspekte
[4.1.11.2]: #41112-durch-ereignisse-ausgelöste-reaktionen
[4.1.11.3]: #41113-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.1.11.4]: #41114-interne-tucs-auch-durch-fachmodule-nutzbar
[4.1.11.4.1]: #411141-tuckon110-kartenbasierte-tlsverbindung-aufbauen
[4.1.11.4.2]: #411142-tuckon111-kartenbasierte-tlsverbindung-abbauen
[4.1.11.5]: #41115-operationen-an-der-außenschnittstelle
[4.1.11.6]: #41116-betriebsaspekte
[4.1.12]: #4112-ldapproxy
[4.1.12.1]: #41121-funktionsmerkmalweite-aspekte
[4.1.12.2]: #41122-durch-ereignisse-ausgelöste-reaktionen
[4.1.12.3]: #41123-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.1.12.4]: #41124-interne-tucs-auch-durch-fachmodule-nutzbar
[4.1.12.4.1]: #411241-tuckon290-ldapverbindung-aufbauen
[4.1.12.4.2]: #411242-tuckon291-verzeichnis-abfragen
[4.1.12.4.3]: #411243-tuckon292-ldapverbindung-trennen
[4.1.12.4.4]: #411244-tuckon293-verzeichnisabfrage-abbrechen
[4.1.12.5]: #41125-operationen-an-der-außenschnittstelle
[4.1.12.5.1]: #411251-unterstützte-ldapv3-operationen
[4.1.12.6]: #41126-betriebsaspekte
[4.1.13]: #4113-authentifizierungsdienst
[4.1.13.1]: #41131-funktionsmerkmalweite-aspekte
[4.1.13.1.1]: #411311-externe-authentisierung
[4.1.13.2]: #41132-durch-ereignisse-ausgelöste-reaktionen
[4.1.13.3]: #41133-interne-tucs
[4.1.13.4]: #41134-operationen-an-der-außenschnittstelle
[4.1.13.4.1]: #411341-externalauthenticate
[4.1.13.5]: #41135-betriebsaspekte
[4.1.14]: #4114-betriebsdatenmeldedienst
[4.2]: #42-netzkonnektor
[4.2.1]: #421-anbindung-lanwan
[4.2.1.1]: #4211-funktionsmerkmalweite-aspekte
[4.2.1.1.1]: #42111-netzwerksegmentierung
[4.2.1.1.2]: #42112-routing-und-firewall
[4.2.1.2]: #4212-durch-ereignisse-ausgelöste-reaktionen
[4.2.1.3]: #4213-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.2.1.3.1]: #42131-tuckon305-lanadapter-initialisieren
[4.2.1.3.2]: #42132-tuckon306-wanadapter-initialisieren
[4.2.1.3.3]: #42133-tuckon304-netzwerkrouten-einrichten
[4.2.1.4]: #4214-interne-tucs-auch-durch-fachmodule-nutzbar
[4.2.1.5]: #4215-operationen-an-der-außenschnittstelle
[4.2.1.6]: #4216-betriebsaspekte
[4.2.2]: #422-dhcpserver
[4.2.2.1]: #4221-funktionsmerkmalweite-aspekte
[4.2.2.2]: #4222-durch-ereignisse-ausgelöste-reaktionen
[4.2.2.3]: #4223-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.2.2.4]: #4224-interne-tucs-auch-durch-fachmodule-nutzbar
[4.2.2.5]: #4225-operationen-an-der-außenschnittstelle
[4.2.2.5.1]: #42251-liefere-netzwerkinformationen-über-dhcp
[4.2.2.6]: #4226-betriebsaspekte
[4.2.2.6.1]: #42261-tuckon343-initialisierung-dhcpserver
[4.2.3]: #423-dhcpclient
[4.2.3.1]: #4231-funktionsmerkmalweite-aspekte
[4.2.3.2]: #4232-durch-ereignisse-ausgelöste-reaktionen
[4.2.3.3]: #4233-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.2.3.3.1]: #42331-tuckon341-dhcpinformationen-beziehen
[4.2.3.4]: #4234-interne-tucs-auch-durch-fachmodule-nutzbar
[4.2.3.5]: #4235-operationen-an-der-außenschnittstelle
[4.2.3.6]: #4236-betriebsaspekte
[4.2.4]: #424-vpnclient
[4.2.4.1]: #4241-funktionsmerkmalweite-aspekte
[4.2.4.2]: #4242-durch-ereignisse-ausgelöste-reaktionen
[4.2.4.3]: #4243-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.2.4.3.1]: #42431-tuckon321-verbindung-zu-dem-vpnkonzentrator-der-ti-aufbauen
[4.2.4.3.2]: #42432-tuckon322-verbindung-zu-dem-vpnkonzentrator-des-sis-aufbauen
[4.2.4.4]: #4244-interne-tucs-auch-durch-fachmodule-nutzbar
[4.2.4.5]: #4245-operationen-an-der-außenschnittstelle
[4.2.4.6]: #4246-betriebsaspekte
[4.2.5]: #425-zeitdienst
[4.2.5.1]: #4251-funktionsmerkmalweite-aspekte
[4.2.5.2]: #4252-durch-ereignisse-ausgelöste-reaktionen
[4.2.5.3]: #4253-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.2.5.4]: #4254-interne-tucs-auch-durch-fachmodule-nutzbar
[4.2.5.4.1]: #42541-tuckon351-liefere-systemzeit”
[4.2.5.5]: #4255-operationen-an-der-außenschnittstelle
[4.2.5.5.1]: #42551-synctime
[4.2.5.6]: #4256-betriebsaspekte
[4.2.5.6.1]: #42561-tuckon352-initialisierung-zeitdienst
[4.2.6]: #426-namensdienst-und-dienstlokalisierung
[4.2.6.1]: #4261-funktionsmerkmalweite-aspekte
[4.2.6.2]: #4262-durch-ereignisse-ausgelöste-reaktionen
[4.2.6.3]: #4263-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.2.6.4]: #4264-interne-tucs-auch-durch-fachmodule-nutzbar
[4.2.6.4.1]: #42641-tuckon361-dnsnamen-auflösen
[4.2.6.4.2]: #42642-tuckon362-liste-der-dienste-abrufen
[4.2.6.4.3]: #42643-tuckon363-dienstdetails-abrufen
[4.2.6.5]: #4265-operationen-an-der-außenschnittstelle
[4.2.6.5.1]: #42651-getipaddress
[4.2.6.6]: #4266-betriebsaspekte
[4.2.7]: #427-optionale-verwendung-von-ipv6
[4.3]: #43-konnektormanagement
[4.3.1]: #431-zugang-und-benutzerverwaltung-des-konnektormanagements
[4.3.2]: #432-konnektorname-und-versionsinformationen
[4.3.3]: #433-konfigurationsdaten-persistieren-sowie-exportimport
[4.3.4]: #434-administration-von-fachmodulen
[4.3.5]: #435-neustart-und-werksreset
[4.3.6]: #436-leistungsumfänge-und-standaloneszenarios
[4.3.7]: #437-onlineanbindung-verwalten
[4.3.8]: #438-reregistrierung-des-konnektors-mit-weiterem-nkzertifikat
[4.3.9]: #439-remote-management-optional
[4.3.10]: #4310-software-und-konfigurationsaktualisierung-ksrclient
[4.3.10.1]: #43101-funktionsmerkmalweite-aspekte
[4.3.10.2]: #43102-durch-ereignisse-ausgelöste-reaktionen
[4.3.10.3]: #43103-interne-tucs-nicht-durch-fachmodule-nutzbar
[4.3.10.3.1]: #431031-tuckon280-konnektoraktualisierung-durchführen
[4.3.10.3.2]: #431032-tuckon281-kartenterminalaktualisierung-anstoßen
[4.3.10.3.3]: #431033-tuckon282-updateinformationen-beziehen
[4.3.10.3.4]: #431034-tuckon283-infrastruktur-konfiguration-aktualisieren
[4.3.10.4]: #43104-interne-tucs-auch-durch-fachmodule-nutzbar
[4.3.10.4.1]: #431041-tuckon285-updateinformationen-für-fachmodul-beziehen
[4.3.10.4.2]: #431042-tuckon286-paket-für-fachmodul-laden
[4.3.10.5]: #43105-operationen-an-der-außenschnittstelle
[4.3.10.6]: #43106-betriebsaspekte
[4.3.10.6.1]: #431061-tuckon284-ksrclient-initialisieren
[4.3.11]: #4311-konnektorstatus
[4.4]: #44-hardwaremerkmale-des-konnektors
[5]: #5-anhang-a-–-verzeichnisse
[5.1]: #51-abkürzungen
[5.2]: #52-glossar
[5.3]: #53-abbildungsverzeichnis
[5.4]: #54-tabellenverzeichnis
[5.5]: #55-referenzierte-dokumente
[5.5.1]: #551-dokumente-der-gematik
[5.5.2]: #552-weitere-dokumente
[6]: #6-anhang-b-–-profilierung-der-signatur-und-verschlüsselungsformate-normativ
[6.1]: #61-profilierung-der-verschlüsselungsformate
[6.2]: #62-profilierung-der-signaturformate
[6.3]: #63-profilierung-verificationreport
[6.4]: #64-profilierung-der-dokumentenformate-und-nachrichten
[7]: #7-anhang-f-–-Übersicht-events
[8]: #8-anhang-h-–-mapping-von-architektur-der-tiplattform-auf-konnektorspezifikation
[9]: #9-anhang-i-–-umsetzungshinweise-informativ
[9.1]: #91-systemüberblick
[9.1.1]: #911-–-hinweise-zur-sicherheitsevaluierung-nach-common-criteria
[9.1.1.1]: #9111-separationsmechanismen-des-konnektors
[9.1.1.2]: #9112-granularität-der-tsf
[9.2]: #92-Übergreifende-festlegungen
[9.2.1]: #921-interne-mechanismen
[9.2.1.1]: #9211-zufallszahlen-und-schlüssel
[9.3]: #93-funktionsmerkmale
[9.3.1]: #931-anwendungskonnektor
[9.3.1.1]: #9311-administration-des-informationsmodells
[9.3.1.2]: #9312-vorgehensvariante-für-das-handling-von-cardsessions
[9.3.1.3]: #9313-darstellung-von-terminalanzeigen-auf-einem-kartenterminal
[10]: #10-anhang-k-–-szenarien-im-dezentralen-umfeld
[10.1]: #101-szenario-1-einfache-installation-ohne-spezielle-anforderungen-und-ohne-bestehende-infrastruktur
[10.1.1]: #1011-beschreibung-des-szenarios
[10.1.2]: #1012-voraussetzungen
[10.1.3]: #1013-auswirkungen
[10.2]: #102-szenario-2-installation-mit-mehreren-behandlungsräumen
[10.2.1]: #1021-beschreibung-des-szenarios
[10.2.2]: #1022-voraussetzungen
[10.2.3]: #1023-auswirkungen
[10.3]: #103-szenario-3-integration-in-bestehende-infrastruktur-ohne-netzsegmentierung
[10.3.1]: #1031-beschreibung-des-szenarios
[10.3.2]: #1032-voraussetzungen
[10.3.3]: #1033-auswirkungen
[10.4]: #104-szenario-4-integration-in-bestehende-infrastruktur-mit-netzsegmentierung
[10.4.1]: #1041-beschreibung-des-szenarios
[10.4.2]: #1042-voraussetzungen
[10.4.3]: #1043-auswirkungen
[10.5]: #105-szenario-5-zentral-gesteckter-hba
[10.5.1]: #1051-beschreibung-des-szenarios
[10.5.2]: #1052-voraussetzungen
[10.5.3]: #1053-auswirkung
[10.6]: #106-szenario-6-installation-mit-zentralem-ps
[10.6.1]: #1061-beschreibung-des-szenarios
[10.6.2]: #1062-voraussetzungen
[10.6.3]: #1063-auswirkungen
[10.7]: #107-szenario-7-mehrere-mandanten
[10.7.1]: #1071-beschreibung-des-szenarios
[10.7.2]: #1072-voraussetzungen
[10.7.3]: #1073-auswirkungen
[10.8]: #108-szenario-9-standalone-konnektor--physische-trennung
[10.8.1]: #1081-beschreibung-des-szenarios
[10.8.2]: #1082-voraussetzungen
[10.8.3]: #1083-auswirkung
[11]: #11-anhang-l-–-datentypen-von-eingangs-und-ausgangsdaten

