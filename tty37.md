# Teletype Model 37 functional specification

## Typing unit and character set

It generates and receives all 128 ASCII characters.
\[Gen301 2.02, 2.14]\[Gen304 2.02, 2.11]

The typing unit prints characters onto paper (called “page copy”) by positioning
the typebox by an “aggregate motion mechanism”. The typebox is moved from
character to character and is retracted when reception stops, making all
characters visible when the machine is idle. \[Gen301 2.06]\[Gen304 2.04]

The typing unit usually only prints the 94 graphic ASCII characters, though is
capable of printing symbols for all 128 characters. \[Gen301 2.07]

The \[Gen304] model prints visible symbols for 127 ASCII characters,
excluding space, and spaces on all characters. It provides an eight-row typebox
with pallets in the upper two rows for 32 control characters. \[2.02, 2.05,
4.08]

A keyboard interlock prevents errors caused from two keys simultaneously
pressed. \[Catalog p7]

Questions:
- Does “aggregate motion” simply refer to two-dimensional movement?
- What are the configurations of number of rows for typeboxes?
- What are the symbols printed for control characters?

## Parity

Generates all 128 ASCII characters with even parity (standard feature).
\[Gen301 2.02]\[Gen304 2.02]

## Escape sequences

\[Type 4.23]\[Catalog p10]

| Sequence | Function               |
| -------- | ---------------------- |
| ESC 1    | Horizontal Tab Set     |
| ESC 2    | Horizontal Tab Clear   |
| ESC 3    | Print Red              |
| ESC 4    | Print Black            |
| ESC 5    | Vertical Tab Set       |
| ESC 6    | Vertical Tab Clear     |
| ESC 7    | Reverse Line Feed      |
| ESC 8    | Half-Reverse Line Feed |
| ESC 9    | Half-Line Feed         |
| ESC :    | Full Duplex (FDX)      |
| ESC ;    | Half-Duplex (HDX)      |

Variable features: Half-forward, Half-reverse, and reverse line feed.
\[Gen301 2.04]

Horizontal Tabulation On-Line Control - This is an on-line feature used to
set and clear tabulation stops in the typing unit horizontal tabulation
mechanism. The characters ESC 1 are used to set tabulator stops and the
characters ESC 2 are used to clear the stops. \[Gen301 2.11]

Vertical Tabulation On-Line Control - This is an on-line feature used to set
and clear the tabulation stops in the typing unit vertical tabulation
mechanism. The characters ESC 5 are used to set the tabulator stops and the
characters ESC 6 are used to clear the stops. \[Gen301 2.11]

**Reverse Line Space and Half Forward and Reverse Line Spacing.** These
features, controlled by two-character sequences, enable the operator or a
distant terminal to follow formats which had been previously impractical or
impossible. In addition, correction of errors, printing of fractions, and other
operations are easily accomplished. When these features are in a page printer
with Vertical Tabulation and Form Feed, the line spacing rate of the Vertical
Tabulation and Form Feed is approximately one and one-half times the normal rate
of line spacing (and the Double Line Space feature is not provided).
\[Catalog p9]

\[Catalog p10]:

**Escape.** Control functions other than those defined by specific ASCII control
characters are initiated by using the ASCII control character Escape (ESC)
followed by a graphic character. (Escape is designated on the keyboard as the
Prefix keytop).

Recognition of “escape” sequences is performed by the stunt box which, in turn,
activates the selected control function. Printing is suppressed for all
characters in the Escape sequence. The page printer always returns to the
unsuppressed mode after the graphic character unless the graphic of the “escape”
sequence is in column 2 of the ASCII code. Print and space suppression will be
affected continually as long as all following graphics are from this row.

The control function description for the “escape” sequence is labeled on the
control panel above the top row of keytops on the keyboard and is as follows:

## Function

Suppression code bar can be operated by stunt box to inhibit operation of
certain function bars. \[Catalog p4]

Question: Which?

FUNCTION MECHANISM
- Senses each new character received. Detects presence of function character and
  operates mechanical linkage or electrical contacts to initiate function.
- Can suppress subsequent print hammer, spacing, and ribbon feed mechanisms.
- Can sense parity (eighth) level.
- Function box contains 42 slots for function bars.

CONTROL FUNCTIONS \[Type 2.10]

2.10 Additional time is required by the typing unit to perform certain machine
control functions. Delete (DEL) characters are used as fill characters in tapes
transmitted and received by the typing unit to provide this additional time;
these fill characters are listed in the following table.

TABLE

DELETE FILL CHARACTERS FOR CONTROL FUNCTIONS

| FUNCTIONS                 | STD UNITS | WIDE PLATEN |
| ------------------------- | --------- | ----------- |
| Carriage Return           | 2         | 3           |
| New Line                  | 2         | 3           |
| Form-Feed                 | 1         | 2           |
| Vertical Tab-Clear        | 1         | 2           |
| Vertical Tab-Set          | 1         | 0           |
| Horizontal Tab-Clear      | 1         | 2           |
| Horizontal Tab-Set        | 1         | 0           |
| DC2                       | 1         | 1           |
| DC4                       | 1         | 1           |
| Carriage Return/Line Feed | 1         | 2           |
| Form-Out                  | 0         | 2           |
| Vertical Tab              | 0         | 2           |
| Horizontal Tab            | 0         | 2           |

Note: Any function that uses a transmitter stop control, requires two deletes
after the control function.

Question: What is "transmitter stop control"?
Note: DEL is a nop.

2.11 The typing unit is designed to accept a full range of options that are
on-line controllable. These options are furnished in the form of modification
kits listed below. \[Type 2.11]

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

**Y. Function Bar Coding**

4.85 The function bar code chart, Figure 60, shows the coding for the ASCII. The
table at the end of this section shows the coding for the common function bars.
The no. 8 tine is shown for even parity. If odd parity or no parity is desired,
the 8th lever may be altered. Refer to Figure 56 to code the function bar tines
1 through 8, and refer to the following instructions for coding the 9th, lOth,
and 11th tines.

Figure 60 - Function Bar Code Chart (Even Parity)

\[Table]

Figure 63 - Visual Aid Overlay

\[Graphic]
Note: This shows the Greek symbols.

TABLE OF FUNCTION BAR CONFIGURATIONS

\[Graphic]

## Character repeat feature

The keyboard permits you to repeat a character by pressing a key harder than
normal (beyond its normal stop position), making it generate the associated
character repeatedly at the maximum character rate. \[Gen301 2.15]\[Gen304 2.12]

Any key can be made repeatable by a technician with a simple modification. In
the standard arrangement, only the ten most commonly used keys are repeatable
(in both the shift and unshift states): \[Catalog p7]\[Gen301 2.04]

- Space
- NEW LINE
- BACKSPACE
- NULL
- DELETE
- Period `.`
- Hyphen `-` or equals `=`
- Underscore `_`
- Colon `:` or asterisk `*`
- Upper case `X` and lower case `x`

Note that letters other than X apparently aren't repeatable in the standard
arrangement (\[Catalog] states that ten keys are repeatable, matching this
list).

In the \[Gen304] KSR model, character repeat is a standard feature and
enabled for every key. \[2.02, 2.12] That model spaces on all characters, even
control characters\[4.08], so this appears to simplify the mechanism.

The maximum character rate (for at least the \[Gen304] model) is 59.02 wpm.
\[2.12]

\[Dolotta] proscribes a desired operation for character repeat like the Model
37, though it is unclear how much of this, if any, corresponds to its actual
operation. It proscribes that character repeat must be optionally available for
all printing keys and the following control keys: backspace, new line, carrier
return, forward/reverse line feed, space/blank, half-line up feed, half-line
down feed, horizontal tab, and vertical tab. [figure 1 note 4] The amount of
pressure required to activate repeat should be user-adjustable, and which keys
have repeat enabled should also be configurable, though possibly by a
technician. \[table I note c]\[figure 1 note 1] The user should be able to
completely disable it, perhaps by moving the repeat mode pressure adjustment to
an extreme position. \[3.2.1]

## Paper

### Sprocket feed

Sprocket feed typing units have the following paper width options:
[Spec50494S table 1 (p15)]

- 9-1/2"
- 9"
- 8-1/2"
- 8"
- 7-1/2"
- 7"
- 6-1/2"
- 6-3/8"
- 6-1/4"
- 6"
- 5-3/4"
- 5-1/2"
- 5"
- 4-1/2"
- 4-5/16"
- 4-1/4"
- 4"
- 3-5/8"

To convert a friction feed typing unit to sprocket feed, see Specification
50494S. To adapt the paper width for a sprocket feed typing unit, see the
modification kits described in Specification 50386S for 9-1/2" and Specification
57925 for the other widths.

## Definitions

- Space and mark are the signals corresponding to 0 and 1 bits, respectively.
  Producing such a signal is spacing or marking.
  \[Type figure 15 (p15)]\[Catalog p26]

## Extant machines

- The [Connections Museum Seattle](https://www.telcomhistory.org/ConnectionsSeattle.html)
  [[Wikipedia](https://en.wikipedia.org/wiki/Connections_Museum)] has a Teletype
  Model 37 ASR in their [collection](https://wiki.connections.museum/w/CMS:Teletype_Collection).
  A [2013 video](https://www.youtube.com/watch?v=MikoF6KZjm0) shows it connected
  to a System V Release 3.2.2 machine, which relayed chat messages to it and
  another 37 at the LCM, dialing with a Dataphone.
- The Living Computers Museum had a Teletype Model 37 ASR in their [collection](https://web.archive.org/web/20161024131926/http://www.livingcomputermuseum.org/The-Collection/Exhibit-Hall.aspx).
  A [2018 video](https://www.youtube.com/watch?v=WqgFK9h75eg) shows it connected
  to a System V Release 3.2.2 machine. It is not listed in the
  [August 2024 auction](https://onlineonly.christies.com/s/firsts-history-computing-paul-g-allen-collection/lots/3726).
- The National Museum of American History, part of the Smithsonian, has
  [a Teletype Model 37](https://www.si.edu/object/teletype-corporation-model-37-teletypewriter-printer:nmah_714260),
  but it is not on display.
- [RTTY Electronics](https://www.johnwhitney.com/misc/paul-rtty.htm) in El
  Sobrante, California sells Teletype machines and parts, probably including the
  Model 37.

## References

- \[Catalog]: Teletype Corporation. [“Teletype Model 37 Product Catalog”](https://archive.org/details/TNM_Model_37_terminal_product_catalog_-_Teletype__20170923_0036).
  April 1969.
  - Includes a high-quality general description and operation, examples printed
    by a Model 37, and options for various models.

- \[Gen301]: Teletype Corporation. [“37 Keyboard Send-Receive (KSR)
  Teletypewriter Set and 37 Automatic Send-Receive (ASR) Teletypewriter Set for
  "DATA-PHONE®" Service: General Description and Operation”](https://www.navy-radio.com/manuals/tty/m37/574-301-100-iss1-7106.pdf).
  Bell System Practices, Section 574-301-100, Issue 1, June 1971.

- \[Gen304]: Teletype Corporation. [“37 Keyboard Send-Receive (KSR)
  Teletypewriter Set Used in Telegraph Test Boards and Service Boards: General
  Description and Operation”](https://www.navy-radio.com/manuals/tty/m37/574-304-100-iss2-7212.pdf).
  Bell System Practices, Section 574-304-100, Issue 2, December 1972.
  - This document appears to be for a more specific configuration of the
    Teletype Model 37 KSR than \[Gen301], as it does not describe ASR, omits
    some features, and makes some optional features standard.

- \[Trouble]: Teletype Corporation. [“37 Automatic Send-Receive (ASR)
  Teletypewriter Set for Switched Network Service: Troubleshooting”](https://www.navy-radio.com/manuals/tty/m37/574-302-300-iss1-7204.pdf).
  Bell System Practices, Section 574-302-300, Issue 1, April 1972.
  - Outlines troubleshooting procedures and possible failures.

- \[Type]: Teletype Corporation. [“37 Typing Unit (37P003 and up): Description
  and Principles of Operation”](https://www.navy-radio.com/manuals/tty/m37/574-320-101-iss2-7302.pdf).
  Bell System Practices, Section 574-320-101, Issue 2, February 1973.

- \[Spec50494S]: Teletype Corporation. [“Instructions for Installing
  Modification Kit 319820 to Convert a Model 37 Friction Feed Typing Unit to a
  Sprocket Feed Typing Unit”](https://www.navy-radio.com/manuals/tty/spec/50494S-6707.pdf).
  Specification 50494S, Issue 1, July 1967.
  - Has illustrations of the typebox and feed mechanisms and a list of sprocket
    feed paper widths. References the modification kits covered by \[Spec57925]
    and \[Spec50386S].

- \[Spec57925]: Teletype Corporation. [“Instructions for Installing Modification
  Kits (172625, 176181 through 176197, 178568 through 178584, 306686 through
  306702, 153926) to Convert a Model 28 or 35 Friction Feed Printer Set to a
  Sprocket Feed Printer Set and for Replacing the 153771 through 153787 Guide
  Bracket Using the 159356 Modification Kit”](https://www.navy-radio.com/manuals/tty/jh/ttyman6/specs/5792S-Iss17.pdf).
  Specification 57925, Issue 17, August 1973.
  - Referenced by \[Spec50494S], so must also apply to Model 37.

- \[Spec50386S]: Teletype Corporation. [“Instructions for Installing the 305037
  and 310733 Modification Kits to Adapt a Model 35 or Model 28 Sprocket Feed
  Typing Unit to Take 9-1/2 Inch Width Paper, Respectively”](https://www.navy-radio.com/manuals/tty/jh/ttyman6/specs/50386S-Iss1.pdf).
  Specification 50386S, Issue 1, March 1965.
  - Referenced by \[Spec50494S], so must also apply to Model 37.

- \[Dolotta]: T. A. Dolotta. [“Functional Specifications for Typewriter-Like
  Time-Sharing Terminals”](https://dl.acm.org/doi/10.1145/356561.356563).
  ACM Computing Surveys, March 1970.
  - A statement to terminal manufacturers on user needs for time-sharing
    computer systems. It references the operation of the Teletype Model 37, but
    cannot be considered reliable.

- \[PartsIndex]: Teletype Corporation. [“37 Page Printer Set (KSR-RO): Parts”](https://www.navy-radio.com/manuals/tty/jh/ttyman0/TeletypeManuals/model37/1209B-Iss1.pdf).
  Bulletin 1209B, Issue 1, December 1967.
  - A short index of section-800 parts documents (all listed below).

### Bell System Practices

Documents in the [Bell System Practices](http://bellsystempractices.org/) series
pertaining to the Teletype Model 37.

TODO:
- Add manuals from the large section “Model 37 - also see here” on [navy-radio](https://www.navy-radio.com/manuals-ttycorp.htm).
  Everything else on that page with “37” has been added.
- Add manuals from [Division 574: Teletypewriter 30 Series and Teleprinters](https://www.telecomarchive.com/574.html).

Referrers:
1. \[Gen301 5.01] (574-301-100)
2. \[Gen304 5.01] (574-304-100)
3. \[PartsIndex]

| Number        | Component                                | Title                                                                | Version                                                                                                              | Referrers |
| ------------- | ---------------------------------------- | -------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- | --------- |
| 570-020-800   |                                          | Type Pallets for Models 28, 35, and 37 Teletypewriter Sets           | [Issue 3, 1974-04](https://www.navy-radio.com/manuals/tty/570-020-800-7404.pdf)                                      |           |
| 570-020-801   |                                          | Keytops for Models 37, CDT and “DATASPEED®” Printer Terminals        | [Issue 2, 1974-05](https://www.navy-radio.com/manuals/tty/570-020-801-7405.pdf)                                      |           |
| 570-220-100   | Motor Unit                               | Description and Principles of Operation                              |                                                                                                                      | 1, 2      |
| 570-220-700   | Motor Unit                               | Adjustments                                                          |                                                                                                                      | 1, 2      |
| 570-220-701   | Motor Unit                               | Lubrication                                                          |                                                                                                                      | 1, 2      |
| 570-220-702   | Motor Unit                               | Disassembly and Reassembly                                           |                                                                                                                      | 1         |
| 570-220-800   | Motor Unit                               | Parts                                                                | [Issue 5, 1972-11](https://www.navy-radio.com/manuals/tty/570-220-800-7211.pdf)                                      | 2         |
| 574-301-100   | KSR and ASR Set                          | General Description and Operation                                    | [Issue 1, 1971-06](https://www.navy-radio.com/manuals/tty/m37/574-301-100-iss1-7106.pdf)                             |           |
| 574-301-102   | KSR Set                                  | General Description                                                  | [Issue 1, 1972-12](https://www.navy-radio.com/manuals/tty/m37/574-301-102-iss1-7212.pdf)                             |           |
| 574-301-200   | KSR Set                                  | Installation                                                         | [Issue 2, 1973-02](https://www.navy-radio.com/manuals/tty/m37/574-301-200-iss2-7302.pdf)                             | 1         |
| 574-301-400   | KSR Set                                  | Wiring Diagram And Circuit Descriptions                              | [Issue 1, 1969-09](https://www.navy-radio.com/manuals/tty/m37/574-301-400-iss1-6909.pdf)                             |           |
| 574-301-702   | KSR Set                                  | Removal and Replacement of Components                                | [Issue 1, 1970-03](https://www.navy-radio.com/manuals/tty/m37/574-301-702-iss1-7003.pdf)                             | 1         |
| 574-302-102   | ASR Set                                  | General Description                                                  | [Issue 1, 1971-05](https://www.navy-radio.com/manuals/tty/m37/574-302-102-iss1-7105.pdf)                             |           |
| 574-302-200   | ASR Set                                  | Installation                                                         | [Issue 2, 1973-02](https://www.navy-radio.com/manuals/tty/m37/574-302-200-iss2-7302.pdf)                             | 1         |
| 574-302-300   | ASR Set                                  | Troubleshooting                                                      | [Issue 1, 1972-04](https://www.navy-radio.com/manuals/tty/m37/574-302-300-iss1-7204.pdf)                             |           |
| 574-302-702   | ASR Set                                  | Removal and Replacement of Components                                | [Issue 1, 1970-03](https://www.navy-radio.com/manuals/tty/m37/574-302-702-iss1-7003.pdf)                             | 1         |
| 574-303-100   | ROTR Set                                 | Description and Operation                                            | [Issue 2, 1973-06](https://www.navy-radio.com/manuals/tty/m37/574-303-100-iss2-7306.pdf)                             |           |
| 574-303-200   | ROTR Set                                 | Installation                                                         | [Issue 1, 1970-11](https://www.navy-radio.com/manuals/tty/m37/574-303-200-iss1-7011.pdf)                             |           |
| 574-303-300   | ROTR Set                                 | Troubleshooting                                                      | [Issue 1, 1973-10](https://www.navy-radio.com/manuals/tty/m37/574-303-300-iss1-7310.pdf)                             |           |
| 574-303-702   | ROTR Set                                 | Removal and Replacement of Components                                | [Issue 1, 1970-06](https://www.navy-radio.com/manuals/tty/m37/574-303-702-iss1-7006.pdf)                             |           |
| 574-304-100   | KSR Set                                  | General Description and Operation                                    | [Issue 2, 1972-12](https://www.navy-radio.com/manuals/tty/m37/574-304-100-iss2-7212.pdf)                             | 2         |
| 574-304-200   | KSR Set                                  | Installation                                                         | [Issue 2, 1972-12](https://www.navy-radio.com/manuals/tty/m37/574-304-200-iss2-7212.pdf)                             | 2         |
| 574-304-300   | KSR Set                                  | Troubleshooting                                                      | [Issue 2, 1972-12](https://www.navy-radio.com/manuals/tty/m37/574-304-300-iss2-7212.pdf)                             | 2         |
| 574-320-101   | Typing Unit (37P003 and up)              | Description and Principles of Operation                              | [Issue 2, 1973-02](https://www.navy-radio.com/manuals/tty/m37/574-320-101-iss2-7302.pdf)                             | 1, 2      |
| 574-320-400   | Typing Unit                              | Wiring Diagrams                                                      | [Issue 1, 1971-01](https://www.navy-radio.com/manuals/tty/m37/574-320-400-iss1-7101.pdf)                             |           |
| 574-320-700   | Typing Unit (Early Design)               | Adjustments                                                          | [Issue 4, 1971-03](https://www.navy-radio.com/manuals/tty/m37/574-320-700-iss4-7103.pdf)                             |           |
| 574-320-702   | Typing Unit                              | Disassembly and Reassembly                                           |                                                                                                                      | 2         |
| 574-320-703   | Typing Unit                              | Adjustments                                                          |                                                                                                                      | 1, 2      |
| 574-320-704   | Typing Unit                              | Lubrication                                                          |                                                                                                                      | 1, 2      |
| 574-320-705   | Typing Unit                              | Disassembly and Reassembly                                           |                                                                                                                      | 1         |
| 574-320-800TC | Typing Unit (YP)                         | Parts                                                                | [Issue 1, 1967-12](https://www.navy-radio.com/manuals/tty/jh/ttyman0/TeletypeManuals/model37/574-320-800TC-Iss1.pdf) | 3         |
| 574-320-801   | Typing Unit                              | Parts                                                                |                                                                                                                      | 2         |
| 574-321-101   | Keyboard Unit                            | Description and Principles of Operation                              |                                                                                                                      | 1, 2      |
| 574-321-703   | Keyboard Unit                            | Adjustments                                                          |                                                                                                                      | 1, 2      |
| 574-321-704   | Keyboard Unit                            | Lubrication                                                          |                                                                                                                      | 1, 2      |
| 574-321-705   | Keyboard Unit                            | Disassembly and Reassembly                                           |                                                                                                                      | 1, 2      |
| 574-321-800TC | Keyboard (YK) and Base (YB)              | Parts                                                                | [Issue 1, 1967-12](https://www.navy-radio.com/manuals/tty/jh/ttyman0/TeletypeManuals/model37/574-321-800TC-Iss1.pdf) | 3         |
| 574-321-801   | Keyboard Unit                            | Parts                                                                |                                                                                                                      | 2         |
| 574-322-101   | Electrical Service Unit                  | Description and Operation                                            |                                                                                                                      | 1         |
| 574-322-800TC | Electrical Service Unit (YESU)           | Parts                                                                | [Issue 1, 1967-12](https://www.navy-radio.com/manuals/tty/jh/ttyman0/TeletypeManuals/model37/574-322-800TC-Iss1.pdf) | 3         |
| 574-322-801   | Electrical Service Unit                  | Parts                                                                |                                                                                                                      | 2         |
| 574-323-101   | Table                                    | Description and Operation                                            |                                                                                                                      | 1         |
| 574-323-703   | Table                                    | Adjustments                                                          |                                                                                                                      | 1         |
| 574-323-800TC | Table (YT)                               | Parts                                                                | [Issue 1, 1967-12](https://www.navy-radio.com/manuals/tty/jh/ttyman0/TeletypeManuals/model37/574-323-800TC-Iss1.pdf) | 3         |
| 574-324-800TC | Electronic Distributor (YTD)             | Parts                                                                | [Issue 1, 1967-12](https://www.navy-radio.com/manuals/tty/jh/ttyman0/TeletypeManuals/model37/574-324-800TC-Iss1.pdf) | 3         |
| 574-325-703   | Answer-Back Unit                         | Adjustments                                                          |                                                                                                                      | 1         |
| 574-325-704   | Answer-Back Unit                         | Lubrication                                                          |                                                                                                                      | 1         |
| 574-325-800TC | Answer Back (YAB)                        | Parts                                                                | [Issue 1, 1967-12](https://www.navy-radio.com/manuals/tty/jh/ttyman0/TeletypeManuals/model37/574-325-800TC-Iss1.pdf) | 3         |
| 574-326-101   | Typing Unit Cover and Pan                | Description and Principles of Operation                              |                                                                                                                      | 1, 2      |
| 574-326-703   | Typing Unit Cover and Pan                | Adjustments                                                          |                                                                                                                      | 1, 2      |
| 574-326-704   | Typing Unit Cover and Pan                | Lubrication                                                          |                                                                                                                      | 1, 2      |
| 574-326-800TC | Typing Unit Cover (YPC)                  | Parts                                                                | [Issue 1, 1967-12](https://www.navy-radio.com/manuals/tty/jh/ttyman0/TeletypeManuals/model37/574-326-800TC-Iss1.pdf) | 3         |
| 574-326-801   | Typing Unit Cover and Pan                | Parts                                                                |                                                                                                                      | 2         |
| 574-327-100   | RT Module Cabinet                        | Description and Operation                                            |                                                                                                                      | 1         |
| 574-327-700   | RT Module Cabinet                        | Adjustments                                                          |                                                                                                                      | 1         |
| 574-327-701   | RT Module Cabinet                        | Lubrication                                                          |                                                                                                                      | 1         |
| 574-329-100   | Nontyping Reperforator                   | Description and Principles of Operation                              |                                                                                                                      | 1         |
| 574-329-700   | Nontyping Reperforator                   | Adjustments                                                          |                                                                                                                      | 1         |
| 574-329-701   | Nontyping Reperforator                   | Lubrication                                                          |                                                                                                                      | 1         |
| 574-329-702   | Nontyping Reperforator                   | Disassembly and Reassembly                                           |                                                                                                                      | 1         |
| 574-330-100   | Typing Reperforator                      | Description and Operation                                            |                                                                                                                      | 1         |
| 574-330-700   | Typing Reperforator                      | Adjustments                                                          |                                                                                                                      | 1         |
| 574-330-701   | Typing Reperforator                      | Lubrication                                                          |                                                                                                                      | 1         |
| 574-330-702   | Typing Reperforator                      | Disassembly and Reassembly                                           |                                                                                                                      | 1         |
| 574-331-100   | Base                                     | Description and Principles of Operation, Adjustments and Lubrication |                                                                                                                      | 2         |
| 574-331-800   | Base                                     | Parts                                                                |                                                                                                                      | 2         |
| 574-332-100   | Paper Winder                             | Description, Installation, Adjustments and Lubrication               |                                                                                                                      | 2         |
| 574-332-800   | Paper Winder                             | Parts                                                                |                                                                                                                      | 2         |
| 579-400-350   | KSR Set                                  | Field Maintenance Practice                                           |                                                                                                                      | 1         |
| 592-801-100   | Tape Reader                              | Description and Principles of Operation                              |                                                                                                                      | 1         |
| 592-801-700   | Tape Reader                              | Adjustments                                                          |                                                                                                                      | 1         |
| 592-801-701   | Tape Reader                              | Lubrication                                                          |                                                                                                                      | 1         |
| 592-801-702   | Tape Reader                              | Disassembly and Reassembly                                           |                                                                                                                      | 1         |
| WDP0283       | Wiring Diagrams and Circuit Descriptions | KSR Set - WD Package                                                 |                                                                                                                      | 2         |

| Number               | Title                                                                                                                                                                                                                                                                                                                | Version                                                                                      |
| -------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------- |
| Specification 5534S  | Instructions for Installing the Manual Power Drive Backspace, and Backspace Cover Modification Kits on Model 28 or Model 35 Perforator or Reperforator (LPR, LPE, LRPE, LTPE, LARP) and Model 37 Reperforator (YPR, YRPE)                                                                                            | [Issue 14, 1971-06](https://www.navy-radio.com/manuals/tty/spec/5534S-iss14-7106.pdf)        |
| Specification 57925  | Instructions for Installing Modification Kits (172625, 176181 through 176197, 178568 through 178584, 306686 through 306702, 153926) to Convert a Model 28 or 35 Friction Feed Printer Set to a Sprocket Feed Printer Set and for Replacing the 153771 through 153787 Guide Bracket Using the 159356 Modification Kit | [Issue 17, 1973-08](https://www.navy-radio.com/manuals/tty/jh/ttyman6/specs/5792S-Iss17.pdf) |
| Specification 50494S | Instructions for Installing Modification Kit 319820 to Convert a Model 37 Friction Feed Typing Unit to a Sprocket Feed Typing Unit                                                                                                                                                                                   | [Issue 1, 1967-07](https://www.navy-radio.com/manuals/tty/spec/50494S-6707.pdf)              |
| Specification 50755S | Instructions for Installing the 343264 Manual Keyboard Entry Modification Kit in Model 37 Contention Type Selective Calling System                                                                                                                                                                                   | 1973-11                                                                                      |

### Collections

- navy-radio: [Teletype Corporation Specifications](https://www.navy-radio.com/tty/ttycorp-specs.htm)
- navy-radio: [Teletype Corp. Maintenance, Installation, Operation, and Parts Publications
  (plus some miscellaneous TTY/RATT/RTTY manuals)](https://www.navy-radio.com/manuals-ttycorp.htm)

### Other

- [“37 Catalog Supplement”](https://www.navy-radio.com/manuals/tty/sales/37-cat-supp-7206.pdf).
  Teletype Corporation. June 1972.
- [“Meet the Teletype Model 37”](https://www.navy-radio.com/manuals/tty/sales/3710-7010.pdf).
  Teletype Corporation. 1970.
- [“Maintenance of Data-Handling Terminal Equipment (Teletypewriter)”](https://www.navy-radio.com/manuals/tty/faa-tty-maint.pdf),
  Department of Transportation, Federal Aviation Administration.
  4 December 1978.
  - Maintenance of Models 28, 35, and 37.
- Unlinked on [navy-radio](https://www.navy-radio.com/manuals-ttycorp.htm):
  - 37 Receive-Only Set for Switched Network Service (316B Vol. 1)
  - 37 Receive-Only Set for Switched Network Service (316B Vol. 2 (4/70))
  - 37 KYBD Send-Receive (KSR) Set for Switched Network Service (317B Vol. 1)
  - 37 KYBD Send-Receive (KSR) Set for Switched Network Service (317B Vol. 2)
  - 37 Auto. Send-Receive (ASR) Set for Switched Network Service (318B Vol. 1 (6/70))
  - 37 Auto. Send-Receive (ASR) Set for Switched Network Service (318B Vol. 2)
  - 37 Auto. Send-Receive (ASR) Set for Switched Network Service (318B Vol. 3 (3/70))
  - 37 Receive-Only (RO) Typing Reperforator Set (ROTR) (334B)
  - 37 Radio Frequency Interference (RFI) Suppression for 37 Teletypewriter Equipment (335B/RF)
  - 37 Keyboard Send-Receive (KSR) with RFI Suppression (NAVELEX 0967-428-4010) (337B/RF Vol. 1)
  - 37 Keyboard Send-Receive (KSR) with RFI Suppression (NAVELEX 0967-428-4010) (337B/RF Vol. 2)
  - 37 Keyboard Send-Receive (KSR) with RFI Suppression (NAVELEX 0967-428-4010) (337B/RF Vol. 3)
  - 37 Keyboard Send-Receive (KSR) with RFI Suppression (NAVELEX 0967-428-4010) (337B/RF Vol. 4)
  - 37 Automatic Send-Receive (ASR) with RFI Suppression (NAVELEX 0967-428-5010) (338B/RF Vol. 1)
  - 37 Automatic Send-Receive (ASR) with RFI Suppression (NAVELEX 0967-428-5020) (338B/RF Vol. 2)
  - 37 Automatic Send-Receive (ASR) with RFI Suppression (NAVELEX 0967-428-5030) (338B/RF Vol. 3)
  - 37 Automatic Send-Receive (ASR) with RFI Suppression (NAVELEX 0967-428-5040) (338B/RF Vol. 4)
  - 37 Automatic Send-Receive Set (ASR) (1214B)
  - 37 Typing Reperforator (ROTR) Set (1217B)
- [Teletype documents](https://www.soemtron.org/teletypemanuals.html) on
  soemtron.org: hosts documents including for Teletype Model 33, 35, and 43 (not
  37), as well as information on [PDP-7 serial numbers](https://www.soemtron.org/pdp7.html)
