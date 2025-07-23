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
- Nonrepeat form feed (variable) \[2.04]
- Disconnect capability on EOT character (variable) \[2.04]
- Form advance (form-out) (variable) \[2.04]
- Vertical tabulation (craftsman adjustable) (variable) \[2.04]
- Horizontal tabulation (craftsman adjustable) (variable) \[2.04]

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

## Interfacing

The channel interface signals conform to the EIA (Electronics Industries
Association) Standard [RS-232-B](https://en.wikipedia.org/wiki/RS-232)
\[1.02]\[2.02]\[2.27]\[4.05]

TODO:
- [Teletype 37 ASR General Description](https://www.navy-radio.virhistory.com/manuals/tty/m37/574-302-102-iss1-7105.pdf)
  (section 574-302-102, issue 1, May 1971)
- <https://retrocomputing.stackexchange.com/questions/4456/what-protocol-do-teletypes-use>
