# DIRNAME(1)

## NAME
dirname - return directory portion of pathname

## SYNOPSIS
**dirname**
string \[...\]

**dirname**
[-z]
string \[...\]

## DESCRIPTION
The **dirname** utility deletes the filename portion, beginning with the last
slash '/' character to the end of string (after first stripping trailing
slashes), and writes the result to the standard output.

### OPTIONS
Options | Use
------- | ---
-z\|--zero|End each output line with NUL, not newline
--debug|Enable debug mode
--help\|-?|Print usage and a short help message and exit
--version|Print version and exit
--|Options processing terminator

## ENVIRONMENT
Contrary to the original [FreeBSD dirname](https://www.freebsd.org/cgi/man.cgi?query=dirname) command,
this version takes the [POSIXLY_CORRECT](https://www.freebsd.org/cgi/man.cgi?query=environ) environment variable
into account, disabling all the command's options except the options terminator (--).

## EXIT STATUS
The **dirname** utility exits 0 on success, and >0 if an error occurs.

## SEE ALSO
[basename(1)](https://github.com/HubTou/basename/blob/main/BASENAME.1.md)
[csh(1)](https://www.freebsd.org/cgi/man.cgi?query=csh),
[sh(1)](https://www.freebsd.org/cgi/man.cgi?query=sh),
[dirname(3)](https://www.freebsd.org/cgi/man.cgi?query=dirname&sektion=3)

## STANDARDS
The **dirname** utility is expected to be IEEE Std 1003.2 (“[POSIX](https://en.wikipedia.org/wiki/POSIX).2”) compatible.

This version is fully compatible with the FreeBSD version (apart from the help and error messages).
It also implements the [GNU coreutils](https://www.gnu.org/software/coreutils/) version specific options
( -z  --zero ).

It tries to follow the [PEP 8](https://www.python.org/dev/peps/pep-0008/) style guide for [Python](https://www.python.org/) code.

## PORTABILITY
Tested OK under Windows (though with backslashes instead os slashes, of course).

## HISTORY
The **dirname** utility first appeared in 4.4BSD.

This version was made for the [PNU project](https://github.com/HubTou/PNU)
in order to test the [b2bt](https://github.com/HubTou/b2bt) command.

## LICENSE
This utility is available under the [3-clause BSD license](https://opensource.org/licenses/BSD-3-Clause).

## AUTHORS
This version was written by [Hubert Tournier](https://github.com/HubTou).

The man page is derived from the [FreeBSD project's one](https://www.freebsd.org/cgi/man.cgi?query=dirname).
