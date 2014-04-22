python-heartbleed
=================

My modifications to the heartbleed python poc.  I've included an option -e to perform non-evasive tests.  Never the less the program can do 64kb heartbleeds, so please be careful and only use this on servers you own (or the cloudflarechallenge).

With a size of 32 responses look like this:
Received heartbeat response:
  0000: 02 00 1D 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C  ...LLLLLLLLLLLLL
  0010: 50 50 50 50 50 50 50 50 50 50 50 50 50 50 50 50  PPPPPPPPPPPPPPPP
  0020: D2 E9 6E AB 40 F3 2A 8E 88 58 74 E2 5D C3 F6 F1  ..n.@.*..Xt.]...

Which only reads into the random padding.
