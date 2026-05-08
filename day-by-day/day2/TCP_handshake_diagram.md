# TCP 3-Way Handshake — Day 2 Notes

## The Handshake
Client          Server
  |--- SYN (seq=x) -------->|
  |<-- SYN-ACK (seq=y, ack=x+1) --|
  |--- ACK (ack=y+1) ------->|
  [connection established]

## What I saw in Wireshark today
- Client ISN: [paste the actual number from your capture]
- Server ISN: [paste it]
- RTT (time between SYN and SYN-ACK): [note the delta]

## The FIN Teardown
[draw it yourself here]

## RST — what it looks like
[note what triggered it and what Wireshark showed]

## Why this matters for attacks
- SYN flood: exhaust server connection table with half-open connections
- TCP session hijacking: predict sequence numbers to inject packets mid-stream
- RST injection: forge RST packets to kill connections (used in censorship + DoS)