# Teletype Model 37 functional specification

## Typing unit and character set

It generates and receives all 128 ASCII characters.
\[General71 2.02, 2.14]\[General72 2.02, 2.11]

The typing unit prints characters onto paper (called “page copy”) by positioning
the typebox by an “aggregate motion mechanism”. The typebox is moved from
character to character and is retracted when reception stops, making all
characters visible when the machine is idle. \[General71 2.06]\[General72 2.04]

The typing unit usually only prints the 94 graphic ASCII characters, though is
capable of printing symbols for all 128 characters. \[General71 2.07]

The \[General72] model prints visible symbols for 127 ASCII characters,
excluding space, and spaces on all characters. It provides an eight-row typebox
with pallets in the upper two rows for 32 control characters. \[2.02, 2.05,
4.08]

Questions:
- Does “aggregate motion” simply refer to two-dimensional movement?
- What are the configurations of number of rows for typeboxes?
- What are the symbols printed for control characters?

## Parity

Generates all 128 ASCII characters with even parity (standard feature).
\[General71 2.02]\[General72 2.02]

## Character repeat feature

When a key is pressed harder than normally (beyond its normal stop position),
its associated character is generated repeatedly at the maximum character rate.
Character repeat is an optional feature and can be enabled or disabled by a
technician. \[General71 2.04, 2.15]\[General72 2.12]

This feature is provided for each key that generates a character. It is normally
disabled on all keys except for the following: space, NEW LINE, BACKSPACE, NULL,
DELETE, period `.`, hyphen `-`, equal `=`, underscore `_`, colon `:`, asterisk
`*`, and character X \[sic]. Form feed is non-repeating. \[General71 2.04, 2.15]

Question: The meaning of “character X” is unclear. Does it mean letters and
possibly also numbers?

In the \[General72] KSR model, character repeat is a standard feature and
enabled for every key. \[2.02, 2.12] That model spaces on all characters, even
control characters\[4.08], so this appears to simplify the mechanism.

The maximum character rate (for at least the \[General72] model) is 59.02 wpm.
\[2.12]

\[Dolotta70] proscribes a desired operation for character repeat like the Model
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

## References

- \[General71]: [“37 Keyboard Send-Receive (KSR) Teletypewriter Set and 37
  Automatic Send-Receive (ASR) Teletypewriter Set for "DATA-PHONE®" Service:
  General Description and Operation”](https://www.navy-radio.virhistory.com/manuals/tty/m37/574-301-100-iss1-7106.pdf).
  Prepared for AT&T by Teletype Corporation.
  Bell System Practices, AT&TCo Standard,
  Section 574-301-100, Issue 1, June 1971.

- \[General72]: [“37 Keyboard Send-Receive (KSR) Teletypewriter Set Used in
  Telegraph Test Boards and Service Boards: General Description and
  Operation”](https://www.navy-radio.virhistory.com/manuals/tty/m37/574-304-100-iss2-7212.pdf).
  Prepared for AT&T by Teletype Corporation.
  Bell System Practices, AT&TCo Standard,
  Section 574-304-100, Issue 2, December 1972.
  - This document appears to be for a more specific configuration of the
    Teletype Model 37 KSR than \[General71], as it does not describe ASR, omits
    some features, and makes some optional features standard.

- \[Dolotta70]: [“Functional Specifications for Typewriter-Like Time-Sharing
  Terminals”](https://dl.acm.org/doi/10.1145/356561.356563).
  T. A. Dolotta. ACM Computing Surveys, March 1970.
  - A statement to terminal manufacturers on user needs for time-sharing
    computer systems. It references the operation of the Teletype Model 37, but
    cannot be considered reliable.

### Bell System Practices

Documents in the [Bell System Practices](http://bellsystempractices.org/) series
pertaining to the 37 KSR and ASR sets.

Referrers:
1. \[General71 5.01]
2. \[General72 5.01]

| Number      | Component                                | Title                                                                | Referrers |
| ----------- | ---------------------------------------- | -------------------------------------------------------------------- | --------- |
| 574-301-200 | KSR Set                                  | Installation                                                         | 1         |
| 574-301-702 | KSR Set                                  | Removal and Replacement of Components                                | 1         |
| 574-304-100 | KSR Set                                  | General Description and Operation                                    | 2         |
| 574-304-200 | KSR Set                                  | Installation                                                         | 2         |
| 574-304-300 | KSR Set                                  | Troubleshooting                                                      | 2         |
| 579-400-350 | KSR Set                                  | Field Maintenance Practice                                           | 1         |
| 574-302-200 | ASR Set                                  | Installation                                                         | 1         |
| 574-302-702 | ASR Set                                  | Removal and Replacement of Components                                | 1         |
| 570-220-100 | Motor Unit                               | Description and Principles of Operation                              | 1, 2      |
| 570-220-700 | Motor Unit                               | Adjustments                                                          | 1, 2      |
| 570-220-701 | Motor Unit                               | Lubrication                                                          | 1, 2      |
| 570-220-702 | Motor Unit                               | Disassembly and Reassembly                                           | 1         |
| 570-220-800 | Motor Unit                               | Parts                                                                | 2         |
| 574-320-101 | Typing Unit                              | Description and Principles of Operation                              | 1, 2      |
| 574-320-702 | Typing Unit                              | Disassembly and Reassembly                                           | 2         |
| 574-320-703 | Typing Unit                              | Adjustments                                                          | 1, 2      |
| 574-320-704 | Typing Unit                              | Lubrication                                                          | 1, 2      |
| 574-320-705 | Typing Unit                              | Disassembly and Reassembly                                           | 1         |
| 574-320-801 | Typing Unit                              | Parts                                                                | 2         |
| 574-321-101 | Keyboard Unit                            | Description and Principles of Operation                              | 1, 2      |
| 574-321-703 | Keyboard Unit                            | Adjustments                                                          | 1, 2      |
| 574-321-704 | Keyboard Unit                            | Lubrication                                                          | 1, 2      |
| 574-321-705 | Keyboard Unit                            | Disassembly and Reassembly                                           | 1, 2      |
| 574-321-801 | Keyboard Unit                            | Parts                                                                | 2         |
| 574-322-101 | Electrical Service Unit                  | Description and Operation                                            | 1         |
| 574-322-801 | Electrical Service Unit                  | Parts                                                                | 2         |
| 574-323-101 | Table                                    | Description and Operation                                            | 1         |
| 574-323-703 | Table                                    | Adjustments                                                          | 1         |
| 574-331-100 | Base                                     | Description and Principles of Operation, Adjustments and Lubrication | 2         |
| 574-331-800 | Base                                     | Parts                                                                | 2         |
| 574-326-101 | Typing Unit Cover and Pan                | Description and Principles of Operation                              | 1, 2      |
| 574-326-703 | Typing Unit Cover and Pan                | Adjustments                                                          | 1, 2      |
| 574-326-704 | Typing Unit Cover and Pan                | Lubrication                                                          | 1, 2      |
| 574-326-801 | Typing Unit Cover and Pan                | Parts                                                                | 2         |
| 574-330-100 | Typing Reperforator                      | Description and Operation                                            | 1         |
| 574-330-700 | Typing Reperforator                      | Adjustments                                                          | 1         |
| 574-330-701 | Typing Reperforator                      | Lubrication                                                          | 1         |
| 574-330-702 | Typing Reperforator                      | Disassembly and Reassembly                                           | 1         |
| 574-325-703 | Answer-Back Unit                         | Adjustments                                                          | 1         |
| 574-325-704 | Answer-Back Unit                         | Lubrication                                                          | 1         |
| 574-329-100 | Nontyping Reperforator                   | Description and Principles of Operation                              | 1         |
| 574-329-700 | Nontyping Reperforator                   | Adjustments                                                          | 1         |
| 574-329-701 | Nontyping Reperforator                   | Lubrication                                                          | 1         |
| 574-329-702 | Nontyping Reperforator                   | Disassembly and Reassembly                                           | 1         |
| 574-332-100 | Paper Winder                             | Description, Installation, Adjustments and Lubrication               | 2         |
| 574-332-800 | Paper Winder                             | Parts                                                                | 2         |
| 592-801-100 | Tape Reader                              | Description and Principles of Operation                              | 1         |
| 592-801-700 | Tape Reader                              | Adjustments                                                          | 1         |
| 592-801-701 | Tape Reader                              | Lubrication                                                          | 1         |
| 592-801-702 | Tape Reader                              | Disassembly and Reassembly                                           | 1         |
| 574-327-100 | RT Module Cabinet                        | Description and Operation                                            | 1         |
| 574-327-700 | RT Module Cabinet                        | Adjustments                                                          | 1         |
| 574-327-701 | RT Module Cabinet                        | Lubrication                                                          | 1         |
| WDP0283     | Wiring Diagrams and Circuit Descriptions | KSR Set - WD Package                                                 | 2         |
