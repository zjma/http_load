AUTOMAKE_OPTIONS = foreign

AM_CFLAGS = -Wall

bin_PROGRAMS = http_load
http_load_SOURCES = http_load.c timers.h port.h timers.c timers.h
http_load_CFLAGS = $(SSL_DEFS) $(SSL_INC)
http_load_LDFLAGS = -s
http_load_LDADD = $(SSL_LIBS) -ldl
man_MANS = http_load.1

