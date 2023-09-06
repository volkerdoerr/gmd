[![CC BY 4.0][cc-by-shield]][cc-by]
[![][ci-badge]][ci.yml]

# gMD

gematik Markdown Prototyp

Dieses Repository dient der Entwicklung der initialen Syntaxdefinition für den Prototyp eines freien menschen- und 
maschinenlesbaren Formats für die zulassungsrelevanten Dokumente der [gematik]. gMD basiert auf [CommonMark]¹ und 
wird durch die Definitionen in input/[gmd-definitions.yml] erweitert. ٭ _This repository is for development of the 
initial syntax definition for certification-relevant gematik documents. gMD is based on CommonMark¹ and is extended 
by the definitions found in input/gmd-definitions.yml._

Beispiele ٭ _Examples_:

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

Der gematik polarion converter ([gpc]) wird vom Continuous-Integration-Job [ci.yml] aufgerufen, der immer dann 
automatisch gestartet wird, wenn Änderungen im Eingabeverzeichnis [input] vorgenommen wurden. Die resultierenden 
Dateien werden automatisch in das Ausgabeverzeichnis [output] gepusht. ٭ _The gematik polarion converter (gpc) tool 
is called by the continous integration job ci.yml, which is started automatically whenever changes are made in 
the input directory._

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





