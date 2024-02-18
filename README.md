# win-bye-pass
A very simple Non destructive solution to reset Windows Password




Steps:-
  1. Burn the iso to a pendrive to make it bootable using rufus(https://rufus.ie/en/) or the most smartest way of Ventoy(https://www.ventoy.net/en/download.html)
  2. Boot from the pendrive(just google for your harware device about shortcut, F12,F9 etc).
  3. After booting you will see it starting and then rebooting normal.
  4. Now when you are at login screen then click on ease of access button shown below and then on On screen keyboard.
     ![image](https://github.com/TinToSer/winbyepass/assets/52107530/9e203555-4326-4eb9-884e-1e9d21bb87b8)
     ![image](https://github.com/TinToSer/winbyepass/assets/52107530/662fa2f4-5b23-4509-9ae3-f996d382b4cc)
  6. You will see that a command window opens, remember it is with highest privilege level(nt authority\SYSTEM) so you can do anything:).
  7. To see usernames type
     ~~~net user
  8. To remove/set password type
     ``` net user joker 123
     here "joker" is my username I am targeting and 123 is the password I am setting, now login with password 123 in joker account
     OR
     ``` net user joker *
     here "joker" is my username I am targeting and 123 is the password I am setting
     When you enter above command it ask to enter password, don't write anything simply press enter and then you see successful message,Now close the command window and click to login :)
     ![image](https://github.com/TinToSer/winbyepass/assets/52107530/9328c429-d9e9-4e26-8291-daa04dc8cf72)

     



Thanks to below for sharing knowledge:-

https://pentestlab.blog/2020/01/13/persistence-image-file-execution-options-injection/

https://learn.microsoft.com/en-us/windows-hardware/manufacture/desktop/winpe-create-usb-bootable-drive?view=windows-11
