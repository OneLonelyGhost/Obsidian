---
title: "Reviewing batch script performance - Comments, approval, and scripting performance | ITS SQ | Lesson | QA Platform"
source: "https://app.qa.com/course/comments-approval-and-scripting-performance-itsl8-sq-a31-1698/reviewing-batch-script-performance/?context_id=12176&context_resource=lp"
author:
  - "[[QA Platform]]"
published:
created: 2025-01-08
description: "Reviewing batch script performance - Comments, approval, and scripting performance | ITS SQ | lesson from QA Platform. Start learning today with our digital training solutions."
tags:
  - "clippings"
---
Fast program performance makes everything you do on your computer or device happen quickly and smoothly, saving you time and reducing frustration.

This level of performance can be challenging to achieve if using scripting languages because they follow a step-by-step approach to execute commands, which can be sluggish especially with repeated tasks. 

While scripting languages may be more user-friendly for basic tasks and automation, if you need performance, then you should consider writing your program in a compiled language like C.  

Despite this, there are still some tricks available to speed up the performance and efficiency of bash shell scripts, which at the very least lead to other programs getting more time to run.

### Bash shell performance tricks

Here are some simple tricks to improve the performance of your bash shell scripts:

**Avoid useless use of commands:** No need for the grep command as the awk command can also do string/pattern matching. 

```
Ps -ef | grep ‘[s]shd’ | awk ‘{print $2}’ 
```

**Replace with #1:** One less process fork. 

```
Ps -ef | awk ‘/[s]shd/{print $2}’ 
```

**Replace with #2:** One less process fork again. 

```
Pgrep ‘sshd’ 
```

**Use internal shell features #1:** The cat command is an unnecessary fork (loading and executing of a process).

```
kill -HUP $(cat /var/run/rsyslog.pid) 
```

**Replace with:** The if-else, read, kill, shell redirection (<), variable substitution ($pid) and echo command are all built-in shell features. 

```
If read pid < /var/run/rsyslog.pid 
```
```
then  
```
```
    kill -HUP $pid 
```
```
else 
```
```
    echo “rsyslog not running” 
```
```
fi 
```

**Use internal shell features #2:** The external system command basename removes the directory part of the string and returns the filename only. 

```
Pathname=”/var/log/messages” 
```
```
filename=“$(basename $pathname)” 
```

**Replace with:** The ##\*/ removes the largest string from the LHS matching all chars up to and including the last / from the pathname. It’s a built inbuilt-in shell variable feature. 

```
pathname=”/var/log/messages” 
```
```
filename=“${pathname##*/}” 
```

**Use internal shell features #3:** Filter the output of the ps command to extract the 2nd field (PID) and send the HUP signal to terminate it. **Four** process forks required. 

```
kill -HUP $(ps -ef | grep ‘bash’ | tr -s  \ 
```
```
           ‘\040\011’ | cut -d’ ‘ -f2) 
```

**Replace with:** The built-in shell set command automatically splits the output line and assigns the fields to built-in shell parameters $1, $2, $3 etc. **Two** less process forks. 

```
set $(ps -ef | grep ‘bash’) 
```
```
kill -HUP $2 
```

**Use internal shell features #4:** One command, but **three** process forks to generate and store the day, month, and year in three shell variables. 

```
Day=”$(date +%d)” 
```
```
month=”$(date +%m)” 
```
```
year=”$(date +%Y)” 
```

**Replace with #1:** Only **one** process to generate date and shell variable string extraction to extract day, month, and year. 

```
today=”$(date +%d-%m-%Y)” 
```
```
day=”${today:0:2}” 
```
```
month=”${today:3:2}” 
```
```
year=”${today:6:4}” 
```

**Replace with #2:** Still only **one** process fork but using the shell Input Field Separator and set command to split string into three strings. 

```
export IFS=”/” 
```
```
set $(date +%d/%m/%Y) 
```
```
day=”$1” 
```
```
month=”$2” 
```
```
year=”$3” 
```

**File handling:** Using pipes for reading a file results in both sides running in their own sub-shell (**two** process forks). It works but variables set in loop are not visible outside! 

```
cat /etc/passwd | while read line 
```
```
do 
```
```
    echo “$line” 
```
```
done 
```

**Replace with #1:** Use the built-in shell redirection feature to open the file once, read one line at a time with loop, and then close file once. **Zero** process forks. All built-in features! 

```
while read line 
```
```
do 
```
```
    echo “$line” 
```
```
done < /etc/passwd 
```

**Replace with #2:** Use the built-in shell IFS variable to automatically split the line and assign each to shell named variable.

```
while IFS=”:” read login x uid gid name home shell 
```
```
do
```
```
    echo -e “$login\t$uid\t$shell”
```
```
done < /etc/passwd 
```

When you're ready, select **Next** to continue.