Below is a guide to completing the activity criteria contained within Bud/Cloud Academy. 

Throughout the guidance, I will give examples of the logic but not give full examples of code for obvious reasons. I have given examples for Task 1, part 1 but this will not extend past this part. Please refer to task exercises and PowerPoint slides for further guidance on the exact code. In some examples, I will give a small portion of a command and in another similar example, I will just refer to it. 

My recommendation is to use PowerShell ISE to write the code. For the below tasks, you should NOT have to run the application as an administrator. Ensure that you use the environment within https://qa.learnondemand.net/

- **Task 1: Audit a local machine**  
  - **Instructions (P1, P6, K3, K4, K10)**  
    - Demonstrate your understanding of the use of the PowerShell Pipeline.  
    - Create a PowerShell script to filter, sort, select, and format relevant data and properties.  
  - **Focus**  
    - This task is based on Days 1 & 2.  
    - Examples of code will be provided to support the task.  

- **Part 1**  
  - Provide an example PowerShell script that audits a local machine.  
  - You may audit:  
    - Local services (status/start type)  
    - Local processes (top N processes)  
    - Local disk volumes (free space)  
  - Use at least two of the following commands:  
    - `Sort-Object` (Sorting)  
    - `Where-Object` (Filtering)  
    - `Select-Object` (Selecting)  
    - `Format-Table`, `Format-Wide`, `Format-List` (Formatting)  

- **Part 2: Personal Case Study**  
  - Your case study should include:  
    - Where the script is stored (local/remote) and why.  
    - A copy of the completed script.  
    - An example of the output.

- **Task 2: Accept user input**  
  - **Instructions (K3, K4, K5, K7, K10, P2, P4, P6)**  
    - Demonstrate understanding of scripts that accept user input instead of hardcoded values.

- **Part 1**  
  - Provide an example PowerShell script that audits remote machines.  
  - Steps:  
    1. Accept user input for computer names using variables.  
    2. Use appropriate variable types and handle multiple entries.  
    3. Add comments in the script (single-line and block comments).  
    4. Output data to a file (txt, csv, xml, json, or html).  
  - Be ready to explain the choice of output file type.  

- **Part 2: Personal Case Study**  
  - Include:  
    - Script storage location.  
    - Script/command.  
    - Output screenshot from PowerShell.

- **Task 3: Functions**  
  - **Instructions (K3, K4, K8, K9, K10, P2, P3, P6)**  
    - Demonstrate knowledge of PowerShell Functions.  
    - Provide responses to knowledge questions or prepare for a discussion with DLC.  
  - **Knowledge Questions**  
    1. Difference between a basic and advanced function.  
    2. Ways to test a function in a script.  
    3. How to load a function into memory without calling it in a script.

- **Task 4: Modules**  
  - **Instructions (K3, K4, K5, K6, K10, K11, P2, P4, P6, P7)**  
    - Create two functions and save them as a PowerShell module.  
    - Functions should automatically load into memory when called.  
  - **Part 1**  
    - Create a PowerShell Script Module with two functions:  
      - One basic function.  
      - One advanced function with parameter input, dynamic comments, and testing capabilities.  
    - Confirm the module storage location.  
  - **Part 2: Personal Case Study**  
    - Evidence of module storage.  
    - Proof of module loading into memory (`Get-Module -All`).  
    - Completed script with both functions.  
    - Input and output examples.

- **Task 5: Summary of scripting knowledge and skills**  
  - **Instructions (K1, K2, P5)**  
  - High-level questions:  
    1. Define the general role of batch scripts in IT support.  
    2. Explain the main features of batch scripts.  
    3. Describe the approval process for deploying scripts in a live environment.

