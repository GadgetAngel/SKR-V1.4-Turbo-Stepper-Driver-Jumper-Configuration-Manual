# SKR-V1.4-Turbo-Stepper-Driver-Jumper-Configuration-Manual
:exclamation: This project provides documentation on how to configure stepper motor driver boards and
how to use them with the SKR V1.4 Turbo 3D printer controller board :exclamation:
```
 I use Git for Windows with VScode to manage this repository.  I also use Git LFS extension for .pdf and .png files.

 Install Git with LFS extension: https://git-lfs.github.com/

To Download the whole repository do the following: select the "Clone or download button" and click on "paste to clipboard" button so you can place the URL for the GitHub repository to the clipboard. Now Open Git Bash.
Change the current working directory to the location where you want the cloned directory.
Type git clone, and then paste the URL you copied earlier.
$ git clone https://github.com/GadgetAngel/SKR-V1.4-Turbo-Stepper-Driver-Jumper-Configuration-Manual.git
Press Enter to create your local clone.
Now open Window explorer to the location of the local clone.
```
The Repository contains a .zip file that contains the whole repository. So, one can just hit one button to download the whole repository.  Just hit the "Download" button on the .zip file itself. If you see "view raw file" you can also mouse right click on the "view raw file" and  select "save link as.." from the pop up menu to save the .zip file to you local drive.

Also, You can download the .zip from my google drive located here:

## The Whole Repository in .zip file is located on Google Drive at:  https://drive.google.com/file/d/1FvFCCCenZh_xMIvMoKWdRaBnWbXT4PAJ/view?usp=sharing

## Table of Contents:

```
Stepper Driver Configurations for SKR V1.4 Turbo Board
By       @GadgetAngel

Preface......................................................................................................1
  What is a stepper motor?...................................................................................2
  Stall Detection and Sensor-less Homing.....................................................................3
    Requirements Needed to Make Sensor-less Homing Work......................................................3
POLOLU A4988.................................................................................................4
  Driver Chip Chart for POLOLU A4988.........................................................................4
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Have RST&SLP PINS Set....5
    Special Consideration of D Jumper (RST&SLP) for SKR V1.4 TURBO Board.....................................6
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Have 
    RST&SLP Set..............................................................................................8
  The (latest release of) Marlin Setup for POLOLU A4988 Drivers.............................................13
BIQU A4988..................................................................................................16
  Driver Chip Chart for BIQU 4988...........................................................................16
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Have RST&SLP PINS Set...17
    Special Consideration of D Jumper (RST&SLP) for SKR V1.4 TURBO Board....................................18
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Have 
    RST&SLP Set.............................................................................................20
  The (latest release of) Marlin Setup for BIQU A4988 Drivers...............................................25
DRV8825.....................................................................................................28
  Driver Chip Chart for POLOLU DRV8825......................................................................28
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Have RST&SLP PINS Set...29
    Special Consideration of D Jumper (RST&SLP) for SKR V1.4 TURBO Board....................................30
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Have 
    RST&SLP Set.............................................................................................32
  The (latest release of) Marlin Setup for DRV8825 Drivers..................................................38
BIQU LV8729.................................................................................................42
  Driver Chip Chart for BIQU LV8729.........................................................................42
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have 
    RST&SLP PINS Set........................................................................................43
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which 
    Do Not Have RST&SLP Set.................................................................................45
  The (latest release of) Marlin Setup for BIQU LV8729 Drivers..............................................51
FYSETC LV8729...............................................................................................56
  Driver Chip Chart for FYSETC LV8729.......................................................................56
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have 
    RST&SLP PINS Set........................................................................................57
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which 
    Do Not Have RST&SLP Set.................................................................................59
  The (latest release of) Marlin Setup for FYSETC LV8729 Drivers............................................65
LERDGE LV8729...............................................................................................70
  Driver Chip Chart for LERDGE LV8729.......................................................................70
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have 
    RST&SLP PINS Set........................................................................................71
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which 
    Do Not Have RST&SLP Set.................................................................................73
  The (latest release of) Marlin Setup for LERDGE LV8729 Drivers............................................79
MKS LV8729..................................................................................................84
  Driver Chip Chart for MKS LV8729..........................................................................84
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have 
    RST&SLP PINS Set........................................................................................85
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which 
    Do Not Have RST&SLP Set.................................................................................87
  The (latest release of) Marlin Setup for MKS LV8729 Drivers...............................................93
FYSETC S6128 V1.1...........................................................................................98
  Driver Chip Chart for FYSETC S6128........................................................................98
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Have RST&SLP PINS Set...99
    Special Consideration of D Jumper (RST&SLP) for SKR V1.4 TURBO Board...................................100
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Have 
    RST&SLP Set............................................................................................102
  The (latest release of) Marlin Setup for FYSETC S6128 V1.1 Drivers.......................................108
FYSETC ST820...............................................................................................113
  Driver Chip Chart for FYSETC ST820.......................................................................113
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Have RST&SLP PINS Set..114
    Special Consideration of D Jumper (RST&SLP) for SKR V1.4 TURBO Board...................................115
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Have 
    RST&SLP Set............................................................................................117
  The (latest release of) Marlin Setup for FYSETC ST820 Drivers............................................123
BIQU ST820.................................................................................................129
  Driver Chip Chart for BIQU ST820.........................................................................129
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Have RST&SLP PINS Set..130
    Special Consideration of D Jumper (RST&SLP) for SKR V1.4 TURBO Board...................................131
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Have 
    RST&SLP Set............................................................................................133
  The (latest release of) Marlin Setup for BIQU ST820 Drivers..............................................139
POLOLU ST820 (STSPIN820)...................................................................................145
  Driver Chip Chart for POLOLU ST820.......................................................................145
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Have RST&SLP PINS Set..146
    Special Consideration of D Jumper (RST&SLP) for SKR V1.4 TURBO Board...................................147
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Have 
    RST&SLP Set............................................................................................149
  The (latest release of) Marlin Setup for POLOLU ST820 (STSPIN820) Drivers................................155
POLOLU MP6500..............................................................................................161
  Driver Chip Chart for POLOLU MP6500......................................................................161
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have 
    RST&SLP PINS Set.......................................................................................162
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers 
    Which Do Not Have RST&SLP Set..........................................................................164
  The (latest release of) Marlin Setup for POLOLU MP6500 Drivers...........................................168
POLOLU TB67S249FTG.........................................................................................173
  Driver Chip Chart for POLOLU TB67S249FTG.................................................................173
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have 
    RST&SLP PINS Set.......................................................................................174
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Do Not 
    Have RST&SLP Set.......................................................................................176
  The (latest release of) Marlin Setup for POLOLU TB67S249FTG Drivers......................................182
BIQU S109..................................................................................................187
  Driver Chip Chart for BIQU S109..........................................................................187
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have 
    RST&SLP PINS Set.......................................................................................188
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Do Not 
    Have RST&SLP Set.......................................................................................190
  The (latest release of) Marlin Setup for BIQU S109 Drivers...............................................196
FYSETC S109................................................................................................201
  Driver Chip Chart for FYSETC S109........................................................................201
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have 
    RST&SLP PINS Set.......................................................................................202
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Do Not 
    Have RST&SLP Set.......................................................................................204
  The (latest release of) Marlin Setup for FYSETC S109 Drivers.............................................210
BIQU TMC2100 Stand-alone Mode..............................................................................215
  Driver Chip Chart for BIQU TMC2100 in Stand-alone Mode...................................................215
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Tri State Stepper Drivers.................................216
    How to Create aa SKR V1.4 TURBO DuPont Jumper Cable to Use with Tri State Drivers......................218
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Tri State Stepper Motor Drivers................220
    Additional Equipment Needed for Low Low (STEP or FULL) Configuration...................................222
  The (latest release of) Marlin Setup for BIQU TMC2100 Drivers in Stand-alone Mode........................230
MKS TMC2100 Stand-alone Mode...............................................................................235
  Driver Chip Chart for MKS TMC2100 in Stand-alone Mode....................................................235
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Tri State Stepper Drivers.................................236
    How to Create a SKR V1.4 TURBO DuPont Jumper Cable to Use with Tri State Drivers.......................238
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Tri State Stepper Motor Drivers................240
    Additional Equipment Needed for Low Low (STEP or FULL) Configuration...................................242
  The (latest release of) Marlin Setup for MKS TMC2100 Drivers in Stand-alone Mode.........................250
BIQU TMC2130 Stand-alone Mode..............................................................................255
  Driver Chip Chart for BIQU TMC2130 in Stand-alone Mode...................................................255
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Tri State Stepper Drivers.................................256
    How to Create a SKR V1.4 TURBO DuPont Jumper Cable to Use with Tri State Drivers.......................258
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Tri State Stepper Motor Drivers................260
    Additional Equipment Needed for Low Low (STEP or FULL) Configuration...................................262
  The (latest release of) Marlin Setup for BIQU TMC2130 Drivers in Stand-alone Mode........................270
BIQU TMC2130 SPI Mode......................................................................................275
  Driver Chip Chart for BIQU TMC2130 in SPI Mode...........................................................275
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Stepper Motor Drivers in SPI Mode..............278
  Information on Sensor-less Homing........................................................................281
  The (latest release of) Marlin Setup for BIQU TMC2130 Drivers in SPI Mode................................285
BIQU TMC2208 V3.0 Stand-alone Mode.........................................................................298
  Driver Chip Chart for BIQU TMC2208 in Stand-alone Mode...................................................298
  SKR V1.4 TURBO LEGEND of Driver Chip for Binary State Stepper Drivers Which Do Not Have RST&SLP PINS Set.299
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Do Not 
    Have RST&SLP Set.......................................................................................301
  The (latest release of) Marlin Setup for BIQU TMC2208 V3.0 Drivers in Stand-alone Mode...................305
BIQU TMC2208 V3.0 One Time Programming (OTP) Mode..........................................................310
  Driver Chip Chart for BIQU TMC2208 in OTP Mode...........................................................310
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have 
    RST&SLP PINS Set.......................................................................................311
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Do Not 
    Have RST&SLP Set.......................................................................................313
  The (latest release of) Marlin Setup for BIQU TMC2208 V3.0 Drivers in One Time Programming (OTP) Mode....317
BIQU TMC2208 V3.0 UART Mode................................................................................322
  Driver Chip Chart for BIQU TMC2208 in UART Mode..........................................................322
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Stepper Motor Drivers in UART Mode.............325
  The (latest release of) Marlin Setup for BIQU TMC2208 V3.0 Drivers in UART Mode..........................331
FYSETC TMC2208 V1.2 Stand-alone Mode.......................................................................341
  Driver Chip Chart for FYSETC TMC2208 in Stand-alone Mode.................................................341
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have 
    RST&SLP PINS Set.......................................................................................342
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Do Not 
    Have RST&SLP Set.......................................................................................344
  The (latest release of) Marlin Setup for FYSETC TMC2208 V1.2 Drivers in Stand-alone Mode.................348
FYSETC TMC2208 V1.2 One Time Programming (OTP) Mode........................................................353
  Driver Chip Chart for FYSETC TMC2208 in OTP Mode.........................................................353
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have 
    RST&SLP PINS Set.......................................................................................354
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Do Not 
    Have RST&SLP Set.......................................................................................356
  The (latest release of) Marlin Setup for FYSETC TMC2208 V1.2 Drivers in One Time Programming (OTP) Mode..360
FYSETC TMC2208 V1.2 UART Mode..............................................................................365
  Driver Chip Chart for FYSETC TMC2208 in UART Mode........................................................365
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Stepper Motor Drivers in UART Mode.............368
  The (latest release of) Marlin Setup for FYSETC TMC2208 V1.2 Drivers in UART Mode........................374
BIQU TMC2225 V1.0 Stand-alone Mode.........................................................................384
  Driver Chip Chart for BIQU TMC2225 in Stand-alone Mode...................................................384
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have 
    RST&SLP PINS Set.......................................................................................385
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Do Not 
    Have RST&SLP Set.......................................................................................387
  The (latest release of) Marlin Setup for BIQU TMC2225 V1.0 Drivers in Stand-alone Mode...................391
BIQU TMC2225 V1.0 One Time Programming (OTP) Mode..........................................................396
  Driver Chip Chart for BIQU TMC2225 in OTP Mode...........................................................396
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have 
    RST&SLP PINS Set.......................................................................................397
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Do Not 
    Have RST&SLP Set.......................................................................................399
  The (latest release of) Marlin Setup for BIQU TMC2225 V1.0 Drivers in One Time Programming (OTP) Mode....403
BIQU TMC2225 V1.0 UART Mode................................................................................408
  Driver Chip Chart for BIQU TMC2225 in UART Mode..........................................................408
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Stepper Motor Drivers in UART Mode.............411
  The (latest release of) Marlin Setup for BIQU TMC2225 V1.0 Drivers in UART Mode..........................417
BIQU TMC2209 V1.2 Stand-alone Mode for StealthChop.........................................................427
  Driver Chip Chart for BIQU TMC2209 in Stand-alone Mode (StealthChop).....................................427
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have 
    RST&SLP PINS Set.......................................................................................428
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Do Not 
    Have RST&SLP Set.......................................................................................430
  The (latest release of) Marlin Setup for BIQU TMC2209 V1.2 Drivers in Stand-alone Mode for StealthChop...434
BIQU TMC2209 V1.2 Stand-alone Mode for SpreadCycle.........................................................439
  Driver Chip Chart for BIQU TMC2209 in Stand-alone Mode (SpreadCycle).....................................439
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have 
    RST&SLP PINS Set.......................................................................................440
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Do Not 
    Have RST&SLP Set.......................................................................................442
  The (latest release of) Marlin Setup for BIQU TMC2209 V1.2 Drivers in Stand-alone Mode for SpreadCycle...446
BIQU TMC2209 V1.2 UART Mode................................................................................451
  Driver Chip Chart for BIQU TMC2209 in UART Mode..........................................................451
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Stepper Motor Drivers in UART Mode.............454
  Information on Sensor-less Homing........................................................................458
  The (latest release of) Marlin Setup for BIQU TMC2209 V1.2 Drivers in UART Mode..........................462
BIQU TMC5160 V1.2 SPI Mode.................................................................................475
  Driver Chip Chart for BIQU TMC5160 in SPI Mode...........................................................475
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Stepper Motor Drivers in SPI Mode..............478
  Information on Sensor-less Homing........................................................................481
  The (latest release of) Marlin Setup for BIQU TMC5160 V1.2 Drivers in SPI Mode...........................485
BIQU TMC5161 V1.0 SPI Mode.................................................................................498
  Driver Chip Chart for BIQU TMC5161 in SPI Mode...........................................................498
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Stepper Motor Drivers in SPI Mode..............501
  Information on Sensor-less Homing........................................................................504
  The (latest release of) Marlin Setup for BIQU TMC5161 V1.0 Drivers in SPI Mode...........................508
APPENDIX A.................................................................................................521
  How to adjust the Vref on a Stepper Motor Driver board using the Potentiometer...........................521
APPENDIX B.................................................................................................523
  For the TMC drivers what's the difference between stand-alone mode and ("UART" or "SPI ") modes?.........523
  How to Calculate Vref for Non-TMC Stepper Motor Divers...................................................523
  How to Calculate Vref for TMC Stepper Motor Drivers......................................................524
  Driving Current Calculation Formulas for TMC Stepper Motor Drivers.......................................525
    #1 TMC2100 with Rs = 0.110Ω (110mΩ)....................................................................525
    #2 TMC2130 with Rs = 0.110Ω (110mΩ)....................................................................525
    #3 TMC2208 with Rs = 0.110Ω (110mΩ) for Stand-alone Mode...............................................525
    #4 TMC2208 with Rs = 0.110Ω (110mΩ) for UART Mode......................................................526
    #5 TMC2209 with Rs = 0.110Ω (110mΩ) for Stand-alone Mode...............................................526
    #6 TMC2209 with Rs = 0.110Ω (110mΩ) for UART Mode......................................................527
    #7 TMC2225 with Rs = 0.150Ω (150mΩ) for UART Mode......................................................527
    #8 TMC5160 with Rs = 0.075Ω (75mΩ) for SPI Mode........................................................527
    #9 TMC5161 with Rs = 0.062Ω (62mΩ) for SPI Mode........................................................528
    #10 TMC2225 with Rs = 0.150Ω (150mΩ) for Stand-alone Mode..............................................528
APPENDIX C.................................................................................................529
  The (Latest Release of) Marlin Setup That Is Common to ALL Stepper Motor Drivers.........................529
    Link to BIGTREETECH SKR V1.4 Instruction Manual.pdf....................................................529
    Link to Download Marlin 2.0.x Firmware Website.........................................................529
    Link to Pronterface Software...........................................................................530
    Link to How to Calibrate your 3D Printer...............................................................530
  SKR V1.4 TURBO Color PIN Diagram.........................................................................543
  SKR V1.4 TURBO Color Wiring Diagram......................................................................544
  DCDC Mode V1.0 Board.....................................................................................547
  SKR V1.4 TURBO Color PIN 1 Diagram.......................................................................549
  SKR V1.4 TURBO Color Schematic Diagram...................................................................550
  SKR V1.4 TURBO Uncolored Schematic Diagram...............................................................551
APPENDIX D.................................................................................................552
  Legends for SKR V1.4 TURBO Stepper Driver Socket Representations.........................................552
    SKR V1.4 TURBO LEGEND COMMON to ALL Driver Socket Representation.......................................553
    SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which 
      Have RST&SLP Set.....................................................................................554
    SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Have 
	  RST&SLP PINS Set.................................................................................557
      Special Consideration of D Jumper (RST&SLP) for SKR V1.4 TURBO Board.................................558
    SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers 
	  Which Do Not Have RST&SLP Set....................................................................559
    SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have 
      RST&SLP PINS Set.....................................................................................562
    SKR V1.4 TURBO LEGEND of Driver Socket Representation for Tri State Stepper Motor Drivers..............563
    SKR V1.4 TURBO LEGEND of Driver Chip Chart for Tri State Stepper Drivers...............................565
      How to Create a SKR V1.4 TURBO DuPont Jumper Cable to Use with Tri State Drivers.....................567
    SKR V1.4 TURBO LEGEND of Driver Socket Representation for SPI Capable Stepper Motor Drivers............568
    SKR V1.4 TURBO LEGEND of Driver Socket Representation for UART Capable Stepper Motor Drivers...........572
    SKR V1.4 TURBO LEGEND of Driver Socket Representation for Sensor-less Homing Capable Stepper 
	  Motor Drivers....................................................................................579
  Examples for Stepper Driver Socket Representations.......................................................584
    Example 1 (LV8729 Driver Board; Binary State Driver without RST&SLP) for SKR V1.4 TURBO Driver Socket 
      Representation.......................................................................................584
    Example 2 (A4988 Driver Board; Binary State Driver with RST&SLP) for SKR V1.4 TURBO Driver Socket 
      Representation.......................................................................................585
    Example 3 (TMC2130 Driver in Stand-alone Mode; Tri State Driver) for SKR V1.4 TURBO Driver Socket 
      Representation.......................................................................................586
    Example 4 (TMC2209 UART with Sensor-less Homing) for SKR V1.4 TURBO Driver Socket Representation.......587
    Example 5 (TMC2209 UART WITHOUT Sensor-less Homing) for SKR V1.4 TURBO Driver Socket Representation....588
    Example 6 (TMC2130 SPI with Sensor-less Homing) for SKR V1.4 TURBO Driver Socket Representation........589
    Example 7 (TMC2130 SPI WITHOUT Sensor-less Homing) for SKR V1.4 TURBO Driver Socket Representation.....590
APPENDIX E.................................................................................................591
  Location Of “firmware.bin” File from the Marlin Compilation for SKR V1.4 TURBO Board.....................591
APPENDIX F.................................................................................................594
  Links to Reference Material..............................................................................594
    Marlin Firmware Documentation..........................................................................594
    Information on Stepper Motor Drivers and Micro-stepping................................................594
    POLOLU A4988 and BIQU A4988............................................................................595
    DRV8825................................................................................................595
    BIQU LV8729, FYSETC LV8729, LERDGE LV8729, and MKS LV8729..............................................596
    BIQU LV8729............................................................................................596
    FYSETC LV8729..........................................................................................597
    LERDGE LV8729..........................................................................................597
    MKS LV8729.............................................................................................598
    FYSETC S6128 V1.1......................................................................................598
    FYSETC ST820...........................................................................................599
    BIQU ST820.............................................................................................599
    POLOLU ST820 (STSPIN820)...............................................................................600
    POLOLU MP6500..........................................................................................600
    POLOLU TB67S249FTG.....................................................................................601
    BIQU S109 and FYSETC S109..............................................................................601
    BIQU S109..............................................................................................602
    FYSETC S109............................................................................................602
    Marlin Firmware Documentation Specific to TMC Drivers..................................................603
    Information Common to All TMC Drivers..................................................................603
    BIQU TMC2100 and MKS TMC2100...........................................................................604
    BIQU TMC2130...........................................................................................605
    Information Common to BIQU TMC2208 V3.0 and FYSETC TMC2208 V1.2........................................605
    Information Common to BIQU TMC2208 V3.0 and FYSETC TMC2208 V1.2 (Continued)............................606
    BIQU TMC2208 V3.0......................................................................................606
    FYSETC TMC2208 V1.2....................................................................................606
    Information Common to TMC2208 and BIQU TMC2225.........................................................607
    BIQU TMC2225 V1.0......................................................................................607
    BIQU TMC2209 V1.2......................................................................................608
    BIQU TMC5160 V1.2......................................................................................608
    BIQU TMC5161 V1.0......................................................................................609
    SKR V1.4 TURBO Board...................................................................................609
    Facebook Groups........................................................................................610
    Miscellaneous Information..............................................................................611
    Miscellaneous Information (continued)..................................................................612
APPENDIX G.................................................................................................614
  BIGTREETECH Reference Material...........................................................................614
    Original PIN Diagram...................................................................................614
    Original Wiring Diagram 1..............................................................................615
    Original Wiring Diagram 2 for STEP/DIR Mode............................................................616
    Original Wiring Diagram 3 for UART Mode................................................................617
    Original Wiring Diagram 4 for SPI Mode.................................................................618
    Original PIN 1 Diagram #1..............................................................................619
    Additional Original Reference Material for PIN 1 Diagram #2............................................620
    Additional Original Reference Material for PIN 1 Diagram #3............................................621
    Original Schematic Diagram.............................................................................622
APPENDIX H.................................................................................................623
  Filament Runout Sensor Guide for SKR V1.4 TURBO Board....................................................623
    Filament Runout Sensor Wired to Limit Switch {X-, Y-, Z-, E0DET, E1DET, or PWRDET}.....................624
    Marlin 2.0.x Setup for Filament Runout Sensor Connected to E0DET Connector.............................625
      Marlin 2.0.x Setup for Filament Runout Sensor........................................................626
APPENDIX I.................................................................................................630
  “Connecting up Raspberry Pi via TFT Connector” Guide for SKR V1.4 TURBO Board............................630
    Connecting SKR V1.4 TURBO to Raspberry Pi to Eliminate USB Cable Via TFT Connector.....................631
      TFT Connector Wiring Diagram for Connecting SKR V1.4 TURBO to Raspberry Pi to Eliminate USB Cable....634
    Marlin 2.0.x Setup for Connecting up Raspberry Pi......................................................637
APPENDIX J.................................................................................................639
  “Connecting up Raspberry Pi via WIFI Header” Guide for SKR V1.4 TURBO Board..............................639
    Connecting SKR V1.4 TURBO to Raspberry Pi to Eliminate USB Cable via WIFI Header.......................640
      WIFI Header Wiring Diagram for Connecting SKR V1.4 TURBO to Raspberry Pi to Eliminate USB Cable......643
    Marlin 2.0.x Setup for Connecting up Raspberry Pi......................................................646
APPENDIX K.................................................................................................648
  BLTouch Guide for SKR V1.4 TURBO Board...................................................................648
    Connecting SKR V1.4 TURBO with BLTouch.................................................................649
      Wiring Diagram for Connecting SKR V1.4 TURBO with BLTouch............................................652
    Marlin 2.0.x Firmware Setup for Connecting a BLTouch to the SKR V1.4 TURBO Board.......................653
      Explanation when to use Marlin variable Z_MIN_PROBE_USES_Z_MIN_ENDSTOP_PIN...........................657
      Understanding Marlin Firmware’s NOZZLE_TO_PROBE_OFFSET Setting.......................................660
APPENDIX L.................................................................................................675
  PT100 Guide for SKR V1.4 TURBO Board.....................................................................675
    Connecting SKR V1.4 TURBO with PT100 Amplifier Board and PT100 Sensor..................................676
      Instructions on How to Perform the SKR V1.4 TURBO Hardware Hack to Obtain an ADC Input on a 
        Thermistor Port....................................................................................681
    Instructions for Suppling Power to the PT100 Amplifier Board...........................................684
      Method #1 for Powering the PT100 Amplifier Board (Digital PWR).......................................685
      Method #2 for Powering PT100 Amplifier Board (Analog PWR)............................................686
    Technique #1 & Method #1 (Digital PWR) Wiring Diagram for Connecting Up Your PT1100 to the TFT Header..687
    Technique #2 & Method #1 (Digital PWR) Wiring Diagram for Connecting Up Your PT100 to the 
      TH0 Connector........................................................................................688
    Technique #2 & Method #2 (Analog PWR) Wiring Diagram for Connecting Up Your PT100 to the TH0 Connector.689
    Marlin 2.0.x Firmware Setup for Connecting a PT100 Sensor to the SKR V1.4 TURBO Board..................690
      Marlin 2.0.x Firmware Setup via Technique #1.........................................................691
      Marlin 2.0.x Firmware Setup via Technique #2.........................................................696
APPENDIX M.................................................................................................701
  K-Type Thermocouple Guide for SKR V1.4 TURBO Board.......................................................701
    Connecting SKR V1.4 TURBO with K-Type Thermocouple Sensor and Adafruit’s AD8495 Amplifier Board........702
      Instructions on How to Perform the SKR V1.4 TURBO Hardware Hack to Obtain an ADC Input on a 
        Thermistor Port....................................................................................707
    Instructions for Suppling Power to the AD8495 Amplifier Board..........................................710
      Method #1 for Powering the AD8495 Amplifier Board (Digital PWR)......................................711
      Method #2 for Powering AD8495 Amplifier Board (Analog PWR)...........................................712
    Technique #1 & Method #1 (Digital PWR) Wiring Diagram for Connecting Up Your K-Type Thermocouple 
      to the TFT Header....................................................................................713
    Technique #2 & Method #1 (Digital PWR) Wring Diagram for Connecting Up Your K-Type Thermocouple 
      to the TH0 Connector.................................................................................714
    Technique #2 & Method #2 (Analog PWR) Wiring Diagram for Connecting Up Your K-Type Thermocouple 
      to the TH0 Connector.................................................................................715
    Marlin 2.0.x Firmware Setup for Connecting a K-Type Thermocouple Sensor and Adafruit’s AD8495 
      Amplifier Board......................................................................................716
      Marlin 2.0.x Firmware Setup via Technique #1.........................................................717
      Marlin 2.0.x Firmware Setup via Technique #2.........................................................723
```
