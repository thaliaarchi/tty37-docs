# Teletype Model 37

[Teletype 37 KSR and ASR General Description and Operation](https://www.navy-radio.virhistory.com/manuals/tty/m37/574-301-100-iss1-7106.pdf)
(section 574-301-100, Issue 1, June 1971)

Research questions:
- What do “on-line”, “type of set”, and “page copy”\[2.06] mean?
- On the control panel, which are buttons and which are lights or both? \[2.21]

Definitions:
- Craftsman adjustable: The feature is enabled or disabled by a craftsman
  \[2.15]

Skipped: 2.05, 2.12, 2.17, 2.19–2.22, 2.24–2.30

TODO: after 2.30

Typical keyboard arrangement: \[Figure 6]

![4-row keyboard configuration](keyboard.png)

Typical control panel arrangements: \[Figure 7]

![Arrangements of the KSR and ASR control panels](control_panel.png)

## Features (unorganized)

The 37 KSR originates data through its keyboard and the ASR originates data
through its keyboard or tape reader.

A 37 can communicate with time-shared computers. \[1.08]

Standard features (KSR and ASR): \[2.02]

- Modular design permits rapid conversion from one type of set (typeset?) to
  another \[1.03]
- Seventy-two characters on a line (10 per inch). Craftsman adjustable for
  shorter or longer lengths up to 80 characters.
- End of printed line indication (lamp) which is craftsman adjustable
- Operator control of multiple copy
- Operator control of vertical spacing: 3 or 6 lines per inch
- Print position indicator (next character indicator)
- Print position scale

ASR-only standard features: \[2.03]

- Local reader character advance
- Low-tape alarm (lamps)
- Send on-line through keyboard or tape reader
- Receives through typing unit or reperforator unit
- Local reperforator backspace

Variable features (KSR and ASR): \[2.04]

Certain options and accessories can be obtained which provide the following
variable features:

- Printed graphics extension
- Carriage return on receipt of NEW LINE, VT, or FF characters
- Optional dedicated half-duplex, dedicated full-duplex, or line control of home
  copy
- Optional power tape handling winder or winder-unwinders (ASR only)
- Optional tape storage bin (ASR only)
- Front or rear loading of forms
- Answer-back triggered either automatically from data set, upon receipt of ENQ
  character, or manually with HERE IS pushbutton
- Keyboard and reader transmission blinded on NAK character, unblinded on ACK
  character
- Incorrect vertical parity indication
- Alarm indication for low-paper (friction feed sets) or paper-out condition
  (sprocket feed sets)

## KSR components

\[Figure 3]

- Keyboard
- Control panel
- Typing unit and cover pan
- Data set
- Attendant set
- Handset
- Utility strip
- Electrical service unit
- Table

## Control characters

- All typing units are equipped with line feed and carriage return (both on-line
  and local), on-line backspace \[2.10]
- On-line backspace \[2.03]
- On-line carriage return and line feed \[2.03]
- Local carriage return \[2.03]
- Local paper feed-out \[2.03]
- Horizontal tabulation on-line control (variable) \[2.04]
- Vertical tabulation on-line control (variable) \[2.04]
- Half-forward, Half-reverse, and reverse line feed (variable) \[2.04]
- Nonrepeat form feed (variable) \[2.04]
- Disconnect capability on EOT character (variable) \[2.04]
- Form advance (form-out) (variable) \[2.04]
- Vertical tabulation (craftsman adjustable) (variable) \[2.04]
- Horizontal tabulation (craftsman adjustable) (variable) \[2.04]

Optional paper positioning controls are provided: \[2.11]
- Form-Feed - When the typing unit detects the form-feed character, it will
  position the paper for printing on the first line of the next page. Pages up
  to 15 inches in length, adjustable by a craftsman, may be accommodated. The
  typing unit form feeds three lines during one character interval. Two
  successive form feeds are prevented unless there has been an intervening line
  feed.
- Horizontal Tabulation - This feature is a fixed tabulator stop type. The fixed
  stops are set by a craftsman to customer specifications.
- Vertical Tabulation - This feature is a fixed tabulator stop type. The fixed
  stops are set by a craftsman to customer specifications.
- Horizontal Tabulation On-Line Control - This is an on-line feature used to set
  and clear tabulation stops in the typing unit horizontal tabulation mechanism.
  The characters ESC 1 are used to set tabulator stops and the characters ESC 2
  are used to clear the stops.
- Vertical Tabulation On-Line Control - This is an on-line feature used to set
  and clear the tabulation stops in the typing unit vertical tabulation
  mechanism. The characters ESC 5 are used to set the tabulator stops and the
  characters ESC 6 are used to clear the stops.

## Character set

- Generates all 128 ASCII characters with even parity \[2.02]
- Receives all 128 ASCII characters - prints 94 graphics including upper and
  lowercase alphabet \[2.02]
- The typing unit is capable of printing symbols for all 128 ASCII characters.
  Normally, however, it will be arranged to print the 94 graphic, numeric, and
  alpha characters of ASCII. \[2.07]

Page copy is provided by the typing unit which prints both upper and lower case
characters utilizing a typebox positioned by an aggregate motion mechanism. The
typebox is moved from character to character and is returned to "home" position
when reception stops, thus, making all characters visible when the machine is
idle. \[2.06]

It is possible to generate all 128 code combinations of ASCII. Upper and lower
case alpha characters, numerics, and special graphic characters are designated
on the keytops. Control characters are designated on the keyboard in two ways.
The most often used controls appear on separate keys and are active in both the
shifted and unshifted modes without use of the CONTRL key. Another group of
controls appear on the same keytop with a graphic. To generate these code
combinations, it is necessary to depress the CONTRL key while the particular key
is struck. All control character designations requiring the depression of the
CONTRL key, as well as the individual key, appear on the keyboard in charcoal
grey. \[2.14]

## Character repeat

A repeat feature is provided on each key generating a character. Further
depression of the key beyond its normal stop position causes the associated
character to be generated repetitively at the maximum character rate. The repeat
feature is enabled or disabled by a craftsman. \[2.15]

Character repeat feature - craftsman adjustable. Note: This feature is normally
disabled on all keys except the following: space, NEW LINE, BACKSPACE, NULL,
DELETE, period (.), hyphen (-), equal (=), underscore (_), colon (:), asterisk
(*), character X \[2.04]

## Control panel

The control panel (Figure 7) which is located above the keyboard contains a
number of nonlocking pushbuttons. In addition, there are two mechanical
pushbuttons designated PAPER ADVANCE and LOCAL RETURN. The two different
arrangements available to meet varying applications are shown in Figure 7.
Functional descriptions of the different controls are given in Table A. \[2.18]

Controls and their functions: \[Table A]
- **OFF LINE**: Depressing this pushbutton lights the associated indicator and
  activates the teletypewriter for use in the off-line (local) mode. A second
  operation of the pushbutton extinguishes the light and conditions the
  equipment for incoming and outgoing calls. If this pushbutton is depressed
  while a data call is in progress, a disconnect will result.
- **PAPER ADVANCE**: Paper is fed out of the typing unit for as long as this
  pushbutton is held depressed. This is a local function only, and has no effect
  on the distant station.
- **LOCAL RETURN**: When this pushbutton is depressed, the typing unit carriage
  returns to the left margin. This is a local function only, and has no effect
  on the distant station.
- **INTRPT** (interrupt): When momentarily depressed, this pushbutton causes a
  timed (380 to 750 millisecond) spacing signal (break) to be sent on-line. It
  is used by the receiving station to interrupt transmission from the sending
  station.
- **PROCEED**: This lamp lights when the station is ready for sending from the
  keyboard. (It will light when the unlighted pushbutton is depressed, or when
  an ACK character is received, and will turn off when a NAK character or
  interrupt signal is received.) Either the receipt of an ACK character or
  manual operation of the PROCEED pushbutton will relight the lamp. The lamp
  turns off when a data call is completed.
- **HERE IS** When momentarily depressed, this pushbutton starts the local
  answer-back mechanism which causes a stored series of characters (such as
  station identification) to be sent. The answer-back only operates on-line.
- **ALARM**: When lighted, this lamp may indicate a low-paper supply condition.
  The ALARM lamp also optionally lights when a character is received with
  incorrect vertical parity. The lamp will be turned off by depressing the ALARM
  pushbutton if a parity error was received. When lighted by a low-paper
  condition, the lamp turns off only after the paper supply is replenished.
- **EOL** (Printer End of Line): This lamp lights to indicate the end of a
  printed line (adjustable for any length of line suitable to the typing unit).
  The light goes off when a new line is started.
- **READER AUTO**: When this pushbutton is depressed, the associated lamp
  lights, and the station is conditioned for auto control of the reader by the
  characters DC1 and DC3. When the pushbutton is depressed again, the light goes
  out and the auto reader control feature is disabled (both the reader and
  typing unit must be on-line).
- **KBD LOCAL**: When this pushbutton is depressed, the associated lamp lights,
  the typing unit motor starts, and the keyboard is placed in the off-line
  (local) mode.
- **PRINTER LOCAL**: When this pushbutton is depressed, the associated lamp
  lights, the typing unit motor starts, and the typing unit is placed in the
  off-line (local) mode. When the pushbutton is depressed again, the typing unit
  is placed in the on-line mode.
- **READER LOCAL**: When this pushbutton is depressed, the associated lamp
  lights, the reader motor is started, and the reader is placed in the off-line
  (local) mode. When the pushbutton is depressed again, the lamp goes out, the
  motor stops, and the reader is placed in the on-line mode.
- **PUNCH LOCAL**: When this pushbutton is depressed, the associated lamp lights
  and the reperforator (punch) is placed in the off-line (local) mode. The punch
  selector may be blinded or not depending on the state of the PUNCH ON
  pushbutton. Depressing the pushbutton again turns off the light and restores
  the reperforator to the idle condition.
- **PUNCH ON**: When this pushbutton is depressed, the associated lamp lights
  and the reperforator selector is unblinded. Depressing the pushbutton again
  turns the lamp off and causes the reperforator selector to be blinded. For
  local operation of the reperforator, the PUNCH ON pushbutton must be depressed
  after PUNCH LOCAL is depressed.
- **KBD EOL** (Keyboard End of Line): This lamp is lighted by a character
  counter and indicates that sufficient characters have been perforated in tape
  to produce a line of characters on page copy. The counter counts down on
  backspace and is reset on carriage return.

## Speeds

Operating speeds (send and receive):
- 15 characters per second (150 words per minute) with a 10-unit code
  transmission pattern \[2.03]
- Optional operating speed of 10 characters per second (100 words per minute)
  with an 11-unit code transmission pattern (variable) \[2.04]

Data is converted to voltage signals, i.e., positive voltage for spacing signals
and negative for marking signals, which is then converted into voice frequency
tones by a data set for transmission. Received data, in the form of voice
frequency tones, is converted into voltage signals by a data set, then copied
onto paper or tape. \[1.05]

The keyboard is an electromechanical device for generating ASCII combinations.
It converts the mechanical depression of a key into electrical code patterns.
Keys move codebars which control electrical contacts. The electrical contacts
present an even vertical parity parallel Wire output to a keyboard control logic
card in the electrical service unit which converts the signals into ASCII.
\[2.13]

## Interfacing

The channel interface signals conform to the EIA (Electronics Industries
Association) Standard [RS-232-B](https://en.wikipedia.org/wiki/RS-232)
\[1.02]\[2.02]\[2.27]\[4.05]

## Transmission disable

A transmission disable feature is provided to prevent transmission from the
keyboard or reader. Transmission may be disabled and enabled under control of
on-line signals as covered in 4.10 and 4.30. This feature does not physically
lock the keys of the keyboard but inhibits output from the transmitter
distributor. \[2.16]

## Paper

Two types of paper feed options are available: \[2.09]
- A typing unit arranged for friction feed is capable of accommodating roll
  paper widths of 3 to 8-1/2 inches and capable of providing multiple copies of
  one original and two carbons.
- A typing unit arranged with sprocket feed is capable of handling sprocket feed
  paper 11 inches long and 9-1/2 inches wide. One-half inch is needed on each
  side of a page to allow for sprocket holes. The typing unit is capable of
  providing multiple copies consisting of one original and up to five carbons.

Roll paper (friction feed sets) or flat-folded, form-feed paper with marginal
perforations (sprocket feed sets) \[2.02]

A number of paper handling accessories are available for sets with sprocket feed
typing units. Modification kits are available for either front or rear loading
of a standard box of paper forms. Front loading of forms can be used for forms
up to 14 inches in length. Forms up to 15 inches long can be loaded from the
rear of the table. A form accumulator is also available as an accessory if
desired. \[2.46]

## Character sizes

Normally the typing unit will print ten characters per inch allowing 72
characters on an 8-1/2 inch platen with normal margins on the paper. Optionally,
other typing units may be arranged to print 12 characters per inch allowing 86
characters on an 8-1/2 inch platen with normal margins on the paper. Line feed
provides for spacing six lines of type per vertical inch. \[2.08] All typing
units are equipped with craftsman adjustable margins. \[2.10]

Eighty-six characters on a line (12 per inch) (variable) \[2.04]

Colors:
- Single color printing \[2.03]
- Two-color ribbon (variable) \[2.04]

Two lids at the top of the cover provide access to the typing unit for ribbon
changing, replenishing paper supply, adjusting print hammer for multiple copy,
etc. \[2.23]

---

TODO:
- [Teletype 37 ASR General Description](https://www.navy-radio.virhistory.com/manuals/tty/m37/574-302-102-iss1-7105.pdf)
  (section 574-302-102, issue 1, May 1971)
- <https://retrocomputing.stackexchange.com/questions/4456/what-protocol-do-teletypes-use>
