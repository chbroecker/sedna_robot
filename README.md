# Sedna

![sedna_robot](sedna_docs/images/sedna_robot.jpg?raw=true "sedna_robot")

## Maintainers
* [Julian Gaal](mailto:gjulian@uos.de)
* [Christopher Broecker](mailto:chbroecker@uos.de)
* [Sebastian Pütz](mailto:spuetz@uos.de)

## Installation

### 1. Install wstool
```
sudo apt install python-wstool
mkdir -p ~/sedna_ws
```

### 2. Use wstool to pull all required packages
```
wstool init src https://raw.githubusercontent.com/chbroecker/sedna_robot/kinetic/sedna_util/sedna.rosinstall
wstool update -t src
```

### 3. Pico Flexx Royale Libary
* download the royale SDK `libroyale.zip` from the [manufacturers website](http://pmdtec.com/picofamily/software/) with the costumer password provided in the pico flexx casing
* Extract the linux 64 bit archive from the extracted SDK to `sedna_ws/src/pico_flexx_driver/royale`

### 4. Update UDEV Rules
Install the udev rules for the pico_flexx
```
cd ~/sedna_ws/src/pico_flexx_driver/royale
sudo cp libroyale-<version_number>-LINUX-64Bit/driver/udev/10-royale-ubuntu.rules /etc/udev/rules.d/
```

Install the udev rules for the sick tim
```
sudo cp ~/sedna_ws/src/sick_tim/udev/81-sick-tim3xx.rules /etc/udev/rules.d
```
Install the udev rules for the phidgets driver
```
sudo cp ~/sedna_ws/src/phidgets_drivers/phidgets_api/share/udev/99-phidgets.rules /etc/udev/rules.d
```

## Sedna_Util
We provide a script for an easy remote connection setup in `sedna_util/sedna.rc`.
*Make sure it is sourced in `~/.bashrc`*

The script contains the following functions:
@TODO

## Remote Connection
@TODO
