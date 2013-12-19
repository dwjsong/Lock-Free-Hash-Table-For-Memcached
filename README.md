# Memcached

## Dependencies

* libevent, http://www.monkey.org/~provos/libevent/ (libevent-dev)
* GCC 4.7, http://gcc.gnu.org/gcc-4.7/

## Environment

Tested On x86_64 Ubuntu 12.04 LTS

## Edited Source Files

Added code to assoc.c so that it would be lock free.  assoc_find, _hashitem_before, assoc_insert, and assoc_delete function is edited to be lock free. The bucket lock itself is called at thread.c file but is commented out now.

## Install Instructions

export CC=gcc-4.7

./configure

make

make install
