# -*- makefile -*-
# -----------------------------------------------------------------------------
#                              src/Makefile.am
#
# -----------------------------------------------------------------------------

clean-local:
	-rm -f log *.log *.log.old *~ *.dat *.gwm

EXTRA_DIST = \
	aclocal.m4 \
	appveyor.yml \
	autom4te.cache \
	bin \
	bootstrap \
	CHANGELOG.md \
	CMakeLists.txt \
	CMakeModules \
	config.guess \
	config.log \
	config.status \
	config.sub \
	configure \
	configure.ac \
	contrib \
	doc \
	docker \
	example \
	include \
	include_dirs.js \
	install-sh \
	library.json \
	libtool \
	license.txt \
	ltmain.sh \
	m4 \
	Makefile.am \
	missing \
	package.json \
	rapidjson.autopkg \
	RapidJSONConfig.cmake.in \
	RapidJSONConfigVersion.cmake.in \
	RapidJSON.pc.in \
	rapidjson.spec.in \
	rapidjson.spec \
	readme.md \
	readme.zh-cn.md \
	test \
	thirdparty \
	travis-doxygen.sh

#dist: rapidjson.@VERSION@-@BUILD@.tar.gz

#rapidjson.@VERSION@-@BUILD@.tar.gz: ${EXTRA_DIST}
#	tar zcf $@ $<

dist-hook: 
	[ ! -f paths ] || cat paths >> rapidjson.spec
	cp rapidjson.spec $(distdir)

# Disable autoheader.
AUTOHEADER=echo 

MAINTAINERCLEANFILES= \
	Makefile.in


CLEANFILES = *~


