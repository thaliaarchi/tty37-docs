# Teletype Model 37 functional specification

## Typing unit and character set

It generates and receives all 128 ASCII characters.
\[Gen301 2.02, 2.14]\[Gen304 2.02, 2.11] It uses specifically ASCII (USAS
X3.4-1968). \[Type figure 16, figure 28]

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

Suppression codebar can be operated by stunt box to inhibit operation of certain
function bars. \[Catalog p4]

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

## Typebox

ASCII characters with their locations in an 8-row typebox and function bar
configurations: \[Type figure 28]

Columns:
- **Name**: ASCII character name
- **Abbr**: Short ASCII character name used in typebox table. \[Type figure 28]
  This seems to be used for brevity only in the table and not elsewhere.
- **ASCII**: ASCII character code in big-endian binary \[Type figure 28]
- **P**: Parity bit (8th bit), to obtain even parity. \[Type figure 16] It is 1
  when the ASCII code has an odd number of 1 bits.
- **Coord**: Coordinate in 8-row typebox \[Type figure 28]
  - Row: 0–7, top to bottom in below table
  - Column: 0–15, right to left in below table
- **Marking**: Function bar code, indicating which code levels are marking (bits
  which are 1). \[Type figure 28] Code levels 1–7 are the ASCII bits
  (least-significant bit first) and code level 8 is the parity bit. Horizontal
  positioning uses code levels 1–4 and is described in \[Type section G];
  vertical positioning uses code levels 5–7 and is described in
  \[Type section I]. The row in the typebox is calculated with
  `b6*4 + b7*2 + b5` and the column with `!b1*8 + b2*4 + b4*2 + b3`, using the
  values for each bit.
  - Code level 1: shift horizontally by 8
  - Code level 2: shift horizontally by 4
  - Code level 3: shift horizontally by 1
  - Code level 4: shift horizontally by 2
  - Code level 5: shift vertically by 1
  - Code level 6: shift vertically by 4
  - Code level 7: shift vertically by 2
  - Code level 8: parity check
- **Spacing**: Function bar code, indicating which code levels are spacing (bits
   which are 0). It is used for configuring a function bar for a code; for each
   level indicated, remove the marking tine, and for each level not indicated,
   remove the spacing tine, leaving one tine per level in the function bar
   \[Type figure 60] It is the complement of column Marking.
- **11–1**: Function bar configurations with S (spacing), M (marking), \* (both
  tines removed), or - (unclear) for each level. Each level has one or zero
  tines, a spacing tine to the right, a marking tine to the left, or neither.
  \[Type p66–68] Note that the bit order is reversed from columns Spacing and
  Marking.
- **Style**: Groups of similarly derived function bar configurations, from my
  observation.
  - A: Parity bit at level 8 and ASCII bits (most-significant bit first) at
    levels 7–1.
  - A+9S: Style A, plus spacing at level 9.
  - _?: Not specified by \[Type p66–68], but inferred from columns Marking and
    Spacing.
- **Function bar name**: The name used in Table of Function Bar Configurations,
  when different from column Name. \[Type p66–68]

Question: How is the parity check performed?

TODO: Locate these parts. They could resolve the ambiguities in Table of
Function Bar Configurations.
> <u>Note 2:</u> Universal function bars TP326076 (11 tines) and TP196342 (9
> tines) can be coded with any function. Note 3: For coding number 9, 10, and 11
> blocking bars, refer to table of function bar configurations.

TODO: Note whether high bits are in each function bar from the figures.

| Name  | Abbr | ASCII   | P | Coord | Marking    | Spacing         | 11| 10| 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 | Style | Function bar name |
| ----- | ---- | ------- | - | ----- | ---------- | --------------- | - | - | - | - | - | - | - | - | - | - | - | ----- | ----------------- |
| NUL   | NL   | 0000000 | 0 | 0,8   | `________` | 1·2·3·4·5·6·7·8 | - | - | - | S | S | S | S | S | S | S | S | A     | |
| SOH   | SH   | 0000001 | 1 | 0,0   | `1______8` | 2·3·4·5·6·7     | - | - | - | M | S | S | S | S | S | S | M | A     | |
| STX   | SX   | 0000010 | 1 | 0,12  | `_2_____8` | 1·3·4·5·6·7     | - | - | - | M | S | S | S | S | S | M | S | A     | |
| ETX   | EX   | 0000011 | 0 | 0,4   | `12______` | 3·4·5·6·7·8     | - | - | S | S | S | S | S | S | S | M | M | A+9S  | |
| EOT   | ET   | 0000100 | 1 | 0,9   | `__3____8` | 1·2·4·5·6·7     | - | - | S | M | S | S | S | S | M | S | S | A+9S  | |
| ENQ   | EQ   | 0000101 | 0 | 0,1   | `1_3_____` | 2·4·5·6·7·8     | - | - | S | S | S | S | S | S | M | S | M | A+9S  | |
| ACK   | AK   | 0000110 | 0 | 0,13  | `_23_____` | 1·4·5·6·7·8     | - | - | S | S | S | S | S | S | M | M | S | A+9S  | |
| BEL   | BL   | 0000111 | 1 | 0,5   | `123____8` | 4·5·6·7         | - | - | S | M | S | S | S | S | M | M | M | A+9S  | |
| BS    |      | 0001000 | 1 | 0,10  | `___4___8` | 1·2·3·5·6·7     | - | - | S | M | S | S | S | M | S | S | S | A+9S  | |
| HT    |      | 0001001 | 0 | 0,2   | `1__4____` | 2·3·5·6·7·8     | - | - | S | S | S | S | S | M | S | S | M | A+9S  | |
| LF    |      | 0001010 | 0 | 0,14  | `_2_4____` | 1·3·5·6·7·8     | - | - | S | S | S | S | S | M | S | M | S | A+9S  | |
| VT    |      | 0001011 | 1 | 0,6   | `12_4___8` | 3·5·6·7         | - | - | S | M | S | S | S | M | S | M | M | A+9S  | |
| FF    |      | 0001100 | 0 | 0,11  | `__34____` | 1·2·5·6·7·8     | - | - | S | S | S | S | S | M | M | S | S | A+9S  | |
| CR    |      | 0001101 | 1 | 0,3   | `1_34___8` | 2·5·6·7         | - | - | S | M | S | S | S | M | M | S | M | A+9S  | |
| SO    |      | 0001110 | 1 | 0,15  | `_234___8` | 1·5·6·7         | - | - | S | M | S | S | S | M | M | M | S | A+9S  | |
| SI    |      | 0001111 | 0 | 0,7   | `1234____` | 5·6·7·8         | - | - | S | S | S | S | S | M | M | M | M | A+9S  | |
| DLE   | DL   | 0010000 | 1 | 1,8   | `____5__8` | 1·2·3·4·6·7     | - | - | S | M | S | S | M | S | S | S | S | A+9S  | |
| DC1   | D1   | 0010001 | 0 | 1,0   | `1___5___` | 2·3·4·6·7·8     | - | - | S | S | S | S | M | S | S | S | M | A+9S  | |
| DC2   | D2   | 0010010 | 0 | 1,12  | `_2__5___` | 1·3·4·6·7·8     | - | - | S | S | S | S | M | S | S | M | S | A+9S  | |
| DC3   | D3   | 0010011 | 1 | 1,4   | `12__5__8` | 3·4·6·7         | - | - | S | M | S | S | M | S | S | M | M | A+9S  | |
| DC4   | D4   | 0010100 | 0 | 1,9   | `__3_5___` | 1·2·4·6·7·8     | - | - | S | S | S | S | M | S | M | S | S | A+9S  | |
| NAK   | NK   | 0010101 | 1 | 1,1   | `1_3_5__8` | 2·4·6·7         | - | - | S | M | S | S | M | S | M | S | M | A+9S  | |
| SYN   | SY   | 0010110 | 1 | 1,13  | `_23_5__8` | 1·4·6·7         | - | - | - | M | S | S | M | S | M | M | S | A     | |
| ETB   | EB   | 0010111 | 0 | 1,5   | `123_5___` | 4·6·7·8         | - | - | - | S | S | S | M | S | M | M | M | A     | |
| CAN   | CN   | 0011000 | 0 | 1,10  | `___45___` | 1·2·3·6·7·8     | - | - | - | S | S | S | M | M | S | S | S | A     | |
| EM    |      | 0011001 | 1 | 1,2   | `1__45__8` | 2·3·6·7         | - | - | - | M | S | S | M | M | S | S | M | A     | |
| SUB   | SB   | 0011010 | 1 | 1,14  | `_2_45__8` | 1·3·6·7         | - | - | - | M | S | S | M | M | S | M | S | A     | |
| ESC   | ES   | 0011011 | 0 | 1,6   | `12_45___` | 3·6·7·8         | - | - | - | S | S | S | M | M | S | M | M | A     | |
| FS    |      | 0011100 | 1 | 1,11  | `__345__8` | 1·2·6·7         | - | - | - | M | S | S | M | M | M | S | S | A     | |
| GS    |      | 0011101 | 0 | 1,3   | `1_345___` | 2·6·7·8         | - | - | - | S | S | S | M | M | M | S | M | A     | |
| RS    |      | 0011110 | 0 | 1,15  | `_2345___` | 1·6·7·8         | - | - | - | S | S | S | M | M | M | M | S | A     | |
| US    |      | 0011111 | 1 | 1,7   | `12345__8` | 6·7             | - | - | - | M | S | S | M | M | M | M | M | A     | |
| Space | SP   | 0100000 | 1 | 4,8   | `_____6_8` | 1·2·3·4·5·7     | - | - | - | M | S | M | S | S | S | S | S | A?    | |
| !     |      | 0100001 | 0 | 4,0   | `1____6__` | 2·3·4·5·7·8     | - | - | - | S | S | M | S | S | S | S | M | A?    | |
| "     |      | 0100010 | 0 | 4,12  | `_2___6__` | 1·3·4·5·7·8     | - | - | - | S | S | M | S | S | S | M | S | A?    | |
| #     |      | 0100011 | 1 | 4,4   | `12___6_8` | 3·4·5·7         | - | - | - | M | S | M | S | S | S | M | M | A?    | |
| $     |      | 0100100 | 0 | 4,9   | `__3__6__` | 1·2·4·5·7·8     | - | - | - | S | S | M | S | S | M | S | S | A?    | |
| %     |      | 0100101 | 1 | 4,1   | `1_3__6_8` | 2·4·5·7         | - | - | - | M | S | M | S | S | M | S | M | A?    | |
| &     |      | 0100110 | 1 | 4,13  | `_23__6_8` | 1·4·5·7         | - | - | - | M | S | M | S | S | M | M | S | A?    | |
| '     |      | 0100111 | 0 | 4,5   | `123__6__` | 4·5·7·8         | - | - | - | S | S | M | S | S | M | M | M | A?    | |
| (     |      | 0101000 | 0 | 4,10  | `___4_6__` | 1·2·3·5·7·8     | - | - | - | S | S | M | S | M | S | S | S | A?    | |
| )     |      | 0101001 | 1 | 4,2   | `1__4_6_8` | 2·3·5·7         | - | - | - | M | S | M | S | M | S | S | M | A?    | |
| *     |      | 0101010 | 1 | 4,14  | `_2_4_6_8` | 1·3·5·7         | - | - | - | M | S | M | S | M | S | M | S | A?    | |
| +     |      | 0101011 | 0 | 4,6   | `12_4_6__` | 3·5·7·8         | - | - | - | S | S | M | S | M | S | M | M | A?    | |
| ,     |      | 0101100 | 1 | 4,11  | `__34_6_8` | 1·2·5·7         | - | - | - | M | S | M | S | M | M | S | S | A?    | |
| -     |      | 0101101 | 0 | 4,3   | `1_34_6__` | 2·5·7·8         | - | - | - | S | S | M | S | M | M | S | M | A?    | |
| .     |      | 0101110 | 0 | 4,15  | `_234_6__` | 1·5·7·8         | - | - | - | S | S | M | S | M | M | M | S | A?    | |
| /     |      | 0101111 | 1 | 4,7   | `1234_6_8` | 5·7             | - | - | - | M | S | M | S | M | M | M | M | A?    | |
| 0     |      | 0110000 | 0 | 5,8   | `____56__` | 1·2·3·4·7·8     | - | - | - | S | S | M | M | S | S | S | S | A?    | |
| 1     |      | 0110001 | 1 | 5,0   | `1___56_8` | 2·3·4·7         | - | - | - | M | S | M | M | S | S | S | M | A?    | |
| 2     |      | 0110010 | 1 | 5,12  | `_2__56_8` | 1·3·4·7         | - | - | - | M | S | M | M | S | S | M | S | A?    | |
| 3     |      | 0110011 | 0 | 5,4   | `12__56__` | 3·4·7·8         | - | - | - | S | S | M | M | S | S | M | M | A?    | |
| 4     |      | 0110100 | 1 | 5,9   | `__3_56_8` | 1·2·4·7         | - | - | - | M | S | M | M | S | M | S | S | A?    | |
| 5     |      | 0110101 | 0 | 5,1   | `1_3_56__` | 2·4·7·8         | - | - | - | S | S | M | M | S | M | S | M | A?    | |
| 6     |      | 0110110 | 0 | 5,13  | `_23_56__` | 1·4·7·8         | - | - | - | S | S | M | M | S | M | M | S | A?    | |
| 7     |      | 0110111 | 1 | 5,5   | `123_56_8` | 4·7             | - | - | - | M | S | M | M | S | M | M | M | A?    | |
| 8     |      | 0111000 | 1 | 5,10  | `___456_8` | 1·2·3·7         | - | - | - | M | S | M | M | M | S | S | S | A?    | |
| 9     |      | 0111001 | 0 | 5,2   | `1__456__` | 2·3·7·8         | - | - | - | S | S | M | M | M | S | S | M | A?    | |
| :     |      | 0111010 | 0 | 5,14  | `_2_456__` | 1·3·7·8         | - | - | - | S | S | M | M | M | S | M | S | A?    | |
| ;     |      | 0111011 | 1 | 5,6   | `12_456_8` | 3·7             | - | - | - | M | S | M | M | M | S | M | M | A?    | |
| <     |      | 0111100 | 0 | 5,11  | `__3456__` | 1·2·7·8         | - | - | - | S | S | M | M | M | M | S | S | A?    | |
| =     |      | 0111101 | 1 | 5,3   | `1_3456_8` | 2·7             | - | - | - | M | S | M | M | M | M | S | M | A?    | |
| >     |      | 0111110 | 1 | 5,15  | `_23456_8` | 1·7             | - | - | - | M | S | M | M | M | M | M | S | A?    | |
| ?     |      | 0111111 | 0 | 5,7   | `123456__` | 7·8             | - | - | - | S | S | M | M | M | M | M | M | A?    | |
| @     |      | 1000000 | 1 | 2,8   | `______78` | 1·2·3·4·5·6     | - | - | - | M | M | S | S | S | S | S | S | A?    | |
| A     |      | 1000001 | 0 | 2,0   | `1_____7_` | 2·3·4·5·6·8     | - | - | - | S | M | S | S | S | S | S | M | A?    | |
| B     |      | 1000010 | 0 | 2,12  | `_2____7_` | 1·3·4·5·6·8     | - | - | - | S | M | S | S | S | S | M | S | A?    | |
| C     |      | 1000011 | 1 | 2,4   | `12____78` | 3·4·5·6         | - | - | - | M | M | S | S | S | S | M | M | A?    | |
| D     |      | 1000100 | 0 | 2,9   | `__3___7_` | 1·2·4·5·6·8     | - | - | - | S | M | S | S | S | M | S | S | A?    | |
| E     |      | 1000101 | 1 | 2,1   | `1_3___78` | 2·4·5·6         | - | - | - | M | M | S | S | S | M | S | M | A?    | |
| F     |      | 1000110 | 1 | 2,13  | `_23___78` | 1·4·5·6         | - | - | - | M | M | S | S | S | M | M | S | A?    | |
| G     |      | 1000111 | 0 | 2,5   | `123___7_` | 4·5·6·8         | - | - | - | S | M | S | S | S | M | M | M | A?    | |
| H     |      | 1001000 | 0 | 2,10  | `___4__7_` | 1·2·3·5·6·8     | - | - | - | S | M | S | S | M | S | S | S | A?    | |
| I     |      | 1001001 | 1 | 2,2   | `1__4__78` | 2·3·5·6         | - | - | - | M | M | S | S | M | S | S | M | A?    | |
| J     |      | 1001010 | 1 | 2,14  | `_2_4__78` | 1·3·5·6         | - | - | - | M | M | S | S | M | S | M | S | A?    | |
| K     |      | 1001011 | 0 | 2,6   | `12_4__7_` | 3·5·6·8         | - | - | - | S | M | S | S | M | S | M | M | A?    | |
| L     |      | 1001100 | 1 | 2,11  | `__34__78` | 1·2·5·6         | - | - | - | M | M | S | S | M | M | S | S | A?    | |
| M     |      | 1001101 | 0 | 2,3   | `1_34__7_` | 2·5·6·8         | - | - | - | S | M | S | S | M | M | S | M | A?    | |
| N     |      | 1001110 | 0 | 2,15  | `_234__7_` | 1·5·6·8         | - | - | - | S | M | S | S | M | M | M | S | A?    | |
| O     |      | 1001111 | 1 | 2,7   | `1234__78` | 5·6             | - | - | - | M | M | S | S | M | M | M | M | A?    | |
| P     |      | 1010000 | 0 | 3,8   | `____5_7_` | 1·2·3·4·6·8     | - | - | - | S | M | S | M | S | S | S | S | A?    | |
| Q     |      | 1010001 | 1 | 3,0   | `1___5_78` | 2·3·4·6         | - | - | - | M | M | S | M | S | S | S | M | A?    | |
| R     |      | 1010010 | 1 | 3,12  | `_2__5_78` | 1·3·4·6         | - | - | - | M | M | S | M | S | S | M | S | A?    | |
| S     |      | 1010011 | 0 | 3,4   | `12__5_7_` | 3·4·6·8         | - | - | - | S | M | S | M | S | S | M | M | A?    | |
| T     |      | 1010100 | 1 | 3,9   | `__3_5_78` | 1·2·4·6         | - | - | - | M | M | S | M | S | M | S | S | A?    | |
| U     |      | 1010101 | 0 | 3,1   | `1_3_5_7_` | 2·4·6·8         | - | - | - | S | M | S | M | S | M | S | M | A?    | |
| V     |      | 1010110 | 0 | 3,13  | `_23_5_7_` | 1·4·6·8         | - | - | - | S | M | S | M | S | M | M | S | A?    | |
| W     |      | 1010111 | 1 | 3,5   | `123_5_78` | 4·6             | - | - | - | M | M | S | M | S | M | M | M | A?    | |
| X     |      | 1011000 | 1 | 3,10  | `___45_78` | 1·2·3·6         | - | - | - | M | M | S | M | M | S | S | S | A?    | |
| Y     |      | 1011001 | 0 | 3,2   | `1__45_7_` | 2·3·6·8         | - | - | - | S | M | S | M | M | S | S | M | A?    | |
| Z     |      | 1011010 | 0 | 3,14  | `_2_45_7_` | 1·3·6·8         | - | - | - | S | M | S | M | M | S | M | S | A?    | |
| [     |      | 1011011 | 1 | 3,6   | `12_45_78` | 3·6             | - | - | - | M | M | S | M | M | S | M | M | A?    | |
| \     |      | 1011100 | 0 | 3,11  | `__345_7_` | 1·2·6·8         | - | - | - | S | M | S | M | M | M | S | S | A?    | |
| ]     |      | 1011101 | 1 | 3,3   | `1_345_78` | 2·6             | - | - | - | M | M | S | M | M | M | S | M | A?    | |
| ^     |      | 1011110 | 1 | 3,15  | `_2345_78` | 1·6             | - | - | - | M | M | S | M | M | M | M | S | A?    | |
| _     |      | 1011111 | 0 | 3,7   | `12345_7_` | 6·8             | - | - | - | S | M | S | M | M | M | M | M | A?    | |
| `     |      | 1100000 | 0 | 6,8   | `_____67_` | 1·2·3·4·5·8     | - | - | - | S | M | M | S | S | S | S | S | A?    | |
| a     |      | 1100001 | 1 | 6,0   | `1____678` | 2·3·4·5         | - | - | - | M | M | M | S | S | S | S | M | A?    | |
| b     |      | 1100010 | 1 | 6,12  | `_2___678` | 1·3·4·5         | - | - | - | M | M | M | S | S | S | M | S | A?    | |
| c     |      | 1100011 | 0 | 6,4   | `12___67_` | 3·4·5·8         | - | - | - | S | M | M | S | S | S | M | M | A?    | |
| d     |      | 1100100 | 1 | 6,9   | `__3__678` | 1·2·4·5         | - | - | - | M | M | M | S | S | M | S | S | A?    | |
| e     |      | 1100101 | 0 | 6,1   | `1_3__67_` | 2·4·5·8         | - | - | - | S | M | M | S | S | M | S | M | A?    | |
| f     |      | 1100110 | 0 | 6,13  | `_23__67_` | 1·4·5·8         | - | - | - | S | M | M | S | S | M | M | S | A?    | |
| g     |      | 1100111 | 1 | 6,5   | `123__678` | 4·5             | - | - | - | M | M | M | S | S | M | M | M | A?    | |
| h     |      | 1101000 | 1 | 6,10  | `___4_678` | 1·2·3·5         | - | - | - | M | M | M | S | M | S | S | S | A?    | |
| i     |      | 1101001 | 0 | 6,2   | `1__4_67_` | 2·3·5·8         | - | - | - | S | M | M | S | M | S | S | M | A?    | |
| j     |      | 1101010 | 0 | 6,14  | `_2_4_67_` | 1·3·5·8         | - | - | - | S | M | M | S | M | S | M | S | A?    | |
| k     |      | 1101011 | 1 | 6,6   | `12_4_678` | 3·5             | - | - | - | M | M | M | S | M | S | M | M | A?    | |
| l     |      | 1101100 | 0 | 6,11  | `__34_67_` | 1·2·5·8         | - | - | - | S | M | M | S | M | M | S | S | A?    | |
| m     |      | 1101101 | 1 | 6,3   | `1_34_678` | 2·5             | - | - | - | M | M | M | S | M | M | S | M | A?    | |
| n     |      | 1101110 | 1 | 6,15  | `_234_678` | 1·5             | - | - | - | M | M | M | S | M | M | M | S | A?    | |
| o     |      | 1101111 | 0 | 6,7   | `1234_67_` | 5·8             | - | - | - | S | M | M | S | M | M | M | M | A?    | |
| p     |      | 1110000 | 1 | 7,8   | `____5678` | 1·2·3·4         | - | - | - | M | M | M | M | S | S | S | S | A?    | |
| q     |      | 1110001 | 0 | 7,0   | `1___567_` | 2·3·4·8         | - | - | - | S | M | M | M | S | S | S | M | A?    | |
| r     |      | 1110010 | 0 | 7,12  | `_2__567_` | 1·3·4·8         | - | - | - | S | M | M | M | S | S | M | S | A?    | |
| s     |      | 1110011 | 1 | 7,4   | `12__5678` | 3·4             | - | - | - | M | M | M | M | S | S | M | M | A?    | |
| t     |      | 1110100 | 0 | 7,9   | `__3_567_` | 1·2·4·8         | - | - | - | S | M | M | M | S | M | S | S | A?    | |
| u     |      | 1110101 | 1 | 7,1   | `1_3_5678` | 2·4             | - | - | - | M | M | M | M | S | M | S | M | A?    | |
| v     |      | 1110110 | 1 | 7,13  | `_23_5678` | 1·4             | - | - | - | M | M | M | M | S | M | M | S | A?    | |
| w     |      | 1110111 | 0 | 7,5   | `123_567_` | 4·8             | - | - | - | S | M | M | M | S | M | M | M | A?    | |
| x     |      | 1111000 | 0 | 7,10  | `___4567_` | 1·2·3·8         | - | - | - | S | M | M | M | M | S | S | S | A?    | |
| y     |      | 1111001 | 1 | 7,2   | `1__45678` | 2·3             | - | - | - | M | M | M | M | M | S | S | M | A?    | |
| z     |      | 1111010 | 1 | 7,14  | `_2_45678` | 1·3             | - | - | - | M | M | M | M | M | S | M | S | A?    | |
| {     |      | 1111011 | 0 | 7,6   | `12_4567_` | 3·8             | - | - | - | S | M | M | M | M | S | M | M | A?    | |
| \|    |      | 1111100 | 1 | 7,11  | `__345678` | 1·2             | - | - | - | M | M | M | M | M | M | S | S | A?    | |
| }     |      | 1111101 | 0 | 7,3   | `1_34567_` | 2·8             | - | - | - | S | M | M | M | M | M | S | M | A?    | |
| ~     |      | 1111110 | 0 | 7,15  | `_234567_` | 1·8             | - | - | - | S | M | M | M | M | M | M | S | A?    | |
| DEL   | DE   | 1111111 | 1 | 7,7   | `12345678` | NONE            | - | - | - | M | M | M | M | M | M | M | M | A     | PRINT & SPACE SUPPRESS DELETE |

Other function bar configurations: \[Type p66–68]

|                                     | 11| 10| 9 | 8 | 7 | 6 | 5 | 4 | 3 | 2 | 1 |
| ----------------------------------- | - | - | - | - | - | - | - | - | - | - | - |
| NEW LINE (LF & VT) **               |   |   | S |   | S | S | S | M | S | M |   |
| ESC HOLD                            |   |   | M |   | S | M | S |   |   |   |   |
| ESC TERMINATE                       |   |   | M |   |   |   |   |   |   |   |   |
| PRINT & SPACE SUPPRESS FUNCTION *** |   |   | S |   | S | S |   |   |   |   |   |
| CR & FF ***                         |   |   | S |   | S | S | S | M | M | S |   |
| PRINT & SUPPRESS SHIFT-OUT ***      |   |   |   |   | M | M |   |   |   |   |   |
| PRINT SUPPRESS NO. 1 ***            |   |   | S |   | S | M |   |   |   |   |   |
| PRINT SUPPRESS NO. 2 ***            |   |   | S |   | M |   |   |   |   |   |   |
| CR & FF (SPECIAL) ***               |   |   |   |   | S | S | S | M | M | S |   |
| LF & VT (SPECIAL) ***               |   |   |   |   | S | S | S | M | S | M |   |
| TILDE (OVERSCORE)                   |   |   | S |   | M | M | M | M | M | M | S |
| HYPHEN (TIME)                       |   |   | S |   | S | M | S | M | M | S | M |
| BLACK                               |   | S | M | M | S | M | M | S | M | S | S |
| RED                                 |   | S | M | S | S | M | M | S | S | M | M |
| HORIZ TAB SET                       |   | S | M | M | S | M | M | S | S | S | M |
| HORIZ TAB CLEAR                     |   | S | M | M | S | M | M | S | S | M | S |
| VERT TAB SET                        |   | S | M | S | S | M | M | S | M | S | M |
| VERT TAB CLEAR                      |   | S | M | S | S | M | M | S | M | M | S |
| REVERSE LINE FEED                   |   | S | M | M | S | M | M | S | M | M | M |
| HALF REVERSE LINE FEED              |   | S | M | M | S | M | M | M | S | S | S |
| HALF LINE FEED                      |   | S | M | S | S | M | M | M | S | S | M |
| HALF DUPLEX                         |   | S | M | M | S | M | M | M | S | M | M |
| FULL DUPLEX                         |   | S | M | S | S | M | M | M | S | M | S |
| PRINT SUPPRESS (ESCAPE ^)           |   | S | M | M | M | S | M | M | M | M | S |
| PRINT SUPPRESS DISABLE (ESCAPE \)   |   | S | M | S | M | S | M | M | M | S | S |
| AUTO CR & LF (SEE Note)             | S | * | * | * | * | * | * | * | * | * | * |

8-row typebox arrangement, as viewed from the print hammer: \[Type figure 28]

|     | Column  | 15   | 14   | 13   | 12   | 11   | 10   | 9    | 8    | 7    | 6    | 5    | 4    | 3    | 2    | 1    | 0    |
| --- | ------- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- | ---- |
| Row | Bits    | 1110 | 1010 | 0110 | 0010 | 1100 | 1000 | 0100 | 0000 | 1111 | 1011 | 0111 | 0011 | 1101 | 1001 | 0101 | 0001 |
| 0   | 000xxxx | SO   | LF   | ACK  | STX  | FF   | BS   | EOT  | NUL  | SI   | VT   | BEL  | ETX  | CR   | HT   | ENQ  | SOH  |
| 1   | 001xxxx | RS   | SUB  | SYN  | DC2  | FS   | CAN  | DC4  | DLE  | US   | ESC  | ETB  | DC3  | GS   | EM   | NAK  | DC1  |
| 2   | 100xxxx | N    | J    | F    | B    | L    | H    | D    | @    | O    | K    | G    | C    | M    | I    | E    | A    |
| 3   | 101xxxx | ^    | Z    | V    | R    | \    | X    | T    | P    | _    | [    | W    | S    | ]    | Y    | U    | Q    |
| 4   | 010xxxx | .    | *    | &    | "    | ,    | (    | $    | Space| /    | +    | '    | #    | -    | )    | %    | !    |
| 5   | 011xxxx | >    | :    | 6    | 2    | <    | 8    | 4    | 0    | ?    | ;    | 7    | 3    | =    | 9    | 5    | 1    |
| 6   | 110xxxx | n    | j    | f    | b    | l    | h    | d    | `    | o    | k    | g    | c    | m    | i    | e    | a    |
| 7   | 111xxxx | ~    | z    | v    | r    | \|   | x    | t    | p    | DEL  | {    | w    | s    | }    | y    | u    | q    |

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
[Spec50494S table 1]

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
  \[Type figure 15]\[Catalog p26]

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
