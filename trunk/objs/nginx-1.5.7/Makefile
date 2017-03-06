
default:	build

clean:
	rm -rf Makefile objs

build:
	$(MAKE) -f objs/Makefile
	$(MAKE) -f objs/Makefile manpage

install:
	$(MAKE) -f objs/Makefile install

upgrade:
	/home/dexing/srs/srs-csdn/trunk/objs/nginx-1.5.7/_release/sbin/nginx -t

	kill -USR2 `cat /home/dexing/srs/srs-csdn/trunk/objs/nginx-1.5.7/_release/logs/nginx.pid`
	sleep 1
	test -f /home/dexing/srs/srs-csdn/trunk/objs/nginx-1.5.7/_release/logs/nginx.pid.oldbin

	kill -QUIT `cat /home/dexing/srs/srs-csdn/trunk/objs/nginx-1.5.7/_release/logs/nginx.pid.oldbin`
