#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

AC_PREREQ([2.69])
AC_INIT([http_load], [1.0])
AM_INIT_AUTOMAKE
AC_CONFIG_SRCDIR([http_load.c])

# Checks for programs.
AC_PROG_CC

# Checks for libraries.
AC_ARG_WITH(
    [ssl],
    [],
    [
        SSL_DEFS="-DUSE_SSL";
        SSL_LIBS="-L$withval/lib -lssl -lcrypto";
        SSL_INC="-I$withval/include"
    ],
    []
)

AC_SUBST(SSL_DEFS)
AC_SUBST(SSL_LIBS)
AC_SUBST(SSL_INC)

# Checks for header files.
AC_CHECK_HEADERS([arpa/inet.h fcntl.h netdb.h netinet/in.h stdlib.h string.h sys/socket.h sys/time.h unistd.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_TYPE_SIZE_T

# Checks for library functions.
AC_FUNC_MALLOC
AC_FUNC_REALLOC
AC_CHECK_FUNCS([gethostbyname gettimeofday memmove memset select socket strcasecmp strchr strdup strerror])

AC_CONFIG_FILES([Makefile])
AC_OUTPUT

