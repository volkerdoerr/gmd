# gMD Syntax

Contents: [Definition](#definition) [Graphs](#graphs) [Examples](#examples) [Todo](#todo)

## Definition

```
gMD = {"eol"}, {Paragraph|List|Table}, {"eol"};

Paragraph = Indent, [HeadingMarker], Text, "eol", {Indent, Text, "eol"}, "eol";
HeadingMarker = "#", ({"#"}|".", ["#", {".", "#"}]|number, ".", [number, {".", number}]);

Text = {"chr"|Modifier|Link|Image}; 
Modifier = ("*"|"**"|"^"|"_"|"↵"|"-----"|"====="|"\");
Link = "[", (Title, "]", [":"], "<", (URL|AliasTitle), ">" | (AliasTitle|URL), "]"); 
Image = "!", "[", (Title, "]", [":"], "<", (URL|DataURI|AliasTitle), ">" | (AliasTitle|URL), "]"); 

List = ListItem, "eol", {ListItem, "eol"}, "eol";
ListItem = Indent, ListMarker, Text, { "eol", Indent, Text} ;
ListMarker = (number, "."|"*"|"+"|"-");

Table = Row, "eol", {Row, "eol"}, [TableFooter, "eol"], "eol"; 
Row = [RulerLine, "eol"], ContentLine, {"eol", ContentLine}; 
TableFooter = RulerLine, [ "eol", FooterLine, {"eol", FooterLine}, "eol", RulerLine ], "eol" ;

RulerLine = "|", Ruler, "|", {Ruler, "|"};
ContentLine = "|", [CellSpan], Text, "|", {[CellSpan], Text, "|"}, [">"];
FooterLine = "|", Text, "|";

Ruler = [":"], ("---", {"-"}|"===", {"="}), [":"];
CellSpan = (RowSpan, [ColSpan] | ColSpan, [RowSpan]);
ColSpan = ">", [number];
RowSpan = "/", [number];
```

## Graphs

![](https://www.plantuml.com/plantuml/svg/bLJHRjCm57ttLnZpqeu2xvHEGviGbLO9bUuf1EHIBukMEfFh2QJOh_mHFyINSAwJYnE91rOfiNtkkSSdljUzE7djlDdRMo6gpPLSoKwPjb5n8RkFskdAwOUxS5sVVDZfVME03uIb47y9I5lRWx5-8OiFHXzgMssqkpUkNCYT-G4uvI2NQICq3kDIJ5AXgPuZPTPXY46zmhn8I9VcX9R1FXxtnc6Lmhpg6VqgbdDOfVtIntsxSofisaDzMnk73xFtONtKbObBAHW6SQREL51dzFg2vokUtpz_uVsIVXXNzCFuMK6UPCXlGNvtjMyC79N9y1jLOlwM0ZVRw_2kgVKfCUQ0pvKCSfQn00hX9KIbIBv8zXco_qFxIdjzirq_QGz1fSKUDAozEUPAJP5HbJWmAZf1VTMuiXthZ0iU9MKpbKvvLBwGJlm57R5A5QDs0sVRVi-ciCX-YaHvtxRUk04jsQKKe2Axs3usng4-9ZCkM-lXYK3kvWb8hP2boUT8f60lVJ2BJB78ddEkP7Cu1P5Hr3SmRT7Fkxp0DHivOt9nQPhcquEs-Nwbl7_YT5BeWd8fihr1A9FO4W93NyserKaKzOYftzDYfU8yzHu9ydPKIfmtJSbSstj0tmrJW4EOBkC0aeVpV6iX1mu7Nay2uiBO0_r9_G40)

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
  - The syntax is not yet clear
  - comments can be inserted everywhere,
  - they are invisible if the document is rendered 
- No HTML
  - html-elements cannot be used in a gMD document
  - due to the possibilities given by attributes, styles and tagging this not neccessary









