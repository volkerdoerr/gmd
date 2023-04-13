# xml2gmd

 - run: Thu Apr 13 10:35:16 2023

### config:

 - self_closing_tags: 1
 - tag '<meta>', ends_at_eol:1, is_key_value-pair:1
 - tag '<afo>', ends_at_eol:1, is_key_value-pair:0
 - tag '<abb>', ends_at_eol:1, is_key_value-pair:0
 - tag '<tab>', ends_at_eol:1, is_key_value-pair:0
 - tag '', ends_at_eol:1, is_key_value-pair:0
 - tag 'data', ends_at_eol:1, is_key_value-pair:0
   - attribute: 'state', value_constraints: AAA BB C

### input:

 - gemProdT_IDP-Sek_PTV_2.0.0-1_V1.0.0 [.html](gemProdT_IDP-Sek_PTV_2.0.0-1_V1.0.html)
 - gemSpec_Net_V1.23.0 [.html](gemSpec_Net_V1.23.html)
 - gemSpec_Kon_V5.18.0 [.html](gemSpec_Kon_V5.18.html)

### output:

 - gemProdT_IDP-Sek_PTV_2.0.0-1_V1.0.0 [.md](gemProdT_IDP-Sek_PTV_2.0.0-1_V1.0.md), [.html](gemProdT_IDP-Sek_PTV_2.0.0-1_V1.0.html), [.debug.txt](gemProdT_IDP-Sek_PTV_2.0.0-1_V1.0.debug.txt)
 - gemSpec_Net_V1.23.0 [.md](gemSpec_Net_V1.23.md), [.html](gemSpec_Net_V1.23.html), [.debug.txt](gemSpec_Net_V1.23.debug.txt)
 - gemSpec_Kon_V5.18.0 [.md](gemSpec_Kon_V5.18.md), [.html](gemSpec_Kon_V5.18.html), [.debug.txt](gemSpec_Kon_V5.18.debug.txt)
 - README.md (this)
