[![CC BY 4.0][cc-by-shield]][cc-by]
[![][ci-badge]][ci.yml]

# gMD

<a href="./gmd-syntax.md"><img src="https://www.plantuml.com/plantuml/proxy?fmt=svg&cache=no&src=https://raw.githubusercontent.com/volkerdoerr/gmd/main/gmd-syntax.ebnf" align="right" width="50%" style="border: solid;"></a>

g<sub>ema</sub>TI<sup>k</sup> Markdown Prototype

Dieses Repository dient der Entwicklung der initialen Syntaxdefinition (siehe: [gmd-syntax.md](gmd-syntax.md)) für den Prototyp eines freien menschen- und 
maschinenlesbaren Formats für die zulassungsrelevanten Dokumente der [gematik]. gMD basiert auf [CommonMark]¹ und 
wird durch die Definitionen in input/[gmd-definitions.yml] erweitert.
/// _This repository is for development of the initial syntax definition (see: gmd-syntax.md)for certification-relevant gematik documents. 
gMD is based on CommonMark¹ and is extended by the definitions found in input/gmd-definitions.yml._

Aktuelle Testbeispiele ٭ _current test examples_:

[output/gemKPT_Betr_V3.21.0.gmd.txt]  
[output/gemSpec_CM_KOMLE_V1.16.0.gmd.txt]  
[output/gemSpec_ePA_FdV_V1.51.0.gmd.txt]

¹) Es gibt leider keinen (modernen) Markdown-Standard; CommonMark ist aber ein allgemein anerkannter Dialekt 
mit Unterstützung durch GitHub, GitLab, Reddit, Qt, Stack Overflow und anderen.
/// _Unfortunately there is no (modern) markdown standard; but CommonMark is a widely accepted dialect, supported 
by GitHub, GitLab, Reddit, Qt, Stack Overflow and others._

---

## Continous-Integration ([ci.yml])

Das gematik Polarion Converter Tool (GPC, siehe weiter unten) wird vom Continuous-Integration Script [ci.yml] aufgerufen,  
welches sowohl manuell gestartet wird, als auch automatisch, wenn Änderungen im Eingabeverzeichnis [input] vorgenommen wurde.
/// _The gematik polarion converter tool (GPC, see below) is called by the continous integration script ci.yml,
which is  either manually started or automatically, whenever changes are made in the input directory._

### convert-test-files (job)

Die resultierenden Dateien werden automatisch in das Ausgabeverzeichnis [output] gepusht. Das Log für den letzten Lauf findet sich in 
[output/log.txt].
/// _The resulting files are pushed automatically in the output directory, the log of the most recent run can be 
found in output/log.txt._

### convert-production-files (job)

Alle resultierenden Dateien werden automatisch nach [gemspec.online] gepusht. Das Log für den letzten Lauf findet sich in 
[gemspec.online/log.txt].
/// _The resulting files are pushed automatically to gemspec.online, the log of the most recent run can be 
found in gemspec.online/log.txt._

| Type                      | Directory    Link            |
|---------------------------|------------------------------|
| Anbietertypsteckbriefe    | [gemspec.online/gemAnbT]     | 
| Anwendungssteckbriefe     | [gemspec.online/gemAnw]      | 
| Featuredokumente          | [gemspec.online/gemF]        | 
| Implementierungsleitfäden | [gemspec.online/gemILF]      | 
| übergreifende Konzepte    | [gemspec.online/gemKPT]      | 
| Produkttypsteckbriefe     | [gemspec.online/gemProdT]    |  
| Richtlinien               | [gemspec.online/gemRL]       | 
| S/MIME-Profile            | [gemspec.online/gemSMIME]    | 
| PS-Schnittstellen         | [gemspec.online/gemSST]      | 
| Spezifikationen           | [gemspec.online/gemSpec]     | 
| Verzeichnisse             | [gemspec.online/gemVZ]       | 
| Wartungsthemen            | [gemspec.online/maintenance] | 
| TI 2.0                    | [gemspec.online/TI2.0]       | 

---

## gematik Polarion Converter (GPC)

Donwload: [releases/download/wip/gpc]

<!-- Das GPC Tool konvertiert die von der gematik aus Polarion heraus exportierten (*.html) Dateien in saubere *.gmd, 
*.html, *.xml, *.xlsx Dateien und eine konsolidierte Datenbank gematik.database.sql.
/// _The GPC tool converts 
the Polarion exported (*.html) files into clean *.gmd, *.html, *.xml, *.xlsx files and generates a consolidated 
gematik.database.sql file._ -->

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
[output/log.txt]: output/log.txt
[releases/download/wip/gpc]: https://github.com/volkerdoerr/gmd/releases/download/wip/gpc
[gemspec.online/log.txt]: https://gemspec.online/log.txt
[gemspec.online]: https://gemspec.online
[gemspec.online/log.txt]: https://gemspec.online/log.txt
[gemspec.online/TI2.0]: https://gemspec.online/TI2.0/
[gemspec.online/gemAnbT]: https://gemspec.online/gemAnbT/
[gemspec.online/gemAnw]: https://gemspec.online/gemAnw/
[gemspec.online/gemF]: https://gemspec.online/gemF/
[gemspec.online/gemILF]: https://gemspec.online/gemILF/
[gemspec.online/gemKPT]: https://gemspec.online/gemKPT/
[gemspec.online/gemProdT]: https://gemspec.online/gemProdT/
[gemspec.online/gemRL]: https://gemspec.online/gemRL/
[gemspec.online/gemSMIME]: https://gemspec.online/gemSMIME/
[gemspec.online/gemSST]: https://gemspec.online/gemSST/
[gemspec.online/gemSpec]: https://gemspec.online/gemSpec/
[gemspec.online/gemVZ]: https://gemspec.online/gemVZ/
[gemspec.online/maintenance]: https://gemspec.online/maintenance/





