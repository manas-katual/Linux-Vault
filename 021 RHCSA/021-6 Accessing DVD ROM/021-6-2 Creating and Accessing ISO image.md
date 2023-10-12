Link : [[021 RHCSA Index]]

# Creating and Accessing ISO image

**Steps to Manage an ISO image of a DVD Rom**

1. Create an ISO image from a DVD Rom
	`# dd if=/dev/sr0 of=/rhel9.iso`
	![[021-6-1 Creating and Accessing ISO image 2023-10-02 14.58.14.excalidraw]]
2. Verify the new ISO image file
	`# ls -lh /rhel9.iso`
1. Mount ISO image on a directory
	<abbr title="loop is the logical device driver for ISO images">`# mount -o loop /rhel9.iso /mnt`</abbr>
1. Make mounting persistent
	<abbr title="/etc/fstab is a file used for storing persistent mount entries">`# echo "/rhel9.iso /mnt iso9660 defaults 0 0" >> /etc/fstab`</abbr>
	`# rebbot`
	`# ls /mnt`
