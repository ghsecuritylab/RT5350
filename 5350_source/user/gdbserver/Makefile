
ifdef CONFIG_COLDFIRE
CFLAGS += -DBUILD_WITHOUT_PIC_CODE=1
endif

# This file was generated automatically by configure.  Do not edit.
#VPATH = .
links =  xm.h tm.h nm.h
host_alias = i686-pc-linux-gnu
host_cpu = i686
host_vendor = pc
host_os = linux-gnu
host_canonical = i686-pc-linux-gnu
target_alias = m68k-elf
target_cpu = m68k
target_vendor = unknown
target_os = elf
target_canonical = m68k-unknown-elf
build_alias = i686-pc-linux-gnu
build_cpu = i686
build_vendor = pc
build_os = linux-gnu
build_canonical = i686-pc-linux-gnu
target_makefile_frag = ../config/m68k/monitor.mt
host_makefile_frag = ../config/i386/linux.mh
gxx_include_dir = ${prefix}/include/g++-
enable_shared = no
enable_version_specific_runtime_libs = no
gcc_version_trigger =
gcc_version =
#Copyright 1989, 90, 91, 92, 93, 94, 95, 96, 1997
#Free Software Foundation, Inc.

# This file is part of GDB.

# This program is free software; you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation; either version 2 of the License, or
# (at your option) any later version.
# 
# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
# 
# You should have received a copy of the GNU General Public License
# along with this program; if not, write to the Free Software
# Foundation, Inc., 59 Temple Place - Suite 330, Boston, MA 02111-1307, USA.

prefix = 

program_transform_name = -e s,^,m68k-elf-, 
exec_prefix = $(prefix)
bindir = ${exec_prefix}/bin
libdir = ${exec_prefix}/lib
tooldir = $(exec_prefix)/m68k-elf

datadir = ${prefix}/share
mandir = ${prefix}/man
man1dir = $(mandir)/man1
man2dir = $(mandir)/man2
man3dir = $(mandir)/man3
man4dir = $(mandir)/man4
man5dir = $(mandir)/man5
man6dir = $(mandir)/man6
man7dir = $(mandir)/man7
man8dir = $(mandir)/man8
man9dir = $(mandir)/man9
infodir = ${prefix}/info
includedir = ${prefix}/include

FLTFLAGS += -s 32768

SHELL = /bin/sh

INSTALL = `cd $(srcdir)/../..;pwd`/install-sh -c
INSTALL_PROGRAM = $(INSTALL)
INSTALL_DATA = $(INSTALL)

#AR = ar
AR_FLAGS = qv
#RANLIB = ranlib

# If you are compiling with GCC, make sure that either 1) You use the
# -traditional flag, or 2) You have the fixed include files where GCC
# can reach them.  Otherwise the ioctl calls in inflow.c
# will be incorrectly compiled.  The "fixincludes" script in the gcc
# distribution will fix your include files up.
#CC=cc
#CC=gcc -traditional
#GCC=gcc

# Directory containing source files.  Don't clean up the spacing,
# this exact string is matched for by the "configure" script.
srcdir = .

# It is also possible that you will need to add -I/usr/include/sys to the
# CFLAGS section if your system doesn't have fcntl.h in /usr/include (which 
# is where it should be according to Posix).

# Set this up with gcc if you have gnu ld and the loader will print out
# line numbers for undefinded refs.
#CC-LD=gcc -static
#CC-LD=${CC}

# Where is the "include" directory?  Traditionally ../include or ./include
#INCLUDE_DIR =  ${srcdir}/../../include
#INCLUDE_DEP = $$(INCLUDE_DIR)

# Where are the BFD library?
BFD_DIR = bfd
BFD = $(BFD_DIR)/libbfd.a
BFD_SRC = $(srcdir)/$(BFD_DIR)
BFD_CFLAGS = -I$(BFD_DIR) -I$(BFD_SRC)

# Where is the source dir for the READLINE library?  Traditionally in .. or .
# (For the binary library built from it, we use ${READLINE_DIR}${subdir}.)
#READLINE_DIR = ${srcdir}/../readline
#READLINE_DEP = $$(READLINE_DIR)

# All the includes used for CFLAGS and for lint.
# -I. for config files.
# -I${srcdir} possibly for regex.h also.
# -I${srcdir}/config for more generic config files.
#INCLUDE_CFLAGS = -I. -I${srcdir} -I${srcdir}/.. -I${srcdir}/../config -I$(INCLUDE_DIR)
INCLUDE_CFLAGS = -Igdb -Iinclude -Iconfig -I.

# M{H,T}_CFLAGS, if defined, has host- and target-dependent CFLAGS
# from the config/ directory.
GLOBAL_CFLAGS = ${MT_CFLAGS} ${MH_CFLAGS}
#PROFILE_CFLAGS = -pg

# CFLAGS is specifically reserved for setting from the command line
# when running make.  I.E.  "make CFLAGS=-Wmissing-prototypes".
#CFLAGS = -g -O2
# INTERNAL_CFLAGS is the aggregate of all other *CFLAGS macros.
INTERNAL_CFLAGS = ${CFLAGS} ${GLOBAL_CFLAGS} ${PROFILE_CFLAGS} \
	${BFD_CFLAGS} ${INCLUDE_CFLAGS}

# LDFLAGS is specifically reserved for setting from the command line
# when running make.

# Perhaps should come from parent Makefile
VERSION = gdbserver-4.12.3
DIST=gdb

LINT=/usr/5bin/lint
LINTFLAGS= $(BFD_CFLAGS)

# Host and target-dependent makefile fragments come in here.
####
# Target: Motorola m68k embedded (EST emulator, rom68k and bug monitors)
TDEPFILES= m68k-tdep.o monitor.o remote-est.o cpu32bug-rom.o rom68k-rom.o abug-rom.o dbug-rom.o dsrec.o
TM_FILE= tm-monitor.h
# Host: Intel 386 running GNU/Linux

XM_FILE= xm-linux.h
XDEPFILES= ser-tcp.o

NAT_FILE= nm-linux.h
# NATDEPFILES= infptrace.o solib.o inftarg.o fork-child.o corelow.o core-aout.o core-regset.o i386v-nat.o i386v4-nat.o
# End of host and target-dependent makefile fragments

# All source files that go into linking GDB remote server.

SFILES = $(srcdir)/low-lynx.c $(srcdir)/low-sparc.c $(srcdir)/low-sun3.c \
	 $(srcdir)/low-hppabsd.c \
	 $(srcdir)/utils.c $(srcdir)/server.c $(srcdir)/remote-utils.c

DEPFILES = $(GDBSERVER_DEPFILES)

SOURCES = $(SFILES) $(ALLDEPFILES)
TAGFILES = $(SOURCES) ${HFILES} ${ALLPARAM} ${POSSLIBS} 

OBS = utils.o low-linux.o server.o remote-utils.o

# Prevent Sun make from putting in the machine type.  Setting
# TARGET_ARCH to nothing works for SunOS 3, 4.0, but not for 4.1.
.c.o:
	${CC} -c ${INTERNAL_CFLAGS} $<

all: gdbserver gdbreplay

# Traditionally "install" depends on "all".  But it may be useful
# not to; for example, if the user has made some trivial change to a 
# source file and doesn't care about rebuilding or just wants to save the
# time it takes for make to check that all is up to date.
# install-only is intended to address that need.
install: all install-only
install-only: 
	n=`echo gdbserver | sed '$(program_transform_name)'`; \
	if [ x$$n = x ]; then n=gdbserver; else true; fi; \
	$(INSTALL_PROGRAM) gdbserver $(bindir)/$$n; \
	$(INSTALL_DATA) $(srcdir)/gdbserver.1 $(man1dir)/$$n.1

uninstall: force
	n=`echo gdbserver | sed '$(program_transform_name)'`; \
	if [ x$$n = x ]; then n=gdbserver; else true; fi; \
	rm -f $(bindir)/$$n $(man1dir)/$$n.1

installcheck:
check:
info dvi:
install-info:
clean-info:

gdbserver: $(OBS) ${ADD_DEPS} ${CDEPS}
	rm -f gdbserver
	$(CC) $(LDFLAGS) -o $@ $(OBS) $(GDBSERVER_LIBS) $(LDLIBS)

gdbreplay: gdbreplay.o
	rm -f gdbreplay
	$(CC) $(LDFLAGS) -o $@ gdbreplay.o $(XM_CLIBX) $(LDLIBS)

romfs:
	$(ROMFSINST) -e CONFIG_USER_GDBSERVER_GDBSERVER /bin/gdbserver
	$(ROMFSINST) -e CONFIG_USER_GDBSERVER_GDBREPLAY /bin/gdbreplay

config.status:
	@echo "You must configure gdbserver.  Look at the README file for details."
	@false

# Put the proper machine-specific files first, so M-. on a machine
# specific routine gets the one for the correct machine.
# The xyzzy stuff below deals with empty DEPFILES
TAGS:	${TAGFILES}
	etags `find ${srcdir}/../config -name $(TM_FILE) -print` \
	  `find ${srcdir}/../config -name ${XM_FILE} -print` \
	  `find ${srcdir}/../config -name ${NAT_FILE} -print` \
	  `for i in yzzy ${DEPFILES}; do \
	     if [ x$$i != xyzzy ]; then \
	       echo ${srcdir}/$$i | sed -e 's/\.o$$/\.c/' ; \
	     fi; \
	   done` \
	  ${TAGFILES}
tags: TAGS

clean:
	rm -f *.elf *.gdb *.o ${ADD_FILES} *~
	rm -f gdbreplay gdbserver core make.log

distclean: clean
	rm -f nm.h tm.h xm.h config.status
	rm -f Makefile

maintainer-clean realclean: clean
	rm -f nm.h tm.h xm.h config.status
	rm -f Makefile

STAGESTUFF=${OBS} ${TSOBS} ${NTSOBS} ${ADD_FILES} init.c init.o version.c gdb

force:

version.c: 
	echo 'char *version = "$(VERSION)";' >version.c

# GNU Make has an annoying habit of putting *all* the Makefile variables
# into the environment, unless you include this target as a circumvention.
# Rumor is that this will be fixed (and this target can be removed)
# in GNU Make 4.0.
.NOEXPORT:

# GNU Make 3.63 has a different problem: it keeps tacking command line
# overrides onto the definition of $(MAKE).  This variable setting
# will remove them.
MAKEOVERRIDES=

## This is ugly, but I don't want GNU make to put these variables in
## the environment.  Older makes will see this as a set of targets
## with no dependencies and no actions.
unexport CHILLFLAGS CHILL_LIB CHILL_FOR_TARGET :

server.o : ${srcdir}/server.c ${srcdir}/server.h
remote-utils.o : ${srcdir}/remote-utils.c ${srcdir}/server.h
low-linux.o : ${srcdir}/low-linux.c ${srcdir}/server.h
low-lynx.o : ${srcdir}/low-lynx.c ${srcdir}/server.h
low-sim.o : ${srcdir}/low-sim.c ${srcdir}/server.h
low-sparc.o : $(srcdir)/low-sparc.c $(srcdir)/server.h
low-sun3.o : $(srcdir)/low-sun3.c $(srcdir)/server.h
low-hppabsd.o : $(srcdir)/low-hppabsd.c $(srcdir)/server.h
utils.o : ${srcdir}/utils.c ${srcdir}/server.h

# This is the end of "Makefile.in".
