# gMD Syntax

Find the examples at the end of this document.

![](https://www.plantuml.com/plantuml/svg/bLJHRjCm57ttLnZpqeu0xqIRXZOXAgqIAjrJ2CXTlIvQcbHk9f1Yl_97_11VmZbkF2VINgYKs3xtt9FZU-rU7ZjjExDfxeNOBQ_bkUoLQMlbCzb_qLRlh3uyk9lgsBcrtjG6-438XNWc86tHR4tJPRBuRFIsQdPBRH-DBJEvDhy0XnpaHje8zSEOYqagDDLhfCnw3DwfTmhY0Ud3d6ZfrF5mXqNpjDyO2p2mueh46FFb766oOPnV3rkzUx3ABTjjTLyPYsqsZswnrplZSoaY3E9CdIcdplZwZkS7dh-__-3zbZ-Cv_nX_ARckQ0CtHVqigwwsg0CgkGAE_YW1Xy4PzpWxUh6VQmhVGnSsfmhMS91i4AbLw3zbzorxlJjQl6oh60x8SjXqPbzwiuOcNGc1aQD9dJgLEnc7tN6JVQIsP7AMevwvK9Ttx2GB9m8HmoSLVipcKeBpmAGygbjEsC7j8mkfG0LsSNggJOMNJ29STKs7JmHZ2Tu0hBXIPe-Ho95z78A9f4fvgFdb2kZEOdT9HGjTP6MdUPzMk1gZPn5Sd5bwlhhGJVfJeMy5t5MIbseCXV9tY2KID4I0Zn7o9_nG5CK_V3XL8V5kVBpZ1mAni-nbQWtfpJNdZn89p4Tm27yVFCaDnQJrKMwgf05DmRUJmBYqZHR_a7z0m00)

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
| \[](https[]()://gematik.de)           | link uses url as title                   |
| \[gematik\]                           | link alias usage with same title         |
| \[gematik homepage\](gematik)         | link alias usage with different title    |  
| \[gematik\]: (https[]()://gematik.de) | link alias definition                    | 
| \[License](./license.txt)             | link to local resource                   |

| Image Examples                                       | Explanation                               |
|:-----------------------------------------------------|:------------------------------------------|
| !\[gematik logo\](https[]()://gematik.de/logo)       | image from website                        |
| !\[\](https[]()://gematik.de/logo)                   | image without title                       |
| !\[logo\]                                            | image alias usage with same title         |
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

_____
_produced using the PlantUML generation service at https://www.plantuml.com/plantuml/uml/_ 







