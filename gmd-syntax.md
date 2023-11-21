# gMD Syntax

generated from [./gmd-syntax.ebnf](./gmd-syntax.ebnf), the semantic rules are yellow:

![](https://www.plantuml.com/plantuml/proxy?fmt=svg&cache=no&src=https://raw.githubusercontent.com/volkerdoerr/gmd/main/gmd-syntax.ebnf)

## Examples

### Paragraph Examples

|                                                               | Explanation                          |
| :------------------------------------------------------------ | :----------------------------------- |
| The quick brown fox<br>jumps over the leazy wall.             | multiline paragraph                  |
| &nbsp;&nbsp;The brown fox<br>&nbsp;&nbsp;over the leazy wall. | multiline paragraph with indentation |
| The quick brown↵ fox jumps over↵ the leazy wall.              | paragraph with manual line breaks    |

### Heading Examples

|                                               | Explanation                         |
| :-------------------------------------------- | :---------------------------------- |
| # Section One                                 | heading h1 traditional form         |
| # $. Section One                              | heading h1 with automatic numbering |
| # 1. Section One                              | heading h1 with manual numbering    |
| ## Section One One                            | heading h2 traditional form         |
| # 1.1 Section One One                         | heading h2 with manual numbering    |
| ### This Is A Really<br>Very long Heading     | heading h3 spanning multiple lines  |
| # $.$.$ This Heading Has↵ A Manual Line Break | heading h3 with manual line break   |

### Link Examples

|                                                   | Explanation                           |
| :------------------------------------------------ | :------------------------------------ |
| \[gematik\]: \<https[]()://gematik.de\>           | link to website                       |
| \[https[]()://gematik.de]                         | link with direct url                  |
| \[gematik\]                                       | link alias usage                      |
| \[gematik homepage\]: \<gematik\>                 | link alias usage with different title |
| \<- $ \[gematik\]: \<https[]()://gematik.de\> -\> | link alias definition                 |
| \[License]: \<./license.txt\>                     | link to local resource                |

### Image Examples

|                                                                | Explanation                             |
| :------------------------------------------------------------- | :-------------------------------------- |
| !\[gematik logo\] \<https[]()://gematik.de/logo\>              | image from website                      |
| !\[https[]()://gematik.de/logo\]                               | image with direct url                   |
| !\[logo\]                                                      | image alias usage                       |
| !\[company logo\] \<logo\>                                     | image alias usage with different title  |
| \<- alias:<br>$ !\[logo\]: \<https[]()://gematik.de/logo\> -\> | image alias definition                  |
| !\[local logo\] \<./logo\>                                     | image from local resource               |
| !\[local logo\] \<data:image/svg;base64,IVBORUIH\>             | image from embedded source (data_uri)   |
|                                                                | image scaling                           |
|                                                                | image horizontal and vertical alignment |

## Todo

- Tags
  - Semantics: opening tags must be closed by \</\> tag,  or defined as  short form
  - Semantics: Short forms finish at next whitespace.
  - Examples: like \<green\>xxx xxx\</\>, short form <id/\> or combination \<ita;14pt;green\>xxxx xxxx\</\>
  
- Calculated Contents
  - [=Expression]
  - pure functions only
  - every expression produces a value
  - references to other "cells" can be used as values
  - no sideeffects at all
  - gMD has predefined functions
  - additional functions can be defined using pragmas 
  
- Unicode  
  - Semantics: nearly all unicode characters and symbols are allowed. it is the resonsibility of the authors to not create messy documents  
  - Syntax and semantics: a tab is interpreted as the equivalent of 4 spaces

- Semantics explanation: Html-elements cannot be used in a gMD document









