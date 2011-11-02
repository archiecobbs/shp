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

dist_bin_SCRIPTS=   shp

man_MANS=           shp.1

pkgdata_DATA=       shp.awk

docdir=             $(datadir)/doc/packages/$(PACKAGE)

doc_DATA=           CHANGES COPYING README INSTALL

EXTRA_DIST=         CHANGES shp.in shp.1.in shp.spec.in shp.awk.in

subst=              sed \
			-e 's|@PACKAGE[@]|$(PACKAGE)|g' \
			-e 's|@PACKAGE_VERSION[@]|$(PACKAGE_VERSION)|g' \
			-e 's|@BASH[@]|$(BASH)|g' \
			-e 's|@GAWK[@]|$(GAWK)|g' \
			-e 's|@OPENSSL[@]|$(OPENSSL)|g' \
			-e 's|@pkgdatadir[@]|$(pkgdatadir)|g' \
			-e 's|@bindir[@]|$(bindir)|g' \
			-e 's|@mandir[@]|$(mandir)|g'

SUFFIXES=           .in
.in:
		    rm -f $@; $(subst) < $< >$@

DISTCLEANFILES=     shp shp.1 shp.spec shp.awk

