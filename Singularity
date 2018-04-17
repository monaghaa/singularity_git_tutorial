Bootstrap:docker  
From:ubuntu:18.04

%labels
MAINTAINER Andy M

%environment
HELLO_BASE=/code
export HELLO_BASE

%runscript
echo "This is run when you run the image!" 
exec /bin/bash /code/hello.sh "$@"  

%post  
echo "This section is performed after you bootstrap to build the image."  
mkdir -p /code  
apt-get install -y vim nano 
echo "echo Hello World" >> /code/hello.sh
chmod u+x /code/hello.sh  
