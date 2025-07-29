*Source*: <https://www.navy-radio.com/manuals/tty/m37/574-320-101-iss2-7302.pdf>

<div style="display: flex; justify-content: space-between;">
<div>BELL SYSTEM PRACTICES<br>AT&TCo Standard</div>
<div style="text-align: right;">SECTION 574-320-101<br>Issue 2, February 1973</div>
</div>

<h1 style="text-align: center; font-size: 1.2em; padding-left: 10%; padding-right: 10%;">
37 TYPING UNIT<br>
37P003 AND UP<br>
DESCRIPTION AND PRINCIPLES OF OPERATION
</h1>

## 1. GENERAL

\[Photo]

Figure 1 - 37 Typing Unit With Variable Features

1.01 This section describes the late design 37 typing unit (Figure 1) and the
wide platen typing unit (Figure 11). This is a general revision which includes
all previously issued supplementary information concerning the description and
principles of operation of the wide platen typing unit. Since this section is a
general revision, marginal arrows normally used to indicate changes or
additions, have been omitted.

*Page 2:*

1.02 The purpose of the unit is to translate electrical code signals into
printed graphics or functions. Other units that support normal operation of the
typing unit include a base with intermediate gear assembly, motor unit, and
electrical service unit. The support units are described in their appropriate
sections.

1.03 The 37 typing unit can be operated at speeds up to 150 words p€r minute.
The selector mechanism of the typing unit receives 10-unit, 8-level serial code.

1.04 Of the eight levels of code information, four levels are used to position
the typebox horizontally, and three levels are used to position the typebox
vertically. The eighth level is not used in typebox positioning. The horizontal
and vertical positioning mechanisms utilize the aggregate motion principle, and
respond immediately to repositioned codebars.

1.05 All eight levels of the ASCII (American National Standard Code for
Information Interchange) system can be sensed by the function mechanism. Seven
levels define a character, and the eighth (parity) level verifies accuracy of
transmission. When parity is used, a function cannot occur unless parity is
correct.

\[Photo]

- PAPER GUIDE
- PAPER STRAIGHTENER
- PLATEN
- PAPER FINGER
- PAPER RELEASE
- **KEYBOARD RESET COUPLER**
  - Extends rotational motion to the keyboard reset mechanism mounted on the
    base unit.
- **SPACING MECHANISM**
  - Advances print hammer and typebox along platen after each graphic is
    printed.
  - Completes spacing cycle in one-sixth revolution of main shaft.
- **SELECTOR MECHANISM**
  - Receives and converts electrical code input to mechanical code output.

(Front Right View)

Figure 2 - 37 Typing Unit

\[Photo]

- **TYPEBOX**
  - Upper and lower case printing with 94 standard character pallets. Two
    additional pallets omitted for the spacing and delete characters.
  - Expanded character set (optional) - an additional 32 special characters in
    addition to the standard graphics of the ASCII plan.
  - Pallets with 10 or 12 characters per inch spacing.
  - Positioned by vertical and horizontal positioning mechanism.
  - Easily removed for cleaning or replacement.
- **PRINT HAMMER MECHANISM**
  - If character is graphic, the print hammer trips and strikes appropriate type
    pallet.
- **MULTIPLE COPY KNOB**
  - Two position adjustable knob. One position for single copy typing. Other
    position for multiple copy typing.
- **HORIZONTAL POSITIONING MECHANISM**
  - Accepts four codebar inputs from codebar mechanism to select vertical row of
    type pallets.
- **HORIZONTAL TABULATION MECHANISM (VARIABLE FEATURE)**
  - Horizontally positions print hammer and typebox. Released by function bar
    and controlled by adjustable index tabs.
- **CARRIAGE RETURN MECHANISM**
  - Returns print hammer and typebox to left margin when CARRIAGE RETURN
    function character or local control key is depressed.

(Front View)

Figure 3 - 37 Typing Unit

*Page 4:*

\[Photo]

- **RETRACTION MECHANISM**
  - Lowers typebox to expose printed graphic after brief idle line.
  - When operated, repositions and 7 codebars to spacing.
- **VERTICAL TABULATION MECHANISM (VARIABLE FEATURE)**
  - Line feeds page or form when released by function bar. Controlled by
    adjustable index tabs.
- **PAPER FEED KNOB**
  - Manually operate platen to feed paper.
- **ON-LINE VERTICAL TAB SET AND CLEAR**
  - Provides operator with on-line control of tabulation.
- **VERTICAL POSITIONING MECHANISM**
  - Accepts three codebar inputs from codebar mechanism to select horizontal row
    of type pallets.
- **CODEBAR MECHANISM**
  - Receives inputs from either selector mechanism or retraction mechanism.
    Provides four outputs to horizontal positioning mechanism and three outputs
    to vertical positioning mechanism. Rear side of codebars provides eight
    outputs to function mechanism.
  - Suppression codebar can be operated by stunt box to inhibit operation of
    certain function bars.

(Left Side View)

Figure 4 - 37 Typing Unit

*Page 5:*

\[Photo]

- **RIBBON MECHANISM**
  - Provides inked source for impressing graphic on paper.
  - Advances ribbon after each graphic is printed.
  - Automatically changes direction of ribbon feed at end of ribbon.
- **TWO COLOR RIBBON MECHANISM (VARIABLE FEATURE)**
  - Magnet operated through function mechanism to shift vertical position of
    ribbon so that one of two colors is opposite of graphic to be printed.
- **RIBBON REVERSE LEVER**
- **RIBBON**
  - Ink impregnated nylon.
- **CODEBAR MECHANISM**
- **TRANSFER MECHANISM**
  - Transfers output from selector mechanism to codebar mechanism.
- **SELECTOR CLUTCH**
- **RANGE FINDER**
  - Select most favorable period for sampling character bits.
- **SELECTOR MAGNETS**

(Right Side View)

Figure 5 - 37 Typing Unit

*Page 6:*

\[Photo]

- **36-PIN CONNECTOR**
  - Electrical interface from the function mechanism to the electrical service
    unit (transmission of control codes for the function box arrangements).
- **15-PIN CONNECTOR**
  - Provides the interface to the selector mechanism from the signal line
    circuits in the electrical service unit.
- **LINE FEED MECHANISM**
  - Advances platen one or two lines when LINE FEED character is received or
    local control key is depressed.
  - Single or double line is preset manually.
  - Completes line feed cycle in one-sixth revolution of main shaft.
  - Fractional line feed - half-forward and reverse.
- **TRIP SHAFT MECHANISM**
  - First operation engages function mechanism.
  - Second operation, if not inhibited, operates print hammer and ribbon feed
    mechanism.
  - Operates vertical and horizontal positioning dampeners.
- **FUNCTION MECHANISM**
  - Senses each new character received. Detects presence of function character
    and operates mechanical linkage or electrical contacts to initiate function.
  - Can suppress subsequent print hammer, spacing, and ribbon feed mechanisms.
  - Can sense parity (eighth) level.
  - Function box contains 42 slots for function bars.

(Rear View)

Figure 6 - 37 Typing Unit

*Page 7:*

## 2. DESCRIPTION

### BASIC UNIT

2.01 The typing unit contains the basic mechanisms to print a graphic or perform
a function. Rotational motion is applied to the main shaft assembly for
distribution to all mechanisms within the unit, and is extended to the keyboard
reset coupler for driving a separately mounted, keyboard reset mechanism.

2.02 The selector (Figure 2) translates a serial code input into a corresponding
mechanical code output. In 8-level, serial code reception, a combination of
eight code bits preceded by a start interval (always spacing) and concluded with
a stop pulse (always marking) establishes a character. The nonprinting character
(if assigned) is a function, and the printing character is a graphic.

2.03 The major mechanisms and variable features are described in Figures 2
through 9. Variable features are options which may be selected to increase the
functions of a basic typing unit.

2.04 The Model 37 can be broken down into five major subassemblies and a main
frame assembly. The subassemblies are: main shaft, function box, selector,
vertical position and a front plate assembly which contains the horizontal
positioning.

2.05 The typing unit is designed to be used with a base unit. Refer to Section
574-331-100 which gives the necessary rigidity to the printer frame. The typing
unit should never be operated under power when loose on the base unit or a
comparable supporting baseplate.

<u>CAUTION</u>: ALWAYS CHECK TO INSURE THAT THE TYPING UNIT IS PROPERLY SECURED
TOA BASE BEFORE OPERATING.

2.06 The base unit supports the typing unit, drive motor, intermediate gear
assembly, and keyboard reset mechanism. The base, with components, is supported
by rubber vibration mounts attached to a pan which is part of the cover
assembly. The rubber shock mounts isolate vibrations originating in the typing
unit, gears, and motor from the cover and table. The typing unit drives the
keyboard reset mechanism through a coupler, refer to Figure 2. A plastic shock
disc is used between the mating coupler to reduce noise and vibrations.

### Main Shaft

2.07 The main shaft (Figure 7) is located in the lower rear portion of the
typing unit and extends the full length of the unit. It is supported by ball
bearings mounted in each side frame. The main shaft includes six clutches, each
when tripped, drives its associated mechanism. Each clutch has two shoes which
bear against the inside surface of a drum when the clutch is engaged. The clutch
and drums are mounted to the main shaft by means of a mounting screw. Two of the
clutches (namely the line feed and the spacing clutches) have six sets of lugs
equally spaced about their periphery for controlling the engagement and
disengagement of the clutch shoes with the drum. Thus, these clutches will turn
only one-sixth of a revolution when tripped, except when the single-double line
feed lever is set for double line feed in which case the line feed clutch will
turn one-third of a revolution. The remaining clutches have two sets of lugs and
will turn half of a complete revolution when tripped.

2.08 The six clutches (Figures 8 and 10) on the main shaft are, from right to
left, selector clutch, codebar clutch, print hammer clutch, spacing clutch,
function clutch, and line feed clutch. The selector clutch provides power for
operating the selector, and also trips the codebar clutch and resets the
retraction mechanism.

*Page 8:*

The codebar clutch drives the codebar positioning mechanism, trips the function
clutch and print hammer clutch. The print hammer clutch drives the print hammer,
ribbon feed, ribbon positioning, dampener detent arms and trips the spacing
clutch. The spacing clutch drives the spacing mechanism. The function clutch
drives the function bar reset bail and the function pawl stripper blade. The
line feed clutch drives the line feed mechanism.

### WIDE PLATEN

2.09 The basic description and operation for the 132 character position wide
platen typing unit (Figures 11 and 12) is similar to the standard typing unit.
This unit contains all the features presently available on the standard platen
sprocket feed unit. The wide platen unit differs from the standard unit for
horizontal tabulation, horizontal tab stop control and the backspace mechanisms.
The right side frame has been moved out for the additional width. An
intermediate casting acts as an auxiliary side frame and provides mounting
facilities for the function box, trip shaft and main shaft extensions. The front
plate, cable assembly, spacing drum and pulley assemblies have been changed. The
spacing drum differs from the standard unit; it contains the carriage return
spring and spacing ratchet. For detailed information on the spacing drum and
cable assembly, refer to Section 574-320-705 on disassembly and reassembly.

### OPTIONAL FEATURES

2.11 The typing unit is designed to accept a full range of options that are
on-line controllable. These options are furnished in the form of modification
kits listed below.

- Horizontal Tab
- Horizontal Tab-Stop Control
- Vertical Tab and Form Feed
- Vertical Tab-Stop Control
- Half-Forward and Reverse Line Feed
- Two-Color Ribbon
- Print (Only) Suppress
- Print, Space and Function Suppression
- Printed Graphics Extension
- Low-Paper Alarm Switch (Friction Feed)
- Paper-Out Alarm Switch (Sprocket Feed)
- Auto Carriage Return and Line Feed
- To Convert Friction Feed to Sprocket Feed
- Escape Mechanism
- Printed Graphics Extension
- Character Received Contacts
- Visual Aid Feature

2.12 In addition to the above features, the function box can be equipped to
perform nonrepeat form feed and carriage return upon reception of line feed,
vertical tab or form feed.

*Page 9:*

\[Photo]

- **MAIN SHAFT ASSEMBLY**
  - Distributes mechanical rotational motion to various clutch-cam and
    clutch-gear assemblies, typebox positioning mechanisms, and spacing
    mechanisms.
  - Two-character cycles per revolution of the main shaft.
  - Positions vertical and horizontal dampeners.

(Bottom View)

Figure 9 - 37 Typing Unit

Figure 10 - Main Shaft

<u>Note:</u> When the typing unit is mated with the keyboard, refer to Section
574-331-100 for the required information concerning the adjustment between the
main shaft driven gear and the intermediate gear assembly.

*Page 10:*

## 3. TECHNICAL DATA

**Signal Input Data**

3.01 The typing unit is capable of printing symbols for all 128 ASCII
characters. Normally, however, it will be arranged to print the 94 graphic,
numeric, and alpha characters.

**Power Input Data**

3.02 Mechanical power is supplied to the printer mechanism by an electric motor
operating at 3600 rpm. An intermediate gear unit is used to reduce this speed,
and to provide a choice of printer main shaft speeds. Operating speeds
considerably lower than 600 operations per minute (100 wpm) may require changes
in the selector cam assembly.

| Unit Code | Levels | Bauds | OPM | Main Shaft Speed |
| --------- | ------ | ----- | --- | ---------------- |
| 10.00     | 8      | 150   | 900 | 500 RPM          |
| 11.00     | 8      | 110   | 600 | 343 RPM          |

**Output Data**

3.03 The standard friction feed typing unit prints the message on a roll of
single or multiple copy paper of 8-1/2 inches maximum width, 5 inches maximum
diameter.

3.04 The standard sprocket feed unit prints the message on up to six copies of
fan-folded form-feed paper with margin perforations spaced to fit the sprocket
teeth on the typing unit platen. Platens are available for the following paper
widths: 3-5/8, 4, 4-1/4, 4-5/16, 4-1/2, 5, 5-1/2, 5-3/4, 6, 6-1/4, 6-3/8, 6-1/2,
7, 7-1/2, 8, 8-1/2, 9, and 9-1/2 inches with the distance between holes being
one-half inch less than the paper width.

**Size and Weight**

3.05 Overall dimensions of the standard typing unit exclusive of the base unit
are:

- Length: 15-3/4 inches
- Height: 9-5/8 inches
- Depth: 10-7/8 inches
- Weight: 32 pounds

*Page 11:*

**Temperature Ranges**

3.06 This equipment is intended to be operated in a room environment within the
temperature range of 40°F to 110°F. Serious damage to it could result if this
range is exceeded. In this connection, particular caution should be exercised in
using acoustical or other enclosures.

- (a) The typing unit is designed to operate with standard lubrication without
  damage in an ambient temperature between 40 degrees and 140 degrees F measured
  inside the closed cover.
- (b) Operation at temperatures down to -20 degrees F is possible with special
  lubrication.

**Operational Requirements**

3.07 The unit operates in an environment ranging from 1 percent to 90 percent
relative humidity.

- (a) Operation is not adversely affected by inclination of up to 45 degrees.
  The timing of the machine makes possible the suppression of printing and
  spacing in the same cycle in which a nonprinting code is read by the function
  box.
- (b) Noise and vibration has been kept to a minimum. Noise and vibration
  isolation is provided in the base mounting, cover, and the cabinet.
- (c) No readily combustible material is used in the construction of the unit.

**Wide Platen Units**

3.08 Wide platen sprocket feed typing units have the same technical requirements
as the standard units except for the following physical requirements. Wide
platen units use a 14-7/8 inch form; the difference between the holes being
one-half inch less than the paper width. The basic wide platen typing unit
weighs approximately 36 pounds. The overall dimensions are:

- Length: 21-5/8 inches
- Height: 9-5/8 inches
- Depth: 10-7/8 inches
- Characters Per Line:
  - 132 characters - 10 per inch
  - 158 characters - 12 per inch
- Wire Rope:
  - Uses one rope 124-1/4 inches long.

## 4. PRINCIPLES OF OPERATION

### A. Selector Mechanism

4.01 The selector mechanism (Figures 2 and 5) consists of the magnet coils and
armature, a selector cam and clutch, and associated levers, arms and bails
necessary to convert the electrical intervals of the start-stop code to the
mechanical motions which are transferred to the codebar positioning mechanism.

**Manual Coding and Operation**

4.02 Manual coding and operation provides a visual check of the various
mechanisms under conditions that are similar to a. unit under power. Before the
unit can be coded and operated manually, the following set up procedures are
required.

<u>CAUTION:</u> IF THE TYPING UNIT IS MOUNTED IN A SET, DISCONNECT ALL
ELECTRICAL POWER TO THE SET AND REMOVE THE TYPING UNIT FROM ITS BASE.

- (a) Tie back the reset slide on the retraction mechanism as shown in Figure
  13. This procedure prevents the retraction mechanism from moving the no. 5, 6,
  and 7 codebars to a spacing condition and does not allow the typebox to move
  to its retracted position (a desirable condition when checking print hammer
  operation).

*Page 13:*

- (b) Attach a selector armature clip (TP321071) to the back of the selector
  mechanism. The installation is performed by inserting the curved end of the
  armature clip between the armature stop bracket and the armature; the other
  end is placed under the lubricator assembly, refer to Figure 14. The armature
  clip holds the selector armature in the attracted (marking) position. When the
  armature is attracted, the push levers for the eight code levels will move to
  a marking condition when the unit is manually operated through one cycle. This
  allows a character code to be manually placed into the selector by lifting off
  the push lever from the selector lever for the spacing bits in the code.
- (c) Install a handwheel (TP161430) with handwheel grip (TP340235) to the
  clutch drum of the selector, refer to Figure 15. The handwheel provides the
  leverage to manually rotate the main shaft.
- (d) Rotate the main shaft counterclockwise until the selector clutch is
  disengaged. Momentarily move the lift lever (Figure 14) down to simulate a
  start pulse and again, rotate the main shaft until all push levers are marking
  and the selector clutch is disengaged. This action clears the selector of any
  previous code and positions the push levers to a marking condition.
- (e) Manually rotate the main shaft in a counterclockwise direction until all
  the clutches are brought to a disengaged position (turning the handwheel with
  a fast spin should latch all the clutches).
- (f) Check to insure that all clutches are fully latched; the main shaft should
  rotate freely without drag. If the clutches are not fully disengaged, use the
  procedure described in the Note in 4.11.

4.03 To manually code and operate a typing unit proceed as follows:

- (a) Determine the spacing bits of the code to be selected from the code chart
  (Figure 16).
- (b) Set the push levers that are to be spacing (spacing bits of the desired
  code) by using a spring hook to push back and release the push lever at the
  point where the spring is hooked, refer to Figure 17. This procedure moves the
  push lever forward which lifts off the push lever from the selector lever and
  causes the code level to go spacing (there is no change in the transfer levers
  at this time).

*Page 14:*

- (c) Push back the intermediate arm latch bail by moving the auxiliary reset
  lever in the same manner as described in coding the push levers, refer to
  Figure 17. This procedure sets up the transfer mechanism for the code selected
  and positions the codebar shiftbars.
- (d) Pull back and hold the codebar clutch trip lever (Figure 18) and start
  turning the handwheel in a counterclockwise direction, then release the trip
  lever.
- (e) Continue turning the main shaft until the character is printed or function
  is performed.
- (f) To repeat the operation of a previously selected character or function,
  lift the appropriate clutch trip lever on the back of the unit (Figure 18).
  For example, if the character "A" has been coded into the selector and
  printed, and it is desired to repeat the printing operation, lift the printing
  clutch trip lever and turn the main shaft through one cycle and the character
  will print again. This method is used to check printing density or print
  hammer alignment with the type pallets. The same principle applies to a
  function coded into the selector. If a repeat is desired lift the function
  clutch trip lever and turn the main shaft.
- (g) To clear the selector of a previous code, push down the selector clutch
  lift lever and rotate the main shaft through one cycle, refer to 4.02 (d),
  (e), and (f).

4.04 The selector clutch and cam sleeve assembly is comprised of the two-stop
clutch, the start bail and lift lever cam, the eighth, seventh, sixth, fifth and
fourth selector lever cams, the cam for the spacing and marking locklevers, the
third, second, and the first selector lever cams, push lever reset bail cam, and
codebar clutch trip cam. Refer to Figures 17 through 21.

<u>Note</u>: On 5- and 6-level cam sleeves, no cams appear in the 6, 7, and 8th
or 7 and 8th positions respectively.

4.05 During the time in which a closed line circuit (marking) condition exists,
the selector magnet coils are energized and hold the selector armature against
the selector magnet pole pieces. In this stop position, the selector armature
blocks the start lever.

*Page 15:*

●Mark to obtain even parity, the characters and functions shown with shaded
backgrounds have 8th bit marking.

Example: Bits 1 through 7 of the bit permutation for the character Marc 1011001,
respectively. \
1 = Mark, 0 = Space

New Controls and Their Meanings (Old Name in Parentheses):

- SOH = Start of Heading (SOM)
- STX = Start of Text (EOA)
- ETX = End of Text (EOM)
- ENQ = Enquiry (WRU)
- ACK = Acknowledge (same meaning but new code)
- BS = Backspace (FE<sub>0</sub>)
- DLE = Data Line Escape (DC<sub>0</sub>)
- OCl = Device Control 1 (X-ON)
- DC2 = Device Control 2 (TAPE)
- DC3 = Device Control 3 (X-OFF)
- DC4 = Device Control 4 (<s>TAPE</s>)
- NAK = Negative Acknowledge (ERR — not same function)
- ETB = End of Transmission Block (LEM — not same function)
- CAN = Cancel (S<sub>0</sub> — not same function)
- EM = End of Medium (S<sub>1</sub> — not same function — same as old LEM)
- SUB = Substitute (S<sub>2</sub> — not same function)
- ESC = Escape (S<sub>3</sub> position — same meaning but new code)
- FS = File Separator (S<sub>4</sub>)
- GS = Group Separator (S<sub>5</sub>)
- RS = Record Separator (S<sub>6</sub>)
- US = Unit Separator (S<sub>7</sub>)
- DEL = Delete (RUBOUT)

Figure 16 - ASCII (X3.4-1968) Chart

*Page 16:*

4.06 At the start of a signal for any character or function, the start (spacing)
interval releases the selector armature which under tension of its spring, moves
away from the magnet pole piece and thus, unblocks the start lever. The start
lever turns clockwise under the tension of its spring to move the start bail
into the indent of its cam.

4.07 As the start bail rotates about its pivot point, the attached stop arm is
moved out of engagement with the clutch shoe lever. The selector cam clutch
engages and begins to rotate. By this time, the start lever tip has moved into
the selector armature extension cut-out and the armature starts moving in
correspondence with the signal bits. Between the second and third signal bit,
the lift lever is pivoted clockwise by the start bail cam and lifts the start
lever above the armature extension. At this same time, the start bail rides to
the high point of its cam where it remains to hold the start lever away from the
selector armature until late in the character cycle. In approximately the middle
of the cycle the lift lever rides down its cam, thus, lowering the start lever.
When the stop impulse at the end of the signal is received, the selector
armature is pulled up to block the start lever. Thus, the start bail is
prevented from dropping into the low part of its cam (stop position of cam
sleeve, and the attached stop arm is held so as to stop the clutch shoe lever).

4.08 The selector cam clutch disc upon which the latchlever rides has an indent
at each of its two stop positions. When the clutch shoe lever strikes the stop
arm, the inertia of the cam disc assembly causes it to continue to turn until
its lug makes contact with the lug on the clutch shoe lever. At this point, the
latchlever drops into the indent in the cam disc, and the clutch is held
disengaged until the next start interval is received.

4.09 The series of up to eight selecting levers and the marking and spacing
locklevers ride their respective cams on the selector clutch and cam sleeve
assembly. As the marking and spacing signal intervals are applied to the
selector magnet, the selector cam sleeve rotates and actuates the selector
levers. When a spacing interval is received, the marking locklever is blocked by
the end of the armature and the spacing locklever swings toward the right above
the armature and locks it in the spacing position until the next signal
transition is due. Extensions on the marking locklever prevent the selector
levers from following their cams. When a marking impulse of the signal is
received, the spacing locklever is blocked by the end of the armature and the
marking locklever swings to the right below the armature to lock it in the
marking position until the next signal transition is due. During this marking
condition the selector levers are not blocked by the marking locklever
extensions, but are permitted to move against their respective cams. The
selecting lever that is opposite the indent in its cam, while the armature
maintains a marking condition, pivots to the right or selected position
momentarily. Each selecting lever has an associated push lever which drops off a
shelf on the top of the selecting lever when it rides into its cam indent. As
the cam sleeve turns, each selecting lever together with its latched push lever
is moved toward the left and held there until all eight code intervals have been
received. After all the selected push levers have been positioned to the left
and all unselected push levers have been positioned to the right, they are held
until the next start interval is received. When the subsequent start interval
again causes the cam sleeve to rotate, the push lever reset bail, in following
its cam, unlatches the selected push levers. The push levers then return to the
unselected (right) position under their spring tension.

4.10 The no, 1 push lever differs in that it uses an auxiliary no. 1 push lever
and auxiliary reset lever. When the no. 1 selector lever is permitted to follow
its cam (marking condition) the auxiliary no. 1 push lever is selected in the
same manner as other push levers. At this time the strip bail is on the high
part of its cam, resetting all the selected push levers above the shelves on
their associated selector levers. When the no. 1 selector lever returns
counterclockwise to the intermediate position on the cam, a tab on the auxiliary
no. 1 push lever engages the no. 1 push lever and drives it to the left in a
marking condition. At approximately midcycle the auxiliary push lever is
stripped by its auxiliary strip bail, thus, the auxiliary no. 1 push lever is
prepared for the next incoming marking pulse. The auxiliary lever action permits
normal strip operation to occur between no. 1 and no. 2 pulse selection.

4.11 The selector cam sleeve clutch has two stop positions and likewise the
individual cams have two complete identical contours in 360 degrees, providing
for two complete cycles of operation for each revolution of the cam sleeve.

*Page 17:*

<u>Note:</u> When rotating the main shaft by hand, the clutches will not fully
disengage upon reaching the stop position. In order to relieve the drag on the
clutch and permit the main shaft to rotate freely, apply pressure on the lug of
the clutch disc to cause it to engage its latchlever. This procedure should be
followed prior to applying power to the unit.

#### Start-Stop Operation (Figure 19)

4.12 Engage-disengage selector cam sleeve with main shaft; responds to start and
stop bits of a character.

Operation

Engage selector cam sleeve with main shaft.
- (1) Start (spacing) bit of new character deenergizes selector magnets and
  releases armature.
- (2) Armature, under tension of armature spring, falls against downstop
  bracket.
- (3) Absence of armature extension unlatches start lever which, under tension
  of start lever spring, pivots inward moving the stop arm bail into the indent
  of its cam. As the stop arm bail pivots inward, the attached stop arm pivots
  out of path of clutch shoe lever.
- (4) Clutch shoe levers expand to engage disc and cam sleeve assembly with
 rotating clutch drum.

Raise, reset, and lower start lever. Block clutch shoe lever.
- (1) Cam sleeve starts rotating. Selector cam sleeve mechanically operates its
  cam followers in a prearranged sequence as code level signals (marking or
  spacing) operate the armature (4.14).
- (2) Between the second and third character bit, lift lever elevates start
  lever above opening in armature extension. Stop arm bail rides to high part of
  stop arm cam forcing start lever away from armature, restoring stop arm to
  blocking position.

Disengage selector cam sleeve from main shaft.
- (1) Lift lever falls into indent of stop arm cam and lowers start lever.
- (2) Stop (marking) bit at end of character energizes selector magnets and
  attracts armature.
- (3) Stop arm cam presents indent to stop arm bail.
- (4) Stop arm bail begins to enter indent, but is prevented from entering fully
  by start lever whose inward movement is blocked by armature extension. Stop
  arm engages shoe lever to disengage cam sleeve from rotating clutch drum.

*Page 18:*

- (5) Clutch disc latched by latchlever.
- (6) Selector mechanism prepared to receive start (spacing) bit of subsequent
  character.

#### Push Lever Reset (Figure 20)

4.13 Strip the previous character from push levers after a start bit causes the
selector cam sleeve to engage the main shaft.

Operation

As cam sleeve begins rotating, high part of push lever reset bail cam lifts push
lever reset bail against tension of spring. Bail pivots, lifting and unlatching
the marking push levers from in front of their selector levers. The bail returns
to the unoperated position when the lobe drops from the high part of the cam.
All of the push levers, except the auxiliary push lever (4.15) will then be in
the spacing condition.

#### Selection (Figure 21)

4.14 Code selections are performed by sequentially positioning push levers as
marking and spacing intervals are applied to selector magnets.

Operation

View (A) - Idle Condition
- (1) Selector cam sleeve shown before starting selection cycle. Marking
  locklever, spacing locklever, and eight selector levers held against cam
  sleeve by their individual springs; the lobes of each lever are riding on high
  part of selector cam sleeve.
- (2) As marking and spacing signal intervals are applied to selector magnets,
  selector cam sleeve rotates and actuates selector levers.

*Page 19:*

<u>Note</u>: The range finder selects the most favorable period for sampling
character bits as received by the selector magnets. The range finder clamp arm,
when pivoted clockwise, permits the range finder scale adjustment. Turning the
range finder scale, mechanically adjusts the position of the stop arm, stop arm
bail, lift lever, and cam sleeve.

*Page 20:*

View (B) - Marking Condition
- (1) When marking impulse is received, the spacing locklever is blocked by end
  of armature extension. Top of marking locklever moves under armature
  extension, supporting armature in marking position until next signal
  transition is due.
- (2) During marking condition, selector levers are not blocked by marking
  locklever extensions, but are permitted to ride against their respective cams,
  Only that selector lever which is opposite the indent in its can affect its
  push lever,
- (3) As the lobe of the selector lever is drawn into its cam indent, the push
  lever drops off the shelf of its selector lever. When the selector lever is
  forced out of its indent, the selected push lever slides to the marking
  position.

View (C) - Spacing Condition
- (1) When spacing interval is received, the marking locklever is blocked by end
  of armature extension. Spacing locklever swings above armature extension and
  locks it in the spacing position until next signal transition is due.
- (2) During spacing condition, selector levers are prevented from riding their
  respective cams by extensions on marking locklever.
- (3) Lobe of selector lever opposite its cam indent cannot enter indent fully.
  Push lever will not latch behind selector lever, but will remain on shelf.

*Page 21:*

*Page 22:*

#### Auxiliary Push Lever (Figure 22)

4.15 Auxiliary push levers sense marking or spacing position of selector lever
no. 1. Normal strip operation (push lever reset) occurs during reception of code
bit no. 1 and does not permit push lever no. 1 to sense position of its selector
lever.

Operation

Auxiliary push lever responds to marking impulse for push lever no. 1. When bit
no. 1 is marking, auxiliary push lever drops behind shoulder of selector lever
as push lever no. 1 is stripped. Tab on auxiliary push lever carries push lever
no. 1 to marking position. When push lever reset bail (4.13) returns to
unoperated position, push lever no. 1 is behind, but not touching, its selector
lever. Approximately half way through selection cycle, auxiliary push lever is
stripped by auxiliary reset lever (4.16). Push lever no. 1 is then latched by
selector lever no. 1.

4.16 The conditions for the trip and reset mechanism are to strip the count on
typebox retraction mechanism; reset auxiliary push lever and intermediate arm
latch bail, and trip codebar clutch.

*Page 23:*

#### Trip Cam and Reset Mechanism (Figure 23)

4.17 The codebar clutch trip cam conditions the trip and reset mechanism to
strip the count on typebox retraction mechanism; reset auxiliary push lever and
intermediate arm latch bail, and trip codebar clutch.

Operation

As cam sleeve rotates, high part of cam ope rates retraction reset lever.
Approximately midcycle, second high part of cam operates auxiliary reset lever.
Tab on auxiliary reset lever strips auxiliary push lever, and pawl resets
intermediate arm latch bail in transfer mechanism (4.18). About the same time,
first high part of codebar clutch trip cam operates codebar clutch trip lever to
initiate operation of codebar shift mechanism (4.19).

*Page 24:*

### B. Transfer Mechanism

4.18 The coded input from the selector levers are conveyed to the codebar shift
mechanism through the transfer mechanism (Figure 1) by the selected positions of
the push levers to the transfer levers that set up the codebar shiftbars.

Operation

Code Bit Marking
- (1) Push lever latches in front of selector lever. As selector lever and push
  lever move toward front, push lever engages intermediate arm.
- (2) Intermediate arm and transfer lever assembly pivots, causing transfer
  lever to push codebar shiftbar toward rear. Extension on intermediate arm
  latches on top of intermediate arm latch bail.

Code Bit Spacing
- (1) Push lever remains on shoulder of selector lever. No action is transferred
  to intermediate arm.
- (1) Intermediate arm and transfer lever assembly remains unselected, extension
  on intermediate arm remains under latch bail, and codebar shiftbar is held
  toward front.

Strip Intermediate Arms
- (1) Intermediate arm latch bail is operated by auxiliary reset lever (4.16) at
  approximately midcycle.
- (2) Previously marking transfer levers return spacing if their respective push
  levers are now spacing.

*Page 25:*

### C. Codebar Shift Mechanism

4.19 The purpose of the codebar shift mechanism (Figure 25) is to transfer
mechanical positions of codebar shiftbar to codebars.

Operation

- (1) Codebar clutch trip lever, operating from cam of selector cam sleeve,
  trips codebar clutch (4.17). Codebar cam going from low to high part, imparts
  transverse motion to cam follower lever. Cam follower lever, by way of
  follower shaft, raises and lowers shift lever link.
- (2) As shift lever moves upward, front codebar shift lever moves all spacing
  codebar shiftbars to the right. Meanwhile, the rear codebar shift lever moves
  all marking codebar shiftbars to the left.
- (3) When shift lever link returns to lowest position, front and rear codebar
  shiftbars are open (front lever to left and rear lever to right) to permit
  codebar shiftbars to be repositioned. Each codebar shiftbar can pivot within
  slot of codebar permitting previous character to remain in codebar mechanism
  as bits of subsequent character are received.

*Page 26:*

### D. Codebar Mechanism

4.20 In the Model 37 typing unit there are 8 codebars and 3 blocking bars
(Figure 26). They are numbered 1 through 11 from the bottom up. The first seven
codebars have two basic uses. First to control the horizontal and vertical
positioning clutches, and second along with the other four bars to be read by
the function box to perform functions. Bar no. 8 is a parity check by the
function box on function codes. Bar no. 9 is used to suppress functions in the
function box and is also used as a gate for Escape sequences. Bar no. 10 is used
as a gate for Escape sequences and may suppress functions if required. Both bars
(9 and 10) are moved by shift forks controlled through the function box when so
equipped. Bar no. 11 is an auxiliary bar which may serve a variety of purposes.
Automatic carriage return is one of the uses for which the no. 11 bar is
intended.

### E. Codebar Positioning

4.21 As the selector finishes its cycle it positions all selected (marking) push
levers towards the front of the machine (Figure 27). As the push levers start to
move they impart a motion to the intermediate levers in the codebar positioning
mechanism which in turn imparts motion to the bottom of the transfer levers
causing the top of the transfer levers to move toward the rear of the machine.
The top portion of the selected transfer levers contacts their corresponding
codebar shiftbars and move the shiftbars toward the rear of the machine; thereby
placing the step in the shiftbars in the path of the shift lever. The shift
lever now begins to move under power from the codebar clutch and drives all
marking shiftbars and corresponding codebars to the left. A second shift lever
drives all spacing (nonselected) shiftbars and corresponding codebars to the
right. The codebars have now been fully positioned and the codebar shift levers
return to their previous position. The selected intermediate levers are now in a
latched condition and therefore are holding the transfer levers and shift levers
marking (toward the rear) unt11 midway through the next cycle of the selector
where upon they will be stripped allowing the shiftbars to return to the spacing
condition (toward the front of the unit). Note that the shiftbars return to
spacing in their front to rear direction, but retain their positions from left
to right. This allows each codebar to remain in position (mark or space) until a
change in code for the level occurs.

4.22 The purpose of codebars is to transfer binary information from codebars to
clutch trip slides associated with horizontal and vertical positioning. The
operation of the marking codebar will drive the clutch trip slide downward. Each
clutch trip slide will operate when its codebar is shifted.

Escape Sequence

4.24 Escape sequences are implemented in the unit in the stunt box in
conjunction with a no. 9 and no. 10 blocking bar.

4.25 Escape is received in the stunt box by a function bar in slot 9 for the no.
9 blocking bar and in slot 25 for the no. 10 blocking bar. Its function lever
shifts the no. 10 blocking bar byway of a fork shift mechanism and latches with
a stripper blade latch,

4.26 The no. 9 and no. 10 blocking levers are similar to a codebar and are
positioned above the codebar assembly, These blocking bars act as a gate that
opens for the duration of one machine cycle.

4.27 The no. 10 blocking bar, when selected, unblocks the function bar of the
second character of the sequence. These function bars are special in that they
have a no. 10 blocking tine to be gated by the no. 10 blocking bar.

*Page 27:*

\[Figure]

- TIE BAR
- SHIFT IN/SHIFT OUT (Slot No. 32)
- NO. 10 SHIFT FORK (Escape)
- NO. 9 SHIFT FORK
- CODEBAR MARKING
- CODEBAR SPACING
- CLUTCH TRIP LEVERS
- NO. 1 CLUTCH TRIP SLIDE
- NO. 2 CLUTCH TRIP SLIDE
- NO. 3 CLUTCH TRIP SLIDE
- NO. 4 CLUTCH TRIP SLIDE
- NO. 9 BLOCKING BAR (Escape or Suppression)
- NO. 10 BLOCKING BAR (Escape)
- NO. 11 BLOCKING BAR (Automatic Carriage Return)

Figure 26 - Codebar Inputs - Horizontal Positioning

*Page 28:*

4.28 After second character of the sequence following escape has been selected,
the escape function lever is unlatched by the stunt box stripper blade which
closes the gate again for any second character sequence selection.

4.29 The second character in the sequence is always print and space suppressed.
For a three character sequence its implementation is as follows: Escape will
open the gate for the second character to come in which in turn unblocks the
adjacent to the left third character function bar for selection. The function
lever of the third character will print and space suppress its own selection and
will be the output link of the sequence.

### F. Typebox and Typebox Carriage

4.30 All alpha, numeric, and special characters are printed by type pallets that
are arranged in the typebox (Figure 28). The typebox has 6 horizontal rows with
16 positions for a total of 96 pallet positions. An 8-row 128 pallet typebox is
available with minor modifications to the unit. The typebox carriage rides on
bearings horizontally over the typebox rail (Figure 29). The carriage is spaced
across the platen in conjunction with the print hammer mechanism by cables
attached to the spacing drum. In order to print any selected character, the
typebox carriage is so positioned that the character on the pallet is directly
over the required location on the paper. Hence, it is necessary to position the
typebox horizontally and vertically. The oscillating rail, which is connected to
the horizontal positioning mechanism, positions the typebox to the left or
right. The typebox rail positions the typebox ina vertical plane, through the
vertical clutches and eccentric links attached to a block, which drives the
typebox rail up and down.

*Page 29:*

<table>
  <thead>
    <tr>
      <th></th>
      <th>1S<br>2M<br>3M<br>4M</th>
      <th>1S<br>2M<br>3S<br>4M</th>
      <th>1S<br>2M<br>3M<br>4S</th>
      <th>1S<br>2M<br>3S<br>4S</th>
      <th>1S<br>2S<br>3M<br>4M</th>
      <th>1S<br>2S<br>3S<br>4M</th>
      <th>1S<br>2S<br>3M<br>4S</th>
      <th>1S<br>2S<br>3S<br>4S</th>
      <th>1M<br>2M<br>3M<br>4M</th>
      <th>1M<br>2M<br>3S<br>4M</th>
      <th>1M<br>2M<br>3M<br>4S</th>
      <th>1M<br>2M<br>3S<br>4S</th>
      <th>1M<br>2S<br>3M<br>4M</th>
      <th>1M<br>2S<br>3S<br>4M</th>
      <th>1M<br>2S<br>3M<br>4S</th>
      <th>1M<br>2S<br>3S<br>4S</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>SO<br>_234_<br>__8</td>
      <td>LF<br>_2_4_<br>___</td>
      <td>AK<br>_23__<br>___</td>
      <td>SX<br>_2___<br>__8</td>
      <td>FF<br>__34_<br>___</td>
      <td>BS<br>___4_<br>__8</td>
      <td>ET<br>__3__<br>__8</td>
      <td>NL<br>_____<br>___</td>
      <td>SI<br>1234_<br>___</td>
      <td>VT<br>12_4_<br>__8</td>
      <td>BL<br>123__<br>__8</td>
      <td>EX<br>12___<br>___</td>
      <td>CR<br>1_34_<br>__8</td>
      <td>HT<br>1__4_<br>___</td>
      <td>EQ<br>1_3__<br>___</td>
      <td>SH<br>1____<br>__8</td>
      <th>5S<br>6S<br>7S</th>
    </tr>
    <tr>
      <th>1</th>
      <td>RS<br>_2345<br>___</td>
      <td>SB<br>_2_45<br>__8</td>
      <td>SY<br>_23_5<br>__8</td>
      <td>D2<br>_2__5<br>___</td>
      <td>FS<br>__345<br>__8</td>
      <td>CN<br>___45<br>___</td>
      <td>D4<br>__3_5<br>___</td>
      <td>DL<br>____5<br>__8</td>
      <td>US<br>12345<br>__8</td>
      <td>ES<br>12_45<br>___</td>
      <td>EB<br>123_5<br>___</td>
      <td>D3<br>12__5<br>__8</td>
      <td>GS<br>1_345<br>___</td>
      <td>EM<br>1__45<br>__8</td>
      <td>NK<br>1_3_5<br>__8</td>
      <td>DI<br>1___5<br>___</td>
      <th>5M<br>6S<br>7S</th>
    </tr>
    <tr>
      <th>2</th>
      <td>N<br>_234_<br>_7_</td>
      <td>J<br>_2_4_<br>_78</td>
      <td>F<br>_23__<br>_78</td>
      <td>B<br>_2___<br>_7_</td>
      <td>L<br>__34_<br>_78</td>
      <td>H<br>___4_<br>_7_</td>
      <td>D<br>__3__<br>_7_</td>
      <td>@<br>_____<br>_78</td>
      <td>O<br>1234_<br>_78</td>
      <td>K<br>12_4_<br>_7_</td>
      <td>G<br>123__<br>_7_</td>
      <td>C<br>12___<br>_78</td>
      <td>M<br>1_34_<br>_7_</td>
      <td>I<br>1__4_<br>_78</td>
      <td>E<br>1_3__<br>_78</td>
      <td>A<br>1____<br>_7_</td>
      <th>5S<br>6S<br>7M</th>
    </tr>
    <tr>
      <th>3</th>
      <td>^<br>_2345<br>_78</td>
      <td>Z<br>_2_45<br>_7_</td>
      <td>V<br>_23_5<br>_7_</td>
      <td>R<br>_2__5<br>_78</td>
      <td>\<br>__345<br>_7_</td>
      <td>X<br>___45<br>_78</td>
      <td>T<br>__3_5<br>_78</td>
      <td>P<br>____5<br>_7_</td>
      <td>_<br>12345<br>_7_</td>
      <td>[<br>12_45<br>_78</td>
      <td>W<br>123_5<br>_78</td>
      <td>S<br>12__5<br>_7_</td>
      <td>]<br>1_345<br>_78</td>
      <td>Y<br>1__45<br>_7_</td>
      <td>U<br>1_3_5<br>_7_</td>
      <td>Q<br>1___5<br>_78</td>
      <th>5M<br>6S<br>7M</th>
    </tr>
    <tr>
      <th>4</th>
      <td>.<br>_234_<br>6__</td>
      <td>*<br>_2_4_<br>6_8</td>
      <td>&<br>_23__<br>6_8</td>
      <td>"<br>_2___<br>6__</td>
      <td>,<br>__34_<br>6_8</td>
      <td>(<br>___4_<br>6__</td>
      <td>$<br>__3__<br>6__</td>
      <td>SP<br>_____<br>6_8</td>
      <td>/<br>1234_<br>6_8</td>
      <td>+<br>12_4_<br>6__</td>
      <td>'<br>123__<br>6__</td>
      <td>#<br>12___<br>6_8</td>
      <td>-<br>1_34_<br>6__</td>
      <td>)<br>1__4_<br>6_8</td>
      <td>%<br>1_3__<br>6_8</td>
      <td>!<br>1____<br>6__</td>
      <th>5S<br>6M<br>7S</th>
    </tr>
    <tr>
      <th>5</th>
      <td>&gt;<br>_2345<br>6_8</td>
      <td>:<br>_2_45<br>6__</td>
      <td>6<br>_23_5<br>6__</td>
      <td>2<br>_2__5<br>6_8</td>
      <td>&lt;<br>__345<br>6__</td>
      <td>8<br>___45<br>6_8</td>
      <td>4<br>__3_5<br>6_8</td>
      <td>0<br>____5<br>6__</td>
      <td>?<br>12345<br>6__</td>
      <td>;<br>12_45<br>6_8</td>
      <td>7<br>123_5<br>6_8</td>
      <td>3<br>12__5<br>6__</td>
      <td>=<br>1_345<br>6_8</td>
      <td>9<br>1__45<br>6__</td>
      <td>5<br>1_3_5<br>6__</td>
      <td>1<br>1___5<br>6_8</td>
      <th>5M<br>6M<br>7S</th>
    </tr>
    <tr>
      <th>6</th>
      <td>n<br>_234_<br>678</td>
      <td>j<br>_2_4_<br>67_</td>
      <td>f<br>_23__<br>67_</td>
      <td>b<br>_2___<br>678</td>
      <td>l<br>__34_<br>67_</td>
      <td>h<br>___4_<br>678</td>
      <td>d<br>__3__<br>678</td>
      <td>`<br>_____<br>67_</td>
      <td>o<br>1234_<br>67_</td>
      <td>k<br>12_4_<br>678</td>
      <td>g<br>123__<br>678</td>
      <td>c<br>12___<br>67_</td>
      <td>m<br>1_34_<br>678</td>
      <td>i<br>1__4_<br>67_</td>
      <td>e<br>1_3__<br>67_</td>
      <td>a<br>1____<br>678</td>
      <th>5S<br>6M<br>7M</th>
    </tr>
    <tr>
      <th>7</th>
      <td>~<br>_2345<br>67_</td>
      <td>z<br>_2_45<br>678</td>
      <td>v<br>_23_5<br>678</td>
      <td>r<br>_2__5<br>67_</td>
      <td>|<br>__345<br>678</td>
      <td>x<br>___45<br>67_</td>
      <td>t<br>__3_5<br>67_</td>
      <td>p<br>____5<br>678</td>
      <td>DE<br>12345<br>678</td>
      <td>{<br>12_45<br>67_</td>
      <td>w<br>123_5<br>67_</td>
      <td>s<br>12__5<br>678</td>
      <td>}<br>1_345<br>67_</td>
      <td>y<br>1__45<br>678</td>
      <td>u<br>1_3_5<br>678</td>
      <td>q<br>1___5<br>67_</td>
      <th>5M<br>6M<br>7M</th>
    </tr>
  </tbody>
</table>

Figure 28 - 8-Row Typebox Arrangement

<u>Note</u>: Typebox arrangement ASCII 68 as viewed from print hammer.

*Page 30:*

*Page 31:*

### G. Horizontal Positioning

4.31 The purpose of the horizontal positioning (Figure 30) is to translate the
mark-space setting of four codebars (1 through 4) into the selection of one
position out of sixteen possible transverse positions of the typebox. The four
codebars concerned are each connected to the aggregate motion mechanism by a
bellcrank which in turn drives a clutch stop slide. The slide has two extensions
so placed that when the slide is at one extreme of its movement one extension
will stand in the path of a clutch arm, and at the other extreme the opposite
extension will stand in the path of the same clutch arm displaced by 180
degrees. By this means each codebar controls the stopping position of a clutch
to one side or the other.

\[Figure]

- CODE LEVEL 1
- CODE LEVEL 2
- CODE LEVEL 3
- CODE LEVEL 4

(Front View)

Figure 30 - Horizontal Positioning Mechanism

4.32 There are four clutches in the horizontal positioning mechanism (Figure
31). Each clutch carries an eccentric which drives a rod carrying the movement
impart by the eccentric to the aggregate motion linkage (Figure 32). The
aggregate motion linkage consists of a system of three levers of double sided
design pivoted one on the other by precision miniature ball bearings in such a
pattern that the four input movements originating at the eccentric and under the
control of the codebars are made to produce a movement at the output of the
mechanism which in turn is connected to the oscillating rail (Figure 29).

4.33 The rail which runs the full length of the printer is supported by two arms
one at each end which in turn are pivoted on the front plate. At the connection
of the rail and the arms are two pulleys upon which rides the rear spacing
cable. One end of the cable is fastened to the spacing drum. From this point, it
passes part way around the spacing drum, upward and around the right oscillating
rail pulley, over to the left oscillating rail pulley, and downward to the
spring drum. After passing part way around the spring drum, the cable is doubled
backward around it and passes upward to the left printing carriage rail pulley
over to the right printing carriage rail pulley, and downward to the spacind
drum to which it is again fastened. As the oscillating rail is moved in a
horizontal arc by the horizontal aggregate, the cable is moved as a unit with
respect to the oscillating rail. Attached to the cable but free to move on the
rail is a sled. This sled is in turn connected to the typebox carriage by the
arm.

<u>CAUTION</u>: DO NOT OPERATE TYPING UNIT WITH TYPEBOX REMOVED, UNLESS TYPEBOX
LATCH TOGGLE IS CAMMED OVER THE TYPEBOX CARRIAGE.

### H. Horizontal Dampener Mechanism

4.34 This mechanism is located behind the carriage return spring drum (Figure
33). The purpose of this mechanism is to dampen out oscillation of the typebox
and to make final correction of type alignment. As the typebox reaches a
printing position a roller mounted on an arm and controlled from a cam on the
print hammer clutch engages a detent wheel which in turn is connected through a
gear to a rack on the oscillating rail support arm. This locks in the position
of the typebox and immediately releases after the print hammer strikes the
pallet. The dampener mechanism is designed so that the horizontal positioning
can override the detent mechanism without serious damage although this condition
should not be permitted to exist for more than a few printer cycles.

*Page 32:*

*Page 34:*

Operation

View as shown is a stop condition. As oscillating rail is driven to left or
right, it will pivot oscillating arm which in turn will rotate the horizontal
dampener detent disc. When printing clutch trips, the detent arm will move up it
will allow detent lever to move into horizontal dampener detent disc.

### I. Vertical Positioning

4.35 The vertical positioning (Figure 34) codebars (5, 6, and 7) are connected
in a manner almost identical to those in the horizontal mechanism. Three
clutches in turn cause movement to be applied to an aggregate motion mechanism,
which gives eight output positions (Figure 35). The output end of this mechanism
is made to drive a vertically mounted rack on the left side of the machine. This
rack is connected to the rail carrying the typebox and is connected to a similar
rack on the right side of the machine through a cross shaft and associated
pinions. In this manner the aggregate motion mechanism causes the rail to be set
in the selected vertical position, but parallelism is maintained between the
rail and the machine center line.

*Page 35:*

*Page 36:*

### J. Vertical Dampening

4.36 The vertical dampening mechanism (Figure 36) is similar in principle to
horizontal dampener and is located on the cross shaft mentioned in 4.34.

Operation

View as shown is in a stop condition. As printing clutch trips, the dampener cam
follower rides high portion of dampener cam, rotating dampener shaft
counterclockwise. As dampener shaft rotates, a spring connected from the detent
arm to the detent lever, causes the detent lever roller to move into the
vertical dampening detent disc.

*Page 37:*

### K. Trip Shaft Mechanism

4.37 The trip shaft mechanism (Figures 6 and 37), located on the back of the
unit, performs one or two operations when the codebar clutch is tripped:
engagement of the function clutch or the print hammer clutch and the spacing
clutch. The reason the function clutch operates first is to determine if a
function has been selected. If a function has been selected the function bar
operates its function lever which operates the suppression bail. When the
suppression bail is operated (pushed forward), the suppression hook operates and
blocks the printing and spacing clutches from operating. Engagement of the
function clutch is started when a carriage return, line feed or any function or
suppressed character is initiated from the function box. If a character
selection is received, the function box does not operate the suppression bail
and the print and spacing clutches are allowed to operate, refer to 4.42.

4.38 When the codebar clutch is tripped the trip shaft cam rotates, and the trip
shaft starts its sequence of operations. The operation of the function clutch
and print hammer clutch is controlled by the trip shaft cam attached to the
codebar clutch on the main shaft. The spacing clutch is tripped by the cam
follower arm mounted on the print hammer clutch. The movement of the trip shaft
is a clockwise or counterclockwise pivoting action which is caused by the trip
shaft cam follower mounted to the trip shaft, refer to Figure 37.

*Page 38:*

Engage Function Clutch

4.39 Refer to Figures 37 and 38; as the codebar clutch rotates, the trip shaft
cam follower rides the high portion of the trip shaft cam, which pivots the trip
shaft ina counterclockwise direction. When the shaft rotates, the function
clutch trip arm pivots, engaging a post on the intermediate lever, causing the
function clutch trip lever to move out of engagement with the function clutch
shoe lever engaging the function clutch.

Engage Print Hammer Clutch

4.40 The trip shaft continues to rotate (Figure 39, the trip shaft cam follower
rides into a low portion of the cam, pivoting the trip shaft in a clockwise
direction. This movement causes the print hammer clutch trip arm to engage the
print hammer clutch trip lever, and moves it out of engagement with the print
hammer clutch shoe lever, operating the print hammer clutch.

*Page 39:*

Engage Spacing Clutch

4.41 As the print hammer clutch rotates, the spacing clutch cam follower arm
rides on the high portion of spacing clutch trip cam, located on print hammer
clutch (Figure 40). This action causes the spacing clutch trip lever to move out
of engagement with the spacing clutch shoe lever engaging the spacing clutch.

Print and Space Suppression

4.42 After the engagement of the function clutch and a function or suppressed
character has been selected in the typing u.nit, the function lever in the
function box moves the suppression bail in contact with the suppression slide
(Figure 41). The suppression slide moves the suppression latch that hooks the
post on the cam follower holding the trip shaft cam follower away from the trip
shaft cam. This operation prevents the trip shaft from pivoting, thus,
inhibiting the print hammer clutch and spacing clutch from engaging.

*Page 40:*

### L. Print Hammer Carriage and Printing Drive Mechanism

4.43 After the typebox has been moved so that the selected type pallet is in its
proper position, it must be struck by a printing hammer in order to print. This
is accomplished by the action of the printing carriage located on the printing
carriage square shaft (Figures 42 and 43).

4.44 The printing carriage rides (on rollers) on the square shaft, which is
carried in bearings mounted to the printer front plate. Rotation of the complete
carriage is prevented by a tracking guide which is part of the carriage frame
assembly and is arranged to follow a steel tracking plate attached to the main
framework of the front plate assembly. The carriage is clamped to the front
spacing cable. This moves the carriage along its track in such a manner that the
hammer advances to the next printing position.

4.45 The printing movement of the hammer is provided by the oscillation of the
square shaft, which is driven through a linkage and drive shaft on the right
side of the unit by a cam on the print hammer clutch. As the printing cycle
begins the square shaft rotates towards the front of the unit transmitting power
through the four rollers to the reset plate. The reset plate in turn drives the
accelerating lever, print hammer lever and print hammer. In this way the print
hammer is driven away from the platen while extending the accelerating lever
spring and allows the accelerating lever to be latched with the latchlever. The
square shaft now begins to rotate toward the rear of the unit to a predetermined
position. At this point the latch is released and the hammer accelerates toward
the pallet carrying it into the ribbon and paper. A return spring then pulls it
out of the path of the pallets where it is picked up through the accelerating
lever and the reset plate by the now forward motion of the square shaft. The
print hammer is then latched in a temporary latched position and the cycle is
completed.

4.46 The force of the hammer blow may be varied to suit single or multiple copy
printing. Clockwise rotation of the knurled knob on the carriage unit to the
position where two notches are up, shifts the hammer spring anchor to give the
spring higher tension. In this setting the machine will give up to six copies on
normal multicopy paper. If single copy is being used, life of the ink ribbon
will be prolonged and clearer copy produced by using the lower tension setting
with one notch on the knob facing up.

Print Hammer Carriage

Operation

View as shown is in a stop position. As square shaft rotates clockwise, the
reset plate will rotate clockwise moving accelerating lever and hammer lever
clockwise, allowing latchlever to latch accelerating lever. As square shaft
rotates counterclockwise, the reset plate will rotate counterclockwise, pivoting
the latchlever clockwise. This releases accelerating lever and hammer lever to
move forward, driving print hammer forward.

*Page 41:*

Printing Drive Mechanism

Operation

View as shown is in a stop condition. As printing clutch trips, the print hammer
cam follower will ride high portion of print hammer cam. This will cause drive
shaft to rotate clockwise allowing drive arm to rotate clockwise. As drive arm
pivots, it causes drive link to move upward rotating square shaft
counterclockwise. As square shaft pivots counterclockwise, it loads and latches
the print hammer mechanism and feeds the ribbon. As print hammer cam follower
rides low portion of print hammer cam, it will cause square shaft to rotate
clockwise tripping print hammer mechanism.

*Page 42:*

### M. Spacing Mechanism

4.47 To properly space the printed characters (Figure 44), the typebox and
printing carriage must be advanced with each character printed. The carriages
are connected to cables (4" 33) which, in turn is fastened to the spring drum,
which contains a torsion spring. The purpose of the spring drum is to keep
tension on the cable rope and carriage (to the left). The spacing drum has
ratchet teeth about its periphery, which are engaged by the eccentric driven
spacing drum feed pawls. The spacing shaft, on which the spacing eccentrics are
mounted, is driven through its helical gear by the helical driving gear attached
to the six-stop spacing clutch on the main shaft. The gear ratio of 3 to 1
causes the spacing shaft to turn one-half of a revolution each time the spacing
clutch is tripped. This allows the feed pawls to advance the spacing drum by the
amount of the ratchet tooth.

4.48 A cam on the print hammer clutch trips the spacing clutch through a bail
which pivots on the trip shaft. This cam is designed so as to allow spacing to
occur after the character has been printed.

### N. Backspace Mechanism

4.49 A backspace signal is received by the printer and recognized by the
function box. Motion is transferred from the function box through a slide arm
and bail which passes through an opening in the front plate. This action
depresses the intermediate lever which actuates the backspace bail through a
link. As the backspace bail begins to rotate a spring pulls the backspace
blocking pawl into engagement with the spacing ratchet on the spacing drum
(Figure 44). Continued rotation of the backspace bail causes the spring to
stretch, putting pressure on the blocking pawl and also lifting the spacing
pawls clear of the spacing ratchet. The spacing drum returns approximately
one-half space under carriage return spring tension until its motion is blocked
by the blocking pawl. The spacing drum, spacing cables, print hammer carriage,
and typebox carriage maintain this position until the function pawl in the
function box is stripped near the end of the machine cycle. Upon stripping of
the function the entire linkage is returned to its previous state, thereby
returning the spacing pawl to the ratchet and removing the blocking pawl from
the ratchet. This allows the spacing drum to return an additional one-half turn
thereby completing a full backspace.

*Page 43:*

Backspace Mechanism — Wide Platen

4.50 The initial operation of the backspace operation for the wide platen
(Figures 11 and 12) is the same as the standard unit. When a signal for
backspace is received, it is recognized by the function box and motion is
transferred from the function box to a slide arm and a bail which extends
through the front plate (Figure 45). The backspace for the wide platen has a new
mechanism mounted on the rear of the stunt box, to trip the spacing clutch
(Figure 12) and the spacing mechanism is different. The changes include the
elimination of the blocking pawl and redesigned spacing feed pawls and linkages.
These changes are the result of the increased length of the platen and the
stronger carriage return spring.

4.51 When the signal for backspace is received, the selected function pawl and
lever in slot no. 9 of the stunt box is positioned to the rear. This movement of
the function lever operates a slide which operates a bail extension that extends
through the front plate. The bail extension actuates a lever with a post which
pivots about an eccentric shoulder screw. A blocking lever is mounted on the
post, when activated, the blocking lever moves the lower spacing pawl away from
the ratchet wheel and is then latched by a latchlever. The blocking lever
remains latched and free of the bail and slide until the spacing clutch is
tripped.

4.52 When the selected function pawl, in slot no. 9 of the function box, is
positioned to the rear, the upward motion of the stripper blade operates the
backspace bail extension mounted at the rear of the stunt box. The bail
extension, when operated, will trip the spacing clutch by means of a link with
an eccentric mechanism. As the spacing clutch rotates, the upper spacing pawl is
driven downward and is followed by the reverse rotation of the spacing drum
which reacts under tension of its carriage return spring. Simultaneously, the
lower spacing pawl is driven upward and is stripped from the blocking lever to
engage and hold the spacing drum. These procedures complete the backward
movement of the spacing drum one space which is determined by the spacing pawls
in relation to the ratchet with lower spacing pawl being kept away from the
ratchet by the blocking lever during its upward movement, refer to Figure 45.

*Page 44:*

### O. Retraction Mechanism

4.53 The purpose of this mechanism (Figures 46 and 47) is to reposition the no.
5, 6, and 7 codebars spacing and to lower the typebox for viewing of the printed
copy. The mechanism is designed to begin lowering the box in a minimum of 10
milliseconds after the character has been printed; but if before this time has
elapsed the next character trips the selector clutch, the mechanism is reset and
retraction will not occur.

4.54 The retract mechanism consists basically of a ratchet driven through a feed
pawl by a cam and a blocking pawl controlled by a cam on the selector cam sleeve
assembly.

4.55 The ratchet is driven continuously by the feed pawl. Attached to the
ratchet is an arm which contacts a slide. If no character is received by the
unit in the time mentioned above the slide will have moved into contact with a
set of bails in the vertical slide control linkage causing the linkage and
slides to go into a spacing condition. This causes all vertical positioning
clutches that were marking to go spacing thereby lowering the typebox to its
lowest position. Upon the reception of a character by the selector, a linkage is
operated by a cam on the selector cam sleeve which moves the blocking pawl from
engagement with the ratchet causing the ratchet and slide to be reset. The
vertical positioning clutch control linkage and clutch remain in a spacing
condition thereby leaving the typebox retracted until normal positioning of the
typebox takes over.

*Page 45:*

Operation

When the selector clutch is operating, its selector trip cam will drive cam
follower clockwise allowing arm and transverse shaft to rotate counterclockwise.
As transverse shaft rotates, a slide will be moved towards the rear moving check
pawl away from the ratchet. This will prevent retraction slide from moving
towards the front of the unit.

Operation

If unit remains in an idle condition, the feed pawl cam follower riding high
portion of eccentric cam will cause feed pawl to move upward, rotating the
ratchet counterclockwise and allow check pawl to override one tooth. As ratchet
rotates, its trip plate will push bellcrank and retraction slide forward. As
feed pawl moves upward the latchlever latches it. As feed pawl cam follower
rides low portion of eccentric gear, the feed pawl will rotate clockwise away
from ratchet. As eccentric gear rotates, a pin attached to it will cause
latchlever to rotate counterclockwise releasing feed pawl to come back in
engagement with ratchet.

*Page 46:*

### P. Function Box and Function Box Drive Mechanism

4.56 The function box in the Model 37 is very similar to that of other
teletypewriter equipment (Figures 48, 49, and 50). The major difference is the
coding of the function bars. The function bar tines are numbered 1 through 11
from the bottom to the top. This numbering corresponds to the number of the
codebars mentioned in 4.20 of this section. Refer to Figure 60 for function bar
coding.

*Page 47:*

Operation

View as shown is in a stop condition. As function clutch trips, the stripper
blade cam will allow the stripper blade cam follower to permit its upper roller
to ride the low portion of cam and the lower roller to ride high portion of cam.
The stripper blade cam follower will rotate clockwise driving drive link upward.
As drive link moves up, the camming shaft will rotate clockwise. At this time
the drive arms will rotate clockwise moving stripper blade downward. When
stripper blade moves up, it will "strip" selected function pawls from function
bars.

*Page 48:*

### Q. Ribbon Positioning Mechanism

4.57 The normal position of the ribbon is below the printing line (Figures 51
and 52). That portion of the ribbon which is directly in front of the print
hammer is raised by a ribbon guide to allow the pallet to strike the ribbon and
print the character. The ribbon guide and guide control arm are moved along
separate shafts beneath the platen by a connection to the print hammer carriage.
The shaft upon which the guide control arm rides is oscillated by a linkage
controlled from the print hammer clutch. Immediately after the character has
been the ribbon is lowered to allow full view of the entire printed line.

*Page 49:*

*Page 50:*

Black Ribbon

When the printing clutch trips, the follower arm will ride the low portion of
cam, allowing the follower arm to pivot clockwise. As the follower arm rotates,
it will pull the transfer link down until it hits against the blocking slide.
The transfer link moving downward will cause the printing shaft to rotate
clockwise, moving the ribbon guide up. The ribbon will only move up far enough
to put the black field of ribbon in front of the print hammer.

Red Ribbon

The magnet energizes pulling the block slide to the rear. When the printing
clutch trips, the follower arm will ride the low portion of the cam allowing the
follower arm to pivot clockwise. As the follower arm rotates, it will pull the
transfer link down. Since the blocking slide is to the rear, it will not block
the travel of the transfer link, therefore, it will move further down. The
transfer link moving further down will cause the printing shaft to rotate more
in a clockwise direction. The printing shaft moving further in a clockwise
direction will cause the ribbon guide to move further up. This will put the red
field of ribbon in front of the print .hammer.

<u>Note</u>: The typing unit requires an ink impregnated nylon ribbon; the
Teletype part numbers are: TP181125 for black and TP326184 for red/black. The
Bell coded part numbers are: 61215 for black and 62215 for red/black.

### R. Ribbon Feeding and Reversing Mechanism

4.58 At each end of the square shaft on which the print hammer carriage rides is
mounted a ribbon feed mechanism and ribbon spool (Figure 53). Each ribbon
mechanism consists basically of a ratchet, feed pawl, check pawl and the ribbon
reversing mechanism. The ratchet upon which the ribbon spool is mounted is
driven by the feed pawl which in turn is powered by the oscillation of the
square shaft, through a drive arm, link and bail. While one ribbon mechanism is
feeding, the other is in a free running condition. A ribbon reverse mechanism
controls which mechanism is feeding.

4.59 On the outside of each ribbon feed mechanism is mounted a guide lever and a
blocking lever. The feed pawl and check pawl in the nonfeed condition are held
away from the ratchet by a reversing lever, which is detented in one of two
positions by a detent lever. The reversing action is initiated by the eyelet at
the end of the ribbon as it comes off the spool and moves the guide lever to the
rear, which causes the latching surface of the blocking lever to move upwards
into the path of the feed pawl extension. As the motion of the feed pawl
extension is being blocked during the backstroke, the feed pawl rotates into
engagement with the ratchet; and moves the reversing lever over to its other
detented position. Through a connecting rod the reversing lever of the other
ribbon feed mechanism moves its feed pawl and check pawl out of engagement with
the ratchet, and keeps this mechanism in a nonfeed condition, The feed pawl
which was previously in a nonfeed condition is now driving the ratchet, and the
ribbon is moving in the opposite direction. The following two paragraphs and
Figure 54 detail the ribbon feeding and reversing operation.

Ribbon Feeding

When the square shaft rotates in a clockwise direction, the feed pawl drive
clamp moves the drive link toward the rear of the unit, causing the right drive
bail to rotate in a clockwise direction. As the right drive bail rotates, the
right feed pawl moves toward the front of the unit, moving the ribbon ratchet in
a clockwise direction. When the square shaft rotates counterclockwise the right
feed pawl will move toward the rear of the unit, overriding a tooth on the
ribbon ratchet. At this time the right check pawl will hold the ribbon ratchet.

Ribbon Reversal

When the left feed pawl is doing the feeding and the right ribbon spool is
approaching the end of the ribbon, the reversing eyelet will pull the right
guide lever towards the rear of the unit, allowing the right blocking lever to
move up. When the right feed pawl moves towards the front of the unit, it will
become latched upon the right blocking lever. As the right feed pawl moves
towards the rear of the unit, it will pivot clockwise moving the right reversing
lever clockwise. This action causes the connecting rod to move to the right,
rotating the left reversing lever clockwise, moving the left feed pawl and left
check pawl out of engagement with the left ribbon ratchet. The right feed pawl
is now doing the feeding.

*Page 52:*

*Page 53:*

### S. Print, Space, and Function Suppression

4.60 When certain functions are selected it is necessary to suppress printing
and spacing. This is accomplished through the function box by the function lever
moving the suppression bail which in turn moves the suppression slide forward
where it will hold the suppression interposing lever in a position to prevent
full movement of the trip shaft cam follower. In this way the trip shaft will
not 'be able to rotate far enough to trip the printing clutch, and thereby also
prevent tripping of the spacing clutch (4.37 through 4.42 and 4.56).

4.61 The print, space, and function suppression is an optional feature that
enables a typing unit to be placed into a condition where printing, spacing, and
all functions are suppressed. This feature is electromagnetically operated
(Figure 55) and requires an electrical service unit that has the associated
driver circuit. The DC2 code combination initiates the suppressed condition
which prevents all printing, spacing, and any function box actuated function
except the release code combination of DC4 or ETX.

4.62 This optional feature requires the DC2, DC4, and ETX function bars and
their associated function box parts and contact assemblies. In addition to the
above the Escape no. 9, and optionally the Escape no. 10 shift fork mechanisms
are required. A modified shift fork for the Escape no. 9 is located in slot no.
7, and a function bar and shift fork mechanism in slot 22 with a link connecting
the shift forks. Printing and spacing is suppressed by locking the suppression
bail into the forward position, and the general functions such as line feed and
carriage return by shifting and locking the no. 9 suppression codebar in the
marking position. The Escape sequences such as tab set and tab clear are
accomplished by preventing the noo 10 codebar from being latched in the marking
position for one function selection following the code combination Escape.

*Page 54:*

4.63 In the normal operation of the printer, the magnets are not energized and
the engaging fork on the armature is held in the up position. When the armature
is up, the linkage causes the latch in slot 22 to be held out of engagement with
its function lever, and the action of the latch in slot 25 is unimpaired. If
Escape 10 is not provided, the references to slot 25 should be disregarded.

4.64 When the printer receives a DC2, the two function bars located in slots 18
and 22 will be selected and returned to their rearward position along with their
respective pawls and function levers. The following sequence describes the
operation.

- (1) The function lever in slot 18 will close a contact which completes a
  circuit to cause the two magnets to be energized and electronically locked in
  the energized condition.
- (2) The function lever slot 22, through its shift fork and linkage to the
  shift fork of slot 7, will shift the no. 9 codebar to the right. The lower
  portion of the function lever will move the suppression bail forward.
- (3) The magnets, now energized, will cause the armature to move downward
  carrying with it the post of the bail. The angular motion given to the bail
  now allows the latch in slot 22 to block the return of its function lever to
  the forward position. Another arm on the bail now engages the latch in slot 25
  and prevents it from _blocking its function lever.
- (4) The DC2 function pawls are stripped by the stripper blade. The function
  lever in slot 22, blocked by its latch, remains in position. The suppression
  bail remains forward, the no. 9 codebar remains to the right, and the latch in
  slot 25 (Escape no. 10) remains disabled. Printing, spacing and all functions
  except DC4 and ETX are disabled and will remain so until current to the
  magnets is interrupted.
- (5) The DC4 and ETX functions are coded so that they can be selected even if a
  printer is in the suppressed condition. When the printer receives either DC4
  or ETX a circuit is completed which breaks the circuit to the magnets.
- (6) As the magnets are de-energized, the armature moves upward under spring
  force. This motion is transmitted through the bail to strip the latch from its
  function lever in slot 22. The function lever, the suppression bail, and the
  no. 9 codebar return to their normal positions and the latch in slot 25 is now
  able to function. The printer is now in its normal mode. As is shown above, a
  break in the circuit to the magnets will return the printer to the normal
  state.

### T. Carriage Return Mechanism

4.65 The carriage return mechanism is located to the right of center of the
typing unit (Figure 56). Reception of the carriage return code causes the
carriage return function bar, pawl and lever to operate, The lower end of the
function lever engages the carriage return slide arm and pushes it forward. The
slide arm, in turn, moves the carriage return bail about its pivot point. As the
front portion of the bail moves downward, it takes with it the lower section of
the spacing drum feed pawl release link. This causes the upper portion of the
link to turn and disengage the spacing drum feed pawls from the spacing drum.
When the carriage return bail reaches its lowest point, the carriage return
latch bail locks it there. The disengagement of the spacing drum feed pawls from
the spacing drum permits the spring drum to return the printing and typebox
carriages toward the left side of the typing unit. As the spacing drum nears the
end of its counterclockwise rotation, the roller on its stop arm contacts the
transfer slide which, in turn, drives the dashpot piston into the dashpot
cylinder.

4.66 A small passageway with an inlet from the inside of the cylinder and two
outlets to the outside is incorporated in the end of the cylinder. The size of
the outlets are controlled by adjustable members. The lowest outlet is
controlled directly by a setscrew which opens and closes the passageway. The
upper outlet is controlled by a spring loaded ball. These two outlets determine
the rate at which the air may escape from the cylinder.

4.67 When the spacing drum reaches its extreme counterclockwise position a post
on the transfer slide contacts the carriage return latch bail and thereby allows
the carriage return bail to be released permitting the feed pawls to engage the
spacing drum.

*Page 55:*

### U. Line Feed Mechanism

4.68 The line feed mechanism is located at the left side of the typing unit.
Upon the receipt of the line feed code, the lower end of the line feed function
lever engages the line feed slide arm and pushes it forward. The slide arm, in
turn, moves the line feed clutch trip arm and the trip lever about their pivoted
point until the trip lever releases the six-stop line feed clutch. The line feed
gearing is such that each one-sixth revolution of the clutch will advance the
platen by one line. Therefore, the length of time that the line feed clutch trip
lever is held away from the clutch will determine the number of line feeds that
occur. The timing relationship between the stripper blade cycle and the main
shaft rotation is such that the function pawl is not stripped from a function
bar until after more than one-sixth of a revolution of the clutch has occurred.
When a single line feed is desired, it is necessary to strip the function pawl
from the line feed function bar before the line feed clutch completes one-sixth
of a revolution. This is accomplished by an auxiliary stripper which is mounted
on the stripper blade, and protrudes above the blade thereby causing the
function pawl to be stripped earlier in the cycle than would normally occur if
stripped by the standard position of the blade. The auxiliary stripper is
allowed to slide from left to right under the control of a lever which is
pivoted on the side frame. Through this lever the slide can be manually
positioned into or out of the path of the line feed function pawl. In this way
single or double line feed is achieved by manually positioning the lever in its
two-position detent.

4.69 Each one-sixth revolution of the line feed clutch causes its attached spur
gear to rotate the line feed eccentric spur gear and its attached eccentrics
one-half of a revolution. The eccentrics, which are offset in. opposite
directions, each carry a line feed bar. These bars, guided by the line feed bar
bellcrank, alternately engage the line feed spur gear on the platen and advance
the platen one line for each one-half turn of the eccentrics.

4.70 When it is desired to manually position the platen, this may be
accomplished by turning the platen handwheel. The platen handwheel spur gear
engages the platen idler spur gear which in turn, is engaged with manual line
feed knob causing the line feed bar release lever to bear on the line feed bar
bellcrank and causes it to disengage the line feed bars from the line feed spur
gear.

*Page 56:*

### V. Vertical Tabulation Mechanism

4.71 Vertical tabulation mechanism provides a means for rapidly positioning the
paper in the line feed direction across the length of the form. Stop positions
are predetermined by a set of tabs contained in a tab wheel (Figure 57). A stop
can be provided for every line on the form. Vertical tabulation code will
tabulate the paper to the next tab-stop. A form-feed tab contained in the tab
wheel meters the length of the form. The form-feed code will tabulate the paper
to the next form-feed stop.

<u>Note</u>: Vertical tabulation and on-line control of tab-stop positions,
operates the same for wide platen units.

4.72 The tabulating speed is three line feeds per machine cycle and is capable
of tabulating one line or any number of lines within the form length per machine
cycle. The addition of the fractional line feed feature to the unit will cut the
tabulating speed in half.

4.73 Vertical tabulation provides for nonrepeat form-feed. This feature makes
form-feed operable only after sending a line feed or vertical tabulation at some
earlier time. Tab wheels are equipped for the maximum form length; if shorter
form lengths are desired and these are within the capability of the particular
wheel (various size wheels are available), the vertical tab-stops must be
removed and replaced with a form-feed stop supplied with the unit, refer to
Figure 57. The function box operation is based upon two different design styles
and are described as follows:

- (a) Units equipped with the nonrepeat formfeed (FF) function pawl latchlever
  (new style): Operates when the form-feed function pawl is stripped by the
  stripper blade and is latched up by the nonrepeat form-feed latch. This will
  prevent the machine from repeating tabulating on FF. Form feeding is
  reinstated upon the receipt of a line feed or vertical tabulation.
- (b) Units equipped with nonrepeat form-feed function bar blocking lever: This
  feature prevents the unit from form feeding when the tab wheel is in
  registration. Registration is when the form-feed sensing pawl is resting on
  the form-feed tab which normally occurs. on line feed, reverse line feed,
  vertical tab or form-feed. Through the form-feed linkage, a blocking lever is
  moved into the path of the form-feed function bar, thereby preventing
  (blocking) the function bar from sensing the codebars. The form-feed becomes
  operable only after sending a line feed or vertical tabulation to cause the
  tab wheel to advance one or more positions.

*Page 57:*

On-Line Control of Tab-Stop Positions

4.74 The vertical tabulation mechanism provides for off-line or on-line tab-set
and tab-clear; form-feed is mechanically operated off the function box by the
vertical tabulation and form-feed code, and the function box contact indicates
the duration of the tabulation. On-line tab-set is actuated by the code ESC5 and
tab-clear is ESC6. Tab-stops are set and cleared by the tab-set and tab-clear
arms that are activated by cables directly off their respective function levers
in the function box. The procedure for setting up a vertical tab format is as
follows.

- (1) Initiated form-feed can be done manually by positioning the tab wheel to
  the form-start position, or on-line by keying form-out. When positioning the
  tab wheel manually, in the case when new paper is inserted, care should be
  taken that the detent roller is fully detenting the line feed spur gear on
  units equipped with fractional line feed. To fully detent the roller, depress
  the one-half line feed (forward or reverse) key once and then manually
  position the tab wheel to the form-start position.
- (2) Follow by line feeds (full line feed only) to position the paper to the
  required stop position" The required stop position might be determined by
  actually spacing the required preprinted form through the machine or by
  predetermining the format and then counting out the number of line feeds.
- (3) Having located the required tabulation-stop position, a tab is set by
  keying ESC5. Tab wheels being divided into two or more form lengths will
  require a repetition of above procedure making sure that the tab format is the
  same on every segment of the tab wheeL
- (4) Vertical tab-clear is performed by actuating and latching up the tab-clear
  arm and at the same time initiating vertical tabulation. The tab-clear arm
  provides a camming surface which will cam any set tab-stops into the clear
  position as the tab wheel rotates. The tab-clear arm is again unlatched at the
  end of the form by the form-out tab-stop which is retained in the tab wheel.
- (5) The tab-clear function lever is in slot no. 40 in the stunt box next to
  vertical tabulation. When tab-clear is selected, its function pawl will also
  pick up the vertical tabulation function lever, and thereby operate both the
  tab-clear arm and vertical tabulation.
- (6) Tab-stops are cleared to the end of the form starting from the position
  the form was in at the time tab-clear was initiated. To clear all tab-stops,
  tab-clear should be preceded by form-out. Tab wheels being divided into two or
  more form lengths will require two or more tab-clears. Since tab-clear is
  performed in conjunction with vertical tabulation, the transmitter control
  contact, if used, will also control tab-clear.

<u>Note</u>: When transmitting at full speed, two deletes are required after the
tab-clear to allow the transmitter to shut off during the tab-clear operation.

### W. Horizontal Tabulation Mechanism

4.75 The horizontal tabulation mechanism provides for rapidly positioning the
carriage across the length of the line with predetermined stop positions. Tabs
are contained in a tab wheel mounted on the spacing drum and these tabs provide
a stop for every space in the line. The tabulating speed is three times the
spacing speed and is mechanically operated off the function box by the
horizontal tab code. The length of time the tabulation mechanism will operate is
controlled by the associated contact assembly mounted on the function box.

4.76 The operation of the horizontal tabulation mechanism consists of the
tabulation wheel being swept past a tab sensing pawl. A tab-stop in the set
position passing this pawl will stop tabulation. After tabulation is started in
the function box, the function lever will trip the spacing clutch by a slide and
operating lever. The operating lever is then latched through the extension link
by the tab sensing blocking lever. The operating lever in the latched position
will keep the spacing clutch engaged. The horizontal tabulation function lever
is retained in the slide which in turn is held captive in the operating lever.
When the operating lever is latched during tabulation, the function lever is
also held in the selected position. The function box contact on top of the
horizontal tabulation function lever will therefore provide transmitter control
during tabulation. A pres tripper, mounted on the stripper blade, prestrips the
function pawl early enough to permit the tabbing of one space.

On-Line Control of Horizontal Tab-Stop Positions

4.77 For on-line control of horizontal tab-set and tab-clear, the tab-stop
positions are located in the horizontal tab whee 1. This optional feature is
operated by the code sequence ESCl and tab-clear by ESC2. Tab-stops are set and
cleared by the tab-set and tab-clear arms which are actuated by cables directly
off their respective function levers in the function box. Horizontal tab-clear
is performed by actuating and latching up the tab-clear arm and at the same time
starting horizontal tabulation. The tab-clear arm provides a caroming surface
which will cam any tab-stops that are set into a clear position as the tab wheel
rotates. The tab-clear arm is again unlatched at the end-of-line by the
end-of-line tab which is located in the tab wheel. The tab-clear function lever
is in slot no. 16 in the function box next to horizontal tabulation. When
tab-clear is selected, its function pawl will also pick up the horizontal
tabulation function lever and thereby operate both the tab-clear arm and
horizontal tabulation. Tab-stops are cleared to the end-of-line, starting from
the position the carriage was in at the time tab-clear was initiated to clear
all tab-stops. The tab-clear should be proceeded by carriage return.

*Page 58:*

<u>Note</u>: When transmitting at full speed, two deletes are required after the
tab-clear to allow the transmitter to shut off during the tab-clear operation.

Horizontal Tabulation — Wide Platen

4.78 The horizontal tabulation and horizontal tab-stop control mechanism
operates the same as the standard units and the mechanism is similar. The
configuration and mounting of the tabulation and tab-stop control mechanism on
the wide platen unit varies from the standard unit. The differences are the
physical location, design of the parts, and a sensing cable has been added in
place of a link.

4.79 The addition of the horizontal tab sensing cable changes the horizontal
sensing pawl operations for the wide platen unit. When the signal for horizontal
tabulation is received, the selected function lever is positioned to the rear
and latches the selected lever. The function lever is held selected by an
auxiliary latch. When the sensing pawl senses a set tab, the pawl is pushed
away, operating a cable that is connected to the auxiliary latch. The downward
movement of the sensing cable on the latch releases the selected function lever
which stops tabulation.

### X. Half-Forward and Reverse Line Feed

4.80 The half-forward and reverse line feed mechanism is provided as an option
that feeds the paper in a forward or reverse direction. This mechanism operates
at 150 WPM and can be used with friction or sprocket feed units and the wide
platen units. The paper advance is half the speed of the standard line feed
mechanism and only single copy paper can be used. The operation is upon receipt
of selected code signals. The accepted code signals (Escape sequences) that will
operate this mechanism are as follows:

- LF will feed the platen one line forward.
- ESC7 will feed the platen one line in reverse.
- ESC8 will feed the platen one-half line in reverse.
- ESC9 will feed the platen one-half line forward.

4.81 The stunt box mechanism for the functions reverse LF, one-half reverse LF,
one-half LF and LF are located in slots 35, 36, 37, and 38, respectively. When
the code signal for one-half LF or LF is recognized by the stunt box, the
forward slide is moved forward by the function lever action. Likewise when
reverse LF or one-half reverse LF is selected, the reverse slide is moved
forward. The forward motion of the slides causes the clutch tripbail to rotate
forward, causing the trip arm and clutch trip lever to move about their pivot
point until the line feed clutch is released and starts rotating, refer to
Figures 58 and 59.

4.82 The line feed clutch has six stop-lugs. The mechanical connection between
the clutch and the platen is such that each one-sixth revolution of the clutch
will advance the platen one-half line. In order to stop the rotation of the line
feed clutch, the function pawl is stripped off the function bar by the upward
motion of the stripper blade, allowing the clutch trip lever to fall in and
engage a stop-lug. The timing relationship between the line feed clutch rotation
and the stripper blade cycle is such. that the clutch trip lever will fall in
and stop the clutch on the second stop-lug. The LF and reverse LF functions are
stripped in this manner, causing the line feed clutch to rotate one-third of a
revolution and thus advancing the platen one line in either forward or reverse
direction. In order to advance the platen one-half line, the function pawls for
the one-half LF and one-half reverse LF functions must be. stripped off earlier
so the clutch trip lever can fall in and engage the first stop-lug. This is
obtained by, a prestripper attached to and extending above the stripper blade.
During the upward motion, the prestripper will strip off the function pawl in
time to stop the line feed clutch after one-sixth of a revolution.

*Page 59:*

\[Figure]

- CLUTCH TRIPBAIL
- GUIDEBAR
- 326041 SLIDE ARM (Reverse)
- SLIDE (Forward)
- FUNCTION LEVERS
  - (35) REV LF
  - (36) 1/2 REV LF
  - (37) 1/2 LF
  - (38) LF

(Top View)

Figure 58 - Function Box for Half-Forward and Reverse Line Feed Mechanism

4.83 Each one-sixth revolution of the line feed clutch causes its attached gear
to rotate the eccentrics assembly one-half of a revolution. The eccentrics, with
an eccentricity half that of the standard line feed mechanism, are offset in
opposite directions, each carrying a line feed bar. A spring loaded roller
engages the line feed bars above the eccentrics and causes them to bear against
the platen gear. The roller also serves as a common pivot point for the bars as
they alternately engage the platen gear to advance the platen one-half line
forward for each one-half turn of the eccentrics.

4.84 The reversing action of the line feed mechanism occurs in the following
manner: When the reverse LF or one-half reverse LF signal is recognized by the
stunt box, the reverse slide is moved forward and causes the line feed clutch to
engage. The forward movement of the reverse slide also provides motion to the
bail, link and blocking lever to bring the blocking roller up into the slots of
the lower ends of the line feed bars. This causes the common pivot point of the
line feed bars to be shifted from the roller above the eccentrics to the
blocking roller below. As the eccentric assembly rotates, the line feed bar in
the high position is moved away from the platen gear. The line feed bar in the
low position stays in engagement with the platen gear during its movement to the
high position, thus causing a reversing action of the platen.

*Page 60:*

*Page 61:*

### Y. Function Bar Coding

4.85 The function bar code chart, Figure 60, shows the coding for the ASCII. The
table at the end of this section shows the coding for the common function bars.
The no. 8 tine is shown for even parity. If odd parity or no parity is desired,
the 8th lever may be altered. Refer to Figure 56 to code the function bar tines
1 through 8, and refer to the following instructions for coding the 9th, lOth,
and 11th tines.

4.86 The no. 9 tine senses the condition of the no. 9 blocking bar. The blocking
bar is in a normal mode (print mode of machine) when it is to the right and in
the alternate mode (nonprinting mode) when it is to the left (as viewed from the
front). The blocking bar is usually positioned in the alternate mode by the
reception of an ESC code. For further discussion of the use of ESC codes see
escape sequences (4.23).

4.87 When coding a function bar it must be decided if the no. 9 tine is to
respond in the normal mode or alternate mode. If it is to respond in the normal
mode, the.tine on the left (as viewed from the front) should be removed. If it
is to respond in the alternate mode, the tine on the right should be removed.

4.88 In principle, the no. 10 and no. 11 blocking bars operate similar to the
no. 9. The difference being that when coding a function bar to respond to the
normal mode, the tine on the right (as viewed from the front) must be removed
and in the alternate mode, the tine on: the left must be removed.

4.89 On machines equipped with automatic carriage return and line feed, both
tines of the 11th level must be removed unless they are automatic carriage
return line feed function bars.

4.90 Function bars which are used to control the position of the blocking bars
must have both tines removed for the level that they control.

*Page 62:*

\[Figure]

- 11 BLOCKING BAR
- 10 " "
- 9 " "
- 8 CODEBAR
- 7 " "
- 6 " "
- 5 " "
- 4 " "
- 3 " "
- 2 " "
- 1 CODEBAR

Figure 60 - Function Bar Code Chart (Even Parity)

## 6. APPENDIX

### A. Printed Graphics Extension (Shift-Out, Shift-In)

6.01 The printed graphics extension feature provides 32 additional graphics that
are obtained by placing the typing unit into the shift-out mode. SO (Shift-Out)
key on the keyboard locks the typing unit, in the shift-out condition until
terminated by sending the function SI (Shift-In) bn the keyboard. In the
shift-out mode the typing unit will print the new set of graphics when keying
capital letters on the keyboard and will print symbols and numeric characters.
The 32 additional graphics feature requires a 8-row typebox where the top two
rows contain the additional type pallets. A 7-row typebox is available where
only 16 additional characters are needed. These additional graphics are not
standardized and each typebox can be filled to the customer's need.

6.02 In the shift-out mode the no. 7 code level positioning clutch is locked
spacing (Figure 35) which positions the typebox to the 0, 1, 4, and 5 rows,
refer to Figure 28. When the no. 7 positioning clutch is spacing, only the
characters in the above mentioned rows in the typebox can be printed. Refer to
Figure 61 to understand the operational sequence that follows.

- (1) The SO key on the keyboard is selected.
- (2) The function bar in slot 30 operates and pulls back the associated
  function lever and locks in the latched position.
- (3) The function lever operates the shift fork mechanism which moves the
  function box slide to the left. (The slide is spring loaded to the right as
  viewed from the front.)
- (4) The function box slide drives the shift-out slide to the left. (The
  shift-out slide is spring loaded to the right as viewed from the front.)
- (5) When the shift-out slide is driven to the left, the no. 7 codebar bail
  with plate is disengaged from the post that is on the shift-out slide. This
  action uncouples the no. 7 codebar bail which when coupled, operates the no. 7
  clutch trip link.

6.03 The results of the above operation are the no. 7 clutch trip link does not
move back to trip the no. 7 clutch to go marking; therefore, the no. 7 clutch is
in the spacing condition. The function box has a contact assembly which is
operated by the shift-out function lever to indicate the shift-out mode and its
duration by a lamp on the control panel.

6.04 The shift-out mode is terminated by sending a SI function from the
keyboard. The SI function releases the function lever in slot no. 30, releasing
the shift fork-mechanism and moves the slides to the right. When the slides are
to the right the two bails are coupled by the post on the shift-out slide and
the typing unit is in the normal printing condition; which permits printing and
spacing on lower case characters.

*Page 64:*

### B. Visual Aid With Graphic Extension

6.05 The visual aid modification kit (Figure 62) is a guide to assist the
attendant in using a typing unit with the printed graphic extension feature
described above. This feature consists of an overlay with a pictorial
representation of the keyboard and holder that adheres magnetically to the front
cover of the typing unit.

6.06 The overlay (Figure 63) is plastic with a nonreflective surface that is
receptive to printing and lettering, so that the additional graphic symbols and
characters can be placed in their respective positions by the customer. With the
visual aid in place, the attendant can visualize which key to depress by
relating the position of the desired character or symbol to the keyboard letters
printed on the overlay.

### C. Character Received Contact Mechanism

6.07 The character received contacts are mounted in back of the selector and
provides a set of contacts which close and open on every selector cycle to
permit recognition of the selector rotation for each character received. The
character received contacts (Figure 64) are used in system applications that are
defined by the customer's requirements. When these contacts are connected to
external circuits, the contacts provide electrical pulses which may be
synchronized with code reading contacts for circuit control. An example would be
to inform the sending station or an internal circuit that a character signal has
been received and acted upon. These contacts are available in normally open or
normally closed (standard) arrangements.

6.08 The operation of the contact assembly is accomplished when the operating
lever which follows the periphery of the existing selector clutch disc, pushes
and releases the contact plunger, opening and closing the contacts. For each
half revolution of the clutch disc, the selector completes one cycle and
operates the contact mechanism. The contact closure (normally closed) will occur
after the start of the no. 1 information pulse and will open before the end of
the no. 7 pulse for a 10-unit code with unity stop pulse. When the selector is
in the stop position, the contact points will remain open.

6.09 The contacts are gold plated and rated for 48 volts de maximum at 10 ma
resistive load. For maximum contact life, the customer should provide contact
protection circuitry suited to the designed load. These are mechanical contacts
and bounce can occur; therefore, associated circuitry should be designed
accordingly.

*Page 65:*

\[Figure]

- OVERLAY
- OVERLAY WITH ADDED GRAPHICS

*Pages 66–68:*
