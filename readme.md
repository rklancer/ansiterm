This project consists of the files Ansiterm.h, Ansiterm.cpp, and ansiTest.pde, which have been extracted from Bruce Robertson's qrpTracker project hosted at http://code.google.com/p/qrptracker/ and then lightly modified.

They implement an Arduino library for emitting ANSI terminal control codes over the serial port. This allows your Arduino program to present "nice", screen-oriented instead of character-by-character output to the computer connected to the Arduino's serial port. See http://wiki.bash-hackers.org/scripting/terminalcodes for more information about ANSI codes.

In order to view the output, you will need to use an ANSI capable terminal emulator program. The serial monitor embedded in the Arduino IDE does not correctly interpret the terminal codes. Instead of seeing a nice display, it shows you something along the lines of

    [40m[1J[H[42mTesting 'forward', 'backward', 'up', 'down', and overwriting ...

OS X includes GNU screen, which is sufficiently capable. Example of use from an OS X Terminal window:

    $ screen /dev/tty.usbmodemfd131 38400

The first argument to `screen` is the TTY device you need to listen to; if your Arduino serial monitor works (except of course for its inability to interpret the codes above) then the correct value of the argument is the value of the checked item under the Tools -> Serial Port menu in the Arduino IDE. The second argument is the baud rate. This is set within your program.
