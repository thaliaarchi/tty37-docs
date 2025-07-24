# Unix terminal support

V7 /usr/man/man0/intro

> ## Logging in.
>
> You must call UNIX from an appropriate terminal. UNIX terminals are typified
> by the TTY 43, the GE Terminet 300, the DASI 300S and 450, and most video
> terminals such as the Datamedia 5120 or HP 2640. You must also have a valid
> user name, which may be obtained, together with the telephone number, from the
> system administrators. The same telephone number serves terminals operating at
> all the standard speeds. After a data connection is established, the login
> procedure depends on what kind of terminal you are using.
>
> **300-baud terminals:**
>
> Such terminals include the GE Terminet 300 and most display terminals run with
> popular modems. These terminals generally have a speed switch which should be
> set at ‘300’ (or ‘30’ for 30 characters per second) and a half/full duplex
> switch which should be set at full-duplex. (This switch will often have to be
> changed since many other systems require half-duplex). When a connection is
> established, the system types ‘login:’; you type your user name, followed by
> the ‘return’ key. If you have a password, the system asks for it and turns off
> the printer on the terminal so the password will not appear. After you have
> logged in, the ‘return’, ‘new line’, or ‘linefeed’ keys will give exactly the
> same results.
>
> **1200- and 150-baud terminals:** If there is a half/full duplex switch, set
> it at full-duplex. When you have established a data connection, the system
> types out a few garbage characters (the ‘login:’ message at the wrong speed).
> Depress the ‘break’ (or ‘interrupt’) key; this is a speed-independent signal
> to UNIX that a different speed terminal is in use. The system then will type
> ‘login:,’ this time at another speed. Continue depressing the break key until
> ‘login:’ appears in clear, then respond with your user name. From the TTY 37
> terminal, and any other which has the ‘newline’ function (combined carriage
> return and linefeed), terminate each line you type with the ‘new line’ key,
> otherwise use the ‘return’ key.
>
> **Hard-wired terminals.**
>
> Hard-wired terminals usually begin at the right speed, up to 9600 baud;
> otherwise the preceding instructions apply.
>
> For all these terminals, it is important that you type your name in lower-case
> if possible; if you type upper-case letters, UNIX will assume that your
> terminal cannot generate lower-case letters and will translate all subsequent
> upper-case letters to lower case.
>
> The evidence that you have successfully logged in is that the Shell program
> will type a ‘$’ to you. (The Shell is described below under ‘How to run a
> program.’)
>
> For more information, consult stty(1), which tells how to adjust terminal
> behavior, getty(8), which discusses the login sequence in more detail, and
> tty(4), which discusses terminal I/O.

## tabs(1)

Supported terminals and their identifiers:

- `dasi300`, `300`: DASI 300
- `dasi300s`, `300s`: DASI 300S
- `dasi450`, `450`: DASI 450
- `37`, `tty37`: Teletype Model 37
- `tn300`, `terminet`, `tn`: TermiNet 300
- `hp`: HP 2645

Procedure for the Teletype Model 37:

1. Shift in: SI
2. Clear tab stops:
   1. Clear horizontal tab stops: ESC 2
   2. Delay for 40 units: DEL (40 times)
   3. New line: CR LF
3. BS (8 times)
4. Set tab stops:
   1. Repeat 8 times or 9 times if `-n`:
      1. Space (8 times)
      2. Set horizontal tab stop: ESC 1
5. LF

> If the -n flag is present then the left margin is not indented as is normal.

## References

- V7 /usr/man/man0/intro
- V7 /usr/src/cmd/tabs.c
- V7 /usr/man/man1/tabs.1
