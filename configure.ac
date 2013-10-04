AC_INIT([dotfiles], [0.0.1], [kspillner@acm.org])
AC_PREREQ([2.59])

# Load local m4 macros
AC_CONFIG_MACRO_DIR([m4])

# Check for GNU Make
AX_CHECK_GNU_MAKE
if ! test x$_cv_gnu_make_command = x; then
  MAKEFILE_SOURCE=GNUMakefile
else
  MAKEFILE_SOURCE=BSDMakefile
fi

AC_CONFIG_FILES([Makefile])

AC_OUTPUT
