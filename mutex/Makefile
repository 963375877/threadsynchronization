inc=
src=./src
obj=./obj
cgi=./cgi
CgiFile=mutex_trylock.out
GCC=gcc

SrcFiles=$(wildcard $(src)/*.c)
ObjFiles=$(patsubst $(src)/%.c,$(obj)/%.o,$(SrcFiles))


.PHONY:all clean


all:$(cgi)/$(CgiFile)

$(cgi)/$(CgiFile):$(ObjFiles)
	$(GCC) -o $@ $< -lpthread

$(obj)/%.o:$(src)/%.c
	$(GCC) -c $< -o $@

clean:
	rm -f $(obj)/*.o
	rm -f $(cgi)/*.out



