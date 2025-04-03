# How to access the BBV. 

From a wired connection (on my macOS), figure out which of the
`/dev/...usbmodem... ` connection correspond to the beagleboneV fire when you 
connect it onto a usb port
`ls /dev/` and find what's changing between when the beaglebone is connected 
and when it is not. If you are unsure you can also look at the kernel log (Ubunut) with `dmesg | grep -i usb` and see where the BeagleV has been registered
Then from the terminal 
```
screen /dev/...usbmodem... 9600
```
To start a session.
Once you are connected, use username:beagle and password:temppwd to logon
Then you can finally gget the IP of the board with: 
```
ifconfg
```
And you should be in business
