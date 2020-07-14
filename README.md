# MacOS-Sierra-and-OpenCore-on-a-computer-with-Asrock-H61M-motherboard-and-Celeron-G-1620-CPU
Sierra with Bootloader Clover works very well. But I want to do the same thing using OpenCore
I used GitHub directions for IvY Bridge, and those for switching from Clover to OpenCore.
In the "logfile" it shows that I am stuck at "SmcReadValue Key 4D535463 Size 1 and SmcReadValue Key 4D534163 Size 2".
But until then, the messages are all marked with "Success", which is why I don't understand anything anymore.
Last message ": Prelinked status - Success". I also attach the EFI folder. I'm stuck, because I can't find an explanation for this message. Is there an indication somewhere, how to proceed? 
With i3-3225 I tested to find out what expectations I can hope for. Using Clover, I managed to install Mojave on this motherboard. Compared to what I left, now there is a great method (I mean hotpatching). I felt that this way I would be able to get some results. Mojave has been installed flawlessly and works perfectly.
I tried to install Catalina as well, but it didn't work with Clover. After the first boot, it gave me an error and refused to install.
Now I end the history of using the Clover. We went on to apply the exceptional experience and knowledge of the programmers on GitHub, regarding OpenCore. My goal is to be able to help those who have a motherboard to install a modern, viable macOS with an attractive design, able to work with a computer with equipment at the level of 2012.
And I built an OpenCore that works with Sierra and above (how high it can get).
The bootable stick for Sierra helped me to install macOS Sierra on a clean hdd. I went ahead and installed an EFI & boot (legacy mode. I wasted a lot of time discovering that Asrock H61M, although it has UEFI support, can only boot legacy mode). √
Currently, the Sierra I installed has the correct resolution, correctly installed sound, sdcard, and usb works without limitations, sleep and sleep return are without reproach. Honestly, I can't tell if I have real macOS or ... a hack. I mean: with absolutely modest computing equipment, I can work as if I had a real macOS. But I tested the OpenCore set by me, including Mojave and Catalina. But I'm not successful yet. But I think that if Movaje is installed with Clover, it must work with OpenCore as well. I still have work to do to see what setting needs to be changed.
However, I was not able to install .icns, in order to have a complete OpenCore bootloader, but I am still documenting myself.
This is my whole work: efi-serra-harddisk.zip
I should add that compared to the motherboard settings for Clover, I haven't changed anything. And for Clover, the motherboard settings are the default ones.
An observation for fixing the sound: In DeviceProperties -> Add, layout-id can be expressed with Date, String or Number. Compared to the tutorial, the value obtained with printf '% x \ n' DECI_VAL, is not type, Number, but probably string (sorry, I haven't checked yet, since I set the correct layout-id value (value 16, in case of ALC662 ) and it works.
