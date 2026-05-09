# Port Reference Cheat Sheet

## Well-Known Ports (0–1023)

### File Transfer
- 20: FTP data
- 21: FTP control
- 22: SSH / SFTP

### Email
- 25: SMTP
- 110: POP3
- 143: IMAP

### Web
- 80: HTTP
- 443: HTTPS
- 8080: HTTP alternate

### Name Resolution
- 53: DNS (UDP for queries, TCP for zone transfers)

### Remote Access
- 23: Telnet (cleartext — never use)
- 3389: RDP (Windows)

### File Sharing
- 445: SMB
- 139: NetBIOS

### Databases
- 1433: MSSQL
- 3306: MySQL
- 5432: PostgreSQL
- 27017: MongoDB

## Attack Surface Notes
- Port 23 open = likely default creds, cleartext traffic
- Port 445 open = check for EternalBlue (MS17-010)
- Port 3389 open = RDP brute force vector
- Port 21 open = check anonymous FTP login