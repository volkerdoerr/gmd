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

![](https://www.plantuml.com/plantuml/svg/bLRDRjj64BxxAQPiWKY6P2E7NkmaID6WY86aADpaP2l1Y1o9YontrTrbP46KZtsZlb2Vf3Exsf8I12FHGIJdP-QRdvdTrpwW2pGtYxEpqVaKq6p0qryjcP8c46eCK5doO6o01aDPCut0Rqp0Xsb52sLKKDQ0yX0SOQ0Aq8DrbJBeDX3e8Lp06TjDEcLG9MgzWT8wHoKRfq2bQ6MdqBG-06flX_weGSEgu5fDVWAMYMwjF84AJxfcpratkbKcEmwuz82EBIoDTLHTd8_FpfRlty1Bs1PaTR6RmFQTyg7xW7DDtH_eSEbmLGiz2Lodb9MsQSW43p6Li5QXXkB5j00q5P2fzfJfgqGfqS2S68ad9vZfAuV2uL14yByRnd5ZAhOxWRktX1pKyZswB-Hc4_X03qoE81XC5XjGT_ld7g6A4YcpSqePnOPWOHrmMa0hSoghEJCWm0umCBZYH_Ozsl9ZrvcscPDZdnTCkyjVs_YPldQphlYfo1BycjdykfkDzpYn3RP1gNFIOdymtq3h-KLGYpIKDJei0pb9OM1KO1V09MvHxzLypAIa0rvA3SsNxgR19NLlhRjjDRdkTrepcRhYHS5vmoNZU5Lq_FA6SaTtxssb5eg5Ytl1MTQkwE9_hdlhsQOuRqqS1AfIKwauBP9OkwPAMb3QgaOFAqTPKZh1aIVtTQycSh40yWNzPFdSC6kdGY0ZKQig5R6oPIkj1rQIKUgsOcEZG_teAJ7pt4Pu6mhWLrHAZDMOdG_0DVlGqu0mZto9Awhwt7iOiNn9n1wbHC_kdur5-DGa3hKmZeFM4X0zx14ld6qoD3IeDrxvs7DIEccrEscr3ofeuaBCOWTT5JD-Vo6CZxVlkb-qGXybnh6MqC6eftKiCewgusiuAXwA50GH0yFn9C8mWQGzoO3Ap1wcVQICW4y5c5FDStQmBJdaSGmajfz4yWC3_ePmtc30ZxSttnTMRbZsCohEpxbR7n_vxzCd_llykSX3nX7qorRaf64N4e3L5LXpQHSBDdh_UF-OMQ02PwNicMmpitmh4rSwjGezdzqD-0VSE9jv42FKgVmOuqlv3M0g4nVJ5HHHGFfG86PYb3vByMWooxfVSFI0PO2V1uqdJjFGnpBy-_S_iXjblVEdF6u2DVrAxId7wpHp1kjPI6ajvXsypOQ6grdMHYygaG_MPgSfXFW-BjAc70cLlyPT8QMSviGShZggG36QgtJs-7JK91PdNpPGd4zn8STmLaQzgd5EyLGyOK3071iOYu7XYdu200TmxFrQTf2ZT51AoVRhGpQxaapBn66huy7p_D3L2RXFknj_dpkCxkQjvhX1SucEp9zBcrNeQwfEiQT5d76v9aXptTfrtqZznux7F8hyPgrKEb5d-wVCByko-bqS36dKNkHNQm97aeXRtWFPmP2powkjuR3KLAO4d5sd7RwotYjsBkcHT9IifqoBik2c_OagAmP3b21JnVK8PN81OZ1T1GPXIBmzthiCAp4ptcFQBiFlTI4d0hZBUogFQYTHajQHE4dVsqE2J5PEn43hJgJ-NA7fRqnH-IGz7-g4PGqb2yYnExpHIIAqPwrBJgey1qT4t6avlXx0jgpTBbeVhDv5obiiZ_Bz7K1svQ8DhIDeFOb1WTbloIlPa6aHy7BeNxVxLtPq8BHtYU34H8g1UOETc0AWE1yfP9pRhoH7TqrOaOl4YxDZ8zDlD6AiQr2VDi983pHHgwMHQSrtqgZcOKuyrJ1gJL0w2QvMnBvD6GzleHWkuP7fiVZJj0ZJQFSgiVFKPga9EBMiZsJ8L4E9aY6HEsa6JNKeBKuRzK1LVxcGX8kSvEpeMfWhB8qO2tpPtvrd_2Qps1Dcq1qI81TutvL7E-dLuKQKF2L5GSKgRMCy10kYUisuChSXPCPp2ONR_8JXooSCYygJLYNcrvmpcfl5Vm00)

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

- Attributes
  - \<green\>xxx xxx\</\>
  - undefined attributes are not allowed
  - attributes are defined by gMD
  - short form finishes at next whitespace:
    \<bgred/\>red not red 
- Styles
  - styles are combinations of attributes and can be used like attributes
  - undefined styles are not allowed
  - styles are defined inside the document or included
  - gMD has predefined and reserved styles
  - short form finishes at next whitespace:
    \<default_text/>default not more 
- Tagging
  - \<id\>xxxx xxx\</\> 
  - undefined tags are not allowed
  - tags are defined inside the document or included
  - gMD has predefined and reserved tags
  - short form finishes at next whitespace:
    \<id/\>A_12345 the following is not part of the id 
- Includes
  - ?
- Language
  - languages denominators are predefined attributes 
- Backslash escapes
  - Insecure characters
  - Characters that would be interpreted 
- Unicode
  - nearly all unicode characters and symbols are allowed. it is the resonsibility of the authors to not create messy documents
- Tabs
  - a tab is interpreted as the equivalent of 4 spaces
- Pre-formatted text
  - Block code
  - Syntax highlighting
  - Block quotations
- Comments
  - comments are written in between a "\<-" "-\>" sequence
  - xxxx xxxxxx \<- this is a comment -\> xxxx xx
  - comments can be inserted everywhere,
  - they are invisible if the document is rendered 
- No HTML
  - html-elements cannot be used in a gMD document
  - due to the possibilities given by attributes, styles and tagging this not neccessary









