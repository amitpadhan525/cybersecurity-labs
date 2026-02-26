# Blue

> Content extracted from TryHackMe for room: blue

## Recon

Press the **Start Machine** button below.





Start the AttackBox by pressing the **Start AttackBox** button at the top of this page. The AttackBox machine will start in Split-Screen view. If it is not visible, use the blue **Show Split View** button at the top of the page.



Scan and learn what exploit this machine is vulnerable to. Please note that this machine does not respond to ping (ICMP) and may take a few minutes to boot up. **This room is not meant to be a boot2root CTF, rather, this is an educational series for complete beginners. Professionals will likely get very little out of this room beyond basic practice as the process here is meant to be beginner-focused. ****
****
**_Art by one of our members, Varg - [THM Profile](https://tryhackme.com/p/Varg) - [Instagram](https://www.instagram.com/varghalladesign/) - [Blue Merch](https://www.redbubble.com/shop/ap/53637482) - [Twitter](https://twitter.com/Vargnaar)_
_Link to Ice, the sequel to Blue: [Link](https://tryhackme.com/room/ice)__You can check out the third box in this series, Blaster, here: [Link](https://tryhackme.com/room/blaster)_-----------------------------------------
The virtual machine used in this room (Blue) can be downloaded for offline usage from [https://darkstar7471.com/resources.html](https://darkstar7471.com/resources.html)[](https://darkstar7471.com/resources.html)
_Enjoy the room! For future rooms and write-ups, follow [@darkstar7471](https://twitter.com/darkstar7471) on Twitter._

### Questions

- Scan the machine. (If you are unsure how to tackle this, I recommend checking out the [Nmap](https://tryhackme.com/room/furthernmap) room)
- How many ports are open with a port number under 1000?
- What is this machine vulnerable to? (Answer in the form of: ms??-???, ex: ms08-067)

---

## Gain Access

Exploit the machine and gain a foothold.

### Questions

- Start [Metasploit](https://tryhackme.com/module/metasploit)
- Find the exploitation code we will run against the machine. What is the full path of the code? (Ex: exploit/........)
- Show options and set the one required value. What is the name of this value? (All caps for submission)
- Usually it would be fine to run this exploit as is; however, for the sake of learning, you should do one more thing before exploiting the target. Enter the following command and press enter:

set payload windows/x64/shell/reverse_tcp

With that done, run the exploit!
- Confirm that the exploit has run correctly. You may have to press enter for the DOS shell to appear. Background this shell (CTRL + Z). If this failed, you may have to reboot the target VM. Try running it again before a reboot of the target.

---

## Escalate

Escalate privileges, learn how to upgrade shells in metasploit.

### Questions

- If you haven't already, background the previously gained shell (CTRL + Z). Research online how to convert a shell to meterpreter shell in metasploit. What is the name of the post module we will use? (Exact path, similar to the exploit we previously selected)
- Select this (use MODULE_PATH). Show options, what option are we required to change?
- Set the required option, you may need to list all of the sessions to find your target here.
- Run! If this doesn't work, try completing the exploit from the previous task once more.
- Once the meterpreter shell conversion completes, select that session for use.
- Verify that we have escalated to NT AUTHORITY\SYSTEM. Run getsystem to confirm this. Feel free to open a dos shell via the command 'shell' and run 'whoami'. This should return that we are indeed system. Background this shell afterwards and select our meterpreter session for usage again.
- List all of the processes running via the 'ps' command. Just because we are system doesn't mean our process is. Find a process towards the bottom of this list that is running at NT AUTHORITY\SYSTEM and write down the process id (far left column).
- Migrate to this process using the 'migrate PROCESS_ID' command where the process id is the one you just wrote down in the previous step. This may take several attempts, migrating processes is not very stable. If this fails, you may need to re-run the conversion process or reboot the machine and start once again. If this happens, try a different process next time.

---

## Cracking

Dump the non-default user's password and crack it!

### Questions

- Within our elevated meterpreter shell, run the command 'hashdump'. This will dump all of the passwords on the machine as long as we have the correct privileges to do so. What is the name of the non-default user?
- Copy this password hash to a file and research how to crack it. What is the cracked password?

---

## Find flags!

Find the three flags planted on this machine. These are not traditional flags, rather, they're meant to represent key locations within the Windows system. Use the hints provided below to complete this room!
-----------------------------------------------------------------
_Completed Blue? Check out Ice: [Link](https://tryhackme.com/room/ice)__You can check out the third box in this series, Blaster, here: [Link](https://tryhackme.com/room/blaster)_

### Questions

- Flag1? _This flag can be found at the system root. _
- Flag2? _This flag can be found at the location where passwords are stored within Windows._




*Errata: Windows really doesn't like the location of this flag and can occasionally delete it. It may be necessary in some cases to terminate/restart the machine and rerun the exploit to find this flag. This relatively rare, however, it can happen.
- flag3? _This flag can be found in an excellent location to loot. After all, Administrators usually have pretty interesting things saved. _

---

