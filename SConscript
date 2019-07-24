#! /bin/env python

Import('defconfig')


lib_name = 'websocket'

source_files = [
    Glob('src/*.c')
]

include_paths = [
    'include',
    '../transport/include',
    '../mbedtls/configs'
]

# Build library
installs = [
	('include', 'include/librws.h')
]

L_CFLAGS = "-DCONFIG_USING_TLS"

# Build library
defconfig.library(lib_name, source_files, CCFLAGS=L_CFLAGS, CPPPATH=include_paths, INSTALL=installs)
