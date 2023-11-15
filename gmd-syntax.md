# gMD Syntax Documentation

_The Ebnf diagrams produced using the PlantUML generation service https://www.plantuml.com/plantuml/uml/. 
For getting the sourcecode of any previously generated URL you simply copy it itnto the URL field 
and click "Decode URL" at it's right side._

![](http://www.plantuml.com/plantuml/svg/dLJHRjCm57ttLroyboRBnWTKGvk6q2fD29NjAGd8MztM8hqfZikGclB81y03dm18V1LVmhbDcYgKbp4fTxRlESVdNjizhuBnmTxnLAbNnfkPDyivdL4wuedba2VqmlagN3ks2QtRLHh4CszDi9vAJ_RzoXGPXxbXcWgOt1OLHs1VbXmShqnm9Ol89Y5joq8FLQShkrrPCt4y0o6zADoC5-3BvCP-bDsufA91q15aEus_rI6r5aeBs0oLwkGaftz_-wvhn1yIVttPng-2Qmq0f8zq0kGf8eRYjrhUOo_H5GtiywuUBSpCrZg6m5jyR_1z4h7FFn4peTxFFOQ8K2UbX2NYAN8ftRXGsAQkD6D64_Cu8gaht-PJVQO7CThexj7bAcF77rpbxa0oXJDOcDYfOoTrD_qOW3Uu7L_N5vBVwaFUsabroCZO5fLzc5jluoW2ETAKm-IsA37vH2UFSphw7wVFJJ2tur7FySl7EKPRApaK-UU2NU3WTiFTHQEXsYq1sDnV6E3LuivwO4vrSup7-4vqr1vtGljhX8cY_T-Q3Xw1NFsC-tS_eOExc_5nGYS9nLJwZ1i75P2jqGsigXk3ri7ek7n0COZTWo656JAwbiPVZTlr7B3BiaXa7TXKFzDjfl_uGCxtKlrC9xlUUwx5c6WE0Iu0w3zCa5ul3SiGwNROOwEODYFguYhjcYujpeTIq2x_z5zvfSujJ-J7wGy0)

## Examples

| Link Examples                        | Explanation                              |
|:-------------------------------------|:-----------------------------------------|
| \[gematik\](https[]()://gematik.de)  | link to website                          |
| \[](https[]()://gematik.de)          | link uses url as title                   |
| \[gematik\]                          | link alias usage with same title         |
| \[gematik homepage\](gematik)        | link alias usage with different title    |  
| \[gematik\]=(https[]()://gematik.de) | link alias definition (always invisible) | 
| \[License](./license.txt)            | link to local resource                   |

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
- Line breaks
- Tabs
- Pre-formatted text
- Block code
- Syntax highlighting
- Block quotations
- Block comments
- No overriding gMD 
- No HTML

   






