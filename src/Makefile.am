EXTRA_DIST = jansson.def dtoa.c

include_HEADERS = jansson.h
nodist_include_HEADERS = jansson_config.h

lib_LTLIBRARIES = libjansson.la
libjansson_la_SOURCES = \
	dump.c \
	error.c \
	hashtable.c \
	hashtable.h \
	hashtable_seed.c \
	jansson_private.h \
	load.c \
	lookup3.h \
	memory.c \
	pack_unpack.c \
	strbuffer.c \
	strbuffer.h \
	strconv.c \
	utf.c \
	utf.h \
	value.c \
	version.c

if DTOA_ENABLED
libjansson_la_SOURCES += dtoa.c
endif

libjansson_la_LDFLAGS = \
	-no-undefined \
	-export-symbols-regex '^json_|^jansson_' \
	-version-info 18:1:14 \
	@JSON_SYMVER_LDFLAGS@ \
	@JSON_BSYMBOLIC_LDFLAGS@
