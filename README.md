# cmpe283-assignment1

## Members
Jinxuan Hu (013728936) Xuan Shi(013856401)

## Contribution of team members
Jinxuan Hu ----Download VMware Fusion and install Ubuntu20.04, setup the enrironment and write code for ProcessBased and Secondary procbased controls.

Xuan Shi ---- Download VMware Fusion and install Ubuntu20.04,setup the enrironment  and write ernel code for Entry and Exit controls.

## Environment setup
1. Download and install VMmare Fusion from VMware official website.
2. Create a new virtual machine and choose Ubuntu 20.04 as the guesting operating system.
3. Preparing for the following three assignments, we configure it with 128GB hard disk space and 4GB memory
4. Install and run Ubuntu20.04 
5. Enable hypervisor application in this virtual machine to enable running modern virtualization applications by providing support for Intel VT-x/EPT inside this virtual machine.
6. Install KVM pakages(for intel processor) using the command
	> $ sudo apt install qemu-kvm libvirt-clients libvirt-daemon-system bridge-utils
7. check is KVM is installed
	> $ sudo kvm-ok
8. Install virt-manager using the command
	> $ sudo apt install virt-manager
9. Check if nested virtulization is enabled by using the command
	> $ cat /proc/cpuinfo

## Implement Process
1. Download cmpe283-1.c and Makefile from Files on Canvas.
2. Add the kernel code for all the MSR's to cmpe283-1.c and save the file.  Each of us build the kernel code for two controls.
3. Install make and gcc using the following commands, which is used for compile the cmpe283-1.c.
	> $ sudo apt install make         
	> $ sudo apt install gcc
2. Compile the file using make command
	> $ make
3. After the compile, the file "cmpe283-1.ko" is created and use below command to load this file
	> $ sudo insmod ./cmpe283-1.ko
4. Use the below command to show the system log. 
	> $ dmesg
  	<image src = "https://github.com/JinxuanHu/cmpe283-assignment1/blob/master/screenshots/ProcBased.png">
  	<image src = "https://github.com/JinxuanHu/cmpe283-assignment1/blob/master/screenshots/ProcBasedSecondary.png">
  	<image src = "https://github.com/JinxuanHu/cmpe283-assignment1/blob/master/screenshots/entry.png">
	<image src = "https://github.com/JinxuanHu/cmpe283-assignment1/blob/master/screenshots/exit.png">
		
5. Unload the kernel by using the below command to clean all the files generate by the above.                                                           
	> $ sudo rmmod cmpe283-1
