############################################################################
######## WARNING, please follow the instructions and try it in a VM ########
############################################################################

1. Instructions before modifiing kernel:

	> zypper install kernel-devel kernel-source 
	> zypper install ncurses-devel
	> cp –LR /usr/src/linux ~/linux_src
	move .config to ~/linux_src
	> make oldconfig
	> make menucondig
		> General Setup-->Local versión – append to kernel release
		> Exit & save
	> cat /etc/default/grub_installdevice
		/dev/sda2 -> here your SO location

	> sudo make bzImage
	> sudo make modules
	> sudo make modules_install
	> sudo make intall
	put a # block in /etc/default/grub
		# GRUB_THEME
		# GRUB_BACKFROUND
	then, execute instructions inside grub

2. Restart your OS, enter in avanced options and enjoy the project
