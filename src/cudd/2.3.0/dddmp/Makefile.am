## ****************************************************************************
##
##  The following code is derived, directly or indirectly, from the SystemC
##  source code Copyright (c) 1996-2002 by all Contributors.
##  All Rights reserved.
##
##  The contents of this file are subject to the restrictions and limitations
##  set forth in the SystemC Open Source License Version 2.3 (the "License");
##  You may not use this file except in compliance with such restrictions and
##  limitations. You may obtain instructions on how to receive a copy of the
##  License at http://www.systemc.org/. Software distributed by Contributors
##  under the License is distributed on an "AS IS" basis, WITHOUT WARRANTY OF
##  ANY KIND, either express or implied. See the License for the specific
##  language governing rights and limitations under the License.
##  
## ****************************************************************************
##
##  Makefile.am --
##  Process this file with automake to produce a Makefile.in file.
## 
## ****************************************************************************
##
##  Original Authors:
##  Norris Ip, Dean Shea, John Rose, Jasvinder Singh, William Paulsen,
##  John Pierce, Rachida Kebichi, Ted Elkind, David Bailey,
##  Cadence Design Systems, Inc., 2002-09-23
##
## ****************************************************************************
##  
##  MODIFICATION LOG - modifiers, enter your name, affiliation, date and
##  changes you are making here.
##
##      Name, Affiliation, Date:
##  Description of Modification:
##
## ****************************************************************************

SHELL = /bin/sh
AUTOMAKE_OPTIONS = foreign
lib_LIBRARIES = libdddmp.a 

SUBDIRS = doc

libdddmp_a_SOURCES = \
		dddmp.h dddmpInt.h \
		dddmpDump.c dddmpBinary.c dddmpConvert.c dddmpDbg.c \
		dddmpDdNode.c 

EXTRA_DIST = \
	0.bdd \
	0or1.bdd \
	1.bdd \
	2.bdd \
	2and3.bdd \
	3.bdd \
	4.bdd \
	4xor5.bdd \
	5.bdd \
	README \
	README.test \
	composeids.txt \
	one.bdd \
	testdddmp.script \
	varauxids.ord \
	varnames.ord \
	zero.bdd 
		
INCLUDES = \
	-I${top_srcdir}/src/cudd/2.3.0/cudd \
	-I${top_srcdir}/src/cudd/2.3.0/util \
	-I${top_srcdir}/src/cudd/2.3.0/mtr \
	-I${top_srcdir}/src \
	-I${buildInc} \
	-DSCV_VERSION=\"$(VERSION)\"

copyFiles = ${top_builddir}/scripts/copyFiles.sh

all : all-recursive
	${copyFiles} -s . ${buildLib} ${lib_LIBRARIES}
