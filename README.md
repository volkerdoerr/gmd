[![license: CC BY 4.0](https://img.shields.io/badge/license-CC_BY_4.0-brightgreen.svg)](https://creativecommons.org/licenses/by/4.0/)
[![](https://github.com/volkerdoerr/gmd/actions/workflows/converter.yml/badge.svg)](https://github.com/volkerdoerr/gmd/actions)

# gMD

gematik Markdown

Dieses Repository dient der Entwicklung der initialen Syntaxdefinition für den Prototyp eines freien menschen- und maschinenlesbaren Formats für die zulassungsrelevanten Dokumente der [gematik](https://www.gematik.de). gMD basiert auf [CommonMark](https://commonmark.org)* und wird durch die Definitionen in [gmd-definitions.yml](gmd-definitions.yml) erweitert. ⸾ _This repository is for development of the initial syntax definition for certification-relevant gematik documents. gMD is based on CommonMark* and is extended by the definitions found in gmd-definitions.yml._

---

## Tooling

[xml2gmd](https://www.to-be-implemeted.com) wird vom Konvertierungsjob [converter.yml](.github/workflows/converter.yml) aufgerufen, der immer dann automatisch gestartet wird, wenn Änderungen im Eingabeverzeichnis [input](input) vorgenommen wurden. Die resultierenden Dateien werden auf die [Github-Seiten dieses Repositorys](https://volkerdoerr.github.io/gmd/) hochgeladen und für Releases auch in das Ausgabeverzeichnis [output](output) gepusht. ⸾ _The xml2gmd tool is called by the conversion job converter.yml, which is started automatically whenever changes are made in the input directory. The resulting files are uploaded onto the github pages of this repository and for releases also pushed into the output directory._

---

*) Es gibt leider keinen (modernen) Markdown-Standard; CommonMark ist aber ein allgemein anerkannter Dialekt mit Unterstützung durch GitHub, GitLab, Reddit, Qt, Stack Overflow und anderen. ⸾ _Unfortunately there is no (modern) markdown standard; but CommonMark is a widely accepted dialect, supported by GitHub, GitLab, Reddit, Qt, Stack Overflow and others._
