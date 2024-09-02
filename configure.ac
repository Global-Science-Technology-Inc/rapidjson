dnl ---------------------------------------------------------------------------
dnl configure.in - an example
dnl
dnl Replace: configure.in, CommCore
dnl ---------------------------------------------------------------------------

dnl ---------------------------------------------------------------------------
dnl ABI release number
dnl
dnl Legend:
dnl
dnl  +1 : ? : +1  == new interface that does not break old one
dnl  +1 : ? : 0   == new interface that breaks old one
dnl   ? : ? : 0   == no new interfaces, but breaks apps
dnl   ? :+1 : ?   == just some internal changes, nothing breaks but might work
dnl                  better
dnl ---------------------------------------------------------------------------

AC_INIT([rapidjson], m4_esyscmd_s([scripts/git-version-gen --pure --prefix release- --fallback 0.0.1 .tarball-version]), [carlnygard@fortna.com])
AM_INIT_AUTOMAKE(tar-ustar)
AC_CONFIG_MACRO_DIR([m4])

dnl ABI_VERSION=0:1:0
DOCROOT=.
RELEASE=$VERSION
BUILD=m4_esyscmd_s([scripts/git-version-gen --build --prefix release- --fallback 1 .tarball-build-version])

AC_SUBST(RELEASE)
AC_SUBST(BUILD)
AC_SUBST(DOCROOT)
dnl AC_SUBST(ABI_VERSION)

dnl Specify a configuration file
dnl AM_CONFIG_HEADER(config.h)

AM_MAINTAINER_MODE
PKG_INSTALLDIR

dnl ---------------------------------------------------------------------------
dnl Check build environment
dnl ---------------------------------------------------------------------------
dnl AC_ISC_POSIX
dnl AC_HEADER_STDC

dnl AC_PROG_CC
AC_PROG_CXX
AC_PROG_CXXCPP
AM_PROG_LIBTOOL
AM_SANITY_CHECK

dnl ---------------------------------------------------------------------------
dnl Set PACKAGE_LOCALE_DIR in config.h.
dnl ---------------------------------------------------------------------------

if test "x${prefix}" = "xNONE"; then
  AC_DEFINE_UNQUOTED(PACKAGE_LOCALE_DIR, "${ac_default_prefix}/${DATADIRNAME}/locale", [Localized package directory])
else
  AC_DEFINE_UNQUOTED(PACKAGE_LOCALE_DIR, "${prefix}/${DATADIRNAME}/locale", [Localized package directory])
fi

AC_LANG_CPLUSPLUS

dnl ---------------------------------------------------------------------------
dnl Checks for header files.
dnl ---------------------------------------------------------------------------
dnl AC_HEADER_DIRENT
dnl AC_HEADER_STDC
dnl AC_CHECK_HEADERS(limits.h unistd.h)

dnl ---------------------------------------------------------------------------
dnl Checks for typedefs, structures, and compiler characteristics.
dnl ---------------------------------------------------------------------------
dnl AC_TYPE_PID_T
dnl AC_TYPE_SIZE_T

dnl ---------------------------------------------------------------------------
dnl Checks for library functions.
dnl ---------------------------------------------------------------------------
dnl AC_CHECK_FUNCS(getcwd mkdir strerror strtol)

dnl ---------------------------------------------------------------------------
dnl Checks for dependent packages
dnl ---------------------------------------------------------------------------

dnl PKG_CHECK_MODULES(GDKPIXBUF, gdk-pixbuf-xlib-2.0 >= )
dnl AC_SUBST(GDKPIXBUF_CFLAGS)
dnl AC_SUBST(GDKPIXBUF_LIBS)

AC_PATH_PROG(CMAKE, cmake, no)
AC_PATH_PROG(PERL, perl, no)
AC_PATH_PROG(SED, sed, no)
AC_PATH_PROG(FIND, find, no)
AC_PATH_PROG(RM, rm, no)
AC_PATH_PROG(RMDIR, rmdir, no)

dnl ---------------------------------------------------------------------------
dnl Options
dnl ---------------------------------------------------------------------------


dnl ---------------------------------------------------------------------------
dnl Debug
dnl ---------------------------------------------------------------------------


dnl ---------------------------------------------------------------------------
dnl Post-processing - make substitution
dnl ---------------------------------------------------------------------------

dnl ---------------------------------------------------------------------------
dnl Generate Make files
dnl ---------------------------------------------------------------------------

dnl -- per library configs
dnl AC_CONFIG_FILES(pc/fixme.pc)
dnl AC_CONFIG_FILES(fixme/Makefile)

AC_CONFIG_FILES(Makefile)
AC_CONFIG_FILES(rapidjson.spec)

AC_OUTPUT
