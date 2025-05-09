# RSF - Router Exploit Framework v6.6.3


> 📡 **RSF** is a modular router exploitation framework built to scan, exploit, brute-force, and interact with vulnerable routers across a wide range of vendors. Inspired by Metasploit and RouterSploit
---

## 🚀 Features

- 🔎 **Automatic Module Discovery**  
- 📜 **103+ Exploit Modules** included (command exec, backdoors, misconfigs, info leaks)
- 🧠 **Intelligent Search & Targeting**  
- 🗃️ Built-in **wordlist support** (auto-detected per module)  
- ⚙️ Interactive CLI with `use`, `info`, `options`, `run` workflow , etc
- 🧪 Supports *blind* injections with clear output warnings  
- ✍️ Fully scriptable for red teaming automation  
- 💻 Works on Kali, parrot OS, nethunter terminal

---
<img src="https://imgur.com/a/VNgc1Lg.png" width="300">


# PLEASE NOTE THAT MOST OF THE MODULES ARE BLIND.

## 🧰 Installation

```bash
git clone https://github.com/ediop3SquadALT/rsf663
cd rsf663
unzip rsf663.zip
cd rsf663
chmod +x rsf663.sh
pip3 install -r requirements.txt
sudo bash rsf663.sh
```

# Example usage
 ```
rsf663 > show modules
rsf663 > use huawei_hg532_rce
Using module huawei_hg532_rce
Module information:
  Name: huawei_hg532_rce
  Description: Module exploits remote command execution in Huawei Router HG532 devices.

rsf663 > set target 192.168.1.248
Target set to 192.168.1.248
rsf663 (192.168.1.248:huawei_hg532_rce) > run
[*] Waiting 4 seconds for module to load properly...
[*] Running vulnerability check...
[-] NOT VULNERABLE: Target does not appear to be vulnerable to huawei_hg532_rce
[*] Module output: 

rsf663 (192.168.1.248:huawei_hg532_rce) >
```

