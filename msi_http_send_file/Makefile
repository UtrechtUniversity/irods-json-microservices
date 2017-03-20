GCC=g++
INC=-I/usr/include/irods/ -I/opt/irods-externals/boost1.60.0-0/include/boost/

all: msi_http_send_file

msi_http_send_file:
	${GCC} ${INC} -DRODS_SERVER -fPIC "-Wl,-E" -shared -g -Wno-deprecated -rdynamic -o lib$@.so $@.cpp `curl-config --libs` /usr/lib/libirods_client.so

clean:
	@rm -f ./*.so
