# 🌐 Networking 101 for Cybersecurity – By Gh0stSh3ll 👻

A complete beginner-friendly breakdown of how Wi-Fi, internet, routers, modems, mobile data, and network security work.  
This marks the first steps in my journey to become an **Ethical Hacker & Cybersecurity Expert**.

---

## 🧠 What is a Network?

- A **network** is a group of two or more devices connected to exchange data.
- Examples:  
  - PC connected to printer (wired) → **LAN**  
  - Your laptop + phone + TV using JioFiber Wi-Fi → **Wireless LAN (WLAN)**

---

## 📶 What is Wi-Fi?

- **Wi-Fi** is a wireless method for devices to connect to a **router** using **radio waves** (2.4GHz or 5GHz).
- It doesn’t provide internet by itself.
- It simply gives **access to the router**, which may or may not be connected to the internet.

---

## 🔌 What is a Router vs Modem?

| Device | Function |
|--------|----------|
| **Modem** | Connects to the **ISP** and brings the **internet** into your home |
| **Router** | Creates your **local network (LAN)** and shares the internet with devices |
| **Router + Modem Combo** | Like JioFiber – does both |

---

## 🛜 What is Mobile Data?

- Your phone’s SIM connects to a **cell tower** (wirelessly).
- The tower is connected to the **ISP’s core network**.
- Data travels through **fiber optic cables** to reach the internet.
- Mobile data = **No router needed**.

---

## 🔁 Can LAN exist without Internet?

✅ Yes!

- A **LAN (Local Area Network)** is just a group of connected devices.
- Even without internet, devices can:
  - Share files
  - Play games
  - Print documents
  - Host local servers

---

## 🧠 How to Find Your Local IP?

### Windows:
```bash
ipconfig
```


### 🌐 Visual of the Path:
```plaintext

📱 (Your Phone)
   ↓ (Radio Waves)
📡 Cell Tower
   ↓ (Fiber Optic)
🏢 ISP Core (Jio, Airtel)
   ↓ (Global Internet Backbone)
🖥️ Netflix Server
   ↓ (Back again)
📡 Tower
   ↓ (Radio Waves)
📱 (You get the movie!)
```


# How Mobile Data Works

- 📱 Your phone sends data via **radio waves** to a nearby cell tower
- 🛰️ Tower sends it through **fiber optic cables** to your **ISP (Jio, Airtel)**
- 🌐 ISP routes the data to services like Netflix, Google, etc.
- 🖥️ Servers respond with data (videos, webpages)
- 🔄 The response travels the same route back to your device

✅ It's always a mix of:
- Radio Waves (Wireless)
- Fiber Optic (Physical cables)


# 📦 OSI Model – Explained with Parcel Delivery Analogy

## What is the OSI Model?
A 7-layer model that explains how data travels through a network.

## Analogy: Sending a Parcel

| OSI Layer | Function | Parcel Analogy |
|-----------|----------|----------------|
| 7. Application | User Interface | You write the letter |
| 6. Presentation | Formatting & Encryption | You encrypt the letter |
| 5. Session | Communication Setup | You call your friend, “I'm sending this” |
| 4. Transport | Delivery method & ports | You choose FedEx or regular post |
| 3. Network | Routing (IP Address) | You write the city + pin code |
| 2. Data Link | Local addressing (MAC) | You add building and flat number |
| 1. Physical | Actual transmission | Truck delivers the box physically |

## Mnemonic:
- Top to Bottom: **All People Seem To Need Data Processing**
- Bottom to Top: **Please Do Not Throw Sausage Pizza Away**

## Why It Matters in Cybersecurity:
- Knowing layers helps target/defend specific attack types
- Different tools work at different OSI levels:
  - Wireshark → Layers 2–4
  - nmap → Layer 3–4
  - Burp Suite → Layer 7


# 🕸️ Spider-Man Networking Example (How Web Works in Real Life)

## Scenario:
You're on JioFiber Wi-Fi and open `netflix.com` to watch Spider-Man.

---

## 🧠 Step-by-Step Networking Breakdown:

1. **DNS Lookup**
   - Browser checks cache
   - If not found, queries DNS servers:
     - Root → TLD → Authoritative → IP returned (e.g. `52.26.14.9`)
   - Protocol: UDP
   - Layers: 7 → 1

2. **TCP 3-Way Handshake**
   - Your device sends SYN to Netflix
   - Netflix replies SYN-ACK
   - You reply ACK
   - Protocol: TCP
   - Layer: 4

3. **HTTPS Request**
   - Secure request sent to Netflix server
   - Passes through WAF (Web Application Firewall)
   - Netflix sends back homepage HTML

4. **Watching Spider-Man**
   - Movie is broken into segments → packets → frames
   - Each frame:
     - Layer 2: MAC header
     - Layer 3: IP header
     - Layer 4: TCP header
     - Layer 7: Encrypted video chunks
   - Sent as radio waves over Wi-Fi
   - Received and reassembled to display video

---

## 🧱 OSI Model Used:
1. **Physical** → Wi-Fi radio signals
2. **Data Link** → MAC addresses, frames
3. **Network** → IP routing
4. **Transport** → TCP reliability
5. **Session** → Communication session
6. **Presentation** → TLS/SSL encryption
7. **Application** → DNS, HTTP, Netflix App

---

## 🧵 Real Protocols Involved:
- **DNS** → UDP
- **TCP** → Reliable data delivery
- **IP** → Routing
- **HTTPS** → Secure web
- **MAC** → Local delivery





