GCC=g++
INC=-I/usr/include/irods/ -I/opt/irods-externals/boost1.60.0-0/include/boost/

all: unmount

unmount:
	${GCC} ${INC} -DRODS_SERVER -fPIC -shared -o libirods_unmount.so unmount.cpp /usr/lib/libirods_client.so

clean:
	@rm -f ./*.so
