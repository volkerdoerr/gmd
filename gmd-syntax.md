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

![](https://www.plantuml.com/plantuml/svg/bLRDRXkt4x_xAUQ__mAH3Cb63htOIP2YGH43IL6uoSbM0eexqXBXaYh9ZInevMFVg2_K9-aCkSpk2eAHwA3bpiVCRpvckAzz42xWqgpEpYRdSn1c1nx_Qj18d46eH83IeWTZ0zGYo8fe27vdWdYObxXIHWLb3IWFmQ48M8BmO5sfZ70x2FWGBk2Cx2OT6PGKMkz0MkTGad4CA5ahEuMwyG64zdRe3sjXI1LSez7Fm1BHRPL7KE59r-GvwqQtocJ7GQmz24SMriOwB2_EfsTdw_Tlu2Ni2xIwECnW_qxvq7uGIutj7yA9jHERYkb9u3gbJDgwHXCyn5J2LeKAYXVp0eGf0KtPKUQl4aKA0qia91uTOyQl50g5Wn71DpU4uyQKP7S6TszHK53hzy9zGRUOmGTy8784GM2Is8Xww9uTGXKbKcQNc38gQeILTK1f0QtCgQpcp0036s4WSCN_oVTaJuz3QvfwYOvyNX3jBh_jusjwEopQugSYIz0ni-buM4mxdA89jXPSvwH5_c2vWyRJWL6pDCYAKYG3EavX85HWLq0bReJkr7pC9AU3S58DpPVsfXPhRDzQTqiDvDhVSKjaR8iN1ULDh0d7gwAbmvjl7Ts-jwLQAH8kxXcdh5pHnlzSzyQJJNRUc3W8MAQcKcbQAB5sYoMt8BTL9Jni76P9xWI77jtNJetaKW7u3Vh9yhbXjaw5W8QZLcKgOcbbmwq7bfCXTLEIiSbOdprbPZUt4TuE0_WDIewnd99pz59iiEppws52W2KYMUKoFBj_DkM9EJbj0oqHMrvh1eqF7QgLitLsBupGEwzyx2ik3xVJ7RVJ1nKqKh8NiKkkYWMTNp3Zu-sxzXUjX8yIqrWlQ67IqreIcKRLwJKS5KYm50GM0qFn9C8mIQWznY6aL8rJEr66mQSaBx6YMHfjH0fv6WE9BSQH_8y0VqSuRqGG7szlVYoit9JaPrASdrD7FZxItwTFzFVvSv47YIBe5ohBSLEkE02hIx3cqgvMPFJ-yVxn6qi5oehicMGpitp3KoMTseIUJ-u6_14tpbyUjWXrpZ_2-99_0vZAnELp1Pq4NnMCCLEJ_5cAIADPL_qQmmSX0_myQ3rssuqs5-BVl__X3SXBd5xvSHEmxXTdJpbUcfapMC9CIiilRzfzDZHSmBmSUb6EVR0SMuqXnFEqIFjmmbHwcxO55tEUKpDUQ5Y28ZHNwORnwK99BCf_sZCqeUo2BzkiBFIc4akCTzy90mpcsC0q6kWNyLC0A81ZxzUyQHocwv1BrYqGtj-ACyqp9neThvVdOrTFm3tjRlfZxaHqjsmqnGsQIdHa_fpRh1I-ml8KUrx4AUUF0MwkMxlj6wb_ET2WHv7VhELA9-gYU_84aooftyNHu4RjHNwr9b0aYRYdJT2nHfn3NcurXQNcF2RWx3PzocoizugSSteu7PBq5BK2hxXvVs_oaX4XIg0fuu84cLm06qmN_Y0CZhV7UvTX9MR6UqmxPFYzBkH407LvJwLHRJbAr3eIP-bzFoRmP0qIaRNkMEhFZJ3zTr5KFadFLpSAMO4a0RvSXzzjd0ZjIUkIaqhFmIKHjnh7DuQzbvKxHEk3vRjAUOlbKRw_wNbRhfhGE8J68njacFsUlE8TcHO1BOV-kE-Ev6WarBaKuDX4Ye5uWvsO0i0u7obaiRHVaI_l2aM9BX8lpewDpB_JYB6k5lgq4K8wqXHQhGrFQ_xoZ6eUbaXJ3PE6kbKdmSq6oRUHyVfcYg4I7fcUiZ-Dgp2FTgyIEqzjbfg1K-jgBCDjFvIG10dTIJF2b6DfTbgh1opxpmjEECjHpeu__dA5kH5ZWI_xB-G5dNWMUy82sZ41kWBdhZpQIQ_66v7pb1G95QiqjQ74Ms3LQyALkJKAOZpdKAZDJnY-VCemgJnfbMD-JJd3fLdz1m00)

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









