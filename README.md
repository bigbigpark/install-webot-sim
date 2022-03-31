# Install-Webot-Sim
This repository accounts for a guideline to install Webot's Simulator <br/>
If you want to install the stable version of Webots, follow these instructions. <br/>

<br/>

## 1. Download Webot's release
You can download webot's here -> https://github.com/cyberbotics/webots/releases <br/>
In my case, I downloaded `webots-R2021a-x86-64_ubuntu-18.04.tar.bz2` <br/>
<br/>

Tested on: <br/>
Ubuntu 18.04 LTS <br/>
ROS melodic <br/>

<br/>

## 2. Unzip the file

~~~bash
$ unzip webots-R2021a-x86-64_ubuntu-18.04.tar.bz2
~~~

<br/>

## 3. Install webots-ros pacakage

~~~bash
$ sudo apt install ros-melodic-webots-ros
~~~

<br>

## 4. Set environment variables

~~~bash
$ gedit ~/.bashrc
~~~

~~~bash
export WEBOTS_HOME=${INSTALLED_PATH} (ex: /home/bigbigpark/tools/webots)
export LD_LIBRARY_PATH=:$LD_LIBRARY_PATH:$WEBOTS_HOME/lib/controller
export PYTHONPATH=$PYTHONPATH:$WEBOTS_HOME/lib/controller/python27
~~~

~~~bash
 $ source ~/.bashrc
~~~

<br/>

## 5. Run

You can run `./webots` at your installed path
