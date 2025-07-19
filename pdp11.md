# Specifications

Research questions:
- What I/O devices did Unix support throughout its lifetime?
- How does Unix transform byte streams for the terminal?
- What I/O devices does SIMH support and what are their protocols?
- How does the PiDP-11 configure its devices?

## SIMH

Interdata [Teletype interface](https://opensimh.org/simdocs/id_doc.html#console-teletype-interface-tt)

### DL11 terminal

SIMH has two devices for the DL11 terminal, Terminal Input (TTI) and Output
(TTO).

They are configured with `SET (TTY|TTO) <OPTION>` and have options for setting
the mode and parity. Only one mode and one parity option is active at once.
`KSR` is an alias for setting `UC` mode and `MARK` parity.[^simh_tables][^simh_dl11_doc]

The possible mode options are:
- `KSR`: Keyboard Send-Receive teletype mode
- `UC`: Uppercase mode
- `7b`: 7-bit mode
- `8b`: 8-bit mode
- `7p`: 7-bit mode - non printing suppressed

The possible parity options are:
- `SPACE`: Space parity
- `MARK`: Mark parity
- `EVEN`: Even parity
- `ODD`: Odd parity

[^simh_dl11_doc]: SIMH: [PDP-11 Simulator Usage](https://simh.trailing-edge.com/pdf/pdp11_doc.pdf),
  sections 2.3.3 DL11 Terminal Input (TTI) and 2.3.4 DL11 Terminal Output (TTO),
  updated 2022-12-12
[^simh_tables]: SIMH: PDP-11 standard I/O devices simulator, tables `tti_mod` and
  `tto_mod` in [PDP11/pdp11_stddev.c](https://github.com/open-simh/simh/blob/c65eb24d9ad1beea0b9c6f5bec1bd9ef351fb6ec/PDP11/pdp11_stddev.c),
  updated 2020-09-15

### Other I/O devices

- [PC11 Paper-Tape Reader/Punch Control](https://gunkies.org/wiki/PC11_High-Speed_Paper-Tape_Reader/Punch_Control)
  (PTR, PTP)
- LP11 Line Printer (LPT)

## Unix

[^setup_v6]: [Setting up UNIX - Sixth Edition](https://gunkies.org/wiki/Setting_up_UNIX_-_Sixth_Edition),
  rendered from V6 [/usr/doc/start/start](https://www.tuhs.org/cgi-bin/utree.pl?file=V6/usr/doc/start/start)
[^setup_v7]: [Setting up UNIX - Seventh Edition](https://gunkies.org/wiki/Setting_Up_Unix_-_Seventh_Edition),
  rendered from V7 [/usr/doc/setup](https://www.tuhs.org/cgi-bin/utree.pl?file=V7/usr/doc/setup)

## PiDP-11
