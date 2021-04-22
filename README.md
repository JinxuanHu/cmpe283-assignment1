# cmpe283-assignment1
## Members
Jinxuan Hu (013728936) Xuan Shi(013856401)
## Contribution of team members
Jinxuan Hu

Xuan Shi
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

2. Build the file using make command
	> $ make
  <image src = "https://github.com/JinxuanHu/cmpe283-assignment1/blob/master/screenshot/command-make.png">
3. After building the file, cmpe283-1.ko is produced

4. Run the kernel code

	> $ sudo insmod ./cmpe283-1.ko
  
	> $ dmesg
  <image src = "https://github.com/JinxuanHu/cmpe283-assignment1/blob/master/screenshot/procbased.png">
  <image src = "https://github.com/JinxuanHu/cmpe283-assignment1/blob/master/screenshot/secondary-entry.png">
  <image src = "https://github.com/JinxuanHu/cmpe283-assignment1/blob/master/screenshot/exit.png">
