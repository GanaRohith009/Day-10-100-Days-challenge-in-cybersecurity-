# Day-10-100-Days-challenge-in-cybersecurity-
# Day 10: Network Anonymity - Proxies & VPNs

**Date:** January 6, 2026
**Topic:** Networking / Anonymity / OPSEC

## 📝 Overview
On Day 10, I focused on the technologies used to mask digital identity. Understanding how traffic is obfuscated is crucial for both offensive operations (evasion) and defensive operations (investigation/intelligence gathering).

## 🧠 Key Concepts Learned

### 1. Proxy vs. VPN
While both mask the IP address, their operation impacts security differently:
* **Proxy (The Middleman):** Acts as a gateway. It handles the request on your behalf.
    * *Limitation:* Often only handles HTTP/HTTPS traffic and does not encrypt the tunnel.
* **VPN (The Armored Tunnel):** Creates a virtual point-to-point connection.
    * *Advantage:* Encrypts all network traffic (not just browser-based) between the device and the exit node.

### 2. The Duality of Use

| Role | Usage | Goal |
| :--- | :--- | :--- |
| **Attacker** | **Obfuscation & Evasion** | To hide the true source IP to prevent law enforcement from tracing the attack back to a physical location. Uses techniques like **Proxy Chaining**. |
| **Investigator** | **OPSEC (Operational Security)** | To prevent the **"Watcher Effect."** If an investigator visits a malicious site directly, the server logs reveal their identity. VPNs allow for "Sandboxed" investigation. |

## 🛡️ Technical Insight: Proxy Chaining
Attackers rarely use a single hop. They chain proxies to complicate the tracing process.
* *Concept:* User -> Proxy A (Russia) -> Proxy B (Brazil) -> Proxy C (France) -> Target.
* *Result:* The target sees the request coming from France. If logs in France are seized, they point to Brazil, and so on.

## 📌 Conclusion
"Attribution" (identifying who is behind an attack) is the most difficult task in cybersecurity because of these tools. Mastering them is essential for understanding the cat-and-mouse game of digital warfare.

---
*Part of the 100 Days of Cybersecurity Challenge.*
