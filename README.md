# README #

# Install necessary libraries

sudo apt-get install libtool pkg-config gcc libpcap-dev libnuma-dev linux-headers-$(uname -r)

# Build nDPI folder

cd vtc

cd nDPI

sudo ./autogen.sh

sudo ./configure

sudo make

sudo make install

# Build PF_RING

cd ../PF_RING

cd kernel 

sudo make

cd userland/examples

sudo make

sudo ./pfbridge -a eth0 -b eth1