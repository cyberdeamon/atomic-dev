# Introduction #

iEMW is an incomplete iOS Emulator designed for Windows. Most of the standard applications are missing. And this software is not recommended. The application icons were taken from:

- http://www.iconseeker.com/search/Phone/8

_**The app icons do not belong to me!**_

# Prerequisites #
  * .NET Framework
  * Windows XP or higher
  * Some basic iOS experience

## Issues ##
# Framework Error:
  * Install .NET Framework from Microsoft
# Calculator crashes!
  * Make sure you are using reasonable numbers. This is not a graphing calculator!

# License #

Copyright (c) 2012, Atomic-Dev
All rights reserved.

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.
Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED
WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR
A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY
DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO,
PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION)
HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING
NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

# Browser History #

### Declarations ###
```
 public string data = null;
        public string safe_directory = Environment.GetFolderPath(Environment.SpecialFolder.MyDocuments) + "/iEMW/";
        public browser()
        {
            InitializeComponent();
            search.SendToBack();            
            this.AcceptButton = search;          
            if (!Directory.Exists(safe_directory))
                Directory.CreateDirectory(safe_directory);
            if (File.Exists(safe_directory + "history.log") == false)
            {
                using (StreamWriter sw = new StreamWriter(safe_directory + "history.log"))
                {
                   sw.Dispose();           /* I don't want it no more... (as in Six Blade Knife by Dire Straits! KILLER BASS LINE!) */
                }
            }
        }
```

### Document Completed ###
```
string url = urlBox.Text;
            int sysd = 0;
            if (url != null && url != "")
                sysd = url.Length;
            
                using (StreamReader sr = new StreamReader(safe_directory + "history.log"))
                {
                    string file = sr.ReadToEnd();
                    string[] filelines = file.Split('\n');
                    int i = 0;
                    var ex = from s in filelines
		                     select s;
                    sr.Dispose();
                    int c = ex.Count();
                    for (i = 0; i < c; i++)
                    {
                        string ltext = filelines[i];
                        if (urlBox.Text == ltext)
                            break;
                        else
                        {
                            break;
                        }
                    }
                    
                }

                data += "\n";
                data += webBrowser1.Url;
```

The browser checks the file to see if the current url is already written to the file. If this is false (0) it is written to the next line.

# Calculator #

Code that allows the calculator to function:

### Functions ###
```

private void subtract_Click(object sender, EventArgs e)
        {
            holder = Int32.Parse(result.Text);
            total = holder;
            mode = "sub"; 
            result.Text = "0";
        }

        private void addition_Click(object sender, EventArgs e)
        {
            mode = "add";
            holder = Int32.Parse(result.Text);
            total += holder;
            result.Text = "0";            
        }

        private void multiply_Click(object sender, EventArgs e)
        {
            mode = "mul";
            holder = Int32.Parse(result.Text);            
            if (total == 0)
                total = holder;
            else total *= holder;
            result.Text = "0";
        }

        private void divideBtn_Click(object sender, EventArgs e)
        {
            mode = "div";
            holder = Int32.Parse(this.result.Text);
            if (total == 0)
                total = holder;
            else total /= holder;
            this.result.Text = "0";
        }

```

### Calculate ###
```
private void equals_Click(object sender, EventArgs e)
        {
            try
            {
                holder2 = Int32.Parse(result.Text);
            } catch
            {
                ;
            }
            if (mode == "add")
            {
                total += holder2;
            }
            else if (mode == "sub")
                total = (total - holder2);
            else if (mode == "mul")
                total *= holder2;
            else if (mode == "div")
                total /= holder2;

            result.Text = total.ToString();
        }

```

# Opensource #
### Public ###
<ul>
<li><b>Through GitHub GUI:</b> <a href='http://github.com/atomic-dev/iEMW/'><a href='http://github.com/atomic-dev/iEMW/'>http://github.com/atomic-dev/iEMW/</a></a></li>
<li><b>Through Git:</b> <code>git clone git://github.com/Atomic-Dev/iEMW.git</code></li>
</ul>
### Contributor ###
<ul>
<li>
<b>Through Git:</b> <code>git clone git@github.com:Atomic-Dev/iEMW.git</code>
</li>
</ul>