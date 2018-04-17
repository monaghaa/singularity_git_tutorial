Bootstrap:docker  
From:ubuntu:latest

%labels
MAINTAINER Andy M

%environment
HELLO_BASE=/code
export HELLO_BASE

%runscript
echo "This is run when you run the image!" 
exec /bin/bash /code/hello.sh "$@"  

%post  
apt-get update
echo "This section is performed after you bootstrap to build the image."  
mkdir -p /code  
apt-get install -y vim nano 
echo "echo Hello World" >> /code/hello.sh
chmod u+x /code/hello.sh  
