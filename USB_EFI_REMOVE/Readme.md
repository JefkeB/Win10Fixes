Sometimes after using a usb disk with some embedded linux experiments a disk contains an EFI part.  
This part cannot be removed from the disk with the disk management tool from windows.

To remove this partition do the following

Open a command prompt and type

> diskpart  
this starts the diskpart commandline utility  

> list disk  
show all disk on the system and find the usb disk in the list  

> sel disk 3
select the correct usb disk  

> list partition  
show all partitions on the disk  

> sel partition1  
select the correct partition  

> SET ID=ebd0a0a2-b9e5-4433-87c0-68b6b72699c7  
change type to a data partition  

From now on the normal windows gui tools can be used to format the disk etc
