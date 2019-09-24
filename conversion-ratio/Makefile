input=list_impl
debug=

#gpp = /usr/local/bin/g++ -std=c++11 -O2
gpp = g++ -std=c++11 -O2
lib = -lpthread
tester=tester

cpdir = ../simple-data-structures/Yi-testfiles

test_all:
	cp $(input).h_save1  $(input).h
	make test
	cp $(input).h_save2  $(input).h
	make test
	cp $(input).h_save3  $(input).h
	make test
	cp $(input).h_save  $(input).h
	make test

test:
	$(gpp) $(tester).cpp $(input).cpp TATAS.cpp $(lib)
	./a.out 2 2

cp_now:
	cp $(input)*.h_save1  $(cpdir)/$(input)
	cp $(input)*.h_save2  $(cpdir)/$(input)
	cp $(input)*.h_save3  $(cpdir)/$(input)
	cp $(input)*.h_save  $(cpdir)/$(input)
	cp $(input)*.h  $(cpdir)/$(input)
	cp TASAS.*  $(cpdir)/$(input)

cp :
	make cp_now input=stack
	make cp_now input=ringbuffer
	make cp_now input=SinglyLinkedList
	make cp_now input=DoublyLinkedList
	make cp_now input=bst-seq

rename_now:
	cp $(input).h_save1  $(input)_save1.h
	cp $(input).h_save2  $(input)_save2.h
	cp $(input).h_save3  $(input)_save3.h
	cp $(input).h_save  $(input)_save.h

rename_all:
	make rename_now input=SinglyLinkedList
	make rename_now input=stack-seq
	make rename_now input=ringbuffer_seq

check:
	make test_all tester=tester input=list_impl
	make test_all tester=tester input=deque_vector
	make test_all tester=tester input=SinglyLinkedList
	make test_all tester=tester input=stack-seq
	make test_all tester=tester input=ringbuffer_seq
	make test_all tester=tester input=bst-seq
	make test_all tester=tester input=DoublyLinkedList
	make test_all tester=map_tester input=hash_map
	make test_all tester=map_tester input=mdlist

clean:
	rm -rf a.out *.o pan.* *.dSYM
