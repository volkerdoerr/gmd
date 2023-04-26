
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

‹AFO-ID› - ‹Titel der Afo›  
 Text / Beschreibung  
 [‹=]  
 Dabei
umfasst die Anforderung sämtliche innerhalb der Afo-ID und der Textmarke
angeführten Inhalte.

‹AFO-ID› - *

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

gefolgt von (falls definiert):[Datentyp]

gefolgt von (falls zutreffend):

- optional; default: ‹Defaultwert› bzw.

- optional;/‹erklärender Text›  

Hierbei bedeuten:  
   
 - optional; kennzeichnet optionale Ein- und
Ausgangsparameter

default: ‹Defaultwert› definiert den Defaultwert für den Fall, dass der
Eingangsparameter leer ist bzw. nicht übergeben wurde

/ ‹erklärender Text› beschreibt Bedingungen, unter denen der
Eingangsparameter optional ist

     gefolgt von (falls vorhanden):(‹erklärender Text›)

b) Namen mit kleinem Anfangsbuchstaben bezeichnen Ein- und Ausgangsparameter;
Namen mit großem Anfangsbuchstaben bezeichnen Datentypen.

Beispiel:

 ---> TABLE

Die im Dokument verwendeten Datentypen sind definiert in [Anhang L –
Datentypen von Eingangs- und Ausgangsdaten].

Festlegungen zur Schreibweise des Aufrufs von TUCs

Ein TUC-Aufruf erfolgt nach folgendem Muster:

‹TUC-Bezeichner› {

   ‹TUC-Eingangsparameter Name› = ‹TUC Eingangsparameter Wert›;

   … }

Beispiel:

TUC_KON_256 {  
     topic = „CT/DISCONNECTED“;  
     eventType =
Op;  
     severity = Info;  
     parameters = („CtID=$CT.CTID,
Hostname=$CT.HOSTNAME“) }

Vereinfachung:

Ist ‹TUC-Eingangsparameter Name› des aufzurufenden TUCs gleich der
Variablen, die als ‹ TUC Eingangsparameter Wert› gesetzt wird, so kann
dieser Bezeichner ohne Zuweisung geschrieben werden.

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
erhoben. Diese Konfigurationsparameter werden über eine ReferenzID definiert.
Definierte Konfigurationsparameter können in allen Kapiteln der Spezifikation
referenziert werden. Den Ort, an welchem ein solcher Konfigurationsparameter
definiert/erhoben und somit dessen Bedeutung beschrieben wird, lässt sich
über den Präfix der ReferenzID erkennen: CERT_CRL_DOWNLOAD_ADDRESS (also
„Cert“) wird im Zertifikatsdienst definiert, MGM_LU_ONLINE (also „MGM“)
wird im Konnektormanagement definiert usw.

Die ReferenzIDs der Konfigurationsparameter besitzen in ihrer Schreibweise nur
innerhalb des Dokuments Gültigkeit. In der Umsetzung können für die
Konfigurationswerte herstellerspezifische Beschreibungen und Labels verwendet
werden.

Vergleichbar zu diesen Konfigurationsparametern, sind Zustandswerte. Auch diese
werden über ReferenzIDs definiert, nur können sie nicht durch den
Administrator verändert oder eingesehen werden. Sie finden nur konnektorintern
Verwendung und sind für die Beschreibung der Verhaltensweise notwendig,
Beispiele sind CTM_CT_LIST für die Liste der durch den Konnektor verwalteten
Kartenterminals oder CM_CARD_LIST für die Liste der aktuell erreichbaren
Karten. Zustandswerte verwenden die gleichen Präfixe wie
Konfigurationsparameter.

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
etc.). Eine Übersicht der Zuordnung „logische Schnittstellen  technische
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

Konfiguration 1: Konnektor als Gateway (ANLW_ANBINDUNGS_MODUS = InReihe):  

Diese Konfiguration ist geeignet für Szenarien, in denen der Konnektor
zwischen das lokale Netz und das Internet Access Gateway (IAG) (z. B. Router
mit DSL-/Kabelmodem) geschaltet wird. (vgl. Anhang K, Szenario 1)

Konfiguration 2: Konnektor eingebettet in existierende Infrastruktur
(ANLW_ANBINDUNGS_MODUS = Parallel): Diese Konfiguration ist geeignet für
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

In [gemSpec_Krypt#6] wird das Kommunikationsprotokoll zwischen einem Client und
einer Vertrauenswürdigen Ausführungsumgebung (VAU) spezifiziert. Dabei wird
ein sicherer Kanal auf HTTP-Anwendungsschicht zwischen dem Client und der VAU
(Server) aufgebaut. Der Client ist hier ein Fachmodul des Konnektors; der
Server ist ein Fachdienst.

Der Gesamtablauf der Schlüsselableitungsfunktionalität gemäß
[gemSpec_SGD#2.3] für den Konnektor als Client ist aufgeteilt zwischen
Basiskonnektor und Fachmodul. Die kryptographischen Vorgaben (u.a.
Durchführung des ECDH, Schlüsselerzeugung, Ver- und Entschlüsselung,
Signaturerzeugung und -prüfung) werden dabei durch den Basiskonnektor
realisiert.

### 3.2 Konnektoridentität und gSMC-K

Die Notwendigkeit, den Konnektor mit mehr als einer gSMC-K zu bestücken, kann
sich aus den Lastanforderungen aus [gemSpec_Perf#4.1.2] ergeben.

gSMC-Ks gemäß [gemSpec_gSMC-K_ObjSys] verfügen über die Möglichkeit zur
nachträglichen Generierung von Schlüsselpaaren und dem Nachladen der
zugehörigen Zertifikate. Dieser Mechanismus wird erst in kommenden Releases
durch den Konnektor unterstützt. Initial sind alle Identitäten bereits einmal
auf der gSMC-K vorhanden.

### 3.2.1 Organisatorische Anforderungen und Sperrprozesse

Die Anforderung ist für die Anwendungsfälle Registrierung,
IPsec-Authentisierung und Autorisierung beim VPN-Zugangsdienst,
TLS-Authentisierung zum eHealth-Kartenterminal, TLS-Authentisierung zum
Primärsystem nachzuweisen. Wenn RSA-2048 in der TI abgekündigt wird,
entfällt dadurch die Anforderung.

Das bedeutet, dass der Konnektorhersteller je Konnektor die für die
Identifikation des C.NK.VPN-Zertifikates relevanten Daten wie z. B.
Seriennummer des Konnektors und Art der verbauten Komponenten, Seriennummer der
gSMC-K, etc. für seinen Sperrprozesse dokumentieren muss.

Sperrberechtigt ist die gematik im Rahmen des Change-Verfahrens (siehe
[gemRL_Betr_TI#5.4).

Dazu bedient er die standardmäßige Schnittstelle zum TSP (siehe
[gemSpec_X.509_TSP#TIP1-A_3643]).

Der Hersteller des Konnektors übernimmt im Rahmen der organisatorischen
Sperrung die Aufgabe der Anwenderkommunikation gegenüber den betroffenen
Anwendern. Die Eckpunkte zur Kommunikation sind Bestandteil des Beschlusses zur
Außerbetriebnahme einer Konnektor-Baureihe und im Rahmen des Change-Verfahrens
zwischen den Beteiligten abgestimmt.

Dies kann bspw. durch Übertragung der Aufgabe an einen Dritten realisiert
werden. Dabei sind die Zuordnungen Konnektor zu Zertifikat gemäß Anforderung
„Dokumentation der Konnektorzertifikatszuordnungen“ zur Verfügung zu
stellen.

Bei der Schlüsselerzeugung für die gSMC-K muss insbesondere auch mit
technischen Maßnahmen die Vertraulichkeit der relevanten Schlüssel
sichergestellt werden:

### 3.3 Bootup-Phase

Die hier gelisteten TUCs bilden nicht die abschließende Menge der während der
Bootup-Phase zu erfüllenden Anforderungen. In den einzelnen Funktionsmerkmalen
werden weitere Einzelanforderungen erhoben, die als Ausführungszeitpunkt die
Bootup-Phase benennen (siehe Unterkapitel „Betriebsaspekte“ der einzelnen
Funktionsmerkmal-Kapiteln, sowie Kapitel 4.3 Konnektormanagement).

### 3.4 Betriebszustand

Erklärung „Minütlich gleitende 10-Minuten-Summe“: Für die jeweilige
Operation wird die Summe aller OK_Val und NOK_Val der letzten 10 Minuten
gebildet. Diese Summe wird jede Minute neu berechnet.

Unter „kartenbasiert“ sind nicht nur Lösungen mit Smartcards sondern auch
solche mit HSMs (Hardware Security Modules) zu verstehen.

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

Bei einem mittleren Zeitabstand zwischen Ausfällen (MTBF) von 50 Jahren ist die
Wahrscheinlichkeit, dass ein Fehlerzustand mit Severity=Fatal auftritt, kleiner
2 % pro Jahr.

### 3.4.1 Betriebsaspekte

Der Konnektor soll per Signaleinrichtung am Konnektor die Fehlerzustände mit
Severity „Error“ und „Fatal“ anzeigen (siehe [TIP1-A_4843]).

### 3.5 Fachliche Anbindung der Clientsysteme

Für die Schnittstellen des Konnektors zu den Clientsystemen kann gesteuert
werden:

 ---> UL

Dabei werden die folgenden zwei Nutzungsszenarien nicht unterschieden:

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

Bei der Authentisierung des Clientsystems geht es um eine Authentisierung in
zwei Richtungen:

 ---> OL

Für beide Richtungen kann das Clientsystem dasselbe Zertifikat verwenden.

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

Aus A_21224 resultiert direkt, dass als Client-Authentisierung für LDAPS nur
Client-Zertifikate unterstützt werden müssen. Die Authentisierung mit
Username/Passwort wird bei LDAPS nicht unterstützt.

Es sei noch einmal betont, dass TIP1-A_5009 sich nur auf SOAP und CETP bezieht
und TIP1-A_4516 das Basic-Authentication Verfahren nur für HTTP fordert.

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

### 3.6 Clientsystemschnittstelle

### 3.6.1 SOAP-Schnittstelle

Für die Beschreibung der SOAP-Schnittstelle zum Clientsystem wird in dieser
Spezifikation WSDL Version 1.1 [WSDL1.1] eingesetzt. Die Interoperabilität
zwischen verschiedenen SOAP-Implementierungen wird durch die Vorgaben des WS-I
Basic Profile erreicht.

Da der Konnektor UTF-16 nicht unterstützt, muss das Clientsystem den Request in
UTF-8 kodieren. Diese Festlegungen gelten nur für die eigentliche
SOAP-Nachricht. Sind in der SOAP-Nachricht base64-encodierte XML-Elemente
vorhanden, so können diese XML-Elemente andere Zeichencodierungen aufweisen.

Fachmodule

Fachmodule können für Web-Services, die Clientsystemen bereitgestellt werden,
entweder [SOAP1.1] mit [BasicProfile1.2] oder [SOAP1.2] mit [BasicProfile2.0]
verwenden. Die genaue Ausprägung erfolgt in der jeweiligen
Interfacebeschreibung des Web-Services für das Fachmodul.

### 3.6.2 Statusrückmeldung und Fehlerbehandlung

Der Konnektor bietet Operationen an der Außenschnittstelle über
SOAP-Webservices an. Treten bei der Ausführung einer Operation Fehler auf, so
werden diese an das aufrufende System gemeldet. Die von den Basisdiensten des
Konnektors angebotenen SOAP-Webservices melden Fehler, die bei der Ausführung
einer Operation auftreten, über eine SOAP-Fault-Nachricht (siehe auch
[gemSpec_OM#3.2.3]).

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

### 3.7 Verwendung manuell importierter CA-Zertifikate

TI-fremde X.509-Zertifikate werden im Rahmen des Verschlüsselungsdienstes
verwendet. Um den Vertrauensraum für diese Zertifikate abzubilden, erlaubt der
Konnektor, X.509-CA-Zertifikate zu diesen TI-fremden X.509-Zertifikaten in eine
interne Liste (CERT_IMPORTED_CA_LIST) zu importieren.

Der Konnektor kann dann im Rahmen der Hybridverschlüsselung den symmetrischen
Schlüssel empfängerspezifisch mit dessem TI-fremden X.509-Zertifikat
verschlüsseln. Die TI-fremden Zertifikate dürfen nicht zu einem anderen Zweck
als diesem eingesetzt werden.

Die Berücksichtigung der CA-Zertifikate aus CERT_IMPORTED_CA_LIST muss auf
folgende Anwendungsfälle beschränkt werden:

1. Prüfung eines Zertifikates im Rahmen der hybriden Verschlüsselung

2. Prüfung eines Zertifikates im Rahmen eines Aufrufes der Operation
"VerifyCertificate"

### 3.8 Testunterstützung

Gemäß Testkonzept der TI [gemKPT_Test#TIP1-A_6526] muss ein Hersteller eines
Konnektors seine Modelle in verschiedenen Ausführungen vorsehen: für
Testumgebung, für die Referenzumgebung und für die Produktivumgebung.  

Damit trotz dieser Forderung die Firmware je Konnektorversion für alle
Umgebungen identisch ist, wird die Erkennung der Umgebung an die gSMC-K
gebunden. Die Konnektor-Firmware muss zwischen den Umgebungen PU und RU/TU
unterscheiden. Die gSMC-K besitzt hierzu den Datencontainer
MF/EF.EnvironmentSettings, der die jeweilige Umgebungskennung enthält (PU bzw.
TU/RU). Die Umgebungskennung wird read-only auf der gSMC-K gespeichert.

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

Hinweis 1:  
 Jede Bedingung ist als Constraint mittels OCL definiert, ist
einzeln prüfbar und hat als Eingangsparameter mandantId, clientSystemId,
workplaceId, ctId, cardHandle und userId.

Hinweis 2:  
 Zur Bezeichnung einer Objektinstanz, die im Informationsmodell
vorhanden ist, wird die Notation ‹‹Entitätsbezeichner››(‹‹Komma
separierte Liste der Identitätsschlüssel›› verwendet.

Hinweis 3:  
Bei manchen Bedingungen gibt es unterschiedliche Fehlermeldungen
für die Außenschnittstelle und für die interne Protokollierung. Dann wird
folgende Notation in Spalte "Error Code" verwendet:

"‹‹Fehlercode›› an der Außenschnittstelle" für den Fehlercode, der
über die Außenschnittstelle zurückgegeben werden muss

"‹‹Fehlercode›› im Protokoll" für den Fehlercode, der für die interne
Protokollierung verwendet werden muss. 

 ---> TABLE

Hinweis zu Fehler 4018: Sicherheitszustand wird bei PIN-Eingabe erhöht.

### 4.1.1.5 Operationen an der Außenschnittstelle

Keine

### 4.1.1.6 Betriebsaspekte

Im Anhang I „Umsetzungshinweise“ werden Empfehlungen zur Umsetzung der
Administration des Informationsmodells gegeben.

### 4.1.2 Dokumentvalidierungsdienst

Der Dokumentvalidierungsdienst ist ein Dienst, der nur intern genutzt wird,
d. h., dass dessen definierte Verhaltensweisen nur in anderen TUCs des
Konnektors nachgenutzt werden. Er bietet Schnittstellen zum Validieren von
Dokumenten an. Dabei werden diejenigen spezifischen Dokumentformate
unterstützt, die an den Außenschnittstellen anderer Dienste wie Signatur- und
Verschlüsselungsdienst auftreten können (Alle_DocFormate gemäß Kapitel 3).

Die jeweils gültigen XML-Schemas der Fachmodule werden den Herstellern von der
gematik bereitgestellt.

### 4.1.2.1 Funktionsmerkmalweite Aspekte

### 4.1.2.2 Durch Ereignisse ausgelöste Reaktionen

Keine.

### 4.1.2.3 Interne TUCs, nicht durch Fachmodule nutzbar

Keine

### 4.1.2.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.1.2.4.1 TUC_KON_080 „Dokument validieren”

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
vordefinierte URL:     https://‹ANLW_LAN_IP_ADDRESS oder    
MGM_KONN_HOSTNAME›/connector.sds oderhttp://‹ANLW_LAN_IP_ADDRESS oder
MGM_KONN_HOSTNAME›/connector.sds des Konnektors auf.

Der Konnektor stellt die Liste der Dienste, der Versionen und die Endpunkte der
Dienste in einem XML-Dokument zusammen. Jeder über SOAP erreichbare
Basisdienst des Konnektors wird in dieser Liste geführt. Ferner können
Fachmodule ihre eigenen Endpunkte über TUC_KON_041 „Einbringen der
Endpunktinformationen während der Bootup-Phase“ einbringen. Die so erstellte
Liste der Dienste wird als Antwort an das Clientsystem übergeben.

Das Clientsystem prüft, ob die gewünschten Dienste und Versionen unterstützt
werden und merkt sich die Endpunkte der Dienste für die späteren Aufrufe.
Danach kann das Clientsystem diese Dienstendpunkte nach Bedarf aufrufen.

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

### 4.1.3.5 Operationen an der Außenschnittstelle

### 4.1.3.6 Betriebsaspekte

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

Zur Unterstützung von HSM-Bs benötigt der Konnektor virtuelle Kartenterminals
(CT.IS_PHYSICAL=Nein), in denen virtuelle SMC-Bs „stecken“ können (siehe
Kapitel 4.1.4). Diese Kartenterminals werden innerhalb des
Zugriffsberechtigungsdienstes sowie des Systeminformationsdienstes wie normale
Kartenterminals berücksichtigt. Weitere Details zu den logischen
Kartenterminals finden sich im Kapitel Betriebsaspekte.

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

 ---> TABLE

### 4.1.4.2 Durch Ereignisse ausgelöste Reaktionen

### 4.1.4.3 Interne TUCs, nicht durch Fachmodule nutzbar

### 4.1.4.3.1 TUC_KON_050 „Beginne Kartenterminalsitzung“

### 4.1.4.3.2 TUC_KON_054 „Kartenterminal hinzufügen“

### 4.1.4.3.3 TUC_KON_053 „Paire Kartenterminal“

### 4.1.4.3.4 TUC_KON_055 „Befülle CT-Object“

### 4.1.4.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.1.4.4.1 TUC_KON_051 „Mit Anwender über Kartenterminal interagieren“

### 4.1.4.4.2 TUC_KON_056 „Karte anfordern“

### 4.1.4.4.3 TUC_KON_057 „Karte auswerfen“

### 4.1.4.4.4 TUC_KON_058 „Displaygröße ermitteln“

### 4.1.4.5 Operationen an der Außenschnittstelle

### 4.1.4.5.1 RequestCard

### 4.1.4.5.2 EjectCard

### 4.1.4.6 Betriebsaspekte

### 4.1.4.6.1 Allgemeine Betriebsaspekte

Hinweis: Bei der Initialiserung des Kartenterminaldienstes liest der Konnektor
noch nicht die Karten, um zu ermitteln, welche Karten gesteckt sind. Dies
erfolgt erst bei Initialisierung des Kartendienstes.

### 4.1.4.6.2 Kartenterminals pflegen

Im Folgenden werden die Administratorinteraktionen beschrieben, die zum
Hinzufügen, Pairen, Bearbeiten und Löschen von Kartenterminals innerhalb der
CTM_CT_LIST angeboten werden müssen. Eine Aktualisierung der Kartenterminals
mit neuer Firmware wird in Kapitel 4.3.9 beschrieben.

Als Sicherung gegen den unbemerkten Austausch von Kartenterminals oder deren
Identitäten wird das gSMC-KT über den Konnektor logisch an das
eHealth-Kartenterminal gebunden. Dieser Vorgang wird als Pairing von
Kartenterminal und gSMC-KT bezeichnet und ist ausführlich in [gemSpec_KT]
beschrieben.

### 4.1.4.6.3 Import der Kartenterminal-Informationen

Im Rahmen des Konnektormanagements müssen die Konfigurationsdaten des
Konnektors ex- und importiert werden können (siehe Kapitel 4.3.3). Eine
Sonderstellung nimmt dabei der Import von Kartenterminalinformationen ein, da
hier im Rahmen des Imports folgende Interaktion mit dem Administrator
erforderlich ist:

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

Es kann notwendig sein, Karten der Generation 2 (G2) näher zu bezeichnen. In
diesem Fall wird in G2.0- und G2.1-Karten unterschieden. Wird von Karten der
Generation 2 gesprochen, so gilt die Festlegung für G2.x (G2.0, G2.1 und
höher) des betrachteten Kartentyps.

Für die TUCs zur PIN-Eingabe, Änderung und Entsperrung sind Festlegungen
hinsichtlich der auf dem Kartenterminal anzuzeigenden Meldungen erforderlich.
Die folgende Tabelle definiert diese Terminalanzeigen gemäß [SICCT#5.5.10.19].

Hinweise zu den Terminalanzeigen bei PIN-Eingaben und zu obiger Tabelle:

 ---> UL

In den Technischen Use Cases TUC_KON_012 „PIN verifizieren“, TUC_KON_019
„PIN ändern“, TUC_KON_021 „PIN entsperren“ wird das
Remote-PIN-Verfahren verwendet, sofern die Zielkarte in einem als für den
Arbeitsplatz entfernt definiertem Kartenterminal steckt (siehe Kap. 4.1.1.1,
Relation [7]). In diesem Fall erfolgt die Nutzerinteraktion am Remote-PIN-KT
von workplaceId (PinInputKT). Dabei wendet der Konnektor das folgende Verfahren
an:

Hinweis: Derzeit schlägt die Freischaltung der SMC-B durch
Card-2-Card-Authentisierung ohne Fehlermeldung fehl. Der Sicherheitszustand der
SMC-B wird nicht verändert. Diese Einschränkung betrifft TUC_KON_005
„Card-to-Card authentisieren“ (TAB_KON_096).

### 4.1.5.2 Durch Ereignisse ausgelöste Reaktionen

### 4.1.5.3 Interne TUCs, nicht durch Fachmodule nutzbar

### 4.1.5.3.1 TUC_KON_001 „Karte öffnen“

### 4.1.5.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.1.5.4.1 TUC_KON_026 „Liefere CardSession“

Hinweis zu TAB_KON_735 - TUC_KON_026: Die WorkplaceId wird als
Eingangsparameter nicht benötigt. Bereits TUC_KON_000 stellt sicher, dass eine
eGK jeweils nur von einem einzigen Arbeitsplatz aus angesprochen werden kann.

### 4.1.5.4.2 TUC_KON_012 „PIN verifizieren“

### 4.1.5.4.3 TUC_KON_019 „PIN ändern“

### 4.1.5.4.4 TUC_KON_021 „PIN entsperren“

### 4.1.5.4.5 TUC_KON_022 „Liefere PIN-Status“

### 4.1.5.4.6 TUC_KON_027 „PIN-Schutz ein-/ausschalten“

### 4.1.5.4.7 TUC_KON_023 „Karte reservieren“

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

### 4.1.5.4.9 TUC_KON_202 „LeseDatei“

### 4.1.5.4.10 TUC_KON_203 „SchreibeDatei“

### 4.1.5.4.11 TUC_KON_204 „LöscheDateiInhalt“

### 4.1.5.4.12 TUC_KON_209 „LeseRecord“

### 4.1.5.4.13 TUC_KON_210 „SchreibeRecord“

### 4.1.5.4.14 TUC_KON_211 „LöscheRecordInhalt“

### 4.1.5.4.15 TUC_KON_214 „FügeHinzuRecord“

### 4.1.5.4.16 TUC_KON_215 „SucheRecord“

### 4.1.5.4.17 TUC_KON_018 „eGK-Sperrung prüfen“

### 4.1.5.4.18 TUC_KON_006 „Datenzugriffsaudit eGK schreiben“

### 4.1.5.4.19 TUC_KON_218 „Signiere“

### 4.1.5.4.20 TUC_KON_219 „Entschlüssele“

### 4.1.5.4.21 TUC_KON_200 „SendeAPDU“

### 4.1.5.4.22 TUC_KON_024 „Karte zurücksetzen“

### 4.1.5.4.23 TUC_KON_216 „LeseZertifikat“

### 4.1.5.4.24 TUC_KON_036 „LiefereFachlicheRolle“

### 4.1.5.5 Operationen an der Außenschnittstelle

### 4.1.5.5.1 VerifyPin

### 4.1.5.5.2 ChangePin

### 4.1.5.5.3 GetPinStatus

### 4.1.5.5.4 UnblockPin

### 4.1.5.5.5 EnablePin

### 4.1.5.5.6 DisablePin

### 4.1.5.6 Betriebsaspekte

### 4.1.5.6.1 TUC_KON_025 "Initialisierung Kartendienst"

### 4.1.5.6.2 Kartenübersicht und PIN-Management

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

Für die Übermittlung der Ereignisse wurde ein leichtgewichtiges Protokoll
gewählt, da vom Clientsystem keine Antwort auf Anwendungsebene erwartet wird.

### 4.1.6.2 Durch Ereignisse ausgelöste Reaktionen

Keine.

### 4.1.6.3 Interne TUCs, nicht durch Fachmodule nutzbar

Keine.

### 4.1.6.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.1.6.4.1 TUC_KON_256 „Systemereignis absetzen“

### 4.1.6.4.2 TUC_KON_252 „Liefere KT_Liste“

### 4.1.6.4.3 TUC_KON_253 „Liefere Karten_Liste“

### 4.1.6.4.4 TUC_KON_254 „Liefere Ressourcendetails“

### 4.1.6.5 Operationen an der Außenschnittstelle

### 4.1.6.5.1 GetCardTerminals

### 4.1.6.5.2 GetCards

### 4.1.6.5.3 GetResourceInformation

### 4.1.6.5.4 Subscribe

### 4.1.6.5.5 Unsubscribe

### 4.1.6.5.6 RenewSubscriptions

### 4.1.6.5.7 GetSubscription

### 4.1.6.6 Betriebsaspekte

### 4.1.7 Verschlüsselungsdienst

Der Verschlüsselungsdienst bietet Schnittstellen zum hybriden und symmetrischen
Ver- und Entschlüsseln von Dokumenten an.

Der Verschlüsselungsdienst bietet für alle Alle_DocFormate die hybride und
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

### 4.1.7.4.2 TUC_KON_071 „Daten hybrid entschlüsseln”

### 4.1.7.4.3 TUC_KON_072 „Daten symmetrisch verschlüsseln”

### 4.1.7.4.4 TUC_KON_073 „Daten symmetrisch entschlüsseln”

### 4.1.7.4.5 TUC_KON_075 „Symmetrisch verschlüsseln“

### 4.1.7.4.6 TUC_KON_076 „Symmetrisch entschlüsseln“

### 4.1.7.5 Operationen an der Außenschnittstelle

### 4.1.7.5.1 EncryptDocument

### 4.1.7.5.2 DecryptDocument

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
Konnektor unterstützt parallele Signaturen (QES und nonQES). Ebenso
unterstützt er Gegensignaturen (QES und nonQES), die jeweils alle bestehenden
Signaturen gegensignieren. Die angebotene Möglichkeit des Gegensignierens
bezieht sich dabei auf das Signieren aller vorhandenen parallelen Signaturen,
während ein Gegensignieren von Gegensignaturen nicht angeboten wird. Der
Konnektor unterstützt ausschließlich eine dokumentexkludierende
Gegensignatur, bei der alle Signaturen gegensigniert werden, aber nicht der
fachliche Inhalt des Dokumentes selbst.

 ---> TABLE

Zu den Begriffen detached, enveloping und enveloped Signaturen siehe
beispielsweise auch [HüKo06#Abs. 4.3.3. und 4.3.1.5].

Durch die Baseline-Profilierung der AdES-BES-Profile wird festgelegt, wie der
Signaturzeitpunkt, gemessen als Systemzeit des Konnektors, in die Signatur
eingebracht wird.

 ---> TABLE

 ---> TABLE

 ---> TABLE

### 4.1.8.1.2 Signaturrichtlinien

Signaturrichtlinien dienen der Profilierung von Signaturerstellung und
-prüfung. Beim Aufruf der Operation SignDocument kann eine URI übergeben
werden, die eine im Konnektor hinterlegte Signaturrichtlinie referenziert. Die
Plattform des Konnektors stellt selbst keine Signaturrichtlinien bereit.
Fachanwendungen, die Signaturrichtlinien erfordern, definieren diese im
Fachmodul des Konnektors. Für XML-Dokumentenformate aus der Menge von
QES_DocFormate können die nachfolgenden Aspekte über eine Signaturrichtlinie
gekapselt festgelegt werden:

 ---> UL

### 4.1.8.1.3 Signaturzeitpunkt

Bezogen auf den vom Konnektor für die Signaturprüfung anzunehmenden
Signaturerstellungszeitpunkt werden in dieser Spezifikation die Bezeichner
Ermittelter_Signaturzeitpunkt und Benutzerdefinierter_Zeitpunkt verwendet.

Ermittelter_Signaturzeitpunkt: Vom Konnektor ermittelter Zeitpunkt, zu dem eine
Signatur geprüft wird. Es werden folgende Signaturzeitpunkte ermittelt:

 ---> OL

Anmerkung: Bei vom Konnektor selbst erstellten Signaturen ist immer ein in der
Signatur eingebetteter Zeitpunkt vorhanden, jedoch kein qualifizierter
Zeitstempel, da in der TI keine qualifizierten Zeitstempel ausgestellt
werden. Sollte ein Dokument mit einem qualifizierten Zeitstempel versehen
sein, so wird dieser nicht für die Ermittlung des Signaturzeitpunktes
herangezogen.

Benutzerdefinierter_Zeitpunkt: Vom Benutzer beim Aufruf der
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
(Komfortsignaturmodus) aktiviert. Dazu muss der HBA-Inhaber die PIN.QES
eingeben.

Der Konnektor merkt sich für die Cardsession des HBA, dass die Komfortsignatur
aktiviert wurde. Bei den folgenden Aufrufen von SignDocumentwerden dann
Komfortsignaturen ausgeführt, solange bis eines der folgenden Abbruchkriterien
eintritt:

·       Die vom HBA (entsprechend Personalisierung) oder die vom
Konnektor (entsprechend Konfiguration SAK_COMFORT_SIGNATURE_MAX) durchgesetzte
maximale Anzahl von Signaturen wurde erreicht.

·       Das konfigurierte Zeitintervall für die Komfortsignatur
(entsprechend Konfiguration SAK_COMFORT_SIGNATURE_TIMER) ist für die
Cardsession abgelaufen.

·       Der Komfortsignaturmodus wurde für die betroffene Cardsession
deaktiviert.

·       Der HBA wurde gezogen.

·       Der Sicherheitszustand des HBA wurde zurückgesetzt.

·       Die Komfortsignaturfunktion wurde für den Konnektor durch den
Administrator deaktiviert.

A_18597 kann z. B. umgesetzt werden, indem

·       ein dedizierter logischer Kanal des HBA für die Komfortsignatur
verwendet wird und

·       im dedizierten logischen Kanal des HBA die Selektion von DF.QES
solange beibehalten wird, bis ein Verlassen von DF.QES durch die Spezifikation
explizit gefordert wird.

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

### 4.1.8.3.2 TUC_KON_165 „Signaturvoraussetzungen für nonQES prüfen“

### 4.1.8.3.3 TUC_KON_166 „nonQES Signaturen erstellen“

### 4.1.8.3.4 TUC_KON_152 "Signaturvoraussetzungen für QES prüfen"

### 4.1.8.3.5 TUC_KON_154 "QES Signaturen erstellen"

Der TUC_KON_154 stellt den Standardsignaturfall in der TI, die Stapelsignatur
dar (auch für Stapel der Größe 1). Da die Stapelsignatur auf der Zielkarte
passende CVC voraussetzt, die auf den HBA-Vorläuferkarten nicht vorhanden
sind, kann dieser TUC nur den HBA unterstützen. Für HBA-Vorläuferkarten kann
TUC_KON_168 verwendet werden.

### 4.1.8.3.6 TUC_KON_168 „Einzelsignatur QES erstellen“

### 4.1.8.3.7 TUC_KON_158 "Komfortsignaturen erstellen"

Der TUC_KON_158 führt die Komfortsignatur für ein Dokument oder mehrere
Dokumente eines Stapels aus. Da die Komfortsignatur auf der Zielkarte passende
CVC voraussetzt, die auf den HBA-Vorläuferkarten nicht vorhanden sind,
unterstützt dieser TUC nur den HBA.

### 4.1.8.4 Interne TUCs, auch durch Fachmodule nutzbar

Die in der obigen Anforderung benannten Signaturen von Dokumentenformaten
umfassen beispielsweise die Signatur von Token nach SAML2 für das Fachmodul
ePA entsprechend [gemSpec_FM_ePA#A_14927].

### 4.1.8.4.1 TUC_KON_160 „Dokumente nonQES signieren”

### 4.1.8.4.2 TUC_KON_161 „nonQES Dokumentsignatur prüfen”

### 4.1.8.4.3 TUC_KON_162 „Kryptographische Prüfung der XML-Dokumentensignatur”

### 4.1.8.4.4 TUC_KON_150 „Dokumente QES signieren”

### 4.1.8.4.5 Anforderungen an die Stapelsignatur

Eine Stapelsignatur definiert sich als „Erstellung einer begrenzten Anzahl
Signaturen nach den zeitlich unmittelbar aufeinander folgenden Prozessen der
Anzeige der zu signierenden Daten und der einmaligen Authentisierung des
Signaturschlüssel-Inhabers gegenüber der qualifizierten elektronischen
Signaturerstellungseinheit“ (siehe [BSI-TR03114]).

### 4.1.8.4.6 TUC_KON_151 „QES Dokumentensignatur prüfen“

### 4.1.8.4.7 TUC_KON_170 „Dokumente mit Komfort signieren”

### 4.1.8.4.8 TUC_KON_171 „Komfortsignatur einschalten”

### 4.1.8.4.9 TUC_KON_172 „Komfortsignatur ausschalten”

### 4.1.8.4.10 TUC_KON_173 „Liefere Signaturmodus”

### 4.1.8.5 Operationen an der Außenschnittstelle

### 4.1.8.5.1 SignDocument (nonQES und QES)

### 4.1.8.5.2 VerifyDocument (nonQES und QES)

### 4.1.8.5.3 StopSignature

### 4.1.8.5.4 GetJobNumber

### 4.1.8.5.5 ActivateComfortSignature

### 4.1.8.5.6 DeactivateComfortSignature

### 4.1.8.5.7 GetSignatureMode

### 4.1.8.6 Betriebsaspekte

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

Bei der Zertifikatsprüfung wird ein übergebenes Zertifikat oder ein Zertifikat
einer referenzierten Karte geprüft. Das konkrete Zertifikatsobjekt einer Karte
ist abhängig vom Kartentyp und dem gewählten kryptographischen Verfahren. Die
folgende Tabelle führt auf, welche Zertifikatsobjekte einer Karte in
Abhängigkeit vom kryptographischen Verfahren für die jeweilige
Zertifikatsreferenz ausgewählt werden.

 ---> TABLE

Dadurch wird gleichzeitig die Spitzenlast bei OCSP-Anfragen begrenzt.

### 4.1.9.2 Durch Ereignisse ausgelöste Reaktionen

Keine.

### 4.1.9.3 Interne TUCs, nicht durch Fachmodule nutzbar

### 4.1.9.3.1 TUC_KON_032 „TSL aktualisieren“

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

Eine erweiterte Übersicht zum Aufbau der detached-Signatur-Datei inkl. Beispiel
finden sie unter [gemGitHub_tslSig].

### 4.1.9.3.2 TUC_KON_031 „BNetzA-VL aktualisieren“

### 4.1.9.3.3 TUC_KON_040 „CRL aktualisieren“

### 4.1.9.3.4 TUC_KON_033 „Zertifikatsablauf prüfen“

### 4.1.9.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.1.9.4.1 TUC_KON_037 „Zertifikat prüfen"

### 4.1.9.4.2 TUC_KON_042 „CV-Zertifikat prüfen“

### 4.1.9.4.3 TUC_KON_034 „Zertifikatsinformationen extrahieren“

### 4.1.9.5 Operationen an der Außenschnittstelle

### 4.1.9.5.1 CheckCertificateExpiration

### 4.1.9.5.2 ReadCardCertificate

### 4.1.9.5.3 VerifyCertificate

### 4.1.9.6 Betriebsaspekte

### 4.1.9.6.1 TUC_KON_035 „Zertifikatsdienst initialisieren“

Der Typ der TSL liefert dem Administrator die Information, ob es sich um eine
TSL handelt, die den TI-Vertrauensraum ausschließlich für Zertifikate mit
kryptographischen Verfahren nach RSA-2048 (TSL(RSA)) oder für Zertifikate mit
kryptographischen Verfahren nach RSA-2048 und ECC-256 (TSL(ECC-RSA))
bereitstellt. Die Information kann aus der Signatur der TSL ermittelt werden.

Auch im Fall des automatischen Imports der TSL muss dies im kritischen
Betriebszustand EC_TSL_Out_Of_Date_Beyond_Grace_Period unterstützt werden.

Für die ECC-Migration ist es notwendig den ECC-RSA-Vertrauensraum zu
etablieren. Dies erfolgt durch das Einspielen eines TSL-Signer-CA
Cross-Zertifikats und das neue TSL-Signer-CA-Zertifikat, wodurch der
ECC-Vertrauensanker im Konnektor im sicheren Datenspeicher gespeichert wird.
Die Prüfung des Cross-Zertifikats erfolgt durch A_17821 - Wechsel des
Vertrauensraumes mittels Cross-Zertifikaten (ECC-Migration). Danach kann die
TSL(ECC-RSA) importiert werden. Das Ergebnis ist ein etablierter
TI-Vertrauensraum für ECC und RSA.  
 Konnektoren müssen den
ECC-Vertrauensraum automatisiert und im Rahmen des Upgrades auf PTV4
etablieren. Manuelle Schritte durch den Administrator sind für den Regelfall
zu vermeiden und sollten nur im Fehlerfall nötig werden. Als Fallback-Lösung
muss das manuelle Verfahren dennoch unterstützt werden.

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

Hinweis:  
 Ereignisse im Protokollierungsdienst adressieren nicht nur zu
protokollierende Events im Sinne des Systeminformationsdienstes sondern alles,
was zu einem Protokolleintrag führen soll (z.B. Fehler, Informationen zu
Ablauf, Debug, Performance).

Innerhalb des Protokollierungsdienstes werden folgende Präfixe für Bezeichner
verwendet:

 ---> UL

### 4.1.10.1 Funktionsmerkmalweite Aspekte

Da sich die Menge an Einträgen nach der Größe der Einsatzumgebung richtet,
ist die Speichergröße nach den in [gemSpec_Perf#3.1.1] beschriebenen
Einsatzumgebungen (LE-Ux, x=1,2,3,4) ausreichend zu wählen.

### 4.1.10.2 Durch Ereignisse ausgelöste Reaktionen

Keine.

### 4.1.10.3 Interne TUCs, nicht durch Fachmodule nutzbar

Keine.

### 4.1.10.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.1.10.4.1 TUC_KON_271 „Schreibe Protokolleintrag“

Die Darstellung PIC_KON_118 veranschaulicht den Aufbau der Protokolle für
Plattform und Fachmodule und die Steuerung der Protokolleinträge in
TUC_KON_271 „Schreibe Protokolleintrag“.

![Abbildung-20][Abbildung-20]

### 4.1.10.5 Operationen an der Außenschnittstelle

Keine

### 4.1.10.6 Betriebsaspekte

### 4.1.10.6.1 TUC_KON_272 „Initialisierung Protokollierungsdienst

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

### 4.1.11.3 Interne TUCs, nicht durch Fachmodule nutzbar

Keine.

### 4.1.11.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.1.11.4.1 TUC_KON_110 „Kartenbasierte TLS-Verbindung aufbauen“

### 4.1.11.4.2 TUC_KON_111 „Kartenbasierte TLS-Verbindung abbauen“

### 4.1.11.5 Operationen an der Außenschnittstelle

Keine.

### 4.1.11.6 Betriebsaspekte

### 4.1.12 LDAP-Proxy

Der Konnektor ermöglicht es Clientsystemen und Fachmodulen durch Nutzung des
LDAP-Proxies Daten aus dem Verzeichnisdienst der TI-Plattform (VZD) abzufragen.
Die Kommunikation erfolgt über das LDAPv3 Protokoll.

Die Funktionalität steht nur zur Verfügung, wenn MGM_LU_ONLINE=Enabled ist
(siehe Kapitel 4.3.6)

### 4.1.12.1 Funktionsmerkmalweite Aspekte

Keine.

### 4.1.12.2 Durch Ereignisse ausgelöste Reaktionen

### 4.1.12.3 Interne TUCs, nicht durch Fachmodule nutzbar

Keine.

### 4.1.12.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.1.12.4.1 TUC_KON_290 „LDAP-Verbindung aufbauen“

### 4.1.12.4.2 TUC_KON_291 „Verzeichnis abfragen“

### 4.1.12.4.3 TUC_KON_292 „LDAP-Verbindung trennen"

### 4.1.12.4.4 TUC_KON_293 „Verzeichnisabfrage abbrechen"

### 4.1.12.5 Operationen an der Außenschnittstelle

### 4.1.12.5.1 Unterstützte LDAPv3 Operationen

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

### 4.1.13.2 Durch Ereignisse ausgelöste Reaktionen

keine

### 4.1.13.3 Interne TUCs

keine

### 4.1.13.4 Operationen an der Außenschnittstelle

### 4.1.13.4.1 ExternalAuthenticate

### 4.1.13.5 Betriebsaspekte

Keine

### 4.1.14 Betriebsdatenmeldedienst

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

In der folgenden Anforderung wird die Terminologie gemäß [RFC2663] verwendet.

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

Umsetzungshinweis für den Hersteller: Es können zwei getrennten
Firewall-Regelsets für den LAN- bzw. für den WAN-Adapter verwendet werden.

### 4.2.1.2 Durch Ereignisse ausgelöste Reaktionen

### 4.2.1.3 Interne TUCs, nicht durch Fachmodule nutzbar

### 4.2.1.3.1 TUC_KON_305 „LAN-Adapter initialisieren“

### 4.2.1.3.2 TUC_KON_306 „WAN-Adapter initialisieren“

### 4.2.1.3.3 TUC_KON_304 „Netzwerk-Routen einrichten“

### 4.2.1.4 Interne TUCs, auch durch Fachmodule nutzbar

Keine.

### 4.2.1.5 Operationen an der Außenschnittstelle

Keine

### 4.2.1.6 Betriebsaspekte

### 4.2.2 DHCP-Server

Innerhalb des Kapitels DHCP-Servers werden folgende Präfixe für Bezeichner
verwendet:

 ---> UL

### 4.2.2.1 Funktionsmerkmalweite Aspekte

### 4.2.2.2 Durch Ereignisse ausgelöste Reaktionen

Keine.

### 4.2.2.3 Interne TUCs, nicht durch Fachmodule nutzbar

Keine.

### 4.2.2.4 Interne TUCs, auch durch Fachmodule nutzbar

Keine.

### 4.2.2.5 Operationen an der Außenschnittstelle

### 4.2.2.5.1 Liefere Netzwerkinformationen über DHCP

### 4.2.2.6 Betriebsaspekte

### 4.2.2.6.1 TUC_KON_343 „Initialisierung DHCP-Server“

### 4.2.3 DHCP-Client

Innerhalb des Kapitels DHCP-Client werden folgende Präfixe für Bezeichner
verwendet:

 ---> UL

### 4.2.3.1 Funktionsmerkmalweite Aspekte

### 4.2.3.2 Durch Ereignisse ausgelöste Reaktionen

### 4.2.3.3 Interne TUCs, nicht durch Fachmodule nutzbar

### 4.2.3.3.1 TUC_KON_341 „DHCP-Informationen beziehen“

### 4.2.3.4 Interne TUCs, auch durch Fachmodule nutzbar

Keine.

### 4.2.3.5 Operationen an der Außenschnittstelle

Keine.

### 4.2.3.6 Betriebsaspekte

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

### 4.2.4.2 Durch Ereignisse ausgelöste Reaktionen

Hinweis: Wenn der IPsec-Tunnel VPN_SIS aufgebaut ist, zeigt die Default Route im
Konnektor auf die innere Tunnel-IP-Adresse des VPN-Konzentrators SIS. Dies ist
bei einer Trennung und dem Wiederaufbau der Verbindung VPN_TI zu beachten.

### 4.2.4.3 Interne TUCs, nicht durch Fachmodule nutzbar

### 4.2.4.3.1 TUC_KON_321 „Verbindung zu dem VPN-Konzentrator der TI aufbauen“

### 4.2.4.3.2 TUC_KON_322 „Verbindung zu dem VPN-Konzentrator des SIS aufbauen“

### 4.2.4.4 Interne TUCs, auch durch Fachmodule nutzbar

Keine

### 4.2.4.5 Operationen an der Außenschnittstelle

Keine

### 4.2.4.6 Betriebsaspekte

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

Falls die Systemzeit des Konnektors zu stark von der Zeit der zentralen
TI-Plattform abweicht, deutet dies auf ein schwerwiegendes Problem im Konnektor
oder der Umgebung hin, da dies im ordnungsgemäßen Betrieb nicht auftreten
sollte.

Der kritische Betriebszustand kann anschließend über einen manuellen Eingriff
(z. B. Reboot) behoben werden (siehe 3.3 Betriebszustand).

### 4.2.5.2 Durch Ereignisse ausgelöste Reaktionen

Keine.

### 4.2.5.3 Interne TUCs, nicht durch Fachmodule nutzbar

Keine.

### 4.2.5.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.2.5.4.1 TUC_KON_351 “Liefere Systemzeit”

### 4.2.5.5 Operationen an der Außenschnittstelle

### 4.2.5.5.1 Sync_Time

### 4.2.5.6 Betriebsaspekte

### 4.2.5.6.1 TUC_KON_352 Initialisierung Zeitdienst

### 4.2.6 Namensdienst und Dienstlokalisierung

Innerhalb des Namensdienstes werden folgende Präfixe für Bezeichner verwendet:

 ---> UL

### 4.2.6.1 Funktionsmerkmalweite Aspekte

### 4.2.6.2 Durch Ereignisse ausgelöste Reaktionen

Keine.

### 4.2.6.3 Interne TUCs, nicht durch Fachmodule nutzbar

Keine.

### 4.2.6.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.2.6.4.1 TUC_KON_361 „DNS-Namen auflösen“

### 4.2.6.4.2 TUC_KON_362 „Liste der Dienste abrufen“

### 4.2.6.4.3 TUC_KON_363 „Dienstdetails abrufen“

### 4.2.6.5 Operationen an der Außenschnittstelle

### 4.2.6.5.1 GetIPAddress

### 4.2.6.6 Betriebsaspekte

### 4.2.7 Optionale Verwendung von IPv6

Der Konnektor kann zusätzlich eine IPv6-Adresse an den Netzwerkschnittstellen
zum Transportnetz implementieren. Entscheidet sich der Hersteller für den
parallelen Einsatz von IPv4 und IPv6 (Dual-Stack-Mode), sind die nachfolgenden
Anforderungen dieses Kapitels umzusetzen. Einhergehend mit der Entscheidung,
IPv6 an diesem Interface zu konfigurieren, ist der spätere VPN-Tunnelaufbau
zur TI und SIS über das IPv6 Interface möglich. Die durch den jeweiligen
IPv6-Tunnel zu transportierenden IP-Pakete sind IPv4 adressierte Pakete.

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

Die über die Managementschnittstelle zu erreichenden und zu verändernden
Inhalte werden erhoben in:

 ---> UL

Eine Ergänzung um weitere, herstellerspezifische Konfigurationsinhalte ist
möglich.

### 4.3.1 Zugang und Benutzerverwaltung des Konnektormanagements

Der Konnektor verfügt über keine Verwaltung der fachlichen Nutzer, wohl aber
über eine Verwaltung der Nutzer, die in der Rolle eines Administrators den
Konnektor konfigurieren und die Protokolle einsehen dürfen. Dabei werden drei
Administrator-Rollen unterschieden:

 ---> OL

Näheres hierzu regeln die Schutzprofile des Konnektors.

### 4.3.2 Konnektorname und Versionsinformationen

Fachmodulversionsinformationen sind nicht Bestandteil der Selbstauskunft gemäß
ProductInformation.xsd.

### 4.3.3 Konfigurationsdaten: Persistieren sowie Export-Import

Nähere Vorgaben zum Ablauf des Imports der Kartenterminalinformationen finden
sich im Kapitel 4.1.4.6.3.

### 4.3.4 Administration von Fachmodulen

Die Konfiguration von Fachmodulen ist innerhalb der Managementschnittstelle des
Konnektors von der Konfiguration der Plattformanteile des Konnektors logisch
entkoppelt. Die Festlegungen, welche Konfigurationsparameter und welche
zusätzlichen administrativen Funktionen für ein Fachmodul benötigt werden,
werden in den jeweiligen Fachmodulspezifikationen getroffen. Der Konnektor muss
aber für jedes Fachmodul hinsichtlich der Administrierbarkeit des Fachmoduls
die folgende Basisfunktionalität zur Verfügung stellen:

### 4.3.5 Neustart und Werksreset

### 4.3.6 Leistungsumfänge und Standalone-Szenarios

Obgleich der Konnektor in seinem Auslieferungszustand alle Leistungsmerkmale
aufweisen muss, die gemäß Produkttypssteckbrief gefordert werden, so soll es
dem Administrator doch ermöglicht werden grundsätzliche Leistungsumfänge
gezielt deaktivieren zu können, um den Konnektor so besser in die
organisatorische/technische Struktur der Betriebsstätte eingliedern zu können.

Der Konfigurationsparameter MGM_LU_SAK wirkt hauptsächlich in dem
Funktionsmerkmal „Signaturdienst“ (siehe Kapitel 4.1.8).

Ist MGM_LU_ONLINE Disabled, so baut der Konnektor grundsätzlich keine
Online-Verbindungen auf (weder zur TI, noch zum SIS). Der Parameter wirkt
hauptsächlich in den Funktionsmerkmalen:

 ---> UL

Ob es sich bei einem Konnektor um den losgelöst (stand alone) vom Netz der
Einsatzumgebung betriebenen handelt, also einen Konnektor, auf welchen kein
Clientsystem zugreift, muss diesem mitgeteilt werden:

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

Die Berechtigung zur Einwahl in die TI ist von der Gültigkeit der beiden bei
der Freischaltung übermittelten Zertifikate abhängig (C.NK.VPN und
C.HCI.OSIG). Die Berechtigung zur Einwahl in die TI wird verweigert, bzw. eine
bestehende Verbindung zur TI wird beendet, wenn ein Zertifikat abgelaufen oder
gesperrt ist. Aus diesem Grund muss der Administrator vor Ablauf eines der
beiden Zertifikate eine wiederholte Registrierung mit neuem
Netzkonnektorzertifikat bzw. neuer SM-B beim ZGDP durchführen. (Hinweis: neue
NK-Zertifikate werden erst mit Etablierung der Nachladefunktionalität für
gSMC-K verfügbar sein.)

Soll ein Konnektor außer Betrieb genommen werden oder wird der Vertrag mit
einem ZGDP gekündigt, muss der Administrator den Konnektor über den
Registrierungsdienst des ZGDP abmelden.

Möchte ein Konnektoreigentümer das Gerät weiterveräußern oder vollständig
außer Betrieb nehmen, so sollte er eine vorhandene Freischaltung zuvor
rückgängig machen.

Es können separate Konfigurationsschalter für einzelne TLS-Strecken umgesetzt
werden.

Es gelten darüber hinaus:

 ---> UL

### 4.3.8 Re-Registrierung des Konnektors mit weiterem NK-Zertifikat

Eine Re-Registrierung eines Konnektors am VPN-Zugangsdienst mit einem neuen
NK-Zertifikat wird im Rahmen der ECC-Migration der IPsec-Kommunikation zum
VPN-Zugangsdienst mit einem ECC-Zertifikat notwendig

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

Das Remote-Management-System authentisiert sich auf Transportebene
zertifikatsbasiert gegenüber dem Konnektor.

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

 ---> TABLE

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
Kartenterminals (CT-Objects in CTM_CT_LIST mit CT.CORRELATION›=„gepairt“
und CT.VALID_VERSION=True und CT.IS_PHYSICAL = Ja) softwareseitig aktualisieren
kann.

Weiterhin muss über den KSR-Client eine Aktualisierung von ausgewählten
Konfigurationsdaten möglich sein.

### 4.3.10.2 Durch Ereignisse ausgelöste Reaktionen

### 4.3.10.3 Interne TUCs, nicht durch Fachmodule nutzbar

### 4.3.10.3.1 TUC_KON_280 „Konnektoraktualisierung durchführen“

### 4.3.10.3.2 TUC_KON_281 „Kartenterminalaktualisierung anstoßen“

Im Vergleich zur Durchführung des Konnektor-Update (TUC_KON_280), werden die
Updates der Kartenterminals nur durch den Konnektor initiiert. Der Konnektor
liefert dem Kartenterminal das Updatefile, der eigentliche Updatevorgang
(inklusive der Prüfung des Updatepakets auf Integrität und Authentizität)
erfolgt ausschließlich und eigenverantwortlich auf Seiten des Kartenterminals.

### 4.3.10.3.3 TUC_KON_282 „UpdateInformationen beziehen“

### 4.3.10.3.4 TUC_KON_283 „Infrastruktur Konfiguration aktualisieren“

### 4.3.10.4 Interne TUCs, auch durch Fachmodule nutzbar

### 4.3.10.4.1 TUC_KON_285 „UpdateInformationen für Fachmodul beziehen“

### 4.3.10.4.2 TUC_KON_286 „Paket für Fachmodul laden“

### 4.3.10.5 Operationen an der Außenschnittstelle

Keine.

### 4.3.10.6 Betriebsaspekte

### 4.3.10.6.1 TUC_KON_284 KSR-Client initialisieren

Hinweis: Die Adressen des Konfigurationsdienstes werden im Rahmen des
VPN-Verbindungsaufbaus ermittelt (siehe [gemSpec_VPN_ZugD#5.1.1.2
TUC_VPN-ZD_0001])

### 4.3.11 Konnektorstatus

### 4.4 Hardware-Merkmale des Konnektors

Diese Anforderung verlangt keinen Schutz gegen Stromausfall in den
Betriebsräumen.

Die Prüfung auf Einhaltung der Versiegelungsvorgaben erfolgt nicht im Rahmen
der CC-Evaluierung, sondern im Zuge der Prüfung auf funktionale Eignung.

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

‹ReturnVerificationReport

xmlns="urn:oasis:names:tc:dss-x:1.0:profiles:verificationreport:schema#"
xmlns:xsi=http://www.w3.org/2001/XMLSchema-instance

xsi:schemaLocation="urn:oasis:names:tc:dss-x:1.0:profiles:verificationreport:schema#

oasis-dssx-1.0-profiles-vr-cd1.xsd"›

‹IncludeVerifier›false‹/IncludeVerifier›

‹IncludeCertificateValues›true‹/IncludeCertificateValues›

‹IncludeRevocationValues›true‹/IncludeRevocationValues›

‹ExpandBinaryValues›false‹/ExpandBinaryValues›  

‹ReportDetailLevel›

urn:oasis:names:tc:dss-x:1.0:profiles:verificationreport:reportdetail:allDetails

‹/ReportDetailLevel›

‹/ReturnVerificationReport›

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

/VerificationReport/  
     IndividualReport/  
   
        Details/  
             dss:VerificationTimeInfo/ 

                 dss:VerificationTime

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

                        Other/  

                            SIG:ShortText

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
zeigt  IdRef auf den jeweiligen gegensignierten Signaturwert  
   

/VerificationReport/

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

./ResultMessage=“Algorithmen seit ‹Jahr› als unsicher eingestuft“

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


[//]: # --------------------------------------------------------- (not rendered)

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
[4.1.8.5.1]:             #41851-signdocument-(nonqes-und-qes)
[4.1.8.5.2]:             #41852-verifydocument-(nonqes-und-qes)
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
[4.3.9]:                 #439-remote-management-(optional)
[4.3.10]:                #4310-software--und-konfigurationsaktualisierung-(ksr-client)
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
[6]:                     #6-anhang-b-–-profilierung-der-signatur--und-verschlüsselungsformate-(normativ)
[6.1]:                   #61-profilierung-der-verschlüsselungsformate
[6.2]:                   #62-profilierung-der-signaturformate
[6.3]:                   #63-profilierung-verificationreport
[6.4]:                   #64-profilierung-der-dokumentenformate-und-nachrichten
[7]:                     #7-anhang-f-–-übersicht-events
[8]:                     #8-anhang-h-–-mapping-von-architektur-der-ti-plattform-auf-konnektorspezifikation
[9]:                     #9-anhang-i-–-umsetzungshinweise-(informativ)
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
[Tbl-001]:               #Tbl-001 (&93836995980344)
[Tbl-002]:               #Tbl-002 (&93836986721640)
[Tbl-003]:               #Tbl-003 (&93836986762896)
[Tabelle-1]:             #Tabelle-1 (&93836986837336)
[Tabelle-2]:             #Tabelle-2 (&93836986849656)
[Tabelle-3]:             #Tabelle-3 (&93836986867720)
[Tabelle-4]:             #Tabelle-4 (&93836996698600)
[Tabelle-5]:             #Tabelle-5 (&93836996862400)
[Tabelle-6]:             #Tabelle-6 (&93836997485376)
[Tabelle-7]:             #Tabelle-7 (&93836988322848)
[Tbl-011]:               #Tbl-011 (&93836988342696)
[Tabelle-9]:             #Tabelle-9 (&93836988400152)
[Tabelle-10]:            #Tabelle-10 (&93836988567120)
[Tabelle-11]:            #Tabelle-11 (&93836988626464)
[Tabelle-12]:            #Tabelle-12 (&93836988824096)
[Tabelle-13]:            #Tabelle-13 (&93836988970136)
[Tabelle-14]:            #Tabelle-14 (&93836996324920)
[Tabelle-15]:            #Tabelle-15 (&93836996374224)
[Tabelle-16]:            #Tabelle-16 (&93836990377888)
[Tabelle-17]:            #Tabelle-17 (&93836990577000)
[Tabelle-18]:            #Tabelle-18 (&93836990652560)
[Tabelle-19]:            #Tabelle-19 (&93836991068568)
[Tabelle-20]:            #Tabelle-20 (&93836991754400)
[Tabelle-21]:            #Tabelle-21 (&93836992198624)
[Tabelle-22]:            #Tabelle-22 (&93836992393176)
[Tabelle-23]:            #Tabelle-23 (&93836992481072)
[Tabelle-24]:            #Tabelle-24 (&93836992537296)
[Tbl-028]:               #Tbl-028 (&93836992611224)
[Tabelle-26]:            #Tabelle-26 (&93836992839296)
[Tabelle-27]:            #Tabelle-27 (&93836992891744)
[Tabelle-28]:            #Tabelle-28 (&93836992982720)
[Tbl-032]:               #Tbl-032 (&93836993002032)
[Tabelle-30]:            #Tabelle-30 (&93836993254112)
[Tabelle-31]:            #Tabelle-31 (&93836994069384)
[Tabelle-32]:            #Tabelle-32 (&93836994095624)
[Tabelle-33]:            #Tabelle-33 (&93836994231168)
[Tabelle-34]:            #Tabelle-34 (&93836994444152)
[Tabelle-35]:            #Tabelle-35 (&93836995245296)
[Tabelle-36]:            #Tabelle-36 (&93836995335216)
[Tabelle-37]:            #Tabelle-37 (&93836995370464)
[Tabelle-38]:            #Tabelle-38 (&93836995539992)
[Tabelle-39]:            #Tabelle-39 (&93836995576432)
[Tabelle-40]:            #Tabelle-40 (&93836995653904)
[Tabelle-41]:            #Tabelle-41 (&93836995746232)
[Tabelle-42]:            #Tabelle-42 (&93836995765632)
[Tabelle-43]:            #Tabelle-43 (&93836998716088)
[Tabelle-44]:            #Tabelle-44 (&93836998823208)
[Tabelle-45]:            #Tabelle-45 (&93836998897336)
[Tabelle-46]:            #Tabelle-46 (&93836998955128)
[Tabelle-47]:            #Tabelle-47 (&93836999062872)
[Tabelle-48]:            #Tabelle-48 (&93836999082488)
[Tabelle-49]:            #Tabelle-49 (&93836999117648)
[Tabelle-50]:            #Tabelle-50 (&93836999176264)
[Tabelle-51]:            #Tabelle-51 (&93836999210416)
[Tabelle-52]:            #Tabelle-52 (&93836999284096)
[Tabelle-53]:            #Tabelle-53 (&93836999334672)
[Tabelle-54]:            #Tabelle-54 (&93836999371480)
[Tabelle-55]:            #Tabelle-55 (&93836999409096)
[Tabelle-56]:            #Tabelle-56 (&93836999463040)
[Tabelle-57]:            #Tabelle-57 (&93836999536736)
[Tabelle-58]:            #Tabelle-58 (&93836999641480)
[Tabelle-59]:            #Tabelle-59 (&93836999775336)
[Tabelle-60]:            #Tabelle-60 (&93837000259224)
[Tabelle-61]:            #Tabelle-61 (&93837000759984)
[Tabelle-62]:            #Tabelle-62 (&93837000829744)
[Tabelle-63]:            #Tabelle-63 (&93837000886408)
[Tabelle-64]:            #Tabelle-64 (&93837000905432)
[Tabelle-65]:            #Tabelle-65 (&93837001075376)
[Tabelle-66]:            #Tabelle-66 (&93837001900136)
[Tabelle-67]:            #Tabelle-67 (&93837002032688)
[Tabelle-68]:            #Tabelle-68 (&93837002167288)
[Tabelle-69]:            #Tabelle-69 (&93837002307584)
[Tabelle-70]:            #Tabelle-70 (&93837002435760)
[Tabelle-71]:            #Tabelle-71 (&93837002495672)
[Tabelle-72]:            #Tabelle-72 (&93837002519928)
[Tabelle-73]:            #Tabelle-73 (&93837002711824)
[Tabelle-74]:            #Tabelle-74 (&93837002729400)
[Tabelle-75]:            #Tabelle-75 (&93837002777336)
[Tabelle-76]:            #Tabelle-76 (&93837002841600)
[Tabelle-77]:            #Tabelle-77 (&93837002872528)
[Tabelle-78]:            #Tabelle-78 (&93837003012480)
[Tabelle-79]:            #Tabelle-79 (&93837003027480)
[Tabelle-80]:            #Tabelle-80 (&93837003106976)
[Tabelle-81]:            #Tabelle-81 (&93837003164648)
[Tabelle-82]:            #Tabelle-82 (&93837003285264)
[Tabelle-83]:            #Tabelle-83 (&93837003321232)
[Tabelle-84]:            #Tabelle-84 (&93837003402312)
[Tabelle-85]:            #Tabelle-85 (&93837003454536)
[Tabelle-86]:            #Tabelle-86 (&93837003574344)
[Tabelle-87]:            #Tabelle-87 (&93837003626864)
[Tabelle-88]:            #Tabelle-88 (&93837003696888)
[Tabelle-89]:            #Tabelle-89 (&93837003743960)
[Tabelle-90]:            #Tabelle-90 (&93837003863872)
[Tabelle-91]:            #Tabelle-91 (&93837003910704)
[Tabelle-92]:            #Tabelle-92 (&93837003982616)
[Tabelle-93]:            #Tabelle-93 (&93837004034480)
[Tabelle-94]:            #Tabelle-94 (&93837004153832)
[Tabelle-95]:            #Tabelle-95 (&93837004194672)
[Tabelle-96]:            #Tabelle-96 (&93837004267336)
[Tabelle-97]:            #Tabelle-97 (&93837004308976)
[Tabelle-98]:            #Tabelle-98 (&93837004426968)
[Tabelle-99]:            #Tabelle-99 (&93837004446744)
[Tabelle-100]:           #Tabelle-100 (&93837004508920)
[Tabelle-101]:           #Tabelle-101 (&93837004533632)
[Tabelle-102]:           #Tabelle-102 (&93837004598832)
[Tabelle-103]:           #Tabelle-103 (&93837005005352)
[Tabelle-104]:           #Tabelle-104 (&93837005077776)
[Tabelle-105]:           #Tabelle-105 (&93837005118840)
[Tabelle-106]:           #Tabelle-106 (&93837005185792)
[Tabelle-107]:           #Tabelle-107 (&93837005265312)
[Tabelle-108]:           #Tabelle-108 (&93837005326440)
[Tabelle-109]:           #Tabelle-109 (&93837005351312)
[Tabelle-110]:           #Tabelle-110 (&93837005406928)
[Tabelle-111]:           #Tabelle-111 (&93837005432024)
[Tabelle-112]:           #Tabelle-112 (&93837005550912)
[Tabelle-113]:           #Tabelle-113 (&93837005581656)
[Tabelle-114]:           #Tabelle-114 (&93837005631224)
[Tabelle-115]:           #Tabelle-115 (&93837005761976)
[Tabelle-116]:           #Tabelle-116 (&93837005814120)
[Tabelle-117]:           #Tabelle-117 (&93837005844336)
[Tabelle-118]:           #Tabelle-118 (&93837006076512)
[Tabelle-119]:           #Tabelle-119 (&93837006122944)
[Tabelle-120]:           #Tabelle-120 (&93837006154024)
[Tabelle-121]:           #Tabelle-121 (&93837006399232)
[Tabelle-122]:           #Tabelle-122 (&93837006440096)
[Tabelle-123]:           #Tabelle-123 (&93837006476744)
[Tabelle-124]:           #Tabelle-124 (&93837006605488)
[Tabelle-125]:           #Tabelle-125 (&93837006653280)
[Tabelle-126]:           #Tabelle-126 (&93837006677992)
[Tabelle-127]:           #Tabelle-127 (&93837006805320)
[Tabelle-128]:           #Tabelle-128 (&93837006854232)
[Tabelle-129]:           #Tabelle-129 (&93837006885024)
[Tabelle-130]:           #Tabelle-130 (&93837006962192)
[Tabelle-131]:           #Tabelle-131 (&93837007061456)
[Tabelle-132]:           #Tabelle-132 (&93837007092624)
[Tabelle-133]:           #Tabelle-133 (&93837007108176)
[Tbl-137]:               #Tbl-137 (&93837007206736)
[Tabelle-135]:           #Tabelle-135 (&93837007531440)
[Tabelle-136]:           #Tabelle-136 (&93837008414128)
[Tabelle-137]:           #Tabelle-137 (&93837008433208)
[Tabelle-138]:           #Tabelle-138 (&93837008497416)
[Tabelle-139]:           #Tabelle-139 (&93837008575248)
[Tabelle-140]:           #Tabelle-140 (&93837008595120)
[Tabelle-141]:           #Tabelle-141 (&93837008727560)
[Tabelle-142]:           #Tabelle-142 (&93837008768904)
[Tbl-146]:               #Tbl-146 (&93837008821240)
[Tbl-147]:               #Tbl-147 (&93837008951584)
[Tbl-148]:               #Tbl-148 (&93837008993104)
[Tabelle-146]:           #Tabelle-146 (&93837009011352)
[Tabelle-147]:           #Tabelle-147 (&93837009222216)
[Tabelle-148]:           #Tabelle-148 (&93837009314960)
[Tabelle-149]:           #Tabelle-149 (&93837009333864)
[Tabelle-150]:           #Tabelle-150 (&93837009504264)
[Tabelle-151]:           #Tabelle-151 (&93837009556672)
[Tbl-155]:               #Tbl-155 (&93837009578176)
[Tbl-156]:               #Tbl-156 (&93837009651920)
[Tbl-157]:               #Tbl-157 (&93837009747976)
[Tbl-158]:               #Tbl-158 (&93837009768592)
[Tbl-159]:               #Tbl-159 (&93837009821432)
[Tbl-160]:               #Tbl-160 (&93837010179560)
[Tbl-161]:               #Tbl-161 (&93837010205192)
[Tbl-162]:               #Tbl-162 (&93837010312472)
[Tbl-163]:               #Tbl-163 (&93837010356304)
[Tbl-164]:               #Tbl-164 (&93837010381936)
[Tbl-165]:               #Tbl-165 (&93837010503528)
[Tbl-166]:               #Tbl-166 (&93837010539736)
[Tbl-167]:               #Tbl-167 (&93837010567200)
[Tbl-168]:               #Tbl-168 (&93837010606616)
[Tabelle-166]:           #Tabelle-166 (&93837010633920)
[Tabelle-167]:           #Tabelle-167 (&93837010777352)
[Tabelle-168]:           #Tabelle-168 (&93837010800632)
[Tabelle-169]:           #Tabelle-169 (&93837010936208)
[Tabelle-170]:           #Tabelle-170 (&93837011074808)
[Tabelle-171]:           #Tabelle-171 (&93837011119352)
[Tabelle-172]:           #Tabelle-172 (&93837011185808)
[Tabelle-173]:           #Tabelle-173 (&93837011954632)
[Tabelle-174]:           #Tabelle-174 (&93837012010616)
[Tabelle-175]:           #Tabelle-175 (&93837012030096)
[Tabelle-176]:           #Tabelle-176 (&93837012076976)
[Tabelle-177]:           #Tabelle-177 (&93837012096200)
[Tabelle-178]:           #Tabelle-178 (&93837012204616)
[Tabelle-179]:           #Tabelle-179 (&93837012259368)
[Tabelle-180]:           #Tabelle-180 (&93837012293336)
[Tabelle-181]:           #Tabelle-181 (&93837012473200)
[Tabelle-182]:           #Tabelle-182 (&93837012509152)
[Tabelle-183]:           #Tabelle-183 (&93837012592888)
[Tabelle-184]:           #Tabelle-184 (&93837012659472)
[Tabelle-185]:           #Tabelle-185 (&93837012690912)
[Tabelle-186]:           #Tabelle-186 (&93837012785776)
[Tabelle-187]:           #Tabelle-187 (&93837012836032)
[Tabelle-188]:           #Tabelle-188 (&93837012983736)
[Tabelle-189]:           #Tabelle-189 (&93837013076976)
[Tbl-193]:               #Tbl-193 (&93837013108616)
[Tabelle-191]:           #Tabelle-191 (&93837013204664)
[Tabelle-192]:           #Tabelle-192 (&93837013223224)
[Tabelle-193]:           #Tabelle-193 (&93837013422224)
[Tabelle-194]:           #Tabelle-194 (&93837014168360)
[Tabelle-195]:           #Tabelle-195 (&93837014186112)
[Tabelle-196]:           #Tabelle-196 (&93837014248832)
[Tabelle-197]:           #Tabelle-197 (&93837014262256)
[Tabelle-198]:           #Tabelle-198 (&93837014369960)
[Tabelle-199]:           #Tabelle-199 (&93837014389216)
[Tabelle-200]:           #Tabelle-200 (&93837014447248)
[Tabelle-201]:           #Tabelle-201 (&93837014461936)
[Tabelle-202]:           #Tabelle-202 (&93837014533144)
[Tabelle-203]:           #Tabelle-203 (&93837015088744)
[Tabelle-204]:           #Tabelle-204 (&93837015143384)
[Tabelle-205]:           #Tabelle-205 (&93837015163376)
[Tabelle-206]:           #Tabelle-206 (&93837015246952)
[Tabelle-207]:           #Tabelle-207 (&93837015276200)
[Tabelle-208]:           #Tabelle-208 (&93837015395128)
[Tabelle-209]:           #Tabelle-209 (&93837015425472)
[Tabelle-210]:           #Tabelle-210 (&93837015498448)
[Tabelle-211]:           #Tabelle-211 (&93837015530328)
[Tabelle-212]:           #Tabelle-212 (&93837016059000)
[Tabelle-213]:           #Tabelle-213 (&93837016102272)
[Tabelle-214]:           #Tabelle-214 (&93837016156672)
[Tabelle-215]:           #Tabelle-215 (&93837016190976)
[Tabelle-216]:           #Tabelle-216 (&93837016298176)
[Tabelle-217]:           #Tabelle-217 (&93837016317744)
[Tabelle-218]:           #Tabelle-218 (&93837016418024)
[Tabelle-219]:           #Tabelle-219 (&93837017110912)
[Tabelle-220]:           #Tabelle-220 (&93837017170680)
[Tabelle-221]:           #Tabelle-221 (&93837017291840)
[Tabelle-222]:           #Tabelle-222 (&93837017388400)
[Tabelle-223]:           #Tabelle-223 (&93837017447408)
[Tabelle-224]:           #Tabelle-224 (&93837017551224)
[Tabelle-225]:           #Tabelle-225 (&93837017654456)
[Tabelle-226]:           #Tabelle-226 (&93837017718752)
[Tabelle-227]:           #Tabelle-227 (&93837017764560)
[Tabelle-228]:           #Tabelle-228 (&93837017840112)
[Tabelle-229]:           #Tabelle-229 (&93837017923968)
[Tabelle-230]:           #Tabelle-230 (&93837017987672)
[Tabelle-231]:           #Tabelle-231 (&93837018003800)
[Tabelle-232]:           #Tabelle-232 (&93837018053600)
[Tabelle-233]:           #Tabelle-233 (&93837018407232)
[Tabelle-234]:           #Tabelle-234 (&93837018449584)
[Tabelle-235]:           #Tabelle-235 (&93837018548032)
[Tabelle-236]:           #Tabelle-236 (&93837018776880)
[Tabelle-237]:           #Tabelle-237 (&93837018868152)
[Tabelle-238]:           #Tabelle-238 (&93837018900968)
[Tabelle-239]:           #Tabelle-239 (&93837018935400)
[Tabelle-240]:           #Tabelle-240 (&93837018950616)
[Tabelle-241]:           #Tabelle-241 (&93837018974664)
[Tabelle-242]:           #Tabelle-242 (&93837019058488)
[Tabelle-243]:           #Tabelle-243 (&93837019075576)
[Tabelle-244]:           #Tabelle-244 (&93837019095752)
[Tabelle-245]:           #Tabelle-245 (&93837019135624)
[Tabelle-246]:           #Tabelle-246 (&93837019168080)
[Tabelle-247]:           #Tabelle-247 (&93837019197568)
[Tabelle-248]:           #Tabelle-248 (&93837019285056)
[Tabelle-249]:           #Tabelle-249 (&93837019303128)
[Tabelle-250]:           #Tabelle-250 (&93837019323112)
[Tabelle-251]:           #Tabelle-251 (&93837019384544)
[Tabelle-252]:           #Tabelle-252 (&93837019415336)
[Tabelle-253]:           #Tabelle-253 (&93837019482408)
[Tabelle-254]:           #Tabelle-254 (&93837019525120)
[Tabelle-255]:           #Tabelle-255 (&93837019583072)
[Tabelle-256]:           #Tabelle-256 (&93837019685872)
[Tbl-260]:               #Tbl-260 (&93837019757528)
[Tabelle-258]:           #Tabelle-258 (&93837019808208)
[Tabelle-259]:           #Tabelle-259 (&93837019830272)
[Tabelle-260]:           #Tabelle-260 (&93837019908312)
[Tabelle-261]:           #Tabelle-261 (&93837019962568)
[Tabelle-262]:           #Tabelle-262 (&93837020073928)
[Tabelle-263]:           #Tabelle-263 (&93837020098688)
[Tabelle-264]:           #Tabelle-264 (&93837020495592)
[Tabelle-265]:           #Tabelle-265 (&93837020513600)
[Tabelle-266]:           #Tabelle-266 (&93837020614384)
[Tabelle-267]:           #Tabelle-267 (&93837020694248)
[Tabelle-268]:           #Tabelle-268 (&93837020807048)
[Tabelle-269]:           #Tabelle-269 (&93837020830392)
[Tabelle-270]:           #Tabelle-270 (&93837020947432)
[Tabelle-271]:           #Tabelle-271 (&93837020970256)
[Tabelle-272]:           #Tabelle-272 (&93837021050704)
[Tabelle-273]:           #Tabelle-273 (&93837021086592)
[Tabelle-274]:           #Tabelle-274 (&93837021126848)
[Tabelle-275]:           #Tabelle-275 (&93837021219392)
[Tabelle-276]:           #Tabelle-276 (&93837021262080)
[Tabelle-277]:           #Tabelle-277 (&93837021291544)
[Tabelle-278]:           #Tabelle-278 (&93837021473088)
[Tabelle-279]:           #Tabelle-279 (&93837021514776)
[Tbl-283]:               #Tbl-283 (&93837021551384)
[Tbl-284]:               #Tbl-284 (&93837021656928)
[Tbl-285]:               #Tbl-285 (&93837021729584)
[Tabelle-283]:           #Tabelle-283 (&93837021748584)
[Tabelle-284]:           #Tabelle-284 (&93837021854992)
[Tabelle-285]:           #Tabelle-285 (&93837021868120)
[Tabelle-286]:           #Tabelle-286 (&93837021927744)
[Tabelle-287]:           #Tabelle-287 (&93837021998904)
[Tabelle-288]:           #Tabelle-288 (&93837022120744)
[Tabelle-289]:           #Tabelle-289 (&93837022210440)
[Tabelle-290]:           #Tabelle-290 (&93837022685272)
[Tabelle-291]:           #Tabelle-291 (&93837022734144)
[Tabelle-292]:           #Tabelle-292 (&93837022794016)
[Tabelle-293]:           #Tabelle-293 (&93837022844712)
[Tabelle-294]:           #Tabelle-294 (&93837022966352)
[Tabelle-295]:           #Tabelle-295 (&93837022994400)
[Tabelle-296]:           #Tabelle-296 (&93837023041752)
[Tabelle-297]:           #Tabelle-297 (&93837023078680)
[Tabelle-298]:           #Tabelle-298 (&93837023123328)
[Tabelle-299]:           #Tabelle-299 (&93837023173680)
[Tabelle-300]:           #Tabelle-300 (&93837023275944)
[Tabelle-301]:           #Tabelle-301 (&93837023339864)
[Tabelle-302]:           #Tabelle-302 (&93837023369640)
[Tabelle-303]:           #Tabelle-303 (&93837023403248)
[Tabelle-304]:           #Tabelle-304 (&93837023570008)
[Tabelle-305]:           #Tabelle-305 (&93837023603848)
[Tabelle-306]:           #Tabelle-306 (&93837023625232)
[Tabelle-307]:           #Tabelle-307 (&93837023751168)
[Tabelle-308]:           #Tabelle-308 (&93837023803432)
[Tabelle-309]:           #Tabelle-309 (&93837023815696)
[Tabelle-310]:           #Tabelle-310 (&93837024301752)
[Tabelle-311]:           #Tabelle-311 (&93837024359816)
[Tabelle-312]:           #Tabelle-312 (&93837024384224)
[Tabelle-313]:           #Tabelle-313 (&93837024481344)
[Tabelle-314]:           #Tabelle-314 (&93837024505752)
[Tabelle-315]:           #Tabelle-315 (&93837024602448)
[Tabelle-316]:           #Tabelle-316 (&93837024641840)
[Tabelle-317]:           #Tabelle-317 (&93837024672128)
[Tabelle-318]:           #Tabelle-318 (&93837024695336)
[Tabelle-319]:           #Tabelle-319 (&93837024778168)
[Tabelle-320]:           #Tabelle-320 (&93837024798792)
[Tabelle-321]:           #Tabelle-321 (&93837024914648)
[Tabelle-322]:           #Tabelle-322 (&93837024941896)
[Tbl-326]:               #Tbl-326 (&93837025020544)
[Tabelle-324]:           #Tabelle-324 (&93837025085024)
[Tabelle-325]:           #Tabelle-325 (&93837025442608)
[Tabelle-326]:           #Tabelle-326 (&93837025525152)
[Tabelle-327]:           #Tabelle-327 (&93837025571032)
[Tabelle-328]:           #Tabelle-328 (&93837025607336)
[Tabelle-329]:           #Tabelle-329 (&93837025711488)
[Tabelle-330]:           #Tabelle-330 (&93837025738984)
[Tabelle-331]:           #Tabelle-331 (&93837025804472)
[Tabelle-332]:           #Tabelle-332 (&93837025867832)
[Tabelle-333]:           #Tabelle-333 (&93837025904160)
[Tabelle-334]:           #Tabelle-334 (&93837026015032)
[Tabelle-335]:           #Tabelle-335 (&93837026059944)
[Tabelle-336]:           #Tabelle-336 (&93837026151920)
[Tabelle-337]:           #Tabelle-337 (&93837026179888)
[Tabelle-338]:           #Tabelle-338 (&93837026273568)
[Tabelle-339]:           #Tabelle-339 (&93837026291816)
[Tabelle-340]:           #Tabelle-340 (&93837026325704)
[Tabelle-341]:           #Tabelle-341 (&93837026342200)
[Tabelle-342]:           #Tabelle-342 (&93837026361752)
[Tabelle-343]:           #Tabelle-343 (&93837026420248)
[Tabelle-344]:           #Tabelle-344 (&93837026449224)
[Tabelle-345]:           #Tabelle-345 (&93837026556264)
[Tabelle-346]:           #Tabelle-346 (&93837026597424)
[Tabelle-347]:           #Tabelle-347 (&93837026620464)
[Tabelle-348]:           #Tabelle-348 (&93837026667504)
[Tabelle-349]:           #Tabelle-349 (&93837026692048)
[Tabelle-350]:           #Tabelle-350 (&93837026736384)
[Tabelle-351]:           #Tabelle-351 (&93837026811064)
[Tabelle-352]:           #Tabelle-352 (&93837026861576)
[Tabelle-353]:           #Tabelle-353 (&93837026887552)
[Tabelle-354]:           #Tabelle-354 (&93837026919904)
[Tabelle-355]:           #Tabelle-355 (&93837026957952)
[Tabelle-356]:           #Tabelle-356 (&93837027045440)
[Tabelle-357]:           #Tabelle-357 (&93837027155080)
[Tabelle-358]:           #Tabelle-358 (&93837027179432)
[Tabelle-359]:           #Tabelle-359 (&93837027194552)
[Tabelle-360]:           #Tabelle-360 (&93837027333840)
[Tabelle-361]:           #Tabelle-361 (&93837027368352)
[Tbl-365]:               #Tbl-365 (&93837027401432)
[Tbl-366]:               #Tbl-366 (&93837027427016)
[Tbl-367]:               #Tbl-367 (&93837027443400)
[Tbl-368]:               #Tbl-368 (&93837027456432)
[Tabelle -366]:          #Tabelle -366 (&93837027529328)
[Tbl-370]:               #Tbl-370 (&93837027630624)
[Tabelle-368]:           #Tabelle-368 (&93837027681648)
[Tbl-372]:               #Tbl-372 (&93837027732008)
[Tabelle-370]:           #Tabelle-370 (&93837027805432)
[Tabelle-371]:           #Tabelle-371 (&93837027947672)
[Tabelle-372]:           #Tabelle-372 (&93837027989840)
[Tabelle-373]:           #Tabelle-373 (&93837028181688)
[Tabelle-374]:           #Tabelle-374 (&93837028206576)
[Tabelle-375]:           #Tabelle-375 (&93837028273464)
[Tabelle-376]:           #Tabelle-376 (&93837028303664)
[Tabelle-377]:           #Tabelle-377 (&93837028434320)
[Tabelle-378]:           #Tabelle-378 (&93837028455520)
[Tabelle-379]:           #Tabelle-379 (&93837028529168)
[Tabelle-380]:           #Tabelle-380 (&93837028559416)
[Tabelle-381]:           #Tabelle-381 (&93837028671864)
[Tabelle-382]:           #Tabelle-382 (&93837028713512)
[Tabelle-383]:           #Tabelle-383 (&93837028761016)
[Tabelle-384]:           #Tabelle-384 (&93837028773840)
[Tabelle-385]:           #Tabelle-385 (&93837028806176)
[Tabelle-386]:           #Tabelle-386 (&93837029012288)
[Tabelle-387]:           #Tabelle-387 (&93837029027288)
[Tabelle-388]:           #Tabelle-388 (&93837029041896)
[Tbl-392]:               #Tbl-392 (&93837029054616)
[Tbl-393]:               #Tbl-393 (&93837029256592)
[Tbl-394]:               #Tbl-394 (&93837029984512)
[Tbl-395]:               #Tbl-395 (&93837030064400)
[Tabelle-389]:           #Tabelle-389 (&93837030513288)
[Tabelle-390]:           #Tabelle-390 (&93837030720176)
[Tabelle-391]:           #Tabelle-391 (&93837030734240)
[Tabelle-392]:           #Tabelle-392 (&93837030746528)
[Tabelle-393]:           #Tabelle-393 (&93837032690056)
[Tabelle-394]:           #Tabelle-394 (&93837033505648)
[Tabelle-395]:           #Tabelle-395 (&93837033738032)
[Tabelle-396]:           #Tabelle-396 (&93837033761496)
[Tabelle-397]:           #Tabelle-397 (&93837037928632)
