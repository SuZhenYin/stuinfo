CC=gcc
AFLAGS=-Wall -g
LDFLAGS= -lmysqlclient
OBJS= stu_add.cgi stu_del.cgi stu_sel.cgi class_add.cgi class_sel.cgi class_del.cgi sc_sel.cgi sc_add.cgi sc_del.cgi

all:$(OBJS)

$(OBJS):%.cgi:%.c
	$(CC) $(AFLAGS) $< cgic.c -o $@ $(LDFLAGS)

.PHONY:clean
clean:
	rm ./*.cgi

install:
	cp *.cgi /usr/lib/cgi-bin/sx/
	cp head.html foot.html /usr/lib/cgi-bin/sx/
