# GTKTerm

GTKTerm is a GTK+ serial port terminal

## License

GPL-3.0 - See COPYING

## Wiki

See https://github.com/zdavkeos/gtkterm/wiki for documentation.

## Usage

### Command line options

> --help or -h : this help screen
> --config <configuration> or -c : load configuration
> --port <device> or -p : serial port device (default /dev/ttyS0)
> --speed <speed> or -s : serial port speed (default 9600)
> --bits <bits> or -b : number of bits (default 8)
> --stopbits <stopbits> or -t : number of stopbits (default 1)
> --parity <odd | even> or -a : parity (default none)
> --flow <Xon | CTS> or -w : flow control (default none)
> --delay <ms> or -d : end of line delay in ms (default none)
> --char <char> or -r : wait for a special char at end of line (default none)
> --file <filename> or -f : default file to send (default none)
> --echo or -e : switch on local echo

### Keyboard shortcuts

As Gtkterm is often used like a terminal emulator, the shortcut keys
are assigned to <ctrl><shift>, rather than just <ctrl>.  This allows
the user to send keystrokes of the form <ctrl>X and not have Gtkterm
intercept them.

> <ctrl><shift>L -- Clear screen
> <ctrl><shift>R -- Send file
> <ctrl><shift>Q -- Quit 
> <ctrl><shift>S -- Configure port
> <ctrl><shift>V -- Paste
> <ctrl><shift>C -- Copy
> <ctrl>B	 -- Send break

## NOTES on RS485

The RS485 flow control is a software user-space emulation and
therefore may not work for all configurations (won't respond quickly
enough).  If this is the case for your setup, you will need to either
use a dedicated RS232 to RS485 converter, or look for a kernel level
driver.  This is an inherent limitation to user space programs.

## Building:

GtkTerm has a few dependencies-

* Gtk+2.0 (version 2.6 or higher)
* vte (version 0.20 or higher)
* intltool (version 0.40.0 or higher)

Once these dependencies are installed, most people should simply run:

> ./configure
>  make

And to install:

> make install
