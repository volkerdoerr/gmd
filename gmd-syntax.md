# gMD Syntax

see also: [Examples](#examples) [Definition](#definition) [Todo](#todo)

## Diagram

![](https://www.plantuml.com/plantuml/svg/bLJHRjCm57ttLnZpaeu0xrITXZOXAgqIAjrJCCYbNXOjTIRN5KYnN_aZVeWluLmdned40rHAR9zxxl69xtMlJavPf_Vcdh5wSyDNl1UwQqKeUVz1MLLRzVJWRvkJypkrRpNmaR1ax0y1QMjpqCQLl7glrQ4nzKRPHsrboNVwE-2OWzn4cw1X79TibWfDyHmfHOyXUF4AyoeYVPmJAhqv7_VQOXN3moenXbMG2rYb_UB7VNsmmc-wGtFVQ8iFCuz-VLIr3alE4WnY8Iw45nVq-epd2vvVFtxY_P9-65Vqm_X9G9vao6z5VgjTurejuKcI9vX-8sXLKF1kU-lVjeqwHT82y49moJqlCkf1eeY4D6VH7Oa_G_u_xd2ZdBhRhlzp9qPbnauqh9q-vghDa6d5Kc3I00GD5KnLxfFEjFY1KtQYqebFIkdZwR-WunPKlTXwu6oxRzaK5jbF5IdlkivfEw8okUGCL6HNstEhBMgbC-EwCmwU24oTFGEfBR8q-Po8LCdB49oBP2mappcN9tCSNvTHLDadMZdC-xp0bKlE9kJgMhVjnoTbybsBUN_5wQJ4fP1BDjhBGfcKB24mTbP1RK-Yg4U8lHyNAn4M9N58C6r7fSHvqvJCTH6alXkd0CSmNSmH90-N-GP33fmKU3qBi2jj3lI7zHi0)

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

## Definition

```
gMD = {"eol"}, {Paragraph|List|Table}, {"eol"};

Paragraph = Indent, [HeadingMarker], Text, "eol", {Indent, Text, "eol"}, "eol";
HeadingMarker = "#", ({"#"}|".", ["#", {".", "#"}]|number, ".", [number, {".", number}]);

Text = {"chr"|Modifier|Link|Image}; 
Modifier = ("*"|"**"|"^"|"_"|"↵"|"-----"|"====="|"\");
Link = "[", ([Title], "]", [ [":"], "(", (URL|AliasTitle), ")" ] | (AliasTitle|URL), "]"); 
Image = "!", "[", ([Title], "]", [ [":"], "(", (URL|DataURI|AliasTitle), ")" ] | (AliasTitle|URL), "]"); 

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

## Todo

- Background for table cells and/or rows 
- Includes
- Attributes
- Spans
- CSS styles
- Class and ID attributes
- Language
- Insecure characters
- Backslash escapes
- Unicode symbols
- Tabs
- Pre-formatted text
- Block code
- Syntax highlighting
- Block quotations
- Block comments
- No overriding gMD 
- No HTML









