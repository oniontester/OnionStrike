# 🧅 OnionStrike v0.1

**OnionStrike** is a modular, Tor-based botnet command-and-control (C2) framework designed for **educational and red teaming purposes**. It allows secure and anonymous management of remote agents capable of executing stress-test (DDoS) tasks against `.onion` targets.

> ⚠️ This tool is intended strictly for ethical use within controlled environments such as labs, research, and authorized penetration testing.

---

## 🎯 Key Features

- 🧠 **Tor Integration** – All agent communication is routed through the Tor network using SOCKS5 proxies, ensuring strong anonymity.
- 🖥️ **Modern TUI Controller** – Built with `rich`, the terminal interface includes animations, tables, and prompts.
- 🤖 **Agent Management** – Real-time tracking of connected agents with live socket monitoring.
- 🧩 **Job Dispatch System** – Send DDoS tasks with customizable parameters (target, thread count, duration, attack mode).
- 🔧 **Cross-Platform Agent Support** – Linux and Windows (x86 & x64), with automatic Tor installation on client systems.
- 🧱 **Extensible Design** – Future-proof architecture with planned modules for builder, persistence, result logging, and evasion techniques.

---

## 🧪 How It Works (Overview)

1. **Controller** listens for agent connections via TCP.
2. **Agents** download and install Tor (if not found), then tunnel traffic to the C2 using SOCKS5.
3. The operator launches jobs from the controller, which are broadcasted to all connected agents.
4. Each agent executes the task and (optionally) returns results (not yet implemented).

This architecture models how real-world botnets anonymize control channels, and how they can coordinate synchronized attacks over dark web infrastructure.

---

## 🧰 Installation

### Controller (C2)
```bash
git clone https://github.com/yourname/onionstrike.git
cd onionstrike
python3 -m pip install -r requirements.txt
python3 src/main.py
````

### Agent

Supports both Windows and Linux. Build or distribute the client (build tool coming soon).

---

## 🎬 Demo

Watch the full walkthrough and demo here:
📺 [https://www.youtube.com/watch?v=OxIRaUSdu7E](https://www.youtube.com/watch?v=OxIRaUSdu7E)

---

## 📚 Educational Use Cases

* Simulate DDoS scenarios in a private lab.
* Teach operational security around botnets.
* Red team practice in dark web-style infrastructure.
* Analyze the limitations of PoW and CAPTCHA-based protections under load.

---

## 📌 Roadmap

* [x] Basic socket communication
* [x] Tor integration
* [x] Animated TUI with `rich`
* [x] Job dispatcher with tracking
* [ ] Agent builder with config
* [ ] Job result collection
* [ ] Persistence mechanism

---

## ❗ Disclaimer

This software is provided **for academic and legal research purposes only**.
You must not use it to attack any target you do not have explicit permission to test.
The developer assumes **no liability** for misuse of this code.

---

## 🧷 Contact & Feedback

Have ideas or want to collaborate? Reach out:

* XMPP / Signal preferred
* No Telegram support

---

## 🏷️ Tags

`#python` `#botnet` `#ddos` `#tor` `#ddos` `#redteam` `#cybersecurity` `#onion` `#c2`


