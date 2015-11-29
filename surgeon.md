# Introduction #

Surgeon is the GUI / patcher for iOS's iBSS and iBEC.


# Details #

## How does it work? ##

The GUI is written in Visual Basic (pardon my laziness), and runs the python patcher via Command Prompt.

## GUI ##

![http://kryptonx.webs.com/img/surgeon.png](http://kryptonx.webs.com/img/surgeon.png)

## Python Script ##
```
# Copyright (C) 2011 KryptonX

# This program is free software: you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation, either version 3 of the License, or
# (at your option) any later version.

# This program is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.

# You should have received a copy of the GNU General Public License
# along with this program.  If not, see <http://www.gnu.org/licenses/>.

import urllib2
import time
import patch
import shutil
import os
import datetime
import math
import urllib
from array import array
import sys

patchfile = open('kry1' + '.iBSS', 'w')
filehandle = urllib.urlopen('URL HERE, I CANT PROVIDE THE URL!')
for lines in filehandle.readlines():
                                str(lines)    
                                patchfile.write(lines)

if (len(sys.argv) > 1):
    if(sys.argv[1] == "-i4" ):
            patchfile = open('n90ap' + '.iBSS', 'w')
            filehandle = urllib.urlopen('URL HERE, I CANT PROVIDE THE URL!')
            for lines in filehandle.readlines():
                                str(lines)    
                                patchfile.write(lines)
                                
            print "Done"                            
    elif(sys.argv[1] == '-ipt4' ):            
            patchfile = open('n81ap' + '.iBSS', 'w')
            filehandle = urllib.urlopen('URL HERE, I CANT PROVIDE THE URL!')
            for lines in filehandle.readlines():
                    str(lines)    
                    patchfile.write(lines)
                                
    elif(sys.argv[1] == '-i3gs'):
        patchfile = open('n88ap' + '.iBSS', 'w')
        filehandle = urllib.urlopen('URL HERE, I CANT PROVIDE THE URL!')
        for lines in filehandle.readlines():
                                str(lines)    
                                patchfile.write(lines)
    elif(sys.argv[1] == '-ipt3'):
           patchfile = open('n18ap' + '.iBSS', 'w')
           filehandle = urllib.urlopen('URL HERE, I CANT PROVIDE THE URL!')
           for lines in filehandle.readlines():
                                str(lines)    
                                patchfile.write(lines)
    elif(sys.argv[1] == '-ipad'):
           patchfile = open('k48ap' + '.iBSS', 'w')
           filehandle = urllib.urlopen('URL HERE, I CANT PROVIDE THE URL!')
           for lines in filehandle.readlines():
                                str(lines)    
                                patchfile.write(lines)         
            
     


def device():
        print "-i4\t\tiPhone 4"
        print "-ipt4\t\tiPod 4"
        print "-i3gs\t\tiPhone 3Gs"
        print "-ipt3\t\tiPod 3G"
        print "-ipad\t\tiPad"
        # Now obtain the raw_input
        device = raw_input("Model: ")
        if device == '-i4':             #iPhone 4
                return define.n90ap
        elif device == '-ipt4':          # iPod 4
                return define.n81ap
        elif device == '-i3gs':         # iPhone 3Gs        
                return define.n88ap
        elif device == '-ipt3':          # iPod 3
                return define.n18ap
        elif device == '-ipad':         # iPad
                return define.k48ap
        else:
                print "Unavailable device"



def check_connection():
                 try:
                        urllib2.urlopen("http://kryptonx.webs.com", timeout=2)
                 except urllib2.URLError:
                        print 'You do not seem to be connected to the internet'
                        print 'This could cause a problem when creating the PATCH file.'
        
                
```


