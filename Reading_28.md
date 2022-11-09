Dean Weiss
9 November 2022

# Log Tampering

### The process
There is a four-step process to covering your tracks by tamping with logs that hackers know like the back of their hand. These steps are:
<br>
<ol>
  <li> Disable auditing </li> 
  <li> Clearing logs </li>
  <li> Modifying logs </li>
  <li> Erasing command history </li>
<ol>
<br>
  
#### 1. Disable auditing
  
Disable auditing is a smart first step for hackers because if logging is turned off, there will be no trail of evidence. 
<br>
In Windows systems, hackers can use the command line favorite, Auditpol, which will not only allow the hacker to disable auditing but will also allow the hacker to see the level of logging that the organization’s system administrator has set. Knowing this will help the hacker see what is logged. This is important because when possible, hackers like to turn off or alter only the logging that captured their activity — making them harder to track.
<br>
<br>
  
#### 2. Clearing logs
  
Since logs preserve the evidence trail of hacking activities, clearing logs is the logical next step for ethical hackers to know about. 
<br>
How to clear logs in Windows
There are a few ways to clear logs in Windows systems. Presented below are the top methods for performing this track-clearing tactic.
<br>
  
##### Clearlogs.exe
  
One way is to use the clearlogs.exe file, which can be found here. Once access to the target Windows system is obtained, the file needs to be installed and then run to clear the security logs. To run the file, enter the following into a command line prompt:
<br>
clearlogs.exe -sec
<br>
This will clear security logs on the target system. To verify if it has worked, open Event Viewer and check the security logs. Voila! 
<br>
Please note — if the hacker does not remove clearlogs.exe, it will serve as hard evidence of log tampering. If this occurs in a Windows 10 system or Windows Server 2016, event ID 1102(S) will be displayed as an event, and overlooking this is a common error many beginner hackers make. 
<br>
  
##### Meterpreter
  
Originally created by Metasploit and Matt “Skape” Miller in 2004, this advanced payload is a type of shell that, without getting too technical, will help to clear all logs in a Windows system in newer versions of Meterpreter. After compromising the system with Metasploit, use a Meterpreter command prompt and enter the following command:
<br>
Meterpreter > clearev
<br>
This will present the ethical hacker with a window stating that all of the security, application and system logs have been cleared. 
<br>
  
##### Windows Event Viewer
  
Even if auditing has been disabled, it is still smart to clear logs in Windows Event Viewer because actions like disabling auditing will display as an event. To perform this simple task, first navigate to Event Viewer under Windows Logs in the folder tree. In the left-hand pane, right-click on the type of logs you want to clear and select Clear All Events. Boom! Done. 
<br>
  
##### Linux systems
  
Linux systems have their own process of log clearing. To perform this, you want to use the Shred tool. To shred and erase the log file on the target system, run the following bash command:
<br>
Shred -vfzu auth.log
<br>
Just like that, with one command your logged tracks in Linux have been wiped out.
<br>
<br>
  
#### 3. Modifying logs
  
Knowing is half the battle, and knowing where the logs are in your target system is crucial for any hacker.
<br>
Being that you are an ethical hacker working on behalf of your organization, you will already know their location. Inexperienced hackers may not, causing wasted time and an increased chance of detection. In some cases, a text editor may be needed to modify logs; regardless, it as easy as modifying a Word file.
<br>
<br>
  
#### 4. Deleting commands
  
The thing with bash is that it retains the history of entered bash commands, so unless you clear it, the administrator will be able to see that the Shred command above was entered. The retained history of bash commands is found in the file ~/.bash_history. 
<br>
sources: https://resources.infosecinstitute.com/topic/ethical-hacking-log-tampering-101/
