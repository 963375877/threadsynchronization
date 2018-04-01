inc=
src=./src
obj=./obj
cgi=./cgi
GCC=gcc

SrcFiles=$(wildcard $(src)/*.c)
ObjFiles=$(patsubst $(src)/%.c,$(obj)/%.o,$(SrcFiles))


.PHONY:all clean


all:$(cgi)/pthread_print.out

$(cgi)/pthread_print.out:$(ObjFiles)
	$(GCC) -o $@ $< -lpthread

$(obj)/%.o:$(src)/%.c
	$(GCC) -c $< -o $@

clean:
	rm -f $(obj)/*.o
	rm -f $(cgi)/*.out



