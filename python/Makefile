TOP        = ./
SWIGEXE    = /usr/local/bin/swig
SWIG_LIB_DIR = /usr/local/share/swig/3.0.12/
CXXSRCS    = ../cxx/src/qbus_record_msg.cc ../cxx/src/qbus_consumer.cc ../cxx/src/qbus_producer.cc ../cxx/src/qbus_config.cc ../cxx/src/qbus_helper.cc ../cxx/util/logger.cc ../cxx/src/qbus_consumer_imp.cc -g
TARGET     = qbus
INTERFACE  = qbus.i
LIBS       = 
SWIGOPT    = -threads

check: build
	$(MAKE) -f $(TOP)/TopMakefile SRCDIR='$(SRCDIR)' python_run

build:
	$(MAKE) -f $(TOP)/TopMakefile SRCDIR='$(SRCDIR)' $(SWIGLIB) CXXSRCS='$(CXXSRCS)' \
	SWIG_LIB_DIR='$(SWIG_LIB_DIR)' SWIGEXE='$(SWIGEXE)' \
	SWIGOPT='$(SWIGOPT)' TARGET='$(TARGET)' INTERFACE='$(INTERFACE)' python_cpp #\
	PYTHON_LINK='$(PYTHON_LINK)' \
	PYTHON_INCLUDE='$(PYTHON_INCLUDE)' \
	CENT_VER='$(CENT_VER)' 

#static:
#	$(MAKE) -f $(TOP)/TopMakefile SRCDIR='$(SRCDIR)' $(SWIGLIB) CXXSRCS='$(CXXSRCS)' \
#	SWIG_LIB_DIR='$(SWIG_LIB_DIR)' SWIGEXE='$(SWIGEXE)' \
#	SWIGOPT='$(SWIGOPT)' TARGET='mypython' INTERFACE='$(INTERFACE)' python_cpp_static

clean:
	$(MAKE) -f $(TOP)/TopMakefile SRCDIR='$(SRCDIR)' TARGET='$(TARGET)' python_clean
