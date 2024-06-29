# LIB2022-X2

## Description
Library repo for Altium components

## Instructions
1. Clone repo preferred on "C:\Users\Public\Documents\Altium\AD21\Library".
2. Install libraries with the Library Manager of Altium:
   a. Go to Components, click on the indicated symbol

   <img src="/Images/Lib-01.png">

   b. Click on the "Installed" tab, and then on "Install..." button

   <img src="/Images/Lib-02.png">

   c. Select all the .IntLib files from Outputs folder and click "Open" button

   <img src="/Images/Lib-03.png">

   c. Close the dialog box

## Component Types at 29-06-2024
The added components start are based on necessity
- Connectors
- Crystals
- Devices
- Filters
- Fuses
- ICs
- Mechanicals
- Optoelectronics
- Passives
- Relays
- Semiconductors
- Switches

## Adding new components
 - Create new branch
 - Open the corresponding .LibPkg
 - On the SchLib entry:
    - Use complete component name
    - Use grid 100mil
    - Pin lenght < 300mil
    - Use same pin names as datasheet
 - On the PcbLib entry:
    - Layers: Name: TOP - BOT
       - 3D Body: 5 - 7
       - Assembly: 8 - 9
       - Courtyard: 4 - 6
    - Separate Courtyard 10mil from Assembly drawing and Pads (wichever corresponds)
    - Silkscreen drawing and width according space, the clearance from pads is 10mil
    - Pin 1 dot indications can go outside the Courtyard if needed
- Compile .LibPkg
- Commit changes to dev branch
- Wait for review
- Make changes if needed
- Wait for next review/merging to main
- Enyoy
