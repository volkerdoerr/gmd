[![CC BY 4.0][cc-by-shield]][cc-by]
[![][ci-badge]][ci.yml]

# gMD

gematik Markdown Prototyp

Dieses Repository dient der Entwicklung der initialen Syntaxdefinition für den Prototyp eines freien menschen- und 
maschinenlesbaren Formats für die zulassungsrelevanten Dokumente der [gematik]. gMD basiert auf [CommonMark]¹ und 
wird durch die Definitionen in input/[gmd-definitions.yml] erweitert. ٭ _This repository is for development of the 
initial syntax definition for certification-relevant gematik documents. gMD is based on CommonMark¹ and is extended 
by the definitions found in input/gmd-definitions.yml._

Aktuelle Beispiele ٭ _current examples_:

- [output/gemKPT_Betr_V3.21.0.gmd.txt]
- [output/gemProdT_Kon_Highspeed_PTV_1.3.0-0_V1.0.0.gmd.txt]
- [output/gemSpec_CM_KOMLE_V1.16.0.gmd.txt]
- [output/gemSpec_ePA_FdV_V1.51.0.gmd.txt]

¹) Es gibt leider keinen (modernen) Markdown-Standard; CommonMark ist aber ein allgemein anerkannter Dialekt 
mit Unterstützung durch GitHub, GitLab, Reddit, Qt, Stack Overflow und anderen. ٭ _Unfortunately there is no 
(modern) markdown standard; but CommonMark is a widely accepted dialect, supported by GitHub, GitLab, Reddit, 
Qt, Stack Overflow and others._

---

## Continous-Integration

Das gematik Polarion Converter Tool (GPC, siehe weiter unter) wird vom Continuous-Integration-Job [ci.yml] aufgerufen, der immer dann 
automatisch gestartet wird, wenn Änderungen im Eingabeverzeichnis [input] vorgenommen wurden. Die resultierenden 
Dateien werden automatisch in das Ausgabeverzeichnis [output] gepusht. Das Log für den letzten Lauf findet sich in 
[output/gpc.log.txt]. ٭ _The gematik polarion converter tool (GPC, see below) is called by the continous integration job ci.yml,
which is started automatically whenever changes are made in the input directory. The log of the most recent run 
can be found in output/gpc.log.txt_

---

## gematik Polarion Converter Tool (GPC)

Donwload executable: [releases/download/wip/gpc]

Das GPC Tool konvertiert die von der gematik aus Polarion heraus exportierten (*.html) Dateien in saubere *.gmd, 
*.html, *.xml, *.xlsx Dateien und eine konsolidierte Datenbank gematik.database.sql. ٭ _The GPC tool converts 
the Polarion exported (*.html) files into clean *.gmd, *.html, *.xml, *.xlsx files and generates a consolidated 
gematik.database.sql file.

~~~
$ gpc
~~~

~~~
GEMATIK POLARION CONVERTER 0.8.0
  converts Polarion exported (*.html) files
  into clean *.gmd, *.html, *.xml, *.xlsx files
  and generates a consolidated gematik.database.sql file.
  ATTENTION: This is a prototype as proof of concept
             with only a subset of features implemented!
Copyright (c) 2023
  Volker Dörr (volker.doerr@cascade.de).
  All rights reserved.
Current path:
  /home/vol/GIT/volkerdoerr/xml2gmd/build-src-Desktop_Qt_Clang_64bit-Debug
ERROR: commandline parameter(s) missing!
  Usage: gpc source target
    source -- path or URL of filelist.txt
    target -- destination path (root of generated files)
  Examples:
    gpc ./input/filelist.txt ./output
    gpc ../../gmd/input/filelist.txt ../../gmd/output
    gpc https://gemspec.dev.ccs.gematik.solutions/docs/filelist.txt /tmp/gpc_test
PROCESS FAILED
~~~

---

This work is licensed under a [Creative Commons Attribution 4.0 International License][cc-by].

<!------------------------- links ------------------------->

[input]: input
[output]: output
[gematik]: https://www.gematik.de
[commonmark]: https://commonmark.org
[gmd-definitions.yml]: input/gmd-definitions.yml
[gpc]: https://github.com/volkerdoerr/gmd/releases/tag/wip
[ci.yml]: https://github.com/volkerdoerr/gmd/actions/workflows/ci.yml
[ci-badge]: https://github.com/volkerdoerr/gmd/actions/workflows/ci.yml/badge.svg
[github-pages]: https://volkerdoerr.github.io/gmd/
[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg
[output/gemKPT_Betr_V3.21.0.gmd.txt]: output/gemKPT_Betr_V3.21.0.gmd.txt
[output/gemProdT_Kon_Highspeed_PTV_1.3.0-0_V1.0.0.gmd.txt]: output/gemProdT_Kon_Highspeed_PTV_1.3.0-0_V1.0.0.gmd.txt
[output/gemSpec_CM_KOMLE_V1.16.0.gmd.txt]: output/gemSpec_CM_KOMLE_V1.16.0.gmd.txt
[output/gemSpec_ePA_FdV_V1.51.0.gmd.txt]: output/gemSpec_ePA_FdV_V1.51.0.gmd.txt
[output/gpc.log.txt]: output/gpc.log.txt
[releases/download/wip/gpc]: https://github.com/volkerdoerr/gmd/releases/download/wip/gpc



