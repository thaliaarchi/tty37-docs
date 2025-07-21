# Teletype Model 37 functional specification

## Character repeat

When a key is pressed harder than normally (beyond its normal stop position),
its associated character is generated repeatedly at the maximum character rate.
Character repeat is an optional feature and can be enabled or disabled by a
technician. \[General71 2.04, 2.15]\[General72 2.12]

This feature is provided for each key that generates a character. It is normally
disabled on all keys except for the following: space, NEW LINE, BACKSPACE, NULL,
DELETE, period `.`, hyphen `-`, equal `=`, underscore `_`, colon `:`, asterisk
`*`, and character X \[sic]. Form feed is non-repeating. \[General71 2.04, 2.15]
(N.B. the meaning of “character X” is unclear; it probably means letters, but
also numbers?)

In the models in \[General72], character repeat is a standard feature and
enabled for every key. \[2.02, 2.12] Those models space on all characters, even
control characters\[4.08], so this appears to simplify the mechanism.

The maximum character rate (only specified for \[General72]) is 59.02 wpm.
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
