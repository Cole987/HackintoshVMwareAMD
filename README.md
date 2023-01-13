# HackintoshVMwareAMD
Code for the VMX in order to make Work any MacOS system on an Virtual Machine Host by VMware Workstation and Player on AMD Processor



You Need first to Install the VMware Unlocker, you can find it there : 

https://github.com/paolo-projects/unlocker



------



After you need to create your Virtual Machine.

![https://freeimage.host/i/HYWEdXe](https://iili.io/HYWEdXe.png)

So Click on Create a new virtual machine

![image-20230114000048008](https://iili.io/HYWEJI9.png)

Click on Custom.



![image-20230114000112144](https://iili.io/HYWE9m7.png)

Click after on Next.

![image-20230114000151550](https://iili.io/HYWEFqb.png)

Then, click on I Will install the Operating system later.



![image-20230114000235568](https://iili.io/HYWEfrx.png)

Select "Apple Mac OS X", and Select the version that you want to install (Here for the example I will install MacOS 11)

![image-20230114000359126](https://iili.io/HYWEBdQ.png)

Select the drive were you want to put your VM and the Name of it (You can leave it by default)

![image-20230114000430338](https://iili.io/HYWEC7V.png)

Here select the number of cores that you want that you Virtual Machine have (You can leave it by default, but I recommend to put 4 cores)

![image-20230114000542818](https://iili.io/HYWEnkB.png)

After select the Amount of memory you want to allow for the Virtual Machine 

![image-20230114000636275](https://iili.io/HYWEomP.png)

Select your network type for the VM (Leave it by default)

![image-20230114000708953](https://iili.io/HYWEzI1.png)

Click on next here

![image-20230114000728217](https://iili.io/HYWEIhF.png)

Click on Next here

![image-20230114000748746](https://iili.io/HYWETLg.png)

Click on Next

![image-20230114000807293](https://iili.io/HYWEREJ.png)

Select Size of the Virtual Machine Hard Drive (Leave it by default or don't go lower then 20GB)

![image-20230114000915463](https://iili.io/HYWE5rv.png)

Click on Next

![image-20230114000935090](https://iili.io/HYWEY2R.png)

And then click on Finish.



Congratulation you have create the Virtual Machine. 

Now we need to do some modification. 



So were you are here click on Open VM Directory

![image-20230114001122539](https://iili.io/HYWEa7p.png)

And select the VMX File open it with the Notepad or the editor of your choice. 



Go all the way down and paste that : 

`smc.version = "0" `

`cpuid.0.eax = "0000:0000:0000:0000:0000:0000:0000:1011" `

`cpuid.0.ebx = "0111:0101:0110:1110:0110:0101:0100:0111" `

`cpuid.0.ecx = "0110:1100:0110:0101:0111:0100:0110:1110" `

`cpuid.0.edx = "0100:1001:0110:0101:0110:1110:0110:1001" `

`cpuid.1.eax = "0000:0000:0000:0001:0000:0110:0111:0001" `

`cpuid.1.ebx = "0000:0010:0000:0001:0000:1000:0000:0000" `

`cpuid.1.ecx = "1000:0010:1001:1000:0010:0010:0000:0011" `

`cpuid.1.edx = "0000:0111:1000:1011:1111:1011:1111:1111" `

`smbios.reflectHost = "TRUE" `

 ` hw.model = "MacBookPro14,3" `

`board-id = "Mac-551B86E5744E2388"`

After to have paste it just save the file. 



Go Back on VMware and select your MacOS ISO. 



And click on Start.



If everything go as expected you Will see that screen after the loading



![image-20230113235815654](https://iili.io/HYWE2Lu.png)

Congratulation you have successfully configure your VM for working with MacOS and your AMD Processor.

If your are not sur of were your are going, you can use my VMX template. 



Have Fun