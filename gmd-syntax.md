# gMD Syntax

- [Definition](#definition) 
- [Graphs](#graphs)
- [Examples](#examples) 
  - [Paragraph Examples](#paragraph-examples)
  - [Heading Examples](#heading-examples)
  - [Link Examples](#link-examples)
  - [Image Examples](#image-examples)
- [Todo](#todo)

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

![](https://www.plantuml.com/plantuml/svg/bLRTRjku4hxFKypHEK3j84xGYtEJj44FJh5eW7QnoBPNILhGrDWYIf5UaceIMCxblj6-q3x9pep4IZACeFM59StFp3S_C-IRc5H8k7IhewFPyGAKUuI8VpJeD9v0gbI2qcC4vnFKAkcAQ0ZnqINri2XnPPn9nZim4L90bR045S67qZWL7Y7XGpg58xBRwUXajBBs4RGF0JKPnuIQjR9Jg9kOGDden_wmLevK8JGMumbu8ePx4n5CUjOrUHRTxDQux3YfTGGLoCBQ-O3bwV7yw6ZzuIsyXcs1tXQx4zY-Dp6r7zNIOlkR2ceTrAPYUYTmqQLC-xf6bo98Ak7Uf0gALui2b2i1NTbJ5fSTHIi7IoGa4GDZncyK2eM3Wk2x6y9nvKgoUm8txr1HKEiFAdp5S7S27_61o0A2m6In4NNNFtk4HYGai-nQCgfgX9KFG6a1QzoXhERC00ERO21mnR_9zsnBZrthcdg9WNoU4kqcVstbi_lQtRN5VueiGQ-PJQ-xktcFKpN9ruhht6cHFrW-GXFfHL2JDEXA1QKJ1avX8bJWLq0bRfJjrQ9aajD1EAc6xcjxLQirjkzyk6uiXlPNl2SojiMhWlAcreJZicZfvUttZcu_-DAi30aNjunJLw5evJ_NlObaavqtJWO1owwfZ4mB9zRVOyajo6rLgGYRW5cIEo5WnF2jLsCvAG1_mJ1PCJVCVJ0feUEeJTaLiVIwuTO3pydGjYd9s6ogBvuwPfvRWVU82U86DSTOpiavHgqsM0xvZJ0Zm1gHh78PNjo-cFF479gsiPQIbhUMGUD3ZseLV9tTAwViOpHH-ehBm-rqm-tqqIIBbEmxwPBpWdfTIZJxTFs-_PyrAeh4NEe5BSm6MaiYSr6TNy1UWHHBGM8nS1HFHnWd2Mr46K9ArJIrC-COV9Va9LOqIvEDI27F9H1fCOxaNmJu1y9vgvBwT7trSs7bfYG_i-Buc3howOd-Fd-clozVYZn85C6mK5cEctB50NXRWdTdVhKYexTFjq_VMIPHLlJ099kP5HkUAXtC9WrySZVYJxWoVtdO1Eg2VuJnDVz6C8sJvNFUptX1M_D8wFhhbF6w43g2HRUkXbs63qed-E-e_zXtDzzIZR___8lN86zo-kJ7LS9ws9u3PNzpPiwmYKMzsu1vtMwpeV4MvWqnY782HXkojPYIlC-BRYdEc4fVyxRWYYvoVgPR3KimXEQyEsQYd2ezYueWoqR6b8pnYPkLbTrKQebo01umm63s3Sp5mB2DdmD00Unxl-1r4r3EH2bPlqMuZaOoJOEd6YjdpCkfgmdS7t4t_pbtIjmj6qjnWwKIxPa_vZOhLQomFCHU53BgSYEWibxx-w6HXeyTJRk8_EAzL5geT_sJnvXaIVr6veCRTH3vltU98kc8Mre7FMl2sUKDLrDOPi630i7VT_UPZO_Ha7DAZwH3avvnZU8zjnWEJzuqAea4EZb35UZEXKnUT-gFmk1u1xmt6LR7p7ZtQRiCVz25d0YWBX-eDAejHudM2l6a-zvE2JnPEH4ZhHkM-dsZt70v4kM3z7n-ez8LQ1AG4tQul4aYR2IjCqugFKSdXQos8RuCOAkhi1Fhemsy4Z799fWu7FUyCbTDQW924v4DCinXMPxpekmM0Is7uNNRlvAZYL3lKa4G4n83ySPdiWI0tNn8o6hflo6Vu1Mg4eCGJu_sZIn-q8ZpeLRsi152Ej5KrgmTJsk-VefQX2NILCEiSSdOJd2pGVBjj9pXJ75KmZtJS_PdSPKMOlUyOq-dzfmA5CowsfD1LuubD472SD2CSkLKcftMvW7BuOv12HSvojd-3J1Nc1jH2dmsN9FlP9GkHuGxQAS4o0Nkkt9l9rrEDwBaIHGP5QaqjQF4Us3L2yALkJKgOhpaKAZD3nW-UyumgJnhbMD-Gpd3fLlz0m00)

_produced using the PlantUML generation service at https://www.plantuml.com/plantuml/uml/_ 

## Examples

### Paragraph Examples

|                                                              | Explanation                          |
| :----------------------------------------------------------- | :----------------------------------- |
| The quick brown fox<br>jumps over the leazy wall.            | multiline paragraph                  |
| &nbsp;&nbsp;The brown fox<br>&nbsp;&nbsp;over the leazy wall. | multiline paragraph with indentation |
| The quick brown↵ fox jumps over↵ the leazy wall.             | paragraph with manual line breaks    |

### Heading Examples

|                                             | Explanation                         |
| :------------------------------------------ | :---------------------------------- |
| # Section One                               | heading h1 traditional form         |
| #. Section One                              | heading h1 with automatic numbering |
| # 1. Section One                            | heading h1 with manual numbering    |
| ## Section One One                          | heading h2 traditional form         |
| #.# Section One One                         | heading h2 with automatic numbering |
| # 1.1 Section One One                       | heading h2 with manual numbering    |
| ### This Is A Really<br>Very long Heading   | heading h3 spanning multiple lines  |
| #.#.# This Heading Has↵ A Manual Line Break | heading h3 with manual line breaks  |

### Link Examples

|                                         | Explanation                           |
| :-------------------------------------- | :------------------------------------ |
| \[gematik\] \<https[]()://gematik.de\>  | link to website                       |
| \[https[]()://gematik.de]               | link with direct url                  |
| \[gematik\]                             | link alias usage                      |
| \[gematik homepage\] \<gematik\>        | link alias usage with different title |
| \[gematik\]: \<https[]()://gematik.de\> | link alias definition                 |
| \[License] \<./license.txt\>            | link to local resource                |

### Image Examples

|                                                    | Explanation                             |
| :------------------------------------------------- | :-------------------------------------- |
| !\[gematik logo\] \<https[]()://gematik.de/logo\>  | image from website                      |
| !\[https[]()://gematik.de/logo\]                   | image with direct url                   |
| !\[logo\]                                          | image alias usage                       |
| !\[company logo\] \<logo\>                         | image alias usage with different title  |
| !\[logo\]: \<https[]()://gematik.de/logo\>         | image alias definition                  |
| !\[local logo\] \<./logo\>                         | image from local resource               |
| !\[local logo\] \<data:image/svg;base64,IVBORUIH\> | image from embedded source (data_uri)   |
|                                                    | image scaling                           |
|                                                    | image horizontal and vertical alignment |

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









