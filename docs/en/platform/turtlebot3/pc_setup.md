---
layout: archive
lang: en
ref: pc_setup
read_time: true
share: true
author_profile: false
permalink: /docs/en/platform/turtlebot3/pc_setup/
sidebar:
  title: TurtleBot3
  nav: "turtlebot3"
product_group: turtlebot3
page_number: 7
---

<div style="counter-reset: h1 6"></div>
<div style="counter-reset: h2 0"></div>

<!--[dummy Header 1]>
  <h1 id="pc-setup"><a href="#pc-setup">PC Setup</a></h1>
<![end dummy Header 1]-->

## [PC Setup](#pc-setup)

![](/assets/images/platform/turtlebot3/software/remote_pc_and_turtlebot.png)

**WARNING**: The contents in this chapter corresponds to the `Remote PC` (your desktop or laptop PC) which will control TurtleBot3. Do not apply this instruction to your TurtleBot3.
{: .notice--warning}

**NOTE**: This instruction was tested on Linux with `Ubuntu 16.04` and `ROS1 Kinetic Kame`, and Windows with `Windows 10` and ROS `ROS1 Melodic Morenia`
{: .notice--info}

Select which Operating System you'd like to use for the remote PC:
- [Ubuntu](#install-ubuntu-on-remote)
- [Windows](#windows-setup-remote-pc)

**NOTE**: ROS on Windows was brought up using [Up2](https://up-board.org/upsquared/specifications/) and an `Intel Nuc`.
{: .notice--warning}


### [Install Ubuntu on Remote PC](#install-ubuntu-on-remote-pc)

Download and install the `Ubuntu 16.04` on the `Remote PC (your desktop or laptop PC)` from the following link.

- [Download link][ubuntu_download_link]

If you need more help for installing Ubuntu, check out the step-by-step guide from the link below.

- [Install ubuntu desktop](https://www.ubuntu.com/download/desktop/install-ubuntu-desktop)

### [Install ROS 1 on Remote PC](#install-ros-1-on-remote-pc)

![](/assets/images/platform/turtlebot3/logo_ros.png)

The following script will allow you to simplify ROS 1 installation procedure. Run the following command in a terminal window. The terminal application can be found with the Ubuntu search icon on the top left corner of the screen, or you can use shortcut key for terminal is `Ctrl`-`Alt`-`T`. After install ROS 1, please reboot Remote PC.

``` bash
$ sudo apt-get update
$ sudo apt-get upgrade
$ wget https://raw.githubusercontent.com/ROBOTIS-GIT/robotis_tools/master/install_ros_kinetic.sh && chmod 755 ./install_ros_kinetic.sh && bash ./install_ros_kinetic.sh
```

If you prefer manual installation, please following the link below.

- [Manual installation of ROS 1 Kinetic](http://wiki.ros.org/kinetic/Installation/Ubuntu)  

**NOTE**: In order to check which packages are installed, please check this link out. [install_ros_kinetic.sh](https://raw.githubusercontent.com/ROBOTIS-GIT/robotis_tools/master/install_ros_kinetic.sh)
{: .notice--info}

{% capture info_01 %}
**NOTE**:  
 - ROBOTIS ROS packages support Melodic Morenia, however, it is recommended to use ROS Kinetic Kame for TurtleBot3.
 - In case of upgrading ROS to Melodic Morenia, please make sure that third party ROS packages are fully supported.
{% endcapture %}
<div class ="notice--info">{{info_01 | markdownify}}</div>

### [Install Dependent ROS 1 Packages](#install-dependent-ros-1-packages)

The next step is to install dependent packages for TurtleBot3 control on Remote PC.

``` bash
$ sudo apt-get install ros-kinetic-joy ros-kinetic-teleop-twist-joy ros-kinetic-teleop-twist-keyboard ros-kinetic-laser-proc ros-kinetic-rgbd-launch ros-kinetic-depthimage-to-laserscan ros-kinetic-rosserial-arduino ros-kinetic-rosserial-python ros-kinetic-rosserial-server ros-kinetic-rosserial-client ros-kinetic-rosserial-msgs ros-kinetic-amcl ros-kinetic-map-server ros-kinetic-move-base ros-kinetic-urdf ros-kinetic-xacro ros-kinetic-compressed-image-transport ros-kinetic-rqt-image-view ros-kinetic-gmapping ros-kinetic-navigation ros-kinetic-interactive-markers
```

``` bash
$ cd ~/catkin_ws/src/
$ git clone https://github.com/ROBOTIS-GIT/turtlebot3_msgs.git
$ git clone -b kinetic-devel https://github.com/ROBOTIS-GIT/turtlebot3.git
$ cd ~/catkin_ws && catkin_make
```

If `catkin_make` command is completed without any errors, the preparation for TurtleBot3 is done.


### [Network Configuration](#network-configuration)

![](/assets/images/platform/turtlebot3/software/network_configuration.png)

ROS 1 requires IP addresses in order to communicate between TurtleBot PC and the remote PC. The remote PC and TurtleBot PC should be connected to the same wifi router.

Enter the below command on the terminal window of the remote PC to find out the IP address of the remote PC.

``` bash
$ ifconfig
```

Text strings in the rectangle is the IP address of the `Remote PC`.

![](/assets/images/platform/turtlebot3/software/network_configuration2.png)

Enter the below command.

``` bash
$ nano ~/.bashrc
```

Press `alt+/` to end line of the file.

Modify the address of `localhost` in the `ROS_MASTER_URI` and `ROS_HOSTNAME` with the IP address acquired from the above terminal window.

![](/assets/images/platform/turtlebot3/software/network_configuration3.png)

Then, source the bashrc with below command.

``` bash
$ source ~/.bashrc
```

[ubuntu_download_link]: https://www.ubuntu.com/download/alternative-downloads

### [[Windows] Setup Remote PC](#windows-setup-remote-pc)

If you do not already have `Windows 10` on your Remote PC (Desktop, Laptop or SBC), you can download a trial of Windows 10 IoT Enterprise from the following link:
- [Download Windows 10 IoT Enterprise(Trial)][windows_download_link]

[windows_download_link]: https://www.microsoft.com/en-us/evalcenter/evaluate-windows-10-enterprise

Please refer to the [ROS Wiki instructions](https://wiki.ros.org/Installation/Windows) for installing ROS on Windows.

### [Windows] Setup TurtleBot3 WS
``` bash
> mkdir c:\ws\turtlebot3\src
> cd c:\ws\turtlebot3\src
> catkin_init_workspace
> git clone -b melodic-devel https://github.com/ROBOTIS-GIT/turtlebot3_msgs
> git clone -b melodic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations
> git clone -b melodic-devel https://github.com/ROBOTIS-GIT/turtlebot3
> git clone -b melodic-devel https://github.com/ROBOTIS-GIT/hls_lfcd_lds_driver
> cd c:\ws\turtlebot3
> rosdep update
> rosdep install --from-paths src --ignore-src -r -y
> catkin_make
> devel\setup.bat
```

### [[Windows] Network Configuration](#windows-network-configuration)
To communicate from a Windows 10 system to a remote single board computer (SBC) running on the turtlebot, set the following environment variables:

``` bash
> set ROS_MASTER_URI=http://<IP address of the SBC>:11311
> set ROS_HOSTNAME=<name of the windows computer>
```





