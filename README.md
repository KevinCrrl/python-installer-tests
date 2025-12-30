# Python packages: Migration from python-pip to python-installer tests

[General Diff](https://github.com/KevinCrrl/blackarch/commit/68963a40ced8e2eb2d743b0965734be913ab1e4b)

## python-arpspoof test

* [Diff 1](https://github.com/KevinCrrl/blackarch/commit/0e6da90364e7aaf62f91bc84f3aac5a4e23fcc89)
* [Diff 2](https://github.com/KevinCrrl/blackarch/commit/eccbc76a80e816e19d60e996b89d8735fed616a2)

```bash
[Kevin@archlinux python-arpspoof]$ LC_ALL=C makepkg -si
==> Making package: python-arpspoof 1.1.2-5 (Mon Dec 29 14:22:17 2025)
==> Checking runtime dependencies...
==> Installing missing dependencies...
[sudo] password for Kevin: 
resolving dependencies...
looking for conflicting packages...

Packages (1) python-pythontoolskit-1.2.6-3

Total Installed Size:  0.34 MiB

:: Proceed with installation? [Y/n] y
(1/1) checking keys in keyring                                               [###########################################] 100%
(1/1) checking package integrity                                             [###########################################] 100%
(1/1) loading package files                                                  [###########################################] 100%
(1/1) checking for file conflicts                                            [###########################################] 100%
(1/1) checking available disk space                                          [###########################################] 100%
:: Processing package changes...
(1/1) installing python-pythontoolskit                                       [###########################################] 100%
:: Running post-transaction hooks...
(1/1) Arming ConditionNeedsUpdate...
==> Checking buildtime dependencies...
==> Retrieving sources...
  -> Downloading ArpSpoof-1.1.2.tar.gz...
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0   0     0   0     0     0     0  --:--:-- --:--:-- --:--:--     0
100 21195 100 21195   0     0 22546     0  --:--:-- --:--:-- --:--:-- 22546
==> Validating source files with sha512sums...
    ArpSpoof-1.1.2.tar.gz ... Passed
==> Extracting sources...
  -> Extracting ArpSpoof-1.1.2.tar.gz with bsdtar
==> Starting build()...
* Getting build dependencies for wheel...
running egg_info
writing ArpSpoof.egg-info/PKG-INFO
writing dependency_links to ArpSpoof.egg-info/dependency_links.txt
writing entry points to ArpSpoof.egg-info/entry_points.txt
writing requirements to ArpSpoof.egg-info/requires.txt
writing top-level names to ArpSpoof.egg-info/top_level.txt
reading manifest file 'ArpSpoof.egg-info/SOURCES.txt'
reading manifest template 'MANIFEST.in'
adding license file 'LICENSE.txt'
writing manifest file 'ArpSpoof.egg-info/SOURCES.txt'
* Building wheel...
running bdist_wheel
running build
running build_py
creating build/lib
copying ArpSpoof.py -> build/lib
installing to build/bdist.linux-x86_64/wheel
running install
running install_lib
creating build/bdist.linux-x86_64/wheel
copying build/lib/ArpSpoof.py -> build/bdist.linux-x86_64/wheel/.
running install_egg_info
running egg_info
writing ArpSpoof.egg-info/PKG-INFO
writing dependency_links to ArpSpoof.egg-info/dependency_links.txt
writing entry points to ArpSpoof.egg-info/entry_points.txt
writing requirements to ArpSpoof.egg-info/requires.txt
writing top-level names to ArpSpoof.egg-info/top_level.txt
reading manifest file 'ArpSpoof.egg-info/SOURCES.txt'
reading manifest template 'MANIFEST.in'
adding license file 'LICENSE.txt'
writing manifest file 'ArpSpoof.egg-info/SOURCES.txt'
Copying ArpSpoof.egg-info to build/bdist.linux-x86_64/wheel/./ArpSpoof-1.1.2-py3.13.egg-info
running install_scripts
creating build/bdist.linux-x86_64/wheel/arpspoof-1.1.2.dist-info/WHEEL
creating '/home/Kevin/blackarch/packages/python-arpspoof/src/ArpSpoof-1.1.2/dist/.tmp-tiyxxube/arpspoof-1.1.2-py3-none-any.whl' and adding 'build/bdist.linux-x86_64/wheel' to it
adding 'ArpSpoof.py'
adding 'arpspoof-1.1.2.dist-info/licenses/LICENSE.txt'
adding 'arpspoof-1.1.2.dist-info/METADATA'
adding 'arpspoof-1.1.2.dist-info/WHEEL'
adding 'arpspoof-1.1.2.dist-info/entry_points.txt'
adding 'arpspoof-1.1.2.dist-info/top_level.txt'
adding 'arpspoof-1.1.2.dist-info/RECORD'
removing build/bdist.linux-x86_64/wheel
Successfully built arpspoof-1.1.2-py3-none-any.whl
==> Entering fakeroot environment...
==> Starting package()...
==> Tidying install...
  -> Removing libtool files...
  -> Purging unreproducible ruby files...
  -> Removing static library files...
  -> Purging unwanted files...
  -> Stripping unneeded symbols from binaries and libraries...
  -> Compressing man and info pages...
==> Checking for packaging issues...
==> Creating package "python-arpspoof"...
  -> Generating .PKGINFO file...
  -> Generating .BUILDINFO file...
  -> Generating .MTREE file...
  -> Compressing package...
==> Leaving fakeroot environment.
==> Finished making: python-arpspoof 1.1.2-5 (Mon Dec 29 14:22:32 2025)
==> Installing package python-arpspoof with pacman -U...
[sudo] password for Kevin: 
loading packages...
resolving dependencies...
looking for conflicting packages...

Packages (1) python-arpspoof-1.1.2-5

Total Installed Size:  0.12 MiB

:: Proceed with installation? [Y/n] y
(1/1) checking keys in keyring                                               [###########################################] 100%
(1/1) checking package integrity                                             [###########################################] 100%
(1/1) loading package files                                                  [###########################################] 100%
(1/1) checking for file conflicts                                            [###########################################] 100%
(1/1) checking available disk space                                          [###########################################] 100%
:: Processing package changes...
(1/1) installing python-arpspoof                                             [###########################################] 100%
:: Running post-transaction hooks...
(1/1) Arming ConditionNeedsUpdate...
[Kevin@archlinux python-arpspoof]$ ArpSpoof

PythonToolsKit  Copyright (C) 2022, 2023  Maurice Lambert
This program comes with ABSOLUTELY NO WARRANTY.
This is free software, and you are welcome to redistribute it
under certain conditions.


ArpSpoof  Copyright (C) 2021, 2022  Maurice Lambert
This program comes with ABSOLUTELY NO WARRANTY.
This is free software, and you are welcome to redistribute it
under certain conditions.

usage: ArpSpoof [-h] [--interface INTERFACE] [--verbose] [--time TIME] [--semi] [--passive] gateway targets
ArpSpoof: error: the following arguments are required: gateway, targets
[Kevin@archlinux python-arpspoof]$ 
```
## python-gnureadline test

* [Diff](https://github.com/KevinCrrl/blackarch/commit/6ace7e33ae27b81387e4ebddfcf9ff92dfedf837)

```bash
[Kevin@archlinux python-gnureadline]$ LC_ALL=C makepkg -si
==> Making package: python-gnureadline 8.2.13-2 (Mon Dec 29 14:27:00 2025)
==> Checking runtime dependencies...
==> Checking buildtime dependencies...
==> Retrieving sources...
  -> Downloading gnureadline-8.2.13.tar.gz...
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0   0     0   0     0     0     0  --:--:-- --:--:-- --:--:--     0
100  3149k 100  3149k   0     0  2268k     0   0:00:01  0:00:01 --:--:--  3126k
==> Validating source files with sha512sums...
    gnureadline-8.2.13.tar.gz ... Passed
==> Extracting sources...
  -> Extracting gnureadline-8.2.13.tar.gz with bsdtar
==> Starting build()...
* Getting build dependencies for wheel...
/usr/lib/python3.13/site-packages/setuptools/dist.py:759: SetuptoolsDeprecationWarning: License classifiers are deprecated.
!!

        ********************************************************************************
        Please consider removing the following classifiers in favor of a SPDX license expression:

        License :: OSI Approved :: GNU General Public License v3 (GPLv3)

        See https://packaging.python.org/en/latest/guides/writing-pyproject-toml/#license for details.
        ********************************************************************************

!!
  self._finalize_license_expression()
running egg_info
writing gnureadline.egg-info/PKG-INFO
writing dependency_links to gnureadline.egg-info/dependency_links.txt
writing top-level names to gnureadline.egg-info/top_level.txt
reading manifest file 'gnureadline.egg-info/SOURCES.txt'
reading manifest template 'MANIFEST.in'
adding license file 'LICENSE'
writing manifest file 'gnureadline.egg-info/SOURCES.txt'
* Building wheel...

============ Building the readline library ============

readline-8.2/
readline-8.2/nls.c
readline-8.2/CHANGES
readline-8.2/histsearch.c
readline-8.2/readline.pc.in
readline-8.2/text.c
readline-8.2/chardefs.h
readline-8.2/histlib.h
readline-8.2/rlmbutil.h
readline-8.2/tilde.c
readline-8.2/colors.h
readline-8.2/vi_keymap.c
readline-8.2/keymaps.h
readline-8.2/histfile.c
readline-8.2/posixtime.h
readline-8.2/support/
readline-8.2/config.h.in
readline-8.2/util.c
readline-8.2/colors.c
readline-8.2/rltty.c
readline-8.2/posixjmp.h
readline-8.2/patchlevel
readline-8.2/rlwinsize.h
readline-8.2/misc.c
readline-8.2/funmap.c
readline-8.2/parse-colors.c
readline-8.2/signals.c
readline-8.2/configure
readline-8.2/INSTALL
readline-8.2/complete.c
readline-8.2/callback.c
readline-8.2/posixdir.h
readline-8.2/ansi_stdlib.h
readline-8.2/configure.ac
readline-8.2/xfree.c
readline-8.2/xmalloc.c
readline-8.2/undo.c
readline-8.2/rlconf.h
readline-8.2/shell.c
readline-8.2/CHANGELOG
readline-8.2/keymaps.c
readline-8.2/doc/
readline-8.2/readline.c
readline-8.2/mbutil.c
readline-8.2/COPYING
readline-8.2/display.c
readline-8.2/terminal.c
readline-8.2/parens.c
readline-8.2/README
readline-8.2/rlstdc.h
readline-8.2/posixselect.h
readline-8.2/history.c
readline-8.2/rltypedefs.h
readline-8.2/history.pc.in
readline-8.2/USAGE
readline-8.2/Makefile.in
readline-8.2/rlprivate.h
readline-8.2/aclocal.m4
readline-8.2/rlshell.h
readline-8.2/examples/
readline-8.2/shlib/
readline-8.2/histexpand.c
readline-8.2/compat.c
readline-8.2/readline.h
readline-8.2/tcap.h
readline-8.2/search.c
readline-8.2/macro.c
readline-8.2/rldefs.h
readline-8.2/MANIFEST
readline-8.2/tilde.h
readline-8.2/parse-colors.h
readline-8.2/vi_mode.c
readline-8.2/emacs_keymap.c
readline-8.2/isearch.c
readline-8.2/kill.c
readline-8.2/input.c
readline-8.2/NEWS
readline-8.2/m4/
readline-8.2/rltty.h
readline-8.2/bind.c
readline-8.2/posixstat.h
readline-8.2/history.h
readline-8.2/savestring.c
readline-8.2/xmalloc.h
readline-8.2/m4/codeset.m4
readline-8.2/shlib/Makefile.in
readline-8.2/examples/rlcat.c
readline-8.2/examples/excallback.c
readline-8.2/examples/rlwrap-0.30.tar.gz
readline-8.2/examples/rl-fgets.c
readline-8.2/examples/rlptytest.c
readline-8.2/examples/rlkeymaps.c
readline-8.2/examples/rl-callbacktest.c
readline-8.2/examples/rlbasic.c
readline-8.2/examples/readlinebuf.h
readline-8.2/examples/Inputrc
readline-8.2/examples/hist_erasedups.c
readline-8.2/examples/rl-timeout.c
readline-8.2/examples/Makefile.in
readline-8.2/examples/rltest.c
readline-8.2/examples/autoconf/
readline-8.2/examples/rl-test-timeout
readline-8.2/examples/manexamp.c
readline-8.2/examples/rlfe/
readline-8.2/examples/rlversion.c
readline-8.2/examples/rl.c
readline-8.2/examples/hist_purgecmd.c
readline-8.2/examples/rlevent.c
readline-8.2/examples/fileman.c
readline-8.2/examples/histexamp.c
readline-8.2/examples/rlfe/config.h.in
readline-8.2/examples/rlfe/configure
readline-8.2/examples/rlfe/pty.c
readline-8.2/examples/rlfe/rlfe.c
readline-8.2/examples/rlfe/ChangeLog
readline-8.2/examples/rlfe/README
readline-8.2/examples/rlfe/Makefile.in
readline-8.2/examples/rlfe/os.h
readline-8.2/examples/rlfe/extern.h
readline-8.2/examples/rlfe/screen.h
readline-8.2/examples/rlfe/configure.in
readline-8.2/examples/autoconf/wi_LIB_READLINE
readline-8.2/examples/autoconf/RL_LIB_READLINE_VERSION
readline-8.2/examples/autoconf/BASH_CHECK_LIB_TERMCAP
readline-8.2/doc/rluserman.pdf
readline-8.2/doc/texinfo.tex
readline-8.2/doc/readline.0
readline-8.2/doc/rluser.texi
readline-8.2/doc/readline.dvi
readline-8.2/doc/fdl.texi
readline-8.2/doc/hsuser.texi
readline-8.2/doc/rluserman.info
readline-8.2/doc/rltech.texi
readline-8.2/doc/rluserman.dvi
readline-8.2/doc/history.ps
readline-8.2/doc/readline_3.ps
readline-8.2/doc/rlman.texi
readline-8.2/doc/texi2html
readline-8.2/doc/readline.ps
readline-8.2/doc/history_3.ps
readline-8.2/doc/readline.info
readline-8.2/doc/readline.pdf
readline-8.2/doc/Makefile.in
readline-8.2/doc/readline.html
readline-8.2/doc/history.pdf
readline-8.2/doc/version.texi
readline-8.2/doc/history.3
readline-8.2/doc/history.texi
readline-8.2/doc/texi2dvi
readline-8.2/doc/hstech.texi
readline-8.2/doc/rluserman.texi
readline-8.2/doc/history.0
readline-8.2/doc/history.info
readline-8.2/doc/history.html
readline-8.2/doc/readline.3
readline-8.2/doc/history.dvi
readline-8.2/doc/rluserman.ps
readline-8.2/doc/rluserman.html
readline-8.2/support/config.sub
readline-8.2/support/mkinstalldirs
readline-8.2/support/shlib-install
readline-8.2/support/mkdist
readline-8.2/support/mkdirs
readline-8.2/support/install.sh
readline-8.2/support/config.rpath
readline-8.2/support/shobj-conf
readline-8.2/support/config.guess
readline-8.2/support/wcwidth.c
patching file nls.c
patching file patchlevel
patching file display.c
patching file patchlevel
patching file colors.c
patching file patchlevel
patching file input.c
patching file patchlevel
patching file callback.c
patching file patchlevel
patching file input.c
Hunk #1 succeeded at 805 (offset -7 lines).
Hunk #2 succeeded at 816 (offset -7 lines).
Hunk #3 succeeded at 895 (offset -7 lines).
Hunk #4 succeeded at 938 (offset -7 lines).
patching file patchlevel
patching file display.c
Hunk #1 succeeded at 3339 (offset -3 lines).
patching file patchlevel
patching file text.c
patching file bind.c
patching file rltty.c
patching file patchlevel
patching file complete.c
patching file patchlevel
patching file complete.c
patching file patchlevel
patching file bind.c
patching file patchlevel
patching file readline.c
patching file isearch.c
patching file patchlevel
patching file text.c
patching file patchlevel
checking build system type... x86_64-pc-linux-gnu
checking host system type... x86_64-pc-linux-gnu

Beginning configuration for readline-8.2 for x86_64-pc-linux-gnu

checking whether make sets $(MAKE)... yes
checking for gcc... gcc
checking whether the C compiler works... yes
checking for C compiler default output file name... a.out
checking for suffix of executables... 
checking whether we are cross compiling... no
checking for suffix of object files... o
checking whether the compiler supports GNU C... yes
checking whether gcc accepts -g... yes
checking for gcc option to enable C11 features... none needed
checking for stdio.h... yes
checking for stdlib.h... yes
checking for string.h... yes
checking for inttypes.h... yes
checking for stdint.h... yes
checking for strings.h... yes
checking for sys/stat.h... yes
checking for sys/types.h... yes
checking for unistd.h... yes
checking for wchar.h... yes
checking for minix/config.h... no
checking whether it is safe to define __EXTENSIONS__... yes
checking whether _XOPEN_SOURCE should be defined... no
checking how to run the C preprocessor... gcc -E
checking for grep that handles long lines and -e... /usr/bin/grep
checking for egrep... /usr/bin/grep -E
checking whether gcc needs -traditional... no
checking for a BSD-compatible install... /usr/bin/install -c
checking for ar... ar
checking for ranlib... ranlib
checking for an ANSI C-conforming const... yes
checking for inline... inline
checking whether char is unsigned... no
checking for working volatile... yes
checking for size_t... yes
checking for ssize_t... yes
checking whether stat file-mode macros are broken... no
checking for dirent.h that defines DIR... yes
checking for library containing opendir... none required
checking for fcntl... yes
checking for gettimeofday... yes
checking for kill... yes
checking for lstat... yes
checking for pselect... yes
checking for readlink... yes
checking for select... yes
checking for setitimer... yes
checking for fnmatch... yes
checking for memmove... yes
checking for putenv... yes
checking for setenv... yes
checking for setlocale... yes
checking for strcasecmp... yes
checking for strpbrk... yes
checking for sysconf... yes
checking for tcgetattr... yes
checking for vsnprintf... yes
checking for isascii... yes
checking for isxdigit... yes
checking for getpwent... yes
checking for getpwnam... yes
checking for getpwuid... yes
checking for uid_t in sys/types.h... yes
checking for working chown... yes
checking for working strcoll... yes
checking for fcntl.h... yes
checking for unistd.h... (cached) yes
checking for stdlib.h... (cached) yes
checking for varargs.h... no
checking for stdarg.h... yes
checking for stdbool.h... yes
checking for string.h... (cached) yes
checking for strings.h... (cached) yes
checking for limits.h... yes
checking for locale.h... yes
checking for pwd.h... yes
checking for memory.h... yes
checking for termcap.h... yes
checking for termios.h... yes
checking for termio.h... no
checking for sys/ioctl.h... yes
checking for sys/pte.h... no
checking for sys/stream.h... no
checking for sys/select.h... yes
checking for sys/time.h... yes
checking for sys/file.h... yes
checking for sys/ptem.h... no
checking for special C compiler options needed for large files... no
checking for _FILE_OFFSET_BITS value needed for large files... no
checking for type of signal functions... posix
checking if signal handlers must be reinstalled when invoked... yes
checking for presence of POSIX-style sigsetjmp/siglongjmp... present
checking for lstat... yes
checking whether or not strcoll and strcmp differ... no
checking whether getpw functions are declared in pwd.h... yes
checking whether termios.h defines TIOCGWINSZ... no
checking whether sys/ioctl.h defines TIOCGWINSZ... yes
checking for inttypes.h... (cached) yes
checking for sig_atomic_t in signal.h... yes
checking for TIOCSTAT in sys/ioctl.h... no
checking for FIONREAD in sys/ioctl.h... yes
checking for speed_t in sys/types.h... no
checking for struct winsize in sys/ioctl.h and termios.h... sys/ioctl.h
checking for struct dirent.d_ino... checking for struct dirent.d_ino... yes
yes
checking for struct dirent.d_fileno... checking for struct dirent.d_fileno... yes
yes
checking for struct timeval in sys/time.h and time.h... yes
checking for libaudit.h... yes
checking for gcc options needed to detect all undeclared functions... none needed
checking whether AUDIT_USER_TTY is declared... yes
checking for tgetent... no
checking for tgetent in -ltermcap... no
checking for tgetent in -ltinfo... yes
checking which library has the termcap functions... using libtinfo
checking for nl_langinfo and CODESET... yes
checking for wctype.h... yes
checking for wchar.h... (cached) yes
checking for langinfo.h... yes
checking for mbstr.h... no
checking for mbrlen... yes
checking for mbscasecmp... no
checking for mbscmp... no
checking for mbsnrtowcs... yes
checking for mbsrtowcs... yes
checking for mbschr... no
checking for wcrtomb... yes
checking for wcscoll... yes
checking for wcsdup... yes
checking for wcwidth... yes
checking for wctype... yes
checking for wcswidth... yes
checking whether mbrtowc and mbstate_t are properly declared... yes
checking for iswlower... yes
checking for iswupper... yes
checking for towlower... yes
checking for towupper... yes
checking for iswctype... yes
checking for wchar_t in wchar.h... yes
checking for wctype_t in wctype.h... yes
checking for wint_t in wctype.h... yes
checking for wcwidth broken with unicode combining characters... yes
checking size of wchar_t... 4
checking configuration for building shared libraries... supported
configure: creating ./config.status
config.status: creating Makefile
config.status: creating doc/Makefile
config.status: creating examples/Makefile
config.status: creating shlib/Makefile
config.status: creating readline.pc
config.status: creating history.pc
config.status: creating config.h
config.status: executing stamp-h commands
rm -f readline.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  readline.c
rm -f vi_mode.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  vi_mode.c
rm -f funmap.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  funmap.c
rm -f keymaps.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  keymaps.c
rm -f parens.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  parens.c
rm -f search.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  search.c
rm -f rltty.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  rltty.c
rm -f complete.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  complete.c
rm -f bind.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  bind.c
rm -f isearch.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  isearch.c
rm -f display.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  display.c
rm -f signals.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  signals.c
rm -f util.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  util.c
rm -f kill.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  kill.c
rm -f undo.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  undo.c
rm -f macro.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  macro.c
rm -f input.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  input.c
rm -f callback.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  callback.c
rm -f terminal.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  terminal.c
rm -f text.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  text.c
rm -f nls.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  nls.c
rm -f misc.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  misc.c
rm -f history.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  history.c
rm -f histexpand.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  histexpand.c
rm -f histfile.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  histfile.c
rm -f histsearch.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  histsearch.c
rm -f shell.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  shell.c
rm -f mbutil.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  mbutil.c
rm -f tilde.o
gcc  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  -DREADLINE_LIBRARY -c ./tilde.c
rm -f colors.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  colors.c
rm -f parse-colors.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  parse-colors.c
rm -f xmalloc.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  xmalloc.c
rm -f xfree.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  xfree.c
rm -f compat.o
gcc -c  -DHAVE_CONFIG_H   -I. -I. -DNEED_EXTERN_PC -fPIC -DRL_LIBRARY_VERSION='"8.2"' -DBRACKETED_PASTE_DEFAULT=1 -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions         -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security         -fstack-clash-protection -fcf-protection         -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto  compat.c
rm -f libreadline.a
ar cr libreadline.a readline.o vi_mode.o funmap.o keymaps.o parens.o search.o rltty.o complete.o bind.o isearch.o display.o signals.o util.o kill.o undo.o macro.o input.o callback.o terminal.o text.o nls.o misc.o history.o histexpand.o histfile.o histsearch.o shell.o mbutil.o tilde.o colors.o parse-colors.o xmalloc.o xfree.o compat.o
test -n "ranlib" && ranlib libreadline.a
rm -f libhistory.a
ar cr libhistory.a history.o histexpand.o histfile.o histsearch.o shell.o mbutil.o xmalloc.o xfree.o
test -n "ranlib" && ranlib libhistory.a

============ Building the readline extension module ============

/usr/lib/python3.13/site-packages/setuptools/dist.py:759: SetuptoolsDeprecationWarning: License classifiers are deprecated.
!!

        ********************************************************************************
        Please consider removing the following classifiers in favor of a SPDX license expression:

        License :: OSI Approved :: GNU General Public License v3 (GPLv3)

        See https://packaging.python.org/en/latest/guides/writing-pyproject-toml/#license for details.
        ********************************************************************************

!!
  self._finalize_license_expression()
running bdist_wheel
running build
running build_py
creating build/lib.linux-x86_64-cpython-313
copying readline.py -> build/lib.linux-x86_64-cpython-313
copying override_readline.py -> build/lib.linux-x86_64-cpython-313
running egg_info
writing gnureadline.egg-info/PKG-INFO
writing dependency_links to gnureadline.egg-info/dependency_links.txt
writing top-level names to gnureadline.egg-info/top_level.txt
reading manifest file 'gnureadline.egg-info/SOURCES.txt'
reading manifest template 'MANIFEST.in'
adding license file 'LICENSE'
writing manifest file 'gnureadline.egg-info/SOURCES.txt'
running build_ext
building 'gnureadline' extension
creating build/temp.linux-x86_64-cpython-313/Modules/3.x
gcc -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security -fstack-clash-protection -fcf-protection -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto -fPIC -DHAVE_RL_APPEND_HISTORY -DHAVE_RL_CALLBACK -DHAVE_RL_CATCH_SIGNAL -DHAVE_RL_COMPDISP_FUNC_T -DHAVE_RL_COMPLETION_APPEND_CHARACTER -DHAVE_RL_COMPLETION_DISPLAY_MATCHES_HOOK -DHAVE_RL_COMPLETION_MATCHES -DHAVE_RL_COMPLETION_SUPPRESS_APPEND -DHAVE_RL_PRE_INPUT_HOOK -DHAVE_RL_RESIZE_TERMINAL -DREADLINE_LIBRARY -I/usr/include/python3.13 -c Modules/3.x/readline.c -o build/temp.linux-x86_64-cpython-313/Modules/3.x/readline.o
gcc -shared -Wl,-O1 -Wl,--sort-common -Wl,--as-needed -Wl,-z,relro -Wl,-z,now -Wl,-z,pack-relative-relocs -flto=auto -Wl,-O1 -Wl,--sort-common -Wl,--as-needed -Wl,-z,relro -Wl,-z,now -Wl,-z,pack-relative-relocs -flto=auto -Wl,-O1 -Wl,--sort-common -Wl,--as-needed -Wl,-z,relro -Wl,-z,now -Wl,-z,pack-relative-relocs -flto=auto -march=x86-64 -mtune=generic -O2 -pipe -fno-plt -fexceptions -Wp,-D_FORTIFY_SOURCE=3 -Wformat -Werror=format-security -fstack-clash-protection -fcf-protection -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer -flto=auto build/temp.linux-x86_64-cpython-313/Modules/3.x/readline.o readline/libreadline.a readline/libhistory.a -L/usr/lib -lncurses -o build/lib.linux-x86_64-cpython-313/gnureadline.cpython-313-x86_64-linux-gnu.so
installing to build/bdist.linux-x86_64/wheel
running install
running install_lib
creating build/bdist.linux-x86_64/wheel
copying build/lib.linux-x86_64-cpython-313/readline.py -> build/bdist.linux-x86_64/wheel/.
copying build/lib.linux-x86_64-cpython-313/gnureadline.cpython-313-x86_64-linux-gnu.so -> build/bdist.linux-x86_64/wheel/.
copying build/lib.linux-x86_64-cpython-313/override_readline.py -> build/bdist.linux-x86_64/wheel/.
running install_egg_info
Copying gnureadline.egg-info to build/bdist.linux-x86_64/wheel/./gnureadline-8.2.13-py3.13.egg-info
running install_scripts
creating build/bdist.linux-x86_64/wheel/gnureadline-8.2.13.dist-info/WHEEL
creating '/home/Kevin/blackarch/packages/python-gnureadline/src/gnureadline-8.2.13/dist/.tmp-zk3kjcej/gnureadline-8.2.13-cp313-cp313-linux_x86_64.whl' and adding 'build/bdist.linux-x86_64/wheel' to it
adding 'gnureadline.cpython-313-x86_64-linux-gnu.so'
adding 'override_readline.py'
adding 'readline.py'
adding 'gnureadline-8.2.13.dist-info/licenses/LICENSE'
adding 'gnureadline-8.2.13.dist-info/METADATA'
adding 'gnureadline-8.2.13.dist-info/WHEEL'
adding 'gnureadline-8.2.13.dist-info/top_level.txt'
adding 'gnureadline-8.2.13.dist-info/RECORD'
removing build/bdist.linux-x86_64/wheel
Successfully built gnureadline-8.2.13-cp313-cp313-linux_x86_64.whl
==> Entering fakeroot environment...
==> Starting package()...
==> Tidying install...
  -> Removing libtool files...
  -> Purging unreproducible ruby files...
  -> Removing static library files...
  -> Purging unwanted files...
  -> Removing empty directories...
  -> Stripping unneeded symbols from binaries and libraries...
  -> Compressing man and info pages...
==> Checking for packaging issues...
==> Creating package "python-gnureadline"...
  -> Generating .PKGINFO file...
  -> Generating .BUILDINFO file...
  -> Generating .MTREE file...
  -> Compressing package...
==> Leaving fakeroot environment.
==> Finished making: python-gnureadline 8.2.13-2 (Mon Dec 29 14:27:26 2025)
==> Installing package python-gnureadline with pacman -U...
[sudo] password for Kevin: 
loading packages...
resolving dependencies...
looking for conflicting packages...

Packages (1) python-gnureadline-8.2.13-2

Total Installed Size:  0.42 MiB
Net Upgrade Size:      0.01 MiB

:: Proceed with installation? [Y/n] y
(1/1) checking keys in keyring                                               [###########################################] 100%
(1/1) checking package integrity                                             [###########################################] 100%
(1/1) loading package files                                                  [###########################################] 100%
(1/1) checking for file conflicts                                            [###########################################] 100%
(1/1) checking available disk space                                          [###########################################] 100%
:: Processing package changes...
(1/1) upgrading python-gnureadline                                           [###########################################] 100%
:: Running post-transaction hooks...
(1/1) Arming ConditionNeedsUpdate...
[Kevin@archlinux python-gnureadline]$ python
Python 3.13.11 (main, Dec  7 2025, 13:01:45) [GCC 15.2.1 20251112] on linux
Type "help", "copyright", "credits" or "license" for more information.
Ctrl click to launch VS Code Native REPL
>>> try:
...     import gnureadline as readline
... except ImportError:
...     print("Error")
... 
>>> 
[Kevin@archlinux python-gnureadline]$ 
```
## pyinstaller test

* [Diff](https://github.com/KevinCrrl/blackarch/commit/686a1f9acd22881857677b6a5c86f953db13748c)

```bash
[Kevin@archlinux pyinstaller]$ LC_ALL=C makepkg -si
==> Making package: pyinstaller 2:6.17.0-2 (Mon Dec 29 14:42:59 2025)
==> Checking runtime dependencies...
==> Checking buildtime dependencies...
==> Installing missing dependencies...
[sudo] password for Kevin: 
resolving dependencies...
looking for conflicting packages...

Packages (5) python-editables-0.5-5  python-pathspec-0.12.1-3  python-pluggy-1.6.0-1  python-trove-classifiers-2025.12.1.14-1
             python-hatchling-1.28.0-1

Total Download Size:   0.27 MiB
Total Installed Size:  1.53 MiB

:: Proceed with installation? [Y/n] y
:: Retrieving packages...
 python-trove-classifiers-2025.12.1.14-1-any      19.9 KiB  20.3 KiB/s 00:01 [###########################################] 100%
 python-editables-0.5-5-any                       10.9 KiB  11.1 KiB/s 00:01 [###########################################] 100%
 python-pluggy-1.6.0-1-any                        44.6 KiB  37.7 KiB/s 00:01 [###########################################] 100%
 python-pathspec-0.12.1-3-any                     47.4 KiB  40.1 KiB/s 00:01 [###########################################] 100%
 python-hatchling-1.28.0-1-any                   155.9 KiB  97.5 KiB/s 00:02 [###########################################] 100%
 Total (5/5)                                     278.7 KiB   154 KiB/s 00:02 [###########################################] 100%
(5/5) checking keys in keyring                                               [###########################################] 100%
(5/5) checking package integrity                                             [###########################################] 100%
(5/5) loading package files                                                  [###########################################] 100%
(5/5) checking for file conflicts                                            [###########################################] 100%
(5/5) checking available disk space                                          [###########################################] 100%
:: Processing package changes...
(1/5) installing python-editables                                            [###########################################] 100%
(2/5) installing python-pathspec                                             [###########################################] 100%
(3/5) installing python-pluggy                                               [###########################################] 100%
(4/5) installing python-trove-classifiers                                    [###########################################] 100%
(5/5) installing python-hatchling                                            [###########################################] 100%
:: Running post-transaction hooks...
(1/1) Arming ConditionNeedsUpdate...
==> Retrieving sources...
  -> Found pyinstaller-6.17.0.tar.gz
  -> Found fortify-source-fix.patch
==> Validating source files with sha512sums...
    pyinstaller-6.17.0.tar.gz ... Passed
    fortify-source-fix.patch ... Passed
==> Extracting sources...
  -> Extracting pyinstaller-6.17.0.tar.gz with bsdtar
==> Starting prepare()...
patching file bootloader/wscript
Hunk #1 succeeded at 546 (offset 28 lines).
==> Removing existing $pkgdir/ directory...
==> Starting build()...
* Getting build dependencies for wheel...
* Building wheel...
No precompiled bootloader found or compile forced. Trying to compile the bootloader for you ...
Setting top to                           : /home/Kevin/blackarch/packages/pyinstaller/src/pyinstaller-6.17.0/bootloader 
Setting out to                           : /home/Kevin/blackarch/packages/pyinstaller/src/pyinstaller-6.17.0/bootloader/build 
Python Version                           : 3.13.11 (main, Dec  7 2025, 13:01:45) [GCC 15.2.1 20251112] 
MSVC target(s)                           : not found 
Checking for 'gcc' (C compiler)          : /usr/bin/gcc 
Checking size of pointer                 : 8 
Platform                                 : Linux-64bit-intel detected based on compiler 
Checking for compiler flags -m64         : yes 
Checking for linker flags -m64           : yes 
Checking for compiler flags -Wno-error=unused-but-set-variable : yes 
Checking for header semaphore.h                                : yes 
Using semaphore API                                            : posix 
Checking for library dl                                        : yes 
Checking for library pthread                                   : yes 
Checking for library m                                         : yes 
Checking for library z                                         : yes 
Build tests                                                    : disabled 
Checking for header stdbool.h                                  : yes 
Checking for function unsetenv                                 : yes 
Checking for function mkdtemp                                  : yes 
Checking for function dirname                                  : yes 
Checking for function basename                                 : yes 
Checking for function wcsdup                                   : yes 
Checking for linker flags -Wl,--as-needed                      : yes 
Checking for program 'strip'                                   : /usr/bin/strip 
'configure' finished successfully (2.820s)
'all' finished successfully (0.000s)
'distclean' finished successfully (0.003s)
Setting top to                           : /home/Kevin/blackarch/packages/pyinstaller/src/pyinstaller-6.17.0/bootloader 
Setting out to                           : /home/Kevin/blackarch/packages/pyinstaller/src/pyinstaller-6.17.0/bootloader/build 
Python Version                           : 3.13.11 (main, Dec  7 2025, 13:01:45) [GCC 15.2.1 20251112] 
MSVC target(s)                           : not found 
Checking for 'gcc' (C compiler)          : /usr/bin/gcc 
Checking size of pointer                 : 8 
Platform                                 : Linux-64bit-intel detected based on compiler 
Checking for compiler flags -m64         : yes 
Checking for linker flags -m64           : yes 
Checking for compiler flags -Wno-error=unused-but-set-variable : yes 
Checking for header semaphore.h                                : yes 
Using semaphore API                                            : posix 
Checking for library dl                                        : yes 
Checking for library pthread                                   : yes 
Checking for library m                                         : yes 
Checking for library z                                         : yes 
Build tests                                                    : disabled 
Checking for header stdbool.h                                  : yes 
Checking for function unsetenv                                 : yes 
Checking for function mkdtemp                                  : yes 
Checking for function dirname                                  : yes 
Checking for function basename                                 : yes 
Checking for function wcsdup                                   : yes 
Checking for linker flags -Wl,--as-needed                      : yes 
Checking for program 'strip'                                   : /usr/bin/strip 
'configure' finished successfully (2.222s)
'make_all' finished successfully (0.006s)
Waf: Entering directory `/home/Kevin/blackarch/packages/pyinstaller/src/pyinstaller-6.17.0/bootloader/build/debug'
[ 1/23] Compiling src/pyi_python.c
[ 2/23] Compiling src/pyi_global_win32.c
[ 3/23] Compiling src/pyi_dylib_python.c
[ 4/23] Compiling src/pyi_apple_events.c
[ 5/23] Compiling src/pyi_pyconfig_pep741.c
[ 6/23] Compiling src/pyi_multipkg.c
[ 7/23] Compiling src/pyi_dylib_tcltk.c
[ 8/23] Compiling src/pyi_utils_posix.c
[ 9/23] Compiling src/pyi_launch.c
[10/23] Compiling src/pyi_splash.c
[11/23] Compiling src/pyi_pyconfig.c
[12/23] Compiling src/pyi_utils_win32_low_level.c
[13/23] Compiling src/pyi_utils.c
[14/23] Compiling src/pyi_main.c
[15/23] Compiling src/pyi_exception_dialog.c
[16/23] Compiling src/pyi_utils_win32.c
[17/23] Compiling src/pyi_path.c
[18/23] Compiling src/pyi_pyconfig_pep587.c
[19/23] Compiling src/pyi_global_posix.c
[20/23] Compiling src/pyi_archive.c
[21/23] Compiling src/main.c
[22/23] Linking build/debug/run_d
[23/23] Stripping binary build/debug/run_d
Waf: Leaving directory `/home/Kevin/blackarch/packages/pyinstaller/src/pyinstaller-6.17.0/bootloader/build/debug'
'build_debug' finished successfully (2.937s)
Waf: Entering directory `/home/Kevin/blackarch/packages/pyinstaller/src/pyinstaller-6.17.0/bootloader/build/release'
[ 1/23] Compiling src/pyi_python.c
[ 2/23] Compiling src/pyi_global_win32.c
[ 3/23] Compiling src/pyi_dylib_python.c
[ 4/23] Compiling src/pyi_apple_events.c
[ 5/23] Compiling src/pyi_pyconfig_pep741.c
[ 6/23] Compiling src/pyi_multipkg.c
[ 7/23] Compiling src/pyi_dylib_tcltk.c
[ 8/23] Compiling src/pyi_utils_posix.c
[ 9/23] Compiling src/pyi_launch.c
[10/23] Compiling src/pyi_splash.c
[11/23] Compiling src/pyi_pyconfig_pep587.c
[12/23] Compiling src/pyi_pyconfig.c
[13/23] Compiling src/pyi_archive.c
[14/23] Compiling src/pyi_path.c
[15/23] Compiling src/pyi_utils.c
[16/23] Compiling src/pyi_exception_dialog.c
[17/23] Compiling src/pyi_utils_win32.c
[18/23] Compiling src/pyi_global_posix.c
[19/23] Compiling src/pyi_utils_win32_low_level.c
[20/23] Compiling src/pyi_main.c
[21/23] Compiling src/main.c
[22/23] Linking build/release/run
[23/23] Stripping binary build/release/run
Waf: Leaving directory `/home/Kevin/blackarch/packages/pyinstaller/src/pyinstaller-6.17.0/bootloader/build/release'
'build_release' finished successfully (2.623s)
Waf: Entering directory `/home/Kevin/blackarch/packages/pyinstaller/src/pyinstaller-6.17.0/bootloader/build/debug'
+ install /home/Kevin/blackarch/packages/pyinstaller/src/pyinstaller-6.17.0/PyInstaller/bootloader/Linux-64bit-intel/run_d (from build/debug/run_d)
Waf: Leaving directory `/home/Kevin/blackarch/packages/pyinstaller/src/pyinstaller-6.17.0/bootloader/build/debug'
'install_debug' finished successfully (0.025s)
Waf: Entering directory `/home/Kevin/blackarch/packages/pyinstaller/src/pyinstaller-6.17.0/bootloader/build/release'
+ install /home/Kevin/blackarch/packages/pyinstaller/src/pyinstaller-6.17.0/PyInstaller/bootloader/Linux-64bit-intel/run (from build/release/run)
Waf: Leaving directory `/home/Kevin/blackarch/packages/pyinstaller/src/pyinstaller-6.17.0/bootloader/build/release'
'install_release' finished successfully (0.023s)
Successfully built pyinstaller-6.17.0-py3-none-any.whl
==> Entering fakeroot environment...
==> Starting package()...
==> Tidying install...
  -> Removing libtool files...
  -> Purging unreproducible ruby files...
  -> Removing static library files...
  -> Purging unwanted files...
  -> Removing empty directories...
  -> Copying source files needed for debug symbols...
  -> Compressing man and info pages...
==> Checking for packaging issues...
==> Creating package "pyinstaller"...
  -> Generating .PKGINFO file...
  -> Generating .BUILDINFO file...
  -> Generating .MTREE file...
  -> Compressing package...
==> Leaving fakeroot environment.
==> Finished making: pyinstaller 2:6.17.0-2 (Mon Dec 29 14:43:40 2025)
==> Installing package pyinstaller with pacman -U...
[sudo] password for Kevin: 
loading packages...
resolving dependencies...
looking for conflicting packages...

Packages (1) pyinstaller-2:6.17.0-2

Total Installed Size:  4.56 MiB
Net Upgrade Size:      2.41 MiB

:: Proceed with installation? [Y/n] y
(1/1) checking keys in keyring                                               [###########################################] 100%
(1/1) checking package integrity                                             [###########################################] 100%
(1/1) loading package files                                                  [###########################################] 100%
(1/1) checking for file conflicts                                            [###########################################] 100%
(1/1) checking available disk space                                          [###########################################] 100%
:: Processing package changes...
(1/1) upgrading pyinstaller                                                  [###########################################] 100%
:: Running post-transaction hooks...
(1/1) Arming ConditionNeedsUpdate...
[Kevin@archlinux pyinstaller]$ pyinstaller --version
6.17.0
[Kevin@archlinux pyinstaller]$ 
```
## python-torf test

* [Diff](https://github.com/KevinCrrl/blackarch/commit/480af53c5735f7b34a9d8886306efc032f537ad5)

```bash
[Kevin@archlinux python-torf]$ LC_ALL=C makepkg -si
==> Making package: python-torf 4.3.0-2 (Tue Dec 30 13:50:16 2025)
==> Checking runtime dependencies...
==> Checking buildtime dependencies...
==> Retrieving sources...
  -> Downloading torf-4.3.0.tar.gz...
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0   0     0   0     0     0     0  --:--:--  0:00:01 --:--:--     0
100 107454 100 107454   0     0 62030     0   0:00:01  0:00:01 --:--:-- 62030
==> Validating source files with sha512sums...
    torf-4.3.0.tar.gz ... Passed
==> Extracting sources...
  -> Extracting torf-4.3.0.tar.gz with bsdtar
==> Starting build()...
* Getting build dependencies for wheel...
/usr/lib/python3.13/site-packages/setuptools/config/_apply_pyprojecttoml.py:82: SetuptoolsDeprecationWarning: `project.license` as a TOML table is deprecated
!!

        ********************************************************************************
        Please use a simple string containing a SPDX expression for `project.license`. You can also use `project.license-files`. (Both options available on setuptools>=77.0.0).

        By 2026-Feb-18, you need to update your project and remove deprecated calls
        or your builds will no longer be supported.

        See https://packaging.python.org/en/latest/guides/writing-pyproject-toml/#license for details.
        ********************************************************************************

!!
  corresp(dist, value, root_dir)
/usr/lib/python3.13/site-packages/setuptools/config/_apply_pyprojecttoml.py:61: SetuptoolsDeprecationWarning: License classifiers are deprecated.
!!

        ********************************************************************************
        Please consider removing the following classifiers in favor of a SPDX license expression:

        License :: OSI Approved :: GNU General Public License v3 or later (GPLv3+)

        See https://packaging.python.org/en/latest/guides/writing-pyproject-toml/#license for details.
        ********************************************************************************

!!
  dist._finalize_license_expression()
/usr/lib/python3.13/site-packages/setuptools/dist.py:759: SetuptoolsDeprecationWarning: License classifiers are deprecated.
!!

        ********************************************************************************
        Please consider removing the following classifiers in favor of a SPDX license expression:

        License :: OSI Approved :: GNU General Public License v3 or later (GPLv3+)

        See https://packaging.python.org/en/latest/guides/writing-pyproject-toml/#license for details.
        ********************************************************************************

!!
  self._finalize_license_expression()
running egg_info
writing torf.egg-info/PKG-INFO
writing dependency_links to torf.egg-info/dependency_links.txt
writing requirements to torf.egg-info/requires.txt
writing top-level names to torf.egg-info/top_level.txt
reading manifest file 'torf.egg-info/SOURCES.txt'
adding license file 'LICENSE'
writing manifest file 'torf.egg-info/SOURCES.txt'
* Building wheel...
/usr/lib/python3.13/site-packages/setuptools/config/_apply_pyprojecttoml.py:82: SetuptoolsDeprecationWarning: `project.license` as a TOML table is deprecated
!!

        ********************************************************************************
        Please use a simple string containing a SPDX expression for `project.license`. You can also use `project.license-files`. (Both options available on setuptools>=77.0.0).

        By 2026-Feb-18, you need to update your project and remove deprecated calls
        or your builds will no longer be supported.

        See https://packaging.python.org/en/latest/guides/writing-pyproject-toml/#license for details.
        ********************************************************************************

!!
  corresp(dist, value, root_dir)
/usr/lib/python3.13/site-packages/setuptools/config/_apply_pyprojecttoml.py:61: SetuptoolsDeprecationWarning: License classifiers are deprecated.
!!

        ********************************************************************************
        Please consider removing the following classifiers in favor of a SPDX license expression:

        License :: OSI Approved :: GNU General Public License v3 or later (GPLv3+)

        See https://packaging.python.org/en/latest/guides/writing-pyproject-toml/#license for details.
        ********************************************************************************

!!
  dist._finalize_license_expression()
/usr/lib/python3.13/site-packages/setuptools/dist.py:759: SetuptoolsDeprecationWarning: License classifiers are deprecated.
!!

        ********************************************************************************
        Please consider removing the following classifiers in favor of a SPDX license expression:

        License :: OSI Approved :: GNU General Public License v3 or later (GPLv3+)

        See https://packaging.python.org/en/latest/guides/writing-pyproject-toml/#license for details.
        ********************************************************************************

!!
  self._finalize_license_expression()
running bdist_wheel
running build
running build_py
creating build/lib/torf
copying torf/_errors.py -> build/lib/torf
copying torf/_utils.py -> build/lib/torf
copying torf/_reuse.py -> build/lib/torf
copying torf/_torrent.py -> build/lib/torf
copying torf/_generate.py -> build/lib/torf
copying torf/_magnet.py -> build/lib/torf
copying torf/__init__.py -> build/lib/torf
copying torf/_stream.py -> build/lib/torf
running egg_info
writing torf.egg-info/PKG-INFO
writing dependency_links to torf.egg-info/dependency_links.txt
writing requirements to torf.egg-info/requires.txt
writing top-level names to torf.egg-info/top_level.txt
reading manifest file 'torf.egg-info/SOURCES.txt'
adding license file 'LICENSE'
writing manifest file 'torf.egg-info/SOURCES.txt'
copying torf/__init__.pyi -> build/lib/torf
copying torf/_errors.pyi -> build/lib/torf
copying torf/_magnet.pyi -> build/lib/torf
copying torf/_stream.pyi -> build/lib/torf
copying torf/_torrent.pyi -> build/lib/torf
copying torf/_utils.pyi -> build/lib/torf
copying torf/py.typed -> build/lib/torf
installing to build/bdist.linux-x86_64/wheel
running install
running install_lib
creating build/bdist.linux-x86_64/wheel
creating build/bdist.linux-x86_64/wheel/torf
copying build/lib/torf/_torrent.pyi -> build/bdist.linux-x86_64/wheel/./torf
copying build/lib/torf/_errors.py -> build/bdist.linux-x86_64/wheel/./torf
copying build/lib/torf/_stream.pyi -> build/bdist.linux-x86_64/wheel/./torf
copying build/lib/torf/_utils.pyi -> build/bdist.linux-x86_64/wheel/./torf
copying build/lib/torf/_utils.py -> build/bdist.linux-x86_64/wheel/./torf
copying build/lib/torf/_reuse.py -> build/bdist.linux-x86_64/wheel/./torf
copying build/lib/torf/_errors.pyi -> build/bdist.linux-x86_64/wheel/./torf
copying build/lib/torf/_torrent.py -> build/bdist.linux-x86_64/wheel/./torf
copying build/lib/torf/_generate.py -> build/bdist.linux-x86_64/wheel/./torf
copying build/lib/torf/_magnet.pyi -> build/bdist.linux-x86_64/wheel/./torf
copying build/lib/torf/__init__.pyi -> build/bdist.linux-x86_64/wheel/./torf
copying build/lib/torf/py.typed -> build/bdist.linux-x86_64/wheel/./torf
copying build/lib/torf/_magnet.py -> build/bdist.linux-x86_64/wheel/./torf
copying build/lib/torf/__init__.py -> build/bdist.linux-x86_64/wheel/./torf
copying build/lib/torf/_stream.py -> build/bdist.linux-x86_64/wheel/./torf
running install_egg_info
Copying torf.egg-info to build/bdist.linux-x86_64/wheel/./torf-4.3.0-py3.13.egg-info
running install_scripts
creating build/bdist.linux-x86_64/wheel/torf-4.3.0.dist-info/WHEEL
creating '/home/Kevin/blackarch/packages/python-torf/src/torf-4.3.0/dist/.tmp-_luv5mux/torf-4.3.0-py3-none-any.whl' and adding 'build/bdist.linux-x86_64/wheel' to it
adding 'torf/__init__.py'
adding 'torf/__init__.pyi'
adding 'torf/_errors.py'
adding 'torf/_errors.pyi'
adding 'torf/_generate.py'
adding 'torf/_magnet.py'
adding 'torf/_magnet.pyi'
adding 'torf/_reuse.py'
adding 'torf/_stream.py'
adding 'torf/_stream.pyi'
adding 'torf/_torrent.py'
adding 'torf/_torrent.pyi'
adding 'torf/_utils.py'
adding 'torf/_utils.pyi'
adding 'torf/py.typed'
adding 'torf-4.3.0.dist-info/licenses/LICENSE'
adding 'torf-4.3.0.dist-info/METADATA'
adding 'torf-4.3.0.dist-info/WHEEL'
adding 'torf-4.3.0.dist-info/top_level.txt'
adding 'torf-4.3.0.dist-info/RECORD'
removing build/bdist.linux-x86_64/wheel
Successfully built torf-4.3.0-py3-none-any.whl
==> Entering fakeroot environment...
==> Starting package()...
==> Tidying install...
  -> Removing libtool files...
  -> Purging unreproducible ruby files...
  -> Removing static library files...
  -> Purging unwanted files...
  -> Stripping unneeded symbols from binaries and libraries...
  -> Compressing man and info pages...
libfakeroot internal error: payload not recognized!
==> Checking for packaging issues...
==> Creating package "python-torf"...
  -> Generating .PKGINFO file...
  -> Generating .BUILDINFO file...
  -> Generating .MTREE file...
  -> Compressing package...
==> Leaving fakeroot environment.
==> Finished making: python-torf 4.3.0-2 (Tue Dec 30 13:50:24 2025)
==> Installing package python-torf with pacman -U...
[sudo] password for Kevin: 
loading packages...
resolving dependencies...
looking for conflicting packages...

Packages (1) python-torf-4.3.0-2

Total Installed Size:  0.66 MiB
Net Upgrade Size:      0.43 MiB

:: Proceed with installation? [Y/n] y
(1/1) checking keys in keyring                                            [##########################################] 100%
(1/1) checking package integrity                                          [##########################################] 100%
(1/1) loading package files                                               [##########################################] 100%
(1/1) checking for file conflicts                                         [##########################################] 100%
(1/1) checking available disk space                                       [##########################################] 100%
:: Processing package changes...
(1/1) upgrading python-torf                                               [##########################################] 100%
:: Running post-transaction hooks...
(1/1) Arming ConditionNeedsUpdate...
[Kevin@archlinux python-torf]$ python
Python 3.13.11 (main, Dec  7 2025, 13:01:45) [GCC 15.2.1 20251112] on linux
Type "help", "copyright", "credits" or "license" for more information.
Ctrl click to launch VS Code Native REPL
>>> from torf import Torrent
>>> 
[Kevin@archlinux python-torf]$ 
```

## python-console-menu test

* [Diff](https://github.com/KevinCrrl/blackarch/commit/820be6018325291bd4b0582f4ebd894d4404f31e)

```bash
[Kevin@archlinux python-console-menu]$ LC_ALL=C makepkg -si
==> Making package: python-console-menu 0.8.0-5 (Tue Dec 30 14:03:05 2025)
==> Checking runtime dependencies...
==> Checking buildtime dependencies...
==> Retrieving sources...
  -> Downloading console-menu-0.8.0.tar.gz...
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0   0     0   0     0     0     0  --:--:-- --:--:-- --:--:--     0
100 48873 100 48873   0     0 74894     0  --:--:-- --:--:-- --:--:-- 74894
==> Validating source files with sha512sums...
    console-menu-0.8.0.tar.gz ... Passed
==> Extracting sources...
  -> Extracting console-menu-0.8.0.tar.gz with bsdtar
==> Starting build()...
* Getting build dependencies for wheel...
/usr/lib/python3.13/site-packages/setuptools/dist.py:759: SetuptoolsDeprecationWarning: License classifiers are deprecated.
!!

        ********************************************************************************
        Please consider removing the following classifiers in favor of a SPDX license expression:

        License :: OSI Approved :: MIT License

        See https://packaging.python.org/en/latest/guides/writing-pyproject-toml/#license for details.
        ********************************************************************************

!!
  self._finalize_license_expression()
running egg_info
writing console_menu.egg-info/PKG-INFO
writing dependency_links to console_menu.egg-info/dependency_links.txt
writing requirements to console_menu.egg-info/requires.txt
writing top-level names to console_menu.egg-info/top_level.txt
reading manifest file 'console_menu.egg-info/SOURCES.txt'
reading manifest template 'MANIFEST.in'
no previously-included directories found matching 'docs/_build'
adding license file 'LICENSE.md'
writing manifest file 'console_menu.egg-info/SOURCES.txt'
* Building wheel...
/usr/lib/python3.13/site-packages/setuptools/dist.py:759: SetuptoolsDeprecationWarning: License classifiers are deprecated.
!!

        ********************************************************************************
        Please consider removing the following classifiers in favor of a SPDX license expression:

        License :: OSI Approved :: MIT License

        See https://packaging.python.org/en/latest/guides/writing-pyproject-toml/#license for details.
        ********************************************************************************

!!
  self._finalize_license_expression()
running bdist_wheel
The [wheel] section is deprecated. Use [bdist_wheel] instead.
/usr/lib/python3.13/site-packages/setuptools/_distutils/cmd.py:135: SetuptoolsDeprecationWarning: bdist_wheel.universal is deprecated
!!

        ********************************************************************************
        With Python 2.7 end-of-life, support for building universal wheels
        (i.e., wheels that support both Python 2 and Python 3)
        is being obviated.
        Please discontinue using this option, or if you still need it,
        file an issue with pypa/setuptools describing your use case.

        This deprecation is overdue, please update your project and remove deprecated
        calls to avoid build errors in the future.
        ********************************************************************************

!!
  self.finalize_options()
running build
running build_py
creating build/lib/consolemenu
copying consolemenu/multiselect_menu.py -> build/lib/consolemenu
copying consolemenu/console_menu.py -> build/lib/consolemenu
copying consolemenu/screen.py -> build/lib/consolemenu
copying consolemenu/prompt_utils.py -> build/lib/consolemenu
copying consolemenu/selection_menu.py -> build/lib/consolemenu
copying consolemenu/menu_formatter.py -> build/lib/consolemenu
copying consolemenu/menu_component.py -> build/lib/consolemenu
copying consolemenu/__init__.py -> build/lib/consolemenu
copying consolemenu/version.py -> build/lib/consolemenu
creating build/lib/consolemenu/items
copying consolemenu/items/submenu_item.py -> build/lib/consolemenu/items
copying consolemenu/items/selection_item.py -> build/lib/consolemenu/items
copying consolemenu/items/command_item.py -> build/lib/consolemenu/items
copying consolemenu/items/function_item.py -> build/lib/consolemenu/items
copying consolemenu/items/external_item.py -> build/lib/consolemenu/items
copying consolemenu/items/__init__.py -> build/lib/consolemenu/items
creating build/lib/consolemenu/validators
copying consolemenu/validators/url.py -> build/lib/consolemenu/validators
copying consolemenu/validators/base.py -> build/lib/consolemenu/validators
copying consolemenu/validators/__init__.py -> build/lib/consolemenu/validators
copying consolemenu/validators/regex.py -> build/lib/consolemenu/validators
creating build/lib/consolemenu/format
copying consolemenu/format/menu_padding.py -> build/lib/consolemenu/format
copying consolemenu/format/menu_margins.py -> build/lib/consolemenu/format
copying consolemenu/format/menu_borders.py -> build/lib/consolemenu/format
copying consolemenu/format/menu_style.py -> build/lib/consolemenu/format
copying consolemenu/format/__init__.py -> build/lib/consolemenu/format
installing to build/bdist.linux-x86_64/wheel
running install
running install_lib
creating build/bdist.linux-x86_64/wheel
creating build/bdist.linux-x86_64/wheel/consolemenu
copying build/lib/consolemenu/multiselect_menu.py -> build/bdist.linux-x86_64/wheel/./consolemenu
creating build/bdist.linux-x86_64/wheel/consolemenu/items
copying build/lib/consolemenu/items/submenu_item.py -> build/bdist.linux-x86_64/wheel/./consolemenu/items
copying build/lib/consolemenu/items/selection_item.py -> build/bdist.linux-x86_64/wheel/./consolemenu/items
copying build/lib/consolemenu/items/command_item.py -> build/bdist.linux-x86_64/wheel/./consolemenu/items
copying build/lib/consolemenu/items/function_item.py -> build/bdist.linux-x86_64/wheel/./consolemenu/items
copying build/lib/consolemenu/items/external_item.py -> build/bdist.linux-x86_64/wheel/./consolemenu/items
copying build/lib/consolemenu/items/__init__.py -> build/bdist.linux-x86_64/wheel/./consolemenu/items
copying build/lib/consolemenu/console_menu.py -> build/bdist.linux-x86_64/wheel/./consolemenu
creating build/bdist.linux-x86_64/wheel/consolemenu/validators
copying build/lib/consolemenu/validators/url.py -> build/bdist.linux-x86_64/wheel/./consolemenu/validators
copying build/lib/consolemenu/validators/base.py -> build/bdist.linux-x86_64/wheel/./consolemenu/validators
copying build/lib/consolemenu/validators/__init__.py -> build/bdist.linux-x86_64/wheel/./consolemenu/validators
copying build/lib/consolemenu/validators/regex.py -> build/bdist.linux-x86_64/wheel/./consolemenu/validators
copying build/lib/consolemenu/screen.py -> build/bdist.linux-x86_64/wheel/./consolemenu
creating build/bdist.linux-x86_64/wheel/consolemenu/format
copying build/lib/consolemenu/format/menu_padding.py -> build/bdist.linux-x86_64/wheel/./consolemenu/format
copying build/lib/consolemenu/format/menu_margins.py -> build/bdist.linux-x86_64/wheel/./consolemenu/format
copying build/lib/consolemenu/format/menu_borders.py -> build/bdist.linux-x86_64/wheel/./consolemenu/format
copying build/lib/consolemenu/format/menu_style.py -> build/bdist.linux-x86_64/wheel/./consolemenu/format
copying build/lib/consolemenu/format/__init__.py -> build/bdist.linux-x86_64/wheel/./consolemenu/format
copying build/lib/consolemenu/prompt_utils.py -> build/bdist.linux-x86_64/wheel/./consolemenu
copying build/lib/consolemenu/selection_menu.py -> build/bdist.linux-x86_64/wheel/./consolemenu
copying build/lib/consolemenu/menu_formatter.py -> build/bdist.linux-x86_64/wheel/./consolemenu
copying build/lib/consolemenu/menu_component.py -> build/bdist.linux-x86_64/wheel/./consolemenu
copying build/lib/consolemenu/__init__.py -> build/bdist.linux-x86_64/wheel/./consolemenu
copying build/lib/consolemenu/version.py -> build/bdist.linux-x86_64/wheel/./consolemenu
running install_egg_info
running egg_info
writing console_menu.egg-info/PKG-INFO
writing dependency_links to console_menu.egg-info/dependency_links.txt
writing requirements to console_menu.egg-info/requires.txt
writing top-level names to console_menu.egg-info/top_level.txt
reading manifest file 'console_menu.egg-info/SOURCES.txt'
reading manifest template 'MANIFEST.in'
no previously-included directories found matching 'docs/_build'
adding license file 'LICENSE.md'
writing manifest file 'console_menu.egg-info/SOURCES.txt'
Copying console_menu.egg-info to build/bdist.linux-x86_64/wheel/./console_menu-0.8.0-py3.13.egg-info
running install_scripts
creating build/bdist.linux-x86_64/wheel/console_menu-0.8.0.dist-info/WHEEL
creating '/home/Kevin/blackarch/packages/python-console-menu/src/console-menu-0.8.0/dist/.tmp-n7djwneb/console_menu-0.8.0-py2.py3-none-any.whl' and adding 'build/bdist.linux-x86_64/wheel' to it
adding 'console_menu-0.8.0.dist-info/licenses/LICENSE.md'
adding 'consolemenu/__init__.py'
adding 'consolemenu/console_menu.py'
adding 'consolemenu/menu_component.py'
adding 'consolemenu/menu_formatter.py'
adding 'consolemenu/multiselect_menu.py'
adding 'consolemenu/prompt_utils.py'
adding 'consolemenu/screen.py'
adding 'consolemenu/selection_menu.py'
adding 'consolemenu/version.py'
adding 'consolemenu/format/__init__.py'
adding 'consolemenu/format/menu_borders.py'
adding 'consolemenu/format/menu_margins.py'
adding 'consolemenu/format/menu_padding.py'
adding 'consolemenu/format/menu_style.py'
adding 'consolemenu/items/__init__.py'
adding 'consolemenu/items/command_item.py'
adding 'consolemenu/items/external_item.py'
adding 'consolemenu/items/function_item.py'
adding 'consolemenu/items/selection_item.py'
adding 'consolemenu/items/submenu_item.py'
adding 'consolemenu/validators/__init__.py'
adding 'consolemenu/validators/base.py'
adding 'consolemenu/validators/regex.py'
adding 'consolemenu/validators/url.py'
adding 'console_menu-0.8.0.dist-info/METADATA'
adding 'console_menu-0.8.0.dist-info/WHEEL'
adding 'console_menu-0.8.0.dist-info/top_level.txt'
adding 'console_menu-0.8.0.dist-info/RECORD'
removing build/bdist.linux-x86_64/wheel
Successfully built console_menu-0.8.0-py2.py3-none-any.whl
==> Entering fakeroot environment...
==> Starting package()...
==> Tidying install...
  -> Removing libtool files...
  -> Purging unreproducible ruby files...
  -> Removing static library files...
  -> Purging unwanted files...
  -> Stripping unneeded symbols from binaries and libraries...
  -> Compressing man and info pages...
==> Checking for packaging issues...
==> Creating package "python-console-menu"...
  -> Generating .PKGINFO file...
  -> Generating .BUILDINFO file...
  -> Generating .MTREE file...
  -> Compressing package...
==> Leaving fakeroot environment.
==> Finished making: python-console-menu 0.8.0-5 (Tue Dec 30 14:03:11 2025)
==> Installing package python-console-menu with pacman -U...
[sudo] password for Kevin: 
loading packages...
resolving dependencies...
looking for conflicting packages...

Packages (1) python-console-menu-0.8.0-5

Total Installed Size:  0.36 MiB
Net Upgrade Size:      0.26 MiB

:: Proceed with installation? [Y/n] y
(1/1) checking keys in keyring                                  [##################################] 100%
(1/1) checking package integrity                                [##################################] 100%
(1/1) loading package files                                     [##################################] 100%
(1/1) checking for file conflicts                               [##################################] 100%
(1/1) checking available disk space                             [##################################] 100%
:: Processing package changes...
(1/1) upgrading python-console-menu                             [##################################] 100%
:: Running post-transaction hooks...
(1/1) Arming ConditionNeedsUpdate...
[Kevin@archlinux python-console-menu]$ python
Python 3.13.11 (main, Dec  7 2025, 13:01:45) [GCC 15.2.1 20251112] on linux
Type "help", "copyright", "credits" or "license" for more information.
Ctrl click to launch VS Code Native REPL
>>> from consolemenu import *
>>> from consolemenu.items import *
>>> menu = ConsoleMenu("Title", "Subtitle")
>>> 
[Kevin@archlinux python-console-menu]$ 
```
