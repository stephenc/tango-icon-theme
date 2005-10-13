# Process this file with autoconf to produce a configure script.
AC_PREREQ(2.53)

AC_INIT([tango-icon-theme], [0.1.0])
AC_CONFIG_SRCDIR(index.theme.in)

AM_INIT_AUTOMAKE([1.9 tar-ustar])

IT_PROG_INTLTOOL([0.33])

GETTEXT_PACKAGE="${PACKAGE}"
AC_SUBST(GETTEXT_PACKAGE)

ALL_LINGUAS=""
AM_GLIB_GNU_GETTEXT

# AM_GLIB_GNU_GETTEXT above subst. $DATADIRNAME
# this is the directory where the *.{mo,gmo} files are installed
localedir='${prefix}/${DATADIRNAME}/locale'
AC_SUBST(localedir)

# Workaround to make aclocal get the right flags
AC_SUBST(ACLOCAL_AMFLAGS, "\${ACLOCAL_FLAGS}")

# Define the toplevel path here
AC_SUBST(themedir, "\${datadir}/icons/Tango")

AC_PATH_PROG(ICONMAP, icon-name-mapping)
if test -z "$ICONMAP"; then
   AC_MSG_ERROR([icon-naming-utils is required for tango-icon-theme])
fi

AC_ARG_ENABLE(icon-framing,
   AC_HELP_STRING([--disable-icon-framing],
                   [disable creation of 24x24 icons [default=no]]),
    enable_framing=$enableval,
    enable_framing=yes)
AM_CONDITIONAL(ENABLE_ICON_FRAMING, test x$enable_framing = xyes)

if test "x$enable_framing" = "xyes"; then
   PKG_CHECK_MODULES(MAGICK, ImageMagick >= 5.5.7,
                     enable_framing=yes, enable_framing=no)
   if test "x$enable_framing" = "xyes"; then
      AC_PATH_PROG(CONVERT, convert)
      if test -z "$CONVERT"; then
      	 AC_MSG_ERROR([ImageMagick is required to build tango-icon-theme])
      fi

      # Add the command line options we need here
      CONVERT="$CONVERT -bordercolor Transparent -border 1x1"
      AC_SUBST(CONVERT)
   else
      AC_MSG_ERROR([ImageMagick is required to build tango-icon-theme])
   fi
fi

AC_CONFIG_FILES([
Makefile
16x16/Makefile
16x16/actions/Makefile
16x16/apps/Makefile
16x16/categories/Makefile
16x16/devices/Makefile
16x16/emblems/Makefile
16x16/emotes/Makefile
16x16/mimetypes/Makefile
16x16/status/Makefile
22x22/Makefile
22x22/actions/Makefile
22x22/apps/Makefile
22x22/categories/Makefile
22x22/devices/Makefile
22x22/emblems/Makefile
22x22/emotes/Makefile
22x22/mimetypes/Makefile
22x22/status/Makefile
scalable/Makefile
scalable/actions/Makefile
scalable/apps/Makefile
scalable/categories/Makefile
scalable/devices/Makefile
scalable/emblems/Makefile
scalable/emotes/Makefile
scalable/mimetypes/Makefile
scalable/status/Makefile
po/Makefile.in	
])	

AC_OUTPUT
