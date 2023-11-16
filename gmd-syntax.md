# gMD Syntax

Contents: [Definition](#definition) [Graphs](#graphs) [Examples](#examples) [Todo](#todo)

## Definition

```
gMD = {"eol"}, {Paragraph|List|Table}, {"eol"};

Paragraph = Indent, [HeadingMarker], Text, "eol", {Indent, Text, "eol"}, "eol";
HeadingMarker = "#", ({"#"}|".", ["#", {".", "#"}]|number, ".", [number, {".", number}]);

Text = {Link|Image|Tag|HorRuler|NewLine|"\", "chr"|"chr"};
Link = "[", (Title, "]", [":"], "<", (URL|AliasTitle), ">" | (AliasTitle|URL), "]"); 
Image = "!", "[", (Title, "]", [":"], "<", (URL|DataURI|AliasTitle), ">" | (AliasTitle|URL), "]"); 
Tag = "<", (Attribute|Style|UserTag|Comment), ">"; 
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

![](https://www.plantuml.com/plantuml/svg/bLHDRnCn4BtxLnXpoK8ATqAgLgbG8wK8fUbfsOD3JBhgVbIEeuBMllAF-4Fy4jxO3Du83X1fk_QRzyRFCxEzE3XjdTbsduNOtrp9kHoKwHiLfdBueAtUM_ruxrVrmVcDtZQ6y4IO2V6R0DcosvdEJMLvRVIkxlOtsZuOMqtbndm173NGCcs4Xb_lcJYH8gTw3ibam2juzGhhCY93N1DQ-UxORet5BeRJZXbf5we2LkaykjogxXxyijLxW_li_NLlryV6MF_UF25alFf8gJ_TM-NfBrsJ96Ic93ERsZK6Z2gwUQCghDzIu6wzyfTDhG-HKG0-LzBBISOyA4MK5ZCfeWTA-mpgVyXzfPs-Mo__wmpS42Ua79VEsNfxTCRVkgz4F1XB5LZqROkEf6JGS4KWdAWp-g4IS_eXfKXbYhv_VFkkK5WQ3MpfjNIcpPrcv8ykSs0qD0IbhlDa39ndF311afgfv73KVgzUu7c9vuoSYZYkuApxfsmAc-odZ9HtVU-G8g4LkvG2LAZBM0owSsOi-ix1KmA7Y9w00UfHQlAGavJi9GLFasGiiEUibMnEudOPHIiyqwPfFUGDvfUTZSZbmZJDxQFkylSPTN_5gLAOZMecs5vEDE0R2P75dX19ivl6XpXeI8Wp53Tp5OeqtyZ8vr4lKN1Qahi-cS1ifoM152Qme1knI9tdpnxfmE70wvE0k33TZlxB_GG0)

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









