# gMD Syntax

Find the examples at the end of this document.

![](https://www.plantuml.com/plantuml/svg/hLJ1ZjCm4BtdAmPpIKA0Ewj5YtOFLEeYL7PFJK1kEssiTPtYk2eepfK_ueVu4cQSEhlL8h58L4fipxnvVfu-vw9rqZfSc7MIRAwlu1mwWOqMVG7THsdbnifTxQUgTVv6BZHoV02S9Sa8eBA9MQ5n1SpVermfixcMzWvjLS0DVdEGvjWkvGv13zdIrCC4jW7Nvba1WPVu0nNNR2nAXnOQ2_XrBtLfN2qDh9Lj7QY0uZhUuLZT7qVUqAnQE2XNbmQtE_STj3AOPsV9YK1IBfxJfcb7G-_5AvhFGwGBSuvMNhIx9ItCVhj0Iy60YYi6nbnVaPw0flQmBcxeL9axFzdA3VhhPgNM2gqNozfI3o7X98kOCoNSAATnw1QjgZo3YlWgpf6iDoBDfLQoBUdiQsMKKut9CuQaV8RRsTI_utoWINE3I3ruL44DqIqUQhJK3zQR2QX8If38Mfw9uly9kf9Etiuc9y8-_9kms3NIbefSU97pwpCzN-ZvzUCdlL_oZyPp_j5O2lgh4pOkLV4mSRYzzzWOURflOia3itDey55qOHTtU6HYjcvf_kJTyNQKPhmUceMFTmDw6FOVJPi-yA8FFNd1JGY73XULCBFcG8Be_OJJGK8ugfdFzXhjb8B7cgg0oyOuail1UFjFWf6UIM8rsyWJB0IAOTwD2_vwZ0JtuFabQlrf9yt9PmDydaM6lo1wlhnlHNKs225UzYXXK_O74r2B-c2Ii3WNFHKIXaiYDNUNci5JbjGC-u67OSh1OtgyxC37YSKaOFmw42rXO-BrIIAvGBFYB-zl)

## Examples

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

| Link Examples                        | Explanation                              |
|:-------------------------------------|:-----------------------------------------|
| \[gematik\](https[]()://gematik.de)  | link to website                          |
| \[](https[]()://gematik.de)          | link uses url as title                   |
| \[gematik\]                          | link alias usage with same title         |
| \[gematik homepage\](gematik)        | link alias usage with different title    |  
| \[gematik\]:(https[]()://gematik.de) | link alias definition                    | 
| \[License](./license.txt)            | link to local resource                   |

| Image Examples                                       | Explanation                               |
|:-----------------------------------------------------|:------------------------------------------|
| !\[gematik logo\](https[]()://gematik.de/logo)       | image from website                        |
| !\[\](https[]()://gematik.de/logo)                   | image without title                       |
| !\[logo\]                                            | image alias usage with same title         |
| !\[company logo\](logo)                              | image alias usage with different title    |
| !\[logo\]:(https[]()://gematik.de/logo)              | image alias definition                    |
| !\[local logo\](./logo)                              | image from local resource                 |
| !\[local logo\](data:image/svg;base64,iVBOR..UIH==)  | image from embedded source (data_uri)     |
|                                                      | image scaling                             |
|                                                      | image horizontal and vertical alignment   |

## Todo

- Table Header
- Table Footer
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







