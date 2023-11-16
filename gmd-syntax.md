# gMD Syntax

Contents: [Definition](#definition) [Graphs](#graphs) [Examples](#examples) [Todo](#todo)

## Definition

```
gMD = {"eol"}, {List|Table|Paragraph}, {"eol"};

Paragraph = Indent, [HeadingMarker], Text, "eol", {Indent, Text, "eol"}, "eol";
HeadingMarker = "#", ({"#"}|".", ["#", {".", "#"}]|number, ".", [number, {".", number}]);
Text = {Link|Image|Tag|Modifier|HorRuler|NewLine|"\", "chr"|"chr"};
Link = "[", (Title, "]", [":"], "<", (URL|AliasTitle), ">" | (AliasTitle|URL), "]"); 
Image = "!", "[", (Title, "]", [":"], "<", (URL|DataURI|AliasTitle), ">" | (AliasTitle|URL), "]"); 
Tag = "<", (Attribute|Style|UserTag|Comment), ">"; 
Modifier = ("*"|"~"|"^"|"_");
HorRuler = ("-----"|"=====");
NewLine = "↵";

List = ListItem, "eol", {ListItem, "eol"}, "eol";
ListItem = Indent, ListMarker, Text, { "eol", Indent, Text} ;
ListMarker = (number, "."|"*"|"+"|"-");

Table = Row, "eol", {Row, "eol"}, [TableFooter, "eol"], "eol"; 
Row = [RulerLine, "eol"], ContentLine, {"eol", ContentLine}; 
TableFooter = RulerLine, [ "eol", FooterLine, {"eol", FooterLine}, "eol", RulerLine ], "eol" ;
RulerLine = "|", Ruler, "|", {Ruler, "|"};
ContentLine = "|", [CellSpan], Text, "|", {[CellSpan], Text, "|"}, [">"];
FooterLine = "|", {chr}, "|";
Ruler = [":"], ("---", {"-"}|"===", {"="}), [":"];
CellSpan = (RowSpan, [ColSpan] | ColSpan, [RowSpan]);
ColSpan = ">", [number];
RowSpan = "/", [number];
```

## Graphs

![](https://www.plantuml.com/plantuml/svg/bLJ1RXCn5BpxAuov9932dT2gA1Lgf0QXD3qj2tB8QxhgPhTo71MqDaV-Y1_YIvXdh_56S818cxNdpJoFdN7EzrORI-lcLeZjuaAUoavHMoi_aTrLjRTkfTSrkVVQwAtH3tV0Uy9KYDyePFDcGusToEAIzAPgjWjjxicK4xcYBu231jf46w2-Vq_5aHGzrLD8HXrUtgaN61S1wSAOqT8rXzsQ36QXd6QH4MU-74y5BuU6s59px-OxlILiREiMxQQwhSYuozOi3pK6x-WH77Bg0o_n-Suenz-yNTQogO9DhIfR4nXbSFLAbHY_viBDyigzgIkz3umnu3CbdHnbp84o3jBnL8fWXji-WVeVUbzegs-My_zQ0rl52jm376jDjJvOSjVsAnFtP51titQteyR6Pj2aeu5mf9xX5BxX-OZd4rgAT5wXUi8VL4xvmzN-47dDdzz_A2I5euGfl-QMTZaF2VaZ2wamY1P3CHifFrtgCuoLbwnEL7Ou28aBUtcEvuITYX1lS9RjOpQ5IVPJ1ChRjhLaUhHCBgK05UeY70RlEJDcRMFXYS5qPuv03_MWDReCcXJ9IomUDycOJvwpLYPpE8KCufTmYJM9uovF4Ew1iKGkPbJNrm-woPSuwFwAyq4XEELKP7UfKOSBv0EhjuH2p7KC3rFmS_YGe30vLNuSiu-6QJceHZXk7hAvDdf0xliXmBxCDxu7sSDP_cj0Et1IuULHGPnJi-5_mby0)

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

| Link Examples                         | Explanation                              |
|:--------------------------------------|:-----------------------------------------|
| \[gematik\](https[]()://gematik.de)   | link to website                          |
| \[https[]()://gematik.de]             | link with direct url                     |
| \[gematik\]                           | link alias usage                         |
| \[gematik homepage\](gematik)         | link alias usage with different title    |  
| \[gematik\]: (https[]()://gematik.de) | link alias definition                    | 
| \[License](./license.txt)             | link to local resource                   |

| Image Examples                                       | Explanation                               |
|:-----------------------------------------------------|:------------------------------------------|
| !\[gematik logo\](https[]()://gematik.de/logo)       | image from website                        |
| !\[https[]()://gematik.de/logo\]                     | image with direct url                     |
| !\[logo\]                                            | image alias usage                         |
| !\[company logo\](logo)                              | image alias usage with different title    |
| !\[logo\]: (https[]()://gematik.de/logo)             | image alias definition                    |
| !\[local logo\](./logo)                              | image from local resource                 |
| !\[local logo\](data:image/svg;base64,iVBOR..UIH==)  | image from embedded source (data_uri)     |
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









