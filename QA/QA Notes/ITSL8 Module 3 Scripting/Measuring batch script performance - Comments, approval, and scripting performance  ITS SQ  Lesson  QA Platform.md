---
title: "Measuring batch script performance - Comments, approval, and scripting performance | ITS SQ | Lesson | QA Platform"
source: "https://app.qa.com/course/comments-approval-and-scripting-performance-itsl8-sq-a31-1698/measuring-batch-script-performance/?context_id=12176&context_resource=lp"
author:
  - "[[QA Platform]]"
published:
created: 2025-01-08
description: "Measuring batch script performance - Comments, approval, and scripting performance | ITS SQ | lesson from QA Platform. Start learning today with our digital training solutions."
tags:
  - "clippings"
---
It is possible to measure the execution time in Bash, PowerShell, and Python, which could be used to benchmark any changes to a script. If the change makes the program faster, then keep it, or discard it if this makes the program slower.

In this step, you will see how all three languages can measure how long a script, function or block of code takes to run. 

You will also see how Python enables you to analyse and provide statistics on the performance of each function call within a script.

### Bash shell 

To measure performance, you could use the built-in shell time command or the GNU Linux /usr/bin/time command. They give similar information on the total elapsed time, time taken for just the user program, and time used by the kernel. In this example, there are two scripts with identical behaviour to compare. One script is poorly written (demo\_bad) and the other uses shell built-in features (demo\_good). Both scripts use a loop to repeat the commands 10 times.

**demo\_bad** 

```
#! /bin/bash 
```
```
# Author: JBloggs 
```
```
# Description: Measure the Performance of a poorly 
```
```
# written script vs a well written script 
```

```
for i in {1..10} 
```
```
do 
```
```
    day="$(date +%d)" 
```
```
    month="$(date +%m)" 
```
```
    year="$(date +%Y)" 
```

```
    echo -e "Day=$day, Month=$month, Year=$year" 
```

```
    # Display Login information. 
```
```
    cat /etc/passwd | while read line 
```
```
    do 
```
```
        echo -e "$line" 
```
```
    done 
```

```
    # kill any cat commands running. 
```
```
    kill -HUP $(ps -ef | grep '[c]at ' | tr -s '\040\011' | cut -d' ' -f2) 2> /dev/null 
```
```
done 
```

**demo\_good** 

```
#! /bin/bash 
```
```
# Author: JBloggs 
```
```
# Description: Measure the Performance of a poorly 
```
```
# written script vs a well written script 
```

```
for i in {1..10} 
```
```
do 
```
```
    today="$(date +%d/%m/%Y)" 
```
```
    day="${today:0:2}" 
```
```
    month="${today:3:2}" 
```
```
    year="${today:6:4}" 
```

```
    echo -e "Day=$day, Month=$month, Year=$year" 
```

```
    # Display Login information. 
```
```
    while read line 
```
```
    do 
```
```
        echo -e "$line" 
```
```
    done < /etc/passwd 
```

```
    # kill any cat commands running. 
```
```
    kill -HUP $(pgrep 'cat') 2> /dev/null 
```
```
done 
```

### Measure performance (bash shell)

```
[qa@rocky ~ ]$ time ./demo_bad > /dev/null 
```
```
real: 0m0.349s 
```
```
user: 0m0.147s 
```
```
sys: 0m0.233s 
```

```
[qa@rocky ~ ]$ time ./demo_good > /dev/null 
```
```
real: 0m0.138s 
```
```
user: 0m0.047s 
```
```
sys: 0m0.087s 
```

As you can see above, the shell built-in time command reports that the demo\_good script is at least 2.5 times as fast as the demo\_bad script. A good result.

### Python 

There are several modules for measuring performance in the Python Standard Library including the timeit and cProfile modules.  

In this example, the cProfile module will be used to analyse and compare how well two near identical scripts perform. Both scripts have been designed to search for a Regex Pattern (strings of 19 characters in length) in a dictionary file and display lines matched. One script recompiles the pattern for every line (45,404 times) and the other pre-compiles the pattern only **once**.

**search\_regex\_recompile\_many.py** 

```
#! /usr/bin/env python3 # Author:      Joe Bloggs # Description: Search for a Regex pattern but recompile pattern  # for every line in file. """     Search for a Regex Pattern in a file. """ import sys import re  def search_pattern(pattern=r"^.{19}$", file=r"C:\labs\words"):     """ Search for Regex pattern in a text file """     lines = 0     with open(file, mode="rt") as fh_in:         for line in fh_in:             m = re.search(pattern, line) # Recompile pattern             if m:                 lines += 1 # Increment number of lines matched.                 print(f"Matched {m.group()}")     return lines def main():     num_lines = search_pattern()     print(f"Lines matched = {num_lines}")     return None if __name__ == "__main__":     import cProfile     cProfile.run("main()")  # Analyse performance of function 
```

```
search_regex_recompile_once.py 
```
```
#! /usr/bin/env python3 # Author:      Joe Bloggs # Description: Search for a Regex pattern but compile pattern  # ONCE only """     Search for a Regex Pattern in a file. """ import sys import re  def search_pattern(pattern=r"^.{19}$", file=r"C:\labs\words"):     """ Search for Regex pattern in a text file """     lines = 0 
```
```
    reobj = re.compile(pattern) # Compile pattern ONCE only     with open(file, mode="rt") as fh_in:         for line in fh_in:             m = reobj.search(pattern, line) # Use compiled pattern             if m:                 lines += 1 # Increment number of lines matched.                 print(f"Matched {m.group()}")     return lines  def main():     num_lines = search_pattern()     print(f"Lines matched = {num_lines}")     return None if __name__ == "__main__":     import cProfile     cProfile.run("main()")  # Analyse performance of function 
```

#### Measure performance (Python) 

By just making one change in the script, the programmer was able to compile the Regex pattern once rather than 45,404 times with a performance improvement of 3.3. Another good result.

### PowerShell

This language has built-in cmdlet called Measure-Command which can be used to analyse the time it takes a command or script block to execute. In this simple example, the cmdlet will be used to measure the time it takes to iterate through piped objects into a for loop with and without output.

#### Measure time for block with no output 

![Output of the Measure-Command cmdlet with no output indicating the process took 2 ms.](https://assets.cloudacademy.com/bakery/media/uploads/entity/blobid1-2d9b7025-a8fa-4976-a8cd-fad926c897f3.png)

#### Measure time for block with output 

![Output of the Measure-Command cmdlet with output indicating the process took 5ms.](https://assets.cloudacademy.com/bakery/media/uploads/entity/blobid3-73557905-0f24-419e-898b-e6710c08b2db.png)

You can see that the script block with no output is faster.

When you’re ready, select **Next** to continue.