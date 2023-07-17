AC_INIT([water], [current], [43019545+rdap@users.noreply.github.com], [water])
AM_INIT_AUTOMAKE([foreign])

AC_PROG_CC_C99

AC_PATH_XTRA
AM_CFLAGS="$AM_CFLAGS $X_CFLAGS"

AC_ARG_ENABLE(xft,
	[  --disable-xft           disable Xft font rendering],
	[case "${enableval}" in
		yes) xft=yes ;;
		no) xft=no ;;
		*) AC_MSG_ERROR(bad value ${enableval} for --enable-xft) ;;
		esac],
	[xft=yes])
if test x$xft = xyes; then
	PKG_CHECK_MODULES([xft], [xft >= 2.0.0], xft=yes, xft=no)
	AM_CFLAGS="$AM_CFLAGS $xft_CFLAGS"
fi
AM_CONDITIONAL(CONFIG_XFT, test x$xft = xyes)

AC_SUBST([AM_CFLAGS])
AC_CONFIG_FILES([Makefile])
AC_OUTPUT
