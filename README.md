Example:  Building Systems With Packer
==============

This is a simple example for using Packer (http://packer.io) to build two types of systems:

1.  A VMWare Fusion Virtual Machine (Mac OS X)
2.  An Amazon AMI

The end result will be output machine templates that run a basic Ubuntu 12.04 LTS release and an install of "Git".  This can obviously be extended to use provisioners and create more interesting machines - but I intend this to be a simple example of using Packer to build basic machines.

## Instructions

1.  Install http://packer.io according to directions.
1.  Clone this repository.
1.  Modify some basic settings (you may want to use a local Ubuntu ISO rather than downloading from the internet) and add your Amazon Access Key / Secret Access Key (etc.)
1.  To create a VMWare Fusion machine run the command (from the git checkout directory) `packer build vmware-example.json`
1.  To create an Amazon AMI run the command `packer build ami-example.json`
1.  To create both at the same time, run `packer build system-build.json`