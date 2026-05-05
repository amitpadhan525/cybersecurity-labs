# OSI Model Cheat Sheet

## Layer 7: Application
- Job: Provides network services to user applications
- Protocols: HTTP, HTTPS, DNS, FTP, SMTP
- Attack: SQLi, XSS, SSRF

## Layer 6: Presentation
- Job: Changes data format
- Encryption/Decryption
- Data compression

## Layer 5: Session
- Job: Establishes session for communication
- Manages session, dialog control, synchronization, authentication

## Layer 4: Transport
- Job: Responsible for end-to-end communication
- Segmentation: Breaks large data into smaller pieces
- Error detection: Checks errors using checksum
- Protocols: TCP, UDP
- Attack: SYN flood

## Layer 3: Network
- Job: Delivers packets across internet
- Uses IP address for routing
- Attack: IP spoofing

## Layer 2: Data Link
- Job: Node-to-node transfer on local network
- Uses MAC address to identify devices uniquely
- Attack: ARP spoofing

## Layer 1: Physical
- Job: Transmits raw bits on the wire
- Examples: Cables, WiFi signals