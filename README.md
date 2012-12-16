Requires Ubuntu Customization Kit 2.4.6+

Building the ISO for ROS Fuerte
--------------------------------
sudo uck-remaster ~/Downloads/ubuntu-12.04-desktop-amd64.iso ~/turtlebot-iso

Config Files
--------------------------------
apt_packages	List of packages to install via apt
apt_deinstall	Packages to remove from the default Ubuntu ISO
deb_packages	Packages that are not in a public repo [for testing]
pip_packages	Python packages installed via pip
inst_packages	Packages only needed for installer
patch_list	ISO patches [if all else fails]

OEM Install
--------------------------------
To prevent the system from being installed with a default password,
hold down the left shift key when grub starts and press F4 to select
'OEM Mode' and select 'Install Ubuntu'. After the machine reboots,
oem-config-prepare or the OEM setup desktop icon must be run to make
the machine ready for the enduser.

Getting it to install from PXE boot is left as an exercise for the
vendor. Patches are appreciated.

Known Bugs
--------------------------------
UEFI sucks. Often the installer will fail, when booting off of USB
make sure to select the non-UEFI option.
