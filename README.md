# Norm
Norm is a Marlin based firmware customized for the Wanhao Duplicator 6/Monoprice Maker Ultimate with a all-metal hotend mod and intended to be used with PETG filament. This version requires manual leveling. I intend on releasing a branch for auto/mesh leveling using a Z-probe mod. This was made using marlin-conf https://github.com/akaJes/marlin-config I highly recommend it! Most values are taken from https://github.com/dot-bob/Marlin-Duplicator-6 otherwise I just googled my ass off and implemented recommmended changes.

Norm is named after my personal "maker muse", Norm Abram. https://en.wikipedia.org/wiki/Norm_Abram

Implemented Customizations:

MACHINE:

-Author and Variant changed to "(garylzimmer, D6-UMM Customized)"

-Custom Machine Name changed to "NORM"

-Inverted X and Z directions, Y is normal

-Z Max Pos changed to 170


EXTRUDER:

-Default Nominal Filament Diameter = 1.75

-Prevent Cold Extrusion = OFF (this is so that I can test extruder feeder gear without having to heat up, might be bad idea...)

-Extrude Min Temp = 0 (see above note)

-Extrude Max Length = 300

-Invert E0 Direction = True


TEMPERATURE:

-Temp Sensor 0 = PT100 UltiMB (20)

-Temp Sensor Bed = EPCOS 100K(1)

-Temp Residency Time = 3

-Temp Window = 2

-Temp Bed Residency Time = 3

-Heater 0 Max Temp = 285

-Bed Max Temp = 120

-PID_AutoTune_Menu = ON

-Default Kp=22.2, Ki=1.08, Kd=144

-PID Temp Bed = ON

-Default Bed Kp=10.00, Ki=0.023, Kd=305.4

-Preheat 1 Temp Hot End = 200 

-Preheat 1 Temp Bed = 60

-Preheat 2 Temp Hot End = 245 (for PETG)

-Preheat 2 Temp Bed = 80

-Print Counter = ON


HOMING:

-X,Y,Z Min End Stop Inverting = True

-Z Homing Height = OFF,0


MOTION:


-Default Axis Steps Per Unit = { 80.0395, 80.0395, 400.48, 99.1 }

-Default Max Accel = { 3000, 3000, 100, 500 }

-Default Accel = 1500

-Default Retract Accel = 1500

-Default Z Jerk = 0.4

-Default E Jerk = 1.0


PROBES:

-Z Min Probe uses Z Min EndStop Pin = OFF

-XY Probe Speed = 9000

-Z Probe Speed Slow = (Z_PROBE_SPEED_FAST / 3)

-Z Clearance Deplay Probe = 2

-Z Clearance Between Probe = 2

-Auto Bed Leveling UBL = ON (ombines the features of 3-point, linear, bilinear, and mesh leveling. As with bilinear leveling, the mesh data generated by UBL is used to adjust Z height across the bed using bilinear interpolation. An LCD controller is currently required.)
-UBL Probe Pt 1 X = 35

-UBL Probe Pt 1 Y = 165

-UBL Probe Pt 2 X = 35

-UBL Probe Pt 2 Y = 35

-UBL Probe Pt 3 X = 165

-UBL Probe Pt 3 Y = 35


EXTRAS:

-EEPROM Settings = ON


LCD:

-SD Support = ON

-Encoder Pulses Per Step = ON, 2

-Encoder Steps per Menu Item = ON, 1

-Reverse Encoder Direction = ON

-Individual Axis Homing Menu = ON

-Speaker = ON

-LCD Feedback Freq Duration MS = On, 5

-LCD Feedback Freq HZ = 1000

-Ultipanel = ON

-U8GLIB_SSD1306 = ON


ADVANCED CONFIG:


TEMP:

-Thermal Protection Period = 90

-Watch Temp Period = 90

-Thermal Protection Bed Period = 90

-Watch Bed Temp Period = 90

-Autotemp = OFF


EXTRUDER:

-Case Light Enable = ON

-Case Light Pin = ON, 8

-Case Light Default Brightness = 255

-Menu Item Case Light = ON

-Lin Advance = ON, K=0


HOMING:

-Quick Home = ON


EXTRAS:

-PWM Motor Current = ON, { 1200, 1200, 1000 }

-Advanced Pause Feature = ON


MACHINE:

-Home After Deactivate = ON


LCD:

-Manual Feedrate = {70*60, 70*60, 15*60, 6*60}

-LCD Info Menu = ON

-LCD Timeout To Status = 60000

-Long Filename Host Support = ON

-Scroll Long Filenames = ON

-Babystepping = ON (Warning: Does not respect endstops!)

-Doubleclick for Z Babystepping = ON (Double-click on the Status Screen for Z Babystepping)
