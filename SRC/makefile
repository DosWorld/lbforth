all: lbf.exe lbfd.exe

lbf.exe: lbforth.c
        wcl -ms lbforth.c -fe=lbf.exe
        upx -9 --8086 lbf.exe

lbfd.exe: lbforth.c
        rem wcl386 -dBITS32 -bcl=pmodew lbforth.c -fe=lbfd.exe
        wcl386 -dBITS32 -bcl=causeway lbforth.c -fe=lbfd.exe
        upx -9 lbfd.exe

install: all
        copy lbf.exe ..\BIN\
        copy lbfd.exe ..\BIN\
clean:
        del *.obj
        del *.exe
        del *.bak

