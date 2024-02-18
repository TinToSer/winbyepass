# win-bye-pass
A very simple Non destructive solution to reset Windows Password


Download iso from below link

https://drive.google.com/file/d/1meeXs9xO36O3no_h78XOASiiHkVMNOSZ/view?usp=sharing


Steps:-

[For Hardware]

  1. Burn the iso to a pendrive to make it bootable using rufus(https://rufus.ie/en/) or the most smartest way of Ventoy(https://www.ventoy.net/en/download.html)
  2. Boot from the pendrive/iso (just google for your harware device about shortcut, F12,F9 etc, in Virtual machine F12 works).
  3. After booting you will see windows is starting and then rebooting again, sometimes says fail to reboot Don't panic just restart. You will observe something like this
     
     ![image](https://github.com/TinToSer/winbyepass/assets/52107530/c710c39d-6b75-4db5-b729-5021732592f8)

  4. Now when you are at login screen then click on ease of access button shown below and then on On screen keyboard.
     ![image](https://github.com/TinToSer/winbyepass/assets/52107530/9e203555-4326-4eb9-884e-1e9d21bb87b8)
     ![image](https://github.com/TinToSer/winbyepass/assets/52107530/662fa2f4-5b23-4509-9ae3-f996d382b4cc)
     
  6. You will see that a command window opens, remember it is with highest privilege level(**nt authority\SYSTEM**) **so you can do anything**:).
  7. To see usernames type
     
     ```net user```

     ![image](https://github.com/TinToSer/winbyepass/assets/52107530/355d4b38-a6e2-415d-9df0-f53e0e7ab621)

     
  8. To remove/set password type
     
     ```net user joker 123```
     
     here "joker" is my targetted username and 123 is the password I am setting, press enter and then you see "Completed successfully" message in the command window, Now close the command window and login with password 123 in joker account
     
     OR
     
     ```net user joker *```
     
     here "joker" is my username I am targeting and 123 is the password I am setting
     When you enter above command it will ask to enter password, don't write anything, press enter and then you see "Completed successfully" message in the command window,Now close the command window and click
     to login :)
     
     ![image](https://github.com/TinToSer/winbyepass/assets/52107530/9328c429-d9e9-4e26-8291-daa04dc8cf72)

  10. After your job is done then either Microsoft windows will automatically remove the backdooring by deleting the registry key we modified or you can also do it by running the below command in cmd as an Admin.
      But before that make sure if registry already removed by microsoft, to do that type below in windows search box and open "On screen keyboard", see whether "On screen keyboard" opens or command window. If
      command window opens then it means Microsoft has not removed the registry on its own :).
      
      ```reg delete "HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Image File Execution options\osk.exe" /f > nul```

[For Virtual machine, ex Vmware]

![image](https://github.com/TinToSer/winbyepass/assets/52107530/117e4826-107b-4805-8676-36cac8155cd8)

And then boot from iso and follow above process for [Hardware] from Step 2.


[Whole Science behind]

It's just a simple registry technique, which makes cmd.exe as a debugger to "on screen keyboard", since you are at login screen so presented with highest privilege command window
     


*********************************************************************Sharing is caring, as usual "Tinkering Bytes To Disintegrate Burdens***************************************************************


Thanks to below which excited me for Fun:-

https://pentestlab.blog/2020/01/13/persistence-image-file-execution-options-injection/

https://learn.microsoft.com/en-us/windows-hardware/manufacture/desktop/winpe-create-usb-bootable-drive?view=windows-11
