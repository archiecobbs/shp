#
# shp - Like PHP except you write your script in shell script
# 
# Copyright 2011 Archie L. Cobbs <archie@dellroad.org>
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
#

AC_INIT([shp Like PHP except you write your script in shell script],
  1.0.0,
  [http://code.google.com/p/shp/], [shp])

# Initialize autoconf
#AC_INIT([shp Like PHP except you write your script in shell script],
#  m4_esyscmd([git describe --tags --always --abbrev=8 --dirty | sed 's/^v//g' | tr '-' '_' | tr -d '\n']),
#  [http://code.google.com/p/shp/], [shp])
AC_CONFIG_AUX_DIR(scripts)
AM_INIT_AUTOMAKE
dnl AM_MAINTAINER_MODE
AC_PREREQ(2.59)
AC_PREFIX_DEFAULT(/usr)
AC_PROG_MAKE_SET

# Check for required programs
AC_PROG_INSTALL
AC_PATH_PROG([BASH], [bash], [], [])
if test -z "${BASH}"; then
    AC_MSG_ERROR([bash not found]);
fi
BASH=`echo "${BASH}" | sed 's|/sh$|/bash|g'`
AC_PATH_PROG([GAWK], [gawk], [], [])
if test -z "${GAWK}"; then
    AC_MSG_ERROR([gawk not found]);
fi
AC_PATH_PROG([OPENSSL], [openssl], [], [])
if test -z "${OPENSSL}"; then
    AC_MSG_ERROR([openssl not found]);
fi

# Check for /dev/urandom
AC_CHECK_FILE([/dev/urandom], [], AC_MSG_ERROR([/dev/urandom not found]))

# Generated files
AC_CONFIG_FILES(Makefile)

# Go
AC_OUTPUT
