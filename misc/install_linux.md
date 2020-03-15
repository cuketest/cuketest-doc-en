# Install CukeTest on Linux

CukeTest is an Automated Testing tool which base on BDD. It is support to run on graphic Linux OS, such as Ubuntu, CentOS, Kylin etc.

## Install by .deb File

CukeTest has `deb` install file which named like `cuketest_*_amd64.deb`. 

### Install by Graphic Interface
Double click `deb` file and wait for system app manage tool. Then click `Install` button to start the setup.

### Install by Command
First, press `ctrl+shift+T` on keyboard open terminal. Then switch to the install path. And suppose the install path is `~/share/`.
```
cd ~/share/
```

The `deb` file is use by system command tool: `dpkg`. Run below command.  
```
sudo dpkg -i cuketesst_*_amd64.deb
```

When the command finished, CukeTest was installed successful:

![deb install](./assets/Setup_EN.png)

## Run CukeTest

And now, CukeTest is ready to run. There has been two ways to launch CukeTest, through command or through graphic user interface.

### Launch from command line
Open termianl and use this command run CukeTest:
```
cuketest 
```

### Launch from UI
Open dash search `cuketest` you'll find the icon of CukeTest, double-click it.

![Welcome](./assets/Welcome_EN.png)