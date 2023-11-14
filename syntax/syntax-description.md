# gMD Syntax

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

- Bulleted (unordered) lists
- Numbered (ordered) lists
- Footnotes
- Endnotes (auto-numbered notes)

## Links 

EBNF: 

- "**[**" → _title_ → "**]**" → [ "**[**" → _hint_ → "**]**" ] → [**=**] → "**(**" → [ "**img:** "|" **inc:** "|" **email:**" ] → _url_ → "**)**"


- Links:
  - with title: \[Title\](https://www.gematik.de)
  - without title: \[\](https://www.gematik.de)
  - with title and hint: \[Title\]\[Hint\](https://www.gematik.de)
- Image links:
  - \[Title\](img: https://www.gematik.de/logo.png)
  - \[Title\](img: ./logo.png)
  - \[Title\](img: src="base64")
- Email link: \[Title\](email: info@gematik.de)
- Include links:
  - \[Title\](inc: https://www.gematik.de/LICENSE.TXT)
  - \[Title\](inc: ./LICENSE.TXT)
- Alias links:
  - Alias link: \[Alias\]=(https://www.gematik.de)
  - Alias link with hint: \[Alias\]\[Hint\]=(img: https://www.gematik.de/logo.png)
- Alias link usage:
  - Alias link with title and hint as defined: \[Alias\]
  - Alias link with different title an no hint: \[Title\](Alias)
  - Alias link with different title and hint: \[Title\][Hint\](Alias)

## Images

- Image with title
- Image without title
- Image with hint
- Image scaling
- Image from another domain
- Horizontal and vertical Alignment
- Image from a remote service
- Image alias
- Embedded image

## Tables

- Header
- Footer
- Spanning rows and columns
- Vertical alignments within a table cell
- Horizontal alignments within a table cell
- Background for table cells and/or rows 

## Attributes

- Alignment
- Indentation
- Spans
- CSS styles
- Class and ID attributes
   






