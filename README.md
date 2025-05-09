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

---![1000026848](https://github.com/user-attachments/assets/cb180bbe-949a-4f95-a15f-e72d19a22d47)



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

![1000027727](https://github.com/user-attachments/assets/be4bec17-b81c-4611-8e7d-4910d7a9ac17)


# search query example. 

 - note: It's better to use ```Show modules.```
 - because search tplink is broken
 - it just returns autopwn

   ```
   rsf663 > search huawei
   Search results for 'huawei':
   autopwn
   huawei_e5331_info_disclosure
   huawei_hg520_udp_info_disclosure
   huawei_hg530_hg520b_password_disclosure
   huawei_hg532_rce
   huawei_hg866_password_change

   rsf663 >
   ```
   ![1000027728](https://github.com/user-attachments/assets/5863563d-1af0-4795-b907-0af523a13831)



brands / modules
✅ 2Wire
Script	Type	Description
2Wire_4011G_5012NV_Path_Traversal.py	Path Traversal	Exploit directory traversal in 2Wire routers
2Wire_Gateway_Auth_Bypass.py	Auth Bypass	Bypass gateway authentication

✅ 3Com
Script	Type
3Com_IMC_info_disclosure.py	Info Disclosure
3Com_IMC_path_traversal.py	Path Traversal
3Com_OfficeConnect_info_disclosure.py	Info Disclosure
3Com_OfficeConnect_rce.py	RCE
3Com_ap8760_password_disclosure.py	Password Disclosure

✅ Asmax
Script	Type
Asmax_AR1004G_password_disclosure.py	Password Disclosure
Asmax_AR804_RCE.py	RCE

✅ BHU
Script	Type
BHU_uRouter_RCE.py	RCE

✅ Billion
Script	Type
Billion_5200W_T_RCE.py	RCE
Billion_7700NR4_Password_Disclosure.py	Password Disclosure

✅ Comtrend
Script	Type
Comtrend_CT_5361T_Password_Disclosure.py	Password Disclosure

✅ D-Link
Script	Type
D-Link_DCS-930L_Auth_RCE.py	RCE/Auth
D-Link_DGS-1510_Add_User.py	Privilege Escalation
D-Link_DIR-300_320_600_Info_Disclosure.py	Info Disclosure
D-Link_DIR-300_320_615_Auth_Bypass.py	Auth Bypass
D-Link_DIR-300_600_RCE.py	RCE
D-Link_DIR-300_DIR-645_DIR-815_UPNP_RCE.py	RCE
D-Link_DIR-645_DIR-815_RCE.py	RCE
D-Link_DIR-645_password_disclosure.py	Password Disclosure
D-Link_DIR-815_850L_RCE.py	RCE
D-Link_DIR-825_path_traversal.py	Path Traversal
D-Link_DIR-850L_creds_disclosure.py	Credential Disclosure
D-Link_DSL-2640B_DNS_change.py	DNS Change
D-Link_DSL-2730U_path_traversal.py	Path Traversal
D-Link_DSL-2740R_DNS_change.py	DNS Change
D-Link_DSL-2750B_RCE.py	RCE
D-Link_DSL-2750B_info_disclosure.py	Info Disclosure
D-Link_DSL-2780B_DNS_change.py	DNS Change
D-Link_DSP-W110_RCE.py	RCE
D-Link_PingTest_RCE.py	RCE

✅ IPFire
Script	Type
IPFire_Oinkcode_RCE.py	RCE
IPFire_Proxy_RCE.py	RCE
IPFire_Shellshock.py	Shellshock (RCE)

✅ LG
Script	Type
LG_NAS_3718.510.a0_RCE.py	RCE

✅ Linksys
Script	Type
Linksys_E1500_E2500_RCE.py	RCE
Linksys_E_Series_TheMoon_RCE.py	RCE (TheMoon Worm)
Linksys_SMART_WiFi_Password_Disclosure.py	Password Disclosure
Linksys_WAP54Gv3_RCE.py	RCE
Linksys_WRT100_WRT110_RCE.py	RCE

✅ Mikrotik
Script	Type
Mikrotik_RouterOS_Jailbreak.py	Privilege Escalation
Mikrotik_WinBox_Auth_Bypass_Creds_Disclosure.py	Auth Bypass + Cred Disclosure

✅ Movistar
Script	Type
Movistar_adsl_router_bhs_rta_path_traversal.py	Path Traversal

✅ Netcore / Netis
Script	Type
Netcore_Netis_UDP_53413_RCE.py	RCE

✅ Netsys
Script	Type
Netsys_multi_rce.py	RCE

✅ Shuttle
Script	Type
Shuttle_915WM_dns_change.py	DNS Change

✅ ZTE
Script	Type
ZTE_F460_F660_Backdoor_RCE.py	RCE
ZTE_ZXHN_H108N_Wifi_Password_Disclosure.py	Password Disclosure
ZTE_ZXV10_RCE.py	RCE

✅ Zyxel
Script	Type
Zyxel_Eir_D1000_RCE.py	RCE
Zyxel_Eir_D1000_WiFi_Password_Disclosure.py	Password Disclosure
Zyxel_P660HN_T_v1_RCE.py	RCE
Zyxel_P660HN_T_v2_RCE.py	RCE
Zyxel_ZyWALL_USG_Extract_Hashes.py	Hash Extraction

✅ AirOS (Ubiquiti)
Script	Type
airos_6x_arbitrary_file_upload.py	File Upload (RCE)

✅ Asus
Script	Type
asus_infosvr_rce.py	RCE
asus_password_disclosure.py	Password Disclosure
asuswrt_lan_rce.py	RCE

✅ Belkin
Script	Type
belkin_auth_bypass.py	Auth Bypass
belkin_g_info_disclosure.py	Info Disclosure
belkin_g_n150_password_disclosure.py	Password Disclosure
belkin_n150_path_traversal.py	Path Traversal
belkin_n750_rce.py	RCE
belkin_play_max_persistent_rce.py	RCE

✅ Cisco
Script	Type
cisco_catalyst_2960_rocem_rce.py	RCE
cisco_dpc2420_info_disclosure.py	Info Disclosure
cisco_firepower_management_path_traversal.py	Path Traversal
cisco_firepower_management_rce.py	RCE
cisco_ios_http_unauth_access.py	Unauthorized Access
cisco_rv320_command_injection.py	Command Injection
cisco_secure_acs_password_change.py	Password Change
cisco_ucm_info_disclosure.py	Info Disclosure
cisco_ucs_manager_rce.py	RCE
cisco_unified_multi_path_traversal.py	Path Traversal

✅ Huawei
Script	Type
huawei_e5331_info_disclosure.py	Info Disclosure
huawei_hg520_udp_info_disclosure.py	Info Disclosure
huawei_hg530_hg520b_password_disclosure.py	Password Disclosure
huawei_hg532_rce.py	RCE
huawei_hg866_password_change.py	Password Change

✅ Netgear
Script	Type
netgear_dgn2200_dnslookup_rce.py	RCE
netgear_dgn2200_ping_rce.py	RCE
netgear_jnr1010_path_traversal.py	Path Traversal
netgear_multi_password_disclosure.py	Password Disclosure
netgear_multi_rce.py	RCE
netgear_n300_auth_bypass.py	Auth Bypass
netgear_prosafe_rce.py	RCE
netgear_r7000_r6400_rce.py	RCE
netgear_rax30_rce.py	RCE
netgear_wnr_path_traversal.py	Path Traversal

✅ Technicolor
Script	Type
technicolor_dwg855_auth_bypass.py	Auth Bypass
technicolor_tc7200_password_disclosure.py	Password Disclosure
technicolor_tc7200_password_disclosure_v2.py	Password Disclosure
technicolor_tg784n_v3_auth_bypass.py	Auth Bypass

✅ Thomson
Script	Type
thomson_twg849_info_disclosure.py	Info Disclosure
thomson_twg850_password_disclosure.py	Password Disclosure

✅ TP-Link
Script	Type
tplink_archer_c2_c20i_rce.py	RCE
tplink_archer_c9_password_reset.py	Password Reset
tplink_wdr740nd_backdoor_rce.py	RCE
tplink_wdr740nd_path_traversal.py	Path Traversal
tplink_wdr842nd_configure_disclosure.py	Info Disclosure

Other Files
Filename	         Description
autopwn.py	  Likely auto-exploit framework
dlink_scanner.py	  Scanner for D-Link targets
proxy.txt. 	 contains proxy list
useragents.txt	contains User-Agent strings


![1000026924](https://github.com/user-attachments/assets/eff47cdd-cdf2-403d-b20c-979ce6d20c26)

   
