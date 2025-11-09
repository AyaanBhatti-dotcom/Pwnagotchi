# How to Install

* Check out the tools in the readme.
* This guide uses a **Raspberry Pi Zero 2 W**.
* Many people choose to make it portable by buying a screen and battery, but for our purposes, we’ll simply be using the web UI.
* The Pi image from the official website may not work with the Pi Zero 2 W. This guide uses an image from: [https://github.com/jayofelony/pwnagotchi](https://github.com/jayofelony/pwnagotchi)
* Use the Raspberry Pi Imager to flash this image onto a micro SD card (preferably 8GB or higher).

## ❗ VERY IMPORTANT!!

> **Once it’s installed, you MUST make a file called `config.toml`.**
> (You can find an example in my repo within the `config` directory).
>
> This file is used to **disable any deauthentication**, making the device passive and legal to operate in most public spaces.

* Once this is done, I used a Mac to access the web UI.
* It takes a few minutes for the Pi to boot and create a network connection with your Mac. Once it’s connected, be sure to change the IP to a static address as well as the DNS.
* If your static IP was `10.0.0.1`, you can navigate to `http://10.0.0.2:8080` on your browser.
* Congrats! You now have a working Pwnagotchi.


![IMG_0098](https://github.com/user-attachments/assets/4f756da1-0630-49cc-83f4-d66b022cc64b)

# What Does It Do?

This video explains it very well: [https://www.youtube.com/watch?v=puOkriFPVtQ](https://www.youtube.com/watch?v=puOkriFPVtQ)

* When a device and an access point establish a connection, they send special data packets called handshakes using WPA2 encryption.
* Let’s say you’re connecting your phone to a Wi-Fi network. Before your phone can connect, the WPA encryption keys have to be generated.
* This is when 4 packets are exchanged between the two devices (a 4-way handshake).
* These packets can be used to derive session keys.
* When the packets are successfully exchanged, your phone (or any client device) is authenticated and can begin to send and receive encrypted data.
* The WPA handshake is contained within the second handshake packet, but its content is hashed.
* The Pwnagotchi simply intercepts these packets and stores them.
* These `.pcap` files are stored with the hashed encryptions, but they can be decrypted using special tools and dictionaries.

# How Does It Collect Handshakes?

### Deauthentication (Active Attack)

The main way it collects handshakes is via deauthentication.

> **⚠️ THIS CAN BE ILLEGAL.** Please only do this on your own network if you choose to do so.

The Pwnagotchi sends a disconnect signal to the client device, so it has to reconnect. When it does, it has to go through the 4-way handshake again, but this time the Pwnagotchi intercepts and saves the packets.

### Other Method (Passive / Association)

Another method involves sending association frames directly to the access points themselves to try to force them to leak the PMKID.
