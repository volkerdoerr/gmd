# gMD Syntax

Contents: [Definition](#definition) [Graphs](#graphs) [Examples](#examples) [Todo](#todo)

## Definition

```
gMD = {"eol"}, {List|Table|Paragraph}, {"eol"};
Paragraph = Indent, [HeadingMarker], Text, "eol", {Indent, Text, "eol"}, "eol";
HeadingMarker = "#", ({"#"} |number, ".", [number, {".", number}] |"$", ".", ["$", {".", "$"}]);
Text = {Link|Image|HorRuler|NewLine|"<", Tag, ">"|TagDefinition|Modifier|"\", "chr"|"chr"};
Link = "[", (Title, "]", [":"], "<", (URL|AliasTitle), ">" | (AliasTitle|URL), "]"); 
Image = "!", "[", (Title, "]", [":"], "<", (URL|DataURI|AliasTitle), ">" | (AliasTitle|URL), "]"); 
Modifier = ("**"|"~~"|"^^"|"__");
HorRuler = ("-----"|"=====");
NewLine = "↵";
List = ListItem, "eol", {ListItem, "eol"}, "eol";
ListItem = Indent, ListMarker, Text, { "eol", Indent, Text};
ListMarker = (number, "."|letter, ")"|"$", ("."|")")|"*"|"-");
Table = Row, "eol", {Row, "eol"}, [TableFooter, "eol"], "eol"; 
Row = [RulerLine, "eol"], ContentLine, {">", "eol", ContentLine}; 
TableFooter = RulerLine, [ "eol", FooterLine, {"eol", FooterLine}, "eol", RulerLine ], "eol" ;
RulerLine = "|", CellRuler, "|", {CellRuler, "|"};
ContentLine = "|", [CellSpan], Text, "|", {[CellSpan], Text, "|"};
FooterLine = "|", {chr}, "|";
CellRuler = (":"|"="|"-"), ("="|"-"), {"="|"-"}, (":"|"="|"-");
CellSpan = ("/", [number], [ ">", [number]] | ">", [number] );
```

## Graphs

![](https://www.plantuml.com/plantuml/svg/bLRDRjj64BxxAQPiWKY6P2E7NkmaID6WY86aADpaP2l1Y1o9YontrTrbP46KZtsZlb2Vf3Exsf8I12FHGLpEpymtFpFBrpwW2pGtYxEpqVaKq6p0qryjcP8c46eCK5doO6o01aDPCut0Rqp0Xsb52sLKKDQ0yX0SOQ0Aq8DrbJBeDX3e8Lp06TjDEcLG9MgzWT8wHoKRfq2bQ6MdqBG-06flX_weGSEgu5fDVWAMYMwjF84AJxfcpratkbKcEmwuz82EBIoDTLHTd8_FpfRlty1Bs1PaTR6RmFQTyg7xW7DDtH_eSEbmLGiz2Lodb9MsQSW43p6Li5QXXkB5j00q5P2fzfJfgqGfqS2S68ad9vZfAuV2uL14yByRnd5ZAhOxWRktX1pKyZswB-Hc4_X03qoE81XC5XjGT_ld7g6A4YcpSqePnOPWOHrmMa0hSoghEJCWm0umCBZYH_Ozsl9ZrvcscPDZdnTCkyjls_YQtdQphlYfo19yp6m-xcRZFKviWsrGwfoqs1_CDz1wEGXgbeQoHeTb82Sf38mAx0Aun2tglPgFcPHqC4wkeVdItJIufEwjTRUj9jVzJcicKrUyA3Xlk6GShugE3syeTtJttbPgeLYuk1USPUsABlxdkhUUROhpriH1e2erbOhJ8ecrQwga1QMjQlImSfGbfHCSUN9VzseY5miWRz1FbiyDitOg138IjQfI4IjRjj9wO2KPfMuhDZOwr8-U4ZFFROIteG1-HQN4M8tPEVaILrJr-VKmOi0baLZbCZoxVpQMYJarRKCjZ2sljO2cXpsgXRDDTey6zSOh7_jAoYFjT2Vjz445JPpiMUoIgsB6vnV2-7Zxhlj5A_HHOXph1HsCUbh78kEeEhw6emAXI44GCJ0SJo8CaqJQKnn2JjLXQaVA2FYKv3dLF4i76v537iT0Oej993ymu6y8vmq6_7XxytrXvQPaFwFY_9mxyl6H_pvzuh_FduiyI1n1lr15Jffo8G5ONO4rbtQnOAFtZ_UFcGKgS5RAdiasCyktCbMbKwlGyzdTW7_0ZVENXor2dSgFCRwKtm2cCd7vN44H1UIc48YP6ANFKZoQpBBkbnWzO1dWvq7ZYTCqsB4C__xzZ-m_MU7yAe-RG4s_DdlAyShCdC4A5b9QVNdFRhEXuVgLrT2BIkI3rTXf2Y6UnqNQXYEXyjkuAwIKqvoOmtL65IX6SvNk5v-kayJYxCkMYVCfBkIgpSgeLpNEATvy9mm8c6C3usYWNyDF0U00ZhrVovvnb2v3ATb-VSZsLf9fcJXiTRnSdX-wUXhk2NVZxtE7qTsyrHmtQ2xHaVbpQRCAVKtLAVQqY3CkdmBINBTstJTI_xBZCOyYlrcRAYtKsVufyykoh7uN1qCQjHVvrPh0aIJYblT0TZ3axF9gQpWiDPKf0MVNwKDcPRrNx5pI8-aeMK-P5cN1JVjRKrOCXYX19bwU26Lo4SSkNVU3C2JU7kzTXfMO6UynRPVXzxgG4m7SvJsLHxMJA4dhI9oaz-qXGIPha8YiTITIVwxGz5z5KVaaFL_SX6KD9Gl8rJhyQfD4QCzQbv9KVWwkYBZJ-lWoW6rPkrsqFbYzYvItM1xb-tjUTkMY3QqZQ3s9GO7PRyahsP1f4V1ow8_R_P4T7GZjNI8uCP5YODvW9wO0ACv72XddzYl9rLqJLkGYyUBisCZq6uqOwnhKfuqmqWDDr6ffP5hpTsTKyp0ddceOjIOedGHNAsBVfeoNjr0Cb_38z5ZyQLg4QRHxbTXvQhFK19nQraSoPAgXHCcGo9qqWwOwb1QdZNgWgl-ua8IB7EVi-DDFAfmRCHRuily-dl59Ph4dpA0x9C2-mBahZtRIgyEDA7bAYenALDh6U0WMHFMQSMLkGyYCvn8Aj_a9mvTF6MQL9wrApAyvPpGtY_y0)

_produced using the PlantUML generation service at https://www.plantuml.com/plantuml/uml/_ 

## Examples

| Paragraph Examples                                            | Explanation                              |
|:--------------------------------------------------------------|:-----------------------------------------|
| The quick brown fox<br>jumps over the leazy wall.             | multiline paragraph                      |
| &nbsp;&nbsp;The brown fox<br>&nbsp;&nbsp;over the leazy wall. | multiline paragraph with indentation     |
| The quick brown↵ fox jumps over↵ the leazy wall.              | paragraph with manual line breaks        |

| Heading Examples                                              | Explanation                              |
|:--------------------------------------------------------------|:-----------------------------------------|
| # Section One                                                 | heading h1 traditional form              |
| #. Section One                                                | heading h1 with automatic numbering      |
| # 1. Section One                                              | heading h1 with manual numbering         |
| ## Section One One                                            | heading h2 traditional form              |
| #.# Section One One                                           | heading h2 with automatic numbering      |
| # 1.1 Section One One                                         | heading h2 with manual numbering         |
| ### This Is A Really<br>Very long Heading                     | heading h3 spanning multiple lines       |
| #.#.# This Heading Has↵ A Manual Line Break                   | heading h3 with manual line breaks       |

| Link Examples                           | Explanation                              |
|:----------------------------------------|:-----------------------------------------|
| \[gematik\] \<https[]()://gematik.de\>  | link to website                          |
| \[https[]()://gematik.de]               | link with direct url                     |
| \[gematik\]                             | link alias usage                         |
| \[gematik homepage\] \<gematik\>        | link alias usage with different title    |
| \[gematik\]: \<https[]()://gematik.de\> | link alias definition                    |
| \[License] \<./license.txt\>            | link to local resource                   |

| Image Examples                                       | Explanation                               |
|:-----------------------------------------------------|:------------------------------------------|
| !\[gematik logo\] \<https[]()://gematik.de/logo\>    | image from website                        |
| !\[https[]()://gematik.de/logo\]                     | image with direct url                     |
| !\[logo\]                                            | image alias usage                         |
| !\[company logo\] \<logo\>                           | image alias usage with different title    |
| !\[logo\]: \<https[]()://gematik.de/logo\>           | image alias definition                    |
| !\[local logo\] \<./logo\>                           | image from local resource                 |
| !\[local logo\] \<data:image/svg;base64,IVBORUIH\>   | image from embedded source (data_uri)     |
|                                                      | image scaling                             |
|                                                      | image horizontal and vertical alignment   |

## Todo

- Tags
  - Syntax and semantics: tag definition
  - Syntax and semantics: combination of tags 
  - Semantics: opening tags must be closed by \</\> tag,  or defined as  short form
  - Semantics: Short forms finish at next whitespace.
  - Examples: like \<green\>xxx xxx\</\>, short form <id/\> or combination \<ita;14pt;green\>xxxx xxxx\</\>
- Includes
  
  - Syntax and semantics: missing
- Unicode
  
  - Semantics: nearly all unicode characters and symbols are allowed. it is the resonsibility of the authors to not create messy documents
  
  - Syntax and semantics: a tab is interpreted as the equivalent of 4 spaces
- Pre-formatted text
  - Syntax and semantics: code block
  - Syntax and semantics: syntax highlighting
  - Syntax and semantics: quotation block
- Semantics explanation: Html-elements cannot be used in a gMD document









