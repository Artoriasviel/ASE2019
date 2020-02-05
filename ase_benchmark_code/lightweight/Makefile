

STRUCT_IMPL=

gpp = g++ -std=c++11 -O3 -g
inc = -I$(PWD)/../include
lib = -lpthread

lightweight_bin:
	@echo $(STRUCT_IMPL)
	$(gpp) $(inc) -D$(STRUCT_IMPL) -DCHECK_CORRECTNESS -o $(STRUCT_IMPL)_tester.o lightweight_bench.cpp $(lib)
	$(gpp) $(inc) -D$(STRUCT_IMPL) -o $(STRUCT_IMPL)_timer.o lightweight_bench.cpp $(lib)

clean:
	rm -f *.o
