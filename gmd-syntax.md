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
Modifier = ("*"|"~"|"^"|"_");
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

![](https://www.plantuml.com/plantuml/svg/bLTVRzis47_tfxXf0se5SO8-x2LfWmuhXWPeXo5hdzoqeAMpHPGYFPAgOrZkuxxHlj0-oUv8qP8CDsi3k9Bkpztl_joHVU6yi1uNUZcPJCzc8FGM7FxLe2xm77mbF9G67MZZeHQ-g8Y6uBRQYuTPYKkffPT6WtJWBGgF9GW7nfPI2xi5Zm_-0YPaD-eKNXP2gIqKnbeio3XwB5WhEOMwSHw4ScRe3skXIHLiez2TWo6YtKY78FsZhibpq4rkfKwElLWv49OihBInM5wSvPF9wirBU0wx38tAzkUmUosTRz-AXSBs3s75oefrnVGeS1rJLfYwHkqTX5J2HleAicUpZ79P0j8lKcOtaL883Gia90ujOyRF50g5Wm71mGtXkDKbsJs7-IiK5DJgZR2VqDwVmrjy8780GM2Is82wxvuTGXaaOcON63CgQeIbiK1f0INrgQocp0036s4WSDcFv7kweyT-0gV-MjtK2xI4v88av-bh5pxZr_x-AwhPJrdIezUaHAzVqyYxI4NZJIsuKw87GWoBBJIENoWyjW55HKccfhDS14znWLa2DKaZLAVcGYqueHGfTO7-rDxMOeNjAsFlg0Lj-pjkY8njzYoZp8iLeRl9MdfvUPY9zeqfvLAISFQUqHULpThmR-gSnf5DTjxeC4fOnhQKOTwuD6Q39JSnDsOb7Amj9adk9OlKH9yxDPOB9UGlw6VJfPRRMEazQevQbh4DIbCqtBnWE1c5QaeoDXthiwV4x2O_mDkY1xV6WcCiSt8-05TteSSH8nwwGgonx7FlO4ho1I9vv18zUVyaP-6JippG4c6WbEA0yA53lBIcJj245chhf0jTowNZPfrpixwLNY4LuZxqrLL6anJADtrtzxhzHKdXWaGUQWajJ7jQIo9vKCsluQXuWgN0inXeYYSIXWb4vJ2CEALndFOf4GXyBC02AvhKqRwbaFCGI6W_ZkG70lmDuRmKNhoxk_s-i5B3afzfTaRD-eL-7-ZtCKi3riyE2N2ZBXcuKJH3-j8ibsJi_PS3GthAHT6pFXmuhk4nAwnS-vxzSSWUCSCyfk4By6RyHz2Uyzy1dgSCXdLs1LaGuDvZU8aOf8d6LL2eLrM_5l610eEV1yt6Jhj1vzJ_-_S_l57vKA1FVjnwhFj5t5EEbt3Y39Owa-8oJPjxbmmD5pglYbwK8n-irLQXz-4zp-BEd3ALll8sr6-M4ZDURqZpJ6YkuedbmW7LiIZxl7N2JB8BFhoJib3hIYmmdAKd332OOmDvCD2lvSS0K037tgzvxrYCnokNh5iPlCqbPvgdJ3Gg75TFnwwEuVwlk_pxt8dWRj4eYXiKbUZ8_1ctMIbSXUKfzYmBSysN2swkExFf6ua--XwQ1v7VZA7aTjJxxiapIxAaFW-3mOtQY_ngjAT88d57iz-nHfnzMcSrXILdF2LWpIRkxRLnJf9pJW-deo0zIQt0Isqss0Hyi_510dKuJ0MBieimTl42CGY3u-tnpXEio4nuZsdx1B_NXPG8e2xlgJIgBKU9IWNYUVpUZGayMOD49AqvI_sv5hg_PmNba_HqaACeAYX8W8_QuJsG4w4SQLroKkavE1R2JkFunh1tHMNtmVfXfo4iOzv2UQJhpttUbSl6DnQXSSW66MQ_9QzuGyP5GCkXVzrrh-He9DIv563PH8o1U8ET60F0C1ynPB4mdv6Fwmf5YJOGBoR7HcRVQ4GRMmjrsWWX7MaA9LUQfpNTP8EQWmNILCEqeMvLKN2zHlAjYt1WCqLJ2OzCv-nFuTBFWjsho1vFxHKLoCfLTIH3RJ-KA0WIsfDcX2x7qkoqbWzOzXSAJZZ9SSwEhuAfmjo8eS2N_TtwFepIpO1m3-sOaEx9gIkFTjBDU2Dodg8YeoALfjQKU0EiUasu4hT6GOod70gr-Gd3buyP9fL7hNBCBoXd_9_K_m00)

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









