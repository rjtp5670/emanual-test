---
layout: archive
lang: en
ref: joule_setup
read_time: true
share: true
author_profile: false
permalink: /docs/en/platform/turtlebot3/joule_setup/
sidebar:
  title: TurtleBot3
  nav: "turtlebot3"
product_group: turtlebot3
page_number: 10
---

<div style="counter-reset: h1 6"></div>
<div style="counter-reset: h2 2"></div>
<div style="counter-reset: h3 1"></div>

<!--[dummy Header 1]>
  <h1 id="setup"><a href="#setup">Setup</a></h1>
  <h2 id="sbc-setup"><a href="#sbc-setup">SBC Setup</a></h2>
<![end dummy Header 1]-->

### [Joule Setup](#joule-setup)

**WARNING**: Setup work requires Power and Time. So battery is not suitable. We recommend using SMPS (AC adapter) during this work.
{: .notice--warning}

#### [Install Linux (Ubuntu)](#install-linux-ubuntu)

In this section, the Alternative Ubuntu Desktop 16.04 LTS will be installed on Intel® Joule™.

**[Remote PC]** Download Ubuntu image `Alternative Ubuntu 16.04 for Intel® Joule™` from the below link.

- [Download Ubuntu 16.04 for Intel® Joule™](http://people.canonical.com/~platform/snappy/tuchuck/desktop-final/tuchuck-xenial-desktop-iso-20170317-0.iso)

**[Remote PC]** In order to make a bootable installation USB drive, please follow the [Alternative install(Ubuntu Desktop 16.04 LTS)][alternative-installubuntu-desktop-1604-lts] section from the below link.

- [Make a bootable installation USB drive](https://developer.ubuntu.com/core/get-started/intel-joule)

**[Remote PC]** Before getting started, The board needs to have its BIOS updated to [BIOS version #193][bios-version-193] to install Ubuntu Image. Download [BIOS version #193][bios-version-193] and flash the BIOS into the Joule by following instructions in the below link.

- [BIOS update](https://software.intel.com/en-us/flashing-the-bios-on-joule)

**WARNING**: Updating to the latest BIOS(1J2 or higher) may cause unexpected problem of `Intel® Joule™` with Ubuntu 16.04 LTS. Please use only the recommended [BIOS version #193][bios-version-193].
{: .notice--warning}

**WARNING**: `Intel® Joule™` comes with `passive heatsink` in the package. It is recommended to use the heatsink. In order to operate Joule without the heatsink, please follow the extra [instruction](https://software.intel.com/en-us/node/721471)
{: .notice--warning}

[bios-version-193]: https://downloadmirror.intel.com/26206/eng/joule-firmware-2017-02-19-193-public.zip
[alternative-installubuntu-desktop-1604-lts]: https://developer.ubuntu.com/core/get-started/intel-joule#alternative-install:-ubuntu-desktop-16.04-lts


If you need following step for installation, please refer to below link

  - [Step by step to install Ubuntu][step_by_step_to_install_ubuntu_on_joule]{: .popup}

#### [Install ROS](#install-ros)

**WARNING**: The contents in this chapter corresponds to the Intel® Joule™ which will be the main computer of **TurtleBot3 Waffle**. Do **NOT** apply this instruction to your Remote PC (your desktop PC or laptop).
{: .notice--warning}

**NOTE**: This instruction takes about 2 hours to install ROS and related packages for TurtleBot3. Elapsed time may vary depending on network environment.
{: .notice--info}

![](/assets/images/platform/turtlebot3/logo_ros.png)

**[TurtleBot]** Install ROS

``` bash
$ sudo apt-get update
$ sudo apt-get upgrade
$ wget https://raw.githubusercontent.com/ROBOTIS-GIT/robotis_tools/master/install_ros_kinetic.sh && chmod 755 ./install_ros_kinetic.sh && bash ./install_ros_kinetic.sh
```

**NOTE**: In order to check which packages are installed, please check this link out. [install_ros_kinetic](https://raw.githubusercontent.com/ROBOTIS-GIT/robotis_tools/master/install_ros_kinetic.sh)
{: .notice--info}

**NOTE**: After install ROS, please reboot Intel® Joule™.
{: .notice--info}

If you prefer manual installation, please following the link below.

- [Install ROS on Ubuntu](http://wiki.ros.org/kinetic/Installation/Ubuntu)

#### [Install Dependent Packages](#install-dependent-packages)

The next step is to install dependent packages for TurtleBot3 control.

**[TurtleBot]** Download packages from github

``` bash
$ cd ~/catkin_ws/src
$ git clone https://github.com/ROBOTIS-GIT/hls_lfcd_lds_driver.git
$ git clone https://github.com/ROBOTIS-GIT/turtlebot3_msgs.git
$ git clone https://github.com/ROBOTIS-GIT/turtlebot3.git
```

**NOTE**: If you want to use Intel® RealSense™, please check related appendix for [Intel® RealSense™](http://emanual.robotis.com/docs/en/platform/turtlebot3/appendix_realsense/#realsense)
{: .notice--info}

**[TurtleBot]** Delete some packages that are not needed in TurtleBot SBC

``` bash
$ cd ~/catkin_ws/src/turtlebot3
$ sudo rm -r turtlebot3_description/ turtlebot3_teleop/ turtlebot3_navigation/ turtlebot3_slam/ turtlebot3_example/
```

**[TurtleBot]** Install dependent packages

``` bash
$ sudo apt-get install ros-kinetic-rosserial-python ros-kinetic-tf
```

**NOTE**: After install packages, please reboot Intel® Joule™.
{: .notice--info}

**[TurtleBot]** Build packages

``` bash
$ cd ~/catkin_ws && catkin_make
```

If catkin_make command is completed without any errors, the preparation for TurtleBot3 is done.

#### [USB Settings](#usb-settings)

**[TurtleBot]** The following commands allow to use USB port for OpenCR1.0 without acquiring root permission.

``` bash
$ rosrun turtlebot3_bringup create_udev_rules
```

#### [Network Configuration](#network-configuration)

![](/assets/images/platform/turtlebot3/software/network_configuration.png)

ROS requires IP addresses in order to communicate between TurtleBot3 and remote PC.

Enter the below command on the terminal window of the SBC in TurtleBot3 to find out the IP address of TurtleBot3.

``` bash
$ ifconfig
```

Texts in the rectangle is the IP address of the `TurtleBot`.

![](/assets/images/platform/turtlebot3/software/network_configuration4.png)

Enter the following command.

``` bash
$ nano ~/.bashrc
```

Press ' `alt+/` ' to end line of the file.

Replace the `localhost` in the ROS_MASTER_URI address with the IP address acquired from [Remote PC Network Configuration](http://emanual.robotis.com/docs/en/platform/turtlebot3/pc_setup/#network-configuration). Also replace the `localhost` in the ROS_HOSTNAME address with the IP address acquired from the above terminal window, which is the IP address of TurtleBot3.

![](/assets/images/platform/turtlebot3/software/network_configuration5.png)

Then, source the bashrc with below command.

``` bash
$ source ~/.bashrc
```

[ros]: http://wiki.ros.org
[step_by_step_to_install_ubuntu_on_joule]: /docs/en/platform/turtlebot3/step_by_step_to_install_ubuntu_on_joule
