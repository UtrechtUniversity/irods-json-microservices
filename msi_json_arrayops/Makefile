GCC = g++
INC=-I/usr/include/irods/ -I/opt/irods-externals/boost1.60.0-0/include/boost/ -I/opt/irods-externals/jansson2.7-0/include

all: libmsi_json_arrayops

libmsi_json_arrayops:
	${GCC} ${INC} -DRODS_SERVER -fPIC "-Wl,-E" -shared -g -Wno-deprecated -rdynamic -o $@.so $@.cpp /usr/lib/libirods_client.so /opt/irods-externals/jansson2.7-0/lib/libjansson.a
     

clean:
	@rm -f ./*.so
