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

A keyboard interlock prevents errors caused from two keys simultaneously
pressed. \[Catalog69]

Questions:
- Does “aggregate motion” simply refer to two-dimensional movement?
- What are the configurations of number of rows for typeboxes?
- What are the symbols printed for control characters?

## Parity

Generates all 128 ASCII characters with even parity (standard feature).
\[General71 2.02]\[General72 2.02]

## Character repeat feature

The keyboard permits you to repeat a character by pressing a key harder than
normal (beyond its normal stop position), making it generate the associated
character repeatedly at the maximum character rate.
\[General71 2.15]\[General72 2.12]

Any key can be made repeatable by a technician with a simple modification. In
the standard arrangement, only the ten most commonly used keys are repeatable
(in both the shift and unshift states): \[Catalog69 7]\[General71 2.04]

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
arrangement (\[Catalog69] states that ten keys are repeatable, matching this
list).

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

- \[Catalog69]: [“Teletype Model 37 Product Catalog”](https://archive.org/details/TNM_Model_37_terminal_product_catalog_-_Teletype__20170923_0036),
  Teletype Corporation. April 1969.
  - Includes a high-quality general description and operation, examples printed
    by a Model 37, and options for various models.

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

- \[Parts67]: [“37 Page Printer Set (KSR-RO): Parts”](https://www.navy-radio.virhistory.com/manuals/tty/jh/ttyman0/TeletypeManuals/model37/1209B-Iss1.pdf).
  Teletype Corporation. Bulletin 1209B, December 1967.
  - A short list of section-800 parts documents (all listed below).

### Bell System Practices

Documents in the [Bell System Practices](http://bellsystempractices.org/) series
pertaining to the 37 KSR and ASR sets.

TODO:
- Add manuals from the large section “Model 37 - also see here” on [navy-radio](https://www.navy-radio.virhistory.com/manuals-ttycorp.htm).
  Everything else on that page with “37” has been added.
- Add manuals from [Division 574: Teletypewriter 30 Series and Teleprinters](https://www.telecomarchive.com/574.html).

Referrers:
1. \[General71 5.01] (574-301-100)
2. \[General72 5.01] (574-304-100)
3. \[Parts67]

| Number        | Component                                | Title                                                                | Version                                                                                             | Referrers |
| ------------- | ---------------------------------------- | -------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- | --------- |
| 570-020-800   |                                          | Type Pallets for Models 28, 35, and 37 Teletypewriter Sets           | [Issue 3, 1974-04](https://www.navy-radio.virhistory.com/manuals/tty/570-020-800-7404.pdf)          |           |
| 570-020-801   |                                          | Keytops for Models 37, CDT and “DATASPEED®” Printer Terminals        | [Issue 2, 1974-05](https://www.navy-radio.virhistory.com/manuals/tty/570-020-801-7405.pdf)          |           |
| 570-220-100   | Motor Unit                               | Description and Principles of Operation                              |                                                                                                     | 1, 2      |
| 570-220-700   | Motor Unit                               | Adjustments                                                          |                                                                                                     | 1, 2      |
| 570-220-701   | Motor Unit                               | Lubrication                                                          |                                                                                                     | 1, 2      |
| 570-220-702   | Motor Unit                               | Disassembly and Reassembly                                           |                                                                                                     | 1         |
| 570-220-800   | Motor Unit                               | Parts                                                                | [Issue 5, 1972-11](https://www.navy-radio.virhistory.com/manuals/tty/570-220-800-7211.pdf)          | 2         |
| 574-301-100   | KSR and ASR Set                          | General Description and Operation                                    | [Issue 1, 1971-06](https://www.navy-radio.virhistory.com/manuals/tty/m37/574-301-100-iss1-7106.pdf) |           |
| 574-301-102   | KSR Set                                  | General Description                                                  | [Issue 1, 1972-12](https://www.navy-radio.virhistory.com/manuals/tty/m37/574-301-102-iss1-7212.pdf) |           |
| 574-301-200   | KSR Set                                  | Installation                                                         | [Issue 2, 1973-02](https://www.navy-radio.virhistory.com/manuals/tty/m37/574-301-200-iss2-7302.pdf) | 1         |
| 574-301-400   | KSR Set                                  | Wiring Diagram And Circuit Descriptions                              | [Issue 1, 1969-09](https://www.navy-radio.virhistory.com/manuals/tty/m37/574-301-400-iss1-6909.pdf) |           |
| 574-301-702   | KSR Set                                  | Removal and Replacement of Components                                | [Issue 1, 1970-03](https://www.navy-radio.virhistory.com/manuals/tty/m37/574-301-702-iss1-7003.pdf) | 1         |
| 574-302-102   | ASR Set                                  | General Description                                                  | [Issue 1, 1971-05](https://www.navy-radio.virhistory.com/manuals/tty/m37/574-302-102-iss1-7105.pdf) |           |
| 574-302-200   | ASR Set                                  | Installation                                                         | [Issue 2, 1973-02](https://www.navy-radio.virhistory.com/manuals/tty/m37/574-302-200-iss2-7302.pdf) | 1         |
| 574-302-300   | ASR Set                                  | Troubleshooting                                                      | [Issue 1, 1972-04](https://www.navy-radio.virhistory.com/manuals/tty/m37/574-302-300-iss1-7204.pdf) |           |
| 574-302-702   | ASR Set                                  | Removal and Replacement of Components                                | [Issue 1, 1970-03](https://www.navy-radio.virhistory.com/manuals/tty/m37/574-302-702-iss1-7003.pdf) | 1         |
| 574-303-100   | ROTR Set                                 | Description and Operation                                            | [Issue 2, 1973-06](https://www.navy-radio.virhistory.com/manuals/tty/m37/574-303-100-iss2-7306.pdf) |           |
| 574-303-200   | ROTR Set                                 | Installation                                                         | [Issue 1, 1970-11](https://www.navy-radio.virhistory.com/manuals/tty/m37/574-303-200-iss1-7011.pdf) |           |
| 574-303-300   | ROTR Set                                 | Troubleshooting                                                      | [Issue 1, 1973-10](https://www.navy-radio.virhistory.com/manuals/tty/m37/574-303-300-iss1-7310.pdf) |           |
| 574-303-702   | ROTR Set                                 | Removal and Replacement of Components                                | [Issue 1, 1970-06](https://www.navy-radio.virhistory.com/manuals/tty/m37/574-303-702-iss1-7006.pdf) |           |
| 574-304-100   | KSR Set                                  | General Description and Operation                                    | [Issue 2, 1972-12](https://www.navy-radio.virhistory.com/manuals/tty/m37/574-304-100-iss2-7212.pdf) | 2         |
| 574-304-200   | KSR Set                                  | Installation                                                         | [Issue 2, 1972-12](https://www.navy-radio.virhistory.com/manuals/tty/m37/574-304-200-iss2-7212.pdf) | 2         |
| 574-304-300   | KSR Set                                  | Troubleshooting                                                      | [Issue 2, 1972-12](https://www.navy-radio.virhistory.com/manuals/tty/m37/574-304-300-iss2-7212.pdf) | 2         |
| 574-320-101   | Typing Unit (37P003 and up)              | Description and Principles of Operation                              | [Issue 2, 1973-02](https://www.navy-radio.virhistory.com/manuals/tty/m37/574-320-101-iss2-7302.pdf) | 1, 2      |
| 574-320-400   | Typing Unit                              | Wiring Diagrams                                                      | [Issue 1, 1971-01](https://www.navy-radio.virhistory.com/manuals/tty/m37/574-320-400-iss1-7101.pdf) |           |
| 574-320-700   | Typing Unit (Early Design)               | Adjustments                                                          | [Issue 4, 1971-03](https://www.navy-radio.virhistory.com/manuals/tty/m37/574-320-700-iss4-7103.pdf) |           |
| 574-320-702   | Typing Unit                              | Disassembly and Reassembly                                           |                                                                                                     | 2         |
| 574-320-703   | Typing Unit                              | Adjustments                                                          |                                                                                                     | 1, 2      |
| 574-320-704   | Typing Unit                              | Lubrication                                                          |                                                                                                     | 1, 2      |
| 574-320-705   | Typing Unit                              | Disassembly and Reassembly                                           |                                                                                                     | 1         |
| 574-320-800TC | Typing Unit (YP)                         |                                                                      | Issue 1, 1967-12                                                                                    | 3         |
| 574-320-801   | Typing Unit                              | Parts                                                                |                                                                                                     | 2         |
| 574-321-101   | Keyboard Unit                            | Description and Principles of Operation                              |                                                                                                     | 1, 2      |
| 574-321-703   | Keyboard Unit                            | Adjustments                                                          |                                                                                                     | 1, 2      |
| 574-321-704   | Keyboard Unit                            | Lubrication                                                          |                                                                                                     | 1, 2      |
| 574-321-705   | Keyboard Unit                            | Disassembly and Reassembly                                           |                                                                                                     | 1, 2      |
| 574-321-800TC | Keyboard (YK) and 37 Base (YB)           |                                                                      | Issue 1, 1967-12                                                                                    | 3         |
| 574-321-801   | Keyboard Unit                            | Parts                                                                |                                                                                                     | 2         |
| 574-322-101   | Electrical Service Unit                  | Description and Operation                                            |                                                                                                     | 1         |
| 574-322-800TC | Electrical Service Unit (YESU)           |                                                                      | Issue 1, 1967-12                                                                                    | 3         |
| 574-322-801   | Electrical Service Unit                  | Parts                                                                |                                                                                                     | 2         |
| 574-323-101   | Table                                    | Description and Operation                                            |                                                                                                     | 1         |
| 574-323-703   | Table                                    | Adjustments                                                          |                                                                                                     | 1         |
| 574-323-800TC | Table (YT)                               |                                                                      | Issue 1, 1967-12                                                                                    | 3         |
| 574-324-800TC | Electronic Distributor (YTD)             |                                                                      | Issue 1, 1967-12                                                                                    | 3         |
| 574-325-703   | Answer-Back Unit                         | Adjustments                                                          |                                                                                                     | 1         |
| 574-325-704   | Answer-Back Unit                         | Lubrication                                                          |                                                                                                     | 1         |
| 574-325-800TC | Answer Back (VAB)                        |                                                                      | Issue 1, 1967-12                                                                                    | 3         |
| 574-326-101   | Typing Unit Cover and Pan                | Description and Principles of Operation                              |                                                                                                     | 1, 2      |
| 574-326-703   | Typing Unit Cover and Pan                | Adjustments                                                          |                                                                                                     | 1, 2      |
| 574-326-704   | Typing Unit Cover and Pan                | Lubrication                                                          |                                                                                                     | 1, 2      |
| 574-326-800TC | Typing Unit Cover (YPC)                  |                                                                      | Issue 1, 1967-12                                                                                    | 3         |
| 574-326-801   | Typing Unit Cover and Pan                | Parts                                                                |                                                                                                     | 2         |
| 574-327-100   | RT Module Cabinet                        | Description and Operation                                            |                                                                                                     | 1         |
| 574-327-700   | RT Module Cabinet                        | Adjustments                                                          |                                                                                                     | 1         |
| 574-327-701   | RT Module Cabinet                        | Lubrication                                                          |                                                                                                     | 1         |
| 574-329-100   | Nontyping Reperforator                   | Description and Principles of Operation                              |                                                                                                     | 1         |
| 574-329-700   | Nontyping Reperforator                   | Adjustments                                                          |                                                                                                     | 1         |
| 574-329-701   | Nontyping Reperforator                   | Lubrication                                                          |                                                                                                     | 1         |
| 574-329-702   | Nontyping Reperforator                   | Disassembly and Reassembly                                           |                                                                                                     | 1         |
| 574-330-100   | Typing Reperforator                      | Description and Operation                                            |                                                                                                     | 1         |
| 574-330-700   | Typing Reperforator                      | Adjustments                                                          |                                                                                                     | 1         |
| 574-330-701   | Typing Reperforator                      | Lubrication                                                          |                                                                                                     | 1         |
| 574-330-702   | Typing Reperforator                      | Disassembly and Reassembly                                           |                                                                                                     | 1         |
| 574-331-100   | Base                                     | Description and Principles of Operation, Adjustments and Lubrication |                                                                                                     | 2         |
| 574-331-800   | Base                                     | Parts                                                                |                                                                                                     | 2         |
| 574-332-100   | Paper Winder                             | Description, Installation, Adjustments and Lubrication               |                                                                                                     | 2         |
| 574-332-800   | Paper Winder                             | Parts                                                                |                                                                                                     | 2         |
| 579-400-350   | KSR Set                                  | Field Maintenance Practice                                           |                                                                                                     | 1         |
| 592-801-100   | Tape Reader                              | Description and Principles of Operation                              |                                                                                                     | 1         |
| 592-801-700   | Tape Reader                              | Adjustments                                                          |                                                                                                     | 1         |
| 592-801-701   | Tape Reader                              | Lubrication                                                          |                                                                                                     | 1         |
| 592-801-702   | Tape Reader                              | Disassembly and Reassembly                                           |                                                                                                     | 1         |
| WDP0283       | Wiring Diagrams and Circuit Descriptions | KSR Set - WD Package                                                 |                                                                                                     | 2         |

### Other

- [“37 Catalog Supplement”](https://www.navy-radio.virhistory.com/manuals/tty/sales/37-cat-supp-7206.pdf).
  Teletype Corporation. June 1972.
- [“Meet the Teletype Model 37”](https://www.navy-radio.virhistory.com/manuals/tty/sales/3710-7010.pdf).
  Teletype Corporation. 1970.
- [“Maintenance of Data-Handling Terminal Equipment (Teletypewriter)”](https://www.navy-radio.virhistory.com/manuals/tty/faa-tty-maint.pdf),
  Department of Transportation, Federal Aviation Administration.
  4 December 1978.
  - Maintenance of Models 28, 35, and 37.
- Unlinked on [navy-radio](https://www.navy-radio.virhistory.com/manuals-ttycorp.htm):
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
