## Introduction ##

iDeviceToolKit is a collection of iPhone interactive opensource software
(for the credits view credits.txt) for the iPhone, iPad and iPod Touch. This is a COLLECTION of software.


&lt;hr /&gt;


## Features ##
```
-a              Activate lib-x-mobiledrive
-b              Create iBSS (requires Python)
-c              Create iBEC (required Python)
-d              ** Grab device info.
-f              ** Save info to file

-h              Access the iPad array
-i              Access the iPhone array
-j              Access the iPod array

-l [iBoot]      ** Load a new iBoot
-m              ** Set auto-boot to true
-n              ** Reset iBoot

-e              * DFU Helper
-o              Kill iTunes
-q              * Enter Recovery (.NET Framework)

-s              ** Execute steaks4uce exploit
-x              ** Execute limera1n exploit

-w              Atomic-Dev
```


&lt;hr /&gt;


## Running ##
1. Run the 'start.bat' file in the root directory.
<br />
2. type 'idevicetoolkit' then 'Enter' to view the list of arguments.


&lt;hr /&gt;


## Legend ##
```
- [Optional]
- <Necessary parameter>
- * (Requires a connected device)
- ** (requires a conected device in DFU or Recovery)
```


&lt;hr /&gt;


## Prerequisites ##
<pre>
- iTunes 10.0 or later.<br>
- Python must be installed for the patchers<br>
- .NET framework must be installed for the 'Enter Recovery' feature.<br>
</pre>


&lt;hr /&gt;


## Credits ##
<pre>
Credits:<br>
<br>
Atomic-Dev Team, 2009 - 2011 -- Thanks to all members for your help and contribution!<br>
<br>
Additional Credits:<br>
<br>
Syringe Library:<br>
by Chronic-Dev Team<br>
<br>
libiRecovery:<br>
by Chronic-Dev Team<br>
<br>
limera1n:<br>
exploit by posixninja<br>
vulnerability by geohot<br>
<br>
steaks4uce:<br>
exploit by posixninja<br>
vulnerability by pod2G<br>
---------------------------<br>
(* Most utilize the Syringe library *)<br>
<br>
DFU:<br>
by KryptonX<br>
<br>
plutonium:<br>
by KryptonX<br>
<br>
dllmanager (calls functions):<br>
by KryptonX<br>
<br>
x-irecovery:<br>
by KryptonX<br>
<br>
k-irecovery:<br>
by KryptonX<br>
<br>
iBSS patcher:<br>
by KryptonX & spyyder<br>
<br>
iBEC patcher:<br>
by KryptonX & spyyder<br>
<br>
grey:<br>
by KryptonX & Al.<br>
<br>
iBoot.exe:<br>
* THIS IS A SCRIPT COMPILED TO AN EXE<br>
</pre>


&lt;hr /&gt;


## Source-code ##
### Public ###
**Through Git:** ` git clone git://github.com/Atomic-Dev/iDeviceToolKit.git `
<br />
**From GitHub:** <a href='http://github.com/atomic-dev/idevicetoolkit/'><a href='http://github.com/atomic-dev/idevicetoolkit/'>http://github.com/atomic-dev/idevicetoolkit/</a></a>
### Contributor ###
**Through Git:** ` git clone git@github.com:Atomic-Dev/iDeviceToolKit.git `


&lt;hr /&gt;


## Argument Vector ##
```
t_atomic_xval arg = argc;    

   int c, except = 0, number = 0, found = 0;   
   /* Parsing */
   
   if (arg < 2) {
           usage(); 
   } else {
   
   while (--argc > 0 && (*++argv)[0] == '-') 
                                 
         c = *++argv[0];
```


