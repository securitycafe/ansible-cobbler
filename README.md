# ansible-cobbler

An ansible playbook for installing cobbler on Centos7, complete with a vagrant VM setup to test.

Prerequisites:

* Host Linux OS (Fedora 23 used to create this system), with:
    - ansible and vagrant packages installed
    - VirtualBox installed

* Downloaded CentOS 7 'Everything' ISO. (https://www.centos.org/download/) available on the Host

To run:

* run ./setup.sh and follow the instructions at the end
* run ./install_test_distro.sh and follwo the instructions at the end

To test the cobbler VM setup works:

* Create a new VirtualBox test VM with default disk size of 8GB
* Set the test VM to boot from the network (PXE boot)
* Set the test VM to use a network Host-only Adapter using the same vboxnet as the cobbler VM,
  this adapter should have the mac address 080027A2FB85
* Mount the CentOS-7 ISO used previosuly as a DVD device in the test VM
* Boot the test VM - it should PXE boot and install CentOS 7
* Once installed, close the VM and set to boot from Hard Drive before restarting
* Party
