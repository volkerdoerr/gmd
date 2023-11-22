# gMD Syntax

generated from [./gmd-syntax.ebnf](./gmd-syntax.ebnf), the semantic rules are yellow:

![](https://www.plantuml.com/plantuml/proxy?fmt=svg&cache=no&src=https://raw.githubusercontent.com/volkerdoerr/gmd/main/gmd-syntax.ebnf)

## Todo

### Link Examples

|                                                   | Explanation                           |
| :------------------------------------------------ | :------------------------------------ |
| \[gematik\]: \<https[]()://gematik.de\>           | link to website                       |
| \[https[]()://gematik.de]                         | link with direct url                  |
| \[gematik\]                                       | link alias usage                      |
| \[gematik homepage\]: \<gematik\>                 | link alias usage with different title |
| \<- $ \[gematik\]: \<https[]()://gematik.de\> -\> | link alias definition                 |
| \[License]: \<./license.txt\>                     | link to local resource                |

- Change "Alias" to "Name/Identifier"

- Tags
  - Semantics: opening tags must be closed by \</\> tag,  or defined as  short form
  - Semantics: Short forms finish at next whitespace.
  - Examples: like \<green\>xxx xxx\</\>, short form <id/\> or combination \<ita;14pt;green\>xxxx xxxx\</\>
  
- Calculated Contents
  - references to identifiers 
  - absolute/relative references to table cells
  
- Unicode  
  - Semantics: nearly all unicode characters and symbols are allowed. it is the resonsibility of the authors to not create messy documents  
  - Syntax and semantics: a tab is interpreted as the equivalent of 4 spaces

- Semantics explanation: Html-elements cannot be used in a gMD document









