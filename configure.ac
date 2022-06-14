dnl Process this file with autoconf to produce a configure script.

m4_define([plugin_version_major], [1])
m4_define([plugin_version_minor], [15])
m4_define([plugin_version], [plugin_version_major.plugin_version_minor])

AC_INIT([deadbeef-mpris2-plugin], [plugin_version], [peterlamby@web.de], [DeaDBeeF MPRIS2 Plugin], [https://github.com/Serranya/deadbeef-mpris2-plugin])

AM_INIT_AUTOMAKE([foreign -Wall -Werror subdir-objects dist-xz no-dist-gzip silent-rules])
AM_SILENT_RULES([yes])

dnl Override $PACKAGE to make $pkglibdir use deadbeef search path
PACKAGE=deadbeef

AC_PROG_CC_C99
AM_PROG_AR
AC_PROG_INSTALL
AC_PROG_LIBTOOL
PKG_PROG_PKG_CONFIG

AC_DEFINE(PLUGIN_VERSION_MAJOR, [plugin_version_major],
          [Define to the plug-in major version])
AC_DEFINE(PLUGIN_VERSION_MINOR, [plugin_version_minor],
          [Define to the plug-in minor version])

LT_INIT

PKG_CHECK_MODULES([MPRIS_DEPS], [glib-2.0>=2.26 gio-2.0 gio-unix-2.0 gthread-2.0])

AS_IF([test "x$ac_cv_prog_cc_c99" = "xno"], AC_MSG_ERROR([C99 Support is required]))

AC_ARG_ENABLE(debug,
              AS_HELP_STRING([--enable-debug], [The plugin will print debug options to stdout.]),
              AC_DEFINE([MPRIS__DEBUG]))

AC_CONFIG_FILES([Makefile])
AC_OUTPUT
