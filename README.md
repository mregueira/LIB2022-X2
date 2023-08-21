# LIB2022-X2

## Description
Library repo for Altium components

## Instructions
1. Clone repo preferred on C:\Users\Public\Documents\Altium\AD21\Library.
2. Install libraries with the Library Manager of Altium. Select the .IntLib files from Outputs folder.

## Component Types at 07-06-2022
The added components start are based on necessity
- Connectors
- ICs
- Optoelectronics
- Passives
- Relays
- Semiconductors

## Adding new components
 - LibPkg:
    - Name: LIB2022 - [Component Type].libpkg
 - SchLib: 
    - Name: [Component Type].schlib
    - Use grid 100mil
 - PcbLib: 
    - Name: [Component Type].pcblib
    - Layers: Name: TOP - BOT
       - 3D Body: 5 - 7
       - Assembly: 8 - 9
       - Courtyard: 4 - 6
    - Separate Courtyard 10mil from Assembly drawing and Pads (wichever corresponds)
