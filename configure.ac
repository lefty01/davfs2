#                                               -*- Autoconf -*-
# Process this file with autoconf to produce a configure script.

# Copyright (C) 2006, 2007, 2008, 2009, 2012, 2020 Werner Baumann
#
# This file is part of davfs2.
#
# davfs2 is free software; you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation; either version 3 of the License, or
# (at your option) any later version.
#
# davfs2 is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with davfs2; if not, write to the Free Software Foundation,
# Inc., 51 Franklin St, Fifth Floor, Boston, MA 02110-1301, USA. */


AC_PREREQ(2.67)
AC_INIT(davfs2, 1.4.6, http://savannah.nongnu.org/projects/davfs2)
AC_CONFIG_SRCDIR([src/cache.c])
AC_CONFIG_AUX_DIR([config])
AM_INIT_AUTOMAKE

AC_CONFIG_HEADER([config.h])

# Checks for programs.
AC_PROG_CC
AC_PROG_GCC_TRADITIONAL
AC_PROG_INSTALL
AC_PROG_LN_S

# Checks for libraries.
AM_GNU_GETTEXT_VERSION(0.19)
AM_GNU_GETTEXT([external])
NE_REQUIRE_VERSIONS([0], [27 28 29 30 31 33])
DAV_CHECK_NEON

# Checks for header files.
AC_HEADER_DIRENT
AC_HEADER_MAJOR
AC_HEADER_STDC
AC_HEADER_TIME
AC_CHECK_HEADERS([fcntl.h langinfo.h libintl.h limits.h locale.h mntent.h stddef.h stdint.h stdlib.h string.h sys/file.h sys/mount.h sys/time.h syslog.h termios.h unistd.h utime.h])

# Checks for typedefs, structures, and compiler characteristics.
AC_C_CONST
AC_TYPE_UID_T
AC_C_INLINE
AC_TYPE_INT16_T
AC_TYPE_INT32_T
AC_TYPE_INT8_T
AC_TYPE_MODE_T
AC_TYPE_OFF_T
AC_TYPE_PID_T
AC_TYPE_SIZE_T
AC_TYPE_SSIZE_T
AC_CHECK_MEMBERS([struct stat.st_blksize])
AC_STRUCT_TM
AC_TYPE_UINT32_T
AC_TYPE_UINT64_T
AC_C_VOLATILE
AC_CHECK_SIZEOF([void *])

# Checks for library functions.
AC_FUNC_CHOWN
AC_FUNC_CLOSEDIR_VOID
AC_FUNC_ERROR_AT_LINE
AC_FUNC_FORK
AC_FUNC_GETGROUPS
AC_FUNC_GETMNTENT
AC_FUNC_MALLOC
AC_FUNC_SELECT_ARGTYPES
AC_FUNC_STRFTIME
AC_FUNC_STAT
AC_FUNC_UTIME_NULL
AC_CHECK_FUNCS([ftruncate getmntent memset mkdir nl_langinfo rpmatch select setlocale strcasecmp strchr strdup strerror strndup strpbrk strrchr strstr strtol strtoull utime])

# Misc.
DAV_DEFAULTS
DAV_LFS
DAV_LINGUAS([])
AC_DEFINE([_GNU_SOURCE], 1, [Define to enable GNU extensions])

AC_CONFIG_FILES([Makefile
                 po/Makefile.in
                 etc/Makefile
                 man/Makefile
                 man/de/Makefile
                 man/es/Makefile
                 src/Makefile])
AC_OUTPUT
DAV_MESSAGE
