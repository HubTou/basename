# Installation
pip install [pnu-basename](https://pypi.org/project/pnu-basename/)

# BASENAME(1)

## NAME
basename - return filename portion of pathname

## SYNOPSIS
**basename**
string \[suffix\]

**basename**
[-a]
[-s suffix]
[-z]
string \[...\]

## DESCRIPTION
The **basename** utility deletes any prefix ending with the last slash character
('/' under Unix-like Operating Systems or '\\' under Windows operating Systems)
present in string (after first stripping trailing slashes), and a suffix, if given.
The suffix is not stripped if it is identical to the remaining characters in string.
The resulting filename is written to the standard output.
A non-existent suffix is ignored.
If -a is specified, then every argument is treated as a string as if basename were
invoked with just one argument.
If -s is specified, then the suffix is taken as its argument, and all other arguments
are treated as a string.

### OPTIONS
Options | Use
------- | ---
-a\|--multiple|Support multiple arguments and treat each as a name
-s\|--suffix SUFFIX|Remove trailing SUFFIX. Implies -a
-z\|--zero|End each output line with NUL, not newline
--debug|Enable debug mode
--help\|-?|Print usage and a short help message and exit
--version|Print version and exit
--|Options processing terminator

## ENVIRONMENT
Contrary to the original [FreeBSD basename](https://www.freebsd.org/cgi/man.cgi?query=basename) command,
this version takes the [POSIXLY_CORRECT](https://www.freebsd.org/cgi/man.cgi?query=environ) environment variable into account,
disabling all the command's options except the options terminator (--).

## EXIT STATUS
The basename utility exits 0 on success, and >0 if an error occurs.

## SEE ALSO
[dirname(1)](https://www.freebsd.org/cgi/man.cgi?query=dirname),
[csh(1)](https://www.freebsd.org/cgi/man.cgi?query=csh),
[sh(1)](https://www.freebsd.org/cgi/man.cgi?query=sh),
[basename(3)](https://www.freebsd.org/cgi/man.cgi?query=basename&sektion=3)

## STANDARDS
The basename utility is expected to be IEEE Std 1003.2 (“[POSIX](https://en.wikipedia.org/wiki/POSIX).2”) compatible.

This version is fully compatible with the FreeBSD version (apart from the
invalid option error message). It also implements the [GNU coreutils](https://www.gnu.org/software/coreutils/) version
specific options (--multiple, --suffix, -z, --zero).

It tries to follow the [PEP 8](https://www.python.org/dev/peps/pep-0008/) style guide for [Python](https://www.python.org/) code.

## PORTABILITY
Tested OK under Windows (though with backslashes instead os slashes, of course).

## HISTORY
The basename utility first appeared in 4.4BSD.

This version was made for [The PNU project / PyNIX](https://github.com/HubTou/PNU)
in order to test the [b2bt](https://github.com/HubTou/b2bt) command.

## LICENSE
This utility is available under the [3-clause BSD license](https://opensource.org/licenses/BSD-3-Clause).

## AUTHORS
This version was written by [Hubert Tournier](https://github.com/HubTou).

The man page is derived from the [FreeBSD project's one](https://www.freebsd.org/cgi/man.cgi?query=basename).
