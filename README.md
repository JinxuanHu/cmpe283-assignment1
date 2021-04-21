# cmpe283-assignment1
## Members
Jinxuan Hu (013728936) Xuan Shi(013856401)
## Contribution of team members
Jinxuan Hu

Xuan Shi
## Environment setup
1. Download and install Parallels Desktop.
2. Choose Ubuntu 64-bit as the guesting perating system.
3. Configure it with 200GB hard disk space and 4GB memory
4. Install Ubuntu 20.04 powered by Parallels Desktop16 and run the VM

## Process
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
