# Day 5 – WEP Cracking

📚 **Completed:** Section 6 of Zaid’s Ethical Hacking Course  
🎯 **Topic:** WEP Cracking (Pre-Shared Key Attacks on Wi-Fi)

## 🧠 What I Learned:
- **WEP (Wired Equivalent Privacy)** is an outdated encryption protocol used in Wi-Fi security.
- It uses weak **RC4 encryption**, which is vulnerable due to **static keys** and **predictable IVs (Initialization Vectors)**.
- WEP networks can be cracked by capturing enough data packets and using tools to analyze them.
- 
## 🛠️ Tools Used in Theory:
| Tool | Purpose |
|------|---------|
| `airmon-ng` | Enables monitor mode on wireless interface |
| `airodump-ng` | Captures packets & identifies WEP networks |
| `aireplay-ng` | Injects fake packets (ARP replay) to speed up capture |
| `aircrack-ng` | Cracks the WEP key from captured `.cap` files |

## 🔐 Steps (Theory Only):
1. **Enable Monitor Mode:**
2. airmon-ng start wlan0
3. **Capture Packets:**
4. airodump-ng wlan0mon
airodump-ng -c [channel] --bssid [target_BSSID] -w capture wlan0mon
3. **Fake Authentication & ARP Injection:**
aireplay-ng -1 0 -a [BSSID] wlan0mon
aireplay-ng -3 -b [BSSID] wlan0mon
4. **Crack WEP Key:**
aircrack-ng capture-01.cap

## 🖼️ Screenshot:
_N/A – No wireless adapter available for practice._

## 🧩 Summary:
Even though I couldn’t practice the commands, I understood the **full WEP cracking workflow**, its tools, and the **vulnerability** that makes WEP insecure.  
This forms the **base for real-world Wi-Fi attacks** later.




