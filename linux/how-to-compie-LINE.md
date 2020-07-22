## how-to-compie-LINE

### 1. install gsl from sourece code: 
```shell
wget http://mirror.yongbok.net/gnu/gsl/gsl-2.6.tar.gz
tar -zxvf gsl-1.6.tar.gz
cd gsl-1.16
./configure
make
sudo make install
```

Add these lines to your .bashrc file on your home directory.

```shell
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/lib
export CFLAGS="-I/usr/local/includ
```
> you may need to ln create a soft link for libgsl.so: 
  ```sudo ln -s libgsl.so libgsl.so.0```

### 2. or install gsl from apt-get

```sudo apt-get install libgsl-dev```
   
### 3. compiler line.cpp to executable 

```shell
g++ -o line ./line.cpp -lgsl -lpthread -lgslcblas
```
