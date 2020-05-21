# SKR-V1.4-Turbo-Stepper-Driver-Jumper-Configuration-Manual
:exclamation: This project provides documentation on how to configure stepper motor driver boards and
how to use them with the SKR V1.4 Turbo 3D printer controller board :exclamation:
```
 I use Git for Windows with VScode to manage this repository.  I also use Git LFS extenstion for .pdf and .png files.

To Download the whole repository do the following: select the "Clone or download button" and click on "paste to clipboard" button so you can place the URL for the GitHub repository to the clipboard. Now Open Git Bash.
Change the current working directory to the location where you want the cloned directory.
Type git clone, and then paste the URL you copied earlier.
$ git clone https://github.com/GadgetAngel/SKR-V1.4-Turbo-Stepper-Driver-Jumper-Configuration-Manual.git
Press Enter to create your local clone.
Now open Window explorer to the location of the local clone.
```
## Table of Contents:

```
Stepper Driver Configurations for SKR V1.4 Turbo Board
By       @GadgetAngel

POLOLU A4988.................................................................................................1
  Driver Chip Chart for POLOLU A4988.........................................................................1
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Have RST&SLP PINS Set....2
  Special Consideration of D Jumper (RST&SLP) for SKR V1.4 TURBO Board.......................................3
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Have 
    RST&SLP Set..............................................................................................5
  The (latest release of) Marlin Setup for POLOLU A4988 Drivers.............................................10
BIQU A4988..................................................................................................13
  Driver Chip Chart for BIQU 4988...........................................................................13
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Have RST&SLP PINS Set...14
  Special Consideration of D Jumper (RST&SLP) for SKR V1.4 TURBO Board......................................15
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Have 
    RST&SLP Set.............................................................................................17
  The (latest release of) Marlin Setup for BIQU A4988 Drivers...............................................22
DRV8825.....................................................................................................25
  Driver Chip Chart for POLOLU DRV8825......................................................................25
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Have RST&SLP PINS Set...26
  Special Consideration of D Jumper (RST&SLP) for SKR V1.4 TURBO Board......................................27
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Have 
    RST&SLP Set.............................................................................................29
  The (latest release of) Marlin Setup for DRV8825 Drivers..................................................35
BIQU LV8729.................................................................................................39
  Driver Chip Chart for BIQU LV8729.........................................................................39
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have RST&SLP 
    PINS Set................................................................................................40
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Do Not 
  Have RST&SLP Set..........................................................................................42
  The (latest release of) Marlin Setup for BIQU LV8729 Drivers..............................................48
FYSETC LV8729...............................................................................................53
  Driver Chip Chart for FYSETC LV8729.......................................................................53
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have RST&SLP 
    PINS Set................................................................................................54
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Do Not 
  Have RST&SLP Set..........................................................................................56
  The (latest release of) Marlin Setup for FYSETC LV8729 Drivers............................................62
LERDGE LV8729...............................................................................................67
  Driver Chip Chart for LERDGE LV8729.......................................................................67
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have RST&SLP 
    PINS Set................................................................................................68
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Do Not 
    Have RST&SLP Set........................................................................................70
  The (latest release of) Marlin Setup for LERDGE LV8729 Drivers............................................76
MKS LV8729..................................................................................................81
  Driver Chip Chart for MKS LV8729..........................................................................81
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have RST&SLP 
    PINS Set................................................................................................82
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Do Not 
    Have RST&SLP Set........................................................................................84
  The (latest release of) Marlin Setup for MKS LV8729 Drivers...............................................90
FYSETC S6128 V1.1...........................................................................................95
  Driver Chip Chart for FYSETC S6128........................................................................95
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Have RST&SLP PINS Set...96
    Special Consideration of D Jumper (RST&SLP) for SKR V1.4 TURBO Board....................................97
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Have 
    RST&SLP Set.............................................................................................99
  The (latest release of) Marlin Setup for FYSETC S6128 V1.1 Drivers.......................................105
FYSETC ST820...............................................................................................110
  Driver Chip Chart for FYSETC ST820.......................................................................110
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Have RST&SLP PINS Set..111
    Special Consideration of D Jumper (RST&SLP) for SKR V1.4 TURBO Board...................................112
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Have 
    RST&SLP Set............................................................................................114
  The (latest release of) Marlin Setup for FYSETC ST820 Drivers............................................120
BIQU ST820.................................................................................................126
  Driver Chip Chart for BIQU ST820.........................................................................126
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Have RST&SLP PINS Set..127
    Special Consideration of D Jumper (RST&SLP) for SKR V1.4 TURBO Board...................................128
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Have 
    RST&SLP Set............................................................................................130
  The (latest release of) Marlin Setup for BIQU ST820 Drivers..............................................136
POLOLU ST820 (STSPIN820)...................................................................................142
  Driver Chip Chart for POLOLU ST820.......................................................................142
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Have RST&SLP PINS Set..143
    Special Consideration of D Jumper (RST&SLP) for SKR V1.4 TURBO Board...................................144
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Have 
    RST&SLP Set............................................................................................146
  The (latest release of) Marlin Setup for POLOLU ST820 (STSPIN820) Drivers................................152
POLOLU MP6500..............................................................................................158
  Driver Chip Chart for POLOLU MP6500......................................................................158
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have RST&SLP 
    PINS Set...............................................................................................159
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Do Not 
    Have RST&SLP Set.......................................................................................161
  The (latest release of) Marlin Setup for POLOLU MP6500 Drivers...........................................165
POLOLU TB67S249FTG.........................................................................................170
  Driver Chip Chart for POLOLU TB67S249FTG.................................................................170
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have RST&SLP 
    PINS Set...............................................................................................171
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Do Not 
    Have RST&SLP Set.......................................................................................173
  The (latest release of) Marlin Setup for POLOLU TB67S249FTG Drivers......................................179
BIQU S109..................................................................................................184
  Driver Chip Chart for BIQU S109..........................................................................184
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have RST&SLP 
    PINS Set...............................................................................................185
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Do Not 
    Have RST&SLP Set.......................................................................................187
  The (latest release of) Marlin Setup for BIQU S109 Drivers...............................................193
FYSETC S109................................................................................................198
  Driver Chip Chart for FYSETC S109........................................................................198
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have RST&SLP 
    PINS Set...............................................................................................199
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Do Not 
    Have RST&SLP Set.......................................................................................201
  The (latest release of) Marlin Setup for FYSETC S109 Drivers.............................................207
BIQU TMC2100 Stand-alone Mode..............................................................................212
  Driver Chip Chart for BIQU TMC2100 in Stand-alone Mode...................................................212
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Tri State Stepper Drivers.................................213
    How to Create aa SKR V1.4 TURBO DuPont Jumper Cable to Use with Tri State Drivers......................215
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Tri State Stepper Motor Drivers................217
    Additional Equipment Needed for Low Low (STEP or FULL) Configuration...................................219
  The (latest release of) Marlin Setup for BIQU TMC2100 Drivers in Stand-alone Mode........................227
MKS TMC2100 Stand-alone Mode...............................................................................232
  Driver Chip Chart for MKS TMC2100 in Stand-alone Mode....................................................232
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Tri State Stepper Drivers.................................233
    How to Create a SKR V1.4 TURBO DuPont Jumper Cable to Use with Tri State Drivers.......................235
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Tri State Stepper Motor Drivers................237
    Additional Equipment Needed for Low Low (STEP or FULL) Configuration...................................239
  The (latest release of) Marlin Setup for MKS TMC2100 Drivers in Stand-alone Mode.........................247
BIQU TMC2130 Stand-alone Mode..............................................................................252
  Driver Chip Chart for BIQU TMC2130 in Stand-alone Mode...................................................252
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Tri State Stepper Drivers.................................253
    How to Create a SKR V1.4 TURBO DuPont Jumper Cable to Use with Tri State Drivers.......................255
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Tri State Stepper Motor Drivers................257
    Additional Equipment Needed for Low Low (STEP or FULL) Configuration...................................259
  The (latest release of) Marlin Setup for BIQU TMC2130 Drivers in Stand-alone Mode........................267
BIQU TMC2130 SPI Mode......................................................................................272
  Driver Chip Chart for BIQU TMC2130 in SPI Mode...........................................................272
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Stepper Drivers in SPI Mode...............................275
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Stepper Motor Drivers in SPI Mode..............277
  Information on Sensor-less Homing........................................................................278
  The (latest release of) Marlin Setup for BIQU TMC2130 Drivers in SPI Mode................................281
BIQU TMC2208 V3.0 Stand-alone Mode.........................................................................294
  Driver Chip Chart for BIQU TMC2208 in Stand-alone Mode...................................................294
  SKR V1.4 TURBO LEGEND of Driver Chip for Binary State Stepper Drivers Which Do Not Have RST&SLP PINS Set.295
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Do Not 
    Have RST&SLP Set.......................................................................................297
  The (latest release of) Marlin Setup for BIQU TMC2208 V3.0 Drivers in Stand-alone Mode...................301
BIQU TMC2208 V3.0 One Time Programming (OTP) Mode..........................................................306
  Driver Chip Chart for BIQU TMC2208 in OTP Mode...........................................................306
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have RST&SLP 
    PINS Set...............................................................................................307
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Do Not 
    Have RST&SLP Set.......................................................................................309
  The (latest release of) Marlin Setup for BIQU TMC2208 V3.0 Drivers in One Time Programming (OTP) Mode....313
BIQU TMC2208 V3.0 UART Mode................................................................................318
  Driver Chip Chart for BIQU TMC2208 in UART Mode..........................................................318
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Stepper Drivers in UART Mode..............................321
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Stepper Motor Drivers in UART Mode.............322
  The (latest release of) Marlin Setup for BIQU TMC2208 V3.0 Drivers in UART Mode..........................324
FYSETC TMC2208 V1.2 Stand-alone Mode.......................................................................334
  Driver Chip Chart for FYSETC TMC2208 in Stand-alone Mode.................................................334
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have RST&SLP 
    PINS Set...............................................................................................335
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Do Not 
    Have RST&SLP Set.......................................................................................337
  The (latest release of) Marlin Setup for FYSETC TMC2208 V1.2 Drivers in Stand-alone Mode.................341
FYSETC TMC2208 V1.2 One Time Programming (OTP) Mode........................................................346
  Driver Chip Chart for FYSETC TMC2208 in OTP Mode.........................................................346
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have RST&SLP 
    PINS Set...............................................................................................347
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Do Not 
    Have RST&SLP Set.......................................................................................349
  The (latest release of) Marlin Setup for FYSETC TMC2208 V1.2 Drivers in One Time Programming (OTP) Mode..353
FYSETC TMC2208 V1.2 UART Mode..............................................................................358
  Driver Chip Chart for FYSETC TMC2208 in UART Mode........................................................358
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Stepper Drivers in UART Mode..............................361
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Stepper Motor Drivers in UART Mode.............362
  The (latest release of) Marlin Setup for FYSETC TMC2208 V1.2 Drivers in UART Mode........................364
BIQU TMC2225 V1.0 Stand-alone Mode.........................................................................374
  Driver Chip Chart for BIQU TMC2225 in Stand-alone Mode...................................................374
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have RST&SLP 
    PINS Set...............................................................................................375
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Do Not 
    Have RST&SLP Set.......................................................................................377
  The (latest release of) Marlin Setup for BIQU TMC2225 V1.0 Drivers in Stand-alone Mode...................381
BIQU TMC2225 V1.0 One Time Programming (OTP) Mode..........................................................386
  Driver Chip Chart for BIQU TMC2225 in OTP Mode...........................................................386
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have RST&SLP 
    PINS Set...............................................................................................387
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Do Not 
    Have RST&SLP Set.......................................................................................389
  The (latest release of) Marlin Setup for BIQU TMC2225 V1.0 Drivers in One Time Programming (OTP) Mode....393
BIQU TMC2225 V1.0 UART Mode................................................................................398
  Driver Chip Chart for BIQU TMC2225 in UART Mode..........................................................398
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Stepper Drivers in UART Mode..............................401
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Stepper Motor Drivers in UART Mode.............402
  The (latest release of) Marlin Setup for BIQU TMC2225 V1.0 Drivers in UART Mode..........................404
BIQU TMC2209 V1.2 Stand-alone Mode for StealthChop.........................................................414
  Driver Chip Chart for BIQU TMC2209 in Stand-alone Mode (StealthChop).....................................414
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have RST&SLP 
    PINS Set...............................................................................................415
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Do Not 
    Have RST&SLP Set.......................................................................................417
  The (latest release of) Marlin Setup for BIQU TMC2209 V1.2 Drivers in Stand-alone Mode for StealthChop...421
BIQU TMC2209 V1.2 Stand-alone Mode for SpreadCycle.........................................................426
  Driver Chip Chart for BIQU TMC2209 in Stand-alone Mode (SpreadCycle).....................................426
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have RST&SLP 
    PINS Set...............................................................................................427
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Do Not 
    Have RST&SLP Set.......................................................................................429
  The (latest release of) Marlin Setup for BIQU TMC2209 V1.2 Drivers in Stand-alone Mode for SpreadCycle...433
BIQU TMC2209 V1.2 UART Mode................................................................................438
  Driver Chip Chart for BIQU TMC2209 in UART Mode..........................................................438
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Stepper Drivers in UART Mode..............................441
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Stepper Motor Drivers in UART Mode.............442
  Information on Sensor-less Homing........................................................................443
  The (latest release of) Marlin Setup for BIQU TMC2209 V1.2 Drivers in UART Mode..........................446
BIQU TMC5160 V1.2 SPI Mode.................................................................................459
  Driver Chip Chart for BIQU TMC5160 in SPI Mode...........................................................459
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Stepper Drivers in SPI Mode...............................462
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Stepper Motor Drivers in SPI Mode..............464
  Information on Sensor-less Homing........................................................................465
  The (latest release of) Marlin Setup for BIQU TMC5160 V1.2 Drivers in SPI Mode...........................468
BIQU TMC5161 V1.0 SPI Mode.................................................................................481
  Driver Chip Chart for BIQU TMC5161 in SPI Mode...........................................................481
  SKR V1.4 TURBO LEGEND of Driver Chip Chart for Stepper Drivers in SPI Mode...............................484
  SKR V1.4 TURBO LEGEND of Driver Socket Representation for Stepper Motor Drivers in SPI Mode..............486
  Information on Sensor-less Homing........................................................................487
  The (latest release of) Marlin Setup for BIQU TMC5161 V1.0 Drivers in SPI Mode...........................490
APPENDIX A.................................................................................................503
  How to adjust the Vref on a Stepper Motor Driver board using the Potentiometer...........................503
APPENDIX B.................................................................................................505
  For the TMC drivers what's the difference between stand-alone mode and ("UART" or "SPI ") modes?.........505
  How to Calculate Vref for Non-TMC Stepper Motor Divers...................................................505
  How to Calculate Vref for TMC Stepper Motor Drivers......................................................506
  Driving Current Calculation Formulas for TMC Stepper Motor Drivers.......................................507
    #1 TMC2100 with Rs = 0.110Ω (110mΩ)....................................................................507
    #2 TMC2130 with Rs = 0.110Ω (110mΩ)....................................................................507
    #3 TMC2208 with Rs = 0.110Ω (110mΩ) for Stand-alone Mode...............................................507
    #4 TMC2208 with Rs = 0.110Ω (110mΩ) for UART Mode......................................................508
    #5 TMC2209 with Rs = 0.110Ω (110mΩ) for Stand-alone Mode...............................................508
    #6 TMC2209 with Rs = 0.110Ω (110mΩ) for UART Mode......................................................509
    #7 TMC2225 with Rs = 0.150Ω (150mΩ) for UART Mode......................................................509
    #8 TMC5160 with Rs = 0.075Ω (75mΩ) for SPI Mode........................................................509
    #9 TMC5161 with Rs = 0.062Ω (62mΩ) for SPI Mode........................................................510
    #10 TMC2225 with Rs = 0.150Ω (150mΩ) for Stand-alone Mode..............................................510
APPENDIX C.................................................................................................511
  The (Latest Release of) Marlin Setup That Is Common to ALL Stepper Motor Drivers.........................511
    Link to BIGTREETECH SKR V1.4 Instruction Manual.pdf....................................................511
    Link to Pronterface Software...........................................................................512
    Link to How to Calibrate your 3D Printer...............................................................512
    SKR V1.4 TURBO Color PIN Diagram.......................................................................524
    SKR V1.4 TURBO Color Wiring Diagram....................................................................525
    DCDC Mode V1.0 Board...................................................................................528
    SKR V1.4 TURBO Color PIN 1 Diagram.....................................................................530
    SKR V1.4 TURBO Color Schematic Diagram.................................................................531
    SKR V1.4 TURBO Uncolored Schematic Diagram.............................................................532
APPENDIX D.................................................................................................533
  Legends for SKR V1.4 TURBO Stepper Driver Socket Representations.........................................533
    SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Have 
      RST&SLP Set..........................................................................................534
    SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Have RST&SLP 
      PINS Set.............................................................................................537
      Special Consideration of D Jumper (RST&SLP) for SKR V1.4 TURBO Board.................................538
    SKR V1.4 TURBO LEGEND of Driver Socket Representation for Binary State Stepper Motor Drivers Which Do 
      Not Have RST&SLP Set.................................................................................539
    SKR V1.4 TURBO LEGEND of Driver Chip Chart for Binary State Stepper Drivers Which Do Not Have RST&SLP 
      PINS Set.............................................................................................542
    SKR V1.4 TURBO LEGEND of Driver Socket Representation for Tri State Stepper Motor Drivers..............543
    SKR V1.4 TURBO LEGEND of Driver Chip Chart for Tri State Stepper Drivers...............................545
      How to Create a SKR V1.4 TURBO DuPont Jumper Cable to Use with Tri State Drivers.....................547
    SKR V1.4 TURBO LEGEND of Driver Socket Representation for SPI Capable Stepper Motor Drivers............548
    SKR V1.4 TURBO LEGEND of Driver Socket Representation for UART Capable Stepper Motor Drivers...........549
    SKR V1.4 TURBO LEGEND of Driver Socket Representation for Sensor-less Homing Capable Stepper Motor 
      Drivers..............................................................................................550
  Examples for Stepper Driver Socket Representations.......................................................552
    Example 1 (LV8729 Driver Board; Binary State Driver without RST&SLP) for SKR V1.4 TURBO Driver Socket 
      Representation.......................................................................................552
    Example 2 (A4988 Driver Board; Binary State Driver with RST&SLP) for SKR V1.4 TURBO Driver Socket 
      Representation.......................................................................................553
    Example 3 (TMC2130 Driver in Stand-alone Mode; Tri State Driver) for SKR V1.4 TURBO Driver Socket 
      Representation.......................................................................................554
    Example 4 (TMC2209 UART with Sensor-less Homing) for SKR V1.4 TURBO Driver Socket Representation.......555
    Example 5 (TMC2209 UART WITHOUT Sensor-less Homing) for SKR V1.4 TURBO Driver Socket Representation....556
    Example 6 (TMC2130 SPI with Sensor-less Homing) for SKR V1.4 TURBO Driver Socket Representation........557
    Example 7 (TMC2130 SPI WITHOUT Sensor-less Homing) for SKR V1.4 TURBO Driver Socket Representation.....558
APPENDIX E.................................................................................................559
  Location Of “firmware.bin” File from the Marlin Compilation for SKR V1.4 TURBO Board.....................559
APPENDIX F.................................................................................................562
  Links to Reference Material..............................................................................562
    Marlin Firmware Documentation..........................................................................562
    Information on Stepper Motor Drivers and Micro-stepping................................................562
    POLOLU A4988 and BIQU A4988............................................................................563
    DRV8825................................................................................................563
    BIQU LV8729, FYSETC LV8729, LERDGE LV8729, and MKS LV8729..............................................564
    BIQU LV8729............................................................................................564
    FYSETC LV8729..........................................................................................565
    LERDGE LV8729..........................................................................................565
    MKS LV8729.............................................................................................566
    FYSETC S6128 V1.1......................................................................................566
    FYSETC ST820...........................................................................................567
    BIQU ST820.............................................................................................567
    POLOLU ST820 (STSPIN820)...............................................................................568
    POLOLU MP6500..........................................................................................568
    POLOLU TB67S249FTG.....................................................................................569
    BIQU S109 and FYSETC S109..............................................................................569
    BIQU S109..............................................................................................570
    FYSETC S109............................................................................................570
    Marlin Firmware Documentation Specific to TMC Drivers..................................................571
    Information Common to All TMC Drivers..................................................................571
    BIQU TMC2100 and MKS TMC2100...........................................................................572
    BIQU TMC2130...........................................................................................573
    Information Common to BIQU TMC2208 V3.0 and FYSETC TMC2208 V1.2........................................573
    Information Common to BIQU TMC2208 V3.0 and FYSETC TMC2208 V1.2 (Continued)............................574
    BIQU TMC2208 V3.0......................................................................................574
    FYSETC TMC2208 V1.2....................................................................................574
    Information Common to TMC2208 and BIQU TMC2225.........................................................575
    BIQU TMC2225 V1.0......................................................................................575
    BIQU TMC2209 V1.2......................................................................................576
    BIQU TMC5160 V1.2......................................................................................576
    BIQU TMC5161 V1.0......................................................................................577
    SKR V1.4 TURBO Board...................................................................................577
    Facebook Groups........................................................................................578
    Miscellaneous Information..............................................................................579
    Miscellaneous Information (continued)..................................................................580
APPENDIX G.................................................................................................581
  BIGTREETECH Reference Material...........................................................................581
    Original PIN Diagram...................................................................................581
    Original Wiring Diagram 1..............................................................................582
    Original Wiring Diagram 2 for STEP/DIR Mode............................................................583
    Original Wiring Diagram 3 for UART Mode................................................................584
    Original Wiring Diagram 4 for SPI Mode.................................................................585
    Original PIN 1 Diagram.................................................................................586
    Additional Original Reference Material for PIN 1 Diagram...............................................587
    Original Schematic Diagram.............................................................................588
```