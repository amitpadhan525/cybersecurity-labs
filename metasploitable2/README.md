# Metasploitable 2 Labs

This folder contains hands-on exploitation notes and walkthroughs targeting [Metasploitable 2](https://sourceforge.net/projects/metasploitable/) — an intentionally vulnerable Linux virtual machine designed for practicing penetration testing techniques in a safe, legal environment.

## What is Metasploitable 2?

Metasploitable 2 is an intentionally insecure Linux virtual machine created by Rapid7. It is packed with numerous deliberately vulnerable services, misconfigurations, and weak credentials, making it an ideal target for learning offensive security skills without any legal or ethical risk.

## Labs

| File | Service / Topic | Difficulty |
|------|----------------|------------|
| [telnet-exploitation.md](./telnet-exploitation.md) | Telnet (Port 23) — Credential abuse, privilege escalation & backdoor creation | Beginner |

## Setup

1. Download Metasploitable 2 from [SourceForge](https://sourceforge.net/projects/metasploitable/).
2. Import the `.vmdk` into VirtualBox or VMware.
3. Set the network adapter to **Host-Only** or **NAT** so the VM is isolated from the internet.
4. Boot the VM — default credentials are `msfadmin` / `msfadmin`.
5. Use `ifconfig` inside the VM (or an Nmap scan from your attack machine) to discover its IP address.

> [!WARNING]
> **Never** expose Metasploitable 2 directly to the internet. It is intentionally vulnerable and will be compromised immediately if publicly reachable.

---

*Authored by Amit Padhan*
