## Process this file with autoconf to produce configure script

## Copyright (C) 2011–2022 Samediggi

## This program is free software: you can redistribute it and/or modify
## it under the terms of the GNU General Public License as published by
## the Free Software Foundation, either version 3 of the License, or
## (at your option) any later version.

## This program is distributed in the hope that it will be useful,
## but WITHOUT ANY WARRANTY; without even the implied warranty of
## MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
## GNU General Public License for more details.

## You should have received a copy of the GNU General Public License
## along with this program.  If not, see <http://www.gnu.org/licenses/>.
AC_INIT([giella-shared-mul], [0.0.3], [bugs@divvun.no], [giella-shared-mul], [http://divvun.no])
AC_CONFIG_AUX_DIR([build-aux])
AM_INIT_AUTOMAKE([1.9 tar-pax -Wall -Werror foreign])

## Program checks:
AC_PROG_MKDIR_P()
AC_PROG_INSTALL()

# for checks
AC_PATH_PROG([HFST_LEXC], [hfst-lexc], false)
AM_CONDITIONAL([CAN_HFST_LEXC], [test x$HFST_LEXC != xfalse])
AC_CONFIG_FILES([Makefile src/Makefile src/fst/Makefile src/fst/stems/Makefile \
                 $PACKAGE.pc])
AC_OUTPUT

cat<<EOF
-- Building $PACKAGE_STRING:

You can now run make and make check to update some of the files and ensure that
the shared files are kind of compilable. Make install will install the shared
data to a known location.
EOF
