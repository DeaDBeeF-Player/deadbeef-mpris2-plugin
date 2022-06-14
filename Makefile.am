pkglib_LTLIBRARIES = mpris.la

ACLOCAL_AMFLAGS= -I m4

mpris_la_SOURCES=src/mpris.c src/mprisServer.c src/mprisServer.h src/logging.c src/logging.h src/artwork.h
mpris_la_CFLAGS=${MPRIS_DEPS_CFLAGS}
mpris_la_LDFLAGS=-module -avoid-version
mpris_la_LIBADD=${MPRIS_DEPS_LIBS}

EXTRA_DIST=LICENSE
