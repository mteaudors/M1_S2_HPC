EXECS = fibo_seq fibo_omp
CFLAGS= -O3 
OUT=output.txt 

all: $(EXECS)

fibo_seq: fibo_seq.c
	gcc $(CFLAGS) -o $@ $<

fibo_omp: fibo_omp.c
	gcc $(CFLAGS) -o $@ $< -fopenmp	

exec: all
	rm -rf $(OUT)
	(export N=50 ; for e in $(EXECS) ; do echo "Running $$e ..." ; echo "" >> $(OUT) ; echo "Running $$e ..." >> $(OUT) ; ./$$e $$N >> $(OUT) ; done)


clean: 
	rm -rf $(EXECS) *~

.phony: all
