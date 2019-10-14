step to run linux0.01:

1. install bochs

2. make floppy disk using bximage,named a.img for example.

3. write  Image to floppy disk
   dd of=a.img	if=Image

4. create config file(config.cfg) for bochs,

   romimage:file=/usr/local/share/bochs/BIOS-bochs-latest
   vgaromimage:file=/usr/local/share/bochs/VGABIOS-lgpl-latest
   floppya:1_44=a.img,status=inserted
   boot:floppy	

5. run bochs with config file
   bochs -f config.cfg
