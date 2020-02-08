# :robot: Kernel Priority Queue Practice :robot:

1. Instructions before modifying kernel:

- Write in command line:
```
zypper install kernel-devel kernel-source 
zypper install ncurses-devel
cp –LR /usr/src/linux ~/linux_src
move .config to ~/linux_src
make oldconfig
make menuconfig
```

- Select in menuconfig
	- General Setup-->Local versión – append to kernel release
	- Exit & save


- Modify grub-installdevice file (Again CL)
```
nano /etc/default/grub_installdevice
```
and write: /dev/sda2 -> here your SO location

Then, in CL:
```
sudo make bzImage
sudo make modules
sudo make modules_install
sudo make install
```

- Finally put a # block in /etc/default/grub
	- ```# GRUB_THEME```
	- ```# GRUB_BACKGROUND```
	
and execute instructions inside grub

2. Restart your OS, enter in avanced options and enjoy the project
