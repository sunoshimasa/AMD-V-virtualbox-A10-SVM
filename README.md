# AMD-V-virtualbox-A10-SVM
Memo AMD A10 AMD-V bios SVM run virtualbox ubuntu 14.04 x64 vhd



Skip to content
Search or jump to…

Pull requests
Issues
Marketplace
Explore
 
@sunoshimasa 
sunoshimasa
/
Tuesday-transmitter
1
00
 Code
 Issues 0
 Pull requests 0 Actions
 Projects 0
 Wiki
 Security 0
 Insights
 Settings
Tuesday-transmitter/virtualbox_amd_a10_amd-v
@sunoshimasa sunoshimasa Create virtualbox_amd_a10_amd-v
e25b87c 8 hours ago
14 lines (8 sloc)  1.56 KB
  
https://h30434.www3.hp.com/t5/Notebook-Boot-and-Lockup/HP-Probook-AMD-A10-Radeon-R6-64-bit-Windows-10-Home/m-p/5910829/highlight/true#M103589

Now for those like me trying to use VB(Oracle VirtualBox ) for using Linux VM under Windows-10 Home And similar HP Laptop ( AMD A10-8700p R6 Radeon) :  I did following to resolve the issue of 64 bit option not being shown in VB:

-- First thing is that this issue is related to BIOS settings and so we need to get into BIOS Menu and so re-start the laptop and keep pressing F2 , it will show HP logo a couple of times and then we can see BIOS diagnostics menu. We need to EXIT from this top Menu ( EXIT --> YES/NO --> Select NO, which will take to next level of Menu).

-- In the Next BIOS Menu, Select ADVANCED option at Top ( use Arrow keys to navigate ). Under ADVANCED Option you can see "svm CPU Virtualization"  with its checkbox as un-checked.   Check this Option and then SAVE and Exit from BIOS Set Up. The Booting of Laptop continues.

-- Shutdown Laptop as soon as it started after BIOS Change as above, and then re-start it, now we should be able to see 64 bit options active in VB Drop-Down.

-- My HP Laptop came with two good set-up utilities from HP called Support Assistant and HP TOuchPoint. These were very helpful initially to upgrade BIOS and other software versions as well as researching the issue of Virtual Box.

start command prompt with administrator rights and type 'bcdedit /set hypervisorlaunchtype off'
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\DeviceGuard\Scenarios\HypervisorEnforcedCode Integrity\Enabled=0
© 2020 GitHub, Inc.
Terms
Privacy
Security
Status
Help
Contact GitHub
Pricing
API
Training
Blog
About
