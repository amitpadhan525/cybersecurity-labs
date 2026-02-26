# Rootme

> Content extracted from TryHackMe for room: rrootme

## Deploy the machine

Connect to TryHackMe network and deploy the machine. If you don't know how to do this, complete the [OpenVPN room](https://tryhackme.com/room/openvpn) first.

### Questions

- Deploy the machine

---

## Reconnaissance

First, let's get information about the target.

### Questions

- Scan the machine, how many ports are open?
- What version of Apache is running?
- What service is running on port 22?
- Find directories on the web server using the GoBuster tool.
- What is the hidden directory?

---

## Getting a shell

Find a form to upload and get a reverse shell, and find the flag.

### Questions

- user.txt

---

## Privilege escalation

Now that we have a shell, let's escalate our privileges to root.

### Questions

- Search for files with SUID permission, which file is weird?
- Find a form to escalate your privileges.
- root.txt

---

