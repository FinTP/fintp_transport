ACLOCAL_AMFLAGS = -I ../fintp_utils/m4

AM_CPPFLAGS = -DUNIX -DDEBUG_ENABLED	\
-I$(FINTP_HOME)/fintp_utils/src	\
-I$(FINTP_HOME)/fintp_log/src	\
@CPPFLAGS@	\
@PTHREAD_CFLAGS@	\
@BOOST_CPPFLAGS@	\
@XERCES_CPPFLAGS@	\
@AMQ_CPPFLAGS@	\
@WMQ_CPPFLAGS@

lib_LTLIBRARIES = libfintp_transport.la

AUTOMAKE_OPTIONS = foreign

libfintp_transport_la_LDFLAGS = @LIBS@ @LDFLAGS@	\
@PTHREAD_LIBS@	\
@WMQ_LDFLAGS@ @WMQ_LIBS@	\
@AMQ_LDFLAGS@	\
-L$(FINTP_HOME)/fintp_utils/.libs -lfintp_utils	\
-L$(FINTP_HOME)/fintp_log/.libs -lfintp_log

if COMP_AMQ
 SRCS = $(COMMON_SRCS)	\
 src/ActiveMq/AmqHelper.cpp
else
 SRCS = $(COMMON_SRCS)
endif

if COMP_WMQ
 libfintp_transport_la_SOURCES = $(SRCS) \
 src/WebsphereMq/WMqHelper.cpp
else
 libfintp_transport_la_SOURCES = $(SRCS)
endif

COMMON_SRCS = src/MqException.cpp	\
src/MqLogPublisher.cpp	\
src/TransportHelper.cpp

nobase_include_HEADERS = src/ActiveMq/AmqHelper.h	\
src/MqException.h	\
src/MqLogPublisher.h	\
src/TransportHelper.h	\
src/WebsphereMq/WMqHelper.h

SUBDIRS = .
