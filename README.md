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
    - "Design Item ID": Use complete component name (use reference from Ordering number of the corresponding manufacturer)
    - "Designator": according (example: IC uses U?, resistor R?, and so on)
    - "Comment": keep blank
    - "Description": use Digikey based description, try not to use strange characters as degree symbols
    - Use grid 100mil
    - Pin lenght <= 200mil
    - Use same pin names as datasheet
    - Add Parameters names (if exists):
      - "JLCPärt" and search if applicable JLCPCB part library code exists on https://jlcpcb.com/parts
      - "Digikey_PN" and search if applicable Digikey appropiate part number code exists on https://www.digikey.com/
   - Add footprint when done (or use existing if applicable)
 - On the PcbLib entry:
    - Name using component manufacturer name (same as symbol "Design Item ID"). Exceptions can be made, for example for Texas Instruments footprints, where they have a complete defined code.
    - Layers: Name: TOP - BOT
       - 3D Body: 5 - 7
       - Assembly: 8 - 9
       - Courtyard: 4 - 6
    - Assembly layer uses a rectangle drawing with the component maximun dimensions excluding leads
    - Courtyard layer uese a rectangle separated approximatly 10mil from Assembly drawing or Pads (wichever corresponds to that side)
    - Silkscreen drawing and width according space, the clearance from pads is 10mil
    - Pin 1 dot indications can go outside the Courtyard if needed/requiered
    - 3D Body should have a 3D model from wherever; if not, place an extruded from Altium tool
- Compile .LibPkg
- Commit changes to dev branch
- Wait for review
- Make changes if needed
- Wait for next review/merging to main
- Enyoy
