[![license: CC BY 4.0](https://img.shields.io/badge/license-CC_BY_4.0-brightgreen.svg)](https://creativecommons.org/licenses/by/4.0/)
[![](https://github.com/volkerdoerr/gmd/actions/workflows/converter.yml/badge.svg)](https://github.com/volkerdoerr/gmd/actions)

# gMD

gematik markdown flavor prototype

Dieses Repository dient der Entwicklung der initialen Syntaxdefinition für den Prototyp eines freien menschen- und maschinenlesbaren Formats für die zulassungsrelevanten Dokumente der [gematik](https://www.gematik.de). ⸾ _This repository is for development of the initial syntax definition for certification-relevant gematik documents._

gMD basiert auf [CommonMark](https://commonmark.org)

Es gibt leider keinen (modernen) Markdown-Standard; CommonMark ist aber ein allgemein anerkannter Dialekt mit Unterstützung durch GitHub, GitLab, Reddit, Qt, Stack Overflow und anderen. Parser-Implementierungen existieren für nahezu alle gängigen Programmiersprachen: [List-of-CommonMark-Implementations](https://github.com/commonmark/commonmark-spec/wiki/List-of-CommonMark-Implementations). ⸾ _Unfortunately there is no (modern) markdown standard; but CommonMark is a widely accepted dialect, supported by GitHub, GitLab, Reddit, Qt, Stack Overflow and others. Parser implementations exist for almost all common programming languages._

---

## Tooling (to be implemented)

[xml2gmd](#tooling-to-be-implemeted) wird vom Konvertierungsjob [converter.yml](.github/workflows/converter.yml) aufgerufen, der immer dann automatisch gestartet wird, wenn Änderungen im Eingabeverzeichnis [input](input) vorgenommen wurden. Die resultierenden Dateien werden im Ausgabeverzeichnis [output](output) abgelegt und automatisch gepushed. ⸾ _The Cascade xml2gmd tool is called by the conversion job converter.yml, which is started automatically whenever changes are made in the input directory. The resulting files are placed in the output directory and are automatically pushed._

---
