# Pwnagotchi
A passive, educational Pwnagotchi setup for learning Wi-Fi security and radio protocols — configured for ethical use, with no deauthentication, no cracking, and full compliance with New York State law.
<br>

<img width="1249" height="612" alt="Screenshot 2025-11-09 at 10 17 41 AM" src="https://github.com/user-attachments/assets/e0ebd92b-5112-49b7-8450-219b2db180c0" />

<br>
<br>
<br>


# Project Overview

This repository documents my ethical, passive Pwnagotchi lab setup, created for educational and research purposes.
It explores how Wi-Fi devices communicate, how WPA2 handshakes function, and how passive network monitoring can be used to understand wireless security — without violating privacy or law.

<br>

Active features (deauth, association) are disabled.
The device only listens for public 802.11 management frames (beacons, probes, EAPOLs) broadcast in the open.

<br>
<br>
<br>

# Ethical Scope
 
  - No packet injection, no interference, no credential cracking.
  - Used for learning protocol behavior, radio traffic patterns, and cybersecurity best practices.

<br>
<br>
<br>

# Legal Context

This project was researched under New York State law (NY Penal Law §§156.05, 250.05).
Passive collection of public Wi-Fi metadata — without accessing protected communications — is not criminalized under current statutes.
<br>
<br>
⚠️ Active interference (deauth, cracking, or connecting to unauthorized networks) would be illegal and is explicitly disabled in this configuration.


# Tools Used

	•	Raspberry Pi Zero W
	•	Pwnagotchi (https://github.com/jayofelony/pwnagotchi)
	•	Wireshark for passive packet analysis
	•	macOS Terminal 
