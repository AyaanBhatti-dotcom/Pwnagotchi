# Legal Summary: Passive Pwnagotchi Use in NYC / New York State

## ❗ Bottom Line

> **Passive-only use** of a Pwnagotchi (listening for publicly broadcast Wi-Fi management frames such as SSIDs, BSSIDs, beacons, probe requests, and observing but not decrypting handshakes) **is generally lawful in New York.**

The risky/illegal actions are the ones that go **beyond** passive listening:
* Active interference (deauthentication/jamming).
* Unauthorized access (cracking/connecting to networks you don’t own).
* Intercepting the *contents* of private communications.

---

## ✅ Why Passive Listening is Generally OK

* **NY computer-crime law** targets **unauthorized access** or knowingly circumventing security protections (i.e., hacking into a system). Simply hearing broadcast radio frames does not equal "accessing" a computer or network.
* **NY eavesdropping/wiretap rules** exclude communications that are **readily accessible to the general public**. Wi-Fi beacon frames and SSID/BSSID broadcasts are public by design, so merely collecting that metadata is not the same as intercepting private communications.

---

## 🚫 What Would Likely Be Illegal

* **Active Attacks:** Deauthentication/jamming or packet injection may violate FCC rules and state law.
* **Cracking or Using Handshakes:** Capturing handshake data to gain access to networks you don’t own could be considered unauthorized access under NY Penal Law.
* **Capturing Private Data:** Capturing and storing/reading the *contents* of private communications (e.g., decrypted payloads, private messages) without consent is likely illegal under eavesdropping laws.

---

## 🛠️ Practical, Safety-First Checklist

Here is what to do to stay legal and ethical:

* Keep deauthentication disabled: `personality.deauth = false`
* Do not store or publish any captured private data or PCAPs that include user traffic.

---

## ⚖️ Disclaimer

Laws are subject to interpretation and can vary by state and circumstance. Regulators (FCC) and institutional policies (school, employer, ISP) also matter.

**This is not legal advice.** If you need a definitive legal opinion—for example, before doing anything borderline—consult a licensed attorney.
