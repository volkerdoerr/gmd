# gMD Syntax Documentation

_The Ebnf diagrams produced using the PlantUML generation service https://www.plantuml.com/plantuml/uml/. 
For getting the sourcecode of any previously generated URL you simply copy it itnto the URL field 
and click "Decode URL" at it's right side._

## Preliminaries

- Language
- Insecure characters
- Backslash escapes
- Unicode symbols
- Line breaks
- Tabs

## Block modifiers

- Paragraphs
- Headings
- Pre-formatted text
- Block code
- Syntax highlighting
- Block quotations
- Block Indentation
- Block comments
- No overriding gMD 
- No HTML

## Lists and notes

![](http://www.plantuml.com/plantuml/svg/BO_1IiOm48JlVOfXJpL63rv5-17qw1C496bNAJJRqjs2KdrtD_O_BCjaC_Cn5xMy6HVvwBgNvxTNF64ohX57MxzuxDfkhpAoM1-oOPw4a_mRmqr4Btijl4NGFVrGyBdrkIC_aQu3HHX_cGjUPXS7nENxcOS-QAwCh5T0J59sGwDmLiD3ahfi35tpmEgu5jPiVXud-OG3KNSrzp5OXxpoYF8DIe7y-qb5At9X9tZHFm00)

| List Examples | 
|:--------------|
| * Item 1<br>&nbsp;&nbsp;- Item A<br>&nbsp;&nbsp;- Item B<br>* Item 2<br>&nbsp;&nbsp;+ Item C<br>&nbsp;&nbsp;+ Item D<br> |
| 1. xxxxx xxx xxx xxx xx<br>&nbsp;&nbsp;&nbsp;1. xxxxxx xx xxxx xxxxxx<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;xxxx xxx xxxx xxxx<br>&nbsp;&nbsp;&nbsp;2. xxxxx xxxx<br>3. xxxxxxxx xxxx xxxxxx<br> |

- Footnotes
- Endnotes (auto-numbered notes)

## Links 

![](http://www.plantuml.com/plantuml/svg/PO_DQiCm383lUGgXYt_86un0DjXWbxo0ROOJAynWb18hj8K-V9FGMqywVDydeRvAN8L6dfllh-47Ea27BJYGB8Mq_UGx2DsazJnk0iefY9n01UMPwXGlb40Mp-WTdWHzG6iWj83XNEImGsr_EUKf2bNFiUIuZqHpvYnvOMiEM--stjRoEFdVw_v0b2gy9PwfLBh-qqhMcBqs2E43cfuu7Syy0G00)

| Link Examples                        | Explanation                              |
|:-------------------------------------|:-----------------------------------------|
| \[gematik\](https[]()://gematik.de)  | link to website                          |
| \[](https[]()://gematik.de)          | link without title                       |
| \[gematik\]                          | link alias usage with same title         |
| \[gematik homepage\](gematik)        | link alias usage with different title    |  
| \[gematik\]=(https[]()://gematik.de) | link alias definition (always invisible) | 
| \[License](./license.txt)            | link to local resource                   |

## Images

![](http://www.plantuml.com/plantuml/svg/PO_DIaD138NtVOgOpVpGDv125HJSz0LcXf9sKXmOKfd9HONxyCQBEpV98by-pZbEfQ5yaTlkvVdq2WV01zm39Xi9j6bd7v_a6vI_T9_biYYuv82aWYik2yyhVN05lMV1d72xO2uO0nGJbKsKy80-labjLrAUMQWtibNvrgHfkqiClxGtsY-ZhvMKpijewmQU_uAScEk4Vx-Mea_-VEV1CGJJ18Jo2BiZ6sJLVW00)

| Image Examples                                       | Explanation                               |
|:-----------------------------------------------------|:------------------------------------------|
| !\[gematik logo\](https[]()://gematik.de/logo)       | image from website |
| !\[\](https[]()://gematik.de/logo)                   | image without title |
| !\[logo\]                                            | image alias usage with same title         |
| !\[company logo\](logo)                              | image alias usage with different title    |
| !\[logo\]=(https[]()://gematik.de/logo)              | image alias definition (always invisible) |
| !\[local logo\]=(./logo)                             | image from local resource                 |
| !\[local logo\]=(data:image/svg;base64,iVBOR..UIH==) | image from embedded source (data_uri)     |
|                                                      | image scaling                             |
|                                                      | image horizontal and vertical alignment   |

## Tables

- Header
- Footer
- Spanning rows and columns
- Vertical alignments within a table cell
- Horizontal alignments within a table cell
- Background for table cells and/or rows 

## Includes

## Attributes

- Alignment
- Indentation
- Spans
- CSS styles
- Class and ID attributes
   






