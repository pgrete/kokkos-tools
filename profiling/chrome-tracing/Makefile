CXX=mpicxx
CFLAGS=-shared -O3 -g -fPIC -std=c++11 -Wall -Wextra

#Turn MPI support off:
#CFLAGS += -DUSE_MPI=0

MAKEFILE_PATH := $(subst Makefile,,$(abspath $(lastword $(MAKEFILE_LIST))))

CXXFLAGS+=-I${MAKEFILE_PATH}

kp_chrome_tracing.so: ${MAKEFILE_PATH}kp_chrome_tracing.cpp
	$(CXX) $(CFLAGS) -o $@ $<

clean:
	rm *.so 
