🏎️ Micro-Mouse 2025 – Power PCB Design (EEE3088F)
 
GitHub repository of the Power PCB which was designed and built as a sub-assembly of the Micro-mouse EEE3088F 2025 UCT course project.

This is one of the first-semester lab sessions, in which groups need to design, simulate, and prepare the production files for the power subsystem of a maze-solver micro-robot ("Micro-mouse"). All that will be provided as documentation, design files, and usage instructions is detailed below.
 

📁 Repository Structure
 

Filename	Description
PCB_UCT-PCB-EEE3088F_2025-04-25.pcbdoc	Altium Designer PCB project file – Editable board layout
Schematic_UCT-PCB-EEE3088F_2025-04-25.pdf	PDF export of the full schematic for report and verification
UCT-PCB-EEE3088F_2025-04-25.zip	Zip file archive of Gerber production files (for ordering with JLCPCB)
 	
---	
 	
## 🎯 Project Purpose & Context	
 	
Objective is to design a low-cost, small Power Module for the UCT 2025 Micro-mouse board. The board delivers, switches, and manages power to the system; features battery charging (multi-mode), manages USB-C power in, and supplies interfaces to power four motors with external high-side load switching and systems telemetry.	
 	
NOTE: Don't need to design the entire Micro-mouse! Just the power system, which will be combined with the base motherboard that you will be given.
 

🛠️ Hardware Overview
 

Power Source: 1S1P LiPo 3.7V, 800mAh battery
Charging: Dual-mode via USB-C and 9V input (200mA or ~600mA configurable)
Outputs: 5V@1.5A, 3.3V@300mA, 4x H-Bridge motor drive with up to 2A combined
Monitoring: INA219 on I2C bus keeps track of battery voltage/current
External loads: 2x High-side switches @ 1A from 5V rail
Switching: True system ON/OFF (<30uA in OFF state)
Connectors: JST PH 2mm for battery, 2x16 header for motherboard
Mechanical: Must be within 82mm x 60mm max, accurate mounting & connector positions needed
Budget Constraint: Entire board (assembly & components) must be less than $70
 

📝 Using This Repository
 

Schematic and Design Viewing
Schematic_UCT-PCB-EEE3088F_2025-04-25.pdf shows the finished schematic, comments and part references. Include a printout in lab demonstrations!
PCB_UCT-PCB-EEE3088F_2025-04-25.pcbdoc can be opened in Altium Designer (version 2020 and upwards), can be edited/traced or checked by DRC.
Putting PCBs into Production Order
UCT-PCB-EEE3088F_2025-04-25.zip contains Gerber, BOM (.csv), and pick-and-place files (.csv).
These files may be uploaded on JLCPCB for assembly and production. Directly upload the zip in its original form on JLCPCB order page. Proper options must be chosen for footprints, and JST and pin headers are not provided by JLC.
Screenshots of uploaded files on BOM and order submit pages are to be copied in interim and final design reports.
Bill of Materials and Populating
All surface-mount components needed for assembly are already included on BOM.
DO NOT install JST headers/connectors on JLC assembly (lab supplies these).
All part numbers are JLCPCB stocked parts where possible, easy to quote and assemble.
Any long components are included, be mindful of total project cost cap!
Testing & Demonstrations
Boards are UCT lab "testing jig" compatible for final testing.
Place the board (side down) on the jig with 2x16 connector.
Demonstrate:
Power rails ON/OFF, during load regulation
9V/USB-C input detection and switching
H-bridge operation
High/low current battery charging
INA219 I2C comms and measurements
OFF-state leakage current
Have all boards & schematic printout available during the demo.
Report Integration
This repository is to be utilized in interim and final-project design reports (see "GitHub Link" section of reports). Keep structure/titles same for ease of grading.
 

📝 Project Assignments and Use
 
You will be required to:
Clone/download this repository to see design files
Run, test, and adjust as necessary for your team's deployment
Gerbers & BOM to upload on JLCPCB before submission deadlines
Use screenshots as documentation in reports globally
Ensure documenting all design decisions, decisions, and potential failure-management steps with clear reference to the documents below
 

🔗 Useful Links
 

Micro-mouse Course Guide (Amathuba)
JLCPCB Online Ordering Platform
Micro-mouse Wikipedia
 

👥 Contributors
 
GDZTAK003 and MRKNIK004
 

📚 Reference
 
For project details requirements, deadlines, and demonstration refer to official course project brief on Amathuba. All mechanical, electrical, and reporting constraints are needed for successful project completion.
 

⚠️ Disclaimer
 
This repository is intended for student project work submission only for academic evaluation. Use in commercial projects without explicit permission of UCT EEE3088F course staff is not allowed.

If you experience any issues with the files or are having difficulties with usage, report an issue here in this repo or to your lab instructor.
 
End of README
