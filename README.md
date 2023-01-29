[![CC BY 4.0][cc-by-shield]][cc-by]
[![][ci-badge]][ci-job]

# gMD

gematik Markdown Prototyp

Dieses Repository dient der Entwicklung der initialen Syntaxdefinition für den Prototyp eines freien menschen- und maschinenlesbaren Formats für die zulassungsrelevanten Dokumente der [gematik]. gMD basiert auf [CommonMark]¹ und wird durch die Definitionen in input/[gmd-definitions.yml] erweitert. ⸾ _This repository is for development of the initial syntax definition for certification-relevant gematik documents. gMD is based on CommonMark* and is extended by the definitions found in input/gmd-definitions.yml._

---

## Continous-Integration

[xml2gmd] wird vom [Continuous-Integration-Job] aufgerufen, der immer dann automatisch gestartet wird, wenn Änderungen im Eingabeverzeichnis [input] vorgenommen wurden. Die resultierenden Dateien werden automatisch in das Ausgabeverzeichnis [output] gepusht und können manuell (mittels [Export-Job]) als Html auf die [Github-Pages] (dieses Projektes) hochgeladen werden. ⸾ _The xml2gmd tool is called by the continous integration job ci.yml, which is started automatically whenever changes are made in the input directory. The resulting files are automatically pushed into the output directory and can also manually (using the export-job) be uploaded as html to this projects github-pages. _

---

¹) Es gibt leider keinen (modernen) Markdown-Standard; CommonMark ist aber ein allgemein anerkannter Dialekt mit Unterstützung durch GitHub, GitLab, Reddit, Qt, Stack Overflow und anderen. ⸾ _Unfortunately there is no (modern) markdown standard; but CommonMark is a widely accepted dialect, supported by GitHub, GitLab, Reddit, Qt, Stack Overflow and others._

---

This work is licensed under a [Creative Commons Attribution 4.0 International License][cc-by].

<!------------------------- links ------------------------->

[input]: input
[output]: output
[gematik]: https://www.gematik.de
[commonmark]: https://commonmark.org
[gmd-definitions.yml]: input/gmd-definitions.yml
[xml2gmd]: https://github.com/volkerdoerr/gmd/releases/tag/wip
[continuous-integration-job]: https://github.com/volkerdoerr/gmd/actions/workflows/continous-integration.yml
[ci-badge]: https://github.com/volkerdoerr/gmd/actions/workflows/continous-integration.yml/badge.svg
[ci-job]: https://github.com/volkerdoerr/gmd/actions/workflows/continous-integration.yml
[export-job]: https://github.com/volkerdoerr/gmd/actions/workflows/export-to-github-pages.yml
[github-pages]: https://volkerdoerr.github.io/gmd/
[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png
[cc-by-shield]: https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg
