*Source*: <https://www.navy-radio.com/manuals/tty/m37/574-304-100-iss2-7212.pdf>

<div style="display: flex; justify-content: space-between;">
<div>BELL SYSTEM PRACTICES<br>AT&TCo Standard</div>
<div style="text-align: right;">SECTION 574-304-100<br>Issue 2, December 1972</div>
</div>

<h1 style="text-align: center; font-size: 1.2em; padding-left: 10%; padding-right: 10%;">
37 KEYBOARD SEND-RECEIVE (KSR) TELETYPEWRITER SET
USED IN TELEGRAPH TEST BOARDS AND SERVICE BOARDS
GENERAL DESCRIPTION AND OPERATION
</h1>

## CONTENTS

- [1. GENERAL](#1-general)
- [2. DESCRIPTION](#2-description)
  - [STANDARD FEATURES](#standard-features)
  - [COMPONENTS](#components)
    - [A. Typing Unit](#a-typing-unit)
    - [B. Keyboard](#b-keyboard)
    - [C. Base](#c-base)
    - [D. Control Panel](#d-control-panel)
    - [E. Motor Unit](#e-motor-unit)
    - [F. Typing Unit Cover and Pan](#f-typing-unit-cover-and-pan)
    - [G. Electrical Service Unit](#g-electrical-service-unit)
  - [ACCESSORIES](#accessories)
- [3. TECHNICAL DATA](#3-technical-data)
- [4. OPERATION](#4-operation)
- [5. REFERENCES](#5-references)

Prepared for American Telephone and Telegraph Company by Teletype Corporation \
© 1969 and 1971 by Teletype Corporation \
All rights reserved \
Printed in U.S.A.

## 1. GENERAL

1.01 This section provides a general description and operation of 37 KSR
(Keyboard Send-Receive) TTY (teletypewriter) Sets (Figure 1) which are used in
test board service in either a 904G/H Data Test Center, No. 2 or No. 9B service
board or DOTC (Data Observing and Testing Center). The KSR set may be used in
conjunction with a 918A Multispeed and Code Converter. The set generates data
from a keyboard and converts received data into printed copy. Since the previous
issue was not available for general distribution, marginal arrows normally used
to indicate changes and additions have been omitted.

1.02 A 37 KSR TTY Set is a heavy-duty terminal that functions with the ASCII
(American National Standard Code for Information Interchange) and has EIA
(Electronics Industries Association) Standard RS-232-B interfacing.

Figure 1 - 37 KSR Teletypewriter Set Used in Test Board Service

1.03 The styling and equipment are designed to complement modern office
furnishings. The operator interface including keyboard layout and touch, quality
of printed copy and equipment noise is comparable to that of an office
typewriter. The console and typing unit are mounted in the teletypewriter
position of the Data Test Center or service board, and the electrical service
unit is mounted separately up to 10 feet away.

1.04 References to left or right, front or rear, top or bottom, etc, apply to
the set in its normal position as viewed by the operator.

1.05 The 37 KSR TTY Set originates data in the form of voltage signals, ie,
positive (+) voltage for spacing signals and negative (-) voltage for marking
signals. The voltage signals are used by the 37 KSR TTY Set to produce printed
data transmission from the set by serial signals.

1.06 Figure 2 is a block diagram illustrating the use of 37 TTY equipment in a
test board application. It should help in understanding the overall capabilities
of a 37 KSR TTY Set. The 37 KSR TTY Set is connected through a 918A Multispeed
and Code Converter, and an interface unit to a hub for communication with
stations of various speeds and signal codes. The typing unit operates at 150 wpm
which is one of the outputs of the 918A Code Converter. The keyboard reset
mechanism has gears that limit the resetting of the keyboard to 59 wpm, slightly
slower than the lowest speed station capable of communicating with the 918A
Converter. The converter can accept and transmit 5- and 8-level signals at 60,
75, 100, and 150 wpm. The 37 KSR TTY Set can also be used without the 918A
Multispeed and Code Converter, if desired.

Figure 2 - Test Board Application Using 37 Teletypewriter Equipment

<u>Note</u>: If the Multispeed and Code Converter 918A is not used, plug the EIA
connector from the YESU819 into the Data Test Center outlet panel. Cord A and
cord D are not used.

## 2. DESCRIPTION

2.01 Figure 3 and Chart show the TTY set which consists of the following
components:

- Typing Unit
- Keyboard
- Control Panel
- Motor Unit
- Typing Unit Cover and Pan
- Electrical Service Unit

CHART - TELETYPEWRITER SET DIMENSIONS

<table>
  <thead>
    <tr><th colspan=2>CONSOLE</th><th colspan=2>YESU819</th></tr>
    <tr><th colspan=2>DIMENSIONS</th><th colspan=2>DIMENSIONS</th></tr>
  </thead>
  <tbody>
    <td>Width</td><td>17-1/2"</td><td>Width</td><td>14-3/4"</td></tr>
    <td>Height</td><td>11-1/2"</td><td>Height</td><td>5-3/4"</td></tr>
    <td>Depth</td><td>19-1/2"</td><td>Depth</td><td>12-1/2"</td></tr>
  </tbody>
</table>

### STANDARD FEATURES

2.02 The following features are standard on this KSR TTY set:

- Modern modular design.
- Interfacing which conforms with EIA Standard RS-232-B except for motor control
  and shift to red leads.
- Printer receives at the speed of 150 wpm (15 characters a second) 10-unit
  code.
- Transmits from keyboard at 59.5 wpm.
- Generates all 128 ASCII characters with even parity.
- Receives all 128 ASCII characters - prints 94 common graphics including upper
  and lower case alphabet. Also prints and spaces for all control characters.
- Eighty-six characters on a line (12 per inch).
- Keyboard end-of-line indication (lamp).
- On-line carriage return and line feed.
- Local carriage return.
- Local paper feed-out.
- Two color printing.
- Operator control of multiple copy.
- Operator control of vertical spacing.
  1. 3 lines per inch.
  2. 6 lines per inch.
- Roll paper (friction feed sets).
- Print position indicator (next character indicator).
- Print position scale.
- Character repeat feature.
- Full duplex operation on-line with provision for typing unit to copy keyboard
  signals in local mode of operation.
- NEW LINE function (carriage return and line feed) in response to Carriage
  Return, Line Feed, Vertical Tabulation and/or Form Feed Characters.
- Automatic carriage return and line feed after 86 characters.
- Paper winder is used with the console. It is not part of the console.

### COMPONENTS

Figure 3 - 37 KSR Teletypewriter Set and Components

#### A. Typing Unit

2.03 The typing unit receives information serially by means of a single magnet
(two coils) type of selector. A function box is provided for character
recognition.

2.04 Page copy is provided by the typing unit which prints both upper and lower
case characters utilizing a typebox positioned by an aggregate motion mechanism.
The typebox is moved from character to character and is retracted when reception
stops, thus, making all characters visible when the machine is idle.

2.05 The typing unit is capable of printing symbols for 127 ASCII characters.
Space character is not printed. An eight row typebox is provided with pallets in
the upper two rows for 32 control characters.

2.06 Typing unit will print 12 characters per inch allowing 86 characters on an
8-1/2 inch platen with normal margins on the paper. Line feed provides for
spacing six lines per vertical inch. The suppression latch (TP306176) and spring
(TP90054) have been removed from the printer to provide spacing on every
character including functions.

2.07 A typing unit arranged for friction feed is capable of accommodating roll
paper in widths of 3 to 8-1/2 inches and capable of providing multiple copies of
one original and two carbons.

2.08 All typing units are equipped with line feed and carriage return (both
on-line and local), and serviceman adjustable margins.

#### B. Keyboard

2.09 A standard 4-row keyboard configuration (Figure 4) is used. The keytop
arrangement is consistent with a standard office typewriter.

2.10 The keyboard is an electromechanical device for generating ASCII code
combinations. It converts the mechanical depression of a key into electrical
code paths. Keys move codebars which control electrical contacts. The electrical
contacts present an even vertical parity parallel wire output to a keyboard
control logic card in the electrical service unit which converts the signals
into ASCII.

2.11 It is possible to generate all 128 code combinations of ASCII. Upper and
lower case alpha characters, numerics, and special graphic characters are
designated on the keytops. Control characters are designated on the keyboard in
two ways. The most often used controls appear on separate keys and are active in
both the shifted and unshifted modes without use of the CONTRL key. Another
group of controls appear on the same keytop with a graphic. To generate these
code combinations, it is necessary to depress the CONTRL key while the
particular key is struck. All control character designations requiring the
depression of the CONTRL key, as well as the individual key, appear on the
keyboard in charcoal grey.

2.12 A repeat feature is provided on every key. Further depression of the key
beyond its normal stop position will cause the associated character to be
generated repetitively at the maximum character rate of 59.02 wpm. The repeat
feature can be enabled or disabled by a serviceman.

Figure 4 - Keyboard Arrangement

#### C. Base

2.13 The base provides mounting facilities for the typing unit, motor unit, and
intermediate gear assembly. Holes are also provided on the base for mounting the
keyboard reset mechanism and margin indicator switch.

#### D. Control Panel

2.14 The control panel which is located above the keyboard contains 18
pushbuttons (keys). In addition, there are two mechanical pushbuttons (keys)
designated PAPER ADVANCE and LOCAL RETURN. The control panel arrangements are
shown in Figure 5. Functional descriptions of the different controls, and the
locations of controls within each arrangement, are given in Table A.

Figure 5 - Control Panel

**TABLE A - CONTROL PANEL SWITCHES AND LAMPS**

| DESIGNATION   | SWITCH | LAMP | DESCRIPTION                                                                         |
| ------------- | ------ | ---- | ----------------------------------------------------------------------------------- |
| MOTOR OFF     | L      |      | Turns off motor in on-line operation.                                               |
| CONTL BLACK   | L      |      | All characters printed in black.                                                    |
| KYBD E.O.L.   |        | X    | Illuminated at end of SO-character line. Turns off when character counter is reset. |
| BREAK         | N      |      | *                                                                                   |
| PAPER ADVANCE |        |      | Mechanically causes paper feed-out by printer.                                      |
| PARITY GEN.   | L      | X    | *                                                                                   |
| ERROR RESET   | N      | X    | *                                                                                   |
| UNSHIFT SPACE | L      |      | *                                                                                   |
| HOLD          | L      |      | *                                                                                   |
| PARITY DET.   | L      |      | *                                                                                   |
| LOCAL RETURN  |        |      | Mechanically causes printer to return carriage.                                     |
| 150 WPM (8)   | L      |      | *                                                                                   |
| 100 WPM (8)   | L      |      | *                                                                                   |
| 100 WPM (5)   | L      |      | *                                                                                   |
| 75 WPM (5)    | L      |      | *                                                                                   |
| 60 WPM (5)    | L      |      | *                                                                                   |

<u>Note</u>: L designates locking, N nonlocking.

*Wiring of switches and lamps are brought out "dry" through 36-pin connector for
use by the 918A Converter.

#### E. Motor Unit

2.15 The function of the motor is to provide electromechanical rotating motion
for operating the typing unit and keyboard reset mechanism.

2.16 The motor is a synchronous-type, rated at 1/20 horsepower, and is operated
from a 115 volt ±10 percent ac, single phase, 60 hertz ±0.75 percent source of
commercial power. It consists of a 2-pole wound stator with two windings (a main
running winding and a start winding), and a ball bearing rotor. A start relay,
capacitor, and thermal cutout switch are mounted in a compartment of the motor
mounting cradle.

#### F. Typing Unit Cover and Pan

2.17 The typing unit cover and pan includes copylights and provides the housing
for the typing unit, keyboard and base, motor, and control panel. The cover and
pan with assembled components mount onto a shelf in the Data Test Center.

2.18 The cover is hinged to the pan and can be easily removed, or it may be
raised and extended over interior components while maintenance is being
performed.

2.19 Two lids at the top of the cover provide access to the typing unit for
ribbon changing, replenishing paper supply, and adjusting print hammer for
multiple copy, etc.

2.20 Two connectors are provided at the rear of the console. P309 connects to
the YESU819 connector J309. J311 connects to the 918A Multispeed and Code
Converter.

#### G. Electrical Service Unit

2.21 The electrical service unit is a chassis assembly which mounts into the
Data Test Center. The chassis assembly has a multivoltage power supply, a wiring
field, and is equipped with five card connectors. A set of circuit cards
provides the logical operations for the set (Table B). The cards mount into the
card connectors.

2.22 Wiring from the card connectors terminates at the wiring field which
provides a centralized wiring location for the set. Two cables terminate at the
wiring field. One plug (J309) connects to the console. The other connector
provides a signal interchange point that connects to the 918A Converter which
generally conforms with the EIA-232-B Standard.

2.23 A power cord from the electrical service unit plugs in to an ac power
receptacle. The ac power for the set is provided over a single ac power cord
which terminates at one of the two terminal boards, and is fused with a 3.2
ampere, slow blow fuse.

2.24 A copylight transformer and motor control relay are also a part of the
YESU819 and derive their power from the multivoltage power supply in the
chassis. Copy lamps go on when the motor goes on.

2.25 The multivoltage power supply converts ac power into appropriate de power
which is used for internal set operation.

2.26 A circuit card extender board, mounted in the electrical service unit is
provided as a circuit card troubleshooting tool.

**TABLE B - CIRCUIT CARDS**

<table>
  <thead><tr><th>CIRCUIT CARD</th><th>PURPOSE</th></tr></thead>
  <tbody>
    <tr>
      <td>Keyboard Control Card (Piggyback on Character Counter-Z10)</td>
      <td>
        <ol><li>Receives output of keyboard contacts and converts the output
          to ASCII signals with even parity in 8th code level.</li>
        <li>Establishes proper parity before a character is read using the shift
          control sample signal. This prevents parity errors if the SHIFT or
          CONTL keys are operated before the character key.</li></ol>
      </td>
    </tr>
    <tr>
      <td>Distributor Card (Z09)</td>
      <td>Serializes the parallel data input from the keyboard. Serialized
        characters from the Distributor card are fed to the Timer and Interface
        card. Take Character, a control signal from the keyboard auxiliary
        contact (closes when a character is generated) is a command to start
        serialization.</td>
    </tr>
    <tr>
      <td>Receiving Device (Z07-Bottom)</td>
      <td>
        <ol><li>Drives the motor control relay in response to command from Timer
          and Interface card.</li>
        <li>Converts logic voltage level signals to power levels suitable for
          typing unit selector magnets.</li></ol>
      </td>
    </tr>
    <tr>
      <td>Character Counter (ZlO)</td>
      <td>Scans every character generated by the keyboard and presents a
        count-up (function and control characters omitted) signal to the counter
        control circuit. The counter is reset on RETURN or NEW LINE. It counts
        down on BACKSPACE characters from the keyboard only.</td>
    </tr>
    <tr>
      <td>Counter Control (Z06)</td>
      <td>Records count up, count down, and reset signals from the Character
        Counter card. At a preselected count it turns on EOL lamp. Card is
        programmed for 80 characters, but may be reprogrammed.</td>
    </tr>
    <tr>
      <td>Ribbon Control (Z07-Top)</td>
      <td>Controls the function of ribbon color selection upon receipt of signal
        from Timer and Interface card for red and from control panel and stunt
        box for black.</td>
    </tr>
    <tr>
      <td>Timer and Interface (Z08)</td>
      <td>
        <ol><li>Converts the Distributor card DTL signals to EIA Send Data
          output of set.</li>
        <li>Converts the EIA received data to DTL level signals for Receiving
          Device card.</li>
        <li>Contains a crystal controlled bit timer to provide timing signals to
          the Distributor card.</li>
        <li>Contains resistors for interface contact closures with their related
          control circuits for motor control operations.</li>
        <li>Provides signals to Ribbon Control card to shift ribbon to red.</li>
        <li>Permanently holds EIA leads Request To Send and Data Terminal Ready
          to high and Ring Indicator and Clear To Send to low state.</li></ol>
      </td>
    </tr>
  </tbody>
</table>

### ACCESSORIES

#### Paper Winder

2.27 The paper winder is mounted in back of the console and will accommodate
paper widths from 4-1/2 to 8-1/2 inches. It will wind 400 feet of single copy
paper. It will not handle multicopy paper.

2.28 The winder has its own motor, fused for 5 amps and is controlled by a power
switch and a mercury switch. When the paper from the typing unit goes slack due
to paper feed-out, the slack paper bail drops, the mercury switch is operated to
turn on the motor. The paper is wound up, the slack bail rises and the mercury
switch turns off the motor.

2.29 A paper display rack is used to elevate the paper off the console to
facilitate reading the copy.

## 3. TECHNICAL DATA

3.01 Electrical and Environmental Characteristics

1. Power:
   - 115 v ±10% ac
   - 60Hz ±0. 75Hz
2. Ambient temperature: From 400F to 1100F
3. Ambient relative humidity: From 0 to 95 percent
4. Power consumption: 250 watts

3.02 Physical Characteristics

1. Dimensions: See Chart
2. Weight: 115 pounds
3. Power cord:
   - Purpose: Provides ac power for entire set
   - Type: Single 3-pin polarized cord
   - Length: 8 feet from electrical service unit.
4. Interface cord
   - Purpose: Provides the Electronic Industries Association (EIA) interface
   - Type: 25-conductor plug
   - Length: 10 feet

3.03 Set Internal Power Supply

1. Multivoltage power supply
   - Output voltages:
     - +12.5 volts dc
     - ±7% maximum current 5 amperes
     - -12.5 volts dc ±5%
     - maximum current 3 amperes
     - +5.25 volts dc ±5%
     - maximum current 3 amperes
     - 12 volts ac
2. Other outputs
   - Output voltages:
     - 115 volts ac
     - 5.5 volts ac

3.04 Convenience outlet: maximum load 10 amps at 130 v ac

## 4. OPERATION

4.01 The KSR set interface leads originate at the electrical service unit. The
interface signals conform to EIA Standard RS-232-B. The interface leads which
have designations beginning with A (ie, AA) are ground leads. The interface
leads which have designations beginning with B (ie, BA) are data leads. The data
leads are positive (+) or high for spacing signals and negative (-) or low for
marking signals. The interface leads which have designations beginning with C
(ie, CB) are control leads. A positive (high) voltage on a control lead means it
is on, and a negative (low) voltage means it is off. The interface leads are
listed, by designation, in Table C along with the name and purpose of each lead.

<u>Note</u>: At the interface, EIA signals are converted into diode transistor
logic (DTL) signals and vice versa. DTL data signals are high (+5.5 volts) for
marking signals and low (zero volts or ground) for spacing signals. DTL control
signals are high when a lead is off and low when a lead is on. Thus, there is a
logic inversion when signals pass through the interface.

Figure 6 is a block diagram which shows the mutual relationship between the
various set logic cards of a 37 KSR TTY Set and identifies the EIA interface
leads. The following functional description of set operation is based upon
Figure 6.

4.02 The normal operation has the set in the on-line mode under the control of
other portions of the Data Test Center. The set will be in full duplex operation
where the keyboard and the printer are independent of each other.

4.03 Data communication is started with the set in the idle condition, Request
To Send, Clear To Send, Data Terminal Ready, and Ring Indicator are all
permanently on. This indicates the KSR and the interface unit are ready to
communicate.

4.04 The motor will start when the Data Test Center supplies a ground to the
Motor Control lead to pull up the motor control relay. The copy lamps will go
on. The motor will stay on until the ground is removed.

**TABLE C - EIA INTERFACE LEADS**

| DESIGNATION | NAME                | PIN NO. | PURPOSE                                                                                                                                                                                 |
| ----------- | ------------------- | ------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| AA          | Protective Ground   | 1       | To connect ac power service ground to equipment chassis. It is electrically isolated from signal ground.                                                                                |
| AB          | Signal Ground       | 7       | To provide ground for all signal circuits.                                                                                                                                              |
| BA          | Send Data           | 2       | To carry set output data when the set is in the on-line mode.                                                                                                                           |
| BB          | Received Data       | 3       | To present incoming data to the set when the set is in the on-line mode.                                                                                                                |
| CA          | Request to Send     | 4       | To condition local line interface unit to transmit. This lead is connected permanently on by the Timer and Interface card in the set.                                                   |
| CB          | Clear to Send       | 5       | To inform set that local data set is ready to transmit any data presented on BA lead.<br><u>Note</u>: This lead is connected permanently on by the Timer and Interface card in the set. |
| CE          | Ring Indicator      | 22      | To inform set of the start of a received call. This lead is permanently connected on in the Timer and Interface card.                                                                   |
| CD          | Data Terminal Ready | 20      | To inform data set that the set is ready to receive data messages. This lead is permanently connected on by the Timer and Interface card in the set.                                    |
|             | Motor Control       | 6       | To provide on-line control of the motor. If connected to ground, motor will go on. If open, motor will tum off.                                                                         |
|             | Ribbon Shift to Red | 25      | To control on-line printing in red color. If connected to ground by code converter, characters will be printed in red. If lead is opened characters will be printed in black.           |

Figure 6 - Typical 37 KSR TTY Set Functional Block Diagram

4.05 The keyboard is connected to the Send Data lead. When the keytop is
depressed the keyboard contacts will close, the reset mechanism clutch will be
released. As the keyboard is reset its auxiliary contact will close to command
the Distributor card to take the character from the contacts. The distributor
will serialize the character and feed it through the Timer and Interface card to
the Send Data lead. The character counter will count the spacing characters
transmitted and light the EOL (End-of-Line) lamp after 80 spacing characters are
in one line.

4.06 Incoming signals are received on the Received Data lead and go through the
Timer and Interface card to the Receiving Device card and the printer selector
magnets. The operator must personally monitor the supply of paper since the low
paper switch is not wired to indicate low-paper condition.

4.07 The 918A Converter in the Data Test Center will provide a ground signal to
the KSR set, on the Ribbon Shift To Red lead for red printing of all characters
to indicate a parity error or another condition. When the CONTL BLACK switch on
the control panel is depressed the printer will print all characters in black.
This switch does not override the Ribbon Shift To Red signal from the 918A
Converter. If CONTL BLACK switch is not depressed the typing unit will print all
characters in black except for control and delete characters. The stunt box
contacts will control the red printing in this mode of operation.

4.08 The typing unit will print all usual characters and special graphics for
all control characters except space. The typing unit will space on all
characters, including control characters. After the 86th character the automatic
carriage return-line feed modification kit will cause a NEW LINE (CR-LF)
operation on the printer at the 87th character received.

4.09 For maintenance of the test board KSR operation and for local testing, the
ON-LINE/LOCAL switch on the electrical service unit is at LOCAL and the Send
Data lead and Receive Data lead are disconnected from the 918A Converter.
Instead the Send Data lead is connected to the Receive Data lead so that the
typing unit monitors the keyboard transmission.

4.10 When the power switch in the electrical service unit is at MAINTENANCE ON
position, the motor is turned on. When the switch is at the NORMAL ON position,
the motor is under the external control of the Data Test Center. When the switch
is at the POWER OFF position all power to the set is off except for the
convenience receptacle. Depressing the MOTOR OFF switch on the control panel
will turn off the motor in on-line mode of operation.

## 5. REFERENCES

5.01 The following sectionalized literature pertains to the 37 KSR Set:

<table>
  <thead>
    <tr><th>TITLE</th><th>NUMBER</th></tr>
  </thead>
  <tbody>
    <tr><th colspan=2>KSR SET</th></tr>
    <tr><td>General Description and Operation</td><td>574-304-100</td></tr>
    <tr><td>Installation</td><td>574-304-200</td></tr>
    <tr><td>Troubleshooting</td><td>574-304-300</td></tr>
    <tr><th colspan=2>MOTOR UNIT</th></tr>
    <tr><td>Description and Principles of Operation</td><td>570-220-100</td></tr>
    <tr><td>Adjustments</td><td>570-220-700</td></tr>
    <tr><td>Lubrication</td><td>570-220-701</td></tr>
    <tr><td>Parts</td><td>570-220-800</td></tr>
    <tr><th colspan=2>TYPING UNIT</th></tr>
    <tr><td>Description and Principles of Operation</td><td>574-320-101</td></tr>
    <tr><td>Disassembly and Reassembly</td><td>574-320-702</td></tr>
    <tr><td>Adjustments</td><td>574-320-703</td></tr>
    <tr><td>Lubrication</td><td>574-320-704</td></tr>
    <tr><td>Parts</td><td>574-320-801</td></tr>
    <tr><th colspan=2>KEYBOARD UNIT</th></tr>
    <tr><td>Description and Principles of Operation</td><td>574-321-101</td></tr>
    <tr><td>Adjustments</td><td>574-321-703</td></tr>
    <tr><td>Lubrication</td><td>574-321-704</td></tr>
    <tr><td>Disassembly and Reassembly</td><td>574-321-705</td></tr>
    <tr><td>Parts</td><td>574-321-801</td></tr>
    <tr><th colspan=2>ELECTRICAL SERVICE UNIT</th></tr>
    <tr><td>Parts</td><td>574-322-801</td></tr>
    <tr><th colspan=2>BASE</th></tr>
    <tr><td>Description and Principles of Operation, Adjustments and Lubrication</td><td>574-331-100</td></tr>
    <tr><td>Parts</td><td>574-331-800</td></tr>
    <tr><th colspan=2>TYPING UNIT COVER AND PAN</th></tr>
    <tr><td>Description and Principles of Operation</td><td>574-326-101</td></tr>
    <tr><td>Adjustments</td><td>574-326-703</td></tr>
    <tr><td>Lubrication</td><td>574-326-704</td></tr>
    <tr><td>Parts</td><td>574-326-801</td></tr>
    <tr><th colspan=2>PAPER WINDER</th></tr>
    <tr><td>Description, Installation, Adjustments and Lubrication</td><td>574-332-100</td></tr>
    <tr><td>Parts</td><td>574-332-800</td></tr>
    <tr><th colspan=2>WIRING DIAGRAMS AND CIRCUIT DESCRIPTIONS</th></tr>
    <tr><td>KSR Set - WD Package</td><td>WDP0283</td></tr>
  </tbody>
</table>
