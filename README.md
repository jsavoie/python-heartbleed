python-heartbleed
=================

My modifications to the heartbleed python poc.  I've included an option -e to perform non-evasive tests.  Never the less the program can do 64kb heartbleeds, so please be careful and only use this on servers you own (or the cloudflarechallenge).

With a size of 16 responses look like this:
Received heartbeat response:
  0000: 02 00 0D 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C 4C  ...LLLLLLLLLLLLL
  0010: 02 2D 54 BD 7E 33 8D 1C 25 95 2C EF D9 29 9B 1B  .-T.~3..%.,..)..

Which only reads into the random padding.
