# gMD Syntax

Contents: [Definition](#definition) [Graphs](#graphs) [Examples](#examples) [Todo](#todo)

## Definition

```
gMD = {"eol"}, {Paragraph|List|Table}, {"eol"};

Paragraph = Indent, [HeadingMarker], Text, "eol", {Indent, Text, "eol"}, "eol";
HeadingMarker = "#", ({"#"}|".", ["#", {".", "#"}]|number, ".", [number, {".", number}]);

Text = {"chr"|Modifier|Link|Image}; 
Modifier = ("*"|"**"|"^"|"_"|"↵"|"-----"|"====="|"\");
Link = "[", (Title, "]", [":"], "(", (URL|AliasTitle), ")" | (AliasTitle|URL), "]"); 
Image = "!", "[", (Title, "]", [":"], "(", (URL|DataURI|AliasTitle), ")" | (AliasTitle|URL), "]"); 

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

![](https://www.plantuml.com/plantuml/svg/bLJHRjCm57ttLnZpaeu0xqITXZOXAgqIAjrJ2CYbNXSjJIRN4qYnN_aZVeWluLod5xk21rOfiNtkkSSdljUzE3XjdTdqjqBibbToBaTbXaw5KeuVjDKxgn_k_7LxS7wjDvqXV29KGlmX86tHRqtlIbc_DthRzhkbjlV6DgLSc--0OmvocPQXuJXMuYGLckevKeeHG_3g5UPrHCOu9xJn_UD-OonMCSohYJ6jGZE3LTelVjpNEwlySjYsjwsn-B3-tY_sUcT29GN381RgJ7brHg_FUBxW-VNZ9zulwOTnJZ-CdnJaIORyrkHttRhEm54J3RzH3UO51MvMr_vjr-f3PCm0pvJqiaYO1uNm1g9IH5ya-qoL_wDzfPs-MIsUj8UWqc8F6XREx5Eb6FchIXp8YaxGL3MkxCWwUS63h4IYqYbdvVFnn5_G4IkgM6mtS5R3jsGgBU2dZfHtm-2CFQ8DkvG2L6JNgyVEMDJ79CRbq3ju8f2xEGTZAsJIv269rEnb2kOYEHROSygLR0wd81AA-dgcbTDyJ8jG2NQMaUjBqtKV7tIVxbVC-oTE9wNELLC9jiT26OajoJdtLK6jJgAeHuZz7XTp5MQnzqYGjwDIuhnfIkQ6oOFqagOJU0pJPJo2vE4ytLh8WSE1roS1SM7wBVr9_GO0)

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









