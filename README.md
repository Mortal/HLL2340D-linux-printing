# Fixes to Brother HLL2340D print driver

The [official Linux drivers for Brother HLL2340D](http://support.brother.com/g/b/downloadlist.aspx?c=us&lang=en&prod=hll2340dw_us_eu_as&os=128)
can be made to work with the modified files in this repository.

Install both the CUPSwrapper printer driver (deb package) and the
LPR printer driver (deb package), since the CUPSwrapper driver uses
programs from the LPR driver.

`/opt/brother/Printers/HLL2340D/lpd/rawtobr3` is a 32-bit program, so you need
to install the libc6-i386 package to avoid the "No such file or directory"
error when executing the program.
