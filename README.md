# openrave-installation

Bash scripts to install OpenRAVE from source. 

Supported distros:
* Ubuntu 14.04
* Ubuntu 16.04
* Ubuntu 18.04

## Travis - Continuous Integration

[![Build Status](https://travis-ci.org/crigroup/openrave-installation.svg?branch=master)](https://travis-ci.org/crigroup/openrave-installation)


## Installation
Run the scripts in the following order:
```bash
./install-dependencies.sh
./install-osg.sh
./install-fcl.sh
./install-openrave.sh
```   
After installation, remove the openscene version(not know why):  
```bash
apt list --installed | grep openscene  
apt-get remove libopenscenegraph-dev/bionic libopenscenegraph100v5/bionic openscenegraph/bionic  
```  
Before run programs, add path to PYTHONPATH
```bash
openrave-config --python-dir
export PYTHONPATH=$PYTHONPATH:"openrave-config --python-dir"
```