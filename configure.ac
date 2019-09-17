#  -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.68])
AC_INIT([stm32flash], [0.5], [])

# Checks for programs.
AM_INIT_AUTOMAKE([foreign -Wall])
AC_PROG_CC
AM_PROG_CC_C_O
AM_PROG_AR
AM_PROG_AS
LT_INIT
AC_CONFIG_MACRO_DIR([m4])

AC_ARG_ENABLE([libgpiod],
	[AC_HELP_STRING([--enable-libgpiod],
		[enable gpiod support [default=no]])],
	[if test "x$enableval" = xyes; then with_libgpiod=true; fi],
	[with_libgpiod=false])
AM_CONDITIONAL([WITH_LIBGPIOD], [test "x$with_libgpiod" = xtrue])
AM_COND_IF([WITH_LIBGPIOD], [
	PKG_CHECK_MODULES([LIBGPIOD], [libgpiod])
	AC_DEFINE([HAVE_LIBGPIOD], [1], [Define to 1 if LIBGPIOD is enabled.])
])

# Checks for programs.

# Checks for libraries.

# Checks for header files.

# Checks for typedefs, structures, and compiler characteristics.

# Checks for library functions.


AC_CONFIG_FILES(
 [
 Makefile
 parsers/Makefile
 ])

AC_OUTPUT
