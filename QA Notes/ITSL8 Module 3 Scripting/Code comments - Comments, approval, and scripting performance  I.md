---
title: "Code comments - Comments, approval, and scripting performance | ITS SQ | Lesson | QA Platform"
source: "https://app.qa.com/course/comments-approval-and-scripting-performance-itsl8-sq-a31-1698/code-comments/?context_id=12176&context_resource=lp"
author:
  - "[[QA Platform]]"
published:
created: 2025-01-08
description: "Code comments - Comments, approval, and scripting performance | ITS SQ | lesson from QA Platform. Start learning today with our digital training solutions."
tags:
  - "clippings"
---
It is easy to spot a program written by an experienced programmer. It will be easy to read, easy to understand, clearly laid out with good use of indentation and spacing, and will be appropriately commented on. 

Remember, not all code requires comments. For example, a loop or if statements can be pretty self-explanatory. However, if you have some tricky code or ever pause to think about the code you are writing, then it should have a comment. 

Comments can be inline where they are tagged on the end of the command, but most batch scripting languages prefer having a comment on its own line **above** the code. You should use as many comment lines as required. 

Spend some time reviewing the examples below.

### Bash shell script (example)

```
#! /bin/bash # Author:  JBloggs, email@qa.com # Version: 1.0 # Description: Terminate User processes  while true do     clear     echo -e “Enter a username (or q=quit): \c”     read user      [[ $user == [qQ] ]] && break      echo -e “Enter a process name to terminate: \c”     read procname      # Extract PIDs from ps command (2nd field) and     # send HUP signal to terminate select processes for user     kill -HUP $(ps -f -u”$user” | awk “/$procname/{print \$2}”)      echo -e “Press any key to continue\c”     read -n1 done  # Exit script with 0 errors. exit 0   
```

### Python script (example)

```
#! /usr/bin/env python3 # Author:      Joe Bloggs # Description: This program will kill user processes by name """     This program will send the TERM signal to user processes """ import sys import os import signal import psutil  def main(): 
```
```
    """ Prompt and kill user processes """      while True:         procname = input("Enter process name to kill: ")         if procname == "q": break          # Iterate through all processes to find process name.         for proc in psutil.process_iter():             if procname.lower() in proc.name().lower():                 print(f"Killing {procname} with PID {proc.pid}")                 # Send TERM signal to processes.                 os.kill(proc.pid, signal.SIGTERM)     return None # Only Execute if ran directly as a program. if __name__ == "__main__":     main()     sys.exit(0) # Exit script with 0 errors. 
```

### Comments for change

If you have to modify existing code, it is usually better to comment out the previous code (using single or multi-line comments) rather than delete the lines. This will make it is easier for you to reinstate the code if required.  

Always add a comment with a timestamp and your name to any changes you make and the reason for the change. This provides traceability if a feature stops working. 

Ensure that your comments and code match! If they don’t, it’s likely that neither are correct.  

#### Commenting changes (example) 

```
    # Username input not required. Jbloggs 01/04/2023     # echo -e “Enter a username (or q=quit): \c”     # read user      # [[ $user == [qQ] ]] && break     echo -e “Enter a process name to terminate: \c”     read procname     # Extract PIDs from ps command (2nd field) and     # send HUP signal to terminate select processes 
```
```
    # kill -HUP $(ps -f -u”$user” | awk “/$procname/{print \$2}”) 
```
```
    kill -HUP $(ps -f | awk “/$procname/{print \$2}”) 
```

### Coding style

Companies and teams will have style guides for the programming languages they use. These guides help with how to format code, use spacing, name variables, and add comments. You should seek out these guides and follow them, even if you disagree with them. Some languages like Python have their own widely followed guides, like [PEP 8](https://peps.python.org/pep-0008/).

### Python DocStrings

To help others (and yourself) understand your Python code, you can use special comments called DocStrings.  

These are multi-line comments using triple-quoted strings (single or double) which are read by the Python built-in help() function. 

Each program, module, class, function, or method should have a Docstring at the start of each structure and before any code and provides additional documentation over standard comments. 

#### Python script (example) 

```
#! /usr/bin/env python3 # Author:      Joe Bloggs # Description: This program will kill user processes by name "“"”"”     This program will send the TERM signal to user processes "“"”"” import sys 
```

When you’re ready, select **Next** to continue.