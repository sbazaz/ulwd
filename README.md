## Universal Library for Linux (WebDAQ)

**Info:** Contains a library to access DAQ modules on the WebDAQ devices over the Linux platform. The UL for Linux binary name is libulwd.

### Install Instructions
---------------------

1. Update your package list:

``` sh
  sudo apt-get update
```
  
2. Download the latest version of **ulwd**:

``` sh
  $ cd ~
  $ wget https://github.com/sbazaz/ulwd/releases/download/v0.0.1-beta.2/libulwd.0.0.1-b2.tar.bz2
```     
3. Extract the tar file:
 
``` sh
  $ tar -xvjf libulwd.0.0.1-b2.tar.bz2
```

4. Run the following commands to install the library:

``` sh
  $ cd libulwd
  $ sudo sh install.sh
```

5. Reboot the WebDAQ system

### Examples

#### Python
The Python examples are located in the examples folder. To execute the examples, run the following commands:

``` sh
  ./AInScan.py
  ./AInScan_IEPE.py
```

#### C
The C examples are located in the examples folder. Run the following commands to build the examples:

``` sh
  cd ~/libulwd/examples
  make
```

To execute the examples, run the following commands:

``` sh
  ./AInScan
  ./AInScan_IEPE
```

#### Note: The DAQ module's firmware is stored in a volatile memory, therefore the firmware image will be lost when the WebDAQ system is shut down. The ulGetDeviceInventory function loads the firmware image to the module when it is invoked for the first time after system boot up. Loading the firmware image takes about 5 to 8 seconds.
