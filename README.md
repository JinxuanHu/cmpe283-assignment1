# cmpe283-assignment1

## Members
Jinxuan Hu (013728936) Xuan Shi(013856401)

## Contribution of team members
Jinxuan Hu ----Download VMvare Fusion and install Ubuntu20.04, setup the enrironment and write code for ProcessBased and Secondary procbased controls.
Xuan Shi ---- Download VMvare Fusion and install Ubuntu20.04,setup the enrironment  and write ernel code for Entry and Exit controls.

## Environment setup
1. Download and install VMvare Fusion from VMvare official website.
2. Create a new virtual machine and choose Ubuntu 20.04 as the guesting operating system.
3. Preparing for the following three assignments, we configure it with 128GB hard disk space and 4GB memory
4. Install and run Ubuntu20.04 
5. Install KVM pakages(for intel processor) using the command
6. Install virt-manager using the command
	> $ sudo apt install virt-manager
8. Check if nested virtulization is enabled by using the command
	> $ cat /proc/cpuinfo

## Implement Process
1. Download cmpe283-1.c and Makefile.
2. Add the kernel code for all the MSR's to cmpe283-1.c
3. Install make and gcc using sudo 
	> $ sudo apt install make         
	> $ sudo apt install gcc
2. Compile the file using make command
	> $ make
3. After the compile, the file "cmpe283-1.ko" is created and use below command to load this file
	> $ sudo insmod ./cmpe283-1.ko
4. Use the below command to show the result
	> $ dmesg
  <image src = "">
  <image src = "">
  <image src = "">
5. Unload the kernel by using the below command to clean all the files generate by the above.
	> $ sudo rmmod cmpe283-1
